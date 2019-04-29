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
# <a name="iablogonadvise"></a><span data-ttu-id="f20df-103">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="f20df-103">IABLogon::Advise</span></span>

  
  
<span data-ttu-id="f20df-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f20df-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f20df-105">発信者が、コンテナー、メッセージングユーザー、または配布リストに影響を与える指定されたイベントの通知を受信するように登録します。</span><span class="sxs-lookup"><span data-stu-id="f20df-105">Registers the caller to receive notification of specified events that affect a container, messaging user, or distribution list.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="f20df-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f20df-106">Parameters</span></span>

 <span data-ttu-id="f20df-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="f20df-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="f20df-108">順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="f20df-108">[in] The count of bytes in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="f20df-109">_lて tryid_</span><span class="sxs-lookup"><span data-stu-id="f20df-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="f20df-110">順番通知を生成するオブジェクトのエントリ id へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f20df-110">[in] A pointer to the entry identifier of the object about which notifications should be generated.</span></span>
    
 <span data-ttu-id="f20df-111">_uleventmask_</span><span class="sxs-lookup"><span data-stu-id="f20df-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="f20df-112">順番呼び出し元が関心を持ち、登録に含める必要がある通知イベントの種類を示す値のビットマスク。</span><span class="sxs-lookup"><span data-stu-id="f20df-112">[in] A bitmask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="f20df-113">イベントに関する情報を保持する各イベントの種類に関連付けられた、対応する[通知](notification.md)構造があります。</span><span class="sxs-lookup"><span data-stu-id="f20df-113">There is a corresponding [NOTIFICATION](notification.md) structure associated with each type of event that holds information about the event.</span></span> <span data-ttu-id="f20df-114">次の表に、 _uleventmask_パラメーターの有効な値と、各値に関連付けられている構造を示します。</span><span class="sxs-lookup"><span data-stu-id="f20df-114">The following table lists the valid values for the  _ulEventMask_ parameter and the structures associated with each value.</span></span> 
    
|<span data-ttu-id="f20df-115">**通知イベントの種類**</span><span class="sxs-lookup"><span data-stu-id="f20df-115">**Notification event type**</span></span>|<span data-ttu-id="f20df-116">**対応する**通知**構造**</span><span class="sxs-lookup"><span data-stu-id="f20df-116">**Corresponding **NOTIFICATION** structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f20df-117">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="f20df-117">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="f20df-118">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="f20df-118">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="f20df-119">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="f20df-119">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="f20df-120">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="f20df-120">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="f20df-121">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="f20df-121">**fnevObjectDeleted**</span></span> <br/> |<span data-ttu-id="f20df-122">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="f20df-122">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="f20df-123">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="f20df-123">**fnevObjectModified**</span></span> <br/> |<span data-ttu-id="f20df-124">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="f20df-124">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="f20df-125">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="f20df-125">**fnevObjectCopied**</span></span> <br/> |<span data-ttu-id="f20df-126">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="f20df-126">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="f20df-127">**fnevObjectMoved**</span><span class="sxs-lookup"><span data-stu-id="f20df-127">**fnevObjectMoved**</span></span> <br/> |<span data-ttu-id="f20df-128">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="f20df-128">**OBJECT_NOTIFICATION**</span></span> <br/> |
   
 <span data-ttu-id="f20df-129">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="f20df-129">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="f20df-130">順番後続の通知を受け取るアドバイズシンクオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="f20df-130">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span>
    
 <span data-ttu-id="f20df-131">_lアウト接続_</span><span class="sxs-lookup"><span data-stu-id="f20df-131">_lpulConnection_</span></span>
  
> <span data-ttu-id="f20df-132">読み上げ通知登録を表す0以外の値へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f20df-132">[out] A pointer to a nonzero value that represents the notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f20df-133">戻り値</span><span class="sxs-lookup"><span data-stu-id="f20df-133">Return value</span></span>

<span data-ttu-id="f20df-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="f20df-134">S_OK</span></span> 
  
> <span data-ttu-id="f20df-135">通知の登録に成功しました。</span><span class="sxs-lookup"><span data-stu-id="f20df-135">The notification registration was successful.</span></span>
    
<span data-ttu-id="f20df-136">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="f20df-136">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="f20df-137">_lて tryid_パラメーターに渡されたエントリ識別子が適切な形式ではありません。</span><span class="sxs-lookup"><span data-stu-id="f20df-137">The entry identifier passed in the  _lpEntryID_ parameter is not in the appropriate format.</span></span> 
    
<span data-ttu-id="f20df-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="f20df-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="f20df-139">アドレス帳プロバイダーは、通知をサポートしていません。オブジェクトへの変更が許可されていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f20df-139">The address book provider does not support notification, possibly because it does not allow changes to be made to its objects.</span></span>
    
<span data-ttu-id="f20df-140">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="f20df-140">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="f20df-141">アドレス帳プロバイダーは、 _lな tryid_で渡されたエントリ識別子を処理できません。</span><span class="sxs-lookup"><span data-stu-id="f20df-141">The address book provider cannot handle the entry identifier passed in  _lpEntryID_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f20df-142">注釈</span><span class="sxs-lookup"><span data-stu-id="f20df-142">Remarks</span></span>

<span data-ttu-id="f20df-143">アドレス帳プロバイダーは、 **IABLogon:: Advise**メソッドを実装して、コンテナーのいずれかのオブジェクトが変更されたときに通知されるように呼び出し元を登録します。</span><span class="sxs-lookup"><span data-stu-id="f20df-143">Address book providers implement the **IABLogon::Advise** method to register the caller to be notified when a change occurs to an object in one of their containers.</span></span> <span data-ttu-id="f20df-144">発信者は、メッセージングユーザー、配布リスト、またはコンテナー全体に関する通知を登録できます。</span><span class="sxs-lookup"><span data-stu-id="f20df-144">Callers can register for notifications regarding messaging users, distribution lists, or entire containers.</span></span> 
  
<span data-ttu-id="f20df-145">通常、クライアントは[IAddrBook:: アドバイズ](iaddrbook-advise.md)メソッドを呼び出して、アドレス帳の通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="f20df-145">Clients typically call the [IAddrBook::Advise](iaddrbook-advise.md) method to register for address book notifications.</span></span> <span data-ttu-id="f20df-146">その後、MAPI は、アドレス帳プロバイダーの**アドバイズ**メソッドを呼び出します。このメソッドは、 _lて tryid_内のエントリ識別子によって表されるオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="f20df-146">MAPI then calls the **Advise** method of the address book provider that is responsible for the object represented by the entry identifier in  _lpEntryID_.</span></span>
  
<span data-ttu-id="f20df-147">_uleventmask_で表される型の指定されたオブジェクトに変更が行われると、 _lpAdviseSink_によって参照されるアドバイズシンクの**onnotify**メソッドが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="f20df-147">When a change occurs to the indicated object of the type represented in  _ulEventMask_, a call is made to the **OnNotify** method of the advise sink pointed to by  _lpAdviseSink_.</span></span> <span data-ttu-id="f20df-148">**通知**構造で**onnotify**ルーチンに渡されるデータは、イベントについての説明です。</span><span class="sxs-lookup"><span data-stu-id="f20df-148">Data passed in the **NOTIFICATION** structure to the **OnNotify** routine describes the event.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f20df-149">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="f20df-149">Notes to implementers</span></span>

<span data-ttu-id="f20df-150">MAPI からのヘルプを含む、または使用しない通知をサポートできます。</span><span class="sxs-lookup"><span data-stu-id="f20df-150">You can support notification with or without help from MAPI.</span></span> <span data-ttu-id="f20df-151">MAPI には、サービスプロバイダーが通知を実装するための3つのサポートオブジェクトメソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="f20df-151">MAPI has three support object methods to help service providers implement notification:</span></span>
  
- [<span data-ttu-id="f20df-152">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="f20df-152">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)
    
- [<span data-ttu-id="f20df-153">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="f20df-153">IMAPISupport::Unsubscribe</span></span>](imapisupport-unsubscribe.md)
    
- [<span data-ttu-id="f20df-154">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="f20df-154">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
    
<span data-ttu-id="f20df-155">MAPI サポートメソッドを使用する場合は、 **Advise**メソッドが呼び出されたときに**Subscribe**を呼び出し、 _lpAdviseSink_ポインターを離します。</span><span class="sxs-lookup"><span data-stu-id="f20df-155">If you elect to use the MAPI support methods, call **Subscribe** when your **Advise** method is called and release the  _lpAdviseSink_ pointer.</span></span> 
  
<span data-ttu-id="f20df-156">自分で通知をサポートすることを選択する場合は、このポインターのコピーを保持するために、 _lpAdviseSink_パラメーターで表されるアドバイズシンクの**AddRef**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f20df-156">If you elect to support notification yourself, call the **AddRef** method of the advise sink represented by the  _lpAdviseSink_ parameter to keep a copy of this pointer.</span></span> <span data-ttu-id="f20df-157">登録を取り消すには、 [IABLogon:: アドバイズ](iablogon-unadvise.md)中止メソッドが呼び出されるまで、このコピーを保持します。</span><span class="sxs-lookup"><span data-stu-id="f20df-157">Maintain this copy until your [IABLogon::Unadvise](iablogon-unadvise.md) method is called to cancel the registration.</span></span> 
  
<span data-ttu-id="f20df-158">通知のサポート方法に関係なく、通知登録に0以外の接続番号を割り当て、lアウト_connection_パラメーターで返します。</span><span class="sxs-lookup"><span data-stu-id="f20df-158">Regardless of how you support notification, assign a nonzero connection number to the notification registration and return it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="f20df-159">この接続番号は、**アドバイズ**中止メソッドが呼び出されるまで解放しないでください。</span><span class="sxs-lookup"><span data-stu-id="f20df-159">Do not release this connection number until the **Unadvise** method has been called.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f20df-160">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="f20df-160">Notes to callers</span></span>

<span data-ttu-id="f20df-161">_lpAdviseSink_パラメーターで指定するアドバイズシンクポインターは、作成し\*\*\*\* たオブジェクト、または MAPI が[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)関数を使用して作成したオブジェクトを指すことができます。</span><span class="sxs-lookup"><span data-stu-id="f20df-161">The advise sink pointer that you pass in the  _lpAdviseSink_ parameter to **Advise** can point to an object that you have created or that MAPI has created through the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> <span data-ttu-id="f20df-162">複数の実行スレッドをサポートしていて、その後の**onnotify**メソッドへの後続の呼び出しが適切なスレッドの適切な時間に発生するようにするには、 **HrThisThreadAdviseSink**を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f20df-162">You might want to use **HrThisThreadAdviseSink** if you support multiple threads of execution and want to be sure that that subsequent calls to your **OnNotify** method occur at an appropriate time on an appropriate thread.</span></span> 
  
<span data-ttu-id="f20df-163">アドバイズシンクオブジェクトは、アドバイズを呼び出した後、**アドバイズ**中止の呼び出し前\*\*\*\* にリリースされるように準備しておいてください。</span><span class="sxs-lookup"><span data-stu-id="f20df-163">Be prepared for your advise sink object to be released any time after your call to **Advise** and before your call to **Unadvise**.</span></span> <span data-ttu-id="f20df-164">そのため、特定の長期に使用していない限り、**アドバイズ**が返された後にアドバイズシンクオブジェクトを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f20df-164">Therefore, you should release your advise sink object after **Advise** returns, unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="f20df-165">通知プロセスの詳細については、「 [MAPI でのイベント通知](event-notification-in-mapi.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f20df-165">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="f20df-166">**imapisupport**メソッドを使用して通知をサポートする方法については、「[サポートイベントの通知](supporting-event-notification.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f20df-166">For information about how to use the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span> <span data-ttu-id="f20df-167">マルチスレッドと mapi の詳細については、「 [mapi でのスレッド処理](threading-in-mapi.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f20df-167">For more information about multithreading and MAPI, see [Threading in MAPI](threading-in-mapi.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f20df-168">関連項目</span><span class="sxs-lookup"><span data-stu-id="f20df-168">See also</span></span>



[<span data-ttu-id="f20df-169">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="f20df-169">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="f20df-170">IABLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="f20df-170">IABLogon::Unadvise</span></span>](iablogon-unadvise.md)
  
[<span data-ttu-id="f20df-171">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="f20df-171">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="f20df-172">�ʒm</span><span class="sxs-lookup"><span data-stu-id="f20df-172">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="f20df-173">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f20df-173">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

