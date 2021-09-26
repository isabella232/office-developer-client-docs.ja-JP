---
title: Command オブジェクトのパラメーター
TOCTitle: Command object parameters
ms:assetid: b43bb20e-9d0a-b361-6845-d537ae667f0c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249862(v=office.15)
ms:contentKeyID: 48547218
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 0cdced5913f397887f9bc69e2db96e59ee43bfe0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59632113"
---
# <a name="command-object-parameters"></a>Command オブジェクトのパラメーター

**適用先**: Access 2013、Office 2013

次の例では、より注意の必要な **Command** オブジェクトの使用方法を示します。ここでは、SQL コマンドのテキストが変更され、パラメーター付きコマンドになっています。これにより、パラメーターとして渡す値をそのつど変えて、コマンドを繰り返し利用できるようになります。 **Command** オブジェクトの **Prepared** プロパティが **True** に設定されているため、プロバイダーは、 **CommandText** で指定されたコマンドを初めて実行する前に、それをコンパイルするよう要求されます。またプロバイダーは、コンパイル済みのコマンドをメモリに保存します。これにより、準備にかかるオーバーヘッドが原因で、コマンドが最初に実行されるときの時間が若干長くなりますが、それ以降にコマンドが呼び出されたときには、毎回短い時間で実行できるようになります。したがって、コマンドの準備は、コマンドが複数回使用される場合のみ実行することをお勧めします。

```vb 
 
'BeginManualParamCmd 
 On Error GoTo ErrHandler: 
 
 Dim objConn As New ADODB.Connection 
 Dim objCmd As New ADODB.Command 
 Dim objParm1 As New ADODB.Parameter 
 Dim objRs As New ADODB.Recordset 
 
 ' Set the CommandText as a parameterized SQL query. 
 objCmd.CommandText = "SELECT OrderID, OrderDate, " & _ 
 "RequiredDate, ShippedDate " & _ 
 "FROM Orders " & _ 
 "WHERE CustomerID = ? " & _ 
 "ORDER BY OrderID" 
 objCmd.CommandType = adCmdText 
 
 ' Prepare command since we will be executing it more than once. 
 objCmd.Prepared = True 
 
 ' Create new parameter for CustomerID. Initial value is ALFKI. 
 Set objParm1 = objCmd.CreateParameter("CustId", adChar, _ 
 adParamInput, 5, "ALFKI") 
 objCmd.Parameters.Append objParm1 
 
 ' Connect to the data source. 
 Set objConn = GetNewConnection 
 objCmd.ActiveConnection = objConn 
 
 ' Execute once and display... 
 Set objRs = objCmd.Execute 
 
 Debug.Print objParm1.Value 
 Do While Not objRs.EOF 
 Debug.Print vbTab & objRs(0) & vbTab & objRs(1) & vbTab & _ 
 objRs(2) & vbTab & objRs(3) 
 objRs.MoveNext 
 Loop 
 
 ' ...then set new param value, re-execute command, and display. 
 objCmd("CustId") = "CACTU" 
 Set objRs = objCmd.Execute 
 
 Debug.Print objParm1.Value 
 Do While Not objRs.EOF 
 Debug.Print vbTab & objRs(0) & vbTab & objRs(1) & vbTab & _ 
 objRs(2) & vbTab & objRs(3) 
 objRs.MoveNext 
 Loop 
 
 'clean up 
 objRs.Close 
 objConn.Close 
 Set objRs = Nothing 
 Set objConn = Nothing 
 Set objCmd = Nothing 
 Set objParm1 = Nothing 
 Exit Sub 
 
ErrHandler: 
 'clean up 
 If objRs.State = adStateOpen Then 
 objRs.Close 
 End If 
 
 If objConn.State = adStateOpen Then 
 objConn.Close 
 End If 
 
 Set objRs = Nothing 
 Set objConn = Nothing 
 Set objCmd = Nothing 
 Set objParm1 = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
'EndManualParamCmd 
```

すべてのプロバイダーが準備されたコマンドをサポートしているわけではありません。プロバイダーがコマンドの準備をサポートしていない場合は、このプロパティが **True** に設定されると、すぐにエラーが返される場合があります。エラーが返されない場合は、コマンドの準備要求が無視され、 **Prepared** プロパティが **False** に設定されます。

