---
title: imapisupportnotify
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326370"
---
# <a name="imapisupportnotify"></a><span data-ttu-id="98376-103">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="98376-103">IMAPISupport::Notify</span></span>

<span data-ttu-id="98376-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98376-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98376-105">指定したイベントの通知を、 [imapisupport:: Subscribe](imapisupport-subscribe.md)メソッドによって最初に通知用に登録されたアドバイズソースに送信します。</span><span class="sxs-lookup"><span data-stu-id="98376-105">Sends a notification of a specified event to an advise source that originally registered for the notification through the [IMAPISupport::Subscribe](imapisupport-subscribe.md) method.</span></span> 
  
```cpp
HRESULT Notify(
LPNOTIFKEY lpKey,
ULONG cNotification,
LPNOTIFICATION lpNotifications,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="98376-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="98376-106">Parameters</span></span>

<span data-ttu-id="98376-107">_lpkey_</span><span class="sxs-lookup"><span data-stu-id="98376-107">_lpKey_</span></span>
  
> <span data-ttu-id="98376-108">順番アドバイズソースオブジェクトの通知キーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="98376-108">[in] A pointer to the notification key for the advise source object.</span></span> <span data-ttu-id="98376-109">_lpkey_パラメーターを NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="98376-109">The  _lpKey_ parameter cannot be NULL.</span></span> 
    
<span data-ttu-id="98376-110">_cnotification_</span><span class="sxs-lookup"><span data-stu-id="98376-110">_cNotification_</span></span>
  
> <span data-ttu-id="98376-111">順番lpnotifications パラメーターが指す通知構造の数__ 。</span><span class="sxs-lookup"><span data-stu-id="98376-111">[in] The count of notification structures pointed to by the  _lpNotifications_ parameter.</span></span> 
    
<span data-ttu-id="98376-112">_lpnotifications_</span><span class="sxs-lookup"><span data-stu-id="98376-112">_lpNotifications_</span></span>
  
> <span data-ttu-id="98376-113">順番保留中の通知を記述する[通知](notification.md)構造の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="98376-113">[in] A pointer to an array of [NOTIFICATION](notification.md) structures that describe pending notifications.</span></span> 
    
<span data-ttu-id="98376-114">_lアウトフラグ_</span><span class="sxs-lookup"><span data-stu-id="98376-114">_lpulFlags_</span></span>
  
> <span data-ttu-id="98376-115">[入力]通知プロセスを制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="98376-115">[in, out] A bitmask of flags that controls the notification process.</span></span> <span data-ttu-id="98376-116">入力時には、次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="98376-116">On input, the following flag can be set:</span></span>
    
  - <span data-ttu-id="98376-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="98376-117">MAPI_UNICODE</span></span> 
    
    > <span data-ttu-id="98376-118">lpnotifications が指す通知構造の文字列は__ 、Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="98376-118">The strings in the notification structures pointed to by  _lpNotifications_ are in Unicode format.</span></span> <span data-ttu-id="98376-119">MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="98376-119">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 

    <span data-ttu-id="98376-120">出力では、MAPI は次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="98376-120">On output, MAPI can set the following flag:</span></span>
        
  - <span data-ttu-id="98376-121">NOTIFY_CANCELED</span><span class="sxs-lookup"><span data-stu-id="98376-121">NOTIFY_CANCELED</span></span> 
    
    > <span data-ttu-id="98376-122">コールバック関数が同期通知をキャンセルしました。</span><span class="sxs-lookup"><span data-stu-id="98376-122">A callback function canceled a synchronous notification.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="98376-123">戻り値</span><span class="sxs-lookup"><span data-stu-id="98376-123">Return value</span></span>

<span data-ttu-id="98376-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="98376-124">S_OK</span></span> 
  
> <span data-ttu-id="98376-125">通知が正常に生成されました。</span><span class="sxs-lookup"><span data-stu-id="98376-125">The notifications were successfully generated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="98376-126">解説</span><span class="sxs-lookup"><span data-stu-id="98376-126">Remarks</span></span>

<span data-ttu-id="98376-127">**imapisupport:: Notify**メソッドは、すべてのサービスプロバイダーサポートオブジェクトに実装されています。</span><span class="sxs-lookup"><span data-stu-id="98376-127">The **IMAPISupport::Notify** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="98376-128">サービスプロバイダーは、MAPI に対して、 **imapisupport:: Subscribe**メソッドによって既に通知が登録されているアドバイズシンクに対して通知を生成することを要求する呼び出し**通知**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="98376-128">Service providers call **Notify** to request that MAPI generate a notification for an advise sink that has previously registered for the notification through the **IMAPISupport::Subscribe** method.</span></span> 
  
<span data-ttu-id="98376-129">**Notify**は、lpnotifications パラメーターが指す__ 構造をメモリにコピーし、適切なアドバイズシンクの[IMAPIAdviseSink:: onnotify](imapiadvisesink-onnotify.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="98376-129">**Notify** copies the structures pointed to by the  _lpNotifications_ parameter into memory and calls the appropriate advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="98376-130">**onnotify**が通知を終了すると、関係するメモリが解放されます。</span><span class="sxs-lookup"><span data-stu-id="98376-130">When **OnNotify** is finished with the notification, it releases the memory involved.</span></span> <span data-ttu-id="98376-131">呼び出し元はメモリを割り当てる必要がありません。MAPI は、必要なすべてのメモリ割り当てを実行します。</span><span class="sxs-lookup"><span data-stu-id="98376-131">The caller does not need to allocate memory; MAPI performs all necessary memory allocation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="98376-132">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="98376-132">Notes to callers</span></span>

<span data-ttu-id="98376-133">_lpkey_パラメーターに渡された通知キーは、 _lpkey_で渡された**imapisupport:: Subscribe**メソッドに渡されるキーと同一である必要があります。</span><span class="sxs-lookup"><span data-stu-id="98376-133">The notification key passed in the  _lpKey_ parameter should be identical to the key passed in  _lpKey_ to the **IMAPISupport::Subscribe** method.</span></span> <span data-ttu-id="98376-134">多くのプロバイダーは、アドバイズ元のエントリ識別子をキーとして使用しますが、ファイルパスなどのその他のデータを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="98376-134">Many providers use the entry identifier of the advise source as the key, but other data, such as a file path, can be used.</span></span> <span data-ttu-id="98376-135">MAPI はこのキーを使用して、指定されたアドバイズ元での通知のすべての登録を検索します。</span><span class="sxs-lookup"><span data-stu-id="98376-135">MAPI uses this key to find all the registrations for notifications on the identified advise source.</span></span> 
  
<span data-ttu-id="98376-136">通知構造の**lて tryid**メンバは、長期のエントリ id に設定してください。</span><span class="sxs-lookup"><span data-stu-id="98376-136">Be sure that you set the **lpEntryID** member of the notification structure to a long-term entry identifier.</span></span> 
  
<span data-ttu-id="98376-137">保留中のいずれかの通知の**サブスクライブ**呼び出しで NOTIFY_SYNC フラグを設定すると、 **IMAPIAdviseSink:: onnotify**メソッドのコールバック関数が呼び出された後に**通知**されます。</span><span class="sxs-lookup"><span data-stu-id="98376-137">If you set the NOTIFY_SYNC flag on the **Subscribe** call for any of the pending notifications, **Notify** calls the **IMAPIAdviseSink::OnNotify** method callback functions before returning.</span></span> <span data-ttu-id="98376-138">アドバイズシンクは、手動で作成することも、 [HrAllocAdviseSink](hrallocadvisesink.md)を呼び出すことによって作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="98376-138">An advise sink can be created manually or by calling [HrAllocAdviseSink](hrallocadvisesink.md).</span></span> <span data-ttu-id="98376-139">**HrAllocAdviseSink**関数を使用すると、発信者は通知の一部として呼び出しを**通知**するコールバック関数を指定できます。</span><span class="sxs-lookup"><span data-stu-id="98376-139">The **HrAllocAdviseSink** function allows its caller to specify a callback function that **Notify** calls as part of the notification.</span></span> <span data-ttu-id="98376-140">コールバック関数は、 [NOTIFCALLBACK](notifcallback.md)プロトタイプに準拠しています。</span><span class="sxs-lookup"><span data-stu-id="98376-140">The callback function conforms to the [NOTIFCALLBACK](notifcallback.md) prototype.</span></span> <span data-ttu-id="98376-141">クライアントによって実装されたコールバック関数は常に S_OK を返します。サービスプロバイダーによって実装されたコールバック関数は、CALLBACK_DISCONTINUE を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="98376-141">Callback functions implemented by clients always return S_OK; callback functions implemented by service providers can return CALLBACK_DISCONTINUE.</span></span> 
  
<span data-ttu-id="98376-142">コールバック関数が CALLBACK_DISCONTINUE を返す場合、MAPI は通知の送信を停止し、 **NOTIFY**メソッドの_lNOTIFY_CANCELED flags_パラメーターでを返します。</span><span class="sxs-lookup"><span data-stu-id="98376-142">If a callback function returns CALLBACK_DISCONTINUE, MAPI stops sending notifications and returns NOTIFY_CANCELED in the **Notify** method's  _lpulFlags_ parameter.</span></span> <span data-ttu-id="98376-143">プロセスが非アクティブであると仮定して、そのプロセスの通知の生成を停止することができます。</span><span class="sxs-lookup"><span data-stu-id="98376-143">You can assume that the process is inactive and stop generating notifications for that process.</span></span> <span data-ttu-id="98376-144">**Notify**で_l出 flags_に0が返された場合、プロセスはアクティブなままで、必要に応じて通知の送信を続行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="98376-144">If **Notify** returns 0 in  _lpulFlags_, the process is still active and you should continue to send notifications, as appropriate.</span></span>
  
<span data-ttu-id="98376-145">同期通知を使用する場合は、デッドロックの状況を回避するために注意してください。</span><span class="sxs-lookup"><span data-stu-id="98376-145">When you use synchronous notifications, be careful to avoid deadlock situations.</span></span>
  
<span data-ttu-id="98376-146">通知プロセスの詳細については、「 [MAPI でのイベント通知](event-notification-in-mapi.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="98376-146">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="98376-147">関連項目</span><span class="sxs-lookup"><span data-stu-id="98376-147">See also</span></span>

- [<span data-ttu-id="98376-148">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="98376-148">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)  
- [<span data-ttu-id="98376-149">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="98376-149">IMAPISupport::Unsubscribe</span></span>](imapisupport-unsubscribe.md)  
- [<span data-ttu-id="98376-150">NOTIFCALLBACK</span><span class="sxs-lookup"><span data-stu-id="98376-150">NOTIFCALLBACK</span></span>](notifcallback.md) 
- [<span data-ttu-id="98376-151">�ʒm</span><span class="sxs-lookup"><span data-stu-id="98376-151">NOTIFICATION</span></span>](notification.md)  
- [<span data-ttu-id="98376-152">NOTIFKEY</span><span class="sxs-lookup"><span data-stu-id="98376-152">NOTIFKEY</span></span>](notifkey.md)  
- [<span data-ttu-id="98376-153">PidTagRecordKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="98376-153">PidTagRecordKey Canonical Property</span></span>](pidtagrecordkey-canonical-property.md)  
- [<span data-ttu-id="98376-154">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="98376-154">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

