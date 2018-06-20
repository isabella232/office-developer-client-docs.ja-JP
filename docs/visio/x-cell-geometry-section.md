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
# <a name="x-cell-geometry-section"></a><span data-ttu-id="71d73-104">[X] セル ([Geometry] セクション)</span><span class="sxs-lookup"><span data-stu-id="71d73-104">X Cell (Geometry Section)</span></span>

<span data-ttu-id="71d73-105">*X*を表す-ローカル座標で図形の座標です。</span><span class="sxs-lookup"><span data-stu-id="71d73-105">Represents an  *x*  -coordinate on a shape in local coordinates.</span></span> <span data-ttu-id="71d73-106">この表に、各行で [X] セルの。</span><span class="sxs-lookup"><span data-stu-id="71d73-106">This table describes the X cell based on the row in which it's located.</span></span> 
  
|<span data-ttu-id="71d73-107">**Row**</span><span class="sxs-lookup"><span data-stu-id="71d73-107">**Row**</span></span>|<span data-ttu-id="71d73-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="71d73-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="71d73-109">[[Moveto]](moveto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="71d73-109">[MoveTo](moveto-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="71d73-110">[Moveto] 行がセクションの最初の行の場合は、[X] セルは*x*を表しますが、パスの最初の頂点の座標です。</span><span class="sxs-lookup"><span data-stu-id="71d73-110">If the MoveTo row is the first row in the section, the X cell represents the  *x*  -coordinate of the first vertex of a path.</span></span> <span data-ttu-id="71d73-111">[X] セルが*x*を表す 2 つの行の間、[moveto] 行が表示されている場合のパスを切断した後の最初の頂点の座標です。</span><span class="sxs-lookup"><span data-stu-id="71d73-111">If the MoveTo row appears between two rows, the X cell represents the  *x*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
|<span data-ttu-id="71d73-112">[[Lineto]](lineto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="71d73-112">[LineTo](lineto-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="71d73-113">*X*の直線の線分の終点の座標です。</span><span class="sxs-lookup"><span data-stu-id="71d73-113">The  *x*  -coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |
|[<span data-ttu-id="71d73-114">ArcTo</span><span class="sxs-lookup"><span data-stu-id="71d73-114">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> | <span data-ttu-id="71d73-115">*X*の円弧の終点の座標です。</span><span class="sxs-lookup"><span data-stu-id="71d73-115">The  *x*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="71d73-116">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="71d73-116">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="71d73-117">*X*の楕円の円弧の終点の座標です。</span><span class="sxs-lookup"><span data-stu-id="71d73-117">The  *x*  -coordinate of the ending vertex of an elliptical arc.</span></span>  <br/> |
|[<span data-ttu-id="71d73-118">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="71d73-118">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> | <span data-ttu-id="71d73-119">*X* -ポリラインの最後の頂点の座標です。</span><span class="sxs-lookup"><span data-stu-id="71d73-119">The  *x*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|<span data-ttu-id="71d73-120">[[Nurbsto]](nurbsto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="71d73-120">[NURBSTo](nurbsto-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="71d73-121">*X*が、不均一な合理性のある B スプライン (NURBS) の最後のコントロール ポイントの座標です。</span><span class="sxs-lookup"><span data-stu-id="71d73-121">The  *x*  -coordinate of the last control point of a nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|<span data-ttu-id="71d73-122">[[A](splinestart-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="71d73-122">[SplineStart](splinestart-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="71d73-123">*X* -スプラインの 2 番目の制御点の座標です。</span><span class="sxs-lookup"><span data-stu-id="71d73-123">The  *x*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="71d73-124">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="71d73-124">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> | <span data-ttu-id="71d73-125">*X* -コントロール ポイントの座標です。</span><span class="sxs-lookup"><span data-stu-id="71d73-125">The  *x*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="71d73-126">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="71d73-126">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="71d73-127">*X* -無限線上の点の座標です。</span><span class="sxs-lookup"><span data-stu-id="71d73-127">An  *x*  -coordinate of a point on the infinite line.</span></span>  <br/> |
|[<span data-ttu-id="71d73-128">楕円</span><span class="sxs-lookup"><span data-stu-id="71d73-128">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="71d73-129">*X*の楕円の中心の座標です。</span><span class="sxs-lookup"><span data-stu-id="71d73-129">The  *x*  -coordinate of the center of the ellipse.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="71d73-130">備考</span><span class="sxs-lookup"><span data-stu-id="71d73-130">Remarks</span></span>

<span data-ttu-id="71d73-131">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [X] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="71d73-131">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="71d73-132">セル名:</span><span class="sxs-lookup"><span data-stu-id="71d73-132">Cell name:</span></span>  <br/> | <span data-ttu-id="71d73-133">ジオメトリの*i*です。*J* x 位置*i*と*j* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="71d73-133">Geometry  *i*  .X  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="71d73-134">ジオメトリの*i*です。X1 (InfiniteLine と楕円の行)、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="71d73-134">Geometry  *i*  .X1 (InfiniteLine and Ellipse rows)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="71d73-135">プログラムから、インデックスによって [X] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="71d73-135">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="71d73-136">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="71d73-136">Section index:</span></span>  <br/> |<span data-ttu-id="71d73-137">**visSectionFirstComponent** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="71d73-137">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="71d73-138">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="71d73-138">Row index:</span></span>  <br/> |<span data-ttu-id="71d73-139">**visRowVertex** +  *j* 、 *j* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="71d73-139">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="71d73-140">**visRowVertex**(InfiniteLine と楕円の行)</span><span class="sxs-lookup"><span data-stu-id="71d73-140">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="71d73-141">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="71d73-141">Cell index:</span></span>  <br/> |<span data-ttu-id="71d73-142">**visX**([Moveto]、[lineto]、ArcTo、EllipticalArcTo、[nurbsto]、ポリライン、[a、および SplineKnot 行)</span><span class="sxs-lookup"><span data-stu-id="71d73-142">**visX** (MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart, and SplineKnot rows)</span></span>  <br/> |
||<span data-ttu-id="71d73-143">**visInfiniteLineX1**(InfiniteLine 行)</span><span class="sxs-lookup"><span data-stu-id="71d73-143">**visInfiniteLineX1** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="71d73-144">**visEllipseCenterX**([Ellipse] 行)</span><span class="sxs-lookup"><span data-stu-id="71d73-144">**visEllipseCenterX** (Ellipse row)</span></span>  <br/> |
   

