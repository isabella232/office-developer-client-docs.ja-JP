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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9748229799641d62b1649491c432f10164b49192
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803998"
---
# <a name="srestriction"></a><span data-ttu-id="54c27-103">SRestriction</span><span class="sxs-lookup"><span data-stu-id="54c27-103">SRestriction</span></span>

  
  
<span data-ttu-id="54c27-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="54c27-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="54c27-105">特定の行をテーブルの表示を制限するフィルターについて説明します。</span><span class="sxs-lookup"><span data-stu-id="54c27-105">Describes a filter for limiting the view of a table to particular rows.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="54c27-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="54c27-106">Header file:</span></span>  <br/> |<span data-ttu-id="54c27-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="54c27-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="54c27-108">Members</span><span class="sxs-lookup"><span data-stu-id="54c27-108">Members</span></span>

 <span data-ttu-id="54c27-109">**rt**</span><span class="sxs-lookup"><span data-stu-id="54c27-109">**rt**</span></span>
  
> <span data-ttu-id="54c27-110">制限の種類です。</span><span class="sxs-lookup"><span data-stu-id="54c27-110">The restriction type.</span></span> <span data-ttu-id="54c27-111">使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="54c27-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="54c27-112">RES_AND</span><span class="sxs-lookup"><span data-stu-id="54c27-112">RES_AND</span></span> 
  
> <span data-ttu-id="54c27-113">ビットごとの**AND**演算が適用される制限**と**制限します。</span><span class="sxs-lookup"><span data-stu-id="54c27-113">An **AND** restriction, which applies a bitwise **AND** operation to a restriction.</span></span> 
    
<span data-ttu-id="54c27-114">RES_BITMASK</span><span class="sxs-lookup"><span data-stu-id="54c27-114">RES_BITMASK</span></span> 
  
> <span data-ttu-id="54c27-115">ビットマスク制限ビットマスク プロパティの値が適用されます。</span><span class="sxs-lookup"><span data-stu-id="54c27-115">A bitmask restriction, which applies a bitmask to a property value.</span></span>
    
<span data-ttu-id="54c27-116">RES_COMMENT</span><span class="sxs-lookup"><span data-stu-id="54c27-116">RES_COMMENT</span></span> 
  
> <span data-ttu-id="54c27-117">コメント制限、制限付きのコメントを関連付けます。</span><span class="sxs-lookup"><span data-stu-id="54c27-117">A comment restriction, which associates a comment with a restriction.</span></span>
    
<span data-ttu-id="54c27-118">RES_COMPAREPROPS</span><span class="sxs-lookup"><span data-stu-id="54c27-118">RES_COMPAREPROPS</span></span> 
  
> <span data-ttu-id="54c27-119">2 つのプロパティ値を比較する、プロパティの比較制限です。</span><span class="sxs-lookup"><span data-stu-id="54c27-119">A property comparison restriction, which compares two property values.</span></span>
    
<span data-ttu-id="54c27-120">RES_CONTENT</span><span class="sxs-lookup"><span data-stu-id="54c27-120">RES_CONTENT</span></span> 
  
> <span data-ttu-id="54c27-121">コンテンツ制限、特定のコンテンツのプロパティ値を検索します。</span><span class="sxs-lookup"><span data-stu-id="54c27-121">A content restriction, which searches a property value for specific content.</span></span>
    
<span data-ttu-id="54c27-122">RES_EXIST</span><span class="sxs-lookup"><span data-stu-id="54c27-122">RES_EXIST</span></span> 
  
> <span data-ttu-id="54c27-123">プロパティがサポートされているかどうかを決定する既存の制限します。</span><span class="sxs-lookup"><span data-stu-id="54c27-123">An exist restriction, which determines whether a property is supported.</span></span>
    
<span data-ttu-id="54c27-124">RES_NOT</span><span class="sxs-lookup"><span data-stu-id="54c27-124">RES_NOT</span></span> 
  
> <span data-ttu-id="54c27-125">**しない**制限、制約を論理**NOT**演算を適用します。</span><span class="sxs-lookup"><span data-stu-id="54c27-125">A **NOT** restriction, which applies a logical **NOT** operation to a restriction.</span></span> 
    
<span data-ttu-id="54c27-126">RES_OR</span><span class="sxs-lookup"><span data-stu-id="54c27-126">RES_OR</span></span> 
  
> <span data-ttu-id="54c27-127">**または**制限、制約を論理**OR**演算が適用されます。</span><span class="sxs-lookup"><span data-stu-id="54c27-127">An **OR** restriction, which applies a logical **OR** operation to a restriction.</span></span> 
    
<span data-ttu-id="54c27-128">RES_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="54c27-128">RES_PROPERTY</span></span> 
  
> <span data-ttu-id="54c27-129">プロパティ制限プロパティの値が特定の値と一致するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="54c27-129">A property restriction, which determines whether a property value matches a particular value.</span></span>
    
<span data-ttu-id="54c27-130">RES_SIZE</span><span class="sxs-lookup"><span data-stu-id="54c27-130">RES_SIZE</span></span> 
  
> <span data-ttu-id="54c27-131">サイズの制限、プロパティの値が特定のサイズであるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="54c27-131">A size restriction, which determines whether a property value is a particular size.</span></span>
    
<span data-ttu-id="54c27-132">RES_SUBRESTRICTION</span><span class="sxs-lookup"><span data-stu-id="54c27-132">RES_SUBRESTRICTION</span></span> 
  
> <span data-ttu-id="54c27-133">サブ オブジェクト制限メッセージの添付ファイル、または受信者に制限を適用します。</span><span class="sxs-lookup"><span data-stu-id="54c27-133">A sub-object restriction, which applies a restriction to a message's attachments or recipients.</span></span>
    
 <span data-ttu-id="54c27-134">**res**</span><span class="sxs-lookup"><span data-stu-id="54c27-134">**res**</span></span>
  
> <span data-ttu-id="54c27-135">制限構造のフィルターを記述するのに適用する共用体です。</span><span class="sxs-lookup"><span data-stu-id="54c27-135">Union of restriction structures describing the filter to be applied.</span></span> <span data-ttu-id="54c27-136">**Res**のメンバーに含まれている特定の構造は、 **rt**のメンバーの値によって異なります。</span><span class="sxs-lookup"><span data-stu-id="54c27-136">The specific structure included in the **res** member depends on the value of the **rt** member.</span></span> <span data-ttu-id="54c27-137">制限の種類と構造間のマッピングは、次の表に表示されます。</span><span class="sxs-lookup"><span data-stu-id="54c27-137">The mapping between restriction type and structure is listed in the following table.</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="54c27-138">**制限の種類**</span><span class="sxs-lookup"><span data-stu-id="54c27-138">**Restriction type**</span></span> <br/> |<span data-ttu-id="54c27-139">**制限構造**</span><span class="sxs-lookup"><span data-stu-id="54c27-139">**Restriction structure**</span></span> <br/> |
|<span data-ttu-id="54c27-140">RES_AND</span><span class="sxs-lookup"><span data-stu-id="54c27-140">RES_AND</span></span>  <br/> |[<span data-ttu-id="54c27-141">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="54c27-141">SAndRestriction</span></span>](sandrestriction.md) <br/> |
|<span data-ttu-id="54c27-142">RES_BITMASK</span><span class="sxs-lookup"><span data-stu-id="54c27-142">RES_BITMASK</span></span>  <br/> |[<span data-ttu-id="54c27-143">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="54c27-143">SBitMaskRestriction</span></span>](sbitmaskrestriction.md) <br/> |
|<span data-ttu-id="54c27-144">RES_COMMENT</span><span class="sxs-lookup"><span data-stu-id="54c27-144">RES_COMMENT</span></span>  <br/> |[<span data-ttu-id="54c27-145">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="54c27-145">SCommentRestriction</span></span>](scommentrestriction.md) <br/> |
|<span data-ttu-id="54c27-146">RES_COMPAREPROPS</span><span class="sxs-lookup"><span data-stu-id="54c27-146">RES_COMPAREPROPS</span></span>  <br/> |[<span data-ttu-id="54c27-147">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="54c27-147">SComparePropsRestriction</span></span>](scomparepropsrestriction.md) <br/> |
|<span data-ttu-id="54c27-148">RES_CONTENT</span><span class="sxs-lookup"><span data-stu-id="54c27-148">RES_CONTENT</span></span>  <br/> |[<span data-ttu-id="54c27-149">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="54c27-149">SContentRestriction</span></span>](scontentrestriction.md) <br/> |
|<span data-ttu-id="54c27-150">RES_EXIST</span><span class="sxs-lookup"><span data-stu-id="54c27-150">RES_EXIST</span></span>  <br/> |[<span data-ttu-id="54c27-151">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="54c27-151">SExistRestriction</span></span>](sexistrestriction.md) <br/> |
|<span data-ttu-id="54c27-152">RES_NOT</span><span class="sxs-lookup"><span data-stu-id="54c27-152">RES_NOT</span></span>  <br/> |[<span data-ttu-id="54c27-153">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="54c27-153">SNotRestriction</span></span>](snotrestriction.md) <br/> |
|<span data-ttu-id="54c27-154">RES_OR</span><span class="sxs-lookup"><span data-stu-id="54c27-154">RES_OR</span></span>  <br/> |[<span data-ttu-id="54c27-155">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="54c27-155">SOrRestriction</span></span>](sorrestriction.md) <br/> |
|<span data-ttu-id="54c27-156">RES_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="54c27-156">RES_PROPERTY</span></span>  <br/> |[<span data-ttu-id="54c27-157">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="54c27-157">SPropertyRestriction</span></span>](spropertyrestriction.md) <br/> |
|<span data-ttu-id="54c27-158">RES_SIZE</span><span class="sxs-lookup"><span data-stu-id="54c27-158">RES_SIZE</span></span>  <br/> |[<span data-ttu-id="54c27-159">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="54c27-159">SSizeRestriction</span></span>](ssizerestriction.md) <br/> |
|<span data-ttu-id="54c27-160">RES_SUBRESTRICTION</span><span class="sxs-lookup"><span data-stu-id="54c27-160">RES_SUBRESTRICTION</span></span>  <br/> |[<span data-ttu-id="54c27-161">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="54c27-161">SSubRestriction</span></span>](ssubrestriction.md) <br/> |
   
## <a name="remarks"></a><span data-ttu-id="54c27-162">注釈</span><span class="sxs-lookup"><span data-stu-id="54c27-162">Remarks</span></span>

<span data-ttu-id="54c27-163">クライアントは、数とそれぞれのテーブルのビュー内の行の種類を制限して、フォルダー内の特定のメッセージを検索するに**SRestriction**構造体を使用します。</span><span class="sxs-lookup"><span data-stu-id="54c27-163">Clients use an **SRestriction** structure to limit the number and type of rows in their view of a table and to search for specific messages in a folder.</span></span> <span data-ttu-id="54c27-164">テーブルの制限を適用するには、クライアントは、 [IMAPITable::Restrict](imapitable-restrict.md)または[IMAPITable::FindRow](imapitable-findrow.md)のいずれかを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="54c27-164">To impose the limitation on a table, clients call either [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> <span data-ttu-id="54c27-165">フォルダーの制限を課すには、クライアントは、フォルダーの[IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="54c27-165">To impose the limitation on a folder, clients call the folder's [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method.</span></span> 
  
<span data-ttu-id="54c27-166">テーブルの制限を使用する方法の詳細については、[制限の詳細](about-restrictions.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="54c27-166">For information about how to use restrictions with tables, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="54c27-167">関連項目</span><span class="sxs-lookup"><span data-stu-id="54c27-167">See also</span></span>



[<span data-ttu-id="54c27-168">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="54c27-168">SAndRestriction</span></span>](sandrestriction.md)
  
[<span data-ttu-id="54c27-169">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="54c27-169">SBitMaskRestriction</span></span>](sbitmaskrestriction.md)
  
[<span data-ttu-id="54c27-170">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="54c27-170">SCommentRestriction</span></span>](scommentrestriction.md)
  
[<span data-ttu-id="54c27-171">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="54c27-171">SComparePropsRestriction</span></span>](scomparepropsrestriction.md)
  
[<span data-ttu-id="54c27-172">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="54c27-172">SContentRestriction</span></span>](scontentrestriction.md)
  
[<span data-ttu-id="54c27-173">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="54c27-173">SExistRestriction</span></span>](sexistrestriction.md)
  
[<span data-ttu-id="54c27-174">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="54c27-174">SNotRestriction</span></span>](snotrestriction.md)
  
[<span data-ttu-id="54c27-175">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="54c27-175">SOrRestriction</span></span>](sorrestriction.md)
  
[<span data-ttu-id="54c27-176">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="54c27-176">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="54c27-177">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="54c27-177">SSizeRestriction</span></span>](ssizerestriction.md)
  
[<span data-ttu-id="54c27-178">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="54c27-178">SSubRestriction</span></span>](ssubrestriction.md)


[<span data-ttu-id="54c27-179">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="54c27-179">MAPI Structures</span></span>](mapi-structures.md)

