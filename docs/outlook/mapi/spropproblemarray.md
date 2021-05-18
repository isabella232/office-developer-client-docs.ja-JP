---
title: SPropProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropProblemArray
api_type:
- COM
ms.assetid: 3fbaa77a-be43-4fce-af67-1826ee101799
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f78e0ed939e190a9855ea4b040d18c01cfecc91d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406858"
---
# <a name="spropproblemarray"></a>SPropProblemArray

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
1 つ以上の [SPropProblem 構造体の配列を格納](spropproblem.md) します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連するマクロ:  <br/> |[CbNewSPropProblemArray](cbnewspropproblemarray.md) <br/> [CbSPropProblemArray](cbspropproblemarray.md) <br/> [SizedSPropProblemArray](sizedspropproblemarray.md) <br/> |
   
```cpp
typedef struct _SPropProblemArray
{
  ULONG cProblem;
  SPropProblem aProblem[MAPI_DIM];
} SPropProblemArray, FAR *LPSPropProblemArray;

```

## <a name="members"></a>Members

 **cProblem**
  
> [aProblem メンバーによって示](spropproblem.md)される配列内の **SPropProblem** 構造体の数。 
    
 **aProblem**
  
> プロパティ エラー **を記述する SPropProblem** 構造体の配列。 
    
## <a name="remarks"></a>注釈

**SPropProblem** 構造体と **SPropProblemArray** 構造体がプロパティに関連するエラーを処理する方法の詳細については、「MAPI 名前付きプロパティ」[を参照してください](mapi-named-properties.md)。 
  
## <a name="see-also"></a>関連項目



[SCODE](scode.md)
  
[SPropProblem](spropproblem.md)


[MAPI の構造](mapi-structures.md)

