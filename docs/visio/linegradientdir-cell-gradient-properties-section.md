---
title: '[LineGradientDir] セル ([グラデーションのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c603f9a5-f887-47ce-90bb-d41ec2d1a6a1
description: 線のグラデーションの方向を決定します。 グラデーションは線形、放射状、角形、またはパスに沿う形を指定できます。
ms.openlocfilehash: 05dcc6904a4e67d97c632dba44635936b1c14049
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350961"
---
# <a name="linegradientdir-cell-gradient-properties-section"></a><span data-ttu-id="fbaae-104">[LineGradientDir] セル ([グラデーションのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="fbaae-104">LineGradientDir Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="fbaae-105">線のグラデーションの方向を決定します。</span><span class="sxs-lookup"><span data-stu-id="fbaae-105">Determines the direction of the line gradient.</span></span> <span data-ttu-id="fbaae-106">グラデーションは線形、放射状、角形、またはパスに沿う形を指定できます。</span><span class="sxs-lookup"><span data-stu-id="fbaae-106">A gradient can be linear, radial, rectangular, or follow a path.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="fbaae-107">線形のグラデーションは、[**LineGradientDir**] セルで指定した追加の角度値を使用する唯一のグラデーションです。</span><span class="sxs-lookup"><span data-stu-id="fbaae-107">A linear gradient is the only gradient that takes an additional angle value (as determined by **LineGradientDir** cell).</span></span> <span data-ttu-id="fbaae-108">他すべてのグラデーションの方向は、事前に設定された列挙型が適用されます。</span><span class="sxs-lookup"><span data-stu-id="fbaae-108">All other gradient directions have preset enumerations.</span></span> 
  
|<span data-ttu-id="fbaae-109">**値**</span><span class="sxs-lookup"><span data-stu-id="fbaae-109">**Value**</span></span>|<span data-ttu-id="fbaae-110">**説明**</span><span class="sxs-lookup"><span data-stu-id="fbaae-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fbaae-111">.0</span><span class="sxs-lookup"><span data-stu-id="fbaae-111">0</span></span>  <br/> |<span data-ttu-id="fbaae-112">線形のグラデーション。</span><span class="sxs-lookup"><span data-stu-id="fbaae-112">Linear gradient.</span></span> <span data-ttu-id="fbaae-113">[**LineGradientAngle**] セルは、グラデーションの方向を決定します。</span><span class="sxs-lookup"><span data-stu-id="fbaae-113">The **LineGradientAngle** cell determines the direction of the gradient.</span></span>  <br/> |
|<span data-ttu-id="fbaae-114">1-7</span><span class="sxs-lookup"><span data-stu-id="fbaae-114">1-7</span></span>  <br/> |<span data-ttu-id="fbaae-p105">放射状のグラデーション。グラデーションは円の中央から外側に向かって拡張されます。</span><span class="sxs-lookup"><span data-stu-id="fbaae-p105">Radial gradients. The gradient extends outwards in a circle from a central point.</span></span>  <br/> |
|<span data-ttu-id="fbaae-117">8-12</span><span class="sxs-lookup"><span data-stu-id="fbaae-117">8-12</span></span>  <br/> |<span data-ttu-id="fbaae-p106">角形のグラデーション。グラデーションは、角形のフェードを使用して原点から矢印線として拡張されます。</span><span class="sxs-lookup"><span data-stu-id="fbaae-p106">Rectangular gradients. The gradient extends as a directional line from an origin with a rectangular-shaped fade.</span></span>  <br/> |
|<span data-ttu-id="fbaae-120">スリー</span><span class="sxs-lookup"><span data-stu-id="fbaae-120">13</span></span>  <br/> |<span data-ttu-id="fbaae-121">パスのグラデーション。</span><span class="sxs-lookup"><span data-stu-id="fbaae-121">Path gradient.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fbaae-122">解説</span><span class="sxs-lookup"><span data-stu-id="fbaae-122">Remarks</span></span>

<span data-ttu-id="fbaae-123">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**LineGradientDir**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="fbaae-123">To get a reference to the **LineGradientDir** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fbaae-124">セル名:</span><span class="sxs-lookup"><span data-stu-id="fbaae-124">Cell name:</span></span>  <br/> | <span data-ttu-id="fbaae-125">[linegradientdir]</span><span class="sxs-lookup"><span data-stu-id="fbaae-125">LineGradientDir</span></span>  <br/> |
   
<span data-ttu-id="fbaae-126">プログラムから、インデックスによって [**LineGradientDir**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="fbaae-126">To get a reference to the **LineGradientDir** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fbaae-127">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="fbaae-127">Section index:</span></span>  <br/> |<span data-ttu-id="fbaae-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fbaae-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="fbaae-129">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="fbaae-129">Row index:</span></span>  <br/> |<span data-ttu-id="fbaae-130">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="fbaae-130">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="fbaae-131">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="fbaae-131">Cell index:</span></span>  <br/> |<span data-ttu-id="fbaae-132">**visLineGradientDir**</span><span class="sxs-lookup"><span data-stu-id="fbaae-132">**visLineGradientDir**</span></span> <br/> |
   

