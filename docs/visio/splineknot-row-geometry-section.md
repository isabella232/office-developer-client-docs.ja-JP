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
description: スプラインのコントロール ポイントとスプラインのノットの x 座標と y 座標を含む。
ms.openlocfilehash: 432b714772d96e0ab0861bbfb62075258404e607
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407418"
---
# <a name="splineknot-row-geometry-section"></a><span data-ttu-id="c14e7-103">[SplineKnot] 行 ([Geometry] セクション)</span><span class="sxs-lookup"><span data-stu-id="c14e7-103">SplineKnot Row (Geometry Section)</span></span>

<span data-ttu-id="c14e7-104">スプラインの  *コントロール ポイント*  とスプラインのノットの x 座標と  *y*  座標を含む。</span><span class="sxs-lookup"><span data-stu-id="c14e7-104">Contains  *x*  - and  *y*  -coordinates for a spline's control point and a spline's knot.</span></span> 
  
<span data-ttu-id="c14e7-105">[SplineKnot] 行には次のセルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="c14e7-105">A SplineKnot row contains the following cells.</span></span>
  
|<span data-ttu-id="c14e7-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="c14e7-106">**Cell**</span></span>|<span data-ttu-id="c14e7-107">**説明**</span><span class="sxs-lookup"><span data-stu-id="c14e7-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c14e7-108">X</span><span class="sxs-lookup"><span data-stu-id="c14e7-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="c14e7-109">コントロール  *ポイントの x*  座標。</span><span class="sxs-lookup"><span data-stu-id="c14e7-109">The  *x*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="c14e7-110">Y</span><span class="sxs-lookup"><span data-stu-id="c14e7-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="c14e7-111">コントロール  *ポイントの y*  座標。</span><span class="sxs-lookup"><span data-stu-id="c14e7-111">The  *y*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="c14e7-112">A</span><span class="sxs-lookup"><span data-stu-id="c14e7-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="c14e7-113">スプラインのノットのいずれか 1 つです (最後のノットと最初の 2 つのノットは除く)。</span><span class="sxs-lookup"><span data-stu-id="c14e7-113">One of the spline's knots (other than the last one or the first two).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c14e7-114">注釈</span><span class="sxs-lookup"><span data-stu-id="c14e7-114">Remarks</span></span>

<span data-ttu-id="c14e7-p101">Visio では、[SplineKnot] 行が後に続く [SplineStart] 行を格納する [Geometry] セクション内のスプラインの定義を表示します。[SplineStart] 行の前には、スプラインの最初のコントロール ポイントを示す別の行 (たとえば [MoveTo] 行など) が必要です。[LineTo]、[ArcTo]、[NURBSTo]、[PolylineTo]、[EllipticalArcTo] などの行は、その行のセグメントにスプラインが従う場合、[SplineStart] 行の前に置くことができます。</span><span class="sxs-lookup"><span data-stu-id="c14e7-p101">Visio displays the definition of a spline in a Geometry section that contains a SplineStart row followed by one or more SplineKnot rows. The SplineStart row must be preceded by another kind of row, such as a MoveTo row, to indicate the first control point of the spline. The preceding row can be a LineTo, ArcTo, NURBSTo, PolylineTo, or EllipticalArcTo row if the spline follows a segment of that type.</span></span>
  

