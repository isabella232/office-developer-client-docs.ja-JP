---
title: SMAPIVerbArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SMAPIVerbArray
api_type:
- COM
ms.assetid: 8736f75c-3e95-42dd-9bc1-2f0bd23c4a02
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: fe3bcec6e8e0c3148314bf97a8597e784c45aefe
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609455"
---
# <a name="smapiverbarray"></a>SMAPIVerbArray

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI 動詞を記述 [する SMAPIVerb](smapiverb.md) 構造体の配列を格納します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform.h  <br/> |
|関連するマクロ:  <br/> |[CbMAPIVerbArray](cbmapiverbarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cMAPIVerb;
  SMAPIVerb aMAPIVerb[MAPI_DIM];
} SMAPIVerbArray, FAR * LPMAPIVERBARRAY;

```

## <a name="members"></a>メンバー

 **cForms**
  
> 配列内の動詞の数。
    
 **aFormInfo**
  
> MAPI 動詞の配列。
    
## <a name="remarks"></a>注釈

**SMAPIVerbArray** 構造体は [、IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md)メソッドでパラメーターとして渡されます。 
  
## <a name="see-also"></a>関連項目



[SMAPIVerb](smapiverb.md)


[MAPI の構造](mapi-structures.md)

