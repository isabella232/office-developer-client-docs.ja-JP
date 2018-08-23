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
ms.openlocfilehash: 134eb844ef7b72d396c300b27a87a3a7ae320cf1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804012"
---
# <a name="ssizerestriction"></a>SSizeRestriction

  
  
**適用対象**: Outlook 
  
プロパティの値のサイズをテストするために使用するサイズの制限について説明します。 
  
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
  
> サイズの比較で使用される関係演算子です。 使用可能な値は次のとおりです。 
    
RELOP_GE 
  
> 比較は以上の最初の値に基づいて作成されます。
    
RELOP_GT 
  
> 比較は、最初の値が大きい値に基づいて作成されます。
    
RELOP_LE 
  
> 比較は同等またはそれ以下の最初の値に基づいて作成されます。
    
RELOP_LT 
  
> 比較は、最初の小さい方の値に基づいて作成されます。
    
RELOP_NE 
  
> 比較は、等しくない値に基づいて作成されます。
    
RELOP_RE 
  
> (正規表現) の値と同じようにに基づいて比較が行われます。
    
RELOP_EQ 
  
> 比較は同等の値に基づいて作成されます。
    
 **ulPropTag**
  
> プロパティ タグをテストするプロパティを識別します。
    
 **cb**
  
> プロパティの値のバイト数をカウントします。
    
## <a name="remarks"></a>注釈

制限のしくみの概要については、[制限の詳細](about-restrictions.md)を参照してください。 
  
## <a name="see-also"></a>関連項目



[SRestriction](srestriction.md)


[MAPI の構造](mapi-structures.md)

