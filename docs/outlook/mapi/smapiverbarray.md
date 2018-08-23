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
ms.openlocfilehash: 1767c86cb5390572b95530060f2295034ed35f43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803972"
---
# <a name="smapiverbarray"></a>SMAPIVerbArray

  
  
**適用対象**: Outlook 
  
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

