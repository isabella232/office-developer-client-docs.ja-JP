---
title: SizedDtblCheckBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblCheckBox
api_type:
- COM
ms.assetid: 9d04a124-54d4-43ac-967f-ea8e7a09b1d0
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6120439ea0d98ed6b64fe1542a4372265574723a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567532"
---
# <a name="sizeddtblcheckbox"></a>SizedDtblCheckBox
 
**適用されます**: Outlook 2013 |Outlook 2016 
  
チェック ボックス コントロールと指定した長さのラベルを記述するための[DTBLCHECKBOX](dtblcheckbox.md)構造体を含む名前付き構造体を作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連の構造体。  <br/> |**DTBLCHECKBOX** <br/> |
   
```cpp
SizedDtblCheckBox (n, u)
```

## <a name="parameters"></a>パラメーター

_n_
  
> 新しい構造体に含まれるラベルの長さです。
    
_u_
  
> 新しい構造体の名前です。
    
## <a name="remarks"></a>注釈

**SizedDtblCheckBox**マクロを使用して、ラベルの文字数がわかっている場合は、チェック ボックスを定義できます。 新しい構造体は、次のメンバーで作成されます。 
  
```cpp
DTBLCHECKBOX dtblcheckbox;
TCHAR lpszLabel[n];
```

**DTBLCHECKBOX**構造体のポインターとして、 **SizedDtblCheckBox**マクロからの結果の構造にポインターを使用するには、次のキャストを実行します。 
  
```cpp
lpDtblCheckBox = (LPDTBLCHECKBOX) &SizedDtblCheckBox;
```

## <a name="see-also"></a>関連項目

- [DTBLCHECKBOX](dtblcheckbox.md)
- [構造体に関連するマクロ](macros-related-to-structures.md)

