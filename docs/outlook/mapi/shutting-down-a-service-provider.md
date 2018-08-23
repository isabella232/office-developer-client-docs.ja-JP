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
ms.openlocfilehash: 70db0b0a62568cc499cf915634756bb422ae82ca
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567196"
---
# <a name="shutting-down-a-service-provider"></a><span data-ttu-id="3a7fc-103">サービス プロバイダーのシャットダウン</span><span class="sxs-lookup"><span data-stu-id="3a7fc-103">Shutting Down a Service Provider</span></span>

 
  
<span data-ttu-id="3a7fc-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3a7fc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3a7fc-105">クライアントがセッションを終了し、すべてのアクティブなサービス プロバイダーをシャット ダウンするには、 [IMAPISession::Logoff](imapisession-logoff.md)メソッドを呼び出すと、MAPI は順に次メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3a7fc-105">When a client calls the [IMAPISession::Logoff](imapisession-logoff.md) method to end the session and shut down all active service providers, MAPI in turn calls the following methods:</span></span> 
  
- <span data-ttu-id="3a7fc-106">アドレス帳プロバイダーの[IABLogon::Logoff](iablogon-logoff.md)にします。</span><span class="sxs-lookup"><span data-stu-id="3a7fc-106">[IABLogon::Logoff](iablogon-logoff.md) for address book providers.</span></span> 
    
- <span data-ttu-id="3a7fc-107">メッセージ ストア プロバイダーの[IMSLogon::Logoff](imslogon-logoff.md)にします。</span><span class="sxs-lookup"><span data-stu-id="3a7fc-107">[IMSLogon::Logoff](imslogon-logoff.md) for message store providers.</span></span> 
    
- <span data-ttu-id="3a7fc-108">トランスポート プロバイダーの[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md)にします。</span><span class="sxs-lookup"><span data-stu-id="3a7fc-108">[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) for transport providers.</span></span> 
    
<span data-ttu-id="3a7fc-109">これらのメソッドでは、ような実装があります。</span><span class="sxs-lookup"><span data-stu-id="3a7fc-109">These methods have similar implementations.</span></span> <span data-ttu-id="3a7fc-110">ログオフ メソッドを実行する主要なタスクは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="3a7fc-110">The main tasks that a logoff method performs are as follows:</span></span>
  
- <span data-ttu-id="3a7fc-111">すべてのサブオブジェクトを含め、開いているオブジェクトと状態オブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="3a7fc-111">Releasing all open objects, including subobjects and status objects.</span></span>
    
- <span data-ttu-id="3a7fc-112">メソッド サポート オブジェクトの[リ ス](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx)の参照カウントをデクリメントします。</span><span class="sxs-lookup"><span data-stu-id="3a7fc-112">Calling the support object's [IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to decrement its reference count.</span></span> 
    
- <span data-ttu-id="3a7fc-113">プロバイダーの登録済みの[MAPIUID](mapiuid.md)構造体のすべてを削除しています。</span><span class="sxs-lookup"><span data-stu-id="3a7fc-113">Removing all of your provider's registered [MAPIUID](mapiuid.md) structures.</span></span> 
    
- <span data-ttu-id="3a7fc-114">ステータスの表に、プロバイダーの行を削除しています。</span><span class="sxs-lookup"><span data-stu-id="3a7fc-114">Removing your provider's row in the status table.</span></span>
    
- <span data-ttu-id="3a7fc-115">次のように、リソースのクリーンアップに関連するすべてのタスクを実行するには。</span><span class="sxs-lookup"><span data-stu-id="3a7fc-115">Performing any tasks that relate to cleaning up resources, such as the following:</span></span>
    
  - <span data-ttu-id="3a7fc-116">リモート サーバーとの接続を終了しています。</span><span class="sxs-lookup"><span data-stu-id="3a7fc-116">Terminating a connection with a remote server.</span></span>
    
  - <span data-ttu-id="3a7fc-117">ログオン オブジェクトの参照をデクリメントする操作をカウントします。</span><span class="sxs-lookup"><span data-stu-id="3a7fc-117">Decrementing the reference count on the logon object.</span></span>
    
  - <span data-ttu-id="3a7fc-118">ログオン オブジェクトをプロバイダーが格納されているログオン オブジェクトの一覧から削除しています。</span><span class="sxs-lookup"><span data-stu-id="3a7fc-118">Removing the logon object from the list of logon objects that your provider stores.</span></span>
    
  - <span data-ttu-id="3a7fc-119">デバッグ モードでのメモリをリークしているオブジェクトを検索するのにはトレースを発行します。</span><span class="sxs-lookup"><span data-stu-id="3a7fc-119">In debug mode, issuing traces to locate objects that have leaked memory.</span></span>
    
<span data-ttu-id="3a7fc-120">ログオフ メソッドから制御が戻るとき、MAPI が次に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3a7fc-120">When your logoff method returns, MAPI calls the following:</span></span>
  
- <span data-ttu-id="3a7fc-121">ログオン オブジェクトの**リ ス**の方法です。</span><span class="sxs-lookup"><span data-stu-id="3a7fc-121">Your logon object's **IUnknown::Release** method.</span></span> 
    
- <span data-ttu-id="3a7fc-122">プロバイダー オブジェクトの最終的なクリーンアップ タスクを実行するのにはメソッドを**シャット ダウン**します。</span><span class="sxs-lookup"><span data-stu-id="3a7fc-122">Your provider object's **Shutdown** method to perform any final cleanup tasks.</span></span> <span data-ttu-id="3a7fc-123">、プロバイダーの種類によって次の方法のいずれかが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3a7fc-123">Depending on the type of your provider, one of the following methods is called:</span></span> 
    
  - <span data-ttu-id="3a7fc-124">アドレス帳プロバイダーの[IABProvider::Shutdown](iabprovider-shutdown.md)</span><span class="sxs-lookup"><span data-stu-id="3a7fc-124">[IABProvider::Shutdown](iabprovider-shutdown.md) for address book providers</span></span> 
    
  - <span data-ttu-id="3a7fc-125">メッセージ ストア プロバイダーの[IMSProvider::Shutdown](imsprovider-shutdown.md)</span><span class="sxs-lookup"><span data-stu-id="3a7fc-125">[IMSProvider::Shutdown](imsprovider-shutdown.md) for message store providers</span></span> 
    
  - <span data-ttu-id="3a7fc-126">トランスポート プロバイダーの[IXPProvider::Shutdown](ixpprovider-shutdown.md)</span><span class="sxs-lookup"><span data-stu-id="3a7fc-126">[IXPProvider::Shutdown](ixpprovider-shutdown.md) for transport providers</span></span> 
    
- <span data-ttu-id="3a7fc-127">プロバイダー オブジェクトの**リ ス**の方法です。</span><span class="sxs-lookup"><span data-stu-id="3a7fc-127">Your provider object's **IUnknown::Release** method.</span></span> 
    
<span data-ttu-id="3a7fc-128">プロバイダーがメッセージ ・ ストアの場合は、 [IMsgStore::StoreLogoff](imsgstore-storelogoff.md)へのクライアント呼び出しがシャット ダウン処理を開始してもできます。</span><span class="sxs-lookup"><span data-stu-id="3a7fc-128">If your provider is a message store, a client call to [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) will also initiate the shutdown process.</span></span> <span data-ttu-id="3a7fc-129">**StoreLogoff**は、1 つの特定のメッセージ ストア プロバイダーをシャット ダウンし、セッションに影響を与えません。</span><span class="sxs-lookup"><span data-stu-id="3a7fc-129">**StoreLogoff** shuts down one particular message store provider and has no effect on the session.</span></span> <span data-ttu-id="3a7fc-130">メッセージ ストア プロバイダーだけをこの方法でシャット ダウンをできます。特定のアドレス帳またはトランスポート プロバイダーをシャット ダウンする明示的な方法はありません。</span><span class="sxs-lookup"><span data-stu-id="3a7fc-130">Only a message store provider can be shut down with this method; there is no explicit way to shut down a particular address book or transport provider.</span></span> <span data-ttu-id="3a7fc-131">の**StoreLogoff**に応答する方法についての情報を呼び出して、[シャット ダウン、メッセージ ストア プロバイダー](shutting-down-a-message-store-provider.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3a7fc-131">For information about how to respond to a **StoreLogoff** call, see [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).</span></span>
  
<span data-ttu-id="3a7fc-132">MAPI は、Win32 API 関数**終わった**が、最後のアクティブなクライアントが[MAPIUninitialize](mapiuninitialize.md)を呼び出した後に行われた呼び出しを呼び出すと、プロバイダーの DLL がアンロードされるされます。</span><span class="sxs-lookup"><span data-stu-id="3a7fc-132">Your provider's DLL will be unloaded when MAPI calls the Win32 API function **FreeLibrary**, a call that is made after the last active client has called [MAPIUninitialize](mapiuninitialize.md).</span></span> <span data-ttu-id="3a7fc-133">この時点で、シャット ダウン、サービス ・ プロバイダーが完了しましたが。</span><span class="sxs-lookup"><span data-stu-id="3a7fc-133">By this time, your service provider will have finished shutting down.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3a7fc-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="3a7fc-134">See also</span></span>



[<span data-ttu-id="3a7fc-135">MAPI サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="3a7fc-135">MAPI Service Providers</span></span>](mapi-service-providers.md)

