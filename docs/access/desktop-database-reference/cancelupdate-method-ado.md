---
title: CancelUpdate メソッド (ADO)
TOCTitle: CancelUpdate Method (ADO)
ms:assetid: 2bd4d168-ba52-7786-5046-44febeda88e1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249065(v=office.15)
ms:contentKeyID: 48543938
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c56d8fc7eaab7989eaa967aa90090ad59c1656dc
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884766"
---
# <a name="cancelupdate-method-ado"></a><span data-ttu-id="09fa0-102">CancelUpdate メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="09fa0-102">CancelUpdate Method (ADO)</span></span>


<span data-ttu-id="09fa0-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="09fa0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="09fa0-104">[Update](recordset-object-ado.md) メソッドを呼び出す前に行った、 [Recordset](fields-collection-ado.md) オブジェクトのカレント行や新規行に対する変更、または [Record](record-object-ado.md) オブジェクトの [Fields](update-method-ado.md) コレクションに対する変更を、すべてキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="09fa0-104">Cancels any changes made to the current or new row of a [Recordset](recordset-object-ado.md) object, or the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md) object, before calling the [Update](update-method-ado.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="09fa0-105">構文</span><span class="sxs-lookup"><span data-stu-id="09fa0-105">Syntax</span></span>

<span data-ttu-id="09fa0-106">*レコード セット*です。CancelUpdate</span><span class="sxs-lookup"><span data-stu-id="09fa0-106">*recordset*.CancelUpdate</span></span>

<span data-ttu-id="09fa0-107">*レコード*です。*フィールド*です。CancelUpdate</span><span class="sxs-lookup"><span data-stu-id="09fa0-107">*record*.*Fields*.CancelUpdate</span></span>

## <a name="remarks"></a><span data-ttu-id="09fa0-108">解説</span><span class="sxs-lookup"><span data-stu-id="09fa0-108">Remarks</span></span>

<span data-ttu-id="09fa0-109">**Recordset**</span><span class="sxs-lookup"><span data-stu-id="09fa0-109">**Recordset**</span></span>

<span data-ttu-id="09fa0-p101">**CancelUpdate** メソッドは、カレント行に対する変更を取り消す場合、または新しく追加した行を破棄する場合に使用します。 **Update** メソッドを呼び出した後では、カレント行に対する変更または新規行を取り消すことはできません。ただし、変更が [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) メソッドでロールバックできるトランザクションの一部である場合、またはバッチ更新の一部である場合を除きます。バッチ更新の場合は、 **CancelUpdate** メソッドまたは **CancelBatch** メソッドで [Update](cancelbatch-method-ado.md) を取り消すこどができます。</span><span class="sxs-lookup"><span data-stu-id="09fa0-p101">Use the **CancelUpdate** method to cancel any changes made to the current row or to discard a newly added row. You cannot cancel changes to the current row or a new row after you call the **Update** method, unless the changes are either part of a transaction that you can roll back with the [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) method, or part of a batch update. In the case of a batch update, you can cancel the **Update** with the **CancelUpdate** or [CancelBatch](cancelbatch-method-ado.md) method.</span></span>

<span data-ttu-id="09fa0-113">新しい行を追加している場合は、 **CancelUpdate** メソッドを呼び出すと、 [AddNew](addnew-method-ado.md) を呼び出す前にカレントであった行がカレント行になります。</span><span class="sxs-lookup"><span data-stu-id="09fa0-113">If you are adding a new row when you call the **CancelUpdate** method, the current row becomes the row that was current before the [AddNew](addnew-method-ado.md) call.</span></span>

<span data-ttu-id="09fa0-p102">編集モードでカレント レコードから移動する (たとえば、[Move](move-method-ado.md)、[NextRecordset](nextrecordset-method-ado.md)、または [Close](close-method-ado.md) を使用して) 場合は、 **CancelUpdate** を使用して、保留中のすべての変更を取り消すこどができます。データ ソースの更新が成功しなかった場合 (たとえば、参照整合性違反のために削除の試みが失敗し、 **Delete** の呼び出しの後で [Recordset](delete-method-ado-recordset.md) が編集モードのままになった場合) には、この処理が必要になることがあります。</span><span class="sxs-lookup"><span data-stu-id="09fa0-p102">If you are in edit mode and want to move off the current record (for example, with [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md), or [Close](close-method-ado.md)), you can use **CancelUpdate** to cancel any pending changes. You may need to do this if the update cannot successfully be posted to the data source (for example, an attempted delete that fails due to referential integrity violations will leave the **Recordset** in edit mode after a call to [Delete](delete-method-ado-recordset.md)).</span></span>

<span data-ttu-id="09fa0-116">**Record**</span><span class="sxs-lookup"><span data-stu-id="09fa0-116">**Record**</span></span>

<span data-ttu-id="09fa0-p103">**CancelUpdate** メソッドは、 [Field](field-object-ado.md) オブジェクトの保留中の挿入または削除をすべてキャンセルし、既存のフィールドの保留中の更新をキャンセルして元の値に戻します。 [Fields](status-property-ado-recordset.md) コレクションのすべてのフィールドの **Status** プロパティは、 **adFieldOK** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="09fa0-p103">The **CancelUpdate** method cancels any pending insertions or deletions of [Field](field-object-ado.md) objects, and cancels pending updates of existing fields and restores them to their original values. The [Status](status-property-ado-recordset.md) property of all fields in the **Fields** collection is set to **adFieldOK**.</span></span>

