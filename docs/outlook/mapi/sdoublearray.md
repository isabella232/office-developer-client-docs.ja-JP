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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 91440d619c8ad8a64b2bac7463a26d9c196a3c0f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439269"
---
# <a name="sdoublearray"></a>SDoubleArray

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
型のプロパティを記述するために使用される倍数の配列が含PT_MV_DOUBLE。
  
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

 **cValues**
  
> **lpdbl** メンバーが指す配列内の値の数。 
    
 **lpdbl**
  
> 倍数の値の配列へのポインター。
    
## <a name="remarks"></a>注釈

プロパティの詳細については、「PT_MV_DOUBLEプロパティ [の種類の一覧」を参照してください](property-types.md)。
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

