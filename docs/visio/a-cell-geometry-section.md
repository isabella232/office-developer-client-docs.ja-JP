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
description: 各行に対応する情報を表示します。 次の表に、各行で [A] セルが示す内容を説明します。
ms.openlocfilehash: 42f346b06cad827cfe56fc113a8387d1a31a6867
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432920"
---
# <a name="a-cell-geometry-section"></a><span data-ttu-id="c54d4-104">[A] セル ([Geometry] セクション)</span><span class="sxs-lookup"><span data-stu-id="c54d4-104">A Cell (Geometry Section)</span></span>

<span data-ttu-id="c54d4-105">各行に対応する情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="c54d4-105">Represents different information in different rows.</span></span> <span data-ttu-id="c54d4-106">次の表に、各行で [A] セルが示す内容を説明します。</span><span class="sxs-lookup"><span data-stu-id="c54d4-106">This table describes the A cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="c54d4-107">**Row**</span><span class="sxs-lookup"><span data-stu-id="c54d4-107">**Row**</span></span>|<span data-ttu-id="c54d4-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="c54d4-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c54d4-109">[[arcto]](arcto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="c54d4-109">[ArcTo](arcto-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="c54d4-110">円弧の中点から弦の中点までの距離です。</span><span class="sxs-lookup"><span data-stu-id="c54d4-110">The distance from the arc's midpoint to the midpoint of its chord.</span></span>  <br/> |
|<span data-ttu-id="c54d4-111">[[ellipticalarcto]](ellipticalarcto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="c54d4-111">[EllipticalArcTo](ellipticalarcto-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="c54d4-112">円弧のコントロールポイントの*x*座標 (円弧上の点)。コントロールポイントは、円弧の始点と終点の間の中間点を中心に配置されます。それ以外の場合、円弧はコントロールポイントを通過するために極端なサイズまで拡大することがあり、予期しない結果が発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="c54d4-112">The  *x*  -coordinate of the arc's control point, a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc. Otherwise, the arc may grow to an extreme size in order to pass through the control point, with unpredictable results.</span></span>  <br/> |
|<span data-ttu-id="c54d4-113">[[polylineto]](polylineto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="c54d4-113">[PolylineTo](polylineto-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="c54d4-114">ポリラインの数式です。</span><span class="sxs-lookup"><span data-stu-id="c54d4-114">The polyline formula.</span></span>  <br/> |
|<span data-ttu-id="c54d4-115">[[nurbsto]](nurbsto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="c54d4-115">[NURBSTo](nurbsto-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="c54d4-116">NURBS (nonuniform rational B-spline) の最後から 2 番目のノットです。</span><span class="sxs-lookup"><span data-stu-id="c54d4-116">The second to the last knot of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|<span data-ttu-id="c54d4-117">[[splinestart]](splinestart-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="c54d4-117">[SplineStart](splinestart-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="c54d4-118">スプラインの 2 番目のノットです。</span><span class="sxs-lookup"><span data-stu-id="c54d4-118">The second knot of the spline.</span></span>  <br/> |
|<span data-ttu-id="c54d4-119">[[splineknot]](splineknot-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="c54d4-119">[SplineKnot](splineknot-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="c54d4-120">スプラインのノットのいずれか 1 つです (最後のノットと最初の 2 つのノットは除く)。</span><span class="sxs-lookup"><span data-stu-id="c54d4-120">One of the spline's knots (other than the last one or the first two).</span></span>  <br/> |
|<span data-ttu-id="c54d4-121">[[infiniteline]](infiniteline-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="c54d4-121">[InfiniteLine](infiniteline-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="c54d4-122">無限線上の点の*x*座標です。対応する*y*座標は [ [B](b-cell-geometry-section.md)セルで表されます。</span><span class="sxs-lookup"><span data-stu-id="c54d4-122">An  *x*  -coordinate of a point on the infinite line; paired with  *y*  -coordinate represented by the [B](b-cell-geometry-section.md) cell.</span></span>  <br/> |
|[<span data-ttu-id="c54d4-123">もう</span><span class="sxs-lookup"><span data-stu-id="c54d4-123">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="c54d4-124">楕円上の点の*x*座標です。対応する*y*座標は [ [B](b-cell-geometry-section.md)セルで表されます。</span><span class="sxs-lookup"><span data-stu-id="c54d4-124">An  *x*  -coordinate of a point on the ellipse; paired with  *y*  -coordinate represented by the [B](b-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c54d4-125">注釈</span><span class="sxs-lookup"><span data-stu-id="c54d4-125">Remarks</span></span>

<span data-ttu-id="c54d4-126">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [A] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="c54d4-126">To get a reference to the A cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c54d4-127">セル名:</span><span class="sxs-lookup"><span data-stu-id="c54d4-127">Cell name:</span></span>  <br/> | <span data-ttu-id="c54d4-128">ジオメトリ*i\*\*j* 、 *i*および*j* = <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="c54d4-128">Geometry  *i*  .A  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="c54d4-129">ジオメトリ*i*A1 ([infiniteline] および楕円の行) *i* = <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="c54d4-129">Geometry  *i*  .A1 (InfiniteLine and Ellipse rows)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="c54d4-130">プログラムから、インデックスによって [A] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="c54d4-130">To get a reference to the A cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c54d4-131">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="c54d4-131">Section index:</span></span>  <br/> |<span data-ttu-id="c54d4-132">**visSectionFirstComponent** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="c54d4-132">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="c54d4-133">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="c54d4-133">Row index:</span></span>  <br/> |<span data-ttu-id="c54d4-134">**visRowVertex** +  *j* where *j* = 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="c54d4-134">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="c54d4-135">**visRowVertex** ([InfiniteLine] 行および [Ellipse] 行)</span><span class="sxs-lookup"><span data-stu-id="c54d4-135">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="c54d4-136">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="c54d4-136">Cell index:</span></span>  <br/> |<span data-ttu-id="c54d4-137">**visBow** ([ArcTo] 行)</span><span class="sxs-lookup"><span data-stu-id="c54d4-137">**visBow** (ArcTo row)</span></span>  <br/> |
||<span data-ttu-id="c54d4-138">**visControlX** ([EllipticalArcTo] 行)</span><span class="sxs-lookup"><span data-stu-id="c54d4-138">**visControlX** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="c54d4-139">**visControlY** ([EllipticalArcTo] 行)</span><span class="sxs-lookup"><span data-stu-id="c54d4-139">**visControlY** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="c54d4-140">**visPolylineData** ([Polyline] 行)</span><span class="sxs-lookup"><span data-stu-id="c54d4-140">**visPolylineData** (Polyline row)</span></span>  <br/> |
||<span data-ttu-id="c54d4-141">**visNURBSKnot** ([NURBSTo] 行)</span><span class="sxs-lookup"><span data-stu-id="c54d4-141">**visNURBSKnot** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="c54d4-142">**visSplineKnot** ([SplineStart] 行および [SplineKnot] 行)</span><span class="sxs-lookup"><span data-stu-id="c54d4-142">**visSplineKnot** (SplineStart and SplineKnot rows)</span></span>  <br/> |
||<span data-ttu-id="c54d4-143">**visInfiniteLineX2** ([InfiniteLine] 行)</span><span class="sxs-lookup"><span data-stu-id="c54d4-143">**visInfiniteLineX2** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="c54d4-144">**visEllipseMajorX** ([Ellipse] 行)</span><span class="sxs-lookup"><span data-stu-id="c54d4-144">**visEllipseMajorX** (Ellipse row)</span></span>  <br/> |
   

