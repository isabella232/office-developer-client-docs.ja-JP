---
title: recordtypeenum (Access デスクトップデータベースリファレンス)
TOCTitle: RecordTypeEnum
ms:assetid: 7edd6508-1507-4649-f1aa-03f1873ef09c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249534(v=office.15)
ms:contentKeyID: 48545890
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c95e4b78a3e2259c3dc5961e87b98ca65ea55692
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309284"
---
# <a name="recordtypeenum"></a>RecordTypeEnum

**適用先:** Access 2013、Office 2013

[Record](record-object-ado.md) オブジェクトの種類を表します。

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
<td><p><strong>adsimplerecord</strong></p></td>
<td><p>.0</p></td>
<td><p>"単純" レコード (子ノードがないレコード) を示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adcollectionrecord</strong></p></td>
<td><p>1-d</p></td>
<td><p>"コレクション" レコード (子ノードがあるレコード) を示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adrecordunknown</strong></p></td>
<td><p>-1</p></td>
<td><p>この <strong>Record</strong> の種類が不明であることを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adStructDoc</strong></p></td>
<td><p>pbm-2</p></td>
<td><p>COM 構造化ドキュメントを表す特殊な "コレクション" レコードを示します。</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC と同等

これらの定数に ADO/WFC 等価はありません。

