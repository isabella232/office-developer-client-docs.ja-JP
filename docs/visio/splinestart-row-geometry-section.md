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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358794"
---
# <a name="splinestart-row-geometry-section"></a><span data-ttu-id="6bd36-103">[SplineStart] 行 ([Geometry] セクション)</span><span class="sxs-lookup"><span data-stu-id="6bd36-103">SplineStart Row (Geometry Section)</span></span>

<span data-ttu-id="6bd36-104">スプラインの2番目のコントロールポイントに対する*x*座標と*y*座標、2番目のノット、最初のノット、最後のノット、およびスプラインの角度を格納します。</span><span class="sxs-lookup"><span data-stu-id="6bd36-104">Contains  *x*  - and  *y*  -coordinates for a spline's second control point, its second knot, its first knot, the last knot, and the degree of the spline.</span></span> 
  
<span data-ttu-id="6bd36-105">[SplineStart] 行には次のセルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="6bd36-105">A SplineStart row contains the following cells.</span></span>
  
|<span data-ttu-id="6bd36-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="6bd36-106">**Cell**</span></span>|<span data-ttu-id="6bd36-107">**説明**</span><span class="sxs-lookup"><span data-stu-id="6bd36-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6bd36-108">X</span><span class="sxs-lookup"><span data-stu-id="6bd36-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="6bd36-109">スプラインの2番目のコントロールポイントに対する*x*座標です。</span><span class="sxs-lookup"><span data-stu-id="6bd36-109">The  *x*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="6bd36-110">Y</span><span class="sxs-lookup"><span data-stu-id="6bd36-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="6bd36-111">スプラインの2番目のコントロールポイントに対する*y*座標です。</span><span class="sxs-lookup"><span data-stu-id="6bd36-111">The  *y*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="6bd36-112">A</span><span class="sxs-lookup"><span data-stu-id="6bd36-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="6bd36-113">スプラインの 2 番目のノットです。</span><span class="sxs-lookup"><span data-stu-id="6bd36-113">The second knot of the spline.</span></span>  <br/> |
|[<span data-ttu-id="6bd36-114">B</span><span class="sxs-lookup"><span data-stu-id="6bd36-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="6bd36-115">スプラインの最初のノットです。</span><span class="sxs-lookup"><span data-stu-id="6bd36-115">The first knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="6bd36-116">C</span><span class="sxs-lookup"><span data-stu-id="6bd36-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="6bd36-117">スプラインの最後のノットです。</span><span class="sxs-lookup"><span data-stu-id="6bd36-117">The last knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="6bd36-118">D</span><span class="sxs-lookup"><span data-stu-id="6bd36-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="6bd36-119">スプラインの角度 (1 ～ 25 の整数) です。</span><span class="sxs-lookup"><span data-stu-id="6bd36-119">The degree of a spline (an integer from 1 to 25).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6bd36-120">解説</span><span class="sxs-lookup"><span data-stu-id="6bd36-120">Remarks</span></span>

<span data-ttu-id="6bd36-p101">Visio では、[SplineKnot] 行が後に続く [SplineStart] 行を格納する [Geometry] セクション内のスプラインの定義を表示します。[SplineStart] 行の前には、スプラインの最初のコントロール ポイントを示す別の行 (たとえば [MoveTo] 行など) が必要です。[LineTo]、[ArcTo]、[NURBSTo]、[PolylineTo]、[EllipticalArcTo] などの行は、その行のセグメントにスプラインが従う場合、[SplineStart] 行の前に置くことができます。</span><span class="sxs-lookup"><span data-stu-id="6bd36-p101">Visio displays the definition of a spline in a Geometry section that contains a SplineStart row followed by one or more SplineKnot rows. The SplineStart row must be preceded by another kind of row, such as a MoveTo row, to indicate the first control point of the spline. The preceding row can be a LineTo, ArcTo, NURBSTo, PolylineTo, or EllipticalArcTo row if the spline follows a segment of that type.</span></span>
  

