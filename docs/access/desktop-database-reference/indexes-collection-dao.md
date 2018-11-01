---
title: Indexes コレクション (DAO)
TOCTitle: Indexes Collection
ms:assetid: 26450e85-c79d-b12a-d760-dfc89c37f36c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191889(v=office.15)
ms:contentKeyID: 48543802
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 96bd1e51f3e8a0ea88c97835ab5b0c3b43419c46
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877374"
---
# <a name="indexes-collection-dao"></a><span data-ttu-id="f483f-102">Indexes コレクション (DAO)</span><span class="sxs-lookup"><span data-stu-id="f483f-102">Indexes Collection (DAO)</span></span>


<span data-ttu-id="f483f-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="f483f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f483f-104">**Indexes** コレクションには、格納されているすべての **TableDef** オブジェクトの **Index** オブジェクトが含まれます (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="f483f-104">An **Indexes** collection contains all the stored **Index** objects of a **TableDef** object (Microsoft Access workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="f483f-105">注釈</span><span class="sxs-lookup"><span data-stu-id="f483f-105">Remarks</span></span>

<span data-ttu-id="f483f-p101">テーブル タイプの Recordset オブジェクトにアクセスする場合は、オブジェクトの **Index** プロパティを使用してレコードの順序を指定します。このプロパティを \*\*\*\*Recordset\*\*\*\* オブジェクトの元になっている [**TableDef**](tabledef-object-dao.md) の **Indexes** コレクションの既存の [Index](recordset-object-dao.md) オブジェクトの **Name** プロパティに設定します。</span><span class="sxs-lookup"><span data-stu-id="f483f-p101">When you access a table-type Recordset object, use the object's **Index** property to specify the order of records. Set this property to the **Name** property setting of an existing **Index** object in the **Indexes** collection of the **[TableDef](tabledef-object-dao.md)** object underlying the **[Recordset](recordset-object-dao.md)** object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="f483f-108">[!メモ] <STRONG>Append</STRONG> または <STRONG>Delete</STRONG> メソッドを <STRONG>Indexes</STRONG> コレクションに使用できるのは、元になる <A href="connection-updatable-property-dao.md">TableDef</A> オブジェクトの <STRONG><STRONG>Updatable</STRONG></STRONG> プロパティの設定が <STRONG>True</STRONG> の場合のみです。</span><span class="sxs-lookup"><span data-stu-id="f483f-108">You can use the <STRONG>Append</STRONG> or <STRONG>Delete</STRONG> method on an <STRONG>Indexes</STRONG> collection only if the <STRONG><A href="connection-updatable-property-dao.md">Updatable</A></STRONG> property setting of the containing <STRONG>TableDef</STRONG> object is <STRONG>True</STRONG>.</span></span></P>



<span data-ttu-id="f483f-109">新しい **Index** オブジェクトを作成した後は、 **Append** メソッドを使用して **TableDef** オブジェクトの **Indexes** コレクションに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f483f-109">After you create a new **Index** object, you should use the **Append** method to add it to the **TableDef** object's **Indexes** collection.</span></span>


> [!IMPORTANT]
> <P><span data-ttu-id="f483f-p102">[!重要] データが新しいインデックスの属性に準拠している必要があります。インデックスに一意の値が必要な場合は、既存のデータ レコードに重複値がないことを確認します。重複がある場合は、Microsoft Access データベース エンジンはインデックスを作成できません。新しいインデックスに Append メソッドを使用しようとすると、トラップ可能なエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f483f-p102">Make sure your data complies with the attributes of your new index. If your index requires unique values, make sure that there are no duplicates in existing data records. If duplicates exist, the Microsoft Access database engine can't create the index; a trappable error results when you attempt to use the Append method on the new index.</span></span></P>



## <a name="example"></a><span data-ttu-id="f483f-113">例</span><span class="sxs-lookup"><span data-stu-id="f483f-113">Example</span></span>

<span data-ttu-id="f483f-p103">この例では、新しい **Index** オブジェクトを作成し、Employees **TableDef** の **Indexes** コレクションに追加し、次に **TableDef** の **Indexes** コレクションを列挙します。その後に、まずプライマリ **Index** を使用し、次に新しい **Index** を使用して、 **Recordset** を列挙します。このプロシージャを実行するには、IndexOutput プロシージャが必要です。</span><span class="sxs-lookup"><span data-stu-id="f483f-p103">This example creates a new **Index** object, appends it to the **Indexes** collection of the Employees **TableDef**, and then enumerates the **Indexes** collection of the **TableDef**. Finally, it enumerates a **Recordset**, first using the primary **Index**, and then using the new **Index**. The IndexOutput procedure is required for this procedure to run.</span></span>

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

<span data-ttu-id="f483f-p104">この例では、 **CreateIndex** メソッドを使用して 2 つの **Index** オブジェクトを新規作成し、Employees **TableDef** オブジェクトの **Indexes** コレクションに追加します。次に、 **TableDef** オブジェクトの **Indexes** コレクション、新しい **Index** オブジェクトの **Fields** コレクション、および新しい **Index** オブジェクトの Properties コレクションを列挙します。このプロシージャを実行するには、CreateIndexOutput 関数が必要です。</span><span class="sxs-lookup"><span data-stu-id="f483f-p104">This example uses the **CreateIndex** method to create two new **Index** objects and then appends them to the **Indexes** collection of the Employees **TableDef** object. It then enumerates the **Indexes** collection of the **TableDef** object, the **Fields** collection of the new **Index** objects, and the Properties collection of the new **Index** objects. The CreateIndexOutput function is required for this procedure to run.</span></span>

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
