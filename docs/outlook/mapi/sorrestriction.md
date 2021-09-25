---
title: SOrRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SOrRestriction
api_type:
- COM
ms.assetid: 6fee29ce-9a34-4e0c-bb71-03120c3f1117
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 20d34d3cdb6eb43ef28b829d7d4a987b8525491b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578572"
---
# <a name="sorrestriction"></a>SOrRestriction

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
論理 OR 操作 **を** 制限に適用するために使用される **OR** 制限について説明します。 
  
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

## <a name="members"></a>メンバー

 **cRes**
  
> lpRes メンバーが指す配列内の **構造体の** 数。 
    
 **lpRes**
  
> 論理 OR 操作を使用して参加する制限を記述する [SRestriction](srestriction.md) 構造体 **への** ポインター。 
    
## <a name="remarks"></a>注釈

**SOrRestriction** 構造の詳細については、「制限について [」を参照してください](about-restrictions.md)。 
  
## <a name="see-also"></a>関連項目



[SRestriction](srestriction.md)


[MAPI の構造](mapi-structures.md)

