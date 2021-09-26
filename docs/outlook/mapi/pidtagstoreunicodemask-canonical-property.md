---
title: PidTagStoreUnicodeMask 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagStoreUnicodeMask
api_type:
- COM
ms.assetid: a6082162-2a74-4850-a0df-4bdbc67b41d8
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 438c770e9c004973e6635d575b7a8134891ee964
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629705"
---
# <a name="pidtagstoreunicodemask-canonical-property"></a>PidTagStoreUnicodeMask 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアント アプリケーションがメッセージ ストアの特性を判断するためにクエリを実行する必要があるフラグのビットマスクが含まれる。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_STORE_UNICODE_MASK  <br/> |
|識別子:  <br/> |0x340F  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI メッセージ ストア  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、メッセージ ストアの機能を、メッセージの送信を計画しているクライアント アプリケーションに公開します。 このフラグは、PR_BODY ([PidTagBody](pidtagbody-canonical-property.md)) を送信するか **、PR_RTF_COMPRESSED** **(** [PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) のみを送信するかなど、クライアントまたは別のストアによる決定を容易にできます。 クライアントは、このプロパティを設定する必要があります。 試行によって、MAPI_E_COMPUTED が **返されます**。 
  
このプロパティには、次のフラグを 1 つ以上設定できます。 
  
STORE_ANSI_OK
  
> (131072、0x00020000)メッセージ ストアは、米国国立標準研究所 (ANSI) (8 ビット) 文字を含むプロパティをサポートしています。
    
STORE_ATTACH_OK 
  
> (32,0x00000020)メッセージ ストアは、メッセージへのオブジェクト リンクと埋め込み (OLE) または OLE 以外の添付ファイルをサポートします。 
    
STORE_CATEGORIZE_OK 
  
> (1024,0x00000400)メッセージ ストアは、テーブルの分類ビューをサポートします。 
    
STORE_CREATE_OK 
  
> (16、0x00000010)メッセージ ストアでは、新しいメッセージの作成がサポートされています。 
    
STORE_ENTRYID_UNIQUE 
  
> (1、0x00000001)メッセージ ストア内のオブジェクトのエントリ識別子は一意です。つまり、ストアの期間中は再利用されません。 
    
STORE_HTML_OK 
  
> (65536、0x00010000)メッセージ ストアは HTML メッセージをサポートします。このメッセージは、PR_BODY_HTML **(** [PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)) プロパティに格納されます。 MAPIDEFS **STORE_HTML_OK** のバージョンでは定義されていない点に注意してください。Microsoft Exchange 2000 Server 以前に含まれる H。 ご使用の開発環境で MAPIDEFS を使用している場合。このファイルを含STORE_HTML_OK H **ファイルは、** 代わりに "0x00010000" を使用します。 
    
STORE_ITEMPROC
  
> (2097152、0x00200000)ラップされた PST ストアで、新しいメッセージがストアに到着すると、ストアはメッセージに対してルールとスパム フィルター処理を個別に実行します。 ストアは [IMAPISupport::Notify](imapisupport-notify.md)を呼び出し、パラメーターとして渡される [NOTIFICATION](notification.md)構造で **fnevNewMail** を設定し、新しいメッセージの詳細をリッスン クライアントに渡します。 その後、リッスンしているクライアントが通知を受信すれば、メッセージに対するルールの処理は行われなくなります。 
    
STORE_LOCALSTORE
  
> (524288、0x00080000)このフラグは予約済みであり、使用できません。
    
STORE_MODIFY_OK 
  
> (8、0x00000008)メッセージ ストアは、既存のメッセージの変更をサポートしています。 
    
STORE_MV_PROPS_OK 
  
> (512,0x00000200)メッセージ ストアは、複数値プロパティをサポートし、保存操作を通じて複数値プロパティの値の順序の安定性を保証し、テーブルでの複数値プロパティのインスタンス化をサポートします。 
    
STORE_NOTIFY_OK 
  
> (256,0x00000100)メッセージ ストアは通知をサポートしています。 
    
STORE_OLE_OK 
  
> (64、0x00000040)メッセージ ストアは OLE 添付ファイルをサポートしています。 OLE データは **、IStorage** インターフェイスを介してアクセスできます (PR_ATTACH_DATA_OBJ **(** [PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) プロパティを使用して使用できます。 
    
STORE_PUBLIC_FOLDERS 
  
> (16384,0x00004000)このストア内のフォルダーはパブリック (マルチユーザー) で、プライベート (マルチインスタンスの場合は複数インスタンスではなく、マルチユーザー) ではありません。 
    
STORE_PUSHER_OK
  
> (8388608、0x00800000)MAPI プロトコル ハンドラーはストアをクロールしません。また、メッセージのインデックスを作成するためにインデクサーに通知を通じて変更をプッシュする責任があります。
    
STORE_READONLY 
  
> (2、0x00000002)メッセージ ストアのすべてのインターフェイスには、読み取り専用アクセス レベルがあります。 
    
STORE_RESTRICTION_OK 
  
> (4096,0x00001000)メッセージ ストアは制限をサポートしています。 
    
STORE_RTF_OK 
  
> (2048,0x00000800)メッセージ ストアは、通常は圧縮されたリッチ テキスト形式 (RTF) メッセージをサポートし、ストア自体が同期 **PR_BODYとPR_RTF_COMPRESSED****保持します**。 
    
STORE_SEARCH_OK 
  
> (4、0x00000004)メッセージ ストアは、検索結果フォルダーをサポートしています。 
    
STORE_SORT_OK 
  
> (8192,0x00002000)メッセージ ストアは、テーブルの並べ替えビューをサポートしています。 
    
STORE_SUBMIT_OK 
  
> (128,0x00000080)メッセージ ストアは、送信用のメッセージのマーキングをサポートしています。 
    
STORE_UNCOMPRESSED_RTF 
  
> (32768,0x00008000)メッセージ ストアでは、変更可能なフォーム テキスト (RTF) メッセージを圧縮されていない形式で保存できます。 圧縮されていない RTF ストリームは、ストリーム ヘッダーの **値 dwMagicUncompressedRTF** によって識別されます。 **dwMagicUncompressedRTF** 値は RTFLIB で定義されます。H ファイル。 
    
STORE_UNICODE_OK
  
> (262144、0x00040000)メッセージ ストアは、Unicode 文字を含むプロパティをサポートしています。
    
メッセージ ストアが RTF 対応でない場合でも、RTF バージョンのメッセージを常に保存できます。 STORE_RTF_OK ビットが特定のストアに対して設定されていない場合、RTF バージョンを管理するクライアントは、それ自体が [RTFSync](rtfsync.md) 関数を呼び出して **、PR_BODY** バージョンと **PR_RTF_COMPRESSED** バージョンをテキスト コンテンツ用に同期する必要があります。 RTF は、実際に **PR_RTF_COMPRESSED** かどうかに関PR_RTF_COMPRESSED常に格納されます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

