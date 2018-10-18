---
<<<<<<< ヘッド タイトル: キーの追加方法、キーの種類、RelatedColumn プロパティの使用例 (VB) TOCTitle: キーの追加方法、キーの種類、RelatedColumn、RelatedTable、UpdateRule プロパティの使用例 (VB) === タイトル: キーの追加のメソッドは、キー型、RelatedColumn プロパティの使用例 (VB) TOCTitle: キーの追加方法、キーの種類、RelatedColumn、RelatedTable、UpdateRule プロパティの使用例 (VB)
>>>>>>> マスターの ms:assetid: d1b0508d-ab2c-eece-061c-09c67ea9ecae ms:mtpsurl: https://msdn.microsoft.com/library/JJ250047(v=office.15) ms:contentKeyID: 48547871 ms.date: 2015/09/18 mtps_version: v=office.15
---

<<<<<<< ヘッド
# <a name="keys-append-method-key-type-relatedcolumn-relatedtable-and-updaterule-properties-example-vb"></a>Keys の Append メソッド、および Key の Type、RelatedColumn、RelatedTable、UpdateRule プロパティの使用例 (VB)
=======
# <a name="keys-append-method-key-type-relatedcolumn-relatedtable-and-updaterule-properties-example-vb"></a>キーの追加方法、キーの種類、RelatedColumn、RelatedTable、UpdateRule プロパティの使用例 (VB)
>>>>>>> master


**適用されます**Access 2013 |。Office 2013

次のコードでは、新しい外部キーの作成方法を示します。 2 つのテーブル (**Customers**と**Orders**) が存在すると仮定します。

```vb 
 
' BeginCreateKeyVB 
Sub Main() 
 On Error GoTo CreateKeyError 
 
 Dim kyForeign As New ADOX.Key 
 Dim cat As New ADOX.Catalog 
 
 ' Connect the catalog 
 cat.ActiveConnection = "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\Microsoft Office\" & _ 
 "Office\Samples\Northwind.mdb';" 
 
 ' Define the foreign key 
 kyForeign.Name = "CustOrder" 
 kyForeign.Type = adKeyForeign 
 kyForeign.RelatedTable = "Customers" 
 kyForeign.Columns.Append "CustomerId" 
 kyForeign.Columns("CustomerId").RelatedColumn = "CustomerId" 
 kyForeign.UpdateRule = adRICascade 
 
 ' Append the foreign key 
 cat.Tables("Orders").Keys.Append kyForeign 
 
 'Delete the Key as this is a demonstration 
 cat.Tables("Orders").Keys.Delete kyForeign.Name 
 
 'Clean up 
 Set cat.ActiveConnection = Nothing 
 Set cat = Nothing 
 Set kyForeign = Nothing 
 Exit Sub 
 
CreateKeyError: 
 Set cat = Nothing 
 Set kyForeign = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
' EndCreateKeyVB 
```

