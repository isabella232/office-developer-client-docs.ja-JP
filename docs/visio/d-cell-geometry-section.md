---
title: '[D] セル ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251753
localization_priority: Normal
ms.assetid: 5f1fdf59-db58-561c-e187-1af72a8b87f2
description: 各行に対応する情報を表示します。 次の表に、各行で [D] セルが示す内容を説明します。
ms.openlocfilehash: a76093f028986907b58175bc6b8c81a7056cfe07
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542500"
---
# <a name="d-cell-geometry-section"></a>[D] セル ([Geometry] セクション)

各行に対応する情報を表示します。 次の表に、各行で [D] セルが示す内容を説明します。
  
|Row|説明|
|:-----|:-----|
|[[Ellipticalarcto]](ellipticalarcto-row-geometry-section.md) <br/> | 円弧の長軸と短軸の比率です。これらの言葉の通常の意味とは関係なく、"長" 軸が "短" 軸よりも長い必要はありません。したがって、比率は 1 より大きい必要はありません。このセルを 0 以下、または 1000 より大きく設定すると、予測できない結果になる可能性があります。  <br/> |
|[[Nurbsto]](nurbsto-row-geometry-section.md) <br/> | NURBS (nonuniform rational B-spline) の最初の太さです。  <br/> |
|[[Splinestart]](splinestart-row-geometry-section.md) <br/> | スプラインの角度 (1 ～ 25 の整数) です。  <br/> |
|[もう](ellipse-row-geometry-section.md) <br/> | 楕円上の点の*y*座標です。[ [C](c-cell-geometry-section.md)セルで表される*x*座標と対にします。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [D] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ジオメトリ*i*D *j* where *i*および*j* = <1>、2、3...  <br/> |
|| ジオメトリ*i*D1 (楕円行) *i* = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [D] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionFirstComponent** +  *i* = ** 0、1、2...  <br/> |
| 行インデックス:  <br/> |**visRowVertex** +  *j* where *j* = 0、1、2...  <br/> |
||**visRowVertex** ([Ellipse] 行)  <br/> |
| セル インデックス:  <br/> |**visAspectRatio** ([EllipticalArcTo] 行)  <br/> |
||**visNURBSWeightPrev** ([NURBSTo] 行)  <br/> |
||**visSplineDegree** ([SplineStart] 行)  <br/> |
||**visEllipseMinorY** ([Ellipse] 行)  <br/> |
   

