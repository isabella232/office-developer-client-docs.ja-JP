---
title: IMsgStoreStoreLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.StoreLogoff
api_type:
- COM
ms.assetid: 3773c98e-531e-4bdc-a39a-2c3bb7378cd3
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: be11c536804682d1baec8188b6d7487c71d411e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424337"
---
# <a name="imsgstorestorelogoff"></a><span data-ttu-id="04bb8-103">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="04bb8-103">IMsgStore::StoreLogoff</span></span>

  
  
<span data-ttu-id="04bb8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="04bb8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="04bb8-105">メッセージストアの正常なログオフを有効にします。</span><span class="sxs-lookup"><span data-stu-id="04bb8-105">Enables the orderly logoff of the message store.</span></span>
  
```cpp
HRESULT StoreLogoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="04bb8-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="04bb8-106">Parameters</span></span>

 <span data-ttu-id="04bb8-107">_lアウトフラグ_</span><span class="sxs-lookup"><span data-stu-id="04bb8-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="04bb8-108">[入力]メッセージストアからのログオフを制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="04bb8-108">[in, out] A bitmask of flags that controls logoff from the message store.</span></span> <span data-ttu-id="04bb8-109">入力時に、このパラメーターに設定されているすべてのフラグは相互に排他的です。発信者は、呼び出しごとに1つのフラグのみを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="04bb8-109">On input, all flags set for this parameter are mutually exclusive; a caller must specify only one flag per call.</span></span> <span data-ttu-id="04bb8-110">入力に対して有効なフラグは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="04bb8-110">The following flags are valid on input:</span></span>
    
<span data-ttu-id="04bb8-111">LOGOFF_ABORT</span><span class="sxs-lookup"><span data-stu-id="04bb8-111">LOGOFF_ABORT</span></span> 
  
> <span data-ttu-id="04bb8-112">このメッセージストアのトランスポートプロバイダーのアクティビティは、ログオフの前に停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="04bb8-112">Any transport provider activity for this message store should be stopped before logoff.</span></span> <span data-ttu-id="04bb8-113">アクティビティが停止した後、制御が発信者に返されます。</span><span class="sxs-lookup"><span data-stu-id="04bb8-113">Control is returned to the caller after activity is stopped.</span></span> <span data-ttu-id="04bb8-114">トランスポートプロバイダーの処理が行われている場合は、ログオフは行われず、MAPI スプーラーまたはトランスポートプロバイダーの動作に対する変更は行われません。</span><span class="sxs-lookup"><span data-stu-id="04bb8-114">If any transport provider activity is taking place, the logoff does not occur and no change in the behavior of the MAPI spooler or transport providers occurs.</span></span> <span data-ttu-id="04bb8-115">トランスポートプロバイダーのアクティビティがアイドル状態の場合、MAPI スプーラーはストアを解放します。</span><span class="sxs-lookup"><span data-stu-id="04bb8-115">If transport provider activity is idle, the MAPI spooler releases the store.</span></span> 
    
<span data-ttu-id="04bb8-116">LOGOFF_NO_WAIT</span><span class="sxs-lookup"><span data-stu-id="04bb8-116">LOGOFF_NO_WAIT</span></span> 
  
> <span data-ttu-id="04bb8-117">メッセージストアは、閉じる前にトランスポートプロバイダーからのメッセージを待機することはできません。</span><span class="sxs-lookup"><span data-stu-id="04bb8-117">The message store should not wait for messages from transport providers before closing.</span></span> <span data-ttu-id="04bb8-118">送信できる状態の送信メッセージが送信されます。</span><span class="sxs-lookup"><span data-stu-id="04bb8-118">Outbound messages that are ready to be sent are sent.</span></span> <span data-ttu-id="04bb8-119">このストアに既定の受信トレイが含まれている場合は、処理中のメッセージが受信されると、さらに受信は無効になります。</span><span class="sxs-lookup"><span data-stu-id="04bb8-119">If this store contains the default Inbox, any in-process messages are received, and then further reception is disabled.</span></span> <span data-ttu-id="04bb8-120">すべてのアクティビティが完了すると、MAPI スプーラーはストアを解放し、コントロールはすぐに呼び出し元に返されます。</span><span class="sxs-lookup"><span data-stu-id="04bb8-120">When all activity is complete, the MAPI spooler releases the store, and control is immediately returned to the caller.</span></span> 
    
<span data-ttu-id="04bb8-121">LOGOFF_ORDERLY</span><span class="sxs-lookup"><span data-stu-id="04bb8-121">LOGOFF_ORDERLY</span></span> 
  
> <span data-ttu-id="04bb8-122">メッセージストアは、閉じる前にトランスポートプロバイダーからの情報を待つことはできません。</span><span class="sxs-lookup"><span data-stu-id="04bb8-122">The message store should not wait for information from transport providers before closing.</span></span> <span data-ttu-id="04bb8-123">現在処理中のメッセージは完了しますが、新しいメッセージは処理されません。</span><span class="sxs-lookup"><span data-stu-id="04bb8-123">Messages that are currently being processed are completed, but no new messages are processed.</span></span> <span data-ttu-id="04bb8-124">すべてのアクティビティが完了すると、MAPI スプーラーがストアを解放し、その直後に control がストアプロバイダーに返されます。</span><span class="sxs-lookup"><span data-stu-id="04bb8-124">When all activity is complete, the MAPI spooler releases the store, and control is immediately returned to the store provider.</span></span> 
    
<span data-ttu-id="04bb8-125">LOGOFF_PURGE</span><span class="sxs-lookup"><span data-stu-id="04bb8-125">LOGOFF_PURGE</span></span> 
  
> <span data-ttu-id="04bb8-126">ログオフは、LOGOFF_NO_WAIT フラグが設定されている場合と同じように動作しますが、適切なトランスポートプロバイダーの[IXPLogon:: flushqueues](ixplogon-flushqueues.md)または[imapistatus:: flushqueues](imapistatus-flushqueues.md)メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="04bb8-126">The logoff should work the same as if the LOGOFF_NO_WAIT flag is set, but either the [IXPLogon::FlushQueues](ixplogon-flushqueues.md) or [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method for the appropriate transport providers should be called.</span></span> <span data-ttu-id="04bb8-127">LOGOFF_PURGE フラグは、完了後に呼び出し元に制御を戻します。</span><span class="sxs-lookup"><span data-stu-id="04bb8-127">The LOGOFF_PURGE flag returns control to the caller after completion.</span></span> 
    
<span data-ttu-id="04bb8-128">LOGOFF_QUIET</span><span class="sxs-lookup"><span data-stu-id="04bb8-128">LOGOFF_QUIET</span></span> 
  
> <span data-ttu-id="04bb8-129">トランスポートプロバイダーの操作が行われている場合は、ログオフを行わないでください。</span><span class="sxs-lookup"><span data-stu-id="04bb8-129">If any transport provider activity is taking place, the logoff should not occur.</span></span>
    
    The following flags are valid on output:
    
<span data-ttu-id="04bb8-130">LOGOFF_INBOUND</span><span class="sxs-lookup"><span data-stu-id="04bb8-130">LOGOFF_INBOUND</span></span> 
  
> <span data-ttu-id="04bb8-131">受信メッセージは現在到着しています。</span><span class="sxs-lookup"><span data-stu-id="04bb8-131">Inbound messages are currently arriving.</span></span>
    
<span data-ttu-id="04bb8-132">LOGOFF_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="04bb8-132">LOGOFF_OUTBOUND</span></span> 
  
> <span data-ttu-id="04bb8-133">送信メッセージの送信中です。</span><span class="sxs-lookup"><span data-stu-id="04bb8-133">Outbound messages are in the process of being sent.</span></span>
    
<span data-ttu-id="04bb8-134">LOGOFF_OUTBOUND_QUEUE</span><span class="sxs-lookup"><span data-stu-id="04bb8-134">LOGOFF_OUTBOUND_QUEUE</span></span> 
  
> <span data-ttu-id="04bb8-135">送信メッセージが保留中 (つまり、送信トレイにある)。</span><span class="sxs-lookup"><span data-stu-id="04bb8-135">Outbound messages are pending (that is, they are in the Outbox).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="04bb8-136">戻り値</span><span class="sxs-lookup"><span data-stu-id="04bb8-136">Return value</span></span>

<span data-ttu-id="04bb8-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="04bb8-137">S_OK</span></span> 
  
> <span data-ttu-id="04bb8-138">ログオフが正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="04bb8-138">The logoff completed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="04bb8-139">注釈</span><span class="sxs-lookup"><span data-stu-id="04bb8-139">Remarks</span></span>

<span data-ttu-id="04bb8-140">**IMsgStore:: storelogoff**メソッドは、ログオフプロセス中に、メッセージストアとトランスポートプロバイダーの相互作用について制御を exerts します。</span><span class="sxs-lookup"><span data-stu-id="04bb8-140">The **IMsgStore::StoreLogoff** method exerts control over the interaction of the message store and transport providers during the logoff process.</span></span> <span data-ttu-id="04bb8-141">**storelogoff**の呼び出しは、発信者のみが使用しているメッセージストアに対してのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="04bb8-141">Calling **StoreLogoff** is valid only for message stores that are being used only by the caller.</span></span> <span data-ttu-id="04bb8-142">たとえば、2つのクライアントが同じメッセージストアを使用していて、そのうちの1人が**storelogoff**を呼び出すと、メッセージストアが直ちに解放され、制御が呼び出し元クライアントに返されます。</span><span class="sxs-lookup"><span data-stu-id="04bb8-142">For example, when two clients are using the same message store and one of them calls **StoreLogoff**, the message store is immediately released and control is returned to the calling client.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="04bb8-143">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="04bb8-143">Notes to implementers</span></span>

<span data-ttu-id="04bb8-144">**storelogoff**に渡されるフラグを保存し、 [imapisupport:: storelogoffトランスポート](imapisupport-storelogofftransports.md)メソッドを呼び出すときに渡します。</span><span class="sxs-lookup"><span data-stu-id="04bb8-144">Save the flags that are passed to **StoreLogoff** and pass them when you call the [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) method.</span></span> <span data-ttu-id="04bb8-145">メッセージストアの参照カウントが0になるまで、 **storelogofftransports**を呼び出しません。</span><span class="sxs-lookup"><span data-stu-id="04bb8-145">Do not call **StoreLogoffTransports** until the message store's reference count drops to zero.</span></span> <span data-ttu-id="04bb8-146">**storelogofftransports**への複数の呼び出しは、保存されたフラグを上書きするだけです。</span><span class="sxs-lookup"><span data-stu-id="04bb8-146">Multiple calls to **StoreLogoffTransports** simply overwrite the saved flags.</span></span> 
  
<span data-ttu-id="04bb8-147">メッセージストアの参照カウントが0になる前に**storelogoff**に呼び出しが行われていない場合は、 **storelogoffトランスポート**に渡す_ulflags_パラメーターに LOGOFF_ABORT フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="04bb8-147">If no call has been made to **StoreLogoff** before the message store's reference count reaches zero, set the LOGOFF_ABORT flag in the  _ulFlags_ parameter that you pass to **StoreLogoffTransports**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="04bb8-148">関連項目</span><span class="sxs-lookup"><span data-stu-id="04bb8-148">See also</span></span>



[<span data-ttu-id="04bb8-149">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="04bb8-149">IMAPIStatus::FlushQueues</span></span>](imapistatus-flushqueues.md)
  
[<span data-ttu-id="04bb8-150">IMAPISupport::StoreLogoffTransports</span><span class="sxs-lookup"><span data-stu-id="04bb8-150">IMAPISupport::StoreLogoffTransports</span></span>](imapisupport-storelogofftransports.md)
  
[<span data-ttu-id="04bb8-151">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="04bb8-151">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
  
[<span data-ttu-id="04bb8-152">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="04bb8-152">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

