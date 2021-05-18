---
title: SizedDtblLabel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblLabel
api_type:
- COM
ms.assetid: c7cb8cf9-7abd-4ee3-b88c-d61695f4ed31
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 1ae675d1d4adf841e18bbfc8990913136afe8b4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408615"
---
# <a name="sizeddtbllabel"></a>SizedDtblLabel

**適用対象**: Outlook 2013 | Outlook 2016 
  
ラベル コントロールと指定した長さの関連付けられたラベルを記述するための [DTBLLABEL](dtbllabel.md) 構造を含む名前付き構造を作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイルで指定します。  <br/> |Mapidefs.h  <br/> |
|関連する構造  <br/> |**DTBLLABEL** <br/> |
   
```cpp
SizedDtblLabel (n, u)
```

## <a name="parameters"></a>パラメーター

_n_
  
> ラベルの長さ。 これには、終了 NULL 文字が含まれます。 
    
_u_
  
> 新しい構造の名前。
    
## <a name="remarks"></a>注釈

**SizedDtblLabel** マクロを使用すると、ラベルの文字数が分かっているときに表示テーブル ラベルを定義できます。 新しい構造は、次のメンバーで作成されます。 
  
```cpp
DTBLLABEL dtbllabel;
TCHAR lpszLabelName[n];
```

**SizedDtblLabel** マクロから生成される構造へのポインターを **DTBLLABEL** 構造体ポインターとして使用するには、次のキャストを実行します。 
  
```cpp
lpDtblLabel = (LPDTBLLABEL) &SizedDtblLabel;
```

## <a name="see-also"></a>関連項目

- [DTBLLABEL](dtbllabel.md)
- [構造に関連するマクロ](macros-related-to-structures.md)

