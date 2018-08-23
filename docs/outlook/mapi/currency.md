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
ms.openlocfilehash: b5a2cd09942559167300d8a921987864b8c5e48f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576464"
---
# <a name="currency"></a>CURRENCY

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
通貨の値を表す 64 ビットの符号付き整数が含まれています。 
  
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

## <a name="members"></a>Members

 **Lo**
  
> 通貨型の値の下位 32 ビット。 
    
 **こんにちは**
  
> 通貨型の値の上位の 32 ビットです。
    
## <a name="remarks"></a>注釈

**通貨**の構造は、小数点の右側に 4 桁の 10 進数の位取り整数表現です。 327500 の格納された値は 32.7500 の通貨値を表すものとして解釈されます。 
  
**通貨**の構造体を使用して、PT_CURRENCY の種類のプロパティを記述します。 プロパティの型については、 [MAPI プロパティの種類の概要](mapi-property-type-overview.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

