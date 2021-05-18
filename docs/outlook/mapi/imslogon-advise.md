---
title: IMSLogonAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.Advise
api_type:
- COM
ms.assetid: a3c5d937-642b-463b-b5a0-5d099e651895
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: abe4867b965f05e781f931d2e72920474d007d78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317312"
---
# <a name="imslogonadvise"></a><span data-ttu-id="4c9b6-103">IMSLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="4c9b6-103">IMSLogon::Advise</span></span>

  
  
<span data-ttu-id="4c9b6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c9b6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c9b6-105">メッセージ ストア内の変更に関する通知のために、メッセージ ストア プロバイダーにオブジェクトを登録します。</span><span class="sxs-lookup"><span data-stu-id="4c9b6-105">Registers an object with a message store provider for notifications about changes in the message store.</span></span> <span data-ttu-id="4c9b6-106">メッセージ ストアは、登録されているオブジェクトに対する変更に関する通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="4c9b6-106">The message store will then send notifications about changes to the registered object.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="4c9b6-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4c9b6-107">Parameters</span></span>

 <span data-ttu-id="4c9b6-108">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="4c9b6-108">_cbEntryID_</span></span>
  
> <span data-ttu-id="4c9b6-109">[in]  _lpEntryID_ パラメーターが指すエントリ識別子のサイズ (バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="4c9b6-109">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="4c9b6-110">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="4c9b6-110">_lpEntryID_</span></span>
  
> <span data-ttu-id="4c9b6-111">[in]どの通知を生成する必要があるオブジェクトのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4c9b6-111">[in] A pointer to the entry identifier of the object about which notifications should be generated.</span></span> <span data-ttu-id="4c9b6-112">このオブジェクトには、フォルダー、メッセージ、またはメッセージ ストア内の他のオブジェクトを指定できます。</span><span class="sxs-lookup"><span data-stu-id="4c9b6-112">This object can be a folder, a message, or any other object in the message store.</span></span> <span data-ttu-id="4c9b6-113">または、MAPI が cbEntryID パラメーターを 0 に設定し _、lpEntryID_ に **null** を渡す場合は、メッセージ ストア全体に対する変更に関する通知が提供されます。 </span><span class="sxs-lookup"><span data-stu-id="4c9b6-113">Alternatively, if MAPI sets the  _cbEntryID_ parameter to 0 and passes **null** for  _lpEntryID_, the advise sink provides notifications about changes to the entire message store.</span></span>
    
 <span data-ttu-id="4c9b6-114">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="4c9b6-114">_ulEventMask_</span></span>
  
> <span data-ttu-id="4c9b6-115">[in]MAPI が通知を生成するオブジェクトに対して発生する通知イベントの種類のイベント マスク。</span><span class="sxs-lookup"><span data-stu-id="4c9b6-115">[in] An event mask of the types of notification events occurring for the object about which MAPI will generate notifications.</span></span> <span data-ttu-id="4c9b6-116">マスクは、特定のケースをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="4c9b6-116">The mask filters specific cases.</span></span> <span data-ttu-id="4c9b6-117">各イベントの種類には、イベントに関する追加情報を含む構造が関連付けられている。</span><span class="sxs-lookup"><span data-stu-id="4c9b6-117">Each event type has a structure associated with it that contains additional information about the event.</span></span> <span data-ttu-id="4c9b6-118">次の表に、可能なイベントの種類と対応する構造を示します。</span><span class="sxs-lookup"><span data-stu-id="4c9b6-118">The following table lists the possible event types along with their corresponding structures.</span></span>
    
|<span data-ttu-id="4c9b6-119">**通知イベントの種類**</span><span class="sxs-lookup"><span data-stu-id="4c9b6-119">**Notification event type**</span></span>|<span data-ttu-id="4c9b6-120">**対応する構造**</span><span class="sxs-lookup"><span data-stu-id="4c9b6-120">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4c9b6-121">fnevCriticalError</span><span class="sxs-lookup"><span data-stu-id="4c9b6-121">fnevCriticalError</span></span>  <br/> |[<span data-ttu-id="4c9b6-122">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4c9b6-122">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="4c9b6-123">fnevNewMail</span><span class="sxs-lookup"><span data-stu-id="4c9b6-123">fnevNewMail</span></span>  <br/> |[<span data-ttu-id="4c9b6-124">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4c9b6-124">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md) <br/> |
|<span data-ttu-id="4c9b6-125">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="4c9b6-125">fnevObjectCreated</span></span>  <br/> |[<span data-ttu-id="4c9b6-126">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4c9b6-126">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="4c9b6-127">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="4c9b6-127">fnevObjectDeleted</span></span>  <br/> |[<span data-ttu-id="4c9b6-128">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4c9b6-128">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="4c9b6-129">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="4c9b6-129">fnevObjectModified</span></span>  <br/> |[<span data-ttu-id="4c9b6-130">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4c9b6-130">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="4c9b6-131">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="4c9b6-131">fnevObjectCopied</span></span>  <br/> |[<span data-ttu-id="4c9b6-132">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4c9b6-132">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="4c9b6-133">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="4c9b6-133">fnevObjectMoved</span></span>  <br/> |[<span data-ttu-id="4c9b6-134">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4c9b6-134">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="4c9b6-135">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="4c9b6-135">fnevSearchComplete</span></span>  <br/> |[<span data-ttu-id="4c9b6-136">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4c9b6-136">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="4c9b6-137">fnevStatusObjectModified</span><span class="sxs-lookup"><span data-stu-id="4c9b6-137">fnevStatusObjectModified</span></span>  <br/> |[<span data-ttu-id="4c9b6-138">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4c9b6-138">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md) <br/> |
   
 <span data-ttu-id="4c9b6-139">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="4c9b6-139">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="4c9b6-140">[in]通知が要求されたセッション オブジェクトに対してイベントが発生した場合に呼び出されるアアドバイス シンク オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="4c9b6-140">[in] A pointer to an advise sink object to be called when an event occurs for the session object about which notification has been requested.</span></span> <span data-ttu-id="4c9b6-141">このアアドバイス シンク オブジェクトは既に存在している必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c9b6-141">This advise sink object must already exist.</span></span>
    
 <span data-ttu-id="4c9b6-142">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="4c9b6-142">_lpulConnection_</span></span>
  
> <span data-ttu-id="4c9b6-143">[out]戻り値が成功すると、通知登録の接続番号を保持する変数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4c9b6-143">[out] A pointer to a variable that upon a successful return holds the connection number for the notification registration.</span></span> <span data-ttu-id="4c9b6-144">接続番号は 0 以外である必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c9b6-144">The connection number must be nonzero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4c9b6-145">戻り値</span><span class="sxs-lookup"><span data-stu-id="4c9b6-145">Return value</span></span>

<span data-ttu-id="4c9b6-146">S_OK</span><span class="sxs-lookup"><span data-stu-id="4c9b6-146">S_OK</span></span> 
  
> <span data-ttu-id="4c9b6-147">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="4c9b6-147">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="4c9b6-148">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="4c9b6-148">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="4c9b6-149">この操作は、MAPI または 1 つ以上のサービス プロバイダーではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="4c9b6-149">The operation is not supported by MAPI or by one or more service providers.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4c9b6-150">注釈</span><span class="sxs-lookup"><span data-stu-id="4c9b6-150">Remarks</span></span>

<span data-ttu-id="4c9b6-151">メッセージ ストア プロバイダーは、通知コールバックのオブジェクトを登録する **IMSLogon::Advise** メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="4c9b6-151">Message store providers implement the **IMSLogon::Advise** method to register an object for notification callbacks.</span></span> <span data-ttu-id="4c9b6-152">指定されたオブジェクトに対して変更が発生するたびに、プロバイダーは  _ulEventMask_ パラメーターで設定されたイベント マスク ビットを確認し、したがって、どのような種類の変更が発生したのかを確認します。</span><span class="sxs-lookup"><span data-stu-id="4c9b6-152">Whenever a change occurs to the indicated object, the provider checks to see what event mask bit was set in the  _ulEventMask_ parameter and, therefore, what type of change occurred.</span></span> <span data-ttu-id="4c9b6-153">ビットが設定されている場合、プロバイダーは、イベントを報告するために lpAdviseSink パラメーターで示されるアアドバイス シンク オブジェクトの[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出します。 </span><span class="sxs-lookup"><span data-stu-id="4c9b6-153">If a bit is set, the provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object indicated by the  _lpAdviseSink_ parameter to report the event.</span></span> <span data-ttu-id="4c9b6-154">通知構造で **OnNotify** ルーチンに渡されたデータは、イベントについて説明します。</span><span class="sxs-lookup"><span data-stu-id="4c9b6-154">Data passed in the notification structure to the **OnNotify** routine describes the event.</span></span> 
  
<span data-ttu-id="4c9b6-155">**OnNotify の呼び出し** は、オブジェクトを変更する呼び出し中、または後で発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4c9b6-155">The call to **OnNotify** can occur during the call that changes the object, or at any later time.</span></span> <span data-ttu-id="4c9b6-156">複数の実行スレッドをサポートするシステムでは **、OnNotify** の呼び出しは任意のスレッドで行われます。</span><span class="sxs-lookup"><span data-stu-id="4c9b6-156">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="4c9b6-157">Inopportune 時に発生する可能性がある **OnNotify** の呼び出しを安全に処理するには、クライアント アプリケーションで [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) 関数を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c9b6-157">To safely handle a call to **OnNotify** that might happen at an inopportune time, a client application should use the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="4c9b6-158">通知を提供するには **、Advise** を実装するメッセージ ストア プロバイダーは _、lpAdviseSink_ アアドバイス シンク オブジェクトへのポインターのコピーを保持する必要があります。これを行うには、[プロバイダーは、IMSLogon::Unadvise](imslogon-unadvise.md)メソッドの呼び出しで通知登録が取り消されるまで、そのオブジェクト ポインターを維持するために、アドバイス シンクの [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4c9b6-158">To provide notifications, the message store provider that implements **Advise** needs to keep a copy of the pointer to the  _lpAdviseSink_ advise sink object; to do so, the provider calls the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method for the advise sink to maintain its object pointer until notification registration is canceled with a call to the [IMSLogon::Unadvise](imslogon-unadvise.md) method.</span></span> <span data-ttu-id="4c9b6-159">**Advise 実装では**、通知登録に接続番号を割り当て、lpulConnection パラメーターで返す前に、この接続番号で **AddRef** _を呼び出す必要_ があります。</span><span class="sxs-lookup"><span data-stu-id="4c9b6-159">The **Advise** implementation should assign a connection number to the notification registration and call **AddRef** on this connection number before returning it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="4c9b6-160">サービス プロバイダーは、登録が取り消される前にアアドバイス シンク オブジェクトを解放できますが **、Unadvise** が呼び出されるまで接続番号を解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c9b6-160">Service providers can release the advise sink object before the registration is canceled, but they must not release the connection number until **Unadvise** has been called.</span></span> 
  
<span data-ttu-id="4c9b6-161">**Advise** の呼び出しが成功し **、Unadvise** が呼び出される前に、アドバイス シンク オブジェクトが解放される準備が必要です。</span><span class="sxs-lookup"><span data-stu-id="4c9b6-161">After a call to **Advise** has succeeded and before **Unadvise** has been called, providers must be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="4c9b6-162">そのため、特定の長期的な使用がない限り、 **プロバイダーは、Advise** が返した後にアアドバイス シンク オブジェクトを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c9b6-162">Therefore, a provider should release its advise sink object after **Advise** returns, unless it has a specific long-term use for it.</span></span> 
  
<span data-ttu-id="4c9b6-163">通知プロセスの詳細については、「MAPI での [イベント通知」を参照してください](event-notification-in-mapi.md)。</span><span class="sxs-lookup"><span data-stu-id="4c9b6-163">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4c9b6-164">関連項目</span><span class="sxs-lookup"><span data-stu-id="4c9b6-164">See also</span></span>



[<span data-ttu-id="4c9b6-165">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="4c9b6-165">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="4c9b6-166">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="4c9b6-166">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="4c9b6-167">IMSLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="4c9b6-167">IMSLogon::Unadvise</span></span>](imslogon-unadvise.md)
  
[<span data-ttu-id="4c9b6-168">�ʒm</span><span class="sxs-lookup"><span data-stu-id="4c9b6-168">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="4c9b6-169">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4c9b6-169">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

