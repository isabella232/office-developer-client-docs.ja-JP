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
description: Y を表す-ローカル座標で図形の座標です。 この表に、各行で [Y] セルの。
ms.openlocfilehash: 461fd0ec41d34132f469c811292550d2f7e094f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806841"
---
# <a name="y-cell-geometry-section"></a><span data-ttu-id="598d1-104">[Y] セル ([図形座標] セクション)</span><span class="sxs-lookup"><span data-stu-id="598d1-104">Y Cell (Geometry Section)</span></span>

<span data-ttu-id="598d1-105">の*y*を表す-ローカル座標で図形の座標です。</span><span class="sxs-lookup"><span data-stu-id="598d1-105">Represents a  *y*  -coordinate on a shape in local coordinates.</span></span> <span data-ttu-id="598d1-106">この表に、各行で [Y] セルの。</span><span class="sxs-lookup"><span data-stu-id="598d1-106">This table describes the Y cell based on the row in which it's located.</span></span> 
  
|<span data-ttu-id="598d1-107">**Row**</span><span class="sxs-lookup"><span data-stu-id="598d1-107">**Row**</span></span>|<span data-ttu-id="598d1-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="598d1-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="598d1-109">[[Nurbsto]](nurbsto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="598d1-109">[NURBSTo](nurbsto-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="598d1-110">[Moveto] 行がセクションの最初の行の場合は、[Y] セルは*y*を表しますが、パスの最初の頂点の座標。</span><span class="sxs-lookup"><span data-stu-id="598d1-110">If the MoveTo row is the first row in the section, the Y cell represents the  *y*  -coordinate of the first vertex of a path.</span></span> <span data-ttu-id="598d1-111">[Y] セルが*y*を表す 2 つの行の間、[moveto] 行が表示されている場合のパスを切断した後の最初の頂点の座標です。</span><span class="sxs-lookup"><span data-stu-id="598d1-111">If the MoveTo row appears between two rows, the Y cell represents the  *y*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
|<span data-ttu-id="598d1-112">[[Lineto]](lineto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="598d1-112">[LineTo](lineto-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="598d1-113">*Y*が直線の線分の終点の座標です。</span><span class="sxs-lookup"><span data-stu-id="598d1-113">The  *y*  -coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |
|[<span data-ttu-id="598d1-114">ArcTo</span><span class="sxs-lookup"><span data-stu-id="598d1-114">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> | <span data-ttu-id="598d1-115">*Y*の円弧の終点の座標です。</span><span class="sxs-lookup"><span data-stu-id="598d1-115">The  *y*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="598d1-116">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="598d1-116">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="598d1-117">*Y*の楕円の円弧の終点の座標です。</span><span class="sxs-lookup"><span data-stu-id="598d1-117">The  *y*  -coordinate of the ending vertex of an elliptical arc.</span></span>  <br/> |
|[<span data-ttu-id="598d1-118">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="598d1-118">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> | <span data-ttu-id="598d1-119">*Y* -ポリラインの最後の頂点の座標です。</span><span class="sxs-lookup"><span data-stu-id="598d1-119">The  *y*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|<span data-ttu-id="598d1-120">[[Nurbsto]](nurbsto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="598d1-120">[NURBSTo](nurbsto-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="598d1-121">*Y*が、不均一な合理性のある B スプライン (NURBS) の最後のコントロール ポイントの座標です。</span><span class="sxs-lookup"><span data-stu-id="598d1-121">The  *y*  -coordinate of the last control point of a nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|<span data-ttu-id="598d1-122">[[A](splinestart-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="598d1-122">[SplineStart](splinestart-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="598d1-123">*Y* -スプラインの 2 番目の制御点の座標です。</span><span class="sxs-lookup"><span data-stu-id="598d1-123">The  *y*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="598d1-124">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="598d1-124">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> | <span data-ttu-id="598d1-125">*Y*のコントロール ポイントの座標です。</span><span class="sxs-lookup"><span data-stu-id="598d1-125">The  *y*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="598d1-126">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="598d1-126">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="598d1-127">*Y -* 無限線上の点の座標です。</span><span class="sxs-lookup"><span data-stu-id="598d1-127">A  *y-*  coordinate of a point on the infinite line.</span></span>  <br/> |
|[<span data-ttu-id="598d1-128">楕円</span><span class="sxs-lookup"><span data-stu-id="598d1-128">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="598d1-129">*Y*の楕円の中心の座標です。</span><span class="sxs-lookup"><span data-stu-id="598d1-129">The  *y*  -coordinate of the center of the ellipse.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="598d1-130">注釈</span><span class="sxs-lookup"><span data-stu-id="598d1-130">Remarks</span></span>

<span data-ttu-id="598d1-131">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Y] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="598d1-131">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="598d1-132">セル名:</span><span class="sxs-lookup"><span data-stu-id="598d1-132">Cell name:</span></span>  <br/> | <span data-ttu-id="598d1-133">ジオメトリの*i*です。Y *j* 、 *i*および*j* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="598d1-133">Geometry  *i*  .Y  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="598d1-134">ジオメトリの*i*です。Y1 (InfiniteLine と楕円の行)、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="598d1-134">Geometry  *i*  .Y1 (InfiniteLine and Ellipse rows)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="598d1-135">プログラムから、インデックスによって [Y] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="598d1-135">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="598d1-136">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="598d1-136">Section index:</span></span>  <br/> |<span data-ttu-id="598d1-137">**visSectionFirstComponent** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="598d1-137">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="598d1-138">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="598d1-138">Row index:</span></span>  <br/> |<span data-ttu-id="598d1-139">**visRowVertex** +  *j* 、 *j* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="598d1-139">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="598d1-140">**visRowVertex** ([InfiniteLine] 行および [Ellipse] 行)</span><span class="sxs-lookup"><span data-stu-id="598d1-140">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="598d1-141">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="598d1-141">Cell index:</span></span>  <br/> |<span data-ttu-id="598d1-142">**visY** ([MoveTo]、[LineTo]、[ArcTo]、[EllipticalArcTo]、[NURBSTo]、[Polyline]、[SplineStart]、および [SplineKnot] 行)</span><span class="sxs-lookup"><span data-stu-id="598d1-142">**visY** (MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart, and SplineKnot rows)</span></span>  <br/> |
||<span data-ttu-id="598d1-143">**visInfiniteLineY1** ([InfiniteLine] 行)</span><span class="sxs-lookup"><span data-stu-id="598d1-143">**visInfiniteLineY1** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="598d1-144">**visEllipseCenterY** ([Ellipse] 行)</span><span class="sxs-lookup"><span data-stu-id="598d1-144">**visEllipseCenterY** (Ellipse row)</span></span>  <br/> |
   

