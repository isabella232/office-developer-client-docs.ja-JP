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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: afac8c352ad0a07fcb1cd98683b6a5c87940ab4d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424477"
---
# <a name="sbitmaskrestriction"></a><span data-ttu-id="ad6da-103">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="ad6da-103">SBitMaskRestriction</span></span>

  
  
<span data-ttu-id="ad6da-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ad6da-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ad6da-105">ビットワイズ AND 操作を実行し、結果をテストするために使用されるビットマスク制限について説明します。</span><span class="sxs-lookup"><span data-stu-id="ad6da-105">Describes a bitmask restriction, which is used to perform a bitwise **AND** operation and test the result.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ad6da-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="ad6da-106">Header file:</span></span>  <br/> |<span data-ttu-id="ad6da-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ad6da-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBitMaskRestriction
{
  ULONG relBMR;
  PT_LONG ulPropTag;
  ULONG ulMask;
} SBitMaskRestriction;

```

## <a name="members"></a><span data-ttu-id="ad6da-108">Members</span><span class="sxs-lookup"><span data-stu-id="ad6da-108">Members</span></span>

 <span data-ttu-id="ad6da-109">**relBMR**</span><span class="sxs-lookup"><span data-stu-id="ad6da-109">**relBMR**</span></span>
  
> <span data-ttu-id="ad6da-110">**ulMask** メンバーで指定されたマスクをプロパティ タグに適用する方法を説明する関係演算子。</span><span class="sxs-lookup"><span data-stu-id="ad6da-110">Relational operator that describes how the mask specified in the **ulMask** member should be applied to the property tag.</span></span> <span data-ttu-id="ad6da-111">指定できる値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="ad6da-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="ad6da-112">BMR_EQZ</span><span class="sxs-lookup"><span data-stu-id="ad6da-112">BMR_EQZ</span></span> 
  
> <span data-ttu-id="ad6da-113">**ulPropTag** メンバーで表されるプロパティを使用して **、ulMask** メンバー内のマスクのビット分割 **AND** 操作を実行し、ゼロに等しいかテストします。</span><span class="sxs-lookup"><span data-stu-id="ad6da-113">Perform a bitwise **AND** operation of the mask in the **ulMask** member with the property represented by the **ulPropTag** member and test for being equal to zero.</span></span> 
    
<span data-ttu-id="ad6da-114">BMR_NEZ</span><span class="sxs-lookup"><span data-stu-id="ad6da-114">BMR_NEZ</span></span> 
  
> <span data-ttu-id="ad6da-115">**ulPropTag** メンバーで表されるプロパティを使用して **、ulMask** メンバー内のマスクのビット分割 **AND** 操作を実行し、ゼロに等しくないかテストします。</span><span class="sxs-lookup"><span data-stu-id="ad6da-115">Perform a bitwise **AND** operation of the mask in the **ulMask** member with the property represented by the **ulPropTag** member and test for being not equal to zero.</span></span> 
    
 <span data-ttu-id="ad6da-116">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="ad6da-116">**ulPropTag**</span></span>
  
> <span data-ttu-id="ad6da-117">ビットマスクが適用されるプロパティのプロパティ タグ。</span><span class="sxs-lookup"><span data-stu-id="ad6da-117">Property tag of the property to which the bitmask is applied.</span></span>
    
 <span data-ttu-id="ad6da-118">**ulMask**</span><span class="sxs-lookup"><span data-stu-id="ad6da-118">**ulMask**</span></span>
  
> <span data-ttu-id="ad6da-119">ulPropTag で識別されるプロパティに適用する **ビットマスク**。</span><span class="sxs-lookup"><span data-stu-id="ad6da-119">Bitmask to apply to the property identified by **ulPropTag**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ad6da-120">注釈</span><span class="sxs-lookup"><span data-stu-id="ad6da-120">Remarks</span></span>

<span data-ttu-id="ad6da-121">**SBitMaskRestriction** 構造体は、ulMaskメンバーで説明されているビットマスクと **、ulPropTag** メンバーによって記述されるプロパティの値を使用してビット演算を実行します。 </span><span class="sxs-lookup"><span data-stu-id="ad6da-121">The **SBitMaskRestriction** structure performs a bitwise **AND** operation using the bitmask described in the **ulMask** member and the value of the property described by the **ulPropTag** member.</span></span> <span data-ttu-id="ad6da-122">結果が 0 の場合は、BMR_EQZが満たされます。</span><span class="sxs-lookup"><span data-stu-id="ad6da-122">If the result is zero, BMR_EQZ is satisfied.</span></span> <span data-ttu-id="ad6da-123">0 以外の場合、つまり、プロパティ値に少なくとも 1 つの同じビットが **ulMask** として設定されている場合、BMR_NEZ満たされます。</span><span class="sxs-lookup"><span data-stu-id="ad6da-123">If it is nonzero, that is, if the property value has at least one of the same bits set as **ulMask**, then BMR_NEZ is satisfied.</span></span>
  
<span data-ttu-id="ad6da-124">**SBitMaskRestriction** 構造と制限全般の詳細については、「制限について [」を参照してください](about-restrictions.md)。</span><span class="sxs-lookup"><span data-stu-id="ad6da-124">For more information about the **SBitMaskRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ad6da-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="ad6da-125">See also</span></span>



[<span data-ttu-id="ad6da-126">SRestriction</span><span class="sxs-lookup"><span data-stu-id="ad6da-126">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="ad6da-127">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="ad6da-127">MAPI Structures</span></span>](mapi-structures.md)

