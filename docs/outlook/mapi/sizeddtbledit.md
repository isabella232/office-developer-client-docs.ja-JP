---
title: SizedDtblEdit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SizedDtblEdit
api_type:
- COM
ms.assetid: a658d027-03a2-4cde-bf99-563e8521cb31
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 22ff75605b9ab7911f0a270a17631f8261b54ffc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566683"
---
# <a name="sizeddtbledit"></a>SizedDtblEdit

**適用対象**: Outlook 2013 | Outlook 2016 
  
編集コントロールを記述するための [DTBLEDIT](dtbledit.md) 構造と、コントロールに入力できる最大文字数を含む名前付き構造を作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連する構造:  <br/> |**DTBLEDIT** <br/> |
   
```cpp
SizedDtblEdit (n, u)
```

## <a name="parameters"></a>パラメーター

_n_
  
> 編集コントロールに入力できる最大文字数。
    
_u_
  
> 新しい構造の名前。
    
## <a name="remarks"></a>注釈

**SizedDtblEdit マクロ** を使用すると、有効な文字の数が分かっているときに編集コントロールを定義できます。 新しい構造は、次のメンバーで作成されます。 
  
```cpp
DTBLEDIT dtbledit;
TCHAR lpszCharsAllowed[n];

```

**SizedDtblEdit** マクロから生成される構造へのポインターを **DTBLEDIT** 構造ポインターとして使用するには、次のキャストを実行します。 
  
```cpp
lpDtblEdit = (LPDTBLEDIT) &SizedDtblEdit;

```

## <a name="see-also"></a>関連項目

- [DTBLEDIT](dtbledit.md)
- [構造に関連するマクロ](macros-related-to-structures.md)

