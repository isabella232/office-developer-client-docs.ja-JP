---
title: QueryDef.SQL プロパティ (DAO)
TOCTitle: SQL property
ms:assetid: 16446789-c8be-bff0-eddd-b5f6a8530128
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845522(v=office.15)
ms:contentKeyID: 48543429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053054
f1_categories:
- Office.Version=v15
ms.localizationpriority: high
ms.openlocfilehash: 3213cf90bc1f2b07f93f19561d24dbd2ee31dd8e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576997"
---
# <a name="querydefsql-property-dao"></a>QueryDef.SQL プロパティ (DAO)

**適用先**: Access 2013、Office 2013

**[QueryDef](querydef-object-dao.md)** オブジェクトが実行するクエリを定義する SQL ステートメントを設定または取得します。

## <a name="syntax"></a>構文

*式* .SQL

*式* **QueryDef** オブジェクトを表す変数。

## <a name="remarks"></a>注釈


            **SQL** プロパティには、クエリの実行時にレコードの選択、グループ化、順序付けの方法を決定する SQL ステートメントが含まれています。クエリを使用すると、**[Recordset](recordset-object-dao.md)** オブジェクトに含めるレコードを選択できます。アクション クエリを定義して、レコードを返さずにデータを変更することもできます。

クエリに使用する SQL 構文は、ワークスペースの種類によって決まるクエリ エンジンの SQL 文法に従っている必要があります。Microsoft Access ワークスペースでは、Microsoft Access の SQL 文法を使用しますが、SQL パススルー クエリを作成する場合は、サーバーの文法を使用する必要があります。

SQL ステートメントにクエリのパラメーターが含まれている場合、実行の前にこれらのパラメーターを設定する必要があります。パラメーターをリセットしない限り、クエリを実行するたびに同じパラメーター値が適用されます。

Microsoft Access ワークスペースの場合、Microsoft Access データベース エンジンに接続されている ODBC データ ソース上で SQL パススルー操作を実行するには、**QueryDef** オブジェクトを使用することをお勧めします。**QueryDef** オブジェクトの **[Connect](querydef-connect-property-dao.md)** プロパティを ODBC データ ソースに設定すると、クエリで外部サーバーに渡す必要がある Microsoft Access データベース以外の SQL を使用できます。たとえば、それ以外の場合 Microsoft Access データベース エンジンでは処理できない、TRANSACT SQL ステートメントを (Microsoft SQL Server または Sybase SQL Server データベースで) 使用できます。

> [!NOTE]
> このプロパティを非整数値と連結された文字列に設定し、かつシステム パラメーターでコンマなどのピリオド以外の小数点の記号が指定されている場合 (たとえば、 `strSQL = "PRICE > " & lngPrice, and lngPrice = 125,50` で )、Microsoft Access データベース エンジンのデータベースで **QueryDef** オブジェクトを実行しようとすると、エラーが発生します。連結時に数値がシステムの既定の小数点の記号を使って文字列に変換されますが、Microsoft Access の SQL で小数点の記号として使用できるのはピリオドのみであるためです。

## <a name="example"></a>例

次の例では、一時的な **QueryDef** オブジェクトの **SQL** プロパティを設定して変更し、結果を比較することで、 **SQL** プロパティの機能を示します。このプロシージャを実行するには、 SQLOutput 関数が必要です。

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

次の例では、**CopyQueryDef** メソッドを使用して、既存の **Recordset** オブジェクトから **QueryDef** オブジェクトのコピーを作成し、**SQL** プロパティに句を追加して、コピーを変更します。永続的な **QueryDef** オブジェクトを作成する場合、**SQL** プロパティに、スペース、セミコロン、またはラインフィードを追加できます。これらの余分な文字は、SQL ステートメントに新しい句を追加する前に取り除く必要があります。

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
```

<br/>

次の例は、CopyQueryNew() の使用例を示しています。 
     
```vb
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

次の例では、**CreateQueryDef** メソッドと **OpenRecordset** メソッド、および **SQL** プロパティを使用して、Microsoft SQL Server サンプル データベース Pubs の題名のテーブルをクエリし、最もよく売れている本の題名と題名識別子を返します。次に、著者のテーブルをクエリし、印税の割合に基づいてそれぞれの著者にボーナス小切手を送信するようユーザーに指示します (ボーナスの合計は 1,000 ドルで、それぞれの著者はこの金額から印税の割合に応じた額を受け取ります)。

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

次の例は、パラメーター クエリを作成する方法を示します。Param1 および Param2 という名前の 2 つのパラメーターを使用して **myQuery** という名前のクエリを作成します。これを行うには、クエリの SQL プロパティを、パラメーターを定義する構造化照会言語 (SQL) ステートメントに設定します。

**サンプル コードの提供元:** [Microsoft Access 2010 プログラマー用リファレンス](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)。

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

以下の例は、保存したクエリ内で構造化照会言語 (SQL) ステートメントを置き換える方法を示しています。

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
