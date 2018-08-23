---
title: SizedSSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSSortOrderSet
api_type:
- COM
ms.assetid: f0b9c2f4-7011-414d-8e6c-ab22893ef132
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2eb92c3f1555407a77332bd6ec3b2b7202f0553f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803945"
---
# <a name="sizedssortorderset"></a>SizedSSortOrderSet

**適用対象**: Outlook 
  
並べ替え順の指定した数値を含む名前付き[SSortOrderSet](ssortorderset.md)構造体を作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連の構造体。  <br/> |**SSortOrderSet** <br/> |
   
```cpp
SizedSSortOrderSet (_csort,_name)
```

## <a name="parameters"></a>パラメーター

__csort_
  
> 新しい構造体に含まれる並べ替え順序の数です。
    
__名_
  
> 新しい構造体の名前です。
    
## <a name="remarks"></a>注釈

明示的な境界を使用して設定の並べ替え順序を作成するのにには、 **SizedSSortOrderSet**マクロを使用します。 
  
**SSortOrderSet**構造体へのポインターとしての**SizedSSortOrderSet**マクロの結果を新しい構造体を使用するには、次のキャストを実行します。 
  
```cpp
lpSSortOrderSet = (LPSSortOrderSet) &SizedSSortOrderSet;

```

## <a name="see-also"></a>関連項目

- [SSortOrderSet](ssortorderset.md)
- [構造体に関連するマクロ](macros-related-to-structures.md)

