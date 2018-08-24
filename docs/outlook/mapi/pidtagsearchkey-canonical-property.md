---
title: PidTagSearchKey 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: fcab369a-a1f4-4425-a272-e35046914a4d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: da7d19407856570a628529877252360d1537bae7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595392"
---
# <a name="pidtagsearchkey-canonical-property"></a><span data-ttu-id="cdeb1-103">PidTagSearchKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="cdeb1-103">PidTagSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="cdeb1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cdeb1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cdeb1-105">検索の相関関係を持つオブジェクトを識別するバイナリの比較可能なキーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="cdeb1-105">Contains a binary-comparable key that identifies correlated objects for a search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cdeb1-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="cdeb1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cdeb1-107">PR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="cdeb1-107">PR_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="cdeb1-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="cdeb1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cdeb1-109">0x300B</span><span class="sxs-lookup"><span data-stu-id="cdeb1-109">0x300B</span></span>  <br/> |
|<span data-ttu-id="cdeb1-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="cdeb1-110">Data type:</span></span>  <br/> |<span data-ttu-id="cdeb1-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="cdeb1-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="cdeb1-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="cdeb1-112">Area:</span></span>  <br/> |<span data-ttu-id="cdeb1-113">ID プロパティ</span><span class="sxs-lookup"><span data-stu-id="cdeb1-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cdeb1-114">注釈</span><span class="sxs-lookup"><span data-stu-id="cdeb1-114">Remarks</span></span>

<span data-ttu-id="cdeb1-115">このプロパティは、メッセージのコピーなどの関連オブジェクトのトレースを提供し、重複した受信者などの不要なアイテムの検索が容易になります。</span><span class="sxs-lookup"><span data-stu-id="cdeb1-115">This property provides a trace for related objects, such as message copies, and facilitates finding unwanted occurrences, such as duplicate recipients.</span></span>
  
<span data-ttu-id="cdeb1-116">MAPI は、メッセージの受信者の検索キーを構築するための特定の規則を使用します。</span><span class="sxs-lookup"><span data-stu-id="cdeb1-116">MAPI uses specific rules for constructing search keys for message recipients.</span></span> <span data-ttu-id="cdeb1-117">検索キーが (大文字で)、アドレスの種類を連結することによって形成されるコロン ':'、電子メール アドレスを標準の形式、および終端の null 文字です。</span><span class="sxs-lookup"><span data-stu-id="cdeb1-117">The search key is formed by concatenating the address type (in uppercase characters), the colon character ':', the email address in canonical form, and the terminating null character.</span></span> <span data-ttu-id="cdeb1-118">正規の形式は、ここでは、大文字・小文字の区別のアドレスが表示され、大文字小文字が区別されていないアドレスは、大文字に変換することを意味します。</span><span class="sxs-lookup"><span data-stu-id="cdeb1-118">Canonical form here means that case-sensitive addresses appear in the correct case, and addresses that are not case-sensitive are converted to uppercase.</span></span> <span data-ttu-id="cdeb1-119">これは、メッセージの相関関係の維持に重要です。</span><span class="sxs-lookup"><span data-stu-id="cdeb1-119">This is important in preserving correlations among messages.</span></span>
  
<span data-ttu-id="cdeb1-120">メッセージのオブジェクトのこのプロパティは、すぐに次のメッセージの作成、 [IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="cdeb1-120">For message objects, this property is available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method immediately following message creation.</span></span> <span data-ttu-id="cdeb1-121">その他のオブジェクトでは、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドへの最初の呼び出しの後に利用可能です。</span><span class="sxs-lookup"><span data-stu-id="cdeb1-121">For other objects, it is available following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="cdeb1-122">このプロパティは変更可能なので、信頼性の高い**SaveChanges**の呼び出しがすべての値を設定または[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドによって変更をコミットするまでの**GetProps**を通じて入手することはできません。</span><span class="sxs-lookup"><span data-stu-id="cdeb1-122">Because this property is changeable, it is unreliable to obtain it through **GetProps** until a **SaveChanges** call has committed any values set or changed by the [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> 
  
<span data-ttu-id="cdeb1-123">プロファイルの場合、MAPI は、ハード コーディングされたプロファイル セクション**MUID_PROFILE_INSTANCE**、1 つのプロパティとしては、このプロパティを使用しても提供します。</span><span class="sxs-lookup"><span data-stu-id="cdeb1-123">For profiles, MAPI also furnishes a hard-coded profile section named **MUID_PROFILE_INSTANCE**, with this property as its single property.</span></span> <span data-ttu-id="cdeb1-124">このキーが作成されると、すべてのプロファイル間で一意であることが保証され、 **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) は、ことができます、たとえば、削除され、同じ名前で再作成するよりも信頼性の高いことができます。</span><span class="sxs-lookup"><span data-stu-id="cdeb1-124">This key is guaranteed to be unique among all profiles ever created, and can be more reliable than the **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) property, which can be, for example, deleted and recreated with the same name.</span></span>
  
<span data-ttu-id="cdeb1-125">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))、 **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))、このプロパティの間の重要な相違点を次の表にまとめます。</span><span class="sxs-lookup"><span data-stu-id="cdeb1-125">The following table summarizes important differences among the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), and this property.</span></span>
  
|<span data-ttu-id="cdeb1-126">**特性**</span><span class="sxs-lookup"><span data-stu-id="cdeb1-126">**Characteristic**</span></span>|<span data-ttu-id="cdeb1-127">PR_ENTRYID。</span><span class="sxs-lookup"><span data-stu-id="cdeb1-127">****PR_ENTRYID****</span></span>|<span data-ttu-id="cdeb1-128">PR_RECORD_KEY。</span><span class="sxs-lookup"><span data-stu-id="cdeb1-128">****PR_RECORD_KEY****</span></span>|<span data-ttu-id="cdeb1-129">PR_SEARCH_KEY。</span><span class="sxs-lookup"><span data-stu-id="cdeb1-129">****PR_SEARCH_KEY****</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cdeb1-130">添付ファイルのオブジェクトで必要な</span><span class="sxs-lookup"><span data-stu-id="cdeb1-130">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="cdeb1-131">いいえ</span><span class="sxs-lookup"><span data-stu-id="cdeb1-131">No</span></span>  <br/> |<span data-ttu-id="cdeb1-132">はい</span><span class="sxs-lookup"><span data-stu-id="cdeb1-132">Yes</span></span>  <br/> |<span data-ttu-id="cdeb1-133">いいえ</span><span class="sxs-lookup"><span data-stu-id="cdeb1-133">No</span></span>  <br/> |
|<span data-ttu-id="cdeb1-134">フォルダー オブジェクトで必要な</span><span class="sxs-lookup"><span data-stu-id="cdeb1-134">Required on folder objects</span></span>  <br/> |<span data-ttu-id="cdeb1-135">はい</span><span class="sxs-lookup"><span data-stu-id="cdeb1-135">Yes</span></span>  <br/> |<span data-ttu-id="cdeb1-136">はい</span><span class="sxs-lookup"><span data-stu-id="cdeb1-136">Yes</span></span>  <br/> |<span data-ttu-id="cdeb1-137">いいえ</span><span class="sxs-lookup"><span data-stu-id="cdeb1-137">No</span></span>  <br/> |
|<span data-ttu-id="cdeb1-138">メッセージ ストア オブジェクトで必要な</span><span class="sxs-lookup"><span data-stu-id="cdeb1-138">Required on message store objects</span></span>  <br/> |<span data-ttu-id="cdeb1-139">はい</span><span class="sxs-lookup"><span data-stu-id="cdeb1-139">Yes</span></span>  <br/> |<span data-ttu-id="cdeb1-140">はい</span><span class="sxs-lookup"><span data-stu-id="cdeb1-140">Yes</span></span>  <br/> |<span data-ttu-id="cdeb1-141">いいえ</span><span class="sxs-lookup"><span data-stu-id="cdeb1-141">No</span></span>  <br/> |
|<span data-ttu-id="cdeb1-142">状態オブジェクトで必要な</span><span class="sxs-lookup"><span data-stu-id="cdeb1-142">Required on status objects</span></span>  <br/> |<span data-ttu-id="cdeb1-143">はい</span><span class="sxs-lookup"><span data-stu-id="cdeb1-143">Yes</span></span>  <br/> |<span data-ttu-id="cdeb1-144">いいえ</span><span class="sxs-lookup"><span data-stu-id="cdeb1-144">No</span></span>  <br/> |<span data-ttu-id="cdeb1-145">いいえ</span><span class="sxs-lookup"><span data-stu-id="cdeb1-145">No</span></span>  <br/> |
|<span data-ttu-id="cdeb1-146">クライアントで作成可能</span><span class="sxs-lookup"><span data-stu-id="cdeb1-146">Creatable by client</span></span>  <br/> |<span data-ttu-id="cdeb1-147">いいえ</span><span class="sxs-lookup"><span data-stu-id="cdeb1-147">No</span></span>  <br/> |<span data-ttu-id="cdeb1-148">いいえ</span><span class="sxs-lookup"><span data-stu-id="cdeb1-148">No</span></span>  <br/> |<span data-ttu-id="cdeb1-149">はい</span><span class="sxs-lookup"><span data-stu-id="cdeb1-149">Yes</span></span>  <br/> |
|<span data-ttu-id="cdeb1-150">**SaveChanges**の前に使用可能です</span><span class="sxs-lookup"><span data-stu-id="cdeb1-150">Available before **SaveChanges**</span></span> <br/> |<span data-ttu-id="cdeb1-151">プロバイダーの実装に依存します。</span><span class="sxs-lookup"><span data-stu-id="cdeb1-151">Depends on the provider implementation</span></span>  <br/> |<span data-ttu-id="cdeb1-152">プロバイダーの実装に依存します。</span><span class="sxs-lookup"><span data-stu-id="cdeb1-152">Depends on the provider implementation</span></span>  <br/> |<span data-ttu-id="cdeb1-153">メッセージは、[はい] です。</span><span class="sxs-lookup"><span data-stu-id="cdeb1-153">For messages, Yes.</span></span> <span data-ttu-id="cdeb1-154">他のユーザーが、プロバイダーの実装によって異なります。</span><span class="sxs-lookup"><span data-stu-id="cdeb1-154">For others, It depends on the provider implementation.</span></span>  <br/> |
|<span data-ttu-id="cdeb1-155">コピー操作で変更</span><span class="sxs-lookup"><span data-stu-id="cdeb1-155">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="cdeb1-156">はい</span><span class="sxs-lookup"><span data-stu-id="cdeb1-156">Yes</span></span>  <br/> |<span data-ttu-id="cdeb1-157">はい</span><span class="sxs-lookup"><span data-stu-id="cdeb1-157">Yes</span></span>  <br/> |<span data-ttu-id="cdeb1-158">いいえ</span><span class="sxs-lookup"><span data-stu-id="cdeb1-158">No</span></span>  <br/> |
|<span data-ttu-id="cdeb1-159">コピー後にクライアントによって変更可能です</span><span class="sxs-lookup"><span data-stu-id="cdeb1-159">Changeable by client after a copy</span></span>  <br/> |<span data-ttu-id="cdeb1-160">いいえ</span><span class="sxs-lookup"><span data-stu-id="cdeb1-160">No</span></span>  <br/> |<span data-ttu-id="cdeb1-161">いいえ</span><span class="sxs-lookup"><span data-stu-id="cdeb1-161">No</span></span>  <br/> |<span data-ttu-id="cdeb1-162">はい</span><span class="sxs-lookup"><span data-stu-id="cdeb1-162">Yes</span></span>  <br/> |
|<span data-ttu-id="cdeb1-163">内で重複しています.</span><span class="sxs-lookup"><span data-stu-id="cdeb1-163">Unique within ...</span></span>  <br/> |<span data-ttu-id="cdeb1-164">全体の世界</span><span class="sxs-lookup"><span data-stu-id="cdeb1-164">Entire world</span></span>  <br/> |<span data-ttu-id="cdeb1-165">プロバイダーのインスタンス</span><span class="sxs-lookup"><span data-stu-id="cdeb1-165">Provider instance</span></span>  <br/> |<span data-ttu-id="cdeb1-166">全体の世界</span><span class="sxs-lookup"><span data-stu-id="cdeb1-166">Entire world</span></span>  <br/> |
|<span data-ttu-id="cdeb1-167">バイナリ (ため) と同じように匹敵します。</span><span class="sxs-lookup"><span data-stu-id="cdeb1-167">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="cdeb1-168">いいえ-- [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)を使用して、</span><span class="sxs-lookup"><span data-stu-id="cdeb1-168">No -- use [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)</span></span> <br/> |<span data-ttu-id="cdeb1-169">はい</span><span class="sxs-lookup"><span data-stu-id="cdeb1-169">Yes</span></span>  <br/> |<span data-ttu-id="cdeb1-170">はい</span><span class="sxs-lookup"><span data-stu-id="cdeb1-170">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="cdeb1-171">関連リソース</span><span class="sxs-lookup"><span data-stu-id="cdeb1-171">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cdeb1-172">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="cdeb1-172">Protocol specifications</span></span>

<span data-ttu-id="cdeb1-173">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cdeb1-173">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cdeb1-174">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="cdeb1-174">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cdeb1-175">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cdeb1-175">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cdeb1-176">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="cdeb1-176">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="cdeb1-177">[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cdeb1-177">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cdeb1-178">プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="cdeb1-178">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cdeb1-179">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="cdeb1-179">Header files</span></span>

<span data-ttu-id="cdeb1-180">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cdeb1-180">Mapidefs.h</span></span>
  
> <span data-ttu-id="cdeb1-181">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="cdeb1-181">Provides data type definitions.</span></span>
    
<span data-ttu-id="cdeb1-182">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cdeb1-182">Mapitags.h</span></span>
  
> <span data-ttu-id="cdeb1-183">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="cdeb1-183">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cdeb1-184">関連項目</span><span class="sxs-lookup"><span data-stu-id="cdeb1-184">See also</span></span>



[<span data-ttu-id="cdeb1-185">PidTagResponsibility 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="cdeb1-185">PidTagResponsibility Canonical Property</span></span>](pidtagresponsibility-canonical-property.md)
  
[<span data-ttu-id="cdeb1-186">PidTagStoreRecordKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="cdeb1-186">PidTagStoreRecordKey Canonical Property</span></span>](pidtagstorerecordkey-canonical-property.md)


[<span data-ttu-id="cdeb1-187">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="cdeb1-187">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cdeb1-188">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="cdeb1-188">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cdeb1-189">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="cdeb1-189">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cdeb1-190">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="cdeb1-190">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

