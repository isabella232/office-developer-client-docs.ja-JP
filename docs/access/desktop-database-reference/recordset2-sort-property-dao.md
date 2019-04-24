---
title: Recordset2 プロパティ (DAO)
TOCTitle: Sort Property
ms:assetid: 523a8c29-46e2-564f-205d-03c214f277fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193917(v=office.15)
ms:contentKeyID: 48544842
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a5784054ce195a1a2ea516d4f6a3417c5a8db71c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309270"
---
# <a name="recordset2sort-property-dao"></a><span data-ttu-id="dc816-102">Recordset2 プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="dc816-102">Recordset2.Sort property (DAO)</span></span>

<span data-ttu-id="dc816-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="dc816-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="dc816-104">**[Recordset](recordset-object-dao.md)** オブジェクト内のレコードの並べ替え順序を設定または取得します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="dc816-104">Sets or returns the sort order for records in a **[Recordset](recordset-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="dc816-105">構文</span><span class="sxs-lookup"><span data-stu-id="dc816-105">Syntax</span></span>

<span data-ttu-id="dc816-106">*式*。モダン</span><span class="sxs-lookup"><span data-stu-id="dc816-106">*expression* .Sort</span></span>

<span data-ttu-id="dc816-107">\*式\***Recordset2**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="dc816-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc816-108">注釈</span><span class="sxs-lookup"><span data-stu-id="dc816-108">Remarks</span></span>

<span data-ttu-id="dc816-109">**Sort** プロパティは、ダイナセット タイプおよびスナップショット タイプの **Recordset** オブジェクトで使用できます。</span><span class="sxs-lookup"><span data-stu-id="dc816-109">You can use the **Sort** property with dynaset– and snapshot–type **Recordset** objects.</span></span>

<span data-ttu-id="dc816-p101">オブジェクトに対してこのプロパティを設定すると、それ以降にそのオブジェクトから **Recordset** オブジェクトを作成するときに、レコードが並べ替えられます。 **Sort** プロパティの設定値は、 **[QueryDef](querydef-object-dao.md)** オブジェクトに指定されているいずれの並べ替え順序よりも優先されます。</span><span class="sxs-lookup"><span data-stu-id="dc816-p101">When you set this property for an object, sorting occurs when a subsequent **Recordset** object is created from that object. The **Sort** property setting overrides any sort order specified for a **[QueryDef](querydef-object-dao.md)** object.</span></span>

<span data-ttu-id="dc816-112">既定の並べ替え順序は、昇順 (A ～ Z、0 ～ 100、あ～ん) です。</span><span class="sxs-lookup"><span data-stu-id="dc816-112">The default sort order is ascending (A to Z or 0 to 100).</span></span>

<span data-ttu-id="dc816-113">**Sort** プロパティは、テーブル タイプまたは前方スクロール タイプの **Recordset** オブジェクトには適用されません。</span><span class="sxs-lookup"><span data-stu-id="dc816-113">The **Sort** property doesn't apply to table– or forward–only–type **Recordset** objects.</span></span> <span data-ttu-id="dc816-114">テーブルタイプの**Recordset**オブジェクトを並べ替えるには、 **[Index](recordset2-index-property-dao.md)** プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="dc816-114">To sort a table–type **Recordset** object, use the **[Index](recordset2-index-property-dao.md)** property.</span></span>

> [!NOTE]
> <span data-ttu-id="dc816-115">多くの場合、並べ替え条件を含む SQL ステートメントを使用すると、新規の **Recordset** オブジェクトをより短時間で開くことができます。</span><span class="sxs-lookup"><span data-stu-id="dc816-115">In many cases, it's faster to open a new **Recordset** object by using an SQL statement that includes the sorting criteria.</span></span>

## <a name="example"></a><span data-ttu-id="dc816-116">例</span><span class="sxs-lookup"><span data-stu-id="dc816-116">Example</span></span>

<span data-ttu-id="dc816-p103">次の例では、 **Sort** プロパティの値を変更して新規の **Recordset** を作成することで、このプロパティの機能を示します。このプロシージャを実行するには、SortOutput 関数が必要です。</span><span class="sxs-lookup"><span data-stu-id="dc816-p103">This example demonstrates the **Sort** property by changing its value and creating a new **Recordset**. The SortOutput function is required for this procedure to run.</span></span>

```vb
    Sub SortX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     Dim rstSortEmployees As Recordset2 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     With rstEmployees 
     SortOutput "Original Recordset:", rstEmployees 
     .Sort = "LastName, FirstName" 
     ' Print report showing Sort property and record order. 
     SortOutput _ 
     "Recordset after changing Sort property:", _ 
     rstEmployees 
     ' Open new Recordset from current one. 
     Set rstSortEmployees = .OpenRecordset 
     ' Print report showing Sort property and record order. 
     SortOutput "New Recordset:", rstSortEmployees 
     rstSortEmployees.Close 
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function SortOutput(strTemp As String, _ 
     rstTemp As Recordset) 
     
     With rstTemp 
     Debug.Print strTemp 
     Debug.Print " Sort = " & _ 
     IIf(.Sort <> "", .Sort, "[Empty]") 
     .MoveFirst 
     
     ' Enumerate Recordset. 
     Do While Not .EOF 
     Debug.Print " " & !LastName & _ 
     ", " & !FirstName 
     .MoveNext 
     Loop 
     
     End With 
     
    End Function 
```

<br/>

<span data-ttu-id="dc816-p104">選択するデータがわかっている場合は、SQL ステートメントを使用して **Recordset** を作成する方が一般に効率的です。次の例では、ただ 1 つの **Recordset** を作成して、前の例と同じ結果を得る方法を示します。</span><span class="sxs-lookup"><span data-stu-id="dc816-p104">When you know the data you want to select, it's usually more efficient to create a **Recordset** with an SQL statement. This example shows how you can create just one **Recordset** and obtain the same results as in the preceding example.</span></span>

```vb
    Sub SortX2() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     ' Open a Recordset from an SQL statement that specifies a 
     ' sort order. 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("SELECT * " & _ 
     "FROM Employees ORDER BY LastName, FirstName", _ 
     dbOpenDynaset) 
     
     dbsNorthwind.Close 
     
    End Sub
```
