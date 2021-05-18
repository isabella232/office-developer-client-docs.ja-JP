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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 88cf91330dea82dda490b81cc8de6fea0504baf7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405710"
---
# <a name="sizedentryid"></a>SizedENTRYID

**適用対象**: Outlook 2013 | Outlook 2016 
  
指定したサイズの [ab メンバー](entryid.md) を含む名前付き **ENTRYID** 構造体を作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連する構造:  <br/> |**ENTRYID** <br/> |
   
```cpp
SizedENTRYID (_cb, _name)
```

## <a name="parameters"></a>パラメーター

_ _cb_
  
> 新しい構造体の **ab メンバー** のバイト数。 
    
_ _name_
  
> 新しい構造の名前。
    
## <a name="remarks"></a>注釈

**SizedENTRYID** マクロを使用すると、配列の長さの要件が分かった後にエントリ識別子を定義できます。 明示的な境界を持つエントリ識別子を作成するには、このマクロを使用します。 
  
**SizedENTRYID** マクロの結果として新しい構造を **ENTRYID** 構造体へのポインターとして使用するには、次のキャストを実行します。 
  
```cpp
lpENTRYID = (LPENTRYID) &SizedENTRYID;

```

## <a name="see-also"></a>関連項目

- [ENTRYID](entryid.md)
- [構造に関連するマクロ](macros-related-to-structures.md)

