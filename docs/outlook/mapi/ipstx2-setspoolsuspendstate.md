---
title: IPSTX2SetSpoolSuspendState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX2.SetSpoolSuspendState
api_type:
- COM
ms.assetid: 396db029-1d4a-203d-2256-3353d03c6767
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: e988114e8e71ad1f80d20ab0d5a30c37425f5952
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407516"
---
# <a name="ipstx2setspoolsuspendstate"></a><span data-ttu-id="a64e1-103">IPSTX2::SetSpoolSuspendState</span><span class="sxs-lookup"><span data-stu-id="a64e1-103">IPSTX2::SetSpoolSuspendState</span></span>

  
  
<span data-ttu-id="a64e1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a64e1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a64e1-105">スプーラーの中断状態を設定します。</span><span class="sxs-lookup"><span data-stu-id="a64e1-105">Sets the suspended state on the spooler.</span></span>
  
```cpp
void SetSpoolSuspendState( 
    ULONG ulState 
);
```

## <a name="parameters"></a><span data-ttu-id="a64e1-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a64e1-106">Parameters</span></span>

 <span data-ttu-id="a64e1-107">_ulstate_</span><span class="sxs-lookup"><span data-stu-id="a64e1-107">_ulState_</span></span>
  
> <span data-ttu-id="a64e1-108">順番スプーラーをに設定する状態。</span><span class="sxs-lookup"><span data-stu-id="a64e1-108">[in] The state to set the spooler to.</span></span> <span data-ttu-id="a64e1-109">次のいずれかの値であることが必要です。</span><span class="sxs-lookup"><span data-stu-id="a64e1-109">It must be one of the following values:</span></span>
    
 <span data-ttu-id="a64e1-110">**SS_ACTIVE**</span><span class="sxs-lookup"><span data-stu-id="a64e1-110">**SS_ACTIVE**</span></span>
  
> 
    
 <span data-ttu-id="a64e1-111">**SS_SUSPENDED**</span><span class="sxs-lookup"><span data-stu-id="a64e1-111">**SS_SUSPENDED**</span></span>
  
> 
    
## <a name="see-also"></a><span data-ttu-id="a64e1-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="a64e1-112">See also</span></span>



[<span data-ttu-id="a64e1-113">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="a64e1-113">MAPI Constants</span></span>](mapi-constants.md)

