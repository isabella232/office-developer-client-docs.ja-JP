---
<span data-ttu-id="1a7d6-101"><<<<<<< ヘッド タイトル: と、AbsolutePage、PageCount、および PageSize プロパティの使用例 (VB) TOCTitle: と、AbsolutePage、PageCount、および PageSize プロパティの使用例 (VB) の ms:assetid: bd13fb6c-8ee4-7475-ef2d-9067e30918de ms:mtpsurl: https://msdn.microsoft.com/library/JJ249911(v=office.15)ms:contentKeyID: 48547426 ms.date: 2015/09/18 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="1a7d6-101"><<<<<<< HEAD title: AbsolutePage, PageCount, and PageSize Properties Example (VB) TOCTitle: AbsolutePage, PageCount, and PageSize Properties Example (VB) ms:assetid: bd13fb6c-8ee4-7475-ef2d-9067e30918de ms:mtpsurl: https://msdn.microsoft.com/library/JJ249911(v=office.15) ms:contentKeyID: 48547426 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

# <a name="absolutepage-pagecount-and-pagesize-properties-example-vb"></a><span data-ttu-id="1a7d6-102">AbsolutePage プロパティ、PageCount プロパティ、および PageSize プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="1a7d6-102">AbsolutePage, PageCount, and PageSize Properties Example (VB)</span></span>
<span data-ttu-id="1a7d6-103">=== タイトル: と、AbsolutePage、PageCount、および PageSize プロパティの使用例 (VB) TOCTitle: と、AbsolutePage、PageCount、および PageSize プロパティの使用例 (VB) ms:assetid: bd13fb6c-8ee4-7475-ef2d-9067e30918de ms:mtpsurl: https://msdn.microsoft.com/library/JJ249911(v=office.15) ms:contentKeyID: 48547426ms.date: 2018/10/17 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="1a7d6-103">======= title: AbsolutePage, PageCount, and PageSize properties example (VB) TOCTitle: AbsolutePage, PageCount, and PageSize properties example (VB) ms:assetid: bd13fb6c-8ee4-7475-ef2d-9067e30918de ms:mtpsurl: https://msdn.microsoft.com/library/JJ249911(v=office.15) ms:contentKeyID: 48547426 ms.date: 10/17/2018 mtps_version: v=office.15</span></span>
---

# <a name="absolutepage-pagecount-and-pagesize-properties-example-vb"></a><span data-ttu-id="1a7d6-104">AbsolutePage、PageCount、および PageSize プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="1a7d6-104">AbsolutePage, PageCount, and PageSize properties example (VB)</span></span>
>>>>>>> <span data-ttu-id="1a7d6-105">master</span><span class="sxs-lookup"><span data-stu-id="1a7d6-105">master</span></span>


<span data-ttu-id="1a7d6-106">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="1a7d6-106">**Applies to**: Access 2013 | Office 2013</span></span>

<a name="-head"></a><span data-ttu-id="1a7d6-107"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="1a7d6-107"><<<<<<< HEAD</span></span>
=======
<span data-ttu-id="1a7d6-108">次の例では、[AbsolutePage](absolutepage-property-ado.md) プロパティ、[PageCount](pagecount-property-ado.md) プロパティ、および [PageSize](pagesize-property-ado.md) プロパティを使用して、***Employee*** テーブルから取得した名前と雇用年月日を一度に 5 レコードずつ表示します。</span><span class="sxs-lookup"><span data-stu-id="1a7d6-108">This example uses the [AbsolutePage](absolutepage-property-ado.md), [PageCount](pagecount-property-ado.md), and [PageSize](pagesize-property-ado.md) properties to display names and hire dates from the ***Employees*** table, five records at a time.</span></span>

>>>>>>> <span data-ttu-id="1a7d6-109">master</span><span class="sxs-lookup"><span data-stu-id="1a7d6-109">master</span></span>
```vb 
 
'BeginAbsolutePageVB 
 
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
 Dim intPage As Integer 
 Dim intPageCount As Integer 
 Dim intRecord As Integer 
 
 'Open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' Open employee recordset 
 ' Use client cursor to enable AbsolutePosition property 
 Set rstEmployees = New ADODB.Recordset 
 strSQL = "employee" 
 rstEmployees.Open strSQL, strCnxn, adUseClient, adLockReadOnly, adCmdTable 
 
 ' Display names and hire dates, five records at a time 
 rstEmployees.PageSize = 5 
 intPageCount = rstEmployees.PageCount 
 For intPage = 1 To intPageCount 
 rstEmployees.AbsolutePage = intPage 
 strMessage = "" 
 For intRecord = 1 To rstEmployees.PageSize 
 strMessage = strMessage & _ 
 rstEmployees!fname & " " & _ 
 rstEmployees!lname & " " & _ 
 rstEmployees!hire_date & vbCr 
 rstEmployees.MoveNext 
 If rstEmployees.EOF Then Exit For 
 Next intRecord 
 MsgBox strMessage 
 Next intPage 
 
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
'EndAbsolutePageVB 
```

