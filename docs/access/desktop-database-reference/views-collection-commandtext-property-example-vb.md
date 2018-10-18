---
<span data-ttu-id="36b0d-101"><<<<<<< ヘッド タイトル: ビューのコレクション、CommandText プロパティの使用例 (VB) TOCTitle: ビューのコレクション、CommandText プロパティの使用例 (VB) === タイトル: Views コレクションでは、CommandText プロパティの使用例 (VB) TOCTitle: ビューのコレクションCommandText プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="36b0d-101"><<<<<<< HEAD title: Views Collection, CommandText Property Example (VB) TOCTitle: Views Collection, CommandText Property Example (VB) ======= title: Views Collection, CommandText property example (VB) TOCTitle: Views Collection, CommandText property example (VB)</span></span>
>>>>>>> <span data-ttu-id="36b0d-102">マスターの ms:assetid: 5dacd3c2-a1b2-57a7-1bac-ce0caa7c1a09 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249331(v=office.15) ms:contentKeyID: 48545120 ms.date: 2015/09/18 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="36b0d-102">master ms:assetid: 5dacd3c2-a1b2-57a7-1bac-ce0caa7c1a09 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249331(v=office.15) ms:contentKeyID: 48545120 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="36b0d-103"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="36b0d-103"><<<<<<< HEAD</span></span>
# <a name="views-collection-commandtext-property-example-vb"></a><span data-ttu-id="36b0d-104">Views コレクションと CommandText プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="36b0d-104">Views Collection, CommandText Property Example (VB)</span></span>
=======
# <a name="views-collection-commandtext-property-example-vb"></a><span data-ttu-id="36b0d-105">Views コレクションでは、CommandText プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="36b0d-105">Views Collection, CommandText property example (VB)</span></span>
>>>>>>> <span data-ttu-id="36b0d-106">master</span><span class="sxs-lookup"><span data-stu-id="36b0d-106">master</span></span>


<span data-ttu-id="36b0d-107">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="36b0d-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="36b0d-108">次のコードでは、ビューのテキストを更新するための、[Command](command-property-adox.md) プロパティの使用方法を示します。</span><span class="sxs-lookup"><span data-stu-id="36b0d-108">The following code demonstrates how to use the [Command](command-property-adox.md) property to update the text of a view.</span></span>

```vb 
 
' BeginViewsCollectionVB 
Sub Main() 
 On Error GoTo ViewTextError 
 
 Dim cnn As New ADODB.Connection 
 Dim cat As New ADOX.Catalog 
 Dim cmd As New ADODB.Command 
 
 ' Open the Connection 
 cnn.Open _ 
 "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\Microsoft Office\" & _ 
 "Office\Samples\Northwind.mdb';" 
 
 ' Open the catalog 
 Set cat.ActiveConnection = cnn 
 
 ' Get the command 
 Set cmd = cat.Views("AllCustomers").Command 
 
 ' Update the CommandText of the Command 
 cmd.CommandText = _ 
 "Select CustomerId, CompanyName, ContactName From Customers" 
 
 ' Update the View 
 Set cat.Views("AllCustomers").Command = cmd 
 
 'Clean up 
 cnn.Close 
 Set cat = Nothing 
 Set cmd = Nothing 
 Set cnn = Nothing 
 Exit Sub 
 
ViewTextError: 
 
 Set cat = Nothing 
 Set cmd = Nothing 
 
 If Not cnn Is Nothing Then 
 If cnn.State = adStateOpen Then cnn.Close 
 End If 
 Set cnn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndViewsCollectionVB 
```

