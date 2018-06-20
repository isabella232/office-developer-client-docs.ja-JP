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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 926fef0e1b2f905d510102e69afb667414e6cce3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800355"
---
# <a name="iablogonadvise"></a><span data-ttu-id="7a978-103">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="7a978-103">IABLogon::Advise</span></span>

  
  
<span data-ttu-id="7a978-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7a978-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7a978-105">コンテナー、ユーザー、または配布リストをメッセージに影響を与える特定のイベントの通知を受け取る呼び出し元を登録します。</span><span class="sxs-lookup"><span data-stu-id="7a978-105">Registers the caller to receive notification of specified events that affect a container, messaging user, or distribution list.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="7a978-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="7a978-106">Parameters</span></span>

 <span data-ttu-id="7a978-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="7a978-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="7a978-108">[in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数のカウントです。</span><span class="sxs-lookup"><span data-stu-id="7a978-108">[in] The count of bytes in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="7a978-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="7a978-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="7a978-110">[in]通知を生成する対象のオブジェクトのエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7a978-110">[in] A pointer to the entry identifier of the object about which notifications should be generated.</span></span>
    
 <span data-ttu-id="7a978-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="7a978-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="7a978-112">[in]呼び出し元に興味を持って登録に含めることが通知イベントの種類を示す値のビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="7a978-112">[in] A bitmask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="7a978-113">各イベントに関する情報を保持するイベントの種類に関連付けられている対応する[通知](notification.md)の構造があります。</span><span class="sxs-lookup"><span data-stu-id="7a978-113">There is a corresponding [NOTIFICATION](notification.md) structure associated with each type of event that holds information about the event.</span></span> <span data-ttu-id="7a978-114">次の表は、 _ulEventMask_パラメーターとそれぞれの値に関連付けられている構造体の有効値を一覧します。</span><span class="sxs-lookup"><span data-stu-id="7a978-114">The following table lists the valid values for the  _ulEventMask_ parameter and the structures associated with each value.</span></span> 
    
|<span data-ttu-id="7a978-115">**通知イベントの種類**</span><span class="sxs-lookup"><span data-stu-id="7a978-115">**Notification event type**</span></span>|<span data-ttu-id="7a978-116">**対応する**通知**の構造体**</span><span class="sxs-lookup"><span data-stu-id="7a978-116">**Corresponding **NOTIFICATION** structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7a978-117">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="7a978-117">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="7a978-118">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="7a978-118">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="7a978-119">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="7a978-119">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="7a978-120">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="7a978-120">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="7a978-121">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="7a978-121">**fnevObjectDeleted**</span></span> <br/> |<span data-ttu-id="7a978-122">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="7a978-122">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="7a978-123">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="7a978-123">**fnevObjectModified**</span></span> <br/> |<span data-ttu-id="7a978-124">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="7a978-124">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="7a978-125">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="7a978-125">**fnevObjectCopied**</span></span> <br/> |<span data-ttu-id="7a978-126">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="7a978-126">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="7a978-127">**fnevObjectMoved**</span><span class="sxs-lookup"><span data-stu-id="7a978-127">**fnevObjectMoved**</span></span> <br/> |<span data-ttu-id="7a978-128">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="7a978-128">**OBJECT_NOTIFICATION**</span></span> <br/> |
   
 <span data-ttu-id="7a978-129">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="7a978-129">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="7a978-130">[in]後続の通知を受信するアドバイズ シンク オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="7a978-130">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span>
    
 <span data-ttu-id="7a978-131">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="7a978-131">_lpulConnection_</span></span>
  
> <span data-ttu-id="7a978-132">[out]通知の登録を表す、0 以外の値へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7a978-132">[out] A pointer to a nonzero value that represents the notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7a978-133">�߂�l</span><span class="sxs-lookup"><span data-stu-id="7a978-133">Return value</span></span>

<span data-ttu-id="7a978-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="7a978-134">S_OK</span></span> 
  
> <span data-ttu-id="7a978-135">通知の登録に成功しました。</span><span class="sxs-lookup"><span data-stu-id="7a978-135">The notification registration was successful.</span></span>
    
<span data-ttu-id="7a978-136">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="7a978-136">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="7a978-137">_LpEntryID_パラメーターで渡されたエントリ id は適切な形式ではありません。</span><span class="sxs-lookup"><span data-stu-id="7a978-137">The entry identifier passed in the  _lpEntryID_ parameter is not in the appropriate format.</span></span> 
    
<span data-ttu-id="7a978-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="7a978-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="7a978-139">アドレス帳プロバイダー サポートしていません通知、場合によってそのオブジェクトへの変更ができないため。</span><span class="sxs-lookup"><span data-stu-id="7a978-139">The address book provider does not support notification, possibly because it does not allow changes to be made to its objects.</span></span>
    
<span data-ttu-id="7a978-140">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="7a978-140">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="7a978-141">アドレス帳プロバイダーは、 _lpEntryID_に渡されたエントリ id を処理できません。</span><span class="sxs-lookup"><span data-stu-id="7a978-141">The address book provider cannot handle the entry identifier passed in  _lpEntryID_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7a978-142">備考</span><span class="sxs-lookup"><span data-stu-id="7a978-142">Remarks</span></span>

<span data-ttu-id="7a978-143">アドレス帳プロバイダーは、そのコンテナーのいずれかのオブジェクトに変更が発生したときに通知する呼び出し元を登録するのには**IABLogon::Advise**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="7a978-143">Address book providers implement the **IABLogon::Advise** method to register the caller to be notified when a change occurs to an object in one of their containers.</span></span> <span data-ttu-id="7a978-144">呼び出し元は、メッセージングのユーザー、配布リスト、または全体のコンテナーに関する通知を登録できます。</span><span class="sxs-lookup"><span data-stu-id="7a978-144">Callers can register for notifications regarding messaging users, distribution lists, or entire containers.</span></span> 
  
<span data-ttu-id="7a978-145">クライアントは、通常、アドレス帳の通知を登録する[IAddrBook::Advise](iaddrbook-advise.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7a978-145">Clients typically call the [IAddrBook::Advise](iaddrbook-advise.md) method to register for address book notifications.</span></span> <span data-ttu-id="7a978-146">MAPI は、 ** _lpEntryID_内のエントリの識別子によって表されるオブジェクトは、アドレス帳プロバイダーのメソッド**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7a978-146">MAPI then calls the **Advise** method of the address book provider that is responsible for the object represented by the entry identifier in  _lpEntryID_.</span></span>
  
<span data-ttu-id="7a978-147">_UlEventMask_で表される型の指定したオブジェクトに変更が発生すると_lpAdviseSink_が指すアドバイズ シンクの**OnNotify**メソッドの呼び出しが行われます。</span><span class="sxs-lookup"><span data-stu-id="7a978-147">When a change occurs to the indicated object of the type represented in  _ulEventMask_, a call is made to the **OnNotify** method of the advise sink pointed to by  _lpAdviseSink_.</span></span> <span data-ttu-id="7a978-148">**OnNotify**ルーチンに渡された**通知**の構造体のデータでは、イベントについて説明します。</span><span class="sxs-lookup"><span data-stu-id="7a978-148">Data passed in the **NOTIFICATION** structure to the **OnNotify** routine describes the event.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7a978-149">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="7a978-149">Notes to implementers</span></span>

<span data-ttu-id="7a978-150">MAPI の支援の有無にかかわらず、通知をサポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="7a978-150">You can support notification with or without help from MAPI.</span></span> <span data-ttu-id="7a978-151">MAPI は、サービス プロバイダーの通知を実装するための 3 つのサポート オブジェクトのメソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="7a978-151">MAPI has three support object methods to help service providers implement notification:</span></span>
  
- [<span data-ttu-id="7a978-152">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="7a978-152">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)
    
- [<span data-ttu-id="7a978-153">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="7a978-153">IMAPISupport::Unsubscribe</span></span>](imapisupport-unsubscribe.md)
    
- [<span data-ttu-id="7a978-154">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="7a978-154">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
    
<span data-ttu-id="7a978-155">MAPI サポートされている方法を使用する場合、 **Subscribe**を呼び出して **、メソッド**が呼び出されたときと、 _lpAdviseSink_ポインターを解放します。</span><span class="sxs-lookup"><span data-stu-id="7a978-155">If you elect to use the MAPI support methods, call **Subscribe** when your **Advise** method is called and release the  _lpAdviseSink_ pointer.</span></span> 
  
<span data-ttu-id="7a978-156">自分で通知をサポートするように選択する場合は、このポインターのコピーを保持するのには、 _lpAdviseSink_パラメーターで表されるアドバイズ シンクの**AddRef**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7a978-156">If you elect to support notification yourself, call the **AddRef** method of the advise sink represented by the  _lpAdviseSink_ parameter to keep a copy of this pointer.</span></span> <span data-ttu-id="7a978-157">登録をキャンセルするのには、 [IABLogon::Unadvise](iablogon-unadvise.md)メソッドが呼び出されるまでは、このコピーを維持します。</span><span class="sxs-lookup"><span data-stu-id="7a978-157">Maintain this copy until your [IABLogon::Unadvise](iablogon-unadvise.md) method is called to cancel the registration.</span></span> 
  
<span data-ttu-id="7a978-158">通知をサポートする方法に関係なく、通知の登録には 0 以外の接続番号を割り当てるし、 _lpulConnection_パラメーターに返すことです。</span><span class="sxs-lookup"><span data-stu-id="7a978-158">Regardless of how you support notification, assign a nonzero connection number to the notification registration and return it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="7a978-159">**Unadvise**メソッドが呼び出されるまでは、この接続の数を解放しません。</span><span class="sxs-lookup"><span data-stu-id="7a978-159">Do not release this connection number until the **Unadvise** method has been called.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7a978-160">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="7a978-160">Notes to callers</span></span>

<span data-ttu-id="7a978-161">アドバイズ シンク ポインター**アドバイズ**する_lpAdviseSink_パラメーターを渡すことは、作成した、または[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)関数を作成した MAPI オブジェクトを指すことができます。</span><span class="sxs-lookup"><span data-stu-id="7a978-161">The advise sink pointer that you pass in the  _lpAdviseSink_ parameter to **Advise** can point to an object that you have created or that MAPI has created through the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> <span data-ttu-id="7a978-162">複数の実行スレッドをサポートし、 **OnNotify**メソッドへの後続の呼び出しは、適切なスレッドに適切なタイミングで発生する可能性があることを確認する場合は、 **HrThisThreadAdviseSink**を使用する場合があります。</span><span class="sxs-lookup"><span data-stu-id="7a978-162">You might want to use **HrThisThreadAdviseSink** if you support multiple threads of execution and want to be sure that that subsequent calls to your **OnNotify** method occur at an appropriate time on an appropriate thread.</span></span> 
  
<span data-ttu-id="7a978-163">**アドバイス**をし**に**、呼び出しの前に電話した後にリリースするアドバイズ シンク オブジェクトを準備します。</span><span class="sxs-lookup"><span data-stu-id="7a978-163">Be prepared for your advise sink object to be released any time after your call to **Advise** and before your call to **Unadvise**.</span></span> <span data-ttu-id="7a978-164">したがって、する必要がありますをリリースするアドバイズ シンク オブジェクト**アドバイズ**が返されると、その特定の長期的な使用がない限り。</span><span class="sxs-lookup"><span data-stu-id="7a978-164">Therefore, you should release your advise sink object after **Advise** returns, unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="7a978-165">通知プロセスの詳細については、 [MAPI でのイベントの通知](event-notification-in-mapi.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7a978-165">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="7a978-166">通知をサポートするために**IMAPISupport**メソッドを使用する方法の詳細については、[イベント通知のサポート](supporting-event-notification.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7a978-166">For information about how to use the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span> <span data-ttu-id="7a978-167">詳細についてはマルチ スレッドおよび MAPI、 [MAPI でのスレッド処理](threading-in-mapi.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7a978-167">For more information about multithreading and MAPI, see [Threading in MAPI](threading-in-mapi.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7a978-168">関連項目</span><span class="sxs-lookup"><span data-stu-id="7a978-168">See also</span></span>



[<span data-ttu-id="7a978-169">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="7a978-169">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="7a978-170">IABLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="7a978-170">IABLogon::Unadvise</span></span>](iablogon-unadvise.md)
  
[<span data-ttu-id="7a978-171">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="7a978-171">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="7a978-172">�ʒm</span><span class="sxs-lookup"><span data-stu-id="7a978-172">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="7a978-173">IABLogon: IUnknown</span><span class="sxs-lookup"><span data-stu-id="7a978-173">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

