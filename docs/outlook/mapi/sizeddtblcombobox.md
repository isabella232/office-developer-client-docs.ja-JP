---
title: SizedDtblComboBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SizedDtblComboBox
api_type:
- COM
ms.assetid: 1e5ea9f2-1029-4584-845a-890d3e956036
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 463c8e82ab99d3b58f2f506438bd423a44224c65
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591123"
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

