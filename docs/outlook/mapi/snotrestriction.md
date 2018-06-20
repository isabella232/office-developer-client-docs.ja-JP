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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: a07a7737e9b9354514a2d5ac2ec37a393a3cd4e4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803966"
---
# <a name="snotrestriction"></a>SNotRestriction

  
  
**適用されます**: Outlook 
  
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

## <a name="members"></a>メンバー

 **ulReserved**
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 **lpRes**
  
> 論理**NOT**演算子に参加している制限を記述する[SRestriction](srestriction.md)構造体へのポインター。 
    
## <a name="remarks"></a>備考

**SNotRestriction**構造体の詳細については、[制限の詳細](about-restrictions.md)を参照してください。 
  
## <a name="see-also"></a>関連項目



[SRestriction](srestriction.md)


[MAPI の構造](mapi-structures.md)

