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
description: 楕円円弧の端点の x 座標と y 座標、円弧上のコントロール ポイントの x 座標と y 座標、x 軸から楕円の長軸への角度、楕円の長軸と短軸の比率を含む。
ms.openlocfilehash: c6db7560a05652ca3bfcadb2fd4857ac39370562
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421404"
---
# <a name="ellipticalarcto-row-geometry-section"></a>[EllipticalArcTo] 行 ([Geometry] セクション)

楕円円弧の端点の x 座標と y 座標、円弧上のコントロール ポイントの x 座標と *y* 座標 *、x* 軸から楕円の長軸への角度、楕円の長軸と短軸の比率を含む。  
  
[EllipticalArcTo] 行には次のセルが含まれます。
  
|**Cell**|**説明**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |円弧  *上*  の終了頂点の x 座標。  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |円弧  *上の*  終了頂点の y 座標。  <br/> |
|[A](a-cell-geometry-section.md) <br/> |円弧  *の*  コントロール ポイントの x 座標。円弧上のポイント。コントロール ポイントは、円弧の開始頂点と終了頂点の約半分の位置に最適です。それ以外の場合、コントロール ポイントを通過するために極端なサイズにアークが大きくなる可能性があります。予期しない結果が得られます。  <br/> |
|[B](b-cell-geometry-section.md) <br/> |円弧  *のコントロール*  ポイントの y 座標。  <br/> |
|[C](c-cell-geometry-section.md) <br/> |親の x 軸に対する円弧の長軸の角度。  <br/> |
|[D](d-cell-geometry-section.md) <br/> |円弧の長軸と短軸の比率です。これらの言葉の通常の意味とは関係なく、"長" 軸が "短" 軸よりも長い必要はありません。したがって、比率は 1 より大きい必要はありません。このセルを 0 以下、または 1000 より大きく設定すると、予測できない結果になる可能性があります。  <br/> |
   

