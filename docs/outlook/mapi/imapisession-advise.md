---
title: imapisessionadvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.Advise
api_type:
- COM
ms.assetid: a6a6b6b1-31e2-4899-a5fe-74d5d1c2ccfc
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d5d87d7be9cb3524445107e975a298d4afd5bf98
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419836"
---
# <a name="imapisessionadvise"></a><span data-ttu-id="47bdb-103">IMAPISession::Advise</span><span class="sxs-lookup"><span data-stu-id="47bdb-103">IMAPISession::Advise</span></span>

  
  
<span data-ttu-id="47bdb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47bdb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47bdb-105">セッションに影響を与える指定したイベントの通知を受信するように登録します。</span><span class="sxs-lookup"><span data-stu-id="47bdb-105">Registers to receive notification of specified events that affect the session.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="47bdb-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="47bdb-106">Parameters</span></span>

 <span data-ttu-id="47bdb-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="47bdb-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="47bdb-108">順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="47bdb-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="47bdb-109">_lて tryid_</span><span class="sxs-lookup"><span data-stu-id="47bdb-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="47bdb-110">順番通知を生成する必要があるアドレス帳またはメッセージストアオブジェクトのエントリ id へのポインター。または、クライアントがセッションにのみ影響を与えるイベントに関する通知を受信するように登録していることを示します。</span><span class="sxs-lookup"><span data-stu-id="47bdb-110">[in] A pointer to the entry identifier of the address book or message store object about which notifications should be generated, or NULL, which indicates that the client is registering to receive notifications about events that affect only the session.</span></span> 
    
 <span data-ttu-id="47bdb-111">_uleventmask_</span><span class="sxs-lookup"><span data-stu-id="47bdb-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="47bdb-112">順番クライアントが関心を持っている通知イベントの種類を示す値のマスク。また、登録に含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="47bdb-112">[in] A mask of values that indicate the types of notification events that the client is interested in and should be included in the registration.</span></span> <span data-ttu-id="47bdb-113">_lな tryid_が NULL の場合、MAPI は、セッションにのみ影響を与える重大なエラーイベントに対してクライアントを自動的に登録します。</span><span class="sxs-lookup"><span data-stu-id="47bdb-113">If  _lpEntryID_ is NULL, MAPI automatically registers the client for critical error events that affect only the session.</span></span> <span data-ttu-id="47bdb-114">_lare tryid_がエントリ識別子を指す場合、 _uleventmask_パラメーターには次の値が有効です。</span><span class="sxs-lookup"><span data-stu-id="47bdb-114">When  _lpEntryID_ points to an entry identifier, the following values are valid for the  _ulEventMask_ parameter:</span></span> 
    
<span data-ttu-id="47bdb-115">fnevCriticalError</span><span class="sxs-lookup"><span data-stu-id="47bdb-115">fnevCriticalError</span></span> 
  
> <span data-ttu-id="47bdb-116">メモリ不足などの重大なエラーに関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="47bdb-116">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
<span data-ttu-id="47bdb-117">fnevExtended</span><span class="sxs-lookup"><span data-stu-id="47bdb-117">fnevExtended</span></span> 
  
> <span data-ttu-id="47bdb-118">特定のアドレス帳またはメッセージストアプロバイダーに固有のイベントと、セッションがシャットダウンしたことに関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="47bdb-118">Registers for notifications about events specific to a particular address book or message store provider and about session shut down.</span></span>
    
<span data-ttu-id="47bdb-119">fnevNewMail</span><span class="sxs-lookup"><span data-stu-id="47bdb-119">fnevNewMail</span></span> 
  
> <span data-ttu-id="47bdb-120">新しいメッセージが到着したことに関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="47bdb-120">Registers for notifications about the arrival of new messages.</span></span> 
    
<span data-ttu-id="47bdb-121">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="47bdb-121">fnevObjectCreated</span></span> 
  
> <span data-ttu-id="47bdb-122">新しいオブジェクトの作成に関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="47bdb-122">Registers for notifications about the creation of a new object.</span></span>
    
<span data-ttu-id="47bdb-123">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="47bdb-123">fnevObjectCopied</span></span>
  
> <span data-ttu-id="47bdb-124">コピーされているオブジェクトに関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="47bdb-124">Registers for notifications about an object being copied.</span></span>
    
<span data-ttu-id="47bdb-125">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="47bdb-125">fnevObjectDeleted</span></span>
  
> <span data-ttu-id="47bdb-126">削除されるオブジェクトに関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="47bdb-126">Registers for notifications about an object being deleted.</span></span>
    
<span data-ttu-id="47bdb-127">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="47bdb-127">fnevObjectModified</span></span>
  
> <span data-ttu-id="47bdb-128">変更されているオブジェクトに関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="47bdb-128">Registers for notifications about an object being modified.</span></span>
    
<span data-ttu-id="47bdb-129">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="47bdb-129">fnevObjectMoved</span></span>
  
> <span data-ttu-id="47bdb-130">移動中のオブジェクトに関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="47bdb-130">Registers for notifications about an object being moved.</span></span>
    
<span data-ttu-id="47bdb-131">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="47bdb-131">fnevSearchComplete</span></span>
  
> <span data-ttu-id="47bdb-132">検索操作の完了に関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="47bdb-132">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="47bdb-133">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="47bdb-133">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="47bdb-134">順番後続の通知を受け取るアドバイズシンクオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="47bdb-134">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="47bdb-135">このアドバイズシンクオブジェクトは、既に割り当てられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="47bdb-135">This advise sink object must have already been allocated.</span></span>
    
 <span data-ttu-id="47bdb-136">_lアウト接続_</span><span class="sxs-lookup"><span data-stu-id="47bdb-136">_lpulConnection_</span></span>
  
> <span data-ttu-id="47bdb-137">読み上げ呼び出し元のアドバイズシンクオブジェクトとセッション間の接続を表す0以外の数値へのポインター。</span><span class="sxs-lookup"><span data-stu-id="47bdb-137">[out] A pointer to a nonzero number that represents the connection between the caller's advise sink object and the session.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="47bdb-138">戻り値</span><span class="sxs-lookup"><span data-stu-id="47bdb-138">Return value</span></span>

<span data-ttu-id="47bdb-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="47bdb-139">S_OK</span></span> 
  
> <span data-ttu-id="47bdb-140">登録に成功しました。</span><span class="sxs-lookup"><span data-stu-id="47bdb-140">The registration was successful.</span></span>
    
<span data-ttu-id="47bdb-141">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="47bdb-141">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="47bdb-142">_lな tryid_が指すエントリ識別子が有効なエントリ識別子を表していません。</span><span class="sxs-lookup"><span data-stu-id="47bdb-142">The entry identifier pointed to by  _lpEntryID_ does not represent a valid entry identifier.</span></span> 
    
<span data-ttu-id="47bdb-143">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="47bdb-143">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="47bdb-144">_lな tryid_で指定されたエントリ識別子を担当するサービスプロバイダーは、 _uleventmask_パラメーターで指定されたイベントの種類をサポートしていないか、または通知をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="47bdb-144">The service provider responsible for the entry identifier pointed to by  _lpEntryID_ either does not support the type of events specified in the  _ulEventMask_ parameter or does not support notification.</span></span> 
    
<span data-ttu-id="47bdb-145">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="47bdb-145">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="47bdb-146">_lな tryid_で示されるエントリ識別子は、プロファイル内のどのサービスプロバイダーでも処理できません。</span><span class="sxs-lookup"><span data-stu-id="47bdb-146">The entry identifier pointed to by  _lpEntryID_ cannot be handled by any of the service providers in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="47bdb-147">注釈</span><span class="sxs-lookup"><span data-stu-id="47bdb-147">Remarks</span></span>

<span data-ttu-id="47bdb-148">**imapisession:: アドバイズ**メソッドは、呼び出し元のアドバイズシンクオブジェクト、セッション、およびサービスプロバイダーの間の接続を確立します。</span><span class="sxs-lookup"><span data-stu-id="47bdb-148">The **IMAPISession::Advise** method establishes a connection between the caller's advise sink object, the session and, optionally, a service provider.</span></span> <span data-ttu-id="47bdb-149">この接続は、 _uleventmask_パラメーターで指定された1つ以上のイベントが、 _lな tryid_によって参照されるオブジェクトに対して発生したときに、アドバイズシンクに通知を送信するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="47bdb-149">This connection is used to send notifications to the advise sink when one or more events specified in the  _ulEventMask_ parameter occur to the object pointed to by  _lpEntryID_.</span></span> <span data-ttu-id="47bdb-150">_lare tryid_が NULL の場合、ターゲットオブジェクトはセッションで、重大なエラーと拡張イベントに対してのみ通知が送信されます。</span><span class="sxs-lookup"><span data-stu-id="47bdb-150">When  _lpEntryID_ is NULL, the target object is the session and notifications are sent only for critical errors and extended events.</span></span> 
  
<span data-ttu-id="47bdb-151">_lpentryid_が有効なエントリ識別子を指している場合、MAPI は、責任のあるサービスプロバイダーに属するログオンオブジェクトの**アドバイズ**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="47bdb-151">When  _lpEntryID_ points to a valid entry identifier, MAPI calls the **Advise** method of the logon object that belongs to the responsible service provider.</span></span> <span data-ttu-id="47bdb-152">たとえば、lIABLogon _tryid_が配布リストのエントリ識別子を指す場合、MAPI は適切なアドレス帳プロバイダーの[:: Advise](iablogon-advise.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="47bdb-152">For example, if  _lpEntryID_ points to the entry identifier of a distribution list, MAPI calls the appropriate address book provider's [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
<span data-ttu-id="47bdb-153">通知を送信するために、サービスプロバイダーまたは MAPI は、登録されているアドバイズシンクの[IMAPIAdviseSink:: onnotify](imapiadvisesink-onnotify.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="47bdb-153">To send a notification, either the service provider or MAPI calls the registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="47bdb-154">**onnotify**へのパラメーターの1つは通知構造で、特定のイベントを説明する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="47bdb-154">One of the parameters to **OnNotify**, a notification structure, contains information that describes the specific event.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="47bdb-155">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="47bdb-155">Notes to callers</span></span>

<span data-ttu-id="47bdb-156">複数の実行スレッドをサポートするシステムでは、 **onnotify**への呼び出しは任意のスレッドでいつでも発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="47bdb-156">On systems that support multiple threads of execution, the call to **OnNotify** can also occur on any thread at any time.</span></span> <span data-ttu-id="47bdb-157">特定のスレッドの特定の時点でのみ通知が発生することを保証する必要がある場合は、 [HrThisThreadAdviseSink](hrthisthreadadvisesink.md)関数を呼び出して、**アドバイズ**メソッドに渡すアドバイズシンクオブジェクトを生成します。</span><span class="sxs-lookup"><span data-stu-id="47bdb-157">If you need assurance that notifications will occur only at a particular time on a particular thread, call the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to generate the advise sink object that you pass to the **Advise** method.</span></span> 
  
<span data-ttu-id="47bdb-158">クライアントがいつログオフしたかを確認するには、 _lcbEntryID tryid_を\*\*\*\* NULL に設定し、 __ を0に設定して、サービスプロバイダーに通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="47bdb-158">To determine when a client has logged off, register for notifications in your service provider by calling **Advise** with  _lpEntryID_ set to NULL and  _cbEntryID_ set to 0.</span></span> <span data-ttu-id="47bdb-159">ログオフが発生すると、fnevExtended 通知が表示されます。</span><span class="sxs-lookup"><span data-stu-id="47bdb-159">When the logoff occurs, you will receive an fnevExtended notification.</span></span> 
  
<span data-ttu-id="47bdb-160">**アドバイズ**の呼び出しが成功し、 [imapisession::](imapisession-unadvise.md)登録をキャンセルする前に、アドバイズシンクを呼び出した後、特定の長期間使用しない限り、アドバイズシンクオブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="47bdb-160">After a call to **Advise** has succeeded and before [IMAPISession::Unadvise](imapisession-unadvise.md) has been called to cancel the registration, release your advise sink object unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="47bdb-161">通知プロセスの概要については、「 [MAPI でのイベント通知](event-notification-in-mapi.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="47bdb-161">For an overview of the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="47bdb-162">通知の処理の詳細については、「[通知の処理](handling-notifications.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="47bdb-162">For more information about handling notifications, see [Handling Notifications](handling-notifications.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="47bdb-163">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="47bdb-163">MFCMAPI reference</span></span>

<span data-ttu-id="47bdb-164">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="47bdb-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="47bdb-165">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="47bdb-165">**File**</span></span>|<span data-ttu-id="47bdb-166">**関数**</span><span class="sxs-lookup"><span data-stu-id="47bdb-166">**Function**</span></span>|<span data-ttu-id="47bdb-167">**コメント**</span><span class="sxs-lookup"><span data-stu-id="47bdb-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="47bdb-168">basedialog</span><span class="sxs-lookup"><span data-stu-id="47bdb-168">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="47bdb-169">cbasedialog:: onnotificationson</span><span class="sxs-lookup"><span data-stu-id="47bdb-169">CBaseDialog::OnNotificationsOn</span></span>  <br/> |<span data-ttu-id="47bdb-170">mfcmapi は、 **imapisession:: アドバイズ**メソッドを使用して、セッションに対する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="47bdb-170">MFCMAPI uses the **IMAPISession::Advise** method to register for notifications against the session.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="47bdb-171">関連項目</span><span class="sxs-lookup"><span data-stu-id="47bdb-171">See also</span></span>



[<span data-ttu-id="47bdb-172">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="47bdb-172">IABLogon::Advise</span></span>](iablogon-advise.md)
  
[<span data-ttu-id="47bdb-173">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="47bdb-173">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="47bdb-174">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="47bdb-174">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="47bdb-175">IMAPISession::Unadvise</span><span class="sxs-lookup"><span data-stu-id="47bdb-175">IMAPISession::Unadvise</span></span>](imapisession-unadvise.md)
  
[<span data-ttu-id="47bdb-176">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="47bdb-176">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


<span data-ttu-id="47bdb-177">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="47bdb-177">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="47bdb-178">MAPI のイベント通知</span><span class="sxs-lookup"><span data-stu-id="47bdb-178">Event Notification in MAPI</span></span>](event-notification-in-mapi.md)

