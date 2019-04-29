---
title: 高速シャットダウンのベストプラクティス
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ae8a9214-e53f-4c57-8dbe-aa7cc6903aa8
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8c7225427b80d89c6dd8adfa85f7d91885850365
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426969"
---
# <a name="best-practices-for-fast-shutdown"></a><span data-ttu-id="62bd9-103">高速シャットダウンのベストプラクティス</span><span class="sxs-lookup"><span data-stu-id="62bd9-103">Best Practices for Fast Shutdown</span></span>

  
  
<span data-ttu-id="62bd9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="62bd9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="62bd9-105">このトピックでは、管理者、mapi クライアント、および mapi プロバイダーが Windows レジストリ設定と高速シャットダウンインターフェイスを使用してクライアントのシャットダウン時のデータ損失を最小限に抑えるためのベストプラクティスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="62bd9-105">This topic recommends best practices for administrators, MAPI clients, and MAPI providers to use Windows registry settings and the fast shutdown interfaces to minimize data loss during client shutdown.</span></span>
  
- <span data-ttu-id="62bd9-106">mapi クライアントが高速シャットダウンを正常に実行するために、プロバイダープロセスがデータ損失を発生させないようにするには、まず、mapi クライアントは[IMAPIClientShutdown:: queryfastshutdown](imapiclientshutdown-queryfastshutdown.md)メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="62bd9-106">For a MAPI client to carry out fast shutdown successfully so that provider processes do not incur data loss, the MAPI client should first call the [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) method.</span></span> <span data-ttu-id="62bd9-107">その後、クライアントは、MAPI サブシステムのサポートに基づいて、 [IMAPIClientShutdown:: notifyprocessshutdown](imapiclientshutdown-notifyprocessshutdown.md)および[IMAPIClientShutdown::D ofastshutdown](imapiclientshutdown-dofastshutdown.md)メソッドを実行する必要があります。の**戻り値によって示されています。IMAPIClientShutdown:: queryfastshutdown**。</span><span class="sxs-lookup"><span data-stu-id="62bd9-107">The client should then proceed with the [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) and [IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md) methods based on the MAPI subsystem's support for fast shutdown, as indicated by the return value of **IMAPIClientShutdown::QueryFastShutdown**.</span></span> <span data-ttu-id="62bd9-108">MAPI クライアントとして、Microsoft Outlook は**IMAPIClientShutdown:: notifyprocessshutdown**または**IMAPIClientShutdown:** : **IMAPIClientShutdown:: queryfastshutdown**がエラーを返す場合は、次のように呼び出しを行いません。</span><span class="sxs-lookup"><span data-stu-id="62bd9-108">As a MAPI client, Microsoft Outlook does not call **IMAPIClientShutdown::NotifyProcessShutdown** or **IMAPIClientShutdown::DoFastShutdown** if **IMAPIClientShutdown::QueryFastShutdown** returns an error.</span></span> <span data-ttu-id="62bd9-109">管理者が Windows レジストリで高速シャットダウンを無効にした場合、MAPI サブシステムは**IMAPIClientShutdown:: queryfastshutdown**に MAPI_E_NO_SUPPORT を返します。</span><span class="sxs-lookup"><span data-stu-id="62bd9-109">If the administrator has disabled fast shutdown in the Windows registry, the MAPI subsystem would return MAPI_E_NO_SUPPORT to **IMAPIClientShutdown::QueryFastShutdown**.</span></span> <span data-ttu-id="62bd9-110">この場合、mapi サブシステムは、すぐにクライアントプロセスの終了の mapi プロバイダーに通知しません。</span><span class="sxs-lookup"><span data-stu-id="62bd9-110">In this case, the MAPI subsystem would not inform MAPI providers of an immediate client process exit.</span></span> <span data-ttu-id="62bd9-111">そのため、mapi クライアントがこのエラーを無視して、高速シャットダウンが行われ、すべての外部参照が切断されると、読み込まれたすべての mapi プロバイダーでデータが失われます。</span><span class="sxs-lookup"><span data-stu-id="62bd9-111">Therefore, if a MAPI client disregards this error return code, proceeds to do fast shutdown, and disconnects all external references, all loaded MAPI providers will have data loss.</span></span> 
    
- <span data-ttu-id="62bd9-112">MAPI プロバイダーは、クライアントが終了する前に、クライアントが外部参照を切断したことによるデータ損失を回避するために必要な手順を実行するために、 [imapiprovidershutdown: IUnknown](imapiprovidershutdowniunknown.md)インターフェイスを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="62bd9-112">MAPI providers should implement the [IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md) interface to carry out timely and necessary steps to avoid data loss due to the client disconnecting external references before the client exits.</span></span> <span data-ttu-id="62bd9-113">プロバイダーは、プライマリデータストアにデータを保存するために必須ではないすべてのものを延期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="62bd9-113">A provider should postpone everything else that is nonessential to saving data to its primary data store.</span></span> <span data-ttu-id="62bd9-114">たとえば、トランスポートプロバイダーは、新しいメールをチェックする不必要なバックグラウンド操作を延期する必要があります。アドレス帳プロバイダーは、サーバーからの最新の変更のダウンロードを延期する必要があります。また、ストアプロバイダーは、次のようなメンテナンスタスクを延期する必要があります。圧縮またはインデックス作成。</span><span class="sxs-lookup"><span data-stu-id="62bd9-114">For example, a transport provider should postpone unnecessary background operations that check for new mail, an address book provider should postpone downloading recent changes from its server, and a store provider should postpone maintenance tasks such as compacting or indexing.</span></span> 
    
- <span data-ttu-id="62bd9-115">MAPI クライアントを閉じるとすぐに終了するようにする場合は、プロバイダーが使用しない限り、高速シャットダウンを可能にする既定のレジストリ設定を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="62bd9-115">Users who want MAPI clients to exit as soon as they close them should use the default registry setting that enables fast shutdown unless a provider opts out.</span></span>
    
- <span data-ttu-id="62bd9-116">mapi クライアントが IMAPIClientShutdown を呼び出すと、 **:D ofastshutdown**は、 [MAPIUninitialize](mapiuninitialize.md)関数を含む mapi に対して追加の呼び出しを行うことはできません。</span><span class="sxs-lookup"><span data-stu-id="62bd9-116">Once a MAPI client calls **IMAPIClientShutdown::DoFastShutdown**, it should not make any additional calls to MAPI, including the [MAPIUninitialize](mapiuninitialize.md) function.</span></span> <span data-ttu-id="62bd9-117">クライアントは、クライアントプロセスの残りの期間に MAPI を使用しないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="62bd9-117">The client should not use MAPI for the rest of the client process's lifetime.</span></span> 
    
- <span data-ttu-id="62bd9-118">MAPI クライアントは、プロバイダーの**imapiprovidershutdown**インターフェイスを直接呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="62bd9-118">A MAPI client should never directly call a provider's **IMAPIProviderShutdown** interface.</span></span> <span data-ttu-id="62bd9-119">MAPI クライアントは常に[IMAPIClientShutdown: IUnknown](imapiclientshutdowniunknown.md)インターフェイスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="62bd9-119">MAPI clients should always use the [IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md) interface.</span></span> 
    
- <span data-ttu-id="62bd9-120">読み込み時に高速シャットダウンが使用されないようにする必要がある場合は、MAPI プロバイダーが**imapiprovidershutdown**インターフェイスを実装し、 **imapiprovidershutdown:: queryfastshutdown**メソッドの MAPI_E_NO_SUPPORT を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="62bd9-120">If a MAPI provider needs to ensure that fast shutdown is not used while it is loaded, it should implement the **IMAPIProviderShutdown** interface and return MAPI_E_NO_SUPPORT for the **IMAPIProviderShutdown::QueryFastShutdown** method.</span></span> <span data-ttu-id="62bd9-121">ただし、Outlook などの MAPI クライアントの場合、クライアントが高速シャットダウンを中止し、シャットダウンにかかる時間が長くなります。</span><span class="sxs-lookup"><span data-stu-id="62bd9-121">However, for MAPI clients such as Outlook, this will cause the client to abandon fast shutdown and take a longer time to shut down.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="62bd9-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="62bd9-122">See also</span></span>



[<span data-ttu-id="62bd9-123">MAPI でのクライアント シャットダウン</span><span class="sxs-lookup"><span data-stu-id="62bd9-123">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)
  
[<span data-ttu-id="62bd9-124">高速シャットダウンの概要</span><span class="sxs-lookup"><span data-stu-id="62bd9-124">Fast Shutdown Overview</span></span>](fast-shutdown-overview.md)
  
[<span data-ttu-id="62bd9-125">高速シャットダウンのユーザーオプション</span><span class="sxs-lookup"><span data-stu-id="62bd9-125">Fast Shutdown User Options</span></span>](fast-shutdown-user-options.md)

