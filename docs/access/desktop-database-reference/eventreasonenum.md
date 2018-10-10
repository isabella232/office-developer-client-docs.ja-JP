---
title: EventReasonEnum (デスクトップ データベース参照のアクセス)
TOCTitle: EventReasonEnum
ms:assetid: 0639928e-d0ef-3db3-887e-f3da03913bc7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248815(v=office.15)
ms:contentKeyID: 48543047
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ec32b47d8e69c065d167fe86553aafdec906bc24
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476282"
---
# <a name="eventreasonenum"></a><span data-ttu-id="f1de3-102">EventReasonEnum</span><span class="sxs-lookup"><span data-stu-id="f1de3-102">EventReasonEnum</span></span>


<span data-ttu-id="f1de3-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="f1de3-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f1de3-104">イベントが発生した理由を表します。</span><span class="sxs-lookup"><span data-stu-id="f1de3-104">Specifies the reason that caused an event to occur.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f1de3-105">定数</span><span class="sxs-lookup"><span data-stu-id="f1de3-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="f1de3-106">値</span><span class="sxs-lookup"><span data-stu-id="f1de3-106">Value</span></span></p></th>
<th><p><span data-ttu-id="f1de3-107">説明</span><span class="sxs-lookup"><span data-stu-id="f1de3-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1de3-108"><strong>adRsnAddNew</strong></span><span class="sxs-lookup"><span data-stu-id="f1de3-108"><strong>adRsnAddNew</strong></span></span></p></td>
<td><p><span data-ttu-id="f1de3-109">1</span><span class="sxs-lookup"><span data-stu-id="f1de3-109">1</span></span></p></td>
<td><p><span data-ttu-id="f1de3-110">新しいレコードが追加されました。</span><span class="sxs-lookup"><span data-stu-id="f1de3-110">An operation added a new record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1de3-111"><strong>adRsnClose</strong></span><span class="sxs-lookup"><span data-stu-id="f1de3-111"><strong>adRsnClose</strong></span></span></p></td>
<td><p><span data-ttu-id="f1de3-112">9</span><span class="sxs-lookup"><span data-stu-id="f1de3-112">9</span></span></p></td>
<td><p><span data-ttu-id="f1de3-113"><strong>Recordset</strong> が閉じられました。</span><span class="sxs-lookup"><span data-stu-id="f1de3-113">An operation closed the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1de3-114"><strong>adRsnDelete</strong></span><span class="sxs-lookup"><span data-stu-id="f1de3-114"><strong>adRsnDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="f1de3-115">2</span><span class="sxs-lookup"><span data-stu-id="f1de3-115">2</span></span></p></td>
<td><p><span data-ttu-id="f1de3-116">レコードが削除されました。</span><span class="sxs-lookup"><span data-stu-id="f1de3-116">An operation deleted a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1de3-117"><strong>adRsnFirstChange</strong></span><span class="sxs-lookup"><span data-stu-id="f1de3-117"><strong>adRsnFirstChange</strong></span></span></p></td>
<td><p><span data-ttu-id="f1de3-118">11</span><span class="sxs-lookup"><span data-stu-id="f1de3-118">11</span></span></p></td>
<td><p><span data-ttu-id="f1de3-119">レコードに初めての変更が加えられました。</span><span class="sxs-lookup"><span data-stu-id="f1de3-119">An operation made the first change to a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1de3-120"><strong>adRsnMove</strong></span><span class="sxs-lookup"><span data-stu-id="f1de3-120"><strong>adRsnMove</strong></span></span></p></td>
<td><p><span data-ttu-id="f1de3-121">10</span><span class="sxs-lookup"><span data-stu-id="f1de3-121">10</span></span></p></td>
<td><p><span data-ttu-id="f1de3-122"><strong>Recordset</strong> 内のレコード ポインターが移動しました。</span><span class="sxs-lookup"><span data-stu-id="f1de3-122">An operation moved the record pointer within the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1de3-123"><strong>adRsnMoveFirst</strong></span><span class="sxs-lookup"><span data-stu-id="f1de3-123"><strong>adRsnMoveFirst</strong></span></span></p></td>
<td><p><span data-ttu-id="f1de3-124">12</span><span class="sxs-lookup"><span data-stu-id="f1de3-124">12</span></span></p></td>
<td><p><span data-ttu-id="f1de3-125">レコード ポインターが <strong>Recordset</strong> の最初のレコードに移動しました。</span><span class="sxs-lookup"><span data-stu-id="f1de3-125">An operation moved the record pointer to the first record in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1de3-126"><strong>adRsnMoveLast</strong></span><span class="sxs-lookup"><span data-stu-id="f1de3-126"><strong>adRsnMoveLast</strong></span></span></p></td>
<td><p><span data-ttu-id="f1de3-127">15</span><span class="sxs-lookup"><span data-stu-id="f1de3-127">15</span></span></p></td>
<td><p><span data-ttu-id="f1de3-128">レコード ポインターが <strong>Recordset</strong> の最後のレコードに移動しました。</span><span class="sxs-lookup"><span data-stu-id="f1de3-128">An operation moved the record pointer to the last record in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1de3-129"><strong>adRsnMoveNext</strong></span><span class="sxs-lookup"><span data-stu-id="f1de3-129"><strong>adRsnMoveNext</strong></span></span></p></td>
<td><p><span data-ttu-id="f1de3-130">13</span><span class="sxs-lookup"><span data-stu-id="f1de3-130">13</span></span></p></td>
<td><p><span data-ttu-id="f1de3-131">レコード ポインターが <strong>Recordset</strong> の次のレコードに移動しました。</span><span class="sxs-lookup"><span data-stu-id="f1de3-131">An operation moved the record pointer to the next record in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1de3-132"><strong>adRsnMovePrevious</strong></span><span class="sxs-lookup"><span data-stu-id="f1de3-132"><strong>adRsnMovePrevious</strong></span></span></p></td>
<td><p><span data-ttu-id="f1de3-133">14</span><span class="sxs-lookup"><span data-stu-id="f1de3-133">14</span></span></p></td>
<td><p><span data-ttu-id="f1de3-134">レコード ポインターが <strong>Recordset</strong> の前のレコードに移動しました。</span><span class="sxs-lookup"><span data-stu-id="f1de3-134">An operation moved the record pointer to the previous record in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1de3-135"><strong>adRsnRequery</strong></span><span class="sxs-lookup"><span data-stu-id="f1de3-135"><strong>adRsnRequery</strong></span></span></p></td>
<td><p><span data-ttu-id="f1de3-136">7</span><span class="sxs-lookup"><span data-stu-id="f1de3-136">7</span></span></p></td>
<td><p><span data-ttu-id="f1de3-137"><a href="recordset-object-ado.md">Recordset</a> が再クエリされました。</span><span class="sxs-lookup"><span data-stu-id="f1de3-137">An operation requeried the <a href="recordset-object-ado.md">Recordset</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1de3-138"><strong>adRsnResynch</strong></span><span class="sxs-lookup"><span data-stu-id="f1de3-138"><strong>adRsnResynch</strong></span></span></p></td>
<td><p><span data-ttu-id="f1de3-139">8</span><span class="sxs-lookup"><span data-stu-id="f1de3-139">8</span></span></p></td>
<td><p><span data-ttu-id="f1de3-140"><strong>Recordset</strong> がデータベースと再同期しました。</span><span class="sxs-lookup"><span data-stu-id="f1de3-140">An operation resynchronized the <strong>Recordset</strong> with the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1de3-141"><strong>adRsnUndoAddNew</strong></span><span class="sxs-lookup"><span data-stu-id="f1de3-141"><strong>adRsnUndoAddNew</strong></span></span></p></td>
<td><p><span data-ttu-id="f1de3-142">5</span><span class="sxs-lookup"><span data-stu-id="f1de3-142">5</span></span></p></td>
<td><p><span data-ttu-id="f1de3-143">新しいレコードの追加が取り消されました。</span><span class="sxs-lookup"><span data-stu-id="f1de3-143">An operation reversed the addition of a new record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1de3-144"><strong>adRsnUndoDelete</strong></span><span class="sxs-lookup"><span data-stu-id="f1de3-144"><strong>adRsnUndoDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="f1de3-145">6</span><span class="sxs-lookup"><span data-stu-id="f1de3-145">6</span></span></p></td>
<td><p><span data-ttu-id="f1de3-146">レコードの削除が取り消されました。</span><span class="sxs-lookup"><span data-stu-id="f1de3-146">An operation reversed the deletion of a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1de3-147"><strong>adRsnUndoUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="f1de3-147"><strong>adRsnUndoUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="f1de3-148">4</span><span class="sxs-lookup"><span data-stu-id="f1de3-148">4</span></span></p></td>
<td><p><span data-ttu-id="f1de3-149">レコードの更新が取り消されました。</span><span class="sxs-lookup"><span data-stu-id="f1de3-149">An operation reversed the update of a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1de3-150"><strong>adRsnUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="f1de3-150"><strong>adRsnUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="f1de3-151">3</span><span class="sxs-lookup"><span data-stu-id="f1de3-151">3</span></span></p></td>
<td><p><span data-ttu-id="f1de3-152">既存のレコードが更新されました。</span><span class="sxs-lookup"><span data-stu-id="f1de3-152">An operation updated an existing record.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f1de3-153">**ADO/WFC 等価**</span><span class="sxs-lookup"><span data-stu-id="f1de3-153">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="f1de3-154">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="f1de3-154">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f1de3-155">定数</span><span class="sxs-lookup"><span data-stu-id="f1de3-155">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1de3-156">AdoEnums.EventReason.ADDNEW</span><span class="sxs-lookup"><span data-stu-id="f1de3-156">AdoEnums.EventReason.ADDNEW</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1de3-157">AdoEnums.EventReason.CLOSE</span><span class="sxs-lookup"><span data-stu-id="f1de3-157">AdoEnums.EventReason.CLOSE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1de3-158">AdoEnums.EventReason.DELETE</span><span class="sxs-lookup"><span data-stu-id="f1de3-158">AdoEnums.EventReason.DELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1de3-159">AdoEnums.EventReason.FIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="f1de3-159">AdoEnums.EventReason.FIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1de3-160">AdoEnums.EventReason.MOVE</span><span class="sxs-lookup"><span data-stu-id="f1de3-160">AdoEnums.EventReason.MOVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1de3-161">AdoEnums.EventReason.MOVEFIRST</span><span class="sxs-lookup"><span data-stu-id="f1de3-161">AdoEnums.EventReason.MOVEFIRST</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1de3-162">AdoEnums.EventReason.MOVELAST</span><span class="sxs-lookup"><span data-stu-id="f1de3-162">AdoEnums.EventReason.MOVELAST</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1de3-163">AdoEnums.EventReason.MOVENEXT</span><span class="sxs-lookup"><span data-stu-id="f1de3-163">AdoEnums.EventReason.MOVENEXT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1de3-164">AdoEnums.EventReason.MOVEPREVIOUS</span><span class="sxs-lookup"><span data-stu-id="f1de3-164">AdoEnums.EventReason.MOVEPREVIOUS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1de3-165">AdoEnums.EventReason.REQUERY</span><span class="sxs-lookup"><span data-stu-id="f1de3-165">AdoEnums.EventReason.REQUERY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1de3-166">AdoEnums.EventReason.RESYNCH</span><span class="sxs-lookup"><span data-stu-id="f1de3-166">AdoEnums.EventReason.RESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1de3-167">AdoEnums.EventReason.UNDOADDNEW</span><span class="sxs-lookup"><span data-stu-id="f1de3-167">AdoEnums.EventReason.UNDOADDNEW</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1de3-168">AdoEnums.EventReason.UNDODELETE</span><span class="sxs-lookup"><span data-stu-id="f1de3-168">AdoEnums.EventReason.UNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1de3-169">AdoEnums.EventReason.UNDOUPDATE</span><span class="sxs-lookup"><span data-stu-id="f1de3-169">AdoEnums.EventReason.UNDOUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1de3-170">AdoEnums.EventReason.UPDATE</span><span class="sxs-lookup"><span data-stu-id="f1de3-170">AdoEnums.EventReason.UPDATE</span></span></p></td>
</tr>
</tbody>
</table>

