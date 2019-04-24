---
title: SizedDtblCheckBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblCheckBox
api_type:
- COM
ms.assetid: 9d04a124-54d4-43ac-967f-ea8e7a09b1d0
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6d23d56a27095497aedc64d7bbf5ffda266d0c97
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282755"
---
# <a name="sizeddtblcheckbox"></a>SizedDtblCheckBox
 
**適用対象**: Outlook 2013 | Outlook 2016 
  
チェックボックスコントロールと指定された長さのラベルを記述するための[dtblcheckbox](dtblcheckbox.md)構造を含む名前付き構造を作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|関連する構造:  <br/> |**DTBLCHECKBOX** <br/> |
   
```cpp
SizedDtblCheckBox (n, u)
```

## <a name="parameters"></a>パラメーター

_n_
  
> 新しい構造に含めるラベルの長さ。
    
_u_
  
> 新しい構造の名前を指定します。
    
## <a name="remarks"></a>解説

**sizeddtblcheckbox**マクロを使用すると、ラベル文字の数が既知の場合にチェックボックスを定義できます。 次のメンバーで新しい構造が作成されます。 
  
```cpp
DTBLCHECKBOX dtblcheckbox;
TCHAR lpszLabel[n];
```

**sizeddtblcheckbox**マクロの結果として得られる構造体へのポインターを**dtblcheckbox**構造体ポインターとして使用するには、次のキャストを実行します。 
  
```cpp
lpDtblCheckBox = (LPDTBLCHECKBOX) &SizedDtblCheckBox;
```

## <a name="see-also"></a>関連項目

- [DTBLCHECKBOX](dtblcheckbox.md)
- [構造に関連するマクロ](macros-related-to-structures.md)

