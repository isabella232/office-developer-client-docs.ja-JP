---
title: 任意のレコードにジャンプする
TOCTitle: Jumping to a Record
ms:assetid: 27177bbe-066c-aeb0-6dfd-45d8c2a87487
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249033(v=office.15)
ms:contentKeyID: 48543829
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d12ab7bedd58743eb7545ed8b0b8b585ab2ea217
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478006"
---
# <a name="jumping-to-a-record"></a><span data-ttu-id="042fa-102">任意のレコードにジャンプする</span><span class="sxs-lookup"><span data-stu-id="042fa-102">Jumping to a Record</span></span>


<span data-ttu-id="042fa-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="042fa-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="042fa-104">次の構文で [Move](move-method-ado.md) メソッドを使用すると、 **Recordset** 内を指定した数の分だけ前後に移動できます。</span><span class="sxs-lookup"><span data-stu-id="042fa-104">The [Move](move-method-ado.md) method allows you to move forward or backward in the **Recordset** a specified number of records by using the following syntax:</span></span>

```vb 
 
oRs.Move NumRecords, Start
```

<span data-ttu-id="042fa-105">**Move** メソッドは、すべての **Recordset** オブジェクトでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="042fa-105">The **Move** method is supported on all **Recordset** objects.</span></span>

<span data-ttu-id="042fa-p101">*NumRecords* 引数がゼロより大きい場合、現在のレコードの位置は前方 (**Recordset** の末尾方向) に移動します。*NumRecords* がゼロより小さい場合、現在のレコードの位置は後方 (**Recordset** の先頭方向) に移動します。</span><span class="sxs-lookup"><span data-stu-id="042fa-p101">If the *NumRecords* argument is greater than zero, the current record position moves forward (toward the end of the **Recordset**). If *NumRecords* is less than zero, the current record position moves backward (toward the beginning of the **Recordset**).</span></span>

<span data-ttu-id="042fa-p102">**Move** の呼び出しにより、現在のレコードの位置が先頭のレコードよりも前に移動した場合、現在のレコードの位置は、**Recordset** 内の先頭のレコードの前に設定されます (**BOF** が **True** になる)。**BOF** プロパティが既に **True** の場合、後方に移動しようとするとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="042fa-p102">If the **Move** call would move the current record position to a point before the first record, ADO sets the current record to the position before the first record in the **Recordset** (**BOF** is **True**). An attempt to move backward when the **BOF** property is already **True** generates an error.</span></span>

<span data-ttu-id="042fa-p103">**Move** の呼び出しにより、現在のレコードの位置が最後のレコードよりも後に移動した場合、現在のレコードの位置は、**Recordset** 内の最後のレコードの後に設定されます (**EOF** が **True** になる)。**EOF** プロパティが既に **True** の場合、前方に移動しようとするとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="042fa-p103">If the **Move** call would move the current record position to a point after the last record, ADO sets the current record to the position after the last record in the **Recordset** (**EOF** is **True**). An attempt to move forward when the **EOF** property is already **True** generates an error.</span></span>

<span data-ttu-id="042fa-112">空の **Recordset** オブジェクトから **Move** メソッドを呼び出すと、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="042fa-112">Calling the **Move** method from an empty **Recordset** object generates an error.</span></span>

<span data-ttu-id="042fa-113">引数*Start*でブックマークを指定した場合、移動は、 **Recordset**オブジェクトがブックマークをサポートするいると仮定して、このブックマークを持つレコードを基準にしてが。</span><span class="sxs-lookup"><span data-stu-id="042fa-113">If you pass a bookmark in the *Start* argument, the move is relative to the record with this bookmark, assuming the **Recordset** object supports bookmarks.</span></span> <span data-ttu-id="042fa-114">ブックマークは、 [Bookmark](bookmark-property-ado.md) プロパティを使用して取得します。</span><span class="sxs-lookup"><span data-stu-id="042fa-114">A bookmark is obtained by using the [Bookmark](bookmark-property-ado.md) property.</span></span> <span data-ttu-id="042fa-115">引数を指定しない場合は、現在のレコードを基準にして移動します。</span><span class="sxs-lookup"><span data-stu-id="042fa-115">If not specified, the move is relative to the current record.</span></span>

<span data-ttu-id="042fa-116">*NumRecords*引数を現在のレコード位置が現在キャッシュされているレコード グループの範囲外に移動する、プロバイダーからのレコードをローカルにキャッシュ、 **CacheSize**プロパティを使用する場合、レコードの新しいグループを取得するために ADO を強制的に移動先のレコードから開始しています。</span><span class="sxs-lookup"><span data-stu-id="042fa-116">If you are using the **CacheSize** property to locally cache records from the provider, passing a *NumRecords* argument that moves the current record position outside the current group of cached records forces ADO to retrieve a new group of records, starting from the destination record.</span></span> <span data-ttu-id="042fa-117">**CacheSize** プロパティが、新規に取得されるグループのサイズを決定し、移動先のレコードが最初に取得されるレコードになります。</span><span class="sxs-lookup"><span data-stu-id="042fa-117">The **CacheSize** property determines the size of the newly retrieved group, and the destination record is the first record retrieved.</span></span>

