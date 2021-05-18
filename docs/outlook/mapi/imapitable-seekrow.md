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
# <a name="imapitableseekrow"></a><span data-ttu-id="7d989-103">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="7d989-103">IMAPITable::SeekRow</span></span>

  
  
<span data-ttu-id="7d989-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d989-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d989-105">テーブル内の特定の位置にカーソルを移動します。</span><span class="sxs-lookup"><span data-stu-id="7d989-105">Moves the cursor to a specific position in the table.</span></span>
  
```cpp
HRESULT SeekRow(
BOOKMARK bkOrigin,
LONG lRowCount,
LONG FAR * lplRowsSought
);
```

## <a name="parameters"></a><span data-ttu-id="7d989-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7d989-106">Parameters</span></span>

 <span data-ttu-id="7d989-107">_bkOrigin_</span><span class="sxs-lookup"><span data-stu-id="7d989-107">_bkOrigin_</span></span>
  
> <span data-ttu-id="7d989-108">[in]シーク操作の開始位置を識別するブックマーク。</span><span class="sxs-lookup"><span data-stu-id="7d989-108">[in] The bookmark identifying the starting position for the seek operation.</span></span> <span data-ttu-id="7d989-109">ブックマークは [、IMAPITable::CreateBookmark](imapitable-createbookmark.md) メソッドを使用して作成するか、次のいずれかの定義済みの値を渡します。</span><span class="sxs-lookup"><span data-stu-id="7d989-109">A bookmark can be created using the [IMAPITable::CreateBookmark](imapitable-createbookmark.md) method, or one of the following predefined values can be passed.</span></span> 
    
<span data-ttu-id="7d989-110">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="7d989-110">BOOKMARK_BEGINNING</span></span> 
  
> <span data-ttu-id="7d989-111">テーブルの先頭からシーク操作を開始します。</span><span class="sxs-lookup"><span data-stu-id="7d989-111">Starts the seek operation from the beginning of the table.</span></span> 
    
<span data-ttu-id="7d989-112">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="7d989-112">BOOKMARK_CURRENT</span></span> 
  
> <span data-ttu-id="7d989-113">カーソルがあるテーブルの行からシーク操作を開始します。</span><span class="sxs-lookup"><span data-stu-id="7d989-113">Starts the seek operation from the row in the table where the cursor is located.</span></span> 
    
<span data-ttu-id="7d989-114">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="7d989-114">BOOKMARK_END</span></span> 
  
> <span data-ttu-id="7d989-115">テーブルの最後からシーク操作を開始します。</span><span class="sxs-lookup"><span data-stu-id="7d989-115">Starts the seek operation from the end of the table.</span></span> 
    
 <span data-ttu-id="7d989-116">_lRowCount_</span><span class="sxs-lookup"><span data-stu-id="7d989-116">_lRowCount_</span></span>
  
> <span data-ttu-id="7d989-117">[in]  _bkOrigin_ パラメーターで識別されるブックマークから始まる、移動する行数の符号付きカウント。</span><span class="sxs-lookup"><span data-stu-id="7d989-117">[in] The signed count of the number of rows to move, starting from the bookmark identified by the  _bkOrigin_ parameter.</span></span> 
    
 <span data-ttu-id="7d989-118">_lplRowsSought_</span><span class="sxs-lookup"><span data-stu-id="7d989-118">_lplRowsSought_</span></span>
  
> <span data-ttu-id="7d989-119">[out]  _lRowCount_ が入力上の有効なポインターである場合  _、lplRowsSought_ はシーク操作で処理された行の数を指し示し、その符号は検索方向、前方方向、または後方方向を示します。</span><span class="sxs-lookup"><span data-stu-id="7d989-119">[out] If  _lRowCount_ is a valid pointer on input,  _lplRowsSought_ points to the number of rows that were processed in the seek operation, the sign of which indicates the direction of search, forward or backward.</span></span> <span data-ttu-id="7d989-120">_lRowCount が_ 負の場合 _、lplRowsSought は_ 負の値になります。</span><span class="sxs-lookup"><span data-stu-id="7d989-120">If  _lRowCount_ is negative, then  _lplRowsSought_ is negative.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7d989-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="7d989-121">Return value</span></span>

<span data-ttu-id="7d989-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="7d989-122">S_OK</span></span> 
  
> <span data-ttu-id="7d989-123">シーク操作が成功しました。</span><span class="sxs-lookup"><span data-stu-id="7d989-123">The seek operation was successful.</span></span>
    
<span data-ttu-id="7d989-124">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="7d989-124">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="7d989-125">行シーク操作の開始を妨げる別の操作が進行中です。</span><span class="sxs-lookup"><span data-stu-id="7d989-125">Another operation is in progress that prevents the row-seeking operation from starting.</span></span> <span data-ttu-id="7d989-126">進行中の操作の完了を許可するか、停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d989-126">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="7d989-127">MAPI_E_INVALID_BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="7d989-127">MAPI_E_INVALID_BOOKMARK</span></span> 
  
> <span data-ttu-id="7d989-128">_bkOrigin_ パラメーターで指定されたブックマークは、削除されたため、または要求された最後の行を超えているため無効です。</span><span class="sxs-lookup"><span data-stu-id="7d989-128">The bookmark specified in the  _bkOrigin_ parameter is invalid because it was removed or because it is beyond the last row requested.</span></span> 
    
<span data-ttu-id="7d989-129">MAPI_W_POSITION_CHANGED</span><span class="sxs-lookup"><span data-stu-id="7d989-129">MAPI_W_POSITION_CHANGED</span></span> 
  
> <span data-ttu-id="7d989-130">呼び出しは成功しましたが  _、bkOrigin_ パラメーターで指定されたブックマークは、前回の使用時と同じ行に設定されなくなりました。</span><span class="sxs-lookup"><span data-stu-id="7d989-130">The call succeeded, but the bookmark specified in the  _bkOrigin_ parameter is no longer set at the same row as it was when it was last used.</span></span> <span data-ttu-id="7d989-131">ブックマークが使用されていない場合、ブックマークは作成された位置と同じ位置になくなりました。</span><span class="sxs-lookup"><span data-stu-id="7d989-131">If the bookmark has not been used, it is no longer in the same position as it was when it was created.</span></span> <span data-ttu-id="7d989-132">この警告が返されると、呼び出しは正常に処理されます。</span><span class="sxs-lookup"><span data-stu-id="7d989-132">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="7d989-133">この警告をテストするには、次のマクロ **HR_FAILED** します。</span><span class="sxs-lookup"><span data-stu-id="7d989-133">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="7d989-134">詳細については、「Using [Macros for Error Handling 」を参照してください](using-macros-for-error-handling.md)。</span><span class="sxs-lookup"><span data-stu-id="7d989-134">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7d989-135">注釈</span><span class="sxs-lookup"><span data-stu-id="7d989-135">Remarks</span></span>

<span data-ttu-id="7d989-136">**IMAPITable::SeekRow** メソッドは、カーソルの新BOOKMARK_CURRENT位置を確立します。</span><span class="sxs-lookup"><span data-stu-id="7d989-136">The **IMAPITable::SeekRow** method establishes a new BOOKMARK_CURRENT position for the cursor.</span></span> <span data-ttu-id="7d989-137">_lRowCount パラメーター_ は、カーソルが移動する行数と移動方向を示します。</span><span class="sxs-lookup"><span data-stu-id="7d989-137">The  _lRowCount_ parameter indicates the number of rows that the cursor moves and the direction of movement.</span></span> 
  
<span data-ttu-id="7d989-138">結果の位置が表の最後の行を超える場合、カーソルは最後の行の後に配置されます。</span><span class="sxs-lookup"><span data-stu-id="7d989-138">If the resulting position is beyond the last row of the table, the cursor is positioned after the last row.</span></span> <span data-ttu-id="7d989-139">結果の位置が表の最初の行の前にある場合、カーソルは最初の行の先頭に配置されます。</span><span class="sxs-lookup"><span data-stu-id="7d989-139">If the resulting position is before the first row of the table, the cursor is positioned at the beginning of the first row.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7d989-140">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="7d989-140">Notes to implementers</span></span>

<span data-ttu-id="7d989-141">_bkOrigin_ が指す行がテーブルに存在しなくなった場合、ブックマークの新しい位置を確立できない場合は、次の値をMAPI_E_INVALID_BOOKMARK。</span><span class="sxs-lookup"><span data-stu-id="7d989-141">If the row pointed to by  _bkOrigin_ no longer exists in the table and you cannot establish a new position for the bookmark, return MAPI_E_INVALID_BOOKMARK.</span></span> <span data-ttu-id="7d989-142">_bkOrigin_ が指す行が存在しなくなった場合、ブックマークの新しい位置を確立できる場合は、次のMAPI_W_POSITION_CHANGED。</span><span class="sxs-lookup"><span data-stu-id="7d989-142">If the row pointed to by  _bkOrigin_ no longer exists and you can establish a new position for the bookmark, return MAPI_W_POSITION_CHANGED.</span></span> 
  
<span data-ttu-id="7d989-143">テーブル ビューから折りたたむ行を指すブックマークは、引き続き使用できます。</span><span class="sxs-lookup"><span data-stu-id="7d989-143">A bookmark pointing to a row that is collapsed out of the table view can still be used.</span></span> <span data-ttu-id="7d989-144">呼び出し元がそのようなブックマークにカーソルを移動しようとした場合は、カーソルを次の表示行に移動し、カーソルを戻MAPI_W_POSITION_CHANGED。</span><span class="sxs-lookup"><span data-stu-id="7d989-144">If the caller attempts to move the cursor to such a bookmark, move the cursor to the next visible row and return MAPI_W_POSITION_CHANGED.</span></span> 
  
<span data-ttu-id="7d989-145">折りたたむ位置のブックマークは、使用時または行が折りたたむ時点で、表示から外れて移動できます。</span><span class="sxs-lookup"><span data-stu-id="7d989-145">You can move bookmarks for positions collapsed out of view, either at the time of use or at the time that the row is collapsed.</span></span> <span data-ttu-id="7d989-146">行が折りたたむ時点でブックマークを移動する場合は、ブックマークが最後に使用された後に移動したかどうかを示すブックマークに少し保持するか、作成後にブックマークが使用されたことがない場合は、ブックマークを移動します。</span><span class="sxs-lookup"><span data-stu-id="7d989-146">If a bookmark is moved at the time that the row is collapsed, keep a bit in the bookmark that indicates whether the bookmark has moved since its last use or, if it has never been used, since its creation.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="7d989-147">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="7d989-147">Notes to callers</span></span>

<span data-ttu-id="7d989-148">SeekRow の逆方向の移動 **を示す場合** は  _、lRowCount で負の値を渡します_。</span><span class="sxs-lookup"><span data-stu-id="7d989-148">To indicate a backward move for **SeekRow**, pass a negative value in  _lRowCount_.</span></span> <span data-ttu-id="7d989-149">テーブルの先頭まで検索するには  _、lRowCount_ で 0 を渡し  _、bkOrigin_ の値BOOKMARK_BEGINNING渡します。</span><span class="sxs-lookup"><span data-stu-id="7d989-149">To search to the beginning of the table, pass zero in  _lRowCount_ and the value BOOKMARK_BEGINNING in  _bkOrigin_.</span></span> 
  
<span data-ttu-id="7d989-150">テーブルに多数の行がある場合 **、SeekRow** 操作が遅くなる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7d989-150">If there are lots of rows in the table, the **SeekRow** operation can be slow.</span></span> <span data-ttu-id="7d989-151">lplRowsSought パラメーターの内容で行数を返す必要がある場合にも、パフォーマンス  _が影響を受ける可能性_ があります。</span><span class="sxs-lookup"><span data-stu-id="7d989-151">Performance can also be affected if you require a row count to be returned in the contents of the  _lplRowsSought_ parameter.</span></span> 
  
 <span data-ttu-id="7d989-152">**SeekRow** は  _、lRowCount_ が指す変数で、実際に検索された行数 (正または負) を返します。</span><span class="sxs-lookup"><span data-stu-id="7d989-152">**SeekRow** returns the number of rows actually searched through, positive or negative, in the variable pointed to by  _lRowCount_.</span></span> <span data-ttu-id="7d989-153">通常の操作では、検索がテーブルの先頭または末尾に達しない限り _、lRowCount_ に渡された _lplRowsSought_ と同じ値を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d989-153">In ordinary operation, it should return the same value for  _lplRowsSought_ as passed in for  _lRowCount_, unless the search reached the beginning or end of the table.</span></span> 
  
<span data-ttu-id="7d989-154">_lRowCount を_ 50 より大きい数値に設定しない。</span><span class="sxs-lookup"><span data-stu-id="7d989-154">Do not set  _lRowCount_ to a number greater than 50.</span></span> <span data-ttu-id="7d989-155">より多くの行をシークするには [、IMAPITable::SeekRowApprox メソッドを使用](imapitable-seekrowapprox.md) します。</span><span class="sxs-lookup"><span data-stu-id="7d989-155">To seek through a larger number of rows, use the [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7d989-156">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="7d989-156">MFCMAPI reference</span></span>

<span data-ttu-id="7d989-157">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7d989-157">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7d989-158">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="7d989-158">**File**</span></span>|<span data-ttu-id="7d989-159">**関数**</span><span class="sxs-lookup"><span data-stu-id="7d989-159">**Function**</span></span>|<span data-ttu-id="7d989-160">**コメント**</span><span class="sxs-lookup"><span data-stu-id="7d989-160">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7d989-161">MAPIProcessor.cpp</span><span class="sxs-lookup"><span data-stu-id="7d989-161">MAPIProcessor.cpp</span></span>  <br/> |<span data-ttu-id="7d989-162">CMAPIProcessor::P rocessMailboxTable</span><span class="sxs-lookup"><span data-stu-id="7d989-162">CMAPIProcessor::ProcessMailboxTable</span></span>  <br/> |<span data-ttu-id="7d989-163">MFCMAPI では **、IMAPITable::SeekRow** メソッドを使用して、処理前にテーブルの先頭を検索します。</span><span class="sxs-lookup"><span data-stu-id="7d989-163">MFCMAPI uses the **IMAPITable::SeekRow** method to locate the beginning of the table before processing.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7d989-164">関連項目</span><span class="sxs-lookup"><span data-stu-id="7d989-164">See also</span></span>



[<span data-ttu-id="7d989-165">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="7d989-165">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="7d989-166">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="7d989-166">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="7d989-167">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="7d989-167">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="7d989-168">IMAPITable::SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="7d989-168">IMAPITable::SeekRowApprox</span></span>](imapitable-seekrowapprox.md)
  
[<span data-ttu-id="7d989-169">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7d989-169">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


<span data-ttu-id="7d989-170">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="7d989-170">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

