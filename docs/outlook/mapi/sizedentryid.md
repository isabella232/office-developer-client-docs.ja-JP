---
title: SizedENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedENTRYID
api_type:
- COM
ms.assetid: 491170af-db35-4d7e-a912-44ffe8c7506b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 88cf91330dea82dda490b81cc8de6fea0504baf7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282685"
---
# <a name="sizedentryid"></a>SizedENTRYID

**適用対象**: Outlook 2013 | Outlook 2016 
  
指定したサイズの**ab**メンバーを含む、名前付き[ENTRYID](entryid.md)構造を作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|関連する構造:  <br/> |**ENTRYID** <br/> |
   
```cpp
SizedENTRYID (_cb, _name)
```

## <a name="parameters"></a>パラメーター

__cb_
  
> 新しい構造の**ab**メンバーのバイト数。 
    
__名前_
  
> 新しい構造の名前を指定します。
    
## <a name="remarks"></a>解説

**sizedentryid**マクロを使用すると、配列の長さの要件を認識した後にエントリ識別子を定義できます。 このマクロを使用して、明示的な境界を持つエントリ識別子を作成します。 
  
**sizedentryid**マクロの結果として得られる新しい構造を、 **ENTRYID**構造体へのポインターとして使用するには、次のキャストを実行します。 
  
```cpp
lpENTRYID = (LPENTRYID) &SizedENTRYID;

```

## <a name="see-also"></a>関連項目

- [ENTRYID](entryid.md)
- [構造に関連するマクロ](macros-related-to-structures.md)

