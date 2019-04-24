---
title: IsolationLevelEnum (Access デスクトップデータベースリファレンス)
TOCTitle: IsolationLevelEnum
ms:assetid: 438af3f3-65ed-237d-94d8-f3aff6addd3b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249204(v=office.15)
ms:contentKeyID: 48544506
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9f0176772b366b39d368f8bae1e402d420f0136c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291157"
---
# <a name="isolationlevelenum"></a>IsolationLevelEnum

**適用先:** Access 2013、Office 2013

[Connection](connection-object-ado.md) オブジェクトのトランザクション分離レベルを表します。

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
<td><p><strong>adXactUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>プロバイダーが指定されたものとは異なる分離レベルを使用していますが、レベルを特定できないことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adXactChaos</strong></p></td>
<td><p>16</p></td>
<td><p>分離度の高いトランザクションからの保留中の変更を上書きできないことを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adXactBrowse</strong></p></td>
<td><p>256</p></td>
<td><p>1つのトランザクションから、他のトランザクションのコミットされていない変更を表示できることを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adXactReadUncommitted</strong></p></td>
<td><p>256</p></td>
<td><p><strong>adXactBrowse</strong>と同じです。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adXactCursorStability</strong></p></td>
<td><p>4096</p></td>
<td><p>1つのトランザクションから、コミットされた後にのみ他のトランザクションの変更を表示できることを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adXactReadCommitted</strong></p></td>
<td><p>4096</p></td>
<td><p><strong>adXactCursorStability</strong>と同じです。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adXactRepeatableRead</strong></p></td>
<td><p>65536</p></td>
<td><p>1つのトランザクションから、他のトランザクションで行われた変更を表示できないが、再クエリで新しい<strong>Recordset</strong>オブジェクトを取得できることを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adXactIsolated</strong></p></td>
<td><p>1048576</p></td>
<td><p>トランザクションが他のトランザクションとは分離して実行されることを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adXactSerializable</strong></p></td>
<td><p>1048576</p></td>
<td><p><strong>adXactIsolated</strong>と同じです。</p></td>
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
<td><p>AdoEnums</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums IsolationLevel</p></td>
</tr>
<tr class="odd">
<td><p>IsolationLevel の安定性 AdoEnums</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums コミットされた IsolationLevel</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums IsolationLevel</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums IsolationLevel</p></td>
</tr>
</tbody>
</table>

