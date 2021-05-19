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
# <a name="imapisupportspoolernotify"></a><span data-ttu-id="c8172-103">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="c8172-103">IMAPISupport::SpoolerNotify</span></span>

  
  
<span data-ttu-id="c8172-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8172-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8172-105">状態の変更またはサービスの要求を MAPI スプーラーに通知します。</span><span class="sxs-lookup"><span data-stu-id="c8172-105">Notifies the MAPI spooler of a change in status or a request for service.</span></span> 
  
```cpp
HRESULT SpoolerNotify(
ULONG ulFlags,
LPVOID lpvData
);
```

## <a name="parameters"></a><span data-ttu-id="c8172-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c8172-106">Parameters</span></span>

 <span data-ttu-id="c8172-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c8172-107">_ulFlags_</span></span>
  
> <span data-ttu-id="c8172-108">[in]通知の種類を示すフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="c8172-108">[in] A bitmask of flags that indicates the type of notification.</span></span> <span data-ttu-id="c8172-109">トランスポート プロバイダーは、すべてのフラグを設定できます 。ただし、NOTIFY_NEWMAIL_RECEIVED。メッセージ NOTIFY_NEWMAIL_RECEIVEDプロバイダー NOTIFY_READTOSEND有効なメッセージ ストア プロバイダーおよびメッセージ ストア プロバイダーのみです。</span><span class="sxs-lookup"><span data-stu-id="c8172-109">Transport providers can set all of the flags except for NOTIFY_NEWMAIL_RECEIVED; only NOTIFY_NEWMAIL_RECEIVED and NOTIFY_READTOSEND are valid for message store providers.</span></span> <span data-ttu-id="c8172-110">ulFlags パラメーターには、次の  _フラグが有効_ です。</span><span class="sxs-lookup"><span data-stu-id="c8172-110">The following flags are valid for the  _ulFlags_ parameter:</span></span> 
    
<span data-ttu-id="c8172-111">NOTIFY_CONFIG_CHANGE</span><span class="sxs-lookup"><span data-stu-id="c8172-111">NOTIFY_CONFIG_CHANGE</span></span> 
  
> <span data-ttu-id="c8172-112">トランスポート プロバイダーの構成を変更する要求を登録します。</span><span class="sxs-lookup"><span data-stu-id="c8172-112">Registers a request to change the transport provider's configuration.</span></span> 
    
<span data-ttu-id="c8172-113">NOTIFY_CRITICAL_ERROR</span><span class="sxs-lookup"><span data-stu-id="c8172-113">NOTIFY_CRITICAL_ERROR</span></span> 
  
> <span data-ttu-id="c8172-114">トランスポート プロバイダーに回復不能なエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="c8172-114">An unrecoverable error has occurred to the transport provider.</span></span> <span data-ttu-id="c8172-115">トランスポート プロバイダー呼びNOTIFY_SENTDEFERREDとNOTIFY_CRITICAL_ERROR  _lpvData_ パラメーターの両方が使用される場合、これらのフラグは相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="c8172-115">Because both NOTIFY_SENTDEFERRED and NOTIFY_CRITICAL_ERROR use the  _lpvData_ parameter for transport provider calls, these flags are mutually exclusive.</span></span> 
    
<span data-ttu-id="c8172-116">NOTIFY_CRITSEC</span><span class="sxs-lookup"><span data-stu-id="c8172-116">NOTIFY_CRITSEC</span></span> 
  
> <span data-ttu-id="c8172-117">トランスポート プロバイダーの重要なセクションを要求します。</span><span class="sxs-lookup"><span data-stu-id="c8172-117">Requests a critical section for the transport provider.</span></span> <span data-ttu-id="c8172-118">_lpvData パラメーターは_ 未定義であり、NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8172-118">The  _lpvData_ parameter is undefined and should be NULL.</span></span> 
    
<span data-ttu-id="c8172-119">NOTIFY_NEWMAIL</span><span class="sxs-lookup"><span data-stu-id="c8172-119">NOTIFY_NEWMAIL</span></span> 
  
> <span data-ttu-id="c8172-120">MAPI スプーラーは、次の利用可能な時刻に新しく受信したメッセージをダウンロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8172-120">The MAPI spooler should download any newly received messages at the next available time.</span></span> <span data-ttu-id="c8172-121">_lpvData パラメーターは_ 未定義であり、NULL に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8172-121">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="c8172-122">NOTIFY_NEWMAIL_RECEIVED</span><span class="sxs-lookup"><span data-stu-id="c8172-122">NOTIFY_NEWMAIL_RECEIVED</span></span> 
  
> <span data-ttu-id="c8172-123">新しいメッセージがメッセージ ストアで受信された。</span><span class="sxs-lookup"><span data-stu-id="c8172-123">A new message has been received in the message store.</span></span> <span data-ttu-id="c8172-124">_lpvData パラメーターは_、メッセージ [をNEWMAIL_NOTIFICATION](newmail_notification.md)構造を示します。</span><span class="sxs-lookup"><span data-stu-id="c8172-124">The  _lpvData_ parameter points to a [NEWMAIL_NOTIFICATION](newmail_notification.md) structure that describes the message.</span></span> <span data-ttu-id="c8172-125">このフラグは、トランスポート プロバイダーと緊密に結合されているメッセージ ストア プロバイダーに使用され、ストア プロバイダーが MAPI_NO_MAIL フラグ セットでログオンしている場合は無視されます。</span><span class="sxs-lookup"><span data-stu-id="c8172-125">This flag is used for message store providers that are tightly coupled with transport providers and is ignored if the store provider is logged on with the MAPI_NO_MAIL flag set.</span></span> 
    
<span data-ttu-id="c8172-126">NOTIFY_NONCRIT</span><span class="sxs-lookup"><span data-stu-id="c8172-126">NOTIFY_NONCRIT</span></span> 
  
> <span data-ttu-id="c8172-127">_ulFlags_ を使用してスプーラー **Notify** を以前の呼び出しで取得した重要なセクションをNOTIFY_CRITSEC。</span><span class="sxs-lookup"><span data-stu-id="c8172-127">Releases a critical section that was obtained with a previous call to **SpoolerNotify** with  _ulFlags_ set to NOTIFY_CRITSEC.</span></span> <span data-ttu-id="c8172-128">_lpvData パラメーターは_ 未定義であり、NULL に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8172-128">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="c8172-129">NOTIFY_READYTOSEND</span><span class="sxs-lookup"><span data-stu-id="c8172-129">NOTIFY_READYTOSEND</span></span> 
  
> <span data-ttu-id="c8172-130">トランスポートまたはメッセージ ストア プロバイダーは、メッセージを送信する準備ができました。</span><span class="sxs-lookup"><span data-stu-id="c8172-130">The transport or message store provider is ready to send messages.</span></span> <span data-ttu-id="c8172-131">_lpvData パラメーターは_ 未定義であり、NULL に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8172-131">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="c8172-132">NOTIFY_SENTDEFERRED</span><span class="sxs-lookup"><span data-stu-id="c8172-132">NOTIFY_SENTDEFERRED</span></span> 
  
> <span data-ttu-id="c8172-133">以前に延期されたメッセージを送信し [、IXPLogon::SubmitMessage](ixplogon-submitmessage.md) メソッドへの呼び出しを使用してメッセージを配信する準備ができたら、トランスポート プロバイダーに通知する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8172-133">A previously deferred message should now be sent, and the transport provider should be notified when the message is ready to be delivered by using a call to the [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) method.</span></span> <span data-ttu-id="c8172-134">遅延メッセージのエントリ識別子は、lpvData が指す [SBinary](sbinary.md)構造 _に含まれる。_</span><span class="sxs-lookup"><span data-stu-id="c8172-134">The entry identifier of the deferred message is contained in an [SBinary](sbinary.md) structure pointed to by  _lpvData_.</span></span> <span data-ttu-id="c8172-135">_lpvData_ パラメーター NOTIFY_SENTDEFERREDとNOTIFY_CRITICAL_ERROR両方が使用できるので、これらのフラグは相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="c8172-135">Because both NOTIFY_SENTDEFERRED and NOTIFY_CRITICAL_ERROR use the  _lpvData_ parameter, these flags are mutually exclusive.</span></span> 
    
 <span data-ttu-id="c8172-136">_lpvData_</span><span class="sxs-lookup"><span data-stu-id="c8172-136">_lpvData_</span></span>
  
> <span data-ttu-id="c8172-137">[in]通知に適用可能な関連データへのポインター。</span><span class="sxs-lookup"><span data-stu-id="c8172-137">[in] A pointer to associated data applicable to a notification.</span></span> <span data-ttu-id="c8172-138">_lpvData パラメーターは_、次のフラグが設定されている場合にのみ有効なデータをポイントします _(ulFlags_ が他の通知の種類に設定されている場合 _、lpvData_ は NULL です)。</span><span class="sxs-lookup"><span data-stu-id="c8172-138">The  _lpvData_ parameter points to valid data only when the following flags are set (_lpvData_ is NULL when  _ulFlags_ is set to the other notification types):</span></span> 
    
|<span data-ttu-id="c8172-139">**_ulFlags_ 設定**</span><span class="sxs-lookup"><span data-stu-id="c8172-139">**_ulFlags_ setting**</span></span>|<span data-ttu-id="c8172-140">**_lpvData_ 値**</span><span class="sxs-lookup"><span data-stu-id="c8172-140">**_lpvData_ value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c8172-141">NOTIFY_CRITICAL_ERROR</span><span class="sxs-lookup"><span data-stu-id="c8172-141">NOTIFY_CRITICAL_ERROR</span></span>  <br/> |<span data-ttu-id="c8172-142">エラーに関する情報。</span><span class="sxs-lookup"><span data-stu-id="c8172-142">Information about the error.</span></span>  <br/> |
|<span data-ttu-id="c8172-143">NOTIFY_NEWMAIL_RECEIVED</span><span class="sxs-lookup"><span data-stu-id="c8172-143">NOTIFY_NEWMAIL_RECEIVED</span></span>  <br/> |<span data-ttu-id="c8172-144">新 **NEWMAIL_NOTIFICATION** メッセージに関する情報を含む、新しいメッセージ構造。</span><span class="sxs-lookup"><span data-stu-id="c8172-144">A **NEWMAIL_NOTIFICATION** structure that contains information about the newly delivered message.</span></span>  <br/> |
|<span data-ttu-id="c8172-145">NOTIFY_SENTDEFERRED</span><span class="sxs-lookup"><span data-stu-id="c8172-145">NOTIFY_SENTDEFERRED</span></span>  <br/> |<span data-ttu-id="c8172-146">遅延 **メッセージのエントリ** 識別子を含む SBinary 構造体。</span><span class="sxs-lookup"><span data-stu-id="c8172-146">An **SBinary** structure that contains the entry identifier of deferred message.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="c8172-147">戻り値</span><span class="sxs-lookup"><span data-stu-id="c8172-147">Return value</span></span>

<span data-ttu-id="c8172-148">S_OK</span><span class="sxs-lookup"><span data-stu-id="c8172-148">S_OK</span></span> 
  
> <span data-ttu-id="c8172-149">通知が成功しました。</span><span class="sxs-lookup"><span data-stu-id="c8172-149">The notification was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c8172-150">注釈</span><span class="sxs-lookup"><span data-stu-id="c8172-150">Remarks</span></span>

<span data-ttu-id="c8172-151">**IMAPISupport::SpoolerNotify** メソッドは、メッセージ ストアおよびトランスポート プロバイダーのサポート オブジェクトに実装されます。</span><span class="sxs-lookup"><span data-stu-id="c8172-151">The **IMAPISupport::SpoolerNotify** method is implemented for message store and transport provider support objects.</span></span> <span data-ttu-id="c8172-152">これらのプロバイダーは、 **状態の変更または** サービスの要求を MAPI スプーラーに通知するためにスプーラーNotify を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c8172-152">These providers call **SpoolerNotify** to notify the MAPI spooler of a change in status or a request for service.</span></span> <span data-ttu-id="c8172-153">**SpoolerNotify** は、主にトランスポート プロバイダーによって呼び出され、セッション中にいつでも呼び出される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c8172-153">**SpoolerNotify** is called primarily by transport providers and may be called at any time during the session.</span></span> 
  
## <a name="notes-to-transport-providers"></a><span data-ttu-id="c8172-154">トランスポート プロバイダーへのメモ</span><span class="sxs-lookup"><span data-stu-id="c8172-154">Notes to Transport Providers</span></span>

<span data-ttu-id="c8172-155">トランスポート プロバイダーの構成を変更した場合は **、SpoolerNotify** を呼び出し  _、ulFlags_ を NOTIFY_CONFIG_CHANGED。</span><span class="sxs-lookup"><span data-stu-id="c8172-155">If you have changed your transport provider configuration, call **SpoolerNotify** and set  _ulFlags_ to NOTIFY_CONFIG_CHANGED.</span></span> <span data-ttu-id="c8172-156">**SpoolerNotify** は、サポートされているアドレスの種類の変更をクエリするために [IXPLogon::AddressTypes](ixplogon-addresstypes.md) メソッドを呼び出して応答します。</span><span class="sxs-lookup"><span data-stu-id="c8172-156">**SpoolerNotify** responds by calling the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method to query for a change in supported address types.</span></span> 
  
<span data-ttu-id="c8172-157">中断のない処理を確実に行う重要なセクションが必要な場合は _、ulFlags_ を設定して **SpoolerNotify** を呼び出NOTIFY_CRITSEC。</span><span class="sxs-lookup"><span data-stu-id="c8172-157">If you need a critical section to ensure uninterrupted processing, call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_CRITSEC.</span></span> <span data-ttu-id="c8172-158">このフラグを設定すると、MAPI スプーラーは [IXPLogon::Idle メソッドと IXPLogon::P oll](ixplogon-idle.md) メソッドを呼び出 [す必要はないと](ixplogon-poll.md) 通知します。</span><span class="sxs-lookup"><span data-stu-id="c8172-158">Setting this flag informs the MAPI spooler that it should not call the [IXPLogon::Idle](ixplogon-idle.md) and [IXPLogon::Poll](ixplogon-poll.md) methods.</span></span> <span data-ttu-id="c8172-159">重要なセクションを開いている間 [、IMAPIStatus::ValidateState](imapistatus-validatestate.md) メソッドMAPI_E_BUSY呼び出されるたびに、このセクションを返します。</span><span class="sxs-lookup"><span data-stu-id="c8172-159">While you have a critical section open, return MAPI_E_BUSY whenever the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method is called.</span></span> <span data-ttu-id="c8172-160">クリティカル セクションが終了したら _、ulFlags_ を設定して **SpoolerNotify** に別の呼び出しをNOTIFY_NONCRIT。</span><span class="sxs-lookup"><span data-stu-id="c8172-160">When you are finished with the critical section, make another call to **SpoolerNotify** with  _ulFlags_ set to NOTIFY_NONCRIT.</span></span> 
  
<span data-ttu-id="c8172-161">たとえば、リモート トランスポート プロバイダーがメッセージのアップロード中である場合、リモート接続を確立するために、ユーザーに電話番号の入力を許可する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="c8172-161">For example, if your remote transport provider is in the process of uploading messages, you might need to allow a user to enter a telephone number to establish the remote connection.</span></span> <span data-ttu-id="c8172-162">ダイアログ ボックスの手順をループする前に、重要なセクションを宣言する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8172-162">Before you loop through the dialog box procedure, you should declare a critical section.</span></span> <span data-ttu-id="c8172-163">ユーザーがダイアログ ボックスを閉じ、ダイアログ ボックスの手順を終了すると、重要なセクションを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8172-163">When the user closes the dialog box, terminating the dialog box procedure, you should release the critical section.</span></span>
  
<span data-ttu-id="c8172-164">_ulFlags を NOTIFY_CRITICAL_ERROR_ すると、MAPI スプーラーはプロバイダーを解放する以外にそれ以上呼び出しません。</span><span class="sxs-lookup"><span data-stu-id="c8172-164">When you set  _ulFlags_ to NOTIFY_CRITICAL_ERROR, the MAPI spooler makes no further calls to the provider except to release it.</span></span> <span data-ttu-id="c8172-165">[IXPLogon::StartMessage](ixplogon-startmessage.md)メソッドまたは [IXPLogon::SubmitMessage](ixplogon-submitmessage.md)メソッドから NOTIFY_CRITICAL_ERROR セットを使用して **SpoolerNotify** を呼び出す場合は、スプーラー **Notify** 呼び出しの直後に **StartMessage** または \*\* SubmitMessage \*\* 呼び出しから適切なエラー値を返します。</span><span class="sxs-lookup"><span data-stu-id="c8172-165">If you call **SpoolerNotify** with NOTIFY_CRITICAL_ERROR set from the [IXPLogon::StartMessage](ixplogon-startmessage.md) or [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) methods, return with an appropriate error value from the **StartMessage** or \*\* SubmitMessage \*\* call immediately after the **SpoolerNotify** call.</span></span> 
  
<span data-ttu-id="c8172-166">以前に障害が発生した状態からトランスポート プロバイダーが回復した場合は _、ulFlags_ を使用してスプーラー **Notify** を呼び出NOTIFY_READYTOSEND。</span><span class="sxs-lookup"><span data-stu-id="c8172-166">If your transport provider recovered from a condition that previously caused it to fail, call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_READYTOSEND.</span></span> <span data-ttu-id="c8172-167">このフラグは、プロバイダーがメッセージを処理する準備ができていることを示します。</span><span class="sxs-lookup"><span data-stu-id="c8172-167">This flag indicates that the provider is again ready to handle messages.</span></span> 
  
## <a name="notes-to-message-store-providers"></a><span data-ttu-id="c8172-168">メッセージ ストア プロバイダーへのメモ</span><span class="sxs-lookup"><span data-stu-id="c8172-168">Notes to Message Store Providers</span></span>

<span data-ttu-id="c8172-169">**SpoolerNotify** を呼び出し **、iMessage::SubmitMessage** で [IMAPISupport::P repareSubmit](imapisupport-preparesubmit.md)に最初の呼び出しを行う前に _、ulFlags_ で NOTIFY_READYTOSEND フラグを渡します。</span><span class="sxs-lookup"><span data-stu-id="c8172-169">Call **SpoolerNotify**, passing the NOTIFY_READYTOSEND flag in  _ulFlags_, before you make your first call to [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) in **IMessage::SubmitMessage**.</span></span> <span data-ttu-id="c8172-170">**SpoolerNotify へのこの呼び出し** は、セッションごとに 1 回だけ行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8172-170">This call to **SpoolerNotify** needs to be made only once per session.</span></span> 
  
<span data-ttu-id="c8172-171">メッセージ ストア プロバイダーがトランスポート プロバイダーと緊密に結合され _、ulFlags_ が NOTIFY_NEWMAIL_RECEIVED に設定されたスプーラー **Notify** を呼び出す場合、MAPI スプーラーは新しいメッセージを開き、新しいメッセージ フック関数の処理を開始します。</span><span class="sxs-lookup"><span data-stu-id="c8172-171">If your message store provider is tightly coupled with a transport provider and you call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_NEWMAIL_RECEIVED, the MAPI spooler opens the new message and begins processing the new message hook function.</span></span> <span data-ttu-id="c8172-172">処理が完了すると、MAPI スプーラーは [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) メソッドを呼び出して、独自の新しいメッセージを通知します。</span><span class="sxs-lookup"><span data-stu-id="c8172-172">When processing is complete, the MAPI spooler calls the [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method to inform you of your own new message.</span></span> 
  
<span data-ttu-id="c8172-173">**SpoolerNotify の呼び出しの詳細については**、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c8172-173">For more information about calling **SpoolerNotify**, see any of the following topics:</span></span>
  
- [<span data-ttu-id="c8172-174">FlushQueues メソッドの実装</span><span class="sxs-lookup"><span data-stu-id="c8172-174">Implementing the FlushQueues Method</span></span>](implementing-the-flushqueues-method.md)
    
- [<span data-ttu-id="c8172-175">MAPI スプーラーの操作</span><span class="sxs-lookup"><span data-stu-id="c8172-175">Interacting with the MAPI Spooler</span></span>](interacting-with-the-mapi-spooler.md)
    
- [<span data-ttu-id="c8172-176">メッセージ受信モデル</span><span class="sxs-lookup"><span data-stu-id="c8172-176">Message Reception Model</span></span>](message-reception-model.md)
    
## <a name="see-also"></a><span data-ttu-id="c8172-177">関連項目</span><span class="sxs-lookup"><span data-stu-id="c8172-177">See also</span></span>



[<span data-ttu-id="c8172-178">IMsgStore::NotifyNewMail</span><span class="sxs-lookup"><span data-stu-id="c8172-178">IMsgStore::NotifyNewMail</span></span>](imsgstore-notifynewmail.md)
  
[<span data-ttu-id="c8172-179">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="c8172-179">IXPLogon::StartMessage</span></span>](ixplogon-startmessage.md)
  
[<span data-ttu-id="c8172-180">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="c8172-180">IXPLogon::SubmitMessage</span></span>](ixplogon-submitmessage.md)
  
[<span data-ttu-id="c8172-181">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="c8172-181">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

