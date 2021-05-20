---
title: SComparePropsRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SComparePropsRestriction
api_type:
- COM
ms.assetid: 3231a91a-1ef2-4dd8-9f3e-79ca56d2eae9
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 513ec0db4e99e687d8aeb9e1d6acdef73df4d158
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33440004"
---
# <a name="scomparepropsrestriction"></a><span data-ttu-id="bc162-103">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="bc162-103">SComparePropsRestriction</span></span>

<span data-ttu-id="bc162-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc162-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc162-105">リレーショナル 演算子を使用して 2 つのプロパティをテストする比較プロパティ制限について説明します。</span><span class="sxs-lookup"><span data-stu-id="bc162-105">Describes a compare property restriction, which tests two properties using a relational operator.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bc162-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="bc162-106">Header file:</span></span>  <br/> |<span data-ttu-id="bc162-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bc162-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SComparePropsRestriction
{
  ULONG relop;
  ULONG ulPropTag1;
  ULONG ulPropTag2;
} SComparePropsRestriction;

```

## <a name="members"></a><span data-ttu-id="bc162-108">Members</span><span class="sxs-lookup"><span data-stu-id="bc162-108">Members</span></span>

<span data-ttu-id="bc162-109">**relop**</span><span class="sxs-lookup"><span data-stu-id="bc162-109">**relop**</span></span>
  
> <span data-ttu-id="bc162-110">2 つのプロパティを比較するために使用する関係演算子。</span><span class="sxs-lookup"><span data-stu-id="bc162-110">Relational operator to use to compare the two properties.</span></span> <span data-ttu-id="bc162-111">指定できる値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="bc162-111">Possible values are as follows:</span></span>
    
  - <span data-ttu-id="bc162-112">RELOP_GE: 比較は、大きいまたは等しい最初の値に基づいて行います。</span><span class="sxs-lookup"><span data-stu-id="bc162-112">RELOP_GE: The comparison is made based on a greater or equal first value.</span></span>
      
  - <span data-ttu-id="bc162-113">RELOP_GT: 比較は、より大きい最初の値に基づいて行います。</span><span class="sxs-lookup"><span data-stu-id="bc162-113">RELOP_GT: The comparison is made based on a greater first value.</span></span>
      
  - <span data-ttu-id="bc162-114">RELOP_LE: 比較は、より小さいか等しい最初の値に基づいて行います。</span><span class="sxs-lookup"><span data-stu-id="bc162-114">RELOP_LE: The comparison is made based on a lesser or equal first value.</span></span>
      
  - <span data-ttu-id="bc162-115">RELOP_LT: 比較は、より小さい最初の値に基づいて行います。</span><span class="sxs-lookup"><span data-stu-id="bc162-115">RELOP_LT: The comparison is made based on a lesser first value.</span></span>
      
  - <span data-ttu-id="bc162-116">RELOP_NE: 比較は、等しくない値に基づいて行います。</span><span class="sxs-lookup"><span data-stu-id="bc162-116">RELOP_NE: The comparison is made based on unequal values.</span></span>
      
  - <span data-ttu-id="bc162-117">RELOP_RE: 比較は LIKE (正規表現) の値に基づいて行います。</span><span class="sxs-lookup"><span data-stu-id="bc162-117">RELOP_RE: The comparison is made based on LIKE (regular expression) values.</span></span>
      
  - <span data-ttu-id="bc162-118">RELOP_EQ: 比較は、等しい値に基づいて行います。</span><span class="sxs-lookup"><span data-stu-id="bc162-118">RELOP_EQ: The comparison is made based on equal values.</span></span>
    
<span data-ttu-id="bc162-119">**ulPropTag1**</span><span class="sxs-lookup"><span data-stu-id="bc162-119">**ulPropTag1**</span></span>
  
> <span data-ttu-id="bc162-120">比較する最初のプロパティのプロパティ タグ。</span><span class="sxs-lookup"><span data-stu-id="bc162-120">Property tag of the first property to be compared.</span></span> 
    
<span data-ttu-id="bc162-121">**ulPropTag2**</span><span class="sxs-lookup"><span data-stu-id="bc162-121">**ulPropTag2**</span></span>
  
> <span data-ttu-id="bc162-122">比較する 2 番目のプロパティのプロパティ タグ。</span><span class="sxs-lookup"><span data-stu-id="bc162-122">Property tag of the second property to be compared.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bc162-123">注釈</span><span class="sxs-lookup"><span data-stu-id="bc162-123">Remarks</span></span>

<span data-ttu-id="bc162-124">比較順序は  _(プロパティ タグ 1) (関係演算子) (プロパティ タグ 2) です_。</span><span class="sxs-lookup"><span data-stu-id="bc162-124">The comparison order is  _(property tag 1) (relational operator) (property tag 2)_.</span></span> <span data-ttu-id="bc162-125">比較するプロパティは、同じ種類である必要があります。</span><span class="sxs-lookup"><span data-stu-id="bc162-125">The properties to be compared must be of the same type.</span></span> <span data-ttu-id="bc162-126">さまざまな種類のプロパティを比較しようとすると、MAPI またはサービス プロバイダーは、構造がパラメーターとして渡される [IMAPITable](imapitableiunknown.md) メソッドからエラー値 MAPI_E_TOO_COMPLEX を返します。</span><span class="sxs-lookup"><span data-stu-id="bc162-126">Attempting to compare properties of different types causes MAPI or the service provider to return the error value MAPI_E_TOO_COMPLEX from the [IMAPITable](imapitableiunknown.md) method to which the structure is passed as a parameter.</span></span> 
  
<span data-ttu-id="bc162-127">プロパティ値の比較の制限の結果は、プロパティの 1 つまたは両方が存在しない場合は未定義です。</span><span class="sxs-lookup"><span data-stu-id="bc162-127">The result of a compare property value restriction is undefined when one or both of the properties do not exist.</span></span> <span data-ttu-id="bc162-128">クライアントがこのような制限に対して十分に定義された動作を必要とし、プロパティが存在するかどうかが分からない場合 (たとえば、テーブルの必須の列ではありません)、比較プロパティ制限に存在する制限を結合する **AND** 制限を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bc162-128">When a client requires well-defined behavior for such a restriction and is not sure whether the property exists, (for example, it is not a required column of a table) it should create an **AND** restriction to join the compare property restriction with an exist restriction.</span></span> <span data-ttu-id="bc162-129">[SExistRestriction](sexistrestriction.md)構造体を使用して、存在制限と [SAndRestriction](sandrestriction.md)構造体を定義して AND 制限 **を定義** します。</span><span class="sxs-lookup"><span data-stu-id="bc162-129">Use an [SExistRestriction](sexistrestriction.md) structure to define the exist restriction and an [SAndRestriction](sandrestriction.md) structure to define the **AND** restriction.</span></span> 
  
<span data-ttu-id="bc162-130">ulPropTag1 および **ulPropTag2** メンバーで指定されたプロパティは、サービス プロバイダーがサポートしている場合、複数値を指定できます。 </span><span class="sxs-lookup"><span data-stu-id="bc162-130">The properties specified in the **ulPropTag1** and **ulPropTag2** members can be multi-valued if the service provider supports it.</span></span> 
  
<span data-ttu-id="bc162-131">**SComparePropsRestriction** の構造と制限全般の詳細については、「制限について」[を参照してください](about-restrictions.md)。</span><span class="sxs-lookup"><span data-stu-id="bc162-131">For more information about the **SComparePropsRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bc162-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="bc162-132">See also</span></span>

- [<span data-ttu-id="bc162-133">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="bc162-133">SBitMaskRestriction</span></span>](sbitmaskrestriction.md)
- [<span data-ttu-id="bc162-134">SRestriction</span><span class="sxs-lookup"><span data-stu-id="bc162-134">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="bc162-135">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="bc162-135">MAPI Structures</span></span>](mapi-structures.md)

