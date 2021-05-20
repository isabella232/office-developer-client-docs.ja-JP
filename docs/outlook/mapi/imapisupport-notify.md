---
title: IMAPISupportNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Notify
api_type:
- COM
ms.assetid: c16c668e-2c8b-4759-bbca-d0c5662b62e9
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6160b8e75bdc9059965c2358b9fe7d296e1f66d2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435937"
---
# <a name="imapisupportnotify"></a><span data-ttu-id="97728-103">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="97728-103">IMAPISupport::Notify</span></span>

<span data-ttu-id="97728-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="97728-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="97728-105">指定したイベントの通知を [、IMAPISupport::Subscribe](imapisupport-subscribe.md) メソッドを介して通知用に登録されたアドバイス ソースに送信します。</span><span class="sxs-lookup"><span data-stu-id="97728-105">Sends a notification of a specified event to an advise source that originally registered for the notification through the [IMAPISupport::Subscribe](imapisupport-subscribe.md) method.</span></span> 
  
```cpp
HRESULT Notify(
LPNOTIFKEY lpKey,
ULONG cNotification,
LPNOTIFICATION lpNotifications,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="97728-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="97728-106">Parameters</span></span>

<span data-ttu-id="97728-107">_lpKey_</span><span class="sxs-lookup"><span data-stu-id="97728-107">_lpKey_</span></span>
  
> <span data-ttu-id="97728-108">[in]アドバイス ソース オブジェクトの通知キーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="97728-108">[in] A pointer to the notification key for the advise source object.</span></span> <span data-ttu-id="97728-109">_lpKey パラメーター_ は NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="97728-109">The  _lpKey_ parameter cannot be NULL.</span></span> 
    
<span data-ttu-id="97728-110">_cNotification_</span><span class="sxs-lookup"><span data-stu-id="97728-110">_cNotification_</span></span>
  
> <span data-ttu-id="97728-111">[in]  _lpNotifications_ パラメーターが指す通知構造の数。</span><span class="sxs-lookup"><span data-stu-id="97728-111">[in] The count of notification structures pointed to by the  _lpNotifications_ parameter.</span></span> 
    
<span data-ttu-id="97728-112">_lpNotifications_</span><span class="sxs-lookup"><span data-stu-id="97728-112">_lpNotifications_</span></span>
  
> <span data-ttu-id="97728-113">[in]保留中の通知を記述 [する NOTIFICATION](notification.md) 構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="97728-113">[in] A pointer to an array of [NOTIFICATION](notification.md) structures that describe pending notifications.</span></span> 
    
<span data-ttu-id="97728-114">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="97728-114">_lpulFlags_</span></span>
  
> <span data-ttu-id="97728-115">[in, out]通知プロセスを制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="97728-115">[in, out] A bitmask of flags that controls the notification process.</span></span> <span data-ttu-id="97728-116">入力時に、次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="97728-116">On input, the following flag can be set:</span></span>
    
  - <span data-ttu-id="97728-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="97728-117">MAPI_UNICODE</span></span> 
    
    > <span data-ttu-id="97728-118">_lpNotifications_ が指す通知構造の文字列は、Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="97728-118">The strings in the notification structures pointed to by  _lpNotifications_ are in Unicode format.</span></span> <span data-ttu-id="97728-119">このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="97728-119">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 

    <span data-ttu-id="97728-120">出力時に、MAPI は次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="97728-120">On output, MAPI can set the following flag:</span></span>
        
  - <span data-ttu-id="97728-121">NOTIFY_CANCELED</span><span class="sxs-lookup"><span data-stu-id="97728-121">NOTIFY_CANCELED</span></span> 
    
    > <span data-ttu-id="97728-122">コールバック関数が同期通知を取り消しました。</span><span class="sxs-lookup"><span data-stu-id="97728-122">A callback function canceled a synchronous notification.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="97728-123">戻り値</span><span class="sxs-lookup"><span data-stu-id="97728-123">Return value</span></span>

<span data-ttu-id="97728-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="97728-124">S_OK</span></span> 
  
> <span data-ttu-id="97728-125">通知が正常に生成されました。</span><span class="sxs-lookup"><span data-stu-id="97728-125">The notifications were successfully generated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="97728-126">注釈</span><span class="sxs-lookup"><span data-stu-id="97728-126">Remarks</span></span>

<span data-ttu-id="97728-127">**IMAPISupport::Notify** メソッドは、すべてのサービス プロバイダー サポート オブジェクトに実装されます。</span><span class="sxs-lookup"><span data-stu-id="97728-127">The **IMAPISupport::Notify** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="97728-128">サービス プロバイダーは **Notify** を呼び出して **、IMAPISupport::Subscribe** メソッドを介して通知に対して以前に登録した通知シンクの通知を MAPI が生成する要求を行います。</span><span class="sxs-lookup"><span data-stu-id="97728-128">Service providers call **Notify** to request that MAPI generate a notification for an advise sink that has previously registered for the notification through the **IMAPISupport::Subscribe** method.</span></span> 
  
<span data-ttu-id="97728-129">**Notify** は  _、lpNotifications_ パラメーターが指す構造体をメモリにコピーし、適切なアアドバイス シンクの [IMAPIAdviseSink::OnNotify メソッドを呼び出](imapiadvisesink-onnotify.md) します。</span><span class="sxs-lookup"><span data-stu-id="97728-129">**Notify** copies the structures pointed to by the  _lpNotifications_ parameter into memory and calls the appropriate advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="97728-130">**通知で OnNotify** が終了すると、関連するメモリが解放されます。</span><span class="sxs-lookup"><span data-stu-id="97728-130">When **OnNotify** is finished with the notification, it releases the memory involved.</span></span> <span data-ttu-id="97728-131">呼び出し元はメモリを割り当てる必要があります。MAPI は、必要なすべてのメモリ割り当てを実行します。</span><span class="sxs-lookup"><span data-stu-id="97728-131">The caller does not need to allocate memory; MAPI performs all necessary memory allocation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="97728-132">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="97728-132">Notes to callers</span></span>

<span data-ttu-id="97728-133">lpKey パラメーターで渡される通知キーは _、lpKey_ で **IMAPISupport::Subscribe** メソッドに渡されるキーと同じである必要があります。 </span><span class="sxs-lookup"><span data-stu-id="97728-133">The notification key passed in the  _lpKey_ parameter should be identical to the key passed in  _lpKey_ to the **IMAPISupport::Subscribe** method.</span></span> <span data-ttu-id="97728-134">多くのプロバイダーは、アドバイス ソースのエントリ識別子をキーとして使用しますが、ファイル パスなどの他のデータを使用できます。</span><span class="sxs-lookup"><span data-stu-id="97728-134">Many providers use the entry identifier of the advise source as the key, but other data, such as a file path, can be used.</span></span> <span data-ttu-id="97728-135">MAPI は、このキーを使用して、識別されたアドバイス ソース上の通知のすべての登録を検索します。</span><span class="sxs-lookup"><span data-stu-id="97728-135">MAPI uses this key to find all the registrations for notifications on the identified advise source.</span></span> 
  
<span data-ttu-id="97728-136">通知構造体の **lpEntryID** メンバーを長期エントリ識別子に設定してください。</span><span class="sxs-lookup"><span data-stu-id="97728-136">Be sure that you set the **lpEntryID** member of the notification structure to a long-term entry identifier.</span></span> 
  
<span data-ttu-id="97728-137">保留中の通知のサブスクライブ呼び出しでNOTIFY_SYNC フラグを設定すると **、Notify** は **IMAPIAdviseSink::OnNotify** メソッドコールバック関数を呼び出してから返します。</span><span class="sxs-lookup"><span data-stu-id="97728-137">If you set the NOTIFY_SYNC flag on the **Subscribe** call for any of the pending notifications, **Notify** calls the **IMAPIAdviseSink::OnNotify** method callback functions before returning.</span></span> <span data-ttu-id="97728-138">アドバイス シンクは、手動で作成するか [、HrAllocAdviseSink を呼び出すことによって作成できます](hrallocadvisesink.md)。</span><span class="sxs-lookup"><span data-stu-id="97728-138">An advise sink can be created manually or by calling [HrAllocAdviseSink](hrallocadvisesink.md).</span></span> <span data-ttu-id="97728-139">**HrAllocAdviseSink** 関数を使用すると、呼び出し元は通知の一部として **Notify** が呼び出すコールバック関数を指定できます。</span><span class="sxs-lookup"><span data-stu-id="97728-139">The **HrAllocAdviseSink** function allows its caller to specify a callback function that **Notify** calls as part of the notification.</span></span> <span data-ttu-id="97728-140">コールバック関数は [NOTIFCALLBACK プロトタイプに準拠](notifcallback.md) しています。</span><span class="sxs-lookup"><span data-stu-id="97728-140">The callback function conforms to the [NOTIFCALLBACK](notifcallback.md) prototype.</span></span> <span data-ttu-id="97728-141">クライアントによって実装されるコールバック関数は、常にS_OK。サービス プロバイダーによって実装されたコールバック関数は、CALLBACK_DISCONTINUE。</span><span class="sxs-lookup"><span data-stu-id="97728-141">Callback functions implemented by clients always return S_OK; callback functions implemented by service providers can return CALLBACK_DISCONTINUE.</span></span> 
  
<span data-ttu-id="97728-142">コールバック関数が通知を返CALLBACK_DISCONTINUE MAPI は通知の送信を停止し **、Notify** メソッドの  _lpulFlags_ パラメーター NOTIFY_CANCELEDを返します。</span><span class="sxs-lookup"><span data-stu-id="97728-142">If a callback function returns CALLBACK_DISCONTINUE, MAPI stops sending notifications and returns NOTIFY_CANCELED in the **Notify** method's  _lpulFlags_ parameter.</span></span> <span data-ttu-id="97728-143">プロセスが非アクティブであり、そのプロセスの通知の生成を停止すると仮定できます。</span><span class="sxs-lookup"><span data-stu-id="97728-143">You can assume that the process is inactive and stop generating notifications for that process.</span></span> <span data-ttu-id="97728-144">Notify **が**  _lpulFlags_ で 0 を返す場合、プロセスはまだアクティブであり、必要に応じて引き続き通知を送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="97728-144">If **Notify** returns 0 in  _lpulFlags_, the process is still active and you should continue to send notifications, as appropriate.</span></span>
  
<span data-ttu-id="97728-145">同期通知を使用する場合は、デッドロックの状況を避けるように注意してください。</span><span class="sxs-lookup"><span data-stu-id="97728-145">When you use synchronous notifications, be careful to avoid deadlock situations.</span></span>
  
<span data-ttu-id="97728-146">通知プロセスの詳細については、「MAPI での [イベント通知」を参照してください](event-notification-in-mapi.md)。</span><span class="sxs-lookup"><span data-stu-id="97728-146">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="97728-147">関連項目</span><span class="sxs-lookup"><span data-stu-id="97728-147">See also</span></span>

- [<span data-ttu-id="97728-148">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="97728-148">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)  
- [<span data-ttu-id="97728-149">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="97728-149">IMAPISupport::Unsubscribe</span></span>](imapisupport-unsubscribe.md)  
- [<span data-ttu-id="97728-150">NOTIFCALLBACK</span><span class="sxs-lookup"><span data-stu-id="97728-150">NOTIFCALLBACK</span></span>](notifcallback.md) 
- [<span data-ttu-id="97728-151">�ʒm</span><span class="sxs-lookup"><span data-stu-id="97728-151">NOTIFICATION</span></span>](notification.md)  
- [<span data-ttu-id="97728-152">NOTIFKEY</span><span class="sxs-lookup"><span data-stu-id="97728-152">NOTIFKEY</span></span>](notifkey.md)  
- [<span data-ttu-id="97728-153">PidTagRecordKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="97728-153">PidTagRecordKey Canonical Property</span></span>](pidtagrecordkey-canonical-property.md)  
- [<span data-ttu-id="97728-154">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="97728-154">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

