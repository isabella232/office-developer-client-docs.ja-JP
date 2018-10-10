---
title: Connection の Close メソッドおよび Table の Type プロパティの使用例 (VB)
TOCTitle: Connection Close Method, Table Type Property Example (VB)
ms:assetid: cd0bb6ad-af7b-fb9c-d45c-5d4b62459c03
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250019(v=office.15)
ms:contentKeyID: 48547754
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b0a7cb6f2f2e78727c8e4a383a901d4712916fee
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476713"
---
# <a name="connection-close-method-table-type-property-example-vb"></a><span data-ttu-id="b0048-102">Connection の Close メソッドおよび Table の Type プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="b0048-102">Connection Close Method, Table Type Property Example (VB)</span></span>

<span data-ttu-id="b0048-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="b0048-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b0048-p101">[ActiveConnection](activeconnection-property-adox.md) プロパティを **Nothing** に設定すると、カタログが閉じます。関連付けられたコレクションは、空になります。カタログのスキーマ オブジェクトから作成されたオブジェクトは、すべて孤立化します。キャッシュされたオブジェクトのプロパティはいずれも使用できますが、プロバイダーの呼び出しが必要なプロパティを取得しようとすると失敗します。</span><span class="sxs-lookup"><span data-stu-id="b0048-p101">Setting the [ActiveConnection](activeconnection-property-adox.md) property to **Nothing** should "close" the catalog. Associated collections will be empty. Any objects that were created from schema objects in the catalog will be orphaned. Any properties on those objects that have been cached will still be available, but attempting to read properties that require a call to the provider will fail.</span></span>

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

<span data-ttu-id="b0048-108">カタログを開くために使用した [Connection](connection-object-ado.md) オブジェクトを閉じると、 **ActiveConnection** プロパティを **Nothing** に設定した場合と同じように、カタログが閉じます。</span><span class="sxs-lookup"><span data-stu-id="b0048-108">Closing a [Connection](connection-object-ado.md) object that was used to "open" the catalog should have the same effect as setting the **ActiveConnection** property to **Nothing**.</span></span>

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
