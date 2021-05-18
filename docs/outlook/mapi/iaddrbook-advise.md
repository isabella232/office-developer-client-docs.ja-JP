---
title: IAddrBookAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Advise
api_type:
- COM
ms.assetid: 2def89ed-e4ce-446a-8b80-132d11ae8f8b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7abafafd3d4bd9618d85a7dac34e4556545167bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406277"
---
# <a name="iaddrbookadvise"></a><span data-ttu-id="c1d83-103">IAddrBook::Advise</span><span class="sxs-lookup"><span data-stu-id="c1d83-103">IAddrBook::Advise</span></span>

  
  
<span data-ttu-id="c1d83-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1d83-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1d83-105">アドレス帳内の 1 つ以上のエントリに対する変更に関する通知を受信するクライアントまたはサービス プロバイダーを登録します。</span><span class="sxs-lookup"><span data-stu-id="c1d83-105">Registers a client or service provider to receive notifications about changes to one or more entries in the address book.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="c1d83-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c1d83-106">Parameters</span></span>

 <span data-ttu-id="c1d83-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="c1d83-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="c1d83-108">[in]  _lpEntryID_ パラメーターが指すエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="c1d83-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="c1d83-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="c1d83-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="c1d83-110">[in]  _ulEventMask_ パラメーターで説明されている型または型が変更された場合に通知を生成するアドレス帳コンテナー、メッセージング ユーザー、または配布リストのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c1d83-110">[in] A pointer to the entry identifier of the address book container, messaging user, or distribution list that will generate a notification when a change occurs of the type or types described in the  _ulEventMask_ parameter.</span></span> 
    
 <span data-ttu-id="c1d83-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="c1d83-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="c1d83-112">[in]発信者が受信登録している 1 つ以上の通知イベント。</span><span class="sxs-lookup"><span data-stu-id="c1d83-112">[in] One or more notification events that the caller is registering to receive.</span></span> <span data-ttu-id="c1d83-113">各イベントは、発生した変更に関する情報を含む特定の通知構造に関連付けられる。</span><span class="sxs-lookup"><span data-stu-id="c1d83-113">Each event is associated with a particular notification structure that contains information about the change that occurred.</span></span> <span data-ttu-id="c1d83-114">次の表に  _、ulEventMask_ とその対応する構造体の有効な値を示します。</span><span class="sxs-lookup"><span data-stu-id="c1d83-114">The following table lists the valid values for  _ulEventMask_ and their corresponding structures.</span></span> 
    
|<span data-ttu-id="c1d83-115">**通知イベント**</span><span class="sxs-lookup"><span data-stu-id="c1d83-115">**Notification event**</span></span>|<span data-ttu-id="c1d83-116">**対応する構造**</span><span class="sxs-lookup"><span data-stu-id="c1d83-116">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c1d83-117">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="c1d83-117">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="c1d83-118">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c1d83-118">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="c1d83-119">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="c1d83-119">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="c1d83-120">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c1d83-120">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="c1d83-121">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="c1d83-121">**fnevObjectDeleted**</span></span> <br/> |[<span data-ttu-id="c1d83-122">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c1d83-122">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="c1d83-123">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="c1d83-123">**fnevObjectModified**</span></span> <br/> |[<span data-ttu-id="c1d83-124">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c1d83-124">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="c1d83-125">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="c1d83-125">**fnevObjectCopied**</span></span> <br/> |[<span data-ttu-id="c1d83-126">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c1d83-126">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="c1d83-127">**fnevObjectMoved**</span><span class="sxs-lookup"><span data-stu-id="c1d83-127">**fnevObjectMoved**</span></span> <br/> |[<span data-ttu-id="c1d83-128">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c1d83-128">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="c1d83-129">**fnevTableModified**</span><span class="sxs-lookup"><span data-stu-id="c1d83-129">**fnevTableModified**</span></span> <br/> |[<span data-ttu-id="c1d83-130">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c1d83-130">TABLE_NOTIFICATION</span></span>](table_notification.md) <br/> |
   
 <span data-ttu-id="c1d83-131">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="c1d83-131">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="c1d83-132">[in]通知が要求されたイベントが発生した場合に呼び出されるアアドバイス シンク オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="c1d83-132">[in] A pointer to the advise sink object to be called when the event for which notification has been requested occurs.</span></span>
    
 <span data-ttu-id="c1d83-133">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="c1d83-133">_lpulConnection_</span></span>
  
> <span data-ttu-id="c1d83-134">[out]通知登録を表す 0 以外の接続番号へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c1d83-134">[out] A pointer to a nonzero connection number that represents the notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c1d83-135">戻り値</span><span class="sxs-lookup"><span data-stu-id="c1d83-135">Return value</span></span>

<span data-ttu-id="c1d83-136">S_OK</span><span class="sxs-lookup"><span data-stu-id="c1d83-136">S_OK</span></span> 
  
> <span data-ttu-id="c1d83-137">通知の登録が成功しました。</span><span class="sxs-lookup"><span data-stu-id="c1d83-137">The notification registration was successful.</span></span>
    
<span data-ttu-id="c1d83-138">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="c1d83-138">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="c1d83-139">_lpEntryID_ で渡されたエントリ識別子を担当するアドレス帳プロバイダーは、対応するエントリの通知を登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c1d83-139">The address book provider responsible for the entry identifier passed in  _lpEntryID_ could not register a notification for the corresponding entry.</span></span> 
    
<span data-ttu-id="c1d83-140">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="c1d83-140">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="c1d83-141">通知は  _、lpEntryID_ パラメーターで渡されたエントリ識別子によって識別されるオブジェクトを担当するアドレス帳プロバイダーではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="c1d83-141">Notification is not supported by the address book provider responsible for the object identified by the entry identifier passed in the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="c1d83-142">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="c1d83-142">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="c1d83-143">_lpEntryID_ で渡されたエントリ識別子は、プロファイル内のアドレス帳プロバイダーでは処理できません。</span><span class="sxs-lookup"><span data-stu-id="c1d83-143">The entry identifier passed in  _lpEntryID_ cannot be handled by any of the address book providers in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c1d83-144">注釈</span><span class="sxs-lookup"><span data-stu-id="c1d83-144">Remarks</span></span>

<span data-ttu-id="c1d83-145">クライアントとサービス プロバイダーは、 **アドレス** 帳エントリの特定の種類または種類の通知に登録するために、Advise メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c1d83-145">Clients and service providers call the **Advise** method to register for a particular type or types of notification on an address book entry.</span></span> <span data-ttu-id="c1d83-146">通知の種類は  _、ulEventMask_ パラメーターで渡されたイベント マスクによって示されます。</span><span class="sxs-lookup"><span data-stu-id="c1d83-146">The types of notification are indicated by the event mask passed in with the  _ulEventMask_ parameter.</span></span> 
  
<span data-ttu-id="c1d83-147">MAPI は、lpEntryID パラメーターのエントリ識別子で示されているエントリを担当するアドレス帳プロバイダーに、この Advise 呼び出し _を転送_ します。 </span><span class="sxs-lookup"><span data-stu-id="c1d83-147">MAPI forwards this **Advise** call to the address book provider that is responsible for the entry as indicated by the entry identifier in the  _lpEntryID_ parameter.</span></span> <span data-ttu-id="c1d83-148">アドレス帳プロバイダーは、登録自体を処理するか、サポート メソッド [IMAPISupport::Subscribe](imapisupport-subscribe.md)を呼び出して、MAPI に発信者の登録を促します。</span><span class="sxs-lookup"><span data-stu-id="c1d83-148">The address book provider either handles the registration itself or calls the support method, [IMAPISupport::Subscribe](imapisupport-subscribe.md), to prompt MAPI to register the caller.</span></span> <span data-ttu-id="c1d83-149">正常な登録を表す 0 以外の接続番号が返されます。</span><span class="sxs-lookup"><span data-stu-id="c1d83-149">A nonzero connection number is returned to represent the successful registration.</span></span>
  
<span data-ttu-id="c1d83-150">通知登録によって示される型のエントリに変更が発生するたびに、アドレス帳プロバイダーは _、lpAdviseSink_ パラメーターで指定されたアドバイス シンク オブジェクトの [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c1d83-150">Whenever a change occurs to the entry of the type indicated by the notification registration, the address book provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object specified in the  _lpAdviseSink_ parameter.</span></span> <span data-ttu-id="c1d83-151">**OnNotify メソッドには**、[イベント](notification.md)を記述するデータを含む入力パラメーターとして NOTIFICATION 構造が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c1d83-151">The **OnNotify** method includes a [NOTIFICATION](notification.md) structure as an input parameter that contains data to describe the event.</span></span> 
  
<span data-ttu-id="c1d83-152">アドレス帳プロバイダーに応じて **、OnNotify** への呼び出しは、登録されたオブジェクトへの変更直後、または後で発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c1d83-152">Depending on the address book provider, the call to **OnNotify** can occur immediately following the change to the registered object or at a later time.</span></span> <span data-ttu-id="c1d83-153">複数の実行スレッドをサポートするシステムでは **、OnNotify** の呼び出しは任意のスレッドで行われます。</span><span class="sxs-lookup"><span data-stu-id="c1d83-153">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="c1d83-154">クライアントは [、HrThisThreadAdviseSink](hrthisthreadadvisesink.md) 関数を呼び出して、Advise に渡されるアアドバイス シンク オブジェクトを作成することで、これらの通知が特定のスレッドで発生する要求 **を行えます**。</span><span class="sxs-lookup"><span data-stu-id="c1d83-154">Clients can request that these notifications occur on a particular thread by calling the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to create the advise sink object that is passed to **Advise**.</span></span> 
  
<span data-ttu-id="c1d83-155">アドレス帳プロバイダーは、Advise 呼び出しが正常に完了した後、および通知をキャンセルする [IAddrBook::Unadvise](iaddrbook-unadvise.md)呼び出しの前に、クライアントが渡したアアドバイス シンク オブジェクトをいつでも解放できます。クライアントは **、Advise** が返されると、そのアアドバイス シンク オブジェクトを解放する必要があります。 </span><span class="sxs-lookup"><span data-stu-id="c1d83-155">Because an address book provider can release the advise sink object passed in by clients at any time after the successful completion of the **Advise** call and before an [IAddrBook::Unadvise](iaddrbook-unadvise.md) call to cancel the notification, clients should release their advise sink objects when **Advise** returns.</span></span> 
  
<span data-ttu-id="c1d83-156">通知プロセスの詳細については、「MAPI での [イベント通知」を参照してください](event-notification-in-mapi.md)。</span><span class="sxs-lookup"><span data-stu-id="c1d83-156">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c1d83-157">関連項目</span><span class="sxs-lookup"><span data-stu-id="c1d83-157">See also</span></span>



[<span data-ttu-id="c1d83-158">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="c1d83-158">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="c1d83-159">IAddrBook::Unadvise</span><span class="sxs-lookup"><span data-stu-id="c1d83-159">IAddrBook::Unadvise</span></span>](iaddrbook-unadvise.md)
  
[<span data-ttu-id="c1d83-160">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="c1d83-160">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="c1d83-161">�ʒm</span><span class="sxs-lookup"><span data-stu-id="c1d83-161">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="c1d83-162">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c1d83-162">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

