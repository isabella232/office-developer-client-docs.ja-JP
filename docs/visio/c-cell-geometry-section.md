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
ms.openlocfilehash: 0284fea02c7eb890b56b6c865a69eb36662d8ae6
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541891"
---
# <a name="c-cell-geometry-section"></a><span data-ttu-id="8fd33-104">[C] セル ([Geometry] セクション)</span><span class="sxs-lookup"><span data-stu-id="8fd33-104">C Cell (Geometry Section)</span></span>

<span data-ttu-id="8fd33-p102">各行に対応する情報を表示します。次の表に、各行で [C] セルが示す内容を説明します。</span><span class="sxs-lookup"><span data-stu-id="8fd33-p102">Represents different information in different rows. This table describes the C cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="8fd33-107">行</span><span class="sxs-lookup"><span data-stu-id="8fd33-107">Row</span></span>|<span data-ttu-id="8fd33-108">説明</span><span class="sxs-lookup"><span data-stu-id="8fd33-108">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8fd33-109">楕円ArcTo</span><span class="sxs-lookup"><span data-stu-id="8fd33-109">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="8fd33-110">親の x 軸に対する円弧の長軸の角度。</span><span class="sxs-lookup"><span data-stu-id="8fd33-110">The angle of an arc's major axis relative to the  *x*  -axis of its parent.</span></span>  <br/> |
|[<span data-ttu-id="8fd33-111">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="8fd33-111">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="8fd33-112">NURBS (nonuniform rational B-spline) の最初のノットです。</span><span class="sxs-lookup"><span data-stu-id="8fd33-112">The first knot of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="8fd33-113">SplineStart</span><span class="sxs-lookup"><span data-stu-id="8fd33-113">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="8fd33-114">スプラインの最後のノットです。</span><span class="sxs-lookup"><span data-stu-id="8fd33-114">The last knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="8fd33-115">楕円</span><span class="sxs-lookup"><span data-stu-id="8fd33-115">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="8fd33-116">楕  *円上*  の点の x 座標。D セルで  *表される y*  座標と組み [合](d-cell-geometry-section.md) わせ。</span><span class="sxs-lookup"><span data-stu-id="8fd33-116">An  *x*  -coordinate of a point on an ellipse; paired with the  *y*  -coordinate represented by the [D](d-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8fd33-117">注釈</span><span class="sxs-lookup"><span data-stu-id="8fd33-117">Remarks</span></span>

<span data-ttu-id="8fd33-118">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [C] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="8fd33-118">To get a reference to the C cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8fd33-119">セル名:</span><span class="sxs-lookup"><span data-stu-id="8fd33-119">Cell name:</span></span>  <br/> | <span data-ttu-id="8fd33-120">Geometry  *i*  .c  *j*            *i と*  j =  *<*  1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="8fd33-120">Geometry  *i*  .C  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="8fd33-121">Geometry  *i*  .C1 (楕円行)</span><span class="sxs-lookup"><span data-stu-id="8fd33-121">Geometry  *i*  .C1 (Ellipse row)</span></span>  <br/> |
   
<span data-ttu-id="8fd33-122">プログラムから、インデックスによって [C] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="8fd33-122">To get a reference to the C cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8fd33-123">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="8fd33-123">Section index:</span></span>  <br/> |<span data-ttu-id="8fd33-124">**visSectionFirstComponent**  +  *i* *=* 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="8fd33-124">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="8fd33-125">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="8fd33-125">Row index:</span></span>  <br/> |<span data-ttu-id="8fd33-126">**visRowVertex**  +  *j* は *j* = 0、1、2..です。</span><span class="sxs-lookup"><span data-stu-id="8fd33-126">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="8fd33-127">**visRowVertex** ([Ellipse] 行)</span><span class="sxs-lookup"><span data-stu-id="8fd33-127">**visRowVertex** (Ellipse row)</span></span>  <br/> |
| <span data-ttu-id="8fd33-128">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="8fd33-128">Cell index:</span></span>  <br/> |<span data-ttu-id="8fd33-129">**visEccentricityAngle** ([EllipticalArcTo] 行)</span><span class="sxs-lookup"><span data-stu-id="8fd33-129">**visEccentricityAngle** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="8fd33-130">**visNURBSKnotPrev** ([NURBSTo] 行)</span><span class="sxs-lookup"><span data-stu-id="8fd33-130">**visNURBSKnotPrev** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="8fd33-131">**visSplineKnot3** ([SplineStart] 行)</span><span class="sxs-lookup"><span data-stu-id="8fd33-131">**visSplineKnot3** (SplineStart row)</span></span>  <br/> |
||<span data-ttu-id="8fd33-132">**visEllipseMinorX** ([Ellipse] 行)</span><span class="sxs-lookup"><span data-stu-id="8fd33-132">**visEllipseMinorX** (Ellipse row)</span></span>  <br/> |
   

