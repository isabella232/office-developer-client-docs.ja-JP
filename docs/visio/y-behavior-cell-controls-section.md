---
title: '[Y Behavior] セル ([Controls] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1190
localization_priority: Normal
ms.assetid: 6d5062d3-743b-8664-8ec9-5a8f11d5edf9
description: Y の動作の種類を制御・ コントロール ハンドルの座標は、ハンドルを移動した後が発生します。 これらの数式を利用できます。
ms.openlocfilehash: ee2a5e28748df603635f64c080119e28569f576a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806828"
---
# <a name="y-behavior-cell-controls-section"></a><span data-ttu-id="7c5a1-104">[Y Behavior] セル ([コントロール] セクション)</span><span class="sxs-lookup"><span data-stu-id="7c5a1-104">Y Behavior Cell (Controls Section)</span></span>

<span data-ttu-id="7c5a1-105">*Y*の動作の種類を制御・ コントロール ハンドルの座標は、ハンドルを移動した後が発生します。</span><span class="sxs-lookup"><span data-stu-id="7c5a1-105">Controls the type of behavior the  *y*  -coordinate of the control handle will exhibit after the handle is moved.</span></span> <span data-ttu-id="7c5a1-106">これらの数式を利用できます。</span><span class="sxs-lookup"><span data-stu-id="7c5a1-106">These formulas are available.</span></span> 
  
|<span data-ttu-id="7c5a1-107">**値**</span><span class="sxs-lookup"><span data-stu-id="7c5a1-107">**Value**</span></span>|<span data-ttu-id="7c5a1-108">**動作**</span><span class="sxs-lookup"><span data-stu-id="7c5a1-108">**Behavior**</span></span>|<span data-ttu-id="7c5a1-109">**定義**</span><span class="sxs-lookup"><span data-stu-id="7c5a1-109">**Definition**</span></span>|<span data-ttu-id="7c5a1-110">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="7c5a1-110">**Automation constant**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="7c5a1-111">0</span><span class="sxs-lookup"><span data-stu-id="7c5a1-111">0</span></span>  <br/> | <span data-ttu-id="7c5a1-112"> 
          プロポーショナル 
        </span><span class="sxs-lookup"><span data-stu-id="7c5a1-112">Proportional</span></span>  <br/> | <span data-ttu-id="7c5a1-113"> 
          コントロール ハンドルを移動できます。また図形を引き伸ばすと、図形に比例して移動します。
        </span><span class="sxs-lookup"><span data-stu-id="7c5a1-113">The control handle can be moved, and it also moves in proportion with the shape when it is stretched.</span></span>  <br/> |<span data-ttu-id="7c5a1-114">**visCtlProportional**</span><span class="sxs-lookup"><span data-stu-id="7c5a1-114">**visCtlProportional**</span></span> <br/> |
| <span data-ttu-id="7c5a1-115">1</span><span class="sxs-lookup"><span data-stu-id="7c5a1-115">1</span></span>  <br/> | <span data-ttu-id="7c5a1-116"> 
          プロポーショナル (ロック) 
        </span><span class="sxs-lookup"><span data-stu-id="7c5a1-116">Proportional locked</span></span>  <br/> | <span data-ttu-id="7c5a1-117">コントロール ハンドル、図形では、比例して移動しますが、コントロール ハンドル自体は移動できません。</span><span class="sxs-lookup"><span data-stu-id="7c5a1-117">The control handle moves in proportion with the shape, but the control handle itself cannot be moved.</span></span>  <br/> |<span data-ttu-id="7c5a1-118">**visCtlLocked**</span><span class="sxs-lookup"><span data-stu-id="7c5a1-118">**visCtlLocked**</span></span> <br/> |
| <span data-ttu-id="7c5a1-119">2</span><span class="sxs-lookup"><span data-stu-id="7c5a1-119">2</span></span>  <br/> | <span data-ttu-id="7c5a1-120"> 
          下端からオフセット 
        </span><span class="sxs-lookup"><span data-stu-id="7c5a1-120">Offset from bottom edge</span></span>  <br/> | <span data-ttu-id="7c5a1-121"> 
          コントロール ハンドルは、図形の底部から一定の距離だけオフセットされます。 
        </span><span class="sxs-lookup"><span data-stu-id="7c5a1-121">The control handle is offset a constant distance from the bottom of the shape.</span></span>  <br/> |<span data-ttu-id="7c5a1-122">**visCtlOffsetMin**</span><span class="sxs-lookup"><span data-stu-id="7c5a1-122">**visCtlOffsetMin**</span></span> <br/> |
| <span data-ttu-id="7c5a1-123">3</span><span class="sxs-lookup"><span data-stu-id="7c5a1-123">3</span></span>  <br/> | <span data-ttu-id="7c5a1-124"> 
          中心からオフセット 
        </span><span class="sxs-lookup"><span data-stu-id="7c5a1-124">Offset from center</span></span>  <br/> | <span data-ttu-id="7c5a1-125"> 
          コントロール ハンドルは、図形の中心から一定の距離だけオフセットされます。
        </span><span class="sxs-lookup"><span data-stu-id="7c5a1-125">The control handle is offset a constant distance from the center of the shape.</span></span>  <br/> |<span data-ttu-id="7c5a1-126">**visCtlOffsetMid**</span><span class="sxs-lookup"><span data-stu-id="7c5a1-126">**visCtlOffsetMid**</span></span> <br/> |
| <span data-ttu-id="7c5a1-127">4</span><span class="sxs-lookup"><span data-stu-id="7c5a1-127">4</span></span>  <br/> | <span data-ttu-id="7c5a1-128"> 
          上端からオフセット 
        </span><span class="sxs-lookup"><span data-stu-id="7c5a1-128">Offset from top edge</span></span>  <br/> | <span data-ttu-id="7c5a1-129"> 
          コントロール ハンドルは、図形の上部から一定の距離だけオフセットされます。 
        </span><span class="sxs-lookup"><span data-stu-id="7c5a1-129">The control handle is offset a constant distance from the top of the shape.</span></span>  <br/> |<span data-ttu-id="7c5a1-130">**visCtlOffsetMax**</span><span class="sxs-lookup"><span data-stu-id="7c5a1-130">**visCtlOffsetMax**</span></span> <br/> |
| <span data-ttu-id="7c5a1-131">5</span><span class="sxs-lookup"><span data-stu-id="7c5a1-131">5</span></span>  <br/> | <span data-ttu-id="7c5a1-132"> 
          プロポーショナル (非表示) 
        </span><span class="sxs-lookup"><span data-stu-id="7c5a1-132">Proportional, hidden</span></span>  <br/> | <span data-ttu-id="7c5a1-133"> 
          0 と同じですが、コントロール ハンドルは表示されません。 
        </span><span class="sxs-lookup"><span data-stu-id="7c5a1-133">Same as 0, but the control handle is not visible.</span></span>  <br/> |<span data-ttu-id="7c5a1-134">**visCtlProportionalHidden**</span><span class="sxs-lookup"><span data-stu-id="7c5a1-134">**visCtlProportionalHidden**</span></span> <br/> |
| <span data-ttu-id="7c5a1-135">6</span><span class="sxs-lookup"><span data-stu-id="7c5a1-135">6</span></span>  <br/> | <span data-ttu-id="7c5a1-136"> 
          プロポーショナル (ロック、非表示) 
        </span><span class="sxs-lookup"><span data-stu-id="7c5a1-136">Proportional locked, hidden</span></span>  <br/> | <span data-ttu-id="7c5a1-137"> 
          1 と同じですが、コントロール ハンドルは表示されません。 
        </span><span class="sxs-lookup"><span data-stu-id="7c5a1-137">Same as 1, but the control handle is not visible.</span></span>  <br/> |<span data-ttu-id="7c5a1-138">**visCtlLockedHiddenv**</span><span class="sxs-lookup"><span data-stu-id="7c5a1-138">**visCtlLockedHiddenv**</span></span> <br/> |
| <span data-ttu-id="7c5a1-139">7</span><span class="sxs-lookup"><span data-stu-id="7c5a1-139">7</span></span>  <br/> | <span data-ttu-id="7c5a1-140"> 
          左端からオフセット (非表示) 
        </span><span class="sxs-lookup"><span data-stu-id="7c5a1-140">Offset from left edge, hidden</span></span>  <br/> | <span data-ttu-id="7c5a1-141"> 
          2 と同じですが、コントロール ハンドルは表示されません。 
        </span><span class="sxs-lookup"><span data-stu-id="7c5a1-141">Same as 2, but the control handle is not visible.</span></span>  <br/> |<span data-ttu-id="7c5a1-142">**visCtlOffsetMinHidden**</span><span class="sxs-lookup"><span data-stu-id="7c5a1-142">**visCtlOffsetMinHidden**</span></span> <br/> |
| <span data-ttu-id="7c5a1-143">8</span><span class="sxs-lookup"><span data-stu-id="7c5a1-143">8</span></span>  <br/> | <span data-ttu-id="7c5a1-144"> 
          中心からオフセット (非表示) 
        </span><span class="sxs-lookup"><span data-stu-id="7c5a1-144">Offset from center, hidden</span></span>  <br/> | <span data-ttu-id="7c5a1-145"> 
          3 と同じですが、コントロール ハンドルは表示されません。 
        </span><span class="sxs-lookup"><span data-stu-id="7c5a1-145">Same as 3, but the control handle is not visible.</span></span>  <br/> |<span data-ttu-id="7c5a1-146">**visCtlOffsetMidHidden**</span><span class="sxs-lookup"><span data-stu-id="7c5a1-146">**visCtlOffsetMidHidden**</span></span> <br/> |
| <span data-ttu-id="7c5a1-147">9</span><span class="sxs-lookup"><span data-stu-id="7c5a1-147">9</span></span>  <br/> | <span data-ttu-id="7c5a1-148"> 
          右端からオフセット (非表示) 
        </span><span class="sxs-lookup"><span data-stu-id="7c5a1-148">Offset from right edge, hidden</span></span>  <br/> | <span data-ttu-id="7c5a1-149"> 
          4 と同じですが、コントロール ハンドルは表示されません。 
        </span><span class="sxs-lookup"><span data-stu-id="7c5a1-149">Same as 4, but the control handle is not visible.</span></span>  <br/> |<span data-ttu-id="7c5a1-150">**visCtlOffsetMaxHidden**</span><span class="sxs-lookup"><span data-stu-id="7c5a1-150">**visCtlOffsetMaxHidden**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7c5a1-151">注釈</span><span class="sxs-lookup"><span data-stu-id="7c5a1-151">Remarks</span></span>

<span data-ttu-id="7c5a1-152">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Y Behavior] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="7c5a1-152">To get a reference to the Y Behavior cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7c5a1-153">セル名:</span><span class="sxs-lookup"><span data-stu-id="7c5a1-153">Cell name:</span></span>  <br/> | <span data-ttu-id="7c5a1-154">制御します。</span><span class="sxs-lookup"><span data-stu-id="7c5a1-154">Controls.</span></span>  <span data-ttu-id="7c5a1-155">*名*です。YConwhere を制御します。</span><span class="sxs-lookup"><span data-stu-id="7c5a1-155">*name*  .YConwhere Controls.</span></span>  <span data-ttu-id="7c5a1-156">*名*は、コントロールの行の名前です。</span><span class="sxs-lookup"><span data-stu-id="7c5a1-156">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="7c5a1-157">プログラムから、インデックスによって [Y Behavior] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="7c5a1-157">To get a reference to the Y Behavior cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7c5a1-158">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="7c5a1-158">Section index:</span></span>  <br/> |<span data-ttu-id="7c5a1-159">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="7c5a1-159">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="7c5a1-160">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="7c5a1-160">Row index:</span></span>  <br/> |<span data-ttu-id="7c5a1-161">**visRowControl** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="7c5a1-161">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="7c5a1-162">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="7c5a1-162">Cell index:</span></span>  <br/> |<span data-ttu-id="7c5a1-163">**visCtlYCon**</span><span class="sxs-lookup"><span data-stu-id="7c5a1-163">**visCtlYCon**</span></span> <br/> |
   

