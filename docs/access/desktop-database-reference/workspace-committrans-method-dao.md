---
title: ワークスペースの CommitTrans メソッド (DAO)
TOCTitle: CommitTrans Method
ms:assetid: e6d129fb-a578-5c79-9c16-6444519f0daf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835985(v=office.15)
ms:contentKeyID: 48548391
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 52af229f03b7ea10510f3e580ba2c4e12784e461
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306035"
---
# <a name="workspacecommittrans-method-dao"></a><span data-ttu-id="76a9b-102">ワークスペースの CommitTrans メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="76a9b-102">Workspace.CommitTrans method (DAO)</span></span>

<span data-ttu-id="76a9b-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="76a9b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="76a9b-104">現在のトランザクションを終了し、変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="76a9b-104">Ends the current transaction and saves the changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="76a9b-105">構文</span><span class="sxs-lookup"><span data-stu-id="76a9b-105">Syntax</span></span>

<span data-ttu-id="76a9b-106">*式*。CommitTrans (***オプション***)</span><span class="sxs-lookup"><span data-stu-id="76a9b-106">*expression* .CommitTrans(***Options***)</span></span>

<span data-ttu-id="76a9b-107">\*式\***Workspace**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="76a9b-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="76a9b-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="76a9b-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="76a9b-109">名前</span><span class="sxs-lookup"><span data-stu-id="76a9b-109">Name</span></span></p></th>
<th><p><span data-ttu-id="76a9b-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="76a9b-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="76a9b-111">データ型</span><span class="sxs-lookup"><span data-stu-id="76a9b-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="76a9b-112">説明</span><span class="sxs-lookup"><span data-stu-id="76a9b-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="76a9b-113"><em>Option</em></span><span class="sxs-lookup"><span data-stu-id="76a9b-113"><em>Option</em></span></span></p></td>
<td><p><span data-ttu-id="76a9b-114">省略可能</span><span class="sxs-lookup"><span data-stu-id="76a9b-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="76a9b-115"><strong>長整数型 (Long)</strong></span><span class="sxs-lookup"><span data-stu-id="76a9b-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="76a9b-p101">Microsoft Access ワークスペースでは、 <strong>CommitTrans</strong> で定数 <strong>dbForceOSFlush</strong> を指定できます。これにより、更新を一時的にキャッシュする代わりに、すべての更新が即座にディスクにフラッシュされます。このオプションを使用しないと、アプリケーション プログラムが <strong>CommitTrans</strong> を呼び出した直後にユーザーに制御が戻り、ユーザーがコンピューターの電源が切ったためにデータがディスクに書き込まれないということが起こり得ます。このオプションを使用すると、アプリケーションのパフォーマンスに影響を与える可能性がありますが、キャッシュされた更新がディスクに保存される前にコンピューターの電源が切れる可能性がある状況においては、このオプションが役立ちます。  </span><span class="sxs-lookup"><span data-stu-id="76a9b-p101">In a Microsoft Access workspace, you can include the <strong>dbForceOSFlush</strong> constant with <strong>CommitTrans</strong>. This forces the database engine to immediately flush all updates to disk, instead of caching them temporarily. Without using this option, a user could get control back immediately after the application program calls <strong>CommitTrans</strong>, turn the computer off, and not have the data written to disk. While using this option may affect your application's performance, it is useful in situations where the computer could be shut off before cached updates are saved to disk.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="76a9b-120">注釈</span><span class="sxs-lookup"><span data-stu-id="76a9b-120">Remarks</span></span>

<span data-ttu-id="76a9b-p102">トランザクション メソッドである **BeginTrans**、 **CommitTrans**、および **Rollback** は、 **Workspace** オブジェクトで定義されるセッションの間に行われるトランザクション処理を管理します。これらのメソッドは、1 セッションの間にデータベースに対して行われる一連の変更を 1 つの単位として扱う場合に、 **Workspace** オブジェクトで使用します。</span><span class="sxs-lookup"><span data-stu-id="76a9b-p102">The transaction methods **BeginTrans**, **CommitTrans**, and **Rollback** manage transaction processing during a session defined by a **Workspace** object. You use these methods with a **Workspace** object when you want to treat a series of changes made to the databases in a session as one unit.</span></span>

<span data-ttu-id="76a9b-p103">通常、トランザクションは、複数のテーブル内のレコードを更新し、すべてのテーブルで変更を確実に完了 (コミット) するか、すべてのテーブルで変更を取り消す (ロールバックする) 必要がある場合に、データの整合性を維持するために使用します。たとえば、ある口座から別の口座にある金額を移す必要がある場合、一方の口座からその金額を引き、もう一方の口座にその金額を足します。いずれかの更新が失敗すると、口座の残高が合わなくなります。最初のレコードを更新する前には **BeginTrans** メソッドを使用し、以降の更新が失敗した場合は **Rollback** メソッドを使用してすべての更新を元に戻すことができます。最後のレコードを正しく更新できたら **CommitTrans** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="76a9b-p103">Typically, you use transactions to maintain the integrity of your data when you must both update records in two or more tables and ensure changes are completed (committed) in all tables or none at all (rolled back). For example, if you transfer money from one account to another, you might subtract an amount from one and add the amount to another. If either update fails, the accounts no longer balance. Use the **BeginTrans** method before updating the first record, and then, if any subsequent update fails, you can use the **Rollback** method to undo all of the updates. Use the **CommitTrans** method after you successfully update the last record.</span></span>

> [!NOTE]
> <span data-ttu-id="76a9b-p104">[!メモ] 1 つの **Workspace** オブジェクトでは、トランザクションは常に **Workspace** 全体に対して実行され、1 つの **Connection** オブジェクトまたは **Database** オブジェクトのみに制限されることはありません。 **Workspace** トランザクション内で複数の接続またはデータベースに対して操作を実行した場合、そのトランザクションを解決 (つまり **CommitTrans** メソッドまたは **Rollback** メソッドを使用) すると、そのワークスペース内のすべての接続およびデータベースに対するすべての操作に影響が及びます。</span><span class="sxs-lookup"><span data-stu-id="76a9b-p104">Within one **Workspace** object, transactions are always global to the **Workspace** and aren't limited to only one **Connection** or **Database** object. If you perform operations on more than one connection or database within a **Workspace** transaction, resolving the transaction (that is, using the **CommitTrans** or **Rollback** method) affects all operations on all connections and databases within that workspace.</span></span>

<span data-ttu-id="76a9b-p105">**CommitTrans** を使用した後は、そのトランザクション中に行った変更を取り消すことはできません (トランザクションが別のトランザクションにネストされていて、ネストしているトランザクション自体がロールバックされる場合を除く)。トランザクションをネストする場合は、現在のトランザクションを解決しない限り、ネスト内でそのトランザクションより上のレベルにあるトランザクションを解決できません。</span><span class="sxs-lookup"><span data-stu-id="76a9b-p105">After you use **CommitTrans**, you can't undo changes made during that transaction unless the transaction is nested within another transaction that is itself rolled back. If you nest transactions, you must resolve the current transaction before you can resolve a transaction at a higher level of nesting.</span></span>

<span data-ttu-id="76a9b-132">複数のトランザクションのスコープが重複しており、ネストしていない場合に、それらのトランザクションを同時実行する場合は、別の **Workspace** オブジェクトを作成して、そのオブジェクトで同時トランザクションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="76a9b-132">If you want to have simultaneous transactions with overlapping, non-nested scopes, you can create additional **Workspace** objects to contain the concurrent transactions.</span></span>

<span data-ttu-id="76a9b-133">保留中のトランザクションを解決せずに **Workspace** オブジェクトを閉じると、それらのトランザクションは自動的にロールバックされます。</span><span class="sxs-lookup"><span data-stu-id="76a9b-133">If you close a **Workspace** object without resolving any pending transactions, the transactions are automatically rolled back.</span></span>

<span data-ttu-id="76a9b-134">先に **BeginTrans** メソッドを使用せずに **CommitTrans** メソッドまたは **Rollback** メソッドを使用すると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="76a9b-134">If you use the **CommitTrans** or **Rollback** method without first using the **BeginTrans** method, an error occurs.</span></span>

<span data-ttu-id="76a9b-135">Microsoft Access ワークスペースで使用される一部の ISAM データベースでは、トランザクションがサポートされておらず、この場合 **Database** オブジェクトまたは **Recordset** オブジェクトの **Transactions** プロパティは **False** です。</span><span class="sxs-lookup"><span data-stu-id="76a9b-135">Some ISAM databases used in a Microsoft Access workspace may not support transactions, in which case the **Transactions** property of the **Database** object or **Recordset** object is **False**.</span></span> <span data-ttu-id="76a9b-136">データベースでトランザクションがサポートされているかどうか確認するには、 **BeginTrans** メソッドを使用する前に **Database** オブジェクトの **Transactions** プロパティを調べます。</span><span class="sxs-lookup"><span data-stu-id="76a9b-136">To make sure the database supports transactions, check the value of the **Transactions** property of the **Database** object before using the **BeginTrans** method.</span></span> <span data-ttu-id="76a9b-137">複数のデータベースを基にした **Recordset** オブジェクトを使用する場合は、 **Recordset** オブジェクトの **Transactions** プロパティを調べます。</span><span class="sxs-lookup"><span data-stu-id="76a9b-137">If you are using a **Recordset** object based on more than one database, check the **Transactions** property of the **Recordset** object.</span></span> 

<span data-ttu-id="76a9b-138">**Recordset** 全体が Microsoft Access データベース エンジンのテーブルを基にしている場合は、常にトランザクションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="76a9b-138">If a **Recordset** is based entirely on Microsoft Access database engine tables, you can always use transactions.</span></span> <span data-ttu-id="76a9b-139">しかし、他のデータベース製品によって作成されたテーブルを基にした **Recordset** オブジェクトでは、トランザクションがサポートされていない場合があります。</span><span class="sxs-lookup"><span data-stu-id="76a9b-139">**Recordset** objects based on tables created by other database products, however, may not support transactions.</span></span> <span data-ttu-id="76a9b-140">たとえば、Paradox のテーブルを基にした **Recordset** ではトランザクションを使用できません。</span><span class="sxs-lookup"><span data-stu-id="76a9b-140">For example, you can't use transactions in a **Recordset** based on a Paradox table.</span></span> <span data-ttu-id="76a9b-141">この場合、 **Transactions** プロパティは **False** です。</span><span class="sxs-lookup"><span data-stu-id="76a9b-141">In this case, the **Transactions** property is **False**.</span></span> <span data-ttu-id="76a9b-142">**Database** または **Recordset** でトランザクションがサポートされていない場合、トランザクション メソッドは無視され、エラーは発生しません。</span><span class="sxs-lookup"><span data-stu-id="76a9b-142">If the **Database** or **Recordset** doesn't support transactions, the methods are ignored and no error occurs.</span></span>

<span data-ttu-id="76a9b-143">ODBC データ ソースに Microsoft Access データベース エンジンを通じてアクセスする場合は、トランザクションをネストできません。</span><span class="sxs-lookup"><span data-stu-id="76a9b-143">You can't nest transactions if you are accessing ODBC data sources through the Microsoft Access database engine.</span></span>

<span data-ttu-id="76a9b-p108">ODBC ワークスペースでは、 **CommitTrans** を使用すると、カーソルが無効になる場合があります。 **Recordset** 内の変更を確認するには、 **Requery** メソッドを使用するか、 **Recordset** を閉じて再度開いてください。</span><span class="sxs-lookup"><span data-stu-id="76a9b-p108">In ODBC workspaces, when you use **CommitTrans** your cursor may no longer be valid. Use the **Requery** method to view the changes in the **Recordset**, or close and re-open the **Recordset**.</span></span>

> [!NOTE]
> - <span data-ttu-id="76a9b-p109">多くの場合、ディスクへのアクセスが必要な操作をトランザクション ブロックとして分離することにより、アプリケーションのパフォーマンスを改善できます。これにより、操作をバッファーに格納できるため、ディスクへのアクセス回数を大幅に削減できる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="76a9b-p109">You can often improve the performance of your application by breaking operations that require disk access into transaction blocks. This buffers your operations and may significantly reduce the number of times a disk is accessed.</span></span>
> - <span data-ttu-id="76a9b-p110">Microsoft Access ワークスペースでは、ワークステーション上の環境変数 TEMP で指定されたディレクトリに保存されたファイルに、トランザクションがログ出力されます。トランザクション ログ ファイルによって TEMP ドライブ上の記憶領域が使い果たされてしまった場合は、データベース エンジンで実行時エラーが発生します。この時点で **CommitTrans** を使用すると、コミットされる操作の数を特定できず、その他の完了していない操作が失われるため、操作を再度実行する必要があります。 **Rollback** メソッドを使用すると、トランザクション ログが解放され、トランザクション内のすべての操作がロールバックされます。</span><span class="sxs-lookup"><span data-stu-id="76a9b-p110">In a Microsoft Access workspace, transactions are logged in a file kept in the directory specified by the TEMP environment variable on the workstation. If the transaction log file exhausts the available storage on your TEMP drive, the database engine triggers a run-time error. At this point, if you use **CommitTrans**, an indeterminate number of operations are committed, but the remaining uncompleted operations are lost, and the operation has to be restarted. Using a **Rollback** method releases the transaction log and rolls back all operations in the transaction.</span></span>
> - <span data-ttu-id="76a9b-152">確定していないトランザクション内で複製の **Recordset** を閉じると、暗黙の **Rollback** 操作が発生します。</span><span class="sxs-lookup"><span data-stu-id="76a9b-152">Closing a clone **Recordset** within a pending transaction will cause an implicit **Rollback** operation.</span></span>

## <a name="example"></a><span data-ttu-id="76a9b-153">例</span><span class="sxs-lookup"><span data-stu-id="76a9b-153">Example</span></span>

<span data-ttu-id="76a9b-154">次の例は、DAO (Data Access Objects) ワークスペース内でトランザクションを使用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="76a9b-154">The following example shows how to use a transaction in a Data Access Objects (DAO) workspace.</span></span>

<span data-ttu-id="76a9b-155">**サンプル コードの提供元:** [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)。</span><span class="sxs-lookup"><span data-stu-id="76a9b-155">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>


```vb
    Public Sub TransferFunds()
        Dim wrk As DAO.Workspace
        Dim dbC As DAO.Database
        Dim dbX As DAO.Database
        
        Set wrk = DBEngine(0)
        Set dbC = CurrentDb
        Set dbX = wrk.OpenDatabase("e:\books\acc2007vba\myDB.accdb")
        
        On Error GoTo trans_Err
        
        'Begin the transaction
        
        wrk.BeginTrans
        
        'Withdraw funds from one account table
        dbC.Execute "INSERT INTO tblAccounts ( Amount, Txn, TxnDate ) SELECT -20, 'DEBIT', Date()", dbFailOnError
    
        'Deposit funds into another account table
        dbX.Execute "INSERT INTO tblAccounts ( Amount, Txn, TxnDate ) SELECT 20, 'CREDIT', Date()", dbFailOnError
        
        'Commit the transaction
        wrk.CommitTrans dbForceOSFlush
        
    trans_Exit:
        'Clean up
        wrk.Close
        Set dbC = Nothing
        Set dbX = Nothing
        Set wrk = Nothing
        Exit Sub
        
    trans_Err:
        'Roll back the transaction
        wrk.Rollback
        Resume trans_Exit
        
    End Sub
```
