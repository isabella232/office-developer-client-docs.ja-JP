---
title: '[C] セル ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm140
localization_priority: Normal
ms.assetid: d51a1dd8-678a-a34d-658d-bd7a027dd379
description: 各行に対応する情報を表示します。次の表に、各行で [C] セルが示す内容を説明します。
ms.openlocfilehash: 0284fea02c7eb890b56b6c865a69eb36662d8ae6
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541891"
---
# <a name="c-cell-geometry-section"></a>[C] セル ([Geometry] セクション)

各行に対応する情報を表示します。次の表に、各行で [C] セルが示す内容を説明します。
  
|行|説明|
|:-----|:-----|
|[楕円ArcTo](ellipticalarcto-row-geometry-section.md) <br/> | 親の x 軸に対する円弧の長軸の角度。  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | NURBS (nonuniform rational B-spline) の最初のノットです。  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | スプラインの最後のノットです。  <br/> |
|[楕円](ellipse-row-geometry-section.md) <br/> | 楕  *円上*  の点の x 座標。D セルで  *表される y*  座標と組み [合](d-cell-geometry-section.md) わせ。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [C] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Geometry  *i*  .c  *j*            *i と*  j =  *<*  1>、2、3...  <br/> |
|| Geometry  *i*  .C1 (楕円行)  <br/> |
   
プログラムから、インデックスによって [C] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionFirstComponent**  +  *i* *=* 0, 1, 2...  <br/> |
| 行インデックス:  <br/> |**visRowVertex**  +  *j* は *j* = 0、1、2..です。  <br/> |
||**visRowVertex** ([Ellipse] 行)  <br/> |
| セル インデックス:  <br/> |**visEccentricityAngle** ([EllipticalArcTo] 行)  <br/> |
||**visNURBSKnotPrev** ([NURBSTo] 行)  <br/> |
||**visSplineKnot3** ([SplineStart] 行)  <br/> |
||**visEllipseMinorX** ([Ellipse] 行)  <br/> |
   

