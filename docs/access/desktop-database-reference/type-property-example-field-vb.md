---
<span data-ttu-id="b2c06-101"><<<<<<< ヘッド タイトル: タイプ プロパティの使用例 (VB) の (フィールド) TOCTitle: タイプ プロパティの使用例 (VB) の (フィールド) === タイトル: タイプ プロパティの使用例 (VB) の (フィールド) TOCTitle: タイプ プロパティの使用例 (VB) の (フィールド)</span><span class="sxs-lookup"><span data-stu-id="b2c06-101"><<<<<<< HEAD title: Type Property Example (Field) (VB) TOCTitle: Type Property Example (Field) (VB) ======= title: Type property example (Field) (VB) TOCTitle: Type property example (Field) (VB)</span></span>
>>>>>>> <span data-ttu-id="b2c06-102">マスターの ms:assetid: ff9e26a8-898d-ec89-5093-69c66dbb05ba ms:mtpsurl: https://msdn.microsoft.com/library/JJ250314(v=office.15) ms:contentKeyID: 48548966 ms.date: 2015/09/18 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="b2c06-102">master ms:assetid: ff9e26a8-898d-ec89-5093-69c66dbb05ba ms:mtpsurl: https://msdn.microsoft.com/library/JJ250314(v=office.15) ms:contentKeyID: 48548966 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="b2c06-103"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="b2c06-103"><<<<<<< HEAD</span></span>
# <a name="type-property-example-field-vb"></a><span data-ttu-id="b2c06-104">Type プロパティの使用例 (Field) (VB)</span><span class="sxs-lookup"><span data-stu-id="b2c06-104">Type Property Example (Field) (VB)</span></span>
=======
# <a name="type-property-example-field-vb"></a><span data-ttu-id="b2c06-105">プロパティの使用例 (VB) の (フィールド) を入力します。</span><span class="sxs-lookup"><span data-stu-id="b2c06-105">Type property example (Field) (VB)</span></span>
>>>>>>> <span data-ttu-id="b2c06-106">master</span><span class="sxs-lookup"><span data-stu-id="b2c06-106">master</span></span>


<span data-ttu-id="b2c06-107">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="b2c06-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b2c06-p101">この例では、***Employees*** テーブルにあるすべての [Field](field-object-ado.md) オブジェクトの [Type](type-property-ado.md) プロパティの値に対応する定数の名前を表示することによって、[Type](type-property-ado.md) プロパティの機能を示します。このプロシージャを実行するには、FieldType 関数が必要です。</span><span class="sxs-lookup"><span data-stu-id="b2c06-p101">This example demonstrates the [Type](type-property-ado.md) property by displaying the name of the constant that corresponds to the value of the [Type](type-property-ado.md) property of all the [Field](field-object-ado.md) objects in the ***Employees*** table. The FieldType function is required for this procedure to run.</span></span>

```vb 
 
'BeginTypeFieldVB 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
 Dim Cnxn As ADODB.Connection 
 Dim rstEmployees As ADODB.Recordset 
 Dim fld As ADODB.Field 
 Dim strCnxn As String 
 Dim strSQLEmployee As String 
 Dim FieldType As String 
 
 ' Open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' Open recordset with data from Employees table 
 Set rstEmployees = New ADODB.Recordset 
 strSQLEmployee = "employee" 
 rstEmployees.Open strSQLEmployee, Cnxn, , , adCmdTable 
 'rstEmployees.Open strSQLEmployee, Cnxn, adOpenStatic, adLockReadOnly, adCmdTable 
 ' the above two lines of code are identical 
 
 Debug.Print "Fields in Employees Table:" & vbCr 
 
 ' Enumerate Fields collection of Employees table 
 For Each fld In rstEmployees.Fields 
 ' translate field-type code to text 
 Select Case fld.Type 
 Case adChar 
 FieldType = "adChar" 
 Case adVarChar 
 FieldType = "adVarChar" 
 Case adSmallInt 
 FieldType = "adSmallInt" 
 Case adUnsignedTinyInt 
 FieldType = "adUnsignedTinyInt" 
 Case adDBTimeStamp 
 FieldType = "adDBTimeStamp" 
 End Select 
 ' show results 
 Debug.Print " Name: " & fld.Name & vbCr & _ 
 " Type: " & FieldType & vbCr 
 Next fld 
 
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
 
 Set fld = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndTypeFieldVB 
```

