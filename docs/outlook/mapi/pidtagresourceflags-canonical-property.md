---
title: PidTagResourceFlags 標準プロパティ
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2fb9eed0beaf7269ac90a021dae650355484ebc2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330185"
---
# <a name="pidtagresourceflags-canonical-property"></a><span data-ttu-id="ac3fb-103">PidTagResourceFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ac3fb-103">PidTagResourceFlags Canonical Property</span></span>

  
  
<span data-ttu-id="ac3fb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac3fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac3fb-105">メッセージサービスとプロバイダーのフラグのビットマスクを含みます。</span><span class="sxs-lookup"><span data-stu-id="ac3fb-105">Contains a bitmask of flags for message services and providers.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ac3fb-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="ac3fb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ac3fb-107">PR_RESOURCE_FLAGS</span><span class="sxs-lookup"><span data-stu-id="ac3fb-107">PR_RESOURCE_FLAGS</span></span>  <br/> |
|<span data-ttu-id="ac3fb-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="ac3fb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ac3fb-109">0x3009</span><span class="sxs-lookup"><span data-stu-id="ac3fb-109">0x3009</span></span>  <br/> |
|<span data-ttu-id="ac3fb-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ac3fb-110">Data type:</span></span>  <br/> |<span data-ttu-id="ac3fb-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ac3fb-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ac3fb-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="ac3fb-112">Area:</span></span>  <br/> |<span data-ttu-id="ac3fb-113">MAPI 共通</span><span class="sxs-lookup"><span data-stu-id="ac3fb-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ac3fb-114">解説</span><span class="sxs-lookup"><span data-stu-id="ac3fb-114">Remarks</span></span>

<span data-ttu-id="ac3fb-115">このプロパティは、メッセージサービス、サービスプロバイダー、または status オブジェクトの特性を表します。</span><span class="sxs-lookup"><span data-stu-id="ac3fb-115">This property describes the characteristics of a message service, a service provider, or a status object.</span></span> <span data-ttu-id="ac3fb-116">このプロパティに設定されているフラグは、そのコンテキストに依存します。</span><span class="sxs-lookup"><span data-stu-id="ac3fb-116">The flags that are set for this property depend on its context.</span></span> <span data-ttu-id="ac3fb-117">たとえば、一部のフラグは、ステータスオブジェクトと、メッセージサービステーブル内の列の他のフラグにのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="ac3fb-117">For example, some flags are valid only for status objects and other flags only for columns in the message service table.</span></span> 
  
<span data-ttu-id="ac3fb-118">フラグには、静的、変更可能、動的の3つのクラスがあります。</span><span class="sxs-lookup"><span data-stu-id="ac3fb-118">The flags are of three classes: static, modifiable, and dynamic.</span></span> <span data-ttu-id="ac3fb-119">静的フラグは、mapisvc.inf のデータから MAPI によって設定されます。INF。変更されません。</span><span class="sxs-lookup"><span data-stu-id="ac3fb-119">Static flags are set by MAPI from data in MAPISVC.INF and never altered.</span></span> <span data-ttu-id="ac3fb-120">変更可能なフラグは、MAPI によって mapisvc.inf から設定されます。INF は後で変更できます。</span><span class="sxs-lookup"><span data-stu-id="ac3fb-120">Modifiable flags are set by MAPI from MAPISVC.INF but can be subsequently changed.</span></span> <span data-ttu-id="ac3fb-121">動的フラグは MAPI メソッドによって設定およびリセットできます。</span><span class="sxs-lookup"><span data-stu-id="ac3fb-121">Dynamic flags can be set and reset by MAPI methods.</span></span>
  
<span data-ttu-id="ac3fb-122">メッセージサービスの場合、このプロパティには次の1つ以上のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="ac3fb-122">For a message service, one or more of the following flags can be set in this property:</span></span>
  
<span data-ttu-id="ac3fb-123">SERVICE_CREATE_WITH_STORE</span><span class="sxs-lookup"><span data-stu-id="ac3fb-123">SERVICE_CREATE_WITH_STORE</span></span> 
  
> <span data-ttu-id="ac3fb-124">予約済み。</span><span class="sxs-lookup"><span data-stu-id="ac3fb-124">Reserved.</span></span> <span data-ttu-id="ac3fb-125">使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="ac3fb-125">Do not use.</span></span>
    
<span data-ttu-id="ac3fb-126">SERVICE_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="ac3fb-126">SERVICE_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="ac3fb-127">な.</span><span class="sxs-lookup"><span data-stu-id="ac3fb-127">Dynamic.</span></span> <span data-ttu-id="ac3fb-128">メッセージサービスには、既定のストアが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ac3fb-128">The message service contains the default store.</span></span> <span data-ttu-id="ac3fb-129">このサービスをプロファイルから削除または移動する前に、ユーザーに確認を求めるメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ac3fb-129">A user interface should be displayed prompting the user for confirmation before deleting or moving this service out of the profile.</span></span> 
    
<span data-ttu-id="ac3fb-130">SERVICE_NO_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="ac3fb-130">SERVICE_NO_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="ac3fb-131">静電気.</span><span class="sxs-lookup"><span data-stu-id="ac3fb-131">Static.</span></span> <span data-ttu-id="ac3fb-132">メッセージサービスのプロバイダーが id の提供に使用できないことを示すために設定する必要があるサービスレベルフラグ。</span><span class="sxs-lookup"><span data-stu-id="ac3fb-132">The service level flag that should be set to indicate that none of the providers in the message service can be used to supply an identity.</span></span> <span data-ttu-id="ac3fb-133">このフラグまたは SERVICE_PRIMARY_IDENTITY のどちらかを設定する必要がありますが、両方を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="ac3fb-133">Either this flag or SERVICE_PRIMARY_IDENTITY should be set, but not both.</span></span>
    
<span data-ttu-id="ac3fb-134">SERVICE_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="ac3fb-134">SERVICE_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="ac3fb-135">可能.</span><span class="sxs-lookup"><span data-stu-id="ac3fb-135">Modifiable.</span></span> <span data-ttu-id="ac3fb-136">対応するメッセージサービスには、このセッションのプライマリ id に使用されるプロバイダーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ac3fb-136">The corresponding message service contains the provider used for the primary identity for this session.</span></span> <span data-ttu-id="ac3fb-137">このフラグを設定するには、 [IMsgServiceAdmin:: setprimaryidentity](imsgserviceadmin-setprimaryidentity.md)を使用します。</span><span class="sxs-lookup"><span data-stu-id="ac3fb-137">Use [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) to set this flag.</span></span> <span data-ttu-id="ac3fb-138">このフラグまたは SERVICE_NO_PRIMARY_IDENTITY のどちらかを設定する必要がありますが、両方を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="ac3fb-138">Either this flag or SERVICE_NO_PRIMARY_IDENTITY should be set, but not both.</span></span> 
    
<span data-ttu-id="ac3fb-139">SERVICE_SINGLE_COPY</span><span class="sxs-lookup"><span data-stu-id="ac3fb-139">SERVICE_SINGLE_COPY</span></span> 
  
> <span data-ttu-id="ac3fb-140">静電気.</span><span class="sxs-lookup"><span data-stu-id="ac3fb-140">Static.</span></span> <span data-ttu-id="ac3fb-141">サービスが既に存在するプロファイルにこのメッセージサービスを作成またはコピーしようとすると、失敗します。</span><span class="sxs-lookup"><span data-stu-id="ac3fb-141">Any attempt to create or copy this message service into a profile where the service already exists will fail.</span></span> <span data-ttu-id="ac3fb-142">単一コピーのメッセージサービスを作成するには、mapisvc.inf のサービスのセクションに**PR_RESOURCE_FLAGS**プロパティを追加します。INF を設定し、このフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="ac3fb-142">To create a single copy message service add the **PR_RESOURCE_FLAGS** property to the service's section in MAPISVC.INF and set this flag.</span></span> 
    
<span data-ttu-id="ac3fb-143">サービスプロバイダーの場合、 **PR_RESOURCE_FLAGS**には次のフラグのうち1つ以上を設定できます。</span><span class="sxs-lookup"><span data-stu-id="ac3fb-143">For a service provider, one or more of the following flags can be set in **PR_RESOURCE_FLAGS**:</span></span>
  
<span data-ttu-id="ac3fb-144">HOOK_INBOUND</span><span class="sxs-lookup"><span data-stu-id="ac3fb-144">HOOK_INBOUND</span></span> 
  
> <span data-ttu-id="ac3fb-145">静電気.</span><span class="sxs-lookup"><span data-stu-id="ac3fb-145">Static.</span></span> <span data-ttu-id="ac3fb-146">スプーラーフックは、受信メッセージを処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ac3fb-146">The spooler hook needs to process inbound messages.</span></span>
    
<span data-ttu-id="ac3fb-147">HOOK_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="ac3fb-147">HOOK_OUTBOUND</span></span> 
  
> <span data-ttu-id="ac3fb-148">静電気.</span><span class="sxs-lookup"><span data-stu-id="ac3fb-148">Static.</span></span> <span data-ttu-id="ac3fb-149">スプーラーフックは、送信メッセージを処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ac3fb-149">The spooler hook needs to process outbound messages.</span></span> 
    
<span data-ttu-id="ac3fb-150">STATUS_DEFAULT_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="ac3fb-150">STATUS_DEFAULT_OUTBOUND</span></span> 
  
> <span data-ttu-id="ac3fb-151">可能.</span><span class="sxs-lookup"><span data-stu-id="ac3fb-151">Modifiable.</span></span> <span data-ttu-id="ac3fb-152">プロファイルにこのトランスポートプロバイダーの複数のインスタンスが含まれている場合は、この id を送信メッセージに適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ac3fb-152">This identity should be applied to outbound messages if the profile contains multiple instances of this transport provider.</span></span> <span data-ttu-id="ac3fb-153">これは、1つのトランスポートプロバイダーの複数のインスタンスがプロファイルに表示された場合に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ac3fb-153">This can happen if multiple instances of a single transport provider appear in the profile.</span></span>
    
<span data-ttu-id="ac3fb-154">STATUS_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="ac3fb-154">STATUS_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="ac3fb-155">可能.</span><span class="sxs-lookup"><span data-stu-id="ac3fb-155">Modifiable.</span></span> <span data-ttu-id="ac3fb-156">このメッセージストアは、プロファイルの既定のストアです。</span><span class="sxs-lookup"><span data-stu-id="ac3fb-156">This message store is the default store for the profile.</span></span> 
    
<span data-ttu-id="ac3fb-157">STATUS_NEED_IPM_TREE</span><span class="sxs-lookup"><span data-stu-id="ac3fb-157">STATUS_NEED_IPM_TREE</span></span> 
  
> <span data-ttu-id="ac3fb-158">な.</span><span class="sxs-lookup"><span data-stu-id="ac3fb-158">Dynamic.</span></span> <span data-ttu-id="ac3fb-159">このメッセージストアの標準フォルダー (個人間メッセージ (IPM) ルートフォルダーを含む) はまだ検証されていません。</span><span class="sxs-lookup"><span data-stu-id="ac3fb-159">The standard folders in this message store, including the interpersonal message (IPM) root folder, have not yet been verified.</span></span> <span data-ttu-id="ac3fb-160">MAPI は、このフラグを設定してクリアします。</span><span class="sxs-lookup"><span data-stu-id="ac3fb-160">MAPI sets and clears this flag.</span></span> 
    
<span data-ttu-id="ac3fb-161">STATUS_NO_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="ac3fb-161">STATUS_NO_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="ac3fb-162">静電気.</span><span class="sxs-lookup"><span data-stu-id="ac3fb-162">Static.</span></span> <span data-ttu-id="ac3fb-163">このメッセージストアは、プロファイルの既定のメッセージストアになることができません。</span><span class="sxs-lookup"><span data-stu-id="ac3fb-163">This message store is incapable of becoming the default message store for the profile.</span></span>
    
<span data-ttu-id="ac3fb-164">STATUS_NO_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="ac3fb-164">STATUS_NO_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="ac3fb-165">静電気.</span><span class="sxs-lookup"><span data-stu-id="ac3fb-165">Static.</span></span> <span data-ttu-id="ac3fb-166">このプロバイダーは、ステータス行で id を提供しません。</span><span class="sxs-lookup"><span data-stu-id="ac3fb-166">This provider does not furnish an identity in its status row.</span></span> <span data-ttu-id="ac3fb-167">このフラグまたは STATUS_PRIMARY_IDENTITY のいずれかを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ac3fb-167">Either this flag or STATUS_PRIMARY_IDENTITY must be set.</span></span>
    
<span data-ttu-id="ac3fb-168">STATUS_OWN_STORE</span><span class="sxs-lookup"><span data-stu-id="ac3fb-168">STATUS_OWN_STORE</span></span> 
  
> <span data-ttu-id="ac3fb-169">静電気.</span><span class="sxs-lookup"><span data-stu-id="ac3fb-169">Static.</span></span> <span data-ttu-id="ac3fb-170">このトランスポートプロバイダーは、メッセージストアと密に結合されており、そのステータス行の**PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) プロパティを furnishes します。</span><span class="sxs-lookup"><span data-stu-id="ac3fb-170">This transport provider is tightly coupled with a message store and furnishes the **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) property in its status row.</span></span>
    
<span data-ttu-id="ac3fb-171">STATUS_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="ac3fb-171">STATUS_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="ac3fb-172">可能.</span><span class="sxs-lookup"><span data-stu-id="ac3fb-172">Modifiable.</span></span> <span data-ttu-id="ac3fb-173">このプロバイダーは、セッションのプライマリ id を furnishes します。id を表すオブジェクトのエントリ識別子は、 [imapisession:: queryidentity](imapisession-queryidentity.md)から返されます。</span><span class="sxs-lookup"><span data-stu-id="ac3fb-173">This provider furnishes the primary identity for the session; the entry identifier for the object furnishing the identity is returned from [IMAPISession::QueryIdentity](imapisession-queryidentity.md).</span></span> <span data-ttu-id="ac3fb-174">このフラグまたは**STATUS_NO_PRIMARY_IDENTITY**のいずれかを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ac3fb-174">Either this flag or **STATUS_NO_PRIMARY_IDENTITY** must be set.</span></span> 
    
<span data-ttu-id="ac3fb-175">STATUS_PRIMARY_STORE</span><span class="sxs-lookup"><span data-stu-id="ac3fb-175">STATUS_PRIMARY_STORE</span></span> 
  
> <span data-ttu-id="ac3fb-176">可能.</span><span class="sxs-lookup"><span data-stu-id="ac3fb-176">Modifiable.</span></span> <span data-ttu-id="ac3fb-177">このメッセージストアは、クライアントアプリケーションがログオンするときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="ac3fb-177">This message store is to be used when a client application logs on.</span></span> <span data-ttu-id="ac3fb-178">このストアを開くと、プロファイルの既定のストアとしてこのストアを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ac3fb-178">Once opened, this store should be set as the default store for the profile.</span></span> 
    
<span data-ttu-id="ac3fb-179">STATUS_SECONDARY_STORE</span><span class="sxs-lookup"><span data-stu-id="ac3fb-179">STATUS_SECONDARY_STORE</span></span> 
  
> <span data-ttu-id="ac3fb-180">可能.</span><span class="sxs-lookup"><span data-stu-id="ac3fb-180">Modifiable.</span></span> <span data-ttu-id="ac3fb-181">このメッセージストアは、クライアントアプリケーションがログオンしたときにプライマリストアが使用できない場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="ac3fb-181">This message store is to be used if the primary store is not available when a client application logs on.</span></span> <span data-ttu-id="ac3fb-182">このストアを開くと、プロファイルの既定のストアとしてこのストアを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ac3fb-182">Once opened, this store should be set as the default store for the profile.</span></span> 
    
<span data-ttu-id="ac3fb-183">STATUS_SIMPLE_STORE</span><span class="sxs-lookup"><span data-stu-id="ac3fb-183">STATUS_SIMPLE_STORE</span></span> 
  
> <span data-ttu-id="ac3fb-184">な.</span><span class="sxs-lookup"><span data-stu-id="ac3fb-184">Dynamic.</span></span> <span data-ttu-id="ac3fb-185">このメッセージストアは、既定のメッセージストアとして簡易 MAPI によって使用されます。</span><span class="sxs-lookup"><span data-stu-id="ac3fb-185">This message store will be used by Simple MAPI as its default message store.</span></span>
    
<span data-ttu-id="ac3fb-186">STATUS_TEMP_SECTION</span><span class="sxs-lookup"><span data-stu-id="ac3fb-186">STATUS_TEMP_SECTION</span></span> 
  
> <span data-ttu-id="ac3fb-187">な.</span><span class="sxs-lookup"><span data-stu-id="ac3fb-187">Dynamic.</span></span> <span data-ttu-id="ac3fb-188">このメッセージストアは、メッセージストアテーブルに公開しないでください。ログオフ後にプロファイルから削除されます。</span><span class="sxs-lookup"><span data-stu-id="ac3fb-188">This message store should not be published in the message store table and will be deleted from the profile after logoff.</span></span> 
    
<span data-ttu-id="ac3fb-189">STATUS_XP_PREFER_LAST</span><span class="sxs-lookup"><span data-stu-id="ac3fb-189">STATUS_XP_PREFER_LAST</span></span> 
  
> <span data-ttu-id="ac3fb-190">静電気.</span><span class="sxs-lookup"><span data-stu-id="ac3fb-190">Static.</span></span> <span data-ttu-id="ac3fb-191">このトランスポートは、複数のトランスポートプロバイダーがメッセージを送信できる場合に、メッセージを送信するために選択された最後のトランスポートであると想定します。</span><span class="sxs-lookup"><span data-stu-id="ac3fb-191">This transport expects to be the last transport selected to send a message when multiple transport providers are able to transmit the message.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="ac3fb-192">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ac3fb-192">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ac3fb-193">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="ac3fb-193">Header files</span></span>

<span data-ttu-id="ac3fb-194">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ac3fb-194">Mapidefs.h</span></span>
  
> <span data-ttu-id="ac3fb-195">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ac3fb-195">Provides data type definitions.</span></span>
    
<span data-ttu-id="ac3fb-196">Mapitags</span><span class="sxs-lookup"><span data-stu-id="ac3fb-196">Mapitags.h</span></span>
  
> <span data-ttu-id="ac3fb-197">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ac3fb-197">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ac3fb-198">関連項目</span><span class="sxs-lookup"><span data-stu-id="ac3fb-198">See also</span></span>



[<span data-ttu-id="ac3fb-199">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="ac3fb-199">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>](imsgserviceadmin-msgservicetransportorder.md)
  
[<span data-ttu-id="ac3fb-200">PidTagIdentityEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ac3fb-200">PidTagIdentityEntryId Canonical Property</span></span>](pidtagidentityentryid-canonical-property.md)


[<span data-ttu-id="ac3fb-201">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="ac3fb-201">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ac3fb-202">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ac3fb-202">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ac3fb-203">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ac3fb-203">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ac3fb-204">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ac3fb-204">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

