---
title: '[A] セル ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm51215
localization_priority: Normal
ms.assetid: 6853df0f-d22e-89ca-7d34-342b9c0bea23
description: 各行に対応する情報を表示します。次の表に、各行で [A] セルが示す内容を説明します。
ms.openlocfilehash: b907552c2346292a6b14baf16481b6b40cc80fc4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804740"
---
# <a name="a-cell-geometry-section"></a>[A] セル ([Geometry] セクション)

各行に対応する情報を表示します。次の表に、各行で [A] セルが示す内容を説明します。
  
|**Row**|**説明**|
|:-----|:-----|
|[ArcTo](arcto-row-geometry-section.md) <br/> | 円弧の中点から弦の中点までの距離です。  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | *X*の円弧のコントロール ポイント、円弧上の点の座標です。コントロール ポイントは、最初と最後の円弧の頂点の間で途中で最適に配置します。それ以外の場合、円弧は、予期しない結果で、コントロール ポイントを通過するために極端になることがあります。  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> | ポリラインの数式です。  <br/> |
|[[Nurbsto]](nurbsto-row-geometry-section.md) <br/> | NURBS (nonuniform rational B-spline) の最後から 2 番目のノットです。  <br/> |
|[[A](splinestart-row-geometry-section.md) <br/> | スプラインの 2 番目のノットです。  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | スプラインのノットのいずれか 1 つです (最後のノットと最初の 2 つのノットは除く)。  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | *X* -無限の線の上の点の座標対応する*y*の座標は、[ [B](b-cell-geometry-section.md) ] セルで表されます。  <br/> |
|[楕円](ellipse-row-geometry-section.md) <br/> | *X* -楕円上の点の座標対応する*y*の座標は、[ [B](b-cell-geometry-section.md) ] セルで表されます。  <br/> |
   
## <a name="remarks"></a>備考

別の数式または**CellsU**プロパティを使用して、プログラムから、名前によって、[A] セルへの参照を取得するには、次のコマンドを使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ジオメトリの*i*です。*J* 、 *i*および*j* = < 1 > では、2、3.  <br/> |
|| ジオメトリの*i*です。A1 (InfiniteLine と楕円の行)、 *i* = < 1 > では、2、3.  <br/> |
   
プログラムから、インデックスによって [A] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionFirstComponent** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| 行インデックス:  <br/> |**visRowVertex** +  *j* 、 *j* = 0, 1, 2.  <br/> |
||**visRowVertex**(InfiniteLine と楕円の行)  <br/> |
| セル インデックス:  <br/> |**visBow**(ArcTo 行)  <br/> |
||**visControlX**(EllipticalArcTo 行)  <br/> |
||**visControlY**(EllipticalArcTo 行)  <br/> |
||**visPolylineData**(ポリライン行)  <br/> |
||**visNURBSKnot**([Nurbsto] 行)  <br/> |
||**visSplineKnot**([A と SplineKnot 行)  <br/> |
||**visInfiniteLineX2**(InfiniteLine 行)  <br/> |
||**visEllipseMajorX**([Ellipse] 行)  <br/> |
   

