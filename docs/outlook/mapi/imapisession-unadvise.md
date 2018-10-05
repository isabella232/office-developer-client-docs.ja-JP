---
title: IMAPISessionUnadvise
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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 98a5faca00f5877eb10110406875b46a69244d94
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397892"
---
# <a name="imapisessionunadvise"></a><span data-ttu-id="c7657-103">IMAPISession::Unadvise</span><span class="sxs-lookup"><span data-stu-id="c7657-103">IMAPISession::Unadvise</span></span>

  
  
<span data-ttu-id="c7657-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c7657-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c7657-105">[IMAPISession::Advise](imapisession-advise.md)メソッドへの呼び出しは、設定済みの通知の送信をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="c7657-105">Cancels the sending of notifications previously set up with a call to the [IMAPISession::Advise](imapisession-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="c7657-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c7657-106">Parameters</span></span>

 <span data-ttu-id="c7657-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="c7657-107">_ulConnection_</span></span>
  
> <span data-ttu-id="c7657-108">[in]作業中の通知の登録に関連付けられている接続の数です。</span><span class="sxs-lookup"><span data-stu-id="c7657-108">[in] A connection number associated with an active notification registration.</span></span> <span data-ttu-id="c7657-109">_UlConnection_の値は、 **IMAPISession::Advise**以前の呼び出しで返されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="c7657-109">The value of  _ulConnection_ must have been returned by a previous call to **IMAPISession::Advise**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c7657-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="c7657-110">Return value</span></span>

<span data-ttu-id="c7657-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="c7657-111">S_OK</span></span> 
  
> <span data-ttu-id="c7657-112">登録は取り消されました。</span><span class="sxs-lookup"><span data-stu-id="c7657-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c7657-113">備考</span><span class="sxs-lookup"><span data-stu-id="c7657-113">Remarks</span></span>

<span data-ttu-id="c7657-114">**IMAPISession::Unadvise**メソッドは、通知の登録をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="c7657-114">The **IMAPISession::Unadvise** method cancels a registration for notification.</span></span> <span data-ttu-id="c7657-115">**Unadvise**リリースがそのポインターを呼び出し元のシンクの登録に使用される**アドバイス**の呼び出しで、受け取ったに案内します。</span><span class="sxs-lookup"><span data-stu-id="c7657-115">**Unadvise** releases its pointer to the caller's advise sink, which it received in the **Advise** call used for registration.</span></span> 
  
<span data-ttu-id="c7657-116">一般に、 **Unadvise**は**Unadvise**の呼び出し時にアドバイズ シンクの[リ ス](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)のメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c7657-116">Generally, **Unadvise** calls the advise sink's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method during the **Unadvise** call.</span></span> <span data-ttu-id="c7657-117">ただし、別のスレッドがアドバイズ シンクの[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出すことであるにある場合は、**リリース**の呼び出しが遅延**OnNotify**メソッドが戻るまで。</span><span class="sxs-lookup"><span data-stu-id="c7657-117">However, if another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c7657-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="c7657-118">See also</span></span>



[<span data-ttu-id="c7657-119">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="c7657-119">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="c7657-120">IMAPISession::Advise</span><span class="sxs-lookup"><span data-stu-id="c7657-120">IMAPISession::Advise</span></span>](imapisession-advise.md)
  
[<span data-ttu-id="c7657-121">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="c7657-121">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)

