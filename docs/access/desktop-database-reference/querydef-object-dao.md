---
title: QueryDef オブジェクト (DAO)
TOCTitle: QueryDef Object
ms:assetid: 0b3d901c-345d-42a2-f5f1-fb09cc562e27
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845129(v=office.15)
ms:contentKeyID: 48543169
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bad2f4795dad8e308af85d3cca4ca0f71d88d9c2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477142"
---
# <a name="querydef-object-dao"></a>QueryDef オブジェクト (DAO)

**に適用されます:** Access 2013 |Office 2013 

**QueryDef** オブジェクトは、Microsoft Access データベース エンジン データベースのクエリのストアド定義を表します。

## <a name="remarks"></a>注釈

**QueryDef** オブジェクトを使用して、クエリを定義できます。たとえば、以下の操作を実行できます。

- **SQL** プロパティを使用して、クエリ定義を設定または取得します。

- **QueryDef** オブジェクトの **Parameters** コレクションを使用して、クエリ パラメーターを設定または取得します。

- **Type** プロパティを使用して、クエリが既存のテーブルからのレコードの選択、新しいテーブルの作成、あるテーブルから別のテーブルへのレコードの挿入、レコードの削除、レコードの更新のいずれを行うかを示す値を取得します。

- **MaxRecords** プロパティを使用して、クエリから返されるレコードの数を制限します。

- **ODBCTimeout** プロパティを使用して、クエリがレコードを返すまでに待機する時間を指定します。 **ODBCTimeout** プロパティは、ODBC データにアクセスするすべてのクエリに適用されます。

- **ReturnsRecords** プロパティを使用して、クエリがレコードを返すことを示します。 **ReturnsRecords** プロパティは、SQL パススルー クエリでのみ有効です。

- **Connect** プロパティを使用して、ODC データベースへの SQL パススルー クエリを作成します。

一時的な **QueryDef** オブジェクトを作成することもできます。永続的な **QueryDef** オブジェクトと異なり、一時的な **QueryDef** オブジェクトは、ディスクに保存されたり、 **QueryDefs** コレクションに追加されたりすることはありません。一時的な **QueryDef** オブジェクトは、特に実行時に SQL ステートメントを作成する場合など、実行時に繰り返し実行する必要があっても、ディスクに保存する必要がないクエリで使用すると便利です。

Microsoft Access ワークスペースの永続的な **QueryDef** オブジェクトは、コンパイル済みの SQL ステートメントと考えることができます。永続的な **QueryDef** オブジェクトからクエリを実行すると、 **OpenRecordset** メソッドから同等の SQL ステートメントを実行する場合よりも実行速度が向上します。これは、Microsoft Access データベース エンジンがクエリを実行する前にコンパイルする必要がないためです。

Microsoft Access データベース エンジンを介してアクセスする外部データベース エンジンの固有の SQL 言語を使用するときには、 **QueryDef** オブジェクトの使用をお勧めします。たとえば、Microsoft SQL Server クエリを作成して、 **QueryDef** オブジェクトに保存できます。Microsoft Access データベース エンジン以外の SQL クエリを使用する場合、外部データ ソースを指す **Connect** プロパティ文字列を指定する必要があります。有効な **Connect** プロパティを持つクエリは、Microsoft Access データベース エンジンを使用せずに、外部データベース サーバーに処理するクエリを直接渡します。

新しい **QueryDef** オブジェクトを作成するには、 **CreateQueryDef** メソッドを使用します。 Microsoft Access ワークスペースでは、name 引数の文字列を指定する場合、または、新しい**QueryDef**オブジェクトの**Name**プロパティを非--長さ 0 の文字列を明示的に設定する場合は、作成が自動的に永続的な**QueryDef****QueryDefs**コレクションに追加し、そのディスクに保存します。 引数 name として長さ 0 の文字列を指定するか、 **Name**プロパティを長さ 0 の文字列に明示的に設定すると、一時的な**QueryDef**オブジェクトが作成されます。

コレクション内の **QueryDef** オブジェクトを、コレクションで付けられたインデックスまたは **Name** プロパティの設定値で参照するには、次のいずれかの構文を使います。

QueryDefs(0)

QueryDefs("name")

クエリ定義の\!\[名\]

一時的な **QueryDef** オブジェクトは、オブジェクトに割り当てたオブジェクト変数でのみ参照できます。

**でリンクが用意されている** [UtterAccess](https://www.utteraccess.com)のコミュニティです。 UtterAccess は非常に優れた Microsoft Access wiki およびヘルプ フォーラムです。

- [Queries: Document SQL to Word](https://www.utteraccess.com/wiki/index.php/queries:_document_sql_to_word)

## <a name="example"></a>例

この例では、新しい **QueryDef** オブジェクトを作成し、Northwind **Database** オブジェクトの **QueryDefs** コレクションに追加します。次に、 **QueryDefs** コレクションおよび新しい **QueryDef** オブジェクトの **Properties** コレクションを列挙します。

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

この例では、 **CreateQueryDef** メソッドを使用して、一時的および永続的な **QueryDef** オブジェクトを両方作成して実行します。このプロシージャを実行するには、 GetrstTemp 関数が必要です。

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

以下の例は、保存したクエリ内で構造化照会言語 (SQL) ステートメントを置き換える方法を示しています。

**によって提供されるサンプル コード**を[Microsoft Access 2010 プログラマーズ リファレンス](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)です。

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

