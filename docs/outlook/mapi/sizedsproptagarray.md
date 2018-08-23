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
ms.openlocfilehash: 7505c5dbcfc98a8b868424ae51cbe9c47b1d4338
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803930"
---
# <a name="sizedsproptagarray"></a>SizedSPropTagArray

**適用対象**: Outlook 
  
プロパティ タグの指定された番号を格納する名前付きの[SPropTagArray](sproptagarray.md)構造を作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連の構造体。  <br/> |**SPropTagArray** <br/> |
   
```cpp
SizedSPropTagArray (_ctag, _name)
```

## <a name="parameters"></a>パラメーター

__ctag_
  
> 新しい構造体に含まれるプロパティ タグの数。
    
__名_
  
> 新しい構造体の名前です。
    
## <a name="remarks"></a>注釈

**SizedSPropTagArray**マクロを使用すると、明示的な境界を持つプロパティ タグ配列を作成します。 
  
**SPropTagArray**構造体へのポインターとしての**SizedSPropTagArray**マクロの結果を新しい構造体を使用するには、次のキャストを実行します。 
  
```cpp
lpPropTagArray = (LPPropTagArray) &SizedSPropTagArray;

```

## <a name="see-also"></a>関連項目

- [SPropTagArray](sproptagarray.md)
- [構造体に関連するマクロ](macros-related-to-structures.md)

