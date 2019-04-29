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
description: ローカル座標での図形の y 座標を表します。 次の表に、各行で [Y] セルが示す内容を説明します。
ms.openlocfilehash: 9e823b8d21682b419a70ce498016abf575f36f6b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420942"
---
# <a name="y-cell-geometry-section"></a>[Y] セル ([Geometry] セクション)

ローカル座標での図形の*y*座標を表します。 次の表に、各行で [Y] セルが示す内容を説明します。 
  
|**Row**|**説明**|
|:-----|:-----|
|[[nurbsto]](nurbsto-row-geometry-section.md) <br/> | [MoveTo] 行がセクションの最初の行の場合、[y] セルは、パスの最初の頂点に対する*y*座標を表します。 [MoveTo] 行が2つの行の間に表示される場合、[y] セルは、パスを切断した後の最初の頂点に対する*y*座標を表します。  <br/> |
|[LineTo](lineto-row-geometry-section.md) <br/> | 直線セグメントの最後の頂点に対する*y*座標です。  <br/> |
|[[arcto]](arcto-row-geometry-section.md) <br/> | 円弧の最後の頂点に対する*y*座標です。  <br/> |
|[[ellipticalarcto]](ellipticalarcto-row-geometry-section.md) <br/> | 楕円の弧の最後の頂点に対する*y*座標です。  <br/> |
|[[polylineto]](polylineto-row-geometry-section.md) <br/> | ポリラインの最後の頂点に対する*y*座標です。  <br/> |
|[[nurbsto]](nurbsto-row-geometry-section.md) <br/> | 不均一な有理数 (NURBS) の最後のコントロールポイントに対する*y*座標です。  <br/> |
|[[splinestart]](splinestart-row-geometry-section.md) <br/> | スプラインの2番目のコントロールポイントに対する*y*座標です。  <br/> |
|[[splineknot]](splineknot-row-geometry-section.md) <br/> | コントロールポイントの*y*座標です。  <br/> |
|[[infiniteline]](infiniteline-row-geometry-section.md) <br/> | 無限線上の点の*y*座標です。  <br/> |
|[もう](ellipse-row-geometry-section.md) <br/> | 楕円の中心点の*y*座標です。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Y] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ジオメトリ*i*Y *j* where *i*および*j* = <1>、2、3...  <br/> |
|| ジオメトリ*i*Y1 ([infiniteline] および楕円の行) *i* = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [Y] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionFirstComponent** +  *i* = ** 0、1、2...  <br/> |
| 行インデックス:  <br/> |**visRowVertex** +  *j* where *j* = 0、1、2...  <br/> |
||**visRowVertex** ([InfiniteLine] 行および [Ellipse] 行)  <br/> |
| セル インデックス:  <br/> |**visY** ([MoveTo]、[LineTo]、[ArcTo]、[EllipticalArcTo]、[NURBSTo]、[Polyline]、[SplineStart]、および [SplineKnot] 行)  <br/> |
||**visInfiniteLineY1** ([InfiniteLine] 行)  <br/> |
||**visEllipseCenterY** ([Ellipse] 行)  <br/> |
   

