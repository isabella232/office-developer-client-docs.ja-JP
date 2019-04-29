---
title: SPropProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropProblemArray
api_type:
- COM
ms.assetid: 3fbaa77a-be43-4fce-af67-1826ee101799
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f78e0ed939e190a9855ea4b040d18c01cfecc91d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406858"
---
# <a name="spropproblemarray"></a>SPropProblemArray

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
1つ以上の[spropproblem](spropproblem.md)構造の配列を含みます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|関連するマクロ:  <br/> |[CbNewSPropProblemArray](cbnewspropproblemarray.md) <br/> [CbSPropProblemArray](cbspropproblemarray.md) <br/> [SizedSPropProblemArray](sizedspropproblemarray.md) <br/> |
   
```cpp
typedef struct _SPropProblemArray
{
  ULONG cProblem;
  SPropProblem aProblem[MAPI_DIM];
} SPropProblemArray, FAR *LPSPropProblemArray;

```

## <a name="members"></a>メンバー

 **cproblem**
  
> **aproblem**メンバーによって示された、配列内の[spropproblem](spropproblem.md)構造体の数。 
    
 **aproblem**
  
> プロパティエラーを説明する**spropproblem**構造の配列です。 
    
## <a name="remarks"></a>注釈

プロパティに関連するエラーについて、 **spropproblem**および**spropproblem の配列**構造がどのように機能するかの詳細については、「 [MAPI の名前付きプロパティ](mapi-named-properties.md)」を参照してください。 
  
## <a name="see-also"></a>関連項目



[SCODE](scode.md)
  
[SPropProblem](spropproblem.md)


[MAPI の構造](mapi-structures.md)

