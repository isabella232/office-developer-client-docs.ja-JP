---
title: IMsgStoreSetLockState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.SetLockState
api_type:
- COM
ms.assetid: 4b1176ec-4126-43f5-856d-cbab8d622825
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9eeede2a430f5186daf429dd6ed59f312ae334be
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423630"
---
# <a name="imsgstoresetlockstate"></a><span data-ttu-id="c355f-103">IMsgStore::SetLockState</span><span class="sxs-lookup"><span data-stu-id="c355f-103">IMsgStore::SetLockState</span></span>

  
  
<span data-ttu-id="c355f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c355f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c355f-105">メッセージをロックまたはロック解除します。</span><span class="sxs-lookup"><span data-stu-id="c355f-105">Locks or unlocks a message.</span></span> <span data-ttu-id="c355f-106">このメソッドは、MAPI スプーラーによってのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="c355f-106">This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT SetLockState(
  LPMESSAGE lpMessage,
  ULONG ulLockState  
);
```

## <a name="parameters"></a><span data-ttu-id="c355f-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c355f-107">Parameters</span></span>

 <span data-ttu-id="c355f-108">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="c355f-108">_lpMessage_</span></span>
  
> <span data-ttu-id="c355f-109">[in]ロックまたはロック解除を行うメッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="c355f-109">[in] A pointer to the message to lock or unlock.</span></span>
    
 <span data-ttu-id="c355f-110">_ulLockState_</span><span class="sxs-lookup"><span data-stu-id="c355f-110">_ulLockState_</span></span>
  
> <span data-ttu-id="c355f-111">[in]メッセージをロックまたはロック解除するかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="c355f-111">[in] A value that indicates whether the message should be locked or unlocked.</span></span> <span data-ttu-id="c355f-112">次のいずれかの値が有効です。</span><span class="sxs-lookup"><span data-stu-id="c355f-112">One of the following values is valid:</span></span>
    
<span data-ttu-id="c355f-113">MSG_LOCKED</span><span class="sxs-lookup"><span data-stu-id="c355f-113">MSG_LOCKED</span></span> 
  
> <span data-ttu-id="c355f-114">メッセージはロックされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="c355f-114">The message should be locked.</span></span> 
    
<span data-ttu-id="c355f-115">MSG_UNLOCKED</span><span class="sxs-lookup"><span data-stu-id="c355f-115">MSG_UNLOCKED</span></span> 
  
> <span data-ttu-id="c355f-116">メッセージのロックを解除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c355f-116">The message should be unlocked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c355f-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="c355f-117">Return value</span></span>

<span data-ttu-id="c355f-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="c355f-118">S_OK</span></span> 
  
> <span data-ttu-id="c355f-119">メッセージのロック状態が正常に設定されました。</span><span class="sxs-lookup"><span data-stu-id="c355f-119">The lock state of the message was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c355f-120">注釈</span><span class="sxs-lookup"><span data-stu-id="c355f-120">Remarks</span></span>

<span data-ttu-id="c355f-121">**IMsgStore::SetLockState** メソッドは、メッセージをロックまたはロック解除します。</span><span class="sxs-lookup"><span data-stu-id="c355f-121">The **IMsgStore::SetLockState** method locks or unlocks a message.</span></span> <span data-ttu-id="c355f-122">**SetLockState** は、メッセージの送信中に MAPI スプーラーによってのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="c355f-122">**SetLockState** can be called only by the MAPI spooler while it is sending the message.</span></span> 
  
<span data-ttu-id="c355f-123">通常、MAPI スプーラーが **SetLockState** を呼び出してメッセージをロックすると、最も古いメッセージ (つまり、MAPI スプーラーが送信するためにキューに入っている次のメッセージ) だけがロックされます。</span><span class="sxs-lookup"><span data-stu-id="c355f-123">Usually, when the MAPI spooler calls **SetLockState** to lock a message, it locks only the oldest message (that is, the next message queued for the MAPI spooler to send).</span></span> <span data-ttu-id="c355f-124">キュー内の最も古いメッセージが一時的に使用できないトランスポート プロバイダーを待機し、キュー内の次のメッセージが別のトランスポート プロバイダーを使用している場合、MAPI スプーラーは後のメッセージの処理を開始できます。</span><span class="sxs-lookup"><span data-stu-id="c355f-124">If the oldest message in the queue is waiting for a temporarily unavailable transport provider, and the next message in the queue uses a different transport provider, the MAPI spooler can begin processing the later message.</span></span> <span data-ttu-id="c355f-125">SetLockState を使用して、そのメッセージをロックして処理 **を開始します**。</span><span class="sxs-lookup"><span data-stu-id="c355f-125">It begins processing by locking that message by using **SetLockState**.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c355f-126">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="c355f-126">Notes to implementers</span></span>

<span data-ttu-id="c355f-127">mapi スプーラーが **setLockState** パラメーターを MSG_LOCKED に設定して  _SetLockState_ を呼び出した後、メッセージの送信を取り消す [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) メソッドを呼び出して失敗する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c355f-127">After the MAPI spooler has called **SetLockState** with the  _ulLockState_ parameter set to MSG_LOCKED, calls to the [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) method to cancel the message's transmission must fail.</span></span> 
  
<span data-ttu-id="c355f-128">SetLockState の実装でメッセージの [IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出して **、SetLockState** 呼び出しが受信される前にメッセージに加えた変更が保存されます。</span><span class="sxs-lookup"><span data-stu-id="c355f-128">Call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method in your **SetLockState** implementation so that any changes that were made to the message before the **SetLockState** call was received are saved.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c355f-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="c355f-129">See also</span></span>



[<span data-ttu-id="c355f-130">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="c355f-130">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)
  
[<span data-ttu-id="c355f-131">IMsgStore::FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="c355f-131">IMsgStore::FinishedMsg</span></span>](imsgstore-finishedmsg.md)
  
[<span data-ttu-id="c355f-132">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c355f-132">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

