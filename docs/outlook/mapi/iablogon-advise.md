---
title: IABLogonAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.Advise
api_type:
- COM
ms.assetid: 375d65b1-607d-4e2a-8052-9bcbf08fc2ac
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 4ab0e4b023e6af19f650abf421aed122dcc21879
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428229"
---
# <a name="iablogonadvise"></a><span data-ttu-id="e6766-103">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="e6766-103">IABLogon::Advise</span></span>

  
  
<span data-ttu-id="e6766-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e6766-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e6766-105">コンテナー、メッセージング ユーザー、または配布リストに影響を与える指定されたイベントの通知を受け取る呼び出し元を登録します。</span><span class="sxs-lookup"><span data-stu-id="e6766-105">Registers the caller to receive notification of specified events that affect a container, messaging user, or distribution list.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="e6766-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e6766-106">Parameters</span></span>

 <span data-ttu-id="e6766-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="e6766-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="e6766-108">[in]  _lpEntryID_ パラメーターが指すエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="e6766-108">[in] The count of bytes in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="e6766-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="e6766-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="e6766-110">[in]どの通知を生成する必要があるオブジェクトのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e6766-110">[in] A pointer to the entry identifier of the object about which notifications should be generated.</span></span>
    
 <span data-ttu-id="e6766-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="e6766-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="e6766-112">[in]呼び出し元が関心を持ち、登録に含める必要がある通知イベントの種類を示す値のビットマスク。</span><span class="sxs-lookup"><span data-stu-id="e6766-112">[in] A bitmask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="e6766-113">イベントに関する [情報を](notification.md) 保持する各種類のイベントに関連付けられた対応する NOTIFICATION 構造があります。</span><span class="sxs-lookup"><span data-stu-id="e6766-113">There is a corresponding [NOTIFICATION](notification.md) structure associated with each type of event that holds information about the event.</span></span> <span data-ttu-id="e6766-114">次の表に  _、ulEventMask_ パラメーターの有効な値と、各値に関連付けられている構造体を示します。</span><span class="sxs-lookup"><span data-stu-id="e6766-114">The following table lists the valid values for the  _ulEventMask_ parameter and the structures associated with each value.</span></span> 
    
|<span data-ttu-id="e6766-115">**通知イベントの種類**</span><span class="sxs-lookup"><span data-stu-id="e6766-115">**Notification event type**</span></span>|<span data-ttu-id="e6766-116">**対応 **する NOTIFICATION** 構造**</span><span class="sxs-lookup"><span data-stu-id="e6766-116">**Corresponding **NOTIFICATION** structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e6766-117">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="e6766-117">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="e6766-118">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e6766-118">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="e6766-119">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="e6766-119">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="e6766-120">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e6766-120">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="e6766-121">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="e6766-121">**fnevObjectDeleted**</span></span> <br/> |<span data-ttu-id="e6766-122">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="e6766-122">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="e6766-123">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="e6766-123">**fnevObjectModified**</span></span> <br/> |<span data-ttu-id="e6766-124">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="e6766-124">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="e6766-125">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="e6766-125">**fnevObjectCopied**</span></span> <br/> |<span data-ttu-id="e6766-126">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="e6766-126">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="e6766-127">**fnevObjectMoved**</span><span class="sxs-lookup"><span data-stu-id="e6766-127">**fnevObjectMoved**</span></span> <br/> |<span data-ttu-id="e6766-128">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="e6766-128">**OBJECT_NOTIFICATION**</span></span> <br/> |
   
 <span data-ttu-id="e6766-129">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="e6766-129">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="e6766-130">[in]後続の通知を受信するアアドバイス シンク オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e6766-130">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span>
    
 <span data-ttu-id="e6766-131">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="e6766-131">_lpulConnection_</span></span>
  
> <span data-ttu-id="e6766-132">[out]通知登録を表す 0 以外の値へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e6766-132">[out] A pointer to a nonzero value that represents the notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e6766-133">戻り値</span><span class="sxs-lookup"><span data-stu-id="e6766-133">Return value</span></span>

<span data-ttu-id="e6766-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="e6766-134">S_OK</span></span> 
  
> <span data-ttu-id="e6766-135">通知の登録が成功しました。</span><span class="sxs-lookup"><span data-stu-id="e6766-135">The notification registration was successful.</span></span>
    
<span data-ttu-id="e6766-136">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="e6766-136">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="e6766-137">_lpEntryID_ パラメーターで渡されるエントリ識別子は、適切な形式ではありません。</span><span class="sxs-lookup"><span data-stu-id="e6766-137">The entry identifier passed in the  _lpEntryID_ parameter is not in the appropriate format.</span></span> 
    
<span data-ttu-id="e6766-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="e6766-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="e6766-139">アドレス帳プロバイダーは、オブジェクトに対して変更を加えないので、通知をサポートしていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e6766-139">The address book provider does not support notification, possibly because it does not allow changes to be made to its objects.</span></span>
    
<span data-ttu-id="e6766-140">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="e6766-140">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="e6766-141">アドレス帳プロバイダーは  _、lpEntryID_ で渡されたエントリ識別子を処理できません。</span><span class="sxs-lookup"><span data-stu-id="e6766-141">The address book provider cannot handle the entry identifier passed in  _lpEntryID_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e6766-142">注釈</span><span class="sxs-lookup"><span data-stu-id="e6766-142">Remarks</span></span>

<span data-ttu-id="e6766-143">アドレス帳プロバイダーは **、IABLogon::Advise** メソッドを実装して、コンテナー内のオブジェクトに変更が発生したときに通知を受け取る呼び出し元を登録します。</span><span class="sxs-lookup"><span data-stu-id="e6766-143">Address book providers implement the **IABLogon::Advise** method to register the caller to be notified when a change occurs to an object in one of their containers.</span></span> <span data-ttu-id="e6766-144">発信者は、メッセージング ユーザー、配布リスト、またはコンテナー全体に関する通知に登録できます。</span><span class="sxs-lookup"><span data-stu-id="e6766-144">Callers can register for notifications regarding messaging users, distribution lists, or entire containers.</span></span> 
  
<span data-ttu-id="e6766-145">クライアントは通常、アドレス帳通知に登録するために [IAddrBook::Advise](iaddrbook-advise.md) メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e6766-145">Clients typically call the [IAddrBook::Advise](iaddrbook-advise.md) method to register for address book notifications.</span></span> <span data-ttu-id="e6766-146">MAPI は **、lpEntryID** のエントリ識別子で表されるオブジェクトを担当するアドレス帳プロバイダーの  _Advise メソッドを呼び出します_。</span><span class="sxs-lookup"><span data-stu-id="e6766-146">MAPI then calls the **Advise** method of the address book provider that is responsible for the object represented by the entry identifier in  _lpEntryID_.</span></span>
  
<span data-ttu-id="e6766-147">_ulEventMask_ で表される型の指定されたオブジェクトに変更が発生すると _、lpAdviseSink_ が指すアアドバイス シンクの **OnNotify** メソッドに対して呼び出しが行われます。</span><span class="sxs-lookup"><span data-stu-id="e6766-147">When a change occurs to the indicated object of the type represented in  _ulEventMask_, a call is made to the **OnNotify** method of the advise sink pointed to by  _lpAdviseSink_.</span></span> <span data-ttu-id="e6766-148">**NOTIFICATION** 構造体で **OnNotify** ルーチンに渡されるデータは、イベントを記述します。</span><span class="sxs-lookup"><span data-stu-id="e6766-148">Data passed in the **NOTIFICATION** structure to the **OnNotify** routine describes the event.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="e6766-149">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="e6766-149">Notes to implementers</span></span>

<span data-ttu-id="e6766-150">MAPI からの通知のサポートとサポートなし。</span><span class="sxs-lookup"><span data-stu-id="e6766-150">You can support notification with or without help from MAPI.</span></span> <span data-ttu-id="e6766-151">MAPI には、サービス プロバイダーが通知を実装するのに役立つ 3 つのサポート オブジェクト メソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="e6766-151">MAPI has three support object methods to help service providers implement notification:</span></span>
  
- [<span data-ttu-id="e6766-152">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="e6766-152">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)
    
- [<span data-ttu-id="e6766-153">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="e6766-153">IMAPISupport::Unsubscribe</span></span>](imapisupport-unsubscribe.md)
    
- [<span data-ttu-id="e6766-154">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="e6766-154">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
    
<span data-ttu-id="e6766-155">MAPI サポート メソッドを使用する場合は **、Advise** メソッドが呼び出されたときに Subscribe を呼び出し _、lpAdviseSink ポインターを解放_ します。 </span><span class="sxs-lookup"><span data-stu-id="e6766-155">If you elect to use the MAPI support methods, call **Subscribe** when your **Advise** method is called and release the  _lpAdviseSink_ pointer.</span></span> 
  
<span data-ttu-id="e6766-156">通知を自分でサポートする場合は _、lpAdviseSink_ パラメーターで表されるアアドバイス シンクの **AddRef** メソッドを呼び出して、このポインターのコピーを保持します。</span><span class="sxs-lookup"><span data-stu-id="e6766-156">If you elect to support notification yourself, call the **AddRef** method of the advise sink represented by the  _lpAdviseSink_ parameter to keep a copy of this pointer.</span></span> <span data-ttu-id="e6766-157">登録を取り消す [IABLogon::Unadvise](iablogon-unadvise.md) メソッドが呼び出されるまで、このコピーを維持します。</span><span class="sxs-lookup"><span data-stu-id="e6766-157">Maintain this copy until your [IABLogon::Unadvise](iablogon-unadvise.md) method is called to cancel the registration.</span></span> 
  
<span data-ttu-id="e6766-158">通知のサポート方法に関係なく、0 以外の接続番号を通知登録に割り当て  _、lpulConnection パラメーターで返_ します。</span><span class="sxs-lookup"><span data-stu-id="e6766-158">Regardless of how you support notification, assign a nonzero connection number to the notification registration and return it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="e6766-159">**Unadvise** メソッドが呼び出されるまで、この接続番号を解放しない。</span><span class="sxs-lookup"><span data-stu-id="e6766-159">Do not release this connection number until the **Unadvise** method has been called.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e6766-160">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="e6766-160">Notes to callers</span></span>

<span data-ttu-id="e6766-161">_lpAdviseSink_ パラメーターで **Advise** に渡すアアドバイス シンク ポインターは、作成したオブジェクト、または [HRThisThreadAdviseSink](hrthisthreadadvisesink.md)関数を使用して MAPI が作成したオブジェクトを指します。</span><span class="sxs-lookup"><span data-stu-id="e6766-161">The advise sink pointer that you pass in the  _lpAdviseSink_ parameter to **Advise** can point to an object that you have created or that MAPI has created through the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> <span data-ttu-id="e6766-162">複数の実行スレッドをサポートし **、OnNotify** メソッドに対する後続の呼び出しが適切なスレッドで適切な時間に実行されるのを確認する場合は **、HrThisThreadAdviseSink** を使用できます。</span><span class="sxs-lookup"><span data-stu-id="e6766-162">You might want to use **HrThisThreadAdviseSink** if you support multiple threads of execution and want to be sure that that subsequent calls to your **OnNotify** method occur at an appropriate time on an appropriate thread.</span></span> 
  
<span data-ttu-id="e6766-163">Advise への呼び出し後、Unadvise への呼び出しの前に、いつでもアアドバイス シンク オブジェクトが解放される準備を **してください**。</span><span class="sxs-lookup"><span data-stu-id="e6766-163">Be prepared for your advise sink object to be released any time after your call to **Advise** and before your call to **Unadvise**.</span></span> <span data-ttu-id="e6766-164">そのため、特定の長期的な使用がない限り **、Advise** が返された後にアアドバイス シンク オブジェクトを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e6766-164">Therefore, you should release your advise sink object after **Advise** returns, unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="e6766-165">通知プロセスの詳細については、「MAPI での [イベント通知」を参照してください](event-notification-in-mapi.md)。</span><span class="sxs-lookup"><span data-stu-id="e6766-165">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="e6766-166">**IMAPISupport** メソッドを使用して通知をサポートする方法については、「Support Event Notification 」[を参照してください](supporting-event-notification.md)。</span><span class="sxs-lookup"><span data-stu-id="e6766-166">For information about how to use the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span> <span data-ttu-id="e6766-167">マルチスレッドと MAPI の詳細については、「MAPI でのスレッド [」を参照してください](threading-in-mapi.md)。</span><span class="sxs-lookup"><span data-stu-id="e6766-167">For more information about multithreading and MAPI, see [Threading in MAPI](threading-in-mapi.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e6766-168">関連項目</span><span class="sxs-lookup"><span data-stu-id="e6766-168">See also</span></span>



[<span data-ttu-id="e6766-169">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="e6766-169">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="e6766-170">IABLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="e6766-170">IABLogon::Unadvise</span></span>](iablogon-unadvise.md)
  
[<span data-ttu-id="e6766-171">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="e6766-171">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="e6766-172">�ʒm</span><span class="sxs-lookup"><span data-stu-id="e6766-172">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="e6766-173">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e6766-173">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

