---
title: PidTagStoreSupportMask 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreSupportMask
api_type:
- COM
ms.assetid: ada5694a-b5b1-471f-be33-906fc052681a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 143e7f0d2cd89cd4e7956cdda05d1bd512db4027
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340972"
---
# <a name="pidtagstoresupportmask-canonical-property"></a>PidTagStoreSupportMask 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージストアの特性を判断するためにクライアントアプリケーションが照会するフラグのビットマスクを含みます。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_STORE_SUPPORT_MASK  <br/> |
|識別子:  <br/> |0x340d  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |その他  <br/> |
   
## <a name="remarks"></a>解説

このプロパティは、メッセージの送信を計画しているクライアントアプリケーションに対して、メッセージストアの機能を discloses ます。 このフラグは、 **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) または**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) のいずれかを送信するかどうかなど、クライアントまたは別のストアによる決定をサポートできます。 クライアントは**PR_STORE_SUPPORT_MASK**を設定してはなりません。このフラグを設定しようとすると、MAPI_E_COMPUTED が返されます。 
  
**PR_STORE_SUPPORT_MASK**ビットマスクには、次の1つ以上のフラグを設定できます。 
  
STORE_ANSI_OK
  
> (131072、0x00020000)メッセージストアは、ANSI (8 ビット) 文字を含むプロパティをサポートします。
    
STORE_ATTACH_OK 
  
> (32、0x00000020)メッセージストアは、メッセージへの添付ファイル (ole または ole 以外) をサポートします。 
    
STORE_CATEGORIZE_OK 
  
> (1024、0x00000400)メッセージストアは、テーブルの分類されたビューをサポートします。 
    
STORE_CREATE_OK 
  
> (16、0x00000010)メッセージストアは新しいメッセージの作成をサポートしています。 
    
STORE_ENTRYID_UNIQUE 
  
> (1, 0x00000001)メッセージストア内のオブジェクトのエントリ識別子は一意であり、ストアの有効期間中は再利用されません。 
    
STORE_HTML_OK 
  
> (65536、0x00010000)メッセージストアは、 **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)) プロパティに格納されている HTML メッセージをサポートします。 開発環境で mapidefs.h を使用している場合。H ファイルに STORE_HTML_OK が含まれていない場合は、値0x00010000 を代わりに使用します。 
    
STORE_ITEMPROC
  
> (2097152、0x00200000)ラップされた PST ストアで、新しいメッセージがストアに到着すると、ストアはメッセージに対してルールおよびスパムフィルター処理を個別に実行することを示します。 ストアは[imapisupport:: Notify](imapisupport-notify.md)を呼び出し、パラメーターとして渡される[通知](notification.md)構造で**fnevNewMail**を設定してから、新しいメッセージの詳細をリスニングクライアントに渡します。 その後、リッスンしているクライアントが通知を受信すれば、メッセージに対するルールの処理は行われなくなります。 
    
STORE_LOCALSTORE
  
> (524288、0x00080000)このフラグは予約されているため、使用しないでください。
    
STORE_MODIFY_OK 
  
> (8, 0x00000008)メッセージストアは、既存のメッセージの変更をサポートしています。 
    
STORE_MV_PROPS_OK 
  
> (512、0x00000200)メッセージストアは、複数値プロパティをサポートしており、保存操作中に複数値プロパティの値の順序の安定性を保証し、テーブル内の複数値プロパティのインスタンス化をサポートします。 
    
STORE_NOTIFY_OK 
  
> (256、0x00000100)メッセージストアが通知をサポートしている。 
    
STORE_OLE_OK 
  
> (64、0x00000040)メッセージストアは OLE 添付ファイルをサポートします。 OLE データには、 **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) プロパティを使用して利用できるような**IStorage**インターフェイスを介してアクセスできます。 
    
STORE_PUBLIC_FOLDERS 
  
> (16384、0x00004000)このストア内のフォルダーはパブリック (マルチユーザー) であり、プライベートではありません (複数のインスタンスが複数のユーザーではない可能性があります)。 
    
STORE_PUSHER_OK
  
> (8388608、0x00800000)MAPI プロトコルハンドラーはストアをクロールしません。ストアは、メッセージをインデックス処理するために、インデクサーに対する通知による変更をすべて受信することを担当します。
    
STORE_READONLY 
  
> (2, 0x00000002)メッセージストアのすべてのインターフェイスには、読み取り専用のアクセスレベルがあります。 
    
STORE_RESTRICTION_OK 
  
> (4096、0x00001000)メッセージストアは制限をサポートします。 
    
STORE_RTF_OK 
  
> (2048、0x00000800)メッセージストアは、リッチテキスト形式 (RTF) メッセージ (通常は圧縮済み) をサポートしており、ストア自体は**PR_BODY**と**PR_RTF_COMPRESSED**の同期を維持します。 
    
STORE_RULES_OK
  
> (268435456、0x10000000)既定のストアではない場合でも、ルールがこの PST ストアに保存されることを示します。 **STORE_RULES_OK**が**NON_EMS_XP_SAVE**と組み合わせて使用されている場合、ルールは既定以外の PST ラップストアに対して実行できます。
    
STORE_SEARCH_OK 
  
> (4、0x00000004)メッセージストアは、検索結果フォルダーをサポートします。 
    
STORE_SORT_OK 
  
> (8192、0x00002000)メッセージストアは、テーブルの並べ替えビューをサポートしています。 
    
STORE_SUBMIT_OK 
  
> (128、0x00000080)メッセージストアは、送信用のメッセージのマーキングをサポートしています。 
    
STORE_UNCOMPRESSED_RTF 
  
> (32768、0x00008000)メッセージストアは、RTF メッセージの保存を未圧縮形式でサポートしています。 圧縮されていない RTF ストリームは、stream ヘッダーの値**dwMagicUncompressedRTF**によって識別されます。 **dwMagicUncompressedRTF**の値は、rtflib で定義されています。H ファイル 
    
STORE_UNICODE_OK
  
> (262144, 0x00040000)メッセージストアが Unicode ストレージをサポートしていることを示します。 クライアントは、フラグの有無を調べて、Unicode の情報を要求するかストアに保存するかを決定できます。 
    
メッセージストアが rtf に対応していない場合でも、メッセージの rtf バージョンを保存できます。 特定のストアに対して STORE_RTF_OK ビットが設定されていない場合、RTF バージョンを保持しているクライアントは、 **PR_BODY**と**PR_RTF_COMPRESSED**のバージョンとテキストコンテンツの同期を維持するために、 [rtfsync](rtfsync.md)関数を呼び出す必要があります。 RTF は、実際に圧縮されているかどうかにかかわらず、常に**PR_RTF_COMPRESSED**に保存されます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXMSG]](https://msdn.microsoft.com/library/b046868c-9fbf-41ae-9ffb-8de2bd4eec82%28Office.15%29.aspx)
  
> クライアント上の共有フォルダーに関連する情報を送信するために使用されるメッセージの形式について説明します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

