---
title: Relation オブジェクト (DAO)
TOCTitle: Relation Object
ms:assetid: 46d6dfaf-a97d-3abd-0b4b-396a41eb3be7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193195(v=office.15)
ms:contentKeyID: 48544578
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3eeaf8bf46d8673731243a1161ac578062a01f89
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307044"
---
# <a name="relation-object-dao"></a>Relation オブジェクト (DAO)


**適用先:** Access 2013、Office 2013

**Relation** オブジェクトは、テーブルまたはクエリのフィールド間のリレーションシップを表します (Microsoft Access データベース エンジン データベースのみ)。

## <a name="remarks"></a>注釈

**Relation** オブジェクトを使用して、新しいリレーションシップを作成し、データベースの既存のリレーションシップを調べることができます。

**Relation** オブジェクトとそのプロパティを使用して、以下の操作を実行できます。

  - ベース テーブルのフィールド間に、参照性合成が適用されたリレーションシップを指定します (クエリまたはリンク テーブル関連のリレーションシップは除く)。

  - あらゆる種類のテーブルまたはクエリ (ネイティブまたはリンク) 間に参照整合性が適用されていないリレーションシップを設定します。

  - **Name** プロパティを使用して、参照先の主テーブルと参照元の外部キー側のテーブルのフィールド間のリレーションシップを参照します。

  - **Attributes** プロパティを使用して、テーブルのフィールド間のリレーションシップが一対一か一対多のいずれかを指定し、参照整合性を適用する方法を指定します。

  - **Attributes** プロパティを使用して、Microsoft Access データベース エンジンが主テーブルと外部キー側のテーブルで連鎖更新操作および連鎖削除操作を実行できるかどうかを指定します。

  - **Attributes** プロパティを使用して、テーブルのフィールド間のリレーションシップが左外部結合か、右外部結合かを指定します。

  - **Relation** オブジェクトの **Fields** コレクションにあるすべての **Field** オブジェクトの **Name** プロパティを使用して、参照先テーブルの主キーのフィールド名を設定または取得するか、 **Field** オブジェクトの **ForeignName** プロパティの設定値を使用して、参照元テーブルの外部キーのフィールド名を設定または取得します。

データベースに設定されたリレーションシップに違反する変更を行うと、トラップ可能なエラーが発生します。連鎖更新または連鎖削除操作を要求すると、Microsoft Access データベース エンジンでは、設定したリレーションシップを適用するために、主キー テーブルまたは外部キー テーブルも変更されます。

たとえば、Northwind データベースに、[受注] テーブルと [顧客] テーブルの間のリレーションシップがあるとします。[顧客] テーブルの CustomerID フィールドが主キーで、[受注] テーブルの CustomerID フィールドが外部キーです。Microsoft Access データベース エンジンが [受注] テーブルの新しいレコードを受け取るには、[顧客] テーブルに [受注] テーブルの CustomerID フィールドと一致するフィールドがあるかどうかを検索します。一致するフィールドが見つからなかった場合、Microsoft Access データベース エンジンは新しいレコードを受け取らず、トラップ可能なエラーが発生します。

参照整合性を適用する場合、参照先テーブルのキー フィールドに一意のインデックスが既に存在している必要があります。Microsoft Access データベース エンジンでは、 **Foreign** プロパティが参照元テーブルの外部キーとして機能するように設定されたインデックスが自動的に作成されます。

新しい **Relation** オブジェクトを作成するには、 **CreateRelation** メソッドを使用します。コレクション内の **Relation** オブジェクトを、コレクションで付けられたインデックスまたは **Name** プロパティの設定値で参照するには、次のいずれかの構文を使います。

**Relations**(0)

**関係**("name")

****\!リレーション\[名\]

## <a name="example"></a>例

次の使用例は、既存の **Relation** オブジェクトによりデータ入力を制御する方法を示しています。故意に正しくない CategoryID を持つレコードを追加しようとすることで、エラー処理ルーチンを起動します。

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

次の使用例は、 **CreateRelation** メソッドを使用して、Employees テーブルの **TableDef** オブジェクトと Departments と呼ばれる新しい **TableDef** オブジェクトの間に **Relation** オブジェクトを作成します。 また、新しい**リレーション**を作成することで、必要な**インデックス**が外部テーブル (Employees テーブルの DepartmentsEmployees インデックス) に作成されることも示します。

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
