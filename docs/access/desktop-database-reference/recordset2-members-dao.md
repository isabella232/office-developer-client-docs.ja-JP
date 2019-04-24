---
title: Recordset2 メンバー (DAO)
TOCTitle: Recordset2 Members
ms:assetid: 6ef57191-9da4-7904-d55c-60b59b895a50
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195572(v=office.15)
ms:contentKeyID: 48545523
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 29d1472e8cd02d8968ba84dbc1c1cf99be7ee858
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307274"
---
# <a name="recordset2-members-dao"></a>Recordset2 メンバー (DAO)


**適用先:** Access 2013、Office 2013

Recordset2 オブジェクトは、ベース テーブルのレコード、またはクエリの実行結果のレコードを表します。

## <a name="methods"></a>メソッド

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>名前</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="recordset2-addnew-method-dao.md">AddNew</a></strong></p></td>
<td><p>更新可能な <strong>Recordset2</strong> オブジェクトの新しいレコードを作成します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-cancel-method-dao.md">Cancel</a></strong></p></td>
<td><p><strong>注</strong>: ODBCDirect ワークスペースは、Microsoft access 2013 ではサポートされていません。 Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</p>
<p>保留中の非同期メソッド呼び出しの実行をキャンセルします (ODBCDirect ワークスペースのみ)。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-cancelupdate-method-dao.md">CancelUpdate</a></strong></p></td>
<td><p><strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトの保留中の更新をキャンセルします。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-clone-method-dao.md">Clone</a></strong></p></td>
<td><p>元の<strong>Recordset2</strong>オブジェクトを参照する、重複した<strong><a href="recordset-object-dao.md">Recordset</a></strong>オブジェクトを作成します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-close-method-dao.md">閉じる</a></strong></p></td>
<td><p>開いている <strong>Recordset</strong> を閉じます。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-copyquerydef-method-dao.md">CopyQueryDef</a></strong></p></td>
<td><p>recordset の<strong><a href="querydef-object-dao.md"></a></strong>プレースホルダーで表される<strong><a href="recordset-object-dao.md">recordset</a></strong>オブジェクトの作成<strong></strong>に使用される querydef オブジェクトを返します (Microsoft Access ワークスペースのみ)。 .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-delete-method-dao.md">Delete</a></strong></p></td>
<td><p>このオブジェクトではサポートされていません。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-edit-method-dao.md">Edit</a></strong></p></td>
<td><p>更新可能な <strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトからカレント レコードをコピー バッファーにコピーし、編集できるようにします。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-fillcache-method-dao.md">FillCache</a></strong></p></td>
<td><p>Microsoft Access データベース エンジンに接続されている ODBC データ ソースからのデータを格納する、 <strong>Recordset</strong> オブジェクト用のローカル キャッシュの全体または一部を埋めます (Microsoft Access データベース エンジンに接続された ODBC データベースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-findfirst-method-dao.md">FindFirst</a></strong></p></td>
<td><p>ダイナセット タイプまたはスナップショット タイプの <strong>Recordset</strong> オブジェクトで、指定された条件を満たす最初のレコードを検索し、そのレコードをカレント レコードにします (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-findlast-method-dao.md">FindLast</a></strong></p></td>
<td><p>ダイナセット タイプまたはスナップショット タイプの <strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトで、指定された条件を満たす最後のレコードを検索し、そのレコードをカレント レコードにします (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-findnext-method-dao.md">FindNext</a></strong></p></td>
<td><p>ダイナセット タイプまたはスナップショット タイプの <strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトで、指定された条件を満たす次のレコードを検索し、そのレコードをカレント レコードにします (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-findprevious-method-dao.md">FindPrevious</a></strong></p></td>
<td><p>ダイナセット タイプまたはスナップショット タイプの <strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトで、指定された条件を満たす前のレコードを検索し、そのレコードをカレント レコードにします (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-getrows-method-dao.md">GetRows</a></strong></p></td>
<td><p><strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトから複数の行を取得します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-move-method-dao.md">Move</a></strong></p></td>
<td><p><strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトのカレント レコードの位置を移動します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-movefirst-method-dao.md">MoveFirst</a></strong></p></td>
<td><p>指定された <strong>Recordset</strong> オブジェクトの最初のレコードに移動し、そのレコードをカレント レコードにします。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-movelast-method-dao.md">MoveLast</a></strong></p></td>
<td><p>指定された <strong>Recordset</strong> オブジェクトの最後のレコードに移動し、そのレコードをカレント レコードにします。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-movenext-method-dao.md">MoveNext</a></strong></p></td>
<td><p>指定された <strong>Recordset</strong> オブジェクトの次のレコードに移動し、そのレコードをカレント レコードにします。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-moveprevious-method-dao.md">MovePrevious</a></strong></p></td>
<td><p>指定された <strong>Recordset</strong> オブジェクトの前のレコードに移動し、そのレコードをカレント レコードにします。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-nextrecordset-method-dao.md">NextRecordset</a></strong></p></td>
<td><p><strong>注</strong>: ODBCDirect ワークスペースは、Microsoft access 2013 ではサポートされていません。 Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</p>
<p><strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong> 呼び出しで複数部分から成る選択クエリによって返される次のレコードのセットがある場合にこれを取得し、保留中のレコードが他にあるかどうかを示すブール型 ( <strong>Boolean</strong>) の値を返します (ODBCDirect ワークスペースのみ)。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-openrecordset-method-dao.md">OpenRecordset</a></strong></p></td>
<td><p>新しい <strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトを作成して <strong>Recordsets</strong> コレクションに追加します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-requery-method-dao.md">Requery</a></strong></p></td>
<td><p><strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトの基になるクエリを再実行することにより、オブジェクト内のデータを更新します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-seek-method-dao.md">Seek</a></strong></p></td>
<td><p>インデックス付きのテーブル タイプの <strong>Recordset</strong> オブジェクトで、現在のインデックスの指定された条件を満たすレコードを検索し、そのレコードをカレント レコードにします (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-update-method-dao.md">Update</a></strong></p></td>
<td><p><strong>注</strong>: ODBCDirect ワークスペースは、Microsoft access 2013 ではサポートされていません。 Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</p>
<p>コピー バッファーの内容を更新可能な <strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトに保存します。</p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a>プロパティ

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>名前</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="recordset2-absoluteposition-property-dao.md">AbsolutePosition</a></strong></p></td>
<td><p><strong>Recordset2</strong> オブジェクトのカレント レコードの相対的なレコード番号を設定または取得します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong></p></td>
<td><p><strong>注</strong>: ODBCDirect ワークスペースは、Microsoft access 2013 ではサポートされていません。 Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</p>
<p>最後の一括更新で更新が完了しなかったレコードの数を取得します (ODBCDirect ワークスペースのみ)。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-batchcollisions-property-dao.md">BatchCollisions</a></strong></p></td>
<td><p><strong>注</strong>: ODBCDirect ワークスペースは、Microsoft access 2013 ではサポートされていません。 Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</p>
<p>最後の一括更新操作で競合が発生した行を示すブックマークの配列を取得します (ODBCDirect ワークスペースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-batchsize-property-dao.md">BatchSize</a></strong></p></td>
<td><p><strong>注</strong>: ODBCDirect ワークスペースは、Microsoft access 2013 ではサポートされていません。 Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</p>
<p>それぞれのバッチでサーバーに返送されるステートメント数を設定または取得します (ODBCDirect ワークスペースのみ)。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-bof-property-dao.md">BOF</a></strong></p></td>
<td><p>カレントレコードの位置が<strong>Recordset</strong>オブジェクトの最初のレコードより前にあるかどうかを示す値を返します。 読み取り専用の <strong>Boolean</strong> です。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-bookmark-property-dao.md">Bookmark</a></strong></p></td>
<td><p><strong>Recordset</strong> オブジェクト内のカレント レコードを一意に識別するブックマークを設定または取得します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-bookmarkable-property-dao.md">Bookmarkable</a></strong></p></td>
<td><p><strong>Recordset</strong> オブジェクトがブックマークをサポートし、 <strong><a href="recordset2-bookmark-property-dao.md">Bookmark</a></strong> プロパティを使用してブックマークを設定できるかどうかを示す値を取得します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-cachesize-property-dao.md">CacheSize</a></strong></p></td>
<td><p>ローカルにキャッシュされる ODBC データソースから取得したレコード数を設定または取得します。 値の取得と設定が可能な長整数型 (<strong>Long</strong>) の値です。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-cachestart-property-dao.md">CacheStart</a></strong></p></td>
<td><p>ODBC データ ソースからローカルでキャッシュされるデータを含むダイナセット タイプの Recordset オブジェクトの最初のレコードのブックマークを指定する値を設定または取得します (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-connection-property-dao.md">Connection</a></strong></p></td>
<td><p>データベースに対応する <strong><a href="connection-object-dao.md">Connection</a></strong> オブジェクトを返します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-datecreated-property-dao.md">DateCreated</a></strong></p></td>
<td><p>ベーステーブルが作成された日付と時刻を返します (Microsoft access ワークスペースのみ)。 読み取り専用 <strong>バリアント</strong> です。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-editmode-property-dao.md">EditMode</a></strong></p></td>
<td><p>カレント レコードの編集状態を示す値を返します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-eof-property-dao.md">EOF</a></strong></p></td>
<td><p>カレントレコードの位置が<strong>Recordset</strong>オブジェクトの最後のレコードより後にあるかどうかを示す値を返します。 読み取り専用の <strong>Boolean</strong> です。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-fields-property-dao.md">Fields</a></strong></p></td>
<td><p>指定されたオブジェクト用に保存されているすべての <strong>Field</strong> オブジェクトを表す <strong>Fields</strong> コレクションを取得します。値の取得のみ可能です。  </p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-filter-property-dao.md">Filter</a></strong></p></td>
<td><p>後で開いた<strong>Recordset</strong>オブジェクトに含まれるレコードを決定する値を設定または取得します (Microsoft access ワークスペースのみ)。 値の取得と設定が可能な文字列型 (<strong>String</strong>) の値です。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-index-property-dao.md">Index</a></strong></p></td>
<td><p>テーブル タイプの <strong><a href="index-object-dao.md">Recordset</a></strong> オブジェクト内にある現在の <strong><a href="recordset-object-dao.md">Index</a></strong> オブジェクトの名前を示す値を設定または取得します (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-lastmodified-property-dao.md">LastModified</a></strong></p></td>
<td><p>最後に追加または変更したレコードを示すブックマークを取得します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-lastupdated-property-dao.md">LastUpdated</a></strong></p></td>
<td><p>ベーステーブルに対して最後に行われた変更の日付と時刻を返します。 読み取り専用 <strong>バリアント</strong> です。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-lockedits-property-dao.md">LockEdits</a></strong></p></td>
<td><p>編集時に有効になるロック状態の種類を示す値を設定または取得します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-name-property-dao.md">Name</a></strong></p></td>
<td><p>指定したオブジェクトの名前を返します。 読み取り専用 <strong>文字列</strong> です。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-nomatch-property-dao.md">NoMatch</a></strong></p></td>
<td><p><strong><a href="recordset2-seek-method-dao.md">Seek</a></strong> メソッドを使用するかまたは <strong><a href="recordset2-findfirst-method-dao.md">Find</a></strong> メソッドの 1 つを使用して特定のレコードが見つかったかどうかを示します (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-parentrecordset-property-dao.md">ParentRecordset</a></strong></p></td>
<td><p>指定したレコードセットの親 <strong>Recordset</strong> を返します。 値の取得のみ可能です。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-percentposition-property-dao.md">PercentPosition</a></strong></p></td>
<td><p><strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクト内のレコード数の割合に基づいて、 <strong>Recordset</strong> オブジェクトのカレント レコードのおよその位置を示す値を設定または取得します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-properties-property-dao.md">Properties</a></strong></p></td>
<td><p>指定したオブジェクトの <strong><a href="properties-collection-dao.md">Properties</a></strong> コレクションを取得します。値の取得のみ可能です。  </p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-recordcount-property-dao.md">RecordCount</a></strong></p></td>
<td><p><strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクト内のアクセス済みのレコード数、またはテーブル タイプの <strong>Recordset</strong> オブジェクト、あるいは <strong><a href="tabledef-object-dao.md">TableDef</a></strong> オブジェクトの合計レコード数を取得します。値の取得のみ可能です。長整数型 ( <strong>Long</strong>) の値を使用します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-recordstatus-property-dao.md">RecordStatus</a></strong></p></td>
<td><p><strong>注</strong>: ODBCDirect ワークスペースは、Microsoft access 2013 ではサポートされていません。 Microsoft Office Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</p>
<p>カレント レコードがバッチ更新の対象である場合に、そのレコードの更新状態を示す値を取得します (ODBCDirect ワークスペースのみ)。値の取得のみ可能です。 <strong><a href="recordstatusenum-enumeration-dao.md">RecordStatusEnum</a></strong> 値を使用します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-restartable-property-dao.md">Restartable</a></strong></p></td>
<td><p><strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトの基になるクエリを再実行する <strong><a href="recordset2-requery-method-dao.md">Requery</a></strong> メソッドを、 <strong>Recordset</strong> オブジェクトがサポートするかどうかを示す値を取得します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-sort-property-dao.md">Sort</a></strong></p></td>
<td><p><strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクト内のレコードの並べ替え順序を設定または取得します (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-stillexecuting-property-dao.md">StillExecuting</a></strong></p></td>
<td><p><strong>注</strong>: ODBCDirect ワークスペースは、Microsoft access 2013 ではサポートされていません。 Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</p>
<p>非同期操作 (つまり、 <strong>dbRunAsync</strong> オプションを指定して呼び出したメソッド) の実行が完了したかどうかを示します (ODBCDirect ワークスペースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-transactions-property-dao.md">トランザクション</a></strong></p></td>
<td><p>オブジェクトがトランザクションをサポートしているかどうかを示す値を返します。 読み取り専用の <strong>Boolean</strong> です。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-type-property-dao.md">種類</a></strong></p></td>
<td><p>オブジェクトの操作の種類またはデータ型を示す値を設定または取得します。 整数型 ( <strong>Integer</strong>) の値を使用します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-updatable-property-dao.md">Updatable</a></strong></p></td>
<td><p>DAO オブジェクトを変更できるかどうかを示す値を取得します。値の取得のみ可能です。ブール型 ( <strong>Boolean</strong> ) の値を使用します。  </p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-updateoptions-property-dao.md">UpdateOptions</a></strong></p></td>
<td><p><strong>注</strong>: ODBCDirect ワークスペースは、Microsoft access 2013 ではサポートされていません。 Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</p>
<p>バッチ更新中に各レコードに対して WHERE 句を作成する方法、およびバッチ更新での UPDATE ステートメントの使用、または DELETE の後に INSERT の実行が必要かどうかを示す値を設定します (ODBCDirect ワークスペースのみ)。値の取得および設定が可能です。 <strong><a href="updatecriteriaenum-enumeration-dao.md">UpdateCriteriaEnum</a></strong> クラスの定数を使用します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-validationrule-property-dao.md">ValidationRule</a></strong></p></td>
<td><p>データの変更時またはテーブルへの追加時に、フィールド内のデータを検証する値を設定または取得します (Microsoft Access ワークスペースのみ) 。値の取得および設定が可能です。文字列型 ( <strong>String</strong> ) の値を使用します。    </p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-validationtext-property-dao.md">ValidationText</a></strong></p></td>
<td><p><strong>Field</strong> オブジェクトの値が <strong>ValidationRule</strong> プロパティの設定で指定された入力規則を満たさない場合に、アプリケーションで表示されるメッセージのテキストを示す値を設定または取得します (Microsoft Access ワークスペースのみ)。値の取得のみ可能です。文字列型 (<strong>String</strong>) の値を使用します。</p></td>
</tr>
</tbody>
</table>

