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
ms.openlocfilehash: 7a3ae7db1fb97e97f7d0939b67f139af62477bf7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355266"
---
# <a name="pidtagrecordkey-canonical-property"></a><span data-ttu-id="7f864-103">PidTagRecordKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7f864-103">PidTagRecordKey Canonical Property</span></span>

  
  
<span data-ttu-id="7f864-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f864-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f864-105">特定のオブジェクトの一意のバイナリ比較識別子を含みます。</span><span class="sxs-lookup"><span data-stu-id="7f864-105">Contains a unique binary-comparable identifier for a specific object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7f864-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="7f864-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7f864-107">PR_RECORD_KEY</span><span class="sxs-lookup"><span data-stu-id="7f864-107">PR_RECORD_KEY</span></span>  <br/> |
|<span data-ttu-id="7f864-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="7f864-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7f864-109">0x0ff9</span><span class="sxs-lookup"><span data-stu-id="7f864-109">0x0FF9</span></span>  <br/> |
|<span data-ttu-id="7f864-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="7f864-110">Data type:</span></span>  <br/> |<span data-ttu-id="7f864-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="7f864-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="7f864-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="7f864-112">Area:</span></span>  <br/> |<span data-ttu-id="7f864-113">ID プロパティ</span><span class="sxs-lookup"><span data-stu-id="7f864-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7f864-114">解説</span><span class="sxs-lookup"><span data-stu-id="7f864-114">Remarks</span></span>

<span data-ttu-id="7f864-115">このプロパティを設定すると、コンテンツテーブル内の行を検索するなど、オブジェクトへの参照を簡単に見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="7f864-115">This property facilitates locating references to an object, such as finding its row in a contents table.</span></span> <span data-ttu-id="7f864-116">このプロパティを使用してオブジェクトを開くことはできません。その目的のためにエントリ識別子を使用します。</span><span class="sxs-lookup"><span data-stu-id="7f864-116">This property cannot be used to open an object; use the entry identifier for that purpose.</span></span>
  
<span data-ttu-id="7f864-117">添付ファイルサブオブジェクトは、このプロパティでメッセージ内で一意に識別する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f864-117">An attachment subobject should be uniquely identified within a message by this property.</span></span> <span data-ttu-id="7f864-118">この識別子は、メッセージを閉じてからもう一度開いた後に維持することが保証されている唯一の添付ファイルの特性です。</span><span class="sxs-lookup"><span data-stu-id="7f864-118">This identifier is the only attachment characteristic guaranteed to stay the same after the message is closed and reopened.</span></span> <span data-ttu-id="7f864-119">ストアプロバイダーは、この保証を確実にするために、セッション間でこのプロパティを保持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f864-119">The store provider must preserve this property across sessions to ensure this guarantee.</span></span>
  
<span data-ttu-id="7f864-120">フォルダーの場合、このプロパティには、フォルダー階層テーブルで使用されるキーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="7f864-120">For folders, this property contains a key used in the folder hierarchy table.</span></span> <span data-ttu-id="7f864-121">通常、これは**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティで提供される値と同じです。</span><span class="sxs-lookup"><span data-stu-id="7f864-121">Typically this is the same value as that provided by the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="7f864-122">メッセージストアの場合、このプロパティは**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)) プロパティと同じです。</span><span class="sxs-lookup"><span data-stu-id="7f864-122">For message stores, this property is identical to the **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="7f864-123">メッセージストアオブジェクトでは、このプロパティはすべてのストアプロバイダーで一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f864-123">In a message store object, this property should be unique across all store providers.</span></span> <span data-ttu-id="7f864-124">そのための方法の1つとして、ストアの**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) プロパティの値を、 [GUID](guid.md)構造または特定のメッセージストアに固有の他の値と組み合わせて使用することができます。</span><span class="sxs-lookup"><span data-stu-id="7f864-124">One way to do this is to combine the value of the **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) property for the store (unique to that provider type) with a [GUID](guid.md) structure or other value unique to the specific message store.</span></span> 
  
<span data-ttu-id="7f864-125">このプロパティは、imapiprop [:: SaveChanges](imapiprop-savechanges.md)メソッドを最初に呼び出した後、 [imapiprop:: GetProps](imapiprop-getprops.md)メソッドを使用して常に使用できます。</span><span class="sxs-lookup"><span data-stu-id="7f864-125">This property is always available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="7f864-126">プロバイダーによっては、インスタンス化の直後に使用できるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="7f864-126">Some providers can make it available immediately after instantiation.</span></span> 
  
<span data-ttu-id="7f864-127">クライアントまたはサービスプロバイダーは、memcmp を使用してこのプロパティの値を比較できます。</span><span class="sxs-lookup"><span data-stu-id="7f864-127">A client or service provider can compare values from this property by using memcmp.</span></span> <span data-ttu-id="7f864-128">これはエントリ識別子の値には使用できません。</span><span class="sxs-lookup"><span data-stu-id="7f864-128">This is not possible for entry identifier values.</span></span> <span data-ttu-id="7f864-129">ただし、このプロパティは同じメッセージストアまたはアドレス帳コンテナー内で一意であることが保証されています。異なるコンテナーからの2つのオブジェクトは、このプロパティの値を持つことができます。</span><span class="sxs-lookup"><span data-stu-id="7f864-129">However, this property is guaranteed to be unique within the same message store or address book container; two objects from different containers can have the same value of this property.</span></span>
  
<span data-ttu-id="7f864-130">record キーと検索キーの違いの1つは、record キーがオブジェクトに固有であるのに対して、検索キーは他のオブジェクトにコピーできるということです。</span><span class="sxs-lookup"><span data-stu-id="7f864-130">One distinction between the record and search keys is that the record key is specific to the object, whereas the search key can be copied to other objects.</span></span> <span data-ttu-id="7f864-131">たとえば、オブジェクトの2つのコピーは同じ**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) 値を持つことができますが、このプロパティには異なる値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f864-131">For example, two copies of the object can have the same **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) value but must have different values for this property.</span></span>
  
<span data-ttu-id="7f864-132">次の表は、 **PR_ENTRYID**、 **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) およびこのプロパティの重要な相違点をまとめたものです。</span><span class="sxs-lookup"><span data-stu-id="7f864-132">The following table summarizes important differences among **PR_ENTRYID**, **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) and this property.</span></span> 
  
|<span data-ttu-id="7f864-133">**特性**</span><span class="sxs-lookup"><span data-stu-id="7f864-133">**Characteristic**</span></span>|<span data-ttu-id="7f864-134">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="7f864-134">**PR_ENTRYID**</span></span>|<span data-ttu-id="7f864-135">**PR_RECORD_KEY**</span><span class="sxs-lookup"><span data-stu-id="7f864-135">**PR_RECORD_KEY**</span></span>|<span data-ttu-id="7f864-136">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="7f864-136">**PR_SEARCH_KEY**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7f864-137">attachment オブジェクトに必要</span><span class="sxs-lookup"><span data-stu-id="7f864-137">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="7f864-138">いいえ</span><span class="sxs-lookup"><span data-stu-id="7f864-138">No</span></span>  <br/> |<span data-ttu-id="7f864-139">はい</span><span class="sxs-lookup"><span data-stu-id="7f864-139">Yes</span></span>  <br/> |<span data-ttu-id="7f864-140">いいえ</span><span class="sxs-lookup"><span data-stu-id="7f864-140">No</span></span>  <br/> |
|<span data-ttu-id="7f864-141">folder オブジェクトで必要</span><span class="sxs-lookup"><span data-stu-id="7f864-141">Required on folder objects</span></span>  <br/> |<span data-ttu-id="7f864-142">はい</span><span class="sxs-lookup"><span data-stu-id="7f864-142">Yes</span></span>  <br/> |<span data-ttu-id="7f864-143">はい</span><span class="sxs-lookup"><span data-stu-id="7f864-143">Yes</span></span>  <br/> |<span data-ttu-id="7f864-144">いいえ</span><span class="sxs-lookup"><span data-stu-id="7f864-144">No</span></span>  <br/> |
|<span data-ttu-id="7f864-145">メッセージストアオブジェクトに必要</span><span class="sxs-lookup"><span data-stu-id="7f864-145">Required on message store objects</span></span>  <br/> |<span data-ttu-id="7f864-146">はい</span><span class="sxs-lookup"><span data-stu-id="7f864-146">Yes</span></span>  <br/> |<span data-ttu-id="7f864-147">はい</span><span class="sxs-lookup"><span data-stu-id="7f864-147">Yes</span></span>  <br/> |<span data-ttu-id="7f864-148">いいえ</span><span class="sxs-lookup"><span data-stu-id="7f864-148">No</span></span>  <br/> |
|<span data-ttu-id="7f864-149">状態オブジェクトに必要です</span><span class="sxs-lookup"><span data-stu-id="7f864-149">Required on status objects</span></span>  <br/> |<span data-ttu-id="7f864-150">はい</span><span class="sxs-lookup"><span data-stu-id="7f864-150">Yes</span></span>  <br/> |<span data-ttu-id="7f864-151">いいえ</span><span class="sxs-lookup"><span data-stu-id="7f864-151">No</span></span>  <br/> |<span data-ttu-id="7f864-152">いいえ</span><span class="sxs-lookup"><span data-stu-id="7f864-152">No</span></span>  <br/> |
|<span data-ttu-id="7f864-153">クライアントによるのが可能</span><span class="sxs-lookup"><span data-stu-id="7f864-153">Creatable by client</span></span>  <br/> |<span data-ttu-id="7f864-154">いいえ</span><span class="sxs-lookup"><span data-stu-id="7f864-154">No</span></span>  <br/> |<span data-ttu-id="7f864-155">いいえ</span><span class="sxs-lookup"><span data-stu-id="7f864-155">No</span></span>  <br/> |<span data-ttu-id="7f864-156">はい</span><span class="sxs-lookup"><span data-stu-id="7f864-156">Yes</span></span>  <br/> |
|<span data-ttu-id="7f864-157">**SaveChanges**を呼び出す前に使用できます。</span><span class="sxs-lookup"><span data-stu-id="7f864-157">Available before a call to **SaveChanges**</span></span> <br/> |<span data-ttu-id="7f864-158">考え</span><span class="sxs-lookup"><span data-stu-id="7f864-158">Maybe</span></span>  <br/> |<span data-ttu-id="7f864-159">考え</span><span class="sxs-lookup"><span data-stu-id="7f864-159">Maybe</span></span>  <br/> |<span data-ttu-id="7f864-160">[その他のメッセージ]</span><span class="sxs-lookup"><span data-stu-id="7f864-160">Messages Yes Others Maybe</span></span>  <br/> |
|<span data-ttu-id="7f864-161">コピー操作で変更</span><span class="sxs-lookup"><span data-stu-id="7f864-161">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="7f864-162">はい</span><span class="sxs-lookup"><span data-stu-id="7f864-162">Yes</span></span>  <br/> |<span data-ttu-id="7f864-163">はい</span><span class="sxs-lookup"><span data-stu-id="7f864-163">Yes</span></span>  <br/> |<span data-ttu-id="7f864-164">いいえ</span><span class="sxs-lookup"><span data-stu-id="7f864-164">No</span></span>  <br/> |
|<span data-ttu-id="7f864-165">コピー後にクライアントによって変更される</span><span class="sxs-lookup"><span data-stu-id="7f864-165">Changeable by a client after a copy</span></span>  <br/> |<span data-ttu-id="7f864-166">いいえ</span><span class="sxs-lookup"><span data-stu-id="7f864-166">No</span></span>  <br/> |<span data-ttu-id="7f864-167">いいえ</span><span class="sxs-lookup"><span data-stu-id="7f864-167">No</span></span>  <br/> |<span data-ttu-id="7f864-168">はい</span><span class="sxs-lookup"><span data-stu-id="7f864-168">Yes</span></span>  <br/> |
|<span data-ttu-id="7f864-169">一意の範囲</span><span class="sxs-lookup"><span data-stu-id="7f864-169">Unique within ...</span></span>  <br/> |<span data-ttu-id="7f864-170">世界全体</span><span class="sxs-lookup"><span data-stu-id="7f864-170">Entire world</span></span>  <br/> |<span data-ttu-id="7f864-171">プロバイダーインスタンス</span><span class="sxs-lookup"><span data-stu-id="7f864-171">Provider instance</span></span>  <br/> |<span data-ttu-id="7f864-172">世界全体</span><span class="sxs-lookup"><span data-stu-id="7f864-172">Entire world</span></span>  <br/> |
|<span data-ttu-id="7f864-173">二項比較 (memcmp と同じ)</span><span class="sxs-lookup"><span data-stu-id="7f864-173">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="7f864-174">No-- **imapisupport:: compareentryids**を使用します。</span><span class="sxs-lookup"><span data-stu-id="7f864-174">No -- use **IMAPISupport:: CompareEntryIDs**</span></span> <br/> |<span data-ttu-id="7f864-175">はい</span><span class="sxs-lookup"><span data-stu-id="7f864-175">Yes</span></span>  <br/> |<span data-ttu-id="7f864-176">はい</span><span class="sxs-lookup"><span data-stu-id="7f864-176">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="7f864-177">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7f864-177">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7f864-178">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="7f864-178">Protocol specifications</span></span>

<span data-ttu-id="7f864-179">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7f864-179">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7f864-180">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="7f864-180">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7f864-181">[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7f864-181">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7f864-182">メッセージと添付ファイルオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="7f864-182">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="7f864-183">[[OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7f864-183">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7f864-184">ユーザー、連絡先、グループ、およびリソースのリストのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="7f864-184">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7f864-185">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="7f864-185">Header files</span></span>

<span data-ttu-id="7f864-186">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7f864-186">Mapidefs.h</span></span>
  
> <span data-ttu-id="7f864-187">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7f864-187">Provides data type definitions.</span></span>
    
<span data-ttu-id="7f864-188">Mapitags</span><span class="sxs-lookup"><span data-stu-id="7f864-188">Mapitags.h</span></span>
  
> <span data-ttu-id="7f864-189">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7f864-189">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7f864-190">関連項目</span><span class="sxs-lookup"><span data-stu-id="7f864-190">See also</span></span>



[<span data-ttu-id="7f864-191">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="7f864-191">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7f864-192">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7f864-192">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7f864-193">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7f864-193">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7f864-194">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7f864-194">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

