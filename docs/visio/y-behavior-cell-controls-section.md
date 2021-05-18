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
description: ハンドルの移動後にコントロール ハンドルの y 座標が表示される動作の種類を制御します。 次の数式を使用できます。
ms.openlocfilehash: bf8cbd490884244c92b68784dcbf041093539c94
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413578"
---
# <a name="y-behavior-cell-controls-section"></a><span data-ttu-id="f8a82-104">[Y Behavior] セル ([Controls] セクション)</span><span class="sxs-lookup"><span data-stu-id="f8a82-104">Y Behavior Cell (Controls Section)</span></span>

<span data-ttu-id="f8a82-105">ハンドルの移動後に  *コントロール ハンドルの y*  座標が表示される動作の種類を制御します。</span><span class="sxs-lookup"><span data-stu-id="f8a82-105">Controls the type of behavior the  *y*  -coordinate of the control handle will exhibit after the handle is moved.</span></span> <span data-ttu-id="f8a82-106">次の数式を使用できます。</span><span class="sxs-lookup"><span data-stu-id="f8a82-106">These formulas are available.</span></span> 
  
|<span data-ttu-id="f8a82-107">**値**</span><span class="sxs-lookup"><span data-stu-id="f8a82-107">**Value**</span></span>|<span data-ttu-id="f8a82-108">**動作**</span><span class="sxs-lookup"><span data-stu-id="f8a82-108">**Behavior**</span></span>|<span data-ttu-id="f8a82-109">**定義**</span><span class="sxs-lookup"><span data-stu-id="f8a82-109">**Definition**</span></span>|<span data-ttu-id="f8a82-110">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="f8a82-110">**Automation constant**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f8a82-111">0</span><span class="sxs-lookup"><span data-stu-id="f8a82-111">0</span></span>  <br/> | <span data-ttu-id="f8a82-112">プロポーショナル</span><span class="sxs-lookup"><span data-stu-id="f8a82-112">Proportional</span></span>  <br/> | <span data-ttu-id="f8a82-113"> 
          コントロール ハンドルを移動できます。また図形を引き伸ばすと、図形に比例して移動します。
        </span><span class="sxs-lookup"><span data-stu-id="f8a82-113">The control handle can be moved, and it also moves in proportion with the shape when it is stretched.</span></span>  <br/> |<span data-ttu-id="f8a82-114">**visCtlProportional**</span><span class="sxs-lookup"><span data-stu-id="f8a82-114">**visCtlProportional**</span></span> <br/> |
| <span data-ttu-id="f8a82-115">1</span><span class="sxs-lookup"><span data-stu-id="f8a82-115">1</span></span>  <br/> | <span data-ttu-id="f8a82-116">プロポーショナル (ロック)</span><span class="sxs-lookup"><span data-stu-id="f8a82-116">Proportional locked</span></span>  <br/> | <span data-ttu-id="f8a82-117">コントロール ハンドルは図形に比例して移動しますが、コントロール ハンドル自体は移動できません。</span><span class="sxs-lookup"><span data-stu-id="f8a82-117">The control handle moves in proportion with the shape, but the control handle itself cannot be moved.</span></span>  <br/> |<span data-ttu-id="f8a82-118">**visCtlLocked**</span><span class="sxs-lookup"><span data-stu-id="f8a82-118">**visCtlLocked**</span></span> <br/> |
| <span data-ttu-id="f8a82-119">2</span><span class="sxs-lookup"><span data-stu-id="f8a82-119">2</span></span>  <br/> | <span data-ttu-id="f8a82-120">下端からオフセット</span><span class="sxs-lookup"><span data-stu-id="f8a82-120">Offset from bottom edge</span></span>  <br/> | <span data-ttu-id="f8a82-121">コントロール ハンドルは、図形の底部から一定の距離だけオフセットされます。</span><span class="sxs-lookup"><span data-stu-id="f8a82-121">The control handle is offset a constant distance from the bottom of the shape.</span></span>  <br/> |<span data-ttu-id="f8a82-122">**visCtlOffsetMin**</span><span class="sxs-lookup"><span data-stu-id="f8a82-122">**visCtlOffsetMin**</span></span> <br/> |
| <span data-ttu-id="f8a82-123">3</span><span class="sxs-lookup"><span data-stu-id="f8a82-123">3</span></span>  <br/> | <span data-ttu-id="f8a82-124">中心からオフセット</span><span class="sxs-lookup"><span data-stu-id="f8a82-124">Offset from center</span></span>  <br/> | <span data-ttu-id="f8a82-125">コントロール ハンドルは、図形の中心から一定の距離だけオフセットされます。</span><span class="sxs-lookup"><span data-stu-id="f8a82-125">The control handle is offset a constant distance from the center of the shape.</span></span>  <br/> |<span data-ttu-id="f8a82-126">**visCtlOffsetMid**</span><span class="sxs-lookup"><span data-stu-id="f8a82-126">**visCtlOffsetMid**</span></span> <br/> |
| <span data-ttu-id="f8a82-127">4</span><span class="sxs-lookup"><span data-stu-id="f8a82-127">4</span></span>  <br/> | <span data-ttu-id="f8a82-128">上端からオフセット</span><span class="sxs-lookup"><span data-stu-id="f8a82-128">Offset from top edge</span></span>  <br/> | <span data-ttu-id="f8a82-129">コントロール ハンドルは、図形の上部から一定の距離だけオフセットされます。</span><span class="sxs-lookup"><span data-stu-id="f8a82-129">The control handle is offset a constant distance from the top of the shape.</span></span>  <br/> |<span data-ttu-id="f8a82-130">**visCtlOffsetMax**</span><span class="sxs-lookup"><span data-stu-id="f8a82-130">**visCtlOffsetMax**</span></span> <br/> |
| <span data-ttu-id="f8a82-131">5</span><span class="sxs-lookup"><span data-stu-id="f8a82-131">5</span></span>  <br/> | <span data-ttu-id="f8a82-132">プロポーショナル (非表示)</span><span class="sxs-lookup"><span data-stu-id="f8a82-132">Proportional, hidden</span></span>  <br/> | <span data-ttu-id="f8a82-133">0 と同じですが、コントロール ハンドルは表示されません。</span><span class="sxs-lookup"><span data-stu-id="f8a82-133">Same as 0, but the control handle is not visible.</span></span>  <br/> |<span data-ttu-id="f8a82-134">**visCtlProportionalHidden**</span><span class="sxs-lookup"><span data-stu-id="f8a82-134">**visCtlProportionalHidden**</span></span> <br/> |
| <span data-ttu-id="f8a82-135">6</span><span class="sxs-lookup"><span data-stu-id="f8a82-135">6</span></span>  <br/> | <span data-ttu-id="f8a82-136">プロポーショナル (ロック、非表示)</span><span class="sxs-lookup"><span data-stu-id="f8a82-136">Proportional locked, hidden</span></span>  <br/> | <span data-ttu-id="f8a82-137">1 と同じですが、コントロール ハンドルは表示されません。</span><span class="sxs-lookup"><span data-stu-id="f8a82-137">Same as 1, but the control handle is not visible.</span></span>  <br/> |<span data-ttu-id="f8a82-138">**visCtlLockedHiddenv**</span><span class="sxs-lookup"><span data-stu-id="f8a82-138">**visCtlLockedHiddenv**</span></span> <br/> |
| <span data-ttu-id="f8a82-139">7</span><span class="sxs-lookup"><span data-stu-id="f8a82-139">7</span></span>  <br/> | <span data-ttu-id="f8a82-140">左端からオフセット (非表示)</span><span class="sxs-lookup"><span data-stu-id="f8a82-140">Offset from left edge, hidden</span></span>  <br/> | <span data-ttu-id="f8a82-141">2 と同じですが、コントロール ハンドルは表示されません。</span><span class="sxs-lookup"><span data-stu-id="f8a82-141">Same as 2, but the control handle is not visible.</span></span>  <br/> |<span data-ttu-id="f8a82-142">**visCtlOffsetMinHidden**</span><span class="sxs-lookup"><span data-stu-id="f8a82-142">**visCtlOffsetMinHidden**</span></span> <br/> |
| <span data-ttu-id="f8a82-143">8</span><span class="sxs-lookup"><span data-stu-id="f8a82-143">8</span></span>  <br/> | <span data-ttu-id="f8a82-144">中心からオフセット (非表示)</span><span class="sxs-lookup"><span data-stu-id="f8a82-144">Offset from center, hidden</span></span>  <br/> | <span data-ttu-id="f8a82-145">3 と同じですが、コントロール ハンドルは表示されません。</span><span class="sxs-lookup"><span data-stu-id="f8a82-145">Same as 3, but the control handle is not visible.</span></span>  <br/> |<span data-ttu-id="f8a82-146">**visCtlOffsetMidHidden**</span><span class="sxs-lookup"><span data-stu-id="f8a82-146">**visCtlOffsetMidHidden**</span></span> <br/> |
| <span data-ttu-id="f8a82-147">9</span><span class="sxs-lookup"><span data-stu-id="f8a82-147">9</span></span>  <br/> | <span data-ttu-id="f8a82-148">右端からオフセット (非表示)</span><span class="sxs-lookup"><span data-stu-id="f8a82-148">Offset from right edge, hidden</span></span>  <br/> | <span data-ttu-id="f8a82-149">4 と同じですが、コントロール ハンドルは表示されません。</span><span class="sxs-lookup"><span data-stu-id="f8a82-149">Same as 4, but the control handle is not visible.</span></span>  <br/> |<span data-ttu-id="f8a82-150">**visCtlOffsetMaxHidden**</span><span class="sxs-lookup"><span data-stu-id="f8a82-150">**visCtlOffsetMaxHidden**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f8a82-151">注釈</span><span class="sxs-lookup"><span data-stu-id="f8a82-151">Remarks</span></span>

<span data-ttu-id="f8a82-152">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Y Behavior] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="f8a82-152">To get a reference to the Y Behavior cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f8a82-153">セル名:</span><span class="sxs-lookup"><span data-stu-id="f8a82-153">Cell name:</span></span>  <br/> | <span data-ttu-id="f8a82-154">コントロール。</span><span class="sxs-lookup"><span data-stu-id="f8a82-154">Controls.</span></span>  <span data-ttu-id="f8a82-155">*name*  .YConwhere コントロール。</span><span class="sxs-lookup"><span data-stu-id="f8a82-155">*name*  .YConwhere Controls.</span></span>  <span data-ttu-id="f8a82-156">*name*  は、コントロール行の名前です。</span><span class="sxs-lookup"><span data-stu-id="f8a82-156">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="f8a82-157">プログラムから、インデックスによって [Y Behavior] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="f8a82-157">To get a reference to the Y Behavior cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f8a82-158">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="f8a82-158">Section index:</span></span>  <br/> |<span data-ttu-id="f8a82-159">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="f8a82-159">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="f8a82-160">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="f8a82-160">Row index:</span></span>  <br/> |<span data-ttu-id="f8a82-161">**visRowControl**  +  *i* *=* 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="f8a82-161">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="f8a82-162">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="f8a82-162">Cell index:</span></span>  <br/> |<span data-ttu-id="f8a82-163">**visCtlYCon**</span><span class="sxs-lookup"><span data-stu-id="f8a82-163">**visCtlYCon**</span></span> <br/> |
   

