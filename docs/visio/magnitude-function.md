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
description: 返すベクトルの大きさの増加は、A の実行は、B、それぞれを掛けた値の定数 constantA と constantB。
ms.openlocfilehash: f4c428b8b381af58958dab66a71ddd0bcaf715c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805812"
---
# <a name="magnitude-function"></a>MAGNITUDE 関数

台頭は、 _A_との実行は、 _B_、それぞれの定数を掛けた値は、ベクトルの大きさを返します_constantA_と_constantB_。 
  
## <a name="syntax"></a>構文

マグニチュード (* * *constantA* * *、* * *A* * *、* * *constantB* * *、* * *B* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _constantA_ <br/> |必須  <br/> |**番号** <br/> |高さを乗算する定数を指定します。  <br/> |
| _A_ <br/> |必須  <br/> |**番号** <br/> |高さを指定します。  <br/> |
| _constantB_ <br/> |必須  <br/> |**番号** <br/> |水平距離を乗算する定数を指定します。  <br/> |
| _B_ <br/> |必須  <br/> |**番号** <br/> |水平距離を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

MAGNITUDE は次の数式に従って計算されます。
  
SQRT ((constantA \* A) ^2 + (constantB \* B) ^2)
  
## <a name="example"></a>例

MAGNITUDE(1, 3, 1, 4) 
  
5 を返します。 
  

