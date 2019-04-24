---
title: imapiofflinegetlevel
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321274"
---
# <a name="imapiofflinegetcurrentstate"></a><span data-ttu-id="d6874-103">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="d6874-103">IMAPIOffline::GetCurrentState</span></span>

  
  
<span data-ttu-id="d6874-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6874-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6874-105">オフラインオブジェクトの現在のオンライン状態またはオフライン状態を取得します。</span><span class="sxs-lookup"><span data-stu-id="d6874-105">Gets the current online or offline state of an offline object.</span></span>
  
```cpp
HRESULT GetCurrentState( 
    ULONG* pulState 
);
```

## <a name="parameters"></a><span data-ttu-id="d6874-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d6874-106">Parameters</span></span>

 <span data-ttu-id="d6874-107">_/アウト状態_</span><span class="sxs-lookup"><span data-stu-id="d6874-107">_pulState_</span></span>
  
> <span data-ttu-id="d6874-108">読み上げオフラインオブジェクトの現在のオンライン状態またはオフライン状態。</span><span class="sxs-lookup"><span data-stu-id="d6874-108">[out] The current online or offline state of an offline object.</span></span> <span data-ttu-id="d6874-109">次の2つの値のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="d6874-109">It must be one of these two values:</span></span>
    
<span data-ttu-id="d6874-110">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="d6874-110">MAPIOFFLINE_STATE_ONLINE</span></span>
  
> 
    
<span data-ttu-id="d6874-111">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="d6874-111">MAPIOFFLINE_STATE_OFFLINE</span></span>
  
> 
    
## <a name="see-also"></a><span data-ttu-id="d6874-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="d6874-112">See also</span></span>



[<span data-ttu-id="d6874-113">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="d6874-113">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="d6874-114">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="d6874-114">IMAPIOffline::SetCurrentState</span></span>](imapioffline-setcurrentstate.md)


[<span data-ttu-id="d6874-115">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="d6874-115">MAPI Constants</span></span>](mapi-constants.md)

