---
title: SizedDtblEdit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblEdit
api_type:
- COM
ms.assetid: a658d027-03a2-4cde-bf99-563e8521cb31
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 4ea77023bdc9442325f4af46d23c107e7172ceaf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803920"
---
# <a name="sizeddtbledit"></a>SizedDtblEdit

**適用されます**: Outlook 
  
エディット コントロールと、コントロールに入力できる文字の最大数を記述するための[DTBLEDIT](dtbledit.md)構造体を含む名前付き構造体を作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連の構造体。  <br/> |**DTBLEDIT** <br/> |
   
```cpp
SizedDtblEdit (n, u)
```

## <a name="parameters"></a>Parameters

_n_
  
> エディット コントロールに入力できる文字の最大数。
    
_u_
  
> 新しい構造体の名前です。
    
## <a name="remarks"></a>備考

**SizedDtblEdit**マクロを使用して、有効な文字の数がわかっている場合は、エディット コントロールを定義できます。 新しい構造体は、次のメンバーで作成されます。 
  
```cpp
DTBLEDIT dtbledit;
TCHAR lpszCharsAllowed[n];

```

**DTBLEDIT**構造体のポインターとして、 **SizedDtblEdit**マクロからの結果の構造にポインターを使用するには、次のキャストを実行します。 
  
```cpp
lpDtblEdit = (LPDTBLEDIT) &SizedDtblEdit;

```

## <a name="see-also"></a>関連項目

- [DTBLEDIT](dtbledit.md)
- [構造体に関連するマクロ](macros-related-to-structures.md)

