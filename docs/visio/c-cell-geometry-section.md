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
description: 各行に対応する情報を表示します。 次の表に、各行で [C] セルが示す内容を説明します。
ms.openlocfilehash: 5599c09ad3656653c486d7feff9aed2ee89e4614
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413368"
---
# <a name="c-cell-geometry-section"></a>[C] セル ([Geometry] セクション)

各行に対応する情報を表示します。 次の表に、各行で [C] セルが示す内容を説明します。
  
|**Row**|**説明**|
|:-----|:-----|
|[[ellipticalarcto]](ellipticalarcto-row-geometry-section.md) <br/> | 親の*x*軸を基準にした円弧の主軸の角度。  <br/> |
|[[nurbsto]](nurbsto-row-geometry-section.md) <br/> | NURBS (nonuniform rational B-spline) の最初のノットです。  <br/> |
|[[splinestart]](splinestart-row-geometry-section.md) <br/> | スプラインの最後のノットです。  <br/> |
|[もう](ellipse-row-geometry-section.md) <br/> | 楕円上の点の*x*座標です。対応する*y*座標は [ [D](d-cell-geometry-section.md)セルで表されます。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [C] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ジオメトリ*i*C *j* where *i*および*j* = <1>、2、3...  <br/> |
|| ジオメトリ*i*C1 (楕円行)  <br/> |
   
プログラムから、インデックスによって [C] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionFirstComponent** +  *i* = ** 0、1、2...  <br/> |
| 行インデックス:  <br/> |**visRowVertex** +  *j* where *j* = 0、1、2...  <br/> |
||**visRowVertex** ([Ellipse] 行)  <br/> |
| セル インデックス:  <br/> |**visEccentricityAngle** ([EllipticalArcTo] 行)  <br/> |
||**visNURBSKnotPrev** ([NURBSTo] 行)  <br/> |
||**visSplineKnot3** ([SplineStart] 行)  <br/> |
||**visEllipseMinorX** ([Ellipse] 行)  <br/> |
   

