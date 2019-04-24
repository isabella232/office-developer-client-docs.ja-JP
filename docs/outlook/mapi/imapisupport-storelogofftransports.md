---
title: imapisupportstorelogofftransports
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326496"
---
# <a name="imapisupportstorelogofftransports"></a><span data-ttu-id="57c58-103">IMAPISupport::StoreLogoffTransports</span><span class="sxs-lookup"><span data-stu-id="57c58-103">IMAPISupport::StoreLogoffTransports</span></span>

  
  
<span data-ttu-id="57c58-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="57c58-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="57c58-105">メッセージストアの正常なリリースを要求します。</span><span class="sxs-lookup"><span data-stu-id="57c58-105">Requests the orderly release of a message store.</span></span>
  
```cpp
HRESULT StoreLogoffTransports(
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="57c58-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="57c58-106">Parameters</span></span>

 <span data-ttu-id="57c58-107">_lアウトフラグ_</span><span class="sxs-lookup"><span data-stu-id="57c58-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="57c58-108">[入力]メッセージストアのログオフを実行する方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="57c58-108">[in, out] A bitmask of flags that controls how message store logoff occurs.</span></span> <span data-ttu-id="57c58-109">入力時に、このパラメーターのすべてのフラグは相互に排他的です。呼び出しごとに設定できるのは、次に示すフラグのいずれか1つだけです。</span><span class="sxs-lookup"><span data-stu-id="57c58-109">On input, all flags for this parameter are mutually exclusive; only one of the following flags can be set per call:</span></span>
    
<span data-ttu-id="57c58-110">LOGOFF_ABORT</span><span class="sxs-lookup"><span data-stu-id="57c58-110">LOGOFF_ABORT</span></span> 
  
> <span data-ttu-id="57c58-111">このストアのトランスポートプロバイダーのアクティビティは、ログオフの前に停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="57c58-111">Any transport provider activity for this store should be stopped before logoff.</span></span> <span data-ttu-id="57c58-112">アクティビティが停止し、MAPI スプーラーがストアからログオフした後に、制御がクライアントに返されます。</span><span class="sxs-lookup"><span data-stu-id="57c58-112">Control is returned to the client after the activity is stopped and the MAPI spooler has logged off the store.</span></span> <span data-ttu-id="57c58-113">いずれかのトランスポートアクティビティが行われている場合は、ログオフは行われず、MAPI スプーラーまたはトランスポートプロバイダーの動作が変更されることはありません。</span><span class="sxs-lookup"><span data-stu-id="57c58-113">If any transport activity is taking place, the logoff does not occur and no change in the MAPI spooler or transport provider behavior occurs.</span></span> <span data-ttu-id="57c58-114">現在、アクティビティがない場合、MAPI スプーラーはストアを解放します。</span><span class="sxs-lookup"><span data-stu-id="57c58-114">If there is currently no activity, the MAPI spooler releases the store.</span></span> 
    
<span data-ttu-id="57c58-115">LOGOFF_NO_WAIT</span><span class="sxs-lookup"><span data-stu-id="57c58-115">LOGOFF_NO_WAIT</span></span> 
  
> <span data-ttu-id="57c58-116">MAPI スプーラーは、送信できる状態になっているすべての送信メールが送信された直後に、ストアを解放し、制御をクライアントに返します。</span><span class="sxs-lookup"><span data-stu-id="57c58-116">The MAPI spooler should release the store and return control to the client immediately after all outbound mail that is ready to be sent is sent.</span></span> <span data-ttu-id="57c58-117">メッセージストアに既定の受信トレイがある場合は、処理中のメッセージを受信すると、さらに受信を無効にします。</span><span class="sxs-lookup"><span data-stu-id="57c58-117">If the message store has the default Inbox, any in-process message is received, and then further reception is disabled.</span></span> 
    
<span data-ttu-id="57c58-118">LOGOFF_ORDERLY</span><span class="sxs-lookup"><span data-stu-id="57c58-118">LOGOFF_ORDERLY</span></span> 
  
> <span data-ttu-id="57c58-119">MAPI スプーラーは、保留中のメッセージの処理が完了した直後にストアを解放し、制御をクライアントに返します。</span><span class="sxs-lookup"><span data-stu-id="57c58-119">The MAPI spooler should release the store and return control to the client immediately after any pending messages are finished processing.</span></span> <span data-ttu-id="57c58-120">新しいメッセージを処理する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="57c58-120">No new messages should be processed.</span></span> 
    
<span data-ttu-id="57c58-121">LOGOFF_PURGE</span><span class="sxs-lookup"><span data-stu-id="57c58-121">LOGOFF_PURGE</span></span> 
  
> <span data-ttu-id="57c58-122">LOGOFF_NO_WAIT フラグと同じ働きをします。</span><span class="sxs-lookup"><span data-stu-id="57c58-122">Works the same as the LOGOFF_NO_WAIT flag.</span></span> <span data-ttu-id="57c58-123">LOGOFF_PURGE フラグは、完了後に呼び出し元に制御を戻します。</span><span class="sxs-lookup"><span data-stu-id="57c58-123">The LOGOFF_PURGE flag returns control to the caller after completion.</span></span> 
    
<span data-ttu-id="57c58-124">LOGOFF_QUIET</span><span class="sxs-lookup"><span data-stu-id="57c58-124">LOGOFF_QUIET</span></span> 
  
> <span data-ttu-id="57c58-125">トランスポートプロバイダーのアクティビティが実行されている場合は、ログオフする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="57c58-125">The logoff should not occur if any transport provider activity is taking place.</span></span> <span data-ttu-id="57c58-126">実行されるアクティビティの種類は、出力のフラグとして返されます。</span><span class="sxs-lookup"><span data-stu-id="57c58-126">The type of activity taking place is returned as a flag on output.</span></span>
    
    On output, MAPI spooler can return one or more of the following flags:
    
<span data-ttu-id="57c58-127">LOGOFF_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="57c58-127">LOGOFF_COMPLETE</span></span> 
  
> <span data-ttu-id="57c58-128">ログオフを完了できます。</span><span class="sxs-lookup"><span data-stu-id="57c58-128">The logoff can complete.</span></span> <span data-ttu-id="57c58-129">ストアに関連付けられているすべてのリソースが解放され、オブジェクトが無効にされました。</span><span class="sxs-lookup"><span data-stu-id="57c58-129">All resources associated with the store have been released, and the object has been invalidated.</span></span> <span data-ttu-id="57c58-130">MAPI スプーラーが実行されたか、すべての要求を実行します。</span><span class="sxs-lookup"><span data-stu-id="57c58-130">The MAPI spooler has performed or will perform all requests.</span></span> <span data-ttu-id="57c58-131">この時点で、メッセージストアの**IUnknown:: Release**メソッドのみを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="57c58-131">Only the message store's **IUnknown::Release** method should be called at this point.</span></span> 
    
<span data-ttu-id="57c58-132">LOGOFF_INBOUND</span><span class="sxs-lookup"><span data-stu-id="57c58-132">LOGOFF_INBOUND</span></span> 
  
> <span data-ttu-id="57c58-133">メッセージが、1つまたは複数のトランスポートプロバイダーからストアに送られてきている。</span><span class="sxs-lookup"><span data-stu-id="57c58-133">A message is currently coming into the store from one or more transport providers.</span></span> 
    
<span data-ttu-id="57c58-134">LOGOFF_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="57c58-134">LOGOFF_OUTBOUND</span></span> 
  
> <span data-ttu-id="57c58-135">現在、1つ以上のトランスポートプロバイダーによってストアからメッセージが送信されています。</span><span class="sxs-lookup"><span data-stu-id="57c58-135">A message is currently being sent from the store by one or more transport providers.</span></span> 
    
<span data-ttu-id="57c58-136">LOGOFF_OUTBOUND_QUEUE</span><span class="sxs-lookup"><span data-stu-id="57c58-136">LOGOFF_OUTBOUND_QUEUE</span></span> 
  
> <span data-ttu-id="57c58-137">現在、ストアの送信キューにメッセージがあります。</span><span class="sxs-lookup"><span data-stu-id="57c58-137">There are currently messages in the outbound queue for the store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="57c58-138">戻り値</span><span class="sxs-lookup"><span data-stu-id="57c58-138">Return value</span></span>

<span data-ttu-id="57c58-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="57c58-139">S_OK</span></span> 
  
> <span data-ttu-id="57c58-140">ログオフ手順は正常に実行されました。</span><span class="sxs-lookup"><span data-stu-id="57c58-140">The logoff procedure was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="57c58-141">解説</span><span class="sxs-lookup"><span data-stu-id="57c58-141">Remarks</span></span>

<span data-ttu-id="57c58-142">**imapisupport:: storelogofftransports**メソッドは、メッセージストアプロバイダーサポートオブジェクトに対して実装されています。</span><span class="sxs-lookup"><span data-stu-id="57c58-142">The **IMAPISupport::StoreLogoffTransports** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="57c58-143">メッセージストアプロバイダーは、 **storelogofftransports**を呼び出して、クライアントアプリケーションに、メッセージストアを閉じるときのトランスポートプロバイダーアクティビティの処理方法を制御できるようにします。</span><span class="sxs-lookup"><span data-stu-id="57c58-143">Message store providers call **StoreLogoffTransports** to give client applications some control over how MAPI handles transport provider activity as a message store is closing.</span></span> 
  
<span data-ttu-id="57c58-144">別のプロセスが同じプロファイルに対してストアを開いて開いた場合、MAPI は**storelogofftransports**への呼び出しを無視し、 _lpulflags_パラメーターでフラグ LOGOFF_COMPLETE を返します。</span><span class="sxs-lookup"><span data-stu-id="57c58-144">If another process has the store to be logged off open for the same profile, MAPI ignores a call to **StoreLogoffTransports** and returns the flag LOGOFF_COMPLETE in the  _lpulFlags_ parameter.</span></span> 
  
<span data-ttu-id="57c58-145">**storelogofftransports**からの戻り値に続くストアプロバイダーの動作は、システム状態を示す_lpulflags_の値に基づいている必要があります。これは、システム状態を示し、ログオフ動作に関するクライアント命令を伝達します。</span><span class="sxs-lookup"><span data-stu-id="57c58-145">The behavior of the store provider following the return from **StoreLogoffTransports** should be based on the value of  _lpulFlags_, which indicates system status and conveys client instructions for logoff behavior.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="57c58-146">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="57c58-146">Notes to callers</span></span>

 <span data-ttu-id="57c58-147">**storelogofftransports**は、通常、ストアプロバイダーの[IMsgStore:: storelogoff](imsgstore-storelogoff.md)メソッドから呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="57c58-147">**StoreLogoffTransports** is typically called from a store provider's [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) method.</span></span> <span data-ttu-id="57c58-148">ただし、メッセージストアの**IUnknown:: Release**メソッドからも呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="57c58-148">However, it can also be called from the **IUnknown::Release** method of the message store.</span></span> <span data-ttu-id="57c58-149">**storelogofftransports**への呼び出しが発生したかどうかを確認できるように、メッセージストアの**Release**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="57c58-149">Implement the **Release** method of your message store so you can check whether or not a call to **StoreLogoffTransports** has occurred.</span></span> <span data-ttu-id="57c58-150">呼び出しが発生していない場合は、LOGOFF_ABORT フラグが設定された**storelogofftransports**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="57c58-150">If a call has not occurred, call **StoreLogoffTransports** with the LOGOFF_ABORT flag set.</span></span> 
  
<span data-ttu-id="57c58-151">_lアウト flags_パラメーターは、クライアントがメッセージストアをシャットダウンする必要があるかどうかを示すフラグに設定されています。</span><span class="sxs-lookup"><span data-stu-id="57c58-151">The  _lpulFlags_ parameter is set to a flag that indicates how the client requires the message store to be shut down.</span></span> <span data-ttu-id="57c58-152">**storelogoff**への呼び出しで対応するパラメーターの設定に基づいて、 _ulflags_に適切な設定を決定します。</span><span class="sxs-lookup"><span data-stu-id="57c58-152">Determine the appropriate setting for  _ulFlags_ based on the setting of the corresponding parameter in the call to **StoreLogoff**.</span></span> <span data-ttu-id="57c58-153">つまり、 _ulflags_を LOGOFF_ORDERLY に設定してクライアントが**storelogoff**メソッドを呼び出した場合は、 _ulflags_を LOGOFF_ORDERLY に設定して**storelogoffトランスポート**を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="57c58-153">That is, if a client called your **StoreLogoff** method with  _ulFlags_ set to LOGOFF_ORDERLY, you should call **StoreLogoffTransports** with  _ulFlags_ set to LOGOFF_ORDERLY.</span></span> 
  
<span data-ttu-id="57c58-154">メッセージストアのログオフプロセスの詳細については、「[メッセージストアプロバイダーのシャットダウン](shutting-down-a-message-store-provider.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="57c58-154">For more information about the message store logoff process, see [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="57c58-155">関連項目</span><span class="sxs-lookup"><span data-stu-id="57c58-155">See also</span></span>



[<span data-ttu-id="57c58-156">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="57c58-156">IMsgStore::StoreLogoff</span></span>](imsgstore-storelogoff.md)
  
[<span data-ttu-id="57c58-157">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="57c58-157">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
  
[<span data-ttu-id="57c58-158">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="57c58-158">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

