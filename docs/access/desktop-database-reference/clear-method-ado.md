---
title: メソッドをオフするには、ActiveX データ オブジェクト (ADO)
TOCTitle: Clear method (ADO)
ms:assetid: 5d51f42c-147b-1fcf-d05b-123e5714ecb7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249329(v=office.15)
ms:contentKeyID: 48545110
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 459ce19fab15e3e9bbd886a0f063005dab674fbc
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929140"
---
# <a name="clear-method-ado"></a><span data-ttu-id="f7187-102">Clear メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="f7187-102">Clear method (ADO)</span></span>


<span data-ttu-id="f7187-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="f7187-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f7187-104">**Errors** コレクションからすべての **Error** オブジェクトを削除します。</span><span class="sxs-lookup"><span data-stu-id="f7187-104">Removes all the **Error** objects from the **Errors** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7187-105">構文</span><span class="sxs-lookup"><span data-stu-id="f7187-105">Syntax</span></span>

<span data-ttu-id="f7187-106">*エラー*です。クリア</span><span class="sxs-lookup"><span data-stu-id="f7187-106">*Errors*.Clear</span></span>

## <a name="remarks"></a><span data-ttu-id="f7187-107">解説</span><span class="sxs-lookup"><span data-stu-id="f7187-107">Remarks</span></span>

<span data-ttu-id="f7187-p101">**Errors** コレクションの [Clear](errors-collection-ado.md) メソッドは、コレクションから既存のすべての [Error](error-object-ado.md) オブジェクトを削除する場合に使用します。エラーが発生すると、 **Errors** コレクションは自動的にクリアされ、新しいエラーに基づく **Error** オブジェクトが格納されます。</span><span class="sxs-lookup"><span data-stu-id="f7187-p101">Use the **Clear** method on the [Errors](errors-collection-ado.md) collection to remove all existing [Error](error-object-ado.md) objects from the collection. When an error occurs, ADO automatically clears the **Errors** collection and fills it with **Error** objects based on the new error.</span></span>

<span data-ttu-id="f7187-p102">プロパティとメソッドの中には、 **Errors** コレクションの **Error** オブジェクトとして警告を返しても、プログラムの実行を停止しないものがあります。 [Recordset](resync-method-ado.md) オブジェクトで [Resync](updatebatch-method-ado.md) メソッド、 [UpdateBatch](cancelbatch-method-ado.md) メソッド、または [CancelBatch](recordset-object-ado.md) メソッドを呼び出す前、 [Connection](open-method-ado-connection.md) オブジェクトで [Open](connection-object-ado.md) メソッドを呼び出す前、または [Recordset](filter-property-ado.md) オブジェクトで **Filter** プロパティを設定する前に、 **Errors** コレクションで **Clear** メソッドを呼び出す必要があります。これにより、 [Errors](count-property-ado.md) コレクションの **Count** プロパティを読み取り、返された警告を調べることができます。</span><span class="sxs-lookup"><span data-stu-id="f7187-p102">Some properties and methods return warnings that appear as **Error** objects in the **Errors** collection but do not halt a program's execution. Before you call the [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), or [CancelBatch](cancelbatch-method-ado.md) methods on a [Recordset](recordset-object-ado.md) object; the [Open](open-method-ado-connection.md) method on a [Connection](connection-object-ado.md) object; or set the [Filter](filter-property-ado.md) property on a **Recordset** object, call the **Clear** method on the **Errors** collection. That way, you can read the [Count](count-property-ado.md) property of the **Errors** collection to test for returned warnings.</span></span>

