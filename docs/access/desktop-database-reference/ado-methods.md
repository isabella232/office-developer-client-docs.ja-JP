---
title: ActiveX データ オブジェクト (ADO) メソッド
TOCTitle: ADO Methods
ms:assetid: 1fd965a0-711c-e199-822c-b9575c5034bd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248984(v=office.15)
ms:contentKeyID: 48543651
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7b7a685352063c3c1dd4c9bbd62e9c1fc4cdfe11
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476453"
---
# <a name="ado-methods"></a>ADO メソッド


**適用されます**Access 2013 |。Office 2013

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
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
<td><p><a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">BeginTrans、CommitTrans、および RollbackTrans</a></p></td>
<td><p><strong>接続</strong>オブジェクト内の処理について次のようにトランザクションを管理する: <strong>BeginTrans</strong> : 新しいトランザクションを開始します。<br />
<strong>CommitTrans</strong> は、すべての変更を保存して現在のトランザクションを終了します。新しいトランザクションを開始する場合もあります。<br />
<strong>RollbackTrans</strong> -行った変更をキャンセルし、現在のトランザクションを終了します。 新しいトランザクションを開始する場合もあります。</p></td>
</tr>
<tr class="odd">
<td><p><a href="cancel-method-ado.md">Cancel</a></p></td>
<td><p>保留中の非同期メソッド呼び出しの実行を取り消します。</p></td>
</tr>
<tr class="even">
<td><p><a href="cancelbatch-method-ado.md">CancelBatch</a></p></td>
<td><p>保留中のバッチ更新をキャンセルします。</p></td>
</tr>
<tr class="odd">
<td><p><a href="cancelupdate-method-ado.md">CancelUpdate</a></p></td>
<td><p><strong>Update</strong> メソッドを呼び出す前に行った、 <strong>Recordset</strong> オブジェクトのカレント行や新規行に対する変更、または <strong>Record</strong> オブジェクトの <strong>Fields</strong> コレクションに対する変更を、すべてキャンセルします。</p></td>
</tr>
<tr class="even">
<td><p><a href="clear-method-ado.md">Clear</a></p></td>
<td><p><strong>Errors</strong> コレクションからすべての <strong>Error</strong> オブジェクトを削除します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="clone-method-ado.md">Clone</a></p></td>
<td><p>既存の <strong>Recordset</strong> オブジェクトから <strong>Recordset</strong> オブジェクトの複製を作成します。必要に応じて、複製を読み取り専用に指定できます。</p></td>
</tr>
<tr class="even">
<td><p><a href="close-method-ado.md">Close</a></p></td>
<td><p>開いているオブジェクトおよびそれに関連するすべてのオブジェクトを閉じます。</p></td>
</tr>
<tr class="odd">
<td><p><a href="comparebookmarks-method-ado.md">CompareBookmarks</a></p></td>
<td><p>2 つのブックマークを比較して、相対的な位置を示す値を返します。</p></td>
</tr>
<tr class="even">
<td><p><a href="copyrecord-method-ado.md">定義</a></p></td>
<td><p>ファイルまたはディレクトリとその内容を、別の場所にコピーします。</p></td>
</tr>
<tr class="odd">
<td><p><a href="copyto-method-ado.md">CopyTo</a></p></td>
<td><p><strong>Stream</strong> オブジェクトから、指定した文字数またはバイト数 ( <strong>Type</strong> によって決まる) のデータを別の <strong>Stream</strong> オブジェクトにコピーします。</p></td>
</tr>
<tr class="even">
<td><p><a href="createparameter-method-ado.md">CreateParameter</a></p></td>
<td><p>指定したプロパティを使用して、新規 <strong>Parameter</strong> オブジェクトを作成します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="delete-method-ado-parameters-collection.md">(ADO Parameters コレクション) を削除します。</a></p></td>
<td><p><strong>Parameters</strong> コレクションからオブジェクトを削除します。</p></td>
</tr>
<tr class="even">
<td><p><a href="delete-method-ado-fields-collection.md">(ADO Fields コレクション) を削除します。</a></p></td>
<td><p><strong>Fields</strong> コレクションからオブジェクトを削除します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="delete-method-ado-recordset.md">(ADO レコード セット) を削除します。</a></p></td>
<td><p>カレント レコードまたはレコードのグループを削除します。</p></td>
</tr>
<tr class="even">
<td><p><a href="deleterecord-method-ado.md">DeleteRecord</a></p></td>
<td><p>ファイルまたはディレクトリとそのすべてのサブディレクトリを削除します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://msdn.microsoft.com/library/jj248785(v=office.15)">(ADO コマンド) を実行します。</a></p></td>
<td><p><strong>CommandText</strong> プロパティで指定されたクエリ、SQL ステートメント、またはストアド プロシージャを実行します。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://msdn.microsoft.com/library/jj249832(v=office.15)">(ADO 接続の場合) を実行します。</a></p></td>
<td><p>指定されたクエリ、SQL ステートメント、ストアド プロシージャ、またはプロバイダー固有のテキストを実行します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="find-method-ado.md">Find</a></p></td>
<td><p><strong>Recordset</strong> から、指定した条件を満たす行を検索します。</p></td>
</tr>
<tr class="even">
<td><p><a href="flush-method-ado.md">フラッシュ</a></p></td>
<td><p>ADO バッファーに残っている <strong>Stream</strong> の内容を、 <strong>Stream</strong> に関連付けられた、基になるオブジェクトに反映します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="getchildren-method-ado.md">GetChildren</a></p></td>
<td><p>この<strong>レコード</strong>によって表されるディレクトリ内のサブディレクトリとファイルを表す行を持つ<strong>レコード セット</strong>を返します。</p></td>
</tr>
<tr class="even">
<td><p><a href="getchunk-method-ado.md">GetChunk</a></p></td>
<td><p>、サイズの大きなテキストまたはバイナリ データの<strong>Field</strong>オブジェクトの内容の一部または返します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="getrows-method-ado.md">GetRows</a></p></td>
<td><p><strong>Recordset</strong> オブジェクトの複数のレコードを配列に取り込みます。</p></td>
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
<td><p><strong>Recordset</strong> オブジェクトでカレント レコードの位置を移動します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst、MoveLast、MoveNext、および MovePrevious</a></p></td>
<td><p>指定された <strong>Recordset</strong> オブジェクトの最初、最後、次、または前のレコードに移動して、そのレコードをカレント レコードにします。</p></td>
</tr>
<tr class="even">
<td><p><a href="moverecord-method-ado.md">関係</a></p></td>
<td><p>ファイルまたはディレクトリとその内容を、別の場所に移動します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="nextrecordset-method-ado.md">NextRecordset</a></p></td>
<td><p>現在の <strong>Recordset</strong> オブジェクトをクリアし、一連のコマンド操作を実行して次の <strong>Recordset</strong> を返します。</p></td>
</tr>
<tr class="even">
<td><p><a href="open-method-ado-connection.md">(ADO 接続の場合) を開く</a></p></td>
<td><p>データ ソースへの接続を開きます。</p></td>
</tr>
<tr class="odd">
<td><p><a href="open-method-ado-record.md">(ADO のレコード) を開く</a></p></td>
<td><p>既存の <strong>Record</strong> オブジェクトを開きます。または、新しいファイルかディレクトリを作成します。</p></td>
</tr>
<tr class="even">
<td><p><a href="open-method-ado-recordset.md">(ADO レコード セット) を開く</a></p></td>
<td><p>カーソルを開きます。</p></td>
</tr>
<tr class="odd">
<td><p><a href="open-method-ado-stream.md">(ADO ストリーム) を開く</a></p></td>
<td><p>バイナリ データまたはテキスト データのストリームを操作するために <strong>Stream</strong> オブジェクトを開きます。</p></td>
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
<td><p><a href="resync-method-ado.md">再同期</a></p></td>
<td><p>現在の <strong>Recordset</strong> オブジェクト、または <strong>Record</strong> オブジェクトの <strong>Fields</strong> コレクションのデータを、基になるデータベースのデータで更新します。</p></td>
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
<td><p><a href="supports-method-ado.md">サポートしています</a></p></td>
<td><p>指定された <strong>Recordset</strong> オブジェクトが特定の種類の機能をサポートしているかどうかを調べます。</p></td>
</tr>
<tr class="odd">
<td><p><a href="update-method-ado.md">Update</a></p></td>
<td><p><strong>Recordset</strong> オブジェクトのカレント行、または <strong>Record</strong> オブジェクトの <strong>Fields</strong> コレクションに加えた変更を保存します。</p></td>
</tr>
<tr class="even">
<td><p><a href="updatebatch-method-ado.md">UpdateBatch</a></p></td>
<td><p>保留中の一括更新をすべてディスクに書き込みます。</p></td>
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

