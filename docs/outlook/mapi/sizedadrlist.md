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
ms.openlocfilehash: 13dad61176a877295069317e4a5b51888b01bebb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803907"
---
# <a name="sizedadrlist"></a>SizedADRLIST

**適用対象**: Outlook 
  
[ADRENTRY](adrentry.md)構造体の指定した数が含まれている指定した名前の[ADRLIST](adrlist.md)構造体を定義します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連の構造体。  <br/> |**ADRLIST** <br/> |
   
```cpp
SizedADRLIST (_centries,_name)
```

## <a name="parameters"></a>パラメーター

__centries_
  
> 新しい**ADRLIST**構造体に含まれる**ADRENTRY**構造体の数です。 
    
__名_
  
> 新しい**ADRLIST**構造体の名前です。 
    
## <a name="remarks"></a>注釈

**SizedADRLIST**マクロを使用して、配列の長さの要件がわかっている場合は、明示的な境界を持つ受信者の一覧を定義できます。 次のコードは、 **SizedADRLIST**マクロ、 **ADRLIST**構造体のポインターにキャストする方法を示しています。 
  
```cpp
lpADRList = (LPADRLIST) &SizedADRList;
```

## <a name="see-also"></a>関連項目

- [ADRLIST](adrlist.md)
- [ADRENTRY](adrentry.md)
- [構造体に関連するマクロ](macros-related-to-structures.md)

