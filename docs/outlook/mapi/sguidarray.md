---
title: SGuidArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SGuidArray
api_type:
- COM
ms.assetid: 2091e5fc-75c8-4ea4-87e9-a9bf508e9c58
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 156234b52f092c25314603f7f65da2b20bdbbbc5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550010"
---
# <a name="sguidarray"></a>SGuidArray

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
型のプロパティを記述するために使用される [GUID](guid.md) 構造体の配列を格納PT_MV_CLSID。 
  
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

 **cValues**
  
> lpguid メンバーが指す配列内 **の値の** 数。 
    
 **lpguid**
  
> クラス識別子の値を **含** む GUID 構造体の配列へのポインター。 
    
## <a name="remarks"></a>注釈

プロパティの詳細については、「PT_MV_CLSIDの [リスト」を参照してください](property-types.md)。
  
## <a name="see-also"></a>関連項目



[GUID](guid.md)
  
[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

