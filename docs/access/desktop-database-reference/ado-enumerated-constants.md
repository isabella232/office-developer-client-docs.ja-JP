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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707942"
---
# <a name="ado-enumerated-constants"></a>ADO の列挙定数

**適用されます**Access 2013、Office 2013。

ここでは、デバッグ用に各定数の実際の値の一覧を示します。ただし、この値は参考用のものであり、ADO のリリースごとに変更されることがあります。コードを記述するときは、列挙定数の実際の値ではなく、名前のみを使って記述するようにしてください。

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th>列挙型定数</th>
<th>説明</th>
</tr>
<tr class="odd">
<td><p><a href="adcprop-asyncthreadpriority-enum.md">ADCPROP_ASYNCTHREADPRIORITY_ENUM</a></p></td>
<td><p>RDS の <strong>Recordset</strong> オブジェクトに対して、データを取得する非同期スレッドの実行優先度を表します。</p></td>
</tr>
<tr class="even">
<td><p><a href="adcprop-autorecalc-enum.md">ADCPROP_AUTORECALC_ENUM</a></p></td>
<td><p><strong>MSDataShape</strong>プロバイダーが再階層<strong>レコード セット</strong>内の集計と集計の列を計算すると指定します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="adcprop-updatecriteria-enum.md">ADCPROP_UPDATECRITERIA_ENUM</a></p></td>
<td><p><strong>Recordset</strong> オブジェクトを使用してデータ ソース行の共有的更新を行う際に、競合の検出に使用するフィールドを表します。</p></td>
</tr>
<tr class="even">
<td><p><a href="adcprop-updateresync-enum.md">ADCPROP_UPDATERESYNC_ENUM</a></p></td>
<td><p><strong>UpdateBatch</strong> メソッドに暗黙の <strong>Resync</strong> メソッド操作が続くかどうかを示し、続く場合はその操作の適用範囲を指定します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="affectenum.md">AffectEnum</a></p></td>
<td><p>操作の対象となるレコードを表します。</p></td>
</tr>
<tr class="even">
<td><p><a href="bookmarkenum.md">BookmarkEnum</a></p></td>
<td><p>操作の開始位置を示すブックマークを表します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="commandtypeenum.md">CommandTypeEnum</a></p></td>
<td><p>コマンド引数の解釈方法を表します。</p></td>
</tr>
<tr class="even">
<td><p><a href="compareenum.md">CompareEnum</a></p></td>
<td><p>ブックマークで表された 2 つのレコードの相対位置を表します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="connectmodeenum.md">ConnectModeEnum</a></p></td>
<td><p><strong>Connection</strong> 内のデータの編集、 <strong>Record</strong> のオープン、または <strong>Record</strong> および <strong>Stream</strong> オブジェクトの <strong>Mode</strong> プロパティの値の指定に対する権限を表します。</p></td>
</tr>
<tr class="even">
<td><p><a href="connectoptionenum.md">ConnectOptionEnum</a></p></td>
<td><p><strong>Connection</strong> オブジェクトの <strong>Open</strong> メソッドから制御が戻るのが、接続確立の後 (同期) か前 (非同期) かを表します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="connectpromptenum.md">ConnectPromptEnum</a></p></td>
<td><p>ODBC データ ソースとの接続を開くときに、不足しているパラメーターを要求するダイアログ ボックスを表示するかどうかを指定します。</p></td>
</tr>
<tr class="even">
<td><p><a href="copyrecordoptionsenum.md">CopyRecordOptionsEnum</a></p></td>
<td><p><strong>CopyRecord</strong> メソッドの動作を表します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="cursorlocationenum.md">CursorLocationEnum</a></p></td>
<td><p>カーソル エンジンの場所を指定します。</p></td>
</tr>
<tr class="even">
<td><p><a href="cursoroptionenum.md">CursorOptionEnum</a></p></td>
<td><p><strong>Supports</strong> メソッドがテストする機能を表します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="cursortypeenum.md">CursorTypeEnum</a></p></td>
<td><p><strong>Recordset</strong> オブジェクトが使用するカーソルの種類を表します。</p></td>
</tr>
<tr class="even">
<td><p><a href="datatypeenum.md">DataTypeEnum</a></p></td>
<td><p><strong>Field</strong>、<strong>Parameter</strong>、または <strong>Property</strong> のデータ型を指定します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="editmodeenum.md">EditModeEnum</a></p></td>
<td><p>レコードの編集状況を示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="errorvalueenum.md">ErrorValueEnum</a></p></td>
<td><p>ADO 実行時エラーの種類を表します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="eventreasonenum.md">EventReasonEnum</a></p></td>
<td><p>イベントが発生した理由を表します。</p></td>
</tr>
<tr class="even">
<td><p><a href="eventstatusenum.md">EventStatusEnum</a></p></td>
<td><p>イベントの実行の現在の状態を表します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="executeoptionenum.md">ExecuteOptionEnum</a></p></td>
<td><p>プロバイダーによるコマンドの実行方法を表します。</p></td>
</tr>
<tr class="even">
<td><p><a href="fieldenum.md">FieldEnum</a></p></td>
<td><p><strong>Record</strong> オブジェクトの <strong>Fields</strong> コレクションで参照される特定のフィールドを表します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="fieldattributeenum.md">FieldAttributeEnum</a></p></td>
<td><p><strong>Field</strong> オブジェクトの 1 つ以上の属性を表します。</p></td>
</tr>
<tr class="even">
<td><p><a href="fieldstatusenum.md">FieldStatusEnum</a></p></td>
<td><p><strong>Field</strong> オブジェクトの状態を表します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="filtergroupenum.md">FilterGroupEnum</a></p></td>
<td><p><strong>Recordset</strong> でフィルターの対象となるレコード グループを表します。</p></td>
</tr>
<tr class="even">
<td><p><a href="getrowsoptionenum.md">GetRowsOptionEnum</a></p></td>
<td><p><strong>Recordset</strong> から取得するレコード数を表します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="isolationlevelenum.md">IsolationLevelEnum</a></p></td>
<td><p><strong>Connection</strong> オブジェクトのトランザクション分離レベルを表します。</p></td>
</tr>
<tr class="even">
<td><p><a href="lineseparatorsenum.md">LineSeparatorsEnum</a></p></td>
<td><p>テキスト <strong>Stream</strong> オブジェクトの行区切り記号に使われている文字を表します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="locktypeenum.md">LockTypeEnum</a></p></td>
<td><p>編集時にレコードに適用されるロックの種類を表します。</p></td>
</tr>
<tr class="even">
<td><p><a href="marshaloptionsenum.md">MarshalOptionsEnum</a></p></td>
<td><p>サーバーにどのレコードが返されるかを表します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="moverecordoptionsenum.md">MoveRecordOptionsEnum</a></p></td>
<td><p><strong>Record</strong> オブジェクトの <strong>MoveRecord</strong> メソッドの動作を表します。</p></td>
</tr>
<tr class="even">
<td><p><a href="objectstateenum.md">ObjectStateEnum</a></p></td>
<td><p>オブジェクトが開いているか閉じているか、データ ソースに接続中か、コマンドを実行中か、またはデータを取得中かどうかを指定します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="parameterattributesenum.md">ParameterAttributesEnum</a></p></td>
<td><p><strong>Parameter</strong> オブジェクトの属性を表します。</p></td>
</tr>
<tr class="even">
<td><p><a href="parameterdirectionenum.md">ParameterDirectionEnum</a></p></td>
<td><p><strong>Parameter</strong> が入力パラメーターと出力パラメーターのいずれか、またはその両方を表すのか、あるいはストアド プロシージャからの戻り値であるかどうかを指定します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="persistformatenum.md">PersistFormatEnum</a></p></td>
<td><p><strong>Recordset</strong> を保存するときの形式を表します。</p></td>
</tr>
<tr class="even">
<td><p><a href="positionenum.md">PositionEnum</a></p></td>
<td><p><strong>Recordset</strong> 内のレコード ポインターの現在の位置を表します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="propertyattributesenum.md">PropertyAttributesEnum</a></p></td>
<td><p><strong>Property</strong> オブジェクトの属性を表します。</p></td>
</tr>
<tr class="even">
<td><p><a href="recordcreateoptionsenum.md">RecordCreateOptionsEnum</a></p></td>
<td><p><strong>Record</strong> オブジェクトの <strong>Open</strong> メソッドに対して、既存の <strong>Record</strong> を開くか、新しい <strong>Record</strong> を作成するかを指定します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="recordopenoptionsenum.md">RecordOpenOptionsEnum</a></p></td>
<td><p><strong>Record</strong> を開くときのオプションを指定します。これらの値は OR 演算子で結合することもできます。</p></td>
</tr>
<tr class="even">
<td><p><a href="recordstatusenum.md">RecordStatusEnum</a></p></td>
<td><p>バッチ更新またはその他の一括操作に関するレコードの状態を表します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="recordtypeenum.md">RecordTypeEnum</a></p></td>
<td><p><strong>Record</strong> オブジェクトの種類を表します。</p></td>
</tr>
<tr class="even">
<td><p><a href="resyncenum.md">ResyncEnum</a></p></td>
<td><p><strong>Resync</strong> の呼び出しによって基になる値が上書きされるかどうかを表します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="saveoptionsenum.md">SaveOptionsEnum</a></p></td>
<td><p><strong>Stream</strong> オブジェクトからファイルに保存するときに、ファイルを作成するか、上書きするかを表します。これらの値は AND 演算子で結合できます。</p></td>
</tr>
<tr class="even">
<td><p><a href="schemaenum.md">SchemaEnum</a></p></td>
<td><p><strong>OpenSchema</strong> メソッドが取得するスキーマ <strong>Recordset</strong> の種類を指定します。<strong>Recordset</strong> 内のレコードの検索方向を表します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="searchdirectionenum.md">SearchDirectionEnum</a></p></td>
<td><p><strong>レコード セット</strong>内のレコードの検索の方向を指定します。実行する<strong>Seek</strong>の種類を指定します。</p></td>
</tr>
<tr class="even">
<td><p><a href="seekenum.md">SeekEnum</a></p></td>
<td><p>実行する<strong>Seek</strong>の種類を指定します。<strong>Stream</strong>オブジェクトを開くためのオプションを指定します。 これらの値は AND 演算子で結合できます。</p></td>
</tr>
<tr class="odd">
<td><p><a href="streamopenoptionsenum.md">StreamOpenOptionsEnum</a></p></td>
<td><p><strong>Stream</strong> オブジェクトを開くときのオプションを表します。 値は、AND 演算子で結合することができます。ストリーム全体、または次の行を<strong>ストリーム</strong>オブジェクトから読み取る必要があるかどうかを指定します。</p></td>
</tr>
<tr class="even">
<td><p><a href="streamreadenum.md">StreamReadEnum</a></p></td>
<td><p>ストリーム全体、または次の行を<strong>ストリーム</strong>オブジェクトから読み取る必要があるかどうかを指定します。<strong>Stream</strong>オブジェクトに格納されたデータの種類を指定します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="streamtypeenum.md">StreamTypeEnum</a></p></td>
<td><p><strong>Stream</strong>オブジェクトに格納されたデータの種類を指定します。<strong>ストリーム</strong>オブジェクトに書き込む文字列を行区切り記号を追加するかどうかを指定します。</p></td>
</tr>
<tr class="even">
<td><p><a href="streamwriteenum.md">StreamWriteEnum</a></p></td>
<td><p><strong>ストリーム</strong>オブジェクトに書き込む文字列を行区切り記号を追加するかどうかを指定します。文字列として<strong>Recordset</strong>を取得するときに形式を指定します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="stringformatenum.md">StringFormatEnum</a></p></td>
<td><p>文字列として<strong>Recordset</strong>を取得するときに形式を指定します。<strong>Connection</strong>オブジェクトのトランザクション属性を指定します。</p></td>
</tr>
<tr class="even">
<td><p><a href="xactattributeenum.md">XactAttributeEnum</a></p></td>
<td><p><strong>Connection</strong> オブジェクトのトランザクション属性を表します。</p></td>
</tr>
</tbody>
</table>

