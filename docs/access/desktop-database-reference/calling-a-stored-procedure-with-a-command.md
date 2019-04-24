---
title: コマンドを使用したストアド プロシージャの呼び出し
TOCTitle: Calling a stored procedure with a command
ms:assetid: 19d600d7-f717-39df-11a0-951e3ed0f812
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248944(v=office.15)
ms:contentKeyID: 48543509
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6578dbfc50ae8ffeaa31f49b694b37ba5fd534e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296711"
---
# <a name="calling-a-stored-procedure-with-a-command"></a>コマンドを使用したストアド プロシージャの呼び出し


**適用先:** Access 2013、Office 2013

ストアド プロシージャを呼び出すときにも、コマンドを使用できます。このトピックのコードでは、Northwind のサンプル データベースで、CustOrdersOrders というストアド プロシージャを呼び出します。このストアド プロシージャは次のように定義されます。

```vb 
 
CREATE PROCEDURE CustOrdersOrders @CustomerID nchar(5) AS 
SELECT OrderID, OrderDate, RequiredDate, ShippedDate 
FROM Orders 
WHERE CustomerID = @CustomerID 
ORDER BY OrderID 
```

このストアド プロシージャは、顧客 ID をパラメーターとして受け取り、その顧客の注文に関する情報を返すという点で、「[Command オブジェクトのパラメーター](command-object-parameters.md)」で使用されているコマンドと似ています。次のコードでは、このストアド プロシージャを ADO の **Recordset** のソースとして使用します。

ストアド プロシージャを使用すると、ADO のもう 1 つの機能である **Parameters** コレクションの **Refresh** メソッドを使用できるようになります。このメソッドを使用することにより、コマンドに必要なパラメーターに関するすべての情報が、実行時に ADO によって自動的に設定されます。この手法を使用すると、ADO がパラメーターに関する情報をデータ ソースに照会する必要があるため、パフォーマンスが低下します。

次に示すコードと、パラメーターが手動で入力される「[Command オブジェクトのパラメーター](command-object-parameters.md)」のコードには、他にも重要な違いがあります。まず、このコードは SQL サーバーのストアド プロシージャであり、定義上あらかじめコンパイルされているため、 **Prepared** プロパティが **True** に設定されません。次に、この例では、 **Command** オブジェクトの **CommandType** プロパティが **adCmdStoredProc** に変更され、コマンドがストアド プロシージャであることが ADO に通知されています。

```vb 
 
'BeginAutoParamCmd 
 On Error GoTo ErrHandler: 
 
 Dim objConn As New ADODB.Connection 
 Dim objCmd As New ADODB.Command 
 Dim objParm1 As New ADODB.Parameter 
 Dim objRs As New ADODB.Recordset 
 
 ' Set CommandText equal to the stored procedure name. 
 objCmd.CommandText = "CustOrdersOrders" 
 objCmd.CommandType = adCmdStoredProc 
 
 ' Connect to the data source. 
 Set objConn = GetNewConnection 
 objCmd.ActiveConnection = objConn 
 
 ' Automatically fill in parameter info from stored procedure. 
 objCmd.Parameters.Refresh 
 
 ' Set the param value. 
 objCmd(1) = "ALFKI" 
 
 ' Execute once and display... 
 Set objRs = objCmd.Execute 
 
 Debug.Print objParm1.Value 
 Do While Not objRs.EOF 
 Debug.Print vbTab & objRs(0) & vbTab & objRs(1) & vbTab & _ 
 objRs(2) & vbTab & objRs(3) 
 objRs.MoveNext 
 Loop 
 
 ' ...then set new param value, re-execute command, and display. 
 objCmd(1) = "CACTU" 
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
'EndAutoParamCmd 
```

