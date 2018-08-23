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
ms.openlocfilehash: e71658922b6cb80dadc7e034a51c10189c4207ed
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568498"
---
# <a name="spropproblemarray"></a><span data-ttu-id="0303d-103">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="0303d-103">SPropProblemArray</span></span>

  
  
<span data-ttu-id="0303d-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0303d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0303d-105">1 つまたは複数の[SPropProblem](spropproblem.md)構造体の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0303d-105">Contains an array of one or more [SPropProblem](spropproblem.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0303d-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="0303d-106">Header file:</span></span>  <br/> |<span data-ttu-id="0303d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0303d-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="0303d-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="0303d-108">Related macros:</span></span>  <br/> |[<span data-ttu-id="0303d-109">CbNewSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="0303d-109">CbNewSPropProblemArray</span></span>](cbnewspropproblemarray.md) <br/> [<span data-ttu-id="0303d-110">CbSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="0303d-110">CbSPropProblemArray</span></span>](cbspropproblemarray.md) <br/> [<span data-ttu-id="0303d-111">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="0303d-111">SizedSPropProblemArray</span></span>](sizedspropproblemarray.md) <br/> |
   
```cpp
typedef struct _SPropProblemArray
{
  ULONG cProblem;
  SPropProblem aProblem[MAPI_DIM];
} SPropProblemArray, FAR *LPSPropProblemArray;

```

## <a name="members"></a><span data-ttu-id="0303d-112">Members</span><span class="sxs-lookup"><span data-stu-id="0303d-112">Members</span></span>

 <span data-ttu-id="0303d-113">**cProblem**</span><span class="sxs-lookup"><span data-stu-id="0303d-113">**cProblem**</span></span>
  
> <span data-ttu-id="0303d-114">**かかわる問題**のメンバーで指定された配列内の[SPropProblem](spropproblem.md)構造体の数です。</span><span class="sxs-lookup"><span data-stu-id="0303d-114">Count of [SPropProblem](spropproblem.md) structures in the array indicated by the **aProblem** member.</span></span> 
    
 <span data-ttu-id="0303d-115">**かかわる問題**</span><span class="sxs-lookup"><span data-stu-id="0303d-115">**aProblem**</span></span>
  
> <span data-ttu-id="0303d-116">プロパティのエラーを記述する**SPropProblem**構造体の配列。</span><span class="sxs-lookup"><span data-stu-id="0303d-116">Array of **SPropProblem** structures, each describing a property error.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0303d-117">注釈</span><span class="sxs-lookup"><span data-stu-id="0303d-117">Remarks</span></span>

<span data-ttu-id="0303d-118">プロパティに関連するエラーと**SPropProblem**と**SPropProblemArray**の構造体のしくみの詳細については、 [MAPI 名前付きプロパティ](mapi-named-properties.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0303d-118">For more information about how the **SPropProblem** and **SPropProblemArray** structures work with errors related to properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0303d-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="0303d-119">See also</span></span>



[<span data-ttu-id="0303d-120">SCODE</span><span class="sxs-lookup"><span data-stu-id="0303d-120">SCODE</span></span>](scode.md)
  
[<span data-ttu-id="0303d-121">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="0303d-121">SPropProblem</span></span>](spropproblem.md)


[<span data-ttu-id="0303d-122">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="0303d-122">MAPI Structures</span></span>](mapi-structures.md)

