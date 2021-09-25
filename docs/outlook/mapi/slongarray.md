---
title: SLongArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SLongArray
api_type:
- COM
ms.assetid: 57435634-202d-4998-9931-4562f1a66f5f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d1f987f87fb07912115057aed82c0e592e0695c5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619737"
---
# <a name="slongarray"></a>SLongArray

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
型のプロパティを記述するために使用される LONG 値型の配列を格納PT_MV_LONG。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SLongArray
{
  ULONG cValues;
  LONG FAR *lpl;
} SLongArray;

```

## <a name="members"></a>メンバー

 **cValues**
  
> lpl メンバーが指す配列内の **値の** 数。 
    
 **lpl**
  
> LONG 値の配列へのポインター。
    
## <a name="remarks"></a>注釈

プロパティの詳細については、「プロパティPT_MV_LONG [リスト」を参照してください](property-types.md)。
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

