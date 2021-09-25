---
title: SizedDtblButton
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SizedDtblButton
api_type:
- COM
ms.assetid: ee73ced9-14d8-4a30-9b9f-d54ed9c3a454
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f5794df4df73d199bf7b0acfc91cc111b0d783b3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578642"
---
# <a name="sizeddtblbutton"></a>SizedDtblButton

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ボタンと指定した長さのラベルを記述するための [DTBLBUTTON](dtblbutton.md) 構造を含む名前付き構造を作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連する構造:  <br/> |**DTBLBUTTON** <br/> |
   
```cpp
SizedDtblButton (n, u)
```

## <a name="parameters"></a>パラメーター

 _n_
  
> 新しい構造に含めるラベルの長さ。
    
 _u_
  
> 新しい構造の名前。
    
## <a name="remarks"></a>注釈

新しい構造は、次のメンバーで作成されます。
  
```
DTBLBUTTON dtblbutton;
TCHAR lpszLabel[n];

```

## <a name="see-also"></a>関連項目



[DTBLBUTTON](dtblbutton.md)


[構造に関連するマクロ](macros-related-to-structures.md)

