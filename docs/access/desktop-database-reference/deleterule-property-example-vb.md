---
title: DeleteRule プロパティの使用例 (VB)
TOCTitle: DeleteRule property example (VB)
ms:assetid: 354e00b6-cecb-1132-6923-fc9e8853fa0e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249114(v=office.15)
ms:contentKeyID: 48544142
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 43177dd707f47106d8be14e174d840b9815f8155
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886131"
---
# <a name="deleterule-property-example-vb"></a>DeleteRule プロパティの使用例 (VB)


**適用されます**Access 2013、Office 2013。

ここでは、[Key](deleterule-property-adox.md) オブジェクトの [DeleteRule](key-object-adox.md) プロパティの使用例を示します。このコードでは、新しい [Table オブジェクト](table-object-adox.md) を追加して新しい主キーを定義し、 **DeleteRule** を **adRICascade** に設定します。

```vb 
 
' BeginDeleteRuleVB 
Sub Main() 
 On Error GoTo DeleteRuleXError 
 
 Dim kyPrimary As New ADOX.Key 
 Dim cat As New ADOX.Catalog 
 Dim tblNew As New ADOX.Table 
 
 ' Connect the catalog 
 cat.ActiveConnection = "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "data source='c:\Program Files\" & _ 
 "Microsoft Office\Office\Samples\Northwind.mdb';" 
 
 ' Name new table 
 tblNew.Name = "NewTable" 
 
 ' Append a numeric and a text field to new table. 
 tblNew.Columns.Append "NumField", adInteger, 20 
 tblNew.Columns.Append "TextField", adVarWChar, 20 
 
 ' Append the new table 
 cat.Tables.Append tblNew 
 
 ' Define the Primary key 
 kyPrimary.Name = "NumField" 
 kyPrimary.Type = adKeyPrimary 
 kyPrimary.RelatedTable = "Customers" 
 kyPrimary.Columns.Append "NumField" 
 kyPrimary.Columns("NumField").RelatedColumn = "CustomerId" 
 kyPrimary.DeleteRule = adRICascade 
 
 ' Append the primary key 
 cat.Tables("NewTable").Keys.Append kyPrimary 
 Debug.Print "The primary key is appended." 
 
 'Delete the table as this is a demonstration. 
 cat.Tables.Delete tblNew.Name 
 Debug.Print "The primary key is deleted." 
 
 'Clean up 
 Set cat.ActiveConnection = Nothing 
 Set cat = Nothing 
 Set kyPrimary = Nothing 
 Set tblNew = Nothing 
 Exit Sub 
 
DeleteRuleXError: 
 
 Set cat = Nothing 
 Set kyPrimary = Nothing 
 Set tblNew = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
' EndDeleteRuleVB 
```

