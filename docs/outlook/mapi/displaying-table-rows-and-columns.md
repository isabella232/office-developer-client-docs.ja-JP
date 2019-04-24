---
title: 表の行と列の表示
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 49567a8d-b58d-4636-bead-a1f84b4f111d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f9f1cc0bebf3c90a5c12f2714e8ab7eea59104da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337024"
---
# <a name="displaying-table-rows-and-columns"></a><span data-ttu-id="a08a1-103">表の行と列の表示</span><span class="sxs-lookup"><span data-stu-id="a08a1-103">Displaying Table Rows and Columns</span></span>

  
  
<span data-ttu-id="a08a1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a08a1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="a08a1-105">プロパティページは、ユーザーが新しい電子メール受信者を定義できるように、アドレス帳プロバイダーが使用できます。</span><span class="sxs-lookup"><span data-stu-id="a08a1-105">A property page can be used by an address book provider to enable users to define new email recipients.</span></span> 
  
<span data-ttu-id="a08a1-106">対応する表示テーブルには、コントロールごとに1つずつ、4つの行が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a08a1-106">The corresponding display table contains four rows, one for each control.</span></span> <span data-ttu-id="a08a1-107">position を示す列の値は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="a08a1-107">The values for the columns that indicate position are as follows.</span></span>
  
|<span data-ttu-id="a08a1-108">**Control**</span><span class="sxs-lookup"><span data-stu-id="a08a1-108">**Control**</span></span>|<span data-ttu-id="a08a1-109">**XPOS**</span><span class="sxs-lookup"><span data-stu-id="a08a1-109">**XPOS**</span></span>|<span data-ttu-id="a08a1-110">**YPOS**</span><span class="sxs-lookup"><span data-stu-id="a08a1-110">**YPOS**</span></span>|<span data-ttu-id="a08a1-111">**deltax**</span><span class="sxs-lookup"><span data-stu-id="a08a1-111">**DELTAX**</span></span>|<span data-ttu-id="a08a1-112">**deltay**</span><span class="sxs-lookup"><span data-stu-id="a08a1-112">**DELTAY**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a08a1-113">表示名ラベル</span><span class="sxs-lookup"><span data-stu-id="a08a1-113">Display name label</span></span>  <br/> |<span data-ttu-id="a08a1-114">第</span><span class="sxs-lookup"><span data-stu-id="a08a1-114">14</span></span>  <br/> |<span data-ttu-id="a08a1-115">個</span><span class="sxs-lookup"><span data-stu-id="a08a1-115">18</span></span>  <br/> |<span data-ttu-id="a08a1-116">49</span><span class="sxs-lookup"><span data-stu-id="a08a1-116">49</span></span>  <br/> |<span data-ttu-id="a08a1-117">~</span><span class="sxs-lookup"><span data-stu-id="a08a1-117">8</span></span>  <br/> |
|<span data-ttu-id="a08a1-118">[表示名] 編集ボックス</span><span class="sxs-lookup"><span data-stu-id="a08a1-118">Display name edit box</span></span>  <br/> |<span data-ttu-id="a08a1-119">76</span><span class="sxs-lookup"><span data-stu-id="a08a1-119">76</span></span>  <br/> |<span data-ttu-id="a08a1-120">16</span><span class="sxs-lookup"><span data-stu-id="a08a1-120">16</span></span>  <br/> |<span data-ttu-id="a08a1-121">89</span><span class="sxs-lookup"><span data-stu-id="a08a1-121">89</span></span>  <br/> |<span data-ttu-id="a08a1-122">個</span><span class="sxs-lookup"><span data-stu-id="a08a1-122">12</span></span>  <br/> |
|<span data-ttu-id="a08a1-123">電子メールアドレスラベル</span><span class="sxs-lookup"><span data-stu-id="a08a1-123">Email address label</span></span>  <br/> |<span data-ttu-id="a08a1-124">第</span><span class="sxs-lookup"><span data-stu-id="a08a1-124">14</span></span>  <br/> |<span data-ttu-id="a08a1-125">42</span><span class="sxs-lookup"><span data-stu-id="a08a1-125">42</span></span>  <br/> |<span data-ttu-id="a08a1-126">50</span><span class="sxs-lookup"><span data-stu-id="a08a1-126">50</span></span>  <br/> |<span data-ttu-id="a08a1-127">~</span><span class="sxs-lookup"><span data-stu-id="a08a1-127">8</span></span>  <br/> |
|<span data-ttu-id="a08a1-128">メールアドレスの編集ボックス</span><span class="sxs-lookup"><span data-stu-id="a08a1-128">Email address edit box</span></span>  <br/> |<span data-ttu-id="a08a1-129">76</span><span class="sxs-lookup"><span data-stu-id="a08a1-129">76</span></span>  <br/> |<span data-ttu-id="a08a1-130">40</span><span class="sxs-lookup"><span data-stu-id="a08a1-130">40</span></span>  <br/> |<span data-ttu-id="a08a1-131">89</span><span class="sxs-lookup"><span data-stu-id="a08a1-131">89</span></span>  <br/> |<span data-ttu-id="a08a1-132">個</span><span class="sxs-lookup"><span data-stu-id="a08a1-132">12</span></span>  <br/> |
|<span data-ttu-id="a08a1-133">チェック ボックス</span><span class="sxs-lookup"><span data-stu-id="a08a1-133">Check box</span></span>  <br/> |<span data-ttu-id="a08a1-134">第</span><span class="sxs-lookup"><span data-stu-id="a08a1-134">14</span></span>  <br/> |<span data-ttu-id="a08a1-135">64</span><span class="sxs-lookup"><span data-stu-id="a08a1-135">64</span></span>  <br/> |<span data-ttu-id="a08a1-136">90</span><span class="sxs-lookup"><span data-stu-id="a08a1-136">90</span></span>  <br/> |<span data-ttu-id="a08a1-137">個</span><span class="sxs-lookup"><span data-stu-id="a08a1-137">12</span></span>  <br/> |
   
<span data-ttu-id="a08a1-138">次の表は、コントロールの種類、 **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) プロパティ、フラグのビットマスク、 **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) プロパティの適切な値を示しています。</span><span class="sxs-lookup"><span data-stu-id="a08a1-138">This next table suggests appropriate values for the control's type, its **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) property, and bitmask of flags, its **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) property.</span></span>
  
|<span data-ttu-id="a08a1-139">**Control**</span><span class="sxs-lookup"><span data-stu-id="a08a1-139">**Control**</span></span>|<span data-ttu-id="a08a1-140">**Type**</span><span class="sxs-lookup"><span data-stu-id="a08a1-140">**Type**</span></span>|<span data-ttu-id="a08a1-141">**Flags**</span><span class="sxs-lookup"><span data-stu-id="a08a1-141">**Flags**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a08a1-142">表示名ラベル</span><span class="sxs-lookup"><span data-stu-id="a08a1-142">Display name label</span></span>  <br/> |<span data-ttu-id="a08a1-143">DTCT_LABEL</span><span class="sxs-lookup"><span data-stu-id="a08a1-143">DTCT_LABEL</span></span>  <br/> |<span data-ttu-id="a08a1-144">.0</span><span class="sxs-lookup"><span data-stu-id="a08a1-144">0</span></span>  <br/> |
|<span data-ttu-id="a08a1-145">[表示名] 編集ボックス</span><span class="sxs-lookup"><span data-stu-id="a08a1-145">Display name edit box</span></span>  <br/> |<span data-ttu-id="a08a1-146">DTCT_EDIT</span><span class="sxs-lookup"><span data-stu-id="a08a1-146">DTCT_EDIT</span></span>  <br/> |<span data-ttu-id="a08a1-147">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="a08a1-147">DT_EDITABLE</span></span> | <span data-ttu-id="a08a1-148">DT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="a08a1-148">DT_REQUIRED</span></span>  <br/> |
|<span data-ttu-id="a08a1-149">電子メールアドレスラベル</span><span class="sxs-lookup"><span data-stu-id="a08a1-149">Email address label</span></span>  <br/> |<span data-ttu-id="a08a1-150">DTCT_LABEL</span><span class="sxs-lookup"><span data-stu-id="a08a1-150">DTCT_LABEL</span></span>  <br/> |<span data-ttu-id="a08a1-151">.0</span><span class="sxs-lookup"><span data-stu-id="a08a1-151">0</span></span>  <br/> |
|<span data-ttu-id="a08a1-152">メールアドレスの編集ボックス</span><span class="sxs-lookup"><span data-stu-id="a08a1-152">Email address edit box</span></span>  <br/> |<span data-ttu-id="a08a1-153">DTCT_EDIT</span><span class="sxs-lookup"><span data-stu-id="a08a1-153">DTCT_EDIT</span></span>  <br/> |<span data-ttu-id="a08a1-154">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="a08a1-154">DT_EDITABLE</span></span> | <span data-ttu-id="a08a1-155">DT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="a08a1-155">DT_REQUIRED</span></span>  <br/> |
|<span data-ttu-id="a08a1-156">チェック ボックス</span><span class="sxs-lookup"><span data-stu-id="a08a1-156">Check box</span></span>  <br/> |<span data-ttu-id="a08a1-157">DTCT_CHECKBOX</span><span class="sxs-lookup"><span data-stu-id="a08a1-157">DTCT_CHECKBOX</span></span>  <br/> |<span data-ttu-id="a08a1-158">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="a08a1-158">DT_EDITABLE</span></span>  <br/> |
   
<span data-ttu-id="a08a1-159">最後の表に、関連付けられたコントロール構造の内容を含む各コントロールの一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="a08a1-159">The final table lists each control with the contents of its associated control structure.</span></span> <span data-ttu-id="a08a1-160">ラベルコントロールのそれぞれの値は、構造体のすぐ後のメモリに表示されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="a08a1-160">Notice that the value for each of the label controls appears in memory directly following the structure.</span></span>
  
|<span data-ttu-id="a08a1-161">**Control**</span><span class="sxs-lookup"><span data-stu-id="a08a1-161">**Control**</span></span>|<span data-ttu-id="a08a1-162">**Structure**</span><span class="sxs-lookup"><span data-stu-id="a08a1-162">**Structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a08a1-163">表示名ラベル</span><span class="sxs-lookup"><span data-stu-id="a08a1-163">Display name label</span></span>  <br/> |<span data-ttu-id="a08a1-164">{sizeof (dtbllabel), 0}"表示名:"</span><span class="sxs-lookup"><span data-stu-id="a08a1-164">{sizeof(DTBLLABEL), 0} "Display name:"</span></span>  <br/> |
|<span data-ttu-id="a08a1-165">[表示名] 編集ボックス</span><span class="sxs-lookup"><span data-stu-id="a08a1-165">Display name edit box</span></span>  <br/> |<span data-ttu-id="a08a1-166">{sizeof (DTBLEDIT)、0、80、PR_DISPLAY_NAME}</span><span class="sxs-lookup"><span data-stu-id="a08a1-166">{sizeof(DTBLEDIT), 0, 80, PR_DISPLAY_NAME}</span></span>  <br/> |
|<span data-ttu-id="a08a1-167">電子メールアドレスラベル</span><span class="sxs-lookup"><span data-stu-id="a08a1-167">Email address label</span></span>  <br/> |<span data-ttu-id="a08a1-168">{sizeof (dtbllabel), 0}"電子メールアドレス:"</span><span class="sxs-lookup"><span data-stu-id="a08a1-168">{sizeof(DTBLLABEL), 0} "Email address:"</span></span>  <br/> |
|<span data-ttu-id="a08a1-169">メールアドレスの編集ボックス</span><span class="sxs-lookup"><span data-stu-id="a08a1-169">Email address edit box</span></span>  <br/> |<span data-ttu-id="a08a1-170">{sizeof (DTBLEDIT)、0、80、PR_EMAIL_ADDRESS}</span><span class="sxs-lookup"><span data-stu-id="a08a1-170">{sizeof(DTBLEDIT), 0, 80, PR_EMAIL_ADDRESS}</span></span>  <br/> |
|<span data-ttu-id="a08a1-171">チェック ボックス</span><span class="sxs-lookup"><span data-stu-id="a08a1-171">Check box</span></span>  <br/> |<span data-ttu-id="a08a1-172">PR_SEND_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="a08a1-172">PR_SEND_RICH_INFO</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="a08a1-173">**[OK]**、 **[キャンセル**]、[**ヘルプ**] の各ボタンは、表示テーブルに含まれていません。</span><span class="sxs-lookup"><span data-stu-id="a08a1-173">The **OK**, **Cancel**, and **Help** buttons are not included in the display table.</span></span> <span data-ttu-id="a08a1-174">ユーザーインターフェイスでは、表示テーブルにないコントロールを追加することによって、ダイアログボックスにコンテキストを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="a08a1-174">The user interface can add context to a dialog box by adding controls not in the display table.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a08a1-175">関連項目</span><span class="sxs-lookup"><span data-stu-id="a08a1-175">See also</span></span>



[<span data-ttu-id="a08a1-176">表示テーブルの実装</span><span class="sxs-lookup"><span data-stu-id="a08a1-176">Display Table Implementation</span></span>](display-table-implementation.md)

