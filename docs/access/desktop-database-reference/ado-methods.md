---
title: ActiveX データオブジェクト (ADO) メソッド
TOCTitle: ADO methods
ms:assetid: 1fd965a0-711c-e199-822c-b9575c5034bd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248984(v=office.15)
ms:contentKeyID: 48543651
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3169b7eaab6ad290bfc385881f5de69edc80111f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283283"
---
# <a name="ado-methods"></a>ADO のメソッド

**適用先:** Access 2013、Office 2013

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th>メソッド</th>
<th>説明</th>
</tr>
<tr class="odd">
<td><p><a href="addnew-method-ado.md">AddNew</a></p></td>
<td><p>更新可能な <strong>Recordset</strong> オブジェクトの新しいレコードを作成します。</p></td>
</tr>
<tr class="even">
<td><p><a href="append-method-ado.md">Append</a></p></td>
<td><p>コレクションにオブジェクトを追加します。コレクションが <strong>Fields</strong> である場合は、コレクションに追加する前に、新しい <strong>Field</strong> オブジェクトを作成できます。</p></td>
</tr>
<tr class="odd">
<td><p><a href="appendchunk-method-ado.md">AppendChunk</a></p></td>
<td><p>大きなサイズのテキストまたはバイナリ データの <strong>Field</strong> オブジェクト、または <strong>Parameter</strong> オブジェクトにデータを追加します。</p></td>
</tr>
<tr class="even">
<td><p><a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">BeginTrans、CommitTrans、RollbackTrans</a></p></td>
<td><p><strong>Connection</strong> オブジェクト内のトランザクション処理を次のように管理します。<br/><br/><strong>BeginTrans</strong> は、新しいトランザクションを開始します。<br/><br/>
<strong>CommitTrans</strong> は、すべての変更を保存して現在のトランザクションを終了します。新しいトランザクションを開始する場合もあります。<br/><br/>
<strong>RollbackTrans</strong> -すべての変更をキャンセルし、現在のトランザクションを終了します。 新しいトランザクションを開始する場合もあります。</p></td>
</tr>
<tr class="odd">
<td><p><a href="cancel-method-ado.md">Cancel</a></p></td>
<td><p>保留中の非同期メソッド呼び出しの実行をキャンセルします。</p></td>
</tr>
<tr class="even">
<td><p><a href="cancelbatch-method-ado.md">CancelBatch</a></p></td>
<td><p>保留中のバッチ更新をキャンセルします。</p></td>
</tr>
<tr class="odd">
<td><p><a href="cancelupdate-method-ado.md">CancelUpdate</a></p></td>
<td><p><strong>Update</strong> メソッドを呼び出す前に行った、<strong>Recordset</strong> オブジェクトのカレント行か新規行、または <strong>Record</strong> オブジェクトの <strong>Fields</strong> コレクションをキャンセルします。</p></td>
</tr>
<tr class="even">
<td><p><a href="clear-method-ado.md">Clear</a></p></td>
<td><p><strong>Errors</strong> コレクションからすべての <strong>Error</strong> オブジェクトを削除します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="clone-method-ado.md">Clone</a></p></td>
<td><p>既存の <strong>Recordset</strong> オブジェクトから <strong>Recordset</strong> オブジェクトの複製を作成します。 必要に応じて、複製を読み取り専用に指定できます。</p></td>
</tr>
<tr class="even">
<td><p><a href="close-method-ado.md">Close</a></p></td>
<td><p>開いているオブジェクトおよびそれに従属するすべてのオブジェクトを閉じます。</p></td>
</tr>
<tr class="odd">
<td><p><a href="comparebookmarks-method-ado.md">CompareBookmarks</a></p></td>
<td><p>2 つのブックマークを比較して、相対的な位置を示す値を返します。</p></td>
</tr>
<tr class="even">
<td><p><a href="copyrecord-method-ado.md">CopyRecord</a></p></td>
<td><p>ファイルまたはディレクトリとその内容を、別の場所にコピーします。</p></td>
</tr>
<tr class="odd">
<td><p><a href="copyto-method-ado.md">CopyTo</a></p></td>
<td><p><strong>Stream</strong> オブジェクトから、指定した文字数またはバイト数 (<strong>Type</strong> によって決まる) のデータを別の <strong>Stream</strong> にコピーします。</p></td>
</tr>
<tr class="even">
<td><p><a href="createparameter-method-ado.md">CreateParameter</a></p></td>
<td><p>プロパティを指定して新しい <strong>Parameter</strong> オブジェクトを作成します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="delete-method-ado-parameters-collection.md">Delete (ADO Parameters コレクション)</a></p></td>
<td><p><strong>Parameters</strong> コレクションからオブジェクトを削除します。</p></td>
</tr>
<tr class="even">
<td><p><a href="delete-method-ado-fields-collection.md">Delete (ADO Fields コレクション)</a></p></td>
<td><p><strong>Fields</strong> コレクションからオブジェクトを削除します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="delete-method-ado-recordset.md">Delete (ADO Recordset)</a></p></td>
<td><p>カレント レコードまたはレコードのグループを削除します。</p></td>
</tr>
<tr class="even">
<td><p><a href="deleterecord-method-ado.md">DeleteRecord</a></p></td>
<td><p>ファイルまたはディレクトリとそのすべてのサブディレクトリを削除します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command">Execute (ADO Command)</a></p></td>
<td><p><strong>CommandText</strong> プロパティで指定されたクエリ、SQL ステートメント、またはストアド プロシージャを実行します。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection">Execute (ADO Connection)</a></p></td>
<td><p>指定されたクエリ、SQL ステートメント、ストアド プロシージャ、またはプロバイダー固有のテキストを実行します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="find-method-ado.md">Find</a></p></td>
<td><p>指定した条件を満たす行を <strong>Recordset</strong> から検索します。</p></td>
</tr>
<tr class="even">
<td><p><a href="flush-method-ado.md">揃え</a></p></td>
<td><p>ADO バッファーに残っている <strong>Stream</strong> の内容を、<strong>Stream</strong> に関連付けられた、基になるオブジェクトに反映します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="getchildren-method-ado.md">GetChildren</a></p></td>
<td><p><strong>Record</strong> で表されるディレクトリ内のファイルとサブディレクトリを表す行を含む <strong>Recordset</strong> を返します。</p></td>
</tr>
<tr class="even">
<td><p><a href="getchunk-method-ado.md">GetChunk</a></p></td>
<td><p>サイズの大きいテキスト データやバイナリ データの <strong>Field</strong> オブジェクトから、内容の全部または一部を返します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="getrows-method-ado.md">GetRows</a></p></td>
<td><p>複数の <strong>Recordset</strong> オブジェクト レコードを配列に取り込みます。</p></td>
</tr>
<tr class="even">
<td><p><a href="getstring-method-ado.md">GetString</a></p></td>
<td><p><strong>Recordset</strong> を文字列として返します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="loadfromfile-method-ado.md">LoadFromFile</a></p></td>
<td><p>既存のファイルの内容を <strong>Stream</strong> に読み込みます。</p></td>
</tr>
<tr class="even">
<td><p><a href="move-method-ado.md">Move</a></p></td>
<td><p><strong>Recordset</strong> オブジェクトのカレント レコードの位置を移動します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst、MoveLast、MoveNext、MovePrevious</a></p></td>
<td><p>指定した <strong>Recordset</strong> オブジェクトの最初、最後、次、または前のレコードに移動して、そのレコードをカレント レコードにします。</p></td>
</tr>
<tr class="even">
<td><p><a href="moverecord-method-ado.md">MoveRecord</a></p></td>
<td><p>ファイルまたはディレクトリとその内容を、別の場所に移動します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="nextrecordset-method-ado.md">NextRecordset</a></p></td>
<td><p>一連のコマンド操作を実行して、現在の <strong>Recordset</strong> オブジェクトをクリアし、次の <strong>Recordset</strong> を返します。</p></td>
</tr>
<tr class="even">
<td><p><a href="open-method-ado-connection.md">Open (ADO Connection)</a></p></td>
<td><p>データ ソースへの接続を開きます。</p></td>
</tr>
<tr class="odd">
<td><p><a href="open-method-ado-record.md">Open (ADO Record)</a></p></td>
<td><p>既存の <strong>Record</strong> オブジェクトを開きます。または、新しいファイルかディレクトリを作成します。</p></td>
</tr>
<tr class="even">
<td><p><a href="open-method-ado-recordset.md">Open (ADO Recordset)</a></p></td>
<td><p>カーソルを開きます。</p></td>
</tr>
<tr class="odd">
<td><p><a href="open-method-ado-stream.md">Open (ADO Stream)</a></p></td>
<td><p>バイナリ データまたはテキスト データのストリームを操作するための <strong>Stream</strong> オブジェクトを開きます。</p></td>
</tr>
<tr class="even">
<td><p><a href="openschema-method-ado.md">OpenSchema</a></p></td>
<td><p>プロバイダーからデータベースのスキーマ情報を取得します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="read-method-ado.md">Read</a></p></td>
<td><p><strong>Stream</strong> オブジェクトから、指定されたバイト数を読み取ります。</p></td>
</tr>
<tr class="even">
<td><p><a href="readtext-method-ado.md">ReadText</a></p></td>
<td><p>テキスト <strong>Stream</strong> オブジェクトから、指定された文字数を読み取ります。</p></td>
</tr>
<tr class="odd">
<td><p><a href="refresh-method-ado.md">Refresh</a></p></td>
<td><p>コレクションのオブジェクトを更新し、プロバイダーから使用可能な、プロバイダーに固有のオブジェクトを反映します。</p></td>
</tr>
<tr class="even">
<td><p><a href="requery-method-ado.md">Requery</a></p></td>
<td><p>オブジェクトの基になるクエリを再実行して、<strong>Recordset</strong> オブジェクトのデータを更新します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="resync-method-ado.md">Resync</a></p></td>
<td><p>基になるデータベースの情報を基に、現在の <strong>Recordset</strong> オブジェクト、または <strong>Record</strong> オブジェクトの <strong>Fields</strong> コレクションのデータを再表示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="save-method-ado.md">Save</a></p></td>
<td><p><strong>Recordset</strong> をファイルまたは <strong>Stream</strong> オブジェクトに保存します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="savetofile-method-ado.md">SaveToFile</a></p></td>
<td><p><strong>Stream</strong> のバイナリの内容をファイルに保存します。</p></td>
</tr>
<tr class="even">
<td><p><a href="seek-method-ado.md">Seek</a></p></td>
<td><p><strong>Recordset</strong> のインデックスを検索して、指定された値と一致する行をすばやく探し、その行をカレント行にします。</p></td>
</tr>
<tr class="odd">
<td><p><a href="seteos-method-ado.md">SetEOS</a></p></td>
<td><p>ストリームの末尾の位置を設定します。</p></td>
</tr>
<tr class="even">
<td><p><a href="skipline-method-ado.md">SkipLine</a></p></td>
<td><p>テキスト ストリームを読み取っているときに、1 行全体をスキップします。</p></td>
</tr>
<tr class="odd">
<td><p><a href="stat-method-ado.md">Stat</a></p></td>
<td><p>開いているストリームに関する統計情報を取得します。</p></td>
</tr>
<tr class="even">
<td><p><a href="supports-method-ado.md">機能</a></p></td>
<td><p>指定した <strong>Recordset</strong> オブジェクトが特定の種類の機能をサポートしているかどうかを判別します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="update-method-ado.md">Update</a></p></td>
<td><p><strong>Recordset</strong> オブジェクトのカレント行、または <strong>Record</strong> オブジェクトの <strong>Fields</strong> コレクションに加えたすべての変更を保存します。</p></td>
</tr>
<tr class="even">
<td><p><a href="updatebatch-method-ado.md">UpdateBatch</a></p></td>
<td><p>保留中のバッチ更新をすべてディスクに書き込みます。</p></td>
</tr>
<tr class="odd">
<td><p><a href="write-method-ado.md">Write</a></p></td>
<td><p>バイナリ データを <strong>Stream</strong> オブジェクトに書き込みます。</p></td>
</tr>
<tr class="even">
<td><p><a href="writetext-method-ado.md">WriteText</a></p></td>
<td><p>指定されたテキスト文字列を <strong>Stream</strong> オブジェクトに書き込みます。</p></td>
</tr>
</tbody>
</table>

<br/>
