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
ms.openlocfilehash: 3fd61828cd631c4abc0131da867ca213a3c44d20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803997"
---
# <a name="spropproblemarray"></a><span data-ttu-id="712df-103">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="712df-103">SPropProblemArray</span></span>

  
  
<span data-ttu-id="712df-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="712df-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="712df-105">1 つまたは複数の[SPropProblem](spropproblem.md)構造体の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="712df-105">Contains an array of one or more [SPropProblem](spropproblem.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="712df-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="712df-106">Header file:</span></span>  <br/> |<span data-ttu-id="712df-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="712df-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="712df-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="712df-108">Related macros:</span></span>  <br/> |[<span data-ttu-id="712df-109">CbNewSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="712df-109">CbNewSPropProblemArray</span></span>](cbnewspropproblemarray.md) <br/> [<span data-ttu-id="712df-110">CbSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="712df-110">CbSPropProblemArray</span></span>](cbspropproblemarray.md) <br/> [<span data-ttu-id="712df-111">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="712df-111">SizedSPropProblemArray</span></span>](sizedspropproblemarray.md) <br/> |
   
```cpp
typedef struct _SPropProblemArray
{
  ULONG cProblem;
  SPropProblem aProblem[MAPI_DIM];
} SPropProblemArray, FAR *LPSPropProblemArray;

```

## <a name="members"></a><span data-ttu-id="712df-112">Members</span><span class="sxs-lookup"><span data-stu-id="712df-112">Members</span></span>

 <span data-ttu-id="712df-113">**cProblem**</span><span class="sxs-lookup"><span data-stu-id="712df-113">**cProblem**</span></span>
  
> <span data-ttu-id="712df-114">**かかわる問題**のメンバーで指定された配列内の[SPropProblem](spropproblem.md)構造体の数です。</span><span class="sxs-lookup"><span data-stu-id="712df-114">Count of [SPropProblem](spropproblem.md) structures in the array indicated by the **aProblem** member.</span></span> 
    
 <span data-ttu-id="712df-115">**かかわる問題**</span><span class="sxs-lookup"><span data-stu-id="712df-115">**aProblem**</span></span>
  
> <span data-ttu-id="712df-116">プロパティのエラーを記述する**SPropProblem**構造体の配列。</span><span class="sxs-lookup"><span data-stu-id="712df-116">Array of **SPropProblem** structures, each describing a property error.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="712df-117">注釈</span><span class="sxs-lookup"><span data-stu-id="712df-117">Remarks</span></span>

<span data-ttu-id="712df-118">プロパティに関連するエラーと**SPropProblem**と**SPropProblemArray**の構造体のしくみの詳細については、 [MAPI 名前付きプロパティ](mapi-named-properties.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="712df-118">For more information about how the **SPropProblem** and **SPropProblemArray** structures work with errors related to properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="712df-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="712df-119">See also</span></span>



[<span data-ttu-id="712df-120">SCODE</span><span class="sxs-lookup"><span data-stu-id="712df-120">SCODE</span></span>](scode.md)
  
[<span data-ttu-id="712df-121">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="712df-121">SPropProblem</span></span>](spropproblem.md)


[<span data-ttu-id="712df-122">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="712df-122">MAPI Structures</span></span>](mapi-structures.md)

