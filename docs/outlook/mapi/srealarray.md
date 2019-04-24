---
title: SRealArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRealArray
api_type:
- COM
ms.assetid: 95be07bf-5732-4775-9e0f-fec47e99d9b7
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8439d6609ebece75699a1150a9d0c1a41277fd52
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344381"
---
# <a name="srealarray"></a>SRealArray

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
PT_MV_R4 型のプロパティを記述するために使用される float 値の配列を格納します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
```cpp
typedef struct _SRealArray
{
  ULONG cValues;
  float FAR *lpflt;
} SRealArray;

```

## <a name="members"></a>Members

 **cvalues**
  
> **lpflt**メンバーが指す配列内の値の数。 
    
 **lpflt**
  
> 浮動小数点型の値の配列へのポインターを指定します。
    
## <a name="remarks"></a>解説

PT_MV_R4 プロパティの種類の詳細については、「[プロパティの種類](property-types.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

