---
title: データベース. createrelation DAO メソッド (DAO)
TOCTitle: CreateRelation Method
ms:assetid: e240c7e3-c293-5e19-afcc-34d9a5549c64
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835692(v=office.15)
ms:contentKeyID: 48548279
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052969
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 365835bc579a431d34b65cd27ed4de4e12bca309
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294954"
---
# <a name="databasecreaterelation-method-dao"></a><span data-ttu-id="93952-102">データベース. createrelation DAO メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="93952-102">Database.CreateRelation method (DAO)</span></span>

<span data-ttu-id="93952-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="93952-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="93952-104">新しい**[Relation](relation-object-dao.md)** オブジェクトを作成します (Microsoft access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="93952-104">Creates a new **[Relation](relation-object-dao.md)** object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="93952-105">.</span><span class="sxs-lookup"><span data-stu-id="93952-105"></span></span>

## <a name="syntax"></a><span data-ttu-id="93952-106">構文</span><span class="sxs-lookup"><span data-stu-id="93952-106">Syntax</span></span>

<span data-ttu-id="93952-107">*式*。createrelation (***Name***, ***Table***, ***ForeignTable***, ***Attributes***)</span><span class="sxs-lookup"><span data-stu-id="93952-107">*expression* .CreateRelation(***Name***, ***Table***, ***ForeignTable***, ***Attributes***)</span></span>

<span data-ttu-id="93952-108">\*式\***Database**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="93952-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="93952-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="93952-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="93952-110">名前</span><span class="sxs-lookup"><span data-stu-id="93952-110">Name</span></span></p></th>
<th><p><span data-ttu-id="93952-111">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="93952-111">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="93952-112">データ型</span><span class="sxs-lookup"><span data-stu-id="93952-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="93952-113">説明</span><span class="sxs-lookup"><span data-stu-id="93952-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93952-114"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="93952-114"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="93952-115">Optional</span><span class="sxs-lookup"><span data-stu-id="93952-115">Optional</span></span></p></td>
<td><p><span data-ttu-id="93952-116"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="93952-116"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="93952-117">新しい <strong>Relation</strong> オブジェクトの一意の名前を表す、サブタイプが文字列型 (<strong>String</strong>) であるバリアント型 (<strong>Variant</strong>) の値。</span><span class="sxs-lookup"><span data-stu-id="93952-117">A <strong>Variant</strong> (<strong>String</strong> subtype) that uniquely names the new <strong>Relation</strong> object.</span></span> <span data-ttu-id="93952-118">有効な<strong>リレーション</strong>名の詳細については、 <strong><a href="connection-name-property-dao.md">Name</a></strong>プロパティを参照してください。</span><span class="sxs-lookup"><span data-stu-id="93952-118">See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for details on valid <strong>Relation</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93952-119"><em>Table</em></span><span class="sxs-lookup"><span data-stu-id="93952-119"><em>Table</em></span></span></p></td>
<td><p><span data-ttu-id="93952-120">Optional</span><span class="sxs-lookup"><span data-stu-id="93952-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="93952-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="93952-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="93952-122">リレーションにおける主テーブルの名前を表す、サブタイプが文字列型 (<strong>String</strong>) であるバリアント型 (<strong>Variant</strong>) の値。</span><span class="sxs-lookup"><span data-stu-id="93952-122">A <strong>Variant</strong> (<strong>String</strong> subtype) that names the primary table in the relation.</span></span> <span data-ttu-id="93952-123"><strong>Relation</strong> オブジェクトを追加する前にこのテーブルが存在していないと、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="93952-123">If the table doesn't exist before you append the <strong>Relation</strong> object, a run-time error occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93952-124"><em>ForeignTable</em></span><span class="sxs-lookup"><span data-stu-id="93952-124"><em>ForeignTable</em></span></span></p></td>
<td><p><span data-ttu-id="93952-125">Optional</span><span class="sxs-lookup"><span data-stu-id="93952-125">Optional</span></span></p></td>
<td><p><span data-ttu-id="93952-126"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="93952-126"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="93952-127">リレーションにおける外部キー側のテーブルの名前を表す、サブタイプが文字列型 (<strong>String</strong>) であるバリアント型 (<strong>Variant</strong>) の値。</span><span class="sxs-lookup"><span data-stu-id="93952-127">A <strong>Variant</strong> (<strong>String</strong> subtype) that names the foreign table in the relation.</span></span> <span data-ttu-id="93952-128"><strong>Relation</strong> オブジェクトを追加する前にこのテーブルが存在していないと、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="93952-128">If the table doesn't exist before you append the <strong>Relation</strong> object, a run-time error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93952-129"><em>Attributes</em></span><span class="sxs-lookup"><span data-stu-id="93952-129"><em>Attributes</em></span></span></p></td>
<td><p><span data-ttu-id="93952-130">Optional</span><span class="sxs-lookup"><span data-stu-id="93952-130">Optional</span></span></p></td>
<td><p><span data-ttu-id="93952-131"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="93952-131"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="93952-132">リレーションシップの種類に関する情報を格納している定数 (または定数の組み合わせ)。</span><span class="sxs-lookup"><span data-stu-id="93952-132">A constant or combination of constants that contains information about the relationship type.</span></span> <span data-ttu-id="93952-133">詳細については、 <strong><a href="field-attributes-property-dao.md">Attributes</a></strong>プロパティを参照してください。</span><span class="sxs-lookup"><span data-stu-id="93952-133">See the <strong><a href="field-attributes-property-dao.md">Attributes</a></strong> property for details.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="93952-134">戻り値</span><span class="sxs-lookup"><span data-stu-id="93952-134">Return value</span></span>

<span data-ttu-id="93952-135">Relation</span><span class="sxs-lookup"><span data-stu-id="93952-135">Relation</span></span>

## <a name="remarks"></a><span data-ttu-id="93952-136">注釈</span><span class="sxs-lookup"><span data-stu-id="93952-136">Remarks</span></span>

<span data-ttu-id="93952-p106">**Relation** オブジェクトは、2 つの **[TableDef](tabledef-object-dao.md)** オブジェクトまたは **[QueryDef](querydef-object-dao.md)** オブジェクト間のリレーションシップに関する情報を Microsoft Access データベース エンジンに渡します。 **Attributes** プロパティを使用して、参照整合性を実装できます。</span><span class="sxs-lookup"><span data-stu-id="93952-p106">The **Relation** object provides information to the Microsoft Access database engine about the relationship between fields in two **[TableDef](tabledef-object-dao.md)** or **[QueryDef](querydef-object-dao.md)** objects. You can implement referential integrity by using the **Attributes** property.</span></span>

<span data-ttu-id="93952-p107">**CreateRelation** メソッドの使用時に省略可能な引数を省略した場合は、新しいオブジェクトをコレクションに追加する前に適切な代入ステートメントを使用して、対応するプロパティを設定またはリセットできます。オブジェクトの追加後は、プロパティの設定は一切変更できません。詳細については、各プロパティのトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="93952-p107">If you omit one or more of the optional parts when you use the **CreateRelation** method, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the object, you can't alter any of its property settings. See the individual property topics for more details.</span></span>

<span data-ttu-id="93952-142">**Relation**オブジェクトで**[Append](fields-append-method-dao.md)** メソッドを使用するには、その前に、適切な**[Field](field-object-dao.md)** オブジェクトを追加して、主キーと外部キーのリレーションシップテーブルを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93952-142">Before you can use the **[Append](fields-append-method-dao.md)** method on a **Relation** object, you must append the appropriate **[Field](field-object-dao.md)** objects to define the primary and foreign key relationship tables.</span></span>

<span data-ttu-id="93952-143">name が既にコレクションのメンバーであるオブジェクトを参照している場合、または下位の**Fields**コレクションで指定された**Field**オブジェクトの名前が無効な場合は、 **Append**メソッドを使用すると、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="93952-143">If name refers to an object that is already a member of the collection or if the **Field** object names provided in the subordinate **Fields** collection are invalid, a run-time error occurs when you use the **Append** method.</span></span>

<span data-ttu-id="93952-144">レプリケートされたテーブルとローカル テーブルの間にリレーションシップを設定したり、設定を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="93952-144">You can't establish or maintain a relationship between a replicated table and a local table.</span></span>

<span data-ttu-id="93952-145">[**Relations**](relations-collection-dao.md) コレクションから **Relation** オブジェクトを削除するには、コレクションの **[Delete](fields-delete-method-dao.md)** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="93952-145">To remove a **Relation** object from the **[Relations](relations-collection-dao.md)** collection, use the **[Delete](fields-delete-method-dao.md)** method on the collection.</span></span>

## <a name="example"></a><span data-ttu-id="93952-146">例</span><span class="sxs-lookup"><span data-stu-id="93952-146">Example</span></span>

<span data-ttu-id="93952-p108">次の使用例は、 **CreateRelation** メソッドを使用して、Employees テーブルの **TableDef** オブジェクトと Departments と呼ばれる新しい **TableDef** オブジェクトの間に **Relation** オブジェクトを作成します。また、新しい **Relation** オブジェクトを作成すると、必要な **Indexes** オブジェクト (社員テーブルの DepartmentsEmployees インデックス) が外部キー側のテーブルに作成されることも示します。</span><span class="sxs-lookup"><span data-stu-id="93952-p108">This example uses the **CreateRelation** method to create a **Relation** between the Employees **TableDef** and a new **TableDef** called Departments. This example also demonstrates how creating a new **Relation** will also create any necessary **Indexes** in the foreign table (the DepartmentsEmployees Index in the Employees table).</span></span>

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
