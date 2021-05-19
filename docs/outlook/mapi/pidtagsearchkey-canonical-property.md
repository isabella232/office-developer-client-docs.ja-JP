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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9e6b9ddf37c1db8ea28ae2f82caed2a487e551e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345466"
---
# <a name="pidtagsearchkey-canonical-property"></a><span data-ttu-id="b2b40-103">PidTagSearchKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b2b40-103">PidTagSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="b2b40-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b2b40-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b2b40-105">検索の関連オブジェクトを識別するバイナリ比較可能なキーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b2b40-105">Contains a binary-comparable key that identifies correlated objects for a search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b2b40-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="b2b40-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b2b40-107">PR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="b2b40-107">PR_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="b2b40-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="b2b40-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b2b40-109">0x300B</span><span class="sxs-lookup"><span data-stu-id="b2b40-109">0x300B</span></span>  <br/> |
|<span data-ttu-id="b2b40-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b2b40-110">Data type:</span></span>  <br/> |<span data-ttu-id="b2b40-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b2b40-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b2b40-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="b2b40-112">Area:</span></span>  <br/> |<span data-ttu-id="b2b40-113">ID プロパティ</span><span class="sxs-lookup"><span data-stu-id="b2b40-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b2b40-114">注釈</span><span class="sxs-lookup"><span data-stu-id="b2b40-114">Remarks</span></span>

<span data-ttu-id="b2b40-115">このプロパティは、メッセージ コピーなどの関連オブジェクトのトレースを提供し、重複する受信者などの不要な発生を見つけ出すのを容易にします。</span><span class="sxs-lookup"><span data-stu-id="b2b40-115">This property provides a trace for related objects, such as message copies, and facilitates finding unwanted occurrences, such as duplicate recipients.</span></span>
  
<span data-ttu-id="b2b40-116">MAPI は、メッセージ受信者の検索キーを作成するための特定のルールを使用します。</span><span class="sxs-lookup"><span data-stu-id="b2b40-116">MAPI uses specific rules for constructing search keys for message recipients.</span></span> <span data-ttu-id="b2b40-117">検索キーは、アドレスの種類 (大文字)、コロン文字 ':'、電子メール アドレスを標準形式で連結し、終端の null 文字を連結して形成されます。</span><span class="sxs-lookup"><span data-stu-id="b2b40-117">The search key is formed by concatenating the address type (in uppercase characters), the colon character ':', the email address in canonical form, and the terminating null character.</span></span> <span data-ttu-id="b2b40-118">ここでの標準の形式は、大文字と小文字を区別するアドレスが正しい場合に表示され、大文字と小文字を区別しないアドレスが大文字に変換されていることを意味します。</span><span class="sxs-lookup"><span data-stu-id="b2b40-118">Canonical form here means that case-sensitive addresses appear in the correct case, and addresses that are not case-sensitive are converted to uppercase.</span></span> <span data-ttu-id="b2b40-119">これは、メッセージ間の相関関係を保持する場合に重要です。</span><span class="sxs-lookup"><span data-stu-id="b2b40-119">This is important in preserving correlations among messages.</span></span>
  
<span data-ttu-id="b2b40-120">メッセージ オブジェクトの場合、このプロパティは、メッセージの作成直後に [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを使用して使用できます。</span><span class="sxs-lookup"><span data-stu-id="b2b40-120">For message objects, this property is available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method immediately following message creation.</span></span> <span data-ttu-id="b2b40-121">他のオブジェクトでは [、IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドの最初の呼び出しに従って使用できます。</span><span class="sxs-lookup"><span data-stu-id="b2b40-121">For other objects, it is available following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="b2b40-122">このプロパティは変更可能なので **、SaveChanges** 呼び出しが [IMAPIProp::SetProps](imapiprop-setprops.md)メソッドによって設定または変更された値をコミットするまで **、GetProps** を使用して取得することはできません。</span><span class="sxs-lookup"><span data-stu-id="b2b40-122">Because this property is changeable, it is unreliable to obtain it through **GetProps** until a **SaveChanges** call has committed any values set or changed by the [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> 
  
<span data-ttu-id="b2b40-123">プロファイルの場合、MAPI は、このプロパティを **単** 一のプロパティとして、MUID_PROFILE_INSTANCE という名前のハードコードされたプロファイル セクションも提供します。</span><span class="sxs-lookup"><span data-stu-id="b2b40-123">For profiles, MAPI also furnishes a hard-coded profile section named **MUID_PROFILE_INSTANCE**, with this property as its single property.</span></span> <span data-ttu-id="b2b40-124">このキーは、これまでに作成されたプロファイル間で一意であることを保証され **、PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) プロパティよりも信頼性が高く、たとえば、同じ名前で削除および再作成できます。</span><span class="sxs-lookup"><span data-stu-id="b2b40-124">This key is guaranteed to be unique among all profiles ever created, and can be more reliable than the **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) property, which can be, for example, deleted and recreated with the same name.</span></span>
  
<span data-ttu-id="b2b40-125">次の表に、PR_ENTRYID **(** [PidTagEntryId)](pidtagentryid-canonical-property.md)、PR_RECORD_KEY **(** [PidTagRecordKey)](pidtagrecordkey-canonical-property.md)、およびこのプロパティの重要な違いを示します。</span><span class="sxs-lookup"><span data-stu-id="b2b40-125">The following table summarizes important differences among the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), and this property.</span></span>
  
|<span data-ttu-id="b2b40-126">**特性**</span><span class="sxs-lookup"><span data-stu-id="b2b40-126">**Characteristic**</span></span>|<span data-ttu-id="b2b40-127">PR_ENTRYID\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="b2b40-127">\*\*\*\*PR_ENTRYID\*\*\*\*</span></span>|<span data-ttu-id="b2b40-128">PR_RECORD_KEY\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="b2b40-128">\*\*\*\*PR_RECORD_KEY\*\*\*\*</span></span>|<span data-ttu-id="b2b40-129">PR_SEARCH_KEY\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="b2b40-129">\*\*\*\*PR_SEARCH_KEY\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b2b40-130">添付ファイル オブジェクトに必須</span><span class="sxs-lookup"><span data-stu-id="b2b40-130">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="b2b40-131">いいえ</span><span class="sxs-lookup"><span data-stu-id="b2b40-131">No</span></span>  <br/> |<span data-ttu-id="b2b40-132">はい</span><span class="sxs-lookup"><span data-stu-id="b2b40-132">Yes</span></span>  <br/> |<span data-ttu-id="b2b40-133">いいえ</span><span class="sxs-lookup"><span data-stu-id="b2b40-133">No</span></span>  <br/> |
|<span data-ttu-id="b2b40-134">フォルダー オブジェクトに必須</span><span class="sxs-lookup"><span data-stu-id="b2b40-134">Required on folder objects</span></span>  <br/> |<span data-ttu-id="b2b40-135">はい</span><span class="sxs-lookup"><span data-stu-id="b2b40-135">Yes</span></span>  <br/> |<span data-ttu-id="b2b40-136">はい</span><span class="sxs-lookup"><span data-stu-id="b2b40-136">Yes</span></span>  <br/> |<span data-ttu-id="b2b40-137">いいえ</span><span class="sxs-lookup"><span data-stu-id="b2b40-137">No</span></span>  <br/> |
|<span data-ttu-id="b2b40-138">メッセージ ストア オブジェクトで必須</span><span class="sxs-lookup"><span data-stu-id="b2b40-138">Required on message store objects</span></span>  <br/> |<span data-ttu-id="b2b40-139">はい</span><span class="sxs-lookup"><span data-stu-id="b2b40-139">Yes</span></span>  <br/> |<span data-ttu-id="b2b40-140">はい</span><span class="sxs-lookup"><span data-stu-id="b2b40-140">Yes</span></span>  <br/> |<span data-ttu-id="b2b40-141">いいえ</span><span class="sxs-lookup"><span data-stu-id="b2b40-141">No</span></span>  <br/> |
|<span data-ttu-id="b2b40-142">状態オブジェクトで必須</span><span class="sxs-lookup"><span data-stu-id="b2b40-142">Required on status objects</span></span>  <br/> |<span data-ttu-id="b2b40-143">はい</span><span class="sxs-lookup"><span data-stu-id="b2b40-143">Yes</span></span>  <br/> |<span data-ttu-id="b2b40-144">いいえ</span><span class="sxs-lookup"><span data-stu-id="b2b40-144">No</span></span>  <br/> |<span data-ttu-id="b2b40-145">いいえ</span><span class="sxs-lookup"><span data-stu-id="b2b40-145">No</span></span>  <br/> |
|<span data-ttu-id="b2b40-146">クライアントによる折りたたみ可能</span><span class="sxs-lookup"><span data-stu-id="b2b40-146">Creatable by client</span></span>  <br/> |<span data-ttu-id="b2b40-147">いいえ</span><span class="sxs-lookup"><span data-stu-id="b2b40-147">No</span></span>  <br/> |<span data-ttu-id="b2b40-148">いいえ</span><span class="sxs-lookup"><span data-stu-id="b2b40-148">No</span></span>  <br/> |<span data-ttu-id="b2b40-149">はい</span><span class="sxs-lookup"><span data-stu-id="b2b40-149">Yes</span></span>  <br/> |
|<span data-ttu-id="b2b40-150">**SaveChanges の前に使用可能**</span><span class="sxs-lookup"><span data-stu-id="b2b40-150">Available before **SaveChanges**</span></span> <br/> |<span data-ttu-id="b2b40-151">プロバイダーの実装によって異なります</span><span class="sxs-lookup"><span data-stu-id="b2b40-151">Depends on the provider implementation</span></span>  <br/> |<span data-ttu-id="b2b40-152">プロバイダーの実装によって異なります</span><span class="sxs-lookup"><span data-stu-id="b2b40-152">Depends on the provider implementation</span></span>  <br/> |<span data-ttu-id="b2b40-153">メッセージの場合は、はい。</span><span class="sxs-lookup"><span data-stu-id="b2b40-153">For messages, Yes.</span></span> <span data-ttu-id="b2b40-154">その他の場合は、プロバイダーの実装によって異なります。</span><span class="sxs-lookup"><span data-stu-id="b2b40-154">For others, It depends on the provider implementation.</span></span>  <br/> |
|<span data-ttu-id="b2b40-155">コピー操作で変更された</span><span class="sxs-lookup"><span data-stu-id="b2b40-155">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="b2b40-156">はい</span><span class="sxs-lookup"><span data-stu-id="b2b40-156">Yes</span></span>  <br/> |<span data-ttu-id="b2b40-157">はい</span><span class="sxs-lookup"><span data-stu-id="b2b40-157">Yes</span></span>  <br/> |<span data-ttu-id="b2b40-158">いいえ</span><span class="sxs-lookup"><span data-stu-id="b2b40-158">No</span></span>  <br/> |
|<span data-ttu-id="b2b40-159">コピー後にクライアントが変更可能</span><span class="sxs-lookup"><span data-stu-id="b2b40-159">Changeable by client after a copy</span></span>  <br/> |<span data-ttu-id="b2b40-160">いいえ</span><span class="sxs-lookup"><span data-stu-id="b2b40-160">No</span></span>  <br/> |<span data-ttu-id="b2b40-161">いいえ</span><span class="sxs-lookup"><span data-stu-id="b2b40-161">No</span></span>  <br/> |<span data-ttu-id="b2b40-162">はい</span><span class="sxs-lookup"><span data-stu-id="b2b40-162">Yes</span></span>  <br/> |
|<span data-ttu-id="b2b40-163">..内で一意です。</span><span class="sxs-lookup"><span data-stu-id="b2b40-163">Unique within ...</span></span>  <br/> |<span data-ttu-id="b2b40-164">ワールド全体</span><span class="sxs-lookup"><span data-stu-id="b2b40-164">Entire world</span></span>  <br/> |<span data-ttu-id="b2b40-165">プロバイダー インスタンス</span><span class="sxs-lookup"><span data-stu-id="b2b40-165">Provider instance</span></span>  <br/> |<span data-ttu-id="b2b40-166">ワールド全体</span><span class="sxs-lookup"><span data-stu-id="b2b40-166">Entire world</span></span>  <br/> |
|<span data-ttu-id="b2b40-167">バイナリ比較 (memcmp と同様)</span><span class="sxs-lookup"><span data-stu-id="b2b40-167">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="b2b40-168">いいえ -- [IMAPISupport::CompareEntryIDs を使用する](imapisupport-compareentryids.md)</span><span class="sxs-lookup"><span data-stu-id="b2b40-168">No -- use [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)</span></span> <br/> |<span data-ttu-id="b2b40-169">はい</span><span class="sxs-lookup"><span data-stu-id="b2b40-169">Yes</span></span>  <br/> |<span data-ttu-id="b2b40-170">はい</span><span class="sxs-lookup"><span data-stu-id="b2b40-170">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="b2b40-171">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b2b40-171">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b2b40-172">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="b2b40-172">Protocol specifications</span></span>

<span data-ttu-id="b2b40-173">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b2b40-173">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b2b40-174">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="b2b40-174">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b2b40-175">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b2b40-175">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b2b40-176">メッセージ オブジェクトと添付ファイル オブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="b2b40-176">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="b2b40-177">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b2b40-177">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b2b40-178">ユーザー、連絡先、グループ、およびリソースの一覧のプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="b2b40-178">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b2b40-179">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b2b40-179">Header files</span></span>

<span data-ttu-id="b2b40-180">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b2b40-180">Mapidefs.h</span></span>
  
> <span data-ttu-id="b2b40-181">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b2b40-181">Provides data type definitions.</span></span>
    
<span data-ttu-id="b2b40-182">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b2b40-182">Mapitags.h</span></span>
  
> <span data-ttu-id="b2b40-183">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="b2b40-183">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b2b40-184">関連項目</span><span class="sxs-lookup"><span data-stu-id="b2b40-184">See also</span></span>



[<span data-ttu-id="b2b40-185">PidTagResponsibility 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b2b40-185">PidTagResponsibility Canonical Property</span></span>](pidtagresponsibility-canonical-property.md)
  
[<span data-ttu-id="b2b40-186">PidTagStoreRecordKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b2b40-186">PidTagStoreRecordKey Canonical Property</span></span>](pidtagstorerecordkey-canonical-property.md)


[<span data-ttu-id="b2b40-187">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="b2b40-187">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b2b40-188">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b2b40-188">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b2b40-189">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="b2b40-189">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b2b40-190">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="b2b40-190">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

