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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 26d6ffe66a5e7749c9d8c4e5210e9f72de808932
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416294"
---
# <a name="imapitablequeryrows"></a><span data-ttu-id="7dd19-103">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="7dd19-103">IMAPITable::QueryRows</span></span>

  
  
<span data-ttu-id="7dd19-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7dd19-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7dd19-105">現在のカーソル位置から始まる、テーブルから 1 つ以上の行を返します。</span><span class="sxs-lookup"><span data-stu-id="7dd19-105">Returns one or more rows from a table, beginning at the current cursor position.</span></span>
  
```cpp
HRESULT QueryRows(
LONG lRowCount,
ULONG ulFlags,
LPSRowSet FAR * lppRows
);
```

## <a name="parameters"></a><span data-ttu-id="7dd19-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7dd19-106">Parameters</span></span>

 <span data-ttu-id="7dd19-107">_lRowCount_</span><span class="sxs-lookup"><span data-stu-id="7dd19-107">_lRowCount_</span></span>
  
> <span data-ttu-id="7dd19-108">[in]返される行の最大数。</span><span class="sxs-lookup"><span data-stu-id="7dd19-108">[in] Maximum number of rows to be returned.</span></span>
    
 <span data-ttu-id="7dd19-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7dd19-109">_ulFlags_</span></span>
  
> <span data-ttu-id="7dd19-110">[in]行の返し方を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="7dd19-110">[in] Bitmask of flags that control how rows are returned.</span></span> <span data-ttu-id="7dd19-111">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="7dd19-111">The following flag can be set:</span></span>
    
<span data-ttu-id="7dd19-112">TBL_NOADVANCE</span><span class="sxs-lookup"><span data-stu-id="7dd19-112">TBL_NOADVANCE</span></span> 
  
> <span data-ttu-id="7dd19-113">行の取得の結果としてカーソルが進むのを防ぐ。</span><span class="sxs-lookup"><span data-stu-id="7dd19-113">Prevents the cursor from advancing as a result of the row retrieval.</span></span> <span data-ttu-id="7dd19-114">このフラグTBL_NOADVANCE設定すると、カーソルは返される最初の行をポイントします。</span><span class="sxs-lookup"><span data-stu-id="7dd19-114">If the TBL_NOADVANCE flag is set, the cursor points to the first row returned.</span></span> <span data-ttu-id="7dd19-115">このフラグTBL_NOADVANCE設定されていない場合、カーソルは最後に返された行の後の行をポイントします。</span><span class="sxs-lookup"><span data-stu-id="7dd19-115">If the TBL_NOADVANCE flag is not set, the cursor points to the row following the last row returned.</span></span>
    
 <span data-ttu-id="7dd19-116">_lppRows_</span><span class="sxs-lookup"><span data-stu-id="7dd19-116">_lppRows_</span></span>
  
> <span data-ttu-id="7dd19-117">[out]テーブルの行を保持する [SRowSet](srowset.md) 構造体へのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="7dd19-117">[out] Pointer to a pointer to an [SRowSet](srowset.md) structure holding the table rows.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7dd19-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="7dd19-118">Return value</span></span>

<span data-ttu-id="7dd19-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="7dd19-119">S_OK</span></span> 
  
> <span data-ttu-id="7dd19-120">行が正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="7dd19-120">The rows were successfully returned.</span></span>
    
<span data-ttu-id="7dd19-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="7dd19-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="7dd19-122">行の取得操作が開始されるのを防ぐ別の操作が進行中です。</span><span class="sxs-lookup"><span data-stu-id="7dd19-122">Another operation is in progress that prevents the row retrieval operation from starting.</span></span> <span data-ttu-id="7dd19-123">進行中の操作の完了を許可するか、停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7dd19-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="7dd19-124">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7dd19-124">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="7dd19-125">_IRowCount パラメーター_ は 0 に設定されます。</span><span class="sxs-lookup"><span data-stu-id="7dd19-125">The  _IRowCount_ parameter is set to zero.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7dd19-126">注釈</span><span class="sxs-lookup"><span data-stu-id="7dd19-126">Remarks</span></span>

<span data-ttu-id="7dd19-127">**IMAPITable::QueryRows** メソッドは、テーブルから 1 行以上のデータを取得します。</span><span class="sxs-lookup"><span data-stu-id="7dd19-127">The **IMAPITable::QueryRows** method gets one or more rows of data from a table.</span></span> <span data-ttu-id="7dd19-128">_IRowCount パラメーターの値_ は、取得の開始点に影響します。</span><span class="sxs-lookup"><span data-stu-id="7dd19-128">The value of the  _IRowCount_ parameter affects the starting point for the retrieval.</span></span> <span data-ttu-id="7dd19-129">_IRowCount が正_ の場合、行は現在の位置から順方向に読み取ります。</span><span class="sxs-lookup"><span data-stu-id="7dd19-129">If  _IRowCount_ is positive, rows are read in a forward direction, starting at the current position.</span></span> <span data-ttu-id="7dd19-130">_IRowCount が_ 負の場合 **、QueryRows は** 指定された行数を後方に移動して開始点をリセットします。</span><span class="sxs-lookup"><span data-stu-id="7dd19-130">If  _IRowCount_ is negative, **QueryRows** resets the starting point by moving backward the indicated number of rows.</span></span> <span data-ttu-id="7dd19-131">カーソルがリセットされた後、行は順方向に読み取りされます。</span><span class="sxs-lookup"><span data-stu-id="7dd19-131">After the cursor is reset, rows are read in forward order.</span></span> 
  
<span data-ttu-id="7dd19-132">**lppRows** パラメーターが指す [SRowSet](srowset.md)構造体の _cRows_ メンバーは、返される行数を示します。</span><span class="sxs-lookup"><span data-stu-id="7dd19-132">The **cRows** member in the [SRowSet](srowset.md) structure pointed to by the  _lppRows_ parameter indicates the number of rows returned.</span></span> <span data-ttu-id="7dd19-133">0 行が返される場合は、次の処理を行います。</span><span class="sxs-lookup"><span data-stu-id="7dd19-133">If zero rows are returned:</span></span> 
  
- <span data-ttu-id="7dd19-134">カーソルはテーブルの先頭に既に配置され  _、IRowCount_ の値は負の値です。</span><span class="sxs-lookup"><span data-stu-id="7dd19-134">The cursor was already positioned at the beginning of the table and the value of  _IRowCount_ is negative.</span></span> <span data-ttu-id="7dd19-135">-Or-</span><span class="sxs-lookup"><span data-stu-id="7dd19-135">-Or-</span></span> 
    
- <span data-ttu-id="7dd19-136">カーソルはテーブルの末尾に既に配置され  _、IRowCount_ の値は正の値です。</span><span class="sxs-lookup"><span data-stu-id="7dd19-136">The cursor was already positioned at the end of the table and the value of  _IRowCount_ is positive.</span></span> 
    
<span data-ttu-id="7dd19-137">列の数とその順序は、各行で同じです。</span><span class="sxs-lookup"><span data-stu-id="7dd19-137">The number of columns and their ordering is the same for each row.</span></span> <span data-ttu-id="7dd19-138">行に対してプロパティが存在しない場合、またはプロパティの読み取りエラーが発生した場合、行のプロパティ **の SPropValue** 構造体には、次の値が含まれます。</span><span class="sxs-lookup"><span data-stu-id="7dd19-138">If a property does not exist for a row or there is an error reading a property, the **SPropValue** structure for the property in the row contains the following values:</span></span> 
  
- <span data-ttu-id="7dd19-139">PT_ERRORのプロパティの種類を **指定** します。</span><span class="sxs-lookup"><span data-stu-id="7dd19-139">PT_ERROR for the property type in the **ulPropTag** member.</span></span> 
    
- <span data-ttu-id="7dd19-140">MAPI_E_NOT_FOUNDメンバー **の値を指定** します。</span><span class="sxs-lookup"><span data-stu-id="7dd19-140">MAPI_E_NOT_FOUND for the **Value** member.</span></span> 
    
<span data-ttu-id="7dd19-141">_lppRows_ パラメーターが指す行セット内の [SPropValue](spropvalue.md)構造体に使用されるメモリは、行ごとに個別に割り当て、解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7dd19-141">Memory used for the [SPropValue](spropvalue.md) structures in the row set pointed to by the  _lppRows_ parameter must be separately allocated and freed for each row.</span></span> <span data-ttu-id="7dd19-142">[MAPIFreeBuffer を使用して](mapifreebuffer.md)、プロパティ値構造を解放し、行セットを解放します。</span><span class="sxs-lookup"><span data-stu-id="7dd19-142">Use [MAPIFreeBuffer](mapifreebuffer.md) to free the property value structures and to free the row set.</span></span> <span data-ttu-id="7dd19-143">**ただし、QueryRows** の呼び出しが 0 を返す場合、テーブルの先頭または末尾を示す場合は **、SRowSet** 構造体自体のみを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7dd19-143">When a call to **QueryRows** returns zero, however, indicating the beginning or end of the table, only the **SRowSet** structure itself needs to be freed.</span></span> <span data-ttu-id="7dd19-144">SRowSet 構造体でメモリを割り当て、解放する方法の詳細については [、「ADRLIST](managing-memory-for-adrlist-and-srowset-structures.md)および **SRowSet** 構造体のメモリの管理」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7dd19-144">For more information about how to allocate and free memory in an **SRowSet** structure, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
<span data-ttu-id="7dd19-145">返される行と、返される順序は [、IMAPITable::Restrict](imapitable-restrict.md) と [IMAPITable::SortTable](imapitable-sorttable.md)に対して正常に呼び出されたかどうかによって異なされます。</span><span class="sxs-lookup"><span data-stu-id="7dd19-145">The rows that are returned and the order in which they are returned depend on whether or not successful calls have been made to [IMAPITable::Restrict](imapitable-restrict.md) and [IMAPITable::SortTable](imapitable-sorttable.md).</span></span> <span data-ttu-id="7dd19-146">**ビュー** からフィルター行を制限すると **、QueryRows** は制限で指定された条件に一致する行のみを返します。</span><span class="sxs-lookup"><span data-stu-id="7dd19-146">**Restrict** filters rows from the view, causing **QueryRows** to return only the rows that match the criteria specified in the restriction.</span></span> <span data-ttu-id="7dd19-147">**SortTable は** 、標準または分類された並べ替え順序を確立し **、QueryRows** によって返される行のシーケンスに影響します。</span><span class="sxs-lookup"><span data-stu-id="7dd19-147">**SortTable** establishes a standard or categorized sort order, affecting the sequence of rows returned by **QueryRows**.</span></span> <span data-ttu-id="7dd19-148">返される行は **、SortTable** に渡される [SSortOrderSet](ssortorderset.md)構造体で指定された順序です。</span><span class="sxs-lookup"><span data-stu-id="7dd19-148">The returned rows are in the order specified in the [SSortOrderSet](ssortorderset.md) structure passed to **SortTable**.</span></span>
  
<span data-ttu-id="7dd19-149">各行に対して返される列と、返される順序は [、IMAPITable::SetColumns](imapitable-setcolumns.md)に対して正常に呼び出されたかどうかによって異なる。</span><span class="sxs-lookup"><span data-stu-id="7dd19-149">The columns returned for each row and the order in which they are returned depend on whether or not a successful call has been made to [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span> <span data-ttu-id="7dd19-150">**SetColumns は** 列セットを確立し、テーブル内の列に含めるプロパティと、その列を含める順序を指定します。</span><span class="sxs-lookup"><span data-stu-id="7dd19-150">**SetColumns** establishes a column set, specifying the properties to be included in columns in the table and the order in which they should be included.</span></span> <span data-ttu-id="7dd19-151">**SetColumns 呼** び出しが行われた場合、各行の特定の列とそれらの列の順序は、呼び出しで指定された列セットと一致します。</span><span class="sxs-lookup"><span data-stu-id="7dd19-151">If a **SetColumns** call has been made, the particular columns in each row and the order of those columns match the column set specified in the call.</span></span> <span data-ttu-id="7dd19-152">**SetColumns 呼び出し** が行われた場合、テーブルは既定の列セットを返します。</span><span class="sxs-lookup"><span data-stu-id="7dd19-152">If no **SetColumns** call has been made, the table returns its default column set.</span></span> 
  
<span data-ttu-id="7dd19-153">これらの呼び出しが行われた場合 **、QueryRows は** テーブル内のすべての行を返します。</span><span class="sxs-lookup"><span data-stu-id="7dd19-153">If none of these calls has been made, **QueryRows** returns all of the rows in the table.</span></span> <span data-ttu-id="7dd19-154">各行には、既定の列セットが既定の順序で含まれる。</span><span class="sxs-lookup"><span data-stu-id="7dd19-154">Each row contains the default column set in default order.</span></span> 
  
<span data-ttu-id="7dd19-155">[IMAPITable::SetColumns](imapitable-setcolumns.md)への呼び出しで確立された列セットに PR_NULL に設定された列が含まれている場合 _、lppRows_ で返される行セット内の [SPropValue](spropvalue.md)配列には空のスロットが含まれます。</span><span class="sxs-lookup"><span data-stu-id="7dd19-155">When the column set established in a call to [IMAPITable::SetColumns](imapitable-setcolumns.md) includes columns set to PR_NULL, the [SPropValue](spropvalue.md) array within the row set returned in  _lppRows_ will contain empty slots.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7dd19-156">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="7dd19-156">Notes to implementers</span></span>

<span data-ttu-id="7dd19-157">呼び出し元が、サポートされていない列を列セットに含める要求を許可できます。</span><span class="sxs-lookup"><span data-stu-id="7dd19-157">You can allow a caller to request an unsupported column to be included in the column set.</span></span> <span data-ttu-id="7dd19-158">この場合は、プロパティ PT_ERRORのプロパティの種類の部分に配置し、サポートされていない列MAPI_E_NOT_FOUNDプロパティ値に配置します。</span><span class="sxs-lookup"><span data-stu-id="7dd19-158">When this occurs, place PT_ERROR in the property type portion of the property tag and MAPI_E_NOT_FOUND in the property value for the unsupported column.</span></span> 
  
<span data-ttu-id="7dd19-159">行数は、要件ではなく要求として扱います。</span><span class="sxs-lookup"><span data-stu-id="7dd19-159">Treat the row count as a request rather than a requirement.</span></span> <span data-ttu-id="7dd19-160">クエリの方向に行がない場合は、ゼロ行から要求された数まで任意の場所を返します。</span><span class="sxs-lookup"><span data-stu-id="7dd19-160">You can return anywhere from zero rows, if there are no rows in the direction of the query, to the number requested.</span></span> 
  
<span data-ttu-id="7dd19-161">分類されたテーブル ビューから行が要求された場合に表示される行のみを返し、呼び出し元はデータの範囲に関する有効な仮定を行い、余分な作業を回避できます。</span><span class="sxs-lookup"><span data-stu-id="7dd19-161">Return only the rows that the user will see when rows are requested from a categorized table view, allowing the caller to make valid assumptions about the scope of the data and avoid extra work.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7dd19-162">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="7dd19-162">Notes to callers</span></span>

<span data-ttu-id="7dd19-163">通常  _、lRowCount_ パラメーターで指定した数の行が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7dd19-163">Usually you will end up with as many rows as you have specified in the  _lRowCount_ parameter.</span></span> <span data-ttu-id="7dd19-164">ただし、メモリまたは実装の制限が問題である場合、または操作がテーブルの開始または終了に途中で達すると **、QueryRows** は要求された行よりも少ない行を返します。</span><span class="sxs-lookup"><span data-stu-id="7dd19-164">However, when memory or implementation limits are an issue or when the operation reaches the beginning or end of the table prematurely, **QueryRows** will return less rows than requested.</span></span> 
  
<span data-ttu-id="7dd19-165">**QueryRows が** MAPI_E_BUSYを返す場合は [、IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md)メソッドを呼び出し、非同期操作が完了したら **QueryRows** への呼び出しを再試行します。</span><span class="sxs-lookup"><span data-stu-id="7dd19-165">If **QueryRows** returns MAPI_E_BUSY, call the [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) method and retry the call to **QueryRows** when the asynchronous operation is complete.</span></span> 
  
<span data-ttu-id="7dd19-166">**QueryRows** を呼び出す場合、非同期通知のタイミングによって **、QueryRows** から取得した行セットが基になるデータを正確に表していない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7dd19-166">When calling **QueryRows**, be aware that the timing of asynchronous notifications can potentially cause the row set that you get back from **QueryRows** not to accurately represent the underlying data.</span></span> <span data-ttu-id="7dd19-167">たとえば、メッセージを削除した後で、対応する通知を受信する前にフォルダーのコンテンツ テーブルに **QueryRows** を呼び出した場合、削除された行が行セットで返されます。</span><span class="sxs-lookup"><span data-stu-id="7dd19-167">For example, a call to **QueryRows** to a folder's contents table following the deletion of a message but prior to the receipt of the corresponding notification will cause the deleted row to be returned in the row set.</span></span> <span data-ttu-id="7dd19-168">ユーザーのデータビューを更新する前に、通知が届くのを常に待ちます。</span><span class="sxs-lookup"><span data-stu-id="7dd19-168">Always wait for a notification to arrive before updating the user's view of the data.</span></span> 
  
<span data-ttu-id="7dd19-169">テーブルから行を取得する方法の詳細については、「 [テーブルの行からデータを取得する」を参照してください](retrieving-data-from-table-rows.md)。</span><span class="sxs-lookup"><span data-stu-id="7dd19-169">For more information about retrieving rows from tables, see [Retrieving Data from Table Rows](retrieving-data-from-table-rows.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7dd19-170">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="7dd19-170">MFCMAPI reference</span></span>

<span data-ttu-id="7dd19-171">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7dd19-171">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7dd19-172">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="7dd19-172">**File**</span></span>|<span data-ttu-id="7dd19-173">**関数**</span><span class="sxs-lookup"><span data-stu-id="7dd19-173">**Function**</span></span>|<span data-ttu-id="7dd19-174">**コメント**</span><span class="sxs-lookup"><span data-stu-id="7dd19-174">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7dd19-175">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="7dd19-175">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="7dd19-176">DwThreadFuncLoadTable</span><span class="sxs-lookup"><span data-stu-id="7dd19-176">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="7dd19-177">MFCMAPI は **IMAPITable::QueryRows** メソッドを使用して、ビューに読み込むテーブル内の行を取得します。</span><span class="sxs-lookup"><span data-stu-id="7dd19-177">MFCMAPI uses the **IMAPITable::QueryRows** method to retrieve rows in the table to load into the view.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7dd19-178">関連項目</span><span class="sxs-lookup"><span data-stu-id="7dd19-178">See also</span></span>



[<span data-ttu-id="7dd19-179">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="7dd19-179">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="7dd19-180">FreeProws</span><span class="sxs-lookup"><span data-stu-id="7dd19-180">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="7dd19-181">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="7dd19-181">HrQueryAllRows</span></span>](hrqueryallrows.md)
  
[<span data-ttu-id="7dd19-182">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="7dd19-182">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="7dd19-183">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="7dd19-183">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="7dd19-184">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="7dd19-184">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md)
  
[<span data-ttu-id="7dd19-185">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="7dd19-185">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="7dd19-186">SRow</span><span class="sxs-lookup"><span data-stu-id="7dd19-186">SRow</span></span>](srow.md)
  
[<span data-ttu-id="7dd19-187">SRowSet</span><span class="sxs-lookup"><span data-stu-id="7dd19-187">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="7dd19-188">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7dd19-188">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


<span data-ttu-id="7dd19-189">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="7dd19-189">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

