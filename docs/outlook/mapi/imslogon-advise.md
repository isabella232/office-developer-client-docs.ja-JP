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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: abe4867b965f05e781f931d2e72920474d007d78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317312"
---
# <a name="imslogonadvise"></a><span data-ttu-id="5c126-103">IMSLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="5c126-103">IMSLogon::Advise</span></span>

  
  
<span data-ttu-id="5c126-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c126-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c126-105">メッセージストアの変更について通知するために、オブジェクトをメッセージストアプロバイダーに登録します。</span><span class="sxs-lookup"><span data-stu-id="5c126-105">Registers an object with a message store provider for notifications about changes in the message store.</span></span> <span data-ttu-id="5c126-106">その後、メッセージストアは、登録されたオブジェクトへの変更に関する通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="5c126-106">The message store will then send notifications about changes to the registered object.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="5c126-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5c126-107">Parameters</span></span>

 <span data-ttu-id="5c126-108">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="5c126-108">_cbEntryID_</span></span>
  
> <span data-ttu-id="5c126-109">順番_lな tryid_パラメーターで指定されたエントリ識別子のサイズ (バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="5c126-109">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="5c126-110">_lて tryid_</span><span class="sxs-lookup"><span data-stu-id="5c126-110">_lpEntryID_</span></span>
  
> <span data-ttu-id="5c126-111">順番通知を生成するオブジェクトのエントリ id へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5c126-111">[in] A pointer to the entry identifier of the object about which notifications should be generated.</span></span> <span data-ttu-id="5c126-112">このオブジェクトには、フォルダー、メッセージ、またはメッセージストア内のその他のオブジェクトを指定できます。</span><span class="sxs-lookup"><span data-stu-id="5c126-112">This object can be a folder, a message, or any other object in the message store.</span></span> <span data-ttu-id="5c126-113">または、MAPI が_cbEntryID_パラメーターを0に設定し、 _l tryid_に対して**null**を渡す場合、アドバイズシンクはメッセージストア全体に対する変更に関する通知を提供します。</span><span class="sxs-lookup"><span data-stu-id="5c126-113">Alternatively, if MAPI sets the  _cbEntryID_ parameter to 0 and passes **null** for  _lpEntryID_, the advise sink provides notifications about changes to the entire message store.</span></span>
    
 <span data-ttu-id="5c126-114">_uleventmask_</span><span class="sxs-lookup"><span data-stu-id="5c126-114">_ulEventMask_</span></span>
  
> <span data-ttu-id="5c126-115">順番MAPI が通知を生成するオブジェクトに対して発生する通知イベントの種類のイベントマスク。</span><span class="sxs-lookup"><span data-stu-id="5c126-115">[in] An event mask of the types of notification events occurring for the object about which MAPI will generate notifications.</span></span> <span data-ttu-id="5c126-116">マスクは特定のケースをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="5c126-116">The mask filters specific cases.</span></span> <span data-ttu-id="5c126-117">各イベントの種類には、イベントに関する追加情報を含む構造が関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="5c126-117">Each event type has a structure associated with it that contains additional information about the event.</span></span> <span data-ttu-id="5c126-118">次の表に、考えられるイベントの種類とそれに対応する構造を示します。</span><span class="sxs-lookup"><span data-stu-id="5c126-118">The following table lists the possible event types along with their corresponding structures.</span></span>
    
|<span data-ttu-id="5c126-119">**通知イベントの種類**</span><span class="sxs-lookup"><span data-stu-id="5c126-119">**Notification event type**</span></span>|<span data-ttu-id="5c126-120">**対応する構造**</span><span class="sxs-lookup"><span data-stu-id="5c126-120">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5c126-121">fnevCriticalError</span><span class="sxs-lookup"><span data-stu-id="5c126-121">fnevCriticalError</span></span>  <br/> |[<span data-ttu-id="5c126-122">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="5c126-122">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="5c126-123">fnevNewMail</span><span class="sxs-lookup"><span data-stu-id="5c126-123">fnevNewMail</span></span>  <br/> |[<span data-ttu-id="5c126-124">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="5c126-124">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md) <br/> |
|<span data-ttu-id="5c126-125">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="5c126-125">fnevObjectCreated</span></span>  <br/> |[<span data-ttu-id="5c126-126">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="5c126-126">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="5c126-127">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="5c126-127">fnevObjectDeleted</span></span>  <br/> |[<span data-ttu-id="5c126-128">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="5c126-128">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="5c126-129">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="5c126-129">fnevObjectModified</span></span>  <br/> |[<span data-ttu-id="5c126-130">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="5c126-130">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="5c126-131">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="5c126-131">fnevObjectCopied</span></span>  <br/> |[<span data-ttu-id="5c126-132">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="5c126-132">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="5c126-133">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="5c126-133">fnevObjectMoved</span></span>  <br/> |[<span data-ttu-id="5c126-134">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="5c126-134">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="5c126-135">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="5c126-135">fnevSearchComplete</span></span>  <br/> |[<span data-ttu-id="5c126-136">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="5c126-136">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="5c126-137">fnevStatusObjectModified</span><span class="sxs-lookup"><span data-stu-id="5c126-137">fnevStatusObjectModified</span></span>  <br/> |[<span data-ttu-id="5c126-138">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="5c126-138">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md) <br/> |
   
 <span data-ttu-id="5c126-139">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="5c126-139">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="5c126-140">順番通知が要求された session オブジェクトに対してイベントが発生したときに呼び出されるアドバイズシンクオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5c126-140">[in] A pointer to an advise sink object to be called when an event occurs for the session object about which notification has been requested.</span></span> <span data-ttu-id="5c126-141">このアドバイズシンクオブジェクトは、既に存在している必要があります。</span><span class="sxs-lookup"><span data-stu-id="5c126-141">This advise sink object must already exist.</span></span>
    
 <span data-ttu-id="5c126-142">_lアウト接続_</span><span class="sxs-lookup"><span data-stu-id="5c126-142">_lpulConnection_</span></span>
  
> <span data-ttu-id="5c126-143">読み上げ成功した場合に、通知登録の接続番号を保持する変数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5c126-143">[out] A pointer to a variable that upon a successful return holds the connection number for the notification registration.</span></span> <span data-ttu-id="5c126-144">接続番号は0以外の値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="5c126-144">The connection number must be nonzero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5c126-145">戻り値</span><span class="sxs-lookup"><span data-stu-id="5c126-145">Return value</span></span>

<span data-ttu-id="5c126-146">S_OK</span><span class="sxs-lookup"><span data-stu-id="5c126-146">S_OK</span></span> 
  
> <span data-ttu-id="5c126-147">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="5c126-147">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="5c126-148">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="5c126-148">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="5c126-149">この操作は、MAPI または1つ以上のサービスプロバイダーによってサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="5c126-149">The operation is not supported by MAPI or by one or more service providers.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5c126-150">解説</span><span class="sxs-lookup"><span data-stu-id="5c126-150">Remarks</span></span>

<span data-ttu-id="5c126-151">メッセージストアプロバイダーは、通知コールバック用のオブジェクトを登録する**IMSLogon:: Advise**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="5c126-151">Message store providers implement the **IMSLogon::Advise** method to register an object for notification callbacks.</span></span> <span data-ttu-id="5c126-152">指定したオブジェクトが変更されるたびに、プロバイダーはイベントマスクビットが_uleventmask_パラメーターで設定されているかどうかを確認します。そのため、発生した変更の種類がわかります。</span><span class="sxs-lookup"><span data-stu-id="5c126-152">Whenever a change occurs to the indicated object, the provider checks to see what event mask bit was set in the  _ulEventMask_ parameter and, therefore, what type of change occurred.</span></span> <span data-ttu-id="5c126-153">ビットが設定されている場合、プロバイダーは、 _lpAdviseSink_パラメーターによって示されるアドバイズシンクオブジェクトの[IMAPIAdviseSink:: onnotify](imapiadvisesink-onnotify.md)メソッドを呼び出して、イベントを報告します。</span><span class="sxs-lookup"><span data-stu-id="5c126-153">If a bit is set, the provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object indicated by the  _lpAdviseSink_ parameter to report the event.</span></span> <span data-ttu-id="5c126-154">通知構造で**onnotify**ルーチンに渡されるデータは、イベントについての説明です。</span><span class="sxs-lookup"><span data-stu-id="5c126-154">Data passed in the notification structure to the **OnNotify** routine describes the event.</span></span> 
  
<span data-ttu-id="5c126-155">**onnotify**への呼び出しは、オブジェクトを変更する呼び出し中、または後で発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="5c126-155">The call to **OnNotify** can occur during the call that changes the object, or at any later time.</span></span> <span data-ttu-id="5c126-156">複数の実行スレッドをサポートするシステムでは、 **onnotify**への呼び出しは任意のスレッドで発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5c126-156">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="5c126-157">inopportune 時に発生する可能性がある**onnotify**への呼び出しを安全に処理するには、クライアントアプリケーションで[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)関数を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5c126-157">To safely handle a call to **OnNotify** that might happen at an inopportune time, a client application should use the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="5c126-158">通知を提供するために、**アドバイズ**を実装するメッセージストアプロバイダーは、 _lpAdviseSink_アドバイズシンクオブジェクトへのポインターのコピーを保持する必要があります。そのために、プロバイダーはアドバイズシンクに対して[IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)メソッドを呼び出し、 [IMSLogon:: アドバイズ](imslogon-unadvise.md)中止メソッドの呼び出しによって通知登録が取り消されるまでオブジェクトポインターを保持します。</span><span class="sxs-lookup"><span data-stu-id="5c126-158">To provide notifications, the message store provider that implements **Advise** needs to keep a copy of the pointer to the  _lpAdviseSink_ advise sink object; to do so, the provider calls the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method for the advise sink to maintain its object pointer until notification registration is canceled with a call to the [IMSLogon::Unadvise](imslogon-unadvise.md) method.</span></span> <span data-ttu-id="5c126-159">**アドバイズ**実装は、接続番号を通知登録に割り当て、この接続番号で**AddRef**を呼び出してから、lアウト_connection_パラメーターで取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5c126-159">The **Advise** implementation should assign a connection number to the notification registration and call **AddRef** on this connection number before returning it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="5c126-160">登録が取り消される前に、サービスプロバイダーはアドバイズシンクオブジェクトを解放できますが、**アドバイズ**が呼び出されるまで接続番号を解放する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="5c126-160">Service providers can release the advise sink object before the registration is canceled, but they must not release the connection number until **Unadvise** has been called.</span></span> 
  
<span data-ttu-id="5c126-161">アドバイズの呼び出しが\*\*\*\* 成功し、**アドバイズ**中止が呼び出される前に、アドバイズシンクオブジェクトをリリースするためのプロバイダーを準備する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5c126-161">After a call to **Advise** has succeeded and before **Unadvise** has been called, providers must be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="5c126-162">そのため、プロバイダーは、特定の長期の使用がない限り、**アドバイズ**が返された後に、アドバイズシンクオブジェクトを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5c126-162">Therefore, a provider should release its advise sink object after **Advise** returns, unless it has a specific long-term use for it.</span></span> 
  
<span data-ttu-id="5c126-163">通知プロセスの詳細については、「 [MAPI でのイベント通知](event-notification-in-mapi.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5c126-163">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5c126-164">関連項目</span><span class="sxs-lookup"><span data-stu-id="5c126-164">See also</span></span>



[<span data-ttu-id="5c126-165">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="5c126-165">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="5c126-166">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="5c126-166">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="5c126-167">IMSLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="5c126-167">IMSLogon::Unadvise</span></span>](imslogon-unadvise.md)
  
[<span data-ttu-id="5c126-168">�ʒm</span><span class="sxs-lookup"><span data-stu-id="5c126-168">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="5c126-169">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5c126-169">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

