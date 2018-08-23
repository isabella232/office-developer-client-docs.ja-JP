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
ms.openlocfilehash: c64e9a7497a70ea34dc09a5749dd281a24f9413d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803992"
---
# <a name="srealarray"></a>SRealArray

  
  
**適用対象**: Outlook 
  
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

