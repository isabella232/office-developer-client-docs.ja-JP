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
# <a name="scomparepropsrestriction"></a><span data-ttu-id="b9af2-103">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="b9af2-103">SComparePropsRestriction</span></span>

<span data-ttu-id="b9af2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b9af2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b9af2-105">リレーションシップ演算子を使用して2つのプロパティをテストする compare プロパティ制限について説明します。</span><span class="sxs-lookup"><span data-stu-id="b9af2-105">Describes a compare property restriction, which tests two properties using a relational operator.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b9af2-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="b9af2-106">Header file:</span></span>  <br/> |<span data-ttu-id="b9af2-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b9af2-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SComparePropsRestriction
{
  ULONG relop;
  ULONG ulPropTag1;
  ULONG ulPropTag2;
} SComparePropsRestriction;

```

## <a name="members"></a><span data-ttu-id="b9af2-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="b9af2-108">Members</span></span>

<span data-ttu-id="b9af2-109">**relop**</span><span class="sxs-lookup"><span data-stu-id="b9af2-109">**relop**</span></span>
  
> <span data-ttu-id="b9af2-110">2つのプロパティを比較するために使用するリレーショナル演算子です。</span><span class="sxs-lookup"><span data-stu-id="b9af2-110">Relational operator to use to compare the two properties.</span></span> <span data-ttu-id="b9af2-111">可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="b9af2-111">Possible values are as follows:</span></span>
    
  - <span data-ttu-id="b9af2-112">RELOP_GE: 比較は、最初の値よりも大きくなるか等しいかに基づいて行われます。</span><span class="sxs-lookup"><span data-stu-id="b9af2-112">RELOP_GE: The comparison is made based on a greater or equal first value.</span></span>
      
  - <span data-ttu-id="b9af2-113">RELOP_GT: 比較は、より大きな最初の値に基づいて行われます。</span><span class="sxs-lookup"><span data-stu-id="b9af2-113">RELOP_GT: The comparison is made based on a greater first value.</span></span>
      
  - <span data-ttu-id="b9af2-114">RELOP_LE: 比較は、最初の値よりも小さいか等しいかに基づいて行われます。</span><span class="sxs-lookup"><span data-stu-id="b9af2-114">RELOP_LE: The comparison is made based on a lesser or equal first value.</span></span>
      
  - <span data-ttu-id="b9af2-115">RELOP_LT: 比較は、小さい方の値に基づいて行われます。</span><span class="sxs-lookup"><span data-stu-id="b9af2-115">RELOP_LT: The comparison is made based on a lesser first value.</span></span>
      
  - <span data-ttu-id="b9af2-116">RELOP_NE: 比較は、等しくない値に基づいて行われます。</span><span class="sxs-lookup"><span data-stu-id="b9af2-116">RELOP_NE: The comparison is made based on unequal values.</span></span>
      
  - <span data-ttu-id="b9af2-117">RELOP_RE: 比較は、LIKE (正規表現) の値に基づいて行われます。</span><span class="sxs-lookup"><span data-stu-id="b9af2-117">RELOP_RE: The comparison is made based on LIKE (regular expression) values.</span></span>
      
  - <span data-ttu-id="b9af2-118">RELOP_EQ: 比較は同じ値に基づいて行われます。</span><span class="sxs-lookup"><span data-stu-id="b9af2-118">RELOP_EQ: The comparison is made based on equal values.</span></span>
    
<span data-ttu-id="b9af2-119">**ulPropTag1**</span><span class="sxs-lookup"><span data-stu-id="b9af2-119">**ulPropTag1**</span></span>
  
> <span data-ttu-id="b9af2-120">比較する最初のプロパティのプロパティタグ。</span><span class="sxs-lookup"><span data-stu-id="b9af2-120">Property tag of the first property to be compared.</span></span> 
    
<span data-ttu-id="b9af2-121">**ulPropTag2**</span><span class="sxs-lookup"><span data-stu-id="b9af2-121">**ulPropTag2**</span></span>
  
> <span data-ttu-id="b9af2-122">比較する2番目のプロパティのプロパティタグ。</span><span class="sxs-lookup"><span data-stu-id="b9af2-122">Property tag of the second property to be compared.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b9af2-123">注釈</span><span class="sxs-lookup"><span data-stu-id="b9af2-123">Remarks</span></span>

<span data-ttu-id="b9af2-124">比較順序は _(プロパティタグ 1) (リレーショナル演算子) (プロパティタグ 2)_ です。</span><span class="sxs-lookup"><span data-stu-id="b9af2-124">The comparison order is  _(property tag 1) (relational operator) (property tag 2)_.</span></span> <span data-ttu-id="b9af2-125">比較するプロパティは同じ型でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="b9af2-125">The properties to be compared must be of the same type.</span></span> <span data-ttu-id="b9af2-126">さまざまな種類のプロパティを比較しようとすると、MAPI またはサービスプロバイダーは、構造体がパラメーターとして渡される[IMAPITable](imapitableiunknown.md)メソッドからエラー値 MAPI_E_TOO_COMPLEX を返します。</span><span class="sxs-lookup"><span data-stu-id="b9af2-126">Attempting to compare properties of different types causes MAPI or the service provider to return the error value MAPI_E_TOO_COMPLEX from the [IMAPITable](imapitableiunknown.md) method to which the structure is passed as a parameter.</span></span> 
  
<span data-ttu-id="b9af2-127">プロパティの一方または両方が存在しない場合、比較プロパティ値の制限の結果は未定義です。</span><span class="sxs-lookup"><span data-stu-id="b9af2-127">The result of a compare property value restriction is undefined when one or both of the properties do not exist.</span></span> <span data-ttu-id="b9af2-128">クライアントでこのような制限に対して適切に定義された動作が必要であり、プロパティが存在するかどうかがわからない (たとえば、テーブルの必須の列\*\*\*\* ではない) 場合は、compare プロパティ制限を既存の値で結合するための制限を作成する必要があります。条件.</span><span class="sxs-lookup"><span data-stu-id="b9af2-128">When a client requires well-defined behavior for such a restriction and is not sure whether the property exists, (for example, it is not a required column of a table) it should create an **AND** restriction to join the compare property restriction with an exist restriction.</span></span> <span data-ttu-id="b9af2-129">[sexistrestriction](sexistrestriction.md)構造を使用して、**と**制限を定義するための、存在制限と[SAndRestriction](sandrestriction.md)構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="b9af2-129">Use an [SExistRestriction](sexistrestriction.md) structure to define the exist restriction and an [SAndRestriction](sandrestriction.md) structure to define the **AND** restriction.</span></span> 
  
<span data-ttu-id="b9af2-130">サービスプロバイダーがサポートしている場合、 **ulPropTag1**メンバーと**ulPropTag2**メンバーで指定されたプロパティは複数値になることができます。</span><span class="sxs-lookup"><span data-stu-id="b9af2-130">The properties specified in the **ulPropTag1** and **ulPropTag2** members can be multi-valued if the service provider supports it.</span></span> 
  
<span data-ttu-id="b9af2-131">**scomparepropsrestriction**構造と一般的な制限事項の詳細については、「[制限につい](about-restrictions.md)て」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b9af2-131">For more information about the **SComparePropsRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b9af2-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="b9af2-132">See also</span></span>

- [<span data-ttu-id="b9af2-133">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="b9af2-133">SBitMaskRestriction</span></span>](sbitmaskrestriction.md)
- [<span data-ttu-id="b9af2-134">SRestriction</span><span class="sxs-lookup"><span data-stu-id="b9af2-134">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="b9af2-135">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="b9af2-135">MAPI Structures</span></span>](mapi-structures.md)

