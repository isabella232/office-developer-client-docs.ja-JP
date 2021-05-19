---
title: SLargeIntegerArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLargeIntegerArray
api_type:
- COM
ms.assetid: 9ec9a674-c1a2-4137-856f-6cabe6f0eb9f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ab82fff2645a5e1861523eb3f1866e0ddc7d13a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331389"
---
# <a name="slargeintegerarray"></a>SLargeIntegerArray

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
型のプロパティ [をLARGE_INTEGERする](https://go.microsoft.com/fwlink/?LinkId=132130) 構造体の配列をPT_MV_I8。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SLargeIntegerArray
{
  ULONG cValues;
  LARGE_INTEGER FAR *lpli;
} SLargeIntegerArray;

```

## <a name="members"></a>Members

 **cValues**
  
> lpli メンバーが指す配列内の **値の** 数。 
    
 **lpli**
  
> 整数値を **保持するLARGE_INTEGER** 配列へのポインター。 
    
## <a name="remarks"></a>注釈

プロパティの詳細については、「PT_MV_18 [の種類」を参照してください](property-types.md)。
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

