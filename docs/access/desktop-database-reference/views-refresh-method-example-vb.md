---
title: Views の Refresh メソッドの使用例 (VB)
TOCTitle: Views Refresh Method Example (VB)
ms:assetid: 607b78d6-1b26-d643-9f97-f47b5f5cffc5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249352(v=office.15)
ms:contentKeyID: 48545182
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cb00909a10b5ab8d65a3f52c9218479d21c01a38
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476493"
---
# <a name="views-refresh-method-example-vb"></a><span data-ttu-id="274ec-102">Views の Refresh メソッドの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="274ec-102">Views Refresh Method Example (VB)</span></span>


<span data-ttu-id="274ec-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="274ec-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="274ec-p101">次のコードでは、[Catalog](views-collection-adox.md) の [Views](catalog-object-adox.md) コレクションを更新する方法を示します。この処理は、 [Catalog](view-object-adox.md) の **View** オブジェクトにアクセスする前に行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="274ec-p101">The following code shows how to refresh the [Views](views-collection-adox.md) collection of a [Catalog](catalog-object-adox.md). This is required before [View](view-object-adox.md) objects from the **Catalog** can be accessed.</span></span>

```vb 
 
' BeginViewsRefreshVB 
Sub Main() 
 On Error GoTo ProcedureViewsRefreshError 
 
 Dim cat As New ADOX.Catalog 
 
 ' Open the Catalog 
 cat.ActiveConnection = "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\" & _ 
 "Microsoft Office\Office\Samples\Northwind.mdb';" 
 
 ' Refresh the Procedures collection 
 cat.Views.Refresh 
 
 'Clean up 
 Set cat = Nothing 
 Exit Sub 
 
ProcedureViewsRefreshError: 
 
 If Not cat Is Nothing Then 
 Set cat = Nothing 
 End If 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndViewsRefreshVB 
```
