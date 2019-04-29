---
title: SizedDtblGroupBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblGroupBox
api_type:
- COM
ms.assetid: 7ca01bf7-5185-41cc-907e-01f256345997
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0a9bda8831f4a38b62d71a54115c40bb3374d97d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419318"
---
# <a name="sizeddtblgroupbox"></a>SizedDtblGroupBox

**適用対象**: Outlook 2013 | Outlook 2016 
  
グループボックスコントロールと指定された長さのラベルを表す[dtblgroupbox](dtblgroupbox.md)構造を含む名前付き構造を作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|関連する構造:  <br/> |**DTBLGROUPBOX** <br/> |
   
```cpp
SizedDtblGroupBox (n, u)
```

## <a name="parameters"></a>パラメーター

_n_
  
> グループボックスのラベルの長さ。 
    
_u_
  
> 新しい構造の名前を指定します。
    
## <a name="remarks"></a>注釈

**sizeddtblgroupbox**マクロを使用すると、ラベルの長さが既知の場合に、グループボックスコントロールを定義できます。 次のメンバーで新しい構造が作成されます。 
  
```cpp
DTBLGROUPBOX dtblgroupbox;
TCHAR lpszLabel[n];

```

**sizeddtblgroupbox**マクロの結果として得られる構造体へのポインターを**dtblgroupbox**構造のポインターとして使用するには、次のキャストを実行します。 
  
```cpp
lpDtblGroupBox = (LPDTBLGROUPBOX) &SizedDtblGroupBox;

```

## <a name="see-also"></a>関連項目

- [DTBLGROUPBOX](dtblgroupbox.md)
- [構造に関連するマクロ](macros-related-to-structures.md)

