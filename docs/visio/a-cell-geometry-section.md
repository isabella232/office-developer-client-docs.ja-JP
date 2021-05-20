---
title: '[A] セル ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm51215
localization_priority: Normal
ms.assetid: 6853df0f-d22e-89ca-7d34-342b9c0bea23
description: 各行に対応する情報を表示します。次の表に、各行で [A] セルが示す内容を説明します。
ms.openlocfilehash: 7009658c7a6844a5c6071f502c05114a4accd7b7
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541303"
---
# <a name="a-cell-geometry-section"></a><span data-ttu-id="bb110-104">[A] セル ([Geometry] セクション)</span><span class="sxs-lookup"><span data-stu-id="bb110-104">A Cell (Geometry Section)</span></span>

<span data-ttu-id="bb110-p102">各行に対応する情報を表示します。次の表に、各行で [A] セルが示す内容を説明します。</span><span class="sxs-lookup"><span data-stu-id="bb110-p102">Represents different information in different rows. This table describes the A cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="bb110-107">行</span><span class="sxs-lookup"><span data-stu-id="bb110-107">Row</span></span>|<span data-ttu-id="bb110-108">説明</span><span class="sxs-lookup"><span data-stu-id="bb110-108">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bb110-109">ArcTo</span><span class="sxs-lookup"><span data-stu-id="bb110-109">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> | <span data-ttu-id="bb110-110">円弧の中点から弦の中点までの距離です。</span><span class="sxs-lookup"><span data-stu-id="bb110-110">The distance from the arc's midpoint to the midpoint of its chord.</span></span>  <br/> |
|[<span data-ttu-id="bb110-111">楕円ArcTo</span><span class="sxs-lookup"><span data-stu-id="bb110-111">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="bb110-112">円弧  *の*  コントロール ポイントの x 座標、円弧上の点。コントロール ポイントは、円弧の開始頂点と終了頂点の約半分の位置に最適です。それ以外の場合、コントロール ポイントを通過するために極端なサイズにアークが大きくなる可能性があります。予期しない結果が得られます。</span><span class="sxs-lookup"><span data-stu-id="bb110-112">The  *x*  -coordinate of the arc's control point, a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc. Otherwise, the arc may grow to an extreme size in order to pass through the control point, with unpredictable results.</span></span>  <br/> |
|[<span data-ttu-id="bb110-113">ポリラインTo</span><span class="sxs-lookup"><span data-stu-id="bb110-113">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> | <span data-ttu-id="bb110-114">ポリラインの数式です。</span><span class="sxs-lookup"><span data-stu-id="bb110-114">The polyline formula.</span></span>  <br/> |
|[<span data-ttu-id="bb110-115">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="bb110-115">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="bb110-116">NURBS (nonuniform rational B-spline) の最後から 2 番目のノットです。</span><span class="sxs-lookup"><span data-stu-id="bb110-116">The second to the last knot of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="bb110-117">SplineStart</span><span class="sxs-lookup"><span data-stu-id="bb110-117">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="bb110-118">スプラインの 2 番目のノットです。</span><span class="sxs-lookup"><span data-stu-id="bb110-118">The second knot of the spline.</span></span>  <br/> |
|[<span data-ttu-id="bb110-119">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="bb110-119">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> | <span data-ttu-id="bb110-120">スプラインのノットのいずれか 1 つです (最後のノットと最初の 2 つのノットは除く)。</span><span class="sxs-lookup"><span data-stu-id="bb110-120">One of the spline's knots (other than the last one or the first two).</span></span>  <br/> |
|[<span data-ttu-id="bb110-121">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="bb110-121">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="bb110-122">無限  *線*  上の点の x 座標。B セルで  *表される y*  座標と組み [合](b-cell-geometry-section.md) わせ。</span><span class="sxs-lookup"><span data-stu-id="bb110-122">An  *x*  -coordinate of a point on the infinite line; paired with  *y*  -coordinate represented by the [B](b-cell-geometry-section.md) cell.</span></span>  <br/> |
|[<span data-ttu-id="bb110-123">楕円</span><span class="sxs-lookup"><span data-stu-id="bb110-123">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="bb110-124">楕  *円上*  の点の x 座標。B セルで  *表される y*  座標と組み [合](b-cell-geometry-section.md) わせ。</span><span class="sxs-lookup"><span data-stu-id="bb110-124">An  *x*  -coordinate of a point on the ellipse; paired with  *y*  -coordinate represented by the [B](b-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bb110-125">注釈</span><span class="sxs-lookup"><span data-stu-id="bb110-125">Remarks</span></span>

<span data-ttu-id="bb110-126">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [A] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="bb110-126">To get a reference to the A cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bb110-127">セル名:</span><span class="sxs-lookup"><span data-stu-id="bb110-127">Cell name:</span></span>  <br/> | <span data-ttu-id="bb110-128">Geometry  *i*  .i  *と*            *j*  =  *<*  1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="bb110-128">Geometry  *i*  .A  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="bb110-129">Geometry  *i*  .A1 (InfiniteLine 行と楕円行) i  *=*  <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="bb110-129">Geometry  *i*  .A1 (InfiniteLine and Ellipse rows)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="bb110-130">プログラムから、インデックスによって [A] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="bb110-130">To get a reference to the A cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bb110-131">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="bb110-131">Section index:</span></span>  <br/> |<span data-ttu-id="bb110-132">**visSectionFirstComponent**  +  *i* *=* 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="bb110-132">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="bb110-133">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="bb110-133">Row index:</span></span>  <br/> |<span data-ttu-id="bb110-134">**visRowVertex**  +  *j* は *j* = 0、1、2..です。</span><span class="sxs-lookup"><span data-stu-id="bb110-134">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="bb110-135">**visRowVertex** ([InfiniteLine] 行および [Ellipse] 行)</span><span class="sxs-lookup"><span data-stu-id="bb110-135">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="bb110-136">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="bb110-136">Cell index:</span></span>  <br/> |<span data-ttu-id="bb110-137">**visBow** ([ArcTo] 行)</span><span class="sxs-lookup"><span data-stu-id="bb110-137">**visBow** (ArcTo row)</span></span>  <br/> |
||<span data-ttu-id="bb110-138">**visControlX** ([EllipticalArcTo] 行)</span><span class="sxs-lookup"><span data-stu-id="bb110-138">**visControlX** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="bb110-139">**visControlY** ([EllipticalArcTo] 行)</span><span class="sxs-lookup"><span data-stu-id="bb110-139">**visControlY** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="bb110-140">**visPolylineData** ([Polyline] 行)</span><span class="sxs-lookup"><span data-stu-id="bb110-140">**visPolylineData** (Polyline row)</span></span>  <br/> |
||<span data-ttu-id="bb110-141">**visNURBSKnot** ([NURBSTo] 行)</span><span class="sxs-lookup"><span data-stu-id="bb110-141">**visNURBSKnot** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="bb110-142">**visSplineKnot** ([SplineStart] 行および [SplineKnot] 行)</span><span class="sxs-lookup"><span data-stu-id="bb110-142">**visSplineKnot** (SplineStart and SplineKnot rows)</span></span>  <br/> |
||<span data-ttu-id="bb110-143">**visInfiniteLineX2** ([InfiniteLine] 行)</span><span class="sxs-lookup"><span data-stu-id="bb110-143">**visInfiniteLineX2** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="bb110-144">**visEllipseMajorX** ([Ellipse] 行)</span><span class="sxs-lookup"><span data-stu-id="bb110-144">**visEllipseMajorX** (Ellipse row)</span></span>  <br/> |
   

