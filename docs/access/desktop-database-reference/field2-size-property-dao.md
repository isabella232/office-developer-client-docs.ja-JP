---
title: Field2.Size プロパティ (DAO)
TOCTitle: Size Property
ms:assetid: e252759a-cea9-25cb-667d-80b422fbf97e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835700(v=office.15)
ms:contentKeyID: 48548282
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 90278f60242b24e9cc46f86478c2c678e8005cb0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602647"
---
# <a name="field2size-property-dao"></a>Field2.Size プロパティ (DAO)


**適用先**: Access 2013、Office 2013


**Field2** オブジェクトの最大サイズをバイト数で示す値を設定または取得します。

## <a name="syntax"></a>構文

*式* .サイズ

*式***Field2** オブジェクトを表す変数。

## <a name="remarks"></a>注釈

**[Fields](fields-collection-dao.md)** コレクションに追加されていないオブジェクトの場合、このプロパティは値の取得および設定が可能です。

文字データを含むフィールド (メモ型 (Memo) フィールドを除く) では、 **Size** プロパティは、そのフィールドが保持できる最大文字数を示します。数値フィールドでは、 **Size** プロパティは保存に必要なバイト数を示します。

**Size** プロパティを使用できるかどうかは、次の表に示すように、 **Field2** オブジェクトが追加される **Fields** コレクションを含むオブジェクトによって決まります。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>オブジェクトの追加先</p></th>
<th><p>使用法</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Index</strong></p></td>
<td><p>サポートされません。</p></td>
</tr>
<tr class="even">
<td><p><strong>QueryDef</strong></p></td>
<td><p>値の取得のみ可能です。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Recordset</strong></p></td>
<td><p>値の取得のみ可能です。</p></td>
</tr>
<tr class="even">
<td><p><strong>Relation</strong></p></td>
<td><p>サポートされません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong></p></td>
<td><p>値の取得のみ可能です。</p></td>
</tr>
</tbody>
</table>


テキスト型 (Text) 以外のデータ型の **Field2** オブジェクトを作成した場合、 **Type** プロパティの設定値により **Size** プロパティの設定値が自動的に決まるため、設定する必要はありません。ただし、テキスト型 (Text) の **Field2** オブジェクトでは、 **Size** プロパティを最大テキスト サイズ (Microsoft Access データベース エンジン データベースの場合 255) までの任意の整数に設定できます。サイズを設定していない場合、フィールドはデータベースで許可されるサイズになります。

ロング バイナリ型 (Long Binary) とメモ型 (Memo) の **Field2** オブジェクトでは、 **Size** は常に 0 に設定されます。特定のレコードのデータのサイズを識別するには、 **Field2** オブジェクトの **FieldSize** プロパティを使用します。ロング バイナリ型 (Long Binary) またはメモ型 (Memo) のフィールドの最大サイズを制限するのは、システム リソースまたはデータベースが許可する最大サイズのみです。

## <a name="example"></a>例

次の使用例は、Employees テーブルの **Field2** オブジェクトの名前とサイズを列挙することで、 **Size** プロパティの機能を示します。

```vb
    Sub SizeX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim fldNew As Field2 
     Dim fldLoop As Field2 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs!Employees 
     
     With tdfEmployees 
     
     ' Create and append a new Field object to the 
     ' Employees table. 
     Set fldNew = .CreateField("FaxPhone") 
     fldNew.Type = dbText 
     fldNew.Size = 20 
     .Fields.Append fldNew 
     
     Debug.Print "TableDef: " & .Name 
     Debug.Print " Field.Name - Field.Type - Field.Size" 
     
     ' Enumerate Fields collection; print field names, 
     ' types, and sizes. 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name & " - " & _ 
     fldLoop.Type & " - " & fldLoop.Size 
     Next fldLoop 
     
     ' Delete new field because this is a demonstration. 
     .Fields.Delete fldNew.Name 
     
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
