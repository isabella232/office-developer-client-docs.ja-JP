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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3d20a0932de0fb29ea73e56c37e262c0ccd062c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424925"
---
# <a name="sguidarray"></a>SGuidArray

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
PT_MV_CLSID 型のプロパティを記述するために使用される[GUID](guid.md)構造の配列を格納します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
```cpp
typedef struct _SGuidArray
{
  ULONG cValues;
  GUID FAR *lpguid;
} SGuidArray;

```

## <a name="members"></a>メンバー

 **cvalues**
  
> **lpguid**メンバーによってポイントされた配列内の値の数。 
    
 **lpguid**
  
> クラス識別子の値を含む**GUID**構造の配列へのポインター。 
    
## <a name="remarks"></a>注釈

PT_MV_CLSID の詳細については、「[プロパティの種類の一覧](property-types.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[GUID](guid.md)
  
[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

