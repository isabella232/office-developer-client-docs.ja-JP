---
title: IMAPITableAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Advise
api_type:
- COM
ms.assetid: e8b5d21e-dc14-4b61-96b3-a51bcfa0d232
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 781146193748cdd9408a3320e90a73a070ced2af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800835"
---
# <a name="imapitableadvise"></a><span data-ttu-id="271e9-103">IMAPITable::Advise</span><span class="sxs-lookup"><span data-stu-id="271e9-103">IMAPITable::Advise</span></span>

  
  
<span data-ttu-id="271e9-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="271e9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="271e9-105">テーブルに影響を与えず、指定されたイベントの通知を受信するアドバイズ シンク オブジェクトを登録します。</span><span class="sxs-lookup"><span data-stu-id="271e9-105">Registers an advise sink object to receive notification of specified events affecting the table.</span></span>
  
```cpp
HRESULT Advise(
ULONG ulEventMask,
LPMAPIADVISESINK lpAdviseSink,
ULONG_PTR FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="271e9-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="271e9-106">Parameters</span></span>

 <span data-ttu-id="271e9-107">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="271e9-107">_ulEventMask_</span></span>
  
> <span data-ttu-id="271e9-108">[in]通知を生成するイベントの種類を示す値です。</span><span class="sxs-lookup"><span data-stu-id="271e9-108">[in] Value indicating the type of event that will generate the notification.</span></span> <span data-ttu-id="271e9-109">次の値だけでは有効です。</span><span class="sxs-lookup"><span data-stu-id="271e9-109">Only the following value is valid:</span></span>
    
 `fnevTableModified`
  
 <span data-ttu-id="271e9-110">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="271e9-110">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="271e9-111">[in]後続の通知を受信するアドバイズ シンク オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="271e9-111">[in] Pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="271e9-112">このアドバイズ シンク オブジェクトする必要があります既に割り当てられています。</span><span class="sxs-lookup"><span data-stu-id="271e9-112">This advise sink object must have been already allocated.</span></span>
    
 <span data-ttu-id="271e9-113">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="271e9-113">_lpulConnection_</span></span>
  
> <span data-ttu-id="271e9-114">[out]成功した通知の登録を表す、0 以外の値へのポインター。</span><span class="sxs-lookup"><span data-stu-id="271e9-114">[out] Pointer to a nonzero value that represents the successful notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="271e9-115">�߂�l</span><span class="sxs-lookup"><span data-stu-id="271e9-115">Return value</span></span>

<span data-ttu-id="271e9-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="271e9-116">S_OK</span></span> 
  
> <span data-ttu-id="271e9-117">通知の登録が正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="271e9-117">The notification registration successfully completed.</span></span>
    
<span data-ttu-id="271e9-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="271e9-118">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="271e9-119">テーブルの実装は、その行と列への変更をサポートしていませんか、または通知をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="271e9-119">The table implementation either does not support changes to its rows and columns or does not support notification.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="271e9-120">注釈</span><span class="sxs-lookup"><span data-stu-id="271e9-120">Remarks</span></span>

<span data-ttu-id="271e9-121">通知コールバックのプロバイダーに実装されている table オブジェクトを登録するのには、 **IMAPITable::Advise**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="271e9-121">Use the **IMAPITable::Advise** method to register a table object implemented in the provider for notification callbacks.</span></span> <span data-ttu-id="271e9-122">Table オブジェクトに変更が発生するたびに、プロバイダーはどのようなイベント マスクのビットは、 _ulEventMask_パラメーターで設定された、つまりどのような種類の変更が発生したを確認します。</span><span class="sxs-lookup"><span data-stu-id="271e9-122">Whenever a change occurs to the table object, the provider checks to see what event mask bit was set in the  _ulEventMask_ parameter and thus what type of change occurred.</span></span> <span data-ttu-id="271e9-123">ビットが設定されている場合、プロバイダーはイベントを通知する_lpAdviseSink_パラメーターで指定されたアドバイズ シンク オブジェクトの[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出しますし。</span><span class="sxs-lookup"><span data-stu-id="271e9-123">If a bit is set, then the provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object indicated by the  _lpAdviseSink_ parameter to report the event.</span></span> <span data-ttu-id="271e9-124">**OnNotify**ルーチンに渡された通知の構造体のデータでは、イベントについて説明します。</span><span class="sxs-lookup"><span data-stu-id="271e9-124">Data passed in the notification structure to the **OnNotify** routine describes the event.</span></span> 
  
<span data-ttu-id="271e9-125">**OnNotify**への呼び出しは、オブジェクトを変更するための呼び出し時に、または時に、次に発生します。</span><span class="sxs-lookup"><span data-stu-id="271e9-125">The call to **OnNotify** can occur during the call that changes the object, or at any following time.</span></span> <span data-ttu-id="271e9-126">複数の実行スレッドをサポートしているシステムでは、任意のスレッドで**OnNotify**への呼び出しが発生します。</span><span class="sxs-lookup"><span data-stu-id="271e9-126">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="271e9-127">**OnNotify**を処理する方が安全であるいずれかに不適切な時点で可能性がある呼び出しを有効にする方法、プロバイダーは、 [HrThisThreadAdviseSink](hrthisthreadadvisesink.md)関数を使用してください。</span><span class="sxs-lookup"><span data-stu-id="271e9-127">For a way to turn a call to **OnNotify** that might happen at an inopportune time into one that is safer to handle, a provider should use the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="271e9-128">通知を提供するには、 _lpAdviseSink_へのポインターのコピーを保持するプロバイダーの実装**アドバイズ**ニーズにアドバイス シンク オブジェクトです。これを行うには、 [IMAPITable::Unadvise](imapitable-unadvise.md)メソッドを呼び出して、通知の登録をキャンセルするまで、オブジェクトを指すポインターを維持するためにアドバイズ シンクの**IUnknown::AddRef**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="271e9-128">To provide notifications, the provider implementing **Advise** needs to keep a copy of the pointer to the  _lpAdviseSink_ advise sink object; to do so, it calls the **IUnknown::AddRef** method for the advise sink to maintain its object pointer until notification registration is canceled with a call to the [IMAPITable::Unadvise](imapitable-unadvise.md) method.</span></span> <span data-ttu-id="271e9-129">**アドバイズ**実装する必要があります通知の登録に接続番号を割り当てるし、 _lpulConnection_パラメーターに返す前に、この接続の数で**AddRef**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="271e9-129">The **Advise** implementation should assign a connection number to the notification registration and call **AddRef** on this connection number before returning it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="271e9-130">まで接続数を解放する必要があります、登録がキャンセルされると、前に、サービス プロバイダーがアドバイズ シンク オブジェクトを解放できます * * Unadvise * * 呼び出されました。</span><span class="sxs-lookup"><span data-stu-id="271e9-130">Service providers can release the advise sink object before the registration is canceled, but they must not release the connection number until ** Unadvise ** has been called.</span></span> 
  
<span data-ttu-id="271e9-131">**Advise**への呼び出しが成功した後、および * * Unadvise * * が呼び出されると、クライアントおく必要がありますアドバイズ シンク オブジェクトを解放するのです。</span><span class="sxs-lookup"><span data-stu-id="271e9-131">After a call to **Advise** has succeeded and before ** Unadvise ** has been called, clients must be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="271e9-132">そのため、クライアントは**アドバイス**がない限り、特定の長期的な使用の制御が戻った後、アドバイズ シンク オブジェクトをリリースしています。</span><span class="sxs-lookup"><span data-stu-id="271e9-132">A client should therefore release its advise sink object after **Advise** returns unless it has a specific long-term use for it.</span></span> 
  
<span data-ttu-id="271e9-133">非同期通知のため、テーブルの列の設定を変更する実装は、前の列の順序で構成情報を使用して通知を受信できます。</span><span class="sxs-lookup"><span data-stu-id="271e9-133">Because of the asynchronous behavior of notification, implementations that change table column settings can receive notifications with information organized in a previous column order.</span></span> <span data-ttu-id="271e9-134">など、コンテナーから削除されているメッセージのテーブルの行が返される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="271e9-134">For instance, a table row might be returned for a message that has just been deleted from the container.</span></span> <span data-ttu-id="271e9-135">列設定の変更が加えられたとそれに関する情報が送信されるが、まだ新しい情報を通知テーブルのビューが更新されていないときは、このような通知が送信されます。</span><span class="sxs-lookup"><span data-stu-id="271e9-135">Such a notification is sent when the column setting change has been made and information about it sent but the notification table view has not been updated with that information yet.</span></span>
  
<span data-ttu-id="271e9-136">通知プロセスの詳細については、 [MAPI でのイベントの通知](event-notification-in-mapi.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="271e9-136">For more information on the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="271e9-137">テーブル通知の詳細については、[テーブルについての通知](about-table-notifications.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="271e9-137">For specific information about table notification, see [About Table Notifications](about-table-notifications.md).</span></span> <span data-ttu-id="271e9-138">通知をサポートするために**IMAPISupport**メソッドを使用する方法の詳細については、[イベント通知のサポート](supporting-event-notification.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="271e9-138">For information about using the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="271e9-139">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="271e9-139">MFCMAPI reference</span></span>

<span data-ttu-id="271e9-140">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="271e9-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="271e9-141">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="271e9-141">**File**</span></span>|<span data-ttu-id="271e9-142">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="271e9-142">**Function**</span></span>|<span data-ttu-id="271e9-143">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="271e9-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="271e9-144">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="271e9-144">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="271e9-145">CContestTableListCtrl::NotificationOn</span><span class="sxs-lookup"><span data-stu-id="271e9-145">CContestTableListCtrl::NotificationOn</span></span>  <br/> |<span data-ttu-id="271e9-146">MFCMAPI では、 **IMAPITable::Advise**メソッドを使用して、常に最新情報を表形式ビューを許可する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="271e9-146">MFCMAPI uses the **IMAPITable::Advise** method to register for notifications to allow the table view to stay current.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="271e9-147">関連項目</span><span class="sxs-lookup"><span data-stu-id="271e9-147">See also</span></span>



[<span data-ttu-id="271e9-148">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="271e9-148">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="271e9-149">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="271e9-149">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="271e9-150">IMAPITable::Unadvise</span><span class="sxs-lookup"><span data-stu-id="271e9-150">IMAPITable::Unadvise</span></span>](imapitable-unadvise.md)
  
[<span data-ttu-id="271e9-151">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="271e9-151">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="271e9-152">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="271e9-152">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


<span data-ttu-id="271e9-153">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="271e9-153">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

