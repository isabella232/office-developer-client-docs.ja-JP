---
title: IMAPISessionAdvise
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
# <a name="imapisessionadvise"></a><span data-ttu-id="b59c4-103">IMAPISession::Advise</span><span class="sxs-lookup"><span data-stu-id="b59c4-103">IMAPISession::Advise</span></span>

  
  
<span data-ttu-id="b59c4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b59c4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b59c4-105">セッションに影響を与える指定されたイベントの通知を受信するために登録します。</span><span class="sxs-lookup"><span data-stu-id="b59c4-105">Registers to receive notification of specified events that affect the session.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="b59c4-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b59c4-106">Parameters</span></span>

 <span data-ttu-id="b59c4-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="b59c4-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="b59c4-108">[in]  _lpEntryID_ パラメーターが指すエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="b59c4-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="b59c4-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="b59c4-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="b59c4-110">[in]生成する必要がある通知に関するアドレス帳またはメッセージ ストア オブジェクトのエントリ識別子へのポインター、または NULL 。これは、クライアントがセッションにのみ影響を与えるイベントに関する通知を受信するために登録中です。</span><span class="sxs-lookup"><span data-stu-id="b59c4-110">[in] A pointer to the entry identifier of the address book or message store object about which notifications should be generated, or NULL, which indicates that the client is registering to receive notifications about events that affect only the session.</span></span> 
    
 <span data-ttu-id="b59c4-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="b59c4-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="b59c4-112">[in]クライアントが関心を持ち、登録に含める必要がある通知イベントの種類を示す値のマスク。</span><span class="sxs-lookup"><span data-stu-id="b59c4-112">[in] A mask of values that indicate the types of notification events that the client is interested in and should be included in the registration.</span></span> <span data-ttu-id="b59c4-113">_lpEntryID が_ NULL の場合、MAPI はセッションにのみ影響する重大なエラー イベントのためにクライアントを自動的に登録します。</span><span class="sxs-lookup"><span data-stu-id="b59c4-113">If  _lpEntryID_ is NULL, MAPI automatically registers the client for critical error events that affect only the session.</span></span> <span data-ttu-id="b59c4-114">_lpEntryID が_ エントリ識別子をポイントすると _、ulEventMask_ パラメーターに対して次の値が有効になります。</span><span class="sxs-lookup"><span data-stu-id="b59c4-114">When  _lpEntryID_ points to an entry identifier, the following values are valid for the  _ulEventMask_ parameter:</span></span> 
    
<span data-ttu-id="b59c4-115">fnevCriticalError</span><span class="sxs-lookup"><span data-stu-id="b59c4-115">fnevCriticalError</span></span> 
  
> <span data-ttu-id="b59c4-116">メモリ不足などの重大なエラーに関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="b59c4-116">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
<span data-ttu-id="b59c4-117">fnevExtended</span><span class="sxs-lookup"><span data-stu-id="b59c4-117">fnevExtended</span></span> 
  
> <span data-ttu-id="b59c4-118">特定のアドレス帳またはメッセージ ストア プロバイダーに固有のイベントとセッションのシャットダウンに関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="b59c4-118">Registers for notifications about events specific to a particular address book or message store provider and about session shut down.</span></span>
    
<span data-ttu-id="b59c4-119">fnevNewMail</span><span class="sxs-lookup"><span data-stu-id="b59c4-119">fnevNewMail</span></span> 
  
> <span data-ttu-id="b59c4-120">新しいメッセージの到着に関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="b59c4-120">Registers for notifications about the arrival of new messages.</span></span> 
    
<span data-ttu-id="b59c4-121">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="b59c4-121">fnevObjectCreated</span></span> 
  
> <span data-ttu-id="b59c4-122">新しいオブジェクトの作成に関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="b59c4-122">Registers for notifications about the creation of a new object.</span></span>
    
<span data-ttu-id="b59c4-123">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="b59c4-123">fnevObjectCopied</span></span>
  
> <span data-ttu-id="b59c4-124">コピーするオブジェクトに関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="b59c4-124">Registers for notifications about an object being copied.</span></span>
    
<span data-ttu-id="b59c4-125">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="b59c4-125">fnevObjectDeleted</span></span>
  
> <span data-ttu-id="b59c4-126">削除するオブジェクトに関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="b59c4-126">Registers for notifications about an object being deleted.</span></span>
    
<span data-ttu-id="b59c4-127">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="b59c4-127">fnevObjectModified</span></span>
  
> <span data-ttu-id="b59c4-128">変更するオブジェクトに関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="b59c4-128">Registers for notifications about an object being modified.</span></span>
    
<span data-ttu-id="b59c4-129">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="b59c4-129">fnevObjectMoved</span></span>
  
> <span data-ttu-id="b59c4-130">移動するオブジェクトに関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="b59c4-130">Registers for notifications about an object being moved.</span></span>
    
<span data-ttu-id="b59c4-131">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="b59c4-131">fnevSearchComplete</span></span>
  
> <span data-ttu-id="b59c4-132">検索操作の完了に関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="b59c4-132">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="b59c4-133">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="b59c4-133">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="b59c4-134">[in]後続の通知を受信するアアドバイス シンク オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="b59c4-134">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="b59c4-135">このアアドバイス シンク オブジェクトは既に割り当てられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b59c4-135">This advise sink object must have already been allocated.</span></span>
    
 <span data-ttu-id="b59c4-136">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="b59c4-136">_lpulConnection_</span></span>
  
> <span data-ttu-id="b59c4-137">[out]呼び出し元の通知シンク オブジェクトとセッションの間の接続を表す 0 以外の数値へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b59c4-137">[out] A pointer to a nonzero number that represents the connection between the caller's advise sink object and the session.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b59c4-138">戻り値</span><span class="sxs-lookup"><span data-stu-id="b59c4-138">Return value</span></span>

<span data-ttu-id="b59c4-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="b59c4-139">S_OK</span></span> 
  
> <span data-ttu-id="b59c4-140">登録が成功しました。</span><span class="sxs-lookup"><span data-stu-id="b59c4-140">The registration was successful.</span></span>
    
<span data-ttu-id="b59c4-141">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="b59c4-141">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="b59c4-142">_lpEntryID_ が指すエントリ識別子は、有効なエントリ識別子を表すではありません。</span><span class="sxs-lookup"><span data-stu-id="b59c4-142">The entry identifier pointed to by  _lpEntryID_ does not represent a valid entry identifier.</span></span> 
    
<span data-ttu-id="b59c4-143">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="b59c4-143">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="b59c4-144">_lpEntryID_ が指すエントリ識別子を担当するサービス プロバイダーは _、ulEventMask_ パラメーターで指定されたイベントの種類をサポートしていないか、通知をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="b59c4-144">The service provider responsible for the entry identifier pointed to by  _lpEntryID_ either does not support the type of events specified in the  _ulEventMask_ parameter or does not support notification.</span></span> 
    
<span data-ttu-id="b59c4-145">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="b59c4-145">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="b59c4-146">_lpEntryID_ が指すエントリ識別子は、プロファイル内のサービス プロバイダーでは処理できません。</span><span class="sxs-lookup"><span data-stu-id="b59c4-146">The entry identifier pointed to by  _lpEntryID_ cannot be handled by any of the service providers in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b59c4-147">注釈</span><span class="sxs-lookup"><span data-stu-id="b59c4-147">Remarks</span></span>

<span data-ttu-id="b59c4-148">**IMAPISession::Advise** メソッドは、呼び出し元のアアドバイス シンク オブジェクト、セッション、およびオプションでサービス プロバイダー間の接続を確立します。</span><span class="sxs-lookup"><span data-stu-id="b59c4-148">The **IMAPISession::Advise** method establishes a connection between the caller's advise sink object, the session and, optionally, a service provider.</span></span> <span data-ttu-id="b59c4-149">この接続は  _、ulEventMask_ パラメーターで指定された 1 つ以上のイベントが  _lpEntryID_ によって指されるオブジェクトに発生した場合に、アアドバイス シンクに通知を送信するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b59c4-149">This connection is used to send notifications to the advise sink when one or more events specified in the  _ulEventMask_ parameter occur to the object pointed to by  _lpEntryID_.</span></span> <span data-ttu-id="b59c4-150">_lpEntryID が_ NULL の場合、ターゲット オブジェクトはセッションであり、重大なエラーと拡張イベントに対してだけ通知が送信されます。</span><span class="sxs-lookup"><span data-stu-id="b59c4-150">When  _lpEntryID_ is NULL, the target object is the session and notifications are sent only for critical errors and extended events.</span></span> 
  
<span data-ttu-id="b59c4-151">_lpEntryID が有効_ なエントリ識別子をポイントすると、MAPI は責任あるサービス プロバイダーに属するログオン オブジェクトの **Advise** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b59c4-151">When  _lpEntryID_ points to a valid entry identifier, MAPI calls the **Advise** method of the logon object that belongs to the responsible service provider.</span></span> <span data-ttu-id="b59c4-152">たとえば  _、lpEntryID_ が配布リストのエントリ識別子をポイントする場合、MAPI は適切なアドレス帳プロバイダーの [IABLogon::Advise メソッドを呼び出](iablogon-advise.md) します。</span><span class="sxs-lookup"><span data-stu-id="b59c4-152">For example, if  _lpEntryID_ points to the entry identifier of a distribution list, MAPI calls the appropriate address book provider's [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
<span data-ttu-id="b59c4-153">通知を送信するには、サービス プロバイダーまたは MAPI が登録されているアアドバイス シンクの [IMAPIAdviseSink::OnNotify メソッドを呼び出](imapiadvisesink-onnotify.md) します。</span><span class="sxs-lookup"><span data-stu-id="b59c4-153">To send a notification, either the service provider or MAPI calls the registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="b59c4-154">通知構造である **OnNotify** のパラメーターの 1 つには、特定のイベントを記述する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b59c4-154">One of the parameters to **OnNotify**, a notification structure, contains information that describes the specific event.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="b59c4-155">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="b59c4-155">Notes to callers</span></span>

<span data-ttu-id="b59c4-156">複数の実行スレッドをサポートするシステムでは **、OnNotify** の呼び出しは、任意のスレッドでもいつでも実行できます。</span><span class="sxs-lookup"><span data-stu-id="b59c4-156">On systems that support multiple threads of execution, the call to **OnNotify** can also occur on any thread at any time.</span></span> <span data-ttu-id="b59c4-157">通知が特定のスレッド上の特定の時間にのみ発生する保証が必要な場合は [、HrThisThreadAdviseSink](hrthisthreadadvisesink.md) 関数を呼び出して **、Advise** メソッドに渡すアアドバイス シンク オブジェクトを生成します。</span><span class="sxs-lookup"><span data-stu-id="b59c4-157">If you need assurance that notifications will occur only at a particular time on a particular thread, call the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to generate the advise sink object that you pass to the **Advise** method.</span></span> 
  
<span data-ttu-id="b59c4-158">クライアントがログオフした時間を確認するには、lpEntryID を NULLに設定し _、cbEntryID_ を 0 に設定して、サービス プロバイダーに通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="b59c4-158">To determine when a client has logged off, register for notifications in your service provider by calling **Advise** with  _lpEntryID_ set to NULL and  _cbEntryID_ set to 0.</span></span> <span data-ttu-id="b59c4-159">ログオフが発生すると、fnevExtended 通知が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b59c4-159">When the logoff occurs, you will receive an fnevExtended notification.</span></span> 
  
<span data-ttu-id="b59c4-160">**Advise** の呼び出しが成功した後 [、IMAPISession::Unadvise](imapisession-unadvise.md)が呼び出され、登録を取り消す前に、特定の長期的な使用がない限り、アアドバイス シンク オブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="b59c4-160">After a call to **Advise** has succeeded and before [IMAPISession::Unadvise](imapisession-unadvise.md) has been called to cancel the registration, release your advise sink object unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="b59c4-161">通知プロセスの概要については、「MAPI の [イベント通知」を参照してください](event-notification-in-mapi.md)。</span><span class="sxs-lookup"><span data-stu-id="b59c4-161">For an overview of the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="b59c4-162">通知の処理の詳細については、「通知の処理」 [を参照してください](handling-notifications.md)。</span><span class="sxs-lookup"><span data-stu-id="b59c4-162">For more information about handling notifications, see [Handling Notifications](handling-notifications.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b59c4-163">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="b59c4-163">MFCMAPI reference</span></span>

<span data-ttu-id="b59c4-164">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b59c4-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b59c4-165">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="b59c4-165">**File**</span></span>|<span data-ttu-id="b59c4-166">**関数**</span><span class="sxs-lookup"><span data-stu-id="b59c4-166">**Function**</span></span>|<span data-ttu-id="b59c4-167">**コメント**</span><span class="sxs-lookup"><span data-stu-id="b59c4-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b59c4-168">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="b59c4-168">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="b59c4-169">CBaseDialog::OnNotificationsOn</span><span class="sxs-lookup"><span data-stu-id="b59c4-169">CBaseDialog::OnNotificationsOn</span></span>  <br/> |<span data-ttu-id="b59c4-170">MFCMAPI は **IMAPISession::Advise** メソッドを使用して、セッションに対する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="b59c4-170">MFCMAPI uses the **IMAPISession::Advise** method to register for notifications against the session.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b59c4-171">関連項目</span><span class="sxs-lookup"><span data-stu-id="b59c4-171">See also</span></span>



[<span data-ttu-id="b59c4-172">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="b59c4-172">IABLogon::Advise</span></span>](iablogon-advise.md)
  
[<span data-ttu-id="b59c4-173">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="b59c4-173">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="b59c4-174">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="b59c4-174">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="b59c4-175">IMAPISession::Unadvise</span><span class="sxs-lookup"><span data-stu-id="b59c4-175">IMAPISession::Unadvise</span></span>](imapisession-unadvise.md)
  
[<span data-ttu-id="b59c4-176">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b59c4-176">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


<span data-ttu-id="b59c4-177">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="b59c4-177">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="b59c4-178">MAPI のイベント通知</span><span class="sxs-lookup"><span data-stu-id="b59c4-178">Event Notification in MAPI</span></span>](event-notification-in-mapi.md)

