---
title: Recordset2.RecordCount プロパティ (DAO)
TOCTitle: RecordCount Property
ms:assetid: 77852966-11e9-1773-6e58-53927b84c03b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196071(v=office.15)
ms:contentKeyID: 48545728
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052890
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 999cebd7fa038d3efeeac963ba6844545a41373a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479565"
---
# <a name="recordset2recordcount-property-dao"></a><span data-ttu-id="d85fc-102">Recordset2.RecordCount プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="d85fc-102">Recordset2.RecordCount Property (DAO)</span></span>


<span data-ttu-id="d85fc-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="d85fc-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d85fc-p101">**[Recordset](recordset-object-dao.md)** オブジェクト内のアクセス済みのレコード数、またはテーブル タイプの **Recordset** オブジェクト、あるいは **[TableDef](tabledef-object-dao.md)** オブジェクトの合計レコード数を取得します。値の取得のみ可能です。長整数型 ( **Long**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="d85fc-p101">Returns the number of records accessed in a **[Recordset](recordset-object-dao.md)** object, or the total number of records in a table-type **Recordset** object. or **[TableDef](tabledef-object-dao.md)** object. Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d85fc-107">構文</span><span class="sxs-lookup"><span data-stu-id="d85fc-107">Syntax</span></span>

<span data-ttu-id="d85fc-108">*式*です。RecordCount</span><span class="sxs-lookup"><span data-stu-id="d85fc-108">*expression* .RecordCount</span></span>

<span data-ttu-id="d85fc-109">\*式\***Recordset2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="d85fc-109">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d85fc-110">注釈</span><span class="sxs-lookup"><span data-stu-id="d85fc-110">Remarks</span></span>

<span data-ttu-id="d85fc-111">**RecordCount** プロパティを使用して、 **Recordset** オブジェクトまたは **TableDef** オブジェクトのアクセス済みのレコード数を調べます。</span><span class="sxs-lookup"><span data-stu-id="d85fc-111">Use the **RecordCount** property to find out how many records in a **Recordset** or **TableDef** object have been accessed.</span></span> <span data-ttu-id="d85fc-112">ダイナセット タイプ、スナップショット タイプまたは前方のみタイプの**Recordset**オブジェクトでレコードの数が含まれているすべてのレコードがアクセス済みになるまで**RecordCount**プロパティに示されません。</span><span class="sxs-lookup"><span data-stu-id="d85fc-112">The **RecordCount** property doesn't indicate how many records are contained in a dynaset–, snapshot–, or forward–only–type **Recordset** object until all records have been accessed.</span></span> <span data-ttu-id="d85fc-113">最後のレコードにアクセスすると、 **Recordset** オブジェクトまたは **TableDef** オブジェクトにある、削除されていないレコードの合計数が **RecordCount** プロパティに示されます。</span><span class="sxs-lookup"><span data-stu-id="d85fc-113">Once the last record has been accessed, the **RecordCount** property indicates the total number of undeleted records in the **Recordset** or **TableDef** object.</span></span> <span data-ttu-id="d85fc-114">最後のレコードを強制的にアクセス済みにするには、 [Recordset](recordset2-movelast-method-dao.md) オブジェクトに対して \*\*\*\*MoveLast\*\*\*\* メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="d85fc-114">To force the last record to be accessed, use the **[MoveLast](recordset2-movelast-method-dao.md)** method on the **Recordset** object.</span></span> <span data-ttu-id="d85fc-115">また、SQL の **Count** 関数を使用して、クエリから返される概算のレコード数を調べることもできます。</span><span class="sxs-lookup"><span data-stu-id="d85fc-115">You can also use an SQL **Count** function to determine the approximate number of records your query will return.</span></span>


> [!NOTE]
> <P><span data-ttu-id="d85fc-p103">[!メモ] 新しく開いた <STRONG>Recordset</STRONG> オブジェクトに、 <STRONG>MoveLast</STRONG> メソッドを使用して値を設定するとパフォーマンスが低下します。 <STRONG>Recordset</STRONG> を開いた直後に正確な <STRONG>RecordCount</STRONG> プロパティの値が必要な場合を除き、コードの他の部分で <STRONG>Recordset</STRONG> オブジェクトに値が設定されるまで待機してから、 <STRONG>RecordCount</STRONG> プロパティを確認することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d85fc-p103">Using the <STRONG>MoveLast</STRONG> method to populate a newly opened <STRONG>Recordset</STRONG> negatively impacts performance. Unless it is necessary to have an accurate <STRONG>RecordCount</STRONG> as soon as you open a <STRONG>Recordset</STRONG>, it's better to wait until you populate the <STRONG>Recordset</STRONG> with other portions of code before checking the <STRONG>RecordCount</STRONG> property.</span></span></P>



<span data-ttu-id="d85fc-p104">ダイナセット タイプの **Recordset** オブジェクトにあるレコードをアプリケーションで削除すると、 **RecordCount** プロパティの値が減少します。ただし、他のユーザーが削除したレコードは、カレント レコードがその削除済みのレコードに移動するまで **RecordCount** プロパティに反映されません。 **RecordCount** プロパティの設定値に影響を与えるトランザクションを実行し、後でそのトランザクションをロールバックすると、残っているレコードの実際の数が **RecordCount** プロパティに反映されません。</span><span class="sxs-lookup"><span data-stu-id="d85fc-p104">As your application deletes records in a dynaset-type **Recordset** object, the value of the **RecordCount** property decreases. However, records deleted by other users aren't reflected by the **RecordCount** property until the current record is positioned to a deleted record. If you execute a transaction that affects the **RecordCount** property setting and you subsequently roll back the transaction, the **RecordCount** property won't reflect the actual number of remaining records.</span></span>

<span data-ttu-id="d85fc-121">スナップショット: または前方のみタイプの**Recordset**オブジェクトの**RecordCount**プロパティは、基になるテーブルの変更の影響を受けません。</span><span class="sxs-lookup"><span data-stu-id="d85fc-121">The **RecordCount** property of a snapshot– or forward–only–type **Recordset** object isn't affected by changes in the underlying tables.</span></span>

<span data-ttu-id="d85fc-122">レコードが格納されていない **Recordset** オブジェクトおよび **TableDef** オブジェクトは、 **RecordCount** プロパティが 0 に設定されます。</span><span class="sxs-lookup"><span data-stu-id="d85fc-122">A **Recordset** or **TableDef** object with no records has a **RecordCount** property setting of 0.</span></span>

<span data-ttu-id="d85fc-123">[Recordset](recordset2-requery-method-dao.md) オブジェクトに対して \*\*\*\*Requery\*\*\*\* メソッドを使用すると、クエリがもう一度実行された場合と同じ設定値に **RecordCount** プロパティが再設定されます。</span><span class="sxs-lookup"><span data-stu-id="d85fc-123">Using the **[Requery](recordset2-requery-method-dao.md)** method on a **Recordset** object resets the **RecordCount** property just as if the query were re-executed.</span></span>

## <a name="example"></a><span data-ttu-id="d85fc-124">例</span><span class="sxs-lookup"><span data-stu-id="d85fc-124">Example</span></span>

<span data-ttu-id="d85fc-125">以下の使用例は、さまざまな種類の **Recordsets** オブジェクトに値を設定する前と後の **RecordCount** プロパティの値を示します。</span><span class="sxs-lookup"><span data-stu-id="d85fc-125">This example demonstrates the **RecordCount** property with different types of **Recordsets** before and after they're populated.</span></span>

```vb
    Sub RecordCountX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Open table-type Recordset and show RecordCount 
     ' property. 
     Set rstEmployees = .OpenRecordset("Employees") 
     Debug.Print _ 
     "Table-type recordset from Employees table" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     ' Open dynaset-type Recordset and show RecordCount 
     ' property before populating the Recordset. 
     Set rstEmployees = .OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     Debug.Print "Dynaset-type recordset " & _ 
     "from Employees table before MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     
     ' Show the RecordCount property after populating the 
     ' Recordset. 
     rstEmployees.MoveLast 
     Debug.Print "Dynaset-type recordset " & _ 
     "from Employees table after MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     ' Open snapshot-type Recordset and show RecordCount 
     ' property before populating the Recordset. 
     Set rstEmployees = .OpenRecordset("Employees", _ 
     dbOpenSnapshot) 
     Debug.Print "Snapshot-type recordset " & _ 
     "from Employees table before MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     
     ' Show the RecordCount property after populating the 
     ' Recordset. 
     rstEmployees.MoveLast 
     Debug.Print "Snapshot-type recordset " & _ 
     "from Employees table after MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     ' Open forward-only-type Recordset and show 
     ' RecordCount property before populating the 
     ' Recordset. 
     Set rstEmployees = .OpenRecordset("Employees", _ 
     dbOpenForwardOnly) 
     Debug.Print "Forward-only-type recordset " & _ 
     "from Employees table before MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     
     ' Show the RecordCount property after calling the 
     ' MoveNext method. 
     rstEmployees.MoveNext 
     Debug.Print "Forward-only-type recordset " & _ 
     "from Employees table after MoveNext" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     .Close 
     End With 
     
    End Sub
```