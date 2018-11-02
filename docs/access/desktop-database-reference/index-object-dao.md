---
title: インデックス オブジェクトのデータ アクセス オブジェクトの (DAO)
TOCTitle: Index Object
ms:assetid: 92c32cad-ec8a-1243-1d18-83f50b269ecb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197655(v=office.15)
ms:contentKeyID: 48546380
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cc849e22da654bd384065e4c169b3fd5540c6061
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928965"
---
# <a name="index-object-dao"></a>インデックス オブジェクト (DAO)

**適用されます**Access 2013、Office 2013。

**Index** オブジェクトは、データベース テーブルからアクセスされるレコードの順序、および重複するレコードを受け付けるかどうかを指定して、データに効率的にアクセスできるようにします。外部データベースの場合、 **Index** オブジェクトは、外部キー側のテーブルに対して設定されたインデックスを記述します (Microsoft Access ワークスペースの場合のみ)。

## <a name="remarks"></a>注釈

Microsoft Access データベース エンジンは、テーブルを結合して **[Recordset](recordset-object-dao.md)** オブジェクトを作成するときに、インデックスを使用します。インデックスにより、テーブル タイプの **Recordset** オブジェクトがレコードを返す順序は決定されますが、Microsoft Access データベース エンジンがベース テーブルにレコードを格納する順序、および他のタイプの **Recordset** オブジェクトがレコードを返す順序は決定されません。

**Index** オブジェクトを使用すると、以下の操作を実行できます。

- **Required** プロパティを使用して、インデックスの **[Field](field-object-dao.md)** オブジェクトに Null 以外の値が必要かどうかを特定し、 **IgnoreNulls** プロパティを使用して、Null 値がインデックスへのエントリを持つかどうかを特定します。

- **Primary** プロパティを使用して、 **Index** オブジェクトの順序を特定し、 **Unique** プロパティを使用して一意性を特定します。

Microsoft Access データベース エンジンは、すべてのベース テーブル インデックスを自動的に保守します。ベース テーブルのレコードに対して追加、変更、または削除を行うたびにインデックスを更新します。データベースを作成した後は、 **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** メソッドを定期的に使用して、インデックス統計を最新の状態にします。

テーブル タイプの **Recordset** オブジェクトにアクセスする場合、オブジェクトの **Index** プロパティを使用してレコードの順序を指定します。このプロパティを、 **Indexes** コレクションの既存の **Index** オブジェクトの **Name** プロパティの設定値に設定します。このコレクションは、操作する [Recordset](tabledef-object-dao.md) オブジェクトの基になる ****TableDef**** オブジェクトに含まれています。

> [!NOTE]
> <P>[!メモ] テーブルのインデックスを作成する必要はありませんが、インデックスが設定されていない大きなテーブルの場合、特定のレコードへのアクセスまたは結合の処理に時間がかかることがあります。逆に、インデックスが多すぎると、テーブル インデックスがそれぞれ修正されるため、データベースの更新速度が遅くなる場合があります。</P>

インデックスの各 [Field](field-attributes-property-dao.md) オブジェクトの ****Attributes**** プロパティは、返されるレコードの順序を決定するため、そのインデックスに使用するアクセス方法も決定されます。

**Index** オブジェクトの **Fields** コレクションの各 **Field** オブジェクトは、インデックスのコンポーネントです。新しい **Index** オブジェクトを定義するときには、コレクションに追加する前にそのプロパティを設定して、 **Index** オブジェクトを以降使用できるようにします。

> [!NOTE]
> <P>[!メモ] 既存の <STRONG>Index</STRONG> オブジェクトの <STRONG>Name</STRONG> プロパティの設定値を変更できるのは、それを含んでいる <A href="connection-updatable-property-dao.md">TableDef</A> オブジェクトの <STRONG><STRONG>Updatable</STRONG></STRONG> プロパティの設定値が <STRONG>True</STRONG> の場合のみです。</P>

テーブルの主キーを設定すると、Microsoft Access データベース エンジンでは、その主キーが主インデックスとして自動的に定義されます。主インデックスは、テーブルのすべてのレコードを定義済みの順序で一意に識別する、1 つ以上のフィールドで構成されます。主インデックス フィールドは一意である必要があるため、Microsoft Access データベース エンジンでは、主 **Index** オブジェクトの **Unique** プロパティが自動的に **True** に設定されます。主インデックスが複数のフィールドで構成される場合、各フィールドに重複する値を含めることができますが、インデックスが設定されたすべてのフィールドの値を組み合わせた結果は一意である必要があります。主インデックスはテーブルの 1 つのキーから成り、常に主キーと同じフィールドで構成されます。

> [!IMPORTANT]
> [!重要] データが新しいインデックスの属性に準拠していることを確認してください。インデックスに一意の値が必要な場合は、既存のデータ レコードに重複がないことを確認します。重複がある場合、Microsoft Access データベース エンジンはインデックスを作成できないため、新しいインデックスで Append メソッドを使用しようとすると、トラップ可能なエラーが発生します。

参照整合性を適用するリレーションシップを作成すると、Microsoft Access データベース エンジンでは、 **Foreign** プロパティを持つインデックスが自動的に作成され、参照先テーブルで外部キーとして設定されます。テーブル リレーションシップを確立すると、Microsoft Access データベース エンジンでは、そのリレーションシップに反するデータベースへの追加または変更は行われません。 [**Relation**](relation-object-dao.md) オブジェクトの **Attributes** プロパティを、連鎖更新および連鎖削除を実行できるように設定すると、Microsoft Access データベース エンジンでは、関連するテーブルのレコードが自動的に更新または削除されます。

1.  **TableDef** オブジェクトに対して **CreateIndex** メソッドを使用します。

2.  **Index** オブジェクトに対して **CreateField** メソッドを使用して、フィールド (列) ごとに **Index** に含まれる **Field** オブジェクトを作成します。

3.  必要に応じて、 **Index** プロパティを設定します。

4.  **Field** オブジェクトを **Fields** コレクションに追加します。

5.  **Index** オブジェクトを **Indexes** コレクションに追加します。
    

    > [!NOTE]
    > <P>[!メモ] クラスター化インデックスをサポートしていない Microsoft Access データベース エンジンを使用するデータベースの場合、 <STRONG>Clustered</STRONG> プロパティは無視されます。</P>



## <a name="example"></a>例

この例では、新しい **Index** オブジェクトを作成し、Employees **TableDef** の **Indexes** コレクションに追加し、次に **TableDef** の **Indexes** コレクションを列挙します。その後に、まずプライマリ **Index** を使用し、次に新しい **Index** を使用して、 **Recordset** を列挙します。このプロシージャを実行するには、IndexOutput プロシージャが必要です。

```vb
    Sub IndexObjectX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxNew As Index 
     Dim idxLoop As Index 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create new index, create and append Field 
     ' objects to its Fields collection. 
     Set idxNew = .CreateIndex("NewIndex") 
     
     With idxNew 
     .Fields.Append .CreateField("Country") 
     .Fields.Append .CreateField("LastName") 
     .Fields.Append .CreateField("FirstName") 
     End With 
     
     ' Add new Index object to the Indexes collection 
     ' of the Employees table collection. 
     .Indexes.Append idxNew 
     .Indexes.Refresh 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection of Employees 
     ' table. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Next idxLoop 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     ' Print report using old and new indexes. 
     IndexOutput rstEmployees, "PrimaryKey" 
     IndexOutput rstEmployees, idxNew.Name 
     rstEmployees.Close 
     
     ' Delete new Index because this is a 
     ' demonstration. 
     .Indexes.Delete idxNew.Name 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub IndexOutput(rstTemp As Recordset, _ 
     strIndex As String) 
     ' Report function for FieldX. 
     
     With rstTemp 
     ' Set the index. 
     .Index = strIndex 
     .MoveFirst 
     Debug.Print "Recordset = " & .Name & _ 
     ", Index = " & .Index 
     Debug.Print " EmployeeID - Country - Name" 
     
     ' Enumerate the recordset using the specified 
     ' index. 
     Do While Not .EOF 
     Debug.Print " " & !EmployeeID & " - " & _ 
     !Country & " - " & !LastName & ", " & !FirstName 
     .MoveNext 
     Loop 
     
     End With 
     
    End Sub 
```

<br/>

この例では、 **CreateIndex** メソッドを使用して 2 つの **Index** オブジェクトを新規作成し、Employees **TableDef** オブジェクトの **Indexes** コレクションに追加します。次に、 **TableDef** オブジェクトの **Indexes** コレクション、新しい **Index** オブジェクトの **Fields** コレクション、および新しい **Index** オブジェクトの Properties コレクションを列挙します。このプロシージャを実行するには、CreateIndexOutput 関数が必要です。

```vb
    Sub CreateIndexX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxCountry As Index 
     Dim idxFirstName As Index 
     Dim idxLoop As Index 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create first Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxCountry = .CreateIndex("CountryIndex") 
     With idxCountry 
     .Fields.Append .CreateField("Country") 
     .Fields.Append .CreateField("LastName") 
     .Fields.Append .CreateField("FirstName") 
     End With 
     .Indexes.Append idxCountry 
     
     ' Create second Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxFirstName = .CreateIndex 
     With idxFirstName 
     .Name = "FirstNameIndex" 
     .Fields.Append .CreateField("FirstName") 
     .Fields.Append .CreateField("LastName") 
     End With 
     .Indexes.Append idxFirstName 
     
     ' Refresh collection so that you can access new Index 
     ' objects. 
     .Indexes.Refresh 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Next idxLoop 
     
     ' Print report. 
     CreateIndexOutput idxCountry 
     CreateIndexOutput idxFirstName 
     
     ' Delete new Index objects because this is a 
     ' demonstration. 
     .Indexes.Delete idxCountry.Name 
     .Indexes.Delete idxFirstName.Name 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function CreateIndexOutput(idxTemp As Index) 
     
     Dim fldLoop As Field 
     Dim prpLoop As Property 
     
     With idxTemp 
     ' Enumerate Fields collection of Index object. 
     Debug.Print "Fields in " & .Name 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name 
     Next fldLoop 
     
     ' Enumerate Properties collection of Index object. 
     Debug.Print "Properties of " & .Name 
     For Each prpLoop In .Properties 
     Debug.Print " " & prpLoop.Name & " - " & _ 
     IIf(prpLoop = "", "[empty]", prpLoop) 
     Next prpLoop 
     End With 
     
    End Function
```
