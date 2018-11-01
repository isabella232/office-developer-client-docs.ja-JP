---
title: EventReasonEnum (デスクトップ データベース参照のアクセス)
TOCTitle: EventReasonEnum
ms:assetid: 0639928e-d0ef-3db3-887e-f3da03913bc7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248815(v=office.15)
ms:contentKeyID: 48543047
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 5ef716bd28092cdb173fc9bd54a71ed7572e810a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888021"
---
# <a name="eventreasonenum"></a><span data-ttu-id="b762b-102">EventReasonEnum</span><span class="sxs-lookup"><span data-stu-id="b762b-102">EventReasonEnum</span></span>

<span data-ttu-id="b762b-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="b762b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b762b-104">イベントが発生した理由を表します。</span><span class="sxs-lookup"><span data-stu-id="b762b-104">Specifies the reason that caused an event to occur.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b762b-105">定数</span><span class="sxs-lookup"><span data-stu-id="b762b-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="b762b-106">値</span><span class="sxs-lookup"><span data-stu-id="b762b-106">Value</span></span></p></th>
<th><p><span data-ttu-id="b762b-107">説明</span><span class="sxs-lookup"><span data-stu-id="b762b-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b762b-108"><strong>adRsnAddNew</strong></span><span class="sxs-lookup"><span data-stu-id="b762b-108"><strong>adRsnAddNew</strong></span></span></p></td>
<td><p><span data-ttu-id="b762b-109">1</span><span class="sxs-lookup"><span data-stu-id="b762b-109">1</span></span></p></td>
<td><p><span data-ttu-id="b762b-110">新しいレコードが追加されました。</span><span class="sxs-lookup"><span data-stu-id="b762b-110">An operation added a new record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b762b-111"><strong>adRsnClose</strong></span><span class="sxs-lookup"><span data-stu-id="b762b-111"><strong>adRsnClose</strong></span></span></p></td>
<td><p><span data-ttu-id="b762b-112">9</span><span class="sxs-lookup"><span data-stu-id="b762b-112">9</span></span></p></td>
<td><p><span data-ttu-id="b762b-113"><strong>Recordset</strong> が閉じられました。</span><span class="sxs-lookup"><span data-stu-id="b762b-113">An operation closed the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b762b-114"><strong>adRsnDelete</strong></span><span class="sxs-lookup"><span data-stu-id="b762b-114"><strong>adRsnDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="b762b-115">2</span><span class="sxs-lookup"><span data-stu-id="b762b-115">2</span></span></p></td>
<td><p><span data-ttu-id="b762b-116">レコードが削除されました。</span><span class="sxs-lookup"><span data-stu-id="b762b-116">An operation deleted a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b762b-117"><strong>adRsnFirstChange</strong></span><span class="sxs-lookup"><span data-stu-id="b762b-117"><strong>adRsnFirstChange</strong></span></span></p></td>
<td><p><span data-ttu-id="b762b-118">11</span><span class="sxs-lookup"><span data-stu-id="b762b-118">11</span></span></p></td>
<td><p><span data-ttu-id="b762b-119">レコードに初めての変更が加えられました。</span><span class="sxs-lookup"><span data-stu-id="b762b-119">An operation made the first change to a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b762b-120"><strong>adRsnMove</strong></span><span class="sxs-lookup"><span data-stu-id="b762b-120"><strong>adRsnMove</strong></span></span></p></td>
<td><p><span data-ttu-id="b762b-121">10</span><span class="sxs-lookup"><span data-stu-id="b762b-121">10</span></span></p></td>
<td><p><span data-ttu-id="b762b-122"><strong>Recordset</strong> 内のレコード ポインターが移動しました。</span><span class="sxs-lookup"><span data-stu-id="b762b-122">An operation moved the record pointer within the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b762b-123"><strong>adRsnMoveFirst</strong></span><span class="sxs-lookup"><span data-stu-id="b762b-123"><strong>adRsnMoveFirst</strong></span></span></p></td>
<td><p><span data-ttu-id="b762b-124">12</span><span class="sxs-lookup"><span data-stu-id="b762b-124">12</span></span></p></td>
<td><p><span data-ttu-id="b762b-125">レコード ポインターが <strong>Recordset</strong> の最初のレコードに移動しました。</span><span class="sxs-lookup"><span data-stu-id="b762b-125">An operation moved the record pointer to the first record in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b762b-126"><strong>adRsnMoveLast</strong></span><span class="sxs-lookup"><span data-stu-id="b762b-126"><strong>adRsnMoveLast</strong></span></span></p></td>
<td><p><span data-ttu-id="b762b-127">15</span><span class="sxs-lookup"><span data-stu-id="b762b-127">15</span></span></p></td>
<td><p><span data-ttu-id="b762b-128">レコード ポインターが <strong>Recordset</strong> の最後のレコードに移動しました。</span><span class="sxs-lookup"><span data-stu-id="b762b-128">An operation moved the record pointer to the last record in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b762b-129"><strong>adRsnMoveNext</strong></span><span class="sxs-lookup"><span data-stu-id="b762b-129"><strong>adRsnMoveNext</strong></span></span></p></td>
<td><p><span data-ttu-id="b762b-130">13</span><span class="sxs-lookup"><span data-stu-id="b762b-130">13</span></span></p></td>
<td><p><span data-ttu-id="b762b-131">レコード ポインターが <strong>Recordset</strong> の次のレコードに移動しました。</span><span class="sxs-lookup"><span data-stu-id="b762b-131">An operation moved the record pointer to the next record in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b762b-132"><strong>adRsnMovePrevious</strong></span><span class="sxs-lookup"><span data-stu-id="b762b-132"><strong>adRsnMovePrevious</strong></span></span></p></td>
<td><p><span data-ttu-id="b762b-133">14</span><span class="sxs-lookup"><span data-stu-id="b762b-133">14</span></span></p></td>
<td><p><span data-ttu-id="b762b-134">レコード ポインターが <strong>Recordset</strong> の前のレコードに移動しました。</span><span class="sxs-lookup"><span data-stu-id="b762b-134">An operation moved the record pointer to the previous record in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b762b-135"><strong>adRsnRequery</strong></span><span class="sxs-lookup"><span data-stu-id="b762b-135"><strong>adRsnRequery</strong></span></span></p></td>
<td><p><span data-ttu-id="b762b-136">7</span><span class="sxs-lookup"><span data-stu-id="b762b-136">7</span></span></p></td>
<td><p><span data-ttu-id="b762b-137"><a href="recordset-object-ado.md">Recordset</a> が再クエリされました。</span><span class="sxs-lookup"><span data-stu-id="b762b-137">An operation requeried the <a href="recordset-object-ado.md">Recordset</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b762b-138"><strong>adRsnResynch</strong></span><span class="sxs-lookup"><span data-stu-id="b762b-138"><strong>adRsnResynch</strong></span></span></p></td>
<td><p><span data-ttu-id="b762b-139">8</span><span class="sxs-lookup"><span data-stu-id="b762b-139">8</span></span></p></td>
<td><p><span data-ttu-id="b762b-140"><strong>Recordset</strong> がデータベースと再同期しました。</span><span class="sxs-lookup"><span data-stu-id="b762b-140">An operation resynchronized the <strong>Recordset</strong> with the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b762b-141"><strong>adRsnUndoAddNew</strong></span><span class="sxs-lookup"><span data-stu-id="b762b-141"><strong>adRsnUndoAddNew</strong></span></span></p></td>
<td><p><span data-ttu-id="b762b-142">5</span><span class="sxs-lookup"><span data-stu-id="b762b-142">5</span></span></p></td>
<td><p><span data-ttu-id="b762b-143">新しいレコードの追加が取り消されました。</span><span class="sxs-lookup"><span data-stu-id="b762b-143">An operation reversed the addition of a new record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b762b-144"><strong>adRsnUndoDelete</strong></span><span class="sxs-lookup"><span data-stu-id="b762b-144"><strong>adRsnUndoDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="b762b-145">6</span><span class="sxs-lookup"><span data-stu-id="b762b-145">6</span></span></p></td>
<td><p><span data-ttu-id="b762b-146">レコードの削除が取り消されました。</span><span class="sxs-lookup"><span data-stu-id="b762b-146">An operation reversed the deletion of a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b762b-147"><strong>adRsnUndoUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="b762b-147"><strong>adRsnUndoUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="b762b-148">4</span><span class="sxs-lookup"><span data-stu-id="b762b-148">4</span></span></p></td>
<td><p><span data-ttu-id="b762b-149">レコードの更新が取り消されました。</span><span class="sxs-lookup"><span data-stu-id="b762b-149">An operation reversed the update of a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b762b-150"><strong>adRsnUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="b762b-150"><strong>adRsnUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="b762b-151">3</span><span class="sxs-lookup"><span data-stu-id="b762b-151">3</span></span></p></td>
<td><p><span data-ttu-id="b762b-152">既存のレコードが更新されました。</span><span class="sxs-lookup"><span data-stu-id="b762b-152">An operation updated an existing record.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="b762b-153">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="b762b-153">ADO/WFC equivalent</span></span>

<span data-ttu-id="b762b-154">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="b762b-154">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b762b-155">定数</span><span class="sxs-lookup"><span data-stu-id="b762b-155">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b762b-156">AdoEnums.EventReason.ADDNEW</span><span class="sxs-lookup"><span data-stu-id="b762b-156">AdoEnums.EventReason.ADDNEW</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b762b-157">AdoEnums.EventReason.CLOSE</span><span class="sxs-lookup"><span data-stu-id="b762b-157">AdoEnums.EventReason.CLOSE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b762b-158">AdoEnums.EventReason.DELETE</span><span class="sxs-lookup"><span data-stu-id="b762b-158">AdoEnums.EventReason.DELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b762b-159">AdoEnums.EventReason.FIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="b762b-159">AdoEnums.EventReason.FIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b762b-160">AdoEnums.EventReason.MOVE</span><span class="sxs-lookup"><span data-stu-id="b762b-160">AdoEnums.EventReason.MOVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b762b-161">AdoEnums.EventReason.MOVEFIRST</span><span class="sxs-lookup"><span data-stu-id="b762b-161">AdoEnums.EventReason.MOVEFIRST</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b762b-162">AdoEnums.EventReason.MOVELAST</span><span class="sxs-lookup"><span data-stu-id="b762b-162">AdoEnums.EventReason.MOVELAST</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b762b-163">AdoEnums.EventReason.MOVENEXT</span><span class="sxs-lookup"><span data-stu-id="b762b-163">AdoEnums.EventReason.MOVENEXT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b762b-164">AdoEnums.EventReason.MOVEPREVIOUS</span><span class="sxs-lookup"><span data-stu-id="b762b-164">AdoEnums.EventReason.MOVEPREVIOUS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b762b-165">AdoEnums.EventReason.REQUERY</span><span class="sxs-lookup"><span data-stu-id="b762b-165">AdoEnums.EventReason.REQUERY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b762b-166">AdoEnums.EventReason.RESYNCH</span><span class="sxs-lookup"><span data-stu-id="b762b-166">AdoEnums.EventReason.RESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b762b-167">AdoEnums.EventReason.UNDOADDNEW</span><span class="sxs-lookup"><span data-stu-id="b762b-167">AdoEnums.EventReason.UNDOADDNEW</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b762b-168">AdoEnums.EventReason.UNDODELETE</span><span class="sxs-lookup"><span data-stu-id="b762b-168">AdoEnums.EventReason.UNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b762b-169">AdoEnums.EventReason.UNDOUPDATE</span><span class="sxs-lookup"><span data-stu-id="b762b-169">AdoEnums.EventReason.UNDOUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b762b-170">AdoEnums.EventReason.UPDATE</span><span class="sxs-lookup"><span data-stu-id="b762b-170">AdoEnums.EventReason.UPDATE</span></span></p></td>
</tr>
</tbody>
</table>

