---
title: SBitMaskRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBitMaskRestriction
api_type:
- COM
ms.assetid: ddd42180-6e4f-410c-9f78-d868a91452dc
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f0cf6fa03d8f38b7d160a8747111445cfdac1ae9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803804"
---
# <a name="sbitmaskrestriction"></a><span data-ttu-id="da239-103">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="da239-103">SBitMaskRestriction</span></span>

  
  
<span data-ttu-id="da239-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="da239-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="da239-105">ビットごとの**AND**演算を実行し、結果をテストするために使用されるビットマスクの制限について説明します。</span><span class="sxs-lookup"><span data-stu-id="da239-105">Describes a bitmask restriction, which is used to perform a bitwise **AND** operation and test the result.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="da239-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="da239-106">Header file:</span></span>  <br/> |<span data-ttu-id="da239-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="da239-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBitMaskRestriction
{
  ULONG relBMR;
  PT_LONG ulPropTag;
  ULONG ulMask;
} SBitMaskRestriction;

```

## <a name="members"></a><span data-ttu-id="da239-108">Members</span><span class="sxs-lookup"><span data-stu-id="da239-108">Members</span></span>

 <span data-ttu-id="da239-109">**relBMR**</span><span class="sxs-lookup"><span data-stu-id="da239-109">**relBMR**</span></span>
  
> <span data-ttu-id="da239-110">プロパティ タグに**ulMask**のメンバーで指定されたマスクを適用する方法を説明する関係演算子です。</span><span class="sxs-lookup"><span data-stu-id="da239-110">Relational operator that describes how the mask specified in the **ulMask** member should be applied to the property tag.</span></span> <span data-ttu-id="da239-111">使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="da239-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="da239-112">BMR_EQZ</span><span class="sxs-lookup"><span data-stu-id="da239-112">BMR_EQZ</span></span> 
  
> <span data-ttu-id="da239-113">0 のテストと**ulPropTag**のメンバーによって表されるプロパティを使用して、 **ulMask**のメンバーで、マスクのビットごとの**AND**演算を実行します。</span><span class="sxs-lookup"><span data-stu-id="da239-113">Perform a bitwise **AND** operation of the mask in the **ulMask** member with the property represented by the **ulPropTag** member and test for being equal to zero.</span></span> 
    
<span data-ttu-id="da239-114">BMR_NEZ</span><span class="sxs-lookup"><span data-stu-id="da239-114">BMR_NEZ</span></span> 
  
> <span data-ttu-id="da239-115">**UlMask**メンバーが 0 のテストと**ulPropTag**のメンバーによって表されるプロパティを使用してマスクのビットごとの**AND**演算を実行します。</span><span class="sxs-lookup"><span data-stu-id="da239-115">Perform a bitwise **AND** operation of the mask in the **ulMask** member with the property represented by the **ulPropTag** member and test for being not equal to zero.</span></span> 
    
 <span data-ttu-id="da239-116">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="da239-116">**ulPropTag**</span></span>
  
> <span data-ttu-id="da239-117">ビット マスクを適用するプロパティのプロパティ タグです。</span><span class="sxs-lookup"><span data-stu-id="da239-117">Property tag of the property to which the bitmask is applied.</span></span>
    
 <span data-ttu-id="da239-118">**ulMask**</span><span class="sxs-lookup"><span data-stu-id="da239-118">**ulMask**</span></span>
  
> <span data-ttu-id="da239-119">**UlPropTag**によって識別されるプロパティに適用するビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="da239-119">Bitmask to apply to the property identified by **ulPropTag**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="da239-120">注釈</span><span class="sxs-lookup"><span data-stu-id="da239-120">Remarks</span></span>

<span data-ttu-id="da239-121">**SBitMaskRestriction**構造体は、 **ulMask**のメンバーと**ulPropTag**のメンバーによって記述されたプロパティの値で説明するビットマスクを使用してビットごとの**AND**演算を実行します。</span><span class="sxs-lookup"><span data-stu-id="da239-121">The **SBitMaskRestriction** structure performs a bitwise **AND** operation using the bitmask described in the **ulMask** member and the value of the property described by the **ulPropTag** member.</span></span> <span data-ttu-id="da239-122">結果がゼロの場合は、BMR_EQZ が満たされます。</span><span class="sxs-lookup"><span data-stu-id="da239-122">If the result is zero, BMR_EQZ is satisfied.</span></span> <span data-ttu-id="da239-123">0 以外の場合は、プロパティの値を持つ**ulMask**、としてセットされている同じビットが少なくとも 1 つの場合、BMR_NEZ、満たされます。</span><span class="sxs-lookup"><span data-stu-id="da239-123">If it is nonzero, that is, if the property value has at least one of the same bits set as **ulMask**, then BMR_NEZ is satisfied.</span></span>
  
<span data-ttu-id="da239-124">**SBitMaskRestriction**構造体および制限の詳細については一般に、[制限の詳細](about-restrictions.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="da239-124">For more information about the **SBitMaskRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="da239-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="da239-125">See also</span></span>



[<span data-ttu-id="da239-126">SRestriction</span><span class="sxs-lookup"><span data-stu-id="da239-126">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="da239-127">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="da239-127">MAPI Structures</span></span>](mapi-structures.md)

