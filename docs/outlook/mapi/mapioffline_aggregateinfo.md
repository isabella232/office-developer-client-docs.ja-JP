---
title: MAPIOFFLINE_AGGREGATEINFO
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2e502d28-ae09-49d9-a35a-5d77acdcd6f4
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 24e16aeb1bbee1c35cf8fbd5813fb3e83b762187
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801504"
---
# <a name="mapiofflineaggregateinfo"></a><span data-ttu-id="19f22-103">MAPIOFFLINE_AGGREGATEINFO</span><span class="sxs-lookup"><span data-stu-id="19f22-103">MAPIOFFLINE_AGGREGATEINFO</span></span>

  
  
<span data-ttu-id="19f22-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="19f22-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="19f22-105">[HrCreateOfflineObj](hrcreateofflineobj.md)構造体が使用されます。</span><span class="sxs-lookup"><span data-stu-id="19f22-105">The structure is used with [HrCreateOfflineObj](hrcreateofflineobj.md).</span></span> 
  
```cpp
typedef struct
{
  ULONG            ulSize;
  IUnknown*          pOuterObj;
  IUnknown*          pRefTrackRoot;
} MAPIOFFLINE_AGGREGATEINFO;
```

## <a name="members"></a><span data-ttu-id="19f22-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="19f22-106">Members</span></span>

 <span data-ttu-id="19f22-107">**ulSize**</span><span class="sxs-lookup"><span data-stu-id="19f22-107">**ulSize**</span></span>
  
> <span data-ttu-id="19f22-108">構造体のサイズです。</span><span class="sxs-lookup"><span data-stu-id="19f22-108">The size of the structure.</span></span>
    
 <span data-ttu-id="19f22-109">**pOuterObj**</span><span class="sxs-lookup"><span data-stu-id="19f22-109">**pOuterObj**</span></span>
  
> <span data-ttu-id="19f22-110">先この集約オブジェクトの IUnknown オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="19f22-110">A pointer to the IUnknown object onto which this object is being aggregated.</span></span> <span data-ttu-id="19f22-111">こうと、作成したオブジェクトを通過するすべての QueryInterface 呼び出しができます。</span><span class="sxs-lookup"><span data-stu-id="19f22-111">This allows any QueryInterface calls to pass through to the created object.</span></span>
    
 <span data-ttu-id="19f22-112">**pRefTrackRoot**</span><span class="sxs-lookup"><span data-stu-id="19f22-112">**pRefTrackRoot**</span></span>
  
> <span data-ttu-id="19f22-113">NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="19f22-113">Must be NULL.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="19f22-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="19f22-114">See also</span></span>



[<span data-ttu-id="19f22-115">HrCreateOfflineObj</span><span class="sxs-lookup"><span data-stu-id="19f22-115">HrCreateOfflineObj</span></span>](hrcreateofflineobj.md)
  
[<span data-ttu-id="19f22-116">MAPIOFFLINE_CREATEINFO</span><span class="sxs-lookup"><span data-stu-id="19f22-116">MAPIOFFLINE_CREATEINFO</span></span>](mapioffline_createinfo.md)

