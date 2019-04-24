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
<td><p><strong>adreccanceled</strong></p></td>
<td><p>0x100</p></td>
<td><p>操作が取り消されたため、レコードが保存されなかったことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adreccantrelease</strong></p></td>
<td><p>解像度</p></td>
<td><p>既存のレコードがロックされていたため、新しいレコードが保存されなかったことを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRecConcurrencyViolation</strong></p></td>
<td><p>0x800</p></td>
<td><p>オプティミスティック同時実行制御が使用されていたため、レコードが保存されなかったことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adrecdbdeleted</strong></p></td>
<td><p>0x40000</p></td>
<td><p>レコードは既にデータ ソースから削除されていることを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adrecdeleted</strong></p></td>
<td><p>0x4</p></td>
<td><p>レコードが削除されたことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecIntegrityViolation</strong></p></td>
<td><p>0x1000</p></td>
<td><p>ユーザーが整合性制約に違反したため、レコードが保存されなかったことを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adrecinvalid</strong></p></td>
<td><p>0x10</p></td>
<td><p>ブックマークが無効なため、レコードが保存されなかったことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecMaxChangesExceeded</strong></p></td>
<td><p>0x2000</p></td>
<td><p>保留中の変更が多すぎたため、レコードが保存されなかったことを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adrecmodified</strong></p></td>
<td><p>0x2</p></td>
<td><p>レコードが変更されたことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adrec乗算の加え</strong></p></td>
<td><p>0x40</p></td>
<td><p>複数のレコードに影響が及ぶため、レコードが保存されなかったことを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adrecnew</strong></p></td>
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
<td><p>.0</p></td>
<td><p>レコードが正常に更新されたことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecOutOfMemory</strong></p></td>
<td><p>0x8000</p></td>
<td><p>メモリ不足のためにレコードが保存されなかったことを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adrecpendingchanges</strong></p></td>
<td><p>0x80</p></td>
<td><p>保留中の挿入を参照しているため、レコードが保存されなかったことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adrecpermissiondenied</strong></p></td>
<td><p>「その他」</p></td>
<td><p>ユーザーの権限不足により、レコードが保存されなかったことを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adrecschemaviolation</strong></p></td>
<td><p>0x20000</p></td>
<td><p>基になるデータベースの構造に違反するので、レコードが保存されなかったことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adrecunmodified 変更</strong></p></td>
<td><p>0x8</p></td>
<td><p>レコードが変更されなかったことを示します。</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC と同等

AdoEnums 状態。

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
<td><p>AdoEnums の状態。取り消し</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums の状態。 cantrelease</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums CONCURRENCYVIOLATION</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums が削除されました</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums の状態を削除しました。</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums INTEGRITYVIOLATION</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums の状態が無効です。</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums MAXCHANGESEXCEEDED</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums の状態。変更</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums の各レコードの状態の設定</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums の状態。新しい</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums ado</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums 状態。 OK</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums OUTOFMEMORY</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums の状態の変更</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums が拒否されました</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums の状態のスキーマ</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums の状態を変更しません。</p></td>
</tr>
</tbody>
</table>

