---
title: SLargeIntegerArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SLargeIntegerArray
api_type:
- COM
ms.assetid: 9ec9a674-c1a2-4137-856f-6cabe6f0eb9f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ea314971e43450235bab8af806ad810a718bd6f6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550002"
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

## <a name="members"></a>メンバー

 **cValues**
  
> lpli メンバーが指す配列内の **値の** 数。 
    
 **lpli**
  
> 整数値を **保持するLARGE_INTEGER** 配列へのポインター。 
    
## <a name="remarks"></a>注釈

プロパティの詳細については、「PT_MV_18 [の種類」を参照してください](property-types.md)。
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

