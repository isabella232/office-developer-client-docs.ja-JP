---
title: Microsoft OLE DB Provider for ODBC
TOCTitle: Microsoft OLE DB Provider for ODBC
ms:assetid: c507567e-5ad1-b32a-f6ad-5ba2c39aa4c2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249964(v=office.15)
ms:contentKeyID: 48547602
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 2bc1d657796a35cc1e371fb302ca069d20befd86
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589373"
---
# <a name="microsoft-ole-db-provider-for-odbc"></a>Microsoft OLE DB Provider for ODBC

**適用先**: Access 2013、Office 2013

ADO または RDS のプログラマにとって、すべてのデータ ソースで OLE DB インターフェイスが公開され、ADO で直接データ ソースを呼び出すことができるのが理想的です。OLE DB インターフェイスを実装するデータベース ベンダーは増えていますが、まだこのインターフェイスを公開していないデータ ソースもあります。ただし、現在使用されている事実上すべての DBMS システムは、ODBC によるアクセスが可能です。

ODBC ドライバーは、Microsoft SQL Server、Microsoft Access (Microsoft Jet データベース エンジン)、および Microsoft FoxPro だけでなく、Oracle などの Microsoft 以外のデータベース製品を含めた、現在使用されているすべての主要 DBMS で使用できます。

ただし、Microsoft ODBC Provider を使用すると、ADO からすべての ODBC データ ソースに接続できます。このプロバイダーはフリースレッドであり、Unicode に対応しています。

このプロバイダーはトランザクションをサポートしていますが、DBMS エンジンの種類によって、サポートするトランザクションの種類が異なります。たとえば、Microsoft Access は 5 レベルまでのネストされたトランザクションをサポートします。

このプロバイダーは ADO の既定のプロバイダーであり、プロバイダーに依存するすべての ADO プロパティおよびメソッドをサポートします。

## <a name="connection-string-parameters"></a>接続文字列パラメーター

このプロバイダーに接続するには、[ConnectionString](connectionstring-property-ado.md) プロパティの **Provider=** 引数を次のように設定します。

```sql 
 
MSDASQL 
```

[Provider](provider-property-ado.md) プロパティを取得した場合も、この文字列が返されます。

## <a name="typical-connection-string"></a>標準的な接続文字列

このプロバイダーの標準的な接続文字列を次に示します。

```sql 
 
"Provider=MSDASQL;DSN=dsnName;UID=userName;PWD=userPassword;" 
```

この文字列は、次に示すキーワードで構成されています。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>キーワード</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Provider</strong></p></td>
<td><p>OLE DB Provider for ODBC を指定します。</p></td>
</tr>
<tr class="even">
<td><p><strong>DSN</strong></p></td>
<td><p>データ ソース名を指定します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>UID</strong></p></td>
<td><p>ユーザー名を指定します。</p></td>
</tr>
<tr class="even">
<td><p><strong>PWD</strong></p></td>
<td><p>ユーザー パスワードを指定します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>URL</strong></p></td>
<td><p>Web フォルダーに公開されているファイルまたはディレクトリの URL を指定します。</p></td>
</tr>
</tbody>
</table>


このプロバイダーは ADO の既定のプロバイダーであるため、接続文字列で **Provider=** パラメーターを省略すると、このプロバイダーへの接続の確立が試行されます。

このプロバイダーは、ADO で定義されたパラメーター以外に独自の接続パラメーターをサポートしません。ただし、ADO 以外の接続パラメーターが指定されている場合は、ODBC ドライバー マネージャーに渡します。

**Provider** パラメーターを省略できるので、同じデータ ソースに対して ODBC 接続文字列と同じ ADO 接続文字列を作成できます。ODBC 接続文字列を作成するときと同じパラメーター名 (**DRIVER=**、**DATABASE=**、**DSN=** など)、値、および構文を使用します。定義済みのデータ ソース名 (DSN) または FileDSN を指定してもしなくても接続できます。

**DSN または FileDSN を指定する場合の構文:**

`"[Provider=MSDASQL;] { DSN=name | FileDSN=filename } ; [DATABASE=database;] UID=user; PWD=password"`

**DSN 指定しない場合の構文 (DSN なしの接続):**

`"[Provider=MSDASQL;] DRIVER=driver; SERVER=server;DATABASE=database; UID=user; PWD=password"`

If you use a **DSN** or **FileDSN**, it must be defined through the ODBC Data Source Administrator in the Windows Control Panel. In Microsoft Windows 2000, the ODBC Administrator is located under Administrative Tools. In previous versions of Windows, the ODBC Administrator icon is named **32-bit ODBC** or simply **ODBC**.

**DSN** を設定する代わりに、"SQL Server" などの ODBC ドライバー (**DRIVER=**)、サーバー名 (**SERVER=**)、およびデータベース名 (**DATABASE=**) を指定することもできます。

ユーザー アカウント名 (**UID=**) と、そのユーザー アカウントのパスワード (**PWD=**) を、ODBC 固有のパラメーターまたは ADO で定義された標準的な *user* パラメーターと *password* パラメーターで指定できます。

DSN 定義 **には** 既にデータベースが指定されていますが、別のデータベースに接続する **DSN** に加えて、データベース パラメーターを指定できます。 DSN を使用する場合は、常に *データベース* パラメーターを含めるのが良 **い考えです**。 This will ensure that you connect to the proper database in the event that another user changed the default database parameter since you last checked the **DSN** definition.

## <a name="provider-specific-connection-properties"></a>プロバイダー固有の Connection のプロパティ

OLE DB Provider for ODBC は、**Connection** オブジェクトの [Properties](properties-collection-ado.md) コレクションにプロパティを追加します。次の表は、これらのプロパティの一覧で、かっこ内は対応する OLE DB プロパティ名です。

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
<td><p>アクセス可能な手順<br />
(KAGPROP_ACCESSIBLEPROCEDURES)</p></td>
<td><p>ユーザーがストアド プロシージャにアクセスできるかどうかを示します。</p></td>
</tr>
<tr class="even">
<td><p>アクセス可能なテーブル<br />
(KAGPROP_ACCESSIBLETABLES)</p></td>
<td><p>ユーザーがデータベースのテーブルに対して SELECT ステートメントを実行する権限を持つかどうかを示します。</p></td>
</tr>
<tr class="odd">
<td><p>Active ステートメント<br />
(KAGPROP_ACTIVESTATEMENTS)</p></td>
<td><p>ODBC ドライバーが 1 つの接続でサポートできるハンドル数を示します。</p></td>
</tr>
<tr class="even">
<td><p>ドライバー名<br />
(KAGPROP_DRIVERNAME)</p></td>
<td><p>ODBC ドライバーのファイル名を示します。</p></td>
</tr>
<tr class="odd">
<td><p>ドライバー ODBC バージョン<br />
(KAGPROP_DRIVERODBCVER)</p></td>
<td><p>このドライバーがサポートする ODBC のバージョンを示します。</p></td>
</tr>
<tr class="even">
<td><p>ファイルの使用法<br />
(KAGPROP_FILEUSAGE)</p></td>
<td><p>ドライバーがデータ ソース内のファイルを、テーブルとして扱うか、カタログとして扱うかを示します。</p></td>
</tr>
<tr class="odd">
<td><p>Like Escape Clause<br />
(KAGPROP_LIKEESCAPECLAUSE)</p></td>
<td><p>ドライバーが、WHERE 句の LIKE 述語でパーセント記号 (%) および下線記号 (_) のエスケープ文字を定義および使用できるかどうかを示します。</p></td>
</tr>
<tr class="even">
<td><p>グループ化の最大列数<br />
(KAGPROP_MAXCOLUMNSINGROUPBY)</p></td>
<td><p>SELECT ステートメントの GROUP BY 句に記述できる最大列数を示します。</p></td>
</tr>
<tr class="odd">
<td><p>インデックスの最大列数<br />
(KAGPROP_MAXCOLUMNSININDEX)</p></td>
<td><p>インデックスに格納できる最大列数を示します。</p></td>
</tr>
<tr class="even">
<td><p>順序による最大列数<br />
(KAGPROP_MAXCOLUMNSINORDERBY)</p></td>
<td><p>SELECT ステートメントの ORDER BY 句に記述できる最大列数を示します。</p></td>
</tr>
<tr class="odd">
<td><p>Select の最大列数<br />
(KAGPROP_MAXCOLUMNSINSELECT)</p></td>
<td><p>SELECT ステートメントの SELECT 部分に記述できる最大列数を示します。</p></td>
</tr>
<tr class="even">
<td><p>テーブル内の最大列数<br />
(KAGPROP_MAXCOLUMNSINTABLE)</p></td>
<td><p>テーブルの最大列数を示します。</p></td>
</tr>
<tr class="odd">
<td><p>数値を処理する関数<br />
(KAGPROP_NUMERICFUNCTIONS)</p></td>
<td><p>ODBC ドライバーがサポートする数値関数を示します。関数名とこのビットマスクで使用される関連付けられた値の一覧については、ODBC マニュアルの「Appendix E: Scalar Functions」 (英語) を参照してください。</p></td>
</tr>
<tr class="even">
<td><p>外部結合機能<br />
(KAGPROP_OJCAPABILITY)</p></td>
<td><p>プロバイダーがサポートする OUTER JOIN の種類を示します。</p></td>
</tr>
<tr class="odd">
<td><p>外部結合<br />
(KAGPROP_OUTERJOINS)</p></td>
<td><p>プロバイダーが OUTER JOIN をサポートするかどうかを示します。</p></td>
</tr>
<tr class="even">
<td><p>特殊文字<br />
(KAGPROP_SPECIALCHARACTERS)</p></td>
<td><p>ODBC ドライバーで特別な意味を持つ文字を示します。</p></td>
</tr>
<tr class="odd">
<td><p>ストアド プロシージャ<br />
(KAGPROP_PROCEDURES)</p></td>
<td><p>この ODBC ドライバーでストアド プロシージャを使用できるかどうかを示します。</p></td>
</tr>
<tr class="even">
<td><p>文字列を処理する関数<br />
(KAGPROP_STRINGFUNCTIONS)</p></td>
<td><p>ODBC ドライバーがサポートする文字列関数を示します。関数名とこのビットマスクで使用される関連付けられた値の一覧については、ODBC マニュアルの「Appendix E: Scalar Functions」を参照してください。</p></td>
</tr>
<tr class="odd">
<td><p>システム関数<br />
(KAGPROP_SYSTEMFUNCTIONS)</p></td>
<td><p>ODBC ドライバーがサポートするシステム関数を示します。関数名とこのビットマスクで使用される関連付けられた値の一覧については、ODBC マニュアルの「Appendix E: Scalar Functions」を参照してください。</p></td>
</tr>
<tr class="even">
<td><p>時刻/日付関数<br />
(KAGPROP_TIMEDATEFUNCTIONS)</p></td>
<td><p>ODBC ドライバーがサポートする時刻/日付関数を示します。関数名とこのビットマスクで使用される関連付けられた値の一覧については、ODBC マニュアルの「Appendix E: Scalar Functions」を参照してください。</p></td>
</tr>
<tr class="odd">
<td><p>SQL文法のサポート<br />
(KAGPROP_ODBCSQLCONFORMANCE)</p></td>
<td><p>ODBC ドライバーがサポートする SQL 文法を示します。</p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a>プロバイダー固有の Recordset および Command のプロパティ

OLE DB Provider for ODBC は、**Recordset** オブジェクトと **Command** オブジェクトの **Properties** コレクションにプロパティを追加します。次の表は、これらのプロパティの一覧で、かっこ内は対応する OLE DB プロパティ名です。

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
<td><p>クエリ ベースの更新/削除/挿入<br />
(KAGPROP_QUERYBASEDUPDATES)</p></td>
<td><p>SQL クエリを使用して更新、削除、および挿入を実行できるかどうかを示します。</p></td>
</tr>
<tr class="even">
<td><p>ODBC 同時実行の種類<br />
(KAGPROP_CONCURRENCY)</p></td>
<td><p>2 人のユーザーがデータ ソースの同じデータに同時にアクセスしようとしたときに発生する問題を減少させるための方法を示します。</p></td>
</tr>
<tr class="odd">
<td><p>カーソルの BLOB アクセシビリティForward-Onlyする<br />
(KAGPROP_BLOBSONFOCURSOR)</p></td>
<td><p>前方のみのカーソルの使用時に BLOB <strong>Fields</strong> にアクセスできるかどうかを示します。</p></td>
</tr>
<tr class="even">
<td><p>QBU WHERE 句に SQL_FLOAT、SQL_DOUBLE、および SQL_REAL を含める<br />
(KAGPROP_INCLUDENONEXACT)</p></td>
<td><p>SQL_FLOAT、SQL_DOUBLE、および SQL_REAL の値を QBU WHERE 句に含めることができるかどうかを示します。</p></td>
</tr>
<tr class="odd">
<td><p>挿入後の最後の行の位置<br />
(KAGPROP_POSITIONONNEWROW)</p></td>
<td><p>新規レコードをテーブルに挿入した後、テーブルの最後の行が現在の行になるかどうかを示します。</p></td>
</tr>
<tr class="even">
<td><p>IRowsetChangeExtInfo<br />
(KAGPROP_IROWSETCHANGEEXTINFO)</p></td>
<td><p><strong>IRowsetChange</strong> インターフェイスが拡張情報を提供するかどうかを示します。</p></td>
</tr>
<tr class="odd">
<td><p>ODBC カーソルの種類<br />
(KAGPROP_CURSOR)</p></td>
<td><p><strong>Recordset</strong> で使用されるカーソルの種類を示します。</p></td>
</tr>
<tr class="even">
<td><p>マーシャリングできる Rowset を生成する<br />
(KAGPROP_MARSHALLABLE)</p></td>
<td><p>ODBC ドライバーがマーシャリング可能なレコードセットを生成することを示します。</p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a>コマンド テキスト

[Command](command-object-ado.md) オブジェクトの使用方法は、データ ソースおよび受け付けられるクエリまたはコマンド ステートメントの種類によって大きく異なります。

ODBC には、ストアド プロシージャを呼び出すための独自の構文があります。**Command** オブジェクトの [CommandText](commandtext-property-ado.md) プロパティ、[Connection](connection-object-ado.md) オブジェクトの **Execute** メソッドの *CommandText* 引数、または [Recordset](recordset-object-ado.md) オブジェクトの **Open** メソッドの *Source* 引数の場合は、次の構文で文字列を渡します。

`"{ [ ? = ] call procedure [ ( ? [, ? [ ,  ]] ) ] }"`

**?** はそれぞれ [Parameters](parameters-collection-ado.md) コレクションのオブジェクトを参照します。最初の **?** は **Parameters**(0) を参照し、次の **?** は **Parameters**(1) を参照し、以下同様に続きます。

パラメーターの参照は省略可能で、ストアド プロシージャの構造に依存します。パラメーターを定義していないストアド プロシージャを呼び出す場合の構文は、次のようになります。

`"{ call procedure }"`

2 つのクエリ パラメーターを持つ場合は、次のようになります。

`"{ call procedure ( ?, ? ) }"`

ストアド プロシージャが値を返す場合、戻り値は別のパラメーターとして扱われます。クエリ パラメーターがなく、戻り値がある場合は、次のようになります。

`"{ ? = call procedure }"`

戻り値があり、2 つのクエリ パラメーターがある場合は、次のようになります。

`"{ ? = call procedure ( ?, ? ) }"`

## <a name="recordset-behavior"></a>Recordset の動作

次の表は、このプロバイダーで開かれた **Recordset** オブジェクトで利用可能な標準の ADO メソッドと ADO プロパティの一覧です。

プロバイダーの構成による **Recordset** の動作の詳細については、 [Supports](supports-method-ado.md) メソッドを実行し、 **Recordset** の **Properties** コレクションを列挙して、プロバイダー固有の動的プロパティが存在するかどうかを確認してください。

標準的な ADO **Recordset** のプロパティの利用可能性は、次のとおりです。

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p>プロパティ</p></th>
<th><p>ForwardOnly</p></th>
<th><p>Dynamic</p></th>
<th><p>Keyset</p></th>
<th><p>静的</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="absolutepage-property-ado.md">AbsolutePage</a></p></td>
<td><p>使用不可</p></td>
<td><p>使用不可</p></td>
<td><p>読み取り/書き込み</p></td>
<td><p>読み取り/書き込み</p></td>
</tr>
<tr class="even">
<td><p><a href="absoluteposition-property-ado.md">AbsolutePosition</a></p></td>
<td><p>使用不可</p></td>
<td><p>使用不可</p></td>
<td><p>読み取り/書き込み</p></td>
<td><p>読み取り/書き込み</p></td>
</tr>
<tr class="odd">
<td><p><a href="activeconnection-property-ado.md">ActiveConnection</a></p></td>
<td><p>読み取り/書き込み</p></td>
<td><p>読み取り/書き込み</p></td>
<td><p>読み取り/書き込み</p></td>
<td><p>読み取り/書き込み</p></td>
</tr>
<tr class="even">
<td><p><a href="bof-eof-properties-ado.md">BOF</a></p></td>
<td><p>読み取り専用</p></td>
<td><p>読み取り専用</p></td>
<td><p>読み取り専用</p></td>
<td><p>読み取り専用</p></td>
</tr>
<tr class="odd">
<td><p><a href="bookmark-property-ado.md">Bookmark</a></p></td>
<td><p>使用不可</p></td>
<td><p>使用不可</p></td>
<td><p>読み取り/書き込み</p></td>
<td><p>読み取り/書き込み</p></td>
</tr>
<tr class="even">
<td><p><a href="cachesize-property-ado.md">CacheSize</a></p></td>
<td><p>読み取り/書き込み</p></td>
<td><p>読み取り/書き込み</p></td>
<td><p>読み取り/書き込み</p></td>
<td><p>読み取り/書き込み</p></td>
</tr>
<tr class="odd">
<td><p><a href="cursorlocation-property-ado.md">CursorLocation</a></p></td>
<td><p>読み取り/書き込み</p></td>
<td><p>読み取り/書き込み</p></td>
<td><p>読み取り/書き込み</p></td>
<td><p>読み取り/書き込み</p></td>
</tr>
<tr class="even">
<td><p><a href="cursortype-property-ado.md">CursorType</a></p></td>
<td><p>読み取り/書き込み</p></td>
<td><p>読み取り/書き込み</p></td>
<td><p>読み取り/書き込み</p></td>
<td><p>読み取り/書き込み</p></td>
</tr>
<tr class="odd">
<td><p><a href="editmode-property-ado.md">EditMode</a></p></td>
<td><p>読み取り専用</p></td>
<td><p>読み取り専用</p></td>
<td><p>読み取り専用</p></td>
<td><p>読み取り専用</p></td>
</tr>
<tr class="even">
<td><p><a href="filter-property-ado.md">Filter</a></p></td>
<td><p>読み取り/書き込み</p></td>
<td><p>読み取り/書き込み</p></td>
<td><p>読み取り/書き込み</p></td>
<td><p>読み取り/書き込み</p></td>
</tr>
<tr class="odd">
<td><p><a href="locktype-property-ado.md">LockType</a></p></td>
<td><p>読み取り/書き込み</p></td>
<td><p>読み取り/書き込み</p></td>
<td><p>読み取り/書き込み</p></td>
<td><p>読み取り/書き込み</p></td>
</tr>
<tr class="even">
<td><p><a href="marshaloptions-property-ado.md">MarshalOptions</a></p></td>
<td><p>読み取り/書き込み</p></td>
<td><p>読み取り/書き込み</p></td>
<td><p>読み取り/書き込み</p></td>
<td><p>読み取り/書き込み</p></td>
</tr>
<tr class="odd">
<td><p><a href="maxrecords-property-ado.md">MaxRecords</a></p></td>
<td><p>読み取り/書き込み</p></td>
<td><p>読み取り/書き込み</p></td>
<td><p>読み取り/書き込み</p></td>
<td><p>読み取り/書き込み</p></td>
</tr>
<tr class="even">
<td><p><a href="pagecount-property-ado.md">PageCount</a></p></td>
<td><p>読み取り/書き込み</p></td>
<td><p>利用不可</p></td>
<td><p>読み取り専用</p></td>
<td><p>読み取り専用</p></td>
</tr>
<tr class="odd">
<td><p><a href="pagesize-property-ado.md">PageSize</a></p></td>
<td><p>読み取り/書き込み</p></td>
<td><p>読み取り/書き込み</p></td>
<td><p>読み取り/書き込み</p></td>
<td><p>読み取り/書き込み</p></td>
</tr>
<tr class="even">
<td><p><a href="recordcount-property-ado.md">RecordCount</a></p></td>
<td><p>読み取り/書き込み</p></td>
<td><p>利用不可</p></td>
<td><p>読み取り専用</p></td>
<td><p>読み取り専用</p></td>
</tr>
<tr class="odd">
<td><p><a href="source-property-ado-recordset.md">Source</a></p></td>
<td><p>読み取り/書き込み</p></td>
<td><p>読み取り/書き込み</p></td>
<td><p>読み取り/書き込み</p></td>
<td><p>読み取り/書き込み</p></td>
</tr>
<tr class="even">
<td><p><a href="state-property-ado.md">State</a></p></td>
<td><p>読み取り専用</p></td>
<td><p>読み取り専用</p></td>
<td><p>読み取り専用</p></td>
<td><p>読み取り専用</p></td>
</tr>
<tr class="odd">
<td><p><a href="status-property-ado-recordset.md">状態</a></p></td>
<td><p>読み取り専用</p></td>
<td><p>読み取り専用</p></td>
<td><p>読み取り専用</p></td>
<td><p>読み取り専用</p></td>
</tr>
</tbody>
</table>


バージョン 1.0 の Microsoft OLE DB Provider for ODBC で ADO を使用する場合、[AbsolutePosition](absoluteposition-property-ado.md) プロパティと [AbsolutePage](absolutepage-property-ado.md) プロパティは値の設定のみ可能です。

標準的な ADO **Recordset** のメソッドの利用可能性は、次のとおりです。

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Method</p></th>
<th><p>ForwardOnly</p></th>
<th><p>Dynamic</p></th>
<th><p>Keyset</p></th>
<th><p>静的</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="addnew-method-ado.md">AddNew</a></p></td>
<td><p>はい</p></td>
<td><p>はい</p></td>
<td><p>はい</p></td>
<td><p>必要</p></td>
</tr>
<tr class="even">
<td><p><a href="cancel-method-ado.md">Cancel</a></p></td>
<td><p>はい</p></td>
<td><p>はい</p></td>
<td><p>はい</p></td>
<td><p>必要</p></td>
</tr>
<tr class="odd">
<td><p><a href="cancelbatch-method-ado.md">CancelBatch</a></p></td>
<td><p>はい</p></td>
<td><p>はい</p></td>
<td><p>はい</p></td>
<td><p>必要</p></td>
</tr>
<tr class="even">
<td><p><a href="cancelupdate-method-ado.md">CancelUpdate </a></p></td>
<td><p>はい</p></td>
<td><p>はい</p></td>
<td><p>はい</p></td>
<td><p>必要</p></td>
</tr>
<tr class="odd">
<td><p><a href="clone-method-ado.md">Clone</a></p></td>
<td><p>いいえ</p></td>
<td><p>いいえ</p></td>
<td><p>はい</p></td>
<td><p>必要</p></td>
</tr>
<tr class="even">
<td><p><a href="close-method-ado.md">Close</a></p></td>
<td><p>はい</p></td>
<td><p>はい</p></td>
<td><p>はい</p></td>
<td><p>必要</p></td>
</tr>
<tr class="odd">
<td><p><a href="delete-method-ado-recordset.md">削除</a></p></td>
<td><p>はい</p></td>
<td><p>はい</p></td>
<td><p>はい</p></td>
<td><p>必要</p></td>
</tr>
<tr class="even">
<td><p><a href="getrows-method-ado.md">GetRows</a></p></td>
<td><p>はい</p></td>
<td><p>はい</p></td>
<td><p>はい</p></td>
<td><p>必要</p></td>
</tr>
<tr class="odd">
<td><p><a href="move-method-ado.md">Move</a></p></td>
<td><p>はい</p></td>
<td><p>はい</p></td>
<td><p>はい</p></td>
<td><p>必要</p></td>
</tr>
<tr class="even">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></p></td>
<td><p>はい</p></td>
<td><p>はい</p></td>
<td><p>はい</p></td>
<td><p>必要</p></td>
</tr>
<tr class="odd">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></p></td>
<td><p>いいえ</p></td>
<td><p>はい</p></td>
<td><p>はい</p></td>
<td><p>必要</p></td>
</tr>
<tr class="even">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></p></td>
<td><p>はい</p></td>
<td><p>はい</p></td>
<td><p>はい</p></td>
<td><p>必要</p></td>
</tr>
<tr class="odd">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></p></td>
<td><p>いいえ</p></td>
<td><p>はい</p></td>
<td><p>はい</p></td>
<td><p>必要</p></td>
</tr>
<tr class="even">
<td><p><a href="nextrecordset-method-ado.md">NextRecordset</a>*</p></td>
<td><p>はい</p></td>
<td><p>はい</p></td>
<td><p>はい</p></td>
<td><p>必要</p></td>
</tr>
<tr class="odd">
<td><p><a href="open-method-ado-recordset.md">開く</a></p></td>
<td><p>はい</p></td>
<td><p>はい</p></td>
<td><p>はい</p></td>
<td><p>必要</p></td>
</tr>
<tr class="even">
<td><p><a href="requery-method-ado.md">Requery</a></p></td>
<td><p>はい</p></td>
<td><p>はい</p></td>
<td><p>はい</p></td>
<td><p>必要</p></td>
</tr>
<tr class="odd">
<td><p><a href="resync-method-ado.md">再同期</a></p></td>
<td><p>いいえ</p></td>
<td><p>いいえ</p></td>
<td><p>はい</p></td>
<td><p>必要</p></td>
</tr>
<tr class="even">
<td><p><a href="supports-method-ado.md">サポート</a></p></td>
<td><p>はい</p></td>
<td><p>はい</p></td>
<td><p>はい</p></td>
<td><p>必要</p></td>
</tr>
<tr class="odd">
<td><p><a href="update-method-ado.md">Update</a></p></td>
<td><p>はい</p></td>
<td><p>はい</p></td>
<td><p>はい</p></td>
<td><p>必要</p></td>
</tr>
<tr class="even">
<td><p><a href="updatebatch-method-ado.md">UpdateBatch</a></p></td>
<td><p>はい</p></td>
<td><p>はい</p></td>
<td><p>はい</p></td>
<td><p>必要</p></td>
</tr>
</tbody>
</table>


\*Microsoft Access データベースではサポートされません。

## <a name="dynamic-properties"></a>動的プロパティ

Microsoft OLE DB Provider for ODBC は、開かれていない [Connection](connection-object-ado.md) オブジェクト、[Recordset](recordset-object-ado.md) オブジェクト、および [Command](command-object-ado.md) オブジェクトの **Properties** コレクションに動的プロパティを挿入します。

以下の表は、各動的プロパティの ADO 名と OLE DB 名の対応表です。 「OLE DB プログラマ リファレンス」では、「説明」欄に ADO プロパティ名が示されています。プロパティの詳細については、「OLE DB プログラマ リファレンス」を参照してください。OLE DB プロパティ名をキーワードとして検索するか、「付録 C: プロパティ表」を参照してください。

## <a name="connection-dynamic-properties"></a>Connection の動的プロパティ

次に示すプロパティが **Connection** オブジェクトの **Properties** コレクションに追加されます。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>ADO プロパティ名</p></th>
<th><p>OLE DB プロパティ名</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Active Sessions</p></td>
<td><p>DBPROP_ACTIVESESSIONS</p></td>
</tr>
<tr class="even">
<td><p>Asynchable Abort</p></td>
<td><p>DBPROP_ASYNCTXNABORT</p></td>
</tr>
<tr class="odd">
<td><p>Asynchable Commit</p></td>
<td><p>DBPROP_ASYNCTNXCOMMIT</p></td>
</tr>
<tr class="even">
<td><p>Autocommit Isolation Levels</p></td>
<td><p>DBPROP_SESS_AUTOCOMMITISOLEVELS</p></td>
</tr>
<tr class="odd">
<td><p>Catalog Location</p></td>
<td><p>DBPROP_CATALOGLOCATION</p></td>
</tr>
<tr class="even">
<td><p>Catalog Term</p></td>
<td><p>DBPROP_CATALOGTERM</p></td>
</tr>
<tr class="odd">
<td><p>Column Definition</p></td>
<td><p>DBPROP_COLUMNDEFINITION</p></td>
</tr>
<tr class="even">
<td><p>Connect Timeout</p></td>
<td><p>DBPROP_INIT_TIMEOUT</p></td>
</tr>
<tr class="odd">
<td><p>Current Catalog</p></td>
<td><p>DBPROP_CURRENTCATALOG</p></td>
</tr>
<tr class="even">
<td><p>Data Source</p></td>
<td><p>DBPROP_INIT_DATASOURCE</p></td>
</tr>
<tr class="odd">
<td><p>Data Source Name</p></td>
<td><p>DBPROP_DATASOURCENAME</p></td>
</tr>
<tr class="even">
<td><p>Data Source Object Threading Model</p></td>
<td><p>DBPROP_DSOTHREADMODEL</p></td>
</tr>
<tr class="odd">
<td><p>DBMS Name</p></td>
<td><p>DBPROP_DBMSNAME</p></td>
</tr>
<tr class="even">
<td><p>DBMS Version</p></td>
<td><p>DBPROP_DBMSVER</p></td>
</tr>
<tr class="odd">
<td><p>Extended Properties</p></td>
<td><p>DBPROP_INIT_PROVIDERSTRING</p></td>
</tr>
<tr class="even">
<td><p>GROUP BY Support</p></td>
<td><p>DBPROP_GROUPBY</p></td>
</tr>
<tr class="odd">
<td><p>Heterogeneous Table Support</p></td>
<td><p>DBPROP_HETEROGENEOUSTABLES</p></td>
</tr>
<tr class="even">
<td><p>Identifier Case Sensitivity</p></td>
<td><p>DBPROP_IDENTIFIERCASE</p></td>
</tr>
<tr class="odd">
<td><p>Initial Catalog</p></td>
<td><p>DBPROP_INIT_CATALOG</p></td>
</tr>
<tr class="even">
<td><p>Isolation Levels</p></td>
<td><p>DBPROP_SUPPORTEDTXNISOLEVELS</p></td>
</tr>
<tr class="odd">
<td><p>Isolation Retention</p></td>
<td><p>DBPROP_SUPPORTEDTXNISORETAIN</p></td>
</tr>
<tr class="even">
<td><p>Locale Identifier</p></td>
<td><p>DBPROP_INIT_LCID</p></td>
</tr>
<tr class="odd">
<td><p>Location</p></td>
<td><p>DBPROP_INIT_LOCATION</p></td>
</tr>
<tr class="even">
<td><p>Maximum Index Size</p></td>
<td><p>DBPROP_MAXINDEXSIZE</p></td>
</tr>
<tr class="odd">
<td><p>Maximum Row Size</p></td>
<td><p>DBPROP_MAXROWSIZE</p></td>
</tr>
<tr class="even">
<td><p>Maximum Row Size Includes BLOB</p></td>
<td><p>DBPROP_MAXROWSIZEINCLUDESBLOB</p></td>
</tr>
<tr class="odd">
<td><p>Maximum Tables in SELECT</p></td>
<td><p>DBPROP_MAXTABLESINSELECT</p></td>
</tr>
<tr class="even">
<td><p>Mode</p></td>
<td><p>DBPROP_INIT_MODE</p></td>
</tr>
<tr class="odd">
<td><p>Multiple Parameter Sets</p></td>
<td><p>DBPROP_MULTIPLEPARAMSETS</p></td>
</tr>
<tr class="even">
<td><p>Multiple Results</p></td>
<td><p>DBPROP_MULTIPLERESULTS</p></td>
</tr>
<tr class="odd">
<td><p>Multiple Storage Objects</p></td>
<td><p>DBPROP_MULTIPLESTORAGEOBJECTS</p></td>
</tr>
<tr class="even">
<td><p>Multi-Table Update</p></td>
<td><p>DBPROP_MULTITABLEUPDATE</p></td>
</tr>
<tr class="odd">
<td><p>NULL Collation Order</p></td>
<td><p>DBPROP_NULLCOLLATION</p></td>
</tr>
<tr class="even">
<td><p>NULL Concatenation Behavior</p></td>
<td><p>DBPROP_CONCATNULLBEHAVIOR</p></td>
</tr>
<tr class="odd">
<td><p>OLE DB Services</p></td>
<td><p>DBPROP_INIT_OLEDBSERVICES</p></td>
</tr>
<tr class="even">
<td><p>OLE DB Version</p></td>
<td><p>DBPROP_PROVIDEROLEDBVER</p></td>
</tr>
<tr class="odd">
<td><p>OLE Object Support</p></td>
<td><p>DBPROP_OLEOBJECTS</p></td>
</tr>
<tr class="even">
<td><p>Open Rowset Support</p></td>
<td><p>DBPROP_OPENROWSETSUPPORT</p></td>
</tr>
<tr class="odd">
<td><p>ORDER BY Columns in Select List</p></td>
<td><p>DBPROP_ORDERBYCOLUMNSINSELECT</p></td>
</tr>
<tr class="even">
<td><p>Output Parameter Availability</p></td>
<td><p>DBPROP_OUTPUTPARAMETERAVAILABILITY</p></td>
</tr>
<tr class="odd">
<td><p>Password</p></td>
<td><p>DBPROP_AUTH_PASSWORD</p></td>
</tr>
<tr class="even">
<td><p>Pass By Ref Accessors</p></td>
<td><p>DBPROP_BYREFACCESSORS</p></td>
</tr>
<tr class="odd">
<td><p>Persist Security Info</p></td>
<td><p>DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</p></td>
</tr>
<tr class="even">
<td><p>Persistent ID Type</p></td>
<td><p>DBPROP_PERSISTENTIDTYPE</p></td>
</tr>
<tr class="odd">
<td><p>Prepare Abort Behavior</p></td>
<td><p>DBPROP_PREPAREABORTBEHAVIOR</p></td>
</tr>
<tr class="even">
<td><p>Prepare Commit Behavior</p></td>
<td><p>DBPROP_PREPARECOMMITBEHAVIOR</p></td>
</tr>
<tr class="odd">
<td><p>Procedure Term</p></td>
<td><p>DBPROP_PROCEDURETERM</p></td>
</tr>
<tr class="even">
<td><p>Prompt</p></td>
<td><p>DBPROP_INIT_PROMPT</p></td>
</tr>
<tr class="odd">
<td><p>Provider Friendly Name</p></td>
<td><p>DBPROP_PROVIDERFRIENDLYNAME</p></td>
</tr>
<tr class="even">
<td><p>Provider Name</p></td>
<td><p>DBPROP_PROVIDERFILENAME</p></td>
</tr>
<tr class="odd">
<td><p>Provider Version</p></td>
<td><p>DBPROP_PROVIDERVER</p></td>
</tr>
<tr class="even">
<td><p>Read-Only Data Source</p></td>
<td><p>DBPROP_DATASOURCEREADONLY</p></td>
</tr>
<tr class="odd">
<td><p>Rowset Conversions on Command</p></td>
<td><p>DBPROP_ROWSETCONVERSIONSONCOMMAND</p></td>
</tr>
<tr class="even">
<td><p>Schema Term</p></td>
<td><p>DBPROP_SCHEMATERM</p></td>
</tr>
<tr class="odd">
<td><p>Schema Usage</p></td>
<td><p>DBPROP_SCHEMAUSAGE</p></td>
</tr>
<tr class="even">
<td><p>SQL Support</p></td>
<td><p>DBPROP_SQLSUPPORT</p></td>
</tr>
<tr class="odd">
<td><p>Structured Storage</p></td>
<td><p>DBPROP_STRUCTUREDSTORAGE</p></td>
</tr>
<tr class="even">
<td><p>Subquery Support</p></td>
<td><p>DBPROP_SUBQUERIES</p></td>
</tr>
<tr class="odd">
<td><p>Table Term</p></td>
<td><p>DBPROP_TABLETERM</p></td>
</tr>
<tr class="even">
<td><p>Transaction DDL</p></td>
<td><p>DBPROP_SUPPORTEDTXNDDL</p></td>
</tr>
<tr class="odd">
<td><p>User ID</p></td>
<td><p>DBPROP_AUTH_USERID</p></td>
</tr>
<tr class="even">
<td><p>User Name</p></td>
<td><p>DBPROP_USERNAME</p></td>
</tr>
<tr class="odd">
<td><p>Window Handle</p></td>
<td><p>DBPROP_INIT_HWND</p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a>Recordset の動的プロパティ

次に示すプロパティが **Recordset** オブジェクトの **Properties** コレクションに追加されます。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>ADO プロパティ名</p></th>
<th><p>OLE DB プロパティ名</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Access Order</p></td>
<td><p>DBPROP_ACCESSORDER</p></td>
</tr>
<tr class="even">
<td><p>Blocking Storage Objects</p></td>
<td><p>DBPROP_BLOCKINGSTORAGEOBJECTS</p></td>
</tr>
<tr class="odd">
<td><p>Bookmark Type</p></td>
<td><p>DBPROP_BOOKMARKTYPE</p></td>
</tr>
<tr class="even">
<td><p>Bookmarkable</p></td>
<td><p>DBPROP_IROWSETLOCATE</p></td>
</tr>
<tr class="odd">
<td><p>Change Inserted Rows</p></td>
<td><p>DBPROP_CHANGEINSERTEDROWS</p></td>
</tr>
<tr class="even">
<td><p>Column Privileges</p></td>
<td><p>DBPROP_COLUMNRESTRICT</p></td>
</tr>
<tr class="odd">
<td><p>Column Set Notification</p></td>
<td><p>DBPROP_NOTIFYCOLUMNSET</p></td>
</tr>
<tr class="even">
<td><p>Delay Storage Object Updates</p></td>
<td><p>DBPROP_DELAYSTORAGEOBJECTS</p></td>
</tr>
<tr class="odd">
<td><p>Fetch Backwards</p></td>
<td><p>DBPROP_CANFETCHBACKWARDS</p></td>
</tr>
<tr class="even">
<td><p>Hold Rows</p></td>
<td><p>DBPROP_CANHOLDROWS</p></td>
</tr>
<tr class="odd">
<td><p>IAccessor</p></td>
<td><p>DBPROP_IAccessor</p></td>
</tr>
<tr class="even">
<td><p>IColumnsInfo</p></td>
<td><p>DBPROP_IColumnsInfo</p></td>
</tr>
<tr class="odd">
<td><p>IColumnsRowset</p></td>
<td><p>DBPROP_IColumnsRowset</p></td>
</tr>
<tr class="even">
<td><p>IConnectionPointContainer</p></td>
<td><p>DBPROP_IConnectionPointContainer</p></td>
</tr>
<tr class="odd">
<td><p>IConvertType</p></td>
<td><p>DBPROP_IConvertType</p></td>
</tr>
<tr class="even">
<td><p>Immobile Rows</p></td>
<td><p>DBPROP_IMMOBILEROWS</p></td>
</tr>
<tr class="odd">
<td><p>IRowset</p></td>
<td><p>DBPROP_IRowset</p></td>
</tr>
<tr class="even">
<td><p>IRowsetChange</p></td>
<td><p>DBPROP_IRowsetChange</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetIdentity</p></td>
<td><p>DBPROP_IRowsetIdentity</p></td>
</tr>
<tr class="even">
<td><p>IRowsetInfo</p></td>
<td><p>DBPROP_IRowsetInfo</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetLocate</p></td>
<td><p>DBPROP_IRowsetLocate</p></td>
</tr>
<tr class="even">
<td><p>IRowsetResynch</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>IRowsetUpdate</p></td>
<td><p>DBPROP_IRowsetUpdate</p></td>
</tr>
<tr class="even">
<td><p>ISequentialStream</p></td>
<td><p>DBPROP_ISequentialStream</p></td>
</tr>
<tr class="odd">
<td><p>ISupportErrorInfo</p></td>
<td><p>DBPROP_ISupportErrorInfo</p></td>
</tr>
<tr class="even">
<td><p>Literal Bookmarks</p></td>
<td><p>DBPROP_LITERALBOOKMARKS</p></td>
</tr>
<tr class="odd">
<td><p>Literal Row Identity</p></td>
<td><p>DBPROP_LITERALIDENTITY</p></td>
</tr>
<tr class="even">
<td><p>Maximum Open Rows</p></td>
<td><p>DBPROP_MAXOPENROWS</p></td>
</tr>
<tr class="odd">
<td><p>Maximum Pending Rows</p></td>
<td><p>DBPROP_MAXPENDINGROWS</p></td>
</tr>
<tr class="even">
<td><p>Maximum Rows</p></td>
<td><p>DBPROP_MAXROWS</p></td>
</tr>
<tr class="odd">
<td><p>Notification Granularity</p></td>
<td><p>DBPROP_NOTIFICATIONGRANULARITY</p></td>
</tr>
<tr class="even">
<td><p>Notification Phases</p></td>
<td><p>DBPROP_NOTIFICATIONPHASES</p></td>
</tr>
<tr class="odd">
<td><p>Objects Transacted</p></td>
<td><p>DBPROP_TRANSACTEDOBJECT</p></td>
</tr>
<tr class="even">
<td><p>Own Changes Visible</p></td>
<td><p>DBPROP_OWNUPDATEDELETE</p></td>
</tr>
<tr class="odd">
<td><p>Own Inserts Visible</p></td>
<td><p>DBPROP_OWNINSERT</p></td>
</tr>
<tr class="even">
<td><p>Preserve on Abort</p></td>
<td><p>DBPROP_ABORTPRESERVE</p></td>
</tr>
<tr class="odd">
<td><p>Preserve on Commit</p></td>
<td><p>DBPROP_COMMITPRESERVE</p></td>
</tr>
<tr class="even">
<td><p>Quick Restart</p></td>
<td><p>DBPROP_QUICKRESTART</p></td>
</tr>
<tr class="odd">
<td><p>Reentrant Events</p></td>
<td><p>DBPROP_REENTRANTEVENTS</p></td>
</tr>
<tr class="even">
<td><p>Remove Deleted Rows</p></td>
<td><p>DBPROP_REMOVEDELETED</p></td>
</tr>
<tr class="odd">
<td><p>Report Multiple Changes</p></td>
<td><p>DBPROP_REPORTMULTIPLECHANGES</p></td>
</tr>
<tr class="even">
<td><p>Return Pending Inserts</p></td>
<td><p>DBPROP_RETURNPENDINGINSERTS</p></td>
</tr>
<tr class="odd">
<td><p>Row Delete Notification</p></td>
<td><p>DBPROP_NOTIFYROWDELETE</p></td>
</tr>
<tr class="even">
<td><p>Row First Change Notification</p></td>
<td><p>DBPROP_NOTIFYROWFIRSTCHANGE</p></td>
</tr>
<tr class="odd">
<td><p>Row Insert Notification</p></td>
<td><p>DBPROP_NOTIFYROWINSERT</p></td>
</tr>
<tr class="even">
<td><p>Row Privileges</p></td>
<td><p>DBPROP_ROWRESTRICT</p></td>
</tr>
<tr class="odd">
<td><p>Row Resynchronization Notification</p></td>
<td><p>DBPROP_NOTIFYROWRESYNCH</p></td>
</tr>
<tr class="even">
<td><p>Row Threading Model</p></td>
<td><p>DBPROP_ROWTHREADMODEL</p></td>
</tr>
<tr class="odd">
<td><p>Row Undo Change Notification</p></td>
<td><p>DBPROP_NOTIFYROWUNDOCHANGE</p></td>
</tr>
<tr class="even">
<td><p>Row Undo Delete Notification</p></td>
<td><p>DBPROP_NOTIFYROWUNDODELETE</p></td>
</tr>
<tr class="odd">
<td><p>Row Undo Insert Notification</p></td>
<td><p>DBPROP_NOTIFYROWUNDOINSERT</p></td>
</tr>
<tr class="even">
<td><p>Row Update Notification</p></td>
<td><p>DBPROP_NOTIFYROWUPDATE</p></td>
</tr>
<tr class="odd">
<td><p>Rowset Fetch Position Change Notification</p></td>
<td><p>DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</p></td>
</tr>
<tr class="even">
<td><p>Rowset Release Notification</p></td>
<td><p>DBPROP_NOTIFYROWSETRELEASE</p></td>
</tr>
<tr class="odd">
<td><p>Scroll Backwards</p></td>
<td><p>DBPROP_CANSCROLLBACKWARDS</p></td>
</tr>
<tr class="even">
<td><p>Skip Deleted Bookmarks</p></td>
<td><p>DBPROP_BOOKMARKSKIPPED</p></td>
</tr>
<tr class="odd">
<td><p>Strong Row Identity</p></td>
<td><p>DBPROP_STRONGITDENTITY</p></td>
</tr>
<tr class="even">
<td><p>Unique Rows</p></td>
<td><p>DBPROP_UNIQUEROWS</p></td>
</tr>
<tr class="odd">
<td><p>Updatability</p></td>
<td><p>DBPROP_UPDATABILITY</p></td>
</tr>
<tr class="even">
<td><p>Use Bookmarks</p></td>
<td><p>DBPROP_BOOKMARKS</p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a>Command の動的プロパティ

次に示すプロパティが **Command** オブジェクトの **Properties** コレクションに追加されます。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>ADO プロパティ名</p></th>
<th><p>OLE DB プロパティ名</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Access Order</p></td>
<td><p>DBPROP_ACCESSORDER</p></td>
</tr>
<tr class="even">
<td><p>Blocking Storage Objects</p></td>
<td><p>DBPROP_BLOCKINGSTORAGEOBJECTS</p></td>
</tr>
<tr class="odd">
<td><p>Bookmark Type</p></td>
<td><p>DBPROP_BOOKMARKTYPE</p></td>
</tr>
<tr class="even">
<td><p>Bookmarkable</p></td>
<td><p>DBPROP_IROWSETLOCATE</p></td>
</tr>
<tr class="odd">
<td><p>Change Inserted Rows</p></td>
<td><p>DBPROP_CHANGEINSERTEDROWS</p></td>
</tr>
<tr class="even">
<td><p>Column Privileges</p></td>
<td><p>DBPROP_COLUMNRESTRICT</p></td>
</tr>
<tr class="odd">
<td><p>Column Set Notification</p></td>
<td><p>DBPROP_NOTIFYCOLUMNSET</p></td>
</tr>
<tr class="even">
<td><p>Delay Storage Object Updates</p></td>
<td><p>DBPROP_DELAYSTORAGEOBJECTS</p></td>
</tr>
<tr class="odd">
<td><p>Fetch Backwards</p></td>
<td><p>DBPROP_CANFETCHBACKWARDS</p></td>
</tr>
<tr class="even">
<td><p>Hold Rows</p></td>
<td><p>DBPROP_CANHOLDROWS</p></td>
</tr>
<tr class="odd">
<td><p>IAccessor</p></td>
<td><p>DBPROP_IAccessor</p></td>
</tr>
<tr class="even">
<td><p>IColumnsInfo</p></td>
<td><p>DBPROP_IColumnsInfo</p></td>
</tr>
<tr class="odd">
<td><p>IColumnsRowset</p></td>
<td><p>DBPROP_IColumnsRowset</p></td>
</tr>
<tr class="even">
<td><p>IConnectionPointContainer</p></td>
<td><p>DBPROP_IConnectionPointContainer</p></td>
</tr>
<tr class="odd">
<td><p>IConvertType</p></td>
<td><p>DBPROP_IConvertType</p></td>
</tr>
<tr class="even">
<td><p>Immobile Rows</p></td>
<td><p>DBPROP_IMMOBILEROWS</p></td>
</tr>
<tr class="odd">
<td><p>IRowset</p></td>
<td><p>DBPROP_IRowset</p></td>
</tr>
<tr class="even">
<td><p>IRowsetChange</p></td>
<td><p>DBPROP_IRowsetChange</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetIdentity</p></td>
<td><p>DBPROP_IRowsetIdentity</p></td>
</tr>
<tr class="even">
<td><p>IRowsetInfo</p></td>
<td><p>DBPROP_IRowsetInfo</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetLocate</p></td>
<td><p>DBPROP_IRowsetLocate</p></td>
</tr>
<tr class="even">
<td><p>IRowsetResynch</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>IRowsetUpdate</p></td>
<td><p>DBPROP_IRowsetUpdate</p></td>
</tr>
<tr class="even">
<td><p>ISequentialStream</p></td>
<td><p>DBPROP_ISequentialStream</p></td>
</tr>
<tr class="odd">
<td><p>ISupportErrorInfo</p></td>
<td><p>DBPROP_ISupportErrorInfo</p></td>
</tr>
<tr class="even">
<td><p>Literal Bookmarks</p></td>
<td><p>DBPROP_LITERALBOOKMARKS</p></td>
</tr>
<tr class="odd">
<td><p>Literal Row Identity</p></td>
<td><p>DBPROP_LITERALIDENTITY</p></td>
</tr>
<tr class="even">
<td><p>Maximum Open Rows</p></td>
<td><p>DBPROP_MAXOPENROWS</p></td>
</tr>
<tr class="odd">
<td><p>Maximum Pending Rows</p></td>
<td><p>DBPROP_MAXPENDINGROWS</p></td>
</tr>
<tr class="even">
<td><p>Maximum Rows</p></td>
<td><p>DBPROP_MAXROWS</p></td>
</tr>
<tr class="odd">
<td><p>Notification Granularity</p></td>
<td><p>DBPROP_NOTIFICATIONGRANULARITY</p></td>
</tr>
<tr class="even">
<td><p>Notification Phases</p></td>
<td><p>DBPROP_NOTIFICATIONPHASES</p></td>
</tr>
<tr class="odd">
<td><p>Objects Transacted</p></td>
<td><p>DBPROP_TRANSACTEDOBJECT</p></td>
</tr>
<tr class="even">
<td><p>Own Changes Visible</p></td>
<td><p>DBPROP_OWNUPDATEDELETE</p></td>
</tr>
<tr class="odd">
<td><p>Own Inserts Visible</p></td>
<td><p>DBPROP_OWNINSERT</p></td>
</tr>
<tr class="even">
<td><p>Preserve on Abort</p></td>
<td><p>DBPROP_ABORTPRESERVE</p></td>
</tr>
<tr class="odd">
<td><p>Preserve on Commit</p></td>
<td><p>DBPROP_COMMITPRESERVE</p></td>
</tr>
<tr class="even">
<td><p>Quick Restart</p></td>
<td><p>DBPROP_QUICKRESTART</p></td>
</tr>
<tr class="odd">
<td><p>Reentrant Events</p></td>
<td><p>DBPROP_REENTRANTEVENTS</p></td>
</tr>
<tr class="even">
<td><p>Remove Deleted Rows</p></td>
<td><p>DBPROP_REMOVEDELETED</p></td>
</tr>
<tr class="odd">
<td><p>Report Multiple Changes</p></td>
<td><p>DBPROP_REPORTMULTIPLECHANGES</p></td>
</tr>
<tr class="even">
<td><p>Return Pending Inserts</p></td>
<td><p>DBPROP_RETURNPENDINGINSERTS</p></td>
</tr>
<tr class="odd">
<td><p>Row Delete Notification</p></td>
<td><p>DBPROP_NOTIFYROWDELETE</p></td>
</tr>
<tr class="even">
<td><p>Row First Change Notification</p></td>
<td><p>DBPROP_NOTIFYROWFIRSTCHANGE</p></td>
</tr>
<tr class="odd">
<td><p>Row Insert Notification</p></td>
<td><p>DBPROP_NOTIFYROWINSERT</p></td>
</tr>
<tr class="even">
<td><p>Row Privileges</p></td>
<td><p>DBPROP_ROWRESTRICT</p></td>
</tr>
<tr class="odd">
<td><p>Row Resynchronization Notification</p></td>
<td><p>DBPROP_NOTIFYROWRESYNCH</p></td>
</tr>
<tr class="even">
<td><p>Row Threading Model</p></td>
<td><p>DBPROP_ROWTHREADMODEL</p></td>
</tr>
<tr class="odd">
<td><p>Row Undo Change Notification</p></td>
<td><p>DBPROP_NOTIFYROWUNDOCHANGE</p></td>
</tr>
<tr class="even">
<td><p>Row Undo Delete Notification</p></td>
<td><p>DBPROP_NOTIFYROWUNDODELETE</p></td>
</tr>
<tr class="odd">
<td><p>Row Undo Insert Notification</p></td>
<td><p>DBPROP_NOTIFYROWUNDOINSERT</p></td>
</tr>
<tr class="even">
<td><p>Row Update Notification</p></td>
<td><p>DBPROP_NOTIFYROWUPDATE</p></td>
</tr>
<tr class="odd">
<td><p>Rowset Fetch Position Change Notification</p></td>
<td><p>DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</p></td>
</tr>
<tr class="even">
<td><p>Rowset Release Notification</p></td>
<td><p>DBPROP_NOTIFYROWSETRELEASE</p></td>
</tr>
<tr class="odd">
<td><p>Scroll Backwards</p></td>
<td><p>DBPROP_CANSCROLLBACKWARDS</p></td>
</tr>
<tr class="even">
<td><p>Skip Deleted Bookmarks</p></td>
<td><p>DBPROP_BOOKMARKSKIP</p></td>
</tr>
<tr class="odd">
<td><p>Strong Row Identity</p></td>
<td><p>DBPROP_STRONGIDENTITY</p></td>
</tr>
<tr class="even">
<td><p>Updatability</p></td>
<td><p>DBPROP_UPDATABILITY</p></td>
</tr>
<tr class="odd">
<td><p>Use Bookmarks</p></td>
<td><p>DBPROP_BOOKMARKS</p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>関連項目

MICROSOFT OLE DB Provider for ODBC に関する具体的な実装および機能情報の詳細については [、OLE DB](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) プログラマ ガイドを参照するか、データ プラットフォーム開発者センター を [参照してください](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017)。

