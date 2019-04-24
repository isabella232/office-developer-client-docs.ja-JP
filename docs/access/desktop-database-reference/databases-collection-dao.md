---
title: Databases コレクション (DAO)
TOCTitle: Databases Collection
ms:assetid: 988ae6f5-ec15-cd1c-191d-f295624425f4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197944(v=office.15)
ms:contentKeyID: 48546493
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dbaa0fe7aaa50c8aec582e2f03cd2849268816b9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294646"
---
# <a name="databases-collection-dao"></a><span data-ttu-id="521c2-102">Databases コレクション (DAO)</span><span class="sxs-lookup"><span data-stu-id="521c2-102">Databases collection (DAO)</span></span>

<span data-ttu-id="521c2-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="521c2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="521c2-104">**Databases** コレクションには、 **Workspace** オブジェクトで開かれた、または作成されたすべての開いている **Database** オブジェクトが含まれます。</span><span class="sxs-lookup"><span data-stu-id="521c2-104">A **Databases** collection contains all open **Database** objects opened or created in a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="521c2-105">注釈</span><span class="sxs-lookup"><span data-stu-id="521c2-105">Remarks</span></span>

<span data-ttu-id="521c2-p101">**Workspace** から既存の **Database** オブジェクトを開くかまたは新しいオブジェクトを作成すると、それらは自動的に **Databases** コレクションに追加されます。 [**Close**](connection-close-method-dao.md) メソッドを使用して **Database** オブジェクトを閉じると、オブジェクトは **Databases** コレクションから削除されます。 **Database** オブジェクトを閉じる前に、開いているすべての **Recordset** オブジェクトを閉じる必要があります。</span><span class="sxs-lookup"><span data-stu-id="521c2-p101">When you open an existing **Database** object or create a new one from a **Workspace**, it is automatically appended to the **Databases** collection. When you close a **Database** object with the **[Close](connection-close-method-dao.md)** method, it is removed from the **Databases** collection but not deleted from disk. You should close all open **Recordset** objects before closing a **Database** object.</span></span>

<span data-ttu-id="521c2-109">Microsoft Access ワークスペースでは、データベースの " **Name**/名前" プロパティの設定値は、データベース ファイルを指定するための文字列です。</span><span class="sxs-lookup"><span data-stu-id="521c2-109">In a Microsoft Access workspace, the **Name** property setting of a database is a string that specifies the path of the database file.</span></span>

<span data-ttu-id="521c2-110">コレクション内の **Database** オブジェクトを、コレクションで付けられたインデックスまたは **Name** プロパティの設定値で参照するには、次のいずれかの構文を使います。</span><span class="sxs-lookup"><span data-stu-id="521c2-110">To refer to a **Database** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="521c2-111">**データベース**.0</span><span class="sxs-lookup"><span data-stu-id="521c2-111">**Databases**(0)</span></span>

- <span data-ttu-id="521c2-112">**データベース**("*name*")</span><span class="sxs-lookup"><span data-stu-id="521c2-112">**Databases**("*name*")</span></span>

- <span data-ttu-id="521c2-113">\*\*\*\*\!データベース\[*名*\]</span><span class="sxs-lookup"><span data-stu-id="521c2-113">**Databases**\!\[*name*\]</span></span>

> [!NOTE]
> <span data-ttu-id="521c2-p102">[!メモ] **Databases** コレクションに重複する名前を作成して同じデータ ソースまたはデータベースを複数回開くことができます。 **Database** オブジェクトをオブジェクト変数に割り当てて変数名で参照する必要があります。</span><span class="sxs-lookup"><span data-stu-id="521c2-p102">You can open the same data source or database more than once, creating duplicate names in the **Databases** collection. You should assign **Database** objects to object variables and refer to them by variable name.</span></span>

## <a name="example"></a><span data-ttu-id="521c2-116">例</span><span class="sxs-lookup"><span data-stu-id="521c2-116">Example</span></span>

<span data-ttu-id="521c2-p103">この例では、新しい **Database** オブジェクトを作成し、既定の **Workspace** オブジェクト内にある既存の **Database** オブジェクトを開きます。次に、 **Databases** コレクションおよび各 **Database** オブジェクトの **Properties** コレクションを列挙します。</span><span class="sxs-lookup"><span data-stu-id="521c2-p103">This example creates a new **Database** object and opens an existing **Database** object in the default **Workspace** object. Then it enumerates the **Database** collection and the **Properties** collection of each **Database** object.</span></span>

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

<span data-ttu-id="521c2-119">この例では、 **CreateDatabase** メソッドを使用して、暗号化された新しい **Database** オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="521c2-119">This example uses **CreateDatabase** to create a new, encrypted **Database** object.</span></span>

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
