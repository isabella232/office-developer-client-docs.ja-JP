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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387791"
---
# <a name="pidtagentryid-canonical-property"></a><span data-ttu-id="aadc9-103">PidTagEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="aadc9-103">PidTagEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="aadc9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aadc9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aadc9-105">開き、特定の MAPI オブジェクトのプロパティを編集するに使用される MAPI エントリの識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="aadc9-105">Contains a MAPI entry identifier used to open and edit properties of a particular MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="aadc9-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="aadc9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="aadc9-107">PR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="aadc9-107">PR_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="aadc9-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="aadc9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="aadc9-109">0x0FFF</span><span class="sxs-lookup"><span data-stu-id="aadc9-109">0x0FFF</span></span>  <br/> |
|<span data-ttu-id="aadc9-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="aadc9-110">Data type:</span></span>  <br/> |<span data-ttu-id="aadc9-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="aadc9-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="aadc9-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="aadc9-112">Area:</span></span>  <br/> |<span data-ttu-id="aadc9-113">ID プロパティ</span><span class="sxs-lookup"><span data-stu-id="aadc9-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aadc9-114">備考</span><span class="sxs-lookup"><span data-stu-id="aadc9-114">Remarks</span></span>

<span data-ttu-id="aadc9-115">このプロパティは、 **OpenEntry**をインスタンス化するためにオブジェクトを識別し、すべての**IMAPIProp**の適切な派生インターフェイスからプロパティへのアクセスが用意されています。</span><span class="sxs-lookup"><span data-stu-id="aadc9-115">This property identifies an object for **OpenEntry** to instantiate and provides access to all of its properties through the appropriate derived interface of **IMAPIProp**.</span></span> 
  
<span data-ttu-id="aadc9-116">このプロパティは、すべてのメッセージング ユーザーのベース アドレスのプロパティのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="aadc9-116">This property is one of the base address properties for all messaging users.</span></span> 
  
<span data-ttu-id="aadc9-117">このプロパティは、長期的または短期的な識別子のいずれかを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="aadc9-117">This property can contain either a long-term or a short-term identifier.</span></span> <span data-ttu-id="aadc9-118">短期的な識別子は、簡単かつ迅速に、構造がの範囲と現在のセッションとワークステーションを通常の期間に制限されてです。</span><span class="sxs-lookup"><span data-stu-id="aadc9-118">Short-term identifiers are easier and faster to construct, but are limited in their scope and duration, typically to the current session and workstation.</span></span> <span data-ttu-id="aadc9-119">一般的にテーブルの行や、ダイアログ ボックスのエントリなどの一時的な性質のオブジェクトの使用はあり、放棄し。</span><span class="sxs-lookup"><span data-stu-id="aadc9-119">They are commonly used for objects of a temporary nature, such as table rows or dialog box entries, and then abandoned.</span></span> <span data-ttu-id="aadc9-120">広範な長期保存性の高いオブジェクトには、長期的な識別子が使用されます。</span><span class="sxs-lookup"><span data-stu-id="aadc9-120">Long-term identifiers are used for objects of a more wide-ranging and long-lasting nature.</span></span> 
  
<span data-ttu-id="aadc9-121">このプロパティは、常に[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドへの最初の呼び出しの後、 [IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="aadc9-121">This property is always available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="aadc9-122">一部のサービス プロバイダーを使用する利用可能なインスタンス化後すぐに。</span><span class="sxs-lookup"><span data-stu-id="aadc9-122">Some service providers can make it available immediately after instantiation.</span></span> <span data-ttu-id="aadc9-123">プロバイダーは、 **GetProps**から長期のエントリ id を常に返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="aadc9-123">The provider must always return a long-term entry identifier from **GetProps**.</span></span> <span data-ttu-id="aadc9-124">したがって、長期的な短期的な識別子に変換、単にオブジェクトを開くし、このプロパティを**GetProps**。</span><span class="sxs-lookup"><span data-stu-id="aadc9-124">Therefore, to convert a short-term identifier to long-term, simply open the object and get its this property through **GetProps**.</span></span> 
  
<span data-ttu-id="aadc9-125">次の表は、 **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) と**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))、このプロパティの間の重要な違いをまとめたものです。</span><span class="sxs-lookup"><span data-stu-id="aadc9-125">The following table summarizes important differences among this property, **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)).</span></span> 
  
|<span data-ttu-id="aadc9-126">**特性**</span><span class="sxs-lookup"><span data-stu-id="aadc9-126">**Characteristic**</span></span>|<span data-ttu-id="aadc9-127">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="aadc9-127">**PR_ENTRYID**</span></span>|<span data-ttu-id="aadc9-128">**PR_RECORD_KEY**</span><span class="sxs-lookup"><span data-stu-id="aadc9-128">**PR_RECORD_KEY**</span></span>|<span data-ttu-id="aadc9-129">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="aadc9-129">**PR_SEARCH_KEY**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="aadc9-130">添付ファイルのオブジェクトで必要な</span><span class="sxs-lookup"><span data-stu-id="aadc9-130">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="aadc9-131">いいえ</span><span class="sxs-lookup"><span data-stu-id="aadc9-131">No</span></span>  <br/> |<span data-ttu-id="aadc9-132">はい</span><span class="sxs-lookup"><span data-stu-id="aadc9-132">Yes</span></span>  <br/> |<span data-ttu-id="aadc9-133">いいえ</span><span class="sxs-lookup"><span data-stu-id="aadc9-133">No</span></span>  <br/> |
|<span data-ttu-id="aadc9-134">フォルダー オブジェクトで必要な</span><span class="sxs-lookup"><span data-stu-id="aadc9-134">Required on folder objects</span></span>  <br/> |<span data-ttu-id="aadc9-135">はい</span><span class="sxs-lookup"><span data-stu-id="aadc9-135">Yes</span></span>  <br/> |<span data-ttu-id="aadc9-136">はい</span><span class="sxs-lookup"><span data-stu-id="aadc9-136">Yes</span></span>  <br/> |<span data-ttu-id="aadc9-137">いいえ</span><span class="sxs-lookup"><span data-stu-id="aadc9-137">No</span></span>  <br/> |
|<span data-ttu-id="aadc9-138">メッセージ ストア オブジェクトで必要な</span><span class="sxs-lookup"><span data-stu-id="aadc9-138">Required on message store objects</span></span>  <br/> |<span data-ttu-id="aadc9-139">はい</span><span class="sxs-lookup"><span data-stu-id="aadc9-139">Yes</span></span>  <br/> |<span data-ttu-id="aadc9-140">はい</span><span class="sxs-lookup"><span data-stu-id="aadc9-140">Yes</span></span>  <br/> |<span data-ttu-id="aadc9-141">いいえ</span><span class="sxs-lookup"><span data-stu-id="aadc9-141">No</span></span>  <br/> |
|<span data-ttu-id="aadc9-142">状態オブジェクトで必要な</span><span class="sxs-lookup"><span data-stu-id="aadc9-142">Required on status objects</span></span>  <br/> |<span data-ttu-id="aadc9-143">はい</span><span class="sxs-lookup"><span data-stu-id="aadc9-143">Yes</span></span>  <br/> |<span data-ttu-id="aadc9-144">いいえ</span><span class="sxs-lookup"><span data-stu-id="aadc9-144">No</span></span>  <br/> |<span data-ttu-id="aadc9-145">いいえ</span><span class="sxs-lookup"><span data-stu-id="aadc9-145">No</span></span>  <br/> |
|<span data-ttu-id="aadc9-146">クライアントによって作成されました。</span><span class="sxs-lookup"><span data-stu-id="aadc9-146">Created by client</span></span>  <br/> |<span data-ttu-id="aadc9-147">いいえ</span><span class="sxs-lookup"><span data-stu-id="aadc9-147">No</span></span>  <br/> |<span data-ttu-id="aadc9-148">いいえ</span><span class="sxs-lookup"><span data-stu-id="aadc9-148">No</span></span>  <br/> |<span data-ttu-id="aadc9-149">はい</span><span class="sxs-lookup"><span data-stu-id="aadc9-149">Yes</span></span>  <br/> |
|<span data-ttu-id="aadc9-150">**Savechanges メソッド**の呼び出しの前に使用可能です</span><span class="sxs-lookup"><span data-stu-id="aadc9-150">Available before call to **SaveChanges**</span></span> <br/> |<span data-ttu-id="aadc9-151">プロバイダーの実装に依存します。</span><span class="sxs-lookup"><span data-stu-id="aadc9-151">Depends on provider implementation</span></span>  <br/> |<span data-ttu-id="aadc9-152">プロバイダーの実装に依存します。</span><span class="sxs-lookup"><span data-stu-id="aadc9-152">Depends on provider implementation</span></span>  <br/> |<span data-ttu-id="aadc9-153">メッセージは、[はい] です。</span><span class="sxs-lookup"><span data-stu-id="aadc9-153">For messages, Yes.</span></span> <span data-ttu-id="aadc9-154">他のユーザーには、プロバイダーの実装に依存します。</span><span class="sxs-lookup"><span data-stu-id="aadc9-154">For others, depends on provider implementation.</span></span>  <br/> |
|<span data-ttu-id="aadc9-155">コピー操作で変更</span><span class="sxs-lookup"><span data-stu-id="aadc9-155">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="aadc9-156">はい</span><span class="sxs-lookup"><span data-stu-id="aadc9-156">Yes</span></span>  <br/> |<span data-ttu-id="aadc9-157">はい</span><span class="sxs-lookup"><span data-stu-id="aadc9-157">Yes</span></span>  <br/> |<span data-ttu-id="aadc9-158">いいえ</span><span class="sxs-lookup"><span data-stu-id="aadc9-158">No</span></span>  <br/> |
|<span data-ttu-id="aadc9-159">コピー後にクライアントによって変更可能です</span><span class="sxs-lookup"><span data-stu-id="aadc9-159">Changeable by client after a copy</span></span>  <br/> |<span data-ttu-id="aadc9-160">いいえ</span><span class="sxs-lookup"><span data-stu-id="aadc9-160">No</span></span>  <br/> |<span data-ttu-id="aadc9-161">いいえ</span><span class="sxs-lookup"><span data-stu-id="aadc9-161">No</span></span>  <br/> |<span data-ttu-id="aadc9-162">はい</span><span class="sxs-lookup"><span data-stu-id="aadc9-162">Yes</span></span>  <br/> |
|<span data-ttu-id="aadc9-163">内で一意</span><span class="sxs-lookup"><span data-stu-id="aadc9-163">Unique within</span></span>  <br/> |<span data-ttu-id="aadc9-164">全体の世界</span><span class="sxs-lookup"><span data-stu-id="aadc9-164">Entire world</span></span>  <br/> |<span data-ttu-id="aadc9-165">プロバイダーのインスタンス</span><span class="sxs-lookup"><span data-stu-id="aadc9-165">Provider instance</span></span>  <br/> |<span data-ttu-id="aadc9-166">全体の世界</span><span class="sxs-lookup"><span data-stu-id="aadc9-166">Entire world</span></span>  <br/> |
|<span data-ttu-id="aadc9-167">バイナリ (ため) と同じように匹敵します。</span><span class="sxs-lookup"><span data-stu-id="aadc9-167">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="aadc9-168">使用しない[IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md)</span><span class="sxs-lookup"><span data-stu-id="aadc9-168">No use [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md)</span></span> <br/> |<span data-ttu-id="aadc9-169">はい</span><span class="sxs-lookup"><span data-stu-id="aadc9-169">Yes</span></span>  <br/> |<span data-ttu-id="aadc9-170">はい</span><span class="sxs-lookup"><span data-stu-id="aadc9-170">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="aadc9-171">関連リソース</span><span class="sxs-lookup"><span data-stu-id="aadc9-171">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="aadc9-172">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="aadc9-172">Protocol specifications</span></span>

<span data-ttu-id="aadc9-173">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aadc9-173">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aadc9-174">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="aadc9-174">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="aadc9-175">[[MS OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aadc9-175">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aadc9-176">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="aadc9-176">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="aadc9-177">[[MS OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aadc9-177">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aadc9-178">プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="aadc9-178">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="aadc9-179">[[MS OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aadc9-179">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aadc9-180">メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。</span><span class="sxs-lookup"><span data-stu-id="aadc9-180">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="aadc9-181">[[MS OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aadc9-181">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aadc9-182">順序と、クライアントとサーバー間のデータ転送のフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="aadc9-182">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="aadc9-183">[[MS OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aadc9-183">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aadc9-184">サーバーに格納されているフォルダーのアクセス許可の一覧の取得を処理します。</span><span class="sxs-lookup"><span data-stu-id="aadc9-184">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
<span data-ttu-id="aadc9-185">[[MS OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aadc9-185">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aadc9-186">接続し、別のユーザーに代わって動作する場合は、デリゲート、およびメッセージと予定表のオブジェクトとの対話としてメールボックスを構成するためのメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="aadc9-186">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="aadc9-187">[[MS OXWAVLS]](https://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aadc9-187">[[MS-OXWAVLS]](https://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aadc9-188">スキーマとユーザーとリソースの利用可能時間情報を要求するために使用するメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="aadc9-188">Specifies the schema and methods that are used to request availability information for users and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="aadc9-189">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="aadc9-189">Header files</span></span>

<span data-ttu-id="aadc9-190">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="aadc9-190">Mapidefs.h</span></span>
  
> <span data-ttu-id="aadc9-191">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="aadc9-191">Provides data type definitions.</span></span>
    
<span data-ttu-id="aadc9-192">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="aadc9-192">Mapitags.h</span></span>
  
> <span data-ttu-id="aadc9-193">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="aadc9-193">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aadc9-194">関連項目</span><span class="sxs-lookup"><span data-stu-id="aadc9-194">See also</span></span>



[<span data-ttu-id="aadc9-195">PidTagStoreEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="aadc9-195">PidTagStoreEntryId Canonical Property</span></span>](pidtagstoreentryid-canonical-property.md)


[<span data-ttu-id="aadc9-196">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="aadc9-196">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="aadc9-197">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="aadc9-197">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="aadc9-198">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="aadc9-198">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="aadc9-199">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="aadc9-199">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

