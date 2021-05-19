---
title: SizedSRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSRowSet
api_type:
- COM
ms.assetid: 419e2c6d-ac3b-46c6-9a12-33f51f6d7f12
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: cb1e19a3f3703dc4943a5f6c322f1c8b429da5fa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410932"
---
# <a name="sizedsrowset"></a>SizedSRowSet

**適用対象**: Outlook 2013 | Outlook 2016 
  
指定した行数 [を含む名前付き SRowSet](srowset.md) 構造体を作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連する構造:  <br/> |**SRowSet** <br/> |
   
```cpp
SizedSRowSet (_crow, _name)
```

## <a name="parameters"></a>パラメーター

_ _crow_
  
> 新しい構造に含める行の数。
    
_ _name_
  
> 新しい構造の名前。
    
## <a name="remarks"></a>注釈

**SizedSRowSet** マクロから得られた新しい構造を **SRowSet** 構造体へのポインターとして使用するには、次のキャストを実行します。 
  
```cpp
lpSRowSet = (LPSRowSet) &SizedSRowSet;

```

## <a name="see-also"></a>関連項目

- [SRowSet](srowset.md)
- [構造に関連するマクロ](macros-related-to-structures.md)

