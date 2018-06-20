---
title: PidTagAdditionalRenEntryIdsEx の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: d3a8dc45bb131f5d2e7ff370617a10e3096a99f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802431"
---
# <a name="pidtagadditionalrenentryidsex-canonical-property"></a><span data-ttu-id="f0ee8-103">PidTagAdditionalRenEntryIdsEx の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="f0ee8-103">PidTagAdditionalRenEntryIdsEx Canonical Property</span></span>

  
  
<span data-ttu-id="f0ee8-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f0ee8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f0ee8-105">ストア オブジェクトの特別なフォルダーのエントリ Id が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-105">Contains special folder entry IDs for a store object.</span></span> <span data-ttu-id="f0ee8-106">この複数値プロパティ内の各エントリは、1 つまたは複数のエントリ Id にマップすることができます、つまり、エントリとその関連付けられたエントリ Id との間の一対多リレーションシップがあります。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-106">Each entry in this multi-valued property can be mapped to one or more entry IDs, that is, there is a one-to-many relationship between an entry and its associated entry IDs.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f0ee8-107">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="f0ee8-108">PR_ADDITIONAL_REN_ENTRYIDS_EX</span><span class="sxs-lookup"><span data-stu-id="f0ee8-108">PR_ADDITIONAL_REN_ENTRYIDS_EX</span></span>  <br/> |
|<span data-ttu-id="f0ee8-109">識別子:</span><span class="sxs-lookup"><span data-stu-id="f0ee8-109">Identifier:</span></span>  <br/> |<span data-ttu-id="f0ee8-110">0x36D9</span><span class="sxs-lookup"><span data-stu-id="f0ee8-110">0x36D9</span></span>  <br/> |
|<span data-ttu-id="f0ee8-111">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-111">Data type:</span></span>  <br/> |<span data-ttu-id="f0ee8-112">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f0ee8-112">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f0ee8-113">領域:</span><span class="sxs-lookup"><span data-stu-id="f0ee8-113">Area:</span></span>  <br/> |<span data-ttu-id="f0ee8-114">Outlook アプリケーション</span><span class="sxs-lookup"><span data-stu-id="f0ee8-114">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f0ee8-115">備考</span><span class="sxs-lookup"><span data-stu-id="f0ee8-115">Remarks</span></span>

<span data-ttu-id="f0ee8-116">このプロパティを使用する場合、フォルダーのエントリ Id を指定するブロックの配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-116">If this property is used, it contains an array of blocks that specifies the entry IDs for the folders.</span></span> <span data-ttu-id="f0ee8-117">ブロックは、次の 4 つのテーブルで指定された形式に従います。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-117">The blocks follow the format specified by the following four tables.</span></span>
  
<span data-ttu-id="f0ee8-118">**ブロックのデータの保持**</span><span class="sxs-lookup"><span data-stu-id="f0ee8-118">**PersistData Block**</span></span>

|<span data-ttu-id="f0ee8-119">**名前**</span><span class="sxs-lookup"><span data-stu-id="f0ee8-119">**Name**</span></span>|<span data-ttu-id="f0ee8-120">**型**</span><span class="sxs-lookup"><span data-stu-id="f0ee8-120">**Type**</span></span>|<span data-ttu-id="f0ee8-121">**Size**</span><span class="sxs-lookup"><span data-stu-id="f0ee8-121">**Size**</span></span>|<span data-ttu-id="f0ee8-122">**説明**</span><span class="sxs-lookup"><span data-stu-id="f0ee8-122">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f0ee8-123">**PersistID**</span><span class="sxs-lookup"><span data-stu-id="f0ee8-123">**PersistID**</span></span> <br/> |<span data-ttu-id="f0ee8-124">WORD</span><span class="sxs-lookup"><span data-stu-id="f0ee8-124">WORD</span></span>  <br/> |<span data-ttu-id="f0ee8-125">2</span><span class="sxs-lookup"><span data-stu-id="f0ee8-125">2</span></span>  <br/> |<span data-ttu-id="f0ee8-126">この**データの保持**のエントリの識別子の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-126">Type identifier value for this **PersistData** entry.</span></span> <span data-ttu-id="f0ee8-127">有効な値の一覧については PersistBlockType 値」の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-127">See the "PersistBlockType Values" table for the list of valid values.</span></span>  <br/> |
|<span data-ttu-id="f0ee8-128">**DataElementsSize**</span><span class="sxs-lookup"><span data-stu-id="f0ee8-128">**DataElementsSize**</span></span> <br/> |<span data-ttu-id="f0ee8-129">WORD</span><span class="sxs-lookup"><span data-stu-id="f0ee8-129">WORD</span></span>  <br/> |<span data-ttu-id="f0ee8-130">2</span><span class="sxs-lookup"><span data-stu-id="f0ee8-130">2</span></span>  <br/> |<span data-ttu-id="f0ee8-131">**DataElements**フィールドのバイト単位のサイズです。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-131">Size, in bytes, of the **DataElements** field.</span></span>  <br/> |
|<span data-ttu-id="f0ee8-132">**DataElements**</span><span class="sxs-lookup"><span data-stu-id="f0ee8-132">**DataElements**</span></span> <br/> |<span data-ttu-id="f0ee8-133">**PersistElement**ブロックの配列</span><span class="sxs-lookup"><span data-stu-id="f0ee8-133">array of **PersistElement** blocks</span></span>  <br/> |<span data-ttu-id="f0ee8-134">変数</span><span class="sxs-lookup"><span data-stu-id="f0ee8-134">variable</span></span>  <br/> |<span data-ttu-id="f0ee8-135">ストアの数の**PersistElement**エントリが存在することを示します。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-135">Indicates how many **PersistElement** entries exist for the store.</span></span> <span data-ttu-id="f0ee8-136">この構造体の形式については「PersistElement ・ ブロック」表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-136">See the "PersistElement Block" table for the format of this structure.</span></span>  <br/> |
   
<span data-ttu-id="f0ee8-137">**PersistBlockType 値**</span><span class="sxs-lookup"><span data-stu-id="f0ee8-137">**PersistBlockType Values**</span></span>

|<span data-ttu-id="f0ee8-138">**名前**</span><span class="sxs-lookup"><span data-stu-id="f0ee8-138">**Name**</span></span>|<span data-ttu-id="f0ee8-139">**値**</span><span class="sxs-lookup"><span data-stu-id="f0ee8-139">**Value**</span></span>|<span data-ttu-id="f0ee8-140">**説明**</span><span class="sxs-lookup"><span data-stu-id="f0ee8-140">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f0ee8-141">PERSIST_SENTINEL</span><span class="sxs-lookup"><span data-stu-id="f0ee8-141">PERSIST_SENTINEL</span></span>  <br/> |<span data-ttu-id="f0ee8-142">0x0000</span><span class="sxs-lookup"><span data-stu-id="f0ee8-142">0x0000</span></span>  <br/> |<span data-ttu-id="f0ee8-143">**データの保持**ブロックを処理することを示します。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-143">Indicates that no more **PersistData** blocks will be processed.</span></span>  <br/> |
|<span data-ttu-id="f0ee8-144">RSF_PID_RSS_SUBSCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f0ee8-144">RSF_PID_RSS_SUBSCRIPTION</span></span>  <br/> |<span data-ttu-id="f0ee8-145">0x8001</span><span class="sxs-lookup"><span data-stu-id="f0ee8-145">0x8001</span></span>  <br/> |<span data-ttu-id="f0ee8-146">このブロックに RSS 購読] フォルダーのデータが含まれていることを示します。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-146">Indicates that this block contains data for the RSS Subscriptions folder.</span></span>  <br/> |
|<span data-ttu-id="f0ee8-147">RSF_PID_SEND_AND_TRACK</span><span class="sxs-lookup"><span data-stu-id="f0ee8-147">RSF_PID_SEND_AND_TRACK</span></span>  <br/> |<span data-ttu-id="f0ee8-148">0x8002</span><span class="sxs-lookup"><span data-stu-id="f0ee8-148">0x8002</span></span>  <br/> |<span data-ttu-id="f0ee8-149">このブロックにメールの処理の履歴フォルダーのデータが含まれていることを示します。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-149">Indicates that this block contains data for the Tracked Mail Processing folder.</span></span>  <br/> |
|<span data-ttu-id="f0ee8-150">RSF_PID_TODO_SEARCH</span><span class="sxs-lookup"><span data-stu-id="f0ee8-150">RSF_PID_TODO_SEARCH</span></span>  <br/> |<span data-ttu-id="f0ee8-151">0x8004</span><span class="sxs-lookup"><span data-stu-id="f0ee8-151">0x8004</span></span>  <br/> |<span data-ttu-id="f0ee8-152">このブロックに to do の検索フォルダーのデータが含まれていることを示します。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-152">Indicates that this block contains data for the To-Do Search folder.</span></span>  <br/> |
|<span data-ttu-id="f0ee8-153">RSF_PID_CONV_ACTIONS</span><span class="sxs-lookup"><span data-stu-id="f0ee8-153">RSF_PID_CONV_ACTIONS</span></span>  <br/> |<span data-ttu-id="f0ee8-154">0x8006</span><span class="sxs-lookup"><span data-stu-id="f0ee8-154">0x8006</span></span>  <br/> |<span data-ttu-id="f0ee8-155">このブロックに、会話のアクションの設定] フォルダーのデータが含まれていることを示します。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-155">Indicates that this block contains data for the Conversation Action Settings folder.</span></span>  <br/> |
|<span data-ttu-id="f0ee8-156">RSF_PID_COMBINED_ACTIONS</span><span class="sxs-lookup"><span data-stu-id="f0ee8-156">RSF_PID_COMBINED_ACTIONS</span></span>  <br/> |<span data-ttu-id="f0ee8-157">0x8007</span><span class="sxs-lookup"><span data-stu-id="f0ee8-157">0x8007</span></span>  <br/> |<span data-ttu-id="f0ee8-158">この値は予約されています。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-158">This value is reserved.</span></span>  <br/> |
|<span data-ttu-id="f0ee8-159">RSF_PID_SUGGESTED_CONTACTS</span><span class="sxs-lookup"><span data-stu-id="f0ee8-159">RSF_PID_SUGGESTED_CONTACTS</span></span>  <br/> |<span data-ttu-id="f0ee8-160">0x8008</span><span class="sxs-lookup"><span data-stu-id="f0ee8-160">0x8008</span></span>  <br/> |<span data-ttu-id="f0ee8-161">このブロックに提案された連絡先フォルダーのデータが含まれていることを示します。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-161">Indicates that this block contains data for the Suggested Contacts folder.</span></span>  <br/> |
|<span data-ttu-id="f0ee8-162">RSF_PID_CONTACT_SEARCH</span><span class="sxs-lookup"><span data-stu-id="f0ee8-162">RSF_PID_CONTACT_SEARCH</span></span>  <br/> |<span data-ttu-id="f0ee8-163">0x8009</span><span class="sxs-lookup"><span data-stu-id="f0ee8-163">0x8009</span></span>  <br/> |<span data-ttu-id="f0ee8-164">このブロックに連絡先の検索フォルダーのデータが含まれていることを示します。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-164">Indicates that this block contains data for the Contacts Search folder.</span></span>  <br/> <span data-ttu-id="f0ee8-165">Outlook でのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-165">Used only by Outlook.</span></span>  <br/> |
|<span data-ttu-id="f0ee8-166">RSF_PID_BUDDYLIST_PDLS</span><span class="sxs-lookup"><span data-stu-id="f0ee8-166">RSF_PID_BUDDYLIST_PDLS</span></span>  <br/> |<span data-ttu-id="f0ee8-167">0x800A</span><span class="sxs-lookup"><span data-stu-id="f0ee8-167">0x800A</span></span>  <br/> |<span data-ttu-id="f0ee8-168">このブロックがインスタント メッセージング (IM) の連絡先リスト フォルダーのデータを格納することを示します。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-168">Indicates that this block contains data for the Instant Messaging (IM) Contact Lists folder.</span></span> <span data-ttu-id="f0ee8-169">個人用配布リスト (Pdl) IM の連絡先リストに含まれる各グループを表す、参照先のフォルダーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-169">The referenced folder contains Personal Distribution Lists (PDLs) representing each group within the IM Contact list.</span></span>  <br/> <span data-ttu-id="f0ee8-170">Outlook と Exchange の両方で使用されます。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-170">Used by both Outlook and Exchange.</span></span>  <br/> |
|<span data-ttu-id="f0ee8-171">RSF_PID_BUDDYLIST_CONTACTS</span><span class="sxs-lookup"><span data-stu-id="f0ee8-171">RSF_PID_BUDDYLIST_CONTACTS</span></span>  <br/> |<span data-ttu-id="f0ee8-172">0x800B</span><span class="sxs-lookup"><span data-stu-id="f0ee8-172">0x800B</span></span>  <br/> |<span data-ttu-id="f0ee8-173">このブロックに IM の連絡先フォルダーのデータが含まれていることを示します。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-173">Indicates that this block contains data for the IM Contacts folder.</span></span> <span data-ttu-id="f0ee8-174">参照先のフォルダーには、IM の連絡先リストのグループによって参照される個々 の連絡先が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-174">The referenced folder contains the individual contacts referenced by the IM Contact List groups.</span></span>  <br/> <span data-ttu-id="f0ee8-175">Outlook と Exchange の両方で使用されます。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-175">Used by both Outlook and Exchange.</span></span>  <br/> |
   
<span data-ttu-id="f0ee8-176">**PersistBlockType**の値がここで定義されているのいずれかでない場合は、**データの保持**のブロックは無視され、PERSIST_SENTINEL **PersistID**が処理されるか、ストリームの末尾に到達するまで処理は続行されます。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-176">If the **PersistBlockType** value is not one of the ones defined here, the **PersistData** block is ignored and processing is continued until either a PERSIST_SENTINEL **PersistID** is processed or the end of the stream is reached.</span></span> 
  
<span data-ttu-id="f0ee8-177">**PersistElementBlock**</span><span class="sxs-lookup"><span data-stu-id="f0ee8-177">**PersistElementBlock**</span></span>

|<span data-ttu-id="f0ee8-178">**名前**</span><span class="sxs-lookup"><span data-stu-id="f0ee8-178">**Name**</span></span>|<span data-ttu-id="f0ee8-179">**型**</span><span class="sxs-lookup"><span data-stu-id="f0ee8-179">**Type**</span></span>|<span data-ttu-id="f0ee8-180">**Size**</span><span class="sxs-lookup"><span data-stu-id="f0ee8-180">**Size**</span></span>|<span data-ttu-id="f0ee8-181">**説明**</span><span class="sxs-lookup"><span data-stu-id="f0ee8-181">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f0ee8-182">**ElementID**</span><span class="sxs-lookup"><span data-stu-id="f0ee8-182">**ElementID**</span></span> <br/> |<span data-ttu-id="f0ee8-183">WORD</span><span class="sxs-lookup"><span data-stu-id="f0ee8-183">WORD</span></span>  <br/> |<span data-ttu-id="f0ee8-184">2</span><span class="sxs-lookup"><span data-stu-id="f0ee8-184">2</span></span>  <br/> |<span data-ttu-id="f0ee8-185">**PersistElement**ブロックの型の識別子の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-185">Specifies the type identifier value for this **PersistElement** block.</span></span> <span data-ttu-id="f0ee8-186">有効な値の一覧については PersistElementType 値」の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-186">See the "PersistElementType Values" table for a list of valid values.</span></span>  <br/> |
|<span data-ttu-id="f0ee8-187">**ElementDataSize**</span><span class="sxs-lookup"><span data-stu-id="f0ee8-187">**ElementDataSize**</span></span> <br/> |<span data-ttu-id="f0ee8-188">WORD</span><span class="sxs-lookup"><span data-stu-id="f0ee8-188">WORD</span></span>  <br/> |<span data-ttu-id="f0ee8-189">2</span><span class="sxs-lookup"><span data-stu-id="f0ee8-189">2</span></span>  <br/> |<span data-ttu-id="f0ee8-190">**ElementData**フィールドのバイト単位のサイズを指定します。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-190">Specifies the size, in bytes, of the **ElementData** field.</span></span>  <br/> |
|<span data-ttu-id="f0ee8-191">**ElementData**</span><span class="sxs-lookup"><span data-stu-id="f0ee8-191">**ElementData**</span></span> <br/> |<span data-ttu-id="f0ee8-192">バイナリ データの配列</span><span class="sxs-lookup"><span data-stu-id="f0ee8-192">array of binary data</span></span>  <br/> |<span data-ttu-id="f0ee8-193">変数</span><span class="sxs-lookup"><span data-stu-id="f0ee8-193">variable</span></span>  <br/> |<span data-ttu-id="f0ee8-194">この**PersistID**のデータが含まれています + **ElementID**のペアです。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-194">Contains the data for this **PersistID** + **ElementID** pair.</span></span>  <br/> |
   
<span data-ttu-id="f0ee8-195">**PersistElementType 値**</span><span class="sxs-lookup"><span data-stu-id="f0ee8-195">**PersistElementType Values**</span></span>

|<span data-ttu-id="f0ee8-196">**名前**</span><span class="sxs-lookup"><span data-stu-id="f0ee8-196">**Name**</span></span>|<span data-ttu-id="f0ee8-197">**値**</span><span class="sxs-lookup"><span data-stu-id="f0ee8-197">**Value**</span></span>|<span data-ttu-id="f0ee8-198">**ElementDataSize の値**</span><span class="sxs-lookup"><span data-stu-id="f0ee8-198">**Value of ElementDataSize**</span></span>|<span data-ttu-id="f0ee8-199">**説明**</span><span class="sxs-lookup"><span data-stu-id="f0ee8-199">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f0ee8-200">RSF_ELID_HEADER</span><span class="sxs-lookup"><span data-stu-id="f0ee8-200">RSF_ELID_HEADER</span></span>  <br/> |<span data-ttu-id="f0ee8-201">0x0002</span><span class="sxs-lookup"><span data-stu-id="f0ee8-201">0x0002</span></span>  <br/> |<span data-ttu-id="f0ee8-202">0x0004</span><span class="sxs-lookup"><span data-stu-id="f0ee8-202">0x0004</span></span>  <br/> |<span data-ttu-id="f0ee8-203">**ElementData**フィールドこのブロックのにはヘッダーの DWORD 値が含まれていることを示します。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-203">Indicates that this block's **ElementData** field contains a DWORD Header value.</span></span> <span data-ttu-id="f0ee8-204">この値を解釈する方法は、ブロックの**PersistID**の種類によって異なります。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-204">How this value is interpreted depends on the block's **PersistID** type.</span></span>  <br/> <span data-ttu-id="f0ee8-205">[[MS OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb.aspx)で指定されたすべての**PersistID**の種類、この値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-205">For all **PersistID** types specified in [[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb.aspx), this value is zero.</span></span>  <br/> |
|<span data-ttu-id="f0ee8-206">RSF_ELID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="f0ee8-206">RSF_ELID_ENTRYID</span></span>  <br/> |<span data-ttu-id="f0ee8-207">0x0001</span><span class="sxs-lookup"><span data-stu-id="f0ee8-207">0x0001</span></span>  <br/> |<span data-ttu-id="f0ee8-208">変数</span><span class="sxs-lookup"><span data-stu-id="f0ee8-208">variable</span></span>  <br/> |<span data-ttu-id="f0ee8-209">このブロックに**PersistID**によって指定されたフォルダーの**エントリ Id**が含まれていることを示します。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-209">Indicates that this block contains the **EntryID** of the folder specified by **PersistID**.</span></span>  <br/> |
|<span data-ttu-id="f0ee8-210">ELEMENT_SENTINEL</span><span class="sxs-lookup"><span data-stu-id="f0ee8-210">ELEMENT_SENTINEL</span></span>  <br/> |<span data-ttu-id="f0ee8-211">0x0000</span><span class="sxs-lookup"><span data-stu-id="f0ee8-211">0x0000</span></span>  <br/> |<span data-ttu-id="f0ee8-212">0x0000</span><span class="sxs-lookup"><span data-stu-id="f0ee8-212">0x0000</span></span>  <br/> |<span data-ttu-id="f0ee8-213">**PersistElement**ブロックを処理することを示します。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-213">Indicates that no more **PersistElement** blocks will be processed.</span></span>  <br/> |
   
<span data-ttu-id="f0ee8-214">**PersistElementType**の値がここで定義されているのいずれかでない場合は、 **PersistElement**ブロックは無視され、ELEMENT_SENTINEL の**ElementID**が処理されるか、ストリームの末尾に到達するまで処理は続行されます。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-214">If the **PersistElementType** value is not one of the ones defined here, the **PersistElement** block is ignored and processing is continued until either an ELEMENT_SENTINEL **ElementID** is processed or the end of the stream is reached.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f0ee8-215">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f0ee8-215">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f0ee8-216">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="f0ee8-216">Protocol specifications</span></span>

<span data-ttu-id="f0ee8-217">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f0ee8-217">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f0ee8-218">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-218">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f0ee8-219">[[MS OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f0ee8-219">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f0ee8-220">許可/禁止リストの処理、迷惑メール メッセージの決定を可能にします。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-220">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="f0ee8-221">[[MS OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f0ee8-221">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f0ee8-222">プロパティを作成すると、メールボックス内の特別なフォルダーを検索する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-222">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="f0ee8-223">[[MS OXPHISH]](http://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f0ee8-223">[[MS-OXPHISH]](http://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f0ee8-224">識別し、だまして受信者 (パスワードやその他の個人情報) などの機密情報を盗み、以外の信頼できる発行元に設計された電子メール メッセージをマークします。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-224">Identifies and marks email messages that are designed to trick recipients into divulging sensitive information (such as passwords and other personal information) to a non-trustworthy source.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f0ee8-225">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f0ee8-225">Header files</span></span>

<span data-ttu-id="f0ee8-226">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f0ee8-226">Mapitags.h</span></span>
  
> <span data-ttu-id="f0ee8-227">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-227">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="f0ee8-228">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f0ee8-228">Mapidefs.h</span></span>
  
> <span data-ttu-id="f0ee8-229">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-229">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f0ee8-230">関連項目</span><span class="sxs-lookup"><span data-stu-id="f0ee8-230">See also</span></span>



[<span data-ttu-id="f0ee8-231">MAPI Property Overview</span><span class="sxs-lookup"><span data-stu-id="f0ee8-231">MAPI Property Overview</span></span>](mapi-property-overview.md)
  
[<span data-ttu-id="f0ee8-232">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f0ee8-232">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f0ee8-233">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="f0ee8-233">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f0ee8-234">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="f0ee8-234">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

