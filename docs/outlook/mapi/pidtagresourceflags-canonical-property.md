---
title: PidTagResourceFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagResourceFlags
api_type:
- COM
ms.assetid: 69be9ad3-006a-459e-9cd4-eb3f609d71ad
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f2e9100993b02f165c58f60b81307b6b5d04c647
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563358"
---
# <a name="pidtagresourceflags-canonical-property"></a>PidTagResourceFlags 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ サービスとプロバイダーのフラグのビットマスクが含まれる。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RESOURCE_FLAGS  <br/> |
|識別子:  <br/> |0x3009  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI 共通  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、メッセージ サービス、サービス プロバイダー、または状態オブジェクトの特性を説明します。 このプロパティに設定されるフラグは、そのコンテキストによって異なる。 たとえば、一部のフラグはステータス オブジェクトにのみ有効で、他のフラグはメッセージ サービス テーブル内の列に対してのみ有効です。 
  
フラグは、静的、変更可能、動的の 3 つのクラスです。 静的フラグは、MAPISVC のデータから MAPI によって設定されます。INF で、変更されません。 変更可能なフラグは、MAPISVC から MAPI によって設定されます。INF が、後で変更できます。 動的フラグは、MAPI メソッドによって設定およびリセットできます。
  
メッセージ サービスの場合、このプロパティで次のフラグを 1 つ以上設定できます。
  
SERVICE_CREATE_WITH_STORE 
  
> 予約済み。 使用しないでください。
    
SERVICE_DEFAULT_STORE 
  
> 動的。 メッセージ サービスには、既定のストアが含まれる。 このサービスをプロファイルから削除または移動する前に、ユーザーに確認を求めるユーザー インターフェイスを表示する必要があります。 
    
SERVICE_NO_PRIMARY_IDENTITY 
  
> 静的。 メッセージ サービス内のプロバイダーのいずれも ID の指定に使用し得ないかどうかを示すために設定する必要があるサービス レベル フラグ。 このフラグまたは設定SERVICE_PRIMARY_IDENTITY設定する必要がありますが、両方は設定できません。
    
SERVICE_PRIMARY_IDENTITY 
  
> 変更可能。 対応するメッセージ サービスには、このセッションのプライマリ ID に使用されるプロバイダーが含まれる。 この [フラグを設定するには、IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) を使用します。 このフラグまたは設定SERVICE_NO_PRIMARY_IDENTITY設定する必要がありますが、両方は設定できません。 
    
SERVICE_SINGLE_COPY 
  
> 静的。 サービスが既に存在するプロファイルにこのメッセージ サービスを作成またはコピーしようとすると、失敗します。 1 つのコピー メッセージ サービスを作成するには **、MAPISVC** PR_RESOURCE_FLAGSに PR_RESOURCE_FLAGS プロパティを追加します。INF とこのフラグを設定します。 
    
サービス プロバイダーの場合は、次のフラグの 1 つ以上を次に設定 **PR_RESOURCE_FLAGS。**
  
HOOK_INBOUND 
  
> 静的。 スプーラー フックは、受信メッセージを処理する必要があります。
    
HOOK_OUTBOUND 
  
> 静的。 スプーラー フックは送信メッセージを処理する必要があります。 
    
STATUS_DEFAULT_OUTBOUND 
  
> 変更可能。 プロファイルにこのトランスポート プロバイダーの複数のインスタンスが含まれている場合は、この ID を送信メッセージに適用する必要があります。 これは、1 つのトランスポート プロバイダーの複数のインスタンスがプロファイルに表示される場合に発生する可能性があります。
    
STATUS_DEFAULT_STORE 
  
> 変更可能。 このメッセージ ストアは、プロファイルの既定のストアです。 
    
STATUS_NEED_IPM_TREE 
  
> 動的。 このメッセージ ストアの標準フォルダー (対人間メッセージ (IPM) ルート フォルダーを含む) は、まだ確認されていません。 MAPI は、このフラグを設定およびクリアします。 
    
STATUS_NO_DEFAULT_STORE 
  
> 静的。 このメッセージ ストアは、プロファイルの既定のメッセージ ストアになるには使用できません。
    
STATUS_NO_PRIMARY_IDENTITY 
  
> 静的。 このプロバイダーは、ステータス行に ID を指定しない。 このフラグまたは設定STATUS_PRIMARY_IDENTITY設定する必要があります。
    
STATUS_OWN_STORE 
  
> 静的。 このトランスポート プロバイダーは、メッセージ ストアと密に結合され、PR_OWN_STORE_ENTRYID **(** [PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) プロパティを状態行に指定します。
    
STATUS_PRIMARY_IDENTITY 
  
> 変更可能。 このプロバイダーは、セッションのプライマリ ID を提供します。ID を提供するオブジェクトのエントリ識別子は [IMAPISession::QueryIdentity から返されます](imapisession-queryidentity.md)。 このフラグ **または設定STATUS_NO_PRIMARY_IDENTITY** 設定する必要があります。 
    
STATUS_PRIMARY_STORE 
  
> 変更可能。 このメッセージ ストアは、クライアント アプリケーションがログオンするときに使用されます。 開いた後、このストアをプロファイルの既定のストアとして設定する必要があります。 
    
STATUS_SECONDARY_STORE 
  
> 変更可能。 このメッセージ ストアは、クライアント アプリケーションのログオン時にプライマリ ストアが使用できない場合に使用します。 開いた後、このストアをプロファイルの既定のストアとして設定する必要があります。 
    
STATUS_SIMPLE_STORE 
  
> 動的。 このメッセージ ストアは、簡易 MAPI が既定のメッセージ ストアとして使用します。
    
STATUS_TEMP_SECTION 
  
> 動的。 このメッセージ ストアは、メッセージ ストア テーブルに発行し、ログオフ後にプロファイルから削除される必要があります。 
    
STATUS_XP_PREFER_LAST 
  
> 静的。 このトランスポートは、複数のトランスポート プロバイダーがメッセージを送信できる場合に、メッセージを送信するために選択された最後のトランスポートである必要があります。
    
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)
  
[PidTagIdentityEntryId 標準プロパティ](pidtagidentityentryid-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

