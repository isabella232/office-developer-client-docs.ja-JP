---
title: Database.CreateRelation メソッド (DAO)
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
ms.openlocfilehash: c7b3c69090a9879f622153f67e2aa264d18a8497
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479440"
---
# <a name="databasecreaterelation-method-dao"></a><span data-ttu-id="1c675-102">Database.CreateRelation メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="1c675-102">Database.CreateRelation Method (DAO)</span></span>

<span data-ttu-id="1c675-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="1c675-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="1c675-p101">新しい **[Relation](relation-object-dao.md)** オブジェクトを作成します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="1c675-p101">Creates a new **[Relation](relation-object-dao.md)** object (Microsoft Access workspaces only). .</span></span>

## <a name="syntax"></a><span data-ttu-id="1c675-106">構文</span><span class="sxs-lookup"><span data-stu-id="1c675-106">Syntax</span></span>

<span data-ttu-id="1c675-107">*式*です。CreateRelation (***名前***、***テーブル***、***外部テーブル\*\*\*\*\*\*の属性***)</span><span class="sxs-lookup"><span data-stu-id="1c675-107">*expression* .CreateRelation(***Name***, ***Table***, ***ForeignTable***, ***Attributes***)</span></span>

<span data-ttu-id="1c675-108">\*式\***データベース**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="1c675-108">*expression* A variable that represents a **Database** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="1c675-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1c675-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1c675-110">名前</span><span class="sxs-lookup"><span data-stu-id="1c675-110">Name</span></span></p></th>
<th><p><span data-ttu-id="1c675-111">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="1c675-111">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="1c675-112">データ型</span><span class="sxs-lookup"><span data-stu-id="1c675-112">Data Type</span></span></p></th>
<th><p><span data-ttu-id="1c675-113">説明</span><span class="sxs-lookup"><span data-stu-id="1c675-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1c675-114">名前</span><span class="sxs-lookup"><span data-stu-id="1c675-114">Name</span></span></p></td>
<td><p><span data-ttu-id="1c675-115">省略可能</span><span class="sxs-lookup"><span data-stu-id="1c675-115">Optional</span></span></p></td>
<td><p><span data-ttu-id="1c675-116"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="1c675-116"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="1c675-p102">新しい <strong>Relation</strong> オブジェクトの一意の名前を表す、サブタイプが文字列型 (<strong>String</strong>) であるバリアント型 (<strong>Variant</strong>) の値。有効な <strong>Relation</strong> 名の詳細については、<strong><a href="connection-name-property-dao.md">Name</a></strong> プロパティを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1c675-p102">A <strong>Variant</strong> (<strong>String</strong> subtype) that uniquely names the new <strong>Relation</strong> object. See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for details on valid <strong>Relation</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c675-119">テーブル</span><span class="sxs-lookup"><span data-stu-id="1c675-119">Table</span></span></p></td>
<td><p><span data-ttu-id="1c675-120">省略可能</span><span class="sxs-lookup"><span data-stu-id="1c675-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="1c675-121"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="1c675-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="1c675-p103">リレーションにおける主テーブルの名前を表す、サブタイプが文字列型 (<strong>String</strong>) であるバリアント型 (<strong>Variant</strong>) の値。<strong>Relation</strong> オブジェクトを追加する前にこのテーブルが存在していないと、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="1c675-p103">A <strong>Variant</strong> (<strong>String</strong> subtype) that names the primary table in the relation. If the table doesn't exist before you append the <strong>Relation</strong> object, a run-time error occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c675-124">外部テーブル</span><span class="sxs-lookup"><span data-stu-id="1c675-124">ForeignTable</span></span></p></td>
<td><p><span data-ttu-id="1c675-125">省略可能</span><span class="sxs-lookup"><span data-stu-id="1c675-125">Optional</span></span></p></td>
<td><p><span data-ttu-id="1c675-126"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="1c675-126"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="1c675-p104">リレーションにおける外部キー側のテーブルの名前を表す、サブタイプが文字列型 (<strong>String</strong>) であるバリアント型 (<strong>Variant</strong>) の値。<strong>Relation</strong> オブジェクトを追加する前にこのテーブルが存在していないと、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="1c675-p104">A <strong>Variant</strong> (<strong>String</strong> subtype) that names the foreign table in the relation. If the table doesn't exist before you append the <strong>Relation</strong> object, a run-time error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c675-129">属性</span><span class="sxs-lookup"><span data-stu-id="1c675-129">Attributes</span></span></p></td>
<td><p><span data-ttu-id="1c675-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="1c675-130">Optional</span></span></p></td>
<td><p><span data-ttu-id="1c675-131"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="1c675-131"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="1c675-p105">リレーションシップの種類に関する情報を格納している定数 (または定数の組み合わせ)。詳細については、<strong><a href="field-attributes-property-dao.md">Attributes</a></strong> プロパティを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1c675-p105">A constant or combination of constants that contains information about the relationship type. See the <strong><a href="field-attributes-property-dao.md">Attributes</a></strong> property for details.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="1c675-134">戻り値</span><span class="sxs-lookup"><span data-stu-id="1c675-134">Return Value</span></span>

<span data-ttu-id="1c675-135">Relation</span><span class="sxs-lookup"><span data-stu-id="1c675-135">Relation</span></span>

## <a name="remarks"></a><span data-ttu-id="1c675-136">注釈</span><span class="sxs-lookup"><span data-stu-id="1c675-136">Remarks</span></span>

<span data-ttu-id="1c675-p106">**Relation** オブジェクトは、2 つの **[TableDef](tabledef-object-dao.md)** オブジェクトまたは **[QueryDef](querydef-object-dao.md)** オブジェクト間のリレーションシップに関する情報を Microsoft Access データベース エンジンに渡します。 **Attributes** プロパティを使用して、参照整合性を実装できます。</span><span class="sxs-lookup"><span data-stu-id="1c675-p106">The **Relation** object provides information to the Microsoft Access database engine about the relationship between fields in two **[TableDef](tabledef-object-dao.md)** or **[QueryDef](querydef-object-dao.md)** objects. You can implement referential integrity by using the **Attributes** property.</span></span>

<span data-ttu-id="1c675-p107">**CreateRelation** メソッドの使用時に省略可能な引数を省略した場合は、新しいオブジェクトをコレクションに追加する前に適切な代入ステートメントを使用して、対応するプロパティを設定またはリセットできます。オブジェクトの追加後は、プロパティの設定は一切変更できません。詳細については、各プロパティのトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1c675-p107">If you omit one or more of the optional parts when you use the **CreateRelation** method, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the object, you can't alter any of its property settings. See the individual property topics for more details.</span></span>

<span data-ttu-id="1c675-142">[Relation](fields-append-method-dao.md) オブジェクトの \*\*\*\*Append\*\*\*\* メソッドを使用する前に、適切な **[Field](field-object-dao.md)** オブジェクトを追加して、主キーと外部キーのリレーションシップのテーブルを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1c675-142">Before you can use the **[Append](fields-append-method-dao.md)** method on a **Relation** object, you must append the appropriate **[Field](field-object-dao.md)** objects to define the primary and foreign key relationship tables.</span></span>

<span data-ttu-id="1c675-143">名が既にコレクションのメンバーであるオブジェクトを参照する場合、または従属**Fields**コレクションに**Field**オブジェクトの名前が無効な場合は、 **Append**メソッドを使用すると、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="1c675-143">If name refers to an object that is already a member of the collection or if the **Field** object names provided in the subordinate **Fields** collection are invalid, a run-time error occurs when you use the **Append** method.</span></span>

<span data-ttu-id="1c675-144">レプリケートされたテーブルとローカル テーブルの間にリレーションシップを設定したり、設定を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="1c675-144">You can't establish or maintain a relationship between a replicated table and a local table.</span></span>

<span data-ttu-id="1c675-145">[**Relations**](relations-collection-dao.md) コレクションから **Relation** オブジェクトを削除するには、コレクションの **[Delete](fields-delete-method-dao.md)** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="1c675-145">To remove a **Relation** object from the **[Relations](relations-collection-dao.md)** collection, use the **[Delete](fields-delete-method-dao.md)** method on the collection.</span></span>

## <a name="example"></a><span data-ttu-id="1c675-146">例</span><span class="sxs-lookup"><span data-stu-id="1c675-146">Example</span></span>

<span data-ttu-id="1c675-p108">この例では、 **CreateRelation** メソッドを使用して、Employees **TableDef** と新規作成された Departments という **TableDef** の間に **Relation** を作成します。この例では、 **Relation** を新規作成することによって、外部テーブルに必要な **Indexes** が作成されることも示します (Employees テーブルの DepartmentsEmployees Index)。</span><span class="sxs-lookup"><span data-stu-id="1c675-p108">This example uses the **CreateRelation** method to create a **Relation** between the Employees **TableDef** and a new **TableDef** called Departments. This example also demonstrates how creating a new **Relation** will also create any necessary **Indexes** in the foreign table (the DepartmentsEmployees Index in the Employees table).</span></span>

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
