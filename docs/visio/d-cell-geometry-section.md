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
description: 各行に対応する情報を表示します。 次の表に、各行で [D] セルが示す内容を説明します。
ms.openlocfilehash: a76093f028986907b58175bc6b8c81a7056cfe07
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542500"
---
# <a name="d-cell-geometry-section"></a><span data-ttu-id="a6585-104">[D] セル ([Geometry] セクション)</span><span class="sxs-lookup"><span data-stu-id="a6585-104">D Cell (Geometry Section)</span></span>

<span data-ttu-id="a6585-105">各行に対応する情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="a6585-105">Represents different information in different rows.</span></span> <span data-ttu-id="a6585-106">次の表に、各行で [D] セルが示す内容を説明します。</span><span class="sxs-lookup"><span data-stu-id="a6585-106">This table describes the D cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="a6585-107">Row</span><span class="sxs-lookup"><span data-stu-id="a6585-107">Row</span></span>|<span data-ttu-id="a6585-108">説明</span><span class="sxs-lookup"><span data-stu-id="a6585-108">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="a6585-109">[[Ellipticalarcto]](ellipticalarcto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="a6585-109">[EllipticalArcTo](ellipticalarcto-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="a6585-p103">円弧の長軸と短軸の比率です。これらの言葉の通常の意味とは関係なく、"長" 軸が "短" 軸よりも長い必要はありません。したがって、比率は 1 より大きい必要はありません。このセルを 0 以下、または 1000 より大きく設定すると、予測できない結果になる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a6585-p103">The ratio of an arc's major axis to its minor axis. Despite the usual meaning of these words, the "major" axis does not have to be greater than the "minor" axis, so this ratio does not have to be greater than 1. Setting this cell to a value less than or equal to 0 or greater than 1000 can lead to unpredictable results.</span></span>  <br/> |
|<span data-ttu-id="a6585-113">[[Nurbsto]](nurbsto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="a6585-113">[NURBSTo](nurbsto-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="a6585-114">NURBS (nonuniform rational B-spline) の最初の太さです。</span><span class="sxs-lookup"><span data-stu-id="a6585-114">The first weight of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|<span data-ttu-id="a6585-115">[[Splinestart]](splinestart-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="a6585-115">[SplineStart](splinestart-row-geometry-section.md)</span></span> <br/> | <span data-ttu-id="a6585-116">スプラインの角度 (1 ～ 25 の整数) です。</span><span class="sxs-lookup"><span data-stu-id="a6585-116">The degree of a spline (an integer from 1 to 25).</span></span>  <br/> |
|[<span data-ttu-id="a6585-117">もう</span><span class="sxs-lookup"><span data-stu-id="a6585-117">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="a6585-118">楕円上の点の*y*座標です。[ [C](c-cell-geometry-section.md)セルで表される*x*座標と対にします。</span><span class="sxs-lookup"><span data-stu-id="a6585-118">A  *y*  -coordinate of a point on an ellipse; paired with the  *x*  -coordinate represented by the [C](c-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a6585-119">注釈</span><span class="sxs-lookup"><span data-stu-id="a6585-119">Remarks</span></span>

<span data-ttu-id="a6585-120">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [D] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="a6585-120">To get a reference to the D cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a6585-121">セル名:</span><span class="sxs-lookup"><span data-stu-id="a6585-121">Cell name:</span></span>  <br/> | <span data-ttu-id="a6585-122">ジオメトリ*i*D *j* where *i*および*j* = <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="a6585-122">Geometry  *i*  .D  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="a6585-123">ジオメトリ*i*D1 (楕円行) *i* = <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="a6585-123">Geometry  *i*  .D1 (Ellipse row)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="a6585-124">プログラムから、インデックスによって [D] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="a6585-124">To get a reference to the D cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a6585-125">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="a6585-125">Section index:</span></span>  <br/> |<span data-ttu-id="a6585-126">**visSectionFirstComponent** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="a6585-126">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="a6585-127">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="a6585-127">Row index:</span></span>  <br/> |<span data-ttu-id="a6585-128">**visRowVertex** +  *j* where *j* = 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="a6585-128">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="a6585-129">**visRowVertex** ([Ellipse] 行)</span><span class="sxs-lookup"><span data-stu-id="a6585-129">**visRowVertex** (Ellipse row)</span></span>  <br/> |
| <span data-ttu-id="a6585-130">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="a6585-130">Cell index</span></span>  <br/> |<span data-ttu-id="a6585-131">**visAspectRatio** ([EllipticalArcTo] 行)</span><span class="sxs-lookup"><span data-stu-id="a6585-131">**visAspectRatio** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="a6585-132">**visNURBSWeightPrev** ([NURBSTo] 行)</span><span class="sxs-lookup"><span data-stu-id="a6585-132">**visNURBSWeightPrev** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="a6585-133">**visSplineDegree** ([SplineStart] 行)</span><span class="sxs-lookup"><span data-stu-id="a6585-133">**visSplineDegree** (SplineStart row)</span></span>  <br/> |
||<span data-ttu-id="a6585-134">**visEllipseMinorY** ([Ellipse] 行)</span><span class="sxs-lookup"><span data-stu-id="a6585-134">**visEllipseMinorY** (Ellipse row)</span></span>  <br/> |
   

