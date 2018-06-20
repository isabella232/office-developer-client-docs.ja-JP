---
title: '[Y] セル ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251750
localization_priority: Normal
ms.assetid: a53b5787-f419-7a36-3c04-c63b3c173ac7
description: Y を表す-ローカル座標で図形の座標です。 この表に、各行で [Y] セルの。
ms.openlocfilehash: 461fd0ec41d34132f469c811292550d2f7e094f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806841"
---
# <a name="y-cell-geometry-section"></a>[Y] セル ([Geometry] セクション)

の*y*を表す-ローカル座標で図形の座標です。 この表に、各行で [Y] セルの。 
  
|**Row**|**説明**|
|:-----|:-----|
|[[Nurbsto]](nurbsto-row-geometry-section.md) <br/> | [Moveto] 行がセクションの最初の行の場合は、[Y] セルは*y*を表しますが、パスの最初の頂点の座標。 [Y] セルが*y*を表す 2 つの行の間、[moveto] 行が表示されている場合のパスを切断した後の最初の頂点の座標です。  <br/> |
|[[Lineto]](lineto-row-geometry-section.md) <br/> | *Y*が直線の線分の終点の座標です。  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> | *Y*の円弧の終点の座標です。  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | *Y*の楕円の円弧の終点の座標です。  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> | *Y* -ポリラインの最後の頂点の座標です。  <br/> |
|[[Nurbsto]](nurbsto-row-geometry-section.md) <br/> | *Y*が、不均一な合理性のある B スプライン (NURBS) の最後のコントロール ポイントの座標です。  <br/> |
|[[A](splinestart-row-geometry-section.md) <br/> | *Y* -スプラインの 2 番目の制御点の座標です。  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | *Y*のコントロール ポイントの座標です。  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | *Y -* 無限線上の点の座標です。  <br/> |
|[楕円](ellipse-row-geometry-section.md) <br/> | *Y*の楕円の中心の座標です。  <br/> |
   
## <a name="remarks"></a>備考

別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [Y] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ジオメトリの*i*です。Y *j* 、 *i*および*j* = < 1 > では、2、3.  <br/> |
|| ジオメトリの*i*です。Y1 (InfiniteLine と楕円の行)、 *i* = < 1 > では、2、3.  <br/> |
   
プログラムから、インデックスによって [Y] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionFirstComponent** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| 行インデックス:  <br/> |**visRowVertex** +  *j* 、 *j* = 0, 1, 2.  <br/> |
||**visRowVertex**(InfiniteLine と楕円の行)  <br/> |
| セル インデックス:  <br/> |**visY**([Moveto]、[lineto]、ArcTo、EllipticalArcTo、[nurbsto]、ポリライン、[a、および SplineKnot 行)  <br/> |
||**visInfiniteLineY1**(InfiniteLine 行)  <br/> |
||**visEllipseCenterY**([Ellipse] 行)  <br/> |
   

