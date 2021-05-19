---
title: サービス プロバイダーのシャットダウン
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
# <a name="shutting-down-a-service-provider"></a><span data-ttu-id="0dd71-103">サービス プロバイダーのシャットダウン</span><span class="sxs-lookup"><span data-stu-id="0dd71-103">Shutting Down a Service Provider</span></span>

 
  
<span data-ttu-id="0dd71-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0dd71-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0dd71-105">クライアントが [IMAPISession::Logoff](imapisession-logoff.md) メソッドを呼び出してセッションを終了し、すべてのアクティブなサービス プロバイダーをシャットダウンすると、MAPI は次のメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0dd71-105">When a client calls the [IMAPISession::Logoff](imapisession-logoff.md) method to end the session and shut down all active service providers, MAPI in turn calls the following methods:</span></span> 
  
- <span data-ttu-id="0dd71-106">[アドレス帳プロバイダーの IABLogon::Logoff。](iablogon-logoff.md)</span><span class="sxs-lookup"><span data-stu-id="0dd71-106">[IABLogon::Logoff](iablogon-logoff.md) for address book providers.</span></span> 
    
- <span data-ttu-id="0dd71-107">[メッセージ ストア プロバイダーの IMSLogon::Logoff。](imslogon-logoff.md)</span><span class="sxs-lookup"><span data-stu-id="0dd71-107">[IMSLogon::Logoff](imslogon-logoff.md) for message store providers.</span></span> 
    
- <span data-ttu-id="0dd71-108">[IXPLogon::TransportLogoff for](ixplogon-transportlogoff.md) transport providers.</span><span class="sxs-lookup"><span data-stu-id="0dd71-108">[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) for transport providers.</span></span> 
    
<span data-ttu-id="0dd71-109">これらのメソッドは、同様の実装を持っています。</span><span class="sxs-lookup"><span data-stu-id="0dd71-109">These methods have similar implementations.</span></span> <span data-ttu-id="0dd71-110">ログオフ メソッドが実行する主なタスクは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="0dd71-110">The main tasks that a logoff method performs are as follows:</span></span>
  
- <span data-ttu-id="0dd71-111">サブオブジェクトや状態オブジェクトを含む、開いているすべてのオブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="0dd71-111">Releasing all open objects, including subobjects and status objects.</span></span>
    
- <span data-ttu-id="0dd71-112">サポート オブジェクトの [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) メソッドを呼び出して、参照カウントをデクレメントします。</span><span class="sxs-lookup"><span data-stu-id="0dd71-112">Calling the support object's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to decrement its reference count.</span></span> 
    
- <span data-ttu-id="0dd71-113">プロバイダーの登録済み [MAPIUID 構造体をすべて削除](mapiuid.md) します。</span><span class="sxs-lookup"><span data-stu-id="0dd71-113">Removing all of your provider's registered [MAPIUID](mapiuid.md) structures.</span></span> 
    
- <span data-ttu-id="0dd71-114">状態テーブル内のプロバイダーの行を削除します。</span><span class="sxs-lookup"><span data-stu-id="0dd71-114">Removing your provider's row in the status table.</span></span>
    
- <span data-ttu-id="0dd71-115">次のようなリソースのクリーンアップに関連するタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="0dd71-115">Performing any tasks that relate to cleaning up resources, such as the following:</span></span>
    
  - <span data-ttu-id="0dd71-116">リモート サーバーとの接続を終了する。</span><span class="sxs-lookup"><span data-stu-id="0dd71-116">Terminating a connection with a remote server.</span></span>
    
  - <span data-ttu-id="0dd71-117">ログオン オブジェクトの参照カウントをデクレメントします。</span><span class="sxs-lookup"><span data-stu-id="0dd71-117">Decrementing the reference count on the logon object.</span></span>
    
  - <span data-ttu-id="0dd71-118">プロバイダーが格納するログオン オブジェクトの一覧からログオン オブジェクトを削除する。</span><span class="sxs-lookup"><span data-stu-id="0dd71-118">Removing the logon object from the list of logon objects that your provider stores.</span></span>
    
  - <span data-ttu-id="0dd71-119">デバッグ モードでは、メモリがリークしたオブジェクトを検索するトレースを発行します。</span><span class="sxs-lookup"><span data-stu-id="0dd71-119">In debug mode, issuing traces to locate objects that have leaked memory.</span></span>
    
<span data-ttu-id="0dd71-120">logoff メソッドが返された場合、MAPI は次を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0dd71-120">When your logoff method returns, MAPI calls the following:</span></span>
  
- <span data-ttu-id="0dd71-121">ログオン オブジェクトの **IUnknown::Release** メソッド。</span><span class="sxs-lookup"><span data-stu-id="0dd71-121">Your logon object's **IUnknown::Release** method.</span></span> 
    
- <span data-ttu-id="0dd71-122">プロバイダー オブジェクトの **Shutdown** メソッドを使用して、最終的なクリーンアップ タスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="0dd71-122">Your provider object's **Shutdown** method to perform any final cleanup tasks.</span></span> <span data-ttu-id="0dd71-123">プロバイダーの種類に応じて、次のいずれかのメソッドが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="0dd71-123">Depending on the type of your provider, one of the following methods is called:</span></span> 
    
  - <span data-ttu-id="0dd71-124">[IABProvider::アドレス帳](iabprovider-shutdown.md) プロバイダーのシャットダウン</span><span class="sxs-lookup"><span data-stu-id="0dd71-124">[IABProvider::Shutdown](iabprovider-shutdown.md) for address book providers</span></span> 
    
  - <span data-ttu-id="0dd71-125">[IMSProvider::メッセージ ストア](imsprovider-shutdown.md) プロバイダーのシャットダウン</span><span class="sxs-lookup"><span data-stu-id="0dd71-125">[IMSProvider::Shutdown](imsprovider-shutdown.md) for message store providers</span></span> 
    
  - <span data-ttu-id="0dd71-126">[IXPProvider::トランスポート](ixpprovider-shutdown.md) プロバイダーのシャットダウン</span><span class="sxs-lookup"><span data-stu-id="0dd71-126">[IXPProvider::Shutdown](ixpprovider-shutdown.md) for transport providers</span></span> 
    
- <span data-ttu-id="0dd71-127">プロバイダー オブジェクトの **IUnknown::Release** メソッド。</span><span class="sxs-lookup"><span data-stu-id="0dd71-127">Your provider object's **IUnknown::Release** method.</span></span> 
    
<span data-ttu-id="0dd71-128">プロバイダーがメッセージ ストアの場合は [、IMsgStore::StoreLogoff](imsgstore-storelogoff.md) へのクライアント呼び出しでもシャットダウン プロセスが開始されます。</span><span class="sxs-lookup"><span data-stu-id="0dd71-128">If your provider is a message store, a client call to [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) will also initiate the shutdown process.</span></span> <span data-ttu-id="0dd71-129">**StoreLogoff は** 、1 つの特定のメッセージ ストア プロバイダーをシャットダウンし、セッションには影響しません。</span><span class="sxs-lookup"><span data-stu-id="0dd71-129">**StoreLogoff** shuts down one particular message store provider and has no effect on the session.</span></span> <span data-ttu-id="0dd71-130">このメソッドを使用してシャットダウンできるのは、メッセージ ストア プロバイダーのみです。特定のアドレス帳またはトランスポート プロバイダーをシャットダウンする明示的な方法はありません。</span><span class="sxs-lookup"><span data-stu-id="0dd71-130">Only a message store provider can be shut down with this method; there is no explicit way to shut down a particular address book or transport provider.</span></span> <span data-ttu-id="0dd71-131">**StoreLogoff** 呼び出しに応答する方法の詳細については、「メッセージ ストア プロバイダーのシャットダウン [」を参照してください](shutting-down-a-message-store-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="0dd71-131">For information about how to respond to a **StoreLogoff** call, see [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).</span></span>
  
<span data-ttu-id="0dd71-132">MAPI が Win32 API 関数 **FreeLibrary** を呼び出す場合、プロバイダーの DLL はアンロードされます。最後のアクティブなクライアントが [MAPIUninitialize](mapiuninitialize.md)を呼び出した後に行われた呼び出しです。</span><span class="sxs-lookup"><span data-stu-id="0dd71-132">Your provider's DLL will be unloaded when MAPI calls the Win32 API function **FreeLibrary**, a call that is made after the last active client has called [MAPIUninitialize](mapiuninitialize.md).</span></span> <span data-ttu-id="0dd71-133">この時点で、サービス プロバイダーはシャットダウンを終了します。</span><span class="sxs-lookup"><span data-stu-id="0dd71-133">By this time, your service provider will have finished shutting down.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0dd71-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="0dd71-134">See also</span></span>



[<span data-ttu-id="0dd71-135">MAPI サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="0dd71-135">MAPI Service Providers</span></span>](mapi-service-providers.md)

