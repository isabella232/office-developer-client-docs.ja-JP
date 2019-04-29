---
title: SBinaryArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBinaryArray
api_type:
- COM
ms.assetid: 2d5b7302-cad2-4522-beb1-7c6c711f42e6
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 12fefbe15491837878608540006e5dd7dc3033ea
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438289"
---
# <a name="sbinaryarray"></a>SBinaryArray

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
バイナリ値の配列を格納します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
```cpp
typedef struct _SBinaryArray
{
  ULONG cValues;
  SBinary FAR *lpbin;
} SBinaryArray;

```

## <a name="members"></a>メンバー

 **cvalues**
  
> **lpbin**メンバーが指す配列内の値の数。 
    
 **lpbin**
  
> バイナリ値を保持する[sbinary](sbinary.md)構造体の配列へのポインター。 
    
## <a name="remarks"></a>注釈

**sbinaryarray**構造体は、PT_MV_BINARY 型のプロパティを記述するために使用されます。 
  
PT_MV_BINARY の詳細については、「[プロパティの種類の一覧](property-types.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[SBinary](sbinary.md)
  
[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

