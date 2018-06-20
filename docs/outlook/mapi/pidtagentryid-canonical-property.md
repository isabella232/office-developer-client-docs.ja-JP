---
title: PidTagEntryId の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 971462b9e85878677b57ec7b53fe46aa64db6dba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802744"
---
# <a name="pidtagentryid-canonical-property"></a><span data-ttu-id="5497e-103">PidTagEntryId の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="5497e-103">PidTagEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="5497e-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5497e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5497e-105">開き、特定の MAPI オブジェクトのプロパティを編集するに使用される MAPI エントリの識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5497e-105">Contains a MAPI entry identifier used to open and edit properties of a particular MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5497e-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="5497e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5497e-107">PR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="5497e-107">PR_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="5497e-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="5497e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5497e-109">0x0FFF</span><span class="sxs-lookup"><span data-stu-id="5497e-109">0x0FFF</span></span>  <br/> |
|<span data-ttu-id="5497e-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="5497e-110">Data type:</span></span>  <br/> |<span data-ttu-id="5497e-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5497e-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5497e-112">領域:</span><span class="sxs-lookup"><span data-stu-id="5497e-112">Area:</span></span>  <br/> |<span data-ttu-id="5497e-113">ID プロパティ</span><span class="sxs-lookup"><span data-stu-id="5497e-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5497e-114">備考</span><span class="sxs-lookup"><span data-stu-id="5497e-114">Remarks</span></span>

<span data-ttu-id="5497e-115">このプロパティは、 **OpenEntry**をインスタンス化するためにオブジェクトを識別し、すべての**IMAPIProp**の適切な派生インターフェイスからプロパティへのアクセスが用意されています。</span><span class="sxs-lookup"><span data-stu-id="5497e-115">This property identifies an object for **OpenEntry** to instantiate and provides access to all of its properties through the appropriate derived interface of **IMAPIProp**.</span></span> 
  
<span data-ttu-id="5497e-116">このプロパティは、すべてのメッセージング ユーザーのベース アドレスのプロパティのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="5497e-116">This property is one of the base address properties for all messaging users.</span></span> 
  
<span data-ttu-id="5497e-117">このプロパティは、長期的または短期的な識別子のいずれかを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="5497e-117">This property can contain either a long-term or a short-term identifier.</span></span> <span data-ttu-id="5497e-118">短期的な識別子は、簡単かつ迅速に、構造がの範囲と現在のセッションとワークステーションを通常の期間に制限されてです。</span><span class="sxs-lookup"><span data-stu-id="5497e-118">Short-term identifiers are easier and faster to construct, but are limited in their scope and duration, typically to the current session and workstation.</span></span> <span data-ttu-id="5497e-119">一般的にテーブルの行や、ダイアログ ボックスのエントリなどの一時的な性質のオブジェクトの使用はあり、放棄し。</span><span class="sxs-lookup"><span data-stu-id="5497e-119">They are commonly used for objects of a temporary nature, such as table rows or dialog box entries, and then abandoned.</span></span> <span data-ttu-id="5497e-120">広範な長期保存性の高いオブジェクトには、長期的な識別子が使用されます。</span><span class="sxs-lookup"><span data-stu-id="5497e-120">Long-term identifiers are used for objects of a more wide-ranging and long-lasting nature.</span></span> 
  
<span data-ttu-id="5497e-121">このプロパティは、常に[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドへの最初の呼び出しの後、 [IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="5497e-121">This property is always available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="5497e-122">一部のサービス プロバイダーを使用する利用可能なインスタンス化後すぐに。</span><span class="sxs-lookup"><span data-stu-id="5497e-122">Some service providers can make it available immediately after instantiation.</span></span> <span data-ttu-id="5497e-123">プロバイダーは、 **GetProps**から長期のエントリ id を常に返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="5497e-123">The provider must always return a long-term entry identifier from **GetProps**.</span></span> <span data-ttu-id="5497e-124">したがって、長期的な短期的な識別子に変換、単にオブジェクトを開くし、このプロパティを**GetProps**。</span><span class="sxs-lookup"><span data-stu-id="5497e-124">Therefore, to convert a short-term identifier to long-term, simply open the object and get its this property through **GetProps**.</span></span> 
  
<span data-ttu-id="5497e-125">次の表は、 **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) と**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))、このプロパティの間の重要な違いをまとめたものです。</span><span class="sxs-lookup"><span data-stu-id="5497e-125">The following table summarizes important differences among this property, **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)).</span></span> 
  
|<span data-ttu-id="5497e-126">**特性**</span><span class="sxs-lookup"><span data-stu-id="5497e-126">**Characteristic**</span></span>|<span data-ttu-id="5497e-127">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="5497e-127">**PR_ENTRYID**</span></span>|<span data-ttu-id="5497e-128">**PR_RECORD_KEY**</span><span class="sxs-lookup"><span data-stu-id="5497e-128">**PR_RECORD_KEY**</span></span>|<span data-ttu-id="5497e-129">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="5497e-129">**PR_SEARCH_KEY**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5497e-130">添付ファイルのオブジェクトで必要な</span><span class="sxs-lookup"><span data-stu-id="5497e-130">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="5497e-131">いいえ</span><span class="sxs-lookup"><span data-stu-id="5497e-131">No</span></span>  <br/> |<span data-ttu-id="5497e-132">はい</span><span class="sxs-lookup"><span data-stu-id="5497e-132">Yes</span></span>  <br/> |<span data-ttu-id="5497e-133">いいえ</span><span class="sxs-lookup"><span data-stu-id="5497e-133">No</span></span>  <br/> |
|<span data-ttu-id="5497e-134">フォルダー オブジェクトで必要な</span><span class="sxs-lookup"><span data-stu-id="5497e-134">Required on folder objects</span></span>  <br/> |<span data-ttu-id="5497e-135">はい</span><span class="sxs-lookup"><span data-stu-id="5497e-135">Yes</span></span>  <br/> |<span data-ttu-id="5497e-136">はい</span><span class="sxs-lookup"><span data-stu-id="5497e-136">Yes</span></span>  <br/> |<span data-ttu-id="5497e-137">いいえ</span><span class="sxs-lookup"><span data-stu-id="5497e-137">No</span></span>  <br/> |
|<span data-ttu-id="5497e-138">メッセージ ストア オブジェクトで必要な</span><span class="sxs-lookup"><span data-stu-id="5497e-138">Required on message store objects</span></span>  <br/> |<span data-ttu-id="5497e-139">はい</span><span class="sxs-lookup"><span data-stu-id="5497e-139">Yes</span></span>  <br/> |<span data-ttu-id="5497e-140">はい</span><span class="sxs-lookup"><span data-stu-id="5497e-140">Yes</span></span>  <br/> |<span data-ttu-id="5497e-141">いいえ</span><span class="sxs-lookup"><span data-stu-id="5497e-141">No</span></span>  <br/> |
|<span data-ttu-id="5497e-142">状態オブジェクトで必要な</span><span class="sxs-lookup"><span data-stu-id="5497e-142">Required on status objects</span></span>  <br/> |<span data-ttu-id="5497e-143">はい</span><span class="sxs-lookup"><span data-stu-id="5497e-143">Yes</span></span>  <br/> |<span data-ttu-id="5497e-144">いいえ</span><span class="sxs-lookup"><span data-stu-id="5497e-144">No</span></span>  <br/> |<span data-ttu-id="5497e-145">いいえ</span><span class="sxs-lookup"><span data-stu-id="5497e-145">No</span></span>  <br/> |
|<span data-ttu-id="5497e-146">クライアントによって作成されました。</span><span class="sxs-lookup"><span data-stu-id="5497e-146">Created by client</span></span>  <br/> |<span data-ttu-id="5497e-147">いいえ</span><span class="sxs-lookup"><span data-stu-id="5497e-147">No</span></span>  <br/> |<span data-ttu-id="5497e-148">いいえ</span><span class="sxs-lookup"><span data-stu-id="5497e-148">No</span></span>  <br/> |<span data-ttu-id="5497e-149">はい</span><span class="sxs-lookup"><span data-stu-id="5497e-149">Yes</span></span>  <br/> |
|<span data-ttu-id="5497e-150">**Savechanges メソッド**の呼び出しの前に使用可能です</span><span class="sxs-lookup"><span data-stu-id="5497e-150">Available before call to **SaveChanges**</span></span> <br/> |<span data-ttu-id="5497e-151">プロバイダーの実装に依存します。</span><span class="sxs-lookup"><span data-stu-id="5497e-151">Depends on provider implementation</span></span>  <br/> |<span data-ttu-id="5497e-152">プロバイダーの実装に依存します。</span><span class="sxs-lookup"><span data-stu-id="5497e-152">Depends on provider implementation</span></span>  <br/> |<span data-ttu-id="5497e-153">メッセージは、[はい] です。</span><span class="sxs-lookup"><span data-stu-id="5497e-153">For messages, Yes.</span></span> <span data-ttu-id="5497e-154">他のユーザーには、プロバイダーの実装に依存します。</span><span class="sxs-lookup"><span data-stu-id="5497e-154">For others, depends on provider implementation.</span></span>  <br/> |
|<span data-ttu-id="5497e-155">コピー操作で変更</span><span class="sxs-lookup"><span data-stu-id="5497e-155">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="5497e-156">はい</span><span class="sxs-lookup"><span data-stu-id="5497e-156">Yes</span></span>  <br/> |<span data-ttu-id="5497e-157">はい</span><span class="sxs-lookup"><span data-stu-id="5497e-157">Yes</span></span>  <br/> |<span data-ttu-id="5497e-158">いいえ</span><span class="sxs-lookup"><span data-stu-id="5497e-158">No</span></span>  <br/> |
|<span data-ttu-id="5497e-159">コピー後にクライアントによって変更可能です</span><span class="sxs-lookup"><span data-stu-id="5497e-159">Changeable by client after a copy</span></span>  <br/> |<span data-ttu-id="5497e-160">いいえ</span><span class="sxs-lookup"><span data-stu-id="5497e-160">No</span></span>  <br/> |<span data-ttu-id="5497e-161">いいえ</span><span class="sxs-lookup"><span data-stu-id="5497e-161">No</span></span>  <br/> |<span data-ttu-id="5497e-162">はい</span><span class="sxs-lookup"><span data-stu-id="5497e-162">Yes</span></span>  <br/> |
|<span data-ttu-id="5497e-163">内で一意</span><span class="sxs-lookup"><span data-stu-id="5497e-163">Unique within</span></span>  <br/> |<span data-ttu-id="5497e-164">全体の世界</span><span class="sxs-lookup"><span data-stu-id="5497e-164">Entire world</span></span>  <br/> |<span data-ttu-id="5497e-165">プロバイダーのインスタンス</span><span class="sxs-lookup"><span data-stu-id="5497e-165">Provider instance</span></span>  <br/> |<span data-ttu-id="5497e-166">全体の世界</span><span class="sxs-lookup"><span data-stu-id="5497e-166">Entire world</span></span>  <br/> |
|<span data-ttu-id="5497e-167">バイナリ (ため) と同じように匹敵します。</span><span class="sxs-lookup"><span data-stu-id="5497e-167">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="5497e-168">使用しない[IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md)</span><span class="sxs-lookup"><span data-stu-id="5497e-168">No use [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md)</span></span> <br/> |<span data-ttu-id="5497e-169">はい</span><span class="sxs-lookup"><span data-stu-id="5497e-169">Yes</span></span>  <br/> |<span data-ttu-id="5497e-170">はい</span><span class="sxs-lookup"><span data-stu-id="5497e-170">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="5497e-171">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5497e-171">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5497e-172">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="5497e-172">Protocol specifications</span></span>

<span data-ttu-id="5497e-173">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5497e-173">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5497e-174">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="5497e-174">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5497e-175">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5497e-175">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5497e-176">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="5497e-176">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="5497e-177">[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5497e-177">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5497e-178">プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="5497e-178">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="5497e-179">[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5497e-179">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5497e-180">メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。</span><span class="sxs-lookup"><span data-stu-id="5497e-180">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="5497e-181">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5497e-181">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5497e-182">順序と、クライアントとサーバー間のデータ転送のフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="5497e-182">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="5497e-183">[[MS OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5497e-183">[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5497e-184">サーバーに格納されているフォルダーのアクセス許可の一覧の取得を処理します。</span><span class="sxs-lookup"><span data-stu-id="5497e-184">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
<span data-ttu-id="5497e-185">[[MS OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5497e-185">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5497e-186">接続し、別のユーザーに代わって動作する場合は、デリゲート、およびメッセージと予定表のオブジェクトとの対話としてメールボックスを構成するためのメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="5497e-186">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="5497e-187">[[MS OXWAVLS]](http://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5497e-187">[[MS-OXWAVLS]](http://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5497e-188">スキーマとユーザーとリソースの利用可能時間情報を要求するために使用するメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="5497e-188">Specifies the schema and methods that are used to request availability information for users and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5497e-189">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="5497e-189">Header files</span></span>

<span data-ttu-id="5497e-190">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5497e-190">Mapidefs.h</span></span>
  
> <span data-ttu-id="5497e-191">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5497e-191">Provides data type definitions.</span></span>
    
<span data-ttu-id="5497e-192">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5497e-192">Mapitags.h</span></span>
  
> <span data-ttu-id="5497e-193">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5497e-193">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5497e-194">関連項目</span><span class="sxs-lookup"><span data-stu-id="5497e-194">See also</span></span>



[<span data-ttu-id="5497e-195">PidTagStoreEntryId の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="5497e-195">PidTagStoreEntryId Canonical Property</span></span>](pidtagstoreentryid-canonical-property.md)


[<span data-ttu-id="5497e-196">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5497e-196">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5497e-197">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5497e-197">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5497e-198">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="5497e-198">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5497e-199">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="5497e-199">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

