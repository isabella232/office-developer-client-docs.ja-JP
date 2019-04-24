---
title: Connection メンバー (DAO)
TOCTitle: Connection Members
ms:assetid: 94fc60ee-b6f2-cf08-b008-ed51bf7e7f8c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197681(v=office.15)
ms:contentKeyID: 48546422
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 098f44d87390351c23e61000ecbe47eae35810ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295906"
---
# <a name="connection-members-dao"></a>Connection メンバー (DAO)

**適用先:** Access 2013、Office 2013

> [!NOTE]
> [!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。 Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。 Connection オブジェクトは、ODBC データベースへの接続を表します (ODBCDirect ワークスペースのみ)。
 
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
<td><p><strong><a href="connection-cancel-method-dao.md">Cancel</a></strong></p></td>
<td><p>保留中の非同期メソッド呼び出しの実行をキャンセルします (ODBCDirect ワークスペースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="connection-close-method-dao.md">閉じる</a></strong></p></td>
<td><p>開いている <strong>Connection</strong> を閉じます。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="connection-createquerydef-method-dao.md">CreateQueryDef</a></strong></p></td>
<td><p>新しい <strong><a href="querydef-object-dao.md">QueryDef</a></strong> オブジェクトを作成します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="connection-execute-method-dao.md">Execute</a></strong></p></td>
<td><p>指定したオブジェクトのアクション クエリまたは SQL ステートメントを実行します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong></p></td>
<td><p>新しい <strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトを作成して <strong>Recordsets</strong> コレクションに追加します。</p></td>
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
<td><p><strong><a href="connection-connect-property-dao.md">Connect</a></strong></p></td>
<td><p>開いている接続のソースに関する情報を提供する値を設定または取得します。 値の取得と設定が可能な文字列型 (<strong>String</strong>) の値です。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="connection-database-property-dao.md">Database</a></strong></p></td>
<td><p>この接続に対応する<strong><a href="database-object-dao.md">Database</a></strong>オブジェクトを返します (ODBCDirect ワークスペースのみ)。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="connection-name-property-dao.md">Name</a></strong></p></td>
<td><p><strong><a href="connection-object-dao.md">Connection</a></strong> オブジェクトの名前を取得します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="connection-querydefs-property-dao.md">QueryDefs</a></strong></p></td>
<td><p>指定した接続のすべての <strong>QueryDef</strong> オブジェクトを含む <strong>QueryDefs</strong> コレクションを返します。 読み取り専用です。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="connection-querytimeout-property-dao.md">QueryTimeout</a></strong></p></td>
<td><p>ODBC データ ソースでクエリが実行される場合の、タイムアウト エラーが発生するまでに待機する秒数を指定する値を設定または取得します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="connection-recordsaffected-property-dao.md">RecordsAffected</a></strong></p></td>
<td><p>最後に呼び出した <strong><a href="connection-execute-method-dao.md">Execute</a></strong> メソッドの処理対象となったレコードの数を取得します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="connection-recordsets-property-dao.md">Recordsets</a></strong></p></td>
<td><p>指定した接続の開いているレコードセットをすべて含む <strong>Recordsets</strong> コレクションを返します。 値の取得のみ可能です。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="connection-stillexecuting-property-dao.md">StillExecuting</a></strong></p></td>
<td><p>非同期操作 (つまり、 <strong>dbRunAsync</strong> オプションを指定して呼び出したメソッド) の実行が完了したかどうかを示します (ODBCDirect ワークスペースのみ)。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="connection-transactions-property-dao.md">トランザクション</a></strong></p></td>
<td><p>オブジェクトがトランザクションをサポートしているかどうかを示す値を返します。 読み取り専用の <strong>Boolean</strong> です。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="connection-updatable-property-dao.md">Updatable</a></strong></p></td>
<td><p>DAO オブジェクトを変更できるかどうかを示す値を取得します。値の取得のみ可能です。ブール型 (<strong>Boolean</strong>) の値を使用します。</p></td>
</tr>
</tbody>
</table>

