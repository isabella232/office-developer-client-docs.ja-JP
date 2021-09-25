---
title: ニックネーム キャッシュ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 2813c102-6778-4443-ab4b-b573f3568705
description: '最終更新日: 2013 年 1 月 30 日'
ms.openlocfilehash: 6c1074086f4aec413c09fdfe3ca8e7b879f083e4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579454"
---
# <a name="nickname-cache"></a>ニックネーム キャッシュ

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
Microsoft Office Outlook 2007、Microsoft Outlook 2010、Microsoft Outlook 2013は、"オートコンプリート ストリーム" とも呼ばれるニックネーム キャッシュと対話します。 オートコンプリート ストリームは、Outlook がオートコンプリート リストを保持する場所です。これは、ユーザーが電子メールを作成している間、To、Cc、および **Bcc** の編集ボックスに表示される名前の一覧です。   このトピックでは、Outlook 2007、Outlook 2010、Outlook 2013 がオートコンプリート ストリームとやり取りする方法と、ファイルのバイナリ形式とオートコンプリート ストリームを操作するための推奨される方法について説明します。 
  
Outlook 2010 または Outlook 2013 と対話するアプリケーションの場合、オートコンプリート ストリームは MAPI プロパティとして格納され、MAPI またはメッセージの **PropertyAccessor** オブジェクトを使用して変更できます。 **PropertyAccessor オブジェクト** は、2010 年または 2013 Outlook 2013 Outlookで公開されます。 
  
2007 オブジェクト モデルOutlook MAPI API には依存関係はありません。 したがって、2007 年から 2007 年Outlookでオートコンプリート ストリームに変更を加えるアプリケーションは、任意のプログラミング言語を使用して記述できます。
  
## <a name="interacting-with-the-autocomplete-stream"></a>オートコンプリート ストリームの操作

メッセージで **[To]** **、Cc、****または Bcc** の編集ボックスにアクセスすると、オートコンプリート ストリームが読み込まれ、ユーザー名の一覧が表示されます。 Outlookオートコンプリート ストリームを操作するには、次の 2 つの方法があります。 
  
1. オートコンプリート ストリームの読み込み 
    
2. オートコンプリート ストリームのデータに対する変更の保存
    
オートコンプリート データを格納する方法は、Outlook 2007 と Outlook 2010 または Outlook 2013 の間で異なります。 
  
 **Outlook 2007**
  
2007 Outlook、オートコンプリート ストリームはプロファイルと同じ名前で拡張子 .nk2 のファイルに格納されます。 たとえば、"outlook" の既定のプロファイルを使用する場合、ファイルは "outlook.nk2" と呼ばれる。 .nk2 ファイルは %APPDATA%\Microsoft\Outlook に格納されます。 ニックネーム キャッシュ バイナリ ファイル形式の詳細については[、「Outlook NK2](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)ファイル形式と開発者向けガイドライン」を参照してください。
  
 **Outlook 2010 および Outlook 2013**
  
Outlook 2010 または Outlook 2013 は、メール アカウントの配信ストアの受信トレイの [関連コンテンツ] テーブルにあるメッセージからオートコンプリート ストリームを読み取ります。 この非表示のメッセージには、IPM のメッセージ クラスと件名があります。Configuration.Autocomplete。 オートコンプリート ストリームは、PR_ROAMING_BINARYSTREAM プロパティ[(PidTagRoamingBinary 標準](pidtagroamingbinary-canonical-property.md)プロパティ) のこのメッセージに格納されます。 オートコンプリート データは、%USERPROFILE%\AppData\Local\Microsoft\Outlook\RoamCache にあるオートコンプリート .dat ファイルに一時的にキャッシュされる可能性があります。 ただし、.dat ファイルはキャッシュのみであり、ユーザーが 2010 年または 2013 年 2013 年に終了した場合、配信ストアに書きOutlookにはOutlookされません。
  
## <a name="loading-the-autocomplete-stream"></a>オートコンプリート ストリームの読み込み

Outlook機能を持つアイテムが初期化されるたびに、オートコンプリート ストリームが読み込まれます。 たとえば、電子メール アドレスは、新しいメール、メール返信、連絡先アイテム、会議出席依頼などで使用されます。 データを読み込むOutlookストリームのすべての内容をメモリに読み込みます。
  
オートコンプリート操作の場合、Outlookプロセスの有効期間の間、このメモリ内構造outlook.exe対話します。 Outlookシャットダウン時にのみ構造が保存されます。 このプロセスの詳細については、次のセクション「オートコンプリート ストリームの保存」を参照してください。
  
## <a name="saving-the-autocomplete-stream"></a>オートコンプリート ストリームの保存

Outlookオートコンプリート リストが次の方法で変更された場合、オートコンプリート ストリームはシャットダウン時に保存されます。
  
- 新しいニックネーム エントリは、名前の解決、アドレス帳ダイアログから受信者の選択、またはリストに未登録の受信者へのメールの送信を通じて追加されます。
    
- エントリは、リスト内の既存の受信者にメールを送信することで変更されます。
    
- UI を使用してユーザーがエントリを削除します。
    
- このトピックに関連しないその他の小さなシナリオ。
    
オートコンプリート データへの変更を保存するには、メモリ内構造をオートコンプリート ストリームに書 [き戻す必要があります](autocomplete-stream.md)。 2007 Outlook操作すると、ストリームはローカルの .nk2 ファイルに保存されます。 2010 Outlook Outlook 2013 の場合、オートコンプリート ストリームはメール アカウントの配信ストアの受信トレイの [関連コンテンツ] テーブルに書き戻されます。
  
## <a name="recommendations"></a>推奨事項

- オートコンプリート ストリームを部分的に変更しない。 サポートされる操作は、1) オートコンプリート ストリーム全体をメモリに読み取り、2) メモリ構造を変更し、3) ストリーム全体をメール アカウントの配信ストアの受信トレイの [関連コンテンツ] テーブル (Outlook 2010 または Outlook 2013) またはローカルの .nk2 ファイル (Outlook 2007) に書き戻します。
    
- ユーザーが実行中にオートコンプリート ストリームOutlook操作しない。 ストリームOutlook実行中は、変更がシャットダウン時に上書きされる可能性があります。
    
- Microsoft PT_MV_UNICODE 2003 PR_MV_STRING8で使用されるオートコンプリート ストリームには、Outlookを記述Outlook。 これらのプロパティは、2007 年Outlook 2010 年Outlook 2013 年Outlookのみです。
    
- Outlook 2007 と対話するコードを開発する場合は、標準のファイル ロック API (C/C++ の **LockFile、C#** の **FileStream.Lock** など) を使用して読み取りおよび書き込み中に、.nk2 ファイルを他のプロセスによる変更からロックすることをお勧めします。 
    
- オートコンプリート ストリームの行セットからの型のプロパティのみを変更します。 オートコンプリート ストリームのプロパティとプロパティの種類の詳細については [、「Autocomplete Stream」を参照してください](autocomplete-stream.md)。
    
## <a name="see-also"></a>関連項目



[オートコンプリート ストリーム](autocomplete-stream.md)
  
[MAPI プロファイル](mapi-profiles.md)


[Outlook 2003/2007 NK2 ファイル形式と開発者向けガイドライン](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)

