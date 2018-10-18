---
<<<<<<< ヘッド タイトル: パラメーターのコレクション、コマンド プロパティの使用例 (VB) TOCTitle: パラメーターのコレクション、コマンド プロパティの使用例 (VB) === タイトル: Parameters コレクションのコマンド プロパティの使用例 (VB) TOCTitle: パラメーターコレクション、コマンド プロパティの使用例 (VB)
>>>>>>> マスターの ms:assetid: 3bb3e6e1-0ee5-70bb-7f2c-beb461d3914a ms:mtpsurl: https://msdn.microsoft.com/library/JJ249151(v=office.15) ms:contentKeyID: 48544290 ms.date: 2015/09/18 mtps_version: v=office.15
---

<<<<<<< ヘッド
# <a name="parameters-collection-command-property-example-vb"></a>Parameters コレクションの Command プロパティの使用例 (VB)
=======
# <a name="parameters-collection-command-property-example-vb"></a>Parameters コレクションのコマンド プロパティの使用例 (VB)
>>>>>>> master


**適用されます**Access 2013 |。Office 2013

次のコードでは、プロシージャのパラメーター情報を取得するために [Command](command-property-adox.md) オブジェクトの [Command](command-object-ado.md) プロパティを使用する方法を示します。

```vb 
 
' BeginParametersVB 
Sub Main() 
 On Error GoTo ProcedureParametersError 
 
 Dim cnn As New ADODB.Connection 
 Dim cmd As ADODB.Command 
 Dim prm As ADODB.Parameter 
 Dim cat As New ADOX.Catalog 
 
 ' Open the Connection 
 cnn.Open _ 
 "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\Microsoft Office\" & _ 
 "Office\Samples\Northwind.mdb';" 
 
 ' Open the catalog 
 Set cat.ActiveConnection = cnn 
 
 ' Get the command object 
 Set cmd = cat.Procedures("CustomerById").Command 
 
 ' Retrieve Parameter information 
 cmd.Parameters.Refresh 
 For Each prm In cmd.Parameters 
 Debug.Print prm.Name & ":" & prm.Type 
 Next 
 
 'Clean up 
 cnn.Close 
 Set cat = Nothing 
 Set cmd = Nothing 
 Set cnn = Nothing 
 Exit Sub 
 
ProcedureParametersError: 
 
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
' EndParametersVB 
```

