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
ms.localizationpriority: high
ms.openlocfilehash: a13db599846ebb851b2eb60de2baf813fabf0907
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565059"
---
# <a name="querydefexecute-method-dao"></a>QueryDef.Execute メソッド (DAO)

**適用先**: Access 2013、Office 2013

指定されたオブジェクトに対して SQL ステートメントを実行します。

## <a name="syntax"></a>構文

*式* .Execute (***Options***)

*式***QueryDef** オブジェクトを表す変数。

## <a name="parameters"></a>パラメーター

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>名前</p></th>
<th><p>必須かどうか</p></th>
<th><p>データ型</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>オプション</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

Options には、次の **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** 定数を使用できます。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>定数</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbDenyWrite</strong></p></td>
<td><p>他のユーザーに対して書き込み権限を許可しません (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong>dbInconsistent</strong></p></td>
<td><p>(既定値) 矛盾した更新を実行します (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbConsistent</strong></p></td>
<td><p>一貫性のある更新を実行します (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSQLPassThrough</strong></p></td>
<td><p>SQL パススルー クエリを実行します。このオプションを設定すると、SQL ステートメントが ODBC データベースに渡されて処理されます (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbFailOnError</strong></p></td>
<td><p>エラーが発生した場合、更新をロールバックします (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSeeChanges</strong></p></td>
<td><p>編集中のデータが他のユーザーによって変更されている場合、実行時エラーを生成します (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbRunAsync</strong></p></td>
<td><p>クエリを非同期に実行します (ODBCDirect の Connection オブジェクトと QueryDef オブジェクトのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong>dbExecDirect</strong></p></td>
<td><p>最初に SQLPrepare ODBC API 関数を呼び出さずにステートメントを実行します (ODBCDirect Connection および QueryDef オブジェクトのみ)。</p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> [!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。

> [!NOTE]
> [!メモ] 定数 **dbConsistent** と **dbInconsistent** は互いに排他的です。1 つの **OpenRecordset** のインスタンスにおいては、どちらか一方を使用できますが、両方を使用することはできません。 **dbConsistent** と **dbInconsistent** の両方を使用すると、エラーが発生します。

**[Connection](querydef-recordsaffected-property-dao.md)** 、 **[Database](connection-object-dao.md)** 、または **[QueryDef](database-object-dao.md)** オブジェクトの **[RecordsAffected](querydef-object-dao.md)** プロパティを使用して、最後に使用された **[Execute](querydef-execute-method-dao.md)** メソッドによって影響を受けたレコードの数を取得できます。たとえば、アクション クエリの実行時に削除、更新、または挿入されたレコードの数が **RecordsAffected** に格納されます。 **Execute** メソッドを使用してクエリを実行すると、 **QueryDef** オブジェクトの **RecordsAffected** プロパティは、影響を受けたレコードの数に設定されます。

Microsoft Access ワークスペースでは、指定した SQL ステートメントの構文が正しく、ユーザーが適切な権限を持っている場合、1 行も変更または削除できなくても、 **Execute** メソッドが失敗することはありません。したがって、 **Execute** メソッドを使って更新または削除のクエリを実行するときは、必ず **dbFailOnError** オプションを指定してください。このオプションを使用すると、影響を受けるレコードの一部がロックされているために更新または削除できない場合、実行時エラーが生成され、既に成功している変更もすべてロールバックされます。

以前のバージョンの Microsoft Jet データベース エンジンでは、暗黙のトランザクション内に自動的に SQL ステートメントが埋め込まれていました。 **dbFailOnError** を指定して実行したステートメントの一部が失敗した場合は、ステートメント全体がロールバックされました。パフォーマンスを向上するために、バージョン 3.5 以降では、この暗黙のトランザクションが取り除かれました。古いバージョンの DAO コードを更新する場合は、 **Execute** ステートメントの前後で明示的なトランザクションを使用することを検討してください。

Microsoft Access ワークスペースでのパフォーマンスを最適にする (特にマルチユーザー環境の場合) には、トランザクション内部に **Execute** メソッドをネストします。現在の **[Workspace](workspace-object-dao.md)** オブジェクトの **[BeginTrans](workspace-begintrans-method-dao.md)** メソッドを使用し、次に **Execute** メソッドを使用し、最後に **Workspace** の **[CommitTrans](workspace-committrans-method-dao.md)** メソッドを使用してトランザクションを完了します。これにより、変更がディスクに保存され、クエリ実行中に適用されていたロックがすべて解除されます。

## <a name="example"></a>例

この例では、**Execute** メソッドを **QueryDef** オブジェクトから実行する場合と **Database** オブジェクトから実行する場合の両方を示します。このプロシージャを実行するには、ExecuteQueryDef プロシージャおよび PrintOutput プロシージャが必要です。

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

次の例は、パラメーター クエリを実行する方法を示します。クエリを実行する前に Parameters コレクションを使用して myActionQuery クエリの Organization パラメーターを設定します。

**サンプル コードの提供元:** [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)。

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
