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
ms.openlocfilehash: c207b1db6a24cc60967735e2f4b1a4aa97007750
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803943"
---
# <a name="slongarray"></a>SLongArray

  
  
**適用対象**: Outlook 
  
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

