---
title: 高速シャットダウンのためのベスト プラクティス
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ae8a9214-e53f-4c57-8dbe-aa7cc6903aa8
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: c92347ab1a786196e7f0d99b286e8f4134ce7c24
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590702"
---
# <a name="best-practices-for-fast-shutdown"></a><span data-ttu-id="8e537-103">高速シャットダウンのためのベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="8e537-103">Best Practices for Fast Shutdown</span></span>

  
  
<span data-ttu-id="8e537-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e537-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e537-105">このトピックでは、管理者、MAPI クライアントでは、および MAPI プロバイダーがクライアントのシャット ダウン時にデータの損失を最小限に抑えるため、Windows レジストリの設定と高速シャット ダウン インターフェイスを使用するためのベスト プラクティスを推奨します。</span><span class="sxs-lookup"><span data-stu-id="8e537-105">This topic recommends best practices for administrators, MAPI clients, and MAPI providers to use Windows registry settings and the fast shutdown interfaces to minimize data loss during client shutdown.</span></span>
  
- <span data-ttu-id="8e537-106">プロバイダーのプロセスは、データの損失を引き起こさないように、高速シャット ダウンを正常に実行するための MAPI クライアントの MAPI クライアントは最初に[IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md)メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="8e537-106">For a MAPI client to carry out fast shutdown successfully so that provider processes do not incur data loss, the MAPI client should first call the [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) method.</span></span> <span data-ttu-id="8e537-107">クライアントし、どうすべき、高速シャット ダウンは、MAPI サブシステムのサポートに基づいた[IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md)と[IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md)メソッドを使用して**の戻り値によって示されるIMAPIClientShutdown::QueryFastShutdown**。</span><span class="sxs-lookup"><span data-stu-id="8e537-107">The client should then proceed with the [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) and [IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md) methods based on the MAPI subsystem's support for fast shutdown, as indicated by the return value of **IMAPIClientShutdown::QueryFastShutdown**.</span></span> <span data-ttu-id="8e537-108">MAPI クライアントとして Microsoft Outlook は呼び出しません**IMAPIClientShutdown::NotifyProcessShutdown**または**IMAPIClientShutdown::DoFastShutdown** **IMAPIClientShutdown::QueryFastShutdown**には、エラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="8e537-108">As a MAPI client, Microsoft Outlook does not call **IMAPIClientShutdown::NotifyProcessShutdown** or **IMAPIClientShutdown::DoFastShutdown** if **IMAPIClientShutdown::QueryFastShutdown** returns an error.</span></span> <span data-ttu-id="8e537-109">管理者は Windows レジストリの高速シャット ダウンを無効にした場合、MAPI サブシステムは**IMAPIClientShutdown::QueryFastShutdown**に MAPI_E_NO_SUPPORT を返します。</span><span class="sxs-lookup"><span data-stu-id="8e537-109">If the administrator has disabled fast shutdown in the Windows registry, the MAPI subsystem would return MAPI_E_NO_SUPPORT to **IMAPIClientShutdown::QueryFastShutdown**.</span></span> <span data-ttu-id="8e537-110">この例では、MAPI サブシステムが通知 MAPI プロバイダーを直接クライアント プロセスの終了。</span><span class="sxs-lookup"><span data-stu-id="8e537-110">In this case, the MAPI subsystem would not inform MAPI providers of an immediate client process exit.</span></span> <span data-ttu-id="8e537-111">したがって、MAPI クライアントは、このエラー コードを無視、高速シャット ダウンの操作を行いますに進み、すべての外部参照を切断、読み込まれているすべての MAPI プロバイダーはデータの損失があります。</span><span class="sxs-lookup"><span data-stu-id="8e537-111">Therefore, if a MAPI client disregards this error return code, proceeds to do fast shutdown, and disconnects all external references, all loaded MAPI providers will have data loss.</span></span> 
    
- <span data-ttu-id="8e537-112">MAPI プロバイダーを実装する必要があります、 [IMAPIProviderShutdown: IUnknown](imapiprovidershutdowniunknown.md)クライアントを終了する前に、外部参照を切断するクライアントによるデータの損失を避けるために、タイムリーかつ必要な手順を実行するインターフェイス。</span><span class="sxs-lookup"><span data-stu-id="8e537-112">MAPI providers should implement the [IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md) interface to carry out timely and necessary steps to avoid data loss due to the client disconnecting external references before the client exits.</span></span> <span data-ttu-id="8e537-113">プロバイダーは、プライマリ ・ データ ・ ストアにデータを保存するのには重要ではないその他のすべてを延期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8e537-113">A provider should postpone everything else that is nonessential to saving data to its primary data store.</span></span> <span data-ttu-id="8e537-114">たとえば、トランスポート プロバイダーは、新しいメールは、アドレス帳プロバイダーが、サーバーから最新の変更のダウンロードを延期する必要があります。 を確認する不要なバック グラウンド操作を延期する必要があり。、ストア プロバイダーは次のように保守タスクを延期する必要があります。最適化するか、インデックスを作成します。</span><span class="sxs-lookup"><span data-stu-id="8e537-114">For example, a transport provider should postpone unnecessary background operations that check for new mail, an address book provider should postpone downloading recent changes from its server, and a store provider should postpone maintenance tasks such as compacting or indexing.</span></span> 
    
- <span data-ttu-id="8e537-115">MAPI クライアントがそれらを閉じるとすぐに終了したいユーザーは、プロバイダーの選択しない限り、高速シャット ダウンを有効にするデフォルトのレジストリ設定を使用してください。</span><span class="sxs-lookup"><span data-stu-id="8e537-115">Users who want MAPI clients to exit as soon as they close them should use the default registry setting that enables fast shutdown unless a provider opts out.</span></span>
    
- <span data-ttu-id="8e537-116">MAPI クライアントは、 **IMAPIClientShutdown::DoFastShutdown**を呼び出すと MAPI、 [MAPIUninitialize](mapiuninitialize.md)関数を含む、追加の呼び出しは作成しないでください。</span><span class="sxs-lookup"><span data-stu-id="8e537-116">Once a MAPI client calls **IMAPIClientShutdown::DoFastShutdown**, it should not make any additional calls to MAPI, including the [MAPIUninitialize](mapiuninitialize.md) function.</span></span> <span data-ttu-id="8e537-117">クライアントは、クライアント プロセスの有効期間の残りの部分に MAPI を使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="8e537-117">The client should not use MAPI for the rest of the client process's lifetime.</span></span> 
    
- <span data-ttu-id="8e537-118">MAPI クライアントは、プロバイダーの**IMAPIProviderShutdown**インターフェイスを直接呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="8e537-118">A MAPI client should never directly call a provider's **IMAPIProviderShutdown** interface.</span></span> <span data-ttu-id="8e537-119">常に MAPI クライアントを使用する必要があります、 [IMAPIClientShutdown: IUnknown](imapiclientshutdowniunknown.md)インタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="8e537-119">MAPI clients should always use the [IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md) interface.</span></span> 
    
- <span data-ttu-id="8e537-120">MAPI プロバイダーが読み込まれるときに、その高速シャット ダウンは使用しないことを確認する場合は、 **IMAPIProviderShutdown**インターフェイスを実装し、 **IMAPIProviderShutdown::QueryFastShutdown**メソッドの MAPI_E_NO_SUPPORT を返すする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8e537-120">If a MAPI provider needs to ensure that fast shutdown is not used while it is loaded, it should implement the **IMAPIProviderShutdown** interface and return MAPI_E_NO_SUPPORT for the **IMAPIProviderShutdown::QueryFastShutdown** method.</span></span> <span data-ttu-id="8e537-121">ただし、Outlook などの MAPI クライアントはこれにより、クライアントが高速シャット ダウンを中止し、シャット ダウンに長い時間がかかります。</span><span class="sxs-lookup"><span data-stu-id="8e537-121">However, for MAPI clients such as Outlook, this will cause the client to abandon fast shutdown and take a longer time to shut down.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="8e537-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="8e537-122">See also</span></span>



[<span data-ttu-id="8e537-123">Mapi クライアントのシャット ダウン</span><span class="sxs-lookup"><span data-stu-id="8e537-123">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)
  
[<span data-ttu-id="8e537-124">高速シャットダウンの概要</span><span class="sxs-lookup"><span data-stu-id="8e537-124">Fast Shutdown Overview</span></span>](fast-shutdown-overview.md)
  
[<span data-ttu-id="8e537-125">高速シャットダウンのユーザー オプション</span><span class="sxs-lookup"><span data-stu-id="8e537-125">Fast Shutdown User Options</span></span>](fast-shutdown-user-options.md)

