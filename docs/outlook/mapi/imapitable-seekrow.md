---
title: IMAPITableSeekRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SeekRow
api_type:
- COM
ms.assetid: 93ac63ae-f254-45e1-a9b1-347d69d2ed9f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: fbc990a8c962883aa07987b200d1d2fd55434f93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413046"
---
# <a name="imapitableseekrow"></a><span data-ttu-id="bcd7b-103">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="bcd7b-103">IMAPITable::SeekRow</span></span>

  
  
<span data-ttu-id="bcd7b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bcd7b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bcd7b-105">テーブル内の特定の位置にカーソルを移動します。</span><span class="sxs-lookup"><span data-stu-id="bcd7b-105">Moves the cursor to a specific position in the table.</span></span>
  
```cpp
HRESULT SeekRow(
BOOKMARK bkOrigin,
LONG lRowCount,
LONG FAR * lplRowsSought
);
```

## <a name="parameters"></a><span data-ttu-id="bcd7b-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcd7b-106">Parameters</span></span>

 <span data-ttu-id="bcd7b-107">_bkOrigin_</span><span class="sxs-lookup"><span data-stu-id="bcd7b-107">_bkOrigin_</span></span>
  
> <span data-ttu-id="bcd7b-108">順番シーク操作の開始位置を識別するブックマーク。</span><span class="sxs-lookup"><span data-stu-id="bcd7b-108">[in] The bookmark identifying the starting position for the seek operation.</span></span> <span data-ttu-id="bcd7b-109">ブックを作成するには、 [IMAPITable:: createbookmark](imapitable-createbookmark.md)メソッドを使用するか、次の定義済みの値のいずれかを渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="bcd7b-109">A bookmark can be created using the [IMAPITable::CreateBookmark](imapitable-createbookmark.md) method, or one of the following predefined values can be passed.</span></span> 
    
<span data-ttu-id="bcd7b-110">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="bcd7b-110">BOOKMARK_BEGINNING</span></span> 
  
> <span data-ttu-id="bcd7b-111">テーブルの先頭からシーク操作を開始します。</span><span class="sxs-lookup"><span data-stu-id="bcd7b-111">Starts the seek operation from the beginning of the table.</span></span> 
    
<span data-ttu-id="bcd7b-112">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="bcd7b-112">BOOKMARK_CURRENT</span></span> 
  
> <span data-ttu-id="bcd7b-113">カーソルが置かれているテーブルの行からシーク操作を開始します。</span><span class="sxs-lookup"><span data-stu-id="bcd7b-113">Starts the seek operation from the row in the table where the cursor is located.</span></span> 
    
<span data-ttu-id="bcd7b-114">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="bcd7b-114">BOOKMARK_END</span></span> 
  
> <span data-ttu-id="bcd7b-115">テーブルの最後からシーク操作を開始します。</span><span class="sxs-lookup"><span data-stu-id="bcd7b-115">Starts the seek operation from the end of the table.</span></span> 
    
 <span data-ttu-id="bcd7b-116">_lrowcount_</span><span class="sxs-lookup"><span data-stu-id="bcd7b-116">_lRowCount_</span></span>
  
> <span data-ttu-id="bcd7b-117">順番_bkOrigin_パラメーターによって識別されるブックマークから開始して、移動する行数の符号付き数。</span><span class="sxs-lookup"><span data-stu-id="bcd7b-117">[in] The signed count of the number of rows to move, starting from the bookmark identified by the  _bkOrigin_ parameter.</span></span> 
    
 <span data-ttu-id="bcd7b-118">_lplrowssought_</span><span class="sxs-lookup"><span data-stu-id="bcd7b-118">_lplRowsSought_</span></span>
  
> <span data-ttu-id="bcd7b-119">読み上げ_lrowcount_が入力の有効なポインターである場合、 _lplrowssは_、シーク操作で処理された行数を指していることを示します。の符号は、検索の方向 (前方または後方) を示します。</span><span class="sxs-lookup"><span data-stu-id="bcd7b-119">[out] If  _lRowCount_ is a valid pointer on input,  _lplRowsSought_ points to the number of rows that were processed in the seek operation, the sign of which indicates the direction of search, forward or backward.</span></span> <span data-ttu-id="bcd7b-120">_lrowcount_が負の場合、 _lplrowssは_負の値になります。</span><span class="sxs-lookup"><span data-stu-id="bcd7b-120">If  _lRowCount_ is negative, then  _lplRowsSought_ is negative.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="bcd7b-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="bcd7b-121">Return value</span></span>

<span data-ttu-id="bcd7b-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="bcd7b-122">S_OK</span></span> 
  
> <span data-ttu-id="bcd7b-123">シーク操作が正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="bcd7b-123">The seek operation was successful.</span></span>
    
<span data-ttu-id="bcd7b-124">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="bcd7b-124">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="bcd7b-125">別の操作が進行中であるため、行シーク操作を開始できません。</span><span class="sxs-lookup"><span data-stu-id="bcd7b-125">Another operation is in progress that prevents the row-seeking operation from starting.</span></span> <span data-ttu-id="bcd7b-126">進行中の操作が完了することを許可するか、停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bcd7b-126">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="bcd7b-127">MAPI_E_INVALID_BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="bcd7b-127">MAPI_E_INVALID_BOOKMARK</span></span> 
  
> <span data-ttu-id="bcd7b-128">_bkOrigin_パラメーターで指定されたブックマークは、削除されたか、要求された最後の行を超えているため、無効です。</span><span class="sxs-lookup"><span data-stu-id="bcd7b-128">The bookmark specified in the  _bkOrigin_ parameter is invalid because it was removed or because it is beyond the last row requested.</span></span> 
    
<span data-ttu-id="bcd7b-129">MAPI_W_POSITION_CHANGED</span><span class="sxs-lookup"><span data-stu-id="bcd7b-129">MAPI_W_POSITION_CHANGED</span></span> 
  
> <span data-ttu-id="bcd7b-130">呼び出しは成功しましたが、 _bkOrigin_パラメーターで指定されたブックマークは、最後に使用されたときと同じ行に設定されていません。</span><span class="sxs-lookup"><span data-stu-id="bcd7b-130">The call succeeded, but the bookmark specified in the  _bkOrigin_ parameter is no longer set at the same row as it was when it was last used.</span></span> <span data-ttu-id="bcd7b-131">ブックマークが使用されていない場合は、作成時と同じ位置になりません。</span><span class="sxs-lookup"><span data-stu-id="bcd7b-131">If the bookmark has not been used, it is no longer in the same position as it was when it was created.</span></span> <span data-ttu-id="bcd7b-132">この警告が返された場合、呼び出しは正常に処理されます。</span><span class="sxs-lookup"><span data-stu-id="bcd7b-132">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="bcd7b-133">この警告をテストするには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="bcd7b-133">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="bcd7b-134">詳細については、「[エラー処理にマクロを使用する](using-macros-for-error-handling.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bcd7b-134">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bcd7b-135">注釈</span><span class="sxs-lookup"><span data-stu-id="bcd7b-135">Remarks</span></span>

<span data-ttu-id="bcd7b-136">**IMAPITable:: seekrow**メソッドは、カーソルの新しい BOOKMARK_CURRENT 位置を確立します。</span><span class="sxs-lookup"><span data-stu-id="bcd7b-136">The **IMAPITable::SeekRow** method establishes a new BOOKMARK_CURRENT position for the cursor.</span></span> <span data-ttu-id="bcd7b-137">_lrowcount_パラメーターは、カーソルが移動する行の数と移動の方向を示します。</span><span class="sxs-lookup"><span data-stu-id="bcd7b-137">The  _lRowCount_ parameter indicates the number of rows that the cursor moves and the direction of movement.</span></span> 
  
<span data-ttu-id="bcd7b-138">結果の位置が表の最後の行を超える場合、カーソルは最後の行の後に配置されます。</span><span class="sxs-lookup"><span data-stu-id="bcd7b-138">If the resulting position is beyond the last row of the table, the cursor is positioned after the last row.</span></span> <span data-ttu-id="bcd7b-139">結果の位置がテーブルの最初の行より前にある場合、カーソルは先頭行の先頭に配置されます。</span><span class="sxs-lookup"><span data-stu-id="bcd7b-139">If the resulting position is before the first row of the table, the cursor is positioned at the beginning of the first row.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="bcd7b-140">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="bcd7b-140">Notes to implementers</span></span>

<span data-ttu-id="bcd7b-141">_bkOrigin_によって参照される行がテーブルに存在しなくなり、ブックマークの新しい位置を設定できない場合は、MAPI_E_INVALID_BOOKMARK を返します。</span><span class="sxs-lookup"><span data-stu-id="bcd7b-141">If the row pointed to by  _bkOrigin_ no longer exists in the table and you cannot establish a new position for the bookmark, return MAPI_E_INVALID_BOOKMARK.</span></span> <span data-ttu-id="bcd7b-142">_bkOrigin_によって参照される行が存在しなくなり、ブックマークの新しい位置を設定できる場合は、MAPI_W_POSITION_CHANGED を返します。</span><span class="sxs-lookup"><span data-stu-id="bcd7b-142">If the row pointed to by  _bkOrigin_ no longer exists and you can establish a new position for the bookmark, return MAPI_W_POSITION_CHANGED.</span></span> 
  
<span data-ttu-id="bcd7b-143">テーブルビューから折りたたまれている行を指すブックマークは、引き続き使用できます。</span><span class="sxs-lookup"><span data-stu-id="bcd7b-143">A bookmark pointing to a row that is collapsed out of the table view can still be used.</span></span> <span data-ttu-id="bcd7b-144">呼び出し元がこのようなブックマークにカーソルを移動しようとした場合は、カーソルを次の表示される行に移動し、MAPI_W_POSITION_CHANGED を返します。</span><span class="sxs-lookup"><span data-stu-id="bcd7b-144">If the caller attempts to move the cursor to such a bookmark, move the cursor to the next visible row and return MAPI_W_POSITION_CHANGED.</span></span> 
  
<span data-ttu-id="bcd7b-145">使用時または行が折りたたまれたときに、表示されていない位置のブックマークを移動できます。</span><span class="sxs-lookup"><span data-stu-id="bcd7b-145">You can move bookmarks for positions collapsed out of view, either at the time of use or at the time that the row is collapsed.</span></span> <span data-ttu-id="bcd7b-146">行が折りたたまれたときにブックマークが移動された場合は、ブックマークが最後に使用されてから移動したか、または作成後に一度も使用されていない場合は、ブックマークが移動したかどうかを示すビットを保持します。</span><span class="sxs-lookup"><span data-stu-id="bcd7b-146">If a bookmark is moved at the time that the row is collapsed, keep a bit in the bookmark that indicates whether the bookmark has moved since its last use or, if it has never been used, since its creation.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="bcd7b-147">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="bcd7b-147">Notes to callers</span></span>

<span data-ttu-id="bcd7b-148">**seekrow**の後方移動を指定するには、 _lrowcount_に負の値を渡します。</span><span class="sxs-lookup"><span data-stu-id="bcd7b-148">To indicate a backward move for **SeekRow**, pass a negative value in  _lRowCount_.</span></span> <span data-ttu-id="bcd7b-149">テーブルの先頭を検索するには、 _lrowcount_の0と、 _bkOrigin_の値 BOOKMARK_BEGINNING を渡します。</span><span class="sxs-lookup"><span data-stu-id="bcd7b-149">To search to the beginning of the table, pass zero in  _lRowCount_ and the value BOOKMARK_BEGINNING in  _bkOrigin_.</span></span> 
  
<span data-ttu-id="bcd7b-150">テーブルに多数の行がある場合、 **seekrow**操作が遅くなることがあります。</span><span class="sxs-lookup"><span data-stu-id="bcd7b-150">If there are lots of rows in the table, the **SeekRow** operation can be slow.</span></span> <span data-ttu-id="bcd7b-151">_lplrowssought_パラメーターの内容で行数を返す必要がある場合は、パフォーマンスに影響することもあります。</span><span class="sxs-lookup"><span data-stu-id="bcd7b-151">Performance can also be affected if you require a row count to be returned in the contents of the  _lplRowsSought_ parameter.</span></span> 
  
 <span data-ttu-id="bcd7b-152">**seekrow**は、 _lrowcount_によって参照される変数内で実際に検索された行の数 (正または負) を返します。</span><span class="sxs-lookup"><span data-stu-id="bcd7b-152">**SeekRow** returns the number of rows actually searched through, positive or negative, in the variable pointed to by  _lRowCount_.</span></span> <span data-ttu-id="bcd7b-153">通常の操作では、検索によってテーブルの先頭または末尾に到達した場合を除いて、 _lrowcount_ _rowssが_渡されたときと同じ値を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="bcd7b-153">In ordinary operation, it should return the same value for  _lplRowsSought_ as passed in for  _lRowCount_, unless the search reached the beginning or end of the table.</span></span> 
  
<span data-ttu-id="bcd7b-154">_lrowcount_を50より大きい数値に設定しないでください。</span><span class="sxs-lookup"><span data-stu-id="bcd7b-154">Do not set  _lRowCount_ to a number greater than 50.</span></span> <span data-ttu-id="bcd7b-155">より多くの行をシークするには、 [IMAPITable:: seekrowapprox](imapitable-seekrowapprox.md)メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="bcd7b-155">To seek through a larger number of rows, use the [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="bcd7b-156">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="bcd7b-156">MFCMAPI reference</span></span>

<span data-ttu-id="bcd7b-157">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bcd7b-157">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="bcd7b-158">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="bcd7b-158">**File**</span></span>|<span data-ttu-id="bcd7b-159">**関数**</span><span class="sxs-lookup"><span data-stu-id="bcd7b-159">**Function**</span></span>|<span data-ttu-id="bcd7b-160">**コメント**</span><span class="sxs-lookup"><span data-stu-id="bcd7b-160">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bcd7b-161">MAPIProcessor</span><span class="sxs-lookup"><span data-stu-id="bcd7b-161">MAPIProcessor.cpp</span></span>  <br/> |<span data-ttu-id="bcd7b-162">cmapiprocessor::P rocessmailboxtable</span><span class="sxs-lookup"><span data-stu-id="bcd7b-162">CMAPIProcessor::ProcessMailboxTable</span></span>  <br/> |<span data-ttu-id="bcd7b-163">mfcmapi は、 **IMAPITable:: seekrow**メソッドを使用して、処理の前にテーブルの先頭を特定します。</span><span class="sxs-lookup"><span data-stu-id="bcd7b-163">MFCMAPI uses the **IMAPITable::SeekRow** method to locate the beginning of the table before processing.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bcd7b-164">関連項目</span><span class="sxs-lookup"><span data-stu-id="bcd7b-164">See also</span></span>



[<span data-ttu-id="bcd7b-165">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="bcd7b-165">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="bcd7b-166">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="bcd7b-166">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="bcd7b-167">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="bcd7b-167">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="bcd7b-168">IMAPITable::SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="bcd7b-168">IMAPITable::SeekRowApprox</span></span>](imapitable-seekrowapprox.md)
  
[<span data-ttu-id="bcd7b-169">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bcd7b-169">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


<span data-ttu-id="bcd7b-170">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="bcd7b-170">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

