---
title: Views の Refresh メソッドの使用例 (VB)
TOCTitle: Views Refresh method example (VB)
ms:assetid: 607b78d6-1b26-d643-9f97-f47b5f5cffc5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249352(v=office.15)
ms:contentKeyID: 48545182
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 953e12d808c5023e7f0c3d20d46be47ab44ad901
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863417"
---
# <a name="views-refresh-method-example-vb"></a><span data-ttu-id="2d2d4-102">Views の Refresh メソッドの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="2d2d4-102">Views Refresh method example (VB)</span></span>


<span data-ttu-id="2d2d4-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="2d2d4-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2d2d4-p101">次のコードでは、[Catalog](views-collection-adox.md) の [Views](catalog-object-adox.md) コレクションを更新する方法を示します。この処理は、 [Catalog](view-object-adox.md) の **View** オブジェクトにアクセスする前に行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="2d2d4-p101">The following code shows how to refresh the [Views](views-collection-adox.md) collection of a [Catalog](catalog-object-adox.md). This is required before [View](view-object-adox.md) objects from the **Catalog** can be accessed.</span></span>

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

