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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c9401c163c74ab303ec39c147e0432d1979426b8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418814"
---
# <a name="imapitableadvise"></a><span data-ttu-id="770e9-103">IMAPITable::Advise</span><span class="sxs-lookup"><span data-stu-id="770e9-103">IMAPITable::Advise</span></span>

  
  
<span data-ttu-id="770e9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="770e9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="770e9-105">アドバイズシンクオブジェクトを登録して、テーブルに影響を与える指定したイベントの通知を受信します。</span><span class="sxs-lookup"><span data-stu-id="770e9-105">Registers an advise sink object to receive notification of specified events affecting the table.</span></span>
  
```cpp
HRESULT Advise(
ULONG ulEventMask,
LPMAPIADVISESINK lpAdviseSink,
ULONG_PTR FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="770e9-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="770e9-106">Parameters</span></span>

 <span data-ttu-id="770e9-107">_uleventmask_</span><span class="sxs-lookup"><span data-stu-id="770e9-107">_ulEventMask_</span></span>
  
> <span data-ttu-id="770e9-108">順番通知を生成するイベントの種類を示す値です。</span><span class="sxs-lookup"><span data-stu-id="770e9-108">[in] Value indicating the type of event that will generate the notification.</span></span> <span data-ttu-id="770e9-109">有効な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="770e9-109">Only the following value is valid:</span></span>
    
 `fnevTableModified`
  
 <span data-ttu-id="770e9-110">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="770e9-110">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="770e9-111">順番後続の通知を受け取るアドバイズシンクオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="770e9-111">[in] Pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="770e9-112">このアドバイズシンクオブジェクトは、既に割り当てられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="770e9-112">This advise sink object must have been already allocated.</span></span>
    
 <span data-ttu-id="770e9-113">_lアウト接続_</span><span class="sxs-lookup"><span data-stu-id="770e9-113">_lpulConnection_</span></span>
  
> <span data-ttu-id="770e9-114">読み上げ正常な通知登録を表す0以外の値へのポインター。</span><span class="sxs-lookup"><span data-stu-id="770e9-114">[out] Pointer to a nonzero value that represents the successful notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="770e9-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="770e9-115">Return value</span></span>

<span data-ttu-id="770e9-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="770e9-116">S_OK</span></span> 
  
> <span data-ttu-id="770e9-117">通知の登録が正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="770e9-117">The notification registration successfully completed.</span></span>
    
<span data-ttu-id="770e9-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="770e9-118">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="770e9-119">テーブルの実装では、行と列の変更がサポートされていないか、通知をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="770e9-119">The table implementation either does not support changes to its rows and columns or does not support notification.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="770e9-120">注釈</span><span class="sxs-lookup"><span data-stu-id="770e9-120">Remarks</span></span>

<span data-ttu-id="770e9-121">**IMAPITable:: アドバイズ**メソッドを使用して、通知コールバック用にプロバイダーに実装されている table オブジェクトを登録します。</span><span class="sxs-lookup"><span data-stu-id="770e9-121">Use the **IMAPITable::Advise** method to register a table object implemented in the provider for notification callbacks.</span></span> <span data-ttu-id="770e9-122">テーブルオブジェクトが変更されるたびに、プロバイダーは、 _uleventmask_パラメーターにどのイベントマスクビットが設定されているかを確認します。したがって、どのような種類の変更が発生したかを確認します。</span><span class="sxs-lookup"><span data-stu-id="770e9-122">Whenever a change occurs to the table object, the provider checks to see what event mask bit was set in the  _ulEventMask_ parameter and thus what type of change occurred.</span></span> <span data-ttu-id="770e9-123">ビットが設定されている場合、プロバイダーはイベントを報告するために、 _lpAdviseSink_パラメーターによって示されるアドバイズシンクオブジェクトの[IMAPIAdviseSink:: onnotify](imapiadvisesink-onnotify.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="770e9-123">If a bit is set, then the provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object indicated by the  _lpAdviseSink_ parameter to report the event.</span></span> <span data-ttu-id="770e9-124">通知構造で**onnotify**ルーチンに渡されるデータは、イベントについての説明です。</span><span class="sxs-lookup"><span data-stu-id="770e9-124">Data passed in the notification structure to the **OnNotify** routine describes the event.</span></span> 
  
<span data-ttu-id="770e9-125">**onnotify**への呼び出しは、オブジェクトを変更する呼び出し中、または次のときに発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="770e9-125">The call to **OnNotify** can occur during the call that changes the object, or at any following time.</span></span> <span data-ttu-id="770e9-126">複数の実行スレッドをサポートするシステムでは、 **onnotify**への呼び出しは任意のスレッドで発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="770e9-126">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="770e9-127">inopportune 時に発生する可能性のある**onnotify**への呼び出しを、より安全に処理できるようにする方法については、プロバイダーが[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)関数を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="770e9-127">For a way to turn a call to **OnNotify** that might happen at an inopportune time into one that is safer to handle, a provider should use the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="770e9-128">通知を提供するには、**アドバイズ**を実装するプロバイダーに、 _lpAdviseSink_アドバイズシンクオブジェクトへのポインターのコピーを保持する必要があります。これを行うには、アドバイズシンクに対して**IUnknown:: AddRef**メソッドを呼び出して、 [IMAPITable:: アドバイズ](imapitable-unadvise.md)中止メソッドへの呼び出しで通知登録が取り消されるまでオブジェクトポインターを保持します。</span><span class="sxs-lookup"><span data-stu-id="770e9-128">To provide notifications, the provider implementing **Advise** needs to keep a copy of the pointer to the  _lpAdviseSink_ advise sink object; to do so, it calls the **IUnknown::AddRef** method for the advise sink to maintain its object pointer until notification registration is canceled with a call to the [IMAPITable::Unadvise](imapitable-unadvise.md) method.</span></span> <span data-ttu-id="770e9-129">**アドバイズ**実装は、接続番号を通知登録に割り当て、この接続番号で**AddRef**を呼び出してから、lアウト_connection_パラメーターで取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="770e9-129">The **Advise** implementation should assign a connection number to the notification registration and call **AddRef** on this connection number before returning it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="770e9-130">登録が取り消される前に、サービスプロバイダーはアドバイズシンクオブジェクトを解放できますが、\* \* アドバイズ中止 \* \* が呼び出されるまで、接続番号を解放してはなりません。</span><span class="sxs-lookup"><span data-stu-id="770e9-130">Service providers can release the advise sink object before the registration is canceled, but they must not release the connection number until \*\* Unadvise \*\* has been called.</span></span> 
  
<span data-ttu-id="770e9-131">**アドバイズ**の呼び出しが成功し、\* \* アドバイズ中止 \* \* が呼び出された後は、アドバイズシンクオブジェクトを解放するためにクライアントを準備する必要があります。</span><span class="sxs-lookup"><span data-stu-id="770e9-131">After a call to **Advise** has succeeded and before \*\* Unadvise \*\* has been called, clients must be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="770e9-132">そのため、特定の長期間使用しない限り、**アドバイズ**が返された後、クライアントはアドバイズシンクオブジェクトを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="770e9-132">A client should therefore release its advise sink object after **Advise** returns unless it has a specific long-term use for it.</span></span> 
  
<span data-ttu-id="770e9-133">通知の非同期動作のため、テーブル列の設定を変更する実装は、前の列の順序で整理された情報に関する通知を受け取ることができます。</span><span class="sxs-lookup"><span data-stu-id="770e9-133">Because of the asynchronous behavior of notification, implementations that change table column settings can receive notifications with information organized in a previous column order.</span></span> <span data-ttu-id="770e9-134">たとえば、コンテナーから削除されたばかりのメッセージに対して、テーブル行が返される場合があります。</span><span class="sxs-lookup"><span data-stu-id="770e9-134">For instance, a table row might be returned for a message that has just been deleted from the container.</span></span> <span data-ttu-id="770e9-135">このような通知は、列設定の変更が行われ、その情報が送信されたが、通知テーブルのビューがその情報に対してまだ更新されていない場合に送信されます。</span><span class="sxs-lookup"><span data-stu-id="770e9-135">Such a notification is sent when the column setting change has been made and information about it sent but the notification table view has not been updated with that information yet.</span></span>
  
<span data-ttu-id="770e9-136">通知プロセスの詳細については、「 [MAPI でのイベント通知](event-notification-in-mapi.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="770e9-136">For more information on the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="770e9-137">テーブル通知に関する特定の情報については、「[テーブル通知につい](about-table-notifications.md)て」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="770e9-137">For specific information about table notification, see [About Table Notifications](about-table-notifications.md).</span></span> <span data-ttu-id="770e9-138">**imapisupport**メソッドを使用して通知をサポートする方法については、「[サポートイベントの通知](supporting-event-notification.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="770e9-138">For information about using the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="770e9-139">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="770e9-139">MFCMAPI reference</span></span>

<span data-ttu-id="770e9-140">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="770e9-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="770e9-141">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="770e9-141">**File**</span></span>|<span data-ttu-id="770e9-142">**関数**</span><span class="sxs-lookup"><span data-stu-id="770e9-142">**Function**</span></span>|<span data-ttu-id="770e9-143">**コメント**</span><span class="sxs-lookup"><span data-stu-id="770e9-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="770e9-144">ContentsTableListCtrl</span><span class="sxs-lookup"><span data-stu-id="770e9-144">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="770e9-145">CContestTableListCtrl:: notificationon</span><span class="sxs-lookup"><span data-stu-id="770e9-145">CContestTableListCtrl::NotificationOn</span></span>  <br/> |<span data-ttu-id="770e9-146">mfcmapi は、 **IMAPITable:: アドバイズ**メソッドを使用して通知を登録し、テーブルビューが最新の状態を維持できるようにします。</span><span class="sxs-lookup"><span data-stu-id="770e9-146">MFCMAPI uses the **IMAPITable::Advise** method to register for notifications to allow the table view to stay current.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="770e9-147">関連項目</span><span class="sxs-lookup"><span data-stu-id="770e9-147">See also</span></span>



[<span data-ttu-id="770e9-148">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="770e9-148">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="770e9-149">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="770e9-149">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="770e9-150">IMAPITable::Unadvise</span><span class="sxs-lookup"><span data-stu-id="770e9-150">IMAPITable::Unadvise</span></span>](imapitable-unadvise.md)
  
[<span data-ttu-id="770e9-151">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="770e9-151">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="770e9-152">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="770e9-152">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


<span data-ttu-id="770e9-153">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="770e9-153">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

