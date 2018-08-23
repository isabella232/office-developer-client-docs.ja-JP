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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b77a58b04e5cdeee7a9e84051a6ed287c1a20115
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578312"
---
# <a name="imapisupportstorelogofftransports"></a><span data-ttu-id="815d0-103">IMAPISupport::StoreLogoffTransports</span><span class="sxs-lookup"><span data-stu-id="815d0-103">IMAPISupport::StoreLogoffTransports</span></span>

  
  
<span data-ttu-id="815d0-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="815d0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="815d0-105">メッセージ ストアの正常型解放を要求します。</span><span class="sxs-lookup"><span data-stu-id="815d0-105">Requests the orderly release of a message store.</span></span>
  
```cpp
HRESULT StoreLogoffTransports(
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="815d0-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="815d0-106">Parameters</span></span>

 <span data-ttu-id="815d0-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="815d0-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="815d0-108">[で [チェック アウト]メッセージ ストアのログオフが行われる方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="815d0-108">[in, out] A bitmask of flags that controls how message store logoff occurs.</span></span> <span data-ttu-id="815d0-109">入力ではこのパラメーターのすべてのフラグは相互に排他的です。呼び出しは、次のフラグの 1 つだけを設定できます。</span><span class="sxs-lookup"><span data-stu-id="815d0-109">On input, all flags for this parameter are mutually exclusive; only one of the following flags can be set per call:</span></span>
    
<span data-ttu-id="815d0-110">LOGOFF_ABORT</span><span class="sxs-lookup"><span data-stu-id="815d0-110">LOGOFF_ABORT</span></span> 
  
> <span data-ttu-id="815d0-111">ログオフする前に、このストア用のトランスポート プロバイダーのアクティビティを停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="815d0-111">Any transport provider activity for this store should be stopped before logoff.</span></span> <span data-ttu-id="815d0-112">活動が停止し、MAPI スプーラーがストアにログオフした後、コントロールがクライアントに返されます。</span><span class="sxs-lookup"><span data-stu-id="815d0-112">Control is returned to the client after the activity is stopped and the MAPI spooler has logged off the store.</span></span> <span data-ttu-id="815d0-113">場合は、任意のトランスポート処理が行われて、ログオフが発生しないと、MAPI スプーラーまたはトランスポート プロバイダーの動作の変更は行われません。</span><span class="sxs-lookup"><span data-stu-id="815d0-113">If any transport activity is taking place, the logoff does not occur and no change in the MAPI spooler or transport provider behavior occurs.</span></span> <span data-ttu-id="815d0-114">現在の活動はありません、MAPI スプーラーは、ストアを解放します。</span><span class="sxs-lookup"><span data-stu-id="815d0-114">If there is currently no activity, the MAPI spooler releases the store.</span></span> 
    
<span data-ttu-id="815d0-115">LOGOFF_NO_WAIT</span><span class="sxs-lookup"><span data-stu-id="815d0-115">LOGOFF_NO_WAIT</span></span> 
  
> <span data-ttu-id="815d0-116">MAPI スプーラーは、ストアを解放し、すべての送信メールを送信する準備が整っているが送信された直後に、コントロールをクライアントに返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="815d0-116">The MAPI spooler should release the store and return control to the client immediately after all outbound mail that is ready to be sent is sent.</span></span> <span data-ttu-id="815d0-117">メッセージ ・ ストアに既定の受信トレイがある場合は、任意のプロセスでメッセージを受信すると、それ以上の受信が無効になります。</span><span class="sxs-lookup"><span data-stu-id="815d0-117">If the message store has the default Inbox, any in-process message is received, and then further reception is disabled.</span></span> 
    
<span data-ttu-id="815d0-118">LOGOFF_ORDERLY</span><span class="sxs-lookup"><span data-stu-id="815d0-118">LOGOFF_ORDERLY</span></span> 
  
> <span data-ttu-id="815d0-119">MAPI スプーラーが、ストアを解放し、保留中のメッセージが終了した後すぐにクライアントに制御を返す必要がありますを処理します。</span><span class="sxs-lookup"><span data-stu-id="815d0-119">The MAPI spooler should release the store and return control to the client immediately after any pending messages are finished processing.</span></span> <span data-ttu-id="815d0-120">新しいメッセージは処理されません。</span><span class="sxs-lookup"><span data-stu-id="815d0-120">No new messages should be processed.</span></span> 
    
<span data-ttu-id="815d0-121">LOGOFF_PURGE</span><span class="sxs-lookup"><span data-stu-id="815d0-121">LOGOFF_PURGE</span></span> 
  
> <span data-ttu-id="815d0-122">LOGOFF_NO_WAIT フラグと同じように動作します。</span><span class="sxs-lookup"><span data-stu-id="815d0-122">Works the same as the LOGOFF_NO_WAIT flag.</span></span> <span data-ttu-id="815d0-123">LOGOFF_PURGE フラグは、完了した後、呼び出し側にコントロールを返します。</span><span class="sxs-lookup"><span data-stu-id="815d0-123">The LOGOFF_PURGE flag returns control to the caller after completion.</span></span> 
    
<span data-ttu-id="815d0-124">LOGOFF_QUIET</span><span class="sxs-lookup"><span data-stu-id="815d0-124">LOGOFF_QUIET</span></span> 
  
> <span data-ttu-id="815d0-125">ログオフする必要がありますトランスポート プロバイダーのすべてのアクティビティが行われる場合は発生しません。</span><span class="sxs-lookup"><span data-stu-id="815d0-125">The logoff should not occur if any transport provider activity is taking place.</span></span> <span data-ttu-id="815d0-126">出力フラグとして実行されているアクティビティの種類が返されます。</span><span class="sxs-lookup"><span data-stu-id="815d0-126">The type of activity taking place is returned as a flag on output.</span></span>
    
    On output, MAPI spooler can return one or more of the following flags:
    
<span data-ttu-id="815d0-127">LOGOFF_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="815d0-127">LOGOFF_COMPLETE</span></span> 
  
> <span data-ttu-id="815d0-128">ログオフを完了できます。</span><span class="sxs-lookup"><span data-stu-id="815d0-128">The logoff can complete.</span></span> <span data-ttu-id="815d0-129">ストアに関連付けられているすべてのリソースが解放されているし、オブジェクトが無効になっています。</span><span class="sxs-lookup"><span data-stu-id="815d0-129">All resources associated with the store have been released, and the object has been invalidated.</span></span> <span data-ttu-id="815d0-130">MAPI スプーラーを実行しているか、すべての要求が実行されます。</span><span class="sxs-lookup"><span data-stu-id="815d0-130">The MAPI spooler has performed or will perform all requests.</span></span> <span data-ttu-id="815d0-131">この時点で、メッセージ ・ ストアの**リ ス**のメソッドのみを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="815d0-131">Only the message store's **IUnknown::Release** method should be called at this point.</span></span> 
    
<span data-ttu-id="815d0-132">LOGOFF_INBOUND</span><span class="sxs-lookup"><span data-stu-id="815d0-132">LOGOFF_INBOUND</span></span> 
  
> <span data-ttu-id="815d0-133">メッセージ現在に由来してストアに 1 つまたは複数のトランスポート プロバイダー。</span><span class="sxs-lookup"><span data-stu-id="815d0-133">A message is currently coming into the store from one or more transport providers.</span></span> 
    
<span data-ttu-id="815d0-134">LOGOFF_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="815d0-134">LOGOFF_OUTBOUND</span></span> 
  
> <span data-ttu-id="815d0-135">1 つまたは複数のトランスポート プロバイダーによって、ストアからメッセージを送信されている現在は。</span><span class="sxs-lookup"><span data-stu-id="815d0-135">A message is currently being sent from the store by one or more transport providers.</span></span> 
    
<span data-ttu-id="815d0-136">LOGOFF_OUTBOUND_QUEUE</span><span class="sxs-lookup"><span data-stu-id="815d0-136">LOGOFF_OUTBOUND_QUEUE</span></span> 
  
> <span data-ttu-id="815d0-137">ストアの送信キューには現在のメッセージがあります。</span><span class="sxs-lookup"><span data-stu-id="815d0-137">There are currently messages in the outbound queue for the store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="815d0-138">�߂�l</span><span class="sxs-lookup"><span data-stu-id="815d0-138">Return value</span></span>

<span data-ttu-id="815d0-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="815d0-139">S_OK</span></span> 
  
> <span data-ttu-id="815d0-140">ログオフ プロシージャが正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="815d0-140">The logoff procedure was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="815d0-141">注釈</span><span class="sxs-lookup"><span data-stu-id="815d0-141">Remarks</span></span>

<span data-ttu-id="815d0-142">メッセージ ストア プロバイダーのサポート オブジェクトの**IMAPISupport::StoreLogoffTransports**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="815d0-142">The **IMAPISupport::StoreLogoffTransports** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="815d0-143">メッセージ ストア プロバイダーは、クライアント アプリケーションにメッセージ ・ ストアとして MAPI ハンドル トランスポート プロバイダーのアクティビティを終了する方法をある程度制御を提供する**StoreLogoffTransports**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="815d0-143">Message store providers call **StoreLogoffTransports** to give client applications some control over how MAPI handles transport provider activity as a message store is closing.</span></span> 
  
<span data-ttu-id="815d0-144">別のプロセスに同じプロファイルを開いてログオフするのには、ストアがある場合は、MAPI は**StoreLogoffTransports**への呼び出しを無視し、 _lpulFlags_パラメーターに LOGOFF_COMPLETE フラグを返します。</span><span class="sxs-lookup"><span data-stu-id="815d0-144">If another process has the store to be logged off open for the same profile, MAPI ignores a call to **StoreLogoffTransports** and returns the flag LOGOFF_COMPLETE in the  _lpulFlags_ parameter.</span></span> 
  
<span data-ttu-id="815d0-145">**StoreLogoffTransports**からの戻り値を次のストア プロバイダーの動作は、 _lpulFlags_システムの状態を示し、ログオフ時の動作については、クライアントに伝達するの値に基づいている必要があります。</span><span class="sxs-lookup"><span data-stu-id="815d0-145">The behavior of the store provider following the return from **StoreLogoffTransports** should be based on the value of  _lpulFlags_, which indicates system status and conveys client instructions for logoff behavior.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="815d0-146">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="815d0-146">Notes to callers</span></span>

 <span data-ttu-id="815d0-147">**StoreLogoffTransports**は、通常、ストア プロバイダーの[IMsgStore::StoreLogoff](imsgstore-storelogoff.md)メソッドから呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="815d0-147">**StoreLogoffTransports** is typically called from a store provider's [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) method.</span></span> <span data-ttu-id="815d0-148">ただしに呼び出すこともできます**が**メソッドのメッセージ ・ ストアから。</span><span class="sxs-lookup"><span data-stu-id="815d0-148">However, it can also be called from the **IUnknown::Release** method of the message store.</span></span> <span data-ttu-id="815d0-149">実装する**StoreLogoffTransports**への呼び出しが開始されているかどうかを確認することができますので、メッセージ ・ ストアの**Release**メソッドが発生しました。</span><span class="sxs-lookup"><span data-stu-id="815d0-149">Implement the **Release** method of your message store so you can check whether or not a call to **StoreLogoffTransports** has occurred.</span></span> <span data-ttu-id="815d0-150">呼び出しが実行されていない場合は、LOGOFF_ABORT フラグを設定して**StoreLogoffTransports**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="815d0-150">If a call has not occurred, call **StoreLogoffTransports** with the LOGOFF_ABORT flag set.</span></span> 
  
<span data-ttu-id="815d0-151">_LpulFlags_パラメーターは、クライアントがメッセージ ・ ストアをシャット ダウンする必要がありますを示すフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="815d0-151">The  _lpulFlags_ parameter is set to a flag that indicates how the client requires the message store to be shut down.</span></span> <span data-ttu-id="815d0-152">_UlFlags_ **StoreLogoff**への呼び出しに対応するパラメーターの設定に基づいて適切な設定を決定します。</span><span class="sxs-lookup"><span data-stu-id="815d0-152">Determine the appropriate setting for  _ulFlags_ based on the setting of the corresponding parameter in the call to **StoreLogoff**.</span></span> <span data-ttu-id="815d0-153">クライアントには、 _ulFlags_ LOGOFF_ORDERLY に設定すると、 **StoreLogoff**メソッドが呼び出されると、 _ulFlags_に LOGOFF_ORDERLY の設定で**StoreLogoffTransports**を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="815d0-153">That is, if a client called your **StoreLogoff** method with  _ulFlags_ set to LOGOFF_ORDERLY, you should call **StoreLogoffTransports** with  _ulFlags_ set to LOGOFF_ORDERLY.</span></span> 
  
<span data-ttu-id="815d0-154">メッセージ ストア ログオフ処理の詳細については、[シャット ダウン、メッセージ ストア プロバイダー](shutting-down-a-message-store-provider.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="815d0-154">For more information about the message store logoff process, see [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="815d0-155">関連項目</span><span class="sxs-lookup"><span data-stu-id="815d0-155">See also</span></span>



[<span data-ttu-id="815d0-156">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="815d0-156">IMsgStore::StoreLogoff</span></span>](imsgstore-storelogoff.md)
  
[<span data-ttu-id="815d0-157">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="815d0-157">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
  
[<span data-ttu-id="815d0-158">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="815d0-158">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

