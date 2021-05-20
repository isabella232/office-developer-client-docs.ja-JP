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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2fb9eed0beaf7269ac90a021dae650355484ebc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436231"
---
# <a name="pidtagresourceflags-canonical-property"></a><span data-ttu-id="32d5c-103">PidTagResourceFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="32d5c-103">PidTagResourceFlags Canonical Property</span></span>

  
  
<span data-ttu-id="32d5c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="32d5c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="32d5c-105">メッセージ サービスとプロバイダーのフラグのビットマスクが含まれる。</span><span class="sxs-lookup"><span data-stu-id="32d5c-105">Contains a bitmask of flags for message services and providers.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="32d5c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="32d5c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="32d5c-107">PR_RESOURCE_FLAGS</span><span class="sxs-lookup"><span data-stu-id="32d5c-107">PR_RESOURCE_FLAGS</span></span>  <br/> |
|<span data-ttu-id="32d5c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="32d5c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="32d5c-109">0x3009</span><span class="sxs-lookup"><span data-stu-id="32d5c-109">0x3009</span></span>  <br/> |
|<span data-ttu-id="32d5c-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="32d5c-110">Data type:</span></span>  <br/> |<span data-ttu-id="32d5c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="32d5c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="32d5c-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="32d5c-112">Area:</span></span>  <br/> |<span data-ttu-id="32d5c-113">MAPI 共通</span><span class="sxs-lookup"><span data-stu-id="32d5c-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="32d5c-114">注釈</span><span class="sxs-lookup"><span data-stu-id="32d5c-114">Remarks</span></span>

<span data-ttu-id="32d5c-115">このプロパティは、メッセージ サービス、サービス プロバイダー、または状態オブジェクトの特性を説明します。</span><span class="sxs-lookup"><span data-stu-id="32d5c-115">This property describes the characteristics of a message service, a service provider, or a status object.</span></span> <span data-ttu-id="32d5c-116">このプロパティに設定されるフラグは、そのコンテキストによって異なる。</span><span class="sxs-lookup"><span data-stu-id="32d5c-116">The flags that are set for this property depend on its context.</span></span> <span data-ttu-id="32d5c-117">たとえば、一部のフラグはステータス オブジェクトにのみ有効で、他のフラグはメッセージ サービス テーブル内の列に対してのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="32d5c-117">For example, some flags are valid only for status objects and other flags only for columns in the message service table.</span></span> 
  
<span data-ttu-id="32d5c-118">フラグは、静的、変更可能、動的の 3 つのクラスです。</span><span class="sxs-lookup"><span data-stu-id="32d5c-118">The flags are of three classes: static, modifiable, and dynamic.</span></span> <span data-ttu-id="32d5c-119">静的フラグは、MAPISVC のデータから MAPI によって設定されます。INF で、変更されません。</span><span class="sxs-lookup"><span data-stu-id="32d5c-119">Static flags are set by MAPI from data in MAPISVC.INF and never altered.</span></span> <span data-ttu-id="32d5c-120">変更可能なフラグは、MAPISVC から MAPI によって設定されます。INF が、後で変更できます。</span><span class="sxs-lookup"><span data-stu-id="32d5c-120">Modifiable flags are set by MAPI from MAPISVC.INF but can be subsequently changed.</span></span> <span data-ttu-id="32d5c-121">動的フラグは、MAPI メソッドによって設定およびリセットできます。</span><span class="sxs-lookup"><span data-stu-id="32d5c-121">Dynamic flags can be set and reset by MAPI methods.</span></span>
  
<span data-ttu-id="32d5c-122">メッセージ サービスの場合、このプロパティで次のフラグを 1 つ以上設定できます。</span><span class="sxs-lookup"><span data-stu-id="32d5c-122">For a message service, one or more of the following flags can be set in this property:</span></span>
  
<span data-ttu-id="32d5c-123">SERVICE_CREATE_WITH_STORE</span><span class="sxs-lookup"><span data-stu-id="32d5c-123">SERVICE_CREATE_WITH_STORE</span></span> 
  
> <span data-ttu-id="32d5c-124">予約済み。</span><span class="sxs-lookup"><span data-stu-id="32d5c-124">Reserved.</span></span> <span data-ttu-id="32d5c-125">使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="32d5c-125">Do not use.</span></span>
    
<span data-ttu-id="32d5c-126">SERVICE_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="32d5c-126">SERVICE_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="32d5c-127">動的。</span><span class="sxs-lookup"><span data-stu-id="32d5c-127">Dynamic.</span></span> <span data-ttu-id="32d5c-128">メッセージ サービスには、既定のストアが含まれる。</span><span class="sxs-lookup"><span data-stu-id="32d5c-128">The message service contains the default store.</span></span> <span data-ttu-id="32d5c-129">このサービスをプロファイルから削除または移動する前に、ユーザーに確認を求めるユーザー インターフェイスを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="32d5c-129">A user interface should be displayed prompting the user for confirmation before deleting or moving this service out of the profile.</span></span> 
    
<span data-ttu-id="32d5c-130">SERVICE_NO_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="32d5c-130">SERVICE_NO_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="32d5c-131">静的。</span><span class="sxs-lookup"><span data-stu-id="32d5c-131">Static.</span></span> <span data-ttu-id="32d5c-132">メッセージ サービス内のプロバイダーのいずれも ID の指定に使用し得ないかどうかを示すために設定する必要があるサービス レベル フラグ。</span><span class="sxs-lookup"><span data-stu-id="32d5c-132">The service level flag that should be set to indicate that none of the providers in the message service can be used to supply an identity.</span></span> <span data-ttu-id="32d5c-133">このフラグまたは設定SERVICE_PRIMARY_IDENTITY設定する必要がありますが、両方は設定できません。</span><span class="sxs-lookup"><span data-stu-id="32d5c-133">Either this flag or SERVICE_PRIMARY_IDENTITY should be set, but not both.</span></span>
    
<span data-ttu-id="32d5c-134">SERVICE_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="32d5c-134">SERVICE_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="32d5c-135">変更可能。</span><span class="sxs-lookup"><span data-stu-id="32d5c-135">Modifiable.</span></span> <span data-ttu-id="32d5c-136">対応するメッセージ サービスには、このセッションのプライマリ ID に使用されるプロバイダーが含まれる。</span><span class="sxs-lookup"><span data-stu-id="32d5c-136">The corresponding message service contains the provider used for the primary identity for this session.</span></span> <span data-ttu-id="32d5c-137">この [フラグを設定するには、IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) を使用します。</span><span class="sxs-lookup"><span data-stu-id="32d5c-137">Use [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) to set this flag.</span></span> <span data-ttu-id="32d5c-138">このフラグまたは設定SERVICE_NO_PRIMARY_IDENTITY設定する必要がありますが、両方は設定できません。</span><span class="sxs-lookup"><span data-stu-id="32d5c-138">Either this flag or SERVICE_NO_PRIMARY_IDENTITY should be set, but not both.</span></span> 
    
<span data-ttu-id="32d5c-139">SERVICE_SINGLE_COPY</span><span class="sxs-lookup"><span data-stu-id="32d5c-139">SERVICE_SINGLE_COPY</span></span> 
  
> <span data-ttu-id="32d5c-140">静的。</span><span class="sxs-lookup"><span data-stu-id="32d5c-140">Static.</span></span> <span data-ttu-id="32d5c-141">サービスが既に存在するプロファイルにこのメッセージ サービスを作成またはコピーしようとすると、失敗します。</span><span class="sxs-lookup"><span data-stu-id="32d5c-141">Any attempt to create or copy this message service into a profile where the service already exists will fail.</span></span> <span data-ttu-id="32d5c-142">1 つのコピー メッセージ サービスを作成するには **、MAPISVC** PR_RESOURCE_FLAGSに PR_RESOURCE_FLAGS プロパティを追加します。INF とこのフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="32d5c-142">To create a single copy message service add the **PR_RESOURCE_FLAGS** property to the service's section in MAPISVC.INF and set this flag.</span></span> 
    
<span data-ttu-id="32d5c-143">サービス プロバイダーの場合は、次のフラグの 1 つ以上を次に設定 **PR_RESOURCE_FLAGS。**</span><span class="sxs-lookup"><span data-stu-id="32d5c-143">For a service provider, one or more of the following flags can be set in **PR_RESOURCE_FLAGS**:</span></span>
  
<span data-ttu-id="32d5c-144">HOOK_INBOUND</span><span class="sxs-lookup"><span data-stu-id="32d5c-144">HOOK_INBOUND</span></span> 
  
> <span data-ttu-id="32d5c-145">静的。</span><span class="sxs-lookup"><span data-stu-id="32d5c-145">Static.</span></span> <span data-ttu-id="32d5c-146">スプーラー フックは、受信メッセージを処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="32d5c-146">The spooler hook needs to process inbound messages.</span></span>
    
<span data-ttu-id="32d5c-147">HOOK_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="32d5c-147">HOOK_OUTBOUND</span></span> 
  
> <span data-ttu-id="32d5c-148">静的。</span><span class="sxs-lookup"><span data-stu-id="32d5c-148">Static.</span></span> <span data-ttu-id="32d5c-149">スプーラー フックは送信メッセージを処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="32d5c-149">The spooler hook needs to process outbound messages.</span></span> 
    
<span data-ttu-id="32d5c-150">STATUS_DEFAULT_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="32d5c-150">STATUS_DEFAULT_OUTBOUND</span></span> 
  
> <span data-ttu-id="32d5c-151">変更可能。</span><span class="sxs-lookup"><span data-stu-id="32d5c-151">Modifiable.</span></span> <span data-ttu-id="32d5c-152">プロファイルにこのトランスポート プロバイダーの複数のインスタンスが含まれている場合は、この ID を送信メッセージに適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="32d5c-152">This identity should be applied to outbound messages if the profile contains multiple instances of this transport provider.</span></span> <span data-ttu-id="32d5c-153">これは、1 つのトランスポート プロバイダーの複数のインスタンスがプロファイルに表示される場合に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="32d5c-153">This can happen if multiple instances of a single transport provider appear in the profile.</span></span>
    
<span data-ttu-id="32d5c-154">STATUS_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="32d5c-154">STATUS_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="32d5c-155">変更可能。</span><span class="sxs-lookup"><span data-stu-id="32d5c-155">Modifiable.</span></span> <span data-ttu-id="32d5c-156">このメッセージ ストアは、プロファイルの既定のストアです。</span><span class="sxs-lookup"><span data-stu-id="32d5c-156">This message store is the default store for the profile.</span></span> 
    
<span data-ttu-id="32d5c-157">STATUS_NEED_IPM_TREE</span><span class="sxs-lookup"><span data-stu-id="32d5c-157">STATUS_NEED_IPM_TREE</span></span> 
  
> <span data-ttu-id="32d5c-158">動的。</span><span class="sxs-lookup"><span data-stu-id="32d5c-158">Dynamic.</span></span> <span data-ttu-id="32d5c-159">このメッセージ ストアの標準フォルダー (対人間メッセージ (IPM) ルート フォルダーを含む) は、まだ確認されていません。</span><span class="sxs-lookup"><span data-stu-id="32d5c-159">The standard folders in this message store, including the interpersonal message (IPM) root folder, have not yet been verified.</span></span> <span data-ttu-id="32d5c-160">MAPI は、このフラグを設定およびクリアします。</span><span class="sxs-lookup"><span data-stu-id="32d5c-160">MAPI sets and clears this flag.</span></span> 
    
<span data-ttu-id="32d5c-161">STATUS_NO_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="32d5c-161">STATUS_NO_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="32d5c-162">静的。</span><span class="sxs-lookup"><span data-stu-id="32d5c-162">Static.</span></span> <span data-ttu-id="32d5c-163">このメッセージ ストアは、プロファイルの既定のメッセージ ストアになるには使用できません。</span><span class="sxs-lookup"><span data-stu-id="32d5c-163">This message store is incapable of becoming the default message store for the profile.</span></span>
    
<span data-ttu-id="32d5c-164">STATUS_NO_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="32d5c-164">STATUS_NO_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="32d5c-165">静的。</span><span class="sxs-lookup"><span data-stu-id="32d5c-165">Static.</span></span> <span data-ttu-id="32d5c-166">このプロバイダーは、ステータス行に ID を指定しない。</span><span class="sxs-lookup"><span data-stu-id="32d5c-166">This provider does not furnish an identity in its status row.</span></span> <span data-ttu-id="32d5c-167">このフラグまたは設定STATUS_PRIMARY_IDENTITY設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="32d5c-167">Either this flag or STATUS_PRIMARY_IDENTITY must be set.</span></span>
    
<span data-ttu-id="32d5c-168">STATUS_OWN_STORE</span><span class="sxs-lookup"><span data-stu-id="32d5c-168">STATUS_OWN_STORE</span></span> 
  
> <span data-ttu-id="32d5c-169">静的。</span><span class="sxs-lookup"><span data-stu-id="32d5c-169">Static.</span></span> <span data-ttu-id="32d5c-170">このトランスポート プロバイダーは、メッセージ ストアと密に結合され、PR_OWN_STORE_ENTRYID **(** [PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) プロパティを状態行に指定します。</span><span class="sxs-lookup"><span data-stu-id="32d5c-170">This transport provider is tightly coupled with a message store and furnishes the **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) property in its status row.</span></span>
    
<span data-ttu-id="32d5c-171">STATUS_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="32d5c-171">STATUS_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="32d5c-172">変更可能。</span><span class="sxs-lookup"><span data-stu-id="32d5c-172">Modifiable.</span></span> <span data-ttu-id="32d5c-173">このプロバイダーは、セッションのプライマリ ID を提供します。ID を提供するオブジェクトのエントリ識別子は [IMAPISession::QueryIdentity から返されます](imapisession-queryidentity.md)。</span><span class="sxs-lookup"><span data-stu-id="32d5c-173">This provider furnishes the primary identity for the session; the entry identifier for the object furnishing the identity is returned from [IMAPISession::QueryIdentity](imapisession-queryidentity.md).</span></span> <span data-ttu-id="32d5c-174">このフラグ **または設定STATUS_NO_PRIMARY_IDENTITY** 設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="32d5c-174">Either this flag or **STATUS_NO_PRIMARY_IDENTITY** must be set.</span></span> 
    
<span data-ttu-id="32d5c-175">STATUS_PRIMARY_STORE</span><span class="sxs-lookup"><span data-stu-id="32d5c-175">STATUS_PRIMARY_STORE</span></span> 
  
> <span data-ttu-id="32d5c-176">変更可能。</span><span class="sxs-lookup"><span data-stu-id="32d5c-176">Modifiable.</span></span> <span data-ttu-id="32d5c-177">このメッセージ ストアは、クライアント アプリケーションがログオンするときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="32d5c-177">This message store is to be used when a client application logs on.</span></span> <span data-ttu-id="32d5c-178">開いた後、このストアをプロファイルの既定のストアとして設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="32d5c-178">Once opened, this store should be set as the default store for the profile.</span></span> 
    
<span data-ttu-id="32d5c-179">STATUS_SECONDARY_STORE</span><span class="sxs-lookup"><span data-stu-id="32d5c-179">STATUS_SECONDARY_STORE</span></span> 
  
> <span data-ttu-id="32d5c-180">変更可能。</span><span class="sxs-lookup"><span data-stu-id="32d5c-180">Modifiable.</span></span> <span data-ttu-id="32d5c-181">このメッセージ ストアは、クライアント アプリケーションのログオン時にプライマリ ストアが使用できない場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="32d5c-181">This message store is to be used if the primary store is not available when a client application logs on.</span></span> <span data-ttu-id="32d5c-182">開いた後、このストアをプロファイルの既定のストアとして設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="32d5c-182">Once opened, this store should be set as the default store for the profile.</span></span> 
    
<span data-ttu-id="32d5c-183">STATUS_SIMPLE_STORE</span><span class="sxs-lookup"><span data-stu-id="32d5c-183">STATUS_SIMPLE_STORE</span></span> 
  
> <span data-ttu-id="32d5c-184">動的。</span><span class="sxs-lookup"><span data-stu-id="32d5c-184">Dynamic.</span></span> <span data-ttu-id="32d5c-185">このメッセージ ストアは、簡易 MAPI が既定のメッセージ ストアとして使用します。</span><span class="sxs-lookup"><span data-stu-id="32d5c-185">This message store will be used by Simple MAPI as its default message store.</span></span>
    
<span data-ttu-id="32d5c-186">STATUS_TEMP_SECTION</span><span class="sxs-lookup"><span data-stu-id="32d5c-186">STATUS_TEMP_SECTION</span></span> 
  
> <span data-ttu-id="32d5c-187">動的。</span><span class="sxs-lookup"><span data-stu-id="32d5c-187">Dynamic.</span></span> <span data-ttu-id="32d5c-188">このメッセージ ストアは、メッセージ ストア テーブルに発行し、ログオフ後にプロファイルから削除される必要があります。</span><span class="sxs-lookup"><span data-stu-id="32d5c-188">This message store should not be published in the message store table and will be deleted from the profile after logoff.</span></span> 
    
<span data-ttu-id="32d5c-189">STATUS_XP_PREFER_LAST</span><span class="sxs-lookup"><span data-stu-id="32d5c-189">STATUS_XP_PREFER_LAST</span></span> 
  
> <span data-ttu-id="32d5c-190">静的。</span><span class="sxs-lookup"><span data-stu-id="32d5c-190">Static.</span></span> <span data-ttu-id="32d5c-191">このトランスポートは、複数のトランスポート プロバイダーがメッセージを送信できる場合に、メッセージを送信するために選択された最後のトランスポートである必要があります。</span><span class="sxs-lookup"><span data-stu-id="32d5c-191">This transport expects to be the last transport selected to send a message when multiple transport providers are able to transmit the message.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="32d5c-192">関連リソース</span><span class="sxs-lookup"><span data-stu-id="32d5c-192">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="32d5c-193">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="32d5c-193">Header files</span></span>

<span data-ttu-id="32d5c-194">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="32d5c-194">Mapidefs.h</span></span>
  
> <span data-ttu-id="32d5c-195">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="32d5c-195">Provides data type definitions.</span></span>
    
<span data-ttu-id="32d5c-196">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="32d5c-196">Mapitags.h</span></span>
  
> <span data-ttu-id="32d5c-197">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="32d5c-197">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="32d5c-198">関連項目</span><span class="sxs-lookup"><span data-stu-id="32d5c-198">See also</span></span>



[<span data-ttu-id="32d5c-199">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="32d5c-199">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>](imsgserviceadmin-msgservicetransportorder.md)
  
[<span data-ttu-id="32d5c-200">PidTagIdentityEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="32d5c-200">PidTagIdentityEntryId Canonical Property</span></span>](pidtagidentityentryid-canonical-property.md)


[<span data-ttu-id="32d5c-201">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="32d5c-201">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="32d5c-202">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="32d5c-202">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="32d5c-203">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="32d5c-203">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="32d5c-204">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="32d5c-204">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

