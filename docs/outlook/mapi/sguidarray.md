---
title: SGuidArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SGuidArray
api_type:
- COM
ms.assetid: 2091e5fc-75c8-4ea4-87e9-a9bf508e9c58
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 553ec17e9caf9bf93278ff139eb94e02e6b48554
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19803905"
---
# <a name="sguidarray"></a>SGuidArray

  
  
**適用されます**: Outlook 
  
PT_MV_CLSID の種類のプロパティを説明するために使用する[GUID](guid.md)構造体の配列が含まれています。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SGuidArray
{
  ULONG cValues;
  GUID FAR *lpguid;
} SGuidArray;

```

## <a name="members"></a>メンバー

 **あう**
  
> **Lpguid**メンバーが指す配列内の値の数です。 
    
 **lpguid**
  
> クラス識別子の値を格納する**GUID**構造体の配列へのポインター。 
    
## <a name="remarks"></a>Remarks

PT_MV_CLSID の詳細については、[プロパティの種類の一覧](property-types.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[GUID](guid.md)
  
[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

