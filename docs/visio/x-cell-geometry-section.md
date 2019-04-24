---
title: '[X] セル ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1135
localization_priority: Normal
ms.assetid: 2416b323-e084-18e1-c9be-a797078dfab9
description: ローカル座標での図形の x 座標を表します。 次の表に、各行で [X] セルが示す内容を説明します。
ms.openlocfilehash: 6554000a86a6bf27d343a5647161bbe416725e64
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285113"
---
# <a name="x-cell-geometry-section"></a><span data-ttu-id="2f8cb-104">[X] セル ([Geometry] セクション)</span><span class="sxs-lookup"><span data-stu-id="2f8cb-104">X Cell (Geometry Section)</span></span>

<span data-ttu-id="2f8cb-105">ローカル座標での図形の*x*座標を表します。</span><span class="sxs-lookup"><span data-stu-id="2f8cb-105">Represents an  *x*  -coordinate on a shape in local coordinates.</span></span> <span data-ttu-id="2f8cb-106">次の表に、各行で [X] セルが示す内容を説明します。</span><span class="sxs-lookup"><span data-stu-id="2f8cb-106">This table describes the X cell based on the row in which it's located.</span></span> 
  
|<span data-ttu-id="2f8cb-107">**行**</span><span class="sxs-lookup"><span data-stu-id="2f8cb-107">**Row**</span></span>|<span data-ttu-id="2f8cb-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="2f8cb-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2f8cb-109">MoveTo</span><span class="sxs-lookup"><span data-stu-id="2f8cb-109">MoveTo</span></span>](moveto-row-geometry-section.md) <br/> | <span data-ttu-id="2f8cb-110">[MoveTo] 行がセクションの最初の行の場合、[x] セルは、パスの最初の頂点に対する*x*座標を表します。</span><span class="sxs-lookup"><span data-stu-id="2f8cb-110">If the MoveTo row is the first row in the section, the X cell represents the  *x*  -coordinate of the first vertex of a path.</span></span> <span data-ttu-id="2f8cb-111">[MoveTo] 行が2つの行の間に表示される場合、[x] セルは、パスを切断した後の最初の頂点に対する*x*座標を表します。</span><span class="sxs-lookup"><span data-stu-id="2f8cb-111">If the MoveTo row appears between two rows, the X cell represents the  *x*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
|[<span data-ttu-id="2f8cb-112">LineTo</span><span class="sxs-lookup"><span data-stu-id="2f8cb-112">LineTo</span></span>](lineto-row-geometry-section.md) <br/> | <span data-ttu-id="2f8cb-113">直線セグメントの最後の頂点に対する*x*座標です。</span><span class="sxs-lookup"><span data-stu-id="2f8cb-113">The  *x*  -coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |
|<span data-ttu-id="2f8cb-114">[[arcto]](arcto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="2f8cb-114">[ArcTo](arcto-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="2f8cb-115">円弧の最後の頂点に対する*x*座標です。</span><span class="sxs-lookup"><span data-stu-id="2f8cb-115">The  *x*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|<span data-ttu-id="2f8cb-116">[[ellipticalarcto]](ellipticalarcto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="2f8cb-116">[EllipticalArcTo](ellipticalarcto-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="2f8cb-117">楕円の弧の最後の頂点に対する*x*座標です。</span><span class="sxs-lookup"><span data-stu-id="2f8cb-117">The  *x*  -coordinate of the ending vertex of an elliptical arc.</span></span>  <br/> |
|<span data-ttu-id="2f8cb-118">[[polylineto]](polylineto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="2f8cb-118">[PolylineTo](polylineto-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="2f8cb-119">ポリラインの最後の頂点に対する*x*座標です。</span><span class="sxs-lookup"><span data-stu-id="2f8cb-119">The  *x*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|<span data-ttu-id="2f8cb-120">[[nurbsto]](nurbsto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="2f8cb-120">[NURBSTo](nurbsto-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="2f8cb-121">不均一な有理数 (NURBS) の最後のコントロールポイントに対する*x*座標です。</span><span class="sxs-lookup"><span data-stu-id="2f8cb-121">The  *x*  -coordinate of the last control point of a nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|<span data-ttu-id="2f8cb-122">[[splinestart]](splinestart-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="2f8cb-122">[SplineStart](splinestart-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="2f8cb-123">スプラインの2番目のコントロールポイントに対する*x*座標です。</span><span class="sxs-lookup"><span data-stu-id="2f8cb-123">The  *x*  -coordinate of a spline's second control point.</span></span>  <br/> |
|<span data-ttu-id="2f8cb-124">[[splineknot]](splineknot-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="2f8cb-124">[SplineKnot](splineknot-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="2f8cb-125">コントロールポイントの*x*座標です。</span><span class="sxs-lookup"><span data-stu-id="2f8cb-125">The  *x*  -coordinate of a control point.</span></span>  <br/> |
|<span data-ttu-id="2f8cb-126">[[infiniteline]](infiniteline-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="2f8cb-126">[InfiniteLine](infiniteline-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="2f8cb-127">無限線上の点の*x*座標です。</span><span class="sxs-lookup"><span data-stu-id="2f8cb-127">An  *x*  -coordinate of a point on the infinite line.</span></span>  <br/> |
|[<span data-ttu-id="2f8cb-128">もう</span><span class="sxs-lookup"><span data-stu-id="2f8cb-128">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="2f8cb-129">楕円の中心点の*x*座標です。</span><span class="sxs-lookup"><span data-stu-id="2f8cb-129">The  *x*  -coordinate of the center of the ellipse.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2f8cb-130">解説</span><span class="sxs-lookup"><span data-stu-id="2f8cb-130">Remarks</span></span>

<span data-ttu-id="2f8cb-131">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [X] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="2f8cb-131">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2f8cb-132">セル名:</span><span class="sxs-lookup"><span data-stu-id="2f8cb-132">Cell name:</span></span>  <br/> | <span data-ttu-id="2f8cb-133">ジオメトリ*i*X *j* where *i*および*j* = <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="2f8cb-133">Geometry  *i*  .X  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="2f8cb-134">ジオメトリ*i*X1 ([infiniteline] および楕円の行) *i* = <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="2f8cb-134">Geometry  *i*  .X1 (InfiniteLine and Ellipse rows)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="2f8cb-135">プログラムから、インデックスによって [X] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="2f8cb-135">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2f8cb-136">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="2f8cb-136">Section index:</span></span>  <br/> |<span data-ttu-id="2f8cb-137">**visSectionFirstComponent** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="2f8cb-137">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="2f8cb-138">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="2f8cb-138">Row index:</span></span>  <br/> |<span data-ttu-id="2f8cb-139">**visRowVertex** +  *j* where *j* = 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="2f8cb-139">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="2f8cb-140">**visRowVertex** ([InfiniteLine] 行および [Ellipse] 行)</span><span class="sxs-lookup"><span data-stu-id="2f8cb-140">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="2f8cb-141">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="2f8cb-141">Cell index:</span></span>  <br/> |<span data-ttu-id="2f8cb-142">**visX** ([MoveTo]、[LineTo]、[ArcTo]、[EllipticalArcTo]、[NURBSTo]、[Polyline]、[SplineStart]、および [SplineKnot] 行)</span><span class="sxs-lookup"><span data-stu-id="2f8cb-142">**visX** (MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart, and SplineKnot rows)</span></span>  <br/> |
||<span data-ttu-id="2f8cb-143">**visInfiniteLineX1** ([InfiniteLine] 行)</span><span class="sxs-lookup"><span data-stu-id="2f8cb-143">**visInfiniteLineX1** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="2f8cb-144">**visEllipseCenterX** ([Ellipse] 行)</span><span class="sxs-lookup"><span data-stu-id="2f8cb-144">**visEllipseCenterX** (Ellipse row)</span></span>  <br/> |
   

