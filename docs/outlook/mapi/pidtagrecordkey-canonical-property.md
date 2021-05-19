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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7a3ae7db1fb97e97f7d0939b67f139af62477bf7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355266"
---
# <a name="pidtagrecordkey-canonical-property"></a><span data-ttu-id="df521-103">PidTagRecordKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="df521-103">PidTagRecordKey Canonical Property</span></span>

  
  
<span data-ttu-id="df521-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df521-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df521-105">特定のオブジェクトの一意のバイナリと同等の識別子を含む。</span><span class="sxs-lookup"><span data-stu-id="df521-105">Contains a unique binary-comparable identifier for a specific object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="df521-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="df521-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="df521-107">PR_RECORD_KEY</span><span class="sxs-lookup"><span data-stu-id="df521-107">PR_RECORD_KEY</span></span>  <br/> |
|<span data-ttu-id="df521-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="df521-108">Identifier:</span></span>  <br/> |<span data-ttu-id="df521-109">0x0FF9</span><span class="sxs-lookup"><span data-stu-id="df521-109">0x0FF9</span></span>  <br/> |
|<span data-ttu-id="df521-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="df521-110">Data type:</span></span>  <br/> |<span data-ttu-id="df521-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="df521-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="df521-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="df521-112">Area:</span></span>  <br/> |<span data-ttu-id="df521-113">ID プロパティ</span><span class="sxs-lookup"><span data-stu-id="df521-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="df521-114">注釈</span><span class="sxs-lookup"><span data-stu-id="df521-114">Remarks</span></span>

<span data-ttu-id="df521-115">このプロパティを使用すると、コンテンツ テーブル内の行の検索など、オブジェクトへの参照を簡単に検索できます。</span><span class="sxs-lookup"><span data-stu-id="df521-115">This property facilitates locating references to an object, such as finding its row in a contents table.</span></span> <span data-ttu-id="df521-116">このプロパティは、オブジェクトを開くのに使用できません。その目的のためにエントリ識別子を使用します。</span><span class="sxs-lookup"><span data-stu-id="df521-116">This property cannot be used to open an object; use the entry identifier for that purpose.</span></span>
  
<span data-ttu-id="df521-117">添付ファイルサブオブジェクトは、このプロパティによってメッセージ内で一意に識別する必要があります。</span><span class="sxs-lookup"><span data-stu-id="df521-117">An attachment subobject should be uniquely identified within a message by this property.</span></span> <span data-ttu-id="df521-118">この識別子は、メッセージを閉じて再び開いた後も同じ状態を続け続け保証される唯一の添付ファイルの特性です。</span><span class="sxs-lookup"><span data-stu-id="df521-118">This identifier is the only attachment characteristic guaranteed to stay the same after the message is closed and reopened.</span></span> <span data-ttu-id="df521-119">ストア プロバイダーは、この保証を保証するために、セッション間でこのプロパティを保持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="df521-119">The store provider must preserve this property across sessions to ensure this guarantee.</span></span>
  
<span data-ttu-id="df521-120">フォルダーの場合、このプロパティには、フォルダー階層テーブルで使用されるキーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="df521-120">For folders, this property contains a key used in the folder hierarchy table.</span></span> <span data-ttu-id="df521-121">通常、これはプロパティ ([PidTagEntryId](pidtagentryid-canonical-property.md) **)** プロパティPR_ENTRYID同じ値です。</span><span class="sxs-lookup"><span data-stu-id="df521-121">Typically this is the same value as that provided by the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="df521-122">メッセージ ストアの場合、このプロパティは PR_STORE_RECORD_KEY **(** [PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)) プロパティと同じです。</span><span class="sxs-lookup"><span data-stu-id="df521-122">For message stores, this property is identical to the **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="df521-123">メッセージ ストア オブジェクトでは、このプロパティは、すべてのストア プロバイダーで一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="df521-123">In a message store object, this property should be unique across all store providers.</span></span> <span data-ttu-id="df521-124">これを行う方法の 1 つは、 **ストアの PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) プロパティの値 (プロバイダーの種類に固有) と [、GUID](guid.md) 構造または特定のメッセージ ストア固有の他の値を組み合わせることです。</span><span class="sxs-lookup"><span data-stu-id="df521-124">One way to do this is to combine the value of the **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) property for the store (unique to that provider type) with a [GUID](guid.md) structure or other value unique to the specific message store.</span></span> 
  
<span data-ttu-id="df521-125">このプロパティは [、IMAPIProp::SaveChanges](imapiprop-getprops.md) メソッドの最初の呼び出しに続く [IMAPIProp::GetProps](imapiprop-savechanges.md) メソッドを通じて常に使用できます。</span><span class="sxs-lookup"><span data-stu-id="df521-125">This property is always available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="df521-126">一部のプロバイダーでは、インスタンス化の直後に使用できます。</span><span class="sxs-lookup"><span data-stu-id="df521-126">Some providers can make it available immediately after instantiation.</span></span> 
  
<span data-ttu-id="df521-127">クライアントまたはサービス プロバイダーは、memcmp を使用して、このプロパティの値を比較できます。</span><span class="sxs-lookup"><span data-stu-id="df521-127">A client or service provider can compare values from this property by using memcmp.</span></span> <span data-ttu-id="df521-128">これは、エントリ識別子の値では使用できない。</span><span class="sxs-lookup"><span data-stu-id="df521-128">This is not possible for entry identifier values.</span></span> <span data-ttu-id="df521-129">ただし、このプロパティは、同じメッセージ ストアまたはアドレス帳コンテナー内で一意である必要があります。異なるコンテナーの 2 つのオブジェクトは、このプロパティの同じ値を持つ場合があります。</span><span class="sxs-lookup"><span data-stu-id="df521-129">However, this property is guaranteed to be unique within the same message store or address book container; two objects from different containers can have the same value of this property.</span></span>
  
<span data-ttu-id="df521-130">レコード キーと検索キーの違いは、レコード キーがオブジェクトに固有であるのに対し、検索キーを他のオブジェクトにコピーできるという違いがあります。</span><span class="sxs-lookup"><span data-stu-id="df521-130">One distinction between the record and search keys is that the record key is specific to the object, whereas the search key can be copied to other objects.</span></span> <span data-ttu-id="df521-131">たとえば、オブジェクトの 2 つのコピーに同じ値[(PidTagSearchKey)](pidtagsearchkey-canonical-property.md)PR_SEARCH_KEYを指定できますが、このプロパティには異なる値が必要です。</span><span class="sxs-lookup"><span data-stu-id="df521-131">For example, two copies of the object can have the same **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) value but must have different values for this property.</span></span>
  
<span data-ttu-id="df521-132">次の表は、このプロパティ 、PR_ENTRYID **、** PR_SEARCH_KEY ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))**の間の** 重要な違いを示しています。</span><span class="sxs-lookup"><span data-stu-id="df521-132">The following table summarizes important differences among **PR_ENTRYID**, **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) and this property.</span></span> 
  
|<span data-ttu-id="df521-133">**特性**</span><span class="sxs-lookup"><span data-stu-id="df521-133">**Characteristic**</span></span>|<span data-ttu-id="df521-134">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="df521-134">**PR_ENTRYID**</span></span>|<span data-ttu-id="df521-135">**PR_RECORD_KEY**</span><span class="sxs-lookup"><span data-stu-id="df521-135">**PR_RECORD_KEY**</span></span>|<span data-ttu-id="df521-136">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="df521-136">**PR_SEARCH_KEY**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="df521-137">添付ファイル オブジェクトに必須</span><span class="sxs-lookup"><span data-stu-id="df521-137">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="df521-138">いいえ</span><span class="sxs-lookup"><span data-stu-id="df521-138">No</span></span>  <br/> |<span data-ttu-id="df521-139">はい</span><span class="sxs-lookup"><span data-stu-id="df521-139">Yes</span></span>  <br/> |<span data-ttu-id="df521-140">いいえ</span><span class="sxs-lookup"><span data-stu-id="df521-140">No</span></span>  <br/> |
|<span data-ttu-id="df521-141">フォルダー オブジェクトに必須</span><span class="sxs-lookup"><span data-stu-id="df521-141">Required on folder objects</span></span>  <br/> |<span data-ttu-id="df521-142">はい</span><span class="sxs-lookup"><span data-stu-id="df521-142">Yes</span></span>  <br/> |<span data-ttu-id="df521-143">はい</span><span class="sxs-lookup"><span data-stu-id="df521-143">Yes</span></span>  <br/> |<span data-ttu-id="df521-144">いいえ</span><span class="sxs-lookup"><span data-stu-id="df521-144">No</span></span>  <br/> |
|<span data-ttu-id="df521-145">メッセージ ストア オブジェクトで必須</span><span class="sxs-lookup"><span data-stu-id="df521-145">Required on message store objects</span></span>  <br/> |<span data-ttu-id="df521-146">はい</span><span class="sxs-lookup"><span data-stu-id="df521-146">Yes</span></span>  <br/> |<span data-ttu-id="df521-147">はい</span><span class="sxs-lookup"><span data-stu-id="df521-147">Yes</span></span>  <br/> |<span data-ttu-id="df521-148">いいえ</span><span class="sxs-lookup"><span data-stu-id="df521-148">No</span></span>  <br/> |
|<span data-ttu-id="df521-149">状態オブジェクトで必須</span><span class="sxs-lookup"><span data-stu-id="df521-149">Required on status objects</span></span>  <br/> |<span data-ttu-id="df521-150">はい</span><span class="sxs-lookup"><span data-stu-id="df521-150">Yes</span></span>  <br/> |<span data-ttu-id="df521-151">いいえ</span><span class="sxs-lookup"><span data-stu-id="df521-151">No</span></span>  <br/> |<span data-ttu-id="df521-152">いいえ</span><span class="sxs-lookup"><span data-stu-id="df521-152">No</span></span>  <br/> |
|<span data-ttu-id="df521-153">クライアントによる折りたたみ可能</span><span class="sxs-lookup"><span data-stu-id="df521-153">Creatable by client</span></span>  <br/> |<span data-ttu-id="df521-154">いいえ</span><span class="sxs-lookup"><span data-stu-id="df521-154">No</span></span>  <br/> |<span data-ttu-id="df521-155">いいえ</span><span class="sxs-lookup"><span data-stu-id="df521-155">No</span></span>  <br/> |<span data-ttu-id="df521-156">はい</span><span class="sxs-lookup"><span data-stu-id="df521-156">Yes</span></span>  <br/> |
|<span data-ttu-id="df521-157">SaveChanges への呼び出し **の前に使用可能**</span><span class="sxs-lookup"><span data-stu-id="df521-157">Available before a call to **SaveChanges**</span></span> <br/> |<span data-ttu-id="df521-158">多分</span><span class="sxs-lookup"><span data-stu-id="df521-158">Maybe</span></span>  <br/> |<span data-ttu-id="df521-159">多分</span><span class="sxs-lookup"><span data-stu-id="df521-159">Maybe</span></span>  <br/> |<span data-ttu-id="df521-160">メッセージ はい その他 多分</span><span class="sxs-lookup"><span data-stu-id="df521-160">Messages Yes Others Maybe</span></span>  <br/> |
|<span data-ttu-id="df521-161">コピー操作で変更された</span><span class="sxs-lookup"><span data-stu-id="df521-161">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="df521-162">はい</span><span class="sxs-lookup"><span data-stu-id="df521-162">Yes</span></span>  <br/> |<span data-ttu-id="df521-163">はい</span><span class="sxs-lookup"><span data-stu-id="df521-163">Yes</span></span>  <br/> |<span data-ttu-id="df521-164">いいえ</span><span class="sxs-lookup"><span data-stu-id="df521-164">No</span></span>  <br/> |
|<span data-ttu-id="df521-165">コピー後にクライアントが変更可能</span><span class="sxs-lookup"><span data-stu-id="df521-165">Changeable by a client after a copy</span></span>  <br/> |<span data-ttu-id="df521-166">いいえ</span><span class="sxs-lookup"><span data-stu-id="df521-166">No</span></span>  <br/> |<span data-ttu-id="df521-167">いいえ</span><span class="sxs-lookup"><span data-stu-id="df521-167">No</span></span>  <br/> |<span data-ttu-id="df521-168">はい</span><span class="sxs-lookup"><span data-stu-id="df521-168">Yes</span></span>  <br/> |
|<span data-ttu-id="df521-169">..内で一意です。</span><span class="sxs-lookup"><span data-stu-id="df521-169">Unique within ...</span></span>  <br/> |<span data-ttu-id="df521-170">ワールド全体</span><span class="sxs-lookup"><span data-stu-id="df521-170">Entire world</span></span>  <br/> |<span data-ttu-id="df521-171">プロバイダー インスタンス</span><span class="sxs-lookup"><span data-stu-id="df521-171">Provider instance</span></span>  <br/> |<span data-ttu-id="df521-172">ワールド全体</span><span class="sxs-lookup"><span data-stu-id="df521-172">Entire world</span></span>  <br/> |
|<span data-ttu-id="df521-173">バイナリ比較 (memcmp と同様)</span><span class="sxs-lookup"><span data-stu-id="df521-173">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="df521-174">いいえ -- **IMAPISupport:: CompareEntryIDs を使用する**</span><span class="sxs-lookup"><span data-stu-id="df521-174">No -- use **IMAPISupport:: CompareEntryIDs**</span></span> <br/> |<span data-ttu-id="df521-175">はい</span><span class="sxs-lookup"><span data-stu-id="df521-175">Yes</span></span>  <br/> |<span data-ttu-id="df521-176">はい</span><span class="sxs-lookup"><span data-stu-id="df521-176">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="df521-177">関連リソース</span><span class="sxs-lookup"><span data-stu-id="df521-177">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="df521-178">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="df521-178">Protocol specifications</span></span>

<span data-ttu-id="df521-179">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="df521-179">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="df521-180">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="df521-180">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="df521-181">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="df521-181">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="df521-182">メッセージ オブジェクトと添付ファイル オブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="df521-182">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="df521-183">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="df521-183">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="df521-184">ユーザー、連絡先、グループ、およびリソースの一覧のプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="df521-184">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="df521-185">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="df521-185">Header files</span></span>

<span data-ttu-id="df521-186">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="df521-186">Mapidefs.h</span></span>
  
> <span data-ttu-id="df521-187">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="df521-187">Provides data type definitions.</span></span>
    
<span data-ttu-id="df521-188">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="df521-188">Mapitags.h</span></span>
  
> <span data-ttu-id="df521-189">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="df521-189">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="df521-190">関連項目</span><span class="sxs-lookup"><span data-stu-id="df521-190">See also</span></span>



[<span data-ttu-id="df521-191">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="df521-191">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="df521-192">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="df521-192">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="df521-193">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="df521-193">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="df521-194">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="df521-194">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

