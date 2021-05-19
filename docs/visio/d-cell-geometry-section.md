---
title: '[D] セル ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251753
localization_priority: Normal
ms.assetid: 5f1fdf59-db58-561c-e187-1af72a8b87f2
description: 各行に対応する情報を表示します。次の表に、各行で [D] セルが示す内容を説明します。
ms.openlocfilehash: a76093f028986907b58175bc6b8c81a7056cfe07
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542500"
---
# <a name="d-cell-geometry-section"></a><span data-ttu-id="ae9bd-104">[D] セル ([Geometry] セクション)</span><span class="sxs-lookup"><span data-stu-id="ae9bd-104">D Cell (Geometry Section)</span></span>

<span data-ttu-id="ae9bd-p102">各行に対応する情報を表示します。次の表に、各行で [D] セルが示す内容を説明します。</span><span class="sxs-lookup"><span data-stu-id="ae9bd-p102">Represents different information in different rows. This table describes the D cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="ae9bd-107">行</span><span class="sxs-lookup"><span data-stu-id="ae9bd-107">Row</span></span>|<span data-ttu-id="ae9bd-108">説明</span><span class="sxs-lookup"><span data-stu-id="ae9bd-108">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ae9bd-109">楕円ArcTo</span><span class="sxs-lookup"><span data-stu-id="ae9bd-109">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="ae9bd-p103">円弧の長軸と短軸の比率です。これらの言葉の通常の意味とは関係なく、"長" 軸が "短" 軸よりも長い必要はありません。したがって、比率は 1 より大きい必要はありません。このセルを 0 以下、または 1000 より大きく設定すると、予測できない結果になる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ae9bd-p103">The ratio of an arc's major axis to its minor axis. Despite the usual meaning of these words, the "major" axis does not have to be greater than the "minor" axis, so this ratio does not have to be greater than 1. Setting this cell to a value less than or equal to 0 or greater than 1000 can lead to unpredictable results.</span></span>  <br/> |
|[<span data-ttu-id="ae9bd-113">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="ae9bd-113">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="ae9bd-114">NURBS (nonuniform rational B-spline) の最初の太さです。</span><span class="sxs-lookup"><span data-stu-id="ae9bd-114">The first weight of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="ae9bd-115">SplineStart</span><span class="sxs-lookup"><span data-stu-id="ae9bd-115">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="ae9bd-116">スプラインの角度 (1 ～ 25 の整数) です。</span><span class="sxs-lookup"><span data-stu-id="ae9bd-116">The degree of a spline (an integer from 1 to 25).</span></span>  <br/> |
|[<span data-ttu-id="ae9bd-117">楕円</span><span class="sxs-lookup"><span data-stu-id="ae9bd-117">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="ae9bd-118">楕  *円上*  の点の y 座標。C セルで  *表される x*  座標と組み [合](c-cell-geometry-section.md) わせ。</span><span class="sxs-lookup"><span data-stu-id="ae9bd-118">A  *y*  -coordinate of a point on an ellipse; paired with the  *x*  -coordinate represented by the [C](c-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ae9bd-119">注釈</span><span class="sxs-lookup"><span data-stu-id="ae9bd-119">Remarks</span></span>

<span data-ttu-id="ae9bd-120">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [D] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="ae9bd-120">To get a reference to the D cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ae9bd-121">セル名:</span><span class="sxs-lookup"><span data-stu-id="ae9bd-121">Cell name:</span></span>  <br/> | <span data-ttu-id="ae9bd-122">Geometry  *i*  .D  *j*            *i と*  j =  *<*  1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="ae9bd-122">Geometry  *i*  .D  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="ae9bd-123">Geometry  *i*  .D1 (楕円行) i =  *<*  1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="ae9bd-123">Geometry  *i*  .D1 (Ellipse row)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="ae9bd-124">プログラムから、インデックスによって [D] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="ae9bd-124">To get a reference to the D cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ae9bd-125">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="ae9bd-125">Section index:</span></span>  <br/> |<span data-ttu-id="ae9bd-126">**visSectionFirstComponent**  +  *i* *=* 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="ae9bd-126">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="ae9bd-127">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="ae9bd-127">Row index:</span></span>  <br/> |<span data-ttu-id="ae9bd-128">**visRowVertex**  +  *j* は *j* = 0、1、2..です。</span><span class="sxs-lookup"><span data-stu-id="ae9bd-128">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="ae9bd-129">**visRowVertex** ([Ellipse] 行)</span><span class="sxs-lookup"><span data-stu-id="ae9bd-129">**visRowVertex** (Ellipse row)</span></span>  <br/> |
| <span data-ttu-id="ae9bd-130">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="ae9bd-130">Cell index</span></span>  <br/> |<span data-ttu-id="ae9bd-131">**visAspectRatio** ([EllipticalArcTo] 行)</span><span class="sxs-lookup"><span data-stu-id="ae9bd-131">**visAspectRatio** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="ae9bd-132">**visNURBSWeightPrev** ([NURBSTo] 行)</span><span class="sxs-lookup"><span data-stu-id="ae9bd-132">**visNURBSWeightPrev** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="ae9bd-133">**visSplineDegree** ([SplineStart] 行)</span><span class="sxs-lookup"><span data-stu-id="ae9bd-133">**visSplineDegree** (SplineStart row)</span></span>  <br/> |
||<span data-ttu-id="ae9bd-134">**visEllipseMinorY** ([Ellipse] 行)</span><span class="sxs-lookup"><span data-stu-id="ae9bd-134">**visEllipseMinorY** (Ellipse row)</span></span>  <br/> |
   

