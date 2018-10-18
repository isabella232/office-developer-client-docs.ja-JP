---
<span data-ttu-id="6eba5-101"><<<<<<< ヘッド タイトル: 列とテーブルの追加方法、名前プロパティの使用例 (VB) TOCTitle: 列とテーブルの追加方法、名前プロパティの使用例 (VB) === タイトル: 列とテーブルの追加方法、名前プロパティの使用例 (VB)TOCTitle: 列とテーブルの追加方法、名前プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="6eba5-101"><<<<<<< HEAD title: Columns and Tables Append Methods, Name Property Example (VB) TOCTitle: Columns and Tables Append Methods, Name Property Example (VB) ======= title: Columns and Tables Append Methods, Name property example (VB) TOCTitle: Columns and Tables Append Methods, Name property example (VB)</span></span>
>>>>>>> <span data-ttu-id="6eba5-102">マスターの ms:assetid: 39458400-f30c-0636-19f2-c2c2788a6534 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249140(v=office.15) ms:contentKeyID: 48544238 ms.date: 2015/09/18 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="6eba5-102">master ms:assetid: 39458400-f30c-0636-19f2-c2c2788a6534 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249140(v=office.15) ms:contentKeyID: 48544238 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="6eba5-103"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="6eba5-103"><<<<<<< HEAD</span></span>
# <a name="columns-and-tables-append-methods-name-property-example-vb"></a><span data-ttu-id="6eba5-104">列とテーブルの Append メソッドと Name プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="6eba5-104">Columns and Tables Append Methods, Name Property Example (VB)</span></span>
=======
# <a name="columns-and-tables-append-methods-name-property-example-vb"></a><span data-ttu-id="6eba5-105">列とテーブルの追加方法、名前プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="6eba5-105">Columns and Tables Append Methods, Name property example (VB)</span></span>
>>>>>>> <span data-ttu-id="6eba5-106">master</span><span class="sxs-lookup"><span data-stu-id="6eba5-106">master</span></span>


<span data-ttu-id="6eba5-107">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="6eba5-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6eba5-108">次のコードでは、新しいテーブルの作成方法を示します。</span><span class="sxs-lookup"><span data-stu-id="6eba5-108">The following code demonstrates how to create a new table.</span></span>

```vb 
 
' BeginCreateTableVB 
Sub Main() 
 On Error GoTo CreateTableError 
 
 Dim tbl As New Table 
 Dim cat As New ADOX.Catalog 
 
 ' Open the Catalog. 
 cat.ActiveConnection = "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\Microsoft Office\" & _ 
 "Office\Samples\Northwind.mdb';" 
 
 tbl.Name = "MyTable" 
 tbl.Columns.Append "Column1", adInteger 
 tbl.Columns.Append "Column2", adInteger 
 tbl.Columns.Append "Column3", adVarWChar, 50 
 cat.Tables.Append tbl 
 Debug.Print "Table 'MyTable' is added." 
 
 'Delete the table as this is a demonstration. 
 cat.Tables.Delete tbl.Name 
 Debug.Print "Table 'MyTable' is deleted." 
 
 'Clean up 
 Set cat.ActiveConnection = Nothing 
 Set cat = Nothing 
 Set tbl = Nothing 
 Exit Sub 
 
CreateTableError: 
 
 Set cat = Nothing 
 Set tbl = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndCreateTableVB 
```

