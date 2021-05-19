---
title: PidLidTimeZoneDescription 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTimeZoneDescription
api_type:
- COM
ms.assetid: 24cb6429-1276-45f1-be0e-6c9d2ff6ce19
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ef68da1723a87fa30861eca5668ee94707f43c8a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351149"
---
# <a name="pidlidtimezonedescription-canonical-property"></a>PidLidTimeZoneDescription 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
タイム ゾーンの文字列の説明を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidTimeZoneDesc  <br/> |
|プロパティ セット:  <br/> |PSETID_Appointment  <br/> |
|長い ID (LID):  <br/> |0x00008234  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|エリア:  <br/> |カレンダー  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは **、dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)) プロパティのデータで表されるタイム ゾーンの人間が読み取り可能な説明を指定します。
  
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

