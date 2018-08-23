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
ms.openlocfilehash: 03465df65498643ce02598fdc26ab78b44e1135a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588679"
---
# <a name="pidtagiconindex-canonical-property"></a><span data-ttu-id="43463-103">PidTagIconIndex 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="43463-103">PidTagIconIndex Canonical Property</span></span>

  
  
<span data-ttu-id="43463-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="43463-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="43463-105">電子メールのオブジェクトのグループを表示するときに使用するアイコンを表す数字が含まれています。</span><span class="sxs-lookup"><span data-stu-id="43463-105">Contains a number that indicates which icon to use when you display a group of email objects.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="43463-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="43463-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="43463-107">PR_ICON_INDEX</span><span class="sxs-lookup"><span data-stu-id="43463-107">PR_ICON_INDEX</span></span>  <br/> |
|<span data-ttu-id="43463-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="43463-108">Identifier:</span></span>  <br/> |<span data-ttu-id="43463-109">0x1080</span><span class="sxs-lookup"><span data-stu-id="43463-109">0x1080</span></span>  <br/> |
|<span data-ttu-id="43463-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="43463-110">Data type:</span></span>  <br/> |<span data-ttu-id="43463-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="43463-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="43463-112">領域:</span><span class="sxs-lookup"><span data-stu-id="43463-112">Area:</span></span>  <br/> |<span data-ttu-id="43463-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="43463-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="43463-114">注釈</span><span class="sxs-lookup"><span data-stu-id="43463-114">Remarks</span></span>

<span data-ttu-id="43463-115">このプロパティは、存在する場合は、クライアントへのヒントです。</span><span class="sxs-lookup"><span data-stu-id="43463-115">This property, if it exists, is a hint to the client.</span></span> <span data-ttu-id="43463-116">クライアントは、このプロパティの値を無視することがあります。</span><span class="sxs-lookup"><span data-stu-id="43463-116">The client may ignore the value of this property.</span></span> 
  
|<span data-ttu-id="43463-117">**メール アイテムの状態**</span><span class="sxs-lookup"><span data-stu-id="43463-117">**Mail item state**</span></span>|<span data-ttu-id="43463-118">**アイコンのインデックス**</span><span class="sxs-lookup"><span data-stu-id="43463-118">**Icon Index**</span></span>|
|:-----|:-----|
|<span data-ttu-id="43463-119">新着メール</span><span class="sxs-lookup"><span data-stu-id="43463-119">New mail</span></span>  <br/> |<span data-ttu-id="43463-120">0 xffffffff</span><span class="sxs-lookup"><span data-stu-id="43463-120">0xFFFFFFFF</span></span>  <br/> |
|<span data-ttu-id="43463-121">投稿</span><span class="sxs-lookup"><span data-stu-id="43463-121">Post</span></span>  <br/> |<span data-ttu-id="43463-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="43463-122">0x00000001</span></span>  <br/> |
|<span data-ttu-id="43463-123">その他</span><span class="sxs-lookup"><span data-stu-id="43463-123">Other</span></span>  <br/> |<span data-ttu-id="43463-124">0x00000003</span><span class="sxs-lookup"><span data-stu-id="43463-124">0x00000003</span></span>  <br/> |
|<span data-ttu-id="43463-125">メールを読む</span><span class="sxs-lookup"><span data-stu-id="43463-125">Read mail</span></span>  <br/> |<span data-ttu-id="43463-126">0x00000100</span><span class="sxs-lookup"><span data-stu-id="43463-126">0x00000100</span></span>  <br/> |
|<span data-ttu-id="43463-127">未読メ ー ル</span><span class="sxs-lookup"><span data-stu-id="43463-127">Unread mail</span></span>  <br/> |<span data-ttu-id="43463-128">0x00000101</span><span class="sxs-lookup"><span data-stu-id="43463-128">0x00000101</span></span>  <br/> |
|<span data-ttu-id="43463-129">送信されたメール</span><span class="sxs-lookup"><span data-stu-id="43463-129">Submitted mail</span></span>  <br/> |<span data-ttu-id="43463-130">0x00000102</span><span class="sxs-lookup"><span data-stu-id="43463-130">0x00000102</span></span>  <br/> |
|<span data-ttu-id="43463-131">未送信メール</span><span class="sxs-lookup"><span data-stu-id="43463-131">Unsent mail</span></span>  <br/> |<span data-ttu-id="43463-132">0x00000103</span><span class="sxs-lookup"><span data-stu-id="43463-132">0x00000103</span></span>  <br/> |
|<span data-ttu-id="43463-133">受信メール</span><span class="sxs-lookup"><span data-stu-id="43463-133">Receipt mail</span></span>  <br/> |<span data-ttu-id="43463-134">0x00000104</span><span class="sxs-lookup"><span data-stu-id="43463-134">0x00000104</span></span>  <br/> |
|<span data-ttu-id="43463-135">返信メール</span><span class="sxs-lookup"><span data-stu-id="43463-135">Replied mail</span></span>  <br/> |<span data-ttu-id="43463-136">0x00000105</span><span class="sxs-lookup"><span data-stu-id="43463-136">0x00000105</span></span>  <br/> |
|<span data-ttu-id="43463-137">転送されたメール</span><span class="sxs-lookup"><span data-stu-id="43463-137">Forwarded mail</span></span>  <br/> |<span data-ttu-id="43463-138">0x00000106</span><span class="sxs-lookup"><span data-stu-id="43463-138">0x00000106</span></span>  <br/> |
|<span data-ttu-id="43463-139">リモート メール</span><span class="sxs-lookup"><span data-stu-id="43463-139">Remote mail</span></span>  <br/> |<span data-ttu-id="43463-140">0x00000107</span><span class="sxs-lookup"><span data-stu-id="43463-140">0x00000107</span></span>  <br/> |
|<span data-ttu-id="43463-141">メールの配信</span><span class="sxs-lookup"><span data-stu-id="43463-141">Delivery mail</span></span>  <br/> |<span data-ttu-id="43463-142">0x00000108</span><span class="sxs-lookup"><span data-stu-id="43463-142">0x00000108</span></span>  <br/> |
|<span data-ttu-id="43463-143">メールを読む</span><span class="sxs-lookup"><span data-stu-id="43463-143">Read mail</span></span>  <br/> |<span data-ttu-id="43463-144">0x00000109</span><span class="sxs-lookup"><span data-stu-id="43463-144">0x00000109</span></span>  <br/> |
|<span data-ttu-id="43463-145">配信不能メール</span><span class="sxs-lookup"><span data-stu-id="43463-145">Nondelivery mail</span></span>  <br/> |<span data-ttu-id="43463-146">0x0000010A</span><span class="sxs-lookup"><span data-stu-id="43463-146">0x0000010A</span></span>  <br/> |
|<span data-ttu-id="43463-147">Nonread メール</span><span class="sxs-lookup"><span data-stu-id="43463-147">Nonread mail</span></span>  <br/> |<span data-ttu-id="43463-148">0x0000010B</span><span class="sxs-lookup"><span data-stu-id="43463-148">0x0000010B</span></span>  <br/> |
|<span data-ttu-id="43463-149">Recall_S メール</span><span class="sxs-lookup"><span data-stu-id="43463-149">Recall_S mail</span></span>  <br/> |<span data-ttu-id="43463-150">0x0000010C</span><span class="sxs-lookup"><span data-stu-id="43463-150">0x0000010C</span></span>  <br/> |
|<span data-ttu-id="43463-151">Recall_F メール</span><span class="sxs-lookup"><span data-stu-id="43463-151">Recall_F mail</span></span>  <br/> |<span data-ttu-id="43463-152">0x0000010D</span><span class="sxs-lookup"><span data-stu-id="43463-152">0x0000010D</span></span>  <br/> |
|<span data-ttu-id="43463-153">メールの追跡</span><span class="sxs-lookup"><span data-stu-id="43463-153">Tracking mail</span></span>  <br/> |<span data-ttu-id="43463-154">0x0000010E</span><span class="sxs-lookup"><span data-stu-id="43463-154">0x0000010E</span></span>  <br/> |
|<span data-ttu-id="43463-155">Office メールから</span><span class="sxs-lookup"><span data-stu-id="43463-155">Out of office mail</span></span>  <br/> |<span data-ttu-id="43463-156">0x0000011B</span><span class="sxs-lookup"><span data-stu-id="43463-156">0x0000011B</span></span>  <br/> |
|<span data-ttu-id="43463-157">メールを取り消し</span><span class="sxs-lookup"><span data-stu-id="43463-157">Recall mail</span></span>  <br/> |<span data-ttu-id="43463-158">0x0000011C</span><span class="sxs-lookup"><span data-stu-id="43463-158">0x0000011C</span></span>  <br/> |
|<span data-ttu-id="43463-159">メッセージの追跡</span><span class="sxs-lookup"><span data-stu-id="43463-159">Tracked mail</span></span>  <br/> |<span data-ttu-id="43463-160">0x00000130</span><span class="sxs-lookup"><span data-stu-id="43463-160">0x00000130</span></span>  <br/> |
|<span data-ttu-id="43463-161">Contact</span><span class="sxs-lookup"><span data-stu-id="43463-161">Contact</span></span>  <br/> |<span data-ttu-id="43463-162">0x00000200</span><span class="sxs-lookup"><span data-stu-id="43463-162">0x00000200</span></span>  <br/> |
|<span data-ttu-id="43463-163">配布リスト</span><span class="sxs-lookup"><span data-stu-id="43463-163">Distribution list</span></span>  <br/> |<span data-ttu-id="43463-164">0x00000202</span><span class="sxs-lookup"><span data-stu-id="43463-164">0x00000202</span></span>  <br/> |
|<span data-ttu-id="43463-165">付箋の青</span><span class="sxs-lookup"><span data-stu-id="43463-165">Sticky note blue</span></span>  <br/> |<span data-ttu-id="43463-166">0x00000300</span><span class="sxs-lookup"><span data-stu-id="43463-166">0x00000300</span></span>  <br/> |
|<span data-ttu-id="43463-167">付箋緑</span><span class="sxs-lookup"><span data-stu-id="43463-167">Sticky note green</span></span>  <br/> |<span data-ttu-id="43463-168">0x00000301</span><span class="sxs-lookup"><span data-stu-id="43463-168">0x00000301</span></span>  <br/> |
|<span data-ttu-id="43463-169">付箋ピンク</span><span class="sxs-lookup"><span data-stu-id="43463-169">Sticky note pink</span></span>  <br/> |<span data-ttu-id="43463-170">0x00000302</span><span class="sxs-lookup"><span data-stu-id="43463-170">0x00000302</span></span>  <br/> |
|<span data-ttu-id="43463-171">付箋イエロー</span><span class="sxs-lookup"><span data-stu-id="43463-171">Sticky note yellow</span></span>  <br/> |<span data-ttu-id="43463-172">0x00000303</span><span class="sxs-lookup"><span data-stu-id="43463-172">0x00000303</span></span>  <br/> |
|<span data-ttu-id="43463-173">付箋ホワイト</span><span class="sxs-lookup"><span data-stu-id="43463-173">Sticky note white</span></span>  <br/> |<span data-ttu-id="43463-174">0x00000304</span><span class="sxs-lookup"><span data-stu-id="43463-174">0x00000304</span></span>  <br/> |
|<span data-ttu-id="43463-175">単独の予定</span><span class="sxs-lookup"><span data-stu-id="43463-175">Single instance appointment</span></span>  <br/> |<span data-ttu-id="43463-176">0x00000400</span><span class="sxs-lookup"><span data-stu-id="43463-176">0x00000400</span></span>  <br/> |
|<span data-ttu-id="43463-177">定期的な予定</span><span class="sxs-lookup"><span data-stu-id="43463-177">Recurring appointment</span></span>  <br/> |<span data-ttu-id="43463-178">0x00000401</span><span class="sxs-lookup"><span data-stu-id="43463-178">0x00000401</span></span>  <br/> |
|<span data-ttu-id="43463-179">単一インスタンスの会議</span><span class="sxs-lookup"><span data-stu-id="43463-179">Single instance meeting</span></span>  <br/> |<span data-ttu-id="43463-180">0x00000402</span><span class="sxs-lookup"><span data-stu-id="43463-180">0x00000402</span></span>  <br/> |
|<span data-ttu-id="43463-181">定期的な会議</span><span class="sxs-lookup"><span data-stu-id="43463-181">Recurring meeting</span></span>  <br/> |<span data-ttu-id="43463-182">0x00000403</span><span class="sxs-lookup"><span data-stu-id="43463-182">0x00000403</span></span>  <br/> |
|<span data-ttu-id="43463-183">会議出席依頼</span><span class="sxs-lookup"><span data-stu-id="43463-183">Meeting request</span></span>  <br/> |<span data-ttu-id="43463-184">0x00000404</span><span class="sxs-lookup"><span data-stu-id="43463-184">0x00000404</span></span>  <br/> |
|<span data-ttu-id="43463-185">Accept</span><span class="sxs-lookup"><span data-stu-id="43463-185">Accept</span></span>  <br/> |<span data-ttu-id="43463-186">0x00000405</span><span class="sxs-lookup"><span data-stu-id="43463-186">0x00000405</span></span>  <br/> |
|<span data-ttu-id="43463-187">辞退</span><span class="sxs-lookup"><span data-stu-id="43463-187">Decline</span></span>  <br/> |<span data-ttu-id="43463-188">0x00000406</span><span class="sxs-lookup"><span data-stu-id="43463-188">0x00000406</span></span>  <br/> |
|<span data-ttu-id="43463-189">Tentativly</span><span class="sxs-lookup"><span data-stu-id="43463-189">Tentativly</span></span>  <br/> |<span data-ttu-id="43463-190">0x00000407</span><span class="sxs-lookup"><span data-stu-id="43463-190">0x00000407</span></span>  <br/> |
|<span data-ttu-id="43463-191">キャンセル</span><span class="sxs-lookup"><span data-stu-id="43463-191">Cancellation</span></span>  <br/> |<span data-ttu-id="43463-192">0x00000408</span><span class="sxs-lookup"><span data-stu-id="43463-192">0x00000408</span></span>  <br/> |
|<span data-ttu-id="43463-193">更新された情報</span><span class="sxs-lookup"><span data-stu-id="43463-193">Informational update</span></span>  <br/> |<span data-ttu-id="43463-194">0x00000409</span><span class="sxs-lookup"><span data-stu-id="43463-194">0x00000409</span></span>  <br/> |
|<span data-ttu-id="43463-195">タスクとタスク</span><span class="sxs-lookup"><span data-stu-id="43463-195">Task/task</span></span>  <br/> |<span data-ttu-id="43463-196">0x00000500</span><span class="sxs-lookup"><span data-stu-id="43463-196">0x00000500</span></span>  <br/> |
|<span data-ttu-id="43463-197">定期的なタスクが割り当てられていません。</span><span class="sxs-lookup"><span data-stu-id="43463-197">Unassigned recurring task</span></span>  <br/> |<span data-ttu-id="43463-198">0x00000501</span><span class="sxs-lookup"><span data-stu-id="43463-198">0x00000501</span></span>  <br/> |
|<span data-ttu-id="43463-199">担当者のタスク</span><span class="sxs-lookup"><span data-stu-id="43463-199">Assignee's task</span></span>  <br/> |<span data-ttu-id="43463-200">0x00000502</span><span class="sxs-lookup"><span data-stu-id="43463-200">0x00000502</span></span>  <br/> |
|<span data-ttu-id="43463-201">仕事を割り当てた人の作業</span><span class="sxs-lookup"><span data-stu-id="43463-201">Assigner's task</span></span>  <br/> |<span data-ttu-id="43463-202">0x00000503</span><span class="sxs-lookup"><span data-stu-id="43463-202">0x00000503</span></span>  <br/> |
|<span data-ttu-id="43463-203">仕事の依頼</span><span class="sxs-lookup"><span data-stu-id="43463-203">Task request</span></span>  <br/> |<span data-ttu-id="43463-204">0x00000504</span><span class="sxs-lookup"><span data-stu-id="43463-204">0x00000504</span></span>  <br/> |
|<span data-ttu-id="43463-205">仕事の承諾</span><span class="sxs-lookup"><span data-stu-id="43463-205">Task acceptance</span></span>  <br/> |<span data-ttu-id="43463-206">0x00000505</span><span class="sxs-lookup"><span data-stu-id="43463-206">0x00000505</span></span>  <br/> |
|<span data-ttu-id="43463-207">タスクの辞退</span><span class="sxs-lookup"><span data-stu-id="43463-207">Task rejection</span></span>  <br/> |<span data-ttu-id="43463-208">0x00000506</span><span class="sxs-lookup"><span data-stu-id="43463-208">0x00000506</span></span>  <br/> |
|<span data-ttu-id="43463-209">仕訳帳の会話</span><span class="sxs-lookup"><span data-stu-id="43463-209">Journal conversation</span></span>  <br/> |<span data-ttu-id="43463-210">0x00000601</span><span class="sxs-lookup"><span data-stu-id="43463-210">0x00000601</span></span>  <br/> |
|<span data-ttu-id="43463-211">ジャーナルの電子メール メッセージ</span><span class="sxs-lookup"><span data-stu-id="43463-211">Journal email message</span></span>  <br/> |<span data-ttu-id="43463-212">0x00000602</span><span class="sxs-lookup"><span data-stu-id="43463-212">0x00000602</span></span>  <br/> |
|<span data-ttu-id="43463-213">仕訳帳の会議出席依頼</span><span class="sxs-lookup"><span data-stu-id="43463-213">Journal meeting request</span></span>  <br/> |<span data-ttu-id="43463-214">0x00000603</span><span class="sxs-lookup"><span data-stu-id="43463-214">0x00000603</span></span>  <br/> |
|<span data-ttu-id="43463-215">仕訳帳の会議の応答</span><span class="sxs-lookup"><span data-stu-id="43463-215">Journal meeting response</span></span>  <br/> |<span data-ttu-id="43463-216">0x00000604</span><span class="sxs-lookup"><span data-stu-id="43463-216">0x00000604</span></span>  <br/> |
|<span data-ttu-id="43463-217">仕訳帳の仕事の依頼</span><span class="sxs-lookup"><span data-stu-id="43463-217">Journal task request</span></span>  <br/> |<span data-ttu-id="43463-218">0x00000606</span><span class="sxs-lookup"><span data-stu-id="43463-218">0x00000606</span></span>  <br/> |
|<span data-ttu-id="43463-219">仕訳帳のタスクの応答</span><span class="sxs-lookup"><span data-stu-id="43463-219">Journal task response</span></span>  <br/> |<span data-ttu-id="43463-220">0x00000607</span><span class="sxs-lookup"><span data-stu-id="43463-220">0x00000607</span></span>  <br/> |
|<span data-ttu-id="43463-221">Journal ノート</span><span class="sxs-lookup"><span data-stu-id="43463-221">Journal note</span></span>  <br/> |<span data-ttu-id="43463-222">0x00000608</span><span class="sxs-lookup"><span data-stu-id="43463-222">0x00000608</span></span>  <br/> |
|<span data-ttu-id="43463-223">仕訳帳の fax</span><span class="sxs-lookup"><span data-stu-id="43463-223">Journal fax</span></span>  <br/> |<span data-ttu-id="43463-224">0x00000609</span><span class="sxs-lookup"><span data-stu-id="43463-224">0x00000609</span></span>  <br/> |
|<span data-ttu-id="43463-225">仕訳帳の電話</span><span class="sxs-lookup"><span data-stu-id="43463-225">Journal phone call</span></span>  <br/> |<span data-ttu-id="43463-226">0x0000060A</span><span class="sxs-lookup"><span data-stu-id="43463-226">0x0000060A</span></span>  <br/> |
|<span data-ttu-id="43463-227">仕訳帳名</span><span class="sxs-lookup"><span data-stu-id="43463-227">Journal letter</span></span>  <br/> |<span data-ttu-id="43463-228">0x0000060C</span><span class="sxs-lookup"><span data-stu-id="43463-228">0x0000060C</span></span>  <br/> |
|<span data-ttu-id="43463-229">Microsoft Office Word の仕訳帳</span><span class="sxs-lookup"><span data-stu-id="43463-229">Journal Microsoft Office Word</span></span>  <br/> |<span data-ttu-id="43463-230">0x0000060D</span><span class="sxs-lookup"><span data-stu-id="43463-230">0x0000060D</span></span>  <br/> |
|<span data-ttu-id="43463-231">Microsoft Office Excel の仕訳帳</span><span class="sxs-lookup"><span data-stu-id="43463-231">Journal Microsoft Office Excel</span></span>  <br/> |<span data-ttu-id="43463-232">0x0000060E</span><span class="sxs-lookup"><span data-stu-id="43463-232">0x0000060E</span></span>  <br/> |
|<span data-ttu-id="43463-233">Microsoft Office PowerPoint の仕訳帳</span><span class="sxs-lookup"><span data-stu-id="43463-233">Journal Microsoft Office PowerPoint</span></span>  <br/> |<span data-ttu-id="43463-234">0x0000060F</span><span class="sxs-lookup"><span data-stu-id="43463-234">0x0000060F</span></span>  <br/> |
|<span data-ttu-id="43463-235">仕訳帳の Microsoft Office のアクセス</span><span class="sxs-lookup"><span data-stu-id="43463-235">Journal Microsoft Office Access</span></span>  <br/> |<span data-ttu-id="43463-236">0x00000610</span><span class="sxs-lookup"><span data-stu-id="43463-236">0x00000610</span></span>  <br/> |
|<span data-ttu-id="43463-237">仕訳帳文書</span><span class="sxs-lookup"><span data-stu-id="43463-237">Journal document</span></span>  <br/> |<span data-ttu-id="43463-238">0x00000612</span><span class="sxs-lookup"><span data-stu-id="43463-238">0x00000612</span></span>  <br/> |
|<span data-ttu-id="43463-239">仕訳帳の会議</span><span class="sxs-lookup"><span data-stu-id="43463-239">Journal meeting</span></span>  <br/> |<span data-ttu-id="43463-240">0x00000613</span><span class="sxs-lookup"><span data-stu-id="43463-240">0x00000613</span></span>  <br/> |
|<span data-ttu-id="43463-241">仕訳帳の会議の取り消し</span><span class="sxs-lookup"><span data-stu-id="43463-241">Journal meeting cancellation</span></span>  <br/> |<span data-ttu-id="43463-242">0x00000614</span><span class="sxs-lookup"><span data-stu-id="43463-242">0x00000614</span></span>  <br/> |
|<span data-ttu-id="43463-243">仕訳帳のリモート セッション</span><span class="sxs-lookup"><span data-stu-id="43463-243">Journal remote session</span></span>  <br/> |<span data-ttu-id="43463-244">0x00000615</span><span class="sxs-lookup"><span data-stu-id="43463-244">0x00000615</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="43463-245">関連リソース</span><span class="sxs-lookup"><span data-stu-id="43463-245">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="43463-246">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="43463-246">Protocol specifications</span></span>

<span data-ttu-id="43463-247">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="43463-247">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="43463-248">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="43463-248">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="43463-249">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="43463-249">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="43463-250">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="43463-250">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="43463-251">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="43463-251">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="43463-252">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="43463-252">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="43463-253">[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="43463-253">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="43463-254">連絡先と個人用配布リストで許可されている操作のプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="43463-254">Specifies the properties and operations that are permissible on contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="43463-255">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="43463-255">Header files</span></span>

<span data-ttu-id="43463-256">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="43463-256">Mapidefs.h</span></span>
  
> <span data-ttu-id="43463-257">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="43463-257">Provides data type definitions.</span></span>
    
<span data-ttu-id="43463-258">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="43463-258">Mapitags.h</span></span>
  
> <span data-ttu-id="43463-259">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="43463-259">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="43463-260">関連項目</span><span class="sxs-lookup"><span data-stu-id="43463-260">See also</span></span>



[<span data-ttu-id="43463-261">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="43463-261">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="43463-262">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="43463-262">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="43463-263">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="43463-263">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="43463-264">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="43463-264">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

