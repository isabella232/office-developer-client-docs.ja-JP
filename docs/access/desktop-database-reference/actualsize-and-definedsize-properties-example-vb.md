---
title: ActualSize プロパティと DefinedSize プロパティの使用例 (VB)
TOCTitle: ActualSize and DefinedSize Properties Example (VB)
ms:assetid: fc268c63-c4b3-f633-1efb-aaf88354efd4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250291(v=office.15)
ms:contentKeyID: 48548884
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4c3d06a5937ed58843271aa2787d5a6f861f981c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478340"
---
# <a name="actualsize-and-definedsize-properties-example-vb"></a><span data-ttu-id="b4024-102">ActualSize プロパティと DefinedSize プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="b4024-102">ActualSize and DefinedSize Properties Example (VB)</span></span>


<span data-ttu-id="b4024-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="b4024-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b4024-104">次の例では、[ActualSize](actualsize-property-ado.md) プロパティと [DefinedSize](definedsize-property-ado.md) プロパティを使用して、フィールドの定義されたサイズと実際のサイズを表示します。</span><span class="sxs-lookup"><span data-stu-id="b4024-104">This example uses the [ActualSize](actualsize-property-ado.md) and [DefinedSize](definedsize-property-ado.md) properties to display the defined size and actual size of a field.</span></span>

```vb 
 
'BeginActualSizeVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'recordset and connection variables 
 Dim rstStores As ADODB.Recordset 
 Dim SQLStores As String 
 Dim strCnxn As String 
 'record variables 
 Dim strMessage As String 
 
 ' Open a recordset for the Stores table 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Northwind';Integrated Security='SSPI';" 
 Set rstStores = New ADODB.Recordset 
 
 SQLStores = "Suppliers" 
 rstStores.Open SQLStores, strCnxn, adOpenForwardOnly, adLockReadOnly, adCmdTable 
 'the above two lines of code are identical as the default values for 
 'CursorType and LockType arguments match those indicated 
 
 ' Loop through the recordset displaying the contents 
 ' of the store_name field, the field's defined size, 
 ' and its actual size. 
 rstStores.MoveFirst 
 
 Do Until rstStores.EOF 
 strMessage = "Company name: " & rstStores!CompanyName & _ 
 vbCrLf & "Defined size: " & _ 
 rstStores!CompanyName.DefinedSize & _ 
 vbCrLf & "Actual size: " & _ 
 rstStores!CompanyName.ActualSize & vbCrLf 
 
 MsgBox strMessage, vbOKCancel, "ADO ActualSize Property (Visual Basic)" 
 rstStores.MoveNext 
 Loop 
 
 ' clean up 
 rstStores.Close 
 Set rstStores = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstStores Is Nothing Then 
 If rstStores.State = adStateOpen Then rstStores.Close 
 End If 
 Set rstStores = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndActualSizeVB 
```
