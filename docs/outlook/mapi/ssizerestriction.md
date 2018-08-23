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
ms.openlocfilehash: 990fe49d39a73c5bf80b9fdda96d2e5997869edf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595420"
---
# <a name="ssizerestriction"></a><span data-ttu-id="834c5-103">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="834c5-103">SSizeRestriction</span></span>

  
  
<span data-ttu-id="834c5-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="834c5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="834c5-105">プロパティの値のサイズをテストするために使用するサイズの制限について説明します。</span><span class="sxs-lookup"><span data-stu-id="834c5-105">Describes a size restriction which is used to test the size of a property value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="834c5-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="834c5-106">Header file:</span></span>  <br/> |<span data-ttu-id="834c5-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="834c5-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSizeRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  ULONG cb;
} SSizeRestriction;

```

## <a name="members"></a><span data-ttu-id="834c5-108">Members</span><span class="sxs-lookup"><span data-stu-id="834c5-108">Members</span></span>

 <span data-ttu-id="834c5-109">**relop**</span><span class="sxs-lookup"><span data-stu-id="834c5-109">**relop**</span></span>
  
> <span data-ttu-id="834c5-110">サイズの比較で使用される関係演算子です。</span><span class="sxs-lookup"><span data-stu-id="834c5-110">Relational operator that is used in the size comparison.</span></span> <span data-ttu-id="834c5-111">使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="834c5-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="834c5-112">RELOP_GE</span><span class="sxs-lookup"><span data-stu-id="834c5-112">RELOP_GE</span></span> 
  
> <span data-ttu-id="834c5-113">比較は以上の最初の値に基づいて作成されます。</span><span class="sxs-lookup"><span data-stu-id="834c5-113">The comparison is made based on a greater or equal first value.</span></span>
    
<span data-ttu-id="834c5-114">RELOP_GT</span><span class="sxs-lookup"><span data-stu-id="834c5-114">RELOP_GT</span></span> 
  
> <span data-ttu-id="834c5-115">比較は、最初の値が大きい値に基づいて作成されます。</span><span class="sxs-lookup"><span data-stu-id="834c5-115">The comparison is made based on a greater first value.</span></span>
    
<span data-ttu-id="834c5-116">RELOP_LE</span><span class="sxs-lookup"><span data-stu-id="834c5-116">RELOP_LE</span></span> 
  
> <span data-ttu-id="834c5-117">比較は同等またはそれ以下の最初の値に基づいて作成されます。</span><span class="sxs-lookup"><span data-stu-id="834c5-117">The comparison is made based on a lesser or equal first value.</span></span>
    
<span data-ttu-id="834c5-118">RELOP_LT</span><span class="sxs-lookup"><span data-stu-id="834c5-118">RELOP_LT</span></span> 
  
> <span data-ttu-id="834c5-119">比較は、最初の小さい方の値に基づいて作成されます。</span><span class="sxs-lookup"><span data-stu-id="834c5-119">The comparison is made based on a lesser first value.</span></span>
    
<span data-ttu-id="834c5-120">RELOP_NE</span><span class="sxs-lookup"><span data-stu-id="834c5-120">RELOP_NE</span></span> 
  
> <span data-ttu-id="834c5-121">比較は、等しくない値に基づいて作成されます。</span><span class="sxs-lookup"><span data-stu-id="834c5-121">The comparison is made based on unequal values.</span></span>
    
<span data-ttu-id="834c5-122">RELOP_RE</span><span class="sxs-lookup"><span data-stu-id="834c5-122">RELOP_RE</span></span> 
  
> <span data-ttu-id="834c5-123">(正規表現) の値と同じようにに基づいて比較が行われます。</span><span class="sxs-lookup"><span data-stu-id="834c5-123">The comparison is made based on LIKE (regular expression) values.</span></span>
    
<span data-ttu-id="834c5-124">RELOP_EQ</span><span class="sxs-lookup"><span data-stu-id="834c5-124">RELOP_EQ</span></span> 
  
> <span data-ttu-id="834c5-125">比較は同等の値に基づいて作成されます。</span><span class="sxs-lookup"><span data-stu-id="834c5-125">The comparison is made based on equal values.</span></span>
    
 <span data-ttu-id="834c5-126">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="834c5-126">**ulPropTag**</span></span>
  
> <span data-ttu-id="834c5-127">プロパティ タグをテストするプロパティを識別します。</span><span class="sxs-lookup"><span data-stu-id="834c5-127">Property tag identifying the property to test.</span></span>
    
 <span data-ttu-id="834c5-128">**cb**</span><span class="sxs-lookup"><span data-stu-id="834c5-128">**cb**</span></span>
  
> <span data-ttu-id="834c5-129">プロパティの値のバイト数をカウントします。</span><span class="sxs-lookup"><span data-stu-id="834c5-129">Count of bytes in the property value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="834c5-130">注釈</span><span class="sxs-lookup"><span data-stu-id="834c5-130">Remarks</span></span>

<span data-ttu-id="834c5-131">制限のしくみの概要については、[制限の詳細](about-restrictions.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="834c5-131">For a general discussion of how restrictions work, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="834c5-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="834c5-132">See also</span></span>



[<span data-ttu-id="834c5-133">SRestriction</span><span class="sxs-lookup"><span data-stu-id="834c5-133">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="834c5-134">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="834c5-134">MAPI Structures</span></span>](mapi-structures.md)

