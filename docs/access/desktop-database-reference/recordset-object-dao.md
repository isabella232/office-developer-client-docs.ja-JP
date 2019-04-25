---
title: Recordset オブジェクト (DAO)
TOCTitle: Recordset Object
ms:assetid: 9774232c-e6da-175b-fc7f-ed2ab7908fa0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197799(v=office.15)
ms:contentKeyID: 48546469
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 19999159f7987be87031f88d1eec87980585f369
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284519"
---
# <a name="recordset-object-dao"></a>Recordset オブジェクト (DAO)

**適用先**: Access 2013、Office 2013

**Recordset** オブジェクトは、ベース テーブルのレコード、またはクエリの実行結果のレコードを表します。

## <a name="remarks"></a>注釈

データベースのデータをレコード レベルで操作するには、 **Recordset** オブジェクトを使用します。DAO オブジェクトを使用する場合は、 **Recordset** オブジェクトを使用してほぼすべてのデータを操作します。すべての **Recordset** オブジェクトは、レコード (行) およびフィールド (列) を使用して構成されます。次の 5 種類の **Recordset** オブジェクトがあります。

- テーブル タイプの Recordset: 1 つのデータベース テーブルのレコードを追加、変更、または削除できるベース テーブルのコード表示形式です (Microsoft Access ワークスペースのみ)。

- ダイナセット タイプの Recordset: 更新可能なレコードを持つクエリの結果です。ダイナセット タイプの **Recordset** オブジェクトは、基となっているデータベース テーブルのレコードを追加、変更、または削除できる動的なレコードセットです。ダイナセット タイプの **Recordset** オブジェクトには、データベース内の複数のテーブルのフィールドを含めることができます。このタイプは、ODBC キーセット カーソルに対応します。

- スナップショット タイプの Recordset: データの検索やレポートの生成に使用できるレコードセットの静的コピーです。スナップショット タイプの **Recordset** オブジェクトには、データベース内の複数のテーブルのフィールドを含めることができますが、更新はできません。このタイプは、ODBC 静的カーソルに対応します。

- 前方スクロール タイプの Recordset: カーソルが提供されない点を除き、スナップショットと同じ働きをします。レコードのスクロール方向が前方向に限定されます。結果セットのスクロールが 1 回だけで十分な場合は、これによってパフォーマンスを向上できます。このタイプは、ODBC 前方スクロール カーソルに対応します。

- 動的タイプの Recordset: 行を返すクエリからレコードを追加、変更、または削除できる 1 つまたは複数のベース テーブルからのクエリの結果セットです。さらに、他のユーザーがベース テーブルで追加、削除、または編集したレコードも **Recordset** オブジェクトに表示されます。このタイプは、ODBC 動的カーソルに対応します (ODBCDirect ワークスペースのみ)。

> [!NOTE]
> [!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。

**OpenRecordset** メソッドの type 引数を使用して、作成できる **Recordset** オブジェクトの種類を選択できます。

Microsoft Access ワークスペースでは、 type を指定しない場合、DAO によって、まず最大限の機能を備えたテーブル タイプの **Recordset** オブジェクトが作成されます。 DAO 試行ダイナセット タイプ、スナップショット、し、最後に、前方の種類でこの種類を使用できない場合 **Recordset** オブジェクトです。

ODBCDirect ワークスペースでは、 type を指定しない場合、DAO によって、まずクエリ応答が最も速い前方スクロール タイプの **Recordset** オブジェクトが作成されます。 前方スクロール タイプが使用できない場合は、スナップショット タイプ、ダイナセット タイプ、最後に動的タイプの順で **Recordset** オブジェクトが作成されます。

Microsoft Access ワークスペースで、リンクされていない [**TableDef**](tabledef-object-dao.md) オブジェクトを使用して **Recordset** オブジェクトを作成すると、テーブル タイプの **Recordset** オブジェクトが作成されます。リンク テーブルまたは Microsoft データベース エンジンに接続された ODBC データベースのテーブルでは、ダイナセット タイプまたはスナップショット タイプの **Recordset** オブジェクトのみを作成できます。

新しい **Recordset** オブジェクトは、オブジェクトを開いたときに **Recordsets** コレクションに自動的に追加され、オブジェクトを閉じたときに自動的に削除されます。

> [!NOTE]
> [!メモ] **Recordset** オブジェクトを表す変数、および **Recordset** オブジェクトを含む **Database** オブジェクトを使用する場合は、変数の適用範囲または有効期間が同じであることを確認してください。たとえば、 **Recordset** オブジェクトを表すパブリック変数を宣言する場合は、 **Recordset** オブジェクトを含む **Database** オブジェクトもパブリックであるか、または **Static** キーワードを使用して **Sub** または **Function** プロシージャで宣言されていることを確認してください。

**Recordset** オブジェクト変数は必要な数だけ作成できます。異なる **Recordset** オブジェクトでも、競合せずに同じテーブル、クエリ、およびフィールドにアクセスできます。

ダイナセット タイプ、スナップショット タイプ、および前方スクロール タイプの **Recordset** オブジェクトは、ローカル メモリに格納されます。ローカル メモリにデータを格納するための十分な空き領域がない場合、Microsoft データベース エンジンでは、追加データが TEMP ディスク領域に格納されます。この領域が不足している場合は、トラップ可能なエラーが発生します。

**Recordset** オブジェクトの既定のコレクションは **Fields** コレクションであり、 **[Field](field-object-dao.md)** オブジェクトの既定のプロパティは **[Value](field-value-property-dao.md)** プロパティです。コードを簡略化するには、これらの既定値を使用します。

**Recordset** オブジェクトを作成すると、レコードがある場合はカレント レコードが最初のレコードに配置されます。レコードがない場合は、 **RecordCount** プロパティ設定が 0 になり、 **BOF** プロパティおよび **EOF** プロパティ設定が **True** になります。

**MoveNext**、**MovePrevious**、**MoveFirst**、**MoveLast** の各メソッドを使用すると、カレント レコードを再配置できます。 前方スクロール タイプの **Recordset** オブジェクトは、**MoveNext** メソッドのみをサポートします。 Move メソッドを使用して各レコードを参照する場合 (または **Recordset** を実行する場合) は、**BOF** および **EOF** プロパティを使用して、**Recordset** オブジェクトの開始または終了を確認できます。

Microsoft Access ワークスペースで、ダイナセット タイプおよびスナップショット タイプの **Recordset** オブジェクトを使用する場合は、 FindFirst などの **Find** メソッドを使用して、基準に基づいて特定のレコードを検索することもできます。 レコードが見つからない場合は、 **NoMatch** プロパティが **True** に設定されます。 テーブル タイプの **Recordset** オブジェクトの場合は、 **Seek** メソッドを使用してレコードをスキャンできます。

**Type** プロパティは、作成される **Recordset** オブジェクトの種類を示し、 **Updatable** プロパティはオブジェクトのレコードを変更できるかどうかを示します。

各 **Field** オブジェクトおよび **Index** オブジェクトの名前およびデータ型など、ベース テーブルの構造に関する情報は、 **TableDef** オブジェクトに格納されます。

コレクション内の **Recordset** オブジェクトを、コレクションで付けられたインデックスまたは **Name** プロパティの設定値で参照するには、次のいずれかの構文を使います。

- **Recordsets**(0)

- **Recordsets** (「名前」)

- **Recordsets**\!\[名前\]

> [!NOTE]
> [!メモ] 同じデータ ソースまたはデータベースから **Recordset** オブジェクトを複数回開いて、 **Recordsets** コレクションに重複する名前を作成できます。 **Recordset** オブジェクトをオブジェクト変数に割り当て、変数名で参照する必要があります。

## <a name="example"></a>例

次の使用例は、4 種類の **Recordset** オブジェクトを開き、現在の **Recordsets** オブジェクトの Recordsets コレクションを列挙して、各 **Recordsets** オブジェクトの **Database** コレクションを列挙することで、 **Properties** オブジェクトおよび **Recordset** コレクションを示します。

```vb
    Sub RecordsetX() 
     
       Dim dbsNorthwind As Database 
       Dim rstTable As Recordset 
       Dim rstDynaset As Recordset 
       Dim rstSnapshot As Recordset 
       Dim rstForwardOnly As Recordset 
       Dim rstLoop As Recordset 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       With dbsNorthwind 
     
          ' Open one of each type of Recordset object. 
          Set rstTable = .OpenRecordset("Categories", _ 
             dbOpenTable) 
          Set rstDynaset = .OpenRecordset("Employees", _ 
             dbOpenDynaset) 
          Set rstSnapshot = .OpenRecordset("Shippers", _ 
             dbOpenSnapshot) 
          Set rstForwardOnly = .OpenRecordset _  
             ("Employees", dbOpenForwardOnly) 
     
          Debug.Print "Recordsets in Recordsets " & _ 
             "collection of dbsNorthwind" 
     
          ' Enumerate Recordsets collection. 
          For Each rstLoop In .Recordsets 
     
             With rstLoop 
                Debug.Print "  " & .Name 
     
                ' Enumerate Properties collection of each 
                ' Recordset object. Trap for any  
                ' properties whose values are invalid in  
                ' this context. 
                For Each prpLoop In .Properties 
                   On Error Resume Next 
                   If prpLoop <> "" Then Debug.Print _ 
                      "    " & prpLoop.Name & _ 
                      " = " & prpLoop 
                   On Error GoTo 0 
                Next prpLoop 
     
             End With 
     
          Next rstLoop 
     
          rstTable.Close 
          rstDynaset.Close 
          rstSnapshot.Close 
          rstForwardOnly.Close 
     
          .Close 
       End With 
     
    End Sub 
```

<br/>

この例では、**OpenRecordset** メソッドを使用して 5 つの異なる **Recordset** オブジェクトを開き、それらの内容を表示します。 このプロシージャを実行するには、OpenRecordsetOutput プロシージャが必要です。

```vb
    Sub OpenRecordsetX() 
     
       Dim wrkAcc As Workspace 
       Dim wrkODBC As Workspace 
       Dim dbsNorthwind As Database 
       Dim conPubs As Connection 
       Dim rstTemp As Recordset 
       Dim rstTemp2 As Recordset 
     
       ' Open Microsoft Access and ODBCDirect workspaces, Microsoft  
       ' Access database, and ODBCDirect connection. 
       Set wrkAcc = CreateWorkspace("", "admin", "", dbUseJet) 
       Set wrkODBC = CreateWorkspace("", "admin", "", dbUseODBC) 
       Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb") 
        
       ' Note: The DSN referenced below must be set to  
       '       use Microsoft Windows NT Authentication Mode to  
       '       authorize user access to the Microsoft SQL Server. 
       Set conPubs = wrkODBC.OpenConnection("", , , _ 
          "ODBC;DATABASE=pubs;DSN=Publishers") 
     
       ' Open five different Recordset objects and display the  
       ' contents of each. 
     
       Debug.Print "Opening forward-only-type recordset " & _ 
          "where the source is a QueryDef object..." 
       Set rstTemp = dbsNorthwind.OpenRecordset( _ 
          "Ten Most Expensive Products", dbOpenForwardOnly) 
       OpenRecordsetOutput rstTemp 
     
       Debug.Print "Opening read-only dynaset-type " & _ 
          "recordset where the source is an SQL statement..." 
       Set rstTemp = dbsNorthwind.OpenRecordset( _ 
          "SELECT * FROM Employees", dbOpenDynaset, dbReadOnly) 
       OpenRecordsetOutput rstTemp 
     
       ' Use the Filter property to retrieve only certain  
       ' records with the next OpenRecordset call. 
       Debug.Print "Opening recordset from existing " & _ 
          "Recordset object to filter records..." 
       rstTemp.Filter = "LastName >= 'M'" 
       Set rstTemp2 = rstTemp.OpenRecordset() 
       OpenRecordsetOutput rstTemp2 
     
       Debug.Print "Opening dynamic-type recordset from " & _ 
          "an ODBC connection..." 
       Set rstTemp = conPubs.OpenRecordset( _ 
          "SELECT * FROM stores", dbOpenDynamic) 
       OpenRecordsetOutput rstTemp 
     
       ' Use the StillExecuting property to determine when the  
       ' Recordset is ready for manipulation. 
       Debug.Print "Opening snapshot-type recordset based " & _ 
          "on asynchronous query to ODBC connection..." 
       Set rstTemp = conPubs.OpenRecordset("publishers", _ 
          dbOpenSnapshot, dbRunAsync) 
       Do While rstTemp.StillExecuting 
          Debug.Print "  [still executing...]" 
       Loop 
       OpenRecordsetOutput rstTemp 
     
       rstTemp.Close 
       dbsNorthwind.Close 
       conPubs.Close 
       wrkAcc.Close 
       wrkODBC.Close 
     
    End Sub 
     
    Sub OpenRecordsetOutput(rstOutput As Recordset) 
     
       ' Enumerate the specified Recordset object. 
       With rstOutput 
          Do While Not .EOF 
             Debug.Print , .Fields(0), .Fields(1) 
             .MoveNext 
          Loop 
       End With 
     
    End Sub 
```

<br/>

この例では、動的タイプの **Recordset** オブジェクトを開き、そのレコードを列挙します。

```vb
    Sub dbOpenDynamicX() 
     
       Dim wrkMain As Workspace 
       Dim conMain As Connection 
       Dim qdfTemp As QueryDef 
       Dim rstTemp As Recordset 
       Dim strSQL As String 
       Dim intLoop As Integer 
     
       ' Create ODBC workspace and open connection to 
       ' SQL Server database. 
       Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
          "admin", "", dbUseODBC) 
           
       ' Note: The DSN referenced below must be configured to  
       '       use Microsoft Windows NT Authentication Mode to  
       '       authorize user access to the Microsoft SQL Server.     
       Set conMain = wrkMain.OpenConnection("Publishers", _ 
          dbDriverNoPrompt, False, _ 
          "ODBC;DATABASE=pubs;DSN=Publishers") 
           
       ' Open dynamic-type recordset. 
       Set rstTemp = _ 
          conMain.OpenRecordset("authors", _ 
          dbOpenDynamic) 
     
       With rstTemp 
          Debug.Print "Dynamic-type recordset: " & .Name 
     
          ' Enumerate records. 
          Do While Not .EOF 
             Debug.Print "    " & !au_lname & ", " & _ 
                !au_fname 
             .MoveNext 
          Loop 
     
          .Close 
       End With 
     
       conMain.Close 
       wrkMain.Close 
     
    End Sub 
```

<br/>

この例では、ダイナセット タイプの **Recordset** を開き、フィールドをどの程度更新できるかを示します。

```vb
    Sub dbOpenDynasetX() 
     
       Dim dbsNorthwind As Database 
       Dim rstInvoices As Recordset 
       Dim fldLoop As Field 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstInvoices = _ 
          dbsNorthwind.OpenRecordset("Invoices", dbOpenDynaset) 
     
       With rstInvoices 
          Debug.Print "Dynaset-type recordset: " & .Name 
     
          If .Updatable Then 
             Debug.Print "  Updatable fields:" 
     
             ' Enumerate Fields collection of dynaset-type 
             ' Recordset object, print only updatable 
             ' fields. 
             For Each fldLoop In .Fields 
                If fldLoop.DataUpdatable Then 
                   Debug.Print "    " & fldLoop.Name 
                End If 
             Next fldLoop 
     
          End If 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

この例では、前方スクロール タイプの **Recordset** を開き、読み取り専用の特性を示し、 **MoveNext** メソッドを使用して **Recordset** を実行します。

```vb 
Sub dbOpenForwardOnlyX() 
 
   Dim dbsNorthwind As Database 
   Dim rstEmployees As Recordset 
   Dim fldLoop As Field 
 
   Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
   ' Open a forward-only-type Recordset object. Only the  
   ' MoveNext and Move methods may be used to navigate  
   ' through the recordset. 
   Set rstEmployees = _ 
      dbsNorthwind.OpenRecordset("Employees", _ 
      dbOpenForwardOnly) 
 
   With rstEmployees 
      Debug.Print "Forward-only-type recordset: " & _ 
         .Name & ", Updatable = " & .Updatable 
 
      Debug.Print "  Field - DataUpdatable" 
      ' Enumerate Fields collection, printing the Name and  
      ' DataUpdatable properties of each Field object. 
      For Each fldLoop In .Fields 
         Debug.Print "    " & _ 
            fldLoop.Name & " - " & fldLoop.DataUpdatable 
      Next fldLoop 
 
      Debug.Print "  Data" 
      ' Enumerate the recordset. 
      Do While Not .EOF 
         Debug.Print "    " & !FirstName & " " & _ 
            !LastName 
         .MoveNext 
      Loop 
 
      .Close 
   End With 
 
   dbsNorthwind.Close 
 
End Sub 
```

<br/>

この例では、スナップショット タイプの **Recordset** を開き、読み取り専用の特性を示します。

```vb
    Sub dbOpenSnapshotX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees", _ 
          dbOpenSnapshot) 
     
       With rstEmployees 
          Debug.Print "Snapshot-type recordset: " & _ 
             .Name 
     
          ' Enumerate the Properties collection of the 
          ' snapshot-type Recordset object, trapping for 
          ' any properties whose values are invalid in  
          ' this context. 
          For Each prpLoop In .Properties 
             On Error Resume Next 
             Debug.Print "  " & _ 
                prpLoop.Name & " = " & prpLoop 
             On Error Goto 0 
          Next prpLoop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

この例では、テーブル タイプの **Recordset** を開き、 **Index** プロパティを設定し、そのレコードを列挙します。

```vb
    Sub dbOpenTableX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' dbOpenTable is default. 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees") 
     
       With rstEmployees 
          Debug.Print "Table-type recordset: " & .Name 
     
          ' Use predefined index. 
          .Index = "LastName" 
          Debug.Print "  Index = " & .Index 
     
          ' Enumerate records. 
          Do While Not .EOF 
             Debug.Print "    " & !LastName & ", " & _ 
                !FirstName 
             .MoveNext 
          Loop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

次の例は、Seek メソッドを使用して、リンクしたテーブル内のレコードを見つける方法を示します。

**サンプル コードの提供元:** [Microsoft Access 2010 プログラマー用リファレンス](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)。


```vb
    Sub TestSeek()
        ' Get the path to the external database that contains
        ' the tblCustomers table we're going to search.
        Dim strMyExternalDatabase
        Dim dbs    As DAO.Database
        Dim dbsExt As DAO.Database
        Dim rst    As DAO.Recordset
        Dim tdf    As DAO.TableDef
        
        Set dbs = CurrentDb()
        Set tdf = dbs.TableDefs("tblCustomers")
        strMyExternalDatabase = Mid(tdf.Connect, 11)
        
        'Open the database that contains the table that is linked
        Set dbsExt = OpenDatabase(strMyExternalDatabase)
        
        'Open a table-type recordset against the external table
        Set rst = dbsExt.OpenRecordset("tblCustomers", dbOpenTable)
        
        'Specify which index to search on
        rst.Index = "PrimaryKey"
        
        'Specify the criteria
        rst.Seek "=", 123
        
        'Check the result
        If rst.NoMatch Then
            MsgBox "Record not found."
        Else
            MsgBox "Customer name: " & rst!CustName
        End If
        
        rst.Close
        dbs.Close
        dbsExt.Close
        Set rst = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
        
        
    End Sub
```

<br/>

次の例は、パラメーター クエリに基づく Recordset を開く方法を示しています。

```vb
    Dim dbs As DAO.Database
    Dim qdf As DAO.QueryDef
    Dim rst As DAO.Recordset
    
    Set dbs = CurrentDb
    
    'Get the parameter query
    Set qfd = dbs.QueryDefs("qryMyParameterQuery")
    
    'Supply the parameter value
    qdf.Parameters("EnterStartDate") = Date
    qdf.Parameters("EnterEndDate") = Date + 7
    
    'Open a Recordset based on the parameter query
    Set rst = qdf.OpenRecordset()
```

<br/>

次の例は、テーブルまたはクエリに基づいて Recordset を開く方法を示しています。

```vb
    Dim dbs As DAO.Database
    Dim rsTable As DAO.Recordset
    Dim rsQuery As DAO.Recordset
    
    Set dbs = CurrentDb
    
    'Open a table-type Recordset
    Set rsTable = dbs.OpenRecordset("Table1", dbOpenTable)
    
    'Open a dynaset-type Recordset using a saved query
    Set rsQuery = dbs.OpenRecordset("qryMyQuery", dbOpenDynaset)
```

<br/>

次の例は、構造化照会言語 (SQL) ステートメントに基づいて Recordset を開く方法を示しています。

```vb
    Dim dbs As DAO.Database
    Dim rsSQL As DAO.Recordset
    Dim strSQL As String
    
    Set dbs = CurrentDb
    
    'Open a snapshot-type Recordset based on an SQL statement
    strSQL = "SELECT * FROM Table1 WHERE Field2 = 33"
    Set rsSQL = dbs.OpenRecordset(strSQL, dbOpenSnapshot)
```

<br/>

次の例は、FindFirst メソッドと FindNext メソッドを使用して Recordset 内のレコードを検索する方法を示しています。

```vb
    Sub FindOrgName()
    
        Dim dbs As DAO.Database
        Dim rst As DAO.Recordset
        
        'Get the database and Recordset
        Set dbs = CurrentDb
        Set rst = dbs.OpenRecordset("tblCustomers")
    
        'Search for the first matching record   
        rst.FindFirst "[OrgName] LIKE '*parts*'"
        
        'Check the result
        If rst.NoMatch Then
            MsgBox "Record not found."
            GotTo Cleanup
        Else
            Do While Not rst.NoMatch
                MsgBox "Customer name: " & rst!CustName
                rst.FindNext "[OrgName] LIKE '*parts*'"
            Loop
    
            'Search for the next matching record
            rst.FindNext "[OrgName] LIKE '*parts*'"
        End If
       
        Cleanup:
            rst.Close
            Set rst = Nothing
            Set dbs = Nothing
    
    End Sub
```

<br/>

次の例は、新しい Microsoft Excel ブックのワークシートにクエリの結果をコピーする方法を示しています。

```vb
    Public Sub CopyDataFromQuery( _
        xlApp As Excel.Application, _
        strQueryName As String)
    
        ' If the xlApp object exists
        If Not xlApp Is Nothing Then
        
            ' If the Workbook exists
            If xlApp.Workbooks.Count = 1 Then
            
                ' Create Recrodset Object from the Query
                Dim rsQuery As DAO.Recordset
                Set rsQuery = Application.CurrentDb.OpenRecordset(strQueryName)
                
                ' Get the Cells object
                Dim Cells As Object
                Set Cells = xlApp.Workbooks(1).ActiveSheet.Cells
                
                ' Copy the Data from the Query into the Sheet
                Cells.CopyFromRecordset rsQuery
                
            End If
        End If
    
    End Sub
```

