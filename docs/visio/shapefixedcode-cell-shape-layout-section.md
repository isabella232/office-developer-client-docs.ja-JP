---
title: '[ShapeFixedCode] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm880
localization_priority: Normal
ms.assetid: a1736a5c-421c-2bdb-b164-76a8cd06cc3d
description: 配置可能な図形について、配置時の動作を指定します。
ms.openlocfilehash: eae44a0579129fbe8da1c0cc8c37318beb024563
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431744"
---
# <a name="shapefixedcode-cell-shape-layout-section"></a><span data-ttu-id="4e736-103">[ShapeFixedCode] セル ([Shape Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="4e736-103">ShapeFixedCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="4e736-104">配置可能な図形について、配置時の動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="4e736-104">Specifies placement behavior for a placeable shape.</span></span>
  
|<span data-ttu-id="4e736-105">**値**</span><span class="sxs-lookup"><span data-stu-id="4e736-105">**Value**</span></span>|<span data-ttu-id="4e736-106">**選択モード**</span><span class="sxs-lookup"><span data-stu-id="4e736-106">**Selection mode**</span></span>|<span data-ttu-id="4e736-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="4e736-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4e736-108">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="4e736-108">&amp;H1</span></span>  <br/> |<span data-ttu-id="4e736-109">[レイアウトの構成] ダイアログ ボックスを使用して図形をレイアウトするときに、この **図形を** 移動しない。</span><span class="sxs-lookup"><span data-stu-id="4e736-109">Don't move this shape when shapes are laid out by using the **Configure Layout** dialog box.</span></span>  <br/> |<span data-ttu-id="4e736-110">**visSLOFixedPlacement**</span><span class="sxs-lookup"><span data-stu-id="4e736-110">**visSLOFixedPlacement**</span></span> <br/> |
|<span data-ttu-id="4e736-111">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="4e736-111">&amp;H2</span></span>  <br/> |<span data-ttu-id="4e736-112">この図形は移動しません。また他の図形をこの図形の上に配置できません。</span><span class="sxs-lookup"><span data-stu-id="4e736-112">Don't move this shape and do not allow shapes that plow to be placed on top of it.</span></span>  <br/> |<span data-ttu-id="4e736-113">**visSLOFixedPlow**</span><span class="sxs-lookup"><span data-stu-id="4e736-113">**visSLOFixedPlow**</span></span> <br/> |
|<span data-ttu-id="4e736-114">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="4e736-114">&amp;H4</span></span>  <br/> |<span data-ttu-id="4e736-115">この図形は移動しません。ただし他の図形をこの図形の上に配置できます。</span><span class="sxs-lookup"><span data-stu-id="4e736-115">Don't move this shape and allow shapes that plow to be placed on top of it.</span></span>  <br/> |<span data-ttu-id="4e736-116">**visSLOFixedPermeablePlow**</span><span class="sxs-lookup"><span data-stu-id="4e736-116">**visSLOFixedPermeablePlow**</span></span> <br/> |
|<span data-ttu-id="4e736-117">&amp;H20 (32)</span><span class="sxs-lookup"><span data-stu-id="4e736-117">&amp;H20 (32)</span></span>  <br/> |<span data-ttu-id="4e736-118">迂回するときに、接続ポイントの位置を無視します。</span><span class="sxs-lookup"><span data-stu-id="4e736-118">Ignore connection point locations when being routed to.</span></span>  <br/> |<span data-ttu-id="4e736-119">**visSLOFixedConnPtsIgnore**</span><span class="sxs-lookup"><span data-stu-id="4e736-119">**visSLOFixedConnPtsIgnore**</span></span> <br/> |
|<span data-ttu-id="4e736-120">&amp;H40 (64)</span><span class="sxs-lookup"><span data-stu-id="4e736-120">&amp;H40 (64)</span></span>  <br/> |<span data-ttu-id="4e736-121">接続ポイントがある側だけに迂回します。</span><span class="sxs-lookup"><span data-stu-id="4e736-121">Only allow routing to sides with connection points.</span></span>  <br/> |<span data-ttu-id="4e736-122">**visSLOFixedConnPtsOnly**</span><span class="sxs-lookup"><span data-stu-id="4e736-122">**visSLOFixedConnPtsOnly**</span></span> <br/> |
|<span data-ttu-id="4e736-123">&amp;H80 (128)</span><span class="sxs-lookup"><span data-stu-id="4e736-123">&amp;H80 (128)</span></span>  <br/> |<span data-ttu-id="4e736-p101">この図形の外周には接着しません。代わりに、図形の図形枠に接着します。</span><span class="sxs-lookup"><span data-stu-id="4e736-p101">Don't glue to the perimeter of this shape. Glue to the shape's alignment box instead.</span></span>  <br/> |<span data-ttu-id="4e736-126">**visSLOFixedNoFoldToShape**</span><span class="sxs-lookup"><span data-stu-id="4e736-126">**visSLOFixedNoFoldToShape**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4e736-127">注釈</span><span class="sxs-lookup"><span data-stu-id="4e736-127">Remarks</span></span>

<span data-ttu-id="4e736-128">[動作] ダイアログ ボックスの [配置] タブで、このセルの値を設定することもできます (図形が選択されている場合は、[開発] タブの[図形のデザイン] グループで、[動作] をクリックし、[配置] タブ **をクリック** します)。  [](run-in-developer-mode-display-the-developer-tab.md)</span><span class="sxs-lookup"><span data-stu-id="4e736-128">You can also set the value of this cell on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="4e736-129">このセルには、上記の値を任意に組み合わせて設定できます。</span><span class="sxs-lookup"><span data-stu-id="4e736-129">You can set any combination of these values for this cell.</span></span> <span data-ttu-id="4e736-130">たとえば、値 3 ( H3) を入力すると、[レイアウトの構成] ダイアログ ボックス &amp; ([デザイン] タブの [レイアウト]グループで、[レイアウトの再レイアウト] ページ) をクリックし、[その他のレイアウト オプション] をクリックして、図形の上または近くに他の配置可能な図形を配置すると、図形をレイアウトするときに移動を排除できます。</span><span class="sxs-lookup"><span data-stu-id="4e736-130">For example, you can enter the value 3 (&amp;H3), which eliminates movement when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options** ) and when other placeable shapes are placed on or near the shape.</span></span> 
  
<span data-ttu-id="4e736-131">Visio 2000 より前のバージョンでは、[Miscellaneous] セクションで [ObjInteract] セルを使用してこの動作を設定していました。</span><span class="sxs-lookup"><span data-stu-id="4e736-131">In versions earlier than Visio 2000, you set this behavior using the ObjInteract cell in the Miscellaneous section.</span></span> 
  
<span data-ttu-id="4e736-132">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShapeFixedCode] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="4e736-132">To get a reference to the ShapeFixedCode cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4e736-133">セル名 :</span><span class="sxs-lookup"><span data-stu-id="4e736-133">Cell name:</span></span>  <br/> |<span data-ttu-id="4e736-134">ShapeFixedCode</span><span class="sxs-lookup"><span data-stu-id="4e736-134">ShapeFixedCode</span></span>  <br/> |
   
<span data-ttu-id="4e736-135">プログラムから、インデックスによって [ShapeFixedCode] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="4e736-135">To get a reference to the ShapeFixedCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4e736-136">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="4e736-136">Section index:</span></span>  <br/> |<span data-ttu-id="4e736-137">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4e736-137">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="4e736-138">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="4e736-138">Row index:</span></span>  <br/> |<span data-ttu-id="4e736-139">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="4e736-139">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="4e736-140">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="4e736-140">Cell index:</span></span>  <br/> |<span data-ttu-id="4e736-141">**visSLOFixedCode**</span><span class="sxs-lookup"><span data-stu-id="4e736-141">**visSLOFixedCode**</span></span> <br/> |
   

