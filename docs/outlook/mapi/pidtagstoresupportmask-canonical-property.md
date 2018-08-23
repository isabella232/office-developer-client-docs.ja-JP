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
ms.openlocfilehash: 1936cb8e95e3faef8c92d6bf28f5b63b3ff72df5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572705"
---
# <a name="pidtagstoresupportmask-canonical-property"></a>PidTagStoreSupportMask 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
フラグのビットマスクにはメッセージ ・ ストアの特性を判断するのにはそのクライアント アプリケーションのクエリが含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_STORE_SUPPORT_MASK  <br/> |
|識別子:  <br/> |0x340D  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|領域:  <br/> |その他  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、メッセージを送信する計画は、クライアント アプリケーションにメッセージ ・ ストアの機能を公開します。 フラグは、クライアントまたは別のストア ([PidTagBody](pidtagbody-canonical-property.md)) である**PR_BODY** **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) をのみを送信するかどうかなど、意思決定をサポートできます。 クライアントは**PR_STORE_SUPPORT_MASK**; を設定しない必要があります。このフラグを設定するには、MAPI_E_COMPUTED が返されます。 
  
**PR_STORE_SUPPORT_MASK**ビットマスクについては、次のフラグの 1 つ以上を設定できます。 
  
STORE_ANSI_OK
  
> (131072、0x00020000)メッセージ ・ ストアには、ANSI (8 ビット) 文字が含まれるプロパティがサポートされています。
    
STORE_ATTACH_OK 
  
> (32、0x00000020)メッセージ ・ ストアは、メッセージ添付ファイル (または非 OLE OLE) をサポートします。 
    
STORE_CATEGORIZE_OK 
  
> (1024、0x00000400)メッセージ ・ ストアでは、テーブルの分類されたビューをサポートします。 
    
STORE_CREATE_OK 
  
> (16、0x00000010)メッセージ ・ ストアには、新しいメッセージの作成がサポートされています。 
    
STORE_ENTRYID_UNIQUE 
  
> (1、0x00000001)エントリ、メッセージ ・ ストア内のオブジェクトの一意な識別子、つまり、ストアの有効期間中に使用されることです。 
    
STORE_HTML_OK 
  
> (65536、0x00010000)メッセージ ・ ストアは、 **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)) のプロパティに格納されている HTML メッセージをサポートしています。 場合は、開発環境は、MAPIDEFS を使用します。H ファイルでは、STORE_HTML_OK ではない値 0x00010000 を代わりに使用します。 
    
STORE_ITEMPROC
  
> (2,097, 152、0x00200000)ラップされた PST ストアのストアでは、新しいメッセージが到着すると、ストアを実行する仕訳ルールと迷惑メール フィルターがメッセージを個別に処理を示します。 ストアの呼び出し[IMAPISupport::Notify](imapisupport-notify.md)、[通知](notification.md)の構造体をパラメーターとして渡され、リッスンしているクライアントに新しいメッセージの詳細を渡すには、設定**fnevNewMail** 。 その後、リッスンしているクライアントでは、通知を受信すると、メッセージのルールは処理されません。 
    
STORE_LOCALSTORE
  
> (524288、0x00080000)このフラグは予約されており、使用する必要があります。
    
STORE_MODIFY_OK 
  
> (8, 0x00000008)メッセージ ・ ストアには、既存のメッセージの変更がサポートしています。 
    
STORE_MV_PROPS_OK 
  
> (512、0x00000200)メッセージ ・ ストアが複数値を持つプロパティをサポートして、セーブセット全体で複数値を持つプロパティの値の順序の安定性を保証する操作、およびテーブル内の複数値を持つプロパティのインスタンス化をサポートしています。 
    
STORE_NOTIFY_OK 
  
> (256、0x00000100)メッセージ ・ ストアは、通知をサポートしています。 
    
STORE_OLE_OK 
  
> (64、0x00000040)メッセージ ・ ストアでは、OLE 添付ファイルをサポートしています。 OLE データにアクセスできますよう、 **IStorage**インターフェイスを使用、 **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) プロパティを使用。 
    
STORE_PUBLIC_FOLDERS 
  
> (16384、0x00004000)このストア内のフォルダーは、パブリック (マルチ ユーザー)、非プライベート (可能性のある複数のインスタンスですが、マルチ ユーザーではなく)。 
    
STORE_PUSHER_OK
  
> (8,388, 608、0x00800000)MAPI プロトコル ハンドラーはストアをクロールしないと、ストアがメッセージをインデックス付けされたインデクサーに通知を使用して、変更をプッシュを行います。
    
STORE_READONLY 
  
> (2, 0x00000002)メッセージ ストアのすべてのインタ フェースでは、読み取り専用のアクセス レベルがあります。 
    
STORE_RESTRICTION_OK 
  
> (4096、0x00001000)メッセージ ・ ストアには、制限がサポートされています。 
    
STORE_RTF_OK 
  
> (2048、0x00000800)メッセージ ・ ストアは、リッチ テキスト形式 (RTF) メッセージは、通常は圧縮をサポートしていて、ストア自体が**PR_BODY**と**PR_RTF_COMPRESSED**の同期を維持します。 
    
STORE_RULES_OK
  
> (268435456、0x10000000)既定のストアではない場合でも、この PST ストアにルールを格納するかを示します。 **STORE_RULES_OK**を**NON_EMS_XP_SAVE**と組み合わせて使用する場合、ルールは、既定ではないラップ PST ストア上で実行すること。
    
STORE_SEARCH_OK 
  
> (4、0x00000004)メッセージ ・ ストアには、検索結果フォルダーがサポートしています。 
    
STORE_SORT_OK 
  
> (8192、0x00002000)メッセージ ・ ストアでは、テーブルのビューが並べ替えをサポートします。 
    
STORE_SUBMIT_OK 
  
> (128, 0x00000080)メッセージ ・ ストアは、メッセージ送信用のマークをサポートします。 
    
STORE_UNCOMPRESSED_RTF 
  
> (32768、0x00008000)メッセージ ・ ストアでは、圧縮されていないフォームに rtf 形式のメッセージの記憶域をサポートしています。 非圧縮の rtf 形式のストリームは、ストリームのヘッダーの値**dwMagicUncompressedRTF**で識別されます。 **DwMagicUncompressedRTF**値は、RTFLIB で定義されています。H ファイルです。 
    
STORE_UNICODE_OK
  
> (262144、0x00040000)メッセージ ・ ストアが Unicode のストレージをサポートしていることを示します。 クライアントは Unicode 情報をストアに保存するかを要求するかを決定するフラグの有無を確認できます。 
    
メッセージ ・ ストアが RTF に対応していない場合でも、rtf メッセージを保存常にできます。 STORE_RTF_OK ビットが特定のストアに設定されていない場合は、rtf 形式のバージョンを管理するクライアント自体関数を呼び出す必要[へ](rtfsync.md)テキストの内容を同期して**PR_BODY**と**PR_RTF_COMPRESSED**のバージョンを保持します。 Rtf 形式は、それが実際に圧縮するかどうかどうかに常に**PR_RTF_COMPRESSED**に格納されます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXMSG]](http://msdn.microsoft.com/library/b046868c-9fbf-41ae-9ffb-8de2bd4eec82%28Office.15%29.aspx)
  
> クライアント上のフォルダーを共有に関連する情報の送信に使用されるメッセージの形式について説明します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

