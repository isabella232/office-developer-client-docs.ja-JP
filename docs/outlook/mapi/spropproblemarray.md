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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e71658922b6cb80dadc7e034a51c10189c4207ed
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568498"
---
# <a name="spropproblemarray"></a>SPropProblemArray

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
1 つまたは複数の[SPropProblem](spropproblem.md)構造体の配列が含まれています。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連するマクロ:  <br/> |[CbNewSPropProblemArray](cbnewspropproblemarray.md) <br/> [CbSPropProblemArray](cbspropproblemarray.md) <br/> [SizedSPropProblemArray](sizedspropproblemarray.md) <br/> |
   
```cpp
typedef struct _SPropProblemArray
{
  ULONG cProblem;
  SPropProblem aProblem[MAPI_DIM];
} SPropProblemArray, FAR *LPSPropProblemArray;

```

## <a name="members"></a>Members

 **cProblem**
  
> **かかわる問題**のメンバーで指定された配列内の[SPropProblem](spropproblem.md)構造体の数です。 
    
 **かかわる問題**
  
> プロパティのエラーを記述する**SPropProblem**構造体の配列。 
    
## <a name="remarks"></a>注釈

プロパティに関連するエラーと**SPropProblem**と**SPropProblemArray**の構造体のしくみの詳細については、 [MAPI 名前付きプロパティ](mapi-named-properties.md)を参照してください。 
  
## <a name="see-also"></a>関連項目



[SCODE](scode.md)
  
[SPropProblem](spropproblem.md)


[MAPI の構造](mapi-structures.md)

