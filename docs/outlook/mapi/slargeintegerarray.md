---
title: SLargeIntegerArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLargeIntegerArray
api_type:
- COM
ms.assetid: 9ec9a674-c1a2-4137-856f-6cabe6f0eb9f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 4d6785783f69857bd93f3c5818983e832e16af05
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803951"
---
# <a name="slargeintegerarray"></a>SLargeIntegerArray

  
  
**適用対象**: Outlook 
  
PT_MV_I8 の種類のプロパティを説明するために使用する[LARGE_INTEGER](http://go.microsoft.com/fwlink/?LinkId=132130)構造体の配列が含まれています。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SLargeIntegerArray
{
  ULONG cValues;
  LARGE_INTEGER FAR *lpli;
} SLargeIntegerArray;

```

## <a name="members"></a>Members

 **あう**
  
> **Lpli**メンバーが指す配列内の値の数です。 
    
 **lpli**
  
> 整数値を保持している**LARGE_INTEGER**構造体の配列へのポインター。 
    
## <a name="remarks"></a>注釈

PT_MV_18 の詳細については、[プロパティの種類の一覧](property-types.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

