---
title: キーの追加方法、キーの種類、RelatedColumn プロパティの使用例 (VB)
TOCTitle: Keys Append Method, Key Type, RelatedColumn, RelatedTable and UpdateRule properties example (VB)
ms:assetid: d1b0508d-ab2c-eece-061c-09c67ea9ecae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250047(v=office.15)
ms:contentKeyID: 48547871
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9120fa718544a0d1d7a132b197517aac955f5fc6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721102"
---
# <a name="keys-append-method-key-type-relatedcolumn-relatedtable-and-updaterule-properties-example-vb"></a><span data-ttu-id="3ac0a-102">キーの追加方法、キーの種類、RelatedColumn、RelatedTable、UpdateRule プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="3ac0a-102">Keys Append Method, Key Type, RelatedColumn, RelatedTable and UpdateRule properties example (VB)</span></span>


<span data-ttu-id="3ac0a-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="3ac0a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3ac0a-104">次のコードでは、新しい外部キーの作成方法を示します。</span><span class="sxs-lookup"><span data-stu-id="3ac0a-104">The following code demonstrates how to create a new foreign key.</span></span> <span data-ttu-id="3ac0a-105">2 つのテーブル (**Customers**と**Orders**) が存在すると仮定します。</span><span class="sxs-lookup"><span data-stu-id="3ac0a-105">It assumes two tables (**Customers** and **Orders**) exist.</span></span>

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

