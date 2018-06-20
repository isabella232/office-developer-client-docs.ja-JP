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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 45033ab924dcf443e9d231b3a7b4348119758935
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800692"
---
# <a name="imapisessionadvise"></a><span data-ttu-id="4eed2-103">IMAPISession::Advise</span><span class="sxs-lookup"><span data-stu-id="4eed2-103">IMAPISession::Advise</span></span>

  
  
<span data-ttu-id="4eed2-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4eed2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4eed2-105">セッションに影響を与える特定のイベントの通知を受け取ることを登録します。</span><span class="sxs-lookup"><span data-stu-id="4eed2-105">Registers to receive notification of specified events that affect the session.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="4eed2-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="4eed2-106">Parameters</span></span>

 <span data-ttu-id="4eed2-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="4eed2-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="4eed2-108">[in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="4eed2-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="4eed2-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="4eed2-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="4eed2-110">[in]アドレス帳またはメッセージ ストアのオブジェクトについては、通知を生成するか、またはセッションにのみ影響するイベントに関する通知を受信するクライアントを登録することを示す、NULL のエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4eed2-110">[in] A pointer to the entry identifier of the address book or message store object about which notifications should be generated, or NULL, which indicates that the client is registering to receive notifications about events that affect only the session.</span></span> 
    
 <span data-ttu-id="4eed2-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="4eed2-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="4eed2-112">[in]クライアントに興味を持って登録に含めることが通知イベントの種類を示す値のマスク。</span><span class="sxs-lookup"><span data-stu-id="4eed2-112">[in] A mask of values that indicate the types of notification events that the client is interested in and should be included in the registration.</span></span> <span data-ttu-id="4eed2-113">_LpEntryID_が NULL の場合は、MAPI セッションのみに影響する重大なエラー イベントのためにクライアントを自動的に登録します。</span><span class="sxs-lookup"><span data-stu-id="4eed2-113">If  _lpEntryID_ is NULL, MAPI automatically registers the client for critical error events that affect only the session.</span></span> <span data-ttu-id="4eed2-114">_LpEntryID_は、エントリ id をポイントしているときに次の値は、 _ulEventMask_パラメーターに有効です。</span><span class="sxs-lookup"><span data-stu-id="4eed2-114">When  _lpEntryID_ points to an entry identifier, the following values are valid for the  _ulEventMask_ parameter:</span></span> 
    
<span data-ttu-id="4eed2-115">fnevCriticalError</span><span class="sxs-lookup"><span data-stu-id="4eed2-115">fnevCriticalError</span></span> 
  
> <span data-ttu-id="4eed2-116">メモリ不足などの重大なエラーに関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="4eed2-116">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
<span data-ttu-id="4eed2-117">fnevExtended</span><span class="sxs-lookup"><span data-stu-id="4eed2-117">fnevExtended</span></span> 
  
> <span data-ttu-id="4eed2-118">レジスタの特定のアドレス帳またはメッセージに特定のイベントに関する通知では、プロバイダーを格納し、セッションのシャット ダウンします。</span><span class="sxs-lookup"><span data-stu-id="4eed2-118">Registers for notifications about events specific to a particular address book or message store provider and about session shut down.</span></span>
    
<span data-ttu-id="4eed2-119">fnevNewMail</span><span class="sxs-lookup"><span data-stu-id="4eed2-119">fnevNewMail</span></span> 
  
> <span data-ttu-id="4eed2-120">新しいメッセージの到着の通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="4eed2-120">Registers for notifications about the arrival of new messages.</span></span> 
    
<span data-ttu-id="4eed2-121">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="4eed2-121">fnevObjectCreated</span></span> 
  
> <span data-ttu-id="4eed2-122">新しいオブジェクトの作成についての通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="4eed2-122">Registers for notifications about the creation of a new object.</span></span>
    
<span data-ttu-id="4eed2-123">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="4eed2-123">fnevObjectCopied</span></span>
  
> <span data-ttu-id="4eed2-124">コピーされているオブジェクトについての通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="4eed2-124">Registers for notifications about an object being copied.</span></span>
    
<span data-ttu-id="4eed2-125">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="4eed2-125">fnevObjectDeleted</span></span>
  
> <span data-ttu-id="4eed2-126">削除されているオブジェクトについての通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="4eed2-126">Registers for notifications about an object being deleted.</span></span>
    
<span data-ttu-id="4eed2-127">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="4eed2-127">fnevObjectModified</span></span>
  
> <span data-ttu-id="4eed2-128">変更されているオブジェクトについての通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="4eed2-128">Registers for notifications about an object being modified.</span></span>
    
<span data-ttu-id="4eed2-129">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="4eed2-129">fnevObjectMoved</span></span>
  
> <span data-ttu-id="4eed2-130">移動されるオブジェクトについての通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="4eed2-130">Registers for notifications about an object being moved.</span></span>
    
<span data-ttu-id="4eed2-131">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="4eed2-131">fnevSearchComplete</span></span>
  
> <span data-ttu-id="4eed2-132">検索操作の完了に関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="4eed2-132">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="4eed2-133">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="4eed2-133">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="4eed2-134">[in]後続の通知を受信するアドバイズ シンク オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="4eed2-134">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="4eed2-135">このアドバイズ シンク オブジェクトは既に割り当てられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="4eed2-135">This advise sink object must have already been allocated.</span></span>
    
 <span data-ttu-id="4eed2-136">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="4eed2-136">_lpulConnection_</span></span>
  
> <span data-ttu-id="4eed2-137">[out]呼び出し元の間の接続を表す数値を 0 以外の値へのポインターでは、シンク オブジェクトとのセッションを案内します。</span><span class="sxs-lookup"><span data-stu-id="4eed2-137">[out] A pointer to a nonzero number that represents the connection between the caller's advise sink object and the session.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4eed2-138">�߂�l</span><span class="sxs-lookup"><span data-stu-id="4eed2-138">Return value</span></span>

<span data-ttu-id="4eed2-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="4eed2-139">S_OK</span></span> 
  
> <span data-ttu-id="4eed2-140">登録が正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="4eed2-140">The registration was successful.</span></span>
    
<span data-ttu-id="4eed2-141">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="4eed2-141">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="4eed2-142">_LpEntryID_で指定されたエントリの識別子は有効なエントリの識別子ではありません。</span><span class="sxs-lookup"><span data-stu-id="4eed2-142">The entry identifier pointed to by  _lpEntryID_ does not represent a valid entry identifier.</span></span> 
    
<span data-ttu-id="4eed2-143">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="4eed2-143">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="4eed2-144">_LpEntryID_で指定されたエントリの識別子を担当するサービス プロバイダーは、 _ulEventMask_パラメーターで指定したイベントの種類をサポートしていないか、または通知をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="4eed2-144">The service provider responsible for the entry identifier pointed to by  _lpEntryID_ either does not support the type of events specified in the  _ulEventMask_ parameter or does not support notification.</span></span> 
    
<span data-ttu-id="4eed2-145">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="4eed2-145">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="4eed2-146">_LpEntryID_で指定されたエントリの識別子は、プロファイル内のサービス プロバイダーのいずれかが処理できません。</span><span class="sxs-lookup"><span data-stu-id="4eed2-146">The entry identifier pointed to by  _lpEntryID_ cannot be handled by any of the service providers in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4eed2-147">備考</span><span class="sxs-lookup"><span data-stu-id="4eed2-147">Remarks</span></span>

<span data-ttu-id="4eed2-148">**IMAPISession::Advise**メソッドでは、シンク オブジェクト、セッション、および必要に応じて、サービス プロバイダーにアドバイスの呼び出し元の間の接続を確立します。</span><span class="sxs-lookup"><span data-stu-id="4eed2-148">The **IMAPISession::Advise** method establishes a connection between the caller's advise sink object, the session and, optionally, a service provider.</span></span> <span data-ttu-id="4eed2-149">この接続を使用していずれかのアドバイズ シンクに通知を送信するか、 _lpEntryID_が指すオブジェクトに、 _ulEventMask_パラメーターで指定されたその他のイベントが発生します。</span><span class="sxs-lookup"><span data-stu-id="4eed2-149">This connection is used to send notifications to the advise sink when one or more events specified in the  _ulEventMask_ parameter occur to the object pointed to by  _lpEntryID_.</span></span> <span data-ttu-id="4eed2-150">_LpEntryID_が NULL の場合は、ターゲット オブジェクトは、セッションとのみ、重大なエラー、および拡張イベントの通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="4eed2-150">When  _lpEntryID_ is NULL, the target object is the session and notifications are sent only for critical errors and extended events.</span></span> 
  
<span data-ttu-id="4eed2-151">_LpEntryID_は、有効なエントリの識別子をポイントしている場合、MAPI は、**担当のサービス プロバイダーに属しているログオン オブジェクトのメソッド**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4eed2-151">When  _lpEntryID_ points to a valid entry identifier, MAPI calls the **Advise** method of the logon object that belongs to the responsible service provider.</span></span> <span data-ttu-id="4eed2-152">などの_lpEntryID_は、配布リストのエントリ id をポイントしている場合、MAPI は、適切なアドレス帳プロバイダーの[IABLogon::Advise](iablogon-advise.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4eed2-152">For example, if  _lpEntryID_ points to the entry identifier of a distribution list, MAPI calls the appropriate address book provider's [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
<span data-ttu-id="4eed2-153">通知を送信するには、サービス プロバイダーまたは MAPI のいずれかが登録されているアドバイズ シンクの[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4eed2-153">To send a notification, either the service provider or MAPI calls the registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="4eed2-154">**OnNotify**通知の構造体をパラメーターの 1 つには、特定のイベントを説明する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4eed2-154">One of the parameters to **OnNotify**, a notification structure, contains information that describes the specific event.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="4eed2-155">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="4eed2-155">Notes to callers</span></span>

<span data-ttu-id="4eed2-156">システムでは複数の実行スレッドをサポートする、 **OnNotify**への呼び出しも発生することが任意のスレッドで任意の時点。</span><span class="sxs-lookup"><span data-stu-id="4eed2-156">On systems that support multiple threads of execution, the call to **OnNotify** can also occur on any thread at any time.</span></span> <span data-ttu-id="4eed2-157">特定のスレッドで特定の時刻にのみ通知が発生する保証が必要な場合は、**メソッド**に渡すアドバイズ シンク オブジェクトを生成する[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4eed2-157">If you need assurance that notifications will occur only at a particular time on a particular thread, call the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to generate the advise sink object that you pass to the **Advise** method.</span></span> 
  
<span data-ttu-id="4eed2-158">調べるには、クライアントからログオフしたとき、 _lpEntryID_を NULL に設定され_cbEntryID_を 0 に設定の**アドバイス**を呼び出すことによって、サービス ・ プロバイダーに通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="4eed2-158">To determine when a client has logged off, register for notifications in your service provider by calling **Advise** with  _lpEntryID_ set to NULL and  _cbEntryID_ set to 0.</span></span> <span data-ttu-id="4eed2-159">ログオフが発生すると、fnevExtended 通知を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="4eed2-159">When the logoff occurs, you will receive an fnevExtended notification.</span></span> 
  
<span data-ttu-id="4eed2-160">**Advise**への呼び出しが成功した後、登録をキャンセルするのには[IMAPISession::Unadvise](imapisession-unadvise.md)前に、特定の長期的な使用がない限り、アドバイズ シンク オブジェクトを放します。</span><span class="sxs-lookup"><span data-stu-id="4eed2-160">After a call to **Advise** has succeeded and before [IMAPISession::Unadvise](imapisession-unadvise.md) has been called to cancel the registration, release your advise sink object unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="4eed2-161">通知の処理の概要については、 [MAPI でのイベントの通知](event-notification-in-mapi.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4eed2-161">For an overview of the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="4eed2-162">通知の処理の詳細については、[通知の処理](handling-notifications.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4eed2-162">For more information about handling notifications, see [Handling Notifications](handling-notifications.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4eed2-163">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="4eed2-163">MFCMAPI reference</span></span>

<span data-ttu-id="4eed2-164">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="4eed2-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4eed2-165">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="4eed2-165">**File**</span></span>|<span data-ttu-id="4eed2-166">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="4eed2-166">**Function**</span></span>|<span data-ttu-id="4eed2-167">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="4eed2-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4eed2-168">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="4eed2-168">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="4eed2-169">CBaseDialog::OnNotificationsOn</span><span class="sxs-lookup"><span data-stu-id="4eed2-169">CBaseDialog::OnNotificationsOn</span></span>  <br/> |<span data-ttu-id="4eed2-170">MFCMAPI では、 **IMAPISession::Advise**メソッドを使用して、セッションに対して通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="4eed2-170">MFCMAPI uses the **IMAPISession::Advise** method to register for notifications against the session.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4eed2-171">関連項目</span><span class="sxs-lookup"><span data-stu-id="4eed2-171">See also</span></span>



[<span data-ttu-id="4eed2-172">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="4eed2-172">IABLogon::Advise</span></span>](iablogon-advise.md)
  
[<span data-ttu-id="4eed2-173">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="4eed2-173">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="4eed2-174">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="4eed2-174">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="4eed2-175">IMAPISession::Unadvise</span><span class="sxs-lookup"><span data-stu-id="4eed2-175">IMAPISession::Unadvise</span></span>](imapisession-unadvise.md)
  
[<span data-ttu-id="4eed2-176">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="4eed2-176">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


<span data-ttu-id="4eed2-177">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="4eed2-177">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="4eed2-178">MAPI でのイベントの通知</span><span class="sxs-lookup"><span data-stu-id="4eed2-178">Event Notification in MAPI</span></span>](event-notification-in-mapi.md)

