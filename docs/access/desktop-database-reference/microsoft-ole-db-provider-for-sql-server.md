---
title: Microsoft OLE DB Provider for SQL Server
TOCTitle: Microsoft OLE DB Provider for SQL Server
ms:assetid: 0ffdea03-1a76-499b-f649-423f6b3c13d7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248868(v=office.15)
ms:contentKeyID: 48543282
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c4faa664ed9001c1c06906f58c7d873faf75a5d0
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705107"
---
# <a name="microsoft-ole-db-provider-for-sql-server"></a><span data-ttu-id="938bc-102">Microsoft OLE DB Provider for SQL Server</span><span class="sxs-lookup"><span data-stu-id="938bc-102">Microsoft OLE DB Provider for SQL Server</span></span>


<span data-ttu-id="938bc-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="938bc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="938bc-104">Microsoft OLE DB Provider for SQL Server (SQLOLEDB) を使用すると、ADO から Microsoft SQL Server にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="938bc-104">The Microsoft OLE DB Provider for SQL Server, SQLOLEDB, allows ADO to access Microsoft SQL Server.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="938bc-105">接続文字列のパラメーター</span><span class="sxs-lookup"><span data-stu-id="938bc-105">Connection String Parameters</span></span>

<span data-ttu-id="938bc-106">このプロバイダーに接続するには、 [ConnectionString](connectionstring-property-ado.md)プロパティを*プロバイダー*の引数を設定します。</span><span class="sxs-lookup"><span data-stu-id="938bc-106">To connect to this provider, set the *Provider* argument to the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```sql 
 
SQLOLEDB 
```

<span data-ttu-id="938bc-107">この値は、[Provider](provider-property-ado.md) プロパティを使用して設定または取得することもできます。</span><span class="sxs-lookup"><span data-stu-id="938bc-107">This value can also be set or read using the [Provider](provider-property-ado.md) property.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="938bc-108">標準的な接続文字列</span><span class="sxs-lookup"><span data-stu-id="938bc-108">Typical Connection String</span></span>

<span data-ttu-id="938bc-109">このプロバイダーの標準的な接続文字列を次に示します。</span><span class="sxs-lookup"><span data-stu-id="938bc-109">A typical connection string for this provider is:</span></span>

```sql 
 
"Provider=SQLOLEDB;Data Source=serverName;" 
Initial Catalog=databaseName; 
User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="938bc-110">この文字列は、次に示すキーワードで構成されています。</span><span class="sxs-lookup"><span data-stu-id="938bc-110">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="938bc-111">キーワード</span><span class="sxs-lookup"><span data-stu-id="938bc-111">Keyword</span></span></p></th>
<th><p><span data-ttu-id="938bc-112">説明</span><span class="sxs-lookup"><span data-stu-id="938bc-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="938bc-113"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="938bc-113"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="938bc-114">OLE DB Provider for SQL Server を指定します。</span><span class="sxs-lookup"><span data-stu-id="938bc-114">Specifies the OLE DB Provider for SQL Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-115"><strong>Data Source</strong> または <strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="938bc-115"><strong>Data Source</strong> or <strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="938bc-116">サーバー名を指定します。</span><span class="sxs-lookup"><span data-stu-id="938bc-116">Specifies the name of a server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-117"><strong>Initial Catalog</strong> または <strong>Database</strong></span><span class="sxs-lookup"><span data-stu-id="938bc-117"><strong>Initial Catalog</strong> or <strong>Database</strong></span></span></p></td>
<td><p><span data-ttu-id="938bc-118">サーバー上のデータベース名を指定します。</span><span class="sxs-lookup"><span data-stu-id="938bc-118">Specifies the name of a database on the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-119"><strong>User ID</strong> または <strong>uid</strong></span><span class="sxs-lookup"><span data-stu-id="938bc-119"><strong>User ID</strong> or <strong>uid</strong></span></span></p></td>
<td><p><span data-ttu-id="938bc-120">SQL Server 認証用のユーザー名を指定します。</span><span class="sxs-lookup"><span data-stu-id="938bc-120">Specifies the user name (for SQL Server Authentication).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-121"><strong>Password</strong> または <strong>pwd</strong></span><span class="sxs-lookup"><span data-stu-id="938bc-121"><strong>Password</strong> or <strong>pwd</strong></span></span></p></td>
<td><p><span data-ttu-id="938bc-122">SQL Server 認証用のユーザー パスワードを指定します。</span><span class="sxs-lookup"><span data-stu-id="938bc-122">Specifies the user password (for SQL Server Authentication).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a><span data-ttu-id="938bc-123">プロバイダー固有の接続パラメーター</span><span class="sxs-lookup"><span data-stu-id="938bc-123">Provider-Specific Connection Parameters</span></span>

<span data-ttu-id="938bc-p101">このプロバイダーは、ADO で定義されたパラメーターに加えて、プロバイダー固有の接続パラメーターをサポートしています。ADO の接続プロパティと同様に、これらのプロバイダー固有のプロパティは [Connection](properties-collection-ado.md) の [Properties](connection-object-ado.md) コレクションで設定することも、 **ConnectionString** の一部として設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="938bc-p101">The provider supports several provider-specific connection parameters in addition to those defined by ADO. As with the ADO connection properties, these provider-specific properties can be set via the [Properties](properties-collection-ado.md) collection of a [Connection](connection-object-ado.md) or can be set as part of the **ConnectionString**.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="938bc-126">パラメーター</span><span class="sxs-lookup"><span data-stu-id="938bc-126">Parameter</span></span></p></th>
<th><p><span data-ttu-id="938bc-127">説明</span><span class="sxs-lookup"><span data-stu-id="938bc-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="938bc-128">度</span><span class="sxs-lookup"><span data-stu-id="938bc-128">Trusted_Connection</span></span></p></td>
<td><p><span data-ttu-id="938bc-p102">ユーザー認証モードを示します。このパラメーターは <strong>Yes</strong> または <strong>No</strong> に設定できます。既定値は <strong>No</strong> です。このプロパティが <strong>Yes</strong> に設定されている場合、SQLOLEDB は Microsoft Windows NT 認証モードを使用して、<strong>Location</strong> プロパティおよび <a href="datasource-property-ado.md">Datasource</a> プロパティの値で指定されている SQL Server データベースへのユーザー アクセスを許可します。このプロパティが <strong>No</strong> に設定されている場合、SQLOLEDB は混合モードを使用して SQL Server データベースへのユーザー アクセスを許可します。SQL Server のログイン名およびパスワードは、<strong>User Id</strong> プロパティと <strong>Password</strong> プロパティで指定します。</span><span class="sxs-lookup"><span data-stu-id="938bc-p102">Indicates the user authentication mode. This can be set to <strong>Yes</strong> or <strong>No</strong>. The default value is <strong>No</strong>. If this property is set to <strong>Yes</strong>, then SQLOLEDB uses Microsoft Windows NT Authentication Mode to authorize user access to the SQL Server database specified by the <strong>Location</strong> and <a href="datasource-property-ado.md">Datasource</a> property values. If this property is set to <strong>No</strong>, then SQLOLEDB uses Mixed Mode to authorize user access to the SQL Server database. The SQL Server login and password are specified in the <strong>User Id</strong> and <strong>Password</strong> properties.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-135">Current Language</span><span class="sxs-lookup"><span data-stu-id="938bc-135">Current Language</span></span></p></td>
<td><p><span data-ttu-id="938bc-p103">SQL Server の言語名を示します。システム メッセージやフォーマットで使用する言語を識別します。指定する言語は SQL Server にインストールされている必要があり、インストールされていない場合は接続を開くことができません。</span><span class="sxs-lookup"><span data-stu-id="938bc-p103">Indicates a SQL Server language name. Identifies the language used for system message selection and formatting. The language must be installed on the SQL Server, otherwise opening the connection will fail.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-139">Network Address</span><span class="sxs-lookup"><span data-stu-id="938bc-139">Network Address</span></span></p></td>
<td><p><span data-ttu-id="938bc-140"><strong>Location</strong> プロパティで指定された SQL Server のネットワーク アドレスを示します。</span><span class="sxs-lookup"><span data-stu-id="938bc-140">Indicates the network address of the SQL Server specified by the <strong>Location</strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-141">Network Library</span><span class="sxs-lookup"><span data-stu-id="938bc-141">Network Library</span></span></p></td>
<td><p><span data-ttu-id="938bc-142">SQL Server と通信するために使用するネットワーク ライブラリ (ダイナミック リンク ライブラリ) の名前を示します。</span><span class="sxs-lookup"><span data-stu-id="938bc-142">Indicates the name of the network library (dynamic-link libraries) used to communicate with the SQL Server.</span></span> <span data-ttu-id="938bc-143">パスまたはファイル名の拡張子が .dll の名前は含まれません。</span><span class="sxs-lookup"><span data-stu-id="938bc-143">The name should not include the path or the .dll file name extension.</span></span> <span data-ttu-id="938bc-144">既定値は、SQL Server クライアントの構成によって提供されます。</span><span class="sxs-lookup"><span data-stu-id="938bc-144">The default is provided by the SQL Server client configuration.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-145">Use Procedure for Prepare</span><span class="sxs-lookup"><span data-stu-id="938bc-145">Use Procedure for Prepare</span></span></p></td>
<td><p><span data-ttu-id="938bc-146"><strong>Prepared</strong> プロパティによって Commands を準備しているときに、SQL Server が一時的なストアド プロシージャを作成するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="938bc-146">Determines whether SQL Server creates temporary stored procedures when Commands are prepared (by the <strong>Prepared</strong> property).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-147">Auto Translate</span><span class="sxs-lookup"><span data-stu-id="938bc-147">Auto Translate</span></span></p></td>
<td><p><span data-ttu-id="938bc-p105">OEM/ANSI 文字変換を実行するかどうかを示します。このプロパティは、<strong>True</strong> または <strong>False</strong> に設定できます。既定値は <strong>True</strong> です。このプロパティが <strong>True</strong> に設定されている場合、マルチバイト文字の文字列を SQL Server から取得するとき、または SQL Server に送信するときに、SQLOLEDB は OEM/ANSI 文字変換を実行します。このプロパティが <strong>False</strong> に設定されている場合、SQLOLEDB はマルチバイト文字の文字列に対して OEM/ANSI 文字変換を実行しません。</span><span class="sxs-lookup"><span data-stu-id="938bc-p105">Indicates whether OEM/ANSI characters are converted. This property can be set to <strong>True</strong> or <strong>False</strong>. The default value is <strong>True</strong>. If this property is set to <strong>True</strong>, then SQLOLEDB performs OEM/ANSI character conversion when multi-byte character strings are retrieved from, or sent to, the SQL Server. If this property is set to <strong>False</strong>, then SQLOLEDB does not perform OEM/ANSI character conversion on multi-byte character string data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-153">Packet Size</span><span class="sxs-lookup"><span data-stu-id="938bc-153">Packet Size</span></span></p></td>
<td><p><span data-ttu-id="938bc-p106">ネットワーク パケット サイズをバイト単位で示します。このプロパティの値は、512 ～ 32767 の範囲である必要があります。SQLOLEDB の既定のネットワーク パケット サイズは 4096 です。</span><span class="sxs-lookup"><span data-stu-id="938bc-p106">Indicates a network packet size in bytes. The packet size property value must be between 512 and 32767. The default SQLOLEDB network packet size is 4096.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-157">Application Name</span><span class="sxs-lookup"><span data-stu-id="938bc-157">Application Name</span></span></p></td>
<td><p><span data-ttu-id="938bc-158">クライアント アプリケーション名を示します。</span><span class="sxs-lookup"><span data-stu-id="938bc-158">Indicates the client application name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-159">Workstation ID</span><span class="sxs-lookup"><span data-stu-id="938bc-159">Workstation ID</span></span></p></td>
<td><p><span data-ttu-id="938bc-160">ワークステーションを識別する文字列です。</span><span class="sxs-lookup"><span data-stu-id="938bc-160">A string identifying the workstation.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-object-usage"></a><span data-ttu-id="938bc-161">Command オブジェクトの使用方法</span><span class="sxs-lookup"><span data-stu-id="938bc-161">Command Object Usage</span></span>

<span data-ttu-id="938bc-p107">SQLOLEDB は、ODBC、ANSI、および SQL Server 固有の Transact-SQL が混在する構文を、有効な構文として受け付けます。たとえば、次の SQL ステートメントでは、ODBC SQL エスケープ シーケンスを使用して文字列関数 LCASE を指定しています。</span><span class="sxs-lookup"><span data-stu-id="938bc-p107">SQLOLEDB accepts an amalgam of ODBC, ANSI, and SQL Server-specific Transact-SQL as valid syntax. For example, the following SQL statement uses an ODBC SQL escape sequence to specify the LCASE string function:</span></span>

```sql 
 
SELECT customerid={fn LCASE(CustomerID)} FROM Customers 
```

<span data-ttu-id="938bc-p108">LCASE は大文字をすべて小文字に変換した文字列を返します。ANSI SQL 文字列関数 LOWER は同じ処理を実行するので、前に示した ODBC によるステートメントを ANSI で指定すると、次のような SQL ステートメントになります。</span><span class="sxs-lookup"><span data-stu-id="938bc-p108">LCASE returns a character string, converting all uppercase characters to their lowercase equivalents. The ANSI SQL string function LOWER performs the same operation, so the following SQL statement is an ANSI equivalent to the ODBC statement presented above:</span></span>

```sql
 
SELECT customerid=LOWER(CustomerID) FROM Customers 
```

<span data-ttu-id="938bc-166">SQLOLEDB は、コマンドのテキストとして指定されている場合、いずれの形式のステートメントも正しく処理します。</span><span class="sxs-lookup"><span data-stu-id="938bc-166">SQLOLEDB successfully processes either form of the statement when specified as text for a command.</span></span>

## <a name="stored-procedures"></a><span data-ttu-id="938bc-167">ストアド プロシージャ</span><span class="sxs-lookup"><span data-stu-id="938bc-167">Stored Procedures</span></span>

<span data-ttu-id="938bc-p109">SQLOLEDB コマンドを使用して SQL Server ストアド プロシージャを実行するときは、コマンド テキストで ODBC プロシージャ コール エスケープ シーケンスを使用します。SQLOLEDB は、SQL Server のリモート プロシージャ コールのメカニズムを使用してコマンド処理を最適化します。たとえば、次の ODBC SQL ステートメントは、その次の Transact-SQL 形式のステートメントよりもコマンド テキストとして適しています。</span><span class="sxs-lookup"><span data-stu-id="938bc-p109">When executing a SQL Server stored procedure using a SQLOLEDB command, use the ODBC procedure call escape sequence in the command text. SQLOLEDB then uses the remote procedure call mechanism of SQL Server to optimize command processing. For example, the following ODBC SQL statement is the preferred command text over the Transact-SQL form:</span></span>

## <a name="odbc-sql"></a><span data-ttu-id="938bc-171">ODBC SQL</span><span class="sxs-lookup"><span data-stu-id="938bc-171">ODBC SQL</span></span>

```sql 
 
{call SalesByCategory('Produce', '1995')} 
```

## <a name="transact-sql"></a><span data-ttu-id="938bc-172">Transact-SQL</span><span class="sxs-lookup"><span data-stu-id="938bc-172">Transact-SQL</span></span>

```sql 
 
EXECUTE SalesByCategory 'Produce', '1995' 
```

## <a name="recordset-behavior"></a><span data-ttu-id="938bc-173">Recordset の動作</span><span class="sxs-lookup"><span data-stu-id="938bc-173">Recordset Behavior</span></span>

<span data-ttu-id="938bc-p110">SQLOLEDB では、SQL Server のカーソルを使用して、複数のコマンドによって生成される複数の結果をサポートすることはできません。コンシューマーが SQL Server カーソルのサポートを必要とするレコードセットを要求した場合、使用したコマンド テキストの結果として複数のレコードセットが生成されると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="938bc-p110">SQLOLEDB cannot use SQL Server cursors to support the multiple-result generated by many commands. If a consumer requests a recordset requiring SQL Server cursor support, an error occurs if the command text used generates more than a single recordset as its result.</span></span>

<span data-ttu-id="938bc-p111">スクロール可能な SQLOLEDB レコードセットは、SQL Server カーソルによってサポートされています。SQL Server では、データベースの他のユーザーによって変更される可能性のあるカーソルに制限を設けています。具体的には、一部のカーソルでは行を並べ替えることができず、SQL ORDER BY 句を含むコマンドを使用してレコードセットを作成できないことがあります。</span><span class="sxs-lookup"><span data-stu-id="938bc-p111">Scrollable SQLOLEDB recordsets are supported by SQL Server cursors. SQL Server imposes limitations on cursors that are sensitive to changes made by other users of the database. Specifically, the rows in some cursors cannot be ordered, and attempting to create a recordset using a command containing an SQL ORDER BY clause can fail.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="938bc-179">動的プロパティ</span><span class="sxs-lookup"><span data-stu-id="938bc-179">Dynamic Properties</span></span>

<span data-ttu-id="938bc-180">Microsoft OLE DB Provider for SQL Server は、開かれていない **Connection** オブジェクト、 [Recordset](connection-object-ado.md) オブジェクト、および [Command](recordset-object-ado.md) オブジェクトの [Properties](command-object-ado.md) コレクションに動的プロパティを挿入します。</span><span class="sxs-lookup"><span data-stu-id="938bc-180">The Microsoft OLE DB Provider for SQL Server inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="938bc-p112">以下の表は、各動的プロパティの ADO 名と OLE DB 名の対応表です。 「OLE DB プログラマ リファレンス」では、「説明」欄に ADO プロパティ名が示されています。プロパティの詳細については、「OLE DB プログラマ リファレンス」を参照してください。OLE DB プロパティ名をキーワードとして検索するか、「付録 C: プロパティ表」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="938bc-p112">The following tables are a cross-index of the ADO and OLE DB names for each dynamic property. The OLE DB Programmer's Reference refers to an ADO property name by the term "Description." You can find more information about these properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="938bc-185">Connection の動的プロパティ</span><span class="sxs-lookup"><span data-stu-id="938bc-185">Connection Dynamic Properties</span></span>

<span data-ttu-id="938bc-186">次に示すプロパティが **Connection** オブジェクトの **Properties** コレクションに追加されます。</span><span class="sxs-lookup"><span data-stu-id="938bc-186">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="938bc-187">ADO プロパティ名</span><span class="sxs-lookup"><span data-stu-id="938bc-187">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="938bc-188">OLE DB プロパティ名</span><span class="sxs-lookup"><span data-stu-id="938bc-188">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="938bc-189">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="938bc-189">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="938bc-190">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="938bc-190">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-191">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="938bc-191">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="938bc-192">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="938bc-192">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-193">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="938bc-193">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="938bc-194">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="938bc-194">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-195">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="938bc-195">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="938bc-196">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="938bc-196">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-197">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="938bc-197">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="938bc-198">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="938bc-198">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-199">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="938bc-199">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="938bc-200">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="938bc-200">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-201">Column Definition</span><span class="sxs-lookup"><span data-stu-id="938bc-201">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="938bc-202">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="938bc-202">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-203">Connect Timeout</span><span class="sxs-lookup"><span data-stu-id="938bc-203">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="938bc-204">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="938bc-204">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-205">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="938bc-205">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="938bc-206">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="938bc-206">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-207">Data Source</span><span class="sxs-lookup"><span data-stu-id="938bc-207">Data Source</span></span></p></td>
<td><p><span data-ttu-id="938bc-208">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="938bc-208">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-209">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="938bc-209">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="938bc-210">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="938bc-210">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-211">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="938bc-211">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="938bc-212">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="938bc-212">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-213">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="938bc-213">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="938bc-214">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="938bc-214">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-215">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="938bc-215">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="938bc-216">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="938bc-216">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-217">Extended Properties</span><span class="sxs-lookup"><span data-stu-id="938bc-217">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="938bc-218">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="938bc-218">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-219">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="938bc-219">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="938bc-220">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="938bc-220">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-221">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="938bc-221">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="938bc-222">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="938bc-222">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-223">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="938bc-223">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="938bc-224">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="938bc-224">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-225">Initial Catalog</span><span class="sxs-lookup"><span data-stu-id="938bc-225">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="938bc-226">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="938bc-226">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-227">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="938bc-227">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="938bc-228">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="938bc-228">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-229">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="938bc-229">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="938bc-230">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="938bc-230">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-231">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="938bc-231">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="938bc-232">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="938bc-232">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-233">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="938bc-233">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="938bc-234">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="938bc-234">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-235">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="938bc-235">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="938bc-236">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="938bc-236">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-237">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="938bc-237">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="938bc-238">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="938bc-238">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-239">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="938bc-239">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="938bc-240">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="938bc-240">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-241">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="938bc-241">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="938bc-242">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="938bc-242">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-243">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="938bc-243">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="938bc-244">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="938bc-244">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-245">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="938bc-245">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="938bc-246">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="938bc-246">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-247">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="938bc-247">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="938bc-248">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="938bc-248">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-249">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="938bc-249">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="938bc-250">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="938bc-250">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-251">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="938bc-251">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="938bc-252">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="938bc-252">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-253">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="938bc-253">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="938bc-254">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="938bc-254">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-255">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="938bc-255">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="938bc-256">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="938bc-256">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-257">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="938bc-257">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="938bc-258">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="938bc-258">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-259">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="938bc-259">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="938bc-260">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="938bc-260">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-261">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="938bc-261">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="938bc-262">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="938bc-262">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-263">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="938bc-263">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="938bc-264">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="938bc-264">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-265">Password</span><span class="sxs-lookup"><span data-stu-id="938bc-265">Password</span></span></p></td>
<td><p><span data-ttu-id="938bc-266">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="938bc-266">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-267">Persist Security Info</span><span class="sxs-lookup"><span data-stu-id="938bc-267">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="938bc-268">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="938bc-268">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-269">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="938bc-269">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="938bc-270">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="938bc-270">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-271">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="938bc-271">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="938bc-272">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="938bc-272">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-273">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="938bc-273">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="938bc-274">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="938bc-274">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-275">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="938bc-275">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="938bc-276">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="938bc-276">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-277">Prompt</span><span class="sxs-lookup"><span data-stu-id="938bc-277">Prompt</span></span></p></td>
<td><p><span data-ttu-id="938bc-278">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="938bc-278">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-279">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="938bc-279">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="938bc-280">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="938bc-280">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-281">Provider Name</span><span class="sxs-lookup"><span data-stu-id="938bc-281">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="938bc-282">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="938bc-282">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-283">Provider Version</span><span class="sxs-lookup"><span data-stu-id="938bc-283">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="938bc-284">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="938bc-284">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-285">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="938bc-285">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="938bc-286">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="938bc-286">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-287">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="938bc-287">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="938bc-288">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="938bc-288">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-289">Schema Term</span><span class="sxs-lookup"><span data-stu-id="938bc-289">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="938bc-290">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="938bc-290">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-291">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="938bc-291">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="938bc-292">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="938bc-292">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-293">SQL Support</span><span class="sxs-lookup"><span data-stu-id="938bc-293">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="938bc-294">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="938bc-294">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-295">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="938bc-295">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="938bc-296">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="938bc-296">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-297">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="938bc-297">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="938bc-298">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="938bc-298">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-299">Table Term</span><span class="sxs-lookup"><span data-stu-id="938bc-299">Table Term</span></span></p></td>
<td><p><span data-ttu-id="938bc-300">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="938bc-300">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-301">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="938bc-301">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="938bc-302">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="938bc-302">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-303">User ID</span><span class="sxs-lookup"><span data-stu-id="938bc-303">User ID</span></span></p></td>
<td><p><span data-ttu-id="938bc-304">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="938bc-304">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-305">User Name</span><span class="sxs-lookup"><span data-stu-id="938bc-305">User Name</span></span></p></td>
<td><p><span data-ttu-id="938bc-306">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="938bc-306">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-307">Window Handle</span><span class="sxs-lookup"><span data-stu-id="938bc-307">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="938bc-308">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="938bc-308">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="938bc-309">Recordset の動的プロパティ</span><span class="sxs-lookup"><span data-stu-id="938bc-309">Recordset Dynamic Properties</span></span>

<span data-ttu-id="938bc-310">次に示すプロパティが **Recordset** オブジェクトの **Properties** コレクションに追加されます。</span><span class="sxs-lookup"><span data-stu-id="938bc-310">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="938bc-311">ADO プロパティ名</span><span class="sxs-lookup"><span data-stu-id="938bc-311">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="938bc-312">OLE DB プロパティ名</span><span class="sxs-lookup"><span data-stu-id="938bc-312">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="938bc-313">Access Order</span><span class="sxs-lookup"><span data-stu-id="938bc-313">Access Order</span></span></p></td>
<td><p><span data-ttu-id="938bc-314">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="938bc-314">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-315">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="938bc-315">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="938bc-316">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="938bc-316">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-317">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="938bc-317">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="938bc-318">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="938bc-318">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-319">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="938bc-319">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="938bc-320">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="938bc-320">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-321">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="938bc-321">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="938bc-322">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="938bc-322">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-323">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="938bc-323">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="938bc-324">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="938bc-324">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-325">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="938bc-325">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="938bc-326">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="938bc-326">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-327">Command Time Out</span><span class="sxs-lookup"><span data-stu-id="938bc-327">Command Time Out</span></span></p></td>
<td><p><span data-ttu-id="938bc-328">DBPROP_COMMANDTIMEOUT</span><span class="sxs-lookup"><span data-stu-id="938bc-328">DBPROP_COMMANDTIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-329">Defer Column</span><span class="sxs-lookup"><span data-stu-id="938bc-329">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="938bc-330">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="938bc-330">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-331">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="938bc-331">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="938bc-332">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="938bc-332">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-333">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="938bc-333">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="938bc-334">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="938bc-334">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-335">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="938bc-335">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="938bc-336">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="938bc-336">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-337">IAccessor</span><span class="sxs-lookup"><span data-stu-id="938bc-337">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="938bc-338">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="938bc-338">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-339">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="938bc-339">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="938bc-340">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="938bc-340">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-341">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="938bc-341">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="938bc-342">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="938bc-342">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-343">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="938bc-343">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="938bc-344">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="938bc-344">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-345">IConvertType</span><span class="sxs-lookup"><span data-stu-id="938bc-345">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="938bc-346">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="938bc-346">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-347">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="938bc-347">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="938bc-348">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="938bc-348">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-349">IRowset</span><span class="sxs-lookup"><span data-stu-id="938bc-349">IRowset</span></span></p></td>
<td><p><span data-ttu-id="938bc-350">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="938bc-350">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-351">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="938bc-351">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="938bc-352">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="938bc-352">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-353">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="938bc-353">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="938bc-354">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="938bc-354">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-355">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="938bc-355">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="938bc-356">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="938bc-356">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-357">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="938bc-357">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="938bc-358">DBPROP_IRowsestLocate</span><span class="sxs-lookup"><span data-stu-id="938bc-358">DBPROP_IRowsestLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-359">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="938bc-359">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-360">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="938bc-360">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="938bc-361">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="938bc-361">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-362">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="938bc-362">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="938bc-363">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="938bc-363">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-364">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="938bc-364">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="938bc-365">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="938bc-365">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-366">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="938bc-366">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="938bc-367">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="938bc-367">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-368">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="938bc-368">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="938bc-369">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="938bc-369">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-370">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="938bc-370">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="938bc-371">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="938bc-371">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-372">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="938bc-372">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="938bc-373">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="938bc-373">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-374">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="938bc-374">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="938bc-375">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="938bc-375">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-376">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="938bc-376">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="938bc-377">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="938bc-377">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-378">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="938bc-378">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="938bc-379">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="938bc-379">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-380">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="938bc-380">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="938bc-381">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="938bc-381">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-382">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="938bc-382">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="938bc-383">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="938bc-383">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-384">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="938bc-384">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="938bc-385">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="938bc-385">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-386">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="938bc-386">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="938bc-387">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="938bc-387">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-388">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="938bc-388">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="938bc-389">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="938bc-389">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-390">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="938bc-390">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="938bc-391">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="938bc-391">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-392">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="938bc-392">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="938bc-393">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="938bc-393">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-394">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="938bc-394">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="938bc-395">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="938bc-395">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-396">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="938bc-396">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="938bc-397">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="938bc-397">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-398">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="938bc-398">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="938bc-399">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="938bc-399">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-400">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="938bc-400">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="938bc-401">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="938bc-401">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-402">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="938bc-402">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="938bc-403">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="938bc-403">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-404">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="938bc-404">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="938bc-405">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="938bc-405">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-406">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="938bc-406">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="938bc-407">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="938bc-407">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-408">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="938bc-408">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="938bc-409">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="938bc-409">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-410">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="938bc-410">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="938bc-411">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="938bc-411">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-412">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="938bc-412">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="938bc-413">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="938bc-413">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-414">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="938bc-414">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="938bc-415">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="938bc-415">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-416">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="938bc-416">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="938bc-417">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="938bc-417">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-418">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="938bc-418">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="938bc-419">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="938bc-419">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-420">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="938bc-420">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="938bc-421">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="938bc-421">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-422">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="938bc-422">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="938bc-423">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="938bc-423">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-424">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="938bc-424">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="938bc-425">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="938bc-425">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-426">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="938bc-426">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="938bc-427">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="938bc-427">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-428">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="938bc-428">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="938bc-429">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="938bc-429">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-430">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="938bc-430">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="938bc-431">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="938bc-431">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-432">Server Cursor</span><span class="sxs-lookup"><span data-stu-id="938bc-432">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="938bc-433">DBPROP_SERVERCURSOR</span><span class="sxs-lookup"><span data-stu-id="938bc-433">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-434">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="938bc-434">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="938bc-435">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="938bc-435">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-436">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="938bc-436">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="938bc-437">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="938bc-437">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-438">Unique Rows</span><span class="sxs-lookup"><span data-stu-id="938bc-438">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="938bc-439">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="938bc-439">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-440">Updatability</span><span class="sxs-lookup"><span data-stu-id="938bc-440">Updatability</span></span></p></td>
<td><p><span data-ttu-id="938bc-441">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="938bc-441">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-442">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="938bc-442">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="938bc-443">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="938bc-443">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="938bc-444">Command の動的プロパティ</span><span class="sxs-lookup"><span data-stu-id="938bc-444">Command Dynamic Properties</span></span>

<span data-ttu-id="938bc-445">次に示すプロパティが **Command** オブジェクトの **Properties** コレクションに追加されます。</span><span class="sxs-lookup"><span data-stu-id="938bc-445">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="938bc-446">ADO プロパティ名</span><span class="sxs-lookup"><span data-stu-id="938bc-446">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="938bc-447">OLE DB プロパティ名</span><span class="sxs-lookup"><span data-stu-id="938bc-447">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="938bc-448">Access Order</span><span class="sxs-lookup"><span data-stu-id="938bc-448">Access Order</span></span></p></td>
<td><p><span data-ttu-id="938bc-449">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="938bc-449">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-450">Base Path</span><span class="sxs-lookup"><span data-stu-id="938bc-450">Base Path</span></span></p></td>
<td><p><span data-ttu-id="938bc-451">SSPROP_STREAM_BASEPATH</span><span class="sxs-lookup"><span data-stu-id="938bc-451">SSPROP_STREAM_BASEPATH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-452">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="938bc-452">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="938bc-453">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="938bc-453">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-454">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="938bc-454">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="938bc-455">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="938bc-455">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-456">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="938bc-456">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="938bc-457">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="938bc-457">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-458">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="938bc-458">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="938bc-459">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="938bc-459">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-460">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="938bc-460">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="938bc-461">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="938bc-461">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-462">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="938bc-462">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="938bc-463">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="938bc-463">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-464">Content Type</span><span class="sxs-lookup"><span data-stu-id="938bc-464">Content Type</span></span></p></td>
<td><p><span data-ttu-id="938bc-465">SSPROP_STREAM_CONTENTTYPE</span><span class="sxs-lookup"><span data-stu-id="938bc-465">SSPROP_STREAM_CONTENTTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-466">Cursor Auto Fetch</span><span class="sxs-lookup"><span data-stu-id="938bc-466">Cursor Auto Fetch</span></span></p></td>
<td><p><span data-ttu-id="938bc-467">SSPROP_CURSORAUTOFETCH</span><span class="sxs-lookup"><span data-stu-id="938bc-467">SSPROP_CURSORAUTOFETCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-468">Defer Column</span><span class="sxs-lookup"><span data-stu-id="938bc-468">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="938bc-469">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="938bc-469">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-470">Defer Prepare</span><span class="sxs-lookup"><span data-stu-id="938bc-470">Defer Prepare</span></span></p></td>
<td><p><span data-ttu-id="938bc-471">SSPROP_DEFERPREPARE</span><span class="sxs-lookup"><span data-stu-id="938bc-471">SSPROP_DEFERPREPARE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-472">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="938bc-472">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="938bc-473">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="938bc-473">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-474">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="938bc-474">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="938bc-475">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="938bc-475">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-476">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="938bc-476">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="938bc-477">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="938bc-477">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-478">IAccessor</span><span class="sxs-lookup"><span data-stu-id="938bc-478">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="938bc-479">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="938bc-479">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-480">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="938bc-480">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="938bc-481">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="938bc-481">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-482">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="938bc-482">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="938bc-483">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="938bc-483">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-484">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="938bc-484">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="938bc-485">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="938bc-485">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-486">IConvertType</span><span class="sxs-lookup"><span data-stu-id="938bc-486">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="938bc-487">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="938bc-487">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-488">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="938bc-488">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="938bc-489">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="938bc-489">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-490">IRowset</span><span class="sxs-lookup"><span data-stu-id="938bc-490">IRowset</span></span></p></td>
<td><p><span data-ttu-id="938bc-491">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="938bc-491">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-492">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="938bc-492">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="938bc-493">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="938bc-493">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-494">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="938bc-494">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="938bc-495">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="938bc-495">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-496">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="938bc-496">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="938bc-497">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="938bc-497">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-498">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="938bc-498">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="938bc-499">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="938bc-499">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-500">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="938bc-500">IRowsetResynch</span></span></p></td>
<td><p><span data-ttu-id="938bc-501">DBPROP_IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="938bc-501">DBPROP_IRowsetResynch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-502">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="938bc-502">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="938bc-503">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="938bc-503">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-504">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="938bc-504">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="938bc-505">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="938bc-505">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-506">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="938bc-506">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="938bc-507">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="938bc-507">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-508">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="938bc-508">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="938bc-509">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="938bc-509">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-510">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="938bc-510">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="938bc-511">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="938bc-511">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-512">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="938bc-512">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="938bc-513">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="938bc-513">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-514">Lock Mode</span><span class="sxs-lookup"><span data-stu-id="938bc-514">Lock Mode</span></span></p></td>
<td><p><span data-ttu-id="938bc-515">DBPROP_LOCKMODE</span><span class="sxs-lookup"><span data-stu-id="938bc-515">DBPROP_LOCKMODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-516">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="938bc-516">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="938bc-517">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="938bc-517">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-518">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="938bc-518">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="938bc-519">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="938bc-519">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-520">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="938bc-520">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="938bc-521">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="938bc-521">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-522">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="938bc-522">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="938bc-523">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="938bc-523">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-524">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="938bc-524">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="938bc-525">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="938bc-525">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-526">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="938bc-526">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="938bc-527">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="938bc-527">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-528">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="938bc-528">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="938bc-529">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="938bc-529">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-530">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="938bc-530">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="938bc-531">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="938bc-531">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-532">Output Encoding Property</span><span class="sxs-lookup"><span data-stu-id="938bc-532">Output Encoding Property</span></span></p></td>
<td><p><span data-ttu-id="938bc-533">DBPROP_OUTPUTENCODING</span><span class="sxs-lookup"><span data-stu-id="938bc-533">DBPROP_OUTPUTENCODING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-534">Output Stream Property</span><span class="sxs-lookup"><span data-stu-id="938bc-534">Output Stream Property</span></span></p></td>
<td><p><span data-ttu-id="938bc-535">DBPROP_OUTPUTSTREAM</span><span class="sxs-lookup"><span data-stu-id="938bc-535">DBPROP_OUTPUTSTREAM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-536">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="938bc-536">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="938bc-537">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="938bc-537">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-538">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="938bc-538">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="938bc-539">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="938bc-539">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-540">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="938bc-540">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="938bc-541">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="938bc-541">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-542">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="938bc-542">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="938bc-543">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="938bc-543">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-544">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="938bc-544">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="938bc-545">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="938bc-545">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-546">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="938bc-546">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="938bc-547">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="938bc-547">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-548">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="938bc-548">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="938bc-549">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="938bc-549">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-550">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="938bc-550">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="938bc-551">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="938bc-551">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-552">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="938bc-552">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="938bc-553">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="938bc-553">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-554">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="938bc-554">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="938bc-555">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="938bc-555">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-556">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="938bc-556">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="938bc-557">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="938bc-557">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-558">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="938bc-558">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="938bc-559">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="938bc-559">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-560">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="938bc-560">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="938bc-561">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="938bc-561">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-562">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="938bc-562">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="938bc-563">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="938bc-563">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-564">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="938bc-564">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="938bc-565">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="938bc-565">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-566">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="938bc-566">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="938bc-567">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="938bc-567">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-568">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="938bc-568">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="938bc-569">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="938bc-569">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-570">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="938bc-570">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="938bc-571">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="938bc-571">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-572">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="938bc-572">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="938bc-573">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="938bc-573">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-574">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="938bc-574">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="938bc-575">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="938bc-575">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-576">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="938bc-576">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="938bc-577">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="938bc-577">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-578">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="938bc-578">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="938bc-579">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="938bc-579">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-580">Server Cursor</span><span class="sxs-lookup"><span data-stu-id="938bc-580">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="938bc-581">DBPROP_SERVERCURSOR</span><span class="sxs-lookup"><span data-stu-id="938bc-581">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-582">Server Data on Insert</span><span class="sxs-lookup"><span data-stu-id="938bc-582">Server Data on Insert</span></span></p></td>
<td><p><span data-ttu-id="938bc-583">DBPROP_SERVERDATAONINSERT</span><span class="sxs-lookup"><span data-stu-id="938bc-583">DBPROP_SERVERDATAONINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-584">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="938bc-584">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="938bc-585">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="938bc-585">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-586">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="938bc-586">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="938bc-587">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="938bc-587">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-588">Updatability</span><span class="sxs-lookup"><span data-stu-id="938bc-588">Updatability</span></span></p></td>
<td><p><span data-ttu-id="938bc-589">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="938bc-589">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-590">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="938bc-590">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="938bc-591">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="938bc-591">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938bc-592">XML Root</span><span class="sxs-lookup"><span data-stu-id="938bc-592">XML Root</span></span></p></td>
<td><p><span data-ttu-id="938bc-593">SSPROP_STREAM_XMLROOT</span><span class="sxs-lookup"><span data-stu-id="938bc-593">SSPROP_STREAM_XMLROOT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938bc-594">XSL</span><span class="sxs-lookup"><span data-stu-id="938bc-594">XSL</span></span></p></td>
<td><p><span data-ttu-id="938bc-595">SSPROP_STREAM_XSL</span><span class="sxs-lookup"><span data-stu-id="938bc-595">SSPROP_STREAM_XSL</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="938bc-596">Microsoft SQL Server OLE DB Provider の実装方法および機能の詳細については、MDAC SDK の OLE DB の OLE DB Provider for SQL Server のマニュアルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="938bc-596">For specific implementation details and functional information about the Microsoft SQL Server OLE DB Provider, consult the OLE DB Provider for SQL Server documentation in the OLE DB section of the MDAC SDK.</span></span>

