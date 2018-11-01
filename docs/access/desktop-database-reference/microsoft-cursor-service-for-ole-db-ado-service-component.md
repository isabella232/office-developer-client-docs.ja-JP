---
title: OLE DB の Microsoft カーソル サービス (ADO サービス コンポーネント)
TOCTitle: Microsoft Cursor Service for OLE DB (ADO Service Component)
ms:assetid: 6818fc05-9c9f-9b67-07d2-e622c93133c2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249405(v=office.15)
ms:contentKeyID: 48545376
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1f164e2671fb27a8e8a8721010bdad518f2d199e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879047"
---
# <a name="microsoft-cursor-service-for-ole-db-ado-service-component"></a>OLE DB の Microsoft カーソル サービス (ADO サービス コンポーネント)


**適用されます**Access 2013、Office 2013。

Microsoft Cursor Service for OLE DB は、データ プロバイダーのカーソル サポート機能を補完します。その結果、すべてのデータ プロバイダーで機能の統一感が向上します。

Cursor Service は、動的プロパティを利用可能にして特定のメソッドの動作を拡張します。たとえば、動的プロパティ [Optimize](optimize-property-dynamic-ado.md) を使用すると、一時インデックスの作成が可能になり、 [Find](find-method-ado.md) メソッドなどの特定の操作が容易になります。

Cursor Service を使用すると、あらゆる場合での一括更新が可能になります。また、静的カーソルのみを提供するデータ プロバイダーでも、動的カーソルなどの、より機能的なカーソルを模擬的に利用できるようにします。

## <a name="keyword"></a>キーワード

このサービス コンポーネントを呼び出すには、[Recordset](recordset-object-ado.md) オブジェクトまたは [Connection](connection-object-ado.md) オブジェクトの [CursorLocation](cursorlocation-property-ado.md) プロパティを **adUseClient** に設定します。

`connection.CursorLocation=adUseClientrecordset.CursorLocation=adUseClient`

## <a name="dynamic-properties"></a>動的プロパティ

Cursor Service for OLE DB を呼び出すと、次に示す動的プロパティが **Recordset** オブジェクトの [Properties](properties-collection-ado.md) コレクションに追加されます。 **Connection** オブジェクトおよび **Recordset** オブジェクトのすべての動的プロパティの一覧については、「 [ADO の動的プロパティ インデックス](ado-dynamic-property-index.md)」を参照してください。対応する OLE DB プロパティ名がある場合は、ADO プロパティ名の後にかっこで囲んで示しています。

Cursor Service を呼び出した後、動的プロパティを変更しても、基になるデータ ソースで認識されない場合があります。 などの**レコード セット**の*コマンドのタイムアウト*プロパティを設定は表示されませんを基になるデータ プロバイダー。

```vb 
... 
Recordset1.CursorLocation = adUseClient 'invokes cursor service 
Recordset1.Open "authors", _ 
 "Provider=SQLOLEDB;Data Source=DBServer;User Id=usr;" & _ 
 "Password=pwd;Initial Catalog=pubs;",,adCmdTable 
Recordset1.Properties.Item("Command Time out") = 50 
' 'Command Time out' property on DBServer is still default (30). 
... 

```

アプリケーションが Cursor Service を必要とし、基になるプロバイダーの動的プロパティを設定する必要がある場合は、Cursor Service を呼び出す前に動的プロパティを設定します。コマンド オブジェクトのプロパティの設定値は、カーソルの位置に関係なく、常に基になるデータ プロバイダーに渡されます。したがって、いつでも、コマンド オブジェクトを使用してプロパティを設定することもできます。

> [!NOTE]
> 動的プロパティ DBPROP_SERVERDATAONINSERT は、基になるデータ プロバイダーでサポートされている場合でも、カーソル サービスではサポートされません。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>プロパティ名</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Auto Recalc<br />
(DBPROP_ADC_AUTORECALC)</p></td>
<td><p>Data Shaping Service で作成されたレコードセットの場合、この値は計算列および集計列の計算頻度を示します。既定値 (1) の場合は、Data Shaping Service で値の変更が確認されるたびに再計算が行われます。この値が 0 の場合は、階層が最初に構築されたときにのみ計算列または集計列が計算されます。</p></td>
</tr>
<tr class="even">
<td><p>Batch Size<br />
(DBPROP_ADC_BATCHSIZE)</p></td>
<td><p>データ ストアに送信するまでにバッチ処理できる更新ステートメントの数を示します。1 回のバッチ処理に含めるステートメント数が多いほど、データ ストアとのやり取りの回数が少なくなります。</p></td>
</tr>
<tr class="odd">
<td><p>Cache Child Rows<br />
(DBPROP_ADC_CACHECHILDROWS)</p></td>
<td><p>Data Shaping Service で作成されたレコードセットの場合、この値は、子レコードセットを後で使用できるようにキャッシュに保存しておくかどうかを示します。</p></td>
</tr>
<tr class="even">
<td><p>Cursor Engine Version<br />
(DBPROP_ADC_CEVER)</p></td>
<td><p>使用する Cursor Service のバージョンを示します。</p></td>
</tr>
<tr class="odd">
<td><p>Maintain Change Status<br />
(DBPROP_ADC_MAINTAINCHANGESTATUS)</p></td>
<td><p>複数のテーブルの結合で、行を再同期化するために使用するコマンドのテキストを示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="optimize-property-dynamic-ado.md">最適化</a></p></td>
<td><p>インデックスを作成するかどうかを示します。<strong>True</strong> に設定すると、特定の操作の実行速度を向上させるために一時的なインデックスの作成が許可されます。</p></td>
</tr>
<tr class="odd">
<td><p><a href="reshape-name-property-dynamic-ado.md">Reshape Name</a></p></td>
<td><p><strong>Recordset</strong> の名前を示します。現在またはそれ以降のデータ シェイプ コマンドで参照される場合があります。</p></td>
</tr>
<tr class="even">
<td><p><a href="resync-command-property-dynamic-ado.md">Resync Command</a></p></td>
<td><p><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table</a> プロパティが有効である場合に、<a href="resync-method-ado.md">Resync</a> メソッドで使用されるカスタム コマンド文字列を示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Catalog</a></p></td>
<td><p><strong>Unique Table</strong> プロパティで参照されるテーブルを格納しているデータベースの名前を示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Schema</a></p></td>
<td><p><strong>Unique Table</strong> プロパティで参照されるテーブルの所有者の名前を示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table</a></p></td>
<td><p>挿入、更新、または削除によって変更された可能性がある複数のテーブルから作成された <strong>Recordset</strong> 内の 1 つのテーブル名を示します。</p></td>
</tr>
<tr class="even">
<td><p>Update Criteria<br />
(DBPROP_ADC_UPDATECRITERIA)</p></td>
<td><p>更新時に発生する競合の処理に使用される <strong>WHERE</strong> 句のフィールドを示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="update-resync-property-dynamic-ado.md">Update Resync</a>(DBPROP_ADC_UPDATERESYNC)</p></td>
<td><p><strong>Unique Table</strong> プロパティが有効である場合に、<a href="updatebatch-method-ado.md">UpdateBatch</a> メソッド (およびその動作) の後に、<strong>Resync</strong> メソッドを暗黙に呼び出すかどうかを示します。</p></td>
</tr>
</tbody>
</table>


動的プロパティの名前を **Properties** コレクションのインデックスとして指定して、動的プロパティを設定または取得することもできます。たとえば、 [Optimize](optimize-property-dynamic-ado.md) 動的プロパティの値を取得して出力した後、新しい値を設定するには、次のように指定します。

```vb 
 
Debug.Print rs.Properties("Optimize") 
rs.Properties("Optimize") = True 
```

## <a name="built-in-property-behavior"></a>組み込みプロパティの動作

Cursor Service for OLE DB は、特定の組み込みプロパティの動作にも影響を与えます。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>プロパティ名</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="cursortype-property-ado.md">カーソル。</a></p></td>
<td><p><strong>Recordset</strong> で利用可能なカーソルの種類を補完します。</p></td>
</tr>
<tr class="even">
<td><p><a href="locktype-property-ado.md">ロック。</a></p></td>
<td><p><strong>Recordset</strong> で利用可能なロックの種類を補完します。一括更新を可能にします。</p></td>
</tr>
<tr class="odd">
<td><p><a href="sort-property-ado.md">Sort</a></p></td>
<td><p><strong>Recordset</strong> の並べ替えに使用するフィールド名、および各フィールドの並べ替え順序が昇順か降順かを指定します。</p></td>
</tr>
</tbody>
</table>


## <a name="method-behavior"></a>メソッドの動作

Cursor Service for OLE DB は、[Field](field-object-ado.md) オブジェクトの [Append](append-method-ado.md) メソッドや、 **Recordset** オブジェクトの [Open](open-method-ado-recordset.md) メソッド、 [Resync](resync-method-ado.md) メソッド、 [UpdateBatch](updatebatch-method-ado.md) メソッド、および [Save](save-method-ado.md) メソッドにも影響を与えます。

