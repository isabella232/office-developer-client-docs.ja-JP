---
title: Databases コレクション (DAO)
TOCTitle: Databases Collection
ms:assetid: 988ae6f5-ec15-cd1c-191d-f295624425f4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197944(v=office.15)
ms:contentKeyID: 48546493
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f93c9dbaf4bca487785084b570efaf0bb482ab68
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565626"
---
# <a name="databases-collection-dao"></a>Databases コレクション (DAO)

**適用先:** Access 2013、Office 2013

**Databases** コレクションには、 **Workspace** オブジェクトで開かれた、または作成されたすべての開いている **Database** オブジェクトが含まれます。

## <a name="remarks"></a>注釈

**Workspace** から既存の **Database** オブジェクトを開くかまたは新しいオブジェクトを作成すると、それらは自動的に **Databases** コレクションに追加されます。 [**Close**](connection-close-method-dao.md) メソッドを使用して **Database** オブジェクトを閉じると、オブジェクトは **Databases** コレクションから削除されます。 **Database** オブジェクトを閉じる前に、開いているすべての **Recordset** オブジェクトを閉じる必要があります。

Microsoft Access ワークスペースでは、データベースの " **Name**/名前" プロパティの設定値は、データベース ファイルを指定するための文字列です。

コレクション内の **Database** オブジェクトを、コレクションで付けられたインデックスまたは **Name** プロパティの設定値で参照するには、次のいずれかの構文を使います。

- **データベース**(0)

- **データベース**("*名前*")

-  \! データベース \[*name*\]

> [!NOTE]
> 同じデータ ソースまたはデータベースを複数回開いて、**Databases** コレクションに重複する名前を作成できます。**Database** オブジェクトをオブジェクト変数に割り当て、変数名で参照する必要があります。

## <a name="example"></a>例

この例では、新しい **Database** オブジェクトを作成し、既定の **Workspace** オブジェクト内にある既存の **Database** オブジェクトを開きます。次に、**Databases** コレクションおよび各 **Database** オブジェクトの  **Properties** コレクションを列挙します。

```vb 
Sub DatabaseObjectX() 
 
 Dim wrkAcc As Workspace 
 Dim dbsNorthwind As Database 
 Dim dbsNew As Database 
 Dim dbsLoop As Database 
 Dim prpLoop As Property 
 
 Set wrkAcc = CreateWorkspace("AccWorkspace", "admin", _ 
 "", dbUseJet) 
 
 ' Make sure there isn't already a file with the name of 
 ' the new database. 
 If Dir("NewDB.mdb") <> "" Then Kill "NewDB.mdb" 
 
 ' Create a new database with the specified 
 ' collating order. 
 Set dbsNew = wrkAcc.CreateDatabase("NewDB.mdb", _ 
 dbLangGeneral) 
 Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb") 
 
 ' Enumerate the Databases collection. 
 For Each dbsLoop In wrkAcc.Databases 
 With dbsLoop 
 Debug.Print "Properties of " & .Name 
 ' Enumerate the Properties collection of each 
 ' Database object. 
 For Each prpLoop In .Properties 
 If prpLoop <> "" Then Debug.Print " " & _ 
 prpLoop.Name & " = " & prpLoop 
 Next prpLoop 
 End With 
 Next dbsLoop 
 
 dbsNew.Close 
 dbsNorthwind.Close 
 wrkAcc.Close 
 
End Sub 
 
```

<br/>

この例では、**CreateDatabase** メソッドを使用して、暗号化された新しい **Database** オブジェクトを作成します。

```vb
    Sub CreateDatabaseX() 
     
     Dim wrkDefault As Workspace 
     Dim dbsNew As DATABASE 
     Dim prpLoop As Property 
     
     ' Get default Workspace. 
     Set wrkDefault = DBEngine.Workspaces(0) 
     
     ' Make sure there isn't already a file with the name of 
     ' the new database. 
     If Dir("NewDB.mdb") <> "" Then Kill "NewDB.mdb" 
     
     ' Create a new encrypted database with the specified 
     ' collating order. 
     Set dbsNew = wrkDefault.CreateDatabase("NewDB.mdb", _ 
     dbLangGeneral, dbEncrypt) 
     
     With dbsNew 
     Debug.Print "Properties of " & .Name 
     ' Enumerate the Properties collection of the new 
     ' Database object. 
     For Each prpLoop In .Properties 
     If prpLoop <> "" Then Debug.Print " " & _ 
     prpLoop.Name & " = " & prpLoop 
     Next prpLoop 
     End With 
     
     dbsNew.Close 
     
    End Sub
```
