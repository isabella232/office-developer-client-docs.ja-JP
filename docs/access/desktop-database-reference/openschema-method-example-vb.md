---
title: OpenSchema メソッドの使用例 (VB)
TOCTitle: OpenSchema method example (VB)
ms:assetid: 02fe101a-c2df-6454-2cca-f5833e60fc03
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248797(v=office.15)
ms:contentKeyID: 48542973
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 199586c22d79b158e78d2a230db8cee081816c56
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577165"
---
# <a name="openschema-method-example-vb"></a>OpenSchema メソッドの使用例 (VB)


**適用先:** Access 2013、Office 2013

この例では、[OpenSchema](openschema-method-ado.md) メソッドを使用して、***Pubs*** データベース内の各テーブルの名前と型を表示します。

```vb 
 
'BeginOpenSchemaVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub OpenSchemaX() 
 On Error GoTo ErrorHandler 
 
 Dim Cnxn As ADODB.Connection 
 Dim rstSchema As ADODB.Recordset 
 Dim strCnxn As String 
 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 Set rstSchema = Cnxn.OpenSchema(adSchemaTables) 
 
 Do Until rstSchema.EOF 
 Debug.Print "Table name: " & _ 
 rstSchema!TABLE_NAME & vbCr & _ 
 "Table type: " & rstSchema!TABLE_TYPE & vbCr 
 rstSchema.MoveNext 
 Loop 
 
 ' clean up 
 rstSchema.Close 
 Cnxn.Close 
 Set rstSchema = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstSchema Is Nothing Then 
 If rstSchema.State = adStateOpen Then rstSchema.Close 
 End If 
 Set rstSchema = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndOpenSchemaVB 
```

<br/>

次の使用例は \_ **、OpenSchema** メソッド Criteria _ 引数に TABLE TYPE クエリ **_制約を_*指定します。その結果、_*_Pubs_** データベースで指定されたビューのスキーマ情報だけが返されます。 その後、この例では各テーブルの名前と型を表示します。

```vb 
 
'BeginOpenSchema2VB 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 Dim Cnxn2 As ADODB.Connection 
 Dim rstSchema As ADODB.Recordset 
 Dim strCnxn As String 
 
 Set Cnxn2 = New ADODB.Connection 
 strCnxn = "Provider=sqloledb;" & _ 
 "Data Source=MySqlServer;Initial Catalog=Pubs;Integrated Security=SSPI; " 
 Cnxn2.Open strCnxn 
 
 Set rstSchema = Cnxn2.OpenSchema(adSchemaTables, Array(Empty, Empty, Empty, "VIEW")) 
 
 Do Until rstSchema.EOF 
 Debug.Print "Table name: " & _ 
 rstSchema!TABLE_NAME & vbCr & _ 
 "Table type: " & rstSchema!TABLE_TYPE & vbCr 
 rstSchema.MoveNext 
 Loop 
 
 ' clean up 
 rstSchema.Close 
 Cnxn2.Close 
 Set rstSchema = Nothing 
 Set Cnxn2 = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstSchema Is Nothing Then 
 If rstSchema.State = adStateOpen Then rstSchema.Close 
 End If 
 Set rstSchema = Nothing 
 
 If Not Cnxn2 Is Nothing Then 
 If Cnxn2.State = adStateOpen Then Cnxn2.Close 
 End If 
 Set Cnxn2 = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndOpenSchema2VB 
```

