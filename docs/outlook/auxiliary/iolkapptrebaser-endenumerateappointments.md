---
title: IOlkApptRebaserEndEnumerateAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bc4506c7-7a4f-940d-d0a6-e0fab4561a88
description: 予定の列挙を完了するには、予定表フォルダーでの待機し、その必要性を再配置する予定のリストを返します。
ms.openlocfilehash: d7d29a88114d7b3973b8f04e924dc1dd8489a097
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799502"
---
# <a name="iolkapptrebaserendenumerateappointments"></a><span data-ttu-id="6787f-103">IOlkApptRebaser::EndEnumerateAppointments</span><span class="sxs-lookup"><span data-stu-id="6787f-103">IOlkApptRebaser::EndEnumerateAppointments</span></span>

<span data-ttu-id="6787f-104">予定の列挙を完了するには、予定表フォルダーでの待機し、その必要性を再配置する予定のリストを返します。</span><span class="sxs-lookup"><span data-stu-id="6787f-104">Waits for appointment enumeration in a calendar folder to complete and returns a list of appointments that need rebasing.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="6787f-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="6787f-105">Quick info</span></span>

<span data-ttu-id="6787f-106">[IOlkApptRebaser](iolkapptrebaser.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6787f-106">See [IOlkApptRebaser](iolkapptrebaser.md).</span></span>
  
```cpp
HRESULT EndEnumerateAppointments( 
    void *pContext, 
    HRESULT *phResult, 
    MAPIERROR **ppError, 
    SRowSet **ppRows);
```

## <a name="parameters"></a><span data-ttu-id="6787f-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6787f-107">Parameters</span></span>

<span data-ttu-id="6787f-108">_pContext_</span><span class="sxs-lookup"><span data-stu-id="6787f-108">_pContext_</span></span>
  
> <span data-ttu-id="6787f-p101">[in]必要があります。[IOlkApptRebaser::BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)の前回の呼び出しから取得されたコンテキストへのポインター。</span><span class="sxs-lookup"><span data-stu-id="6787f-p101">[in] Required. A pointer to the context obtained from a prior call to [IOlkApptRebaser::BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md).</span></span>
    
<span data-ttu-id="6787f-111">_phResult_</span><span class="sxs-lookup"><span data-stu-id="6787f-111">_phResult_</span></span>
  
> <span data-ttu-id="6787f-p102">[out]必要があります。列挙操作の結果を取得するためには、 **HRESULT** へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6787f-p102">[out] Required. A pointer to an **HRESULT** to retrieve the results of the enumeration operation.</span></span> 
    
<span data-ttu-id="6787f-114">_ppError_</span><span class="sxs-lookup"><span data-stu-id="6787f-114">_ppError_</span></span>
  
> <span data-ttu-id="6787f-p103">[out]省略可能です。拡張エラー情報を取得する **MAPIERROR** 構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="6787f-p103">[out] Optional. A pointer to a pointer to a **MAPIERROR** structure to retrieve extended error information.</span></span> 
    
<span data-ttu-id="6787f-117">_ppRows_</span><span class="sxs-lookup"><span data-stu-id="6787f-117">_ppRows_</span></span>
  
> <span data-ttu-id="6787f-p104">[out]必要があります。再配置する必要がある予定を記述する[SRowSet](http://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)構造体へのポインターへのポインター。通常、この構造体は[IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)に渡されます。</span><span class="sxs-lookup"><span data-stu-id="6787f-p104">[out] Required. A pointer to a pointer to an [SRowSet](http://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx) structure that describes the appointments that need rebasing. This structure will usually be passed to [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span></span>
    
## <a name="return-values"></a><span data-ttu-id="6787f-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="6787f-121">Return values</span></span>

<span data-ttu-id="6787f-122">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="6787f-122">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6787f-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="6787f-123">See also</span></span>

- [<span data-ttu-id="6787f-124">夏時間のプログラムを使用して予定表を再配置する方法</span><span class="sxs-lookup"><span data-stu-id="6787f-124">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

