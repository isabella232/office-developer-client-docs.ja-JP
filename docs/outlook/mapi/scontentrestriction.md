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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 34177aee48adad7eecb40836a247705fc22d2a32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803840"
---
# <a name="scontentrestriction"></a><span data-ttu-id="624c9-103">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="624c9-103">SContentRestriction</span></span>
 
<span data-ttu-id="624c9-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="624c9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="624c9-105">検索文字列に一致する内容を持つ列を含む行だけを表形式ビューを制限するために使用されるコンテンツの制限について説明します。</span><span class="sxs-lookup"><span data-stu-id="624c9-105">Describes a content restriction, which is used to limit a table view to only those rows that include a column with contents matching a search string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="624c9-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="624c9-106">Header file:</span></span>  <br/> |<span data-ttu-id="624c9-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="624c9-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SContentRestriction
{
  ULONG        ulFuzzyLevel;
  ULONG        ulPropTag;
  LPSPropValue lpProp;
} SContentRestriction;

```

## <a name="members"></a><span data-ttu-id="624c9-108">Members</span><span class="sxs-lookup"><span data-stu-id="624c9-108">Members</span></span>

<span data-ttu-id="624c9-109">**ulFuzzyLevel**</span><span class="sxs-lookup"><span data-stu-id="624c9-109">**ulFuzzyLevel**</span></span>
  
> <span data-ttu-id="624c9-110">オプションの設定が一致することを確認するときにコンテンツの制限が設定されている preciseness のレベルを定義します。</span><span class="sxs-lookup"><span data-stu-id="624c9-110">Option settings defining the level of preciseness that the content restriction should enforce when you verify for a match.</span></span>
    
   <span data-ttu-id="624c9-111">**UlFuzzyLevel**メンバーの**下位 16 ビット**は、PT_BINARY と PT_STRING8 プロパティの型に適用し、次の値のいずれかに設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="624c9-111">The **lower 16 bits** of the **ulFuzzyLevel** member apply to properties of type PT_BINARY and PT_STRING8 and must be set to one of the following values:</span></span> 
    
   - <span data-ttu-id="624c9-112">FL_FULLSTRING: 一致するには、 **lpProp**の検索文字列含める必要があります**ulPropTag**によって識別されるプロパティにします。</span><span class="sxs-lookup"><span data-stu-id="624c9-112">FL_FULLSTRING: To match, the **lpProp** search string must be contained in the property identified by **ulPropTag**.</span></span>
        
   - <span data-ttu-id="624c9-113">FL_PREFIX: 一致するには、 **lpProp**の検索文字列必要があります**ulPropTag**によって識別されるプロパティの先頭にします。</span><span class="sxs-lookup"><span data-stu-id="624c9-113">FL_PREFIX : To match, the **lpProp** search string must appear at the start of the property identified by **ulPropTag**.</span></span> <span data-ttu-id="624c9-114">**LpProp**によって示される検索文字列の長さの分だけ、2 つの文字列を比較する必要があります。</span><span class="sxs-lookup"><span data-stu-id="624c9-114">The two strings should be compared only up to the length of the search string indicated by **lpProp**.</span></span> 
        
   - <span data-ttu-id="624c9-115">FL_SUBSTRING: 一致するには、 **lpProp**検索文字列含める必要があります任意の場所**ulPropTag**によって識別されるプロパティにします。</span><span class="sxs-lookup"><span data-stu-id="624c9-115">FL_SUBSTRING: To match, the **lpProp** search string must be contained anywhere in the property identified by **ulPropTag**.</span></span> 
        
   <span data-ttu-id="624c9-116">**UlFuzzyLevel**メンバーの**上位 16 ビット**では、型 PT_STRING8 プロパティにのみ適用され、任意の組み合わせで次の値を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="624c9-116">The **upper 16 bits** of the **ulFuzzyLevel** member apply only to properties of type PT_STRING8 and can be set to the following values in any combination:</span></span> 
        
   - <span data-ttu-id="624c9-117">FL_IGNORECASE: 大文字と小文字を考慮せず、比較を行ってください。</span><span class="sxs-lookup"><span data-stu-id="624c9-117">FL_IGNORECASE: The comparison should be made without considering case.</span></span> 
        
   - <span data-ttu-id="624c9-118">FL_IGNORENONSPACE: 比較は、アクセント記号などの Unicode が定義されている空白でない文字を無視してください。</span><span class="sxs-lookup"><span data-stu-id="624c9-118">FL_IGNORENONSPACE: The comparison should ignore Unicode-defined non-spacing characters such as diacritical marks.</span></span> 
        
   - <span data-ttu-id="624c9-119">FL_LOOSE: 比較頂いた一致する限り、大文字と小文字、空白でない文字を無視しています。</span><span class="sxs-lookup"><span data-stu-id="624c9-119">FL_LOOSE: The comparison should give you a match whenever possible, ignoring case and non-spacing characters.</span></span> 
    
<span data-ttu-id="624c9-120">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="624c9-120">**ulPropTag**</span></span>
  
> <span data-ttu-id="624c9-121">プロパティ タグが検索文字列の出現箇所をチェックする文字列プロパティを識別します。</span><span class="sxs-lookup"><span data-stu-id="624c9-121">Property tag identifying the string property to be checked for occurrence of the search string.</span></span> 
    
<span data-ttu-id="624c9-122">**lpProp**</span><span class="sxs-lookup"><span data-stu-id="624c9-122">**lpProp**</span></span>
  
> <span data-ttu-id="624c9-123">検索文字列として使用する文字列値を格納するプロパティ値の構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="624c9-123">Pointer to a property value structure that contains the string value to use as the search string.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="624c9-124">注釈</span><span class="sxs-lookup"><span data-stu-id="624c9-124">Remarks</span></span>

<span data-ttu-id="624c9-125">**SContentRestriction**構造体には 2 つのプロパティ タグがあります: **lpProp**が指す**ulPropTag**のメンバーと、 **ulPropTag** 、 **SPropValue**構造体のメンバーで、その他のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="624c9-125">There are two property tags in an **SContentRestriction** structure: one in the **ulPropTag** member and the other in the **ulPropTag** member of the **SPropValue** structure pointed to by **lpProp**.</span></span> <span data-ttu-id="624c9-126">両方のタグでは、MAPI プロパティの種類のフィールドだけが必要ですでプロパティの識別子フィールドは無視されます。</span><span class="sxs-lookup"><span data-stu-id="624c9-126">In both tags, MAPI requires only the property type field and ignores the property identifier field.</span></span> <span data-ttu-id="624c9-127">ただし、2 つのプロパティの型が一致する必要がありますか、またはエラー値の制限は、 [IMAPITable::Restrict](imapitable-restrict.md)または[IMAPITable::FindRow](imapitable-findrow.md)への呼び出しで使用すると MAPI_E_TOO_COMPLEX が返されます。</span><span class="sxs-lookup"><span data-stu-id="624c9-127">However, the two property types must match, or else the error value MAPI_E_TOO_COMPLEX is returned when the restriction is used in a call to [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> 
  
<span data-ttu-id="624c9-128">FL_FULLSTRING、FL_PREFIX、FL_SUBSTRING の値は、相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="624c9-128">The values FL_FULLSTRING, FL_PREFIX, and FL_SUBSTRING are mutually exclusive.</span></span> <span data-ttu-id="624c9-129">それらの 1 つだけを設定することができ、それらのいずれかを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="624c9-129">Only one of them can be set, and one of them must be set.</span></span> <span data-ttu-id="624c9-130">その意味は固定で、プロバイダーは定義されているとおりに正確にして実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="624c9-130">Their meanings are fixed, and the provider must implement them exactly as defined.</span></span> <span data-ttu-id="624c9-131">プロバイダーは、これらの値をサポートするためにできない場合、MAPI_E_TOO_COMPLEX を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="624c9-131">The provider should return MAPI_E_TOO_COMPLEX if it is unable to support these values.</span></span> 
  
<span data-ttu-id="624c9-132">FL_IGNORECASE、FL_IGNORENONSPACE、FL_LOOSE の値は独立しています。</span><span class="sxs-lookup"><span data-stu-id="624c9-132">The values FL_IGNORECASE, FL_IGNORENONSPACE, and FL_LOOSE are independent.</span></span> <span data-ttu-id="624c9-133">任意の場所それらのすべての 3 つのゼロからを設定できます。</span><span class="sxs-lookup"><span data-stu-id="624c9-133">Anywhere from zero to all three of them can be set.</span></span> <span data-ttu-id="624c9-134">ガイドラインとしてのみ、その定義が用意されているし、プロバイダーは、各フラグの特定の意味は、独自に実装するために自由です。</span><span class="sxs-lookup"><span data-stu-id="624c9-134">Their definitions are provided as a guideline only, and the provider is free to implement its own specific meaning of each flag.</span></span> <span data-ttu-id="624c9-135">プロバイダーでは指定されたフラグの実装が存在しない場合、エラーは返されません。</span><span class="sxs-lookup"><span data-stu-id="624c9-135">The provider should not return any error indication if it has no implementation of a specified flag.</span></span> 
  
<span data-ttu-id="624c9-136">プロパティが存在しない場合、プロパティに対して設定されたコンテンツの制限の結果は定義されていません。</span><span class="sxs-lookup"><span data-stu-id="624c9-136">The result of a content restriction imposed against a property is undefined when the property does not exist.</span></span> <span data-ttu-id="624c9-137">クライアントは、このような制限について明確に定義された動作が必要で、たとえばプロパティが存在するかどうかでないことが必要なテーブルの列ではありません、既存の制限のあるコンテンツの制限に参加する**と**制限も作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="624c9-137">When a client requires well-defined behavior for such a restriction and is not sure whether the property exists for example, it is not a required column of a table it should create an **AND** restriction to join the content restriction with an exist restriction.</span></span> <span data-ttu-id="624c9-138">[SExistRestriction](sexistrestriction.md)構造体を使用すると、既存の制限、**および**制限を定義するのには、 [SAndRestriction](sandrestriction.md)構造体を定義します。</span><span class="sxs-lookup"><span data-stu-id="624c9-138">Use an [SExistRestriction](sexistrestriction.md) structure to define the exist restriction and an [SAndRestriction](sandrestriction.md) structure to define the **AND** restriction.</span></span> 
  
<span data-ttu-id="624c9-139">**SContentRestriction**構造体および制限の詳細については一般に、[制限の詳細](about-restrictions.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="624c9-139">For more information about the **SContentRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="624c9-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="624c9-140">See also</span></span>

- [<span data-ttu-id="624c9-141">SPropValue</span><span class="sxs-lookup"><span data-stu-id="624c9-141">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="624c9-142">SRestriction</span><span class="sxs-lookup"><span data-stu-id="624c9-142">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="624c9-143">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="624c9-143">MAPI Structures</span></span>](mapi-structures.md)

