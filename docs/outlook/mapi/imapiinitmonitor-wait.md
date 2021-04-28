---
title: imapiinitmonitor-wait
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIINITMONITOR.Wait
api_type:
- COM
ms.assetid: ed566cae-35a2-4716-817b-54d1ba6825c6
description: IMAPIAMonitor::Wait
Last modified: April 26, 2021
ms.openlocfilehash: ee46a2744e67804c9dfdac8d7512db1d7b07f8ba
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062012"
---
# <a name="imapiinitmonitorwait"></a><span data-ttu-id="8d006-103">IMAPIInitMonitor::Wait</span><span class="sxs-lookup"><span data-stu-id="8d006-103">IMAPIInitMonitor::Wait</span></span>
  
<span data-ttu-id="8d006-104">**適用対象 :** Outlook 2013 |Outlook 2016 |2019</span><span class="sxs-lookup"><span data-stu-id="8d006-104">**Applies to**: Outlook 2013 | Outlook 2016 | 2019</span></span>
  
<span data-ttu-id="8d006-105">このスレッドで BLOCKING 呼び出しを開始します。指定したミリ秒数が経過するか、MAPI が初期化された場合に返されます。</span><span class="sxs-lookup"><span data-stu-id="8d006-105">Initiates a BLOCKING call on this thread, which will return either when the specified number of milliseconds have elapsed or MAPI has been initialized.</span></span> <span data-ttu-id="8d006-106">INFINITE は、無限の待機に使用できます。</span><span class="sxs-lookup"><span data-stu-id="8d006-106">INFINITE can be used to for an infinite wait.</span></span>

```cpp
HRESULT IMAPIInitMonitor::Wait(DWORD timeout)
```

## <a name="parameters"></a><span data-ttu-id="8d006-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8d006-107">Parameters</span></span>
<span data-ttu-id="8d006-108">_timeout_</span><span class="sxs-lookup"><span data-stu-id="8d006-108">_timeout_</span></span>
> <span data-ttu-id="8d006-109">[in]MAPI が初期化されるのを待つミリ秒単位で、INFINITE (0xFFFFFFFF) を渡して永遠に待機できます。</span><span class="sxs-lookup"><span data-stu-id="8d006-109">[in] The number of milliseconds to wait for MAPI to be initialized, you can pass INFINITE (0xFFFFFFFF) to wait forever.</span></span>

## <a name="return-value"></a><span data-ttu-id="8d006-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="8d006-110">Return value</span></span>

<span data-ttu-id="8d006-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="8d006-111">S_OK</span></span>
> <span data-ttu-id="8d006-112">MAPI が正常に初期化されました。</span><span class="sxs-lookup"><span data-stu-id="8d006-112">MAPI has been initialized successfully.</span></span>

<span data-ttu-id="8d006-113">HRESULT_FROM_WIN32(ERROR_TIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="8d006-113">HRESULT_FROM_WIN32(ERROR_TIMEOUT)</span></span>
> <span data-ttu-id="8d006-114">無限でないタイムアウトが与えられた場合、これは MAPI が初期化されていない期間を示します。</span><span class="sxs-lookup"><span data-stu-id="8d006-114">When given a non-infinite timeout this indicates MAPI was not initialized during that period.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d006-115">解説</span><span class="sxs-lookup"><span data-stu-id="8d006-115">Remarks</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8d006-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="8d006-116">See also</span></span>

[<span data-ttu-id="8d006-117">IMAPIInitMonitor</span><span class="sxs-lookup"><span data-stu-id="8d006-117">IMAPIInitMonitor</span></span>](imapiinitmonitoriunknown.md)

[<span data-ttu-id="8d006-118">IMAPIInitMonitor::IsInitialized</span><span class="sxs-lookup"><span data-stu-id="8d006-118">IMAPIInitMonitor::IsInitialized</span></span>](imapiinitmonitor-isinitialized.md)

[<span data-ttu-id="8d006-119">IMAPIInitMonitor::BeginWait</span><span class="sxs-lookup"><span data-stu-id="8d006-119">IMAPIInitMonitor::BeginWait</span></span>](imapiinitmonitor-beginwait.md)

[<span data-ttu-id="8d006-120">CreateMAPIInitializationMonitor</span><span class="sxs-lookup"><span data-stu-id="8d006-120">CreateMAPIInitializationMonitor</span></span>](createmapiinitializationmonitor.md)

[<span data-ttu-id="8d006-121">IMAPIWaitResult</span><span class="sxs-lookup"><span data-stu-id="8d006-121">IMAPIWaitResult</span></span>](imapiwaitresultiunknown.md)
