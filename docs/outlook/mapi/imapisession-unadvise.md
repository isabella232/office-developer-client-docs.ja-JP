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
ms.openlocfilehash: 25f80ddce60ab5a8966a62761d234accafbb54be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800711"
---
# <a name="imapisessionunadvise"></a><span data-ttu-id="5f388-103">IMAPISession::Unadvise</span><span class="sxs-lookup"><span data-stu-id="5f388-103">IMAPISession::Unadvise</span></span>

  
  
<span data-ttu-id="5f388-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5f388-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5f388-105">[IMAPISession::Advise](imapisession-advise.md)メソッドへの呼び出しは、設定済みの通知の送信をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="5f388-105">Cancels the sending of notifications previously set up with a call to the [IMAPISession::Advise](imapisession-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="5f388-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="5f388-106">Parameters</span></span>

 <span data-ttu-id="5f388-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="5f388-107">_ulConnection_</span></span>
  
> <span data-ttu-id="5f388-108">[in]作業中の通知の登録に関連付けられている接続の数です。</span><span class="sxs-lookup"><span data-stu-id="5f388-108">[in] A connection number associated with an active notification registration.</span></span> <span data-ttu-id="5f388-109">_UlConnection_の値は、 **IMAPISession::Advise**以前の呼び出しで返されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f388-109">The value of  _ulConnection_ must have been returned by a previous call to **IMAPISession::Advise**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5f388-110">�߂�l</span><span class="sxs-lookup"><span data-stu-id="5f388-110">Return value</span></span>

<span data-ttu-id="5f388-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="5f388-111">S_OK</span></span> 
  
> <span data-ttu-id="5f388-112">登録は取り消されました。</span><span class="sxs-lookup"><span data-stu-id="5f388-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5f388-113">備考</span><span class="sxs-lookup"><span data-stu-id="5f388-113">Remarks</span></span>

<span data-ttu-id="5f388-114">**IMAPISession::Unadvise**メソッドは、通知の登録をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="5f388-114">The **IMAPISession::Unadvise** method cancels a registration for notification.</span></span> <span data-ttu-id="5f388-115">**Unadvise**リリースがそのポインターを呼び出し元のシンクの登録に使用される**アドバイス**の呼び出しで、受け取ったに案内します。</span><span class="sxs-lookup"><span data-stu-id="5f388-115">**Unadvise** releases its pointer to the caller's advise sink, which it received in the **Advise** call used for registration.</span></span> 
  
<span data-ttu-id="5f388-116">一般に、 **Unadvise**は**Unadvise**の呼び出し時にアドバイズ シンクの[リ ス](http://msdn.microsoft.com/ja-jp/library/ms682317%28v=VS.85%29.aspx)のメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5f388-116">Generally, **Unadvise** calls the advise sink's [IUnknown::Release](http://msdn.microsoft.com/ja-jp/library/ms682317%28v=VS.85%29.aspx) method during the **Unadvise** call.</span></span> <span data-ttu-id="5f388-117">ただし、別のスレッドがアドバイズ シンクの[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出すことであるにある場合は、**リリース**の呼び出しが遅延**OnNotify**メソッドが戻るまで。</span><span class="sxs-lookup"><span data-stu-id="5f388-117">However, if another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5f388-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="5f388-118">See also</span></span>



[<span data-ttu-id="5f388-119">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="5f388-119">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="5f388-120">IMAPISession::Advise</span><span class="sxs-lookup"><span data-stu-id="5f388-120">IMAPISession::Advise</span></span>](imapisession-advise.md)
  
[<span data-ttu-id="5f388-121">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="5f388-121">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)

