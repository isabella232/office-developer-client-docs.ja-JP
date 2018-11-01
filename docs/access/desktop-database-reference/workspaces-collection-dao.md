---
title: Workspaces コレクション (DAO)
TOCTitle: Workspaces Collection
ms:assetid: 88b851ce-4180-964f-582e-bc9571bf554c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197057(v=office.15)
ms:contentKeyID: 48546142
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4108be7d6c1b2ee66ec5cddf4d26599796bf844c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870269"
---
# <a name="workspaces-collection-dao"></a><span data-ttu-id="788a6-102">Workspaces コレクション (DAO)</span><span class="sxs-lookup"><span data-stu-id="788a6-102">Workspaces Collection (DAO)</span></span>


<span data-ttu-id="788a6-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="788a6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="788a6-p101">**Workspaces** コレクションには、 **DBEngine** オブジェクトの、表示されているアクティブなすべての **Workspace** オブジェクトが含まれます。非表示の **Workspace** オブジェクトはコレクションに追加されず、割り当てられている変数によって参照されます。</span><span class="sxs-lookup"><span data-stu-id="788a6-p101">A **Workspaces** collection contains all active, unhidden **Workspace** objects of the **DBEngine** object. (Hidden **Workspace** objects are not appended to the collection and referenced by the variable to which they are assigned.)</span></span>

## <a name="remarks"></a><span data-ttu-id="788a6-106">注釈</span><span class="sxs-lookup"><span data-stu-id="788a6-106">Remarks</span></span>

<span data-ttu-id="788a6-107">**Workspace** オブジェクトを使用して、現在のセッションを管理するか別のセッションを開始します。</span><span class="sxs-lookup"><span data-stu-id="788a6-107">Use the **Workspace** object to manage the current session or to start an additional session.</span></span>

<span data-ttu-id="788a6-108">最初を参照してくださいか、**ワークスペース**オブジェクトを使用して、DBEngine.Workspaces(0)、既定のワークスペースを自動的に作成します。</span><span class="sxs-lookup"><span data-stu-id="788a6-108">When you first refer to or use a **Workspace** object, you automatically create the default workspace, DBEngine.Workspaces(0).</span></span> <span data-ttu-id="788a6-109">既定のワークスペースの**名前**と**ユーザー名**のプロパティの設定は、"\#既定のワークスぺース\#」と「Admin」に、それぞれ。</span><span class="sxs-lookup"><span data-stu-id="788a6-109">The settings of the **Name** and **UserName** properties of the default workspace are "\#Default Workspace\#" and "Admin," respectively.</span></span> <span data-ttu-id="788a6-110">セキュリティが有効になっている場合、 **UserName** プロパティの設定はログオンしたユーザーの名前になります。</span><span class="sxs-lookup"><span data-stu-id="788a6-110">If security is enabled, the **UserName** property setting is the name of the user who logged on.</span></span>

<span data-ttu-id="788a6-p103">[**CreateWorkspace**](dbengine-createworkspace-method-dao.md) メソッドを使用すると、新しい **Workspace** オブジェクトを作成できます。新しい **Workspace** オブジェクトを作成した後、それを **Workspaces** コレクションから参照する必要がある場合は、オブジェクトを **Workspaces** コレクションに追加する必要があります。ただし、新しく作成した **Workspace** オブジェクトは、 **Workspaces** コレクションに追加せずに使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="788a6-p103">You can create new **Workspace** objects with the **[CreateWorkspace](dbengine-createworkspace-method-dao.md)** method. After you create a new **Workspace** object, you must append it to the **Workspaces** collection if you need to refer to it from the **Workspaces** collection. You can, however, use a newly created **Workspace** object without appending it to the **Workspaces** collection.</span></span>

<span data-ttu-id="788a6-114">コレクション内の **Workspace** オブジェクトを、コレクションで付けられたインデックスまたは **Name** プロパティの設定値で参照するには、次のいずれかの構文を使います。</span><span class="sxs-lookup"><span data-stu-id="788a6-114">To refer to a **Workspace** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="788a6-115">**DBEngine**。**ワークスペース**(0)</span><span class="sxs-lookup"><span data-stu-id="788a6-115">**DBEngine**.**Workspaces**(0)</span></span>

<span data-ttu-id="788a6-116">**DBEngine**。**ワークスペース**("name")</span><span class="sxs-lookup"><span data-stu-id="788a6-116">**DBEngine**.**Workspaces**("name")</span></span>

<span data-ttu-id="788a6-117">**DBEngine**。**ワークスペース**\!\[名\]</span><span class="sxs-lookup"><span data-stu-id="788a6-117">**DBEngine**.**Workspaces**\!\[name\]</span></span>


> [!NOTE]
> <span data-ttu-id="788a6-p104">[!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</span><span class="sxs-lookup"><span data-stu-id="788a6-p104">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>



## <a name="example"></a><span data-ttu-id="788a6-120">例</span><span class="sxs-lookup"><span data-stu-id="788a6-120">Example</span></span>

<span data-ttu-id="788a6-p105">この例では、新しい Microsoft Access ワークスペース オブジェクトを作成し、 **Workspaces** コレクションに追加します。次に、 **Workspaces** コレクションおよび **Workspace** オブジェクトの **Properties** コレクションを列挙します。</span><span class="sxs-lookup"><span data-stu-id="788a6-p105">This example creates a new Microsoft Access Workspace object and appends it to the **Workspaces** collection. It then enumerates the **Workspaces** collections and the **Properties** collection of the **Workspace** object.</span></span>

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
 If prpLoop <> "" Then Debug.Print " " & _ 
 prpLoop.Name & " = " & prpLoop 
 On Error GoTo 0 
 Next prpLoop 
 End With 
 Next wrkLoop 
 
 wrkNewAcc.Close 
End Sub 
```

<br/>

<span data-ttu-id="788a6-p106">この例では、 **CreateWorkspace** メソッドを使用して、Microsoft Access ワークスペースを作成します。次に、そのワークスペースのプロパティの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="788a6-p106">This example uses the **CreateWorkspace** method to create a Microsoft Access workspace. It then lists the properties of theworkspace.</span></span>

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
 Debug.Print " " & wrkLoop.Name 
 Next wrkLoop 
 
 With wrkAcc 
 ' Enumerate Properties collection of Microsoft Access 
 ' workspace. 
 Debug.Print _ 
 "Properties of unnamed Microsoft Access workspace" 
 On Error Resume Next 
 For Each prpLoop In .Properties 
 Debug.Print " " & prpLoop.Name & " = " & prpLoop 
 Next prpLoop 
 On Error GoTo 0 
 End With 
 
 wrkAcc.Close 
 
End Sub 
 
```

