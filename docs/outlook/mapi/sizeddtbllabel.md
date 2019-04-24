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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 1ae675d1d4adf841e18bbfc8990913136afe8b4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282706"
---
# <a name="sizeddtbllabel"></a>SizedDtblLabel

**適用対象**: Outlook 2013 | Outlook 2016 
  
ラベルコントロールと、指定した長さの関連付けられたラベルを記述するための[dtbllabel](dtbllabel.md)構造を含む名前付き構造を作成します。 
  
|||
|:-----|:-----|
|ヘッダーファイルで指定します。  <br/> |mapidefs.h  <br/> |
|関連する構造  <br/> |**DTBLLABEL** <br/> |
   
```cpp
SizedDtblLabel (n, u)
```

## <a name="parameters"></a>パラメーター

_n_
  
> ラベルの長さ。 これには、末尾の NULL 文字が含まれます。 
    
_u_
  
> 新しい構造の名前を指定します。
    
## <a name="remarks"></a>解説

**sizeddtbllabel**マクロを使用すると、ラベル内の文字数が既知の場合に、表示テーブルのラベルを定義できます。 次のメンバーで新しい構造が作成されます。 
  
```cpp
DTBLLABEL dtbllabel;
TCHAR lpszLabelName[n];
```

結果の構造体へのポインターを、 **sizeddtbllabel**マクロから**dtbllabel**構造体へのポインターとして使用するには、次のキャストを実行します。 
  
```cpp
lpDtblLabel = (LPDTBLLABEL) &SizedDtblLabel;
```

## <a name="see-also"></a>関連項目

- [DTBLLABEL](dtbllabel.md)
- [構造に関連するマクロ](macros-related-to-structures.md)

