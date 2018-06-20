---
title: 高速シャット ダウンの概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a7830d73-427c-4f8b-86f4-51e040c142c3
description: '最終更新日: 2012 年 6 月 26 日'
ms.openlocfilehash: 17b1307427af2c35fe9ba8ee40dc78958e6b4a21
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800028"
---
# <a name="fast-shutdown-overview"></a><span data-ttu-id="e9a0d-103">高速シャット ダウンの概要</span><span class="sxs-lookup"><span data-stu-id="e9a0d-103">Fast Shutdown Overview</span></span>

<span data-ttu-id="e9a0d-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e9a0d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e9a0d-105">高速シャット ダウンは、簡易クライアントがクライアント プロセスが終了する前に、データや設定を保存するのにはアクティブな MAPI セッションを持っているすべてのプロバイダーに通知する、クライアント プロセスのシャット ダウンを開始するのには MAPI クライアントのための機構です。</span><span class="sxs-lookup"><span data-stu-id="e9a0d-105">Fast shutdown is a mechanism for a MAPI client to initiate a quick shutdown of the client process, notifying all providers with which the client has an active MAPI session to save data and settings before the client process exits.</span></span> <span data-ttu-id="e9a0d-106">このトピックでは、高速シャット ダウンの基本的なメカニズムについて説明します。</span><span class="sxs-lookup"><span data-stu-id="e9a0d-106">This topic describes the basic mechanism of fast shutdown.</span></span> 

<span data-ttu-id="e9a0d-107">MAPI サブシステムは、Microsoft Outlook 2010 で起動して、Microsoft Outlook 2013 を含むようになりました、 [IMAPIClientShutdown: IUnknown](imapiclientshutdowniunknown.md)インタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="e9a0d-107">Starting in Microsoft Outlook 2010 and now including Microsoft Outlook 2013, the MAPI subsystem provides the [IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md) interface.</span></span> <span data-ttu-id="e9a0d-108">Outlook およびその他の MAPI クライアントは、クライアントのプロセスを終了するのには既定の機構として、高速シャット ダウンを採用することができます。</span><span class="sxs-lookup"><span data-stu-id="e9a0d-108">Outlook and other MAPI clients can adopt fast shutdown as the default mechanism to exit the client process.</span></span> <span data-ttu-id="e9a0d-109">クライアント コンピューターの Windows レジストリにユーザー レベルの設定は、そのコンピューターでそのユーザーのすべての MAPI クライアント用の高速シャット ダウンの導入を制御します。</span><span class="sxs-lookup"><span data-stu-id="e9a0d-109">A user-level setting in the Windows registry of the client computer controls the adoption of fast shutdown for all MAPI clients for that user on that computer.</span></span> <span data-ttu-id="e9a0d-110">レジストリ設定の詳細については、[高速シャット ダウンのユーザー オプション](fast-shutdown-user-options.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e9a0d-110">For details about the registry settings, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span>
  
<span data-ttu-id="e9a0d-111">それを使用する必要がある場合は、MAPI クライアントでは、高速シャット ダウンを採用する必要がある、 **IMAPIClientShutdown: IUnknown**インタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="e9a0d-111">If a MAPI client needs to adopt fast shutdown, it must use the **IMAPIClientShutdown : IUnknown** interface.</span></span> <span data-ttu-id="e9a0d-112">以下は、クライアントがシャット ダウンしようとするときのイベントの標準的なコースです。</span><span class="sxs-lookup"><span data-stu-id="e9a0d-112">The following is the typical course of events when the client attempts to shut down:</span></span> 
  
1. <span data-ttu-id="e9a0d-113">MAPI クライアントは、MAPI サブシステムが高速シャット ダウンをサポートしているかどうかを決定する[IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md)メソッドを呼び出すことによって、シャット ダウンを開始します。</span><span class="sxs-lookup"><span data-stu-id="e9a0d-113">The MAPI client initiates the shutdown by calling the [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) method to determine whether the MAPI subsystem supports fast shutdown.</span></span> 
    
2. <span data-ttu-id="e9a0d-114">MAPI サブシステムは、次の手順を使用して、クライアントの**IMAPIClientShutdown::QueryFastShutdown**の呼び出しに使用可能な高速シャット ダウンのサポートを使用して応答します。</span><span class="sxs-lookup"><span data-stu-id="e9a0d-114">The MAPI subsystem responds with the available fast shutdown support to the client's **IMAPIClientShutdown::QueryFastShutdown** call by using the following procedure:</span></span> 
    
    1. <span data-ttu-id="e9a0d-115">プロバイダーが実装されている場合、MAPI サブシステムが MAPI クライアント プロセスが、アクティブな MAPI セッションを各 MAPI プロバイダーの[IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md)メソッドを呼び出し、 [IMAPIProviderShutdown: IUnknown](imapiprovidershutdowniunknown.md)インタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="e9a0d-115">The MAPI subsystem calls the [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) method for each MAPI provider with which the MAPI client process has an active MAPI session, if the provider has implemented the [IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md) interface.</span></span> 
        
       > [!NOTE]
       >  <span data-ttu-id="e9a0d-116">MAPI サブシステムは、常にクエリを実行しからの MAPI プロバイダーに通知、 **IMAPIProviderShutdown: IUnknown**次の順序では、各 MAPI セッション内でのインターフェイス。</span><span class="sxs-lookup"><span data-stu-id="e9a0d-116">The MAPI subsystem always queries and notifies MAPI providers through the **IMAPIProviderShutdown : IUnknown** interface within each MAPI session in the following order:</span></span>
       > 1. <span data-ttu-id="e9a0d-117">トランスポート プロバイダー</span><span class="sxs-lookup"><span data-stu-id="e9a0d-117">Transport providers</span></span>
       > 2. <span data-ttu-id="e9a0d-118">アドレス帳プロバイダー</span><span class="sxs-lookup"><span data-stu-id="e9a0d-118">Address book providers</span></span>
       > 3. <span data-ttu-id="e9a0d-119">ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="e9a0d-119">Store providers</span></span> 
    
    2. <span data-ttu-id="e9a0d-120">クライアント コンピューターでそのユーザーの高速シャット ダウンのレジストリ設定によっては、MAPI サブシステムは、 **IMAPIClientShutdown::QueryFastShutdown**への適切なリターン コードを指定します。</span><span class="sxs-lookup"><span data-stu-id="e9a0d-120">Depending on the fast shutdown registry setting for that user on the client computer, the MAPI subsystem specifies the appropriate return code to **IMAPIClientShutdown::QueryFastShutdown**.</span></span> <span data-ttu-id="e9a0d-121">リターン コードは、S_OK または MAPI_E_NO_SUPPORT のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="e9a0d-121">The return code is either S_OK or MAPI_E_NO_SUPPORT.</span></span>
        
    3. <span data-ttu-id="e9a0d-122">MAPI クライアントは、MAPI サブシステムにシャット ダウンするという意図を示すために[IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e9a0d-122">The MAPI client calls the [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) method to indicate to the MAPI subsystem the intention to shut down.</span></span> 
        
    4. <span data-ttu-id="e9a0d-123">MAPI サブシステムは、MAPI クライアントをシャット ダウンする読み込まれた各 MAPI プロバイダーに指示します。</span><span class="sxs-lookup"><span data-stu-id="e9a0d-123">The MAPI subsystem indicates to each loaded MAPI provider that the MAPI client will shut down.</span></span> <span data-ttu-id="e9a0d-124">これらのプロバイダーを実装しているため、 **IMAPIProviderShutdown: IUnknown**インタ フェースでは、MAPI サブシステムは対応する[IMAPIProviderShutdown::NotifyProcessShutdown](imapiprovidershutdown-notifyprocessshutdown.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e9a0d-124">For those providers that have implemented the **IMAPIProviderShutdown : IUnknown** interface, the MAPI subsystem calls the corresponding [IMAPIProviderShutdown::NotifyProcessShutdown](imapiprovidershutdown-notifyprocessshutdown.md) method.</span></span> 
        
    5. <span data-ttu-id="e9a0d-125">MAPI クライアントは、MAPI サブシステムには、クライアント プロセスがすぐに終了することを示すために[IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e9a0d-125">The MAPI client calls the [IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md) method to indicate to the MAPI subsystem that the client process is exiting immediately.</span></span> 
        
    6. <span data-ttu-id="e9a0d-126">MAPI サブシステムは、MAPI クライアントのプロセスを終了すること、読み込まれた各 MAPI プロバイダーを示します。</span><span class="sxs-lookup"><span data-stu-id="e9a0d-126">The MAPI subsystem indicates to each loaded MAPI provider that the MAPI client process is exiting.</span></span> <span data-ttu-id="e9a0d-127">これらのプロバイダーを実装しているため、 **IMAPIProviderShutdown: IUnknown**インタ フェースでは、MAPI サブシステムは対応する[IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e9a0d-127">For those providers that have implemented the **IMAPIProviderShutdown : IUnknown** interface, the MAPI subsystem calls the corresponding [IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) method.</span></span> <span data-ttu-id="e9a0d-128">この時点では、これらの MAPI プロバイダーがデータと設定を保存するなど、必要なすべてのアクションがすぐにすべての参照を切断しを終了するには、MAPI クライアントのための準備の完了を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9a0d-128">At this point, these MAPI providers should verify that all necessary actions, such as saving data and settings, are complete in preparation for the MAPI client to immediately disconnect all references and exit.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="e9a0d-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="e9a0d-129">See also</span></span>

- [<span data-ttu-id="e9a0d-130">Mapi クライアントのシャット ダウン</span><span class="sxs-lookup"><span data-stu-id="e9a0d-130">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)
- [<span data-ttu-id="e9a0d-131">高速シャット ダウンのユーザー オプション</span><span class="sxs-lookup"><span data-stu-id="e9a0d-131">Fast Shutdown User Options</span></span>](fast-shutdown-user-options.md)
- [<span data-ttu-id="e9a0d-132">高速シャット ダウンのためのベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="e9a0d-132">Best Practices for Fast Shutdown</span></span>](best-practices-for-fast-shutdown.md)

