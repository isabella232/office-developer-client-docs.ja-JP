---
title: インデックス オブジェクトのデータ アクセス オブジェクトの (DAO)
TOCTitle: Index Object
ms:assetid: 92c32cad-ec8a-1243-1d18-83f50b269ecb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197655(v=office.15)
ms:contentKeyID: 48546380
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5d4ed801dfa746af3ad649738e32cec58afe17f6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877080"
---
# <a name="index-object-dao"></a><span data-ttu-id="658dd-102">Index オブジェクト (DAO)</span><span class="sxs-lookup"><span data-stu-id="658dd-102">Index Object (DAO)</span></span>

<span data-ttu-id="658dd-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="658dd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="658dd-p101">**Index** オブジェクトは、データベース テーブルからアクセスされるレコードの順序、および重複するレコードを受け付けるかどうかを指定して、データに効率的にアクセスできるようにします。外部データベースの場合、 **Index** オブジェクトは、外部キー側のテーブルに対して設定されたインデックスを記述します (Microsoft Access ワークスペースの場合のみ)。</span><span class="sxs-lookup"><span data-stu-id="658dd-p101">**Index** objects specify the order of records accessed from database tables and whether or not duplicate records are accepted, providing efficient access to data. For external databases, **Index** objects describe the indexes established for external tables (Microsoft Access workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="658dd-106">注釈</span><span class="sxs-lookup"><span data-stu-id="658dd-106">Remarks</span></span>

<span data-ttu-id="658dd-p102">Microsoft Access データベース エンジンは、テーブルを結合して **[Recordset](recordset-object-dao.md)** オブジェクトを作成するときに、インデックスを使用します。インデックスにより、テーブル タイプの **Recordset** オブジェクトがレコードを返す順序は決定されますが、Microsoft Access データベース エンジンがベース テーブルにレコードを格納する順序、および他のタイプの **Recordset** オブジェクトがレコードを返す順序は決定されません。</span><span class="sxs-lookup"><span data-stu-id="658dd-p102">The Microsoft Access database engine uses indexes when it joins tables and creates **[Recordset](recordset-object-dao.md)** objects. Indexes determine the order in which table-type **Recordset** objects return records, but they don't determine the order in which the Microsoft Access database engine stores records in the base table or the order in which any other type of **Recordset** object returns records.</span></span>

<span data-ttu-id="658dd-109">**Index** オブジェクトを使用すると、以下の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="658dd-109">With an **Index** object, you can:</span></span>

- <span data-ttu-id="658dd-110">**Required** プロパティを使用して、インデックスの **[Field](field-object-dao.md)** オブジェクトに Null 以外の値が必要かどうかを特定し、 **IgnoreNulls** プロパティを使用して、Null 値がインデックスへのエントリを持つかどうかを特定します。</span><span class="sxs-lookup"><span data-stu-id="658dd-110">Use the **Required** property to determine whether the **[Field](field-object-dao.md)** objects in the index require values that are not Null, and then use the **IgnoreNulls** property to determine whether the null values have index entries.</span></span>

- <span data-ttu-id="658dd-111">**Primary** プロパティを使用して、 **Index** オブジェクトの順序を特定し、 **Unique** プロパティを使用して一意性を特定します。</span><span class="sxs-lookup"><span data-stu-id="658dd-111">Use the **Primary** and **Unique** properties to determine the ordering and uniqueness of the **Index** object.</span></span>

<span data-ttu-id="658dd-p103">Microsoft Access データベース エンジンは、すべてのベース テーブル インデックスを自動的に保守します。ベース テーブルのレコードに対して追加、変更、または削除を行うたびにインデックスを更新します。データベースを作成した後は、 **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** メソッドを定期的に使用して、インデックス統計を最新の状態にします。</span><span class="sxs-lookup"><span data-stu-id="658dd-p103">The Microsoft Access database engine maintains all base table indexes automatically. It updates indexes whenever you add, change, or delete records from the base table. Once you create the database, use the **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** method periodically to bring index statistics up-to-date.</span></span>

<span data-ttu-id="658dd-p104">テーブル タイプの **Recordset** オブジェクトにアクセスする場合、オブジェクトの **Index** プロパティを使用してレコードの順序を指定します。このプロパティを、 **Indexes** コレクションの既存の **Index** オブジェクトの **Name** プロパティの設定値に設定します。このコレクションは、操作する [Recordset](tabledef-object-dao.md) オブジェクトの基になる \*\*\*\*TableDef\*\*\*\* オブジェクトに含まれています。</span><span class="sxs-lookup"><span data-stu-id="658dd-p104">When accessing a table-type **Recordset** object, you specify the order of records using the object's **Index** property. Set this property to the **Name** property setting of an existing **Index** object in the **Indexes** collection. This collection is contained by the **[TableDef](tabledef-object-dao.md)** object underlying the **Recordset** object that you're populating.</span></span>

> [!NOTE]
> <P><span data-ttu-id="658dd-p105">[!メモ] テーブルのインデックスを作成する必要はありませんが、インデックスが設定されていない大きなテーブルの場合、特定のレコードへのアクセスまたは結合の処理に時間がかかることがあります。逆に、インデックスが多すぎると、テーブル インデックスがそれぞれ修正されるため、データベースの更新速度が遅くなる場合があります。</span><span class="sxs-lookup"><span data-stu-id="658dd-p105">You don't have to create indexes for a table, but for large, unindexed tables, accessing a specific record or processing joins can take a long time. Conversely, having too many indexes can slow down updates to the database as each of the table indexes is amended.</span></span></P>

<span data-ttu-id="658dd-120">インデックスの各 [Field](field-attributes-property-dao.md) オブジェクトの \*\*\*\*Attributes\*\*\*\* プロパティは、返されるレコードの順序を決定するため、そのインデックスに使用するアクセス方法も決定されます。</span><span class="sxs-lookup"><span data-stu-id="658dd-120">The **[Attributes](field-attributes-property-dao.md)** property of each **Field** object in the index determines the order of records returned and consequently determines which access techniques to use for that index.</span></span>

<span data-ttu-id="658dd-p106">**Index** オブジェクトの **Fields** コレクションの各 **Field** オブジェクトは、インデックスのコンポーネントです。新しい **Index** オブジェクトを定義するときには、コレクションに追加する前にそのプロパティを設定して、 **Index** オブジェクトを以降使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="658dd-p106">Each **Field** object in the **Fields** collection of an **Index** object is a component of the index. To define a new **Index** object, set its properties before you append it to a collection, making the **Index** object available for subsequent use.</span></span>

> [!NOTE]
> <P><span data-ttu-id="658dd-123">[!メモ] 既存の <STRONG>Index</STRONG> オブジェクトの <STRONG>Name</STRONG> プロパティの設定値を変更できるのは、それを含んでいる <A href="connection-updatable-property-dao.md">TableDef</A> オブジェクトの <STRONG><STRONG>Updatable</STRONG></STRONG> プロパティの設定値が <STRONG>True</STRONG> の場合のみです。</span><span class="sxs-lookup"><span data-stu-id="658dd-123">You can modify the <STRONG>Name</STRONG> property setting of an existing <STRONG>Index</STRONG> object only if the <STRONG><A href="connection-updatable-property-dao.md">Updatable</A></STRONG> property setting of the containing <STRONG>TableDef</STRONG> object is <STRONG>True</STRONG>.</span></span></P>

<span data-ttu-id="658dd-p107">テーブルの主キーを設定すると、Microsoft Access データベース エンジンでは、その主キーが主インデックスとして自動的に定義されます。主インデックスは、テーブルのすべてのレコードを定義済みの順序で一意に識別する、1 つ以上のフィールドで構成されます。主インデックス フィールドは一意である必要があるため、Microsoft Access データベース エンジンでは、主 **Index** オブジェクトの **Unique** プロパティが自動的に **True** に設定されます。主インデックスが複数のフィールドで構成される場合、各フィールドに重複する値を含めることができますが、インデックスが設定されたすべてのフィールドの値を組み合わせた結果は一意である必要があります。主インデックスはテーブルの 1 つのキーから成り、常に主キーと同じフィールドで構成されます。</span><span class="sxs-lookup"><span data-stu-id="658dd-p107">When you set a primary key for a table, the Microsoft Access database engine automatically defines it as the primary index. A primary index consists of one or more fields that uniquely identify all records in a table in a predefined order. Because the primary index field must be unique, the Microsoft Access database engine automatically sets the **Unique** property of the primary **Index** object to **True**. If the primary index consists of more than one field, each field can contain duplicate values, but the combination of values from all the indexed fields must be unique. A primary index consists of a key for the table and is always made up of the same fields as the primary key.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="658dd-p108">[!重要] データが新しいインデックスの属性に準拠していることを確認してください。インデックスに一意の値が必要な場合は、既存のデータ レコードに重複がないことを確認します。重複がある場合、Microsoft Access データベース エンジンはインデックスを作成できないため、新しいインデックスで Append メソッドを使用しようとすると、トラップ可能なエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="658dd-p108">Make sure your data complies with the attributes of your new index. If your index requires unique values, make sure that there are no duplicates in existing data records. If duplicates exist, the Microsoft Access database engine can't create the index; a trappable error results when you attempt to use the Append method on the new index.</span></span>

<span data-ttu-id="658dd-p109">参照整合性を適用するリレーションシップを作成すると、Microsoft Access データベース エンジンでは、 **Foreign** プロパティを持つインデックスが自動的に作成され、参照先テーブルで外部キーとして設定されます。テーブル リレーションシップを確立すると、Microsoft Access データベース エンジンでは、そのリレーションシップに反するデータベースへの追加または変更は行われません。 [**Relation**](relation-object-dao.md) オブジェクトの **Attributes** プロパティを、連鎖更新および連鎖削除を実行できるように設定すると、Microsoft Access データベース エンジンでは、関連するテーブルのレコードが自動的に更新または削除されます。</span><span class="sxs-lookup"><span data-stu-id="658dd-p109">When you create a relationship that enforces referential integrity, the Microsoft Access database engine automatically creates an index with the **Foreign** property, set as the foreign key in the referencing table. After you've established a table relationship, the Microsoft Access database engine prevents additions or changes to the database that violate that relationship. If you set the **Attributes** property of the **[Relation](relation-object-dao.md)** object to allow cascading updates and cascading deletes, the Microsoft Access database engine updates or deletes records in related tables automatically.</span></span>

1.  <span data-ttu-id="658dd-135">**TableDef** オブジェクトに対して **CreateIndex** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="658dd-135">Use the **CreateIndex** method on a **TableDef** object.</span></span>

2.  <span data-ttu-id="658dd-136">**Index** オブジェクトに対して **CreateField** メソッドを使用して、フィールド (列) ごとに **Index** に含まれる **Field** オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="658dd-136">Use the **CreateField** method on the **Index** object to create a **Field** object for each field (column) to be included in the **Index** object.</span></span>

3.  <span data-ttu-id="658dd-137">必要に応じて、 **Index** プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="658dd-137">Set **Index** properties as needed.</span></span>

4.  <span data-ttu-id="658dd-138">**Field** オブジェクトを **Fields** コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="658dd-138">Append the **Field** object to the **Fields** collection.</span></span>

5.  <span data-ttu-id="658dd-139">**Index** オブジェクトを **Indexes** コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="658dd-139">Append the **Index** object to the **Indexes** collection.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="658dd-140">[!メモ] クラスター化インデックスをサポートしていない Microsoft Access データベース エンジンを使用するデータベースの場合、 <STRONG>Clustered</STRONG> プロパティは無視されます。</span><span class="sxs-lookup"><span data-stu-id="658dd-140">The <STRONG>Clustered</STRONG> property is ignored for databases that use the Microsoft Access database engine, which doesn't support clustered indexes.</span></span></P>



## <a name="example"></a><span data-ttu-id="658dd-141">例</span><span class="sxs-lookup"><span data-stu-id="658dd-141">Example</span></span>

<span data-ttu-id="658dd-p110">この例では、新しい **Index** オブジェクトを作成し、Employees **TableDef** の **Indexes** コレクションに追加し、次に **TableDef** の **Indexes** コレクションを列挙します。その後に、まずプライマリ **Index** を使用し、次に新しい **Index** を使用して、 **Recordset** を列挙します。このプロシージャを実行するには、IndexOutput プロシージャが必要です。</span><span class="sxs-lookup"><span data-stu-id="658dd-p110">This example creates a new **Index** object, appends it to the **Indexes** collection of the Employees **TableDef**, and then enumerates the **Indexes** collection of the **TableDef**. Finally, it enumerates a **Recordset**, first using the primary **Index**, and then using the new **Index**. The IndexOutput procedure is required for this procedure to run.</span></span>

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

<span data-ttu-id="658dd-p111">この例では、 **CreateIndex** メソッドを使用して 2 つの **Index** オブジェクトを新規作成し、Employees **TableDef** オブジェクトの **Indexes** コレクションに追加します。次に、 **TableDef** オブジェクトの **Indexes** コレクション、新しい **Index** オブジェクトの **Fields** コレクション、および新しい **Index** オブジェクトの Properties コレクションを列挙します。このプロシージャを実行するには、CreateIndexOutput 関数が必要です。</span><span class="sxs-lookup"><span data-stu-id="658dd-p111">This example uses the **CreateIndex** method to create two new **Index** objects and then appends them to the **Indexes** collection of the Employees **TableDef** object. It then enumerates the **Indexes** collection of the **TableDef** object, the **Fields** collection of the new **Index** objects, and the Properties collection of the new **Index** objects. The CreateIndexOutput function is required for this procedure to run.</span></span>

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
