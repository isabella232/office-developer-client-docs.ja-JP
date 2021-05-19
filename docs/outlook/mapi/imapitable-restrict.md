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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6cca6bc12fa6f100885b7bf705d79fa24a2e2f91
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414621"
---
# <a name="imapitablerestrict"></a><span data-ttu-id="cf5b0-103">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="cf5b0-103">IMAPITable::Restrict</span></span>

  
  
<span data-ttu-id="cf5b0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf5b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf5b0-105">テーブルにフィルターを適用し、指定した条件に一致する行にのみ行セットを減らします。</span><span class="sxs-lookup"><span data-stu-id="cf5b0-105">Applies a filter to a table, reducing the row set to only those rows matching the specified criteria.</span></span>
  
```cpp
HRESULT Restrict(
LPSRestriction lpRestriction,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="cf5b0-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cf5b0-106">Parameters</span></span>

 <span data-ttu-id="cf5b0-107">_lpRestriction_</span><span class="sxs-lookup"><span data-stu-id="cf5b0-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="cf5b0-108">[in]フィルターの [条件を定義する SRestriction](srestriction.md) 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="cf5b0-108">[in] Pointer to an [SRestriction](srestriction.md) structure defining the conditions of the filter.</span></span> <span data-ttu-id="cf5b0-109">_lpRestriction_ パラメーターに NULL を渡すと、現在のフィルターが削除されます。</span><span class="sxs-lookup"><span data-stu-id="cf5b0-109">Passing NULL in the  _lpRestriction_ parameter removes the current filter.</span></span> 
    
 <span data-ttu-id="cf5b0-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cf5b0-110">_ulFlags_</span></span>
  
> <span data-ttu-id="cf5b0-111">[in]制限操作のタイミングを制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="cf5b0-111">[in] Bitmask of flags that controls the timing of the restriction operation.</span></span> <span data-ttu-id="cf5b0-112">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="cf5b0-112">The following flags can be set:</span></span>
    
<span data-ttu-id="cf5b0-113">TBL_ASYNC</span><span class="sxs-lookup"><span data-stu-id="cf5b0-113">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="cf5b0-114">操作を非同期的に開始し、操作が完了する前に返します。</span><span class="sxs-lookup"><span data-stu-id="cf5b0-114">Starts the operation asynchronously and returns before the operation completes.</span></span>
    
<span data-ttu-id="cf5b0-115">TBL_BATCH</span><span class="sxs-lookup"><span data-stu-id="cf5b0-115">TBL_BATCH</span></span> 
  
> <span data-ttu-id="cf5b0-116">テーブル内のデータが必要になるまで、フィルターの評価を延期します。</span><span class="sxs-lookup"><span data-stu-id="cf5b0-116">Defers evaluation of the filter until the data in the table is required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cf5b0-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="cf5b0-117">Return value</span></span>

<span data-ttu-id="cf5b0-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="cf5b0-118">S_OK</span></span> 
  
> <span data-ttu-id="cf5b0-119">フィルターが正常に適用されました。</span><span class="sxs-lookup"><span data-stu-id="cf5b0-119">The filter was successfully applied.</span></span>
    
<span data-ttu-id="cf5b0-120">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="cf5b0-120">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="cf5b0-121">制限操作の開始を妨げる別の操作が進行中です。</span><span class="sxs-lookup"><span data-stu-id="cf5b0-121">Another operation is in progress that prevents the restriction operation from starting.</span></span> <span data-ttu-id="cf5b0-122">進行中の操作の完了を許可するか、停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf5b0-122">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="cf5b0-123">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="cf5b0-123">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="cf5b0-124">_lpRestriction_ パラメーターが指す特定のフィルターが複雑すぎるため、テーブルで操作を実行できません。</span><span class="sxs-lookup"><span data-stu-id="cf5b0-124">The table cannot perform the operation because the particular filter pointed to by the  _lpRestriction_ parameter is too complicated.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="cf5b0-125">注釈</span><span class="sxs-lookup"><span data-stu-id="cf5b0-125">Remarks</span></span>

<span data-ttu-id="cf5b0-126">**IMAPITable::Restrict** メソッドは、テーブルに制限 (フィルター) を設定します。</span><span class="sxs-lookup"><span data-stu-id="cf5b0-126">The **IMAPITable::Restrict** method establishes a restriction, or filter, on a table.</span></span> <span data-ttu-id="cf5b0-127">以前の制限がある場合は破棄され、新しい制限が適用されます。</span><span class="sxs-lookup"><span data-stu-id="cf5b0-127">If there is a previous restriction, it is discarded and the new one applied.</span></span> <span data-ttu-id="cf5b0-128">制限を適用すると、テーブルの基になるデータに影響はありません。取得できる行を、制限を満たすデータを含む行に制限することで、ビューを変更します。</span><span class="sxs-lookup"><span data-stu-id="cf5b0-128">Applying a restriction has no affect on the underlying data of a table; it simply alters the view by limiting the rows that can be retrieved to rows containing data that satisfy the restriction.</span></span> 
  
<span data-ttu-id="cf5b0-129">制限にはいくつかの種類があります。それぞれ異なる構造で説明されています。</span><span class="sxs-lookup"><span data-stu-id="cf5b0-129">There are several different types of restrictions, each described with a different structure.</span></span> <span data-ttu-id="cf5b0-130">[SRestriction 構造体には](srestriction.md)、制限の種類と、その型に適用可能な特定の構造を示す値の 2 つのメンバーが含まれる。</span><span class="sxs-lookup"><span data-stu-id="cf5b0-130">The [SRestriction](srestriction.md) structure contains two members: a value that indicates the type of restriction and the specific structure applicable for that type.</span></span> 
  
<span data-ttu-id="cf5b0-131">Restrict の呼び出しによって表示から非表示にされたテーブル行 **の通知** は生成されません。</span><span class="sxs-lookup"><span data-stu-id="cf5b0-131">Notifications for table rows that are hidden from view by calls to **Restrict** are never generated.</span></span> 
  
<span data-ttu-id="cf5b0-132">複数値プロパティのプロパティ制限は、単一値プロパティの制限と同様に機能します。</span><span class="sxs-lookup"><span data-stu-id="cf5b0-132">A property restriction on a multivalued property works like a restriction on a single-valued property.</span></span> <span data-ttu-id="cf5b0-133">プロパティ制限で使用する複数値プロパティには、プロパティ フラグが設定MVI_FLAG必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf5b0-133">A multivalued property to be used in a property restriction must have the MVI_FLAG flag set.</span></span> <span data-ttu-id="cf5b0-134">このフラグを設定しない場合は、完全に順序付けられたタプルとして扱います。</span><span class="sxs-lookup"><span data-stu-id="cf5b0-134">If it doesn't have this flag set, it is treated as a totally ordered tuple.</span></span> <span data-ttu-id="cf5b0-135">2 つの複数値列の比較では、列要素を順番に比較し、列の関係を最初の不等式で報告します。</span><span class="sxs-lookup"><span data-stu-id="cf5b0-135">A comparison of two multivalued columns compares the column elements in order, reporting the relation of the columns at the first inequality.</span></span> <span data-ttu-id="cf5b0-136">等号は、比較される列に同じ値が同じ順序で含まれている場合にのみ返されます。</span><span class="sxs-lookup"><span data-stu-id="cf5b0-136">Equality is returned only if the columns compared contain the same values in the same order.</span></span> <span data-ttu-id="cf5b0-137">1 つの列の値が他の列よりも少ない場合、報告される関係は、もう一方の値に対する null 値の関係になります。</span><span class="sxs-lookup"><span data-stu-id="cf5b0-137">If one column has fewer values than the other, the reported relation is that of a null value to the other value.</span></span>
  
<span data-ttu-id="cf5b0-138">制限の詳細については、「制限について [」を参照してください](about-restrictions.md)。</span><span class="sxs-lookup"><span data-stu-id="cf5b0-138">For more information about restrictions, see [About Restrictions](about-restrictions.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="cf5b0-139">サーバー上のデータを検索する動的クエリを作成する場合は **、Restrict** メソッドと **QueryRows** メソッドを一緒に使用する代わりに **FindRow** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="cf5b0-139">If you create dynamic queries to search for data on the server, use the **FindRow** method instead of using the **Restrict** method and the **QueryRows** method together.</span></span> <span data-ttu-id="cf5b0-140">**Restrict メソッド** は、ベース フォルダーに追加または変更されたメッセージを評価するために使用されるキャッシュ ビューを作成します。</span><span class="sxs-lookup"><span data-stu-id="cf5b0-140">The **Restrict** method creates a cached view that is used to evaluate all messages added to or modified in the base folder.</span></span> <span data-ttu-id="cf5b0-141">クライアント アプリケーションが動的クエリごとに **Restrict** メソッドを使用する場合は、クエリごとにキャッシュ ビューが作成されます。</span><span class="sxs-lookup"><span data-stu-id="cf5b0-141">If a client application uses the **Restrict** method for each dynamic query, a cached view will be created for each query.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="cf5b0-142">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="cf5b0-142">Notes to callers</span></span>

<span data-ttu-id="cf5b0-143">新しい制限を作成せずに現在の制限を破棄するには  _、lpRestriction で NULL を渡します_。</span><span class="sxs-lookup"><span data-stu-id="cf5b0-143">To discard the current restriction without creating a new one, pass NULL in  _lpRestriction_.</span></span>
  
<span data-ttu-id="cf5b0-144">別の非同期テーブル呼び出しが進行中で、Restrict が MAPI_E_BUSY を返す場合は[、IMAPITable::Abort](imapitable-abort.md)を呼び出して呼び出しを停止できます。</span><span class="sxs-lookup"><span data-stu-id="cf5b0-144">If another asynchronous table call is in progress, causing **Restrict** to return MAPI_E_BUSY, you can call [IMAPITable::Abort](imapitable-abort.md) to stop the call.</span></span> 
  
 <span data-ttu-id="cf5b0-145">**Restrict** は、フラグのいずれかを設定しない限り、同期的に動作します。</span><span class="sxs-lookup"><span data-stu-id="cf5b0-145">**Restrict** operates synchronously unless you set one of the flags.</span></span> <span data-ttu-id="cf5b0-146">[制限] フラグをTBL_BATCH **場合** は、データを要求しない限り、制限の評価が延期されます。</span><span class="sxs-lookup"><span data-stu-id="cf5b0-146">If you set the TBL_BATCH flag, **Restrict** postpones the evaluation of the restriction unless you request the data.</span></span> <span data-ttu-id="cf5b0-147">このフラグTBL_ASYNC設定されている場合 **、Restrict** は非同期的に動作し、操作が完了する前に戻る可能性があります。</span><span class="sxs-lookup"><span data-stu-id="cf5b0-147">If the TBL_ASYNC flag is set, **Restrict** operates asynchronously, potentially returning before the completion of the operation.</span></span>
  
<span data-ttu-id="cf5b0-148">テーブルのすべてのブックマークは **、Restrict** の呼び出しが行われたときに破棄され、現在のカーソル位置である BOOKMARK_CURRENT がテーブルの先頭に設定されます。</span><span class="sxs-lookup"><span data-stu-id="cf5b0-148">All bookmarks for a table are discarded when a call to **Restrict** is made, and BOOKMARK_CURRENT, the current cursor position, is set to the beginning of the table.</span></span> 
  
<span data-ttu-id="cf5b0-149">テーブルの列セットに含めされていないプロパティにプロパティ制限を適用しようとすると、結果は未定義になります。</span><span class="sxs-lookup"><span data-stu-id="cf5b0-149">If you attempt to impose a property restriction on a property that is not in the table's column set, the results are undefined.</span></span> <span data-ttu-id="cf5b0-150">プロパティがテーブルでサポートされるかどうかが不明な場合は、プロパティ制限と存在する制限を組み合わせます。</span><span class="sxs-lookup"><span data-stu-id="cf5b0-150">Whenever you are unsure as to whether a property is supported in a table, combine the property restriction with an exists restriction.</span></span> <span data-ttu-id="cf5b0-151">存在する制限は、プロパティ制限を適用する前に、プロパティの存在をチェックします。</span><span class="sxs-lookup"><span data-stu-id="cf5b0-151">The exists restriction checks for the existence of the property before attempting to impose the property restriction.</span></span> 
  
<span data-ttu-id="cf5b0-152">制限のためにテーブルからフィルター処理された行に対するテーブル通知を受け取る必要はありません。</span><span class="sxs-lookup"><span data-stu-id="cf5b0-152">Do not expect to receive a table notification on a row that has been filtered from a table due to a restriction.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="cf5b0-153">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="cf5b0-153">MFCMAPI reference</span></span>

<span data-ttu-id="cf5b0-154">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cf5b0-154">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="cf5b0-155">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="cf5b0-155">**File**</span></span>|<span data-ttu-id="cf5b0-156">**関数**</span><span class="sxs-lookup"><span data-stu-id="cf5b0-156">**Function**</span></span>|<span data-ttu-id="cf5b0-157">**コメント**</span><span class="sxs-lookup"><span data-stu-id="cf5b0-157">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cf5b0-158">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="cf5b0-158">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="cf5b0-159">CContentsTableListCtrl::ApplyRestriction</span><span class="sxs-lookup"><span data-stu-id="cf5b0-159">CContentsTableListCtrl::ApplyRestriction</span></span>  <br/> |<span data-ttu-id="cf5b0-160">MFCMAPI は **IMAPITable::Restrict** メソッドを使用して、テーブルに制限を設定します。</span><span class="sxs-lookup"><span data-stu-id="cf5b0-160">MFCMAPI uses the **IMAPITable::Restrict** method to set a restriction on a table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cf5b0-161">関連項目</span><span class="sxs-lookup"><span data-stu-id="cf5b0-161">See also</span></span>



[<span data-ttu-id="cf5b0-162">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="cf5b0-162">IMAPITable::Abort</span></span>](imapitable-abort.md)
  
[<span data-ttu-id="cf5b0-163">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="cf5b0-163">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="cf5b0-164">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="cf5b0-164">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="cf5b0-165">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="cf5b0-165">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="cf5b0-166">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="cf5b0-166">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="cf5b0-167">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cf5b0-167">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


<span data-ttu-id="cf5b0-168">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="cf5b0-168">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

