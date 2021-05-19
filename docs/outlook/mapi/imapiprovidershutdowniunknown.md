---
title: IMAPIProviderShutdown IUnknown
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
# <a name="imapiprovidershutdown--iunknown"></a><span data-ttu-id="25202-103">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="25202-103">IMAPIProviderShutdown : IUnknown</span></span>

  
  
<span data-ttu-id="25202-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="25202-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="25202-105">MAPI サブシステムが MAPI クライアントの高速シャットダウンを MAPI プロバイダーに通知して、MAPI プロバイダーがシャットダウンに応答できます。</span><span class="sxs-lookup"><span data-stu-id="25202-105">Allows the MAPI subsystem to inform a MAPI provider of the fast shutdown of a MAPI client, so that the MAPI provider can respond to the shutdown.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="25202-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="25202-106">Header file:</span></span>  <br/> |<span data-ttu-id="25202-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="25202-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="25202-108">次のユーザーによって公開されます。</span><span class="sxs-lookup"><span data-stu-id="25202-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="25202-109">プロバイダー オブジェクト: [IXPProvider、IABProvider、](ixpprovideriunknown.md)または[IMSProvider](imsprovideriunknown.md) [](iabprovideriunknown.md)</span><span class="sxs-lookup"><span data-stu-id="25202-109">Provider objects: [IXPProvider](ixpprovideriunknown.md), [IABProvider](iabprovideriunknown.md), or [IMSProvider](imsprovideriunknown.md)</span></span> <br/> |
|<span data-ttu-id="25202-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="25202-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="25202-111">MAPI プロバイダー</span><span class="sxs-lookup"><span data-stu-id="25202-111">MAPI provider</span></span>  <br/> |
|<span data-ttu-id="25202-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="25202-112">Called by:</span></span>  <br/> |<span data-ttu-id="25202-113">MAPI サブシステム</span><span class="sxs-lookup"><span data-stu-id="25202-113">MAPI subsystem</span></span>  <br/> |
|<span data-ttu-id="25202-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="25202-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="25202-115">IID_IMAPIProviderShutdown</span><span class="sxs-lookup"><span data-stu-id="25202-115">IID_IMAPIProviderShutdown</span></span>  <br/> |
|<span data-ttu-id="25202-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="25202-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="25202-117">LPMAPIPROVIDERSHUTDOWN</span><span class="sxs-lookup"><span data-stu-id="25202-117">LPMAPIPROVIDERSHUTDOWN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="25202-118">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="25202-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="25202-119">QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="25202-119">QueryFastShutdown</span></span>](imapiprovidershutdown-queryfastshutdown.md) <br/> |<span data-ttu-id="25202-120">MAPI プロバイダーに高速シャットダウンのサポートを照会します。</span><span class="sxs-lookup"><span data-stu-id="25202-120">Queries the MAPI provider for fast shutdown support.</span></span>  <br/> |
|[<span data-ttu-id="25202-121">NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="25202-121">NotifyProcessShutdown</span></span>](imapiprovidershutdown-notifyprocessshutdown.md) <br/> |<span data-ttu-id="25202-122">MAPI クライアントが高速シャットダウンを実行し、プロバイダーがデータ損失を防止するアクションを実行できるよう、MAPI プロバイダーに対して示します。</span><span class="sxs-lookup"><span data-stu-id="25202-122">Indicates to the MAPI provider that a MAPI client is going to do a fast shutdown, so that the provider can take actions to prevent data loss.</span></span>  <br/> |
|[<span data-ttu-id="25202-123">DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="25202-123">DoFastShutdown</span></span>](imapiprovidershutdown-dofastshutdown.md) <br/> |<span data-ttu-id="25202-124">MAPI クライアントが直ちに終了し、MAPI プロバイダーがデータ損失を防ぐために変更を保持する MAPI プロバイダーを示します。</span><span class="sxs-lookup"><span data-stu-id="25202-124">Indicates to the MAPI provider that the MAPI client is exiting immediately, so that the MAPI provider will persist changes to prevent data loss.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25202-125">注釈</span><span class="sxs-lookup"><span data-stu-id="25202-125">Remarks</span></span>

<span data-ttu-id="25202-126">高速シャットダウンにより、MAPI クライアントは、クライアントと読み込まれた MAPI プロバイダーが MAPI 設定とデータを保存した後、短時間でプロセスを終了できます。</span><span class="sxs-lookup"><span data-stu-id="25202-126">Fast shutdown allows a MAPI client to exit its process within a short time, hopefully after the client and loaded MAPI providers have saved MAPI settings and data.</span></span> <span data-ttu-id="25202-127">MAPI クライアントは常に高速シャットダウンを開始し、読み込まれた MAPI プロバイダーからの高速シャットダウンのサポートを MAPI サブシステムに照会する必要があります。</span><span class="sxs-lookup"><span data-stu-id="25202-127">The MAPI client always initiates a fast shutdown and should query the MAPI subsystem for fast shutdown support from the loaded MAPI providers.</span></span> <span data-ttu-id="25202-128">管理者は、ユーザー レベルWindowsレジストリを設定して、すべての MAPI クライアントの高速シャットダウンを許可するために必要なプロバイダー サポートのレベルを指定できます。</span><span class="sxs-lookup"><span data-stu-id="25202-128">An administrator can set the Windows registry at the user level to specify the level of provider support that is necessary to allow fast shutdown of all MAPI clients.</span></span> <span data-ttu-id="25202-129">レジストリ設定の詳細については、「Fast Shutdown [User Options」を参照してください](fast-shutdown-user-options.md)。</span><span class="sxs-lookup"><span data-stu-id="25202-129">For more information about the registry settings, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span> <span data-ttu-id="25202-130">ただし、データ損失なしで高速シャットダウンが正常に行われるには、MAPI プロバイダーが **IMAPIProviderShutdown インターフェイスを実装する必要** があります。</span><span class="sxs-lookup"><span data-stu-id="25202-130">However, for fast shutdown to successfully occur without data loss, MAPI providers should implement the **IMAPIProviderShutdown** interface.</span></span> 
  
<span data-ttu-id="25202-131">クライアントの高速シャットダウンをサポートする必要がある MAPI プロバイダーは **、IMAPIProviderShutdown::QueryFastShutdown** メソッドの MAPI サブシステムにS_OKを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="25202-131">A MAPI provider that needs to support client fast shutdown should return S_OK to the MAPI subsystem in the **IMAPIProviderShutdown::QueryFastShutdown** method.</span></span> <span data-ttu-id="25202-132">MAPI サブシステムが後で **IMAPIProviderShutdown::NotifyProcessShutdown** と **IMAPIProviderShutdown::D oFastShutdown** メソッドを呼び出す場合、MAPI プロバイダーは MAPI 設定とデータを保存し、クライアントの終了に備える必要なアクションを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="25202-132">When the MAPI subsystem subsequently calls the **IMAPIProviderShutdown::NotifyProcessShutdown** and **IMAPIProviderShutdown::DoFastShutdown** methods, the MAPI provider should take necessary actions to save MAPI settings and data and prepare for the client's exit.</span></span> 
  
<span data-ttu-id="25202-133">クライアントの高速シャットダウンをサポートする必要のない MAPI プロバイダーは **、IMAPIProviderShutdown** インターフェイスを実装し **、IMAPIProviderShutdown::QueryFastShutdown** メソッドが MAPI_E_NO_SUPPORT を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="25202-133">MAPI providers that do not need to support client fast shutdown should still implement the **IMAPIProviderShutdown** interface, and have the **IMAPIProviderShutdown::QueryFastShutdown** method return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="25202-134">MAPI Outlookとして使用すると、Outlook前にすべての外部参照が解放されるのを待つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="25202-134">For Outlook as a MAPI client, this causes Outlook to wait for all external references to be released before it exits.</span></span> 
  
<span data-ttu-id="25202-135">高速シャットダウン用のユーザーの Windows レジストリ設定によっては **、IMAPIProviderShutdown** インターフェイスを実装しない場合でも、クライアントの高速シャットダウンが必ずしも妨げであるとは限りません。</span><span class="sxs-lookup"><span data-stu-id="25202-135">Depending on the user's Windows registry setting for fast shutdown, not implementing the **IMAPIProviderShutdown** interface does not necessarily prevent a client fast shutdown.</span></span> 
  
<span data-ttu-id="25202-136">高速シャットダウンのプロセスの詳細については、「Fast Shutdown Overview 」 [を参照してください](fast-shutdown-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="25202-136">For more information about the process of fast shutdown, see [Fast Shutdown Overview](fast-shutdown-overview.md).</span></span> <span data-ttu-id="25202-137">高速シャットダウンを正常に実行する方法については、「Fast Shutdown の [ベスト プラクティス」を参照してください](best-practices-for-fast-shutdown.md)。</span><span class="sxs-lookup"><span data-stu-id="25202-137">For information about how to carry out fast shutdown successfully, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="25202-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="25202-138">See also</span></span>



[<span data-ttu-id="25202-139">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="25202-139">MAPI Interfaces</span></span>](mapi-interfaces.md)
  
[<span data-ttu-id="25202-140">MAPI でのクライアント シャットダウン</span><span class="sxs-lookup"><span data-stu-id="25202-140">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

