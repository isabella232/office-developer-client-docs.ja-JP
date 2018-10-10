---
title: AbsolutePosition プロパティと CursorLocation プロパティの使用例 (VB)
TOCTitle: AbsolutePosition and CursorLocation Properties Example (VB)
ms:assetid: 572c1a51-b7f4-5861-cfb9-960219e0a831
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249293(v=office.15)
ms:contentKeyID: 48544966
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d32d302e1e20534e40d6d3f4c12e3fcbce78816a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478241"
---
# <a name="absoluteposition-and-cursorlocation-properties-example-vb"></a><span data-ttu-id="00974-102">AbsolutePosition プロパティと CursorLocation プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="00974-102">AbsolutePosition and CursorLocation Properties Example (VB)</span></span>


<span data-ttu-id="00974-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="00974-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="00974-p101">次の例では、[AbsolutePosition](absoluteposition-property-ado.md) プロパティを使用して [Recordset](recordset-object-ado.md) の全レコードを列挙するループの進捗を追跡する方法を示します。この例では、 [CursorLocation](cursorlocation-property-ado.md) プロパティを使用して、カーソルをクライアント カーソルに設定することにより、 **AbsolutePosition** プロパティを有効にしています。</span><span class="sxs-lookup"><span data-stu-id="00974-p101">This example demonstrates how the [AbsolutePosition](absoluteposition-property-ado.md) property can track the progress of a loop that enumerates all the records of a [Recordset](recordset-object-ado.md). It uses the [CursorLocation](cursorlocation-property-ado.md) property to enable the **AbsolutePosition** property by setting the cursor to a client cursor.</span></span>

```vb 
 
'BeginAbsolutePositionVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'recordset and connection variables 
 Dim rstEmployees As ADODB.Recordset 
 Dim Cnxn As ADODB.Connection 
 Dim strCnxn As String 
 Dim strSQL As String 
 'record variables 
 Dim strMessage As String 
 
 'Open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' Open Employee recordset with 
 ' Client-side cursor to enable AbsolutePosition property 
 Set rstEmployees = New ADODB.Recordset 
 strSQL = "employee" 
 rstEmployees.Open strSQL, strCnxn, adUseClient, adLockReadOnly, adCmdTable 
 
 ' Enumerate Recordset 
 Do While Not rstEmployees.EOF 
 ' Display current record information 
 strMessage = "Employee: " & rstEmployees!lname & vbCr & _ 
 "(record " & rstEmployees.AbsolutePosition & _ 
 " of " & rstEmployees.RecordCount & ")" 
 If MsgBox(strMessage, vbOKCancel) = vbCancel Then Exit Do 
 rstEmployees.MoveNext 
 Loop 
 
 ' clean up 
 rstEmployees.Close 
 Cnxn.Close 
 Set rstEmployees = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstEmployees Is Nothing Then 
 If rstEmployees.State = adStateOpen Then rstEmployees.Close 
 End If 
 Set rstEmployees = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndAbsolutePositionVB 
```
