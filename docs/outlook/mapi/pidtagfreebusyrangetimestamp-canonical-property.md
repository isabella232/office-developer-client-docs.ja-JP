---
title: PidTagFreeBusyRangeTimestamp 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFreeBusyRangeTimestamp
api_type:
- HeaderDef
ms.assetid: 142d955f-f92d-485a-80c9-9c72e82af0f2
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 24c3369d1d6db4977d26e4d31678a4f2cc5808a2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316178"
---
# <a name="pidtagfreebusyrangetimestamp-canonical-property"></a>PidTagFreeBusyRangeTimestamp 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
データが公開された時刻を格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_FREEBUSY_RANGE_TIMESTAMP  <br/> |
|識別子:  <br/> |0x6868  <br/> |
|データの種類 :   <br/> |PT_SYSTIME  <br/> |
|エリア:  <br/> |空き時間情報  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、協定世界時 (UTC) の 1601 年 1 月 1 日午前 0 時からの分数です。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> ユーザーまたはリソースの可用性を公開します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

