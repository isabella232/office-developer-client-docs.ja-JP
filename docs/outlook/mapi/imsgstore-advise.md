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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3b4abef731541e308b2c2ebc6f4aaddf4458e257
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317326"
---
# <a name="imsgstoreadvise"></a><span data-ttu-id="37f90-103">IMsgStore::Advise</span><span class="sxs-lookup"><span data-stu-id="37f90-103">IMsgStore::Advise</span></span>

  
  
<span data-ttu-id="37f90-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="37f90-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="37f90-105">メッセージ ストアに影響を与える指定されたイベントの通知を受信するために登録します。</span><span class="sxs-lookup"><span data-stu-id="37f90-105">Registers to receive notification of specified events that affect the message store.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="37f90-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37f90-106">Parameters</span></span>

 <span data-ttu-id="37f90-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="37f90-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="37f90-108">[in]  _lpEntryID_ パラメーターが指すエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="37f90-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="37f90-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="37f90-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="37f90-110">[in]生成する通知に関するフォルダーまたはメッセージのエントリ識別子へのポインター、または **null** です。</span><span class="sxs-lookup"><span data-stu-id="37f90-110">[in] A pointer to the entry identifier of the folder or message about which notifications should be generated, or **null**.</span></span> <span data-ttu-id="37f90-111">_lpEntryID が_ NULL に設定されている場合は、**メッセージ** ストア全体で通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="37f90-111">If  _lpEntryID_ is set to NULL, **Advise** registers for notifications on the entire message store.</span></span> 
    
 <span data-ttu-id="37f90-112">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="37f90-112">_ulEventMask_</span></span>
  
> <span data-ttu-id="37f90-113">[in]呼び出し元が関心を持ち、登録に含める必要がある通知イベントの種類を示す値のマスク。</span><span class="sxs-lookup"><span data-stu-id="37f90-113">[in] A mask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="37f90-114">イベントに関する [情報を](notification.md) 保持する各種類のイベントに関連付けられた対応する NOTIFICATION 構造があります。</span><span class="sxs-lookup"><span data-stu-id="37f90-114">There is a corresponding [NOTIFICATION](notification.md) structure associated with each type of event that holds information about the event.</span></span> <span data-ttu-id="37f90-115">ulEventMask パラメーターの有効な値  _を次に示_ します。</span><span class="sxs-lookup"><span data-stu-id="37f90-115">The following are valid values for the  _ulEventMask_ parameter:</span></span> 
    
 <span data-ttu-id="37f90-116">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="37f90-116">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="37f90-117">メモリ不足などの重大なエラーに関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="37f90-117">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
 <span data-ttu-id="37f90-118">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="37f90-118">_fnevExtended_</span></span>
  
> <span data-ttu-id="37f90-119">特定のメッセージ ストア プロバイダーに固有のイベントに関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="37f90-119">Registers for notifications about events specific to the particular message store provider.</span></span>
    
 <span data-ttu-id="37f90-120">_fnevNewMail_</span><span class="sxs-lookup"><span data-stu-id="37f90-120">_fnevNewMail_</span></span>
  
> <span data-ttu-id="37f90-121">新しいメッセージの到着に関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="37f90-121">Registers for notifications about the arrival of new messages.</span></span> 
    
 <span data-ttu-id="37f90-122">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="37f90-122">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="37f90-123">新しいフォルダーまたはメッセージの作成に関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="37f90-123">Registers for notifications about the creation of a new folder or message.</span></span>
    
 <span data-ttu-id="37f90-124">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="37f90-124">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="37f90-125">コピーするフォルダーまたはメッセージに関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="37f90-125">Registers for notifications about a folder or message being copied.</span></span>
    
 <span data-ttu-id="37f90-126">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="37f90-126">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="37f90-127">削除するフォルダーまたはメッセージに関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="37f90-127">Registers for notifications about a folder or message being deleted.</span></span>
    
 <span data-ttu-id="37f90-128">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="37f90-128">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="37f90-129">変更するフォルダーまたはメッセージに関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="37f90-129">Registers for notifications about a folder or message being modified.</span></span>
    
 <span data-ttu-id="37f90-130">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="37f90-130">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="37f90-131">移動するフォルダーまたはメッセージに関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="37f90-131">Registers for notifications about a folder or message being moved.</span></span>
    
 <span data-ttu-id="37f90-132">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="37f90-132">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="37f90-133">検索操作の完了に関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="37f90-133">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="37f90-134">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="37f90-134">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="37f90-135">[in]後続の通知を受信するアアドバイス シンク オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="37f90-135">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="37f90-136">このアアドバイス シンク オブジェクトは既に割り当てられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="37f90-136">This advise sink object must have already been allocated.</span></span>
    
 <span data-ttu-id="37f90-137">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="37f90-137">_lpulConnection_</span></span>
  
> <span data-ttu-id="37f90-138">[out]呼び出し元の通知シンク オブジェクトとセッションの間の接続を表す 0 以外の数値へのポインター。</span><span class="sxs-lookup"><span data-stu-id="37f90-138">[out] A pointer to a nonzero number that represents the connection between the caller's advise sink object and the session.</span></span> 
    
 <span data-ttu-id="37f90-139">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="37f90-139">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="37f90-140">[in]後続の通知を受信するアアドバイス シンク オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="37f90-140">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="37f90-141">このアアドバイス シンク オブジェクトは既に割り当てられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="37f90-141">This advise sink object must have already been allocated.</span></span> 
    
 <span data-ttu-id="37f90-142">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="37f90-142">_lpulConnection_</span></span>
  
> <span data-ttu-id="37f90-143">[out]呼び出し元のアアドバイス シンク オブジェクトとメッセージ ストア間の接続を表す 0 以外の接続番号へのポインター。</span><span class="sxs-lookup"><span data-stu-id="37f90-143">[out] A pointer to a nonzero connection number that represents the connection between the caller's advise sink object and the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="37f90-144">戻り値</span><span class="sxs-lookup"><span data-stu-id="37f90-144">Return value</span></span>

<span data-ttu-id="37f90-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="37f90-145">S_OK</span></span> 
  
> <span data-ttu-id="37f90-146">登録が成功しました。</span><span class="sxs-lookup"><span data-stu-id="37f90-146">The registration was successful.</span></span>
    
<span data-ttu-id="37f90-147">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="37f90-147">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="37f90-148">メッセージ ストア プロバイダーは、メッセージ ストアを通じた通知の登録をサポートしていない。</span><span class="sxs-lookup"><span data-stu-id="37f90-148">The message store provider does not support registration for notification through the message store.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="37f90-149">注釈</span><span class="sxs-lookup"><span data-stu-id="37f90-149">Remarks</span></span>

<span data-ttu-id="37f90-150">**IMsgStore::Advise** メソッドは、呼び出し元のアドバイス シンク オブジェクトと、メッセージ ストアまたはメッセージ ストア内のオブジェクトとの間の接続を確立します。</span><span class="sxs-lookup"><span data-stu-id="37f90-150">The **IMsgStore::Advise** method establishes a connection between the caller's advise sink object and either the message store or an object in the message store.</span></span> <span data-ttu-id="37f90-151">この接続は  _、ulEventMask_ パラメーターで指定されている 1 つ以上のイベントがアアドバイス ソース オブジェクトに発生した場合に、通知シンクに通知を送信するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="37f90-151">This connection is used to send notifications to the advise sink when one or more events, as specified in the  _ulEventMask_ parameter, occur to the advise source object.</span></span> <span data-ttu-id="37f90-152">_lpEntryID_ パラメーターが有効なエントリ識別子をポイントする場合、アドバイス ソースは、このエントリ識別子で識別されるオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="37f90-152">When the  _lpEntryID_ parameter points to a valid entry identifier, the advise source is the object identified by this entry identifier.</span></span> <span data-ttu-id="37f90-153">_lpEntryID が_ NULL の場合、アドバイス ソースはメッセージ ストアです。</span><span class="sxs-lookup"><span data-stu-id="37f90-153">When  _lpEntryID_ is NULL, the advise source is the message store.</span></span> 
  
<span data-ttu-id="37f90-154">通知を送信するには、メッセージ ストア プロバイダーまたは MAPI が登録されているアアドバイス シンクの [IMAPIAdviseSink::OnNotify メソッドを呼び出](imapiadvisesink-onnotify.md) します。</span><span class="sxs-lookup"><span data-stu-id="37f90-154">To send a notification, either the message store provider or MAPI calls the registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="37f90-155">通知構造である **OnNotify** のパラメーターの 1 つには、特定のイベントを記述する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="37f90-155">One of the parameters to **OnNotify**, a notification structure, contains information that describes the specific event.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="37f90-156">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="37f90-156">Notes to implementers</span></span>

<span data-ttu-id="37f90-157">MAPI からの通知のサポートとサポートなし。</span><span class="sxs-lookup"><span data-stu-id="37f90-157">You can support notification with or without help from MAPI.</span></span> <span data-ttu-id="37f90-158">MAPI には、サービス プロバイダーが通知を実装するための 3 つのサポート オブジェクト メソッドがあります[。IMAPISupport::Subscribe](imapisupport-subscribe.md) [、IMAPISupport::Unsubscribe、](imapisupport-unsubscribe.md)[および IMAPISupport::Notify](imapisupport-notify.md)です。</span><span class="sxs-lookup"><span data-stu-id="37f90-158">MAPI has three support object methods for helping service providers implement notification: [IMAPISupport::Subscribe](imapisupport-subscribe.md), [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md), and [IMAPISupport::Notify](imapisupport-notify.md).</span></span> <span data-ttu-id="37f90-159">MAPI サポート メソッドを使用する場合は **、Advise** メソッドが呼び出されたときに Subscribe を呼び出し _、lpAdviseSink ポインターを解放_ します。 </span><span class="sxs-lookup"><span data-stu-id="37f90-159">If you elect to use the MAPI support methods, call **Subscribe** when your **Advise** method is called and release the  _lpAdviseSink_ pointer.</span></span> 
  
<span data-ttu-id="37f90-160">通知を自分でサポートする場合は _、lpAdviseSink_ パラメーターで表されるアアドバイス シンクの [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)メソッドを呼び出して、このポインターのコピーを保持します。</span><span class="sxs-lookup"><span data-stu-id="37f90-160">If you elect to support notification yourself, call the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method of the advise sink represented by the  _lpAdviseSink_ parameter to keep a copy of this pointer.</span></span> <span data-ttu-id="37f90-161">登録を取り消す [IMsgStore::Unadvise](imsgstore-unadvise.md) メソッドが呼び出されるまで、このコピーを維持します。</span><span class="sxs-lookup"><span data-stu-id="37f90-161">Maintain this copy until your [IMsgStore::Unadvise](imsgstore-unadvise.md) method is called to cancel the registration.</span></span> 
  
<span data-ttu-id="37f90-162">通知のサポート方法に関係なく、0 以外の接続番号を通知登録に割り当て  _、lpulConnection パラメーターで返_ します。</span><span class="sxs-lookup"><span data-stu-id="37f90-162">Regardless of how you support notification, assign a nonzero connection number to the notification registration and return it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="37f90-163">**Unadvise** が呼び出され、完了するまで、この接続番号を解放しない。</span><span class="sxs-lookup"><span data-stu-id="37f90-163">Do not release this connection number until **Unadvise** has been called and has completed.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="37f90-164">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="37f90-164">Notes to callers</span></span>

<span data-ttu-id="37f90-165">複数の実行スレッドをサポートするシステムでは **、OnNotify** の呼び出しは、任意のスレッドでもいつでも実行できます。</span><span class="sxs-lookup"><span data-stu-id="37f90-165">On systems that support multiple threads of execution, the call to **OnNotify** can also occur on any thread at any time.</span></span> <span data-ttu-id="37f90-166">通知が特定のスレッドの特定の時刻にのみ発生すると確信する必要がある場合は [、HrThisThreadAdviseSink](hrthisthreadadvisesink.md) 関数を呼び出して **、Advise** に渡すアアドバイス シンク オブジェクトを生成します。</span><span class="sxs-lookup"><span data-stu-id="37f90-166">If you must be assured that notifications occur only at a particular time on a particular thread, call the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to generate the advise sink object that you pass to **Advise**.</span></span> 
  
<span data-ttu-id="37f90-167">Advise の呼 **び出** しが成功し、登録を取り消す **Unadvise** が呼び出される前に、アアドバイス シンク オブジェクトが解放される準備をしてください。</span><span class="sxs-lookup"><span data-stu-id="37f90-167">After a call to **Advise** has succeeded and before **Unadvise** has been called to cancel the registration, be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="37f90-168">特定の長期的な使用がない限り **、Advise** が返された後にアアドバイス シンク オブジェクトを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="37f90-168">You should release your advise sink object after **Advise** returns unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="37f90-169">通知プロセスの詳細については、「MAPI での [イベント通知」を参照してください](event-notification-in-mapi.md)。</span><span class="sxs-lookup"><span data-stu-id="37f90-169">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="37f90-170">通知の処理の詳細については、「通知の処理」 [を参照してください](handling-notifications.md)。</span><span class="sxs-lookup"><span data-stu-id="37f90-170">For more information about handling notifications, see [Handling Notifications](handling-notifications.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="37f90-171">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="37f90-171">MFCMAPI reference</span></span>

<span data-ttu-id="37f90-172">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="37f90-172">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="37f90-173">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="37f90-173">**File**</span></span>|<span data-ttu-id="37f90-174">**関数**</span><span class="sxs-lookup"><span data-stu-id="37f90-174">**Function**</span></span>|<span data-ttu-id="37f90-175">**コメント**</span><span class="sxs-lookup"><span data-stu-id="37f90-175">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="37f90-176">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="37f90-176">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="37f90-177">CBaseDialog::OnNotificationsOn</span><span class="sxs-lookup"><span data-stu-id="37f90-177">CBaseDialog::OnNotificationsOn</span></span>  <br/> |<span data-ttu-id="37f90-178">MFCMAPI は **、IMsgStore::Advise** メソッドを使用して、メッセージ ストア全体の通知に登録します。</span><span class="sxs-lookup"><span data-stu-id="37f90-178">MFCMAPI uses the **IMsgStore::Advise** method to register for notifications on the entire message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="37f90-179">関連項目</span><span class="sxs-lookup"><span data-stu-id="37f90-179">See also</span></span>



[<span data-ttu-id="37f90-180">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="37f90-180">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="37f90-181">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="37f90-181">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="37f90-182">IMsgStore::Unadvise</span><span class="sxs-lookup"><span data-stu-id="37f90-182">IMsgStore::Unadvise</span></span>](imsgstore-unadvise.md)
  
[<span data-ttu-id="37f90-183">�ʒm</span><span class="sxs-lookup"><span data-stu-id="37f90-183">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="37f90-184">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="37f90-184">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


<span data-ttu-id="37f90-185">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="37f90-185">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

