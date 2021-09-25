---
title: SDateTimeArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SDateTimeArray
api_type:
- COM
ms.assetid: 6a0dff65-1055-487c-9d15-4cfe336f2ad7
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: af16c7ab02a2cc5dbc72f828d29e292547051d95
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578691"
---
# <a name="sdatetimearray"></a>SDateTimeArray

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
型のプロパティを記述するために使用される時刻値の配列をPT_MV_SYSTIME。
  
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

## <a name="members"></a>メンバー

 **cValues**
  
> lpft メンバーが指す配列内の **値の** 数。 
    
 **lpft**
  
> 時刻値を含む [FILETIME](filetime.md) 構造体の配列へのポインター。 
    
## <a name="remarks"></a>注釈

プロパティの詳細については、「PT_MV_SYSTIME [のリスト」を参照してください](property-types.md)。
  
## <a name="see-also"></a>関連項目



[FILETIME](filetime.md)
  
[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

