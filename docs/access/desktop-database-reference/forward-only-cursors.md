---
title: 前方のみカーソル
TOCTitle: Forward-Only Cursors
ms:assetid: 27541bac-077b-bfe6-d9d8-713e4a945125
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249035(v=office.15)
ms:contentKeyID: 48543834
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0fdcdde9859ec0f31326134a240c7b703f4a71d1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477610"
---
# <a name="forward-only-cursors"></a><span data-ttu-id="eb545-102">前方のみカーソル</span><span class="sxs-lookup"><span data-stu-id="eb545-102">Forward-Only Cursors</span></span>


<span data-ttu-id="eb545-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="eb545-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="eb545-p101">一般的な既定のカーソルの種類は、前方のみ (またはスクロール不可) カーソルと呼ばれ、結果セットの前方だけに移動できます。前方のみカーソルは、スクロール (結果セット内を前後に移動できる機能) をサポートしておらず、結果セットの先頭から末尾の方向に行をフェッチする機能のみサポートしています。一部の前方のみカーソル (SQL Server カーソル ライブラリを使用する場合など) では、現在のユーザーが実行した (または他のユーザーがコミットした)、結果セットの行に影響する挿入、更新、および削除の各ステートメントが、行のフェッチと同時にすべて反映されます。しかし、カーソルが後方に移動できないため、行のフェッチ後にデータベースの行に加えられた変更は、カーソルを通じて反映されません。</span><span class="sxs-lookup"><span data-stu-id="eb545-p101">The typical default cursor type, called a forward-only (or non-scrollable) cursor, can move only forward through the result set. A forward-only cursor does not support scrolling (the ability to move forward and backward in the result set); it only supports fetching rows from the start to the end of the result set. With some forward-only cursors (such as with the SQL Server cursor library), all insert, update, and delete statements made by the current user (or committed by other users) that affect rows in the result set are visible as the rows are fetched. Because the cursor cannot be scrolled backward, however, changes made to rows in the database after the row was fetched are not visible through the cursor.</span></span>

<span data-ttu-id="eb545-p102">現在の行のデータが処理されると、前方のみカーソルは、そのデータの格納に使用されていたリソースを解放します。前方のみカーソルは既定で動的になっています。つまり、現在の行が処理されると同時に、すべての変更が検出されます。これにより、カーソルを迅速に開くことができ、基になるテーブルに対して実行された更新を結果セットに反映させることができます。</span><span class="sxs-lookup"><span data-stu-id="eb545-p102">After the data for the current row is processed, the forward-only cursor releases the resources that were used to hold that data. Forward-only cursors are dynamic by default, meaning that all changes are detected as the current row is processed. This provides faster cursor opening and enables the result set to display updates made to the underlying tables.</span></span>

<span data-ttu-id="eb545-p103">前方のみカーソルは後方スクロールをサポートしていませんが、アプリケーションでカーソルを閉じてから再度開くことにより、結果セットの先頭に戻ることができます。これは、データの量が少ない場合に効果的な方法です。別の方法として、アプリケーションで結果セットをいったん読み込み、データをローカルにキャッシュしてから、ローカルのデータ キャッシュを閲覧することもできます。</span><span class="sxs-lookup"><span data-stu-id="eb545-p103">While forward-only cursors do not support backward scrolling, your application can return to the beginning of the result set by closing and reopening the cursor. This is an effective way to work with small amounts of data. As an alternative, your application could read the result set once, cache the data locally, and then browse the local data cache.</span></span>

<span data-ttu-id="eb545-p104">アプリケーションで結果セット内をスクロールする必要がない場合、前方のみカーソルは、最少限のオーバーヘッドで迅速にデータを取得するための最良の方法です。ADO で前方のみカーソルを使用することを示すには、 **adOpenForwardOnly** **CursorTypeEnum** を使用します。</span><span class="sxs-lookup"><span data-stu-id="eb545-p104">If your application does not require scrolling through the result set, the forward-only cursor is the best way to retrieve data quickly with the least amount of overhead. Use the **adOpenForwardOnly** **CursorTypeEnum** to indicate that you want to use a forward-only cursor in ADO.</span></span>

