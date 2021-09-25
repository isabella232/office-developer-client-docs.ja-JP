---
title: RecordOpenOptionsEnum
TOCTitle: RecordOpenOptionsEnum
ms:assetid: 44a69719-0789-a084-fb96-21468e270205
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249207(v=office.15)
ms:contentKeyID: 48544534
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: e4a348338e66e0d20153c41fb48ab76e1fd0b681
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568545"
---
# <a name="recordopenoptionsenum"></a>RecordOpenOptionsEnum


**適用先:** Access 2013、Office 2013

[Record](record-object-ado.md) を開くときのオプションを表します。これらの値は OR 演算子で結合できます。

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
<td><p><strong>adDelayFetchFields</strong></p></td>
<td><p>0x8000</p></td>
<td><p>プロバイダーに対して、<strong>Record</strong> に関連付けられたフィールドは、当初は取得する必要がなく、フィールドへの最初のアクセス時に取得できることを示します。このフラグが指定されていない場合の既定動作では、<strong>Record</strong> オブジェクトのすべてのフィールドが取得されます。</p></td>
</tr>
<tr class="even">
<td><p><strong>adDelayFetchStream</strong></p></td>
<td><p>0x4000</p></td>
<td><p>プロバイダーに対して、<strong>Record</strong> に関連付けられた既定ストリームを当初は取得する必要がないことを示します。このフラグが指定されていない場合の既定動作では、<strong>Record</strong> オブジェクトに関連付けられた既定ストリームが取得されます。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenAsync</strong></p></td>
<td><p>0x1000</p></td>
<td><p><strong>Record</strong> オブジェクトが非同期モードで開かれることを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenExecuteCommand</strong></p></td>
<td><p>0x10000</p></td>
<td><p>Source 文字列に、実行されるコマンド テキストが含まれることを示します。この値は、<strong>Recordset.Open</strong> の <strong>adCmdText</strong> オプションと等価です。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenRecordUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>既定値。オプションが指定されていないことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenOutput</strong></p></td>
<td><p>0x800000</p></td>
<td><p>実行可能スクリプト (拡張子が .ASP のページなど) があるノードをソースが指定している場合、実行したスクリプトの結果が、開いている <strong>Record</strong> に含まれることを示します。この値は、コレクションのないレコードにのみ有効です。</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC と同等

これらの定数に ADO/WFC 等価はありません。

