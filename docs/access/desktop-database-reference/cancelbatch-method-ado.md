---
title: CancelBatch メソッド (ADO)
TOCTitle: CancelBatch Method (ADO)
ms:assetid: be7bf073-ed0b-e24c-7ec0-b7379236782a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249925(v=office.15)
ms:contentKeyID: 48547463
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cbc16d01e04bbcff7ff28ccc8e7cb4f3fd6f3dec
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478586"
---
# <a name="cancelbatch-method-ado"></a><span data-ttu-id="38b6d-102">CancelBatch メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="38b6d-102">CancelBatch Method (ADO)</span></span>


<span data-ttu-id="38b6d-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="38b6d-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="38b6d-104">保留中のバッチ更新をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="38b6d-104">Cancels a pending batch update.</span></span>

## <a name="syntax"></a><span data-ttu-id="38b6d-105">構文</span><span class="sxs-lookup"><span data-stu-id="38b6d-105">Syntax</span></span>

<span data-ttu-id="38b6d-106">*レコード セット*です。CancelBatch *AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="38b6d-106">*recordset*.CancelBatch *AffectRecords*</span></span>

## <a name="parameters"></a><span data-ttu-id="38b6d-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="38b6d-107">Parameters</span></span>

  - <span data-ttu-id="38b6d-108">*AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="38b6d-108">*AffectRecords*</span></span>

  - <span data-ttu-id="38b6d-p101">省略可能です。 [CancelBatch](affectenum.md) メソッドで処理するレコードの数を示す **AffectEnum** 値です。</span><span class="sxs-lookup"><span data-stu-id="38b6d-p101">Optional. An [AffectEnum](affectenum.md) value that indicates how many records the **CancelBatch** method will affect.</span></span>

## <a name="remarks"></a><span data-ttu-id="38b6d-111">解説</span><span class="sxs-lookup"><span data-stu-id="38b6d-111">Remarks</span></span>

<span data-ttu-id="38b6d-p102">**CancelBatch** メソッドは、バッチ更新モードの [Recordset](recordset-object-ado.md) で保留中の更新をすべて取り消す場合に使用します。即時更新モードの **Recordset** では、 **adAffectCurrent** を指定しないで **CancelBatch** を呼び出すと、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="38b6d-p102">Use the **CancelBatch** method to cancel any pending updates in a [Recordset](recordset-object-ado.md) in batch update mode. If the **Recordset** is in immediate update mode, calling **CancelBatch** without **adAffectCurrent** generates an error.</span></span>

<span data-ttu-id="38b6d-p103">カレント レコードの編集中または新規レコードの追加中に **CancelBatch** メソッドを呼び出すと、最初に [CancelUpdate](cancelupdate-method-ado.md) メソッドが呼び出されて、キャッシュされているすべての変更が取り消されます。その後、 **Recordset** で保留中のすべての変更が取り消されます。</span><span class="sxs-lookup"><span data-stu-id="38b6d-p103">If you are editing the current record or are adding a new record when you call **CancelBatch**, ADO first calls the [CancelUpdate](cancelupdate-method-ado.md) method to cancel any cached changes. After that, all pending changes in the **Recordset** are canceled.</span></span>

<span data-ttu-id="38b6d-p104">**CancelBatch** を呼び出した後は、カレント レコードを特定できない可能性があります。特に、新規レコードの追加処理中の場合は、その可能性が高くなります。このため、 **CancelBatch** の呼び出し後は、カレント レコードの位置を **Recordset** 内の既知の位置に設定することをお勧めします。たとえば、 [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="38b6d-p104">It's possible that the current record will be indeterminable after a **CancelBatch** call, especially if you were in the process of adding a new record. For this reason, it is prudent to set the current record position to a known location in the **Recordset** after the **CancelBatch** call. For example, call the [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) method.</span></span>

<span data-ttu-id="38b6d-p105">基になるデータとの競合 (たとえば、他のユーザーによってレコードが削除されている場合) が原因で保留中の更新を取り消すこどができない場合、プロバイダーは [Errors](errors-collection-ado.md) コレクションに警告を返しますが、プログラムの実行は停止しません。要求したすべてのレコードで競合が発生した場合にのみ、実行時エラーが発生します。競合しているレコードを特定するには、[Filter](filter-property-ado.md) プロパティ (**adFilterAffectedRecords**) と [Status](status-property-ado-recordset.md) プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="38b6d-p105">If the attempt to cancel the pending updates fails because of a conflict with the underlying data (for example, a record has been deleted by another user), the provider returns warnings to the [Errors](errors-collection-ado.md) collection but does not halt program execution. A run-time error occurs only if there are conflicts on all the requested records. Use the [Filter](filter-property-ado.md) property (**adFilterAffectedRecords**) and the [Status](status-property-ado-recordset.md) property to locate records with conflicts.</span></span>

