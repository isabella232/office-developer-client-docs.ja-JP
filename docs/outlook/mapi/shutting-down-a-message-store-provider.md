---
title: メッセージストアプロバイダーのシャットダウン
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e38219db-f867-4c1d-9973-0e025779e8b6
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8e4712572eaff465bb23b55eccc3670f637c0f9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339201"
---
# <a name="shutting-down-a-message-store-provider"></a><span data-ttu-id="aa717-103">メッセージストアプロバイダーのシャットダウン</span><span class="sxs-lookup"><span data-stu-id="aa717-103">Shutting Down a Message Store Provider</span></span>

  
  
<span data-ttu-id="aa717-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aa717-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aa717-105">プロバイダーがメッセージストアプロバイダーの場合は、次のいずれかの方法でシャットダウンできます。</span><span class="sxs-lookup"><span data-stu-id="aa717-105">If your provider is a message store provider, it can be shut down in one of the following ways:</span></span>
  
- <span data-ttu-id="aa717-106">クライアントまたは MAPI スプーラーが[IMsgStore:: storelogoff](imsgstore-storelogoff.md)を呼び出したとき。</span><span class="sxs-lookup"><span data-stu-id="aa717-106">When a client or the MAPI spooler calls [IMsgStore::StoreLogoff](imsgstore-storelogoff.md).</span></span> <span data-ttu-id="aa717-107">**storelogoff**を使用してメッセージストアプロバイダーをシャットダウンすると、シャットダウンが整然と制御された方法で発生します。</span><span class="sxs-lookup"><span data-stu-id="aa717-107">Shutting down a message store provider with **StoreLogoff** causes the shutdown to occur in an orderly and controlled manner.</span></span> 
    
- <span data-ttu-id="aa717-108">クライアントが[imapisession:: Logoff](imapisession-logoff.md)を呼び出すとき。</span><span class="sxs-lookup"><span data-stu-id="aa717-108">When a client calls [IMAPISession::Logoff](imapisession-logoff.md).</span></span> 
    
<span data-ttu-id="aa717-109">**IMsgStore:: storelogoff**の実装は、 [imapisupport:: storelogofftransport](imapisupport-storelogofftransports.md)を呼び出して、シャットダウン中であることを MAPI に通知することによって開始します。これは、関連するすべてのトランスポートプロバイダーをログオフする必要があることを意味します。</span><span class="sxs-lookup"><span data-stu-id="aa717-109">Your implementation of **IMsgStore::StoreLogoff** should begin by calling [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) to inform MAPI that it is being shut down, indicating that any related transport providers should be logged off.</span></span> <span data-ttu-id="aa717-110">**IMsgStore:: storelogoff**は、メッセージストアの[IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="aa717-110">When **IMsgStore::StoreLogoff** returns, its caller invokes your message store's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method.</span></span> <span data-ttu-id="aa717-111">サポートオブジェクトの**IUnknown:: release**メソッドを呼び出して、この**Release**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="aa717-111">Implement this **Release** method by calling the support object's **IUnknown::Release** method.</span></span> 
  
<span data-ttu-id="aa717-112">MAPI は、メッセージストアの**IUnknown:: Release**の実装で、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="aa717-112">MAPI performs the following tasks in its implementation of **IUnknown::Release** for message stores:</span></span> 
  
1. <span data-ttu-id="aa717-113">メッセージストアプロバイダーによって登録されたすべての[MAPIUID](mapiuid.md)構造を削除します。</span><span class="sxs-lookup"><span data-stu-id="aa717-113">Removes all of the [MAPIUID](mapiuid.md) structures registered by the message store provider.</span></span> 
    
2. <span data-ttu-id="aa717-114">メッセージストアプロバイダーの行を状態テーブルから削除します。</span><span class="sxs-lookup"><span data-stu-id="aa717-114">Removes the message store provider's row from the status table.</span></span>
    
3. <span data-ttu-id="aa717-115">[IMSLogon:: Logoff](imslogon-logoff.md)を呼び出して、開いているすべてのオブジェクト、サブオブジェクト、およびステータスオブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="aa717-115">Calls [IMSLogon::Logoff](imslogon-logoff.md) to release all open objects, subobjects, and status objects.</span></span> 
    
4. <span data-ttu-id="aa717-116">[IUnknown:: release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx)を呼び出して、メッセージストアプロバイダーのログオンオブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="aa717-116">Calls [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) to release the message store provider's logon object.</span></span> 
    
<span data-ttu-id="aa717-117">クライアントによっては、 **IMsgStore:: storelogoff**への呼び出しを省略して、メッセージストアの**IUnknown:: Release**メソッドへの呼び出しを使用して、メッセージストアプロバイダーのシャットダウンを開始する場合があります。</span><span class="sxs-lookup"><span data-stu-id="aa717-117">Some clients might omit the call to **IMsgStore::StoreLogoff**, initiating the shutdown of your message store provider with the call to the message store's **IUnknown::Release** method.</span></span> <span data-ttu-id="aa717-118">**storelogoff**への呼び出しなしで、このような状況下でのシャットダウンは、整然と制御されません。</span><span class="sxs-lookup"><span data-stu-id="aa717-118">A shutdown under these circumstances without the call to **StoreLogoff** is less orderly and controlled.</span></span> <span data-ttu-id="aa717-119">この可能性を処理するために、メッセージストアの**Release**メソッドを記述し、 **: storelogofftransports**が発生したかどうかを追跡します。</span><span class="sxs-lookup"><span data-stu-id="aa717-119">Write your message store's **Release** method to handle this possibility and keep track of whether or not a call to **IMAPISupport::StoreLogoffTransports** has occurred.</span></span> <span data-ttu-id="aa717-120">**storelogofftransports**は、シャットダウンプロセス中に1回呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="aa717-120">**StoreLogoffTransports** must be called once during the shutdown process.</span></span> <span data-ttu-id="aa717-121">**storelogofftransports**がまだ呼び出されていない**リリース**方法で検出した場合は、LOGOFF_ABORT フラグを使用して呼び出します。</span><span class="sxs-lookup"><span data-stu-id="aa717-121">If you detect in your **Release** method that **StoreLogoffTransports** has not yet been called, invoke it with the LOGOFF_ABORT flag.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="aa717-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="aa717-122">See also</span></span>



[<span data-ttu-id="aa717-123">サービスプロバイダーのシャットダウン</span><span class="sxs-lookup"><span data-stu-id="aa717-123">Shutting Down a Service Provider</span></span>](shutting-down-a-service-provider.md)

