---
title: PrimaryKey プロパティと Unique プロパティの使用例 (VB)
TOCTitle: PrimaryKey and Unique properties example (VB)
ms:assetid: 888f1a35-b883-2449-3b70-103e5116b29f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249597(v=office.15)
ms:contentKeyID: 48546137
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 0548f3fe629ab78fcbbebd84e9a61a3cc7a79d14
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565143"
---
# <a name="primarykey-and-unique-properties-example-vb"></a>PrimaryKey プロパティと Unique プロパティの使用例 (VB)


**適用先:** Access 2013、Office 2013

ここでは、[Index](primarykey-property-adox.md) の [PrimaryKey](unique-property-adox.md) プロパティおよび [Unique](index-object-adox.md) プロパティのコード例を示します。このコードでは 2 つの列を持つ新しいテーブルを作成します。 **PrimaryKey** プロパティおよび **Unique** プロパティを使用して列の 1 つに主キーを設定すると、重複した値の入力ができなくなります。

```vb 
 
' BeginPrimaryKeyVB 
Sub Main() 
 On Error GoTo PrimaryKeyXError 
 
 Dim catNorthwind As New ADOX.Catalog 
 Dim tblNew As New ADOX.Table 
 Dim idxNew As New ADOX.Index 
 Dim idxLoop As New ADOX.Index 
 Dim colLoop As New ADOX.Column 
 
 ' Connect the catalog 
 catNorthwind.ActiveConnection = "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\" & _ 
 "Microsoft Office\Office\Samples\Northwind.mdb';" 
 
 ' Name new table 
 tblNew.Name = "NewTable" 
 
 ' Append a numeric and a text field to new table. 
 tblNew.Columns.Append "NumField", adInteger, 20 
 tblNew.Columns.Append "TextField", adVarWChar, 20 
 
 ' Append new Primary Key index on NumField column 
 ' to new table 
 idxNew.Name = "NumIndex" 
 idxNew.Columns.Append "NumField" 
 idxNew.PrimaryKey = True 
 idxNew.Unique = True 
 tblNew.Indexes.Append idxNew 
 
 ' Append an index on Textfield to new table. 
 ' Note the different technique: Specifying index and 
 ' column name as parameters of the Append method 
 tblNew.Indexes.Append "TextIndex", "TextField" 
 
 ' Append the new table 
 catNorthwind.Tables.Append tblNew 
 
 With tblNew 
 Debug.Print tblNew.Indexes.Count & " Indexes in " & _ 
 tblNew.Name & " Table" 
 
 ' Enumerate Indexes collection. 
 For Each idxLoop In .Indexes 
 With idxLoop 
 Debug.Print "Index " & .Name 
 Debug.Print " Primary key = " & .PrimaryKey 
 Debug.Print " Unique = " & .Unique 
 
 ' Enumerate Columns collection of each Index 
 ' object. 
 Debug.Print " Columns" 
 For Each colLoop In .Columns 
 Debug.Print " " & colLoop.Name 
 Next colLoop 
 End With 
 Next idxLoop 
 
 End With 
 
 ' Delete new table as this is a demonstration. 
 catNorthwind.Tables.Delete tblNew.Name 
 
 'Clean up 
 Set catNorthwind.ActiveConnection = Nothing 
 Set catNorthwind = Nothing 
 Set tblNew = Nothing 
 Set idxNew = Nothing 
 Set idxLoop = Nothing 
 Set colLoop = Nothing 
 Exit Sub 
 
PrimaryKeyXError: 
 
 Set catNorthwind = Nothing 
 Set tblNew = Nothing 
 Set idxNew = Nothing 
 Set idxLoop = Nothing 
 Set colLoop = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndPrimaryKeyVB 
```

