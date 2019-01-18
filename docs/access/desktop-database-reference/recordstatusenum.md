---
title: 可能 (デスクトップ データベース参照のアクセス)
TOCTitle: RecordStatusEnum
ms:assetid: 302915b8-494d-0be2-6dce-eaf91a0ea8ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249080(v=office.15)
ms:contentKeyID: 48544022
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a83de7730224c5ecd5080c795d38cf2e9a3305a9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722712"
---
# <a name="recordstatusenum"></a><span data-ttu-id="94de2-102">RecordStatusEnum</span><span class="sxs-lookup"><span data-stu-id="94de2-102">RecordStatusEnum</span></span>

<span data-ttu-id="94de2-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="94de2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="94de2-104">バッチ更新またはその他の一括操作に関するレコードの状態を表します。</span><span class="sxs-lookup"><span data-stu-id="94de2-104">Specifies the status of a record with regard to batch updates and other bulk operations.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="94de2-105">定数</span><span class="sxs-lookup"><span data-stu-id="94de2-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="94de2-106">値</span><span class="sxs-lookup"><span data-stu-id="94de2-106">Value</span></span></p></th>
<th><p><span data-ttu-id="94de2-107">説明</span><span class="sxs-lookup"><span data-stu-id="94de2-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="94de2-108"><strong>adRecCanceled</strong></span><span class="sxs-lookup"><span data-stu-id="94de2-108"><strong>adRecCanceled</strong></span></span></p></td>
<td><p><span data-ttu-id="94de2-109">0x100</span><span class="sxs-lookup"><span data-stu-id="94de2-109">0x100</span></span></p></td>
<td><p><span data-ttu-id="94de2-110">操作が取り消されたため、レコードが保存されなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="94de2-110">Indicates that the record was not saved because the operation was canceled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94de2-111"><strong>adRecCantRelease</strong></span><span class="sxs-lookup"><span data-stu-id="94de2-111"><strong>adRecCantRelease</strong></span></span></p></td>
<td><p><span data-ttu-id="94de2-112">0x400</span><span class="sxs-lookup"><span data-stu-id="94de2-112">0x400</span></span></p></td>
<td><p><span data-ttu-id="94de2-113">既存のレコードがロックされていたため、新しいレコードが保存されなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="94de2-113">Indicates that the new record was not saved because the existing record was locked.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94de2-114"><strong>adRecConcurrencyViolation</strong></span><span class="sxs-lookup"><span data-stu-id="94de2-114"><strong>adRecConcurrencyViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="94de2-115">0x800</span><span class="sxs-lookup"><span data-stu-id="94de2-115">0x800</span></span></p></td>
<td><p><span data-ttu-id="94de2-116">オプティミスティック同時実行制御が使用されていたため、レコードが保存されなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="94de2-116">Indicates that the record was not saved because optimistic concurrency was in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94de2-117"><strong>adRecDBDeleted</strong></span><span class="sxs-lookup"><span data-stu-id="94de2-117"><strong>adRecDBDeleted</strong></span></span></p></td>
<td><p><span data-ttu-id="94de2-118">0x40000</span><span class="sxs-lookup"><span data-stu-id="94de2-118">0x40000</span></span></p></td>
<td><p><span data-ttu-id="94de2-119">レコードは既にデータ ソースから削除されていることを示します。</span><span class="sxs-lookup"><span data-stu-id="94de2-119">Indicates that the record has already been deleted from the data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94de2-120"><strong>adRecDeleted</strong></span><span class="sxs-lookup"><span data-stu-id="94de2-120"><strong>adRecDeleted</strong></span></span></p></td>
<td><p><span data-ttu-id="94de2-121">0x4</span><span class="sxs-lookup"><span data-stu-id="94de2-121">0x4</span></span></p></td>
<td><p><span data-ttu-id="94de2-122">レコードが削除されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="94de2-122">Indicates that the record was deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94de2-123"><strong>adRecIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="94de2-123"><strong>adRecIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="94de2-124">0x1000</span><span class="sxs-lookup"><span data-stu-id="94de2-124">0x1000</span></span></p></td>
<td><p><span data-ttu-id="94de2-125">ユーザーが整合性制約に違反したため、レコードが保存されなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="94de2-125">Indicates that the record was not saved because the user violated integrity constraints.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94de2-126"><strong>adRecInvalid</strong></span><span class="sxs-lookup"><span data-stu-id="94de2-126"><strong>adRecInvalid</strong></span></span></p></td>
<td><p><span data-ttu-id="94de2-127">0x10</span><span class="sxs-lookup"><span data-stu-id="94de2-127">0x10</span></span></p></td>
<td><p><span data-ttu-id="94de2-128">ブックマークが無効なため、レコードが保存されなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="94de2-128">Indicates that the record was not saved because its bookmark is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94de2-129"><strong>adRecMaxChangesExceeded</strong></span><span class="sxs-lookup"><span data-stu-id="94de2-129"><strong>adRecMaxChangesExceeded</strong></span></span></p></td>
<td><p><span data-ttu-id="94de2-130">0x2000</span><span class="sxs-lookup"><span data-stu-id="94de2-130">0x2000</span></span></p></td>
<td><p><span data-ttu-id="94de2-131">保留中の変更が多すぎたため、レコードが保存されなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="94de2-131">Indicates that the record was not saved because there were too many pending changes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94de2-132"><strong>adRecModified</strong></span><span class="sxs-lookup"><span data-stu-id="94de2-132"><strong>adRecModified</strong></span></span></p></td>
<td><p><span data-ttu-id="94de2-133">0x2</span><span class="sxs-lookup"><span data-stu-id="94de2-133">0x2</span></span></p></td>
<td><p><span data-ttu-id="94de2-134">レコードが変更されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="94de2-134">Indicates that the record was modified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94de2-135"><strong>adRecMultipleChanges</strong></span><span class="sxs-lookup"><span data-stu-id="94de2-135"><strong>adRecMultipleChanges</strong></span></span></p></td>
<td><p><span data-ttu-id="94de2-136">0x40</span><span class="sxs-lookup"><span data-stu-id="94de2-136">0x40</span></span></p></td>
<td><p><span data-ttu-id="94de2-137">複数のレコードに影響が及ぶため、レコードが保存されなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="94de2-137">Indicates that the record was not saved because it would have affected multiple records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94de2-138"><strong>adRecNew</strong></span><span class="sxs-lookup"><span data-stu-id="94de2-138"><strong>adRecNew</strong></span></span></p></td>
<td><p><span data-ttu-id="94de2-139">0x1</span><span class="sxs-lookup"><span data-stu-id="94de2-139">0x1</span></span></p></td>
<td><p><span data-ttu-id="94de2-140">レコードが新しいことを示します。</span><span class="sxs-lookup"><span data-stu-id="94de2-140">Indicates that the record is new.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94de2-141"><strong>adRecObjectOpen</strong></span><span class="sxs-lookup"><span data-stu-id="94de2-141"><strong>adRecObjectOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="94de2-142">0x4000</span><span class="sxs-lookup"><span data-stu-id="94de2-142">0x4000</span></span></p></td>
<td><p><span data-ttu-id="94de2-143">開いているストレージ オブジェクトとの競合のため、レコードが保存されなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="94de2-143">Indicates that the record was not saved because of a conflict with an open storage object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94de2-144"><strong>adRecOK</strong></span><span class="sxs-lookup"><span data-stu-id="94de2-144"><strong>adRecOK</strong></span></span></p></td>
<td><p><span data-ttu-id="94de2-145">0</span><span class="sxs-lookup"><span data-stu-id="94de2-145">0</span></span></p></td>
<td><p><span data-ttu-id="94de2-146">レコードが正常に更新されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="94de2-146">Indicates that the record was successfully updated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94de2-147"><strong>adRecOutOfMemory</strong></span><span class="sxs-lookup"><span data-stu-id="94de2-147"><strong>adRecOutOfMemory</strong></span></span></p></td>
<td><p><span data-ttu-id="94de2-148">0x8000</span><span class="sxs-lookup"><span data-stu-id="94de2-148">0x8000</span></span></p></td>
<td><p><span data-ttu-id="94de2-149">メモリ不足のためにレコードが保存されなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="94de2-149">Indicates that the record was not saved because the computer has run out of memory.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94de2-150"><strong>adRecPendingChanges</strong></span><span class="sxs-lookup"><span data-stu-id="94de2-150"><strong>adRecPendingChanges</strong></span></span></p></td>
<td><p><span data-ttu-id="94de2-151">0x80</span><span class="sxs-lookup"><span data-stu-id="94de2-151">0x80</span></span></p></td>
<td><p><span data-ttu-id="94de2-152">保留中の挿入を参照しているため、レコードが保存されなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="94de2-152">Indicates that the record was not saved because it refers to a pending insert.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94de2-153"><strong>adRecPermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="94de2-153"><strong>adRecPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="94de2-154">0x10000</span><span class="sxs-lookup"><span data-stu-id="94de2-154">0x10000</span></span></p></td>
<td><p><span data-ttu-id="94de2-155">ユーザーの権限不足により、レコードが保存されなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="94de2-155">Indicates that the record was not saved because the user has insufficient permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94de2-156"><strong>adRecSchemaViolation</strong></span><span class="sxs-lookup"><span data-stu-id="94de2-156"><strong>adRecSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="94de2-157">0x20000</span><span class="sxs-lookup"><span data-stu-id="94de2-157">0x20000</span></span></p></td>
<td><p><span data-ttu-id="94de2-158">基になるデータベースの構造に違反するので、レコードが保存されなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="94de2-158">Indicates that the record was not saved because it violates the structure of the underlying database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94de2-159"><strong>adRecUnmodified</strong></span><span class="sxs-lookup"><span data-stu-id="94de2-159"><strong>adRecUnmodified</strong></span></span></p></td>
<td><p><span data-ttu-id="94de2-160">0x8</span><span class="sxs-lookup"><span data-stu-id="94de2-160">0x8</span></span></p></td>
<td><p><span data-ttu-id="94de2-161">レコードが変更されなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="94de2-161">Indicates that the record was not modified.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="94de2-162">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="94de2-162">ADO/WFC equivalent</span></span>

<span data-ttu-id="94de2-163">AdoEnums.RecordStatus。</span><span class="sxs-lookup"><span data-stu-id="94de2-163">AdoEnums.RecordStatus.</span></span>

<span data-ttu-id="94de2-164">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="94de2-164">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="94de2-165">定数</span><span class="sxs-lookup"><span data-stu-id="94de2-165">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="94de2-166">AdoEnums.RecordStatus.CANCELED</span><span class="sxs-lookup"><span data-stu-id="94de2-166">AdoEnums.RecordStatus.CANCELED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94de2-167">AdoEnums.RecordStatus.CANTRELEASE</span><span class="sxs-lookup"><span data-stu-id="94de2-167">AdoEnums.RecordStatus.CANTRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94de2-168">AdoEnums.RecordStatus.CONCURRENCYVIOLATION</span><span class="sxs-lookup"><span data-stu-id="94de2-168">AdoEnums.RecordStatus.CONCURRENCYVIOLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94de2-169">AdoEnums.RecordStatus.DBDELETED</span><span class="sxs-lookup"><span data-stu-id="94de2-169">AdoEnums.RecordStatus.DBDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94de2-170">AdoEnums.RecordStatus.DELETED</span><span class="sxs-lookup"><span data-stu-id="94de2-170">AdoEnums.RecordStatus.DELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94de2-171">AdoEnums.RecordStatus.INTEGRITYVIOLATION</span><span class="sxs-lookup"><span data-stu-id="94de2-171">AdoEnums.RecordStatus.INTEGRITYVIOLATION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94de2-172">AdoEnums.RecordStatus.INVALID</span><span class="sxs-lookup"><span data-stu-id="94de2-172">AdoEnums.RecordStatus.INVALID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94de2-173">AdoEnums.RecordStatus.MAXCHANGESEXCEEDED</span><span class="sxs-lookup"><span data-stu-id="94de2-173">AdoEnums.RecordStatus.MAXCHANGESEXCEEDED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94de2-174">AdoEnums.RecordStatus.MODIFIED</span><span class="sxs-lookup"><span data-stu-id="94de2-174">AdoEnums.RecordStatus.MODIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94de2-175">AdoEnums.RecordStatus.MULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="94de2-175">AdoEnums.RecordStatus.MULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94de2-176">AdoEnums.RecordStatus.NEW</span><span class="sxs-lookup"><span data-stu-id="94de2-176">AdoEnums.RecordStatus.NEW</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94de2-177">AdoEnums.RecordStatus.OBJECTOPEN</span><span class="sxs-lookup"><span data-stu-id="94de2-177">AdoEnums.RecordStatus.OBJECTOPEN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94de2-178">AdoEnums.RecordStatus.OK</span><span class="sxs-lookup"><span data-stu-id="94de2-178">AdoEnums.RecordStatus.OK</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94de2-179">AdoEnums.RecordStatus.OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="94de2-179">AdoEnums.RecordStatus.OUTOFMEMORY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94de2-180">AdoEnums.RecordStatus.PENDINGCHANGES</span><span class="sxs-lookup"><span data-stu-id="94de2-180">AdoEnums.RecordStatus.PENDINGCHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94de2-181">AdoEnums.RecordStatus.PERMISSIONDENIED</span><span class="sxs-lookup"><span data-stu-id="94de2-181">AdoEnums.RecordStatus.PERMISSIONDENIED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94de2-182">AdoEnums.RecordStatus.SCHEMAVIOLATION</span><span class="sxs-lookup"><span data-stu-id="94de2-182">AdoEnums.RecordStatus.SCHEMAVIOLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94de2-183">AdoEnums.RecordStatus.UNMODIFIED</span><span class="sxs-lookup"><span data-stu-id="94de2-183">AdoEnums.RecordStatus.UNMODIFIED</span></span></p></td>
</tr>
</tbody>
</table>

