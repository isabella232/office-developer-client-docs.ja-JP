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
# <a name="imapitablefindrow"></a><span data-ttu-id="8d52d-103">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="8d52d-103">IMAPITable::FindRow</span></span>

  
  
<span data-ttu-id="8d52d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d52d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d52d-105">特定の検索条件に一致するテーブル内の次の行を検索し、カーソルをその行に移動します。</span><span class="sxs-lookup"><span data-stu-id="8d52d-105">Finds the next row in a table that matches specific search criteria and moves the cursor to that row.</span></span>
  
```cpp
HRESULT FindRow(
LPSRestriction lpRestriction,
BOOKMARK BkOrigin,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="8d52d-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8d52d-106">Parameters</span></span>

 <span data-ttu-id="8d52d-107">_lpRestriction_</span><span class="sxs-lookup"><span data-stu-id="8d52d-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="8d52d-108">[in]検索条件を記述 [する SRestriction](srestriction.md) 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="8d52d-108">[in] A pointer to an [SRestriction](srestriction.md) structure that describes the search criteria.</span></span> 
    
 <span data-ttu-id="8d52d-109">_BkOrigin_</span><span class="sxs-lookup"><span data-stu-id="8d52d-109">_BkOrigin_</span></span>
  
> <span data-ttu-id="8d52d-110">[in]FindRow が検索を開始する **行を** 識別するブックマーク。</span><span class="sxs-lookup"><span data-stu-id="8d52d-110">[in] A bookmark identifying the row where **FindRow** should begin its search.</span></span> <span data-ttu-id="8d52d-111">ブックマークは [、IMAPITable::CreateBookmark](imapitable-createbookmark.md) メソッドを使用して作成するか、次のいずれかの定義済みの値を渡します。</span><span class="sxs-lookup"><span data-stu-id="8d52d-111">A bookmark can be created using the [IMAPITable::CreateBookmark](imapitable-createbookmark.md) method, or one of the following predefined values can be passed.</span></span> 
    
<span data-ttu-id="8d52d-112">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="8d52d-112">BOOKMARK_BEGINNING</span></span> 
  
> <span data-ttu-id="8d52d-113">テーブルの先頭から検索します。</span><span class="sxs-lookup"><span data-stu-id="8d52d-113">Searches from the beginning of the table.</span></span> 
    
<span data-ttu-id="8d52d-114">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="8d52d-114">BOOKMARK_CURRENT</span></span> 
  
> <span data-ttu-id="8d52d-115">カーソルがあるテーブル内の行から検索します。</span><span class="sxs-lookup"><span data-stu-id="8d52d-115">Searches from the row in the table where the cursor is located.</span></span> 
    
<span data-ttu-id="8d52d-116">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="8d52d-116">BOOKMARK_END</span></span> 
  
> <span data-ttu-id="8d52d-117">テーブルの末尾から検索します。</span><span class="sxs-lookup"><span data-stu-id="8d52d-117">Searches from the end of the table.</span></span> 
    
 <span data-ttu-id="8d52d-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8d52d-118">_ulFlags_</span></span>
  
> <span data-ttu-id="8d52d-119">[in]検索の方向を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="8d52d-119">[in] A bitmask of flags that controls the direction of the search.</span></span> <span data-ttu-id="8d52d-120">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="8d52d-120">The following flag can be set:</span></span>
    
<span data-ttu-id="8d52d-121">DIR_BACKWARD</span><span class="sxs-lookup"><span data-stu-id="8d52d-121">DIR_BACKWARD</span></span> 
  
> <span data-ttu-id="8d52d-122">ブックマークで識別された行から後方に検索します。</span><span class="sxs-lookup"><span data-stu-id="8d52d-122">Searches backward from the row identified by the bookmark.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8d52d-123">戻り値</span><span class="sxs-lookup"><span data-stu-id="8d52d-123">Return value</span></span>

<span data-ttu-id="8d52d-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="8d52d-124">S_OK</span></span> 
  
> <span data-ttu-id="8d52d-125">検索操作が成功しました。</span><span class="sxs-lookup"><span data-stu-id="8d52d-125">The find operation was successful.</span></span>
    
<span data-ttu-id="8d52d-126">MAPI_E_INVALID_BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="8d52d-126">MAPI_E_INVALID_BOOKMARK</span></span> 
  
> <span data-ttu-id="8d52d-127">_BkOrigin_ パラメーターのブックマークは、削除されたため、または要求された最後の行を超えているため無効です。</span><span class="sxs-lookup"><span data-stu-id="8d52d-127">The bookmark in the  _BkOrigin_ parameter is invalid because it has been removed or because it is beyond the last row requested.</span></span> 
    
<span data-ttu-id="8d52d-128">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="8d52d-128">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="8d52d-129">制限に一致する行が見つかりませんでした。</span><span class="sxs-lookup"><span data-stu-id="8d52d-129">No rows were found that matched the restriction.</span></span>
    
<span data-ttu-id="8d52d-130">MAPI_W_POSITION_CHANGED</span><span class="sxs-lookup"><span data-stu-id="8d52d-130">MAPI_W_POSITION_CHANGED</span></span>
  
> <span data-ttu-id="8d52d-131">呼び出しは成功しましたが、操作で使用されるブックマークは、最後に使用された行と同じ行に設定されなくなりました。ブックマークが使用されていない場合、ブックマークは作成された位置と同じ位置になくなりました。</span><span class="sxs-lookup"><span data-stu-id="8d52d-131">The call succeeded, but the bookmark used in the operation is no longer set at the same row as when it was last used; if the bookmark has not been used, it is no longer in the same position as when it was created.</span></span> <span data-ttu-id="8d52d-132">この警告が返されると、呼び出しは正常に処理されます。</span><span class="sxs-lookup"><span data-stu-id="8d52d-132">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="8d52d-133">この警告をテストするには、次のマクロ **HR_FAILED** します。</span><span class="sxs-lookup"><span data-stu-id="8d52d-133">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="8d52d-134">「エラー [処理のためのマクロの使用」を参照してください](using-macros-for-error-handling.md)。</span><span class="sxs-lookup"><span data-stu-id="8d52d-134">See [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8d52d-135">注釈</span><span class="sxs-lookup"><span data-stu-id="8d52d-135">Remarks</span></span>

<span data-ttu-id="8d52d-136">**IMAPITable::FindRow** メソッドは _、lpRestriction_ パラメーターが指す **SRestriction** 構造で説明されている一連の検索条件に一致するように表の最初の行を検索します。</span><span class="sxs-lookup"><span data-stu-id="8d52d-136">The **IMAPITable::FindRow** method locates the first row in the table to match a set of search criteria described in the **SRestriction** structure pointed to by the  _lpRestriction_ parameter.</span></span> 
  
<span data-ttu-id="8d52d-137">通常 **、FindRow は** 指定したブックマークから前方に検索します。</span><span class="sxs-lookup"><span data-stu-id="8d52d-137">Usually, **FindRow** searches forward from the specified bookmark.</span></span> <span data-ttu-id="8d52d-138">呼び出し元は  _、ulFlags_ パラメーターで DIR_BACKWARDフラグを設定することで、ブックマークから後方に移動する検索を設定できます。</span><span class="sxs-lookup"><span data-stu-id="8d52d-138">The caller can set the search to move backward from the bookmark by setting the DIR_BACKWARD flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="8d52d-139">前方検索は、現在のブックマークから開始します。ブックマークの前の行から後方検索が開始されます。</span><span class="sxs-lookup"><span data-stu-id="8d52d-139">Searching forward starts from the current bookmark; searching backward starts from the row prior to the bookmark.</span></span> <span data-ttu-id="8d52d-140">検索の終了位置は、制限を満たした最初の行が見つかる直前です。</span><span class="sxs-lookup"><span data-stu-id="8d52d-140">The end position of the search is just before the first row found that satisfied the restriction.</span></span> 
  
<span data-ttu-id="8d52d-141">_BkOrigin_ パラメーター内のブックマークが指す行がテーブルに存在しなくなった場合、テーブルはブックマークの新しい位置を確立できない場合 **、FindRow** は新しい位置をMAPI_E_INVALID_BOOKMARK。</span><span class="sxs-lookup"><span data-stu-id="8d52d-141">If the row pointed to by the bookmark in the  _BkOrigin_ parameter no longer exists in the table and the table cannot establish a new position for the bookmark, **FindRow** returns MAPI_E_INVALID_BOOKMARK.</span></span> <span data-ttu-id="8d52d-142">_BkOrigin_ が指す行が存在しなくなった場合に、テーブルがブックマークの新しい位置を確立できる場合 **、FindRow** はブックマークをMAPI_W_POSITION_CHANGED。</span><span class="sxs-lookup"><span data-stu-id="8d52d-142">If the row pointed to by  _BkOrigin_ no longer exists and the table is able to establish a new position for the bookmark, **FindRow** returns MAPI_W_POSITION_CHANGED.</span></span> 
  
<span data-ttu-id="8d52d-143">_BkOrigin_ で渡されたブックマークがBOOKMARK_BEGINNINGまたはBOOKMARK_END、一致する行MAPI_E_NOT_FOUND場合 **、FindRow** は値を返します。</span><span class="sxs-lookup"><span data-stu-id="8d52d-143">If the bookmark passed in  _BkOrigin_ is either BOOKMARK_BEGINNING or BOOKMARK_END, **FindRow** returns MAPI_E_NOT_FOUND if no matching row is found.</span></span> <span data-ttu-id="8d52d-144">_BkOrigin_ で使用されるブックマークが BOOKMARK_CURRENT の場合 **、FindRow** は常に現在のカーソル位置MAPI_W_POSITION_CHANGEDを返すが、MAPI_E_INVALID_BOOKMARK を返すことはありません。</span><span class="sxs-lookup"><span data-stu-id="8d52d-144">If the bookmark used in  _BkOrigin_ is BOOKMARK_CURRENT, **FindRow** can return MAPI_W_POSITION_CHANGED but not MAPI_E_INVALID_BOOKMARK because there is always a current cursor position.</span></span> 
  
<span data-ttu-id="8d52d-145">すべての **テーブルPR_INSTANCE_KEY** プロパティ ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) プロパティ列が必要であり **、FindRow** のすべての実装は、PR_INSTANCE_KEY に基づいて行を求める呼び出しをサポートするために必要です。</span><span class="sxs-lookup"><span data-stu-id="8d52d-145">The **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property column is required for all tables, and all implementations of **FindRow** are required to support calls seeking a row based on PR_INSTANCE_KEY.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="8d52d-146">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="8d52d-146">Notes to implementers</span></span>

<span data-ttu-id="8d52d-147">**FindRow** によって実行されるプレフィックス検索の種類は、検索がテーブルの組織と同じ方向に従う場合にのみ役立ちます。</span><span class="sxs-lookup"><span data-stu-id="8d52d-147">The type of prefix searching performed by **FindRow** is only useful when the search follows the same direction as the table organization.</span></span> <span data-ttu-id="8d52d-148">必要な動作を実現するために、プロパティ制限構造で渡される **RELOP_GE** によって暗示される比較関数は、テーブルの並べ替え順序が基になるのと同じ比較関数である必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d52d-148">In order to achieve the required behavior, the comparison function implied by the **RELOP_GE** passed in the property restriction structure should be the same comparison function on which the table sort order is based.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8d52d-149">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="8d52d-149">Notes to callers</span></span>

<span data-ttu-id="8d52d-150">**FindRow を使用すると**、特にアドレス ダイアログ ボックス内のリスト ボックスで、ユーザーが入力した文字列に基づいてスクロールをサポートできます。</span><span class="sxs-lookup"><span data-stu-id="8d52d-150">You can use **FindRow** to support scrolling based on strings typed in by the user, especially in list boxes within address dialog boxes.</span></span> <span data-ttu-id="8d52d-151">この種類のスクロールでは、ユーザーは目的の文字列値の徐々に長いプレフィックスを入力し **、FindRow** 呼び出しを定期的に発行して、プレフィックスに一致する最初の行にジャンプできます。</span><span class="sxs-lookup"><span data-stu-id="8d52d-151">In this type of scrolling, users enter progressively longer prefixes of a desired string value, and you can periodically issue a **FindRow** call to jump to the first row that matches the prefix.</span></span> <span data-ttu-id="8d52d-152">カーソルがジャンプする方向は、検索を実行する方向によって異なります。</span><span class="sxs-lookup"><span data-stu-id="8d52d-152">Which direction the cursor jumps depends on which direction the search is set to run.</span></span> 
  
<span data-ttu-id="8d52d-153">**FindRow を使用するには、** ブックマークを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d52d-153">To use **FindRow**, a bookmark must be set.</span></span> <span data-ttu-id="8d52d-154">文字列検索は、現在の位置とテーブルの先頭と末尾を示す事前設定のブックマークを含む、任意のブックマークから発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8d52d-154">The string search can originate from any bookmark, including from the preset bookmarks indicating the current position and the beginning and end of the table.</span></span> <span data-ttu-id="8d52d-155">テーブル内に多数の行がある場合、検索操作が遅くなる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8d52d-155">If there are a large number of rows in the table, the search operation can be slow.</span></span>
  
<span data-ttu-id="8d52d-156">次のようにスクロールする文字列プレフィックスを検索するには、制限を使用します。</span><span class="sxs-lookup"><span data-stu-id="8d52d-156">Use a restriction to find a string prefix for scrolling as follows.</span></span> <span data-ttu-id="8d52d-157">昇順で並べ替えた列で順方向検索を行い、降順に並べ替えた列を逆方向に検索するには _、lpRestriction_ パラメーターのプロパティ制限構造を、関連付け **RELOP_GE** と適切なプロパティ タグとプレフィックスを使用して、形式タグ **GE** プレフィックスを使用して渡します。</span><span class="sxs-lookup"><span data-stu-id="8d52d-157">For forward searching on a column sorted in ascending order and for backward searching on a column sorted in descending order, pass a property restriction structure in the  _lpRestriction_ parameter with the relation **RELOP_GE** and the appropriate property tag and prefix, using the format  _tag_ **GE** _prefix_.</span></span> 
  
<span data-ttu-id="8d52d-158">制限構造を使用してフィルターを指定する方法の詳細については、「 [制限について」を参照してください](about-restrictions.md)。</span><span class="sxs-lookup"><span data-stu-id="8d52d-158">For more information about using restriction structures to specify a filter, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8d52d-159">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="8d52d-159">MFCMAPI reference</span></span>

<span data-ttu-id="8d52d-160">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8d52d-160">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8d52d-161">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="8d52d-161">**File**</span></span>|<span data-ttu-id="8d52d-162">**関数**</span><span class="sxs-lookup"><span data-stu-id="8d52d-162">**Function**</span></span>|<span data-ttu-id="8d52d-163">**コメント**</span><span class="sxs-lookup"><span data-stu-id="8d52d-163">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8d52d-164">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="8d52d-164">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="8d52d-165">DwThreadFuncLoadTable</span><span class="sxs-lookup"><span data-stu-id="8d52d-165">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="8d52d-166">MFCMAPI は **IMAPITable::FindRow** メソッドを使用して、制限に一致する行を検索します。</span><span class="sxs-lookup"><span data-stu-id="8d52d-166">MFCMAPI uses the **IMAPITable::FindRow** method to find rows which match a restriction.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8d52d-167">関連項目</span><span class="sxs-lookup"><span data-stu-id="8d52d-167">See also</span></span>



[<span data-ttu-id="8d52d-168">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="8d52d-168">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="8d52d-169">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="8d52d-169">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="8d52d-170">SRestriction</span><span class="sxs-lookup"><span data-stu-id="8d52d-170">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="8d52d-171">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8d52d-171">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


<span data-ttu-id="8d52d-172">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="8d52d-172">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

