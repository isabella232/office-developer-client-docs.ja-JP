---
title: ActiveX データ オブジェクト (ADO) メソッド
TOCTitle: ADO Methods
ms:assetid: 1fd965a0-711c-e199-822c-b9575c5034bd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248984(v=office.15)
ms:contentKeyID: 48543651
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6ef05e7f322b769102ce25aab7dfc26a75b0aa22
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879334"
---
# <a name="ado-methods"></a><span data-ttu-id="9f97d-102">ADO メソッド</span><span class="sxs-lookup"><span data-stu-id="9f97d-102">ADO Methods</span></span>


<span data-ttu-id="9f97d-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="9f97d-103">**Applies to**: Access 2013, Office 2013</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9f97d-104"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-104"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-105">更新可能な <strong>Recordset</strong> オブジェクトの新しいレコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="9f97d-105">Creates a new record for an updatable <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f97d-106"><a href="append-method-ado.md">Append</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-106"><a href="append-method-ado.md">Append</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-p101">コレクションにオブジェクトを追加します。コレクションが <strong>Fields</strong> である場合は、コレクションに追加する前に、新しい <strong>Field</strong> オブジェクトを作成できます。</span><span class="sxs-lookup"><span data-stu-id="9f97d-p101">Appends an object to a collection. If the collection is <strong>Fields</strong>, a new <strong>Field</strong> object may be created before it is appended to the collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f97d-109"><a href="appendchunk-method-ado.md">AppendChunk</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-109"><a href="appendchunk-method-ado.md">AppendChunk</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-110">大きなサイズのテキストまたはバイナリ データの <strong>Field</strong> オブジェクト、または <strong>Parameter</strong> オブジェクトにデータを追加します。</span><span class="sxs-lookup"><span data-stu-id="9f97d-110">Appends data to a large text or binary data <strong>Field</strong>, or to a <strong>Parameter</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f97d-111"><a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">BeginTrans、CommitTrans、および RollbackTrans</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-111"><a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">BeginTrans, CommitTrans, and RollbackTrans</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-112"><strong>接続</strong>オブジェクト内の処理について次のようにトランザクションを管理する: <strong>BeginTrans</strong> : 新しいトランザクションを開始します。</span><span class="sxs-lookup"><span data-stu-id="9f97d-112">Manages transaction processing within a <strong>Connection</strong> object as follows: <strong>BeginTrans</strong> — Begins a new transaction.</span></span><br /><span data-ttu-id="9f97d-p102">
<strong>CommitTrans</strong> は、すべての変更を保存して現在のトランザクションを終了します。新しいトランザクションを開始する場合もあります。</span><span class="sxs-lookup"><span data-stu-id="9f97d-p102">
<strong>CommitTrans</strong> — Saves any changes and ends the current transaction. It may also start a new transaction.</span></span><br /><span data-ttu-id="9f97d-115">
<strong>RollbackTrans</strong> -行った変更をキャンセルし、現在のトランザクションを終了します。</span><span class="sxs-lookup"><span data-stu-id="9f97d-115">
<strong>RollbackTrans</strong> — Cancels any changes and ends the current transaction.</span></span> <span data-ttu-id="9f97d-116">新しいトランザクションを開始する場合もあります。</span><span class="sxs-lookup"><span data-stu-id="9f97d-116">It may also start a new transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f97d-117"><a href="cancel-method-ado.md">Cancel</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-117"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-118">保留中の非同期メソッド呼び出しの実行を取り消します。</span><span class="sxs-lookup"><span data-stu-id="9f97d-118">Cancels execution of a pending, asynchronous method call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f97d-119"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-119"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-120">保留中のバッチ更新をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="9f97d-120">Cancels a pending batch update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f97d-121"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-121"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-122"><strong>Update</strong> メソッドを呼び出す前に行った、 <strong>Recordset</strong> オブジェクトのカレント行や新規行に対する変更、または <strong>Record</strong> オブジェクトの <strong>Fields</strong> コレクションに対する変更を、すべてキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="9f97d-122">Cancels any changes made to the current or new row of a <strong>Recordset</strong> object, or the <strong>Fields</strong> collection of a <strong>Record</strong> object, before calling the <strong>Update</strong> method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f97d-123"><a href="clear-method-ado.md">Clear</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-123"><a href="clear-method-ado.md">Clear</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-124"><strong>Errors</strong> コレクションからすべての <strong>Error</strong> オブジェクトを削除します。</span><span class="sxs-lookup"><span data-stu-id="9f97d-124">Removes all the <strong>Error</strong> objects from the <strong>Errors</strong> collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f97d-125"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-125"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-p104">既存の <strong>Recordset</strong> オブジェクトから <strong>Recordset</strong> オブジェクトの複製を作成します。必要に応じて、複製を読み取り専用に指定できます。</span><span class="sxs-lookup"><span data-stu-id="9f97d-p104">Creates a duplicate <strong>Recordset</strong> object from an existing <strong>Recordset</strong> object. Optionally, specifies that the clone be read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f97d-128"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-128"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-129">開いているオブジェクトおよびそれに関連するすべてのオブジェクトを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9f97d-129">Closes an open object and any dependent objects.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f97d-130"><a href="comparebookmarks-method-ado.md">CompareBookmarks</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-130"><a href="comparebookmarks-method-ado.md">CompareBookmarks</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-131">2 つのブックマークを比較して、相対的な位置を示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="9f97d-131">Compares two bookmarks and returns an indication of their relative values.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f97d-132"><a href="copyrecord-method-ado.md">定義</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-132"><a href="copyrecord-method-ado.md">CopyRecord</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-133">ファイルまたはディレクトリとその内容を、別の場所にコピーします。</span><span class="sxs-lookup"><span data-stu-id="9f97d-133">Copies a file or directory, and its contents, to another location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f97d-134"><a href="copyto-method-ado.md">CopyTo</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-134"><a href="copyto-method-ado.md">CopyTo</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-135"><strong>Stream</strong> オブジェクトから、指定した文字数またはバイト数 ( <strong>Type</strong> によって決まる) のデータを別の <strong>Stream</strong> オブジェクトにコピーします。</span><span class="sxs-lookup"><span data-stu-id="9f97d-135">Copies the specified number of characters or bytes (depending on <strong>Type</strong>) in the <strong>Stream</strong> to another <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f97d-136"><a href="createparameter-method-ado.md">CreateParameter</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-136"><a href="createparameter-method-ado.md">CreateParameter</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-137">指定したプロパティを使用して、新規 <strong>Parameter</strong> オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="9f97d-137">Creates a new <strong>Parameter</strong> object with the specified properties.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f97d-138"><a href="delete-method-ado-parameters-collection.md">(ADO Parameters コレクション) を削除します。</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-138"><a href="delete-method-ado-parameters-collection.md">Delete (ADO Parameters Collection)</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-139"><strong>Parameters</strong> コレクションからオブジェクトを削除します。</span><span class="sxs-lookup"><span data-stu-id="9f97d-139">Deletes an object from the <strong>Parameters</strong> collection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f97d-140"><a href="delete-method-ado-fields-collection.md">(ADO Fields コレクション) を削除します。</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-140"><a href="delete-method-ado-fields-collection.md">Delete (ADO Fields Collection)</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-141"><strong>Fields</strong> コレクションからオブジェクトを削除します。</span><span class="sxs-lookup"><span data-stu-id="9f97d-141">Deletes an object from the <strong>Fields</strong> collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f97d-142"><a href="delete-method-ado-recordset.md">(ADO レコード セット) を削除します。</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-142"><a href="delete-method-ado-recordset.md">Delete (ADO Recordset)</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-143">カレント レコードまたはレコードのグループを削除します。</span><span class="sxs-lookup"><span data-stu-id="9f97d-143">Deletes the current record or a group of records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f97d-144"><a href="deleterecord-method-ado.md">DeleteRecord</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-144"><a href="deleterecord-method-ado.md">DeleteRecord</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-145">ファイルまたはディレクトリとそのすべてのサブディレクトリを削除します。</span><span class="sxs-lookup"><span data-stu-id="9f97d-145">Deletes a file or directory, and all its subdirectories.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f97d-146"><a href="https://msdn.microsoft.com/library/jj248785(v=office.15)">(ADO コマンド) を実行します。</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-146"><a href="https://msdn.microsoft.com/library/jj248785(v=office.15)">Execute (ADO Command)</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-147"><strong>CommandText</strong> プロパティで指定されたクエリ、SQL ステートメント、またはストアド プロシージャを実行します。</span><span class="sxs-lookup"><span data-stu-id="9f97d-147">Executes the query, SQL statement, or stored procedure specified in the <strong>CommandText</strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f97d-148"><a href="https://msdn.microsoft.com/library/jj249832(v=office.15)">(ADO 接続の場合) を実行します。</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-148"><a href="https://msdn.microsoft.com/library/jj249832(v=office.15)">Execute (ADO Connection)</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-149">指定されたクエリ、SQL ステートメント、ストアド プロシージャ、またはプロバイダー固有のテキストを実行します。</span><span class="sxs-lookup"><span data-stu-id="9f97d-149">Executes the specified query, SQL statement, stored procedure, or provider-specific text.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f97d-150"><a href="find-method-ado.md">Find</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-150"><a href="find-method-ado.md">Find</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-151"><strong>Recordset</strong> から、指定した条件を満たす行を検索します。</span><span class="sxs-lookup"><span data-stu-id="9f97d-151">Searches a <strong>Recordset</strong> for the row that satisfies the specified criteria.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f97d-152"><a href="flush-method-ado.md">フラッシュ</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-152"><a href="flush-method-ado.md">Flush</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-153">ADO バッファーに残っている <strong>Stream</strong> の内容を、 <strong>Stream</strong> に関連付けられた、基になるオブジェクトに反映します。</span><span class="sxs-lookup"><span data-stu-id="9f97d-153">Forces the contents of the <strong>Stream</strong> remaining in the ADO buffer to the underlying object with which the <strong>Stream</strong> is associated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f97d-154"><a href="getchildren-method-ado.md">GetChildren</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-154"><a href="getchildren-method-ado.md">GetChildren</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-155">この<strong>レコード</strong>によって表されるディレクトリ内のサブディレクトリとファイルを表す行を持つ<strong>レコード セット</strong>を返します。</span><span class="sxs-lookup"><span data-stu-id="9f97d-155">Returns a <strong>Recordset</strong> whose rows represent the files and subdirectories in the directory represented by this <strong>Record</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f97d-156"><a href="getchunk-method-ado.md">GetChunk</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-156"><a href="getchunk-method-ado.md">GetChunk</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-157">、サイズの大きなテキストまたはバイナリ データの<strong>Field</strong>オブジェクトの内容の一部または返します。</span><span class="sxs-lookup"><span data-stu-id="9f97d-157">Returns all, or a portion of, the contents of a large text or binary data <strong>Field</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f97d-158"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-158"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-159"><strong>Recordset</strong> オブジェクトの複数のレコードを配列に取り込みます。</span><span class="sxs-lookup"><span data-stu-id="9f97d-159">Retrieves multiple records of a <strong>Recordset</strong> object into an array.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f97d-160"><a href="getstring-method-ado.md">GetString</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-160"><a href="getstring-method-ado.md">GetString</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-161"><strong>Recordset</strong> を文字列として返します。</span><span class="sxs-lookup"><span data-stu-id="9f97d-161">Returns the <strong>Recordset</strong> as a string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f97d-162"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-162"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-163">既存のファイルの内容を <strong>Stream</strong> に読み込みます。</span><span class="sxs-lookup"><span data-stu-id="9f97d-163">Loads the contents of an existing file into a <strong>Stream</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f97d-164"><a href="move-method-ado.md">Move</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-164"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-165"><strong>Recordset</strong> オブジェクトでカレント レコードの位置を移動します。</span><span class="sxs-lookup"><span data-stu-id="9f97d-165">Moves the position of the current record in a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f97d-166"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst、MoveLast、MoveNext、および MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-166"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst, MoveLast, MoveNext, and MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-167">指定された <strong>Recordset</strong> オブジェクトの最初、最後、次、または前のレコードに移動して、そのレコードをカレント レコードにします。</span><span class="sxs-lookup"><span data-stu-id="9f97d-167">Moves to the first, last, next, or previous record in a specified <strong>Recordset</strong> object and makes that record the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f97d-168"><a href="moverecord-method-ado.md">関係</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-168"><a href="moverecord-method-ado.md">MoveRecord</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-169">ファイルまたはディレクトリとその内容を、別の場所に移動します。</span><span class="sxs-lookup"><span data-stu-id="9f97d-169">Moves a file, or a directory and its contents, to another location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f97d-170"><a href="nextrecordset-method-ado.md">NextRecordset</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-170"><a href="nextrecordset-method-ado.md">NextRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-171">現在の <strong>Recordset</strong> オブジェクトをクリアし、一連のコマンド操作を実行して次の <strong>Recordset</strong> を返します。</span><span class="sxs-lookup"><span data-stu-id="9f97d-171">Clears the current <strong>Recordset</strong> object and returns the next <strong>Recordset</strong> by advancing through a series of commands.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f97d-172"><a href="open-method-ado-connection.md">(ADO 接続の場合) を開く</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-172"><a href="open-method-ado-connection.md">Open (ADO Connection)</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-173">データ ソースへの接続を開きます。</span><span class="sxs-lookup"><span data-stu-id="9f97d-173">Opens a connection to a data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f97d-174"><a href="open-method-ado-record.md">(ADO のレコード) を開く</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-174"><a href="open-method-ado-record.md">Open (ADO Record)</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-175">既存の <strong>Record</strong> オブジェクトを開きます。または、新しいファイルかディレクトリを作成します。</span><span class="sxs-lookup"><span data-stu-id="9f97d-175">Opens an existing <strong>Record</strong> object, or creates a new file or directory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f97d-176"><a href="open-method-ado-recordset.md">(ADO レコード セット) を開く</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-176"><a href="open-method-ado-recordset.md">Open (ADO Recordset)</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-177">カーソルを開きます。</span><span class="sxs-lookup"><span data-stu-id="9f97d-177">Opens a cursor.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f97d-178"><a href="open-method-ado-stream.md">(ADO ストリーム) を開く</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-178"><a href="open-method-ado-stream.md">Open (ADO Stream)</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-179">バイナリ データまたはテキスト データのストリームを操作するために <strong>Stream</strong> オブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="9f97d-179">Opens a <strong>Stream</strong> object to manipulate streams of binary or text data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f97d-180"><a href="openschema-method-ado.md">OpenSchema</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-180"><a href="openschema-method-ado.md">OpenSchema</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-181">プロバイダーからデータベースのスキーマ情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="9f97d-181">Obtains database schema information from the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f97d-182"><a href="read-method-ado.md">Read</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-182"><a href="read-method-ado.md">Read</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-183"><strong>Stream</strong> オブジェクトから、指定されたバイト数を読み取ります。</span><span class="sxs-lookup"><span data-stu-id="9f97d-183">Reads a specified number of bytes from a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f97d-184"><a href="readtext-method-ado.md">ReadText</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-184"><a href="readtext-method-ado.md">ReadText</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-185">テキスト <strong>Stream</strong> オブジェクトから、指定された文字数を読み取ります。</span><span class="sxs-lookup"><span data-stu-id="9f97d-185">Reads a specified number of characters from a text <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f97d-186"><a href="refresh-method-ado.md">Refresh</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-186"><a href="refresh-method-ado.md">Refresh</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-187">コレクションのオブジェクトを更新し、プロバイダーから使用可能な、プロバイダーに固有のオブジェクトを反映します。</span><span class="sxs-lookup"><span data-stu-id="9f97d-187">Updates the objects in a collection to reflect objects available from, and specific to, the provider.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f97d-188"><a href="requery-method-ado.md">Requery</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-188"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-189">オブジェクトの基になるクエリを再実行して、<strong>Recordset</strong> オブジェクトのデータを更新します。</span><span class="sxs-lookup"><span data-stu-id="9f97d-189">Updates the data in a <strong>Recordset</strong> object by re-executing the query on which the object is based.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f97d-190"><a href="resync-method-ado.md">再同期</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-190"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-191">現在の <strong>Recordset</strong> オブジェクト、または <strong>Record</strong> オブジェクトの <strong>Fields</strong> コレクションのデータを、基になるデータベースのデータで更新します。</span><span class="sxs-lookup"><span data-stu-id="9f97d-191">Refreshes the data in the current <strong>Recordset</strong> object, or <strong>Fields</strong> collection of a <strong>Record</strong> object, from the underlying database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f97d-192"><a href="save-method-ado.md">Save</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-192"><a href="save-method-ado.md">Save</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-193"><strong>Recordset</strong> をファイルまたは <strong>Stream</strong> オブジェクトに保存します。</span><span class="sxs-lookup"><span data-stu-id="9f97d-193">Saves the <strong>Recordset</strong> in a file or <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f97d-194"><a href="savetofile-method-ado.md">SaveToFile</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-194"><a href="savetofile-method-ado.md">SaveToFile</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-195"><strong>Stream</strong> のバイナリの内容をファイルに保存します。</span><span class="sxs-lookup"><span data-stu-id="9f97d-195">Saves the binary contents of a <strong>Stream</strong> to a file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f97d-196"><a href="seek-method-ado.md">Seek</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-196"><a href="seek-method-ado.md">Seek</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-197"><strong>Recordset</strong> のインデックスを検索して、指定された値と一致する行をすばやく探し、その行をカレント行にします。</span><span class="sxs-lookup"><span data-stu-id="9f97d-197">Searches the index of a <strong>Recordset</strong> to quickly locate the row that matches the specified values, and changes the current row position to that row.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f97d-198"><a href="seteos-method-ado.md">SetEOS</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-198"><a href="seteos-method-ado.md">SetEOS</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-199">ストリームの末尾の位置を設定します。</span><span class="sxs-lookup"><span data-stu-id="9f97d-199">Sets the position that is the end of the stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f97d-200"><a href="skipline-method-ado.md">SkipLine</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-200"><a href="skipline-method-ado.md">SkipLine</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-201">テキスト ストリームを読み取っているときに、1 行全体をスキップします。</span><span class="sxs-lookup"><span data-stu-id="9f97d-201">Skips one entire line when reading a text stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f97d-202"><a href="stat-method-ado.md">Stat</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-202"><a href="stat-method-ado.md">Stat</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-203">開いているストリームに関する統計情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="9f97d-203">Gets statistical information about an open stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f97d-204"><a href="supports-method-ado.md">サポートしています</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-204"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-205">指定された <strong>Recordset</strong> オブジェクトが特定の種類の機能をサポートしているかどうかを調べます。</span><span class="sxs-lookup"><span data-stu-id="9f97d-205">Determines whether a specified <strong>Recordset</strong> object supports a particular type of functionality.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f97d-206"><a href="update-method-ado.md">Update</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-206"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-207"><strong>Recordset</strong> オブジェクトのカレント行、または <strong>Record</strong> オブジェクトの <strong>Fields</strong> コレクションに加えた変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="9f97d-207">Saves any changes you make to the current row of a <strong>Recordset</strong> object, or the <strong>Fields</strong> collection of a <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f97d-208"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-208"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-209">保留中の一括更新をすべてディスクに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="9f97d-209">Writes all pending batch updates to disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f97d-210"><a href="write-method-ado.md">Write</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-210"><a href="write-method-ado.md">Write</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-211">バイナリ データを <strong>Stream</strong> オブジェクトに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="9f97d-211">Writes binary data to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f97d-212"><a href="writetext-method-ado.md">WriteText</a></span><span class="sxs-lookup"><span data-stu-id="9f97d-212"><a href="writetext-method-ado.md">WriteText</a></span></span></p></td>
<td><p><span data-ttu-id="9f97d-213">指定されたテキスト文字列を <strong>Stream</strong> オブジェクトに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="9f97d-213">Writes a specified text string to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>

