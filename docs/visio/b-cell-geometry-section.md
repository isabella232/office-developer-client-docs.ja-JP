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
description: 各行に対応する情報を表示します。 次の表に、各行で [B] セルが示す内容を説明します。
ms.openlocfilehash: 46c8aa418f495905630fed2833d84afc93945346
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537795"
---
# <a name="b-cell-geometry-section"></a><span data-ttu-id="99786-104">[B] セル ([Geometry] セクション)</span><span class="sxs-lookup"><span data-stu-id="99786-104">B Cell (Geometry Section)</span></span>

<span data-ttu-id="99786-105">各行に対応する情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="99786-105">Represents different information in different rows.</span></span> <span data-ttu-id="99786-106">次の表に、各行で [B] セルが示す内容を説明します。</span><span class="sxs-lookup"><span data-stu-id="99786-106">This table describes the B cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="99786-107">Row</span><span class="sxs-lookup"><span data-stu-id="99786-107">Row</span></span>|<span data-ttu-id="99786-108">説明</span><span class="sxs-lookup"><span data-stu-id="99786-108">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="99786-109">[[Ellipticalarcto]](ellipticalarcto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="99786-109">[EllipticalArcTo](ellipticalarcto-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="99786-110">円弧のコントロールポイントの*y*座標です。</span><span class="sxs-lookup"><span data-stu-id="99786-110">The  *y*  -coordinate of an arc's control point.</span></span>  <br/> |
|<span data-ttu-id="99786-111">[[Nurbsto]](nurbsto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="99786-111">[NURBSTo](nurbsto-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="99786-112">NURBS (nonuniform rational B-spline) の最後の太さです。</span><span class="sxs-lookup"><span data-stu-id="99786-112">The last weight of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|<span data-ttu-id="99786-113">[[Splinestart]](splinestart-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="99786-113">[SplineStart](splinestart-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="99786-114">スプラインの最初のノットです。</span><span class="sxs-lookup"><span data-stu-id="99786-114">The first knot of a spline.</span></span>  <br/> |
|<span data-ttu-id="99786-115">[[Infiniteline]](infiniteline-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="99786-115">[InfiniteLine](infiniteline-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="99786-116">無限線上の点の*y*座標です。対応する*x*座標[は、A](a-cell-geometry-section.md)セルで表されます。</span><span class="sxs-lookup"><span data-stu-id="99786-116">A  *y*  -coordinate of a point on an infinite line; paired with  *x*  -coordinate represented by the [A](a-cell-geometry-section.md) cell.</span></span>  <br/> |
|[<span data-ttu-id="99786-117">もう</span><span class="sxs-lookup"><span data-stu-id="99786-117">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="99786-118">楕円上の点の*y*座標です。対応する*x*座標[は、A](a-cell-geometry-section.md)セルで表されます。</span><span class="sxs-lookup"><span data-stu-id="99786-118">A  *y*  -coordinate of a point on an ellipse; paired with  *x*  -coordinate represented by the [A](a-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="99786-119">注釈</span><span class="sxs-lookup"><span data-stu-id="99786-119">Remarks</span></span>

<span data-ttu-id="99786-120">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [B] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="99786-120">To get a reference to the B cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="99786-121">セル名:</span><span class="sxs-lookup"><span data-stu-id="99786-121">Cell name:</span></span>  <br/> | <span data-ttu-id="99786-122">ジオメトリ*i*B *j* where *i*および*j* = <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="99786-122">Geometry  *i*  .B  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="99786-123">ジオメトリ*i*B1 ([Infiniteline] および楕円の行)</span><span class="sxs-lookup"><span data-stu-id="99786-123">Geometry  *i*  .B1 (InfiniteLine and Ellipse rows)</span></span>  <br/> |
   
<span data-ttu-id="99786-124">プログラムから、インデックスによって [B] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="99786-124">To get a reference to the B cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="99786-125">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="99786-125">Section index:</span></span>  <br/> |<span data-ttu-id="99786-126">**visSectionFirstComponent** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="99786-126">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="99786-127">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="99786-127">Row index:</span></span>  <br/> |<span data-ttu-id="99786-128">**visRowVertex** +  *j* where *j* = 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="99786-128">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="99786-129">**visRowVertex** ([InfiniteLine] 行および [Ellipse] 行)</span><span class="sxs-lookup"><span data-stu-id="99786-129">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="99786-130">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="99786-130">Cell index:</span></span>  <br/> |<span data-ttu-id="99786-131">**visControlX** ([EllipticalArcTo] 行)</span><span class="sxs-lookup"><span data-stu-id="99786-131">**visControlX** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="99786-132">**visControlY** ([EllipticalArcTo] 行)</span><span class="sxs-lookup"><span data-stu-id="99786-132">**visControlY** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="99786-133">**visNURBSWeight** ([NURBSTo] 行)</span><span class="sxs-lookup"><span data-stu-id="99786-133">**visNURBSWeight** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="99786-134">**visSplineKnot2** ([SplineStart] 行)</span><span class="sxs-lookup"><span data-stu-id="99786-134">**visSplineKnot2** (SplineStart row)</span></span>  <br/> |
||<span data-ttu-id="99786-135">**visInfiniteLineY2** ([InfiniteLine] 行)</span><span class="sxs-lookup"><span data-stu-id="99786-135">**visInfiniteLineY2** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="99786-136">**visEllipseMajorY** ([Ellipse] 行)</span><span class="sxs-lookup"><span data-stu-id="99786-136">**visEllipseMajorY** (Ellipse row)</span></span>  <br/> |
   

