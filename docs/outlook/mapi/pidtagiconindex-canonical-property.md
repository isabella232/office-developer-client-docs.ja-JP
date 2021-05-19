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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 35d9d0a50539f8aab2d26730dd4e4544c2535e60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346621"
---
# <a name="pidtagiconindex-canonical-property"></a><span data-ttu-id="c6305-103">PidTagIconIndex 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c6305-103">PidTagIconIndex Canonical Property</span></span>

  
  
<span data-ttu-id="c6305-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c6305-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c6305-105">電子メール オブジェクトのグループを表示するときに使用するアイコンを示す番号が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c6305-105">Contains a number that indicates which icon to use when you display a group of email objects.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c6305-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c6305-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c6305-107">PR_ICON_INDEX</span><span class="sxs-lookup"><span data-stu-id="c6305-107">PR_ICON_INDEX</span></span>  <br/> |
|<span data-ttu-id="c6305-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="c6305-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c6305-109">0x1080</span><span class="sxs-lookup"><span data-stu-id="c6305-109">0x1080</span></span>  <br/> |
|<span data-ttu-id="c6305-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c6305-110">Data type:</span></span>  <br/> |<span data-ttu-id="c6305-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c6305-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c6305-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="c6305-112">Area:</span></span>  <br/> |<span data-ttu-id="c6305-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="c6305-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c6305-114">注釈</span><span class="sxs-lookup"><span data-stu-id="c6305-114">Remarks</span></span>

<span data-ttu-id="c6305-115">このプロパティが存在する場合は、クライアントへのヒントです。</span><span class="sxs-lookup"><span data-stu-id="c6305-115">This property, if it exists, is a hint to the client.</span></span> <span data-ttu-id="c6305-116">クライアントは、このプロパティの値を無視できます。</span><span class="sxs-lookup"><span data-stu-id="c6305-116">The client may ignore the value of this property.</span></span> 
  
|<span data-ttu-id="c6305-117">**メール アイテムの状態**</span><span class="sxs-lookup"><span data-stu-id="c6305-117">**Mail item state**</span></span>|<span data-ttu-id="c6305-118">**アイコン インデックス**</span><span class="sxs-lookup"><span data-stu-id="c6305-118">**Icon Index**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c6305-119">新しいメール</span><span class="sxs-lookup"><span data-stu-id="c6305-119">New mail</span></span>  <br/> |<span data-ttu-id="c6305-120">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="c6305-120">0xFFFFFFFF</span></span>  <br/> |
|<span data-ttu-id="c6305-121">投稿</span><span class="sxs-lookup"><span data-stu-id="c6305-121">Post</span></span>  <br/> |<span data-ttu-id="c6305-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c6305-122">0x00000001</span></span>  <br/> |
|<span data-ttu-id="c6305-123">その他</span><span class="sxs-lookup"><span data-stu-id="c6305-123">Other</span></span>  <br/> |<span data-ttu-id="c6305-124">0x00000003</span><span class="sxs-lookup"><span data-stu-id="c6305-124">0x00000003</span></span>  <br/> |
|<span data-ttu-id="c6305-125">メールの読み取り</span><span class="sxs-lookup"><span data-stu-id="c6305-125">Read mail</span></span>  <br/> |<span data-ttu-id="c6305-126">0x00000100</span><span class="sxs-lookup"><span data-stu-id="c6305-126">0x00000100</span></span>  <br/> |
|<span data-ttu-id="c6305-127">未読メール</span><span class="sxs-lookup"><span data-stu-id="c6305-127">Unread mail</span></span>  <br/> |<span data-ttu-id="c6305-128">0x00000101</span><span class="sxs-lookup"><span data-stu-id="c6305-128">0x00000101</span></span>  <br/> |
|<span data-ttu-id="c6305-129">送信済みメール</span><span class="sxs-lookup"><span data-stu-id="c6305-129">Submitted mail</span></span>  <br/> |<span data-ttu-id="c6305-130">0x00000102</span><span class="sxs-lookup"><span data-stu-id="c6305-130">0x00000102</span></span>  <br/> |
|<span data-ttu-id="c6305-131">送信されていないメール</span><span class="sxs-lookup"><span data-stu-id="c6305-131">Unsent mail</span></span>  <br/> |<span data-ttu-id="c6305-132">0x00000103</span><span class="sxs-lookup"><span data-stu-id="c6305-132">0x00000103</span></span>  <br/> |
|<span data-ttu-id="c6305-133">受信メール</span><span class="sxs-lookup"><span data-stu-id="c6305-133">Receipt mail</span></span>  <br/> |<span data-ttu-id="c6305-134">0x00000104</span><span class="sxs-lookup"><span data-stu-id="c6305-134">0x00000104</span></span>  <br/> |
|<span data-ttu-id="c6305-135">返信メール</span><span class="sxs-lookup"><span data-stu-id="c6305-135">Replied mail</span></span>  <br/> |<span data-ttu-id="c6305-136">0x00000105</span><span class="sxs-lookup"><span data-stu-id="c6305-136">0x00000105</span></span>  <br/> |
|<span data-ttu-id="c6305-137">転送されたメール</span><span class="sxs-lookup"><span data-stu-id="c6305-137">Forwarded mail</span></span>  <br/> |<span data-ttu-id="c6305-138">0x00000106</span><span class="sxs-lookup"><span data-stu-id="c6305-138">0x00000106</span></span>  <br/> |
|<span data-ttu-id="c6305-139">リモート メール</span><span class="sxs-lookup"><span data-stu-id="c6305-139">Remote mail</span></span>  <br/> |<span data-ttu-id="c6305-140">0x00000107</span><span class="sxs-lookup"><span data-stu-id="c6305-140">0x00000107</span></span>  <br/> |
|<span data-ttu-id="c6305-141">配信メール</span><span class="sxs-lookup"><span data-stu-id="c6305-141">Delivery mail</span></span>  <br/> |<span data-ttu-id="c6305-142">0x00000108</span><span class="sxs-lookup"><span data-stu-id="c6305-142">0x00000108</span></span>  <br/> |
|<span data-ttu-id="c6305-143">メールの読み取り</span><span class="sxs-lookup"><span data-stu-id="c6305-143">Read mail</span></span>  <br/> |<span data-ttu-id="c6305-144">0x00000109</span><span class="sxs-lookup"><span data-stu-id="c6305-144">0x00000109</span></span>  <br/> |
|<span data-ttu-id="c6305-145">配信以外のメール</span><span class="sxs-lookup"><span data-stu-id="c6305-145">Nondelivery mail</span></span>  <br/> |<span data-ttu-id="c6305-146">0x0000010A</span><span class="sxs-lookup"><span data-stu-id="c6305-146">0x0000010A</span></span>  <br/> |
|<span data-ttu-id="c6305-147">未読メール</span><span class="sxs-lookup"><span data-stu-id="c6305-147">Nonread mail</span></span>  <br/> |<span data-ttu-id="c6305-148">0x0000010B</span><span class="sxs-lookup"><span data-stu-id="c6305-148">0x0000010B</span></span>  <br/> |
|<span data-ttu-id="c6305-149">Recall_Sメール</span><span class="sxs-lookup"><span data-stu-id="c6305-149">Recall_S mail</span></span>  <br/> |<span data-ttu-id="c6305-150">0x0000010C</span><span class="sxs-lookup"><span data-stu-id="c6305-150">0x0000010C</span></span>  <br/> |
|<span data-ttu-id="c6305-151">Recall_Fメール</span><span class="sxs-lookup"><span data-stu-id="c6305-151">Recall_F mail</span></span>  <br/> |<span data-ttu-id="c6305-152">0x0000010D</span><span class="sxs-lookup"><span data-stu-id="c6305-152">0x0000010D</span></span>  <br/> |
|<span data-ttu-id="c6305-153">メールの追跡</span><span class="sxs-lookup"><span data-stu-id="c6305-153">Tracking mail</span></span>  <br/> |<span data-ttu-id="c6305-154">0x0000010E</span><span class="sxs-lookup"><span data-stu-id="c6305-154">0x0000010E</span></span>  <br/> |
|<span data-ttu-id="c6305-155">アウトオブオフィスメール</span><span class="sxs-lookup"><span data-stu-id="c6305-155">Out of office mail</span></span>  <br/> |<span data-ttu-id="c6305-156">0x0000011B</span><span class="sxs-lookup"><span data-stu-id="c6305-156">0x0000011B</span></span>  <br/> |
|<span data-ttu-id="c6305-157">メールの取り消し</span><span class="sxs-lookup"><span data-stu-id="c6305-157">Recall mail</span></span>  <br/> |<span data-ttu-id="c6305-158">0x0000011C</span><span class="sxs-lookup"><span data-stu-id="c6305-158">0x0000011C</span></span>  <br/> |
|<span data-ttu-id="c6305-159">追跡メール</span><span class="sxs-lookup"><span data-stu-id="c6305-159">Tracked mail</span></span>  <br/> |<span data-ttu-id="c6305-160">0x00000130</span><span class="sxs-lookup"><span data-stu-id="c6305-160">0x00000130</span></span>  <br/> |
|<span data-ttu-id="c6305-161">Contact</span><span class="sxs-lookup"><span data-stu-id="c6305-161">Contact</span></span>  <br/> |<span data-ttu-id="c6305-162">0x00000200</span><span class="sxs-lookup"><span data-stu-id="c6305-162">0x00000200</span></span>  <br/> |
|<span data-ttu-id="c6305-163">配布リスト</span><span class="sxs-lookup"><span data-stu-id="c6305-163">Distribution list</span></span>  <br/> |<span data-ttu-id="c6305-164">0x00000202</span><span class="sxs-lookup"><span data-stu-id="c6305-164">0x00000202</span></span>  <br/> |
|<span data-ttu-id="c6305-165">付箋青</span><span class="sxs-lookup"><span data-stu-id="c6305-165">Sticky note blue</span></span>  <br/> |<span data-ttu-id="c6305-166">0x00000300</span><span class="sxs-lookup"><span data-stu-id="c6305-166">0x00000300</span></span>  <br/> |
|<span data-ttu-id="c6305-167">付箋グリーン</span><span class="sxs-lookup"><span data-stu-id="c6305-167">Sticky note green</span></span>  <br/> |<span data-ttu-id="c6305-168">0x00000301</span><span class="sxs-lookup"><span data-stu-id="c6305-168">0x00000301</span></span>  <br/> |
|<span data-ttu-id="c6305-169">付箋ピンク</span><span class="sxs-lookup"><span data-stu-id="c6305-169">Sticky note pink</span></span>  <br/> |<span data-ttu-id="c6305-170">0x00000302</span><span class="sxs-lookup"><span data-stu-id="c6305-170">0x00000302</span></span>  <br/> |
|<span data-ttu-id="c6305-171">付箋の黄色</span><span class="sxs-lookup"><span data-stu-id="c6305-171">Sticky note yellow</span></span>  <br/> |<span data-ttu-id="c6305-172">0x00000303</span><span class="sxs-lookup"><span data-stu-id="c6305-172">0x00000303</span></span>  <br/> |
|<span data-ttu-id="c6305-173">付箋白</span><span class="sxs-lookup"><span data-stu-id="c6305-173">Sticky note white</span></span>  <br/> |<span data-ttu-id="c6305-174">0x00000304</span><span class="sxs-lookup"><span data-stu-id="c6305-174">0x00000304</span></span>  <br/> |
|<span data-ttu-id="c6305-175">単一インスタンスの予定</span><span class="sxs-lookup"><span data-stu-id="c6305-175">Single instance appointment</span></span>  <br/> |<span data-ttu-id="c6305-176">0x00000400</span><span class="sxs-lookup"><span data-stu-id="c6305-176">0x00000400</span></span>  <br/> |
|<span data-ttu-id="c6305-177">定期的な予定</span><span class="sxs-lookup"><span data-stu-id="c6305-177">Recurring appointment</span></span>  <br/> |<span data-ttu-id="c6305-178">0x00000401</span><span class="sxs-lookup"><span data-stu-id="c6305-178">0x00000401</span></span>  <br/> |
|<span data-ttu-id="c6305-179">単一インスタンス会議</span><span class="sxs-lookup"><span data-stu-id="c6305-179">Single instance meeting</span></span>  <br/> |<span data-ttu-id="c6305-180">0x00000402</span><span class="sxs-lookup"><span data-stu-id="c6305-180">0x00000402</span></span>  <br/> |
|<span data-ttu-id="c6305-181">定期的な会議</span><span class="sxs-lookup"><span data-stu-id="c6305-181">Recurring meeting</span></span>  <br/> |<span data-ttu-id="c6305-182">0x00000403</span><span class="sxs-lookup"><span data-stu-id="c6305-182">0x00000403</span></span>  <br/> |
|<span data-ttu-id="c6305-183">会議出席依頼</span><span class="sxs-lookup"><span data-stu-id="c6305-183">Meeting request</span></span>  <br/> |<span data-ttu-id="c6305-184">0x00000404</span><span class="sxs-lookup"><span data-stu-id="c6305-184">0x00000404</span></span>  <br/> |
|<span data-ttu-id="c6305-185">承諾</span><span class="sxs-lookup"><span data-stu-id="c6305-185">Accept</span></span>  <br/> |<span data-ttu-id="c6305-186">0x00000405</span><span class="sxs-lookup"><span data-stu-id="c6305-186">0x00000405</span></span>  <br/> |
|<span data-ttu-id="c6305-187">拒否</span><span class="sxs-lookup"><span data-stu-id="c6305-187">Decline</span></span>  <br/> |<span data-ttu-id="c6305-188">0x00000406</span><span class="sxs-lookup"><span data-stu-id="c6305-188">0x00000406</span></span>  <br/> |
|<span data-ttu-id="c6305-189">Tentativly</span><span class="sxs-lookup"><span data-stu-id="c6305-189">Tentativly</span></span>  <br/> |<span data-ttu-id="c6305-190">0x00000407</span><span class="sxs-lookup"><span data-stu-id="c6305-190">0x00000407</span></span>  <br/> |
|<span data-ttu-id="c6305-191">取り消し</span><span class="sxs-lookup"><span data-stu-id="c6305-191">Cancellation</span></span>  <br/> |<span data-ttu-id="c6305-192">0x00000408</span><span class="sxs-lookup"><span data-stu-id="c6305-192">0x00000408</span></span>  <br/> |
|<span data-ttu-id="c6305-193">情報更新</span><span class="sxs-lookup"><span data-stu-id="c6305-193">Informational update</span></span>  <br/> |<span data-ttu-id="c6305-194">0x00000409</span><span class="sxs-lookup"><span data-stu-id="c6305-194">0x00000409</span></span>  <br/> |
|<span data-ttu-id="c6305-195">タスク/タスク</span><span class="sxs-lookup"><span data-stu-id="c6305-195">Task/task</span></span>  <br/> |<span data-ttu-id="c6305-196">0x00000500</span><span class="sxs-lookup"><span data-stu-id="c6305-196">0x00000500</span></span>  <br/> |
|<span data-ttu-id="c6305-197">割り当てられていない定期的なタスク</span><span class="sxs-lookup"><span data-stu-id="c6305-197">Unassigned recurring task</span></span>  <br/> |<span data-ttu-id="c6305-198">0x00000501</span><span class="sxs-lookup"><span data-stu-id="c6305-198">0x00000501</span></span>  <br/> |
|<span data-ttu-id="c6305-199">割り当て先のタスク</span><span class="sxs-lookup"><span data-stu-id="c6305-199">Assignee's task</span></span>  <br/> |<span data-ttu-id="c6305-200">0x00000502</span><span class="sxs-lookup"><span data-stu-id="c6305-200">0x00000502</span></span>  <br/> |
|<span data-ttu-id="c6305-201">割り当て人のタスク</span><span class="sxs-lookup"><span data-stu-id="c6305-201">Assigner's task</span></span>  <br/> |<span data-ttu-id="c6305-202">0x00000503</span><span class="sxs-lookup"><span data-stu-id="c6305-202">0x00000503</span></span>  <br/> |
|<span data-ttu-id="c6305-203">タスク要求</span><span class="sxs-lookup"><span data-stu-id="c6305-203">Task request</span></span>  <br/> |<span data-ttu-id="c6305-204">0x00000504</span><span class="sxs-lookup"><span data-stu-id="c6305-204">0x00000504</span></span>  <br/> |
|<span data-ttu-id="c6305-205">タスクの受け入れ</span><span class="sxs-lookup"><span data-stu-id="c6305-205">Task acceptance</span></span>  <br/> |<span data-ttu-id="c6305-206">0x00000505</span><span class="sxs-lookup"><span data-stu-id="c6305-206">0x00000505</span></span>  <br/> |
|<span data-ttu-id="c6305-207">タスクの拒否</span><span class="sxs-lookup"><span data-stu-id="c6305-207">Task rejection</span></span>  <br/> |<span data-ttu-id="c6305-208">0x00000506</span><span class="sxs-lookup"><span data-stu-id="c6305-208">0x00000506</span></span>  <br/> |
|<span data-ttu-id="c6305-209">ジャーナルの会話</span><span class="sxs-lookup"><span data-stu-id="c6305-209">Journal conversation</span></span>  <br/> |<span data-ttu-id="c6305-210">0x00000601</span><span class="sxs-lookup"><span data-stu-id="c6305-210">0x00000601</span></span>  <br/> |
|<span data-ttu-id="c6305-211">ジャーナル電子メール メッセージ</span><span class="sxs-lookup"><span data-stu-id="c6305-211">Journal email message</span></span>  <br/> |<span data-ttu-id="c6305-212">0x00000602</span><span class="sxs-lookup"><span data-stu-id="c6305-212">0x00000602</span></span>  <br/> |
|<span data-ttu-id="c6305-213">ジャーナル会議出席依頼</span><span class="sxs-lookup"><span data-stu-id="c6305-213">Journal meeting request</span></span>  <br/> |<span data-ttu-id="c6305-214">0x00000603</span><span class="sxs-lookup"><span data-stu-id="c6305-214">0x00000603</span></span>  <br/> |
|<span data-ttu-id="c6305-215">ジャーナル会議の応答</span><span class="sxs-lookup"><span data-stu-id="c6305-215">Journal meeting response</span></span>  <br/> |<span data-ttu-id="c6305-216">0x00000604</span><span class="sxs-lookup"><span data-stu-id="c6305-216">0x00000604</span></span>  <br/> |
|<span data-ttu-id="c6305-217">ジャーナル タスク要求</span><span class="sxs-lookup"><span data-stu-id="c6305-217">Journal task request</span></span>  <br/> |<span data-ttu-id="c6305-218">0x00000606</span><span class="sxs-lookup"><span data-stu-id="c6305-218">0x00000606</span></span>  <br/> |
|<span data-ttu-id="c6305-219">ジャーナル タスクの応答</span><span class="sxs-lookup"><span data-stu-id="c6305-219">Journal task response</span></span>  <br/> |<span data-ttu-id="c6305-220">0x00000607</span><span class="sxs-lookup"><span data-stu-id="c6305-220">0x00000607</span></span>  <br/> |
|<span data-ttu-id="c6305-221">ジャーナル ノート</span><span class="sxs-lookup"><span data-stu-id="c6305-221">Journal note</span></span>  <br/> |<span data-ttu-id="c6305-222">0x00000608</span><span class="sxs-lookup"><span data-stu-id="c6305-222">0x00000608</span></span>  <br/> |
|<span data-ttu-id="c6305-223">ジャーナル FAX</span><span class="sxs-lookup"><span data-stu-id="c6305-223">Journal fax</span></span>  <br/> |<span data-ttu-id="c6305-224">0x00000609</span><span class="sxs-lookup"><span data-stu-id="c6305-224">0x00000609</span></span>  <br/> |
|<span data-ttu-id="c6305-225">ジャーナル電話</span><span class="sxs-lookup"><span data-stu-id="c6305-225">Journal phone call</span></span>  <br/> |<span data-ttu-id="c6305-226">0x0000060A</span><span class="sxs-lookup"><span data-stu-id="c6305-226">0x0000060A</span></span>  <br/> |
|<span data-ttu-id="c6305-227">ジャーナル レター</span><span class="sxs-lookup"><span data-stu-id="c6305-227">Journal letter</span></span>  <br/> |<span data-ttu-id="c6305-228">0x0000060C</span><span class="sxs-lookup"><span data-stu-id="c6305-228">0x0000060C</span></span>  <br/> |
|<span data-ttu-id="c6305-229">ジャーナル Microsoft Office Word</span><span class="sxs-lookup"><span data-stu-id="c6305-229">Journal Microsoft Office Word</span></span>  <br/> |<span data-ttu-id="c6305-230">0x0000060D</span><span class="sxs-lookup"><span data-stu-id="c6305-230">0x0000060D</span></span>  <br/> |
|<span data-ttu-id="c6305-231">ジャーナル Microsoft Office Excel</span><span class="sxs-lookup"><span data-stu-id="c6305-231">Journal Microsoft Office Excel</span></span>  <br/> |<span data-ttu-id="c6305-232">0x0000060E</span><span class="sxs-lookup"><span data-stu-id="c6305-232">0x0000060E</span></span>  <br/> |
|<span data-ttu-id="c6305-233">ジャーナル Microsoft Office PowerPoint</span><span class="sxs-lookup"><span data-stu-id="c6305-233">Journal Microsoft Office PowerPoint</span></span>  <br/> |<span data-ttu-id="c6305-234">0x0000060F</span><span class="sxs-lookup"><span data-stu-id="c6305-234">0x0000060F</span></span>  <br/> |
|<span data-ttu-id="c6305-235">ジャーナル Microsoft Office Access</span><span class="sxs-lookup"><span data-stu-id="c6305-235">Journal Microsoft Office Access</span></span>  <br/> |<span data-ttu-id="c6305-236">0x00000610</span><span class="sxs-lookup"><span data-stu-id="c6305-236">0x00000610</span></span>  <br/> |
|<span data-ttu-id="c6305-237">ジャーナル ドキュメント</span><span class="sxs-lookup"><span data-stu-id="c6305-237">Journal document</span></span>  <br/> |<span data-ttu-id="c6305-238">0x00000612</span><span class="sxs-lookup"><span data-stu-id="c6305-238">0x00000612</span></span>  <br/> |
|<span data-ttu-id="c6305-239">ジャーナル会議</span><span class="sxs-lookup"><span data-stu-id="c6305-239">Journal meeting</span></span>  <br/> |<span data-ttu-id="c6305-240">0x00000613</span><span class="sxs-lookup"><span data-stu-id="c6305-240">0x00000613</span></span>  <br/> |
|<span data-ttu-id="c6305-241">ジャーナル 会議の取り消し</span><span class="sxs-lookup"><span data-stu-id="c6305-241">Journal meeting cancellation</span></span>  <br/> |<span data-ttu-id="c6305-242">0x00000614</span><span class="sxs-lookup"><span data-stu-id="c6305-242">0x00000614</span></span>  <br/> |
|<span data-ttu-id="c6305-243">ジャーナル リモート セッション</span><span class="sxs-lookup"><span data-stu-id="c6305-243">Journal remote session</span></span>  <br/> |<span data-ttu-id="c6305-244">0x00000615</span><span class="sxs-lookup"><span data-stu-id="c6305-244">0x00000615</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="c6305-245">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c6305-245">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c6305-246">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c6305-246">Protocol specifications</span></span>

<span data-ttu-id="c6305-247">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c6305-247">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c6305-248">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="c6305-248">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c6305-249">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c6305-249">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c6305-250">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="c6305-250">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="c6305-251">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c6305-251">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c6305-252">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="c6305-252">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="c6305-253">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c6305-253">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c6305-254">連絡先と個人用配布リストで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="c6305-254">Specifies the properties and operations that are permissible on contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c6305-255">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c6305-255">Header files</span></span>

<span data-ttu-id="c6305-256">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c6305-256">Mapidefs.h</span></span>
  
> <span data-ttu-id="c6305-257">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c6305-257">Provides data type definitions.</span></span>
    
<span data-ttu-id="c6305-258">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c6305-258">Mapitags.h</span></span>
  
> <span data-ttu-id="c6305-259">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="c6305-259">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c6305-260">関連項目</span><span class="sxs-lookup"><span data-stu-id="c6305-260">See also</span></span>



[<span data-ttu-id="c6305-261">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="c6305-261">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c6305-262">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c6305-262">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c6305-263">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c6305-263">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c6305-264">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c6305-264">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

