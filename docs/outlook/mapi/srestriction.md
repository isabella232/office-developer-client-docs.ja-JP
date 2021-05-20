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
# <a name="srestriction"></a><span data-ttu-id="e5206-103">SRestriction</span><span class="sxs-lookup"><span data-stu-id="e5206-103">SRestriction</span></span>

  
  
<span data-ttu-id="e5206-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e5206-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e5206-105">テーブルのビューを特定の行に制限するフィルターについて説明します。</span><span class="sxs-lookup"><span data-stu-id="e5206-105">Describes a filter for limiting the view of a table to particular rows.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e5206-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="e5206-106">Header file:</span></span>  <br/> |<span data-ttu-id="e5206-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e5206-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="e5206-108">Members</span><span class="sxs-lookup"><span data-stu-id="e5206-108">Members</span></span>

 <span data-ttu-id="e5206-109">**rt**</span><span class="sxs-lookup"><span data-stu-id="e5206-109">**rt**</span></span>
  
> <span data-ttu-id="e5206-110">制限の種類。</span><span class="sxs-lookup"><span data-stu-id="e5206-110">The restriction type.</span></span> <span data-ttu-id="e5206-111">指定できる値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="e5206-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="e5206-112">RES_AND</span><span class="sxs-lookup"><span data-stu-id="e5206-112">RES_AND</span></span> 
  
> <span data-ttu-id="e5206-113">**AND 制限**。これは、ビットワイズ **AND** 操作を制限に適用します。</span><span class="sxs-lookup"><span data-stu-id="e5206-113">An **AND** restriction, which applies a bitwise **AND** operation to a restriction.</span></span> 
    
<span data-ttu-id="e5206-114">RES_BITMASK</span><span class="sxs-lookup"><span data-stu-id="e5206-114">RES_BITMASK</span></span> 
  
> <span data-ttu-id="e5206-115">ビットマスクの制限 。これは、プロパティ値にビットマスクを適用します。</span><span class="sxs-lookup"><span data-stu-id="e5206-115">A bitmask restriction, which applies a bitmask to a property value.</span></span>
    
<span data-ttu-id="e5206-116">RES_COMMENT</span><span class="sxs-lookup"><span data-stu-id="e5206-116">RES_COMMENT</span></span> 
  
> <span data-ttu-id="e5206-117">コメントの制限。コメントを制限に関連付ける。</span><span class="sxs-lookup"><span data-stu-id="e5206-117">A comment restriction, which associates a comment with a restriction.</span></span>
    
<span data-ttu-id="e5206-118">RES_COMPAREPROPS</span><span class="sxs-lookup"><span data-stu-id="e5206-118">RES_COMPAREPROPS</span></span> 
  
> <span data-ttu-id="e5206-119">2 つのプロパティ値を比較するプロパティ比較の制限。</span><span class="sxs-lookup"><span data-stu-id="e5206-119">A property comparison restriction, which compares two property values.</span></span>
    
<span data-ttu-id="e5206-120">RES_CONTENT</span><span class="sxs-lookup"><span data-stu-id="e5206-120">RES_CONTENT</span></span> 
  
> <span data-ttu-id="e5206-121">特定のコンテンツのプロパティ値を検索するコンテンツ制限。</span><span class="sxs-lookup"><span data-stu-id="e5206-121">A content restriction, which searches a property value for specific content.</span></span>
    
<span data-ttu-id="e5206-122">RES_EXIST</span><span class="sxs-lookup"><span data-stu-id="e5206-122">RES_EXIST</span></span> 
  
> <span data-ttu-id="e5206-123">プロパティがサポートされているかどうかを決定する存在制限。</span><span class="sxs-lookup"><span data-stu-id="e5206-123">An exist restriction, which determines whether a property is supported.</span></span>
    
<span data-ttu-id="e5206-124">RES_NOT</span><span class="sxs-lookup"><span data-stu-id="e5206-124">RES_NOT</span></span> 
  
> <span data-ttu-id="e5206-125">NOT **制限** 。これは、論理 NOT 操作 **を制限** に適用します。</span><span class="sxs-lookup"><span data-stu-id="e5206-125">A **NOT** restriction, which applies a logical **NOT** operation to a restriction.</span></span> 
    
<span data-ttu-id="e5206-126">RES_OR</span><span class="sxs-lookup"><span data-stu-id="e5206-126">RES_OR</span></span> 
  
> <span data-ttu-id="e5206-127">論理 **OR** 操作を制限に適用 **する OR** 制限。</span><span class="sxs-lookup"><span data-stu-id="e5206-127">An **OR** restriction, which applies a logical **OR** operation to a restriction.</span></span> 
    
<span data-ttu-id="e5206-128">RES_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="e5206-128">RES_PROPERTY</span></span> 
  
> <span data-ttu-id="e5206-129">プロパティの値が特定の値と一致するかどうかを決定するプロパティ制限。</span><span class="sxs-lookup"><span data-stu-id="e5206-129">A property restriction, which determines whether a property value matches a particular value.</span></span>
    
<span data-ttu-id="e5206-130">RES_SIZE</span><span class="sxs-lookup"><span data-stu-id="e5206-130">RES_SIZE</span></span> 
  
> <span data-ttu-id="e5206-131">プロパティの値が特定のサイズであるかどうかを決定するサイズ制限。</span><span class="sxs-lookup"><span data-stu-id="e5206-131">A size restriction, which determines whether a property value is a particular size.</span></span>
    
<span data-ttu-id="e5206-132">RES_SUBRESTRICTION</span><span class="sxs-lookup"><span data-stu-id="e5206-132">RES_SUBRESTRICTION</span></span> 
  
> <span data-ttu-id="e5206-133">メッセージの添付ファイルまたは受信者に制限を適用するサブオブジェクト制限。</span><span class="sxs-lookup"><span data-stu-id="e5206-133">A sub-object restriction, which applies a restriction to a message's attachments or recipients.</span></span>
    
 <span data-ttu-id="e5206-134">**res**</span><span class="sxs-lookup"><span data-stu-id="e5206-134">**res**</span></span>
  
> <span data-ttu-id="e5206-135">適用するフィルターを記述する制限構造の一体。</span><span class="sxs-lookup"><span data-stu-id="e5206-135">Union of restriction structures describing the filter to be applied.</span></span> <span data-ttu-id="e5206-136">**res** メンバーに含まれる特定の構造は **、rt** メンバーの値によって異なります。</span><span class="sxs-lookup"><span data-stu-id="e5206-136">The specific structure included in the **res** member depends on the value of the **rt** member.</span></span> <span data-ttu-id="e5206-137">制限の種類と構造のマッピングを次の表に示します。</span><span class="sxs-lookup"><span data-stu-id="e5206-137">The mapping between restriction type and structure is listed in the following table.</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="e5206-138">**制限の種類**</span><span class="sxs-lookup"><span data-stu-id="e5206-138">**Restriction type**</span></span> <br/> |<span data-ttu-id="e5206-139">**制限構造**</span><span class="sxs-lookup"><span data-stu-id="e5206-139">**Restriction structure**</span></span> <br/> |
|<span data-ttu-id="e5206-140">RES_AND</span><span class="sxs-lookup"><span data-stu-id="e5206-140">RES_AND</span></span>  <br/> |[<span data-ttu-id="e5206-141">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="e5206-141">SAndRestriction</span></span>](sandrestriction.md) <br/> |
|<span data-ttu-id="e5206-142">RES_BITMASK</span><span class="sxs-lookup"><span data-stu-id="e5206-142">RES_BITMASK</span></span>  <br/> |[<span data-ttu-id="e5206-143">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="e5206-143">SBitMaskRestriction</span></span>](sbitmaskrestriction.md) <br/> |
|<span data-ttu-id="e5206-144">RES_COMMENT</span><span class="sxs-lookup"><span data-stu-id="e5206-144">RES_COMMENT</span></span>  <br/> |[<span data-ttu-id="e5206-145">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="e5206-145">SCommentRestriction</span></span>](scommentrestriction.md) <br/> |
|<span data-ttu-id="e5206-146">RES_COMPAREPROPS</span><span class="sxs-lookup"><span data-stu-id="e5206-146">RES_COMPAREPROPS</span></span>  <br/> |[<span data-ttu-id="e5206-147">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="e5206-147">SComparePropsRestriction</span></span>](scomparepropsrestriction.md) <br/> |
|<span data-ttu-id="e5206-148">RES_CONTENT</span><span class="sxs-lookup"><span data-stu-id="e5206-148">RES_CONTENT</span></span>  <br/> |[<span data-ttu-id="e5206-149">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="e5206-149">SContentRestriction</span></span>](scontentrestriction.md) <br/> |
|<span data-ttu-id="e5206-150">RES_EXIST</span><span class="sxs-lookup"><span data-stu-id="e5206-150">RES_EXIST</span></span>  <br/> |[<span data-ttu-id="e5206-151">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="e5206-151">SExistRestriction</span></span>](sexistrestriction.md) <br/> |
|<span data-ttu-id="e5206-152">RES_NOT</span><span class="sxs-lookup"><span data-stu-id="e5206-152">RES_NOT</span></span>  <br/> |[<span data-ttu-id="e5206-153">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="e5206-153">SNotRestriction</span></span>](snotrestriction.md) <br/> |
|<span data-ttu-id="e5206-154">RES_OR</span><span class="sxs-lookup"><span data-stu-id="e5206-154">RES_OR</span></span>  <br/> |[<span data-ttu-id="e5206-155">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="e5206-155">SOrRestriction</span></span>](sorrestriction.md) <br/> |
|<span data-ttu-id="e5206-156">RES_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="e5206-156">RES_PROPERTY</span></span>  <br/> |[<span data-ttu-id="e5206-157">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="e5206-157">SPropertyRestriction</span></span>](spropertyrestriction.md) <br/> |
|<span data-ttu-id="e5206-158">RES_SIZE</span><span class="sxs-lookup"><span data-stu-id="e5206-158">RES_SIZE</span></span>  <br/> |[<span data-ttu-id="e5206-159">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="e5206-159">SSizeRestriction</span></span>](ssizerestriction.md) <br/> |
|<span data-ttu-id="e5206-160">RES_SUBRESTRICTION</span><span class="sxs-lookup"><span data-stu-id="e5206-160">RES_SUBRESTRICTION</span></span>  <br/> |[<span data-ttu-id="e5206-161">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="e5206-161">SSubRestriction</span></span>](ssubrestriction.md) <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e5206-162">注釈</span><span class="sxs-lookup"><span data-stu-id="e5206-162">Remarks</span></span>

<span data-ttu-id="e5206-163">クライアントは **、SRestriction** 構造を使用して、テーブルのビュー内の行の数と種類を制限し、フォルダー内の特定のメッセージを検索します。</span><span class="sxs-lookup"><span data-stu-id="e5206-163">Clients use an **SRestriction** structure to limit the number and type of rows in their view of a table and to search for specific messages in a folder.</span></span> <span data-ttu-id="e5206-164">テーブルに制限を適用するには、クライアントは [IMAPITable::Restrict](imapitable-restrict.md) または [IMAPITable::FindRow を呼び出します](imapitable-findrow.md)。</span><span class="sxs-lookup"><span data-stu-id="e5206-164">To impose the limitation on a table, clients call either [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> <span data-ttu-id="e5206-165">フォルダーに制限を適用するには、クライアントはフォルダーの [IMAPIContainer::SetSearchCriteria メソッドを呼び出](imapicontainer-setsearchcriteria.md) します。</span><span class="sxs-lookup"><span data-stu-id="e5206-165">To impose the limitation on a folder, clients call the folder's [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method.</span></span> 
  
<span data-ttu-id="e5206-166">テーブルで制限を使用する方法については、「制限について [」を参照してください](about-restrictions.md)。</span><span class="sxs-lookup"><span data-stu-id="e5206-166">For information about how to use restrictions with tables, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e5206-167">関連項目</span><span class="sxs-lookup"><span data-stu-id="e5206-167">See also</span></span>



[<span data-ttu-id="e5206-168">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="e5206-168">SAndRestriction</span></span>](sandrestriction.md)
  
[<span data-ttu-id="e5206-169">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="e5206-169">SBitMaskRestriction</span></span>](sbitmaskrestriction.md)
  
[<span data-ttu-id="e5206-170">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="e5206-170">SCommentRestriction</span></span>](scommentrestriction.md)
  
[<span data-ttu-id="e5206-171">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="e5206-171">SComparePropsRestriction</span></span>](scomparepropsrestriction.md)
  
[<span data-ttu-id="e5206-172">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="e5206-172">SContentRestriction</span></span>](scontentrestriction.md)
  
[<span data-ttu-id="e5206-173">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="e5206-173">SExistRestriction</span></span>](sexistrestriction.md)
  
[<span data-ttu-id="e5206-174">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="e5206-174">SNotRestriction</span></span>](snotrestriction.md)
  
[<span data-ttu-id="e5206-175">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="e5206-175">SOrRestriction</span></span>](sorrestriction.md)
  
[<span data-ttu-id="e5206-176">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="e5206-176">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="e5206-177">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="e5206-177">SSizeRestriction</span></span>](ssizerestriction.md)
  
[<span data-ttu-id="e5206-178">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="e5206-178">SSubRestriction</span></span>](ssubrestriction.md)


[<span data-ttu-id="e5206-179">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="e5206-179">MAPI Structures</span></span>](mapi-structures.md)

