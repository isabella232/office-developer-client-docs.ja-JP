---
title: ワークスペース オブジェクト (DAO)
TOCTitle: Workspace Object
ms:assetid: bf3ab863-5e9a-4842-1f82-2ccf958d9779
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822782(v=office.15)
ms:contentKeyID: 48547481
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 2c734d5e0f022faec4ebb9efe2dfc2f7dd7b7979
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711582"
---
# <a name="workspace-object-dao"></a><span data-ttu-id="1bf11-102">ワークスペース オブジェクト (DAO)</span><span class="sxs-lookup"><span data-stu-id="1bf11-102">Workspace object (DAO)</span></span>

<span data-ttu-id="1bf11-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="1bf11-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1bf11-p101">**Workspace** オブジェクトは、ユーザー用に名前付きセッションを定義します。これには開いているデータベースが含まれ、同時実行トランザクションのメカニズムを提供し、Microsoft Access ワークスペースの場合は、セキュリティが設定されたワークグループをサポートします。</span><span class="sxs-lookup"><span data-stu-id="1bf11-p101">A **Workspace** object defines a named session for a user. It contains open databases and provides mechanisms for simultaneous transactions and, in Microsoft Access workspaces, secure workgroup support.</span></span>

## <a name="remarks"></a><span data-ttu-id="1bf11-106">注釈</span><span class="sxs-lookup"><span data-stu-id="1bf11-106">Remarks</span></span>

<span data-ttu-id="1bf11-p102">**Workspace** オブジェクトは、アプリケーションが Microsoft Access データベース エンジンを使用してデータを操作する方法を定義する非永続的なオブジェクトです。現在のセッションの管理、または追加のセッションの開始に、 **Workspace** オブジェクトを使用します。セッションでは、複数のデータベースまたは接続を開き、トランザクションを管理できます。たとえば、以下の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="1bf11-p102">A **Workspace** is a non-persistent object that defines how your application interacts with data by using the Microsoft Access database engine. Use the **Workspace** object to manage the current session or to start an additional session. In a session, you can open multiple databases or connections, and manage transactions. For example, you can:</span></span>

- <span data-ttu-id="1bf11-p103">**Name** 、 **UserName** 、および **Type** の各プロパティを使用して、名前付きセッションを確立します。セッションでは、複数のデータベースを開き、ネストされたトランザクションの 1 つのインスタンスを実行できる適用範囲が作成されます。</span><span class="sxs-lookup"><span data-stu-id="1bf11-p103">Use the **Name**, **UserName**, and **Type** properties to establish a named session. The session creates a scope in which you can open multiple databases and conduct one instance of nested transactions.</span></span>

- <span data-ttu-id="1bf11-113">**Close** メソッドを使用して、セッションを終了します。</span><span class="sxs-lookup"><span data-stu-id="1bf11-113">Use the **Close** method to terminate a session.</span></span>

- <span data-ttu-id="1bf11-114">**OpenDatabase** メソッドを使用して、 **Workspace** で 1 つまたは複数の既存のデータベースを開きます。</span><span class="sxs-lookup"><span data-stu-id="1bf11-114">Use the **OpenDatabase** method to open one or more existing databases on a **Workspace**.</span></span>

- <span data-ttu-id="1bf11-115">**BeginTrans** 、 **CommitTrans** 、および **Rollback** の各メソッドを使用して、 **Workspace** 内のネストされたトランザクションの処理を管理し、複数の **Workspace** オブジェクトを使用して、複数のトランザクション、同時実行トランザクション、および重なり合うトランザクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="1bf11-115">Use the **BeginTrans**, **CommitTrans**, and **Rollback** methods to manage nested transaction processing within a **Workspace** and use several **Workspace** objects to conduct multiple, simultaneous, and overlapping transactions.</span></span>

<span data-ttu-id="1bf11-116">最初を参照してくださいか、**ワークスペース**オブジェクトを使用して、DBEngine.Workspaces(0)、既定のワークスペースを自動的に作成します。</span><span class="sxs-lookup"><span data-stu-id="1bf11-116">When you first refer to or use a **Workspace** object, you automatically create the default workspace, DBEngine.Workspaces(0).</span></span> <span data-ttu-id="1bf11-117">既定のワークスペースの**名前**と**ユーザー名**のプロパティの設定は、"\#既定のワークスぺース\#」と「Admin」に、それぞれ。</span><span class="sxs-lookup"><span data-stu-id="1bf11-117">The settings of the **Name** and **UserName** properties of the default workspace are "\#Default Workspace\#" and "Admin," respectively.</span></span> <span data-ttu-id="1bf11-118">セキュリティが有効になっている場合、 **UserName** プロパティの設定はログオンしたユーザーの名前になります。</span><span class="sxs-lookup"><span data-stu-id="1bf11-118">If security is enabled, the **UserName** property setting is the name of the user who logged on.</span></span>

<span data-ttu-id="1bf11-p105">トランザクションを使用する場合、 **Workspace** オブジェクトで複数の **Database** オブジェクトが開かれていると、指定した **Workspace** オブジェクトのすべてのデータベースが影響を受けます。たとえば、 **BeginTrans** メソッドを使用し、あるデータベースの複数のレコードを更新した後、別のデータベースのレコードを削除します。次に、 **Rollback** メソッドを使用すると、更新と削除の両方の操作がキャンセルされ、ロールバックされます。複数の **Database** オブジェクトにまたがってトランザクションを個別に管理するには、追加の **Workspace** オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="1bf11-p105">When you use transactions, all databases in the specified **Workspace** are affected— even if multiple **Database** objects are opened in the **Workspace**. For example, you use a **BeginTrans** method, update several records in a database, and then delete records in another database. If you then use the **Rollback** method, both the update and delete operations are canceled and rolled back. You can create additional **Workspace** objects to manage transactions independently across **Database** objects.</span></span>

<span data-ttu-id="1bf11-p106">**CreateWorkspace** メソッドを使用して、 **Workspace** オブジェクトを作成できます。新しい **Workspace** オブジェクトを作成した後、それを **Workspaces** コレクションから参照する必要がある場合は、オブジェクトを **Workspaces** コレクションに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1bf11-p106">You can create **Workspace** objects with the **CreateWorkspace** method. After you create a new **Workspace** object, you must append it to the **Workspaces** collection if you need to refer to it from the **Workspaces** collection.</span></span>

<span data-ttu-id="1bf11-p107">新規に作成された **Workspace** オブジェクトは、 **Workspaces** コレクションに追加しなくても使用できます。ただし、オブジェクトに割り当てたオブジェクト変数で参照する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1bf11-p107">You can use a newly created **Workspace** object without appending it to the **Workspaces** collection. However, you must refer to it by the object variable to which you have assigned it.</span></span>

<span data-ttu-id="1bf11-127">コレクション内の **Workspace** オブジェクトを、コレクションで付けられたインデックスまたは **Name** プロパティの設定値で参照するには、次のいずれかの構文を使います。</span><span class="sxs-lookup"><span data-stu-id="1bf11-127">To refer to a **Workspace** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="1bf11-128">**DBEngine**。**ワークスペース**(0)</span><span class="sxs-lookup"><span data-stu-id="1bf11-128">**DBEngine**.**Workspaces**(0)</span></span>

<span data-ttu-id="1bf11-129">**DBEngine**。**ワークスペース**("name")</span><span class="sxs-lookup"><span data-stu-id="1bf11-129">**DBEngine**.**Workspaces**("name")</span></span>

<span data-ttu-id="1bf11-130">**DBEngine**。**ワークスペース**\!\[名\]</span><span class="sxs-lookup"><span data-stu-id="1bf11-130">**DBEngine**.**Workspaces**\!\[name\]</span></span>

> [!NOTE]
> <span data-ttu-id="1bf11-p108">[!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</span><span class="sxs-lookup"><span data-stu-id="1bf11-p108">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


## <a name="example"></a><span data-ttu-id="1bf11-133">例</span><span class="sxs-lookup"><span data-stu-id="1bf11-133">Example</span></span>

<span data-ttu-id="1bf11-p109">この例では、新しい Microsoft Access ワークスペース オブジェクトを作成し、 **Workspaces** コレクションに追加します。次に、 **Workspaces** コレクションおよび **Workspace** オブジェクトの **Properties** コレクションを列挙します。</span><span class="sxs-lookup"><span data-stu-id="1bf11-p109">This example creates a new Microsoft Access Workspace object and appends it to the **Workspaces** collection. It then enumerates the **Workspaces** collections and the **Properties** collection of the **Workspace** object.</span></span>

```vb 
Sub WorkspaceX() 
 
   Dim wrkNewAcc As Workspace 
   Dim wrkLoop As Workspace 
   Dim prpLoop As Property 
 
   ' Create a new Microsoft Access workspace. 
   Set wrkNewAcc = CreateWorkspace("NewAccessWorkspace", _ 
      "admin", "", dbUseJet) 
   Workspaces.Append wrkNewAcc 
 
   ' Enumerate the Workspaces collection. 
   For Each wrkLoop In Workspaces 
      With wrkLoop 
         Debug.Print "Properties of " & .Name 
         ' Enumerate the Properties collection of the new 
         ' Workspace object. 
         For Each prpLoop In .Properties 
            On Error Resume Next 
            If prpLoop <> "" Then Debug.Print "  " & _ 
               prpLoop.Name & " = " & prpLoop 
            On Error GoTo 0 
         Next prpLoop 
      End With 
   Next wrkLoop 
 
   wrkNewAcc.Close 
End Sub 
```

<br/>

<span data-ttu-id="1bf11-p110">この例では、 **CreateWorkspace** メソッドを使用して、Microsoft Access ワークスペースを作成します。次に、そのワークスペースのプロパティの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="1bf11-p110">This example uses the **CreateWorkspace** method to create a Microsoft Access workspace. It then lists the properties of theworkspace.</span></span>

```vb 
Sub CreateWorkspaceX() 
 
   Dim wrkAcc As Workspace 
   Dim wrkLoop As Workspace 
   Dim prpLoop As Property 
 
 
   DefaultType = dbUseJet 
   ' Create an unnamed Workspace object of the type  
   ' specified by the DefaultType property of DBEngine  
   ' (dbUseJet). 
   Set wrkAcc = CreateWorkspace("", "admin", "") 
 
   ' Enumerate Workspaces collection. 
   Debug.Print "Workspace objects in Workspaces collection:" 
   For Each wrkLoop In Workspaces 
      Debug.Print "  " & wrkLoop.Name 
   Next wrkLoop 
 
   With wrkAcc 
      ' Enumerate Properties collection of Microsoft Access  
      ' workspace. 
      Debug.Print _ 
         "Properties of unnamed Microsoft Access workspace" 
      On Error Resume Next 
      For Each prpLoop In .Properties 
         Debug.Print "  " & prpLoop.Name & " = " & prpLoop 
      Next prpLoop 
      On Error GoTo 0 
   End With 
 
   wrkAcc.Close 
 
End Sub 
```

<br/>

<span data-ttu-id="1bf11-138">次の例は、DAO (Data Access Objects) ワークスペース内でトランザクションを使用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="1bf11-138">The following example shows how to use a transaction in a Data Access Objects (DAO) workspace.</span></span>

<span data-ttu-id="1bf11-139">**によって提供されるサンプル コード**を[Microsoft Access 2010 プログラマーズ リファレンス](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)です。</span><span class="sxs-lookup"><span data-stu-id="1bf11-139">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>


```vb
    Public Sub TransferFunds()
        Dim wrk As DAO.Workspace
        Dim dbC As DAO.Database
        Dim dbX As DAO.Database
        
        Set wrk = DBEngine(0)
        Set dbC = CurrentDb
        Set dbX = wrk.OpenDatabase("e:\books\acc2007vba\myDB.accdb")
        
        On Error GoTo trans_Err
        
        'Begin the transaction
        
        wrk.BeginTrans
        
        'Withdraw funds from one account table
        dbC.Execute "INSERT INTO tblAccounts ( Amount, Txn, TxnDate ) SELECT -20, 'DEBIT', Date()", dbFailOnError
    
        'Deposit funds into another account table
        dbX.Execute "INSERT INTO tblAccounts ( Amount, Txn, TxnDate ) SELECT 20, 'CREDIT', Date()", dbFailOnError
        
        'Commit the transaction
        wrk.CommitTrans dbForceOSFlush
        
    trans_Exit:
        'Clean up
        wrk.Close
        Set dbC = Nothing
        Set dbX = Nothing
        Set wrk = Nothing
        Exit Sub
        
    trans_Err:
        'Roll back the transaction
        wrk.Rollback
        Resume trans_Exit
        
    End Sub
```
