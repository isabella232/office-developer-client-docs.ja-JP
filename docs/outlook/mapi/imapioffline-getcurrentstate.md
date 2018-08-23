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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 5d6b1dfcd3866b0d0e7151e9d5399e1274810d14
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568204"
---
# <a name="imapiofflinegetcurrentstate"></a><span data-ttu-id="d83c8-103">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="d83c8-103">IMAPIOffline::GetCurrentState</span></span>

  
  
<span data-ttu-id="d83c8-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d83c8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d83c8-105">オフライン オブジェクトの現在のオンラインまたはオフラインの状態を取得します。</span><span class="sxs-lookup"><span data-stu-id="d83c8-105">Gets the current online or offline state of an offline object.</span></span>
  
```cpp
HRESULT GetCurrentState( 
    ULONG* pulState 
);
```

## <a name="parameters"></a><span data-ttu-id="d83c8-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d83c8-106">Parameters</span></span>

 <span data-ttu-id="d83c8-107">_pulState_</span><span class="sxs-lookup"><span data-stu-id="d83c8-107">_pulState_</span></span>
  
> <span data-ttu-id="d83c8-108">[out]オンラインまたはオフラインの現在の状態がオフラインのオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="d83c8-108">[out] The current online or offline state of an offline object.</span></span> <span data-ttu-id="d83c8-109">これら 2 つの値のいずれかを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d83c8-109">It must be one of these two values:</span></span>
    
<span data-ttu-id="d83c8-110">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="d83c8-110">MAPIOFFLINE_STATE_ONLINE</span></span>
  
> 
    
<span data-ttu-id="d83c8-111">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="d83c8-111">MAPIOFFLINE_STATE_OFFLINE</span></span>
  
> 
    
## <a name="see-also"></a><span data-ttu-id="d83c8-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="d83c8-112">See also</span></span>



[<span data-ttu-id="d83c8-113">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="d83c8-113">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="d83c8-114">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="d83c8-114">IMAPIOffline::SetCurrentState</span></span>](imapioffline-setcurrentstate.md)


[<span data-ttu-id="d83c8-115">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="d83c8-115">MAPI Constants</span></span>](mapi-constants.md)

