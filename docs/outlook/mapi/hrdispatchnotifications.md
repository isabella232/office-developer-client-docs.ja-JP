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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385565"
---
# <a name="hrdispatchnotifications"></a><span data-ttu-id="9ac53-103">HrDispatchNotifications</span><span class="sxs-lookup"><span data-stu-id="9ac53-103">HrDispatchNotifications</span></span>

  
  
<span data-ttu-id="9ac53-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ac53-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ac53-105">フォースは、キューに登録されたすべての通知のディスパッチします。</span><span class="sxs-lookup"><span data-stu-id="9ac53-105">Forces dispatching of all queued notifications.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9ac53-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="9ac53-106">Header file:</span></span>  <br/> |<span data-ttu-id="9ac53-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="9ac53-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="9ac53-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="9ac53-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9ac53-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9ac53-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9ac53-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="9ac53-110">Called by:</span></span>  <br/> |<span data-ttu-id="9ac53-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="9ac53-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrDispatchNotifications(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="9ac53-112">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="9ac53-112">Parameters</span></span>

 <span data-ttu-id="9ac53-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9ac53-113">_ulFlags_</span></span>
  
> <span data-ttu-id="9ac53-114">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="9ac53-114">[in] Reserved; must be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9ac53-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="9ac53-115">Return value</span></span>

<span data-ttu-id="9ac53-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="9ac53-116">S_OK</span></span>
  
> <span data-ttu-id="9ac53-117">すべてのキューに登録された通知がディスパッチされました。</span><span class="sxs-lookup"><span data-stu-id="9ac53-117">All queued notifications have been dispatched.</span></span>
    
<span data-ttu-id="9ac53-118">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="9ac53-118">MAPI_E_USER_CANCEL</span></span>
  
> <span data-ttu-id="9ac53-119">WM_QUIT、られる、または WM_ENDSESSION を受信しました。</span><span class="sxs-lookup"><span data-stu-id="9ac53-119">WM_QUIT, WM_QUERYENDSESSION, or WM_ENDSESSION was received.</span></span>
    
<span data-ttu-id="9ac53-120">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="9ac53-120">MAPI_E_NOT_INITIALIZED</span></span>
  
> <span data-ttu-id="9ac53-121">MAPI は初期化されませんでした。</span><span class="sxs-lookup"><span data-stu-id="9ac53-121">MAPI was not initialized.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9ac53-122">備考</span><span class="sxs-lookup"><span data-stu-id="9ac53-122">Remarks</span></span>

<span data-ttu-id="9ac53-123">**HrDispatchNotifications**関数は、MAPI メッセージのディスパッチを待たずに、MAPI 通知エンジンにキューイングされているすべての通知をディスパッチするときに発生します。</span><span class="sxs-lookup"><span data-stu-id="9ac53-123">The **HrDispatchNotifications** function causes MAPI to dispatch all notifications that are currently queued in the MAPI notification engine without waiting for a message dispatch.</span></span> <span data-ttu-id="9ac53-124">これにより、メモリの使用率に効果をもたらさないことができます。</span><span class="sxs-lookup"><span data-stu-id="9ac53-124">This can have a beneficial effect on memory utilization.</span></span> <span data-ttu-id="9ac53-125">詳細については、[強制的に通知](forcing-a-notification.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ac53-125">For more information, see [Forcing a Notification](forcing-a-notification.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9ac53-126">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="9ac53-126">Notes to callers</span></span>

<span data-ttu-id="9ac53-127">Windows [PeekMessage](https://msdn.microsoft.com/library/ms644943.aspx)と[もないとき](https://msdn.microsoft.com/library/ms644934.aspx)の関数を使用してタイムアウト ループ内での通知メッセージの一部のアプリケーションを待ちます。</span><span class="sxs-lookup"><span data-stu-id="9ac53-127">Some applications wait for a notification message in a timeout loop using the Windows [PeekMessage](https://msdn.microsoft.com/library/ms644943.aspx) and [DispatchMessage](https://msdn.microsoft.com/library/ms644934.aspx) functions.</span></span> <span data-ttu-id="9ac53-128">最速のプラットフォームはすべて、このようなアプリケーションがありますパフォーマンスが低下または通知の偶数進行を妨げています。</span><span class="sxs-lookup"><span data-stu-id="9ac53-128">On all but the fastest platforms, such applications might experience poor performance or even blockage of notifications.</span></span> <span data-ttu-id="9ac53-129">**HrDispatchNotifications**を使用して、コードを削減するだけでなく、パフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="9ac53-129">Using **HrDispatchNotifications** not only reduces code but improves performance.</span></span> 
  

