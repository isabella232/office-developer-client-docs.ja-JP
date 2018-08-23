---
title: IMsgStoreUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.Unadvise
api_type:
- COM
ms.assetid: 1394039b-d509-49a5-8421-b7362d906879
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 516de39d721c532c003775bd366a52ed8144ab88
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801041"
---
# <a name="imsgstoreunadvise"></a><span data-ttu-id="ff7d9-103">IMsgStore::Unadvise</span><span class="sxs-lookup"><span data-stu-id="ff7d9-103">IMsgStore::Unadvise</span></span>

  
  
<span data-ttu-id="ff7d9-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ff7d9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ff7d9-105">[IMsgStore::Advise](imsgstore-advise.md)メソッドへの呼び出しは、設定済みの通知の送信をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="ff7d9-105">Cancels the sending of notifications previously set up with a call to the [IMsgStore::Advise](imsgstore-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="ff7d9-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ff7d9-106">Parameters</span></span>

 <span data-ttu-id="ff7d9-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="ff7d9-107">_ulConnection_</span></span>
  
> <span data-ttu-id="ff7d9-108">[in]作業中の通知の登録に関連付けられている接続の数です。</span><span class="sxs-lookup"><span data-stu-id="ff7d9-108">[in] The connection number associated with an active notification registration.</span></span> <span data-ttu-id="ff7d9-109">_UlConnection_の値は、 **IMsgStore::Advise**メソッドへの前回の呼び出しで返されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff7d9-109">The value of  _ulConnection_ must have been returned by a previous call to the **IMsgStore::Advise** method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ff7d9-110">�߂�l</span><span class="sxs-lookup"><span data-stu-id="ff7d9-110">Return value</span></span>

<span data-ttu-id="ff7d9-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="ff7d9-111">S_OK</span></span> 
  
> <span data-ttu-id="ff7d9-112">登録は取り消されました。</span><span class="sxs-lookup"><span data-stu-id="ff7d9-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ff7d9-113">注釈</span><span class="sxs-lookup"><span data-stu-id="ff7d9-113">Remarks</span></span>

<span data-ttu-id="ff7d9-114">**IMsgStore::Unadvise**メソッドは、通知の登録をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="ff7d9-114">The **IMsgStore::Unadvise** method cancels a registration for notification.</span></span> <span data-ttu-id="ff7d9-115">**Unadvise**リリースがそのポインターを呼び出し元のシンクの登録に使用される**アドバイス**の呼び出しで、受け取ったに案内します。</span><span class="sxs-lookup"><span data-stu-id="ff7d9-115">**Unadvise** releases its pointer to the caller's advise sink, which it received in the **Advise** call used for registration.</span></span> 
  
<span data-ttu-id="ff7d9-116">一般に、 **Unadvise**は**Unadvise**の呼び出し時にアドバイズ シンクの[リ ス](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx)のメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ff7d9-116">Generally, **Unadvise** calls the advise sink's [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) method during the **Unadvise** call.</span></span> <span data-ttu-id="ff7d9-117">ただし、別のスレッドがアドバイズ シンクの[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出すことであるにある場合は、**リリース**の呼び出しが遅延**OnNotify**メソッドが戻るまで。</span><span class="sxs-lookup"><span data-stu-id="ff7d9-117">However, if another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ff7d9-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="ff7d9-118">See also</span></span>



[<span data-ttu-id="ff7d9-119">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="ff7d9-119">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="ff7d9-120">IMsgStore::Advise</span><span class="sxs-lookup"><span data-stu-id="ff7d9-120">IMsgStore::Advise</span></span>](imsgstore-advise.md)
  
[<span data-ttu-id="ff7d9-121">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ff7d9-121">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

