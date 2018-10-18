---
<span data-ttu-id="d27fa-101"><<<<<<< ヘッド タイトル: StayInSync プロパティの使用例 (VB) TOCTitle: StayInSync プロパティの使用例 (VB) === タイトル: StayInSync プロパティの使用例 (VB) TOCTitle: StayInSync プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="d27fa-101"><<<<<<< HEAD title: StayInSync Property Example (VB) TOCTitle: StayInSync Property Example (VB) ======= title: StayInSync property example (VB) TOCTitle: StayInSync property example (VB)</span></span>
>>>>>>> <span data-ttu-id="d27fa-102">マスターの ms:assetid: 1b35f19a-0104-efd5-5222-55f92e08473b ms:mtpsurl: https://msdn.microsoft.com/library/JJ248952(v=office.15) ms:contentKeyID: 48543535 ms.date: 2015/09/18 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="d27fa-102">master ms:assetid: 1b35f19a-0104-efd5-5222-55f92e08473b ms:mtpsurl: https://msdn.microsoft.com/library/JJ248952(v=office.15) ms:contentKeyID: 48543535 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="d27fa-103"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="d27fa-103"><<<<<<< HEAD</span></span>
# <a name="stayinsync-property-example-vb"></a><span data-ttu-id="d27fa-104">StayInSync プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="d27fa-104">StayInSync Property Example (VB)</span></span>
=======
# <a name="stayinsync-property-example-vb"></a><span data-ttu-id="d27fa-105">StayInSync プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="d27fa-105">StayInSync property example (VB)</span></span>
>>>>>>> <span data-ttu-id="d27fa-106">master</span><span class="sxs-lookup"><span data-stu-id="d27fa-106">master</span></span>


<span data-ttu-id="d27fa-107">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="d27fa-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d27fa-108">この例では、階層 [Recordset](stayinsync-property-ado.md) 内の行へのアクセスを容易にする [StayInSync](recordset-object-ado.md) プロパティの機能を示します。</span><span class="sxs-lookup"><span data-stu-id="d27fa-108">This example demonstrates how the [StayInSync](stayinsync-property-ado.md) property facilitates accessing rows in a hierarchical [Recordset](recordset-object-ado.md).</span></span>

<span data-ttu-id="d27fa-p101">外側のループで、各作成者の姓名、州、および ID を表示します。各行に追加された **Recordset** が [Fields](fields-collection-ado.md) コレクションから取得され、親の **Recordset** が新しい行に移動するたびに **StayInSync** プロパティによって自動的に **rstTitleAuthor** に割り当てられます。内側のループでは、追加されたレコードセットの各行から 4 つのフィールドを表示します。</span><span class="sxs-lookup"><span data-stu-id="d27fa-p101">The outer loop displays each author's first and last name, state, and identification. The appended **Recordset** for each row is retrieved from the [Fields](fields-collection-ado.md) collection and automatically assigned to **rstTitleAuthor** by the **StayInSync** property whenever the parent **Recordset** moves to a new row. The inner loop displays four fields from each row in the appended recordset.</span></span>

```vb 
 
'BeginStayInSyncVB 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'To integrate this code create a DSN called Pubs 
 'with a user_id = sa and no password 
 
 Dim Cnxn As ADODB.Connection 
 Dim rst As ADODB.Recordset 
 Dim rstTitleAuthor As New ADODB.Recordset 
 Dim strCnxn As String 
 
 ' open connection with Data Shape attributes 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider=MSDataShape;Data Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' create recordset 
 Set rst = New ADODB.Recordset 
 rst.StayInSync = True 
 rst.Open "SHAPE {select * from Authors} " & _ 
 "APPEND ( { select * from titleauthor} AS chapTitleAuthor " & _ 
 "RELATE au_id TO au_id) ", Cnxn, , , adCmdText 
 
 Set rstTitleAuthor = rst("chapTitleAuthor").Value 
 Do Until rst.EOF 
 Debug.Print rst!au_fname & " " & rst!au_lname & " " & _ 
 rst!State & " " & rst!au_id 
 
 Do Until rstTitleAuthor.EOF 
 Debug.Print rstTitleAuthor(0) & " " & rstTitleAuthor(1) & " " & _ 
 rstTitleAuthor(2) & " " & rstTitleAuthor(3) 
 rstTitleAuthor.MoveNext 
 Loop 
 
 rst.MoveNext 
 Loop 
 
 ' clean up 
 rst.Close 
 Cnxn.Close 
 Set rst = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rst Is Nothing Then 
 If rst.State = adStateOpen Then rst.Close 
 End If 
 Set rst = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndStayInSyncVB 
```

