---
title: SizedDtblPage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SizedDtblPage
api_type:
- COM
ms.assetid: 47b2a69d-e902-429f-8b31-166b51aeaf7f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 344403fa1dd4301ab6dee0118d30d23df8c3b1bb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566627"
---
# <a name="sizeddtblpage"></a>SizedDtblPage

**適用対象**: Outlook 2013 | Outlook 2016 
  
タブ付きページ コントロール、指定した長さのラベル、および指定した長さのヘルプ ファイル エントリを記述するための [DTBLPAGE](dtblpage.md) 構造を含む名前付き構造を作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連する構造:  <br/> |**DTBLPAGE** <br/> |
   
```cpp
SizedDtblPage (n, n1, u)
```

## <a name="parameters"></a>パラメーター

_n_
  
> ページ タブのラベルの長さ。
    
_n1_
  
> タブ付きページ コントロールで使用されるヘルプ ファイルを識別する Mapisvc.inf ファイルに表示されるエントリの長さ。
    
_u_
  
> 新しい構造の名前。
    
## <a name="remarks"></a>注釈

**SizedDtblPage** マクロを使用すると、関連付けられたラベルとヘルプ ファイルエントリの文字数が分かっているときに、タブ付きページ コントロールを定義できます。 新しい構造は、次のメンバーで作成されます。 
  
```cpp
DTBLPAGE dtblpage;
TCHAR lpszLabel[n];
TCHAR lpszComponent[n1];
```

**SizedDtblPage** マクロから生成される構造へのポインターを **DTBLPAGE** 構造ポインターとして使用するには、次のキャストを実行します。 
  
```cpp
lpDtblPage = (LPDTBLPAGE) &SizedDtblPage;
```

## <a name="see-also"></a>関連項目

- [DTBLPAGE](dtblpage.md)
- [構造に関連するマクロ](macros-related-to-structures.md)

