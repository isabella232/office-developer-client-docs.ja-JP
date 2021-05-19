---
title: IMAPITableSetColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SetColumns
api_type:
- COM
ms.assetid: 9a39cf8d-df0f-493c-b272-f15c65b3f15e
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 897330feb216dbc3ab143378977c77141cf488f0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416350"
---
# <a name="imapitablesetcolumns"></a><span data-ttu-id="45036-103">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="45036-103">IMAPITable::SetColumns</span></span>

  
  
<span data-ttu-id="45036-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45036-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45036-105">テーブルに列として表示するプロパティの特定のプロパティと順序を定義します。</span><span class="sxs-lookup"><span data-stu-id="45036-105">Defines the particular properties and order of properties to appear as columns in the table.</span></span>
  
```cpp
HRESULT SetColumns(
LPSPropTagArray lpPropTagArray,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="45036-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="45036-106">Parameters</span></span>

 <span data-ttu-id="45036-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="45036-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="45036-108">[in]テーブルに列として含めるプロパティを識別するプロパティ タグの配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="45036-108">[in] Pointer to an array of property tags identifying properties to be included as columns in the table.</span></span> <span data-ttu-id="45036-109">各タグのプロパティの種類の部分は、有効な型に設定するか、後続のPR_NULL領域を予約するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="45036-109">The property type portion of each tag can be set to a valid type or to **PR_NULL** to reserve space for subsequent additions.</span></span> <span data-ttu-id="45036-110">_lpPropTagArray_ パラメーターを NULL に設定することはできません。すべてのテーブルには、少なくとも 1 つの列が必要です。</span><span class="sxs-lookup"><span data-stu-id="45036-110">The  _lpPropTagArray_ parameter cannot be set to NULL; every table must have at least one column.</span></span> 
    
 <span data-ttu-id="45036-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="45036-111">_ulFlags_</span></span>
  
> <span data-ttu-id="45036-112">[in]通知で **SetColumns** を使用する場合など **、SetColumns** への非同期呼び出しの戻りを制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="45036-112">[in] Bitmask of flags that controls the return of an asynchronous call to **SetColumns**, for example when **SetColumns** is used in notification.</span></span> <span data-ttu-id="45036-113">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="45036-113">The following flags can be set:</span></span> 
    
<span data-ttu-id="45036-114">TBL_ASYNC</span><span class="sxs-lookup"><span data-stu-id="45036-114">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="45036-115">列設定操作を非同期的に実行して、操作が完全に完了する前に **SetColumns** が戻る可能性があるという要求。</span><span class="sxs-lookup"><span data-stu-id="45036-115">Requests that the column setting operation be performed asynchronously causing **SetColumns** to potentially return before the operation has fully completed.</span></span> 
    
<span data-ttu-id="45036-116">TBL_BATCH</span><span class="sxs-lookup"><span data-stu-id="45036-116">TBL_BATCH</span></span> 
  
> <span data-ttu-id="45036-117">データが実際に必要になるまで、テーブルが列設定操作を延期できます。</span><span class="sxs-lookup"><span data-stu-id="45036-117">Permits the table to postpone the column setting operation until the data is actually required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="45036-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="45036-118">Return value</span></span>

<span data-ttu-id="45036-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="45036-119">S_OK</span></span> 
  
> <span data-ttu-id="45036-120">列の設定操作が成功しました。</span><span class="sxs-lookup"><span data-stu-id="45036-120">The column setting operation was successful.</span></span>
    
<span data-ttu-id="45036-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="45036-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="45036-122">別の操作が進行中で、列の設定操作が開始しなかっています。</span><span class="sxs-lookup"><span data-stu-id="45036-122">Another operation is in progress that prevents the column setting operation from starting.</span></span> <span data-ttu-id="45036-123">進行中の操作の完了を許可するか、停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="45036-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="45036-124">注釈</span><span class="sxs-lookup"><span data-stu-id="45036-124">Remarks</span></span>

<span data-ttu-id="45036-125">テーブルの列セットは、テーブル内の行の列を表すプロパティのグループです。</span><span class="sxs-lookup"><span data-stu-id="45036-125">The column set of a table is the group of properties that make up the columns for the rows in the table.</span></span> <span data-ttu-id="45036-126">テーブルの種類ごとに既定の列セットがあります。</span><span class="sxs-lookup"><span data-stu-id="45036-126">There is a default column set for each type of table.</span></span> <span data-ttu-id="45036-127">既定の列セットは、テーブル実装者が自動的に含むプロパティで構成されます。</span><span class="sxs-lookup"><span data-stu-id="45036-127">The default column set is made up of the properties that the table implementer automatically includes.</span></span> <span data-ttu-id="45036-128">テーブル ユーザーは **、IMAPITable::SetColumns メソッドを呼び出すことによって、この既定のセットを変更** できます。</span><span class="sxs-lookup"><span data-stu-id="45036-128">Table users can alter this default set by calling the **IMAPITable::SetColumns** method.</span></span> <span data-ttu-id="45036-129">テーブルの実装者が列の削除をサポートしている場合、または列の順序を変更する場合は、他の列を既定のセットに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="45036-129">They can request that other columns be added to the default set if the table implementer supports them that columns be removed, or that the order of columns be changed.</span></span> <span data-ttu-id="45036-130">**SetColumns は** 、各行で返される列と、行内のこれらの列の順序を指定します。</span><span class="sxs-lookup"><span data-stu-id="45036-130">**SetColumns** specifies the columns that are returned with each row and the order of these columns within the row.</span></span> 
  
<span data-ttu-id="45036-131">**SetColumns** 操作の成功は、テーブルのデータを取得するために後続の呼び出しが行われた後にのみ明らかです。</span><span class="sxs-lookup"><span data-stu-id="45036-131">The success of the **SetColumns** operation is apparent only after a subsequent call has been made to retrieve the data of the table.</span></span> <span data-ttu-id="45036-132">その後、エラーが報告されます。</span><span class="sxs-lookup"><span data-stu-id="45036-132">It is then that any errors are reported.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="45036-133">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="45036-133">Notes to implementers</span></span>

<span data-ttu-id="45036-134">一部のプロバイダーでは **、SetColumns** 呼び出しを使用して、テーブル ビューで使用可能な列の一部であるテーブル列のみを順序付けできます。</span><span class="sxs-lookup"><span data-stu-id="45036-134">Some providers allow a **SetColumns** call to order only table columns that are part of the available columns for a table view.</span></span> <span data-ttu-id="45036-135">他のプロバイダーでは **、SetColumns** 呼び出しを使用して、元の列セットに含まれるプロパティを含むすべてのテーブル列を並び替えできます。</span><span class="sxs-lookup"><span data-stu-id="45036-135">Other providers allow a **SetColumns** call to order all table columns, including those containing properties not in the original column set.</span></span> 
  
<span data-ttu-id="45036-136">非同期TBL_BATCH設定されている場合、プロバイダーはプロパティの種類 PT_ERROR と、サポートされていない列のプロパティ値 NULL を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="45036-136">When TBL_BATCH is set for asynchronous operations, providers should return a property type of PT_ERROR and a property value of NULL for columns that are not supported.</span></span>
  
<span data-ttu-id="45036-137">操作を非同期に要求するTBL_ASYNCフラグに応答する必要はない。</span><span class="sxs-lookup"><span data-stu-id="45036-137">You do not need to respond to the TBL_ASYNC flag requesting that the operation be asynchronous.</span></span> <span data-ttu-id="45036-138">非同期列セット定義をサポートしない場合は、同期的に操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="45036-138">If you do not support asynchronous column set definition, perform the operation synchronously.</span></span> <span data-ttu-id="45036-139">このフラグをサポートして、TBL_ASYNC非同期操作がまだ進行中の場合は、このフラグをMAPI_E_BUSY。</span><span class="sxs-lookup"><span data-stu-id="45036-139">If you can support the TBL_ASYNC flag and another asynchronous operation is still in progress, return MAPI_E_BUSY.</span></span> <span data-ttu-id="45036-140">それ以外の場合S_OK、プロパティ タグ配列に含まれるすべてのプロパティをサポートするかどうかに関係なく、値を返します。</span><span class="sxs-lookup"><span data-stu-id="45036-140">Otherwise, return S_OK regardless of whether or not you support all of the properties included in the property tag array.</span></span> <span data-ttu-id="45036-141">サポートされていないプロパティに起因するエラーは **、QueryRows** などのデータを取得する IMAPITable メソッドから **返す必要があります**。</span><span class="sxs-lookup"><span data-stu-id="45036-141">Errors resulting from unsupported properties should be returned from **IMAPITable** methods that retrieve data, such as **QueryRows**.</span></span> 
  
<span data-ttu-id="45036-142">Restrict の呼び出しによって表示されないテーブル行に対する通知を生成 **しません**。</span><span class="sxs-lookup"><span data-stu-id="45036-142">Do not generate notifications for table rows that are hidden from view by calls to **Restrict**.</span></span> 
  
<span data-ttu-id="45036-143">テーブル通知を送信する場合、TABLE_NOTIFICATION 構造体の行メンバー内のプロパティの順序と、最新の **SetColumns** 呼び出しで指定された順序は、通知要求が送信された時刻と同じにする必要があります。 [](table_notification.md)</span><span class="sxs-lookup"><span data-stu-id="45036-143">When sending table notifications, the order of the properties in the **row** member of the [TABLE_NOTIFICATION](table_notification.md) structure and the order specified by the most recent **SetColumns** call must be the same as of the time that the notification request was sent.</span></span> 
  
<span data-ttu-id="45036-144">別のフラグTBL_BATCHを使用すると、呼び出し元は、テーブルの実装者が操作の結果の評価を後で延期できると指定できます。</span><span class="sxs-lookup"><span data-stu-id="45036-144">Another flag, TBL_BATCH, allows callers to specify that the table implementer can defer evaluating the results of the operation until a later time.</span></span> <span data-ttu-id="45036-145">可能な限り、バッチ処理された操作によってパフォーマンスが向上するために、呼び出し元はこのフラグを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="45036-145">Whenever possible, callers should set this flag because batched operation improves performance.</span></span>
  
<span data-ttu-id="45036-146">多くの場合、呼び出し元は、取得した行セットの一部の列を予約して、後で値を追加する場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="45036-146">It is often convenient for callers to reserve some columns in the retrieved row set for values to be added later.</span></span> <span data-ttu-id="45036-147">呼び出し元は、SetColumns に渡 **PR_NULLプロパティ** タグ配列内の目的の位置に [(PidTagNull)](pidtagnull-canonical-property.md)を配置して **、これを行います**。次に **、QueryRows** で **取得PR_NULL** 行の位置にテーブルが戻されます。</span><span class="sxs-lookup"><span data-stu-id="45036-147">Callers do this by placing **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) at the desired positions in the property tag array passed to **SetColumns**; the table will then pass back **PR_NULL** at those positions in all rows retrieved with **QueryRows**.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="45036-148">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="45036-148">Notes to callers</span></span>

<span data-ttu-id="45036-149">_lpPropTagArray_ パラメーターのプロパティ タグ配列を作成する場合は、テーブル ビューに列を表示する順序でタグを並び替えます。</span><span class="sxs-lookup"><span data-stu-id="45036-149">When building the property tag array for the  _lpPropTagArray_ parameter, order the tags in the order that you want the columns to appear in the table view.</span></span> 
  
<span data-ttu-id="45036-150">複数値インスタンス フラグまたは定数をプロパティ タグに適用することで、列セットに含める複数値プロパティMVI_FLAG指定できます。</span><span class="sxs-lookup"><span data-stu-id="45036-150">You can specify multivalued properties to be included in the column set by applying the multivalued instance flag, or MVI_FLAG constant, to the property tag.</span></span> <span data-ttu-id="45036-151">このフラグを設定するには、プロパティの単一値バージョンのプロパティ タグをパラメーターとして、MVI_PROPマクロに渡します。</span><span class="sxs-lookup"><span data-stu-id="45036-151">Set this flag by passing the property tag for the single-valued version of the property as a parameter to the MVI_PROP macro as follows:</span></span>
  
```
MVI_PROP(ulPropTag)

```

<span data-ttu-id="45036-152">プロパティMVI_PROPマクロMVI_FLAG設定し、タグを複数値タグに変換します。</span><span class="sxs-lookup"><span data-stu-id="45036-152">The MVI_PROP macro will set MVI_FLAG for the property, turning the tag into a multivalued tag.</span></span> <span data-ttu-id="45036-153">1 つの値を持つプロパティMVI_PROP誤って呼び出しを試みた場合、MAPI は呼び出しを無視し、プロパティ タグを変更しません。</span><span class="sxs-lookup"><span data-stu-id="45036-153">If you erroneously try to call MVI_PROP on a single-valued property, MAPI will ignore the call and leave the property tag unchanged.</span></span> 
  
<span data-ttu-id="45036-154">プロパティ タグ配列にプロパティタグPR_NULLを含め、列セット内の領域を予約できます。</span><span class="sxs-lookup"><span data-stu-id="45036-154">You can include property tags set to **PR_NULL** in the property tag array to reserve space in the column set.</span></span> <span data-ttu-id="45036-155">領域を予約すると、新しいプロパティ タグ配列を割り当てなくても列セットに追加できます。</span><span class="sxs-lookup"><span data-stu-id="45036-155">Reserving space allows you to add to a column set without having to allocate a new property tag array.</span></span> 
  
<span data-ttu-id="45036-156">**SetColumns** の呼び出しによってテーブルの列の順序が変更され、これらの列の 1 つ以上が複数値プロパティを表す場合、テーブル内の行数が増える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="45036-156">When your call to **SetColumns** causes a change to the order of a table's columns and one or more of these columns represent a multivalued property, it is possible for the number of rows in the table to increase.</span></span> <span data-ttu-id="45036-157">この場合、テーブルのすべてのブックマークが破棄されます。</span><span class="sxs-lookup"><span data-stu-id="45036-157">If this occurs, all of the bookmarks for the table are discarded.</span></span> <span data-ttu-id="45036-158">複数値の列がテーブルに与える影響の詳細については、「複数値列の操作 [」を参照してください](working-with-multivalued-columns.md)。</span><span class="sxs-lookup"><span data-stu-id="45036-158">For more information about how multivalued columns affect tables, see [Working with Multivalued Columns](working-with-multivalued-columns.md).</span></span>
  
<span data-ttu-id="45036-159">列の設定は、既定では同期操作です。</span><span class="sxs-lookup"><span data-stu-id="45036-159">Setting columns is by default a synchronous operation.</span></span> <span data-ttu-id="45036-160">ただし、データが必要になるまで、テーブルで操作を延期するには、このフラグを設定TBL_BATCHできます。</span><span class="sxs-lookup"><span data-stu-id="45036-160">However, you can allow the table to postpone the operation until such time as the data is needed by setting the TBL_BATCH flag.</span></span> <span data-ttu-id="45036-161">このフラグを設定すると、パフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="45036-161">Setting this flag can improve performance.</span></span> <span data-ttu-id="45036-162">別のフラグTBL_ASYNC、操作を非同期にし、操作が完了する前に **SetColumns** を返します。</span><span class="sxs-lookup"><span data-stu-id="45036-162">Another flag, TBL_ASYNC, makes the operation asynchronous, allowing **SetColumns** to return before the operation is complete.</span></span> <span data-ttu-id="45036-163">完了が発生した時刻を確認するには [、IMAPITable::GetStatus を呼び出します](imapitable-getstatus.md)。</span><span class="sxs-lookup"><span data-stu-id="45036-163">To determine when completion occurs, call [IMAPITable::GetStatus](imapitable-getstatus.md).</span></span>
  
<span data-ttu-id="45036-164">**SetColumns** の呼び出しが MAPI_E_BUSY を返し、別の操作によって操作が開始されていないことを示す場合は [、IMAPITable::Abort](imapitable-abort.md)を呼び出して、進行中の操作を停止できます。</span><span class="sxs-lookup"><span data-stu-id="45036-164">If a call to **SetColumns** returns MAPI_E_BUSY, indicating that another operation is preventing your operation from starting, you can call [IMAPITable::Abort](imapitable-abort.md) to stop the operation in progress.</span></span> 
  
<span data-ttu-id="45036-165">また [、HrAddColumnsEx を呼び出して](hraddcolumnsex.md) 列セットを変更できます。</span><span class="sxs-lookup"><span data-stu-id="45036-165">You can also call [HrAddColumnsEx](hraddcolumnsex.md) to change a column set.</span></span> <span data-ttu-id="45036-166">**HrAddColumnsEx** と **IMAPITable::SetColumns** の違いは **、HrAddColumnsEx** の柔軟性が低い点です。列の追加のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="45036-166">The difference between **HrAddColumnsEx** and **IMAPITable::SetColumns** is that **HrAddColumnsEx** is less flexible; it can only add columns.</span></span> <span data-ttu-id="45036-167">追加の列は、列セットの先頭に配置されます。すべての既存の列は、これらの列の後に表示されます。</span><span class="sxs-lookup"><span data-stu-id="45036-167">The additional columns are placed at the beginning of the column set; all existing columns appear following these columns.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="45036-168">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="45036-168">MFCMAPI reference</span></span>

<span data-ttu-id="45036-169">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="45036-169">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="45036-170">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="45036-170">**File**</span></span>|<span data-ttu-id="45036-171">**関数**</span><span class="sxs-lookup"><span data-stu-id="45036-171">**Function**</span></span>|<span data-ttu-id="45036-172">**コメント**</span><span class="sxs-lookup"><span data-stu-id="45036-172">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="45036-173">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="45036-173">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="45036-174">CContentsTableListCtrl::D oSetColumns</span><span class="sxs-lookup"><span data-stu-id="45036-174">CContentsTableListCtrl::DoSetColumns</span></span>  <br/> |<span data-ttu-id="45036-175">MFCMAPI は **IMAPITable::SetColumns** メソッドを使用して、テーブルに必要な列を設定します。</span><span class="sxs-lookup"><span data-stu-id="45036-175">MFCMAPI uses the **IMAPITable::SetColumns** method to set the desired columns for the table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="45036-176">関連項目</span><span class="sxs-lookup"><span data-stu-id="45036-176">See also</span></span>



[<span data-ttu-id="45036-177">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="45036-177">HrQueryAllRows</span></span>](hrqueryallrows.md)
  
[<span data-ttu-id="45036-178">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="45036-178">IMAPITable::Abort</span></span>](imapitable-abort.md)
  
[<span data-ttu-id="45036-179">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="45036-179">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="45036-180">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="45036-180">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="45036-181">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="45036-181">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="45036-182">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="45036-182">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="45036-183">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="45036-183">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="45036-184">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="45036-184">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="45036-185">SPropValue</span><span class="sxs-lookup"><span data-stu-id="45036-185">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="45036-186">SRowSet</span><span class="sxs-lookup"><span data-stu-id="45036-186">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="45036-187">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="45036-187">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="45036-188">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="45036-188">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


<span data-ttu-id="45036-189">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="45036-189">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

