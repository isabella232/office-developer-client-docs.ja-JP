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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 6ebc4e9cbc79a71a91f1f2f3eec0d40de979ab18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803832"
---
# <a name="scomparepropsrestriction"></a><span data-ttu-id="19e5e-103">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="19e5e-103">SComparePropsRestriction</span></span>

<span data-ttu-id="19e5e-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="19e5e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="19e5e-105">リレーショナル演算子を使用して 2 つのプロパティをテストする比較プロパティの制限について説明します。</span><span class="sxs-lookup"><span data-stu-id="19e5e-105">Describes a compare property restriction, which tests two properties using a relational operator.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="19e5e-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="19e5e-106">Header file:</span></span>  <br/> |<span data-ttu-id="19e5e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="19e5e-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SComparePropsRestriction
{
  ULONG relop;
  ULONG ulPropTag1;
  ULONG ulPropTag2;
} SComparePropsRestriction;

```

## <a name="members"></a><span data-ttu-id="19e5e-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="19e5e-108">Members</span></span>

<span data-ttu-id="19e5e-109">**relop**</span><span class="sxs-lookup"><span data-stu-id="19e5e-109">**relop**</span></span>
  
> <span data-ttu-id="19e5e-110">2 つのプロパティを比較に使用する関係演算子です。</span><span class="sxs-lookup"><span data-stu-id="19e5e-110">Relational operator to use to compare the two properties.</span></span> <span data-ttu-id="19e5e-111">使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="19e5e-111">Possible values are as follows:</span></span>
    
  - <span data-ttu-id="19e5e-112">RELOP_GE: 比較を行うベースの最初の値が大きいか等しい。</span><span class="sxs-lookup"><span data-stu-id="19e5e-112">RELOP_GE: The comparison is made based on a greater or equal first value.</span></span>
      
  - <span data-ttu-id="19e5e-113">RELOP_GT: 比較を行うベースの最初の値が大きい。</span><span class="sxs-lookup"><span data-stu-id="19e5e-113">RELOP_GT: The comparison is made based on a greater first value.</span></span>
      
  - <span data-ttu-id="19e5e-114">RELOP_LE: 比較を行うに基づいて最初の値が同等またはそれ以下にします。</span><span class="sxs-lookup"><span data-stu-id="19e5e-114">RELOP_LE: The comparison is made based on a lesser or equal first value.</span></span>
      
  - <span data-ttu-id="19e5e-115">RELOP_LT: 比較を行うベースの最初の値が小さい方です。</span><span class="sxs-lookup"><span data-stu-id="19e5e-115">RELOP_LT: The comparison is made based on a lesser first value.</span></span>
      
  - <span data-ttu-id="19e5e-116">RELOP_NE: 比較を行うベースの値が等しくないです。</span><span class="sxs-lookup"><span data-stu-id="19e5e-116">RELOP_NE: The comparison is made based on unequal values.</span></span>
      
  - <span data-ttu-id="19e5e-117">RELOP_RE: 比較を (正規表現) の値などを基に行われます。</span><span class="sxs-lookup"><span data-stu-id="19e5e-117">RELOP_RE: The comparison is made based on LIKE (regular expression) values.</span></span>
      
  - <span data-ttu-id="19e5e-118">RELOP_EQ: 比較で行われるベースの値に等しい。</span><span class="sxs-lookup"><span data-stu-id="19e5e-118">RELOP_EQ: The comparison is made based on equal values.</span></span>
    
<span data-ttu-id="19e5e-119">**ulPropTag1**</span><span class="sxs-lookup"><span data-stu-id="19e5e-119">**ulPropTag1**</span></span>
  
> <span data-ttu-id="19e5e-120">比較する最初のプロパティのプロパティ タグです。</span><span class="sxs-lookup"><span data-stu-id="19e5e-120">Property tag of the first property to be compared.</span></span> 
    
<span data-ttu-id="19e5e-121">**ulPropTag2**</span><span class="sxs-lookup"><span data-stu-id="19e5e-121">**ulPropTag2**</span></span>
  
> <span data-ttu-id="19e5e-122">比較する 2 番目のプロパティのプロパティ タグです。</span><span class="sxs-lookup"><span data-stu-id="19e5e-122">Property tag of the second property to be compared.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="19e5e-123">備考</span><span class="sxs-lookup"><span data-stu-id="19e5e-123">Remarks</span></span>

<span data-ttu-id="19e5e-124">比較の順序は、 _(1) (関係演算子) のプロパティ タグ (プロパティ タグ 2)_。</span><span class="sxs-lookup"><span data-stu-id="19e5e-124">The comparison order is  _(property tag 1) (relational operator) (property tag 2)_.</span></span> <span data-ttu-id="19e5e-125">比較するプロパティは、同じ型でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="19e5e-125">The properties to be compared must be of the same type.</span></span> <span data-ttu-id="19e5e-126">構造体はパラメーターとして渡す[IMAPITable](imapitableiunknown.md)メソッドからエラー値 MAPI_E_TOO_COMPLEX を取得するには、MAPI またはサービス プロバイダーは、さまざまな種類のプロパティを比較しようとしています。</span><span class="sxs-lookup"><span data-stu-id="19e5e-126">Attempting to compare properties of different types causes MAPI or the service provider to return the error value MAPI_E_TOO_COMPLEX from the [IMAPITable](imapitableiunknown.md) method to which the structure is passed as a parameter.</span></span> 
  
<span data-ttu-id="19e5e-127">プロパティの一方または両方が存在しない場合、比較のプロパティ値の制限の結果は定義されていません。</span><span class="sxs-lookup"><span data-stu-id="19e5e-127">The result of a compare property value restriction is undefined when one or both of the properties do not exist.</span></span> <span data-ttu-id="19e5e-128">クライアントなどの制限について明確に定義された動作を必要とし、ないときことを確認して、プロパティが存在するかどうか (たとえばは必要なテーブルの列) と、既存の比較プロパティの制限に参加する**と**制限を作成する必要があります制限です。</span><span class="sxs-lookup"><span data-stu-id="19e5e-128">When a client requires well-defined behavior for such a restriction and is not sure whether the property exists, (for example, it is not a required column of a table) it should create an **AND** restriction to join the compare property restriction with an exist restriction.</span></span> <span data-ttu-id="19e5e-129">[SExistRestriction](sexistrestriction.md)構造体を使用すると、既存の制限、**および**制限を定義するのには、 [SAndRestriction](sandrestriction.md)構造体を定義します。</span><span class="sxs-lookup"><span data-stu-id="19e5e-129">Use an [SExistRestriction](sexistrestriction.md) structure to define the exist restriction and an [SAndRestriction](sandrestriction.md) structure to define the **AND** restriction.</span></span> 
  
<span data-ttu-id="19e5e-130">**UlPropTag1**と**ulPropTag2**のメンバーで指定されたプロパティは、サービス プロバイダーがサポートしている場合、複数値を持つことができます。</span><span class="sxs-lookup"><span data-stu-id="19e5e-130">The properties specified in the **ulPropTag1** and **ulPropTag2** members can be multi-valued if the service provider supports it.</span></span> 
  
<span data-ttu-id="19e5e-131">**SComparePropsRestriction**構造体および制限の詳細については一般に、[制限の詳細](about-restrictions.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="19e5e-131">For more information about the **SComparePropsRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="19e5e-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="19e5e-132">See also</span></span>

- [<span data-ttu-id="19e5e-133">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="19e5e-133">SBitMaskRestriction</span></span>](sbitmaskrestriction.md)
- [<span data-ttu-id="19e5e-134">SRestriction</span><span class="sxs-lookup"><span data-stu-id="19e5e-134">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="19e5e-135">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="19e5e-135">MAPI Structures</span></span>](mapi-structures.md)

