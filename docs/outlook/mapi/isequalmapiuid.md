---
title: IsEqualMAPIUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.IsEqualMAPIUID
api_type:
- COM
ms.assetid: 85d71b73-0630-4c5d-b0e3-b48d27a300d0
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 248d0452b45e8e715b067fc96fcd2ab2a52f7323
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556239"
---
# <a name="isequalmapiuid"></a>IsEqualMAPIUID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
2 [つの MAPIUID](mapiuid.md) 構造体をテストして、同じ識別子が含まれているかどうかを判断します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連する構造:  <br/> |**MAPIUID** <br/> |
   
```cpp
IsEqualMAPIUID(lpuid1, lpuid2)
```

## <a name="parameters"></a>パラメーター

 _lpuid1_
  
> テストする最初 **の MAPIUID** 構造体へのポインター。 
    
 _lpuid2_
  
> テストする **2 番目の MAPIUID** 構造体へのポインター。 
    
## <a name="remarks"></a>注釈

**IsEqualMAPIUID** マクロは、2 つの **MAPIUID** 構造体に同じ識別子が含まれている場合は TRUE を返し、指定しない場合は FALSE を返します。 
  
**IsEqualMAPIUID** マクロでは、ヘッダー ファイル Memory.h を含める必要があります。 
  
## <a name="see-also"></a>関連項目



[MAPIUID](mapiuid.md)


[構造に関連するマクロ](macros-related-to-structures.md)

