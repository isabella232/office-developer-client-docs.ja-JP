---
<span data-ttu-id="9c652-101"><<<<<<< ヘッド タイトル: キーの追加方法、キーの種類、RelatedColumn プロパティの使用例 (VB) TOCTitle: キーの追加方法、キーの種類、RelatedColumn、RelatedTable、UpdateRule プロパティの使用例 (VB) === タイトル: キーの追加のメソッドは、キー型、RelatedColumn プロパティの使用例 (VB) TOCTitle: キーの追加方法、キーの種類、RelatedColumn、RelatedTable、UpdateRule プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9c652-101"><<<<<<< HEAD title: Keys Append Method, Key Type, RelatedColumn Properties Example (VB) TOCTitle: Keys Append Method, Key Type, RelatedColumn, RelatedTable and UpdateRule Properties Example (VB) ======= title: Keys Append Method, Key Type, RelatedColumn properties example (VB) TOCTitle: Keys Append Method, Key Type, RelatedColumn, RelatedTable and UpdateRule properties example (VB)</span></span>
>>>>>>> <span data-ttu-id="9c652-102">マスターの ms:assetid: d1b0508d-ab2c-eece-061c-09c67ea9ecae ms:mtpsurl: https://msdn.microsoft.com/library/JJ250047(v=office.15) ms:contentKeyID: 48547871 ms.date: 2015/09/18 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="9c652-102">master ms:assetid: d1b0508d-ab2c-eece-061c-09c67ea9ecae ms:mtpsurl: https://msdn.microsoft.com/library/JJ250047(v=office.15) ms:contentKeyID: 48547871 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="9c652-103"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="9c652-103"><<<<<<< HEAD</span></span>
# <a name="keys-append-method-key-type-relatedcolumn-relatedtable-and-updaterule-properties-example-vb"></a><span data-ttu-id="9c652-104">Keys の Append メソッド、および Key の Type、RelatedColumn、RelatedTable、UpdateRule プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9c652-104">Keys Append Method, Key Type, RelatedColumn, RelatedTable and UpdateRule Properties Example (VB)</span></span>
=======
# <a name="keys-append-method-key-type-relatedcolumn-relatedtable-and-updaterule-properties-example-vb"></a><span data-ttu-id="9c652-105">キーの追加方法、キーの種類、RelatedColumn、RelatedTable、UpdateRule プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9c652-105">Keys Append Method, Key Type, RelatedColumn, RelatedTable and UpdateRule properties example (VB)</span></span>
>>>>>>> <span data-ttu-id="9c652-106">master</span><span class="sxs-lookup"><span data-stu-id="9c652-106">master</span></span>


<span data-ttu-id="9c652-107">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="9c652-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9c652-108">次のコードでは、新しい外部キーの作成方法を示します。</span><span class="sxs-lookup"><span data-stu-id="9c652-108">The following code demonstrates how to create a new foreign key.</span></span> <span data-ttu-id="9c652-109">2 つのテーブル (**Customers**と**Orders**) が存在すると仮定します。</span><span class="sxs-lookup"><span data-stu-id="9c652-109">It assumes two tables (**Customers** and **Orders**) exist.</span></span>

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

