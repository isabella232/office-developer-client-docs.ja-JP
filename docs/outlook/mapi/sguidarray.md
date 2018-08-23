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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: bc0ae6d69db6077c17d2efa66d04a5366f2395a0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585571"
---
# <a name="sguidarray"></a>SGuidArray

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
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

## <a name="members"></a>Members

 **あう**
  
> **Lpguid**メンバーが指す配列内の値の数です。 
    
 **lpguid**
  
> クラス識別子の値を格納する**GUID**構造体の配列へのポインター。 
    
## <a name="remarks"></a>注釈

PT_MV_CLSID の詳細については、[プロパティの種類の一覧](property-types.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[GUID](guid.md)
  
[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

