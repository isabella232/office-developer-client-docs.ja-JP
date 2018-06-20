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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a4e924489f2ec656f473f28407d528e9c2ddda5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801005"
---
# <a name="imsgstoresetlockstate"></a><span data-ttu-id="2017e-103">IMsgStore::SetLockState</span><span class="sxs-lookup"><span data-stu-id="2017e-103">IMsgStore::SetLockState</span></span>

  
  
<span data-ttu-id="2017e-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2017e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2017e-105">ロックまたはメッセージのロックを解除します。</span><span class="sxs-lookup"><span data-stu-id="2017e-105">Locks or unlocks a message.</span></span> <span data-ttu-id="2017e-106">このメソッドは、MAPI スプーラーによってのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2017e-106">This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT SetLockState(
  LPMESSAGE lpMessage,
  ULONG ulLockState  
);
```

## <a name="parameters"></a><span data-ttu-id="2017e-107">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="2017e-107">Parameters</span></span>

 <span data-ttu-id="2017e-108">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="2017e-108">_lpMessage_</span></span>
  
> <span data-ttu-id="2017e-109">[in]ロックまたはロック解除のメッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="2017e-109">[in] A pointer to the message to lock or unlock.</span></span>
    
 <span data-ttu-id="2017e-110">_ulLockState_</span><span class="sxs-lookup"><span data-stu-id="2017e-110">_ulLockState_</span></span>
  
> <span data-ttu-id="2017e-111">[in]メッセージをロックまたはロック解除するかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="2017e-111">[in] A value that indicates whether the message should be locked or unlocked.</span></span> <span data-ttu-id="2017e-112">次のいずれかの機能は有効です。</span><span class="sxs-lookup"><span data-stu-id="2017e-112">One of the following values is valid:</span></span>
    
<span data-ttu-id="2017e-113">MSG_LOCKED</span><span class="sxs-lookup"><span data-stu-id="2017e-113">MSG_LOCKED</span></span> 
  
> <span data-ttu-id="2017e-114">メッセージをロックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2017e-114">The message should be locked.</span></span> 
    
<span data-ttu-id="2017e-115">MSG_UNLOCKED</span><span class="sxs-lookup"><span data-stu-id="2017e-115">MSG_UNLOCKED</span></span> 
  
> <span data-ttu-id="2017e-116">メッセージをロック解除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2017e-116">The message should be unlocked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2017e-117">�߂�l</span><span class="sxs-lookup"><span data-stu-id="2017e-117">Return value</span></span>

<span data-ttu-id="2017e-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="2017e-118">S_OK</span></span> 
  
> <span data-ttu-id="2017e-119">メッセージのロック状態は正常に設定されました。</span><span class="sxs-lookup"><span data-stu-id="2017e-119">The lock state of the message was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2017e-120">備考</span><span class="sxs-lookup"><span data-stu-id="2017e-120">Remarks</span></span>

<span data-ttu-id="2017e-121">**IMsgStore::SetLockState**メソッドは、ロックまたは、メッセージのロックを解除します。</span><span class="sxs-lookup"><span data-stu-id="2017e-121">The **IMsgStore::SetLockState** method locks or unlocks a message.</span></span> <span data-ttu-id="2017e-122">**SetLockState**はメッセージを送信するときに、MAPI スプーラーによってのみ呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="2017e-122">**SetLockState** can be called only by the MAPI spooler while it is sending the message.</span></span> 
  
<span data-ttu-id="2017e-123">通常、MAPI スプーラーを呼び出すと、メッセージをロックするのには**SetLockState** 、ロックのみの最も古いメッセージ (つまり、次のメッセージ キューに入れられた MAPI スプーラーに送信するため)。</span><span class="sxs-lookup"><span data-stu-id="2017e-123">Usually, when the MAPI spooler calls **SetLockState** to lock a message, it locks only the oldest message (that is, the next message queued for the MAPI spooler to send).</span></span> <span data-ttu-id="2017e-124">キュー内の最も古いメッセージが一時的に使用不可のトランスポート プロバイダーでは、待機している次のメッセージ キューを別のトランスポート プロバイダーを使用する場合は、MAPI スプーラーは後でメッセージの処理を開始できます。</span><span class="sxs-lookup"><span data-stu-id="2017e-124">If the oldest message in the queue is waiting for a temporarily unavailable transport provider, and the next message in the queue uses a different transport provider, the MAPI spooler can begin processing the later message.</span></span> <span data-ttu-id="2017e-125">**SetLockState**を使用して、そのメッセージをロックすることにより、処理を開始します。</span><span class="sxs-lookup"><span data-stu-id="2017e-125">It begins processing by locking that message by using **SetLockState**.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="2017e-126">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="2017e-126">Notes to implementers</span></span>

<span data-ttu-id="2017e-127">MAPI スプーラーは、 _ulLockState_パラメーターを MSG_LOCKED を設定して**SetLockState**を呼び出すと、メッセージの転送をキャンセルするのには、 [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)メソッドへの呼び出しは失敗する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2017e-127">After the MAPI spooler has called **SetLockState** with the  _ulLockState_ parameter set to MSG_LOCKED, calls to the [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) method to cancel the message's transmission must fail.</span></span> 
  
<span data-ttu-id="2017e-128">**SetLockState**の呼び出しを受け取る前に、メッセージに加えられた変更が保存されるように、 **SetLockState**の実装では、メッセージの[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2017e-128">Call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method in your **SetLockState** implementation so that any changes that were made to the message before the **SetLockState** call was received are saved.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2017e-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="2017e-129">See also</span></span>



[<span data-ttu-id="2017e-130">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="2017e-130">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)
  
[<span data-ttu-id="2017e-131">IMsgStore::FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="2017e-131">IMsgStore::FinishedMsg</span></span>](imsgstore-finishedmsg.md)
  
[<span data-ttu-id="2017e-132">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="2017e-132">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

