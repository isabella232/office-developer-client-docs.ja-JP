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
# <a name="geometry-section"></a><span data-ttu-id="271f1-103">[Geometry] セクション</span><span class="sxs-lookup"><span data-stu-id="271f1-103">Geometry Section</span></span>

<span data-ttu-id="271f1-104">図形を構成する直線と円弧の頂点の座標を一覧表示する行を格納します。</span><span class="sxs-lookup"><span data-stu-id="271f1-104">Contains rows that list the coordinates of the vertices for the lines and arcs that make up the shape.</span></span> 
  
<span data-ttu-id="271f1-105">図形のジオメトリは、複数の [ **geometry** ] セクションで表すことができます。</span><span class="sxs-lookup"><span data-stu-id="271f1-105">The geometry of a shape can be expressed in multiple **Geometry** sections.</span></span> <span data-ttu-id="271f1-106">複数のパスが異なるプロパティ ([画像のクリッピング](clippingpath-cell-foreign-image-info-section.md)パスなど) を持つ場合は、複数のパスが役に立つことがあります。</span><span class="sxs-lookup"><span data-stu-id="271f1-106">Multiple paths can be useful when multiple paths have different properties (e.g. [image clipping](clippingpath-cell-foreign-image-info-section.md) paths).</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="271f1-107">注釈</span><span class="sxs-lookup"><span data-stu-id="271f1-107">Remarks</span></span>

<span data-ttu-id="271f1-108">[ **Geometry** ] セクションには、次の行の種類が含まれます。</span><span class="sxs-lookup"><span data-stu-id="271f1-108">The **Geometry** section contains the following row types.</span></span> <span data-ttu-id="271f1-109">詳細については、各行のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="271f1-109">For details, see the row topics.</span></span> 
  
|<span data-ttu-id="271f1-110">Row</span><span class="sxs-lookup"><span data-stu-id="271f1-110">Row</span></span>|<span data-ttu-id="271f1-111">説明</span><span class="sxs-lookup"><span data-stu-id="271f1-111">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="271f1-112">MoveTo</span><span class="sxs-lookup"><span data-stu-id="271f1-112">MoveTo</span></span>](moveto-row-geometry-section.md) <br/> |<span data-ttu-id="271f1-113">目的の座標に移動します。</span><span class="sxs-lookup"><span data-stu-id="271f1-113">Move to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="271f1-114">LineTo</span><span class="sxs-lookup"><span data-stu-id="271f1-114">LineTo</span></span>](lineto-row-geometry-section.md) <br/> |<span data-ttu-id="271f1-115">座標までの線を描画します。</span><span class="sxs-lookup"><span data-stu-id="271f1-115">Draw a line to a coordinate.</span></span>  <br/> |
|<span data-ttu-id="271f1-116">[[Arcto]](arcto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="271f1-116">[ArcTo](arcto-row-geometry-section.md)</span></span> <br/> |<span data-ttu-id="271f1-117">座標までの真円の弧を描画します。</span><span class="sxs-lookup"><span data-stu-id="271f1-117">Draw a circular arc to a coordinate.</span></span>  <br/> |
|<span data-ttu-id="271f1-118">[[Ellipticalarcto]](ellipticalarcto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="271f1-118">[EllipticalArcTo](ellipticalarcto-row-geometry-section.md)</span></span> <br/> |<span data-ttu-id="271f1-119">座標までの楕円の弧を描画します。</span><span class="sxs-lookup"><span data-stu-id="271f1-119">Draw an elliptical arc to a coordinate.</span></span>  <br/> |
|<span data-ttu-id="271f1-120">[[Polylineto]](polylineto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="271f1-120">[PolylineTo](polylineto-row-geometry-section.md)</span></span> <br/> |<span data-ttu-id="271f1-121">座標までのポリラインまたは連続した線を描画します。</span><span class="sxs-lookup"><span data-stu-id="271f1-121">Draw a polyline, or consecutive lines, to a coordinate.</span></span>  <br/> |
|<span data-ttu-id="271f1-122">[[Nurbsto]](nurbsto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="271f1-122">[NURBSTo](nurbsto-row-geometry-section.md)</span></span> <br/> |<span data-ttu-id="271f1-123">座標に一様でない有理数 (NURBS) を描画します。</span><span class="sxs-lookup"><span data-stu-id="271f1-123">Draw a non-uniform rational B-spline (NURBS) to a coordinate.</span></span>  <br/> |
|<span data-ttu-id="271f1-124">[[Splinestart]](splinestart-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="271f1-124">[SplineStart](splinestart-row-geometry-section.md)</span></span> <br/> |<span data-ttu-id="271f1-125">スプラインを開始します。</span><span class="sxs-lookup"><span data-stu-id="271f1-125">Start a spline.</span></span>  <br/> |
|<span data-ttu-id="271f1-126">[[Splineknot]](splineknot-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="271f1-126">[SplineKnot](splineknot-row-geometry-section.md)</span></span> <br/> |<span data-ttu-id="271f1-127">ノット座標までのスプライン セグメントを描画します。</span><span class="sxs-lookup"><span data-stu-id="271f1-127">Draw a spline segment to a knot coordinate.</span></span>  <br/> |
|<span data-ttu-id="271f1-128">[[Infiniteline]](infiniteline-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="271f1-128">[InfiniteLine](infiniteline-row-geometry-section.md)</span></span> <br/> |<span data-ttu-id="271f1-129">1 つの座標から別の座標に無限線を描画します。</span><span class="sxs-lookup"><span data-stu-id="271f1-129">Draw an infinite line from one coordinate to another.</span></span>  <br/> |
|[<span data-ttu-id="271f1-130">もう</span><span class="sxs-lookup"><span data-stu-id="271f1-130">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> |<span data-ttu-id="271f1-131">中心座標および長軸/短軸から楕円を描画します。</span><span class="sxs-lookup"><span data-stu-id="271f1-131">Draw an ellipse from a center coordinate and a major/minor axis.</span></span>  <br/> |
|<span data-ttu-id="271f1-132">[[Relcubbezto]](relcubbezto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="271f1-132">[RelCubBezTo](relcubbezto-row-geometry-section.md)</span></span> <br/> |<span data-ttu-id="271f1-133">図形の幅と高さを基準に3次ベジエ曲線を描画します。</span><span class="sxs-lookup"><span data-stu-id="271f1-133">Draw a cubic Bezier curve relative to the width and height of the shape.</span></span>  <br/> |
|<span data-ttu-id="271f1-134">[[Relellipticalarcto]](relellipticalarcto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="271f1-134">[RelEllipticalArcTo](relellipticalarcto-row-geometry-section.md)</span></span> <br/> |<span data-ttu-id="271f1-135">図形の高さと幅を基準にして、座標に楕円の弧を描画します。</span><span class="sxs-lookup"><span data-stu-id="271f1-135">Draw an elliptical arc to a coordinate relative to the height and width of the shape.</span></span>  <br/> |
|<span data-ttu-id="271f1-136">[[Rellineto]](rellineto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="271f1-136">[RelLineTo](rellineto-row-geometry-section.md)</span></span> <br/> |<span data-ttu-id="271f1-137">図形の高さと幅を基準にして、座標に直線を描画します。</span><span class="sxs-lookup"><span data-stu-id="271f1-137">Draw a line to a coordinate relative the height and width of a shape.</span></span>  <br/> |
|<span data-ttu-id="271f1-138">[[Relmoveto]](relmoveto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="271f1-138">[RelMoveTo](relmoveto-row-geometry-section.md)</span></span> <br/> |<span data-ttu-id="271f1-139">図形の幅と高さを基準にして座標に移動します。</span><span class="sxs-lookup"><span data-stu-id="271f1-139">Move to a coordinate relative to the width and height of the shape.</span></span>  <br/> |
|<span data-ttu-id="271f1-140">[[Relquadbezto]](relquadbezto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="271f1-140">[RelQuadBezTo](relquadbezto-row-geometry-section.md)</span></span> <br/> |<span data-ttu-id="271f1-141">図形の幅と高さを基準にして、2次ベジエ曲線を描画します。</span><span class="sxs-lookup"><span data-stu-id="271f1-141">Draws a quadratic Bezier curve relative to the width and height of the shape.</span></span>  <br/> |
   
<span data-ttu-id="271f1-142">このセクションにある行の種類を変更するには、行を右クリックして、ショートカット メニューの [**図形要素の変更**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="271f1-142">To change a row type in this section, right-click the row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  

