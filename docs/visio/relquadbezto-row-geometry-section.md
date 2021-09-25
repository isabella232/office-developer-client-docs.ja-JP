---
title: '[RelQuadBezTo] 行 ([図形座標] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 5ae57707-5a50-43f0-8c78-516790b5034e
description: 図形の幅と高さに対する 2 次ベジエ曲線の端点の x 座標と y 座標、および図形の幅と高さを基準にした曲線のコントロール ポイントの x 座標と y 座標を格納します。
ms.openlocfilehash: dd555b85a09a7cc01e84967b96f31a08aaa783d6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573545"
---
# <a name="relquadbezto-row-geometry-section"></a>[RelQuadBezTo] 行 ([図形座標] セクション)

図形の幅と高さに対する 2 次ベジエ曲線の端点の x 座標と *y* 座標、および図形の幅と高さを基準にした曲線のコントロール ポイントの *x* 座標と *y* 座標を格納します。 
  
> [!NOTE]
> [**RelQuadBezTo**] 行は、.vsdx、.vsdm、.vstx、.vstm、.vssx、および .vssm のファイル形式でのみ保存できます。 ファイルを 2003 から 2010 の Visio 形式に保存すると **、RelQuadBezTo** 行は [NURBSTo](nurbsto-row-geometry-section.md)行に変換されます。 
  
[**RelQuadBezTo**] 行には次のセルが含まれます。 
  
|**Cell**|**説明**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |図形  *の*  幅に対する 2 次ベジエ曲線の終了頂点の x 座標。  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |図形  *の高*  さを基準にした 2 次ベジエ曲線の終了頂点の y 座標。  <br/> |
|[A](a-cell-geometry-section.md) <br/> |図形  *の*  幅を基準にした曲線のコントロール ポイントの x 座標。円弧上のポイント。コントロール ポイントは、円弧の開始頂点と終了頂点の約半分の位置に最適です。  <br/> |
|[B](b-cell-geometry-section.md) <br/> |図形  *の高*  さを基準にした曲線のコントロール ポイントの y 座標。  <br/> |
   

