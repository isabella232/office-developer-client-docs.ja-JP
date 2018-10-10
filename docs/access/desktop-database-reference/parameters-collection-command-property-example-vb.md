---
title: Parameters コレクションの Command プロパティの使用例 (VB)
TOCTitle: Parameters Collection, Command Property Example (VB)
ms:assetid: 3bb3e6e1-0ee5-70bb-7f2c-beb461d3914a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249151(v=office.15)
ms:contentKeyID: 48544290
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b4a1f1074a81ef5d5aa14192e784b91d0c9fcddb
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478341"
---
# <a name="parameters-collection-command-property-example-vb"></a><span data-ttu-id="baffd-102">Parameters コレクションの Command プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="baffd-102">Parameters Collection, Command Property Example (VB)</span></span>


<span data-ttu-id="baffd-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="baffd-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="baffd-104">次のコードでは、プロシージャのパラメーター情報を取得するために [Command](command-property-adox.md) オブジェクトの [Command](command-object-ado.md) プロパティを使用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="baffd-104">The following code demonstrates how to use the [Command](command-property-adox.md) property with the [Command](command-object-ado.md) object to retrieve parameter information for the procedure.</span></span>

```vb 
 
' BeginParametersVB 
Sub Main() 
 On Error GoTo ProcedureParametersError 
 
 Dim cnn As New ADODB.Connection 
 Dim cmd As ADODB.Command 
 Dim prm As ADODB.Parameter 
 Dim cat As New ADOX.Catalog 
 
 ' Open the Connection 
 cnn.Open _ 
 "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\Microsoft Office\" & _ 
 "Office\Samples\Northwind.mdb';" 
 
 ' Open the catalog 
 Set cat.ActiveConnection = cnn 
 
 ' Get the command object 
 Set cmd = cat.Procedures("CustomerById").Command 
 
 ' Retrieve Parameter information 
 cmd.Parameters.Refresh 
 For Each prm In cmd.Parameters 
 Debug.Print prm.Name & ":" & prm.Type 
 Next 
 
 'Clean up 
 cnn.Close 
 Set cat = Nothing 
 Set cmd = Nothing 
 Set cnn = Nothing 
 Exit Sub 
 
ProcedureParametersError: 
 
 Set cat = Nothing 
 Set cmd = Nothing 
 
 If Not cnn Is Nothing Then 
 If cnn.State = adStateOpen Then cnn.Close 
 End If 
 Set cnn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndParametersVB 
```

