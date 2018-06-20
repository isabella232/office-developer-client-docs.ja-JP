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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: fd9a8d731d141dbb71a204a2d20b268951bef42f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803802"
---
# <a name="sbinaryarray"></a>SBinaryArray

  
  
**適用されます**: Outlook 
  
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

## <a name="members"></a>メンバー

 **あう**
  
> **Lpbin**メンバーが指す配列内の値の数です。 
    
 **lpbin**
  
> バイナリ値を格納する[SBinary](sbinary.md)構造体の配列へのポインター。 
    
## <a name="remarks"></a>備考

**SBinaryArray**構造体を使用して、PT_MV_BINARY の種類のプロパティを記述します。 
  
PT_MV_BINARY の詳細については、[プロパティの種類の一覧](property-types.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[SBinary](sbinary.md)
  
[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

