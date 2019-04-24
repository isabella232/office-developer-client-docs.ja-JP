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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 92067b5badfb2aab40f3b3735a164bc09321702c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322408"
---
# <a name="imapiprovidershutdown--iunknown"></a><span data-ttu-id="80af1-103">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="80af1-103">IMAPIProviderShutdown : IUnknown</span></span>

  
  
<span data-ttu-id="80af1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="80af1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="80af1-105">mapi サブシステムが mapi クライアントの高速シャットダウンの mapi プロバイダーに通知できるようにして、mapi プロバイダーがシャットダウンに応答できるようにします。</span><span class="sxs-lookup"><span data-stu-id="80af1-105">Allows the MAPI subsystem to inform a MAPI provider of the fast shutdown of a MAPI client, so that the MAPI provider can respond to the shutdown.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="80af1-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="80af1-106">Header file:</span></span>  <br/> |<span data-ttu-id="80af1-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="80af1-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="80af1-108">公開者:</span><span class="sxs-lookup"><span data-stu-id="80af1-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="80af1-109">プロバイダーオブジェクト: [ixpprovider](ixpprovideriunknown.md)、 [IABProvider](iabprovideriunknown.md)、または[IMSProvider](imsprovideriunknown.md)</span><span class="sxs-lookup"><span data-stu-id="80af1-109">Provider objects: [IXPProvider](ixpprovideriunknown.md), [IABProvider](iabprovideriunknown.md), or [IMSProvider](imsprovideriunknown.md)</span></span> <br/> |
|<span data-ttu-id="80af1-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="80af1-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="80af1-111">MAPI プロバイダー</span><span class="sxs-lookup"><span data-stu-id="80af1-111">MAPI provider</span></span>  <br/> |
|<span data-ttu-id="80af1-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="80af1-112">Called by:</span></span>  <br/> |<span data-ttu-id="80af1-113">MAPI サブシステム</span><span class="sxs-lookup"><span data-stu-id="80af1-113">MAPI subsystem</span></span>  <br/> |
|<span data-ttu-id="80af1-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="80af1-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="80af1-115">IID_IMAPIProviderShutdown</span><span class="sxs-lookup"><span data-stu-id="80af1-115">IID_IMAPIProviderShutdown</span></span>  <br/> |
|<span data-ttu-id="80af1-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="80af1-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="80af1-117">LPMAPIPROVIDERSHUTDOWN</span><span class="sxs-lookup"><span data-stu-id="80af1-117">LPMAPIPROVIDERSHUTDOWN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="80af1-118">v の順序</span><span class="sxs-lookup"><span data-stu-id="80af1-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="80af1-119">QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="80af1-119">QueryFastShutdown</span></span>](imapiprovidershutdown-queryfastshutdown.md) <br/> |<span data-ttu-id="80af1-120">MAPI プロバイダーに対して、高速シャットダウンのサポートを照会します。</span><span class="sxs-lookup"><span data-stu-id="80af1-120">Queries the MAPI provider for fast shutdown support.</span></span>  <br/> |
|[<span data-ttu-id="80af1-121">notifyprocessshutdown</span><span class="sxs-lookup"><span data-stu-id="80af1-121">NotifyProcessShutdown</span></span>](imapiprovidershutdown-notifyprocessshutdown.md) <br/> |<span data-ttu-id="80af1-122">mapi クライアントが高速シャットダウンを実行することを mapi プロバイダーに示します。これにより、プロバイダーはデータ損失を防止するアクションを実行できるようになります。</span><span class="sxs-lookup"><span data-stu-id="80af1-122">Indicates to the MAPI provider that a MAPI client is going to do a fast shutdown, so that the provider can take actions to prevent data loss.</span></span>  <br/> |
|[<span data-ttu-id="80af1-123">dofastshutdown</span><span class="sxs-lookup"><span data-stu-id="80af1-123">DoFastShutdown</span></span>](imapiprovidershutdown-dofastshutdown.md) <br/> |<span data-ttu-id="80af1-124">mapi プロバイダーに対して、mapi クライアントが直ちに終了していることを示します。したがって、データ損失を防止するために mapi プロバイダーは変更を保持します。</span><span class="sxs-lookup"><span data-stu-id="80af1-124">Indicates to the MAPI provider that the MAPI client is exiting immediately, so that the MAPI provider will persist changes to prevent data loss.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="80af1-125">解説</span><span class="sxs-lookup"><span data-stu-id="80af1-125">Remarks</span></span>

<span data-ttu-id="80af1-126">高速シャットダウンを使用すると、クライアントとロードされた mapi プロバイダーが mapi の設定とデータを保存した後に、mapi クライアントが短時間でプロセスを終了することができます。</span><span class="sxs-lookup"><span data-stu-id="80af1-126">Fast shutdown allows a MAPI client to exit its process within a short time, hopefully after the client and loaded MAPI providers have saved MAPI settings and data.</span></span> <span data-ttu-id="80af1-127">mapi クライアントは、常に高速シャットダウンを開始し、読み込み済みの mapi プロバイダーからの高速シャットダウンのサポートのために mapi サブシステムに対してクエリを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="80af1-127">The MAPI client always initiates a fast shutdown and should query the MAPI subsystem for fast shutdown support from the loaded MAPI providers.</span></span> <span data-ttu-id="80af1-128">管理者は、ユーザーレベルで Windows レジストリを設定して、すべての MAPI クライアントの高速シャットダウンを可能にするために必要なプロバイダーサポートのレベルを指定することができます。</span><span class="sxs-lookup"><span data-stu-id="80af1-128">An administrator can set the Windows registry at the user level to specify the level of provider support that is necessary to allow fast shutdown of all MAPI clients.</span></span> <span data-ttu-id="80af1-129">レジストリ設定の詳細については、「 [Fast Shutdown User Options](fast-shutdown-user-options.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="80af1-129">For more information about the registry settings, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span> <span data-ttu-id="80af1-130">しかし、データ損失が発生することなく、高速なシャットダウンが正常に実行されるようにするには、MAPI プロバイダーが**imapiprovidershutdown**インターフェイスを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="80af1-130">However, for fast shutdown to successfully occur without data loss, MAPI providers should implement the **IMAPIProviderShutdown** interface.</span></span> 
  
<span data-ttu-id="80af1-131">クライアントの高速シャットダウンをサポートする必要がある mapi プロバイダーは、 **imapiprovidershutdown:: queryfastshutdown**メソッド内の mapi サブシステムに S_OK を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="80af1-131">A MAPI provider that needs to support client fast shutdown should return S_OK to the MAPI subsystem in the **IMAPIProviderShutdown::QueryFastShutdown** method.</span></span> <span data-ttu-id="80af1-132">mapi サブシステムが、 **imapiprovidershutdown:: notifyprocessshutdown**および**imapiprovidershutdown**を呼び出した場合、mapi プロバイダーは mapi の設定とデータを保存するために必要なアクションを実行する必要があります。クライアントの終了を準備します。</span><span class="sxs-lookup"><span data-stu-id="80af1-132">When the MAPI subsystem subsequently calls the **IMAPIProviderShutdown::NotifyProcessShutdown** and **IMAPIProviderShutdown::DoFastShutdown** methods, the MAPI provider should take necessary actions to save MAPI settings and data and prepare for the client's exit.</span></span> 
  
<span data-ttu-id="80af1-133">クライアントの高速シャットダウンをサポートする必要がない MAPI プロバイダーは、まだ**imapiprovidershutdown**インターフェイスを実装していて、 **imapiprovidershutdown:: queryfastshutdown**メソッドが MAPI_E_NO_SUPPORT を返すようにしてください。</span><span class="sxs-lookup"><span data-stu-id="80af1-133">MAPI providers that do not need to support client fast shutdown should still implement the **IMAPIProviderShutdown** interface, and have the **IMAPIProviderShutdown::QueryFastShutdown** method return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="80af1-134">outlook を MAPI クライアントとして使用する場合、outlook は、すべての外部参照が終了するまで待機します。</span><span class="sxs-lookup"><span data-stu-id="80af1-134">For Outlook as a MAPI client, this causes Outlook to wait for all external references to be released before it exits.</span></span> 
  
<span data-ttu-id="80af1-135">高速シャットダウンのためのユーザーの Windows レジストリ設定によっては、 **imapiprovidershutdown**インターフェイスを実装していないと、クライアントの高速シャットダウンが必ずしも妨げられるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="80af1-135">Depending on the user's Windows registry setting for fast shutdown, not implementing the **IMAPIProviderShutdown** interface does not necessarily prevent a client fast shutdown.</span></span> 
  
<span data-ttu-id="80af1-136">高速シャットダウンのプロセスの詳細については、「[高速シャットダウンの概要](fast-shutdown-overview.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="80af1-136">For more information about the process of fast shutdown, see [Fast Shutdown Overview](fast-shutdown-overview.md).</span></span> <span data-ttu-id="80af1-137">高速シャットダウンを正常に実行する方法については、「[ファストシャットダウンのベストプラクティス](best-practices-for-fast-shutdown.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="80af1-137">For information about how to carry out fast shutdown successfully, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="80af1-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="80af1-138">See also</span></span>



[<span data-ttu-id="80af1-139">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="80af1-139">MAPI Interfaces</span></span>](mapi-interfaces.md)
  
[<span data-ttu-id="80af1-140">MAPI でのクライアント シャットダウン</span><span class="sxs-lookup"><span data-stu-id="80af1-140">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

