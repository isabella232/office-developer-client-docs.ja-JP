---
title: IMAPITableQueryRows
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QueryRows
api_type:
- COM
ms.assetid: f26384f1-467e-4343-92b3-0425da9d2123
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: a6659f64f6e8d2e3dc61819b2263efe672cdd15c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800865"
---
# <a name="imapitablequeryrows"></a><span data-ttu-id="eecf3-103">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="eecf3-103">IMAPITable::QueryRows</span></span>

  
  
<span data-ttu-id="eecf3-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="eecf3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="eecf3-105">現在のカーソル位置から開始し、テーブルから 1 つまたは複数の行を返します。</span><span class="sxs-lookup"><span data-stu-id="eecf3-105">Returns one or more rows from a table, beginning at the current cursor position.</span></span>
  
```cpp
HRESULT QueryRows(
LONG lRowCount,
ULONG ulFlags,
LPSRowSet FAR * lppRows
);
```

## <a name="parameters"></a><span data-ttu-id="eecf3-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="eecf3-106">Parameters</span></span>

 <span data-ttu-id="eecf3-107">_lRowCount_</span><span class="sxs-lookup"><span data-stu-id="eecf3-107">_lRowCount_</span></span>
  
> <span data-ttu-id="eecf3-108">[in]返される行の最大数。</span><span class="sxs-lookup"><span data-stu-id="eecf3-108">[in] Maximum number of rows to be returned.</span></span>
    
 <span data-ttu-id="eecf3-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="eecf3-109">_ulFlags_</span></span>
  
> <span data-ttu-id="eecf3-110">[in]行を返す方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="eecf3-110">[in] Bitmask of flags that control how rows are returned.</span></span> <span data-ttu-id="eecf3-111">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="eecf3-111">The following flag can be set:</span></span>
    
<span data-ttu-id="eecf3-112">TBL_NOADVANCE</span><span class="sxs-lookup"><span data-stu-id="eecf3-112">TBL_NOADVANCE</span></span> 
  
> <span data-ttu-id="eecf3-113">カーソルが行の取得の結果として進化するを防ぎます。</span><span class="sxs-lookup"><span data-stu-id="eecf3-113">Prevents the cursor from advancing as a result of the row retrieval.</span></span> <span data-ttu-id="eecf3-114">TBL_NOADVANCE フラグが設定されている場合、カーソルが指す最初の行が返されます。</span><span class="sxs-lookup"><span data-stu-id="eecf3-114">If the TBL_NOADVANCE flag is set, the cursor points to the first row returned.</span></span> <span data-ttu-id="eecf3-115">TBL_NOADVANCE フラグが設定されていない場合、カーソルは、返された最後の行を次の行をポイントします。</span><span class="sxs-lookup"><span data-stu-id="eecf3-115">If the TBL_NOADVANCE flag is not set, the cursor points to the row following the last row returned.</span></span>
    
 <span data-ttu-id="eecf3-116">_lppRows_</span><span class="sxs-lookup"><span data-stu-id="eecf3-116">_lppRows_</span></span>
  
> <span data-ttu-id="eecf3-117">[out]テーブルの行を保持している[SRowSet](srowset.md)構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="eecf3-117">[out] Pointer to a pointer to an [SRowSet](srowset.md) structure holding the table rows.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="eecf3-118">�߂�l</span><span class="sxs-lookup"><span data-stu-id="eecf3-118">Return value</span></span>

<span data-ttu-id="eecf3-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="eecf3-119">S_OK</span></span> 
  
> <span data-ttu-id="eecf3-120">行は正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="eecf3-120">The rows were successfully returned.</span></span>
    
<span data-ttu-id="eecf3-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="eecf3-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="eecf3-122">別の操作は、行の取得操作の開始を防止する処理中です。</span><span class="sxs-lookup"><span data-stu-id="eecf3-122">Another operation is in progress that prevents the row retrieval operation from starting.</span></span> <span data-ttu-id="eecf3-123">実行中の操作を完了できるか、それを停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eecf3-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="eecf3-124">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="eecf3-124">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="eecf3-125">_IRowCount_パラメーターは、0 に設定されています。</span><span class="sxs-lookup"><span data-stu-id="eecf3-125">The  _IRowCount_ parameter is set to zero.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="eecf3-126">備考</span><span class="sxs-lookup"><span data-stu-id="eecf3-126">Remarks</span></span>

<span data-ttu-id="eecf3-127">**IMAPITable::QueryRows**メソッドは、テーブルから 1 つまたは複数行のデータを取得します。</span><span class="sxs-lookup"><span data-stu-id="eecf3-127">The **IMAPITable::QueryRows** method gets one or more rows of data from a table.</span></span> <span data-ttu-id="eecf3-128">_IRowCount_パラメーターの値は、検索の開始点に影響します。</span><span class="sxs-lookup"><span data-stu-id="eecf3-128">The value of the  _IRowCount_ parameter affects the starting point for the retrieval.</span></span> <span data-ttu-id="eecf3-129">_IRowCount_が正の場合は、現在位置から前方に行が読み取られます。</span><span class="sxs-lookup"><span data-stu-id="eecf3-129">If  _IRowCount_ is positive, rows are read in a forward direction, starting at the current position.</span></span> <span data-ttu-id="eecf3-130">_IRowCount_が負の場合は、**スプーラー**は、指定された行の数を逆方向に移動開始点をリセットします。</span><span class="sxs-lookup"><span data-stu-id="eecf3-130">If  _IRowCount_ is negative, **QueryRows** resets the starting point by moving backward the indicated number of rows.</span></span> <span data-ttu-id="eecf3-131">カーソルをリセットした後は、前方の順序で行が読み取られます。</span><span class="sxs-lookup"><span data-stu-id="eecf3-131">After the cursor is reset, rows are read in forward order.</span></span> 
  
<span data-ttu-id="eecf3-132">[SRowSet](srowset.md)構造体を_lppRows_パラメーターが指す**カラス**のメンバーでは、返される行の数を示します。</span><span class="sxs-lookup"><span data-stu-id="eecf3-132">The **cRows** member in the [SRowSet](srowset.md) structure pointed to by the  _lppRows_ parameter indicates the number of rows returned.</span></span> <span data-ttu-id="eecf3-133">場合は 0 個の行が返されます。</span><span class="sxs-lookup"><span data-stu-id="eecf3-133">If zero rows are returned:</span></span> 
  
- <span data-ttu-id="eecf3-134">テーブルの先頭にカーソルが位置し、 _IRowCount_の値が負の値です。</span><span class="sxs-lookup"><span data-stu-id="eecf3-134">The cursor was already positioned at the beginning of the table and the value of  _IRowCount_ is negative.</span></span> <span data-ttu-id="eecf3-135">- または -</span><span class="sxs-lookup"><span data-stu-id="eecf3-135">-Or-</span></span> 
    
- <span data-ttu-id="eecf3-136">テーブルの末尾にカーソルが既に配置されているし、 _IRowCount_の値が正の数値です。</span><span class="sxs-lookup"><span data-stu-id="eecf3-136">The cursor was already positioned at the end of the table and the value of  _IRowCount_ is positive.</span></span> 
    
<span data-ttu-id="eecf3-137">列とその順序の数は、行ごとに同じです。</span><span class="sxs-lookup"><span data-stu-id="eecf3-137">The number of columns and their ordering is the same for each row.</span></span> <span data-ttu-id="eecf3-138">行のプロパティが存在しません、またはプロパティを読み取り中にエラーがありますが、行のプロパティに [ **SPropValue**構造体には、次の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="eecf3-138">If a property does not exist for a row or there is an error reading a property, the **SPropValue** structure for the property in the row contains the following values:</span></span> 
  
- <span data-ttu-id="eecf3-139">**UlPropTag**メンバーのプロパティの型の PT_ERROR。</span><span class="sxs-lookup"><span data-stu-id="eecf3-139">PT_ERROR for the property type in the **ulPropTag** member.</span></span> 
    
- <span data-ttu-id="eecf3-140">**値**メンバーの MAPI_E_NOT_FOUND。</span><span class="sxs-lookup"><span data-stu-id="eecf3-140">MAPI_E_NOT_FOUND for the **Value** member.</span></span> 
    
<span data-ttu-id="eecf3-141">_LppRows_パラメーターで指定された行セット内の[SPropValue](spropvalue.md)構造体に使用されるメモリ必要があります個別に割り当てられ、行ごとに解放します。</span><span class="sxs-lookup"><span data-stu-id="eecf3-141">Memory used for the [SPropValue](spropvalue.md) structures in the row set pointed to by the  _lppRows_ parameter must be separately allocated and freed for each row.</span></span> <span data-ttu-id="eecf3-142">[MAPIFreeBuffer](mapifreebuffer.md)を使用して、プロパティ値の構造体を解放して行を解放するために設定します。</span><span class="sxs-lookup"><span data-stu-id="eecf3-142">Use [MAPIFreeBuffer](mapifreebuffer.md) to free the property value structures and to free the row set.</span></span> <span data-ttu-id="eecf3-143">**スプーラー**への呼び出しでは、0 を返す、ただし、先頭または末尾の表に示す**SRowSet**構造のみ必要がありますが解放されます。</span><span class="sxs-lookup"><span data-stu-id="eecf3-143">When a call to **QueryRows** returns zero, however, indicating the beginning or end of the table, only the **SRowSet** structure itself needs to be freed.</span></span> <span data-ttu-id="eecf3-144">割り当ておよび**SRowSet**構造体にメモリを解放する方法の詳細については、 [ADRLIST および SRowSet 構造体のメモリを管理する](managing-memory-for-adrlist-and-srowset-structures.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="eecf3-144">For more information about how to allocate and free memory in an **SRowSet** structure, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
<span data-ttu-id="eecf3-145">返される行とは、返される順序は、かどうか成功した呼び出しに加えられた[IMAPITable::Restrict](imapitable-restrict.md)および[IMAPITable::SortTable](imapitable-sorttable.md)によって異なります。</span><span class="sxs-lookup"><span data-stu-id="eecf3-145">The rows that are returned and the order in which they are returned depend on whether or not successful calls have been made to [IMAPITable::Restrict](imapitable-restrict.md) and [IMAPITable::SortTable](imapitable-sorttable.md).</span></span> <span data-ttu-id="eecf3-146">**制限**は、制限で指定された条件に一致する行だけを返すには、**スプーラー**の原因と、ビューから行をフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="eecf3-146">**Restrict** filters rows from the view, causing **QueryRows** to return only the rows that match the criteria specified in the restriction.</span></span> <span data-ttu-id="eecf3-147">**SortTable**は、標準を確立または**スプーラー**によって返される行の順序に影響を与えず、並べ替え順序を分類します。</span><span class="sxs-lookup"><span data-stu-id="eecf3-147">**SortTable** establishes a standard or categorized sort order, affecting the sequence of rows returned by **QueryRows**.</span></span> <span data-ttu-id="eecf3-148">**SortTable**に渡された[SSortOrderSet](ssortorderset.md)の構造体で指定された順序では、返される行です。</span><span class="sxs-lookup"><span data-stu-id="eecf3-148">The returned rows are in the order specified in the [SSortOrderSet](ssortorderset.md) structure passed to **SortTable**.</span></span>
  
<span data-ttu-id="eecf3-149">行ごとに列が返されに[IMAPITable::SetColumns](imapitable-setcolumns.md)するかどうかの正常な呼び出しがありましたが返される順序に依存しています。</span><span class="sxs-lookup"><span data-stu-id="eecf3-149">The columns returned for each row and the order in which they are returned depend on whether or not a successful call has been made to [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span> <span data-ttu-id="eecf3-150">**SetColumns**では、テーブルと、それらを含めるように順序の列に含まれるプロパティを指定する、列のセットを確立します。</span><span class="sxs-lookup"><span data-stu-id="eecf3-150">**SetColumns** establishes a column set, specifying the properties to be included in columns in the table and the order in which they should be included.</span></span> <span data-ttu-id="eecf3-151">**SetColumns**呼び出しを行った場合それぞれの行と列の順序で特定の列の設定の呼び出しで指定した列と同じです。</span><span class="sxs-lookup"><span data-stu-id="eecf3-151">If a **SetColumns** call has been made, the particular columns in each row and the order of those columns match the column set specified in the call.</span></span> <span data-ttu-id="eecf3-152">**SetColumns**呼び出しが作成されなかった場合、テーブルは、既定の列セットを返します。</span><span class="sxs-lookup"><span data-stu-id="eecf3-152">If no **SetColumns** call has been made, the table returns its default column set.</span></span> 
  
<span data-ttu-id="eecf3-153">なしのこれらの呼び出しを行った場合は、**スプーラー**はテーブルのすべての行を返します。</span><span class="sxs-lookup"><span data-stu-id="eecf3-153">If none of these calls has been made, **QueryRows** returns all of the rows in the table.</span></span> <span data-ttu-id="eecf3-154">各行には、既定の順序で設定する既定の列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="eecf3-154">Each row contains the default column set in default order.</span></span> 
  
<span data-ttu-id="eecf3-155">[IMAPITable::SetColumns](imapitable-setcolumns.md)への呼び出しで確立された列のセットには、PR_NULL に設定された列が含まれている_lppRows_で返される行セット内で[SPropValue](spropvalue.md)配列に空のスロットが含まれます。</span><span class="sxs-lookup"><span data-stu-id="eecf3-155">When the column set established in a call to [IMAPITable::SetColumns](imapitable-setcolumns.md) includes columns set to PR_NULL, the [SPropValue](spropvalue.md) array within the row set returned in  _lppRows_ will contain empty slots.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="eecf3-156">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="eecf3-156">Notes to implementers</span></span>

<span data-ttu-id="eecf3-157">列セットに含まれる、サポートされていない列を要求する呼び出し元を許可できます。</span><span class="sxs-lookup"><span data-stu-id="eecf3-157">You can allow a caller to request an unsupported column to be included in the column set.</span></span> <span data-ttu-id="eecf3-158">この問題が発生したときは、サポートされていない列のプロパティの値のプロパティ タグは MAPI_E_NOT_FOUND のプロパティの型の部分で PT_ERROR を配置します。</span><span class="sxs-lookup"><span data-stu-id="eecf3-158">When this occurs, place PT_ERROR in the property type portion of the property tag and MAPI_E_NOT_FOUND in the property value for the unsupported column.</span></span> 
  
<span data-ttu-id="eecf3-159">要件ではなく、要求には、ローの数を処理します。</span><span class="sxs-lookup"><span data-stu-id="eecf3-159">Treat the row count as a request rather than a requirement.</span></span> <span data-ttu-id="eecf3-160">返品できます任意の場所から 0 個の行では、要求数、クエリの方向に行がない場合。</span><span class="sxs-lookup"><span data-stu-id="eecf3-160">You can return anywhere from zero rows, if there are no rows in the direction of the query, to the number requested.</span></span> 
  
<span data-ttu-id="eecf3-161">ユーザーに表示される行を分類した表のビューでは、要求時にデータの範囲について、有効な判断を行うし、余分な作業を避けるために呼び出し元を許可する行のみを返します。</span><span class="sxs-lookup"><span data-stu-id="eecf3-161">Return only the rows that the user will see when rows are requested from a categorized table view, allowing the caller to make valid assumptions about the scope of the data and avoid extra work.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="eecf3-162">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="eecf3-162">Notes to callers</span></span>

<span data-ttu-id="eecf3-163">通常は最終的に、 _lRowCount_パラメーターで指定した数の行です。</span><span class="sxs-lookup"><span data-stu-id="eecf3-163">Usually you will end up with as many rows as you have specified in the  _lRowCount_ parameter.</span></span> <span data-ttu-id="eecf3-164">ただし、メモリまたは実装の制限が問題である場合、または操作に達すると、テーブルの前後処理の途中では、**スプーラー**は要求されたよりも行数が少ないを返します。</span><span class="sxs-lookup"><span data-stu-id="eecf3-164">However, when memory or implementation limits are an issue or when the operation reaches the beginning or end of the table prematurely, **QueryRows** will return less rows than requested.</span></span> 
  
<span data-ttu-id="eecf3-165">**スプーラー**では、MAPI_E_BUSY が返された場合は、 [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md)メソッドを呼び出すし、非同期操作が完了すると、**スプーラー**への呼び出しを再試行してください。</span><span class="sxs-lookup"><span data-stu-id="eecf3-165">If **QueryRows** returns MAPI_E_BUSY, call the [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) method and retry the call to **QueryRows** when the asynchronous operation is complete.</span></span> 
  
<span data-ttu-id="eecf3-166">**スプーラー**を呼び出すときは、非同期通知のタイミングになる戻る**スプーラー**から基になるデータを正確に表現する行セットを引き起こす可能性ことに注意します。</span><span class="sxs-lookup"><span data-stu-id="eecf3-166">When calling **QueryRows**, be aware that the timing of asynchronous notifications can potentially cause the row set that you get back from **QueryRows** not to accurately represent the underlying data.</span></span> <span data-ttu-id="eecf3-167">たとえば、メッセージが対応する通知の受信前に削除する削除された行の行に返されると、フォルダーの内容の表の次に**スプーラー**に呼び出しを設定します。</span><span class="sxs-lookup"><span data-stu-id="eecf3-167">For example, a call to **QueryRows** to a folder's contents table following the deletion of a message but prior to the receipt of the corresponding notification will cause the deleted row to be returned in the row set.</span></span> <span data-ttu-id="eecf3-168">常に通知データのユーザーのビューを更新する前に到着するまで待機します。</span><span class="sxs-lookup"><span data-stu-id="eecf3-168">Always wait for a notification to arrive before updating the user's view of the data.</span></span> 
  
<span data-ttu-id="eecf3-169">テーブルから行を取得する方法の詳細については、[テーブルの行からのデータの取得](retrieving-data-from-table-rows.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="eecf3-169">For more information about retrieving rows from tables, see [Retrieving Data from Table Rows](retrieving-data-from-table-rows.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="eecf3-170">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="eecf3-170">MFCMAPI reference</span></span>

<span data-ttu-id="eecf3-171">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="eecf3-171">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="eecf3-172">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="eecf3-172">**File**</span></span>|<span data-ttu-id="eecf3-173">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="eecf3-173">**Function**</span></span>|<span data-ttu-id="eecf3-174">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="eecf3-174">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="eecf3-175">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="eecf3-175">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="eecf3-176">DwThreadFuncLoadTable</span><span class="sxs-lookup"><span data-stu-id="eecf3-176">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="eecf3-177">MFCMAPI では、 **IMAPITable::QueryRows**メソッドを使用して、ビューにロードするテーブル内の行を取得します。</span><span class="sxs-lookup"><span data-stu-id="eecf3-177">MFCMAPI uses the **IMAPITable::QueryRows** method to retrieve rows in the table to load into the view.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eecf3-178">関連項目</span><span class="sxs-lookup"><span data-stu-id="eecf3-178">See also</span></span>



[<span data-ttu-id="eecf3-179">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="eecf3-179">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="eecf3-180">FreeProws</span><span class="sxs-lookup"><span data-stu-id="eecf3-180">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="eecf3-181">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="eecf3-181">HrQueryAllRows</span></span>](hrqueryallrows.md)
  
[<span data-ttu-id="eecf3-182">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="eecf3-182">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="eecf3-183">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="eecf3-183">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="eecf3-184">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="eecf3-184">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md)
  
[<span data-ttu-id="eecf3-185">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="eecf3-185">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="eecf3-186">SRow</span><span class="sxs-lookup"><span data-stu-id="eecf3-186">SRow</span></span>](srow.md)
  
[<span data-ttu-id="eecf3-187">SRowSet</span><span class="sxs-lookup"><span data-stu-id="eecf3-187">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="eecf3-188">IMAPITable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="eecf3-188">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


<span data-ttu-id="eecf3-189">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="eecf3-189">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

