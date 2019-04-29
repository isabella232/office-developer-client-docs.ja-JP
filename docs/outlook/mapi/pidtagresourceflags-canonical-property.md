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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2fb9eed0beaf7269ac90a021dae650355484ebc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436231"
---
# <a name="pidtagresourceflags-canonical-property"></a>PidTagResourceFlags 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージサービスとプロバイダーのフラグのビットマスクを含みます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RESOURCE_FLAGS  <br/> |
|識別子:  <br/> |0x3009  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI 共通  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、メッセージサービス、サービスプロバイダー、または status オブジェクトの特性を表します。 このプロパティに設定されているフラグは、そのコンテキストに依存します。 たとえば、一部のフラグは、ステータスオブジェクトと、メッセージサービステーブル内の列の他のフラグにのみ有効です。 
  
フラグには、静的、変更可能、動的の3つのクラスがあります。 静的フラグは、mapisvc.inf のデータから MAPI によって設定されます。INF。変更されません。 変更可能なフラグは、MAPI によって mapisvc.inf から設定されます。INF は後で変更できます。 動的フラグは MAPI メソッドによって設定およびリセットできます。
  
メッセージサービスの場合、このプロパティには次の1つ以上のフラグを設定できます。
  
SERVICE_CREATE_WITH_STORE 
  
> 予約済み。 使用しないでください。
    
SERVICE_DEFAULT_STORE 
  
> な. メッセージサービスには、既定のストアが含まれています。 このサービスをプロファイルから削除または移動する前に、ユーザーに確認を求めるメッセージが表示されます。 
    
SERVICE_NO_PRIMARY_IDENTITY 
  
> 静電気. メッセージサービスのプロバイダーが id の提供に使用できないことを示すために設定する必要があるサービスレベルフラグ。 このフラグまたは SERVICE_PRIMARY_IDENTITY のどちらかを設定する必要がありますが、両方を設定することはできません。
    
SERVICE_PRIMARY_IDENTITY 
  
> 可能. 対応するメッセージサービスには、このセッションのプライマリ id に使用されるプロバイダーが含まれています。 このフラグを設定するには、 [IMsgServiceAdmin:: setprimaryidentity](imsgserviceadmin-setprimaryidentity.md)を使用します。 このフラグまたは SERVICE_NO_PRIMARY_IDENTITY のどちらかを設定する必要がありますが、両方を設定することはできません。 
    
SERVICE_SINGLE_COPY 
  
> 静電気. サービスが既に存在するプロファイルにこのメッセージサービスを作成またはコピーしようとすると、失敗します。 単一コピーのメッセージサービスを作成するには、mapisvc.inf のサービスのセクションに**PR_RESOURCE_FLAGS**プロパティを追加します。INF を設定し、このフラグを設定します。 
    
サービスプロバイダーの場合、 **PR_RESOURCE_FLAGS**には次のフラグのうち1つ以上を設定できます。
  
HOOK_INBOUND 
  
> 静電気. スプーラーフックは、受信メッセージを処理する必要があります。
    
HOOK_OUTBOUND 
  
> 静電気. スプーラーフックは、送信メッセージを処理する必要があります。 
    
STATUS_DEFAULT_OUTBOUND 
  
> 可能. プロファイルにこのトランスポートプロバイダーの複数のインスタンスが含まれている場合は、この id を送信メッセージに適用する必要があります。 これは、1つのトランスポートプロバイダーの複数のインスタンスがプロファイルに表示された場合に発生する可能性があります。
    
STATUS_DEFAULT_STORE 
  
> 可能. このメッセージストアは、プロファイルの既定のストアです。 
    
STATUS_NEED_IPM_TREE 
  
> な. このメッセージストアの標準フォルダー (個人間メッセージ (IPM) ルートフォルダーを含む) はまだ検証されていません。 MAPI は、このフラグを設定してクリアします。 
    
STATUS_NO_DEFAULT_STORE 
  
> 静電気. このメッセージストアは、プロファイルの既定のメッセージストアになることができません。
    
STATUS_NO_PRIMARY_IDENTITY 
  
> 静電気. このプロバイダーは、ステータス行で id を提供しません。 このフラグまたは STATUS_PRIMARY_IDENTITY のいずれかを設定する必要があります。
    
STATUS_OWN_STORE 
  
> 静電気. このトランスポートプロバイダーは、メッセージストアと密に結合されており、そのステータス行の**PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) プロパティを furnishes します。
    
STATUS_PRIMARY_IDENTITY 
  
> 可能. このプロバイダーは、セッションのプライマリ id を furnishes します。id を表すオブジェクトのエントリ識別子は、 [imapisession:: queryidentity](imapisession-queryidentity.md)から返されます。 このフラグまたは**STATUS_NO_PRIMARY_IDENTITY**のいずれかを設定する必要があります。 
    
STATUS_PRIMARY_STORE 
  
> 可能. このメッセージストアは、クライアントアプリケーションがログオンするときに使用されます。 このストアを開くと、プロファイルの既定のストアとしてこのストアを設定する必要があります。 
    
STATUS_SECONDARY_STORE 
  
> 可能. このメッセージストアは、クライアントアプリケーションがログオンしたときにプライマリストアが使用できない場合に使用されます。 このストアを開くと、プロファイルの既定のストアとしてこのストアを設定する必要があります。 
    
STATUS_SIMPLE_STORE 
  
> な. このメッセージストアは、既定のメッセージストアとして簡易 MAPI によって使用されます。
    
STATUS_TEMP_SECTION 
  
> な. このメッセージストアは、メッセージストアテーブルに公開しないでください。ログオフ後にプロファイルから削除されます。 
    
STATUS_XP_PREFER_LAST 
  
> 静電気. このトランスポートは、複数のトランスポートプロバイダーがメッセージを送信できる場合に、メッセージを送信するために選択された最後のトランスポートであると想定します。
    
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)
  
[PidTagIdentityEntryId 標準プロパティ](pidtagidentityentryid-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

