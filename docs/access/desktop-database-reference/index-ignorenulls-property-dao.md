---
title: Index.IgnoreNulls プロパティ (DAO)
TOCTitle: IgnoreNulls Property
ms:assetid: f49f17b8-d7c1-18ab-07a8-e1be61488519
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836698(v=office.15)
ms:contentKeyID: 48548694
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052931
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 51d6ffd9c07ec9d03f9dfce54f98b8edaabf7145
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585635"
---
# <a name="indexignorenulls-property-dao"></a>Index.IgnoreNulls プロパティ (DAO)


**適用先:** Access 2013、Office 2013

インデックス フィールドに Null 値を持つレコードがインデックス エントリを持つかどうかを示す値を設定または取得します (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式* .IgnoreNulls

*式* Index オブジェクトを表す **変数** 。

## <a name="remarks"></a>注釈

このプロパティは、新しい **[Index](index-object-dao.md)** オブジェクトがコレクションに追加されていない場合は値の取得および設定が可能で、 [**Indexes**](indexes-collection-dao.md) コレクション内の既存の **Index** オブジェクトの場合は値の取得のみ可能です。

レコードをより短時間で検索するために、フィールドのインデックスを定義できます。インデックス フィールドへの **null** の入力を許可し、多くの入力値が **null** になる場合、 **Index** オブジェクトの **IgnoreNulls** プロパティを **True** に設定すると、インデックスによって使用される記憶域の容量を節約できます。

**IgnoreNulls** プロパティの設定および **[Required](field-required-property-dao.md)** プロパティの設定によって、インデックス値が **null** のレコードがインデックス エントリを持つかどうかが決まります。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>IgnoreNulls の値</p></th>
<th><p>Required の値</p></th>
<th><p>Then</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>True</p></td>
<td><p>False</p></td>
<td><p>インデックス フィールドへの Null 値の入力が許可されます。インデックス エントリは追加されません。</p></td>
</tr>
<tr class="even">
<td><p>False</p></td>
<td><p>False</p></td>
<td><p>インデックス フィールドへの Null 値の入力が許可されます。インデックス エントリが追加されます。</p></td>
</tr>
<tr class="odd">
<td><p>True または False</p></td>
<td><p>正解</p></td>
<td><p>インデックス フィールドへの Null 値の入力は許可されません。インデックス エントリは追加されません。</p></td>
</tr>
</tbody>
</table>


## <a name="example"></a>例

この例では、新しい **Index** オブジェクトの **IgnoreNulls** プロパティを、ユーザーの入力に基づいて **True** または **False** に設定し、キー フィールドに **Null** 値が含まれているレコードによる **Recordset** オブジェクトへの影響を示します。

```vb
    Sub IgnoreNullsX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxNew As Index 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create a new Index object. 
     Set idxNew = .CreateIndex("NewIndex") 
     idxNew.Fields.Append idxNew.CreateField("Country") 
     
     ' Set the IgnoreNulls property of the new Index object 
     ' based on the user's input. 
     Select Case MsgBox("Set IgnoreNulls to True?", _ 
     vbYesNoCancel) 
     Case vbYes 
     idxNew.IgnoreNulls = True 
     Case vbNo 
     idxNew.IgnoreNulls = False 
     Case Else 
     dbsNorthwind.Close 
     End 
     End Select 
     
     ' Append the new Index object to the Indexes 
     ' collection of the Employees table. 
     .Indexes.Append idxNew 
     .Indexes.Refresh 
     End With 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     With rstEmployees 
     ' Add a new record to the Employees table. 
     .AddNew 
     !FirstName = "Gary" 
     !LastName = "Haarsager" 
     .Update 
     
     ' Use the new index to set the order of the records. 
     .Index = idxNew.Name 
     .MoveFirst 
     
     Debug.Print "Index = " & .Index & _ 
     ", IgnoreNulls = " & idxNew.IgnoreNulls 
     Debug.Print " Country - Name" 
     
     ' Enumerate the Recordset. The value of the 
     ' IgnoreNulls property will determine if the newly 
     ' added record appears in the output. 
     Do While Not .EOF 
     Debug.Print " " & _ 
     IIf(IsNull(!Country), "[Null]", !Country) & _ 
     " - " & !FirstName & " " & !LastName 
     .MoveNext 
     Loop 
     
     ' Delete new record because this is a demonstration. 
     .Index = "" 
     .Bookmark = .LastModified 
     .Delete 
     .Close 
     End With 
     
     ' Delete new Index because this is a demonstration. 
     tdfEmployees.Indexes.Delete idxNew.Name 
     dbsNorthwind.Close 
     
    End Sub
```
