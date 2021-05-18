---
title: SPropProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropProblemArray
api_type:
- COM
ms.assetid: 3fbaa77a-be43-4fce-af67-1826ee101799
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f78e0ed939e190a9855ea4b040d18c01cfecc91d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406858"
---
# <a name="spropproblemarray"></a><span data-ttu-id="2aede-103">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="2aede-103">SPropProblemArray</span></span>

  
  
<span data-ttu-id="2aede-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2aede-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2aede-105">1 つ以上の [SPropProblem 構造体の配列を格納](spropproblem.md) します。</span><span class="sxs-lookup"><span data-stu-id="2aede-105">Contains an array of one or more [SPropProblem](spropproblem.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2aede-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="2aede-106">Header file:</span></span>  <br/> |<span data-ttu-id="2aede-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2aede-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="2aede-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="2aede-108">Related macros:</span></span>  <br/> |[<span data-ttu-id="2aede-109">CbNewSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="2aede-109">CbNewSPropProblemArray</span></span>](cbnewspropproblemarray.md) <br/> [<span data-ttu-id="2aede-110">CbSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="2aede-110">CbSPropProblemArray</span></span>](cbspropproblemarray.md) <br/> [<span data-ttu-id="2aede-111">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="2aede-111">SizedSPropProblemArray</span></span>](sizedspropproblemarray.md) <br/> |
   
```cpp
typedef struct _SPropProblemArray
{
  ULONG cProblem;
  SPropProblem aProblem[MAPI_DIM];
} SPropProblemArray, FAR *LPSPropProblemArray;

```

## <a name="members"></a><span data-ttu-id="2aede-112">Members</span><span class="sxs-lookup"><span data-stu-id="2aede-112">Members</span></span>

 <span data-ttu-id="2aede-113">**cProblem**</span><span class="sxs-lookup"><span data-stu-id="2aede-113">**cProblem**</span></span>
  
> <span data-ttu-id="2aede-114">[aProblem メンバーによって示](spropproblem.md)される配列内の **SPropProblem** 構造体の数。</span><span class="sxs-lookup"><span data-stu-id="2aede-114">Count of [SPropProblem](spropproblem.md) structures in the array indicated by the **aProblem** member.</span></span> 
    
 <span data-ttu-id="2aede-115">**aProblem**</span><span class="sxs-lookup"><span data-stu-id="2aede-115">**aProblem**</span></span>
  
> <span data-ttu-id="2aede-116">プロパティ エラー **を記述する SPropProblem** 構造体の配列。</span><span class="sxs-lookup"><span data-stu-id="2aede-116">Array of **SPropProblem** structures, each describing a property error.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2aede-117">注釈</span><span class="sxs-lookup"><span data-stu-id="2aede-117">Remarks</span></span>

<span data-ttu-id="2aede-118">**SPropProblem** 構造体と **SPropProblemArray** 構造体がプロパティに関連するエラーを処理する方法の詳細については、「MAPI 名前付きプロパティ」[を参照してください](mapi-named-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="2aede-118">For more information about how the **SPropProblem** and **SPropProblemArray** structures work with errors related to properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2aede-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="2aede-119">See also</span></span>



[<span data-ttu-id="2aede-120">SCODE</span><span class="sxs-lookup"><span data-stu-id="2aede-120">SCODE</span></span>](scode.md)
  
[<span data-ttu-id="2aede-121">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="2aede-121">SPropProblem</span></span>](spropproblem.md)


[<span data-ttu-id="2aede-122">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="2aede-122">MAPI Structures</span></span>](mapi-structures.md)

