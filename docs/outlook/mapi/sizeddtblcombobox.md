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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8861c8f86eaab6defb270b673e0ee200446aedb3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282825"
---
# <a name="sizeddtblcombobox"></a>SizedDtblComboBox
 
**適用対象**: Outlook 2013 | Outlook 2016 
  
コンボボックスコントロールを記述するための[dtblcombobox](dtblcombobox.md)構造体と、関連する編集コントロールに入力できる最大文字数を含む名前付き構造を作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|関連する構造:  <br/> |**DTBLCOMBOBOX** <br/> |
   
```cpp
SizedDtblComboBox (n, u)
```

## <a name="parameters"></a>パラメーター

_n_
  
> コンボボックスの [編集] コントロールに入力できる文字数を指定します。 
    
_u_
  
> 新しい構造の名前を指定します。
    
## <a name="remarks"></a>解説

**sizeddtblcombobox**マクロを使用すると、有効な文字列の長さが既知の場合にコンボボックスを定義できます。 次のメンバーで新しい構造が作成されます。 
  
```cpp
DTBLCOMBOBOX dtblcombobox;
TCHAR lpszCharsAllowed[n];

```

**sizeddtblcombobox**マクロの結果として得られる構造体へのポインターを**dtblcombobox**構造体のポインターとして使用するには、次のキャストを実行します。 
  
```cpp
lpDtblComboBox = (LPDTBLCOMBOBOX) &SizedDtblComboBox;

```

## <a name="see-also"></a>関連項目

- [DTBLCOMBOBOX](dtblcombobox.md)
- [構造に関連するマクロ](macros-related-to-structures.md)

