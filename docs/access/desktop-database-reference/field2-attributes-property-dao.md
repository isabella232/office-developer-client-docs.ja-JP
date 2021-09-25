---
title: Field2.Attributes プロパティ (DAO)
TOCTitle: Attributes Property
ms:assetid: 08ae9b6b-21e4-9b7e-0852-cfc6639027a7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845025(v=office.15)
ms:contentKeyID: 48543102
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052896
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 767e4cf78f8c77dc1f20a5ee24336e25d05cae46
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577396"
---
# <a name="field2attributes-property-dao"></a>Field2.Attributes プロパティ (DAO)


**適用先:** Access 2013、Office 2013


**Field2** オブジェクトの 1 つまたは複数の特性を示す値を設定または取得します。値の取得および設定が可能です。長整数型 ( **Long**) の値を使用します。

## <a name="syntax"></a>構文

*式* .Attributes

*式***Field2** オブジェクトを表す変数。

## <a name="remarks"></a>注釈

この値は、 **Field2** オブジェクトで表されるフィールドの特性を指定するもので、以下の定数の組み合わせを指定できます。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>定数</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbAutoIncrField</strong></p></td>
<td><p>新しいレコードのフィールド値は、一意の長整数型の値に自動的に増分され、変更はできません (Microsoft Access ワークスペースでは、Microsoft Office Access データベース エンジン データベース テーブルでのみサポート)。</p></td>
</tr>
<tr class="even">
<td><p><strong>dbDescending</strong></p></td>
<td><p>フィールドを降順 (Z ～ A、100 ～ 0、ん～あ) で並べ替えるオプションで、これは、<strong>Index</strong> オブジェクトの <strong>Fields</strong> コレクションの <strong>Field2</strong> オブジェクトのみに適用されます。この定数を省略すると、フィールドは昇順 (A ～ Z、0 ～ 100、あ～ん) で並べ替えられます。これは、<strong>Index</strong> フィールドおよび <strong>TableDef</strong> フィールドの既定値です (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbFixedField</strong></p></td>
<td><p>フィールド サイズは固定です (数値フィールドの既定)。</p></td>
</tr>
<tr class="even">
<td><p><strong>dbHyperlinkField</strong></p></td>
<td><p>フィールドにはハイパーリンク情報が含まれます (メモ型フィールドのみ)。</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSystemField</strong></p></td>
<td><p>レプリカのレプリケーション情報が保存される、削除できないタイプのフィールドです (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong>dbUpdatableField</strong></p></td>
<td><p>フィールド値を変更できます。</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVariableField</strong></p></td>
<td><p>フィールド サイズは可変です (テキスト フィールドのみ)。</p></td>
</tr>
</tbody>
</table>


コレクションに追加されていないオブジェクトの場合、このプロパティは値の取得および設定が可能です。追加された **Field2** オブジェクトの場合、 **Attributes** プロパティを使用できるかどうかは、 **Fields** コレクションを含むオブジェクトによって異なります。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Field オブジェクトの所属先</p></th>
<th><p>Attributes プロパティの使用</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Index</strong> オブジェクト</p></td>
<td><p><strong>Index</strong> オブジェクトが追加される <strong>TableDef</strong> オブジェクトが <strong>Database</strong> オブジェクトに追加されるまでは値の設定と取得が可能で、追加後は値の取得のみが可能です。</p></td>
</tr>
<tr class="even">
<td><p><strong>QueryDef</strong> オブジェクト</p></td>
<td><p>読み取り専用</p></td>
</tr>
<tr class="odd">
<td><p><strong>Recordset</strong> オブジェクト</p></td>
<td><p>読み取り専用</p></td>
</tr>
<tr class="even">
<td><p><strong>Relation</strong> オブジェクト</p></td>
<td><p>非サポート</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong> オブジェクト</p></td>
<td><p>読み取り/書き込み</p></td>
</tr>
</tbody>
</table>


複数の属性を設定する場合は、該当する定数をまとめて組み合わせることができます。無効な値は、エラーを発生させずに無視されます。

## <a name="example"></a>例

次の使用例は、ノースウィンド データベースの **Field2**、 **Relation**、および **TableDef** の各オブジェクトの **Attributes** プロパティを表示します。

```vb 
Sub AttributesX() 
 
 Dim dbsNorthwind As Database 
 Dim fldLoop As Field2 
 Dim relLoop As Relation 
 Dim tdfloop As TableDef 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 
 ' Display the attributes of a TableDef object's 
 ' fields. 
 Debug.Print "Attributes of fields in " & _ 
 .TableDefs(0).Name & " table:" 
 For Each fldLoop In .TableDefs(0).Fields 
 Debug.Print " " & fldLoop.Name & " = " & _ 
 fldLoop.Attributes 
 Next fldLoop 
 
 ' Display the attributes of the Northwind database's 
 ' relations. 
 Debug.Print "Attributes of relations in " & _ 
 .Name & ":" 
 For Each relLoop In .Relations 
 Debug.Print " " & relLoop.Name & " = " & _ 
 relLoop.Attributes 
 Next relLoop 
 
 ' Display the attributes of the Northwind database's 
 ' tables. 
 Debug.Print "Attributes of tables in " & .Name & ":" 
 For Each tdfloop In .TableDefs 
 Debug.Print " " & tdfloop.Name & " = " & _ 
 tdfloop.Attributes 
 Next tdfloop 
 
 .Close 
 End With 
 
End Sub 
 
```

