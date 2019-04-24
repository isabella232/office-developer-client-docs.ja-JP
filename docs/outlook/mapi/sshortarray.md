---
title: SShortArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SShortArray
api_type:
- COM
ms.assetid: 201ceb76-41bc-4d7b-835d-5196bf3dc234
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8ea7d51b15a6e6acd44a3c0b6158378661f311bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344500"
---
# <a name="sshortarray"></a>SShortArray

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
PT_MV_SHORT 型のプロパティを記述するために使用される、符号なし整数値の配列を格納します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
```cpp
typedef struct _SShortArray
{
  ULONG cValues;
  short int FAR *lpi;
} SShortArray;

```

## <a name="members"></a>Members

 **cvalues**
  
> **lpi**メンバーが指す配列内の値の数。 
    
 **lpi**
  
> 符号なし整数値の配列へのポインター。
    
## <a name="remarks"></a>解説

PT_MV_SHORT およびその他のプロパティの種類の詳細については、「[プロパティの種類](property-types.md)」を参照してください。 
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

