---
title: ActiveX データ オブジェクト (ADO) メソッド
TOCTitle: ADO methods
ms:assetid: 1fd965a0-711c-e199-822c-b9575c5034bd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248984(v=office.15)
ms:contentKeyID: 48543651
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5d5b08478b714a9b70e5cb08daff6e04b8883071
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026380"
---
# <a name="ado-methods"></a><span data-ttu-id="0069a-102">ADO のメソッド</span><span class="sxs-lookup"><span data-stu-id="0069a-102">ADO methods</span></span>

<span data-ttu-id="0069a-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="0069a-103">**Applies to**: Access 2013, Office 2013</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th><span data-ttu-id="0069a-104">メソッド</span><span class="sxs-lookup"><span data-stu-id="0069a-104">Method</span></span></th>
<th><span data-ttu-id="0069a-105">説明</span><span class="sxs-lookup"><span data-stu-id="0069a-105">Description</span></span></th>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0069a-106"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="0069a-106"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-107">更新可能な <strong>Recordset</strong> オブジェクトの新しいレコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="0069a-107">Creates a new record for an updatable <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0069a-108"><a href="append-method-ado.md">Append</a></span><span class="sxs-lookup"><span data-stu-id="0069a-108"><a href="append-method-ado.md">Append</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-p101">コレクションにオブジェクトを追加します。コレクションが <strong>Fields</strong> である場合は、コレクションに追加する前に、新しい <strong>Field</strong> オブジェクトを作成できます。</span><span class="sxs-lookup"><span data-stu-id="0069a-p101">Appends an object to a collection. If the collection is <strong>Fields</strong>, a new <strong>Field</strong> object may be created before it is appended to the collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0069a-111"><a href="appendchunk-method-ado.md">AppendChunk</a></span><span class="sxs-lookup"><span data-stu-id="0069a-111"><a href="appendchunk-method-ado.md">AppendChunk</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-112">大きなサイズのテキストまたはバイナリ データの <strong>Field</strong> オブジェクト、または <strong>Parameter</strong> オブジェクトにデータを追加します。</span><span class="sxs-lookup"><span data-stu-id="0069a-112">Appends data to a large text or binary data <strong>Field</strong>, or to a <strong>Parameter</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0069a-113"><a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">BeginTrans、CommitTrans、および RollbackTrans</a></span><span class="sxs-lookup"><span data-stu-id="0069a-113"><a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">BeginTrans, CommitTrans, and RollbackTrans</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-114"><strong>Connection</strong> オブジェクト内のトランザクション処理を次のように管理します。
</span><span class="sxs-lookup"><span data-stu-id="0069a-114">Manages transaction processing within a <strong>Connection</strong> object as follows:</span></span><br/><br/><span data-ttu-id="0069a-115"><strong>BeginTrans</strong> は、新しいトランザクションを開始します。</span><span class="sxs-lookup"><span data-stu-id="0069a-115"><strong>BeginTrans</strong> — Begins a new transaction.</span></span><br/><br/><span data-ttu-id="0069a-p102">
<strong>CommitTrans</strong> は、すべての変更を保存して現在のトランザクションを終了します。新しいトランザクションを開始する場合もあります。</span><span class="sxs-lookup"><span data-stu-id="0069a-p102">
<strong>CommitTrans</strong> — Saves any changes and ends the current transaction. It may also start a new transaction.</span></span><br/><br/><span data-ttu-id="0069a-118">
<strong>RollbackTrans</strong> -行った変更をキャンセルし、現在のトランザクションを終了します。</span><span class="sxs-lookup"><span data-stu-id="0069a-118">
<strong>RollbackTrans</strong> — Cancels any changes and ends the current transaction.</span></span> <span data-ttu-id="0069a-119">新しいトランザクションを開始する場合もあります。</span><span class="sxs-lookup"><span data-stu-id="0069a-119">It may also start a new transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0069a-120"><a href="cancel-method-ado.md">Cancel</a></span><span class="sxs-lookup"><span data-stu-id="0069a-120"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-121">保留中の非同期メソッド呼び出しの実行を取り消します。</span><span class="sxs-lookup"><span data-stu-id="0069a-121">Cancels execution of a pending, asynchronous method call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0069a-122"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="0069a-122"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-123">保留中のバッチ更新をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="0069a-123">Cancels a pending batch update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0069a-124"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="0069a-124"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-125"><strong>Update</strong> メソッドを呼び出す前に行った、 <strong>Recordset</strong> オブジェクトのカレント行や新規行に対する変更、または <strong>Record</strong> オブジェクトの <strong>Fields</strong> コレクションに対する変更を、すべてキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="0069a-125">Cancels any changes made to the current or new row of a <strong>Recordset</strong> object, or the <strong>Fields</strong> collection of a <strong>Record</strong> object, before calling the <strong>Update</strong> method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0069a-126"><a href="clear-method-ado.md">Clear</a></span><span class="sxs-lookup"><span data-stu-id="0069a-126"><a href="clear-method-ado.md">Clear</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-127"><strong>Errors</strong> コレクションからすべての <strong>Error</strong> オブジェクトを削除します。</span><span class="sxs-lookup"><span data-stu-id="0069a-127">Removes all the <strong>Error</strong> objects from the <strong>Errors</strong> collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0069a-128"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="0069a-128"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-p104">既存の <strong>Recordset</strong> オブジェクトから <strong>Recordset</strong> オブジェクトの複製を作成します。必要に応じて、複製を読み取り専用に指定できます。</span><span class="sxs-lookup"><span data-stu-id="0069a-p104">Creates a duplicate <strong>Recordset</strong> object from an existing <strong>Recordset</strong> object. Optionally, specifies that the clone be read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0069a-131"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="0069a-131"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-132">開いているオブジェクトおよびそれに関連するすべてのオブジェクトを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0069a-132">Closes an open object and any dependent objects.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0069a-133"><a href="comparebookmarks-method-ado.md">CompareBookmarks</a></span><span class="sxs-lookup"><span data-stu-id="0069a-133"><a href="comparebookmarks-method-ado.md">CompareBookmarks</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-134">2 つのブックマークを比較して、相対的な位置を示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="0069a-134">Compares two bookmarks and returns an indication of their relative values.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0069a-135"><a href="copyrecord-method-ado.md">定義</a></span><span class="sxs-lookup"><span data-stu-id="0069a-135"><a href="copyrecord-method-ado.md">CopyRecord</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-136">ファイルまたはディレクトリとその内容を、別の場所にコピーします。</span><span class="sxs-lookup"><span data-stu-id="0069a-136">Copies a file or directory, and its contents, to another location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0069a-137"><a href="copyto-method-ado.md">CopyTo</a></span><span class="sxs-lookup"><span data-stu-id="0069a-137"><a href="copyto-method-ado.md">CopyTo</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-138"><strong>Stream</strong> オブジェクトから、指定した文字数またはバイト数 ( <strong>Type</strong> によって決まる) のデータを別の <strong>Stream</strong> オブジェクトにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0069a-138">Copies the specified number of characters or bytes (depending on <strong>Type</strong>) in the <strong>Stream</strong> to another <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0069a-139"><a href="createparameter-method-ado.md">CreateParameter</a></span><span class="sxs-lookup"><span data-stu-id="0069a-139"><a href="createparameter-method-ado.md">CreateParameter</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-140">指定したプロパティを使用して、新規 <strong>Parameter</strong> オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="0069a-140">Creates a new <strong>Parameter</strong> object with the specified properties.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0069a-141"><a href="delete-method-ado-parameters-collection.md">(ADO Parameters コレクション) を削除します。</a></span><span class="sxs-lookup"><span data-stu-id="0069a-141"><a href="delete-method-ado-parameters-collection.md">Delete (ADO Parameters Collection)</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-142"><strong>Parameters</strong> コレクションからオブジェクトを削除します。</span><span class="sxs-lookup"><span data-stu-id="0069a-142">Deletes an object from the <strong>Parameters</strong> collection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0069a-143"><a href="delete-method-ado-fields-collection.md">(ADO Fields コレクション) を削除します。</a></span><span class="sxs-lookup"><span data-stu-id="0069a-143"><a href="delete-method-ado-fields-collection.md">Delete (ADO Fields Collection)</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-144"><strong>Fields</strong> コレクションからオブジェクトを削除します。</span><span class="sxs-lookup"><span data-stu-id="0069a-144">Deletes an object from the <strong>Fields</strong> collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0069a-145"><a href="delete-method-ado-recordset.md">(ADO レコード セット) を削除します。</a></span><span class="sxs-lookup"><span data-stu-id="0069a-145"><a href="delete-method-ado-recordset.md">Delete (ADO Recordset)</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-146">カレント レコードまたはレコードのグループを削除します。</span><span class="sxs-lookup"><span data-stu-id="0069a-146">Deletes the current record or a group of records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0069a-147"><a href="deleterecord-method-ado.md">DeleteRecord</a></span><span class="sxs-lookup"><span data-stu-id="0069a-147"><a href="deleterecord-method-ado.md">DeleteRecord</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-148">ファイルまたはディレクトリとそのすべてのサブディレクトリを削除します。</span><span class="sxs-lookup"><span data-stu-id="0069a-148">Deletes a file or directory, and all its subdirectories.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0069a-149"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command">(ADO コマンド) を実行します。</a></span><span class="sxs-lookup"><span data-stu-id="0069a-149"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command">Execute (ADO Command)</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-150"><strong>CommandText</strong> プロパティで指定されたクエリ、SQL ステートメント、またはストアド プロシージャを実行します。</span><span class="sxs-lookup"><span data-stu-id="0069a-150">Executes the query, SQL statement, or stored procedure specified in the <strong>CommandText</strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0069a-151"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection">(ADO 接続の場合) を実行します。</a></span><span class="sxs-lookup"><span data-stu-id="0069a-151"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection">Execute (ADO Connection)</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-152">指定されたクエリ、SQL ステートメント、ストアド プロシージャ、またはプロバイダー固有のテキストを実行します。</span><span class="sxs-lookup"><span data-stu-id="0069a-152">Executes the specified query, SQL statement, stored procedure, or provider-specific text.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0069a-153"><a href="find-method-ado.md">Find</a></span><span class="sxs-lookup"><span data-stu-id="0069a-153"><a href="find-method-ado.md">Find</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-154"><strong>Recordset</strong> から、指定した条件を満たす行を検索します。</span><span class="sxs-lookup"><span data-stu-id="0069a-154">Searches a <strong>Recordset</strong> for the row that satisfies the specified criteria.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0069a-155"><a href="flush-method-ado.md">フラッシュ</a></span><span class="sxs-lookup"><span data-stu-id="0069a-155"><a href="flush-method-ado.md">Flush</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-156">ADO バッファーに残っている <strong>Stream</strong> の内容を、 <strong>Stream</strong> に関連付けられた、基になるオブジェクトに反映します。</span><span class="sxs-lookup"><span data-stu-id="0069a-156">Forces the contents of the <strong>Stream</strong> remaining in the ADO buffer to the underlying object with which the <strong>Stream</strong> is associated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0069a-157"><a href="getchildren-method-ado.md">GetChildren</a></span><span class="sxs-lookup"><span data-stu-id="0069a-157"><a href="getchildren-method-ado.md">GetChildren</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-158">この<strong>レコード</strong>によって表されるディレクトリ内のサブディレクトリとファイルを表す行を持つ<strong>レコード セット</strong>を返します。</span><span class="sxs-lookup"><span data-stu-id="0069a-158">Returns a <strong>Recordset</strong> whose rows represent the files and subdirectories in the directory represented by this <strong>Record</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0069a-159"><a href="getchunk-method-ado.md">GetChunk</a></span><span class="sxs-lookup"><span data-stu-id="0069a-159"><a href="getchunk-method-ado.md">GetChunk</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-160">、サイズの大きなテキストまたはバイナリ データの<strong>Field</strong>オブジェクトの内容の一部または返します。</span><span class="sxs-lookup"><span data-stu-id="0069a-160">Returns all, or a portion of, the contents of a large text or binary data <strong>Field</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0069a-161"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="0069a-161"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-162"><strong>Recordset</strong> オブジェクトの複数のレコードを配列に取り込みます。</span><span class="sxs-lookup"><span data-stu-id="0069a-162">Retrieves multiple records of a <strong>Recordset</strong> object into an array.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0069a-163"><a href="getstring-method-ado.md">GetString</a></span><span class="sxs-lookup"><span data-stu-id="0069a-163"><a href="getstring-method-ado.md">GetString</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-164"><strong>Recordset</strong> を文字列として返します。</span><span class="sxs-lookup"><span data-stu-id="0069a-164">Returns the <strong>Recordset</strong> as a string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0069a-165"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span><span class="sxs-lookup"><span data-stu-id="0069a-165"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-166">既存のファイルの内容を <strong>Stream</strong> に読み込みます。</span><span class="sxs-lookup"><span data-stu-id="0069a-166">Loads the contents of an existing file into a <strong>Stream</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0069a-167"><a href="move-method-ado.md">Move</a></span><span class="sxs-lookup"><span data-stu-id="0069a-167"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-168"><strong>Recordset</strong> オブジェクトでカレント レコードの位置を移動します。</span><span class="sxs-lookup"><span data-stu-id="0069a-168">Moves the position of the current record in a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0069a-169"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst、MoveLast、MoveNext、および MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="0069a-169"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst, MoveLast, MoveNext, and MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-170">指定された <strong>Recordset</strong> オブジェクトの最初、最後、次、または前のレコードに移動して、そのレコードをカレント レコードにします。</span><span class="sxs-lookup"><span data-stu-id="0069a-170">Moves to the first, last, next, or previous record in a specified <strong>Recordset</strong> object and makes that record the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0069a-171"><a href="moverecord-method-ado.md">関係</a></span><span class="sxs-lookup"><span data-stu-id="0069a-171"><a href="moverecord-method-ado.md">MoveRecord</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-172">ファイルまたはディレクトリとその内容を、別の場所に移動します。</span><span class="sxs-lookup"><span data-stu-id="0069a-172">Moves a file, or a directory and its contents, to another location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0069a-173"><a href="nextrecordset-method-ado.md">NextRecordset</a></span><span class="sxs-lookup"><span data-stu-id="0069a-173"><a href="nextrecordset-method-ado.md">NextRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-174">現在の <strong>Recordset</strong> オブジェクトをクリアし、一連のコマンド操作を実行して次の <strong>Recordset</strong> を返します。</span><span class="sxs-lookup"><span data-stu-id="0069a-174">Clears the current <strong>Recordset</strong> object and returns the next <strong>Recordset</strong> by advancing through a series of commands.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0069a-175"><a href="open-method-ado-connection.md">(ADO 接続の場合) を開く</a></span><span class="sxs-lookup"><span data-stu-id="0069a-175"><a href="open-method-ado-connection.md">Open (ADO Connection)</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-176">データ ソースへの接続を開きます。</span><span class="sxs-lookup"><span data-stu-id="0069a-176">Opens a connection to a data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0069a-177"><a href="open-method-ado-record.md">(ADO のレコード) を開く</a></span><span class="sxs-lookup"><span data-stu-id="0069a-177"><a href="open-method-ado-record.md">Open (ADO Record)</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-178">既存の <strong>Record</strong> オブジェクトを開きます。または、新しいファイルかディレクトリを作成します。</span><span class="sxs-lookup"><span data-stu-id="0069a-178">Opens an existing <strong>Record</strong> object, or creates a new file or directory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0069a-179"><a href="open-method-ado-recordset.md">(ADO レコード セット) を開く</a></span><span class="sxs-lookup"><span data-stu-id="0069a-179"><a href="open-method-ado-recordset.md">Open (ADO Recordset)</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-180">カーソルを開きます。</span><span class="sxs-lookup"><span data-stu-id="0069a-180">Opens a cursor.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0069a-181"><a href="open-method-ado-stream.md">(ADO ストリーム) を開く</a></span><span class="sxs-lookup"><span data-stu-id="0069a-181"><a href="open-method-ado-stream.md">Open (ADO Stream)</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-182">バイナリ データまたはテキスト データのストリームを操作するために <strong>Stream</strong> オブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="0069a-182">Opens a <strong>Stream</strong> object to manipulate streams of binary or text data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0069a-183"><a href="openschema-method-ado.md">OpenSchema</a></span><span class="sxs-lookup"><span data-stu-id="0069a-183"><a href="openschema-method-ado.md">OpenSchema</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-184">プロバイダーからデータベースのスキーマ情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="0069a-184">Obtains database schema information from the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0069a-185"><a href="read-method-ado.md">Read</a></span><span class="sxs-lookup"><span data-stu-id="0069a-185"><a href="read-method-ado.md">Read</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-186"><strong>Stream</strong> オブジェクトから、指定されたバイト数を読み取ります。</span><span class="sxs-lookup"><span data-stu-id="0069a-186">Reads a specified number of bytes from a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0069a-187"><a href="readtext-method-ado.md">ReadText</a></span><span class="sxs-lookup"><span data-stu-id="0069a-187"><a href="readtext-method-ado.md">ReadText</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-188">テキスト <strong>Stream</strong> オブジェクトから、指定された文字数を読み取ります。</span><span class="sxs-lookup"><span data-stu-id="0069a-188">Reads a specified number of characters from a text <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0069a-189"><a href="refresh-method-ado.md">Refresh</a></span><span class="sxs-lookup"><span data-stu-id="0069a-189"><a href="refresh-method-ado.md">Refresh</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-190">コレクションのオブジェクトを更新し、プロバイダーから使用可能な、プロバイダーに固有のオブジェクトを反映します。</span><span class="sxs-lookup"><span data-stu-id="0069a-190">Updates the objects in a collection to reflect objects available from, and specific to, the provider.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0069a-191"><a href="requery-method-ado.md">Requery</a></span><span class="sxs-lookup"><span data-stu-id="0069a-191"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-192">オブジェクトの基になるクエリを再実行して、<strong>Recordset</strong> オブジェクトのデータを更新します。</span><span class="sxs-lookup"><span data-stu-id="0069a-192">Updates the data in a <strong>Recordset</strong> object by re-executing the query on which the object is based.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0069a-193"><a href="resync-method-ado.md">再同期</a></span><span class="sxs-lookup"><span data-stu-id="0069a-193"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-194">現在の <strong>Recordset</strong> オブジェクト、または <strong>Record</strong> オブジェクトの <strong>Fields</strong> コレクションのデータを、基になるデータベースのデータで更新します。</span><span class="sxs-lookup"><span data-stu-id="0069a-194">Refreshes the data in the current <strong>Recordset</strong> object, or <strong>Fields</strong> collection of a <strong>Record</strong> object, from the underlying database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0069a-195"><a href="save-method-ado.md">Save</a></span><span class="sxs-lookup"><span data-stu-id="0069a-195"><a href="save-method-ado.md">Save</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-196"><strong>Recordset</strong> をファイルまたは <strong>Stream</strong> オブジェクトに保存します。</span><span class="sxs-lookup"><span data-stu-id="0069a-196">Saves the <strong>Recordset</strong> in a file or <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0069a-197"><a href="savetofile-method-ado.md">SaveToFile</a></span><span class="sxs-lookup"><span data-stu-id="0069a-197"><a href="savetofile-method-ado.md">SaveToFile</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-198"><strong>Stream</strong> のバイナリの内容をファイルに保存します。</span><span class="sxs-lookup"><span data-stu-id="0069a-198">Saves the binary contents of a <strong>Stream</strong> to a file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0069a-199"><a href="seek-method-ado.md">Seek</a></span><span class="sxs-lookup"><span data-stu-id="0069a-199"><a href="seek-method-ado.md">Seek</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-200"><strong>Recordset</strong> のインデックスを検索して、指定された値と一致する行をすばやく探し、その行をカレント行にします。</span><span class="sxs-lookup"><span data-stu-id="0069a-200">Searches the index of a <strong>Recordset</strong> to quickly locate the row that matches the specified values, and changes the current row position to that row.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0069a-201"><a href="seteos-method-ado.md">SetEOS</a></span><span class="sxs-lookup"><span data-stu-id="0069a-201"><a href="seteos-method-ado.md">SetEOS</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-202">ストリームの末尾の位置を設定します。</span><span class="sxs-lookup"><span data-stu-id="0069a-202">Sets the position that is the end of the stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0069a-203"><a href="skipline-method-ado.md">SkipLine</a></span><span class="sxs-lookup"><span data-stu-id="0069a-203"><a href="skipline-method-ado.md">SkipLine</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-204">テキスト ストリームを読み取っているときに、1 行全体をスキップします。</span><span class="sxs-lookup"><span data-stu-id="0069a-204">Skips one entire line when reading a text stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0069a-205"><a href="stat-method-ado.md">Stat</a></span><span class="sxs-lookup"><span data-stu-id="0069a-205"><a href="stat-method-ado.md">Stat</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-206">開いているストリームに関する統計情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="0069a-206">Gets statistical information about an open stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0069a-207"><a href="supports-method-ado.md">サポートしています</a></span><span class="sxs-lookup"><span data-stu-id="0069a-207"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-208">指定された <strong>Recordset</strong> オブジェクトが特定の種類の機能をサポートしているかどうかを調べます。</span><span class="sxs-lookup"><span data-stu-id="0069a-208">Determines whether a specified <strong>Recordset</strong> object supports a particular type of functionality.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0069a-209"><a href="update-method-ado.md">Update</a></span><span class="sxs-lookup"><span data-stu-id="0069a-209"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-210"><strong>Recordset</strong> オブジェクトのカレント行、または <strong>Record</strong> オブジェクトの <strong>Fields</strong> コレクションに加えた変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="0069a-210">Saves any changes you make to the current row of a <strong>Recordset</strong> object, or the <strong>Fields</strong> collection of a <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0069a-211"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="0069a-211"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-212">保留中の一括更新をすべてディスクに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="0069a-212">Writes all pending batch updates to disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0069a-213"><a href="write-method-ado.md">Write</a></span><span class="sxs-lookup"><span data-stu-id="0069a-213"><a href="write-method-ado.md">Write</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-214">バイナリ データを <strong>Stream</strong> オブジェクトに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="0069a-214">Writes binary data to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0069a-215"><a href="writetext-method-ado.md">WriteText</a></span><span class="sxs-lookup"><span data-stu-id="0069a-215"><a href="writetext-method-ado.md">WriteText</a></span></span></p></td>
<td><p><span data-ttu-id="0069a-216">指定されたテキスト文字列を <strong>Stream</strong> オブジェクトに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="0069a-216">Writes a specified text string to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>