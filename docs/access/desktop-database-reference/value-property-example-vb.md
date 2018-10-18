---
<<<<<<< ヘッド タイトル: 値のプロパティの使用例 (VB) TOCTitle: 値のプロパティの使用例 (VB) === タイトル: 値プロパティの使用例 (VB) TOCTitle: 値プロパティの使用例 (VB)
>>>>>>> マスターの ms:assetid: c2319a14-e86f-6dc1-b203-fd5f35ffa04f ms:mtpsurl: https://msdn.microsoft.com/library/JJ249947(v=office.15) ms:contentKeyID: 48547547 ms.date: 2015/09/18 mtps_version: v=office.15
---

<<<<<<< ヘッド
# <a name="value-property-example-vb"></a>Value プロパティの使用例 (VB)
=======
# <a name="value-property-example-vb"></a>値プロパティの使用例 (VB)
>>>>>>> master


**適用されます**Access 2013 |。Office 2013

この例では、[Field](field-object-ado.md) オブジェクトや [Property](property-object-ado.md) オブジェクトで [Value](value-property-ado.md) プロパティを使用して、***Employees*** テーブルのフィールドとプロパティの値を表示します。

```vb 
 
'BeginValueVB 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
 ' connection and recordset variables 
 Dim rstEmployees As ADODB.Recordset 
 Dim Cnxn As ADODB.Connection 
 Dim strCnxn As String 
 Dim strSQLEmployees As String 
 ' field property variables 
 Dim fld As ADODB.Field 
 Dim prp As ADODB.Property 
 
 ' Open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' Open recordset with data from Employees table 
 Set rstEmployees = New ADODB.Recordset 
 strSQLEmployees = "employee" 
 rstEmployees.Open strSQLEmployees, Cnxn, , , adCmdTable 
 'rstEmployees.Open strSQLEmployees, Cnxn, adOpenStatic, adLockReadOnly, adCmdTable 
 ' the above two lines of code are identical 
 
 Debug.Print "Field values in rstEmployees" 
 
 ' Enumerate the Fields collection of the Employees table 
 For Each fld In rstEmployees.Fields 
 ' Because Value is the default property of a 
 ' Field object, the use of the actual keyword 
 ' here is optional. 
 Debug.Print " " & fld.Name & " = " & fld.Value 
 Next fld 
 
 Debug.Print "Property values in rstEmployees" 
 
 ' Enumerate the Properties collection of the Recordset object 
 For Each prp In rstEmployees.Properties 
 Debug.Print " " & prp.Name & " = " & prp.Value 
 ' because Value is the default property of a Property object 
 ' use of the actual Value keyword is optional 
 Next prp 
 
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
'EndValueVB 
```

