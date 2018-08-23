---
title: テーブルの行と列の表示
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 49567a8d-b58d-4636-bead-a1f84b4f111d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: dba7bd1fb7b0ca9bc23dbc45e07f44d0cc0dc8fe
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568141"
---
# <a name="displaying-table-rows-and-columns"></a><span data-ttu-id="bf0d3-103">テーブルの行と列の表示</span><span class="sxs-lookup"><span data-stu-id="bf0d3-103">Displaying Table Rows and Columns</span></span>

  
  
<span data-ttu-id="bf0d3-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf0d3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="bf0d3-105">新しい電子メールの受信者を定義するユーザーを有効にするのには、アドレス帳プロバイダーがプロパティ ページを使用できます。</span><span class="sxs-lookup"><span data-stu-id="bf0d3-105">A property page can be used by an address book provider to enable users to define new email recipients.</span></span> 
  
<span data-ttu-id="bf0d3-106">表示された対応する表には、コントロールごとに 1 つ、4 つの行が含まれています。</span><span class="sxs-lookup"><span data-stu-id="bf0d3-106">The corresponding display table contains four rows, one for each control.</span></span> <span data-ttu-id="bf0d3-107">位置を示す列の値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="bf0d3-107">The values for the columns that indicate position are as follows.</span></span>
  
|<span data-ttu-id="bf0d3-108">**Control**</span><span class="sxs-lookup"><span data-stu-id="bf0d3-108">**Control**</span></span>|<span data-ttu-id="bf0d3-109">**XPOS**</span><span class="sxs-lookup"><span data-stu-id="bf0d3-109">**XPOS**</span></span>|<span data-ttu-id="bf0d3-110">**YPOS**</span><span class="sxs-lookup"><span data-stu-id="bf0d3-110">**YPOS**</span></span>|<span data-ttu-id="bf0d3-111">**DELTAX**</span><span class="sxs-lookup"><span data-stu-id="bf0d3-111">**DELTAX**</span></span>|<span data-ttu-id="bf0d3-112">**DELTAY**</span><span class="sxs-lookup"><span data-stu-id="bf0d3-112">**DELTAY**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="bf0d3-113">名前ラベルを表示</span><span class="sxs-lookup"><span data-stu-id="bf0d3-113">Display name label</span></span>  <br/> |<span data-ttu-id="bf0d3-114">14</span><span class="sxs-lookup"><span data-stu-id="bf0d3-114">14</span></span>  <br/> |<span data-ttu-id="bf0d3-115">18</span><span class="sxs-lookup"><span data-stu-id="bf0d3-115">18</span></span>  <br/> |<span data-ttu-id="bf0d3-116">49</span><span class="sxs-lookup"><span data-stu-id="bf0d3-116">49</span></span>  <br/> |<span data-ttu-id="bf0d3-117">8</span><span class="sxs-lookup"><span data-stu-id="bf0d3-117">8</span></span>  <br/> |
|<span data-ttu-id="bf0d3-118">表示名の編集] ボックス</span><span class="sxs-lookup"><span data-stu-id="bf0d3-118">Display name edit box</span></span>  <br/> |<span data-ttu-id="bf0d3-119">76</span><span class="sxs-lookup"><span data-stu-id="bf0d3-119">76</span></span>  <br/> |<span data-ttu-id="bf0d3-120">16</span><span class="sxs-lookup"><span data-stu-id="bf0d3-120">16</span></span>  <br/> |<span data-ttu-id="bf0d3-121">89</span><span class="sxs-lookup"><span data-stu-id="bf0d3-121">89</span></span>  <br/> |<span data-ttu-id="bf0d3-122">12</span><span class="sxs-lookup"><span data-stu-id="bf0d3-122">12</span></span>  <br/> |
|<span data-ttu-id="bf0d3-123">電子メール アドレスのラベル</span><span class="sxs-lookup"><span data-stu-id="bf0d3-123">Email address label</span></span>  <br/> |<span data-ttu-id="bf0d3-124">14</span><span class="sxs-lookup"><span data-stu-id="bf0d3-124">14</span></span>  <br/> |<span data-ttu-id="bf0d3-125">42</span><span class="sxs-lookup"><span data-stu-id="bf0d3-125">42</span></span>  <br/> |<span data-ttu-id="bf0d3-126">50</span><span class="sxs-lookup"><span data-stu-id="bf0d3-126">50</span></span>  <br/> |<span data-ttu-id="bf0d3-127">8</span><span class="sxs-lookup"><span data-stu-id="bf0d3-127">8</span></span>  <br/> |
|<span data-ttu-id="bf0d3-128">電子メール アドレスの編集] ボックス</span><span class="sxs-lookup"><span data-stu-id="bf0d3-128">Email address edit box</span></span>  <br/> |<span data-ttu-id="bf0d3-129">76</span><span class="sxs-lookup"><span data-stu-id="bf0d3-129">76</span></span>  <br/> |<span data-ttu-id="bf0d3-130">40</span><span class="sxs-lookup"><span data-stu-id="bf0d3-130">40</span></span>  <br/> |<span data-ttu-id="bf0d3-131">89</span><span class="sxs-lookup"><span data-stu-id="bf0d3-131">89</span></span>  <br/> |<span data-ttu-id="bf0d3-132">12</span><span class="sxs-lookup"><span data-stu-id="bf0d3-132">12</span></span>  <br/> |
|<span data-ttu-id="bf0d3-133">チェック ボックス</span><span class="sxs-lookup"><span data-stu-id="bf0d3-133">Check box</span></span>  <br/> |<span data-ttu-id="bf0d3-134">14</span><span class="sxs-lookup"><span data-stu-id="bf0d3-134">14</span></span>  <br/> |<span data-ttu-id="bf0d3-135">64</span><span class="sxs-lookup"><span data-stu-id="bf0d3-135">64</span></span>  <br/> |<span data-ttu-id="bf0d3-136">90</span><span class="sxs-lookup"><span data-stu-id="bf0d3-136">90</span></span>  <br/> |<span data-ttu-id="bf0d3-137">12</span><span class="sxs-lookup"><span data-stu-id="bf0d3-137">12</span></span>  <br/> |
   
<span data-ttu-id="bf0d3-138">この次の表では、コントロールの種類、 **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) のプロパティ、および、 **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) プロパティのフラグのビットマスクの適切な値を示しています。</span><span class="sxs-lookup"><span data-stu-id="bf0d3-138">This next table suggests appropriate values for the control's type, its **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) property, and bitmask of flags, its **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) property.</span></span>
  
|<span data-ttu-id="bf0d3-139">**Control**</span><span class="sxs-lookup"><span data-stu-id="bf0d3-139">**Control**</span></span>|<span data-ttu-id="bf0d3-140">**型**</span><span class="sxs-lookup"><span data-stu-id="bf0d3-140">**Type**</span></span>|<span data-ttu-id="bf0d3-141">**Flags**</span><span class="sxs-lookup"><span data-stu-id="bf0d3-141">**Flags**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bf0d3-142">名前ラベルを表示</span><span class="sxs-lookup"><span data-stu-id="bf0d3-142">Display name label</span></span>  <br/> |<span data-ttu-id="bf0d3-143">DTCT_LABEL</span><span class="sxs-lookup"><span data-stu-id="bf0d3-143">DTCT_LABEL</span></span>  <br/> |<span data-ttu-id="bf0d3-144">0</span><span class="sxs-lookup"><span data-stu-id="bf0d3-144">0</span></span>  <br/> |
|<span data-ttu-id="bf0d3-145">表示名の編集] ボックス</span><span class="sxs-lookup"><span data-stu-id="bf0d3-145">Display name edit box</span></span>  <br/> |<span data-ttu-id="bf0d3-146">DTCT_EDIT</span><span class="sxs-lookup"><span data-stu-id="bf0d3-146">DTCT_EDIT</span></span>  <br/> |<span data-ttu-id="bf0d3-147">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="bf0d3-147">DT_EDITABLE</span></span> | <span data-ttu-id="bf0d3-148">DT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="bf0d3-148">DT_REQUIRED</span></span>  <br/> |
|<span data-ttu-id="bf0d3-149">電子メール アドレスのラベル</span><span class="sxs-lookup"><span data-stu-id="bf0d3-149">Email address label</span></span>  <br/> |<span data-ttu-id="bf0d3-150">DTCT_LABEL</span><span class="sxs-lookup"><span data-stu-id="bf0d3-150">DTCT_LABEL</span></span>  <br/> |<span data-ttu-id="bf0d3-151">0</span><span class="sxs-lookup"><span data-stu-id="bf0d3-151">0</span></span>  <br/> |
|<span data-ttu-id="bf0d3-152">電子メール アドレスの編集] ボックス</span><span class="sxs-lookup"><span data-stu-id="bf0d3-152">Email address edit box</span></span>  <br/> |<span data-ttu-id="bf0d3-153">DTCT_EDIT</span><span class="sxs-lookup"><span data-stu-id="bf0d3-153">DTCT_EDIT</span></span>  <br/> |<span data-ttu-id="bf0d3-154">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="bf0d3-154">DT_EDITABLE</span></span> | <span data-ttu-id="bf0d3-155">DT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="bf0d3-155">DT_REQUIRED</span></span>  <br/> |
|<span data-ttu-id="bf0d3-156">チェック ボックス</span><span class="sxs-lookup"><span data-stu-id="bf0d3-156">Check box</span></span>  <br/> |<span data-ttu-id="bf0d3-157">DTCT_CHECKBOX</span><span class="sxs-lookup"><span data-stu-id="bf0d3-157">DTCT_CHECKBOX</span></span>  <br/> |<span data-ttu-id="bf0d3-158">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="bf0d3-158">DT_EDITABLE</span></span>  <br/> |
   
<span data-ttu-id="bf0d3-159">最後の表は、各コントロールを関連付けられているコントロールの構造体の内容です。</span><span class="sxs-lookup"><span data-stu-id="bf0d3-159">The final table lists each control with the contents of its associated control structure.</span></span> <span data-ttu-id="bf0d3-160">直接次の構造体のメモリ内の各ラベルのコントロールの値が表示されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="bf0d3-160">Notice that the value for each of the label controls appears in memory directly following the structure.</span></span>
  
|<span data-ttu-id="bf0d3-161">**Control**</span><span class="sxs-lookup"><span data-stu-id="bf0d3-161">**Control**</span></span>|<span data-ttu-id="bf0d3-162">**Structure**</span><span class="sxs-lookup"><span data-stu-id="bf0d3-162">**Structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bf0d3-163">名前ラベルを表示</span><span class="sxs-lookup"><span data-stu-id="bf0d3-163">Display name label</span></span>  <br/> |<span data-ttu-id="bf0d3-164">{sizeof(DTBLLABEL)、0}"表示名:"</span><span class="sxs-lookup"><span data-stu-id="bf0d3-164">{sizeof(DTBLLABEL), 0} "Display name:"</span></span>  <br/> |
|<span data-ttu-id="bf0d3-165">表示名の編集] ボックス</span><span class="sxs-lookup"><span data-stu-id="bf0d3-165">Display name edit box</span></span>  <br/> |<span data-ttu-id="bf0d3-166">{sizeof(DTBLEDIT)、0、80、PR_DISPLAY_NAME}</span><span class="sxs-lookup"><span data-stu-id="bf0d3-166">{sizeof(DTBLEDIT), 0, 80, PR_DISPLAY_NAME}</span></span>  <br/> |
|<span data-ttu-id="bf0d3-167">電子メール アドレスのラベル</span><span class="sxs-lookup"><span data-stu-id="bf0d3-167">Email address label</span></span>  <br/> |<span data-ttu-id="bf0d3-168">{sizeof(DTBLLABEL)、0}"電子メール アドレス:"</span><span class="sxs-lookup"><span data-stu-id="bf0d3-168">{sizeof(DTBLLABEL), 0} "Email address:"</span></span>  <br/> |
|<span data-ttu-id="bf0d3-169">電子メール アドレスの編集] ボックス</span><span class="sxs-lookup"><span data-stu-id="bf0d3-169">Email address edit box</span></span>  <br/> |<span data-ttu-id="bf0d3-170">{sizeof(DTBLEDIT)、0、80、PR_EMAIL_ADDRESS}</span><span class="sxs-lookup"><span data-stu-id="bf0d3-170">{sizeof(DTBLEDIT), 0, 80, PR_EMAIL_ADDRESS}</span></span>  <br/> |
|<span data-ttu-id="bf0d3-171">チェック ボックス</span><span class="sxs-lookup"><span data-stu-id="bf0d3-171">Check box</span></span>  <br/> |<span data-ttu-id="bf0d3-172">PR_SEND_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="bf0d3-172">PR_SEND_RICH_INFO</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="bf0d3-173">**[Ok]**、**キャンセル**、および**ヘルプ**のボタンは、表示された表には含まれません。</span><span class="sxs-lookup"><span data-stu-id="bf0d3-173">The **OK**, **Cancel**, and **Help** buttons are not included in the display table.</span></span> <span data-ttu-id="bf0d3-174">ユーザー ・ インタ フェースは、表示テーブルにないコントロールを追加することによって、ダイアログ ボックスにコンテキストを追加できます。</span><span class="sxs-lookup"><span data-stu-id="bf0d3-174">The user interface can add context to a dialog box by adding controls not in the display table.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bf0d3-175">関連項目</span><span class="sxs-lookup"><span data-stu-id="bf0d3-175">See also</span></span>



[<span data-ttu-id="bf0d3-176">表示テーブルの実装</span><span class="sxs-lookup"><span data-stu-id="bf0d3-176">Display Table Implementation</span></span>](display-table-implementation.md)

