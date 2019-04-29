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
# <a name="iablogonunadvise"></a><span data-ttu-id="f0344-103">IABLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="f0344-103">IABLogon::Unadvise</span></span>

  
  
<span data-ttu-id="f0344-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f0344-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f0344-105">[IABLogon:: Advise](iablogon-advise.md)メソッドの呼び出しで以前に設定された通知をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="f0344-105">Cancels notifications that were previously set up with a call to the [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="f0344-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f0344-106">Parameters</span></span>

 <span data-ttu-id="f0344-107">_ulconnection_</span><span class="sxs-lookup"><span data-stu-id="f0344-107">_ulConnection_</span></span>
  
> <span data-ttu-id="f0344-108">順番アクティブな通知登録に関連付けられている接続番号。</span><span class="sxs-lookup"><span data-stu-id="f0344-108">[in] The connection number associated with an active notification registration.</span></span> <span data-ttu-id="f0344-109">**アドバイズ**の前の呼び出しでは、 _ulconnection_の値が返されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="f0344-109">A previous call to **Advise** must have returned the value of  _ulConnection_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f0344-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="f0344-110">Return value</span></span>

<span data-ttu-id="f0344-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="f0344-111">S_OK</span></span> 
  
> <span data-ttu-id="f0344-112">通知登録が正常にキャンセルされました。</span><span class="sxs-lookup"><span data-stu-id="f0344-112">The notification registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f0344-113">注釈</span><span class="sxs-lookup"><span data-stu-id="f0344-113">Remarks</span></span>

<span data-ttu-id="f0344-114">MAPI は、**アドバイズ**中止メソッドを呼び出して、コンテナー、メッセージングユーザー、または配布リストオブジェクトの通知の登録を取り消します。</span><span class="sxs-lookup"><span data-stu-id="f0344-114">MAPI calls the **Unadvise** method to cancel a notification registration for a container, messaging user, or distribution list object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f0344-115">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="f0344-115">Notes to implementers</span></span>

<span data-ttu-id="f0344-116">**アドバイズ**の実装は、MAPI のヘルプまたは手動で通知をサポートしているかどうかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="f0344-116">Your implementation of **Unadvise** will depend on whether you support notification with MAPI's help or manually.</span></span> <span data-ttu-id="f0344-117">MAPI がサポートを提供する場合は、 [imapisupport:: 講読解除](imapisupport-unsubscribe.md)メソッドを呼び出して、登録を取り消します。</span><span class="sxs-lookup"><span data-stu-id="f0344-117">If MAPI provides your support, call the [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md) method to cancel the registration.</span></span> <span data-ttu-id="f0344-118">別のスレッドがアドバイズシンクの[IMAPIAdviseSink:: onnotify](imapiadvisesink-onnotify.md)メソッドを呼び出しているプロセス内にある場合は、 **onnotify**が返されるまで遅延させることができます。</span><span class="sxs-lookup"><span data-stu-id="f0344-118">If another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, it can be delayed until **OnNotify** has returned.</span></span> 
  
<span data-ttu-id="f0344-119">通知プロセスの詳細については、「 [MAPI でのイベント通知](event-notification-in-mapi.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f0344-119">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="f0344-120">[imapisupport:](imapisupportiunknown.md)通知をサポートするための IUnknown メソッドの使用方法については、「[サポートイベントの通知](supporting-event-notification.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f0344-120">For information about how to use the [IMAPISupport : IUnknown](imapisupportiunknown.md) methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f0344-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="f0344-121">See also</span></span>



[<span data-ttu-id="f0344-122">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="f0344-122">IABLogon::Advise</span></span>](iablogon-advise.md)
  
[<span data-ttu-id="f0344-123">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="f0344-123">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="f0344-124">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f0344-124">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

