---
title: IMAPIAdviseSinkOnNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIAdviseSink.OnNotify
api_type:
- COM
ms.assetid: 9eec90d3-2369-4340-86ed-0efa58918ed5
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5983ed3229f6b0053f15a614116cf5680e942587
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407362"
---
# <a name="imapiadvisesinkonnotify"></a><span data-ttu-id="cd64c-103">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="cd64c-103">IMAPIAdviseSink::OnNotify</span></span>

  
  
<span data-ttu-id="cd64c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd64c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd64c-105">1つまたは複数のタスクを実行して通知に応答します。</span><span class="sxs-lookup"><span data-stu-id="cd64c-105">Responds to a notification by performing one or more tasks.</span></span> <span data-ttu-id="cd64c-106">実行されるタスクは、イベントの種類と通知を生成するオブジェクトによって異なります。</span><span class="sxs-lookup"><span data-stu-id="cd64c-106">The tasks performed depend on the type of event and the object that generates the notification.</span></span> 
  
```cpp
ULONG OnNotify(
  ULONG cNotif,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a><span data-ttu-id="cd64c-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cd64c-107">Parameters</span></span>

 <span data-ttu-id="cd64c-108">_cNotif_</span><span class="sxs-lookup"><span data-stu-id="cd64c-108">_cNotif_</span></span>
  
> <span data-ttu-id="cd64c-109">順番lpnotifications パラメーターが指す[通知](notification.md)構造の数__ 。</span><span class="sxs-lookup"><span data-stu-id="cd64c-109">[in] The count of [NOTIFICATION](notification.md) structures pointed to by the  _lpNotifications_ parameter.</span></span> 
    
 <span data-ttu-id="cd64c-110">_lpnotifications_</span><span class="sxs-lookup"><span data-stu-id="cd64c-110">_lpNotifications_</span></span>
  
> <span data-ttu-id="cd64c-111">順番発生したイベントに関する情報を提供する1つまたは複数の**通知**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="cd64c-111">[in] A pointer to one or more **NOTIFICATION** structures that provide information about the events that have occurred.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cd64c-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="cd64c-112">Return value</span></span>

<span data-ttu-id="cd64c-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="cd64c-113">S_OK</span></span> 
  
> <span data-ttu-id="cd64c-114">通知が正常に処理されました。</span><span class="sxs-lookup"><span data-stu-id="cd64c-114">The notification was processed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cd64c-115">注釈</span><span class="sxs-lookup"><span data-stu-id="cd64c-115">Remarks</span></span>

<span data-ttu-id="cd64c-116">通知プロセスは、クライアントまたは MAPI が、特定のオブジェクトの特定の種類の通知を受信するために登録するために、サービスプロバイダーの**アドバイズ**メソッドを呼び出すと開始されます。</span><span class="sxs-lookup"><span data-stu-id="cd64c-116">The notification process starts when a client or MAPI makes a call to a service provider's **Advise** method to register to receive a notification of a particular type for a particular object.</span></span> <span data-ttu-id="cd64c-117">**advise**メソッドへのパラメーターの1つは、 [IMAPIAdviseSink](imapiadvisesinkiunknown.md)インターフェイスを実装するアドバイズシンクオブジェクトへのポインターです。</span><span class="sxs-lookup"><span data-stu-id="cd64c-117">One of the parameters to the **Advise** method is a pointer to an advise sink object that implements the [IMAPIAdviseSink](imapiadvisesinkiunknown.md) interface.</span></span> <span data-ttu-id="cd64c-118">登録されている通知に対応するターゲットオブジェクトに対してイベントが発生すると、サービスプロバイダーは MAPI を使用して直接または間接的に、アドバイズシンクの**onnotify**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="cd64c-118">When an event occurs to the target object that corresponds to the registered notification, the service provider, either directly or indirectly through MAPI, calls the advise sink's **OnNotify** method.</span></span> 
  
<span data-ttu-id="cd64c-119">**onnotify**への呼び出しは、そのイベントを発生させた MAPI 呼び出しの間、または後で発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="cd64c-119">The call to **OnNotify** can occur either during the MAPI call that is causing the event or at some later time.</span></span> <span data-ttu-id="cd64c-120">複数の実行スレッドをサポートするシステムでは、 **onnotify**は、登録に使用したのと同じスレッドで、または別のスレッドで呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="cd64c-120">On systems that support multiple threads of execution, **OnNotify** can be called either on the same thread that was used for registration or on a different thread.</span></span> <span data-ttu-id="cd64c-121">クライアントでは、 [HrThisThreadAdviseSink](hrthisthreadadvisesink.md)関数を使用して**アドバイズ**するアドバイズシンクを作成すること\*\*\*\* によって、notify の呼び出しに使用したのと同じスレッドで**onnotify**呼び出しが行われるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="cd64c-121">Clients can make sure that the **OnNotify** call is made on the same thread used to call **Advise** by creating the advise sink that they pass to **Advise** with the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="cd64c-122">_lpnotifications_パラメーターは、イベント中に変更された内容を示す1つ以上の**通知**構造を指します。</span><span class="sxs-lookup"><span data-stu-id="cd64c-122">The  _lpNotifications_ parameter points to one or more **NOTIFICATION** structures that describe what has changed during the event.</span></span> <span data-ttu-id="cd64c-123">イベントの種類ごとに異なる種類の**通知**構造があります。</span><span class="sxs-lookup"><span data-stu-id="cd64c-123">There is a different type of **NOTIFICATION** structure for each type of event.</span></span> 
  
<span data-ttu-id="cd64c-124">次の表に、使用可能なイベントの種類と、各値に関連付けられている構造を表すために使用される値を示します。</span><span class="sxs-lookup"><span data-stu-id="cd64c-124">The following table lists the values that are used to represent the possible types of events and the structures associated with each value:</span></span>
  
|<span data-ttu-id="cd64c-125">**通知イベントの種類**</span><span class="sxs-lookup"><span data-stu-id="cd64c-125">**Notification event type**</span></span>|<span data-ttu-id="cd64c-126">**対応する構造**</span><span class="sxs-lookup"><span data-stu-id="cd64c-126">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd64c-127">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="cd64c-127">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="cd64c-128">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="cd64c-128">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="cd64c-129">**fnevNewMail**</span><span class="sxs-lookup"><span data-stu-id="cd64c-129">**fnevNewMail**</span></span> <br/> |[<span data-ttu-id="cd64c-130">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="cd64c-130">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md) <br/> |
|<span data-ttu-id="cd64c-131">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="cd64c-131">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="cd64c-132">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="cd64c-132">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="cd64c-133">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="cd64c-133">**fnevObjectDeleted**</span></span> <br/> |[<span data-ttu-id="cd64c-134">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="cd64c-134">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="cd64c-135">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="cd64c-135">**fnevObjectModified**</span></span> <br/> |[<span data-ttu-id="cd64c-136">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="cd64c-136">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="cd64c-137">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="cd64c-137">**fnevObjectCopied**</span></span> <br/> |[<span data-ttu-id="cd64c-138">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="cd64c-138">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="cd64c-139">**fnevSearchComplete**</span><span class="sxs-lookup"><span data-stu-id="cd64c-139">**fnevSearchComplete**</span></span> <br/> |[<span data-ttu-id="cd64c-140">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="cd64c-140">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="cd64c-141">**fnevTableModified**</span><span class="sxs-lookup"><span data-stu-id="cd64c-141">**fnevTableModified**</span></span> <br/> |[<span data-ttu-id="cd64c-142">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="cd64c-142">TABLE_NOTIFICATION</span></span>](table_notification.md) <br/> |
|<span data-ttu-id="cd64c-143">**fnevStatusObjectModified**</span><span class="sxs-lookup"><span data-stu-id="cd64c-143">**fnevStatusObjectModified**</span></span> <br/> |[<span data-ttu-id="cd64c-144">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="cd64c-144">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md) <br/> |
|<span data-ttu-id="cd64c-145">**fnevExtended**</span><span class="sxs-lookup"><span data-stu-id="cd64c-145">**fnevExtended**</span></span> <br/> |[<span data-ttu-id="cd64c-146">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="cd64c-146">EXTENDED_NOTIFICATION</span></span>](extended_notification.md) <br/> |
   
<span data-ttu-id="cd64c-147">通知の設定および停止の詳細については、次のいずれかのインターフェイスの**Advise**および**アドバイズ**メソッドの参照エントリを参照してください。 [IABLogon](iablogoniunknown.md)、 [IAddrBook](iaddrbookimapiprop.md)、 [imapiform](imapiformiunknown.md)、 [imapisession](imapisessioniunknown.md)、 [IMAPITable](imapitableiunknown.md)、 [IMsgStore](imsgstoreimapiprop.md)、および[IMSLogon](imslogoniunknown.md)。</span><span class="sxs-lookup"><span data-stu-id="cd64c-147">For more information about how to set up and stop notifications, see the reference entries for the **Advise** and **Unadvise** methods for any of the following interfaces: [IABLogon](iablogoniunknown.md), [IAddrBook](iaddrbookimapiprop.md), [IMAPIForm](imapiformiunknown.md), [IMAPISession](imapisessioniunknown.md), [IMAPITable](imapitableiunknown.md), [IMsgStore](imsgstoreimapiprop.md), and [IMSLogon](imslogoniunknown.md).</span></span> 
  
<span data-ttu-id="cd64c-148">通知プロセスに関する一般的な情報については、「 [MAPI でのイベント通知](event-notification-in-mapi.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cd64c-148">For general information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="cd64c-149">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="cd64c-149">Notes to implementers</span></span>

<span data-ttu-id="cd64c-150">通常、 **onnotify**実装は、受信する通知の種類ごとに1つ以上のコードブロックで構成されます。</span><span class="sxs-lookup"><span data-stu-id="cd64c-150">Your **OnNotify** implementation will typically consist of one or more blocks of code for each type of notification you expect to receive.</span></span> <span data-ttu-id="cd64c-151">これらのコードブロック内で、通知への応答として必要と考えられるすべてのタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="cd64c-151">Within these blocks of code, perform any tasks that you consider necessary as a response to the notification.</span></span> <span data-ttu-id="cd64c-152">たとえば、ダイアログボックスの表示に含まれているフォルダーで**fnevObjectModified**通知を受信するように登録したとします。</span><span class="sxs-lookup"><span data-stu-id="cd64c-152">For example, suppose you register to receive **fnevObjectModified** notifications on a folder that is included in a dialog box display.</span></span> <span data-ttu-id="cd64c-153">**fnevObjectModified**通知を処理するために**onnotify**メソッドに含めるコードのブロックでは、Windows メッセージをダイアログボックスに送信して、更新された表示を要求することができます。</span><span class="sxs-lookup"><span data-stu-id="cd64c-153">In the block of code that you include in your **OnNotify** method to handle **fnevObjectModified** notifications, you might send a Windows message to the dialog box to request an updated display.</span></span> 
  
<span data-ttu-id="cd64c-154">**onnotify**に渡された**通知**構造を変更または解放しないでください。</span><span class="sxs-lookup"><span data-stu-id="cd64c-154">Do not modify or free the **NOTIFICATION** structure passed to **OnNotify**.</span></span> <span data-ttu-id="cd64c-155">構造内のデータは、 **onnotify**から戻るまで有効です。</span><span class="sxs-lookup"><span data-stu-id="cd64c-155">The data in the structure is valid only until **OnNotify** returns.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="cd64c-156">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="cd64c-156">Notes to callers</span></span>

<span data-ttu-id="cd64c-157">複数のオブジェクトに変更が発生した場合は、メモリの制約に応じて、 **onnotify**または複数の呼び出しに対して、登録されているアドバイズシンクに対して1回の呼び出しで通知できます。</span><span class="sxs-lookup"><span data-stu-id="cd64c-157">When changes occur to multiple objects, you can notify a registered advise sink in a single call to **OnNotify** or in multiple calls depending on memory constraints.</span></span> <span data-ttu-id="cd64c-158">これは、変更が1つのメソッド呼び出しまたは複数の方法の結果であるかどうかに関係なく該当します。</span><span class="sxs-lookup"><span data-stu-id="cd64c-158">This is true regardless of whether the changes are the result of one method call or several.</span></span> <span data-ttu-id="cd64c-159">たとえば、 [imapifolder:: copymessages](imapifolder-copymessages.md)を呼び出すと、複数のメッセージとフォルダーが影響を受ける可能性があります。</span><span class="sxs-lookup"><span data-stu-id="cd64c-159">For example, a call to [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) can affect multiple messages and folders.</span></span> <span data-ttu-id="cd64c-160">メッセージストアプロバイダーとして、1回の呼び出しを\*\*\*\* 、ターゲットフォルダーの**fnevObjectModified**イベントの種類を使用して、または複数の呼び出しを行うことができます。それぞれがメッセージに影響します。</span><span class="sxs-lookup"><span data-stu-id="cd64c-160">As a message store provider, you can make one call to **OnNotify** with an **fnevObjectModified** event type for the target folder or many calls, one for each affect messages.</span></span> <span data-ttu-id="cd64c-161">同様に、クライアントが[imapifolder:: CreateMessage](imapifolder-createmessage.md)を繰り返し呼び出した場合、これらの呼び出しはフォルダーの1つの**fnevObjectModified**イベントに結合するか、新しいメッセージごとに個別の**fnevObjectCreated**イベントに分割することができます。</span><span class="sxs-lookup"><span data-stu-id="cd64c-161">Similarly, if a client makes repeated calls to [IMAPIFolder::CreateMessage](imapifolder-createmessage.md), these calls can be combined into one **fnevObjectModified** event for the folder or separated into individual **fnevObjectCreated** events for each new message.</span></span> 
  
<span data-ttu-id="cd64c-162">通知を生成する方法とタイミングの詳細については、「 [MAPI でのイベント通知](event-notification-in-mapi.md)」と「[サポートイベントの通知](supporting-event-notification.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cd64c-162">For more information about how and when to generate notifications, see [Event Notification in MAPI](event-notification-in-mapi.md) and [Supporting Event Notification](supporting-event-notification.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="cd64c-163">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="cd64c-163">MFCMAPI reference</span></span>

<span data-ttu-id="cd64c-164">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cd64c-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="cd64c-165">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="cd64c-165">**File**</span></span>|<span data-ttu-id="cd64c-166">**関数**</span><span class="sxs-lookup"><span data-stu-id="cd64c-166">**Function**</span></span>|<span data-ttu-id="cd64c-167">**コメント**</span><span class="sxs-lookup"><span data-stu-id="cd64c-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cd64c-168">AdviseSink および AdviseSink</span><span class="sxs-lookup"><span data-stu-id="cd64c-168">AdviseSink.h and AdviseSink.cpp</span></span>  <br/> |<span data-ttu-id="cd64c-169">CAdviseSink:: onnotifydesc</span><span class="sxs-lookup"><span data-stu-id="cd64c-169">CAdviseSink::OnNotifyDesc</span></span>  <br/> |<span data-ttu-id="cd64c-170">CAdviseSink クラスは、すべての通知を mfcmapi で処理するために実装されています。</span><span class="sxs-lookup"><span data-stu-id="cd64c-170">The CAdviseSink class is implemented to handle all notifications in MFCMAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cd64c-171">関連項目</span><span class="sxs-lookup"><span data-stu-id="cd64c-171">See also</span></span>



[<span data-ttu-id="cd64c-172">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="cd64c-172">HrAllocAdviseSink</span></span>](hrallocadvisesink.md)
  
[<span data-ttu-id="cd64c-173">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="cd64c-173">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="cd64c-174">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="cd64c-174">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
  
[<span data-ttu-id="cd64c-175">�ʒm</span><span class="sxs-lookup"><span data-stu-id="cd64c-175">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="cd64c-176">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cd64c-176">IMAPIAdviseSink : IUnknown</span></span>](imapiadvisesinkiunknown.md)


<span data-ttu-id="cd64c-177">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="cd64c-177">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

