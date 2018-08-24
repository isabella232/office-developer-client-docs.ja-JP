---
title: SDateTimeArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SDateTimeArray
api_type:
- COM
ms.assetid: 6a0dff65-1055-487c-9d15-4cfe336f2ad7
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: dc90f15835de35354a271d87a736366a4caf8dd9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578781"
---
# <a name="sdatetimearray"></a>SDateTimeArray

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
PT_MV_SYSTIME の種類のプロパティを説明するために使用する時刻の値の配列が含まれています。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SDateTimeArray
{
  ULONG cValues;
  FILETIME FAR *lpft;
} SDateTimeArray;

```

## <a name="members"></a>Members

 **あう**
  
> **Lpft**メンバーが指す配列内の値の数です。 
    
 **lpft**
  
> Time 値を格納する[FILETIME](filetime.md)構造体の配列へのポインター。 
    
## <a name="remarks"></a>注釈

PT_MV_SYSTIME の詳細については、[プロパティの種類の一覧](property-types.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[FILETIME](filetime.md)
  
[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

