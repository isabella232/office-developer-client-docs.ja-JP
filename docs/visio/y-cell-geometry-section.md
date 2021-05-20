---
title: '[Y] セル ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251750
localization_priority: Normal
ms.assetid: a53b5787-f419-7a36-3c04-c63b3c173ac7
description: ローカル座標の図形の y 座標を表します。 次の表に、各行で [Y] セルが示す内容を説明します。
ms.openlocfilehash: 7dea96b544c84f09abe1d72304da0bacaa09432f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540491"
---
# <a name="y-cell-geometry-section"></a><span data-ttu-id="c90b7-104">[Y] セル ([Geometry] セクション)</span><span class="sxs-lookup"><span data-stu-id="c90b7-104">Y Cell (Geometry Section)</span></span>

<span data-ttu-id="c90b7-105">ローカル座標の  *図形の y*  座標を表します。</span><span class="sxs-lookup"><span data-stu-id="c90b7-105">Represents a  *y*  -coordinate on a shape in local coordinates.</span></span> <span data-ttu-id="c90b7-106">次の表に、各行で [Y] セルが示す内容を説明します。</span><span class="sxs-lookup"><span data-stu-id="c90b7-106">This table describes the Y cell based on the row in which it's located.</span></span> 
  
|<span data-ttu-id="c90b7-107">行</span><span class="sxs-lookup"><span data-stu-id="c90b7-107">Row</span></span>|<span data-ttu-id="c90b7-108">説明</span><span class="sxs-lookup"><span data-stu-id="c90b7-108">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c90b7-109">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="c90b7-109">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="c90b7-110">MoveTo 行がセクションの最初の行である場合、Y セルはパスの最初の頂点の  *y*  座標を表します。</span><span class="sxs-lookup"><span data-stu-id="c90b7-110">If the MoveTo row is the first row in the section, the Y cell represents the  *y*  -coordinate of the first vertex of a path.</span></span> <span data-ttu-id="c90b7-111">MoveTo 行が 2 行の間に表示される場合、Y セルはパスのブレーク後の最初の頂点の  *y*  座標を表します。</span><span class="sxs-lookup"><span data-stu-id="c90b7-111">If the MoveTo row appears between two rows, the Y cell represents the  *y*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
|[<span data-ttu-id="c90b7-112">LineTo</span><span class="sxs-lookup"><span data-stu-id="c90b7-112">LineTo</span></span>](lineto-row-geometry-section.md) <br/> | <span data-ttu-id="c90b7-113">直線  *セグメントの*  終了頂点の y 座標。</span><span class="sxs-lookup"><span data-stu-id="c90b7-113">The  *y*  -coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |
|[<span data-ttu-id="c90b7-114">ArcTo</span><span class="sxs-lookup"><span data-stu-id="c90b7-114">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> | <span data-ttu-id="c90b7-115">円弧  *の終了*  頂点の y 座標。</span><span class="sxs-lookup"><span data-stu-id="c90b7-115">The  *y*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="c90b7-116">楕円ArcTo</span><span class="sxs-lookup"><span data-stu-id="c90b7-116">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="c90b7-117">楕  *円円弧*  の終了頂点の y 座標。</span><span class="sxs-lookup"><span data-stu-id="c90b7-117">The  *y*  -coordinate of the ending vertex of an elliptical arc.</span></span>  <br/> |
|[<span data-ttu-id="c90b7-118">ポリラインTo</span><span class="sxs-lookup"><span data-stu-id="c90b7-118">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> | <span data-ttu-id="c90b7-119">ポリライン  *の終了*  頂点の y 座標。</span><span class="sxs-lookup"><span data-stu-id="c90b7-119">The  *y*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|[<span data-ttu-id="c90b7-120">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="c90b7-120">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="c90b7-121">非  *ユニフォーム*  有理 B スプライン (NURBS) の最後のコントロール ポイントの y 座標。</span><span class="sxs-lookup"><span data-stu-id="c90b7-121">The  *y*  -coordinate of the last control point of a nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="c90b7-122">SplineStart</span><span class="sxs-lookup"><span data-stu-id="c90b7-122">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="c90b7-123">スプライン  *の 2*  番目のコントロール ポイントの y 座標。</span><span class="sxs-lookup"><span data-stu-id="c90b7-123">The  *y*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="c90b7-124">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="c90b7-124">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> | <span data-ttu-id="c90b7-125">コントロール  *ポイントの y*  座標。</span><span class="sxs-lookup"><span data-stu-id="c90b7-125">The  *y*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="c90b7-126">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="c90b7-126">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="c90b7-127">無限  *線上*  の点の y 座標。</span><span class="sxs-lookup"><span data-stu-id="c90b7-127">A  *y-*  coordinate of a point on the infinite line.</span></span>  <br/> |
|[<span data-ttu-id="c90b7-128">楕円</span><span class="sxs-lookup"><span data-stu-id="c90b7-128">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="c90b7-129">楕  *円の*  中心の y 座標。</span><span class="sxs-lookup"><span data-stu-id="c90b7-129">The  *y*  -coordinate of the center of the ellipse.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c90b7-130">注釈</span><span class="sxs-lookup"><span data-stu-id="c90b7-130">Remarks</span></span>

<span data-ttu-id="c90b7-131">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Y] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="c90b7-131">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c90b7-132">セル名:</span><span class="sxs-lookup"><span data-stu-id="c90b7-132">Cell name:</span></span>  <br/> | <span data-ttu-id="c90b7-133">Geometry  *i*  .Y  *j*            *i と*  j =  *<*  1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="c90b7-133">Geometry  *i*  .Y  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="c90b7-134">Geometry  *i*  .Y1 (InfiniteLine 行と楕円行) i  *=*  <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="c90b7-134">Geometry  *i*  .Y1 (InfiniteLine and Ellipse rows)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="c90b7-135">プログラムから、インデックスによって [Y] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="c90b7-135">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c90b7-136">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="c90b7-136">Section index:</span></span>  <br/> |<span data-ttu-id="c90b7-137">**visSectionFirstComponent**  +  *i* *=* 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c90b7-137">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="c90b7-138">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="c90b7-138">Row index:</span></span>  <br/> |<span data-ttu-id="c90b7-139">**visRowVertex**  +  *j* は *j* = 0、1、2..です。</span><span class="sxs-lookup"><span data-stu-id="c90b7-139">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="c90b7-140">**visRowVertex** ([InfiniteLine] 行および [Ellipse] 行)</span><span class="sxs-lookup"><span data-stu-id="c90b7-140">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="c90b7-141">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="c90b7-141">Cell index:</span></span>  <br/> |<span data-ttu-id="c90b7-142">**visY** ([MoveTo]、[LineTo]、[ArcTo]、[EllipticalArcTo]、[NURBSTo]、[Polyline]、[SplineStart]、および [SplineKnot] 行)</span><span class="sxs-lookup"><span data-stu-id="c90b7-142">**visY** (MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart, and SplineKnot rows)</span></span>  <br/> |
||<span data-ttu-id="c90b7-143">**visInfiniteLineY1** ([InfiniteLine] 行)</span><span class="sxs-lookup"><span data-stu-id="c90b7-143">**visInfiniteLineY1** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="c90b7-144">**visEllipseCenterY** ([Ellipse] 行)</span><span class="sxs-lookup"><span data-stu-id="c90b7-144">**visEllipseCenterY** (Ellipse row)</span></span>  <br/> |
   

