---
title: MAGNITUDE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251461
localization_priority: Normal
ms.assetid: 9f443687-9861-5f51-94c4-f056805f736b
description: constantA と constantB のそれぞれの定数によって、x がで、その実行が B であるベクトルの大きさを返します。
ms.openlocfilehash: 6393c7827e2553ca4948c8b9c51075ca8e4783bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317816"
---
# <a name="magnitude-function"></a>MAGNITUDE 関数

_constantA_と_constantB_のそれぞれの定数によっ__ て、x がで、その実行が_B_であるベクトルの大きさを返します。 
  
## <a name="syntax"></a>構文

マグニチュード (* * *constantA* * *、* * *A* * *、* * *constantB* * *、* * *B* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _constantA_ <br/> |必須  <br/> |**数値** <br/> |高さを乗算する定数を指定します。  <br/> |
| _A_ <br/> |必須  <br/> |**数値** <br/> |高さを指定します。  <br/> |
| _constantB_ <br/> |必須  <br/> |**数値** <br/> |水平距離を乗算する定数を指定します。  <br/> |
| _B_ <br/> |必須  <br/> |**数値** <br/> |水平距離を指定します。  <br/> |
   
## <a name="remarks"></a>解説

MAGNITUDE は次の数式に従って計算されます。
  
SQRT ((constantA \* A) ^ 2 + (constantB \* B) ^ 2)
  
## <a name="example"></a>例

MAGNITUDE(1, 3, 1, 4) 
  
5 を返します。 
  

