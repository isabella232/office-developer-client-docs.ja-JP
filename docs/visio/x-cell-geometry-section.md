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
description: ローカル座標の図形の x 座標を表します。 次の表に、各行で [X] セルが示す内容を説明します。
ms.openlocfilehash: 2b3303533db446780ef797844ac5e1438cec242f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538215"
---
# <a name="x-cell-geometry-section"></a><span data-ttu-id="a9372-104">[X] セル ([Geometry] セクション)</span><span class="sxs-lookup"><span data-stu-id="a9372-104">X Cell (Geometry Section)</span></span>

<span data-ttu-id="a9372-105">ローカル座標の  *図形*  の x 座標を表します。</span><span class="sxs-lookup"><span data-stu-id="a9372-105">Represents an  *x*  -coordinate on a shape in local coordinates.</span></span> <span data-ttu-id="a9372-106">次の表に、各行で [X] セルが示す内容を説明します。</span><span class="sxs-lookup"><span data-stu-id="a9372-106">This table describes the X cell based on the row in which it's located.</span></span> 
  
|<span data-ttu-id="a9372-107">行</span><span class="sxs-lookup"><span data-stu-id="a9372-107">Row</span></span>|<span data-ttu-id="a9372-108">説明</span><span class="sxs-lookup"><span data-stu-id="a9372-108">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a9372-109">MoveTo</span><span class="sxs-lookup"><span data-stu-id="a9372-109">MoveTo</span></span>](moveto-row-geometry-section.md) <br/> | <span data-ttu-id="a9372-110">MoveTo 行がセクションの最初の行である場合、X セルはパスの最初の頂点の  *x*  座標を表します。</span><span class="sxs-lookup"><span data-stu-id="a9372-110">If the MoveTo row is the first row in the section, the X cell represents the  *x*  -coordinate of the first vertex of a path.</span></span> <span data-ttu-id="a9372-111">MoveTo 行が 2 行の間に表示される場合、X セルはパスのブレーク後の最初の頂点の  *x*  座標を表します。</span><span class="sxs-lookup"><span data-stu-id="a9372-111">If the MoveTo row appears between two rows, the X cell represents the  *x*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
|[<span data-ttu-id="a9372-112">LineTo</span><span class="sxs-lookup"><span data-stu-id="a9372-112">LineTo</span></span>](lineto-row-geometry-section.md) <br/> | <span data-ttu-id="a9372-113">直線  *セグメント*  の終了頂点の x 座標。</span><span class="sxs-lookup"><span data-stu-id="a9372-113">The  *x*  -coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |
|[<span data-ttu-id="a9372-114">ArcTo</span><span class="sxs-lookup"><span data-stu-id="a9372-114">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> | <span data-ttu-id="a9372-115">円弧  *の*  終了頂点の x 座標。</span><span class="sxs-lookup"><span data-stu-id="a9372-115">The  *x*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="a9372-116">楕円ArcTo</span><span class="sxs-lookup"><span data-stu-id="a9372-116">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="a9372-117">楕  *円円弧*  の終了頂点の x 座標。</span><span class="sxs-lookup"><span data-stu-id="a9372-117">The  *x*  -coordinate of the ending vertex of an elliptical arc.</span></span>  <br/> |
|[<span data-ttu-id="a9372-118">ポリラインTo</span><span class="sxs-lookup"><span data-stu-id="a9372-118">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> | <span data-ttu-id="a9372-119">ポリライン  *の*  終了頂点の x 座標。</span><span class="sxs-lookup"><span data-stu-id="a9372-119">The  *x*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|[<span data-ttu-id="a9372-120">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="a9372-120">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="a9372-121">非  *ユニフォーム*  有理 B スプライン (NURBS) の最後のコントロール ポイントの x 座標。</span><span class="sxs-lookup"><span data-stu-id="a9372-121">The  *x*  -coordinate of the last control point of a nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="a9372-122">SplineStart</span><span class="sxs-lookup"><span data-stu-id="a9372-122">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="a9372-123">スプライン  *の*  2 番目のコントロール ポイントの x 座標。</span><span class="sxs-lookup"><span data-stu-id="a9372-123">The  *x*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="a9372-124">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="a9372-124">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> | <span data-ttu-id="a9372-125">コントロール  *ポイントの x*  座標。</span><span class="sxs-lookup"><span data-stu-id="a9372-125">The  *x*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="a9372-126">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="a9372-126">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="a9372-127">無限  *線*  上の点の x 座標。</span><span class="sxs-lookup"><span data-stu-id="a9372-127">An  *x*  -coordinate of a point on the infinite line.</span></span>  <br/> |
|[<span data-ttu-id="a9372-128">楕円</span><span class="sxs-lookup"><span data-stu-id="a9372-128">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="a9372-129">楕  *円*  の中心の x 座標。</span><span class="sxs-lookup"><span data-stu-id="a9372-129">The  *x*  -coordinate of the center of the ellipse.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a9372-130">注釈</span><span class="sxs-lookup"><span data-stu-id="a9372-130">Remarks</span></span>

<span data-ttu-id="a9372-131">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [X] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="a9372-131">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a9372-132">セル名:</span><span class="sxs-lookup"><span data-stu-id="a9372-132">Cell name:</span></span>  <br/> | <span data-ttu-id="a9372-133">Geometry  *i*  .x  *j*            *i と*  j =  *<*  1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="a9372-133">Geometry  *i*  .X  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="a9372-134">Geometry  *i*  .X1 (InfiniteLine 行と楕円行) i  *=*  <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="a9372-134">Geometry  *i*  .X1 (InfiniteLine and Ellipse rows)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="a9372-135">プログラムから、インデックスによって [X] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="a9372-135">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a9372-136">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="a9372-136">Section index:</span></span>  <br/> |<span data-ttu-id="a9372-137">**visSectionFirstComponent**  +  *i* *=* 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="a9372-137">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="a9372-138">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="a9372-138">Row index:</span></span>  <br/> |<span data-ttu-id="a9372-139">**visRowVertex**  +  *j* は *j* = 0、1、2..です。</span><span class="sxs-lookup"><span data-stu-id="a9372-139">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="a9372-140">**visRowVertex** ([InfiniteLine] 行および [Ellipse] 行)</span><span class="sxs-lookup"><span data-stu-id="a9372-140">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="a9372-141">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="a9372-141">Cell index:</span></span>  <br/> |<span data-ttu-id="a9372-142">**visX** ([MoveTo]、[LineTo]、[ArcTo]、[EllipticalArcTo]、[NURBSTo]、[Polyline]、[SplineStart]、および [SplineKnot] 行)</span><span class="sxs-lookup"><span data-stu-id="a9372-142">**visX** (MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart, and SplineKnot rows)</span></span>  <br/> |
||<span data-ttu-id="a9372-143">**visInfiniteLineX1** ([InfiniteLine] 行)</span><span class="sxs-lookup"><span data-stu-id="a9372-143">**visInfiniteLineX1** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="a9372-144">**visEllipseCenterX** ([Ellipse] 行)</span><span class="sxs-lookup"><span data-stu-id="a9372-144">**visEllipseCenterX** (Ellipse row)</span></span>  <br/> |
   

