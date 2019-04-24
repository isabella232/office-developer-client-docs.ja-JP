---
title: HrDispatchNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrDispatchNotifications
api_type:
- COM
ms.assetid: 42ec4266-67b9-416e-8b9b-163c95011626
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f4af3f2fd094942c48e02849c60f3e46acb1a5f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348098"
---
# <a name="hrdispatchnotifications"></a><span data-ttu-id="bea50-103">HrDispatchNotifications</span><span class="sxs-lookup"><span data-stu-id="bea50-103">HrDispatchNotifications</span></span>

  
  
<span data-ttu-id="bea50-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bea50-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bea50-105">キューに入っているすべての通知を強制的にディスパッチします。</span><span class="sxs-lookup"><span data-stu-id="bea50-105">Forces dispatching of all queued notifications.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bea50-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="bea50-106">Header file:</span></span>  <br/> |<span data-ttu-id="bea50-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="bea50-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="bea50-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="bea50-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="bea50-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="bea50-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="bea50-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="bea50-110">Called by:</span></span>  <br/> |<span data-ttu-id="bea50-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="bea50-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrDispatchNotifications(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="bea50-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bea50-112">Parameters</span></span>

 <span data-ttu-id="bea50-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bea50-113">_ulFlags_</span></span>
  
> <span data-ttu-id="bea50-114">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="bea50-114">[in] Reserved; must be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="bea50-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="bea50-115">Return value</span></span>

<span data-ttu-id="bea50-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="bea50-116">S_OK</span></span>
  
> <span data-ttu-id="bea50-117">キューに入っているすべての通知がディスパッチされました。</span><span class="sxs-lookup"><span data-stu-id="bea50-117">All queued notifications have been dispatched.</span></span>
    
<span data-ttu-id="bea50-118">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="bea50-118">MAPI_E_USER_CANCEL</span></span>
  
> <span data-ttu-id="bea50-119">WM_QUIT、WM_QUERYENDSESSION、または WM_ENDSESSION を受信しました。</span><span class="sxs-lookup"><span data-stu-id="bea50-119">WM_QUIT, WM_QUERYENDSESSION, or WM_ENDSESSION was received.</span></span>
    
<span data-ttu-id="bea50-120">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="bea50-120">MAPI_E_NOT_INITIALIZED</span></span>
  
> <span data-ttu-id="bea50-121">MAPI が初期化されていません。</span><span class="sxs-lookup"><span data-stu-id="bea50-121">MAPI was not initialized.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bea50-122">解説</span><span class="sxs-lookup"><span data-stu-id="bea50-122">Remarks</span></span>

<span data-ttu-id="bea50-123">**HrDispatchNotifications**関数を使用すると、mapi は、メッセージのディスパッチを待つことなく、現在 mapi 通知エンジンでキューに入れられているすべての通知をディスパッチします。</span><span class="sxs-lookup"><span data-stu-id="bea50-123">The **HrDispatchNotifications** function causes MAPI to dispatch all notifications that are currently queued in the MAPI notification engine without waiting for a message dispatch.</span></span> <span data-ttu-id="bea50-124">これにより、メモリ使用率に対する効果が向上します。</span><span class="sxs-lookup"><span data-stu-id="bea50-124">This can have a beneficial effect on memory utilization.</span></span> <span data-ttu-id="bea50-125">詳細については、「[強制的な通知](forcing-a-notification.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bea50-125">For more information, see [Forcing a Notification](forcing-a-notification.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="bea50-126">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="bea50-126">Notes to callers</span></span>

<span data-ttu-id="bea50-127">一部のアプリケーションは、Windows の[PeekMessage](https://msdn.microsoft.com/library/ms644943.aspx)関数と[DispatchMessage](https://msdn.microsoft.com/library/ms644934.aspx)関数を使用して、タイムアウトループで通知メッセージを待機します。</span><span class="sxs-lookup"><span data-stu-id="bea50-127">Some applications wait for a notification message in a timeout loop using the Windows [PeekMessage](https://msdn.microsoft.com/library/ms644943.aspx) and [DispatchMessage](https://msdn.microsoft.com/library/ms644934.aspx) functions.</span></span> <span data-ttu-id="bea50-128">最速のプラットフォームを除くすべてのプラットフォームで、このようなアプリケーションでは、パフォーマンスが低下したり、通知がブロックされることもあります。</span><span class="sxs-lookup"><span data-stu-id="bea50-128">On all but the fastest platforms, such applications might experience poor performance or even blockage of notifications.</span></span> <span data-ttu-id="bea50-129">**HrDispatchNotifications**を使用すると、コードが減少するだけでなく、パフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="bea50-129">Using **HrDispatchNotifications** not only reduces code but improves performance.</span></span> 
  

