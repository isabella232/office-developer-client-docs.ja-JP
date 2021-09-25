---
title: ADO イベント ハンドラーの概要
TOCTitle: ADO event handler summary
ms:assetid: f50b9eb4-df6e-7b9d-0b3d-dca8945167a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250247(v=office.15)
ms:contentKeyID: 48548701
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ce180d7ebf76c758155b8af006100a070596875c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59553390"
---
# <a name="ado-event-handler-summary"></a>ADO イベント ハンドラーの概要


**適用先:** Access 2013、Office 2013

イベントを発行できる ADO オブジェクトは、[Connection](connection-object-ado.md) オブジェクトと [Recordset](recordset-object-ado.md) オブジェクトの 2 つです。 **ConnectionEvent** 系は **Connection** オブジェクトの操作に関係し、 **RecordsetEvent** 系は **Recordset** オブジェクトの操作に関係します。

- **Connection Events**: 接続上でのトランザクション開始時、コミット時またはロール バック時、 [Command](command-object-ado.md) の実行時、 **Connection Event** 操作中の警告発生時、または **Connection** の開始時か終了時にイベントが発行されます。

- **Recordset Events**: **Recordset** オブジェクトの行内での移動時、 **Recordset** の行内のフィールド変更時、 **Recordset** の行の変更時、サーバー側カーソルで **Recordset** を開いたとき、 **Recordset** を閉じたとき、または **Recordset** 内で変更が行われたとき、および非同期のフェッチ操作に関連してもイベントが発行されます。

次の表は、イベントとその説明の一覧です。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>ConnectionEvent</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete</a>, CommitTransComplete, RollbackTransComplete</p></td>
<td><p><strong>トランザクション管理</strong> 接続上でカレント トランザクションが開始されたこと、コミットされたこと、またはロール バックされたことを通知します。</p></td>
</tr>
<tr class="even">
<td><p><a href="willconnect-event-ado.md">WillConnect</a>、<a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete、Disconnect</a></p></td>
<td><p><strong>接続管理</strong> 現在の接続がこれから開始されること、開始されたこと、または終了したことを通知します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="willexecute-event-ado.md">WillExecute</a>、 <a href="executecomplete-event-ado.md">ExecuteComplete</a></p></td>
<td><p><strong>コマンド実行管理</strong> 接続上で現在のコマンドの実行がこれから開始されること、または終了したことを通知します。</p></td>
</tr>
<tr class="even">
<td><p><a href="infomessage-event-ado.md">InfoMessage</a></p></td>
<td><p><strong>情報</strong> 現在の操作についての詳細な情報があることを通知します。</p></td>
</tr>
</tbody>
</table>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>RecordsetEvent</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="fetchprogress-event-ado.md">FetchProgress</a>, <a href="fetchcomplete-event-ado.md">FetchComplete</a></p></td>
<td><p><strong>取得状況</strong> データ取得操作が進行中であること、または完了したことを通知します。これらのイベントは、<strong>Recordset</strong> がクライアント側カーソルを使用して開かれたときにのみ利用できます。</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField, FieldChangeComplete</a></p></td>
<td><p><strong>フィールド変更管理</strong> 現在のフィールド値をこれから変更すること、または変更したことを通知します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="willmove-and-movecomplete-events-ado.md">WillMove、 MoveComplete</a>、 <a href="endofrecordset-event-ado.md">EndOfRecordset</a></p></td>
<td><p><strong>移動管理</strong><strong>Recordset</strong> でのカレント行の位置をこれから変更すること、変更が完了したこと、または <strong>Recordset</strong> の最後に達したことを通知します。</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord, RecordChangeComplete</a></p></td>
<td><p><strong>行変更管理</strong><strong>Recordset</strong> のカレント行の内容をこれから変更すること、または変更したことを通知します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset, RecordsetChangeComplete</a></p></td>
<td><p><strong>Recordset 変更管理</strong> 現在の <strong>Recordset</strong> の内容をこれから変更すること、または変更したことを通知します。</p></td>
</tr>
</tbody>
</table>

