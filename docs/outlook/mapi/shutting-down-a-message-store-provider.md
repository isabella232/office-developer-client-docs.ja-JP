---
title: メッセージ ストア プロバイダーのシャットダウン
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e38219db-f867-4c1d-9973-0e025779e8b6
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 8e4712572eaff465bb23b55eccc3670f637c0f9c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386055"
---
# <a name="shutting-down-a-message-store-provider"></a><span data-ttu-id="dafe9-103">メッセージ ストア プロバイダーのシャットダウン</span><span class="sxs-lookup"><span data-stu-id="dafe9-103">Shutting Down a Message Store Provider</span></span>

  
  
<span data-ttu-id="dafe9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dafe9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dafe9-105">プロバイダーがメッセージ ストア プロバイダーの場合は、それをシャット ダウンできる次の方法のいずれかで。</span><span class="sxs-lookup"><span data-stu-id="dafe9-105">If your provider is a message store provider, it can be shut down in one of the following ways:</span></span>
  
- <span data-ttu-id="dafe9-106">クライアントまたは MAPI スプーラーを呼び出すと[IMsgStore::StoreLogoff](imsgstore-storelogoff.md)を。</span><span class="sxs-lookup"><span data-stu-id="dafe9-106">When a client or the MAPI spooler calls [IMsgStore::StoreLogoff](imsgstore-storelogoff.md).</span></span> <span data-ttu-id="dafe9-107">規則的かつ制御された方法で発生するシャット ダウンは、 **StoreLogoff**のメッセージ ストア プロバイダーをシャット ダウンします。</span><span class="sxs-lookup"><span data-stu-id="dafe9-107">Shutting down a message store provider with **StoreLogoff** causes the shutdown to occur in an orderly and controlled manner.</span></span> 
    
- <span data-ttu-id="dafe9-108">クライアントは、 [IMAPISession::Logoff](imapisession-logoff.md)を呼び出すとします。</span><span class="sxs-lookup"><span data-stu-id="dafe9-108">When a client calls [IMAPISession::Logoff](imapisession-logoff.md).</span></span> 
    
<span data-ttu-id="dafe9-109">シャット ダウン、、関連するトランスポート プロバイダーを記録する必要があることを示す MAPI を通知するために[IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md)を呼び出すことによって**IMsgStore::StoreLogoff**の実装を開始する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dafe9-109">Your implementation of **IMsgStore::StoreLogoff** should begin by calling [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) to inform MAPI that it is being shut down, indicating that any related transport providers should be logged off.</span></span> <span data-ttu-id="dafe9-110">**IMsgStore::StoreLogoff**が返されるとき、呼び出し元は、メッセージ ・ ストアの[リ ス](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx)のメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="dafe9-110">When **IMsgStore::StoreLogoff** returns, its caller invokes your message store's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method.</span></span> <span data-ttu-id="dafe9-111">サポート オブジェクト**が**メソッドを呼び出して、**このメソッド**を実装します。</span><span class="sxs-lookup"><span data-stu-id="dafe9-111">Implement this **Release** method by calling the support object's **IUnknown::Release** method.</span></span> 
  
<span data-ttu-id="dafe9-112">MAPI は、メッセージ ・ ストアの**リ ス**の実装で、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="dafe9-112">MAPI performs the following tasks in its implementation of **IUnknown::Release** for message stores:</span></span> 
  
1. <span data-ttu-id="dafe9-113">メッセージ ストア プロバイダーが登録されている[MAPIUID](mapiuid.md)の構造体のすべてを削除します。</span><span class="sxs-lookup"><span data-stu-id="dafe9-113">Removes all of the [MAPIUID](mapiuid.md) structures registered by the message store provider.</span></span> 
    
2. <span data-ttu-id="dafe9-114">状態テーブルからには、メッセージ ストア プロバイダーの行を削除します。</span><span class="sxs-lookup"><span data-stu-id="dafe9-114">Removes the message store provider's row from the status table.</span></span>
    
3. <span data-ttu-id="dafe9-115">すべての開いているオブジェクトは、下位オブジェクト、および状態オブジェクトを解放するのには[IMSLogon::Logoff](imslogon-logoff.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="dafe9-115">Calls [IMSLogon::Logoff](imslogon-logoff.md) to release all open objects, subobjects, and status objects.</span></span> 
    
4. <span data-ttu-id="dafe9-116">メッセージ ストア プロバイダーのログオン オブジェクトを解放する[リ ス](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="dafe9-116">Calls [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) to release the message store provider's logon object.</span></span> 
    
<span data-ttu-id="dafe9-117">一部のクライアントは、 **IMsgStore::StoreLogoff**、メッセージ ストアの\*\*\*\* メソッドの呼び出しでは、メッセージ ストア プロバイダーのシャット ダウンを開始する呼び出しを省略可能性があります。</span><span class="sxs-lookup"><span data-stu-id="dafe9-117">Some clients might omit the call to **IMsgStore::StoreLogoff**, initiating the shutdown of your message store provider with the call to the message store's **IUnknown::Release** method.</span></span> <span data-ttu-id="dafe9-118">**StoreLogoff**への呼び出しがない状況ではこれらのシャット ダウンは、あまり規則的で制御されました。</span><span class="sxs-lookup"><span data-stu-id="dafe9-118">A shutdown under these circumstances without the call to **StoreLogoff** is less orderly and controlled.</span></span> <span data-ttu-id="dafe9-119">この可能性を処理し、 **IMAPISupport::StoreLogoffTransports**への呼び出しが発生したかどうかの追跡、メッセージ ・ ストアの**Release**のメソッドを記述します。</span><span class="sxs-lookup"><span data-stu-id="dafe9-119">Write your message store's **Release** method to handle this possibility and keep track of whether or not a call to **IMAPISupport::StoreLogoffTransports** has occurred.</span></span> <span data-ttu-id="dafe9-120">**StoreLogoffTransports**は、シャット ダウン処理中に 1 回呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="dafe9-120">**StoreLogoffTransports** must be called once during the shutdown process.</span></span> <span data-ttu-id="dafe9-121">検出した場合、 **Release**のメソッドである**StoreLogoffTransports**がまだ呼び出されていない、LOGOFF_ABORT フラグを指定して呼び出すことです。</span><span class="sxs-lookup"><span data-stu-id="dafe9-121">If you detect in your **Release** method that **StoreLogoffTransports** has not yet been called, invoke it with the LOGOFF_ABORT flag.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dafe9-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="dafe9-122">See also</span></span>



[<span data-ttu-id="dafe9-123">サービス プロバイダーのシャットダウン</span><span class="sxs-lookup"><span data-stu-id="dafe9-123">Shutting Down a Service Provider</span></span>](shutting-down-a-service-provider.md)

