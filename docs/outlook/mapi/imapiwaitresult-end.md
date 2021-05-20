---
title: IMAPIWaitResult::End
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIWaitResult.End
api_type:
- COM
ms.assetid: 7463c9e8-d065-4cc3-ac01-d428b57bbc88
description: IMAPIWaitResult::End
Last modified: April 26, 2021
ms.openlocfilehash: 3432bf3b71fa7e15cb4621d461a8d4bbe962f1ba
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062033"
---
# <a name="imapiwaitresultend"></a><span data-ttu-id="bc3a9-103">IMAPIWaitResult::End</span><span class="sxs-lookup"><span data-stu-id="bc3a9-103">IMAPIWaitResult::End</span></span>
  
<span data-ttu-id="bc3a9-104">**適用対象 :** Outlook 2013 |Outlook 2016 |2019</span><span class="sxs-lookup"><span data-stu-id="bc3a9-104">**Applies to**: Outlook 2013 | Outlook 2016 | 2019</span></span>

<span data-ttu-id="bc3a9-105">このスレッドで BLOCKING 呼び出しを開始します。指定したミリ秒数が経過するか、MAPI が初期化された場合に返されます。</span><span class="sxs-lookup"><span data-stu-id="bc3a9-105">Initiates a BLOCKING call on this thread, which will return either when the specified number of milliseconds have elapsed or MAPI has been initialized.</span></span> <span data-ttu-id="bc3a9-106">INFINITE は、無限の待機に使用できます。</span><span class="sxs-lookup"><span data-stu-id="bc3a9-106">INFINITE can be used to for an infinite wait.</span></span>

```cpp
HRESULT IMAPIWaitResult::End(DWORD timeout)
```

## <a name="parameters"></a><span data-ttu-id="bc3a9-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bc3a9-107">Parameters</span></span>

<span data-ttu-id="bc3a9-108">_timeout_</span><span class="sxs-lookup"><span data-stu-id="bc3a9-108">_timeout_</span></span>
> <span data-ttu-id="bc3a9-109">[in]MAPI が初期化されるのを待つミリ秒単位で、INFINITE (0xFFFFFFFF) を渡して永遠に待機できます。</span><span class="sxs-lookup"><span data-stu-id="bc3a9-109">[in] The number of millisecond to wait for MAPI to be initialized, you can pass INFINITE (0xFFFFFFFF) to wait forever.</span></span>

## <a name="return-value"></a><span data-ttu-id="bc3a9-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="bc3a9-110">Return value</span></span>

<span data-ttu-id="bc3a9-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="bc3a9-111">S_OK</span></span>
> <span data-ttu-id="bc3a9-112">MAPI が正常に初期化されました</span><span class="sxs-lookup"><span data-stu-id="bc3a9-112">MAPI has been initialized successfully</span></span>

<span data-ttu-id="bc3a9-113">HRESULT_FROM_WIN32(ERROR_TIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="bc3a9-113">HRESULT_FROM_WIN32(ERROR_TIMEOUT)</span></span>
> <span data-ttu-id="bc3a9-114">無限でないタイムアウトが与えられた場合、これは MAPI が初期化されていない期間を示します。</span><span class="sxs-lookup"><span data-stu-id="bc3a9-114">When given a non-infinite timeout this indicates MAPI was not initialized during that period.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc3a9-115">注釈</span><span class="sxs-lookup"><span data-stu-id="bc3a9-115">Remarks</span></span>
<span data-ttu-id="bc3a9-116">この API は [、IMAPInitMonitor::Wait とまったく同じ動作をします](imapiinitmonitor-wait.md)。</span><span class="sxs-lookup"><span data-stu-id="bc3a9-116">This API behaves exactly the same as [IMAPInitMonitor::Wait](imapiinitmonitor-wait.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bc3a9-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="bc3a9-117">See also</span></span>

[<span data-ttu-id="bc3a9-118">IMAPIInitMonitor::IsInitialized</span><span class="sxs-lookup"><span data-stu-id="bc3a9-118">IMAPIInitMonitor::IsInitialized</span></span>](imapiinitmonitor-isinitialized.md)

[<span data-ttu-id="bc3a9-119">IMAPIInitMonitor::BeginWait</span><span class="sxs-lookup"><span data-stu-id="bc3a9-119">IMAPIInitMonitor::BeginWait</span></span>](imapiinitmonitor-beginwait.md)

[<span data-ttu-id="bc3a9-120">CreateMAPIInitializationMonitor</span><span class="sxs-lookup"><span data-stu-id="bc3a9-120">CreateMAPIInitializationMonitor</span></span>](createmapiinitializationmonitor.md)

[<span data-ttu-id="bc3a9-121">IMAPIWaitResult</span><span class="sxs-lookup"><span data-stu-id="bc3a9-121">IMAPIWaitResult</span></span>](imapiwaitresultiunknown.md)
