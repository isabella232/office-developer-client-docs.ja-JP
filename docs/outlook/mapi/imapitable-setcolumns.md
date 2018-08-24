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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b6a27231c8dd2c0796b2dcba268de54fcd93e38d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587909"
---
# <a name="imapitablesetcolumns"></a><span data-ttu-id="43712-103">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="43712-103">IMAPITable::SetColumns</span></span>

  
  
<span data-ttu-id="43712-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="43712-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="43712-105">特定のプロパティと、テーブル内の列として表示するプロパティの順序を定義します。</span><span class="sxs-lookup"><span data-stu-id="43712-105">Defines the particular properties and order of properties to appear as columns in the table.</span></span>
  
```cpp
HRESULT SetColumns(
LPSPropTagArray lpPropTagArray,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="43712-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="43712-106">Parameters</span></span>

 <span data-ttu-id="43712-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="43712-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="43712-108">[in]テーブル内の列として含まれるプロパティを識別するプロパティ タグの配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="43712-108">[in] Pointer to an array of property tags identifying properties to be included as columns in the table.</span></span> <span data-ttu-id="43712-109">各タグのプロパティの型の部分は、以降の追加の領域を予約するのには有効な型または**PR_NULL**を設定できます。</span><span class="sxs-lookup"><span data-stu-id="43712-109">The property type portion of each tag can be set to a valid type or to **PR_NULL** to reserve space for subsequent additions.</span></span> <span data-ttu-id="43712-110">_LpPropTagArray_パラメーターを null に設定できません。すべてのテーブルには、少なくとも 1 つの列が必要です。</span><span class="sxs-lookup"><span data-stu-id="43712-110">The  _lpPropTagArray_ parameter cannot be set to NULL; every table must have at least one column.</span></span> 
    
 <span data-ttu-id="43712-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="43712-111">_ulFlags_</span></span>
  
> <span data-ttu-id="43712-112">[in]**SetColumns**、 **SetColumns**が通知で使用する場合などの非同期の呼び出しの戻り値を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="43712-112">[in] Bitmask of flags that controls the return of an asynchronous call to **SetColumns**, for example when **SetColumns** is used in notification.</span></span> <span data-ttu-id="43712-113">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="43712-113">The following flags can be set:</span></span> 
    
<span data-ttu-id="43712-114">TBL_ASYNC</span><span class="sxs-lookup"><span data-stu-id="43712-114">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="43712-115">列の設定操作の要求では、可能性のある操作が完全に終了する前に取得する**SetColumns**を非同期的に原因を実行します。</span><span class="sxs-lookup"><span data-stu-id="43712-115">Requests that the column setting operation be performed asynchronously causing **SetColumns** to potentially return before the operation has fully completed.</span></span> 
    
<span data-ttu-id="43712-116">TBL_BATCH</span><span class="sxs-lookup"><span data-stu-id="43712-116">TBL_BATCH</span></span> 
  
> <span data-ttu-id="43712-117">データが実際に必要になるまで、列の設定操作を延期するテーブルを許可します。</span><span class="sxs-lookup"><span data-stu-id="43712-117">Permits the table to postpone the column setting operation until the data is actually required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="43712-118">�߂�l</span><span class="sxs-lookup"><span data-stu-id="43712-118">Return value</span></span>

<span data-ttu-id="43712-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="43712-119">S_OK</span></span> 
  
> <span data-ttu-id="43712-120">列の設定の操作が正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="43712-120">The column setting operation was successful.</span></span>
    
<span data-ttu-id="43712-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="43712-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="43712-122">別進行中に、列の操作の開始を設定しないようにします。</span><span class="sxs-lookup"><span data-stu-id="43712-122">Another operation is in progress that prevents the column setting operation from starting.</span></span> <span data-ttu-id="43712-123">実行中の操作を完了できるか、それを停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="43712-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="43712-124">注釈</span><span class="sxs-lookup"><span data-stu-id="43712-124">Remarks</span></span>

<span data-ttu-id="43712-125">テーブルの列のセットは、テーブル内の行の列を構成するプロパティのグループです。</span><span class="sxs-lookup"><span data-stu-id="43712-125">The column set of a table is the group of properties that make up the columns for the rows in the table.</span></span> <span data-ttu-id="43712-126">テーブルの種類ごとに設定する既定の列があります。</span><span class="sxs-lookup"><span data-stu-id="43712-126">There is a default column set for each type of table.</span></span> <span data-ttu-id="43712-127">自動的にテーブルの作成者を含むプロパティの既定の列セットが構成されています。</span><span class="sxs-lookup"><span data-stu-id="43712-127">The default column set is made up of the properties that the table implementer automatically includes.</span></span> <span data-ttu-id="43712-128">テーブルのユーザーには、この既定値は、 **IMAPITable::SetColumns**メソッドを呼び出すことによって設定を変更できます。</span><span class="sxs-lookup"><span data-stu-id="43712-128">Table users can alter this default set by calling the **IMAPITable::SetColumns** method.</span></span> <span data-ttu-id="43712-129">その他の列がテーブルの作成者はこれらの列を削除することや、列の順序を変更することをサポートしている場合は、設定の既定値に追加することを要求することができます。</span><span class="sxs-lookup"><span data-stu-id="43712-129">They can request that other columns be added to the default set if the table implementer supports them that columns be removed, or that the order of columns be changed.</span></span> <span data-ttu-id="43712-130">**SetColumns**では、それぞれの行と行にこれらの列の順序で返される列を指定します。</span><span class="sxs-lookup"><span data-stu-id="43712-130">**SetColumns** specifies the columns that are returned with each row and the order of these columns within the row.</span></span> 
  
<span data-ttu-id="43712-131">**SetColumns**操作の成功は、テーブルのデータを取得するために後続の呼び出しを実行した後にのみ明らかです。</span><span class="sxs-lookup"><span data-stu-id="43712-131">The success of the **SetColumns** operation is apparent only after a subsequent call has been made to retrieve the data of the table.</span></span> <span data-ttu-id="43712-132">エラーが報告されることですし。</span><span class="sxs-lookup"><span data-stu-id="43712-132">It is then that any errors are reported.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="43712-133">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="43712-133">Notes to implementers</span></span>

<span data-ttu-id="43712-134">一部のプロバイダーは、テーブル ビューの使用可能な列の一部であるテーブルの列のみを注文する**SetColumns**呼び出しを許可します。</span><span class="sxs-lookup"><span data-stu-id="43712-134">Some providers allow a **SetColumns** call to order only table columns that are part of the available columns for a table view.</span></span> <span data-ttu-id="43712-135">他のプロバイダーでは、 **SetColumns**呼び出し元の列のセットではなくプロパティが含まれているものも含めて、すべてのテーブルの列の順序を使用できます。</span><span class="sxs-lookup"><span data-stu-id="43712-135">Other providers allow a **SetColumns** call to order all table columns, including those containing properties not in the original column set.</span></span> 
  
<span data-ttu-id="43712-136">非同期操作の TBL_BATCH を設定すると、プロバイダーは PT_ERROR のプロパティの種類とサポートされていない列の null プロパティの値を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="43712-136">When TBL_BATCH is set for asynchronous operations, providers should return a property type of PT_ERROR and a property value of NULL for columns that are not supported.</span></span>
  
<span data-ttu-id="43712-137">TBL_ASYNC フラグを要求する操作を非同期にすることに応答する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="43712-137">You do not need to respond to the TBL_ASYNC flag requesting that the operation be asynchronous.</span></span> <span data-ttu-id="43712-138">非同期の列のセットの定義をサポートしていない場合は、同期的に操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="43712-138">If you do not support asynchronous column set definition, perform the operation synchronously.</span></span> <span data-ttu-id="43712-139">TBL_ASYNC のフラグは、別の非同期の操作をサポートできる場合、操作は、進行中、MAPI_E_BUSY の戻り値では。</span><span class="sxs-lookup"><span data-stu-id="43712-139">If you can support the TBL_ASYNC flag and another asynchronous operation is still in progress, return MAPI_E_BUSY.</span></span> <span data-ttu-id="43712-140">それ以外の場合、すべてのプロパティ タグ配列に含まれているプロパティをサポートするかどうかに関係なく S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="43712-140">Otherwise, return S_OK regardless of whether or not you support all of the properties included in the property tag array.</span></span> <span data-ttu-id="43712-141">**スプーラー**などのデータを取得する**IMAPITable**メソッドからエラーがサポートされていないプロパティの結果が返されます。</span><span class="sxs-lookup"><span data-stu-id="43712-141">Errors resulting from unsupported properties should be returned from **IMAPITable** methods that retrieve data, such as **QueryRows**.</span></span> 
  
<span data-ttu-id="43712-142">**制限**を呼び出すことによってビューから非表示になっているテーブルの行への通知は生成されません。</span><span class="sxs-lookup"><span data-stu-id="43712-142">Do not generate notifications for table rows that are hidden from view by calls to **Restrict**.</span></span> 
  
<span data-ttu-id="43712-143">指定されたテーブルの通知、 [TABLE_NOTIFICATION](table_notification.md)構造体の**行**メンバーのプロパティの順序と順序を送信するときに最新の**SetColumns**呼び出し必要があります、通知を要求する時と同じ送信されました。</span><span class="sxs-lookup"><span data-stu-id="43712-143">When sending table notifications, the order of the properties in the **row** member of the [TABLE_NOTIFICATION](table_notification.md) structure and the order specified by the most recent **SetColumns** call must be the same as of the time that the notification request was sent.</span></span> 
  
<span data-ttu-id="43712-144">別のフラグ、TBL_BATCH では、しばらくの間操作の結果を評価することができますテーブル実装側で遅延を指定する呼び出し元を許可します。</span><span class="sxs-lookup"><span data-stu-id="43712-144">Another flag, TBL_BATCH, allows callers to specify that the table implementer can defer evaluating the results of the operation until a later time.</span></span> <span data-ttu-id="43712-145">可能な限り、呼び出し元は、バッチ操作のパフォーマンスが向上するためにこのフラグを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="43712-145">Whenever possible, callers should set this flag because batched operation improves performance.</span></span>
  
<span data-ttu-id="43712-146">呼び出し元が後で追加される値を取得した行セットの一部のカラムを予約する場合に便利なことがよくあります。</span><span class="sxs-lookup"><span data-stu-id="43712-146">It is often convenient for callers to reserve some columns in the retrieved row set for values to be added later.</span></span> <span data-ttu-id="43712-147">呼び出し元が**SetColumns**; に渡されるプロパティ タグ配列で、目的の位置に**PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) を配置することによってこれを行うテーブルは、**スプーラー**を返しますこれらのすべての行の位置に**PR_NULL**を取得し、されます。</span><span class="sxs-lookup"><span data-stu-id="43712-147">Callers do this by placing **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) at the desired positions in the property tag array passed to **SetColumns**; the table will then pass back **PR_NULL** at those positions in all rows retrieved with **QueryRows**.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="43712-148">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="43712-148">Notes to callers</span></span>

<span data-ttu-id="43712-149">_LpPropTagArray_パラメーターのプロパティ タグ配列を作成するときは、テーブル ビューに表示する列を希望する順序で、タグを注文します。</span><span class="sxs-lookup"><span data-stu-id="43712-149">When building the property tag array for the  _lpPropTagArray_ parameter, order the tags in the order that you want the columns to appear in the table view.</span></span> 
  
<span data-ttu-id="43712-150">プロパティ タグに複数値を持つインスタンスのフラグ、または MVI_FLAG の定数を適用することで設定する列に含まれる複数値を持つプロパティを指定できます。</span><span class="sxs-lookup"><span data-stu-id="43712-150">You can specify multivalued properties to be included in the column set by applying the multivalued instance flag, or MVI_FLAG constant, to the property tag.</span></span> <span data-ttu-id="43712-151">単一値プロパティのバージョンのプロパティ タグ パラメーターとして渡し、MVI_PROP マクロを次のようにこのフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="43712-151">Set this flag by passing the property tag for the single-valued version of the property as a parameter to the MVI_PROP macro as follows:</span></span>
  
```
MVI_PROP(ulPropTag)

```

<span data-ttu-id="43712-152">MVI_PROP マクロは、プロパティは、複数値を持つタグにタグを有効にする MVI_FLAG を設定します。</span><span class="sxs-lookup"><span data-stu-id="43712-152">The MVI_PROP macro will set MVI_FLAG for the property, turning the tag into a multivalued tag.</span></span> <span data-ttu-id="43712-153">誤っては、単一値プロパティに MVI_PROP を呼び出すと、MAPI 呼び出しを無視して、変更されていないプロパティ タグのままにします。</span><span class="sxs-lookup"><span data-stu-id="43712-153">If you erroneously try to call MVI_PROP on a single-valued property, MAPI will ignore the call and leave the property tag unchanged.</span></span> 
  
<span data-ttu-id="43712-154">プロパティ タグを**PR_NULL**に設定すると、列のセット内の領域を予約するプロパティ タグ配列を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="43712-154">You can include property tags set to **PR_NULL** in the property tag array to reserve space in the column set.</span></span> <span data-ttu-id="43712-155">領域を予約する、新しいプロパティ タグ配列を割り当てることがなく設定されている列を追加できます。</span><span class="sxs-lookup"><span data-stu-id="43712-155">Reserving space allows you to add to a column set without having to allocate a new property tag array.</span></span> 
  
<span data-ttu-id="43712-156">**SetColumns**を呼び出すは、テーブルの列の順序変更し、1 つ以上のこれらの列は、複数値を持つプロパティを表す、増加するテーブル内の行の数のことができます。</span><span class="sxs-lookup"><span data-stu-id="43712-156">When your call to **SetColumns** causes a change to the order of a table's columns and one or more of these columns represent a multivalued property, it is possible for the number of rows in the table to increase.</span></span> <span data-ttu-id="43712-157">このような場合は、テーブルのブックマークをすべて破棄されます。</span><span class="sxs-lookup"><span data-stu-id="43712-157">If this occurs, all of the bookmarks for the table are discarded.</span></span> <span data-ttu-id="43712-158">方法の詳細については、複数値を持つ列はテーブルに影響を与える、[複数値を持つ列の使用](working-with-multivalued-columns.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="43712-158">For more information about how multivalued columns affect tables, see [Working with Multivalued Columns](working-with-multivalued-columns.md).</span></span>
  
<span data-ttu-id="43712-159">列の設定は既定では同期操作です。</span><span class="sxs-lookup"><span data-stu-id="43712-159">Setting columns is by default a synchronous operation.</span></span> <span data-ttu-id="43712-160">ただし、TBL_BATCH フラグを設定することによってデータが必要になるまで、操作を延期するテーブルを許可できます。</span><span class="sxs-lookup"><span data-stu-id="43712-160">However, you can allow the table to postpone the operation until such time as the data is needed by setting the TBL_BATCH flag.</span></span> <span data-ttu-id="43712-161">このフラグを設定すると、パフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="43712-161">Setting this flag can improve performance.</span></span> <span data-ttu-id="43712-162">別のフラグ、TBL_ASYNC によって操作が非同期操作が完了する前に戻るには、 **SetColumns**を許可します。</span><span class="sxs-lookup"><span data-stu-id="43712-162">Another flag, TBL_ASYNC, makes the operation asynchronous, allowing **SetColumns** to return before the operation is complete.</span></span> <span data-ttu-id="43712-163">完了が発生した場合を確認するのには、 [IMAPITable::GetStatus](imapitable-getstatus.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="43712-163">To determine when completion occurs, call [IMAPITable::GetStatus](imapitable-getstatus.md).</span></span>
  
<span data-ttu-id="43712-164">**SetColumns**呼び出しが別の操作が、操作の開始を拒否されていることを示す、MAPI_E_BUSY を返す場合は、実行中の操作を停止するのには[IMAPITable::Abort](imapitable-abort.md)を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="43712-164">If a call to **SetColumns** returns MAPI_E_BUSY, indicating that another operation is preventing your operation from starting, you can call [IMAPITable::Abort](imapitable-abort.md) to stop the operation in progress.</span></span> 
  
<span data-ttu-id="43712-165">列セットを変更するのには[HrAddColumnsEx](hraddcolumnsex.md)を呼び出すこともできます。</span><span class="sxs-lookup"><span data-stu-id="43712-165">You can also call [HrAddColumnsEx](hraddcolumnsex.md) to change a column set.</span></span> <span data-ttu-id="43712-166">**HrAddColumnsEx**と**IMAPITable::SetColumns**の違いは、 **HrAddColumnsEx**が少ない柔軟性があります。列のみ追加できます。</span><span class="sxs-lookup"><span data-stu-id="43712-166">The difference between **HrAddColumnsEx** and **IMAPITable::SetColumns** is that **HrAddColumnsEx** is less flexible; it can only add columns.</span></span> <span data-ttu-id="43712-167">追加の列は列セットの先頭に配置されます。これらの列の後にすべての既存の列が表示されます。</span><span class="sxs-lookup"><span data-stu-id="43712-167">The additional columns are placed at the beginning of the column set; all existing columns appear following these columns.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="43712-168">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="43712-168">MFCMAPI reference</span></span>

<span data-ttu-id="43712-169">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="43712-169">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="43712-170">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="43712-170">**File**</span></span>|<span data-ttu-id="43712-171">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="43712-171">**Function**</span></span>|<span data-ttu-id="43712-172">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="43712-172">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="43712-173">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="43712-173">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="43712-174">CContentsTableListCtrl::DoSetColumns</span><span class="sxs-lookup"><span data-stu-id="43712-174">CContentsTableListCtrl::DoSetColumns</span></span>  <br/> |<span data-ttu-id="43712-175">MFCMAPI では、 **IMAPITable::SetColumns**メソッドを使用して、目的のテーブルの列を設定します。</span><span class="sxs-lookup"><span data-stu-id="43712-175">MFCMAPI uses the **IMAPITable::SetColumns** method to set the desired columns for the table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="43712-176">関連項目</span><span class="sxs-lookup"><span data-stu-id="43712-176">See also</span></span>



[<span data-ttu-id="43712-177">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="43712-177">HrQueryAllRows</span></span>](hrqueryallrows.md)
  
[<span data-ttu-id="43712-178">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="43712-178">IMAPITable::Abort</span></span>](imapitable-abort.md)
  
[<span data-ttu-id="43712-179">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="43712-179">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="43712-180">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="43712-180">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="43712-181">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="43712-181">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="43712-182">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="43712-182">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="43712-183">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="43712-183">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="43712-184">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="43712-184">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="43712-185">SPropValue</span><span class="sxs-lookup"><span data-stu-id="43712-185">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="43712-186">SRowSet</span><span class="sxs-lookup"><span data-stu-id="43712-186">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="43712-187">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="43712-187">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="43712-188">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="43712-188">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


<span data-ttu-id="43712-189">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="43712-189">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

