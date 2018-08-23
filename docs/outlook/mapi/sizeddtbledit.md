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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7e50589b52f3e99bf2569a55bb7d3ca4f8247fd6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591661"
---
# <a name="sizeddtbledit"></a>SizedDtblEdit

**適用されます**: Outlook 2013 |Outlook 2016 
  
エディット コントロールと、コントロールに入力できる文字の最大数を記述するための[DTBLEDIT](dtbledit.md)構造体を含む名前付き構造体を作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連の構造体。  <br/> |**DTBLEDIT** <br/> |
   
```cpp
SizedDtblEdit (n, u)
```

## <a name="parameters"></a>パラメーター

_n_
  
> エディット コントロールに入力できる文字の最大数。
    
_u_
  
> 新しい構造体の名前です。
    
## <a name="remarks"></a>注釈

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

