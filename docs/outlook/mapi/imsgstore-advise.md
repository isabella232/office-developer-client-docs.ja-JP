---
title: IMsgStoreAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.Advise
api_type:
- COM
ms.assetid: 8c57e743-a798-4e39-a61a-46dff8b1ac7c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6a315cef8263f7e241a815a0f054dc3174d88fa7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800989"
---
# <a name="imsgstoreadvise"></a><span data-ttu-id="ecce8-103">IMsgStore::Advise</span><span class="sxs-lookup"><span data-stu-id="ecce8-103">IMsgStore::Advise</span></span>

  
  
<span data-ttu-id="ecce8-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ecce8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ecce8-105">メッセージ ・ ストアに影響を与える特定のイベントの通知を受け取ることを登録します。</span><span class="sxs-lookup"><span data-stu-id="ecce8-105">Registers to receive notification of specified events that affect the message store.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="ecce8-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ecce8-106">Parameters</span></span>

 <span data-ttu-id="ecce8-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="ecce8-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="ecce8-108">[in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="ecce8-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="ecce8-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="ecce8-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="ecce8-110">[in]フォルダーまたはメッセージに関する通知を生成するか、または**null**のエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ecce8-110">[in] A pointer to the entry identifier of the folder or message about which notifications should be generated, or **null**.</span></span> <span data-ttu-id="ecce8-111">_LpEntryID_を NULL に設定すると、**アドバイス**は全体のメッセージ ・ ストアに通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="ecce8-111">If  _lpEntryID_ is set to NULL, **Advise** registers for notifications on the entire message store.</span></span> 
    
 <span data-ttu-id="ecce8-112">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="ecce8-112">_ulEventMask_</span></span>
  
> <span data-ttu-id="ecce8-113">[in]呼び出し元に興味を持って登録に含めることが通知イベントの種類を示す値のマスク。</span><span class="sxs-lookup"><span data-stu-id="ecce8-113">[in] A mask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="ecce8-114">各イベントに関する情報を保持するイベントの種類に関連付けられている対応する[通知](notification.md)の構造があります。</span><span class="sxs-lookup"><span data-stu-id="ecce8-114">There is a corresponding [NOTIFICATION](notification.md) structure associated with each type of event that holds information about the event.</span></span> <span data-ttu-id="ecce8-115">_UlEventMask_パラメーターに有効な値は、次のように。</span><span class="sxs-lookup"><span data-stu-id="ecce8-115">The following are valid values for the  _ulEventMask_ parameter:</span></span> 
    
 <span data-ttu-id="ecce8-116">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="ecce8-116">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="ecce8-117">メモリ不足などの重大なエラーに関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="ecce8-117">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
 <span data-ttu-id="ecce8-118">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="ecce8-118">_fnevExtended_</span></span>
  
> <span data-ttu-id="ecce8-119">プロバイダーを格納する特定のメッセージに特定のイベントに関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="ecce8-119">Registers for notifications about events specific to the particular message store provider.</span></span>
    
 <span data-ttu-id="ecce8-120">_fnevNewMail_</span><span class="sxs-lookup"><span data-stu-id="ecce8-120">_fnevNewMail_</span></span>
  
> <span data-ttu-id="ecce8-121">新しいメッセージの到着の通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="ecce8-121">Registers for notifications about the arrival of new messages.</span></span> 
    
 <span data-ttu-id="ecce8-122">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="ecce8-122">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="ecce8-123">新しいフォルダーまたはメッセージの作成についての通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="ecce8-123">Registers for notifications about the creation of a new folder or message.</span></span>
    
 <span data-ttu-id="ecce8-124">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="ecce8-124">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="ecce8-125">フォルダーまたはコピーするメッセージに関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="ecce8-125">Registers for notifications about a folder or message being copied.</span></span>
    
 <span data-ttu-id="ecce8-126">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="ecce8-126">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="ecce8-127">フォルダーまたはメッセージの削除についての通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="ecce8-127">Registers for notifications about a folder or message being deleted.</span></span>
    
 <span data-ttu-id="ecce8-128">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="ecce8-128">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="ecce8-129">フォルダーまたはメッセージの変更に関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="ecce8-129">Registers for notifications about a folder or message being modified.</span></span>
    
 <span data-ttu-id="ecce8-130">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="ecce8-130">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="ecce8-131">フォルダーまたは移動するメッセージに関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="ecce8-131">Registers for notifications about a folder or message being moved.</span></span>
    
 <span data-ttu-id="ecce8-132">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="ecce8-132">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="ecce8-133">検索操作の完了に関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="ecce8-133">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="ecce8-134">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="ecce8-134">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="ecce8-135">[in]後続の通知を受信するアドバイズ シンク オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ecce8-135">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="ecce8-136">このアドバイズ シンク オブジェクトは既に割り当てられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="ecce8-136">This advise sink object must have already been allocated.</span></span>
    
 <span data-ttu-id="ecce8-137">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="ecce8-137">_lpulConnection_</span></span>
  
> <span data-ttu-id="ecce8-138">[out]呼び出し元の間の接続を表す数値を 0 以外の値へのポインターでは、シンク オブジェクトとのセッションを案内します。</span><span class="sxs-lookup"><span data-stu-id="ecce8-138">[out] A pointer to a nonzero number that represents the connection between the caller's advise sink object and the session.</span></span> 
    
 <span data-ttu-id="ecce8-139">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="ecce8-139">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="ecce8-140">[in]後続の通知を受信するアドバイズ シンク オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ecce8-140">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="ecce8-141">このアドバイズ シンク オブジェクトは既に割り当てられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="ecce8-141">This advise sink object must have already been allocated.</span></span> 
    
 <span data-ttu-id="ecce8-142">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="ecce8-142">_lpulConnection_</span></span>
  
> <span data-ttu-id="ecce8-143">[out]呼び出し元の間の接続を表す、0 以外の接続番号へのポインターでは、シンク オブジェクトとメッセージ ストアを案内します。</span><span class="sxs-lookup"><span data-stu-id="ecce8-143">[out] A pointer to a nonzero connection number that represents the connection between the caller's advise sink object and the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ecce8-144">�߂�l</span><span class="sxs-lookup"><span data-stu-id="ecce8-144">Return value</span></span>

<span data-ttu-id="ecce8-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="ecce8-145">S_OK</span></span> 
  
> <span data-ttu-id="ecce8-146">登録が正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="ecce8-146">The registration was successful.</span></span>
    
<span data-ttu-id="ecce8-147">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="ecce8-147">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="ecce8-148">メッセージ ストア プロバイダーは、メッセージ ・ ストアを使用して通知の登録をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="ecce8-148">The message store provider does not support registration for notification through the message store.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ecce8-149">注釈</span><span class="sxs-lookup"><span data-stu-id="ecce8-149">Remarks</span></span>

<span data-ttu-id="ecce8-150">**IMsgStore::Advise**メソッドでは、シンク オブジェクトと、メッセージ ストアまたはメッセージ ・ ストア内のオブジェクトにアドバイスの呼び出し元の間の接続を確立します。</span><span class="sxs-lookup"><span data-stu-id="ecce8-150">The **IMsgStore::Advise** method establishes a connection between the caller's advise sink object and either the message store or an object in the message store.</span></span> <span data-ttu-id="ecce8-151">この接続を使用していずれかのアドバイズ シンクに通知を送信するか、アドバイズ ソース オブジェクトに、 _ulEventMask_パラメーターで指定されているより多くのイベントが発生します。</span><span class="sxs-lookup"><span data-stu-id="ecce8-151">This connection is used to send notifications to the advise sink when one or more events, as specified in the  _ulEventMask_ parameter, occur to the advise source object.</span></span> <span data-ttu-id="ecce8-152">_LpEntryID_パラメーターが有効なエントリの識別子にポイントして、アドバイズ ソースは、このエントリの識別子によって識別されるオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="ecce8-152">When the  _lpEntryID_ parameter points to a valid entry identifier, the advise source is the object identified by this entry identifier.</span></span> <span data-ttu-id="ecce8-153">_LpEntryID_が NULL の場合は、アドバイスのソースは、メッセージ ストアです。</span><span class="sxs-lookup"><span data-stu-id="ecce8-153">When  _lpEntryID_ is NULL, the advise source is the message store.</span></span> 
  
<span data-ttu-id="ecce8-154">通知を送信するには、メッセージ ストア プロバイダーまたは MAPI のいずれかが登録されているアドバイズ シンクの[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ecce8-154">To send a notification, either the message store provider or MAPI calls the registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="ecce8-155">**OnNotify**通知の構造体をパラメーターの 1 つには、特定のイベントを説明する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ecce8-155">One of the parameters to **OnNotify**, a notification structure, contains information that describes the specific event.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ecce8-156">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="ecce8-156">Notes to implementers</span></span>

<span data-ttu-id="ecce8-157">MAPI の支援の有無にかかわらず、通知をサポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="ecce8-157">You can support notification with or without help from MAPI.</span></span> <span data-ttu-id="ecce8-158">MAPI サービス プロバイダーの通知を実装するために役立つ 3 つのサポート オブジェクトのメソッドを持つ: [IMAPISupport::Subscribe](imapisupport-subscribe.md)、 [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)、および[IMAPISupport::Notify](imapisupport-notify.md)。</span><span class="sxs-lookup"><span data-stu-id="ecce8-158">MAPI has three support object methods for helping service providers implement notification: [IMAPISupport::Subscribe](imapisupport-subscribe.md), [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md), and [IMAPISupport::Notify](imapisupport-notify.md).</span></span> <span data-ttu-id="ecce8-159">MAPI サポートされている方法を使用する場合、 **Subscribe**を呼び出して **、メソッド**が呼び出されたときと、 _lpAdviseSink_ポインターを解放します。</span><span class="sxs-lookup"><span data-stu-id="ecce8-159">If you elect to use the MAPI support methods, call **Subscribe** when your **Advise** method is called and release the  _lpAdviseSink_ pointer.</span></span> 
  
<span data-ttu-id="ecce8-160">自分で通知をサポートするように選択する場合は、このポインターのコピーを保持するのには、 _lpAdviseSink_パラメーターで表されるアドバイズ シンクの[IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ecce8-160">If you elect to support notification yourself, call the [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) method of the advise sink represented by the  _lpAdviseSink_ parameter to keep a copy of this pointer.</span></span> <span data-ttu-id="ecce8-161">登録をキャンセルするのには、 [IMsgStore::Unadvise](imsgstore-unadvise.md)メソッドが呼び出されるまでは、このコピーを維持します。</span><span class="sxs-lookup"><span data-stu-id="ecce8-161">Maintain this copy until your [IMsgStore::Unadvise](imsgstore-unadvise.md) method is called to cancel the registration.</span></span> 
  
<span data-ttu-id="ecce8-162">通知をサポートする方法に関係なく、通知の登録には 0 以外の接続番号を割り当てるし、 _lpulConnection_パラメーターに返すことです。</span><span class="sxs-lookup"><span data-stu-id="ecce8-162">Regardless of how you support notification, assign a nonzero connection number to the notification registration and return it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="ecce8-163">**Unadvise**が呼び出され、完了するまでは、この接続の数を解放しません。</span><span class="sxs-lookup"><span data-stu-id="ecce8-163">Do not release this connection number until **Unadvise** has been called and has completed.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ecce8-164">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="ecce8-164">Notes to callers</span></span>

<span data-ttu-id="ecce8-165">システムでは複数の実行スレッドをサポートする、 **OnNotify**への呼び出しも発生することが任意のスレッドで任意の時点。</span><span class="sxs-lookup"><span data-stu-id="ecce8-165">On systems that support multiple threads of execution, the call to **OnNotify** can also occur on any thread at any time.</span></span> <span data-ttu-id="ecce8-166">必要がありますが確実に特定のスレッドで特定の時刻にのみ通知が発生する場合、は、**アドバイス**に渡すアドバイズ シンク オブジェクトを生成する[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ecce8-166">If you must be assured that notifications occur only at a particular time on a particular thread, call the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to generate the advise sink object that you pass to **Advise**.</span></span> 
  
<span data-ttu-id="ecce8-167">**Advise**への呼び出しの後が成功し、 **Unadvise**は、登録をキャンセルするのには呼び出されると、前に、リリースするアドバイズ シンク オブジェクトを準備します。</span><span class="sxs-lookup"><span data-stu-id="ecce8-167">After a call to **Advise** has succeeded and before **Unadvise** has been called to cancel the registration, be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="ecce8-168">特定の長期的な使用がない限り、**アドバイス**が返された後は、アドバイズ シンク オブジェクトを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ecce8-168">You should release your advise sink object after **Advise** returns unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="ecce8-169">通知プロセスの詳細については、 [MAPI でのイベントの通知](event-notification-in-mapi.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ecce8-169">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="ecce8-170">通知の処理の詳細については、[通知の処理](handling-notifications.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ecce8-170">For more information about handling notifications, see [Handling Notifications](handling-notifications.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ecce8-171">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="ecce8-171">MFCMAPI reference</span></span>

<span data-ttu-id="ecce8-172">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="ecce8-172">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ecce8-173">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="ecce8-173">**File**</span></span>|<span data-ttu-id="ecce8-174">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="ecce8-174">**Function**</span></span>|<span data-ttu-id="ecce8-175">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="ecce8-175">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ecce8-176">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="ecce8-176">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="ecce8-177">CBaseDialog::OnNotificationsOn</span><span class="sxs-lookup"><span data-stu-id="ecce8-177">CBaseDialog::OnNotificationsOn</span></span>  <br/> |<span data-ttu-id="ecce8-178">MFCMAPI では、 **IMsgStore::Advise**メソッドを使用して、全体のメッセージ ・ ストアに通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="ecce8-178">MFCMAPI uses the **IMsgStore::Advise** method to register for notifications on the entire message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ecce8-179">関連項目</span><span class="sxs-lookup"><span data-stu-id="ecce8-179">See also</span></span>



[<span data-ttu-id="ecce8-180">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="ecce8-180">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="ecce8-181">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="ecce8-181">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="ecce8-182">IMsgStore::Unadvise</span><span class="sxs-lookup"><span data-stu-id="ecce8-182">IMsgStore::Unadvise</span></span>](imsgstore-unadvise.md)
  
[<span data-ttu-id="ecce8-183">�ʒm</span><span class="sxs-lookup"><span data-stu-id="ecce8-183">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="ecce8-184">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ecce8-184">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


<span data-ttu-id="ecce8-185">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="ecce8-185">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

