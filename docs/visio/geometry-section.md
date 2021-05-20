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
description: 図形を構成する直線と円弧の頂点の座標を一覧表示する行を格納します。
ms.openlocfilehash: d45f960ecc697dc6f0f5a0efa18e6cbbc6e4fff0
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542283"
---
# <a name="geometry-section"></a><span data-ttu-id="171e5-103">[Geometry] セクション</span><span class="sxs-lookup"><span data-stu-id="171e5-103">Geometry Section</span></span>

<span data-ttu-id="171e5-104">図形を構成する直線と円弧の頂点の座標を一覧表示する行を格納します。</span><span class="sxs-lookup"><span data-stu-id="171e5-104">Contains rows that list the coordinates of the vertices for the lines and arcs that make up the shape.</span></span> 
  
<span data-ttu-id="171e5-105">図形のジオメトリは、複数の Geometry セクション **で** 表現できます。</span><span class="sxs-lookup"><span data-stu-id="171e5-105">The geometry of a shape can be expressed in multiple **Geometry** sections.</span></span> <span data-ttu-id="171e5-106">複数のパスが異なるプロパティ (イメージ クリッピング パスなど) を持つ場合は、複数 [のパスを使用すると](clippingpath-cell-foreign-image-info-section.md) 便利です。</span><span class="sxs-lookup"><span data-stu-id="171e5-106">Multiple paths can be useful when multiple paths have different properties (e.g. [image clipping](clippingpath-cell-foreign-image-info-section.md) paths).</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="171e5-107">注釈</span><span class="sxs-lookup"><span data-stu-id="171e5-107">Remarks</span></span>

<span data-ttu-id="171e5-108">**[Geometry]** セクションには、次の行の種類が含まれます。</span><span class="sxs-lookup"><span data-stu-id="171e5-108">The **Geometry** section contains the following row types.</span></span> <span data-ttu-id="171e5-109">詳細については、各行のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="171e5-109">For details, see the row topics.</span></span> 
  
|<span data-ttu-id="171e5-110">行</span><span class="sxs-lookup"><span data-stu-id="171e5-110">Row</span></span>|<span data-ttu-id="171e5-111">説明</span><span class="sxs-lookup"><span data-stu-id="171e5-111">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="171e5-112">MoveTo</span><span class="sxs-lookup"><span data-stu-id="171e5-112">MoveTo</span></span>](moveto-row-geometry-section.md) <br/> |<span data-ttu-id="171e5-113">目的の座標に移動します。</span><span class="sxs-lookup"><span data-stu-id="171e5-113">Move to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="171e5-114">LineTo</span><span class="sxs-lookup"><span data-stu-id="171e5-114">LineTo</span></span>](lineto-row-geometry-section.md) <br/> |<span data-ttu-id="171e5-115">座標までの線を描画します。</span><span class="sxs-lookup"><span data-stu-id="171e5-115">Draw a line to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="171e5-116">ArcTo</span><span class="sxs-lookup"><span data-stu-id="171e5-116">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> |<span data-ttu-id="171e5-117">座標までの真円の弧を描画します。</span><span class="sxs-lookup"><span data-stu-id="171e5-117">Draw a circular arc to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="171e5-118">楕円ArcTo</span><span class="sxs-lookup"><span data-stu-id="171e5-118">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> |<span data-ttu-id="171e5-119">座標までの楕円の弧を描画します。</span><span class="sxs-lookup"><span data-stu-id="171e5-119">Draw an elliptical arc to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="171e5-120">ポリラインTo</span><span class="sxs-lookup"><span data-stu-id="171e5-120">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> |<span data-ttu-id="171e5-121">座標までのポリラインまたは連続した線を描画します。</span><span class="sxs-lookup"><span data-stu-id="171e5-121">Draw a polyline, or consecutive lines, to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="171e5-122">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="171e5-122">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> |<span data-ttu-id="171e5-123">非一様な合理的な B スプライン (NURBS) を座標に描画します。</span><span class="sxs-lookup"><span data-stu-id="171e5-123">Draw a non-uniform rational B-spline (NURBS) to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="171e5-124">SplineStart</span><span class="sxs-lookup"><span data-stu-id="171e5-124">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> |<span data-ttu-id="171e5-125">スプラインを開始します。</span><span class="sxs-lookup"><span data-stu-id="171e5-125">Start a spline.</span></span>  <br/> |
|[<span data-ttu-id="171e5-126">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="171e5-126">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> |<span data-ttu-id="171e5-127">ノット座標までのスプライン セグメントを描画します。</span><span class="sxs-lookup"><span data-stu-id="171e5-127">Draw a spline segment to a knot coordinate.</span></span>  <br/> |
|[<span data-ttu-id="171e5-128">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="171e5-128">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> |<span data-ttu-id="171e5-129">1 つの座標から別の座標に無限線を描画します。</span><span class="sxs-lookup"><span data-stu-id="171e5-129">Draw an infinite line from one coordinate to another.</span></span>  <br/> |
|[<span data-ttu-id="171e5-130">楕円</span><span class="sxs-lookup"><span data-stu-id="171e5-130">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> |<span data-ttu-id="171e5-131">中心座標および長軸/短軸から楕円を描画します。</span><span class="sxs-lookup"><span data-stu-id="171e5-131">Draw an ellipse from a center coordinate and a major/minor axis.</span></span>  <br/> |
|[<span data-ttu-id="171e5-132">RelCubBezTo</span><span class="sxs-lookup"><span data-stu-id="171e5-132">RelCubBezTo</span></span>](relcubbezto-row-geometry-section.md) <br/> |<span data-ttu-id="171e5-133">図形の幅と高さを基準に 3 次ベジエ曲線を描画します。</span><span class="sxs-lookup"><span data-stu-id="171e5-133">Draw a cubic Bezier curve relative to the width and height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="171e5-134">RelEllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="171e5-134">RelEllipticalArcTo</span></span>](relellipticalarcto-row-geometry-section.md) <br/> |<span data-ttu-id="171e5-135">図形の高さと幅を基準に楕円円弧を座標に描画します。</span><span class="sxs-lookup"><span data-stu-id="171e5-135">Draw an elliptical arc to a coordinate relative to the height and width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="171e5-136">RelLineTo</span><span class="sxs-lookup"><span data-stu-id="171e5-136">RelLineTo</span></span>](rellineto-row-geometry-section.md) <br/> |<span data-ttu-id="171e5-137">図形の高さと幅を基準に座標に線を描画します。</span><span class="sxs-lookup"><span data-stu-id="171e5-137">Draw a line to a coordinate relative the height and width of a shape.</span></span>  <br/> |
|[<span data-ttu-id="171e5-138">RelMoveTo</span><span class="sxs-lookup"><span data-stu-id="171e5-138">RelMoveTo</span></span>](relmoveto-row-geometry-section.md) <br/> |<span data-ttu-id="171e5-139">図形の幅と高さを基準に座標に移動します。</span><span class="sxs-lookup"><span data-stu-id="171e5-139">Move to a coordinate relative to the width and height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="171e5-140">RelQuadBezTo</span><span class="sxs-lookup"><span data-stu-id="171e5-140">RelQuadBezTo</span></span>](relquadbezto-row-geometry-section.md) <br/> |<span data-ttu-id="171e5-141">図形の幅と高さを基準に 2 次ベジエ曲線を描画します。</span><span class="sxs-lookup"><span data-stu-id="171e5-141">Draws a quadratic Bezier curve relative to the width and height of the shape.</span></span>  <br/> |
   
<span data-ttu-id="171e5-142">このセクションにある行の種類を変更するには、行を右クリックして、ショートカット メニューの [**図形要素の変更**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="171e5-142">To change a row type in this section, right-click the row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  

