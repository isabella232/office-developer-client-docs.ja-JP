---
title: IMAPISupportSpoolerNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.SpoolerNotify
api_type:
- COM
ms.assetid: d4f153b2-939f-4153-85fb-dc510193848c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 99377d63b4b5cf8731809446b70770f0c24231ed
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423770"
---
# <a name="imapisupportspoolernotify"></a><span data-ttu-id="25eeb-103">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="25eeb-103">IMAPISupport::SpoolerNotify</span></span>

  
  
<span data-ttu-id="25eeb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="25eeb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="25eeb-105">状態の変更またはサービスの要求の MAPI スプーラーに通知します。</span><span class="sxs-lookup"><span data-stu-id="25eeb-105">Notifies the MAPI spooler of a change in status or a request for service.</span></span> 
  
```cpp
HRESULT SpoolerNotify(
ULONG ulFlags,
LPVOID lpvData
);
```

## <a name="parameters"></a><span data-ttu-id="25eeb-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="25eeb-106">Parameters</span></span>

 <span data-ttu-id="25eeb-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="25eeb-107">_ulFlags_</span></span>
  
> <span data-ttu-id="25eeb-108">順番通知の種類を示すフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="25eeb-108">[in] A bitmask of flags that indicates the type of notification.</span></span> <span data-ttu-id="25eeb-109">トランスポートプロバイダーは、NOTIFY_NEWMAIL_RECEIVED 以外のすべてのフラグを設定できます。NOTIFY_NEWMAIL_RECEIVED と NOTIFY_READTOSEND のみが、メッセージストアプロバイダーに対して有効です。</span><span class="sxs-lookup"><span data-stu-id="25eeb-109">Transport providers can set all of the flags except for NOTIFY_NEWMAIL_RECEIVED; only NOTIFY_NEWMAIL_RECEIVED and NOTIFY_READTOSEND are valid for message store providers.</span></span> <span data-ttu-id="25eeb-110">_ulflags_パラメーターには、次のフラグが有効です。</span><span class="sxs-lookup"><span data-stu-id="25eeb-110">The following flags are valid for the  _ulFlags_ parameter:</span></span> 
    
<span data-ttu-id="25eeb-111">NOTIFY_CONFIG_CHANGE</span><span class="sxs-lookup"><span data-stu-id="25eeb-111">NOTIFY_CONFIG_CHANGE</span></span> 
  
> <span data-ttu-id="25eeb-112">トランスポートプロバイダーの構成を変更するための要求を登録します。</span><span class="sxs-lookup"><span data-stu-id="25eeb-112">Registers a request to change the transport provider's configuration.</span></span> 
    
<span data-ttu-id="25eeb-113">NOTIFY_CRITICAL_ERROR</span><span class="sxs-lookup"><span data-stu-id="25eeb-113">NOTIFY_CRITICAL_ERROR</span></span> 
  
> <span data-ttu-id="25eeb-114">トランスポートプロバイダーへの回復不能なエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="25eeb-114">An unrecoverable error has occurred to the transport provider.</span></span> <span data-ttu-id="25eeb-115">NOTIFY_SENTDEFERRED と NOTIFY_CRITICAL_ERROR の両方がトランスポートプロバイダー呼び出しに_lpvdata_パラメーターを使用するため、これらのフラグは相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="25eeb-115">Because both NOTIFY_SENTDEFERRED and NOTIFY_CRITICAL_ERROR use the  _lpvData_ parameter for transport provider calls, these flags are mutually exclusive.</span></span> 
    
<span data-ttu-id="25eeb-116">NOTIFY_CRITSEC</span><span class="sxs-lookup"><span data-stu-id="25eeb-116">NOTIFY_CRITSEC</span></span> 
  
> <span data-ttu-id="25eeb-117">トランスポートプロバイダーの重要なセクションを要求します。</span><span class="sxs-lookup"><span data-stu-id="25eeb-117">Requests a critical section for the transport provider.</span></span> <span data-ttu-id="25eeb-118">_lpvdata_パラメーターは未定義で、NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="25eeb-118">The  _lpvData_ parameter is undefined and should be NULL.</span></span> 
    
<span data-ttu-id="25eeb-119">NOTIFY_NEWMAIL</span><span class="sxs-lookup"><span data-stu-id="25eeb-119">NOTIFY_NEWMAIL</span></span> 
  
> <span data-ttu-id="25eeb-120">MAPI スプーラーは、新しく受信したメッセージを次回の利用可能な時間にダウンロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="25eeb-120">The MAPI spooler should download any newly received messages at the next available time.</span></span> <span data-ttu-id="25eeb-121">_lpvdata_パラメーターは未定義で、NULL に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="25eeb-121">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="25eeb-122">NOTIFY_NEWMAIL_RECEIVED</span><span class="sxs-lookup"><span data-stu-id="25eeb-122">NOTIFY_NEWMAIL_RECEIVED</span></span> 
  
> <span data-ttu-id="25eeb-123">メッセージストアで新しいメッセージを受信しました。</span><span class="sxs-lookup"><span data-stu-id="25eeb-123">A new message has been received in the message store.</span></span> <span data-ttu-id="25eeb-124">_lpvdata_パラメーターは、メッセージを記述する[NEWMAIL_NOTIFICATION](newmail_notification.md)構造体を指します。</span><span class="sxs-lookup"><span data-stu-id="25eeb-124">The  _lpvData_ parameter points to a [NEWMAIL_NOTIFICATION](newmail_notification.md) structure that describes the message.</span></span> <span data-ttu-id="25eeb-125">このフラグは、トランスポートプロバイダーと密に結合しているメッセージストアプロバイダーに使用され、ストアプロバイダーが MAPI_NO_MAIL フラグセットを使用してログオンしている場合は無視されます。</span><span class="sxs-lookup"><span data-stu-id="25eeb-125">This flag is used for message store providers that are tightly coupled with transport providers and is ignored if the store provider is logged on with the MAPI_NO_MAIL flag set.</span></span> 
    
<span data-ttu-id="25eeb-126">NOTIFY_NONCRIT</span><span class="sxs-lookup"><span data-stu-id="25eeb-126">NOTIFY_NONCRIT</span></span> 
  
> <span data-ttu-id="25eeb-127">_ulflags_が NOTIFY_CRITSEC に設定されている**SpoolerNotify**の以前の呼び出しで取得された重要なセクションを解放します。</span><span class="sxs-lookup"><span data-stu-id="25eeb-127">Releases a critical section that was obtained with a previous call to **SpoolerNotify** with  _ulFlags_ set to NOTIFY_CRITSEC.</span></span> <span data-ttu-id="25eeb-128">_lpvdata_パラメーターは未定義で、NULL に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="25eeb-128">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="25eeb-129">NOTIFY_READYTOSEND</span><span class="sxs-lookup"><span data-stu-id="25eeb-129">NOTIFY_READYTOSEND</span></span> 
  
> <span data-ttu-id="25eeb-130">トランスポートまたはメッセージストアプロバイダーがメッセージを送信する準備ができました。</span><span class="sxs-lookup"><span data-stu-id="25eeb-130">The transport or message store provider is ready to send messages.</span></span> <span data-ttu-id="25eeb-131">_lpvdata_パラメーターは未定義で、NULL に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="25eeb-131">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="25eeb-132">NOTIFY_SENTDEFERRED</span><span class="sxs-lookup"><span data-stu-id="25eeb-132">NOTIFY_SENTDEFERRED</span></span> 
  
> <span data-ttu-id="25eeb-133">これで、以前に遅延したメッセージが送信され、 [IXPLogon:: submitmessage](ixplogon-submitmessage.md)メソッドの呼び出しを使用して、メッセージが配信できる状態になったときにトランスポートプロバイダーに通知されるようになります。</span><span class="sxs-lookup"><span data-stu-id="25eeb-133">A previously deferred message should now be sent, and the transport provider should be notified when the message is ready to be delivered by using a call to the [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) method.</span></span> <span data-ttu-id="25eeb-134">遅延したメッセージのエントリ識別子は、 _lpvdata_が指す[sbinary](sbinary.md)構造に含まれています。</span><span class="sxs-lookup"><span data-stu-id="25eeb-134">The entry identifier of the deferred message is contained in an [SBinary](sbinary.md) structure pointed to by  _lpvData_.</span></span> <span data-ttu-id="25eeb-135">NOTIFY_SENTDEFERRED と NOTIFY_CRITICAL_ERROR の両方が_lpvdata_パラメーターを使用するため、これらのフラグは相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="25eeb-135">Because both NOTIFY_SENTDEFERRED and NOTIFY_CRITICAL_ERROR use the  _lpvData_ parameter, these flags are mutually exclusive.</span></span> 
    
 <span data-ttu-id="25eeb-136">_lpvdata_</span><span class="sxs-lookup"><span data-stu-id="25eeb-136">_lpvData_</span></span>
  
> <span data-ttu-id="25eeb-137">順番通知に適用される関連データへのポインター。</span><span class="sxs-lookup"><span data-stu-id="25eeb-137">[in] A pointer to associated data applicable to a notification.</span></span> <span data-ttu-id="25eeb-138">_lpvdata_パラメーターは、次のフラグが設定されている場合にのみ有効なデータをポイントします ( _ulflags_が他の通知タイプに設定されている場合は_lpvdata_が NULL になります)。</span><span class="sxs-lookup"><span data-stu-id="25eeb-138">The  _lpvData_ parameter points to valid data only when the following flags are set (_lpvData_ is NULL when  _ulFlags_ is set to the other notification types):</span></span> 
    
|<span data-ttu-id="25eeb-139">**_ulflags_設定**</span><span class="sxs-lookup"><span data-stu-id="25eeb-139">**_ulFlags_ setting**</span></span>|<span data-ttu-id="25eeb-140">**_lpvdata_値**</span><span class="sxs-lookup"><span data-stu-id="25eeb-140">**_lpvData_ value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="25eeb-141">NOTIFY_CRITICAL_ERROR</span><span class="sxs-lookup"><span data-stu-id="25eeb-141">NOTIFY_CRITICAL_ERROR</span></span>  <br/> |<span data-ttu-id="25eeb-142">エラーに関する情報。</span><span class="sxs-lookup"><span data-stu-id="25eeb-142">Information about the error.</span></span>  <br/> |
|<span data-ttu-id="25eeb-143">NOTIFY_NEWMAIL_RECEIVED</span><span class="sxs-lookup"><span data-stu-id="25eeb-143">NOTIFY_NEWMAIL_RECEIVED</span></span>  <br/> |<span data-ttu-id="25eeb-144">新しく配信されたメッセージに関する情報を含む**NEWMAIL_NOTIFICATION**構造体。</span><span class="sxs-lookup"><span data-stu-id="25eeb-144">A **NEWMAIL_NOTIFICATION** structure that contains information about the newly delivered message.</span></span>  <br/> |
|<span data-ttu-id="25eeb-145">NOTIFY_SENTDEFERRED</span><span class="sxs-lookup"><span data-stu-id="25eeb-145">NOTIFY_SENTDEFERRED</span></span>  <br/> |<span data-ttu-id="25eeb-146">延期されたメッセージのエントリ識別子を含む**sbinary**構造。</span><span class="sxs-lookup"><span data-stu-id="25eeb-146">An **SBinary** structure that contains the entry identifier of deferred message.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="25eeb-147">戻り値</span><span class="sxs-lookup"><span data-stu-id="25eeb-147">Return value</span></span>

<span data-ttu-id="25eeb-148">S_OK</span><span class="sxs-lookup"><span data-stu-id="25eeb-148">S_OK</span></span> 
  
> <span data-ttu-id="25eeb-149">通知は正常に実行されました。</span><span class="sxs-lookup"><span data-stu-id="25eeb-149">The notification was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="25eeb-150">注釈</span><span class="sxs-lookup"><span data-stu-id="25eeb-150">Remarks</span></span>

<span data-ttu-id="25eeb-151">**imapisupport:: SpoolerNotify**メソッドは、メッセージストアとトランスポートプロバイダーのサポートオブジェクトに実装されています。</span><span class="sxs-lookup"><span data-stu-id="25eeb-151">The **IMAPISupport::SpoolerNotify** method is implemented for message store and transport provider support objects.</span></span> <span data-ttu-id="25eeb-152">これらのプロバイダーは**SpoolerNotify**を呼び出して、状態が変化した場合またはサービスの要求を行った場合に、MAPI スプーラーに通知します。</span><span class="sxs-lookup"><span data-stu-id="25eeb-152">These providers call **SpoolerNotify** to notify the MAPI spooler of a change in status or a request for service.</span></span> <span data-ttu-id="25eeb-153">**SpoolerNotify**は、主にトランスポートプロバイダーによって呼び出され、セッション中にいつでも呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="25eeb-153">**SpoolerNotify** is called primarily by transport providers and may be called at any time during the session.</span></span> 
  
## <a name="notes-to-transport-providers"></a><span data-ttu-id="25eeb-154">トランスポートプロバイダーへのメモ</span><span class="sxs-lookup"><span data-stu-id="25eeb-154">Notes to Transport Providers</span></span>

<span data-ttu-id="25eeb-155">トランスポートプロバイダーの構成を変更した場合は、 **SpoolerNotify**を呼び出し、 _ulflags_を NOTIFY_CONFIG_CHANGED に設定します。</span><span class="sxs-lookup"><span data-stu-id="25eeb-155">If you have changed your transport provider configuration, call **SpoolerNotify** and set  _ulFlags_ to NOTIFY_CONFIG_CHANGED.</span></span> <span data-ttu-id="25eeb-156">**SpoolerNotify**は、 [IXPLogon:: AddressTypes](ixplogon-addresstypes.md)メソッドを呼び出して、サポートされているアドレスの種類の変更を照会することによって応答します。</span><span class="sxs-lookup"><span data-stu-id="25eeb-156">**SpoolerNotify** responds by calling the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method to query for a change in supported address types.</span></span> 
  
<span data-ttu-id="25eeb-157">処理が中断されないようにするために重要なセクションが必要な場合は、 _ulflags_が NOTIFY_CRITSEC に設定されている**SpoolerNotify**を呼び出してください。</span><span class="sxs-lookup"><span data-stu-id="25eeb-157">If you need a critical section to ensure uninterrupted processing, call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_CRITSEC.</span></span> <span data-ttu-id="25eeb-158">このフラグを設定すると、 [IXPLogon:: Idle](ixplogon-idle.md)および[IXPLogon::P oll](ixplogon-poll.md)メソッドを呼び出さないように MAPI スプーラーに通知されます。</span><span class="sxs-lookup"><span data-stu-id="25eeb-158">Setting this flag informs the MAPI spooler that it should not call the [IXPLogon::Idle](ixplogon-idle.md) and [IXPLogon::Poll](ixplogon-poll.md) methods.</span></span> <span data-ttu-id="25eeb-159">重要なセクションが開いている間は、 [imapistatus:: validatestate](imapistatus-validatestate.md)メソッドが呼び出されるたびに MAPI_E_BUSY を返します。</span><span class="sxs-lookup"><span data-stu-id="25eeb-159">While you have a critical section open, return MAPI_E_BUSY whenever the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method is called.</span></span> <span data-ttu-id="25eeb-160">クリティカルセクションの作業が終了したら、 _ulflags_が NOTIFY_NONCRIT に設定されている**SpoolerNotify**をもう一度呼び出してください。</span><span class="sxs-lookup"><span data-stu-id="25eeb-160">When you are finished with the critical section, make another call to **SpoolerNotify** with  _ulFlags_ set to NOTIFY_NONCRIT.</span></span> 
  
<span data-ttu-id="25eeb-161">たとえば、リモートトランスポートプロバイダーがメッセージのアップロードプロセス中の場合は、ユーザーが電話番号を入力してリモート接続を確立できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="25eeb-161">For example, if your remote transport provider is in the process of uploading messages, you might need to allow a user to enter a telephone number to establish the remote connection.</span></span> <span data-ttu-id="25eeb-162">ダイアログボックスプロシージャをループ処理する前に、クリティカルセクションを宣言する必要があります。</span><span class="sxs-lookup"><span data-stu-id="25eeb-162">Before you loop through the dialog box procedure, you should declare a critical section.</span></span> <span data-ttu-id="25eeb-163">ユーザーがダイアログボックスを閉じ、ダイアログボックスのプロシージャを終了すると、クリティカルセクションを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="25eeb-163">When the user closes the dialog box, terminating the dialog box procedure, you should release the critical section.</span></span>
  
<span data-ttu-id="25eeb-164">_ulflags_を NOTIFY_CRITICAL_ERROR に設定すると、MAPI スプーラーは、プロバイダーを解放する以外の呼び出しを行いません。</span><span class="sxs-lookup"><span data-stu-id="25eeb-164">When you set  _ulFlags_ to NOTIFY_CRITICAL_ERROR, the MAPI spooler makes no further calls to the provider except to release it.</span></span> <span data-ttu-id="25eeb-165">[IXPLogon:: startmessage](ixplogon-startmessage.md)メソッドまたは[IXPLogon:: submitmessage](ixplogon-submitmessage.md)メソッドから NOTIFY_CRITICAL_ERROR set を使用して**SpoolerNotify**を呼び出す場合は、 **startmessage**または \* \* submitmessage \* \* 呼び出しからの適切なエラー値を返します。**SpoolerNotify**呼び出しの直後。</span><span class="sxs-lookup"><span data-stu-id="25eeb-165">If you call **SpoolerNotify** with NOTIFY_CRITICAL_ERROR set from the [IXPLogon::StartMessage](ixplogon-startmessage.md) or [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) methods, return with an appropriate error value from the **StartMessage** or \*\* SubmitMessage \*\* call immediately after the **SpoolerNotify** call.</span></span> 
  
<span data-ttu-id="25eeb-166">トランスポートプロバイダーが以前に失敗した状態から回復した場合は、NOTIFY_READYTOSEND に設定された_ulflags_を使用して**SpoolerNotify**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="25eeb-166">If your transport provider recovered from a condition that previously caused it to fail, call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_READYTOSEND.</span></span> <span data-ttu-id="25eeb-167">このフラグは、プロバイダーが再度メッセージを処理できる状態になっていることを示します。</span><span class="sxs-lookup"><span data-stu-id="25eeb-167">This flag indicates that the provider is again ready to handle messages.</span></span> 
  
## <a name="notes-to-message-store-providers"></a><span data-ttu-id="25eeb-168">メッセージストアプロバイダーへの注意事項</span><span class="sxs-lookup"><span data-stu-id="25eeb-168">Notes to Message Store Providers</span></span>

<span data-ttu-id="25eeb-169">imapisupport への最初の呼び出しを行う前に、 **SpoolerNotify**を呼び出して NOTIFY_READYTOSEND フラグを_ulflags_に渡します。次に、 **IMessage:: submitmessage**で[repare:P](imapisupport-preparesubmit.md)します。</span><span class="sxs-lookup"><span data-stu-id="25eeb-169">Call **SpoolerNotify**, passing the NOTIFY_READYTOSEND flag in  _ulFlags_, before you make your first call to [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) in **IMessage::SubmitMessage**.</span></span> <span data-ttu-id="25eeb-170">この**SpoolerNotify**への呼び出しは、セッションごとに1回だけ行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="25eeb-170">This call to **SpoolerNotify** needs to be made only once per session.</span></span> 
  
<span data-ttu-id="25eeb-171">メッセージストアプロバイダーがトランスポートプロバイダーと密に結合していて、 _ulflags_が NOTIFY_NEWMAIL_RECEIVED に設定されている**SpoolerNotify**を呼び出す場合、MAPI スプーラーは新しいメッセージを開き、新しいメッセージフック関数の処理を開始します。</span><span class="sxs-lookup"><span data-stu-id="25eeb-171">If your message store provider is tightly coupled with a transport provider and you call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_NEWMAIL_RECEIVED, the MAPI spooler opens the new message and begins processing the new message hook function.</span></span> <span data-ttu-id="25eeb-172">処理が完了すると、MAPI スプーラーは[IMsgStore:: NotifyNewMail](imsgstore-notifynewmail.md)メソッドを呼び出して、自分の新しいメッセージを通知します。</span><span class="sxs-lookup"><span data-stu-id="25eeb-172">When processing is complete, the MAPI spooler calls the [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method to inform you of your own new message.</span></span> 
  
<span data-ttu-id="25eeb-173">**SpoolerNotify**の呼び出しの詳細については、次のいずれかのトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="25eeb-173">For more information about calling **SpoolerNotify**, see any of the following topics:</span></span>
  
- [<span data-ttu-id="25eeb-174">flushqueues メソッドの実装</span><span class="sxs-lookup"><span data-stu-id="25eeb-174">Implementing the FlushQueues Method</span></span>](implementing-the-flushqueues-method.md)
    
- [<span data-ttu-id="25eeb-175">MAPI スプーラーとの対話</span><span class="sxs-lookup"><span data-stu-id="25eeb-175">Interacting with the MAPI Spooler</span></span>](interacting-with-the-mapi-spooler.md)
    
- [<span data-ttu-id="25eeb-176">メッセージ受信モデル</span><span class="sxs-lookup"><span data-stu-id="25eeb-176">Message Reception Model</span></span>](message-reception-model.md)
    
## <a name="see-also"></a><span data-ttu-id="25eeb-177">関連項目</span><span class="sxs-lookup"><span data-stu-id="25eeb-177">See also</span></span>



[<span data-ttu-id="25eeb-178">IMsgStore::NotifyNewMail</span><span class="sxs-lookup"><span data-stu-id="25eeb-178">IMsgStore::NotifyNewMail</span></span>](imsgstore-notifynewmail.md)
  
[<span data-ttu-id="25eeb-179">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="25eeb-179">IXPLogon::StartMessage</span></span>](ixplogon-startmessage.md)
  
[<span data-ttu-id="25eeb-180">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="25eeb-180">IXPLogon::SubmitMessage</span></span>](ixplogon-submitmessage.md)
  
[<span data-ttu-id="25eeb-181">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="25eeb-181">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

