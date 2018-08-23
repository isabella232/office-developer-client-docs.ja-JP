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
ms.openlocfilehash: b8521172b441bd26a6562aa28f836d453544928f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803927"
---
# <a name="sizedspropproblemarray"></a><span data-ttu-id="7d1b0-103">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="7d1b0-103">SizedSPropProblemArray</span></span>

<span data-ttu-id="7d1b0-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7d1b0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7d1b0-105">[SPropProblem](spropproblem.md)構造体の指定した数値を含む名前付き[SPropProblemArray](spropproblemarray.md)構造体を作成します。</span><span class="sxs-lookup"><span data-stu-id="7d1b0-105">Creates a named [SPropProblemArray](spropproblemarray.md) structure that contains a specified number of [SPropProblem](spropproblem.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7d1b0-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="7d1b0-106">Header file:</span></span>  <br/> |<span data-ttu-id="7d1b0-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7d1b0-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="7d1b0-108">関連の構造体。</span><span class="sxs-lookup"><span data-stu-id="7d1b0-108">Related structure:</span></span>  <br/> |<span data-ttu-id="7d1b0-109">**SPropProblemArray**</span><span class="sxs-lookup"><span data-stu-id="7d1b0-109">**SPropProblemArray**</span></span> <br/> |
   
```cpp
SizedSPropProblemArray(_cprob, _name)
```

## <a name="parameters"></a><span data-ttu-id="7d1b0-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7d1b0-110">Parameters</span></span>

<span data-ttu-id="7d1b0-111">__cprob_</span><span class="sxs-lookup"><span data-stu-id="7d1b0-111">__cprob_</span></span>
  
> <span data-ttu-id="7d1b0-112">新しい構造体に含まれる**SPropProblem**構造体の数です。</span><span class="sxs-lookup"><span data-stu-id="7d1b0-112">Count of **SPropProblem** structures to be included in the new structure.</span></span> 
    
<span data-ttu-id="7d1b0-113">__名_</span><span class="sxs-lookup"><span data-stu-id="7d1b0-113">__name_</span></span>
  
> <span data-ttu-id="7d1b0-114">新しい構造体の名前です。</span><span class="sxs-lookup"><span data-stu-id="7d1b0-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7d1b0-115">注釈</span><span class="sxs-lookup"><span data-stu-id="7d1b0-115">Remarks</span></span>

<span data-ttu-id="7d1b0-116">**SizedSPropProblemArray**マクロを使用すると、明示的な境界を持つプロパティの問題の配列を作成します。</span><span class="sxs-lookup"><span data-stu-id="7d1b0-116">Use the **SizedSPropProblemArray** macro to create a property problem array with explicit bounds.</span></span> <span data-ttu-id="7d1b0-117">**SPropProblemArray**構造体へのポインターとしての**SizedSPropProblemArray**マクロの結果を新しい構造体を使用するには、次のキャストを実行します。</span><span class="sxs-lookup"><span data-stu-id="7d1b0-117">To use the new structure that results from the **SizedSPropProblemArray** macro as a pointer to an **SPropProblemArray** structure, perform the following cast:</span></span> 
  
```cpp
lpPropProbArray = (LPSPropProblemArray) &SizedSPropProblemArray;
```

## <a name="see-also"></a><span data-ttu-id="7d1b0-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="7d1b0-118">See also</span></span>

- [<span data-ttu-id="7d1b0-119">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="7d1b0-119">SPropProblemArray</span></span>](spropproblemarray.md)
- [<span data-ttu-id="7d1b0-120">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="7d1b0-120">SPropProblem</span></span>](spropproblem.md)
- [<span data-ttu-id="7d1b0-121">構造体に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="7d1b0-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

