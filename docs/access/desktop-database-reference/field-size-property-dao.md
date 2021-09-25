---
title: Field.Size プロパティ (DAO)
TOCTitle: Size Property
ms:assetid: 15e25201-87b6-f62f-ff18-259414a47891
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845510(v=office.15)
ms:contentKeyID: 48543419
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052878
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: d0651e41cb03e5b689093cea5e33ba95d9d8684a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597318"
---
# <a name="fieldsize-property-dao"></a>Field.Size プロパティ (DAO)


**適用先**: Access 2013、Office 2013


**[Field](field-object-dao.md)** オブジェクトの最大サイズをバイト数で示す値を設定または取得します。

## <a name="syntax"></a>構文

*式* .サイズ

*expression*: **Field** オブジェクトを表す変数。

## <a name="remarks"></a>注釈

**[Fields](fields-collection-dao.md)** コレクションに追加されていないオブジェクトの場合、このプロパティは値の取得および設定が可能です。

文字データを含むフィールド (メモ型フィールドを除く) の場合、 **Size** プロパティは、フィールドが保持できる最大文字数を示します。数値フィールドの場合、 **Size** プロパティは、格納に必要なバイト数を示します。

**Size** プロパティを使用するかどうかは、次の表に示すように、 **Field** オブジェクトの追加先の **Fields** コレクションを含むオブジェクトによって異なります。

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


テキスト型 (Text) 以外のデータ型で **Field** オブジェクトを作成する場合、 **[Type](field-type-property-dao.md)** プロパティの設定によって **Size** プロパティの設定が自動的に決まり、ユーザーが設定する必要はありません。ただし、テキスト型 (Text) のデータ型を持つ **Field** オブジェクトの場合、 **Size** を最大テキスト サイズ以内の任意の整数 (Microsoft Access データベースでは 255) に設定できます。サイズを指定しない場合、フィールドはデータベースで許容される最大サイズになります。

ロング バイナリ型 (Long Binary) とメモ型 (Memo) の **Field** オブジェクトの場合、**Size** は常に 0 に設定されます。 特定の **[レコード内の](field-fieldsize-property-dao.md)** データのサイズを決定するには **、Field** オブジェクトの FieldSize プロパティを使用します。 ロング バイナリ型 (Long Binary) またはメモ型 (Memo) のフィールドの最大サイズを制限するのは、システム リソースまたはデータベースが許可する最大サイズのみです。

## <a name="example"></a>例

次の例では、"Employees" テーブルの **Field** オブジェクトの名前とサイズを列挙することで、**Size** プロパティの機能を示します。

```vb
    Sub SizeX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim fldNew As Field 
     Dim fldLoop As Field 
     
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
