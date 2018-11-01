---
title: QueryDef.SQL プロパティ (DAO)
TOCTitle: SQL Property
ms:assetid: 16446789-c8be-bff0-eddd-b5f6a8530128
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845522(v=office.15)
ms:contentKeyID: 48543429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053054
f1_categories:
- Office.Version=v15
ms.openlocfilehash: a8e33f1a22e1ffd6dffbb67b8bafd5fae78f39c6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881616"
---
# <a name="querydefsql-property-dao"></a><span data-ttu-id="fe750-102">QueryDef.SQL プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="fe750-102">QueryDef.SQL Property (DAO)</span></span>

<span data-ttu-id="fe750-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="fe750-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fe750-104">**[QueryDef](querydef-object-dao.md)** オブジェクトが実行するクエリを定義する SQL ステートメントを設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="fe750-104">Sets or returns the SQL statement that defines the query executed by a **[QueryDef](querydef-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe750-105">構文</span><span class="sxs-lookup"><span data-stu-id="fe750-105">Syntax</span></span>

<span data-ttu-id="fe750-106">*式*です。SQL</span><span class="sxs-lookup"><span data-stu-id="fe750-106">*expression* .SQL</span></span>

<span data-ttu-id="fe750-107">\*式\***クエリ定義**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="fe750-107">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe750-108">注釈</span><span class="sxs-lookup"><span data-stu-id="fe750-108">Remarks</span></span>

<span data-ttu-id="fe750-p101">**SQL** プロパティには、クエリの実行時にレコードの選択、グループ化、順序付けの方法を決定する SQL ステートメントが含まれています。クエリを使用すると、 **[Recordset](recordset-object-dao.md)** オブジェクトに含めるレコードを選択できます。アクション クエリを定義して、レコードを返さずにデータを変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="fe750-p101">The **SQL** property contains the SQL statement that determines how records are selected, grouped, and ordered when you execute the query. You can use the query to select records to include in a **[Recordset](recordset-object-dao.md)** object. You can also define action queries to modify data without returning records.</span></span>

<span data-ttu-id="fe750-p102">クエリに使用する SQL 構文は、ワークスペースの種類によって決まるクエリ エンジンの SQL 文法に従っている必要があります。Microsoft Access ワークスペースでは、Microsoft Access の SQL 文法を使用しますが、SQL パススルー クエリを作成する場合は、サーバーの文法を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fe750-p102">The SQL syntax used in a query must conform to the SQL dialect of the query engine, which is determined by the type of workspace. In a Microsoft Access workspace, use the Microsoft Access SQL dialect, unless you create an SQL pass-through query, in which case you should use the dialect of the server.</span></span>

<span data-ttu-id="fe750-p103">SQL ステートメントにクエリのパラメーターが含まれている場合、実行の前にこれらのパラメーターを設定する必要があります。パラメーターをリセットしない限り、クエリを実行するたびに同じパラメーター値が適用されます。</span><span class="sxs-lookup"><span data-stu-id="fe750-p103">If the SQL statement includes parameters for the query, you must set these before execution. Until you reset the parameters, the same parameter values are applied each time you execute the query.</span></span>

<span data-ttu-id="fe750-116">Microsoft Access ワークスペースの場合、Microsoft Access データベース エンジンに接続されている ODBC データ ソース上で SQL パススルー操作を実行するには、 **QueryDef** オブジェクトを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="fe750-116">In a Microsoft Access workspace, using a **QueryDef** object is the preferred way to perform SQL pass-through operations on Microsoft Access database engine-connected ODBC data sources.</span></span> <span data-ttu-id="fe750-117">ODBC データ ソースに**クエリ定義**オブジェクトの**[接続](querydef-connect-property-dao.md)** プロパティの設定によっては、外部サーバーに渡される – マイクロソフト – アクセス – データベース以外の SQL クエリでを使用できます。</span><span class="sxs-lookup"><span data-stu-id="fe750-117">By setting the **QueryDef** object's **[Connect](querydef-connect-property-dao.md)** property to an ODBC data source, you can use non–Microsoft–Access–database SQL in the query to be passed to the external server.</span></span> <span data-ttu-id="fe750-118">たとえば、それ以外の場合 Microsoft Access データベース エンジンでは処理できない、TRANSACT SQL ステートメントを (Microsoft SQL Server または Sybase SQL Server データベースで) 使用できます。</span><span class="sxs-lookup"><span data-stu-id="fe750-118">For example, you can use TRANSACT SQL statements (with Microsoft SQL Server or Sybase SQL Server databases), which the Microsoft Access database engine would otherwise not process.</span></span>

> [!NOTE]
> <span data-ttu-id="fe750-119">文字列、整数以外の値に連結するプロパティを設定して、システム ・ パラメーターは、米国以外の小数点の記号、カンマなどを指定する場合 (たとえば、strSQL ="価格&gt;" &amp; lngPrice でと lngPrice = 125,50)、エラーが発生とします。Microsoft Access データベース エンジン データベースの**クエリ定義**オブジェクトを実行しようとしてください。</span><span class="sxs-lookup"><span data-stu-id="fe750-119">If you set the property to a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error will result when you try to execute the **QueryDef** object in a Microsoft Access database engine database.</span></span> <span data-ttu-id="fe750-120">連結時に数値がシステムの既定の小数点の記号を使って文字列に変換されますが、Microsoft Access の SQL で小数点の記号として使用できるのはピリオドのみであるためです。</span><span class="sxs-lookup"><span data-stu-id="fe750-120">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>

## <a name="example"></a><span data-ttu-id="fe750-121">例</span><span class="sxs-lookup"><span data-stu-id="fe750-121">Example</span></span>

<span data-ttu-id="fe750-p106">次の例では、一時的な **QueryDef** オブジェクトの **SQL** プロパティを設定して変更し、結果を比較することで、 **SQL** プロパティの機能を示します。このプロシージャを実行するには、 SQLOutput 関数が必要です。</span><span class="sxs-lookup"><span data-stu-id="fe750-p106">This example demonstrates the **SQL** property by setting and changing the **SQL** property of a temporary **QueryDef** and comparing the results. The SQLOutput function is required for this procedure to run.</span></span>

```vb
    Sub SQLX() 
     
       Dim dbsNorthwind As Database 
       Dim qdfTemp As QueryDef 
       Dim rstEmployees As Recordset 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set qdfTemp = dbsNorthwind.CreateQueryDef("") 
     
       ' Open Recordset using temporary QueryDef object and  
       ' print report. 
       SQLOutput "SELECT * FROM Employees " & _ 
          "WHERE Country = 'USA' " & _ 
          "ORDER BY LastName", qdfTemp 
     
       ' Open Recordset using temporary QueryDef object and  
       ' print report. 
       SQLOutput "SELECT * FROM Employees " & _ 
          "WHERE Country = 'UK' " & _ 
          "ORDER BY LastName", qdfTemp 
     
       dbsNorthwind.Close 
     
    End Sub 
     
    Function SQLOutput(strSQL As String, qdfTemp As QueryDef) 
     
       Dim rstEmployees As Recordset 
     
       ' Set SQL property of temporary QueryDef object and open  
       ' a Recordset. 
       qdfTemp.SQL = strSQL 
       Set rstEmployees = qdfTemp.OpenRecordset 
     
       Debug.Print strSQL 
     
       With rstEmployees 
          ' Enumerate Recordset. 
          Do While Not .EOF 
             Debug.Print "  " & !FirstName & " " & _ 
                !LastName & ", " & !Country 
             .MoveNext 
          Loop 
          .Close 
       End With 
     
    End Function 
```

<br/>

<span data-ttu-id="fe750-p107">次の例では、 **CopyQueryDef** メソッドを使用して、既存の **Recordset** オブジェクトから **QueryDef** オブジェクトのコピーを作成し、 **SQL** プロパティに句を追加して、コピーを変更します。永続的な **QueryDef** オブジェクトを作成する場合、 **SQL** プロパティに、スペース、セミコロン、またはラインフィードを追加できます。これらの余分な文字は、SQL ステートメントに新しい句を追加する前に取り除く必要があります。</span><span class="sxs-lookup"><span data-stu-id="fe750-p107">This example uses the **CopyQueryDef** method to create a copy of a **QueryDef** from an existing **Recordset** and modifies the copy by adding a clause to the **SQL** property. When you create a permanent **QueryDef**, spaces, semicolons, or linefeeds may be added to the **SQL** property; these extra characters must be stripped before any new clauses can be attached to the SQL statement.</span></span>

```vb
    Function CopyQueryNew(rstTemp As Recordset, _ 
       strAdd As String) As QueryDef 
     
       Dim strSQL As String 
       Dim strRightSQL As String 
     
       Set CopyQueryNew = rstTemp.CopyQueryDef 
       With CopyQueryNew 
          ' Strip extra characters. 
          strSQL = .SQL 
          strRightSQL = Right(strSQL, 1) 
          Do While strRightSQL = " " Or strRightSQL = ";" Or _ 
                strRightSQL = Chr(10) Or strRightSQL = vbCr 
             strSQL = Left(strSQL, Len(strSQL) - 1) 
             strRightSQL = Right(strSQL, 1) 
          Loop 
          .SQL = strSQL & strAdd 
       End With 
     
    End Function 
     
    This example shows a possible use of CopyQueryNew(). 
     
    Sub CopyQueryDefX() 
     
       Dim dbsNorthwind As Database 
       Dim qdfEmployees As QueryDef 
       Dim rstEmployees As Recordset 
       Dim intCommand As Integer 
       Dim strOrderBy As String 
       Dim qdfCopy As QueryDef 
       Dim rstCopy As Recordset 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set qdfEmployees = dbsNorthwind.CreateQueryDef( _ 
          "NewQueryDef", "SELECT FirstName, LastName, " & _ 
          "BirthDate FROM Employees") 
       Set rstEmployees = qdfEmployees.OpenRecordset( _ 
          dbOpenForwardOnly) 
     
       Do While True 
          intCommand = Val(InputBox( _ 
             "Choose field on which to order a new " & _ 
             "Recordset:" & vbCr & "1 - FirstName" & vbCr & _ 
             "2 - LastName" & vbCr & "3 - BirthDate" & vbCr & _ 
             "[Cancel - exit]")) 
          Select Case intCommand 
             Case 1 
                strOrderBy = " ORDER BY FirstName" 
             Case 2 
                strOrderBy = " ORDER BY LastName" 
             Case 3 
                strOrderBy = " ORDER BY BirthDate" 
             Case Else 
                Exit Do 
          End Select 
          Set qdfCopy = CopyQueryNew(rstEmployees, strOrderBy) 
          Set rstCopy = qdfCopy.OpenRecordset(dbOpenSnapshot, _ 
             dbForwardOnly) 
          With rstCopy 
             Do While Not .EOF 
                Debug.Print !LastName & ", " & !FirstName & _ 
                   " - " & !BirthDate 
                .MoveNext 
             Loop 
             .Close 
          End With 
          Exit Do 
       Loop 
     
       rstEmployees.Close 
       ' Delete new QueryDef because this is a demonstration. 
       dbsNorthwind.QueryDefs.Delete qdfEmployees.Name 
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="fe750-p108">次の例では、 **CreateQueryDef** メソッドと **OpenRecordset** メソッド、および **SQL** プロパティを使用して、Microsoft SQL Server サンプル データベース Pubs の題名のテーブルをクエリし、最もよく売れている本の題名と題名識別子を返します。次に、著者のテーブルをクエリし、印税の割合に基づいてそれぞれの著者にボーナス小切手を送信するようユーザーに指示します (ボーナスの合計は 1,000 ドルで、それぞれの著者はこの金額から印税の割合に応じた額を受け取ります)。</span><span class="sxs-lookup"><span data-stu-id="fe750-p108">This example uses the **CreateQueryDef** and **OpenRecordset** methods and the **SQL** property to query the table of titles in the Microsoft SQL Server sample database Pubs and return the title and title identifier of the best-selling book. The example then queries the table of authors and instructs the user to send a bonus check to each author based on his or her royalty share (the total bonus is $1,000 and each author should receive a percentage of that amount).</span></span>

```vb
    Sub ClientServerX2() 
     
       Dim dbsCurrent As Database 
       Dim qdfBestSellers As QueryDef 
       Dim qdfBonusEarners As QueryDef 
       Dim rstTopSeller As Recordset 
       Dim rstBonusRecipients As Recordset 
       Dim strAuthorList As String 
     
       ' Open a database from which QueryDef objects can be  
       ' created. 
       Set dbsCurrent = OpenDatabase("DB1.mdb") 
     
       ' Create a temporary QueryDef object to retrieve 
       ' data from a Microsoft SQL Server database. 
       Set qdfBestSellers = dbsCurrent.CreateQueryDef("") 
       With qdfBestSellers 
          ' Note: The DSN referenced below must be configured to  
          '       use Microsoft Windows NT Authentication Mode to  
          '       authorize user access to the Microsoft SQL Server. 
          .Connect = "ODBC;DATABASE=pubs;DSN=Publishers" 
          .SQL = "SELECT title, title_id FROM titles " & _ 
             "ORDER BY ytd_sales DESC" 
          Set rstTopSeller = .OpenRecordset() 
          rstTopSeller.MoveFirst 
       End With 
     
       ' Create a temporary QueryDef to retrieve data from 
       ' a Microsoft SQL Server database based on the results from 
       ' the first query. 
       Set qdfBonusEarners = dbsCurrent.CreateQueryDef("") 
       With qdfBonusEarners 
          ' Note: The DSN referenced below must be configured to  
          '       use Microsoft Windows NT Authentication Mode to  
          '       authorize user access to the Microsoft SQL Server. 
          .Connect = "ODBC;DATABASE=pubs;DSN=Publishers" 
          .SQL = "SELECT * FROM titleauthor " & _ 
             "WHERE title_id = '" & _ 
             rstTopSeller!title_id & "'" 
          Set rstBonusRecipients = .OpenRecordset() 
       End With 
     
       ' Build the output string. 
       With rstBonusRecipients 
          Do While Not .EOF 
             strAuthorList = strAuthorList & "  " & _ 
                !au_id & ":  $" & (10 * !royaltyper) & vbCr 
             .MoveNext 
          Loop 
       End With 
     
       ' Display results. 
       MsgBox "Please send a check to the following " & _ 
          "authors in the amounts shown:" & vbCr & _ 
          strAuthorList & "for outstanding sales of " & _ 
          rstTopSeller!Title & "." 
     
       rstTopSeller.Close 
       dbsCurrent.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="fe750-128">次の例は、パラメーター クエリを作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="fe750-128">The following example shows how to create a parameter query.</span></span> <span data-ttu-id="fe750-129">Param1 とパラメーター 2 という名前の 2 つのパラメーターには、 **myQuery**をという名前のクエリが作成されます。</span><span class="sxs-lookup"><span data-stu-id="fe750-129">A query named **myQuery** is created with two parameters, named Param1 and Param2.</span></span> <span data-ttu-id="fe750-130">これを行うには、クエリの SQL プロパティを、パラメーターを定義する構造化照会言語 (SQL) ステートメントに設定します。</span><span class="sxs-lookup"><span data-stu-id="fe750-130">To do this, the SQL property of the query is set to a Structured Query Language (SQL) statement that defines the parameters.</span></span>

<span data-ttu-id="fe750-131">**によって提供されるサンプル コード**を[Microsoft Access 2010 プログラマーズ リファレンス](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)です。</span><span class="sxs-lookup"><span data-stu-id="fe750-131">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Sub CreateQueryWithParameters()
    
        Dim dbs As DAO.Database
        Dim qdf As DAO.QueryDef
        Dim strSQL As String
    
        Set dbs = CurrentDb
        Set qdf = dbs.CreateQueryDef("myQuery")
        Application.RefreshDatabaseWindow
    
        strSQL = "PARAMETERS Param1 TEXT, Param2 INT; "
        strSQL = strSQL & "SELECT * FROM [Table1] "
        strSQL = strSQL & "WHERE [Field1] = [Param1] AND [Field2] = [Param2];"
        qdf.SQL = strSQL
    
        qdf.Close
        Set qdf = Nothing
        Set dbs = Nothing
    
    End Sub
```

<br/>

<span data-ttu-id="fe750-132">以下の例は、保存したクエリ内で構造化照会言語 (SQL) ステートメントを置き換える方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="fe750-132">The following example shows how to replace the Structured Query Language (SQL) statement in a saved query.</span></span>

```vb
    Dim qdf as QueryDef
    Dim db as Database
    Set db = CurrentDB
    Set qdf = db.QueryDefs("YourQueryName")
    qdf.SQL = ReplaceWhereClause(qdf.SQL, strYourNewWhereClause)
    set qdf = Nothing
    set db = Nothing
    
    Public Function ReplaceWhereClause(strSQL As Variant, strNewWHERE As Variant)
    On Error GoTo Error_Handler
    
    ‘This subroutine accepts a valid SQL string and Where clause, and
    ‘returns the same SQL statement with the original Where clause (if any)
    ‘replaced by the passed in Where clause.
    ‘
    ‘INPUT:
    ‘ strSQL valid SQL string to change
    ‘OUTPUT:
    ‘ strNewWHERE New WHERE clause to insert into SQL statement
    ‘
    Dim strSELECT As String, strWhere As String
    Dim strOrderBy As String, strGROUPBY As String, strHAVING As String
    
    Call ParseSQL(strSQL, strSELECT, strWhere, strOrderBy, _
    strGROUPBY, strHAVING)
    
    ReplaceWhereClause = strSELECT &""& strNewWHERE &""_
    & strGROUPBY &""& strHAVING &""& strOrderBy
    
    Exit_Procedure:
      Exit Function
    
    Error_Handler:
      MsgBox (Err.Number & ": " & Err.Description)
      Resume Exit_Procedure
    
    End Function
```
