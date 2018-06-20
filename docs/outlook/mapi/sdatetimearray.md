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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 9734adff9c9c7526fc8ff46d17ca913752e104b3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803841"
---
# <a name="sdatetimearray"></a>SDateTimeArray

  
  
**適用されます**: Outlook 
  
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

## <a name="members"></a>メンバー

 **あう**
  
> **Lpft**メンバーが指す配列内の値の数です。 
    
 **lpft**
  
> Time 値を格納する[FILETIME](filetime.md)構造体の配列へのポインター。 
    
## <a name="remarks"></a>備考

PT_MV_SYSTIME の詳細については、[プロパティの種類の一覧](property-types.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[FILETIME](filetime.md)
  
[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

