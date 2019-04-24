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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b3818e5e1429c7e2b7d5f7533db733ba29e672c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282692"
---
# <a name="sizedspropproblemarray"></a>SizedSPropProblemArray

**適用対象**: Outlook 2013 | Outlook 2016 
  
指定した数の[sprop問題](spropproblem.md)構造体を含む名前付き[sprop問題の配列](spropproblemarray.md)構造を作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|関連する構造:  <br/> |**SPropProblemArray** <br/> |
   
```cpp
SizedSPropProblemArray(_cprob, _name)
```

## <a name="parameters"></a>パラメーター

__cprob_
  
> 新しい構造に含めることができる**spropproblem**構造の数。 
    
__名前_
  
> 新しい構造の名前を指定します。
    
## <a name="remarks"></a>解説

**sizedsprop問題の配列**マクロを使用して、明示的な境界を持つプロパティ問題の配列を作成します。 **sizedspropの配列**マクロの結果として得られる新しい構造を、 **spropの配列**構造体へのポインターとして使用するには、次のキャストを実行します。 
  
```cpp
lpPropProbArray = (LPSPropProblemArray) &SizedSPropProblemArray;
```

## <a name="see-also"></a>関連項目

- [SPropProblemArray](spropproblemarray.md)
- [SPropProblem](spropproblem.md)
- [構造に関連するマクロ](macros-related-to-structures.md)

