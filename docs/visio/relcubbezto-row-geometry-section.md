---
title: '[RelCubBezTo] 行 ([図形座標] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 77777dd4-5a2c-4048-9ea4-9bd876862963
description: 図形の幅と高さを基準にした 3 次ベジエ曲線の端点の x 座標と y 座標、曲線の幅と高さの先頭のコントロール ポイントの x 座標と y 座標、および曲線相対図形の幅と高さの終了のコントロール ポイントの x 座標と y 座標を格納します。
ms.openlocfilehash: a5a3f0e5550b4f4c003e928299a9d129a808282e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570205"
---
# <a name="relcubbezto-row-geometry-section"></a>[RelCubBezTo] 行 ([図形座標] セクション)

図形の幅と高さを基準にした 3 次ベジエ曲線の端点の x 座標と *y* 座標、曲線の幅と高さの先頭のコントロール ポイントの x 座標と y 座標、および曲線相対図形の幅と高さの終了のコントロール ポイントの *x* 座標と *y* 座標を格納します。  
  
> [!NOTE]
> [**RelCubBezTo**] 行は、.vsdx、.vsdm、.vstx、.vstm、.vssx、および .vssm のファイル形式でのみ保存できます。 ファイルを Visio 2003- 2010 形式に保存すると **、RelCubBezTo** 行は [NURBSTo](nurbsto-row-geometry-section.md)行に変換されます。 
  
[**RelCubBezTo**] 行には次のセルが含まれます。 
  
|**Cell**|**説明**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |図形  *の*  幅に対する 3 次ベジエ曲線の終了頂点の x 座標。  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |図形  *の高*  さに対する 3 次ベジエ曲線の終了頂点の y 座標。  <br/> |
|[A](a-cell-geometry-section.md) <br/> |図形  *の*  幅に対する曲線の開始コントロール ポイントの x 座標。円弧上のポイント。コントロール ポイントは、円弧の開始頂点と終了頂点の間に最適です。  <br/> |
|[B](b-cell-geometry-section.md) <br/> |図形  *の高*  さを基準にした曲線の開始コントロール ポイントの y 座標。  <br/> |
|[C](c-cell-geometry-section.md) <br/> |図形  *の*  幅に対する曲線の終了コントロール ポイントの x 座標。円弧上のポイント。コントロール ポイントは、円弧の開始コントロール ポイントと終了頂点の間に最適です。  <br/> |
|[D](d-cell-geometry-section.md) <br/> |図形  *の高*  さを基準にした曲線の終了コントロール ポイントの y 座標。  <br/> |
   

