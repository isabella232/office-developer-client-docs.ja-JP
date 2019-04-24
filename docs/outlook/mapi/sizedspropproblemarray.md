---
title: SizedSPropProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSPropProblemArray
api_type:
- COM
ms.assetid: 2fc3febb-8c69-4315-a112-a28eee98013d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b3818e5e1429c7e2b7d5f7533db733ba29e672c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282692"
---
# <a name="sizedspropproblemarray"></a><span data-ttu-id="df2e8-103">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="df2e8-103">SizedSPropProblemArray</span></span>

<span data-ttu-id="df2e8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df2e8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df2e8-105">指定した数の[sprop問題](spropproblem.md)構造体を含む名前付き[sprop問題の配列](spropproblemarray.md)構造を作成します。</span><span class="sxs-lookup"><span data-stu-id="df2e8-105">Creates a named [SPropProblemArray](spropproblemarray.md) structure that contains a specified number of [SPropProblem](spropproblem.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="df2e8-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="df2e8-106">Header file:</span></span>  <br/> |<span data-ttu-id="df2e8-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="df2e8-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="df2e8-108">関連する構造:</span><span class="sxs-lookup"><span data-stu-id="df2e8-108">Related structure:</span></span>  <br/> |<span data-ttu-id="df2e8-109">**SPropProblemArray**</span><span class="sxs-lookup"><span data-stu-id="df2e8-109">**SPropProblemArray**</span></span> <br/> |
   
```cpp
SizedSPropProblemArray(_cprob, _name)
```

## <a name="parameters"></a><span data-ttu-id="df2e8-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="df2e8-110">Parameters</span></span>

<span data-ttu-id="df2e8-111">__cprob_</span><span class="sxs-lookup"><span data-stu-id="df2e8-111">__cprob_</span></span>
  
> <span data-ttu-id="df2e8-112">新しい構造に含めることができる**spropproblem**構造の数。</span><span class="sxs-lookup"><span data-stu-id="df2e8-112">Count of **SPropProblem** structures to be included in the new structure.</span></span> 
    
<span data-ttu-id="df2e8-113">__名前_</span><span class="sxs-lookup"><span data-stu-id="df2e8-113">__name_</span></span>
  
> <span data-ttu-id="df2e8-114">新しい構造の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="df2e8-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="df2e8-115">解説</span><span class="sxs-lookup"><span data-stu-id="df2e8-115">Remarks</span></span>

<span data-ttu-id="df2e8-116">**sizedsprop問題の配列**マクロを使用して、明示的な境界を持つプロパティ問題の配列を作成します。</span><span class="sxs-lookup"><span data-stu-id="df2e8-116">Use the **SizedSPropProblemArray** macro to create a property problem array with explicit bounds.</span></span> <span data-ttu-id="df2e8-117">**sizedspropの配列**マクロの結果として得られる新しい構造を、 **spropの配列**構造体へのポインターとして使用するには、次のキャストを実行します。</span><span class="sxs-lookup"><span data-stu-id="df2e8-117">To use the new structure that results from the **SizedSPropProblemArray** macro as a pointer to an **SPropProblemArray** structure, perform the following cast:</span></span> 
  
```cpp
lpPropProbArray = (LPSPropProblemArray) &SizedSPropProblemArray;
```

## <a name="see-also"></a><span data-ttu-id="df2e8-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="df2e8-118">See also</span></span>

- [<span data-ttu-id="df2e8-119">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="df2e8-119">SPropProblemArray</span></span>](spropproblemarray.md)
- [<span data-ttu-id="df2e8-120">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="df2e8-120">SPropProblem</span></span>](spropproblem.md)
- [<span data-ttu-id="df2e8-121">構造に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="df2e8-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

