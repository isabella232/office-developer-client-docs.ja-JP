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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e601a59a68a3a7d248165d4e573c5abc34d27e2a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586467"
---
# <a name="sbinaryarray"></a>SBinaryArray

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
バイナリ値の配列が含まれています。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SBinaryArray
{
  ULONG cValues;
  SBinary FAR *lpbin;
} SBinaryArray;

```

## <a name="members"></a>Members

 **あう**
  
> **Lpbin**メンバーが指す配列内の値の数です。 
    
 **lpbin**
  
> バイナリ値を格納する[SBinary](sbinary.md)構造体の配列へのポインター。 
    
## <a name="remarks"></a>注釈

**SBinaryArray**構造体を使用して、PT_MV_BINARY の種類のプロパティを記述します。 
  
PT_MV_BINARY の詳細については、[プロパティの種類の一覧](property-types.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[SBinary](sbinary.md)
  
[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

