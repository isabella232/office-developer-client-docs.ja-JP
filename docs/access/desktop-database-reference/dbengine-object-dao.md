---
title: DBEngine オブジェクト (DAO)
TOCTitle: DBEngine Object
ms:assetid: ceaeb505-615e-37ba-4633-27240ef8c5de
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834506(v=office.15)
ms:contentKeyID: 48547792
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dc2889ad38bdc95316735901b25314f26d8df754
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479105"
---
# <a name="dbengine-object-dao"></a><span data-ttu-id="6351c-102">DBEngine オブジェクト (DAO)</span><span class="sxs-lookup"><span data-stu-id="6351c-102">DBEngine Object (DAO)</span></span>

<span data-ttu-id="6351c-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="6351c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6351c-104">**DBEngine** オブジェクトは、DAO オブジェクト モデル内のトップ レベル オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="6351c-104">The **DBEngine** object is the top level object in the DAO object model.</span></span>

## <a name="remarks"></a><span data-ttu-id="6351c-105">解説</span><span class="sxs-lookup"><span data-stu-id="6351c-105">Remarks</span></span>

<span data-ttu-id="6351c-p101">**DBEngine** オブジェクトは、DAO オブジェクトの階層内にあるその他のすべてのオブジェクトを含み、制御を行います。追加の **DBEngine** オブジェクトの作成はできず、 **DBEngine** オブジェクトはコレクションの要素ではありません。</span><span class="sxs-lookup"><span data-stu-id="6351c-p101">The **DBEngine** object contains and controls all other objects in the hierarchy of DAO objects. You can't create additional **DBEngine** objects, and the **DBEngine** object isn't an element of any collection.</span></span>

<span data-ttu-id="6351c-108">いずれのデータベースまたは接続を使用しても、以下の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="6351c-108">With any type of database or connection, you can:</span></span>

  - <span data-ttu-id="6351c-109">**Version** プロパティを使用して、DAO バージョン番号を取得します。</span><span class="sxs-lookup"><span data-stu-id="6351c-109">Use the **Version** property to obtain the DAO version number.</span></span>

  - <span data-ttu-id="6351c-110">**LoginTimeout** プロパティを使用して、ODBC ログイン タイムアウトを取得または設定し、 **RegisterDatabase** メソッドを使用して、Microsoft Access データベース エンジンに ODBC 情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="6351c-110">Use the **LoginTimeout** property to obtain or set the ODBC login timeout, and the **RegisterDatabase** method to provide ODBC information to the Microsoft Access database engine.</span></span>

  - <span data-ttu-id="6351c-111">**DefaultPassword** プロパティおよび **DefaultUser** プロパティを使用して、既定の **Workspace** オブジェクトのユーザー ID とパスワードを設定します。</span><span class="sxs-lookup"><span data-stu-id="6351c-111">Use the **DefaultPassword** and **DefaultUser** properties to set the user identification and password for the default **Workspace** object.</span></span>

  - <span data-ttu-id="6351c-p102">**CreateWorkspace** メソッドを使用して、新しい **Workspace** オブジェクトを作成します。オプションの引数を使用すると、 **DefaultType** 、 **DefaultPassword** 、および **DefaultUser** の各プロパティの設定を無効にできます。</span><span class="sxs-lookup"><span data-stu-id="6351c-p102">Use the **CreateWorkspace** method to create a new **Workspace** object. You can use optional arguments to override the settings of the **DefaultType**, **DefaultPassword**, and **DefaultUser** properties.</span></span>

  - <span data-ttu-id="6351c-114">**OpenDatabase** メソッドを使用して、既定の **Workspace** 内のデータベースを開き、 **BeginTrans** 、 **Commit** 、および **Rollback** の各メソッドを使用して、既定の **Workspace** オブジェクト上のトランザクションを制御します。</span><span class="sxs-lookup"><span data-stu-id="6351c-114">Use the **OpenDatabase** method to open a database in the default **Workspace**, and use the **BeginTrans**, **Commit**, and **Rollback** methods to control transactions on the default **Workspace**.</span></span>

  - <span data-ttu-id="6351c-115">**Workspaces** コレクションを使用して、特定の **Workspace** オブジェクトを参照します。</span><span class="sxs-lookup"><span data-stu-id="6351c-115">Use the **Workspaces** collection to reference specific **Workspace** objects.</span></span>

  - <span data-ttu-id="6351c-116">**Errors** コレクションを使用して、データ アクセス エラーの詳細を調べます。</span><span class="sxs-lookup"><span data-stu-id="6351c-116">Use the **Errors** collection to examine data access error details.</span></span>

<span data-ttu-id="6351c-p103">その他のプロパティとメソッドは、DAO と Microsoft Access データベース エンジンを組み合わせて使用する場合のみ使用できます。この組み合わせを使用すると、Microsoft Access データベース エンジンの制御、そのプロパティの操作、およびコレクションの要素ではない一時オブジェクトに対するタスクの実行が可能です。たとえば、以下の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="6351c-p103">Other properties and methods are only available when you use DAO with the Microsoft Access database engine. You can use them to control the Microsoft Access database engine, manipulate its properties, and perform tasks on temporary objects that aren't elements of collections. For example, you can:</span></span>

  - <span data-ttu-id="6351c-120">**CreateDatabase** メソッドを使用して、新しい Microsoft Access データベース エンジン **Database** オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="6351c-120">Use the **CreateDatabase** method to create a new Microsoft Access database engine **Database** object.</span></span>

  - <span data-ttu-id="6351c-121">**Idle** メソッドを使用して、Microsoft Access データベース エンジンが任意の保留中タスクを完了できるようにします。</span><span class="sxs-lookup"><span data-stu-id="6351c-121">Use the **Idle** method to enable the Microsoft Access database engine to complete any pending tasks.</span></span>

  - <span data-ttu-id="6351c-122">**CompactDatabase** メソッドおよび **RepairDatabase** メソッドを使用して、データベース ファイルを保守します。</span><span class="sxs-lookup"><span data-stu-id="6351c-122">Use the **CompactDatabase** and **RepairDatabase** methods to maintain database files.</span></span>

  - <span data-ttu-id="6351c-p104">**IniPath** プロパティを使用して、Microsoft Access データベース エンジンの Windows レジストリ情報の位置を指定し、 **SystemDB** プロパティを使用して、Microsoft Access ワークグループ情報ファイルの位置を指定します。 **SetOption** メソッドを使用すると、Microsoft Access データベース エンジンの Windows レジストリ設定を上書きできます。</span><span class="sxs-lookup"><span data-stu-id="6351c-p104">Use the **IniPath** and **SystemDB** properties to specify the location of Microsoft Access database engine Windows Registry information and the Microsoft Access workgroup information file, respectively. The **SetOption** method allows you override windows registry settings for the Microsoft Access database engine.</span></span>

<span data-ttu-id="6351c-125">**DefaultType** プロパティ設定および **IniPath** プロパティ設定を変更すると、これらの変更は後続の **Workspace** オブジェクトのみに反映されます。</span><span class="sxs-lookup"><span data-stu-id="6351c-125">After you change the **DefaultType** and **IniPath** property settings, only subsequent **Workspace** objects will reflect these changes.</span></span>

<span data-ttu-id="6351c-126">**DBEngine** オブジェクトに属するコレクション、またはこのオブジェクトに適用されるメソッドまたはプロパティを参照するには、次の構文を使用します。</span><span class="sxs-lookup"><span data-stu-id="6351c-126">To refer to a collection that belongs to the **DBEngine** object, or to refer to a method or property that applies to this object, use this syntax:</span></span>

<span data-ttu-id="6351c-127">\[**DBEngine**。\]\[コレクション |メソッド。プロパティ\]</span><span class="sxs-lookup"><span data-stu-id="6351c-127">\[**DBEngine**.\]\[collection | method | property\]</span></span>

## <a name="example"></a><span data-ttu-id="6351c-128">例</span><span class="sxs-lookup"><span data-stu-id="6351c-128">Example</span></span>

<span data-ttu-id="6351c-129">この例では、 **DBEngine** オブジェクトのコレクションを列挙します。</span><span class="sxs-lookup"><span data-stu-id="6351c-129">This example enumerates the collections of the **DBEngine** object.</span></span>

```vb
    Sub DBEngineX() 
     
     Dim wrkLoop As Workspace 
     Dim prpLoop As Property 
     
     With DBEngine 
     Debug.Print "DBEngine Properties" 
     
     ' Enumerate Properties collection of DBEngine, 
     ' trapping for properties whose values are 
     ' invalid in this context. 
     For Each prpLoop In .Properties 
     On Error Resume Next 
     Debug.Print " " & prpLoop.Name & " = " _ 
     & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     Debug.Print "Workspaces collection of DBEngine" 
     
     ' Enumerate Workspaces collection of DBEngine. 
     For Each wrkLoop In .Workspaces 
     Debug.Print " " & wrkLoop.Name 
     
     ' Enumerate Properties collection of each 
     ' Workspace object, trapping for properties 
     ' whose values are invalid in this context. 
     For Each prpLoop In wrkLoop.Properties 
     On Error Resume Next 
     Debug.Print " " & prpLoop.Name & _ 
     " = " & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     Next wrkLoop 
     
     End With 
     
    End Sub
```
