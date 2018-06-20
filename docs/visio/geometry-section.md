---
title: '[Geometry] セクション'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm2055
localization_priority: Normal
ms.assetid: 75601a1e-6b1a-27ee-a2bd-69e569315982
description: 直線と図形を構成する円弧の頂点の座標を一覧表示する行が含まれています。
ms.openlocfilehash: 59f85c512b7038f6cfddcb657435730a2e724bd6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805462"
---
# <a name="geometry-section"></a><span data-ttu-id="07c1b-103">[Geometry] セクション</span><span class="sxs-lookup"><span data-stu-id="07c1b-103">Geometry Section</span></span>

<span data-ttu-id="07c1b-104">直線と図形を構成する円弧の頂点の座標を一覧表示する行が含まれています。</span><span class="sxs-lookup"><span data-stu-id="07c1b-104">Contains rows that list the coordinates of the vertices for the lines and arcs that make up the shape.</span></span> 
  
<span data-ttu-id="07c1b-105">**ジオメトリ**の複数のセクションでは、図形の形状を表すことができます。</span><span class="sxs-lookup"><span data-stu-id="07c1b-105">The geometry of a shape can be expressed in multiple **Geometry** sections.</span></span> <span data-ttu-id="07c1b-106">複数のパスは、さまざまなプロパティ ([イメージのクリッピング](clippingpath-cell-foreign-image-info-section.md)・ パスなど) を複数のパスがあるときに役に立ちます。</span><span class="sxs-lookup"><span data-stu-id="07c1b-106">Multiple paths can be useful when multiple paths have different properties (e.g. [image clipping](clippingpath-cell-foreign-image-info-section.md) paths).</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="07c1b-107">備考</span><span class="sxs-lookup"><span data-stu-id="07c1b-107">Remarks</span></span>

<span data-ttu-id="07c1b-108">**[Geometry** ] セクションには、次の行の種類が含まれています。</span><span class="sxs-lookup"><span data-stu-id="07c1b-108">The **Geometry** section contains the following row types.</span></span> <span data-ttu-id="07c1b-109">詳細については、各行のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="07c1b-109">For details, see the row topics.</span></span> 
  
|<span data-ttu-id="07c1b-110">**Row**</span><span class="sxs-lookup"><span data-stu-id="07c1b-110">**Row**</span></span>|<span data-ttu-id="07c1b-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="07c1b-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="07c1b-112">[[Moveto]](moveto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="07c1b-112">[MoveTo](moveto-row-geometry-section.md)</span></span> <br/> |<span data-ttu-id="07c1b-113">目的の座標に移動します。</span><span class="sxs-lookup"><span data-stu-id="07c1b-113">Move to a coordinate.</span></span>  <br/> |
|<span data-ttu-id="07c1b-114">[[Lineto]](lineto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="07c1b-114">[LineTo](lineto-row-geometry-section.md)</span></span> <br/> |<span data-ttu-id="07c1b-115">座標までの線を描画します。</span><span class="sxs-lookup"><span data-stu-id="07c1b-115">Draw a line to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="07c1b-116">ArcTo</span><span class="sxs-lookup"><span data-stu-id="07c1b-116">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> |<span data-ttu-id="07c1b-117">座標までの真円の弧を描画します。</span><span class="sxs-lookup"><span data-stu-id="07c1b-117">Draw a circular arc to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="07c1b-118">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="07c1b-118">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> |<span data-ttu-id="07c1b-119">座標までの楕円の弧を描画します。</span><span class="sxs-lookup"><span data-stu-id="07c1b-119">Draw an elliptical arc to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="07c1b-120">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="07c1b-120">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> |<span data-ttu-id="07c1b-121">座標までのポリラインまたは連続した線を描画します。</span><span class="sxs-lookup"><span data-stu-id="07c1b-121">Draw a polyline, or consecutive lines, to a coordinate.</span></span>  <br/> |
|<span data-ttu-id="07c1b-122">[[Nurbsto]](nurbsto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="07c1b-122">[NURBSTo](nurbsto-row-geometry-section.md)</span></span> <br/> |<span data-ttu-id="07c1b-123">座標までの一様でない回転 B-スプライン (NURBS) を描画します。</span><span class="sxs-lookup"><span data-stu-id="07c1b-123">Draw a non-uniform rational B-spline (NURBS) to a coordinate.</span></span>  <br/> |
|<span data-ttu-id="07c1b-124">[[A](splinestart-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="07c1b-124">[SplineStart](splinestart-row-geometry-section.md)</span></span> <br/> |<span data-ttu-id="07c1b-125">スプラインを開始します。</span><span class="sxs-lookup"><span data-stu-id="07c1b-125">Start a spline.</span></span>  <br/> |
|[<span data-ttu-id="07c1b-126">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="07c1b-126">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> |<span data-ttu-id="07c1b-127">ノット座標までのスプライン セグメントを描画します。</span><span class="sxs-lookup"><span data-stu-id="07c1b-127">Draw a spline segment to a knot coordinate.</span></span>  <br/> |
|[<span data-ttu-id="07c1b-128">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="07c1b-128">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> |<span data-ttu-id="07c1b-129">1 つの座標から別の座標に無限線を描画します。</span><span class="sxs-lookup"><span data-stu-id="07c1b-129">Draw an infinite line from one coordinate to another.</span></span>  <br/> |
|[<span data-ttu-id="07c1b-130">楕円</span><span class="sxs-lookup"><span data-stu-id="07c1b-130">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> |<span data-ttu-id="07c1b-131">中心座標および長軸/短軸から楕円を描画します。</span><span class="sxs-lookup"><span data-stu-id="07c1b-131">Draw an ellipse from a center coordinate and a major/minor axis.</span></span>  <br/> |
|[<span data-ttu-id="07c1b-132">RelCubBezTo</span><span class="sxs-lookup"><span data-stu-id="07c1b-132">RelCubBezTo</span></span>](relcubbezto-row-geometry-section.md) <br/> |<span data-ttu-id="07c1b-133">図形の高さと幅を基準にして 3 次ベジエ曲線を描画します。</span><span class="sxs-lookup"><span data-stu-id="07c1b-133">Draw a cubic Bezier curve relative to the width and height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="07c1b-134">RelEllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="07c1b-134">RelEllipticalArcTo</span></span>](relellipticalarcto-row-geometry-section.md) <br/> |<span data-ttu-id="07c1b-135">図形の幅と高さを基準にして座標を楕円の円弧を描画します。</span><span class="sxs-lookup"><span data-stu-id="07c1b-135">Draw an elliptical arc to a coordinate relative to the height and width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="07c1b-136">RelLineTo</span><span class="sxs-lookup"><span data-stu-id="07c1b-136">RelLineTo</span></span>](rellineto-row-geometry-section.md) <br/> |<span data-ttu-id="07c1b-137">図形の幅と高さは、相対座標に線を引きます。</span><span class="sxs-lookup"><span data-stu-id="07c1b-137">Draw a line to a coordinate relative the height and width of a shape.</span></span>  <br/> |
|[<span data-ttu-id="07c1b-138">RelMoveTo</span><span class="sxs-lookup"><span data-stu-id="07c1b-138">RelMoveTo</span></span>](relmoveto-row-geometry-section.md) <br/> |<span data-ttu-id="07c1b-139">図形の高さと幅を基準にして座標に移動します。</span><span class="sxs-lookup"><span data-stu-id="07c1b-139">Move to a coordinate relative to the width and height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="07c1b-140">RelQuadBezTo</span><span class="sxs-lookup"><span data-stu-id="07c1b-140">RelQuadBezTo</span></span>](relquadbezto-row-geometry-section.md) <br/> |<span data-ttu-id="07c1b-141">図形の高さと幅の 2 次ベジエ曲線を描画します。</span><span class="sxs-lookup"><span data-stu-id="07c1b-141">Draws a quadratic Bezier curve relative to the width and height of the shape.</span></span>  <br/> |
   
<span data-ttu-id="07c1b-142">このセクション内の行タイプを変更するのには、行を右クリックし、し、ショートカット メニューの [**行の種類の変更**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="07c1b-142">To change a row type in this section, right-click the row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  

