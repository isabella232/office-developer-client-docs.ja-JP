---
title: RecordStatusEnum (Access デスクトップ データベース リファレンス)
TOCTitle: RecordStatusEnum
ms:assetid: 302915b8-494d-0be2-6dce-eaf91a0ea8ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249080(v=office.15)
ms:contentKeyID: 48544022
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c86a7038fdcabfc5a30eaf79ddf87521b68d8f58
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557898"
---
# <a name="recordstatusenum"></a>RecordStatusEnum

**適用先:** Access 2013、Office 2013

バッチ更新またはその他の一括操作に関するレコードの状態を表します。

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>定数</p></th>
<th><p>値</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adRecCanceled</strong></p></td>
<td><p>0x100</p></td>
<td><p>操作が取り消されたため、レコードが保存されなかったことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecCantRelease</strong></p></td>
<td><p>0x400</p></td>
<td><p>既存のレコードがロックされていたため、新しいレコードが保存されなかったことを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRecConcurrencyViolation</strong></p></td>
<td><p>0x800</p></td>
<td><p>オプティミスティック同時実行制御が使用されていたため、レコードが保存されなかったことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecDBDeleted</strong></p></td>
<td><p>0x40000</p></td>
<td><p>レコードは既にデータ ソースから削除されていることを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRecDeleted</strong></p></td>
<td><p>0x4</p></td>
<td><p>レコードが削除されたことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecIntegrityViolation</strong></p></td>
<td><p>0x1000</p></td>
<td><p>ユーザーが整合性制約に違反したため、レコードが保存されなかったことを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRecInvalid</strong></p></td>
<td><p>0x10</p></td>
<td><p>ブックマークが無効なため、レコードが保存されなかったことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecMaxChangesExceeded</strong></p></td>
<td><p>0x2000</p></td>
<td><p>保留中の変更が多すぎたため、レコードが保存されなかったことを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRecModified</strong></p></td>
<td><p>0x2</p></td>
<td><p>レコードが変更されたことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecMultipleChanges</strong></p></td>
<td><p>0x40</p></td>
<td><p>複数のレコードに影響が及ぶため、レコードが保存されなかったことを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRecNew</strong></p></td>
<td><p>0x1</p></td>
<td><p>レコードが新しいことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecObjectOpen</strong></p></td>
<td><p>0x4000</p></td>
<td><p>開いているストレージ オブジェクトとの競合のため、レコードが保存されなかったことを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRecOK</strong></p></td>
<td><p>0</p></td>
<td><p>レコードが正常に更新されたことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecOutOfMemory</strong></p></td>
<td><p>0x8000</p></td>
<td><p>メモリ不足のためにレコードが保存されなかったことを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRecPendingChanges</strong></p></td>
<td><p>0x80</p></td>
<td><p>保留中の挿入を参照しているため、レコードが保存されなかったことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecPermissionDenied</strong></p></td>
<td><p>0x10000</p></td>
<td><p>ユーザーの権限不足により、レコードが保存されなかったことを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRecSchemaViolation</strong></p></td>
<td><p>0x20000</p></td>
<td><p>基になるデータベースの構造に違反するので、レコードが保存されなかったことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecUnmodified</strong></p></td>
<td><p>0x8</p></td>
<td><p>レコードが変更されなかったことを示します。</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC と同等

AdoEnums.RecordStatus。

パッケージ: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>定数</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.RecordStatus.CANCELED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.RecordStatus.CANTRELEASE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.RecordStatus.CONCURRENCYVIOLATION</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.RecordStatus.DBDELETED</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.RecordStatus.DELETED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.RecordStatus.INTEGRITYVIOLATION</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.RecordStatus.INVALID</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.RecordStatus.MAXCHANGESEXCEEDED</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.RecordStatus.MODIFIED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.RecordStatus.MULTIPLECHANGES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.RecordStatus.NEW</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.RecordStatus.OBJECTOPEN</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.RecordStatus.OK</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.RecordStatus.OUTOFMEMORY</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.RecordStatus.PENDINGCHANGES</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.RecordStatus.PERMISSIONDENIED</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.RecordStatus.SCHEMAVIOLATION</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.RecordStatus.UNMODIFIED</p></td>
</tr>
</tbody>
</table>

