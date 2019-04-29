---
title: SMAPIVerbArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIVerbArray
api_type:
- COM
ms.assetid: 8736f75c-3e95-42dd-9bc1-2f0bd23c4a02
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7cba5dce60ce15ddb12776d619143849298aac9f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433914"
---
# <a name="smapiverbarray"></a>SMAPIVerbArray

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI 動詞を記述する[smapiverb](smapiverb.md)構造の配列が含まれています。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform  <br/> |
|関連するマクロ:  <br/> |[CbMAPIVerbArray](cbmapiverbarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cMAPIVerb;
  SMAPIVerb aMAPIVerb[MAPI_DIM];
} SMAPIVerbArray, FAR * LPMAPIVERBARRAY;

```

## <a name="members"></a>メンバー

 **cforms**
  
> 配列内の動詞の数。
    
 **aforminfo**
  
> MAPI 動詞の配列。
    
## <a name="remarks"></a>注釈

**SMAPIVerbArray**構造体は、 [imapiforminfo:: CalcVerbSet](imapiforminfo-calcverbset.md)メソッドのパラメーターとして渡されます。 
  
## <a name="see-also"></a>関連項目



[SMAPIVerb](smapiverb.md)


[MAPI の構造](mapi-structures.md)

