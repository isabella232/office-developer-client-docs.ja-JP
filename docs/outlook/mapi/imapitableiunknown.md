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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 0ffaf5909c978059343067c93a2b30f5969327e4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800852"
---
# <a name="imapitable--iunknown"></a><span data-ttu-id="3f92a-103">IMAPITable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="3f92a-103">IMAPITable : IUnknown</span></span>

  
  
<span data-ttu-id="3f92a-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3f92a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3f92a-105">テーブルの読み取り専用ビューを提供します。</span><span class="sxs-lookup"><span data-stu-id="3f92a-105">Provides a read-only view of a table.</span></span> <span data-ttu-id="3f92a-106">**IMAPITable**は、テーブルの表示方法を操作するクライアントとサービス ・ プロバイダーによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="3f92a-106">**IMAPITable** is used by clients and service providers to manipulate the way a table appears.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3f92a-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="3f92a-107">Header file:</span></span>  <br/> |<span data-ttu-id="3f92a-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3f92a-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="3f92a-109">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="3f92a-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="3f92a-110">テーブル オブジェクト</span><span class="sxs-lookup"><span data-stu-id="3f92a-110">Table objects</span></span>  <br/> |
|<span data-ttu-id="3f92a-111">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="3f92a-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="3f92a-112">サービス プロバイダーおよび MAPI</span><span class="sxs-lookup"><span data-stu-id="3f92a-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="3f92a-113">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3f92a-113">Called by:</span></span>  <br/> |<span data-ttu-id="3f92a-114">クライアント アプリケーション、サービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="3f92a-114">Client applications, service providers</span></span>  <br/> |
|<span data-ttu-id="3f92a-115">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="3f92a-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="3f92a-116">IID_IMAPITable</span><span class="sxs-lookup"><span data-stu-id="3f92a-116">IID_IMAPITable</span></span>  <br/> |
|<span data-ttu-id="3f92a-117">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="3f92a-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="3f92a-118">LPMAPITABLE</span><span class="sxs-lookup"><span data-stu-id="3f92a-118">LPMAPITABLE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="3f92a-119">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="3f92a-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="3f92a-120">発生しました</span><span class="sxs-lookup"><span data-stu-id="3f92a-120">GetLastError</span></span>](imapitable-getlasterror.md) <br/> |<span data-ttu-id="3f92a-121">テーブルの前のエラーに関する情報を含む[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="3f92a-121">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error on the table.</span></span>  <br/> |
|[<span data-ttu-id="3f92a-122">アドバイス</span><span class="sxs-lookup"><span data-stu-id="3f92a-122">Advise</span></span>](imapitable-advise.md) <br/> |<span data-ttu-id="3f92a-123">テーブルに影響を与えず、指定されたイベントの通知を受け取ることを登録します。</span><span class="sxs-lookup"><span data-stu-id="3f92a-123">Registers to receive notification of specified events affecting the table.</span></span>  <br/> |
|[<span data-ttu-id="3f92a-124">アドバイズ中止します。</span><span class="sxs-lookup"><span data-stu-id="3f92a-124">Unadvise</span></span>](imapitable-unadvise.md) <br/> |<span data-ttu-id="3f92a-125">**IMAPITable::Advise**メソッドへの呼び出しは、設定済みの通知の送信をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="3f92a-125">Cancels the sending of notifications previously set up with a call to the **IMAPITable::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="3f92a-126">GetStatus</span><span class="sxs-lookup"><span data-stu-id="3f92a-126">GetStatus</span></span>](imapitable-getstatus.md) <br/> |<span data-ttu-id="3f92a-127">テーブルのステータスおよび種類を返します。</span><span class="sxs-lookup"><span data-stu-id="3f92a-127">Returns the table's status and type.</span></span>  <br/> |
|[<span data-ttu-id="3f92a-128">SetColumns</span><span class="sxs-lookup"><span data-stu-id="3f92a-128">SetColumns</span></span>](imapitable-setcolumns.md) <br/> |<span data-ttu-id="3f92a-129">特定のプロパティと、テーブル内の列として表示するプロパティの順序を定義します。</span><span class="sxs-lookup"><span data-stu-id="3f92a-129">Defines the particular properties and order of properties to appear as columns in the table.</span></span>  <br/> |
|[<span data-ttu-id="3f92a-130">QueryColumns</span><span class="sxs-lookup"><span data-stu-id="3f92a-130">QueryColumns</span></span>](imapitable-querycolumns.md) <br/> |<span data-ttu-id="3f92a-131">テーブルの列の一覧を返します。</span><span class="sxs-lookup"><span data-stu-id="3f92a-131">Returns a list of columns for the table.</span></span>  <br/> |
|[<span data-ttu-id="3f92a-132">な</span><span class="sxs-lookup"><span data-stu-id="3f92a-132">GetRowCount</span></span>](imapitable-getrowcount.md) <br/> |<span data-ttu-id="3f92a-133">テーブル内の行の合計数を返します。</span><span class="sxs-lookup"><span data-stu-id="3f92a-133">Returns the total number of rows in the table.</span></span>  <br/> |
|[<span data-ttu-id="3f92a-134">SeekRow</span><span class="sxs-lookup"><span data-stu-id="3f92a-134">SeekRow</span></span>](imapitable-seekrow.md) <br/> |<span data-ttu-id="3f92a-135">テーブル内の特定の位置にカーソルを移動します。</span><span class="sxs-lookup"><span data-stu-id="3f92a-135">Moves the cursor to a specific position in the table.</span></span>  <br/> |
|[<span data-ttu-id="3f92a-136">SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="3f92a-136">SeekRowApprox</span></span>](imapitable-seekrowapprox.md) <br/> |<span data-ttu-id="3f92a-137">テーブルのおおよその小数部から成る位置にカーソルを移動します。</span><span class="sxs-lookup"><span data-stu-id="3f92a-137">Moves the cursor to an approximate fractional position in the table.</span></span>  <br/> |
|[<span data-ttu-id="3f92a-138">QueryPosition</span><span class="sxs-lookup"><span data-stu-id="3f92a-138">QueryPosition</span></span>](imapitable-queryposition.md) <br/> |<span data-ttu-id="3f92a-139">小数部の値に基づいて、カーソルの現在のテーブルの行位置を取得します。</span><span class="sxs-lookup"><span data-stu-id="3f92a-139">Retrieves the current table row position of the cursor, based on a fractional value.</span></span>  <br/> |
|[<span data-ttu-id="3f92a-140">FindRow</span><span class="sxs-lookup"><span data-stu-id="3f92a-140">FindRow</span></span>](imapitable-findrow.md) <br/> |<span data-ttu-id="3f92a-141">特定の検索条件に一致するテーブル内には、次の行を検索します。</span><span class="sxs-lookup"><span data-stu-id="3f92a-141">Finds the next row in a table that matches specific search criteria.</span></span>  <br/> |
|[<span data-ttu-id="3f92a-142">制限します。</span><span class="sxs-lookup"><span data-stu-id="3f92a-142">Restrict</span></span>](imapitable-restrict.md) <br/> |<span data-ttu-id="3f92a-143">指定した条件に一致する行のみに設定した行を減らすこと、テーブルにフィルターを適用します。</span><span class="sxs-lookup"><span data-stu-id="3f92a-143">Applies a filter to a table, reducing the row set to only those rows matching the specified criteria.</span></span>  <br/> |
|[<span data-ttu-id="3f92a-144">CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="3f92a-144">CreateBookmark</span></span>](imapitable-createbookmark.md) <br/> |<span data-ttu-id="3f92a-145">テーブルの現在の位置をマークします。</span><span class="sxs-lookup"><span data-stu-id="3f92a-145">Marks the table's current position.</span></span>  <br/> |
|[<span data-ttu-id="3f92a-146">FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="3f92a-146">FreeBookmark</span></span>](imapitable-freebookmark.md) <br/> |<span data-ttu-id="3f92a-147">ブックマークに関連付けられているメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="3f92a-147">Releases the memory associated with a bookmark.</span></span>  <br/> |
|[<span data-ttu-id="3f92a-148">SortTable</span><span class="sxs-lookup"><span data-stu-id="3f92a-148">SortTable</span></span>](imapitable-sorttable.md) <br/> |<span data-ttu-id="3f92a-149">並べ替え条件に基づいて、テーブルの行を順序付けします。</span><span class="sxs-lookup"><span data-stu-id="3f92a-149">Orders the rows of the table based on sort criteria.</span></span>  <br/> |
|[<span data-ttu-id="3f92a-150">QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="3f92a-150">QuerySortOrder</span></span>](imapitable-querysortorder.md) <br/> |<span data-ttu-id="3f92a-151">テーブルの現在の並べ替え順序を取得します。</span><span class="sxs-lookup"><span data-stu-id="3f92a-151">Retrieves the current sort order for a table.</span></span>  <br/> |
|[<span data-ttu-id="3f92a-152">QueryRows</span><span class="sxs-lookup"><span data-stu-id="3f92a-152">QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="3f92a-153">現在のカーソル位置から開始し、テーブルから 1 つまたは複数の行を返します。</span><span class="sxs-lookup"><span data-stu-id="3f92a-153">Returns one or more rows from a table, beginning at the current cursor position.</span></span>  <br/> |
|[<span data-ttu-id="3f92a-154">中止</span><span class="sxs-lookup"><span data-stu-id="3f92a-154">Abort</span></span>](imapitable-abort.md) <br/> |<span data-ttu-id="3f92a-155">テーブルの現在進行中のすべての非同期操作を停止します。</span><span class="sxs-lookup"><span data-stu-id="3f92a-155">Stops any asynchronous operations currently in progress for the table.</span></span>  <br/> |
|[<span data-ttu-id="3f92a-156">ExpandRow</span><span class="sxs-lookup"><span data-stu-id="3f92a-156">ExpandRow</span></span>](imapitable-expandrow.md) <br/> |<span data-ttu-id="3f92a-157">テーブル ビューをカテゴリに属しているリーフ行の追加、折りたたまれているテーブルのカテゴリを展開します。</span><span class="sxs-lookup"><span data-stu-id="3f92a-157">Expands a collapsed table category, adding the leaf rows belonging to the category to the table view.</span></span>  <br/> |
|[<span data-ttu-id="3f92a-158">CollapseRow</span><span class="sxs-lookup"><span data-stu-id="3f92a-158">CollapseRow</span></span>](imapitable-collapserow.md) <br/> |<span data-ttu-id="3f92a-159">テーブル ・ ビューのカテゴリに属するリーフ行を削除する、拡張テーブルのカテゴリを折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="3f92a-159">Collapses an expanded table category, removing the leaf rows belonging to the category from the table view.</span></span>  <br/> |
|[<span data-ttu-id="3f92a-160">WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="3f92a-160">WaitForCompletion</span></span>](imapitable-waitforcompletion.md) <br/> |<span data-ttu-id="3f92a-161">1 つまたは複数の非同期操作の進行状況でテーブルに完了するまでの処理を中断します。</span><span class="sxs-lookup"><span data-stu-id="3f92a-161">Suspends processing until one or more asynchronous operations in progress on the table have completed.</span></span>  <br/> |
|[<span data-ttu-id="3f92a-162">GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="3f92a-162">GetCollapseState</span></span>](imapitable-getcollapsestate.md) <br/> |<span data-ttu-id="3f92a-163">現在を再構築するために必要なデータを返しますは、折りたたむか、カテゴリ別のテーブルの状態を展開します。</span><span class="sxs-lookup"><span data-stu-id="3f92a-163">Returns the data necessary to rebuild the current collapsed or expanded state of a categorized table.</span></span>  <br/> |
|[<span data-ttu-id="3f92a-164">SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="3f92a-164">SetCollapseState</span></span>](imapitable-setcollapsestate.md) <br/> |<span data-ttu-id="3f92a-165">**IMAPITable::GetCollapseState**メソッドへの前回の呼び出しによって保存されたデータを使用して分類されたテーブルの現在の展開または折りたたみの状態を再構築します。</span><span class="sxs-lookup"><span data-stu-id="3f92a-165">Rebuilds the current expanded or collapsed state of a categorized table using data that was saved by a prior call to the **IMAPITable::GetCollapseState** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3f92a-166">関連項目</span><span class="sxs-lookup"><span data-stu-id="3f92a-166">See also</span></span>



[<span data-ttu-id="3f92a-167">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="3f92a-167">MAPI Interfaces</span></span>](mapi-interfaces.md)

