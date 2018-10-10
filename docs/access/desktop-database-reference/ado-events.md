---
title: ActiveX データ オブジェクト (ADO) のイベント
TOCTitle: ADO Events
ms:assetid: 84ca9525-99cb-4ba6-2a4d-172414b8f0cc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249576(v=office.15)
ms:contentKeyID: 48546041
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5938ed58e3b0074f69a4380fd4a0ac0be857084b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479264"
---
# <a name="ado-events"></a><span data-ttu-id="28560-102">ADO イベント</span><span class="sxs-lookup"><span data-stu-id="28560-102">ADO Events</span></span>


<span data-ttu-id="28560-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="28560-103">**Applies to**: Access 2013 | Office 2013</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="28560-104"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete</a></span><span class="sxs-lookup"><span data-stu-id="28560-104"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete</a></span></span></p></td>
<td><p><span data-ttu-id="28560-105"><strong>BeginTrans</strong> の操作が終了した後に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="28560-105">Called after the <strong>BeginTrans</strong> operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28560-106"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">CommitTransComplete</a></span><span class="sxs-lookup"><span data-stu-id="28560-106"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">CommitTransComplete</a></span></span></p></td>
<td><p><span data-ttu-id="28560-107"><strong>CommitTrans</strong> の操作が終了した後に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="28560-107">Called after the <strong>CommitTrans</strong> operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28560-108"><a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a></span><span class="sxs-lookup"><span data-stu-id="28560-108"><a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a></span></span></p></td>
<td><p><span data-ttu-id="28560-109">接続が開始された後に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="28560-109">Called after a connection starts.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28560-110"><a href="connectcomplete-and-disconnect-events-ado.md">切断</a></span><span class="sxs-lookup"><span data-stu-id="28560-110"><a href="connectcomplete-and-disconnect-events-ado.md">Disconnect</a></span></span></p></td>
<td><p><span data-ttu-id="28560-111">接続が終了した後に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="28560-111">Called after a connection ends.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28560-112"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span><span class="sxs-lookup"><span data-stu-id="28560-112"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="28560-113"><strong>Recordset</strong> の末尾以降の行に移動しようとすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="28560-113">Called when there is an attempt to move to a row past the end of the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28560-114"><a href="executecomplete-event-ado.md">ExecuteComplete</a></span><span class="sxs-lookup"><span data-stu-id="28560-114"><a href="executecomplete-event-ado.md">ExecuteComplete</a></span></span></p></td>
<td><p><span data-ttu-id="28560-115">コマンドが実行を終了した後に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="28560-115">Called after a command has finished executing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28560-116"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span><span class="sxs-lookup"><span data-stu-id="28560-116"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span></span></p></td>
<td><p><span data-ttu-id="28560-117">長い非同期操作のすべてのレコードが、<strong>Recordset</strong> に取得された後に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="28560-117">Called after all the records in a lengthy asynchronous operation have been retrieved into the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28560-118"><a href="fetchprogress-event-ado.md">FetchProgress</a></span><span class="sxs-lookup"><span data-stu-id="28560-118"><a href="fetchprogress-event-ado.md">FetchProgress</a></span></span></p></td>
<td><p><span data-ttu-id="28560-119">長い非同期操作時に、現在までに <strong>Recordset</strong> に取得された行数を報告するために定期的に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="28560-119">Called periodically during a lengthy asynchronous operation to report how many rows have currently been retrieved into the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28560-120"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="28560-120"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="28560-121">1 つまたは複数の <strong>Field</strong> オブジェクトの値が変更された後に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="28560-121">Called after the value of one or more <strong>Field</strong> objects has changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28560-122"><a href="infomessage-event-ado.md">InfoMessage</a></span><span class="sxs-lookup"><span data-stu-id="28560-122"><a href="infomessage-event-ado.md">InfoMessage</a></span></span></p></td>
<td><p><span data-ttu-id="28560-123"><strong>ConnectionEvent</strong> 操作の間に警告が発生するたびに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="28560-123">Called whenever a warning occurs during a <strong>ConnectionEvent</strong> operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28560-124"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span><span class="sxs-lookup"><span data-stu-id="28560-124"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span></span></p></td>
<td><p><span data-ttu-id="28560-125"><strong>Recordset</strong> における現在の位置が変更された後に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="28560-125">Called after the current position in the <strong>Recordset</strong> changes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28560-126"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="28560-126"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="28560-127">1 つまたは複数のレコードが変更されると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="28560-127">Called after one or more records change.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28560-128"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="28560-128"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="28560-129"><strong>Recordset</strong> が変更されると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="28560-129">Called after the <strong>Recordset</strong> has changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28560-130"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">RollbackTransComplete</a></span><span class="sxs-lookup"><span data-stu-id="28560-130"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">RollbackTransComplete</a></span></span></p></td>
<td><p><span data-ttu-id="28560-131"><strong>RollbackTrans</strong> 操作後に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="28560-131">Called after the <strong>RollbackTrans</strong> operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28560-132"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span><span class="sxs-lookup"><span data-stu-id="28560-132"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span></span></p></td>
<td><p><span data-ttu-id="28560-133">保留操作で <strong>Recordset</strong> 内の 1 つまたは複数の <strong>Field</strong> オブジェクトの値が変更される前に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="28560-133">Called before a pending operation changes the value of one or more <strong>Field</strong> objects in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28560-134"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span><span class="sxs-lookup"><span data-stu-id="28560-134"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span></span></p></td>
<td><p><span data-ttu-id="28560-135"><strong>Recordset</strong> 内の 1 つまたは複数のレコード (行) が変更される前に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="28560-135">Called before one or more records (rows) in the <strong>Recordset</strong> change.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28560-136"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span><span class="sxs-lookup"><span data-stu-id="28560-136"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="28560-137">保留操作で <strong>Recordset</strong> が変更される前に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="28560-137">Called before a pending operation changes the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28560-138"><a href="willconnect-event-ado.md">WillConnect</a></span><span class="sxs-lookup"><span data-stu-id="28560-138"><a href="willconnect-event-ado.md">WillConnect</a></span></span></p></td>
<td><p><span data-ttu-id="28560-139">接続が開始される前に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="28560-139">Called before a connection starts.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28560-140"><a href="willexecute-event-ado.md">アクティビ ティー</a></span><span class="sxs-lookup"><span data-stu-id="28560-140"><a href="willexecute-event-ado.md">WillExecute</a></span></span></p></td>
<td><p><span data-ttu-id="28560-141">保留中のコマンドがこの接続で実行される直前に呼び出され、ユーザーに、保留中の実行パラメーターの確認と変更を行う機会を与えます。</span><span class="sxs-lookup"><span data-stu-id="28560-141">Called just before a pending command executes on this connection and affords the user an opportunity to examine and modify the pending execution parameters.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28560-142"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span><span class="sxs-lookup"><span data-stu-id="28560-142"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span></span></p></td>
<td><p><span data-ttu-id="28560-143"><strong>WillMove</strong>イベントが呼び出された<em>する前に</em>保留中の操作は、<strong>レコード セット</strong>内の現在位置を変更します。</span><span class="sxs-lookup"><span data-stu-id="28560-143">The <strong>WillMove</strong> event is called <em>before</em> a pending operation changes the current position in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>
