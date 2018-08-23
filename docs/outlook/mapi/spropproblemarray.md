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
ms.openlocfilehash: 3fd61828cd631c4abc0131da867ca213a3c44d20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803997"
---
# <a name="spropproblemarray"></a>SPropProblemArray

  
  
**適用対象**: Outlook 
  
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

