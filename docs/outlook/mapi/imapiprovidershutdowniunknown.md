---
title: imapiprovidershutdown IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown
api_type:
- COM
ms.assetid: fd86c8a5-f251-46c3-ace9-515e94e504ac
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 92067b5badfb2aab40f3b3735a164bc09321702c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409658"
---
# <a name="imapiprovidershutdown--iunknown"></a><span data-ttu-id="44927-103">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="44927-103">IMAPIProviderShutdown : IUnknown</span></span>

  
  
<span data-ttu-id="44927-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44927-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44927-105">mapi サブシステムが mapi クライアントの高速シャットダウンの mapi プロバイダーに通知できるようにして、mapi プロバイダーがシャットダウンに応答できるようにします。</span><span class="sxs-lookup"><span data-stu-id="44927-105">Allows the MAPI subsystem to inform a MAPI provider of the fast shutdown of a MAPI client, so that the MAPI provider can respond to the shutdown.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="44927-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="44927-106">Header file:</span></span>  <br/> |<span data-ttu-id="44927-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="44927-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="44927-108">公開者:</span><span class="sxs-lookup"><span data-stu-id="44927-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="44927-109">プロバイダーオブジェクト: [ixpprovider](ixpprovideriunknown.md)、 [IABProvider](iabprovideriunknown.md)、または[IMSProvider](imsprovideriunknown.md)</span><span class="sxs-lookup"><span data-stu-id="44927-109">Provider objects: [IXPProvider](ixpprovideriunknown.md), [IABProvider](iabprovideriunknown.md), or [IMSProvider](imsprovideriunknown.md)</span></span> <br/> |
|<span data-ttu-id="44927-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="44927-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="44927-111">MAPI プロバイダー</span><span class="sxs-lookup"><span data-stu-id="44927-111">MAPI provider</span></span>  <br/> |
|<span data-ttu-id="44927-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="44927-112">Called by:</span></span>  <br/> |<span data-ttu-id="44927-113">MAPI サブシステム</span><span class="sxs-lookup"><span data-stu-id="44927-113">MAPI subsystem</span></span>  <br/> |
|<span data-ttu-id="44927-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="44927-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="44927-115">IID_IMAPIProviderShutdown</span><span class="sxs-lookup"><span data-stu-id="44927-115">IID_IMAPIProviderShutdown</span></span>  <br/> |
|<span data-ttu-id="44927-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="44927-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="44927-117">LPMAPIPROVIDERSHUTDOWN</span><span class="sxs-lookup"><span data-stu-id="44927-117">LPMAPIPROVIDERSHUTDOWN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="44927-118">v の順序</span><span class="sxs-lookup"><span data-stu-id="44927-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="44927-119">QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="44927-119">QueryFastShutdown</span></span>](imapiprovidershutdown-queryfastshutdown.md) <br/> |<span data-ttu-id="44927-120">MAPI プロバイダーに対して、高速シャットダウンのサポートを照会します。</span><span class="sxs-lookup"><span data-stu-id="44927-120">Queries the MAPI provider for fast shutdown support.</span></span>  <br/> |
|[<span data-ttu-id="44927-121">notifyprocessshutdown</span><span class="sxs-lookup"><span data-stu-id="44927-121">NotifyProcessShutdown</span></span>](imapiprovidershutdown-notifyprocessshutdown.md) <br/> |<span data-ttu-id="44927-122">mapi クライアントが高速シャットダウンを実行することを mapi プロバイダーに示します。これにより、プロバイダーはデータ損失を防止するアクションを実行できるようになります。</span><span class="sxs-lookup"><span data-stu-id="44927-122">Indicates to the MAPI provider that a MAPI client is going to do a fast shutdown, so that the provider can take actions to prevent data loss.</span></span>  <br/> |
|[<span data-ttu-id="44927-123">dofastshutdown</span><span class="sxs-lookup"><span data-stu-id="44927-123">DoFastShutdown</span></span>](imapiprovidershutdown-dofastshutdown.md) <br/> |<span data-ttu-id="44927-124">mapi プロバイダーに対して、mapi クライアントが直ちに終了していることを示します。したがって、データ損失を防止するために mapi プロバイダーは変更を保持します。</span><span class="sxs-lookup"><span data-stu-id="44927-124">Indicates to the MAPI provider that the MAPI client is exiting immediately, so that the MAPI provider will persist changes to prevent data loss.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="44927-125">注釈</span><span class="sxs-lookup"><span data-stu-id="44927-125">Remarks</span></span>

<span data-ttu-id="44927-126">高速シャットダウンを使用すると、クライアントとロードされた mapi プロバイダーが mapi の設定とデータを保存した後に、mapi クライアントが短時間でプロセスを終了することができます。</span><span class="sxs-lookup"><span data-stu-id="44927-126">Fast shutdown allows a MAPI client to exit its process within a short time, hopefully after the client and loaded MAPI providers have saved MAPI settings and data.</span></span> <span data-ttu-id="44927-127">mapi クライアントは、常に高速シャットダウンを開始し、読み込み済みの mapi プロバイダーからの高速シャットダウンのサポートのために mapi サブシステムに対してクエリを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="44927-127">The MAPI client always initiates a fast shutdown and should query the MAPI subsystem for fast shutdown support from the loaded MAPI providers.</span></span> <span data-ttu-id="44927-128">管理者は、ユーザーレベルで Windows レジストリを設定して、すべての MAPI クライアントの高速シャットダウンを可能にするために必要なプロバイダーサポートのレベルを指定することができます。</span><span class="sxs-lookup"><span data-stu-id="44927-128">An administrator can set the Windows registry at the user level to specify the level of provider support that is necessary to allow fast shutdown of all MAPI clients.</span></span> <span data-ttu-id="44927-129">レジストリ設定の詳細については、「 [Fast Shutdown User Options](fast-shutdown-user-options.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="44927-129">For more information about the registry settings, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span> <span data-ttu-id="44927-130">しかし、データ損失が発生することなく、高速なシャットダウンが正常に実行されるようにするには、MAPI プロバイダーが**imapiprovidershutdown**インターフェイスを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="44927-130">However, for fast shutdown to successfully occur without data loss, MAPI providers should implement the **IMAPIProviderShutdown** interface.</span></span> 
  
<span data-ttu-id="44927-131">クライアントの高速シャットダウンをサポートする必要がある mapi プロバイダーは、 **imapiprovidershutdown:: queryfastshutdown**メソッド内の mapi サブシステムに S_OK を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="44927-131">A MAPI provider that needs to support client fast shutdown should return S_OK to the MAPI subsystem in the **IMAPIProviderShutdown::QueryFastShutdown** method.</span></span> <span data-ttu-id="44927-132">mapi サブシステムが、 **imapiprovidershutdown:: notifyprocessshutdown**および**imapiprovidershutdown**を呼び出した場合、mapi プロバイダーは mapi の設定とデータを保存するために必要なアクションを実行する必要があります。クライアントの終了を準備します。</span><span class="sxs-lookup"><span data-stu-id="44927-132">When the MAPI subsystem subsequently calls the **IMAPIProviderShutdown::NotifyProcessShutdown** and **IMAPIProviderShutdown::DoFastShutdown** methods, the MAPI provider should take necessary actions to save MAPI settings and data and prepare for the client's exit.</span></span> 
  
<span data-ttu-id="44927-133">クライアントの高速シャットダウンをサポートする必要がない MAPI プロバイダーは、まだ**imapiprovidershutdown**インターフェイスを実装していて、 **imapiprovidershutdown:: queryfastshutdown**メソッドが MAPI_E_NO_SUPPORT を返すようにしてください。</span><span class="sxs-lookup"><span data-stu-id="44927-133">MAPI providers that do not need to support client fast shutdown should still implement the **IMAPIProviderShutdown** interface, and have the **IMAPIProviderShutdown::QueryFastShutdown** method return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="44927-134">outlook を MAPI クライアントとして使用する場合、outlook は、すべての外部参照が終了するまで待機します。</span><span class="sxs-lookup"><span data-stu-id="44927-134">For Outlook as a MAPI client, this causes Outlook to wait for all external references to be released before it exits.</span></span> 
  
<span data-ttu-id="44927-135">高速シャットダウンのためのユーザーの Windows レジストリ設定によっては、 **imapiprovidershutdown**インターフェイスを実装していないと、クライアントの高速シャットダウンが必ずしも妨げられるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="44927-135">Depending on the user's Windows registry setting for fast shutdown, not implementing the **IMAPIProviderShutdown** interface does not necessarily prevent a client fast shutdown.</span></span> 
  
<span data-ttu-id="44927-136">高速シャットダウンのプロセスの詳細については、「[高速シャットダウンの概要](fast-shutdown-overview.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="44927-136">For more information about the process of fast shutdown, see [Fast Shutdown Overview](fast-shutdown-overview.md).</span></span> <span data-ttu-id="44927-137">高速シャットダウンを正常に実行する方法については、「[ファストシャットダウンのベストプラクティス](best-practices-for-fast-shutdown.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="44927-137">For information about how to carry out fast shutdown successfully, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="44927-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="44927-138">See also</span></span>



[<span data-ttu-id="44927-139">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="44927-139">MAPI Interfaces</span></span>](mapi-interfaces.md)
  
[<span data-ttu-id="44927-140">MAPI でのクライアント シャットダウン</span><span class="sxs-lookup"><span data-stu-id="44927-140">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

