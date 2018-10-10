---
title: トランザクションを制御する
TOCTitle: Controlling Transactions
ms:assetid: 21a9f055-6907-3818-e232-21e579cc67b7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248994(v=office.15)
ms:contentKeyID: 48543685
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b70e6586e17286f4f7a13417d0901f1250635631
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479411"
---
# <a name="controlling-transactions"></a><span data-ttu-id="e0819-102">トランザクションを制御する</span><span class="sxs-lookup"><span data-stu-id="e0819-102">Controlling Transactions</span></span>


<span data-ttu-id="e0819-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="e0819-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e0819-104">*トランザクション*では、先頭と末尾の一連の接続の両端でデータ アクセス操作を区切ります。</span><span class="sxs-lookup"><span data-stu-id="e0819-104">A *transaction* delimits the beginning and end of a series of data access operations that transpire across a connection.</span></span> <span data-ttu-id="e0819-105">トランザクションの機能によって、データ ソース、**接続**オブジェクトも使用するを作成し、トランザクションを管理できます。</span><span class="sxs-lookup"><span data-stu-id="e0819-105">Subject to the transactional capabilities of your data source, the **Connection** object also allows you to create and manage transactions.</span></span> <span data-ttu-id="e0819-106">たとえば、Microsoft SQL Server 2000 上のデータベースにアクセスするには、Microsoft OLE DB プロバイダーの SQL Server を使用して、作成できますを実行するコマンドの複数の入れ子になったトランザクション。</span><span class="sxs-lookup"><span data-stu-id="e0819-106">For example, using the Microsoft OLE DB Provider for SQL Server to access a database on Microsoft SQL Server 2000, you can create multiple nested transactions for the commands you execute.</span></span>

<span data-ttu-id="e0819-107">ADO では、トランザクション内の操作によって発生するデータ ソースの変更が、すべて正常に実行されるか、まったく実行されないかのいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="e0819-107">ADO ensures that changes to a data source resulting from operations in a transaction occur successfully together or not at all.</span></span>

<span data-ttu-id="e0819-p102">トランザクションが取り消されるか、その操作のうちいずれかが失敗した場合、最終的には、トランザクション内の操作がまったく発生しなかったときと同じ結果になります。データ ソースは、トランザクションの開始前と同じ状態のままです。</span><span class="sxs-lookup"><span data-stu-id="e0819-p102">If you cancel the transaction, or if one of its operations fails, the ultimate result will be as if none of the operations in the transaction occurred. The data source will remain as it was before the transaction began.</span></span>

<span data-ttu-id="e0819-110">ADO のオブジェクト モデルでは、トランザクションは明示的に定義されていませんが、**Connection** オブジェクトの一連のメソッド (**BeginTrans**、**CommitTrans**、および **RollbackTrans**) として表現されています。</span><span class="sxs-lookup"><span data-stu-id="e0819-110">The ADO object model does not explicitly include transactions, but represents them with a set of **Connection** object methods (**BeginTrans**, **CommitTrans**, and **RollbackTrans**).</span></span>

<span data-ttu-id="e0819-111">トランザクションの詳細については、「[5 章: データを更新し、保存する](chapter-5-updating-and-persisting-data.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e0819-111">For more information about transactions, see [Chapter 5: Updating and Persisting Data](chapter-5-updating-and-persisting-data.md).</span></span>

