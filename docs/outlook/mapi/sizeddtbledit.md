---
title: SizedDtblEdit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblEdit
api_type:
- COM
ms.assetid: a658d027-03a2-4cde-bf99-563e8521cb31
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b5b9c42d944ad9d3ce92e99d08d29964944c8028
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437645"
---
# <a name="sizeddtbledit"></a>SizedDtblEdit

**適用対象**: Outlook 2013 | Outlook 2016 
  
編集コントロールを記述するための[DTBLEDIT](dtbledit.md)構造体と、コントロールに入力できる最大文字数を含む名前付き構造を作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|関連する構造:  <br/> |**DTBLEDIT** <br/> |
   
```cpp
SizedDtblEdit (n, u)
```

## <a name="parameters"></a>パラメーター

_n_
  
> 編集コントロールに入力できる最大文字数。
    
_u_
  
> 新しい構造の名前を指定します。
    
## <a name="remarks"></a>注釈

**SizedDtblEdit**マクロを使用すると、有効な文字数が既知の場合に編集コントロールを定義できます。 次のメンバーで新しい構造が作成されます。 
  
```cpp
DTBLEDIT dtbledit;
TCHAR lpszCharsAllowed[n];

```

**SizedDtblEdit**マクロの結果として得られる構造体へのポインターを**DTBLEDIT**構造体ポインターとして使用するには、次のキャストを実行します。 
  
```cpp
lpDtblEdit = (LPDTBLEDIT) &SizedDtblEdit;

```

## <a name="see-also"></a>関連項目

- [DTBLEDIT](dtbledit.md)
- [構造に関連するマクロ](macros-related-to-structures.md)

