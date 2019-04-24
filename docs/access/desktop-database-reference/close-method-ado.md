---
title: Close メソッド-ActiveX データオブジェクト (ADO)
TOCTitle: Close method (ADO)
ms:assetid: 26a7cced-ebeb-70be-f5de-96a35711bc37
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249029(v=office.15)
ms:contentKeyID: 48543818
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 269a782e85fab1e5dc47cd32f2e2c11306e11470
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296312"
---
# <a name="close-method-ado"></a><span data-ttu-id="81549-102">Close メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="81549-102">Close method (ADO)</span></span>


<span data-ttu-id="81549-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="81549-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="81549-104">開いているオブジェクトおよびそれに関連するすべてのオブジェクトを閉じます。</span><span class="sxs-lookup"><span data-stu-id="81549-104">Closes an open object and any dependent objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="81549-105">構文</span><span class="sxs-lookup"><span data-stu-id="81549-105">Syntax</span></span>

<span data-ttu-id="81549-106">*object*.Close</span><span class="sxs-lookup"><span data-stu-id="81549-106">*object*.Close</span></span>

## <a name="remarks"></a><span data-ttu-id="81549-107">注釈</span><span class="sxs-lookup"><span data-stu-id="81549-107">Remarks</span></span>

<span data-ttu-id="81549-108">**Close** メソッドは、 [Connection](connection-object-ado.md) オブジェクト、 [Record](record-object-ado.md) オブジェクト、 [Recordset](recordset-object-ado.md) オブジェクト、または [Stream](stream-object-ado.md) オブジェクトを閉じて、関連するすべてのシステム リソースを解放する場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="81549-108">Use the **Close** method to close a [Connection](connection-object-ado.md), a [Record](record-object-ado.md), a [Recordset](recordset-object-ado.md), or a [Stream](stream-object-ado.md) object to free any associated system resources.</span></span> <span data-ttu-id="81549-109">オブジェクトを閉じてもメモリからは削除されず、プロパティ設定を変更してもう一度開くことができます。</span><span class="sxs-lookup"><span data-stu-id="81549-109">Closing an object does not remove it from memory; you can change its property settings and open it again later.</span></span> <span data-ttu-id="81549-110">オブジェクトをメモリから完全に削除するには、オブジェクトを閉じた後に、オブジェクト変数を*Nothing* (Visual Basic) に設定します。</span><span class="sxs-lookup"><span data-stu-id="81549-110">To completely eliminate an object from memory, set the object variable to *Nothing* (in Visual Basic) after closing the object.</span></span>

<span data-ttu-id="81549-111">**Connection**</span><span class="sxs-lookup"><span data-stu-id="81549-111">**Connection**</span></span>

<span data-ttu-id="81549-p102">**Close** メソッドを使用して **Connection** オブジェクトを閉じると、その接続に関連するアクティブな **Recordset** オブジェクトもすべて閉じます。閉じた [Connection](command-object-ado.md) オブジェクトに関連する **Command** オブジェクトはそのまま維持されますが、 **Connection** オブジェクトとの関連はなくなります。つまり、 [ActiveConnection](activeconnection-property-ado.md) プロパティは **Nothing** に設定されます。また、 **Command** オブジェクトの [Parameters](parameters-collection-ado.md) コレクション内のプロバイダー定義のパラメーターはすべてクリアされます。</span><span class="sxs-lookup"><span data-stu-id="81549-p102">Using the **Close** method to close a **Connection** object also closes any active **Recordset** objects associated with the connection. A [Command](command-object-ado.md) object associated with the **Connection** object you are closing will persist, but it will no longer be associated with a **Connection** object; that is, its [ActiveConnection](activeconnection-property-ado.md) property will be set to **Nothing**. Also, the **Command** object's [Parameters](parameters-collection-ado.md) collection will be cleared of any provider-defined parameters.</span></span>

<span data-ttu-id="81549-p103">後で [Open](open-method-ado-connection.md) メソッドを呼び出して、同じデータ ソースまたは別のデータ ソースへの接続を再度確立することができます。 **Connection** オブジェクトが閉じている間に、データ ソースに対する開いた接続を必要とするメソッドを呼び出すと、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="81549-p103">You can later call the [Open](open-method-ado-connection.md) method to re-establish the connection to the same, or another, data source. While the **Connection** object is closed, calling any methods that require an open connection to the data source generates an error.</span></span>

<span data-ttu-id="81549-p104">接続上に開いた **Recordset** オブジェクトがある状態で **Connection** オブジェクトを閉じると、すべての **Recordset** オブジェクトの保留中の変更がすべてロールバックされます。トランザクションの処理中に **Close** メソッドを呼び出して明示的に **Connection** オブジェクトを閉じると、エラーが発生します。トランザクションの処理中に **Connection** オブジェクトが適用範囲を外れると、トランザクションは自動的にロールバックされます。</span><span class="sxs-lookup"><span data-stu-id="81549-p104">Closing a **Connection** object while there are open **Recordset** objects on the connection rolls back any pending changes in all of the **Recordset** objects. Explicitly closing a **Connection** object (calling the **Close** method) while a transaction is in progress generates an error. If a **Connection** object falls out of scope while a transaction is in progress, ADO automatically rolls back the transaction.</span></span>

<span data-ttu-id="81549-120">**Recordset、Record、および Stream**</span><span class="sxs-lookup"><span data-stu-id="81549-120">**Recordset, Record, Stream**</span></span>

<span data-ttu-id="81549-p105">**Close** メソッドを使用して **Recordset** オブジェクト、 **Record** オブジェクト、または **Stream** オブジェクトを閉じると、関連するデータ、およびデータに対するそのオブジェクトからの排他アクセスが、すべて解放されます。後で [Open](open-method-ado-recordset.md) メソッドを呼び出し、同じ属性で、または属性を変更して、オブジェクトを再度開くことができます。</span><span class="sxs-lookup"><span data-stu-id="81549-p105">Using the **Close** method to close a **Recordset**, **Record**, or **Stream** object releases the associated data and any exclusive access you may have had to the data through this particular object. You can later call the [Open](open-method-ado-recordset.md) method to reopen the object with the same, or modified, attributes.</span></span>

<span data-ttu-id="81549-123">**Recordset** オブジェクトが閉じている間に、有効なカーソルを必要とするメソッドを呼び出すと、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="81549-123">While a **Recordset** object is closed, calling any methods that require a live cursor generates an error.</span></span>

<span data-ttu-id="81549-p106">即時更新モードで編集を行っているときに **Close** メソッドを呼び出すと、エラーが発生します。 [Update](update-method-ado.md) メソッドまたは [CancelUpdate](cancelupdate-method-ado.md) メソッドを先に呼び出す必要があります。バッチ更新モードの実行中に **Recordset** オブジェクトを閉じると、最後に [UpdateBatch](updatebatch-method-ado.md) を呼び出した後で行われた変更がすべて失われます。</span><span class="sxs-lookup"><span data-stu-id="81549-p106">If an edit is in progress while in immediate update mode, calling the **Close** method generates an error; instead, call the [Update](update-method-ado.md) or [CancelUpdate](cancelupdate-method-ado.md) method first. If you close the **Recordset** object while in batch update mode, all changes since the last [UpdateBatch](updatebatch-method-ado.md) call are lost.</span></span>

<span data-ttu-id="81549-126">[Clone](clone-method-ado.md) メソッドを使用して、開いている **Recordset** オブジェクトの複製を作成した場合、元のオブジェクトまたはいずれかの複製を閉じても、他の複製には影響しません。</span><span class="sxs-lookup"><span data-stu-id="81549-126">If you use the [Clone](clone-method-ado.md) method to create copies of an open **Recordset** object, closing the original or a clone does not affect any of the other copies.</span></span>

