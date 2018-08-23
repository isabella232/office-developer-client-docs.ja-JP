---
title: '[SplineStart] 行 ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3055
localization_priority: Normal
ms.assetid: 8e327e00-0844-efa4-900b-6954d3b009bb
description: 含まれています x および y の座標、スプラインの 2 番目の制御点、2 番目のノット、最初のノット、最後のノット、およびスプラインの角度です。
ms.openlocfilehash: 0944da12e6090fde41dc5927b5705e103d29f76d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806559"
---
# <a name="splinestart-row-geometry-section"></a>[SplineStart] 行 ([図形座標] セクション)

*X*および*y*が含まれています-スプラインの 2 番目の制御点、2 番目のノット、最初のノット、最後のノット、およびスプラインの角度の座標です。 
  
[SplineStart] 行には次のセルが含まれます。
  
|**Cell**|**説明**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |*X* -スプラインの 2 番目の制御点の座標です。  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |*Y* -スプラインの 2 番目の制御点の座標です。  <br/> |
|[A](a-cell-geometry-section.md) <br/> |スプラインの 2 番目のノットです。  <br/> |
|[B](b-cell-geometry-section.md) <br/> |スプラインの最初のノットです。  <br/> |
|[C](c-cell-geometry-section.md) <br/> |スプラインの最後のノットです。  <br/> |
|[D](d-cell-geometry-section.md) <br/> |スプラインの角度 (1 ～ 25 の整数) です。  <br/> |
   
## <a name="remarks"></a>備考

Visio では、[SplineKnot] 行が後に続く [SplineStart] 行を格納する [Geometry] セクション内のスプラインの定義を表示します。[SplineStart] 行の前には、スプラインの最初のコントロール ポイントを示す別の行 (たとえば [MoveTo] 行など) が必要です。[LineTo]、[ArcTo]、[NURBSTo]、[PolylineTo]、[EllipticalArcTo] などの行は、その行のセグメントにスプラインが従う場合、[SplineStart] 行の前に置くことができます。
  

