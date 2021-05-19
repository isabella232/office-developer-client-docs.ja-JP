---
title: IMAPISupportStoreLogoffTransports
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.StoreLogoffTransports
api_type:
- COM
ms.assetid: f21fba96-c5ca-4d41-9b93-c7955ab7327f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 30c91ec7a5a28b0c270da5223a2a245fb504d8c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421383"
---
# <a name="imapisupportstorelogofftransports"></a><span data-ttu-id="b0ea0-103">IMAPISupport::StoreLogoffTransports</span><span class="sxs-lookup"><span data-stu-id="b0ea0-103">IMAPISupport::StoreLogoffTransports</span></span>

  
  
<span data-ttu-id="b0ea0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b0ea0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b0ea0-105">メッセージ ストアの順序付きリリースを要求します。</span><span class="sxs-lookup"><span data-stu-id="b0ea0-105">Requests the orderly release of a message store.</span></span>
  
```cpp
HRESULT StoreLogoffTransports(
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="b0ea0-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b0ea0-106">Parameters</span></span>

 <span data-ttu-id="b0ea0-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="b0ea0-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="b0ea0-108">[in, out]メッセージ ストアログオフの発生方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="b0ea0-108">[in, out] A bitmask of flags that controls how message store logoff occurs.</span></span> <span data-ttu-id="b0ea0-109">入力では、このパラメーターのすべてのフラグは相互に排他的です。呼び出しごとに設定できるフラグは、次の 1 つのみです。</span><span class="sxs-lookup"><span data-stu-id="b0ea0-109">On input, all flags for this parameter are mutually exclusive; only one of the following flags can be set per call:</span></span>
    
<span data-ttu-id="b0ea0-110">LOGOFF_ABORT</span><span class="sxs-lookup"><span data-stu-id="b0ea0-110">LOGOFF_ABORT</span></span> 
  
> <span data-ttu-id="b0ea0-111">ログオフの前に、このストアのトランスポート プロバイダーアクティビティを停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b0ea0-111">Any transport provider activity for this store should be stopped before logoff.</span></span> <span data-ttu-id="b0ea0-112">アクティビティが停止し、MAPI スプーラーがストアからログオフした後、コントロールがクライアントに返されます。</span><span class="sxs-lookup"><span data-stu-id="b0ea0-112">Control is returned to the client after the activity is stopped and the MAPI spooler has logged off the store.</span></span> <span data-ttu-id="b0ea0-113">トランスポート アクティビティが発生している場合、ログオフは発生しません。MAPI スプーラーまたはトランスポート プロバイダーの動作に変更は発生しません。</span><span class="sxs-lookup"><span data-stu-id="b0ea0-113">If any transport activity is taking place, the logoff does not occur and no change in the MAPI spooler or transport provider behavior occurs.</span></span> <span data-ttu-id="b0ea0-114">現在アクティビティがない場合、MAPI スプーラーはストアを解放します。</span><span class="sxs-lookup"><span data-stu-id="b0ea0-114">If there is currently no activity, the MAPI spooler releases the store.</span></span> 
    
<span data-ttu-id="b0ea0-115">LOGOFF_NO_WAIT</span><span class="sxs-lookup"><span data-stu-id="b0ea0-115">LOGOFF_NO_WAIT</span></span> 
  
> <span data-ttu-id="b0ea0-116">MAPI スプーラーは、ストアを解放し、送信する準備ができているすべての送信メールが送信された直後にクライアントに制御を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="b0ea0-116">The MAPI spooler should release the store and return control to the client immediately after all outbound mail that is ready to be sent is sent.</span></span> <span data-ttu-id="b0ea0-117">メッセージ ストアに既定の受信トレイがある場合、インプロセス メッセージが受信され、それ以降の受信は無効になります。</span><span class="sxs-lookup"><span data-stu-id="b0ea0-117">If the message store has the default Inbox, any in-process message is received, and then further reception is disabled.</span></span> 
    
<span data-ttu-id="b0ea0-118">LOGOFF_ORDERLY</span><span class="sxs-lookup"><span data-stu-id="b0ea0-118">LOGOFF_ORDERLY</span></span> 
  
> <span data-ttu-id="b0ea0-119">MAPI スプーラーは、保留中のメッセージの処理が終了した直後にストアを解放し、クライアントにコントロールを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="b0ea0-119">The MAPI spooler should release the store and return control to the client immediately after any pending messages are finished processing.</span></span> <span data-ttu-id="b0ea0-120">新しいメッセージを処理する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="b0ea0-120">No new messages should be processed.</span></span> 
    
<span data-ttu-id="b0ea0-121">LOGOFF_PURGE</span><span class="sxs-lookup"><span data-stu-id="b0ea0-121">LOGOFF_PURGE</span></span> 
  
> <span data-ttu-id="b0ea0-122">このフラグと同LOGOFF_NO_WAITします。</span><span class="sxs-lookup"><span data-stu-id="b0ea0-122">Works the same as the LOGOFF_NO_WAIT flag.</span></span> <span data-ttu-id="b0ea0-123">このLOGOFF_PURGEは、完了後に呼び出し元に制御を返します。</span><span class="sxs-lookup"><span data-stu-id="b0ea0-123">The LOGOFF_PURGE flag returns control to the caller after completion.</span></span> 
    
<span data-ttu-id="b0ea0-124">LOGOFF_QUIET</span><span class="sxs-lookup"><span data-stu-id="b0ea0-124">LOGOFF_QUIET</span></span> 
  
> <span data-ttu-id="b0ea0-125">トランスポート プロバイダーのアクティビティが行われる場合、ログオフは発生しません。</span><span class="sxs-lookup"><span data-stu-id="b0ea0-125">The logoff should not occur if any transport provider activity is taking place.</span></span> <span data-ttu-id="b0ea0-126">行うアクティビティの種類は、出力時にフラグとして返されます。</span><span class="sxs-lookup"><span data-stu-id="b0ea0-126">The type of activity taking place is returned as a flag on output.</span></span>
    
    On output, MAPI spooler can return one or more of the following flags:
    
<span data-ttu-id="b0ea0-127">LOGOFF_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="b0ea0-127">LOGOFF_COMPLETE</span></span> 
  
> <span data-ttu-id="b0ea0-128">ログオフは完了できます。</span><span class="sxs-lookup"><span data-stu-id="b0ea0-128">The logoff can complete.</span></span> <span data-ttu-id="b0ea0-129">ストアに関連付けられているすべてのリソースが解放され、オブジェクトが無効になります。</span><span class="sxs-lookup"><span data-stu-id="b0ea0-129">All resources associated with the store have been released, and the object has been invalidated.</span></span> <span data-ttu-id="b0ea0-130">MAPI スプーラーが実行またはすべての要求を実行します。</span><span class="sxs-lookup"><span data-stu-id="b0ea0-130">The MAPI spooler has performed or will perform all requests.</span></span> <span data-ttu-id="b0ea0-131">この時点で呼び出す必要があるのは、メッセージ ストアの **IUnknown::Release** メソッドのみです。</span><span class="sxs-lookup"><span data-stu-id="b0ea0-131">Only the message store's **IUnknown::Release** method should be called at this point.</span></span> 
    
<span data-ttu-id="b0ea0-132">LOGOFF_INBOUND</span><span class="sxs-lookup"><span data-stu-id="b0ea0-132">LOGOFF_INBOUND</span></span> 
  
> <span data-ttu-id="b0ea0-133">現在、1 つ以上のトランスポート プロバイダーからストアにメッセージが送信されています。</span><span class="sxs-lookup"><span data-stu-id="b0ea0-133">A message is currently coming into the store from one or more transport providers.</span></span> 
    
<span data-ttu-id="b0ea0-134">LOGOFF_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="b0ea0-134">LOGOFF_OUTBOUND</span></span> 
  
> <span data-ttu-id="b0ea0-135">メッセージは現在、1 つ以上のトランスポート プロバイダーによってストアから送信されています。</span><span class="sxs-lookup"><span data-stu-id="b0ea0-135">A message is currently being sent from the store by one or more transport providers.</span></span> 
    
<span data-ttu-id="b0ea0-136">LOGOFF_OUTBOUND_QUEUE</span><span class="sxs-lookup"><span data-stu-id="b0ea0-136">LOGOFF_OUTBOUND_QUEUE</span></span> 
  
> <span data-ttu-id="b0ea0-137">現在、ストアの送信キューにメッセージがあります。</span><span class="sxs-lookup"><span data-stu-id="b0ea0-137">There are currently messages in the outbound queue for the store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b0ea0-138">戻り値</span><span class="sxs-lookup"><span data-stu-id="b0ea0-138">Return value</span></span>

<span data-ttu-id="b0ea0-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="b0ea0-139">S_OK</span></span> 
  
> <span data-ttu-id="b0ea0-140">ログオフ手順が成功しました。</span><span class="sxs-lookup"><span data-stu-id="b0ea0-140">The logoff procedure was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b0ea0-141">注釈</span><span class="sxs-lookup"><span data-stu-id="b0ea0-141">Remarks</span></span>

<span data-ttu-id="b0ea0-142">**IMAPISupport::StoreLogoffTransports** メソッドは、メッセージ ストア プロバイダーのサポート オブジェクトに実装されます。</span><span class="sxs-lookup"><span data-stu-id="b0ea0-142">The **IMAPISupport::StoreLogoffTransports** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="b0ea0-143">メッセージ ストア プロバイダーは **StoreLogoffTransports** を呼び出して、メッセージ ストアが閉じると、MAPI がトランスポート プロバイダーのアクティビティを処理する方法をクライアント アプリケーションに制御します。</span><span class="sxs-lookup"><span data-stu-id="b0ea0-143">Message store providers call **StoreLogoffTransports** to give client applications some control over how MAPI handles transport provider activity as a message store is closing.</span></span> 
  
<span data-ttu-id="b0ea0-144">別のプロセスで同じプロファイルに対してログオフするストアがある場合、MAPI は **StoreLogoffTransports** の呼び出しを無視し  _、lpulFlags_ パラメーターのフラグ LOGOFF_COMPLETE を返します。</span><span class="sxs-lookup"><span data-stu-id="b0ea0-144">If another process has the store to be logged off open for the same profile, MAPI ignores a call to **StoreLogoffTransports** and returns the flag LOGOFF_COMPLETE in the  _lpulFlags_ parameter.</span></span> 
  
<span data-ttu-id="b0ea0-145">**StoreLogoffTransports** からの戻り値に続くストア プロバイダーの動作は、システムの状態を示し、ログオフ動作のクライアント指示を伝える _lpulFlags_ の値に基づく必要があります。</span><span class="sxs-lookup"><span data-stu-id="b0ea0-145">The behavior of the store provider following the return from **StoreLogoffTransports** should be based on the value of  _lpulFlags_, which indicates system status and conveys client instructions for logoff behavior.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b0ea0-146">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="b0ea0-146">Notes to callers</span></span>

 <span data-ttu-id="b0ea0-147">**StoreLogoffTransports は** 、通常、ストア プロバイダーの [IMsgStore::StoreLogoff メソッドから呼び出](imsgstore-storelogoff.md) されます。</span><span class="sxs-lookup"><span data-stu-id="b0ea0-147">**StoreLogoffTransports** is typically called from a store provider's [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) method.</span></span> <span data-ttu-id="b0ea0-148">ただし、メッセージ ストアの **IUnknown::Release** メソッドから呼び出す場合があります。</span><span class="sxs-lookup"><span data-stu-id="b0ea0-148">However, it can also be called from the **IUnknown::Release** method of the message store.</span></span> <span data-ttu-id="b0ea0-149">メッセージ ストア **の Release** メソッドを実装して **、StoreLogoffTransports** の呼び出しが発生したかどうかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="b0ea0-149">Implement the **Release** method of your message store so you can check whether or not a call to **StoreLogoffTransports** has occurred.</span></span> <span data-ttu-id="b0ea0-150">呼び出しが発生していない場合は **、StoreLogoffTransports** を呼び出し、LOGOFF_ABORT設定します。</span><span class="sxs-lookup"><span data-stu-id="b0ea0-150">If a call has not occurred, call **StoreLogoffTransports** with the LOGOFF_ABORT flag set.</span></span> 
  
<span data-ttu-id="b0ea0-151">_lpulFlags_ パラメーターは、クライアントがメッセージ ストアのシャットダウンを要求する方法を示すフラグに設定されます。</span><span class="sxs-lookup"><span data-stu-id="b0ea0-151">The  _lpulFlags_ parameter is set to a flag that indicates how the client requires the message store to be shut down.</span></span> <span data-ttu-id="b0ea0-152">StoreLogoff の呼び出しで対応するパラメーターの設定に基づいて  _、ulFlags_ の適切な設定 **を決定します**。</span><span class="sxs-lookup"><span data-stu-id="b0ea0-152">Determine the appropriate setting for  _ulFlags_ based on the setting of the corresponding parameter in the call to **StoreLogoff**.</span></span> <span data-ttu-id="b0ea0-153">つまり、クライアントが _ulFlags_ を LOGOFF_ORDERLY に設定した **StoreLogoff** メソッドを呼び出した場合は、ulFlags を LOGOFF_ORDERLY に設定して **StoreLogoffTransports** を呼び出す必要があります。 </span><span class="sxs-lookup"><span data-stu-id="b0ea0-153">That is, if a client called your **StoreLogoff** method with  _ulFlags_ set to LOGOFF_ORDERLY, you should call **StoreLogoffTransports** with  _ulFlags_ set to LOGOFF_ORDERLY.</span></span> 
  
<span data-ttu-id="b0ea0-154">メッセージ ストア ログオフ プロセスの詳細については、「メッセージ ストア プロバイダーのシャットダウン [」を参照してください](shutting-down-a-message-store-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="b0ea0-154">For more information about the message store logoff process, see [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b0ea0-155">関連項目</span><span class="sxs-lookup"><span data-stu-id="b0ea0-155">See also</span></span>



[<span data-ttu-id="b0ea0-156">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="b0ea0-156">IMsgStore::StoreLogoff</span></span>](imsgstore-storelogoff.md)
  
[<span data-ttu-id="b0ea0-157">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="b0ea0-157">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
  
[<span data-ttu-id="b0ea0-158">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b0ea0-158">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

