---
title: MoveFirst メソッド、MoveLast メソッド、MoveNext メソッド、MovePrevious メソッド (ADO)
TOCTitle: MoveFirst, MoveLast, MoveNext, and MovePrevious methods (ADO)
ms:assetid: d04ce41c-77c9-df42-115a-65c50a38518a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250039(v=office.15)
ms:contentKeyID: 48547836
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2cb6ea7f82ac37460d7f2a4dd998ae7435c04230
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704126"
---
# <a name="movefirst-movelast-movenext-and-moveprevious-methods-ado"></a><span data-ttu-id="83160-102">MoveFirst メソッド、MoveLast メソッド、MoveNext メソッド、MovePrevious メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="83160-102">MoveFirst, MoveLast, MoveNext, and MovePrevious methods (ADO)</span></span>


<span data-ttu-id="83160-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="83160-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="83160-104">指定された [Recordset](recordset-object-ado.md) オブジェクトの最初、最後、次、または前のレコードに移動して、そのレコードをカレント レコードにします。</span><span class="sxs-lookup"><span data-stu-id="83160-104">Moves to the first, last, next, or previous record in a specified [Recordset](recordset-object-ado.md) object and makes that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="83160-105">構文</span><span class="sxs-lookup"><span data-stu-id="83160-105">Syntax</span></span>

<span data-ttu-id="83160-106">*レコード セット*です。{</span><span class="sxs-lookup"><span data-stu-id="83160-106">*recordset*.{</span></span> <span data-ttu-id="83160-107">MoveFirst |MoveLast |MoveNext |MovePrevious}</span><span class="sxs-lookup"><span data-stu-id="83160-107">MoveFirst | MoveLast | MoveNext | MovePrevious}</span></span>

## <a name="remarks"></a><span data-ttu-id="83160-108">解説</span><span class="sxs-lookup"><span data-stu-id="83160-108">Remarks</span></span>

<span data-ttu-id="83160-109">**MoveFirst** メソッドを使用して、カレント レコードの位置を **Recordset** の最初のレコードに移動します。</span><span class="sxs-lookup"><span data-stu-id="83160-109">Use the **MoveFirst** method to move the current record position to the first record in the **Recordset**.</span></span>

<span data-ttu-id="83160-p102">**MoveLast** メソッドを使用して、カレント レコードの位置を **Recordset** の最後のレコードに移動します。 **Recordset** オブジェクトはブックマークまたは後方へのカーソル移動をサポートしている必要があり、サポートしていない場合、このメソッドを呼び出すとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="83160-p102">Use the **MoveLast** method to move the current record position to the last record in the **Recordset**. The **Recordset** object must support bookmarks or backward cursor movement; otherwise, the method call will generate an error.</span></span>

<span data-ttu-id="83160-112">**Recordset** が空 ( **BOF** と **EOF** の両方が True) の場合、 **MoveFirst** または **MoveLast** を呼び出すとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="83160-112">A call to either **MoveFirst** or **MoveLast** when the **Recordset** is empty (both **BOF** and **EOF** are True) generates an error.</span></span>

<span data-ttu-id="83160-p103">**MoveNext** メソッドを使用して、カレント レコードの位置を 1 レコード前方 (**Recordset** の終端方向) に移動します。カレント レコードが最後のレコードの場合に **MoveNext** メソッドを呼び出すと、カレント レコードが **Recordset** の最後のレコードの後に設定され、[EOF](bof-eof-properties-ado.md) が **True** になります。**EOF** プロパティが既に **True** の場合、前方へ移動しようとするとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="83160-p103">Use the **MoveNext** method to move the current record position one record forward (toward the bottom of the **Recordset**). If the last record is the current record and you call the **MoveNext** method, ADO sets the current record to the position after the last record in the **Recordset** ([EOF](bof-eof-properties-ado.md) is **True**). An attempt to move forward when the **EOF** property is already **True** generates an error.</span></span>

<span data-ttu-id="83160-116">フィルターまたはソートが実行された **Recordset** でカレント レコードのデータを変更すると、その位置も変更されることがあります。</span><span class="sxs-lookup"><span data-stu-id="83160-116">In cases where the **Recordset** has been filtered or sorted and the current record's data is changed, the position may also change.</span></span> <span data-ttu-id="83160-117">その場合、 **MoveNext** メソッドは正常に動作しますが、その位置が、元の位置からではなく、変更後の位置から 1 レコード先に移動されることに注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="83160-117">In such cases the **MoveNext** method works normally, but you should be aware that the position is moved one record forward from the new position, not the old position.</span></span> <span data-ttu-id="83160-118">たとえば、レコードが並べ替えられた**レコード セット**の末尾に移動するように、現在のレコードのデータを変更することは、 **MoveNext**の呼び出し元が得られる ADO では、**の最後のレコードより後に位置する現在のレコードを設定レコード セット**(**EOF** = **場合は True**)。</span><span class="sxs-lookup"><span data-stu-id="83160-118">For example, changing the data in the current record, such that the record is moved to the end of the sorted **Recordset,** would mean that calling **MoveNext** results in ADO setting the current record to the position after the last record in the **Recordset** (**EOF** = **True**).</span></span>

<span data-ttu-id="83160-p105">**MovePrevious** メソッドを使用して、カレント レコードの位置を 1 レコード後方 (**Recordset** の始端方向) に移動します。**Recordset** オブジェクトはブックマークまたは後方へのカーソル移動をサポートしている必要があり、サポートしていない場合、このメソッドを呼び出すとエラーが発生します。カレント レコードが最初のレコードの場合に **MovePrevious** メソッドを呼び出すと、カレント レコードは **Recordset** の最初のレコードの前に設定され、[BOF](bof-eof-properties-ado.md) が **True** になります。**BOF** プロパティが既に **True** の場合、後方へ移動しようとすると、エラーが発生します。**Recordset** オブジェクトがブックマークまたは後方へのカーソル移動をサポートしていない場合、**MovePrevious** メソッドを実行すると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="83160-p105">Use the **MovePrevious** method to move the current record position one record backward (toward the top of the **Recordset**). The **Recordset** object must support bookmarks or backward cursor movement; otherwise, the method call will generate an error. If the first record is the current record and you call the **MovePrevious** method, ADO sets the current record to the position before the first record in the **Recordset** ([BOF](bof-eof-properties-ado.md) is **True**). An attempt to move backward when the **BOF** property is already **True** generates an error. If the **Recordset** object does not support either bookmarks or backward cursor movement, the **MovePrevious** method will generate an error.</span></span>

<span data-ttu-id="83160-p106">前方スクロールのみ可能な **Recordset** で両方向スクロールのサポートが必要な場合、 [CacheSize](cachesize-property-ado.md) プロパティを使用して後方へのカーソル移動をサポートするレコード キャッシュを作成し、 [Move](move-method-ado.md) メソッドを使用して移動することができます。キャッシュされたレコードはメモリに読み込まれるため、必要以上のレコードのキャッシュは避けてください。前方スクロールのみ可能な **Recordset** オブジェクトで **MoveFirst** メソッドを呼び出すことはできますが、その場合、 **Recordset** オブジェクトを生成するコマンドがプロバイダーで再度実行されることがあります。</span><span class="sxs-lookup"><span data-stu-id="83160-p106">If the **Recordset** is forward only and you want to support both forward and backward scrolling, you can use the [CacheSize](cachesize-property-ado.md) property to create a record cache that will support backward cursor movement through the [Move](move-method-ado.md) method. Because cached records are loaded into memory, you should avoid caching more records than is necessary. You can call the **MoveFirst** method in a forward-only **Recordset** object; doing so may cause the provider to re-execute the command that generated the **Recordset** object.</span></span>

