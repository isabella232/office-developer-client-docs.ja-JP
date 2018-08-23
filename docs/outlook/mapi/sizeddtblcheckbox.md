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
ms.openlocfilehash: 9a30554253bc11c8905273079429e4b41c20583a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803915"
---
# <a name="sizeddtblcheckbox"></a>SizedDtblCheckBox
 
**適用対象**: Outlook 
  
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

