---
title: NURBS 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251579
localization_priority: Normal
ms.assetid: f34db20d-6501-2026-a5e8-29c4d4cb2405
description: 一様でない有理数 B スプライン (NURBS) を返します。 この関数は、[nurbsto] geometry 行の E セルで使用されます。
ms.openlocfilehash: af92374a829c0df8e71ac81e630abc4fa64988dc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438457"
---
# <a name="nurbs-function"></a>NURBS 関数

一様でない有理数 B スプライン (NURBS) を返します。 この関数は、[nurbsto] geometry 行の E セルで使用されます。
  
## <a name="syntax"></a>構文

NURBS (* * *knotLast* * *、* **度** *、* * *xType* * *、* * *yType* * *、* * *x1* * *、* * *y1* * *、* * *knot1* * *、* * *weight1* * *、...) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _knotLast_ <br/> |必須  <br/> |**string** <br/> | 最後のノットを指定します。  <br/> |
| _度合_ <br/> |必須  <br/> |**数値** <br/> |スプラインの角度を指定します。  <br/> |
| _xType_ <br/> |必須  <br/> |**数値** <br/> |_x_入力データを解釈する方法を指定します。 _xType_が0の場合、すべての_x_入力データは幅に対する割合として解釈されます。 _xType_が1の場合、すべての_x_入力データはローカル座標として解釈されます。  <br/> |
| _yType_ <br/> |必須  <br/> |**数値** <br/> |_y_入力データの解釈方法を指定します。 _yType_が0の場合、すべての_y_入力データは、高さの割合として解釈されます。 _yType_が1の場合、すべての_y_入力データはローカル座標として解釈されます。  <br/> |
| _x1_ <br/> |必須  <br/> |**String** <br/> |x 座標を指定します。  <br/> |
| _y1_ <br/> |必須  <br/> |**String** <br/> |y 座標を指定します。  <br/> |
| _knot1_ <br/> |必須  <br/> |**String** <br/> |B スプライン上のノットを指定します。  <br/> |
| _weight1_ <br/> |必須  <br/> |**String** <br/> |B スプラインの太さを指定します。  <br/> |
   
## <a name="remarks"></a>注釈

すべての*x*引数に対して、 *y*引数が必要です。それ以外の場合は、エラーが返されます。 
  
少なくとも1つの*x*、 *y*、*ノット*、および*weight*引数を指定する必要があります。それ以外の場合、Visio はエラーを返します。 
  

