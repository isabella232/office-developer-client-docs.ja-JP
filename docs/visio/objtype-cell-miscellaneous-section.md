---
title: '[ObjType] セル ([Miscellaneous] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm745
localization_priority: Normal
ms.assetid: 3afee07b-e91a-a91c-fba2-0e3251dd6385
description: オブジェクトを判断するかどうか配置可能なまたは図でルーティング可能な図形をレイアウトするのには、[レイアウトの構成] ダイアログ ボックスを使用するとします。
ms.openlocfilehash: 23887e1d265e9e5ac1dfa9750bab65e8428b1c76
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805949"
---
# <a name="objtype-cell-miscellaneous-section"></a><span data-ttu-id="61282-103">[ObjType] セル ([Miscellaneous] セクション)</span><span class="sxs-lookup"><span data-stu-id="61282-103">ObjType Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="61282-104">オブジェクトを判断するかどうか配置可能なまたは図でルーティング可能な図形をレイアウトするのには、[**レイアウトの構成**] ダイアログ ボックスを使用するとします。</span><span class="sxs-lookup"><span data-stu-id="61282-104">Determines whether objects are placeable or routable in diagrams when you use the **Configure Layout** dialog box to lay out shapes.</span></span> 
  
|<span data-ttu-id="61282-105">**値**</span><span class="sxs-lookup"><span data-stu-id="61282-105">**Value**</span></span>|<span data-ttu-id="61282-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="61282-106">**Description**</span></span>|<span data-ttu-id="61282-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="61282-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="61282-108">&amp;H0</span><span class="sxs-lookup"><span data-stu-id="61282-108">&amp;H0</span></span>  <br/> |<span data-ttu-id="61282-p101">既定値です。図面のコンテキストに基づいて決定されます。</span><span class="sxs-lookup"><span data-stu-id="61282-p101">Default. The application decides based on the drawing context.</span></span>  <br/> |<span data-ttu-id="61282-111">**visLOFlagsVisDecides**</span><span class="sxs-lookup"><span data-stu-id="61282-111">**visLOFlagsVisDecides**</span></span> <br/> |
|<span data-ttu-id="61282-112">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="61282-112">&amp;H1</span></span>  <br/> |<span data-ttu-id="61282-113">図形は配置可能です。</span><span class="sxs-lookup"><span data-stu-id="61282-113">Shape is placeable.</span></span>  <br/> |<span data-ttu-id="61282-114">**visLOFlagsPlacable**</span><span class="sxs-lookup"><span data-stu-id="61282-114">**visLOFlagsPlacable**</span></span> <br/> |
|<span data-ttu-id="61282-115">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="61282-115">&amp;H2</span></span>  <br/> |<span data-ttu-id="61282-p102">図形は迂回可能です。ただし 1 次元 (1-D) 図形でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="61282-p102">Shape is routable. Must be a one-dimensional (1-D) shape.</span></span>  <br/> |<span data-ttu-id="61282-118">**visLOFlagsRoutable**</span><span class="sxs-lookup"><span data-stu-id="61282-118">**visLOFlagsRoutable**</span></span> <br/> |
|<span data-ttu-id="61282-119">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="61282-119">&amp;H4</span></span>  <br/> |<span data-ttu-id="61282-120">図形は、配置も迂回もできません。</span><span class="sxs-lookup"><span data-stu-id="61282-120">Shape is not placeable, not routable.</span></span>  <br/> |<span data-ttu-id="61282-121">**visLOFlagsDont**</span><span class="sxs-lookup"><span data-stu-id="61282-121">**visLOFlagsDont**</span></span> <br/> |
|<span data-ttu-id="61282-122">&amp;H8</span><span class="sxs-lookup"><span data-stu-id="61282-122">&amp;H8</span></span>  <br/> |<span data-ttu-id="61282-123">グループには、配置可能/迂回可能な図形が含まれます。</span><span class="sxs-lookup"><span data-stu-id="61282-123">Group contains placeable/routable shapes.</span></span>  <br/> |<span data-ttu-id="61282-124">**visLOFlagsPNRGroup**</span><span class="sxs-lookup"><span data-stu-id="61282-124">**visLOFlagsPNRGroup**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="61282-125">備考</span><span class="sxs-lookup"><span data-stu-id="61282-125">Remarks</span></span>

<span data-ttu-id="61282-126">既定では、なしの数式を 0 に評価されると、図形、図形のコンテキストに応じて配置できるかどうかをアプリケーションが決定されることを意味する [objtype] セルを設定します。</span><span class="sxs-lookup"><span data-stu-id="61282-126">By default, the ObjType cell is set to No Formula for a shape, which evaluates to 0, meaning that the application determines whether the shape can be placeable depending on its context.</span></span> <span data-ttu-id="61282-127">単純な四角形を描画する場合、[objtype] セルの値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="61282-127">For example, if you draw a simple rectangle, the value of its ObjType cell is 0.</span></span> <span data-ttu-id="61282-128">四角形を別の図形に接続する**コネクタ**ツールを使用する場合、Visio は 1 (配置可能) に四角形の [objtype] セルの値をリセットします。</span><span class="sxs-lookup"><span data-stu-id="61282-128">If you then use the **Connector** tool to connect the rectangle to another shape, Visio resets the value of the rectangle's ObjType cell to 1 (placeable).</span></span> 
  
<span data-ttu-id="61282-129">[Objtype] セルの値は、値の組み合わせにできます。</span><span class="sxs-lookup"><span data-stu-id="61282-129">The value of the ObjType cell can be a combination of values.</span></span> <span data-ttu-id="61282-130">配置可能ではないビットが設定されている場合 (&amp;H4)、ただし、それよりも優先グループの値を除くその他の値 (&amp;H8)。</span><span class="sxs-lookup"><span data-stu-id="61282-130">If the non-placeable bit is set (&amp;H4), however, it takes precedence over other values except the group value (&amp;H8).</span></span>
  
<span data-ttu-id="61282-131">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [objtype] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="61282-131">To get a reference to the ObjType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="61282-132">セル名 :</span><span class="sxs-lookup"><span data-stu-id="61282-132">Cell name:</span></span>  <br/> |<span data-ttu-id="61282-133">[Objtype]</span><span class="sxs-lookup"><span data-stu-id="61282-133">ObjType</span></span>  <br/> |
   
<span data-ttu-id="61282-134">プログラムから、インデックスによって [objtype] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="61282-134">To get a reference to the ObjType cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="61282-135">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="61282-135">Section index:</span></span>  <br/> |<span data-ttu-id="61282-136">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="61282-136">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="61282-137">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="61282-137">Row index:</span></span>  <br/> |<span data-ttu-id="61282-138">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="61282-138">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="61282-139">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="61282-139">Cell index:</span></span>  <br/> |<span data-ttu-id="61282-140">**visLOFlags**</span><span class="sxs-lookup"><span data-stu-id="61282-140">**visLOFlags**</span></span> <br/> |
   

