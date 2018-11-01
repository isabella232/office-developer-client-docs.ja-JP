---
title: ADO イベント ハンドラーの概要
TOCTitle: ADO Event Handler Summary
ms:assetid: f50b9eb4-df6e-7b9d-0b3d-dca8945167a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250247(v=office.15)
ms:contentKeyID: 48548701
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5e47cf076c213707857285757d936d58bd153e7c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880601"
---
# <a name="ado-event-handler-summary"></a><span data-ttu-id="5802e-102">ADO イベント ハンドラーの概要</span><span class="sxs-lookup"><span data-stu-id="5802e-102">ADO Event Handler Summary</span></span>


<span data-ttu-id="5802e-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="5802e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5802e-p101">イベントを発行できる ADO オブジェクトは、[Connection](connection-object-ado.md) オブジェクトと [Recordset](recordset-object-ado.md) オブジェクトの 2 つです。 **ConnectionEvent** 系は **Connection** オブジェクトの操作に関係し、 **RecordsetEvent** 系は **Recordset** オブジェクトの操作に関係します。</span><span class="sxs-lookup"><span data-stu-id="5802e-p101">Two ADO objects can raise events: the [Connection](connection-object-ado.md) object and the [Recordset](recordset-object-ado.md) object. The **ConnectionEvent** family pertains to operations on the **Connection** object, and the **RecordsetEvent** family pertains to operations on the **Recordset** object.</span></span>

  - <span data-ttu-id="5802e-106">**Connection Events**: 接続上でのトランザクション開始時、コミット時またはロール バック時、 [Command](command-object-ado.md) の実行時、 **Connection Event** 操作中の警告発生時、または **Connection** の開始時か終了時にイベントが発行されます。</span><span class="sxs-lookup"><span data-stu-id="5802e-106">**Connection Events**: Events are issued when a transaction on a connection begins, is committed, or is rolled back; when a [Command](command-object-ado.md) executes; when a warning occurs during a **Connection Event** operation; or when a **Connection** starts or ends.</span></span>

  - <span data-ttu-id="5802e-107">**Recordset Events**: **Recordset** オブジェクトの行内での移動時、 **Recordset** の行内のフィールド変更時、 **Recordset** の行の変更時、サーバー側カーソルで **Recordset** を開いたとき、 **Recordset** を閉じたとき、または **Recordset** 内で変更が行われたとき、および非同期のフェッチ操作に関連してもイベントが発行されます。</span><span class="sxs-lookup"><span data-stu-id="5802e-107">**Recordset Events**: Events are issued around asynchronous fetch operations as well as when you navigate through the rows of a **Recordset** object, change a field in a row of a **Recordset**, change a row in a **Recordset**, open a **Recordset** with a server-side cursor, close a **Recordset**, or make any change whatsoever in the **Recordset**.</span></span>

<span data-ttu-id="5802e-108">次の表は、イベントとその説明の一覧です。</span><span class="sxs-lookup"><span data-stu-id="5802e-108">The following tables summarize the events and their descriptions.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5802e-109">ConnectionEvent</span><span class="sxs-lookup"><span data-stu-id="5802e-109">ConnectionEvent</span></span></p></th>
<th><p><span data-ttu-id="5802e-110">説明</span><span class="sxs-lookup"><span data-stu-id="5802e-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5802e-111"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete</a>CommitTransComplete、RollbackTransComplete</span><span class="sxs-lookup"><span data-stu-id="5802e-111"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete</a>, CommitTransComplete, RollbackTransComplete</span></span></p></td>
<td><p><span data-ttu-id="5802e-112"><strong>トランザクション管理</strong> 接続上でカレント トランザクションが開始されたこと、コミットされたこと、またはロール バックされたことを通知します。</span><span class="sxs-lookup"><span data-stu-id="5802e-112"><strong>Transaction Management</strong> — Notification that the current transaction on the connection has started, committed, or rolled back.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5802e-113"><a href="willconnect-event-ado.md">WillConnect</a>、 <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete、切断</a></span><span class="sxs-lookup"><span data-stu-id="5802e-113"><a href="willconnect-event-ado.md">WillConnect</a>, <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete, Disconnect</a></span></span></p></td>
<td><p><span data-ttu-id="5802e-114"><strong>接続管理</strong> 現在の接続がこれから開始されること、開始されたこと、または終了したことを通知します。</span><span class="sxs-lookup"><span data-stu-id="5802e-114"><strong>Connection Management</strong> — Notification that the current connection will start, has started, or has ended.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5802e-115"><a href="willexecute-event-ado.md">アクティビ ティー</a>、 <a href="executecomplete-event-ado.md">ExecuteComplete</a></span><span class="sxs-lookup"><span data-stu-id="5802e-115"><a href="willexecute-event-ado.md">WillExecute</a>, <a href="executecomplete-event-ado.md">ExecuteComplete</a></span></span></p></td>
<td><p><span data-ttu-id="5802e-116"><strong>コマンド実行管理</strong> 接続上で現在のコマンドの実行がこれから開始されること、または終了したことを通知します。</span><span class="sxs-lookup"><span data-stu-id="5802e-116"><strong>Command Execution Management</strong> — Notification that the execution of the current command on the connection will start or has ended.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5802e-117"><a href="infomessage-event-ado.md">InfoMessage</a></span><span class="sxs-lookup"><span data-stu-id="5802e-117"><a href="infomessage-event-ado.md">InfoMessage</a></span></span></p></td>
<td><p><span data-ttu-id="5802e-118"><strong>情報</strong> 現在の操作についての詳細な情報があることを通知します。</span><span class="sxs-lookup"><span data-stu-id="5802e-118"><strong>Informational</strong> — Notification that there is additional information about the current operation.</span></span></p></td>
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
<th><p><span data-ttu-id="5802e-119">RecordsetEvent</span><span class="sxs-lookup"><span data-stu-id="5802e-119">RecordsetEvent</span></span></p></th>
<th><p><span data-ttu-id="5802e-120">説明</span><span class="sxs-lookup"><span data-stu-id="5802e-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5802e-121"><a href="fetchprogress-event-ado.md">FetchProgress</a>、 <a href="fetchcomplete-event-ado.md">FetchComplete</a></span><span class="sxs-lookup"><span data-stu-id="5802e-121"><a href="fetchprogress-event-ado.md">FetchProgress</a>, <a href="fetchcomplete-event-ado.md">FetchComplete</a></span></span></p></td>
<td><p><span data-ttu-id="5802e-p102"><strong>取得状況</strong> データ取得操作が進行中であること、または完了したことを通知します。これらのイベントは、<strong>Recordset</strong> がクライアント側カーソルを使用して開かれたときにのみ利用できます。</span><span class="sxs-lookup"><span data-stu-id="5802e-p102"><strong>Retrieval Status</strong> — Notification of the progress of a data retrieval operation, or that the retrieval operation has completed. These events are only available if the <strong>Recordset</strong> was opened using a client-side cursor.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5802e-124"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField、FieldChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="5802e-124"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField, FieldChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="5802e-125"><strong>フィールド変更管理</strong> 現在のフィールド値をこれから変更すること、または変更したことを通知します。</span><span class="sxs-lookup"><span data-stu-id="5802e-125"><strong>Field Change Management</strong> — Notification that the value of the current field will change, or has changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5802e-126"><a href="willmove-and-movecomplete-events-ado.md">WillMove、MoveComplete</a>、 <a href="endofrecordset-event-ado.md">EndOfRecordset</a></span><span class="sxs-lookup"><span data-stu-id="5802e-126"><a href="willmove-and-movecomplete-events-ado.md">WillMove, MoveComplete</a>, <a href="endofrecordset-event-ado.md">EndOfRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="5802e-127"><strong>移動管理</strong><strong>Recordset</strong> でのカレント行の位置をこれから変更すること、変更が完了したこと、または <strong>Recordset</strong> の最後に達したことを通知します。</span><span class="sxs-lookup"><span data-stu-id="5802e-127"><strong>Navigation Management</strong> — Notification that the current row position in a <strong>Recordset</strong> will change, has changed, or has reached the end of the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5802e-128"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord、RecordChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="5802e-128"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord, RecordChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="5802e-129"><strong>行変更管理</strong><strong>Recordset</strong> のカレント行の内容をこれから変更すること、または変更したことを通知します。</span><span class="sxs-lookup"><span data-stu-id="5802e-129"><strong>Row Change Management</strong> — Notification that something in the current row of the <strong>Recordset</strong> will change, or has changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5802e-130"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset、RecordsetChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="5802e-130"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset, RecordsetChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="5802e-131"><strong>Recordset 変更管理</strong> 現在の <strong>Recordset</strong> の内容をこれから変更すること、または変更したことを通知します。</span><span class="sxs-lookup"><span data-stu-id="5802e-131"><strong>Recordset Change Management</strong> — Notification that something in the current <strong>Recordset</strong> will change, or has changed.</span></span></p></td>
</tr>
</tbody>
</table>

