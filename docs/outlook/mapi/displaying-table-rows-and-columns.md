---
title: テーブルの行と列の表示
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 49567a8d-b58d-4636-bead-a1f84b4f111d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f9f1cc0bebf3c90a5c12f2714e8ab7eea59104da
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407117"
---
# <a name="displaying-table-rows-and-columns"></a><span data-ttu-id="73f8f-103">テーブルの行と列の表示</span><span class="sxs-lookup"><span data-stu-id="73f8f-103">Displaying Table Rows and Columns</span></span>

  
  
<span data-ttu-id="73f8f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="73f8f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="73f8f-105">アドレス帳プロバイダーは、プロパティ ページを使用して、ユーザーが新しい電子メール受信者を定義できます。</span><span class="sxs-lookup"><span data-stu-id="73f8f-105">A property page can be used by an address book provider to enable users to define new email recipients.</span></span> 
  
<span data-ttu-id="73f8f-106">対応する表示テーブルには、コントロールごとに 1 行の 4 行が含まれます。</span><span class="sxs-lookup"><span data-stu-id="73f8f-106">The corresponding display table contains four rows, one for each control.</span></span> <span data-ttu-id="73f8f-107">位置を示す列の値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="73f8f-107">The values for the columns that indicate position are as follows.</span></span>
  
|<span data-ttu-id="73f8f-108">**Control**</span><span class="sxs-lookup"><span data-stu-id="73f8f-108">**Control**</span></span>|<span data-ttu-id="73f8f-109">**XPOS**</span><span class="sxs-lookup"><span data-stu-id="73f8f-109">**XPOS**</span></span>|<span data-ttu-id="73f8f-110">**YPOS**</span><span class="sxs-lookup"><span data-stu-id="73f8f-110">**YPOS**</span></span>|<span data-ttu-id="73f8f-111">**DELTAX**</span><span class="sxs-lookup"><span data-stu-id="73f8f-111">**DELTAX**</span></span>|<span data-ttu-id="73f8f-112">**DELTAY**</span><span class="sxs-lookup"><span data-stu-id="73f8f-112">**DELTAY**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="73f8f-113">表示名ラベル</span><span class="sxs-lookup"><span data-stu-id="73f8f-113">Display name label</span></span>  <br/> |<span data-ttu-id="73f8f-114">14 </span><span class="sxs-lookup"><span data-stu-id="73f8f-114">14</span></span>  <br/> |<span data-ttu-id="73f8f-115">18 </span><span class="sxs-lookup"><span data-stu-id="73f8f-115">18</span></span>  <br/> |<span data-ttu-id="73f8f-116">49</span><span class="sxs-lookup"><span data-stu-id="73f8f-116">49</span></span>  <br/> |<span data-ttu-id="73f8f-117">8</span><span class="sxs-lookup"><span data-stu-id="73f8f-117">8</span></span>  <br/> |
|<span data-ttu-id="73f8f-118">[表示名] 編集ボックス</span><span class="sxs-lookup"><span data-stu-id="73f8f-118">Display name edit box</span></span>  <br/> |<span data-ttu-id="73f8f-119">76</span><span class="sxs-lookup"><span data-stu-id="73f8f-119">76</span></span>  <br/> |<span data-ttu-id="73f8f-120">16 </span><span class="sxs-lookup"><span data-stu-id="73f8f-120">16</span></span>  <br/> |<span data-ttu-id="73f8f-121">89</span><span class="sxs-lookup"><span data-stu-id="73f8f-121">89</span></span>  <br/> |<span data-ttu-id="73f8f-122">12 </span><span class="sxs-lookup"><span data-stu-id="73f8f-122">12</span></span>  <br/> |
|<span data-ttu-id="73f8f-123">電子メール アドレス ラベル</span><span class="sxs-lookup"><span data-stu-id="73f8f-123">Email address label</span></span>  <br/> |<span data-ttu-id="73f8f-124">14 </span><span class="sxs-lookup"><span data-stu-id="73f8f-124">14</span></span>  <br/> |<span data-ttu-id="73f8f-125">42</span><span class="sxs-lookup"><span data-stu-id="73f8f-125">42</span></span>  <br/> |<span data-ttu-id="73f8f-126">50</span><span class="sxs-lookup"><span data-stu-id="73f8f-126">50</span></span>  <br/> |<span data-ttu-id="73f8f-127">8</span><span class="sxs-lookup"><span data-stu-id="73f8f-127">8</span></span>  <br/> |
|<span data-ttu-id="73f8f-128">[電子メール アドレスの編集] ボックス</span><span class="sxs-lookup"><span data-stu-id="73f8f-128">Email address edit box</span></span>  <br/> |<span data-ttu-id="73f8f-129">76</span><span class="sxs-lookup"><span data-stu-id="73f8f-129">76</span></span>  <br/> |<span data-ttu-id="73f8f-130">40</span><span class="sxs-lookup"><span data-stu-id="73f8f-130">40</span></span>  <br/> |<span data-ttu-id="73f8f-131">89</span><span class="sxs-lookup"><span data-stu-id="73f8f-131">89</span></span>  <br/> |<span data-ttu-id="73f8f-132">12 </span><span class="sxs-lookup"><span data-stu-id="73f8f-132">12</span></span>  <br/> |
|<span data-ttu-id="73f8f-133">チェック ボックス</span><span class="sxs-lookup"><span data-stu-id="73f8f-133">Check box</span></span>  <br/> |<span data-ttu-id="73f8f-134">14 </span><span class="sxs-lookup"><span data-stu-id="73f8f-134">14</span></span>  <br/> |<span data-ttu-id="73f8f-135">64</span><span class="sxs-lookup"><span data-stu-id="73f8f-135">64</span></span>  <br/> |<span data-ttu-id="73f8f-136">90</span><span class="sxs-lookup"><span data-stu-id="73f8f-136">90</span></span>  <br/> |<span data-ttu-id="73f8f-137">12 </span><span class="sxs-lookup"><span data-stu-id="73f8f-137">12</span></span>  <br/> |
   
<span data-ttu-id="73f8f-138">次の表は、コントロールの型、 **その PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) プロパティ、およびフラグのビットマスク 、その PR_CONTROL_FLAGS **(** [PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) プロパティに適切な値を示します。</span><span class="sxs-lookup"><span data-stu-id="73f8f-138">This next table suggests appropriate values for the control's type, its **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) property, and bitmask of flags, its **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) property.</span></span>
  
|<span data-ttu-id="73f8f-139">**Control**</span><span class="sxs-lookup"><span data-stu-id="73f8f-139">**Control**</span></span>|<span data-ttu-id="73f8f-140">**Type**</span><span class="sxs-lookup"><span data-stu-id="73f8f-140">**Type**</span></span>|<span data-ttu-id="73f8f-141">**Flags**</span><span class="sxs-lookup"><span data-stu-id="73f8f-141">**Flags**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="73f8f-142">表示名ラベル</span><span class="sxs-lookup"><span data-stu-id="73f8f-142">Display name label</span></span>  <br/> |<span data-ttu-id="73f8f-143">DTCT_LABEL</span><span class="sxs-lookup"><span data-stu-id="73f8f-143">DTCT_LABEL</span></span>  <br/> |<span data-ttu-id="73f8f-144">0</span><span class="sxs-lookup"><span data-stu-id="73f8f-144">0</span></span>  <br/> |
|<span data-ttu-id="73f8f-145">[表示名] 編集ボックス</span><span class="sxs-lookup"><span data-stu-id="73f8f-145">Display name edit box</span></span>  <br/> |<span data-ttu-id="73f8f-146">DTCT_EDIT</span><span class="sxs-lookup"><span data-stu-id="73f8f-146">DTCT_EDIT</span></span>  <br/> |<span data-ttu-id="73f8f-147">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="73f8f-147">DT_EDITABLE</span></span> | <span data-ttu-id="73f8f-148">DT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="73f8f-148">DT_REQUIRED</span></span>  <br/> |
|<span data-ttu-id="73f8f-149">電子メール アドレス ラベル</span><span class="sxs-lookup"><span data-stu-id="73f8f-149">Email address label</span></span>  <br/> |<span data-ttu-id="73f8f-150">DTCT_LABEL</span><span class="sxs-lookup"><span data-stu-id="73f8f-150">DTCT_LABEL</span></span>  <br/> |<span data-ttu-id="73f8f-151">0</span><span class="sxs-lookup"><span data-stu-id="73f8f-151">0</span></span>  <br/> |
|<span data-ttu-id="73f8f-152">[電子メール アドレスの編集] ボックス</span><span class="sxs-lookup"><span data-stu-id="73f8f-152">Email address edit box</span></span>  <br/> |<span data-ttu-id="73f8f-153">DTCT_EDIT</span><span class="sxs-lookup"><span data-stu-id="73f8f-153">DTCT_EDIT</span></span>  <br/> |<span data-ttu-id="73f8f-154">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="73f8f-154">DT_EDITABLE</span></span> | <span data-ttu-id="73f8f-155">DT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="73f8f-155">DT_REQUIRED</span></span>  <br/> |
|<span data-ttu-id="73f8f-156">チェック ボックス</span><span class="sxs-lookup"><span data-stu-id="73f8f-156">Check box</span></span>  <br/> |<span data-ttu-id="73f8f-157">DTCT_CHECKBOX</span><span class="sxs-lookup"><span data-stu-id="73f8f-157">DTCT_CHECKBOX</span></span>  <br/> |<span data-ttu-id="73f8f-158">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="73f8f-158">DT_EDITABLE</span></span>  <br/> |
   
<span data-ttu-id="73f8f-159">最後の表には、関連付けられたコントロール構造の内容を含む各コントロールが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="73f8f-159">The final table lists each control with the contents of its associated control structure.</span></span> <span data-ttu-id="73f8f-160">各ラベル コントロールの値は、構造体の直下のメモリに表示されます。</span><span class="sxs-lookup"><span data-stu-id="73f8f-160">Notice that the value for each of the label controls appears in memory directly following the structure.</span></span>
  
|<span data-ttu-id="73f8f-161">**Control**</span><span class="sxs-lookup"><span data-stu-id="73f8f-161">**Control**</span></span>|<span data-ttu-id="73f8f-162">**Structure**</span><span class="sxs-lookup"><span data-stu-id="73f8f-162">**Structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="73f8f-163">表示名ラベル</span><span class="sxs-lookup"><span data-stu-id="73f8f-163">Display name label</span></span>  <br/> |<span data-ttu-id="73f8f-164">{sizeof(DTBLLABEL), 0}"表示名:"</span><span class="sxs-lookup"><span data-stu-id="73f8f-164">{sizeof(DTBLLABEL), 0} "Display name:"</span></span>  <br/> |
|<span data-ttu-id="73f8f-165">[表示名] 編集ボックス</span><span class="sxs-lookup"><span data-stu-id="73f8f-165">Display name edit box</span></span>  <br/> |<span data-ttu-id="73f8f-166">{sizeof(DTBLEDIT), 0, 80, PR_DISPLAY_NAME}</span><span class="sxs-lookup"><span data-stu-id="73f8f-166">{sizeof(DTBLEDIT), 0, 80, PR_DISPLAY_NAME}</span></span>  <br/> |
|<span data-ttu-id="73f8f-167">電子メール アドレス ラベル</span><span class="sxs-lookup"><span data-stu-id="73f8f-167">Email address label</span></span>  <br/> |<span data-ttu-id="73f8f-168">{sizeof(DTBLLABEL), 0}"Email address:"</span><span class="sxs-lookup"><span data-stu-id="73f8f-168">{sizeof(DTBLLABEL), 0} "Email address:"</span></span>  <br/> |
|<span data-ttu-id="73f8f-169">[電子メール アドレスの編集] ボックス</span><span class="sxs-lookup"><span data-stu-id="73f8f-169">Email address edit box</span></span>  <br/> |<span data-ttu-id="73f8f-170">{sizeof(DTBLEDIT), 0, 80, PR_EMAIL_ADDRESS}</span><span class="sxs-lookup"><span data-stu-id="73f8f-170">{sizeof(DTBLEDIT), 0, 80, PR_EMAIL_ADDRESS}</span></span>  <br/> |
|<span data-ttu-id="73f8f-171">チェック ボックス</span><span class="sxs-lookup"><span data-stu-id="73f8f-171">Check box</span></span>  <br/> |<span data-ttu-id="73f8f-172">PR_SEND_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="73f8f-172">PR_SEND_RICH_INFO</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="73f8f-173">**[OK]、[\*\*\*\*キャンセル**]、**および [ヘルプ**] ボタンは、表示テーブルには含まれません。</span><span class="sxs-lookup"><span data-stu-id="73f8f-173">The **OK**, **Cancel**, and **Help** buttons are not included in the display table.</span></span> <span data-ttu-id="73f8f-174">ユーザー インターフェイスは、表示テーブルではなくコントロールを追加することで、ダイアログ ボックスにコンテキストを追加できます。</span><span class="sxs-lookup"><span data-stu-id="73f8f-174">The user interface can add context to a dialog box by adding controls not in the display table.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="73f8f-175">関連項目</span><span class="sxs-lookup"><span data-stu-id="73f8f-175">See also</span></span>



[<span data-ttu-id="73f8f-176">表示テーブルの実装</span><span class="sxs-lookup"><span data-stu-id="73f8f-176">Display Table Implementation</span></span>](display-table-implementation.md)

