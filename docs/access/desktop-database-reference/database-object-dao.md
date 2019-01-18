---
title: データベース オブジェクト (DAO)
TOCTitle: Database Object
ms:assetid: 6cf2ddf8-3957-a15e-5eeb-85f81c1e415e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195520(v=office.15)
ms:contentKeyID: 48545482
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm0
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: c23772c54f2f980b8d10d4afc352687935840752
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707788"
---
# <a name="database-object-dao"></a><span data-ttu-id="23ff0-102">データベース オブジェクト (DAO)</span><span class="sxs-lookup"><span data-stu-id="23ff0-102">Database object (DAO)</span></span>

<span data-ttu-id="23ff0-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="23ff0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="23ff0-104">**Database** オブジェクトは、開いているデータベースを表します。</span><span class="sxs-lookup"><span data-stu-id="23ff0-104">A **Database** object represents an open database.</span></span>

## <a name="remarks"></a><span data-ttu-id="23ff0-105">解説</span><span class="sxs-lookup"><span data-stu-id="23ff0-105">Remarks</span></span>

<span data-ttu-id="23ff0-p101">開いているデータベースを操作するには、 **Database** オブジェクトとそのメソッドおよびプロパティを使用します。あらゆる種類のデータベースで、以下の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="23ff0-p101">You use the **Database** object and its methods and properties to manipulate an open database. In any type of database, you can:</span></span>

  - <span data-ttu-id="23ff0-108">**Execute** メソッドを使用して、アクション クエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="23ff0-108">Use the **Execute** method to run an action query.</span></span>

  - <span data-ttu-id="23ff0-109">**Connect** プロパティを設定して、ODBC データ ソースへの接続を確立します。</span><span class="sxs-lookup"><span data-stu-id="23ff0-109">Set the **Connect** property to establish a connection to an ODBC data source.</span></span>

  - <span data-ttu-id="23ff0-110">**QueryTimeout** プロパティを設定して、ODBC データ ソースに対して実行するクエリを待機する時間を制限します。</span><span class="sxs-lookup"><span data-stu-id="23ff0-110">Set the **QueryTimeout** property to limit the length of time to wait for a query to execute against an ODBC data source.</span></span>

  - <span data-ttu-id="23ff0-111">**RecordsAffected** プロパティを使用して、アクション クエリによって変更されたレコードの数を確認します。</span><span class="sxs-lookup"><span data-stu-id="23ff0-111">Use the **RecordsAffected** property to determine how many records were changed by an action query.</span></span>

  - <span data-ttu-id="23ff0-112">**OpenRecordset** メソッドを使用して、選択クエリを実行し、 **Recordset** オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="23ff0-112">Use the **OpenRecordset** method to execute a select query and create a **Recordset** object.</span></span>

  - <span data-ttu-id="23ff0-113">**Version** プロパティを使用して、データベースを作成したデータベース エンジンのバージョンを確認します。</span><span class="sxs-lookup"><span data-stu-id="23ff0-113">Use the **Version** property to determine which version of a database engine created the database.</span></span>

<span data-ttu-id="23ff0-p102">Microsoft Access データベース エンジン データベースを使用すると、Database オブジェクトのテーブル、クエリ、およびリレーションシップに関する情報を作成、変更、または取得するだけでなく、他のメソッド、プロパティ、およびコレクションを使用して **Database** オブジェクトを操作することもできます。たとえば、以下の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="23ff0-p102">With a Microsoft Access database engine database, you can also use other methods, properties, and collections to manipulate a **Database** object, as well as create, modify, or get information about its tables, queries, and relationships. For example, you can:</span></span>

  - <span data-ttu-id="23ff0-116">**CreateTableDef** メソッドを使用してテーブルを作成し、 **CreateRelation** メソッドを使用してリレーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="23ff0-116">Use the **CreateTableDef** and **CreateRelation** methods to create tables and relations, respectively.</span></span>

  - <span data-ttu-id="23ff0-117">**CreateProperty** メソッドを使用して、新しい **Database** プロパティを定義します。</span><span class="sxs-lookup"><span data-stu-id="23ff0-117">Use the **CreateProperty** method to define new **Database** properties.</span></span>

  - <span data-ttu-id="23ff0-118">**CreateQueryDef** メソッドを使用して、持続的または一時的なクエリ定義を作成します。</span><span class="sxs-lookup"><span data-stu-id="23ff0-118">Use the **CreateQueryDef** method to create a persistent or temporary query definition.</span></span>

  - <span data-ttu-id="23ff0-119">**MakeReplica** 、 **Synchronize** 、および **PopulatePartial** の各メソッドを使用して、データベースのフルまたは部分レプリカを作成して同期します。</span><span class="sxs-lookup"><span data-stu-id="23ff0-119">Use **MakeReplica**, **Synchronize**, and **PopulatePartial** methods to create and synchronize full or partial replicas of your database.</span></span>

  - <span data-ttu-id="23ff0-120">**CollatingOrder** プロパティを設定して、異なる言語の文字ベース フィールドに五十音順の並べ替え順序を設定します。</span><span class="sxs-lookup"><span data-stu-id="23ff0-120">Set the **CollatingOrder** property to establish the alphabetic sorting order for character-based fields in different languages.</span></span>

<span data-ttu-id="23ff0-121">**CreateDatabase** メソッドを使用して、 **Databases** コレクションに自動的に追加される永続的な **Database** オブジェクトを作成し、ディスクに保存します。</span><span class="sxs-lookup"><span data-stu-id="23ff0-121">You use the **CreateDatabase** method to create a persistent **Database** object that is automatically appended to the **Databases** collection, thereby saving it to disk.</span></span>

<span data-ttu-id="23ff0-122">**OpenDatabase** メソッドを使用する場合、 **DBEngine** オブジェクトを指定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="23ff0-122">You don't need to specify the **DBEngine** object when you use the **OpenDatabase** method.</span></span>

<span data-ttu-id="23ff0-p103">リンク テーブルを使用するデータベースを開いても、指定した外部ファイルへのリンクは自動的に確立されません。テーブルの **TableDef** オブジェクトまたは **Field** オブジェクトを参照するか、 **Recordset** オブジェクトを開く必要があります。これらのテーブルへのリンクを設定できない場合、トラップ可能なエラーが発生します。データベースにアクセスする権限が必要な場合も、別のユーザーがデータベースを排他的に開いている可能性もあります。このような場合、トラップ可能なエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="23ff0-p103">Opening a database with linked tables doesn't automatically establish links to the specified external files. You must either reference the table's **TableDef** or **Field** objects or open a **Recordset** object. If you can't establish links to these tables, a trappable error occurs. You may also need permission to access the database, or another user might have the database opened exclusively. In these cases, trappable errors occur.</span></span>

<span data-ttu-id="23ff0-p104">**Database** オブジェクトを宣言するプロシージャが実行されると、開いているすべての **Recordset** オブジェクトと共にローカルの **Database** オブジェクトが閉じられます。保留中の更新は失われ、保留中のトランザクションはロールバックされますが、トラップ可能なエラーは発生しません。 **Recordset** オブジェクト変数および **Database** オブジェクト変数をローカルに宣言するプロシージャを終了する前に、保留中のトランザクションまたは編集を明示的に完了し、これらのオブジェクトを閉じる必要があります。</span><span class="sxs-lookup"><span data-stu-id="23ff0-p104">When a procedure that declares a **Database** object has executed, local **Database** objects are closed along with any open **Recordset** objects. Any pending updates are lost and any pending transactions are rolled back, but no trappable error occurs. You should explicitly complete any pending transactions or edits and close **Recordset** objects and **Database** objects before exiting procedures that declare these object variables locally.</span></span>

<span data-ttu-id="23ff0-p105">**Workspace** オブジェクトでトランザクション メソッド (**BeginTrans**、**CommitTrans**、または **Rollback**) のいずれかを使用する場合、これらのトランザクションは、**Database** オブジェクトを開いた **Workspace** オブジェクトに対して開かれるすべてのデータベースに適用されます。個別のトランザクションを使用するには、追加の **Workspace** オブジェクトを開いてから、その **Workspace** オブジェクト内でもう 1 つ **Database** オブジェクトを開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="23ff0-p105">When you use one of the transaction methods (**BeginTrans**, **CommitTrans**, or **Rollback**) on the **Workspace** object, these transactions apply to all databases opened on the **Workspace** from which the **Database** object was opened. If you want to use independent transactions, you must first open an additional **Workspace** object, and then open another **Database** object in that **Workspace** object.</span></span>


> [!NOTE]
> <span data-ttu-id="23ff0-p106">[!メモ] **Databases** コレクションに重複する名前を作成して同じデータ ソースまたはデータベースを複数回開くことができます。 **Database** オブジェクトをオブジェクト変数に割り当てて変数名で参照する必要があります。</span><span class="sxs-lookup"><span data-stu-id="23ff0-p106">You can open the same data source or database more than once, creating duplicate names in the **Databases** collection. You should assign **Database** objects to object variables and refer to them by variable name.</span></span>



## <a name="example"></a><span data-ttu-id="23ff0-135">例</span><span class="sxs-lookup"><span data-stu-id="23ff0-135">Example</span></span>

<span data-ttu-id="23ff0-p107">この例では、新しい **Database** オブジェクトを作成し、既定の **Workspace** オブジェクト内にある既存の **Database** オブジェクトを開きます。次に、 **Databases** コレクションおよび各 **Database** オブジェクトの **Properties** コレクションを列挙します。</span><span class="sxs-lookup"><span data-stu-id="23ff0-p107">This example creates a new **Database** object and opens an existing **Database** object in the default **Workspace** object. Then it enumerates the **Database** collection and the **Properties** collection of each **Database** object.</span></span>

```vb 
Sub DatabaseObjectX() 
 
 Dim wrkAcc As Workspace 
 Dim dbsNorthwind As Database 
 Dim dbsNew As Database 
 Dim dbsLoop As Database 
 Dim prpLoop As Property 
 
 Set wrkAcc = CreateWorkspace("AccessWorkspace", "admin", _ 
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

<span data-ttu-id="23ff0-138">この例では、 **CreateDatabase** メソッドを使用して、暗号化された新しい **Database** オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="23ff0-138">This example uses **CreateDatabase** to create a new, encrypted **Database** object.</span></span>

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
