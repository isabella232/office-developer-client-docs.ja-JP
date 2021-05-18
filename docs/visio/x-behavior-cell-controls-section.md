---
title: '[X Behavior] セル ([Controls] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251285
localization_priority: Normal
ms.assetid: 82423d08-b6ce-0f23-8b61-354c3e5f323e
description: ハンドルの移動後にコントロール ハンドルの x 座標が表示される動作の種類を制御します。
ms.openlocfilehash: 50b08664deec69659ff70a0bf9a17a148ed0e110
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413949"
---
# <a name="x-behavior-cell-controls-section"></a><span data-ttu-id="17180-103">[X Behavior] セル ([Controls] セクション)</span><span class="sxs-lookup"><span data-stu-id="17180-103">X Behavior Cell (Controls Section)</span></span>

<span data-ttu-id="17180-104">ハンドルの移動後にコントロール ハンドル  *の x*  座標が表示される動作の種類を制御します。</span><span class="sxs-lookup"><span data-stu-id="17180-104">Controls the type of behavior the  *x*  -coordinate of the control handle will exhibit after the handle is moved.</span></span> 
  
|<span data-ttu-id="17180-105">**値**</span><span class="sxs-lookup"><span data-stu-id="17180-105">**Value**</span></span>|<span data-ttu-id="17180-106">**動作**</span><span class="sxs-lookup"><span data-stu-id="17180-106">**Behavior**</span></span>|<span data-ttu-id="17180-107">**定義**</span><span class="sxs-lookup"><span data-stu-id="17180-107">**Definition**</span></span>|<span data-ttu-id="17180-108">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="17180-108">**Automation constant**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="17180-109">0</span><span class="sxs-lookup"><span data-stu-id="17180-109">0</span></span>  <br/> | <span data-ttu-id="17180-110">プロポーショナル</span><span class="sxs-lookup"><span data-stu-id="17180-110">Proportional</span></span>  <br/> | <span data-ttu-id="17180-111"> 
          コントロール ハンドルを移動できます。また図形を引き伸ばすと、図形に比例して移動します。
        </span><span class="sxs-lookup"><span data-stu-id="17180-111">The control handle can be moved, and it also moves in proportion with the shape when it is stretched.</span></span>  <br/> |<span data-ttu-id="17180-112">**visCtlProportional**</span><span class="sxs-lookup"><span data-stu-id="17180-112">**visCtlProportional**</span></span> <br/> |
| <span data-ttu-id="17180-113">1</span><span class="sxs-lookup"><span data-stu-id="17180-113">1</span></span>  <br/> | <span data-ttu-id="17180-114">プロポーショナル (ロック)</span><span class="sxs-lookup"><span data-stu-id="17180-114">Proportional locked</span></span>  <br/> | <span data-ttu-id="17180-115">コントロール ハンドルは図形に比例して移動しますが、コントロール ハンドル自体は移動できません。</span><span class="sxs-lookup"><span data-stu-id="17180-115">The control handle moves in proportion with the shape but the control handle itself cannot be moved.</span></span>  <br/> |<span data-ttu-id="17180-116">**visCtlLocked**</span><span class="sxs-lookup"><span data-stu-id="17180-116">**visCtlLocked**</span></span> <br/> |
| <span data-ttu-id="17180-117">2</span><span class="sxs-lookup"><span data-stu-id="17180-117">2</span></span>  <br/> | <span data-ttu-id="17180-118">左端からオフセット</span><span class="sxs-lookup"><span data-stu-id="17180-118">Offset from left edge</span></span>  <br/> | <span data-ttu-id="17180-119">コントロール ハンドルは、図形の左辺から一定の距離だけオフセットされます。</span><span class="sxs-lookup"><span data-stu-id="17180-119">The control handle is offset a constant distance from the left side of the shape.</span></span>  <br/> |<span data-ttu-id="17180-120">**visCtlOffsetMin**</span><span class="sxs-lookup"><span data-stu-id="17180-120">**visCtlOffsetMin**</span></span> <br/> |
| <span data-ttu-id="17180-121">3</span><span class="sxs-lookup"><span data-stu-id="17180-121">3</span></span>  <br/> | <span data-ttu-id="17180-122">中心からオフセット</span><span class="sxs-lookup"><span data-stu-id="17180-122">Offset from center</span></span>  <br/> | <span data-ttu-id="17180-123">コントロール ハンドルは、図形の中心から一定の距離だけオフセットされます。</span><span class="sxs-lookup"><span data-stu-id="17180-123">The control handle is offset a constant distance from the center of the shape.</span></span>  <br/> |<span data-ttu-id="17180-124">**visCtlOffsetMid**</span><span class="sxs-lookup"><span data-stu-id="17180-124">**visCtlOffsetMid**</span></span> <br/> |
| <span data-ttu-id="17180-125">4</span><span class="sxs-lookup"><span data-stu-id="17180-125">4</span></span>  <br/> | <span data-ttu-id="17180-126">右端からオフセット</span><span class="sxs-lookup"><span data-stu-id="17180-126">Offset from right edge</span></span>  <br/> | <span data-ttu-id="17180-127">コントロール ハンドルは、図形の右辺から一定の距離だけオフセットされます。</span><span class="sxs-lookup"><span data-stu-id="17180-127">The control handle is offset a constant distance from the right side of the shape.</span></span>  <br/> |<span data-ttu-id="17180-128">**visCtlOffsetMax**</span><span class="sxs-lookup"><span data-stu-id="17180-128">**visCtlOffsetMax**</span></span> <br/> |
| <span data-ttu-id="17180-129">5</span><span class="sxs-lookup"><span data-stu-id="17180-129">5</span></span>  <br/> | <span data-ttu-id="17180-130">プロポーショナル (非表示)</span><span class="sxs-lookup"><span data-stu-id="17180-130">Proportional, hidden</span></span>  <br/> | <span data-ttu-id="17180-131">0 と同じですが、コントロール ハンドルは表示されません。</span><span class="sxs-lookup"><span data-stu-id="17180-131">Same as 0, but the control handle is not visible.</span></span>  <br/> |<span data-ttu-id="17180-132">**visCtlProportionalHidden**</span><span class="sxs-lookup"><span data-stu-id="17180-132">**visCtlProportionalHidden**</span></span> <br/> |
| <span data-ttu-id="17180-133">6</span><span class="sxs-lookup"><span data-stu-id="17180-133">6</span></span>  <br/> | <span data-ttu-id="17180-134">プロポーショナル (ロック、非表示)</span><span class="sxs-lookup"><span data-stu-id="17180-134">Proportional locked, hidden</span></span>  <br/> | <span data-ttu-id="17180-135">1 と同じですが、コントロール ハンドルは表示されません。</span><span class="sxs-lookup"><span data-stu-id="17180-135">Same as 1, but the control handle is not visible.</span></span>  <br/> |<span data-ttu-id="17180-136">**visCtlLockedHiddenv**</span><span class="sxs-lookup"><span data-stu-id="17180-136">**visCtlLockedHiddenv**</span></span> <br/> |
| <span data-ttu-id="17180-137">7</span><span class="sxs-lookup"><span data-stu-id="17180-137">7</span></span>  <br/> | <span data-ttu-id="17180-138">左端からオフセット (非表示)</span><span class="sxs-lookup"><span data-stu-id="17180-138">Offset from left edge, hidden</span></span>  <br/> | <span data-ttu-id="17180-139">2 と同じですが、コントロール ハンドルは表示されません。</span><span class="sxs-lookup"><span data-stu-id="17180-139">Same as 2, but the control handle is not visible.</span></span>  <br/> |<span data-ttu-id="17180-140">**visCtlOffsetMinHidden**</span><span class="sxs-lookup"><span data-stu-id="17180-140">**visCtlOffsetMinHidden**</span></span> <br/> |
| <span data-ttu-id="17180-141">8</span><span class="sxs-lookup"><span data-stu-id="17180-141">8</span></span>  <br/> | <span data-ttu-id="17180-142">中心からオフセット (非表示)</span><span class="sxs-lookup"><span data-stu-id="17180-142">Offset from center, hidden</span></span>  <br/> | <span data-ttu-id="17180-143">3 と同じですが、コントロール ハンドルは表示されません。</span><span class="sxs-lookup"><span data-stu-id="17180-143">Same as 3, but the control handle is not visible.</span></span>  <br/> |<span data-ttu-id="17180-144">**visCtlOffsetMidHidden**</span><span class="sxs-lookup"><span data-stu-id="17180-144">**visCtlOffsetMidHidden**</span></span> <br/> |
| <span data-ttu-id="17180-145">9</span><span class="sxs-lookup"><span data-stu-id="17180-145">9</span></span>  <br/> | <span data-ttu-id="17180-146">右端からオフセット (非表示)</span><span class="sxs-lookup"><span data-stu-id="17180-146">Offset from right edge, hidden</span></span>  <br/> | <span data-ttu-id="17180-147">4 と同じですが、コントロール ハンドルは表示されません。</span><span class="sxs-lookup"><span data-stu-id="17180-147">Same as 4, but the control handle is not visible.</span></span>  <br/> |<span data-ttu-id="17180-148">**visCtlOffsetMaxHidden**</span><span class="sxs-lookup"><span data-stu-id="17180-148">**visCtlOffsetMaxHidden**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="17180-149">注釈</span><span class="sxs-lookup"><span data-stu-id="17180-149">Remarks</span></span>

<span data-ttu-id="17180-150">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [X Behavior] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="17180-150">To get a reference to the X Behavior cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="17180-151">セル名:</span><span class="sxs-lookup"><span data-stu-id="17180-151">Cell name:</span></span>  <br/> | <span data-ttu-id="17180-152">コントロール。</span><span class="sxs-lookup"><span data-stu-id="17180-152">Controls.</span></span>  <span data-ttu-id="17180-153">*name*  .XConwhere コントロール。</span><span class="sxs-lookup"><span data-stu-id="17180-153">*name*  .XConwhere Controls.</span></span>  <span data-ttu-id="17180-154">*name*  は、コントロール行の名前です。</span><span class="sxs-lookup"><span data-stu-id="17180-154">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="17180-155">プログラムから、インデックスによって [X Behavior] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="17180-155">To get a reference to the X Behavior cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="17180-156">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="17180-156">Section index:</span></span>  <br/> |<span data-ttu-id="17180-157">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="17180-157">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="17180-158">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="17180-158">Row index:</span></span>  <br/> |<span data-ttu-id="17180-159">**visRowControl**  +  *i* *=* 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="17180-159">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="17180-160">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="17180-160">Cell index:</span></span>  <br/> |<span data-ttu-id="17180-161">**visCtlXCon**</span><span class="sxs-lookup"><span data-stu-id="17180-161">**visCtlXCon**</span></span> <br/> |
   

