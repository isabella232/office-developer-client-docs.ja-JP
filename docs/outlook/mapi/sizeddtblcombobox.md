---
title: SizedDtblComboBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblComboBox
api_type:
- COM
ms.assetid: 1e5ea9f2-1029-4584-845a-890d3e956036
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8861c8f86eaab6defb270b673e0ee200446aedb3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416266"
---
# <a name="sizeddtblcombobox"></a>SizedDtblComboBox
 
**適用対象**: Outlook 2013 | Outlook 2016 
  
コンボ ボックス コントロールを記述するための [DTBLCOMBOBOX](dtblcombobox.md) 構造と、関連付けられた編集コントロールに入力できる最大文字数を含む名前付き構造を作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連する構造:  <br/> |**DTBLCOMBOBOX** <br/> |
   
```cpp
SizedDtblComboBox (n, u)
```

## <a name="parameters"></a>パラメーター

_n_
  
> コンボ ボックスの編集コントロールに入力できる文字数。 
    
_u_
  
> 新しい構造の名前。
    
## <a name="remarks"></a>注釈

**SizedDtblComboBox** マクロを使用すると、有効な文字列の長さが分かっているときにコンボ ボックスを定義できます。 新しい構造は、次のメンバーで作成されます。 
  
```cpp
DTBLCOMBOBOX dtblcombobox;
TCHAR lpszCharsAllowed[n];

```

**SizedDtblComboBox** マクロから生成される構造体へのポインターを **DTBLCOMBOBOX** 構造体ポインターとして使用するには、次のキャストを実行します。 
  
```cpp
lpDtblComboBox = (LPDTBLCOMBOBOX) &SizedDtblComboBox;

```

## <a name="see-also"></a>関連項目

- [DTBLCOMBOBOX](dtblcombobox.md)
- [構造に関連するマクロ](macros-related-to-structures.md)

