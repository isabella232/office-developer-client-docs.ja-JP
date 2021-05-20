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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 24ceb7b5358447de3a240756227b86224d2c354c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439087"
---
# <a name="ssizerestriction"></a><span data-ttu-id="170a8-103">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="170a8-103">SSizeRestriction</span></span>

  
  
<span data-ttu-id="170a8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="170a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="170a8-105">プロパティ値のサイズをテストするために使用されるサイズ制限について説明します。</span><span class="sxs-lookup"><span data-stu-id="170a8-105">Describes a size restriction which is used to test the size of a property value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="170a8-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="170a8-106">Header file:</span></span>  <br/> |<span data-ttu-id="170a8-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="170a8-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSizeRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  ULONG cb;
} SSizeRestriction;

```

## <a name="members"></a><span data-ttu-id="170a8-108">Members</span><span class="sxs-lookup"><span data-stu-id="170a8-108">Members</span></span>

 <span data-ttu-id="170a8-109">**relop**</span><span class="sxs-lookup"><span data-stu-id="170a8-109">**relop**</span></span>
  
> <span data-ttu-id="170a8-110">サイズ比較で使用される関係演算子。</span><span class="sxs-lookup"><span data-stu-id="170a8-110">Relational operator that is used in the size comparison.</span></span> <span data-ttu-id="170a8-111">指定できる値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="170a8-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="170a8-112">RELOP_GE</span><span class="sxs-lookup"><span data-stu-id="170a8-112">RELOP_GE</span></span> 
  
> <span data-ttu-id="170a8-113">比較は、大きいまたは等しい最初の値に基づいて行います。</span><span class="sxs-lookup"><span data-stu-id="170a8-113">The comparison is made based on a greater or equal first value.</span></span>
    
<span data-ttu-id="170a8-114">RELOP_GT</span><span class="sxs-lookup"><span data-stu-id="170a8-114">RELOP_GT</span></span> 
  
> <span data-ttu-id="170a8-115">比較は、大きい最初の値に基づいて行います。</span><span class="sxs-lookup"><span data-stu-id="170a8-115">The comparison is made based on a greater first value.</span></span>
    
<span data-ttu-id="170a8-116">RELOP_LE</span><span class="sxs-lookup"><span data-stu-id="170a8-116">RELOP_LE</span></span> 
  
> <span data-ttu-id="170a8-117">比較は、より小さいか等しい最初の値に基づいて行います。</span><span class="sxs-lookup"><span data-stu-id="170a8-117">The comparison is made based on a lesser or equal first value.</span></span>
    
<span data-ttu-id="170a8-118">RELOP_LT</span><span class="sxs-lookup"><span data-stu-id="170a8-118">RELOP_LT</span></span> 
  
> <span data-ttu-id="170a8-119">比較は、より小さい最初の値に基づいて行います。</span><span class="sxs-lookup"><span data-stu-id="170a8-119">The comparison is made based on a lesser first value.</span></span>
    
<span data-ttu-id="170a8-120">RELOP_NE</span><span class="sxs-lookup"><span data-stu-id="170a8-120">RELOP_NE</span></span> 
  
> <span data-ttu-id="170a8-121">比較は、等しくない値に基づいて行います。</span><span class="sxs-lookup"><span data-stu-id="170a8-121">The comparison is made based on unequal values.</span></span>
    
<span data-ttu-id="170a8-122">RELOP_RE</span><span class="sxs-lookup"><span data-stu-id="170a8-122">RELOP_RE</span></span> 
  
> <span data-ttu-id="170a8-123">比較は LIKE (正規表現) の値に基づいて行います。</span><span class="sxs-lookup"><span data-stu-id="170a8-123">The comparison is made based on LIKE (regular expression) values.</span></span>
    
<span data-ttu-id="170a8-124">RELOP_EQ</span><span class="sxs-lookup"><span data-stu-id="170a8-124">RELOP_EQ</span></span> 
  
> <span data-ttu-id="170a8-125">比較は、等しい値に基づいて行います。</span><span class="sxs-lookup"><span data-stu-id="170a8-125">The comparison is made based on equal values.</span></span>
    
 <span data-ttu-id="170a8-126">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="170a8-126">**ulPropTag**</span></span>
  
> <span data-ttu-id="170a8-127">テストするプロパティを識別するプロパティ タグ。</span><span class="sxs-lookup"><span data-stu-id="170a8-127">Property tag identifying the property to test.</span></span>
    
 <span data-ttu-id="170a8-128">**cb**</span><span class="sxs-lookup"><span data-stu-id="170a8-128">**cb**</span></span>
  
> <span data-ttu-id="170a8-129">プロパティ値のバイト数。</span><span class="sxs-lookup"><span data-stu-id="170a8-129">Count of bytes in the property value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="170a8-130">注釈</span><span class="sxs-lookup"><span data-stu-id="170a8-130">Remarks</span></span>

<span data-ttu-id="170a8-131">制限の動作の一般的な説明については、「 [制限について」を参照してください](about-restrictions.md)。</span><span class="sxs-lookup"><span data-stu-id="170a8-131">For a general discussion of how restrictions work, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="170a8-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="170a8-132">See also</span></span>



[<span data-ttu-id="170a8-133">SRestriction</span><span class="sxs-lookup"><span data-stu-id="170a8-133">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="170a8-134">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="170a8-134">MAPI Structures</span></span>](mapi-structures.md)

