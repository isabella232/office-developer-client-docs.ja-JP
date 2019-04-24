---
title: CURRENCY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CURRENCY
api_type:
- COM
ms.assetid: cffc05a0-95e4-4b9f-bf8f-c4272a75afa8
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: dccb6b19af72d0f748a3a513b7f3d78904ebc789
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315135"
---
# <a name="currency"></a>CURRENCY

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
通貨値を表す、符号付きの64ビット整数を含みます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
```cpp
typedef struct tagCY
{
  unsigned long Lo;
  long Hi;
} CURRENCY;

```

## <a name="members"></a>Members

 **Lo**
  
> 通貨値の低順位32ビット。 
    
 **こんにちは**
  
> 通貨値の上位32ビット。
    
## <a name="remarks"></a>解説

**通貨**構造は、小数点の右側に4桁の10進数を使用した10進数の整数表現です。 たとえば、327500の格納された値は、32.7500 の通貨値を表すものとして解釈されます。 
  
**通貨**構造は、PT_CURRENCY 型のプロパティを記述するために使用されます。 プロパティの種類の詳細については、「 [MAPI プロパティの種類の概要](mapi-property-type-overview.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

