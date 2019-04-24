---
title: event理由列挙 (Access デスクトップデータベースリファレンス)
TOCTitle: EventReasonEnum
ms:assetid: 0639928e-d0ef-3db3-887e-f3da03913bc7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248815(v=office.15)
ms:contentKeyID: 48543047
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4948cd9a5f1436e4e1afc61bef87b63675e115ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293330"
---
# <a name="eventreasonenum"></a><span data-ttu-id="324b8-102">EventReasonEnum</span><span class="sxs-lookup"><span data-stu-id="324b8-102">EventReasonEnum</span></span>

<span data-ttu-id="324b8-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="324b8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="324b8-104">イベントが発生した理由を表します。</span><span class="sxs-lookup"><span data-stu-id="324b8-104">Specifies the reason that caused an event to occur.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="324b8-105">定数</span><span class="sxs-lookup"><span data-stu-id="324b8-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="324b8-106">値</span><span class="sxs-lookup"><span data-stu-id="324b8-106">Value</span></span></p></th>
<th><p><span data-ttu-id="324b8-107">説明</span><span class="sxs-lookup"><span data-stu-id="324b8-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="324b8-108"><strong>adrsnaddnew</strong></span><span class="sxs-lookup"><span data-stu-id="324b8-108"><strong>adRsnAddNew</strong></span></span></p></td>
<td><p><span data-ttu-id="324b8-109">1-d</span><span class="sxs-lookup"><span data-stu-id="324b8-109">1</span></span></p></td>
<td><p><span data-ttu-id="324b8-110">新しいレコードが追加されました。</span><span class="sxs-lookup"><span data-stu-id="324b8-110">An operation added a new record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="324b8-111"><strong>adrsnclose</strong></span><span class="sxs-lookup"><span data-stu-id="324b8-111"><strong>adRsnClose</strong></span></span></p></td>
<td><p><span data-ttu-id="324b8-112">i-9</span><span class="sxs-lookup"><span data-stu-id="324b8-112">9</span></span></p></td>
<td><p><span data-ttu-id="324b8-113"><strong>Recordset</strong> が閉じられました。</span><span class="sxs-lookup"><span data-stu-id="324b8-113">An operation closed the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="324b8-114"><strong>adrsndelete</strong></span><span class="sxs-lookup"><span data-stu-id="324b8-114"><strong>adRsnDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="324b8-115">pbm-2</span><span class="sxs-lookup"><span data-stu-id="324b8-115">2</span></span></p></td>
<td><p><span data-ttu-id="324b8-116">レコードが削除されました。</span><span class="sxs-lookup"><span data-stu-id="324b8-116">An operation deleted a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="324b8-117"><strong>adrsnfirstchange</strong></span><span class="sxs-lookup"><span data-stu-id="324b8-117"><strong>adRsnFirstChange</strong></span></span></p></td>
<td><p><span data-ttu-id="324b8-118">#</span><span class="sxs-lookup"><span data-stu-id="324b8-118">11</span></span></p></td>
<td><p><span data-ttu-id="324b8-119">レコードに初めての変更が加えられました。</span><span class="sxs-lookup"><span data-stu-id="324b8-119">An operation made the first change to a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="324b8-120"><strong>adrsnmove</strong></span><span class="sxs-lookup"><span data-stu-id="324b8-120"><strong>adRsnMove</strong></span></span></p></td>
<td><p><span data-ttu-id="324b8-121">個</span><span class="sxs-lookup"><span data-stu-id="324b8-121">10</span></span></p></td>
<td><p><span data-ttu-id="324b8-122"><strong>Recordset</strong> 内のレコード ポインターが移動しました。</span><span class="sxs-lookup"><span data-stu-id="324b8-122">An operation moved the record pointer within the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="324b8-123"><strong>adrsnmovefirst</strong></span><span class="sxs-lookup"><span data-stu-id="324b8-123"><strong>adRsnMoveFirst</strong></span></span></p></td>
<td><p><span data-ttu-id="324b8-124">個</span><span class="sxs-lookup"><span data-stu-id="324b8-124">12</span></span></p></td>
<td><p><span data-ttu-id="324b8-125">レコード ポインターが <strong>Recordset</strong> の最初のレコードに移動しました。</span><span class="sxs-lookup"><span data-stu-id="324b8-125">An operation moved the record pointer to the first record in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="324b8-126"><strong>adrsnmovelast</strong></span><span class="sxs-lookup"><span data-stu-id="324b8-126"><strong>adRsnMoveLast</strong></span></span></p></td>
<td><p><span data-ttu-id="324b8-127">約</span><span class="sxs-lookup"><span data-stu-id="324b8-127">15</span></span></p></td>
<td><p><span data-ttu-id="324b8-128">レコード ポインターが <strong>Recordset</strong> の最後のレコードに移動しました。</span><span class="sxs-lookup"><span data-stu-id="324b8-128">An operation moved the record pointer to the last record in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="324b8-129"><strong>adrsnmovenext</strong></span><span class="sxs-lookup"><span data-stu-id="324b8-129"><strong>adRsnMoveNext</strong></span></span></p></td>
<td><p><span data-ttu-id="324b8-130">スリー</span><span class="sxs-lookup"><span data-stu-id="324b8-130">13</span></span></p></td>
<td><p><span data-ttu-id="324b8-131">レコード ポインターが <strong>Recordset</strong> の次のレコードに移動しました。</span><span class="sxs-lookup"><span data-stu-id="324b8-131">An operation moved the record pointer to the next record in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="324b8-132"><strong>adRsnMovePrevious</strong></span><span class="sxs-lookup"><span data-stu-id="324b8-132"><strong>adRsnMovePrevious</strong></span></span></p></td>
<td><p><span data-ttu-id="324b8-133">第</span><span class="sxs-lookup"><span data-stu-id="324b8-133">14</span></span></p></td>
<td><p><span data-ttu-id="324b8-134">レコード ポインターが <strong>Recordset</strong> の前のレコードに移動しました。</span><span class="sxs-lookup"><span data-stu-id="324b8-134">An operation moved the record pointer to the previous record in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="324b8-135"><strong>adrsnrequery</strong></span><span class="sxs-lookup"><span data-stu-id="324b8-135"><strong>adRsnRequery</strong></span></span></p></td>
<td><p><span data-ttu-id="324b8-136">7</span><span class="sxs-lookup"><span data-stu-id="324b8-136">7</span></span></p></td>
<td><p><span data-ttu-id="324b8-137"><a href="recordset-object-ado.md">Recordset</a> が再クエリされました。</span><span class="sxs-lookup"><span data-stu-id="324b8-137">An operation requeried the <a href="recordset-object-ado.md">Recordset</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="324b8-138"><strong>adrsnresynch 同期</strong></span><span class="sxs-lookup"><span data-stu-id="324b8-138"><strong>adRsnResynch</strong></span></span></p></td>
<td><p><span data-ttu-id="324b8-139">~</span><span class="sxs-lookup"><span data-stu-id="324b8-139">8</span></span></p></td>
<td><p><span data-ttu-id="324b8-140"><strong>Recordset</strong> がデータベースと再同期しました。</span><span class="sxs-lookup"><span data-stu-id="324b8-140">An operation resynchronized the <strong>Recordset</strong> with the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="324b8-141"><strong>adRsnUndoAddNew</strong></span><span class="sxs-lookup"><span data-stu-id="324b8-141"><strong>adRsnUndoAddNew</strong></span></span></p></td>
<td><p><span data-ttu-id="324b8-142">5</span><span class="sxs-lookup"><span data-stu-id="324b8-142">5</span></span></p></td>
<td><p><span data-ttu-id="324b8-143">新しいレコードの追加が取り消されました。</span><span class="sxs-lookup"><span data-stu-id="324b8-143">An operation reversed the addition of a new record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="324b8-144"><strong>adRsnUndoDelete</strong></span><span class="sxs-lookup"><span data-stu-id="324b8-144"><strong>adRsnUndoDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="324b8-145">シックス</span><span class="sxs-lookup"><span data-stu-id="324b8-145">6</span></span></p></td>
<td><p><span data-ttu-id="324b8-146">レコードの削除が取り消されました。</span><span class="sxs-lookup"><span data-stu-id="324b8-146">An operation reversed the deletion of a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="324b8-147"><strong>adRsnUndoUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="324b8-147"><strong>adRsnUndoUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="324b8-148">2/4</span><span class="sxs-lookup"><span data-stu-id="324b8-148">4</span></span></p></td>
<td><p><span data-ttu-id="324b8-149">レコードの更新が取り消されました。</span><span class="sxs-lookup"><span data-stu-id="324b8-149">An operation reversed the update of a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="324b8-150"><strong>adrsnupdate</strong></span><span class="sxs-lookup"><span data-stu-id="324b8-150"><strong>adRsnUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="324b8-151">1/3</span><span class="sxs-lookup"><span data-stu-id="324b8-151">3</span></span></p></td>
<td><p><span data-ttu-id="324b8-152">既存のレコードが更新されました。</span><span class="sxs-lookup"><span data-stu-id="324b8-152">An operation updated an existing record.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="324b8-153">ADO/WFC と同等</span><span class="sxs-lookup"><span data-stu-id="324b8-153">ADO/WFC equivalent</span></span>

<span data-ttu-id="324b8-154">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="324b8-154">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="324b8-155">定数</span><span class="sxs-lookup"><span data-stu-id="324b8-155">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="324b8-156">AdoEnums のイベント</span><span class="sxs-lookup"><span data-stu-id="324b8-156">AdoEnums.EventReason.ADDNEW</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="324b8-157">AdoEnums を閉じます。</span><span class="sxs-lookup"><span data-stu-id="324b8-157">AdoEnums.EventReason.CLOSE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="324b8-158">AdoEnums の削除</span><span class="sxs-lookup"><span data-stu-id="324b8-158">AdoEnums.EventReason.DELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="324b8-159">AdoEnums の変更</span><span class="sxs-lookup"><span data-stu-id="324b8-159">AdoEnums.EventReason.FIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="324b8-160">AdoEnums の移動</span><span class="sxs-lookup"><span data-stu-id="324b8-160">AdoEnums.EventReason.MOVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="324b8-161">AdoEnums のためのイベント</span><span class="sxs-lookup"><span data-stu-id="324b8-161">AdoEnums.EventReason.MOVEFIRST</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="324b8-162">AdoEnums のためのイベント</span><span class="sxs-lookup"><span data-stu-id="324b8-162">AdoEnums.EventReason.MOVELAST</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="324b8-163">AdoEnums のためのイベント</span><span class="sxs-lookup"><span data-stu-id="324b8-163">AdoEnums.EventReason.MOVENEXT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="324b8-164">AdoEnums MOVEPREVIOUS</span><span class="sxs-lookup"><span data-stu-id="324b8-164">AdoEnums.EventReason.MOVEPREVIOUS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="324b8-165">AdoEnums の再クエリ</span><span class="sxs-lookup"><span data-stu-id="324b8-165">AdoEnums.EventReason.REQUERY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="324b8-166">AdoEnums の再同期</span><span class="sxs-lookup"><span data-stu-id="324b8-166">AdoEnums.EventReason.RESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="324b8-167">AdoEnums UNDOADDNEW</span><span class="sxs-lookup"><span data-stu-id="324b8-167">AdoEnums.EventReason.UNDOADDNEW</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="324b8-168">AdoEnums UNDODELETE</span><span class="sxs-lookup"><span data-stu-id="324b8-168">AdoEnums.EventReason.UNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="324b8-169">AdoEnums UNDOUPDATE</span><span class="sxs-lookup"><span data-stu-id="324b8-169">AdoEnums.EventReason.UNDOUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="324b8-170">AdoEnums の更新</span><span class="sxs-lookup"><span data-stu-id="324b8-170">AdoEnums.EventReason.UPDATE</span></span></p></td>
</tr>
</tbody>
</table>

