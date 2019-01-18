---
title: リレーションシップ オブジェクト (DAO)
TOCTitle: Relation Object
ms:assetid: 46d6dfaf-a97d-3abd-0b4b-396a41eb3be7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193195(v=office.15)
ms:contentKeyID: 48544578
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3eeaf8bf46d8673731243a1161ac578062a01f89
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716279"
---
# <a name="relation-object-dao"></a><span data-ttu-id="23ab4-102">リレーションシップ オブジェクト (DAO)</span><span class="sxs-lookup"><span data-stu-id="23ab4-102">Relation object (DAO)</span></span>


<span data-ttu-id="23ab4-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="23ab4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="23ab4-104">**Relation** オブジェクトは、テーブルまたはクエリのフィールド間のリレーションシップを表します (Microsoft Access データベース エンジン データベースのみ)。</span><span class="sxs-lookup"><span data-stu-id="23ab4-104">A **Relation** object represents a relationship between fields in tables or queries (Microsoft Access database engine databases only).</span></span>

## <a name="remarks"></a><span data-ttu-id="23ab4-105">注釈</span><span class="sxs-lookup"><span data-stu-id="23ab4-105">Remarks</span></span>

<span data-ttu-id="23ab4-106">**Relation** オブジェクトを使用して、新しいリレーションシップを作成し、データベースの既存のリレーションシップを調べることができます。</span><span class="sxs-lookup"><span data-stu-id="23ab4-106">You can use the **Relation** object to create new relationships and examine existing relationships in your database.</span></span>

<span data-ttu-id="23ab4-107">**Relation** オブジェクトとそのプロパティを使用して、以下の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="23ab4-107">Using a **Relation** object and its properties, you can:</span></span>

  - <span data-ttu-id="23ab4-108">ベース テーブルのフィールド間に、参照性合成が適用されたリレーションシップを指定します (クエリまたはリンク テーブル関連のリレーションシップは除く)。</span><span class="sxs-lookup"><span data-stu-id="23ab4-108">Specify an enforced relationship between fields in base tables (but not a relationship that involves a query or a linked table).</span></span>

  - <span data-ttu-id="23ab4-109">あらゆる種類のテーブルまたはクエリ (ネイティブまたはリンク) 間に参照整合性が適用されていないリレーションシップを設定します。</span><span class="sxs-lookup"><span data-stu-id="23ab4-109">Establish unenforced relationships between any type of table or query— native or linked.</span></span>

  - <span data-ttu-id="23ab4-110">**Name** プロパティを使用して、参照先の主テーブルと参照元の外部キー側のテーブルのフィールド間のリレーションシップを参照します。</span><span class="sxs-lookup"><span data-stu-id="23ab4-110">Use the **Name** property to refer to the relationship between the fields in the referenced primary table and the referencing foreign table.</span></span>

  - <span data-ttu-id="23ab4-111">**Attributes** プロパティを使用して、テーブルのフィールド間のリレーションシップが一対一か一対多のいずれかを指定し、参照整合性を適用する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="23ab4-111">Use the **Attributes** property to determine whether the relationship between fields in the table is one-to-one or one-to-many and how to enforce referential integrity.</span></span>

  - <span data-ttu-id="23ab4-112">**Attributes** プロパティを使用して、Microsoft Access データベース エンジンが主テーブルと外部キー側のテーブルで連鎖更新操作および連鎖削除操作を実行できるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="23ab4-112">Use the **Attributes** property to determine whether the Microsoft Access database engine can perform cascading update and cascading delete operations on primary and foreign tables.</span></span>

  - <span data-ttu-id="23ab4-113">**Attributes** プロパティを使用して、テーブルのフィールド間のリレーションシップが左外部結合か、右外部結合かを指定します。</span><span class="sxs-lookup"><span data-stu-id="23ab4-113">Use the **Attributes** property to determine whether the relationship between fields in the table is left join or right join.</span></span>

  - <span data-ttu-id="23ab4-114">**Relation** オブジェクトの **Fields** コレクションにあるすべての **Field** オブジェクトの **Name** プロパティを使用して、参照先テーブルの主キーのフィールド名を設定または取得するか、 **Field** オブジェクトの **ForeignName** プロパティの設定値を使用して、参照元テーブルの外部キーのフィールド名を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="23ab4-114">Use the **Name** property of all **Field** objects in the **Fields** collection of a **Relation** object to set or return the names of the fields in the primary key of the referenced table, or the **ForeignName** property settings of the **Field** objects to set or return the names of the fields in the foreign key of the referencing table.</span></span>

<span data-ttu-id="23ab4-p101">データベースに設定されたリレーションシップに違反する変更を行うと、トラップ可能なエラーが発生します。連鎖更新または連鎖削除操作を要求すると、Microsoft Access データベース エンジンでは、設定したリレーションシップを適用するために、主キー テーブルまたは外部キー テーブルも変更されます。</span><span class="sxs-lookup"><span data-stu-id="23ab4-p101">If you make changes that violate the relationships established for the database, a trappable error occurs. If you request cascading update or cascading delete operations, the Microsoft Access database engine also modifies the primary key or foreign key tables to enforce the relationships you establish.</span></span>

<span data-ttu-id="23ab4-p102">たとえば、Northwind データベースに、[受注] テーブルと [顧客] テーブルの間のリレーションシップがあるとします。[顧客] テーブルの CustomerID フィールドが主キーで、[受注] テーブルの CustomerID フィールドが外部キーです。Microsoft Access データベース エンジンが [受注] テーブルの新しいレコードを受け取るには、[顧客] テーブルに [受注] テーブルの CustomerID フィールドと一致するフィールドがあるかどうかを検索します。一致するフィールドが見つからなかった場合、Microsoft Access データベース エンジンは新しいレコードを受け取らず、トラップ可能なエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="23ab4-p102">For example, the Northwind database contains a relationship between an Orders table and a Customers table. The CustomerID field of the Customers table is the primary key, and the CustomerID field of the Orders table is the foreign key. For the Microsoft Access database engine to accept a new record in the Orders table, it searches the Customers table for a match on the CustomerID field of the Orders table. If the Microsoft Access database engine doesn't find a match, it doesn't accept the new record, and a trappable error occurs.</span></span>

<span data-ttu-id="23ab4-p103">参照整合性を適用する場合、参照先テーブルのキー フィールドに一意のインデックスが既に存在している必要があります。Microsoft Access データベース エンジンでは、 **Foreign** プロパティが参照元テーブルの外部キーとして機能するように設定されたインデックスが自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="23ab4-p103">When you enforce referential integrity, a unique index must already exist for the key field of the referenced table. The Microsoft Access database engine automatically creates an index with the **Foreign** property set to act as the foreign key in the referencing table.</span></span>

<span data-ttu-id="23ab4-p104">新しい **Relation** オブジェクトを作成するには、 **CreateRelation** メソッドを使用します。コレクション内の **Relation** オブジェクトを、コレクションで付けられたインデックスまたは **Name** プロパティの設定値で参照するには、次のいずれかの構文を使います。</span><span class="sxs-lookup"><span data-stu-id="23ab4-p104">To create a new **Relation** object, use the **CreateRelation** method. To refer to a **Relation** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="23ab4-125">**Relations**(0)</span><span class="sxs-lookup"><span data-stu-id="23ab4-125">**Relations**(0)</span></span>

<span data-ttu-id="23ab4-126">**関係**("name")</span><span class="sxs-lookup"><span data-stu-id="23ab4-126">**Relations**("name")</span></span>

<span data-ttu-id="23ab4-127">**関係**\!\[名\]</span><span class="sxs-lookup"><span data-stu-id="23ab4-127">**Relations**\!\[name\]</span></span>

## <a name="example"></a><span data-ttu-id="23ab4-128">例</span><span class="sxs-lookup"><span data-stu-id="23ab4-128">Example</span></span>

<span data-ttu-id="23ab4-p105">この例では、既存の **Relation** オブジェクトがデータ入力を制御する方法を示します。このプロシージャは、故意に正しくない CategoryID を使用してレコードを追加します。これによって、エラー処理ルーチンが起動します。</span><span class="sxs-lookup"><span data-stu-id="23ab4-p105">This example shows how an existing **Relation** object can control data entry. The procedure attempts to add a record with a deliberately incorrect CategoryID; this triggers the error-handling routine.</span></span>

```vb 
    Sub RelationX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset 
     Dim prpLoop As Property 
     Dim fldLoop As Field 
     Dim errLoop As Error 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstProducts = dbsNorthwind.OpenRecordset("Products") 
     
     ' Print a report showing all the different parts of 
     ' the relation and where each part is stored. 
     With dbsNorthwind.Relations!CategoriesProducts 
     Debug.Print "Properties of " & .Name & " Relation" 
     Debug.Print " Table = " & .Table 
     Debug.Print " ForeignTable = " & .ForeignTable 
     Debug.Print "Fields of " & .Name & " Relation" 
     With .Fields!CategoryID 
     Debug.Print " " & .Name 
     Debug.Print " Name = " & .Name 
     Debug.Print " ForeignName = " & .ForeignName 
     End With 
     End With 
     
     ' Attempt to add a record that violates the relation. 
     With rstProducts 
     .AddNew 
     !ProductName = "Trygve's Lutefisk" 
     !CategoryID = 10 
     On Error GoTo Err_Relation 
     .Update 
     On Error GoTo 0 
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
     Exit Sub 
     
    Err_Relation: 
     
     ' Notify user of any errors that result from 
     ' the invalid data. 
     If DBEngine.Errors.Count > 0 Then 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & _ 
     vbCr & errLoop.Description 
     Next errLoop 
     End If 
     
     Resume Next 
     
    End Sub 
```

<br/>

<span data-ttu-id="23ab4-131">この例では、 **CreateRelation** メソッドを使用して、Employees **TableDef** と新規作成された Departments という **TableDef** の間に **Relation** を作成します。</span><span class="sxs-lookup"><span data-stu-id="23ab4-131">This example uses the **CreateRelation** method to create a **Relation** between the Employees **TableDef** and a new **TableDef** called Departments.</span></span> <span data-ttu-id="23ab4-132">新しい**リレーション**を作成するがも作成方法、必要な**インデックス**テーブル (Employees テーブルの DepartmentsEmployees インデックス) のも示します。</span><span class="sxs-lookup"><span data-stu-id="23ab4-132">It also demonstrates how creating a new **Relation** will also create any necessary **Indexes** in the foreign table (the DepartmentsEmployees Index in the Employees table).</span></span>

```vb
    Sub CreateRelationX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim tdfNew As TableDef 
     Dim idxNew As Index 
     Dim relNew As Relation 
     Dim idxLoop As Index 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Add new field to Employees table. 
     Set tdfEmployees = .TableDefs!Employees 
     tdfEmployees.Fields.Append _ 
     tdfEmployees.CreateField("DeptID", dbInteger, 2) 
     
     ' Create new Departments table. 
     Set tdfNew = .CreateTableDef("Departments") 
     
     With tdfNew 
     ' Create and append Field objects to Fields 
     ' collection of the new TableDef object. 
     .Fields.Append .CreateField("DeptID", dbInteger, 2) 
     .Fields.Append .CreateField("DeptName", dbText, 20) 
     
     ' Create Index object for Departments table. 
     Set idxNew = .CreateIndex("DeptIDIndex") 
     ' Create and append Field object to Fields 
     ' collection of the new Index object. 
     idxNew.Fields.Append idxNew.CreateField("DeptID") 
     ' The index in the primary table must be Unique in 
     ' order to be part of a Relation. 
     idxNew.Unique = True 
     .Indexes.Append idxNew 
     End With 
     
     .TableDefs.Append tdfNew 
     
     ' Create EmployeesDepartments Relation object, using 
     ' the names of the two tables in the relation. 
     Set relNew = .CreateRelation("EmployeesDepartments", _ 
     tdfNew.Name, tdfEmployees.Name, _ 
     dbRelationUpdateCascade) 
     
     ' Create Field object for the Fields collection of the 
     ' new Relation object. Set the Name and ForeignName 
     ' properties based on the fields to be used for the 
     ' relation. 
     relNew.Fields.Append relNew.CreateField("DeptID") 
     relNew.Fields!DeptID.ForeignName = "DeptID" 
     .Relations.Append relNew 
     
     ' Print report. 
     Debug.Print "Properties of " & relNew.Name & _ 
     " Relation" 
     Debug.Print " Table = " & relNew.Table 
     Debug.Print " ForeignTable = " & _ 
     relNew.ForeignTable 
     Debug.Print "Fields of " & relNew.Name & " Relation" 
     
     With relNew.Fields!DeptID 
     Debug.Print " " & .Name 
     Debug.Print " Name = " & .Name 
     Debug.Print " ForeignName = " & .ForeignName 
     End With 
     
     Debug.Print "Indexes in " & tdfEmployees.Name & _ 
     " TableDef" 
     For Each idxLoop In tdfEmployees.Indexes 
     Debug.Print " " & idxLoop.Name & _ 
     ", Foreign = " & idxLoop.Foreign 
     Next idxLoop 
     
     ' Delete new objects because this is a demonstration. 
     .Relations.Delete relNew.Name 
     .TableDefs.Delete tdfNew.Name 
     tdfEmployees.Fields.Delete "DeptID" 
     .Close 
     End With 
     
    End Sub
```
