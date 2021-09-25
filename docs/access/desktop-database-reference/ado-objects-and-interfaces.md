---
title: ADO のオブジェクトとインターフェイス
TOCTitle: ADO objects and interfaces
ms:assetid: bebf4a80-8b6e-c43c-4138-897055cc60d3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249927(v=office.15)
ms:contentKeyID: 48547471
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 92599e81fcaf1303bd1c77c1d6f09acfe5dd63a2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59553236"
---
# <a name="ado-objects-and-interfaces"></a>ADO のオブジェクトとインターフェイス

**適用先:** Access 2013、Office 2013

これらのオブジェクト間の関係は、データ オブジェクト (ADO) ActiveXモデルで表されます。

各オブジェクトは、対応するコレクションに格納できます。 たとえば、[Error](error-object-ado.md) オブジェクトは [Errors](errors-collection-ado.md) コレクションに格納できます。 詳細については [、「ADO コレクションまたは特定のコレクションの](ado-collections.md) トピック」を参照してください。

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th>オブジェクト</th>
<th>説明</th>
</tr>
<tr class="odd">
<td><p><a href="adorecordconstruction-interface-ado.md">ADORecordConstruction</a></p></td>
<td><p>C/C++ アプリケーションで OLE DB <strong>Row</strong> オブジェクトから ADO <strong>Record</strong> オブジェクトを構築します。</p></td>
</tr>
<tr class="even">
<td><p><a href="adorecordsetconstruction-interface-ado.md">ADORecordsetConstruction</a></p></td>
<td><p>C/C++ アプリケーションで OLE DB <strong>Rowset</strong> オブジェクトから ADO <strong>Recordset</strong> オブジェクトを構築します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="error-object-ado.md">Command</a></p></td>
<td><p>データ ソースに対して実行する特定のコマンドを定義します。</p></td>
</tr>
<tr class="even">
<td><p><a href="field-object-ado.md">Connection</a></p></td>
<td><p>データ ソースに対して開かれている接続を表します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="error-object-ado.md">エラー</a></p></td>
<td><p>プロバイダーを含む単一の操作に関連して発生した、データ アクセス エラーの詳細情報を格納しています。</p></td>
</tr>
<tr class="even">
<td><p><a href="field-object-ado.md">Field</a></p></td>
<td><p>共通のデータ型を持つデータの列を表します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="parameter-object-ado.md">パラメーター</a></p></td>
<td><p>パラメーター クエリまたはストアド プロシージャに基づく、<strong>Command</strong> オブジェクトに関連付けられたパラメーターまたは引数を表します。</p></td>
</tr>
<tr class="even">
<td><p><a href="property-object-ado.md">プロパティ</a></p></td>
<td><p>プロバイダーで定義される ADO オブジェクトの動的特性を表します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="record-object-ado.md">Record</a></p></td>
<td><p><strong>Recordset</strong> の行、またはファイル システム内のディレクトリやファイルを表します。</p></td>
</tr>
<tr class="even">
<td><p><a href="recordset-object-ado.md">Recordset</a></p></td>
<td><p>基になるテーブルのレコードセット全体、またはコマンドの実行によって返された結果を表します。 <strong>Recordset</strong> オブジェクトでは、常にレコードセット内の 1 つのレコードのみをカレント レコードとして参照します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="stream-object-ado.md">Stream</a></p></td>
<td><p>データのバイナリ ストリームを表します。</p></td>
</tr>
</tbody>
</table>

<br/>

