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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a2837e5470729ae3cdd0b83e17d0342620c986e8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592116"
---
# <a name="imapisupportspoolernotify"></a><span data-ttu-id="fe184-103">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="fe184-103">IMAPISupport::SpoolerNotify</span></span>

  
  
<span data-ttu-id="fe184-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fe184-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fe184-105">またはサービスの要求のステータスが変更された、MAPI スプーラーに通知します。</span><span class="sxs-lookup"><span data-stu-id="fe184-105">Notifies the MAPI spooler of a change in status or a request for service.</span></span> 
  
```cpp
HRESULT SpoolerNotify(
ULONG ulFlags,
LPVOID lpvData
);
```

## <a name="parameters"></a><span data-ttu-id="fe184-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="fe184-106">Parameters</span></span>

 <span data-ttu-id="fe184-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fe184-107">_ulFlags_</span></span>
  
> <span data-ttu-id="fe184-108">[in]通知の種類を示すフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="fe184-108">[in] A bitmask of flags that indicates the type of notification.</span></span> <span data-ttu-id="fe184-109">トランスポート プロバイダーは、すべての NOTIFY_NEWMAIL_RECEIVED; 以外のフラグを設定できます。NOTIFY_NEWMAIL_RECEIVED と NOTIFY_READTOSEND だけは、メッセージ ストア プロバイダーに対して有効です。</span><span class="sxs-lookup"><span data-stu-id="fe184-109">Transport providers can set all of the flags except for NOTIFY_NEWMAIL_RECEIVED; only NOTIFY_NEWMAIL_RECEIVED and NOTIFY_READTOSEND are valid for message store providers.</span></span> <span data-ttu-id="fe184-110">次のフラグは、 _ulFlags_パラメーターに有効です。</span><span class="sxs-lookup"><span data-stu-id="fe184-110">The following flags are valid for the  _ulFlags_ parameter:</span></span> 
    
<span data-ttu-id="fe184-111">NOTIFY_CONFIG_CHANGE</span><span class="sxs-lookup"><span data-stu-id="fe184-111">NOTIFY_CONFIG_CHANGE</span></span> 
  
> <span data-ttu-id="fe184-112">トランスポート プロバイダーの構成を変更する要求を登録します。</span><span class="sxs-lookup"><span data-stu-id="fe184-112">Registers a request to change the transport provider's configuration.</span></span> 
    
<span data-ttu-id="fe184-113">NOTIFY_CRITICAL_ERROR</span><span class="sxs-lookup"><span data-stu-id="fe184-113">NOTIFY_CRITICAL_ERROR</span></span> 
  
> <span data-ttu-id="fe184-114">トランスポート プロバイダーには、回復不能なエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="fe184-114">An unrecoverable error has occurred to the transport provider.</span></span> <span data-ttu-id="fe184-115">NOTIFY_SENTDEFERRED と NOTIFY_CRITICAL_ERROR の両方は、トランスポート プロバイダーの呼び出しを_lpvData_パラメーターを使用するため、これらのフラグは、相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="fe184-115">Because both NOTIFY_SENTDEFERRED and NOTIFY_CRITICAL_ERROR use the  _lpvData_ parameter for transport provider calls, these flags are mutually exclusive.</span></span> 
    
<span data-ttu-id="fe184-116">NOTIFY_CRITSEC</span><span class="sxs-lookup"><span data-stu-id="fe184-116">NOTIFY_CRITSEC</span></span> 
  
> <span data-ttu-id="fe184-117">トランスポート プロバイダーの重要なセクションを要求します。</span><span class="sxs-lookup"><span data-stu-id="fe184-117">Requests a critical section for the transport provider.</span></span> <span data-ttu-id="fe184-118">_LpvData_パラメーターは、定義されていないと、NULL にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="fe184-118">The  _lpvData_ parameter is undefined and should be NULL.</span></span> 
    
<span data-ttu-id="fe184-119">NOTIFY_NEWMAIL</span><span class="sxs-lookup"><span data-stu-id="fe184-119">NOTIFY_NEWMAIL</span></span> 
  
> <span data-ttu-id="fe184-120">MAPI スプーラーは、次の使用時に、新しく受信したメッセージをダウンロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="fe184-120">The MAPI spooler should download any newly received messages at the next available time.</span></span> <span data-ttu-id="fe184-121">_LpvData_パラメーターは、定義されていないと、NULL に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fe184-121">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="fe184-122">NOTIFY_NEWMAIL_RECEIVED</span><span class="sxs-lookup"><span data-stu-id="fe184-122">NOTIFY_NEWMAIL_RECEIVED</span></span> 
  
> <span data-ttu-id="fe184-123">メッセージ ・ ストアに新しいメッセージを受信しました。</span><span class="sxs-lookup"><span data-stu-id="fe184-123">A new message has been received in the message store.</span></span> <span data-ttu-id="fe184-124">_LpvData_パラメーターは、メッセージを記述する[NEWMAIL_NOTIFICATION](newmail_notification.md)構造体を指します。</span><span class="sxs-lookup"><span data-stu-id="fe184-124">The  _lpvData_ parameter points to a [NEWMAIL_NOTIFICATION](newmail_notification.md) structure that describes the message.</span></span> <span data-ttu-id="fe184-125">このフラグは、トランスポート プロバイダーと緊密に結合されているメッセージ ストア プロバイダーの使用は、ストア プロバイダーが、MAPI_NO_MAIL フラグを設定してログオンしている場合は無視されます。</span><span class="sxs-lookup"><span data-stu-id="fe184-125">This flag is used for message store providers that are tightly coupled with transport providers and is ignored if the store provider is logged on with the MAPI_NO_MAIL flag set.</span></span> 
    
<span data-ttu-id="fe184-126">NOTIFY_NONCRIT</span><span class="sxs-lookup"><span data-stu-id="fe184-126">NOTIFY_NONCRIT</span></span> 
  
> <span data-ttu-id="fe184-127">_UlFlags_ NOTIFY_CRITSEC に設定を**SpoolerNotify**に前の呼び出しで取得した重要なセクションを解放します。</span><span class="sxs-lookup"><span data-stu-id="fe184-127">Releases a critical section that was obtained with a previous call to **SpoolerNotify** with  _ulFlags_ set to NOTIFY_CRITSEC.</span></span> <span data-ttu-id="fe184-128">_LpvData_パラメーターは、定義されていないと、NULL に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fe184-128">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="fe184-129">NOTIFY_READYTOSEND</span><span class="sxs-lookup"><span data-stu-id="fe184-129">NOTIFY_READYTOSEND</span></span> 
  
> <span data-ttu-id="fe184-130">トランスポートまたはメッセージ ストア プロバイダーは、メッセージを送信する準備ができました。</span><span class="sxs-lookup"><span data-stu-id="fe184-130">The transport or message store provider is ready to send messages.</span></span> <span data-ttu-id="fe184-131">_LpvData_パラメーターは、定義されていないと、NULL に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fe184-131">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="fe184-132">NOTIFY_SENTDEFERRED</span><span class="sxs-lookup"><span data-stu-id="fe184-132">NOTIFY_SENTDEFERRED</span></span> 
  
> <span data-ttu-id="fe184-133">延期されていたメッセージを送信する必要がありますようになりましたと[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)メソッドの呼び出しを使用して配信する準備ができたら、メッセージ トランスポート プロバイダーに通知するか。</span><span class="sxs-lookup"><span data-stu-id="fe184-133">A previously deferred message should now be sent, and the transport provider should be notified when the message is ready to be delivered by using a call to the [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) method.</span></span> <span data-ttu-id="fe184-134">遅延メッセージのエントリ id は、 _lpvData_で示される[SBinary](sbinary.md)構造に含まれています。</span><span class="sxs-lookup"><span data-stu-id="fe184-134">The entry identifier of the deferred message is contained in an [SBinary](sbinary.md) structure pointed to by  _lpvData_.</span></span> <span data-ttu-id="fe184-135">NOTIFY_SENTDEFERRED と NOTIFY_CRITICAL_ERROR の両方は、 _lpvData_パラメーターを使用するため、これらのフラグは、相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="fe184-135">Because both NOTIFY_SENTDEFERRED and NOTIFY_CRITICAL_ERROR use the  _lpvData_ parameter, these flags are mutually exclusive.</span></span> 
    
 <span data-ttu-id="fe184-136">_lpvData_</span><span class="sxs-lookup"><span data-stu-id="fe184-136">_lpvData_</span></span>
  
> <span data-ttu-id="fe184-137">[in]通知に適用可能な関連のデータへのポインター。</span><span class="sxs-lookup"><span data-stu-id="fe184-137">[in] A pointer to associated data applicable to a notification.</span></span> <span data-ttu-id="fe184-138">_LpvData_パラメーターは、次のフラグが設定されている場合にのみ有効なデータを指す_lpvData_です_ulFlags_は、他の種類の通知に設定されている場合)。</span><span class="sxs-lookup"><span data-stu-id="fe184-138">The  _lpvData_ parameter points to valid data only when the following flags are set (_lpvData_ is NULL when  _ulFlags_ is set to the other notification types):</span></span> 
    
|<span data-ttu-id="fe184-139">**_ulFlags_設定**</span><span class="sxs-lookup"><span data-stu-id="fe184-139">**_ulFlags_ setting**</span></span>|<span data-ttu-id="fe184-140">**_lpvData_値**</span><span class="sxs-lookup"><span data-stu-id="fe184-140">**_lpvData_ value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fe184-141">NOTIFY_CRITICAL_ERROR</span><span class="sxs-lookup"><span data-stu-id="fe184-141">NOTIFY_CRITICAL_ERROR</span></span>  <br/> |<span data-ttu-id="fe184-142">エラーに関する情報です。</span><span class="sxs-lookup"><span data-stu-id="fe184-142">Information about the error.</span></span>  <br/> |
|<span data-ttu-id="fe184-143">NOTIFY_NEWMAIL_RECEIVED</span><span class="sxs-lookup"><span data-stu-id="fe184-143">NOTIFY_NEWMAIL_RECEIVED</span></span>  <br/> |<span data-ttu-id="fe184-144">新たに配信されたメッセージに関する情報を格納する**NEWMAIL_NOTIFICATION**構造体です。</span><span class="sxs-lookup"><span data-stu-id="fe184-144">A **NEWMAIL_NOTIFICATION** structure that contains information about the newly delivered message.</span></span>  <br/> |
|<span data-ttu-id="fe184-145">NOTIFY_SENTDEFERRED</span><span class="sxs-lookup"><span data-stu-id="fe184-145">NOTIFY_SENTDEFERRED</span></span>  <br/> |<span data-ttu-id="fe184-146">遅延メッセージのエントリ id が含まれています、 **SBinary**構造体です。</span><span class="sxs-lookup"><span data-stu-id="fe184-146">An **SBinary** structure that contains the entry identifier of deferred message.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="fe184-147">�߂�l</span><span class="sxs-lookup"><span data-stu-id="fe184-147">Return value</span></span>

<span data-ttu-id="fe184-148">S_OK</span><span class="sxs-lookup"><span data-stu-id="fe184-148">S_OK</span></span> 
  
> <span data-ttu-id="fe184-149">通知が正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="fe184-149">The notification was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fe184-150">注釈</span><span class="sxs-lookup"><span data-stu-id="fe184-150">Remarks</span></span>

<span data-ttu-id="fe184-151">**IMAPISupport::SpoolerNotify**メソッドはメッセージの格納およびプロバイダーのサポートのオブジェクトを転送します。</span><span class="sxs-lookup"><span data-stu-id="fe184-151">The **IMAPISupport::SpoolerNotify** method is implemented for message store and transport provider support objects.</span></span> <span data-ttu-id="fe184-152">これらのプロバイダーは、状態、またはサービスの要求が変更された、MAPI スプーラーを通知するために**SpoolerNotify**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="fe184-152">These providers call **SpoolerNotify** to notify the MAPI spooler of a change in status or a request for service.</span></span> <span data-ttu-id="fe184-153">**SpoolerNotify**は主にトランスポート プロバイダーによって呼び出され、セッション中にいつでも呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="fe184-153">**SpoolerNotify** is called primarily by transport providers and may be called at any time during the session.</span></span> 
  
## <a name="notes-to-transport-providers"></a><span data-ttu-id="fe184-154">トランスポート プロバイダーへのメモ</span><span class="sxs-lookup"><span data-stu-id="fe184-154">Notes to Transport Providers</span></span>

<span data-ttu-id="fe184-155">トランスポート プロバイダーの構成を変更した場合、 **SpoolerNotify**を呼び出すし、 _ulFlags_を NOTIFY_CONFIG_CHANGED に設定します。</span><span class="sxs-lookup"><span data-stu-id="fe184-155">If you have changed your transport provider configuration, call **SpoolerNotify** and set  _ulFlags_ to NOTIFY_CONFIG_CHANGED.</span></span> <span data-ttu-id="fe184-156">**SpoolerNotify**は、サポートされているアドレスの種類の変更をクエリに[IXPLogon::AddressTypes](ixplogon-addresstypes.md)メソッドを呼び出すことによって応答します。</span><span class="sxs-lookup"><span data-stu-id="fe184-156">**SpoolerNotify** responds by calling the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method to query for a change in supported address types.</span></span> 
  
<span data-ttu-id="fe184-157">処理が中断されないことを確認するクリティカル セクションが必要な場合は、 _ulFlags_ NOTIFY_CRITSEC に設定して**SpoolerNotify**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="fe184-157">If you need a critical section to ensure uninterrupted processing, call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_CRITSEC.</span></span> <span data-ttu-id="fe184-158">このフラグを設定する通知 MAPI スプーラー、 [IXPLogon::Idle](ixplogon-idle.md)メソッドと[IXPLogon::Poll](ixplogon-poll.md)メソッドは呼び出さないことです。</span><span class="sxs-lookup"><span data-stu-id="fe184-158">Setting this flag informs the MAPI spooler that it should not call the [IXPLogon::Idle](ixplogon-idle.md) and [IXPLogon::Poll](ixplogon-poll.md) methods.</span></span> <span data-ttu-id="fe184-159">開くには、クリティカル セクションがありますが、 [IMAPIStatus::ValidateState](imapistatus-validatestate.md)メソッドが呼び出されるたびに、MAPI_E_BUSY を返します。</span><span class="sxs-lookup"><span data-stu-id="fe184-159">While you have a critical section open, return MAPI_E_BUSY whenever the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method is called.</span></span> <span data-ttu-id="fe184-160">クリティカル セクションが完了したら、 _ulFlags_ NOTIFY_NONCRIT に設定を**SpoolerNotify**に対して別の呼び出しを行います。</span><span class="sxs-lookup"><span data-stu-id="fe184-160">When you are finished with the critical section, make another call to **SpoolerNotify** with  _ulFlags_ set to NOTIFY_NONCRIT.</span></span> 
  
<span data-ttu-id="fe184-161">たとえば、メッセージをアップロードして、リモート トランスポート プロバイダーがある場合は、ユーザーがリモート接続を確立するために電話番号を入力できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="fe184-161">For example, if your remote transport provider is in the process of uploading messages, you might need to allow a user to enter a telephone number to establish the remote connection.</span></span> <span data-ttu-id="fe184-162">ダイアログ ボックス プロシージャをループする前に、クリティカル セクションを宣言する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fe184-162">Before you loop through the dialog box procedure, you should declare a critical section.</span></span> <span data-ttu-id="fe184-163">ユーザーは、ダイアログ ボックスを終了するとき、ダイアログ ボックス プロシージャを終了する必要がありますクリティカル セクションを解放します。</span><span class="sxs-lookup"><span data-stu-id="fe184-163">When the user closes the dialog box, terminating the dialog box procedure, you should release the critical section.</span></span>
  
<span data-ttu-id="fe184-164">_UlFlags_を NOTIFY_CRITICAL_ERROR に設定すると、MAPI スプーラーにはそれ以降の呼び出し以外に元のプロバイダーがありません。</span><span class="sxs-lookup"><span data-stu-id="fe184-164">When you set  _ulFlags_ to NOTIFY_CRITICAL_ERROR, the MAPI spooler makes no further calls to the provider except to release it.</span></span> <span data-ttu-id="fe184-165">呼び出した場合、 [IXPLogon::StartMessage](ixplogon-startmessage.md)メソッドまたは[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)メソッドから NOTIFY_CRITICAL_ERROR と**SpoolerNotify** 、 **StartMessage**から適切なエラー値を返すか、* * SubmitMessage * * を呼び出すすぐに呼び出しの後、 **SpoolerNotify** 。</span><span class="sxs-lookup"><span data-stu-id="fe184-165">If you call **SpoolerNotify** with NOTIFY_CRITICAL_ERROR set from the [IXPLogon::StartMessage](ixplogon-startmessage.md) or [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) methods, return with an appropriate error value from the **StartMessage** or ** SubmitMessage ** call immediately after the **SpoolerNotify** call.</span></span> 
  
<span data-ttu-id="fe184-166">場合は、トランスポート プロバイダーは、以前エラーが発生する原因になった状態から回復は、 _ulFlags_ NOTIFY_READYTOSEND に設定して**SpoolerNotify**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="fe184-166">If your transport provider recovered from a condition that previously caused it to fail, call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_READYTOSEND.</span></span> <span data-ttu-id="fe184-167">このフラグは、プロバイダーがメッセージを処理する準備がもう一度ことを示します。</span><span class="sxs-lookup"><span data-stu-id="fe184-167">This flag indicates that the provider is again ready to handle messages.</span></span> 
  
## <a name="notes-to-message-store-providers"></a><span data-ttu-id="fe184-168">メッセージ ストア プロバイダーへのメモ</span><span class="sxs-lookup"><span data-stu-id="fe184-168">Notes to Message Store Providers</span></span>

<span data-ttu-id="fe184-169">**SpoolerNotify**、 _ulFlags_、 **IMessage::SubmitMessage**で[IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md)最初の呼び出しを行う前に NOTIFY_READYTOSEND フラグを渡してを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="fe184-169">Call **SpoolerNotify**, passing the NOTIFY_READYTOSEND flag in  _ulFlags_, before you make your first call to [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) in **IMessage::SubmitMessage**.</span></span> <span data-ttu-id="fe184-170">**SpoolerNotify**への呼び出しは、1 セッションあたり 1 回だけ行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="fe184-170">This call to **SpoolerNotify** needs to be made only once per session.</span></span> 
  
<span data-ttu-id="fe184-171">メッセージ ストア プロバイダーが密に結合されている場合、トランスポートを使用してプロバイダーを呼び出す**SpoolerNotify** NOTIFY_NEWMAIL_RECEIVED に設定された_ulFlags_ 、MAPI スプーラーが新しいメッセージを開くし、新しいメッセージ用のフック関数の処理を開始します。</span><span class="sxs-lookup"><span data-stu-id="fe184-171">If your message store provider is tightly coupled with a transport provider and you call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_NEWMAIL_RECEIVED, the MAPI spooler opens the new message and begins processing the new message hook function.</span></span> <span data-ttu-id="fe184-172">処理が完了すると、MAPI スプーラーは、独自の新しいメッセージを通知するために[IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="fe184-172">When processing is complete, the MAPI spooler calls the [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method to inform you of your own new message.</span></span> 
  
<span data-ttu-id="fe184-173">**SpoolerNotify**を呼び出す方法の詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="fe184-173">For more information about calling **SpoolerNotify**, see any of the following topics:</span></span>
  
- [<span data-ttu-id="fe184-174">FlushQueues メソッドの実装</span><span class="sxs-lookup"><span data-stu-id="fe184-174">Implementing the FlushQueues Method</span></span>](implementing-the-flushqueues-method.md)
    
- [<span data-ttu-id="fe184-175">MAPI スプーラーとの対話</span><span class="sxs-lookup"><span data-stu-id="fe184-175">Interacting with the MAPI Spooler</span></span>](interacting-with-the-mapi-spooler.md)
    
- [<span data-ttu-id="fe184-176">メッセージ受信モデル</span><span class="sxs-lookup"><span data-stu-id="fe184-176">Message Reception Model</span></span>](message-reception-model.md)
    
## <a name="see-also"></a><span data-ttu-id="fe184-177">関連項目</span><span class="sxs-lookup"><span data-stu-id="fe184-177">See also</span></span>



[<span data-ttu-id="fe184-178">IMsgStore::NotifyNewMail</span><span class="sxs-lookup"><span data-stu-id="fe184-178">IMsgStore::NotifyNewMail</span></span>](imsgstore-notifynewmail.md)
  
[<span data-ttu-id="fe184-179">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="fe184-179">IXPLogon::StartMessage</span></span>](ixplogon-startmessage.md)
  
[<span data-ttu-id="fe184-180">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="fe184-180">IXPLogon::SubmitMessage</span></span>](ixplogon-submitmessage.md)
  
[<span data-ttu-id="fe184-181">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="fe184-181">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

