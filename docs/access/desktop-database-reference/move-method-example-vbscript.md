---
title: Move メソッドの使用例 (VBScript)
TOCTitle: Move method example (VBScript)
ms:assetid: 42f2eb08-47cf-f422-6176-badd414d0bfc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249198(v=office.15)
ms:contentKeyID: 48544489
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 3a0fd0094169589762012102b85bdffe4c873eb3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589387"
---
# <a name="move-method-example-vbscript"></a>Move メソッドの使用例 (VBScript)


**適用先**: Access 2013、Office 2013

この例では、[Move](move-method-ado.md) メソッドを使用して、ユーザーの入力に基づいてレコード ポインターを配置します。

次の例は、Active Server Pages (ASP) で使用してください。

**Find** を使用してファイル Adovbs.inc を検索し、使用するディレクトリに置きます。次のコードをコピーして Windows のメモ帳またはその他のテキスト エディターに貼り付け、 **MoveVBS.asp** として保存してください。結果は任意のブラウザーで表示できます。

英字や整数以外の数を入力すると、エラー処理の動作を確認できます。

```vb 
 
<!-- BeginMoveVBS --> 
<%@ Language=VBScript %> 
<%' use this meta tag instead of adovbs.inc%> 
<!--METADATA TYPE="typelib" uuid="00000205-0000-0010-8000-00AA006D2EA4" --> 
<HTML> 
<HEAD> 
<TITLE>ADO Move Methods</TITLE> 
<STYLE> 
<!-- 
BODY { 
   font-family: "MS SANS SERIF",sans-serif; 
    } 
.thead1 { 
   background-color: #008080;  
   font-family: 'Arial Narrow','Arial',sans-serif;  
   font-size: x-small; 
   color: white; 
   } 
.tbody {  
   text-align: center; 
   background-color: #f7efde; 
   font-family: 'Arial Narrow','Arial',sans-serif;  
   font-size: x-small; 
    } 
--> 
</STYLE> 
</HEAD> 
<BODY>  
<H3>ADO Move Methods</H3> 
<% ' to integrate/test this code replace the  
   ' Data Source value in the Connection string%> 
<%  
    ' connection and recordset variables 
    Dim Cnxn, strCnxn 
    Dim rsCustomers, strSQLCustomers 
 
    ' open connection 
    Set Cnxn = Server.CreateObject("ADODB.Connection") 
    strCnxn = "Provider='sqloledb';Data Source=" & _ 
            Request.ServerVariables("SERVER_NAME") & ";" & _ 
            "Integrated Security='SSPI';Initial Catalog='Northwind';" 
 
    Cnxn.Open strCnxn 
         
     ' create and open Recordset using object refs 
    Set rsCustomers = Server.CreateObject("ADODB.Recordset") 
    strSQLCustomers = "Customers" 
     
    rsCustomers.ActiveConnection = Cnxn 
    rsCustomers.CursorLocation = adUseClient 
    rsCustomers.CursorType = adOpenKeyset 
    rsCustomers.LockType = adLockOptimistic 
    rsCustomers.Source = strSQLCustomers 
    rsCustomers.Open 
 
    'Check number of user moves this session and increment by entry 
    Session("Clicks") = Session("Clicks") + Request.Form("MoveAmount") 
    Clicks = Session("Clicks") 
    ' Move to last known recordset position plus amount passed  
    rsCustomers.Move CInt(Clicks) 
 
    'Error Handling 
    If rsCustomers.EOF Then 
        Session("Clicks") = rsCustomers.RecordCount 
        Response.Write "This is the Last Record" 
        rsCustomers.MoveLast 
    ElseIf rsCustomers.BOF Then 
        Session("Clicks") = 1 
        rsCustomers.MoveFirst 
        Response.Write "This is the First Record" 
    End If 
    %> 
 
    <H3>Current Record Number is <BR> 
    <%  
    If Session("Clicks") = 0 Then Session("Clicks") = 1 
    Response.Write(Session("Clicks") )%> of <%=rsCustomers.RecordCount%></H3> 
    <HR> 
 
 
    <TABLE COLSPAN=8 CELLPADDING=5 BORDER=0> 
 
    <!-- BEGIN column header row for Customer Table--> 
 
    <TR CLASS=thead1> 
       <TD>Company Name</TD> 
       <TD>Contact Name</TD> 
       <TD>City</TD> 
    </TR> 
        <% 'display%> 
        <TR CLASS=tbody> 
          <TD> <%= rsCustomers("CompanyName")%> </TD> 
          <TD> <%= rsCustomers("ContactName")%></TD> 
          <TD> <%= rsCustomers("City")%> </TD> 
        </TR>  
    </TABLE> 
 
    <HR> 
    <Input Type=Button Name=cmdDown  Value="&lt;  "> 
    <Input Type=Button Name=cmdUp Value=" &gt;"> 
    <H5>Click Direction Arrows for Previous or Next Record 
    <BR> <BR> 
 
    <FORM Method = Post Action="MoveVbs.asp" Name=Form> 
    <TABLE> 
        <TR> 
           <TD><Input Type="Button" Name=Move Value="Move Amount "></TD> 
           <TD></TD> 
           <TD><Input Type="Text" Size="4" Name="MoveAmount" Value=0></TD> 
        <TR> 
    </TABLE> 

    Click Move Amount to use Move Method<br> 
    Enter Number of Records to Move + or - </H5>    </FORM> 
</BODY> 
 
<Script Language = "VBScript"> 
 
Sub Move_OnClick 
   ' Make sure move value entered is an integer 
   If IsNumeric(Document.Form.MoveAmount.Value)Then 
      Document.Form.MoveAmount.Value = CInt(Document.Form.MoveAmount.Value) 
      Document.Form.Submit 
   Else 
      MsgBox "You Must Enter a Number", ,"ADO-ASP Example" 
      Document.Form.MoveAmount.Value = 0 
   End If 
End Sub 
 
Sub cmdDown_OnClick 
   Document.Form.MoveAmount.Value = -1 
   Document.Form.Submit 
End Sub 
 
Sub cmdUp_OnClick 
   Document.Form.MoveAmount.Value = 1 
   Document.Form.Submit 
End Sub 
</Script> 
 
<% 
    ' clean up 
    If rsCustomers.State = adStateOpen then 
        rsCustomers.Close 
    End If 
    If Cnxn.State = adStateOpen then 
        Cnxn.Close 
    End If 
%> 
</HTML> 
<!-- EndMoveVBS --> 
```

