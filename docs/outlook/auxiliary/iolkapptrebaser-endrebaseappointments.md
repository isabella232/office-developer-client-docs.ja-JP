---
title: IOlkApptRebaserEndRebaseAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e47d5a8d-6a13-f430-fbfd-00df04b4a006
description: 完了する再配置を予定するまで待機し、結果を取得します。
ms.openlocfilehash: a6e62cff9efea1fc7079d04bc9b032b5637f8847
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431002"
---
# <a name="iolkapptrebaserendrebaseappointments"></a><span data-ttu-id="b9499-103">IOlkApptRebaser::EndRebaseAppointments</span><span class="sxs-lookup"><span data-stu-id="b9499-103">IOlkApptRebaser::EndRebaseAppointments</span></span>

<span data-ttu-id="b9499-104">完了する再配置を予定するまで待機し、結果を取得します。</span><span class="sxs-lookup"><span data-stu-id="b9499-104">Waits for appointment rebasing to complete and retrieves the results.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b9499-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="b9499-105">Quick info</span></span>

<span data-ttu-id="b9499-106">[IOlkApptRebaser](iolkapptrebaser.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b9499-106">See [IOlkApptRebaser](iolkapptrebaser.md).</span></span>
  
```cpp
HRESULT EndRebaseAppointments( 
    void *pContext, 
    HRESULT *phResult);
```

## <a name="parameters"></a><span data-ttu-id="b9499-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b9499-107">Parameters</span></span>

<span data-ttu-id="b9499-108">_pContext_</span><span class="sxs-lookup"><span data-stu-id="b9499-108">_pContext_</span></span>
  
> <span data-ttu-id="b9499-p101">[in]必要があります。[IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)への呼び出しから取得されたコンテキストへのポインター。</span><span class="sxs-lookup"><span data-stu-id="b9499-p101">[in] Required. A pointer to the context obtained from a call to [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span></span>
    
<span data-ttu-id="b9499-111">_phResult_</span><span class="sxs-lookup"><span data-stu-id="b9499-111">_phResult_</span></span>
  
> <span data-ttu-id="b9499-p102">[out]必要があります。再配置の操作の結果を取得するためには、 **HRESULT** へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b9499-p102">[out] Required. A pointer to an **HRESULT** to retrieve the result of the rebasing operation.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="b9499-114">戻り値</span><span class="sxs-lookup"><span data-stu-id="b9499-114">Return values</span></span>

<span data-ttu-id="b9499-115">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="b9499-115">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b9499-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="b9499-116">See also</span></span>

- [<span data-ttu-id="b9499-117">夏時間のプログラムを使用して予定表を再配置する方法</span><span class="sxs-lookup"><span data-stu-id="b9499-117">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

