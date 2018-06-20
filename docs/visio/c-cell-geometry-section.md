---
title: '[C] セル ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm140
localization_priority: Normal
ms.assetid: d51a1dd8-678a-a34d-658d-bd7a027dd379
description: 各行に対応する情報を表示します。次の表に、各行で [C] セルが示す内容を説明します。
ms.openlocfilehash: 1b9a813be825f2deeb5c90d596ffd9f3705bcef6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804946"
---
# <a name="c-cell-geometry-section"></a>[C] セル ([Geometry] セクション)

各行に対応する情報を表示します。次の表に、各行で [C] セルが示す内容を説明します。
  
|**Row**|**説明**|
|:-----|:-----|
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | *X*を基準にして、円弧の長軸の角度を親の軸です。  <br/> |
|[[Nurbsto]](nurbsto-row-geometry-section.md) <br/> | NURBS (nonuniform rational B-spline) の最初のノットです。  <br/> |
|[[A](splinestart-row-geometry-section.md) <br/> | スプラインの最後のノットです。  <br/> |
|[楕円](ellipse-row-geometry-section.md) <br/> | *X* -楕円上の点の座標対応する*y*の座標は[[D](d-cell-geometry-section.md) ] セルで表されます。  <br/> |
   
## <a name="remarks"></a>備考

別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[C] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ジオメトリの*i*です。C *j* 、 *i*および*j* = < 1 > では、2、3.  <br/> |
|| ジオメトリの*i*です。C1 ([Ellipse] 行)  <br/> |
   
プログラムから、インデックスによって [C] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionFirstComponent** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| 行インデックス:  <br/> |**visRowVertex** +  *j* 、 *j* = 0, 1, 2.  <br/> |
||**visRowVertex**([Ellipse] 行)  <br/> |
| セル インデックス:  <br/> |**visEccentricityAngle**(EllipticalArcTo 行)  <br/> |
||**visNURBSKnotPrev**([Nurbsto] 行)  <br/> |
||**visSplineKnot3**([A 行)  <br/> |
||**visEllipseMinorX**([Ellipse] 行)  <br/> |
   

