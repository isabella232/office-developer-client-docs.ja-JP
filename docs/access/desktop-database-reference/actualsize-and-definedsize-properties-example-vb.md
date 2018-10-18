---
<span data-ttu-id="fd39e-101"><<<<<<< ヘッド タイトル: ActualSize、DefinedSize プロパティの使用例 (VB) TOCTitle: ActualSize、DefinedSize プロパティの使用例 (VB) の ms:assetid: fc268c63-c4b3-f633-1efb-aaf88354efd4 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250291(v=office.15) ms:contentKeyID。48548884 ms.date: 2015/09/18 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="fd39e-101"><<<<<<< HEAD title: ActualSize and DefinedSize Properties Example (VB) TOCTitle: ActualSize and DefinedSize Properties Example (VB) ms:assetid: fc268c63-c4b3-f633-1efb-aaf88354efd4 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250291(v=office.15) ms:contentKeyID: 48548884 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

# <a name="actualsize-and-definedsize-properties-example-vb"></a><span data-ttu-id="fd39e-102">ActualSize プロパティと DefinedSize プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="fd39e-102">ActualSize and DefinedSize Properties Example (VB)</span></span>
<span data-ttu-id="fd39e-103">=== タイトル: ActualSize、DefinedSize プロパティの使用例 (VB) TOCTitle: ActualSize、DefinedSize プロパティの使用例 (VB) ms:assetid: fc268c63-c4b3-f633-1efb-aaf88354efd4 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250291(v=office.15) ms:contentKeyID: 48548884 ms.date: 2018/10/16 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="fd39e-103">======= title: ActualSize and DefinedSize properties example (VB) TOCTitle: ActualSize and DefinedSize properties example (VB) ms:assetid: fc268c63-c4b3-f633-1efb-aaf88354efd4 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250291(v=office.15) ms:contentKeyID: 48548884 ms.date: 10/16/2018 mtps_version: v=office.15</span></span>
---

# <a name="actualsize-and-definedsize-properties-example-vb"></a><span data-ttu-id="fd39e-104">ActualSize、DefinedSize プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="fd39e-104">ActualSize and DefinedSize properties example (VB)</span></span>
>>>>>>> <span data-ttu-id="fd39e-105">master</span><span class="sxs-lookup"><span data-stu-id="fd39e-105">master</span></span>


<span data-ttu-id="fd39e-106">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="fd39e-106">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="fd39e-107">次の例では、[ActualSize](actualsize-property-ado.md) プロパティと [DefinedSize](definedsize-property-ado.md) プロパティを使用して、フィールドの定義されたサイズと実際のサイズを表示します。</span><span class="sxs-lookup"><span data-stu-id="fd39e-107">This example uses the [ActualSize](actualsize-property-ado.md) and [DefinedSize](definedsize-property-ado.md) properties to display the defined size and actual size of a field.</span></span>

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

