---
title: SBinary
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBinary
api_type:
- COM
ms.assetid: f21b5e6c-7a63-46bf-acbf-0e042e3519f7
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: fe07ed7c7f9c76f82b54732c019b9b5f8beb5db2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803799"
---
# <a name="sbinary"></a>SBinary

  
  
**適用対象**: Outlook 
  
PT_BINARY の型のプロパティについて説明します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SBinary
{
  ULONG      cb;
  LPBYTE     lpb;
} SBinary, FAR *LPSBinary;

```

## <a name="members"></a>Members

 **cb**
  
> **Lpb**のメンバーのバイト数をカウントします。 
    
 **lpb**
  
> PT_BINARY プロパティの値へのポインター。
    
## <a name="remarks"></a>注釈

プロパティの型については、 [MAPI プロパティの種類の概要](mapi-property-type-overview.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

