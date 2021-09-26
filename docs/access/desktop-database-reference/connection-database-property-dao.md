---
title: Connection.Database プロパティ (DAO)
TOCTitle: Database Property
ms:assetid: cf871353-0ea4-f995-6e0e-812af443daf9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834675(v=office.15)
ms:contentKeyID: 48547809
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053581
f1_categories:
- Office.Version=v15
ms.localizationpriority: high
ms.openlocfilehash: eaca7976e417d61ef8d70f0d60aa2438f89072ad
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586041"
---
# <a name="connectiondatabase-property-dao"></a>Connection.Database プロパティ (DAO)


**適用先**: Access 2013、Office 2013



## <a name="syntax"></a>構文

*式* . Database

*式***Connection** オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

**[Connection](connection-object-dao.md)** オブジェクトで、**Database** プロパティを使用して、**Connection** オブジェクトに対応する **Database** オブジェクトへの参照を取得します。DAO では、**Connection** オブジェクトとそれに対応する **Database** オブジェクトは、同じオブジェクトへの 2 つの異なるオブジェクト変数参照です。**Connection** オブジェクトの **Database** プロパティと **Database** オブジェクトの **[Connection](database-connection-property-dao.md)** プロパティを利用すると、Microsoft Access データベース エンジンを介した ODBC データ ソースへの接続を変更して ODBCDirect を使用することが容易になります。

## <a name="example"></a>例

この例では、**Database** プロパティを使用して、Microsoft Access データベース エンジンを介して ODBC データにアクセスするときに使用されるコードを変換して、ODBCDirect Connection オブジェクトを使用する方法を示します。

OldDatabaseCode プロシージャは、Microsoft Access データベース エンジンに接続されたデータ ソースを使用して ODBC データベースにアクセスします。

```vb
    Sub OldDatabaseCode() 
     
     Dim wrkMain As Workspace 
     Dim dbsPubs As Database 
     Dim prpLoop As Property 
     
     ' Create a Workspace object. 
     Set wrkMain = CreateWorkspace("", "admin", "", dbUseJet) 
     
     ' Open a Database object based on information in 
     ' the connect string. 
     
     'Note: The DSN referenced below must be configured to 
     ' use Microsoft Windows NT Authentication Mode to 
     ' authorize user access to the Microsoft SQL Server. 
     Set dbsPubs = wrkMain.OpenDatabase("Publishers", _ 
     dbDriverNoPrompt, False, _ 
     "ODBC;DATABASE=pubs;DSN=Publishers") 
     
     ' Enumerate the Properties collection of the Database 
     ' object. 
     With dbsPubs 
     Debug.Print "Database properties for " & _ 
     .Name & ":" 
     
     On Error Resume Next 
     For Each prpLoop In .Properties 
     If prpLoop.Name = "Connection" Then 
     ' Property actually returns a Connection object. 
     Debug.Print " Connection[.Name] = " & _ 
     .Connection.Name 
     Else 
     Debug.Print " " & prpLoop.Name & " = " & _ 
     prpLoop 
     End If 
     Next prpLoop 
     On Error GoTo 0 
     
     End With 
     
     dbsPubs.Close 
     wrkMain.Close 
     
    End Sub 
```

NewDatabaseCode の例は、ODBCDirect ワークスペースの **Connection** オブジェクトを開きます。次に、 **Connection** オブジェクトの **Database** プロパティを、前のプロシージャのデータ ソースと同じ名前のオブジェクト変数に割り当てます。後続のコードは、Microsoft Access ワークスペースに固有の機能を使用しない限り、変更の必要はありません。

```vb 
Sub NewDatabaseCode() 
 
 Dim wrkMain As Workspace 
 Dim conPubs As Connection 
 Dim dbsPubs As Database 
 Dim prpLoop As Property 
 
 ' Create ODBCDirect Workspace object instead of Microsoft 
 ' Access Workspace object. 
 Set wrkMain = CreateWorkspace("", "admin", "", dbUseODBC) 
 
 ' Open Connection object based on information in 
 ' the connect string. 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conPubs = wrkMain.OpenConnection("Publishers", _ 
 dbDriverNoPrompt, False, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 ' Assign the Database property to the same object 
 ' variable as in the old code. 
 Set dbsPubs = conPubs.Database 
 
 ' Enumerate the Properties collection of the Database 
 ' object. From this point on, the code is the same as the 
 ' old example. 
 With dbsPubs 
 Debug.Print "Database properties for " & _ 
 .Name & ":" 
 
 On Error Resume Next 
 For Each prpLoop In .Properties 
 If prpLoop.Name = "Connection" Then 
 ' Property actually returns a Connection object. 
 Debug.Print " Connection[.Name] = " & _ 
 .Connection.Name 
 Else 
 Debug.Print " " & prpLoop.Name & " = " & _ 
 prpLoop 
 End If 
 Next prpLoop 
 On Error GoTo 0 
 
 End With 
 
 dbsPubs.Close 
 wrkMain.Close 
 
End Sub 
 
```

