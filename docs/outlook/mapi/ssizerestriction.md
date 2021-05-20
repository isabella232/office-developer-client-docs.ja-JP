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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 24ceb7b5358447de3a240756227b86224d2c354c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439087"
---
# <a name="ssizerestriction"></a>SSizeRestriction

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロパティ値のサイズをテストするために使用されるサイズ制限について説明します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
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
  
> サイズ比較で使用される関係演算子。 指定できる値は次のとおりです。 
    
RELOP_GE 
  
> 比較は、大きいまたは等しい最初の値に基づいて行います。
    
RELOP_GT 
  
> 比較は、大きい最初の値に基づいて行います。
    
RELOP_LE 
  
> 比較は、より小さいか等しい最初の値に基づいて行います。
    
RELOP_LT 
  
> 比較は、より小さい最初の値に基づいて行います。
    
RELOP_NE 
  
> 比較は、等しくない値に基づいて行います。
    
RELOP_RE 
  
> 比較は LIKE (正規表現) の値に基づいて行います。
    
RELOP_EQ 
  
> 比較は、等しい値に基づいて行います。
    
 **ulPropTag**
  
> テストするプロパティを識別するプロパティ タグ。
    
 **cb**
  
> プロパティ値のバイト数。
    
## <a name="remarks"></a>注釈

制限の動作の一般的な説明については、「 [制限について」を参照してください](about-restrictions.md)。 
  
## <a name="see-also"></a>関連項目



[SRestriction](srestriction.md)


[MAPI の構造](mapi-structures.md)

