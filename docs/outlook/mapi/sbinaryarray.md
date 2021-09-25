---
title: SBinaryArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SBinaryArray
api_type:
- COM
ms.assetid: 2d5b7302-cad2-4522-beb1-7c6c711f42e6
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 865cfe1df39c3c4070ac24ba2e2b9ff5aea75a66
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609531"
---
# <a name="sbinaryarray"></a>SBinaryArray

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
バイナリ値の配列を含む。 
  
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

## <a name="members"></a>メンバー

 **cValues**
  
> lpbin メンバーが指す配列内の **値の** 数。 
    
 **lpbin**
  
> バイナリ値を保持 [する SBinary](sbinary.md) 構造体の配列へのポインター。 
    
## <a name="remarks"></a>注釈

**SBinaryArray 構造体は**、型のプロパティを記述するために使用PT_MV_BINARY。 
  
プロパティの詳細については、「プロパティPT_MV_BINARY [リスト」を参照してください](property-types.md)。
  
## <a name="see-also"></a>関連項目



[SBinary](sbinary.md)
  
[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

