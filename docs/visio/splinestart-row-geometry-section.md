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
description: スプラインの2番目のコントロールポイントに対する x 座標と y 座標、2番目のノット、最初のノット、最後のノット、およびスプラインの角度を格納します。
ms.openlocfilehash: 2ec06619770af4e5dbcc1a763595b6e01a39052b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417477"
---
# <a name="splinestart-row-geometry-section"></a>[SplineStart] 行 ([Geometry] セクション)

スプラインの2番目のコントロールポイントに対する*x*座標と*y*座標、2番目のノット、最初のノット、最後のノット、およびスプラインの角度を格納します。 
  
[SplineStart] 行には次のセルが含まれます。
  
|**Cell**|**説明**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |スプラインの2番目のコントロールポイントに対する*x*座標です。  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |スプラインの2番目のコントロールポイントに対する*y*座標です。  <br/> |
|[A](a-cell-geometry-section.md) <br/> |スプラインの 2 番目のノットです。  <br/> |
|[B](b-cell-geometry-section.md) <br/> |スプラインの最初のノットです。  <br/> |
|[C](c-cell-geometry-section.md) <br/> |スプラインの最後のノットです。  <br/> |
|[D](d-cell-geometry-section.md) <br/> |スプラインの角度 (1 ～ 25 の整数) です。  <br/> |
   
## <a name="remarks"></a>注釈

Visio では、[SplineKnot] 行が後に続く [SplineStart] 行を格納する [Geometry] セクション内のスプラインの定義を表示します。[SplineStart] 行の前には、スプラインの最初のコントロール ポイントを示す別の行 (たとえば [MoveTo] 行など) が必要です。[LineTo]、[ArcTo]、[NURBSTo]、[PolylineTo]、[EllipticalArcTo] などの行は、その行のセグメントにスプラインが従う場合、[SplineStart] 行の前に置くことができます。
  

