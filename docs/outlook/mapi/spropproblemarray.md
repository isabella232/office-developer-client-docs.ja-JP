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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f78e0ed939e190a9855ea4b040d18c01cfecc91d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357842"
---
# <a name="spropproblemarray"></a><span data-ttu-id="0c74e-103">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="0c74e-103">SPropProblemArray</span></span>

  
  
<span data-ttu-id="0c74e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c74e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c74e-105">1つ以上の[spropproblem](spropproblem.md)構造の配列を含みます。</span><span class="sxs-lookup"><span data-stu-id="0c74e-105">Contains an array of one or more [SPropProblem](spropproblem.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0c74e-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="0c74e-106">Header file:</span></span>  <br/> |<span data-ttu-id="0c74e-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0c74e-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="0c74e-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="0c74e-108">Related macros:</span></span>  <br/> |[<span data-ttu-id="0c74e-109">CbNewSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="0c74e-109">CbNewSPropProblemArray</span></span>](cbnewspropproblemarray.md) <br/> [<span data-ttu-id="0c74e-110">CbSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="0c74e-110">CbSPropProblemArray</span></span>](cbspropproblemarray.md) <br/> [<span data-ttu-id="0c74e-111">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="0c74e-111">SizedSPropProblemArray</span></span>](sizedspropproblemarray.md) <br/> |
   
```cpp
typedef struct _SPropProblemArray
{
  ULONG cProblem;
  SPropProblem aProblem[MAPI_DIM];
} SPropProblemArray, FAR *LPSPropProblemArray;

```

## <a name="members"></a><span data-ttu-id="0c74e-112">Members</span><span class="sxs-lookup"><span data-stu-id="0c74e-112">Members</span></span>

 <span data-ttu-id="0c74e-113">**cproblem**</span><span class="sxs-lookup"><span data-stu-id="0c74e-113">**cProblem**</span></span>
  
> <span data-ttu-id="0c74e-114">**aproblem**メンバーによって示された、配列内の[spropproblem](spropproblem.md)構造体の数。</span><span class="sxs-lookup"><span data-stu-id="0c74e-114">Count of [SPropProblem](spropproblem.md) structures in the array indicated by the **aProblem** member.</span></span> 
    
 <span data-ttu-id="0c74e-115">**aproblem**</span><span class="sxs-lookup"><span data-stu-id="0c74e-115">**aProblem**</span></span>
  
> <span data-ttu-id="0c74e-116">プロパティエラーを説明する**spropproblem**構造の配列です。</span><span class="sxs-lookup"><span data-stu-id="0c74e-116">Array of **SPropProblem** structures, each describing a property error.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0c74e-117">解説</span><span class="sxs-lookup"><span data-stu-id="0c74e-117">Remarks</span></span>

<span data-ttu-id="0c74e-118">プロパティに関連するエラーについて、 **spropproblem**および**spropproblem の配列**構造がどのように機能するかの詳細については、「 [MAPI の名前付きプロパティ](mapi-named-properties.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0c74e-118">For more information about how the **SPropProblem** and **SPropProblemArray** structures work with errors related to properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0c74e-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="0c74e-119">See also</span></span>



[<span data-ttu-id="0c74e-120">SCODE</span><span class="sxs-lookup"><span data-stu-id="0c74e-120">SCODE</span></span>](scode.md)
  
[<span data-ttu-id="0c74e-121">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="0c74e-121">SPropProblem</span></span>](spropproblem.md)


[<span data-ttu-id="0c74e-122">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="0c74e-122">MAPI Structures</span></span>](mapi-structures.md)

