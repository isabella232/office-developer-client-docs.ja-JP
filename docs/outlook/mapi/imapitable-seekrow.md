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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 143ca03a5e98d638d29394f5c0803e349ab4de25
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800848"
---
# <a name="imapitableseekrow"></a><span data-ttu-id="21df9-103">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="21df9-103">IMAPITable::SeekRow</span></span>

  
  
<span data-ttu-id="21df9-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="21df9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="21df9-105">テーブル内の特定の位置にカーソルを移動します。</span><span class="sxs-lookup"><span data-stu-id="21df9-105">Moves the cursor to a specific position in the table.</span></span>
  
```cpp
HRESULT SeekRow(
BOOKMARK bkOrigin,
LONG lRowCount,
LONG FAR * lplRowsSought
);
```

## <a name="parameters"></a><span data-ttu-id="21df9-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="21df9-106">Parameters</span></span>

 <span data-ttu-id="21df9-107">_bkOrigin_</span><span class="sxs-lookup"><span data-stu-id="21df9-107">_bkOrigin_</span></span>
  
> <span data-ttu-id="21df9-108">[in]シーク操作の開始位置を識別するブックマークです。</span><span class="sxs-lookup"><span data-stu-id="21df9-108">[in] The bookmark identifying the starting position for the seek operation.</span></span> <span data-ttu-id="21df9-109">、 [IMAPITable::CreateBookmark](imapitable-createbookmark.md)メソッドを使用してブックマークを作成することができますか、次の定義済み値の 1 つ渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="21df9-109">A bookmark can be created using the [IMAPITable::CreateBookmark](imapitable-createbookmark.md) method, or one of the following predefined values can be passed.</span></span> 
    
<span data-ttu-id="21df9-110">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="21df9-110">BOOKMARK_BEGINNING</span></span> 
  
> <span data-ttu-id="21df9-111">テーブルの先頭からシーク操作を開始します。</span><span class="sxs-lookup"><span data-stu-id="21df9-111">Starts the seek operation from the beginning of the table.</span></span> 
    
<span data-ttu-id="21df9-112">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="21df9-112">BOOKMARK_CURRENT</span></span> 
  
> <span data-ttu-id="21df9-113">シーク操作は、カーソルが配置されているテーブル内の行から開始します。</span><span class="sxs-lookup"><span data-stu-id="21df9-113">Starts the seek operation from the row in the table where the cursor is located.</span></span> 
    
<span data-ttu-id="21df9-114">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="21df9-114">BOOKMARK_END</span></span> 
  
> <span data-ttu-id="21df9-115">テーブルの末尾からシーク操作を開始します。</span><span class="sxs-lookup"><span data-stu-id="21df9-115">Starts the seek operation from the end of the table.</span></span> 
    
 <span data-ttu-id="21df9-116">_lRowCount_</span><span class="sxs-lookup"><span data-stu-id="21df9-116">_lRowCount_</span></span>
  
> <span data-ttu-id="21df9-117">[in]移動する行の数の符号付きの数、ブックマークから、 _bkOrigin_パラメーターで識別されます。</span><span class="sxs-lookup"><span data-stu-id="21df9-117">[in] The signed count of the number of rows to move, starting from the bookmark identified by the  _bkOrigin_ parameter.</span></span> 
    
 <span data-ttu-id="21df9-118">_lplRowsSought_</span><span class="sxs-lookup"><span data-stu-id="21df9-118">_lplRowsSought_</span></span>
  
> <span data-ttu-id="21df9-119">[out]_LRowCount_がシーク操作で処理された行の数を入力すると、 _lplRowsSought_のポイントの有効なポインターである場合は、先の符号は、前方または後方検索の方向を示します。</span><span class="sxs-lookup"><span data-stu-id="21df9-119">[out] If  _lRowCount_ is a valid pointer on input,  _lplRowsSought_ points to the number of rows that were processed in the seek operation, the sign of which indicates the direction of search, forward or backward.</span></span> <span data-ttu-id="21df9-120">_LRowCount_が負の場合は、 _lplRowsSought_が負の値です。</span><span class="sxs-lookup"><span data-stu-id="21df9-120">If  _lRowCount_ is negative, then  _lplRowsSought_ is negative.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="21df9-121">�߂�l</span><span class="sxs-lookup"><span data-stu-id="21df9-121">Return value</span></span>

<span data-ttu-id="21df9-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="21df9-122">S_OK</span></span> 
  
> <span data-ttu-id="21df9-123">シーク操作が正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="21df9-123">The seek operation was successful.</span></span>
    
<span data-ttu-id="21df9-124">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="21df9-124">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="21df9-125">別の操作は、行のシーク操作の開始を防止する処理中です。</span><span class="sxs-lookup"><span data-stu-id="21df9-125">Another operation is in progress that prevents the row-seeking operation from starting.</span></span> <span data-ttu-id="21df9-126">実行中の操作を完了できるか、それを停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="21df9-126">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="21df9-127">MAPI_E_INVALID_BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="21df9-127">MAPI_E_INVALID_BOOKMARK</span></span> 
  
> <span data-ttu-id="21df9-128">削除されたため、または要求された最後の行を越えることがあるために、 _bkOrigin_パラメーターで指定されたブックマークは無効です。</span><span class="sxs-lookup"><span data-stu-id="21df9-128">The bookmark specified in the  _bkOrigin_ parameter is invalid because it was removed or because it is beyond the last row requested.</span></span> 
    
<span data-ttu-id="21df9-129">MAPI_W_POSITION_CHANGED</span><span class="sxs-lookup"><span data-stu-id="21df9-129">MAPI_W_POSITION_CHANGED</span></span> 
  
> <span data-ttu-id="21df9-130">呼び出しが成功したが、最後に使用されたときと同じ行に、 _bkOrigin_パラメーターで指定されたブックマークが設定されないことです。</span><span class="sxs-lookup"><span data-stu-id="21df9-130">The call succeeded, but the bookmark specified in the  _bkOrigin_ parameter is no longer set at the same row as it was when it was last used.</span></span> <span data-ttu-id="21df9-131">ブックマークが使用されていない場合は不要になった同じ位置に作成されたときと同じ</span><span class="sxs-lookup"><span data-stu-id="21df9-131">If the bookmark has not been used, it is no longer in the same position as it was when it was created.</span></span> <span data-ttu-id="21df9-132">この警告が返されると、呼び出しを成功として処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="21df9-132">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="21df9-133">この警告をテストするには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="21df9-133">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="21df9-134">詳細については、[エラーを処理するためのマクロの使用](using-macros-for-error-handling.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="21df9-134">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="21df9-135">備考</span><span class="sxs-lookup"><span data-stu-id="21df9-135">Remarks</span></span>

<span data-ttu-id="21df9-136">**IMAPITable::SeekRow**メソッドは、カーソルの新しい BOOKMARK_CURRENT の位置を確立します。</span><span class="sxs-lookup"><span data-stu-id="21df9-136">The **IMAPITable::SeekRow** method establishes a new BOOKMARK_CURRENT position for the cursor.</span></span> <span data-ttu-id="21df9-137">_LRowCount_パラメーターでは、カーソルを移動する行と移動の方向の数を示します。</span><span class="sxs-lookup"><span data-stu-id="21df9-137">The  _lRowCount_ parameter indicates the number of rows that the cursor moves and the direction of movement.</span></span> 
  
<span data-ttu-id="21df9-138">結果の位置がテーブルの最後の行以外の場合は、最後の行の後、カーソルが配置されます。</span><span class="sxs-lookup"><span data-stu-id="21df9-138">If the resulting position is beyond the last row of the table, the cursor is positioned after the last row.</span></span> <span data-ttu-id="21df9-139">結果の位置がテーブルの最初の行の前にある場合は、最初の行の先頭にカーソルが配置されます。</span><span class="sxs-lookup"><span data-stu-id="21df9-139">If the resulting position is before the first row of the table, the cursor is positioned at the beginning of the first row.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="21df9-140">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="21df9-140">Notes to implementers</span></span>

<span data-ttu-id="21df9-141">_BkOrigin_で指定された行がテーブルに存在していませんし、新しいブックマークの位置を確立することはできません、する場合は、MAPI_E_INVALID_BOOKMARK を返します。</span><span class="sxs-lookup"><span data-stu-id="21df9-141">If the row pointed to by  _bkOrigin_ no longer exists in the table and you cannot establish a new position for the bookmark, return MAPI_E_INVALID_BOOKMARK.</span></span> <span data-ttu-id="21df9-142">_BkOrigin_で指定された行が存在しないと、新しいブックマークの位置を確立することができます、MAPI_W_POSITION_CHANGED を返します。</span><span class="sxs-lookup"><span data-stu-id="21df9-142">If the row pointed to by  _bkOrigin_ no longer exists and you can establish a new position for the bookmark, return MAPI_W_POSITION_CHANGED.</span></span> 
  
<span data-ttu-id="21df9-143">テーブルの表示が折りたたまれている行を示すブックマークを使用することがまだできます。</span><span class="sxs-lookup"><span data-stu-id="21df9-143">A bookmark pointing to a row that is collapsed out of the table view can still be used.</span></span> <span data-ttu-id="21df9-144">呼び出し元がこのようなブックマークにカーソルを移動しようとすると場合、は、次の表示されている行にカーソルを移動し、MAPI_W_POSITION_CHANGED を返します。</span><span class="sxs-lookup"><span data-stu-id="21df9-144">If the caller attempts to move the cursor to such a bookmark, move the cursor to the next visible row and return MAPI_W_POSITION_CHANGED.</span></span> 
  
<span data-ttu-id="21df9-145">位置の使用時に、または行が折りたたまれているときに見えなくなり、折りたたまれているためにブックマークを移動することができます。</span><span class="sxs-lookup"><span data-stu-id="21df9-145">You can move bookmarks for positions collapsed out of view, either at the time of use or at the time that the row is collapsed.</span></span> <span data-ttu-id="21df9-146">ブックマークは、行が折りたたまれているときに移動する場合は、かを示すかどうか、ブックマークが最後に使用してから移動、ことはありませんが使用されて、作成されてからブックマークに少ししてください。</span><span class="sxs-lookup"><span data-stu-id="21df9-146">If a bookmark is moved at the time that the row is collapsed, keep a bit in the bookmark that indicates whether the bookmark has moved since its last use or, if it has never been used, since its creation.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="21df9-147">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="21df9-147">Notes to callers</span></span>

<span data-ttu-id="21df9-148">**SeekRow**の逆方向の移動を示す、 _lRowCount_の負の値を渡します。</span><span class="sxs-lookup"><span data-stu-id="21df9-148">To indicate a backward move for **SeekRow**, pass a negative value in  _lRowCount_.</span></span> <span data-ttu-id="21df9-149">テーブルの先頭を検索するには、 _lRowCount_と_bkOrigin_の BOOKMARK_BEGINNING の値に 0 を渡します。</span><span class="sxs-lookup"><span data-stu-id="21df9-149">To search to the beginning of the table, pass zero in  _lRowCount_ and the value BOOKMARK_BEGINNING in  _bkOrigin_.</span></span> 
  
<span data-ttu-id="21df9-150">多くのテーブル内の行がある場合は、 **SeekRow**操作が低下することができます。</span><span class="sxs-lookup"><span data-stu-id="21df9-150">If there are lots of rows in the table, the **SeekRow** operation can be slow.</span></span> <span data-ttu-id="21df9-151">パフォーマンスは、 _lplRowsSought_パラメーターの内容で返される行の数を必要とする場合にも影響します。</span><span class="sxs-lookup"><span data-stu-id="21df9-151">Performance can also be affected if you require a row count to be returned in the contents of the  _lplRowsSought_ parameter.</span></span> 
  
 <span data-ttu-id="21df9-152">**SeekRow**は、実際を検索、正または負の場合、 _lRowCount_が指す変数の行の数を返します。</span><span class="sxs-lookup"><span data-stu-id="21df9-152">**SeekRow** returns the number of rows actually searched through, positive or negative, in the variable pointed to by  _lRowCount_.</span></span> <span data-ttu-id="21df9-153">通常の操作で、返す必要があります_lplRowsSought_の値が同じように_lRowCount_、ために渡された検索は先頭またはテーブルの末尾に到達しない限り。</span><span class="sxs-lookup"><span data-stu-id="21df9-153">In ordinary operation, it should return the same value for  _lplRowsSought_ as passed in for  _lRowCount_, unless the search reached the beginning or end of the table.</span></span> 
  
<span data-ttu-id="21df9-154">設定しないで_lRowCount_を番号に 50 を超える。</span><span class="sxs-lookup"><span data-stu-id="21df9-154">Do not set  _lRowCount_ to a number greater than 50.</span></span> <span data-ttu-id="21df9-155">多数の行をシーク、 [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="21df9-155">To seek through a larger number of rows, use the [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="21df9-156">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="21df9-156">MFCMAPI reference</span></span>

<span data-ttu-id="21df9-157">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="21df9-157">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="21df9-158">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="21df9-158">**File**</span></span>|<span data-ttu-id="21df9-159">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="21df9-159">**Function**</span></span>|<span data-ttu-id="21df9-160">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="21df9-160">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="21df9-161">MAPIProcessor.cpp</span><span class="sxs-lookup"><span data-stu-id="21df9-161">MAPIProcessor.cpp</span></span>  <br/> |<span data-ttu-id="21df9-162">CMAPIProcessor::ProcessMailboxTable</span><span class="sxs-lookup"><span data-stu-id="21df9-162">CMAPIProcessor::ProcessMailboxTable</span></span>  <br/> |<span data-ttu-id="21df9-163">MFCMAPI では、 **IMAPITable::SeekRow**メソッドを使用して、処理する前にテーブルの先頭を見つけます。</span><span class="sxs-lookup"><span data-stu-id="21df9-163">MFCMAPI uses the **IMAPITable::SeekRow** method to locate the beginning of the table before processing.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="21df9-164">関連項目</span><span class="sxs-lookup"><span data-stu-id="21df9-164">See also</span></span>



[<span data-ttu-id="21df9-165">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="21df9-165">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="21df9-166">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="21df9-166">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="21df9-167">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="21df9-167">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="21df9-168">IMAPITable::SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="21df9-168">IMAPITable::SeekRowApprox</span></span>](imapitable-seekrowapprox.md)
  
[<span data-ttu-id="21df9-169">IMAPITable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="21df9-169">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


<span data-ttu-id="21df9-170">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="21df9-170">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

