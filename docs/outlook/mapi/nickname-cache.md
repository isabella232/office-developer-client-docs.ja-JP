---
title: ニックネームのキャッシュ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2813c102-6778-4443-ab4b-b573f3568705
description: '最終更新日: 2013 年 1 月 30 日'
ms.openlocfilehash: 1ea1d3e6f636cf6a3ad47b6fdfe88d0f7130a5f3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801661"
---
# <a name="nickname-cache"></a>ニックネームのキャッシュ

 
  
**適用されます**: Outlook 
  
Microsoft Office Outlook 2007、Microsoft Outlook 2010 では、および Microsoft Outlook 2013 の対話、ニックネームのキャッシュとも呼ばれる「オートコンプリートのストリーム。」 オートコンプリートのストリームでは、Outlook には、オートコンプリートの一覧**に** **[cc]**、[表示名のリストが引き続き発生して、ユーザーが電子メールを作成するときに、 **[Bcc** ] ボックス。 このトピックでは、Outlook 2007 と Outlook 2010、Outlook 2013 がオートコンプリートのストリームとどのようにやり取りする方法について説明し、オートコンプリートのストリームと対話するための推奨される方法と、ファイルのバイナリ形式についても説明します。 
  
Outlook 2010 または Outlook 2013 とやり取りするアプリケーションの場合は、オートコンプリートのストリームが MAPI プロパティとして格納されているし、MAPI またはメッセージの**PropertyAccessor**オブジェクトを使用して変更することができます。 **PropertyAccessor**オブジェクトは、Outlook 2010 または Outlook 2013 オブジェクト モデルで公開されます。 
  
Outlook 2007 オブジェクト モデルまたは MAPI Api への依存関係はありません。 したがって、Outlook 2007 のオートコンプリートのストリームを変更するアプリケーションは、任意のプログラミング言語を使用して記述できます。
  
## <a name="interacting-with-the-autocomplete-stream"></a>オートコンプリートのストリームを操作します。

メッセージでアクセスすると、**宛先**、 **Cc**、または [ **Bcc**のエディット ボックスのように、オートコンプリートのストリームが読み込まれ、ユーザー名の一覧が表示されます。 Outlook は、2 つの方法でオートコンプリート ストリームと対話します。 
  
1. オートコンプリートのストリームの読み込み 
    
2. オートコンプリートのストリーム内のデータに変更を保存します。
    
オートコンプリートのデータを格納するための手段は、次のように Outlook 2007 および Outlook 2010 または Outlook 2013 の間で異なります。 
  
 **Outlook 2007**
  
Outlook 2007 では、オートコンプリートのストリームは、同じ名前のプロファイルと .nk2 という拡張子を持つファイルに格納されます。 たとえば、"outlook"の既定のプロファイルを使用する場合、"outlook.nk2"にファイルが呼び出されます。 .Nk2 ファイルは、%appdata%\microsoft\outlook に格納されます。 ニックネーム キャッシュのバイナリ ファイル形式の詳細については、 [Outlook 2003/2007 NK2 ファイル形式と開発者のガイドライン](http://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)を参照してください。
  
 **Outlook 2010、Outlook 2013**
  
Outlook 2010 または Outlook 2013 は、メール アカウントの配信ストアの受信トレイの内容を関連付けられているテーブル内のメッセージからオートコンプリートのストリームを読み取ります。 この隠しメッセージがあり、メッセージ クラス IPM の件名です。Configuration.Autocomplete。 オートコンプリートのストリームは、PR_ROAMING_BINARYSTREAM プロパティ ([PidTagRoamingBinary の標準的なプロパティ](pidtagroamingbinary-canonical-property.md)) では、このメッセージに格納されます。 %Userprofile%\appdata\local\microsoft\outlook\roamcache 内にある、オートコンプリートの .dat ファイルで、オートコンプリートのデータを一時的にキャッシュ可能性があります。 ただし、.dat ファイルはキャッシュのみであり、Outlook 2010 または Outlook 2013 を終了するとき、配信ストアへの書き戻しには使われません。
  
## <a name="loading-the-autocomplete-stream"></a>オートコンプリートのストリームの読み込み

Outlook は、アドレス指定機能を持つ項目が初期化されるたびに、オートコンプリートのストリームを読み込みます。 たとえば、電子メール アドレスは、新着メール、メールの返信、連絡先アイテム、会議出席依頼、およびなどで使用されます。 データを読み込むには、Outlook は、すべてのストリームの内容をメモリに読み込みます。
  
オートコンプリート機能の操作を Outlook はこのメモリ内の構造体だけを outlook.exe プロセスの有効期間の間に対話します。 Outlook はシャット ダウン時にのみ、構造を保存します。 このプロセスの詳細については、次のセクション「[オートコンプリート ストリームを保存」を参照してください。
  
## <a name="saving-the-autocomplete-stream"></a>オートコンプリートのストリームを保存します。

オートコンプリート リストは、次の方法のいずれかで変更された場合、outlook はシャット ダウン時にオートコンプリートのストリームを保存します。
  
- 名前を解決する、アドレス帳ダイアログ ボックスで、受信者を選択、またはまだリストされていない受信者にメールを送信することによって、新しいニックネーム エントリが追加されます。
    
- エントリを変更するには、リスト内の既存の受信者にメールを送信します。
    
- UI を通じてユーザーが、エントリが削除されます。
    
- このトピックに関係のない小さなシナリオです。
    
オートコンプリートのデータに変更を保存するには、[オートコンプリートのストリーム](autocomplete-stream.md)にメモリ内構造の書き戻しが含まれます。 Outlook 2007 との対話、ストリームは、ローカル .nk2 ファイルに保存されます。 Outlook 2010 または Outlook 2013 では、オートコンプリートのストリームに書き込みます、メール アカウントの配信ストアの受信トレイの内容を関連付けられているテーブル。
  
## <a name="recommendations"></a>推奨事項

- 決して部分的にオートコンプリートのストリームを変更します。 1) 全体のオートコンプリートのストリームをメモリに読み込む、2) 構造を変更、メモリ、および 3) 全体のストリームに書き込みますか、メール アカウントの配信ストアの受信トレイの内容を関連付けられているテーブルには、サポートされている操作 (Outlook 2010 またはOutlook 2013) またはローカル .nk2 ファイル (Outlook 2007)。
    
- 対話せず、オートコンプリート ストリーム Outlook の実行中にします。 ストリームを変更するときに Outlook が実行中の場合、シャット ダウン時、変更内容が上書きされます可能性があります。
    
- 操作を行いますしない書き込み] のプロパティ PT_MV_UNICODE および PR_MV_STRING8 Microsoft Outlook 2003 が使用するオートコンプリート ストリームにします。 これらのプロパティは、Outlook 2007 と Outlook 2010、Outlook 2013 でのみ認識されます。
    
- 読み書きしている標準的なファイル ・ ロック ・ (たとえば、**ロック ファイル**で C または C++ および**の Api を使用してその中に他のプロセスによって変更から .nk2 ファイルをロックすることをお勧めして Outlook 2007 を操作するコードを開発する場合FileStream.Lock**では C#)。 
    
- オートコンプリート ストリームの行セットからの型のプロパティを変更するだけです。 オートコンプリートのストリームのプロパティとプロパティの型の詳細については、[オートコンプリートのストリーム](autocomplete-stream.md)を参照してください。
    
## <a name="see-also"></a>関連項目



[オートコンプリート ストリーム](autocomplete-stream.md)
  
[MAPI プロファイル](mapi-profiles.md)


[Outlook 2003/2007 の NK2 ファイル形式と開発者のガイドライン](http://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)

