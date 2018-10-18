---
<span data-ttu-id="8eb88-101"><<<<<<< ヘッド タイトル: クラスター化されたプロパティの使用例 (VB) TOCTitle: クラスター化されたプロパティの使用例 (VB) === タイトル: クラスター化されたプロパティの使用例 (VB) TOCTitle: クラスター化されたプロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="8eb88-101"><<<<<<< HEAD title: Clustered Property Example (VB) TOCTitle: Clustered Property Example (VB) ======= title: Clustered property example (VB) TOCTitle: Clustered property example (VB)</span></span>
>>>>>>> <span data-ttu-id="8eb88-102">マスターの ms:assetid: 1065622d-9473-209a-95be-c4b0ab5b687a ms:mtpsurl: https://msdn.microsoft.com/library/JJ248872(v=office.15) ms:contentKeyID: 48543293 ms.date: 2015/09/18 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="8eb88-102">master ms:assetid: 1065622d-9473-209a-95be-c4b0ab5b687a ms:mtpsurl: https://msdn.microsoft.com/library/JJ248872(v=office.15) ms:contentKeyID: 48543293 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="8eb88-103"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="8eb88-103"><<<<<<< HEAD</span></span>
# <a name="clustered-property-example-vb"></a><span data-ttu-id="8eb88-104">Clustered プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="8eb88-104">Clustered Property Example (VB)</span></span>
=======
# <a name="clustered-property-example-vb"></a><span data-ttu-id="8eb88-105">クラスター化プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="8eb88-105">Clustered property example (VB)</span></span>
>>>>>>> <span data-ttu-id="8eb88-106">master</span><span class="sxs-lookup"><span data-stu-id="8eb88-106">master</span></span>


<span data-ttu-id="8eb88-107">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="8eb88-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8eb88-108">ここでは、[Index](clustered-property-adox.md) の [Clustered](index-object-adox.md) プロパティの使用例を示します。</span><span class="sxs-lookup"><span data-stu-id="8eb88-108">This example demonstrates the [Clustered](clustered-property-adox.md) property of an [Index](index-object-adox.md).</span></span> <span data-ttu-id="8eb88-109">Microsoft Jet データベースはサポートできないというクラスター化インデックスは、次の使用例は、 *Northwind*データベース内のすべてのインデックスの**Clustered**プロパティを**False**が戻りますので注意してください。</span><span class="sxs-lookup"><span data-stu-id="8eb88-109">Note that Microsoft Jet databases do not support clustered indexes, so this example will return **False** for the **Clustered** property of all indexes in the *Northwind* database.</span></span>

```vb 
 
' BeginClusteredVB 
Sub Main() 
 On Error GoTo ClusteredXError 
 
 Dim cnn As New ADODB.Connection 
 Dim cat As New ADOX.Catalog 
 Dim tblLoop As ADOX.Table 
 Dim idxLoop As ADOX.Index 
 Dim strCnn As String 
 
 strCnn = "Provider='SQLOLEDB';Data Source='MySqlServer';Initial Catalog='pubs';" & _ 
 "Integrated Security='SSPI';" 
 ' Connect the catalog. 
 cnn.Open strCnn 
 cat.ActiveConnection = cnn 
 
 ' Enumerate Tables 
 For Each tblLoop In cat.Tables 
 'Enumerate Indexes 
 For Each idxLoop In tblLoop.Indexes 
 Debug.Print tblLoop.Name & " " & _ 
 idxLoop.Name & " " & idxLoop.Clustered 
 Next idxLoop 
 Next tblLoop 
 
 'Clean up 
 cnn.Close 
 Set cat = Nothing 
 Set cnn = Nothing 
 Exit Sub 
 
ClusteredXError: 
 
 Set cat = Nothing 
 
 If Not cnn Is Nothing Then 
 If cnn.State = adStateOpen Then cnn.Close 
 End If 
 Set cnn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndClusteredVB 
```

