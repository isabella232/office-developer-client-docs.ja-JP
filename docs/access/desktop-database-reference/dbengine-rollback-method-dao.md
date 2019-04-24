---
title: DBEngine (Rollback) メソッド (DAO)
TOCTitle: Rollback Method
ms:assetid: da7e2fe0-c837-7b1e-d35c-98e6cb0a7bbe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835327(v=office.15)
ms:contentKeyID: 48548084
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053424
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 378baa8cd2923366a453a6cf23d51af0ab0df5ee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294205"
---
# <a name="dbenginerollback-method-dao"></a><span data-ttu-id="21b4e-102">DBEngine (Rollback) メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="21b4e-102">DBEngine.Rollback method (DAO)</span></span>


<span data-ttu-id="21b4e-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="21b4e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="21b4e-104">現在のトランザクションを終了し、 **Workspace** オブジェクト内のデータベースを現在のトランザクションが開始された時点の状態に戻します。</span><span class="sxs-lookup"><span data-stu-id="21b4e-104">Ends the current transaction and restores the databases in the **Workspace** object to the state they were in when the current transaction began.</span></span>

## <a name="syntax"></a><span data-ttu-id="21b4e-105">構文</span><span class="sxs-lookup"><span data-stu-id="21b4e-105">Syntax</span></span>

<span data-ttu-id="21b4e-106">*式*。戻す</span><span class="sxs-lookup"><span data-stu-id="21b4e-106">*expression* .Rollback</span></span>

<span data-ttu-id="21b4e-107">\*式\***DBEngine**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="21b4e-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="21b4e-108">注釈</span><span class="sxs-lookup"><span data-stu-id="21b4e-108">Remarks</span></span>

<span data-ttu-id="21b4e-p101">トランザクション メソッドである **BeginTrans**、 **CommitTrans**、および **Rollback** は、 **Workspace** オブジェクトで定義されるセッションの間に行われるトランザクション処理を管理します。これらのメソッドは、1 セッションの間にデータベースに対して行われる一連の変更を 1 つの単位として扱う場合に、 **Workspace** オブジェクトで使用します。</span><span class="sxs-lookup"><span data-stu-id="21b4e-p101">The transaction methods **BeginTrans**, **CommitTrans**, and **Rollback** manage transaction processing during a session defined by a **Workspace** object. You use these methods with a **Workspace** object when you want to treat a series of changes made to the databases in a session as one unit.</span></span>

<span data-ttu-id="21b4e-p102">通常、トランザクションは、複数のテーブル内のレコードを更新し、すべてのテーブルで変更を確実に完了 (コミット) するか、すべてのテーブルで変更を取り消す (ロールバックする) 必要がある場合に、データの整合性を維持するために使用します。たとえば、ある口座から別の口座にある金額を移す必要がある場合、一方の口座からその金額を引き、もう一方の口座にその金額を足します。いずれかの更新が失敗すると、口座の残高が合わなくなります。最初のレコードを更新する前には **BeginTrans** メソッドを使用し、以降の更新が失敗した場合は **Rollback** メソッドを使用してすべての更新を元に戻すことができます。最後のレコードを正しく更新できたら **CommitTrans** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="21b4e-p102">Typically, you use transactions to maintain the integrity of your data when you must both update records in two or more tables and ensure changes are completed (committed) in all tables or none at all (rolled back). For example, if you transfer money from one account to another, you might subtract an amount from one and add the amount to another. If either update fails, the accounts no longer balance. Use the **BeginTrans** method before updating the first record, and then, if any subsequent update fails, you can use the **Rollback** method to undo all of the updates. Use the **CommitTrans** method after you successfully update the last record.</span></span>

> [!NOTE]
> <span data-ttu-id="21b4e-p103">[!メモ] 1 つの **Workspace** オブジェクトでは、トランザクションは常に **Workspace** 全体に対して実行され、1 つの **Connection** オブジェクトまたは **Database** オブジェクトのみに制限されることはありません。 **Workspace** トランザクション内で複数の接続またはデータベースに対して操作を実行した場合、そのトランザクションを解決 (つまり **CommitTrans** メソッドまたは **Rollback** メソッドを使用) すると、そのワークスペース内のすべての接続およびデータベースに対するすべての操作に影響が及びます。</span><span class="sxs-lookup"><span data-stu-id="21b4e-p103">Within one **Workspace** object, transactions are always global to the **Workspace** and aren't limited to only one **Connection** or **Database** object. If you perform operations on more than one connection or database within a **Workspace** transaction, resolving the transaction (that is, using the **CommitTrans** or **Rollback** method) affects all operations on all connections and databases within that workspace.</span></span>

<span data-ttu-id="21b4e-p104">**CommitTrans** を使用した後は、そのトランザクション中に行った変更を取り消すことはできません (トランザクションが別のトランザクションにネストされていて、ネストしているトランザクション自体がロールバックされる場合を除く)。トランザクションをネストする場合は、現在のトランザクションを解決しない限り、ネスト内でそのトランザクションより上のレベルにあるトランザクションを解決できません。</span><span class="sxs-lookup"><span data-stu-id="21b4e-p104">After you use **CommitTrans**, you can't undo changes made during that transaction unless the transaction is nested within another transaction that is itself rolled back. If you nest transactions, you must resolve the current transaction before you can resolve a transaction at a higher level of nesting.</span></span>

<span data-ttu-id="21b4e-120">複数のトランザクションのスコープが重複しており、ネストしていない場合に、それらのトランザクションを同時実行する場合は、別の **Workspace** オブジェクトを作成して、そのオブジェクトで同時トランザクションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="21b4e-120">If you want to have simultaneous transactions with overlapping, non-nested scopes, you can create additional **Workspace** objects to contain the concurrent transactions.</span></span>

<span data-ttu-id="21b4e-121">保留中のトランザクションを解決せずに **Workspace** オブジェクトを閉じると、それらのトランザクションは自動的にロールバックされます。</span><span class="sxs-lookup"><span data-stu-id="21b4e-121">If you close a **Workspace** object without resolving any pending transactions, the transactions are automatically rolled back.</span></span>

<span data-ttu-id="21b4e-122">先に **BeginTrans** メソッドを使用せずに **CommitTrans** メソッドまたは **Rollback** メソッドを使用すると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="21b4e-122">If you use the **CommitTrans** or **Rollback** method without first using the **BeginTrans** method, an error occurs.</span></span>

<span data-ttu-id="21b4e-p105">Microsoft Access ワークスペースで使用される一部の ISAM データベースでは、トランザクションがサポートされておらず、この場合 **Database** オブジェクトまたは **Recordset** オブジェクトの **Transactions** プロパティは **False** です。データベースでトランザクションがサポートされているかどうか確認するには、 **BeginTrans** メソッドを使用する前に **Database** オブジェクトの **Transactions** プロパティを調べます。複数のデータベースを基にした **Recordset** オブジェクトを使用する場合は、 **Recordset** オブジェクトの **Transactions** プロパティを調べます。 **Recordset** 全体が Microsoft Access データベース エンジンのテーブルを基にしている場合は、常にトランザクションを使用できます。しかし、他のデータベース製品によって作成されたテーブルを基にした **Recordset** オブジェクトでは、トランザクションがサポートされていない場合があります。たとえば、Paradox のテーブルを基にした **Recordset** ではトランザクションを使用できません。この場合、 **Transactions** プロパティは **False** です。 **Database** または **Recordset** でトランザクションがサポートされていない場合、トランザクション メソッドは無視され、エラーは発生しません。</span><span class="sxs-lookup"><span data-stu-id="21b4e-p105">Some ISAM databases used in a Microsoft Access workspace may not support transactions, in which case the **Transactions** property of the **Database** object or **Recordset** object is **False**. To make sure the database supports transactions, check the value of the **Transactions** property of the **Database** object before using the **BeginTrans** method. If you are using a **Recordset** object based on more than one database, check the **Transactions** property of the **Recordset** object. If a **Recordset** is based entirely on Microsoft Access database engine tables, you can always use transactions. **Recordset** objects based on tables created by other database products, however, may not support transactions. For example, you can't use transactions in a **Recordset** based on a Paradox table. In this case, the **Transactions** property is **False**. If the **Database** or **Recordset** doesn't support transactions, the methods are ignored and no error occurs.</span></span>

<span data-ttu-id="21b4e-131">ODBC データ ソースに Microsoft Access データベース エンジンを通じてアクセスする場合は、トランザクションをネストできません。</span><span class="sxs-lookup"><span data-stu-id="21b4e-131">You can't nest transactions if you are accessing ODBC data sources through the Microsoft Access database engine.</span></span>

<span data-ttu-id="21b4e-p106">ODBC ワークスペースでは、 **CommitTrans** を使用すると、カーソルが無効になる場合があります。 **Recordset** 内の変更を確認するには、 **Requery** メソッドを使用するか、 **Recordset** を閉じて再度開いてください。</span><span class="sxs-lookup"><span data-stu-id="21b4e-p106">In ODBC workspaces, when you use **CommitTrans** your cursor may no longer be valid. Use the **Requery** method to view the changes in the **Recordset**, or close and re-open the **Recordset**.</span></span>

  - <span data-ttu-id="21b4e-p107">多くの場合、ディスクへのアクセスが必要な操作をトランザクション ブロックとして分離することにより、アプリケーションのパフォーマンスを改善できます。これにより、操作をバッファーに格納できるため、ディスクへのアクセス回数を大幅に削減できる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="21b4e-p107">You can often improve the performance of your application by breaking operations that require disk access into transaction blocks. This buffers your operations and may significantly reduce the number of times a disk is accessed.</span></span>

  - <span data-ttu-id="21b4e-p108">Microsoft Access ワークスペースでは、ワークステーション上の環境変数 TEMP で指定されたディレクトリに保存されたファイルに、トランザクションがログ出力されます。トランザクション ログ ファイルによって TEMP ドライブ上の記憶領域が使い果たされてしまった場合は、データベース エンジンで実行時エラーが発生します。この時点で **CommitTrans** を使用すると、コミットされる操作の数を特定できず、その他の完了していない操作が失われるため、操作を再度実行する必要があります。 **Rollback** メソッドを使用すると、トランザクション ログが解放され、トランザクション内のすべての操作がロールバックされます。</span><span class="sxs-lookup"><span data-stu-id="21b4e-p108">In a Microsoft Access workspace, transactions are logged in a file kept in the directory specified by the TEMP environment variable on the workstation. If the transaction log file exhausts the available storage on your TEMP drive, the database engine triggers a run-time error. At this point, if you use **CommitTrans**, an indeterminate number of operations are committed, but the remaining uncompleted operations are lost, and the operation has to be restarted. Using a **Rollback** method releases the transaction log and rolls back all operations in the transaction.</span></span>

  - <span data-ttu-id="21b4e-140">保留中のトランザクション内の複製の **Recordset** を閉じると、 **Rollback** 操作が暗黙的に実行されます。</span><span class="sxs-lookup"><span data-stu-id="21b4e-140">Closing a clone **Recordset** within a pending transaction will cause an implicit **Rollback** operation.</span></span>

