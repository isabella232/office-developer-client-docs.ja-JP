---
title: DBEngine メンバー (DAO)
TOCTitle: DBEngine Members
ms:assetid: 740b6a85-585f-0e1d-710b-84ba24825325
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195868(v=office.15)
ms:contentKeyID: 48545652
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1128b27385ef9f8c898fb79d05ae28d596c4af6a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294282"
---
# <a name="dbengine-members-dao"></a>DBEngine メンバー (DAO)


**適用先:** Access 2013、Office 2013

DBEngine オブジェクトは、DAO オブジェクト モデル内のトップ レベル オブジェクトです。

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
<td><p><strong><a href="dbengine-begintrans-method-dao.md">BeginTrans</a></strong></p></td>
<td><p>新しいトランザクションを開始します。 読み取り/書き込みの<strong>データベース</strong>です。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-committrans-method-dao.md">CommitTrans</a></strong></p></td>
<td><p>現在のトランザクションを終了し、変更を保存します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-compactdatabase-method-dao.md">CompactDatabase</a></strong></p></td>
<td><p>閉じられたデータベースをコピーして最適化し、そのデータベースのバージョン、照合順序、暗号化を変更するオプションを使用できます。 (Microsoft access ワークスペースのみ)。 .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-createdatabase-method-dao.md">CreateDatabase</a></strong></p></td>
<td><p>新しい <strong><a href="database-object-dao.md">Database</a></strong> オブジェクトを作成し、そのデータベースをディスクに保存し、開かれた <strong>Database</strong> オブジェクトとして返します (Microsoft Access ワークスペースのみ)。 .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-createworkspace-method-dao.md">CreateWorkspace</a></strong></p></td>
<td><p>新しい <strong><a href="workspace-object-dao.md">Workspace</a></strong> オブジェクトを作成します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-idle-method-dao.md">アイドル</a></strong></p></td>
<td><p>データの処理を中断し、Microsoft Access データベース エンジンでメモリの最適化やページのタイムアウトなどのタスクを完了できるようにします (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-openconnection-method-dao.md">OpenConnection</a></strong></p></td>
<td><p><strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong>値の1つ。</p>
<td><p><strong>注</strong>: ODBCDirect ワークスペースは、Microsoft access 2013 ではサポートされていません。 Microsoft Office Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</p>
<p>ODBC データ ソースの <strong><a href="connection-object-dao.md">Connection</a></strong> オブジェクトを開きます (ODBCDirect ワークスペースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong></p></td>
<td><p>指定されたデータベースを開き、そのデータベースを表す <strong><a href="database-object-dao.md">Database</a></strong> オブジェクトへの参照を取得します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-registerdatabase-method-dao.md">RegisterDatabase</a></strong></p></td>
<td><p>ODBC データ ソースの接続情報を Windows レジストリに追加します。ODBC ドライバーでは、セッション中に ODBC データ ソースが開かれるときに、接続情報が必要になります。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-rollback-method-dao.md">Rollback</a></strong></p></td>
<td><p>現在のトランザクションを終了し、 <strong>Workspace</strong> オブジェクト内のデータベースを現在のトランザクションが開始された時点の状態に戻します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-setoption-method-dao.md">SetOption</a></strong></p></td>
<td><p>Windows レジストリに登録されている Microsoft Access データベース エンジンのキーの値を一時的に上書きします (Microsoft Access ワークスペースのみ)。</p></td>
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
<td><p><strong><a href="dbengine-defaultpassword-property-dao.md">DefaultPassword</a></strong></p></td>
<td><p>初期化されたときに、既定の<strong>Workspace</strong>オブジェクトを作成するために使用するパスワードを設定します。 値の取得と設定が可能な文字列型 (<strong>String</strong>) の値です。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-defaulttype-property-dao.md">DefaultType</a></strong></p></td>
<td><p>次に作成される <strong><a href="workspace-object-dao.md">Workspace</a></strong> オブジェクトが使用するワークスペースの種類を示す値を設定または取得します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-defaultuser-property-dao.md">DefaultUser</a></strong></p></td>
<td><p>初期化されたときに、既定の<strong>Workspace</strong>オブジェクトを作成するために使用されるユーザー名を設定します。 値の取得と設定が可能な文字列型 (<strong>String</strong>) の値です。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-errors-property-dao.md">エラー</a></strong></p></td>
<td><p>指定したオブジェクトの、すべての保存された <strong>Error</strong> オブジェクトを含む <strong>Errors</strong> コレクションを返します。 値の取得のみ可能です。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-inipath-property-dao.md">IniPath</a></strong></p></td>
<td><p>Microsoft Access データベース エンジン用の値が含まれた Windows レジストリ キーに関する情報を設定または取得します (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-logintimeout-property-dao.md">LoginTimeout</a></strong></p></td>
<td><p>ODBC データベースへのログオン試行でエラーが発生するまでの秒数を設定または取得します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-properties-property-dao.md">Properties</a></strong></p></td>
<td><p>指定したオブジェクトの <strong><a href="properties-collection-dao.md">Properties</a></strong> コレクションを取得します。値の取得のみ可能です。  </p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-version-property-dao.md">バージョン</a></strong></p></td>
<td><p>rreturns 現在使用されている DAO のバージョンを返します。 読み取りのみ可能な <strong>String</strong> 値です。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-workspaces-property-dao.md">Workspaces</a></strong></p></td>
<td><p>アクティブな、隠されていない <strong>Workspace</strong> オブジェクトをすべて含む <strong>Workspaces</strong> コレクションを返します。 値の取得のみ可能です。</p></td>
</tr>
</tbody>
</table>

