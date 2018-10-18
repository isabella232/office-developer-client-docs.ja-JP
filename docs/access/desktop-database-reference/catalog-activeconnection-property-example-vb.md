---
<<<<<<< ヘッド タイトル: カタログの ActiveConnection プロパティの使用例 (VB) TOCTitle: カタログの ActiveConnection プロパティの使用例 (VB) === タイトル: カタログの ActiveConnection プロパティの使用例 (VB) TOCTitle: カタログの ActiveConnectionプロパティの使用例 (VB)
>>>>>>> マスターの ms:assetid: 12a34091-e451-dbd1-e7f3-f794b84ee5b0 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248901(v=office.15) ms:contentKeyID: 48543348 ms.date: 2015/09/18 mtps_version: v=office.15
---

<<<<<<< ヘッド
# <a name="catalog-activeconnection-property-example-vb"></a>Catalog の ActiveConnection プロパティの使用例 (VB)
=======
# <a name="catalog-activeconnection-property-example-vb"></a>カタログの ActiveConnection プロパティの使用例 (VB)
>>>>>>> master

**適用されます**Access 2013 |。Office 2013

[ActiveConnection](activeconnection-property-adox.md) プロパティを有効に設定すると、開いている接続によってカタログが開かれます。開いたカタログから、そのカタログに含まれるスキーマ オブジェクトにアクセスできます。

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

**ActiveConnection** プロパティを有効な接続文字列に設定した場合も、カタログを開くことができます。

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
