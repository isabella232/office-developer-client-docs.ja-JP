---
title: PidTagResourceFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourceFlags
api_type:
- COM
ms.assetid: 69be9ad3-006a-459e-9cd4-eb3f609d71ad
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 875b37183134a6c5beca76ab7910cf601d1b6175
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567504"
---
# <a name="pidtagresourceflags-canonical-property"></a>PidTagResourceFlags 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メッセージ サービスおよびプロバイダーのフラグのビットマスクを格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RESOURCE_FLAGS  <br/> |
|識別子:  <br/> |0x3009  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|領域:  <br/> |一般的な MAPI  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティでは、メッセージ サービス、サービス プロバイダー、または状態オブジェクトの特性について説明します。 このプロパティに設定されているフラグは、そのコンテキストに依存します。 などのいくつかのフラグは、オブジェクトのステータスおよびその他のフラグをメッセージ サービス テーブルの列に対してのみに対してのみ有効です。 
  
フラグは、3 つのクラス: 静的で、変更可能なおよび動的な。 静的なフラグは、MAPISVC 内のデータから、MAPI によって設定されます。INF し、改ざんを防止します。 MAPISVC から MAPI で変更可能なフラグが設定されています。INF が後で変更できます。 動的フラグを設定し、MAPI の方法をリセットできます。
  
メッセージ サービスは、次のフラグの 1 つ以上設定できますこのプロパティにします。
  
SERVICE_CREATE_WITH_STORE 
  
> 予約済み。 使用しないでください。
    
SERVICE_DEFAULT_STORE 
  
> 動的です。 メッセージ サービスには、既定のストアが含まれています。 削除するか、プロファイルからこのサービスを移動する前に確認のプロンプトを表示、ユーザー インターフェイスが表示されます。 
    
SERVICE_NO_PRIMARY_IDENTITY 
  
> 静的です。 サービス レベルのフラグなしでメッセージ サービス プロバイダーの使用できることを id を指定するを示すために設定する必要があります。 セットは、このフラグまたは SERVICE_PRIMARY_IDENTITY 必要があります。
    
SERVICE_PRIMARY_IDENTITY 
  
> 変更可能です。 対応するメッセージ サービスには、このセッションのプライマリ id に使用されるプロバイダーが含まれています。 [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md)を使用すると、このフラグを設定できます。 セットは、このフラグまたは SERVICE_NO_PRIMARY_IDENTITY 必要があります。 
    
SERVICE_SINGLE_COPY 
  
> 静的です。 作成するか、このメッセージ サービスをサービスが既に存在するプロファイルにコピーしようが失敗します。 1 つのコピーを作成するのには、メッセージ サービスは、MAPISVC でのサービスのセクションに**PR_RESOURCE_FLAGS**プロパティを追加します。INF、このフラグを設定します。 
    
サービス プロバイダーには、次のフラグの 1 つ以上設定できますで**PR_RESOURCE_FLAGS**。
  
HOOK_INBOUND 
  
> 静的です。 スプーラーのフックは、受信メッセージを処理する必要があります。
    
HOOK_OUTBOUND 
  
> 静的です。 スプーラーのフックは、送信メッセージを処理する必要があります。 
    
STATUS_DEFAULT_OUTBOUND 
  
> 変更可能です。 プロファイルには、このトランスポート プロバイダーの複数のインスタンスが含まれている場合、この id を送信メッセージに適用する必要があります。 これは、プロファイルに 1 つのトランスポート プロバイダーの複数のインスタンスが表示される場合に発生します。
    
STATUS_DEFAULT_STORE 
  
> 変更可能です。 このメッセージ ・ ストアは、プロファイルの既定のストアです。 
    
STATUS_NEED_IPM_TREE 
  
> 動的です。 個人間メッセージ (IPM) のルート フォルダーを含めて、このメッセージ ストア内の標準のフォルダーは、まだ確認されていません。 MAPI では、設定し、このフラグをクリアします。 
    
STATUS_NO_DEFAULT_STORE 
  
> 静的です。 このメッセージ ・ ストアは、プロファイルの既定のメッセージ ストアになることはありません。
    
STATUS_NO_PRIMARY_IDENTITY 
  
> 静的です。 このプロバイダーは、その [状態] 行の id を提供していません。 このフラグまたは STATUS_PRIMARY_IDENTITY のいずれかを設定する必要があります。
    
STATUS_OWN_STORE 
  
> 静的です。 このトランスポート プロバイダーは、メッセージ ストアと密接に関連し、のステータス行に、 **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) のプロパティを提供します。
    
STATUS_PRIMARY_IDENTITY 
  
> 変更可能です。 このプロバイダーがセッションのプライマリ id を提供します。[IMAPISession::QueryIdentity](imapisession-queryidentity.md)から id を使用する際のオブジェクトのエントリ id が返されます。 このフラグまたは**STATUS_NO_PRIMARY_IDENTITY**のいずれかを設定する必要があります。 
    
STATUS_PRIMARY_STORE 
  
> 変更可能です。 このメッセージ ストアは、クライアント アプリケーションがログオンするときに使用します。 開くと、このストアは、プロファイルの既定のストアとして設定してください。 
    
STATUS_SECONDARY_STORE 
  
> 変更可能です。 このメッセージ ストアは、クライアント アプリケーションがログオンすると、プライマリ ストアが使用できない場合に使用します。 開くと、このストアは、プロファイルの既定のストアとして設定してください。 
    
STATUS_SIMPLE_STORE 
  
> 動的です。 このメッセージ ・ ストアは、簡易 MAPI での既定のメッセージ ストアとして使用されます。
    
STATUS_TEMP_SECTION 
  
> 動的です。 このメッセージ ・ ストアは、メッセージ ストアの表には公開しないようにし、ログオフ後、プロファイルから削除されます。 
    
STATUS_XP_PREFER_LAST 
  
> 静的です。 このトランスポートは、複数のトランスポート プロバイダーは、メッセージを送信できなかったときにメッセージを送信する選択されている最後のトランスポートを期待しています。
    
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)
  
[PidTagIdentityEntryId 標準プロパティ](pidtagidentityentryid-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

