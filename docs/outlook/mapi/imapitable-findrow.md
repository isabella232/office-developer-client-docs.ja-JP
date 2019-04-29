---
title: IMAPITableFindRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.FindRow
api_type:
- COM
ms.assetid: 6511368c-9777-497e-9eea-cf390c04b92e
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a5364af229721d101f38d2f054f528169b48c09e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429573"
---
# <a name="imapitablefindrow"></a><span data-ttu-id="e9c87-103">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="e9c87-103">IMAPITable::FindRow</span></span>

  
  
<span data-ttu-id="e9c87-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e9c87-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e9c87-105">特定の検索条件に一致するテーブル内の次の行を検索し、その行にカーソルを移動します。</span><span class="sxs-lookup"><span data-stu-id="e9c87-105">Finds the next row in a table that matches specific search criteria and moves the cursor to that row.</span></span>
  
```cpp
HRESULT FindRow(
LPSRestriction lpRestriction,
BOOKMARK BkOrigin,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="e9c87-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e9c87-106">Parameters</span></span>

 <span data-ttu-id="e9c87-107">_lpRestriction_</span><span class="sxs-lookup"><span data-stu-id="e9c87-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="e9c87-108">順番検索条件を記述する[srestriction](srestriction.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e9c87-108">[in] A pointer to an [SRestriction](srestriction.md) structure that describes the search criteria.</span></span> 
    
 <span data-ttu-id="e9c87-109">_BkOrigin_</span><span class="sxs-lookup"><span data-stu-id="e9c87-109">_BkOrigin_</span></span>
  
> <span data-ttu-id="e9c87-110">順番**FindRow**が検索を開始する行を識別するブックマーク。</span><span class="sxs-lookup"><span data-stu-id="e9c87-110">[in] A bookmark identifying the row where **FindRow** should begin its search.</span></span> <span data-ttu-id="e9c87-111">ブックを作成するには、 [IMAPITable:: createbookmark](imapitable-createbookmark.md)メソッドを使用するか、次の定義済みの値のいずれかを渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="e9c87-111">A bookmark can be created using the [IMAPITable::CreateBookmark](imapitable-createbookmark.md) method, or one of the following predefined values can be passed.</span></span> 
    
<span data-ttu-id="e9c87-112">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="e9c87-112">BOOKMARK_BEGINNING</span></span> 
  
> <span data-ttu-id="e9c87-113">表の先頭から検索します。</span><span class="sxs-lookup"><span data-stu-id="e9c87-113">Searches from the beginning of the table.</span></span> 
    
<span data-ttu-id="e9c87-114">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="e9c87-114">BOOKMARK_CURRENT</span></span> 
  
> <span data-ttu-id="e9c87-115">カーソルが置かれているテーブルの行から検索します。</span><span class="sxs-lookup"><span data-stu-id="e9c87-115">Searches from the row in the table where the cursor is located.</span></span> 
    
<span data-ttu-id="e9c87-116">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="e9c87-116">BOOKMARK_END</span></span> 
  
> <span data-ttu-id="e9c87-117">表の末尾から検索します。</span><span class="sxs-lookup"><span data-stu-id="e9c87-117">Searches from the end of the table.</span></span> 
    
 <span data-ttu-id="e9c87-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e9c87-118">_ulFlags_</span></span>
  
> <span data-ttu-id="e9c87-119">順番検索の方向を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="e9c87-119">[in] A bitmask of flags that controls the direction of the search.</span></span> <span data-ttu-id="e9c87-120">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="e9c87-120">The following flag can be set:</span></span>
    
<span data-ttu-id="e9c87-121">DIR_BACKWARD</span><span class="sxs-lookup"><span data-stu-id="e9c87-121">DIR_BACKWARD</span></span> 
  
> <span data-ttu-id="e9c87-122">ブックマークで指定された行から後方へ検索します。</span><span class="sxs-lookup"><span data-stu-id="e9c87-122">Searches backward from the row identified by the bookmark.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e9c87-123">戻り値</span><span class="sxs-lookup"><span data-stu-id="e9c87-123">Return value</span></span>

<span data-ttu-id="e9c87-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="e9c87-124">S_OK</span></span> 
  
> <span data-ttu-id="e9c87-125">検索操作が正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="e9c87-125">The find operation was successful.</span></span>
    
<span data-ttu-id="e9c87-126">MAPI_E_INVALID_BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="e9c87-126">MAPI_E_INVALID_BOOKMARK</span></span> 
  
> <span data-ttu-id="e9c87-127">_BkOrigin_パラメーターのブックマークは、削除されたか、要求された最後の行を超えているため、無効です。</span><span class="sxs-lookup"><span data-stu-id="e9c87-127">The bookmark in the  _BkOrigin_ parameter is invalid because it has been removed or because it is beyond the last row requested.</span></span> 
    
<span data-ttu-id="e9c87-128">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="e9c87-128">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="e9c87-129">制限に一致する行が見つかりませんでした。</span><span class="sxs-lookup"><span data-stu-id="e9c87-129">No rows were found that matched the restriction.</span></span>
    
<span data-ttu-id="e9c87-130">MAPI_W_POSITION_CHANGED</span><span class="sxs-lookup"><span data-stu-id="e9c87-130">MAPI_W_POSITION_CHANGED</span></span>
  
> <span data-ttu-id="e9c87-131">呼び出しは成功しましたが、操作に使用されたブックマークは、最後に使用されたときと同じ行に設定されていません。ブックマークが使用されていない場合は、作成時と同じ位置になりません。</span><span class="sxs-lookup"><span data-stu-id="e9c87-131">The call succeeded, but the bookmark used in the operation is no longer set at the same row as when it was last used; if the bookmark has not been used, it is no longer in the same position as when it was created.</span></span> <span data-ttu-id="e9c87-132">この警告が返された場合、呼び出しは正常に処理されます。</span><span class="sxs-lookup"><span data-stu-id="e9c87-132">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="e9c87-133">この警告をテストするには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="e9c87-133">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="e9c87-134">「[エラー処理にマクロを使用する](using-macros-for-error-handling.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e9c87-134">See [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e9c87-135">注釈</span><span class="sxs-lookup"><span data-stu-id="e9c87-135">Remarks</span></span>

<span data-ttu-id="e9c87-136">**IMAPITable:: FindRow**メソッドは、表の最初の行を検索し、 _lpRestriction_パラメーターで指定された**srestriction**構造で記述された一連の検索条件に一致するようにします。</span><span class="sxs-lookup"><span data-stu-id="e9c87-136">The **IMAPITable::FindRow** method locates the first row in the table to match a set of search criteria described in the **SRestriction** structure pointed to by the  _lpRestriction_ parameter.</span></span> 
  
<span data-ttu-id="e9c87-137">通常、 **FindRow**は指定されたブックマークから前方へ検索します。</span><span class="sxs-lookup"><span data-stu-id="e9c87-137">Usually, **FindRow** searches forward from the specified bookmark.</span></span> <span data-ttu-id="e9c87-138">呼び出し元は、 _ulflags_パラメーターに DIR_BACKWARD フラグを設定することによって、ブックマークから後方に移動するように検索を設定できます。</span><span class="sxs-lookup"><span data-stu-id="e9c87-138">The caller can set the search to move backward from the bookmark by setting the DIR_BACKWARD flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="e9c87-139">前方検索は現在のブックマークから開始されます。後方検索は、ブックマークの前の行から開始されます。</span><span class="sxs-lookup"><span data-stu-id="e9c87-139">Searching forward starts from the current bookmark; searching backward starts from the row prior to the bookmark.</span></span> <span data-ttu-id="e9c87-140">検索の終了位置は、制限を満たす最初の行の直前にあります。</span><span class="sxs-lookup"><span data-stu-id="e9c87-140">The end position of the search is just before the first row found that satisfied the restriction.</span></span> 
  
<span data-ttu-id="e9c87-141">_BkOrigin_パラメーターで指定されたブックマークによって参照されている行がテーブルに存在しない場合、テーブルでブックマークの新しい位置を設定できない場合、 **FindRow**は MAPI_E_INVALID_BOOKMARK を返します。</span><span class="sxs-lookup"><span data-stu-id="e9c87-141">If the row pointed to by the bookmark in the  _BkOrigin_ parameter no longer exists in the table and the table cannot establish a new position for the bookmark, **FindRow** returns MAPI_E_INVALID_BOOKMARK.</span></span> <span data-ttu-id="e9c87-142">_BkOrigin_によって参照される行が存在しなくなり、テーブルがブックマークの新しい位置を確立できる場合、 **FindRow**は MAPI_W_POSITION_CHANGED を返します。</span><span class="sxs-lookup"><span data-stu-id="e9c87-142">If the row pointed to by  _BkOrigin_ no longer exists and the table is able to establish a new position for the bookmark, **FindRow** returns MAPI_W_POSITION_CHANGED.</span></span> 
  
<span data-ttu-id="e9c87-143">_BkOrigin_で渡されたブックマークが BOOKMARK_BEGINNING または BOOKMARK_END の\*\*\*\* いずれかである場合、一致する行が見つからない場合は MAPI_E_NOT_FOUND が返されます。</span><span class="sxs-lookup"><span data-stu-id="e9c87-143">If the bookmark passed in  _BkOrigin_ is either BOOKMARK_BEGINNING or BOOKMARK_END, **FindRow** returns MAPI_E_NOT_FOUND if no matching row is found.</span></span> <span data-ttu-id="e9c87-144">_BkOrigin_で使用されているブックマークが BOOKMARK_CURRENT の場合、 **FindRow**は MAPI_W_POSITION_CHANGED を返すことができますが、常に現在のカーソル位置があるため、MAPI_E_INVALID_BOOKMARK は返しません。</span><span class="sxs-lookup"><span data-stu-id="e9c87-144">If the bookmark used in  _BkOrigin_ is BOOKMARK_CURRENT, **FindRow** can return MAPI_W_POSITION_CHANGED but not MAPI_E_INVALID_BOOKMARK because there is always a current cursor position.</span></span> 
  
<span data-ttu-id="e9c87-145">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) プロパティ列はすべてのテーブルに必要であり、PR_INSTANCE_KEY に基づいて行をシークする呼び出しをサポートするには、 **FindRow**のすべての実装が必要です。</span><span class="sxs-lookup"><span data-stu-id="e9c87-145">The **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property column is required for all tables, and all implementations of **FindRow** are required to support calls seeking a row based on PR_INSTANCE_KEY.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="e9c87-146">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="e9c87-146">Notes to implementers</span></span>

<span data-ttu-id="e9c87-147">**FindRow**によって実行されるプレフィックス検索の種類は、検索がテーブル組織と同じ方向にある場合にのみ役立ちます。</span><span class="sxs-lookup"><span data-stu-id="e9c87-147">The type of prefix searching performed by **FindRow** is only useful when the search follows the same direction as the table organization.</span></span> <span data-ttu-id="e9c87-148">必要な動作を実現するために、プロパティ制限構造で渡された**RELOP_GE**によって暗黙的に指定された比較関数は、テーブルの並べ替え順序を基にした比較関数と同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9c87-148">In order to achieve the required behavior, the comparison function implied by the **RELOP_GE** passed in the property restriction structure should be the same comparison function on which the table sort order is based.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e9c87-149">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="e9c87-149">Notes to callers</span></span>

<span data-ttu-id="e9c87-150">**FindRow**を使用すると、ユーザーが入力した文字列 (特にアドレスダイアログボックス内のリストボックス) に基づいたスクロールをサポートできます。</span><span class="sxs-lookup"><span data-stu-id="e9c87-150">You can use **FindRow** to support scrolling based on strings typed in by the user, especially in list boxes within address dialog boxes.</span></span> <span data-ttu-id="e9c87-151">この種類のスクロールでは、ユーザーは必要な文字列値のプレフィックスを徐々に入力し、 **FindRow**の呼び出しを定期的に発行して、プレフィックスに一致する最初の行にジャンプできます。</span><span class="sxs-lookup"><span data-stu-id="e9c87-151">In this type of scrolling, users enter progressively longer prefixes of a desired string value, and you can periodically issue a **FindRow** call to jump to the first row that matches the prefix.</span></span> <span data-ttu-id="e9c87-152">カーソルジャンプの方向は、検索を実行する方向によって決まります。</span><span class="sxs-lookup"><span data-stu-id="e9c87-152">Which direction the cursor jumps depends on which direction the search is set to run.</span></span> 
  
<span data-ttu-id="e9c87-153">**FindRow**を使用するには、ブックマークが設定されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9c87-153">To use **FindRow**, a bookmark must be set.</span></span> <span data-ttu-id="e9c87-154">文字列検索は、すべてのブックマーク (現在の位置と表の開始および終了を示す事前設定されたブックマークを含む) から開始できます。</span><span class="sxs-lookup"><span data-stu-id="e9c87-154">The string search can originate from any bookmark, including from the preset bookmarks indicating the current position and the beginning and end of the table.</span></span> <span data-ttu-id="e9c87-155">テーブルに多数の行がある場合、検索操作に時間がかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="e9c87-155">If there are a large number of rows in the table, the search operation can be slow.</span></span>
  
<span data-ttu-id="e9c87-156">次のようにスクロールする文字列プレフィックスを検索するには、制限を使用します。</span><span class="sxs-lookup"><span data-stu-id="e9c87-156">Use a restriction to find a string prefix for scrolling as follows.</span></span> <span data-ttu-id="e9c87-157">昇順で並べ替えられた列の前方検索に対して、降順に並べ替えられた列の後方検索の場合は、 _lpRestriction_パラメータのプロパティ制限構造をリレーションシップ**RELOP_GE**に渡して、適切な_タグ_ \*\*\*\* __ とプレフィックスの形式を使用します。</span><span class="sxs-lookup"><span data-stu-id="e9c87-157">For forward searching on a column sorted in ascending order and for backward searching on a column sorted in descending order, pass a property restriction structure in the  _lpRestriction_ parameter with the relation **RELOP_GE** and the appropriate property tag and prefix, using the format  _tag_ **GE** _prefix_.</span></span> 
  
<span data-ttu-id="e9c87-158">制限構造を使用してフィルターを指定する方法の詳細については、「[制限につい](about-restrictions.md)て」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e9c87-158">For more information about using restriction structures to specify a filter, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e9c87-159">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="e9c87-159">MFCMAPI reference</span></span>

<span data-ttu-id="e9c87-160">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e9c87-160">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e9c87-161">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="e9c87-161">**File**</span></span>|<span data-ttu-id="e9c87-162">**関数**</span><span class="sxs-lookup"><span data-stu-id="e9c87-162">**Function**</span></span>|<span data-ttu-id="e9c87-163">**コメント**</span><span class="sxs-lookup"><span data-stu-id="e9c87-163">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e9c87-164">ContentsTableListCtrl</span><span class="sxs-lookup"><span data-stu-id="e9c87-164">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="e9c87-165">dwthreadの loadtable</span><span class="sxs-lookup"><span data-stu-id="e9c87-165">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="e9c87-166">mfcmapi は、 **IMAPITable:: FindRow**メソッドを使用して、制限に一致する行を検索します。</span><span class="sxs-lookup"><span data-stu-id="e9c87-166">MFCMAPI uses the **IMAPITable::FindRow** method to find rows which match a restriction.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e9c87-167">関連項目</span><span class="sxs-lookup"><span data-stu-id="e9c87-167">See also</span></span>



[<span data-ttu-id="e9c87-168">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="e9c87-168">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="e9c87-169">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="e9c87-169">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="e9c87-170">SRestriction</span><span class="sxs-lookup"><span data-stu-id="e9c87-170">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="e9c87-171">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e9c87-171">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


<span data-ttu-id="e9c87-172">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="e9c87-172">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

