---
title: イミディ エイト モード (デスクトップ データベース参照のアクセス)
TOCTitle: Immediate mode
ms:assetid: 61bd3645-6e84-2e3a-7814-37d8c1247df0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249362(v=office.15)
ms:contentKeyID: 48545220
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3abc2e8365c60987fedc0d306b274df74c7ee551
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706948"
---
# <a name="immediate-mode"></a><span data-ttu-id="e4cbb-102">イミディエイト モード</span><span class="sxs-lookup"><span data-stu-id="e4cbb-102">Immediate mode</span></span>


<span data-ttu-id="e4cbb-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="e4cbb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e4cbb-p101">イミディエイト モードは、 **LockType** プロパティが **adLockOptimistic** または **adLockPessimistic** に設定されているときに有効になります。イミディエイト モードでは、 **Update** メソッドを呼び出すことによって、行に対する操作が完了したことを宣言すると直ちにレコードに対する変更が通知されます。</span><span class="sxs-lookup"><span data-stu-id="e4cbb-p101">Immediate mode is in effect when the **LockType** property is set to **adLockOptimistic** or **adLockPessimistic**. In immediate mode, changes to a record are propagated to the data source as soon as you declare the work on a row complete by calling the **Update** method.</span></span>

## <a name="calling-update"></a><span data-ttu-id="e4cbb-106">Update を呼び出す</span><span class="sxs-lookup"><span data-stu-id="e4cbb-106">Calling Update</span></span>

<span data-ttu-id="e4cbb-p102">**Update** メソッドを呼び出す前に、追加または編集中のレコードから移動すると、ADO によって **Update** が自動的に呼び出され、変更が保存されます。現在のレコードに対する変更を取り消す場合や、新しく追加したレコードを破棄する場合は、移動する前に **CancelUpdate** メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="e4cbb-p102">If you move from the record you are adding or editing before calling the **Update** method, ADO will automatically call **Update** to save the changes. You must call the **CancelUpdate** method before navigation if you want to cancel any changes made to the current record or discard a newly added record.</span></span>

<span data-ttu-id="e4cbb-109">現在のレコードは、 **Update** メソッドの呼び出し後も現在のレコードのままです。</span><span class="sxs-lookup"><span data-stu-id="e4cbb-109">The current record remains current after you call the **Update** method.</span></span>

## <a name="cancelupdate"></a><span data-ttu-id="e4cbb-110">CancelUpdate</span><span class="sxs-lookup"><span data-stu-id="e4cbb-110">CancelUpdate</span></span>

<span data-ttu-id="e4cbb-p103">**CancelUpdate** メソッドを使用すると、現在の行に対する変更を取り消したり、新しく追加した行を破棄したりできます。 **Update** メソッドを呼び出した後は、現在のレコードに対する変更や新しい行を取り消すことができません。ただし、変更が **RollbackTrans** メソッドによってロールバックできるトランザクションの一部である場合や、バッチ更新の一部である場合を除きます。バッチ更新の場合は、 **Update** を **CancelUpdate** メソッドまたは **CancelBatch** メソッドによって取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="e4cbb-p103">Use the **CancelUpdate** method to cancel any changes made to the current row or to discard a newly added row. You cannot cancel changes to the current row or a new row after you call the **Update** method, unless the changes are either part of a transaction that you can roll back with the **RollbackTrans** method or part of a batch update. In the case of a batch update, you can cancel the **Update** with the **CancelUpdate** or **CancelBatch** method.</span></span>

<span data-ttu-id="e4cbb-114">**CancelUpdate** メソッドを呼び出したときに新しい行を追加している途中であった場合は、 **AddNew** を呼び出す前に現在の行であった行が現在の行になります。</span><span class="sxs-lookup"><span data-stu-id="e4cbb-114">If you are adding a new row when you call the **CancelUpdate** method, the current row becomes the row that was current before the **AddNew** call.</span></span>

<span data-ttu-id="e4cbb-115">現在の行を変更したり、新しい行を追加したりしていない場合に **CancelUpdate** メソッドを呼び出すと、エラーが生成されます。</span><span class="sxs-lookup"><span data-stu-id="e4cbb-115">If you have not changed the current row or added a new row, calling the **CancelUpdate** method generates an error.</span></span>

