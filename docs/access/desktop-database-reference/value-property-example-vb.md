---
<span data-ttu-id="8e175-101"><<<<<<< ヘッド タイトル: 値のプロパティの使用例 (VB) TOCTitle: 値のプロパティの使用例 (VB) === タイトル: 値プロパティの使用例 (VB) TOCTitle: 値プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="8e175-101"><<<<<<< HEAD title: Value Property Example (VB) TOCTitle: Value Property Example (VB) ======= title: Value property example (VB) TOCTitle: Value property example (VB)</span></span>
>>>>>>> <span data-ttu-id="8e175-102">マスターの ms:assetid: c2319a14-e86f-6dc1-b203-fd5f35ffa04f ms:mtpsurl: https://msdn.microsoft.com/library/JJ249947(v=office.15) ms:contentKeyID: 48547547 ms.date: 2015/09/18 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="8e175-102">master ms:assetid: c2319a14-e86f-6dc1-b203-fd5f35ffa04f ms:mtpsurl: https://msdn.microsoft.com/library/JJ249947(v=office.15) ms:contentKeyID: 48547547 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="8e175-103"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="8e175-103"><<<<<<< HEAD</span></span>
# <a name="value-property-example-vb"></a><span data-ttu-id="8e175-104">Value プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="8e175-104">Value Property Example (VB)</span></span>
=======
# <a name="value-property-example-vb"></a><span data-ttu-id="8e175-105">値プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="8e175-105">Value property example (VB)</span></span>
>>>>>>> <span data-ttu-id="8e175-106">master</span><span class="sxs-lookup"><span data-stu-id="8e175-106">master</span></span>


<span data-ttu-id="8e175-107">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="8e175-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8e175-108">この例では、[Field](field-object-ado.md) オブジェクトや [Property](property-object-ado.md) オブジェクトで [Value](value-property-ado.md) プロパティを使用して、***Employees*** テーブルのフィールドとプロパティの値を表示します。</span><span class="sxs-lookup"><span data-stu-id="8e175-108">This example demonstrates the [Value](value-property-ado.md) property with [Field](field-object-ado.md) and [Property](property-object-ado.md) objects by displaying field and property values for the ***Employees*** table.</span></span>

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

