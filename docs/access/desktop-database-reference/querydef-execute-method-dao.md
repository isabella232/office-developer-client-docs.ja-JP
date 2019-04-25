---
title: QueryDef.Execute メソッド (DAO)
TOCTitle: Execute Method
ms:assetid: ad9e859e-c6fe-496c-a1f2-a000cf4bebcc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821728(v=office.15)
ms:contentKeyID: 48547043
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052884
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 7ef7f61ef632617b8d64a3fd9c34e5887e50065c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302962"
---
# <a name="querydefexecute-method-dao"></a><span data-ttu-id="4cb4b-102">QueryDef.Execute メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="4cb4b-102">QueryDef.Execute Method (DAO)</span></span>

<span data-ttu-id="4cb4b-103">**適用先**: Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="4cb4b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4cb4b-104">指定されたオブジェクトに対して SQL ステートメントを実行します。</span><span class="sxs-lookup"><span data-stu-id="4cb4b-104">Executes an SQL statement on the specified object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cb4b-105">構文</span><span class="sxs-lookup"><span data-stu-id="4cb4b-105">Syntax</span></span>

<span data-ttu-id="4cb4b-106">*式* .Execute (***Options***)</span><span class="sxs-lookup"><span data-stu-id="4cb4b-106">*expression* .Execute(***Options***)</span></span>

<span data-ttu-id="4cb4b-107">*式\*\*\*QueryDef*\* オブジェクトを表す変数。</span><span class="sxs-lookup"><span data-stu-id="4cb4b-107">*expression*  A variable that represents a **QueryDef** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="4cb4b-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4cb4b-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4cb4b-109">名前</span><span class="sxs-lookup"><span data-stu-id="4cb4b-109">Name</span></span></p></th>
<th><p><span data-ttu-id="4cb4b-110">必須/省略可能</span><span class="sxs-lookup"><span data-stu-id="4cb4b-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="4cb4b-111">データ型</span><span class="sxs-lookup"><span data-stu-id="4cb4b-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="4cb4b-112">説明</span><span class="sxs-lookup"><span data-stu-id="4cb4b-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4cb4b-113"><em>オプション</em></span><span class="sxs-lookup"><span data-stu-id="4cb4b-113"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="4cb4b-114">省略可能</span><span class="sxs-lookup"><span data-stu-id="4cb4b-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="4cb4b-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="4cb4b-115"><strong>Variant</strong></span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="4cb4b-116">注釈</span><span class="sxs-lookup"><span data-stu-id="4cb4b-116">Remarks</span></span>

<span data-ttu-id="4cb4b-117">Options には、次の **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** 定数を使用できます。</span><span class="sxs-lookup"><span data-stu-id="4cb4b-117">You can use the following  RecordsetOptionEnum  constants for Options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4cb4b-118">定数</span><span class="sxs-lookup"><span data-stu-id="4cb4b-118">Constant</span></span></p></th>
<th><p><span data-ttu-id="4cb4b-119">説明</span><span class="sxs-lookup"><span data-stu-id="4cb4b-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4cb4b-120"><strong>dbDenyWrite</strong></span><span class="sxs-lookup"><span data-stu-id="4cb4b-120"><strong>dbDenyWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="4cb4b-121">他のユーザーに対して書き込み権限を許可しません (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="4cb4b-121">Denies write permission to other users (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4cb4b-122"><strong>dbInconsistent</strong></span><span class="sxs-lookup"><span data-stu-id="4cb4b-122"><strong>dbInconsistent</strong></span></span></p></td>
<td><p><span data-ttu-id="4cb4b-123">(既定値) 矛盾した更新を実行します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="4cb4b-123">(Default) Executes inconsistent updates (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4cb4b-124"><strong>dbConsistent</strong></span><span class="sxs-lookup"><span data-stu-id="4cb4b-124"><strong>dbConsistent</strong></span></span></p></td>
<td><p><span data-ttu-id="4cb4b-125">一貫性のある更新を実行します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="4cb4b-125">Executes consistent updates (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4cb4b-126"><strong>dbSQLPassThrough</strong></span><span class="sxs-lookup"><span data-stu-id="4cb4b-126"><strong>dbSQLPassThrough</strong></span></span></p></td>
<td><p><span data-ttu-id="4cb4b-127">SQL パススルー クエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="4cb4b-127">Executes an SQL pass-through query.</span></span> <span data-ttu-id="4cb4b-128">このオプションを設定すると、SQL ステートメントが ODBC データベースに渡されて処理されます (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="4cb4b-128">Setting this option passes the SQL statement to an ODBC database for processing (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4cb4b-129"><strong>dbFailOnError</strong></span><span class="sxs-lookup"><span data-stu-id="4cb4b-129"><strong>dbFailOnError</strong></span></span></p></td>
<td><p><span data-ttu-id="4cb4b-130">エラーが発生した場合、更新をロールバックします (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="4cb4b-130">Rolls back updates if an error occurs (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4cb4b-131"><strong>dbSeeChanges</strong></span><span class="sxs-lookup"><span data-stu-id="4cb4b-131"><strong>dbSeeChanges</strong></span></span></p></td>
<td><p><span data-ttu-id="4cb4b-132">編集中のデータが他のユーザーによって変更されている場合、実行時エラーを生成します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="4cb4b-132">Generates a run-time error if another user is changing data you are editing (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4cb4b-133"><strong>dbRunAsync</strong></span><span class="sxs-lookup"><span data-stu-id="4cb4b-133"><strong>dbRunAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="4cb4b-134">クエリを非同期に実行します (ODBCDirect の Connection オブジェクトと QueryDef オブジェクトのみ)。</span><span class="sxs-lookup"><span data-stu-id="4cb4b-134">Executes the query asynchronously (ODBCDirect Connection and QueryDef objects only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4cb4b-135"><strong>dbExecDirect</strong></span><span class="sxs-lookup"><span data-stu-id="4cb4b-135"><strong>dbExecDirect</strong></span></span></p></td>
<td><p><span data-ttu-id="4cb4b-136">最初に SQLPrepare ODBC API 関数を呼び出さずにステートメントを実行します (ODBCDirect Connection および QueryDef オブジェクトのみ)。</span><span class="sxs-lookup"><span data-stu-id="4cb4b-136">Executes the statement without first calling SQLPrepare ODBC API function (ODBCDirect Connection and QueryDef objects only).</span></span></p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> <span data-ttu-id="4cb4b-p102">[!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</span><span class="sxs-lookup"><span data-stu-id="4cb4b-p102">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

> [!NOTE]
> <span data-ttu-id="4cb4b-p103">[!メモ] 定数 **dbConsistent** と **dbInconsistent** は互いに排他的です。1 つの **OpenRecordset** のインスタンスにおいては、どちらか一方を使用できますが、両方を使用することはできません。 **dbConsistent** と **dbInconsistent** の両方を使用すると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="4cb4b-p103">The constants **dbConsistent** and **dbInconsistent** are mutually exclusive. You can use one or the other, but not both in a given instance of **OpenRecordset**. Using both **dbConsistent** and **dbInconsistent** causes an error.</span></span>

<span data-ttu-id="4cb4b-p104">**[Connection](querydef-recordsaffected-property-dao.md)** 、 **[Database](connection-object-dao.md)** 、または **[QueryDef](database-object-dao.md)** オブジェクトの **[RecordsAffected](querydef-object-dao.md)** プロパティを使用して、最後に使用された **[Execute](querydef-execute-method-dao.md)** メソッドによって影響を受けたレコードの数を取得できます。たとえば、アクション クエリの実行時に削除、更新、または挿入されたレコードの数が **RecordsAffected** に格納されます。 **Execute** メソッドを使用してクエリを実行すると、 **QueryDef** オブジェクトの **RecordsAffected** プロパティは、影響を受けたレコードの数に設定されます。</span><span class="sxs-lookup"><span data-stu-id="4cb4b-p104">Use the **[RecordsAffected](querydef-recordsaffected-property-dao.md)** property of the **[Connection](connection-object-dao.md)**, **[Database](database-object-dao.md)**, or **[QueryDef](querydef-object-dao.md)** object to determine the number of records affected by the most recent **[Execute](querydef-execute-method-dao.md)** method. For example, **RecordsAffected** contains the number of records deleted, updated, or inserted when executing an action query. When you use the **Execute** method to run a query, the **RecordsAffected** property of the **QueryDef** object is set to the number of records affected.</span></span>

<span data-ttu-id="4cb4b-p105">Microsoft Access ワークスペースでは、指定した SQL ステートメントの構文が正しく、ユーザーが適切な権限を持っている場合、1 行も変更または削除できなくても、 **Execute** メソッドが失敗することはありません。したがって、 **Execute** メソッドを使って更新または削除のクエリを実行するときは、必ず **dbFailOnError** オプションを指定してください。このオプションを使用すると、影響を受けるレコードの一部がロックされているために更新または削除できない場合、実行時エラーが生成され、既に成功している変更もすべてロールバックされます。</span><span class="sxs-lookup"><span data-stu-id="4cb4b-p105">In a Microsoft Access workspace, if you provide a syntactically correct SQL statement and have the appropriate permissions, the **Execute** method won't fail — even if not a single row can be modified or deleted. Therefore, always use the **dbFailOnError** option when using the **Execute** method to run an update or delete query. This option generates a run-time error and rolls back all successful changes if any of the records affected are locked and can't be updated or deleted.</span></span>

<span data-ttu-id="4cb4b-p106">以前のバージョンの Microsoft Jet データベース エンジンでは、暗黙のトランザクション内に自動的に SQL ステートメントが埋め込まれていました。 **dbFailOnError** を指定して実行したステートメントの一部が失敗した場合は、ステートメント全体がロールバックされました。パフォーマンスを向上するために、バージョン 3.5 以降では、この暗黙のトランザクションが取り除かれました。古いバージョンの DAO コードを更新する場合は、 **Execute** ステートメントの前後で明示的なトランザクションを使用することを検討してください。</span><span class="sxs-lookup"><span data-stu-id="4cb4b-p106">In earlier versions of the Microsoft Jet database engine, SQL statements were automatically embedded in implicit transactions. If part of a statement executed with **dbFailOnError** failed, the entire statement would be rolled back. To improve performance, these implicit transactions were removed starting with version 3.5. If you are updating older DAO code, be sure to consider using explicit transactions around **Execute** statements.</span></span>

<span data-ttu-id="4cb4b-152">Microsoft Access ワークスペース、特にマルチユーザー環境で最高のパフォーマンスを得るには、トランザクション内に **Execute** メソッドをネストします。</span><span class="sxs-lookup"><span data-stu-id="4cb4b-152">For best performance in a Microsoft Access workspace, especially in a multiuser environment, nest the **Execute** method inside a transaction.</span></span> <span data-ttu-id="4cb4b-153">現在の**[Workspace](workspace-object-dao.md)** オブジェクトの **[BeginTrans](workspace-begintrans-method-dao.md)** メソッドを使用し、次に **Execute** メソッドを使用し、最後に **Workspace** の **[CommitTrans](workspace-committrans-method-dao.md)** メソッドを使用してトランザクションを完了します。</span><span class="sxs-lookup"><span data-stu-id="4cb4b-153">Use the BeginTrans method on the current Workspace object, then use the Execute method, and complete the transaction by using the CommitTrans method on the Workspace.</span></span> <span data-ttu-id="4cb4b-154">これにより、変更がディスクに保存され、クエリ実行中に適用されていたロックがすべて解除されます。</span><span class="sxs-lookup"><span data-stu-id="4cb4b-154">This saves changes on disk and frees any locks placed while the query is running.</span></span>

## <a name="example"></a><span data-ttu-id="4cb4b-155">例</span><span class="sxs-lookup"><span data-stu-id="4cb4b-155">Example</span></span>

<span data-ttu-id="4cb4b-p108">この例では、**Execute** メソッドを **QueryDef** オブジェクトから実行する場合と **Database** オブジェクトから実行する場合の両方を示します。このプロシージャを実行するには、ExecuteQueryDef プロシージャおよび PrintOutput プロシージャが必要です。</span><span class="sxs-lookup"><span data-stu-id="4cb4b-p108">This example demonstrates the **Execute** method when run from both a **QueryDef** object and a **Database** object. The ExecuteQueryDef and PrintOutput procedures are required for this procedure to run.</span></span>

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
          Debug.Print "  " & rstTemp!LastName & _ 
             ", " & rstTemp!Country 
          rstTemp.MoveNext 
       Loop 
     
    End Sub 
```

<br/>

<span data-ttu-id="4cb4b-158">次の例は、パラメータ クエリを実行する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="4cb4b-158">The following example shows how to execute a parameter query.</span></span> <span data-ttu-id="4cb4b-159">Parameters コレクションは、クエリが実行される前に myActionQuery クエリの Organization パラメータを設定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="4cb4b-159">The Parameters collection is used to set the Organization parameter of the myActionQuery query before the query is executed.</span></span>

<span data-ttu-id="4cb4b-160">**サンプル コードの提供元:** [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)。</span><span class="sxs-lookup"><span data-stu-id="4cb4b-160">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Public Sub ExecParameterQuery()
    
        Dim dbs As DAO.Database
        Dim qdf As DAO.QueryDef
    
        Set dbs = CurrentDb
        Set qdf = dbs.QueryDefs("myActionQuery")
    
        'Set the value of the QueryDef's parameter
        qdf.Parameters("Organization").Value = "Microsoft"
    
        'Execute the query
        qdf.Execute dbFailOnError
    
        'Clean up
        qdf.Close
        Set qdf = Nothing
        Set dbs = Nothing
    
    End Sub
```
