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
# <a name="splineknot-row-geometry-section"></a><span data-ttu-id="a9f32-103">[SplineKnot] 行 ([Geometry] セクション)</span><span class="sxs-lookup"><span data-stu-id="a9f32-103">SplineKnot Row (Geometry Section)</span></span>

<span data-ttu-id="a9f32-104">*X*および*y*が含まれています-座標、スプラインの制御点をスプラインのノットです。</span><span class="sxs-lookup"><span data-stu-id="a9f32-104">Contains  *x*  - and  *y*  -coordinates for a spline's control point and a spline's knot.</span></span> 
  
<span data-ttu-id="a9f32-105">[SplineKnot] 行には次のセルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="a9f32-105">A SplineKnot row contains the following cells.</span></span>
  
|<span data-ttu-id="a9f32-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="a9f32-106">**Cell**</span></span>|<span data-ttu-id="a9f32-107">**説明**</span><span class="sxs-lookup"><span data-stu-id="a9f32-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a9f32-108">X</span><span class="sxs-lookup"><span data-stu-id="a9f32-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="a9f32-109">*X* -コントロール ポイントの座標です。</span><span class="sxs-lookup"><span data-stu-id="a9f32-109">The  *x*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="a9f32-110">Y</span><span class="sxs-lookup"><span data-stu-id="a9f32-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="a9f32-111">*Y*のコントロール ポイントの座標です。</span><span class="sxs-lookup"><span data-stu-id="a9f32-111">The  *y*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="a9f32-112">A</span><span class="sxs-lookup"><span data-stu-id="a9f32-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="a9f32-113">スプラインのノットのいずれか 1 つです (最後のノットと最初の 2 つのノットは除く)。</span><span class="sxs-lookup"><span data-stu-id="a9f32-113">One of the spline's knots (other than the last one or the first two).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a9f32-114">備考</span><span class="sxs-lookup"><span data-stu-id="a9f32-114">Remarks</span></span>

<span data-ttu-id="a9f32-p101">Visio では、[SplineKnot] 行が後に続く [SplineStart] 行を格納する [Geometry] セクション内のスプラインの定義を表示します。[SplineStart] 行の前には、スプラインの最初のコントロール ポイントを示す別の行 (たとえば [MoveTo] 行など) が必要です。[LineTo]、[ArcTo]、[NURBSTo]、[PolylineTo]、[EllipticalArcTo] などの行は、その行のセグメントにスプラインが従う場合、[SplineStart] 行の前に置くことができます。</span><span class="sxs-lookup"><span data-stu-id="a9f32-p101">Visio displays the definition of a spline in a Geometry section that contains a SplineStart row followed by one or more SplineKnot rows. The SplineStart row must be preceded by another kind of row, such as a MoveTo row, to indicate the first control point of the spline. The preceding row can be a LineTo, ArcTo, NURBSTo, PolylineTo, or EllipticalArcTo row if the spline follows a segment of that type.</span></span>
  

