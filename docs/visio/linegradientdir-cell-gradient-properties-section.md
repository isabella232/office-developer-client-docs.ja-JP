---
title: '[LineGradientDir] セル ([グラデーションのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c603f9a5-f887-47ce-90bb-d41ec2d1a6a1
description: 線のグラデーションの方向を決定します。グラデーションは線形、放射状、角形、またはパスに沿う形を指定できます。
ms.openlocfilehash: 6243d7a6b470db0915ba6fc462f05b72a9814f66
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805712"
---
# <a name="linegradientdir-cell-gradient-properties-section"></a><span data-ttu-id="8380c-104">[LineGradientDir] セル ([グラデーションのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="8380c-104">LineGradientDir Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="8380c-p102">線のグラデーションの方向を決定します。グラデーションは線形、放射状、角形、またはパスに沿う形を指定できます。</span><span class="sxs-lookup"><span data-stu-id="8380c-p102">Determines the direction of the line gradient. A gradient can be linear, radial, rectangular, or follow a path.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8380c-p103">線形のグラデーションは、[**LineGradientDir**] セルで指定した追加の角度値を使用する唯一のグラデーションです。他すべてのグラデーションの方向は、事前に設定された列挙型が適用されます。</span><span class="sxs-lookup"><span data-stu-id="8380c-p103">A linear gradient is the only gradient that takes an additional angle value (as determined by **LineGradientDir** cell). All other gradient directions have preset enumerations.</span></span> 
  
|<span data-ttu-id="8380c-109">**値**</span><span class="sxs-lookup"><span data-stu-id="8380c-109">**Value**</span></span>|<span data-ttu-id="8380c-110">**説明**</span><span class="sxs-lookup"><span data-stu-id="8380c-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8380c-111">0</span><span class="sxs-lookup"><span data-stu-id="8380c-111">0</span></span>  <br/> |<span data-ttu-id="8380c-p104">線形のグラデーション。[**LineGradientAngle**] セルは、グラデーションの方向を決定します。</span><span class="sxs-lookup"><span data-stu-id="8380c-p104">Linear gradient. The **LineGradientAngle** cell determines the direction of the gradient.  </span></span><br/> |
|<span data-ttu-id="8380c-114">1-7</span><span class="sxs-lookup"><span data-stu-id="8380c-114">1-7</span></span>  <br/> |<span data-ttu-id="8380c-p105">放射状のグラデーション。グラデーションは円の中央から外側に向かって拡張されます。</span><span class="sxs-lookup"><span data-stu-id="8380c-p105">Radial gradients. The gradient extends outwards in a circle from a central point.</span></span>  <br/> |
|<span data-ttu-id="8380c-117">8-12</span><span class="sxs-lookup"><span data-stu-id="8380c-117">8-12</span></span>  <br/> |<span data-ttu-id="8380c-p106">角形のグラデーション。グラデーションは、角形のフェードを使用して原点から矢印線として拡張されます。</span><span class="sxs-lookup"><span data-stu-id="8380c-p106">Rectangular gradients. The gradient extends as a directional line from an origin with a rectangular-shaped fade.</span></span>  <br/> |
|<span data-ttu-id="8380c-120">13</span><span class="sxs-lookup"><span data-stu-id="8380c-120">13</span></span>  <br/> |<span data-ttu-id="8380c-121">パスのグラデーション。</span><span class="sxs-lookup"><span data-stu-id="8380c-121">Path gradient.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8380c-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="8380c-122">Remarks</span></span>

<span data-ttu-id="8380c-123">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**LineGradientDir**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="8380c-123">To get a reference to the **LineGradientDir** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8380c-124">セル名:</span><span class="sxs-lookup"><span data-stu-id="8380c-124">Cell name:</span></span>  <br/> | <span data-ttu-id="8380c-125">LineGradientDir</span><span class="sxs-lookup"><span data-stu-id="8380c-125">LineGradientDir</span></span>  <br/> |
   
<span data-ttu-id="8380c-126">プログラムから、インデックスによって [**LineGradientDir**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="8380c-126">To get a reference to the **LineGradientDir** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8380c-127">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="8380c-127">Section index:</span></span>  <br/> |<span data-ttu-id="8380c-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8380c-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="8380c-129">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="8380c-129">Row index:</span></span>  <br/> |<span data-ttu-id="8380c-130">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="8380c-130">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="8380c-131">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="8380c-131">Cell index:</span></span>  <br/> |<span data-ttu-id="8380c-132">**visLineGradientDir**</span><span class="sxs-lookup"><span data-stu-id="8380c-132">**visLineGradientDir**</span></span> <br/> |
   

