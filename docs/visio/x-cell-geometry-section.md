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
description: ローカル座標での図形の x 座標を表します。 次の表に、各行で [X] セルが示す内容を説明します。
ms.openlocfilehash: 2b3303533db446780ef797844ac5e1438cec242f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538215"
---
# <a name="x-cell-geometry-section"></a>[X] セル ([Geometry] セクション)

ローカル座標での図形の*x*座標を表します。 次の表に、各行で [X] セルが示す内容を説明します。 
  
|Row|説明|
|:-----|:-----|
|[MoveTo](moveto-row-geometry-section.md) <br/> | [MoveTo] 行がセクションの最初の行の場合、[X] セルは、パスの最初の頂点に対する*x*座標を表します。 [MoveTo] 行が2つの行の間に表示される場合、[X] セルは、パスを切断した後の最初の頂点に対する*x*座標を表します。  <br/> |
|[LineTo](lineto-row-geometry-section.md) <br/> | 直線セグメントの最後の頂点に対する*x*座標です。  <br/> |
|[[Arcto]](arcto-row-geometry-section.md) <br/> | 円弧の最後の頂点に対する*x*座標です。  <br/> |
|[[Ellipticalarcto]](ellipticalarcto-row-geometry-section.md) <br/> | 楕円の弧の最後の頂点に対する*x*座標です。  <br/> |
|[[Polylineto]](polylineto-row-geometry-section.md) <br/> | ポリラインの最後の頂点に対する*x*座標です。  <br/> |
|[[Nurbsto]](nurbsto-row-geometry-section.md) <br/> | 不均一な有理数 (NURBS) の最後のコントロールポイントに対する*x*座標です。  <br/> |
|[[Splinestart]](splinestart-row-geometry-section.md) <br/> | スプラインの2番目のコントロールポイントに対する*x*座標です。  <br/> |
|[[Splineknot]](splineknot-row-geometry-section.md) <br/> | コントロールポイントの*x*座標です。  <br/> |
|[[Infiniteline]](infiniteline-row-geometry-section.md) <br/> | 無限線上の点の*x*座標です。  <br/> |
|[もう](ellipse-row-geometry-section.md) <br/> | 楕円の中心点の*x*座標です。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [X] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ジオメトリ*i*X *j* where *i*および*j* = <1>、2、3...  <br/> |
|| ジオメトリ*i*X1 ([Infiniteline] および楕円の行) *i* = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [X] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionFirstComponent** +  *i* = ** 0、1、2...  <br/> |
| 行インデックス:  <br/> |**visRowVertex** +  *j* where *j* = 0、1、2...  <br/> |
||**visRowVertex** ([InfiniteLine] 行および [Ellipse] 行)  <br/> |
| セル インデックス:  <br/> |**visX** ([MoveTo]、[LineTo]、[ArcTo]、[EllipticalArcTo]、[NURBSTo]、[Polyline]、[SplineStart]、および [SplineKnot] 行)  <br/> |
||**visInfiniteLineX1** ([InfiniteLine] 行)  <br/> |
||**visEllipseCenterX** ([Ellipse] 行)  <br/> |
   

