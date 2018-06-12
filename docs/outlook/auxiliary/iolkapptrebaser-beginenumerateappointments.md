---
title: IOlkApptRebaserBeginEnumerateAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8946703a-aaa8-6b3f-aa68-931365db620d
description: タスクを再配置する必要がある予定を検索するには、予定表フォルダーの予定の列挙を開始します。
ms.openlocfilehash: 2ad26692483d87166a538ec2f04d3fc13b9ea930
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799485"
---
# <a name="iolkapptrebaserbeginenumerateappointments"></a><span data-ttu-id="d29af-103">IOlkApptRebaser::BeginEnumerateAppointments</span><span class="sxs-lookup"><span data-stu-id="d29af-103">IOlkApptRebaser::BeginEnumerateAppointments</span></span>

<span data-ttu-id="d29af-104">タスクを再配置する必要がある予定を検索するには、予定表フォルダーの予定の列挙を開始します。</span><span class="sxs-lookup"><span data-stu-id="d29af-104">Begins a task for appointment enumeration in a calendar folder to find the appointments that need rebasing.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d29af-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="d29af-105">Quick info</span></span>

<span data-ttu-id="d29af-106">[IOlkApptRebaser](iolkapptrebaser.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d29af-106">See [IOlkApptRebaser](iolkapptrebaser.md).</span></span>
  
```cpp
HRESULT BeginEnumerateAppointments( 
    PFNREBASETASKPROGRESS pfnProgress, 
    void **ppContext);
```

## <a name="parameters"></a><span data-ttu-id="d29af-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d29af-107">Parameters</span></span>

<span data-ttu-id="d29af-108">_pfnProgress_</span><span class="sxs-lookup"><span data-stu-id="d29af-108">_pfnProgress_</span></span>
  
> <span data-ttu-id="d29af-p101">[in]省略可能です。進行状況が表示されることを再作業の進行状況関数へのポインター。 **PFNREBASETASKPROGRESS** は、tzmovelib.h で定義されます。</span><span class="sxs-lookup"><span data-stu-id="d29af-p101">[in] Optional. A pointer to a rebase task progress function to receive progress. **PFNREBASETASKPROGRESS** is defined in tzmovelib.h.</span></span> 
    
<span data-ttu-id="d29af-112">_ppContext_</span><span class="sxs-lookup"><span data-stu-id="d29af-112">_ppContext_</span></span>
  
> <span data-ttu-id="d29af-p102">[out]必要があります。返されるコンテキストへのポインターへのポインター。このコンテキストは、 [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)に渡されます。</span><span class="sxs-lookup"><span data-stu-id="d29af-p102">[out] Required. A pointer to a pointer to the returned context. This context will be passed to [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span></span>
    
## <a name="return-values"></a><span data-ttu-id="d29af-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="d29af-116">Return values</span></span>

<span data-ttu-id="d29af-117">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="d29af-117">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d29af-118">解釈</span><span class="sxs-lookup"><span data-stu-id="d29af-118">Remarks</span></span>

<span data-ttu-id="d29af-119">このタスクは、新しいスレッドで実行されます。</span><span class="sxs-lookup"><span data-stu-id="d29af-119">This task runs on a new thread.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d29af-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="d29af-120">See also</span></span>

- [<span data-ttu-id="d29af-121">夏時間のプログラムを使用して予定表を再配置する方法</span><span class="sxs-lookup"><span data-stu-id="d29af-121">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

