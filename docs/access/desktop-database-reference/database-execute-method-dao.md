---
title: Database.Execute メソッド (DAO)
TOCTitle: Execute Method
ms:assetid: 9294d530-f70f-e1ed-3990-ce128de4378b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197654(v=office.15)
ms:contentKeyID: 48546378
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1c66e6d3297359b3f3584932d8a1faa5dbee0fd7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476695"
---
# <a name="databaseexecute-method-dao"></a><span data-ttu-id="5d872-102">Database.Execute メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="5d872-102">Database.Execute Method (DAO)</span></span>

<span data-ttu-id="5d872-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="5d872-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5d872-104">指定したオブジェクトのアクション クエリまたは SQL ステートメントを実行します。</span><span class="sxs-lookup"><span data-stu-id="5d872-104">Runs an action query or executes an SQL statement on the specified object.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d872-105">構文</span><span class="sxs-lookup"><span data-stu-id="5d872-105">Syntax</span></span>

<span data-ttu-id="5d872-106">*式*です。(***クエリ\*\*\*\*\*\*のオプション***) を実行します。</span><span class="sxs-lookup"><span data-stu-id="5d872-106">*expression* .Execute(***Query***, ***Options***)</span></span>

<span data-ttu-id="5d872-107">\*式\***データベース**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="5d872-107">*expression* A variable that represents a **Database** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="5d872-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5d872-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5d872-109">名前</span><span class="sxs-lookup"><span data-stu-id="5d872-109">Name</span></span></p></th>
<th><p><span data-ttu-id="5d872-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="5d872-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="5d872-111">データ型</span><span class="sxs-lookup"><span data-stu-id="5d872-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="5d872-112">説明</span><span class="sxs-lookup"><span data-stu-id="5d872-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5d872-113">Query</span><span class="sxs-lookup"><span data-stu-id="5d872-113">Query</span></span></p></td>
<td><p><span data-ttu-id="5d872-114">必須</span><span class="sxs-lookup"><span data-stu-id="5d872-114">Required</span></span></p></td>
<td><p><span data-ttu-id="5d872-115"><strong>文字列型 (String)</strong></span><span class="sxs-lookup"><span data-stu-id="5d872-115"><strong>String</strong></span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d872-116">選択肢</span><span class="sxs-lookup"><span data-stu-id="5d872-116">Options</span></span></p></td>
<td><p><span data-ttu-id="5d872-117">省略可能</span><span class="sxs-lookup"><span data-stu-id="5d872-117">Optional</span></span></p></td>
<td><p><span data-ttu-id="5d872-118"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="5d872-118"><strong>Variant</strong></span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="5d872-119">注釈</span><span class="sxs-lookup"><span data-stu-id="5d872-119">Remarks</span></span>

<span data-ttu-id="5d872-120">**[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** 定数は、次は、オプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="5d872-120">You can use the following **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** constants for options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5d872-121">定数</span><span class="sxs-lookup"><span data-stu-id="5d872-121">Constant</span></span></p></th>
<th><p><span data-ttu-id="5d872-122">説明</span><span class="sxs-lookup"><span data-stu-id="5d872-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5d872-123"><strong>dbDenyWrite</strong></span><span class="sxs-lookup"><span data-stu-id="5d872-123"><strong>dbDenyWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="5d872-124">他のユーザーに対して書き込み権限を許可しません (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="5d872-124">Denies write permission to other users (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d872-125"><strong>組み合わせて</strong></span><span class="sxs-lookup"><span data-stu-id="5d872-125"><strong>dbInconsistent</strong></span></span></p></td>
<td><p><span data-ttu-id="5d872-126">(既定値) 矛盾した更新を実行します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="5d872-126">(Default) Executes inconsistent updates (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d872-127"><strong>指定できます。</strong></span><span class="sxs-lookup"><span data-stu-id="5d872-127"><strong>dbConsistent</strong></span></span></p></td>
<td><p><span data-ttu-id="5d872-128">一貫性のある更新を実行します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="5d872-128">Executes consistent updates (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d872-129"><strong>dbSQLPassThrough</strong></span><span class="sxs-lookup"><span data-stu-id="5d872-129"><strong>dbSQLPassThrough</strong></span></span></p></td>
<td><p><span data-ttu-id="5d872-p101">SQL パススルー クエリを実行します。このオプションを設定すると、SQL ステートメントが ODBC データベースに渡されて処理されます (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="5d872-p101">Executes an SQL pass-through query. Setting this option passes the SQL statement to an ODBC database for processing (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d872-132"><strong>dbFailOnError</strong></span><span class="sxs-lookup"><span data-stu-id="5d872-132"><strong>dbFailOnError</strong></span></span></p></td>
<td><p><span data-ttu-id="5d872-133">エラーが発生した場合、更新をロールバックします (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="5d872-133">Rolls back updates if an error occurs (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d872-134"><strong>dbSeeChanges</strong></span><span class="sxs-lookup"><span data-stu-id="5d872-134"><strong>dbSeeChanges</strong></span></span></p></td>
<td><p><span data-ttu-id="5d872-135">編集中のデータが他のユーザーによって変更されている場合、実行時エラーを生成します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="5d872-135">Generates a run-time error if another user is changing data you are editing (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d872-136"><strong>dbRunAsync</strong></span><span class="sxs-lookup"><span data-stu-id="5d872-136"><strong>dbRunAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="5d872-137">クエリを非同期に実行します (ODBCDirect の Connection オブジェクトと QueryDef オブジェクトのみ)。</span><span class="sxs-lookup"><span data-stu-id="5d872-137">Executes the query asynchronously (ODBCDirect Connection and QueryDef objects only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d872-138"><strong>dbExecDirect</strong></span><span class="sxs-lookup"><span data-stu-id="5d872-138"><strong>dbExecDirect</strong></span></span></p></td>
<td><p><span data-ttu-id="5d872-139">SQLPrepare ODBC API 関数を呼び出さずにステートメントを実行します (ODBCDirect の Connection オブジェクトと QueryDef オブジェクトのみ)。</span><span class="sxs-lookup"><span data-stu-id="5d872-139">Executes the statement without first calling SQLPrepare ODBC API function (ODBCDirect Connection and QueryDef objects only).</span></span></p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> <span data-ttu-id="5d872-p102">[!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</span><span class="sxs-lookup"><span data-stu-id="5d872-p102">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

> [!NOTE]
> <span data-ttu-id="5d872-p103">[!メモ] 定数 **dbConsistent** と **dbInconsistent** は互いに排他的です。1 つの **OpenRecordset** のインスタンスにおいては、どちらか一方を使用できますが、両方を使用することはできません。 **dbConsistent** と **dbInconsistent** の両方を使用すると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="5d872-p103">The constants **dbConsistent** and **dbInconsistent** are mutually exclusive. You can use one or the other, but not both in a given instance of **OpenRecordset**. Using both **dbConsistent** and **dbInconsistent** causes an error.</span></span>

<span data-ttu-id="5d872-p104">**Execute** メソッドはアクション クエリでのみ有効です。別の種類のクエリで **Execute** を使用すると、エラーが発生します。アクション クエリはレコードを返さないので、 **Execute** は **Recordset** を返しません。 **Recordset** が返されない場合は、ODBCDirect ワークスペースで SQL パススルー クエリを実行してもエラーは返されません。</span><span class="sxs-lookup"><span data-stu-id="5d872-p104">The **Execute** method is valid only for action queries. If you use **Execute** with another type of query, an error occurs. Because an action query doesn't return any records, **Execute** doesn't return a **Recordset**. (Executing an SQL pass-through query in an ODBCDirect workspace will not return an error if a **Recordset** isn't returned.)</span></span>

<span data-ttu-id="5d872-p105">**Connection** 、 **Database** 、または **QueryDef** のオブジェクトの **RecordsAffected** プロパティを使用して、最後に使用された **Execute** メソッドによって影響を受けたレコードの数を取得できます。たとえば、アクション クエリの実行時に削除、更新、または挿入されたレコードの数が **RecordsAffected** に格納されます。 **Execute** メソッドを使用してクエリを実行すると、 **QueryDef** オブジェクトの **RecordsAffected** プロパティは、影響を受けたレコードの数に設定されます。</span><span class="sxs-lookup"><span data-stu-id="5d872-p105">Use the **RecordsAffected** property of the **Connection**, **Database**, or **QueryDef** object to determine the number of records affected by the most recent **Execute** method. For example, **RecordsAffected** contains the number of records deleted, updated, or inserted when executing an action query. When you use the **Execute** method to run a query, the **RecordsAffected** property of the **QueryDef** object is set to the number of records affected.</span></span>

<span data-ttu-id="5d872-p106">Microsoft Access ワークスペースでは、指定した SQL ステートメントの構文が正しく、ユーザーが適切な権限を持っている場合、1 行も変更または削除できなくても、 **Execute** メソッドが失敗することはありません。したがって、 **Execute** メソッドを使って更新または削除のクエリを実行するときは、必ず **dbFailOnError** オプションを指定してください。このオプションを使用すると、影響を受けるレコードの一部がロックされているために更新または削除できない場合、実行時エラーが生成され、既に成功している変更もすべてロールバックされます。</span><span class="sxs-lookup"><span data-stu-id="5d872-p106">In a Microsoft Access workspace, if you provide a syntactically correct SQL statement and have the appropriate permissions, the **Execute** method won't fail — even if not a single row can be modified or deleted. Therefore, always use the **dbFailOnError** option when using the **Execute** method to run an update or delete query. This option generates a run-time error and rolls back all successful changes if any of the records affected are locked and can't be updated or deleted.</span></span>

<span data-ttu-id="5d872-p107">以前のバージョンの Microsoft Jet データベース エンジンでは、暗黙のトランザクション内に自動的に SQL ステートメントが埋め込まれていました。 **dbFailOnError** を指定して実行したステートメントの一部が失敗した場合は、ステートメント全体がロールバックされました。パフォーマンスを向上するために、バージョン 3.5 以降では、この暗黙のトランザクションが取り除かれました。古いバージョンの DAO コードを更新する場合は、 **Execute** ステートメントの前後で明示的なトランザクションを使用することを検討してください。</span><span class="sxs-lookup"><span data-stu-id="5d872-p107">In earlier versions of the Microsoft Jet database engine, SQL statements were automatically embedded in implicit transactions. If part of a statement executed with **dbFailOnError** failed, the entire statement would be rolled back. To improve performance, these implicit transactions were removed starting with version 3.5. If you are updating older DAO code, be sure to consider using explicit transactions around **Execute** statements.</span></span>

<span data-ttu-id="5d872-p108">Microsoft Access ワークスペースでのパフォーマンスを最適にする (特にマルチユーザー環境の場合) には、トランザクション内部に **Execute** メソッドをネストします。現在の **Workspace** オブジェクトの **BeginTrans** メソッドを使用し、次に **Execute** メソッドを使用し、最後に **Workspace** の **CommitTrans** メソッドを使用してトランザクションを完了します。これにより、変更がディスクに保存され、クエリ実行中に適用されていたロックがすべて解除されます。</span><span class="sxs-lookup"><span data-stu-id="5d872-p108">For best performance in a Microsoft Access workspace, especially in a multiuser environment, nest the **Execute** method inside a transaction. Use the **BeginTrans** method on the current **Workspace** object, then use the **Execute** method, and complete the transaction by using the **CommitTrans** method on the **Workspace**. This saves changes on disk and frees any locks placed while the query is running.</span></span>

## <a name="example"></a><span data-ttu-id="5d872-162">例</span><span class="sxs-lookup"><span data-stu-id="5d872-162">Example</span></span>

<span data-ttu-id="5d872-p109">この例では、 **Execute** メソッドを **QueryDef** オブジェクトから実行する場合と **Database** オブジェクトから実行する場合の両方を示します。このプロシージャを実行するには、ExecuteQueryDef プロシージャおよび PrintOutput プロシージャが必要です。</span><span class="sxs-lookup"><span data-stu-id="5d872-p109">This example demonstrates the **Execute** method when run from both a **QueryDef** object and a **Database** object. The ExecuteQueryDef and PrintOutput procedures are required for this procedure to run.</span></span>

```vb
    Sub ExecuteX() 
     
     Dim dbsNorthwind As Database 
     Dim strSQLChange As String 
     Dim strSQLRestore As String 
     Dim qdfChange As QueryDef 
     Dim rstEmployees As Recordset 
     Dim errLoop As Error 
     
     ' Define two SQL statements for action queries. 
     strSQLChange = "UPDATE Employees SET Country = " & _ 
     "'United States' WHERE Country = 'USA'" 
     strSQLRestore = "UPDATE Employees SET Country = " & _ 
     "'USA' WHERE Country = 'United States'" 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     ' Create temporary QueryDef object. 
     Set qdfChange = dbsNorthwind.CreateQueryDef("", _ 
     strSQLChange) 
     Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
     "SELECT LastName, Country FROM Employees", _ 
     dbOpenForwardOnly) 
     
     ' Print report of original data. 
     Debug.Print _ 
     "Data in Employees table before executing the query" 
     PrintOutput rstEmployees 
     
     ' Run temporary QueryDef. 
     ExecuteQueryDef qdfChange, rstEmployees 
     
     ' Print report of new data. 
     Debug.Print _ 
     "Data in Employees table after executing the query" 
     PrintOutput rstEmployees 
     
     ' Run action query to restore data. Trap for errors, 
     ' checking the Errors collection if necessary. 
     On Error GoTo Err_Execute 
     dbsNorthwind.Execute strSQLRestore, dbFailOnError 
     On Error GoTo 0 
     
     ' Retrieve the current data by requerying the recordset. 
     rstEmployees.Requery 
     
     ' Print report of restored data. 
     Debug.Print "Data after executing the query " & _ 
     "to restore the original information" 
     PrintOutput rstEmployees 
     
     rstEmployees.Close 
     
     Exit Sub 
     
    Err_Execute: 
     
     ' Notify user of any errors that result from 
     ' executing the query. 
     If DBEngine.Errors.Count > 0 Then 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & vbCr & _ 
     errLoop.Description 
     Next errLoop 
     End If 
     
     Resume Next 
     
    End Sub 
     
    Sub ExecuteQueryDef(qdfTemp As QueryDef, _ 
     rstTemp As Recordset) 
     
     Dim errLoop As Error 
     
     ' Run the specified QueryDef object. Trap for errors, 
     ' checking the Errors collection if necessary. 
     On Error GoTo Err_Execute 
     qdfTemp.Execute dbFailOnError 
     On Error GoTo 0 
     
     ' Retrieve the current data by requerying the recordset. 
     rstTemp.Requery 
     
     Exit Sub 
     
    Err_Execute: 
     
     ' Notify user of any errors that result from 
     ' executing the query. 
     If DBEngine.Errors.Count > 0 Then 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & vbCr & _ 
     errLoop.Description 
     Next errLoop 
     End If 
     
     Resume Next 
     
    End Sub 
     
    Sub PrintOutput(rstTemp As Recordset) 
     
     ' Enumerate Recordset. 
     Do While Not rstTemp.EOF 
     Debug.Print " " & rstTemp!LastName & _ 
     ", " & rstTemp!Country 
     rstTemp.MoveNext 
     Loop 
     
    End Sub
```
