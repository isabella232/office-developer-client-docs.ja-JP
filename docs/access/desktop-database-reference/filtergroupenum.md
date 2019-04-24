---
title: filtergroupenum (Access デスクトップデータベースリファレンス)
TOCTitle: FilterGroupEnum
ms:assetid: 141f8f9a-c188-5937-91cc-3155eaebebd2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248912(v=office.15)
ms:contentKeyID: 48543381
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: be2ce54fe743c46468850abc5dc16520e208ec9e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292420"
---
# <a name="filtergroupenum"></a>FilterGroupEnum

**適用先:** Access 2013、Office 2013

[Recordset](recordset-object-ado.md) でフィルターの対象となるレコード グループを表します。

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
<td><p><strong>adFilterAffectedRecords</strong></p></td>
<td><p>pbm-2</p></td>
<td><p>最後に行った <a href="delete-method-ado-recordset.md">Delete</a>、<a href="resync-method-ado.md">Resync</a>、<a href="updatebatch-method-ado.md">UpdateBatch</a>、または <a href="cancelbatch-method-ado.md">CancelBatch</a> 呼び出しで影響を受けたレコードのみを表示するようにフィルター処理します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adFilterConflictingRecords</strong></p></td>
<td><p>5</p></td>
<td><p>最後に行ったバッチ更新が失敗したレコードを表示するようにフィルター処理します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adfilterfetchedrecords</strong></p></td>
<td><p>1/3</p></td>
<td><p>データベースから最後に取得されたレコードである現在のキャッシュ内のレコードを表示するようにフィルター処理します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adFilterNone</strong></p></td>
<td><p>.0</p></td>
<td><p>現在のフィルターを削除し、すべてのレコードを復元して表示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adfilterpendingrecords</strong></p></td>
<td><p>1-d</p></td>
<td><p>変更が行われたが、変更内容がサーバーにまだ送信されていないレコードのみを表示するようにフィルター処理します。バッチ更新モードの場合のみ使用できます。</p></td>
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
<td><p>AdoEnums AFFECTEDRECORDS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums レコードの競合</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums レコードのフェッチ</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums。 NONE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums レコードのフィルター</p></td>
</tr>
</tbody>
</table>

