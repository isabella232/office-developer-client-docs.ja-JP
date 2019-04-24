---
title: SizedADRLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedADRLIST
api_type:
- COM
ms.assetid: 5c64d74a-83a7-4122-b1d1-fcca0f4a6cdb
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c35a1eb54b29c04bc8eed453272b59aae0ea737e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282776"
---
# <a name="sizedadrlist"></a>SizedADRLIST

**適用対象**: Outlook 2013 | Outlook 2016 
  
指定された名前を持つ[adrlist](adrlist.md)構造を定義します。この構造体には、指定した数の[adrlist](adrentry.md)構造が含まれています。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|関連する構造:  <br/> |**ADRLIST** <br/> |
   
```cpp
SizedADRLIST (_centries,_name)
```

## <a name="parameters"></a>パラメーター

__centries_
  
> 新しい**adrentry**構造に含める**adrentry**構造体の数。 
    
__名前_
  
> 新しい**adrlist**構造体の名前。 
    
## <a name="remarks"></a>解説

**sizedadrlist**マクロを使用すると、配列の長さの要件がわかっている場合に、明示的な境界を持つ受信者リストを定義できます。 次のコードは、 **sizedadrlist**マクロの結果を**adrlist**構造体のポインターにキャストする方法を示しています。 
  
```cpp
lpADRList = (LPADRLIST) &SizedADRList;
```

## <a name="see-also"></a>関連項目

- [ADRLIST](adrlist.md)
- [ADRENTRY](adrentry.md)
- [構造に関連するマクロ](macros-related-to-structures.md)

