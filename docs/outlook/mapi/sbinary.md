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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 38263f46ccb50e1836f31d457f54f52abca7ce9f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407845"
---
# <a name="sbinary"></a>SBinary

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
型のプロパティをPT_BINARY。
  
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
  
> **lpb** メンバー内のバイト数。 
    
 **lpb**
  
> プロパティ値PT_BINARYポインター。
    
## <a name="remarks"></a>注釈

プロパティの種類の詳細については [、「MAPI プロパティの種類の概要」を参照してください](mapi-property-type-overview.md)。
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

