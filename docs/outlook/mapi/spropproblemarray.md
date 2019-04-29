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
# <a name="spropproblemarray"></a><span data-ttu-id="f8dbf-103">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="f8dbf-103">SPropProblemArray</span></span>

  
  
<span data-ttu-id="f8dbf-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f8dbf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f8dbf-105">1つ以上の[spropproblem](spropproblem.md)構造の配列を含みます。</span><span class="sxs-lookup"><span data-stu-id="f8dbf-105">Contains an array of one or more [SPropProblem](spropproblem.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f8dbf-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="f8dbf-106">Header file:</span></span>  <br/> |<span data-ttu-id="f8dbf-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f8dbf-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="f8dbf-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="f8dbf-108">Related macros:</span></span>  <br/> |[<span data-ttu-id="f8dbf-109">CbNewSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="f8dbf-109">CbNewSPropProblemArray</span></span>](cbnewspropproblemarray.md) <br/> [<span data-ttu-id="f8dbf-110">CbSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="f8dbf-110">CbSPropProblemArray</span></span>](cbspropproblemarray.md) <br/> [<span data-ttu-id="f8dbf-111">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="f8dbf-111">SizedSPropProblemArray</span></span>](sizedspropproblemarray.md) <br/> |
   
```cpp
typedef struct _SPropProblemArray
{
  ULONG cProblem;
  SPropProblem aProblem[MAPI_DIM];
} SPropProblemArray, FAR *LPSPropProblemArray;

```

## <a name="members"></a><span data-ttu-id="f8dbf-112">メンバー</span><span class="sxs-lookup"><span data-stu-id="f8dbf-112">Members</span></span>

 <span data-ttu-id="f8dbf-113">**cproblem**</span><span class="sxs-lookup"><span data-stu-id="f8dbf-113">**cProblem**</span></span>
  
> <span data-ttu-id="f8dbf-114">**aproblem**メンバーによって示された、配列内の[spropproblem](spropproblem.md)構造体の数。</span><span class="sxs-lookup"><span data-stu-id="f8dbf-114">Count of [SPropProblem](spropproblem.md) structures in the array indicated by the **aProblem** member.</span></span> 
    
 <span data-ttu-id="f8dbf-115">**aproblem**</span><span class="sxs-lookup"><span data-stu-id="f8dbf-115">**aProblem**</span></span>
  
> <span data-ttu-id="f8dbf-116">プロパティエラーを説明する**spropproblem**構造の配列です。</span><span class="sxs-lookup"><span data-stu-id="f8dbf-116">Array of **SPropProblem** structures, each describing a property error.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f8dbf-117">注釈</span><span class="sxs-lookup"><span data-stu-id="f8dbf-117">Remarks</span></span>

<span data-ttu-id="f8dbf-118">プロパティに関連するエラーについて、 **spropproblem**および**spropproblem の配列**構造がどのように機能するかの詳細については、「 [MAPI の名前付きプロパティ](mapi-named-properties.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8dbf-118">For more information about how the **SPropProblem** and **SPropProblemArray** structures work with errors related to properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f8dbf-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="f8dbf-119">See also</span></span>



[<span data-ttu-id="f8dbf-120">SCODE</span><span class="sxs-lookup"><span data-stu-id="f8dbf-120">SCODE</span></span>](scode.md)
  
[<span data-ttu-id="f8dbf-121">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="f8dbf-121">SPropProblem</span></span>](spropproblem.md)


[<span data-ttu-id="f8dbf-122">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="f8dbf-122">MAPI Structures</span></span>](mapi-structures.md)

