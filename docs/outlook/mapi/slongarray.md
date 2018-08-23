---
title: SLongArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLongArray
api_type:
- COM
ms.assetid: 57435634-202d-4998-9931-4562f1a66f5f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a44974accea30b5d1406c9cc74570012f61639e5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580650"
---
# <a name="slongarray"></a>SLongArray

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
PT_MV_LONG の種類のプロパティを説明するために使用する long 型の値型の配列が含まれています。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SLongArray
{
  ULONG cValues;
  LONG FAR *lpl;
} SLongArray;

```

## <a name="members"></a>Members

 **あう**
  
> **Lpl**メンバーが指す配列内の値の数です。 
    
 **lpl**
  
> LONG 値の配列へのポインター。
    
## <a name="remarks"></a>注釈

PT_MV_LONG の詳細については、[プロパティの種類の一覧](property-types.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

