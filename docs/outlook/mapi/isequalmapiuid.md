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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0c72164cac8a37d0372ac93f4ed6d3face966ddb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566664"
---
# <a name="isequalmapiuid"></a>IsEqualMAPIUID

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
同じ識別子が含まれているかどうかを決定する 2 つの[MAPIUID](mapiuid.md)構造体をテストします。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連の構造体。  <br/> |**MAPIUID** <br/> |
   
```cpp
IsEqualMAPIUID(lpuid1, lpuid2)
```

## <a name="parameters"></a>パラメーター

 _lpuid1_
  
> テストする最初の**MAPIUID**構造体へのポインター。 
    
 _lpuid2_
  
> テストする 2 番目の**MAPIUID**構造体へのポインター。 
    
## <a name="remarks"></a>注釈

**IsEqualMAPIUID**マクロは、2 つの**MAPIUID**構造体が含まれる場合、同じ識別子と FALSE そうでない場合に TRUE を返します。 
  
**IsEqualMAPIUID**マクロには、ヘッダー ファイル Memory.h が含まれていることが必要です。 
  
## <a name="see-also"></a>関連項目



[MAPIUID](mapiuid.md)


[構造体に関連するマクロ](macros-related-to-structures.md)

