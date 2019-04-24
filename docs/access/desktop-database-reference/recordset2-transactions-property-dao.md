---
title: Recordset2 プロパティ (DAO)
TOCTitle: Transactions Property
ms:assetid: f2169565-f782-4089-0e4b-bc5d58d37db5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836614(v=office.15)
ms:contentKeyID: 48548642
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 58610ee87e61a8b342955107c2ba2b690e610c8b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309243"
---
# <a name="recordset2transactions-property-dao"></a><span data-ttu-id="baf84-102">Recordset2 プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="baf84-102">Recordset2.Transactions property (DAO)</span></span>


<span data-ttu-id="baf84-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="baf84-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="baf84-104">オブジェクトがトランザクションをサポートしているかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="baf84-104">Returns a value that indicates whether an object supports transactions.</span></span> <span data-ttu-id="baf84-105">値の取得のみ可能なブール型 (**Boolean**) の値です。</span><span class="sxs-lookup"><span data-stu-id="baf84-105">Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="baf84-106">構文</span><span class="sxs-lookup"><span data-stu-id="baf84-106">Syntax</span></span>

<span data-ttu-id="baf84-107">*式*。トランザクション</span><span class="sxs-lookup"><span data-stu-id="baf84-107">*expression* .Transactions</span></span>

<span data-ttu-id="baf84-108">\*式\***Recordset2**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="baf84-108">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="baf84-109">注釈</span><span class="sxs-lookup"><span data-stu-id="baf84-109">Remarks</span></span>

<span data-ttu-id="baf84-110">Microsoft Access ワークスペースでは、ダイナセット タイプまたはテーブル タイプの **Recordset** オブジェクトでも **Transactions** プロパティを使用できます。</span><span class="sxs-lookup"><span data-stu-id="baf84-110">In a Microsoft Access workspace, you can also use the **Transactions** property with dynaset- or table-type **Recordset** objects.</span></span> <span data-ttu-id="baf84-111">スナップショットおよび前方スクロールタイプの**[Recordset](recordset-object-dao.md)** オブジェクトでは、常に**False**が返されます。</span><span class="sxs-lookup"><span data-stu-id="baf84-111">Snapshot- and forward–only–type **[Recordset](recordset-object-dao.md)** objects always return **False**.</span></span>

<span data-ttu-id="baf84-p103">ダイナセット タイプまたはテーブル タイプの **Recordset** が Microsoft Access データベース エンジン テーブルに基づいている場合、 **Transactions** プロパティは **True** となるため、トランザクションを使用できます。他のデータベース エンジンでは、トランザクションがサポートされていないことがあります。たとえば、Paradox テーブルに基づくダイナセット タイプの **Recordset** オブジェクトでは、トランザクションを使用できません。</span><span class="sxs-lookup"><span data-stu-id="baf84-p103">If a dynaset- or table-type **Recordset** is based on a Microsoft Access database engine table, the **Transactions** property is **True** and you can use transactions. Other database engines may not support transactions. For example, you can't use transactions in a dynaset-type **Recordset** object based on a Paradox table.</span></span>

<span data-ttu-id="baf84-p104">**Recordset** オブジェクトの **[Workspace](dbengine-begintrans-method-dao.md)** オブジェクトで [**BeginTrans**](workspace-object-dao.md) メソッドを使用する前に、 **Transactions** プロパティでトランザクションがサポートされているかどうかを確認してください。トランザクションがサポートされていないオブジェクト上で **BeginTrans**、 **CommitTrans**、または **Rollback** の各メソッドを使用しても、何も変化しません。</span><span class="sxs-lookup"><span data-stu-id="baf84-p104">Check the **Transactions** property before using the **[BeginTrans](dbengine-begintrans-method-dao.md)** method on the **Recordset** object's **[Workspace](workspace-object-dao.md)** object to make sure that transactions are supported. Using the **BeginTrans**, **CommitTrans**, or **Rollback** methods on an unsupported object has no effect.</span></span>

## <a name="example"></a><span data-ttu-id="baf84-117">例</span><span class="sxs-lookup"><span data-stu-id="baf84-117">Example</span></span>

<span data-ttu-id="baf84-118">次の例では、Microsoft Access ワークスペースでの **Transactions** プロパティの機能を示します。</span><span class="sxs-lookup"><span data-stu-id="baf84-118">This example demonstrates the **Transactions** property in Microsoft Access workspaces.</span></span>

```vb 
Sub TransactionsX() 
 
 Dim wrkAcc As Workspace 
 Dim dbsNorthwind As Database 
 Dim conPubs As Connection 
 Dim rstTemp As Recordset 
 
 Set wrkAcc = CreateWorkspace("", "admin", "", dbUseJet) 
 Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb") 
 
 ' Open two different Recordset objects and display the 
 ' Transactions property of each. 
 
 Debug.Print "Opening Microsoft Access table-type " & _ 
 "recordset..." 
 Set rstTemp = dbsNorthwind.OpenRecordset( _ 
 "Employees", dbOpenTable) 
 Debug.Print " Transactions = " & rstTemp.Transactions 
 
 Debug.Print "Opening forward-only-type " & _ 
 "recordset where the source is an SQL statement..." 
 Set rstTemp = dbsNorthwind.OpenRecordset( _ 
 "SELECT * FROM Employees", dbOpenForwardOnly) 
 Debug.Print " Transactions = " & rstTemp.Transactions 
 
 rstTemp.Close 
 dbsNorthwind.Close 
 conPubs.Close 
 wrkAcc.Close 
End Sub 
 
```

