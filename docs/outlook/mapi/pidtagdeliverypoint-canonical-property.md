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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2d8157c761cd21d5c8fcdf04948646d8102e774a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580139"
---
# <a name="pidtagdeliverypoint-canonical-property"></a>PidTagDeliveryPoint 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
使用して、メッセージまたは受信者に配信されるように機能エンティティの種類を指定します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DELIVERY_POINT  <br/> |
|識別子:  <br/> |0x0C07  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|領域:  <br/> |MAPI 受信者  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、次の値の 1 つだけ持つことができます。 
  
MAPI_MH_DP_ML 
  
> 配布リストに配信、配信は、先に配布することが多くの受信者にメッセージをポイントします。
    
MAPI_MH_DP_MS 
  
> 代わりに、受信者に直接のメッセージ ・ ストアに配信されます。
    
MAPI_MH_DP_OTHER_AU 
  
> FAX システムなどの物理的な配信アクセス ユニット (PDAU)、以外のアクセス単位 (AU) に配信されます。
    
MAPI_MH_DP_PDAU 
  
> 人間の郵便キャリアなどの物理的な配信アクセス ユニットに配信されます。
    
MAPI_MH_DP_PDS_PATRON 
  
> 従来の郵便番号のメールボックスなどの物理的な配信システムの patron に配信されます。
    
MAPI_MH_DP_PRIVATE_UA 
  
> 社内メッセージング システム内のクライアントなど、プライベートなユーザー エージェント (UA) に配信されます。
    
MAPI_MH_DP_PUBLIC_UA 
  
> パブリックのユーザー エージェント、またはサービス プロバイダーに提供します。
    
既定値は、MAPI_MH_DP_PRIVATE_UA、つまり、MAPI クライアントです。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

