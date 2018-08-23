---
title: SizedDtblLabel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblLabel
api_type:
- COM
ms.assetid: c7cb8cf9-7abd-4ee3-b88c-d61695f4ed31
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c2e275e373677e50510a0aa87f5060070a870a0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803937"
---
# <a name="sizeddtbllabel"></a>SizedDtblLabel

**適用対象**: Outlook 
  
Label コントロールと関連付けられている指定された長さのラベルを記述するための[DTBLLABEL](dtbllabel.md)構造体を含む名前付き構造体を作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイルに指定します。  <br/> |Mapidefs.h  <br/> |
|関連の構造  <br/> |**DTBLLABEL** <br/> |
   
```cpp
SizedDtblLabel (n, u)
```

## <a name="parameters"></a>パラメーター

_n_
  
> ラベルの長さです。 これには、終了の NULL 文字が含まれます。 
    
_u_
  
> 新しい構造体の名前です。
    
## <a name="remarks"></a>注釈

**SizedDtblLabel**マクロを使用して、ラベルの文字数がわかっている場合、表示テーブルのラベルを定義できます。 新しい構造体は、次のメンバーで作成されます。 
  
```cpp
DTBLLABEL dtbllabel;
TCHAR lpszLabelName[n];
```

**DTBLLABEL**構造体のポインターとして、 **SizedDtblLabel**マクロからの結果の構造にポインターを使用するには、次のキャストを実行します。 
  
```cpp
lpDtblLabel = (LPDTBLLABEL) &SizedDtblLabel;
```

## <a name="see-also"></a>関連項目

- [DTBLLABEL](dtbllabel.md)
- [構造体に関連するマクロ](macros-related-to-structures.md)

