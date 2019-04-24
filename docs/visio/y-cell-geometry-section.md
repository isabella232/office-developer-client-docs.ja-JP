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
description: ローカル座標での図形の y 座標を表します。 次の表に、各行で [Y] セルが示す内容を説明します。
ms.openlocfilehash: 9e823b8d21682b419a70ce498016abf575f36f6b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342813"
---
# <a name="y-cell-geometry-section"></a><span data-ttu-id="18210-104">[Y] セル ([Geometry] セクション)</span><span class="sxs-lookup"><span data-stu-id="18210-104">Y Cell (Geometry Section)</span></span>

<span data-ttu-id="18210-105">ローカル座標での図形の*y*座標を表します。</span><span class="sxs-lookup"><span data-stu-id="18210-105">Represents a  *y*  -coordinate on a shape in local coordinates.</span></span> <span data-ttu-id="18210-106">次の表に、各行で [Y] セルが示す内容を説明します。</span><span class="sxs-lookup"><span data-stu-id="18210-106">This table describes the Y cell based on the row in which it's located.</span></span> 
  
|<span data-ttu-id="18210-107">**行**</span><span class="sxs-lookup"><span data-stu-id="18210-107">**Row**</span></span>|<span data-ttu-id="18210-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="18210-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="18210-109">[[nurbsto]](nurbsto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="18210-109">[NURBSTo](nurbsto-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="18210-110">[MoveTo] 行がセクションの最初の行の場合、[y] セルは、パスの最初の頂点に対する*y*座標を表します。</span><span class="sxs-lookup"><span data-stu-id="18210-110">If the MoveTo row is the first row in the section, the Y cell represents the  *y*  -coordinate of the first vertex of a path.</span></span> <span data-ttu-id="18210-111">[MoveTo] 行が2つの行の間に表示される場合、[y] セルは、パスを切断した後の最初の頂点に対する*y*座標を表します。</span><span class="sxs-lookup"><span data-stu-id="18210-111">If the MoveTo row appears between two rows, the Y cell represents the  *y*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
|[<span data-ttu-id="18210-112">LineTo</span><span class="sxs-lookup"><span data-stu-id="18210-112">LineTo</span></span>](lineto-row-geometry-section.md) <br/> | <span data-ttu-id="18210-113">直線セグメントの最後の頂点に対する*y*座標です。</span><span class="sxs-lookup"><span data-stu-id="18210-113">The  *y*  -coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |
|<span data-ttu-id="18210-114">[[arcto]](arcto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="18210-114">[ArcTo](arcto-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="18210-115">円弧の最後の頂点に対する*y*座標です。</span><span class="sxs-lookup"><span data-stu-id="18210-115">The  *y*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|<span data-ttu-id="18210-116">[[ellipticalarcto]](ellipticalarcto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="18210-116">[EllipticalArcTo](ellipticalarcto-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="18210-117">楕円の弧の最後の頂点に対する*y*座標です。</span><span class="sxs-lookup"><span data-stu-id="18210-117">The  *y*  -coordinate of the ending vertex of an elliptical arc.</span></span>  <br/> |
|<span data-ttu-id="18210-118">[[polylineto]](polylineto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="18210-118">[PolylineTo](polylineto-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="18210-119">ポリラインの最後の頂点に対する*y*座標です。</span><span class="sxs-lookup"><span data-stu-id="18210-119">The  *y*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|<span data-ttu-id="18210-120">[[nurbsto]](nurbsto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="18210-120">[NURBSTo](nurbsto-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="18210-121">不均一な有理数 (NURBS) の最後のコントロールポイントに対する*y*座標です。</span><span class="sxs-lookup"><span data-stu-id="18210-121">The  *y*  -coordinate of the last control point of a nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|<span data-ttu-id="18210-122">[[splinestart]](splinestart-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="18210-122">[SplineStart](splinestart-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="18210-123">スプラインの2番目のコントロールポイントに対する*y*座標です。</span><span class="sxs-lookup"><span data-stu-id="18210-123">The  *y*  -coordinate of a spline's second control point.</span></span>  <br/> |
|<span data-ttu-id="18210-124">[[splineknot]](splineknot-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="18210-124">[SplineKnot](splineknot-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="18210-125">コントロールポイントの*y*座標です。</span><span class="sxs-lookup"><span data-stu-id="18210-125">The  *y*  -coordinate of a control point.</span></span>  <br/> |
|<span data-ttu-id="18210-126">[[infiniteline]](infiniteline-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="18210-126">[InfiniteLine](infiniteline-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="18210-127">無限線上の点の*y*座標です。</span><span class="sxs-lookup"><span data-stu-id="18210-127">A  *y-*  coordinate of a point on the infinite line.</span></span>  <br/> |
|[<span data-ttu-id="18210-128">もう</span><span class="sxs-lookup"><span data-stu-id="18210-128">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="18210-129">楕円の中心点の*y*座標です。</span><span class="sxs-lookup"><span data-stu-id="18210-129">The  *y*  -coordinate of the center of the ellipse.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18210-130">解説</span><span class="sxs-lookup"><span data-stu-id="18210-130">Remarks</span></span>

<span data-ttu-id="18210-131">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Y] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="18210-131">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="18210-132">セル名:</span><span class="sxs-lookup"><span data-stu-id="18210-132">Cell name:</span></span>  <br/> | <span data-ttu-id="18210-133">ジオメトリ*i*Y *j* where *i*および*j* = <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="18210-133">Geometry  *i*  .Y  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="18210-134">ジオメトリ*i*Y1 ([infiniteline] および楕円の行) *i* = <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="18210-134">Geometry  *i*  .Y1 (InfiniteLine and Ellipse rows)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="18210-135">プログラムから、インデックスによって [Y] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="18210-135">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="18210-136">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="18210-136">Section index:</span></span>  <br/> |<span data-ttu-id="18210-137">**visSectionFirstComponent** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="18210-137">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="18210-138">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="18210-138">Row index:</span></span>  <br/> |<span data-ttu-id="18210-139">**visRowVertex** +  *j* where *j* = 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="18210-139">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="18210-140">**visRowVertex** ([InfiniteLine] 行および [Ellipse] 行)</span><span class="sxs-lookup"><span data-stu-id="18210-140">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="18210-141">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="18210-141">Cell index:</span></span>  <br/> |<span data-ttu-id="18210-142">**visY** ([MoveTo]、[LineTo]、[ArcTo]、[EllipticalArcTo]、[NURBSTo]、[Polyline]、[SplineStart]、および [SplineKnot] 行)</span><span class="sxs-lookup"><span data-stu-id="18210-142">**visY** (MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart, and SplineKnot rows)</span></span>  <br/> |
||<span data-ttu-id="18210-143">**visInfiniteLineY1** ([InfiniteLine] 行)</span><span class="sxs-lookup"><span data-stu-id="18210-143">**visInfiniteLineY1** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="18210-144">**visEllipseCenterY** ([Ellipse] 行)</span><span class="sxs-lookup"><span data-stu-id="18210-144">**visEllipseCenterY** (Ellipse row)</span></span>  <br/> |
   

