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
# <a name="imapitable--iunknown"></a><span data-ttu-id="96bd7-103">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="96bd7-103">IMAPITable : IUnknown</span></span>

  
  
<span data-ttu-id="96bd7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="96bd7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="96bd7-105">テーブルの読み取り専用ビューを提供します。</span><span class="sxs-lookup"><span data-stu-id="96bd7-105">Provides a read-only view of a table.</span></span> <span data-ttu-id="96bd7-106">**IMAPITable は** 、クライアントとサービス プロバイダーがテーブルの表示方法を操作するために使用します。</span><span class="sxs-lookup"><span data-stu-id="96bd7-106">**IMAPITable** is used by clients and service providers to manipulate the way a table appears.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="96bd7-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="96bd7-107">Header file:</span></span>  <br/> |<span data-ttu-id="96bd7-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="96bd7-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="96bd7-109">次のユーザーによって公開されます。</span><span class="sxs-lookup"><span data-stu-id="96bd7-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="96bd7-110">Table オブジェクト</span><span class="sxs-lookup"><span data-stu-id="96bd7-110">Table objects</span></span>  <br/> |
|<span data-ttu-id="96bd7-111">実装元:</span><span class="sxs-lookup"><span data-stu-id="96bd7-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="96bd7-112">サービス プロバイダーと MAPI</span><span class="sxs-lookup"><span data-stu-id="96bd7-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="96bd7-113">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="96bd7-113">Called by:</span></span>  <br/> |<span data-ttu-id="96bd7-114">クライアント アプリケーション、サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="96bd7-114">Client applications, service providers</span></span>  <br/> |
|<span data-ttu-id="96bd7-115">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="96bd7-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="96bd7-116">IID_IMAPITable</span><span class="sxs-lookup"><span data-stu-id="96bd7-116">IID_IMAPITable</span></span>  <br/> |
|<span data-ttu-id="96bd7-117">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="96bd7-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="96bd7-118">LPMAPITABLE</span><span class="sxs-lookup"><span data-stu-id="96bd7-118">LPMAPITABLE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="96bd7-119">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="96bd7-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="96bd7-120">GetLastError</span><span class="sxs-lookup"><span data-stu-id="96bd7-120">GetLastError</span></span>](imapitable-getlasterror.md) <br/> |<span data-ttu-id="96bd7-121">テーブルの前 [のエラー](mapierror.md) に関する情報を含む MAPIERROR 構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="96bd7-121">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error on the table.</span></span>  <br/> |
|[<span data-ttu-id="96bd7-122">アドバイス</span><span class="sxs-lookup"><span data-stu-id="96bd7-122">Advise</span></span>](imapitable-advise.md) <br/> |<span data-ttu-id="96bd7-123">テーブルに影響を与える指定されたイベントの通知を受信するために登録します。</span><span class="sxs-lookup"><span data-stu-id="96bd7-123">Registers to receive notification of specified events affecting the table.</span></span>  <br/> |
|[<span data-ttu-id="96bd7-124">Unadvise</span><span class="sxs-lookup"><span data-stu-id="96bd7-124">Unadvise</span></span>](imapitable-unadvise.md) <br/> |<span data-ttu-id="96bd7-125">**IMAPITable::Advise** メソッドへの呼び出しで以前に設定された通知の送信をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="96bd7-125">Cancels the sending of notifications previously set up with a call to the **IMAPITable::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="96bd7-126">GetStatus</span><span class="sxs-lookup"><span data-stu-id="96bd7-126">GetStatus</span></span>](imapitable-getstatus.md) <br/> |<span data-ttu-id="96bd7-127">テーブルの状態と型を返します。</span><span class="sxs-lookup"><span data-stu-id="96bd7-127">Returns the table's status and type.</span></span>  <br/> |
|[<span data-ttu-id="96bd7-128">SetColumns</span><span class="sxs-lookup"><span data-stu-id="96bd7-128">SetColumns</span></span>](imapitable-setcolumns.md) <br/> |<span data-ttu-id="96bd7-129">テーブルに列として表示するプロパティの特定のプロパティと順序を定義します。</span><span class="sxs-lookup"><span data-stu-id="96bd7-129">Defines the particular properties and order of properties to appear as columns in the table.</span></span>  <br/> |
|[<span data-ttu-id="96bd7-130">QueryColumns</span><span class="sxs-lookup"><span data-stu-id="96bd7-130">QueryColumns</span></span>](imapitable-querycolumns.md) <br/> |<span data-ttu-id="96bd7-131">テーブルの列の一覧を返します。</span><span class="sxs-lookup"><span data-stu-id="96bd7-131">Returns a list of columns for the table.</span></span>  <br/> |
|[<span data-ttu-id="96bd7-132">GetRowCount</span><span class="sxs-lookup"><span data-stu-id="96bd7-132">GetRowCount</span></span>](imapitable-getrowcount.md) <br/> |<span data-ttu-id="96bd7-133">テーブル内の行の総数を返します。</span><span class="sxs-lookup"><span data-stu-id="96bd7-133">Returns the total number of rows in the table.</span></span>  <br/> |
|[<span data-ttu-id="96bd7-134">SeekRow</span><span class="sxs-lookup"><span data-stu-id="96bd7-134">SeekRow</span></span>](imapitable-seekrow.md) <br/> |<span data-ttu-id="96bd7-135">テーブル内の特定の位置にカーソルを移動します。</span><span class="sxs-lookup"><span data-stu-id="96bd7-135">Moves the cursor to a specific position in the table.</span></span>  <br/> |
|[<span data-ttu-id="96bd7-136">SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="96bd7-136">SeekRowApprox</span></span>](imapitable-seekrowapprox.md) <br/> |<span data-ttu-id="96bd7-137">カーソルをテーブル内のおおよその小数位置に移動します。</span><span class="sxs-lookup"><span data-stu-id="96bd7-137">Moves the cursor to an approximate fractional position in the table.</span></span>  <br/> |
|[<span data-ttu-id="96bd7-138">QueryPosition</span><span class="sxs-lookup"><span data-stu-id="96bd7-138">QueryPosition</span></span>](imapitable-queryposition.md) <br/> |<span data-ttu-id="96bd7-139">小数部の値に基づいて、カーソルの現在のテーブル行の位置を取得します。</span><span class="sxs-lookup"><span data-stu-id="96bd7-139">Retrieves the current table row position of the cursor, based on a fractional value.</span></span>  <br/> |
|[<span data-ttu-id="96bd7-140">FindRow</span><span class="sxs-lookup"><span data-stu-id="96bd7-140">FindRow</span></span>](imapitable-findrow.md) <br/> |<span data-ttu-id="96bd7-141">特定の検索条件に一致するテーブル内の次の行を検索します。</span><span class="sxs-lookup"><span data-stu-id="96bd7-141">Finds the next row in a table that matches specific search criteria.</span></span>  <br/> |
|[<span data-ttu-id="96bd7-142">Restrict</span><span class="sxs-lookup"><span data-stu-id="96bd7-142">Restrict</span></span>](imapitable-restrict.md) <br/> |<span data-ttu-id="96bd7-143">テーブルにフィルターを適用し、指定した条件に一致する行にのみ行セットを減らします。</span><span class="sxs-lookup"><span data-stu-id="96bd7-143">Applies a filter to a table, reducing the row set to only those rows matching the specified criteria.</span></span>  <br/> |
|[<span data-ttu-id="96bd7-144">CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="96bd7-144">CreateBookmark</span></span>](imapitable-createbookmark.md) <br/> |<span data-ttu-id="96bd7-145">テーブルの現在の位置をマークします。</span><span class="sxs-lookup"><span data-stu-id="96bd7-145">Marks the table's current position.</span></span>  <br/> |
|[<span data-ttu-id="96bd7-146">FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="96bd7-146">FreeBookmark</span></span>](imapitable-freebookmark.md) <br/> |<span data-ttu-id="96bd7-147">ブックマークに関連付けられているメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="96bd7-147">Releases the memory associated with a bookmark.</span></span>  <br/> |
|[<span data-ttu-id="96bd7-148">SortTable</span><span class="sxs-lookup"><span data-stu-id="96bd7-148">SortTable</span></span>](imapitable-sorttable.md) <br/> |<span data-ttu-id="96bd7-149">並べ替え条件に基づいてテーブルの行を並べ替える。</span><span class="sxs-lookup"><span data-stu-id="96bd7-149">Orders the rows of the table based on sort criteria.</span></span>  <br/> |
|[<span data-ttu-id="96bd7-150">QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="96bd7-150">QuerySortOrder</span></span>](imapitable-querysortorder.md) <br/> |<span data-ttu-id="96bd7-151">テーブルの現在の並べ替え順序を取得します。</span><span class="sxs-lookup"><span data-stu-id="96bd7-151">Retrieves the current sort order for a table.</span></span>  <br/> |
|[<span data-ttu-id="96bd7-152">QueryRows</span><span class="sxs-lookup"><span data-stu-id="96bd7-152">QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="96bd7-153">現在のカーソル位置から始まる、テーブルから 1 つ以上の行を返します。</span><span class="sxs-lookup"><span data-stu-id="96bd7-153">Returns one or more rows from a table, beginning at the current cursor position.</span></span>  <br/> |
|[<span data-ttu-id="96bd7-154">中止</span><span class="sxs-lookup"><span data-stu-id="96bd7-154">Abort</span></span>](imapitable-abort.md) <br/> |<span data-ttu-id="96bd7-155">テーブルの現在進行中の非同期操作を停止します。</span><span class="sxs-lookup"><span data-stu-id="96bd7-155">Stops any asynchronous operations currently in progress for the table.</span></span>  <br/> |
|[<span data-ttu-id="96bd7-156">ExpandRow</span><span class="sxs-lookup"><span data-stu-id="96bd7-156">ExpandRow</span></span>](imapitable-expandrow.md) <br/> |<span data-ttu-id="96bd7-157">折りたたみテーブル カテゴリを展開し、そのカテゴリに属するリーフ行をテーブル ビューに追加します。</span><span class="sxs-lookup"><span data-stu-id="96bd7-157">Expands a collapsed table category, adding the leaf rows belonging to the category to the table view.</span></span>  <br/> |
|[<span data-ttu-id="96bd7-158">CollapseRow</span><span class="sxs-lookup"><span data-stu-id="96bd7-158">CollapseRow</span></span>](imapitable-collapserow.md) <br/> |<span data-ttu-id="96bd7-159">展開されたテーブル カテゴリを折りたたみ、そのカテゴリに属するリーフ行をテーブル ビューから削除します。</span><span class="sxs-lookup"><span data-stu-id="96bd7-159">Collapses an expanded table category, removing the leaf rows belonging to the category from the table view.</span></span>  <br/> |
|[<span data-ttu-id="96bd7-160">WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="96bd7-160">WaitForCompletion</span></span>](imapitable-waitforcompletion.md) <br/> |<span data-ttu-id="96bd7-161">テーブルで進行中の 1 つ以上の非同期操作が完了するまで、処理を中断します。</span><span class="sxs-lookup"><span data-stu-id="96bd7-161">Suspends processing until one or more asynchronous operations in progress on the table have completed.</span></span>  <br/> |
|[<span data-ttu-id="96bd7-162">GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="96bd7-162">GetCollapseState</span></span>](imapitable-getcollapsestate.md) <br/> |<span data-ttu-id="96bd7-163">分類されたテーブルの現在の折りたたみ状態または展開状態を再構築するために必要なデータを返します。</span><span class="sxs-lookup"><span data-stu-id="96bd7-163">Returns the data necessary to rebuild the current collapsed or expanded state of a categorized table.</span></span>  <br/> |
|[<span data-ttu-id="96bd7-164">SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="96bd7-164">SetCollapseState</span></span>](imapitable-setcollapsestate.md) <br/> |<span data-ttu-id="96bd7-165">**IMAPITable::GetCollapseState** メソッドの以前の呼び出しによって保存されたデータを使用して、分類されたテーブルの現在の展開状態または折りたたみ状態を再構築します。</span><span class="sxs-lookup"><span data-stu-id="96bd7-165">Rebuilds the current expanded or collapsed state of a categorized table using data that was saved by a prior call to the **IMAPITable::GetCollapseState** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="96bd7-166">関連項目</span><span class="sxs-lookup"><span data-stu-id="96bd7-166">See also</span></span>



[<span data-ttu-id="96bd7-167">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="96bd7-167">MAPI Interfaces</span></span>](mapi-interfaces.md)

