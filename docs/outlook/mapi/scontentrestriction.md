---
title: SContentRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SContentRestriction
api_type:
- COM
ms.assetid: 784c8a5a-493e-48e6-8784-ba8122c76e3d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 87be6df27a3e6729cb514118438521d76a66b30c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423665"
---
# <a name="scontentrestriction"></a><span data-ttu-id="fcfd6-103">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="fcfd6-103">SContentRestriction</span></span>
 
<span data-ttu-id="fcfd6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fcfd6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fcfd6-105">テーブル ビューを、検索文字列に一致するコンテンツを含む列を含む行にのみ制限するために使用されるコンテンツ制限について説明します。</span><span class="sxs-lookup"><span data-stu-id="fcfd6-105">Describes a content restriction, which is used to limit a table view to only those rows that include a column with contents matching a search string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fcfd6-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="fcfd6-106">Header file:</span></span>  <br/> |<span data-ttu-id="fcfd6-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fcfd6-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SContentRestriction
{
  ULONG        ulFuzzyLevel;
  ULONG        ulPropTag;
  LPSPropValue lpProp;
} SContentRestriction;

```

## <a name="members"></a><span data-ttu-id="fcfd6-108">Members</span><span class="sxs-lookup"><span data-stu-id="fcfd6-108">Members</span></span>

<span data-ttu-id="fcfd6-109">**ulFuzzyLevel**</span><span class="sxs-lookup"><span data-stu-id="fcfd6-109">**ulFuzzyLevel**</span></span>
  
> <span data-ttu-id="fcfd6-110">一致を確認するときにコンテンツ制限が適用する精度のレベルを定義するオプション設定。</span><span class="sxs-lookup"><span data-stu-id="fcfd6-110">Option settings defining the level of preciseness that the content restriction should enforce when you verify for a match.</span></span>
    
   <span data-ttu-id="fcfd6-111">**ulFuzzyLevel** メンバーの下位 **16** ビットは、PT_BINARY および PT_STRING8 型のプロパティに適用され、次のいずれかの値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fcfd6-111">The **lower 16 bits** of the **ulFuzzyLevel** member apply to properties of type PT_BINARY and PT_STRING8 and must be set to one of the following values:</span></span> 
    
   - <span data-ttu-id="fcfd6-112">FL_FULLSTRING: 一致するには **、lpProp** 検索文字列が ulPropTag で識別されるプロパティに含 **まれている必要があります**。</span><span class="sxs-lookup"><span data-stu-id="fcfd6-112">FL_FULLSTRING: To match, the **lpProp** search string must be contained in the property identified by **ulPropTag**.</span></span>
        
   - <span data-ttu-id="fcfd6-113">FL_PREFIX : 一致するには **、ulPropTag** で識別されるプロパティの最初に lpProp 検索文字列が **表示されている必要があります**。</span><span class="sxs-lookup"><span data-stu-id="fcfd6-113">FL_PREFIX : To match, the **lpProp** search string must appear at the start of the property identified by **ulPropTag**.</span></span> <span data-ttu-id="fcfd6-114">2 つの文字列は、lpProp で示される検索文字列の長さまでのみ比較 **する必要があります**。</span><span class="sxs-lookup"><span data-stu-id="fcfd6-114">The two strings should be compared only up to the length of the search string indicated by **lpProp**.</span></span> 
        
   - <span data-ttu-id="fcfd6-115">FL_SUBSTRING: 一致するには **、lpProp** 検索文字列が ulPropTag で識別されるプロパティの任意の場所に **含まれている必要があります**。</span><span class="sxs-lookup"><span data-stu-id="fcfd6-115">FL_SUBSTRING: To match, the **lpProp** search string must be contained anywhere in the property identified by **ulPropTag**.</span></span> 
        
   <span data-ttu-id="fcfd6-116">**ulFuzzyLevel** メンバーの上位 **16** ビットは、PT_STRING8 型のプロパティにのみ適用され、任意の組み合わせで次の値に設定できます。</span><span class="sxs-lookup"><span data-stu-id="fcfd6-116">The **upper 16 bits** of the **ulFuzzyLevel** member apply only to properties of type PT_STRING8 and can be set to the following values in any combination:</span></span> 
        
   - <span data-ttu-id="fcfd6-117">FL_IGNORECASE: ケースを考慮せずに比較を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="fcfd6-117">FL_IGNORECASE: The comparison should be made without considering case.</span></span> 
        
   - <span data-ttu-id="fcfd6-118">FL_IGNORENONSPACE: この比較では、二等分記号などの Unicode で定義された非間隔文字は無視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fcfd6-118">FL_IGNORENONSPACE: The comparison should ignore Unicode-defined non-spacing characters such as diacritical marks.</span></span> 
        
   - <span data-ttu-id="fcfd6-119">FL_LOOSE: 大文字と小文字を無視して、可能な限り一致する比較を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="fcfd6-119">FL_LOOSE: The comparison should give you a match whenever possible, ignoring case and non-spacing characters.</span></span> 
    
<span data-ttu-id="fcfd6-120">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="fcfd6-120">**ulPropTag**</span></span>
  
> <span data-ttu-id="fcfd6-121">検索文字列の出現をチェックする文字列プロパティを識別するプロパティ タグ。</span><span class="sxs-lookup"><span data-stu-id="fcfd6-121">Property tag identifying the string property to be checked for occurrence of the search string.</span></span> 
    
<span data-ttu-id="fcfd6-122">**lpProp**</span><span class="sxs-lookup"><span data-stu-id="fcfd6-122">**lpProp**</span></span>
  
> <span data-ttu-id="fcfd6-123">検索文字列として使用する文字列値を含むプロパティ値構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="fcfd6-123">Pointer to a property value structure that contains the string value to use as the search string.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fcfd6-124">注釈</span><span class="sxs-lookup"><span data-stu-id="fcfd6-124">Remarks</span></span>

<span data-ttu-id="fcfd6-125">**SContentRestriction** 構造体には **、1 つは ulPropTag** メンバー、もう 1 つは **lpProp** によって指される **SPropValue** 構造体の **ulPropTag** メンバーの 2 つのプロパティ タグがあります。</span><span class="sxs-lookup"><span data-stu-id="fcfd6-125">There are two property tags in an **SContentRestriction** structure: one in the **ulPropTag** member and the other in the **ulPropTag** member of the **SPropValue** structure pointed to by **lpProp**.</span></span> <span data-ttu-id="fcfd6-126">どちらのタグでも、MAPI はプロパティの種類フィールドのみを必要とし、プロパティ識別子フィールドを無視します。</span><span class="sxs-lookup"><span data-stu-id="fcfd6-126">In both tags, MAPI requires only the property type field and ignores the property identifier field.</span></span> <span data-ttu-id="fcfd6-127">ただし、2 つのプロパティの種類が一致する必要があります。それ以外の場合は [、IMAPITable::Restrict](imapitable-restrict.md) または [IMAPITable::FindRow](imapitable-findrow.md)の呼び出しで制限が使用される場合、エラー値 MAPI_E_TOO_COMPLEX が返されます。</span><span class="sxs-lookup"><span data-stu-id="fcfd6-127">However, the two property types must match, or else the error value MAPI_E_TOO_COMPLEX is returned when the restriction is used in a call to [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> 
  
<span data-ttu-id="fcfd6-128">値はFL_FULLSTRING、FL_PREFIX、およびFL_SUBSTRING排他的です。</span><span class="sxs-lookup"><span data-stu-id="fcfd6-128">The values FL_FULLSTRING, FL_PREFIX, and FL_SUBSTRING are mutually exclusive.</span></span> <span data-ttu-id="fcfd6-129">設定できるのは 1 つのみであり、そのうちの 1 つを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fcfd6-129">Only one of them can be set, and one of them must be set.</span></span> <span data-ttu-id="fcfd6-130">その意味は固定され、プロバイダーは定義されたとおりに実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fcfd6-130">Their meanings are fixed, and the provider must implement them exactly as defined.</span></span> <span data-ttu-id="fcfd6-131">プロバイダーは、これらの値MAPI_E_TOO_COMPLEXサポートできない場合は、この値を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="fcfd6-131">The provider should return MAPI_E_TOO_COMPLEX if it is unable to support these values.</span></span> 
  
<span data-ttu-id="fcfd6-132">値はFL_IGNORECASE、FL_IGNORENONSPACE、およびFL_LOOSE独立しています。</span><span class="sxs-lookup"><span data-stu-id="fcfd6-132">The values FL_IGNORECASE, FL_IGNORENONSPACE, and FL_LOOSE are independent.</span></span> <span data-ttu-id="fcfd6-133">ゼロから 3 つすべての任意の場所に設定できます。</span><span class="sxs-lookup"><span data-stu-id="fcfd6-133">Anywhere from zero to all three of them can be set.</span></span> <span data-ttu-id="fcfd6-134">これらの定義はガイドラインとしてのみ提供され、プロバイダーは各フラグの固有の意味を自由に実装できます。</span><span class="sxs-lookup"><span data-stu-id="fcfd6-134">Their definitions are provided as a guideline only, and the provider is free to implement its own specific meaning of each flag.</span></span> <span data-ttu-id="fcfd6-135">指定したフラグが実装されていない場合、プロバイダーはエラーの表示を返す必要はありません。</span><span class="sxs-lookup"><span data-stu-id="fcfd6-135">The provider should not return any error indication if it has no implementation of a specified flag.</span></span> 
  
<span data-ttu-id="fcfd6-136">プロパティに対してコンテンツ制限が適用された結果は、プロパティが存在しない場合は未定義です。</span><span class="sxs-lookup"><span data-stu-id="fcfd6-136">The result of a content restriction imposed against a property is undefined when the property does not exist.</span></span> <span data-ttu-id="fcfd6-137">クライアントがこのような制限に対して十分に定義された動作を必要とし、プロパティが存在するかどうかが分からない場合、プロパティがテーブルの必須列ではない場合は、存在制限を使用してコンテンツ制限に参加する **AND** 制限を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fcfd6-137">When a client requires well-defined behavior for such a restriction and is not sure whether the property exists for example, it is not a required column of a table it should create an **AND** restriction to join the content restriction with an exist restriction.</span></span> <span data-ttu-id="fcfd6-138">[SExistRestriction](sexistrestriction.md)構造体を使用して、存在制限と [SAndRestriction](sandrestriction.md)構造体を定義して AND 制限 **を定義** します。</span><span class="sxs-lookup"><span data-stu-id="fcfd6-138">Use an [SExistRestriction](sexistrestriction.md) structure to define the exist restriction and an [SAndRestriction](sandrestriction.md) structure to define the **AND** restriction.</span></span> 
  
<span data-ttu-id="fcfd6-139">**SContentRestriction** 構造と制限全般の詳細については、「制限について」[を参照してください](about-restrictions.md)。</span><span class="sxs-lookup"><span data-stu-id="fcfd6-139">For more information about the **SContentRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fcfd6-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="fcfd6-140">See also</span></span>

- [<span data-ttu-id="fcfd6-141">SPropValue</span><span class="sxs-lookup"><span data-stu-id="fcfd6-141">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="fcfd6-142">SRestriction</span><span class="sxs-lookup"><span data-stu-id="fcfd6-142">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="fcfd6-143">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="fcfd6-143">MAPI Structures</span></span>](mapi-structures.md)

