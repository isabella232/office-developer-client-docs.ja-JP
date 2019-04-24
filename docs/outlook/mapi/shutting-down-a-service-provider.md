---
title: サービスプロバイダーのシャットダウン
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e518830b-0aaa-4ce4-a85a-07e4f00750a9
description: '�ŏI�X�V��: 2015�N12��7��'
ms.openlocfilehash: 4e25dad1e04927e10af38cdfbf8f30c9bd04234b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339208"
---
# <a name="shutting-down-a-service-provider"></a><span data-ttu-id="6f962-103">サービスプロバイダーのシャットダウン</span><span class="sxs-lookup"><span data-stu-id="6f962-103">Shutting Down a Service Provider</span></span>

 
  
<span data-ttu-id="6f962-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6f962-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6f962-105">クライアントが[imapisession:: Logoff](imapisession-logoff.md)メソッドを呼び出してセッションを終了し、すべてのアクティブなサービスプロバイダーをシャットダウンすると、次のメソッドが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6f962-105">When a client calls the [IMAPISession::Logoff](imapisession-logoff.md) method to end the session and shut down all active service providers, MAPI in turn calls the following methods:</span></span> 
  
- <span data-ttu-id="6f962-106">[IABLogon:: ログオフ](iablogon-logoff.md)アドレス帳プロバイダー。</span><span class="sxs-lookup"><span data-stu-id="6f962-106">[IABLogon::Logoff](iablogon-logoff.md) for address book providers.</span></span> 
    
- <span data-ttu-id="6f962-107">[IMSLogon:: ログオフ](imslogon-logoff.md)するメッセージストアプロバイダー。</span><span class="sxs-lookup"><span data-stu-id="6f962-107">[IMSLogon::Logoff](imslogon-logoff.md) for message store providers.</span></span> 
    
- <span data-ttu-id="6f962-108">[IXPLogon::](ixplogon-transportlogoff.md)トランスポートプロバイダーの transportlogoff。</span><span class="sxs-lookup"><span data-stu-id="6f962-108">[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) for transport providers.</span></span> 
    
<span data-ttu-id="6f962-109">これらのメソッドには、同様の実装があります。</span><span class="sxs-lookup"><span data-stu-id="6f962-109">These methods have similar implementations.</span></span> <span data-ttu-id="6f962-110">logoff メソッドが実行する主要なタスクは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="6f962-110">The main tasks that a logoff method performs are as follows:</span></span>
  
- <span data-ttu-id="6f962-111">サブオブジェクトおよびステータスオブジェクトを含む、開いているオブジェクトをすべて解放します。</span><span class="sxs-lookup"><span data-stu-id="6f962-111">Releasing all open objects, including subobjects and status objects.</span></span>
    
- <span data-ttu-id="6f962-112">サポートオブジェクトの[IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx)メソッドを呼び出して、参照カウントをデクリメントします。</span><span class="sxs-lookup"><span data-stu-id="6f962-112">Calling the support object's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to decrement its reference count.</span></span> 
    
- <span data-ttu-id="6f962-113">プロバイダーの登録済みの[MAPIUID](mapiuid.md)構造体をすべて削除します。</span><span class="sxs-lookup"><span data-stu-id="6f962-113">Removing all of your provider's registered [MAPIUID](mapiuid.md) structures.</span></span> 
    
- <span data-ttu-id="6f962-114">状態テーブルのプロバイダーの行を削除します。</span><span class="sxs-lookup"><span data-stu-id="6f962-114">Removing your provider's row in the status table.</span></span>
    
- <span data-ttu-id="6f962-115">リソースのクリーンアップに関連するすべてのタスクを実行します。たとえば、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="6f962-115">Performing any tasks that relate to cleaning up resources, such as the following:</span></span>
    
  - <span data-ttu-id="6f962-116">リモートサーバーとの接続を終了します。</span><span class="sxs-lookup"><span data-stu-id="6f962-116">Terminating a connection with a remote server.</span></span>
    
  - <span data-ttu-id="6f962-117">ログオンオブジェクトの参照カウントをデクリメントします。</span><span class="sxs-lookup"><span data-stu-id="6f962-117">Decrementing the reference count on the logon object.</span></span>
    
  - <span data-ttu-id="6f962-118">プロバイダーが格納するログオンオブジェクトの一覧から、ログオンオブジェクトを削除します。</span><span class="sxs-lookup"><span data-stu-id="6f962-118">Removing the logon object from the list of logon objects that your provider stores.</span></span>
    
  - <span data-ttu-id="6f962-119">デバッグモードで、リークしたメモリがあるオブジェクトを検索するためのトレースを発行します。</span><span class="sxs-lookup"><span data-stu-id="6f962-119">In debug mode, issuing traces to locate objects that have leaked memory.</span></span>
    
<span data-ttu-id="6f962-120">logoff メソッドが戻ると、MAPI は次のように呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6f962-120">When your logoff method returns, MAPI calls the following:</span></span>
  
- <span data-ttu-id="6f962-121">ログオンオブジェクトの**IUnknown:: Release**メソッド。</span><span class="sxs-lookup"><span data-stu-id="6f962-121">Your logon object's **IUnknown::Release** method.</span></span> 
    
- <span data-ttu-id="6f962-122">最終的なクリーンアップタスクを実行するには、プロバイダーオブジェクトの**Shutdown**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="6f962-122">Your provider object's **Shutdown** method to perform any final cleanup tasks.</span></span> <span data-ttu-id="6f962-123">プロバイダーの種類に応じて、次のいずれかのメソッドが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6f962-123">Depending on the type of your provider, one of the following methods is called:</span></span> 
    
  - <span data-ttu-id="6f962-124">[IABProvider::](iabprovider-shutdown.md)アドレス帳プロバイダーのシャットダウン</span><span class="sxs-lookup"><span data-stu-id="6f962-124">[IABProvider::Shutdown](iabprovider-shutdown.md) for address book providers</span></span> 
    
  - <span data-ttu-id="6f962-125">[IMSProvider::](imsprovider-shutdown.md)メッセージストアプロバイダーのシャットダウン</span><span class="sxs-lookup"><span data-stu-id="6f962-125">[IMSProvider::Shutdown](imsprovider-shutdown.md) for message store providers</span></span> 
    
  - <span data-ttu-id="6f962-126">[ixpprovider:: Shutdown](ixpprovider-shutdown.md) for transport providers</span><span class="sxs-lookup"><span data-stu-id="6f962-126">[IXPProvider::Shutdown](ixpprovider-shutdown.md) for transport providers</span></span> 
    
- <span data-ttu-id="6f962-127">プロバイダーオブジェクトの**IUnknown:: Release**メソッド。</span><span class="sxs-lookup"><span data-stu-id="6f962-127">Your provider object's **IUnknown::Release** method.</span></span> 
    
<span data-ttu-id="6f962-128">プロバイダーがメッセージストアの場合、 [IMsgStore:: storelogoff](imsgstore-storelogoff.md)へのクライアント呼び出しでも、シャットダウンプロセスが開始されます。</span><span class="sxs-lookup"><span data-stu-id="6f962-128">If your provider is a message store, a client call to [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) will also initiate the shutdown process.</span></span> <span data-ttu-id="6f962-129">**storelogoff**は、1つの特定のメッセージストアプロバイダーをシャットダウンし、セッションには影響を与えません。</span><span class="sxs-lookup"><span data-stu-id="6f962-129">**StoreLogoff** shuts down one particular message store provider and has no effect on the session.</span></span> <span data-ttu-id="6f962-130">このメソッドを使用すると、メッセージストアプロバイダーのみをシャットダウンできます。特定のアドレス帳またはトランスポートプロバイダーをシャットダウンする明示的な方法はありません。</span><span class="sxs-lookup"><span data-stu-id="6f962-130">Only a message store provider can be shut down with this method; there is no explicit way to shut down a particular address book or transport provider.</span></span> <span data-ttu-id="6f962-131">**storelogoff**呼び出しに応答する方法については、「[メッセージストアプロバイダーのシャットダウン](shutting-down-a-message-store-provider.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f962-131">For information about how to respond to a **StoreLogoff** call, see [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).</span></span>
  
<span data-ttu-id="6f962-132">MAPI が Win32 API 関数**FreeLibrary**を呼び出すときに、プロバイダーの DLL がアンロードされます。最後にアクティブなクライアントが[MAPIUninitialize](mapiuninitialize.md)を呼び出した後で行われます。</span><span class="sxs-lookup"><span data-stu-id="6f962-132">Your provider's DLL will be unloaded when MAPI calls the Win32 API function **FreeLibrary**, a call that is made after the last active client has called [MAPIUninitialize](mapiuninitialize.md).</span></span> <span data-ttu-id="6f962-133">この時点で、サービスプロバイダーはシャットダウンを終了しています。</span><span class="sxs-lookup"><span data-stu-id="6f962-133">By this time, your service provider will have finished shutting down.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6f962-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="6f962-134">See also</span></span>



[<span data-ttu-id="6f962-135">MAPI サービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="6f962-135">MAPI Service Providers</span></span>](mapi-service-providers.md)

