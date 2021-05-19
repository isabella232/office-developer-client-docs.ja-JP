---
title: IMAPIOfflineGetCurrentState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline.GetCurrentState
api_type:
- COM
ms.assetid: f3769e83-d678-1087-fc0f-b4f156386333
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: f5170ceb443dcde075440bf84d29000afe4680c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419871"
---
# <a name="imapiofflinegetcurrentstate"></a><span data-ttu-id="1426b-103">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="1426b-103">IMAPIOffline::GetCurrentState</span></span>

  
  
<span data-ttu-id="1426b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1426b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1426b-105">オフライン オブジェクトの現在のオンライン状態またはオフライン状態を取得します。</span><span class="sxs-lookup"><span data-stu-id="1426b-105">Gets the current online or offline state of an offline object.</span></span>
  
```cpp
HRESULT GetCurrentState( 
    ULONG* pulState 
);
```

## <a name="parameters"></a><span data-ttu-id="1426b-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1426b-106">Parameters</span></span>

 <span data-ttu-id="1426b-107">_pulState_</span><span class="sxs-lookup"><span data-stu-id="1426b-107">_pulState_</span></span>
  
> <span data-ttu-id="1426b-108">[out]オフライン オブジェクトの現在のオンライン状態またはオフライン状態。</span><span class="sxs-lookup"><span data-stu-id="1426b-108">[out] The current online or offline state of an offline object.</span></span> <span data-ttu-id="1426b-109">この値は、次の 2 つの値の 1 つである必要があります。</span><span class="sxs-lookup"><span data-stu-id="1426b-109">It must be one of these two values:</span></span>
    
<span data-ttu-id="1426b-110">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="1426b-110">MAPIOFFLINE_STATE_ONLINE</span></span>
  
> 
    
<span data-ttu-id="1426b-111">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="1426b-111">MAPIOFFLINE_STATE_OFFLINE</span></span>
  
> 
    
## <a name="see-also"></a><span data-ttu-id="1426b-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="1426b-112">See also</span></span>



[<span data-ttu-id="1426b-113">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="1426b-113">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="1426b-114">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="1426b-114">IMAPIOffline::SetCurrentState</span></span>](imapioffline-setcurrentstate.md)


[<span data-ttu-id="1426b-115">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="1426b-115">MAPI Constants</span></span>](mapi-constants.md)

