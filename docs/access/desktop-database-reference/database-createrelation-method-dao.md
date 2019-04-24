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
# <a name="databasecreaterelation-method-dao"></a>データベース. createrelation DAO メソッド (DAO)

**適用先:** Access 2013、Office 2013

新しい**[Relation](relation-object-dao.md)** オブジェクトを作成します (Microsoft access ワークスペースのみ)。 .

## <a name="syntax"></a>構文

*式*。createrelation (***Name***, ***Table***, ***ForeignTable***, ***Attributes***)

*式***Database**オブジェクトを表す変数を取得します。

## <a name="parameters"></a>パラメーター

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>名前</p></th>
<th><p>必須/オプション</p></th>
<th><p>データ型</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>新しい <strong>Relation</strong> オブジェクトの一意の名前を表す、サブタイプが文字列型 (<strong>String</strong>) であるバリアント型 (<strong>Variant</strong>) の値。 有効な<strong>リレーション</strong>名の詳細については、 <strong><a href="connection-name-property-dao.md">Name</a></strong>プロパティを参照してください。</p></td>
</tr>
<tr class="even">
<td><p><em>Table</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>リレーションにおける主テーブルの名前を表す、サブタイプが文字列型 (<strong>String</strong>) であるバリアント型 (<strong>Variant</strong>) の値。 <strong>Relation</strong> オブジェクトを追加する前にこのテーブルが存在していないと、実行時エラーが発生します。</p></td>
</tr>
<tr class="odd">
<td><p><em>ForeignTable</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>リレーションにおける外部キー側のテーブルの名前を表す、サブタイプが文字列型 (<strong>String</strong>) であるバリアント型 (<strong>Variant</strong>) の値。 <strong>Relation</strong> オブジェクトを追加する前にこのテーブルが存在していないと、実行時エラーが発生します。</p></td>
</tr>
<tr class="even">
<td><p><em>Attributes</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>リレーションシップの種類に関する情報を格納している定数 (または定数の組み合わせ)。 詳細については、 <strong><a href="field-attributes-property-dao.md">Attributes</a></strong>プロパティを参照してください。</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>戻り値

Relation

## <a name="remarks"></a>注釈

**Relation** オブジェクトは、2 つの **[TableDef](tabledef-object-dao.md)** オブジェクトまたは **[QueryDef](querydef-object-dao.md)** オブジェクト間のリレーションシップに関する情報を Microsoft Access データベース エンジンに渡します。 **Attributes** プロパティを使用して、参照整合性を実装できます。

**CreateRelation** メソッドの使用時に省略可能な引数を省略した場合は、新しいオブジェクトをコレクションに追加する前に適切な代入ステートメントを使用して、対応するプロパティを設定またはリセットできます。オブジェクトの追加後は、プロパティの設定は一切変更できません。詳細については、各プロパティのトピックを参照してください。

**Relation**オブジェクトで**[Append](fields-append-method-dao.md)** メソッドを使用するには、その前に、適切な**[Field](field-object-dao.md)** オブジェクトを追加して、主キーと外部キーのリレーションシップテーブルを定義する必要があります。

name が既にコレクションのメンバーであるオブジェクトを参照している場合、または下位の**Fields**コレクションで指定された**Field**オブジェクトの名前が無効な場合は、 **Append**メソッドを使用すると、実行時エラーが発生します。

レプリケートされたテーブルとローカル テーブルの間にリレーションシップを設定したり、設定を変更することはできません。

[**Relations**](relations-collection-dao.md) コレクションから **Relation** オブジェクトを削除するには、コレクションの **[Delete](fields-delete-method-dao.md)** メソッドを使用します。

## <a name="example"></a>例

次の使用例は、 **CreateRelation** メソッドを使用して、Employees テーブルの **TableDef** オブジェクトと Departments と呼ばれる新しい **TableDef** オブジェクトの間に **Relation** オブジェクトを作成します。また、新しい **Relation** オブジェクトを作成すると、必要な **Indexes** オブジェクト (社員テーブルの DepartmentsEmployees インデックス) が外部キー側のテーブルに作成されることも示します。

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
