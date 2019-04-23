---
title: レコードセットでのその他の移動方法
TOCTitle: More ways to move in a Recordset
ms:assetid: ae49b20e-0050-c44b-67e9-7e39de5098c4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249822(v=office.15)
ms:contentKeyID: 48547067
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2d10a493aac39934a047c6fa311233fd6c9fac4e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288863"
---
# <a name="more-ways-to-move-in-a-recordset"></a><span data-ttu-id="f3a97-102">レコードセットでのその他の移動方法</span><span class="sxs-lookup"><span data-stu-id="f3a97-102">More ways to move in a Recordset</span></span>

<span data-ttu-id="f3a97-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="f3a97-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f3a97-p101">**MoveFirst、MoveLast、MoveNext、および MovePrevious** の 4 つのメソッドを使用すると、 [Recordset](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) 内を移動またはスクロールできます (前方スクロール カーソルでは使用できないメソッドもあります)。</span><span class="sxs-lookup"><span data-stu-id="f3a97-p101">The following four methods are used to move around, or scroll, in the **Recordset**: [MoveFirst, MoveLast, MoveNext, and MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md). (Some of these methods are unavailable on forward-only cursors.)</span></span>

<span data-ttu-id="f3a97-p102">**MoveFirst** は、現在のレコードの位置を **Recordset** 内の最初のレコードに変更します。 **MoveLast** は、現在のレコードの位置を **Recordset** 内の最後のレコードに変更します。 **MoveFirst** または **MoveLast** を使用するには、 **Recordset** オブジェクトがブックマークまたは後方スクロール カーソルの移動をサポートしている必要があります。それ以外の場合にメソッドを呼び出すと、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f3a97-p102">**MoveFirst** changes the current record position to the first record in the **Recordset**. **MoveLast** changes the current record position to the last record in the **Recordset**. To use **MoveFirst** or **MoveLast**, the **Recordset** object must support bookmarks or backward cursor movement; otherwise, the method call will generate an error.</span></span>

<span data-ttu-id="f3a97-p103">**MoveNext** は、現在のレコードの位置を 1 つ進めます。最後のレコードで **MoveNext** を呼び出すと、 **EOF** が **True** に設定されます。 **MovePrevious** は、現在のレコードの位置を 1 つ戻します。最初のレコードで **MovePrevious** を呼び出すと、 **BOF** が **True** に設定されます。次に示すように、これらのメソッドを使用するときには、 **EOF** プロパティと **BOF** プロパティを調べ、 **Recordset** のいずれかの端を超えたときには、カーソルを有効な現在のレコードの位置に戻します。</span><span class="sxs-lookup"><span data-stu-id="f3a97-p103">**MoveNext** moves the current record position one place forward. If you are on the last record when you call **MoveNext**, **EOF** will be set to **True**. **MovePrevious** moves the current record position one place backward. If you are on the first record when you call **MovePrevious**, **BOF** will be set to **True**. It is wise to check the **EOF** and **BOF** properties when using these methods and to move the cursor back to a valid current record position if you move off either end of the **Recordset**, as shown here:</span></span>

```vb
. . . 
oRs.MoveNext 
If oRs.EOF Then oRs.MoveLast 
. . . 
```

<span data-ttu-id="f3a97-114">**MovePrevious** メソッドの場合は、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="f3a97-114">Or, in the case of the **MovePrevious** method:</span></span>

```vb
. . . 
oRs.MovePrevious 
If oRs.BOF Then oRs.MoveFirst 
. . . 
```

<span data-ttu-id="f3a97-115">フィルター処理または並べ替えが行われた **Recordset** で現在のレコードのデータを変更すると、その位置も変更されることがあります。</span><span class="sxs-lookup"><span data-stu-id="f3a97-115">In cases where the **Recordset** has been filtered or sorted and the current record's data is changed, the position may also change.</span></span> <span data-ttu-id="f3a97-116">その場合、 **MoveNext** メソッドは正常に動作しますが、その位置が、元の位置からではなく、変更後の位置から 1 つ前に移動されることに注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3a97-116">In such cases the **MoveNext** method works normally, but be aware that the position is moved one record forward from the new position, not the old position.</span></span> <span data-ttu-id="f3a97-117">たとえば、レコードが並べ替えられた**Recordset**の末尾に移動されるように、現在のレコードのデータを変更すると、ADO で**MoveNext**の結果を呼び出したときに、現在のレコードの最後のレコード**の位置をRecordset** (**EOF** = **True**)。</span><span class="sxs-lookup"><span data-stu-id="f3a97-117">For example, changing the data in the current record, such that the record is moved to the end of the sorted **Recordset**, would mean that calling **MoveNext** results in ADO setting the current record to the position after the last record in the **Recordset** (**EOF** = **True**).</span></span>

<span data-ttu-id="f3a97-p105">**Recordset** オブジェクトのさまざまな Move メソッドの動作は、 **Recordset** 内のデータによってある程度異なります。 **Recordset** に追加された新規レコードは、最初はデータ ソースで定義され、新規レコードのデータに暗黙的または明示的に依存する特定の順序で追加されます。たとえば、 **Recordset** を設定するクエリで並べ替えまたは結合を実行すると、 **Recordset** 内の該当する位置に新規レコードが挿入されます。 **Recordset** の作成時に順序が明示的に指定されていない場合、データ ソースの実装を変更すると、返される行の順序が予期せずに変更されることがあります。さらに、 **Recordset** の並べ替え、フィルター、および編集機能は順序にも影響し、表示されるレコードセットの行にも影響する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f3a97-p105">The behavior of the various Move methods of the **Recordset** object depends, to some extent, on the data within the **Recordset**. New records added to the **Recordset** are initially added in a particular order, which is defined by the data source and may be dependent implicitly or explicitly on the data in the new record. For example, if a sort or a join is done within the query that populates the **Recordset**, the new record will be inserted in the appropriate place within the **Recordset**. If ordering is not explicitly specified when creating the **Recordset**, changes in the data source implementation may cause the ordering of the returned rows to change inadvertently. In addition, the sorting, filtering, and editing functions of the **Recordset** can affect the order and possibly which rows in the recordset will be visible.</span></span>

<span data-ttu-id="f3a97-p106">したがって、 **MoveNext** 、 **MovePrevious** 、 **MoveFirst** 、 **MoveLast** 、および **Move** の各メソッドはすべて、同じ **Recordset** で行われるその他の操作に影響されることがあります。ADO は明示的に移動されるまで現在の位置を維持しようとしますが、途中で変更すると、その後の移動の結果を考えるのが難しくなります。たとえば、 **MoveFirst** を呼び出して、並べ替えられた **Recordset** の最初の行に移動し、並べ替えの順序を昇順から降順に変更すると、同じ行が表示されていますが、それは **Recordset** の最後の行になっています。 **MoveFirst** を使用すると、別の行 (変更後の最初の行) に移動します。</span><span class="sxs-lookup"><span data-stu-id="f3a97-p106">Therefore, **MoveNext**, **MovePrevious**, **MoveFirst**, **MoveLast**, and **Move** are all sensitive to other operations performed on the same **Recordset**. ADO will always try to maintain your current position until you explicitly move it, but sometimes intervening changes make it difficult to understand the effects of a subsequent move. For example, if you call **MoveFirst** to position on the first row of a sorted **Recordset** and you change the sort from ascending order to descending order, you are still on the same row — but now it is the last row in the **Recordset**. **MoveFirst** will take you to a different row (the new first row).</span></span>

<span data-ttu-id="f3a97-p107">別の例として、 **Recordset** の途中にある特定の行で、 **Delete** を呼び出してから **MoveNext** を呼び出すと、削除されたレコードのすぐ次のレコードが表示されます。そこで **MovePrevious** を呼び出すと、削除されたレコードは、 **Recordset** のアクティブなメンバーシップとして数えられなくなるため、現在のレコードは、削除したレコードの前のレコードになります。</span><span class="sxs-lookup"><span data-stu-id="f3a97-p107">As another example, if you are positioned on a particular row in the middle of a **Recordset** and you call **Delete** and then call **MoveNext**, you are now on the record immediately following the deleted record. But calling **MovePrevious** makes the record preceding the one you deleted the current record, because the deleted record is no longer counted in the active membership of the **Recordset**.</span></span>

<span data-ttu-id="f3a97-p108">現在のレコードを基準にして相対的に移動するメソッド (**MovePrevious**、**MoveNext**、および **Move**) について、現在のレコードでデータを変更した場合の移動の形式を、すべてのプロバイダーで一貫して定義するのはたいへん困難です。たとえば、並べ替えおよびフィルター処理が行われた **Recordset** で、現在のレコードがその他のすべてのレコードより前になるようにデータを変更したが、変更したデータがフィルターに一致しなくなった場合、**MoveNext** 操作による移動先は予期できません。レコードの編集、追加、または削除中にデータを変更する場合は、**Recordset** 内を相対的に移動する方が、**MoveFirst** や **MoveLast** を使用して絶対的に移動するよりも危険です。主キーまたは ID は値が変わらないため、並べ替えおよびフィルターは、これらの値に基づいて行ってください。</span><span class="sxs-lookup"><span data-stu-id="f3a97-p108">It is particularly difficult to define consistent move semantics across all providers for methods that move relative to the current record — **MovePrevious**, **MoveNext**, and **Move** — in the face of changing data in the current record. For example, if you are working with a sorted, filtered **Recordset**, and you change the data in the current record so that it would precede all other records, but your changed data also no longer matches the filter, it is not clear where a **MoveNext** operation should take you. The safest conclusion is that relative movement within a **Recordset** is riskier than absolute movement (such as using **MoveFirst** or **MoveLast**) when the data is changing while records are being edited, added, or deleted. Sorting and filtering should be based on a primary key or ID, because this type of value should not change.</span></span>

