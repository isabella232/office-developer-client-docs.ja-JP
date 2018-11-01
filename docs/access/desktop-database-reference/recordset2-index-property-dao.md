---
title: Recordset2.Index プロパティ (DAO)
TOCTitle: Index Property
ms:assetid: 614bdf53-aca3-25ef-a23c-50095b345d20
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194872(v=office.15)
ms:contentKeyID: 48545209
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 897fa6fc41657f1291a726a7ac86b2c6d579abee
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885865"
---
# <a name="recordset2index-property-dao"></a>Recordset2.Index プロパティ (DAO)


**適用されます**Access 2013、Office 2013。

テーブル タイプの **[Recordset](index-object-dao.md)** オブジェクト内にある現在の **[Index](recordset-object-dao.md)** オブジェクトの名前を示す値を設定または取得します (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式*です。インデックス

*式***Recordset2**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

レコードはベース テーブルに特定の順序で格納されているわけではありません。 **Index** プロパティを設定すると、データベースから取得されるレコードの順序は変わりますが、格納されているレコードの順序は変わりません。

指定する **Index** オブジェクトは前もって定義しておく必要があります。存在していない **Index** オブジェクトに **Index** プロパティを設定するか、または [**Seek**](recordset2-seek-method-dao.md) メソッドを使用するときに **Index** プロパティが設定されていない場合、トラップ可能なエラーが発生します。

**TableDef** オブジェクトの **Indexes** コレクションを調べ、 **TableDef** オブジェクトから作成されたテーブル タイプの **Recordset** オブジェクトに使用できる **Index** オブジェクトを特定します。

テーブルの新しいインデックスを作成する場合は、新しい **Index** オブジェクトを作成し、そのプロパティを設定して、基になる **TableDef** オブジェクトの **Indexes** コレクションにそのオブジェクトを追加した後、再び **Recordset** オブジェクトを開きます。

テーブル タイプの **Recordset** オブジェクトは、基になる **TableDef** オブジェクトにインデックスを定義した場合にのみ、レコードを必要な順序で取得できます。 別の順序でレコードを並べ替えるには、ORDER BY 句を持つ SQL ステートメントを使用して、ダイナセット タイプ、スナップショット タイプまたは前方のみタイプの**Recordset**オブジェクトを開くことができます。


> [!NOTE]
> <UL>
> <LI>
> <P>テーブルにインデックスを作成するのは必須ではありません。大きなテーブルではインデックスを持たないと、特定のレコードへのアクセスまたは <STRONG>Recordset</STRONG> オブジェクトの作成に長い時間がかかる場合があります。一方、インデックスを多く作成しすぎると、すべてのインデックスが自動的に更新されるため、更新、追加、および削除を実行する速度が低下します。</P>
> <LI>
> <P>インデックスを持たないテーブルから返されるレコードの順序は特定できません。</P>
> <LI>
> <P><A href="field-attributes-property-dao.md">Index</A> オブジェクト内にある各 <A href="field-object-dao.md"><STRONG>Field</STRONG></A> オブジェクトの <STRONG><STRONG>Attributes</STRONG></STRONG> プロパティによってレコードの順序が決まり、その結果、そのインデックスに対して使用するアクセス方法が決まります。</P>
> <LI>
> <P>一意のインデックスを使用すると、最適な方法でレコードを検索できます。</P>
> <LI>
> <P>インデックスは、ベース テーブルの物理的な順序には影響を与えません。特定のインデックスを選択するか、 <STRONG>Recordset</STRONG> オブジェクトを開く際の、テーブル タイプの <STRONG>Recordset</STRONG> オブジェクトによるレコードへのアクセス方法にのみ影響を与えます。</P></LI></UL>



## <a name="example"></a>例

この例では、 **Index** プロパティを使用して、テーブル タイプの **Recordset** オブジェクトにさまざまなレコード順序を設定します。

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
