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
ms.openlocfilehash: b8521172b441bd26a6562aa28f836d453544928f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803927"
---
# <a name="sizedspropproblemarray"></a>SizedSPropProblemArray

**適用対象**: Outlook 
  
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

