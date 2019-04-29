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
description: 各行に対応する情報を表示します。 次の表に、各行で [A] セルが示す内容を説明します。
ms.openlocfilehash: 42f346b06cad827cfe56fc113a8387d1a31a6867
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432920"
---
# <a name="a-cell-geometry-section"></a>[A] セル ([Geometry] セクション)

各行に対応する情報を表示します。 次の表に、各行で [A] セルが示す内容を説明します。
  
|**Row**|**説明**|
|:-----|:-----|
|[[arcto]](arcto-row-geometry-section.md) <br/> | 円弧の中点から弦の中点までの距離です。  <br/> |
|[[ellipticalarcto]](ellipticalarcto-row-geometry-section.md) <br/> | 円弧のコントロールポイントの*x*座標 (円弧上の点)。コントロールポイントは、円弧の始点と終点の間の中間点を中心に配置されます。それ以外の場合、円弧はコントロールポイントを通過するために極端なサイズまで拡大することがあり、予期しない結果が発生することがあります。  <br/> |
|[[polylineto]](polylineto-row-geometry-section.md) <br/> | ポリラインの数式です。  <br/> |
|[[nurbsto]](nurbsto-row-geometry-section.md) <br/> | NURBS (nonuniform rational B-spline) の最後から 2 番目のノットです。  <br/> |
|[[splinestart]](splinestart-row-geometry-section.md) <br/> | スプラインの 2 番目のノットです。  <br/> |
|[[splineknot]](splineknot-row-geometry-section.md) <br/> | スプラインのノットのいずれか 1 つです (最後のノットと最初の 2 つのノットは除く)。  <br/> |
|[[infiniteline]](infiniteline-row-geometry-section.md) <br/> | 無限線上の点の*x*座標です。対応する*y*座標は [ [B](b-cell-geometry-section.md)セルで表されます。  <br/> |
|[もう](ellipse-row-geometry-section.md) <br/> | 楕円上の点の*x*座標です。対応する*y*座標は [ [B](b-cell-geometry-section.md)セルで表されます。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [A] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ジオメトリ*i**j* 、 *i*および*j* = <1>、2、3...  <br/> |
|| ジオメトリ*i*A1 ([infiniteline] および楕円の行) *i* = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [A] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionFirstComponent** +  *i* = ** 0、1、2...  <br/> |
| 行インデックス:  <br/> |**visRowVertex** +  *j* where *j* = 0、1、2...  <br/> |
||**visRowVertex** ([InfiniteLine] 行および [Ellipse] 行)  <br/> |
| セル インデックス:  <br/> |**visBow** ([ArcTo] 行)  <br/> |
||**visControlX** ([EllipticalArcTo] 行)  <br/> |
||**visControlY** ([EllipticalArcTo] 行)  <br/> |
||**visPolylineData** ([Polyline] 行)  <br/> |
||**visNURBSKnot** ([NURBSTo] 行)  <br/> |
||**visSplineKnot** ([SplineStart] 行および [SplineKnot] 行)  <br/> |
||**visInfiniteLineX2** ([InfiniteLine] 行)  <br/> |
||**visEllipseMajorX** ([Ellipse] 行)  <br/> |
   

