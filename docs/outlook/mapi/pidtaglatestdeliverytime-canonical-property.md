---
title: PidTagLatestDeliveryTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagLatestDeliveryTime
api_type:
- HeaderDef
ms.assetid: 6c2e64bc-786e-4867-a504-46f4d1214337
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3640ec4471b72dea81d56cc2c462ef145095480f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590926"
---
# <a name="pidtaglatestdeliverytime-canonical-property"></a>PidTagLatestDeliveryTime 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
最新の日付と時刻のメッセージ転送エージェント (MTA) がメッセージを配信する場合が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_LATEST_DELIVERY_TIME  <br/> |
|識別子:  <br/> |0x0019  <br/> |
|データの種類 :   <br/> |PT_SYSTIME  <br/> |
|領域:  <br/> |メッセージ全般  <br/> |
   
## <a name="remarks"></a>注釈

MTA は、このプロパティは、指定の時間でメッセージを配信することはできません、する場合は、メッセージを配信せずをキャンセルします。 
  
## <a name="related-resources"></a>関連リソース

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

