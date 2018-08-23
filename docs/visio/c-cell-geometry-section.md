---
title: '[C] セル ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm140
localization_priority: Normal
ms.assetid: d51a1dd8-678a-a34d-658d-bd7a027dd379
description: 各行に対応する情報を表示します。次の表に、各行で [C] セルが示す内容を説明します。
ms.openlocfilehash: 1b9a813be825f2deeb5c90d596ffd9f3705bcef6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804946"
---
# <a name="c-cell-geometry-section"></a><span data-ttu-id="204b8-104">[C] セル ([図形座標] セクション)</span><span class="sxs-lookup"><span data-stu-id="204b8-104">C Cell (Geometry Section)</span></span>

<span data-ttu-id="204b8-p102">各行に対応する情報を表示します。次の表に、各行で [C] セルが示す内容を説明します。</span><span class="sxs-lookup"><span data-stu-id="204b8-p102">Represents different information in different rows. This table describes the C cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="204b8-107">**Row**</span><span class="sxs-lookup"><span data-stu-id="204b8-107">**Row**</span></span>|<span data-ttu-id="204b8-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="204b8-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="204b8-109">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="204b8-109">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="204b8-110">*X*を基準にして、円弧の長軸の角度を親の軸です。</span><span class="sxs-lookup"><span data-stu-id="204b8-110">The angle of an arc's major axis relative to the  *x*  -axis of its parent.</span></span>  <br/> |
|<span data-ttu-id="204b8-111">[[Nurbsto]](nurbsto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="204b8-111">[NURBSTo](nurbsto-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="204b8-112">NURBS (nonuniform rational B-spline) の最初のノットです。</span><span class="sxs-lookup"><span data-stu-id="204b8-112">The first knot of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|<span data-ttu-id="204b8-113">[[A](splinestart-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="204b8-113">[SplineStart](splinestart-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="204b8-114">スプラインの最後のノットです。</span><span class="sxs-lookup"><span data-stu-id="204b8-114">The last knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="204b8-115">楕円</span><span class="sxs-lookup"><span data-stu-id="204b8-115">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="204b8-116">*X* -楕円上の点の座標対応する*y*の座標は[[D](d-cell-geometry-section.md) ] セルで表されます。</span><span class="sxs-lookup"><span data-stu-id="204b8-116">An  *x*  -coordinate of a point on an ellipse; paired with the  *y*  -coordinate represented by the [D](d-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="204b8-117">注釈</span><span class="sxs-lookup"><span data-stu-id="204b8-117">Remarks</span></span>

<span data-ttu-id="204b8-118">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [C] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="204b8-118">To get a reference to the C cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="204b8-119">セル名:</span><span class="sxs-lookup"><span data-stu-id="204b8-119">Cell name:</span></span>  <br/> | <span data-ttu-id="204b8-120">ジオメトリの*i*です。C *j* 、 *i*および*j* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="204b8-120">Geometry  *i*  .C  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="204b8-121">ジオメトリの*i*です。C1 ([Ellipse] 行)</span><span class="sxs-lookup"><span data-stu-id="204b8-121">Geometry  *i*  .C1 (Ellipse row)</span></span>  <br/> |
   
<span data-ttu-id="204b8-122">プログラムから、インデックスによって [C] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="204b8-122">To get a reference to the C cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="204b8-123">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="204b8-123">Section index:</span></span>  <br/> |<span data-ttu-id="204b8-124">**visSectionFirstComponent** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="204b8-124">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="204b8-125">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="204b8-125">Row index:</span></span>  <br/> |<span data-ttu-id="204b8-126">**visRowVertex** +  *j* 、 *j* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="204b8-126">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="204b8-127">**visRowVertex** ([Ellipse] 行)</span><span class="sxs-lookup"><span data-stu-id="204b8-127">**visRowVertex** (Ellipse row)</span></span>  <br/> |
| <span data-ttu-id="204b8-128">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="204b8-128">Cell index:</span></span>  <br/> |<span data-ttu-id="204b8-129">**visEccentricityAngle** ([EllipticalArcTo] 行)</span><span class="sxs-lookup"><span data-stu-id="204b8-129">**visEccentricityAngle** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="204b8-130">**visNURBSKnotPrev** ([NURBSTo] 行)</span><span class="sxs-lookup"><span data-stu-id="204b8-130">**visNURBSKnotPrev** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="204b8-131">**visSplineKnot3** ([SplineStart] 行)</span><span class="sxs-lookup"><span data-stu-id="204b8-131">**visSplineKnot3** (SplineStart row)</span></span>  <br/> |
||<span data-ttu-id="204b8-132">**visEllipseMinorX** ([Ellipse] 行)</span><span class="sxs-lookup"><span data-stu-id="204b8-132">**visEllipseMinorX** (Ellipse row)</span></span>  <br/> |
   

