---
title: Field オブジェクト - データ アクセス オブジェクト (DAO)
TOCTitle: Field Object
ms:assetid: 47282ce2-9b49-ccf9-ad37-c4bb25cfd037
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193203(v=office.15)
ms:contentKeyID: 48544587
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: c58896fb0d0a5c5a28844fdd3a6df922dd587f32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293043"
---
# <a name="field-object-dao"></a>Field オブジェクト (DAO)

**適用先**: Access 2013、Office 2013

**Field** オブジェクトは、共通のデータ型およびプロパティの共通セットを持つ、データの列を表します。

## <a name="remarks"></a>注釈

**Index** 、 **QueryDef** 、 **Relation** 、および **TableDef** の各オブジェクトの **Fields** コレクションには、そのオブジェクトが表すフィールドの定義が含まれます。 **Recordset** オブジェクトの **Fields** コレクションは、データの行、またはレコードの **Field** オブジェクトを表します。 **Recordset** オブジェクトのカレント レコードのフィールドの値を取得および設定するには、 **Recordset** オブジェクトの **Field** オブジェクトを使用します。

Microsoft Access ワークスペースで、 **Field** オブジェクトとそのメソッドおよびプロパティを使用して、フィールドを操作できます。たとえば、以下の操作を実行できます。

  - **OrdinalPosition** プロパティを使用して、 **Fields** コレクションの **Field** オブジェクトの表示順序を設定または取得します。

  - **Recordset** オブジェクトのフィールドの **Value** プロパティを使用して、保存されているデータを設定または取得します。

  - **AppendChunk** メソッドおよび **GetChunk** メソッドと **FieldSize** プロパティを使用して、 **Recordset** オブジェクトの OLE オブジェクトまたはメモ型フィールドの値を取得または設定します。

  - **Type** 、 **Size** 、および **Attributes** の各プロパティを使用して、フィールドに保存できるデータの種類を特定します。

  - **SourceField** プロパティおよび **SourceTable** プロパティを使用して、データの元のソースを特定します。

  - **ForeignName** プロパティを使用して、 **Relation** オブジェクトの外部フィールドに関する情報を設定または取得します。

  - **AllowZeroLength** 、 **DefaultValue** 、 **Required** 、 **ValidateOnSet** 、 **ValidationRule** 、 **ValidationText** のいずれかのプロパティを使用して、入力検査の条件を設定または取得します。

  - **TableDef** オブジェクトのフィールドの **DefaultValue** プロパティを使用して、新しいレコードが追加されたときのこのフィールドの既定値を設定します。

**Index** 、 **TableDef** 、または **Relation** のいずれかのオブジェクト内に新しい **Field** オブジェクトを作成するには、 **CreateField** メソッドを使用します。

**Recordset** オブジェクトの一部である **Field** オブジェクトにアクセスすると、現在のレコードのデータが **Field** オブジェクトの **Value** プロパティに表示されます。 **Recordset** オブジェクトのデータを操作するには、通常は **Fields** コレクションを直接参照するのではなく、 **Recordset** オブジェクトの **Fields** コレクションに含まれる **Field** オブジェクトの **Value** プロパティを間接的に参照します。

コレクション内の **Field** オブジェクトを、コレクションで付けられたインデックスまたは **Name** プロパティの設定値で参照するには、次のいずれかの構文を使います。

- **Fields**(0)

- **Fields**(「名前」)

- **Fields**\!\[名前\]

同じ構文を使用して、作成して **Fields** コレクションに追加する **Field** オブジェクトの **Value** プロパティを参照することもできます。フィールド参照のコンテキストにより、**Field** オブジェクトと **Field** オブジェクトの **Value** プロパティのいずれを参照するかが決まります。

## <a name="example"></a>例

この例では、**Field** オブジェクトの場所 (**TableDef** の **Fields** コレクション、**QueryDef** の **Fields** コレクションなど) に応じた、**Field** オブジェクトに対して有効なプロパティを示します。このプロシージャを実行するには、FieldOutput プロシージャが必要です。

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

この例では、**CreateField** メソッドを使用して、新しい **TableDef** に 3 つの **Fields** オブジェクトを作成します。次に、**CreateField** メソッドによって自動的に設定される、これらの **Field** オブジェクトのプロパティを表示します (**Field** オブジェクトの作成時に値が空のプロパティは表示されません)。

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
