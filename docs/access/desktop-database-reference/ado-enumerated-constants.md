---
title: ADO の列挙定数
TOCTitle: ADO enumerated constants
ms:assetid: 7c983acd-8b38-dc3c-6704-46e649ebb7d6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249522(v=office.15)
ms:contentKeyID: 48545841
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 05e5d3a77dc7db5ef5a0d81a3f13d5fc5987f5de
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283409"
---
# <a name="ado-enumerated-constants"></a>ADO の列挙定数

**適用先:** Access 2013、Office 2013

ここでは、デバッグ用に各定数の実際の値の一覧を示します。ただし、この値は参考用のものであり、ADO のリリースごとに変更されることがあります。コードを記述するときは、列挙定数の実際の値ではなく、名前のみを使って記述するようにしてください。

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th>列挙定数</th>
<th>説明</th>
</tr>
<tr class="odd">
<td><p><a href="adcprop-asyncthreadpriority-enum.md">ADCPROP_ASYNCTHREADPRIORITY_ENUM</a></p></td>
<td><p>RDS の <strong>Recordset</strong> オブジェクトに対して、データを取得する非同期スレッドの実行優先順位を指定します。</p></td>
</tr>
<tr class="even">
<td><p><a href="adcprop-autorecalc-enum.md">ADCPROP_AUTORECALC_ENUM</a></p></td>
<td><p>階層 <strong>Recordset</strong> の集計列と計算列を <strong>MSDataShape</strong> プロバイダーがいつ再計算するかを指定します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="adcprop-updatecriteria-enum.md">ADCPROP_UPDATECRITERIA_ENUM</a></p></td>
<td><p><strong>Recordset</strong> オブジェクトがあるデータ ソース行の共有的更新時に、競合の検出に使用するフィールドを指定します。</p></td>
</tr>
<tr class="even">
<td><p><a href="adcprop-updateresync-enum.md">ADCPROP_UPDATERESYNC_ENUM</a></p></td>
<td><p><strong>UpdateBatch</strong> メソッドに暗黙の <strong>Resync</strong> メソッド操作を実行するかどうか、実行する場合は、その操作の適用範囲を指定します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="affectenum.md">AffectEnum</a></p></td>
<td><p>操作の対象となるレコードを指定します。</p></td>
</tr>
<tr class="even">
<td><p><a href="bookmarkenum.md">BookmarkEnum</a></p></td>
<td><p>操作の開始位置を示すブックマークを指定します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="commandtypeenum.md">CommandTypeEnum</a></p></td>
<td><p>コマンド引数をどのように解釈するかを指定します。</p></td>
</tr>
<tr class="even">
<td><p><a href="compareenum.md">CompareEnum</a></p></td>
<td><p>ブックマークで表された 2 つのレコードの相対位置を指定します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="connectmodeenum.md">ConnectModeEnum</a></p></td>
<td><p><strong>Connection</strong> 内のデータ編集、<strong>Record</strong> のオープン、または <strong>Record</strong> オブジェクトと <strong>Stream</strong> オブジェクトの <strong>Mode</strong> プロパティの値の指定に対する権限を指定します。</p></td>
</tr>
<tr class="even">
<td><p><a href="connectoptionenum.md">ConnectOptionEnum</a></p></td>
<td><p><strong>Connection</strong> オブジェクトの <strong>Open</strong> メソッドからの戻りが、接続が確立された後 (同期) か前 (非同期) かを指定します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="connectpromptenum.md">ConnectPromptEnum</a></p></td>
<td><p>ODBC データ ソースとの接続を開くときに、不足しているパラメーターを要求するダイアログ ボックスを表示するかどうかを指定します。</p></td>
</tr>
<tr class="even">
<td><p><a href="copyrecordoptionsenum.md">CopyRecordOptionsEnum</a></p></td>
<td><p><strong>CopyRecord</strong> メソッドの動作を指定します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="cursorlocationenum.md">CursorLocationEnum</a></p></td>
<td><p>カーソル エンジンの場所を指定します。</p></td>
</tr>
<tr class="even">
<td><p><a href="cursoroptionenum.md">CursorOptionEnum</a></p></td>
<td><p><strong>Supports</strong> メソッドがテストする機能を指定します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="cursortypeenum.md">CursorTypeEnum</a></p></td>
<td><p><strong>Recordset</strong> オブジェクトが使用するカーソルの種類を指定します。</p></td>
</tr>
<tr class="even">
<td><p><a href="datatypeenum.md">DataTypeEnum</a></p></td>
<td><p><strong>Field</strong>、<strong>Parameter</strong>、または <strong>Property</strong> のデータ型を指定します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="editmodeenum.md">EditModeEnum</a></p></td>
<td><p>レコードの編集ステータスを指定します。</p></td>
</tr>
<tr class="even">
<td><p><a href="errorvalueenum.md">ErrorValueEnum</a></p></td>
<td><p>ADO 実行時エラーの種類を指定します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="eventreasonenum.md">EventReasonEnum</a></p></td>
<td><p>イベントが発生する理由を指定します。</p></td>
</tr>
<tr class="even">
<td><p><a href="eventstatusenum.md">EventStatusEnum</a></p></td>
<td><p>イベント実行のカレント ステータスを指定します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="executeoptionenum.md">ExecuteOptionEnum</a></p></td>
<td><p>プロバイダーによるコマンドの実行方法を指定します。</p></td>
</tr>
<tr class="even">
<td><p><a href="fieldenum.md">FieldEnum</a></p></td>
<td><p><strong>Record</strong> オブジェクトの <strong>Fields</strong> コレクションで参照される特定のフィールドを指定します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="fieldattributeenum.md">FieldAttributeEnum</a></p></td>
<td><p>1 つまたは複数の <strong>Field</strong> オブジェクトの属性を指定します。</p></td>
</tr>
<tr class="even">
<td><p><a href="fieldstatusenum.md">FieldStatusEnum</a></p></td>
<td><p><strong>Field</strong> オブジェクトのステータスを指定します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="filtergroupenum.md">FilterGroupEnum</a></p></td>
<td><p><strong>Recordset</strong> でフィルターの対象となるレコード グループを指定します。</p></td>
</tr>
<tr class="even">
<td><p><a href="getrowsoptionenum.md">GetRowsOptionEnum</a></p></td>
<td><p><strong>Recordset</strong> から取得するレコード数を指定します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="isolationlevelenum.md">IsolationLevelEnum</a></p></td>
<td><p><strong>Connection</strong> オブジェクトのトランザクション分離レベルを指定します。</p></td>
</tr>
<tr class="even">
<td><p><a href="lineseparatorsenum.md">LineSeparatorsEnum</a></p></td>
<td><p>テキスト <strong>Stream</strong> オブジェクトの行区切り記号に使用されている文字を指定します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="locktypeenum.md">LockTypeEnum</a></p></td>
<td><p>編集時にレコードに適用されるロックの種類を指定します。</p></td>
</tr>
<tr class="even">
<td><p><a href="marshaloptionsenum.md">MarshalOptionsEnum</a></p></td>
<td><p>サーバーにどのレコードが返されるかを指定します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="moverecordoptionsenum.md">MoveRecordOptionsEnum</a></p></td>
<td><p><strong>Record</strong> オブジェクトの <strong>MoveRecord</strong> メソッドの動作を指定します。</p></td>
</tr>
<tr class="even">
<td><p><a href="objectstateenum.md">ObjectStateEnum</a></p></td>
<td><p>オブジェクトが開いているか閉じているか、データ ソースに接続中か、コマンドを実行中か、またはデータを取得中かどうかを指定します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="parameterattributesenum.md">ParameterAttributesEnum</a></p></td>
<td><p><strong>Parameter</strong> オブジェクトの属性を指定します。</p></td>
</tr>
<tr class="even">
<td><p><a href="parameterdirectionenum.md">ParameterDirectionEnum</a></p></td>
<td><p><strong>Parameter</strong> が入力パラメーターと出力パラメーターのいずれか、またはその両方を表すのか、あるいはストアド プロシージャからの戻り値であるかどうかを指定します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="persistformatenum.md">PersistFormatEnum</a></p></td>
<td><p><strong>Recordset</strong> を保存するときの形式を指定します。</p></td>
</tr>
<tr class="even">
<td><p><a href="positionenum.md">PositionEnum</a></p></td>
<td><p><strong>Recordset</strong> 内のレコード ポインターの現在の位置を指定します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="propertyattributesenum.md">PropertyAttributesEnum</a></p></td>
<td><p><strong>Property</strong> オブジェクトの属性を指定します。</p></td>
</tr>
<tr class="even">
<td><p><a href="recordcreateoptionsenum.md">RecordCreateOptionsEnum</a></p></td>
<td><p><strong>Record</strong> オブジェクトの <strong>Open</strong> メソッドに対して、既存の <strong>Record</strong> を開くか、新しい <strong>Record</strong> を作成するかを指定します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="recordopenoptionsenum.md">RecordOpenOptionsEnum</a></p></td>
<td><p><strong>Record</strong> を開くときのオプションを指定します。 これらの値は OR 演算子で結合することもできます。</p></td>
</tr>
<tr class="even">
<td><p><a href="recordstatusenum.md">RecordStatusEnum</a></p></td>
<td><p>バッチ更新または別の大量の操作に関するレコードのステータスを指定します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="recordtypeenum.md">RecordTypeEnum</a></p></td>
<td><p><strong>Record</strong> オブジェクトの種類を指定します。</p></td>
</tr>
<tr class="even">
<td><p><a href="resyncenum.md">ResyncEnum</a></p></td>
<td><p><strong>Resync</strong> の呼び出しによって、基になる値が上書きされるかどうかを表します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="saveoptionsenum.md">SaveOptionsEnum</a></p></td>
<td><p><strong>Stream</strong> オブジェクトからファイルに保存するときに、ファイルを作成するか、上書きするかを表します。これらの値は AND 演算子で結合できます。</p></td>
</tr>
<tr class="even">
<td><p><a href="schemaenum.md">SchemaEnum</a></p></td>
<td><p><strong>OpenSchema</strong> メソッドが取得するスキーマ <strong>Recordset</strong> の種類を指定します。 <strong>Recordset</strong> 内のレコードの検索方向を表します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="searchdirectionenum.md">SearchDirectionEnum</a></p></td>
<td><p><strong>Recordset</strong>内でのレコード検索の方向を指定します。実行する<strong>Seek</strong>の種類を指定します。</p></td>
</tr>
<tr class="even">
<td><p><a href="seekenum.md">SeekEnum</a></p></td>
<td><p>実行する<strong>Seek</strong>の種類を指定します。<strong>Stream</strong>オブジェクトを開くときのオプションを指定します。 これらの値は AND 演算子で結合できます。</p></td>
</tr>
<tr class="odd">
<td><p><a href="streamopenoptionsenum.md">StreamOpenOptionsEnum</a></p></td>
<td><p><strong>Stream</strong> オブジェクトを開くときのオプションを表します。 これらの値は、and 演算子と組み合わせて使用できます。stream オブジェクトから、ストリーム全体を読み取るか、または次の<strong></strong>行を読み取るかを指定します。</p></td>
</tr>
<tr class="even">
<td><p><a href="streamreadenum.md">StreamReadEnum</a></p></td>
<td><p>stream オブジェクトから、ストリーム全体を読み取るか、または次の<strong></strong>行を読み取るかを指定します。<strong>Stream</strong>オブジェクトに格納されているデータの種類を指定します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="streamtypeenum.md">StreamTypeEnum</a></p></td>
<td><p><strong>Stream</strong>オブジェクトに格納されているデータの種類を指定します。<strong>Stream</strong>オブジェクトに書き込む文字列に、行区切り記号を追加するかどうかを指定します。</p></td>
</tr>
<tr class="even">
<td><p><a href="streamwriteenum.md">StreamWriteEnum</a></p></td>
<td><p><strong>Stream</strong>オブジェクトに書き込む文字列に、行区切り記号を追加するかどうかを指定します。文字列として<strong>Recordset</strong>を取得するときの形式を指定します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="stringformatenum.md">StringFormatEnum</a></p></td>
<td><p>文字列として<strong>Recordset</strong>を取得するときの形式を指定します。<strong>Connection</strong>オブジェクトのトランザクション属性を指定します。</p></td>
</tr>
<tr class="even">
<td><p><a href="xactattributeenum.md">XactAttributeEnum</a></p></td>
<td><p><strong>Connection</strong> オブジェクトのトランザクション属性を表します。</p></td>
</tr>
</tbody>
</table>

