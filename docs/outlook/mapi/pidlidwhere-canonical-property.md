---
title: PidLidWhere 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidWhere
api_type:
- COM
ms.assetid: b21a3aa4-7536-4728-b4a4-273cfb25c57e
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 19c3ed57d2a0bdd6902a93ca5f29deb91418b8ca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360432"
---
# <a name="pidlidwhere-canonical-property"></a>PidLidWhere 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
イベントの場所を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |LID_WHERE  <br/> |
|プロパティセット:  <br/> |PSETID_Meeting  <br/> |
|ロング ID (LID):  <br/> |0x00000002  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|エリア:  <br/> |Meetings  <br/> |
   
## <a name="remarks"></a>解説

このプロパティの値は、関連付けられている会議の**dispidlocation** ([PidLidLocation](pidlidlocation-canonical-property.md)) プロパティの値と同じである必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> 予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

