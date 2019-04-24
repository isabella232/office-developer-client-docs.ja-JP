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
ms.openlocfilehash: afac8c352ad0a07fcb1cd98683b6a5c87940ab4d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357527"
---
# <a name="sbitmaskrestriction"></a><span data-ttu-id="05526-103">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="05526-103">SBitMaskRestriction</span></span>

  
  
<span data-ttu-id="05526-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="05526-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="05526-105">ビット単位の**and**演算を実行し、結果をテストするために使用されるビットマスク制限について説明します。</span><span class="sxs-lookup"><span data-stu-id="05526-105">Describes a bitmask restriction, which is used to perform a bitwise **AND** operation and test the result.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="05526-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="05526-106">Header file:</span></span>  <br/> |<span data-ttu-id="05526-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="05526-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBitMaskRestriction
{
  ULONG relBMR;
  PT_LONG ulPropTag;
  ULONG ulMask;
} SBitMaskRestriction;

```

## <a name="members"></a><span data-ttu-id="05526-108">Members</span><span class="sxs-lookup"><span data-stu-id="05526-108">Members</span></span>

 <span data-ttu-id="05526-109">**relbmr**</span><span class="sxs-lookup"><span data-stu-id="05526-109">**relBMR**</span></span>
  
> <span data-ttu-id="05526-110">**ulmask**メンバーで指定されたマスクを property タグに適用する方法を記述するリレーショナル演算子です。</span><span class="sxs-lookup"><span data-stu-id="05526-110">Relational operator that describes how the mask specified in the **ulMask** member should be applied to the property tag.</span></span> <span data-ttu-id="05526-111">可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="05526-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="05526-112">BMR_EQZ</span><span class="sxs-lookup"><span data-stu-id="05526-112">BMR_EQZ</span></span> 
  
> <span data-ttu-id="05526-113">**ulPropTag**メンバーによって表されるプロパティを使用して、 **ulmask**メンバーのマスクのビット単位の**and**演算を実行し、0と等しいことをテストします。</span><span class="sxs-lookup"><span data-stu-id="05526-113">Perform a bitwise **AND** operation of the mask in the **ulMask** member with the property represented by the **ulPropTag** member and test for being equal to zero.</span></span> 
    
<span data-ttu-id="05526-114">BMR_NEZ</span><span class="sxs-lookup"><span data-stu-id="05526-114">BMR_NEZ</span></span> 
  
> <span data-ttu-id="05526-115">**ulPropTag**メンバーによって表されるプロパティを使用して**ulmask**メンバーのマスクのビット単位の**and**演算を実行し、0と等しくないことをテストします。</span><span class="sxs-lookup"><span data-stu-id="05526-115">Perform a bitwise **AND** operation of the mask in the **ulMask** member with the property represented by the **ulPropTag** member and test for being not equal to zero.</span></span> 
    
 <span data-ttu-id="05526-116">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="05526-116">**ulPropTag**</span></span>
  
> <span data-ttu-id="05526-117">ビットマスクを適用するプロパティのプロパティタグ。</span><span class="sxs-lookup"><span data-stu-id="05526-117">Property tag of the property to which the bitmask is applied.</span></span>
    
 <span data-ttu-id="05526-118">**ulmask**</span><span class="sxs-lookup"><span data-stu-id="05526-118">**ulMask**</span></span>
  
> <span data-ttu-id="05526-119">**ulPropTag**によって識別されるプロパティに適用するビットマスク。</span><span class="sxs-lookup"><span data-stu-id="05526-119">Bitmask to apply to the property identified by **ulPropTag**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="05526-120">解説</span><span class="sxs-lookup"><span data-stu-id="05526-120">Remarks</span></span>

<span data-ttu-id="05526-121">**sbitmaskrestriction**構造体は、 **ulmask**メンバーで記述されたビットマスクと**ulPropTag**メンバーによって記述されたプロパティの値を使用して、ビット単位の**and**演算を実行します。</span><span class="sxs-lookup"><span data-stu-id="05526-121">The **SBitMaskRestriction** structure performs a bitwise **AND** operation using the bitmask described in the **ulMask** member and the value of the property described by the **ulPropTag** member.</span></span> <span data-ttu-id="05526-122">result が0の場合は、BMR_EQZ が満たされています。</span><span class="sxs-lookup"><span data-stu-id="05526-122">If the result is zero, BMR_EQZ is satisfied.</span></span> <span data-ttu-id="05526-123">0以外の場合、つまり、プロパティ値に**ulmask**として設定されている同じビットが少なくとも1つある場合、BMR_NEZ は満たされています。</span><span class="sxs-lookup"><span data-stu-id="05526-123">If it is nonzero, that is, if the property value has at least one of the same bits set as **ulMask**, then BMR_NEZ is satisfied.</span></span>
  
<span data-ttu-id="05526-124">一般的な**sbitmaskrestriction**構造体と制限事項の詳細については、「[制限につい](about-restrictions.md)て」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="05526-124">For more information about the **SBitMaskRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="05526-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="05526-125">See also</span></span>



[<span data-ttu-id="05526-126">SRestriction</span><span class="sxs-lookup"><span data-stu-id="05526-126">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="05526-127">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="05526-127">MAPI Structures</span></span>](mapi-structures.md)

