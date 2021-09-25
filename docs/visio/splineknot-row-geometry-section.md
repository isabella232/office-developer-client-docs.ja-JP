---
title: '[SplineKnot] 行 ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm3050
ms.localizationpriority: medium
ms.assetid: 9fbae27d-4f1b-c5f7-aacb-16f359331e83
description: スプラインのコントロール ポイントとスプラインのノットの x 座標と y 座標を含む。
ms.openlocfilehash: e2fb84bbd269768e3bd7f85874bb8f8865ea8d94
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559462"
---
# <a name="splineknot-row-geometry-section"></a>[SplineKnot] 行 ([Geometry] セクション)

スプラインの  *コントロール ポイント*  とスプラインのノットの x 座標と  *y*  座標を含む。 
  
[SplineKnot] 行には次のセルが含まれます。
  
|**Cell**|**説明**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |コントロール  *ポイントの x*  座標。  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |コントロール  *ポイントの y*  座標。  <br/> |
|[A](a-cell-geometry-section.md) <br/> |スプラインのノットのいずれか 1 つです (最後のノットと最初の 2 つのノットは除く)。  <br/> |
   
## <a name="remarks"></a>注釈

Visio では、[SplineKnot] 行が後に続く [SplineStart] 行を格納する [Geometry] セクション内のスプラインの定義を表示します。[SplineStart] 行の前には、スプラインの最初のコントロール ポイントを示す別の行 (たとえば [MoveTo] 行など) が必要です。[LineTo]、[ArcTo]、[NURBSTo]、[PolylineTo]、[EllipticalArcTo] などの行は、その行のセグメントにスプラインが従う場合、[SplineStart] 行の前に置くことができます。
  

