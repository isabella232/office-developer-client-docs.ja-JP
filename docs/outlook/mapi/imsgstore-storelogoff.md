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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a55fc361120472473bcba70152c153fb7824fb9e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566552"
---
# <a name="imsgstorestorelogoff"></a><span data-ttu-id="a1663-103">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="a1663-103">IMsgStore::StoreLogoff</span></span>

  
  
<span data-ttu-id="a1663-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1663-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1663-105">メッセージ ・ ストアの通常のログオフを有効にします。</span><span class="sxs-lookup"><span data-stu-id="a1663-105">Enables the orderly logoff of the message store.</span></span>
  
```cpp
HRESULT StoreLogoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a1663-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a1663-106">Parameters</span></span>

 <span data-ttu-id="a1663-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="a1663-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="a1663-108">[で [チェック アウト]メッセージ ・ ストアからのログオフを制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="a1663-108">[in, out] A bitmask of flags that controls logoff from the message store.</span></span> <span data-ttu-id="a1663-109">入力ではこのパラメーターの設定のすべてのフラグは相互に排他的です。呼び出し元は呼び出しごとの 1 つだけのフラグを指定しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="a1663-109">On input, all flags set for this parameter are mutually exclusive; a caller must specify only one flag per call.</span></span> <span data-ttu-id="a1663-110">次のフラグは、入力時に有効です。</span><span class="sxs-lookup"><span data-stu-id="a1663-110">The following flags are valid on input:</span></span>
    
<span data-ttu-id="a1663-111">LOGOFF_ABORT</span><span class="sxs-lookup"><span data-stu-id="a1663-111">LOGOFF_ABORT</span></span> 
  
> <span data-ttu-id="a1663-112">ログオフする前に、このメッセージ ストア用のトランスポート プロバイダーのアクティビティを停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a1663-112">Any transport provider activity for this message store should be stopped before logoff.</span></span> <span data-ttu-id="a1663-113">アクティビティが停止した後、呼び出し元に制御が返されます。</span><span class="sxs-lookup"><span data-stu-id="a1663-113">Control is returned to the caller after activity is stopped.</span></span> <span data-ttu-id="a1663-114">トランスポート プロバイダーのすべてのアクティビティが行われて場合、ログオフが発生しないと、MAPI スプーラーまたはトランスポート プロバイダーの動作の変更は行われません。</span><span class="sxs-lookup"><span data-stu-id="a1663-114">If any transport provider activity is taking place, the logoff does not occur and no change in the behavior of the MAPI spooler or transport providers occurs.</span></span> <span data-ttu-id="a1663-115">トランスポート プロバイダーのアクティビティがアイドル状態の場合は、MAPI スプーラーは、ストアを解放します。</span><span class="sxs-lookup"><span data-stu-id="a1663-115">If transport provider activity is idle, the MAPI spooler releases the store.</span></span> 
    
<span data-ttu-id="a1663-116">LOGOFF_NO_WAIT</span><span class="sxs-lookup"><span data-stu-id="a1663-116">LOGOFF_NO_WAIT</span></span> 
  
> <span data-ttu-id="a1663-117">メッセージ ・ ストアを閉じる前に、トランスポート プロバイダーからのメッセージを待たないようにします。</span><span class="sxs-lookup"><span data-stu-id="a1663-117">The message store should not wait for messages from transport providers before closing.</span></span> <span data-ttu-id="a1663-118">送信メッセージを送信する準備ができているが送信されます。</span><span class="sxs-lookup"><span data-stu-id="a1663-118">Outbound messages that are ready to be sent are sent.</span></span> <span data-ttu-id="a1663-119">このストアに既定の受信トレイが含まれている場合、処理中のメッセージが受信されると、それ以上の受信が無効になります。</span><span class="sxs-lookup"><span data-stu-id="a1663-119">If this store contains the default Inbox, any in-process messages are received, and then further reception is disabled.</span></span> <span data-ttu-id="a1663-120">すべてのアクティビティが完了すると、MAPI スプーラーが、ストアを解放し、コントロールが呼び出し元にすぐに返されます。</span><span class="sxs-lookup"><span data-stu-id="a1663-120">When all activity is complete, the MAPI spooler releases the store, and control is immediately returned to the caller.</span></span> 
    
<span data-ttu-id="a1663-121">LOGOFF_ORDERLY</span><span class="sxs-lookup"><span data-stu-id="a1663-121">LOGOFF_ORDERLY</span></span> 
  
> <span data-ttu-id="a1663-122">メッセージ ・ ストアを閉じる前に、トランスポート プロバイダーから情報を待たないようにします。</span><span class="sxs-lookup"><span data-stu-id="a1663-122">The message store should not wait for information from transport providers before closing.</span></span> <span data-ttu-id="a1663-123">現在処理されているメッセージは完了しましたが、新しいメッセージは処理されません。</span><span class="sxs-lookup"><span data-stu-id="a1663-123">Messages that are currently being processed are completed, but no new messages are processed.</span></span> <span data-ttu-id="a1663-124">すべてのアクティビティが完了すると、MAPI スプーラーが、ストアを解放し、コントロールは、ストア プロバイダーをすぐに返されます。</span><span class="sxs-lookup"><span data-stu-id="a1663-124">When all activity is complete, the MAPI spooler releases the store, and control is immediately returned to the store provider.</span></span> 
    
<span data-ttu-id="a1663-125">LOGOFF_PURGE</span><span class="sxs-lookup"><span data-stu-id="a1663-125">LOGOFF_PURGE</span></span> 
  
> <span data-ttu-id="a1663-126">ログオフする必要があります作業、同じ LOGOFF_NO_WAIT のフラグが設定されていますが、適切なトランスポート プロバイダーの[IXPLogon::FlushQueues](ixplogon-flushqueues.md)または[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)のいずれかのメソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="a1663-126">The logoff should work the same as if the LOGOFF_NO_WAIT flag is set, but either the [IXPLogon::FlushQueues](ixplogon-flushqueues.md) or [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method for the appropriate transport providers should be called.</span></span> <span data-ttu-id="a1663-127">LOGOFF_PURGE フラグは、完了した後、呼び出し側にコントロールを返します。</span><span class="sxs-lookup"><span data-stu-id="a1663-127">The LOGOFF_PURGE flag returns control to the caller after completion.</span></span> 
    
<span data-ttu-id="a1663-128">LOGOFF_QUIET</span><span class="sxs-lookup"><span data-stu-id="a1663-128">LOGOFF_QUIET</span></span> 
  
> <span data-ttu-id="a1663-129">トランスポート プロバイダーのすべてのアクティビティが行われて、ログオフが発生しませんする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a1663-129">If any transport provider activity is taking place, the logoff should not occur.</span></span>
    
    The following flags are valid on output:
    
<span data-ttu-id="a1663-130">LOGOFF_INBOUND</span><span class="sxs-lookup"><span data-stu-id="a1663-130">LOGOFF_INBOUND</span></span> 
  
> <span data-ttu-id="a1663-131">受信メッセージが到着した現在。</span><span class="sxs-lookup"><span data-stu-id="a1663-131">Inbound messages are currently arriving.</span></span>
    
<span data-ttu-id="a1663-132">LOGOFF_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="a1663-132">LOGOFF_OUTBOUND</span></span> 
  
> <span data-ttu-id="a1663-133">送信処理中は、メッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="a1663-133">Outbound messages are in the process of being sent.</span></span>
    
<span data-ttu-id="a1663-134">LOGOFF_OUTBOUND_QUEUE</span><span class="sxs-lookup"><span data-stu-id="a1663-134">LOGOFF_OUTBOUND_QUEUE</span></span> 
  
> <span data-ttu-id="a1663-135">送信メッセージは保留中 (つまり、それらが送信トレイに)。</span><span class="sxs-lookup"><span data-stu-id="a1663-135">Outbound messages are pending (that is, they are in the Outbox).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a1663-136">�߂�l</span><span class="sxs-lookup"><span data-stu-id="a1663-136">Return value</span></span>

<span data-ttu-id="a1663-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="a1663-137">S_OK</span></span> 
  
> <span data-ttu-id="a1663-138">ログオフが正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="a1663-138">The logoff completed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a1663-139">注釈</span><span class="sxs-lookup"><span data-stu-id="a1663-139">Remarks</span></span>

<span data-ttu-id="a1663-140">**IMsgStore::StoreLogoff**メソッドは、コントロールを行使メッセージの相互関係を保存し、トランスポート プロバイダーのログオフ処理中にします。</span><span class="sxs-lookup"><span data-stu-id="a1663-140">The **IMsgStore::StoreLogoff** method exerts control over the interaction of the message store and transport providers during the logoff process.</span></span> <span data-ttu-id="a1663-141">**StoreLogoff**の呼び出しは、呼び出し元だけが使用されているメッセージ ストアに対してのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="a1663-141">Calling **StoreLogoff** is valid only for message stores that are being used only by the caller.</span></span> <span data-ttu-id="a1663-142">などの 2 つのクライアントは、同じメッセージ ストアを使用しているし、 **StoreLogoff**を呼び出すことのいずれか、メッセージ ・ ストアがすぐに解放され、コントロールが呼び出し元のクライアントに返されます。</span><span class="sxs-lookup"><span data-stu-id="a1663-142">For example, when two clients are using the same message store and one of them calls **StoreLogoff**, the message store is immediately released and control is returned to the calling client.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a1663-143">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="a1663-143">Notes to implementers</span></span>

<span data-ttu-id="a1663-144">**StoreLogoff**に渡されるフラグを保存し、 [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md)メソッドを呼び出すと、それらを渡します。</span><span class="sxs-lookup"><span data-stu-id="a1663-144">Save the flags that are passed to **StoreLogoff** and pass them when you call the [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) method.</span></span> <span data-ttu-id="a1663-145">メッセージ ストアの参照カウントがゼロになるまで、 **StoreLogoffTransports**を呼び出さないようにします。</span><span class="sxs-lookup"><span data-stu-id="a1663-145">Do not call **StoreLogoffTransports** until the message store's reference count drops to zero.</span></span> <span data-ttu-id="a1663-146">**StoreLogoffTransports**に複数の呼び出しは、単に保存済みのフラグを上書きします。</span><span class="sxs-lookup"><span data-stu-id="a1663-146">Multiple calls to **StoreLogoffTransports** simply overwrite the saved flags.</span></span> 
  
<span data-ttu-id="a1663-147">**StoreLogoff**への呼び出しが行われない場合は、メッセージの前にストアの参照カウントがゼロになる、 **StoreLogoffTransports**に渡す_ulFlags_パラメーターに LOGOFF_ABORT フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="a1663-147">If no call has been made to **StoreLogoff** before the message store's reference count reaches zero, set the LOGOFF_ABORT flag in the  _ulFlags_ parameter that you pass to **StoreLogoffTransports**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a1663-148">関連項目</span><span class="sxs-lookup"><span data-stu-id="a1663-148">See also</span></span>



[<span data-ttu-id="a1663-149">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="a1663-149">IMAPIStatus::FlushQueues</span></span>](imapistatus-flushqueues.md)
  
[<span data-ttu-id="a1663-150">IMAPISupport::StoreLogoffTransports</span><span class="sxs-lookup"><span data-stu-id="a1663-150">IMAPISupport::StoreLogoffTransports</span></span>](imapisupport-storelogofftransports.md)
  
[<span data-ttu-id="a1663-151">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="a1663-151">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
  
[<span data-ttu-id="a1663-152">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a1663-152">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

