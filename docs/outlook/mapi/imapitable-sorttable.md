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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328855"
---
# <a name="imapitablesorttable"></a><span data-ttu-id="75bf7-103">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="75bf7-103">IMAPITable::SortTable</span></span>

<span data-ttu-id="75bf7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="75bf7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="75bf7-105">**IMAPITable:: sorttable**メソッドは、並べ替え条件に従って、テーブルの行を順序付けることができます。</span><span class="sxs-lookup"><span data-stu-id="75bf7-105">The **IMAPITable::SortTable** method orders the rows of the table, depending on sort criteria.</span></span> 
  
```cpp
HRESULT SortTable(
LPSSortOrderSet lpSortCriteria,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="75bf7-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="75bf7-106">Parameters</span></span>

<span data-ttu-id="75bf7-107">_lpsortcriteria_</span><span class="sxs-lookup"><span data-stu-id="75bf7-107">_lpSortCriteria_</span></span>
  
> <span data-ttu-id="75bf7-108">順番適用する並べ替え基準を含む[ssortorderset](ssortorderset.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="75bf7-108">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure that contains the sort criteria to apply.</span></span> <span data-ttu-id="75bf7-109">列が0の**ssortorderset**構造を渡すと、テーブルを特定の順序で並べ替える必要がないことを示します。</span><span class="sxs-lookup"><span data-stu-id="75bf7-109">Passing an **SSortOrderSet** structure that contains zero columns indicates that the table does not have to be sorted in any particular order.</span></span> 
    
<span data-ttu-id="75bf7-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="75bf7-110">_ulFlags_</span></span>
  
> <span data-ttu-id="75bf7-111">順番**IMAPITable:: sorttable**操作のタイミングを制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="75bf7-111">[in] Bitmask of flags that controls the timing of the **IMAPITable::SortTable** operation.</span></span> <span data-ttu-id="75bf7-112">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="75bf7-112">The following flags can be set:</span></span> 
    
<span data-ttu-id="75bf7-113">TBL_ASYNC</span><span class="sxs-lookup"><span data-stu-id="75bf7-113">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="75bf7-114">操作を非同期的に開始し、操作が完了する前に制御を戻します。</span><span class="sxs-lookup"><span data-stu-id="75bf7-114">Starts the operation asynchronously and returns before the operation is complete.</span></span>
    
<span data-ttu-id="75bf7-115">TBL_BATCH</span><span class="sxs-lookup"><span data-stu-id="75bf7-115">TBL_BATCH</span></span> 
  
> <span data-ttu-id="75bf7-116">テーブル内のデータが必要になるまで、並べ替えの完了を延期します。</span><span class="sxs-lookup"><span data-stu-id="75bf7-116">Defers the completion of the sort until the data in the table is required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="75bf7-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="75bf7-117">Return value</span></span>

<span data-ttu-id="75bf7-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="75bf7-118">S_OK</span></span> 
  
> <span data-ttu-id="75bf7-119">並べ替え操作が正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="75bf7-119">The sort operation was successful.</span></span>
    
<span data-ttu-id="75bf7-120">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="75bf7-120">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="75bf7-121">別の操作が進行中なので、並べ替え操作を開始できません。</span><span class="sxs-lookup"><span data-stu-id="75bf7-121">Another operation is in progress that prevents the sort operation from starting.</span></span> <span data-ttu-id="75bf7-122">進行中の操作が完了することを許可するか、停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="75bf7-122">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="75bf7-123">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="75bf7-123">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="75bf7-124">テーブルは、要求された並べ替えの種類をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="75bf7-124">The table does not support the type of sorting requested.</span></span>
    
<span data-ttu-id="75bf7-125">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="75bf7-125">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="75bf7-126">_lpsortcriteria_パラメーターによって指定された特定の並べ替え条件が複雑すぎるため、テーブルが操作を実行できません。</span><span class="sxs-lookup"><span data-stu-id="75bf7-126">The table cannot perform the operation because the particular sort criteria pointed to by the  _lpSortCriteria_ parameter is too complex.</span></span> <span data-ttu-id="75bf7-127">**sorttable**は、次の条件下で MAPI_E_TOO_COMPLEX を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="75bf7-127">**SortTable** can return MAPI_E_TOO_COMPLEX under the following conditions.</span></span> 
    
   - <span data-ttu-id="75bf7-128">実装で並べ替えることができないプロパティ列に対して並べ替え操作が要求されています。</span><span class="sxs-lookup"><span data-stu-id="75bf7-128">A sort operation is requested for a property column that the implementation cannot sort.</span></span>
    
   - <span data-ttu-id="75bf7-129">実装では、 **ssortorderset**構造の**ulorder**メンバーで要求されている並べ替え順序はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="75bf7-129">The implementation does not support the sort order requested in the **ulOrder** member of the **SSortOrderSet** structure.</span></span> 
    
   - <span data-ttu-id="75bf7-130">**ssortorderset**の csorts メンバーで指定され\*\*\*\* ているように並べ替えられる列の数が、実装で処理できるサイズを超えています。</span><span class="sxs-lookup"><span data-stu-id="75bf7-130">The number of columns to be sorted, as specified in the **cSorts** member in **SSortOrderSet**, is larger than the implementation can handle.</span></span>
    
   - <span data-ttu-id="75bf7-131">使用可能なセットまたはアクティブなセットに含まれていないプロパティに基づいて、 **ssortorderset**のプロパティタグによって示されているように、並べ替え操作が要求されます。実装は、使用可能なセットに含まれていないプロパティに対する並べ替えをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="75bf7-131">A sort operation is requested, as indicated by a property tag in **SSortOrderSet**, based on a property that is not in the available or active set and the implementation does not support sorting on properties not in the available set.</span></span>
    
   - <span data-ttu-id="75bf7-132">1つのプロパティが、同じプロパティタグの複数のインスタンスによって示されるように、並べ替え順序セットで複数回指定されています。実装では、このような並べ替え操作を実行できません。</span><span class="sxs-lookup"><span data-stu-id="75bf7-132">One property is specified multiple times in a sort order set, as indicated by multiple instances of the same property tag, and the implementation cannot perform such a sort operation.</span></span>
    
   - <span data-ttu-id="75bf7-133">複数値プロパティ列に基づく並べ替え操作は、MVI_FLAG を使用して要求されます。実装では、複数値プロパティの並べ替えはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="75bf7-133">A sort operation based on multivalued property columns is requested using MVI_FLAG and the implementation does not support sorting on multivalued properties.</span></span> 
    
   - <span data-ttu-id="75bf7-134">**ssortorderset**のプロパティのプロパティタグには、実装でサポートされていないプロパティまたは型が指定されています。</span><span class="sxs-lookup"><span data-stu-id="75bf7-134">A property tag for a property in **SSortOrderSet** specifies a property or type that the implementation does not support.</span></span> 
    
   - <span data-ttu-id="75bf7-135">**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) プロパティの前にあるテーブルを処理する以外の並べ替え操作は、この種類の並べ替えをサポートする添付ファイルテーブルに対してのみ指定されます。</span><span class="sxs-lookup"><span data-stu-id="75bf7-135">A sort operation other than one that proceeds through the table from the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property forward is specified only for an attachment table that supports this type of sorting.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="75bf7-136">解説</span><span class="sxs-lookup"><span data-stu-id="75bf7-136">Remarks</span></span>

<span data-ttu-id="75bf7-137">**IMAPITable:: sorttable**メソッドは、テーブルビュー内の行の順序を示します。</span><span class="sxs-lookup"><span data-stu-id="75bf7-137">The **IMAPITable::SortTable** method orders the rows in a table view.</span></span> <span data-ttu-id="75bf7-138">一部の表では、さまざまな並べ替えキー列に対して標準の並べ替えと分類された並べ替えの両方をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="75bf7-138">Whereas some tables support both standard and categorized sorting on various sort key columns, other tables are more limited in their support.</span></span> <span data-ttu-id="75bf7-139">アドレス帳プロバイダーは、通常、テーブルの並べ替えをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="75bf7-139">Address book providers ordinarily do not support table sorting.</span></span> <span data-ttu-id="75bf7-140">通常、メッセージストアプロバイダーは、完全なテーブル (制限なしのテーブル) が並べ替えられている場合に、結果となるフォルダーの並べ替え順序を維持することによって、エクステントへの並べ替えをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="75bf7-140">Message store providers usually support sorting to the extent that they keep the sort order of folders that results when a full table (a table without restrictions) is sorted.</span></span> 
  
<span data-ttu-id="75bf7-141">テーブルによっては、任意の表の列に対して並べ替えを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="75bf7-141">Some tables allow sorting to be done on any table column.</span></span> <span data-ttu-id="75bf7-142">その他のテーブルは含まれません。テーブルビューに含まれていない列は、 **sorttable**呼び出しの影響を受けません。</span><span class="sxs-lookup"><span data-stu-id="75bf7-142">Other tables do not; columns not included in the table view are unaffected by a **SortTable** call.</span></span> <span data-ttu-id="75bf7-143">一部のテーブルでは、テーブルの現在の列セットの列を指定して並べ替えキーを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="75bf7-143">Some tables require that sort keys be built only with columns in the table's current column set.</span></span> 
  
<span data-ttu-id="75bf7-144">表は、並べ替え操作を完了できない\*\*\*\* 場合に、MAPI_E_NO_SUPPORT または MAPI_E_TOO_COMPLEX のいずれかを返すことができます。</span><span class="sxs-lookup"><span data-stu-id="75bf7-144">A table can return either MAPI_E_NO_SUPPORT or MAPI_E_TOO_COMPLEX from **SortTable** when it cannot complete a sort operation.</span></span> <span data-ttu-id="75bf7-145">さらに、ストアプロバイダーは、階層テーブルに指定された並べ替え順序セットを優先することを保証されません。</span><span class="sxs-lookup"><span data-stu-id="75bf7-145">Moreover, store providers are not guaranteed to honor the sort order set specified for hierarchy tables.</span></span> 
  
<span data-ttu-id="75bf7-146">_lpsortcriteria_パラメーターで指定された[ssortorderset](ssortorderset.md)構造体に0列がある場合、テーブルは現在の列セットを返します。</span><span class="sxs-lookup"><span data-stu-id="75bf7-146">When there are zero columns in the [SSortOrderSet](ssortorderset.md) structure pointed to by the  _lpSortCriteria_ parameter, the table returns the current column set.</span></span> <span data-ttu-id="75bf7-147">現在の並べ替え順序を取得するには、テーブルの[IMAPITable:: querysortorder](imapitable-querysortorder.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="75bf7-147">The current sort order can be retrieved by calling the table's [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
<span data-ttu-id="75bf7-148">テーブルのすべてのブックマークは無効になっており、 **sorttable**への呼び出しが行われ、現在のカーソル位置を示す BOOKMARK_CURRENT ブックマークがテーブルの先頭に設定されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="75bf7-148">All bookmarks for a table are invalidated and should be deleted when a call to **SortTable** is made, and the BOOKMARK_CURRENT bookmark that indicates the current cursor position, should be set to the beginning of the table.</span></span> 
  
<span data-ttu-id="75bf7-149">MVI_FLAG フラグが設定されていない複数値プロパティを含む列に対して並べ替えを行う場合、列の値は完全に順序付けられた組として扱われます。</span><span class="sxs-lookup"><span data-stu-id="75bf7-149">If you are sorting on a column that contains a multivalued property without the MVI_FLAG flag set, the column's values are treated as a completely ordered tuple.</span></span> <span data-ttu-id="75bf7-150">2つの複数値列の比較によって、列の要素が順に比較され、最初の不等式の列のリレーションシップがレポートされます。比較する列に同じ順序で同じ値が含まれている場合にのみ、等価を返します。</span><span class="sxs-lookup"><span data-stu-id="75bf7-150">A comparison of two multivalued columns compares the column elements in order, reporting the relation of the columns at the first inequality, and returns equality only if the columns being compared contain the same values in the same order.</span></span> <span data-ttu-id="75bf7-151">一方の列の値がもう一方の列の値よりも小さい場合は、レポートされたリレーションシップは、null 値が他の値になることを示します。</span><span class="sxs-lookup"><span data-stu-id="75bf7-151">If one column has fewer values than the other, the reported relation is that of a null value to the other value.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="75bf7-152">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="75bf7-152">Notes to callers</span></span>

<span data-ttu-id="75bf7-153">**sorttable**は、フラグの1つを設定しない限り、同期して動作します。</span><span class="sxs-lookup"><span data-stu-id="75bf7-153">**SortTable** operates synchronously unless you set one of the flags.</span></span> <span data-ttu-id="75bf7-154">TBL_BATCH フラグを設定すると、データを要求しない限り、 **sorttable**は並べ替え操作を延期します。</span><span class="sxs-lookup"><span data-stu-id="75bf7-154">If you set the TBL_BATCH flag, **SortTable** postpones the sort operation unless you request the data.</span></span> <span data-ttu-id="75bf7-155">TBL_ASYNC フラグが設定されている場合、 **sorttable**は非同期で動作し、操作が完了する前に戻る可能性があります。</span><span class="sxs-lookup"><span data-stu-id="75bf7-155">If the TBL_ASYNC flag is set, **SortTable** operates asynchronously, potentially returning before the completion of the operation.</span></span> 
  
<span data-ttu-id="75bf7-156">必要な処理を停止するには、 [IMAPITable:: Abort](imapitable-abort.md)メソッドを呼び出します。並べ替えをすぐに実行する必要がある場合です。</span><span class="sxs-lookup"><span data-stu-id="75bf7-156">Call the [IMAPITable::Abort](imapitable-abort.md) method to stop an asynchronous operation in progress if your sort must be done immediately.</span></span> <span data-ttu-id="75bf7-157">テーブルに対する1つ以上の非同期操作が進行中であるために**sorttable**を続行できない場合は、MAPI_E_BUSY が返されます。</span><span class="sxs-lookup"><span data-stu-id="75bf7-157">If **SortTable** cannot continue because one or more asynchronous operations on the table are in progress, it returns MAPI_E_BUSY.</span></span> 
  
<span data-ttu-id="75bf7-158">最適なパフォーマンスを得るために、 **SetColumns**を呼び出してテーブルの列セットをカスタマイズし、並べ替えを実行する前にテーブル\*\*\*\* の行数を制限するように**制限**します。</span><span class="sxs-lookup"><span data-stu-id="75bf7-158">For best performance, call **SetColumns** to customize the table's column set and **Restrict** to limit the number of rows in the table before you call **SortTable** to perform the sort.</span></span> 
  
<span data-ttu-id="75bf7-159">**sorttable**に障害が発生すると、その前に有効になっていた並べ替え順序が引き続き有効になります。</span><span class="sxs-lookup"><span data-stu-id="75bf7-159">Whenever **SortTable** fails, the sort order that was in effect before the failure is still in effect.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="75bf7-160">関連項目</span><span class="sxs-lookup"><span data-stu-id="75bf7-160">See also</span></span>

- [<span data-ttu-id="75bf7-161">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="75bf7-161">IMAPITable::Abort</span></span>](imapitable-abort.md)
- [<span data-ttu-id="75bf7-162">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="75bf7-162">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
- [<span data-ttu-id="75bf7-163">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="75bf7-163">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
- [<span data-ttu-id="75bf7-164">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="75bf7-164">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
- [<span data-ttu-id="75bf7-165">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="75bf7-165">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
- [<span data-ttu-id="75bf7-166">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="75bf7-166">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="75bf7-167">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="75bf7-167">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

