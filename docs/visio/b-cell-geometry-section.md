---
title: '[B] セル ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251751
localization_priority: Normal
ms.assetid: b0fb6a47-47d8-ab9c-854d-0b0bbfdfcc27
description: 各行に対応する情報を表示します。次の表に、各行で [B] セルが示す内容を説明します。
ms.openlocfilehash: 7d6f51d037be4852c6a101ad6e576a3a13488cb7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804798"
---
# <a name="b-cell-geometry-section"></a><span data-ttu-id="80cce-104">[B] セル ([Geometry] セクション)</span><span class="sxs-lookup"><span data-stu-id="80cce-104">B Cell (Geometry Section)</span></span>

<span data-ttu-id="80cce-p102">各行に対応する情報を表示します。次の表に、各行で [B] セルが示す内容を説明します。</span><span class="sxs-lookup"><span data-stu-id="80cce-p102">Represents different information in different rows. This table describes the B cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="80cce-107">**Row**</span><span class="sxs-lookup"><span data-stu-id="80cce-107">**Row**</span></span>|<span data-ttu-id="80cce-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="80cce-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="80cce-109">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="80cce-109">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="80cce-110">*Y*の円弧のコントロール ポイントの座標です。</span><span class="sxs-lookup"><span data-stu-id="80cce-110">The  *y*  -coordinate of an arc's control point.</span></span>  <br/> |
|<span data-ttu-id="80cce-111">[[Nurbsto]](nurbsto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="80cce-111">[NURBSTo](nurbsto-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="80cce-112">NURBS (nonuniform rational B-spline) の最後の太さです。</span><span class="sxs-lookup"><span data-stu-id="80cce-112">The last weight of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|<span data-ttu-id="80cce-113">[[A](splinestart-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="80cce-113">[SplineStart](splinestart-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="80cce-114">スプラインの最初のノットです。</span><span class="sxs-lookup"><span data-stu-id="80cce-114">The first knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="80cce-115">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="80cce-115">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="80cce-116">*Y* -無限線上の点の座標対応する*x*の座標は、[ [A](a-cell-geometry-section.md) ] セルで表されます。</span><span class="sxs-lookup"><span data-stu-id="80cce-116">A  *y*  -coordinate of a point on an infinite line; paired with  *x*  -coordinate represented by the [A](a-cell-geometry-section.md) cell.</span></span>  <br/> |
|[<span data-ttu-id="80cce-117">楕円</span><span class="sxs-lookup"><span data-stu-id="80cce-117">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="80cce-118">*Y* -楕円上の点の座標対応する*x*の座標は、[ [A](a-cell-geometry-section.md) ] セルで表されます。</span><span class="sxs-lookup"><span data-stu-id="80cce-118">A  *y*  -coordinate of a point on an ellipse; paired with  *x*  -coordinate represented by the [A](a-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="80cce-119">備考</span><span class="sxs-lookup"><span data-stu-id="80cce-119">Remarks</span></span>

<span data-ttu-id="80cce-120">別の数式または**CellsU**プロパティを使用して、プログラムから、名前によって、[B] セルへの参照を取得するには、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="80cce-120">To get a reference to the B cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="80cce-121">セル名:</span><span class="sxs-lookup"><span data-stu-id="80cce-121">Cell name:</span></span>  <br/> | <span data-ttu-id="80cce-122">ジオメトリの*i*です。B *j* 、 *i*および*j* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="80cce-122">Geometry  *i*  .B  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="80cce-123">ジオメトリの*i*です。B1 (InfiniteLine と楕円の行)</span><span class="sxs-lookup"><span data-stu-id="80cce-123">Geometry  *i*  .B1 (InfiniteLine and Ellipse rows)</span></span>  <br/> |
   
<span data-ttu-id="80cce-124">プログラムから、インデックスによって [B] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="80cce-124">To get a reference to the B cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="80cce-125">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="80cce-125">Section index:</span></span>  <br/> |<span data-ttu-id="80cce-126">**visSectionFirstComponent** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="80cce-126">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="80cce-127">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="80cce-127">Row index:</span></span>  <br/> |<span data-ttu-id="80cce-128">**visRowVertex** +  *j* 、 *j* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="80cce-128">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="80cce-129">**visRowVertex**(InfiniteLine と楕円の行)</span><span class="sxs-lookup"><span data-stu-id="80cce-129">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="80cce-130">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="80cce-130">Cell index:</span></span>  <br/> |<span data-ttu-id="80cce-131">**visControlX**(EllipticalArcTo 行)</span><span class="sxs-lookup"><span data-stu-id="80cce-131">**visControlX** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="80cce-132">**visControlY**(EllipticalArcTo 行)</span><span class="sxs-lookup"><span data-stu-id="80cce-132">**visControlY** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="80cce-133">**visNURBSWeight**([Nurbsto] 行)</span><span class="sxs-lookup"><span data-stu-id="80cce-133">**visNURBSWeight** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="80cce-134">**visSplineKnot2**([A 行)</span><span class="sxs-lookup"><span data-stu-id="80cce-134">**visSplineKnot2** (SplineStart row)</span></span>  <br/> |
||<span data-ttu-id="80cce-135">**visInfiniteLineY2**(InfiniteLine 行)</span><span class="sxs-lookup"><span data-stu-id="80cce-135">**visInfiniteLineY2** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="80cce-136">**visEllipseMajorY**([Ellipse] 行)</span><span class="sxs-lookup"><span data-stu-id="80cce-136">**visEllipseMajorY** (Ellipse row)</span></span>  <br/> |
   

