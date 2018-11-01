---
title: Recordset.Transactions プロパティ (DAO)
TOCTitle: Transactions Property
ms:assetid: 7830c056-8d6a-7942-7993-aa04b29cd77f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196110(v=office.15)
ms:contentKeyID: 48545746
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c3b34f8f027b2e70ada94c6d15584cf25a4aec1c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873293"
---
# <a name="recordsettransactions-property-dao"></a><span data-ttu-id="54609-102">Recordset.Transactions プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="54609-102">Recordset.Transactions Property (DAO)</span></span>


<span data-ttu-id="54609-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="54609-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="54609-p101">オブジェクトがトランザクションをサポートしているかどうかを示す値を取得します。値の取得のみ可能です。ブール型 ( **Boolean**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="54609-p101">Returns a value that indicates whether an object supports transactions. Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="54609-106">構文</span><span class="sxs-lookup"><span data-stu-id="54609-106">Syntax</span></span>

<span data-ttu-id="54609-107">*式*です。トランザクション</span><span class="sxs-lookup"><span data-stu-id="54609-107">*expression* .Transactions</span></span>

<span data-ttu-id="54609-108">\*式\***レコード セット**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="54609-108">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="54609-109">注釈</span><span class="sxs-lookup"><span data-stu-id="54609-109">Remarks</span></span>

<span data-ttu-id="54609-110">Microsoft Access ワークスペースでは、ダイナセット タイプまたはテーブル タイプの **Recordset** オブジェクトでも **Transactions** プロパティを使用できます。</span><span class="sxs-lookup"><span data-stu-id="54609-110">In a Microsoft Access workspace, you can also use the **Transactions** property with dynaset- or table-type **Recordset** objects.</span></span> <span data-ttu-id="54609-111">スナップショット- および前方のみタイプの**[Recordset](recordset-object-dao.md)** オブジェクトは常に**False**を返します。</span><span class="sxs-lookup"><span data-stu-id="54609-111">Snapshot- and forward–only–type **[Recordset](recordset-object-dao.md)** objects always return **False**.</span></span>

<span data-ttu-id="54609-p103">ダイナセット タイプまたはテーブル タイプの **Recordset** が Microsoft Access データベース エンジン テーブルに基づいている場合、 **Transactions** プロパティは **True** となるため、トランザクションを使用できます。他のデータベース エンジンでは、トランザクションがサポートされていないことがあります。たとえば、Paradox テーブルに基づくダイナセット タイプの **Recordset** オブジェクトでは、トランザクションを使用できません。</span><span class="sxs-lookup"><span data-stu-id="54609-p103">If a dynaset- or table-type **Recordset** is based on a Microsoft Access database engine table, the **Transactions** property is **True** and you can use transactions. Other database engines may not support transactions. For example, you can't use transactions in a dynaset-type **Recordset** object based on a Paradox table.</span></span>

<span data-ttu-id="54609-p104">**Recordset** オブジェクトの **[Workspace](dbengine-begintrans-method-dao.md)** オブジェクトで [**BeginTrans**](workspace-object-dao.md) メソッドを使用する前に、 **Transactions** プロパティでトランザクションがサポートされているかどうかを確認してください。トランザクションがサポートされていないオブジェクト上で **BeginTrans**、 **CommitTrans**、または **Rollback** の各メソッドを使用しても、何も変化しません。</span><span class="sxs-lookup"><span data-stu-id="54609-p104">Check the **Transactions** property before using the **[BeginTrans](dbengine-begintrans-method-dao.md)** method on the **Recordset** object's **[Workspace](workspace-object-dao.md)** object to make sure that transactions are supported. Using the **BeginTrans**, **CommitTrans**, or **Rollback** methods on an unsupported object has no effect.</span></span>

## <a name="example"></a><span data-ttu-id="54609-117">例</span><span class="sxs-lookup"><span data-stu-id="54609-117">Example</span></span>

<span data-ttu-id="54609-118">次の例では、Microsoft Access ワークスペースでの **Transactions** プロパティの機能を示します。</span><span class="sxs-lookup"><span data-stu-id="54609-118">This example demonstrates the **Transactions** property in Microsoft Access workspaces.</span></span>

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

