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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f79e5eaa3155bbe3373f5ad9c5182a4a65c62648
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572040"
---
# <a name="imapisupportnotify"></a><span data-ttu-id="0183e-103">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="0183e-103">IMAPISupport::Notify</span></span>

<span data-ttu-id="0183e-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0183e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0183e-105">通知の[IMAPISupport::Subscribe](imapisupport-subscribe.md)メソッドを最初に登録されたアドバイズ ソースに指定されたイベントの通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="0183e-105">Sends a notification of a specified event to an advise source that originally registered for the notification through the [IMAPISupport::Subscribe](imapisupport-subscribe.md) method.</span></span> 
  
```cpp
HRESULT Notify(
LPNOTIFKEY lpKey,
ULONG cNotification,
LPNOTIFICATION lpNotifications,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="0183e-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0183e-106">Parameters</span></span>

<span data-ttu-id="0183e-107">_lpKey_</span><span class="sxs-lookup"><span data-stu-id="0183e-107">_lpKey_</span></span>
  
> <span data-ttu-id="0183e-108">[in]アドバイズ ソース オブジェクトの通知のキーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="0183e-108">[in] A pointer to the notification key for the advise source object.</span></span> <span data-ttu-id="0183e-109">_LpKey_パラメーターは、NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="0183e-109">The  _lpKey_ parameter cannot be NULL.</span></span> 
    
<span data-ttu-id="0183e-110">_cNotification_</span><span class="sxs-lookup"><span data-stu-id="0183e-110">_cNotification_</span></span>
  
> <span data-ttu-id="0183e-111">[in]_LpNotifications_パラメーターで指定された通知の構造体の数です。</span><span class="sxs-lookup"><span data-stu-id="0183e-111">[in] The count of notification structures pointed to by the  _lpNotifications_ parameter.</span></span> 
    
<span data-ttu-id="0183e-112">_lpNotifications_</span><span class="sxs-lookup"><span data-stu-id="0183e-112">_lpNotifications_</span></span>
  
> <span data-ttu-id="0183e-113">[in]保留中の通知を説明する[通知](notification.md)の構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0183e-113">[in] A pointer to an array of [NOTIFICATION](notification.md) structures that describe pending notifications.</span></span> 
    
<span data-ttu-id="0183e-114">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="0183e-114">_lpulFlags_</span></span>
  
> <span data-ttu-id="0183e-115">[で [チェック アウト]通知の処理を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="0183e-115">[in, out] A bitmask of flags that controls the notification process.</span></span> <span data-ttu-id="0183e-116">入力では、次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="0183e-116">On input, the following flag can be set:</span></span>
    
  - <span data-ttu-id="0183e-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0183e-117">MAPI_UNICODE</span></span> 
    
    > <span data-ttu-id="0183e-118">_LpNotifications_で指定された通知の構造体の文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="0183e-118">The strings in the notification structures pointed to by  _lpNotifications_ are in Unicode format.</span></span> <span data-ttu-id="0183e-119">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="0183e-119">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 

    <span data-ttu-id="0183e-120">出力では、MAPI は、次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="0183e-120">On output, MAPI can set the following flag:</span></span>
        
  - <span data-ttu-id="0183e-121">NOTIFY_CANCELED</span><span class="sxs-lookup"><span data-stu-id="0183e-121">NOTIFY_CANCELED</span></span> 
    
    > <span data-ttu-id="0183e-122">コールバック関数は、同期の通知をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="0183e-122">A callback function canceled a synchronous notification.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0183e-123">�߂�l</span><span class="sxs-lookup"><span data-stu-id="0183e-123">Return value</span></span>

<span data-ttu-id="0183e-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="0183e-124">S_OK</span></span> 
  
> <span data-ttu-id="0183e-125">通知が正常に生成されました。</span><span class="sxs-lookup"><span data-stu-id="0183e-125">The notifications were successfully generated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0183e-126">注釈</span><span class="sxs-lookup"><span data-stu-id="0183e-126">Remarks</span></span>

<span data-ttu-id="0183e-127">サービス プロバイダーのサポートのすべてのオブジェクトの**IMAPISupport::Notify**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="0183e-127">The **IMAPISupport::Notify** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="0183e-128">サービス プロバイダーでは、MAPI が以前に**IMAPISupport::Subscribe**メソッドを介して通知の登録がアドバイズ シンクに通知を生成することを要求する**通知**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0183e-128">Service providers call **Notify** to request that MAPI generate a notification for an advise sink that has previously registered for the notification through the **IMAPISupport::Subscribe** method.</span></span> 
  
<span data-ttu-id="0183e-129">**通知**のコピーの構造体はメモリに、 _lpNotifications_パラメーターで指定され、適切なアドバイズ シンクの[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0183e-129">**Notify** copies the structures pointed to by the  _lpNotifications_ parameter into memory and calls the appropriate advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="0183e-130">**OnNotify**終了すると、通知に関連するメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="0183e-130">When **OnNotify** is finished with the notification, it releases the memory involved.</span></span> <span data-ttu-id="0183e-131">呼び出し元がメモリを割り当てる必要はありません。MAPI は、すべての必要なメモリ割り当てを実行します。</span><span class="sxs-lookup"><span data-stu-id="0183e-131">The caller does not need to allocate memory; MAPI performs all necessary memory allocation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0183e-132">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="0183e-132">Notes to callers</span></span>

<span data-ttu-id="0183e-133">_LpKey_パラメーターに渡された通知のキーは、 _lpKey_ 、 **IMAPISupport::Subscribe**メソッドに渡されたキーと同じはずです。</span><span class="sxs-lookup"><span data-stu-id="0183e-133">The notification key passed in the  _lpKey_ parameter should be identical to the key passed in  _lpKey_ to the **IMAPISupport::Subscribe** method.</span></span> <span data-ttu-id="0183e-134">多くのプロバイダーでは、アドバイズ ソースのエントリ id を使用して、キーには、ファイル パスなど、他のデータを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="0183e-134">Many providers use the entry identifier of the advise source as the key, but other data, such as a file path, can be used.</span></span> <span data-ttu-id="0183e-135">MAPI では、特定のアドバイスのソース上の通知のすべての登録を検索するのにはこのキーを使用します。</span><span class="sxs-lookup"><span data-stu-id="0183e-135">MAPI uses this key to find all the registrations for notifications on the identified advise source.</span></span> 
  
<span data-ttu-id="0183e-136">長期のエントリ id には、通知の構造体の**lpEntryID**メンバーを設定することを確認します。</span><span class="sxs-lookup"><span data-stu-id="0183e-136">Be sure that you set the **lpEntryID** member of the notification structure to a long-term entry identifier.</span></span> 
  
<span data-ttu-id="0183e-137">設定する場合は、**購読**に NOTIFY_SYNC フラグを呼び出す保留中の通知では、**通知**のいずれかの呼び出し**IMAPIAdviseSink::OnNotify**メソッドのコールバック関数を返す前に。</span><span class="sxs-lookup"><span data-stu-id="0183e-137">If you set the NOTIFY_SYNC flag on the **Subscribe** call for any of the pending notifications, **Notify** calls the **IMAPIAdviseSink::OnNotify** method callback functions before returning.</span></span> <span data-ttu-id="0183e-138">手動でまたは[HrAllocAdviseSink](hrallocadvisesink.md)を呼び出すことによって、アドバイズ シンクを作成できます。</span><span class="sxs-lookup"><span data-stu-id="0183e-138">An advise sink can be created manually or by calling [HrAllocAdviseSink](hrallocadvisesink.md).</span></span> <span data-ttu-id="0183e-139">**HrAllocAdviseSink**関数では、通知の一部としてその**通知**呼び出しのコールバック関数を指定する呼び出し元を使用できます。</span><span class="sxs-lookup"><span data-stu-id="0183e-139">The **HrAllocAdviseSink** function allows its caller to specify a callback function that **Notify** calls as part of the notification.</span></span> <span data-ttu-id="0183e-140">コールバック関数は、 [NOTIFCALLBACK](notifcallback.md)のプロトタイプに準拠しています。</span><span class="sxs-lookup"><span data-stu-id="0183e-140">The callback function conforms to the [NOTIFCALLBACK](notifcallback.md) prototype.</span></span> <span data-ttu-id="0183e-141">常にクライアントによって実装されるコールバック関数は、S_OK を返すサービス プロバイダーによって実装されるコールバック関数は、CALLBACK_DISCONTINUE を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="0183e-141">Callback functions implemented by clients always return S_OK; callback functions implemented by service providers can return CALLBACK_DISCONTINUE.</span></span> 
  
<span data-ttu-id="0183e-142">コールバック関数には、CALLBACK_DISCONTINUE が返された場合、MAPI は通知の送信を停止し、**通知**メソッドの_lpulFlags_パラメーターで NOTIFY_CANCELED を返します。</span><span class="sxs-lookup"><span data-stu-id="0183e-142">If a callback function returns CALLBACK_DISCONTINUE, MAPI stops sending notifications and returns NOTIFY_CANCELED in the **Notify** method's  _lpulFlags_ parameter.</span></span> <span data-ttu-id="0183e-143">プロセスは、非アクティブであり、そのプロセスの通知を生成する停止を想定することができます。</span><span class="sxs-lookup"><span data-stu-id="0183e-143">You can assume that the process is inactive and stop generating notifications for that process.</span></span> <span data-ttu-id="0183e-144">**通知**では、 _lpulFlags_で 0 が返された場合、プロセスがアクティブであると、必要に応じて、通知の送信を続行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0183e-144">If **Notify** returns 0 in  _lpulFlags_, the process is still active and you should continue to send notifications, as appropriate.</span></span>
  
<span data-ttu-id="0183e-145">同期の通知を使用する場合は、デッドロックを回避するのには注意が必要です。</span><span class="sxs-lookup"><span data-stu-id="0183e-145">When you use synchronous notifications, be careful to avoid deadlock situations.</span></span>
  
<span data-ttu-id="0183e-146">通知プロセスの詳細については、 [MAPI でのイベントの通知](event-notification-in-mapi.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0183e-146">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0183e-147">関連項目</span><span class="sxs-lookup"><span data-stu-id="0183e-147">See also</span></span>

- [<span data-ttu-id="0183e-148">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="0183e-148">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)  
- [<span data-ttu-id="0183e-149">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="0183e-149">IMAPISupport::Unsubscribe</span></span>](imapisupport-unsubscribe.md)  
- [<span data-ttu-id="0183e-150">NOTIFCALLBACK</span><span class="sxs-lookup"><span data-stu-id="0183e-150">NOTIFCALLBACK</span></span>](notifcallback.md) 
- [<span data-ttu-id="0183e-151">�ʒm</span><span class="sxs-lookup"><span data-stu-id="0183e-151">NOTIFICATION</span></span>](notification.md)  
- [<span data-ttu-id="0183e-152">NOTIFKEY</span><span class="sxs-lookup"><span data-stu-id="0183e-152">NOTIFKEY</span></span>](notifkey.md)  
- [<span data-ttu-id="0183e-153">PidTagRecordKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0183e-153">PidTagRecordKey Canonical Property</span></span>](pidtagrecordkey-canonical-property.md)  
- [<span data-ttu-id="0183e-154">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="0183e-154">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

