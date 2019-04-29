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
# <a name="imapitablesetcolumns"></a><span data-ttu-id="cf8dd-103">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="cf8dd-103">IMAPITable::SetColumns</span></span>

  
  
<span data-ttu-id="cf8dd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf8dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf8dd-105">表に列として表示されるプロパティとプロパティの順序を定義します。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-105">Defines the particular properties and order of properties to appear as columns in the table.</span></span>
  
```cpp
HRESULT SetColumns(
LPSPropTagArray lpPropTagArray,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="cf8dd-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cf8dd-106">Parameters</span></span>

 <span data-ttu-id="cf8dd-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="cf8dd-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="cf8dd-108">順番テーブル内の列として含めるプロパティを識別するプロパティタグの配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-108">[in] Pointer to an array of property tags identifying properties to be included as columns in the table.</span></span> <span data-ttu-id="cf8dd-109">各タグのプロパティの種類の部分は、有効な種類または**PR_NULL**に設定して、以降の追加のためにスペースを予約できます。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-109">The property type portion of each tag can be set to a valid type or to **PR_NULL** to reserve space for subsequent additions.</span></span> <span data-ttu-id="cf8dd-110">_lpPropTagArray_パラメーターを NULL に設定することはできません。各テーブルには、少なくとも1つの列が必要です。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-110">The  _lpPropTagArray_ parameter cannot be set to NULL; every table must have at least one column.</span></span> 
    
 <span data-ttu-id="cf8dd-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cf8dd-111">_ulFlags_</span></span>
  
> <span data-ttu-id="cf8dd-112">順番**SetColumns**が通知で使用されている場合など、 **SetColumns**への非同期呼び出しの戻りを制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-112">[in] Bitmask of flags that controls the return of an asynchronous call to **SetColumns**, for example when **SetColumns** is used in notification.</span></span> <span data-ttu-id="cf8dd-113">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-113">The following flags can be set:</span></span> 
    
<span data-ttu-id="cf8dd-114">TBL_ASYNC</span><span class="sxs-lookup"><span data-stu-id="cf8dd-114">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="cf8dd-115">操作が完全に完了する前に**SetColumns**を戻すことができるように、列設定操作を非同期的に実行するように要求します。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-115">Requests that the column setting operation be performed asynchronously causing **SetColumns** to potentially return before the operation has fully completed.</span></span> 
    
<span data-ttu-id="cf8dd-116">TBL_BATCH</span><span class="sxs-lookup"><span data-stu-id="cf8dd-116">TBL_BATCH</span></span> 
  
> <span data-ttu-id="cf8dd-117">テーブルで、データが実際に必要になるまで、列設定操作を延期できるようにします。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-117">Permits the table to postpone the column setting operation until the data is actually required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cf8dd-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="cf8dd-118">Return value</span></span>

<span data-ttu-id="cf8dd-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="cf8dd-119">S_OK</span></span> 
  
> <span data-ttu-id="cf8dd-120">列の設定操作が正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-120">The column setting operation was successful.</span></span>
    
<span data-ttu-id="cf8dd-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="cf8dd-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="cf8dd-122">別の操作が進行中であるため、列の設定操作を開始できません。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-122">Another operation is in progress that prevents the column setting operation from starting.</span></span> <span data-ttu-id="cf8dd-123">進行中の操作が完了することを許可するか、停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cf8dd-124">注釈</span><span class="sxs-lookup"><span data-stu-id="cf8dd-124">Remarks</span></span>

<span data-ttu-id="cf8dd-125">table の列セットは、テーブル内の行の列を構成するプロパティのグループです。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-125">The column set of a table is the group of properties that make up the columns for the rows in the table.</span></span> <span data-ttu-id="cf8dd-126">テーブルの種類ごとに既定の列セットがあります。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-126">There is a default column set for each type of table.</span></span> <span data-ttu-id="cf8dd-127">既定の列セットは、テーブルの作成者が自動的に含めるプロパティで構成されます。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-127">The default column set is made up of the properties that the table implementer automatically includes.</span></span> <span data-ttu-id="cf8dd-128">Table ユーザーは、 **IMAPITable:: SetColumns**メソッドを呼び出すことによって、この既定のセットを変更できます。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-128">Table users can alter this default set by calling the **IMAPITable::SetColumns** method.</span></span> <span data-ttu-id="cf8dd-129">これらのユーザーは、テーブルの実装で列が削除されるか、列の順序が変更される場合に、他の列が既定のセットに追加されるように要求できます。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-129">They can request that other columns be added to the default set if the table implementer supports them that columns be removed, or that the order of columns be changed.</span></span> <span data-ttu-id="cf8dd-130">**SetColumns**各行で返される列と、行内でこれらの列の順序を指定します。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-130">**SetColumns** specifies the columns that are returned with each row and the order of these columns within the row.</span></span> 
  
<span data-ttu-id="cf8dd-131">**SetColumns**操作の成功は、テーブルのデータを取得するために後続の呼び出しが行われた後にのみ、明らかです。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-131">The success of the **SetColumns** operation is apparent only after a subsequent call has been made to retrieve the data of the table.</span></span> <span data-ttu-id="cf8dd-132">これにより、エラーが報告されます。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-132">It is then that any errors are reported.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="cf8dd-133">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="cf8dd-133">Notes to implementers</span></span>

<span data-ttu-id="cf8dd-134">プロバイダーによっては、テーブルビューで使用可能な列の一部であるテーブル列のみを注文する**SetColumns**呼び出しを許可します。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-134">Some providers allow a **SetColumns** call to order only table columns that are part of the available columns for a table view.</span></span> <span data-ttu-id="cf8dd-135">その他のプロバイダーでは、 **SetColumns**呼び出しを使用して、元の列セットにないプロパティを含むすべてのテーブル列を並べ替えることができます。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-135">Other providers allow a **SetColumns** call to order all table columns, including those containing properties not in the original column set.</span></span> 
  
<span data-ttu-id="cf8dd-136">TBL_BATCH が非同期操作のために設定されている場合、プロバイダーは、サポートされていない列の PT_ERROR のプロパティの種類とプロパティの値を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-136">When TBL_BATCH is set for asynchronous operations, providers should return a property type of PT_ERROR and a property value of NULL for columns that are not supported.</span></span>
  
<span data-ttu-id="cf8dd-137">操作が非同期であることを要求する TBL_ASYNC フラグに応答する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-137">You do not need to respond to the TBL_ASYNC flag requesting that the operation be asynchronous.</span></span> <span data-ttu-id="cf8dd-138">非同期列セット定義をサポートしていない場合は、操作を同期的に実行します。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-138">If you do not support asynchronous column set definition, perform the operation synchronously.</span></span> <span data-ttu-id="cf8dd-139">TBL_ASYNC フラグをサポートしていて、別の非同期操作がまだ実行中の場合は、MAPI_E_BUSY を返します。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-139">If you can support the TBL_ASYNC flag and another asynchronous operation is still in progress, return MAPI_E_BUSY.</span></span> <span data-ttu-id="cf8dd-140">それ以外の場合は、プロパティタグ配列に含まれるすべてのプロパティをサポートしているかどうかにかかわらず、S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-140">Otherwise, return S_OK regardless of whether or not you support all of the properties included in the property tag array.</span></span> <span data-ttu-id="cf8dd-141">サポートされていないプロパティから生じるエラーは、 **QueryRows**などのデータを取得する**IMAPITable**メソッドから返されます。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-141">Errors resulting from unsupported properties should be returned from **IMAPITable** methods that retrieve data, such as **QueryRows**.</span></span> 
  
<span data-ttu-id="cf8dd-142">**制限**の呼び出しによって非表示になっているテーブルの行については通知を生成しません。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-142">Do not generate notifications for table rows that are hidden from view by calls to **Restrict**.</span></span> 
  
<span data-ttu-id="cf8dd-143">テーブル通知を送信する場合、 [TABLE_NOTIFICATION](table_notification.md)構造体の**行**メンバーのプロパティと、最新の**SetColumns**呼び出しで指定されている順序は、通知要求の時刻と同じである必要があります。送信されました。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-143">When sending table notifications, the order of the properties in the **row** member of the [TABLE_NOTIFICATION](table_notification.md) structure and the order specified by the most recent **SetColumns** call must be the same as of the time that the notification request was sent.</span></span> 
  
<span data-ttu-id="cf8dd-144">もう1つのフラグ TBL_BATCH を使用すると、テーブルの実装者が後で操作の結果を評価することを指定できます。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-144">Another flag, TBL_BATCH, allows callers to specify that the table implementer can defer evaluating the results of the operation until a later time.</span></span> <span data-ttu-id="cf8dd-145">バッチ処理を行うとパフォーマンスが向上するため、可能な限り、発信者はこのフラグを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-145">Whenever possible, callers should set this flag because batched operation improves performance.</span></span>
  
<span data-ttu-id="cf8dd-146">後で値を追加するために、発信者が取得した行セットのいくつかの列を予約しておくと便利な場合がよくあります。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-146">It is often convenient for callers to reserve some columns in the retrieved row set for values to be added later.</span></span> <span data-ttu-id="cf8dd-147">呼び出し元は、 **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) を、 **SetColumns**に渡されたプロパティタグ配列内の目的の位置に配置することでこれを行います。その後、テーブルは**QueryRows**で取得されたすべての行のこれらの位置で**PR_NULL**を渡します。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-147">Callers do this by placing **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) at the desired positions in the property tag array passed to **SetColumns**; the table will then pass back **PR_NULL** at those positions in all rows retrieved with **QueryRows**.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="cf8dd-148">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="cf8dd-148">Notes to callers</span></span>

<span data-ttu-id="cf8dd-149">_lpPropTagArray_パラメーターのプロパティタグの配列を作成するときは、テーブルビューに表示される列の順序でタグを並べ替えます。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-149">When building the property tag array for the  _lpPropTagArray_ parameter, order the tags in the order that you want the columns to appear in the table view.</span></span> 
  
<span data-ttu-id="cf8dd-150">複数値のプロパティを指定するには、複数値のインスタンスのフラグ (MVI_FLAG 定数) を property タグに適用します。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-150">You can specify multivalued properties to be included in the column set by applying the multivalued instance flag, or MVI_FLAG constant, to the property tag.</span></span> <span data-ttu-id="cf8dd-151">このフラグを設定するには、プロパティの単一値バージョンのプロパティタグを、次のように MVI_PROP マクロのパラメーターとして渡します。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-151">Set this flag by passing the property tag for the single-valued version of the property as a parameter to the MVI_PROP macro as follows:</span></span>
  
```
MVI_PROP(ulPropTag)

```

<span data-ttu-id="cf8dd-152">MVI_PROP マクロは、プロパティの MVI_FLAG を設定し、タグを複数値のタグに変換します。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-152">The MVI_PROP macro will set MVI_FLAG for the property, turning the tag into a multivalued tag.</span></span> <span data-ttu-id="cf8dd-153">単一値のプロパティで誤って MVI_PROP を呼び出そうとすると、MAPI は呼び出しを無視し、property タグを変更しないでおきます。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-153">If you erroneously try to call MVI_PROP on a single-valued property, MAPI will ignore the call and leave the property tag unchanged.</span></span> 
  
<span data-ttu-id="cf8dd-154">プロパティタグの配列で**PR_NULL**に設定されているプロパティタグを、列セットにスペースを予約するように含めることができます。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-154">You can include property tags set to **PR_NULL** in the property tag array to reserve space in the column set.</span></span> <span data-ttu-id="cf8dd-155">スペースを予約すると、新しいプロパティタグ配列を割り当てずに、列セットを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-155">Reserving space allows you to add to a column set without having to allocate a new property tag array.</span></span> 
  
<span data-ttu-id="cf8dd-156">**SetColumns**の呼び出しによってテーブルの列の順序が変更され、これらの列の1つ以上が複数値プロパティを表している場合は、テーブル内の行数を増やすことができます。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-156">When your call to **SetColumns** causes a change to the order of a table's columns and one or more of these columns represent a multivalued property, it is possible for the number of rows in the table to increase.</span></span> <span data-ttu-id="cf8dd-157">この場合、テーブルのすべてのブックマークが破棄されます。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-157">If this occurs, all of the bookmarks for the table are discarded.</span></span> <span data-ttu-id="cf8dd-158">複数値列がテーブルにどのように影響するかの詳細については、「[複数値列の操作](working-with-multivalued-columns.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-158">For more information about how multivalued columns affect tables, see [Working with Multivalued Columns](working-with-multivalued-columns.md).</span></span>
  
<span data-ttu-id="cf8dd-159">既定では、列の設定は同期操作になります。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-159">Setting columns is by default a synchronous operation.</span></span> <span data-ttu-id="cf8dd-160">ただし、TBL_BATCH フラグを設定することによって、データが必要になるまで、テーブルが操作を延期できるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-160">However, you can allow the table to postpone the operation until such time as the data is needed by setting the TBL_BATCH flag.</span></span> <span data-ttu-id="cf8dd-161">このフラグを設定すると、パフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-161">Setting this flag can improve performance.</span></span> <span data-ttu-id="cf8dd-162">もう1つのフラグ TBL_ASYNC は、処理を非同期に行い、操作が完了する前に**SetColumns**を返すことができるようにします。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-162">Another flag, TBL_ASYNC, makes the operation asynchronous, allowing **SetColumns** to return before the operation is complete.</span></span> <span data-ttu-id="cf8dd-163">完了がいつ発生するかを確認するには、 [IMAPITable:: GetStatus](imapitable-getstatus.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-163">To determine when completion occurs, call [IMAPITable::GetStatus](imapitable-getstatus.md).</span></span>
  
<span data-ttu-id="cf8dd-164">**SetColumns**の呼び出しによって MAPI_E_BUSY が返された場合は、別の操作によって操作を開始できないことを示します。 [IMAPITable:: Abort](imapitable-abort.md)を呼び出して、進行中の操作を停止することができます。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-164">If a call to **SetColumns** returns MAPI_E_BUSY, indicating that another operation is preventing your operation from starting, you can call [IMAPITable::Abort](imapitable-abort.md) to stop the operation in progress.</span></span> 
  
<span data-ttu-id="cf8dd-165">[hraddcolumnsex](hraddcolumnsex.md)を呼び出して、列セットを変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-165">You can also call [HrAddColumnsEx](hraddcolumnsex.md) to change a column set.</span></span> <span data-ttu-id="cf8dd-166">**hraddcolumnsex**と**IMAPITable:: SetColumns**の違いは、 **hraddcolumnsex**の柔軟性が低いことです。列を追加することはできません。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-166">The difference between **HrAddColumnsEx** and **IMAPITable::SetColumns** is that **HrAddColumnsEx** is less flexible; it can only add columns.</span></span> <span data-ttu-id="cf8dd-167">追加の列は、列セットの先頭に配置されます。これらの列の下には、既存のすべての列が表示されます。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-167">The additional columns are placed at the beginning of the column set; all existing columns appear following these columns.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="cf8dd-168">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="cf8dd-168">MFCMAPI reference</span></span>

<span data-ttu-id="cf8dd-169">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-169">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="cf8dd-170">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="cf8dd-170">**File**</span></span>|<span data-ttu-id="cf8dd-171">**関数**</span><span class="sxs-lookup"><span data-stu-id="cf8dd-171">**Function**</span></span>|<span data-ttu-id="cf8dd-172">**コメント**</span><span class="sxs-lookup"><span data-stu-id="cf8dd-172">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cf8dd-173">ContentsTableListCtrl</span><span class="sxs-lookup"><span data-stu-id="cf8dd-173">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="cf8dd-174">CContentsTableListCtrl::D osetcolumns</span><span class="sxs-lookup"><span data-stu-id="cf8dd-174">CContentsTableListCtrl::DoSetColumns</span></span>  <br/> |<span data-ttu-id="cf8dd-175">mfcmapi は、 **IMAPITable:: SetColumns**メソッドを使用して、テーブルに必要な列を設定します。</span><span class="sxs-lookup"><span data-stu-id="cf8dd-175">MFCMAPI uses the **IMAPITable::SetColumns** method to set the desired columns for the table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cf8dd-176">関連項目</span><span class="sxs-lookup"><span data-stu-id="cf8dd-176">See also</span></span>



[<span data-ttu-id="cf8dd-177">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="cf8dd-177">HrQueryAllRows</span></span>](hrqueryallrows.md)
  
[<span data-ttu-id="cf8dd-178">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="cf8dd-178">IMAPITable::Abort</span></span>](imapitable-abort.md)
  
[<span data-ttu-id="cf8dd-179">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="cf8dd-179">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="cf8dd-180">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="cf8dd-180">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="cf8dd-181">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="cf8dd-181">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="cf8dd-182">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="cf8dd-182">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="cf8dd-183">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="cf8dd-183">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="cf8dd-184">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="cf8dd-184">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="cf8dd-185">SPropValue</span><span class="sxs-lookup"><span data-stu-id="cf8dd-185">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="cf8dd-186">SRowSet</span><span class="sxs-lookup"><span data-stu-id="cf8dd-186">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="cf8dd-187">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="cf8dd-187">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="cf8dd-188">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cf8dd-188">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


<span data-ttu-id="cf8dd-189">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="cf8dd-189">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

