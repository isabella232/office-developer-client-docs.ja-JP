---
title: VBScript でのエラー処理
TOCTitle: Handling errors in VBScript
ms:assetid: df8f96d5-b917-ddac-d274-6345b2499bf1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250135(v=office.15)
ms:contentKeyID: 48548222
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 1b5386cad5c916c8ee2276af5e1741b418a42d22
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589506"
---
# <a name="handling-errors-in-vbscript"></a>VBScript でのエラー処理


**適用先**: Access 2013、Office 2013

Visual Basic で使用する方法と VBScript で使用する方法には、若干の違いがあります。 主な違いは、VBScript では、ラベルで実行を継続することによるエラー処理の概念がサポートされていないことです。 つまり、VBScript で On Error GoTo を使用することはできません。 代わりに、VBScript で On Error Resume Next を使用し、次の例に示すように **、Errors** コレクションの **Err.Number** プロパティと **Count** プロパティの両方をチェックします。

```vb 
 
<!-- BeginErrorExampleVBS --> 
<HTML> 
<HEAD> 
<META NAME="GENERATOR" Content="Microsoft Visual Studio 6.0"> 
<TITLE>Error Handling example (VBScript)</TITLE> 
</HEAD> 
<BODY> 
 
<h1>Error Handling example (VBScript)</h1> 
 
<% 
 Dim errLoop 
 Dim strError 
 
 On Error Resume Next 
 
 ' Intentionally trigger an error. 
 Set cnn1 = Server.CreateObject("ADODB.Connection") 
 cnn1.Open "nothing" 
 
 If cnn1.Errors.Count > 0 Then 
 ' Enumerate Errors collection and display 
 ' properties of each Error object. 
 For Each errLoop In cnn1.Errors 
 strError = "Error #" & errLoop.Number & "<br>" & _ 
 " " & errLoop.Description & "<br>" & _ 
 " (Source: " & errLoop.Source & ")" & "<br>" & _ 
 " (SQL State: " & errLoop.SQLState & ")" & "<br>" & _ 
 " (NativeError: " & errLoop.NativeError & ")" & "<br>" 
 If errLoop.HelpFile = "" Then 
 strError = strError & _ 
 " No Help file available" & _ 
 "<br><br>" 
 Else 
 strError = strError & _ 
 " (HelpFile: " & errLoop.HelpFile & ")" & "<br>" & _ 
 " (HelpContext: " & errLoop.HelpContext & ")" & _ 
 "<br><br>" 
 End If 
 Response.Write ("<p>" & strError & "</p>") 
 Next 
 End If 
%> 
 
</BODY> 
</HTML> 
<!-- EndErrorExampleVBS --> 
```

