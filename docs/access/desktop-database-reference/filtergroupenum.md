---
title: FilterGroupEnum (デスクトップ データベース参照のアクセス)
TOCTitle: FilterGroupEnum
ms:assetid: 141f8f9a-c188-5937-91cc-3155eaebebd2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248912(v=office.15)
ms:contentKeyID: 48543381
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 5c42b703536e931405325d3a91219a148e6580d1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873287"
---
# <a name="filtergroupenum"></a>FilterGroupEnum

**適用されます**Access 2013、Office 2013。

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
<td><p>2</p></td>
<td><p>最後に行った <a href="delete-method-ado-recordset.md">Delete</a>、<a href="resync-method-ado.md">Resync</a>、<a href="updatebatch-method-ado.md">UpdateBatch</a>、または <a href="cancelbatch-method-ado.md">CancelBatch</a> 呼び出しで影響を受けたレコードのみを表示するようにフィルター処理します。</p></td>
</tr>
<tr class="even">
<td><p><strong>競合</strong></p></td>
<td><p>5</p></td>
<td><p>最後に行ったバッチ更新が失敗したレコードを表示するようにフィルター処理します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFilterFetchedRecords</strong></p></td>
<td><p>3</p></td>
<td><p>データベースから最後に取得されたレコードである現在のキャッシュ内のレコードを表示するようにフィルター処理します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adFilterNone</strong></p></td>
<td><p>0</p></td>
<td><p>現在のフィルターを削除し、すべてのレコードを復元して表示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>行と列</strong></p></td>
<td><p>1</p></td>
<td><p>変更が行われたが、変更内容がサーバーにまだ送信されていないレコードのみを表示するようにフィルター処理します。バッチ更新モードの場合のみ使用できます。</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC に相当

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
<td><p>AdoEnums.FilterGroup.AFFECTEDRECORDS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.FilterGroup.CONFLICTINGRECORDS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.FilterGroup.FETCHEDRECORDS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.FilterGroup.NONE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.FilterGroup.PENDINGRECORDS</p></td>
</tr>
</tbody>
</table>

