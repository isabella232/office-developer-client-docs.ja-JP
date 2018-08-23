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
ms.openlocfilehash: 06b9b6a046aaa0f16418f75d402cc5be44f845a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803974"
---
# <a name="sorrestriction"></a>SOrRestriction

  
  
**適用対象**: Outlook 
  
制約を論理**OR**演算を適用するために使用する**か**制限について説明します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SOrRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SOrRestriction;

```

## <a name="members"></a>Members

 **cRes**
  
> **LpRes**メンバーが指す配列内の構造体の数です。 
    
 **lpRes**
  
> 論理**OR**演算を使用して参加している制限を表す[SRestriction](srestriction.md)構造体へのポインター。 
    
## <a name="remarks"></a>注釈

**SOrRestriction**構造体の詳細については、[制限の詳細](about-restrictions.md)を参照してください。 
  
## <a name="see-also"></a>関連項目



[SRestriction](srestriction.md)


[MAPI の構造](mapi-structures.md)

