---
title: imapisessionunadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.Unadvise
api_type:
- COM
ms.assetid: 5e608cb0-808d-4418-8521-71dcbce8cdff
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 98a5faca00f5877eb10110406875b46a69244d94
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335703"
---
# <a name="imapisessionunadvise"></a><span data-ttu-id="6a72a-103">IMAPISession::Unadvise</span><span class="sxs-lookup"><span data-stu-id="6a72a-103">IMAPISession::Unadvise</span></span>

  
  
<span data-ttu-id="6a72a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6a72a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6a72a-105">[imapisession:: Advise](imapisession-advise.md)メソッドへの呼び出しを使用して、以前に設定した通知の送信をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="6a72a-105">Cancels the sending of notifications previously set up with a call to the [IMAPISession::Advise](imapisession-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="6a72a-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6a72a-106">Parameters</span></span>

 <span data-ttu-id="6a72a-107">_ulconnection_</span><span class="sxs-lookup"><span data-stu-id="6a72a-107">_ulConnection_</span></span>
  
> <span data-ttu-id="6a72a-108">順番アクティブな通知登録に関連付けられている接続番号。</span><span class="sxs-lookup"><span data-stu-id="6a72a-108">[in] A connection number associated with an active notification registration.</span></span> <span data-ttu-id="6a72a-109">_ulconnection_の値は、以前の**imapisession:: Advise**の呼び出しによって返されたものである必要があります。</span><span class="sxs-lookup"><span data-stu-id="6a72a-109">The value of  _ulConnection_ must have been returned by a previous call to **IMAPISession::Advise**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6a72a-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="6a72a-110">Return value</span></span>

<span data-ttu-id="6a72a-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="6a72a-111">S_OK</span></span> 
  
> <span data-ttu-id="6a72a-112">登録が正常にキャンセルされました。</span><span class="sxs-lookup"><span data-stu-id="6a72a-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6a72a-113">解説</span><span class="sxs-lookup"><span data-stu-id="6a72a-113">Remarks</span></span>

<span data-ttu-id="6a72a-114">**imapisession:: アドバイズ**中止メソッドは、通知の登録を取り消します。</span><span class="sxs-lookup"><span data-stu-id="6a72a-114">The **IMAPISession::Unadvise** method cancels a registration for notification.</span></span> <span data-ttu-id="6a72a-115">**アドバイズ**中止は、登録に使用された**アドバイズ**呼び出しで受け取った発信者のアドバイズシンクへのポインターを解放します。</span><span class="sxs-lookup"><span data-stu-id="6a72a-115">**Unadvise** releases its pointer to the caller's advise sink, which it received in the **Advise** call used for registration.</span></span> 
  
<span data-ttu-id="6a72a-116">通常、 \*\*\*\* アドバイズ中止呼び出し中にアドバイズシンクの[IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)メソッド\*\*\*\* を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6a72a-116">Generally, **Unadvise** calls the advise sink's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method during the **Unadvise** call.</span></span> <span data-ttu-id="6a72a-117">ただし、アドバイズシンクの[IMAPIAdviseSink:: onnotify](imapiadvisesink-onnotify.md)メソッドを呼び出しているプロセスに別のスレッドがある場合は、 **onnotify**メソッドが戻るまで**リリース**呼び出しが遅延します。</span><span class="sxs-lookup"><span data-stu-id="6a72a-117">However, if another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6a72a-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="6a72a-118">See also</span></span>



[<span data-ttu-id="6a72a-119">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="6a72a-119">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="6a72a-120">IMAPISession::Advise</span><span class="sxs-lookup"><span data-stu-id="6a72a-120">IMAPISession::Advise</span></span>](imapisession-advise.md)
  
[<span data-ttu-id="6a72a-121">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="6a72a-121">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)

