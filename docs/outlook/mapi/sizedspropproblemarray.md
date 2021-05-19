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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b3818e5e1429c7e2b7d5f7533db733ba29e672c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418114"
---
# <a name="sizedspropproblemarray"></a><span data-ttu-id="60a15-103">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="60a15-103">SizedSPropProblemArray</span></span>

<span data-ttu-id="60a15-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="60a15-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="60a15-105">指定した [数の SPropProblem](spropproblemarray.md) 構造体を含む名前付き [SPropProblemArray 構造体を作成](spropproblem.md) します。</span><span class="sxs-lookup"><span data-stu-id="60a15-105">Creates a named [SPropProblemArray](spropproblemarray.md) structure that contains a specified number of [SPropProblem](spropproblem.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="60a15-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="60a15-106">Header file:</span></span>  <br/> |<span data-ttu-id="60a15-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="60a15-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="60a15-108">関連する構造:</span><span class="sxs-lookup"><span data-stu-id="60a15-108">Related structure:</span></span>  <br/> |<span data-ttu-id="60a15-109">**SPropProblemArray**</span><span class="sxs-lookup"><span data-stu-id="60a15-109">**SPropProblemArray**</span></span> <br/> |
   
```cpp
SizedSPropProblemArray(_cprob, _name)
```

## <a name="parameters"></a><span data-ttu-id="60a15-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="60a15-110">Parameters</span></span>

<span data-ttu-id="60a15-111">_ _cprob_</span><span class="sxs-lookup"><span data-stu-id="60a15-111">_ _cprob_</span></span>
  
> <span data-ttu-id="60a15-112">新しい **構造に含める SPropProblem** 構造体の数。</span><span class="sxs-lookup"><span data-stu-id="60a15-112">Count of **SPropProblem** structures to be included in the new structure.</span></span> 
    
<span data-ttu-id="60a15-113">_ _name_</span><span class="sxs-lookup"><span data-stu-id="60a15-113">_ _name_</span></span>
  
> <span data-ttu-id="60a15-114">新しい構造の名前。</span><span class="sxs-lookup"><span data-stu-id="60a15-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="60a15-115">注釈</span><span class="sxs-lookup"><span data-stu-id="60a15-115">Remarks</span></span>

<span data-ttu-id="60a15-116">**SizedSPropProblemArray** マクロを使用して、明示的な境界を持つプロパティの問題配列を作成します。</span><span class="sxs-lookup"><span data-stu-id="60a15-116">Use the **SizedSPropProblemArray** macro to create a property problem array with explicit bounds.</span></span> <span data-ttu-id="60a15-117">**SizedSPropProblemArray** マクロから得られた新しい構造を **SPropProblemArray** 構造体へのポインターとして使用するには、次のキャストを実行します。</span><span class="sxs-lookup"><span data-stu-id="60a15-117">To use the new structure that results from the **SizedSPropProblemArray** macro as a pointer to an **SPropProblemArray** structure, perform the following cast:</span></span> 
  
```cpp
lpPropProbArray = (LPSPropProblemArray) &SizedSPropProblemArray;
```

## <a name="see-also"></a><span data-ttu-id="60a15-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="60a15-118">See also</span></span>

- [<span data-ttu-id="60a15-119">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="60a15-119">SPropProblemArray</span></span>](spropproblemarray.md)
- [<span data-ttu-id="60a15-120">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="60a15-120">SPropProblem</span></span>](spropproblem.md)
- [<span data-ttu-id="60a15-121">構造に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="60a15-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

