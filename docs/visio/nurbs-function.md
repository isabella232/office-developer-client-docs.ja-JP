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
description: 不均一な合理性のある B スプライン (NURBS) を返します。 [Nurbsto] のジオメトリの行の [E] セルでは、この関数が使用されます。
ms.openlocfilehash: 005a66b9da2425beaf416ec2273c10446c183add
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19805965"
---
# <a name="nurbs-function"></a>NURBS 関数

不均一な合理性のある B スプライン (NURBS) を返します。 [Nurbsto] のジオメトリの行の [E] セルでは、この関数が使用されます。
  
## <a name="syntax"></a>構文

NURBS (* * *knotLast* * *、* **度** *、* * *xType* * *、* * *yType* * *、* * *x1* * *、* * *y1* * *、* * *knot1* * *、* * *weight1* * *,...) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _knotLast_ <br/> |必須  <br/> |**string** <br/> | 最後のノットを指定します。  <br/> |
| _度_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |スプラインの角度を指定します。  <br/> |
| _xType_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |_X_の入力データを解釈する方法を指定します。 _XType_が 0 の場合は、入力データ_x_のすべては幅に対する割合として解釈されます。 _XType_が 1 の場合は、入力データ_x_のすべてはローカル座標として解釈されます。  <br/> |
| _yType_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |入力データ_y_の解釈方法を指定します。 _YType_が 0 の場合は、入力データ_y_のすべては高さに対する割合として解釈されます。 _YType_が 1 の場合は、入力データ_y_のすべてはローカル座標として解釈されます。  <br/> |
| _x1_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |x 座標を指定します。  <br/> |
| _y1_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |y 座標を指定します。  <br/> |
| _knot1_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |B スプライン上のノットを指定します。  <br/> |
| _weight1_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |B スプラインの太さを指定します。  <br/> |
   
## <a name="remarks"></a>注釈

すべての*x*引数では、必要があります、 *y*引数を指定します。それ以外の場合、エラーが返されます。 
  
少なくとも 1 つの*x*、 *y*、*ノット*、および*重量*の引数を指定する必要があります。それ以外の場合、Visio では、エラーが返されます。 
  

