---
title: GetPermissions メソッドと SetPermissions メソッドの使用例 (VB)
TOCTitle: GetPermissions and SetPermissions methods example (VB)
ms:assetid: 930d9b58-2fc8-efa9-edfe-05ef9039a74d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249649(v=office.15)
ms:contentKeyID: 48546390
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 93105c4a1705aa022d9bc9bb69fbe25943b6d50e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292273"
---
# <a name="getpermissions-and-setpermissions-methods-example-vb"></a><span data-ttu-id="9a849-102">GetPermissions メソッドと SetPermissions メソッドの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="9a849-102">GetPermissions and SetPermissions methods example (VB)</span></span>


<span data-ttu-id="9a849-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="9a849-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9a849-104">この例では、[GetPermissions](getpermissions-method-adox.md) メソッドと [SetPermissions](setpermissions-method-adox.md) メソッドの機能を示します。</span><span class="sxs-lookup"><span data-stu-id="9a849-104">This example demonstrates the [GetPermissions](getpermissions-method-adox.md) and [SetPermissions](setpermissions-method-adox.md) methods.</span></span> <span data-ttu-id="9a849-105">次のコードによって、Orders テーブルへのフル アクセス権が管理者ユーザーに与えられます。</span><span class="sxs-lookup"><span data-stu-id="9a849-105">The following code gives full access for the Orders table to the Admin user.</span></span>

```vb 
 
' BeginGrantPermissionsVB 
Sub GrantPermissions() 
 On Error GoTo GrantPermissionsError 
 
 Dim cnn As New ADODB.Connection 
 Dim cat As New ADOX.Catalog 
 Dim lngPerm As Long 
 
 ' Opens a connection to the northwind database 
 ' using the Microsoft Jet 4.0 provider 
 cnn.Provider = "Microsoft.Jet.OLEDB.4.0" 
 cnn.Open "Data Source='c:\Program Files\" & _ 
 "Microsoft Office\Office\Samples\Northwind.mdb';" & _ 
 "jet oledb:system database=" & _ 
 "'c:\Program Files\Microsoft Office\Office\system.mdw'" 
 
 Set cat.ActiveConnection = cnn 
 
 ' Retrieve original permissions 
 lngPerm = cat.Users("admin").GetPermissions("Orders", adPermObjTable) 
 Debug.Print "Original permissions: " & Str(lngPerm) 
 
 ' Revoke all permissions 
 cat.Users("admin").SetPermissions "Orders", adPermObjTable, _ 
 adAccessRevoke, adRightFull 
 
 ' Display permissions 
 Debug.Print "Revoked permissions: " & _ 
 Str(cat.Users("admin").GetPermissions("Orders", adPermObjTable)) 
 
 ' Give the Admin user full rights on the orders object 
 cat.Users("admin").SetPermissions "Orders", adPermObjTable, _ 
 adAccessSet, adRightFull 
 
 ' Display permissions 
 Debug.Print "Full permissions: " & _ 
 Str(cat.Users("admin").GetPermissions("Orders", adPermObjTable)) 
 
 ' Restore original permissions 
 cat.Users("admin").SetPermissions "Orders", adPermObjTable, _ 
 adAccessSet, lngPerm 
 
 ' Display permissions 
 Debug.Print "Final permissions: " & _ 
 Str(cat.Users("admin").GetPermissions("Orders", adPermObjTable)) 
 
 'Clean up 
 cnn.Close 
 Set cat = Nothing 
 Set cnn = Nothing 
 Exit Sub 
 
GrantPermissionsError: 
 
 Set cat = Nothing 
 
 If Not cnn Is Nothing Then 
 If cnn.State = adStateOpen Then cnn.Close 
 End If 
 Set cnn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
' EndGrantPermissionsVB 
```

