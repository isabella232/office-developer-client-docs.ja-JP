---
<span data-ttu-id="d46b2-101"><<<<<<< ヘッド タイトル: DefinedSize プロパティの使用例 (VB) TOCTitle: DefinedSize プロパティの使用例 (VB) === タイトル: DefinedSize プロパティの使用例 (VB) TOCTitle: DefinedSize プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="d46b2-101"><<<<<<< HEAD title: DefinedSize Property Example (VB) TOCTitle: DefinedSize Property Example (VB) ======= title: DefinedSize property example (VB) TOCTitle: DefinedSize property example (VB)</span></span>
>>>>>>> <span data-ttu-id="d46b2-102">マスターの ms:assetid: 1bad5efa-dd23-b70d-c078-85a3be0729f1 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248957(v=office.15) ms:contentKeyID: 48543551 ms.date: 2015/09/18 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="d46b2-102">master ms:assetid: 1bad5efa-dd23-b70d-c078-85a3be0729f1 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248957(v=office.15) ms:contentKeyID: 48543551 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="d46b2-103"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="d46b2-103"><<<<<<< HEAD</span></span>
# <a name="definedsize-property-example-vb"></a><span data-ttu-id="d46b2-104">DefinedSize プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="d46b2-104">DefinedSize Property Example (VB)</span></span>
=======
# <a name="definedsize-property-example-vb"></a><span data-ttu-id="d46b2-105">DefinedSize プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="d46b2-105">DefinedSize property example (VB)</span></span>
>>>>>>> <span data-ttu-id="d46b2-106">master</span><span class="sxs-lookup"><span data-stu-id="d46b2-106">master</span></span>


<span data-ttu-id="d46b2-107">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="d46b2-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d46b2-108">ここでは、[Column](definedsize-property-adox.md) の [DefinedSize](column-object-adox.md) プロパティの使用例を示します。</span><span class="sxs-lookup"><span data-stu-id="d46b2-108">This example demonstrates the [DefinedSize](definedsize-property-adox.md) property of a [Column](column-object-adox.md).</span></span> <span data-ttu-id="d46b2-109">コードは、 *Northwind*データベースの [**社員**] テーブルの [フリガナ] 列のサイズを再定義します。</span><span class="sxs-lookup"><span data-stu-id="d46b2-109">The code will redefine the size of the FirstName column of the **Employees** table of the *Northwind* database.</span></span> <span data-ttu-id="d46b2-110">次に、 [Employees](field-object-ado.md) テーブルに基づいた [レコードセット](recordset-object-ado.md)の FirstName **フィールド**の値の変更が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d46b2-110">Then, the change in the values of the FirstName [Field](field-object-ado.md) of a [Recordset](recordset-object-ado.md) based on the **Employees** table is displayed.</span></span> <span data-ttu-id="d46b2-111">既定では、 **DefinedSize** プロパティを再定義すると、FirstName フィールドがスペースで埋められます。</span><span class="sxs-lookup"><span data-stu-id="d46b2-111">Note that by default, the FirstName field becomes padded with spaces after you redefine the **DefinedSize** property.</span></span>

```vb 
 
' BeginDefinedSizeVB 
Public Sub Main() 
 On Error GoTo DefinedSizeXError 
 
 Dim rstEmployees As ADODB.Recordset 
 Dim catNorthwind As New ADOX.Catalog 
 Dim colFirstName As ADOX.Column 
 Dim colNewFirstName As New ADOX.Column 
 Dim aryFirstName() As String 
 Dim i As Integer 
 Dim strCnn As String 
 
 strCnn = "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\" & _ 
 "Microsoft Office\Office\Samples\Northwind.mdb';" 
 
 ' Open a Recordset for the Employees table. 
 Set rstEmployees = New ADODB.Recordset 
 rstEmployees.Open "Employees", strCnn, adOpenKeyset, , adCmdTable 
 ReDim aryFirstName(rstEmployees.RecordCount) 
 
 ' Open a Catalog for the Northwind database, 
 ' using same connection as rstEmployees 
 Set catNorthwind.ActiveConnection = rstEmployees.ActiveConnection 
 
 ' Loop through the recordset displaying the contents 
 ' of the FirstName field, the field's defined size, 
 ' and its actual size. 
 ' Also store FirstName values in aryFirstName array. 
 rstEmployees.MoveFirst 
 Debug.Print " " 
 Debug.Print "Original Defined Size and Actual Size" 
 i = 0 
 Do Until rstEmployees.EOF 
 Debug.Print "Employee name: " & rstEmployees!FirstName & _ 
 " " & rstEmployees!LastName 
 Debug.Print " FirstName Defined size: " _ 
 & rstEmployees!FirstName.DefinedSize 
 Debug.Print " FirstName Actual size: " & _ 
 rstEmployees!FirstName.ActualSize 
 If Not rstEmployees!FirstName = Null Then 
 aryFirstName(i) = rstEmployees!FirstName 
 End If 
 rstEmployees.MoveNext 
 i = i + 1 
 Loop 
 rstEmployees.Close 
 
 ' Redefine the DefinedSize of FirstName in the catalog 
 Set colFirstName = catNorthwind.Tables("Employees").Columns("FirstName") 
 colNewFirstName.Name = colFirstName.Name 
 colNewFirstName.Type = colFirstName.Type 
 colNewFirstName.DefinedSize = colFirstName.DefinedSize + 1 
 
 ' Append new FirstName column to catalog 
 catNorthwind.Tables("Employees").Columns.Delete colFirstName.Name 
 catNorthwind.Tables("Employees").Columns.Append colNewFirstName 
 
 ' Open Employee table in Recordset for updating 
 rstEmployees.Open "Employees", catNorthwind.ActiveConnection, _ 
 adOpenKeyset, adLockOptimistic, adCmdTable 
 
 ' Loop through the recordset displaying the contents 
 ' of the FirstName field, the field's defined size, 
 ' and its actual size. 
 ' Also restore FirstName values from aryFirstName. 
 rstEmployees.MoveFirst 
 Debug.Print " " 
 Debug.Print "New Defined Size and Actual Size" 
 i = 0 
 Do Until rstEmployees.EOF 
 rstEmployees!FirstName = aryFirstName(i) 
 Debug.Print "Employee name: " & rstEmployees!FirstName & _ 
 " " & rstEmployees!LastName 
 Debug.Print " FirstName Defined size: " _ 
 & rstEmployees!FirstName.DefinedSize 
 Debug.Print " FirstName Actual size: " & _ 
 rstEmployees!FirstName.ActualSize 
 rstEmployees.MoveNext 
 i = i + 1 
 Loop 
 rstEmployees.Close 
 
 ' Restore original FirstName column to catalog 
 catNorthwind.Tables("Employees").Columns.Delete colNewFirstName.Name 
 catNorthwind.Tables("Employees").Columns.Append colFirstName 
 
 ' Restore original FirstName values to Employees table 
 rstEmployees.Open "Employees", catNorthwind.ActiveConnection, _ 
 adOpenKeyset, adLockOptimistic, adCmdTable 
 
 rstEmployees.MoveFirst 
 i = 0 
 Do Until rstEmployees.EOF 
 rstEmployees!FirstName = aryFirstName(i) 
 rstEmployees.MoveNext 
 i = i + 1 
 Loop 
 rstEmployees.Close 
 
 'Clean up 
 Set catNorthwind = Nothing 
 Set colNewFirstName = Nothing 
 Set colFirstName = Nothing 
 Set rstEmployees = Nothing 
 Exit Sub 
 
DefinedSizeXError: 
 Set catNorthwind = Nothing 
 Set colNewFirstName = Nothing 
 Set colFirstName = Nothing 
 
 If Not rstEmployees Is Nothing Then 
 If rstEmployees.State = adStateOpen Then rstEmployees.Close 
 End If 
 Set rstEmployees = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
' EndDefinedSizeVB 
```

