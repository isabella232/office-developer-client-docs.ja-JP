---
title: ActiveX データ オブジェクト (ADO) のイベント
TOCTitle: ADO events
ms:assetid: 84ca9525-99cb-4ba6-2a4d-172414b8f0cc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249576(v=office.15)
ms:contentKeyID: 48546041
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3cc8ac02e2410a2f7bfe1038851e16f50c1ea2ee
ms.sourcegitcommit: 48bfe5ab15b11105f4f52937b886c92bdc26525a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25910944"
---
# <a name="ado-events"></a>ADO イベント

**適用されます**Access 2013、Office 2013。

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th>イベント</th>
<th>説明</th>
</tr>
<tr class="odd">
<td><p><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete</a></p></td>
<td><p><strong>BeginTrans</strong> の操作が終了した後に呼び出されます。</p></td>
</tr>
<tr class="even">
<td><p><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">CommitTransComplete</a></p></td>
<td><p><strong>CommitTrans</strong> の操作が終了した後に呼び出されます。</p></td>
</tr>
<tr class="odd">
<td><p><a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a></p></td>
<td><p>接続が開始された後に呼び出されます。</p></td>
</tr>
<tr class="even">
<td><p><a href="connectcomplete-and-disconnect-events-ado.md">切断</a></p></td>
<td><p>接続が終了した後に呼び出されます。</p></td>
</tr>
<tr class="odd">
<td><p><a href="endofrecordset-event-ado.md">EndOfRecordset</a></p></td>
<td><p><strong>Recordset</strong> の末尾以降の行に移動しようとすると呼び出されます。</p></td>
</tr>
<tr class="even">
<td><p><a href="executecomplete-event-ado.md">ExecuteComplete</a></p></td>
<td><p>コマンドが実行を終了した後に呼び出されます。</p></td>
</tr>
<tr class="odd">
<td><p><a href="fetchcomplete-event-ado.md">FetchComplete</a></p></td>
<td><p>長い非同期操作のすべてのレコードが、<strong>Recordset</strong> に取得された後に呼び出されます。</p></td>
</tr>
<tr class="even">
<td><p><a href="fetchprogress-event-ado.md">FetchProgress</a></p></td>
<td><p>長い非同期操作時に、現在までに <strong>Recordset</strong> に取得された行数を報告するために定期的に呼び出されます。</p></td>
</tr>
<tr class="odd">
<td><p><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></p></td>
<td><p>1 つまたは複数の <strong>Field</strong> オブジェクトの値が変更された後に呼び出されます。</p></td>
</tr>
<tr class="even">
<td><p><a href="infomessage-event-ado.md">InfoMessage</a></p></td>
<td><p><strong>ConnectionEvent</strong> 操作の間に警告が発生するたびに呼び出されます。</p></td>
</tr>
<tr class="odd">
<td><p><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></p></td>
<td><p><strong>Recordset</strong> における現在の位置が変更された後に呼び出されます。</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></p></td>
<td><p>1 つまたは複数のレコードが変更されると呼び出されます。</p></td>
</tr>
<tr class="odd">
<td><p><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></p></td>
<td><p><strong>Recordset</strong> が変更されると呼び出されます。</p></td>
</tr>
<tr class="even">
<td><p><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">RollbackTransComplete</a></p></td>
<td><p><strong>RollbackTrans</strong> 操作後に呼び出されます。</p></td>
</tr>
<tr class="odd">
<td><p><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></p></td>
<td><p>保留操作で <strong>Recordset</strong> 内の 1 つまたは複数の <strong>Field</strong> オブジェクトの値が変更される前に呼び出されます。</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></p></td>
<td><p><strong>Recordset</strong> 内の 1 つまたは複数のレコード (行) が変更される前に呼び出されます。</p></td>
</tr>
<tr class="odd">
<td><p><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></p></td>
<td><p>保留操作で <strong>Recordset</strong> が変更される前に呼び出されます。</p></td>
</tr>
<tr class="even">
<td><p><a href="willconnect-event-ado.md">WillConnect</a></p></td>
<td><p>接続が開始される前に呼び出されます。</p></td>
</tr>
<tr class="odd">
<td><p><a href="willexecute-event-ado.md">アクティビ ティー</a></p></td>
<td><p>保留中のコマンドがこの接続で実行される直前に呼び出され、ユーザーに、保留中の実行パラメーターの確認と変更を行う機会を与えます。</p></td>
</tr>
<tr class="even">
<td><p><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></p></td>
<td><p><strong>WillMove</strong>イベントが呼び出された<em>する前に</em>保留中の操作は、<strong>レコード セット</strong>内の現在位置を変更します。</p></td>
</tr>
</tbody>
</table>

<br/>