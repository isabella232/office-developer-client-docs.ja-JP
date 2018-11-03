---
title: 動的カーソル (デスクトップ データベース参照のアクセス)
TOCTitle: Dynamic cursors
ms:assetid: ae599d86-6b89-6103-fda1-c899a6138e1d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249823(v=office.15)
ms:contentKeyID: 48547068
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 63c67e028eaa478a2d348bd7c4dc4e945b3256a6
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947155"
---
# <a name="dynamic-cursors"></a><span data-ttu-id="6d058-102">動的カーソル</span><span class="sxs-lookup"><span data-stu-id="6d058-102">Dynamic cursors</span></span>


<span data-ttu-id="6d058-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="6d058-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6d058-p101">動的カーソルは、結果セット内の行に対して加えられる変更を、それがカーソルの内側から行われたのか、カーソルの外側の他のユーザーによって行われたのかにかかわらず、すべて検出します。すべてのユーザーが実行したすべての挿入、更新、および削除のステートメントは、このカーソルを通じて確認できます。動的カーソルは、カーソルが開かれた後に結果セットに対して加えられた行、順序、および値の変更を、すべて検出できます。カーソルの外側で行われた更新は、コミットされるまで表示されません (ただし、カーソルのトランザクション分離レベルが "uncommitted" に設定されている場合を除きます)。</span><span class="sxs-lookup"><span data-stu-id="6d058-p101">Dynamic cursors detect all changes made to the rows in the result set, regardless of whether the changes occur from inside the cursor or by other users outside the cursor. All insert, update, and delete statements made by all users are visible through the cursor. The dynamic cursor can detect any changes made to the rows, order, and values in the result set after the cursor is opened. Updates made outside the cursor are not visible until they are committed (unless the cursor transaction isolation level is set to "uncommitted").</span></span>

<span data-ttu-id="6d058-p102">たとえば、カーソルが 2 つの行と他のアプリケーションをフェッチし、その後それらの行のうち 1 つを更新し、もう 1 つを削除した場合を考えてみます。その後、動的カーソルがこれらの行をフェッチすると、削除された行は検出されませんが、更新された行の新しい値は表示されます。</span><span class="sxs-lookup"><span data-stu-id="6d058-p102">For example, suppose a dynamic cursor fetches two rows and another application, and then updates one of those rows and deletes the other. If the dynamic cursor then fetches those rows, it will not find the deleted row, but it will display the new values for the updated row.</span></span>

<span data-ttu-id="6d058-p103">動的カーソルは、他のユーザーが同時に行った更新操作を、アプリケーションですべて検出する必要がある場合に便利です。ADO で動的カーソルを使用することを示すには、 **adOpenDynamic** **CursorTypeEnum** を使用します。</span><span class="sxs-lookup"><span data-stu-id="6d058-p103">The dynamic cursor is a good choice if your application must detect all concurrent updates made by other users. Use the **adOpenDynamic** **CursorTypeEnum** to indicate that you want to use a dynamic cursor in ADO.</span></span>

<span data-ttu-id="6d058-112">[前方のみカーソル](forward-only-cursors.md) | [静的カーソル](static-cursors.md) | [キーセット カーソル](keyset-cursors.md)</span><span class="sxs-lookup"><span data-stu-id="6d058-112">[Forward-Only Cursors](forward-only-cursors.md) | [Static Cursors](static-cursors.md) | [Keyset Cursors](keyset-cursors.md)</span></span>

