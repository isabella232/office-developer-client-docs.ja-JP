---
title: SSizeRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSizeRestriction
api_type:
- COM
ms.assetid: 4e7340d1-3cb9-4276-b83f-1c8f94acb909
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 24ceb7b5358447de3a240756227b86224d2c354c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344479"
---
# <a name="ssizerestriction"></a>SSizeRestriction

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロパティ値のサイズをテストするために使用されるサイズ制限を記述します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
```cpp
typedef struct _SSizeRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  ULONG cb;
} SSizeRestriction;

```

## <a name="members"></a>Members

 **relop**
  
> サイズ比較で使用されるリレーショナル演算子です。 可能な値は次のとおりです。 
    
RELOP_GE 
  
> この比較は、最初の値よりも大きくなるか等しいかに基づいて行われます。
    
RELOP_GT 
  
> 比較は、より大きな最初の値に基づいて行われます。
    
RELOP_LE 
  
> 比較は、1番目の値よりも小さいか等しいかに基づいて行われます。
    
RELOP_LT 
  
> 比較は、小さい方の値に基づいて行われます。
    
RELOP_NE 
  
> 比較は、等しくない値に基づいて行われます。
    
RELOP_RE 
  
> 比較は、LIKE (正規表現) の値に基づいて行われます。
    
RELOP_EQ 
  
> 比較は同じ値に基づいて行われます。
    
 **ulPropTag**
  
> テストするプロパティを識別するプロパティタグ。
    
 **cb**
  
> プロパティ値のバイト数。
    
## <a name="remarks"></a>解説

制限のしくみについての一般的な説明については、「[制限につい](about-restrictions.md)て」を参照してください。 
  
## <a name="see-also"></a>関連項目



[SRestriction](srestriction.md)


[MAPI の構造](mapi-structures.md)

