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
# <a name="spropertyrestriction"></a><span data-ttu-id="71165-103">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="71165-103">SPropertyRestriction</span></span>

<span data-ttu-id="71165-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="71165-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="71165-105">定数とプロパティの値を一致するために使用されるプロパティ制限について説明します。</span><span class="sxs-lookup"><span data-stu-id="71165-105">Describes a property restriction that is used to match a constant with the value of a property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="71165-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="71165-106">Header file:</span></span>  <br/> |<span data-ttu-id="71165-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="71165-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SPropertyRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  LPSPropValue lpProp;
} SPropertyRestriction;

```

## <a name="members"></a><span data-ttu-id="71165-108">Members</span><span class="sxs-lookup"><span data-stu-id="71165-108">Members</span></span>

<span data-ttu-id="71165-109">**relop**</span><span class="sxs-lookup"><span data-stu-id="71165-109">**relop**</span></span>
  
> <span data-ttu-id="71165-110">検索で使用される関係演算子。</span><span class="sxs-lookup"><span data-stu-id="71165-110">Relational operator that will be used in the search.</span></span> <span data-ttu-id="71165-111">指定できる値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="71165-111">Possible values are as follows:</span></span>
    
  - <span data-ttu-id="71165-112">RELOP_GE: 比較は、大きいまたは等しい最初の値に基づいて行います。</span><span class="sxs-lookup"><span data-stu-id="71165-112">RELOP_GE: The comparison is made based on a greater or equal first value.</span></span>
        
  - <span data-ttu-id="71165-113">RELOP_GT: 比較は、より大きい最初の値に基づいて行います。</span><span class="sxs-lookup"><span data-stu-id="71165-113">RELOP_GT: The comparison is made based on a greater first value.</span></span>
        
  - <span data-ttu-id="71165-114">RELOP_LE: 比較は、より小さいか等しい最初の値に基づいて行います。</span><span class="sxs-lookup"><span data-stu-id="71165-114">RELOP_LE: The comparison is made based on a lesser or equal first value.</span></span>
        
  - <span data-ttu-id="71165-115">RELOP_LT: 比較は、より小さい最初の値に基づいて行います。</span><span class="sxs-lookup"><span data-stu-id="71165-115">RELOP_LT: The comparison is made based on a lesser first value.</span></span>
        
  - <span data-ttu-id="71165-116">RELOP_NE: 比較は、等しくない値に基づいて行います。</span><span class="sxs-lookup"><span data-stu-id="71165-116">RELOP_NE: The comparison is made based on unequal values.</span></span>
        
  - <span data-ttu-id="71165-117">RELOP_RE: 比較は LIKE (正規表現) の値に基づいて行います。</span><span class="sxs-lookup"><span data-stu-id="71165-117">RELOP_RE: The comparison is made based on LIKE (regular expression) values.</span></span>
        
  - <span data-ttu-id="71165-118">RELOP_EQ: 比較は、等しい値に基づいて行います。</span><span class="sxs-lookup"><span data-stu-id="71165-118">RELOP_EQ: The comparison is made based on equal values.</span></span>
    
<span data-ttu-id="71165-119">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="71165-119">**ulPropTag**</span></span>
  
> <span data-ttu-id="71165-120">比較するプロパティを識別するプロパティ タグ。</span><span class="sxs-lookup"><span data-stu-id="71165-120">Property tag identifying the property to be compared.</span></span> 
    
<span data-ttu-id="71165-121">**lpProp**</span><span class="sxs-lookup"><span data-stu-id="71165-121">**lpProp**</span></span>
  
> <span data-ttu-id="71165-122">比較で使用される定数値を含む [SPropValue](spropvalue.md) 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="71165-122">Pointer to an [SPropValue](spropvalue.md) structure that contains the constant value that will be used in the comparison.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="71165-123">注釈</span><span class="sxs-lookup"><span data-stu-id="71165-123">Remarks</span></span>

<span data-ttu-id="71165-124">**SPropertyRestriction** 構造体には 2 つのプロパティ タグがあります。</span><span class="sxs-lookup"><span data-stu-id="71165-124">There are two property tags in an **SPropertyRestriction** structure.</span></span> <span data-ttu-id="71165-125">1 つは **ulPropTag** メンバーに、もう 1 つは lpProp によって指される **SPropValue 構造体の ulPropTag** メンバー **に含されます**。 </span><span class="sxs-lookup"><span data-stu-id="71165-125">One is in the **ulPropTag** member and the other is in the **ulPropTag** member of the **SPropValue** structure pointed to by **lpProp**.</span></span> <span data-ttu-id="71165-126">MAPI には、プロパティ識別子フィールドとプロパティの種類フィールドの両方が必要です。</span><span class="sxs-lookup"><span data-stu-id="71165-126">MAPI requires both the property identifier field and the property type field.</span></span> <span data-ttu-id="71165-127">**SPropertyRestriction の ulPropTag** は一致するプロパティであり **、SPropertyRestriction** の **lpProp** ポインターは **、lpProp** union のメンバー値の解釈方法を示します。   </span><span class="sxs-lookup"><span data-stu-id="71165-127">The **ulPropTag** in **SPropertyRestriction** is the property to be matched, and the **lpProp** pointer of the **SPropertyRestriction** to the **ulPropTag**'s type of the **SPropValue** indicates how the members value of the **lpProp** union are interpreted.</span></span> <span data-ttu-id="71165-128">2 つのプロパティの種類が一致する必要があります。それ以外の場合は [、IMAPITable::Restrict](imapitable-restrict.md) または [IMAPITable::FindRow](imapitable-findrow.md)の呼び出しで制限が使用される場合、エラー値 MAPI_E_TOO_COMPLEX が返されます。</span><span class="sxs-lookup"><span data-stu-id="71165-128">The two property types must match, or else the error value MAPI_E_TOO_COMPLEX is returned when the restriction is used in a call to [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> 
  
<span data-ttu-id="71165-129">比較順序は  _(プロパティ値) (関係演算子) (定数値) です_。</span><span class="sxs-lookup"><span data-stu-id="71165-129">The comparison order is  _(property value) (relational operator) (constant value)_.</span></span>
  
<span data-ttu-id="71165-130">プロパティ制限が **IMAPITable::Restrict** または **IMAPITable::FindRow** に渡され、ターゲット プロパティが存在しない場合、制限の結果は未定義になります。</span><span class="sxs-lookup"><span data-stu-id="71165-130">When a property restriction is passed to **IMAPITable::Restrict** or **IMAPITable::FindRow** and the target property does not exist, the results of the restriction are undefined.</span></span> <span data-ttu-id="71165-131">プロパティ制限と EXIST 制限を結合する **AND** 制限を作成することで、呼び出し元は正確な結果を保証できます。</span><span class="sxs-lookup"><span data-stu-id="71165-131">By creating an **AND** restriction that joins the property restriction with an **EXIST** restriction, a caller can be guaranteed accurate results.</span></span> <span data-ttu-id="71165-132">[SExistRestriction](sexistrestriction.md)構造体を使用して **、EXIST** 制限と [SAndRestriction](sandrestriction.md)構造体を定義して AND 制限 **を定義** します。</span><span class="sxs-lookup"><span data-stu-id="71165-132">Use an [SExistRestriction](sexistrestriction.md) structure to define the **EXIST** restriction and an [SAndRestriction](sandrestriction.md) structure to define the **AND** restriction.</span></span> 
  
<span data-ttu-id="71165-133">複数値のプロパティ タグは、テーブルを実装するサービス プロバイダーがそれらをサポートしている場合、プロパティ制限で使用できます。</span><span class="sxs-lookup"><span data-stu-id="71165-133">Multi-valued property tags can be used in property restrictions if the service provider implementing the table supports them.</span></span> <span data-ttu-id="71165-134">サポートされている場合、複数値プロパティ タグは、単一値プロパティ タグを使用できる任意の場所で使用できます。</span><span class="sxs-lookup"><span data-stu-id="71165-134">If supported, multi-valued property tags can be used anywhere single-valued property tags can be used.</span></span> 
  
<span data-ttu-id="71165-135">複数値のプロパティ タグは、次のメソッドで使用できます。</span><span class="sxs-lookup"><span data-stu-id="71165-135">Multi-valued property tags can be used in the following methods:</span></span>
  
- [<span data-ttu-id="71165-136">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="71165-136">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
- [<span data-ttu-id="71165-137">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="71165-137">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
    
- [<span data-ttu-id="71165-138">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="71165-138">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
    
- [<span data-ttu-id="71165-139">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="71165-139">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
- [<span data-ttu-id="71165-140">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="71165-140">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
    
> [!IMPORTANT]
> <span data-ttu-id="71165-141">2 つのプロパティ タグが一致しない場合の大きなケースは、複数値のプロパティを制限する場合です。</span><span class="sxs-lookup"><span data-stu-id="71165-141">A notable case when the two property tags won't match is if restricting on a multi-value property.</span></span> <span data-ttu-id="71165-142">この場合、次の値を true に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="71165-142">In this case the following must be true.</span></span> <span data-ttu-id="71165-143">> **SPropertyRestriction** の **ulPropTag** のプロパティ型に複数値プロパティ型ビット フラグ MV_FLAG (0x1000) が含まれている場合 **、SPropValue** の **ulPropTag** のプロパティ型は、前者から MV_FLAG ビット フラグを差し引いたもの、つまり逆になります。</span><span class="sxs-lookup"><span data-stu-id="71165-143">> If the property type of the **ulPropTag** of **SPropertyRestriction** contains the multi-value property type bit flag MV_FLAG (0x1000), the property type of the **ulPropTag** of **SPropValue** should match the former minus the MV_FLAG bit flag, that is, its inverse.</span></span> <span data-ttu-id="71165-144">> たとえば、プロパティ 0x8012101f のプロパティ タグを持つカテゴリ 、つまり PROP_TAG(MV_FLAG|PT_UNICODE, 0x8012) などの複数値のカスタム文字列プロパティの使用を制限するには、対応する **SPropertyRestriction** が次のように表示されます。</span><span class="sxs-lookup"><span data-stu-id="71165-144">> For example, to restrict using a multi-value custom string property such as a category with a property tag for the property 0x8012101f, that is, PROP_TAG(MV_FLAG|PT_UNICODE, 0x8012)), the corresponding **SPropertyRestriction** would appear as follows.</span></span><span data-ttu-id="71165-145"> >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";`> **SPropValue** の **ulPropTag** のプロパティの種類に MV_FLAG ビット フラグが含まれている場合、返される可能性が高MAPI_E_TOO_COMPLEX。</span><span class="sxs-lookup"><span data-stu-id="71165-145"> >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";`> Note that if the property type of the **ulPropTag** of **SPropValue** contains the MV_FLAG bit flag, the likely return is MAPI_E_TOO_COMPLEX.</span></span> 
  
<span data-ttu-id="71165-146">**SPropertyRestriction** 構造の詳細については、「制限について [」を参照してください](about-restrictions.md)。</span><span class="sxs-lookup"><span data-stu-id="71165-146">For more information about the **SPropertyRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="71165-147">関連項目</span><span class="sxs-lookup"><span data-stu-id="71165-147">See also</span></span>

- [<span data-ttu-id="71165-148">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="71165-148">SExistRestriction</span></span>](sexistrestriction.md)
- [<span data-ttu-id="71165-149">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="71165-149">SAndRestriction</span></span>](sandrestriction.md)
- [<span data-ttu-id="71165-150">SPropValue</span><span class="sxs-lookup"><span data-stu-id="71165-150">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="71165-151">SRestriction</span><span class="sxs-lookup"><span data-stu-id="71165-151">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="71165-152">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="71165-152">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
- [<span data-ttu-id="71165-153">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="71165-153">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
- [<span data-ttu-id="71165-154">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="71165-154">MAPI Structures</span></span>](mapi-structures.md)

