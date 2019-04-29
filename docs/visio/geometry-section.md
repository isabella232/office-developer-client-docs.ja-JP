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
ms.openlocfilehash: 32a815015c7d1764399215767b674668b7235832
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423910"
---
# <a name="geometry-section"></a><span data-ttu-id="794a0-103">[Geometry] セクション</span><span class="sxs-lookup"><span data-stu-id="794a0-103">Geometry Section</span></span>

<span data-ttu-id="794a0-104">図形を構成する直線と円弧の頂点の座標を一覧表示する行を格納します。</span><span class="sxs-lookup"><span data-stu-id="794a0-104">Contains rows that list the coordinates of the vertices for the lines and arcs that make up the shape.</span></span> 
  
<span data-ttu-id="794a0-105">図形のジオメトリは、複数の [ **geometry** ] セクションで表すことができます。</span><span class="sxs-lookup"><span data-stu-id="794a0-105">The geometry of a shape can be expressed in multiple **Geometry** sections.</span></span> <span data-ttu-id="794a0-106">複数のパスが異なるプロパティ ([画像のクリッピング](clippingpath-cell-foreign-image-info-section.md)パスなど) を持つ場合は、複数のパスが役に立つことがあります。</span><span class="sxs-lookup"><span data-stu-id="794a0-106">Multiple paths can be useful when multiple paths have different properties (e.g. [image clipping](clippingpath-cell-foreign-image-info-section.md) paths).</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="794a0-107">注釈</span><span class="sxs-lookup"><span data-stu-id="794a0-107">Remarks</span></span>

<span data-ttu-id="794a0-108">[ **Geometry** ] セクションには、次の行の種類が含まれます。</span><span class="sxs-lookup"><span data-stu-id="794a0-108">The **Geometry** section contains the following row types.</span></span> <span data-ttu-id="794a0-109">詳細については、各行のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="794a0-109">For details, see the row topics.</span></span> 
  
|<span data-ttu-id="794a0-110">**Row**</span><span class="sxs-lookup"><span data-stu-id="794a0-110">**Row**</span></span>|<span data-ttu-id="794a0-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="794a0-111">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="794a0-112">MoveTo</span><span class="sxs-lookup"><span data-stu-id="794a0-112">MoveTo</span></span>](moveto-row-geometry-section.md) <br/> |<span data-ttu-id="794a0-113">目的の座標に移動します。</span><span class="sxs-lookup"><span data-stu-id="794a0-113">Move to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="794a0-114">LineTo</span><span class="sxs-lookup"><span data-stu-id="794a0-114">LineTo</span></span>](lineto-row-geometry-section.md) <br/> |<span data-ttu-id="794a0-115">座標までの線を描画します。</span><span class="sxs-lookup"><span data-stu-id="794a0-115">Draw a line to a coordinate.</span></span>  <br/> |
|<span data-ttu-id="794a0-116">[[arcto]](arcto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="794a0-116">[ArcTo](arcto-row-geometry-section.md)</span></span> <br/> |<span data-ttu-id="794a0-117">座標までの真円の弧を描画します。</span><span class="sxs-lookup"><span data-stu-id="794a0-117">Draw a circular arc to a coordinate.</span></span>  <br/> |
|<span data-ttu-id="794a0-118">[[ellipticalarcto]](ellipticalarcto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="794a0-118">[EllipticalArcTo](ellipticalarcto-row-geometry-section.md)</span></span> <br/> |<span data-ttu-id="794a0-119">座標までの楕円の弧を描画します。</span><span class="sxs-lookup"><span data-stu-id="794a0-119">Draw an elliptical arc to a coordinate.</span></span>  <br/> |
|<span data-ttu-id="794a0-120">[[polylineto]](polylineto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="794a0-120">[PolylineTo](polylineto-row-geometry-section.md)</span></span> <br/> |<span data-ttu-id="794a0-121">座標までのポリラインまたは連続した線を描画します。</span><span class="sxs-lookup"><span data-stu-id="794a0-121">Draw a polyline, or consecutive lines, to a coordinate.</span></span>  <br/> |
|<span data-ttu-id="794a0-122">[[nurbsto]](nurbsto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="794a0-122">[NURBSTo](nurbsto-row-geometry-section.md)</span></span> <br/> |<span data-ttu-id="794a0-123">座標に一様でない有理数 (NURBS) を描画します。</span><span class="sxs-lookup"><span data-stu-id="794a0-123">Draw a non-uniform rational B-spline (NURBS) to a coordinate.</span></span>  <br/> |
|<span data-ttu-id="794a0-124">[[splinestart]](splinestart-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="794a0-124">[SplineStart](splinestart-row-geometry-section.md)</span></span> <br/> |<span data-ttu-id="794a0-125">スプラインを開始します。</span><span class="sxs-lookup"><span data-stu-id="794a0-125">Start a spline.</span></span>  <br/> |
|<span data-ttu-id="794a0-126">[[splineknot]](splineknot-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="794a0-126">[SplineKnot](splineknot-row-geometry-section.md)</span></span> <br/> |<span data-ttu-id="794a0-127">ノット座標までのスプライン セグメントを描画します。</span><span class="sxs-lookup"><span data-stu-id="794a0-127">Draw a spline segment to a knot coordinate.</span></span>  <br/> |
|<span data-ttu-id="794a0-128">[[infiniteline]](infiniteline-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="794a0-128">[InfiniteLine](infiniteline-row-geometry-section.md)</span></span> <br/> |<span data-ttu-id="794a0-129">1 つの座標から別の座標に無限線を描画します。</span><span class="sxs-lookup"><span data-stu-id="794a0-129">Draw an infinite line from one coordinate to another.</span></span>  <br/> |
|[<span data-ttu-id="794a0-130">もう</span><span class="sxs-lookup"><span data-stu-id="794a0-130">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> |<span data-ttu-id="794a0-131">中心座標および長軸/短軸から楕円を描画します。</span><span class="sxs-lookup"><span data-stu-id="794a0-131">Draw an ellipse from a center coordinate and a major/minor axis.</span></span>  <br/> |
|<span data-ttu-id="794a0-132">[[relcubbezto]](relcubbezto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="794a0-132">[RelCubBezTo](relcubbezto-row-geometry-section.md)</span></span> <br/> |<span data-ttu-id="794a0-133">図形の幅と高さを基準に3次ベジエ曲線を描画します。</span><span class="sxs-lookup"><span data-stu-id="794a0-133">Draw a cubic Bezier curve relative to the width and height of the shape.</span></span>  <br/> |
|<span data-ttu-id="794a0-134">[[relellipticalarcto]](relellipticalarcto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="794a0-134">[RelEllipticalArcTo](relellipticalarcto-row-geometry-section.md)</span></span> <br/> |<span data-ttu-id="794a0-135">図形の高さと幅を基準にして、座標に楕円の弧を描画します。</span><span class="sxs-lookup"><span data-stu-id="794a0-135">Draw an elliptical arc to a coordinate relative to the height and width of the shape.</span></span>  <br/> |
|<span data-ttu-id="794a0-136">[[rellineto]](rellineto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="794a0-136">[RelLineTo](rellineto-row-geometry-section.md)</span></span> <br/> |<span data-ttu-id="794a0-137">図形の高さと幅を基準にして、座標に直線を描画します。</span><span class="sxs-lookup"><span data-stu-id="794a0-137">Draw a line to a coordinate relative the height and width of a shape.</span></span>  <br/> |
|<span data-ttu-id="794a0-138">[[relmoveto]](relmoveto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="794a0-138">[RelMoveTo](relmoveto-row-geometry-section.md)</span></span> <br/> |<span data-ttu-id="794a0-139">図形の幅と高さを基準にして座標に移動します。</span><span class="sxs-lookup"><span data-stu-id="794a0-139">Move to a coordinate relative to the width and height of the shape.</span></span>  <br/> |
|<span data-ttu-id="794a0-140">[[relquadbezto]](relquadbezto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="794a0-140">[RelQuadBezTo](relquadbezto-row-geometry-section.md)</span></span> <br/> |<span data-ttu-id="794a0-141">図形の幅と高さを基準にして、2次ベジエ曲線を描画します。</span><span class="sxs-lookup"><span data-stu-id="794a0-141">Draws a quadratic Bezier curve relative to the width and height of the shape.</span></span>  <br/> |
   
<span data-ttu-id="794a0-142">このセクションにある行の種類を変更するには、行を右クリックして、ショートカット メニューの [**図形要素の変更**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="794a0-142">To change a row type in this section, right-click the row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  

