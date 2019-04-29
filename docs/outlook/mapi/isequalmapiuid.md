---
title: IsEqualMAPIUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.IsEqualMAPIUID
api_type:
- COM
ms.assetid: 85d71b73-0630-4c5d-b0e3-b48d27a300d0
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 44e3613338c8932bc80dd1150392033dfa3cd050
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426934"
---
# <a name="isequalmapiuid"></a>IsEqualMAPIUID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
2つの[MAPIUID](mapiuid.md)構造体をテストして、同じ識別子を含んでいるかどうかを確認します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|関連する構造:  <br/> |**MAPIUID** <br/> |
   
```cpp
IsEqualMAPIUID(lpuid1, lpuid2)
```

## <a name="parameters"></a>パラメーター

 _lpuid1_
  
> テストする最初の**MAPIUID**構造体へのポインター。 
    
 _lpuid2_
  
> テストする2番目の**MAPIUID**構造体へのポインター。 
    
## <a name="remarks"></a>注釈

**IsEqualMAPIUID**マクロは、2つの**MAPIUID**構造体に同じ識別子が含まれている場合は TRUE を返し、そうでない場合は FALSE を返します。 
  
**IsEqualMAPIUID**マクロを使用するには、ヘッダーファイルのメモリを含める必要があります。 
  
## <a name="see-also"></a>関連項目



[MAPIUID](mapiuid.md)


[構造に関連するマクロ](macros-related-to-structures.md)

