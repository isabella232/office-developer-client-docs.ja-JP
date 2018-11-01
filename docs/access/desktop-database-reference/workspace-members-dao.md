---
title: Workspace メンバー (DAO)
TOCTitle: Workspace Members
ms:assetid: 13ac7d41-1b25-20d2-5c85-0f21bfd38328
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845437(v=office.15)
ms:contentKeyID: 48543374
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ec5e11a8bdc33923ca92f96833605338e9f19566
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889995"
---
# <a name="workspace-members-dao"></a>Workspace メンバー (DAO)


**適用されます**Access 2013、Office 2013。

Workspace オブジェクトは、ユーザー用に名前付きセッションを定義します。これには開いているデータベースが含まれ、同時実行トランザクションのメカニズムを提供し、Microsoft Access ワークスペースの場合は、セキュリティが設定されたワークグループをサポートします。

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
<td><p><strong><a href="workspace-begintrans-method-dao.md">BeginTrans</a></strong></p></td>
<td><p>新しいトランザクションを開始します。値の取得および設定が可能です。データベース型 ( <strong>Database</strong>) の値を使用します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="workspace-close-method-dao.md">閉じる</a></strong></p></td>
<td><p>開いている <strong>Workspace</strong> を閉じます。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="workspace-committrans-method-dao.md">CommitTrans</a></strong></p></td>
<td><p>現在のトランザクションを終了し、変更を保存します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="workspace-createdatabase-method-dao.md">データベース</a></strong></p></td>
<td><p>新しい <strong><a href="database-object-dao.md">Database</a></strong> オブジェクトを作成し、そのデータベースをディスクに保存し、開かれた <strong>Database</strong> オブジェクトとして返します (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="workspace-openconnection-method-dao.md">されます</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>[!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</P>


<p>ODBC データ ソースの <strong><a href="connection-object-dao.md">Connection</a></strong> オブジェクトを開きます (ODBCDirect ワークスペースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="workspace-opendatabase-method-dao.md">OpenDatabase</a></strong></p></td>
<td><p><strong><a href="workspace-object-dao.md">Workspace</a></strong> オブジェクト内で指定されたデータベースを開き、そのデータベースを表す <strong><a href="database-object-dao.md">Database</a></strong> オブジェクトへの参照を返します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="workspace-rollback-method-dao.md">Rollback</a></strong></p></td>
<td><p>現在のトランザクションを終了し、 <strong>Workspace</strong> オブジェクト内のすべてのデータベースを、現在のトランザクションが開始される前の状態に戻します。</p></td>
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
<td><p><strong><a href="workspace-connections-property-dao.md">Connections</a></strong></p></td>
<td><p>指定された <strong>Workspace</strong> の現在の接続を表す <strong>Connections</strong> コレクションを取得します。値の取得のみ可能です。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="workspace-databases-property-dao.md">Databases</a></strong></p></td>
<td><p>指定された <strong>Workspace</strong> の開いているデータベースを表す <strong>Databases</strong> コレクションを取得します。値の取得のみ可能です。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="workspace-defaultcursordriver-property-dao.md">DefaultCursorDriver</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>[!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</P>


<p><strong><a href="dbengine-openconnection-method-dao.md">OpenConnection</a></strong> メソッドまたは <strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong> メソッドによって作成された接続で使用されるカーソル ドライバーの種類を設定または取得します (ODBCDirect ワークスペースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="workspace-isolateodbctrans-property-dao.md">IsolateODBCTrans</a></strong></p></td>
<td><p>同じ Microsoft Access データベース エンジンに接続された ODBC データ ソースに関連する複数のトランザクションが分離されているかどうかを示す値を設定または取得します (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="workspace-logintimeout-property-dao.md">LoginTimeout</a></strong></p></td>
<td><p>ODBC データベースへのログオンを試みてからエラーが発生するまでの秒数を設定または取得します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="workspace-name-property-dao.md">Name</a></strong></p></td>
<td><p>指定したオブジェクトの名前を取得または設定します。オブジェクトがコレクションに追加されていない場合、値の取得および設定が可能です。文字列型 ( <strong>String</strong>) の値を使用します。オブジェクトがコレクションに追加されている場合、値の取得のみ可能です。文字列型 ( <strong>String</strong>) の値を使用します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="workspace-properties-property-dao.md">Properties</a></strong></p></td>
<td><p>指定したオブジェクトの <strong><a href="properties-collection-dao.md">Properties</a></strong> コレクションを取得します。値の取得のみ可能です。  </p></td>
</tr>
<tr class="even">
<td><p><strong><a href="workspace-type-property-dao.md">型</a></strong></p></td>
<td><p>オブジェクトの操作の種類またはデータ型を示す値を設定または取得します。値の取得のみ可能です。整数型 ( <strong>Integer</strong> ) の値を使用します。</p></td>
</tr>
</tbody>
</table>

