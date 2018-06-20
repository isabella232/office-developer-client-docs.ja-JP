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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: cb777074d1657a3ee5c2f1e9f70d2b304858c1b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800832"
---
# <a name="imapitablefindrow"></a><span data-ttu-id="563f6-103">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="563f6-103">IMAPITable::FindRow</span></span>

  
  
<span data-ttu-id="563f6-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="563f6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="563f6-105">特定の検索条件に一致し、その行にカーソルを移動するテーブル内の次の行を検索します。</span><span class="sxs-lookup"><span data-stu-id="563f6-105">Finds the next row in a table that matches specific search criteria and moves the cursor to that row.</span></span>
  
```cpp
HRESULT FindRow(
LPSRestriction lpRestriction,
BOOKMARK BkOrigin,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="563f6-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="563f6-106">Parameters</span></span>

 <span data-ttu-id="563f6-107">_lpRestriction_</span><span class="sxs-lookup"><span data-stu-id="563f6-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="563f6-108">[in]検索条件を記述する[SRestriction](srestriction.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="563f6-108">[in] A pointer to an [SRestriction](srestriction.md) structure that describes the search criteria.</span></span> 
    
 <span data-ttu-id="563f6-109">_BkOrigin_</span><span class="sxs-lookup"><span data-stu-id="563f6-109">_BkOrigin_</span></span>
  
> <span data-ttu-id="563f6-110">[in]**FindRow**が検索を開始する位置を示す行を識別するブックマークです。</span><span class="sxs-lookup"><span data-stu-id="563f6-110">[in] A bookmark identifying the row where **FindRow** should begin its search.</span></span> <span data-ttu-id="563f6-111">、 [IMAPITable::CreateBookmark](imapitable-createbookmark.md)メソッドを使用してブックマークを作成することができますか、次の定義済み値の 1 つ渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="563f6-111">A bookmark can be created using the [IMAPITable::CreateBookmark](imapitable-createbookmark.md) method, or one of the following predefined values can be passed.</span></span> 
    
<span data-ttu-id="563f6-112">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="563f6-112">BOOKMARK_BEGINNING</span></span> 
  
> <span data-ttu-id="563f6-113">テーブルの先頭から検索します。</span><span class="sxs-lookup"><span data-stu-id="563f6-113">Searches from the beginning of the table.</span></span> 
    
<span data-ttu-id="563f6-114">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="563f6-114">BOOKMARK_CURRENT</span></span> 
  
> <span data-ttu-id="563f6-115">カーソルが配置されているテーブルの行を検索します。</span><span class="sxs-lookup"><span data-stu-id="563f6-115">Searches from the row in the table where the cursor is located.</span></span> 
    
<span data-ttu-id="563f6-116">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="563f6-116">BOOKMARK_END</span></span> 
  
> <span data-ttu-id="563f6-117">テーブルの最後から検索します。</span><span class="sxs-lookup"><span data-stu-id="563f6-117">Searches from the end of the table.</span></span> 
    
 <span data-ttu-id="563f6-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="563f6-118">_ulFlags_</span></span>
  
> <span data-ttu-id="563f6-119">[in]検索の方向を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="563f6-119">[in] A bitmask of flags that controls the direction of the search.</span></span> <span data-ttu-id="563f6-120">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="563f6-120">The following flag can be set:</span></span>
    
<span data-ttu-id="563f6-121">DIR_BACKWARD</span><span class="sxs-lookup"><span data-stu-id="563f6-121">DIR_BACKWARD</span></span> 
  
> <span data-ttu-id="563f6-122">ブックマークで識別される行から逆方向に検索します。</span><span class="sxs-lookup"><span data-stu-id="563f6-122">Searches backward from the row identified by the bookmark.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="563f6-123">�߂�l</span><span class="sxs-lookup"><span data-stu-id="563f6-123">Return value</span></span>

<span data-ttu-id="563f6-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="563f6-124">S_OK</span></span> 
  
> <span data-ttu-id="563f6-125">検索操作が正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="563f6-125">The find operation was successful.</span></span>
    
<span data-ttu-id="563f6-126">MAPI_E_INVALID_BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="563f6-126">MAPI_E_INVALID_BOOKMARK</span></span> 
  
> <span data-ttu-id="563f6-127">削除されているため、または要求された最後の行を越えることがあるために、 _BkOrigin_パラメーター内のブックマークは無効です。</span><span class="sxs-lookup"><span data-stu-id="563f6-127">The bookmark in the  _BkOrigin_ parameter is invalid because it has been removed or because it is beyond the last row requested.</span></span> 
    
<span data-ttu-id="563f6-128">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="563f6-128">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="563f6-129">制限に一致する行が見つかりませんでした。</span><span class="sxs-lookup"><span data-stu-id="563f6-129">No rows were found that matched the restriction.</span></span>
    
<span data-ttu-id="563f6-130">MAPI_W_POSITION_CHANGED</span><span class="sxs-lookup"><span data-stu-id="563f6-130">MAPI_W_POSITION_CHANGED</span></span>
  
> <span data-ttu-id="563f6-131">呼び出しが成功したが、ときに最後に使用されたのと同じ行に、操作で使用するブックマークが設定されていません。ブックマークが使用されていない場合は不要になったと同じ位置に作成されたとき</span><span class="sxs-lookup"><span data-stu-id="563f6-131">The call succeeded, but the bookmark used in the operation is no longer set at the same row as when it was last used; if the bookmark has not been used, it is no longer in the same position as when it was created.</span></span> <span data-ttu-id="563f6-132">この警告が返されると、呼び出しを成功として処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="563f6-132">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="563f6-133">この警告をテストするには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="563f6-133">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="563f6-134">[エラー処理のためのマクロを使用する](using-macros-for-error-handling.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="563f6-134">See [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="563f6-135">備考</span><span class="sxs-lookup"><span data-stu-id="563f6-135">Remarks</span></span>

<span data-ttu-id="563f6-136">**IMAPITable::FindRow**メソッドは、 _lpRestriction_パラメーターが指す**SRestriction**構造で説明されている検索条件のセットに一致するテーブル内の最初の行を検索します。</span><span class="sxs-lookup"><span data-stu-id="563f6-136">The **IMAPITable::FindRow** method locates the first row in the table to match a set of search criteria described in the **SRestriction** structure pointed to by the  _lpRestriction_ parameter.</span></span> 
  
<span data-ttu-id="563f6-137">通常、 **FindRow**は指定されたブックマークから順方向に検索します。</span><span class="sxs-lookup"><span data-stu-id="563f6-137">Usually, **FindRow** searches forward from the specified bookmark.</span></span> <span data-ttu-id="563f6-138">_UlFlags_パラメーターに DIR_BACKWARD フラグを設定することで、ブックマークから後方へ移動するのには検索、呼び出し元を設定します。</span><span class="sxs-lookup"><span data-stu-id="563f6-138">The caller can set the search to move backward from the bookmark by setting the DIR_BACKWARD flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="563f6-139">現在のブックマークの開始方向へ検索しますブックマークより前の行から下方向へ検索を開始します。</span><span class="sxs-lookup"><span data-stu-id="563f6-139">Searching forward starts from the current bookmark; searching backward starts from the row prior to the bookmark.</span></span> <span data-ttu-id="563f6-140">検索の終了位置は、制限を満たす最初の行が見つかる前にだけです。</span><span class="sxs-lookup"><span data-stu-id="563f6-140">The end position of the search is just before the first row found that satisfied the restriction.</span></span> 
  
<span data-ttu-id="563f6-141">そのブックマークは、 _BkOrigin_パラメーターで指定された行がテーブルに存在しないテーブルは、新しいブックマークの位置を確立できない場合、 **FindRow**は MAPI_E_INVALID_BOOKMARK を返します。</span><span class="sxs-lookup"><span data-stu-id="563f6-141">If the row pointed to by the bookmark in the  _BkOrigin_ parameter no longer exists in the table and the table cannot establish a new position for the bookmark, **FindRow** returns MAPI_E_INVALID_BOOKMARK.</span></span> <span data-ttu-id="563f6-142">_BkOrigin_で指定された行が存在しないテーブルは、新しいブックマークの位置を確立することが場合、 **FindRow**は MAPI_W_POSITION_CHANGED を返します。</span><span class="sxs-lookup"><span data-stu-id="563f6-142">If the row pointed to by  _BkOrigin_ no longer exists and the table is able to establish a new position for the bookmark, **FindRow** returns MAPI_W_POSITION_CHANGED.</span></span> 
  
<span data-ttu-id="563f6-143">_BkOrigin_に渡されるブックマークが BOOKMARK_BEGINNING または BOOKMARK_END のいずれかの場合、 **FindRow**は、一致する行が見つからない場合は MAPI_E_NOT_FOUND を返します。</span><span class="sxs-lookup"><span data-stu-id="563f6-143">If the bookmark passed in  _BkOrigin_ is either BOOKMARK_BEGINNING or BOOKMARK_END, **FindRow** returns MAPI_E_NOT_FOUND if no matching row is found.</span></span> <span data-ttu-id="563f6-144">_BkOrigin_で使用されているブックマークが BOOKMARK_CURRENT である場合、 **FindRow**は必要は常に、現在のカーソル位置があるため MAPI_W_POSITION_CHANGED が MAPI_E_INVALID_BOOKMARK ではないと返すことができます。</span><span class="sxs-lookup"><span data-stu-id="563f6-144">If the bookmark used in  _BkOrigin_ is BOOKMARK_CURRENT, **FindRow** can return MAPI_W_POSITION_CHANGED but not MAPI_E_INVALID_BOOKMARK because there is always a current cursor position.</span></span> 
  
<span data-ttu-id="563f6-145">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) のプロパティ列は、他のすべてのテーブルに必要な**FindRow**のすべての実装は、PR_INSTANCE_KEY に基づいている行をシークの呼び出しをサポートする必要が.</span><span class="sxs-lookup"><span data-stu-id="563f6-145">The **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property column is required for all tables, and all implementations of **FindRow** are required to support calls seeking a row based on PR_INSTANCE_KEY.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="563f6-146">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="563f6-146">Notes to implementers</span></span>

<span data-ttu-id="563f6-147">**FindRow**によって実行されるプレフィックスの検索の型は、テーブルの構成と同じ方向に依存して、検索するときにのみ役立ちます。</span><span class="sxs-lookup"><span data-stu-id="563f6-147">The type of prefix searching performed by **FindRow** is only useful when the search follows the same direction as the table organization.</span></span> <span data-ttu-id="563f6-148">必要な動作を実現するためにプロパティ制限の構造体に渡された**RELOP_GE**によって暗黙的に指定の比較関数に同じ比較関数がテーブルの並べ替え順序を基になることがあります。</span><span class="sxs-lookup"><span data-stu-id="563f6-148">In order to achieve the required behavior, the comparison function implied by the **RELOP_GE** passed in the property restriction structure should be the same comparison function on which the table sort order is based.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="563f6-149">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="563f6-149">Notes to callers</span></span>

<span data-ttu-id="563f6-150">**FindRow**を使用すると、特にアドレス] ダイアログ ボックス内のリスト ボックスで、ユーザーが入力した文字列のスクロールをサポートします。</span><span class="sxs-lookup"><span data-stu-id="563f6-150">You can use **FindRow** to support scrolling based on strings typed in by the user, especially in list boxes within address dialog boxes.</span></span> <span data-ttu-id="563f6-151">この種類のスクロールでは、ユーザー入力、目的の文字列値のプレフィックスを徐々 に長く、および**FindRow**の呼び出しのプレフィックスに一致する最初の行にジャンプするのには定期的に発行することができます。</span><span class="sxs-lookup"><span data-stu-id="563f6-151">In this type of scrolling, users enter progressively longer prefixes of a desired string value, and you can periodically issue a **FindRow** call to jump to the first row that matches the prefix.</span></span> <span data-ttu-id="563f6-152">検索依存のどちらの方向にカーソルが移動する方向は、実行に設定されています。</span><span class="sxs-lookup"><span data-stu-id="563f6-152">Which direction the cursor jumps depends on which direction the search is set to run.</span></span> 
  
<span data-ttu-id="563f6-153">**FindRow**を使用するには、ブックマークを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="563f6-153">To use **FindRow**, a bookmark must be set.</span></span> <span data-ttu-id="563f6-154">現在の位置の先頭と末尾の表に示す既定のブックマークを含む、任意のブックマークから開始できるは、文字列の検索します。</span><span class="sxs-lookup"><span data-stu-id="563f6-154">The string search can originate from any bookmark, including from the preset bookmarks indicating the current position and the beginning and end of the table.</span></span> <span data-ttu-id="563f6-155">テーブル内の行の数が多い場合は、検索操作が遅くなることがあります。</span><span class="sxs-lookup"><span data-stu-id="563f6-155">If there are a large number of rows in the table, the search operation can be slow.</span></span>
  
<span data-ttu-id="563f6-156">制限を使用すると、次のようにスクロールするための文字列の接頭辞を検索できます。</span><span class="sxs-lookup"><span data-stu-id="563f6-156">Use a restriction to find a string prefix for scrolling as follows.</span></span> <span data-ttu-id="563f6-157">前方の昇順で並べ替えられた列で検索し、降順で並べ替えられた列の後方に検索するための関係の**RELOP_GE**に_lpRestriction_パラメーターは、適切なプロパティ制限構造体を渡しプロパティ タグと_タグ_ **GE**の形式_のプレフィックス_を使用して、プレフィックス。</span><span class="sxs-lookup"><span data-stu-id="563f6-157">For forward searching on a column sorted in ascending order and for backward searching on a column sorted in descending order, pass a property restriction structure in the  _lpRestriction_ parameter with the relation **RELOP_GE** and the appropriate property tag and prefix, using the format  _tag_ **GE** _prefix_.</span></span> 
  
<span data-ttu-id="563f6-158">フィルターを指定する構造体の制限の使用に関する詳細については、[制限の詳細](about-restrictions.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="563f6-158">For more information about using restriction structures to specify a filter, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="563f6-159">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="563f6-159">MFCMAPI reference</span></span>

<span data-ttu-id="563f6-160">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="563f6-160">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="563f6-161">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="563f6-161">**File**</span></span>|<span data-ttu-id="563f6-162">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="563f6-162">**Function**</span></span>|<span data-ttu-id="563f6-163">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="563f6-163">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="563f6-164">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="563f6-164">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="563f6-165">DwThreadFuncLoadTable</span><span class="sxs-lookup"><span data-stu-id="563f6-165">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="563f6-166">MFCMAPI では、 **IMAPITable::FindRow**メソッドを使用して、制約に一致する行を検索します。</span><span class="sxs-lookup"><span data-stu-id="563f6-166">MFCMAPI uses the **IMAPITable::FindRow** method to find rows which match a restriction.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="563f6-167">関連項目</span><span class="sxs-lookup"><span data-stu-id="563f6-167">See also</span></span>



[<span data-ttu-id="563f6-168">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="563f6-168">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="563f6-169">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="563f6-169">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="563f6-170">SRestriction</span><span class="sxs-lookup"><span data-stu-id="563f6-170">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="563f6-171">IMAPITable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="563f6-171">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


<span data-ttu-id="563f6-172">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="563f6-172">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

