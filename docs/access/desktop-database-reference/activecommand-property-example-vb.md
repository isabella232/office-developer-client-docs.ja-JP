---
<span data-ttu-id="a794c-101"><<<<<<< ヘッド タイトル: ActiveCommand プロパティの使用例 (VB) TOCTitle: ActiveCommand プロパティの使用例 (VB) ms:assetid: 831032cb-d557-aa98-5637-07bad65f924a ms:mtpsurl: https://msdn.microsoft.com/library/JJ249569(v=office.15) ms:contentKeyID: 48545999 ms.date: 2015/09/18 mtps_バージョン: v=office.15</span><span class="sxs-lookup"><span data-stu-id="a794c-101"><<<<<<< HEAD title: ActiveCommand Property Example (VB) TOCTitle: ActiveCommand Property Example (VB) ms:assetid: 831032cb-d557-aa98-5637-07bad65f924a ms:mtpsurl: https://msdn.microsoft.com/library/JJ249569(v=office.15) ms:contentKeyID: 48545999 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

# <a name="activecommand-property-example-vb"></a><span data-ttu-id="a794c-102">ActiveCommand プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="a794c-102">ActiveCommand Property Example (VB)</span></span>
<span data-ttu-id="a794c-103">=== タイトル: ActiveCommand プロパティの使用例 (VB) TOCTitle: ActiveCommand プロパティの使用例 (VB) ms:assetid: 831032cb-d557-aa98-5637-07bad65f924a ms:mtpsurl: https://msdn.microsoft.com/library/JJ249569(v=office.15) ms:contentKeyID: 48545999 ms.date: 2018/10/17 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="a794c-103">======= title: ActiveCommand property example (VB) TOCTitle: ActiveCommand property example (VB) ms:assetid: 831032cb-d557-aa98-5637-07bad65f924a ms:mtpsurl: https://msdn.microsoft.com/library/JJ249569(v=office.15) ms:contentKeyID: 48545999 ms.date: 10/17/2018 mtps_version: v=office.15</span></span>
---

# <a name="activecommand-property-example-vb"></a><span data-ttu-id="a794c-104">ActiveCommand プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="a794c-104">ActiveCommand property example (VB)</span></span>
>>>>>>> <span data-ttu-id="a794c-105">master</span><span class="sxs-lookup"><span data-stu-id="a794c-105">master</span></span>


<span data-ttu-id="a794c-106">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="a794c-106">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a794c-107">次の例では、[ActiveCommand](activecommand-property-ado.md) プロパティの使用方法を示します。</span><span class="sxs-lookup"><span data-stu-id="a794c-107">This example demonstrates the [ActiveCommand](activecommand-property-ado.md) property.</span></span>

<span data-ttu-id="a794c-108">サブルーチンが、[Recordset](recordset-object-ado.md) オブジェクトを受け取り、その **ActiveCommand** プロパティを使用して、 **Recordset** を作成したコマンド テキストとパラメーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="a794c-108">A subroutine is given a [Recordset](recordset-object-ado.md) object whose **ActiveCommand** property is used to display the command text and parameter that created the **Recordset**.</span></span>

```vb 
 
'BeginActiveCommandVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'recordset and connection variables 
 Dim cmd As ADODB.Command 
 Dim rst As ADODB.Recordset 
 Dim Cnxn As ADODB.Connection 
 Dim strCnxn As String 
 'record variables 
 Dim strPrompt As String 
 Dim strName As String 
 
 Set Cnxn = New ADODB.Connection 
 Set cmd = New ADODB.Command 
 
 strPrompt = "Enter an author's name (e.g., Ringer): " 
 strName = Trim(InputBox(strPrompt, "ActiveCommandX Example")) 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 
 'create SQL command string 
 cmd.CommandText = "SELECT * FROM Authors WHERE au_lname = ?" 
 cmd.Parameters.Append cmd.CreateParameter("LastName", adChar, adParamInput, 20, strName) 
 
 Cnxn.Open strCnxn 
 cmd.ActiveConnection = Cnxn 
 
 'create the recordset by executing command string 
 Set rst = cmd.Execute(, , adCmdText) 
 'see the results 
 Call ActiveCommandXprint(rst) 
 
 ' clean up 
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
'EndActiveCommandVB 
```

<span data-ttu-id="a794c-p101">**ActiveCommandXprint** ルーチンは、 **Recordset** オブジェクトしか受け取りませんが、その **Recordset** を作成したコマンド テキストとパラメーターを表示する必要があります。これが可能なのは、関連付けられている **Command** オブジェクトを **Recordset** オブジェクトの [ActiveCommand](command-object-ado.md) プロパティから取得できるからです。</span><span class="sxs-lookup"><span data-stu-id="a794c-p101">The **ActiveCommandXprint** routine is given only a **Recordset** object, yet it must print the command text and parameter that created the **Recordset**. This can be done because the **Recordset** object's **ActiveCommand** property yields the associated [Command](command-object-ado.md) object.</span></span>

<span data-ttu-id="a794c-p102">**Command** オブジェクトの [CommandText](commandtext-property-ado.md) プロパティから、**Recordset** の作成に使用されたパラメーター化されたコマンドを取得できます。**Command** オブジェクトの [Parameters](parameters-collection-ado.md) コレクションから、コマンドのパラメーター プレースホルダー ("**?**") を置き換えた値を取得できます。</span><span class="sxs-lookup"><span data-stu-id="a794c-p102">The **Command** object's [CommandText](commandtext-property-ado.md) property yields the parameterized command that created the **Recordset**. The **Command** object's [Parameters](parameters-collection-ado.md) collection yields the value that was substituted for the command's parameter placeholder ("**?**").</span></span>

<span data-ttu-id="a794c-113">最後に、エラー メッセージまたは作成者の名前と ID が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a794c-113">Finally, an error message or the author's name and ID are printed.</span></span>

```vb 
 
'BeginActiveCommandPrintVB 
Public Sub ActiveCommandXprint(rstp As ADODB.Recordset) 
 
 Dim strName As String 
 
 strName = rstp.ActiveCommand.Parameters.Item("LastName").Value 
 
 Debug.Print "Command text = '"; rstp.ActiveCommand.CommandText; "'" 
 Debug.Print "Parameter = '"; strName; "'" 
 
 If rstp.BOF = True Then 
 Debug.Print "Name = '"; strName; "', not found." 
 Else 
 Debug.Print "Name = '"; rstp!au_fname; " "; rstp!au_lname; _ 
 "', author ID = '"; rstp!au_id; "'" 
 End If 
 
 rstp.Close 
 Set rstp = Nothing 
End Sub 
'EndActiveCommandPrintVB 
```

