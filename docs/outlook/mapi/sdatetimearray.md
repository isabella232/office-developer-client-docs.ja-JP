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
ms.openlocfilehash: 9d9fd04776742383f40c6989bcf588b24b33d84b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339796"
---
# <a name="sdatetimearray"></a>SDateTimeArray

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
PT_MV_SYSTIME 型のプロパティを記述するために使用される時間の値の配列を格納します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
```cpp
typedef struct _SDateTimeArray
{
  ULONG cValues;
  FILETIME FAR *lpft;
} SDateTimeArray;

```

## <a name="members"></a>Members

 **cvalues**
  
> **lpft**メンバーが指す配列内の値の数。 
    
 **lpft**
  
> 時刻の値を含む[FILETIME](filetime.md)構造体の配列へのポインター。 
    
## <a name="remarks"></a>解説

PT_MV_SYSTIME の詳細については、「[プロパティの種類の一覧](property-types.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[FILETIME](filetime.md)
  
[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

