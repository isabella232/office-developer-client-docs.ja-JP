---
title: PidLidIntendedBusyStatus 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidIntendedBusyStatus
api_type:
- COM
ms.assetid: 84221dd3-de71-4c10-abd7-9f15aefd02ed
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 30f1e2389698f5ec96874f46a685a7e087dbb773
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802010"
---
# <a name="pidlidintendedbusystatus-canonical-property"></a>PidLidIntendedBusyStatus 標準プロパティ

  
  
**適用対象**: Outlook 
  
会議出席依頼または会議の更新が送信された場合は、開催者の予定表で会議の**dispidBusyStatus** ([PidLidBusyStatus](pidlidbusystatus-canonical-property.md)) プロパティの値を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidIntendedBusyStatus  <br/> |
|プロパティを設定します。  <br/> |PSETID_Appointment  <br/> |
|長い ID (LID):  <br/> |0x00008224  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|領域:  <br/> |会議  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティで使用できる値は、プロパティ**dispidBusyStatus**の場合と同じです。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

