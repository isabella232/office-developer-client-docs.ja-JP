---
title: IOlkApptRebaserBeginRebaseAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed50422e-9edf-4b73-1789-340b70532621
description: 予定を再配置する通常IOlkApptRebaser::EndEnumerateAppointmentsから取得予定の一覧を指定するためのタスクを開始します。
ms.openlocfilehash: 2becb305eebe448e2adecf91c2a111f86d97fe50
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799504"
---
# <a name="iolkapptrebaserbeginrebaseappointments"></a><span data-ttu-id="179c3-103">IOlkApptRebaser::BeginRebaseAppointments</span><span class="sxs-lookup"><span data-stu-id="179c3-103">IOlkApptRebaser::BeginRebaseAppointments</span></span>

<span data-ttu-id="179c3-104">予定を再配置する通常[IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)から取得予定の一覧を指定するためのタスクを開始します。</span><span class="sxs-lookup"><span data-stu-id="179c3-104">Begins a task for appointment rebasing given a list of appointments, usually obtained from [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="179c3-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="179c3-105">Quick info</span></span>

<span data-ttu-id="179c3-106">[IOlkApptRebaser](iolkapptrebaser.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="179c3-106">See [IOlkApptRebaser](iolkapptrebaser.md).</span></span>
  
```cpp
HRESULT BeginRebaseAppointments( 
    const SRowSet *pRows, 
    PFNREBASETASKPROGRESS pfnProgress, 
    PFNREBASETASKCOMPLETE pfnComplete, 
    void **ppContext);
```

## <a name="parameters"></a><span data-ttu-id="179c3-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="179c3-107">Parameters</span></span>

<span data-ttu-id="179c3-108">_pRows_</span><span class="sxs-lookup"><span data-stu-id="179c3-108">_pRows_</span></span>
  
> <span data-ttu-id="179c3-p101">[in]必要があります。再配置する必要がある予定を記述する[SRowSet](http://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)構造体へのポインター。通常、この構造体は[IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)の前回の呼び出しから取得されます。</span><span class="sxs-lookup"><span data-stu-id="179c3-p101">[in] Required. A pointer to an [SRowSet](http://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx) structure that describes the appointments that need rebasing. This structure is usually obtained from a prior call to [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span></span>
    
<span data-ttu-id="179c3-112">_pfnProgress_</span><span class="sxs-lookup"><span data-stu-id="179c3-112">_pfnProgress_</span></span>
  
> <span data-ttu-id="179c3-p102">[in]省略可能です。進行状況が表示されることを再作業の進行状況関数へのポインター。 **PFNREBASETASKPROGRESS** は、tzmovelib.h で定義されます。</span><span class="sxs-lookup"><span data-stu-id="179c3-p102">[in] Optional. A pointer to a rebase task progress function to receive progress. **PFNREBASETASKPROGRESS** is defined in tzmovelib.h.</span></span> 
    
<span data-ttu-id="179c3-116">_pfnComplete_</span><span class="sxs-lookup"><span data-stu-id="179c3-116">_pfnComplete_</span></span>
  
> <span data-ttu-id="179c3-p103">[out]省略可能です。再配置の完了の通知を受信するには、再作業完了関数へのポインター。 **PFNREBASETASKCOMPLETE** は、tzmovelib.h で定義されます。</span><span class="sxs-lookup"><span data-stu-id="179c3-p103">[out] Optional. A pointer to a rebase task completion function to receive notification of rebase completion. **PFNREBASETASKCOMPLETE** is defined in tzmovelib.h.</span></span> 
    
<span data-ttu-id="179c3-120">_ppContext_</span><span class="sxs-lookup"><span data-stu-id="179c3-120">_ppContext_</span></span>
  
> <span data-ttu-id="179c3-p104">[out]必要があります。返されるコンテキストへのポインターへのポインター。このコンテキストは、通常[IOlkApptRebaser::EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)に渡されます。</span><span class="sxs-lookup"><span data-stu-id="179c3-p104">[out] Required. A pointer to a pointer to the returned context. This context will usually be passed to [IOlkApptRebaser::EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md).</span></span>
    
## <a name="return-values"></a><span data-ttu-id="179c3-124">戻り値</span><span class="sxs-lookup"><span data-stu-id="179c3-124">Return values</span></span>

<span data-ttu-id="179c3-125">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="179c3-125">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="179c3-126">解釈</span><span class="sxs-lookup"><span data-stu-id="179c3-126">Remarks</span></span>

<span data-ttu-id="179c3-127">このタスクは、新しいスレッドで実行されます。</span><span class="sxs-lookup"><span data-stu-id="179c3-127">This task runs on a new thread.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="179c3-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="179c3-128">See also</span></span>

- [<span data-ttu-id="179c3-129">夏時間のプログラムを使用して予定表を再配置する方法</span><span class="sxs-lookup"><span data-stu-id="179c3-129">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

