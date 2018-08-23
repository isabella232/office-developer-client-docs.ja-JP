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
ms.openlocfilehash: b907552c2346292a6b14baf16481b6b40cc80fc4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804740"
---
# <a name="a-cell-geometry-section"></a><span data-ttu-id="49005-104">[A] セル ([図形座標] セクション)</span><span class="sxs-lookup"><span data-stu-id="49005-104">A Cell (Geometry Section)</span></span>

<span data-ttu-id="49005-p102">各行に対応する情報を表示します。次の表に、各行で [A] セルが示す内容を説明します。</span><span class="sxs-lookup"><span data-stu-id="49005-p102">Represents different information in different rows. This table describes the A cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="49005-107">**Row**</span><span class="sxs-lookup"><span data-stu-id="49005-107">**Row**</span></span>|<span data-ttu-id="49005-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="49005-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="49005-109">ArcTo</span><span class="sxs-lookup"><span data-stu-id="49005-109">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> | <span data-ttu-id="49005-110">円弧の中点から弦の中点までの距離です。</span><span class="sxs-lookup"><span data-stu-id="49005-110">The distance from the arc's midpoint to the midpoint of its chord.</span></span>  <br/> |
|[<span data-ttu-id="49005-111">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="49005-111">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="49005-112">*X*の円弧のコントロール ポイント、円弧上の点の座標です。コントロール ポイントは、最初と最後の円弧の頂点の間で途中で最適に配置します。それ以外の場合、円弧は、予期しない結果で、コントロール ポイントを通過するために極端になることがあります。</span><span class="sxs-lookup"><span data-stu-id="49005-112">The  *x*  -coordinate of the arc's control point, a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc. Otherwise, the arc may grow to an extreme size in order to pass through the control point, with unpredictable results.</span></span>  <br/> |
|[<span data-ttu-id="49005-113">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="49005-113">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> | <span data-ttu-id="49005-114">ポリラインの数式です。</span><span class="sxs-lookup"><span data-stu-id="49005-114">The polyline formula.</span></span>  <br/> |
|<span data-ttu-id="49005-115">[[Nurbsto]](nurbsto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="49005-115">[NURBSTo](nurbsto-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="49005-116">NURBS (nonuniform rational B-spline) の最後から 2 番目のノットです。</span><span class="sxs-lookup"><span data-stu-id="49005-116">The second to the last knot of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|<span data-ttu-id="49005-117">[[A](splinestart-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="49005-117">[SplineStart](splinestart-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="49005-118">スプラインの 2 番目のノットです。</span><span class="sxs-lookup"><span data-stu-id="49005-118">The second knot of the spline.</span></span>  <br/> |
|[<span data-ttu-id="49005-119">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="49005-119">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> | <span data-ttu-id="49005-120">スプラインのノットのいずれか 1 つです (最後のノットと最初の 2 つのノットは除く)。</span><span class="sxs-lookup"><span data-stu-id="49005-120">One of the spline's knots (other than the last one or the first two).</span></span>  <br/> |
|[<span data-ttu-id="49005-121">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="49005-121">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="49005-122">*X* -無限の線の上の点の座標対応する*y*の座標は、[ [B](b-cell-geometry-section.md) ] セルで表されます。</span><span class="sxs-lookup"><span data-stu-id="49005-122">An  *x*  -coordinate of a point on the infinite line; paired with  *y*  -coordinate represented by the [B](b-cell-geometry-section.md) cell.</span></span>  <br/> |
|[<span data-ttu-id="49005-123">楕円</span><span class="sxs-lookup"><span data-stu-id="49005-123">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="49005-124">*X* -楕円上の点の座標対応する*y*の座標は、[ [B](b-cell-geometry-section.md) ] セルで表されます。</span><span class="sxs-lookup"><span data-stu-id="49005-124">An  *x*  -coordinate of a point on the ellipse; paired with  *y*  -coordinate represented by the [B](b-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="49005-125">注釈</span><span class="sxs-lookup"><span data-stu-id="49005-125">Remarks</span></span>

<span data-ttu-id="49005-126">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [A] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="49005-126">To get a reference to the A cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="49005-127">セル名:</span><span class="sxs-lookup"><span data-stu-id="49005-127">Cell name:</span></span>  <br/> | <span data-ttu-id="49005-128">ジオメトリの*i*です。*J* 、 *i*および*j* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="49005-128">Geometry  *i*  .A  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="49005-129">ジオメトリの*i*です。A1 (InfiniteLine と楕円の行)、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="49005-129">Geometry  *i*  .A1 (InfiniteLine and Ellipse rows)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="49005-130">プログラムから、インデックスによって [A] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="49005-130">To get a reference to the A cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="49005-131">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="49005-131">Section index:</span></span>  <br/> |<span data-ttu-id="49005-132">**visSectionFirstComponent** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="49005-132">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="49005-133">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="49005-133">Row index:</span></span>  <br/> |<span data-ttu-id="49005-134">**visRowVertex** +  *j* 、 *j* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="49005-134">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="49005-135">**visRowVertex** ([InfiniteLine] 行および [Ellipse] 行)</span><span class="sxs-lookup"><span data-stu-id="49005-135">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="49005-136">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="49005-136">Cell index:</span></span>  <br/> |<span data-ttu-id="49005-137">**visBow** ([ArcTo] 行)</span><span class="sxs-lookup"><span data-stu-id="49005-137">**visBow** (ArcTo row)</span></span>  <br/> |
||<span data-ttu-id="49005-138">**visControlX** ([EllipticalArcTo] 行)</span><span class="sxs-lookup"><span data-stu-id="49005-138">**visControlX** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="49005-139">**visControlY** ([EllipticalArcTo] 行)</span><span class="sxs-lookup"><span data-stu-id="49005-139">**visControlY** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="49005-140">**visPolylineData** ([Polyline] 行)</span><span class="sxs-lookup"><span data-stu-id="49005-140">**visPolylineData** (Polyline row)</span></span>  <br/> |
||<span data-ttu-id="49005-141">**visNURBSKnot** ([NURBSTo] 行)</span><span class="sxs-lookup"><span data-stu-id="49005-141">**visNURBSKnot** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="49005-142">**visSplineKnot** ([SplineStart] 行および [SplineKnot] 行)</span><span class="sxs-lookup"><span data-stu-id="49005-142">**visSplineKnot** (SplineStart and SplineKnot rows)</span></span>  <br/> |
||<span data-ttu-id="49005-143">**visInfiniteLineX2** ([InfiniteLine] 行)</span><span class="sxs-lookup"><span data-stu-id="49005-143">**visInfiniteLineX2** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="49005-144">**visEllipseMajorX** ([Ellipse] 行)</span><span class="sxs-lookup"><span data-stu-id="49005-144">**visEllipseMajorX** (Ellipse row)</span></span>  <br/> |
   

