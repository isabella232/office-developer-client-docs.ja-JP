---
title: PidTagDeliveryPoint 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDeliveryPoint
api_type:
- HeaderDef
ms.assetid: 715a9dbd-78f8-41e1-a76e-29448d06ec19
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 736d98fd779d9e22553ac076f7f6a4deaacc1597
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566739"
---
# <a name="pidtagdeliverypoint-canonical-property"></a>PidTagDeliveryPoint 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージが受信者に配信された、または配信された可能性のある機能エンティティの性質を指定します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DELIVERY_POINT  <br/> |
|識別子:  <br/> |0x0C07  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI 受信者  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティには、次のいずれかの値を指定できます。 
  
MAPI_MH_DP_ML 
  
> 配布リストに配信され、配信ポイントがメッセージを多くの受信者に配布する可能性があります。
    
MAPI_MH_DP_MS 
  
> 受信者に直接配信されるのではなく、メッセージ ストアに配信されます。
    
MAPI_MH_DP_OTHER_AU 
  
> FAX システムなどの物理配信アクセス ユニット (PDAU) 以外のアクセス ユニット (AU) に配信されます。
    
MAPI_MH_DP_PDAU 
  
> 人間の郵便運送業者などの物理的な配信アクセス ユニットに配信されます。
    
MAPI_MH_DP_PDS_PATRON 
  
> 従来の郵便メールボックスなどの物理的な配信システムのパトロンに配信されます。
    
MAPI_MH_DP_PRIVATE_UA 
  
> プライベート ユーザー エージェント (UA) (インハウス メッセージング システムのクライアントなど) に配信されます。
    
MAPI_MH_DP_PUBLIC_UA 
  
> パブリック ユーザー エージェントまたはパブリック サービス プロバイダーに配信されます。
    
既定値は、mapi MAPI_MH_DP_PRIVATE_UA MAPI クライアントの値です。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

