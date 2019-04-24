---
title: recordstatusenum (Access デスクトップデータベースリファレンス)
TOCTitle: RecordStatusEnum
ms:assetid: 302915b8-494d-0be2-6dce-eaf91a0ea8ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249080(v=office.15)
ms:contentKeyID: 48544022
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a83de7730224c5ecd5080c795d38cf2e9a3305a9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309381"
---
# <a name="recordstatusenum"></a><span data-ttu-id="fe139-102">RecordStatusEnum</span><span class="sxs-lookup"><span data-stu-id="fe139-102">RecordStatusEnum</span></span>

<span data-ttu-id="fe139-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="fe139-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fe139-104">バッチ更新またはその他の一括操作に関するレコードの状態を表します。</span><span class="sxs-lookup"><span data-stu-id="fe139-104">Specifies the status of a record with regard to batch updates and other bulk operations.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fe139-105">定数</span><span class="sxs-lookup"><span data-stu-id="fe139-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="fe139-106">値</span><span class="sxs-lookup"><span data-stu-id="fe139-106">Value</span></span></p></th>
<th><p><span data-ttu-id="fe139-107">説明</span><span class="sxs-lookup"><span data-stu-id="fe139-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe139-108"><strong>adreccanceled</strong></span><span class="sxs-lookup"><span data-stu-id="fe139-108"><strong>adRecCanceled</strong></span></span></p></td>
<td><p><span data-ttu-id="fe139-109">0x100</span><span class="sxs-lookup"><span data-stu-id="fe139-109">0x100</span></span></p></td>
<td><p><span data-ttu-id="fe139-110">操作が取り消されたため、レコードが保存されなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="fe139-110">Indicates that the record was not saved because the operation was canceled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe139-111"><strong>adreccantrelease</strong></span><span class="sxs-lookup"><span data-stu-id="fe139-111"><strong>adRecCantRelease</strong></span></span></p></td>
<td><p><span data-ttu-id="fe139-112">解像度</span><span class="sxs-lookup"><span data-stu-id="fe139-112">0x400</span></span></p></td>
<td><p><span data-ttu-id="fe139-113">既存のレコードがロックされていたため、新しいレコードが保存されなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="fe139-113">Indicates that the new record was not saved because the existing record was locked.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe139-114"><strong>adRecConcurrencyViolation</strong></span><span class="sxs-lookup"><span data-stu-id="fe139-114"><strong>adRecConcurrencyViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="fe139-115">0x800</span><span class="sxs-lookup"><span data-stu-id="fe139-115">0x800</span></span></p></td>
<td><p><span data-ttu-id="fe139-116">オプティミスティック同時実行制御が使用されていたため、レコードが保存されなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="fe139-116">Indicates that the record was not saved because optimistic concurrency was in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe139-117"><strong>adrecdbdeleted</strong></span><span class="sxs-lookup"><span data-stu-id="fe139-117"><strong>adRecDBDeleted</strong></span></span></p></td>
<td><p><span data-ttu-id="fe139-118">0x40000</span><span class="sxs-lookup"><span data-stu-id="fe139-118">0x40000</span></span></p></td>
<td><p><span data-ttu-id="fe139-119">レコードは既にデータ ソースから削除されていることを示します。</span><span class="sxs-lookup"><span data-stu-id="fe139-119">Indicates that the record has already been deleted from the data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe139-120"><strong>adrecdeleted</strong></span><span class="sxs-lookup"><span data-stu-id="fe139-120"><strong>adRecDeleted</strong></span></span></p></td>
<td><p><span data-ttu-id="fe139-121">0x4</span><span class="sxs-lookup"><span data-stu-id="fe139-121">0x4</span></span></p></td>
<td><p><span data-ttu-id="fe139-122">レコードが削除されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="fe139-122">Indicates that the record was deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe139-123"><strong>adRecIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="fe139-123"><strong>adRecIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="fe139-124">0x1000</span><span class="sxs-lookup"><span data-stu-id="fe139-124">0x1000</span></span></p></td>
<td><p><span data-ttu-id="fe139-125">ユーザーが整合性制約に違反したため、レコードが保存されなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="fe139-125">Indicates that the record was not saved because the user violated integrity constraints.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe139-126"><strong>adrecinvalid</strong></span><span class="sxs-lookup"><span data-stu-id="fe139-126"><strong>adRecInvalid</strong></span></span></p></td>
<td><p><span data-ttu-id="fe139-127">0x10</span><span class="sxs-lookup"><span data-stu-id="fe139-127">0x10</span></span></p></td>
<td><p><span data-ttu-id="fe139-128">ブックマークが無効なため、レコードが保存されなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="fe139-128">Indicates that the record was not saved because its bookmark is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe139-129"><strong>adRecMaxChangesExceeded</strong></span><span class="sxs-lookup"><span data-stu-id="fe139-129"><strong>adRecMaxChangesExceeded</strong></span></span></p></td>
<td><p><span data-ttu-id="fe139-130">0x2000</span><span class="sxs-lookup"><span data-stu-id="fe139-130">0x2000</span></span></p></td>
<td><p><span data-ttu-id="fe139-131">保留中の変更が多すぎたため、レコードが保存されなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="fe139-131">Indicates that the record was not saved because there were too many pending changes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe139-132"><strong>adrecmodified</strong></span><span class="sxs-lookup"><span data-stu-id="fe139-132"><strong>adRecModified</strong></span></span></p></td>
<td><p><span data-ttu-id="fe139-133">0x2</span><span class="sxs-lookup"><span data-stu-id="fe139-133">0x2</span></span></p></td>
<td><p><span data-ttu-id="fe139-134">レコードが変更されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="fe139-134">Indicates that the record was modified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe139-135"><strong>adrec乗算の加え</strong></span><span class="sxs-lookup"><span data-stu-id="fe139-135"><strong>adRecMultipleChanges</strong></span></span></p></td>
<td><p><span data-ttu-id="fe139-136">0x40</span><span class="sxs-lookup"><span data-stu-id="fe139-136">0x40</span></span></p></td>
<td><p><span data-ttu-id="fe139-137">複数のレコードに影響が及ぶため、レコードが保存されなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="fe139-137">Indicates that the record was not saved because it would have affected multiple records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe139-138"><strong>adrecnew</strong></span><span class="sxs-lookup"><span data-stu-id="fe139-138"><strong>adRecNew</strong></span></span></p></td>
<td><p><span data-ttu-id="fe139-139">0x1</span><span class="sxs-lookup"><span data-stu-id="fe139-139">0x1</span></span></p></td>
<td><p><span data-ttu-id="fe139-140">レコードが新しいことを示します。</span><span class="sxs-lookup"><span data-stu-id="fe139-140">Indicates that the record is new.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe139-141"><strong>adRecObjectOpen</strong></span><span class="sxs-lookup"><span data-stu-id="fe139-141"><strong>adRecObjectOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="fe139-142">0x4000</span><span class="sxs-lookup"><span data-stu-id="fe139-142">0x4000</span></span></p></td>
<td><p><span data-ttu-id="fe139-143">開いているストレージ オブジェクトとの競合のため、レコードが保存されなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="fe139-143">Indicates that the record was not saved because of a conflict with an open storage object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe139-144"><strong>adRecOK</strong></span><span class="sxs-lookup"><span data-stu-id="fe139-144"><strong>adRecOK</strong></span></span></p></td>
<td><p><span data-ttu-id="fe139-145">.0</span><span class="sxs-lookup"><span data-stu-id="fe139-145">0</span></span></p></td>
<td><p><span data-ttu-id="fe139-146">レコードが正常に更新されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="fe139-146">Indicates that the record was successfully updated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe139-147"><strong>adRecOutOfMemory</strong></span><span class="sxs-lookup"><span data-stu-id="fe139-147"><strong>adRecOutOfMemory</strong></span></span></p></td>
<td><p><span data-ttu-id="fe139-148">0x8000</span><span class="sxs-lookup"><span data-stu-id="fe139-148">0x8000</span></span></p></td>
<td><p><span data-ttu-id="fe139-149">メモリ不足のためにレコードが保存されなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="fe139-149">Indicates that the record was not saved because the computer has run out of memory.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe139-150"><strong>adrecpendingchanges</strong></span><span class="sxs-lookup"><span data-stu-id="fe139-150"><strong>adRecPendingChanges</strong></span></span></p></td>
<td><p><span data-ttu-id="fe139-151">0x80</span><span class="sxs-lookup"><span data-stu-id="fe139-151">0x80</span></span></p></td>
<td><p><span data-ttu-id="fe139-152">保留中の挿入を参照しているため、レコードが保存されなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="fe139-152">Indicates that the record was not saved because it refers to a pending insert.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe139-153"><strong>adrecpermissiondenied</strong></span><span class="sxs-lookup"><span data-stu-id="fe139-153"><strong>adRecPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="fe139-154">「その他」</span><span class="sxs-lookup"><span data-stu-id="fe139-154">0x10000</span></span></p></td>
<td><p><span data-ttu-id="fe139-155">ユーザーの権限不足により、レコードが保存されなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="fe139-155">Indicates that the record was not saved because the user has insufficient permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe139-156"><strong>adrecschemaviolation</strong></span><span class="sxs-lookup"><span data-stu-id="fe139-156"><strong>adRecSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="fe139-157">0x20000</span><span class="sxs-lookup"><span data-stu-id="fe139-157">0x20000</span></span></p></td>
<td><p><span data-ttu-id="fe139-158">基になるデータベースの構造に違反するので、レコードが保存されなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="fe139-158">Indicates that the record was not saved because it violates the structure of the underlying database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe139-159"><strong>adrecunmodified 変更</strong></span><span class="sxs-lookup"><span data-stu-id="fe139-159"><strong>adRecUnmodified</strong></span></span></p></td>
<td><p><span data-ttu-id="fe139-160">0x8</span><span class="sxs-lookup"><span data-stu-id="fe139-160">0x8</span></span></p></td>
<td><p><span data-ttu-id="fe139-161">レコードが変更されなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="fe139-161">Indicates that the record was not modified.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="fe139-162">ADO/WFC と同等</span><span class="sxs-lookup"><span data-stu-id="fe139-162">ADO/WFC equivalent</span></span>

<span data-ttu-id="fe139-163">AdoEnums 状態。</span><span class="sxs-lookup"><span data-stu-id="fe139-163">AdoEnums.RecordStatus.</span></span>

<span data-ttu-id="fe139-164">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="fe139-164">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fe139-165">定数</span><span class="sxs-lookup"><span data-stu-id="fe139-165">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe139-166">AdoEnums の状態。取り消し</span><span class="sxs-lookup"><span data-stu-id="fe139-166">AdoEnums.RecordStatus.CANCELED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe139-167">AdoEnums の状態。 cantrelease</span><span class="sxs-lookup"><span data-stu-id="fe139-167">AdoEnums.RecordStatus.CANTRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe139-168">AdoEnums CONCURRENCYVIOLATION</span><span class="sxs-lookup"><span data-stu-id="fe139-168">AdoEnums.RecordStatus.CONCURRENCYVIOLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe139-169">AdoEnums が削除されました</span><span class="sxs-lookup"><span data-stu-id="fe139-169">AdoEnums.RecordStatus.DBDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe139-170">AdoEnums の状態を削除しました。</span><span class="sxs-lookup"><span data-stu-id="fe139-170">AdoEnums.RecordStatus.DELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe139-171">AdoEnums INTEGRITYVIOLATION</span><span class="sxs-lookup"><span data-stu-id="fe139-171">AdoEnums.RecordStatus.INTEGRITYVIOLATION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe139-172">AdoEnums の状態が無効です。</span><span class="sxs-lookup"><span data-stu-id="fe139-172">AdoEnums.RecordStatus.INVALID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe139-173">AdoEnums MAXCHANGESEXCEEDED</span><span class="sxs-lookup"><span data-stu-id="fe139-173">AdoEnums.RecordStatus.MAXCHANGESEXCEEDED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe139-174">AdoEnums の状態。変更</span><span class="sxs-lookup"><span data-stu-id="fe139-174">AdoEnums.RecordStatus.MODIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe139-175">AdoEnums の各レコードの状態の設定</span><span class="sxs-lookup"><span data-stu-id="fe139-175">AdoEnums.RecordStatus.MULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe139-176">AdoEnums の状態。新しい</span><span class="sxs-lookup"><span data-stu-id="fe139-176">AdoEnums.RecordStatus.NEW</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe139-177">AdoEnums ado</span><span class="sxs-lookup"><span data-stu-id="fe139-177">AdoEnums.RecordStatus.OBJECTOPEN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe139-178">AdoEnums 状態。 OK</span><span class="sxs-lookup"><span data-stu-id="fe139-178">AdoEnums.RecordStatus.OK</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe139-179">AdoEnums OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="fe139-179">AdoEnums.RecordStatus.OUTOFMEMORY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe139-180">AdoEnums の状態の変更</span><span class="sxs-lookup"><span data-stu-id="fe139-180">AdoEnums.RecordStatus.PENDINGCHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe139-181">AdoEnums が拒否されました</span><span class="sxs-lookup"><span data-stu-id="fe139-181">AdoEnums.RecordStatus.PERMISSIONDENIED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe139-182">AdoEnums の状態のスキーマ</span><span class="sxs-lookup"><span data-stu-id="fe139-182">AdoEnums.RecordStatus.SCHEMAVIOLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe139-183">AdoEnums の状態を変更しません。</span><span class="sxs-lookup"><span data-stu-id="fe139-183">AdoEnums.RecordStatus.UNMODIFIED</span></span></p></td>
</tr>
</tbody>
</table>

