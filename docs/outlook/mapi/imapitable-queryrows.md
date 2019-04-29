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
# <a name="imapitablequeryrows"></a><span data-ttu-id="483c3-103">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="483c3-103">IMAPITable::QueryRows</span></span>

  
  
<span data-ttu-id="483c3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="483c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="483c3-105">現在のカーソル位置から、1つまたは複数の行をテーブルから返します。</span><span class="sxs-lookup"><span data-stu-id="483c3-105">Returns one or more rows from a table, beginning at the current cursor position.</span></span>
  
```cpp
HRESULT QueryRows(
LONG lRowCount,
ULONG ulFlags,
LPSRowSet FAR * lppRows
);
```

## <a name="parameters"></a><span data-ttu-id="483c3-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="483c3-106">Parameters</span></span>

 <span data-ttu-id="483c3-107">_lrowcount_</span><span class="sxs-lookup"><span data-stu-id="483c3-107">_lRowCount_</span></span>
  
> <span data-ttu-id="483c3-108">順番返される行の最大数。</span><span class="sxs-lookup"><span data-stu-id="483c3-108">[in] Maximum number of rows to be returned.</span></span>
    
 <span data-ttu-id="483c3-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="483c3-109">_ulFlags_</span></span>
  
> <span data-ttu-id="483c3-110">順番行が返される方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="483c3-110">[in] Bitmask of flags that control how rows are returned.</span></span> <span data-ttu-id="483c3-111">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="483c3-111">The following flag can be set:</span></span>
    
<span data-ttu-id="483c3-112">TBL_NOADVANCE</span><span class="sxs-lookup"><span data-stu-id="483c3-112">TBL_NOADVANCE</span></span> 
  
> <span data-ttu-id="483c3-113">行の取得の結果として、カーソルが昇格しないようにします。</span><span class="sxs-lookup"><span data-stu-id="483c3-113">Prevents the cursor from advancing as a result of the row retrieval.</span></span> <span data-ttu-id="483c3-114">TBL_NOADVANCE フラグが設定されている場合、カーソルは返される最初の行を指します。</span><span class="sxs-lookup"><span data-stu-id="483c3-114">If the TBL_NOADVANCE flag is set, the cursor points to the first row returned.</span></span> <span data-ttu-id="483c3-115">TBL_NOADVANCE フラグが設定されていない場合、カーソルは、返される最後の行の次の行を指します。</span><span class="sxs-lookup"><span data-stu-id="483c3-115">If the TBL_NOADVANCE flag is not set, the cursor points to the row following the last row returned.</span></span>
    
 <span data-ttu-id="483c3-116">_lpprows_</span><span class="sxs-lookup"><span data-stu-id="483c3-116">_lppRows_</span></span>
  
> <span data-ttu-id="483c3-117">読み上げテーブルの行を保持する[srowset](srowset.md)構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="483c3-117">[out] Pointer to a pointer to an [SRowSet](srowset.md) structure holding the table rows.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="483c3-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="483c3-118">Return value</span></span>

<span data-ttu-id="483c3-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="483c3-119">S_OK</span></span> 
  
> <span data-ttu-id="483c3-120">行が正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="483c3-120">The rows were successfully returned.</span></span>
    
<span data-ttu-id="483c3-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="483c3-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="483c3-122">別の操作が進行中なので、行取得操作を開始できません。</span><span class="sxs-lookup"><span data-stu-id="483c3-122">Another operation is in progress that prevents the row retrieval operation from starting.</span></span> <span data-ttu-id="483c3-123">進行中の操作が完了することを許可するか、停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="483c3-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="483c3-124">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="483c3-124">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="483c3-125">_irowcount_パラメーターは0に設定されています。</span><span class="sxs-lookup"><span data-stu-id="483c3-125">The  _IRowCount_ parameter is set to zero.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="483c3-126">注釈</span><span class="sxs-lookup"><span data-stu-id="483c3-126">Remarks</span></span>

<span data-ttu-id="483c3-127">**IMAPITable:: QueryRows**メソッドは、テーブルから1つまたは複数のデータ行を取得します。</span><span class="sxs-lookup"><span data-stu-id="483c3-127">The **IMAPITable::QueryRows** method gets one or more rows of data from a table.</span></span> <span data-ttu-id="483c3-128">_irowcount_パラメーターの値は、取得の開始点に影響します。</span><span class="sxs-lookup"><span data-stu-id="483c3-128">The value of the  _IRowCount_ parameter affects the starting point for the retrieval.</span></span> <span data-ttu-id="483c3-129">_irowcount_が正の場合は、現在の位置から順に行が読み取られます。</span><span class="sxs-lookup"><span data-stu-id="483c3-129">If  _IRowCount_ is positive, rows are read in a forward direction, starting at the current position.</span></span> <span data-ttu-id="483c3-130">_irowcount_が負の場合、 **QueryRows**は指定された行数だけ後方に移動して開始点をリセットします。</span><span class="sxs-lookup"><span data-stu-id="483c3-130">If  _IRowCount_ is negative, **QueryRows** resets the starting point by moving backward the indicated number of rows.</span></span> <span data-ttu-id="483c3-131">カーソルがリセットされると、行は前方に読み上げられます。</span><span class="sxs-lookup"><span data-stu-id="483c3-131">After the cursor is reset, rows are read in forward order.</span></span> 
  
<span data-ttu-id="483c3-132">_lpprows_パラメーターが指す[srowset](srowset.md)構造の**cRows**メンバは、返される行数を示しています。</span><span class="sxs-lookup"><span data-stu-id="483c3-132">The **cRows** member in the [SRowSet](srowset.md) structure pointed to by the  _lppRows_ parameter indicates the number of rows returned.</span></span> <span data-ttu-id="483c3-133">0行が返される場合:</span><span class="sxs-lookup"><span data-stu-id="483c3-133">If zero rows are returned:</span></span> 
  
- <span data-ttu-id="483c3-134">カーソルは既にテーブルの先頭に配置されており、 _irowcount_の値が負になります。</span><span class="sxs-lookup"><span data-stu-id="483c3-134">The cursor was already positioned at the beginning of the table and the value of  _IRowCount_ is negative.</span></span> <span data-ttu-id="483c3-135">や</span><span class="sxs-lookup"><span data-stu-id="483c3-135">-Or-</span></span> 
    
- <span data-ttu-id="483c3-136">カーソルは既にテーブルの最後に配置されており、 _irowcount_の値は正です。</span><span class="sxs-lookup"><span data-stu-id="483c3-136">The cursor was already positioned at the end of the table and the value of  _IRowCount_ is positive.</span></span> 
    
<span data-ttu-id="483c3-137">列の数とその順序は、各行で同じです。</span><span class="sxs-lookup"><span data-stu-id="483c3-137">The number of columns and their ordering is the same for each row.</span></span> <span data-ttu-id="483c3-138">行のプロパティが存在しない場合、またはプロパティの読み取りエラーが発生した場合、行内のプロパティの**spropvalue**構造体には次の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="483c3-138">If a property does not exist for a row or there is an error reading a property, the **SPropValue** structure for the property in the row contains the following values:</span></span> 
  
- <span data-ttu-id="483c3-139">**ulPropTag**メンバーのプロパティの種類の PT_ERROR。</span><span class="sxs-lookup"><span data-stu-id="483c3-139">PT_ERROR for the property type in the **ulPropTag** member.</span></span> 
    
- <span data-ttu-id="483c3-140">**Value**メンバーの MAPI_E_NOT_FOUND。</span><span class="sxs-lookup"><span data-stu-id="483c3-140">MAPI_E_NOT_FOUND for the **Value** member.</span></span> 
    
<span data-ttu-id="483c3-141">_lpprows_パラメーターによって指定された行セットの[spropvalue](spropvalue.md)構造体に使用されるメモリは、各行に対して個別に割り当てて解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="483c3-141">Memory used for the [SPropValue](spropvalue.md) structures in the row set pointed to by the  _lppRows_ parameter must be separately allocated and freed for each row.</span></span> <span data-ttu-id="483c3-142">[MAPIFreeBuffer](mapifreebuffer.md)を使用して、プロパティの値構造を解放し、行セットを解放します。</span><span class="sxs-lookup"><span data-stu-id="483c3-142">Use [MAPIFreeBuffer](mapifreebuffer.md) to free the property value structures and to free the row set.</span></span> <span data-ttu-id="483c3-143">**QueryRows**の呼び出しによって0が返されますが、テーブルの先頭または末尾を示している場合は、 **srowset**構造自体のみを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="483c3-143">When a call to **QueryRows** returns zero, however, indicating the beginning or end of the table, only the **SRowSet** structure itself needs to be freed.</span></span> <span data-ttu-id="483c3-144">**srowset**構造のメモリを割り当てて解放する方法の詳細については、「 [adrlist および srowset 構造体のメモリの管理](managing-memory-for-adrlist-and-srowset-structures.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="483c3-144">For more information about how to allocate and free memory in an **SRowSet** structure, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
<span data-ttu-id="483c3-145">返される行と、返される順序は、 [IMAPITable:: Restrict](imapitable-restrict.md)と[imapitable:: sorttable](imapitable-sorttable.md)に成功したかどうかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="483c3-145">The rows that are returned and the order in which they are returned depend on whether or not successful calls have been made to [IMAPITable::Restrict](imapitable-restrict.md) and [IMAPITable::SortTable](imapitable-sorttable.md).</span></span> <span data-ttu-id="483c3-146">ビューからフィルター行を**制限**します。これにより、 **QueryRows**は、制限で指定された条件に一致する行のみを返します。</span><span class="sxs-lookup"><span data-stu-id="483c3-146">**Restrict** filters rows from the view, causing **QueryRows** to return only the rows that match the criteria specified in the restriction.</span></span> <span data-ttu-id="483c3-147">**sorttable**は、標準または分類された並べ替え順序を確立し、 **QueryRows**によって返される一連の行に影響します。</span><span class="sxs-lookup"><span data-stu-id="483c3-147">**SortTable** establishes a standard or categorized sort order, affecting the sequence of rows returned by **QueryRows**.</span></span> <span data-ttu-id="483c3-148">返される行は、 [ssortorderset](ssortorderset.md)構造で指定された順序で**sorttable**に渡されます。</span><span class="sxs-lookup"><span data-stu-id="483c3-148">The returned rows are in the order specified in the [SSortOrderSet](ssortorderset.md) structure passed to **SortTable**.</span></span>
  
<span data-ttu-id="483c3-149">各行に返される列と返される順序は、 [IMAPITable:: SetColumns](imapitable-setcolumns.md)に正常に呼び出しが行われたかどうかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="483c3-149">The columns returned for each row and the order in which they are returned depend on whether or not a successful call has been made to [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span> <span data-ttu-id="483c3-150">**SetColumns**は列セットを確立し、テーブルの列に含めるプロパティと、それらを含める順序を指定します。</span><span class="sxs-lookup"><span data-stu-id="483c3-150">**SetColumns** establishes a column set, specifying the properties to be included in columns in the table and the order in which they should be included.</span></span> <span data-ttu-id="483c3-151">**SetColumns**呼び出しが行われている場合、各行の特定の列とそれらの列の順序は、呼び出しで指定された列セットと一致します。</span><span class="sxs-lookup"><span data-stu-id="483c3-151">If a **SetColumns** call has been made, the particular columns in each row and the order of those columns match the column set specified in the call.</span></span> <span data-ttu-id="483c3-152">**SetColumns**呼び出しが行われていない場合、テーブルは既定の列セットを返します。</span><span class="sxs-lookup"><span data-stu-id="483c3-152">If no **SetColumns** call has been made, the table returns its default column set.</span></span> 
  
<span data-ttu-id="483c3-153">これらの呼び出しが行われていない場合、 **QueryRows**はテーブル内のすべての行を返します。</span><span class="sxs-lookup"><span data-stu-id="483c3-153">If none of these calls has been made, **QueryRows** returns all of the rows in the table.</span></span> <span data-ttu-id="483c3-154">各行には、既定の順序で設定された既定の列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="483c3-154">Each row contains the default column set in default order.</span></span> 
  
<span data-ttu-id="483c3-155">[IMAPITable:: SetColumns](imapitable-setcolumns.md)の呼び出しで設定された列セットが PR_NULL に設定されている場合、 _lpprows_で返される行セット内の[spropvalue](spropvalue.md)配列には空のスロットが含まれます。</span><span class="sxs-lookup"><span data-stu-id="483c3-155">When the column set established in a call to [IMAPITable::SetColumns](imapitable-setcolumns.md) includes columns set to PR_NULL, the [SPropValue](spropvalue.md) array within the row set returned in  _lppRows_ will contain empty slots.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="483c3-156">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="483c3-156">Notes to implementers</span></span>

<span data-ttu-id="483c3-157">発信者は、サポートされていない列を列セットに含めることを要求できます。</span><span class="sxs-lookup"><span data-stu-id="483c3-157">You can allow a caller to request an unsupported column to be included in the column set.</span></span> <span data-ttu-id="483c3-158">この場合、PT_ERROR をプロパティタグのプロパティの種類部分に配置し、サポートされていない列のプロパティ値に MAPI_E_NOT_FOUND を設定します。</span><span class="sxs-lookup"><span data-stu-id="483c3-158">When this occurs, place PT_ERROR in the property type portion of the property tag and MAPI_E_NOT_FOUND in the property value for the unsupported column.</span></span> 
  
<span data-ttu-id="483c3-159">行カウントは、要件ではなく要求として処理します。</span><span class="sxs-lookup"><span data-stu-id="483c3-159">Treat the row count as a request rather than a requirement.</span></span> <span data-ttu-id="483c3-160">クエリの方向に行がない場合は、要求された数になるまで、0行から任意の値を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="483c3-160">You can return anywhere from zero rows, if there are no rows in the direction of the query, to the number requested.</span></span> 
  
<span data-ttu-id="483c3-161">カテゴリ別のテーブルビューから行が要求されたときにユーザーに表示される行のみを返します。これにより、呼び出し元は、データの範囲に関する有効な前提条件を作成し、余分な作業を避けることができます。</span><span class="sxs-lookup"><span data-stu-id="483c3-161">Return only the rows that the user will see when rows are requested from a categorized table view, allowing the caller to make valid assumptions about the scope of the data and avoid extra work.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="483c3-162">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="483c3-162">Notes to callers</span></span>

<span data-ttu-id="483c3-163">通常は、 _lrowcount_パラメーターで指定した行数だけ行が入力されます。</span><span class="sxs-lookup"><span data-stu-id="483c3-163">Usually you will end up with as many rows as you have specified in the  _lRowCount_ parameter.</span></span> <span data-ttu-id="483c3-164">ただし、メモリまたは実装の制限が問題になる場合や、処理がテーブルの先頭または末尾に達した後に発生した場合、 **QueryRows**は要求されたよりも少ない行数を返します。</span><span class="sxs-lookup"><span data-stu-id="483c3-164">However, when memory or implementation limits are an issue or when the operation reaches the beginning or end of the table prematurely, **QueryRows** will return less rows than requested.</span></span> 
  
<span data-ttu-id="483c3-165">**QueryRows**が MAPI_E_BUSY を返す場合は、 [IMAPITable:: waitforcompletion](imapitable-waitforcompletion.md)メソッドを呼び出して、非同期操作が完了したときに**QueryRows**の呼び出しを再試行します。</span><span class="sxs-lookup"><span data-stu-id="483c3-165">If **QueryRows** returns MAPI_E_BUSY, call the [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) method and retry the call to **QueryRows** when the asynchronous operation is complete.</span></span> 
  
<span data-ttu-id="483c3-166">**QueryRows**を呼び出すときは、非同期通知のタイミングが原因で、 **QueryRows**から返される行セットが、基になるデータを正確に表示しない可能性があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="483c3-166">When calling **QueryRows**, be aware that the timing of asynchronous notifications can potentially cause the row set that you get back from **QueryRows** not to accurately represent the underlying data.</span></span> <span data-ttu-id="483c3-167">たとえば、メッセージを削除した後、それに対応する通知を受信する前に、フォルダーの contents テーブルに**QueryRows**を呼び出すと、削除された行が行セットに返されることになります。</span><span class="sxs-lookup"><span data-stu-id="483c3-167">For example, a call to **QueryRows** to a folder's contents table following the deletion of a message but prior to the receipt of the corresponding notification will cause the deleted row to be returned in the row set.</span></span> <span data-ttu-id="483c3-168">ユーザーのデータの表示を更新する前に通知が到着するのを常に待機します。</span><span class="sxs-lookup"><span data-stu-id="483c3-168">Always wait for a notification to arrive before updating the user's view of the data.</span></span> 
  
<span data-ttu-id="483c3-169">テーブルから行を取得する方法の詳細については、「[テーブルの行からデータを取得](retrieving-data-from-table-rows.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="483c3-169">For more information about retrieving rows from tables, see [Retrieving Data from Table Rows](retrieving-data-from-table-rows.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="483c3-170">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="483c3-170">MFCMAPI reference</span></span>

<span data-ttu-id="483c3-171">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="483c3-171">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="483c3-172">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="483c3-172">**File**</span></span>|<span data-ttu-id="483c3-173">**関数**</span><span class="sxs-lookup"><span data-stu-id="483c3-173">**Function**</span></span>|<span data-ttu-id="483c3-174">**コメント**</span><span class="sxs-lookup"><span data-stu-id="483c3-174">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="483c3-175">ContentsTableListCtrl</span><span class="sxs-lookup"><span data-stu-id="483c3-175">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="483c3-176">dwthreadの loadtable</span><span class="sxs-lookup"><span data-stu-id="483c3-176">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="483c3-177">mfcmapi は、 **IMAPITable:: QueryRows**メソッドを使用して、ビューに読み込むテーブル内の行を取得します。</span><span class="sxs-lookup"><span data-stu-id="483c3-177">MFCMAPI uses the **IMAPITable::QueryRows** method to retrieve rows in the table to load into the view.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="483c3-178">関連項目</span><span class="sxs-lookup"><span data-stu-id="483c3-178">See also</span></span>



[<span data-ttu-id="483c3-179">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="483c3-179">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="483c3-180">FreeProws</span><span class="sxs-lookup"><span data-stu-id="483c3-180">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="483c3-181">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="483c3-181">HrQueryAllRows</span></span>](hrqueryallrows.md)
  
[<span data-ttu-id="483c3-182">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="483c3-182">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="483c3-183">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="483c3-183">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="483c3-184">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="483c3-184">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md)
  
[<span data-ttu-id="483c3-185">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="483c3-185">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="483c3-186">SRow</span><span class="sxs-lookup"><span data-stu-id="483c3-186">SRow</span></span>](srow.md)
  
[<span data-ttu-id="483c3-187">SRowSet</span><span class="sxs-lookup"><span data-stu-id="483c3-187">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="483c3-188">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="483c3-188">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


<span data-ttu-id="483c3-189">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="483c3-189">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

