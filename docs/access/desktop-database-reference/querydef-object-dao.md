---
title: クエリ定義オブジェクト (DAO)
TOCTitle: QueryDef Object
ms:assetid: 0b3d901c-345d-42a2-f5f1-fb09cc562e27
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845129(v=office.15)
ms:contentKeyID: 48543169
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: a94d34a2dbe8043e6db637b649f59047cf3f1dda
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713556"
---
# <a name="querydef-object-dao"></a><span data-ttu-id="6e6eb-102">クエリ定義オブジェクト (DAO)</span><span class="sxs-lookup"><span data-stu-id="6e6eb-102">QueryDef object (DAO)</span></span>

<span data-ttu-id="6e6eb-103">**に適用されます:** Access 2013 |Office 2013</span><span class="sxs-lookup"><span data-stu-id="6e6eb-103">**Applies to:** Access 2013 | Office 2013</span></span> 

<span data-ttu-id="6e6eb-104">**QueryDef** オブジェクトは、Microsoft Access データベース エンジン データベースのクエリのストアド定義を表します。</span><span class="sxs-lookup"><span data-stu-id="6e6eb-104">A **QueryDef** object is a stored definition of a query in a Microsoft Access database engine database.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e6eb-105">注釈</span><span class="sxs-lookup"><span data-stu-id="6e6eb-105">Remarks</span></span>

<span data-ttu-id="6e6eb-p101">**QueryDef** オブジェクトを使用して、クエリを定義できます。たとえば、以下の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="6e6eb-p101">You can use the **QueryDef** object to define a query. For example, you can:</span></span>

- <span data-ttu-id="6e6eb-108">**SQL** プロパティを使用して、クエリ定義を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="6e6eb-108">Use the **SQL** property to set or return the query definition.</span></span>

- <span data-ttu-id="6e6eb-109">**QueryDef** オブジェクトの **Parameters** コレクションを使用して、クエリ パラメーターを設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="6e6eb-109">Use the **QueryDef** object's **Parameters** collection to set or return query parameters.</span></span>

- <span data-ttu-id="6e6eb-110">**Type** プロパティを使用して、クエリが既存のテーブルからのレコードの選択、新しいテーブルの作成、あるテーブルから別のテーブルへのレコードの挿入、レコードの削除、レコードの更新のいずれを行うかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="6e6eb-110">Use the **Type** property to return a value indicating whether the query selects records from an existing table, makes a new table, inserts records from one table into another table, deletes records, or updates records.</span></span>

- <span data-ttu-id="6e6eb-111">**MaxRecords** プロパティを使用して、クエリから返されるレコードの数を制限します。</span><span class="sxs-lookup"><span data-stu-id="6e6eb-111">Use the **MaxRecords** property to limit the number of records returned from a query.</span></span>

- <span data-ttu-id="6e6eb-p102">**ODBCTimeout** プロパティを使用して、クエリがレコードを返すまでに待機する時間を指定します。 **ODBCTimeout** プロパティは、ODBC データにアクセスするすべてのクエリに適用されます。</span><span class="sxs-lookup"><span data-stu-id="6e6eb-p102">Use the **ODBCTimeout** property to indicate how long to wait before the query returns records. The **ODBCTimeout** property applies to any query that accesses ODBC data.</span></span>

- <span data-ttu-id="6e6eb-p103">**ReturnsRecords** プロパティを使用して、クエリがレコードを返すことを示します。 **ReturnsRecords** プロパティは、SQL パススルー クエリでのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="6e6eb-p103">Use the **ReturnsRecords** property to indicate that the query returns records. The **ReturnsRecords** property is only valid on SQL pass-through queries.</span></span>

- <span data-ttu-id="6e6eb-116">**Connect** プロパティを使用して、ODC データベースへの SQL パススルー クエリを作成します。</span><span class="sxs-lookup"><span data-stu-id="6e6eb-116">Use the **Connect** property to make an SQL pass-through query to an ODC database.</span></span>

<span data-ttu-id="6e6eb-p104">一時的な **QueryDef** オブジェクトを作成することもできます。永続的な **QueryDef** オブジェクトと異なり、一時的な **QueryDef** オブジェクトは、ディスクに保存されたり、 **QueryDefs** コレクションに追加されたりすることはありません。一時的な **QueryDef** オブジェクトは、特に実行時に SQL ステートメントを作成する場合など、実行時に繰り返し実行する必要があっても、ディスクに保存する必要がないクエリで使用すると便利です。</span><span class="sxs-lookup"><span data-stu-id="6e6eb-p104">You can also create temporary **QueryDef** objects. Unlike permanent **QueryDef** objects, temporary **QueryDef** objects are not saved to disk or appended to the **QueryDefs** collection. Temporary **QueryDef** objects are useful for queries that you must run repeatedly during run time but do not not need to save to disk, particularly if you create their SQL statements during run time.</span></span>

<span data-ttu-id="6e6eb-p105">Microsoft Access ワークスペースの永続的な **QueryDef** オブジェクトは、コンパイル済みの SQL ステートメントと考えることができます。永続的な **QueryDef** オブジェクトからクエリを実行すると、 **OpenRecordset** メソッドから同等の SQL ステートメントを実行する場合よりも実行速度が向上します。これは、Microsoft Access データベース エンジンがクエリを実行する前にコンパイルする必要がないためです。</span><span class="sxs-lookup"><span data-stu-id="6e6eb-p105">You can think of a permanent **QueryDef** object in a Microsoft Access workspace as a compiled SQL statement. If you execute a query from a permanent **QueryDef** object, the query will run faster than if you run the equivalent SQL statement from the **OpenRecordset** method. This is because the Microsoft Access database engine doesn't need to compile the query before executing it.</span></span>

<span data-ttu-id="6e6eb-p106">Microsoft Access データベース エンジンを介してアクセスする外部データベース エンジンの固有の SQL 言語を使用するときには、 **QueryDef** オブジェクトの使用をお勧めします。たとえば、Microsoft SQL Server クエリを作成して、 **QueryDef** オブジェクトに保存できます。Microsoft Access データベース エンジン以外の SQL クエリを使用する場合、外部データ ソースを指す **Connect** プロパティ文字列を指定する必要があります。有効な **Connect** プロパティを持つクエリは、Microsoft Access データベース エンジンを使用せずに、外部データベース サーバーに処理するクエリを直接渡します。</span><span class="sxs-lookup"><span data-stu-id="6e6eb-p106">The preferred way to use the native SQL dialect of an external database engine accessed through the Microsoft Access database engine is through **QueryDef** objects. For example, you can create a Microsoft SQL Server query and store it in a **QueryDef** object. When you need to use a non-Microsoft Access database engine SQL query, you must provide a **Connect** property string that points to the external data source. Queries with valid **Connect** properties bypass the Microsoft Access database engine and pass the query directly to the external database server for processing.</span></span>

<span data-ttu-id="6e6eb-127">新しい **QueryDef** オブジェクトを作成するには、 **CreateQueryDef** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="6e6eb-127">To create a new **QueryDef** object, use the **CreateQueryDef** method.</span></span> <span data-ttu-id="6e6eb-128">Microsoft Access ワークスペースでは、name 引数の文字列を指定する場合、または、新しい**QueryDef**オブジェクトの**Name**プロパティを非--長さ 0 の文字列を明示的に設定する場合は、作成が自動的に永続的な**QueryDef\*\*\*\*QueryDefs**コレクションに追加し、そのディスクに保存します。</span><span class="sxs-lookup"><span data-stu-id="6e6eb-128">In a Microsoft Access workspace, if you supply a string for the name argument or if you explicitly set the **Name** property of the new **QueryDef** object to a non–zero-length string, you will create a permanent **QueryDef** that will automatically be appended to the **QueryDefs** collection and saved to disk.</span></span> <span data-ttu-id="6e6eb-129">引数 name として長さ 0 の文字列を指定するか、 **Name**プロパティを長さ 0 の文字列に明示的に設定すると、一時的な**QueryDef**オブジェクトが作成されます。</span><span class="sxs-lookup"><span data-stu-id="6e6eb-129">Supplying a zero-length string as the name argument or explicitly setting the **Name** property to a zero-length string will result in a temporary **QueryDef** object.</span></span>

<span data-ttu-id="6e6eb-130">コレクション内の **QueryDef** オブジェクトを、コレクションで付けられたインデックスまたは **Name** プロパティの設定値で参照するには、次のいずれかの構文を使います。</span><span class="sxs-lookup"><span data-stu-id="6e6eb-130">To refer to a **QueryDef** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="6e6eb-131">QueryDefs(0)</span><span class="sxs-lookup"><span data-stu-id="6e6eb-131">QueryDefs(0)</span></span>

<span data-ttu-id="6e6eb-132">QueryDefs("name")</span><span class="sxs-lookup"><span data-stu-id="6e6eb-132">QueryDefs("name")</span></span>

<span data-ttu-id="6e6eb-133">クエリ定義の\!\[名\]</span><span class="sxs-lookup"><span data-stu-id="6e6eb-133">QueryDefs\!\[ name\]</span></span>

<span data-ttu-id="6e6eb-134">一時的な **QueryDef** オブジェクトは、オブジェクトに割り当てたオブジェクト変数でのみ参照できます。</span><span class="sxs-lookup"><span data-stu-id="6e6eb-134">You can refer to temporary **QueryDef** objects only by the object variables that you have assigned to them.</span></span>

<span data-ttu-id="6e6eb-135">**でリンクが用意されている** [UtterAccess](https://www.utteraccess.com)のコミュニティです。</span><span class="sxs-lookup"><span data-stu-id="6e6eb-135">**Link provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="6e6eb-136">UtterAccess は非常に優れた Microsoft Access wiki およびヘルプ フォーラムです。</span><span class="sxs-lookup"><span data-stu-id="6e6eb-136">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="6e6eb-137">Queries: Document SQL to Word</span><span class="sxs-lookup"><span data-stu-id="6e6eb-137">Queries: Document SQL to Word</span></span>](https://www.utteraccess.com/wiki/index.php/queries:_document_sql_to_word)

## <a name="example"></a><span data-ttu-id="6e6eb-138">例</span><span class="sxs-lookup"><span data-stu-id="6e6eb-138">Example</span></span>

<span data-ttu-id="6e6eb-p109">この例では、新しい **QueryDef** オブジェクトを作成し、Northwind **Database** オブジェクトの **QueryDefs** コレクションに追加します。次に、 **QueryDefs** コレクションおよび新しい **QueryDef** オブジェクトの **Properties** コレクションを列挙します。</span><span class="sxs-lookup"><span data-stu-id="6e6eb-p109">This example creates a new **QueryDef** object and appends it to the **QueryDefs** collection of the Northwind **Database** object. It then enumerates the **QueryDefs** collection and the **Properties** collection of the new **QueryDef**.</span></span>

```vb
    Sub QueryDefX() 
     
       Dim dbsNorthwind As Database 
       Dim qdfNew As QueryDef 
       Dim qdfLoop As QueryDef 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' Create new QueryDef object. Because it has a  
       ' name, it is automatically appended to the  
       ' QueryDefs collection. 
       Set qdfNew = dbsNorthwind.CreateQueryDef("NewQueryDef", _ 
             "SELECT * FROM Categories") 
     
       With dbsNorthwind 
          Debug.Print .QueryDefs.Count & _ 
             " QueryDefs in " & .Name 
     
          ' Enumerate QueryDefs collection. 
          For Each qdfLoop In .QueryDefs 
             Debug.Print "  " & qdfLoop.Name 
          Next qdfLoop 
     
          With qdfNew 
             Debug.Print "Properties of " & .Name 
     
             ' Enumerate Properties collection of new  
             ' QueryDef object. 
             For Each prpLoop In .Properties 
                On Error Resume Next 
                Debug.Print "  " & prpLoop.Name & " - " & _ 
                   IIf(prpLoop = "", "[empty]", prpLoop) 
                On Error Goto 0 
             Next prpLoop 
          End With 
     
          ' Delete new QueryDef because this is a  
          ' demonstration. 
          .QueryDefs.Delete qdfNew.Name 
          .Close 
       End With 
     
    End Sub 
```

<br/>

<span data-ttu-id="6e6eb-p110">この例では、 **CreateQueryDef** メソッドを使用して、一時的および永続的な **QueryDef** オブジェクトを両方作成して実行します。このプロシージャを実行するには、 GetrstTemp 関数が必要です。</span><span class="sxs-lookup"><span data-stu-id="6e6eb-p110">This example uses the **CreateQueryDef** method to create and execute both a temporary and a permanent **QueryDef**. The GetrstTemp function is required for this procedure to run.</span></span>

```vb
    Sub CreateQueryDefX() 
     
       Dim dbsNorthwind As Database 
       Dim qdfTemp As QueryDef 
       Dim qdfNew As QueryDef 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       With dbsNorthwind 
          ' Create temporary QueryDef. 
          Set qdfTemp = .CreateQueryDef("", _ 
             "SELECT * FROM Employees") 
          ' Open Recordset and print report. 
          GetrstTemp qdfTemp 
          ' Create permanent QueryDef. 
          Set qdfNew = .CreateQueryDef("NewQueryDef", _ 
             "SELECT * FROM Categories") 
          ' Open Recordset and print report. 
          GetrstTemp qdfNew 
          ' Delete new QueryDef because this is a demonstration. 
          .QueryDefs.Delete qdfNew.Name 
          .Close 
       End With 
     
    End Sub 
     
    Function GetrstTemp(qdfTemp As QueryDef) 
     
       Dim rstTemp As Recordset 
     
       With qdfTemp 
          Debug.Print .Name 
          Debug.Print "  " & .SQL 
          ' Open Recordset from QueryDef. 
          Set rstTemp = .OpenRecordset(dbOpenSnapshot) 
     
          With rstTemp 
             ' Populate Recordset and print number of records. 
             .MoveLast 
             Debug.Print "  Number of records = " & _ 
                .RecordCount 
             Debug.Print 
             .Close 
          End With 
     
       End With 
     
    End Function 
```

<br/>

<span data-ttu-id="6e6eb-143">以下の例は、保存したクエリ内で構造化照会言語 (SQL) ステートメントを置き換える方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="6e6eb-143">The following example shows how to replace the Structured Query Language (SQL) statement in a saved query.</span></span>

<span data-ttu-id="6e6eb-144">**によって提供されるサンプル コード**を[Microsoft Access 2010 プログラマーズ リファレンス](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)です。</span><span class="sxs-lookup"><span data-stu-id="6e6eb-144">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    ‘To change the Where clause in a saved query  
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

