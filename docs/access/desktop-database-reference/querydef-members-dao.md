---
title: QueryDef メンバー (DAO)
TOCTitle: QueryDef Members
ms:assetid: 3f914d23-aa63-3ebd-1d86-4f53da71131b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192855(v=office.15)
ms:contentKeyID: 48544403
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5b3afc134636d5621f38ece4530be5312e42bc74
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302983"
---
# <a name="querydef-members-dao"></a>QueryDef メンバー (DAO)


**適用先:** Access 2013、Office 2013

QueryDef オブジェクトは、Microsoft Access データベース エンジン データベースのクエリのストアド定義を表します。

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
<td><p><strong><a href="querydef-cancel-method-dao.md">Cancel</a></strong></p></td>
<td><p><strong>注</strong>: ODBCDirect ワークスペースは、Microsoft access 2013 ではサポートされていません。 Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</p>
<p>保留中の非同期メソッド呼び出しの実行をキャンセルします (ODBCDirect ワークスペースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-close-method-dao.md">閉じる</a></strong></p></td>
<td><p>開いている <strong>QueryDef</strong> を閉じます。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-createproperty-method-dao.md">CreateProperty</a></strong></p></td>
<td><p>新しいユーザー定義の <strong><a href="property-object-dao.md">Property</a></strong> オブジェクトを作成します (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-execute-method-dao.md">Execute</a></strong></p></td>
<td><p>指定したオブジェクトの SQL ステートメントを実行します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-openrecordset-method-dao.md">OpenRecordset</a></strong></p></td>
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
<td><p><strong><a href="querydef-cachesize-property-dao.md">CacheSize</a></strong></p></td>
<td><p>ローカルにキャッシュされる ODBC データソースから取得したレコード数を設定または取得します。 値の取得と設定が可能な長整数型 (<strong>Long</strong>) の値です。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-connect-property-dao.md">Connect</a></strong></p></td>
<td><p>パススルークエリで使用されるデータベースのソースについての情報を提供する値を設定または取得します。 読み取りのみ可能な <strong>String</strong> 値です。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-datecreated-property-dao.md">DateCreated</a></strong></p></td>
<td><p>オブジェクトを作成した日付と時刻を取得します (Microsoft Access ワークスペースのみ)。値の取得のみ可能です。バリアント型 ( <strong>Variant</strong> ) の値を使用します。  </p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-fields-property-dao.md">Fields</a></strong></p></td>
<td><p>指定したオブジェクトに格納されているすべての <strong><a href="fields-collection-dao.md">Field</a></strong> オブジェクトを表す <strong><a href="field-object-dao.md">Fields</a></strong> コレクションを取得します。 値の取得のみ可能です。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-lastupdated-property-dao.md">LastUpdated</a></strong></p></td>
<td><p>オブジェクトを最後に変更した日付および時刻を取得します。値の取得のみ可能です。バリアント型 ( <strong>Variant</strong> ) の値を使用します。  </p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-maxrecords-property-dao.md">MaxRecords</a></strong></p></td>
<td><p>ODBC データ ソースに対して実行するクエリから返されるレコードの最大数を設定または取得します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-name-property-dao.md">Name</a></strong></p></td>
<td><p>指定したオブジェクトの名前を取得または設定します。値の取得および設定が可能です。文字列型 ( <strong>String</strong> ) の値を使用します。  </p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-odbctimeout-property-dao.md">ODBCTimeout</a></strong></p></td>
<td><p>ODBC データベースに対して <strong><a href="querydef-object-dao.md">QueryDef</a></strong> を実行したときに、タイムアウト エラーが発生するまでの待ち時間を秒単位で示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-parameters-property-dao.md">パラメーター</a></strong></p></td>
<td><p>指定した<strong>QueryDef</strong>のすべての<strong><a href="parameter-object-dao.md">Parameter</a></strong>オブジェクトを含む<strong><a href="parameters-collection-dao.md">Parameters</a></strong>コレクションを返します。 読み取り専用です。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-prepare-property-dao.md">準備</a></strong></p></td>
<td><p><strong>注</strong>: ODBCDirect ワークスペースは、Microsoft access 2013 ではサポートされていません。 Microsoft Office Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</p>
<p>ODBC <strong>SQLPrepare</strong> API 関数を使用して、実行する前にクエリを一時的なストアド プロシージャとしてサーバーに準備する必要があるか、または ODBC <strong>SQLExecDirect</strong> API 関数を使用して、クエリを直接実行するかどうかを示す値を設定します (ODBCDirect ワークスペースのみ)。値の取得および設定が可能です。 <strong><a href="querydefstateenum-enumeration-dao.md">QueryDefStateEnum</a></strong> クラスの定数を使用します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-properties-property-dao.md">Properties</a></strong></p></td>
<td><p>指定したオブジェクトの <strong><a href="properties-collection-dao.md">Properties</a></strong> コレクションを取得します。値の取得のみ可能です。  </p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-recordsaffected-property-dao.md">RecordsAffected</a></strong></p></td>
<td><p>最後に呼び出した <strong><a href="querydef-execute-method-dao.md">Execute</a></strong> メソッドの処理対象となったレコードの数を取得します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-returnsrecords-property-dao.md">ReturnsRecords</a></strong></p></td>
<td><p>外部データベースに対する SQL パススルー クエリでレコードを返すかどうかを示す値を設定または取得します (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-sql-property-dao.md">SQL</a></strong></p></td>
<td><p><strong><a href="querydef-object-dao.md">QueryDef</a></strong> オブジェクトが実行するクエリを定義する SQL ステートメントを設定または取得します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-stillexecuting-property-dao.md">StillExecuting</a></strong></p></td>
<td><p><strong>注</strong>: ODBCDirect ワークスペースは、Microsoft access 2013 ではサポートされていません。 Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</p>
<p>非同期操作 (つまり、 <a href="recordsetoptionenum-enumeration-dao.md">dbRunAsync</a> オプションを指定して呼び出したメソッド) の実行が完了したかどうかを示します (ODBCDirect ワークスペースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-type-property-dao.md">種類</a></strong></p></td>
<td><p>オブジェクトの操作の種類またはデータ型を示す値を設定または取得します。 読み取り専用<strong>整数</strong>です。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-updatable-property-dao.md">Updatable</a></strong></p></td>
<td><p>DAO オブジェクトを変更できるかどうかを示す値を取得します。値の取得のみ可能です。ブール型 ( <strong>Boolean</strong> ) の値を使用します。  </p></td>
</tr>
</tbody>
</table>

