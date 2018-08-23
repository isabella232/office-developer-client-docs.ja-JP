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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 73eb92b0c1b88e114775231695b91157a3d26a2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800435"
---
# <a name="imapiadvisesinkonnotify"></a><span data-ttu-id="1132c-103">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="1132c-103">IMAPIAdviseSink::OnNotify</span></span>

  
  
<span data-ttu-id="1132c-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1132c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1132c-105">通知に応答するには、1 つまたは複数のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="1132c-105">Responds to a notification by performing one or more tasks.</span></span> <span data-ttu-id="1132c-106">実行するタスクは、イベントおよび通知を生成するオブジェクトの種類によって異なります。</span><span class="sxs-lookup"><span data-stu-id="1132c-106">The tasks performed depend on the type of event and the object that generates the notification.</span></span> 
  
```cpp
ULONG OnNotify(
  ULONG cNotif,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a><span data-ttu-id="1132c-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1132c-107">Parameters</span></span>

 <span data-ttu-id="1132c-108">_cNotif_</span><span class="sxs-lookup"><span data-stu-id="1132c-108">_cNotif_</span></span>
  
> <span data-ttu-id="1132c-109">[in]_LpNotifications_パラメーターで指定された[通知](notification.md)の構造体の数です。</span><span class="sxs-lookup"><span data-stu-id="1132c-109">[in] The count of [NOTIFICATION](notification.md) structures pointed to by the  _lpNotifications_ parameter.</span></span> 
    
 <span data-ttu-id="1132c-110">_lpNotifications_</span><span class="sxs-lookup"><span data-stu-id="1132c-110">_lpNotifications_</span></span>
  
> <span data-ttu-id="1132c-111">[in]発生したイベントに関する情報を提供する 1 つまたは複数の**通知**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1132c-111">[in] A pointer to one or more **NOTIFICATION** structures that provide information about the events that have occurred.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1132c-112">�߂�l</span><span class="sxs-lookup"><span data-stu-id="1132c-112">Return value</span></span>

<span data-ttu-id="1132c-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="1132c-113">S_OK</span></span> 
  
> <span data-ttu-id="1132c-114">通知が正常に処理されました。</span><span class="sxs-lookup"><span data-stu-id="1132c-114">The notification was processed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1132c-115">注釈</span><span class="sxs-lookup"><span data-stu-id="1132c-115">Remarks</span></span>

<span data-ttu-id="1132c-116">クライアントまたは MAPI は、特定のオブジェクトの特定の種類の通知を受け取るに登録するのには**サービス プロバイダーのメソッド**を呼び出しを行うときに、通知の処理が開始されます。</span><span class="sxs-lookup"><span data-stu-id="1132c-116">The notification process starts when a client or MAPI makes a call to a service provider's **Advise** method to register to receive a notification of a particular type for a particular object.</span></span> <span data-ttu-id="1132c-117">**アドバイズ**メソッドにパラメーターの 1 つは、 [IMAPIAdviseSink](imapiadvisesinkiunknown.md)インターフェイスを実装するアドバイズ シンク オブジェクトへのポインターです。</span><span class="sxs-lookup"><span data-stu-id="1132c-117">One of the parameters to the **Advise** method is a pointer to an advise sink object that implements the [IMAPIAdviseSink](imapiadvisesinkiunknown.md) interface.</span></span> <span data-ttu-id="1132c-118">MAPI を介して直接または間接的を登録済みの通知は、サービス プロバイダーに対応するターゲット オブジェクトにイベントが発生したときは、アドバイズ シンクの**OnNotify**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1132c-118">When an event occurs to the target object that corresponds to the registered notification, the service provider, either directly or indirectly through MAPI, calls the advise sink's **OnNotify** method.</span></span> 
  
<span data-ttu-id="1132c-119">**OnNotify**への呼び出しは、イベントの原因となっている MAPI の呼び出し時に、または後でに発生します。</span><span class="sxs-lookup"><span data-stu-id="1132c-119">The call to **OnNotify** can occur either during the MAPI call that is causing the event or at some later time.</span></span> <span data-ttu-id="1132c-120">**システムでは複数の実行スレッドをサポートする、ことがでく onnotify 登録に使用した同じスレッドまたは別のスレッドのいずれかです。**</span><span class="sxs-lookup"><span data-stu-id="1132c-120">On systems that support multiple threads of execution, **OnNotify** can be called either on the same thread that was used for registration or on a different thread.</span></span> <span data-ttu-id="1132c-121">クライアントを**OnNotify**呼び出しが[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)関数を使用して**アドバイズ**に渡すアドバイズ シンクを作成することで**アドバイス**を呼び出すために使用する同じスレッドで作成していることを確認して行うことができます。</span><span class="sxs-lookup"><span data-stu-id="1132c-121">Clients can make sure that the **OnNotify** call is made on the same thread used to call **Advise** by creating the advise sink that they pass to **Advise** with the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="1132c-122">_LpNotifications_パラメーターは、イベント中に変更内容を記述する 1 つまたは複数の**通知**構造体を指します。</span><span class="sxs-lookup"><span data-stu-id="1132c-122">The  _lpNotifications_ parameter points to one or more **NOTIFICATION** structures that describe what has changed during the event.</span></span> <span data-ttu-id="1132c-123">イベントの種類ごとに**通知**の構造体のさまざまな種類があります。</span><span class="sxs-lookup"><span data-stu-id="1132c-123">There is a different type of **NOTIFICATION** structure for each type of event.</span></span> 
  
<span data-ttu-id="1132c-124">イベントとそれぞれの値に関連付けられている構造体の種類を表すために使用される値を次の表に一覧します。</span><span class="sxs-lookup"><span data-stu-id="1132c-124">The following table lists the values that are used to represent the possible types of events and the structures associated with each value:</span></span>
  
|<span data-ttu-id="1132c-125">**通知イベントの種類**</span><span class="sxs-lookup"><span data-stu-id="1132c-125">**Notification event type**</span></span>|<span data-ttu-id="1132c-126">**対応する構造体**</span><span class="sxs-lookup"><span data-stu-id="1132c-126">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1132c-127">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="1132c-127">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="1132c-128">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="1132c-128">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="1132c-129">**fnevNewMail**</span><span class="sxs-lookup"><span data-stu-id="1132c-129">**fnevNewMail**</span></span> <br/> |[<span data-ttu-id="1132c-130">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="1132c-130">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md) <br/> |
|<span data-ttu-id="1132c-131">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="1132c-131">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="1132c-132">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="1132c-132">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="1132c-133">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="1132c-133">**fnevObjectDeleted**</span></span> <br/> |[<span data-ttu-id="1132c-134">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="1132c-134">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="1132c-135">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="1132c-135">**fnevObjectModified**</span></span> <br/> |[<span data-ttu-id="1132c-136">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="1132c-136">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="1132c-137">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="1132c-137">**fnevObjectCopied**</span></span> <br/> |[<span data-ttu-id="1132c-138">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="1132c-138">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="1132c-139">**fnevSearchComplete**</span><span class="sxs-lookup"><span data-stu-id="1132c-139">**fnevSearchComplete**</span></span> <br/> |[<span data-ttu-id="1132c-140">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="1132c-140">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="1132c-141">**fnevTableModified**</span><span class="sxs-lookup"><span data-stu-id="1132c-141">**fnevTableModified**</span></span> <br/> |[<span data-ttu-id="1132c-142">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="1132c-142">TABLE_NOTIFICATION</span></span>](table_notification.md) <br/> |
|<span data-ttu-id="1132c-143">**fnevStatusObjectModified**</span><span class="sxs-lookup"><span data-stu-id="1132c-143">**fnevStatusObjectModified**</span></span> <br/> |[<span data-ttu-id="1132c-144">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="1132c-144">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md) <br/> |
|<span data-ttu-id="1132c-145">**fnevExtended**</span><span class="sxs-lookup"><span data-stu-id="1132c-145">**fnevExtended**</span></span> <br/> |[<span data-ttu-id="1132c-146">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="1132c-146">EXTENDED_NOTIFICATION</span></span>](extended_notification.md) <br/> |
   
<span data-ttu-id="1132c-147">設定し、通知を停止する方法の詳細については、次のインターフェイスのいずれかの**アドバイス**と**Unadvise**のメソッドの参照のエントリを参照してください: [IABLogon](iablogoniunknown.md)、 [IAddrBook](iaddrbookimapiprop.md)、 [IMAPIForm](imapiformiunknown.md)、 [IMAPISession](imapisessioniunknown.md)、 [IMAPITable](imapitableiunknown.md)、 [IMsgStore](imsgstoreimapiprop.md)、および[IMSLogon](imslogoniunknown.md)。</span><span class="sxs-lookup"><span data-stu-id="1132c-147">For more information about how to set up and stop notifications, see the reference entries for the **Advise** and **Unadvise** methods for any of the following interfaces: [IABLogon](iablogoniunknown.md), [IAddrBook](iaddrbookimapiprop.md), [IMAPIForm](imapiformiunknown.md), [IMAPISession](imapisessioniunknown.md), [IMAPITable](imapitableiunknown.md), [IMsgStore](imsgstoreimapiprop.md), and [IMSLogon](imslogoniunknown.md).</span></span> 
  
<span data-ttu-id="1132c-148">通知プロセスの詳細については、 [MAPI でのイベントの通知](event-notification-in-mapi.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1132c-148">For general information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="1132c-149">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="1132c-149">Notes to implementers</span></span>

<span data-ttu-id="1132c-150">**OnNotify**実装は、受信する通知の種類ごとにコードのブロックを 1 つまたは複数の通常から構成されます。</span><span class="sxs-lookup"><span data-stu-id="1132c-150">Your **OnNotify** implementation will typically consist of one or more blocks of code for each type of notification you expect to receive.</span></span> <span data-ttu-id="1132c-151">これらのコードのブロック内には、通知への応答として必要と思われるすべてのタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="1132c-151">Within these blocks of code, perform any tasks that you consider necessary as a response to the notification.</span></span> <span data-ttu-id="1132c-152">たとえば、ダイアログ ボックスの表示に含まれているフォルダーに、 **fnevObjectModified**通知を受信する登録するとします。</span><span class="sxs-lookup"><span data-stu-id="1132c-152">For example, suppose you register to receive **fnevObjectModified** notifications on a folder that is included in a dialog box display.</span></span> <span data-ttu-id="1132c-153">**OnNotify** **fnevObjectModified**通知を処理するメソッドに追加することをコードのブロック内には、更新の表示を要求するダイアログ ボックスに Windows メッセージを送信する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="1132c-153">In the block of code that you include in your **OnNotify** method to handle **fnevObjectModified** notifications, you might send a Windows message to the dialog box to request an updated display.</span></span> 
  
<span data-ttu-id="1132c-154">変更したり、 **OnNotify**に渡された**通知**の構造体を解放しないでください。</span><span class="sxs-lookup"><span data-stu-id="1132c-154">Do not modify or free the **NOTIFICATION** structure passed to **OnNotify**.</span></span> <span data-ttu-id="1132c-155">構造内のデータは、 **OnNotify**を返すまでの間だけ有効です。</span><span class="sxs-lookup"><span data-stu-id="1132c-155">The data in the structure is valid only until **OnNotify** returns.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1132c-156">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="1132c-156">Notes to callers</span></span>

<span data-ttu-id="1132c-157">複数のオブジェクトに変更が発生すると、 **OnNotify**を単一の呼び出しまたはメモリの制約によって、複数の呼び出しでは、登録されているアドバイズ シンクを通知できます。</span><span class="sxs-lookup"><span data-stu-id="1132c-157">When changes occur to multiple objects, you can notify a registered advise sink in a single call to **OnNotify** or in multiple calls depending on memory constraints.</span></span> <span data-ttu-id="1132c-158">かどうかにかかわらず、変更のいくつかの 1 つのメソッド呼び出しの結果です。</span><span class="sxs-lookup"><span data-stu-id="1132c-158">This is true regardless of whether the changes are the result of one method call or several.</span></span> <span data-ttu-id="1132c-159">たとえば、複数のメッセージおよびフォルダー [IMAPIFolder::CopyMessages](imapifolder-copymessages.md)の呼び出しに影響します。</span><span class="sxs-lookup"><span data-stu-id="1132c-159">For example, a call to [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) can affect multiple messages and folders.</span></span> <span data-ttu-id="1132c-160">メッセージ ストア プロバイダーでは、対象となるフォルダーまたは多数の呼び出しがあり、それぞれに影響を与えるメッセージのいずれかに、 **fnevObjectModified**イベントの種類の**OnNotify**を 1 つの呼び出しを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="1132c-160">As a message store provider, you can make one call to **OnNotify** with an **fnevObjectModified** event type for the target folder or many calls, one for each affect messages.</span></span> <span data-ttu-id="1132c-161">同様に、クライアント[IMAPIFolder::CreateMessage](imapifolder-createmessage.md)を繰り返し呼び出す場合は、これらの呼び出しするフォルダーの 1 つの**fnevObjectModified**イベントに結合したり、新しいメッセージごとに個別の**fnevObjectCreated**イベントに分割できます。</span><span class="sxs-lookup"><span data-stu-id="1132c-161">Similarly, if a client makes repeated calls to [IMAPIFolder::CreateMessage](imapifolder-createmessage.md), these calls can be combined into one **fnevObjectModified** event for the folder or separated into individual **fnevObjectCreated** events for each new message.</span></span> 
  
<span data-ttu-id="1132c-162">方法の詳細については、通知を生成する場合に、 [MAPI でのイベント通知](event-notification-in-mapi.md)[イベント通知のサポート](supporting-event-notification.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1132c-162">For more information about how and when to generate notifications, see [Event Notification in MAPI](event-notification-in-mapi.md) and [Supporting Event Notification](supporting-event-notification.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1132c-163">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="1132c-163">MFCMAPI reference</span></span>

<span data-ttu-id="1132c-164">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="1132c-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1132c-165">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="1132c-165">**File**</span></span>|<span data-ttu-id="1132c-166">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="1132c-166">**Function**</span></span>|<span data-ttu-id="1132c-167">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="1132c-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1132c-168">AdviseSink.h と AdviseSink.cpp</span><span class="sxs-lookup"><span data-stu-id="1132c-168">AdviseSink.h and AdviseSink.cpp</span></span>  <br/> |<span data-ttu-id="1132c-169">CAdviseSink::OnNotifyDesc</span><span class="sxs-lookup"><span data-stu-id="1132c-169">CAdviseSink::OnNotifyDesc</span></span>  <br/> |<span data-ttu-id="1132c-170">MFCMAPI ですべての通知を処理するためには、CAdviseSink クラスが実装されます。</span><span class="sxs-lookup"><span data-stu-id="1132c-170">The CAdviseSink class is implemented to handle all notifications in MFCMAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1132c-171">関連項目</span><span class="sxs-lookup"><span data-stu-id="1132c-171">See also</span></span>



[<span data-ttu-id="1132c-172">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="1132c-172">HrAllocAdviseSink</span></span>](hrallocadvisesink.md)
  
[<span data-ttu-id="1132c-173">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="1132c-173">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="1132c-174">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="1132c-174">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
  
[<span data-ttu-id="1132c-175">�ʒm</span><span class="sxs-lookup"><span data-stu-id="1132c-175">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="1132c-176">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1132c-176">IMAPIAdviseSink : IUnknown</span></span>](imapiadvisesinkiunknown.md)


<span data-ttu-id="1132c-177">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="1132c-177">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

