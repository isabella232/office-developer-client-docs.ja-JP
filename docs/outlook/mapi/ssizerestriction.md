---
title: SSizeRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSizeRestriction
api_type:
- COM
ms.assetid: 4e7340d1-3cb9-4276-b83f-1c8f94acb909
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 24ceb7b5358447de3a240756227b86224d2c354c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344479"
---
# <a name="ssizerestriction"></a><span data-ttu-id="604dc-103">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="604dc-103">SSizeRestriction</span></span>

  
  
<span data-ttu-id="604dc-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="604dc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="604dc-105">プロパティ値のサイズをテストするために使用されるサイズ制限を記述します。</span><span class="sxs-lookup"><span data-stu-id="604dc-105">Describes a size restriction which is used to test the size of a property value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="604dc-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="604dc-106">Header file:</span></span>  <br/> |<span data-ttu-id="604dc-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="604dc-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSizeRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  ULONG cb;
} SSizeRestriction;

```

## <a name="members"></a><span data-ttu-id="604dc-108">Members</span><span class="sxs-lookup"><span data-stu-id="604dc-108">Members</span></span>

 <span data-ttu-id="604dc-109">**relop**</span><span class="sxs-lookup"><span data-stu-id="604dc-109">**relop**</span></span>
  
> <span data-ttu-id="604dc-110">サイズ比較で使用されるリレーショナル演算子です。</span><span class="sxs-lookup"><span data-stu-id="604dc-110">Relational operator that is used in the size comparison.</span></span> <span data-ttu-id="604dc-111">可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="604dc-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="604dc-112">RELOP_GE</span><span class="sxs-lookup"><span data-stu-id="604dc-112">RELOP_GE</span></span> 
  
> <span data-ttu-id="604dc-113">この比較は、最初の値よりも大きくなるか等しいかに基づいて行われます。</span><span class="sxs-lookup"><span data-stu-id="604dc-113">The comparison is made based on a greater or equal first value.</span></span>
    
<span data-ttu-id="604dc-114">RELOP_GT</span><span class="sxs-lookup"><span data-stu-id="604dc-114">RELOP_GT</span></span> 
  
> <span data-ttu-id="604dc-115">比較は、より大きな最初の値に基づいて行われます。</span><span class="sxs-lookup"><span data-stu-id="604dc-115">The comparison is made based on a greater first value.</span></span>
    
<span data-ttu-id="604dc-116">RELOP_LE</span><span class="sxs-lookup"><span data-stu-id="604dc-116">RELOP_LE</span></span> 
  
> <span data-ttu-id="604dc-117">比較は、1番目の値よりも小さいか等しいかに基づいて行われます。</span><span class="sxs-lookup"><span data-stu-id="604dc-117">The comparison is made based on a lesser or equal first value.</span></span>
    
<span data-ttu-id="604dc-118">RELOP_LT</span><span class="sxs-lookup"><span data-stu-id="604dc-118">RELOP_LT</span></span> 
  
> <span data-ttu-id="604dc-119">比較は、小さい方の値に基づいて行われます。</span><span class="sxs-lookup"><span data-stu-id="604dc-119">The comparison is made based on a lesser first value.</span></span>
    
<span data-ttu-id="604dc-120">RELOP_NE</span><span class="sxs-lookup"><span data-stu-id="604dc-120">RELOP_NE</span></span> 
  
> <span data-ttu-id="604dc-121">比較は、等しくない値に基づいて行われます。</span><span class="sxs-lookup"><span data-stu-id="604dc-121">The comparison is made based on unequal values.</span></span>
    
<span data-ttu-id="604dc-122">RELOP_RE</span><span class="sxs-lookup"><span data-stu-id="604dc-122">RELOP_RE</span></span> 
  
> <span data-ttu-id="604dc-123">比較は、LIKE (正規表現) の値に基づいて行われます。</span><span class="sxs-lookup"><span data-stu-id="604dc-123">The comparison is made based on LIKE (regular expression) values.</span></span>
    
<span data-ttu-id="604dc-124">RELOP_EQ</span><span class="sxs-lookup"><span data-stu-id="604dc-124">RELOP_EQ</span></span> 
  
> <span data-ttu-id="604dc-125">比較は同じ値に基づいて行われます。</span><span class="sxs-lookup"><span data-stu-id="604dc-125">The comparison is made based on equal values.</span></span>
    
 <span data-ttu-id="604dc-126">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="604dc-126">**ulPropTag**</span></span>
  
> <span data-ttu-id="604dc-127">テストするプロパティを識別するプロパティタグ。</span><span class="sxs-lookup"><span data-stu-id="604dc-127">Property tag identifying the property to test.</span></span>
    
 <span data-ttu-id="604dc-128">**cb**</span><span class="sxs-lookup"><span data-stu-id="604dc-128">**cb**</span></span>
  
> <span data-ttu-id="604dc-129">プロパティ値のバイト数。</span><span class="sxs-lookup"><span data-stu-id="604dc-129">Count of bytes in the property value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="604dc-130">解説</span><span class="sxs-lookup"><span data-stu-id="604dc-130">Remarks</span></span>

<span data-ttu-id="604dc-131">制限のしくみについての一般的な説明については、「[制限につい](about-restrictions.md)て」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="604dc-131">For a general discussion of how restrictions work, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="604dc-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="604dc-132">See also</span></span>



[<span data-ttu-id="604dc-133">SRestriction</span><span class="sxs-lookup"><span data-stu-id="604dc-133">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="604dc-134">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="604dc-134">MAPI Structures</span></span>](mapi-structures.md)

