---
title: PidTagIconIndex 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIconIndex
api_type:
- HeaderDef
ms.assetid: 35bb0d6d-41d4-47d6-b161-be3721894201
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 35d9d0a50539f8aab2d26730dd4e4544c2535e60
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398109"
---
# <a name="pidtagiconindex-canonical-property"></a><span data-ttu-id="d0be6-103">PidTagIconIndex 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d0be6-103">PidTagIconIndex Canonical Property</span></span>

  
  
<span data-ttu-id="d0be6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d0be6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d0be6-105">電子メールのオブジェクトのグループを表示するときに使用するアイコンを表す数字が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d0be6-105">Contains a number that indicates which icon to use when you display a group of email objects.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d0be6-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d0be6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d0be6-107">PR_ICON_INDEX</span><span class="sxs-lookup"><span data-stu-id="d0be6-107">PR_ICON_INDEX</span></span>  <br/> |
|<span data-ttu-id="d0be6-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="d0be6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d0be6-109">0x1080</span><span class="sxs-lookup"><span data-stu-id="d0be6-109">0x1080</span></span>  <br/> |
|<span data-ttu-id="d0be6-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d0be6-110">Data type:</span></span>  <br/> |<span data-ttu-id="d0be6-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d0be6-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d0be6-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="d0be6-112">Area:</span></span>  <br/> |<span data-ttu-id="d0be6-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="d0be6-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d0be6-114">備考</span><span class="sxs-lookup"><span data-stu-id="d0be6-114">Remarks</span></span>

<span data-ttu-id="d0be6-115">このプロパティは、存在する場合は、クライアントへのヒントです。</span><span class="sxs-lookup"><span data-stu-id="d0be6-115">This property, if it exists, is a hint to the client.</span></span> <span data-ttu-id="d0be6-116">クライアントは、このプロパティの値を無視することがあります。</span><span class="sxs-lookup"><span data-stu-id="d0be6-116">The client may ignore the value of this property.</span></span> 
  
|<span data-ttu-id="d0be6-117">**メール アイテムの状態**</span><span class="sxs-lookup"><span data-stu-id="d0be6-117">**Mail item state**</span></span>|<span data-ttu-id="d0be6-118">**アイコンのインデックス**</span><span class="sxs-lookup"><span data-stu-id="d0be6-118">**Icon Index**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d0be6-119">新着メール</span><span class="sxs-lookup"><span data-stu-id="d0be6-119">New mail</span></span>  <br/> |<span data-ttu-id="d0be6-120">0 xffffffff</span><span class="sxs-lookup"><span data-stu-id="d0be6-120">0xFFFFFFFF</span></span>  <br/> |
|<span data-ttu-id="d0be6-121">投稿</span><span class="sxs-lookup"><span data-stu-id="d0be6-121">Post</span></span>  <br/> |<span data-ttu-id="d0be6-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d0be6-122">0x00000001</span></span>  <br/> |
|<span data-ttu-id="d0be6-123">その他</span><span class="sxs-lookup"><span data-stu-id="d0be6-123">Other</span></span>  <br/> |<span data-ttu-id="d0be6-124">0x00000003</span><span class="sxs-lookup"><span data-stu-id="d0be6-124">0x00000003</span></span>  <br/> |
|<span data-ttu-id="d0be6-125">メールを読む</span><span class="sxs-lookup"><span data-stu-id="d0be6-125">Read mail</span></span>  <br/> |<span data-ttu-id="d0be6-126">0x00000100</span><span class="sxs-lookup"><span data-stu-id="d0be6-126">0x00000100</span></span>  <br/> |
|<span data-ttu-id="d0be6-127">未読メ ー ル</span><span class="sxs-lookup"><span data-stu-id="d0be6-127">Unread mail</span></span>  <br/> |<span data-ttu-id="d0be6-128">0x00000101</span><span class="sxs-lookup"><span data-stu-id="d0be6-128">0x00000101</span></span>  <br/> |
|<span data-ttu-id="d0be6-129">送信されたメール</span><span class="sxs-lookup"><span data-stu-id="d0be6-129">Submitted mail</span></span>  <br/> |<span data-ttu-id="d0be6-130">0x00000102</span><span class="sxs-lookup"><span data-stu-id="d0be6-130">0x00000102</span></span>  <br/> |
|<span data-ttu-id="d0be6-131">未送信メール</span><span class="sxs-lookup"><span data-stu-id="d0be6-131">Unsent mail</span></span>  <br/> |<span data-ttu-id="d0be6-132">0x00000103</span><span class="sxs-lookup"><span data-stu-id="d0be6-132">0x00000103</span></span>  <br/> |
|<span data-ttu-id="d0be6-133">受信メール</span><span class="sxs-lookup"><span data-stu-id="d0be6-133">Receipt mail</span></span>  <br/> |<span data-ttu-id="d0be6-134">0x00000104</span><span class="sxs-lookup"><span data-stu-id="d0be6-134">0x00000104</span></span>  <br/> |
|<span data-ttu-id="d0be6-135">返信メール</span><span class="sxs-lookup"><span data-stu-id="d0be6-135">Replied mail</span></span>  <br/> |<span data-ttu-id="d0be6-136">0x00000105</span><span class="sxs-lookup"><span data-stu-id="d0be6-136">0x00000105</span></span>  <br/> |
|<span data-ttu-id="d0be6-137">転送されたメール</span><span class="sxs-lookup"><span data-stu-id="d0be6-137">Forwarded mail</span></span>  <br/> |<span data-ttu-id="d0be6-138">0x00000106</span><span class="sxs-lookup"><span data-stu-id="d0be6-138">0x00000106</span></span>  <br/> |
|<span data-ttu-id="d0be6-139">リモート メール</span><span class="sxs-lookup"><span data-stu-id="d0be6-139">Remote mail</span></span>  <br/> |<span data-ttu-id="d0be6-140">0x00000107</span><span class="sxs-lookup"><span data-stu-id="d0be6-140">0x00000107</span></span>  <br/> |
|<span data-ttu-id="d0be6-141">メールの配信</span><span class="sxs-lookup"><span data-stu-id="d0be6-141">Delivery mail</span></span>  <br/> |<span data-ttu-id="d0be6-142">0x00000108</span><span class="sxs-lookup"><span data-stu-id="d0be6-142">0x00000108</span></span>  <br/> |
|<span data-ttu-id="d0be6-143">メールを読む</span><span class="sxs-lookup"><span data-stu-id="d0be6-143">Read mail</span></span>  <br/> |<span data-ttu-id="d0be6-144">0x00000109</span><span class="sxs-lookup"><span data-stu-id="d0be6-144">0x00000109</span></span>  <br/> |
|<span data-ttu-id="d0be6-145">配信不能メール</span><span class="sxs-lookup"><span data-stu-id="d0be6-145">Nondelivery mail</span></span>  <br/> |<span data-ttu-id="d0be6-146">0x0000010A</span><span class="sxs-lookup"><span data-stu-id="d0be6-146">0x0000010A</span></span>  <br/> |
|<span data-ttu-id="d0be6-147">Nonread メール</span><span class="sxs-lookup"><span data-stu-id="d0be6-147">Nonread mail</span></span>  <br/> |<span data-ttu-id="d0be6-148">0x0000010B</span><span class="sxs-lookup"><span data-stu-id="d0be6-148">0x0000010B</span></span>  <br/> |
|<span data-ttu-id="d0be6-149">Recall_S メール</span><span class="sxs-lookup"><span data-stu-id="d0be6-149">Recall_S mail</span></span>  <br/> |<span data-ttu-id="d0be6-150">0x0000010C</span><span class="sxs-lookup"><span data-stu-id="d0be6-150">0x0000010C</span></span>  <br/> |
|<span data-ttu-id="d0be6-151">Recall_F メール</span><span class="sxs-lookup"><span data-stu-id="d0be6-151">Recall_F mail</span></span>  <br/> |<span data-ttu-id="d0be6-152">0x0000010D</span><span class="sxs-lookup"><span data-stu-id="d0be6-152">0x0000010D</span></span>  <br/> |
|<span data-ttu-id="d0be6-153">メールの追跡</span><span class="sxs-lookup"><span data-stu-id="d0be6-153">Tracking mail</span></span>  <br/> |<span data-ttu-id="d0be6-154">0x0000010E</span><span class="sxs-lookup"><span data-stu-id="d0be6-154">0x0000010E</span></span>  <br/> |
|<span data-ttu-id="d0be6-155">Office メールから</span><span class="sxs-lookup"><span data-stu-id="d0be6-155">Out of office mail</span></span>  <br/> |<span data-ttu-id="d0be6-156">0x0000011B</span><span class="sxs-lookup"><span data-stu-id="d0be6-156">0x0000011B</span></span>  <br/> |
|<span data-ttu-id="d0be6-157">メールを取り消し</span><span class="sxs-lookup"><span data-stu-id="d0be6-157">Recall mail</span></span>  <br/> |<span data-ttu-id="d0be6-158">0x0000011C</span><span class="sxs-lookup"><span data-stu-id="d0be6-158">0x0000011C</span></span>  <br/> |
|<span data-ttu-id="d0be6-159">メッセージの追跡</span><span class="sxs-lookup"><span data-stu-id="d0be6-159">Tracked mail</span></span>  <br/> |<span data-ttu-id="d0be6-160">0x00000130</span><span class="sxs-lookup"><span data-stu-id="d0be6-160">0x00000130</span></span>  <br/> |
|<span data-ttu-id="d0be6-161">Contact</span><span class="sxs-lookup"><span data-stu-id="d0be6-161">Contact</span></span>  <br/> |<span data-ttu-id="d0be6-162">0x00000200</span><span class="sxs-lookup"><span data-stu-id="d0be6-162">0x00000200</span></span>  <br/> |
|<span data-ttu-id="d0be6-163">配布リスト</span><span class="sxs-lookup"><span data-stu-id="d0be6-163">Distribution list</span></span>  <br/> |<span data-ttu-id="d0be6-164">0x00000202</span><span class="sxs-lookup"><span data-stu-id="d0be6-164">0x00000202</span></span>  <br/> |
|<span data-ttu-id="d0be6-165">付箋の青</span><span class="sxs-lookup"><span data-stu-id="d0be6-165">Sticky note blue</span></span>  <br/> |<span data-ttu-id="d0be6-166">0x00000300</span><span class="sxs-lookup"><span data-stu-id="d0be6-166">0x00000300</span></span>  <br/> |
|<span data-ttu-id="d0be6-167">付箋緑</span><span class="sxs-lookup"><span data-stu-id="d0be6-167">Sticky note green</span></span>  <br/> |<span data-ttu-id="d0be6-168">0x00000301</span><span class="sxs-lookup"><span data-stu-id="d0be6-168">0x00000301</span></span>  <br/> |
|<span data-ttu-id="d0be6-169">付箋ピンク</span><span class="sxs-lookup"><span data-stu-id="d0be6-169">Sticky note pink</span></span>  <br/> |<span data-ttu-id="d0be6-170">0x00000302</span><span class="sxs-lookup"><span data-stu-id="d0be6-170">0x00000302</span></span>  <br/> |
|<span data-ttu-id="d0be6-171">付箋イエロー</span><span class="sxs-lookup"><span data-stu-id="d0be6-171">Sticky note yellow</span></span>  <br/> |<span data-ttu-id="d0be6-172">0x00000303</span><span class="sxs-lookup"><span data-stu-id="d0be6-172">0x00000303</span></span>  <br/> |
|<span data-ttu-id="d0be6-173">付箋ホワイト</span><span class="sxs-lookup"><span data-stu-id="d0be6-173">Sticky note white</span></span>  <br/> |<span data-ttu-id="d0be6-174">0x00000304</span><span class="sxs-lookup"><span data-stu-id="d0be6-174">0x00000304</span></span>  <br/> |
|<span data-ttu-id="d0be6-175">単独の予定</span><span class="sxs-lookup"><span data-stu-id="d0be6-175">Single instance appointment</span></span>  <br/> |<span data-ttu-id="d0be6-176">0x00000400</span><span class="sxs-lookup"><span data-stu-id="d0be6-176">0x00000400</span></span>  <br/> |
|<span data-ttu-id="d0be6-177">定期的な予定</span><span class="sxs-lookup"><span data-stu-id="d0be6-177">Recurring appointment</span></span>  <br/> |<span data-ttu-id="d0be6-178">0x00000401</span><span class="sxs-lookup"><span data-stu-id="d0be6-178">0x00000401</span></span>  <br/> |
|<span data-ttu-id="d0be6-179">単一インスタンスの会議</span><span class="sxs-lookup"><span data-stu-id="d0be6-179">Single instance meeting</span></span>  <br/> |<span data-ttu-id="d0be6-180">0x00000402</span><span class="sxs-lookup"><span data-stu-id="d0be6-180">0x00000402</span></span>  <br/> |
|<span data-ttu-id="d0be6-181">定期的な会議</span><span class="sxs-lookup"><span data-stu-id="d0be6-181">Recurring meeting</span></span>  <br/> |<span data-ttu-id="d0be6-182">0x00000403</span><span class="sxs-lookup"><span data-stu-id="d0be6-182">0x00000403</span></span>  <br/> |
|<span data-ttu-id="d0be6-183">会議出席依頼</span><span class="sxs-lookup"><span data-stu-id="d0be6-183">Meeting request</span></span>  <br/> |<span data-ttu-id="d0be6-184">0x00000404</span><span class="sxs-lookup"><span data-stu-id="d0be6-184">0x00000404</span></span>  <br/> |
|<span data-ttu-id="d0be6-185">Accept</span><span class="sxs-lookup"><span data-stu-id="d0be6-185">Accept</span></span>  <br/> |<span data-ttu-id="d0be6-186">0x00000405</span><span class="sxs-lookup"><span data-stu-id="d0be6-186">0x00000405</span></span>  <br/> |
|<span data-ttu-id="d0be6-187">辞退</span><span class="sxs-lookup"><span data-stu-id="d0be6-187">Decline</span></span>  <br/> |<span data-ttu-id="d0be6-188">0x00000406</span><span class="sxs-lookup"><span data-stu-id="d0be6-188">0x00000406</span></span>  <br/> |
|<span data-ttu-id="d0be6-189">Tentativly</span><span class="sxs-lookup"><span data-stu-id="d0be6-189">Tentativly</span></span>  <br/> |<span data-ttu-id="d0be6-190">0x00000407</span><span class="sxs-lookup"><span data-stu-id="d0be6-190">0x00000407</span></span>  <br/> |
|<span data-ttu-id="d0be6-191">キャンセル</span><span class="sxs-lookup"><span data-stu-id="d0be6-191">Cancellation</span></span>  <br/> |<span data-ttu-id="d0be6-192">0x00000408</span><span class="sxs-lookup"><span data-stu-id="d0be6-192">0x00000408</span></span>  <br/> |
|<span data-ttu-id="d0be6-193">更新された情報</span><span class="sxs-lookup"><span data-stu-id="d0be6-193">Informational update</span></span>  <br/> |<span data-ttu-id="d0be6-194">0x00000409</span><span class="sxs-lookup"><span data-stu-id="d0be6-194">0x00000409</span></span>  <br/> |
|<span data-ttu-id="d0be6-195">タスクとタスク</span><span class="sxs-lookup"><span data-stu-id="d0be6-195">Task/task</span></span>  <br/> |<span data-ttu-id="d0be6-196">0x00000500</span><span class="sxs-lookup"><span data-stu-id="d0be6-196">0x00000500</span></span>  <br/> |
|<span data-ttu-id="d0be6-197">定期的なタスクが割り当てられていません。</span><span class="sxs-lookup"><span data-stu-id="d0be6-197">Unassigned recurring task</span></span>  <br/> |<span data-ttu-id="d0be6-198">0x00000501</span><span class="sxs-lookup"><span data-stu-id="d0be6-198">0x00000501</span></span>  <br/> |
|<span data-ttu-id="d0be6-199">担当者のタスク</span><span class="sxs-lookup"><span data-stu-id="d0be6-199">Assignee's task</span></span>  <br/> |<span data-ttu-id="d0be6-200">0x00000502</span><span class="sxs-lookup"><span data-stu-id="d0be6-200">0x00000502</span></span>  <br/> |
|<span data-ttu-id="d0be6-201">仕事を割り当てた人の作業</span><span class="sxs-lookup"><span data-stu-id="d0be6-201">Assigner's task</span></span>  <br/> |<span data-ttu-id="d0be6-202">0x00000503</span><span class="sxs-lookup"><span data-stu-id="d0be6-202">0x00000503</span></span>  <br/> |
|<span data-ttu-id="d0be6-203">仕事の依頼</span><span class="sxs-lookup"><span data-stu-id="d0be6-203">Task request</span></span>  <br/> |<span data-ttu-id="d0be6-204">0x00000504</span><span class="sxs-lookup"><span data-stu-id="d0be6-204">0x00000504</span></span>  <br/> |
|<span data-ttu-id="d0be6-205">仕事の承諾</span><span class="sxs-lookup"><span data-stu-id="d0be6-205">Task acceptance</span></span>  <br/> |<span data-ttu-id="d0be6-206">0x00000505</span><span class="sxs-lookup"><span data-stu-id="d0be6-206">0x00000505</span></span>  <br/> |
|<span data-ttu-id="d0be6-207">タスクの辞退</span><span class="sxs-lookup"><span data-stu-id="d0be6-207">Task rejection</span></span>  <br/> |<span data-ttu-id="d0be6-208">0x00000506</span><span class="sxs-lookup"><span data-stu-id="d0be6-208">0x00000506</span></span>  <br/> |
|<span data-ttu-id="d0be6-209">仕訳帳の会話</span><span class="sxs-lookup"><span data-stu-id="d0be6-209">Journal conversation</span></span>  <br/> |<span data-ttu-id="d0be6-210">0x00000601</span><span class="sxs-lookup"><span data-stu-id="d0be6-210">0x00000601</span></span>  <br/> |
|<span data-ttu-id="d0be6-211">ジャーナルの電子メール メッセージ</span><span class="sxs-lookup"><span data-stu-id="d0be6-211">Journal email message</span></span>  <br/> |<span data-ttu-id="d0be6-212">0x00000602</span><span class="sxs-lookup"><span data-stu-id="d0be6-212">0x00000602</span></span>  <br/> |
|<span data-ttu-id="d0be6-213">仕訳帳の会議出席依頼</span><span class="sxs-lookup"><span data-stu-id="d0be6-213">Journal meeting request</span></span>  <br/> |<span data-ttu-id="d0be6-214">0x00000603</span><span class="sxs-lookup"><span data-stu-id="d0be6-214">0x00000603</span></span>  <br/> |
|<span data-ttu-id="d0be6-215">仕訳帳の会議の応答</span><span class="sxs-lookup"><span data-stu-id="d0be6-215">Journal meeting response</span></span>  <br/> |<span data-ttu-id="d0be6-216">0x00000604</span><span class="sxs-lookup"><span data-stu-id="d0be6-216">0x00000604</span></span>  <br/> |
|<span data-ttu-id="d0be6-217">仕訳帳の仕事の依頼</span><span class="sxs-lookup"><span data-stu-id="d0be6-217">Journal task request</span></span>  <br/> |<span data-ttu-id="d0be6-218">0x00000606</span><span class="sxs-lookup"><span data-stu-id="d0be6-218">0x00000606</span></span>  <br/> |
|<span data-ttu-id="d0be6-219">仕訳帳のタスクの応答</span><span class="sxs-lookup"><span data-stu-id="d0be6-219">Journal task response</span></span>  <br/> |<span data-ttu-id="d0be6-220">0x00000607</span><span class="sxs-lookup"><span data-stu-id="d0be6-220">0x00000607</span></span>  <br/> |
|<span data-ttu-id="d0be6-221">Journal ノート</span><span class="sxs-lookup"><span data-stu-id="d0be6-221">Journal note</span></span>  <br/> |<span data-ttu-id="d0be6-222">0x00000608</span><span class="sxs-lookup"><span data-stu-id="d0be6-222">0x00000608</span></span>  <br/> |
|<span data-ttu-id="d0be6-223">仕訳帳の fax</span><span class="sxs-lookup"><span data-stu-id="d0be6-223">Journal fax</span></span>  <br/> |<span data-ttu-id="d0be6-224">0x00000609</span><span class="sxs-lookup"><span data-stu-id="d0be6-224">0x00000609</span></span>  <br/> |
|<span data-ttu-id="d0be6-225">仕訳帳の電話</span><span class="sxs-lookup"><span data-stu-id="d0be6-225">Journal phone call</span></span>  <br/> |<span data-ttu-id="d0be6-226">0x0000060A</span><span class="sxs-lookup"><span data-stu-id="d0be6-226">0x0000060A</span></span>  <br/> |
|<span data-ttu-id="d0be6-227">仕訳帳名</span><span class="sxs-lookup"><span data-stu-id="d0be6-227">Journal letter</span></span>  <br/> |<span data-ttu-id="d0be6-228">0x0000060C</span><span class="sxs-lookup"><span data-stu-id="d0be6-228">0x0000060C</span></span>  <br/> |
|<span data-ttu-id="d0be6-229">Microsoft Office Word の仕訳帳</span><span class="sxs-lookup"><span data-stu-id="d0be6-229">Journal Microsoft Office Word</span></span>  <br/> |<span data-ttu-id="d0be6-230">0x0000060D</span><span class="sxs-lookup"><span data-stu-id="d0be6-230">0x0000060D</span></span>  <br/> |
|<span data-ttu-id="d0be6-231">Microsoft Office Excel の仕訳帳</span><span class="sxs-lookup"><span data-stu-id="d0be6-231">Journal Microsoft Office Excel</span></span>  <br/> |<span data-ttu-id="d0be6-232">0x0000060E</span><span class="sxs-lookup"><span data-stu-id="d0be6-232">0x0000060E</span></span>  <br/> |
|<span data-ttu-id="d0be6-233">Microsoft Office PowerPoint の仕訳帳</span><span class="sxs-lookup"><span data-stu-id="d0be6-233">Journal Microsoft Office PowerPoint</span></span>  <br/> |<span data-ttu-id="d0be6-234">0x0000060F</span><span class="sxs-lookup"><span data-stu-id="d0be6-234">0x0000060F</span></span>  <br/> |
|<span data-ttu-id="d0be6-235">仕訳帳の Microsoft Office のアクセス</span><span class="sxs-lookup"><span data-stu-id="d0be6-235">Journal Microsoft Office Access</span></span>  <br/> |<span data-ttu-id="d0be6-236">0x00000610</span><span class="sxs-lookup"><span data-stu-id="d0be6-236">0x00000610</span></span>  <br/> |
|<span data-ttu-id="d0be6-237">仕訳帳文書</span><span class="sxs-lookup"><span data-stu-id="d0be6-237">Journal document</span></span>  <br/> |<span data-ttu-id="d0be6-238">0x00000612</span><span class="sxs-lookup"><span data-stu-id="d0be6-238">0x00000612</span></span>  <br/> |
|<span data-ttu-id="d0be6-239">仕訳帳の会議</span><span class="sxs-lookup"><span data-stu-id="d0be6-239">Journal meeting</span></span>  <br/> |<span data-ttu-id="d0be6-240">0x00000613</span><span class="sxs-lookup"><span data-stu-id="d0be6-240">0x00000613</span></span>  <br/> |
|<span data-ttu-id="d0be6-241">仕訳帳の会議の取り消し</span><span class="sxs-lookup"><span data-stu-id="d0be6-241">Journal meeting cancellation</span></span>  <br/> |<span data-ttu-id="d0be6-242">0x00000614</span><span class="sxs-lookup"><span data-stu-id="d0be6-242">0x00000614</span></span>  <br/> |
|<span data-ttu-id="d0be6-243">仕訳帳のリモート セッション</span><span class="sxs-lookup"><span data-stu-id="d0be6-243">Journal remote session</span></span>  <br/> |<span data-ttu-id="d0be6-244">0x00000615</span><span class="sxs-lookup"><span data-stu-id="d0be6-244">0x00000615</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="d0be6-245">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d0be6-245">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d0be6-246">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="d0be6-246">Protocol specifications</span></span>

<span data-ttu-id="d0be6-247">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d0be6-247">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d0be6-248">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="d0be6-248">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d0be6-249">[[MS OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d0be6-249">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d0be6-250">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="d0be6-250">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="d0be6-251">[[MS OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d0be6-251">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d0be6-252">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="d0be6-252">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="d0be6-253">[[MS OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d0be6-253">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d0be6-254">連絡先と個人用配布リストで許可されている操作のプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="d0be6-254">Specifies the properties and operations that are permissible on contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d0be6-255">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="d0be6-255">Header files</span></span>

<span data-ttu-id="d0be6-256">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d0be6-256">Mapidefs.h</span></span>
  
> <span data-ttu-id="d0be6-257">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d0be6-257">Provides data type definitions.</span></span>
    
<span data-ttu-id="d0be6-258">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d0be6-258">Mapitags.h</span></span>
  
> <span data-ttu-id="d0be6-259">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d0be6-259">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d0be6-260">関連項目</span><span class="sxs-lookup"><span data-stu-id="d0be6-260">See also</span></span>



[<span data-ttu-id="d0be6-261">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="d0be6-261">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d0be6-262">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="d0be6-262">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d0be6-263">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d0be6-263">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d0be6-264">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d0be6-264">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

