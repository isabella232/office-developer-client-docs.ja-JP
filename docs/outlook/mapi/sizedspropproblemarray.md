---
title: SizedSPropProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSPropProblemArray
api_type:
- COM
ms.assetid: 2fc3febb-8c69-4315-a112-a28eee98013d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b3818e5e1429c7e2b7d5f7533db733ba29e672c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418114"
---
# <a name="sizedspropproblemarray"></a>SizedSPropProblemArray

**適用対象**: Outlook 2013 | Outlook 2016 
  
指定した [数の SPropProblem](spropproblemarray.md) 構造体を含む名前付き [SPropProblemArray 構造体を作成](spropproblem.md) します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連する構造:  <br/> |**SPropProblemArray** <br/> |
   
```cpp
SizedSPropProblemArray(_cprob, _name)
```

## <a name="parameters"></a>パラメーター

_ _cprob_
  
> 新しい **構造に含める SPropProblem** 構造体の数。 
    
_ _name_
  
> 新しい構造の名前。
    
## <a name="remarks"></a>注釈

**SizedSPropProblemArray** マクロを使用して、明示的な境界を持つプロパティの問題配列を作成します。 **SizedSPropProblemArray** マクロから得られた新しい構造を **SPropProblemArray** 構造体へのポインターとして使用するには、次のキャストを実行します。 
  
```cpp
lpPropProbArray = (LPSPropProblemArray) &SizedSPropProblemArray;
```

## <a name="see-also"></a>関連項目

- [SPropProblemArray](spropproblemarray.md)
- [SPropProblem](spropproblem.md)
- [構造に関連するマクロ](macros-related-to-structures.md)

