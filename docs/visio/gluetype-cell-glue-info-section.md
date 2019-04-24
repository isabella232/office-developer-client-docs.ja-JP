---
title: '[GlueType] セル ([Glue Info] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm420
localization_priority: Normal
ms.assetid: fffbefd6-8b0b-0023-6b03-026d1c6e885e
description: 1-D 図形を別の図形に接着するときに静的接着 (点から点) と動的接着 (図形から図形) のどちらを使用するかを指定します。
ms.openlocfilehash: ae4eddf17c6e7b5e56cb3397f03d0721d965c9b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339516"
---
# <a name="gluetype-cell-glue-info-section"></a><span data-ttu-id="f51b1-103">[GlueType] セル ([Glue Info] セクション)</span><span class="sxs-lookup"><span data-stu-id="f51b1-103">GlueType Cell (Glue Info Section)</span></span>

<span data-ttu-id="f51b1-104">1-D 図形を別の図形に接着するときに静的接着 (点から点) と動的接着 (図形から図形) のどちらを使用するかを指定します。</span><span class="sxs-lookup"><span data-stu-id="f51b1-104">Determines whether a 1-D shape uses static (point-to-point) or dynamic (shape-to-shape) glue when it is glued to another shape.</span></span>
  
|<span data-ttu-id="f51b1-105">**値**</span><span class="sxs-lookup"><span data-stu-id="f51b1-105">**Value**</span></span>|<span data-ttu-id="f51b1-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="f51b1-106">**Description**</span></span>|<span data-ttu-id="f51b1-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="f51b1-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="f51b1-108">&amp;H0</span><span class="sxs-lookup"><span data-stu-id="f51b1-108">&amp;H0</span></span>  <br/> | <span data-ttu-id="f51b1-p101">既定値です。動的コネクタの場合にだけ動的接着を使用します。それ以外の場合は静的接着を使用します。</span><span class="sxs-lookup"><span data-stu-id="f51b1-p101">Default. Allow dynamic glue for the dynamic connector only; otherwise, use static glue.</span></span>  <br/> |<span data-ttu-id="f51b1-111">**visGlueTypeDefault**</span><span class="sxs-lookup"><span data-stu-id="f51b1-111">**visGlueTypeDefault**</span></span> <br/> |
| <span data-ttu-id="f51b1-112">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="f51b1-112">&amp;H1</span></span>  <br/> | <span data-ttu-id="f51b1-113">動的接着を使用します。</span><span class="sxs-lookup"><span data-stu-id="f51b1-113">Allow dynamic glue.</span></span>  <br/> | <span data-ttu-id="f51b1-114">Visio 2002 で廃止されました。</span><span class="sxs-lookup"><span data-stu-id="f51b1-114">Obsolete in Visio 2002</span></span>  <br/> |
| <span data-ttu-id="f51b1-115">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="f51b1-115">&amp;H2</span></span>  <br/> | <span data-ttu-id="f51b1-116">動的接着を使用します。</span><span class="sxs-lookup"><span data-stu-id="f51b1-116">Allow dynamic glue.</span></span>  <br/> |<span data-ttu-id="f51b1-117">**visGlueTypeWalking**</span><span class="sxs-lookup"><span data-stu-id="f51b1-117">**visGlueTypeWalking**</span></span> <br/> |
| <span data-ttu-id="f51b1-118">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="f51b1-118">&amp;H4</span></span>  <br/> | <span data-ttu-id="f51b1-119">動的接着を使用しません。</span><span class="sxs-lookup"><span data-stu-id="f51b1-119">Do not allow dynamic glue.</span></span>  <br/> |<span data-ttu-id="f51b1-120">**visGlueTypeNoWalking**</span><span class="sxs-lookup"><span data-stu-id="f51b1-120">**visGlueTypeNoWalking**</span></span> <br/> |
| <span data-ttu-id="f51b1-121">&amp;H8</span><span class="sxs-lookup"><span data-stu-id="f51b1-121">&amp;H8</span></span>  <br/> | <span data-ttu-id="f51b1-122">この 2-D 図形に対しては、動的接着による接続はできません。</span><span class="sxs-lookup"><span data-stu-id="f51b1-122">Do not allow this 2-D shape to be connected to with dynamic glue.</span></span>  <br/> |<span data-ttu-id="f51b1-123">**visGlueTypeNoWalkingTo**</span><span class="sxs-lookup"><span data-stu-id="f51b1-123">**visGlueTypeNoWalkingTo**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f51b1-124">解説</span><span class="sxs-lookup"><span data-stu-id="f51b1-124">Remarks</span></span>

<span data-ttu-id="f51b1-125">このセルの値が 1、2、または 3 の場合、次の操作のいずれかが行われたときに動的接着が使用されます。</span><span class="sxs-lookup"><span data-stu-id="f51b1-125">If this cell contains a value of 1, 2 or 3, dynamic glue will be established when either of the following occurs:</span></span>
  
- <span data-ttu-id="f51b1-126">ユーザー インターフェイスを使用して図形が動的に接着される。</span><span class="sxs-lookup"><span data-stu-id="f51b1-126">Shapes are dynamically glued in the user interface.</span></span>
    
- <span data-ttu-id="f51b1-127">プログラムを使用して別の図形の [PinX] セルまたは [PinY] セルに図形が接着される。</span><span class="sxs-lookup"><span data-stu-id="f51b1-127">Shapes are glued to the PinX or PinY cell of another shape from a program.</span></span>
    
<span data-ttu-id="f51b1-128">プログラムによって [PinX] または [PinY] 以外のセルに図形が接着される場合は、静的接着が使用されます。</span><span class="sxs-lookup"><span data-stu-id="f51b1-128">If shapes are glued to shape cells other than PinX or PinY from a program, then static glue is used.</span></span>
  
<span data-ttu-id="f51b1-p102">この値を、動的接着を許可するものから禁止するものに変更しても、既存の動的接着が切り離されたり、変更されることはありません。[GlueType] セルで動的接着が無効になっている場合でも、プログラムからは動的接着を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="f51b1-p102">Changing this value from allowing to not allowing dynamic glue does not sever or change existing dynamic glue. Programs can establish dynamic glue even if dynamic glue is disabled in the GlueType cell.</span></span>
  
<span data-ttu-id="f51b1-131">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [GlueType] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="f51b1-131">To get a reference to the GlueType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f51b1-132">セル名:</span><span class="sxs-lookup"><span data-stu-id="f51b1-132">Cell name:</span></span>  <br/> | <span data-ttu-id="f51b1-133">[gluetype]</span><span class="sxs-lookup"><span data-stu-id="f51b1-133">GlueType</span></span>  <br/> |
   
<span data-ttu-id="f51b1-134">プログラムから、インデックスによって [GlueType] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="f51b1-134">To get a reference to the GlueType cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f51b1-135">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="f51b1-135">Section index:</span></span>  <br/> |<span data-ttu-id="f51b1-136">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f51b1-136">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f51b1-137">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="f51b1-137">Row index:</span></span>  <br/> |<span data-ttu-id="f51b1-138">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="f51b1-138">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="f51b1-139">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="f51b1-139">Cell index:</span></span>  <br/> |<span data-ttu-id="f51b1-140">**visGlueType**</span><span class="sxs-lookup"><span data-stu-id="f51b1-140">**visGlueType**</span></span> <br/> |
   

