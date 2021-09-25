---
title: SizedDtblGroupBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SizedDtblGroupBox
api_type:
- COM
ms.assetid: 7ca01bf7-5185-41cc-907e-01f256345997
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 1a9f5b2d26c4cfaa0232193e1a75ca3a7edca7a7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566676"
---
# <a name="sizeddtblgroupbox"></a>SizedDtblGroupBox

**適用対象**: Outlook 2013 | Outlook 2016 
  
グループ ボックス コントロールと指定した長さのラベルを記述するための [DTBLGROUPBOX](dtblgroupbox.md) 構造体を含む名前付き構造を作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連する構造:  <br/> |**DTBLGROUPBOX** <br/> |
   
```cpp
SizedDtblGroupBox (n, u)
```

## <a name="parameters"></a>パラメーター

_n_
  
> グループ ボックスのラベルの長さ。 
    
_u_
  
> 新しい構造の名前。
    
## <a name="remarks"></a>注釈

**SizedDtblGroupBox** マクロを使用すると、ラベルの長さが分かっているときにグループ ボックス コントロールを定義できます。 新しい構造は、次のメンバーで作成されます。 
  
```cpp
DTBLGROUPBOX dtblgroupbox;
TCHAR lpszLabel[n];

```

**SizedDtblGroupBox** マクロから生成される構造へのポインターを **DTBLGROUPBOX** 構造ポインターとして使用するには、次のキャストを実行します。 
  
```cpp
lpDtblGroupBox = (LPDTBLGROUPBOX) &SizedDtblGroupBox;

```

## <a name="see-also"></a>関連項目

- [DTBLGROUPBOX](dtblgroupbox.md)
- [構造に関連するマクロ](macros-related-to-structures.md)

