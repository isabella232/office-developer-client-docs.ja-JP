---
title: IMAPITableSortTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SortTable
api_type:
- COM
ms.assetid: ff5f78ac-06cf-46fb-93da-5f4a3a5d1b22
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 46a87a6eb5c80244c04ae6257cd4441b8797ba36
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800857"
---
# <a name="imapitablesorttable"></a><span data-ttu-id="c7a38-103">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="c7a38-103">IMAPITable::SortTable</span></span>

<span data-ttu-id="c7a38-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c7a38-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c7a38-105">**IMAPITable::SortTable**メソッドは、条件の並べ替えによって、テーブルの行を指示します。</span><span class="sxs-lookup"><span data-stu-id="c7a38-105">The **IMAPITable::SortTable** method orders the rows of the table, depending on sort criteria.</span></span> 
  
```cpp
HRESULT SortTable(
LPSSortOrderSet lpSortCriteria,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="c7a38-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="c7a38-106">Parameters</span></span>

<span data-ttu-id="c7a38-107">_lpSortCriteria_</span><span class="sxs-lookup"><span data-stu-id="c7a38-107">_lpSortCriteria_</span></span>
  
> <span data-ttu-id="c7a38-108">[in]適用する並べ替え条件を含む[SSortOrderSet](ssortorderset.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c7a38-108">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure that contains the sort criteria to apply.</span></span> <span data-ttu-id="c7a38-109">0 の列を含む**SSortOrderSet**構造体を渡すと、特定の順序でソートするテーブルがないことを示します。</span><span class="sxs-lookup"><span data-stu-id="c7a38-109">Passing an **SSortOrderSet** structure that contains zero columns indicates that the table does not have to be sorted in any particular order.</span></span> 
    
<span data-ttu-id="c7a38-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c7a38-110">_ulFlags_</span></span>
  
> <span data-ttu-id="c7a38-111">[in]**IMAPITable::SortTable**操作のタイミングを制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="c7a38-111">[in] Bitmask of flags that controls the timing of the **IMAPITable::SortTable** operation.</span></span> <span data-ttu-id="c7a38-112">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="c7a38-112">The following flags can be set:</span></span> 
    
<span data-ttu-id="c7a38-113">TBL_ASYNC</span><span class="sxs-lookup"><span data-stu-id="c7a38-113">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="c7a38-114">操作を非同期に開始し、操作が完了する前に返します。</span><span class="sxs-lookup"><span data-stu-id="c7a38-114">Starts the operation asynchronously and returns before the operation is complete.</span></span>
    
<span data-ttu-id="c7a38-115">TBL_BATCH</span><span class="sxs-lookup"><span data-stu-id="c7a38-115">TBL_BATCH</span></span> 
  
> <span data-ttu-id="c7a38-116">テーブル内のデータが必要になるまでは、並べ替えの完了を延期します。</span><span class="sxs-lookup"><span data-stu-id="c7a38-116">Defers the completion of the sort until the data in the table is required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c7a38-117">�߂�l</span><span class="sxs-lookup"><span data-stu-id="c7a38-117">Return value</span></span>

<span data-ttu-id="c7a38-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="c7a38-118">S_OK</span></span> 
  
> <span data-ttu-id="c7a38-119">並べ替え操作が正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="c7a38-119">The sort operation was successful.</span></span>
    
<span data-ttu-id="c7a38-120">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="c7a38-120">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="c7a38-121">別の操作は、並べ替え操作の開始を防止する処理中です。</span><span class="sxs-lookup"><span data-stu-id="c7a38-121">Another operation is in progress that prevents the sort operation from starting.</span></span> <span data-ttu-id="c7a38-122">実行中の操作を完了できるか、それを停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c7a38-122">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="c7a38-123">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="c7a38-123">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="c7a38-124">テーブルは、要求の並べ替えの種類をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="c7a38-124">The table does not support the type of sorting requested.</span></span>
    
<span data-ttu-id="c7a38-125">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="c7a38-125">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="c7a38-126">テーブルは、 _lpSortCriteria_パラメーターで指定された特定の並べ替え条件が複雑すぎるために、操作を実行できません。</span><span class="sxs-lookup"><span data-stu-id="c7a38-126">The table cannot perform the operation because the particular sort criteria pointed to by the  _lpSortCriteria_ parameter is too complex.</span></span> <span data-ttu-id="c7a38-127">**SortTable**は、次の条件下で、MAPI_E_TOO_COMPLEX を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="c7a38-127">**SortTable** can return MAPI_E_TOO_COMPLEX under the following conditions.</span></span> 
    
   - <span data-ttu-id="c7a38-128">並べ替え操作がプロパティの列の要求された実装を並べ替えることはできません。</span><span class="sxs-lookup"><span data-stu-id="c7a38-128">A sort operation is requested for a property column that the implementation cannot sort.</span></span>
    
   - <span data-ttu-id="c7a38-129">実装は、 **ulOrder**の**SSortOrderSet**構造体のメンバーに要求された並べ替え順序をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="c7a38-129">The implementation does not support the sort order requested in the **ulOrder** member of the **SSortOrderSet** structure.</span></span> 
    
   - <span data-ttu-id="c7a38-130">、ソートする列の数は**SSortOrderSet**で**cSorts**のメンバーで指定された、実装が処理できるよりも大きい。</span><span class="sxs-lookup"><span data-stu-id="c7a38-130">The number of columns to be sorted, as specified in the **cSorts** member in **SSortOrderSet**, is larger than the implementation can handle.</span></span>
    
   - <span data-ttu-id="c7a38-131">**SSortOrderSet**、利用可能なまたはアクティブなセットに含まれていないプロパティに基づく内のプロパティ タグで示されるように、並べ替え操作が要求され、実装が利用可能なセットではなくプロパティの並べ替えをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="c7a38-131">A sort operation is requested, as indicated by a property tag in **SSortOrderSet**, based on a property that is not in the available or active set and the implementation does not support sorting on properties not in the available set.</span></span>
    
   - <span data-ttu-id="c7a38-132">1 つのプロパティが複数回指定されて、並べ替え順のセットで、同じプロパティ タグの複数のインスタンスによって示されると、実装は、このような並べ替え操作を実行できません。</span><span class="sxs-lookup"><span data-stu-id="c7a38-132">One property is specified multiple times in a sort order set, as indicated by multiple instances of the same property tag, and the implementation cannot perform such a sort operation.</span></span>
    
   - <span data-ttu-id="c7a38-133">MVI_FLAG を使用して複数値を持つプロパティの列に基づいて並べ替え操作が要求され、実装は、複数値を持つプロパティの並べ替えをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="c7a38-133">A sort operation based on multivalued property columns is requested using MVI_FLAG and the implementation does not support sorting on multivalued properties.</span></span> 
    
   - <span data-ttu-id="c7a38-134">**SSortOrderSet**でのプロパティのプロパティ タグは、プロパティまたは実装でサポートされていない型を指定します。</span><span class="sxs-lookup"><span data-stu-id="c7a38-134">A property tag for a property in **SSortOrderSet** specifies a property or type that the implementation does not support.</span></span> 
    
   - <span data-ttu-id="c7a38-135">以外の**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) は前方からのテーブルを処理する 1 つの並べ替え操作は、このような並べ替えをサポートしている添付ファイル テーブルに対してのみ指定されます。</span><span class="sxs-lookup"><span data-stu-id="c7a38-135">A sort operation other than one that proceeds through the table from the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property forward is specified only for an attachment table that supports this type of sorting.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c7a38-136">備考</span><span class="sxs-lookup"><span data-stu-id="c7a38-136">Remarks</span></span>

<span data-ttu-id="c7a38-137">**IMAPITable::SortTable**メソッドでは、表形式ビューで行を順序付けします。</span><span class="sxs-lookup"><span data-stu-id="c7a38-137">The **IMAPITable::SortTable** method orders the rows in a table view.</span></span> <span data-ttu-id="c7a38-138">いくつかのテーブルでは、標準と分類の両方のさまざまな並べ替えのキー列の並べ替えをサポートするが、他のテーブルは多くのサポートに制限します。</span><span class="sxs-lookup"><span data-stu-id="c7a38-138">Whereas some tables support both standard and categorized sorting on various sort key columns, other tables are more limited in their support.</span></span> <span data-ttu-id="c7a38-139">通常、アドレス帳プロバイダーはテーブルの並べ替えをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="c7a38-139">Address book providers ordinarily do not support table sorting.</span></span> <span data-ttu-id="c7a38-140">メッセージ ストア プロバイダーは、通常、(テーブル制限なし) の完全テーブルが並べ替えられたときに発生する、フォルダーの並べ替え順序を維持する並べ替えをサポートします。</span><span class="sxs-lookup"><span data-stu-id="c7a38-140">Message store providers usually support sorting to the extent that they keep the sort order of folders that results when a full table (a table without restrictions) is sorted.</span></span> 
  
<span data-ttu-id="c7a38-141">いくつかのテーブルでは、任意のテーブル列で実行する並べ替えを許可します。</span><span class="sxs-lookup"><span data-stu-id="c7a38-141">Some tables allow sorting to be done on any table column.</span></span> <span data-ttu-id="c7a38-142">他のテーブルの操作を行います。テーブル ビューに含まれていない列は、 **SortTable**の呼び出しによって影響を受けません。</span><span class="sxs-lookup"><span data-stu-id="c7a38-142">Other tables do not; columns not included in the table view are unaffected by a **SortTable** call.</span></span> <span data-ttu-id="c7a38-143">いくつかのテーブルは、テーブルの現在の列セットの列にのみ並べ替えキーが作成されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="c7a38-143">Some tables require that sort keys be built only with columns in the table's current column set.</span></span> 
  
<span data-ttu-id="c7a38-144">テーブルでは、並べ替え操作を完了できないことと、MAPI_E_NO_SUPPORT または MAPI_E_TOO_COMPLEX のいずれかを**SortTable**から返すことができます。</span><span class="sxs-lookup"><span data-stu-id="c7a38-144">A table can return either MAPI_E_NO_SUPPORT or MAPI_E_TOO_COMPLEX from **SortTable** when it cannot complete a sort operation.</span></span> <span data-ttu-id="c7a38-145">さらに、ストア プロバイダーは、階層テーブルの指定した並べ替え順を優先するとは限りません。</span><span class="sxs-lookup"><span data-stu-id="c7a38-145">Moreover, store providers are not guaranteed to honor the sort order set specified for hierarchy tables.</span></span> 
  
<span data-ttu-id="c7a38-146">_LpSortCriteria_パラメーターで指定された[SSortOrderSet](ssortorderset.md)構造体で 0 個の列がある場合、テーブルは、現在の列のセットを返します。</span><span class="sxs-lookup"><span data-stu-id="c7a38-146">When there are zero columns in the [SSortOrderSet](ssortorderset.md) structure pointed to by the  _lpSortCriteria_ parameter, the table returns the current column set.</span></span> <span data-ttu-id="c7a38-147">現在の並べ替え順序は、テーブルの[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)メソッドを呼び出すことによって取得できます。</span><span class="sxs-lookup"><span data-stu-id="c7a38-147">The current sort order can be retrieved by calling the table's [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
<span data-ttu-id="c7a38-148">テーブルのすべてのブックマークは無効になり、 **SortTable**への呼び出しが作成され、テーブルの先頭に、現在のカーソル位置を示す BOOKMARK_CURRENT のブックマークを指定するときに削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c7a38-148">All bookmarks for a table are invalidated and should be deleted when a call to **SortTable** is made, and the BOOKMARK_CURRENT bookmark that indicates the current cursor position, should be set to the beginning of the table.</span></span> 
  
<span data-ttu-id="c7a38-149">MVI_FLAG フラグが設定されていない複数値を持つプロパティを含む列を並べ替える場合、列の値は、完全に順序付けられた組として扱われます。</span><span class="sxs-lookup"><span data-stu-id="c7a38-149">If you are sorting on a column that contains a multivalued property without the MVI_FLAG flag set, the column's values are treated as a completely ordered tuple.</span></span> <span data-ttu-id="c7a38-150">2 つの複数値を持つ列の比較では、列の要素には、最初の非等値の列の関係を報告を比較し、比較対象の列には、同じ順序で同じ値が含まれている場合にのみ、等しいかどうかを返します。</span><span class="sxs-lookup"><span data-stu-id="c7a38-150">A comparison of two multivalued columns compares the column elements in order, reporting the relation of the columns at the first inequality, and returns equality only if the columns being compared contain the same values in the same order.</span></span> <span data-ttu-id="c7a38-151">もう一方よりも少ない値を 1 つの列には、報告された関係が他の値に null 値の</span><span class="sxs-lookup"><span data-stu-id="c7a38-151">If one column has fewer values than the other, the reported relation is that of a null value to the other value.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="c7a38-152">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="c7a38-152">Notes to callers</span></span>

<span data-ttu-id="c7a38-153">フラグのいずれかを設定しない限り、 **SortTable**は同期的に動作します。</span><span class="sxs-lookup"><span data-stu-id="c7a38-153">**SortTable** operates synchronously unless you set one of the flags.</span></span> <span data-ttu-id="c7a38-154">**SortTable**に TBL_BATCH フラグを設定すると、データを要求する場合を除き、並べ替え操作を延期します。</span><span class="sxs-lookup"><span data-stu-id="c7a38-154">If you set the TBL_BATCH flag, **SortTable** postpones the sort operation unless you request the data.</span></span> <span data-ttu-id="c7a38-155">TBL_ASYNC フラグが設定されている場合**SortTable**は、非同期的に、操作を完了する前に返す可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c7a38-155">If the TBL_ASYNC flag is set, **SortTable** operates asynchronously, potentially returning before the completion of the operation.</span></span> 
  
<span data-ttu-id="c7a38-156">並べ替えをすぐに行う必要がある場合は、進行中の非同期操作を停止するのには[IMAPITable::Abort](imapitable-abort.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c7a38-156">Call the [IMAPITable::Abort](imapitable-abort.md) method to stop an asynchronous operation in progress if your sort must be done immediately.</span></span> <span data-ttu-id="c7a38-157">**SortTable**は、テーブルの 1 つまたは複数の非同期操作が実行されているために続行できません、MAPI_E_BUSY が返されます。</span><span class="sxs-lookup"><span data-stu-id="c7a38-157">If **SortTable** cannot continue because one or more asynchronous operations on the table are in progress, it returns MAPI_E_BUSY.</span></span> 
  
<span data-ttu-id="c7a38-158">最適なパフォーマンスを得るには、テーブルの列のセットをカスタマイズする**SetColumns**と並べ替えを実行するのには**SortTable**を呼び出す前に、テーブル内の行の数を制限するため**だけに制限する**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c7a38-158">For best performance, call **SetColumns** to customize the table's column set and **Restrict** to limit the number of rows in the table before you call **SortTable** to perform the sort.</span></span> 
  
<span data-ttu-id="c7a38-159">**SortTable**が失敗したときに、問題が発生する前に有効であった並べ替え順序は、有効です。</span><span class="sxs-lookup"><span data-stu-id="c7a38-159">Whenever **SortTable** fails, the sort order that was in effect before the failure is still in effect.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c7a38-160">関連項目</span><span class="sxs-lookup"><span data-stu-id="c7a38-160">See also</span></span>

- [<span data-ttu-id="c7a38-161">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="c7a38-161">IMAPITable::Abort</span></span>](imapitable-abort.md)
- [<span data-ttu-id="c7a38-162">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="c7a38-162">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
- [<span data-ttu-id="c7a38-163">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="c7a38-163">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
- [<span data-ttu-id="c7a38-164">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="c7a38-164">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
- [<span data-ttu-id="c7a38-165">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="c7a38-165">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
- [<span data-ttu-id="c7a38-166">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="c7a38-166">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="c7a38-167">IMAPITable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="c7a38-167">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

