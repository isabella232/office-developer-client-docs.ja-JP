---
title: '[SplineStart] 行 ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3055
ms.localizationpriority: medium
ms.assetid: 8e327e00-0844-efa4-900b-6954d3b009bb
description: スプラインの 2 番目のコントロール ポイント、2 番目のノット、最初のノット、最後のノット、スプラインの角度の x 座標と y 座標を含む。
ms.openlocfilehash: 26ef4d10af7dff9376ac214123f1391b38f84dd5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569945"
---
# <a name="splinestart-row-geometry-section"></a>[SplineStart] 行 ([Geometry] セクション)

スプラインの  *2*  番目のコントロール ポイント  *、2*  番目のノット、最初のノット、最後のノット、スプラインの角度の x 座標と y 座標を含む。 
  
[SplineStart] 行には次のセルが含まれます。
  
|**Cell**|**説明**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |スプライン  *の*  2 番目のコントロール ポイントの x 座標。  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |スプライン  *の 2*  番目のコントロール ポイントの y 座標。  <br/> |
|[A](a-cell-geometry-section.md) <br/> |スプラインの 2 番目のノットです。  <br/> |
|[B](b-cell-geometry-section.md) <br/> |スプラインの最初のノットです。  <br/> |
|[C](c-cell-geometry-section.md) <br/> |スプラインの最後のノットです。  <br/> |
|[D](d-cell-geometry-section.md) <br/> |スプラインの角度 (1 ～ 25 の整数) です。  <br/> |
   
## <a name="remarks"></a>注釈

Visio では、[SplineKnot] 行が後に続く [SplineStart] 行を格納する [Geometry] セクション内のスプラインの定義を表示します。[SplineStart] 行の前には、スプラインの最初のコントロール ポイントを示す別の行 (たとえば [MoveTo] 行など) が必要です。[LineTo]、[ArcTo]、[NURBSTo]、[PolylineTo]、[EllipticalArcTo] などの行は、その行のセグメントにスプラインが従う場合、[SplineStart] 行の前に置くことができます。
  

