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
ms.openlocfilehash: 60c5d7e980d1dc4d4263a2be2267008dbee1fd4d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594699"
---
# <a name="hrdispatchnotifications"></a><span data-ttu-id="89eaa-103">HrDispatchNotifications</span><span class="sxs-lookup"><span data-stu-id="89eaa-103">HrDispatchNotifications</span></span>

  
  
<span data-ttu-id="89eaa-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="89eaa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="89eaa-105">フォースは、キューに登録されたすべての通知のディスパッチします。</span><span class="sxs-lookup"><span data-stu-id="89eaa-105">Forces dispatching of all queued notifications.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="89eaa-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="89eaa-106">Header file:</span></span>  <br/> |<span data-ttu-id="89eaa-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="89eaa-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="89eaa-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="89eaa-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="89eaa-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="89eaa-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="89eaa-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="89eaa-110">Called by:</span></span>  <br/> |<span data-ttu-id="89eaa-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="89eaa-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrDispatchNotifications(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="89eaa-112">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="89eaa-112">Parameters</span></span>

 <span data-ttu-id="89eaa-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="89eaa-113">_ulFlags_</span></span>
  
> <span data-ttu-id="89eaa-114">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="89eaa-114">[in] Reserved; must be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="89eaa-115">�߂�l</span><span class="sxs-lookup"><span data-stu-id="89eaa-115">Return value</span></span>

<span data-ttu-id="89eaa-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="89eaa-116">S_OK</span></span>
  
> <span data-ttu-id="89eaa-117">すべてのキューに登録された通知がディスパッチされました。</span><span class="sxs-lookup"><span data-stu-id="89eaa-117">All queued notifications have been dispatched.</span></span>
    
<span data-ttu-id="89eaa-118">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="89eaa-118">MAPI_E_USER_CANCEL</span></span>
  
> <span data-ttu-id="89eaa-119">WM_QUIT、られる、または WM_ENDSESSION を受信しました。</span><span class="sxs-lookup"><span data-stu-id="89eaa-119">WM_QUIT, WM_QUERYENDSESSION, or WM_ENDSESSION was received.</span></span>
    
<span data-ttu-id="89eaa-120">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="89eaa-120">MAPI_E_NOT_INITIALIZED</span></span>
  
> <span data-ttu-id="89eaa-121">MAPI は初期化されませんでした。</span><span class="sxs-lookup"><span data-stu-id="89eaa-121">MAPI was not initialized.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="89eaa-122">注釈</span><span class="sxs-lookup"><span data-stu-id="89eaa-122">Remarks</span></span>

<span data-ttu-id="89eaa-123">**HrDispatchNotifications**関数は、MAPI メッセージのディスパッチを待たずに、MAPI 通知エンジンにキューイングされているすべての通知をディスパッチするときに発生します。</span><span class="sxs-lookup"><span data-stu-id="89eaa-123">The **HrDispatchNotifications** function causes MAPI to dispatch all notifications that are currently queued in the MAPI notification engine without waiting for a message dispatch.</span></span> <span data-ttu-id="89eaa-124">これにより、メモリの使用率に効果をもたらさないことができます。</span><span class="sxs-lookup"><span data-stu-id="89eaa-124">This can have a beneficial effect on memory utilization.</span></span> <span data-ttu-id="89eaa-125">詳細については、[強制的に通知](forcing-a-notification.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="89eaa-125">For more information, see [Forcing a Notification](forcing-a-notification.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="89eaa-126">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="89eaa-126">Notes to callers</span></span>

<span data-ttu-id="89eaa-127">Windows [PeekMessage](http://msdn.microsoft.com/en-us/library/ms644943.aspx)と[もないとき](http://msdn.microsoft.com/en-us/library/ms644934.aspx)の関数を使用してタイムアウト ループ内での通知メッセージの一部のアプリケーションを待ちます。</span><span class="sxs-lookup"><span data-stu-id="89eaa-127">Some applications wait for a notification message in a timeout loop using the Windows [PeekMessage](http://msdn.microsoft.com/en-us/library/ms644943.aspx) and [DispatchMessage](http://msdn.microsoft.com/en-us/library/ms644934.aspx) functions.</span></span> <span data-ttu-id="89eaa-128">最速のプラットフォームはすべて、このようなアプリケーションがありますパフォーマンスが低下または通知の偶数進行を妨げています。</span><span class="sxs-lookup"><span data-stu-id="89eaa-128">On all but the fastest platforms, such applications might experience poor performance or even blockage of notifications.</span></span> <span data-ttu-id="89eaa-129">**HrDispatchNotifications**を使用して、コードを削減するだけでなく、パフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="89eaa-129">Using **HrDispatchNotifications** not only reduces code but improves performance.</span></span> 
  

