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
# <a name="scontentrestriction"></a><span data-ttu-id="454b1-103">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="454b1-103">SContentRestriction</span></span>
 
<span data-ttu-id="454b1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="454b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="454b1-105">コンテンツ制限について説明します。これは、テーブルビューを、検索文字列と一致するコンテンツを持つ列を含む行だけに制限するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="454b1-105">Describes a content restriction, which is used to limit a table view to only those rows that include a column with contents matching a search string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="454b1-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="454b1-106">Header file:</span></span>  <br/> |<span data-ttu-id="454b1-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="454b1-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SContentRestriction
{
  ULONG        ulFuzzyLevel;
  ULONG        ulPropTag;
  LPSPropValue lpProp;
} SContentRestriction;

```

## <a name="members"></a><span data-ttu-id="454b1-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="454b1-108">Members</span></span>

<span data-ttu-id="454b1-109">**ulFuzzyLevel**</span><span class="sxs-lookup"><span data-stu-id="454b1-109">**ulFuzzyLevel**</span></span>
  
> <span data-ttu-id="454b1-110">一致するかどうかを確認するときにコンテンツ制限に適用する preciseness レベルを定義するオプション設定。</span><span class="sxs-lookup"><span data-stu-id="454b1-110">Option settings defining the level of preciseness that the content restriction should enforce when you verify for a match.</span></span>
    
   <span data-ttu-id="454b1-111">**ulFuzzyLevel**メンバーの**下位16ビット**は、PT_BINARY および PT_STRING8 型のプロパティに適用され、次のいずれかの値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="454b1-111">The **lower 16 bits** of the **ulFuzzyLevel** member apply to properties of type PT_BINARY and PT_STRING8 and must be set to one of the following values:</span></span> 
    
   - <span data-ttu-id="454b1-112">FL_FULLSTRING: 一致するには、 **lpprop**検索文字列が**ulPropTag**で識別されるプロパティに含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="454b1-112">FL_FULLSTRING: To match, the **lpProp** search string must be contained in the property identified by **ulPropTag**.</span></span>
        
   - <span data-ttu-id="454b1-113">FL_PREFIX: 一致するには、 **ulPropTag**で識別されるプロパティの先頭に**lpprop**検索文字列を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="454b1-113">FL_PREFIX : To match, the **lpProp** search string must appear at the start of the property identified by **ulPropTag**.</span></span> <span data-ttu-id="454b1-114">2つの文字列は、 **lpprop**で示される検索文字列の長さまで比較する必要があります。</span><span class="sxs-lookup"><span data-stu-id="454b1-114">The two strings should be compared only up to the length of the search string indicated by **lpProp**.</span></span> 
        
   - <span data-ttu-id="454b1-115">FL_SUBSTRING: 一致するには、 **lpprop**検索文字列が**ulPropTag**で識別されるプロパティの任意の場所に含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="454b1-115">FL_SUBSTRING: To match, the **lpProp** search string must be contained anywhere in the property identified by **ulPropTag**.</span></span> 
        
   <span data-ttu-id="454b1-116">**ulFuzzyLevel**メンバーの**上位16ビット**は、PT_STRING8 型のプロパティにのみ適用され、任意の組み合わせで次の値に設定できます。</span><span class="sxs-lookup"><span data-stu-id="454b1-116">The **upper 16 bits** of the **ulFuzzyLevel** member apply only to properties of type PT_STRING8 and can be set to the following values in any combination:</span></span> 
        
   - <span data-ttu-id="454b1-117">FL_IGNORECASE: 比較は、大文字と小文字を区別せずに行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="454b1-117">FL_IGNORECASE: The comparison should be made without considering case.</span></span> 
        
   - <span data-ttu-id="454b1-118">FL_IGNORENONSPACE: 比較では、Unicode で定義されたスペース以外の文字 (分音記号など) を無視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="454b1-118">FL_IGNORENONSPACE: The comparison should ignore Unicode-defined non-spacing characters such as diacritical marks.</span></span> 
        
   - <span data-ttu-id="454b1-119">FL_LOOSE: 比較によって、大文字と小文字を区別せずに、可能な限り一致が得られます。</span><span class="sxs-lookup"><span data-stu-id="454b1-119">FL_LOOSE: The comparison should give you a match whenever possible, ignoring case and non-spacing characters.</span></span> 
    
<span data-ttu-id="454b1-120">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="454b1-120">**ulPropTag**</span></span>
  
> <span data-ttu-id="454b1-121">検索文字列の出現をチェックする文字列プロパティを識別するプロパティタグ。</span><span class="sxs-lookup"><span data-stu-id="454b1-121">Property tag identifying the string property to be checked for occurrence of the search string.</span></span> 
    
<span data-ttu-id="454b1-122">**lpprop**</span><span class="sxs-lookup"><span data-stu-id="454b1-122">**lpProp**</span></span>
  
> <span data-ttu-id="454b1-123">検索文字列として使用する文字列値を含むプロパティ値構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="454b1-123">Pointer to a property value structure that contains the string value to use as the search string.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="454b1-124">注釈</span><span class="sxs-lookup"><span data-stu-id="454b1-124">Remarks</span></span>

<span data-ttu-id="454b1-125">**scontentrestriction**構造体には、 **ulPropTag**メンバーと、 **lpprop**でポイントされている**scontentrestriction**構造の**ulPropTag**メンバー内の2つのプロパティタグがあります。</span><span class="sxs-lookup"><span data-stu-id="454b1-125">There are two property tags in an **SContentRestriction** structure: one in the **ulPropTag** member and the other in the **ulPropTag** member of the **SPropValue** structure pointed to by **lpProp**.</span></span> <span data-ttu-id="454b1-126">両方のタグで、MAPI は property type フィールドのみを必要とし、[プロパティ識別子] フィールドは無視されます。</span><span class="sxs-lookup"><span data-stu-id="454b1-126">In both tags, MAPI requires only the property type field and ignores the property identifier field.</span></span> <span data-ttu-id="454b1-127">ただし、2つのプロパティの型が一致している必要があります。または、制限が[imapitable:: Restrict](imapitable-restrict.md)または[imapitable:: FindRow](imapitable-findrow.md)の呼び出しで使用されている場合は、エラー値 MAPI_E_TOO_COMPLEX が返されます。</span><span class="sxs-lookup"><span data-stu-id="454b1-127">However, the two property types must match, or else the error value MAPI_E_TOO_COMPLEX is returned when the restriction is used in a call to [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> 
  
<span data-ttu-id="454b1-128">FL_FULLSTRING、FL_PREFIX、および FL_SUBSTRING の値は相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="454b1-128">The values FL_FULLSTRING, FL_PREFIX, and FL_SUBSTRING are mutually exclusive.</span></span> <span data-ttu-id="454b1-129">設定できるのは1つだけで、そのうちの1つを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="454b1-129">Only one of them can be set, and one of them must be set.</span></span> <span data-ttu-id="454b1-130">これらの意味は固定されており、プロバイダーは定義されたとおりに実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="454b1-130">Their meanings are fixed, and the provider must implement them exactly as defined.</span></span> <span data-ttu-id="454b1-131">プロバイダーは、これらの値をサポートできない場合は MAPI_E_TOO_COMPLEX を返します。</span><span class="sxs-lookup"><span data-stu-id="454b1-131">The provider should return MAPI_E_TOO_COMPLEX if it is unable to support these values.</span></span> 
  
<span data-ttu-id="454b1-132">FL_IGNORECASE、FL_IGNORENONSPACE、および FL_LOOSE の値は独立しています。</span><span class="sxs-lookup"><span data-stu-id="454b1-132">The values FL_IGNORECASE, FL_IGNORENONSPACE, and FL_LOOSE are independent.</span></span> <span data-ttu-id="454b1-133">ゼロから3つまでのすべての場所を設定できます。</span><span class="sxs-lookup"><span data-stu-id="454b1-133">Anywhere from zero to all three of them can be set.</span></span> <span data-ttu-id="454b1-134">これらの定義はガイドラインとしてのみ提供されており、プロバイダーは各フラグの固有の意味を自由に実装することができます。</span><span class="sxs-lookup"><span data-stu-id="454b1-134">Their definitions are provided as a guideline only, and the provider is free to implement its own specific meaning of each flag.</span></span> <span data-ttu-id="454b1-135">プロバイダーは、指定されたフラグの実装がない場合は、エラー表示を返さないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="454b1-135">The provider should not return any error indication if it has no implementation of a specified flag.</span></span> 
  
<span data-ttu-id="454b1-136">プロパティが存在しない場合、プロパティに対して適用されるコンテンツ制限の結果は未定義です。</span><span class="sxs-lookup"><span data-stu-id="454b1-136">The result of a content restriction imposed against a property is undefined when the property does not exist.</span></span> <span data-ttu-id="454b1-137">クライアントでこのような制限に対して適切に定義された動作が必要であり、そのプロパティが存在するかどうかが不明な場合は、そのプロパティが存在するかどうかは、テーブルの必須列ではないので、コンテンツ制限を既存の制限で結合するための**と**制限を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="454b1-137">When a client requires well-defined behavior for such a restriction and is not sure whether the property exists for example, it is not a required column of a table it should create an **AND** restriction to join the content restriction with an exist restriction.</span></span> <span data-ttu-id="454b1-138">[sexistrestriction](sexistrestriction.md)構造を使用して、**と**制限を定義するための、存在制限と[SAndRestriction](sandrestriction.md)構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="454b1-138">Use an [SExistRestriction](sexistrestriction.md) structure to define the exist restriction and an [SAndRestriction](sandrestriction.md) structure to define the **AND** restriction.</span></span> 
  
<span data-ttu-id="454b1-139">**scontentrestriction**構造と一般的な制限の詳細については、「[制限につい](about-restrictions.md)て」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="454b1-139">For more information about the **SContentRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="454b1-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="454b1-140">See also</span></span>

- [<span data-ttu-id="454b1-141">SPropValue</span><span class="sxs-lookup"><span data-stu-id="454b1-141">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="454b1-142">SRestriction</span><span class="sxs-lookup"><span data-stu-id="454b1-142">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="454b1-143">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="454b1-143">MAPI Structures</span></span>](mapi-structures.md)

