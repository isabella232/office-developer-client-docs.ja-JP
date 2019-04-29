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
description: 各行に対応する情報を表示します。 次の表に、各行で [C] セルが示す内容を説明します。
ms.openlocfilehash: 5599c09ad3656653c486d7feff9aed2ee89e4614
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413368"
---
# <a name="c-cell-geometry-section"></a><span data-ttu-id="51e43-104">[C] セル ([Geometry] セクション)</span><span class="sxs-lookup"><span data-stu-id="51e43-104">C Cell (Geometry Section)</span></span>

<span data-ttu-id="51e43-105">各行に対応する情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="51e43-105">Represents different information in different rows.</span></span> <span data-ttu-id="51e43-106">次の表に、各行で [C] セルが示す内容を説明します。</span><span class="sxs-lookup"><span data-stu-id="51e43-106">This table describes the C cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="51e43-107">**Row**</span><span class="sxs-lookup"><span data-stu-id="51e43-107">**Row**</span></span>|<span data-ttu-id="51e43-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="51e43-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="51e43-109">[[ellipticalarcto]](ellipticalarcto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="51e43-109">[EllipticalArcTo](ellipticalarcto-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="51e43-110">親の*x*軸を基準にした円弧の主軸の角度。</span><span class="sxs-lookup"><span data-stu-id="51e43-110">The angle of an arc's major axis relative to the  *x*  -axis of its parent.</span></span>  <br/> |
|<span data-ttu-id="51e43-111">[[nurbsto]](nurbsto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="51e43-111">[NURBSTo](nurbsto-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="51e43-112">NURBS (nonuniform rational B-spline) の最初のノットです。</span><span class="sxs-lookup"><span data-stu-id="51e43-112">The first knot of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|<span data-ttu-id="51e43-113">[[splinestart]](splinestart-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="51e43-113">[SplineStart](splinestart-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="51e43-114">スプラインの最後のノットです。</span><span class="sxs-lookup"><span data-stu-id="51e43-114">The last knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="51e43-115">もう</span><span class="sxs-lookup"><span data-stu-id="51e43-115">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="51e43-116">楕円上の点の*x*座標です。対応する*y*座標は [ [D](d-cell-geometry-section.md)セルで表されます。</span><span class="sxs-lookup"><span data-stu-id="51e43-116">An  *x*  -coordinate of a point on an ellipse; paired with the  *y*  -coordinate represented by the [D](d-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="51e43-117">注釈</span><span class="sxs-lookup"><span data-stu-id="51e43-117">Remarks</span></span>

<span data-ttu-id="51e43-118">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [C] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="51e43-118">To get a reference to the C cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="51e43-119">セル名:</span><span class="sxs-lookup"><span data-stu-id="51e43-119">Cell name:</span></span>  <br/> | <span data-ttu-id="51e43-120">ジオメトリ*i*C *j* where *i*および*j* = <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="51e43-120">Geometry  *i*  .C  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="51e43-121">ジオメトリ*i*C1 (楕円行)</span><span class="sxs-lookup"><span data-stu-id="51e43-121">Geometry  *i*  .C1 (Ellipse row)</span></span>  <br/> |
   
<span data-ttu-id="51e43-122">プログラムから、インデックスによって [C] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="51e43-122">To get a reference to the C cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="51e43-123">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="51e43-123">Section index:</span></span>  <br/> |<span data-ttu-id="51e43-124">**visSectionFirstComponent** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="51e43-124">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="51e43-125">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="51e43-125">Row index:</span></span>  <br/> |<span data-ttu-id="51e43-126">**visRowVertex** +  *j* where *j* = 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="51e43-126">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="51e43-127">**visRowVertex** ([Ellipse] 行)</span><span class="sxs-lookup"><span data-stu-id="51e43-127">**visRowVertex** (Ellipse row)</span></span>  <br/> |
| <span data-ttu-id="51e43-128">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="51e43-128">Cell index:</span></span>  <br/> |<span data-ttu-id="51e43-129">**visEccentricityAngle** ([EllipticalArcTo] 行)</span><span class="sxs-lookup"><span data-stu-id="51e43-129">**visEccentricityAngle** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="51e43-130">**visNURBSKnotPrev** ([NURBSTo] 行)</span><span class="sxs-lookup"><span data-stu-id="51e43-130">**visNURBSKnotPrev** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="51e43-131">**visSplineKnot3** ([SplineStart] 行)</span><span class="sxs-lookup"><span data-stu-id="51e43-131">**visSplineKnot3** (SplineStart row)</span></span>  <br/> |
||<span data-ttu-id="51e43-132">**visEllipseMinorX** ([Ellipse] 行)</span><span class="sxs-lookup"><span data-stu-id="51e43-132">**visEllipseMinorX** (Ellipse row)</span></span>  <br/> |
   

