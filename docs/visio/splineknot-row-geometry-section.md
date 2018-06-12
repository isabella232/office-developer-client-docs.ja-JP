---
title: '[SplineKnot] 行 ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm3050
localization_priority: Normal
ms.assetid: 9fbae27d-4f1b-c5f7-aacb-16f359331e83
description: 含まれています x および y の座標、スプラインの制御点をスプラインのノットです。
ms.openlocfilehash: 297889208e064870dd37ed45a17fef7cb4b333b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806557"
---
# <a name="splineknot-row-geometry-section"></a>[SplineKnot] 行 ([Geometry] セクション)

*X*および*y*が含まれています-座標、スプラインの制御点をスプラインのノットです。 
  
[SplineKnot] 行には次のセルが含まれます。
  
|**Cell**|**説明**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |*X* -コントロール ポイントの座標です。  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |*Y*のコントロール ポイントの座標です。  <br/> |
|[A](a-cell-geometry-section.md) <br/> |スプラインのノットのいずれか 1 つです (最後のノットと最初の 2 つのノットは除く)。  <br/> |
   
## <a name="remarks"></a>備考

Visio では、[SplineKnot] 行が後に続く [SplineStart] 行を格納する [Geometry] セクション内のスプラインの定義を表示します。[SplineStart] 行の前には、スプラインの最初のコントロール ポイントを示す別の行 (たとえば [MoveTo] 行など) が必要です。[LineTo]、[ArcTo]、[NURBSTo]、[PolylineTo]、[EllipticalArcTo] などの行は、その行のセグメントにスプラインが従う場合、[SplineStart] 行の前に置くことができます。
  

