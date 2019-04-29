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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 07a1a0a1953d136da534fbdc6339d326c877bebf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426654"
---
# <a name="snotrestriction"></a>SNotRestriction

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
制限に制限を適用するのでは**なく**、制限に対して論理**not**演算を適用する場合に使用します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
```cpp
typedef struct _SNotRestriction
{
  ULONG ulReserved;
  LPSRestriction lpRes;
} SNotRestriction;

```

## <a name="members"></a>メンバー

 **ulreserved**
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 **lpres**
  
> 論理**not**演算子に結合する制限を説明する[srestriction](srestriction.md)構造体へのポインター。 
    
## <a name="remarks"></a>注釈

**snotrestriction**構造の詳細については、「[制限につい](about-restrictions.md)て」を参照してください。 
  
## <a name="see-also"></a>関連項目



[SRestriction](srestriction.md)


[MAPI の構造](mapi-structures.md)

