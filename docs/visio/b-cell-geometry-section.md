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
description: 各行に対応する情報を表示します。次の表に、各行で [B] セルが示す内容を説明します。
ms.openlocfilehash: 7d6f51d037be4852c6a101ad6e576a3a13488cb7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804798"
---
# <a name="b-cell-geometry-section"></a>[B] セル ([図形座標] セクション)

各行に対応する情報を表示します。次の表に、各行で [B] セルが示す内容を説明します。
  
|**Row**|**説明**|
|:-----|:-----|
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | *Y*の円弧のコントロール ポイントの座標です。  <br/> |
|[[Nurbsto]](nurbsto-row-geometry-section.md) <br/> | NURBS (nonuniform rational B-spline) の最後の太さです。  <br/> |
|[[A](splinestart-row-geometry-section.md) <br/> | スプラインの最初のノットです。  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | *Y* -無限線上の点の座標対応する*x*の座標は、[ [A](a-cell-geometry-section.md) ] セルで表されます。  <br/> |
|[楕円](ellipse-row-geometry-section.md) <br/> | *Y* -楕円上の点の座標対応する*x*の座標は、[ [A](a-cell-geometry-section.md) ] セルで表されます。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [B] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ジオメトリの*i*です。B *j* 、 *i*および*j* = < 1 > では、2、3.  <br/> |
|| ジオメトリの*i*です。B1 (InfiniteLine と楕円の行)  <br/> |
   
プログラムから、インデックスによって [B] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionFirstComponent** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| 行インデックス:  <br/> |**visRowVertex** +  *j* 、 *j* = 0, 1, 2.  <br/> |
||**visRowVertex** ([InfiniteLine] 行および [Ellipse] 行)  <br/> |
| セル インデックス:  <br/> |**visControlX** ([EllipticalArcTo] 行)  <br/> |
||**visControlY** ([EllipticalArcTo] 行)  <br/> |
||**visNURBSWeight** ([NURBSTo] 行)  <br/> |
||**visSplineKnot2** ([SplineStart] 行)  <br/> |
||**visInfiniteLineY2** ([InfiniteLine] 行)  <br/> |
||**visEllipseMajorY** ([Ellipse] 行)  <br/> |
   

