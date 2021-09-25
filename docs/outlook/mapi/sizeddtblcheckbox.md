---
title: SizedDtblCheckBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SizedDtblCheckBox
api_type:
- COM
ms.assetid: 9d04a124-54d4-43ac-967f-ea8e7a09b1d0
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9282562032279ab11a36d0ed1687ccd1d1ae8365
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586727"
---
# <a name="sizeddtblcheckbox"></a>SizedDtblCheckBox
 
**適用対象**: Outlook 2013 | Outlook 2016 
  
チェック ボックス コントロールと指定した長さのラベルを記述するための [DTBLCHECKBOX](dtblcheckbox.md) 構造体を含む名前付き構造を作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連する構造:  <br/> |**DTBLCHECKBOX** <br/> |
   
```cpp
SizedDtblCheckBox (n, u)
```

## <a name="parameters"></a>パラメーター

_n_
  
> 新しい構造に含めるラベルの長さ。
    
_u_
  
> 新しい構造の名前。
    
## <a name="remarks"></a>注釈

**SizedDtblCheckBox** マクロを使用すると、ラベル文字の数が分かっている場合にチェック ボックスを定義できます。 新しい構造は、次のメンバーで作成されます。 
  
```cpp
DTBLCHECKBOX dtblcheckbox;
TCHAR lpszLabel[n];
```

**SizedDtblCheckBox** マクロから生成される構造体へのポインターを **DTBLCHECKBOX** 構造ポインターとして使用するには、次のキャストを実行します。 
  
```cpp
lpDtblCheckBox = (LPDTBLCHECKBOX) &SizedDtblCheckBox;
```

## <a name="see-also"></a>関連項目

- [DTBLCHECKBOX](dtblcheckbox.md)
- [構造に関連するマクロ](macros-related-to-structures.md)

