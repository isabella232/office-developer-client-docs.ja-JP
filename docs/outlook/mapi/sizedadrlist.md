---
title: SizedADRLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SizedADRLIST
api_type:
- COM
ms.assetid: 5c64d74a-83a7-4122-b1d1-fcca0f4a6cdb
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7b4bbc92c1e7784053773d70c49d204a39e1967f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550015"
---
# <a name="sizedadrlist"></a>SizedADRLIST

**適用対象**: Outlook 2013 | Outlook 2016 
  
指定した [数の ADRENTRY](adrlist.md) 構造体を含む、指定した名前の [ADRLIST 構造体を定義](adrentry.md) します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連する構造:  <br/> |**ADRLIST** <br/> |
   
```cpp
SizedADRLIST (_centries,_name)
```

## <a name="parameters"></a>パラメーター

_ _centries_
  
> 新しい **ADRLIST** 構造に含める **ADRENTRY** 構造体の数。 
    
_ _name_
  
> 新しい **ADRLIST 構造の名前** 。 
    
## <a name="remarks"></a>注釈

**SizedADRLIST** マクロを使用すると、配列の長さの要件が分かっているときに明示的な境界を持つ受信者リストを定義できます。 次のコードは **、SizedADRLIST** マクロの結果を **ADRLIST 構造ポインターにキャストする方法を** 示しています。 
  
```cpp
lpADRList = (LPADRLIST) &SizedADRList;
```

## <a name="see-also"></a>関連項目

- [ADRLIST](adrlist.md)
- [ADRENTRY](adrentry.md)
- [構造に関連するマクロ](macros-related-to-structures.md)

