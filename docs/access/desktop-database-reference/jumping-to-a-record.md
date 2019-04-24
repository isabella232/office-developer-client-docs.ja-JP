---
title: レコードへのジャンプ
TOCTitle: Jumping to a record
ms:assetid: 27177bbe-066c-aeb0-6dfd-45d8c2a87487
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249033(v=office.15)
ms:contentKeyID: 48543829
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 08d8a3d7b3d6012867a91aa306f45872bfebb2e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290787"
---
# <a name="jumping-to-a-record"></a><span data-ttu-id="b4200-102">レコードへのジャンプ</span><span class="sxs-lookup"><span data-stu-id="b4200-102">Jumping to a record</span></span>


<span data-ttu-id="b4200-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="b4200-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b4200-104">次の構文で [Move](move-method-ado.md) メソッドを使用すると、 **Recordset** 内を指定した数の分だけ前後に移動できます。</span><span class="sxs-lookup"><span data-stu-id="b4200-104">The [Move](move-method-ado.md) method allows you to move forward or backward in the **Recordset** a specified number of records by using the following syntax:</span></span>

```vb 
 
oRs.Move NumRecords, Start
```

<span data-ttu-id="b4200-105">**Move** メソッドは、すべての **Recordset** オブジェクトでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="b4200-105">The **Move** method is supported on all **Recordset** objects.</span></span>

<span data-ttu-id="b4200-p101">*NumRecords* 引数がゼロより大きい場合、現在のレコードの位置は前方 (**Recordset** の末尾方向) に移動します。*NumRecords* がゼロより小さい場合、現在のレコードの位置は後方 (**Recordset** の先頭方向) に移動します。</span><span class="sxs-lookup"><span data-stu-id="b4200-p101">If the *NumRecords* argument is greater than zero, the current record position moves forward (toward the end of the **Recordset**). If *NumRecords* is less than zero, the current record position moves backward (toward the beginning of the **Recordset**).</span></span>

<span data-ttu-id="b4200-p102">**Move** の呼び出しにより、現在のレコードの位置が先頭のレコードよりも前に移動した場合、現在のレコードの位置は、**Recordset** 内の先頭のレコードの前に設定されます (**BOF** が **True** になる)。**BOF** プロパティが既に **True** の場合、後方に移動しようとするとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="b4200-p102">If the **Move** call would move the current record position to a point before the first record, ADO sets the current record to the position before the first record in the **Recordset** (**BOF** is **True**). An attempt to move backward when the **BOF** property is already **True** generates an error.</span></span>

<span data-ttu-id="b4200-p103">**Move** の呼び出しにより、現在のレコードの位置が最後のレコードよりも後に移動した場合、現在のレコードの位置は、**Recordset** 内の最後のレコードの後に設定されます (**EOF** が **True** になる)。**EOF** プロパティが既に **True** の場合、前方に移動しようとするとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="b4200-p103">If the **Move** call would move the current record position to a point after the last record, ADO sets the current record to the position after the last record in the **Recordset** (**EOF** is **True**). An attempt to move forward when the **EOF** property is already **True** generates an error.</span></span>

<span data-ttu-id="b4200-112">空の **Recordset** オブジェクトで **Move** メソッドを呼び出すと、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="b4200-112">Calling the **Move** method from an empty **Recordset** object generates an error.</span></span>

<span data-ttu-id="b4200-p104">**Recordset** オブジェクトでブックマークがサポートされている場合、*Start* 引数でブックマークを指定すると、このブックマークが指すレコードを基準にして移動します。ブックマークは、[Bookmark](bookmark-property-ado.md) プロパティを使用して取得します。引数を指定しない場合は、現在のレコードを基準にして移動します。</span><span class="sxs-lookup"><span data-stu-id="b4200-p104">If you pass a bookmark in the *Start* argument, the move is relative to the record with this bookmark, assuming the **Recordset** object supports bookmarks. A bookmark is obtained by using the [Bookmark](bookmark-property-ado.md) property. If not specified, the move is relative to the current record.</span></span>

<span data-ttu-id="b4200-p105">**CacheSize** プロパティを使用してプロバイダーからのレコードをローカルにキャッシュしている場合、*NumRecords* 引数を渡して、現在キャッシュされているレコード グループの範囲外に現在のレコード位置を移動すると、移動先のレコードから始まる新規レコード グループが強制的に取得されます。**CacheSize** プロパティが、新規に取得されるグループのサイズを決定し、移動先のレコードが最初に取得されるレコードになります。</span><span class="sxs-lookup"><span data-stu-id="b4200-p105">If you are using the **CacheSize** property to locally cache records from the provider, passing a *NumRecords* argument that moves the current record position outside the current group of cached records forces ADO to retrieve a new group of records, starting from the destination record. The **CacheSize** property determines the size of the newly retrieved group, and the destination record is the first record retrieved.</span></span>

