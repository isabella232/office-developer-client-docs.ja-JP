---
title: ParentCatalog プロパティの使用例 (VB)
TOCTitle: ParentCatalog Property Example (VB)
ms:assetid: 3bd01153-40b5-1a45-67e2-eb8154c3fe33
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249152(v=office.15)
ms:contentKeyID: 48544295
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d8ea3b28b6b6d6dff7de630beeb8929b050a7609
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478211"
---
# <a name="parentcatalog-property-example-vb"></a><span data-ttu-id="4fe51-102">ParentCatalog プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="4fe51-102">ParentCatalog Property Example (VB)</span></span>


<span data-ttu-id="4fe51-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="4fe51-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4fe51-p101">次のコードでは、テーブルをカタログに追加する前に プロバイダー に固有のプロパティにアクセスするための、[ParentCatalog](parentcatalog-property-adox.md) プロパティの使用方法を示します。このプロパティは、Microsoft Jet データベース内に AutoIncrement フィールドを作成する AutoIncrement です。</span><span class="sxs-lookup"><span data-stu-id="4fe51-p101">The following code demonstrates how to use the [ParentCatalog](parentcatalog-property-adox.md) property to access a provider-specific property prior to appending a table to a catalog. The property is AutoIncrement, which creates an AutoIncrement field in a Microsoft Jet database.</span></span>

```vb 
 
' BeginCreateAutoIncrColumnVB 
Sub Main() 
 On Error GoTo CreateAutoIncrColumnError 
 
 Dim cnn As New ADODB.Connection 
 Dim cat As New ADOX.Catalog 
 Dim tbl As New ADOX.Table 
 
 cnn.Open "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\" & _ 
 "Microsoft Office\Office\Samples\Northwind.mdb';" 
 Set cat.ActiveConnection = cnn 
 
 With tbl 
 .Name = "MyContacts" 
 Set .ParentCatalog = cat 
 ' Create fields and append them to the new Table object. 
 .Columns.Append "ContactId", adInteger 
 ' Make the ContactId column and auto incrementing column 
 .Columns("ContactId").Properties("AutoIncrement") = True 
 .Columns.Append "CustomerID", adVarWChar 
 .Columns.Append "FirstName", adVarWChar 
 .Columns.Append "LastName", adVarWChar 
 .Columns.Append "Phone", adVarWChar, 20 
 .Columns.Append "Notes", adLongVarWChar 
 End With 
 
 cat.Tables.Append tbl 
 Debug.Print "Table 'MyContacts' is added." 
 
 ' Delete the table as this is a demonstration. 
 cat.Tables.Delete tbl.Name 
 Debug.Print "Table 'MyContacts' is delete." 
 
 'Clean up 
 cnn.Close 
 Set cat = Nothing 
 Set tbl = Nothing 
 Set cnn = Nothing 
 Exit Sub 
 
CreateAutoIncrColumnError: 
 
 Set cat = Nothing 
 Set tbl = Nothing 
 
 If Not cnn Is Nothing Then 
 If cnn.State = adStateOpen Then cnn.Close 
 End If 
 Set cnn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
' EndCreateAutoIncrColumnVB 
```
