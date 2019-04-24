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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: f85b662b7fe710c66a2e69dd3cd3db22e3283ddb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309724"
---
# <a name="imsgstoreunadvise"></a><span data-ttu-id="56809-103">IMsgStore::Unadvise</span><span class="sxs-lookup"><span data-stu-id="56809-103">IMsgStore::Unadvise</span></span>

  
  
<span data-ttu-id="56809-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="56809-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="56809-105">[IMsgStore:: Advise](imsgstore-advise.md)メソッドへの呼び出しによって、以前に設定された通知の送信をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="56809-105">Cancels the sending of notifications previously set up with a call to the [IMsgStore::Advise](imsgstore-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="56809-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="56809-106">Parameters</span></span>

 <span data-ttu-id="56809-107">_ulconnection_</span><span class="sxs-lookup"><span data-stu-id="56809-107">_ulConnection_</span></span>
  
> <span data-ttu-id="56809-108">順番アクティブな通知登録に関連付けられている接続番号。</span><span class="sxs-lookup"><span data-stu-id="56809-108">[in] The connection number associated with an active notification registration.</span></span> <span data-ttu-id="56809-109">_ulconnection_の値は、 **IMsgStore:: Advise**メソッドへの以前の呼び出しによって返されたものである必要があります。</span><span class="sxs-lookup"><span data-stu-id="56809-109">The value of  _ulConnection_ must have been returned by a previous call to the **IMsgStore::Advise** method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="56809-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="56809-110">Return value</span></span>

<span data-ttu-id="56809-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="56809-111">S_OK</span></span> 
  
> <span data-ttu-id="56809-112">登録が正常にキャンセルされました。</span><span class="sxs-lookup"><span data-stu-id="56809-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="56809-113">解説</span><span class="sxs-lookup"><span data-stu-id="56809-113">Remarks</span></span>

<span data-ttu-id="56809-114">**IMsgStore:: アドバイズ**中止メソッドは、通知の登録をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="56809-114">The **IMsgStore::Unadvise** method cancels a registration for notification.</span></span> <span data-ttu-id="56809-115">**アドバイズ**中止は、登録に使用された**アドバイズ**呼び出しで受け取った発信者のアドバイズシンクへのポインターを解放します。</span><span class="sxs-lookup"><span data-stu-id="56809-115">**Unadvise** releases its pointer to the caller's advise sink, which it received in the **Advise** call used for registration.</span></span> 
  
<span data-ttu-id="56809-116">通常、 \*\*\*\* アドバイズ中止呼び出し中にアドバイズシンクの[IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)メソッド\*\*\*\* を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="56809-116">Generally, **Unadvise** calls the advise sink's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method during the **Unadvise** call.</span></span> <span data-ttu-id="56809-117">ただし、アドバイズシンクの[IMAPIAdviseSink:: onnotify](imapiadvisesink-onnotify.md)メソッドを呼び出しているプロセスに別のスレッドがある場合は、 **onnotify**メソッドが戻るまで**リリース**呼び出しが遅延します。</span><span class="sxs-lookup"><span data-stu-id="56809-117">However, if another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="56809-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="56809-118">See also</span></span>



[<span data-ttu-id="56809-119">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="56809-119">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="56809-120">IMsgStore::Advise</span><span class="sxs-lookup"><span data-stu-id="56809-120">IMsgStore::Advise</span></span>](imsgstore-advise.md)
  
[<span data-ttu-id="56809-121">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="56809-121">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

