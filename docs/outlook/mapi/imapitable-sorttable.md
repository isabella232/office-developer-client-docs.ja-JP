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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: f16ba9164d55fdb7bd688d4068f99dc4407e5413
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432367"
---
# <a name="imapitablesorttable"></a><span data-ttu-id="a110f-103">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="a110f-103">IMAPITable::SortTable</span></span>

<span data-ttu-id="a110f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a110f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a110f-105">**IMAPITable::SortTable** メソッドは、並べ替え条件に応じて、テーブルの行を順序付けします。</span><span class="sxs-lookup"><span data-stu-id="a110f-105">The **IMAPITable::SortTable** method orders the rows of the table, depending on sort criteria.</span></span> 
  
```cpp
HRESULT SortTable(
LPSSortOrderSet lpSortCriteria,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a110f-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a110f-106">Parameters</span></span>

<span data-ttu-id="a110f-107">_lpSortCriteria_</span><span class="sxs-lookup"><span data-stu-id="a110f-107">_lpSortCriteria_</span></span>
  
> <span data-ttu-id="a110f-108">[in]適用する並べ替え条件を含む [SSortOrderSet](ssortorderset.md) 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a110f-108">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure that contains the sort criteria to apply.</span></span> <span data-ttu-id="a110f-109">0 **列を含む SSortOrderSet** 構造体を渡す場合は、テーブルを特定の順序で並べ替える必要が無い場合を示します。</span><span class="sxs-lookup"><span data-stu-id="a110f-109">Passing an **SSortOrderSet** structure that contains zero columns indicates that the table does not have to be sorted in any particular order.</span></span> 
    
<span data-ttu-id="a110f-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a110f-110">_ulFlags_</span></span>
  
> <span data-ttu-id="a110f-111">[in] **IMAPITable::SortTable** 操作のタイミングを制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="a110f-111">[in] Bitmask of flags that controls the timing of the **IMAPITable::SortTable** operation.</span></span> <span data-ttu-id="a110f-112">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="a110f-112">The following flags can be set:</span></span> 
    
<span data-ttu-id="a110f-113">TBL_ASYNC</span><span class="sxs-lookup"><span data-stu-id="a110f-113">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="a110f-114">操作を非同期的に開始し、操作が完了する前に返します。</span><span class="sxs-lookup"><span data-stu-id="a110f-114">Starts the operation asynchronously and returns before the operation is complete.</span></span>
    
<span data-ttu-id="a110f-115">TBL_BATCH</span><span class="sxs-lookup"><span data-stu-id="a110f-115">TBL_BATCH</span></span> 
  
> <span data-ttu-id="a110f-116">テーブル内のデータが必要になるまで、並べ替えの完了を延期します。</span><span class="sxs-lookup"><span data-stu-id="a110f-116">Defers the completion of the sort until the data in the table is required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a110f-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="a110f-117">Return value</span></span>

<span data-ttu-id="a110f-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="a110f-118">S_OK</span></span> 
  
> <span data-ttu-id="a110f-119">並べ替え操作が成功しました。</span><span class="sxs-lookup"><span data-stu-id="a110f-119">The sort operation was successful.</span></span>
    
<span data-ttu-id="a110f-120">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="a110f-120">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="a110f-121">並べ替え操作の開始を妨げる別の操作が進行中です。</span><span class="sxs-lookup"><span data-stu-id="a110f-121">Another operation is in progress that prevents the sort operation from starting.</span></span> <span data-ttu-id="a110f-122">進行中の操作の完了を許可するか、停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a110f-122">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="a110f-123">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="a110f-123">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="a110f-124">テーブルは、要求された並べ替えの種類をサポートしていない。</span><span class="sxs-lookup"><span data-stu-id="a110f-124">The table does not support the type of sorting requested.</span></span>
    
<span data-ttu-id="a110f-125">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="a110f-125">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="a110f-126">_lpSortCriteria_ パラメーターが指す特定の並べ替え条件が複雑すぎるため、テーブルは操作を実行できません。</span><span class="sxs-lookup"><span data-stu-id="a110f-126">The table cannot perform the operation because the particular sort criteria pointed to by the  _lpSortCriteria_ parameter is too complex.</span></span> <span data-ttu-id="a110f-127">**SortTable は** 、次のMAPI_E_TOO_COMPLEXの値を返します。</span><span class="sxs-lookup"><span data-stu-id="a110f-127">**SortTable** can return MAPI_E_TOO_COMPLEX under the following conditions.</span></span> 
    
   - <span data-ttu-id="a110f-128">実装で並べ替えできないプロパティ列の並べ替え操作が要求されます。</span><span class="sxs-lookup"><span data-stu-id="a110f-128">A sort operation is requested for a property column that the implementation cannot sort.</span></span>
    
   - <span data-ttu-id="a110f-129">実装では **、SSortOrderSet** 構造体の **ulOrder** メンバーで要求された並べ替え順序はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="a110f-129">The implementation does not support the sort order requested in the **ulOrder** member of the **SSortOrderSet** structure.</span></span> 
    
   - <span data-ttu-id="a110f-130">**SSortOrderSet** の **cSorts** メンバーで指定されている並べ替える列の数は、実装で処理できる列よりも大きくなります。</span><span class="sxs-lookup"><span data-stu-id="a110f-130">The number of columns to be sorted, as specified in the **cSorts** member in **SSortOrderSet**, is larger than the implementation can handle.</span></span>
    
   - <span data-ttu-id="a110f-131">**SSortOrderSet** のプロパティ タグで示される並べ替え操作は、使用可能なセットまたはアクティブなセットに含けられていないプロパティに基づいて要求され、実装では、使用可能なセット内に存在しないプロパティの並べ替えをサポートしていない。</span><span class="sxs-lookup"><span data-stu-id="a110f-131">A sort operation is requested, as indicated by a property tag in **SSortOrderSet**, based on a property that is not in the available or active set and the implementation does not support sorting on properties not in the available set.</span></span>
    
   - <span data-ttu-id="a110f-132">1 つのプロパティは、同じプロパティ タグの複数のインスタンスで示される並べ替え順序セットで複数回指定され、実装ではこのような並べ替え操作を実行できません。</span><span class="sxs-lookup"><span data-stu-id="a110f-132">One property is specified multiple times in a sort order set, as indicated by multiple instances of the same property tag, and the implementation cannot perform such a sort operation.</span></span>
    
   - <span data-ttu-id="a110f-133">複数値プロパティ列に基づく並べ替え操作は、MVI_FLAG を使用して要求され、実装では複数値プロパティの並べ替えをサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="a110f-133">A sort operation based on multivalued property columns is requested using MVI_FLAG and the implementation does not support sorting on multivalued properties.</span></span> 
    
   - <span data-ttu-id="a110f-134">**SSortOrderSet** のプロパティのプロパティ タグは、実装がサポートしていないプロパティまたは型を指定します。</span><span class="sxs-lookup"><span data-stu-id="a110f-134">A property tag for a property in **SSortOrderSet** specifies a property or type that the implementation does not support.</span></span> 
    
   - <span data-ttu-id="a110f-135">**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) プロパティからテーブルを順方向に移動する並べ替え操作以外の並べ替え操作は、この種類の並べ替えをサポートする添付ファイル テーブルにのみ指定されます。</span><span class="sxs-lookup"><span data-stu-id="a110f-135">A sort operation other than one that proceeds through the table from the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property forward is specified only for an attachment table that supports this type of sorting.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a110f-136">注釈</span><span class="sxs-lookup"><span data-stu-id="a110f-136">Remarks</span></span>

<span data-ttu-id="a110f-137">**IMAPITable::SortTable** メソッドは、テーブル ビュー内の行を並べ替えます。</span><span class="sxs-lookup"><span data-stu-id="a110f-137">The **IMAPITable::SortTable** method orders the rows in a table view.</span></span> <span data-ttu-id="a110f-138">一部のテーブルでは、さまざまな並べ替えキー列での標準並べ替えと分類された並べ替えの両方がサポートされている一方で、他のテーブルではサポートが制限されています。</span><span class="sxs-lookup"><span data-stu-id="a110f-138">Whereas some tables support both standard and categorized sorting on various sort key columns, other tables are more limited in their support.</span></span> <span data-ttu-id="a110f-139">通常、アドレス帳プロバイダーはテーブルの並べ替えをサポートしていない。</span><span class="sxs-lookup"><span data-stu-id="a110f-139">Address book providers ordinarily do not support table sorting.</span></span> <span data-ttu-id="a110f-140">メッセージ ストア プロバイダーは、通常、完全なテーブル (制限のないテーブル) を並べ替えたときに結果のフォルダーの並べ替え順序を維持する範囲で並べ替えをサポートします。</span><span class="sxs-lookup"><span data-stu-id="a110f-140">Message store providers usually support sorting to the extent that they keep the sort order of folders that results when a full table (a table without restrictions) is sorted.</span></span> 
  
<span data-ttu-id="a110f-141">一部のテーブルでは、任意のテーブル列で並べ替えを実行できます。</span><span class="sxs-lookup"><span data-stu-id="a110f-141">Some tables allow sorting to be done on any table column.</span></span> <span data-ttu-id="a110f-142">他のテーブルは使用できません。テーブル ビューに含まれていない列は、SortTable 呼び出し **の影響を受** けません。</span><span class="sxs-lookup"><span data-stu-id="a110f-142">Other tables do not; columns not included in the table view are unaffected by a **SortTable** call.</span></span> <span data-ttu-id="a110f-143">一部のテーブルでは、テーブルの現在の列セット内の列でのみ並べ替えキーを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a110f-143">Some tables require that sort keys be built only with columns in the table's current column set.</span></span> 
  
<span data-ttu-id="a110f-144">並べ替え操作をMAPI_E_NO_SUPPORTできない **MAPI_E_TOO_COMPLEX、SortTable** からテーブルを返す場合があります。</span><span class="sxs-lookup"><span data-stu-id="a110f-144">A table can return either MAPI_E_NO_SUPPORT or MAPI_E_TOO_COMPLEX from **SortTable** when it cannot complete a sort operation.</span></span> <span data-ttu-id="a110f-145">さらに、ストア プロバイダーは、階層テーブルに指定された並べ替え順序セットを尊重する保証はありません。</span><span class="sxs-lookup"><span data-stu-id="a110f-145">Moreover, store providers are not guaranteed to honor the sort order set specified for hierarchy tables.</span></span> 
  
<span data-ttu-id="a110f-146">_lpSortCriteria_ パラメーターが指す [SSortOrderSet](ssortorderset.md)構造体に列が 0 の場合、テーブルは現在の列セットを返します。</span><span class="sxs-lookup"><span data-stu-id="a110f-146">When there are zero columns in the [SSortOrderSet](ssortorderset.md) structure pointed to by the  _lpSortCriteria_ parameter, the table returns the current column set.</span></span> <span data-ttu-id="a110f-147">現在の並べ替え順序は、テーブルの [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) メソッドを呼び出すことによって取得できます。</span><span class="sxs-lookup"><span data-stu-id="a110f-147">The current sort order can be retrieved by calling the table's [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
<span data-ttu-id="a110f-148">テーブルのすべてのブックマークは無効化され **、SortTable** の呼び出しが行われたときに削除され、現在のカーソル位置を示す BOOKMARK_CURRENT ブックマークをテーブルの先頭に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a110f-148">All bookmarks for a table are invalidated and should be deleted when a call to **SortTable** is made, and the BOOKMARK_CURRENT bookmark that indicates the current cursor position, should be set to the beginning of the table.</span></span> 
  
<span data-ttu-id="a110f-149">MVI_FLAG フラグを設定せずに複数値プロパティを含む列で並べ替える場合、列の値は完全に順序付けられた組として扱います。</span><span class="sxs-lookup"><span data-stu-id="a110f-149">If you are sorting on a column that contains a multivalued property without the MVI_FLAG flag set, the column's values are treated as a completely ordered tuple.</span></span> <span data-ttu-id="a110f-150">2 つの複数値列の比較では、列要素を順番に比較し、列の関係を最初の不等式で報告し、比較対象の列に同じ値が同じ順序で含まれている場合にのみ等値を返します。</span><span class="sxs-lookup"><span data-stu-id="a110f-150">A comparison of two multivalued columns compares the column elements in order, reporting the relation of the columns at the first inequality, and returns equality only if the columns being compared contain the same values in the same order.</span></span> <span data-ttu-id="a110f-151">1 つの列の値が他の列よりも少ない場合、報告される関係は、もう一方の値に対する null 値の関係になります。</span><span class="sxs-lookup"><span data-stu-id="a110f-151">If one column has fewer values than the other, the reported relation is that of a null value to the other value.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="a110f-152">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="a110f-152">Notes to callers</span></span>

<span data-ttu-id="a110f-153">フラグのいずれかを設定しない限り **、SortTable** は同期的に動作します。</span><span class="sxs-lookup"><span data-stu-id="a110f-153">**SortTable** operates synchronously unless you set one of the flags.</span></span> <span data-ttu-id="a110f-154">このフラグを設定TBL_BATCH、データを要求しない限り **、SortTable** は並べ替え操作を延期します。</span><span class="sxs-lookup"><span data-stu-id="a110f-154">If you set the TBL_BATCH flag, **SortTable** postpones the sort operation unless you request the data.</span></span> <span data-ttu-id="a110f-155">このフラグTBL_ASYNC設定すると **、SortTable** は非同期的に動作し、操作が完了する前に戻る可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a110f-155">If the TBL_ASYNC flag is set, **SortTable** operates asynchronously, potentially returning before the completion of the operation.</span></span> 
  
<span data-ttu-id="a110f-156">並べ替えを直ちに行う必要がある場合は [、IMAPITable::Abort](imapitable-abort.md) メソッドを呼び出して、進行中の非同期操作を停止します。</span><span class="sxs-lookup"><span data-stu-id="a110f-156">Call the [IMAPITable::Abort](imapitable-abort.md) method to stop an asynchronous operation in progress if your sort must be done immediately.</span></span> <span data-ttu-id="a110f-157">テーブル **に対する 1** つ以上の非同期操作が進行中のため、SortTable を続行できない場合は、テーブルのMAPI_E_BUSY。</span><span class="sxs-lookup"><span data-stu-id="a110f-157">If **SortTable** cannot continue because one or more asynchronous operations on the table are in progress, it returns MAPI_E_BUSY.</span></span> 
  
<span data-ttu-id="a110f-158">最適なパフォーマンスを得る場合は **、SetColumns** を呼び出してテーブルの列セットをカスタマイズし、並べ替えを実行するために **SortTable** を呼び出す前に、テーブル内の行数を制限します。</span><span class="sxs-lookup"><span data-stu-id="a110f-158">For best performance, call **SetColumns** to customize the table's column set and **Restrict** to limit the number of rows in the table before you call **SortTable** to perform the sort.</span></span> 
  
<span data-ttu-id="a110f-159">**SortTable が失敗** するたびに、エラーが発生する前に有効だった並べ替え順序は引き続き有効です。</span><span class="sxs-lookup"><span data-stu-id="a110f-159">Whenever **SortTable** fails, the sort order that was in effect before the failure is still in effect.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a110f-160">関連項目</span><span class="sxs-lookup"><span data-stu-id="a110f-160">See also</span></span>

- [<span data-ttu-id="a110f-161">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="a110f-161">IMAPITable::Abort</span></span>](imapitable-abort.md)
- [<span data-ttu-id="a110f-162">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="a110f-162">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
- [<span data-ttu-id="a110f-163">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="a110f-163">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
- [<span data-ttu-id="a110f-164">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="a110f-164">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
- [<span data-ttu-id="a110f-165">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="a110f-165">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
- [<span data-ttu-id="a110f-166">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="a110f-166">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="a110f-167">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a110f-167">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

