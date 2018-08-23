---
title: '[RelCubBezTo] 行 ([図形座標] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 77777dd4-5a2c-4048-9ea4-9bd876862963
description: X と y に対して、図形の幅と高さ、x の 3 次ベジエ曲線の端点の座標のとの曲線の相対的な図形の幅と高さ、および x の先頭のコントロール ポイントの座標の y と y の座標を移動するのl は、曲線の相対的な図形の幅と高さの最後のポイントです。
ms.openlocfilehash: 918701c19e36753dcbf1a210dda2234d1e540d6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806183"
---
# <a name="relcubbezto-row-geometry-section"></a>[RelCubBezTo] 行 ([図形座標] セクション)

*X*と*y*の基準にして図形の幅と高さ、 *x*の 3 次ベジエ曲線の端点の座標および*y*が含まれています-曲線の相対的な図形の幅と高さの最初の制御点の座標および*x*と*y*の曲線の相対的な図形の幅と高さの最後のコントロール ポイントの座標です。 
  
> [!NOTE]
> **RelCubBezTo**行は、.vsdx、.vsdm、.vstx、.vstm、.vssx、および .vssm のファイル形式でのみ保持できます。 ファイル保存すると、Visio 2003 から 2010 年の書式には、 **RelCubBezTo**行が[[nurbsto]](nurbsto-row-geometry-section.md)行に変換されます。 
  
[**RelCubBezTo**] 行には次のセルが含まれます。 
  
|**Cell**|**説明**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |*X* -図形の幅を基準に、3 次ベジエ曲線の終点の座標です。  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |*Y* -図形の高さを基準にして、3 次ベジエ曲線の終点の座標です。  <br/> |
|[A](a-cell-geometry-section.md) <br/> |*X*の曲線の座標は図形の幅を基準にコントロール ポイントを開始の円弧上の点。コントロール ポイントは、最初と最後の円弧の頂点の間で置くが最適です。  <br/> |
|[B](b-cell-geometry-section.md) <br/> |*Y*の曲線の座標は、図形の高さを基準にコントロール ポイントを始めるのです。  <br/> |
|[C](c-cell-geometry-section.md) <br/> |*X*の曲線の座標に図形の幅を基準にコントロール ポイントの終了円弧上の点。コントロール ポイントは、円弧の先頭のコントロール ポイントおよび終了頂点の間で置くが最適です。  <br/> |
|[D](d-cell-geometry-section.md) <br/> |*Y*の座標の曲線の図形の高さを基準にコントロール ポイントを終了します。  <br/> |
   

