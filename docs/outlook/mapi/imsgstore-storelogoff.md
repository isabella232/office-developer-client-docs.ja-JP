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
# <a name="imsgstorestorelogoff"></a><span data-ttu-id="7d5e6-103">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="7d5e6-103">IMsgStore::StoreLogoff</span></span>

  
  
<span data-ttu-id="7d5e6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d5e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d5e6-105">メッセージ ストアの順序付けされたログオフを有効にします。</span><span class="sxs-lookup"><span data-stu-id="7d5e6-105">Enables the orderly logoff of the message store.</span></span>
  
```cpp
HRESULT StoreLogoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="7d5e6-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7d5e6-106">Parameters</span></span>

 <span data-ttu-id="7d5e6-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="7d5e6-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="7d5e6-108">[in, out]メッセージ ストアからのログオフを制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="7d5e6-108">[in, out] A bitmask of flags that controls logoff from the message store.</span></span> <span data-ttu-id="7d5e6-109">入力では、このパラメーターに設定されているフラグはすべて相互に排他的です。呼び出し元は、呼び出しごとに 1 つのフラグのみを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d5e6-109">On input, all flags set for this parameter are mutually exclusive; a caller must specify only one flag per call.</span></span> <span data-ttu-id="7d5e6-110">次のフラグは、入力時に有効です。</span><span class="sxs-lookup"><span data-stu-id="7d5e6-110">The following flags are valid on input:</span></span>
    
<span data-ttu-id="7d5e6-111">LOGOFF_ABORT</span><span class="sxs-lookup"><span data-stu-id="7d5e6-111">LOGOFF_ABORT</span></span> 
  
> <span data-ttu-id="7d5e6-112">ログオフの前に、このメッセージ ストアのトランスポート プロバイダーアクティビティを停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d5e6-112">Any transport provider activity for this message store should be stopped before logoff.</span></span> <span data-ttu-id="7d5e6-113">アクティビティが停止した後、呼び出し元に制御が返されます。</span><span class="sxs-lookup"><span data-stu-id="7d5e6-113">Control is returned to the caller after activity is stopped.</span></span> <span data-ttu-id="7d5e6-114">トランスポート プロバイダーのアクティビティが行われる場合、ログオフは発生しません。MAPI スプーラーまたはトランスポート プロバイダーの動作は変更されません。</span><span class="sxs-lookup"><span data-stu-id="7d5e6-114">If any transport provider activity is taking place, the logoff does not occur and no change in the behavior of the MAPI spooler or transport providers occurs.</span></span> <span data-ttu-id="7d5e6-115">トランスポート プロバイダーのアクティビティがアイドル状態の場合、MAPI スプーラーはストアを解放します。</span><span class="sxs-lookup"><span data-stu-id="7d5e6-115">If transport provider activity is idle, the MAPI spooler releases the store.</span></span> 
    
<span data-ttu-id="7d5e6-116">LOGOFF_NO_WAIT</span><span class="sxs-lookup"><span data-stu-id="7d5e6-116">LOGOFF_NO_WAIT</span></span> 
  
> <span data-ttu-id="7d5e6-117">メッセージ ストアは、閉じる前にトランスポート プロバイダーからのメッセージを待つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d5e6-117">The message store should not wait for messages from transport providers before closing.</span></span> <span data-ttu-id="7d5e6-118">送信する準備ができている送信メッセージが送信されます。</span><span class="sxs-lookup"><span data-stu-id="7d5e6-118">Outbound messages that are ready to be sent are sent.</span></span> <span data-ttu-id="7d5e6-119">このストアに既定の受信トレイが含まれている場合、インプロセス メッセージが受信され、さらに受信が無効になります。</span><span class="sxs-lookup"><span data-stu-id="7d5e6-119">If this store contains the default Inbox, any in-process messages are received, and then further reception is disabled.</span></span> <span data-ttu-id="7d5e6-120">すべてのアクティビティが完了すると、MAPI スプーラーはストアを解放し、コントロールはすぐに呼び出し元に返されます。</span><span class="sxs-lookup"><span data-stu-id="7d5e6-120">When all activity is complete, the MAPI spooler releases the store, and control is immediately returned to the caller.</span></span> 
    
<span data-ttu-id="7d5e6-121">LOGOFF_ORDERLY</span><span class="sxs-lookup"><span data-stu-id="7d5e6-121">LOGOFF_ORDERLY</span></span> 
  
> <span data-ttu-id="7d5e6-122">メッセージ ストアは、閉じる前にトランスポート プロバイダーからの情報を待つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d5e6-122">The message store should not wait for information from transport providers before closing.</span></span> <span data-ttu-id="7d5e6-123">現在処理中のメッセージは完了しますが、新しいメッセージは処理されません。</span><span class="sxs-lookup"><span data-stu-id="7d5e6-123">Messages that are currently being processed are completed, but no new messages are processed.</span></span> <span data-ttu-id="7d5e6-124">すべてのアクティビティが完了すると、MAPI スプーラーはストアを解放し、コントロールはすぐにストア プロバイダーに返されます。</span><span class="sxs-lookup"><span data-stu-id="7d5e6-124">When all activity is complete, the MAPI spooler releases the store, and control is immediately returned to the store provider.</span></span> 
    
<span data-ttu-id="7d5e6-125">LOGOFF_PURGE</span><span class="sxs-lookup"><span data-stu-id="7d5e6-125">LOGOFF_PURGE</span></span> 
  
> <span data-ttu-id="7d5e6-126">ログオフは、LOGOFF_NO_WAIT フラグが設定されている場合と同じように動作する必要がありますが、適切なトランスポート プロバイダーの [IXPLogon::FlushQueues](ixplogon-flushqueues.md) または [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d5e6-126">The logoff should work the same as if the LOGOFF_NO_WAIT flag is set, but either the [IXPLogon::FlushQueues](ixplogon-flushqueues.md) or [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method for the appropriate transport providers should be called.</span></span> <span data-ttu-id="7d5e6-127">このLOGOFF_PURGEは、完了後に呼び出し元に制御を返します。</span><span class="sxs-lookup"><span data-stu-id="7d5e6-127">The LOGOFF_PURGE flag returns control to the caller after completion.</span></span> 
    
<span data-ttu-id="7d5e6-128">LOGOFF_QUIET</span><span class="sxs-lookup"><span data-stu-id="7d5e6-128">LOGOFF_QUIET</span></span> 
  
> <span data-ttu-id="7d5e6-129">トランスポート プロバイダーのアクティビティが行われる場合、ログオフは発生しません。</span><span class="sxs-lookup"><span data-stu-id="7d5e6-129">If any transport provider activity is taking place, the logoff should not occur.</span></span>
    
    The following flags are valid on output:
    
<span data-ttu-id="7d5e6-130">LOGOFF_INBOUND</span><span class="sxs-lookup"><span data-stu-id="7d5e6-130">LOGOFF_INBOUND</span></span> 
  
> <span data-ttu-id="7d5e6-131">受信メッセージは現在到着中です。</span><span class="sxs-lookup"><span data-stu-id="7d5e6-131">Inbound messages are currently arriving.</span></span>
    
<span data-ttu-id="7d5e6-132">LOGOFF_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="7d5e6-132">LOGOFF_OUTBOUND</span></span> 
  
> <span data-ttu-id="7d5e6-133">送信メッセージは送信中です。</span><span class="sxs-lookup"><span data-stu-id="7d5e6-133">Outbound messages are in the process of being sent.</span></span>
    
<span data-ttu-id="7d5e6-134">LOGOFF_OUTBOUND_QUEUE</span><span class="sxs-lookup"><span data-stu-id="7d5e6-134">LOGOFF_OUTBOUND_QUEUE</span></span> 
  
> <span data-ttu-id="7d5e6-135">送信メッセージは保留中です (つまり、送信ボックスに含まれます)。</span><span class="sxs-lookup"><span data-stu-id="7d5e6-135">Outbound messages are pending (that is, they are in the Outbox).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7d5e6-136">戻り値</span><span class="sxs-lookup"><span data-stu-id="7d5e6-136">Return value</span></span>

<span data-ttu-id="7d5e6-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="7d5e6-137">S_OK</span></span> 
  
> <span data-ttu-id="7d5e6-138">ログオフは正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="7d5e6-138">The logoff completed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7d5e6-139">注釈</span><span class="sxs-lookup"><span data-stu-id="7d5e6-139">Remarks</span></span>

<span data-ttu-id="7d5e6-140">**IMsgStore::StoreLogoff** メソッドは、ログオフ プロセス中のメッセージ ストアとトランスポート プロバイダーの相互作用を制御します。</span><span class="sxs-lookup"><span data-stu-id="7d5e6-140">The **IMsgStore::StoreLogoff** method exerts control over the interaction of the message store and transport providers during the logoff process.</span></span> <span data-ttu-id="7d5e6-141">**StoreLogoff の呼び** 出しは、呼び出し元によってのみ使用されているメッセージ ストアでのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="7d5e6-141">Calling **StoreLogoff** is valid only for message stores that are being used only by the caller.</span></span> <span data-ttu-id="7d5e6-142">たとえば、2 つのクライアントが同じメッセージ ストアを使用し、そのうちの 1 つが **StoreLogoff** を呼び出す場合、メッセージ ストアはすぐに解放され、コントロールは呼び出し元のクライアントに返されます。</span><span class="sxs-lookup"><span data-stu-id="7d5e6-142">For example, when two clients are using the same message store and one of them calls **StoreLogoff**, the message store is immediately released and control is returned to the calling client.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7d5e6-143">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="7d5e6-143">Notes to implementers</span></span>

<span data-ttu-id="7d5e6-144">**STORELogoff** に渡されるフラグを保存し [、IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md)メソッドを呼び出す際に渡します。</span><span class="sxs-lookup"><span data-stu-id="7d5e6-144">Save the flags that are passed to **StoreLogoff** and pass them when you call the [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) method.</span></span> <span data-ttu-id="7d5e6-145">メッセージ ストアの参照カウントが 0 に低下するまで **、StoreLogoffTransports** を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d5e6-145">Do not call **StoreLogoffTransports** until the message store's reference count drops to zero.</span></span> <span data-ttu-id="7d5e6-146">**StoreLogoffTransports への複数の呼び出しは、** 保存されたフラグを上書きするだけで済む。</span><span class="sxs-lookup"><span data-stu-id="7d5e6-146">Multiple calls to **StoreLogoffTransports** simply overwrite the saved flags.</span></span> 
  
<span data-ttu-id="7d5e6-147">メッセージ ストアの参照カウントが 0 に達する前に **StoreLogoff** に呼び出しが行われた場合は **、StoreLogoffTransports** に渡す _ulFlags_ パラメーターに LOGOFF_ABORT フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="7d5e6-147">If no call has been made to **StoreLogoff** before the message store's reference count reaches zero, set the LOGOFF_ABORT flag in the  _ulFlags_ parameter that you pass to **StoreLogoffTransports**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7d5e6-148">関連項目</span><span class="sxs-lookup"><span data-stu-id="7d5e6-148">See also</span></span>



[<span data-ttu-id="7d5e6-149">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="7d5e6-149">IMAPIStatus::FlushQueues</span></span>](imapistatus-flushqueues.md)
  
[<span data-ttu-id="7d5e6-150">IMAPISupport::StoreLogoffTransports</span><span class="sxs-lookup"><span data-stu-id="7d5e6-150">IMAPISupport::StoreLogoffTransports</span></span>](imapisupport-storelogofftransports.md)
  
[<span data-ttu-id="7d5e6-151">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="7d5e6-151">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
  
[<span data-ttu-id="7d5e6-152">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7d5e6-152">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

