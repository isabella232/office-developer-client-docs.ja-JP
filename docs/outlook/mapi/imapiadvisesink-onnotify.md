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
# <a name="imapiadvisesinkonnotify"></a><span data-ttu-id="19f93-103">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="19f93-103">IMAPIAdviseSink::OnNotify</span></span>

  
  
<span data-ttu-id="19f93-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="19f93-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="19f93-105">1 つ以上のタスクを実行して通知に応答します。</span><span class="sxs-lookup"><span data-stu-id="19f93-105">Responds to a notification by performing one or more tasks.</span></span> <span data-ttu-id="19f93-106">実行されるタスクは、イベントの種類と通知を生成するオブジェクトによって異なります。</span><span class="sxs-lookup"><span data-stu-id="19f93-106">The tasks performed depend on the type of event and the object that generates the notification.</span></span> 
  
```cpp
ULONG OnNotify(
  ULONG cNotif,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a><span data-ttu-id="19f93-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="19f93-107">Parameters</span></span>

 <span data-ttu-id="19f93-108">_cNotif_</span><span class="sxs-lookup"><span data-stu-id="19f93-108">_cNotif_</span></span>
  
> <span data-ttu-id="19f93-109">[in]_lpNotifications_[パラメーターが](notification.md)指す NOTIFICATION 構造体の数。</span><span class="sxs-lookup"><span data-stu-id="19f93-109">[in] The count of [NOTIFICATION](notification.md) structures pointed to by the  _lpNotifications_ parameter.</span></span> 
    
 <span data-ttu-id="19f93-110">_lpNotifications_</span><span class="sxs-lookup"><span data-stu-id="19f93-110">_lpNotifications_</span></span>
  
> <span data-ttu-id="19f93-111">[in]発生したイベントに関する **情報** を提供する 1 つ以上の NOTIFICATION 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="19f93-111">[in] A pointer to one or more **NOTIFICATION** structures that provide information about the events that have occurred.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="19f93-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="19f93-112">Return value</span></span>

<span data-ttu-id="19f93-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="19f93-113">S_OK</span></span> 
  
> <span data-ttu-id="19f93-114">通知が正常に処理されました。</span><span class="sxs-lookup"><span data-stu-id="19f93-114">The notification was processed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="19f93-115">注釈</span><span class="sxs-lookup"><span data-stu-id="19f93-115">Remarks</span></span>

<span data-ttu-id="19f93-116">通知プロセスは、クライアントまたは MAPI がサービス プロバイダーの **Advise** メソッドを呼び出して、特定のオブジェクトの特定の種類の通知を受信するために登録するときに開始されます。</span><span class="sxs-lookup"><span data-stu-id="19f93-116">The notification process starts when a client or MAPI makes a call to a service provider's **Advise** method to register to receive a notification of a particular type for a particular object.</span></span> <span data-ttu-id="19f93-117">Advise メソッドのパラメーターの **1** つは [、IMAPIAdviseSink](imapiadvisesinkiunknown.md) インターフェイスを実装するアアドバイス シンク オブジェクトへのポインターです。</span><span class="sxs-lookup"><span data-stu-id="19f93-117">One of the parameters to the **Advise** method is a pointer to an advise sink object that implements the [IMAPIAdviseSink](imapiadvisesinkiunknown.md) interface.</span></span> <span data-ttu-id="19f93-118">登録された通知に対応するターゲット オブジェクトに対してイベントが発生すると、サービス プロバイダーは MAPI を介して直接または間接的に、アドバイス シンクの **OnNotify** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="19f93-118">When an event occurs to the target object that corresponds to the registered notification, the service provider, either directly or indirectly through MAPI, calls the advise sink's **OnNotify** method.</span></span> 
  
<span data-ttu-id="19f93-119">**OnNotify の呼び出し** は、イベントの原因となっている MAPI 呼び出し中、または後で発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="19f93-119">The call to **OnNotify** can occur either during the MAPI call that is causing the event or at some later time.</span></span> <span data-ttu-id="19f93-120">複数の実行スレッドをサポートするシステムでは、登録に使用された同じスレッドまたは別のスレッドで **OnNotify** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="19f93-120">On systems that support multiple threads of execution, **OnNotify** can be called either on the same thread that was used for registration or on a different thread.</span></span> <span data-ttu-id="19f93-121">クライアントは [、HrThisThreadAdviseSink](hrthisthreadadvisesink.md)関数を使用して Advise に渡すアドバイス シンクを作成して、Advise を呼び出すのと同じスレッドで **OnNotify** 呼び出しが行われることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="19f93-121">Clients can make sure that the **OnNotify** call is made on the same thread used to call **Advise** by creating the advise sink that they pass to **Advise** with the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="19f93-122">_lpNotifications パラメーターは_、イベント中に変更された情報を記述する 1 つ以上の **NOTIFICATION** 構造体をポイントします。</span><span class="sxs-lookup"><span data-stu-id="19f93-122">The  _lpNotifications_ parameter points to one or more **NOTIFICATION** structures that describe what has changed during the event.</span></span> <span data-ttu-id="19f93-123">イベントの種類ごとに異なる **種類** の NOTIFICATION 構造があります。</span><span class="sxs-lookup"><span data-stu-id="19f93-123">There is a different type of **NOTIFICATION** structure for each type of event.</span></span> 
  
<span data-ttu-id="19f93-124">次の表に、可能な種類のイベントを表す値と、各値に関連付けられている構造を示します。</span><span class="sxs-lookup"><span data-stu-id="19f93-124">The following table lists the values that are used to represent the possible types of events and the structures associated with each value:</span></span>
  
|<span data-ttu-id="19f93-125">**通知イベントの種類**</span><span class="sxs-lookup"><span data-stu-id="19f93-125">**Notification event type**</span></span>|<span data-ttu-id="19f93-126">**対応する構造**</span><span class="sxs-lookup"><span data-stu-id="19f93-126">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="19f93-127">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="19f93-127">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="19f93-128">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="19f93-128">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="19f93-129">**fnevNewMail**</span><span class="sxs-lookup"><span data-stu-id="19f93-129">**fnevNewMail**</span></span> <br/> |[<span data-ttu-id="19f93-130">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="19f93-130">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md) <br/> |
|<span data-ttu-id="19f93-131">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="19f93-131">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="19f93-132">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="19f93-132">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="19f93-133">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="19f93-133">**fnevObjectDeleted**</span></span> <br/> |[<span data-ttu-id="19f93-134">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="19f93-134">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="19f93-135">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="19f93-135">**fnevObjectModified**</span></span> <br/> |[<span data-ttu-id="19f93-136">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="19f93-136">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="19f93-137">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="19f93-137">**fnevObjectCopied**</span></span> <br/> |[<span data-ttu-id="19f93-138">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="19f93-138">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="19f93-139">**fnevSearchComplete**</span><span class="sxs-lookup"><span data-stu-id="19f93-139">**fnevSearchComplete**</span></span> <br/> |[<span data-ttu-id="19f93-140">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="19f93-140">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="19f93-141">**fnevTableModified**</span><span class="sxs-lookup"><span data-stu-id="19f93-141">**fnevTableModified**</span></span> <br/> |[<span data-ttu-id="19f93-142">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="19f93-142">TABLE_NOTIFICATION</span></span>](table_notification.md) <br/> |
|<span data-ttu-id="19f93-143">**fnevStatusObjectModified**</span><span class="sxs-lookup"><span data-stu-id="19f93-143">**fnevStatusObjectModified**</span></span> <br/> |[<span data-ttu-id="19f93-144">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="19f93-144">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md) <br/> |
|<span data-ttu-id="19f93-145">**fnevExtended**</span><span class="sxs-lookup"><span data-stu-id="19f93-145">**fnevExtended**</span></span> <br/> |[<span data-ttu-id="19f93-146">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="19f93-146">EXTENDED_NOTIFICATION</span></span>](extended_notification.md) <br/> |
   
<span data-ttu-id="19f93-147">通知を設定および停止する方法の詳細については [、IABLogon、IAddrBook、IMAPIForm、IMAPISession、IMAPITable、IMsgStore、](iablogoniunknown.md)および [](imapiformiunknown.md)[IMSLogon](imslogoniunknown.md)のインターフェイス [](imapisessioniunknown.md)の Advise メソッドと [](imapitableiunknown.md)**Unadvise** メソッドのリファレンス エントリを参照してください。  [](iaddrbookimapiprop.md) [](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="19f93-147">For more information about how to set up and stop notifications, see the reference entries for the **Advise** and **Unadvise** methods for any of the following interfaces: [IABLogon](iablogoniunknown.md), [IAddrBook](iaddrbookimapiprop.md), [IMAPIForm](imapiformiunknown.md), [IMAPISession](imapisessioniunknown.md), [IMAPITable](imapitableiunknown.md), [IMsgStore](imsgstoreimapiprop.md), and [IMSLogon](imslogoniunknown.md).</span></span> 
  
<span data-ttu-id="19f93-148">通知プロセスの一般的な情報については [、「MAPI でのイベント通知」を参照してください](event-notification-in-mapi.md)。</span><span class="sxs-lookup"><span data-stu-id="19f93-148">For general information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="19f93-149">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="19f93-149">Notes to implementers</span></span>

<span data-ttu-id="19f93-150">**OnNotify の実装** は、通常、受信する通知の種類ごとに 1 つ以上のコード ブロックで構成されます。</span><span class="sxs-lookup"><span data-stu-id="19f93-150">Your **OnNotify** implementation will typically consist of one or more blocks of code for each type of notification you expect to receive.</span></span> <span data-ttu-id="19f93-151">これらのコード ブロック内で、通知への応答として必要と考えるタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="19f93-151">Within these blocks of code, perform any tasks that you consider necessary as a response to the notification.</span></span> <span data-ttu-id="19f93-152">たとえば、ダイアログ ボックスの表示に含まれるフォルダーで **fnevObjectModified** 通知を受信するために登録するとします。</span><span class="sxs-lookup"><span data-stu-id="19f93-152">For example, suppose you register to receive **fnevObjectModified** notifications on a folder that is included in a dialog box display.</span></span> <span data-ttu-id="19f93-153">**fnevObjectModified** 通知を処理するために **OnNotify** メソッドに含めるコードブロックで、Windows メッセージをダイアログ ボックスに送信して、更新された表示を要求する場合があります。</span><span class="sxs-lookup"><span data-stu-id="19f93-153">In the block of code that you include in your **OnNotify** method to handle **fnevObjectModified** notifications, you might send a Windows message to the dialog box to request an updated display.</span></span> 
  
<span data-ttu-id="19f93-154">**OnNotify** に渡される **NOTIFICATION** 構造を変更または解放しない。</span><span class="sxs-lookup"><span data-stu-id="19f93-154">Do not modify or free the **NOTIFICATION** structure passed to **OnNotify**.</span></span> <span data-ttu-id="19f93-155">構造体内のデータは **、OnNotify** が返されるまで有効です。</span><span class="sxs-lookup"><span data-stu-id="19f93-155">The data in the structure is valid only until **OnNotify** returns.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="19f93-156">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="19f93-156">Notes to callers</span></span>

<span data-ttu-id="19f93-157">複数のオブジェクトに対して変更が発生した場合は、登録されたアアドバイス シンクに **対して、OnNotify** への 1 回の呼び出し、またはメモリの制約に応じて複数の呼び出しで通知できます。</span><span class="sxs-lookup"><span data-stu-id="19f93-157">When changes occur to multiple objects, you can notify a registered advise sink in a single call to **OnNotify** or in multiple calls depending on memory constraints.</span></span> <span data-ttu-id="19f93-158">これは、変更が 1 つのメソッド呼び出しまたは複数のメソッド呼び出しの結果かどうかに関係なく当てはまる。</span><span class="sxs-lookup"><span data-stu-id="19f93-158">This is true regardless of whether the changes are the result of one method call or several.</span></span> <span data-ttu-id="19f93-159">たとえば [、IMAPIFolder::CopyMessages](imapifolder-copymessages.md) への呼び出しは、複数のメッセージとフォルダーに影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="19f93-159">For example, a call to [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) can affect multiple messages and folders.</span></span> <span data-ttu-id="19f93-160">メッセージ ストア プロバイダーとして、ターゲット フォルダーの **fnevObjectModified** イベントの種類を使用して **OnNotify** を 1 回呼び出したり、メッセージに影響を与えるメッセージごとに 1 回の呼び出しを行います。</span><span class="sxs-lookup"><span data-stu-id="19f93-160">As a message store provider, you can make one call to **OnNotify** with an **fnevObjectModified** event type for the target folder or many calls, one for each affect messages.</span></span> <span data-ttu-id="19f93-161">同様に、クライアントが [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)を繰り返し呼び出す場合、これらの呼び出しは、フォルダーの **1 つの fnevObjectModified** イベントに結合したり、新しいメッセージごとに個別の **fnevObjectCreated** イベントに分割することができます。</span><span class="sxs-lookup"><span data-stu-id="19f93-161">Similarly, if a client makes repeated calls to [IMAPIFolder::CreateMessage](imapifolder-createmessage.md), these calls can be combined into one **fnevObjectModified** event for the folder or separated into individual **fnevObjectCreated** events for each new message.</span></span> 
  
<span data-ttu-id="19f93-162">通知を生成する方法と時間の詳細については [、「MAPI](event-notification-in-mapi.md) でのイベント通知」および「サポート イベント通知」 [を参照してください](supporting-event-notification.md)。</span><span class="sxs-lookup"><span data-stu-id="19f93-162">For more information about how and when to generate notifications, see [Event Notification in MAPI](event-notification-in-mapi.md) and [Supporting Event Notification](supporting-event-notification.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="19f93-163">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="19f93-163">MFCMAPI reference</span></span>

<span data-ttu-id="19f93-164">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="19f93-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="19f93-165">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="19f93-165">**File**</span></span>|<span data-ttu-id="19f93-166">**関数**</span><span class="sxs-lookup"><span data-stu-id="19f93-166">**Function**</span></span>|<span data-ttu-id="19f93-167">**コメント**</span><span class="sxs-lookup"><span data-stu-id="19f93-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="19f93-168">AdviseSink.h と AdviseSink.cpp</span><span class="sxs-lookup"><span data-stu-id="19f93-168">AdviseSink.h and AdviseSink.cpp</span></span>  <br/> |<span data-ttu-id="19f93-169">CAdviseSink::OnNotifyDesc</span><span class="sxs-lookup"><span data-stu-id="19f93-169">CAdviseSink::OnNotifyDesc</span></span>  <br/> |<span data-ttu-id="19f93-170">CAdviseSink クラスは、MFCMAPI のすべての通知を処理するために実装されます。</span><span class="sxs-lookup"><span data-stu-id="19f93-170">The CAdviseSink class is implemented to handle all notifications in MFCMAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="19f93-171">関連項目</span><span class="sxs-lookup"><span data-stu-id="19f93-171">See also</span></span>



[<span data-ttu-id="19f93-172">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="19f93-172">HrAllocAdviseSink</span></span>](hrallocadvisesink.md)
  
[<span data-ttu-id="19f93-173">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="19f93-173">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="19f93-174">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="19f93-174">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
  
[<span data-ttu-id="19f93-175">�ʒm</span><span class="sxs-lookup"><span data-stu-id="19f93-175">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="19f93-176">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="19f93-176">IMAPIAdviseSink : IUnknown</span></span>](imapiadvisesinkiunknown.md)


<span data-ttu-id="19f93-177">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="19f93-177">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

