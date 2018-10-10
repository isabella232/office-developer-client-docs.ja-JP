---
title: 静的カーソル (デスクトップ データベース参照のアクセス)
TOCTitle: Static Cursors
ms:assetid: 1acf7fc5-fb12-e59e-f480-dde378a29c53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248950(v=office.15)
ms:contentKeyID: 48543524
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8878333c8390ffcc075c0160f246e7f16757d226
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478515"
---
# <a name="static-cursors"></a><span data-ttu-id="8ee33-102">静的カーソル</span><span class="sxs-lookup"><span data-stu-id="8ee33-102">Static Cursors</span></span>


<span data-ttu-id="8ee33-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="8ee33-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8ee33-p101">静的カーソルは、カーソルを最初に開いたときの状態の結果セットを常に表示します。実装によって、静的カーソルは読み取り専用または読み取り/書き込みのいずれかで、前方および後方のスクロール機能を提供します。通常、静的カーソルでは、カーソルを開いた後にメンバーシップ、順序、または結果セットの値に加えられた変更を検出しません。静的カーソルは、カーソル自体の更新、削除、および挿入を検出できますが、そのような機能は不要です。</span><span class="sxs-lookup"><span data-stu-id="8ee33-p101">The static cursor always displays the result set as it was when the cursor was first opened. Depending on implementation, static cursors are either read-only or read/write and provide forward and backward scrolling. The static cursor does not usually detect changes made to the membership, order, or values of the result set after the cursor is opened. Static cursors may detect their own updates, deletes, and inserts, although they are not required to do so.</span></span>

<span data-ttu-id="8ee33-p102">静的カーソルが、他の更新、削除、および挿入を検出することはありません。たとえば、静的カーソルが行をフェッチした後、別のアプリケーションがその行を更新したとします。アプリケーションが静的カーソルからその行を再フェッチすると、他のアプリケーションが変更を加えたにもかかわらず、表示される行の値は変わりません。すべての種類のスクロールがサポートされますが、ブックマークのサポートはプロバイダーによって異なります。</span><span class="sxs-lookup"><span data-stu-id="8ee33-p102">Static cursors never detect other updates, deletes, and inserts. For example, suppose a static cursor fetches a row, and another application then updates that row. If the application refetches the row from the static cursor, the values it sees are unchanged, despite the changes made by the other application. All types of scrolling are supported, but providers may or may not support bookmarks.</span></span>

<span data-ttu-id="8ee33-p103">アプリケーションでデータの変更を検出する必要がなく、スクロールが必要な場合は、静的カーソルを選択することをお勧めします。ADO で静的カーソルを使用するように指定するには、 **adOpenStatic** **CursorTypeEnum** を使用します。</span><span class="sxs-lookup"><span data-stu-id="8ee33-p103">If your application does not need to detect data changes and requires scrolling, the static cursor is the best choice. Use the **adOpenStatic** **CursorTypeEnum** to indicate that you want to use a static cursor in ADO.</span></span>

