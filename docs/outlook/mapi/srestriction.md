---
title: SRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRestriction
api_type:
- COM
ms.assetid: c12b4409-da6f-480b-87af-1e5baea2e8bd
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a2a6d273495df52adb83393dc5549b0872c8f6f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439360"
---
# <a name="srestriction"></a><span data-ttu-id="62d50-103">SRestriction</span><span class="sxs-lookup"><span data-stu-id="62d50-103">SRestriction</span></span>

  
  
<span data-ttu-id="62d50-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="62d50-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="62d50-105">特定の行にテーブルのビューを制限するためのフィルターを記述します。</span><span class="sxs-lookup"><span data-stu-id="62d50-105">Describes a filter for limiting the view of a table to particular rows.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="62d50-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="62d50-106">Header file:</span></span>  <br/> |<span data-ttu-id="62d50-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="62d50-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SRestriction
{
  ULONG rt;
  union
  {
    SComparePropsRestriction resCompareProps;
    SAndRestriction resAnd;
    SOrRestriction resOr;
    SNotRestriction resNot;
    SContentRestriction resContent;
    SPropertyRestriction resProperty;
    SBitMaskRestriction resBitMask;
    SSizeRestriction resSize;
    SExistRestriction resExist;
    SSubRestriction resSub;
    SCommentRestriction resComment;
  } res;
} SRestriction;

```

## <a name="members"></a><span data-ttu-id="62d50-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="62d50-108">Members</span></span>

 <span data-ttu-id="62d50-109">**rt**</span><span class="sxs-lookup"><span data-stu-id="62d50-109">**rt**</span></span>
  
> <span data-ttu-id="62d50-110">制限の種類。</span><span class="sxs-lookup"><span data-stu-id="62d50-110">The restriction type.</span></span> <span data-ttu-id="62d50-111">可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="62d50-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="62d50-112">RES_AND</span><span class="sxs-lookup"><span data-stu-id="62d50-112">RES_AND</span></span> 
  
> <span data-ttu-id="62d50-113">or \*\*\*\* 制限。これは、制限にビット単位の**and**演算を適用します。</span><span class="sxs-lookup"><span data-stu-id="62d50-113">An **AND** restriction, which applies a bitwise **AND** operation to a restriction.</span></span> 
    
<span data-ttu-id="62d50-114">RES_BITMASK</span><span class="sxs-lookup"><span data-stu-id="62d50-114">RES_BITMASK</span></span> 
  
> <span data-ttu-id="62d50-115">ビットマスク制限。これは、プロパティ値にビットマスクを適用します。</span><span class="sxs-lookup"><span data-stu-id="62d50-115">A bitmask restriction, which applies a bitmask to a property value.</span></span>
    
<span data-ttu-id="62d50-116">RES_COMMENT</span><span class="sxs-lookup"><span data-stu-id="62d50-116">RES_COMMENT</span></span> 
  
> <span data-ttu-id="62d50-117">コメント制限。コメントを制限に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="62d50-117">A comment restriction, which associates a comment with a restriction.</span></span>
    
<span data-ttu-id="62d50-118">RES_COMPAREPROPS</span><span class="sxs-lookup"><span data-stu-id="62d50-118">RES_COMPAREPROPS</span></span> 
  
> <span data-ttu-id="62d50-119">2つのプロパティ値を比較するプロパティ比較制限。</span><span class="sxs-lookup"><span data-stu-id="62d50-119">A property comparison restriction, which compares two property values.</span></span>
    
<span data-ttu-id="62d50-120">RES_CONTENT</span><span class="sxs-lookup"><span data-stu-id="62d50-120">RES_CONTENT</span></span> 
  
> <span data-ttu-id="62d50-121">コンテンツ制限。特定のコンテンツのプロパティ値を検索します。</span><span class="sxs-lookup"><span data-stu-id="62d50-121">A content restriction, which searches a property value for specific content.</span></span>
    
<span data-ttu-id="62d50-122">RES_EXIST</span><span class="sxs-lookup"><span data-stu-id="62d50-122">RES_EXIST</span></span> 
  
> <span data-ttu-id="62d50-123">プロパティがサポートされているかどうかを判断する、存在する制限。</span><span class="sxs-lookup"><span data-stu-id="62d50-123">An exist restriction, which determines whether a property is supported.</span></span>
    
<span data-ttu-id="62d50-124">RES_NOT</span><span class="sxs-lookup"><span data-stu-id="62d50-124">RES_NOT</span></span> 
  
> <span data-ttu-id="62d50-125">制限を適用**せず**、制限に対する論理**not**演算を適用します。</span><span class="sxs-lookup"><span data-stu-id="62d50-125">A **NOT** restriction, which applies a logical **NOT** operation to a restriction.</span></span> 
    
<span data-ttu-id="62d50-126">RES_OR</span><span class="sxs-lookup"><span data-stu-id="62d50-126">RES_OR</span></span> 
  
> <span data-ttu-id="62d50-127">**or**制限。これは、制限に対して論理**or**演算を適用します。</span><span class="sxs-lookup"><span data-stu-id="62d50-127">An **OR** restriction, which applies a logical **OR** operation to a restriction.</span></span> 
    
<span data-ttu-id="62d50-128">RES_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="62d50-128">RES_PROPERTY</span></span> 
  
> <span data-ttu-id="62d50-129">プロパティの値が特定の値と一致するかどうかを決定するプロパティ制限。</span><span class="sxs-lookup"><span data-stu-id="62d50-129">A property restriction, which determines whether a property value matches a particular value.</span></span>
    
<span data-ttu-id="62d50-130">RES_SIZE</span><span class="sxs-lookup"><span data-stu-id="62d50-130">RES_SIZE</span></span> 
  
> <span data-ttu-id="62d50-131">サイズ制限。プロパティ値が特定のサイズかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="62d50-131">A size restriction, which determines whether a property value is a particular size.</span></span>
    
<span data-ttu-id="62d50-132">RES_SUBRESTRICTION</span><span class="sxs-lookup"><span data-stu-id="62d50-132">RES_SUBRESTRICTION</span></span> 
  
> <span data-ttu-id="62d50-133">サブオブジェクト制限。これは、メッセージの添付ファイルまたは受信者に制限を適用します。</span><span class="sxs-lookup"><span data-stu-id="62d50-133">A sub-object restriction, which applies a restriction to a message's attachments or recipients.</span></span>
    
 <span data-ttu-id="62d50-134">**res**</span><span class="sxs-lookup"><span data-stu-id="62d50-134">**res**</span></span>
  
> <span data-ttu-id="62d50-135">適用するフィルターを記述する制限構造の和集合。</span><span class="sxs-lookup"><span data-stu-id="62d50-135">Union of restriction structures describing the filter to be applied.</span></span> <span data-ttu-id="62d50-136">**res**メンバーに含まれる特定の構造体は、 **rt**メンバーの値に依存します。</span><span class="sxs-lookup"><span data-stu-id="62d50-136">The specific structure included in the **res** member depends on the value of the **rt** member.</span></span> <span data-ttu-id="62d50-137">次の表に、制限の種類と構造の間のマッピングを示します。</span><span class="sxs-lookup"><span data-stu-id="62d50-137">The mapping between restriction type and structure is listed in the following table.</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="62d50-138">**制限の種類**</span><span class="sxs-lookup"><span data-stu-id="62d50-138">**Restriction type**</span></span> <br/> |<span data-ttu-id="62d50-139">**制限構造**</span><span class="sxs-lookup"><span data-stu-id="62d50-139">**Restriction structure**</span></span> <br/> |
|<span data-ttu-id="62d50-140">RES_AND</span><span class="sxs-lookup"><span data-stu-id="62d50-140">RES_AND</span></span>  <br/> |[<span data-ttu-id="62d50-141">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="62d50-141">SAndRestriction</span></span>](sandrestriction.md) <br/> |
|<span data-ttu-id="62d50-142">RES_BITMASK</span><span class="sxs-lookup"><span data-stu-id="62d50-142">RES_BITMASK</span></span>  <br/> |[<span data-ttu-id="62d50-143">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="62d50-143">SBitMaskRestriction</span></span>](sbitmaskrestriction.md) <br/> |
|<span data-ttu-id="62d50-144">RES_COMMENT</span><span class="sxs-lookup"><span data-stu-id="62d50-144">RES_COMMENT</span></span>  <br/> |[<span data-ttu-id="62d50-145">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="62d50-145">SCommentRestriction</span></span>](scommentrestriction.md) <br/> |
|<span data-ttu-id="62d50-146">RES_COMPAREPROPS</span><span class="sxs-lookup"><span data-stu-id="62d50-146">RES_COMPAREPROPS</span></span>  <br/> |[<span data-ttu-id="62d50-147">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="62d50-147">SComparePropsRestriction</span></span>](scomparepropsrestriction.md) <br/> |
|<span data-ttu-id="62d50-148">RES_CONTENT</span><span class="sxs-lookup"><span data-stu-id="62d50-148">RES_CONTENT</span></span>  <br/> |[<span data-ttu-id="62d50-149">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="62d50-149">SContentRestriction</span></span>](scontentrestriction.md) <br/> |
|<span data-ttu-id="62d50-150">RES_EXIST</span><span class="sxs-lookup"><span data-stu-id="62d50-150">RES_EXIST</span></span>  <br/> |[<span data-ttu-id="62d50-151">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="62d50-151">SExistRestriction</span></span>](sexistrestriction.md) <br/> |
|<span data-ttu-id="62d50-152">RES_NOT</span><span class="sxs-lookup"><span data-stu-id="62d50-152">RES_NOT</span></span>  <br/> |[<span data-ttu-id="62d50-153">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="62d50-153">SNotRestriction</span></span>](snotrestriction.md) <br/> |
|<span data-ttu-id="62d50-154">RES_OR</span><span class="sxs-lookup"><span data-stu-id="62d50-154">RES_OR</span></span>  <br/> |[<span data-ttu-id="62d50-155">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="62d50-155">SOrRestriction</span></span>](sorrestriction.md) <br/> |
|<span data-ttu-id="62d50-156">RES_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="62d50-156">RES_PROPERTY</span></span>  <br/> |[<span data-ttu-id="62d50-157">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="62d50-157">SPropertyRestriction</span></span>](spropertyrestriction.md) <br/> |
|<span data-ttu-id="62d50-158">RES_SIZE</span><span class="sxs-lookup"><span data-stu-id="62d50-158">RES_SIZE</span></span>  <br/> |[<span data-ttu-id="62d50-159">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="62d50-159">SSizeRestriction</span></span>](ssizerestriction.md) <br/> |
|<span data-ttu-id="62d50-160">RES_SUBRESTRICTION</span><span class="sxs-lookup"><span data-stu-id="62d50-160">RES_SUBRESTRICTION</span></span>  <br/> |[<span data-ttu-id="62d50-161">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="62d50-161">SSubRestriction</span></span>](ssubrestriction.md) <br/> |
   
## <a name="remarks"></a><span data-ttu-id="62d50-162">注釈</span><span class="sxs-lookup"><span data-stu-id="62d50-162">Remarks</span></span>

<span data-ttu-id="62d50-163">クライアントは、 **srestriction**構造を使用して、テーブルのビュー内の行の数と種類を制限したり、フォルダー内の特定のメッセージを検索したりします。</span><span class="sxs-lookup"><span data-stu-id="62d50-163">Clients use an **SRestriction** structure to limit the number and type of rows in their view of a table and to search for specific messages in a folder.</span></span> <span data-ttu-id="62d50-164">テーブルに制限を課すために、クライアントは[IMAPITable:: Restrict](imapitable-restrict.md)または[imapitable:: FindRow](imapitable-findrow.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="62d50-164">To impose the limitation on a table, clients call either [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> <span data-ttu-id="62d50-165">フォルダーに制限を課すために、クライアントはフォルダーの[IMAPIContainer:: setsearchcriteria](imapicontainer-setsearchcriteria.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="62d50-165">To impose the limitation on a folder, clients call the folder's [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method.</span></span> 
  
<span data-ttu-id="62d50-166">テーブルで制限を使用する方法については、「[制限につい](about-restrictions.md)て」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="62d50-166">For information about how to use restrictions with tables, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="62d50-167">関連項目</span><span class="sxs-lookup"><span data-stu-id="62d50-167">See also</span></span>



[<span data-ttu-id="62d50-168">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="62d50-168">SAndRestriction</span></span>](sandrestriction.md)
  
[<span data-ttu-id="62d50-169">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="62d50-169">SBitMaskRestriction</span></span>](sbitmaskrestriction.md)
  
[<span data-ttu-id="62d50-170">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="62d50-170">SCommentRestriction</span></span>](scommentrestriction.md)
  
[<span data-ttu-id="62d50-171">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="62d50-171">SComparePropsRestriction</span></span>](scomparepropsrestriction.md)
  
[<span data-ttu-id="62d50-172">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="62d50-172">SContentRestriction</span></span>](scontentrestriction.md)
  
[<span data-ttu-id="62d50-173">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="62d50-173">SExistRestriction</span></span>](sexistrestriction.md)
  
[<span data-ttu-id="62d50-174">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="62d50-174">SNotRestriction</span></span>](snotrestriction.md)
  
[<span data-ttu-id="62d50-175">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="62d50-175">SOrRestriction</span></span>](sorrestriction.md)
  
[<span data-ttu-id="62d50-176">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="62d50-176">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="62d50-177">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="62d50-177">SSizeRestriction</span></span>](ssizerestriction.md)
  
[<span data-ttu-id="62d50-178">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="62d50-178">SSubRestriction</span></span>](ssubrestriction.md)


[<span data-ttu-id="62d50-179">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="62d50-179">MAPI Structures</span></span>](mapi-structures.md)

