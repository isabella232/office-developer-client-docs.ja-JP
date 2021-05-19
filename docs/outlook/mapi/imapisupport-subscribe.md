---
title: IMAPISupportSubscribe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Subscribe
api_type:
- COM
ms.assetid: e6baaff1-446e-431a-a09b-9b529153382b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 5a8c288e877078ece6ab2da8c6494d96e1714ad7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419927"
---
# <a name="imapisupportsubscribe"></a><span data-ttu-id="bbf0c-103">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="bbf0c-103">IMAPISupport::Subscribe</span></span>

  
  
<span data-ttu-id="bbf0c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bbf0c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bbf0c-105">MAPI 経由で通知を受け取るアドバイス シンクを登録します。</span><span class="sxs-lookup"><span data-stu-id="bbf0c-105">Registers an advise sink to receive notifications through MAPI.</span></span>
  
```cpp
HRESULT Subscribe(
LPNOTIFKEY lpKey,
ULONG ulEventMask,
ULONG ulFlags,
LPMAPIADVISESINK lpAdviseSink,
ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="bbf0c-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bbf0c-106">Parameters</span></span>

 <span data-ttu-id="bbf0c-107">_lpKey_</span><span class="sxs-lookup"><span data-stu-id="bbf0c-107">_lpKey_</span></span>
  
> <span data-ttu-id="bbf0c-108">[in]アドバイス ソース オブジェクトを表す通知キーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="bbf0c-108">[in] A pointer to a notification key that represents the advise source object.</span></span> <span data-ttu-id="bbf0c-109">_lpKey パラメーター_ は NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="bbf0c-109">The  _lpKey_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="bbf0c-110">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="bbf0c-110">_ulEventMask_</span></span>
  
> <span data-ttu-id="bbf0c-111">[in]呼び出し元が関心を持ち、登録に含める必要がある通知イベントの種類を示す値のマスク。</span><span class="sxs-lookup"><span data-stu-id="bbf0c-111">[in] A mask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="bbf0c-112">次の値が有効です。</span><span class="sxs-lookup"><span data-stu-id="bbf0c-112">The following values are valid:</span></span>
    
 <span data-ttu-id="bbf0c-113">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="bbf0c-113">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="bbf0c-114">メモリ不足などの重大なエラーに関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="bbf0c-114">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
 <span data-ttu-id="bbf0c-115">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="bbf0c-115">_fnevExtended_</span></span>
  
> <span data-ttu-id="bbf0c-116">特定のアドレス帳またはメッセージ ストア プロバイダーに固有のイベントに関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="bbf0c-116">Registers for notifications about events specific to the particular address book or message store provider.</span></span>
    
 <span data-ttu-id="bbf0c-117">_fnevNewMail_</span><span class="sxs-lookup"><span data-stu-id="bbf0c-117">_fnevNewMail_</span></span>
  
> <span data-ttu-id="bbf0c-118">新しいメッセージの到着に関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="bbf0c-118">Registers for notifications about the arrival of new messages.</span></span> 
    
 <span data-ttu-id="bbf0c-119">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="bbf0c-119">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="bbf0c-120">新しいオブジェクトの作成に関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="bbf0c-120">Registers for notifications about the creation of a new object.</span></span>
    
 <span data-ttu-id="bbf0c-121">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="bbf0c-121">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="bbf0c-122">コピーするオブジェクトに関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="bbf0c-122">Registers for notifications about an object being copied.</span></span>
    
 <span data-ttu-id="bbf0c-123">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="bbf0c-123">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="bbf0c-124">削除するオブジェクトに関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="bbf0c-124">Registers for notifications about an object being deleted.</span></span>
    
 <span data-ttu-id="bbf0c-125">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="bbf0c-125">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="bbf0c-126">変更するオブジェクトに関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="bbf0c-126">Registers for notifications about an object being modified.</span></span>
    
 <span data-ttu-id="bbf0c-127">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="bbf0c-127">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="bbf0c-128">移動するオブジェクトに関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="bbf0c-128">Registers for notifications about an object being moved.</span></span>
    
 <span data-ttu-id="bbf0c-129">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="bbf0c-129">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="bbf0c-130">検索操作の完了に関する通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="bbf0c-130">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="bbf0c-131">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bbf0c-131">_ulFlags_</span></span>
  
> <span data-ttu-id="bbf0c-132">[in]通知の発生方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="bbf0c-132">[in] A bitmask of flags that controls how notification occurs.</span></span> <span data-ttu-id="bbf0c-133">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="bbf0c-133">The following flag can be set:</span></span>
    
<span data-ttu-id="bbf0c-134">NOTIFY_SYNC</span><span class="sxs-lookup"><span data-stu-id="bbf0c-134">NOTIFY_SYNC</span></span> 
  
> <span data-ttu-id="bbf0c-135">呼び出し元が [IMAPISupport::Notify](imapisupport-notify.md) メソッドを呼び出してこの通知シンクの通知を生成する場合 **、Notify** は、返す前にシンクに通知するために必要なすべての呼び出しを行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="bbf0c-135">When the caller calls the [IMAPISupport::Notify](imapisupport-notify.md) method to generate notifications for this advise sink, **Notify** should make all necessary calls to advise sinks before returning.</span></span> <span data-ttu-id="bbf0c-136">このフラグが設定されていない場合、通知は非同期であり、これらのプロセスが CPU の制御を得る際にサブスクライブおよび開始されたプロセスにコールバックがキューに入れられます。</span><span class="sxs-lookup"><span data-stu-id="bbf0c-136">If this flag is not set, notification is asynchronous and callbacks are queued to the processes that have subscribed and started when those processes gain control of the CPU.</span></span> 
    
 <span data-ttu-id="bbf0c-137">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="bbf0c-137">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="bbf0c-138">[in]アアドバイス シンク オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="bbf0c-138">[in] A pointer to an advise sink object.</span></span> 
    
 <span data-ttu-id="bbf0c-139">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="bbf0c-139">_lpulConnection_</span></span>
  
> <span data-ttu-id="bbf0c-140">[out]登録を表す 0 以外の接続番号へのポインター。</span><span class="sxs-lookup"><span data-stu-id="bbf0c-140">[out] A pointer to a nonzero connection number that represents the registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bbf0c-141">戻り値</span><span class="sxs-lookup"><span data-stu-id="bbf0c-141">Return value</span></span>

<span data-ttu-id="bbf0c-142">S_OK</span><span class="sxs-lookup"><span data-stu-id="bbf0c-142">S_OK</span></span> 
  
> <span data-ttu-id="bbf0c-143">通知の登録が成功しました。</span><span class="sxs-lookup"><span data-stu-id="bbf0c-143">The notification registration was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bbf0c-144">注釈</span><span class="sxs-lookup"><span data-stu-id="bbf0c-144">Remarks</span></span>

<span data-ttu-id="bbf0c-145">**IMAPISupport::Subscribe** メソッドは、すべてのサービス プロバイダー サポート オブジェクトに実装されます。</span><span class="sxs-lookup"><span data-stu-id="bbf0c-145">The **IMAPISupport::Subscribe** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="bbf0c-146">サービス プロバイダーは、 **通知の管理** を MAPI に許可するために **、Advise** メソッドの 1 つから Subscribe を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="bbf0c-146">Service providers call **Subscribe** from one of their **Advise** methods to allow MAPI to manage the notifications.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="bbf0c-147">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="bbf0c-147">Notes to callers</span></span>

<span data-ttu-id="bbf0c-148">通知に MAPI サポート メソッドを使用するには、通知を生成する必要があるオブジェクトをアドバイス ソースのキーを作成します。</span><span class="sxs-lookup"><span data-stu-id="bbf0c-148">To use the MAPI support methods for notification, create a key for the advise source the object about which notifications should be generated.</span></span> <span data-ttu-id="bbf0c-149">キーの値は一意である必要があります。オブジェクトが変更されるごとに簡単に再生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bbf0c-149">The value of the key must be unique and should be easily regenerated each time the object changes.</span></span> 
  
<span data-ttu-id="bbf0c-150">MAPI は通知キーを使用して、対応するアドバイス ソースの [HrAllocAdviseSink](hrallocadvisesink.md) 関数を介して登録されたコールバック関数を検索します。</span><span class="sxs-lookup"><span data-stu-id="bbf0c-150">MAPI uses the notification key to search for any callback functions registered through the [HrAllocAdviseSink](hrallocadvisesink.md) function for the corresponding advise source.</span></span> <span data-ttu-id="bbf0c-151">このキーを **IMAPISupport::Notify に** 渡して、対応するアドバイス ソースの通知を生成する必要がある場合はいつでも通知します。</span><span class="sxs-lookup"><span data-stu-id="bbf0c-151">Pass this key to **IMAPISupport::Notify** whenever you need to generate a notification for the corresponding advise source.</span></span> 
  
<span data-ttu-id="bbf0c-152">このフラグNOTIFY_SYNCは、Notify への後続の呼び出しの操作に **影響します**。</span><span class="sxs-lookup"><span data-stu-id="bbf0c-152">The NOTIFY_SYNC flag affects the operation of subsequent calls to **Notify**.</span></span> <span data-ttu-id="bbf0c-153">[通知] NOTIFY_SYNC設定すると、必要なすべての通知の送信が完了するまで **、Notify** は返されません。</span><span class="sxs-lookup"><span data-stu-id="bbf0c-153">When you set NOTIFY_SYNC, **Notify** does not return until it has finished sending all of the necessary notifications.</span></span> <span data-ttu-id="bbf0c-154">通知を設定しない場合NOTIFY_SYNC通知は非同期的に動作し、すべての通知が送信される前に返される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="bbf0c-154">When you do not set NOTIFY_SYNC, **Notify** operates asynchronously, possibly returning before all of the notifications have been sent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bbf0c-155">関連項目</span><span class="sxs-lookup"><span data-stu-id="bbf0c-155">See also</span></span>



[<span data-ttu-id="bbf0c-156">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="bbf0c-156">HrAllocAdviseSink</span></span>](hrallocadvisesink.md)
  
[<span data-ttu-id="bbf0c-157">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="bbf0c-157">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="bbf0c-158">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="bbf0c-158">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
  
[<span data-ttu-id="bbf0c-159">�ʒm</span><span class="sxs-lookup"><span data-stu-id="bbf0c-159">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="bbf0c-160">NOTIFKEY</span><span class="sxs-lookup"><span data-stu-id="bbf0c-160">NOTIFKEY</span></span>](notifkey.md)
  
[<span data-ttu-id="bbf0c-161">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="bbf0c-161">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

