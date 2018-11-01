---
title: Clustered プロパティの使用例 (VB)
TOCTitle: Clustered property example (VB)
ms:assetid: 1065622d-9473-209a-95be-c4b0ab5b687a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248872(v=office.15)
ms:contentKeyID: 48543293
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3f1ebd893418cde5b499be9d34c7d50aadff78f3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872761"
---
# <a name="clustered-property-example-vb"></a><span data-ttu-id="39b87-102">Clustered プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="39b87-102">Clustered property example (VB)</span></span>


<span data-ttu-id="39b87-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="39b87-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="39b87-104">ここでは、[Index](clustered-property-adox.md) の [Clustered](index-object-adox.md) プロパティの使用例を示します。</span><span class="sxs-lookup"><span data-stu-id="39b87-104">This example demonstrates the [Clustered](clustered-property-adox.md) property of an [Index](index-object-adox.md).</span></span> <span data-ttu-id="39b87-105">Microsoft Jet データベースはサポートできないというクラスター化インデックスは、次の使用例は、 *Northwind*データベース内のすべてのインデックスの**Clustered**プロパティを**False**が戻りますので注意してください。</span><span class="sxs-lookup"><span data-stu-id="39b87-105">Note that Microsoft Jet databases do not support clustered indexes, so this example will return **False** for the **Clustered** property of all indexes in the *Northwind* database.</span></span>

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

