---
title: SOrRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SOrRestriction
api_type:
- COM
ms.assetid: 6fee29ce-9a34-4e0c-bb71-03120c3f1117
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9b4ca4628f356142eb5303c064e3916474810fda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345102"
---
# <a name="sorrestriction"></a>SOrRestriction

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
制限に論理**or**演算を適用するために使用される**or**制限について説明します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
```cpp
typedef struct _SOrRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SOrRestriction;

```

## <a name="members"></a>Members

 **cres**
  
> **lpres**メンバによって参照されている配列内の構造体の数。 
    
 **lpres**
  
> 論理**OR**演算を使用して結合する制限について説明する[srestriction](srestriction.md)構造体へのポインター。 
    
## <a name="remarks"></a>解説

**sorrestriction**構造の詳細については、「[制限につい](about-restrictions.md)て」を参照してください。 
  
## <a name="see-also"></a>関連項目



[SRestriction](srestriction.md)


[MAPI の構造](mapi-structures.md)

