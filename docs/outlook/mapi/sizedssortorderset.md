---
title: SizedSSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSSortOrderSet
api_type:
- COM
ms.assetid: f0b9c2f4-7011-414d-8e6c-ab22893ef132
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 60a335f85eea8778580e0bd74693a5c28591103c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428607"
---
# <a name="sizedssortorderset"></a>SizedSSortOrderSet

**適用対象**: Outlook 2013 | Outlook 2016 
  
指定した数の並べ替え順序を含む名前付き [SSortOrderSet](ssortorderset.md) 構造体を作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連する構造:  <br/> |**SSortOrderSet** <br/> |
   
```cpp
SizedSSortOrderSet (_csort,_name)
```

## <a name="parameters"></a>パラメーター

_ _csort_
  
> 新しい構造に含める並べ替え順序の数。
    
_ _name_
  
> 新しい構造の名前。
    
## <a name="remarks"></a>注釈

**SizedSSortOrderSet** マクロを使用して、明示的な境界を持つ並べ替え順序セットを作成します。 
  
**SizedSSortOrderSet** マクロから得られた新しい構造を **SSortOrderSet** 構造体へのポインターとして使用するには、次のキャストを実行します。 
  
```cpp
lpSSortOrderSet = (LPSSortOrderSet) &SizedSSortOrderSet;

```

## <a name="see-also"></a>関連項目

- [SSortOrderSet](ssortorderset.md)
- [構造に関連するマクロ](macros-related-to-structures.md)

