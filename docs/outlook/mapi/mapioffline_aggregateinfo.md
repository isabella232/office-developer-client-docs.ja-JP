---
title: MAPIOFFLINE_AGGREGATEINFO
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2e502d28-ae09-49d9-a35a-5d77acdcd6f4
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 4775de0707eb90549f07525e3aa54ec5842f6050
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438163"
---
# <a name="mapiofflineaggregateinfo"></a><span data-ttu-id="e34de-103">MAPIOFFLINE_AGGREGATEINFO</span><span class="sxs-lookup"><span data-stu-id="e34de-103">MAPIOFFLINE_AGGREGATEINFO</span></span>

  
  
<span data-ttu-id="e34de-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e34de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e34de-105">この構造体は、 [hrcreateofflineobj](hrcreateofflineobj.md)と共に使用されます。</span><span class="sxs-lookup"><span data-stu-id="e34de-105">The structure is used with [HrCreateOfflineObj](hrcreateofflineobj.md).</span></span> 
  
```cpp
typedef struct
{
  ULONG            ulSize;
  IUnknown*          pOuterObj;
  IUnknown*          pRefTrackRoot;
} MAPIOFFLINE_AGGREGATEINFO;
```

## <a name="members"></a><span data-ttu-id="e34de-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="e34de-106">Members</span></span>

 <span data-ttu-id="e34de-107">**ulsize**</span><span class="sxs-lookup"><span data-stu-id="e34de-107">**ulSize**</span></span>
  
> <span data-ttu-id="e34de-108">構造体のサイズ。</span><span class="sxs-lookup"><span data-stu-id="e34de-108">The size of the structure.</span></span>
    
 <span data-ttu-id="e34de-109">**pouterobj**</span><span class="sxs-lookup"><span data-stu-id="e34de-109">**pOuterObj**</span></span>
  
> <span data-ttu-id="e34de-110">このオブジェクトの集約先の IUnknown オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e34de-110">A pointer to the IUnknown object onto which this object is being aggregated.</span></span> <span data-ttu-id="e34de-111">これにより、作成されたオブジェクトに QueryInterface 呼び出しをパススルーすることができます。</span><span class="sxs-lookup"><span data-stu-id="e34de-111">This allows any QueryInterface calls to pass through to the created object.</span></span>
    
 <span data-ttu-id="e34de-112">**pRefTrackRoot**</span><span class="sxs-lookup"><span data-stu-id="e34de-112">**pRefTrackRoot**</span></span>
  
> <span data-ttu-id="e34de-113">NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="e34de-113">Must be NULL.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e34de-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="e34de-114">See also</span></span>



[<span data-ttu-id="e34de-115">HrCreateOfflineObj</span><span class="sxs-lookup"><span data-stu-id="e34de-115">HrCreateOfflineObj</span></span>](hrcreateofflineobj.md)
  
[<span data-ttu-id="e34de-116">MAPIOFFLINE_CREATEINFO</span><span class="sxs-lookup"><span data-stu-id="e34de-116">MAPIOFFLINE_CREATEINFO</span></span>](mapioffline_createinfo.md)

