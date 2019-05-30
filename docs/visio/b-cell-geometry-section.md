---
title: '[B] セル ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251751
localization_priority: Normal
ms.assetid: b0fb6a47-47d8-ab9c-854d-0b0bbfdfcc27
description: 各行に対応する情報を表示します。 次の表に、各行で [B] セルが示す内容を説明します。
ms.openlocfilehash: 46c8aa418f495905630fed2833d84afc93945346
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537795"
---
# <a name="b-cell-geometry-section"></a>[B] セル ([Geometry] セクション)

各行に対応する情報を表示します。 次の表に、各行で [B] セルが示す内容を説明します。
  
|Row|説明|
|:-----|:-----|
|[[Ellipticalarcto]](ellipticalarcto-row-geometry-section.md) <br/> | 円弧のコントロールポイントの*y*座標です。  <br/> |
|[[Nurbsto]](nurbsto-row-geometry-section.md) <br/> | NURBS (nonuniform rational B-spline) の最後の太さです。  <br/> |
|[[Splinestart]](splinestart-row-geometry-section.md) <br/> | スプラインの最初のノットです。  <br/> |
|[[Infiniteline]](infiniteline-row-geometry-section.md) <br/> | 無限線上の点の*y*座標です。対応する*x*座標[は、A](a-cell-geometry-section.md)セルで表されます。  <br/> |
|[もう](ellipse-row-geometry-section.md) <br/> | 楕円上の点の*y*座標です。対応する*x*座標[は、A](a-cell-geometry-section.md)セルで表されます。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [B] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ジオメトリ*i*B *j* where *i*および*j* = <1>、2、3...  <br/> |
|| ジオメトリ*i*B1 ([Infiniteline] および楕円の行)  <br/> |
   
プログラムから、インデックスによって [B] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionFirstComponent** +  *i* = ** 0、1、2...  <br/> |
| 行インデックス:  <br/> |**visRowVertex** +  *j* where *j* = 0、1、2...  <br/> |
||**visRowVertex** ([InfiniteLine] 行および [Ellipse] 行)  <br/> |
| セル インデックス:  <br/> |**visControlX** ([EllipticalArcTo] 行)  <br/> |
||**visControlY** ([EllipticalArcTo] 行)  <br/> |
||**visNURBSWeight** ([NURBSTo] 行)  <br/> |
||**visSplineKnot2** ([SplineStart] 行)  <br/> |
||**visInfiniteLineY2** ([InfiniteLine] 行)  <br/> |
||**visEllipseMajorY** ([Ellipse] 行)  <br/> |
   

