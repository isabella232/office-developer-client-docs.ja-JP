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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 57ab68d4c53693c769a4aadf8737f57ef5e73fcd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335204"
---
# <a name="pidtagadditionalrenentryidsex-canonical-property"></a><span data-ttu-id="2ae13-103">PidTagAdditionalRenEntryIdsEx 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2ae13-103">PidTagAdditionalRenEntryIdsEx Canonical Property</span></span>

  
  
<span data-ttu-id="2ae13-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ae13-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ae13-105">store オブジェクトの特別なフォルダーエントリ id が格納されています。</span><span class="sxs-lookup"><span data-stu-id="2ae13-105">Contains special folder entry IDs for a store object.</span></span> <span data-ttu-id="2ae13-106">この複数値を持つプロパティの各エントリは、1つまたは複数のエントリ id にマップできます。つまり、エントリとそれに関連付けられたエントリ id との間に一対多の関係があります。</span><span class="sxs-lookup"><span data-stu-id="2ae13-106">Each entry in this multi-valued property can be mapped to one or more entry IDs, that is, there is a one-to-many relationship between an entry and its associated entry IDs.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2ae13-107">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="2ae13-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="2ae13-108">PR_ADDITIONAL_REN_ENTRYIDS_EX</span><span class="sxs-lookup"><span data-stu-id="2ae13-108">PR_ADDITIONAL_REN_ENTRYIDS_EX</span></span>  <br/> |
|<span data-ttu-id="2ae13-109">識別子:</span><span class="sxs-lookup"><span data-stu-id="2ae13-109">Identifier:</span></span>  <br/> |<span data-ttu-id="2ae13-110">0x36D9</span><span class="sxs-lookup"><span data-stu-id="2ae13-110">0x36D9</span></span>  <br/> |
|<span data-ttu-id="2ae13-111">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="2ae13-111">Data type:</span></span>  <br/> |<span data-ttu-id="2ae13-112">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="2ae13-112">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="2ae13-113">エリア:</span><span class="sxs-lookup"><span data-stu-id="2ae13-113">Area:</span></span>  <br/> |<span data-ttu-id="2ae13-114">Outlook アプリケーション</span><span class="sxs-lookup"><span data-stu-id="2ae13-114">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2ae13-115">解説</span><span class="sxs-lookup"><span data-stu-id="2ae13-115">Remarks</span></span>

<span data-ttu-id="2ae13-116">このプロパティを使用すると、フォルダーのエントリ id を指定するブロックの配列が含まれます。</span><span class="sxs-lookup"><span data-stu-id="2ae13-116">If this property is used, it contains an array of blocks that specifies the entry IDs for the folders.</span></span> <span data-ttu-id="2ae13-117">ブロックは、次の4つの表で指定された形式に従います。</span><span class="sxs-lookup"><span data-stu-id="2ae13-117">The blocks follow the format specified by the following four tables.</span></span>
  
<span data-ttu-id="2ae13-118">**persistdata ブロック**</span><span class="sxs-lookup"><span data-stu-id="2ae13-118">**PersistData Block**</span></span>

|<span data-ttu-id="2ae13-119">**名前**</span><span class="sxs-lookup"><span data-stu-id="2ae13-119">**Name**</span></span>|<span data-ttu-id="2ae13-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="2ae13-120">**Type**</span></span>|<span data-ttu-id="2ae13-121">**Size**</span><span class="sxs-lookup"><span data-stu-id="2ae13-121">**Size**</span></span>|<span data-ttu-id="2ae13-122">**説明**</span><span class="sxs-lookup"><span data-stu-id="2ae13-122">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2ae13-123">**persistid**</span><span class="sxs-lookup"><span data-stu-id="2ae13-123">**PersistID**</span></span> <br/> |<span data-ttu-id="2ae13-124">WORD</span><span class="sxs-lookup"><span data-stu-id="2ae13-124">WORD</span></span>  <br/> |<span data-ttu-id="2ae13-125">pbm-2</span><span class="sxs-lookup"><span data-stu-id="2ae13-125">2</span></span>  <br/> |<span data-ttu-id="2ae13-126">この**persistdata**エントリの型識別子の値。</span><span class="sxs-lookup"><span data-stu-id="2ae13-126">Type identifier value for this **PersistData** entry.</span></span> <span data-ttu-id="2ae13-127">有効な値の一覧については、「persistblocktype Values」テーブルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2ae13-127">See the "PersistBlockType Values" table for the list of valid values.</span></span>  <br/> |
|<span data-ttu-id="2ae13-128">**data要素サイズ**</span><span class="sxs-lookup"><span data-stu-id="2ae13-128">**DataElementsSize**</span></span> <br/> |<span data-ttu-id="2ae13-129">WORD</span><span class="sxs-lookup"><span data-stu-id="2ae13-129">WORD</span></span>  <br/> |<span data-ttu-id="2ae13-130">pbm-2</span><span class="sxs-lookup"><span data-stu-id="2ae13-130">2</span></span>  <br/> |<span data-ttu-id="2ae13-131">**dataelements**フィールドのサイズ (バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="2ae13-131">Size, in bytes, of the **DataElements** field.</span></span>  <br/> |
|<span data-ttu-id="2ae13-132">**dataelements**</span><span class="sxs-lookup"><span data-stu-id="2ae13-132">**DataElements**</span></span> <br/> |<span data-ttu-id="2ae13-133">**persistelement**ブロックの配列</span><span class="sxs-lookup"><span data-stu-id="2ae13-133">array of **PersistElement** blocks</span></span>  <br/> |<span data-ttu-id="2ae13-134">変数</span><span class="sxs-lookup"><span data-stu-id="2ae13-134">variable</span></span>  <br/> |<span data-ttu-id="2ae13-135">ストアに存在する**persistelement**エントリの数を示します。</span><span class="sxs-lookup"><span data-stu-id="2ae13-135">Indicates how many **PersistElement** entries exist for the store.</span></span> <span data-ttu-id="2ae13-136">この構造体の形式については、「persistelement Block」の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2ae13-136">See the "PersistElement Block" table for the format of this structure.</span></span>  <br/> |
   
<span data-ttu-id="2ae13-137">**persistblocktype の値**</span><span class="sxs-lookup"><span data-stu-id="2ae13-137">**PersistBlockType Values**</span></span>

|<span data-ttu-id="2ae13-138">**Name**</span><span class="sxs-lookup"><span data-stu-id="2ae13-138">**Name**</span></span>|<span data-ttu-id="2ae13-139">**値**</span><span class="sxs-lookup"><span data-stu-id="2ae13-139">**Value**</span></span>|<span data-ttu-id="2ae13-140">**説明**</span><span class="sxs-lookup"><span data-stu-id="2ae13-140">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2ae13-141">PERSIST_SENTINEL</span><span class="sxs-lookup"><span data-stu-id="2ae13-141">PERSIST_SENTINEL</span></span>  <br/> |<span data-ttu-id="2ae13-142">0x0000</span><span class="sxs-lookup"><span data-stu-id="2ae13-142">0x0000</span></span>  <br/> |<span data-ttu-id="2ae13-143">これ以上の**persistdata**ブロックは処理されないことを示します。</span><span class="sxs-lookup"><span data-stu-id="2ae13-143">Indicates that no more **PersistData** blocks will be processed.</span></span>  <br/> |
|<span data-ttu-id="2ae13-144">RSF_PID_RSS_SUBSCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2ae13-144">RSF_PID_RSS_SUBSCRIPTION</span></span>  <br/> |<span data-ttu-id="2ae13-145">0x8001</span><span class="sxs-lookup"><span data-stu-id="2ae13-145">0x8001</span></span>  <br/> |<span data-ttu-id="2ae13-146">このブロックには、RSS 購読フォルダーのデータが含まれていることを示します。</span><span class="sxs-lookup"><span data-stu-id="2ae13-146">Indicates that this block contains data for the RSS Subscriptions folder.</span></span>  <br/> |
|<span data-ttu-id="2ae13-147">RSF_PID_SEND_AND_TRACK</span><span class="sxs-lookup"><span data-stu-id="2ae13-147">RSF_PID_SEND_AND_TRACK</span></span>  <br/> |<span data-ttu-id="2ae13-148">0x8002</span><span class="sxs-lookup"><span data-stu-id="2ae13-148">0x8002</span></span>  <br/> |<span data-ttu-id="2ae13-149">このブロックには、追跡対象メール処理フォルダーのデータが含まれていることを示します。</span><span class="sxs-lookup"><span data-stu-id="2ae13-149">Indicates that this block contains data for the Tracked Mail Processing folder.</span></span>  <br/> |
|<span data-ttu-id="2ae13-150">RSF_PID_TODO_SEARCH</span><span class="sxs-lookup"><span data-stu-id="2ae13-150">RSF_PID_TODO_SEARCH</span></span>  <br/> |<span data-ttu-id="2ae13-151">0x8004</span><span class="sxs-lookup"><span data-stu-id="2ae13-151">0x8004</span></span>  <br/> |<span data-ttu-id="2ae13-152">このブロックに、To do 検索フォルダーのデータが含まれていることを示します。</span><span class="sxs-lookup"><span data-stu-id="2ae13-152">Indicates that this block contains data for the To-Do Search folder.</span></span>  <br/> |
|<span data-ttu-id="2ae13-153">RSF_PID_CONV_ACTIONS</span><span class="sxs-lookup"><span data-stu-id="2ae13-153">RSF_PID_CONV_ACTIONS</span></span>  <br/> |<span data-ttu-id="2ae13-154">0x8006</span><span class="sxs-lookup"><span data-stu-id="2ae13-154">0x8006</span></span>  <br/> |<span data-ttu-id="2ae13-155">このブロックに、会話アクション設定フォルダーのデータが含まれていることを示します。</span><span class="sxs-lookup"><span data-stu-id="2ae13-155">Indicates that this block contains data for the Conversation Action Settings folder.</span></span>  <br/> |
|<span data-ttu-id="2ae13-156">RSF_PID_COMBINED_ACTIONS</span><span class="sxs-lookup"><span data-stu-id="2ae13-156">RSF_PID_COMBINED_ACTIONS</span></span>  <br/> |<span data-ttu-id="2ae13-157">0x8007</span><span class="sxs-lookup"><span data-stu-id="2ae13-157">0x8007</span></span>  <br/> |<span data-ttu-id="2ae13-158">この値は予約されています。</span><span class="sxs-lookup"><span data-stu-id="2ae13-158">This value is reserved.</span></span>  <br/> |
|<span data-ttu-id="2ae13-159">RSF_PID_SUGGESTED_CONTACTS</span><span class="sxs-lookup"><span data-stu-id="2ae13-159">RSF_PID_SUGGESTED_CONTACTS</span></span>  <br/> |<span data-ttu-id="2ae13-160">0x8008</span><span class="sxs-lookup"><span data-stu-id="2ae13-160">0x8008</span></span>  <br/> |<span data-ttu-id="2ae13-161">このブロックには、推奨される連絡先フォルダーのデータが含まれていることを示します。</span><span class="sxs-lookup"><span data-stu-id="2ae13-161">Indicates that this block contains data for the Suggested Contacts folder.</span></span>  <br/> |
|<span data-ttu-id="2ae13-162">RSF_PID_CONTACT_SEARCH</span><span class="sxs-lookup"><span data-stu-id="2ae13-162">RSF_PID_CONTACT_SEARCH</span></span>  <br/> |<span data-ttu-id="2ae13-163">0x8009</span><span class="sxs-lookup"><span data-stu-id="2ae13-163">0x8009</span></span>  <br/> |<span data-ttu-id="2ae13-164">このブロックに、連絡先検索フォルダーのデータが含まれていることを示します。</span><span class="sxs-lookup"><span data-stu-id="2ae13-164">Indicates that this block contains data for the Contacts Search folder.</span></span>  <br/> <span data-ttu-id="2ae13-165">Outlook でのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="2ae13-165">Used only by Outlook.</span></span>  <br/> |
|<span data-ttu-id="2ae13-166">RSF_PID_BUDDYLIST_PDLS</span><span class="sxs-lookup"><span data-stu-id="2ae13-166">RSF_PID_BUDDYLIST_PDLS</span></span>  <br/> |<span data-ttu-id="2ae13-167">0x800a</span><span class="sxs-lookup"><span data-stu-id="2ae13-167">0x800A</span></span>  <br/> |<span data-ttu-id="2ae13-168">このブロックに、インスタントメッセージング (IM) 連絡先リストフォルダーのデータが含まれていることを示します。</span><span class="sxs-lookup"><span data-stu-id="2ae13-168">Indicates that this block contains data for the Instant Messaging (IM) Contact Lists folder.</span></span> <span data-ttu-id="2ae13-169">参照フォルダーには、IM 連絡先リスト内の各グループを表す個人用配布リスト (pdls) が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2ae13-169">The referenced folder contains Personal Distribution Lists (PDLs) representing each group within the IM Contact list.</span></span>  <br/> <span data-ttu-id="2ae13-170">Outlook と Exchange の両方で使用されます。</span><span class="sxs-lookup"><span data-stu-id="2ae13-170">Used by both Outlook and Exchange.</span></span>  <br/> |
|<span data-ttu-id="2ae13-171">RSF_PID_BUDDYLIST_CONTACTS</span><span class="sxs-lookup"><span data-stu-id="2ae13-171">RSF_PID_BUDDYLIST_CONTACTS</span></span>  <br/> |<span data-ttu-id="2ae13-172">0x800b</span><span class="sxs-lookup"><span data-stu-id="2ae13-172">0x800B</span></span>  <br/> |<span data-ttu-id="2ae13-173">このブロックには、IM 連絡先フォルダーのデータが含まれていることを示します。</span><span class="sxs-lookup"><span data-stu-id="2ae13-173">Indicates that this block contains data for the IM Contacts folder.</span></span> <span data-ttu-id="2ae13-174">参照フォルダーには、IM 連絡先リストグループによって参照される個々の連絡先が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2ae13-174">The referenced folder contains the individual contacts referenced by the IM Contact List groups.</span></span>  <br/> <span data-ttu-id="2ae13-175">Outlook と Exchange の両方で使用されます。</span><span class="sxs-lookup"><span data-stu-id="2ae13-175">Used by both Outlook and Exchange.</span></span>  <br/> |
   
<span data-ttu-id="2ae13-176">**persistblocktype**値がここで定義されていない場合、 **persistdata**ブロックは無視され、PERSIST_SENTINEL **persistid**が処理されるか、またはストリームの終わりに達するまで、処理は続行されます。</span><span class="sxs-lookup"><span data-stu-id="2ae13-176">If the **PersistBlockType** value is not one of the ones defined here, the **PersistData** block is ignored and processing is continued until either a PERSIST_SENTINEL **PersistID** is processed or the end of the stream is reached.</span></span> 
  
<span data-ttu-id="2ae13-177">**persistelementblock**</span><span class="sxs-lookup"><span data-stu-id="2ae13-177">**PersistElementBlock**</span></span>

|<span data-ttu-id="2ae13-178">**名前**</span><span class="sxs-lookup"><span data-stu-id="2ae13-178">**Name**</span></span>|<span data-ttu-id="2ae13-179">**Type**</span><span class="sxs-lookup"><span data-stu-id="2ae13-179">**Type**</span></span>|<span data-ttu-id="2ae13-180">**Size**</span><span class="sxs-lookup"><span data-stu-id="2ae13-180">**Size**</span></span>|<span data-ttu-id="2ae13-181">**説明**</span><span class="sxs-lookup"><span data-stu-id="2ae13-181">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2ae13-182">**ElementID**</span><span class="sxs-lookup"><span data-stu-id="2ae13-182">**ElementID**</span></span> <br/> |<span data-ttu-id="2ae13-183">WORD</span><span class="sxs-lookup"><span data-stu-id="2ae13-183">WORD</span></span>  <br/> |<span data-ttu-id="2ae13-184">pbm-2</span><span class="sxs-lookup"><span data-stu-id="2ae13-184">2</span></span>  <br/> |<span data-ttu-id="2ae13-185">この**persistelement**ブロックの型識別子の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="2ae13-185">Specifies the type identifier value for this **PersistElement** block.</span></span> <span data-ttu-id="2ae13-186">有効な値の一覧については、「persistelementtype Values」テーブルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2ae13-186">See the "PersistElementType Values" table for a list of valid values.</span></span>  <br/> |
|<span data-ttu-id="2ae13-187">**elementdatasize**</span><span class="sxs-lookup"><span data-stu-id="2ae13-187">**ElementDataSize**</span></span> <br/> |<span data-ttu-id="2ae13-188">WORD</span><span class="sxs-lookup"><span data-stu-id="2ae13-188">WORD</span></span>  <br/> |<span data-ttu-id="2ae13-189">pbm-2</span><span class="sxs-lookup"><span data-stu-id="2ae13-189">2</span></span>  <br/> |<span data-ttu-id="2ae13-190">**elementdata**フィールドのサイズをバイト単位で指定します。</span><span class="sxs-lookup"><span data-stu-id="2ae13-190">Specifies the size, in bytes, of the **ElementData** field.</span></span>  <br/> |
|<span data-ttu-id="2ae13-191">**elementdata**</span><span class="sxs-lookup"><span data-stu-id="2ae13-191">**ElementData**</span></span> <br/> |<span data-ttu-id="2ae13-192">バイナリデータの配列</span><span class="sxs-lookup"><span data-stu-id="2ae13-192">array of binary data</span></span>  <br/> |<span data-ttu-id="2ae13-193">変数</span><span class="sxs-lookup"><span data-stu-id="2ae13-193">variable</span></span>  <br/> |<span data-ttu-id="2ae13-194">この**persistid** + の**ElementID**ペアのデータを格納します。</span><span class="sxs-lookup"><span data-stu-id="2ae13-194">Contains the data for this **PersistID** + **ElementID** pair.</span></span>  <br/> |
   
<span data-ttu-id="2ae13-195">**persistelementtype の値**</span><span class="sxs-lookup"><span data-stu-id="2ae13-195">**PersistElementType Values**</span></span>

|<span data-ttu-id="2ae13-196">**Name**</span><span class="sxs-lookup"><span data-stu-id="2ae13-196">**Name**</span></span>|<span data-ttu-id="2ae13-197">**Value**</span><span class="sxs-lookup"><span data-stu-id="2ae13-197">**Value**</span></span>|<span data-ttu-id="2ae13-198">**elementdatasize の値**</span><span class="sxs-lookup"><span data-stu-id="2ae13-198">**Value of ElementDataSize**</span></span>|<span data-ttu-id="2ae13-199">**説明**</span><span class="sxs-lookup"><span data-stu-id="2ae13-199">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2ae13-200">RSF_ELID_HEADER</span><span class="sxs-lookup"><span data-stu-id="2ae13-200">RSF_ELID_HEADER</span></span>  <br/> |<span data-ttu-id="2ae13-201">0x0002</span><span class="sxs-lookup"><span data-stu-id="2ae13-201">0x0002</span></span>  <br/> |<span data-ttu-id="2ae13-202">0x0004</span><span class="sxs-lookup"><span data-stu-id="2ae13-202">0x0004</span></span>  <br/> |<span data-ttu-id="2ae13-203">このブロックの**elementdata**フィールドに DWORD ヘッダーの値が含まれていることを示します。</span><span class="sxs-lookup"><span data-stu-id="2ae13-203">Indicates that this block's **ElementData** field contains a DWORD Header value.</span></span> <span data-ttu-id="2ae13-204">この値がどのように解釈されるかは、ブロックの**persistid**型によって異なります。</span><span class="sxs-lookup"><span data-stu-id="2ae13-204">How this value is interpreted depends on the block's **PersistID** type.</span></span>  <br/> <span data-ttu-id="2ae13-205">[[OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb.aspx)で指定されているすべての**persistid**型の場合、この値は0です。</span><span class="sxs-lookup"><span data-stu-id="2ae13-205">For all **PersistID** types specified in [[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb.aspx), this value is zero.</span></span>  <br/> |
|<span data-ttu-id="2ae13-206">RSF_ELID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="2ae13-206">RSF_ELID_ENTRYID</span></span>  <br/> |<span data-ttu-id="2ae13-207">0x0001</span><span class="sxs-lookup"><span data-stu-id="2ae13-207">0x0001</span></span>  <br/> |<span data-ttu-id="2ae13-208">変数</span><span class="sxs-lookup"><span data-stu-id="2ae13-208">variable</span></span>  <br/> |<span data-ttu-id="2ae13-209">このブロックには、 **persistid**で指定されたフォルダーの**EntryID**が含まれていることを示します。</span><span class="sxs-lookup"><span data-stu-id="2ae13-209">Indicates that this block contains the **EntryID** of the folder specified by **PersistID**.</span></span>  <br/> |
|<span data-ttu-id="2ae13-210">ELEMENT_SENTINEL</span><span class="sxs-lookup"><span data-stu-id="2ae13-210">ELEMENT_SENTINEL</span></span>  <br/> |<span data-ttu-id="2ae13-211">0x0000</span><span class="sxs-lookup"><span data-stu-id="2ae13-211">0x0000</span></span>  <br/> |<span data-ttu-id="2ae13-212">0x0000</span><span class="sxs-lookup"><span data-stu-id="2ae13-212">0x0000</span></span>  <br/> |<span data-ttu-id="2ae13-213">これ以上、 **persistelement**ブロックが処理されないことを示します。</span><span class="sxs-lookup"><span data-stu-id="2ae13-213">Indicates that no more **PersistElement** blocks will be processed.</span></span>  <br/> |
   
<span data-ttu-id="2ae13-214">**persistelementtype**の値がここで定義されている値ではない場合、 **persistelementtype**ブロックは無視され、ELEMENT_SENTINEL **ElementID**が処理されるか、またはストリームの終わりに達するまで、処理は続行されます。</span><span class="sxs-lookup"><span data-stu-id="2ae13-214">If the **PersistElementType** value is not one of the ones defined here, the **PersistElement** block is ignored and processing is continued until either an ELEMENT_SENTINEL **ElementID** is processed or the end of the stream is reached.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2ae13-215">関連リソース</span><span class="sxs-lookup"><span data-stu-id="2ae13-215">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2ae13-216">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="2ae13-216">Protocol specifications</span></span>

<span data-ttu-id="2ae13-217">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2ae13-217">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2ae13-218">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="2ae13-218">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2ae13-219">[[OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2ae13-219">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2ae13-220">許可/ブロックリストの処理と、迷惑メールメッセージの決定を有効にします。</span><span class="sxs-lookup"><span data-stu-id="2ae13-220">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="2ae13-221">[[OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2ae13-221">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2ae13-222">メールボックス内の特別なフォルダーを作成および検索するためのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="2ae13-222">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="2ae13-223">[[OXPHISH]](https://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2ae13-223">[[MS-OXPHISH]](https://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2ae13-224">受信者を漏洩機密情報 (パスワードやその他の個人情報など) に信頼できないソースに誘導するように設計された電子メールメッセージを識別してマークします。</span><span class="sxs-lookup"><span data-stu-id="2ae13-224">Identifies and marks email messages that are designed to trick recipients into divulging sensitive information (such as passwords and other personal information) to a non-trustworthy source.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2ae13-225">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="2ae13-225">Header files</span></span>

<span data-ttu-id="2ae13-226">Mapitags</span><span class="sxs-lookup"><span data-stu-id="2ae13-226">Mapitags.h</span></span>
  
> <span data-ttu-id="2ae13-227">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="2ae13-227">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="2ae13-228">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2ae13-228">Mapidefs.h</span></span>
  
> <span data-ttu-id="2ae13-229">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="2ae13-229">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2ae13-230">関連項目</span><span class="sxs-lookup"><span data-stu-id="2ae13-230">See also</span></span>



[<span data-ttu-id="2ae13-231">MAPI のプロパティの概要</span><span class="sxs-lookup"><span data-stu-id="2ae13-231">MAPI Property Overview</span></span>](mapi-property-overview.md)
  
[<span data-ttu-id="2ae13-232">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2ae13-232">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2ae13-233">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2ae13-233">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2ae13-234">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2ae13-234">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

