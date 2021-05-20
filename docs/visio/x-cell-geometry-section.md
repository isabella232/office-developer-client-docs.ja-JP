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
description: ローカル座標の図形の x 座標を表します。 次の表に、各行で [X] セルが示す内容を説明します。
ms.openlocfilehash: 2b3303533db446780ef797844ac5e1438cec242f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538215"
---
# <a name="x-cell-geometry-section"></a>[X] セル ([Geometry] セクション)

ローカル座標の  *図形*  の x 座標を表します。 次の表に、各行で [X] セルが示す内容を説明します。 
  
|行|説明|
|:-----|:-----|
|[MoveTo](moveto-row-geometry-section.md) <br/> | MoveTo 行がセクションの最初の行である場合、X セルはパスの最初の頂点の  *x*  座標を表します。 MoveTo 行が 2 行の間に表示される場合、X セルはパスのブレーク後の最初の頂点の  *x*  座標を表します。  <br/> |
|[LineTo](lineto-row-geometry-section.md) <br/> | 直線  *セグメント*  の終了頂点の x 座標。  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> | 円弧  *の*  終了頂点の x 座標。  <br/> |
|[楕円ArcTo](ellipticalarcto-row-geometry-section.md) <br/> | 楕  *円円弧*  の終了頂点の x 座標。  <br/> |
|[ポリラインTo](polylineto-row-geometry-section.md) <br/> | ポリライン  *の*  終了頂点の x 座標。  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | 非  *ユニフォーム*  有理 B スプライン (NURBS) の最後のコントロール ポイントの x 座標。  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | スプライン  *の*  2 番目のコントロール ポイントの x 座標。  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | コントロール  *ポイントの x*  座標。  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | 無限  *線*  上の点の x 座標。  <br/> |
|[楕円](ellipse-row-geometry-section.md) <br/> | 楕  *円*  の中心の x 座標。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [X] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Geometry  *i*  .x  *j*            *i と*  j =  *<*  1>、2、3...  <br/> |
|| Geometry  *i*  .X1 (InfiniteLine 行と楕円行) i  *=*  <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [X] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionFirstComponent**  +  *i* *=* 0, 1, 2...  <br/> |
| 行インデックス:  <br/> |**visRowVertex**  +  *j* は *j* = 0、1、2..です。  <br/> |
||**visRowVertex** ([InfiniteLine] 行および [Ellipse] 行)  <br/> |
| セル インデックス:  <br/> |**visX** ([MoveTo]、[LineTo]、[ArcTo]、[EllipticalArcTo]、[NURBSTo]、[Polyline]、[SplineStart]、および [SplineKnot] 行)  <br/> |
||**visInfiniteLineX1** ([InfiniteLine] 行)  <br/> |
||**visEllipseCenterX** ([Ellipse] 行)  <br/> |
   

