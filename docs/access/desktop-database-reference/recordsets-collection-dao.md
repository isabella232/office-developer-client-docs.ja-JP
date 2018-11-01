---
title: Recordsets コレクション (DAO)
TOCTitle: Recordsets Collection
ms:assetid: 246d9a78-4ce8-6393-982b-77ac00cd85bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191819(v=office.15)
ms:contentKeyID: 48543756
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1a32c52f60ed8c7bd68f32ed9986638bffcdec84
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869002"
---
# <a name="recordsets-collection-dao"></a><span data-ttu-id="b814d-102">Recordsets コレクション (DAO)</span><span class="sxs-lookup"><span data-stu-id="b814d-102">Recordsets Collection (DAO)</span></span>

<span data-ttu-id="b814d-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="b814d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b814d-104">**Recordsets** コレクションには、 **Connection** または **Database** オブジェクト内のすべての開いている **Recordset** オブジェクトが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b814d-104">A **Recordsets** collection contains all open **Recordset** objects in a **Connection** or **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b814d-105">注釈</span><span class="sxs-lookup"><span data-stu-id="b814d-105">Remarks</span></span>

<span data-ttu-id="b814d-106">DAO オブジェクトを使用する場合は、 **Recordset** オブジェクトを使用してほぼすべてのデータを操作します。</span><span class="sxs-lookup"><span data-stu-id="b814d-106">When you use DAO objects, you manipulate data almost entirely using **Recordset** objects.</span></span>

<span data-ttu-id="b814d-107">新しい **Recordset** オブジェクトは、 **Recordset** オブジェクトを開いたときに **Recordsets** コレクションに自動的に追加され、オブジェクトを閉じたときに自動的に削除されます。</span><span class="sxs-lookup"><span data-stu-id="b814d-107">A new **Recordset** object is automatically added to the **Recordsets** collection when you open the **Recordset** object, and is automatically removed when you close it.</span></span>

<span data-ttu-id="b814d-p101">**Recordset** オブジェクト変数は必要な数だけ作成できます。異なる **Recordset** オブジェクトでも、競合せずに同じテーブル、クエリ、およびフィールドにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="b814d-p101">You can create as many **Recordset** object variables as needed. Different **Recordset** objects can access the same tables, queries, and fields without conflicting.</span></span>

<span data-ttu-id="b814d-110">コレクション内の **Recordset** オブジェクトを、コレクションで付けられたインデックスまたは **Name** プロパティの設定値で参照するには、次のいずれかの構文を使います。</span><span class="sxs-lookup"><span data-stu-id="b814d-110">To refer to a **Recordset** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="b814d-111">**Recordsets**(0)</span><span class="sxs-lookup"><span data-stu-id="b814d-111">**Recordsets**(0)</span></span>

- <span data-ttu-id="b814d-112">**レコード セット**("name")</span><span class="sxs-lookup"><span data-stu-id="b814d-112">**Recordsets**("name")</span></span>

- <span data-ttu-id="b814d-113">**レコード セット**\!\[名\]</span><span class="sxs-lookup"><span data-stu-id="b814d-113">**Recordsets**\!\[name\]</span></span>

> [!NOTE]
> <span data-ttu-id="b814d-p102">[!メモ] 同じデータ ソースまたはデータベースから **Recordset** オブジェクトを複数回開いて、 **Recordsets** コレクションに重複する名前を作成できます。 **Recordset** オブジェクトをオブジェクト変数に割り当て、変数名で参照する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b814d-p102">You can open a **Recordset** object from the same data source or database more than once, creating duplicate names in the **Recordsets** collection. You should assign **Recordset** objects to object variables and refer to them by variable name.</span></span>

## <a name="example"></a><span data-ttu-id="b814d-116">例</span><span class="sxs-lookup"><span data-stu-id="b814d-116">Example</span></span>

<span data-ttu-id="b814d-117">次の使用例は、4 種類の **Recordset** オブジェクトを開き、現在の **Recordsets** オブジェクトの Recordsets コレクションを列挙して、各 **Recordsets** オブジェクトの **Database** コレクションを列挙することで、 **Properties** オブジェクトおよび **Recordset** コレクションを示します。</span><span class="sxs-lookup"><span data-stu-id="b814d-117">This example demonstrates **Recordset** objects and the **Recordsets** collection by opening four different types of **Recordsets**, enumerating the Recordsets collection of the current **Database**, and enumerating the **Properties** collection of each **Recordset**.</span></span>

```vb
    Sub RecordsetX() 
     
     Dim dbsNorthwind As Database 
     Dim rstTable As Recordset 
     Dim rstDynaset As Recordset 
     Dim rstSnapshot As Recordset 
     Dim rstForwardOnly As Recordset 
     Dim rstLoop As Recordset 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     
     ' Open one of each type of Recordset object. 
     Set rstTable = .OpenRecordset("Categories", _ 
     dbOpenTable) 
     Set rstDynaset = .OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     Set rstSnapshot = .OpenRecordset("Shippers", _ 
     dbOpenSnapshot) 
     Set rstForwardOnly = .OpenRecordset _ 
     ("Employees", dbOpenForwardOnly) 
     
     Debug.Print "Recordsets in Recordsets " & _ 
     "collection of dbsNorthwind" 
     
     ' Enumerate Recordsets collection. 
     For Each rstLoop In .Recordsets 
     
     With rstLoop 
     Debug.Print " " & .Name 
     
     ' Enumerate Properties collection of each 
     ' Recordset object. Trap for any 
     ' properties whose values are invalid in 
     ' this context. 
     For Each prpLoop In .Properties 
     On Error Resume Next 
     If prpLoop <> "" Then Debug.Print _ 
     " " & prpLoop.Name & _ 
     " = " & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     End With 
     
     Next rstLoop 
     
     rstTable.Close 
     rstDynaset.Close 
     rstSnapshot.Close 
     rstForwardOnly.Close 
     
     .Close 
     End With 
     
    End Sub
```
