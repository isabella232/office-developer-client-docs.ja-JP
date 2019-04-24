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
ms.openlocfilehash: 9e6b9ddf37c1db8ea28ae2f82caed2a487e551e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345466"
---
# <a name="pidtagsearchkey-canonical-property"></a><span data-ttu-id="44cf7-103">PidTagSearchKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="44cf7-103">PidTagSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="44cf7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44cf7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44cf7-105">検索の相関オブジェクトを識別する2つの比較可能なキーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="44cf7-105">Contains a binary-comparable key that identifies correlated objects for a search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="44cf7-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="44cf7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="44cf7-107">PR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="44cf7-107">PR_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="44cf7-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="44cf7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="44cf7-109">0x300b</span><span class="sxs-lookup"><span data-stu-id="44cf7-109">0x300B</span></span>  <br/> |
|<span data-ttu-id="44cf7-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="44cf7-110">Data type:</span></span>  <br/> |<span data-ttu-id="44cf7-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="44cf7-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="44cf7-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="44cf7-112">Area:</span></span>  <br/> |<span data-ttu-id="44cf7-113">ID プロパティ</span><span class="sxs-lookup"><span data-stu-id="44cf7-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="44cf7-114">解説</span><span class="sxs-lookup"><span data-stu-id="44cf7-114">Remarks</span></span>

<span data-ttu-id="44cf7-115">このプロパティは、メッセージのコピーなどの関連オブジェクトのトレースを提供し、重複した受信者などの不必要な出現を検索しやすくします。</span><span class="sxs-lookup"><span data-stu-id="44cf7-115">This property provides a trace for related objects, such as message copies, and facilitates finding unwanted occurrences, such as duplicate recipients.</span></span>
  
<span data-ttu-id="44cf7-116">MAPI では、メッセージの受信者の検索キーを作成するための特定のルールを使用します。</span><span class="sxs-lookup"><span data-stu-id="44cf7-116">MAPI uses specific rules for constructing search keys for message recipients.</span></span> <span data-ttu-id="44cf7-117">検索キーは、アドレスの種類 (大文字で表記)、コロン文字 ': '、標準形式の電子メールアドレス、および終端の null 文字を連結して形成されます。</span><span class="sxs-lookup"><span data-stu-id="44cf7-117">The search key is formed by concatenating the address type (in uppercase characters), the colon character ':', the email address in canonical form, and the terminating null character.</span></span> <span data-ttu-id="44cf7-118">ここでは、大文字と小文字が区別され、大文字と小文字が区別されないアドレスが大文字に変換されることを意味します。</span><span class="sxs-lookup"><span data-stu-id="44cf7-118">Canonical form here means that case-sensitive addresses appear in the correct case, and addresses that are not case-sensitive are converted to uppercase.</span></span> <span data-ttu-id="44cf7-119">これは、メッセージ間の相互関係を維持するために重要です。</span><span class="sxs-lookup"><span data-stu-id="44cf7-119">This is important in preserving correlations among messages.</span></span>
  
<span data-ttu-id="44cf7-120">message オブジェクトの場合、このプロパティは、メッセージの作成直後に[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを通じて使用できます。</span><span class="sxs-lookup"><span data-stu-id="44cf7-120">For message objects, this property is available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method immediately following message creation.</span></span> <span data-ttu-id="44cf7-121">その他のオブジェクトの場合は、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを最初に呼び出した後に使用できます。</span><span class="sxs-lookup"><span data-stu-id="44cf7-121">For other objects, it is available following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="44cf7-122">このプロパティは変更可能なので、 **SaveChanges**呼び出しが[imapiprop:: setprops](imapiprop-setprops.md)メソッドによって設定または変更された値をコミットするまでは、 **GetProps**経由で取得することはできません。</span><span class="sxs-lookup"><span data-stu-id="44cf7-122">Because this property is changeable, it is unreliable to obtain it through **GetProps** until a **SaveChanges** call has committed any values set or changed by the [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> 
  
<span data-ttu-id="44cf7-123">プロファイルの場合、MAPI は、 **MUID_PROFILE_INSTANCE**というハードコードされたプロファイルセクションを furnishes します。このプロパティは、このプロパティを単一のプロパティとして使用します。</span><span class="sxs-lookup"><span data-stu-id="44cf7-123">For profiles, MAPI also furnishes a hard-coded profile section named **MUID_PROFILE_INSTANCE**, with this property as its single property.</span></span> <span data-ttu-id="44cf7-124">このキーは、作成されたすべてのプロファイル間で一意であることが保証されており、 **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) プロパティよりも信頼性が高くなることがあります。たとえば、削除されて同じ名前で再作成されます。</span><span class="sxs-lookup"><span data-stu-id="44cf7-124">This key is guaranteed to be unique among all profiles ever created, and can be more reliable than the **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) property, which can be, for example, deleted and recreated with the same name.</span></span>
  
<span data-ttu-id="44cf7-125">次の表は、 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))、 **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))、およびこのプロパティの重要な相違点をまとめたものです。</span><span class="sxs-lookup"><span data-stu-id="44cf7-125">The following table summarizes important differences among the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), and this property.</span></span>
  
|<span data-ttu-id="44cf7-126">**特性**</span><span class="sxs-lookup"><span data-stu-id="44cf7-126">**Characteristic**</span></span>|<span data-ttu-id="44cf7-127">PR_ENTRYID \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="44cf7-127">\*\*\*\*PR_ENTRYID\*\*\*\*</span></span>|<span data-ttu-id="44cf7-128">PR_RECORD_KEY \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="44cf7-128">\*\*\*\*PR_RECORD_KEY\*\*\*\*</span></span>|<span data-ttu-id="44cf7-129">PR_SEARCH_KEY \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="44cf7-129">\*\*\*\*PR_SEARCH_KEY\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="44cf7-130">attachment オブジェクトに必要</span><span class="sxs-lookup"><span data-stu-id="44cf7-130">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="44cf7-131">いいえ</span><span class="sxs-lookup"><span data-stu-id="44cf7-131">No</span></span>  <br/> |<span data-ttu-id="44cf7-132">はい</span><span class="sxs-lookup"><span data-stu-id="44cf7-132">Yes</span></span>  <br/> |<span data-ttu-id="44cf7-133">いいえ</span><span class="sxs-lookup"><span data-stu-id="44cf7-133">No</span></span>  <br/> |
|<span data-ttu-id="44cf7-134">folder オブジェクトで必要</span><span class="sxs-lookup"><span data-stu-id="44cf7-134">Required on folder objects</span></span>  <br/> |<span data-ttu-id="44cf7-135">はい</span><span class="sxs-lookup"><span data-stu-id="44cf7-135">Yes</span></span>  <br/> |<span data-ttu-id="44cf7-136">はい</span><span class="sxs-lookup"><span data-stu-id="44cf7-136">Yes</span></span>  <br/> |<span data-ttu-id="44cf7-137">いいえ</span><span class="sxs-lookup"><span data-stu-id="44cf7-137">No</span></span>  <br/> |
|<span data-ttu-id="44cf7-138">メッセージストアオブジェクトに必要</span><span class="sxs-lookup"><span data-stu-id="44cf7-138">Required on message store objects</span></span>  <br/> |<span data-ttu-id="44cf7-139">はい</span><span class="sxs-lookup"><span data-stu-id="44cf7-139">Yes</span></span>  <br/> |<span data-ttu-id="44cf7-140">はい</span><span class="sxs-lookup"><span data-stu-id="44cf7-140">Yes</span></span>  <br/> |<span data-ttu-id="44cf7-141">いいえ</span><span class="sxs-lookup"><span data-stu-id="44cf7-141">No</span></span>  <br/> |
|<span data-ttu-id="44cf7-142">状態オブジェクトに必要です</span><span class="sxs-lookup"><span data-stu-id="44cf7-142">Required on status objects</span></span>  <br/> |<span data-ttu-id="44cf7-143">はい</span><span class="sxs-lookup"><span data-stu-id="44cf7-143">Yes</span></span>  <br/> |<span data-ttu-id="44cf7-144">いいえ</span><span class="sxs-lookup"><span data-stu-id="44cf7-144">No</span></span>  <br/> |<span data-ttu-id="44cf7-145">いいえ</span><span class="sxs-lookup"><span data-stu-id="44cf7-145">No</span></span>  <br/> |
|<span data-ttu-id="44cf7-146">クライアントによるのが可能</span><span class="sxs-lookup"><span data-stu-id="44cf7-146">Creatable by client</span></span>  <br/> |<span data-ttu-id="44cf7-147">いいえ</span><span class="sxs-lookup"><span data-stu-id="44cf7-147">No</span></span>  <br/> |<span data-ttu-id="44cf7-148">いいえ</span><span class="sxs-lookup"><span data-stu-id="44cf7-148">No</span></span>  <br/> |<span data-ttu-id="44cf7-149">はい</span><span class="sxs-lookup"><span data-stu-id="44cf7-149">Yes</span></span>  <br/> |
|<span data-ttu-id="44cf7-150">**SaveChanges**の前に使用可能</span><span class="sxs-lookup"><span data-stu-id="44cf7-150">Available before **SaveChanges**</span></span> <br/> |<span data-ttu-id="44cf7-151">プロバイダーの実装によって異なります。</span><span class="sxs-lookup"><span data-stu-id="44cf7-151">Depends on the provider implementation</span></span>  <br/> |<span data-ttu-id="44cf7-152">プロバイダーの実装によって異なります。</span><span class="sxs-lookup"><span data-stu-id="44cf7-152">Depends on the provider implementation</span></span>  <br/> |<span data-ttu-id="44cf7-153">メッセージの場合は、はい。</span><span class="sxs-lookup"><span data-stu-id="44cf7-153">For messages, Yes.</span></span> <span data-ttu-id="44cf7-154">その他の場合は、プロバイダーの実装によって異なります。</span><span class="sxs-lookup"><span data-stu-id="44cf7-154">For others, It depends on the provider implementation.</span></span>  <br/> |
|<span data-ttu-id="44cf7-155">コピー操作で変更</span><span class="sxs-lookup"><span data-stu-id="44cf7-155">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="44cf7-156">はい</span><span class="sxs-lookup"><span data-stu-id="44cf7-156">Yes</span></span>  <br/> |<span data-ttu-id="44cf7-157">はい</span><span class="sxs-lookup"><span data-stu-id="44cf7-157">Yes</span></span>  <br/> |<span data-ttu-id="44cf7-158">いいえ</span><span class="sxs-lookup"><span data-stu-id="44cf7-158">No</span></span>  <br/> |
|<span data-ttu-id="44cf7-159">コピー後にクライアントによって変更可能</span><span class="sxs-lookup"><span data-stu-id="44cf7-159">Changeable by client after a copy</span></span>  <br/> |<span data-ttu-id="44cf7-160">いいえ</span><span class="sxs-lookup"><span data-stu-id="44cf7-160">No</span></span>  <br/> |<span data-ttu-id="44cf7-161">いいえ</span><span class="sxs-lookup"><span data-stu-id="44cf7-161">No</span></span>  <br/> |<span data-ttu-id="44cf7-162">はい</span><span class="sxs-lookup"><span data-stu-id="44cf7-162">Yes</span></span>  <br/> |
|<span data-ttu-id="44cf7-163">一意の範囲</span><span class="sxs-lookup"><span data-stu-id="44cf7-163">Unique within ...</span></span>  <br/> |<span data-ttu-id="44cf7-164">世界全体</span><span class="sxs-lookup"><span data-stu-id="44cf7-164">Entire world</span></span>  <br/> |<span data-ttu-id="44cf7-165">プロバイダーインスタンス</span><span class="sxs-lookup"><span data-stu-id="44cf7-165">Provider instance</span></span>  <br/> |<span data-ttu-id="44cf7-166">世界全体</span><span class="sxs-lookup"><span data-stu-id="44cf7-166">Entire world</span></span>  <br/> |
|<span data-ttu-id="44cf7-167">二項比較 (memcmp と同じ)</span><span class="sxs-lookup"><span data-stu-id="44cf7-167">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="44cf7-168">No-- [imapisupport:: compareentryids](imapisupport-compareentryids.md)を使用します。</span><span class="sxs-lookup"><span data-stu-id="44cf7-168">No -- use [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)</span></span> <br/> |<span data-ttu-id="44cf7-169">はい</span><span class="sxs-lookup"><span data-stu-id="44cf7-169">Yes</span></span>  <br/> |<span data-ttu-id="44cf7-170">はい</span><span class="sxs-lookup"><span data-stu-id="44cf7-170">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="44cf7-171">関連リソース</span><span class="sxs-lookup"><span data-stu-id="44cf7-171">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="44cf7-172">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="44cf7-172">Protocol specifications</span></span>

<span data-ttu-id="44cf7-173">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="44cf7-173">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="44cf7-174">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="44cf7-174">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="44cf7-175">[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="44cf7-175">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="44cf7-176">メッセージと添付ファイルオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="44cf7-176">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="44cf7-177">[[OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="44cf7-177">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="44cf7-178">ユーザー、連絡先、グループ、およびリソースのリストのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="44cf7-178">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="44cf7-179">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="44cf7-179">Header files</span></span>

<span data-ttu-id="44cf7-180">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="44cf7-180">Mapidefs.h</span></span>
  
> <span data-ttu-id="44cf7-181">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="44cf7-181">Provides data type definitions.</span></span>
    
<span data-ttu-id="44cf7-182">Mapitags</span><span class="sxs-lookup"><span data-stu-id="44cf7-182">Mapitags.h</span></span>
  
> <span data-ttu-id="44cf7-183">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="44cf7-183">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="44cf7-184">関連項目</span><span class="sxs-lookup"><span data-stu-id="44cf7-184">See also</span></span>



[<span data-ttu-id="44cf7-185">PidTagResponsibility 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="44cf7-185">PidTagResponsibility Canonical Property</span></span>](pidtagresponsibility-canonical-property.md)
  
[<span data-ttu-id="44cf7-186">PidTagStoreRecordKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="44cf7-186">PidTagStoreRecordKey Canonical Property</span></span>](pidtagstorerecordkey-canonical-property.md)


[<span data-ttu-id="44cf7-187">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="44cf7-187">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="44cf7-188">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="44cf7-188">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="44cf7-189">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="44cf7-189">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="44cf7-190">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="44cf7-190">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

