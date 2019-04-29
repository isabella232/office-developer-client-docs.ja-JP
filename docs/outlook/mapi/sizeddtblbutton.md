---
title: SizedDtblButton
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblButton
api_type:
- COM
ms.assetid: ee73ced9-14d8-4a30-9b9f-d54ed9c3a454
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a7d62d29638ae234667eb33a8103fb3a716afc32
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421915"
---
# <a name="sizeddtblbutton"></a>SizedDtblButton

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ボタンと指定された長さのラベルを記述するための[dtblbutton](dtblbutton.md)構造を含む名前付き構造を作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|関連する構造:  <br/> |**DTBLBUTTON** <br/> |
   
```cpp
SizedDtblButton (n, u)
```

## <a name="parameters"></a>パラメーター

 _n_
  
> 新しい構造に含めるラベルの長さ。
    
 _u_
  
> 新しい構造の名前を指定します。
    
## <a name="remarks"></a>注釈

次のメンバーで新しい構造が作成されます。
  
```
DTBLBUTTON dtblbutton;
TCHAR lpszLabel[n];

```

## <a name="see-also"></a>関連項目



[DTBLBUTTON](dtblbutton.md)


[構造に関連するマクロ](macros-related-to-structures.md)

