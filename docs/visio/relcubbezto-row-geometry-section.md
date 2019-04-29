---
title: '[RelCubBezTo] 行 ([図形座標] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 77777dd4-5a2c-4048-9ea4-9bd876862963
description: 図形の幅と高さを基準にした三次ベジェ曲線の x 座標と y 座標、図形の幅と高さに相対する曲線の始点のコントロールポイントの x 座標および y 座標、および表示される図形の x 座標と y 座標を格納します。図形の幅と高さを基準にして、曲線の終点の l 点を指定します。
ms.openlocfilehash: cb886706c4c5cbb3488a95b57dcc84e0e45ee326
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430330"
---
# <a name="relcubbezto-row-geometry-section"></a>[RelCubBezTo] 行 ([図形座標] セクション)

図形の幅と高さに相対する3次ベジエ曲線の*x*座標と*y*座標、図形の幅と高さに相対する曲線の始点のコントロールポイントの*x*座標および*y*座標を格納します。この値は、図形の幅と高さを基準にして、曲線の終点のコントロールポイントの*x*座標と*y*座標を指定します。 
  
> [!NOTE]
> [**RelCubBezTo**] 行は、.vsdx、.vsdm、.vstx、.vstm、.vssx、および .vssm のファイル形式でのみ保存できます。 Visio 2003-2010 形式でファイルを保存すると、 **[relcubbezto]** 行は[[nurbsto]](nurbsto-row-geometry-section.md)の行に変換されます。 
  
[**RelCubBezTo**] 行には次のセルが含まれます。 
  
|**Cell**|**説明**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |図形の幅を基準にした3次ベジエ曲線の最後の頂点に対する*x*座標です。  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |図形の高さを基準にした3次ベジエ曲線の最後の頂点に対する*y*座標です。  <br/> |
|[A](a-cell-geometry-section.md) <br/> |図形の幅を基準にした、曲線の開始位置を示す*x*座標を指定します。弧の点を指定します。コントロールポイントは、円弧の始点と終点の間に配置するのが最適です。  <br/> |
|[B](b-cell-geometry-section.md) <br/> |図形の高さを基準にした、曲線の開始位置を示す*y*座標です。  <br/> |
|[C](c-cell-geometry-section.md) <br/> |図形の幅を基準にした曲線の終了位置の*x*座標を指定します。弧の点を指定します。コントロールポイントは、最初のコントロールポイントと円弧の最後の頂点の間に配置するのが最適です。  <br/> |
|[D](d-cell-geometry-section.md) <br/> |図形の高さを基準にした、曲線の終了位置の*y*座標です。  <br/> |
   

