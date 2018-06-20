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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 134eb844ef7b72d396c300b27a87a3a7ae320cf1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804012"
---
# <a name="ssizerestriction"></a><span data-ttu-id="25f83-103">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="25f83-103">SSizeRestriction</span></span>

  
  
<span data-ttu-id="25f83-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="25f83-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="25f83-105">プロパティの値のサイズをテストするために使用するサイズの制限について説明します。</span><span class="sxs-lookup"><span data-stu-id="25f83-105">Describes a size restriction which is used to test the size of a property value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="25f83-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="25f83-106">Header file:</span></span>  <br/> |<span data-ttu-id="25f83-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="25f83-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSizeRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  ULONG cb;
} SSizeRestriction;

```

## <a name="members"></a><span data-ttu-id="25f83-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="25f83-108">Members</span></span>

 <span data-ttu-id="25f83-109">**relop**</span><span class="sxs-lookup"><span data-stu-id="25f83-109">**relop**</span></span>
  
> <span data-ttu-id="25f83-110">サイズの比較で使用される関係演算子です。</span><span class="sxs-lookup"><span data-stu-id="25f83-110">Relational operator that is used in the size comparison.</span></span> <span data-ttu-id="25f83-111">使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="25f83-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="25f83-112">RELOP_GE</span><span class="sxs-lookup"><span data-stu-id="25f83-112">RELOP_GE</span></span> 
  
> <span data-ttu-id="25f83-113">比較は以上の最初の値に基づいて作成されます。</span><span class="sxs-lookup"><span data-stu-id="25f83-113">The comparison is made based on a greater or equal first value.</span></span>
    
<span data-ttu-id="25f83-114">RELOP_GT</span><span class="sxs-lookup"><span data-stu-id="25f83-114">RELOP_GT</span></span> 
  
> <span data-ttu-id="25f83-115">比較は、最初の値が大きい値に基づいて作成されます。</span><span class="sxs-lookup"><span data-stu-id="25f83-115">The comparison is made based on a greater first value.</span></span>
    
<span data-ttu-id="25f83-116">RELOP_LE</span><span class="sxs-lookup"><span data-stu-id="25f83-116">RELOP_LE</span></span> 
  
> <span data-ttu-id="25f83-117">比較は同等またはそれ以下の最初の値に基づいて作成されます。</span><span class="sxs-lookup"><span data-stu-id="25f83-117">The comparison is made based on a lesser or equal first value.</span></span>
    
<span data-ttu-id="25f83-118">RELOP_LT</span><span class="sxs-lookup"><span data-stu-id="25f83-118">RELOP_LT</span></span> 
  
> <span data-ttu-id="25f83-119">比較は、最初の小さい方の値に基づいて作成されます。</span><span class="sxs-lookup"><span data-stu-id="25f83-119">The comparison is made based on a lesser first value.</span></span>
    
<span data-ttu-id="25f83-120">RELOP_NE</span><span class="sxs-lookup"><span data-stu-id="25f83-120">RELOP_NE</span></span> 
  
> <span data-ttu-id="25f83-121">比較は、等しくない値に基づいて作成されます。</span><span class="sxs-lookup"><span data-stu-id="25f83-121">The comparison is made based on unequal values.</span></span>
    
<span data-ttu-id="25f83-122">RELOP_RE</span><span class="sxs-lookup"><span data-stu-id="25f83-122">RELOP_RE</span></span> 
  
> <span data-ttu-id="25f83-123">(正規表現) の値と同じようにに基づいて比較が行われます。</span><span class="sxs-lookup"><span data-stu-id="25f83-123">The comparison is made based on LIKE (regular expression) values.</span></span>
    
<span data-ttu-id="25f83-124">RELOP_EQ</span><span class="sxs-lookup"><span data-stu-id="25f83-124">RELOP_EQ</span></span> 
  
> <span data-ttu-id="25f83-125">比較は同等の値に基づいて作成されます。</span><span class="sxs-lookup"><span data-stu-id="25f83-125">The comparison is made based on equal values.</span></span>
    
 <span data-ttu-id="25f83-126">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="25f83-126">**ulPropTag**</span></span>
  
> <span data-ttu-id="25f83-127">プロパティ タグをテストするプロパティを識別します。</span><span class="sxs-lookup"><span data-stu-id="25f83-127">Property tag identifying the property to test.</span></span>
    
 <span data-ttu-id="25f83-128">**cb**</span><span class="sxs-lookup"><span data-stu-id="25f83-128">**cb**</span></span>
  
> <span data-ttu-id="25f83-129">プロパティの値のバイト数をカウントします。</span><span class="sxs-lookup"><span data-stu-id="25f83-129">Count of bytes in the property value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="25f83-130">備考</span><span class="sxs-lookup"><span data-stu-id="25f83-130">Remarks</span></span>

<span data-ttu-id="25f83-131">制限のしくみの概要については、[制限の詳細](about-restrictions.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="25f83-131">For a general discussion of how restrictions work, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="25f83-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="25f83-132">See also</span></span>



[<span data-ttu-id="25f83-133">SRestriction</span><span class="sxs-lookup"><span data-stu-id="25f83-133">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="25f83-134">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="25f83-134">MAPI Structures</span></span>](mapi-structures.md)

