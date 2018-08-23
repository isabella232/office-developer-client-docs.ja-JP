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
ms.openlocfilehash: bbced8412c2c3438c58af74ef072a46606b59ddc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594615"
---
# <a name="sizedspropproblemarray"></a>SizedSPropProblemArray

**適用されます**: Outlook 2013 |Outlook 2016 
  
[SPropProblem](spropproblem.md)構造体の指定した数値を含む名前付き[SPropProblemArray](spropproblemarray.md)構造体を作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連の構造体。  <br/> |**SPropProblemArray** <br/> |
   
```cpp
SizedSPropProblemArray(_cprob, _name)
```

## <a name="parameters"></a>パラメーター

__cprob_
  
> 新しい構造体に含まれる**SPropProblem**構造体の数です。 
    
__名_
  
> 新しい構造体の名前です。
    
## <a name="remarks"></a>注釈

**SizedSPropProblemArray**マクロを使用すると、明示的な境界を持つプロパティの問題の配列を作成します。 **SPropProblemArray**構造体へのポインターとしての**SizedSPropProblemArray**マクロの結果を新しい構造体を使用するには、次のキャストを実行します。 
  
```cpp
lpPropProbArray = (LPSPropProblemArray) &SizedSPropProblemArray;
```

## <a name="see-also"></a>関連項目

- [SPropProblemArray](spropproblemarray.md)
- [SPropProblem](spropproblem.md)
- [構造体に関連するマクロ](macros-related-to-structures.md)

