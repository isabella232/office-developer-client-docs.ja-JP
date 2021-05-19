---
title: 高速シャットダウンのベスト プラクティス
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
# <a name="best-practices-for-fast-shutdown"></a><span data-ttu-id="2ba2d-103">高速シャットダウンのベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="2ba2d-103">Best Practices for Fast Shutdown</span></span>

  
  
<span data-ttu-id="2ba2d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ba2d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ba2d-105">このトピックでは、管理者、MAPI クライアント、MAPI プロバイダーが Windows レジストリ設定と高速シャットダウン インターフェイスを使用して、クライアントのシャットダウン時のデータ損失を最小限に抑えるためのベスト プラクティスを推奨します。</span><span class="sxs-lookup"><span data-stu-id="2ba2d-105">This topic recommends best practices for administrators, MAPI clients, and MAPI providers to use Windows registry settings and the fast shutdown interfaces to minimize data loss during client shutdown.</span></span>
  
- <span data-ttu-id="2ba2d-106">プロバイダー プロセスでデータ損失が発生しないので、MAPI クライアントが高速シャットダウンを正常に実行するには、MAPI クライアントが最初に [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="2ba2d-106">For a MAPI client to carry out fast shutdown successfully so that provider processes do not incur data loss, the MAPI client should first call the [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) method.</span></span> <span data-ttu-id="2ba2d-107">クライアントは [、IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) および [IMAPIClientShutdown::D oFastShutdown](imapiclientshutdown-dofastshutdown.md) メソッドを **、IMAPIClientShutdown::QueryFastShutdown** の戻り値で示される MAPI サブシステムの高速シャットダウンのサポートに基づいて続行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2ba2d-107">The client should then proceed with the [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) and [IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md) methods based on the MAPI subsystem's support for fast shutdown, as indicated by the return value of **IMAPIClientShutdown::QueryFastShutdown**.</span></span> <span data-ttu-id="2ba2d-108">MAPI クライアントとして、Microsoft Outlook は **IMAPIClientShutdown::NotifyProcessShutdown** または **IMAPIClientShutdown::D oFastShutdown** を呼び出す必要はありません **。IMAPIClientShutdown::QueryFastShutdown** はエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="2ba2d-108">As a MAPI client, Microsoft Outlook does not call **IMAPIClientShutdown::NotifyProcessShutdown** or **IMAPIClientShutdown::DoFastShutdown** if **IMAPIClientShutdown::QueryFastShutdown** returns an error.</span></span> <span data-ttu-id="2ba2d-109">管理者が Windows レジストリで高速シャットダウンを無効にした場合、MAPI サブシステムは **IMAPIClientShutdown::QueryFastShutdown** に MAPI_E_NO_SUPPORT を返します。</span><span class="sxs-lookup"><span data-stu-id="2ba2d-109">If the administrator has disabled fast shutdown in the Windows registry, the MAPI subsystem would return MAPI_E_NO_SUPPORT to **IMAPIClientShutdown::QueryFastShutdown**.</span></span> <span data-ttu-id="2ba2d-110">この場合、MAPI サブシステムは、MAPI プロバイダーに即時のクライアント プロセスの終了を通知しない。</span><span class="sxs-lookup"><span data-stu-id="2ba2d-110">In this case, the MAPI subsystem would not inform MAPI providers of an immediate client process exit.</span></span> <span data-ttu-id="2ba2d-111">したがって、MAPI クライアントがこのエラー戻りコードを無視し、高速シャットダウンを実行し、すべての外部参照を切断すると、読み込まれたすべての MAPI プロバイダーにデータ損失が発生します。</span><span class="sxs-lookup"><span data-stu-id="2ba2d-111">Therefore, if a MAPI client disregards this error return code, proceeds to do fast shutdown, and disconnects all external references, all loaded MAPI providers will have data loss.</span></span> 
    
- <span data-ttu-id="2ba2d-112">MAPI プロバイダーは [、IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md) インターフェイスを実装して、クライアントがクライアントを終了する前に外部参照を切断した場合のデータ損失を回避するために、必要な手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2ba2d-112">MAPI providers should implement the [IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md) interface to carry out timely and necessary steps to avoid data loss due to the client disconnecting external references before the client exits.</span></span> <span data-ttu-id="2ba2d-113">プロバイダーは、データをプライマリ データ ストアに保存する必要がない他のすべてを延期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2ba2d-113">A provider should postpone everything else that is nonessential to saving data to its primary data store.</span></span> <span data-ttu-id="2ba2d-114">たとえば、トランスポート プロバイダーは、新しいメールをチェックする不要なバックグラウンド操作を延期し、アドレス帳プロバイダーはサーバーからの最近の変更のダウンロードを延期し、ストア プロバイダーは圧縮やインデックス作成などのメンテナンス タスクを延期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2ba2d-114">For example, a transport provider should postpone unnecessary background operations that check for new mail, an address book provider should postpone downloading recent changes from its server, and a store provider should postpone maintenance tasks such as compacting or indexing.</span></span> 
    
- <span data-ttu-id="2ba2d-115">MAPI クライアントを閉じるとすぐに終了するユーザーは、プロバイダーがオプトアウトしない限り、高速シャットダウンを有効にする既定のレジストリ設定を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2ba2d-115">Users who want MAPI clients to exit as soon as they close them should use the default registry setting that enables fast shutdown unless a provider opts out.</span></span>
    
- <span data-ttu-id="2ba2d-116">MAPI クライアントが **IMAPIClientShutdown::D oFastShutdown** を呼び出したら [、MAPIUninitialize](mapiuninitialize.md) 関数を含む MAPI への追加の呼び出しを行う必要はありません。</span><span class="sxs-lookup"><span data-stu-id="2ba2d-116">Once a MAPI client calls **IMAPIClientShutdown::DoFastShutdown**, it should not make any additional calls to MAPI, including the [MAPIUninitialize](mapiuninitialize.md) function.</span></span> <span data-ttu-id="2ba2d-117">クライアントは、クライアント プロセスの残りの期間、MAPI を使用しなく必要があります。</span><span class="sxs-lookup"><span data-stu-id="2ba2d-117">The client should not use MAPI for the rest of the client process's lifetime.</span></span> 
    
- <span data-ttu-id="2ba2d-118">MAPI クライアントは、プロバイダーの **IMAPIProviderShutdown インターフェイスを直接呼び出す必要** があります。</span><span class="sxs-lookup"><span data-stu-id="2ba2d-118">A MAPI client should never directly call a provider's **IMAPIProviderShutdown** interface.</span></span> <span data-ttu-id="2ba2d-119">MAPI クライアントは常に [IMAPIClientShutdown : IUnknown インターフェイスを使用する必要](imapiclientshutdowniunknown.md) があります。</span><span class="sxs-lookup"><span data-stu-id="2ba2d-119">MAPI clients should always use the [IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md) interface.</span></span> 
    
- <span data-ttu-id="2ba2d-120">MAPI プロバイダーが読み込み中に高速シャットダウンが使用されない必要がある場合は **、IMAPIProviderShutdown インターフェイスを実装し、IMAPIProviderShutdown::QueryFastShutdown** メソッドの MAPI_E_NO_SUPPORT を返す必要があります。 </span><span class="sxs-lookup"><span data-stu-id="2ba2d-120">If a MAPI provider needs to ensure that fast shutdown is not used while it is loaded, it should implement the **IMAPIProviderShutdown** interface and return MAPI_E_NO_SUPPORT for the **IMAPIProviderShutdown::QueryFastShutdown** method.</span></span> <span data-ttu-id="2ba2d-121">ただし、MAPI クライアント (Outlookなど) の場合、クライアントは高速シャットダウンを放棄し、シャットダウンに時間がかかります。</span><span class="sxs-lookup"><span data-stu-id="2ba2d-121">However, for MAPI clients such as Outlook, this will cause the client to abandon fast shutdown and take a longer time to shut down.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="2ba2d-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="2ba2d-122">See also</span></span>



[<span data-ttu-id="2ba2d-123">MAPI でのクライアント シャットダウン</span><span class="sxs-lookup"><span data-stu-id="2ba2d-123">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)
  
[<span data-ttu-id="2ba2d-124">高速シャットダウンの概要</span><span class="sxs-lookup"><span data-stu-id="2ba2d-124">Fast Shutdown Overview</span></span>](fast-shutdown-overview.md)
  
[<span data-ttu-id="2ba2d-125">Fast Shutdown User Options</span><span class="sxs-lookup"><span data-stu-id="2ba2d-125">Fast Shutdown User Options</span></span>](fast-shutdown-user-options.md)

