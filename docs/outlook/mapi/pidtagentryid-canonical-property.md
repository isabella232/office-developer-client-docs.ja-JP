---
title: PidTagEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagEntryId
api_type:
- HeaderDef
ms.assetid: ca02e873-c2d2-4d58-8df8-c05fbcdc8fba
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: feb34cdbf8ba917936c3272bcaaf6eff040ddc3a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328589"
---
# <a name="pidtagentryid-canonical-property"></a><span data-ttu-id="d57d4-103">PidTagEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d57d4-103">PidTagEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="d57d4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d57d4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d57d4-105">特定の MAPI オブジェクトのプロパティを開いて編集するために使用される MAPI エントリ識別子が含まれる。</span><span class="sxs-lookup"><span data-stu-id="d57d4-105">Contains a MAPI entry identifier used to open and edit properties of a particular MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d57d4-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d57d4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d57d4-107">PR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="d57d4-107">PR_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="d57d4-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="d57d4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d57d4-109">0x0FFF</span><span class="sxs-lookup"><span data-stu-id="d57d4-109">0x0FFF</span></span>  <br/> |
|<span data-ttu-id="d57d4-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d57d4-110">Data type:</span></span>  <br/> |<span data-ttu-id="d57d4-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d57d4-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d57d4-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="d57d4-112">Area:</span></span>  <br/> |<span data-ttu-id="d57d4-113">ID プロパティ</span><span class="sxs-lookup"><span data-stu-id="d57d4-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d57d4-114">注釈</span><span class="sxs-lookup"><span data-stu-id="d57d4-114">Remarks</span></span>

<span data-ttu-id="d57d4-115">このプロパティは **、OpenEntry** がインスタンス化するオブジェクトを識別し、IMAPIProp の適切な派生インターフェイスを介してすべてのプロパティへの **アクセスを提供します**。</span><span class="sxs-lookup"><span data-stu-id="d57d4-115">This property identifies an object for **OpenEntry** to instantiate and provides access to all of its properties through the appropriate derived interface of **IMAPIProp**.</span></span> 
  
<span data-ttu-id="d57d4-116">このプロパティは、すべてのメッセージング ユーザーの基本アドレス プロパティの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="d57d4-116">This property is one of the base address properties for all messaging users.</span></span> 
  
<span data-ttu-id="d57d4-117">このプロパティには、長期識別子または短期識別子を含めできます。</span><span class="sxs-lookup"><span data-stu-id="d57d4-117">This property can contain either a long-term or a short-term identifier.</span></span> <span data-ttu-id="d57d4-118">短期的な識別子は、作成が簡単かつ高速ですが、スコープと期間は制限されます(通常は現在のセッションとワークステーションに限定されます)。</span><span class="sxs-lookup"><span data-stu-id="d57d4-118">Short-term identifiers are easier and faster to construct, but are limited in their scope and duration, typically to the current session and workstation.</span></span> <span data-ttu-id="d57d4-119">一般に、テーブル行やダイアログ ボックスエントリなどの一時的な性質のオブジェクトに使用され、破棄されます。</span><span class="sxs-lookup"><span data-stu-id="d57d4-119">They are commonly used for objects of a temporary nature, such as table rows or dialog box entries, and then abandoned.</span></span> <span data-ttu-id="d57d4-120">長期的な識別子は、より広範囲で長期的な性質のオブジェクトに使用されます。</span><span class="sxs-lookup"><span data-stu-id="d57d4-120">Long-term identifiers are used for objects of a more wide-ranging and long-lasting nature.</span></span> 
  
<span data-ttu-id="d57d4-121">このプロパティは [、IMAPIProp::SaveChanges](imapiprop-getprops.md) メソッドの最初の呼び出しに続く [IMAPIProp::GetProps](imapiprop-savechanges.md) メソッドを通じて常に使用できます。</span><span class="sxs-lookup"><span data-stu-id="d57d4-121">This property is always available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="d57d4-122">一部のサービス プロバイダーは、インスタンス化の直後に利用できます。</span><span class="sxs-lookup"><span data-stu-id="d57d4-122">Some service providers can make it available immediately after instantiation.</span></span> <span data-ttu-id="d57d4-123">プロバイダーは、常に GetProps から長期エントリ識別子を **返す必要があります**。</span><span class="sxs-lookup"><span data-stu-id="d57d4-123">The provider must always return a long-term entry identifier from **GetProps**.</span></span> <span data-ttu-id="d57d4-124">したがって、短期的な識別子を長期的に変換するには、オブジェクトを開き **、GetProps** を使用してこのプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="d57d4-124">Therefore, to convert a short-term identifier to long-term, simply open the object and get its this property through **GetProps**.</span></span> 
  
<span data-ttu-id="d57d4-125">次の表に、このプロパティ 、PR_RECORD_KEY **(** [PidTagRecordKey)](pidtagrecordkey-canonical-property.md)、および PR_SEARCH_KEY ([PidTagSearchKey)](pidtagsearchkey-canonical-property.md)の重要な違 **い** を示します。</span><span class="sxs-lookup"><span data-stu-id="d57d4-125">The following table summarizes important differences among this property, **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)).</span></span> 
  
|<span data-ttu-id="d57d4-126">**特性**</span><span class="sxs-lookup"><span data-stu-id="d57d4-126">**Characteristic**</span></span>|<span data-ttu-id="d57d4-127">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="d57d4-127">**PR_ENTRYID**</span></span>|<span data-ttu-id="d57d4-128">**PR_RECORD_KEY**</span><span class="sxs-lookup"><span data-stu-id="d57d4-128">**PR_RECORD_KEY**</span></span>|<span data-ttu-id="d57d4-129">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="d57d4-129">**PR_SEARCH_KEY**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d57d4-130">添付ファイル オブジェクトに必須</span><span class="sxs-lookup"><span data-stu-id="d57d4-130">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="d57d4-131">いいえ</span><span class="sxs-lookup"><span data-stu-id="d57d4-131">No</span></span>  <br/> |<span data-ttu-id="d57d4-132">はい</span><span class="sxs-lookup"><span data-stu-id="d57d4-132">Yes</span></span>  <br/> |<span data-ttu-id="d57d4-133">いいえ</span><span class="sxs-lookup"><span data-stu-id="d57d4-133">No</span></span>  <br/> |
|<span data-ttu-id="d57d4-134">フォルダー オブジェクトに必須</span><span class="sxs-lookup"><span data-stu-id="d57d4-134">Required on folder objects</span></span>  <br/> |<span data-ttu-id="d57d4-135">はい</span><span class="sxs-lookup"><span data-stu-id="d57d4-135">Yes</span></span>  <br/> |<span data-ttu-id="d57d4-136">はい</span><span class="sxs-lookup"><span data-stu-id="d57d4-136">Yes</span></span>  <br/> |<span data-ttu-id="d57d4-137">いいえ</span><span class="sxs-lookup"><span data-stu-id="d57d4-137">No</span></span>  <br/> |
|<span data-ttu-id="d57d4-138">メッセージ ストア オブジェクトで必須</span><span class="sxs-lookup"><span data-stu-id="d57d4-138">Required on message store objects</span></span>  <br/> |<span data-ttu-id="d57d4-139">はい</span><span class="sxs-lookup"><span data-stu-id="d57d4-139">Yes</span></span>  <br/> |<span data-ttu-id="d57d4-140">はい</span><span class="sxs-lookup"><span data-stu-id="d57d4-140">Yes</span></span>  <br/> |<span data-ttu-id="d57d4-141">いいえ</span><span class="sxs-lookup"><span data-stu-id="d57d4-141">No</span></span>  <br/> |
|<span data-ttu-id="d57d4-142">状態オブジェクトで必須</span><span class="sxs-lookup"><span data-stu-id="d57d4-142">Required on status objects</span></span>  <br/> |<span data-ttu-id="d57d4-143">はい</span><span class="sxs-lookup"><span data-stu-id="d57d4-143">Yes</span></span>  <br/> |<span data-ttu-id="d57d4-144">いいえ</span><span class="sxs-lookup"><span data-stu-id="d57d4-144">No</span></span>  <br/> |<span data-ttu-id="d57d4-145">いいえ</span><span class="sxs-lookup"><span data-stu-id="d57d4-145">No</span></span>  <br/> |
|<span data-ttu-id="d57d4-146">クライアントによって作成される</span><span class="sxs-lookup"><span data-stu-id="d57d4-146">Created by client</span></span>  <br/> |<span data-ttu-id="d57d4-147">いいえ</span><span class="sxs-lookup"><span data-stu-id="d57d4-147">No</span></span>  <br/> |<span data-ttu-id="d57d4-148">いいえ</span><span class="sxs-lookup"><span data-stu-id="d57d4-148">No</span></span>  <br/> |<span data-ttu-id="d57d4-149">はい</span><span class="sxs-lookup"><span data-stu-id="d57d4-149">Yes</span></span>  <br/> |
|<span data-ttu-id="d57d4-150">SaveChanges の呼び **出し前に使用可能**</span><span class="sxs-lookup"><span data-stu-id="d57d4-150">Available before call to **SaveChanges**</span></span> <br/> |<span data-ttu-id="d57d4-151">プロバイダーの実装によって異なります</span><span class="sxs-lookup"><span data-stu-id="d57d4-151">Depends on provider implementation</span></span>  <br/> |<span data-ttu-id="d57d4-152">プロバイダーの実装によって異なります</span><span class="sxs-lookup"><span data-stu-id="d57d4-152">Depends on provider implementation</span></span>  <br/> |<span data-ttu-id="d57d4-153">メッセージの場合は、はい。</span><span class="sxs-lookup"><span data-stu-id="d57d4-153">For messages, Yes.</span></span> <span data-ttu-id="d57d4-154">その他の場合は、プロバイダーの実装に依存します。</span><span class="sxs-lookup"><span data-stu-id="d57d4-154">For others, depends on provider implementation.</span></span>  <br/> |
|<span data-ttu-id="d57d4-155">コピー操作で変更された</span><span class="sxs-lookup"><span data-stu-id="d57d4-155">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="d57d4-156">はい</span><span class="sxs-lookup"><span data-stu-id="d57d4-156">Yes</span></span>  <br/> |<span data-ttu-id="d57d4-157">はい</span><span class="sxs-lookup"><span data-stu-id="d57d4-157">Yes</span></span>  <br/> |<span data-ttu-id="d57d4-158">いいえ</span><span class="sxs-lookup"><span data-stu-id="d57d4-158">No</span></span>  <br/> |
|<span data-ttu-id="d57d4-159">コピー後にクライアントが変更可能</span><span class="sxs-lookup"><span data-stu-id="d57d4-159">Changeable by client after a copy</span></span>  <br/> |<span data-ttu-id="d57d4-160">いいえ</span><span class="sxs-lookup"><span data-stu-id="d57d4-160">No</span></span>  <br/> |<span data-ttu-id="d57d4-161">いいえ</span><span class="sxs-lookup"><span data-stu-id="d57d4-161">No</span></span>  <br/> |<span data-ttu-id="d57d4-162">はい</span><span class="sxs-lookup"><span data-stu-id="d57d4-162">Yes</span></span>  <br/> |
|<span data-ttu-id="d57d4-163">内で一意</span><span class="sxs-lookup"><span data-stu-id="d57d4-163">Unique within</span></span>  <br/> |<span data-ttu-id="d57d4-164">ワールド全体</span><span class="sxs-lookup"><span data-stu-id="d57d4-164">Entire world</span></span>  <br/> |<span data-ttu-id="d57d4-165">プロバイダー インスタンス</span><span class="sxs-lookup"><span data-stu-id="d57d4-165">Provider instance</span></span>  <br/> |<span data-ttu-id="d57d4-166">ワールド全体</span><span class="sxs-lookup"><span data-stu-id="d57d4-166">Entire world</span></span>  <br/> |
|<span data-ttu-id="d57d4-167">バイナリ比較 (memcmp と同様)</span><span class="sxs-lookup"><span data-stu-id="d57d4-167">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="d57d4-168">[IMAPISupport:: CompareEntryIDs を使用しない](imapisupport-compareentryids.md)</span><span class="sxs-lookup"><span data-stu-id="d57d4-168">No use [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md)</span></span> <br/> |<span data-ttu-id="d57d4-169">はい</span><span class="sxs-lookup"><span data-stu-id="d57d4-169">Yes</span></span>  <br/> |<span data-ttu-id="d57d4-170">はい</span><span class="sxs-lookup"><span data-stu-id="d57d4-170">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="d57d4-171">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d57d4-171">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d57d4-172">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="d57d4-172">Protocol specifications</span></span>

<span data-ttu-id="d57d4-173">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d57d4-173">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d57d4-174">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="d57d4-174">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d57d4-175">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d57d4-175">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d57d4-176">メッセージ オブジェクトと添付ファイル オブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="d57d4-176">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="d57d4-177">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d57d4-177">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d57d4-178">ユーザー、連絡先、グループ、およびリソースの一覧のプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="d57d4-178">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="d57d4-179">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d57d4-179">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d57d4-180">インターネット標準の電子メール規則からメッセージ オブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="d57d4-180">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="d57d4-181">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d57d4-181">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d57d4-182">クライアントとサーバー間のデータ転送の順序とフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="d57d4-182">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="d57d4-183">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d57d4-183">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d57d4-184">サーバーに保存されているフォルダーのアクセス許可リストの取得を処理します。</span><span class="sxs-lookup"><span data-stu-id="d57d4-184">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
<span data-ttu-id="d57d4-185">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d57d4-185">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d57d4-186">メールボックスを代理人として接続および構成するためのメソッド、および他のユーザーの代理として動作するメッセージ オブジェクトと予定表オブジェクトとのやり取りを指定します。</span><span class="sxs-lookup"><span data-stu-id="d57d4-186">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="d57d4-187">[[MS-OXWAVLS]](https://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d57d4-187">[[MS-OXWAVLS]](https://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d57d4-188">ユーザーとリソースの可用性情報を要求するために使用するスキーマとメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="d57d4-188">Specifies the schema and methods that are used to request availability information for users and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d57d4-189">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="d57d4-189">Header files</span></span>

<span data-ttu-id="d57d4-190">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d57d4-190">Mapidefs.h</span></span>
  
> <span data-ttu-id="d57d4-191">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d57d4-191">Provides data type definitions.</span></span>
    
<span data-ttu-id="d57d4-192">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d57d4-192">Mapitags.h</span></span>
  
> <span data-ttu-id="d57d4-193">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="d57d4-193">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d57d4-194">関連項目</span><span class="sxs-lookup"><span data-stu-id="d57d4-194">See also</span></span>



[<span data-ttu-id="d57d4-195">PidTagStoreEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d57d4-195">PidTagStoreEntryId Canonical Property</span></span>](pidtagstoreentryid-canonical-property.md)


[<span data-ttu-id="d57d4-196">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="d57d4-196">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d57d4-197">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d57d4-197">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d57d4-198">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="d57d4-198">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d57d4-199">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="d57d4-199">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

