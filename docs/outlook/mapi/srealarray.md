---
title: SRealArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRealArray
api_type:
- COM
ms.assetid: 95be07bf-5732-4775-9e0f-fec47e99d9b7
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8c7ce2805248bf91ce7da071c67ece28a5b8ca07
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564284"
---
# <a name="srealarray"></a>SRealArray

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
PT_MV_R4 の種類のプロパティを説明するために使用される浮動小数点値の配列が含まれています。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SRealArray
{
  ULONG cValues;
  float FAR *lpflt;
} SRealArray;

```

## <a name="members"></a>Members

 **あう**
  
> **Lpflt**メンバーが指す配列内の値の数です。 
    
 **lpflt**
  
> Float 値の配列へのポインター。
    
## <a name="remarks"></a>注釈

PT_MV_R4 プロパティのデータ型の詳細については、[プロパティの型](property-types.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

