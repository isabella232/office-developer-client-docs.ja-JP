---
title: 高速シャットダウンの概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a7830d73-427c-4f8b-86f4-51e040c142c3
description: '最終更新日: 2012 年 6 月 26 日'
ms.openlocfilehash: 8c33214b04e7c41eab173196c09f145c20ddf219
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427207"
---
# <a name="fast-shutdown-overview"></a><span data-ttu-id="4fdeb-103">高速シャットダウンの概要</span><span class="sxs-lookup"><span data-stu-id="4fdeb-103">Fast Shutdown Overview</span></span>

<span data-ttu-id="4fdeb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4fdeb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4fdeb-105">高速シャットダウンは、MAPI クライアントがクライアント プロセスのクイック シャットダウンを開始するメカニズムであり、クライアントがアクティブな MAPI セッションを持つすべてのプロバイダーに通知して、クライアント プロセスが終了する前にデータと設定を保存します。</span><span class="sxs-lookup"><span data-stu-id="4fdeb-105">Fast shutdown is a mechanism for a MAPI client to initiate a quick shutdown of the client process, notifying all providers with which the client has an active MAPI session to save data and settings before the client process exits.</span></span> <span data-ttu-id="4fdeb-106">このトピックでは、高速シャットダウンの基本的なメカニズムについて説明します。</span><span class="sxs-lookup"><span data-stu-id="4fdeb-106">This topic describes the basic mechanism of fast shutdown.</span></span> 

<span data-ttu-id="4fdeb-107">MAPI サブシステムは、Microsoft Outlook 2010から開始し[Microsoft Outlook 2013、IMAPIClientShutdown : IUnknown インターフェイスを提供](imapiclientshutdowniunknown.md)します。</span><span class="sxs-lookup"><span data-stu-id="4fdeb-107">Starting in Microsoft Outlook 2010 and now including Microsoft Outlook 2013, the MAPI subsystem provides the [IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md) interface.</span></span> <span data-ttu-id="4fdeb-108">Outlook MAPI クライアントは、クライアント プロセスを終了するための既定のメカニズムとして高速シャットダウンを採用できます。</span><span class="sxs-lookup"><span data-stu-id="4fdeb-108">Outlook and other MAPI clients can adopt fast shutdown as the default mechanism to exit the client process.</span></span> <span data-ttu-id="4fdeb-109">クライアント コンピューターの Windows レジストリのユーザー レベルの設定は、そのコンピューター上のすべての MAPI クライアントに対する高速シャットダウンの採用を制御します。</span><span class="sxs-lookup"><span data-stu-id="4fdeb-109">A user-level setting in the Windows registry of the client computer controls the adoption of fast shutdown for all MAPI clients for that user on that computer.</span></span> <span data-ttu-id="4fdeb-110">レジストリ設定の詳細については、「Fast [Shutdown User Options」を参照してください](fast-shutdown-user-options.md)。</span><span class="sxs-lookup"><span data-stu-id="4fdeb-110">For details about the registry settings, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span>
  
<span data-ttu-id="4fdeb-111">MAPI クライアントが高速シャットダウンを採用する必要がある場合は **、IMAPIClientShutdown : IUnknown インターフェイスを使用する必要** があります。</span><span class="sxs-lookup"><span data-stu-id="4fdeb-111">If a MAPI client needs to adopt fast shutdown, it must use the **IMAPIClientShutdown : IUnknown** interface.</span></span> <span data-ttu-id="4fdeb-112">クライアントがシャットダウンを試みる一般的なイベントの一般的なコースを次に示します。</span><span class="sxs-lookup"><span data-stu-id="4fdeb-112">The following is the typical course of events when the client attempts to shut down:</span></span> 
  
1. <span data-ttu-id="4fdeb-113">MAPI クライアントは [、IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) メソッドを呼び出して、MAPI サブシステムが高速シャットダウンをサポートするかどうかを判断して、シャットダウンを開始します。</span><span class="sxs-lookup"><span data-stu-id="4fdeb-113">The MAPI client initiates the shutdown by calling the [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) method to determine whether the MAPI subsystem supports fast shutdown.</span></span> 
    
2. <span data-ttu-id="4fdeb-114">MAPI サブシステムは、次の手順を使用して、クライアントの **IMAPIClientShutdown::QueryFastShutdown** 呼び出しに対して、利用可能な高速シャットダウンサポートに応答します。</span><span class="sxs-lookup"><span data-stu-id="4fdeb-114">The MAPI subsystem responds with the available fast shutdown support to the client's **IMAPIClientShutdown::QueryFastShutdown** call by using the following procedure:</span></span> 
    
    1. <span data-ttu-id="4fdeb-115">MAPI サブシステムは、MAPI クライアント プロセスがアクティブな MAPI セッションを持つ MAPI プロバイダーごとに [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) メソッドを呼び出します。プロバイダーが [IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md) インターフェイスを実装している場合。</span><span class="sxs-lookup"><span data-stu-id="4fdeb-115">The MAPI subsystem calls the [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) method for each MAPI provider with which the MAPI client process has an active MAPI session, if the provider has implemented the [IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md) interface.</span></span> 
        
       > [!NOTE]
       >  <span data-ttu-id="4fdeb-116">MAPI サブシステムは常に **、IMAPIProviderShutdown : IUnknown** インターフェイスを使用して MAPI プロバイダーに対して次の順序でクエリを実行し、通知します。</span><span class="sxs-lookup"><span data-stu-id="4fdeb-116">The MAPI subsystem always queries and notifies MAPI providers through the **IMAPIProviderShutdown : IUnknown** interface within each MAPI session in the following order:</span></span>
       > 1. <span data-ttu-id="4fdeb-117">トランスポート プロバイダー</span><span class="sxs-lookup"><span data-stu-id="4fdeb-117">Transport providers</span></span>
       > 2. <span data-ttu-id="4fdeb-118">アドレス帳プロバイダー</span><span class="sxs-lookup"><span data-stu-id="4fdeb-118">Address book providers</span></span>
       > 3. <span data-ttu-id="4fdeb-119">ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="4fdeb-119">Store providers</span></span> 
    
    2. <span data-ttu-id="4fdeb-120">クライアント コンピューター上のユーザーの高速シャットダウン レジストリ設定に応じて、MAPI サブシステムは **IMAPIClientShutdown::QueryFastShutdown** に適切な戻りコードを指定します。</span><span class="sxs-lookup"><span data-stu-id="4fdeb-120">Depending on the fast shutdown registry setting for that user on the client computer, the MAPI subsystem specifies the appropriate return code to **IMAPIClientShutdown::QueryFastShutdown**.</span></span> <span data-ttu-id="4fdeb-121">戻りコードは、S_OKまたはMAPI_E_NO_SUPPORT。</span><span class="sxs-lookup"><span data-stu-id="4fdeb-121">The return code is either S_OK or MAPI_E_NO_SUPPORT.</span></span>
        
    3. <span data-ttu-id="4fdeb-122">MAPI クライアントは [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) メソッドを呼び出して、シャットダウンの意図を MAPI サブシステムに示します。</span><span class="sxs-lookup"><span data-stu-id="4fdeb-122">The MAPI client calls the [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) method to indicate to the MAPI subsystem the intention to shut down.</span></span> 
        
    4. <span data-ttu-id="4fdeb-123">MAPI サブシステムは、読み込まれた各 MAPI プロバイダーに対して、MAPI クライアントがシャットダウンを示します。</span><span class="sxs-lookup"><span data-stu-id="4fdeb-123">The MAPI subsystem indicates to each loaded MAPI provider that the MAPI client will shut down.</span></span> <span data-ttu-id="4fdeb-124">**IMAPIProviderShutdown : IUnknown** インターフェイスを実装したプロバイダーの場合、MAPI サブシステムは対応する [IMAPIProviderShutdown::NotifyProcessShutdown](imapiprovidershutdown-notifyprocessshutdown.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4fdeb-124">For those providers that have implemented the **IMAPIProviderShutdown : IUnknown** interface, the MAPI subsystem calls the corresponding [IMAPIProviderShutdown::NotifyProcessShutdown](imapiprovidershutdown-notifyprocessshutdown.md) method.</span></span> 
        
    5. <span data-ttu-id="4fdeb-125">MAPI クライアントは [IMAPIClientShutdown::D oFastShutdown](imapiclientshutdown-dofastshutdown.md) メソッドを呼び出して、クライアント プロセスが直ちに終了している MAPI サブシステムに示します。</span><span class="sxs-lookup"><span data-stu-id="4fdeb-125">The MAPI client calls the [IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md) method to indicate to the MAPI subsystem that the client process is exiting immediately.</span></span> 
        
    6. <span data-ttu-id="4fdeb-126">MAPI サブシステムは、読み込まれた各 MAPI プロバイダーに対して、MAPI クライアント プロセスが終了中かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="4fdeb-126">The MAPI subsystem indicates to each loaded MAPI provider that the MAPI client process is exiting.</span></span> <span data-ttu-id="4fdeb-127">**IMAPIProviderShutdown : IUnknown** インターフェイスを実装したプロバイダーの場合、MAPI サブシステムは対応する [IMAPIProviderShutdown::D oFastShutdown](imapiprovidershutdown-dofastshutdown.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4fdeb-127">For those providers that have implemented the **IMAPIProviderShutdown : IUnknown** interface, the MAPI subsystem calls the corresponding [IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) method.</span></span> <span data-ttu-id="4fdeb-128">この時点で、これらの MAPI プロバイダーは、データや設定の保存など、すべての必要なアクションが完了し、MAPI クライアントがすべての参照を直ちに切断して終了する準備が完了している必要があります。</span><span class="sxs-lookup"><span data-stu-id="4fdeb-128">At this point, these MAPI providers should verify that all necessary actions, such as saving data and settings, are complete in preparation for the MAPI client to immediately disconnect all references and exit.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="4fdeb-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="4fdeb-129">See also</span></span>

- [<span data-ttu-id="4fdeb-130">MAPI でのクライアント シャットダウン</span><span class="sxs-lookup"><span data-stu-id="4fdeb-130">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)
- [<span data-ttu-id="4fdeb-131">Fast Shutdown User Options</span><span class="sxs-lookup"><span data-stu-id="4fdeb-131">Fast Shutdown User Options</span></span>](fast-shutdown-user-options.md)
- [<span data-ttu-id="4fdeb-132">高速シャットダウンのためのベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="4fdeb-132">Best Practices for Fast Shutdown</span></span>](best-practices-for-fast-shutdown.md)

