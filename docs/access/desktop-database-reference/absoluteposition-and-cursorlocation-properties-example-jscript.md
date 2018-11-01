---
title: AbsolutePosition プロパティと CursorLocation プロパティの使用例 (JScript)
TOCTitle: AbsolutePosition and CursorLocation properties example (JScript)
ms:assetid: dc98dbcc-ad00-91cb-1cf0-ee6c9150a391
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250117(v=office.15)
ms:contentKeyID: 48548142
ms.date: 10/17/2018
mtps_version: v=office.15
ms.openlocfilehash: 85dbd90fcf70b9c98414e1e2d496a51c356d096d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885606"
---
# <a name="absoluteposition-and-cursorlocation-properties-example-jscript"></a><span data-ttu-id="c0f80-102">AbsolutePosition プロパティと CursorLocation プロパティの使用例 (JScript)</span><span class="sxs-lookup"><span data-stu-id="c0f80-102">AbsolutePosition and CursorLocation properties example (JScript)</span></span>

<span data-ttu-id="c0f80-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="c0f80-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c0f80-p101">次の例では、[AbsolutePosition](absoluteposition-property-ado.md) プロパティを使用して [Recordset](recordset-object-ado.md) の全レコードを列挙するループの進捗を追跡する方法を示します。この例では、 [CursorLocation](cursorlocation-property-ado.md) プロパティを使用して、カーソルをクライアント カーソルに設定することにより、 **AbsolutePosition** プロパティを有効にしています。以下のコードをコピーして、メモ帳などのテキスト エディターに貼り付け、" **AbsolutePositionJS.asp** " という名前で保存してください。</span><span class="sxs-lookup"><span data-stu-id="c0f80-p101">This example demonstrates how the [AbsolutePosition](absoluteposition-property-ado.md) property can track the progress of a loop that enumerates all the records of a [Recordset](recordset-object-ado.md). It uses the [CursorLocation](cursorlocation-property-ado.md) property to enable the **AbsolutePosition** property by setting the cursor to a client cursor. Cut and paste the following code to Notepad or another text editor, and save it as **AbsolutePositionJS.asp**.</span></span>

```javascript
<!-- BeginAbsolutePositionJS --> 
<%@LANGUAGE="JScript" %> 
<%// use this meta tag instead of adojavas.inc%> 
<!--METADATA TYPE="typelib" uuid="00000205-0000-0010-8000-00AA006D2EA4" --> 
 
<html> 
 
<head> 
<title>AbsolutePosition and CursorLocation properties example (JScript)</title> 
<style> 
<!-- 
BODY { 
 font-family: 'Verdana','Arial','Helvetica',sans-serif; 
 BACKGROUND-COLOR:white; 
 COLOR:black; 
 } 
.thead2 { 
 background-color: #800000; 
 font-family: 'Verdana','Arial','Helvetica',sans-serif; 
 font-size: x-small; 
 color: white; 
 } 
.tbody { 
 text-align: center; 
 background-color: #f7efde; 
 font-family: 'Verdana','Arial','Helvetica',sans-serif; 
 font-size: x-small; 
 } 
--> 
</style> 
</head> 
 
<body> 
<h1>AbsolutePosition and CursorLocation properties example (JScript)</h1> 
<% 
 // connection and recordset variables 
 var strCnxn = "Provider='sqloledb';Data Source=" + Request.ServerVariables("SERVER_NAME") + ";" + 
 "Initial Catalog='Northwind';Integrated Security='SSPI';"; 
 var rsEmployee = Server.CreateObject("ADODB.Recordset"); 
 // display string 
 var strMessage; 
 
 try 
 { 
 // Open a recordset on the Employee table using 
 // a client-side cursor to enable AbsolutePosition property. 
 rsEmployee.CursorLocation = adUseClient; 
 rsEmployee.Open("employees", strCnxn, adOpenStatic, adLockOptimistic, adCmdTable); 
 
 // Write beginning of table to the document. 
 Response.Write('<table border="0" align="center">'); 
 Response.Write('<tr class="thead2">'); 
 Response.Write("<th>AbsolutePosition</th><th>Name</th><th>Hire Date</th></tr>"); 
 
 while (!rsEmployee.EOF) 
 { 
 strMessage = ""; 
 
 // Start a new table row. 
 strMessage = '<tr class="tbody">'; 
 
 // First column in row contains AbsolutePosition value. 
 strMessage += "<td>" + rsEmployee.AbsolutePosition + " of " + rsEmployee.RecordCount + "</td>" 
 
 // First and last name are in first column. 
 strMessage += "<td>" + rsEmployee.Fields("FirstName") + " "; 
 strMessage += rsEmployee.Fields("LastName") + " " + "</td>"; 
 
 // Hire date in second column. 
 strMessage += "<td>" + rsEmployee.Fields("HireDate") + "</td>"; 
 
 // End the row. 
 strMessage += "</tr>"; 
 
 // Write line to document. 
 Response.Write(strMessage); 
 
 // Get next record. 
 rsEmployee.MoveNext; 
 } 
 
 // Finish writing document. 
 Response.Write("</table>"); 
 } 
 catch (e) 
 { 
 Response.Write(e.message); 
 } 
 finally 
 { 
 // 'clean up 
 if (rsEmployee.State == adStateOpen) 
 rsEmployee.Close; 
 rsEmployee = null; 
 } 
%> 
 
</html> 
<!-- EndAbsolutePositionJS --> 
```

