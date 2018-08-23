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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f59b0041f271010e56dda2f73d2248f133bc1325
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803978"
---
# <a name="spropertyrestriction"></a><span data-ttu-id="d0fc4-103">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="d0fc4-103">SPropertyRestriction</span></span>

<span data-ttu-id="d0fc4-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d0fc4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d0fc4-105">プロパティの値を持つ定数を一致させるために使用されるプロパティの制限について説明します。</span><span class="sxs-lookup"><span data-stu-id="d0fc4-105">Describes a property restriction that is used to match a constant with the value of a property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d0fc4-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="d0fc4-106">Header file:</span></span>  <br/> |<span data-ttu-id="d0fc4-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d0fc4-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SPropertyRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  LPSPropValue lpProp;
} SPropertyRestriction;

```

## <a name="members"></a><span data-ttu-id="d0fc4-108">Members</span><span class="sxs-lookup"><span data-stu-id="d0fc4-108">Members</span></span>

<span data-ttu-id="d0fc4-109">**relop**</span><span class="sxs-lookup"><span data-stu-id="d0fc4-109">**relop**</span></span>
  
> <span data-ttu-id="d0fc4-110">検索に使用される関係演算子です。</span><span class="sxs-lookup"><span data-stu-id="d0fc4-110">Relational operator that will be used in the search.</span></span> <span data-ttu-id="d0fc4-111">使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="d0fc4-111">Possible values are as follows:</span></span>
    
  - <span data-ttu-id="d0fc4-112">RELOP_GE: 比較を行うベースの最初の値が大きいか等しい。</span><span class="sxs-lookup"><span data-stu-id="d0fc4-112">RELOP_GE: The comparison is made based on a greater or equal first value.</span></span>
        
  - <span data-ttu-id="d0fc4-113">RELOP_GT: 比較を行うベースの最初の値が大きい。</span><span class="sxs-lookup"><span data-stu-id="d0fc4-113">RELOP_GT: The comparison is made based on a greater first value.</span></span>
        
  - <span data-ttu-id="d0fc4-114">RELOP_LE: 比較を行うに基づいて最初の値が同等またはそれ以下にします。</span><span class="sxs-lookup"><span data-stu-id="d0fc4-114">RELOP_LE: The comparison is made based on a lesser or equal first value.</span></span>
        
  - <span data-ttu-id="d0fc4-115">RELOP_LT: 比較を行うベースの最初の値が小さい方です。</span><span class="sxs-lookup"><span data-stu-id="d0fc4-115">RELOP_LT: The comparison is made based on a lesser first value.</span></span>
        
  - <span data-ttu-id="d0fc4-116">RELOP_NE: 比較を行うベースの値が等しくないです。</span><span class="sxs-lookup"><span data-stu-id="d0fc4-116">RELOP_NE: The comparison is made based on unequal values.</span></span>
        
  - <span data-ttu-id="d0fc4-117">RELOP_RE: 比較を (正規表現) の値などを基に行われます。</span><span class="sxs-lookup"><span data-stu-id="d0fc4-117">RELOP_RE: The comparison is made based on LIKE (regular expression) values.</span></span>
        
  - <span data-ttu-id="d0fc4-118">RELOP_EQ: 比較で行われるベースの値に等しい。</span><span class="sxs-lookup"><span data-stu-id="d0fc4-118">RELOP_EQ: The comparison is made based on equal values.</span></span>
    
<span data-ttu-id="d0fc4-119">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="d0fc4-119">**ulPropTag**</span></span>
  
> <span data-ttu-id="d0fc4-120">プロパティ タグを比較するプロパティを識別します。</span><span class="sxs-lookup"><span data-stu-id="d0fc4-120">Property tag identifying the property to be compared.</span></span> 
    
<span data-ttu-id="d0fc4-121">**lpProp**</span><span class="sxs-lookup"><span data-stu-id="d0fc4-121">**lpProp**</span></span>
  
> <span data-ttu-id="d0fc4-122">比較で使用される定数値を含む[SPropValue](spropvalue.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d0fc4-122">Pointer to an [SPropValue](spropvalue.md) structure that contains the constant value that will be used in the comparison.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d0fc4-123">注釈</span><span class="sxs-lookup"><span data-stu-id="d0fc4-123">Remarks</span></span>

<span data-ttu-id="d0fc4-124">**SPropertyRestriction**構造体では、2 つのプロパティ タグがあります。</span><span class="sxs-lookup"><span data-stu-id="d0fc4-124">There are two property tags in an **SPropertyRestriction** structure.</span></span> <span data-ttu-id="d0fc4-125">1 **ulPropTag**のメンバーで、 **lpProp**が指す**SPropValue**構造体の**ulPropTag**メンバーには、他のです。</span><span class="sxs-lookup"><span data-stu-id="d0fc4-125">One is in the **ulPropTag** member and the other is in the **ulPropTag** member of the **SPropValue** structure pointed to by **lpProp**.</span></span> <span data-ttu-id="d0fc4-126">MAPI には、プロパティの識別子フィールドとプロパティの種類] フィールドの両方が必要です。</span><span class="sxs-lookup"><span data-stu-id="d0fc4-126">MAPI requires both the property identifier field and the property type field.</span></span> <span data-ttu-id="d0fc4-127">**SPropertyRestriction**で**ulPropTag**では、対応するプロパティと**SPropValue**の**ulPropTag**の型に**SPropertyRestriction**の**lpProp**のポインターを示す方法のメンバーの値、**lpProp**共用体が解釈されます。</span><span class="sxs-lookup"><span data-stu-id="d0fc4-127">The **ulPropTag** in **SPropertyRestriction** is the property to be matched, and the **lpProp** pointer of the **SPropertyRestriction** to the **ulPropTag**'s type of the **SPropValue** indicates how the members value of the **lpProp** union are interpreted.</span></span> <span data-ttu-id="d0fc4-128">2 つのプロパティの型が一致する必要がありますが、そのエラー値の制限は、 [IMAPITable::Restrict](imapitable-restrict.md)または[IMAPITable::FindRow](imapitable-findrow.md)への呼び出しで使用すると MAPI_E_TOO_COMPLEX が返されます。</span><span class="sxs-lookup"><span data-stu-id="d0fc4-128">The two property types must match, or else the error value MAPI_E_TOO_COMPLEX is returned when the restriction is used in a call to [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> 
  
<span data-ttu-id="d0fc4-129">比較の順序は、 _(プロパティの値) (関係演算子) (定数)_。</span><span class="sxs-lookup"><span data-stu-id="d0fc4-129">The comparison order is  _(property value) (relational operator) (constant value)_.</span></span>
  
<span data-ttu-id="d0fc4-130">プロパティの制限が**IMAPITable::Restrict**または**IMAPITable::FindRow**に渡され、ターゲット プロパティが存在しない、制限の結果は定義されていません。</span><span class="sxs-lookup"><span data-stu-id="d0fc4-130">When a property restriction is passed to **IMAPITable::Restrict** or **IMAPITable::FindRow** and the target property does not exist, the results of the restriction are undefined.</span></span> <span data-ttu-id="d0fc4-131">**既存**の制限のプロパティの制限を結合して**** の制限を作成すると、呼び出し元を正確な結果保証することができます。</span><span class="sxs-lookup"><span data-stu-id="d0fc4-131">By creating an **AND** restriction that joins the property restriction with an **EXIST** restriction, a caller can be guaranteed accurate results.</span></span> <span data-ttu-id="d0fc4-132">[SExistRestriction](sexistrestriction.md)構造体を使用すると、**既存**の制限、**および**制限を定義するのには、 [SAndRestriction](sandrestriction.md)構造体を定義します。</span><span class="sxs-lookup"><span data-stu-id="d0fc4-132">Use an [SExistRestriction](sexistrestriction.md) structure to define the **EXIST** restriction and an [SAndRestriction](sandrestriction.md) structure to define the **AND** restriction.</span></span> 
  
<span data-ttu-id="d0fc4-133">複数値を持つプロパティ タグは、テーブルを実装するサービス プロバイダーによってサポートされる場合、プロパティ制限で使用できます。</span><span class="sxs-lookup"><span data-stu-id="d0fc4-133">Multi-valued property tags can be used in property restrictions if the service provider implementing the table supports them.</span></span> <span data-ttu-id="d0fc4-134">サポートされている場合は、複数値を持つプロパティ タグも使えます単一値プロパティ タグを使用できます。</span><span class="sxs-lookup"><span data-stu-id="d0fc4-134">If supported, multi-valued property tags can be used anywhere single-valued property tags can be used.</span></span> 
  
<span data-ttu-id="d0fc4-135">複数値を持つプロパティ タグは、次の方法で使用できます。</span><span class="sxs-lookup"><span data-stu-id="d0fc4-135">Multi-valued property tags can be used in the following methods:</span></span>
  
- [<span data-ttu-id="d0fc4-136">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="d0fc4-136">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
- [<span data-ttu-id="d0fc4-137">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="d0fc4-137">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
    
- [<span data-ttu-id="d0fc4-138">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="d0fc4-138">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
    
- [<span data-ttu-id="d0fc4-139">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="d0fc4-139">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
- [<span data-ttu-id="d0fc4-140">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="d0fc4-140">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
    
> [!IMPORTANT]
> <span data-ttu-id="d0fc4-141">注目すべき場合は、2 つのプロパティ タグが一致しない場合は、複数値プロパティに制限する場合です。</span><span class="sxs-lookup"><span data-stu-id="d0fc4-141">A notable case when the two property tags won't match is if restricting on a multi-value property.</span></span> <span data-ttu-id="d0fc4-142">このケースでは、次の満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="d0fc4-142">In this case the following must be true.</span></span> <span data-ttu-id="d0fc4-143">> **SPropValue**の**ulPropTag**のプロパティの型が以前の MV_-に一致する必要があります**SPropertyRestriction**の**ulPropTag**のプロパティの型には、複数値プロパティの型のビット フラグの MV_FLAG (0x1000) が含まれている場合、フラグのビット フラグのうち、その逆行列は、です。</span><span class="sxs-lookup"><span data-stu-id="d0fc4-143">> If the property type of the **ulPropTag** of **SPropertyRestriction** contains the multi-value property type bit flag MV_FLAG (0x1000), the property type of the **ulPropTag** of **SPropValue** should match the former minus the MV_FLAG bit flag, that is, its inverse.</span></span> <span data-ttu-id="d0fc4-144">> の例では、0x8012101f、PROP_TAG は、このプロパティのプロパティ タグを使用して、カテゴリなどの複数の値のカスタム文字列プロパティを使用して制限するのには (MV_FLAG | PT_UNICODE、0x8012))、対応する**SPropertyRestriction**のようになります次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="d0fc4-144">> For example, to restrict using a multi-value custom string property such as a category with a property tag for the property 0x8012101f, that is, PROP_TAG(MV_FLAG|PT_UNICODE, 0x8012)), the corresponding **SPropertyRestriction** would appear as follows.</span></span><span data-ttu-id="d0fc4-145"> >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";`> **SPropValue**の**ulPropTag**のプロパティの型に MV_FLAG ビット フラグが含まれている可能性があります戻り値が MAPI_E_TOO_COMPLEX に注意してください。</span><span class="sxs-lookup"><span data-stu-id="d0fc4-145"> >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";`> Note that if the property type of the **ulPropTag** of **SPropValue** contains the MV_FLAG bit flag, the likely return is MAPI_E_TOO_COMPLEX.</span></span> 
  
<span data-ttu-id="d0fc4-146">**SPropertyRestriction**構造体の詳細については、[制限の詳細](about-restrictions.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d0fc4-146">For more information about the **SPropertyRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d0fc4-147">関連項目</span><span class="sxs-lookup"><span data-stu-id="d0fc4-147">See also</span></span>

- [<span data-ttu-id="d0fc4-148">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="d0fc4-148">SExistRestriction</span></span>](sexistrestriction.md)
- [<span data-ttu-id="d0fc4-149">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="d0fc4-149">SAndRestriction</span></span>](sandrestriction.md)
- [<span data-ttu-id="d0fc4-150">SPropValue</span><span class="sxs-lookup"><span data-stu-id="d0fc4-150">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="d0fc4-151">SRestriction</span><span class="sxs-lookup"><span data-stu-id="d0fc4-151">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="d0fc4-152">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="d0fc4-152">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
- [<span data-ttu-id="d0fc4-153">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="d0fc4-153">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
- [<span data-ttu-id="d0fc4-154">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="d0fc4-154">MAPI Structures</span></span>](mapi-structures.md)

