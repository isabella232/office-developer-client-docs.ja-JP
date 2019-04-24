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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: feb34cdbf8ba917936c3272bcaaf6eff040ddc3a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328589"
---
# <a name="pidtagentryid-canonical-property"></a><span data-ttu-id="8bb64-103">PidTagEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8bb64-103">PidTagEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="8bb64-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8bb64-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8bb64-105">特定の mapi オブジェクトのプロパティを開いて編集するために使用する mapi エントリ識別子を含みます。</span><span class="sxs-lookup"><span data-stu-id="8bb64-105">Contains a MAPI entry identifier used to open and edit properties of a particular MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8bb64-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="8bb64-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8bb64-107">PR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="8bb64-107">PR_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="8bb64-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="8bb64-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8bb64-109">0x0FFF</span><span class="sxs-lookup"><span data-stu-id="8bb64-109">0x0FFF</span></span>  <br/> |
|<span data-ttu-id="8bb64-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="8bb64-110">Data type:</span></span>  <br/> |<span data-ttu-id="8bb64-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8bb64-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8bb64-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="8bb64-112">Area:</span></span>  <br/> |<span data-ttu-id="8bb64-113">ID プロパティ</span><span class="sxs-lookup"><span data-stu-id="8bb64-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8bb64-114">解説</span><span class="sxs-lookup"><span data-stu-id="8bb64-114">Remarks</span></span>

<span data-ttu-id="8bb64-115">このプロパティは、インスタンス化する**openentry**のオブジェクトを識別し、 **imapiprop**の適切な派生インターフェイスを使用して、そのすべてのプロパティにアクセスできるようにします。</span><span class="sxs-lookup"><span data-stu-id="8bb64-115">This property identifies an object for **OpenEntry** to instantiate and provides access to all of its properties through the appropriate derived interface of **IMAPIProp**.</span></span> 
  
<span data-ttu-id="8bb64-116">このプロパティは、すべてのメッセージングユーザーのベースアドレスプロパティの1つです。</span><span class="sxs-lookup"><span data-stu-id="8bb64-116">This property is one of the base address properties for all messaging users.</span></span> 
  
<span data-ttu-id="8bb64-117">このプロパティには、長期間または短期識別子のいずれかを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="8bb64-117">This property can contain either a long-term or a short-term identifier.</span></span> <span data-ttu-id="8bb64-118">短時間の識別子は簡単に作成できますが、そのスコープと期間は、通常現在のセッションとワークステーションに制限されます。</span><span class="sxs-lookup"><span data-stu-id="8bb64-118">Short-term identifiers are easier and faster to construct, but are limited in their scope and duration, typically to the current session and workstation.</span></span> <span data-ttu-id="8bb64-119">これらのオブジェクトは、テーブルの行やダイアログボックスのエントリなど、一時的な性質を持つオブジェクトでよく使用され、破棄されます。</span><span class="sxs-lookup"><span data-stu-id="8bb64-119">They are commonly used for objects of a temporary nature, such as table rows or dialog box entries, and then abandoned.</span></span> <span data-ttu-id="8bb64-120">長期間の識別子は、より広範囲で長期的な性質を持つオブジェクトに使用されます。</span><span class="sxs-lookup"><span data-stu-id="8bb64-120">Long-term identifiers are used for objects of a more wide-ranging and long-lasting nature.</span></span> 
  
<span data-ttu-id="8bb64-121">このプロパティは、imapiprop [:: SaveChanges](imapiprop-savechanges.md)メソッドを最初に呼び出した後、 [imapiprop:: GetProps](imapiprop-getprops.md)メソッドを使用して常に使用できます。</span><span class="sxs-lookup"><span data-stu-id="8bb64-121">This property is always available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="8bb64-122">一部のサービスプロバイダーは、インスタンス化後すぐに使用できるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="8bb64-122">Some service providers can make it available immediately after instantiation.</span></span> <span data-ttu-id="8bb64-123">プロバイダーは常に、 **GetProps**から長期のエントリ id を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="8bb64-123">The provider must always return a long-term entry identifier from **GetProps**.</span></span> <span data-ttu-id="8bb64-124">そのため、短い用語識別子を長期に変換するには、単にオブジェクトを開き、 **GetProps**を使用してこのプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="8bb64-124">Therefore, to convert a short-term identifier to long-term, simply open the object and get its this property through **GetProps**.</span></span> 
  
<span data-ttu-id="8bb64-125">次の表は、このプロパティ、 **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))、および**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) の重要な相違点をまとめたものです。</span><span class="sxs-lookup"><span data-stu-id="8bb64-125">The following table summarizes important differences among this property, **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)).</span></span> 
  
|<span data-ttu-id="8bb64-126">**特性**</span><span class="sxs-lookup"><span data-stu-id="8bb64-126">**Characteristic**</span></span>|<span data-ttu-id="8bb64-127">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="8bb64-127">**PR_ENTRYID**</span></span>|<span data-ttu-id="8bb64-128">**PR_RECORD_KEY**</span><span class="sxs-lookup"><span data-stu-id="8bb64-128">**PR_RECORD_KEY**</span></span>|<span data-ttu-id="8bb64-129">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="8bb64-129">**PR_SEARCH_KEY**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8bb64-130">attachment オブジェクトに必要</span><span class="sxs-lookup"><span data-stu-id="8bb64-130">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="8bb64-131">いいえ</span><span class="sxs-lookup"><span data-stu-id="8bb64-131">No</span></span>  <br/> |<span data-ttu-id="8bb64-132">はい</span><span class="sxs-lookup"><span data-stu-id="8bb64-132">Yes</span></span>  <br/> |<span data-ttu-id="8bb64-133">いいえ</span><span class="sxs-lookup"><span data-stu-id="8bb64-133">No</span></span>  <br/> |
|<span data-ttu-id="8bb64-134">folder オブジェクトで必要</span><span class="sxs-lookup"><span data-stu-id="8bb64-134">Required on folder objects</span></span>  <br/> |<span data-ttu-id="8bb64-135">はい</span><span class="sxs-lookup"><span data-stu-id="8bb64-135">Yes</span></span>  <br/> |<span data-ttu-id="8bb64-136">はい</span><span class="sxs-lookup"><span data-stu-id="8bb64-136">Yes</span></span>  <br/> |<span data-ttu-id="8bb64-137">いいえ</span><span class="sxs-lookup"><span data-stu-id="8bb64-137">No</span></span>  <br/> |
|<span data-ttu-id="8bb64-138">メッセージストアオブジェクトに必要</span><span class="sxs-lookup"><span data-stu-id="8bb64-138">Required on message store objects</span></span>  <br/> |<span data-ttu-id="8bb64-139">はい</span><span class="sxs-lookup"><span data-stu-id="8bb64-139">Yes</span></span>  <br/> |<span data-ttu-id="8bb64-140">はい</span><span class="sxs-lookup"><span data-stu-id="8bb64-140">Yes</span></span>  <br/> |<span data-ttu-id="8bb64-141">いいえ</span><span class="sxs-lookup"><span data-stu-id="8bb64-141">No</span></span>  <br/> |
|<span data-ttu-id="8bb64-142">状態オブジェクトに必要です</span><span class="sxs-lookup"><span data-stu-id="8bb64-142">Required on status objects</span></span>  <br/> |<span data-ttu-id="8bb64-143">はい</span><span class="sxs-lookup"><span data-stu-id="8bb64-143">Yes</span></span>  <br/> |<span data-ttu-id="8bb64-144">いいえ</span><span class="sxs-lookup"><span data-stu-id="8bb64-144">No</span></span>  <br/> |<span data-ttu-id="8bb64-145">いいえ</span><span class="sxs-lookup"><span data-stu-id="8bb64-145">No</span></span>  <br/> |
|<span data-ttu-id="8bb64-146">クライアントによって作成</span><span class="sxs-lookup"><span data-stu-id="8bb64-146">Created by client</span></span>  <br/> |<span data-ttu-id="8bb64-147">いいえ</span><span class="sxs-lookup"><span data-stu-id="8bb64-147">No</span></span>  <br/> |<span data-ttu-id="8bb64-148">いいえ</span><span class="sxs-lookup"><span data-stu-id="8bb64-148">No</span></span>  <br/> |<span data-ttu-id="8bb64-149">はい</span><span class="sxs-lookup"><span data-stu-id="8bb64-149">Yes</span></span>  <br/> |
|<span data-ttu-id="8bb64-150">**SaveChanges**の呼び出し前に使用できます。</span><span class="sxs-lookup"><span data-stu-id="8bb64-150">Available before call to **SaveChanges**</span></span> <br/> |<span data-ttu-id="8bb64-151">プロバイダーの実装によって異なります。</span><span class="sxs-lookup"><span data-stu-id="8bb64-151">Depends on provider implementation</span></span>  <br/> |<span data-ttu-id="8bb64-152">プロバイダーの実装によって異なります。</span><span class="sxs-lookup"><span data-stu-id="8bb64-152">Depends on provider implementation</span></span>  <br/> |<span data-ttu-id="8bb64-153">メッセージの場合は、はい。</span><span class="sxs-lookup"><span data-stu-id="8bb64-153">For messages, Yes.</span></span> <span data-ttu-id="8bb64-154">その他の場合は、プロバイダーの実装によって異なります。</span><span class="sxs-lookup"><span data-stu-id="8bb64-154">For others, depends on provider implementation.</span></span>  <br/> |
|<span data-ttu-id="8bb64-155">コピー操作で変更</span><span class="sxs-lookup"><span data-stu-id="8bb64-155">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="8bb64-156">はい</span><span class="sxs-lookup"><span data-stu-id="8bb64-156">Yes</span></span>  <br/> |<span data-ttu-id="8bb64-157">はい</span><span class="sxs-lookup"><span data-stu-id="8bb64-157">Yes</span></span>  <br/> |<span data-ttu-id="8bb64-158">いいえ</span><span class="sxs-lookup"><span data-stu-id="8bb64-158">No</span></span>  <br/> |
|<span data-ttu-id="8bb64-159">コピー後にクライアントによって変更可能</span><span class="sxs-lookup"><span data-stu-id="8bb64-159">Changeable by client after a copy</span></span>  <br/> |<span data-ttu-id="8bb64-160">いいえ</span><span class="sxs-lookup"><span data-stu-id="8bb64-160">No</span></span>  <br/> |<span data-ttu-id="8bb64-161">いいえ</span><span class="sxs-lookup"><span data-stu-id="8bb64-161">No</span></span>  <br/> |<span data-ttu-id="8bb64-162">はい</span><span class="sxs-lookup"><span data-stu-id="8bb64-162">Yes</span></span>  <br/> |
|<span data-ttu-id="8bb64-163">内で一意</span><span class="sxs-lookup"><span data-stu-id="8bb64-163">Unique within</span></span>  <br/> |<span data-ttu-id="8bb64-164">世界全体</span><span class="sxs-lookup"><span data-stu-id="8bb64-164">Entire world</span></span>  <br/> |<span data-ttu-id="8bb64-165">プロバイダーインスタンス</span><span class="sxs-lookup"><span data-stu-id="8bb64-165">Provider instance</span></span>  <br/> |<span data-ttu-id="8bb64-166">世界全体</span><span class="sxs-lookup"><span data-stu-id="8bb64-166">Entire world</span></span>  <br/> |
|<span data-ttu-id="8bb64-167">二項比較 (memcmp と同じ)</span><span class="sxs-lookup"><span data-stu-id="8bb64-167">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="8bb64-168">使用しない[imapisupport:: compareentryids](imapisupport-compareentryids.md)</span><span class="sxs-lookup"><span data-stu-id="8bb64-168">No use [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md)</span></span> <br/> |<span data-ttu-id="8bb64-169">はい</span><span class="sxs-lookup"><span data-stu-id="8bb64-169">Yes</span></span>  <br/> |<span data-ttu-id="8bb64-170">はい</span><span class="sxs-lookup"><span data-stu-id="8bb64-170">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="8bb64-171">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8bb64-171">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8bb64-172">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="8bb64-172">Protocol specifications</span></span>

<span data-ttu-id="8bb64-173">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8bb64-173">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8bb64-174">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="8bb64-174">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8bb64-175">[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8bb64-175">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8bb64-176">メッセージと添付ファイルオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="8bb64-176">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="8bb64-177">[[OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8bb64-177">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8bb64-178">ユーザー、連絡先、グループ、およびリソースのリストのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="8bb64-178">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="8bb64-179">[[OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8bb64-179">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8bb64-180">インターネット標準の電子メールの規則からメッセージオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="8bb64-180">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="8bb64-181">[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8bb64-181">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8bb64-182">クライアントとサーバー間のデータ転送の順序と流れを処理します。</span><span class="sxs-lookup"><span data-stu-id="8bb64-182">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="8bb64-183">[[OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8bb64-183">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8bb64-184">サーバーに格納されているフォルダーのアクセス許可リストの取得を処理します。</span><span class="sxs-lookup"><span data-stu-id="8bb64-184">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
<span data-ttu-id="8bb64-185">[[OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8bb64-185">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8bb64-186">代理人としてメールボックスに接続して構成するためのメソッド、および別のユーザーの代理として実行されたときに、メッセージおよび予定表オブジェクトとの相互作用を指定します。</span><span class="sxs-lookup"><span data-stu-id="8bb64-186">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="8bb64-187">[[OXWAVLS]](https://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8bb64-187">[[MS-OXWAVLS]](https://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8bb64-188">ユーザーとリソースの空き時間情報を要求するために使用するスキーマとメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="8bb64-188">Specifies the schema and methods that are used to request availability information for users and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8bb64-189">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="8bb64-189">Header files</span></span>

<span data-ttu-id="8bb64-190">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8bb64-190">Mapidefs.h</span></span>
  
> <span data-ttu-id="8bb64-191">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8bb64-191">Provides data type definitions.</span></span>
    
<span data-ttu-id="8bb64-192">Mapitags</span><span class="sxs-lookup"><span data-stu-id="8bb64-192">Mapitags.h</span></span>
  
> <span data-ttu-id="8bb64-193">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8bb64-193">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8bb64-194">関連項目</span><span class="sxs-lookup"><span data-stu-id="8bb64-194">See also</span></span>



[<span data-ttu-id="8bb64-195">PidTagStoreEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8bb64-195">PidTagStoreEntryId Canonical Property</span></span>](pidtagstoreentryid-canonical-property.md)


[<span data-ttu-id="8bb64-196">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="8bb64-196">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8bb64-197">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8bb64-197">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8bb64-198">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8bb64-198">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8bb64-199">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8bb64-199">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

