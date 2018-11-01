---
title: Errors コレクション (ADO)
TOCTitle: Errors Collection (ADO)
ms:assetid: 76c234b8-7fec-11c5-275e-864d5d880ee7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249486(v=office.15)
ms:contentKeyID: 48545706
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fb58176e51a9e73f8551abb05636af1cfbe48d57
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875218"
---
# <a name="errors-collection-ado"></a><span data-ttu-id="09506-102">Errors コレクション (ADO)</span><span class="sxs-lookup"><span data-stu-id="09506-102">Errors Collection (ADO)</span></span>


<span data-ttu-id="09506-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="09506-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="09506-104">プロバイダー関連の 1 つのエラーに対応して発生するすべての [Error](error-object-ado.md) オブジェクトを格納します。</span><span class="sxs-lookup"><span data-stu-id="09506-104">Contains all the [Error](error-object-ado.md) objects created in response to a single provider-related failure provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="09506-105">解説</span><span class="sxs-lookup"><span data-stu-id="09506-105">Remarks</span></span>

<span data-ttu-id="09506-p101">ADO オブジェクトに関係するすべての操作では、1 つ以上のプロバイダー エラーが発生する場合があります。エラーが発生するたびに、1 つ以上の **Error** オブジェクトが **Connection** オブジェクトの [Errors](connection-object-ado.md) コレクションに追加される可能性があります。別の ADO 操作でエラーが発生すると、 **Errors** コレクションがクリアされ、 **Error** オブジェクトの新しいセットが **Errors** コレクションに配置される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="09506-p101">Any operation involving ADO objects can generate one or more provider errors. As each error occurs, one or more **Error** objects can be placed in the **Errors** collection of the [Connection](connection-object-ado.md) object. When another ADO operation generates an error, the **Errors** collection is cleared, and the new set of **Error** objects can be placed in the **Errors** collection.</span></span>

<span data-ttu-id="09506-p102">各 **Error** オブジェクトは、ADO エラーではなく特定のプロバイダー エラーを表します。ADO エラーは、実行時の例外処理メカニズムに公開されます。たとえば、Microsoft Visual Basic の場合、ADO 固有のエラーが発生すると、 [onError](onerror-event-rds.md) イベントが実行され、そのエラーが **Err** オブジェクトに追加されます。</span><span class="sxs-lookup"><span data-stu-id="09506-p102">Each **Error** object represents a specific provider error, not an ADO error. ADO errors are exposed to the run-time exception-handling mechanism. For example, in Microsoft Visual Basic, the occurrence of an ADO-specific error will trigger an [onError](onerror-event-rds.md) event and appear in the **Err** object.</span></span>

<span data-ttu-id="09506-p103">エラーが発生しない ADO 操作は、 **Errors** コレクションには影響を与えません。 [Errors](clear-method-ado.md) コレクションを手動でクリアするには、 **Clear** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="09506-p103">ADO operations that don't generate an error have no effect on the **Errors** collection. Use the [Clear](clear-method-ado.md) method to manually clear the **Errors** collection.</span></span>

<span data-ttu-id="09506-p104">**Errors** コレクション内の **Error** オブジェクトのセットは、1 つのステートメントに対応して発生するすべてのエラーを記述します。 **Errors** コレクションの特定のエラーを列挙すると、エラー処理ルーチンでは、エラーの原因と発生源をより正確に特定し、適切な回復手順を実行できます。</span><span class="sxs-lookup"><span data-stu-id="09506-p104">The set of **Error** objects in the **Errors** collection describes all errors that occurred in response to a single statement. Enumerating the specific errors in the **Errors** collection enables your error-handling routines to more precisely determine the cause and origin of an error, and take appropriate steps to recover.</span></span>

<span data-ttu-id="09506-p105">プロパティとメソッドの中には、 **Errors** コレクションの **Error** オブジェクトとして警告を返しても、プログラムの実行を停止しないものがあります。 [Recordset](resync-method-ado.md) オブジェクトで [Resync](updatebatch-method-ado.md) メソッド、 [UpdateBatch](cancelbatch-method-ado.md) メソッド、または [CancelBatch](recordset-object-ado.md) メソッドを呼び出す前、 [Connection](open-method-ado-connection.md) オブジェクトで **Open** メソッドを呼び出す前、または [Recordset](filter-property-ado.md) オブジェクトで **Filter** プロパティを設定する前に、 **Errors** コレクションで **Clear** メソッドを呼び出す必要があります。これにより、 [Errors](count-property-ado.md) コレクションの **Count** プロパティを読み取り、返された警告を調べることができます。</span><span class="sxs-lookup"><span data-stu-id="09506-p105">Some properties and methods return warnings that appear as **Error** objects in the **Errors** collection but do not halt a program's execution. Before you call the [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), or [CancelBatch](cancelbatch-method-ado.md) methods on a [Recordset](recordset-object-ado.md) object, the [Open](open-method-ado-connection.md) method on a **Connection** object, or set the [Filter](filter-property-ado.md) property on a **Recordset** object, call the **Clear** method on the **Errors** collection. That way you can read the [Count](count-property-ado.md) property of the **Errors** collection to test for returned warnings.</span></span>


> [!NOTE]
> <span data-ttu-id="09506-119">[!メモ] 1 つの ADO 操作で複数のエラーが発生する場合の詳細については、 **Error** オブジェクトのトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="09506-119">See the **Error** object topic for a more detailed explanation of the way a single ADO operation can generate multiple errors.</span></span>


