---
title: PidTagResourceFlags の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourceFlags
api_type:
- COM
ms.assetid: 69be9ad3-006a-459e-9cd4-eb3f609d71ad
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: dae917b3e536aee5f24879edc3ccf0736e7c9f34
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803353"
---
# <a name="pidtagresourceflags-canonical-property"></a><span data-ttu-id="ddacd-103">PidTagResourceFlags の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="ddacd-103">PidTagResourceFlags Canonical Property</span></span>

  
  
<span data-ttu-id="ddacd-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ddacd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ddacd-105">メッセージ サービスおよびプロバイダーのフラグのビットマスクを格納します。</span><span class="sxs-lookup"><span data-stu-id="ddacd-105">Contains a bitmask of flags for message services and providers.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ddacd-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="ddacd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ddacd-107">PR_RESOURCE_FLAGS</span><span class="sxs-lookup"><span data-stu-id="ddacd-107">PR_RESOURCE_FLAGS</span></span>  <br/> |
|<span data-ttu-id="ddacd-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="ddacd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ddacd-109">0x3009</span><span class="sxs-lookup"><span data-stu-id="ddacd-109">0x3009</span></span>  <br/> |
|<span data-ttu-id="ddacd-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="ddacd-110">Data type:</span></span>  <br/> |<span data-ttu-id="ddacd-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ddacd-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ddacd-112">領域:</span><span class="sxs-lookup"><span data-stu-id="ddacd-112">Area:</span></span>  <br/> |<span data-ttu-id="ddacd-113">一般的な MAPI</span><span class="sxs-lookup"><span data-stu-id="ddacd-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ddacd-114">備考</span><span class="sxs-lookup"><span data-stu-id="ddacd-114">Remarks</span></span>

<span data-ttu-id="ddacd-115">このプロパティでは、メッセージ サービス、サービス プロバイダー、または状態オブジェクトの特性について説明します。</span><span class="sxs-lookup"><span data-stu-id="ddacd-115">This property describes the characteristics of a message service, a service provider, or a status object.</span></span> <span data-ttu-id="ddacd-116">このプロパティに設定されているフラグは、そのコンテキストに依存します。</span><span class="sxs-lookup"><span data-stu-id="ddacd-116">The flags that are set for this property depend on its context.</span></span> <span data-ttu-id="ddacd-117">などのいくつかのフラグは、オブジェクトのステータスおよびその他のフラグをメッセージ サービス テーブルの列に対してのみに対してのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="ddacd-117">For example, some flags are valid only for status objects and other flags only for columns in the message service table.</span></span> 
  
<span data-ttu-id="ddacd-118">フラグは、3 つのクラス: 静的で、変更可能なおよび動的な。</span><span class="sxs-lookup"><span data-stu-id="ddacd-118">The flags are of three classes: static, modifiable, and dynamic.</span></span> <span data-ttu-id="ddacd-119">静的なフラグは、MAPISVC 内のデータから、MAPI によって設定されます。INF し、改ざんを防止します。</span><span class="sxs-lookup"><span data-stu-id="ddacd-119">Static flags are set by MAPI from data in MAPISVC.INF and never altered.</span></span> <span data-ttu-id="ddacd-120">MAPISVC から MAPI で変更可能なフラグが設定されています。INF が後で変更できます。</span><span class="sxs-lookup"><span data-stu-id="ddacd-120">Modifiable flags are set by MAPI from MAPISVC.INF but can be subsequently changed.</span></span> <span data-ttu-id="ddacd-121">動的フラグを設定し、MAPI の方法をリセットできます。</span><span class="sxs-lookup"><span data-stu-id="ddacd-121">Dynamic flags can be set and reset by MAPI methods.</span></span>
  
<span data-ttu-id="ddacd-122">メッセージ サービスは、次のフラグの 1 つ以上設定できますこのプロパティにします。</span><span class="sxs-lookup"><span data-stu-id="ddacd-122">For a message service, one or more of the following flags can be set in this property:</span></span>
  
<span data-ttu-id="ddacd-123">SERVICE_CREATE_WITH_STORE</span><span class="sxs-lookup"><span data-stu-id="ddacd-123">SERVICE_CREATE_WITH_STORE</span></span> 
  
> <span data-ttu-id="ddacd-124">予約済み。</span><span class="sxs-lookup"><span data-stu-id="ddacd-124">Reserved.</span></span> <span data-ttu-id="ddacd-125">使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="ddacd-125">Do not use.</span></span>
    
<span data-ttu-id="ddacd-126">SERVICE_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="ddacd-126">SERVICE_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="ddacd-127">動的です。</span><span class="sxs-lookup"><span data-stu-id="ddacd-127">Dynamic.</span></span> <span data-ttu-id="ddacd-128">メッセージ サービスには、既定のストアが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ddacd-128">The message service contains the default store.</span></span> <span data-ttu-id="ddacd-129">削除するか、プロファイルからこのサービスを移動する前に確認のプロンプトを表示、ユーザー インターフェイスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ddacd-129">A user interface should be displayed prompting the user for confirmation before deleting or moving this service out of the profile.</span></span> 
    
<span data-ttu-id="ddacd-130">SERVICE_NO_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="ddacd-130">SERVICE_NO_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="ddacd-131">静的です。</span><span class="sxs-lookup"><span data-stu-id="ddacd-131">Static.</span></span> <span data-ttu-id="ddacd-132">サービス レベルのフラグなしでメッセージ サービス プロバイダーの使用できることを id を指定するを示すために設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ddacd-132">The service level flag that should be set to indicate that none of the providers in the message service can be used to supply an identity.</span></span> <span data-ttu-id="ddacd-133">セットは、このフラグまたは SERVICE_PRIMARY_IDENTITY 必要があります。</span><span class="sxs-lookup"><span data-stu-id="ddacd-133">Either this flag or SERVICE_PRIMARY_IDENTITY should be set, but not both.</span></span>
    
<span data-ttu-id="ddacd-134">SERVICE_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="ddacd-134">SERVICE_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="ddacd-135">変更可能です。</span><span class="sxs-lookup"><span data-stu-id="ddacd-135">Modifiable.</span></span> <span data-ttu-id="ddacd-136">対応するメッセージ サービスには、このセッションのプライマリ id に使用されるプロバイダーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ddacd-136">The corresponding message service contains the provider used for the primary identity for this session.</span></span> <span data-ttu-id="ddacd-137">[IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md)を使用すると、このフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="ddacd-137">Use [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) to set this flag.</span></span> <span data-ttu-id="ddacd-138">セットは、このフラグまたは SERVICE_NO_PRIMARY_IDENTITY 必要があります。</span><span class="sxs-lookup"><span data-stu-id="ddacd-138">Either this flag or SERVICE_NO_PRIMARY_IDENTITY should be set, but not both.</span></span> 
    
<span data-ttu-id="ddacd-139">SERVICE_SINGLE_COPY</span><span class="sxs-lookup"><span data-stu-id="ddacd-139">SERVICE_SINGLE_COPY</span></span> 
  
> <span data-ttu-id="ddacd-140">静的です。</span><span class="sxs-lookup"><span data-stu-id="ddacd-140">Static.</span></span> <span data-ttu-id="ddacd-141">作成するか、このメッセージ サービスをサービスが既に存在するプロファイルにコピーしようが失敗します。</span><span class="sxs-lookup"><span data-stu-id="ddacd-141">Any attempt to create or copy this message service into a profile where the service already exists will fail.</span></span> <span data-ttu-id="ddacd-142">1 つのコピーを作成するのには、メッセージ サービスは、MAPISVC でのサービスのセクションに**PR_RESOURCE_FLAGS**プロパティを追加します。INF、このフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="ddacd-142">To create a single copy message service add the **PR_RESOURCE_FLAGS** property to the service's section in MAPISVC.INF and set this flag.</span></span> 
    
<span data-ttu-id="ddacd-143">サービス プロバイダーには、次のフラグの 1 つ以上設定できますで**PR_RESOURCE_FLAGS**。</span><span class="sxs-lookup"><span data-stu-id="ddacd-143">For a service provider, one or more of the following flags can be set in **PR_RESOURCE_FLAGS**:</span></span>
  
<span data-ttu-id="ddacd-144">HOOK_INBOUND</span><span class="sxs-lookup"><span data-stu-id="ddacd-144">HOOK_INBOUND</span></span> 
  
> <span data-ttu-id="ddacd-145">静的です。</span><span class="sxs-lookup"><span data-stu-id="ddacd-145">Static.</span></span> <span data-ttu-id="ddacd-146">スプーラーのフックは、受信メッセージを処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ddacd-146">The spooler hook needs to process inbound messages.</span></span>
    
<span data-ttu-id="ddacd-147">HOOK_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="ddacd-147">HOOK_OUTBOUND</span></span> 
  
> <span data-ttu-id="ddacd-148">静的です。</span><span class="sxs-lookup"><span data-stu-id="ddacd-148">Static.</span></span> <span data-ttu-id="ddacd-149">スプーラーのフックは、送信メッセージを処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ddacd-149">The spooler hook needs to process outbound messages.</span></span> 
    
<span data-ttu-id="ddacd-150">STATUS_DEFAULT_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="ddacd-150">STATUS_DEFAULT_OUTBOUND</span></span> 
  
> <span data-ttu-id="ddacd-151">変更可能です。</span><span class="sxs-lookup"><span data-stu-id="ddacd-151">Modifiable.</span></span> <span data-ttu-id="ddacd-152">プロファイルには、このトランスポート プロバイダーの複数のインスタンスが含まれている場合、この id を送信メッセージに適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ddacd-152">This identity should be applied to outbound messages if the profile contains multiple instances of this transport provider.</span></span> <span data-ttu-id="ddacd-153">これは、プロファイルに 1 つのトランスポート プロバイダーの複数のインスタンスが表示される場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="ddacd-153">This can happen if multiple instances of a single transport provider appear in the profile.</span></span>
    
<span data-ttu-id="ddacd-154">STATUS_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="ddacd-154">STATUS_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="ddacd-155">変更可能です。</span><span class="sxs-lookup"><span data-stu-id="ddacd-155">Modifiable.</span></span> <span data-ttu-id="ddacd-156">このメッセージ ・ ストアは、プロファイルの既定のストアです。</span><span class="sxs-lookup"><span data-stu-id="ddacd-156">This message store is the default store for the profile.</span></span> 
    
<span data-ttu-id="ddacd-157">STATUS_NEED_IPM_TREE</span><span class="sxs-lookup"><span data-stu-id="ddacd-157">STATUS_NEED_IPM_TREE</span></span> 
  
> <span data-ttu-id="ddacd-158">動的です。</span><span class="sxs-lookup"><span data-stu-id="ddacd-158">Dynamic.</span></span> <span data-ttu-id="ddacd-159">個人間メッセージ (IPM) のルート フォルダーを含めて、このメッセージ ストア内の標準のフォルダーは、まだ確認されていません。</span><span class="sxs-lookup"><span data-stu-id="ddacd-159">The standard folders in this message store, including the interpersonal message (IPM) root folder, have not yet been verified.</span></span> <span data-ttu-id="ddacd-160">MAPI では、設定し、このフラグをクリアします。</span><span class="sxs-lookup"><span data-stu-id="ddacd-160">MAPI sets and clears this flag.</span></span> 
    
<span data-ttu-id="ddacd-161">STATUS_NO_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="ddacd-161">STATUS_NO_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="ddacd-162">静的です。</span><span class="sxs-lookup"><span data-stu-id="ddacd-162">Static.</span></span> <span data-ttu-id="ddacd-163">このメッセージ ・ ストアは、プロファイルの既定のメッセージ ストアになることはありません。</span><span class="sxs-lookup"><span data-stu-id="ddacd-163">This message store is incapable of becoming the default message store for the profile.</span></span>
    
<span data-ttu-id="ddacd-164">STATUS_NO_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="ddacd-164">STATUS_NO_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="ddacd-165">静的です。</span><span class="sxs-lookup"><span data-stu-id="ddacd-165">Static.</span></span> <span data-ttu-id="ddacd-166">このプロバイダーは、その [状態] 行の id を提供していません。</span><span class="sxs-lookup"><span data-stu-id="ddacd-166">This provider does not furnish an identity in its status row.</span></span> <span data-ttu-id="ddacd-167">このフラグまたは STATUS_PRIMARY_IDENTITY のいずれかを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ddacd-167">Either this flag or STATUS_PRIMARY_IDENTITY must be set.</span></span>
    
<span data-ttu-id="ddacd-168">STATUS_OWN_STORE</span><span class="sxs-lookup"><span data-stu-id="ddacd-168">STATUS_OWN_STORE</span></span> 
  
> <span data-ttu-id="ddacd-169">静的です。</span><span class="sxs-lookup"><span data-stu-id="ddacd-169">Static.</span></span> <span data-ttu-id="ddacd-170">このトランスポート プロバイダーは、メッセージ ストアと密接に関連し、のステータス行に、 **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) のプロパティを提供します。</span><span class="sxs-lookup"><span data-stu-id="ddacd-170">This transport provider is tightly coupled with a message store and furnishes the **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) property in its status row.</span></span>
    
<span data-ttu-id="ddacd-171">STATUS_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="ddacd-171">STATUS_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="ddacd-172">変更可能です。</span><span class="sxs-lookup"><span data-stu-id="ddacd-172">Modifiable.</span></span> <span data-ttu-id="ddacd-173">このプロバイダーがセッションのプライマリ id を提供します。[IMAPISession::QueryIdentity](imapisession-queryidentity.md)から id を使用する際のオブジェクトのエントリ id が返されます。</span><span class="sxs-lookup"><span data-stu-id="ddacd-173">This provider furnishes the primary identity for the session; the entry identifier for the object furnishing the identity is returned from [IMAPISession::QueryIdentity](imapisession-queryidentity.md).</span></span> <span data-ttu-id="ddacd-174">このフラグまたは**STATUS_NO_PRIMARY_IDENTITY**のいずれかを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ddacd-174">Either this flag or **STATUS_NO_PRIMARY_IDENTITY** must be set.</span></span> 
    
<span data-ttu-id="ddacd-175">STATUS_PRIMARY_STORE</span><span class="sxs-lookup"><span data-stu-id="ddacd-175">STATUS_PRIMARY_STORE</span></span> 
  
> <span data-ttu-id="ddacd-176">変更可能です。</span><span class="sxs-lookup"><span data-stu-id="ddacd-176">Modifiable.</span></span> <span data-ttu-id="ddacd-177">このメッセージ ストアは、クライアント アプリケーションがログオンするときに使用します。</span><span class="sxs-lookup"><span data-stu-id="ddacd-177">This message store is to be used when a client application logs on.</span></span> <span data-ttu-id="ddacd-178">開くと、このストアは、プロファイルの既定のストアとして設定してください。</span><span class="sxs-lookup"><span data-stu-id="ddacd-178">Once opened, this store should be set as the default store for the profile.</span></span> 
    
<span data-ttu-id="ddacd-179">STATUS_SECONDARY_STORE</span><span class="sxs-lookup"><span data-stu-id="ddacd-179">STATUS_SECONDARY_STORE</span></span> 
  
> <span data-ttu-id="ddacd-180">変更可能です。</span><span class="sxs-lookup"><span data-stu-id="ddacd-180">Modifiable.</span></span> <span data-ttu-id="ddacd-181">このメッセージ ストアは、クライアント アプリケーションがログオンすると、プライマリ ストアが使用できない場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="ddacd-181">This message store is to be used if the primary store is not available when a client application logs on.</span></span> <span data-ttu-id="ddacd-182">開くと、このストアは、プロファイルの既定のストアとして設定してください。</span><span class="sxs-lookup"><span data-stu-id="ddacd-182">Once opened, this store should be set as the default store for the profile.</span></span> 
    
<span data-ttu-id="ddacd-183">STATUS_SIMPLE_STORE</span><span class="sxs-lookup"><span data-stu-id="ddacd-183">STATUS_SIMPLE_STORE</span></span> 
  
> <span data-ttu-id="ddacd-184">動的です。</span><span class="sxs-lookup"><span data-stu-id="ddacd-184">Dynamic.</span></span> <span data-ttu-id="ddacd-185">このメッセージ ・ ストアは、簡易 MAPI での既定のメッセージ ストアとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="ddacd-185">This message store will be used by Simple MAPI as its default message store.</span></span>
    
<span data-ttu-id="ddacd-186">STATUS_TEMP_SECTION</span><span class="sxs-lookup"><span data-stu-id="ddacd-186">STATUS_TEMP_SECTION</span></span> 
  
> <span data-ttu-id="ddacd-187">動的です。</span><span class="sxs-lookup"><span data-stu-id="ddacd-187">Dynamic.</span></span> <span data-ttu-id="ddacd-188">このメッセージ ・ ストアは、メッセージ ストアの表には公開しないようにし、ログオフ後、プロファイルから削除されます。</span><span class="sxs-lookup"><span data-stu-id="ddacd-188">This message store should not be published in the message store table and will be deleted from the profile after logoff.</span></span> 
    
<span data-ttu-id="ddacd-189">STATUS_XP_PREFER_LAST</span><span class="sxs-lookup"><span data-stu-id="ddacd-189">STATUS_XP_PREFER_LAST</span></span> 
  
> <span data-ttu-id="ddacd-190">静的です。</span><span class="sxs-lookup"><span data-stu-id="ddacd-190">Static.</span></span> <span data-ttu-id="ddacd-191">このトランスポートは、複数のトランスポート プロバイダーは、メッセージを送信できなかったときにメッセージを送信する選択されている最後のトランスポートを期待しています。</span><span class="sxs-lookup"><span data-stu-id="ddacd-191">This transport expects to be the last transport selected to send a message when multiple transport providers are able to transmit the message.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="ddacd-192">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ddacd-192">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ddacd-193">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="ddacd-193">Header files</span></span>

<span data-ttu-id="ddacd-194">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ddacd-194">Mapidefs.h</span></span>
  
> <span data-ttu-id="ddacd-195">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ddacd-195">Provides data type definitions.</span></span>
    
<span data-ttu-id="ddacd-196">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ddacd-196">Mapitags.h</span></span>
  
> <span data-ttu-id="ddacd-197">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ddacd-197">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ddacd-198">関連項目</span><span class="sxs-lookup"><span data-stu-id="ddacd-198">See also</span></span>



[<span data-ttu-id="ddacd-199">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="ddacd-199">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>](imsgserviceadmin-msgservicetransportorder.md)
  
[<span data-ttu-id="ddacd-200">PidTagIdentityEntryId の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="ddacd-200">PidTagIdentityEntryId Canonical Property</span></span>](pidtagidentityentryid-canonical-property.md)


[<span data-ttu-id="ddacd-201">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ddacd-201">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ddacd-202">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ddacd-202">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ddacd-203">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="ddacd-203">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ddacd-204">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="ddacd-204">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

