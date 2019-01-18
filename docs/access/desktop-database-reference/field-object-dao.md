---
title: Field オブジェクトのデータ アクセス オブジェクトの (DAO)
TOCTitle: Field Object
ms:assetid: 47282ce2-9b49-ccf9-ad37-c4bb25cfd037
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193203(v=office.15)
ms:contentKeyID: 48544587
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: c58896fb0d0a5c5a28844fdd3a6df922dd587f32
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703644"
---
# <a name="field-object-dao"></a><span data-ttu-id="0068c-102">フィールド オブジェクト (DAO)</span><span class="sxs-lookup"><span data-stu-id="0068c-102">Field object (DAO)</span></span>

<span data-ttu-id="0068c-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="0068c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0068c-104">**Field** オブジェクトは、共通のデータ型およびプロパティの共通セットを持つ、データの列を表します。</span><span class="sxs-lookup"><span data-stu-id="0068c-104">A **Field** object represents a column of data with a common data type and a common set of properties.</span></span>

## <a name="remarks"></a><span data-ttu-id="0068c-105">解説</span><span class="sxs-lookup"><span data-stu-id="0068c-105">Remarks</span></span>

<span data-ttu-id="0068c-p101">**Index** 、 **QueryDef** 、 **Relation** 、および **TableDef** の各オブジェクトの **Fields** コレクションには、そのオブジェクトが表すフィールドの定義が含まれます。 **Recordset** オブジェクトの **Fields** コレクションは、データの行、またはレコードの **Field** オブジェクトを表します。 **Recordset** オブジェクトのカレント レコードのフィールドの値を取得および設定するには、 **Recordset** オブジェクトの **Field** オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="0068c-p101">The **Fields** collections of **Index**, **QueryDef**, **Relation**, and **TableDef** objects contain the specifications for the fields those objects represent. The **Fields** collection of a **Recordset** object represents the **Field** objects in a row of data, or in a record. You use the **Field** objects in a **Recordset** object to read and set values for the fields in the current record of the **Recordset** object.</span></span>

<span data-ttu-id="0068c-p102">Microsoft Access ワークスペースで、 **Field** オブジェクトとそのメソッドおよびプロパティを使用して、フィールドを操作できます。たとえば、以下の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="0068c-p102">In a Microsoft Access workspacee, you manipulate a field using a **Field** object and its methods and properties. For example, you can:</span></span>

  - <span data-ttu-id="0068c-111">**OrdinalPosition** プロパティを使用して、 **Fields** コレクションの **Field** オブジェクトの表示順序を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="0068c-111">Use the **OrdinalPosition** property to set or return the presentation order of the **Field** object in a **Fields** collection.</span></span>

  - <span data-ttu-id="0068c-112">**Recordset** オブジェクトのフィールドの **Value** プロパティを使用して、保存されているデータを設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="0068c-112">Use the **Value** property of a field in a **Recordset** object to set or return stored data.</span></span>

  - <span data-ttu-id="0068c-113">**AppendChunk** メソッドおよび **GetChunk** メソッドと **FieldSize** プロパティを使用して、 **Recordset** オブジェクトの OLE オブジェクトまたはメモ型フィールドの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0068c-113">Use the **AppendChunk** and **GetChunk** methods and the **FieldSize** property to get or set a value in an OLE Object or Memo field of a **Recordset** object.</span></span>

  - <span data-ttu-id="0068c-114">**Type** 、 **Size** 、および **Attributes** の各プロパティを使用して、フィールドに保存できるデータの種類を特定します。</span><span class="sxs-lookup"><span data-stu-id="0068c-114">Use the **Type**, **Size**, and **Attributes** properties to determine the type of data that can be stored in the field.</span></span>

  - <span data-ttu-id="0068c-115">**SourceField** プロパティおよび **SourceTable** プロパティを使用して、データの元のソースを特定します。</span><span class="sxs-lookup"><span data-stu-id="0068c-115">Use the **SourceField** and **SourceTable** properties to determine the original source of the data.</span></span>

  - <span data-ttu-id="0068c-116">**ForeignName** プロパティを使用して、 **Relation** オブジェクトの外部フィールドに関する情報を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="0068c-116">Use the **ForeignName** property to set or return information about a foreign field in a **Relation** object.</span></span>

  - <span data-ttu-id="0068c-117">**AllowZeroLength** 、 **DefaultValue** 、 **Required** 、 **ValidateOnSet** 、 **ValidationRule** 、 **ValidationText** のいずれかのプロパティを使用して、入力検査の条件を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="0068c-117">Use the **AllowZeroLength**, **DefaultValue**, **Required**, **ValidateOnSet**, **ValidationRule**, or **ValidationText** properties to set or return validation conditions.</span></span>

  - <span data-ttu-id="0068c-118">**TableDef** オブジェクトのフィールドの **DefaultValue** プロパティを使用して、新しいレコードが追加されたときのこのフィールドの既定値を設定します。</span><span class="sxs-lookup"><span data-stu-id="0068c-118">Use the **DefaultValue** property of a field on a **TableDef** object to set the default value for this field when new records are added.</span></span>

<span data-ttu-id="0068c-119">**Index** 、 **TableDef** 、または **Relation** のいずれかのオブジェクト内に新しい **Field** オブジェクトを作成するには、 **CreateField** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="0068c-119">To create a new **Field** object in an **Index**, **TableDef**, or **Relation** object, use the **CreateField** method.</span></span>

<span data-ttu-id="0068c-p103">**Recordset** オブジェクトの一部である **Field** オブジェクトにアクセスすると、現在のレコードのデータが **Field** オブジェクトの **Value** プロパティに表示されます。 **Recordset** オブジェクトのデータを操作するには、通常は **Fields** コレクションを直接参照するのではなく、 **Recordset** オブジェクトの **Fields** コレクションに含まれる **Field** オブジェクトの **Value** プロパティを間接的に参照します。</span><span class="sxs-lookup"><span data-stu-id="0068c-p103">When you access a **Field** object as part of a **Recordset** object, data from the current record is visible in the **Field** object's **Value** property. To manipulate data in the **Recordset** object, you don't usually reference the **Fields** collection directly; instead, you indirectly reference the **Value** property of the **Field** object in the **Fields** collection of the **Recordset** object.</span></span>

<span data-ttu-id="0068c-122">コレクション内の **Field** オブジェクトを、コレクションで付けられたインデックスまたは **Name** プロパティの設定値で参照するには、次のいずれかの構文を使います。</span><span class="sxs-lookup"><span data-stu-id="0068c-122">To refer to a **Field** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="0068c-123">**Fields**(0)</span><span class="sxs-lookup"><span data-stu-id="0068c-123">**Fields**(0)</span></span>

- <span data-ttu-id="0068c-124">**フィールド**("name")</span><span class="sxs-lookup"><span data-stu-id="0068c-124">**Fields**("name")</span></span>

- <span data-ttu-id="0068c-125">**フィールド**\!\[名\]</span><span class="sxs-lookup"><span data-stu-id="0068c-125">**Fields**\!\[name\]</span></span>

<span data-ttu-id="0068c-p104">同じ構文を使用して、作成して **Fields** コレクションに追加する **Field** オブジェクトの **Value** プロパティを参照することもできます。フィールド参照のコンテキストにより、 **Field** オブジェクトと **Field** オブジェクトの **Value** プロパティのいずれを参照するかが決まります。</span><span class="sxs-lookup"><span data-stu-id="0068c-p104">With the same syntax forms, you can also refer to the **Value** property of a **Field** object that you create and append to a **Fields** collection. The context of the field reference will determine whether you are referring to the **Field** object or the **Value** property of the **Field** object.</span></span>

## <a name="example"></a><span data-ttu-id="0068c-128">例</span><span class="sxs-lookup"><span data-stu-id="0068c-128">Example</span></span>

<span data-ttu-id="0068c-p105">この例では、 **Field** オブジェクトの場所 ( **TableDef** の **Fields** コレクション、 **QueryDef** の **Fields** コレクションなど) に応じた、 **Field** オブジェクトに対して有効なプロパティを示します。このプロシージャを実行するには、FieldOutput プロシージャが必要です。</span><span class="sxs-lookup"><span data-stu-id="0068c-p105">This example shows what properties are valid for a **Field** object depending on where the **Field** resides (for example, the **Fields** collection of a **TableDef**, the **Fields** collection of a **QueryDef**, and so forth). The FieldOutput procedure is required for this procedure to run.</span></span>

```vb
    Sub FieldX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim fldTableDef As Field 
     Dim fldQueryDef As Field 
     Dim fldRecordset As Field 
     Dim fldRelation As Field 
     Dim fldIndex As Field 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     ' Assign a Field object from different Fields 
     ' collections to object variables. 
     Set fldTableDef = _ 
     dbsNorthwind.TableDefs(0).Fields(0) 
     Set fldQueryDef =dbsNorthwind.QueryDefs(0).Fields(0) 
     Set fldRecordset = rstEmployees.Fields(0) 
     Set fldRelation =dbsNorthwind.Relations(0).Fields(0) 
     Set fldIndex = _ 
     dbsNorthwind.TableDefs(0).Indexes(0).Fields(0) 
     
     ' Print report. 
     FieldOutput "TableDef", fldTableDef 
     FieldOutput "QueryDef", fldQueryDef 
     FieldOutput "Recordset", fldRecordset 
     FieldOutput "Relation", fldRelation 
     FieldOutput "Index", fldIndex 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub FieldOutput(strTemp As String, fldTemp As Field) 
     ' Report function for FieldX. 
     
     Dim prpLoop As Property 
     
     Debug.Print "Valid Field properties in " & strTemp 
     
     ' Enumerate Properties collection of passed Field 
     ' object. 
     For Each prpLoop In fldTemp.Properties 
     ' Some properties are invalid in certain 
     ' contexts (the Value property in the Fields 
     ' collection of a TableDef for example). Any 
     ' attempt to use an invalid property will 
     ' trigger an error. 
     On Error Resume Next 
     Debug.Print " " & prpLoop.Name & " = " & _ 
     prpLoop.Value 
     On Error GoTo 0 
     Next prpLoop 
     
    End Sub 
```

<br/>

<span data-ttu-id="0068c-p106">この例では、 **CreateField** メソッドを使用して、新しい **TableDef** に 3 つの **Fields** オブジェクトを作成します。次に、 **CreateField** メソッドによって自動的に設定される、これらの **Field** オブジェクトのプロパティを表示します ( **Field** オブジェクトの作成時に値が空のプロパティは表示されません)。</span><span class="sxs-lookup"><span data-stu-id="0068c-p106">This example uses the **CreateField** method to create three **Fields** for a new **TableDef**. It then displays the properties of those **Field** objects that are automatically set by the **CreateField** method. (Properties whose values are empty at the time of **Field** creation are not shown.)</span></span>

```vb
    Sub CreateFieldX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfNew As TableDef 
     Dim fldLoop As Field 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     Set tdfNew = dbsNorthwind.CreateTableDef("NewTableDef") 
     
     ' Create and append new Field objects for the new 
     ' TableDef object. 
     With tdfNew 
     ' The CreateField method will set a default Size 
     ' for a new Field object if one is not specified. 
     .Fields.Append .CreateField("TextField", dbText) 
     .Fields.Append .CreateField("IntegerField", dbInteger) 
     .Fields.Append .CreateField("DateField", dbDate) 
     End With 
     
     dbsNorthwind.TableDefs.Append tdfNew 
     
     Debug.Print "Properties of new Fields in " & tdfNew.Name 
     
     ' Enumerate Fields collection to show the properties of 
     ' the new Field objects. 
     For Each fldLoop In tdfNew.Fields 
     Debug.Print " " & fldLoop.Name 
     
     For Each prpLoop In fldLoop.Properties 
     ' Properties that are invalid in the context of 
     ' TableDefs will trigger an error if an attempt 
     ' is made to read their values. 
     On Error Resume Next 
     Debug.Print " " & prpLoop.Name & " - " & _ 
     IIf(prpLoop = "", "[empty]", prpLoop) 
     On Error GoTo 0 
     Next prpLoop 
     
     Next fldLoop 
     
     ' Delete new TableDef because this is a demonstration. 
     dbsNorthwind.TableDefs.Delete tdfNew.Name 
     dbsNorthwind.Close 
     
    End Sub
```
