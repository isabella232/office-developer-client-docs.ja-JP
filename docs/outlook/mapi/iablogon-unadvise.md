---
title: IABLogonUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.Unadvise
api_type:
- COM
ms.assetid: 3e506b29-c7e3-40d6-a08b-22fa87088c2d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: fe87de4466413e317edea5d358c9e4769d0c5593
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424078"
---
# <a name="iablogonunadvise"></a><span data-ttu-id="f07bc-103">IABLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="f07bc-103">IABLogon::Unadvise</span></span>

  
  
<span data-ttu-id="f07bc-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f07bc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f07bc-105">[IABLogon::Advise](iablogon-advise.md)メソッドへの呼び出しで以前に設定された通知をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="f07bc-105">Cancels notifications that were previously set up with a call to the [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="f07bc-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f07bc-106">Parameters</span></span>

 <span data-ttu-id="f07bc-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="f07bc-107">_ulConnection_</span></span>
  
> <span data-ttu-id="f07bc-108">[in]アクティブな通知登録に関連付けられている接続番号。</span><span class="sxs-lookup"><span data-stu-id="f07bc-108">[in] The connection number associated with an active notification registration.</span></span> <span data-ttu-id="f07bc-109">Advise の以前の **呼び出しでは**_、ulConnection の値が返されている必要があります_。</span><span class="sxs-lookup"><span data-stu-id="f07bc-109">A previous call to **Advise** must have returned the value of  _ulConnection_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f07bc-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="f07bc-110">Return value</span></span>

<span data-ttu-id="f07bc-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="f07bc-111">S_OK</span></span> 
  
> <span data-ttu-id="f07bc-112">通知登録が正常に取り消されました。</span><span class="sxs-lookup"><span data-stu-id="f07bc-112">The notification registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f07bc-113">注釈</span><span class="sxs-lookup"><span data-stu-id="f07bc-113">Remarks</span></span>

<span data-ttu-id="f07bc-114">MAPI は **Unadvise メソッドを呼** び出して、コンテナー、メッセージング ユーザー、または配布リスト オブジェクトの通知登録を取り消します。</span><span class="sxs-lookup"><span data-stu-id="f07bc-114">MAPI calls the **Unadvise** method to cancel a notification registration for a container, messaging user, or distribution list object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f07bc-115">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="f07bc-115">Notes to implementers</span></span>

<span data-ttu-id="f07bc-116">**Unadvise の実装は**、MAPI のヘルプを使用して通知をサポートするか手動でサポートするかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="f07bc-116">Your implementation of **Unadvise** will depend on whether you support notification with MAPI's help or manually.</span></span> <span data-ttu-id="f07bc-117">MAPI がサポートを提供している場合は [、IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md) メソッドを呼び出して登録を取り消します。</span><span class="sxs-lookup"><span data-stu-id="f07bc-117">If MAPI provides your support, call the [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md) method to cancel the registration.</span></span> <span data-ttu-id="f07bc-118">別のスレッドがアアドバイス シンクの [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) メソッドを呼び出す過程にある場合 **、OnNotify** が返されるまで遅延する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f07bc-118">If another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, it can be delayed until **OnNotify** has returned.</span></span> 
  
<span data-ttu-id="f07bc-119">通知プロセスの詳細については、「MAPI での [イベント通知」を参照してください](event-notification-in-mapi.md)。</span><span class="sxs-lookup"><span data-stu-id="f07bc-119">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="f07bc-120">[IMAPISupport : IUnknown](imapisupportiunknown.md)メソッドを使用して通知をサポートする方法については、「Support Event Notification 」[を参照してください](supporting-event-notification.md)。</span><span class="sxs-lookup"><span data-stu-id="f07bc-120">For information about how to use the [IMAPISupport : IUnknown](imapisupportiunknown.md) methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f07bc-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="f07bc-121">See also</span></span>



[<span data-ttu-id="f07bc-122">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="f07bc-122">IABLogon::Advise</span></span>](iablogon-advise.md)
  
[<span data-ttu-id="f07bc-123">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="f07bc-123">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="f07bc-124">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f07bc-124">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

