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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346621"
---
# <a name="pidtagiconindex-canonical-property"></a><span data-ttu-id="07835-103">PidTagIconIndex 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="07835-103">PidTagIconIndex Canonical Property</span></span>

  
  
<span data-ttu-id="07835-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="07835-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="07835-105">電子メールオブジェクトのグループを表示するときに使用するアイコンを示す番号を格納します。</span><span class="sxs-lookup"><span data-stu-id="07835-105">Contains a number that indicates which icon to use when you display a group of email objects.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="07835-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="07835-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="07835-107">PR_ICON_INDEX</span><span class="sxs-lookup"><span data-stu-id="07835-107">PR_ICON_INDEX</span></span>  <br/> |
|<span data-ttu-id="07835-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="07835-108">Identifier:</span></span>  <br/> |<span data-ttu-id="07835-109">0x1080</span><span class="sxs-lookup"><span data-stu-id="07835-109">0x1080</span></span>  <br/> |
|<span data-ttu-id="07835-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="07835-110">Data type:</span></span>  <br/> |<span data-ttu-id="07835-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="07835-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="07835-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="07835-112">Area:</span></span>  <br/> |<span data-ttu-id="07835-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="07835-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="07835-114">解説</span><span class="sxs-lookup"><span data-stu-id="07835-114">Remarks</span></span>

<span data-ttu-id="07835-115">このプロパティは、存在する場合、クライアントに対するヒントです。</span><span class="sxs-lookup"><span data-stu-id="07835-115">This property, if it exists, is a hint to the client.</span></span> <span data-ttu-id="07835-116">クライアントは、このプロパティの値を無視することができます。</span><span class="sxs-lookup"><span data-stu-id="07835-116">The client may ignore the value of this property.</span></span> 
  
|<span data-ttu-id="07835-117">**メールアイテムの状態**</span><span class="sxs-lookup"><span data-stu-id="07835-117">**Mail item state**</span></span>|<span data-ttu-id="07835-118">**アイコンのインデックス**</span><span class="sxs-lookup"><span data-stu-id="07835-118">**Icon Index**</span></span>|
|:-----|:-----|
|<span data-ttu-id="07835-119">新しいメール</span><span class="sxs-lookup"><span data-stu-id="07835-119">New mail</span></span>  <br/> |<span data-ttu-id="07835-120">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="07835-120">0xFFFFFFFF</span></span>  <br/> |
|<span data-ttu-id="07835-121">投稿</span><span class="sxs-lookup"><span data-stu-id="07835-121">Post</span></span>  <br/> |<span data-ttu-id="07835-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="07835-122">0x00000001</span></span>  <br/> |
|<span data-ttu-id="07835-123">その他</span><span class="sxs-lookup"><span data-stu-id="07835-123">Other</span></span>  <br/> |<span data-ttu-id="07835-124">0x00000003</span><span class="sxs-lookup"><span data-stu-id="07835-124">0x00000003</span></span>  <br/> |
|<span data-ttu-id="07835-125">メールの読み取り</span><span class="sxs-lookup"><span data-stu-id="07835-125">Read mail</span></span>  <br/> |<span data-ttu-id="07835-126">0x00000100</span><span class="sxs-lookup"><span data-stu-id="07835-126">0x00000100</span></span>  <br/> |
|<span data-ttu-id="07835-127">未読メール</span><span class="sxs-lookup"><span data-stu-id="07835-127">Unread mail</span></span>  <br/> |<span data-ttu-id="07835-128">0x00000101</span><span class="sxs-lookup"><span data-stu-id="07835-128">0x00000101</span></span>  <br/> |
|<span data-ttu-id="07835-129">送信されたメール</span><span class="sxs-lookup"><span data-stu-id="07835-129">Submitted mail</span></span>  <br/> |<span data-ttu-id="07835-130">0x00000102</span><span class="sxs-lookup"><span data-stu-id="07835-130">0x00000102</span></span>  <br/> |
|<span data-ttu-id="07835-131">未送信メール</span><span class="sxs-lookup"><span data-stu-id="07835-131">Unsent mail</span></span>  <br/> |<span data-ttu-id="07835-132">0x00000103</span><span class="sxs-lookup"><span data-stu-id="07835-132">0x00000103</span></span>  <br/> |
|<span data-ttu-id="07835-133">受信メール</span><span class="sxs-lookup"><span data-stu-id="07835-133">Receipt mail</span></span>  <br/> |<span data-ttu-id="07835-134">0x00000104</span><span class="sxs-lookup"><span data-stu-id="07835-134">0x00000104</span></span>  <br/> |
|<span data-ttu-id="07835-135">返信済みメール</span><span class="sxs-lookup"><span data-stu-id="07835-135">Replied mail</span></span>  <br/> |<span data-ttu-id="07835-136">0x00000105</span><span class="sxs-lookup"><span data-stu-id="07835-136">0x00000105</span></span>  <br/> |
|<span data-ttu-id="07835-137">転送されたメール</span><span class="sxs-lookup"><span data-stu-id="07835-137">Forwarded mail</span></span>  <br/> |<span data-ttu-id="07835-138">0x00000106</span><span class="sxs-lookup"><span data-stu-id="07835-138">0x00000106</span></span>  <br/> |
|<span data-ttu-id="07835-139">リモートメール</span><span class="sxs-lookup"><span data-stu-id="07835-139">Remote mail</span></span>  <br/> |<span data-ttu-id="07835-140">0x00000107</span><span class="sxs-lookup"><span data-stu-id="07835-140">0x00000107</span></span>  <br/> |
|<span data-ttu-id="07835-141">配信メール</span><span class="sxs-lookup"><span data-stu-id="07835-141">Delivery mail</span></span>  <br/> |<span data-ttu-id="07835-142">0x00000108</span><span class="sxs-lookup"><span data-stu-id="07835-142">0x00000108</span></span>  <br/> |
|<span data-ttu-id="07835-143">メールの読み取り</span><span class="sxs-lookup"><span data-stu-id="07835-143">Read mail</span></span>  <br/> |<span data-ttu-id="07835-144">0x00000109</span><span class="sxs-lookup"><span data-stu-id="07835-144">0x00000109</span></span>  <br/> |
|<span data-ttu-id="07835-145">配信不能メール</span><span class="sxs-lookup"><span data-stu-id="07835-145">Nondelivery mail</span></span>  <br/> |<span data-ttu-id="07835-146">0x0000010A</span><span class="sxs-lookup"><span data-stu-id="07835-146">0x0000010A</span></span>  <br/> |
|<span data-ttu-id="07835-147">非開封メール</span><span class="sxs-lookup"><span data-stu-id="07835-147">Nonread mail</span></span>  <br/> |<span data-ttu-id="07835-148">0x0000010B</span><span class="sxs-lookup"><span data-stu-id="07835-148">0x0000010B</span></span>  <br/> |
|<span data-ttu-id="07835-149">Recall_S メール</span><span class="sxs-lookup"><span data-stu-id="07835-149">Recall_S mail</span></span>  <br/> |<span data-ttu-id="07835-150">0x0000010C</span><span class="sxs-lookup"><span data-stu-id="07835-150">0x0000010C</span></span>  <br/> |
|<span data-ttu-id="07835-151">Recall_F メール</span><span class="sxs-lookup"><span data-stu-id="07835-151">Recall_F mail</span></span>  <br/> |<span data-ttu-id="07835-152">0x0000010D</span><span class="sxs-lookup"><span data-stu-id="07835-152">0x0000010D</span></span>  <br/> |
|<span data-ttu-id="07835-153">メールの追跡</span><span class="sxs-lookup"><span data-stu-id="07835-153">Tracking mail</span></span>  <br/> |<span data-ttu-id="07835-154">0x0000010E</span><span class="sxs-lookup"><span data-stu-id="07835-154">0x0000010E</span></span>  <br/> |
|<span data-ttu-id="07835-155">不在時のメール</span><span class="sxs-lookup"><span data-stu-id="07835-155">Out of office mail</span></span>  <br/> |<span data-ttu-id="07835-156">0x0000011b</span><span class="sxs-lookup"><span data-stu-id="07835-156">0x0000011B</span></span>  <br/> |
|<span data-ttu-id="07835-157">メールの取り消し</span><span class="sxs-lookup"><span data-stu-id="07835-157">Recall mail</span></span>  <br/> |<span data-ttu-id="07835-158">0x0000011c</span><span class="sxs-lookup"><span data-stu-id="07835-158">0x0000011C</span></span>  <br/> |
|<span data-ttu-id="07835-159">追跡されたメール</span><span class="sxs-lookup"><span data-stu-id="07835-159">Tracked mail</span></span>  <br/> |<span data-ttu-id="07835-160">0x00000130</span><span class="sxs-lookup"><span data-stu-id="07835-160">0x00000130</span></span>  <br/> |
|<span data-ttu-id="07835-161">連絡先</span><span class="sxs-lookup"><span data-stu-id="07835-161">Contact</span></span>  <br/> |<span data-ttu-id="07835-162">0x00000200</span><span class="sxs-lookup"><span data-stu-id="07835-162">0x00000200</span></span>  <br/> |
|<span data-ttu-id="07835-163">配布リスト</span><span class="sxs-lookup"><span data-stu-id="07835-163">Distribution list</span></span>  <br/> |<span data-ttu-id="07835-164">0x00000202</span><span class="sxs-lookup"><span data-stu-id="07835-164">0x00000202</span></span>  <br/> |
|<span data-ttu-id="07835-165">固定メモ青</span><span class="sxs-lookup"><span data-stu-id="07835-165">Sticky note blue</span></span>  <br/> |<span data-ttu-id="07835-166">0x00000300</span><span class="sxs-lookup"><span data-stu-id="07835-166">0x00000300</span></span>  <br/> |
|<span data-ttu-id="07835-167">固定メモ緑</span><span class="sxs-lookup"><span data-stu-id="07835-167">Sticky note green</span></span>  <br/> |<span data-ttu-id="07835-168">0x00000301</span><span class="sxs-lookup"><span data-stu-id="07835-168">0x00000301</span></span>  <br/> |
|<span data-ttu-id="07835-169">固定メモピンク</span><span class="sxs-lookup"><span data-stu-id="07835-169">Sticky note pink</span></span>  <br/> |<span data-ttu-id="07835-170">0x00000302</span><span class="sxs-lookup"><span data-stu-id="07835-170">0x00000302</span></span>  <br/> |
|<span data-ttu-id="07835-171">固定メモ (黄)</span><span class="sxs-lookup"><span data-stu-id="07835-171">Sticky note yellow</span></span>  <br/> |<span data-ttu-id="07835-172">0x00000303</span><span class="sxs-lookup"><span data-stu-id="07835-172">0x00000303</span></span>  <br/> |
|<span data-ttu-id="07835-173">付箋 (白)</span><span class="sxs-lookup"><span data-stu-id="07835-173">Sticky note white</span></span>  <br/> |<span data-ttu-id="07835-174">0x00000304</span><span class="sxs-lookup"><span data-stu-id="07835-174">0x00000304</span></span>  <br/> |
|<span data-ttu-id="07835-175">単一インスタンスの予定</span><span class="sxs-lookup"><span data-stu-id="07835-175">Single instance appointment</span></span>  <br/> |<span data-ttu-id="07835-176">0x00000400</span><span class="sxs-lookup"><span data-stu-id="07835-176">0x00000400</span></span>  <br/> |
|<span data-ttu-id="07835-177">定期的な予定</span><span class="sxs-lookup"><span data-stu-id="07835-177">Recurring appointment</span></span>  <br/> |<span data-ttu-id="07835-178">0x00000401</span><span class="sxs-lookup"><span data-stu-id="07835-178">0x00000401</span></span>  <br/> |
|<span data-ttu-id="07835-179">シングルインスタンス会議</span><span class="sxs-lookup"><span data-stu-id="07835-179">Single instance meeting</span></span>  <br/> |<span data-ttu-id="07835-180">0x00000402</span><span class="sxs-lookup"><span data-stu-id="07835-180">0x00000402</span></span>  <br/> |
|<span data-ttu-id="07835-181">定期的な会議</span><span class="sxs-lookup"><span data-stu-id="07835-181">Recurring meeting</span></span>  <br/> |<span data-ttu-id="07835-182">0x00000403</span><span class="sxs-lookup"><span data-stu-id="07835-182">0x00000403</span></span>  <br/> |
|<span data-ttu-id="07835-183">会議出席依頼</span><span class="sxs-lookup"><span data-stu-id="07835-183">Meeting request</span></span>  <br/> |<span data-ttu-id="07835-184">0x00000404</span><span class="sxs-lookup"><span data-stu-id="07835-184">0x00000404</span></span>  <br/> |
|<span data-ttu-id="07835-185">承諾</span><span class="sxs-lookup"><span data-stu-id="07835-185">Accept</span></span>  <br/> |<span data-ttu-id="07835-186">0x00000405</span><span class="sxs-lookup"><span data-stu-id="07835-186">0x00000405</span></span>  <br/> |
|<span data-ttu-id="07835-187">同意</span><span class="sxs-lookup"><span data-stu-id="07835-187">Decline</span></span>  <br/> |<span data-ttu-id="07835-188">0x00000406</span><span class="sxs-lookup"><span data-stu-id="07835-188">0x00000406</span></span>  <br/> |
|<span data-ttu-id="07835-189">Tentativly</span><span class="sxs-lookup"><span data-stu-id="07835-189">Tentativly</span></span>  <br/> |<span data-ttu-id="07835-190">0x00000407</span><span class="sxs-lookup"><span data-stu-id="07835-190">0x00000407</span></span>  <br/> |
|<span data-ttu-id="07835-191">取り消し</span><span class="sxs-lookup"><span data-stu-id="07835-191">Cancellation</span></span>  <br/> |<span data-ttu-id="07835-192">0x00000408</span><span class="sxs-lookup"><span data-stu-id="07835-192">0x00000408</span></span>  <br/> |
|<span data-ttu-id="07835-193">情報更新</span><span class="sxs-lookup"><span data-stu-id="07835-193">Informational update</span></span>  <br/> |<span data-ttu-id="07835-194">0x00000409</span><span class="sxs-lookup"><span data-stu-id="07835-194">0x00000409</span></span>  <br/> |
|<span data-ttu-id="07835-195">タスク/タスク</span><span class="sxs-lookup"><span data-stu-id="07835-195">Task/task</span></span>  <br/> |<span data-ttu-id="07835-196">0x00000500</span><span class="sxs-lookup"><span data-stu-id="07835-196">0x00000500</span></span>  <br/> |
|<span data-ttu-id="07835-197">割り当てられていない定期タスク</span><span class="sxs-lookup"><span data-stu-id="07835-197">Unassigned recurring task</span></span>  <br/> |<span data-ttu-id="07835-198">0x00000501</span><span class="sxs-lookup"><span data-stu-id="07835-198">0x00000501</span></span>  <br/> |
|<span data-ttu-id="07835-199">担当者のタスク</span><span class="sxs-lookup"><span data-stu-id="07835-199">Assignee's task</span></span>  <br/> |<span data-ttu-id="07835-200">0x00000502</span><span class="sxs-lookup"><span data-stu-id="07835-200">0x00000502</span></span>  <br/> |
|<span data-ttu-id="07835-201">Assigner のタスク</span><span class="sxs-lookup"><span data-stu-id="07835-201">Assigner's task</span></span>  <br/> |<span data-ttu-id="07835-202">0x00000503</span><span class="sxs-lookup"><span data-stu-id="07835-202">0x00000503</span></span>  <br/> |
|<span data-ttu-id="07835-203">タスクの依頼</span><span class="sxs-lookup"><span data-stu-id="07835-203">Task request</span></span>  <br/> |<span data-ttu-id="07835-204">0x00000504</span><span class="sxs-lookup"><span data-stu-id="07835-204">0x00000504</span></span>  <br/> |
|<span data-ttu-id="07835-205">タスクの承諾</span><span class="sxs-lookup"><span data-stu-id="07835-205">Task acceptance</span></span>  <br/> |<span data-ttu-id="07835-206">0x00000505</span><span class="sxs-lookup"><span data-stu-id="07835-206">0x00000505</span></span>  <br/> |
|<span data-ttu-id="07835-207">タスクの却下</span><span class="sxs-lookup"><span data-stu-id="07835-207">Task rejection</span></span>  <br/> |<span data-ttu-id="07835-208">0x00000506</span><span class="sxs-lookup"><span data-stu-id="07835-208">0x00000506</span></span>  <br/> |
|<span data-ttu-id="07835-209">ジャーナルの会話</span><span class="sxs-lookup"><span data-stu-id="07835-209">Journal conversation</span></span>  <br/> |<span data-ttu-id="07835-210">0x00000601</span><span class="sxs-lookup"><span data-stu-id="07835-210">0x00000601</span></span>  <br/> |
|<span data-ttu-id="07835-211">ジャーナルメールメッセージ</span><span class="sxs-lookup"><span data-stu-id="07835-211">Journal email message</span></span>  <br/> |<span data-ttu-id="07835-212">0x00000602</span><span class="sxs-lookup"><span data-stu-id="07835-212">0x00000602</span></span>  <br/> |
|<span data-ttu-id="07835-213">ジャーナル会議出席依頼</span><span class="sxs-lookup"><span data-stu-id="07835-213">Journal meeting request</span></span>  <br/> |<span data-ttu-id="07835-214">0x00000603</span><span class="sxs-lookup"><span data-stu-id="07835-214">0x00000603</span></span>  <br/> |
|<span data-ttu-id="07835-215">ジャーナル会議の応答</span><span class="sxs-lookup"><span data-stu-id="07835-215">Journal meeting response</span></span>  <br/> |<span data-ttu-id="07835-216">0x00000604</span><span class="sxs-lookup"><span data-stu-id="07835-216">0x00000604</span></span>  <br/> |
|<span data-ttu-id="07835-217">ジャーナルタスクの依頼</span><span class="sxs-lookup"><span data-stu-id="07835-217">Journal task request</span></span>  <br/> |<span data-ttu-id="07835-218">0x00000606</span><span class="sxs-lookup"><span data-stu-id="07835-218">0x00000606</span></span>  <br/> |
|<span data-ttu-id="07835-219">ジャーナルタスクの応答</span><span class="sxs-lookup"><span data-stu-id="07835-219">Journal task response</span></span>  <br/> |<span data-ttu-id="07835-220">0x00000607</span><span class="sxs-lookup"><span data-stu-id="07835-220">0x00000607</span></span>  <br/> |
|<span data-ttu-id="07835-221">ジャーナルメモ</span><span class="sxs-lookup"><span data-stu-id="07835-221">Journal note</span></span>  <br/> |<span data-ttu-id="07835-222">0x00000608</span><span class="sxs-lookup"><span data-stu-id="07835-222">0x00000608</span></span>  <br/> |
|<span data-ttu-id="07835-223">ジャーナル fax</span><span class="sxs-lookup"><span data-stu-id="07835-223">Journal fax</span></span>  <br/> |<span data-ttu-id="07835-224">0x00000609</span><span class="sxs-lookup"><span data-stu-id="07835-224">0x00000609</span></span>  <br/> |
|<span data-ttu-id="07835-225">履歴電話</span><span class="sxs-lookup"><span data-stu-id="07835-225">Journal phone call</span></span>  <br/> |<span data-ttu-id="07835-226">0x0000060a</span><span class="sxs-lookup"><span data-stu-id="07835-226">0x0000060A</span></span>  <br/> |
|<span data-ttu-id="07835-227">仕訳帳レター</span><span class="sxs-lookup"><span data-stu-id="07835-227">Journal letter</span></span>  <br/> |<span data-ttu-id="07835-228">0x0000060c</span><span class="sxs-lookup"><span data-stu-id="07835-228">0x0000060C</span></span>  <br/> |
|<span data-ttu-id="07835-229">Journal Microsoft Office Word</span><span class="sxs-lookup"><span data-stu-id="07835-229">Journal Microsoft Office Word</span></span>  <br/> |<span data-ttu-id="07835-230">0x0000060d</span><span class="sxs-lookup"><span data-stu-id="07835-230">0x0000060D</span></span>  <br/> |
|<span data-ttu-id="07835-231">Journal Microsoft Office Excel</span><span class="sxs-lookup"><span data-stu-id="07835-231">Journal Microsoft Office Excel</span></span>  <br/> |<span data-ttu-id="07835-232">0x0000060E</span><span class="sxs-lookup"><span data-stu-id="07835-232">0x0000060E</span></span>  <br/> |
|<span data-ttu-id="07835-233">Microsoft Office PowerPoint のジャーナル</span><span class="sxs-lookup"><span data-stu-id="07835-233">Journal Microsoft Office PowerPoint</span></span>  <br/> |<span data-ttu-id="07835-234">0x0000060f</span><span class="sxs-lookup"><span data-stu-id="07835-234">0x0000060F</span></span>  <br/> |
|<span data-ttu-id="07835-235">Microsoft Office access のジャーナル</span><span class="sxs-lookup"><span data-stu-id="07835-235">Journal Microsoft Office Access</span></span>  <br/> |<span data-ttu-id="07835-236">0x00000610</span><span class="sxs-lookup"><span data-stu-id="07835-236">0x00000610</span></span>  <br/> |
|<span data-ttu-id="07835-237">ジャーナルドキュメント</span><span class="sxs-lookup"><span data-stu-id="07835-237">Journal document</span></span>  <br/> |<span data-ttu-id="07835-238">0x00000612</span><span class="sxs-lookup"><span data-stu-id="07835-238">0x00000612</span></span>  <br/> |
|<span data-ttu-id="07835-239">ジャーナル会議</span><span class="sxs-lookup"><span data-stu-id="07835-239">Journal meeting</span></span>  <br/> |<span data-ttu-id="07835-240">0x00000613</span><span class="sxs-lookup"><span data-stu-id="07835-240">0x00000613</span></span>  <br/> |
|<span data-ttu-id="07835-241">ジャーナル会議の取り消し</span><span class="sxs-lookup"><span data-stu-id="07835-241">Journal meeting cancellation</span></span>  <br/> |<span data-ttu-id="07835-242">0x00000614</span><span class="sxs-lookup"><span data-stu-id="07835-242">0x00000614</span></span>  <br/> |
|<span data-ttu-id="07835-243">ジャーナルリモートセッション</span><span class="sxs-lookup"><span data-stu-id="07835-243">Journal remote session</span></span>  <br/> |<span data-ttu-id="07835-244">0x00000615</span><span class="sxs-lookup"><span data-stu-id="07835-244">0x00000615</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="07835-245">関連リソース</span><span class="sxs-lookup"><span data-stu-id="07835-245">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="07835-246">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="07835-246">Protocol specifications</span></span>

<span data-ttu-id="07835-247">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="07835-247">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="07835-248">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="07835-248">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="07835-249">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="07835-249">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="07835-250">電子メールメッセージオブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="07835-250">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="07835-251">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="07835-251">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="07835-252">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="07835-252">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="07835-253">[[OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="07835-253">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="07835-254">連絡先および個人用配布リストで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="07835-254">Specifies the properties and operations that are permissible on contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="07835-255">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="07835-255">Header files</span></span>

<span data-ttu-id="07835-256">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="07835-256">Mapidefs.h</span></span>
  
> <span data-ttu-id="07835-257">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="07835-257">Provides data type definitions.</span></span>
    
<span data-ttu-id="07835-258">Mapitags</span><span class="sxs-lookup"><span data-stu-id="07835-258">Mapitags.h</span></span>
  
> <span data-ttu-id="07835-259">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="07835-259">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="07835-260">関連項目</span><span class="sxs-lookup"><span data-stu-id="07835-260">See also</span></span>



[<span data-ttu-id="07835-261">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="07835-261">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="07835-262">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="07835-262">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="07835-263">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="07835-263">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="07835-264">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="07835-264">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

