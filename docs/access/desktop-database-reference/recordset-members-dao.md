---
title: レコード セットのメンバー (DAO)
TOCTitle: Recordset Members
ms:assetid: cfaae9ec-1b88-4285-1ebe-637564e99dc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834683(v=office.15)
ms:contentKeyID: 48547815
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 73c83f4bba44ed7e30a45a02b1b273beb85a2851
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928293"
---
# <a name="recordset-members-dao"></a>レコード セットのメンバー (DAO)


**適用されます**Access 2013、Office 2013。

Recordset オブジェクトは、ベース テーブルのレコード、またはクエリの実行結果のレコードを表します。

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
<td><p><strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong></p></td>
<td><p>更新可能な <strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトの新しいレコードを作成します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-cancel-method-dao.md">Cancel</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>[!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</P>


<p>保留中の非同期メソッド呼び出しの実行をキャンセルします (ODBCDirect ワークスペースのみ)。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-cancelupdate-method-dao.md">CancelUpdate</a></strong></p></td>
<td><p><strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトで保留中のすべての更新を取り消します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-clone-method-dao.md">Clone</a></strong></p></td>
<td><p>元の <a href="recordset-object-dao.md">Recordset</a> オブジェクトを参照する、複数の <strong><strong>Recordset</strong></strong> オブジェクトを作成します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-close-method-dao.md">閉じる</a></strong></p></td>
<td><p>開いている <strong>Recordset</strong> を閉じます。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-copyquerydef-method-dao.md">CopyQueryDef</a></strong></p></td>
<td><p>レコード セットのプレース ホルダー (Microsoft Access ワークスペースのみ) で表される<strong><a href="recordset-object-dao.md">Recordset</a></strong>オブジェクトを作成するのには<strong>クエリ定義</strong>のコピーである<strong><a href="querydef-object-dao.md">QueryDef</a></strong>オブジェクトの使用を返します。 .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-delete-method-dao.md">Delete</a></strong></p></td>
<td><p>このオブジェクトではサポートされていません。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-edit-method-dao.md">Edit</a></strong></p></td>
<td><p>更新可能な <strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトからカレント レコードをコピー バッファーにコピーし、編集できるようにします。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-fillcache-method-dao.md">FillCache</a></strong></p></td>
<td><p>Microsoft Access データベース エンジンに接続している ODBC データ ソースのデータを格納している <strong>Recordset</strong> オブジェクトについて、ローカル キャッシュの全部または一部にデータを格納します (Microsoft Access データベース エンジンに接続している ODBC データベースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-findfirst-method-dao.md">FindFirst</a></strong></p></td>
<td><p>ダイナセット タイプまたはスナップショット タイプの <strong>Recordset</strong> オブジェクトで、指定された条件を満たす最初のレコードを検索し、そのレコードをカレント レコードにします (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-findlast-method-dao.md">FindLast</a></strong></p></td>
<td><p>ダイナセット タイプまたはスナップショット タイプの <strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトで、指定された条件を満たす最後のレコードを検索し、そのレコードをカレント レコードにします (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-findnext-method-dao.md">FindNext</a></strong></p></td>
<td><p>ダイナセット タイプまたはスナップショット タイプの <strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトで、指定された条件を満たす次のレコードを検索し、そのレコードをカレント レコードにします (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-findprevious-method-dao.md">FindPrevious</a></strong></p></td>
<td><p>ダイナセット タイプまたはスナップショット タイプの <strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトで、指定された条件を満たす前のレコードを検索し、そのレコードをカレント レコードにします (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-getrows-method-dao.md">GetRows</a></strong></p></td>
<td><p><strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトから複数の行を取得します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-move-method-dao.md">Move</a></strong></p></td>
<td><p><strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトでカレント レコードの位置を移動します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-movefirst-method-dao.md">MoveFirst</a></strong></p></td>
<td><p>指定した <strong>Recordset</strong> オブジェクトの最初のレコードに移動して、そのレコードをカレント レコードにします。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-movelast-method-dao.md">MoveLast</a></strong></p></td>
<td><p>指定された <strong>Recordset</strong> オブジェクトの最後のレコードに移動し、そのレコードをカレント レコードにします。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-movenext-method-dao.md">MoveNext</a></strong></p></td>
<td><p>指定された <strong>Recordset</strong> オブジェクトの次のレコードに移動し、そのレコードをカレント レコードにします。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-moveprevious-method-dao.md">MovePrevious</a></strong></p></td>
<td><p>指定された <strong>Recordset</strong> オブジェクトの前のレコードに移動し、そのレコードをカレント レコードにします。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-nextrecordset-method-dao.md">NextRecordset</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>[!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</P>


<p><strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong> 呼び出しで複数部分から成る選択クエリによって返される次のレコードのセットがある場合にこれを取得し、保留中のレコードが他にあるかどうかを示すブール型 ( <strong>Boolean</strong> ) の値を取得します (ODBCDirect ワークスペースのみ)。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-openrecordset-method-dao.md">何らか</a></strong></p></td>
<td><p>新しい <strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトを作成して <strong>Recordsets</strong> コレクションに追加します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-requery-method-dao.md">Requery</a></strong></p></td>
<td><p><strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトの基になるクエリを再実行することにより、オブジェクト内のデータを更新します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-seek-method-dao.md">シーク</a></strong></p></td>
<td><p>インデックス付きのテーブル タイプの <strong>Recordset</strong> オブジェクトで、現在のインデックスの指定された条件を満たすレコードを検索し、そのレコードをカレント レコードにします (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-update-method-dao.md">Update</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>[!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</P>


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
<td><p><strong><a href="recordset-absoluteposition-property-dao.md">AbsolutePosition</a></strong></p></td>
<td><p><strong>Recordset</strong> オブジェクトのカレント レコードの相対的なレコード番号を設定または取得します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>[!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</P>


<p>最後のバッチ更新が完了していないレコード数を返します (ODBCDirect ワークスペースのみ)。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-batchcollisions-property-dao.md">BatchCollisions</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>[!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</P>


<p>最後のバッチ更新操作で競合が生成された行を示すブックマークの配列を返します (ODBCDirect ワークスペースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-batchsize-property-dao.md">BatchSize</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>[!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</P>


<p>各バッチにおいてサーバーに送り返されるステートメントの数を設定または取得します (ODBCDirect ワークスペースのみ)。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-bof-property-dao.md">BOF</a></strong></p></td>
<td><p>カレント レコードの位置が <strong>Recordset</strong> オブジェクトの最初のレコードの前であることを示す値を返します。取得のみが可能です。ブール型 ( <strong>Boolean</strong>) の値を使用します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-bookmark-property-dao.md">ブックマーク</a></strong></p></td>
<td><p><strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトのカレント レコードを一意に識別するブックマークを設定または取得します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-bookmarkable-property-dao.md">Bookmarkable</a></strong></p></td>
<td><p><strong>Recordset</strong> オブジェクトがブックマークをサポートしているかどうかを示す、 <strong><a href="recordset-bookmark-property-dao.md">Bookmark</a></strong> プロパティを使用して設定できる値を返します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-cachesize-property-dao.md">CacheSize</a></strong></p></td>
<td><p>ローカル メモリにキャッシュされた ODBC データ ソースから取得したレコード数を設定または取得します。値の取得および設定が可能です。長整数型 ( <strong>Long</strong>) の値を使用します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-cachestart-property-dao.md">CacheStart</a></strong></p></td>
<td><p>ODBC データ ソースからローカルでキャッシュされるデータを含むダイナセット タイプの Recordset オブジェクトの最初のレコードのブックマークを指定する値を設定または取得します (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-connection-property-dao.md">Connection</a></strong></p></td>
<td><p>データベースに対応する <strong><a href="connection-object-dao.md">Connection</a></strong> オブジェクトを取得します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-datecreated-property-dao.md">DateCreated</a></strong></p></td>
<td><p>ベース テーブルを作成した日付と時刻を取得します (Microsoft Access ワークスペースのみ)。値の取得のみ可能です。バリアント型 ( <strong>Variant</strong>) の値を使用します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-editmode-property-dao.md">EditMode</a></strong></p></td>
<td><p>カレント レコードの編集状態を示す値を返します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-eof-property-dao.md">EOF</a></strong></p></td>
<td><p>カレント レコードの位置が、 <strong>Recordset</strong> オブジェクトの最後のレコードより後にあるかどうかを示す値を取得します。値の取得のみ可能です。ブール型 ( <strong>Boolean</strong> ) の値を使用します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-fields-property-dao.md">Fields</a></strong></p></td>
<td><p>指定されたオブジェクト用に保存されているすべての <strong>Field</strong> オブジェクトを表す <strong>Fields</strong> コレクションを取得します。値の取得のみ可能です。  </p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-filter-property-dao.md">フィルター</a></strong></p></td>
<td><p>次に開く <strong>Recordset</strong> オブジェクトに含めるレコードを決める値を設定または取得します (Microsoft Access ワークスペースのみ)。値の取得および設定が可能です。文字列型 ( <strong>String</strong> ) の値を使用します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-index-property-dao.md">Index</a></strong></p></td>
<td><p>テーブル タイプの <strong><a href="index-object-dao.md">Recordset</a></strong> オブジェクト内にある現在の <strong><a href="recordset-object-dao.md">Index</a></strong> オブジェクトの名前を示す値を設定または取得します (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-lastmodified-property-dao.md">LastModified</a></strong></p></td>
<td><p>最後に追加または変更したレコードを示すブックマークを取得します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-lastupdated-property-dao.md">LastUpdated</a></strong></p></td>
<td><p>ベース テーブルに対して行われた最新の変更の日付と時刻を取得します。値の取得のみ可能です。バリアント型 ( <strong>Variant</strong>) の値を使用します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-lockedits-property-dao.md">LockEdits</a></strong></p></td>
<td><p>編集時に有効になるロック状態の種類を示す値を設定または取得します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-name-property-dao.md">Name</a></strong></p></td>
<td><p>指定したオブジェクトの名前を取得します。値の取得のみ可能です。文字列型 ( <strong>String</strong>) の値を使用します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-nomatch-property-dao.md">NoMatch</a></strong></p></td>
<td><p><strong><a href="recordset-seek-method-dao.md">Seek</a></strong> メソッドを使用するかまたは <strong><a href="recordset-findfirst-method-dao.md">Find</a></strong> メソッドの 1 つを使用して、特定のレコードが見つかったかどうかを示します (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-percentposition-property-dao.md">PercentPosition</a></strong></p></td>
<td><p><strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクト内のレコード数の割合に基づいて、 <strong>Recordset</strong> オブジェクトのカレント レコードのおよその位置を示す値を設定または取得します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-properties-property-dao.md">Properties</a></strong></p></td>
<td><p>指定したオブジェクトの <strong><a href="properties-collection-dao.md">Properties</a></strong> コレクションを取得します。値の取得のみ可能です。  </p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-recordcount-property-dao.md">RecordCount</a></strong></p></td>
<td><p><strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクト内のアクセス済みのレコード数、またはテーブル タイプの <strong>Recordset</strong> オブジェクト、あるいは <strong><a href="tabledef-object-dao.md">TableDef</a></strong> オブジェクトの合計レコード数を取得します。値の取得のみ可能です。長整数型 ( <strong>Long</strong>) の値を使用します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-recordstatus-property-dao.md">RecordStatus</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>[!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</P>


<p>カレント レコードがバッチ更新の対象である場合に、そのレコードの更新状態を示す値を取得します (ODBCDirect ワークスペースのみ)。値の取得のみ可能です。 <strong><a href="recordstatusenum-enumeration-dao.md">RecordStatusEnum</a></strong> 値を使用します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-restartable-property-dao.md">Restartable</a></strong></p></td>
<td><p><strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトの基になるクエリを再実行する <strong><a href="recordset-requery-method-dao.md">Requery</a></strong> メソッドを、 <strong>Recordset</strong> オブジェクトがサポートするかどうかを示す値を取得します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-sort-property-dao.md">Sort</a></strong></p></td>
<td><p><strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクト内のレコードの並べ替え順序を設定または取得します (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-stillexecuting-property-dao.md">StillExecuting</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>[!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</P>


<p>非同期操作 (つまり、 <strong>dbRunAsync</strong> オプションを指定して呼び出したメソッド) の実行が完了したかどうかを示します (ODBCDirect ワークスペースのみ)。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-transactions-property-dao.md">トランザクション</a></strong></p></td>
<td><p>オブジェクトがトランザクションをサポートしているかどうかを示す値を取得します。値の取得のみ可能です。ブール型 ( <strong>Boolean</strong>) の値を使用します。</p></td>
</tr>
<tr class="even">
<td><p><strong>型</strong></p></td>
<td><p>このメンバーの説明は、Office 14 の最終リリースに表示されます。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-updatable-property-dao.md">Updatable</a></strong></p></td>
<td><p>DAO オブジェクトを変更できるかどうかを示す値を取得します。値の取得のみ可能です。ブール型 ( <strong>Boolean</strong> ) の値を使用します。  </p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-updateoptions-property-dao.md">UpdateOptions</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>[!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</P>


<p>バッチ更新中に各レコードに対して WHERE 句を作成する方法、およびバッチ更新での UPDATE ステートメントの使用、または DELETE の後に INSERT の実行が必要かどうかを示す値を設定します (ODBCDirect ワークスペースのみ)。値の取得および設定が可能です。 <strong><a href="updatecriteriaenum-enumeration-dao.md">UpdateCriteriaEnum</a></strong> クラスの定数を使用します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-validationrule-property-dao.md">ValidationRule</a></strong></p></td>
<td><p>データの変更時またはテーブルへの追加時に、フィールド内のデータを検証する値を設定または取得します (Microsoft Access ワークスペースのみ) 。値の取得および設定が可能です。文字列型 ( <strong>String</strong> ) の値を使用します。  </p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-validationtext-property-dao.md">ValidationText</a></strong></p></td>
<td><p><strong>Field</strong> オブジェクトの値が <strong>ValidationRule</strong> プロパティの設定で指定された入力規則を満たさない場合に、アプリケーションで表示されるメッセージのテキストを示す値を設定または取得します (Microsoft Access ワークスペースのみ)。値の取得のみが可能です。文字列型 ( <strong>String</strong>) の値を使用します。</p></td>
</tr>
</tbody>
</table>

