---
title: Recordset.Index プロパティ (DAO)
TOCTitle: Index Property
ms:assetid: 54626de0-eb51-31f2-bf24-e29cbfbbaa02
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194103(v=office.15)
ms:contentKeyID: 48544895
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052906
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b5f568889d020676be420186b49c9c50c444ee54
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926137"
---
# <a name="recordsetindex-property-dao"></a>Recordset.Index プロパティ (DAO)

**適用されます**Access 2013、Office 2013。

テーブル タイプの **[Recordset](index-object-dao.md)** オブジェクト内にある現在の **[Index](recordset-object-dao.md)** オブジェクトの名前を示す値を設定または取得します (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式*です。インデックス

*式***レコード セット**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

レコードはベース テーブルに特定の順序で格納されているわけではありません。 **Index** プロパティを設定すると、データベースから取得されるレコードの順序は変わりますが、格納されているレコードの順序は変わりません。

指定する **Index** オブジェクトは前もって定義しておく必要があります。存在していない **Index** オブジェクトに **Index** プロパティを設定するか、または [**Seek**](recordset-seek-method-dao.md) メソッドを使用するときに **Index** プロパティが設定されていない場合、トラップ可能なエラーが発生します。

**TableDef** オブジェクトの **Indexes** コレクションを調べ、 **TableDef** オブジェクトから作成されたテーブル タイプの **Recordset** オブジェクトに使用できる **Index** オブジェクトを特定します。

テーブルの新しいインデックスを作成する場合は、新しい **Index** オブジェクトを作成し、そのプロパティを設定して、基になる **TableDef** オブジェクトの **Indexes** コレクションにそのオブジェクトを追加した後、再び **Recordset** オブジェクトを開きます。

テーブル タイプの **Recordset** オブジェクトは、基になる **TableDef** オブジェクトにインデックスを定義した場合にのみ、レコードを必要な順序で取得できます。 別の順序でレコードを並べ替えるには、ORDER BY 句を持つ SQL ステートメントを使用して、ダイナセット タイプ、スナップショット タイプまたは前方のみタイプの**Recordset**オブジェクトを開くことができます。


> [!NOTE]
> - テーブルにインデックスを作成するのは必須ではありません。大きなテーブルではインデックスを持たないと、特定のレコードへのアクセスまたは **Recordset** オブジェクトの作成に長い時間がかかる場合があります。一方、インデックスを多く作成しすぎると、すべてのインデックスが自動的に更新されるため、更新、追加、および削除を実行する速度が低下します。
> - インデックスを持たないテーブルから返されるレコードの順序は特定できません。
> - [Index](field-attributes-property-dao.md) オブジェクト内にある各 [**Field**](field-object-dao.md) オブジェクトの ****Attributes**** プロパティによってレコードの順序が決まり、その結果、そのインデックスに対して使用するアクセス方法が決まります。
> - 一意のインデックスを使用すると、最適な方法でレコードを検索できます。
> - インデックスを作成してもベース テーブルの物理的な順序は変更されません。インデックスによって変わるのは、特定のインデックスを選択するか、または **Recordset** オブジェクトを開いた場合に、テーブル タイプの **Recordset** オブジェクトでレコードにアクセスする方法のみです。


## <a name="example"></a>例

この例では、 **Index** プロパティを使用して、テーブル タイプの **Recordset** オブジェクトにさまざまなレコード順序を設定します。

```vb
    Sub IndexPropertyX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfEmployees As TableDef 
       Dim rstEmployees As Recordset 
       Dim idxLoop As Index 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees") 
       Set tdfEmployees = dbsNorthwind.TableDefs!Employees 
     
       With rstEmployees 
     
          ' Enumerate Indexes collection of Employees table. 
          For Each idxLoop In tdfEmployees.Indexes 
             .Index = idxLoop.Name 
             Debug.Print "Index = " & .Index 
             Debug.Print "  EmployeeID - PostalCode - Name" 
             .MoveFirst 
     
             ' Enumerate Recordset to show the order of records. 
             Do While Not .EOF 
                Debug.Print "    " & !EmployeeID & " - " & _ 
                   !PostalCode & " - " & !FirstName & " " & _ 
                   !LastName 
                .MoveNext 
             Loop 
     
          Next idxLoop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

この例では、 **Seek** メソッドを使用して、ユーザーが ID 番号に基づき製品を検索できるようにする方法を示します。

```vb
    Sub SeekX() 
     
       Dim dbsNorthwind As Database 
       Dim rstProducts As Recordset 
       Dim intFirst As Integer 
       Dim intLast As Integer 
       Dim strMessage As String 
       Dim strSeek As String 
       Dim varBookmark As Variant 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' You must open a table-type Recordset to use an index,  
       ' and hence the Seek method. 
       Set rstProducts = _ 
          dbsNorthwind.OpenRecordset("Products", dbOpenTable) 
     
       With rstProducts 
          ' Set the index. 
          .Index = "PrimaryKey" 
     
          ' Get the lowest and highest product IDs. 
          .MoveLast 
          intLast = !ProductID 
          .MoveFirst 
          intFirst = !ProductID 
     
          Do While True 
             ' Display current record information and ask user  
             ' for ID number. 
             strMessage = "Product ID: " & !ProductID & vbCr & _ 
                "Name: " & !ProductName & vbCr & vbCr & _ 
                "Enter a product ID between " & intFirst & _ 
                " and " & intLast & "." 
             strSeek = InputBox(strMessage) 
     
             If strSeek = "" Then Exit Do 
     
             ' Store current bookmark in case the Seek fails. 
             varBookmark = .Bookmark 
     
             .Seek "=", Val(strSeek) 
     
             ' Return to the current record if the Seek fails. 
             If .NoMatch Then 
                MsgBox "ID not found!" 
                .Bookmark = varBookmark 
             End If 
          Loop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

次の例は、 Seek メソッドを使用して、リンクしたテーブル内のレコードを見つける方法を示します。

**によって提供されるサンプル コード**を[Microsoft Access 2010 プログラマーズ リファレンス](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)です。

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
