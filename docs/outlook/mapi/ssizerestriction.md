---
title: SSizeRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SSizeRestriction
api_type:
- COM
ms.assetid: 4e7340d1-3cb9-4276-b83f-1c8f94acb909
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 1d96ab1a4bb8e56bd055af05054f5a8f16448a96
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566452"
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

## <a name="members"></a>メンバー

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

