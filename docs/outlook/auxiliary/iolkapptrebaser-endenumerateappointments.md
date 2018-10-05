---
title: IOlkApptRebaserEndEnumerateAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bc4506c7-7a4f-940d-d0a6-e0fab4561a88
description: 予定の列挙を完了するには、予定表フォルダーでの待機し、その必要性を再配置する予定のリストを返します。
ms.openlocfilehash: 5be6fd9ce33374725b36429cd0fbc717776c9ab9
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392019"
---
# <a name="iolkapptrebaserendenumerateappointments"></a><span data-ttu-id="a5cc0-103">IOlkApptRebaser::EndEnumerateAppointments</span><span class="sxs-lookup"><span data-stu-id="a5cc0-103">IOlkApptRebaser::EndEnumerateAppointments</span></span>

<span data-ttu-id="a5cc0-104">予定の列挙を完了するには、予定表フォルダーでの待機し、その必要性を再配置する予定のリストを返します。</span><span class="sxs-lookup"><span data-stu-id="a5cc0-104">Waits for appointment enumeration in a calendar folder to complete and returns a list of appointments that need rebasing.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a5cc0-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="a5cc0-105">Quick info</span></span>

<span data-ttu-id="a5cc0-106">[IOlkApptRebaser](iolkapptrebaser.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a5cc0-106">See [IOlkApptRebaser](iolkapptrebaser.md).</span></span>
  
```cpp
HRESULT EndEnumerateAppointments( 
    void *pContext, 
    HRESULT *phResult, 
    MAPIERROR **ppError, 
    SRowSet **ppRows);
```

## <a name="parameters"></a><span data-ttu-id="a5cc0-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a5cc0-107">Parameters</span></span>

<span data-ttu-id="a5cc0-108">_pContext_</span><span class="sxs-lookup"><span data-stu-id="a5cc0-108">_pContext_</span></span>
  
> <span data-ttu-id="a5cc0-p101">[in]必要があります。[IOlkApptRebaser::BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)の前回の呼び出しから取得されたコンテキストへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a5cc0-p101">[in] Required. A pointer to the context obtained from a prior call to [IOlkApptRebaser::BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md).</span></span>
    
<span data-ttu-id="a5cc0-111">_phResult_</span><span class="sxs-lookup"><span data-stu-id="a5cc0-111">_phResult_</span></span>
  
> <span data-ttu-id="a5cc0-p102">[out]必要があります。列挙操作の結果を取得するためには、 **HRESULT** へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a5cc0-p102">[out] Required. A pointer to an **HRESULT** to retrieve the results of the enumeration operation.</span></span> 
    
<span data-ttu-id="a5cc0-114">_ppError_</span><span class="sxs-lookup"><span data-stu-id="a5cc0-114">_ppError_</span></span>
  
> <span data-ttu-id="a5cc0-p103">[out]省略可能です。拡張エラー情報を取得する **MAPIERROR** 構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a5cc0-p103">[out] Optional. A pointer to a pointer to a **MAPIERROR** structure to retrieve extended error information.</span></span> 
    
<span data-ttu-id="a5cc0-117">_ppRows_</span><span class="sxs-lookup"><span data-stu-id="a5cc0-117">_ppRows_</span></span>
  
> <span data-ttu-id="a5cc0-p104">[out]必要があります。再配置する必要がある予定を記述する[SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)構造体へのポインターへのポインター。通常、この構造体は[IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)に渡されます。</span><span class="sxs-lookup"><span data-stu-id="a5cc0-p104">[out] Required. A pointer to a pointer to an [SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx) structure that describes the appointments that need rebasing. This structure will usually be passed to [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span></span>
    
## <a name="return-values"></a><span data-ttu-id="a5cc0-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="a5cc0-121">Return values</span></span>

<span data-ttu-id="a5cc0-122">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="a5cc0-122">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a5cc0-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="a5cc0-123">See also</span></span>

- [<span data-ttu-id="a5cc0-124">夏時間のプログラムを使用して予定表を再配置する方法</span><span class="sxs-lookup"><span data-stu-id="a5cc0-124">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

