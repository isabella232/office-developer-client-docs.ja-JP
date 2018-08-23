---
title: SNotRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SNotRestriction
api_type:
- COM
ms.assetid: e86ca032-d973-4b79-976e-5240ab38a0da
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 174da93e7682246565b12c4fc4ffa6d1a9de065c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575064"
---
# <a name="snotrestriction"></a>SNotRestriction

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
**しない**制限、制約を論理**NOT**演算を適用するために使用について説明します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SNotRestriction
{
  ULONG ulReserved;
  LPSRestriction lpRes;
} SNotRestriction;

```

## <a name="members"></a>Members

 **ulReserved**
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 **lpRes**
  
> 論理**NOT**演算子に参加している制限を記述する[SRestriction](srestriction.md)構造体へのポインター。 
    
## <a name="remarks"></a>注釈

**SNotRestriction**構造体の詳細については、[制限の詳細](about-restrictions.md)を参照してください。 
  
## <a name="see-also"></a>関連項目



[SRestriction](srestriction.md)


[MAPI の構造](mapi-structures.md)

