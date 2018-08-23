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
ms.openlocfilehash: 6ae83fa70cc545c88080ce27046bd8c226c060e3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806386"
---
# <a name="shapefixedcode-cell-shape-layout-section"></a><span data-ttu-id="0bfc9-103">[ShapeFixedCode] セル ([図形レイアウト] セクション)</span><span class="sxs-lookup"><span data-stu-id="0bfc9-103">ShapeFixedCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="0bfc9-104">配置可能な図形について、配置時の動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="0bfc9-104">Specifies placement behavior for a placeable shape.</span></span>
  
|<span data-ttu-id="0bfc9-105">**値**</span><span class="sxs-lookup"><span data-stu-id="0bfc9-105">**Value**</span></span>|<span data-ttu-id="0bfc9-106">**選択モード**</span><span class="sxs-lookup"><span data-stu-id="0bfc9-106">**Selection mode**</span></span>|<span data-ttu-id="0bfc9-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="0bfc9-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0bfc9-108">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="0bfc9-108">&amp;H1</span></span>  <br/> |<span data-ttu-id="0bfc9-109">**レイアウトの構成**] ダイアログ ボックスを使用して図形をレイアウトするとき、この図形を移動しません。</span><span class="sxs-lookup"><span data-stu-id="0bfc9-109">Don't move this shape when shapes are laid out by using the **Configure Layout** dialog box.</span></span>  <br/> |<span data-ttu-id="0bfc9-110">**visSLOFixedPlacement**</span><span class="sxs-lookup"><span data-stu-id="0bfc9-110">**visSLOFixedPlacement**</span></span> <br/> |
|<span data-ttu-id="0bfc9-111">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="0bfc9-111">&amp;H2</span></span>  <br/> |<span data-ttu-id="0bfc9-112">この図形は移動しません。また他の図形をこの図形の上に配置できません。</span><span class="sxs-lookup"><span data-stu-id="0bfc9-112">Don't move this shape and do not allow shapes that plow to be placed on top of it.</span></span>  <br/> |<span data-ttu-id="0bfc9-113">**visSLOFixedPlow**</span><span class="sxs-lookup"><span data-stu-id="0bfc9-113">**visSLOFixedPlow**</span></span> <br/> |
|<span data-ttu-id="0bfc9-114">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="0bfc9-114">&amp;H4</span></span>  <br/> |<span data-ttu-id="0bfc9-115">この図形は移動しません。ただし他の図形をこの図形の上に配置できます。</span><span class="sxs-lookup"><span data-stu-id="0bfc9-115">Don't move this shape and allow shapes that plow to be placed on top of it.</span></span>  <br/> |<span data-ttu-id="0bfc9-116">**visSLOFixedPermeablePlow**</span><span class="sxs-lookup"><span data-stu-id="0bfc9-116">**visSLOFixedPermeablePlow**</span></span> <br/> |
|<span data-ttu-id="0bfc9-117">&amp;H20 (32)</span><span class="sxs-lookup"><span data-stu-id="0bfc9-117">&amp;H20 (32)</span></span>  <br/> |<span data-ttu-id="0bfc9-118">迂回するときに、接続ポイントの位置を無視します。</span><span class="sxs-lookup"><span data-stu-id="0bfc9-118">Ignore connection point locations when being routed to.</span></span>  <br/> |<span data-ttu-id="0bfc9-119">**visSLOFixedConnPtsIgnore**</span><span class="sxs-lookup"><span data-stu-id="0bfc9-119">**visSLOFixedConnPtsIgnore**</span></span> <br/> |
|<span data-ttu-id="0bfc9-120">&amp;H40 (64)</span><span class="sxs-lookup"><span data-stu-id="0bfc9-120">&amp;H40 (64)</span></span>  <br/> |<span data-ttu-id="0bfc9-121">接続ポイントがある側だけに迂回します。</span><span class="sxs-lookup"><span data-stu-id="0bfc9-121">Only allow routing to sides with connection points.</span></span>  <br/> |<span data-ttu-id="0bfc9-122">**visSLOFixedConnPtsOnly**</span><span class="sxs-lookup"><span data-stu-id="0bfc9-122">**visSLOFixedConnPtsOnly**</span></span> <br/> |
|<span data-ttu-id="0bfc9-123">&amp;H80 (128)</span><span class="sxs-lookup"><span data-stu-id="0bfc9-123">&amp;H80 (128)</span></span>  <br/> |<span data-ttu-id="0bfc9-p101">この図形の外周には接着しません。代わりに、図形の図形枠に接着します。</span><span class="sxs-lookup"><span data-stu-id="0bfc9-p101">Don't glue to the perimeter of this shape. Glue to the shape's alignment box instead.</span></span>  <br/> |<span data-ttu-id="0bfc9-126">**visSLOFixedNoFoldToShape**</span><span class="sxs-lookup"><span data-stu-id="0bfc9-126">**visSLOFixedNoFoldToShape**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0bfc9-127">注釈</span><span class="sxs-lookup"><span data-stu-id="0bfc9-127">Remarks</span></span>

<span data-ttu-id="0bfc9-128">**動作**] ダイアログ ボックスの [**配置**] タブで、このセルの値を設定することもできます (図形を選択して、[[開発](run-in-developer-mode-display-the-developer-tab.md)] タブの [**図形のデザイン**] で、[**動作**] をクリックし、[**配置**] タブをクリックして).</span><span class="sxs-lookup"><span data-stu-id="0bfc9-128">You can also set the value of this cell on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="0bfc9-129">このセルの値の任意の組み合わせを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="0bfc9-129">You can set any combination of these values for this cell.</span></span> <span data-ttu-id="0bfc9-130">値 3 を入力するたとえば、(&amp;H3)、**レイアウトの構成**] ダイアログ ボックスを使用して図形をレイアウトするときの動きを排除する ([**デザイン**] タブの [**レイアウト**] で、**ページの再レイアウト**] をクリックし、 **他のレイアウト オプション**) または図形の近くに他の配置可能な図形を配置するときとします。</span><span class="sxs-lookup"><span data-stu-id="0bfc9-130">For example, you can enter the value 3 (&amp;H3), which eliminates movement when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options** ) and when other placeable shapes are placed on or near the shape.</span></span> 
  
<span data-ttu-id="0bfc9-131">Visio 2000 より前のバージョンでは、[Miscellaneous] セクションで [ObjInteract] セルを使用してこの動作を設定していました。</span><span class="sxs-lookup"><span data-stu-id="0bfc9-131">In versions earlier than Visio 2000, you set this behavior using the ObjInteract cell in the Miscellaneous section.</span></span> 
  
<span data-ttu-id="0bfc9-132">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShapeFixedCode] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="0bfc9-132">To get a reference to the ShapeFixedCode cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0bfc9-133">セル名 :</span><span class="sxs-lookup"><span data-stu-id="0bfc9-133">Cell name:</span></span>  <br/> |<span data-ttu-id="0bfc9-134">ShapeFixedCode</span><span class="sxs-lookup"><span data-stu-id="0bfc9-134">ShapeFixedCode</span></span>  <br/> |
   
<span data-ttu-id="0bfc9-135">プログラムから、インデックスによって [ShapeFixedCode] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="0bfc9-135">To get a reference to the ShapeFixedCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0bfc9-136">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="0bfc9-136">Section index:</span></span>  <br/> |<span data-ttu-id="0bfc9-137">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0bfc9-137">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="0bfc9-138">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="0bfc9-138">Row index:</span></span>  <br/> |<span data-ttu-id="0bfc9-139">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="0bfc9-139">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="0bfc9-140">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="0bfc9-140">Cell index:</span></span>  <br/> |<span data-ttu-id="0bfc9-141">**visSLOFixedCode**</span><span class="sxs-lookup"><span data-stu-id="0bfc9-141">**visSLOFixedCode**</span></span> <br/> |
   

