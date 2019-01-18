---
title: EventReasonEnum (デスクトップ データベース参照のアクセス)
TOCTitle: EventReasonEnum
ms:assetid: 0639928e-d0ef-3db3-887e-f3da03913bc7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248815(v=office.15)
ms:contentKeyID: 48543047
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4948cd9a5f1436e4e1afc61bef87b63675e115ff
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707417"
---
# <a name="eventreasonenum"></a><span data-ttu-id="72c5e-102">EventReasonEnum</span><span class="sxs-lookup"><span data-stu-id="72c5e-102">EventReasonEnum</span></span>

<span data-ttu-id="72c5e-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="72c5e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="72c5e-104">イベントが発生した理由を表します。</span><span class="sxs-lookup"><span data-stu-id="72c5e-104">Specifies the reason that caused an event to occur.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="72c5e-105">定数</span><span class="sxs-lookup"><span data-stu-id="72c5e-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="72c5e-106">値</span><span class="sxs-lookup"><span data-stu-id="72c5e-106">Value</span></span></p></th>
<th><p><span data-ttu-id="72c5e-107">説明</span><span class="sxs-lookup"><span data-stu-id="72c5e-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="72c5e-108"><strong>adRsnAddNew</strong></span><span class="sxs-lookup"><span data-stu-id="72c5e-108"><strong>adRsnAddNew</strong></span></span></p></td>
<td><p><span data-ttu-id="72c5e-109">1</span><span class="sxs-lookup"><span data-stu-id="72c5e-109">1</span></span></p></td>
<td><p><span data-ttu-id="72c5e-110">新しいレコードが追加されました。</span><span class="sxs-lookup"><span data-stu-id="72c5e-110">An operation added a new record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72c5e-111"><strong>adRsnClose</strong></span><span class="sxs-lookup"><span data-stu-id="72c5e-111"><strong>adRsnClose</strong></span></span></p></td>
<td><p><span data-ttu-id="72c5e-112">9</span><span class="sxs-lookup"><span data-stu-id="72c5e-112">9</span></span></p></td>
<td><p><span data-ttu-id="72c5e-113"><strong>Recordset</strong> が閉じられました。</span><span class="sxs-lookup"><span data-stu-id="72c5e-113">An operation closed the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72c5e-114"><strong>adRsnDelete</strong></span><span class="sxs-lookup"><span data-stu-id="72c5e-114"><strong>adRsnDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="72c5e-115">2</span><span class="sxs-lookup"><span data-stu-id="72c5e-115">2</span></span></p></td>
<td><p><span data-ttu-id="72c5e-116">レコードが削除されました。</span><span class="sxs-lookup"><span data-stu-id="72c5e-116">An operation deleted a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72c5e-117"><strong>adRsnFirstChange</strong></span><span class="sxs-lookup"><span data-stu-id="72c5e-117"><strong>adRsnFirstChange</strong></span></span></p></td>
<td><p><span data-ttu-id="72c5e-118">11</span><span class="sxs-lookup"><span data-stu-id="72c5e-118">11</span></span></p></td>
<td><p><span data-ttu-id="72c5e-119">レコードに初めての変更が加えられました。</span><span class="sxs-lookup"><span data-stu-id="72c5e-119">An operation made the first change to a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72c5e-120"><strong>adRsnMove</strong></span><span class="sxs-lookup"><span data-stu-id="72c5e-120"><strong>adRsnMove</strong></span></span></p></td>
<td><p><span data-ttu-id="72c5e-121">10</span><span class="sxs-lookup"><span data-stu-id="72c5e-121">10</span></span></p></td>
<td><p><span data-ttu-id="72c5e-122"><strong>Recordset</strong> 内のレコード ポインターが移動しました。</span><span class="sxs-lookup"><span data-stu-id="72c5e-122">An operation moved the record pointer within the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72c5e-123"><strong>adRsnMoveFirst</strong></span><span class="sxs-lookup"><span data-stu-id="72c5e-123"><strong>adRsnMoveFirst</strong></span></span></p></td>
<td><p><span data-ttu-id="72c5e-124">12</span><span class="sxs-lookup"><span data-stu-id="72c5e-124">12</span></span></p></td>
<td><p><span data-ttu-id="72c5e-125">レコード ポインターが <strong>Recordset</strong> の最初のレコードに移動しました。</span><span class="sxs-lookup"><span data-stu-id="72c5e-125">An operation moved the record pointer to the first record in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72c5e-126"><strong>adRsnMoveLast</strong></span><span class="sxs-lookup"><span data-stu-id="72c5e-126"><strong>adRsnMoveLast</strong></span></span></p></td>
<td><p><span data-ttu-id="72c5e-127">15</span><span class="sxs-lookup"><span data-stu-id="72c5e-127">15</span></span></p></td>
<td><p><span data-ttu-id="72c5e-128">レコード ポインターが <strong>Recordset</strong> の最後のレコードに移動しました。</span><span class="sxs-lookup"><span data-stu-id="72c5e-128">An operation moved the record pointer to the last record in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72c5e-129"><strong>adRsnMoveNext</strong></span><span class="sxs-lookup"><span data-stu-id="72c5e-129"><strong>adRsnMoveNext</strong></span></span></p></td>
<td><p><span data-ttu-id="72c5e-130">13</span><span class="sxs-lookup"><span data-stu-id="72c5e-130">13</span></span></p></td>
<td><p><span data-ttu-id="72c5e-131">レコード ポインターが <strong>Recordset</strong> の次のレコードに移動しました。</span><span class="sxs-lookup"><span data-stu-id="72c5e-131">An operation moved the record pointer to the next record in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72c5e-132"><strong>adRsnMovePrevious</strong></span><span class="sxs-lookup"><span data-stu-id="72c5e-132"><strong>adRsnMovePrevious</strong></span></span></p></td>
<td><p><span data-ttu-id="72c5e-133">14</span><span class="sxs-lookup"><span data-stu-id="72c5e-133">14</span></span></p></td>
<td><p><span data-ttu-id="72c5e-134">レコード ポインターが <strong>Recordset</strong> の前のレコードに移動しました。</span><span class="sxs-lookup"><span data-stu-id="72c5e-134">An operation moved the record pointer to the previous record in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72c5e-135"><strong>adRsnRequery</strong></span><span class="sxs-lookup"><span data-stu-id="72c5e-135"><strong>adRsnRequery</strong></span></span></p></td>
<td><p><span data-ttu-id="72c5e-136">7</span><span class="sxs-lookup"><span data-stu-id="72c5e-136">7</span></span></p></td>
<td><p><span data-ttu-id="72c5e-137"><a href="recordset-object-ado.md">Recordset</a> が再クエリされました。</span><span class="sxs-lookup"><span data-stu-id="72c5e-137">An operation requeried the <a href="recordset-object-ado.md">Recordset</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72c5e-138"><strong>adRsnResynch</strong></span><span class="sxs-lookup"><span data-stu-id="72c5e-138"><strong>adRsnResynch</strong></span></span></p></td>
<td><p><span data-ttu-id="72c5e-139">8</span><span class="sxs-lookup"><span data-stu-id="72c5e-139">8</span></span></p></td>
<td><p><span data-ttu-id="72c5e-140"><strong>Recordset</strong> がデータベースと再同期しました。</span><span class="sxs-lookup"><span data-stu-id="72c5e-140">An operation resynchronized the <strong>Recordset</strong> with the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72c5e-141"><strong>adRsnUndoAddNew</strong></span><span class="sxs-lookup"><span data-stu-id="72c5e-141"><strong>adRsnUndoAddNew</strong></span></span></p></td>
<td><p><span data-ttu-id="72c5e-142">5</span><span class="sxs-lookup"><span data-stu-id="72c5e-142">5</span></span></p></td>
<td><p><span data-ttu-id="72c5e-143">新しいレコードの追加が取り消されました。</span><span class="sxs-lookup"><span data-stu-id="72c5e-143">An operation reversed the addition of a new record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72c5e-144"><strong>adRsnUndoDelete</strong></span><span class="sxs-lookup"><span data-stu-id="72c5e-144"><strong>adRsnUndoDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="72c5e-145">6</span><span class="sxs-lookup"><span data-stu-id="72c5e-145">6</span></span></p></td>
<td><p><span data-ttu-id="72c5e-146">レコードの削除が取り消されました。</span><span class="sxs-lookup"><span data-stu-id="72c5e-146">An operation reversed the deletion of a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72c5e-147"><strong>adRsnUndoUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="72c5e-147"><strong>adRsnUndoUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="72c5e-148">4</span><span class="sxs-lookup"><span data-stu-id="72c5e-148">4</span></span></p></td>
<td><p><span data-ttu-id="72c5e-149">レコードの更新が取り消されました。</span><span class="sxs-lookup"><span data-stu-id="72c5e-149">An operation reversed the update of a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72c5e-150"><strong>adRsnUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="72c5e-150"><strong>adRsnUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="72c5e-151">3</span><span class="sxs-lookup"><span data-stu-id="72c5e-151">3</span></span></p></td>
<td><p><span data-ttu-id="72c5e-152">既存のレコードが更新されました。</span><span class="sxs-lookup"><span data-stu-id="72c5e-152">An operation updated an existing record.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="72c5e-153">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="72c5e-153">ADO/WFC equivalent</span></span>

<span data-ttu-id="72c5e-154">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="72c5e-154">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="72c5e-155">定数</span><span class="sxs-lookup"><span data-stu-id="72c5e-155">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="72c5e-156">AdoEnums.EventReason.ADDNEW</span><span class="sxs-lookup"><span data-stu-id="72c5e-156">AdoEnums.EventReason.ADDNEW</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72c5e-157">AdoEnums.EventReason.CLOSE</span><span class="sxs-lookup"><span data-stu-id="72c5e-157">AdoEnums.EventReason.CLOSE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72c5e-158">AdoEnums.EventReason.DELETE</span><span class="sxs-lookup"><span data-stu-id="72c5e-158">AdoEnums.EventReason.DELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72c5e-159">AdoEnums.EventReason.FIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="72c5e-159">AdoEnums.EventReason.FIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72c5e-160">AdoEnums.EventReason.MOVE</span><span class="sxs-lookup"><span data-stu-id="72c5e-160">AdoEnums.EventReason.MOVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72c5e-161">AdoEnums.EventReason.MOVEFIRST</span><span class="sxs-lookup"><span data-stu-id="72c5e-161">AdoEnums.EventReason.MOVEFIRST</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72c5e-162">AdoEnums.EventReason.MOVELAST</span><span class="sxs-lookup"><span data-stu-id="72c5e-162">AdoEnums.EventReason.MOVELAST</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72c5e-163">AdoEnums.EventReason.MOVENEXT</span><span class="sxs-lookup"><span data-stu-id="72c5e-163">AdoEnums.EventReason.MOVENEXT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72c5e-164">AdoEnums.EventReason.MOVEPREVIOUS</span><span class="sxs-lookup"><span data-stu-id="72c5e-164">AdoEnums.EventReason.MOVEPREVIOUS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72c5e-165">AdoEnums.EventReason.REQUERY</span><span class="sxs-lookup"><span data-stu-id="72c5e-165">AdoEnums.EventReason.REQUERY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72c5e-166">AdoEnums.EventReason.RESYNCH</span><span class="sxs-lookup"><span data-stu-id="72c5e-166">AdoEnums.EventReason.RESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72c5e-167">AdoEnums.EventReason.UNDOADDNEW</span><span class="sxs-lookup"><span data-stu-id="72c5e-167">AdoEnums.EventReason.UNDOADDNEW</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72c5e-168">AdoEnums.EventReason.UNDODELETE</span><span class="sxs-lookup"><span data-stu-id="72c5e-168">AdoEnums.EventReason.UNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72c5e-169">AdoEnums.EventReason.UNDOUPDATE</span><span class="sxs-lookup"><span data-stu-id="72c5e-169">AdoEnums.EventReason.UNDOUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72c5e-170">AdoEnums.EventReason.UPDATE</span><span class="sxs-lookup"><span data-stu-id="72c5e-170">AdoEnums.EventReason.UPDATE</span></span></p></td>
</tr>
</tbody>
</table>

