---
<<<<<<< ヘッド タイトル: 接続の終了方法、テーブルの種類プロパティの使用例 (VB) TOCTitle: 接続の終了メソッドは、テーブルの種類プロパティの使用例 (VB) === タイトル: 接続の Close メソッドをテーブル型のプロパティの使用例 (VB) TOCTitle:接続の Close メソッドをテーブル型のプロパティの使用例 (VB)
>>>>>>> マスターの ms:assetid: cd0bb6ad-af7b-fb9c-d45c-5d4b62459c03 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250019(v=office.15) ms:contentKeyID: 48547754 ms.date: 2015/09/18 mtps_version: v=office.15
---

<<<<<<< ヘッド
# <a name="connection-close-method-table-type-property-example-vb"></a>Connection の Close メソッドおよび Table の Type プロパティの使用例 (VB)
=======
# <a name="connection-close-method-table-type-property-example-vb"></a>接続の Close メソッドをテーブル型のプロパティの使用例 (VB)
>>>>>>> master

**適用されます**Access 2013 |。Office 2013

[ActiveConnection](activeconnection-property-adox.md) プロパティを **Nothing** に設定すると、カタログが閉じます。関連付けられたコレクションは、空になります。カタログのスキーマ オブジェクトから作成されたオブジェクトは、すべて孤立化します。キャッシュされたオブジェクトのプロパティはいずれも使用できますが、プロバイダーの呼び出しが必要なプロパティを取得しようとすると失敗します。

```vb 
 
    ' BeginCloseConnectionVB 
    Sub Main() 
    On Error GoTo CloseConnectionByNothingError 
    
    Dim cnn As New ADODB.Connection 
    Dim cat As New ADOX.Catalog 
    Dim tbl As ADOX.Table 
    
    cnn.Open "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
    "Data Source= 'c:\Program Files\Microsoft Office\" & _ 
    "Office\Samples\Northwind.mdb';" 
    Set cat.ActiveConnection = cnn 
    Set tbl = cat.Tables(0) 
    Debug.Print tbl.Type ' Cache tbl.Type info 
    Set cat.ActiveConnection = Nothing 
    Debug.Print tbl.Type ' tbl is orphaned 
    ' Previous line will succeed if this was cached 
    Debug.Print tbl.Columns(0).DefinedSize 
    ' Previous line will fail if this info has not been cached 
    
    'Clean up 
    cnn.Close 
    Set cat = Nothing 
    Set cnn = Nothing 
    Exit Sub 
    
    CloseConnectionByNothingError: 
    Set cat = Nothing 
    
    If Not cnn Is Nothing Then 
    If cnn.State = adStateOpen Then cnn.Close 
    End If 
    Set cnn = Nothing 
    
    If Err <> 0 Then 
    MsgBox Err.Source & "-->" & Err.Description, , "Error" 
    End If 
    End Sub 
    ' EndCloseConnectionVB 
```

<br/>

カタログを開くために使用した [Connection](connection-object-ado.md) オブジェクトを閉じると、 **ActiveConnection** プロパティを **Nothing** に設定した場合と同じように、カタログが閉じます。

```vb
    Sub CloseConnection() 
     On Error GoTo CloseConnectionError 
     
     Dim cnn As New ADODB.Connection 
     Dim cat As New ADOX.Catalog 
     Dim tbl As ADOX.Table 
     
     cnn.Open "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
     "Data Source= 'c:\Program Files\Microsoft Office\" & _ 
     "Office\Samples\Northwind.mdb';" 
     Set cat.ActiveConnection = cnn 
     Set tbl = cat.Tables(0) 
     Debug.Print tbl.Type ' Cache tbl.Type info 
     cnn.Close 
     Debug.Print tbl.Type ' tbl is orphaned 
     ' Previous line will succeed if this was cached 
     Debug.Print tbl.Columns(0).DefinedSize 
     ' Previous line will fail if this info has not been cached 
     
     'Clean up 
     Set cat = Nothing 
     Set cnn = Nothing 
     Exit Sub 
     
    CloseConnectionError: 
     
     Set cat = Nothing 
     
     If Not cnn Is Nothing Then 
     If cnn.State = adStateOpen Then cnn.Close 
     End If 
     Set cnn = Nothing 
     
     If Err <> 0 Then 
     MsgBox Err.Source & "-->" & Err.Description, , "Error" 
     End If 
    End Sub 
    ' EndCloseConnection2VB
```
