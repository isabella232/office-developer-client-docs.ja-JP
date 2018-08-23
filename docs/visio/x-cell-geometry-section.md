---
title: '[X] セル ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1135
localization_priority: Normal
ms.assetid: 2416b323-e084-18e1-c9be-a797078dfab9
description: X を表す-ローカル座標で図形の座標です。 この表に、各行で [X] セルの。
ms.openlocfilehash: e5bc99d4f73d49741c4378009dfc2a883bb655ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806806"
---
# <a name="x-cell-geometry-section"></a>[X] セル ([図形座標] セクション)

*X*を表す-ローカル座標で図形の座標です。 この表に、各行で [X] セルの。 
  
|**Row**|**説明**|
|:-----|:-----|
|[MoveTo](moveto-row-geometry-section.md) <br/> | [Moveto] 行がセクションの最初の行の場合は、[X] セルは*x*を表しますが、パスの最初の頂点の座標です。 [X] セルが*x*を表す 2 つの行の間、[moveto] 行が表示されている場合のパスを切断した後の最初の頂点の座標です。  <br/> |
|[[Lineto]](lineto-row-geometry-section.md) <br/> | *X*の直線の線分の終点の座標です。  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> | *X*の円弧の終点の座標です。  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | *X*の楕円の円弧の終点の座標です。  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> | *X* -ポリラインの最後の頂点の座標です。  <br/> |
|[[Nurbsto]](nurbsto-row-geometry-section.md) <br/> | *X*が、不均一な合理性のある B スプライン (NURBS) の最後のコントロール ポイントの座標です。  <br/> |
|[[A](splinestart-row-geometry-section.md) <br/> | *X* -スプラインの 2 番目の制御点の座標です。  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | *X* -コントロール ポイントの座標です。  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | *X* -無限線上の点の座標です。  <br/> |
|[楕円](ellipse-row-geometry-section.md) <br/> | *X*の楕円の中心の座標です。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [X] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ジオメトリの*i*です。*J* x 位置*i*と*j* = < 1 > では、2、3.  <br/> |
|| ジオメトリの*i*です。X1 (InfiniteLine と楕円の行)、 *i* = < 1 > では、2、3.  <br/> |
   
プログラムから、インデックスによって [X] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionFirstComponent** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| 行インデックス:  <br/> |**visRowVertex** +  *j* 、 *j* = 0, 1, 2.  <br/> |
||**visRowVertex** ([InfiniteLine] 行および [Ellipse] 行)  <br/> |
| セル インデックス:  <br/> |**visX** ([MoveTo]、[LineTo]、[ArcTo]、[EllipticalArcTo]、[NURBSTo]、[Polyline]、[SplineStart]、および [SplineKnot] 行)  <br/> |
||**visInfiniteLineX1** ([InfiniteLine] 行)  <br/> |
||**visEllipseCenterX** ([Ellipse] 行)  <br/> |
   

