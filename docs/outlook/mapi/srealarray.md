---
title: SRealArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SRealArray
api_type:
- COM
ms.assetid: 95be07bf-5732-4775-9e0f-fec47e99d9b7
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8c6fc32463fda6589f1cf8b2508c826bbcab1560
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566522"
---
# <a name="srealarray"></a>SRealArray

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
データ型のプロパティを記述するために使用される浮動小数点値の配列をPT_MV_R4。 
  
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

## <a name="members"></a>メンバー

 **cValues**
  
> lpflt メンバーが指す配列内 **の値の** 数。 
    
 **lpflt**
  
> 浮動小数点値の配列へのポインター。
    
## <a name="remarks"></a>注釈

プロパティの種類の詳細については、「PT_MV_R4プロパティの [種類」を参照してください](property-types.md)。
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

