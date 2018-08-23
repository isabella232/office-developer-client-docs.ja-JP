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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7a2911779e5f9edb8c0bba7c3476a74ce410477c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569464"
---
# <a name="smapiverbarray"></a>SMAPIVerbArray

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
MAPI の動詞を記述する[SMAPIVerb](smapiverb.md)構造体の配列が含まれています。 
  
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

## <a name="members"></a>Members

 **cForms**
  
> 配列内の動詞の数です。
    
 **aFormInfo**
  
> MAPI の動詞の配列です。
    
## <a name="remarks"></a>注釈

**SMAPIVerbArray**構造体は、 [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md)メソッドのパラメーターとして渡されます。 
  
## <a name="see-also"></a>関連項目



[SMAPIVerb](smapiverb.md)


[MAPI の構造](mapi-structures.md)

