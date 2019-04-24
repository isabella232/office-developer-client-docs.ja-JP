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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341101"
---
# <a name="fast-shutdown-overview"></a><span data-ttu-id="9aab0-103">高速シャットダウンの概要</span><span class="sxs-lookup"><span data-stu-id="9aab0-103">Fast Shutdown Overview</span></span>

<span data-ttu-id="9aab0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9aab0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9aab0-105">高速シャットダウンは、クライアントがアクティブな mapi セッションを持っているすべてのプロバイダーに、クライアントプロセスが終了する前にデータおよび設定を保存するように通知する、mapi クライアントのメカニズムです。</span><span class="sxs-lookup"><span data-stu-id="9aab0-105">Fast shutdown is a mechanism for a MAPI client to initiate a quick shutdown of the client process, notifying all providers with which the client has an active MAPI session to save data and settings before the client process exits.</span></span> <span data-ttu-id="9aab0-106">このトピックでは、高速シャットダウンの基本的なメカニズムについて説明します。</span><span class="sxs-lookup"><span data-stu-id="9aab0-106">This topic describes the basic mechanism of fast shutdown.</span></span> 

<span data-ttu-id="9aab0-107">microsoft outlook 2010 以降では、microsoft outlook 2013 を含む現在、MAPI サブシステムは[IMAPIClientShutdown: IUnknown](imapiclientshutdowniunknown.md)インターフェイスを提供しています。</span><span class="sxs-lookup"><span data-stu-id="9aab0-107">Starting in Microsoft Outlook 2010 and now including Microsoft Outlook 2013, the MAPI subsystem provides the [IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md) interface.</span></span> <span data-ttu-id="9aab0-108">Outlook およびその他の MAPI クライアントは、クライアントプロセスを終了するための既定のメカニズムとして、高速シャットダウンを採用できます。</span><span class="sxs-lookup"><span data-stu-id="9aab0-108">Outlook and other MAPI clients can adopt fast shutdown as the default mechanism to exit the client process.</span></span> <span data-ttu-id="9aab0-109">クライアントコンピューターの Windows レジストリのユーザーレベルの設定により、そのコンピューター上のそのユーザーのすべての MAPI クライアントに対する高速シャットダウンの導入が制御されます。</span><span class="sxs-lookup"><span data-stu-id="9aab0-109">A user-level setting in the Windows registry of the client computer controls the adoption of fast shutdown for all MAPI clients for that user on that computer.</span></span> <span data-ttu-id="9aab0-110">レジストリ設定の詳細については、「 [Fast Shutdown User Options](fast-shutdown-user-options.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9aab0-110">For details about the registry settings, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span>
  
<span data-ttu-id="9aab0-111">MAPI クライアントで高速シャットダウンを導入する必要がある場合は、 **IMAPIClientShutdown: IUnknown**インターフェイスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9aab0-111">If a MAPI client needs to adopt fast shutdown, it must use the **IMAPIClientShutdown : IUnknown** interface.</span></span> <span data-ttu-id="9aab0-112">クライアントがシャットダウンしようとする場合の一般的なイベントの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="9aab0-112">The following is the typical course of events when the client attempts to shut down:</span></span> 
  
1. <span data-ttu-id="9aab0-113">mapi クライアントは、 [IMAPIClientShutdown:: queryfastshutdown](imapiclientshutdown-queryfastshutdown.md)メソッドを呼び出してシャットダウンを開始し、mapi サブシステムが高速シャットダウンをサポートしているかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="9aab0-113">The MAPI client initiates the shutdown by calling the [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) method to determine whether the MAPI subsystem supports fast shutdown.</span></span> 
    
2. <span data-ttu-id="9aab0-114">MAPI サブシステムは、次の手順を使用して、クライアントの**IMAPIClientShutdown:: queryfastshutdown**呼び出しに対して使用可能な高速シャットダウンサポートで応答します。</span><span class="sxs-lookup"><span data-stu-id="9aab0-114">The MAPI subsystem responds with the available fast shutdown support to the client's **IMAPIClientShutdown::QueryFastShutdown** call by using the following procedure:</span></span> 
    
    1. <span data-ttu-id="9aab0-115">mapi サブシステムは、mapi クライアントプロセスがアクティブな mapi セッションを持つ mapi プロバイダーごとに、imapiprovidershutdown: [: queryfastshutdown](imapiprovidershutdown-queryfastshutdown.md)メソッドを呼び出します。これは、プロバイダーが[imapiprovidershutdown: IUnknown](imapiprovidershutdowniunknown.md)を実装している場合です。インターフェイス.</span><span class="sxs-lookup"><span data-stu-id="9aab0-115">The MAPI subsystem calls the [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) method for each MAPI provider with which the MAPI client process has an active MAPI session, if the provider has implemented the [IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md) interface.</span></span> 
        
       > [!NOTE]
       >  <span data-ttu-id="9aab0-116">mapi サブシステムは常に、次の順序で mapi プロバイダーに対して、 **imapiprovidershutdown: IUnknown**インターフェイスを通じて mapi プロバイダーに対してクエリを実行し、それぞれの mapi セッションで通知します。</span><span class="sxs-lookup"><span data-stu-id="9aab0-116">The MAPI subsystem always queries and notifies MAPI providers through the **IMAPIProviderShutdown : IUnknown** interface within each MAPI session in the following order:</span></span>
       > 1. <span data-ttu-id="9aab0-117">トランスポートプロバイダー</span><span class="sxs-lookup"><span data-stu-id="9aab0-117">Transport providers</span></span>
       > 2. <span data-ttu-id="9aab0-118">アドレス帳プロバイダー</span><span class="sxs-lookup"><span data-stu-id="9aab0-118">Address book providers</span></span>
       > 3. <span data-ttu-id="9aab0-119">ストアプロバイダー</span><span class="sxs-lookup"><span data-stu-id="9aab0-119">Store providers</span></span> 
    
    2. <span data-ttu-id="9aab0-120">クライアントコンピューターでのそのユーザーの高速シャットダウンのレジストリ設定に応じて、MAPI サブシステムは**IMAPIClientShutdown:: queryfastshutdown**に対して適切なリターンコードを指定します。</span><span class="sxs-lookup"><span data-stu-id="9aab0-120">Depending on the fast shutdown registry setting for that user on the client computer, the MAPI subsystem specifies the appropriate return code to **IMAPIClientShutdown::QueryFastShutdown**.</span></span> <span data-ttu-id="9aab0-121">戻り値のコードは、S_OK または MAPI_E_NO_SUPPORT のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="9aab0-121">The return code is either S_OK or MAPI_E_NO_SUPPORT.</span></span>
        
    3. <span data-ttu-id="9aab0-122">mapi クライアントは[IMAPIClientShutdown:: notifyprocessshutdown](imapiclientshutdown-notifyprocessshutdown.md)メソッドを呼び出して、mapi サブシステムにシャットダウンの意図を示します。</span><span class="sxs-lookup"><span data-stu-id="9aab0-122">The MAPI client calls the [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) method to indicate to the MAPI subsystem the intention to shut down.</span></span> 
        
    4. <span data-ttu-id="9aab0-123">mapi サブシステムは、読み込まれた mapi プロバイダーごとに、mapi クライアントがシャットダウンすることを示します。</span><span class="sxs-lookup"><span data-stu-id="9aab0-123">The MAPI subsystem indicates to each loaded MAPI provider that the MAPI client will shut down.</span></span> <span data-ttu-id="9aab0-124">**imapiprovidershutdown: IUnknown**インターフェイスを実装しているプロバイダーの MAPI サブシステムは、対応する[imapiprovidershutdown:: notifyprocessshutdown](imapiprovidershutdown-notifyprocessshutdown.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9aab0-124">For those providers that have implemented the **IMAPIProviderShutdown : IUnknown** interface, the MAPI subsystem calls the corresponding [IMAPIProviderShutdown::NotifyProcessShutdown](imapiprovidershutdown-notifyprocessshutdown.md) method.</span></span> 
        
    5. <span data-ttu-id="9aab0-125">mapi クライアントは[IMAPIClientShutdown::D ofastshutdown](imapiclientshutdown-dofastshutdown.md)メソッドを呼び出して、クライアントプロセスが直ちに終了したことを mapi サブシステムに示します。</span><span class="sxs-lookup"><span data-stu-id="9aab0-125">The MAPI client calls the [IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md) method to indicate to the MAPI subsystem that the client process is exiting immediately.</span></span> 
        
    6. <span data-ttu-id="9aab0-126">mapi サブシステムは、mapi クライアントプロセスを終了する、読み込まれた各 mapi プロバイダーを示します。</span><span class="sxs-lookup"><span data-stu-id="9aab0-126">The MAPI subsystem indicates to each loaded MAPI provider that the MAPI client process is exiting.</span></span> <span data-ttu-id="9aab0-127">**imapiprovidershutdown: IUnknown**インターフェイスを実装しているプロバイダーの MAPI サブシステムは、対応する[imapiprovidershutdown::D ofastshutdown](imapiprovidershutdown-dofastshutdown.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9aab0-127">For those providers that have implemented the **IMAPIProviderShutdown : IUnknown** interface, the MAPI subsystem calls the corresponding [IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) method.</span></span> <span data-ttu-id="9aab0-128">この時点で、これらの mapi プロバイダーは、データや設定の保存など、必要なすべての操作が完了したことを、mapi クライアントが直ちにすべての参照を切断して終了することを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9aab0-128">At this point, these MAPI providers should verify that all necessary actions, such as saving data and settings, are complete in preparation for the MAPI client to immediately disconnect all references and exit.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="9aab0-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="9aab0-129">See also</span></span>

- [<span data-ttu-id="9aab0-130">MAPI でのクライアント シャットダウン</span><span class="sxs-lookup"><span data-stu-id="9aab0-130">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)
- [<span data-ttu-id="9aab0-131">高速シャットダウンのユーザーオプション</span><span class="sxs-lookup"><span data-stu-id="9aab0-131">Fast Shutdown User Options</span></span>](fast-shutdown-user-options.md)
- [<span data-ttu-id="9aab0-132">高速シャットダウンのためのベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="9aab0-132">Best Practices for Fast Shutdown</span></span>](best-practices-for-fast-shutdown.md)

