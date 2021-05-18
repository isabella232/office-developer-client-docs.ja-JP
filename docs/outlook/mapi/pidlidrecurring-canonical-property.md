---
title: PidLidRecurring 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRecurring
api_type:
- COM
ms.assetid: 3d39a053-277f-4d59-ab2e-cee81710f2ab
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 85e78695a7c4fca5a1e5cd28b0254d4559be0c13
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315919"
---
# <a name="pidlidrecurring-canonical-property"></a>PidLidRecurring 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
予定メッセージが繰り返し表示されるかどうかを指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidRecurring  <br/> |
|プロパティ セット:  <br/> |PSETID_Appointment  <br/> |
|長い ID (LID):  <br/> |0x00008223  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |カレンダー  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、予定が定期的な予定の場合は TRUE、定期的ではない場合は FALSE です。
  
このプロパティは、オブジェクトが定期的な系列を表すかどうかを指定します。 TRUE の値は、オブジェクトが定期的な系列を表します。 FALSE の値、またはこのプロパティがない場合は、オブジェクトが単一のインスタンスまたは例外 (孤立インスタンスを含む) を表します。 このプロパティとプロパティ ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md) **)** プロパティLID_IS_RECURRINGの違いに注意してください。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> 予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

