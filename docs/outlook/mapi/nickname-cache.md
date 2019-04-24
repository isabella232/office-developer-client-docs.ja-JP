---
title: ニックネーム キャッシュ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2813c102-6778-4443-ab4b-b573f3568705
description: '最終更新日: 2013 年1月30日'
ms.openlocfilehash: 841b01ae8dfcf841b0a1d64113ce7258c4c61583
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334518"
---
# <a name="nickname-cache"></a>ニックネーム キャッシュ

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
microsoft Office Outlook 2007、microsoft outlook 2010、および microsoft outlook 2013 は、"オートコンプリートストリーム" とも呼ばれるニックネームキャッシュを操作します。 オートコンプリートストリームは、Outlook では、ユーザーが電子メールを作成している間に [**宛先**]、[ **Cc**]、および [ **Bcc** ] の各編集ボックスに表示される名前の一覧を保持します。 このトピックでは、outlook 2007、outlook 2010、および outlook 2013 がオートコンプリートストリームを操作する方法について説明し、ファイルのバイナリ形式およびオートコンプリートストリームと対話するための推奨される方法についても説明します。 
  
outlook 2010 または outlook 2013 と対話するアプリケーションでは、オートコンプリートストリームは mapi プロパティとして格納され、メッセージの mapi または**PropertyAccessor**オブジェクトを使用して変更できます。 **PropertyAccessor**オブジェクトは、outlook 2010 または outlook 2013 オブジェクトモデルで公開されます。 
  
Outlook 2007 オブジェクトモデルまたは MAPI api に依存関係はありません。 そのため、Outlook 2007 内のオートコンプリートストリームに変更を加えるアプリケーションは、任意のプログラミング言語を使用して記述できます。
  
## <a name="interacting-with-the-autocomplete-stream"></a>オートコンプリートストリームとの対話

[**宛先**]、[ **Cc**]、または [ **Bcc** ] 編集ボックスにメッセージがアクセスされると、オートコンプリートストリームが読み込まれ、ユーザー名の一覧が表示されます。 Outlook は、次の2つの方法で、オートコンプリートストリームと対話します。 
  
1. オートコンプリートストリームを読み込む 
    
2. オートコンプリートストリームのデータに加えた変更を保存する
    
次に示すように、オートコンプリートデータを保存する方法は、outlook 2007 と outlook 2010 または outlook 2013 で異なります。 
  
 **Outlook 2007**
  
Outlook 2007 では、オートコンプリートストリームはプロファイルと同じ名前のファイルに格納され、拡張子は nk2 になります。 たとえば、既定の "outlook" プロファイルが使用されている場合、ファイルは "nk2" という名前になります。 nk2 ファイルは%APPDATA%\Microsoft\Outlook. に保存されます。 ニックネームキャッシュバイナリファイル形式の詳細については、「 [Outlook 2003/2007 NK2 ファイル形式と開発者ガイドライン](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)」を参照してください。
  
 **outlook 2010 および outlook 2013**
  
outlook 2010 または outlook 2013 は、メールアカウントの配信ストアの受信トレイにある [関連付けられたコンテンツ] テーブル内のメッセージから、オートコンプリートストリームを読み取ります。 この隠しメッセージには、メッセージクラスと IPM の件名があります。構成のオートコンプリート。 オートコンプリートストリームは、このメッセージの PR_ROAMING_BINARYSTREAM プロパティ ([PidTagRoamingBinary 標準プロパティ](pidtagroamingbinary-canonical-property.md)) に格納されます。 オートコンプリートデータが%USERPROFILE%\AppData\Local\Microsoft\Outlook\RoamCache. にある自動保存ファイルに一時的にキャッシュされることがあります。 ただし、.dat ファイルはキャッシュのみであり、ユーザーが outlook 2010 または outlook 2013 を終了するときに配信ストアに書き戻すためには使用されません。
  
## <a name="loading-the-autocomplete-stream"></a>オートコンプリートストリームを読み込む

Outlook は、アドレス指定機能を持つアイテムが初期化されるたびに、オートコンプリートストリームを読み込みます。 たとえば、新しいメール、メールの返信、連絡先アイテム、会議出席依頼などの電子メールアドレスが使用されます。 データを読み込むために、Outlook はストリームのすべての内容をメモリに読み取ります。
  
オートコンプリート操作の場合、outlook は、outlook .exe プロセスの有効期間中は、このようなインメモリ構造に排他的に作用します。 Outlook では、この構造体はシャットダウン時にのみ保存されます。 このプロセスの詳細については、次のセクション「オートコンプリートストリームの保存」を参照してください。
  
## <a name="saving-the-autocomplete-stream"></a>オートコンプリートストリームの保存

次のいずれかの方法でオートコンプリートの一覧が変更された場合、Outlook は、オートコンプリートストリームをシャットダウン時に保存します。
  
- 名前の解決、[アドレス帳] ダイアログからの受信者の選択、またはまだリストにない受信者へのメールの送信によって、新しいニックネームエントリが追加されます。
    
- エントリは、リスト内の既存の受信者にメールを送信することによって変更されます。
    
- ユーザーが UI を通じてエントリを削除します。
    
- その他の重要なシナリオは、このトピックに関連していません。
    
オートコンプリートデータへの変更を保存するには、メモリ内構造を[オートコンプリートストリーム](autocomplete-stream.md)に書き戻す必要があります。 Outlook 2007 と対話する場合、stream はローカルの nk2 ファイルに保存されます。 outlook 2010 または outlook 2013 の場合、オートコンプリートストリームは、メールアカウントの配信ストアの受信トレイの関連コンテンツテーブルに書き戻します。
  
## <a name="recommendations"></a>推奨事項

- オートコンプリートストリームを部分的に変更することはありません。 サポートされている相互作用は、すべてのオートコンプリートストリームをメモリに読み取り、2) メモリ構造を変更し、3) メールアカウントの配信ストアの受信トレイの関連するコンテンツテーブルにストリーム全体を書き込む (Outlook 2010 またはoutlook 2013) または nk2 ファイル (outlook 2007)。
    
- Outlook の実行中は、オートコンプリートストリームと対話しません。 ストリームを変更している間に Outlook が実行されている場合は、シャットダウン時に変更内容が上書きされる可能性があります。
    
- PT_MV_UNICODE および PR_MV_STRING8 型のプロパティを、Microsoft Outlook 2003 で使用されるオートコンプリートストリームに書き込むことはできません。 これらのプロパティは、outlook 2007、outlook 2010、および outlook 2013 でのみ認識されます。
    
- Outlook 2007 と対話するコードを開発する場合は、他のプロセスによって、nk2 ファイルを変更しないようにすることをお勧めします。これは、標準的**** なファイルロック api (たとえば、C/c + +**で LockFile) を使用して読み取りおよび書き込みを行っています。** C# でのロック)。 
    
- オートコンプリートストリームの行セットにある型のプロパティのみを変更します。 オートコンプリートストリームのプロパティとプロパティの種類の詳細については、「 [autocomplete stream](autocomplete-stream.md)」を参照してください。
    
## <a name="see-also"></a>関連項目



[オートコンプリートストリーム](autocomplete-stream.md)
  
[MAPI プロファイル](mapi-profiles.md)


[Outlook 2003/2007 NK2 ファイル形式と開発者ガイドライン](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)

