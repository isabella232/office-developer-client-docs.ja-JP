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
description: スプラインの 2 番目のコントロール ポイント、2 番目のノット、最初のノット、最後のノット、スプラインの角度の x 座標と y 座標を含む。
ms.openlocfilehash: 2ec06619770af4e5dbcc1a763595b6e01a39052b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417477"
---
# <a name="splinestart-row-geometry-section"></a><span data-ttu-id="cd43e-103">[SplineStart] 行 ([Geometry] セクション)</span><span class="sxs-lookup"><span data-stu-id="cd43e-103">SplineStart Row (Geometry Section)</span></span>

<span data-ttu-id="cd43e-104">スプラインの  *2*  番目のコントロール ポイント  *、2*  番目のノット、最初のノット、最後のノット、スプラインの角度の x 座標と y 座標を含む。</span><span class="sxs-lookup"><span data-stu-id="cd43e-104">Contains  *x*  - and  *y*  -coordinates for a spline's second control point, its second knot, its first knot, the last knot, and the degree of the spline.</span></span> 
  
<span data-ttu-id="cd43e-105">[SplineStart] 行には次のセルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="cd43e-105">A SplineStart row contains the following cells.</span></span>
  
|<span data-ttu-id="cd43e-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="cd43e-106">**Cell**</span></span>|<span data-ttu-id="cd43e-107">**説明**</span><span class="sxs-lookup"><span data-stu-id="cd43e-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cd43e-108">X</span><span class="sxs-lookup"><span data-stu-id="cd43e-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="cd43e-109">スプライン  *の*  2 番目のコントロール ポイントの x 座標。</span><span class="sxs-lookup"><span data-stu-id="cd43e-109">The  *x*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="cd43e-110">Y</span><span class="sxs-lookup"><span data-stu-id="cd43e-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="cd43e-111">スプライン  *の 2*  番目のコントロール ポイントの y 座標。</span><span class="sxs-lookup"><span data-stu-id="cd43e-111">The  *y*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="cd43e-112">A</span><span class="sxs-lookup"><span data-stu-id="cd43e-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="cd43e-113">スプラインの 2 番目のノットです。</span><span class="sxs-lookup"><span data-stu-id="cd43e-113">The second knot of the spline.</span></span>  <br/> |
|[<span data-ttu-id="cd43e-114">B</span><span class="sxs-lookup"><span data-stu-id="cd43e-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="cd43e-115">スプラインの最初のノットです。</span><span class="sxs-lookup"><span data-stu-id="cd43e-115">The first knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="cd43e-116">C</span><span class="sxs-lookup"><span data-stu-id="cd43e-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="cd43e-117">スプラインの最後のノットです。</span><span class="sxs-lookup"><span data-stu-id="cd43e-117">The last knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="cd43e-118">D</span><span class="sxs-lookup"><span data-stu-id="cd43e-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="cd43e-119">スプラインの角度 (1 ～ 25 の整数) です。</span><span class="sxs-lookup"><span data-stu-id="cd43e-119">The degree of a spline (an integer from 1 to 25).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cd43e-120">注釈</span><span class="sxs-lookup"><span data-stu-id="cd43e-120">Remarks</span></span>

<span data-ttu-id="cd43e-p101">Visio では、[SplineKnot] 行が後に続く [SplineStart] 行を格納する [Geometry] セクション内のスプラインの定義を表示します。[SplineStart] 行の前には、スプラインの最初のコントロール ポイントを示す別の行 (たとえば [MoveTo] 行など) が必要です。[LineTo]、[ArcTo]、[NURBSTo]、[PolylineTo]、[EllipticalArcTo] などの行は、その行のセグメントにスプラインが従う場合、[SplineStart] 行の前に置くことができます。</span><span class="sxs-lookup"><span data-stu-id="cd43e-p101">Visio displays the definition of a spline in a Geometry section that contains a SplineStart row followed by one or more SplineKnot rows. The SplineStart row must be preceded by another kind of row, such as a MoveTo row, to indicate the first control point of the spline. The preceding row can be a LineTo, ArcTo, NURBSTo, PolylineTo, or EllipticalArcTo row if the spline follows a segment of that type.</span></span>
  

