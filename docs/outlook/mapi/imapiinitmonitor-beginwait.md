---
title: imapiinitmonitor-beginwait
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIINITMONITOR.BeginWait
api_type:
- COM
ms.assetid: 71f565a9-651c-42b5-9102-91b728b681ae
description: IMAPIInitMonitor::BeginWait"
Last modified: April 26, 2021
ms.openlocfilehash: 43a88507cbfc23b3b842f51e69eb4bd791bcfda8
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062019"
---
# <a name="imapiinitmonitorbeginwait"></a><span data-ttu-id="3ebc1-103">IMAPIInitMonitor::BeginWait</span><span class="sxs-lookup"><span data-stu-id="3ebc1-103">IMAPIInitMonitor::BeginWait</span></span>
  
<span data-ttu-id="3ebc1-104">**適用対象 :** Outlook 2016 |2019</span><span class="sxs-lookup"><span data-stu-id="3ebc1-104">**Applies to**: Outlook 2016 | 2019</span></span>
  
<span data-ttu-id="3ebc1-105">MAPI の初期化または指定した経過時間 (ミリ秒単位) の待機を開始します。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-105">Start a wait for MAPI initialization or the specified number of milliseconds to elapse.</span></span> <span data-ttu-id="3ebc1-106">これにより、IMAPIWaitResult::End を呼び出して待機を開始する必要がある **IMAPIWaitResult** インターフェイスが返されます。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-106">This returns an IMAPIWaitResult interface which should have **IMAPIWaitResult::End** called in order initiate the wait.</span></span> <span data-ttu-id="3ebc1-107">これにより、呼び出し元は、待機中にブロックされるスレッドを制御できます。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-107">This allows the caller to control which thread is blocked while we are waiting.</span></span>

```cpp
HRESULT IMAPIInitMonitor::BeginWait(DWORD timeout, IMAPIWaitResult** ppResult)
```

## <a name="parameters"></a><span data-ttu-id="3ebc1-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3ebc1-108">Parameters</span></span>
<span data-ttu-id="3ebc1-109">_timeout_</span><span class="sxs-lookup"><span data-stu-id="3ebc1-109">_timeout_</span></span>
><span data-ttu-id="3ebc1-110">[in]MAPI の初期化を待機するミリ秒単位で、初期化が実行されるのを永遠に待機するために INFINITE に設定できます。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-110">[in] The number of millisecond to wait for MAPI initialization, this can set to INFINITE to wait forever for the initialization to happen.</span></span>

<span data-ttu-id="3ebc1-111">_ppResult_</span><span class="sxs-lookup"><span data-stu-id="3ebc1-111">_ppResult_</span></span>
><span data-ttu-id="3ebc1-112">[out]新しく作成された待機インターフェイスを受け取るポインター。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-112">[out] A pointer to recieve the newly create wait interface.</span></span>

## <a name="return-value"></a><span data-ttu-id="3ebc1-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="3ebc1-113">Return value</span></span>
<span data-ttu-id="3ebc1-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="3ebc1-114">S_OK</span></span>
><span data-ttu-id="3ebc1-115">待機操作が正常に開始されました。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-115">A wait operation was successfully started.</span></span>

<span data-ttu-id="3ebc1-116">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="3ebc1-116">E_OUTOFMEMORY</span></span>
><span data-ttu-id="3ebc1-117">新しいオブジェクトを作成するのに十分なメモリがなかった</span><span class="sxs-lookup"><span data-stu-id="3ebc1-117">There was not enough memory to create a new object</span></span>

## <a name="remarks"></a><span data-ttu-id="3ebc1-118">解説</span><span class="sxs-lookup"><span data-stu-id="3ebc1-118">Remarks</span></span>
<span data-ttu-id="3ebc1-119">この API は、呼び出し元にインターフェイス (スレッド セーフ) を提供し、MAPI 初期化のブロック待機を開始できます。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-119">This API provided the caller with an interface (which is thread-safe) which can be used initiate a blocking wait for MAPI initialization.</span></span> <span data-ttu-id="3ebc1-120">これにより、コンシューマーはアプリケーションを待つ最も良い待ち時間を取りやめできます。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-120">This allows the consumer to deterime the best wait to wait for thier application.</span></span>   <span data-ttu-id="3ebc1-121">IMAPIWaitResult::End を呼び出す動作は、IMAPIInitMonitor::Wait の呼び出しと同じです。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-121">The behavior of calling IMAPIWaitResult::End is identical to calling IMAPIInitMonitor::Wait.</span></span>

## <a name="see-also"></a><span data-ttu-id="3ebc1-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="3ebc1-122">See also</span></span>

[<span data-ttu-id="3ebc1-123">IMAPIInitMonitor</span><span class="sxs-lookup"><span data-stu-id="3ebc1-123">IMAPIInitMonitor</span></span>](imapiinitmonitoriunknown.md)

[<span data-ttu-id="3ebc1-124">IMAPIInitMonitor::IsInitialized</span><span class="sxs-lookup"><span data-stu-id="3ebc1-124">IMAPIInitMonitor::IsInitialized</span></span>](imapiinitmonitor-isinitialized.md)

[<span data-ttu-id="3ebc1-125">IMAPIInitMonitor::Wait</span><span class="sxs-lookup"><span data-stu-id="3ebc1-125">IMAPIInitMonitor::Wait</span></span>](imapiinitmonitor-wait.md)

[<span data-ttu-id="3ebc1-126">CreateMAPIInitializationMonitor</span><span class="sxs-lookup"><span data-stu-id="3ebc1-126">CreateMAPIInitializationMonitor</span></span>](createmapiinitializationmonitor.md)

[<span data-ttu-id="3ebc1-127">IMAPIWaitResult</span><span class="sxs-lookup"><span data-stu-id="3ebc1-127">IMAPIWaitResult</span></span>](imapiwaitresultiunknown.md)
