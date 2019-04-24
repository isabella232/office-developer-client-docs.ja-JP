---
title: eventstatusenum (Access デスクトップデータベースリファレンス)
TOCTitle: EventStatusEnum
ms:assetid: ae1711bc-2af5-04fd-7d8c-222d8afc9d3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249821(v=office.15)
ms:contentKeyID: 48547059
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 654d2a485c9273072d1daa61321e73418a15e969
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293274"
---
# <a name="eventstatusenum"></a>EventStatusEnum

**適用先:** Access 2013、Office 2013

イベントの実行の現在の状態を表します。

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
<td><p><strong>adStatusCancel</strong></p></td>
<td><p>2/4</p></td>
<td><p>イベントを発生させた操作の取り消しを要求します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adStatusCantDeny</strong></p></td>
<td><p>1/3</p></td>
<td><p>保留中の操作の取り消しを要求できないことを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adStatusErrorsOccurred</strong></p></td>
<td><p>pbm-2</p></td>
<td><p>イベントを発生させた操作がエラーによって失敗したことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adStatusOK</strong></p></td>
<td><p>1-d</p></td>
<td><p>イベントを発生させた操作が成功したことを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adStatusUnwantedEvent</strong></p></td>
<td><p>5</p></td>
<td><p>イベント メソッドの実行が終了するまで、後続の通知が行われません。</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC と同等

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
<td><p>AdoEnums を取り消します。</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums の状態。 cantdeny</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums の状態 (エラー)</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums の状態。 OK</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums UNWANTEDEVENT</p></td>
</tr>
</tbody>
</table>

