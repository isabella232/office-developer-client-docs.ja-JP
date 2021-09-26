---
title: Recordset2.Index プロパティ (DAO)
TOCTitle: Index Property
ms:assetid: 614bdf53-aca3-25ef-a23c-50095b345d20
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194872(v=office.15)
ms:contentKeyID: 48545209
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: a01adf65d4358d12983c7d0c2e90aa9de02f1937
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611736"
---
# <a name="recordset2index-property-dao"></a>Recordset2.Index プロパティ (DAO)

**適用先**: Access 2013、Office 2013

テーブル型の **[Recordset](recordset-object-dao.md)** オブジェクト内の現在の **[Index](index-object-dao.md)** オブジェクトの名前を示す値を設定または返します (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式* .Index

*式* Recordset2 オブジェクトを **表す変数** 。

## <a name="remarks"></a>注釈

レコードはベース テーブルに特定の順序で格納されているわけではありません。 **Index** プロパティを設定すると、データベースから取得されるレコードの順序は変わりますが、格納されているレコードの順序は変わりません。

指定する **Index** オブジェクトは前もって定義しておく必要があります。存在していない **Index** オブジェクトに **Index** プロパティを設定するか、または [**Seek**](recordset2-seek-method-dao.md) メソッドを使用するときに **Index** プロパティが設定されていない場合、トラップ可能なエラーが発生します。

**TableDef** オブジェクトの **Indexes** コレクションを調べて、その **TableDef** オブジェクトから作成された、テーブル タイプの **Recordset** オブジェクトに使用できる **Index** オブジェクトを識別します。

テーブルの新しいインデックスを作成する場合は、新しい **Index** オブジェクトを作成し、そのプロパティを設定して、基になる **TableDef** オブジェクトの **Indexes** コレクションにそのオブジェクトを追加した後、再び **Recordset** オブジェクトを開きます。

テーブル タイプの **Recordset** オブジェクトは、基になる **TableDef** オブジェクトにインデックスを定義した場合にのみ、レコードを必要な順序で取得できます。別の順序でレコードを並べ替えるには、SQL ステートメントで ORDER BY 句を使用して、ダイナセット タイプ、スナップショット タイプ、または前方スクロール タイプの **Recordset** オブジェクトを開きます。

> [!NOTE]
> - テーブルにインデックスを作成するのは必須ではありません。大きなテーブルではインデックスを持たないと、特定のレコードへのアクセスまたは **Recordset** オブジェクトの作成に長い時間がかかる場合があります。一方、インデックスを多く作成しすぎると、すべてのインデックスが自動的に更新されるため、更新、追加、および削除を実行する速度が低下します。
> - インデックスを持たないテーブルから返されるレコードの順序は特定できません。
> - **Index** オブジェクト内にある各 **[Field](field-object-dao.md)** オブジェクトの **[Attributes](field-attributes-property-dao.md)** プロパティによってレコードの順序が決まり、その結果、そのインデックスに対して使用するアクセス方法が決まります。
> - 一意のインデックスを使用すると、最適な方法でレコードを検索できます。
> - インデックスは、ベース テーブルの物理的な順序には影響を与えません。特定のインデックスを選択するか、 **Recordset** オブジェクトを開く際の、テーブル タイプの **Recordset** オブジェクトによるレコードへのアクセス方法にのみ影響を与えます。

## <a name="example"></a>例

この例では、**Index** プロパティを使用して、テーブル タイプの **Recordset** オブジェクトにさまざまなレコード順序を設定します。

```vb
    Sub IndexPropertyX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfEmployees As TableDef 
       Dim rstEmployees As Recordset2 
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
       Dim rstProducts As Recordset2 
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
