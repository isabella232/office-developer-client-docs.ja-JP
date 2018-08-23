---
title: 高速シャット ダウンのユーザー オプション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 220aeab5-20f6-4520-96c9-8aaa0e8ea15b
description: '最終更新日: 2012 年 6 月 26 日'
ms.openlocfilehash: a58f8b98ab2f5a5c1028440676a561427272d028
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800031"
---
# <a name="fast-shutdown-user-options"></a><span data-ttu-id="d9821-103">高速シャット ダウンのユーザー オプション</span><span class="sxs-lookup"><span data-stu-id="d9821-103">Fast shutdown user options</span></span>

<span data-ttu-id="d9821-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d9821-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d9821-105">このトピックでは、3 つ Windows レジストリ設定、使用可能な Microsoft Outlook 2010 で起動して、Microsoft Outlook 2013 では、ユーザーの MAPI クライアントの高速シャット ダウンを含むについて説明します。</span><span class="sxs-lookup"><span data-stu-id="d9821-105">This topic describes the three Windows registry settings that are available, starting in Microsoft Outlook 2010 and now including Microsoft Outlook 2013, for fast shutdown of a user's MAPI clients.</span></span> <span data-ttu-id="d9821-106">管理者は、クライアントの高速シャット ダウンの MAPI プロバイダーのサポートによって優先するクライアントのシャット ダウン動作を指定するのにこれらのレジストリ設定を使用できます。</span><span class="sxs-lookup"><span data-stu-id="d9821-106">Administrators can use these registry settings to specify the preferred client shutdown behavior depending on the MAPI providers' support for client fast shutdown.</span></span> <span data-ttu-id="d9821-107">管理者の設定には、MAPI サブシステムが高速シャット ダウンの利用可能なサポートの観点から[IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md)の MAPI クライアントの呼び出しに応答する方法を決定します。</span><span class="sxs-lookup"><span data-stu-id="d9821-107">The administrator's setting, in turn, determines how the MAPI subsystem responds to the MAPI client's call to [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) in terms of available fast shutdown support.</span></span> 
  
<span data-ttu-id="d9821-108">MAPI クライアントの開発者が、クライアントがその他の MAPI クライアントとは別に高速シャット ダウンをサポートしているかどうかを決定できる場合でも、レジストリの設定では、すべての MAPI クライアントの高速シャット ダウンのユーザー レベルでの管理者の設定を反映と管理者のレジストリ設定です。</span><span class="sxs-lookup"><span data-stu-id="d9821-108">Even though a registry setting reflects the administrator's preference at the user level for fast shutdown for all MAPI clients, a MAPI client developer can decide whether the client supports fast shutdown independently of other MAPI clients and the administrator's registry setting.</span></span> <span data-ttu-id="d9821-109">とはいえ、正常に実行するのには高速シャット ダウンのユーザーは、必要なレジストリ設定を持つ必要があります、MAPI クライアントを使用して、高速シャット ダウンを開始する必要があります、 [IMAPIClientShutdown: IUnknown](imapiclientshutdowniunknown.md)インターフェイス、および MAPI プロバイダーと連携する、クライアントを実装する必要があります、 [IMAPIProviderShutdown: IUnknown](imapiprovidershutdowniunknown.md)クライアントの高速シャット ダウンをサポートするインターフェイス。</span><span class="sxs-lookup"><span data-stu-id="d9821-109">Nonetheless, for fast shutdown to take place successfully, the user must have the necessary registry setting, a MAPI client must initiate the fast shutdown by using the [IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md) interface, and MAPI providers that work with the client should implement the [IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md) interface to support client fast shutdown.</span></span> 
  
<span data-ttu-id="d9821-110">次の一覧では、ユーザー レベルの 3 つのオプションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="d9821-110">The following list describes the three user-level options.</span></span>
  
### <a name="option-1-the-mapi-subsystem-enables-fast-shutdown-unless-mapi-providers-explicitly-opt-out"></a><span data-ttu-id="d9821-111">オプション 1: MAPI のサブシステムにより、高速シャット ダウン MAPI プロバイダーが明示的に選択しない限り、</span><span class="sxs-lookup"><span data-stu-id="d9821-111">Option 1: The MAPI subsystem enables fast shutdown, unless MAPI providers explicitly opt out</span></span> 
    
<span data-ttu-id="d9821-112">開始すると、Outlook 2010 では、これは、Outlook が MAPI クライアントの場合それは必ずしも他の MAPI クライアントの既定の動作ではありません。</span><span class="sxs-lookup"><span data-stu-id="d9821-112">Starting in Outlook 2010, this is the default behavior when Outlook is the MAPI client; it is not necessarily the default behavior for other MAPI clients.</span></span> <span data-ttu-id="d9821-113">Outlook でこのオプションを明示的に指定するには、管理者は、次のレジストリ キーと値を設定するのには選択できます。</span><span class="sxs-lookup"><span data-stu-id="d9821-113">To explicitly specify this option for Outlook, administrators can choose to set the following registry key and value.</span></span>
    
<span data-ttu-id="d9821-114">レジストリ キー:</span><span class="sxs-lookup"><span data-stu-id="d9821-114">Registry key:</span></span>
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
<span data-ttu-id="d9821-115">値:</span><span class="sxs-lookup"><span data-stu-id="d9821-115">Value:</span></span>
  
>  `"FastShutdownBehavior"=dword:00000000`
    
<span data-ttu-id="d9821-116">返すことによって、MAPI サブシステムがクエリに応答の MAPI クライアントでは、高速シャット ダウンを開始し、高速シャット ダウンをサポートするため、クエリするために**IMAPIClientShutdown::QueryFastShutdown**を呼び出す、ときに S\_限り、アクティブな MAPI いる MAPI プロバイダーがありません [ok]MAPI クライアントとのセッションが高速シャット ダウンのサポートを選択して明示的にします。</span><span class="sxs-lookup"><span data-stu-id="d9821-116">When a MAPI client initiates a fast shutdown and calls **IMAPIClientShutdown::QueryFastShutdown** to query for fast shutdown support, the MAPI subsystem responds to the query by returning S\_OK as long as no MAPI provider that has an active MAPI session with the MAPI client has explicitly opted out of fast shutdown support.</span></span> 

<span data-ttu-id="d9821-117">MAPI プロバイダーがエラーを返す[IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md)メソッドを実装することにより高速シャット ダウンを選んだ (MAPI\_E\_NO\_のサポート)。</span><span class="sxs-lookup"><span data-stu-id="d9821-117">A MAPI provider opts out of fast shutdown by implementing the [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) method to return an error (MAPI\_E\_NO\_SUPPORT).</span></span> <span data-ttu-id="d9821-118">MAPI サブシステムが MAPI_\E_\NO を返す場合は 1 つまたは複数の MAPI プロバイダーは、 **IMAPIProviderShutdown::QueryFastShutdown**でエラーを返す、\_ **IMAPIClientShutdown::QueryFastShutdown**をサポートします。</span><span class="sxs-lookup"><span data-stu-id="d9821-118">If one or more MAPI providers return an error in **IMAPIProviderShutdown::QueryFastShutdown**, the MAPI subsystem returns MAPI_\E_\NO\_SUPPORT to **IMAPIClientShutdown::QueryFastShutdown**.</span></span> 

<span data-ttu-id="d9821-119">MAPI プロバイダーが、MAPI のサブシステムを返します S を選んだ場合を除き、\_確かに、1 つまたは複数のプロバイダーを実装していない場合でも、 **IMAPIProviderShutdown: IUnknown**インタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="d9821-119">Unless a MAPI provider opts out, the MAPI subsystem returns S\_OK, even if one or more providers have not implemented the **IMAPIProviderShutdown : IUnknown** interface.</span></span> 
    
### <a name="option-2-the-mapi-subsystem-enables-fast-shutdown-only-if-every-mapi-provider-explicitly-opts-in"></a><span data-ttu-id="d9821-120">オプション 2: MAPI のサブシステムにより、高速シャット ダウンのすべての MAPI プロバイダーが明示的に選んだ場合にのみ</span><span class="sxs-lookup"><span data-stu-id="d9821-120">Option 2: The MAPI subsystem enables fast shutdown only if every MAPI provider explicitly opts in</span></span> 
    
<span data-ttu-id="d9821-121">管理者は、次のレジストリ キーおよびクライアントの高速シャット ダウンの環境設定を指定する値を明示的に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9821-121">Administrators must explicitly set the following registry key and value to specify this preference for client fast shutdown.</span></span>
    
<span data-ttu-id="d9821-122">レジストリ キー:</span><span class="sxs-lookup"><span data-stu-id="d9821-122">Registry key:</span></span>
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
<span data-ttu-id="d9821-123">値:</span><span class="sxs-lookup"><span data-stu-id="d9821-123">Value:</span></span>
  
>  `"FastShutdownBehavior"=dword:00000001`
    
<span data-ttu-id="d9821-124">返すことによって、MAPI サブシステムがクエリに応答の MAPI クライアントでは、高速シャット ダウンを開始し、高速シャット ダウンをサポートするため、クエリするために**IMAPIClientShutdown::QueryFastShutdown**を呼び出す、ときに S\_すべての MAPI プロバイダーがアクティブなセッションがある場合に [ok]MAPI クライアント サポート高速シャット ダウンします。</span><span class="sxs-lookup"><span data-stu-id="d9821-124">When a MAPI client initiates a fast shutdown and calls **IMAPIClientShutdown::QueryFastShutdown** to query for fast shutdown support, the MAPI subsystem responds to the query by returning S\_OK if all MAPI providers that have active sessions with the MAPI client support fast shutdown.</span></span> <span data-ttu-id="d9821-125">MAPI プロバイダーがエラーのないコードを返すには、 **IMAPIProviderShutdown::QueryFastShutdown**を実装することでのサポートを示します (S\_[ok])。</span><span class="sxs-lookup"><span data-stu-id="d9821-125">A MAPI provider demonstrates its support by implementing **IMAPIProviderShutdown::QueryFastShutdown** to return a non-error code (S\_OK).</span></span> 

<span data-ttu-id="d9821-126">このような MAPI プロバイダーが 1 つまたは複数が MAPI を返す場合は、\_E\_NO\_のサポート、または**IMAPIProviderShutdown::QueryFastShutdown**を実装していない MAPI サブシステムは、 **IMAPIClientShutdown::QueryFastShutdown**にエラー コードを返します.</span><span class="sxs-lookup"><span data-stu-id="d9821-126">If one or more such MAPI providers return MAPI\_E\_NO\_SUPPORT, or do not implement **IMAPIProviderShutdown::QueryFastShutdown**, the MAPI subsystem returns an error code to **IMAPIClientShutdown::QueryFastShutdown**.</span></span>
    
### <a name="option-3-an-administrator-disables-support-for-client-fast-shutdown"></a><span data-ttu-id="d9821-127">オプション 3: 管理者はクライアントの高速シャット ダウンのサポートを無効にします</span><span class="sxs-lookup"><span data-stu-id="d9821-127">Option 3: An administrator disables support for client fast shutdown</span></span>
    
<span data-ttu-id="d9821-128">管理者は、次のレジストリ キーと値をクライアントの高速シャット ダウンのサポートを無効にするを明示的に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9821-128">Administrators must explicitly set the following registry key and value to disable support for client fast shutdown.</span></span>
    
<span data-ttu-id="d9821-129">レジストリ キー:</span><span class="sxs-lookup"><span data-stu-id="d9821-129">Registry key:</span></span>
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
<span data-ttu-id="d9821-130">値:</span><span class="sxs-lookup"><span data-stu-id="d9821-130">Value:</span></span>
  
>  `"FastShutdownBehavior"=dword:00000002`
    
<span data-ttu-id="d9821-131">かどうかに関係なく、MAPI_E_NO_SUPPORT を返すことによって、MAPI サブシステムがクエリに応答と、MAPI クライアントは、高速シャット ダウンを開始し、クエリを高速シャット ダウンをサポートするため**IMAPIClientShutdown::QueryFastShutdown**を呼び出して、任意の MAPI プロバイダーサポートには、シャット ダウンが高速です。</span><span class="sxs-lookup"><span data-stu-id="d9821-131">When a MAPI client initiates a fast shutdown and calls **IMAPIClientShutdown::QueryFastShutdown** to query for fast shutdown support, the MAPI subsystem responds to the query by returning MAPI_E_NO_SUPPORT, regardless of whether any MAPI provider supports fast shutdown.</span></span> <span data-ttu-id="d9821-132">このレジストリ設定は、[MAPI サブシステムは決して任意のプロバイダーの**IMAPIProviderShutdown::QueryFastShutdown**または[IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d9821-132">Under this registry setting, the MAPI subsystem never calls the **IMAPIProviderShutdown::QueryFastShutdown** or [IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) method of any of the providers.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="d9821-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="d9821-133">See also</span></span>

- [<span data-ttu-id="d9821-134">Mapi クライアントのシャット ダウン</span><span class="sxs-lookup"><span data-stu-id="d9821-134">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)
- [<span data-ttu-id="d9821-135">高速シャットダウンの概要</span><span class="sxs-lookup"><span data-stu-id="d9821-135">Fast Shutdown Overview</span></span>](fast-shutdown-overview.md)
- [<span data-ttu-id="d9821-136">高速シャットダウンのためのベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="d9821-136">Best Practices for Fast Shutdown</span></span>](best-practices-for-fast-shutdown.md)

