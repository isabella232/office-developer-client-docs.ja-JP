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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: d9f69098f9c53e75dea6f485248d61d277e181c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800356"
---
# <a name="iablogonunadvise"></a><span data-ttu-id="fa08c-103">IABLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="fa08c-103">IABLogon::Unadvise</span></span>

  
  
<span data-ttu-id="fa08c-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fa08c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fa08c-105">[IABLogon::Advise](iablogon-advise.md)メソッドの呼び出しで以前設定された通知をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="fa08c-105">Cancels notifications that were previously set up with a call to the [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="fa08c-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="fa08c-106">Parameters</span></span>

 <span data-ttu-id="fa08c-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="fa08c-107">_ulConnection_</span></span>
  
> <span data-ttu-id="fa08c-108">[in]作業中の通知の登録に関連付けられている接続の数です。</span><span class="sxs-lookup"><span data-stu-id="fa08c-108">[in] The connection number associated with an active notification registration.</span></span> <span data-ttu-id="fa08c-109">**アドバイズ**する前回の呼び出しには、 _ulConnection_の値を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="fa08c-109">A previous call to **Advise** must have returned the value of  _ulConnection_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fa08c-110">�߂�l</span><span class="sxs-lookup"><span data-stu-id="fa08c-110">Return value</span></span>

<span data-ttu-id="fa08c-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="fa08c-111">S_OK</span></span> 
  
> <span data-ttu-id="fa08c-112">通知の登録は取り消されました。</span><span class="sxs-lookup"><span data-stu-id="fa08c-112">The notification registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fa08c-113">注釈</span><span class="sxs-lookup"><span data-stu-id="fa08c-113">Remarks</span></span>

<span data-ttu-id="fa08c-114">MAPI では、メッセージングのユーザーまたは配布リスト オブジェクトのコンテナーであり、通知の登録をキャンセルするのには**Unadvise**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="fa08c-114">MAPI calls the **Unadvise** method to cancel a notification registration for a container, messaging user, or distribution list object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="fa08c-115">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="fa08c-115">Notes to implementers</span></span>

<span data-ttu-id="fa08c-116">**Unadvise**の実装は、MAPI のヘルプまたは手動での通知をサポートするかどうかに依存します。</span><span class="sxs-lookup"><span data-stu-id="fa08c-116">Your implementation of **Unadvise** will depend on whether you support notification with MAPI's help or manually.</span></span> <span data-ttu-id="fa08c-117">MAPI のサポートを提供する場合は、登録をキャンセルする[IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="fa08c-117">If MAPI provides your support, call the [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md) method to cancel the registration.</span></span> <span data-ttu-id="fa08c-118">別のスレッドがアドバイズ シンクの[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出すことであるにある場合は、 **OnNotify**が返されるまで遅延できます。</span><span class="sxs-lookup"><span data-stu-id="fa08c-118">If another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, it can be delayed until **OnNotify** has returned.</span></span> 
  
<span data-ttu-id="fa08c-119">通知プロセスの詳細については、 [MAPI でのイベントの通知](event-notification-in-mapi.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fa08c-119">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="fa08c-120">使用する方法の詳細については、 [IMAPISupport: IUnknown](imapisupportiunknown.md)通知をサポートするメソッドは、[イベント通知をサポートしている](supporting-event-notification.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fa08c-120">For information about how to use the [IMAPISupport : IUnknown](imapisupportiunknown.md) methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fa08c-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="fa08c-121">See also</span></span>



[<span data-ttu-id="fa08c-122">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="fa08c-122">IABLogon::Advise</span></span>](iablogon-advise.md)
  
[<span data-ttu-id="fa08c-123">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="fa08c-123">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="fa08c-124">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fa08c-124">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

