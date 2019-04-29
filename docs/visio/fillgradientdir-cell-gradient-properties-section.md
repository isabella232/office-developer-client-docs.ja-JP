---
title: '[FillGradientDir] セル ([グラデーションのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e8156ff1-c540-44b8-8b69-ba4d54883260
description: 塗りつぶしのグラデーションの方向を決定します。 グラデーションは線形、放射状、角形、またはパスに沿う形を指定できます。
ms.openlocfilehash: 53aad056c7fc1674e00e142fd72a10134103b390
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406718"
---
# <a name="fillgradientdir-cell-gradient-properties-section"></a><span data-ttu-id="b1dd7-104">[FillGradientDir] セル ([グラデーションのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="b1dd7-104">FillGradientDir Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="b1dd7-105">塗りつぶしのグラデーションの方向を決定します。</span><span class="sxs-lookup"><span data-stu-id="b1dd7-105">Determines the direction of the fill gradient.</span></span> <span data-ttu-id="b1dd7-106">グラデーションは線形、放射状、角形、またはパスに沿う形を指定できます。</span><span class="sxs-lookup"><span data-stu-id="b1dd7-106">A gradient can be linear, radial, rectangular, or follow a path.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b1dd7-107">線形のグラデーションは、[**FillGradientDir**] セルで指定した追加の角度値を使用する唯一のグラデーションです。</span><span class="sxs-lookup"><span data-stu-id="b1dd7-107">A linear gradient is the only gradient that takes an additional angle value (as determined by **FillGradientDir** cell).</span></span> <span data-ttu-id="b1dd7-108">他すべてのグラデーションの方向は、事前に設定された列挙型が適用されます。</span><span class="sxs-lookup"><span data-stu-id="b1dd7-108">All other gradient directions have preset enumerations.</span></span> 
  
****

|<span data-ttu-id="b1dd7-109">**値**</span><span class="sxs-lookup"><span data-stu-id="b1dd7-109">**Value**</span></span>|<span data-ttu-id="b1dd7-110">**説明**</span><span class="sxs-lookup"><span data-stu-id="b1dd7-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b1dd7-111">.0</span><span class="sxs-lookup"><span data-stu-id="b1dd7-111">0</span></span>  <br/> |<span data-ttu-id="b1dd7-112">線形のグラデーション。</span><span class="sxs-lookup"><span data-stu-id="b1dd7-112">Linear gradient.</span></span> <span data-ttu-id="b1dd7-113">[**FillGradientAngle**] セルは、グラデーションの方向を決定します。</span><span class="sxs-lookup"><span data-stu-id="b1dd7-113">The **FillGradientAngle** cell determines the direction of the gradient.</span></span>  <br/> |
|<span data-ttu-id="b1dd7-114">1-7</span><span class="sxs-lookup"><span data-stu-id="b1dd7-114">1-7</span></span>  <br/> |<span data-ttu-id="b1dd7-p105">放射状のグラデーション。グラデーションは円の中央から外側に向かって拡張されます。</span><span class="sxs-lookup"><span data-stu-id="b1dd7-p105">Radial gradients. The gradient extends outwards in a circle from a central point.</span></span>  <br/> |
|<span data-ttu-id="b1dd7-117">8-12</span><span class="sxs-lookup"><span data-stu-id="b1dd7-117">8-12</span></span>  <br/> |<span data-ttu-id="b1dd7-p106">角形のグラデーション。グラデーションは、角形のフェードを使用して原点から矢印線として拡張されます。</span><span class="sxs-lookup"><span data-stu-id="b1dd7-p106">Rectangular gradients. The gradient extends as a directional line from an origin with a rectangular-shaped fade.</span></span>  <br/> |
|<span data-ttu-id="b1dd7-120">13 </span><span class="sxs-lookup"><span data-stu-id="b1dd7-120">13</span></span>  <br/> |<span data-ttu-id="b1dd7-121">パスのグラデーション。</span><span class="sxs-lookup"><span data-stu-id="b1dd7-121">Path gradient.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b1dd7-122">注釈</span><span class="sxs-lookup"><span data-stu-id="b1dd7-122">Remarks</span></span>

<span data-ttu-id="b1dd7-123">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**FillGradientDir**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="b1dd7-123">To get a reference to the **FillGradientDir** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b1dd7-124">セル名:</span><span class="sxs-lookup"><span data-stu-id="b1dd7-124">Cell name:</span></span>  <br/> | <span data-ttu-id="b1dd7-125">[fillgradientdir]</span><span class="sxs-lookup"><span data-stu-id="b1dd7-125">FillGradientDir</span></span>  <br/> |
   
<span data-ttu-id="b1dd7-126">プログラムから、インデックスによって [**FillGradientDir**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="b1dd7-126">To get a reference to the **FillGradientDir** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b1dd7-127">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="b1dd7-127">Section index:</span></span>  <br/> |<span data-ttu-id="b1dd7-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b1dd7-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b1dd7-129">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="b1dd7-129">Row index:</span></span>  <br/> |<span data-ttu-id="b1dd7-130">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="b1dd7-130">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="b1dd7-131">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="b1dd7-131">Cell index:</span></span>  <br/> |<span data-ttu-id="b1dd7-132">**visFillGradientDir**</span><span class="sxs-lookup"><span data-stu-id="b1dd7-132">**visFillGradientDir**</span></span> <br/> |
   

