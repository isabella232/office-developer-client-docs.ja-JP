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
ms.openlocfilehash: 7622baaebf6918cf84c48e53291cf5ec2c0b1a4a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572565"
---
# <a name="sizedssortorderset"></a>SizedSSortOrderSet

**適用されます**: Outlook 2013 |Outlook 2016 
  
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

