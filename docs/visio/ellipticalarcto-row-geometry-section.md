---
title: '[EllipticalArcTo] 行 ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm3015
localization_priority: Normal
ms.assetid: 7ceb30a8-1d05-feff-35d8-08a198784a27
description: 楕円の弧の端点に対する x 座標と y 座標、円弧のコントロールポイントの x 座標と y 座標、x 軸から楕円の長軸までの角度、および楕円の長軸と短軸との比率を格納します。
ms.openlocfilehash: c6db7560a05652ca3bfcadb2fd4857ac39370562
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421404"
---
# <a name="ellipticalarcto-row-geometry-section"></a>[EllipticalArcTo] 行 ([Geometry] セクション)

楕円の弧の端点に対する*x*座標と*y*座標、円弧のコントロールポイントの*x*座標と*y*座標、 *x*軸から楕円の長軸までの角度、および楕円の長軸と mino の比率を格納します。r 軸 
  
[EllipticalArcTo] 行には次のセルが含まれます。
  
|**Cell**|**説明**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |円弧の最後の頂点に対する*x*座標です。  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |円弧の最後の頂点に対する*y*座標です。  <br/> |
|[A](a-cell-geometry-section.md) <br/> |円弧のコントロールポイントの*x*座標です。弧の点を指定します。コントロールポイントは、円弧の始点と終点の間の中間点を中心に配置されます。それ以外の場合、円弧はコントロールポイントを通過するために極端なサイズまで拡大することがあり、予期しない結果が発生することがあります。  <br/> |
|[B](b-cell-geometry-section.md) <br/> |円弧のコントロールポイントの*y*座標です。  <br/> |
|[C](c-cell-geometry-section.md) <br/> |親の*x*軸を基準にした円弧の主軸の角度。  <br/> |
|[D](d-cell-geometry-section.md) <br/> |円弧の長軸と短軸の比率です。これらの言葉の通常の意味とは関係なく、"長" 軸が "短" 軸よりも長い必要はありません。したがって、比率は 1 より大きい必要はありません。このセルを 0 以下、または 1000 より大きく設定すると、予測できない結果になる可能性があります。  <br/> |
   

