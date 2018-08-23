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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a3d8a76905aa9abb0e5bf001688608e03446704a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803928"
---
# <a name="sizeddtblgroupbox"></a>SizedDtblGroupBox

**適用対象**: Outlook 
  
グループ ボックス コントロールと指定した長さのラベルを記述するための[DTBLGROUPBOX](dtblgroupbox.md)構造体を含む名前付き構造体を作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連の構造体。  <br/> |**DTBLGROUPBOX** <br/> |
   
```cpp
SizedDtblGroupBox (n, u)
```

## <a name="parameters"></a>パラメーター

_n_
  
> グループ ボックスのラベルの長さです。 
    
_u_
  
> 新しい構造体の名前です。
    
## <a name="remarks"></a>注釈

**SizedDtblGroupBox**マクロを使用して、ラベルの長さがわかっている場合、グループ ボックス コントロールを定義できます。 新しい構造体は、次のメンバーで作成されます。 
  
```cpp
DTBLGROUPBOX dtblgroupbox;
TCHAR lpszLabel[n];

```

**DTBLGROUPBOX**構造体のポインターとして、 **SizedDtblGroupBox**マクロからの結果の構造にポインターを使用するには、次のキャストを実行します。 
  
```cpp
lpDtblGroupBox = (LPDTBLGROUPBOX) &SizedDtblGroupBox;

```

## <a name="see-also"></a>関連項目

- [DTBLGROUPBOX](dtblgroupbox.md)
- [構造体に関連するマクロ](macros-related-to-structures.md)

