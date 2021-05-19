---
title: PidTagAdditionalRenEntryIdsEx 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAdditionalRenEntryIdsEx
api_type:
- HeaderDef
ms.assetid: b5e896e7-c0c6-4ad1-bf91-9daba3a1e4d4
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 57ab68d4c53693c769a4aadf8737f57ef5e73fcd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335204"
---
# <a name="pidtagadditionalrenentryidsex-canonical-property"></a><span data-ttu-id="075f2-103">PidTagAdditionalRenEntryIdsEx 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="075f2-103">PidTagAdditionalRenEntryIdsEx Canonical Property</span></span>

  
  
<span data-ttu-id="075f2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="075f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="075f2-105">ストア オブジェクトの特別なフォルダー エントリの ID を格納します。</span><span class="sxs-lookup"><span data-stu-id="075f2-105">Contains special folder entry IDs for a store object.</span></span> <span data-ttu-id="075f2-106">この複数値プロパティの各エントリは、1 つ以上のエントリ ID にマップできます。つまり、エントリと関連するエントリ ID の間には 1 対多の関係があります。</span><span class="sxs-lookup"><span data-stu-id="075f2-106">Each entry in this multi-valued property can be mapped to one or more entry IDs, that is, there is a one-to-many relationship between an entry and its associated entry IDs.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="075f2-107">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="075f2-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="075f2-108">PR_ADDITIONAL_REN_ENTRYIDS_EX</span><span class="sxs-lookup"><span data-stu-id="075f2-108">PR_ADDITIONAL_REN_ENTRYIDS_EX</span></span>  <br/> |
|<span data-ttu-id="075f2-109">識別子:</span><span class="sxs-lookup"><span data-stu-id="075f2-109">Identifier:</span></span>  <br/> |<span data-ttu-id="075f2-110">0x36D9</span><span class="sxs-lookup"><span data-stu-id="075f2-110">0x36D9</span></span>  <br/> |
|<span data-ttu-id="075f2-111">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="075f2-111">Data type:</span></span>  <br/> |<span data-ttu-id="075f2-112">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="075f2-112">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="075f2-113">エリア:</span><span class="sxs-lookup"><span data-stu-id="075f2-113">Area:</span></span>  <br/> |<span data-ttu-id="075f2-114">Outlookアプリケーション</span><span class="sxs-lookup"><span data-stu-id="075f2-114">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="075f2-115">注釈</span><span class="sxs-lookup"><span data-stu-id="075f2-115">Remarks</span></span>

<span data-ttu-id="075f2-116">このプロパティを使用する場合は、フォルダーのエントリの ID を指定するブロックの配列が含まれます。</span><span class="sxs-lookup"><span data-stu-id="075f2-116">If this property is used, it contains an array of blocks that specifies the entry IDs for the folders.</span></span> <span data-ttu-id="075f2-117">ブロックは、次の 4 つの表で指定された形式に従います。</span><span class="sxs-lookup"><span data-stu-id="075f2-117">The blocks follow the format specified by the following four tables.</span></span>
  
<span data-ttu-id="075f2-118">**PersistData ブロック**</span><span class="sxs-lookup"><span data-stu-id="075f2-118">**PersistData Block**</span></span>

|<span data-ttu-id="075f2-119">**名前**</span><span class="sxs-lookup"><span data-stu-id="075f2-119">**Name**</span></span>|<span data-ttu-id="075f2-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="075f2-120">**Type**</span></span>|<span data-ttu-id="075f2-121">**[サイズ]**</span><span class="sxs-lookup"><span data-stu-id="075f2-121">**Size**</span></span>|<span data-ttu-id="075f2-122">**説明**</span><span class="sxs-lookup"><span data-stu-id="075f2-122">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="075f2-123">**PersistID**</span><span class="sxs-lookup"><span data-stu-id="075f2-123">**PersistID**</span></span> <br/> |<span data-ttu-id="075f2-124">WORD</span><span class="sxs-lookup"><span data-stu-id="075f2-124">WORD</span></span>  <br/> |<span data-ttu-id="075f2-125">2</span><span class="sxs-lookup"><span data-stu-id="075f2-125">2</span></span>  <br/> |<span data-ttu-id="075f2-126">この PersistData エントリの識別子 **の値を入力** します。</span><span class="sxs-lookup"><span data-stu-id="075f2-126">Type identifier value for this **PersistData** entry.</span></span> <span data-ttu-id="075f2-127">有効な値の一覧については、「PersistBlockType Values」テーブルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="075f2-127">See the "PersistBlockType Values" table for the list of valid values.</span></span>  <br/> |
|<span data-ttu-id="075f2-128">**DataElementsSize**</span><span class="sxs-lookup"><span data-stu-id="075f2-128">**DataElementsSize**</span></span> <br/> |<span data-ttu-id="075f2-129">WORD</span><span class="sxs-lookup"><span data-stu-id="075f2-129">WORD</span></span>  <br/> |<span data-ttu-id="075f2-130">2</span><span class="sxs-lookup"><span data-stu-id="075f2-130">2</span></span>  <br/> |<span data-ttu-id="075f2-131">**DataElements** フィールドのサイズ (バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="075f2-131">Size, in bytes, of the **DataElements** field.</span></span>  <br/> |
|<span data-ttu-id="075f2-132">**DataElements**</span><span class="sxs-lookup"><span data-stu-id="075f2-132">**DataElements**</span></span> <br/> |<span data-ttu-id="075f2-133">**PersistElement ブロックの** 配列</span><span class="sxs-lookup"><span data-stu-id="075f2-133">array of **PersistElement** blocks</span></span>  <br/> |<span data-ttu-id="075f2-134">変数</span><span class="sxs-lookup"><span data-stu-id="075f2-134">variable</span></span>  <br/> |<span data-ttu-id="075f2-135">ストアに存在 **する PersistElement** エントリの数を示します。</span><span class="sxs-lookup"><span data-stu-id="075f2-135">Indicates how many **PersistElement** entries exist for the store.</span></span> <span data-ttu-id="075f2-136">この構造の形式については、「PersistElement Block」テーブルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="075f2-136">See the "PersistElement Block" table for the format of this structure.</span></span>  <br/> |
   
<span data-ttu-id="075f2-137">**PersistBlockType 値**</span><span class="sxs-lookup"><span data-stu-id="075f2-137">**PersistBlockType Values**</span></span>

|<span data-ttu-id="075f2-138">**名前**</span><span class="sxs-lookup"><span data-stu-id="075f2-138">**Name**</span></span>|<span data-ttu-id="075f2-139">**値**</span><span class="sxs-lookup"><span data-stu-id="075f2-139">**Value**</span></span>|<span data-ttu-id="075f2-140">**説明**</span><span class="sxs-lookup"><span data-stu-id="075f2-140">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="075f2-141">PERSIST_SENTINEL</span><span class="sxs-lookup"><span data-stu-id="075f2-141">PERSIST_SENTINEL</span></span>  <br/> |<span data-ttu-id="075f2-142">0x0000</span><span class="sxs-lookup"><span data-stu-id="075f2-142">0x0000</span></span>  <br/> |<span data-ttu-id="075f2-143">PersistData ブロックが **処理され** なきを示します。</span><span class="sxs-lookup"><span data-stu-id="075f2-143">Indicates that no more **PersistData** blocks will be processed.</span></span>  <br/> |
|<span data-ttu-id="075f2-144">RSF_PID_RSS_SUBSCRIPTION</span><span class="sxs-lookup"><span data-stu-id="075f2-144">RSF_PID_RSS_SUBSCRIPTION</span></span>  <br/> |<span data-ttu-id="075f2-145">0x8001</span><span class="sxs-lookup"><span data-stu-id="075f2-145">0x8001</span></span>  <br/> |<span data-ttu-id="075f2-146">このブロックに RSS サブスクリプション フォルダーのデータが含まれているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="075f2-146">Indicates that this block contains data for the RSS Subscriptions folder.</span></span>  <br/> |
|<span data-ttu-id="075f2-147">RSF_PID_SEND_AND_TRACK</span><span class="sxs-lookup"><span data-stu-id="075f2-147">RSF_PID_SEND_AND_TRACK</span></span>  <br/> |<span data-ttu-id="075f2-148">0x8002</span><span class="sxs-lookup"><span data-stu-id="075f2-148">0x8002</span></span>  <br/> |<span data-ttu-id="075f2-149">このブロックに、追跡メール処理フォルダーのデータが含まれているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="075f2-149">Indicates that this block contains data for the Tracked Mail Processing folder.</span></span>  <br/> |
|<span data-ttu-id="075f2-150">RSF_PID_TODO_SEARCH</span><span class="sxs-lookup"><span data-stu-id="075f2-150">RSF_PID_TODO_SEARCH</span></span>  <br/> |<span data-ttu-id="075f2-151">0x8004</span><span class="sxs-lookup"><span data-stu-id="075f2-151">0x8004</span></span>  <br/> |<span data-ttu-id="075f2-152">このブロックに、検索フォルダーのデータTo-Do示します。</span><span class="sxs-lookup"><span data-stu-id="075f2-152">Indicates that this block contains data for the To-Do Search folder.</span></span>  <br/> |
|<span data-ttu-id="075f2-153">RSF_PID_CONV_ACTIONS</span><span class="sxs-lookup"><span data-stu-id="075f2-153">RSF_PID_CONV_ACTIONS</span></span>  <br/> |<span data-ttu-id="075f2-154">0x8006</span><span class="sxs-lookup"><span data-stu-id="075f2-154">0x8006</span></span>  <br/> |<span data-ttu-id="075f2-155">このブロックに、スレッド アクション フォルダーのデータが含設定します。</span><span class="sxs-lookup"><span data-stu-id="075f2-155">Indicates that this block contains data for the Conversation Action Settings folder.</span></span>  <br/> |
|<span data-ttu-id="075f2-156">RSF_PID_COMBINED_ACTIONS</span><span class="sxs-lookup"><span data-stu-id="075f2-156">RSF_PID_COMBINED_ACTIONS</span></span>  <br/> |<span data-ttu-id="075f2-157">0x8007</span><span class="sxs-lookup"><span data-stu-id="075f2-157">0x8007</span></span>  <br/> |<span data-ttu-id="075f2-158">この値は予約済みです。</span><span class="sxs-lookup"><span data-stu-id="075f2-158">This value is reserved.</span></span>  <br/> |
|<span data-ttu-id="075f2-159">RSF_PID_SUGGESTED_CONTACTS</span><span class="sxs-lookup"><span data-stu-id="075f2-159">RSF_PID_SUGGESTED_CONTACTS</span></span>  <br/> |<span data-ttu-id="075f2-160">0x8008</span><span class="sxs-lookup"><span data-stu-id="075f2-160">0x8008</span></span>  <br/> |<span data-ttu-id="075f2-161">このブロックに[推奨連絡先] フォルダーのデータが含まれていることを示します。</span><span class="sxs-lookup"><span data-stu-id="075f2-161">Indicates that this block contains data for the Suggested Contacts folder.</span></span>  <br/> |
|<span data-ttu-id="075f2-162">RSF_PID_CONTACT_SEARCH</span><span class="sxs-lookup"><span data-stu-id="075f2-162">RSF_PID_CONTACT_SEARCH</span></span>  <br/> |<span data-ttu-id="075f2-163">0x8009</span><span class="sxs-lookup"><span data-stu-id="075f2-163">0x8009</span></span>  <br/> |<span data-ttu-id="075f2-164">このブロックに連絡先検索フォルダーのデータが含まれているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="075f2-164">Indicates that this block contains data for the Contacts Search folder.</span></span>  <br/> <span data-ttu-id="075f2-165">ユーザーが使用するOutlook。</span><span class="sxs-lookup"><span data-stu-id="075f2-165">Used only by Outlook.</span></span>  <br/> |
|<span data-ttu-id="075f2-166">RSF_PID_BUDDYLIST_PDLS</span><span class="sxs-lookup"><span data-stu-id="075f2-166">RSF_PID_BUDDYLIST_PDLS</span></span>  <br/> |<span data-ttu-id="075f2-167">0x800A</span><span class="sxs-lookup"><span data-stu-id="075f2-167">0x800A</span></span>  <br/> |<span data-ttu-id="075f2-168">このブロックにインスタント メッセージング (IM) 連絡先リスト フォルダーのデータが含まれているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="075f2-168">Indicates that this block contains data for the Instant Messaging (IM) Contact Lists folder.</span></span> <span data-ttu-id="075f2-169">参照先のフォルダーには、IM 連絡先リスト内の各グループを表す個人用配布リスト (PDL) が含まれる。</span><span class="sxs-lookup"><span data-stu-id="075f2-169">The referenced folder contains Personal Distribution Lists (PDLs) representing each group within the IM Contact list.</span></span>  <br/> <span data-ttu-id="075f2-170">この値は、OutlookとExchange。</span><span class="sxs-lookup"><span data-stu-id="075f2-170">Used by both Outlook and Exchange.</span></span>  <br/> |
|<span data-ttu-id="075f2-171">RSF_PID_BUDDYLIST_CONTACTS</span><span class="sxs-lookup"><span data-stu-id="075f2-171">RSF_PID_BUDDYLIST_CONTACTS</span></span>  <br/> |<span data-ttu-id="075f2-172">0x800B</span><span class="sxs-lookup"><span data-stu-id="075f2-172">0x800B</span></span>  <br/> |<span data-ttu-id="075f2-173">このブロックに IM 連絡先フォルダーのデータが含まれているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="075f2-173">Indicates that this block contains data for the IM Contacts folder.</span></span> <span data-ttu-id="075f2-174">参照先フォルダーには、IM 連絡先一覧グループによって参照される個々の連絡先が含まれる。</span><span class="sxs-lookup"><span data-stu-id="075f2-174">The referenced folder contains the individual contacts referenced by the IM Contact List groups.</span></span>  <br/> <span data-ttu-id="075f2-175">この値は、OutlookとExchange。</span><span class="sxs-lookup"><span data-stu-id="075f2-175">Used by both Outlook and Exchange.</span></span>  <br/> |
   
<span data-ttu-id="075f2-176">**PersistBlockType** 値がここで定義されている値の 1 つではない場合 **、PersistData** ブロックは無視され、PERSIST_SENTINEL **PersistID** が処理されるまで、またはストリームの末尾に達するまで処理が継続されます。</span><span class="sxs-lookup"><span data-stu-id="075f2-176">If the **PersistBlockType** value is not one of the ones defined here, the **PersistData** block is ignored and processing is continued until either a PERSIST_SENTINEL **PersistID** is processed or the end of the stream is reached.</span></span> 
  
<span data-ttu-id="075f2-177">**PersistElementBlock**</span><span class="sxs-lookup"><span data-stu-id="075f2-177">**PersistElementBlock**</span></span>

|<span data-ttu-id="075f2-178">**名前**</span><span class="sxs-lookup"><span data-stu-id="075f2-178">**Name**</span></span>|<span data-ttu-id="075f2-179">**Type**</span><span class="sxs-lookup"><span data-stu-id="075f2-179">**Type**</span></span>|<span data-ttu-id="075f2-180">**[サイズ]**</span><span class="sxs-lookup"><span data-stu-id="075f2-180">**Size**</span></span>|<span data-ttu-id="075f2-181">**説明**</span><span class="sxs-lookup"><span data-stu-id="075f2-181">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="075f2-182">**ElementID**</span><span class="sxs-lookup"><span data-stu-id="075f2-182">**ElementID**</span></span> <br/> |<span data-ttu-id="075f2-183">WORD</span><span class="sxs-lookup"><span data-stu-id="075f2-183">WORD</span></span>  <br/> |<span data-ttu-id="075f2-184">2</span><span class="sxs-lookup"><span data-stu-id="075f2-184">2</span></span>  <br/> |<span data-ttu-id="075f2-185">この PersistElement ブロックの型識別子 **の値を指定** します。</span><span class="sxs-lookup"><span data-stu-id="075f2-185">Specifies the type identifier value for this **PersistElement** block.</span></span> <span data-ttu-id="075f2-186">有効な値の一覧については、「PersistElementType Values」の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="075f2-186">See the "PersistElementType Values" table for a list of valid values.</span></span>  <br/> |
|<span data-ttu-id="075f2-187">**ElementDataSize**</span><span class="sxs-lookup"><span data-stu-id="075f2-187">**ElementDataSize**</span></span> <br/> |<span data-ttu-id="075f2-188">WORD</span><span class="sxs-lookup"><span data-stu-id="075f2-188">WORD</span></span>  <br/> |<span data-ttu-id="075f2-189">2</span><span class="sxs-lookup"><span data-stu-id="075f2-189">2</span></span>  <br/> |<span data-ttu-id="075f2-190">ElementData フィールドのサイズをバイト単位 **で指定** します。</span><span class="sxs-lookup"><span data-stu-id="075f2-190">Specifies the size, in bytes, of the **ElementData** field.</span></span>  <br/> |
|<span data-ttu-id="075f2-191">**ElementData**</span><span class="sxs-lookup"><span data-stu-id="075f2-191">**ElementData**</span></span> <br/> |<span data-ttu-id="075f2-192">バイナリ データの配列</span><span class="sxs-lookup"><span data-stu-id="075f2-192">array of binary data</span></span>  <br/> |<span data-ttu-id="075f2-193">変数</span><span class="sxs-lookup"><span data-stu-id="075f2-193">variable</span></span>  <br/> |<span data-ttu-id="075f2-194">この **PersistID ElementID ペアの**  +  **データを格納** します。</span><span class="sxs-lookup"><span data-stu-id="075f2-194">Contains the data for this **PersistID** + **ElementID** pair.</span></span>  <br/> |
   
<span data-ttu-id="075f2-195">**PersistElementType 値**</span><span class="sxs-lookup"><span data-stu-id="075f2-195">**PersistElementType Values**</span></span>

|<span data-ttu-id="075f2-196">**名前**</span><span class="sxs-lookup"><span data-stu-id="075f2-196">**Name**</span></span>|<span data-ttu-id="075f2-197">**Value**</span><span class="sxs-lookup"><span data-stu-id="075f2-197">**Value**</span></span>|<span data-ttu-id="075f2-198">**ElementDataSize の値**</span><span class="sxs-lookup"><span data-stu-id="075f2-198">**Value of ElementDataSize**</span></span>|<span data-ttu-id="075f2-199">**説明**</span><span class="sxs-lookup"><span data-stu-id="075f2-199">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="075f2-200">RSF_ELID_HEADER</span><span class="sxs-lookup"><span data-stu-id="075f2-200">RSF_ELID_HEADER</span></span>  <br/> |<span data-ttu-id="075f2-201">0x0002</span><span class="sxs-lookup"><span data-stu-id="075f2-201">0x0002</span></span>  <br/> |<span data-ttu-id="075f2-202">0x0004</span><span class="sxs-lookup"><span data-stu-id="075f2-202">0x0004</span></span>  <br/> |<span data-ttu-id="075f2-203">このブロックの **ElementData** フィールドに DWORD ヘッダー値が含まれているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="075f2-203">Indicates that this block's **ElementData** field contains a DWORD Header value.</span></span> <span data-ttu-id="075f2-204">この値の解釈方法は、ブロックの **PersistID 型によって異** なります。</span><span class="sxs-lookup"><span data-stu-id="075f2-204">How this value is interpreted depends on the block's **PersistID** type.</span></span>  <br/> <span data-ttu-id="075f2-205">[[MS-OXOSFLD] で](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb.aspx)指定された **PersistID** 型の場合、この値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="075f2-205">For all **PersistID** types specified in [[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb.aspx), this value is zero.</span></span>  <br/> |
|<span data-ttu-id="075f2-206">RSF_ELID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="075f2-206">RSF_ELID_ENTRYID</span></span>  <br/> |<span data-ttu-id="075f2-207">0x0001</span><span class="sxs-lookup"><span data-stu-id="075f2-207">0x0001</span></span>  <br/> |<span data-ttu-id="075f2-208">変数</span><span class="sxs-lookup"><span data-stu-id="075f2-208">variable</span></span>  <br/> |<span data-ttu-id="075f2-209">このブロックに **、PersistID** で指定されたフォルダーの **EntryID が含まれるかどうかを示します**。</span><span class="sxs-lookup"><span data-stu-id="075f2-209">Indicates that this block contains the **EntryID** of the folder specified by **PersistID**.</span></span>  <br/> |
|<span data-ttu-id="075f2-210">ELEMENT_SENTINEL</span><span class="sxs-lookup"><span data-stu-id="075f2-210">ELEMENT_SENTINEL</span></span>  <br/> |<span data-ttu-id="075f2-211">0x0000</span><span class="sxs-lookup"><span data-stu-id="075f2-211">0x0000</span></span>  <br/> |<span data-ttu-id="075f2-212">0x0000</span><span class="sxs-lookup"><span data-stu-id="075f2-212">0x0000</span></span>  <br/> |<span data-ttu-id="075f2-213">**PersistElement** ブロックが処理されなきを示します。</span><span class="sxs-lookup"><span data-stu-id="075f2-213">Indicates that no more **PersistElement** blocks will be processed.</span></span>  <br/> |
   
<span data-ttu-id="075f2-214">**PersistElementType** 値がここで定義されている値の 1 つではない場合 **、PersistElement** ブロックは無視され、ELEMENT_SENTINEL **ElementID** が処理されるまで、またはストリームの末尾に達するまで処理が継続されます。</span><span class="sxs-lookup"><span data-stu-id="075f2-214">If the **PersistElementType** value is not one of the ones defined here, the **PersistElement** block is ignored and processing is continued until either an ELEMENT_SENTINEL **ElementID** is processed or the end of the stream is reached.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="075f2-215">関連リソース</span><span class="sxs-lookup"><span data-stu-id="075f2-215">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="075f2-216">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="075f2-216">Protocol specifications</span></span>

<span data-ttu-id="075f2-217">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="075f2-217">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="075f2-218">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="075f2-218">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="075f2-219">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="075f2-219">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="075f2-220">許可/ブロック リストの処理と迷惑メール メッセージの決定を有効にできます。</span><span class="sxs-lookup"><span data-stu-id="075f2-220">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="075f2-221">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="075f2-221">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="075f2-222">メールボックス内の特別なフォルダーを作成および検索するためのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="075f2-222">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="075f2-223">[[MS-OXPHISH]](https://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="075f2-223">[[MS-OXPHISH]](https://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="075f2-224">受信者を騙して機密情報 (パスワードや他の個人情報など) を信頼できないソースに開示するように設計された電子メール メッセージを識別およびマークします。</span><span class="sxs-lookup"><span data-stu-id="075f2-224">Identifies and marks email messages that are designed to trick recipients into divulging sensitive information (such as passwords and other personal information) to a non-trustworthy source.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="075f2-225">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="075f2-225">Header files</span></span>

<span data-ttu-id="075f2-226">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="075f2-226">Mapitags.h</span></span>
  
> <span data-ttu-id="075f2-227">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="075f2-227">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="075f2-228">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="075f2-228">Mapidefs.h</span></span>
  
> <span data-ttu-id="075f2-229">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="075f2-229">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="075f2-230">関連項目</span><span class="sxs-lookup"><span data-stu-id="075f2-230">See also</span></span>



[<span data-ttu-id="075f2-231">MAPI のプロパティの概要</span><span class="sxs-lookup"><span data-stu-id="075f2-231">MAPI Property Overview</span></span>](mapi-property-overview.md)
  
[<span data-ttu-id="075f2-232">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="075f2-232">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="075f2-233">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="075f2-233">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="075f2-234">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="075f2-234">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

