---
title: PidLidCleanGlobalObjectId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCleanGlobalObjectId
api_type:
- COM
ms.assetid: 59b85997-7972-492e-9786-3f0f367dc3e3
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 38442b763ec97969f73b11b346d638d547302715
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589001"
---
# <a name="pidlidcleanglobalobjectid-canonical-property"></a>PidLidCleanGlobalObjectId 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
クリーンなグローバル**オブジェクト Id**を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidCleanGlobalObjId  <br/> |
|プロパティを設定します。  <br/> |PSETID_Meeting  <br/> |
|長い ID (LID):  <br/> |0x00000023  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|領域:  <br/> |会議  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティの形式は、 **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) のものと同じです。 このプロパティの値は、 **LID_GLOBAL_OBJID**YH、YL、M 以外の値に等しいである必要があり、D のフィールドは 0 である必要があります。 自体には、定期的な系列だけでなく、(孤立したインスタンスを含む)、定期的な系列のインスタンスを参照するすべてのオブジェクトには、このプロパティに対して同じ値があります。
  
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

