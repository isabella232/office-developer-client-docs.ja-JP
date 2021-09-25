---
title: '[D] セル ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251753
ms.localizationpriority: medium
ms.assetid: 5f1fdf59-db58-561c-e187-1af72a8b87f2
description: 各行に対応する情報を表示します。次の表に、各行で [D] セルが示す内容を説明します。
ms.openlocfilehash: a36f021096b28e92ff9bd2d78ef089d759cef600
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586608"
---
# <a name="d-cell-geometry-section"></a>[D] セル ([Geometry] セクション)

各行に対応する情報を表示します。次の表に、各行で [D] セルが示す内容を説明します。
  
|行|説明|
|:-----|:-----|
|[楕円ArcTo](ellipticalarcto-row-geometry-section.md) <br/> | 円弧の長軸と短軸の比率です。これらの言葉の通常の意味とは関係なく、"長" 軸が "短" 軸よりも長い必要はありません。したがって、比率は 1 より大きい必要はありません。このセルを 0 以下、または 1000 より大きく設定すると、予測できない結果になる可能性があります。  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | NURBS (nonuniform rational B-spline) の最初の太さです。  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | スプラインの角度 (1 ～ 25 の整数) です。  <br/> |
|[楕円](ellipse-row-geometry-section.md) <br/> | 楕  *円上*  の点の y 座標。C セルで  *表される x*  座標と組み [合](c-cell-geometry-section.md) わせ。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [D] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Geometry  *i*  .D  *j*            *i と*  j =  *<*  1>、2、3...  <br/> |
|| Geometry  *i*  .D1 (楕円行) i =  *<*  1>、2、3...  <br/> |
   
プログラムから、インデックスによって [D] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionFirstComponent**  +  *i* *=* 0, 1, 2...  <br/> |
| 行インデックス:  <br/> |**visRowVertex**  +  *j* は *j* = 0、1、2..です。  <br/> |
||**visRowVertex** ([Ellipse] 行)  <br/> |
| セル インデックス:  <br/> |**visAspectRatio** ([EllipticalArcTo] 行)  <br/> |
||**visNURBSWeightPrev** ([NURBSTo] 行)  <br/> |
||**visSplineDegree** ([SplineStart] 行)  <br/> |
||**visEllipseMinorY** ([Ellipse] 行)  <br/> |
   

