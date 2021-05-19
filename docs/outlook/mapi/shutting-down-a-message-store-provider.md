---
title: メッセージ ストア プロバイダーのシャットダウン
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
# <a name="shutting-down-a-message-store-provider"></a><span data-ttu-id="48f35-103">メッセージ ストア プロバイダーのシャットダウン</span><span class="sxs-lookup"><span data-stu-id="48f35-103">Shutting Down a Message Store Provider</span></span>

  
  
<span data-ttu-id="48f35-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="48f35-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="48f35-105">プロバイダーがメッセージ ストア プロバイダーの場合は、次のいずれかの方法でシャットダウンできます。</span><span class="sxs-lookup"><span data-stu-id="48f35-105">If your provider is a message store provider, it can be shut down in one of the following ways:</span></span>
  
- <span data-ttu-id="48f35-106">クライアントまたは MAPI スプーラーが [IMsgStore::StoreLogoff を呼び出す場合](imsgstore-storelogoff.md)。</span><span class="sxs-lookup"><span data-stu-id="48f35-106">When a client or the MAPI spooler calls [IMsgStore::StoreLogoff](imsgstore-storelogoff.md).</span></span> <span data-ttu-id="48f35-107">**StoreLogoff** を使用してメッセージ ストア プロバイダーをシャットダウンすると、シャットダウンが順序付けされ、制御された方法で実行されます。</span><span class="sxs-lookup"><span data-stu-id="48f35-107">Shutting down a message store provider with **StoreLogoff** causes the shutdown to occur in an orderly and controlled manner.</span></span> 
    
- <span data-ttu-id="48f35-108">クライアントが [IMAPISession::Logoff を呼び出す場合](imapisession-logoff.md)。</span><span class="sxs-lookup"><span data-stu-id="48f35-108">When a client calls [IMAPISession::Logoff](imapisession-logoff.md).</span></span> 
    
<span data-ttu-id="48f35-109">**IMsgStore::StoreLogoff** の実装は [、IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md)を呼び出して、MAPI がシャットダウンされたことを通知し、関連するトランスポート プロバイダーをログオフする必要があります。</span><span class="sxs-lookup"><span data-stu-id="48f35-109">Your implementation of **IMsgStore::StoreLogoff** should begin by calling [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) to inform MAPI that it is being shut down, indicating that any related transport providers should be logged off.</span></span> <span data-ttu-id="48f35-110">**IMsgStore::StoreLogoff が** 返された場合、その呼び出し元はメッセージ ストアの [IUnknown::Release メソッドを呼び出](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx)します。</span><span class="sxs-lookup"><span data-stu-id="48f35-110">When **IMsgStore::StoreLogoff** returns, its caller invokes your message store's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method.</span></span> <span data-ttu-id="48f35-111">サポート オブジェクト **の\*\*\*\*IUnknown::Release** メソッドを呼び出して、この Release メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="48f35-111">Implement this **Release** method by calling the support object's **IUnknown::Release** method.</span></span> 
  
<span data-ttu-id="48f35-112">MAPI は、メッセージ ストアの **IUnknown::Release** の実装で次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="48f35-112">MAPI performs the following tasks in its implementation of **IUnknown::Release** for message stores:</span></span> 
  
1. <span data-ttu-id="48f35-113">メッセージ ストア プロバイダーによって登録されている [MAPIUID](mapiuid.md) 構造をすべて削除します。</span><span class="sxs-lookup"><span data-stu-id="48f35-113">Removes all of the [MAPIUID](mapiuid.md) structures registered by the message store provider.</span></span> 
    
2. <span data-ttu-id="48f35-114">メッセージ ストア プロバイダーの行を状態テーブルから削除します。</span><span class="sxs-lookup"><span data-stu-id="48f35-114">Removes the message store provider's row from the status table.</span></span>
    
3. <span data-ttu-id="48f35-115">[IMSLogon::Logoff](imslogon-logoff.md)を呼び出して、開いているすべてのオブジェクト、サブオブジェクト、および状態オブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="48f35-115">Calls [IMSLogon::Logoff](imslogon-logoff.md) to release all open objects, subobjects, and status objects.</span></span> 
    
4. <span data-ttu-id="48f35-116">[IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx)を呼び出して、メッセージ ストア プロバイダーのログオン オブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="48f35-116">Calls [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) to release the message store provider's logon object.</span></span> 
    
<span data-ttu-id="48f35-117">一部のクライアントでは **、IMsgStore::StoreLogoff** への呼び出しを省略し、メッセージ ストアの **IUnknown::Release** メソッドへの呼び出しでメッセージ ストア プロバイダーのシャットダウンを開始する場合があります。</span><span class="sxs-lookup"><span data-stu-id="48f35-117">Some clients might omit the call to **IMsgStore::StoreLogoff**, initiating the shutdown of your message store provider with the call to the message store's **IUnknown::Release** method.</span></span> <span data-ttu-id="48f35-118">このような状況では **、StoreLogoff** を呼び出さずにシャットダウンを実行すると、順序が低く制御されます。</span><span class="sxs-lookup"><span data-stu-id="48f35-118">A shutdown under these circumstances without the call to **StoreLogoff** is less orderly and controlled.</span></span> <span data-ttu-id="48f35-119">この可能性を処理し **、IMAPISupport::StoreLogoffTransports** への呼び出しが発生したかどうかを追跡するために、メッセージ ストアの Release メソッドを記述します。 </span><span class="sxs-lookup"><span data-stu-id="48f35-119">Write your message store's **Release** method to handle this possibility and keep track of whether or not a call to **IMAPISupport::StoreLogoffTransports** has occurred.</span></span> <span data-ttu-id="48f35-120">**StoreLogoffTransports は、** シャットダウン プロセス中に 1 回呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="48f35-120">**StoreLogoffTransports** must be called once during the shutdown process.</span></span> <span data-ttu-id="48f35-121">Release メソッドで **StoreLogoffTransports** がまだ呼び出されていないことを検出した場合は、このフラグを使用して呼びLOGOFF_ABORTします。</span><span class="sxs-lookup"><span data-stu-id="48f35-121">If you detect in your **Release** method that **StoreLogoffTransports** has not yet been called, invoke it with the LOGOFF_ABORT flag.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="48f35-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="48f35-122">See also</span></span>



[<span data-ttu-id="48f35-123">サービス プロバイダーのシャットダウン</span><span class="sxs-lookup"><span data-stu-id="48f35-123">Shutting Down a Service Provider</span></span>](shutting-down-a-service-provider.md)

