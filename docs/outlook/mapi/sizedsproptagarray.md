---
title: SizedSPropTagArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSPropTagArray
api_type:
- COM
ms.assetid: 1d2dc6e9-735d-4b5b-af6f-adf6a32a666d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f873ad5234460f9f1781c7427b60d285f7486196
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282699"
---
# <a name="sizedsproptagarray"></a>SizedSPropTagArray

**適用対象**: Outlook 2013 | Outlook 2016 
  
指定した数のプロパティタグを含む名前付きの[SPropTagArray](sproptagarray.md)構造を作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|関連する構造:  <br/> |**SPropTagArray** <br/> |
   
```cpp
SizedSPropTagArray (_ctag, _name)
```

## <a name="parameters"></a>パラメーター

__ctag_
  
> 新しい構造に含めるプロパティタグの数。
    
__名前_
  
> 新しい構造の名前を指定します。
    
## <a name="remarks"></a>解説

**SizedSPropTagArray**マクロを使用して、明示的な境界を持つプロパティタグ配列を作成します。 
  
**SizedSPropTagArray**マクロの結果として得られる新しい構造を**SPropTagArray**構造体へのポインターとして使用するには、次のキャストを実行します。 
  
```cpp
lpPropTagArray = (LPPropTagArray) &SizedSPropTagArray;

```

## <a name="see-also"></a>関連項目

- [SPropTagArray](sproptagarray.md)
- [構造に関連するマクロ](macros-related-to-structures.md)

