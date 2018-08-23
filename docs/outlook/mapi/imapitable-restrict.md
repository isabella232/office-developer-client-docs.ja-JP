---
title: IMAPITableRestrict
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Restrict
api_type:
- COM
ms.assetid: a5bfc190-b58f-44c3-893c-8727df14ee58
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 924715f26e104739f2e60762511221da5facd5a5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578326"
---
# <a name="imapitablerestrict"></a><span data-ttu-id="5a42f-103">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="5a42f-103">IMAPITable::Restrict</span></span>

  
  
<span data-ttu-id="5a42f-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a42f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a42f-105">指定した条件に一致する行のみに設定した行を減らすこと、テーブルにフィルターを適用します。</span><span class="sxs-lookup"><span data-stu-id="5a42f-105">Applies a filter to a table, reducing the row set to only those rows matching the specified criteria.</span></span>
  
```cpp
HRESULT Restrict(
LPSRestriction lpRestriction,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="5a42f-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5a42f-106">Parameters</span></span>

 <span data-ttu-id="5a42f-107">_lpRestriction_</span><span class="sxs-lookup"><span data-stu-id="5a42f-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="5a42f-108">[in][SRestriction](srestriction.md)フィルターの条件を定義する構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5a42f-108">[in] Pointer to an [SRestriction](srestriction.md) structure defining the conditions of the filter.</span></span> <span data-ttu-id="5a42f-109">_LpRestriction_パラメーターに NULL を渡すと、現在のフィルターが削除されます。</span><span class="sxs-lookup"><span data-stu-id="5a42f-109">Passing NULL in the  _lpRestriction_ parameter removes the current filter.</span></span> 
    
 <span data-ttu-id="5a42f-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5a42f-110">_ulFlags_</span></span>
  
> <span data-ttu-id="5a42f-111">[in]制限操作のタイミングを制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="5a42f-111">[in] Bitmask of flags that controls the timing of the restriction operation.</span></span> <span data-ttu-id="5a42f-112">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="5a42f-112">The following flags can be set:</span></span>
    
<span data-ttu-id="5a42f-113">TBL_ASYNC</span><span class="sxs-lookup"><span data-stu-id="5a42f-113">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="5a42f-114">操作を非同期に開始し、操作が完了する前に返します。</span><span class="sxs-lookup"><span data-stu-id="5a42f-114">Starts the operation asynchronously and returns before the operation completes.</span></span>
    
<span data-ttu-id="5a42f-115">TBL_BATCH</span><span class="sxs-lookup"><span data-stu-id="5a42f-115">TBL_BATCH</span></span> 
  
> <span data-ttu-id="5a42f-116">テーブル内のデータが必要になるまでは、フィルターの評価を延期します。</span><span class="sxs-lookup"><span data-stu-id="5a42f-116">Defers evaluation of the filter until the data in the table is required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5a42f-117">�߂�l</span><span class="sxs-lookup"><span data-stu-id="5a42f-117">Return value</span></span>

<span data-ttu-id="5a42f-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="5a42f-118">S_OK</span></span> 
  
> <span data-ttu-id="5a42f-119">フィルターが正常に適用されました。</span><span class="sxs-lookup"><span data-stu-id="5a42f-119">The filter was successfully applied.</span></span>
    
<span data-ttu-id="5a42f-120">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="5a42f-120">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="5a42f-121">別の操作では、制限操作の開始を防止する処理中です。</span><span class="sxs-lookup"><span data-stu-id="5a42f-121">Another operation is in progress that prevents the restriction operation from starting.</span></span> <span data-ttu-id="5a42f-122">実行中の操作を完了できるか、それを停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a42f-122">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="5a42f-123">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="5a42f-123">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="5a42f-124">テーブルは、 _lpRestriction_パラメーターで指定された特定のフィルターが複雑すぎるために、操作を実行できません。</span><span class="sxs-lookup"><span data-stu-id="5a42f-124">The table cannot perform the operation because the particular filter pointed to by the  _lpRestriction_ parameter is too complicated.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5a42f-125">注釈</span><span class="sxs-lookup"><span data-stu-id="5a42f-125">Remarks</span></span>

<span data-ttu-id="5a42f-126">**IMAPITable::Restrict**メソッドは、制限、またはテーブル上のフィルターを設定します。</span><span class="sxs-lookup"><span data-stu-id="5a42f-126">The **IMAPITable::Restrict** method establishes a restriction, or filter, on a table.</span></span> <span data-ttu-id="5a42f-127">以前の制限がある場合は、それは破棄され、新しいものが適用されます。</span><span class="sxs-lookup"><span data-stu-id="5a42f-127">If there is a previous restriction, it is discarded and the new one applied.</span></span> <span data-ttu-id="5a42f-128">制限を適用するのには影響しません、テーブルの基になるデータだけで、制限を満たすデータを含む行を取得できる行数を制限することによってビューを変更します。</span><span class="sxs-lookup"><span data-stu-id="5a42f-128">Applying a restriction has no affect on the underlying data of a table; it simply alters the view by limiting the rows that can be retrieved to rows containing data that satisfy the restriction.</span></span> 
  
<span data-ttu-id="5a42f-129">さまざまな種類の制限、構造が異なると、それぞれについて説明します。</span><span class="sxs-lookup"><span data-stu-id="5a42f-129">There are several different types of restrictions, each described with a different structure.</span></span> <span data-ttu-id="5a42f-130">[SRestriction](srestriction.md)構造には、2 つのメンバーが含まれています: を制限し、そのタイプに該当する特定の構造の種類を示す値です。</span><span class="sxs-lookup"><span data-stu-id="5a42f-130">The [SRestriction](srestriction.md) structure contains two members: a value that indicates the type of restriction and the specific structure applicable for that type.</span></span> 
  
<span data-ttu-id="5a42f-131">ビューから非表示に**制限**を呼び出すことによってテーブルの行の通知が生成されることはありません。</span><span class="sxs-lookup"><span data-stu-id="5a42f-131">Notifications for table rows that are hidden from view by calls to **Restrict** are never generated.</span></span> 
  
<span data-ttu-id="5a42f-132">複数値を持つプロパティのプロパティの制限は、単一値を持つプロパティに対する制限と同じように動作します。</span><span class="sxs-lookup"><span data-stu-id="5a42f-132">A property restriction on a multivalued property works like a restriction on a single-valued property.</span></span> <span data-ttu-id="5a42f-133">プロパティ制限で使用する複数値を持つプロパティには、MVI_FLAG フラグが設定されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a42f-133">A multivalued property to be used in a property restriction must have the MVI_FLAG flag set.</span></span> <span data-ttu-id="5a42f-134">このフラグが設定されていない場合、は、完全に順序付けられた組として扱われます。</span><span class="sxs-lookup"><span data-stu-id="5a42f-134">If it doesn't have this flag set, it is treated as a totally ordered tuple.</span></span> <span data-ttu-id="5a42f-135">2 つの複数値を持つ列の比較では、最初の非等値の列の関係をレポートの列の要素を比較します。</span><span class="sxs-lookup"><span data-stu-id="5a42f-135">A comparison of two multivalued columns compares the column elements in order, reporting the relation of the columns at the first inequality.</span></span> <span data-ttu-id="5a42f-136">比較の列に同じ順序で同じ値が含まれている場合にのみ、等しいかどうかが返されます。</span><span class="sxs-lookup"><span data-stu-id="5a42f-136">Equality is returned only if the columns compared contain the same values in the same order.</span></span> <span data-ttu-id="5a42f-137">もう一方よりも少ない値を 1 つの列には、報告された関係が他の値に null 値の</span><span class="sxs-lookup"><span data-stu-id="5a42f-137">If one column has fewer values than the other, the reported relation is that of a null value to the other value.</span></span>
  
<span data-ttu-id="5a42f-138">制限の詳細については、[制限の詳細](about-restrictions.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5a42f-138">For more information about restrictions, see [About Restrictions](about-restrictions.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="5a42f-139">サーバー上のデータを検索する動的なクエリを作成する場合は、 **Restrict**メソッドおよび**スプーラー**メソッドを共に使用するのではなく**FindRow**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="5a42f-139">If you create dynamic queries to search for data on the server, use the **FindRow** method instead of using the **Restrict** method and the **QueryRows** method together.</span></span> <span data-ttu-id="5a42f-140">**Restrict**メソッドでは、すべてのメッセージでは、ベースのフォルダーを追加または変更を評価するために使用されるキャッシュされたビューを作成します。</span><span class="sxs-lookup"><span data-stu-id="5a42f-140">The **Restrict** method creates a cached view that is used to evaluate all messages added to or modified in the base folder.</span></span> <span data-ttu-id="5a42f-141">クライアント アプリケーションは、動的クエリごとに、 **Restrict**メソッドを使用する場合、キャッシュされたビューはクエリごとに作成されます。</span><span class="sxs-lookup"><span data-stu-id="5a42f-141">If a client application uses the **Restrict** method for each dynamic query, a cached view will be created for each query.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5a42f-142">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="5a42f-142">Notes to callers</span></span>

<span data-ttu-id="5a42f-143">新規に作成することがなく、現在の制限を破棄するには、 _lpRestriction_に NULL を渡します。</span><span class="sxs-lookup"><span data-stu-id="5a42f-143">To discard the current restriction without creating a new one, pass NULL in  _lpRestriction_.</span></span>
  
<span data-ttu-id="5a42f-144">別のテーブルの非同期呼び出しが実行中である場合、MAPI_E_BUSY に戻るには、**制限**の原因で呼び出すことができます、呼び出しを停止するのには[IMAPITable::Abort](imapitable-abort.md) 。</span><span class="sxs-lookup"><span data-stu-id="5a42f-144">If another asynchronous table call is in progress, causing **Restrict** to return MAPI_E_BUSY, you can call [IMAPITable::Abort](imapitable-abort.md) to stop the call.</span></span> 
  
 <span data-ttu-id="5a42f-145">フラグのいずれかを設定しない限り、**制限**は同期的に動作します。</span><span class="sxs-lookup"><span data-stu-id="5a42f-145">**Restrict** operates synchronously unless you set one of the flags.</span></span> <span data-ttu-id="5a42f-146">TBL_BATCH フラグを設定する場合、**制限**は、データを要求する場合を除き、制限の評価を延期します。</span><span class="sxs-lookup"><span data-stu-id="5a42f-146">If you set the TBL_BATCH flag, **Restrict** postpones the evaluation of the restriction unless you request the data.</span></span> <span data-ttu-id="5a42f-147">TBL_ASYNC フラグが設定されている場合**だけに制限する**機能、非同期的に操作が完了する前に返す可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5a42f-147">If the TBL_ASYNC flag is set, **Restrict**operates asynchronously, potentially returning before the completion of the operation.</span></span>
  
<span data-ttu-id="5a42f-148">**制限**への呼び出しが作成され、テーブルの先頭に BOOKMARK_CURRENT、現在のカーソル位置を設定すると、テーブルのすべてのブックマークは破棄されます。</span><span class="sxs-lookup"><span data-stu-id="5a42f-148">All bookmarks for a table are discarded when a call to **Restrict** is made, and BOOKMARK_CURRENT, the current cursor position, is set to the beginning of the table.</span></span> 
  
<span data-ttu-id="5a42f-149">テーブルの列のセットに含まれていないプロパティのプロパティの制限を適用しようとした場合、結果は定義されていません。</span><span class="sxs-lookup"><span data-stu-id="5a42f-149">If you attempt to impose a property restriction on a property that is not in the table's column set, the results are undefined.</span></span> <span data-ttu-id="5a42f-150">使用しているテーブルのプロパティがサポートされているかどうかには、結合のプロパティ制限で、制限が存在します。</span><span class="sxs-lookup"><span data-stu-id="5a42f-150">Whenever you are unsure as to whether a property is supported in a table, combine the property restriction with an exists restriction.</span></span> <span data-ttu-id="5a42f-151">プロパティの制限を適用する前にプロパティが存在する制限の確認が存在します。</span><span class="sxs-lookup"><span data-stu-id="5a42f-151">The exists restriction checks for the existence of the property before attempting to impose the property restriction.</span></span> 
  
<span data-ttu-id="5a42f-152">制限があるため、テーブルのフィルターされた行をテーブル通知が受信されないようにします。</span><span class="sxs-lookup"><span data-stu-id="5a42f-152">Do not expect to receive a table notification on a row that has been filtered from a table due to a restriction.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5a42f-153">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="5a42f-153">MFCMAPI reference</span></span>

<span data-ttu-id="5a42f-154">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="5a42f-154">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5a42f-155">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="5a42f-155">**File**</span></span>|<span data-ttu-id="5a42f-156">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="5a42f-156">**Function**</span></span>|<span data-ttu-id="5a42f-157">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="5a42f-157">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5a42f-158">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="5a42f-158">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="5a42f-159">CContentsTableListCtrl::ApplyRestriction</span><span class="sxs-lookup"><span data-stu-id="5a42f-159">CContentsTableListCtrl::ApplyRestriction</span></span>  <br/> |<span data-ttu-id="5a42f-160">MFCMAPI では、 **IMAPITable::Restrict**メソッドを使用して、テーブル上の制限を設定します。</span><span class="sxs-lookup"><span data-stu-id="5a42f-160">MFCMAPI uses the **IMAPITable::Restrict** method to set a restriction on a table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5a42f-161">関連項目</span><span class="sxs-lookup"><span data-stu-id="5a42f-161">See also</span></span>



[<span data-ttu-id="5a42f-162">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="5a42f-162">IMAPITable::Abort</span></span>](imapitable-abort.md)
  
[<span data-ttu-id="5a42f-163">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="5a42f-163">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="5a42f-164">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="5a42f-164">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="5a42f-165">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="5a42f-165">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="5a42f-166">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="5a42f-166">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="5a42f-167">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5a42f-167">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


<span data-ttu-id="5a42f-168">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="5a42f-168">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

