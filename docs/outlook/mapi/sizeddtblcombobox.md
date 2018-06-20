---
title: SizedDtblComboBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblComboBox
api_type:
- COM
ms.assetid: 1e5ea9f2-1029-4584-845a-890d3e956036
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: fea2b496a34d7aa7f9469158fae14daf6a770608
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803932"
---
# <a name="sizeddtblcombobox"></a>SizedDtblComboBox
 
**適用されます**: Outlook 
  
コンボ ボックス コントロールと関連付けられたエディット コントロールに入力できる文字の最大数を記述するための[DTBLCOMBOBOX](dtblcombobox.md)構造体を含む名前付き構造体を作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連の構造体。  <br/> |**DTBLCOMBOBOX** <br/> |
   
```cpp
SizedDtblComboBox (n, u)
```

## <a name="parameters"></a>Parameters

_n_
  
> コンボ ボックスの入力できる文字数は、コントロールを編集します。 
    
_u_
  
> 新しい構造体の名前です。
    
## <a name="remarks"></a>備考

**SizedDtblComboBox**マクロを使用して、有効な文字の文字列の長さがわかっている場合は、コンボ ボックスを定義できます。 新しい構造体は、次のメンバーで作成されます。 
  
```cpp
DTBLCOMBOBOX dtblcombobox;
TCHAR lpszCharsAllowed[n];

```

**DTBLCOMBOBOX**構造体のポインターとして、 **SizedDtblComboBox**マクロからの結果の構造にポインターを使用するには、次のキャストを実行します。 
  
```cpp
lpDtblComboBox = (LPDTBLCOMBOBOX) &SizedDtblComboBox;

```

## <a name="see-also"></a>関連項目

- [DTBLCOMBOBOX](dtblcombobox.md)
- [構造体に関連するマクロ](macros-related-to-structures.md)

