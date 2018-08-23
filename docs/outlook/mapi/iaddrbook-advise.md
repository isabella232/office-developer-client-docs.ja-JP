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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 43569b22cace7b2700d37ace49fd734b45fec73c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580881"
---
# <a name="iaddrbookadvise"></a><span data-ttu-id="038c3-103">IAddrBook::Advise</span><span class="sxs-lookup"><span data-stu-id="038c3-103">IAddrBook::Advise</span></span>

  
  
<span data-ttu-id="038c3-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="038c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="038c3-105">アドレス帳の 1 つまたは複数のエントリへの変更に関する通知を受信するクライアントまたはサービス プロバイダーを登録します。</span><span class="sxs-lookup"><span data-stu-id="038c3-105">Registers a client or service provider to receive notifications about changes to one or more entries in the address book.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="038c3-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="038c3-106">Parameters</span></span>

 <span data-ttu-id="038c3-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="038c3-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="038c3-108">[in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="038c3-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="038c3-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="038c3-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="038c3-110">[in]メッセージング ユーザー、または_ulEventMask_パラメーターで示された種類の変更が発生したときに通知を生成する配布リスト、アドレス帳コンテナーのエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="038c3-110">[in] A pointer to the entry identifier of the address book container, messaging user, or distribution list that will generate a notification when a change occurs of the type or types described in the  _ulEventMask_ parameter.</span></span> 
    
 <span data-ttu-id="038c3-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="038c3-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="038c3-112">[in]受け取る、呼び出し元を登録する 1 つ以上の通知イベントです。</span><span class="sxs-lookup"><span data-stu-id="038c3-112">[in] One or more notification events that the caller is registering to receive.</span></span> <span data-ttu-id="038c3-113">各イベントは、発生した変更に関する情報を含む特定の通知構造体に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="038c3-113">Each event is associated with a particular notification structure that contains information about the change that occurred.</span></span> <span data-ttu-id="038c3-114">_UlEventMask_およびそれらに対応する構造体の有効な値を次の表に一覧します。</span><span class="sxs-lookup"><span data-stu-id="038c3-114">The following table lists the valid values for  _ulEventMask_ and their corresponding structures.</span></span> 
    
|<span data-ttu-id="038c3-115">**通知イベント**</span><span class="sxs-lookup"><span data-stu-id="038c3-115">**Notification event**</span></span>|<span data-ttu-id="038c3-116">**対応する構造体**</span><span class="sxs-lookup"><span data-stu-id="038c3-116">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="038c3-117">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="038c3-117">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="038c3-118">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="038c3-118">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="038c3-119">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="038c3-119">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="038c3-120">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="038c3-120">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="038c3-121">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="038c3-121">**fnevObjectDeleted**</span></span> <br/> |[<span data-ttu-id="038c3-122">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="038c3-122">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="038c3-123">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="038c3-123">**fnevObjectModified**</span></span> <br/> |[<span data-ttu-id="038c3-124">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="038c3-124">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="038c3-125">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="038c3-125">**fnevObjectCopied**</span></span> <br/> |[<span data-ttu-id="038c3-126">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="038c3-126">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="038c3-127">**fnevObjectMoved**</span><span class="sxs-lookup"><span data-stu-id="038c3-127">**fnevObjectMoved**</span></span> <br/> |[<span data-ttu-id="038c3-128">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="038c3-128">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="038c3-129">**fnevTableModified**</span><span class="sxs-lookup"><span data-stu-id="038c3-129">**fnevTableModified**</span></span> <br/> |[<span data-ttu-id="038c3-130">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="038c3-130">TABLE_NOTIFICATION</span></span>](table_notification.md) <br/> |
   
 <span data-ttu-id="038c3-131">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="038c3-131">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="038c3-132">[in]オブジェクトへのポインター、アドバイズ シンクの通知の要求対象となるイベントが発生したときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="038c3-132">[in] A pointer to the advise sink object to be called when the event for which notification has been requested occurs.</span></span>
    
 <span data-ttu-id="038c3-133">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="038c3-133">_lpulConnection_</span></span>
  
> <span data-ttu-id="038c3-134">[out]通知の登録を表す、0 以外の接続数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="038c3-134">[out] A pointer to a nonzero connection number that represents the notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="038c3-135">�߂�l</span><span class="sxs-lookup"><span data-stu-id="038c3-135">Return value</span></span>

<span data-ttu-id="038c3-136">S_OK</span><span class="sxs-lookup"><span data-stu-id="038c3-136">S_OK</span></span> 
  
> <span data-ttu-id="038c3-137">通知の登録に成功しました。</span><span class="sxs-lookup"><span data-stu-id="038c3-137">The notification registration was successful.</span></span>
    
<span data-ttu-id="038c3-138">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="038c3-138">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="038c3-139">_LpEntryID_に渡されたエントリ id のアドレス帳プロバイダーは、対応するエントリの通知を登録できませんでした。</span><span class="sxs-lookup"><span data-stu-id="038c3-139">The address book provider responsible for the entry identifier passed in  _lpEntryID_ could not register a notification for the corresponding entry.</span></span> 
    
<span data-ttu-id="038c3-140">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="038c3-140">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="038c3-141">通知は、 _lpEntryID_パラメーターで渡されたエントリ id によって識別されるオブジェクトのアドレス帳のプロバイダーではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="038c3-141">Notification is not supported by the address book provider responsible for the object identified by the entry identifier passed in the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="038c3-142">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="038c3-142">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="038c3-143">_LpEntryID_に渡されたエントリ id は、プロファイル内のアドレス帳プロバイダーのいずれかが処理できません。</span><span class="sxs-lookup"><span data-stu-id="038c3-143">The entry identifier passed in  _lpEntryID_ cannot be handled by any of the address book providers in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="038c3-144">注釈</span><span class="sxs-lookup"><span data-stu-id="038c3-144">Remarks</span></span>

<span data-ttu-id="038c3-145">クライアントとサービス ・ プロバイダー**の特定の種類または種類のアドレス帳エントリに通知を登録するメソッド**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="038c3-145">Clients and service providers call the **Advise** method to register for a particular type or types of notification on an address book entry.</span></span> <span data-ttu-id="038c3-146">通知の種類は、 _ulEventMask_パラメーターに渡されるイベント マスクによって示されます。</span><span class="sxs-lookup"><span data-stu-id="038c3-146">The types of notification are indicated by the event mask passed in with the  _ulEventMask_ parameter.</span></span> 
  
<span data-ttu-id="038c3-147">MAPI では、 _lpEntryID_パラメーターのエントリの識別子で示されるエントリは、アドレス帳プロバイダーにこの**アドバイス**の呼び出しを転送します。</span><span class="sxs-lookup"><span data-stu-id="038c3-147">MAPI forwards this **Advise** call to the address book provider that is responsible for the entry as indicated by the entry identifier in the  _lpEntryID_ parameter.</span></span> <span data-ttu-id="038c3-148">アドレス帳プロバイダーは、登録自体を処理するか、または[IMAPISupport::Subscribe](imapisupport-subscribe.md)、呼び出し元を登録するのには MAPI メッセージを表示するのには、サポート メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="038c3-148">The address book provider either handles the registration itself or calls the support method, [IMAPISupport::Subscribe](imapisupport-subscribe.md), to prompt MAPI to register the caller.</span></span> <span data-ttu-id="038c3-149">登録の成功を表す、0 以外の接続の数が返されます。</span><span class="sxs-lookup"><span data-stu-id="038c3-149">A nonzero connection number is returned to represent the successful registration.</span></span>
  
<span data-ttu-id="038c3-150">通知の登録で指定された種類のエントリに変更が発生すると、アドレス帳プロバイダーは、 _lpAdviseSink_パラメーターで指定されているアドバイズ シンク オブジェクトの[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="038c3-150">Whenever a change occurs to the entry of the type indicated by the notification registration, the address book provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object specified in the  _lpAdviseSink_ parameter.</span></span> <span data-ttu-id="038c3-151">**OnNotify**メソッドには、イベントを記述するデータを含む入力パラメーターとして、[通知](notification.md)の構造体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="038c3-151">The **OnNotify** method includes a [NOTIFICATION](notification.md) structure as an input parameter that contains data to describe the event.</span></span> 
  
<span data-ttu-id="038c3-152">アドレス帳プロバイダーによって登録されているオブジェクトに、または後で変更の直後**OnNotify**への呼び出しが発生します。</span><span class="sxs-lookup"><span data-stu-id="038c3-152">Depending on the address book provider, the call to **OnNotify** can occur immediately following the change to the registered object or at a later time.</span></span> <span data-ttu-id="038c3-153">複数の実行スレッドをサポートしているシステムでは、任意のスレッドで**OnNotify**への呼び出しが発生します。</span><span class="sxs-lookup"><span data-stu-id="038c3-153">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="038c3-154">**アドバイズ**に渡されるアドバイズ シンク オブジェクトを作成する[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)関数を呼び出すことで特定のスレッドでこれらの通知が発生するクライアントを要求できます。</span><span class="sxs-lookup"><span data-stu-id="038c3-154">Clients can request that these notifications occur on a particular thread by calling the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to create the advise sink object that is passed to **Advise**.</span></span> 
  
<span data-ttu-id="038c3-155">クライアントが解放する必要がありますので、アドレス帳プロバイダーが**アドバイズ**を正常に完了が呼び出すし、 [IAddrBook::Unadvise](iaddrbook-unadvise.md)する前に呼び出しの通知をキャンセルした後は、いつでもクライアントから渡されたアドバイズ シンク オブジェクトを解放できます。アドバイズ シンク オブジェクト**アドバイズ**が返されるときにします。</span><span class="sxs-lookup"><span data-stu-id="038c3-155">Because an address book provider can release the advise sink object passed in by clients at any time after the successful completion of the **Advise** call and before an [IAddrBook::Unadvise](iaddrbook-unadvise.md) call to cancel the notification, clients should release their advise sink objects when **Advise** returns.</span></span> 
  
<span data-ttu-id="038c3-156">通知プロセスの詳細については、 [MAPI でのイベントの通知](event-notification-in-mapi.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="038c3-156">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="038c3-157">関連項目</span><span class="sxs-lookup"><span data-stu-id="038c3-157">See also</span></span>



[<span data-ttu-id="038c3-158">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="038c3-158">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="038c3-159">IAddrBook::Unadvise</span><span class="sxs-lookup"><span data-stu-id="038c3-159">IAddrBook::Unadvise</span></span>](iaddrbook-unadvise.md)
  
[<span data-ttu-id="038c3-160">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="038c3-160">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="038c3-161">�ʒm</span><span class="sxs-lookup"><span data-stu-id="038c3-161">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="038c3-162">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="038c3-162">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

