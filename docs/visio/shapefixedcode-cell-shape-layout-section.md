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
# <a name="shapefixedcode-cell-shape-layout-section"></a><span data-ttu-id="de92c-103">[ShapeFixedCode] セル ([Shape Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="de92c-103">ShapeFixedCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="de92c-104">配置可能な図形について、配置時の動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="de92c-104">Specifies placement behavior for a placeable shape.</span></span>
  
|<span data-ttu-id="de92c-105">**値**</span><span class="sxs-lookup"><span data-stu-id="de92c-105">**Value**</span></span>|<span data-ttu-id="de92c-106">**選択モード**</span><span class="sxs-lookup"><span data-stu-id="de92c-106">**Selection mode**</span></span>|<span data-ttu-id="de92c-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="de92c-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="de92c-108">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="de92c-108">&amp;H1</span></span>  <br/> |<span data-ttu-id="de92c-109">[**レイアウトの構成**] ダイアログボックスを使用して図形をレイアウトするときに、この図形は移動しません。</span><span class="sxs-lookup"><span data-stu-id="de92c-109">Don't move this shape when shapes are laid out by using the **Configure Layout** dialog box.</span></span>  <br/> |<span data-ttu-id="de92c-110">**visslofixedplacement**</span><span class="sxs-lookup"><span data-stu-id="de92c-110">**visSLOFixedPlacement**</span></span> <br/> |
|<span data-ttu-id="de92c-111">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="de92c-111">&amp;H2</span></span>  <br/> |<span data-ttu-id="de92c-112">この図形は移動しません。また他の図形をこの図形の上に配置できません。</span><span class="sxs-lookup"><span data-stu-id="de92c-112">Don't move this shape and do not allow shapes that plow to be placed on top of it.</span></span>  <br/> |<span data-ttu-id="de92c-113">**visslofixedplow 移動**</span><span class="sxs-lookup"><span data-stu-id="de92c-113">**visSLOFixedPlow**</span></span> <br/> |
|<span data-ttu-id="de92c-114">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="de92c-114">&amp;H4</span></span>  <br/> |<span data-ttu-id="de92c-115">この図形は移動しません。ただし他の図形をこの図形の上に配置できます。</span><span class="sxs-lookup"><span data-stu-id="de92c-115">Don't move this shape and allow shapes that plow to be placed on top of it.</span></span>  <br/> |<span data-ttu-id="de92c-116">**visSLOFixedPermeablePlow**</span><span class="sxs-lookup"><span data-stu-id="de92c-116">**visSLOFixedPermeablePlow**</span></span> <br/> |
|<span data-ttu-id="de92c-117">&amp;H20 (32)</span><span class="sxs-lookup"><span data-stu-id="de92c-117">&amp;H20 (32)</span></span>  <br/> |<span data-ttu-id="de92c-118">迂回するときに、接続ポイントの位置を無視します。</span><span class="sxs-lookup"><span data-stu-id="de92c-118">Ignore connection point locations when being routed to.</span></span>  <br/> |<span data-ttu-id="de92c-119">**visslofixedconnptsignore**</span><span class="sxs-lookup"><span data-stu-id="de92c-119">**visSLOFixedConnPtsIgnore**</span></span> <br/> |
|<span data-ttu-id="de92c-120">&amp;H40 (64)</span><span class="sxs-lookup"><span data-stu-id="de92c-120">&amp;H40 (64)</span></span>  <br/> |<span data-ttu-id="de92c-121">接続ポイントがある側だけに迂回します。</span><span class="sxs-lookup"><span data-stu-id="de92c-121">Only allow routing to sides with connection points.</span></span>  <br/> |<span data-ttu-id="de92c-122">**visslofixedconnptsonly**</span><span class="sxs-lookup"><span data-stu-id="de92c-122">**visSLOFixedConnPtsOnly**</span></span> <br/> |
|<span data-ttu-id="de92c-123">&amp;H80 (128)</span><span class="sxs-lookup"><span data-stu-id="de92c-123">&amp;H80 (128)</span></span>  <br/> |<span data-ttu-id="de92c-124">この図形の外周には接着しません。</span><span class="sxs-lookup"><span data-stu-id="de92c-124">Don't glue to the perimeter of this shape.</span></span> <span data-ttu-id="de92c-125">代わりに、図形の図形枠に接着します。</span><span class="sxs-lookup"><span data-stu-id="de92c-125">Glue to the shape's alignment box instead.</span></span>  <br/> |<span data-ttu-id="de92c-126">**visSLOFixedNoFoldToShape**</span><span class="sxs-lookup"><span data-stu-id="de92c-126">**visSLOFixedNoFoldToShape**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="de92c-127">注釈</span><span class="sxs-lookup"><span data-stu-id="de92c-127">Remarks</span></span>

<span data-ttu-id="de92c-128">このセルの値は、[**基本動作**] ダイアログボックスの [**配置**] タブで設定することもできます (図形が選択されている場合)、[[開発](run-in-developer-mode-display-the-developer-tab.md)] タブの [**図形のデザイン**] グループで、[**基本動作**] をクリックし、[**配置**] タブをクリックします。).</span><span class="sxs-lookup"><span data-stu-id="de92c-128">You can also set the value of this cell on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="de92c-129">このセルには、上記の値を任意に組み合わせて設定できます。</span><span class="sxs-lookup"><span data-stu-id="de92c-129">You can set any combination of these values for this cell.</span></span> <span data-ttu-id="de92c-130">たとえば、値 3&amp;(H3) を入力すると、[レイアウトの**構成**] ダイアログボックス ([**デザイン**] タブの [**レイアウト**] グループで、[ページ\*\*\*\*\*\*の再レイアウト] をクリックし、[] をクリックします) を使用して、図形をレイアウトするときに移動を省略できます。\*\* その他のレイアウトオプション) と、他の配置可能な図形を図形の上または近くに配置する場合。</span><span class="sxs-lookup"><span data-stu-id="de92c-130">For example, you can enter the value 3 (&amp;H3), which eliminates movement when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options** ) and when other placeable shapes are placed on or near the shape.</span></span> 
  
<span data-ttu-id="de92c-131">Visio 2000 より前のバージョンでは、[Miscellaneous] セクションで [ObjInteract] セルを使用してこの動作を設定していました。</span><span class="sxs-lookup"><span data-stu-id="de92c-131">In versions earlier than Visio 2000, you set this behavior using the ObjInteract cell in the Miscellaneous section.</span></span> 
  
<span data-ttu-id="de92c-132">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShapeFixedCode] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="de92c-132">To get a reference to the ShapeFixedCode cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="de92c-133">セル名 :</span><span class="sxs-lookup"><span data-stu-id="de92c-133">Cell name:</span></span>  <br/> |<span data-ttu-id="de92c-134">[shapefixedcode]</span><span class="sxs-lookup"><span data-stu-id="de92c-134">ShapeFixedCode</span></span>  <br/> |
   
<span data-ttu-id="de92c-135">プログラムから、インデックスによって [ShapeFixedCode] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="de92c-135">To get a reference to the ShapeFixedCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="de92c-136">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="de92c-136">Section index:</span></span>  <br/> |<span data-ttu-id="de92c-137">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="de92c-137">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="de92c-138">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="de92c-138">Row index:</span></span>  <br/> |<span data-ttu-id="de92c-139">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="de92c-139">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="de92c-140">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="de92c-140">Cell index:</span></span>  <br/> |<span data-ttu-id="de92c-141">**visslofixedcode**</span><span class="sxs-lookup"><span data-stu-id="de92c-141">**visSLOFixedCode**</span></span> <br/> |
   

