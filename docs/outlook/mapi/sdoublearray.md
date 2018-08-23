---
title: SDoubleArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SDoubleArray
api_type:
- COM
ms.assetid: b63b26de-faf9-453c-ab8b-fb703ed09ae8
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: cde59b73381458533910dc8f0a728cc4e6ca0c01
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803853"
---
# <a name="sdoublearray"></a>SDoubleArray

  
  
**適用対象**: Outlook 
  
PT_MV_DOUBLE の種類のプロパティを説明するために使用する double 値の配列が含まれています。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SDoubleArray
{
  ULONG cValues;
  double FAR *lpdbl;
} SDoubleArray;

```

## <a name="members"></a>Members

 **あう**
  
> **Lpdbl**メンバーが指す配列内の値の数です。 
    
 **lpdbl**
  
> Double 値の配列へのポインター。
    
## <a name="remarks"></a>注釈

PT_MV_DOUBLE の詳細については、[プロパティの種類の一覧](property-types.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

