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
# <a name="imapitableadvise"></a><span data-ttu-id="8b78f-103">IMAPITable::Advise</span><span class="sxs-lookup"><span data-stu-id="8b78f-103">IMAPITable::Advise</span></span>

  
  
<span data-ttu-id="8b78f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b78f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b78f-105">テーブルに影響を与える指定されたイベントの通知を受信するアアドバイス シンク オブジェクトを登録します。</span><span class="sxs-lookup"><span data-stu-id="8b78f-105">Registers an advise sink object to receive notification of specified events affecting the table.</span></span>
  
```cpp
HRESULT Advise(
ULONG ulEventMask,
LPMAPIADVISESINK lpAdviseSink,
ULONG_PTR FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="8b78f-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8b78f-106">Parameters</span></span>

 <span data-ttu-id="8b78f-107">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="8b78f-107">_ulEventMask_</span></span>
  
> <span data-ttu-id="8b78f-108">[in]通知を生成するイベントの種類を示す値。</span><span class="sxs-lookup"><span data-stu-id="8b78f-108">[in] Value indicating the type of event that will generate the notification.</span></span> <span data-ttu-id="8b78f-109">有効な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="8b78f-109">Only the following value is valid:</span></span>
    
 `fnevTableModified`
  
 <span data-ttu-id="8b78f-110">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="8b78f-110">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="8b78f-111">[in]後続の通知を受信するアアドバイス シンク オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="8b78f-111">[in] Pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="8b78f-112">このアアドバイス シンク オブジェクトは、既に割り当てられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b78f-112">This advise sink object must have been already allocated.</span></span>
    
 <span data-ttu-id="8b78f-113">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="8b78f-113">_lpulConnection_</span></span>
  
> <span data-ttu-id="8b78f-114">[out]正常な通知登録を表す 0 以外の値へのポインター。</span><span class="sxs-lookup"><span data-stu-id="8b78f-114">[out] Pointer to a nonzero value that represents the successful notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8b78f-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="8b78f-115">Return value</span></span>

<span data-ttu-id="8b78f-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="8b78f-116">S_OK</span></span> 
  
> <span data-ttu-id="8b78f-117">通知登録が正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="8b78f-117">The notification registration successfully completed.</span></span>
    
<span data-ttu-id="8b78f-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="8b78f-118">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="8b78f-119">テーブルの実装では、行と列の変更がサポートされていないか、通知がサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="8b78f-119">The table implementation either does not support changes to its rows and columns or does not support notification.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8b78f-120">注釈</span><span class="sxs-lookup"><span data-stu-id="8b78f-120">Remarks</span></span>

<span data-ttu-id="8b78f-121">**IMAPITable::Advise メソッドを使用して**、通知コールバック用にプロバイダーに実装されたテーブル オブジェクトを登録します。</span><span class="sxs-lookup"><span data-stu-id="8b78f-121">Use the **IMAPITable::Advise** method to register a table object implemented in the provider for notification callbacks.</span></span> <span data-ttu-id="8b78f-122">テーブル オブジェクトに変更が発生するたびに、プロバイダーは  _ulEventMask_ パラメーターで設定されたイベント マスク ビットと、発生した変更の種類を確認します。</span><span class="sxs-lookup"><span data-stu-id="8b78f-122">Whenever a change occurs to the table object, the provider checks to see what event mask bit was set in the  _ulEventMask_ parameter and thus what type of change occurred.</span></span> <span data-ttu-id="8b78f-123">ビットが設定されている場合、プロバイダーは _、lpAdviseSink_ パラメーターで示されるアアドバイス シンク オブジェクトの [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出して、イベントを報告します。</span><span class="sxs-lookup"><span data-stu-id="8b78f-123">If a bit is set, then the provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object indicated by the  _lpAdviseSink_ parameter to report the event.</span></span> <span data-ttu-id="8b78f-124">通知構造で **OnNotify** ルーチンに渡されたデータは、イベントについて説明します。</span><span class="sxs-lookup"><span data-stu-id="8b78f-124">Data passed in the notification structure to the **OnNotify** routine describes the event.</span></span> 
  
<span data-ttu-id="8b78f-125">**OnNotify の呼び出し** は、オブジェクトを変更する呼び出し中、または次の任意の時点で発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8b78f-125">The call to **OnNotify** can occur during the call that changes the object, or at any following time.</span></span> <span data-ttu-id="8b78f-126">複数の実行スレッドをサポートするシステムでは **、OnNotify** の呼び出しは任意のスレッドで行われます。</span><span class="sxs-lookup"><span data-stu-id="8b78f-126">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="8b78f-127">**Inopportune** 時に発生する可能性がある OnNotify への呼び出しを、より安全に処理できる呼び出しに変える方法として、プロバイダーは [HrThisThreadAdviseSink](hrthisthreadadvisesink.md)関数を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b78f-127">For a way to turn a call to **OnNotify** that might happen at an inopportune time into one that is safer to handle, a provider should use the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="8b78f-128">通知を提供するには、**アドバイス** を実装するプロバイダーは _、lpAdviseSink_ アアドバイス シンク オブジェクトへのポインターのコピーを保持する必要があります。これを行うには、通知登録が [IMAPITable::Unadvise](imapitable-unadvise.md)メソッドの呼び出しで取り消されるまで、そのオブジェクト ポインターを維持するために、アドバイス シンクの **IUnknown::AddRef** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="8b78f-128">To provide notifications, the provider implementing **Advise** needs to keep a copy of the pointer to the  _lpAdviseSink_ advise sink object; to do so, it calls the **IUnknown::AddRef** method for the advise sink to maintain its object pointer until notification registration is canceled with a call to the [IMAPITable::Unadvise](imapitable-unadvise.md) method.</span></span> <span data-ttu-id="8b78f-129">**Advise 実装では**、通知登録に接続番号を割り当て、lpulConnection パラメーターで返す前に、この接続番号で **AddRef** _を呼び出す必要_ があります。</span><span class="sxs-lookup"><span data-stu-id="8b78f-129">The **Advise** implementation should assign a connection number to the notification registration and call **AddRef** on this connection number before returning it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="8b78f-130">サービス プロバイダーは、登録が取り消される前にアアドバイス シンク オブジェクトを解放できますが、\*\* Unadvise \*\* が呼び出されるまで接続番号を解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b78f-130">Service providers can release the advise sink object before the registration is canceled, but they must not release the connection number until \*\* Unadvise \*\* has been called.</span></span> 
  
<span data-ttu-id="8b78f-131">**Advise** の呼び出しが成功した後、\*\* Unadvise \*\* が呼び出される前に、クライアントは、アアドバイス シンク オブジェクトが解放される準備が必要です。</span><span class="sxs-lookup"><span data-stu-id="8b78f-131">After a call to **Advise** has succeeded and before \*\* Unadvise \*\* has been called, clients must be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="8b78f-132">そのため、クライアントは、特定の長期的な使用がない限り **、Advise** が返した後にアアドバイス シンク オブジェクトを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b78f-132">A client should therefore release its advise sink object after **Advise** returns unless it has a specific long-term use for it.</span></span> 
  
<span data-ttu-id="8b78f-133">通知の非同期動作のため、テーブル列の設定を変更する実装は、前の列の順序で整理された情報を含む通知を受信できます。</span><span class="sxs-lookup"><span data-stu-id="8b78f-133">Because of the asynchronous behavior of notification, implementations that change table column settings can receive notifications with information organized in a previous column order.</span></span> <span data-ttu-id="8b78f-134">たとえば、コンテナーから削除されたばかりのメッセージに対してテーブル行が返される場合があります。</span><span class="sxs-lookup"><span data-stu-id="8b78f-134">For instance, a table row might be returned for a message that has just been deleted from the container.</span></span> <span data-ttu-id="8b78f-135">このような通知は、列設定の変更が行われたときに送信され、その通知に関する情報が送信されましたが、通知テーブル ビューがまだその情報で更新されていません。</span><span class="sxs-lookup"><span data-stu-id="8b78f-135">Such a notification is sent when the column setting change has been made and information about it sent but the notification table view has not been updated with that information yet.</span></span>
  
<span data-ttu-id="8b78f-136">通知プロセスの詳細については、「MAPI での [イベント通知」を参照してください](event-notification-in-mapi.md)。</span><span class="sxs-lookup"><span data-stu-id="8b78f-136">For more information on the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="8b78f-137">テーブル通知の詳細については、「テーブル通知について [」を参照してください](about-table-notifications.md)。</span><span class="sxs-lookup"><span data-stu-id="8b78f-137">For specific information about table notification, see [About Table Notifications](about-table-notifications.md).</span></span> <span data-ttu-id="8b78f-138">**IMAPISupport メソッドを使用して通知を** サポートする方法については、「Support Event Notification 」[を参照してください](supporting-event-notification.md)。</span><span class="sxs-lookup"><span data-stu-id="8b78f-138">For information about using the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8b78f-139">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="8b78f-139">MFCMAPI reference</span></span>

<span data-ttu-id="8b78f-140">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b78f-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8b78f-141">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="8b78f-141">**File**</span></span>|<span data-ttu-id="8b78f-142">**関数**</span><span class="sxs-lookup"><span data-stu-id="8b78f-142">**Function**</span></span>|<span data-ttu-id="8b78f-143">**コメント**</span><span class="sxs-lookup"><span data-stu-id="8b78f-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8b78f-144">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="8b78f-144">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="8b78f-145">CContestTableListCtrl::NotificationOn</span><span class="sxs-lookup"><span data-stu-id="8b78f-145">CContestTableListCtrl::NotificationOn</span></span>  <br/> |<span data-ttu-id="8b78f-146">MFCMAPI では **、IMAPITable::Advise** メソッドを使用して通知を登録し、テーブル ビューを最新の状態にできます。</span><span class="sxs-lookup"><span data-stu-id="8b78f-146">MFCMAPI uses the **IMAPITable::Advise** method to register for notifications to allow the table view to stay current.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8b78f-147">関連項目</span><span class="sxs-lookup"><span data-stu-id="8b78f-147">See also</span></span>



[<span data-ttu-id="8b78f-148">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="8b78f-148">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="8b78f-149">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="8b78f-149">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="8b78f-150">IMAPITable::Unadvise</span><span class="sxs-lookup"><span data-stu-id="8b78f-150">IMAPITable::Unadvise</span></span>](imapitable-unadvise.md)
  
[<span data-ttu-id="8b78f-151">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="8b78f-151">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="8b78f-152">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8b78f-152">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


<span data-ttu-id="8b78f-153">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="8b78f-153">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

