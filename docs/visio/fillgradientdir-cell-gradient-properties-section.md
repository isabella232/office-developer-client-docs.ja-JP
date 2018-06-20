---
title: '[FillGradientDir] セル ([グラデーションのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e8156ff1-c540-44b8-8b69-ba4d54883260
description: 塗りつぶしのグラデーションの方向を決定します。グラデーションは線形、放射状、角形、またはパスに沿う形を指定できます。
ms.openlocfilehash: 9b4226892e70fcffe7a78d109bd852e6d4f93838
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805376"
---
# <a name="fillgradientdir-cell-gradient-properties-section"></a><span data-ttu-id="02ae6-104">[FillGradientDir] セル ([グラデーションのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="02ae6-104">FillGradientDir Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="02ae6-p102">塗りつぶしのグラデーションの方向を決定します。グラデーションは線形、放射状、角形、またはパスに沿う形を指定できます。</span><span class="sxs-lookup"><span data-stu-id="02ae6-p102">Determines the direction of the fill gradient. A gradient can be linear, radial, rectangular, or follow a path.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="02ae6-107">線形グラデーションは、グラデーション ( **FillGradientDir**セルによって決まります)、その他の角度の値を受け取るだけです。</span><span class="sxs-lookup"><span data-stu-id="02ae6-107">A linear gradient is the only gradient that takes an additional angle value (as determined by **FillGradientDir** cell).</span></span> <span data-ttu-id="02ae6-108">他のすべてのグラデーションの方向には、列挙値が事前設定されます。</span><span class="sxs-lookup"><span data-stu-id="02ae6-108">All other gradient directions have preset enumerations.</span></span> 
  
****

|<span data-ttu-id="02ae6-109">**値**</span><span class="sxs-lookup"><span data-stu-id="02ae6-109">**Value**</span></span>|<span data-ttu-id="02ae6-110">**説明**</span><span class="sxs-lookup"><span data-stu-id="02ae6-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="02ae6-111">0</span><span class="sxs-lookup"><span data-stu-id="02ae6-111">0</span></span>  <br/> |<span data-ttu-id="02ae6-112">線形グラデーションです。</span><span class="sxs-lookup"><span data-stu-id="02ae6-112">Linear gradient.</span></span> <span data-ttu-id="02ae6-113">**FillGradientAngle**セルでは、グラデーションの方向を決定します。</span><span class="sxs-lookup"><span data-stu-id="02ae6-113">The **FillGradientAngle** cell determines the direction of the gradient.</span></span>  <br/> |
|<span data-ttu-id="02ae6-114">1-7</span><span class="sxs-lookup"><span data-stu-id="02ae6-114">1-7</span></span>  <br/> |<span data-ttu-id="02ae6-p105">放射状のグラデーション。グラデーションは円の中央から外側に向かって拡張されます。</span><span class="sxs-lookup"><span data-stu-id="02ae6-p105">Radial gradients. The gradient extends outwards in a circle from a central point.</span></span>  <br/> |
|<span data-ttu-id="02ae6-117">8-12</span><span class="sxs-lookup"><span data-stu-id="02ae6-117">8-12</span></span>  <br/> |<span data-ttu-id="02ae6-p106">角形のグラデーション。グラデーションは、角形のフェードを使用して原点から矢印線として拡張されます。</span><span class="sxs-lookup"><span data-stu-id="02ae6-p106">Rectangular gradients. The gradient extends as a directional line from an origin with a rectangular-shaped fade.</span></span>  <br/> |
|<span data-ttu-id="02ae6-120">13</span><span class="sxs-lookup"><span data-stu-id="02ae6-120">13</span></span>  <br/> |<span data-ttu-id="02ae6-121">パスのグラデーション。</span><span class="sxs-lookup"><span data-stu-id="02ae6-121">Path gradient.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="02ae6-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="02ae6-122">Remarks</span></span>

<span data-ttu-id="02ae6-123">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **FillGradientDir** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="02ae6-123">To get a reference to the **FillGradientDir** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="02ae6-124">セル名:</span><span class="sxs-lookup"><span data-stu-id="02ae6-124">Cell name:</span></span>  <br/> | <span data-ttu-id="02ae6-125">FillGradientDir</span><span class="sxs-lookup"><span data-stu-id="02ae6-125">FillGradientDir</span></span>  <br/> |
   
<span data-ttu-id="02ae6-126">プログラムから、インデックスによって [ **FillGradientDir** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="02ae6-126">To get a reference to the **FillGradientDir** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="02ae6-127">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="02ae6-127">Section index:</span></span>  <br/> |<span data-ttu-id="02ae6-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="02ae6-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="02ae6-129">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="02ae6-129">Row index:</span></span>  <br/> |<span data-ttu-id="02ae6-130">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="02ae6-130">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="02ae6-131">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="02ae6-131">Cell index:</span></span>  <br/> |<span data-ttu-id="02ae6-132">**visFillGradientDir**</span><span class="sxs-lookup"><span data-stu-id="02ae6-132">**visFillGradientDir**</span></span> <br/> |
   

