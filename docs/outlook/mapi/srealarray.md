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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8439d6609ebece75699a1150a9d0c1a41277fd52
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429874"
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

## <a name="members"></a>Members

 **cValues**
  
> lpflt メンバーが指す配列内 **の値の** 数。 
    
 **lpflt**
  
> 浮動小数点値の配列へのポインター。
    
## <a name="remarks"></a>注釈

プロパティの種類の詳細については、「PT_MV_R4プロパティの [種類」を参照してください](property-types.md)。
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

