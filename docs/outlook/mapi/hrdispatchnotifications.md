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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f4af3f2fd094942c48e02849c60f3e46acb1a5f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348098"
---
# <a name="hrdispatchnotifications"></a><span data-ttu-id="14b25-103">HrDispatchNotifications</span><span class="sxs-lookup"><span data-stu-id="14b25-103">HrDispatchNotifications</span></span>

  
  
<span data-ttu-id="14b25-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="14b25-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="14b25-105">キューに入っているすべての通知を強制的にディスパッチします。</span><span class="sxs-lookup"><span data-stu-id="14b25-105">Forces dispatching of all queued notifications.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="14b25-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="14b25-106">Header file:</span></span>  <br/> |<span data-ttu-id="14b25-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="14b25-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="14b25-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="14b25-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="14b25-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="14b25-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="14b25-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="14b25-110">Called by:</span></span>  <br/> |<span data-ttu-id="14b25-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="14b25-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrDispatchNotifications(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="14b25-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="14b25-112">Parameters</span></span>

 <span data-ttu-id="14b25-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="14b25-113">_ulFlags_</span></span>
  
> <span data-ttu-id="14b25-114">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="14b25-114">[in] Reserved; must be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="14b25-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="14b25-115">Return value</span></span>

<span data-ttu-id="14b25-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="14b25-116">S_OK</span></span>
  
> <span data-ttu-id="14b25-117">キューに登録された通知はすべてディスパッチされています。</span><span class="sxs-lookup"><span data-stu-id="14b25-117">All queued notifications have been dispatched.</span></span>
    
<span data-ttu-id="14b25-118">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="14b25-118">MAPI_E_USER_CANCEL</span></span>
  
> <span data-ttu-id="14b25-119">WM_QUIT、WM_QUERYENDSESSION、またはWM_ENDSESSION受信しました。</span><span class="sxs-lookup"><span data-stu-id="14b25-119">WM_QUIT, WM_QUERYENDSESSION, or WM_ENDSESSION was received.</span></span>
    
<span data-ttu-id="14b25-120">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="14b25-120">MAPI_E_NOT_INITIALIZED</span></span>
  
> <span data-ttu-id="14b25-121">MAPI が初期化されていません。</span><span class="sxs-lookup"><span data-stu-id="14b25-121">MAPI was not initialized.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="14b25-122">注釈</span><span class="sxs-lookup"><span data-stu-id="14b25-122">Remarks</span></span>

<span data-ttu-id="14b25-123">**HrDispatchNotifications** 関数を使用すると、MAPI は、メッセージのディスパッチを待たずに、MAPI 通知エンジンに現在キューに入っているすべての通知をディスパッチします。</span><span class="sxs-lookup"><span data-stu-id="14b25-123">The **HrDispatchNotifications** function causes MAPI to dispatch all notifications that are currently queued in the MAPI notification engine without waiting for a message dispatch.</span></span> <span data-ttu-id="14b25-124">これは、メモリ使用率に有益な影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="14b25-124">This can have a beneficial effect on memory utilization.</span></span> <span data-ttu-id="14b25-125">詳細については、「通知の [送信」を参照してください](forcing-a-notification.md)。</span><span class="sxs-lookup"><span data-stu-id="14b25-125">For more information, see [Forcing a Notification](forcing-a-notification.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="14b25-126">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="14b25-126">Notes to callers</span></span>

<span data-ttu-id="14b25-127">一部のアプリケーションは、PeekMessage 関数と[DispatchMessage](https://msdn.microsoft.com/library/ms644943.aspx)関数を使用して、タイムアウト ループWindows[を待機](https://msdn.microsoft.com/library/ms644934.aspx)します。</span><span class="sxs-lookup"><span data-stu-id="14b25-127">Some applications wait for a notification message in a timeout loop using the Windows [PeekMessage](https://msdn.microsoft.com/library/ms644943.aspx) and [DispatchMessage](https://msdn.microsoft.com/library/ms644934.aspx) functions.</span></span> <span data-ttu-id="14b25-128">最も高速なプラットフォームを含むすべてのプラットフォームでは、このようなアプリケーションのパフォーマンスが低下したり、通知がブロックされる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="14b25-128">On all but the fastest platforms, such applications might experience poor performance or even blockage of notifications.</span></span> <span data-ttu-id="14b25-129">**HrDispatchNotifications を使用すると、コード** が減少するだけでなく、パフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="14b25-129">Using **HrDispatchNotifications** not only reduces code but improves performance.</span></span> 
  

