---
title: SPropertyRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropertyRestriction
api_type:
- COM
ms.assetid: 2bbf13e9-05b3-4498-8e08-d9e07505190d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 29d392eba530126e06a672c10044c5b4df0618c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406088"
---
# <a name="spropertyrestriction"></a><span data-ttu-id="42e90-103">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="42e90-103">SPropertyRestriction</span></span>

<span data-ttu-id="42e90-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="42e90-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="42e90-105">定数をプロパティの値と照合するために使用されるプロパティ制限を記述します。</span><span class="sxs-lookup"><span data-stu-id="42e90-105">Describes a property restriction that is used to match a constant with the value of a property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="42e90-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="42e90-106">Header file:</span></span>  <br/> |<span data-ttu-id="42e90-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="42e90-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SPropertyRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  LPSPropValue lpProp;
} SPropertyRestriction;

```

## <a name="members"></a><span data-ttu-id="42e90-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="42e90-108">Members</span></span>

<span data-ttu-id="42e90-109">**relop**</span><span class="sxs-lookup"><span data-stu-id="42e90-109">**relop**</span></span>
  
> <span data-ttu-id="42e90-110">検索で使用される関係演算子です。</span><span class="sxs-lookup"><span data-stu-id="42e90-110">Relational operator that will be used in the search.</span></span> <span data-ttu-id="42e90-111">可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="42e90-111">Possible values are as follows:</span></span>
    
  - <span data-ttu-id="42e90-112">RELOP_GE: 比較は、最初の値よりも大きくなるか等しいかに基づいて行われます。</span><span class="sxs-lookup"><span data-stu-id="42e90-112">RELOP_GE: The comparison is made based on a greater or equal first value.</span></span>
        
  - <span data-ttu-id="42e90-113">RELOP_GT: 比較は、より大きな最初の値に基づいて行われます。</span><span class="sxs-lookup"><span data-stu-id="42e90-113">RELOP_GT: The comparison is made based on a greater first value.</span></span>
        
  - <span data-ttu-id="42e90-114">RELOP_LE: 比較は、最初の値よりも小さいか等しいかに基づいて行われます。</span><span class="sxs-lookup"><span data-stu-id="42e90-114">RELOP_LE: The comparison is made based on a lesser or equal first value.</span></span>
        
  - <span data-ttu-id="42e90-115">RELOP_LT: 比較は、小さい方の値に基づいて行われます。</span><span class="sxs-lookup"><span data-stu-id="42e90-115">RELOP_LT: The comparison is made based on a lesser first value.</span></span>
        
  - <span data-ttu-id="42e90-116">RELOP_NE: 比較は、等しくない値に基づいて行われます。</span><span class="sxs-lookup"><span data-stu-id="42e90-116">RELOP_NE: The comparison is made based on unequal values.</span></span>
        
  - <span data-ttu-id="42e90-117">RELOP_RE: 比較は、LIKE (正規表現) の値に基づいて行われます。</span><span class="sxs-lookup"><span data-stu-id="42e90-117">RELOP_RE: The comparison is made based on LIKE (regular expression) values.</span></span>
        
  - <span data-ttu-id="42e90-118">RELOP_EQ: 比較は同じ値に基づいて行われます。</span><span class="sxs-lookup"><span data-stu-id="42e90-118">RELOP_EQ: The comparison is made based on equal values.</span></span>
    
<span data-ttu-id="42e90-119">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="42e90-119">**ulPropTag**</span></span>
  
> <span data-ttu-id="42e90-120">比較するプロパティを識別するプロパティタグ。</span><span class="sxs-lookup"><span data-stu-id="42e90-120">Property tag identifying the property to be compared.</span></span> 
    
<span data-ttu-id="42e90-121">**lpprop**</span><span class="sxs-lookup"><span data-stu-id="42e90-121">**lpProp**</span></span>
  
> <span data-ttu-id="42e90-122">比較で使用される定数値を含む[spropvalue](spropvalue.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="42e90-122">Pointer to an [SPropValue](spropvalue.md) structure that contains the constant value that will be used in the comparison.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="42e90-123">注釈</span><span class="sxs-lookup"><span data-stu-id="42e90-123">Remarks</span></span>

<span data-ttu-id="42e90-124">**spropertyrestriction**構造には、2つのプロパティタグがあります。</span><span class="sxs-lookup"><span data-stu-id="42e90-124">There are two property tags in an **SPropertyRestriction** structure.</span></span> <span data-ttu-id="42e90-125">一方は**ulPropTag**メンバーで、もう1つは**lpprop**でポイントされた**spropvalue**構造の**ulPropTag**メンバーにあります。</span><span class="sxs-lookup"><span data-stu-id="42e90-125">One is in the **ulPropTag** member and the other is in the **ulPropTag** member of the **SPropValue** structure pointed to by **lpProp**.</span></span> <span data-ttu-id="42e90-126">MAPI には、[プロパティ識別子] フィールドと [プロパティの種類] フィールドの両方が必要です。</span><span class="sxs-lookup"><span data-stu-id="42e90-126">MAPI requires both the property identifier field and the property type field.</span></span> <span data-ttu-id="42e90-127">**spropertyrestriction**の**ulPropTag**は一致するプロパティを示し、 **spropertyrestriction**の**ulPropTag**の種類に対する**spropertyrestriction**の**lpprop**ポインターは、のメンバーの値がどのように表示されるかを示しています。**lpprop**ユニオンが解釈されます。</span><span class="sxs-lookup"><span data-stu-id="42e90-127">The **ulPropTag** in **SPropertyRestriction** is the property to be matched, and the **lpProp** pointer of the **SPropertyRestriction** to the **ulPropTag**'s type of the **SPropValue** indicates how the members value of the **lpProp** union are interpreted.</span></span> <span data-ttu-id="42e90-128">2つのプロパティの型は一致している必要があります。または、制限が[imapitable:: Restrict](imapitable-restrict.md)または[imapitable:: FindRow](imapitable-findrow.md)の呼び出しで使用されている場合、エラー値 MAPI_E_TOO_COMPLEX が返されます。</span><span class="sxs-lookup"><span data-stu-id="42e90-128">The two property types must match, or else the error value MAPI_E_TOO_COMPLEX is returned when the restriction is used in a call to [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> 
  
<span data-ttu-id="42e90-129">比較順序は、 _(プロパティ値) (リレーショナル演算子) (定数値_) です。</span><span class="sxs-lookup"><span data-stu-id="42e90-129">The comparison order is  _(property value) (relational operator) (constant value)_.</span></span>
  
<span data-ttu-id="42e90-130">プロパティ制限が**IMAPITable:: Restrict**または**imapitable:: FindRow**に渡され、target プロパティが存在しない場合、制限の結果は未定義となります。</span><span class="sxs-lookup"><span data-stu-id="42e90-130">When a property restriction is passed to **IMAPITable::Restrict** or **IMAPITable::FindRow** and the target property does not exist, the results of the restriction are undefined.</span></span> <span data-ttu-id="42e90-131">プロパティ制限に参加する**と**制限が存在し、制限が**存在**することにより、発信者が正確な結果を保証できます。</span><span class="sxs-lookup"><span data-stu-id="42e90-131">By creating an **AND** restriction that joins the property restriction with an **EXIST** restriction, a caller can be guaranteed accurate results.</span></span> <span data-ttu-id="42e90-132">[sexistrestriction](sexistrestriction.md)構造を使用して、**と**制限を定義するための、**存在**制限と[SAndRestriction](sandrestriction.md)構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="42e90-132">Use an [SExistRestriction](sexistrestriction.md) structure to define the **EXIST** restriction and an [SAndRestriction](sandrestriction.md) structure to define the **AND** restriction.</span></span> 
  
<span data-ttu-id="42e90-133">テーブルを実装しているサービスプロバイダーがそれらをサポートしている場合は、プロパティ制限で複数値プロパティタグを使用できます。</span><span class="sxs-lookup"><span data-stu-id="42e90-133">Multi-valued property tags can be used in property restrictions if the service provider implementing the table supports them.</span></span> <span data-ttu-id="42e90-134">サポートされている場合は、複数値プロパティタグを使用して、単一値のプロパティタグを任意の場所で使用できます。</span><span class="sxs-lookup"><span data-stu-id="42e90-134">If supported, multi-valued property tags can be used anywhere single-valued property tags can be used.</span></span> 
  
<span data-ttu-id="42e90-135">複数値プロパティタグは、次の方法で使用できます。</span><span class="sxs-lookup"><span data-stu-id="42e90-135">Multi-valued property tags can be used in the following methods:</span></span>
  
- [<span data-ttu-id="42e90-136">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="42e90-136">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
- [<span data-ttu-id="42e90-137">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="42e90-137">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
    
- [<span data-ttu-id="42e90-138">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="42e90-138">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
    
- [<span data-ttu-id="42e90-139">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="42e90-139">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
- [<span data-ttu-id="42e90-140">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="42e90-140">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
    
> [!IMPORTANT]
> <span data-ttu-id="42e90-141">複数値のプロパティを制限する場合は、2つのプロパティタグが一致しないようなケースがあります。</span><span class="sxs-lookup"><span data-stu-id="42e90-141">A notable case when the two property tags won't match is if restricting on a multi-value property.</span></span> <span data-ttu-id="42e90-142">この場合は、次の条件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="42e90-142">In this case the following must be true.</span></span> <span data-ttu-id="42e90-143">> **spropertyrestriction**の**ulPropTag**のプロパティの種類に、複数値のプロパティの種類のビットフラグ MV_FLAG (0x1000) が含まれている場合、 **spropertyrestriction**の**ulPropTag**のプロパティの型は、以前の MV_ を除いた値と一致する必要があります。フラグビットフラグ (逆)。</span><span class="sxs-lookup"><span data-stu-id="42e90-143">> If the property type of the **ulPropTag** of **SPropertyRestriction** contains the multi-value property type bit flag MV_FLAG (0x1000), the property type of the **ulPropTag** of **SPropValue** should match the former minus the MV_FLAG bit flag, that is, its inverse.</span></span> <span data-ttu-id="42e90-144">> たとえば、プロパティ0x8012101f のプロパティタグを持つカテゴリなど、複数値のカスタム文字列プロパティを使用するように制限するには、PROP_TAG (MV_FLAG | PT_UNICODE, 0x8012) のように、対応する**spropertyrestriction**が表示されます。示し.</span><span class="sxs-lookup"><span data-stu-id="42e90-144">> For example, to restrict using a multi-value custom string property such as a category with a property tag for the property 0x8012101f, that is, PROP_TAG(MV_FLAG|PT_UNICODE, 0x8012)), the corresponding **SPropertyRestriction** would appear as follows.</span></span><span data-ttu-id="42e90-145"> >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property\`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid\`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";\`> *\*spropvalue*\*の*\*ulPropTag*\*のプロパティの種類に MV_FLAG ビットフラグが含まれている場合は、戻り値は MAPI_E_TOO_COMPLEX になる可能性があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="42e90-145"> >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property\`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid\`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";\`> Note that if the property type of the *\*ulPropTag** of *\*SPropValue** contains the MV_FLAG bit flag, the likely return is MAPI_E_TOO_COMPLEX.</span></span> 
  
<span data-ttu-id="42e90-146">**spropertyrestriction**構造の詳細については、「[制限につい](about-restrictions.md)て」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="42e90-146">For more information about the **SPropertyRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="42e90-147">関連項目</span><span class="sxs-lookup"><span data-stu-id="42e90-147">See also</span></span>

- [<span data-ttu-id="42e90-148">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="42e90-148">SExistRestriction</span></span>](sexistrestriction.md)
- [<span data-ttu-id="42e90-149">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="42e90-149">SAndRestriction</span></span>](sandrestriction.md)
- [<span data-ttu-id="42e90-150">SPropValue</span><span class="sxs-lookup"><span data-stu-id="42e90-150">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="42e90-151">SRestriction</span><span class="sxs-lookup"><span data-stu-id="42e90-151">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="42e90-152">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="42e90-152">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
- [<span data-ttu-id="42e90-153">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="42e90-153">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
- [<span data-ttu-id="42e90-154">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="42e90-154">MAPI Structures</span></span>](mapi-structures.md)

