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
ms.openlocfilehash: bbced8412c2c3438c58af74ef072a46606b59ddc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594615"
---
# <a name="sizedspropproblemarray"></a><span data-ttu-id="da274-103">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="da274-103">SizedSPropProblemArray</span></span>

<span data-ttu-id="da274-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="da274-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="da274-105">[SPropProblem](spropproblem.md)構造体の指定した数値を含む名前付き[SPropProblemArray](spropproblemarray.md)構造体を作成します。</span><span class="sxs-lookup"><span data-stu-id="da274-105">Creates a named [SPropProblemArray](spropproblemarray.md) structure that contains a specified number of [SPropProblem](spropproblem.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="da274-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="da274-106">Header file:</span></span>  <br/> |<span data-ttu-id="da274-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="da274-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="da274-108">関連の構造体。</span><span class="sxs-lookup"><span data-stu-id="da274-108">Related structure:</span></span>  <br/> |<span data-ttu-id="da274-109">**SPropProblemArray**</span><span class="sxs-lookup"><span data-stu-id="da274-109">**SPropProblemArray**</span></span> <br/> |
   
```cpp
SizedSPropProblemArray(_cprob, _name)
```

## <a name="parameters"></a><span data-ttu-id="da274-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="da274-110">Parameters</span></span>

<span data-ttu-id="da274-111">__cprob_</span><span class="sxs-lookup"><span data-stu-id="da274-111">__cprob_</span></span>
  
> <span data-ttu-id="da274-112">新しい構造体に含まれる**SPropProblem**構造体の数です。</span><span class="sxs-lookup"><span data-stu-id="da274-112">Count of **SPropProblem** structures to be included in the new structure.</span></span> 
    
<span data-ttu-id="da274-113">__名_</span><span class="sxs-lookup"><span data-stu-id="da274-113">__name_</span></span>
  
> <span data-ttu-id="da274-114">新しい構造体の名前です。</span><span class="sxs-lookup"><span data-stu-id="da274-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="da274-115">注釈</span><span class="sxs-lookup"><span data-stu-id="da274-115">Remarks</span></span>

<span data-ttu-id="da274-116">**SizedSPropProblemArray**マクロを使用すると、明示的な境界を持つプロパティの問題の配列を作成します。</span><span class="sxs-lookup"><span data-stu-id="da274-116">Use the **SizedSPropProblemArray** macro to create a property problem array with explicit bounds.</span></span> <span data-ttu-id="da274-117">**SPropProblemArray**構造体へのポインターとしての**SizedSPropProblemArray**マクロの結果を新しい構造体を使用するには、次のキャストを実行します。</span><span class="sxs-lookup"><span data-stu-id="da274-117">To use the new structure that results from the **SizedSPropProblemArray** macro as a pointer to an **SPropProblemArray** structure, perform the following cast:</span></span> 
  
```cpp
lpPropProbArray = (LPSPropProblemArray) &SizedSPropProblemArray;
```

## <a name="see-also"></a><span data-ttu-id="da274-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="da274-118">See also</span></span>

- [<span data-ttu-id="da274-119">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="da274-119">SPropProblemArray</span></span>](spropproblemarray.md)
- [<span data-ttu-id="da274-120">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="da274-120">SPropProblem</span></span>](spropproblem.md)
- [<span data-ttu-id="da274-121">構造体に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="da274-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

