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
description: X を表す-ローカル座標で図形の座標です。 この表に、各行で [X] セルの。
ms.openlocfilehash: e5bc99d4f73d49741c4378009dfc2a883bb655ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806806"
---
# <a name="x-cell-geometry-section"></a><span data-ttu-id="b0c18-104">[X] セル ([図形座標] セクション)</span><span class="sxs-lookup"><span data-stu-id="b0c18-104">X Cell (Geometry Section)</span></span>

<span data-ttu-id="b0c18-105">*X*を表す-ローカル座標で図形の座標です。</span><span class="sxs-lookup"><span data-stu-id="b0c18-105">Represents an  *x*  -coordinate on a shape in local coordinates.</span></span> <span data-ttu-id="b0c18-106">この表に、各行で [X] セルの。</span><span class="sxs-lookup"><span data-stu-id="b0c18-106">This table describes the X cell based on the row in which it's located.</span></span> 
  
|<span data-ttu-id="b0c18-107">**Row**</span><span class="sxs-lookup"><span data-stu-id="b0c18-107">**Row**</span></span>|<span data-ttu-id="b0c18-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="b0c18-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b0c18-109">MoveTo</span><span class="sxs-lookup"><span data-stu-id="b0c18-109">MoveTo</span></span>](moveto-row-geometry-section.md) <br/> | <span data-ttu-id="b0c18-110">[Moveto] 行がセクションの最初の行の場合は、[X] セルは*x*を表しますが、パスの最初の頂点の座標です。</span><span class="sxs-lookup"><span data-stu-id="b0c18-110">If the MoveTo row is the first row in the section, the X cell represents the  *x*  -coordinate of the first vertex of a path.</span></span> <span data-ttu-id="b0c18-111">[X] セルが*x*を表す 2 つの行の間、[moveto] 行が表示されている場合のパスを切断した後の最初の頂点の座標です。</span><span class="sxs-lookup"><span data-stu-id="b0c18-111">If the MoveTo row appears between two rows, the X cell represents the  *x*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
|<span data-ttu-id="b0c18-112">[[Lineto]](lineto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="b0c18-112">[LineTo](lineto-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="b0c18-113">*X*の直線の線分の終点の座標です。</span><span class="sxs-lookup"><span data-stu-id="b0c18-113">The  *x*  -coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |
|[<span data-ttu-id="b0c18-114">ArcTo</span><span class="sxs-lookup"><span data-stu-id="b0c18-114">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> | <span data-ttu-id="b0c18-115">*X*の円弧の終点の座標です。</span><span class="sxs-lookup"><span data-stu-id="b0c18-115">The  *x*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="b0c18-116">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="b0c18-116">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="b0c18-117">*X*の楕円の円弧の終点の座標です。</span><span class="sxs-lookup"><span data-stu-id="b0c18-117">The  *x*  -coordinate of the ending vertex of an elliptical arc.</span></span>  <br/> |
|[<span data-ttu-id="b0c18-118">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="b0c18-118">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> | <span data-ttu-id="b0c18-119">*X* -ポリラインの最後の頂点の座標です。</span><span class="sxs-lookup"><span data-stu-id="b0c18-119">The  *x*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|<span data-ttu-id="b0c18-120">[[Nurbsto]](nurbsto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="b0c18-120">[NURBSTo](nurbsto-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="b0c18-121">*X*が、不均一な合理性のある B スプライン (NURBS) の最後のコントロール ポイントの座標です。</span><span class="sxs-lookup"><span data-stu-id="b0c18-121">The  *x*  -coordinate of the last control point of a nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|<span data-ttu-id="b0c18-122">[[A](splinestart-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="b0c18-122">[SplineStart](splinestart-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="b0c18-123">*X* -スプラインの 2 番目の制御点の座標です。</span><span class="sxs-lookup"><span data-stu-id="b0c18-123">The  *x*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="b0c18-124">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="b0c18-124">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> | <span data-ttu-id="b0c18-125">*X* -コントロール ポイントの座標です。</span><span class="sxs-lookup"><span data-stu-id="b0c18-125">The  *x*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="b0c18-126">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="b0c18-126">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="b0c18-127">*X* -無限線上の点の座標です。</span><span class="sxs-lookup"><span data-stu-id="b0c18-127">An  *x*  -coordinate of a point on the infinite line.</span></span>  <br/> |
|[<span data-ttu-id="b0c18-128">楕円</span><span class="sxs-lookup"><span data-stu-id="b0c18-128">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="b0c18-129">*X*の楕円の中心の座標です。</span><span class="sxs-lookup"><span data-stu-id="b0c18-129">The  *x*  -coordinate of the center of the ellipse.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b0c18-130">注釈</span><span class="sxs-lookup"><span data-stu-id="b0c18-130">Remarks</span></span>

<span data-ttu-id="b0c18-131">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [X] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="b0c18-131">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b0c18-132">セル名:</span><span class="sxs-lookup"><span data-stu-id="b0c18-132">Cell name:</span></span>  <br/> | <span data-ttu-id="b0c18-133">ジオメトリの*i*です。*J* x 位置*i*と*j* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="b0c18-133">Geometry  *i*  .X  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="b0c18-134">ジオメトリの*i*です。X1 (InfiniteLine と楕円の行)、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="b0c18-134">Geometry  *i*  .X1 (InfiniteLine and Ellipse rows)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="b0c18-135">プログラムから、インデックスによって [X] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="b0c18-135">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b0c18-136">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="b0c18-136">Section index:</span></span>  <br/> |<span data-ttu-id="b0c18-137">**visSectionFirstComponent** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="b0c18-137">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="b0c18-138">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="b0c18-138">Row index:</span></span>  <br/> |<span data-ttu-id="b0c18-139">**visRowVertex** +  *j* 、 *j* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="b0c18-139">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="b0c18-140">**visRowVertex** ([InfiniteLine] 行および [Ellipse] 行)</span><span class="sxs-lookup"><span data-stu-id="b0c18-140">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="b0c18-141">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="b0c18-141">Cell index:</span></span>  <br/> |<span data-ttu-id="b0c18-142">**visX** ([MoveTo]、[LineTo]、[ArcTo]、[EllipticalArcTo]、[NURBSTo]、[Polyline]、[SplineStart]、および [SplineKnot] 行)</span><span class="sxs-lookup"><span data-stu-id="b0c18-142">**visX** (MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart, and SplineKnot rows)</span></span>  <br/> |
||<span data-ttu-id="b0c18-143">**visInfiniteLineX1** ([InfiniteLine] 行)</span><span class="sxs-lookup"><span data-stu-id="b0c18-143">**visInfiniteLineX1** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="b0c18-144">**visEllipseCenterX** ([Ellipse] 行)</span><span class="sxs-lookup"><span data-stu-id="b0c18-144">**visEllipseCenterX** (Ellipse row)</span></span>  <br/> |
   

