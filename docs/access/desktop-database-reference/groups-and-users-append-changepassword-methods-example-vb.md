---
title: Groups と Users の Append メソッドおよび ChangePassword メソッドの使用例 (VB)
TOCTitle: Groups and Users Append, ChangePassword methods example (VB)
ms:assetid: e9ae5f1c-d1fa-ab58-c889-b4e197cecf4c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250183(v=office.15)
ms:contentKeyID: 48548445
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a1801dafe83ed2fc0752ef189c41e70318ef690f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718281"
---
# <a name="groups-and-users-append-changepassword-methods-example-vb"></a>Groups と Users の Append メソッドおよび ChangePassword メソッドの使用例 (VB)


**適用されます**Access 2013、Office 2013。

この例では、新しい [Group](group-object-adox.md) および新しい [User](user-object-adox.md) をシステムに追加することによって、[Groups](groups-collection-adox.md) の [Append](append-method-adox-groups.md) メソッドと [Users](users-collection-adox.md) の [Append](append-method-adox-users.md) メソッドの機能を示します。新しい **Group** は、新しい **User** の ** Groups** コレクションに追加されます。したがって、新しい **User** が **Group** に追加されます。また、[ChangePassword](changepassword-method-adox.md) メソッドは、**User** のパスワードを指定するために使用されます。

```vb 
 
' BeginGroupVB 
Sub Main() 
 On Error GoTo GroupXError 
 
 Dim cat As ADOX.Catalog 
 Dim usrNew As ADOX.User 
 Dim usrLoop As ADOX.User 
 Dim grpLoop As ADOX.Group 
 
 Set cat = New ADOX.Catalog 
 
 cat.ActiveConnection = "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\" & _ 
 "Microsoft Office\Office\Samples\Northwind.mdb';" & _ 
 "jet oledb:system database=" & _ 
 "'c:\Program Files\Microsoft Office\Office\system.mdw'" 
 
 With cat 
 'Create and append new group with a string. 
 .Groups.Append "Accounting" 
 
 ' Create and append new user with an object. 
 Set usrNew = New ADOX.User 
 usrNew.Name = "Pat Smith" 
 usrNew.ChangePassword "", "Password1" 
 .Users.Append usrNew 
 
 ' Make the user Pat Smith a member of the 
 ' Accounting group by creating and adding the 
 ' appropriate Group object to the user's Groups 
 ' collection. The same is accomplished if a User 
 ' object representing Pat Smith is created and 
 ' appended to the Accounting group Users collection 
 usrNew.Groups.Append "Accounting" 
 
 ' Enumerate all User objects in the 
 ' catalog's Users collection. 
 For Each usrLoop In .Users 
 Debug.Print " " & usrLoop.Name 
 Debug.Print " Belongs to these groups:" 
 ' Enumerate all Group objects in each User 
 ' object's Groups collection. 
 If usrLoop.Groups.Count <> 0 Then 
 For Each grpLoop In usrLoop.Groups 
 Debug.Print " " & grpLoop.Name 
 Next grpLoop 
 Else 
 Debug.Print " [None]" 
 End If 
 Next usrLoop 
 
 ' Enumerate all Group objects in the default 
 ' workspace's Groups collection. 
 For Each grpLoop In .Groups 
 Debug.Print " " & grpLoop.Name 
 Debug.Print " Has as its members:" 
 ' Enumerate all User objects in each Group 
 ' object's Users collection. 
 If grpLoop.Users.Count <> 0 Then 
 For Each usrLoop In grpLoop.Users 
 Debug.Print " " & usrLoop.Name 
 Next usrLoop 
 Else 
 Debug.Print " [None]" 
 End If 
 Next grpLoop 
 
 ' Delete new User and Group objects because this 
 ' is only a demonstration. 
 ' These two line are commented out because the sub "OwnersX" uses 
 ' the group "Accounting". 
' .Users.Delete "Pat Smith" 
' .Groups.Delete "Accounting" 
 
 End With 
 
 'Clean up 
 Set cat.ActiveConnection = Nothing 
 Set cat = Nothing 
 Set usrNew = Nothing 
 Exit Sub 
 
GroupXError: 
 
 Set cat = Nothing 
 Set usrNew = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndGroupVB 
```

