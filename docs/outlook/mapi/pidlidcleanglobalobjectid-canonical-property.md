---
title: PidLidCleanGlobalObjectId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidCleanGlobalObjectId
api_type:
- COM
ms.assetid: 59b85997-7972-492e-9786-3f0f367dc3e3
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a81d6e0011ba6d4c873cc9eeef3bf81212faec09
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59555896"
---
# <a name="pidlidcleanglobalobjectid-canonical-property"></a>PidLidCleanGlobalObjectId 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クリーン グローバル **ObjectID を指定します**。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidCleanGlobalObjId  <br/> |
|プロパティ セット:  <br/> |PSETID_Meeting  <br/> |
|長い ID (LID):  <br/> |0x00000023  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |会議  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティの形式は、 ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md) **)** LID_GLOBAL_OBJIDと同じです。 このプロパティの値は、YH、YL、M、および D フィールド **を** 除き、LID_GLOBAL_OBJID の値と等しくする必要があります。 定期的な系列のインスタンス (孤立したインスタンスを含む) と定期的な系列自体を参照するオブジェクトはすべて、このプロパティの値が同じになります。
  
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

