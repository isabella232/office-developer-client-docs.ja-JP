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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 30ec82788e46ca07c6529ce74872e0a0c7c012a1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801181"
---
# <a name="ipstx2setspoolsuspendstate"></a><span data-ttu-id="3743a-103">IPSTX2::SetSpoolSuspendState</span><span class="sxs-lookup"><span data-stu-id="3743a-103">IPSTX2::SetSpoolSuspendState</span></span>

  
  
<span data-ttu-id="3743a-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3743a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3743a-105">スプーラーを一時停止の状態を設定します。</span><span class="sxs-lookup"><span data-stu-id="3743a-105">Sets the suspended state on the spooler.</span></span>
  
```cpp
void SetSpoolSuspendState( 
    ULONG ulState 
);
```

## <a name="parameters"></a><span data-ttu-id="3743a-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3743a-106">Parameters</span></span>

 <span data-ttu-id="3743a-107">_ulState_</span><span class="sxs-lookup"><span data-stu-id="3743a-107">_ulState_</span></span>
  
> <span data-ttu-id="3743a-108">[in]スプーラーに設定する状態です。</span><span class="sxs-lookup"><span data-stu-id="3743a-108">[in] The state to set the spooler to.</span></span> <span data-ttu-id="3743a-109">次の値のいずれかを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3743a-109">It must be one of the following values:</span></span>
    
 <span data-ttu-id="3743a-110">**SS_ACTIVE**</span><span class="sxs-lookup"><span data-stu-id="3743a-110">**SS_ACTIVE**</span></span>
  
> 
    
 <span data-ttu-id="3743a-111">**SS_SUSPENDED**</span><span class="sxs-lookup"><span data-stu-id="3743a-111">**SS_SUSPENDED**</span></span>
  
> 
    
## <a name="see-also"></a><span data-ttu-id="3743a-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="3743a-112">See also</span></span>



[<span data-ttu-id="3743a-113">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="3743a-113">MAPI Constants</span></span>](mapi-constants.md)

