---
title: 高速シャットダウンのユーザー オプション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
api_type:
- COM
ms.assetid: 220aeab5-20f6-4520-96c9-8aaa0e8ea15b
description: '最終更新日: 2012 年 6 月 26 日'
localization_priority: Priority
ms.openlocfilehash: 3c60862733c6b38e60650ae9daba9bba578fcd58
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716370"
---
# <a name="fast-shutdown-user-options"></a><span data-ttu-id="8f2d3-103">高速シャットダウンのユーザー オプション</span><span class="sxs-lookup"><span data-stu-id="8f2d3-103">Fast shutdown user options</span></span>

<span data-ttu-id="8f2d3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8f2d3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8f2d3-105">このトピックでは、ユーザーの MAPI クライアントを高速シャットダウンするための 3 つの Windows レジストリ設定について説明します。この設定は、この設定は、Microsoft Outlook 2010 から現在の Microsoft Outlook 2013 で使用できます。</span><span class="sxs-lookup"><span data-stu-id="8f2d3-105">This topic describes the three Windows registry settings that are available, starting in Microsoft Outlook 2010 and now including Microsoft Outlook 2013, for fast shutdown of a user's MAPI clients.</span></span> <span data-ttu-id="8f2d3-106">この 3 つのレジストリ設定を使用することで、管理者はクライアントの高速シャットダウンに対する MAPI プロバイダーのサポートに応じて優先されるクライアント シャットダウン動作を指定できます。</span><span class="sxs-lookup"><span data-stu-id="8f2d3-106">Administrators can use these registry settings to specify the preferred client shutdown behavior depending on the MAPI providers' support for client fast shutdown.</span></span> <span data-ttu-id="8f2d3-107">管理者の設定により、MAPI サブシステムが [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) に対する MAPI クライアントの呼び出しに利用可能な高速シャットダウンのサポートに関して応答する方法が決まります。</span><span class="sxs-lookup"><span data-stu-id="8f2d3-107">The administrator's setting, in turn, determines how the MAPI subsystem responds to the MAPI client's call to [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) in terms of available fast shutdown support.</span></span> 
  
<span data-ttu-id="8f2d3-108">レジストリ設定は、すべての MAPI クライアントの高速シャットダウンに対する管理者の優先設定をユーザー レベルで反映しますが、MAPI クライアントの開発者は、その他の MAPI クライアントの設定および管理者のレジストリ設定とは無関係に、クライアントで高速シャットダウンをサポートするかどうかを決定できます。</span><span class="sxs-lookup"><span data-stu-id="8f2d3-108">Even though a registry setting reflects the administrator's preference at the user level for fast shutdown for all MAPI clients, a MAPI client developer can decide whether the client supports fast shutdown independently of other MAPI clients and the administrator's registry setting.</span></span> <span data-ttu-id="8f2d3-109">ただし、高速シャットダウンを正常に実施するには、ユーザーが必要なレジストリ設定を保持し、MAPI クライアントが [IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md) インターフェイスを使用して高速シャットダウンを開始し、クライアントと連携する MAPI プロバイダーはクライアントの高速シャットダウンをサポートする [IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md) インターフェイスを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f2d3-109">Nonetheless, for fast shutdown to take place successfully, the user must have the necessary registry setting, a MAPI client must initiate the fast shutdown by using the [IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md) interface, and MAPI providers that work with the client should implement the [IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md) interface to support client fast shutdown.</span></span> 
  
<span data-ttu-id="8f2d3-110">次に、これら 3 つのユーザー レベルのオプションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="8f2d3-110">The following list describes the three user-level options.</span></span>
  
### <a name="option-1-the-mapi-subsystem-enables-fast-shutdown-unless-mapi-providers-explicitly-opt-out"></a><span data-ttu-id="8f2d3-111">オプション 1: MAPI サブシステムで高速シャットダウンを有効にする (ただし、MAPI プロバイダーが明示的に無効にしている場合を除く)</span><span class="sxs-lookup"><span data-stu-id="8f2d3-111">Option 1: The MAPI subsystem enables fast shutdown, unless MAPI providers explicitly opt out</span></span> 
    
<span data-ttu-id="8f2d3-112">Outlook 2010 以降、Outlook が MAPI クライアントのときには、この動作が既定の動作になります。これは、その他の MAPI クライアントの既定の動作ではない場合があります。</span><span class="sxs-lookup"><span data-stu-id="8f2d3-112">Starting in Outlook 2010, this is the default behavior when Outlook is the MAPI client; it is not necessarily the default behavior for other MAPI clients.</span></span> <span data-ttu-id="8f2d3-113">このオプションを Outlook に明示的に指定するために、管理者は次のレジストリ キーと値を設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="8f2d3-113">To explicitly specify this option for Outlook, administrators can choose to set the following registry key and value.</span></span>
    
<span data-ttu-id="8f2d3-114">レジストリ キー:</span><span class="sxs-lookup"><span data-stu-id="8f2d3-114">Registry Key</span></span>
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
<span data-ttu-id="8f2d3-115">値:</span><span class="sxs-lookup"><span data-stu-id="8f2d3-115">Value</span></span>
  
>  `"FastShutdownBehavior"=dword:00000000`
    
<span data-ttu-id="8f2d3-116">MAPI クライアントが高速シャットダウンを開始し、高速シャットダウンのサポートについてクエリするために **IMAPIClientShutdown::QueryFastShutdown** を呼び出すと、MAPI サブシステムは、S\_OK を返すことでクエリに応答します。ただし、MAPI クライアントとのアクティブな MAPI セッションを持つ MAPI プロバイダーが高速シャットダウンのサポートを明示的に無効にしている場合を除きます。</span><span class="sxs-lookup"><span data-stu-id="8f2d3-116">When a MAPI client initiates a fast shutdown and calls **IMAPIClientShutdown::QueryFastShutdown** to query for fast shutdown support, the MAPI subsystem responds to the query by returning S\_OK as long as no MAPI provider that has an active MAPI session with the MAPI client has explicitly opted out of fast shutdown support.</span></span> 

<span data-ttu-id="8f2d3-117">MAPI プロバイダーは、エラー (MAPI\_E\_NO\_SUPPORT) を返す [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) メソッドを実装することで、高速シャットダウンを無効にします。</span><span class="sxs-lookup"><span data-stu-id="8f2d3-117">A MAPI provider opts out of fast shutdown by implementing the [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) method to return an error (MAPI\_E\_NO\_SUPPORT).</span></span> <span data-ttu-id="8f2d3-118">1 つ以上の MAPI プロバイダーが **IMAPIProviderShutdown::QueryFastShutdown** でエラーを返すと、MAPI サブシステムは **IMAPIClientShutdown::QueryFastShutdown** に MAPI_\E_\NO\_SUPPORT を返します。</span><span class="sxs-lookup"><span data-stu-id="8f2d3-118">If one or more MAPI providers return an error in **IMAPIProviderShutdown::QueryFastShutdown**, the MAPI subsystem returns MAPI_\E_\NO\_SUPPORT to **IMAPIClientShutdown::QueryFastShutdown**.</span></span> 

<span data-ttu-id="8f2d3-119">MAPI プロバイダーが無効にしていない限り、1 つ以上のプロバイダーが **IMAPIProviderShutdown : IUnknown** を実装していない場合でも、MAPI サブシステムは S\_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="8f2d3-119">Unless a MAPI provider opts out, the MAPI subsystem returns S\_OK, even if one or more providers have not implemented the **IMAPIProviderShutdown : IUnknown** interface.</span></span> 
    
### <a name="option-2-the-mapi-subsystem-enables-fast-shutdown-only-if-every-mapi-provider-explicitly-opts-in"></a><span data-ttu-id="8f2d3-120">オプション 2: すべての MAPI プロバイダーが明示的に有効化している場合にのみ MAPI サブシステムで高速シャットダウンを有効にする</span><span class="sxs-lookup"><span data-stu-id="8f2d3-120">Option 2: The MAPI subsystem enables fast shutdown only if every MAPI provider explicitly opts in</span></span> 
    
<span data-ttu-id="8f2d3-121">管理者は、この優先設定をクライアントの高速シャットダウンに指定するために、次のレジストリ キーと値を明示的に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f2d3-121">Administrators must explicitly set the following registry key and value to specify this preference for client fast shutdown.</span></span>
    
<span data-ttu-id="8f2d3-122">レジストリ キー:</span><span class="sxs-lookup"><span data-stu-id="8f2d3-122">Registry Key</span></span>
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
<span data-ttu-id="8f2d3-123">値:</span><span class="sxs-lookup"><span data-stu-id="8f2d3-123">Value</span></span>
  
>  `"FastShutdownBehavior"=dword:00000001`
    
<span data-ttu-id="8f2d3-124">MAPI クライアントが高速シャットダウンを開始し、高速シャットダウンのサポートについてクエリするために **IMAPIClientShutdown::QueryFastShutdown** を呼び出すと、MAPI サブシステムは、MAPI クライアントとのアクティブな MAPI セッションを持つすべての MAPI プロバイダーが高速シャットダウンをサポートしている場合に S\_OK を返すことでクエリに応答します。</span><span class="sxs-lookup"><span data-stu-id="8f2d3-124">When a MAPI client initiates a fast shutdown and calls **IMAPIClientShutdown::QueryFastShutdown** to query for fast shutdown support, the MAPI subsystem responds to the query by returning S\_OK if all MAPI providers that have active sessions with the MAPI client support fast shutdown.</span></span> <span data-ttu-id="8f2d3-125">MAPI プロバイダーは、エラーではないコード (S\_OK) を返す **IMAPIProviderShutdown::QueryFastShutdown** を実装することで、サポートしていることを示します。</span><span class="sxs-lookup"><span data-stu-id="8f2d3-125">A MAPI provider demonstrates its support by implementing **IMAPIProviderShutdown::QueryFastShutdown** to return a non-error code (S\_OK).</span></span> 

<span data-ttu-id="8f2d3-126">1 つ以上の MAPI プロバイダーが MAPI\_E\_NO\_SUPPORT を返した場合や、**IMAPIProviderShutdown::QueryFastShutdown** を実装していない場合、MAPI サブシステムは **IMAPIClientShutdown::QueryFastShutdown** にエラー コードを返します。</span><span class="sxs-lookup"><span data-stu-id="8f2d3-126">If one or more such MAPI providers return MAPI\_E\_NO\_SUPPORT, or do not implement **IMAPIProviderShutdown::QueryFastShutdown**, the MAPI subsystem returns an error code to **IMAPIClientShutdown::QueryFastShutdown**.</span></span>
    
### <a name="option-3-an-administrator-disables-support-for-client-fast-shutdown"></a><span data-ttu-id="8f2d3-127">オプション 3: 管理者がクライアントの高速シャットダウンを無効にする</span><span class="sxs-lookup"><span data-stu-id="8f2d3-127">Option 3: An administrator disables support for client fast shutdown</span></span>
    
<span data-ttu-id="8f2d3-128">管理者は、クライアントの高速シャットダウンを無効にするために、次のレジストリ キーと値を明示的に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f2d3-128">Administrators must explicitly set the following registry key and value to disable support for client fast shutdown.</span></span>
    
<span data-ttu-id="8f2d3-129">レジストリ キー:</span><span class="sxs-lookup"><span data-stu-id="8f2d3-129">Registry Key</span></span>
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
<span data-ttu-id="8f2d3-130">値:</span><span class="sxs-lookup"><span data-stu-id="8f2d3-130">Value</span></span>
  
>  `"FastShutdownBehavior"=dword:00000002`
    
<span data-ttu-id="8f2d3-131">MAPI クライアントが高速シャットダウンを開始し、高速シャットダウンのサポートについてクエリするために **IMAPIClientShutdown::QueryFastShutdown** を呼び出すと、MAPI サブシステムは、MAPI プロバイダーが高速シャットダウンをサポートしているかどうかに関係なく MAPI_E_NO_SUPPORT を返すことでクエリに応答します。</span><span class="sxs-lookup"><span data-stu-id="8f2d3-131">When a MAPI client initiates a fast shutdown and calls **IMAPIClientShutdown::QueryFastShutdown** to query for fast shutdown support, the MAPI subsystem responds to the query by returning MAPI_E_NO_SUPPORT, regardless of whether any MAPI provider supports fast shutdown.</span></span> <span data-ttu-id="8f2d3-132">このレジストリ設定により、MAPI サブシステムはプロバイダーの **IMAPIProviderShutdown::QueryFastShutdown** メソッドまたは [IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) メソッドを呼び出さなくなります。</span><span class="sxs-lookup"><span data-stu-id="8f2d3-132">Under this registry setting, the MAPI subsystem never calls the **IMAPIProviderShutdown::QueryFastShutdown** or [IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) method of any of the providers.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="8f2d3-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="8f2d3-133">See also</span></span>

- [<span data-ttu-id="8f2d3-134">MAPI でのクライアント シャットダウン</span><span class="sxs-lookup"><span data-stu-id="8f2d3-134">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)
- [<span data-ttu-id="8f2d3-135">高速シャットダウンの概要</span><span class="sxs-lookup"><span data-stu-id="8f2d3-135">Fast shutdown overview</span></span>](fast-shutdown-overview.md)
- [<span data-ttu-id="8f2d3-136">高速シャットダウンのためのベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="8f2d3-136">Best practices for fast shutdown</span></span>](best-practices-for-fast-shutdown.md)

