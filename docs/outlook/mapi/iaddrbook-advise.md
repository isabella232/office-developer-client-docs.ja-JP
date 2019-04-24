---
title: iaddrbookadvise
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7abafafd3d4bd9618d85a7dac34e4556545167bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334756"
---
# <a name="iaddrbookadvise"></a><span data-ttu-id="7a09a-103">IAddrBook::Advise</span><span class="sxs-lookup"><span data-stu-id="7a09a-103">IAddrBook::Advise</span></span>

  
  
<span data-ttu-id="7a09a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a09a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a09a-105">クライアントまたはサービスプロバイダーに、アドレス帳の1つまたは複数のエントリの変更に関する通知を受信するように登録します。</span><span class="sxs-lookup"><span data-stu-id="7a09a-105">Registers a client or service provider to receive notifications about changes to one or more entries in the address book.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="7a09a-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a09a-106">Parameters</span></span>

 <span data-ttu-id="7a09a-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="7a09a-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="7a09a-108">順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="7a09a-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="7a09a-109">_lて tryid_</span><span class="sxs-lookup"><span data-stu-id="7a09a-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="7a09a-110">順番_uleventmask_パラメーターに記述されている種類または種類の変更が発生したときに通知を生成するアドレス帳コンテナー、メッセージングユーザー、または配布リストのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7a09a-110">[in] A pointer to the entry identifier of the address book container, messaging user, or distribution list that will generate a notification when a change occurs of the type or types described in the  _ulEventMask_ parameter.</span></span> 
    
 <span data-ttu-id="7a09a-111">_uleventmask_</span><span class="sxs-lookup"><span data-stu-id="7a09a-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="7a09a-112">順番発信者が受信するように登録している1つ以上の通知イベント。</span><span class="sxs-lookup"><span data-stu-id="7a09a-112">[in] One or more notification events that the caller is registering to receive.</span></span> <span data-ttu-id="7a09a-113">各イベントは、発生した変更に関する情報を含む特定の通知構造に関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="7a09a-113">Each event is associated with a particular notification structure that contains information about the change that occurred.</span></span> <span data-ttu-id="7a09a-114">次の表に、 _uleventmask_の有効な値とそれに対応する構造を示します。</span><span class="sxs-lookup"><span data-stu-id="7a09a-114">The following table lists the valid values for  _ulEventMask_ and their corresponding structures.</span></span> 
    
|<span data-ttu-id="7a09a-115">**通知イベント**</span><span class="sxs-lookup"><span data-stu-id="7a09a-115">**Notification event**</span></span>|<span data-ttu-id="7a09a-116">**対応する構造**</span><span class="sxs-lookup"><span data-stu-id="7a09a-116">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7a09a-117">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="7a09a-117">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="7a09a-118">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="7a09a-118">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="7a09a-119">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="7a09a-119">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="7a09a-120">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="7a09a-120">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="7a09a-121">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="7a09a-121">**fnevObjectDeleted**</span></span> <br/> |[<span data-ttu-id="7a09a-122">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="7a09a-122">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="7a09a-123">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="7a09a-123">**fnevObjectModified**</span></span> <br/> |[<span data-ttu-id="7a09a-124">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="7a09a-124">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="7a09a-125">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="7a09a-125">**fnevObjectCopied**</span></span> <br/> |[<span data-ttu-id="7a09a-126">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="7a09a-126">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="7a09a-127">**fnevObjectMoved**</span><span class="sxs-lookup"><span data-stu-id="7a09a-127">**fnevObjectMoved**</span></span> <br/> |[<span data-ttu-id="7a09a-128">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="7a09a-128">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="7a09a-129">**fnevTableModified**</span><span class="sxs-lookup"><span data-stu-id="7a09a-129">**fnevTableModified**</span></span> <br/> |[<span data-ttu-id="7a09a-130">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="7a09a-130">TABLE_NOTIFICATION</span></span>](table_notification.md) <br/> |
   
 <span data-ttu-id="7a09a-131">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="7a09a-131">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="7a09a-132">順番通知が要求されたイベントが発生したときに呼び出されるアドバイズシンクオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="7a09a-132">[in] A pointer to the advise sink object to be called when the event for which notification has been requested occurs.</span></span>
    
 <span data-ttu-id="7a09a-133">_lアウト接続_</span><span class="sxs-lookup"><span data-stu-id="7a09a-133">_lpulConnection_</span></span>
  
> <span data-ttu-id="7a09a-134">読み上げ通知登録を表す0以外の接続番号へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7a09a-134">[out] A pointer to a nonzero connection number that represents the notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7a09a-135">戻り値</span><span class="sxs-lookup"><span data-stu-id="7a09a-135">Return value</span></span>

<span data-ttu-id="7a09a-136">S_OK</span><span class="sxs-lookup"><span data-stu-id="7a09a-136">S_OK</span></span> 
  
> <span data-ttu-id="7a09a-137">通知の登録に成功しました。</span><span class="sxs-lookup"><span data-stu-id="7a09a-137">The notification registration was successful.</span></span>
    
<span data-ttu-id="7a09a-138">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="7a09a-138">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="7a09a-139">_lな tryid_で渡されたエントリ id を処理するアドレス帳プロバイダーが、対応するエントリの通知を登録できませんでした。</span><span class="sxs-lookup"><span data-stu-id="7a09a-139">The address book provider responsible for the entry identifier passed in  _lpEntryID_ could not register a notification for the corresponding entry.</span></span> 
    
<span data-ttu-id="7a09a-140">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="7a09a-140">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="7a09a-141">通知は、 _lpentryid_パラメーターで渡されたエントリ id によって識別されるオブジェクトを担当するアドレス帳プロバイダーではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="7a09a-141">Notification is not supported by the address book provider responsible for the object identified by the entry identifier passed in the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="7a09a-142">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="7a09a-142">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="7a09a-143">_lな tryid_で渡されるエントリ識別子は、プロファイル内のどのアドレス帳プロバイダーでも処理できません。</span><span class="sxs-lookup"><span data-stu-id="7a09a-143">The entry identifier passed in  _lpEntryID_ cannot be handled by any of the address book providers in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7a09a-144">解説</span><span class="sxs-lookup"><span data-stu-id="7a09a-144">Remarks</span></span>

<span data-ttu-id="7a09a-145">クライアントおよびサービスプロバイダーは、**アドバイズ**メソッドを呼び出して、アドレス帳エントリの特定の種類または通知の種類を登録します。</span><span class="sxs-lookup"><span data-stu-id="7a09a-145">Clients and service providers call the **Advise** method to register for a particular type or types of notification on an address book entry.</span></span> <span data-ttu-id="7a09a-146">通知の種類は、 _uleventmask_パラメーターで渡されるイベントマスクによって示されます。</span><span class="sxs-lookup"><span data-stu-id="7a09a-146">The types of notification are indicated by the event mask passed in with the  _ulEventMask_ parameter.</span></span> 
  
<span data-ttu-id="7a09a-147">MAPI は、この**アドバイズ**呼び出しを、 _lpentryid_パラメーターのエントリ id で示されているように、エントリを担当するアドレス帳プロバイダーに転送します。</span><span class="sxs-lookup"><span data-stu-id="7a09a-147">MAPI forwards this **Advise** call to the address book provider that is responsible for the entry as indicated by the entry identifier in the  _lpEntryID_ parameter.</span></span> <span data-ttu-id="7a09a-148">アドレス帳プロバイダーは、登録自体を処理するか、または support メソッドの[imapisupport:: Subscribe](imapisupport-subscribe.md)を呼び出して、MAPI に発信者の登録を促します。</span><span class="sxs-lookup"><span data-stu-id="7a09a-148">The address book provider either handles the registration itself or calls the support method, [IMAPISupport::Subscribe](imapisupport-subscribe.md), to prompt MAPI to register the caller.</span></span> <span data-ttu-id="7a09a-149">成功した登録を表す、0以外の接続番号が返されます。</span><span class="sxs-lookup"><span data-stu-id="7a09a-149">A nonzero connection number is returned to represent the successful registration.</span></span>
  
<span data-ttu-id="7a09a-150">通知登録によって示される型のエントリが変更されるたびに、アドレス帳プロバイダーは、 _lpAdviseSink_パラメーターで指定されたアドバイズシンクオブジェクトの[IMAPIAdviseSink:: onnotify](imapiadvisesink-onnotify.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7a09a-150">Whenever a change occurs to the entry of the type indicated by the notification registration, the address book provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object specified in the  _lpAdviseSink_ parameter.</span></span> <span data-ttu-id="7a09a-151">**onnotify**メソッドには、イベントを記述するためのデータを含む入力パラメーターとして[通知](notification.md)構造が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7a09a-151">The **OnNotify** method includes a [NOTIFICATION](notification.md) structure as an input parameter that contains data to describe the event.</span></span> 
  
<span data-ttu-id="7a09a-152">アドレス帳プロバイダーに応じて、 **onnotify**への呼び出しは、登録されたオブジェクトへの変更の直後または後で発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="7a09a-152">Depending on the address book provider, the call to **OnNotify** can occur immediately following the change to the registered object or at a later time.</span></span> <span data-ttu-id="7a09a-153">複数の実行スレッドをサポートするシステムでは、 **onnotify**への呼び出しは任意のスレッドで発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7a09a-153">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="7a09a-154">クライアントは、 [HrThisThreadAdviseSink](hrthisthreadadvisesink.md)関数を呼び出して、**アドバイズ**に渡されるアドバイズシンクオブジェクトを作成することで、これらの通知が特定のスレッドで発生することを要求できます。</span><span class="sxs-lookup"><span data-stu-id="7a09a-154">Clients can request that these notifications occur on a particular thread by calling the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to create the advise sink object that is passed to **Advise**.</span></span> 
  
<span data-ttu-id="7a09a-155">アドレス帳プロバイダーは、**アドバイズ**呼び出しが正常に完了した後、 [IAddrBook:: アドバイズ](iaddrbook-unadvise.md)中止呼び出しの前にクライアントによって渡されたアドバイズシンクオブジェクトを解放できるため、通知をキャンセルするには、クライアントがリリースする必要があります。**アドバイズ**から返されるアドバイズシンクオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="7a09a-155">Because an address book provider can release the advise sink object passed in by clients at any time after the successful completion of the **Advise** call and before an [IAddrBook::Unadvise](iaddrbook-unadvise.md) call to cancel the notification, clients should release their advise sink objects when **Advise** returns.</span></span> 
  
<span data-ttu-id="7a09a-156">通知プロセスの詳細については、「 [MAPI でのイベント通知](event-notification-in-mapi.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7a09a-156">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7a09a-157">関連項目</span><span class="sxs-lookup"><span data-stu-id="7a09a-157">See also</span></span>



[<span data-ttu-id="7a09a-158">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="7a09a-158">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="7a09a-159">IAddrBook::Unadvise</span><span class="sxs-lookup"><span data-stu-id="7a09a-159">IAddrBook::Unadvise</span></span>](iaddrbook-unadvise.md)
  
[<span data-ttu-id="7a09a-160">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="7a09a-160">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="7a09a-161">�ʒm</span><span class="sxs-lookup"><span data-stu-id="7a09a-161">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="7a09a-162">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7a09a-162">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

