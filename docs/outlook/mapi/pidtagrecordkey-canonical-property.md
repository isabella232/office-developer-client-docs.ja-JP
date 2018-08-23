---
title: PidTagRecordKey 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecordKey
api_type:
- COM
ms.assetid: a12fb9a2-799d-4112-b26c-4b2854c47cc2
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9add9246cdfb22f7c5ad579f425932f49d4a9ecd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581245"
---
# <a name="pidtagrecordkey-canonical-property"></a><span data-ttu-id="e3d5f-103">PidTagRecordKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e3d5f-103">PidTagRecordKey Canonical Property</span></span>

  
  
<span data-ttu-id="e3d5f-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3d5f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3d5f-105">特定のオブジェクトのバイナリ比較が可能な一意の識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e3d5f-105">Contains a unique binary-comparable identifier for a specific object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e3d5f-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e3d5f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e3d5f-107">PR_RECORD_KEY</span><span class="sxs-lookup"><span data-stu-id="e3d5f-107">PR_RECORD_KEY</span></span>  <br/> |
|<span data-ttu-id="e3d5f-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e3d5f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e3d5f-109">0x0FF9</span><span class="sxs-lookup"><span data-stu-id="e3d5f-109">0x0FF9</span></span>  <br/> |
|<span data-ttu-id="e3d5f-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e3d5f-110">Data type:</span></span>  <br/> |<span data-ttu-id="e3d5f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e3d5f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e3d5f-112">領域:</span><span class="sxs-lookup"><span data-stu-id="e3d5f-112">Area:</span></span>  <br/> |<span data-ttu-id="e3d5f-113">ID プロパティ</span><span class="sxs-lookup"><span data-stu-id="e3d5f-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e3d5f-114">注釈</span><span class="sxs-lookup"><span data-stu-id="e3d5f-114">Remarks</span></span>

<span data-ttu-id="e3d5f-115">このプロパティには、内容のテーブル内の行を検索するなどのオブジェクトへの参照を検索が容易になります。</span><span class="sxs-lookup"><span data-stu-id="e3d5f-115">This property facilitates locating references to an object, such as finding its row in a contents table.</span></span> <span data-ttu-id="e3d5f-116">このプロパティは、オブジェクトを開くには使用できません。目的のためのエントリ id を使用します。</span><span class="sxs-lookup"><span data-stu-id="e3d5f-116">This property cannot be used to open an object; use the entry identifier for that purpose.</span></span>
  
<span data-ttu-id="e3d5f-117">添付ファイルのサブオブジェクトは、このプロパティによって、メッセージ内で一意に識別する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e3d5f-117">An attachment subobject should be uniquely identified within a message by this property.</span></span> <span data-ttu-id="e3d5f-118">この識別子は、常に同じメッセージが閉じられ、再オープン後に保証されるだけの添付ファイル特性です。</span><span class="sxs-lookup"><span data-stu-id="e3d5f-118">This identifier is the only attachment characteristic guaranteed to stay the same after the message is closed and reopened.</span></span> <span data-ttu-id="e3d5f-119">ストア プロバイダーは、この保証を確認するのにはセッション間でこのプロパティを保持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e3d5f-119">The store provider must preserve this property across sessions to ensure this guarantee.</span></span>
  
<span data-ttu-id="e3d5f-120">フォルダーは、このプロパティには、フォルダーの階層テーブルで使用されるキーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="e3d5f-120">For folders, this property contains a key used in the folder hierarchy table.</span></span> <span data-ttu-id="e3d5f-121">通常これは、 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティによって提供されるものと同じ値です。</span><span class="sxs-lookup"><span data-stu-id="e3d5f-121">Typically this is the same value as that provided by the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="e3d5f-122">メッセージ ・ ストアのこのプロパティでは、 **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)) のプロパティと同じです。</span><span class="sxs-lookup"><span data-stu-id="e3d5f-122">For message stores, this property is identical to the **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="e3d5f-123">メッセージ ストア オブジェクトでこのプロパティは、一意なすべてのストア プロバイダーで。</span><span class="sxs-lookup"><span data-stu-id="e3d5f-123">In a message store object, this property should be unique across all store providers.</span></span> <span data-ttu-id="e3d5f-124">これを行う方法の 1 つでは、 [GUID](guid.md)構造体、またはその他の値が特定のメッセージ ストアに固有のストア (そのプロバイダーの種類に固有) の**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) プロパティの値を結合します。</span><span class="sxs-lookup"><span data-stu-id="e3d5f-124">One way to do this is to combine the value of the **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) property for the store (unique to that provider type) with a [GUID](guid.md) structure or other value unique to the specific message store.</span></span> 
  
<span data-ttu-id="e3d5f-125">このプロパティは、常に[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドへの最初の呼び出しの後、 [IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="e3d5f-125">This property is always available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="e3d5f-126">一部のプロバイダーを使用する利用可能なインスタンス化後すぐに。</span><span class="sxs-lookup"><span data-stu-id="e3d5f-126">Some providers can make it available immediately after instantiation.</span></span> 
  
<span data-ttu-id="e3d5f-127">クライアントまたはサービス プロバイダーでは、ためを使用して、このプロパティの値を比較できます。</span><span class="sxs-lookup"><span data-stu-id="e3d5f-127">A client or service provider can compare values from this property by using memcmp.</span></span> <span data-ttu-id="e3d5f-128">エントリの識別子の値のことではありません。</span><span class="sxs-lookup"><span data-stu-id="e3d5f-128">This is not possible for entry identifier values.</span></span> <span data-ttu-id="e3d5f-129">ただし、このプロパティが保証される、同じメッセージ ・ ストア内で一意であるか、アドレス帳コンテナーです。別のコンテナーからの 2 つのオブジェクトには、このプロパティの値と同じことができます。</span><span class="sxs-lookup"><span data-stu-id="e3d5f-129">However, this property is guaranteed to be unique within the same message store or address book container; two objects from different containers can have the same value of this property.</span></span>
  
<span data-ttu-id="e3d5f-130">レコードおよび検索キーの 1 つの違いは、レコードのキー、オブジェクトに固有の他のオブジェクトに検索キーをコピーすることができますが、です。</span><span class="sxs-lookup"><span data-stu-id="e3d5f-130">One distinction between the record and search keys is that the record key is specific to the object, whereas the search key can be copied to other objects.</span></span> <span data-ttu-id="e3d5f-131">などのオブジェクトの 2 つのコピーは同じ**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) の値を持つことができますが、このプロパティに異なる値を持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="e3d5f-131">For example, two copies of the object can have the same **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) value but must have different values for this property.</span></span>
  
<span data-ttu-id="e3d5f-132">**PR_ENTRYID**、 **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))、このプロパティの間で重要な相違点を次の表にまとめます。</span><span class="sxs-lookup"><span data-stu-id="e3d5f-132">The following table summarizes important differences among **PR_ENTRYID**, **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) and this property.</span></span> 
  
|<span data-ttu-id="e3d5f-133">**特性**</span><span class="sxs-lookup"><span data-stu-id="e3d5f-133">**Characteristic**</span></span>|<span data-ttu-id="e3d5f-134">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="e3d5f-134">**PR_ENTRYID**</span></span>|<span data-ttu-id="e3d5f-135">**PR_RECORD_KEY**</span><span class="sxs-lookup"><span data-stu-id="e3d5f-135">**PR_RECORD_KEY**</span></span>|<span data-ttu-id="e3d5f-136">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="e3d5f-136">**PR_SEARCH_KEY**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e3d5f-137">添付ファイルのオブジェクトで必要な</span><span class="sxs-lookup"><span data-stu-id="e3d5f-137">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="e3d5f-138">いいえ</span><span class="sxs-lookup"><span data-stu-id="e3d5f-138">No</span></span>  <br/> |<span data-ttu-id="e3d5f-139">はい</span><span class="sxs-lookup"><span data-stu-id="e3d5f-139">Yes</span></span>  <br/> |<span data-ttu-id="e3d5f-140">いいえ</span><span class="sxs-lookup"><span data-stu-id="e3d5f-140">No</span></span>  <br/> |
|<span data-ttu-id="e3d5f-141">フォルダー オブジェクトで必要な</span><span class="sxs-lookup"><span data-stu-id="e3d5f-141">Required on folder objects</span></span>  <br/> |<span data-ttu-id="e3d5f-142">はい</span><span class="sxs-lookup"><span data-stu-id="e3d5f-142">Yes</span></span>  <br/> |<span data-ttu-id="e3d5f-143">はい</span><span class="sxs-lookup"><span data-stu-id="e3d5f-143">Yes</span></span>  <br/> |<span data-ttu-id="e3d5f-144">いいえ</span><span class="sxs-lookup"><span data-stu-id="e3d5f-144">No</span></span>  <br/> |
|<span data-ttu-id="e3d5f-145">メッセージ ストア オブジェクトで必要な</span><span class="sxs-lookup"><span data-stu-id="e3d5f-145">Required on message store objects</span></span>  <br/> |<span data-ttu-id="e3d5f-146">はい</span><span class="sxs-lookup"><span data-stu-id="e3d5f-146">Yes</span></span>  <br/> |<span data-ttu-id="e3d5f-147">はい</span><span class="sxs-lookup"><span data-stu-id="e3d5f-147">Yes</span></span>  <br/> |<span data-ttu-id="e3d5f-148">いいえ</span><span class="sxs-lookup"><span data-stu-id="e3d5f-148">No</span></span>  <br/> |
|<span data-ttu-id="e3d5f-149">状態オブジェクトで必要な</span><span class="sxs-lookup"><span data-stu-id="e3d5f-149">Required on status objects</span></span>  <br/> |<span data-ttu-id="e3d5f-150">はい</span><span class="sxs-lookup"><span data-stu-id="e3d5f-150">Yes</span></span>  <br/> |<span data-ttu-id="e3d5f-151">いいえ</span><span class="sxs-lookup"><span data-stu-id="e3d5f-151">No</span></span>  <br/> |<span data-ttu-id="e3d5f-152">いいえ</span><span class="sxs-lookup"><span data-stu-id="e3d5f-152">No</span></span>  <br/> |
|<span data-ttu-id="e3d5f-153">クライアントで作成可能</span><span class="sxs-lookup"><span data-stu-id="e3d5f-153">Creatable by client</span></span>  <br/> |<span data-ttu-id="e3d5f-154">いいえ</span><span class="sxs-lookup"><span data-stu-id="e3d5f-154">No</span></span>  <br/> |<span data-ttu-id="e3d5f-155">いいえ</span><span class="sxs-lookup"><span data-stu-id="e3d5f-155">No</span></span>  <br/> |<span data-ttu-id="e3d5f-156">はい</span><span class="sxs-lookup"><span data-stu-id="e3d5f-156">Yes</span></span>  <br/> |
|<span data-ttu-id="e3d5f-157">**Savechanges メソッド**の呼び出しの前に使用可能です</span><span class="sxs-lookup"><span data-stu-id="e3d5f-157">Available before a call to **SaveChanges**</span></span> <br/> |<span data-ttu-id="e3d5f-158">かもしれません</span><span class="sxs-lookup"><span data-stu-id="e3d5f-158">Maybe</span></span>  <br/> |<span data-ttu-id="e3d5f-159">かもしれません</span><span class="sxs-lookup"><span data-stu-id="e3d5f-159">Maybe</span></span>  <br/> |<span data-ttu-id="e3d5f-160">メッセージは他の人をたぶんはい</span><span class="sxs-lookup"><span data-stu-id="e3d5f-160">Messages Yes Others Maybe</span></span>  <br/> |
|<span data-ttu-id="e3d5f-161">コピー操作で変更</span><span class="sxs-lookup"><span data-stu-id="e3d5f-161">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="e3d5f-162">はい</span><span class="sxs-lookup"><span data-stu-id="e3d5f-162">Yes</span></span>  <br/> |<span data-ttu-id="e3d5f-163">はい</span><span class="sxs-lookup"><span data-stu-id="e3d5f-163">Yes</span></span>  <br/> |<span data-ttu-id="e3d5f-164">いいえ</span><span class="sxs-lookup"><span data-stu-id="e3d5f-164">No</span></span>  <br/> |
|<span data-ttu-id="e3d5f-165">コピー後にクライアントによって変更可能です</span><span class="sxs-lookup"><span data-stu-id="e3d5f-165">Changeable by a client after a copy</span></span>  <br/> |<span data-ttu-id="e3d5f-166">いいえ</span><span class="sxs-lookup"><span data-stu-id="e3d5f-166">No</span></span>  <br/> |<span data-ttu-id="e3d5f-167">いいえ</span><span class="sxs-lookup"><span data-stu-id="e3d5f-167">No</span></span>  <br/> |<span data-ttu-id="e3d5f-168">はい</span><span class="sxs-lookup"><span data-stu-id="e3d5f-168">Yes</span></span>  <br/> |
|<span data-ttu-id="e3d5f-169">内で重複しています.</span><span class="sxs-lookup"><span data-stu-id="e3d5f-169">Unique within ...</span></span>  <br/> |<span data-ttu-id="e3d5f-170">全体の世界</span><span class="sxs-lookup"><span data-stu-id="e3d5f-170">Entire world</span></span>  <br/> |<span data-ttu-id="e3d5f-171">プロバイダーのインスタンス</span><span class="sxs-lookup"><span data-stu-id="e3d5f-171">Provider instance</span></span>  <br/> |<span data-ttu-id="e3d5f-172">全体の世界</span><span class="sxs-lookup"><span data-stu-id="e3d5f-172">Entire world</span></span>  <br/> |
|<span data-ttu-id="e3d5f-173">バイナリ (ため) と同じように匹敵します。</span><span class="sxs-lookup"><span data-stu-id="e3d5f-173">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="e3d5f-174">いいえ--を使用して**IMAPISupport:: CompareEntryIDs**</span><span class="sxs-lookup"><span data-stu-id="e3d5f-174">No -- use **IMAPISupport:: CompareEntryIDs**</span></span> <br/> |<span data-ttu-id="e3d5f-175">はい</span><span class="sxs-lookup"><span data-stu-id="e3d5f-175">Yes</span></span>  <br/> |<span data-ttu-id="e3d5f-176">はい</span><span class="sxs-lookup"><span data-stu-id="e3d5f-176">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="e3d5f-177">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e3d5f-177">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e3d5f-178">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e3d5f-178">Protocol specifications</span></span>

<span data-ttu-id="e3d5f-179">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e3d5f-179">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e3d5f-180">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="e3d5f-180">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e3d5f-181">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e3d5f-181">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e3d5f-182">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="e3d5f-182">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="e3d5f-183">[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e3d5f-183">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e3d5f-184">プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e3d5f-184">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e3d5f-185">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e3d5f-185">Header files</span></span>

<span data-ttu-id="e3d5f-186">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e3d5f-186">Mapidefs.h</span></span>
  
> <span data-ttu-id="e3d5f-187">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e3d5f-187">Provides data type definitions.</span></span>
    
<span data-ttu-id="e3d5f-188">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e3d5f-188">Mapitags.h</span></span>
  
> <span data-ttu-id="e3d5f-189">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e3d5f-189">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e3d5f-190">関連項目</span><span class="sxs-lookup"><span data-stu-id="e3d5f-190">See also</span></span>



[<span data-ttu-id="e3d5f-191">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e3d5f-191">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e3d5f-192">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e3d5f-192">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e3d5f-193">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e3d5f-193">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e3d5f-194">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e3d5f-194">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

