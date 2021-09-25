---
title: ActiveCommand プロパティの使用例 (VB)
TOCTitle: ActiveCommand property example (VB)
ms:assetid: 831032cb-d557-aa98-5637-07bad65f924a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249569(v=office.15)
ms:contentKeyID: 48545999
ms.date: 10/17/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 56834e151381c43a978f792a12d6c7d59c0df54e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586307"
---
# <a name="activecommand-property-example-vb"></a>ActiveCommand プロパティの使用例 (VB)


**適用先**: Access 2013、Office 2013

次の例では、[ActiveCommand](activecommand-property-ado.md) プロパティの使用方法を示します。

サブルーチンが、[Recordset](recordset-object-ado.md) オブジェクトを受け取り、その **ActiveCommand** プロパティを使用して、 **Recordset** を作成したコマンド テキストとパラメーターを表示します。

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

**ActiveCommandXprint** ルーチンは、 **Recordset** オブジェクトしか受け取りませんが、その **Recordset** を作成したコマンド テキストとパラメーターを表示する必要があります。これが可能なのは、関連付けられている **Command** オブジェクトを **Recordset** オブジェクトの [ActiveCommand](command-object-ado.md) プロパティから取得できるからです。

**Command** オブジェクトの [CommandText](commandtext-property-ado.md) プロパティから、**Recordset** の作成に使用されたパラメーター化されたコマンドを取得できます。**Command** オブジェクトの [Parameters](parameters-collection-ado.md) コレクションから、コマンドのパラメーター プレースホルダー ("**?**") を置き換えた値を取得できます。

最後に、エラー メッセージまたは作成者の名前と ID が表示されます。

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

