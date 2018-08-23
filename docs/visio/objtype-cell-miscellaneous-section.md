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
description: '[レイアウトの構成] ダイアログ ボックスを使用して図形をレイアウトするときに、図面上のオブジェクトが配置可能かどうか、または迂回可能かどうかを指定します。'
ms.openlocfilehash: 23887e1d265e9e5ac1dfa9750bab65e8428b1c76
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805949"
---
# <a name="objtype-cell-miscellaneous-section"></a><span data-ttu-id="f4a92-103">[ObjType] セル ([その他] セクション)</span><span class="sxs-lookup"><span data-stu-id="f4a92-103">ObjType Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="f4a92-104">[**レイアウトの構成**] ダイアログ ボックスを使用して図形をレイアウトするときに、図面上のオブジェクトが配置可能かどうか、または迂回可能かどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="f4a92-104">Determines whether objects are placeable or routable in diagrams when you use the **Configure Layout** dialog box to lay out shapes.</span></span> 
  
|<span data-ttu-id="f4a92-105">**値**</span><span class="sxs-lookup"><span data-stu-id="f4a92-105">**Value**</span></span>|<span data-ttu-id="f4a92-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="f4a92-106">**Description**</span></span>|<span data-ttu-id="f4a92-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="f4a92-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f4a92-108">&amp;H0</span><span class="sxs-lookup"><span data-stu-id="f4a92-108">&amp;H0</span></span>  <br/> |<span data-ttu-id="f4a92-p101">既定値です。図面のコンテキストに基づいて決定されます。</span><span class="sxs-lookup"><span data-stu-id="f4a92-p101">Default. The application decides based on the drawing context.</span></span>  <br/> |<span data-ttu-id="f4a92-111">**visLOFlagsVisDecides**</span><span class="sxs-lookup"><span data-stu-id="f4a92-111">**visLOFlagsVisDecides**</span></span> <br/> |
|<span data-ttu-id="f4a92-112">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="f4a92-112">&amp;H1</span></span>  <br/> |<span data-ttu-id="f4a92-113">図形は配置可能です。</span><span class="sxs-lookup"><span data-stu-id="f4a92-113">Shape is placeable.</span></span>  <br/> |<span data-ttu-id="f4a92-114">**visLOFlagsPlacable**</span><span class="sxs-lookup"><span data-stu-id="f4a92-114">**visLOFlagsPlacable**</span></span> <br/> |
|<span data-ttu-id="f4a92-115">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="f4a92-115">&amp;H2</span></span>  <br/> |<span data-ttu-id="f4a92-p102">図形は迂回可能です。ただし 1 次元 (1-D) 図形でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="f4a92-p102">Shape is routable. Must be a one-dimensional (1-D) shape.</span></span>  <br/> |<span data-ttu-id="f4a92-118">**visLOFlagsRoutable**</span><span class="sxs-lookup"><span data-stu-id="f4a92-118">**visLOFlagsRoutable**</span></span> <br/> |
|<span data-ttu-id="f4a92-119">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="f4a92-119">&amp;H4</span></span>  <br/> |<span data-ttu-id="f4a92-120">図形は、配置も迂回もできません。</span><span class="sxs-lookup"><span data-stu-id="f4a92-120">Shape is not placeable, not routable.</span></span>  <br/> |<span data-ttu-id="f4a92-121">**visLOFlagsDont**</span><span class="sxs-lookup"><span data-stu-id="f4a92-121">**visLOFlagsDont**</span></span> <br/> |
|<span data-ttu-id="f4a92-122">&amp;H8</span><span class="sxs-lookup"><span data-stu-id="f4a92-122">&amp;H8</span></span>  <br/> |<span data-ttu-id="f4a92-123">グループには、配置可能/迂回可能な図形が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f4a92-123">Group contains placeable/routable shapes.</span></span>  <br/> |<span data-ttu-id="f4a92-124">**visLOFlagsPNRGroup**</span><span class="sxs-lookup"><span data-stu-id="f4a92-124">**visLOFlagsPNRGroup**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f4a92-125">注釈</span><span class="sxs-lookup"><span data-stu-id="f4a92-125">Remarks</span></span>

<span data-ttu-id="f4a92-p103">既定では、図形の [ObjType] セルは "No Formula" に設定されます。これは 0 と評価され、図形が配置可能かどうかはコンテキストに応じて決定されます。たとえば、単純な四角形を描画すると、[ObjType] セルの値は 0 になります。[**コネクタ**] ツールを使用して、この四角形を別の図形に接続すると、四角形の [ObjType] セルの値は 1 (配置可能) になります。</span><span class="sxs-lookup"><span data-stu-id="f4a92-p103">By default, the ObjType cell is set to No Formula for a shape, which evaluates to 0, meaning that the application determines whether the shape can be placeable depending on its context. For example, if you draw a simple rectangle, the value of its ObjType cell is 0. If you then use the **Connector** tool to connect the rectangle to another shape, Visio resets the value of the rectangle's ObjType cell to 1 (placeable).</span></span> 
  
<span data-ttu-id="f4a92-129">[Objtype] セルの値は、値の組み合わせにできます。</span><span class="sxs-lookup"><span data-stu-id="f4a92-129">The value of the ObjType cell can be a combination of values.</span></span> <span data-ttu-id="f4a92-130">配置可能ではないビットが設定されている場合 (&amp;H4)、ただし、それよりも優先グループの値を除くその他の値 (&amp;H8)。</span><span class="sxs-lookup"><span data-stu-id="f4a92-130">If the non-placeable bit is set (&amp;H4), however, it takes precedence over other values except the group value (&amp;H8).</span></span>
  
<span data-ttu-id="f4a92-131">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ObjType] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="f4a92-131">To get a reference to the ObjType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f4a92-132">セル名 :</span><span class="sxs-lookup"><span data-stu-id="f4a92-132">Cell name:</span></span>  <br/> |<span data-ttu-id="f4a92-133">[Objtype]</span><span class="sxs-lookup"><span data-stu-id="f4a92-133">ObjType</span></span>  <br/> |
   
<span data-ttu-id="f4a92-134">プログラムから、インデックスによって [ObjType] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="f4a92-134">To get a reference to the ObjType cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f4a92-135">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="f4a92-135">Section index:</span></span>  <br/> |<span data-ttu-id="f4a92-136">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f4a92-136">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="f4a92-137">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="f4a92-137">Row index:</span></span>  <br/> |<span data-ttu-id="f4a92-138">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="f4a92-138">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="f4a92-139">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="f4a92-139">Cell index:</span></span>  <br/> |<span data-ttu-id="f4a92-140">**visLOFlags**</span><span class="sxs-lookup"><span data-stu-id="f4a92-140">**visLOFlags**</span></span> <br/> |
   

