---
title: '[A] セル ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm51215
ms.localizationpriority: medium
ms.assetid: 6853df0f-d22e-89ca-7d34-342b9c0bea23
description: 各行に対応する情報を表示します。次の表に、各行で [A] セルが示す内容を説明します。
ms.openlocfilehash: 260c9cb9a6bc5b538857585208ba9b8d719f07ad
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608768"
---
# <a name="a-cell-geometry-section"></a>[A] セル ([Geometry] セクション)

各行に対応する情報を表示します。次の表に、各行で [A] セルが示す内容を説明します。
  
|行|説明|
|:-----|:-----|
|[ArcTo](arcto-row-geometry-section.md) <br/> | 円弧の中点から弦の中点までの距離です。  <br/> |
|[楕円ArcTo](ellipticalarcto-row-geometry-section.md) <br/> | 円弧  *の*  コントロール ポイントの x 座標、円弧上の点。コントロール ポイントは、円弧の開始頂点と終了頂点の約半分の位置に最適です。それ以外の場合、コントロール ポイントを通過するために極端なサイズにアークが大きくなる可能性があります。予期しない結果が得られます。  <br/> |
|[ポリラインTo](polylineto-row-geometry-section.md) <br/> | ポリラインの数式です。  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | NURBS (nonuniform rational B-spline) の最後から 2 番目のノットです。  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | スプラインの 2 番目のノットです。  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | スプラインのノットのいずれか 1 つです (最後のノットと最初の 2 つのノットは除く)。  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | 無限  *線*  上の点の x 座標。B セルで  *表される y*  座標と組み [合](b-cell-geometry-section.md) わせ。  <br/> |
|[楕円](ellipse-row-geometry-section.md) <br/> | 楕  *円上*  の点の x 座標。B セルで  *表される y*  座標と組み [合](b-cell-geometry-section.md) わせ。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [A] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Geometry  *i*  .i  *と*            *j*  =  *<*  1>、2、3...  <br/> |
|| Geometry  *i*  .A1 (InfiniteLine 行と楕円行) i  *=*  <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [A] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionFirstComponent**  +  *i* *=* 0, 1, 2...  <br/> |
| 行インデックス:  <br/> |**visRowVertex**  +  *j* は *j* = 0、1、2..です。  <br/> |
||**visRowVertex** ([InfiniteLine] 行および [Ellipse] 行)  <br/> |
| セル インデックス:  <br/> |**visBow** ([ArcTo] 行)  <br/> |
||**visControlX** ([EllipticalArcTo] 行)  <br/> |
||**visControlY** ([EllipticalArcTo] 行)  <br/> |
||**visPolylineData** ([Polyline] 行)  <br/> |
||**visNURBSKnot** ([NURBSTo] 行)  <br/> |
||**visSplineKnot** ([SplineStart] 行および [SplineKnot] 行)  <br/> |
||**visInfiniteLineX2** ([InfiniteLine] 行)  <br/> |
||**visEllipseMajorX** ([Ellipse] 行)  <br/> |
   

