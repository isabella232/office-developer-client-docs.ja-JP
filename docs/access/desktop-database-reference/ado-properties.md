---
title: ActiveX データ オブジェクト (ADO) のプロパティ
TOCTitle: ADO Properties
ms:assetid: 04f08f22-6327-c603-229e-d06a9f1c0d83
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248809(v=office.15)
ms:contentKeyID: 48543020
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 387ab87bb21d9c49c58a72bb4958426367493c11
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476821"
---
# <a name="ado-properties"></a>ADO プロパティ


**適用されます**Access 2013 |。Office 2013

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
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
<td><p>指定された <strong>Command</strong> オブジェクト、 <strong>Recordset</strong> オブジェクト、または <strong>Record</strong> オブジェクトが現在属している <strong>Connection</strong> オブジェクトを示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="actualsize-property-ado.md">ActualSize</a></p></td>
<td><p>フィールドの値の実際の長さを示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="attributes-property-ado.md">Attributes</a></p></td>
<td><p>オブジェクトの 1 つまたは複数の属性を示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="bof-eof-properties-ado.md">Bof プロパティと EOF</a></p></td>
<td><p><strong>Bof プロパティ</strong>-現在のレコードの位置が<strong>Recordset</strong>オブジェクトの最初のレコードより前にあることを示します。 <strong>EOF</strong> : カレント レコードの位置が<strong>Recordset</strong>オブジェクトの最後のレコードの後にあることを示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="bookmark-property-ado.md">Bookmark</a></p></td>
<td><p><strong>Recordset</strong> オブジェクトでカレント レコードを一意に識別するブックマークを示します。または、 <strong>Recordset</strong> オブジェクトのカレント レコードを、有効なブックマークで識別されるレコードに設定します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="cachesize-property-ado.md">CacheSize</a></p></td>
<td><p>ローカル メモリにキャッシュされる <strong>Recordset</strong> オブジェクトのレコード数を示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="chapter-property-ado.md">章</a></p></td>
<td><p>OLE DB Chapter オブジェクトを ADORecordsetConstruction オブジェクトから取得するか、または、OLE DB Chapter オブジェクトを ADORecordsetConstruction オブジェクトに設定します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="charset-property-ado.md">文字セット</a></p></td>
<td><p>テキスト <strong>Stream</strong> の内容を変換する文字セットを示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="commandtext-property-ado.md">CommandText</a></p></td>
<td><p>プロバイダーに対して発行するコマンド文字列を示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="commandtimeout-property-ado.md">CommandTimeout</a></p></td>
<td><p>実行しようとしたコマンドを中止して、エラーを生成するまでの待機時間を示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="commandtype-property-ado.md">CommandType</a></p></td>
<td><p><strong>Command</strong> オブジェクトの型を示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="connectionstring-property-ado.md">ConnectionString プロパティ (ADO)</a></p></td>
<td><p>データ ソースとの接続を確立するために使用される情報を示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="connectiontimeout-property-ado.md">ConnectionTimeout</a></p></td>
<td><p>接続操作を中止して、エラーを生成するまでの待機時間を示します。</p></td>
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
<td><p><a href="cursortype-property-ado.md">カーソル。</a></p></td>
<td><p><strong>Recordset</strong> オブジェクトで使用されているカーソルの種類を示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="datamember-property-ado.md">データ メンバー</a></p></td>
<td><p><strong>DataSource</strong> プロパティによって参照されるオブジェクトから取得するデータ メンバーの名前を示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="datasource-property-ado.md">DataSource</a></p></td>
<td><p><strong>Recordset</strong> オブジェクトとして表されるデータを持つオブジェクトを示します。</p></td>
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
<td><p><strong>Error</strong> オブジェクトを記述します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="direction-property-ado.md">Direction</a></p></td>
<td><p><strong>Parameter</strong> が、入力パラメーターと出力パラメーターのいずれか、またはその両方を表すのか、あるいはストアド プロシージャからの戻り値であるかどうかを示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="editmode-property-ado.md">EditMode</a></p></td>
<td><p>現在のレコードの編集ステータスを示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="eos-property-ado.md">EOS</a></p></td>
<td><p>現在の位置がストリームの末尾にあるかどうかを示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="filter-property-ado.md">Filter</a></p></td>
<td><p><strong>Recordset</strong> のデータに対するフィルターを示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="helpcontext-helpfile-properties-ado.md">HelpContext、HelpFile</a></p></td>
<td><p><strong>Error</strong> オブジェクトに関連するヘルプ ファイルおよびヘルプ トピックを示します。 <strong>HelpContextID</strong>: ヘルプ ファイルのトピックのコンテキスト ID を長整数型 ( <strong>Long</strong> ) の値で返します。 <strong>HelpFile</strong>: ヘルプ ファイルへの完全なパスに評価される文字列型 ( <strong>String</strong> ) の値を返します。</p></td>
</tr>
<tr class="even">
<td><p><a href="index-property-ado.md">Index</a></p></td>
<td><p><strong>Recordset</strong> オブジェクトに対して現在有効なインデックスの名前を示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="isolationlevel-property-ado.md">IsolationLevel</a></p></td>
<td><p><strong>Connection</strong> オブジェクトの分離レベルを示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="item-property-ado.md">Item</a></p></td>
<td><p>コレクションの特定のメンバーをその名前または序数で示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="lineseparator-property-ado.md">LineSeparator</a></p></td>
<td><p>テキスト <strong>Stream</strong> オブジェクトの行区切り文字として使用するバイナリ文字を示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="locktype-property-ado.md">ロック。</a></p></td>
<td><p>編集時にレコードに適用されるロックの種類を示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="marshaloptions-property-ado.md">スレッド</a></p></td>
<td><p>どのレコードがサーバーにマーシャリングされるかを示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="maxrecords-property-ado.md">MaxRecords</a></p></td>
<td><p>クエリから <strong>Recordset</strong> に返す最大レコード数を示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="mode-property-ado.md">Mode</a></p></td>
<td><p><strong>Connection</strong> オブジェクト、 <strong>Record</strong> オブジェクト、または <strong>Stream</strong> オブジェクトで使用可能なデータ変更権限を示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="name-property-ado.md">名前</a></p></td>
<td><p>オブジェクトの名前を示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="nativeerror-property-ado.md">以下</a></p></td>
<td><p>指定された <strong>Error</strong> オブジェクトでプロバイダー固有のエラー コードを示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="number-property-ado.md">番号</a></p></td>
<td><p><strong>Error</strong> オブジェクトを一意に識別する数値を示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="numericscale-property-ado.md">NumericScale</a></p></td>
<td><p><strong>Parameter</strong> オブジェクトまたは <strong>Field</strong> オブジェクトの数値の桁数を示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="originalvalue-property-ado.md">OriginalValue</a></p></td>
<td><p>変更が行われる前のレコードに存在していた <strong>Field</strong> の値を示します。</p></td>
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
<td><p>OLE DB <strong>Row</strong> オブジェクトのコンテナーを <strong>ADORecordConstruction</strong> オブジェクトに設定し、行の親が ADO <strong>Record</strong> オブジェクトに変換されるようにします。</p></td>
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
<td><p>Precision<a href="precision-property-ado.md"></a></p></td>
<td><p><strong>Parameter</strong> オブジェクト内の数値または数値型の <strong>Field</strong> オブジェクトの精度を示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="prepared-property-ado.md">準備</a></p></td>
<td><p>コンパイルされたバージョンのコマンドを実行前に保存するかどうかを示します。</p></td>
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
<td><p><a href="row-property-ado.md">Row</a></p></td>
<td><p><strong>ADORecordConstruction</strong> オブジェクトの OLE DB <strong>Row</strong> オブジェクトを設定または取得します。</p></td>
</tr>
<tr class="even">
<td><p><a href="rowposition-property-ado.md">RowPosition</a></p></td>
<td><p><strong>ADORecordsetConstruction</strong> オブジェクトの OLE DB <strong>RowPosition</strong> オブジェクトを取得または設定します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="rowset-property-ado.md">行セット</a></p></td>
<td><p><strong>ADORecordsetConstruction</strong> オブジェクトの OLE DB <strong>Rowset</strong> オブジェクトを取得または設定します。</p></td>
</tr>
<tr class="even">
<td><p><a href="size-property-ado.md">Size</a></p></td>
<td><p><strong>Parameter</strong> オブジェクトの最大サイズをバイト数または文字数で示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://msdn.microsoft.com/library/jj250128(v=office.15)">サイズ (ADO ストリーム)</a></p></td>
<td><p>ストリームの合計サイズをバイト数で示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="sort-property-ado.md">Sort</a></p></td>
<td><p><strong>Recordset</strong> の並べ替えに使用するフィールド名、および各フィールドの並べ替え順序が昇順か降順かを示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="source-property-ado-error.md">ソース (ADO エラー)</a></p></td>
<td><p>エラーの発生源のオブジェクトまたはアプリケーションの名前を示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="source-property-ado-record.md">ソース (ADO Record)</a></p></td>
<td><p><strong>Record</strong> オブジェクトによって表されるエンティティを示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="source-property-ado-recordset.md">ソース (ADO レコード セット)</a></p></td>
<td><p><strong>Recordset</strong> オブジェクトのデータのソースを示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="sqlstate-property-ado.md">SQLState</a></p></td>
<td><p>特定の <strong>Error</strong> オブジェクトの SQL 状態を示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="state-property-ado.md">State</a></p></td>
<td><p>対象になるすべてのオブジェクトについて、オブジェクトの状態が開いているか、閉じているかを示します。 非同期メソッドを実行しているすべての対象オブジェクトについて、そのオブジェクトが現在、接続、実行、または取得のどの状態であるかを示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="status-property-ado-field.md">状態 (ADO フィールド)</a></p></td>
<td><p><strong>Field</strong> オブジェクトのステータスを示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="status-property-ado-recordset.md">状態 (ADO レコード セット)</a></p></td>
<td><p>一括更新またはその他の一括操作に関して現在のレコードのステータスを示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="stayinsync-property-ado.md">StayInSync</a></p></td>
<td><p>親の行の位置が変更されたときに、基になる子のレコード (つまり、この<em>章</em>) への参照が変更されたかどうかを階層<strong>レコード セット</strong>オブジェクト内に示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="type-property-ado.md">型</a></p></td>
<td><p><strong>Parameter</strong> オブジェクト、 <strong>Field</strong> オブジェクト、または <strong>Property</strong> オブジェクトの操作の種類またはデータ型を示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="type-property-ado-stream.md">型 (ADO ストリーム)</a></p></td>
<td><p><strong>Stream</strong> (バイナリまたはテキスト) に格納されているデータの種類を示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="underlyingvalue-property-ado.md">UnderlyingValue</a></p></td>
<td><p>データベース内の <strong>Field</strong> オブジェクトの現在の値を示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="value-property-ado.md">値</a></p></td>
<td><p><strong>Field</strong> オブジェクト、 <strong>Parameter</strong> オブジェクト、または <strong>Property</strong> オブジェクトに割り当てられた値を示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="version-property-ado.md">Version</a></p></td>
<td><p>ADO のバージョン番号を示します。</p></td>
</tr>
</tbody>
</table>

