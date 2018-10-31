---
title: GetObjectOwner メソッドと SetObjectOwner メソッドの使用例 (VB)
TOCTitle: GetObjectOwner and SetObjectOwner methods example (VB)
ms:assetid: 0a30cce1-7626-8db3-4af4-84098c284db0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248833(v=office.15)
ms:contentKeyID: 48543146
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e1e79e57cc88e85c9533201ca791fba13c9e3c65
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862927"
---
# <a name="getobjectowner-and-setobjectowner-methods-example-vb"></a><span data-ttu-id="d0067-102">GetObjectOwner メソッドと SetObjectOwner メソッドの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="d0067-102">GetObjectOwner and SetObjectOwner methods example (VB)</span></span>


<span data-ttu-id="d0067-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="d0067-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d0067-104">この例では、[GetObjectOwner](getobjectowner-method-adox.md) メソッドと [SetObjectOwner](https://msdn.microsoft.com/library/jj249006\(v=office.15\)) メソッドの機能を示します。</span><span class="sxs-lookup"><span data-stu-id="d0067-104">This example demonstrates the [GetObjectOwner](getobjectowner-method-adox.md) and [SetObjectOwner](https://msdn.microsoft.com/library/jj249006\(v=office.15\)) methods.</span></span> <span data-ttu-id="d0067-105">このコード グループの存在を前提としています (参照[グループおよびユーザーの追加、パスワードの変更方法の例 (VB)](groups-and-users-append-changepassword-methods-example-vb.md)をこのグループをシステムに追加する方法を参照してください) の会計です。</span><span class="sxs-lookup"><span data-stu-id="d0067-105">This code assumes the existence of the group Accounting (see the [Groups and Users Append, ChangePassword methods example (VB)](groups-and-users-append-changepassword-methods-example-vb.md) to see how to add this group to the system).</span></span> <span data-ttu-id="d0067-106">Categories テーブルの所有者は Accounting に設定されます。</span><span class="sxs-lookup"><span data-stu-id="d0067-106">The owner of the Categories table is set to Accounting.</span></span>

```vb 
 
' BeginOwnersVB 
Sub Main() 
 On Error GoTo OwnersXError 
 
 Dim tblLoop As New ADOX.Table 
 Dim cat As New ADOX.Catalog 
 Dim strOwner As String 
 
 ' Open the Catalog. 
 cat.ActiveConnection = "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\" & _ 
 "Microsoft Office\Office\Samples\Northwind.mdb';" & _ 
 "jet oledb:system database=" & _ 
 "'c:\Program Files\Microsoft Office\Office\system.mdw'" 
 
 ' Print the original owner of Categories 
 strOwner = cat.GetObjectOwner("Categories", adPermObjTable) 
 Debug.Print "Owner of Categories: " & strOwner 
 
 ' Set the owner of Categories to Accounting 
 cat.SetObjectOwner "Categories", adPermObjTable, "Accounting" 
 
 ' List the owners of all tables and columns in the catalog. 
 For Each tblLoop In cat.Tables 
 Debug.Print "Table: " & tblLoop.Name 
 Debug.Print " Owner: " & _ 
 cat.GetObjectOwner(tblLoop.Name, adPermObjTable) 
 Next tblLoop 
 
 ' Restore the original owner of Categories 
 cat.SetObjectOwner "Categories", adPermObjTable, strOwner 
 
 'Clean up 
 Set cat.ActiveConnection = Nothing 
 Set cat = Nothing 
 Exit Sub 
 
OwnersXError: 
 
 Set cat = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
' EndOwnersVB 
```

