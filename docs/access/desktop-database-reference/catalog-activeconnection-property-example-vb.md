---
<span data-ttu-id="20f83-101"><<<<<<< ヘッド タイトル: カタログの ActiveConnection プロパティの使用例 (VB) TOCTitle: カタログの ActiveConnection プロパティの使用例 (VB) === タイトル: カタログの ActiveConnection プロパティの使用例 (VB) TOCTitle: カタログの ActiveConnectionプロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="20f83-101"><<<<<<< HEAD title: Catalog ActiveConnection Property Example (VB) TOCTitle: Catalog ActiveConnection Property Example (VB) ======= title: Catalog ActiveConnection property example (VB) TOCTitle: Catalog ActiveConnection property example (VB)</span></span>
>>>>>>> <span data-ttu-id="20f83-102">マスターの ms:assetid: 12a34091-e451-dbd1-e7f3-f794b84ee5b0 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248901(v=office.15) ms:contentKeyID: 48543348 ms.date: 2015/09/18 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="20f83-102">master ms:assetid: 12a34091-e451-dbd1-e7f3-f794b84ee5b0 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248901(v=office.15) ms:contentKeyID: 48543348 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="20f83-103"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="20f83-103"><<<<<<< HEAD</span></span>
# <a name="catalog-activeconnection-property-example-vb"></a><span data-ttu-id="20f83-104">Catalog の ActiveConnection プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="20f83-104">Catalog ActiveConnection Property Example (VB)</span></span>
=======
# <a name="catalog-activeconnection-property-example-vb"></a><span data-ttu-id="20f83-105">カタログの ActiveConnection プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="20f83-105">Catalog ActiveConnection property example (VB)</span></span>
>>>>>>> <span data-ttu-id="20f83-106">master</span><span class="sxs-lookup"><span data-stu-id="20f83-106">master</span></span>

<span data-ttu-id="20f83-107">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="20f83-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="20f83-p101">[ActiveConnection](activeconnection-property-adox.md) プロパティを有効に設定すると、開いている接続によってカタログが開かれます。開いたカタログから、そのカタログに含まれるスキーマ オブジェクトにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="20f83-p101">Setting the [ActiveConnection](activeconnection-property-adox.md) property to a valid, open connection "opens" the catalog. From an open catalog, you can access the schema objects contained within that catalog.</span></span>

```vb 
 
    ' BeginOpenConnectionVB 
    Sub OpenConnection() 
    On Error GoTo OpenConnectionError 
    
    Dim cnn As New ADODB.Connection 
    Dim cat As New ADOX.Catalog 
    
    cnn.Open "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
    "Data Source= 'c:\Program Files\Microsoft Office\" & _ 
    "Office\Samples\Northwind.mdb';" 
    Set cat.ActiveConnection = cnn 
    Debug.Print cat.Tables(0).Type 
    
    'Clean up 
    cnn.Close 
    Set cat = Nothing 
    Set cnn = Nothing 
    Exit Sub 
    
    OpenConnectionError: 
    
    Set cat = Nothing 
    
    If Not cnn Is Nothing Then 
    If cnn.State = adStateOpen Then cnn.Close 
    End If 
    Set cnn = Nothing 
    
    If Err <> 0 Then 
    MsgBox Err.Source & "-->" & Err.Description, , "Error" 
    End If 
    End Sub 
    ' EndOpenConnectionVB 
```

<span data-ttu-id="20f83-110">**ActiveConnection** プロパティを有効な接続文字列に設定した場合も、カタログを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="20f83-110">Setting the **ActiveConnection** property to a valid connection string also "opens" the catalog.</span></span>

```vb
    ' BeginOpenConnection2VB 
    Sub Main() 
     On Error GoTo OpenConnectionWithStringError 
     Dim cat As New ADOX.Catalog 
     
     cat.ActiveConnection = "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
     "Data Source='c:\Program Files\Microsoft Office\" & _ 
     "Office\Samples\Northwind.mdb';" 
     Debug.Print cat.Tables(0).Type 
     
     'Clean up 
     Set cat.ActiveConnection = Nothing 
     Exit Sub 
     
    OpenConnectionWithStringError: 
     Set cat = Nothing 
     
     If Err <> 0 Then 
     MsgBox Err.Source & "-->" & Err.Description, , "Error" 
     End If 
    End Sub 
    ' EndOpenConnection2VB
```
