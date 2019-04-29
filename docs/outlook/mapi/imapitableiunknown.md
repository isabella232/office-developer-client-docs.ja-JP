---
title: IMAPITable IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable
api_type:
- COM
ms.assetid: f25be2b1-0f94-4a0c-b29d-d2201dc70ab7
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d6a13799da4ef9315f9c23317fa18853d71c72f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420116"
---
# <a name="imapitable--iunknown"></a><span data-ttu-id="ea2d8-103">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ea2d8-103">IMAPITable : IUnknown</span></span>

  
  
<span data-ttu-id="ea2d8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ea2d8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ea2d8-105">テーブルの読み取り専用のビューを提供します。</span><span class="sxs-lookup"><span data-stu-id="ea2d8-105">Provides a read-only view of a table.</span></span> <span data-ttu-id="ea2d8-106">**IMAPITable**は、クライアントとサービスプロバイダーが表の表示方法を操作するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ea2d8-106">**IMAPITable** is used by clients and service providers to manipulate the way a table appears.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ea2d8-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="ea2d8-107">Header file:</span></span>  <br/> |<span data-ttu-id="ea2d8-108">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ea2d8-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ea2d8-109">公開者:</span><span class="sxs-lookup"><span data-stu-id="ea2d8-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="ea2d8-110">Table オブジェクト</span><span class="sxs-lookup"><span data-stu-id="ea2d8-110">Table objects</span></span>  <br/> |
|<span data-ttu-id="ea2d8-111">実装元:</span><span class="sxs-lookup"><span data-stu-id="ea2d8-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="ea2d8-112">サービスプロバイダーと MAPI</span><span class="sxs-lookup"><span data-stu-id="ea2d8-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="ea2d8-113">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="ea2d8-113">Called by:</span></span>  <br/> |<span data-ttu-id="ea2d8-114">クライアントアプリケーション、サービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="ea2d8-114">Client applications, service providers</span></span>  <br/> |
|<span data-ttu-id="ea2d8-115">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="ea2d8-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="ea2d8-116">IID_IMAPITable</span><span class="sxs-lookup"><span data-stu-id="ea2d8-116">IID_IMAPITable</span></span>  <br/> |
|<span data-ttu-id="ea2d8-117">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="ea2d8-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="ea2d8-118">LPMAPITABLE</span><span class="sxs-lookup"><span data-stu-id="ea2d8-118">LPMAPITABLE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="ea2d8-119">v の順序</span><span class="sxs-lookup"><span data-stu-id="ea2d8-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="ea2d8-120">GetLastError</span><span class="sxs-lookup"><span data-stu-id="ea2d8-120">GetLastError</span></span>](imapitable-getlasterror.md) <br/> |<span data-ttu-id="ea2d8-121">表の前のエラーについての情報を含む[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="ea2d8-121">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error on the table.</span></span>  <br/> |
|[<span data-ttu-id="ea2d8-122">助言</span><span class="sxs-lookup"><span data-stu-id="ea2d8-122">Advise</span></span>](imapitable-advise.md) <br/> |<span data-ttu-id="ea2d8-123">テーブルに影響を与える指定したイベントの通知を受信するように登録します。</span><span class="sxs-lookup"><span data-stu-id="ea2d8-123">Registers to receive notification of specified events affecting the table.</span></span>  <br/> |
|[<span data-ttu-id="ea2d8-124">アドバイズ</span><span class="sxs-lookup"><span data-stu-id="ea2d8-124">Unadvise</span></span>](imapitable-unadvise.md) <br/> |<span data-ttu-id="ea2d8-125">**IMAPITable:: Advise**メソッドへの呼び出しを使用して、以前に設定した通知の送信をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="ea2d8-125">Cancels the sending of notifications previously set up with a call to the **IMAPITable::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="ea2d8-126">GetStatus</span><span class="sxs-lookup"><span data-stu-id="ea2d8-126">GetStatus</span></span>](imapitable-getstatus.md) <br/> |<span data-ttu-id="ea2d8-127">テーブルの状態と種類を返します。</span><span class="sxs-lookup"><span data-stu-id="ea2d8-127">Returns the table's status and type.</span></span>  <br/> |
|[<span data-ttu-id="ea2d8-128">SetColumns</span><span class="sxs-lookup"><span data-stu-id="ea2d8-128">SetColumns</span></span>](imapitable-setcolumns.md) <br/> |<span data-ttu-id="ea2d8-129">表に列として表示されるプロパティとプロパティの順序を定義します。</span><span class="sxs-lookup"><span data-stu-id="ea2d8-129">Defines the particular properties and order of properties to appear as columns in the table.</span></span>  <br/> |
|[<span data-ttu-id="ea2d8-130">querycolumns</span><span class="sxs-lookup"><span data-stu-id="ea2d8-130">QueryColumns</span></span>](imapitable-querycolumns.md) <br/> |<span data-ttu-id="ea2d8-131">テーブルの列のリストを返します。</span><span class="sxs-lookup"><span data-stu-id="ea2d8-131">Returns a list of columns for the table.</span></span>  <br/> |
|[<span data-ttu-id="ea2d8-132">GetRowCount</span><span class="sxs-lookup"><span data-stu-id="ea2d8-132">GetRowCount</span></span>](imapitable-getrowcount.md) <br/> |<span data-ttu-id="ea2d8-133">テーブル内の行の総数を返します。</span><span class="sxs-lookup"><span data-stu-id="ea2d8-133">Returns the total number of rows in the table.</span></span>  <br/> |
|[<span data-ttu-id="ea2d8-134">seekrow</span><span class="sxs-lookup"><span data-stu-id="ea2d8-134">SeekRow</span></span>](imapitable-seekrow.md) <br/> |<span data-ttu-id="ea2d8-135">テーブル内の特定の位置にカーソルを移動します。</span><span class="sxs-lookup"><span data-stu-id="ea2d8-135">Moves the cursor to a specific position in the table.</span></span>  <br/> |
|[<span data-ttu-id="ea2d8-136">seekrowapprox</span><span class="sxs-lookup"><span data-stu-id="ea2d8-136">SeekRowApprox</span></span>](imapitable-seekrowapprox.md) <br/> |<span data-ttu-id="ea2d8-137">テーブル内のおおよその分数位置にカーソルを移動します。</span><span class="sxs-lookup"><span data-stu-id="ea2d8-137">Moves the cursor to an approximate fractional position in the table.</span></span>  <br/> |
|[<span data-ttu-id="ea2d8-138">queryposition</span><span class="sxs-lookup"><span data-stu-id="ea2d8-138">QueryPosition</span></span>](imapitable-queryposition.md) <br/> |<span data-ttu-id="ea2d8-139">小数値に基づいて、カーソルの現在のテーブル行の位置を取得します。</span><span class="sxs-lookup"><span data-stu-id="ea2d8-139">Retrieves the current table row position of the cursor, based on a fractional value.</span></span>  <br/> |
|[<span data-ttu-id="ea2d8-140">FindRow</span><span class="sxs-lookup"><span data-stu-id="ea2d8-140">FindRow</span></span>](imapitable-findrow.md) <br/> |<span data-ttu-id="ea2d8-141">特定の検索条件に一致するテーブル内の次の行を検索します。</span><span class="sxs-lookup"><span data-stu-id="ea2d8-141">Finds the next row in a table that matches specific search criteria.</span></span>  <br/> |
|[<span data-ttu-id="ea2d8-142">Restrict</span><span class="sxs-lookup"><span data-stu-id="ea2d8-142">Restrict</span></span>](imapitable-restrict.md) <br/> |<span data-ttu-id="ea2d8-143">テーブルにフィルターを適用し、指定された条件に一致する行だけを行のセットに絞ります。</span><span class="sxs-lookup"><span data-stu-id="ea2d8-143">Applies a filter to a table, reducing the row set to only those rows matching the specified criteria.</span></span>  <br/> |
|[<span data-ttu-id="ea2d8-144">createbookmark</span><span class="sxs-lookup"><span data-stu-id="ea2d8-144">CreateBookmark</span></span>](imapitable-createbookmark.md) <br/> |<span data-ttu-id="ea2d8-145">テーブルの現在の位置を示します。</span><span class="sxs-lookup"><span data-stu-id="ea2d8-145">Marks the table's current position.</span></span>  <br/> |
|[<span data-ttu-id="ea2d8-146">freebookmark</span><span class="sxs-lookup"><span data-stu-id="ea2d8-146">FreeBookmark</span></span>](imapitable-freebookmark.md) <br/> |<span data-ttu-id="ea2d8-147">ブックマークに関連付けられているメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="ea2d8-147">Releases the memory associated with a bookmark.</span></span>  <br/> |
|[<span data-ttu-id="ea2d8-148">sorttable</span><span class="sxs-lookup"><span data-stu-id="ea2d8-148">SortTable</span></span>](imapitable-sorttable.md) <br/> |<span data-ttu-id="ea2d8-149">並べ替えの基準に基づいて、テーブルの行の順序を示します。</span><span class="sxs-lookup"><span data-stu-id="ea2d8-149">Orders the rows of the table based on sort criteria.</span></span>  <br/> |
|[<span data-ttu-id="ea2d8-150">querysortorder</span><span class="sxs-lookup"><span data-stu-id="ea2d8-150">QuerySortOrder</span></span>](imapitable-querysortorder.md) <br/> |<span data-ttu-id="ea2d8-151">テーブルの現在の並べ替え順序を取得します。</span><span class="sxs-lookup"><span data-stu-id="ea2d8-151">Retrieves the current sort order for a table.</span></span>  <br/> |
|[<span data-ttu-id="ea2d8-152">QueryRows</span><span class="sxs-lookup"><span data-stu-id="ea2d8-152">QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="ea2d8-153">現在のカーソル位置から、1つまたは複数の行をテーブルから返します。</span><span class="sxs-lookup"><span data-stu-id="ea2d8-153">Returns one or more rows from a table, beginning at the current cursor position.</span></span>  <br/> |
|[<span data-ttu-id="ea2d8-154">中止</span><span class="sxs-lookup"><span data-stu-id="ea2d8-154">Abort</span></span>](imapitable-abort.md) <br/> |<span data-ttu-id="ea2d8-155">テーブルに対して現在進行中のすべての非同期操作を停止します。</span><span class="sxs-lookup"><span data-stu-id="ea2d8-155">Stops any asynchronous operations currently in progress for the table.</span></span>  <br/> |
|[<span data-ttu-id="ea2d8-156">expandrow</span><span class="sxs-lookup"><span data-stu-id="ea2d8-156">ExpandRow</span></span>](imapitable-expandrow.md) <br/> |<span data-ttu-id="ea2d8-157">折りたたまれたテーブルカテゴリを展開し、そのカテゴリに属するリーフ行をテーブルビューに追加します。</span><span class="sxs-lookup"><span data-stu-id="ea2d8-157">Expands a collapsed table category, adding the leaf rows belonging to the category to the table view.</span></span>  <br/> |
|[<span data-ttu-id="ea2d8-158">CollapseRow</span><span class="sxs-lookup"><span data-stu-id="ea2d8-158">CollapseRow</span></span>](imapitable-collapserow.md) <br/> |<span data-ttu-id="ea2d8-159">拡張されたテーブルカテゴリを折りたたみ、テーブルビューからそのカテゴリに属するリーフ行を削除します。</span><span class="sxs-lookup"><span data-stu-id="ea2d8-159">Collapses an expanded table category, removing the leaf rows belonging to the category from the table view.</span></span>  <br/> |
|[<span data-ttu-id="ea2d8-160">waitforcompletion</span><span class="sxs-lookup"><span data-stu-id="ea2d8-160">WaitForCompletion</span></span>](imapitable-waitforcompletion.md) <br/> |<span data-ttu-id="ea2d8-161">テーブルで進行中の1つ以上の非同期操作が完了するまで処理を中断します。</span><span class="sxs-lookup"><span data-stu-id="ea2d8-161">Suspends processing until one or more asynchronous operations in progress on the table have completed.</span></span>  <br/> |
|[<span data-ttu-id="ea2d8-162">GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="ea2d8-162">GetCollapseState</span></span>](imapitable-getcollapsestate.md) <br/> |<span data-ttu-id="ea2d8-163">カテゴリ化されたテーブルの現在の折りたたまれた状態または展開された状態を再構築するために必要なデータを返します。</span><span class="sxs-lookup"><span data-stu-id="ea2d8-163">Returns the data necessary to rebuild the current collapsed or expanded state of a categorized table.</span></span>  <br/> |
|[<span data-ttu-id="ea2d8-164">SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="ea2d8-164">SetCollapseState</span></span>](imapitable-setcollapsestate.md) <br/> |<span data-ttu-id="ea2d8-165">以前の**IMAPITable:: GetCollapseState**メソッドの呼び出しによって保存されたデータを使用して、カテゴリ化されたテーブルの現在の展開状態または折りたたみ状態を再構築します。</span><span class="sxs-lookup"><span data-stu-id="ea2d8-165">Rebuilds the current expanded or collapsed state of a categorized table using data that was saved by a prior call to the **IMAPITable::GetCollapseState** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ea2d8-166">関連項目</span><span class="sxs-lookup"><span data-stu-id="ea2d8-166">See also</span></span>



[<span data-ttu-id="ea2d8-167">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="ea2d8-167">MAPI Interfaces</span></span>](mapi-interfaces.md)

