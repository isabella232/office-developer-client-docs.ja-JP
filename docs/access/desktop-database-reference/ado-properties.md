---
title: ActiveX Data Objects (ADO) プロパティ
TOCTitle: ADO properties
ms:assetid: 04f08f22-6327-c603-229e-d06a9f1c0d83
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248809(v=office.15)
ms:contentKeyID: 48543020
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a0efb40d1b5e4c5d675d8add7cdb7a05760578a9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283234"
---
# <a name="ado-properties"></a>ADO プロパティ

**適用先:** Access 2013、Office 2013

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th>プロパティ</th>
<th>説明</th>
</tr>
<tr class="odd">
<td><p><a href="absolutepage-property-ado.md">AbsolutePage</a></p></td>
<td><p>カレント レコードがあるページを示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="absoluteposition-property-ado.md">AbsolutePosition</a></p></td>
<td><p><strong>Recordset</strong> オブジェクト内のカレント レコードの位置を表す値を示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="activecommand-property-ado.md">ActiveCommand</a></p></td>
<td><p>関連付けられた <strong>Recordset</strong> オブジェクトを作成した <strong>Command</strong> オブジェクトを示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="activeconnection-property-ado.md">ActiveConnection</a></p></td>
<td><p>指定した <strong>Command</strong>、<strong>Recordset</strong>、または <strong>Record</strong> オブジェクトが、現在どの <strong>Connection</strong> オブジェクトに属するかを示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="actualsize-property-ado.md">ActualSize</a></p></td>
<td><p>フィールド値の実際の長さを示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="attributes-property-ado.md">属性</a></p></td>
<td><p>オブジェクトの 1 つまたは複数の特性を示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="bof-eof-properties-ado.md">BOF、EOF</a></p></td>
<td><p><strong>BOF</strong> カレント レコードの位置が <strong>Recordset</strong> オブジェクトの最初のレコードより前にあることを示します。 <strong>EOF</strong> カレント レコードの位置が <strong>Recordset</strong> オブジェクトの最後のレコードより後にあることを示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="bookmark-property-ado.md">Bookmark</a></p></td>
<td><p><strong>Recordset</strong> オブジェクトでカレント レコードを一意に識別するブックマークを示すか、または、<strong>Recordset</strong> オブジェクトのカレント レコードを有効なブックマークで識別されるレコードに設定します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="cachesize-property-ado.md">CacheSize</a></p></td>
<td><p>ローカル メモリにキャッシュされた <strong>Recordset</strong> オブジェクトのレコード数を示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="chapter-property-ado.md">節</a></p></td>
<td><p>Gets or sets an OLE DB <strong>Chapter</strong> object from/on an <strong>ADORecordsetConstruction</strong> object.</p></td>
</tr>
<tr class="odd">
<td><p><a href="charset-property-ado.md">CharSet</a></p></td>
<td><p>テキスト <strong>Stream</strong> の内容を変換する文字セットを示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="commandtext-property-ado.md">CommandText</a></p></td>
<td><p>プロバイダーに対して発行するコマンド文字列を示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="commandtimeout-property-ado.md">CommandTimeout</a></p></td>
<td><p>実行しようとしたコマンドを中止して、エラーを発生させるまでの待機時間を示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="commandtype-property-ado.md">CommandType</a></p></td>
<td><p><strong>Command</strong> オブジェクトの型を示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="connectionstring-property-ado.md">ConnectionString プロパティ</a></p></td>
<td><p>データ ソースとの接続に必要な情報を示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="connectiontimeout-property-ado.md">ConnectionTimeout</a></p></td>
<td><p>接続試行操作を中止して、エラーを発生させるまでの待機時間を示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="count-property-ado.md">Count</a></p></td>
<td><p>コレクション内のオブジェクト数を示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="cursorlocation-property-ado.md">CursorLocation</a></p></td>
<td><p>カーソル サービスの場所を示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="cursortype-property-ado.md">CursorType</a></p></td>
<td><p><strong>Recordset</strong> オブジェクトで使用されているカーソルの種類を示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="datamember-property-ado.md">DataMember</a></p></td>
<td><p><strong>DataSource</strong> プロパティによるオブジェクト参照から取得するデータ メンバー名を示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="datasource-property-ado.md">DataSource</a></p></td>
<td><p><strong>Recordset</strong> オブジェクトとして表されるデータを格納しているオブジェクトを示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="defaultdatabase-property-ado.md">DefaultDatabase</a></p></td>
<td><p><strong>Connection</strong> オブジェクトの既定のデータベースを示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="definedsize-property-ado.md">DefinedSize</a></p></td>
<td><p><strong>Field</strong> オブジェクトのデータ容量を示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="description-property-ado.md">説明</a></p></td>
<td><p><strong>Error</strong> オブジェクトを示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="direction-property-ado.md">Direction</a></p></td>
<td><p><strong>Parameter</strong> が、入力パラメーターと出力パラメーターのいずれか、またはその両方を表すのか、あるいはストアド プロシージャからの戻り値であるかどうかを示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="editmode-property-ado.md">EditMode</a></p></td>
<td><p>カレント レコードの編集ステータスを示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="eos-property-ado.md">EOS</a></p></td>
<td><p>現在の位置がストリームの最後かどうかを示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="filter-property-ado.md">Filter</a></p></td>
<td><p><strong>Recordset</strong> のデータに対するフィルターを示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="helpcontext-helpfile-properties-ado.md">HelpContext、HelpFile</a></p></td>
<td><p><strong>Error</strong> オブジェクトに関連付けられたヘルプ ファイルとトピックを示します。 <strong>HelpContextID</strong> ヘルプ ファイルのトピックのコンテキスト ID を長整数型 (<strong>Long</strong>) の値で返します。 <strong>HelpFile</strong> ヘルプ ファイルへの完全なパスを示す文字列型 (<strong>String</strong>) の値を返します。</p></td>
</tr>
<tr class="even">
<td><p><a href="index-property-ado.md">インデックス</a></p></td>
<td><p><strong>Recordset</strong> オブジェクトに対して現在有効なインデックス名を示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="isolationlevel-property-ado.md">IsolationLevel</a></p></td>
<td><p><strong>Connection</strong> オブジェクトの分離レベルを示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="item-property-ado.md">Item</a></p></td>
<td><p>コレクションの特定のメンバーをその名前またはインデックスで示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="lineseparator-property-ado.md">LineSeparator</a></p></td>
<td><p>テキスト <strong>Stream</strong> オブジェクトの行区切り文字として使用するバイナリ文字を示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="locktype-property-ado.md">LockType</a></p></td>
<td><p>編集時にレコードに適用されるロックの種類を示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="marshaloptions-property-ado.md">MarshalOptions</a></p></td>
<td><p>どのレコードがサーバーにマーシャリングされるかを示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="maxrecords-property-ado.md">MaxRecords</a></p></td>
<td><p>クエリから <strong>Recordset</strong> に返される最大レコード数を示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="mode-property-ado.md">Mode</a></p></td>
<td><p><strong>Connection</strong>、<strong>Record</strong>、または <strong>Stream</strong> オブジェクトでデータを変更するために使用できる権限を示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="name-property-ado.md">Name</a></p></td>
<td><p>オブジェクトの名前を示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="nativeerror-property-ado.md">NativeError</a></p></td>
<td><p>指定された <strong>Error</strong> オブジェクトでプロバイダー固有のエラー コードを示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="number-property-ado.md">数値</a></p></td>
<td><p><strong>Error</strong> オブジェクトを一意に識別する数値を示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="numericscale-property-ado.md">NumericScale</a></p></td>
<td><p><strong>Parameter</strong> オブジェクトまたは <strong>Field</strong> オブジェクトの数値型 (Numeric) の値を示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="originalvalue-property-ado.md">OriginalValue</a></p></td>
<td><p>変更前のレコード内に存在する <strong>Field</strong> 値を示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="pagecount-property-ado.md">PageCount</a></p></td>
<td><p><strong>Recordset</strong> オブジェクトに含まれるデータのページ数を示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="pagesize-property-ado.md">PageSize</a></p></td>
<td><p><strong>Recordset</strong> の 1 ページを構成するレコード数を示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="parentrow-property-ado.md">ParentRow</a></p></td>
<td><p>OLE DB <strong>Row</strong> オブジェクトのコンテナーを <strong>ADORecordConstruction</strong> オブジェクトに設定し、親行が ADO <strong>Record</strong> オブジェクトになるようにします。</p></td>
</tr>
<tr class="even">
<td><p><a href="parenturl-property-ado.md">ParentURL</a></p></td>
<td><p>現在の <strong>Record</strong> オブジェクトの親 <strong>Record</strong> を示す絶対 URL 文字列を示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="position-property-ado.md">Position</a></p></td>
<td><p><strong>Stream</strong> オブジェクト内の現在の位置を示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="precision-property-ado.md">精度</a></p></td>
<td><p><strong>Parameter</strong> オブジェクトの数値型 (Numeric) の値、または数値型の <strong>Field</strong> オブジェクトの精度を示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="prepared-property-ado.md">整え</a></p></td>
<td><p>コンパイルされたバージョンのコマンドを、実行前に保存するかどうかを示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="provider-property-ado.md">Provider</a></p></td>
<td><p><strong>Connection</strong> オブジェクトのプロバイダー名を示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="recordcount-property-ado.md">RecordCount</a></p></td>
<td><p><strong>Recordset</strong> オブジェクト内のレコード数を示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="recordtype-property-ado.md">RecordType</a></p></td>
<td><p><strong>Record</strong> オブジェクトの種類を示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="row-property-ado.md">行</a></p></td>
<td><p><strong>ADORecordConstruction</strong> オブジェクトの OLE DB <strong>Row</strong> オブジェクトを設定または取得します。</p></td>
</tr>
<tr class="even">
<td><p><a href="rowposition-property-ado.md">RowPosition</a></p></td>
<td><p><strong>ADORecordsetConstruction</strong> オブジェクトの OLE DB <strong>RowPosition</strong> オブジェクトを取得または設定します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="rowset-property-ado.md">行</a></p></td>
<td><p><strong>ADORecordsetConstruction</strong> オブジェクトの OLE DB <strong>Rowset</strong> オブジェクトを取得または設定します。</p></td>
</tr>
<tr class="even">
<td><p><a href="size-property-ado.md">Size</a></p></td>
<td><p><strong>Parameter</strong> オブジェクトの最大サイズをバイト数または文字数で示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream">Size (ADO Stream)</a></p></td>
<td><p>ストリームの合計サイズをバイト数で示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="sort-property-ado.md">Sort</a></p></td>
<td><p><strong>Recordset</strong> がソートされる 1 つまたは複数のフィールド名と、各フィールドが昇順または降順のいずれでソートされるかを示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="source-property-ado-error.md">Source (ADO Error)</a></p></td>
<td><p>エラーの発生源のオブジェクト名またはアプリケーション名を示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="source-property-ado-record.md">Source (ADO Record)</a></p></td>
<td><p><strong>Record</strong> オブジェクトによって表されるエンティティを示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="source-property-ado-recordset.md">Source (ADO Recordset)</a></p></td>
<td><p><strong>Recordset</strong> オブジェクトのデータのソースを示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="sqlstate-property-ado.md">SQLState</a></p></td>
<td><p>指定された <strong>Error</strong> オブジェクトの SQL 状態を示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="state-property-ado.md">State</a></p></td>
<td><p>該当するすべてのオブジェクトについて、オブジェクトの状態がオープンかクローズかを示します。 非同期メソッドを実行しているすべての対象オブジェクトについて、そのオブジェクトが現在、接続、実行、または取得のどの状態であるかを示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="status-property-ado-field.md">Status (ADO Field)</a></p></td>
<td><p><strong>Field</strong> オブジェクトのステータスを示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="status-property-ado-recordset.md">Status (ADO Recordset)</a></p></td>
<td><p>バッチ更新または別の大量の操作に関するカレント レコードのステータスを指定します。</p></td>
</tr>
<tr class="even">
<td><p><a href="stayinsync-property-ado.md">StayInSync</a></p></td>
<td><p>親の行の位置が変更されたときに、基になる子のレコード (つまり、<em>チャプター</em>) への参照を変更するかどうかを、階層<strong>Recordset</strong>オブジェクト内に示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="type-property-ado.md">Type</a></p></td>
<td><p><strong>Parameter</strong>、<strong>Field</strong>、または <strong>Property</strong> オブジェクトの操作の種類またはデータ型を示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="type-property-ado-stream.md">Type (ADO Stream)</a></p></td>
<td><p><strong>Stream</strong> に含まれるデータの種類を示します (バイナリまたはテキスト)。</p></td>
</tr>
<tr class="odd">
<td><p><a href="underlyingvalue-property-ado.md">UnderlyingValue</a></p></td>
<td><p>データベース内の <strong>Field</strong> オブジェクトの現在の値を示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="value-property-ado.md">値</a></p></td>
<td><p><strong>Field</strong>、<strong>Parameter</strong>、または <strong>Property</strong> オブジェクトに代入された値を示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="version-property-ado.md">バージョン</a></p></td>
<td><p>ADO のバージョン番号を示します。</p></td>
</tr>
</tbody>
</table>

<br/>
