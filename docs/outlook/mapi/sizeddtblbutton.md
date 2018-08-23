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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: dc4d3a7a827e728dfd6725ac269350067d4530cb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590345"
---
# <a name="sizeddtblbutton"></a>SizedDtblButton

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
ボタンと指定された長さのラベルを記述するための[DTBLBUTTON](dtblbutton.md)構造体を含む名前付き構造体を作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連の構造体。  <br/> |**DTBLBUTTON** <br/> |
   
```cpp
SizedDtblButton (n, u)
```

## <a name="parameters"></a>パラメーター

 _n_
  
> 新しい構造体に含まれるラベルの長さです。
    
 _u_
  
> 新しい構造体の名前です。
    
## <a name="remarks"></a>注釈

新しい構造体は、次のメンバーで作成されます。
  
```
DTBLBUTTON dtblbutton;
TCHAR lpszLabel[n];

```

## <a name="see-also"></a>関連項目



[DTBLBUTTON](dtblbutton.md)


[構造体に関連するマクロ](macros-related-to-structures.md)

