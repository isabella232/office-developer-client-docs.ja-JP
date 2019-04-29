---
title: PidTagDeliveryPoint 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeliveryPoint
api_type:
- HeaderDef
ms.assetid: 715a9dbd-78f8-41e1-a76e-29448d06ec19
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e18b08bcbd76cacf7dbb5b5fd36d80d5f266364d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439423"
---
# <a name="pidtagdeliverypoint-canonical-property"></a>PidTagDeliveryPoint 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
機能エンティティの性質を指定します。これにより、メッセージが受信者に配信されたかどうかを指定します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DELIVERY_POINT  <br/> |
|識別子:  <br/> |0x0c07  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI 受信者  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティには、次のいずれかの値を指定できます。 
  
MAPI_MH_DP_ML 
  
> 配布リストに配信されます。この配信ポイントによって、メッセージが多数の受信者に配布される場合があります。
    
MAPI_MH_DP_MS 
  
> 受信者に直接配信される代わりに、メッセージストアに配信されます。
    
MAPI_MH_DP_OTHER_AU 
  
> FAX システムなどの物理的な配信アクセス装置 (pdau) 以外のアクセスユニット (au) に配信されます。
    
MAPI_MH_DP_PDAU 
  
> ユーザーは、実際の郵便電話会社などの物理的な配信アクセス単位に配信されます。
    
MAPI_MH_DP_PDS_PATRON 
  
> 従来の郵便メールボックスのような、物理的な配信システムの場合に送信されます。
    
MAPI_MH_DP_PRIVATE_UA 
  
> 社内メッセージングシステムのクライアントなど、プライベートユーザーエージェント (UA) に配信されます。
    
MAPI_MH_DP_PUBLIC_UA 
  
> パブリックユーザーエージェントまたはパブリックサービスプロバイダに配信されます。
    
既定値は MAPI_MH_DP_PRIVATE_UA です。つまり、MAPI クライアントです。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 関連するプロパティとしてリストされているプロパティの定義が含まれます。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

