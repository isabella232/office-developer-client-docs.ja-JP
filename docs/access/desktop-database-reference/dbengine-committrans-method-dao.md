---
title: DBEngine.CommitTrans メソッド (DAO)
TOCTitle: CommitTrans Method
ms:assetid: 0c9d345f-13ff-7fe6-789d-fbdb43fa54b8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845171(v=office.15)
ms:contentKeyID: 48543197
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 530f638cbf996d84b476f1d9cf259f6ab444978f
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996910"
---
# <a name="dbenginecommittrans-method-dao"></a><span data-ttu-id="1c4af-102">DBEngine.CommitTrans メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="1c4af-102">DBEngine.CommitTrans method (DAO)</span></span>


<span data-ttu-id="1c4af-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="1c4af-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1c4af-104">現在のトランザクションを終了し、変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="1c4af-104">Ends the current transaction and saves the changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c4af-105">構文</span><span class="sxs-lookup"><span data-stu-id="1c4af-105">Syntax</span></span>

<span data-ttu-id="1c4af-106">*式*です。CommitTrans (***オプション***)</span><span class="sxs-lookup"><span data-stu-id="1c4af-106">*expression* .CommitTrans(***Option***)</span></span>

<span data-ttu-id="1c4af-107">\*式\***DBEngine**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="1c4af-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="1c4af-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1c4af-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1c4af-109">名前</span><span class="sxs-lookup"><span data-stu-id="1c4af-109">Name</span></span></p></th>
<th><p><span data-ttu-id="1c4af-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="1c4af-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="1c4af-111">データ型</span><span class="sxs-lookup"><span data-stu-id="1c4af-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="1c4af-112">説明</span><span class="sxs-lookup"><span data-stu-id="1c4af-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1c4af-113"><em>Option</em></span><span class="sxs-lookup"><span data-stu-id="1c4af-113"><em>Option</em></span></span></p></td>
<td><p><span data-ttu-id="1c4af-114">省略可能</span><span class="sxs-lookup"><span data-stu-id="1c4af-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="1c4af-115"><strong>長整数型 (Long)</strong></span><span class="sxs-lookup"><span data-stu-id="1c4af-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="1c4af-p101">Microsoft Access ワークスペースでは、 <strong>CommitTrans</strong> で定数 <strong>dbForceOSFlush</strong> を指定できます。これにより、更新を一時的にキャッシュする代わりに、すべての更新が即座にディスクにフラッシュされます。このオプションを使用しないと、アプリケーション プログラムが <strong>CommitTrans</strong> を呼び出した直後にユーザーに制御が戻り、ユーザーがコンピューターの電源が切ったためにデータがディスクに書き込まれないということが起こり得ます。このオプションを使用すると、アプリケーションのパフォーマンスに影響を与える可能性がありますが、キャッシュされた更新がディスクに保存される前にコンピューターの電源が切れる可能性がある状況においては、このオプションが役立ちます。  </span><span class="sxs-lookup"><span data-stu-id="1c4af-p101">In a Microsoft Access workspace, you can include the <strong>dbForceOSFlush</strong> constant with <strong>CommitTrans</strong>. This forces the database engine to immediately flush all updates to disk, instead of caching them temporarily. Without using this option, a user could get control back immediately after the application program calls <strong>CommitTrans</strong>, turn the computer off, and not have the data written to disk. While using this option may affect your application's performance, it is useful in situations where the computer could be shut off before cached updates are saved to disk.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="1c4af-120">注釈</span><span class="sxs-lookup"><span data-stu-id="1c4af-120">Remarks</span></span>

<span data-ttu-id="1c4af-p102">トランザクションのメソッド **BeginTrans**、 **CommitTrans**、および **Rollback** は、 **Workspace** オブジェクトによって定義されたセッション中のトランザクション処理を管理します。これらのメソッドを **Workspace** オブジェクトで使用すると、1 つのセッション中にデータベースに対して行われた一連の変更を 1 つの単位として扱うことができます。</span><span class="sxs-lookup"><span data-stu-id="1c4af-p102">The transaction methods **BeginTrans**, **CommitTrans**, and **Rollback** manage transaction processing during a session defined by a **Workspace** object. You use these methods with a **Workspace** object when you want to treat a series of changes made to the databases in a session as one unit.</span></span>

<span data-ttu-id="1c4af-p103">一般に、2 つ以上のテーブルのレコードを更新する必要があり、かつ変更がすべてのテーブルで完了する (コミットされる) か変更が一切行われない (ロールバックされる) ようにする必要がある場合、データの整合性を保つためにトランザクションが使用されます。たとえば、ある口座から別の口座に送金する場合は、一方の口座から金額を減らし、その金額をもう一方の口座に加算します。どちらか一方の更新が失敗すると口座の残高が合わなくなります。最初のレコードを更新する前に **BeginTrans** メソッドを使用し、以降の更新が 1 つでも失敗した場合は、 **Rollback** メソッドを使用してすべての更新を取り消すことができます。最後のレコードが正常に更新された後に **CommitTrans** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="1c4af-p103">Typically, you use transactions to maintain the integrity of your data when you must both update records in two or more tables and ensure changes are completed (committed) in all tables or none at all (rolled back). For example, if you transfer money from one account to another, you might subtract an amount from one and add the amount to another. If either update fails, the accounts no longer balance. Use the **BeginTrans** method before updating the first record, and then, if any subsequent update fails, you can use the **Rollback** method to undo all of the updates. Use the **CommitTrans** method after you successfully update the last record.</span></span>

> [!NOTE]
> <span data-ttu-id="1c4af-p104">[!メモ] 1 つの **Workspace** オブジェクト内では、トランザクションは **Workspace** に対して常にグローバルに適用され、1 つの **Connection** オブジェクトや **Database** オブジェクトに制限されることはありません。 **Workspace** の 1 つのトランザクション内の複数の接続またはデータベースに対して操作を実行する場合は、そのトランザクションを解決 (つまり、 **CommitTrans** メソッドまたは **Rollback** メソッドを使用) することにより、そのワークスペース内のすべての接続およびデータベースに対するすべての操作が影響を受けます。</span><span class="sxs-lookup"><span data-stu-id="1c4af-p104">Within one **Workspace** object, transactions are always global to the **Workspace** and aren't limited to only one **Connection** or **Database** object. If you perform operations on more than one connection or database within a **Workspace** transaction, resolving the transaction (that is, using the **CommitTrans** or **Rollback** method) affects all operations on all connections and databases within that workspace.</span></span>

<span data-ttu-id="1c4af-p105">**CommitTrans** を使用した後は、そのトランザクション中に行った変更を取り消すことはできません (トランザクションが別のトランザクションにネストされていて、ネストしているトランザクション自体がロールバックされる場合を除く)。トランザクションをネストする場合は、現在のトランザクションを解決しない限り、ネスト内でそのトランザクションより上のレベルにあるトランザクションを解決できません。</span><span class="sxs-lookup"><span data-stu-id="1c4af-p105">After you use **CommitTrans**, you can't undo changes made during that transaction unless the transaction is nested within another transaction that is itself rolled back. If you nest transactions, you must resolve the current transaction before you can resolve a transaction at a higher level of nesting.</span></span>

<span data-ttu-id="1c4af-132">部分的に重なり、ネストしていない適用範囲を持つ同時トランザクションを定義するには、同時トランザクションを格納するための追加の **Workspace** オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="1c4af-132">If you want to have simultaneous transactions with overlapping, non-nested scopes, you can create additional **Workspace** objects to contain the concurrent transactions.</span></span>

<span data-ttu-id="1c4af-133">確定していないトランザクションを解決せずに **Workspace** オブジェクトを閉じた場合、すべてのトランザクションが自動的にロールバックされます。</span><span class="sxs-lookup"><span data-stu-id="1c4af-133">If you close a **Workspace** object without resolving any pending transactions, the transactions are automatically rolled back.</span></span>

<span data-ttu-id="1c4af-134">最初に **BeginTrans** メソッドを使用せずに **CommitTrans** メソッドまたは **Rollback** メソッドを使用すると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="1c4af-134">If you use the **CommitTrans** or **Rollback** method without first using the **BeginTrans** method, an error occurs.</span></span>

<span data-ttu-id="1c4af-p106">Microsoft Access ワークスペースで使用される一部の ISAM データベースはトランザクションをサポートしていない場合があります ( **Database** オブジェクトまたは **Recordset** オブジェクトの **Transactions** プロパティが **False**)。データベースでトランザクションがサポートされていることを確認するには、 **BeginTrans** メソッドを使用する前に **Database** オブジェクトの **Transactions** プロパティの値を調べます。複数のデータベースに基づく **Recordset** オブジェクトを使用している場合は、 **Recordset** オブジェクトの **Transactions** プロパティを調べます。 **Recordset** が Microsoft Access データベース エンジンのテーブルのみに基づいている場合は、トランザクションを使用できます。一方、他のデータベース製品によって作成されたテーブルに基づく **Recordset** オブジェクトの場合は、トランザクションをサポートしていないことがあります。たとえば、Paradox テーブルに基づく **Recordset** では、トランザクションを使用できません。この場合、 **Transactions** プロパティは **False** です。 **Database** または **Recordset** がトランザクションをサポートしていない場合、メソッドは無視され、エラーは発生しません。</span><span class="sxs-lookup"><span data-stu-id="1c4af-p106">Some ISAM databases used in a Microsoft Access workspace may not support transactions, in which case the **Transactions** property of the **Database** object or **Recordset** object is **False**. To make sure the database supports transactions, check the value of the **Transactions** property of the **Database** object before using the **BeginTrans** method. If you are using a **Recordset** object based on more than one database, check the **Transactions** property of the **Recordset** object. If a **Recordset** is based entirely on Microsoft Access database engine tables, you can always use transactions. **Recordset** objects based on tables created by other database products, however, may not support transactions. For example, you can't use transactions in a **Recordset** based on a Paradox table. In this case, the **Transactions** property is **False**. If the **Database** or **Recordset** doesn't support transactions, the methods are ignored and no error occurs.</span></span>

<span data-ttu-id="1c4af-143">Microsoft Access データベース エンジンを通じて ODBC データ ソースにアクセスする場合は、トランザクションをネストできません。</span><span class="sxs-lookup"><span data-stu-id="1c4af-143">You can't nest transactions if you are accessing ODBC data sources through the Microsoft Access database engine.</span></span>

<span data-ttu-id="1c4af-p107">ODBC ワークスペースでは、 **CommitTrans** を使用すると、カーソルが無効になることがあります。 **Requery** メソッドを使って **Recordset** 内の変更を確認するか、 **Recordset** をいったん閉じて、開き直してください。</span><span class="sxs-lookup"><span data-stu-id="1c4af-p107">In ODBC workspaces, when you use **CommitTrans** your cursor may no longer be valid. Use the **Requery** method to view the changes in the **Recordset**, or close and re-open the **Recordset**.</span></span>


> [!NOTE]
> - <span data-ttu-id="1c4af-p108">多くの場合、ディスクへのアクセスを必要とする操作をトランザクション ブロックに分割することにより、アプリケーションのパフォーマンスを向上できます。この場合、操作がバッファーされるので、ディスクへのアクセス回数が大幅に減ります。</span><span class="sxs-lookup"><span data-stu-id="1c4af-p108">You can often improve the performance of your application by breaking operations that require disk access into transaction blocks. This buffers your operations and may significantly reduce the number of times a disk is accessed.</span></span>
> - <span data-ttu-id="1c4af-p109">Microsoft Access ワークスペースでは、ワークステーション上の TEMP 環境変数で指定されたディレクトリ内にあるファイルに、トランザクション ログが記録されます。TEMP ドライブ上の使用可能な記憶域がトランザクション ログ ファイルによって使い尽くされた場合、実行時エラーが発生します。この時点で **CommitTrans** を使用すると、一部の操作はコミットされますが、残りの未完了の操作は失われるため、操作をやり直す必要があります。 **Rollback** メソッドを使用すると、トランザクション ログが解放され、そのトランザクション内のすべての操作がロールバックされます。</span><span class="sxs-lookup"><span data-stu-id="1c4af-p109">In a Microsoft Access workspace, transactions are logged in a file kept in the directory specified by the TEMP environment variable on the workstation. If the transaction log file exhausts the available storage on your TEMP drive, the database engine triggers a run-time error. At this point, if you use **CommitTrans**, an indeterminate number of operations are committed, but the remaining uncompleted operations are lost, and the operation has to be restarted. Using a **Rollback** method releases the transaction log and rolls back all operations in the transaction.</span></span>
> - <span data-ttu-id="1c4af-152">確定していないトランザクション内で複製の **Recordset** を閉じると、暗黙の **Rollback** 操作が発生します。</span><span class="sxs-lookup"><span data-stu-id="1c4af-152">Closing a clone **Recordset** within a pending transaction will cause an implicit **Rollback** operation.</span></span>


