---
title: SShortArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SShortArray
api_type:
- COM
ms.assetid: 201ceb76-41bc-4d7b-835d-5196bf3dc234
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 99d2cfb9b4d460ed6a86235a011f9bf244aac0a2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566466"
---
# <a name="sshortarray"></a>SShortArray

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
型のプロパティを記述するために使用される符号なし整数値の配列をPT_MV_SHORT。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SShortArray
{
  ULONG cValues;
  short int FAR *lpi;
} SShortArray;

```

## <a name="members"></a>メンバー

 **cValues**
  
> lpi メンバーが指す配列内の **値の** 数。 
    
 **lpi**
  
> 符号なし整数値の配列へのポインター。
    
## <a name="remarks"></a>注釈

プロパティおよび他のプロパティPT_MV_SHORT詳細については [、「Property Types」を参照してください](property-types.md)。 
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

