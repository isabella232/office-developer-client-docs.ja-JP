---
title: CURRENCY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CURRENCY
api_type:
- COM
ms.assetid: cffc05a0-95e4-4b9f-bf8f-c4272a75afa8
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5da768e4d26ad76e17a1c7271405739b52a2c028
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592523"
---
# <a name="currency"></a>CURRENCY

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
通貨値を表す符号付き 64 ビット整数を含む。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct tagCY
{
  unsigned long Lo;
  long Hi;
} CURRENCY;

```

## <a name="members"></a>メンバー

 **Lo**
  
> 通貨値の低次 32 ビット。 
    
 **こんにちは**
  
> 通貨値の高次 32 ビット。
    
## <a name="remarks"></a>注釈

**CURRENCY 構造体** は、小数点の右側に 4 桁の数字を持つ 10 進数の拡大縮小整数表現です。 たとえば、格納されている値 327500 は、通貨値 32.7500 を表すと解釈されます。 
  
**CURRENCY 構造体** は、プロパティの種類のプロパティを記述するために使用PT_CURRENCY。 プロパティの種類の詳細については [、「MAPI プロパティの種類の概要」を参照してください](mapi-property-type-overview.md)。
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

