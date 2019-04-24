---
title: Microsoft OLE DB Provider for ODBC
TOCTitle: Microsoft OLE DB Provider for ODBC
ms:assetid: c507567e-5ad1-b32a-f6ad-5ba2c39aa4c2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249964(v=office.15)
ms:contentKeyID: 48547602
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4f5ffae4880cadb90f47f1ac348ffc8b3ea58785
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288912"
---
# <a name="microsoft-ole-db-provider-for-odbc"></a><span data-ttu-id="5834b-102">Microsoft OLE DB Provider for ODBC</span><span class="sxs-lookup"><span data-stu-id="5834b-102">Microsoft OLE DB Provider for ODBC</span></span>

<span data-ttu-id="5834b-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="5834b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5834b-p101">ADO または RDS のプログラマにとって、すべてのデータ ソースで OLE DB インターフェイスが公開され、ADO で直接データ ソースを呼び出すことができるのが理想的です。OLE DB インターフェイスを実装するデータベース ベンダーは増えていますが、まだこのインターフェイスを公開していないデータ ソースもあります。ただし、現在使用されている事実上すべての DBMS システムは、ODBC によるアクセスが可能です。</span><span class="sxs-lookup"><span data-stu-id="5834b-p101">To an ADO or RDS programmer, an ideal world would be one in which every data source exposes an OLE DB interface, so that ADO could call directly into the data source. Although increasingly more database vendors are implementing OLE DB interfaces, some data sources are not yet exposed this way. However, virtually all DBMS systems in use today can be accessed through ODBC.</span></span>

<span data-ttu-id="5834b-107">ODBC ドライバーは、Microsoft SQL Server、Microsoft Access (Microsoft Jet データベース エンジン)、および Microsoft FoxPro だけでなく、Oracle などの Microsoft 以外のデータベース製品を含めた、現在使用されているすべての主要 DBMS で使用できます。</span><span class="sxs-lookup"><span data-stu-id="5834b-107">ODBC drivers are available for every major DBMS in use today, including Microsoft SQL Server, Microsoft Access (Microsoft Jet database engine), and Microsoft FoxPro, in addition to non-Microsoft database products such as Oracle.</span></span>

<span data-ttu-id="5834b-p102">ただし、Microsoft ODBC Provider を使用すると、ADO からすべての ODBC データ ソースに接続できます。このプロバイダーはフリースレッドであり、Unicode に対応しています。</span><span class="sxs-lookup"><span data-stu-id="5834b-p102">The Microsoft ODBC Provider, however, allows ADO to connect to any ODBC data source. The provider is free-threaded and Unicode enabled.</span></span>

<span data-ttu-id="5834b-p103">このプロバイダーはトランザクションをサポートしていますが、DBMS エンジンの種類によって、サポートするトランザクションの種類が異なります。たとえば、Microsoft Access は 5 レベルまでのネストされたトランザクションをサポートします。</span><span class="sxs-lookup"><span data-stu-id="5834b-p103">The provider supports transactions, although different DBMS engines offer different types of transaction support. For example, Microsoft Access supports nested transactions up to five levels deep.</span></span>

<span data-ttu-id="5834b-112">このプロバイダーは ADO の既定のプロバイダーであり、プロバイダーに依存するすべての ADO プロパティおよびメソッドをサポートします。</span><span class="sxs-lookup"><span data-stu-id="5834b-112">This is the default provider for ADO, and all provider-dependent ADO properties and methods are supported.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="5834b-113">接続文字列パラメーター</span><span class="sxs-lookup"><span data-stu-id="5834b-113">Connection String Parameters</span></span>

<span data-ttu-id="5834b-114">このプロバイダーに接続するには、[ConnectionString](connectionstring-property-ado.md) プロパティの **Provider=** 引数を次のように設定します。</span><span class="sxs-lookup"><span data-stu-id="5834b-114">To connect to this provider, set the **Provider=** argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```sql 
 
MSDASQL 
```

<span data-ttu-id="5834b-115">[Provider](provider-property-ado.md) プロパティを取得した場合も、この文字列が返されます。</span><span class="sxs-lookup"><span data-stu-id="5834b-115">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="5834b-116">標準的な接続文字列</span><span class="sxs-lookup"><span data-stu-id="5834b-116">Typical Connection String</span></span>

<span data-ttu-id="5834b-117">このプロバイダーの標準的な接続文字列を次に示します。</span><span class="sxs-lookup"><span data-stu-id="5834b-117">A typical connection string for this provider is:</span></span>

```sql 
 
"Provider=MSDASQL;DSN=dsnName;UID=userName;PWD=userPassword;" 
```

<span data-ttu-id="5834b-118">この文字列は、次に示すキーワードで構成されています。</span><span class="sxs-lookup"><span data-stu-id="5834b-118">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5834b-119">キーワード</span><span class="sxs-lookup"><span data-stu-id="5834b-119">Keyword</span></span></p></th>
<th><p><span data-ttu-id="5834b-120">説明</span><span class="sxs-lookup"><span data-stu-id="5834b-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5834b-121"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="5834b-121"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="5834b-122">OLE DB Provider for ODBC を指定します。</span><span class="sxs-lookup"><span data-stu-id="5834b-122">Specifies the OLE DB Provider for ODBC.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-123"><strong>DSN</strong></span><span class="sxs-lookup"><span data-stu-id="5834b-123"><strong>DSN</strong></span></span></p></td>
<td><p><span data-ttu-id="5834b-124">データ ソース名を指定します。</span><span class="sxs-lookup"><span data-stu-id="5834b-124">Specifies the data source name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-125"><strong>UID</strong></span><span class="sxs-lookup"><span data-stu-id="5834b-125"><strong>UID</strong></span></span></p></td>
<td><p><span data-ttu-id="5834b-126">ユーザー名を指定します。</span><span class="sxs-lookup"><span data-stu-id="5834b-126">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-127"><strong>PWD</strong></span><span class="sxs-lookup"><span data-stu-id="5834b-127"><strong>PWD</strong></span></span></p></td>
<td><p><span data-ttu-id="5834b-128">ユーザー パスワードを指定します。</span><span class="sxs-lookup"><span data-stu-id="5834b-128">Specifies the user password.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-129"><strong>URL</strong></span><span class="sxs-lookup"><span data-stu-id="5834b-129"><strong>URL</strong></span></span></p></td>
<td><p><span data-ttu-id="5834b-130">web フォルダーに公開されているファイルまたはディレクトリの URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="5834b-130">Specifies the URL of a file or directory published in a web folder.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5834b-131">このプロバイダーは ADO の既定のプロバイダーであるため、接続文字列で **Provider=** パラメーターを省略すると、このプロバイダーへの接続の確立が試行されます。</span><span class="sxs-lookup"><span data-stu-id="5834b-131">Because this is the default provider for ADO, if you omit the **Provider=** parameter from the connection string, ADO will attempt to establish a connection to this provider.</span></span>

<span data-ttu-id="5834b-p104">このプロバイダーは、ADO で定義されたパラメーター以外に独自の接続パラメーターをサポートしません。ただし、ADO 以外の接続パラメーターが指定されている場合は、ODBC ドライバー マネージャーに渡します。</span><span class="sxs-lookup"><span data-stu-id="5834b-p104">The provider does not support any specific connection parameters in addition to those defined by ADO. However, the provider will pass any non-ADO connection parameters to the ODBC driver manager.</span></span>

<span data-ttu-id="5834b-p105">**Provider** パラメーターを省略できるので、同じデータ ソースに対して ODBC 接続文字列と同じ ADO 接続文字列を作成できます。ODBC 接続文字列を作成するときと同じパラメーター名 (**DRIVER=**、**DATABASE=**、**DSN=** など)、値、および構文を使用します。定義済みのデータ ソース名 (DSN) または FileDSN を指定してもしなくても接続できます。</span><span class="sxs-lookup"><span data-stu-id="5834b-p105">Because you can omit the **Provider** parameter, you can therefore compose an ADO connection string that is identical to an ODBC connection string for the same data source. Use the same parameter names (**DRIVER=**, **DATABASE=**, **DSN=**, and so on), values, and syntax as you would when composing an ODBC connection string. You can connect with or without a predefined data source name (DSN) or FileDSN.</span></span>

<span data-ttu-id="5834b-137">**DSN または FileDSN を指定する場合の構文:**</span><span class="sxs-lookup"><span data-stu-id="5834b-137">**Syntax with a DSN or FileDSN:**</span></span>

`"[Provider=MSDASQL;] { DSN=name | FileDSN=filename } ; [DATABASE=database;] UID=user; PWD=password"`

<span data-ttu-id="5834b-138">**DSN 指定しない場合の構文 (DSN なしの接続):**</span><span class="sxs-lookup"><span data-stu-id="5834b-138">**Syntax without a DSN (DSN-less connection):**</span></span>

`"[Provider=MSDASQL;] DRIVER=driver; SERVER=server;DATABASE=database; UID=user; PWD=password"`

<span data-ttu-id="5834b-p106">If you use a **DSN** or **FileDSN**, it must be defined through the ODBC Data Source Administrator in the Windows Control Panel. In Microsoft Windows 2000, the ODBC Administrator is located under Administrative Tools. In previous versions of Windows, the ODBC Administrator icon is named **32-bit ODBC** or simply **ODBC**.</span><span class="sxs-lookup"><span data-stu-id="5834b-p106">If you use a **DSN** or **FileDSN**, it must be defined through the ODBC Data Source Administrator in the Windows Control Panel. In Microsoft Windows 2000, the ODBC Administrator is located under Administrative Tools. In previous versions of Windows, the ODBC Administrator icon is named **32-bit ODBC** or simply **ODBC**.</span></span>

<span data-ttu-id="5834b-142">**DSN** を設定する代わりに、"SQL Server" などの ODBC ドライバー (**DRIVER=**)、サーバー名 (**SERVER=**)、およびデータベース名 (**DATABASE=**) を指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="5834b-142">As an alternative to setting a **DSN**, you can specify the ODBC driver (**DRIVER=**), such as "SQL Server;" the server name (**SERVER=**); and the database name (**DATABASE=**).</span></span>

<span data-ttu-id="5834b-143">ユーザー アカウント名 (**UID=**) と、そのユーザー アカウントのパスワード (**PWD=**) を、ODBC 固有のパラメーターまたは ADO で定義された標準的な *user* パラメーターと *password* パラメーターで指定できます。</span><span class="sxs-lookup"><span data-stu-id="5834b-143">You can also specify a user account name (**UID=**), and the password for the user account (**PWD=**) in the ODBC-specific parameters or in the standard ADO-defined *user* and *password* parameters.</span></span>

<span data-ttu-id="5834b-144">**dsn**定義は既にデータベースを指定しています\*\* が、別のデータベースに接続するために**dsn**だけでなく*database*パラメーターを指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="5834b-144">Although a **DSN** definition already specifies a database, you can specify *a* *database* parameter in addition to a **DSN** to connect to a different database.</span></span> <span data-ttu-id="5834b-145">**DSN**を使用するときは *、* 常に*database*パラメーターを含めることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="5834b-145">It is a good idea to always include *the* *database* parameter when you use a **DSN**.</span></span> <span data-ttu-id="5834b-146">This will ensure that you connect to the proper database in the event that another user changed the default database parameter since you last checked the **DSN** definition.</span><span class="sxs-lookup"><span data-stu-id="5834b-146">This will ensure that you connect to the proper database in the event that another user changed the default database parameter since you last checked the **DSN** definition.</span></span>

## <a name="provider-specific-connection-properties"></a><span data-ttu-id="5834b-147">プロバイダー固有の Connection のプロパティ</span><span class="sxs-lookup"><span data-stu-id="5834b-147">Provider-Specific Connection Properties</span></span>

<span data-ttu-id="5834b-p108">OLE DB Provider for ODBC は、**Connection** オブジェクトの [Properties](properties-collection-ado.md) コレクションにプロパティを追加します。次の表は、これらのプロパティの一覧で、かっこ内は対応する OLE DB プロパティ名です。</span><span class="sxs-lookup"><span data-stu-id="5834b-p108">The OLE DB provider for ODBC adds several properties to the [Properties](properties-collection-ado.md) collection of the **Connection** object. The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5834b-150">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="5834b-150">Property Name</span></span></p></th>
<th><p><span data-ttu-id="5834b-151">説明</span><span class="sxs-lookup"><span data-stu-id="5834b-151">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5834b-152">アクセス可能な手順</span><span class="sxs-lookup"><span data-stu-id="5834b-152">Accessible Procedures</span></span><br />
<span data-ttu-id="5834b-153">(KAGPROP_ACCESSIBLEPROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="5834b-153">(KAGPROP_ACCESSIBLEPROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="5834b-154">ユーザーがストアド プロシージャにアクセスできるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="5834b-154">Indicates whether the user has access to stored procedures.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-155">アクセス可能なテーブル</span><span class="sxs-lookup"><span data-stu-id="5834b-155">Accessible Tables</span></span><br />
<span data-ttu-id="5834b-156">(KAGPROP_ACCESSIBLETABLES)</span><span class="sxs-lookup"><span data-stu-id="5834b-156">(KAGPROP_ACCESSIBLETABLES)</span></span></p></td>
<td><p><span data-ttu-id="5834b-157">ユーザーがデータベースのテーブルに対して SELECT ステートメントを実行する権限を持つかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="5834b-157">Indicates whether the user has permission to execute SELECT statements against the database tables.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-158">アクティブなステートメント</span><span class="sxs-lookup"><span data-stu-id="5834b-158">Active Statements</span></span><br />
<span data-ttu-id="5834b-159">(KAGPROP_ACTIVESTATEMENTS)</span><span class="sxs-lookup"><span data-stu-id="5834b-159">(KAGPROP_ACTIVESTATEMENTS)</span></span></p></td>
<td><p><span data-ttu-id="5834b-160">ODBC ドライバーが 1 つの接続でサポートできるハンドル数を示します。</span><span class="sxs-lookup"><span data-stu-id="5834b-160">Indicates the number of handles an ODBC driver can support on a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-161">ドライバー名</span><span class="sxs-lookup"><span data-stu-id="5834b-161">Driver Name</span></span><br />
<span data-ttu-id="5834b-162">(KAGPROP_DRIVERNAME)</span><span class="sxs-lookup"><span data-stu-id="5834b-162">(KAGPROP_DRIVERNAME)</span></span></p></td>
<td><p><span data-ttu-id="5834b-163">ODBC ドライバーのファイル名を示します。</span><span class="sxs-lookup"><span data-stu-id="5834b-163">Indicates the file name of the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-164">ドライバーの ODBC バージョン</span><span class="sxs-lookup"><span data-stu-id="5834b-164">Driver ODBC Version</span></span><br />
<span data-ttu-id="5834b-165">(KAGPROP_DRIVERODBCVER)</span><span class="sxs-lookup"><span data-stu-id="5834b-165">(KAGPROP_DRIVERODBCVER)</span></span></p></td>
<td><p><span data-ttu-id="5834b-166">このドライバーがサポートする ODBC のバージョンを示します。</span><span class="sxs-lookup"><span data-stu-id="5834b-166">Indicates the version of ODBC that this driver supports.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-167">ファイルの使用状況</span><span class="sxs-lookup"><span data-stu-id="5834b-167">File Usage</span></span><br />
<span data-ttu-id="5834b-168">(KAGPROP_FILEUSAGE)</span><span class="sxs-lookup"><span data-stu-id="5834b-168">(KAGPROP_FILEUSAGE)</span></span></p></td>
<td><p><span data-ttu-id="5834b-169">ドライバーがデータ ソース内のファイルを、テーブルとして扱うか、カタログとして扱うかを示します。</span><span class="sxs-lookup"><span data-stu-id="5834b-169">Indicates how the driver treats a file in a data source; as a table or as a catalog.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-170">Like Escape 句</span><span class="sxs-lookup"><span data-stu-id="5834b-170">Like Escape Clause</span></span><br />
<span data-ttu-id="5834b-171">(KAGPROP_LIKEESCAPECLAUSE)</span><span class="sxs-lookup"><span data-stu-id="5834b-171">(KAGPROP_LIKEESCAPECLAUSE)</span></span></p></td>
<td><p><span data-ttu-id="5834b-172">ドライバーが、WHERE 句の LIKE 述語でパーセント記号 (%) および下線記号 (_) のエスケープ文字を定義および使用できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="5834b-172">Indicates whether the driver supports the definition and use of an escape character for the percent character (%) and underline character (_) in the LIKE predicate of a WHERE clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-173">Group By の最大列</span><span class="sxs-lookup"><span data-stu-id="5834b-173">Max Columns in Group By</span></span><br />
<span data-ttu-id="5834b-174">(KAGPROP_MAXCOLUMNSINGROUPBY)</span><span class="sxs-lookup"><span data-stu-id="5834b-174">(KAGPROP_MAXCOLUMNSINGROUPBY)</span></span></p></td>
<td><p><span data-ttu-id="5834b-175">SELECT ステートメントの GROUP BY 句に記述できる最大列数を示します。</span><span class="sxs-lookup"><span data-stu-id="5834b-175">Indicates the maximum number of columns that can be listed in the GROUP BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-176">インデックスの最大列数</span><span class="sxs-lookup"><span data-stu-id="5834b-176">Max Columns in Index</span></span><br />
<span data-ttu-id="5834b-177">(KAGPROP_MAXCOLUMNSININDEX)</span><span class="sxs-lookup"><span data-stu-id="5834b-177">(KAGPROP_MAXCOLUMNSININDEX)</span></span></p></td>
<td><p><span data-ttu-id="5834b-178">インデックスに格納できる最大列数を示します。</span><span class="sxs-lookup"><span data-stu-id="5834b-178">Indicates the maximum number of columns that can be included in an index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-179">Order By における最大列数</span><span class="sxs-lookup"><span data-stu-id="5834b-179">Max Columns in Order By</span></span><br />
<span data-ttu-id="5834b-180">(KAGPROP_MAXCOLUMNSINORDERBY)</span><span class="sxs-lookup"><span data-stu-id="5834b-180">(KAGPROP_MAXCOLUMNSINORDERBY)</span></span></p></td>
<td><p><span data-ttu-id="5834b-181">SELECT ステートメントの ORDER BY 句に記述できる最大列数を示します。</span><span class="sxs-lookup"><span data-stu-id="5834b-181">Indicates the maximum number of columns that can be listed in the ORDER BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-182">Select の最大列</span><span class="sxs-lookup"><span data-stu-id="5834b-182">Max Columns in Select</span></span><br />
<span data-ttu-id="5834b-183">(KAGPROP_MAXCOLUMNSINSELECT)</span><span class="sxs-lookup"><span data-stu-id="5834b-183">(KAGPROP_MAXCOLUMNSINSELECT)</span></span></p></td>
<td><p><span data-ttu-id="5834b-184">SELECT ステートメントの SELECT 部分に記述できる最大列数を示します。</span><span class="sxs-lookup"><span data-stu-id="5834b-184">Indicates the maximum number of columns that can be listed in the SELECT portion of a SELECT statement.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-185">テーブルの最大列数</span><span class="sxs-lookup"><span data-stu-id="5834b-185">Max Columns in Table</span></span><br />
<span data-ttu-id="5834b-186">(KAGPROP_MAXCOLUMNSINTABLE)</span><span class="sxs-lookup"><span data-stu-id="5834b-186">(KAGPROP_MAXCOLUMNSINTABLE)</span></span></p></td>
<td><p><span data-ttu-id="5834b-187">テーブルの最大列数を示します。</span><span class="sxs-lookup"><span data-stu-id="5834b-187">Indicates the maximum number of columns allowed in a table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-188">数値を処理する関数</span><span class="sxs-lookup"><span data-stu-id="5834b-188">Numeric Functions</span></span><br />
<span data-ttu-id="5834b-189">(KAGPROP_NUMERICFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="5834b-189">(KAGPROP_NUMERICFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="5834b-p109">ODBC ドライバーがサポートする数値関数を示します。関数名とこのビットマスクで使用される関連付けられた値の一覧については、ODBC マニュアルの「Appendix E: Scalar Functions」 (英語) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5834b-p109">Indicates which numeric functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-192">外部参加機能</span><span class="sxs-lookup"><span data-stu-id="5834b-192">Outer Join Capabilities</span></span><br />
<span data-ttu-id="5834b-193">(KAGPROP_OJCAPABILITY)</span><span class="sxs-lookup"><span data-stu-id="5834b-193">(KAGPROP_OJCAPABILITY)</span></span></p></td>
<td><p><span data-ttu-id="5834b-194">プロバイダーがサポートする OUTER JOIN の種類を示します。</span><span class="sxs-lookup"><span data-stu-id="5834b-194">Indicates the types of OUTER JOINs supported by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-195">外部結合</span><span class="sxs-lookup"><span data-stu-id="5834b-195">Outer Joins</span></span><br />
<span data-ttu-id="5834b-196">(KAGPROP_OUTERJOINS)</span><span class="sxs-lookup"><span data-stu-id="5834b-196">(KAGPROP_OUTERJOINS)</span></span></p></td>
<td><p><span data-ttu-id="5834b-197">プロバイダーが OUTER JOIN をサポートするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="5834b-197">Indicates whether the provider supports OUTER JOINs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-198">特殊文字</span><span class="sxs-lookup"><span data-stu-id="5834b-198">Special Characters</span></span><br />
<span data-ttu-id="5834b-199">(KAGPROP_SPECIALCHARACTERS)</span><span class="sxs-lookup"><span data-stu-id="5834b-199">(KAGPROP_SPECIALCHARACTERS)</span></span></p></td>
<td><p><span data-ttu-id="5834b-200">ODBC ドライバーで特別な意味を持つ文字を示します。</span><span class="sxs-lookup"><span data-stu-id="5834b-200">Indicates which characters have special meaning for the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-201">ストアド プロシージャ</span><span class="sxs-lookup"><span data-stu-id="5834b-201">Stored Procedures</span></span><br />
<span data-ttu-id="5834b-202">(KAGPROP_PROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="5834b-202">(KAGPROP_PROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="5834b-203">この ODBC ドライバーでストアド プロシージャを使用できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="5834b-203">Indicates whether stored procedures are available for use with this ODBC driver.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-204">文字列を処理する関数</span><span class="sxs-lookup"><span data-stu-id="5834b-204">String Functions</span></span><br />
<span data-ttu-id="5834b-205">(KAGPROP_STRINGFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="5834b-205">(KAGPROP_STRINGFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="5834b-p110">ODBC ドライバーがサポートする文字列関数を示します。関数名とこのビットマスクで使用される関連付けられた値の一覧については、ODBC マニュアルの「Appendix E: Scalar Functions」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5834b-p110">Indicates which string functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-208">システム関数</span><span class="sxs-lookup"><span data-stu-id="5834b-208">System Functions</span></span><br />
<span data-ttu-id="5834b-209">(KAGPROP_SYSTEMFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="5834b-209">(KAGPROP_SYSTEMFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="5834b-p111">ODBC ドライバーがサポートするシステム関数を示します。関数名とこのビットマスクで使用される関連付けられた値の一覧については、ODBC マニュアルの「Appendix E: Scalar Functions」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5834b-p111">Indicates which system functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-212">日付/時刻関数</span><span class="sxs-lookup"><span data-stu-id="5834b-212">Time/Date Functions</span></span><br />
<span data-ttu-id="5834b-213">(KAGPROP_TIMEDATEFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="5834b-213">(KAGPROP_TIMEDATEFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="5834b-p112">ODBC ドライバーがサポートする時刻/日付関数を示します。関数名とこのビットマスクで使用される関連付けられた値の一覧については、ODBC マニュアルの「Appendix E: Scalar Functions」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5834b-p112">Indicates which time and date functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-216">SQL 文法のサポート</span><span class="sxs-lookup"><span data-stu-id="5834b-216">SQL Grammar Support</span></span><br />
<span data-ttu-id="5834b-217">(KAGPROP_ODBCSQLCONFORMANCE)</span><span class="sxs-lookup"><span data-stu-id="5834b-217">(KAGPROP_ODBCSQLCONFORMANCE)</span></span></p></td>
<td><p><span data-ttu-id="5834b-218">ODBC ドライバーがサポートする SQL 文法を示します。</span><span class="sxs-lookup"><span data-stu-id="5834b-218">Indicates the SQL grammar that the ODBC driver supports.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a><span data-ttu-id="5834b-219">プロバイダー固有の Recordset および Command のプロパティ</span><span class="sxs-lookup"><span data-stu-id="5834b-219">Provider-Specific Recordset and Command Properties</span></span>

<span data-ttu-id="5834b-p113">OLE DB Provider for ODBC は、**Recordset** オブジェクトと **Command** オブジェクトの **Properties** コレクションにプロパティを追加します。次の表は、これらのプロパティの一覧で、かっこ内は対応する OLE DB プロパティ名です。</span><span class="sxs-lookup"><span data-stu-id="5834b-p113">The OLE DB provider for ODBC adds several properties to the **Properties** collection of the **Recordset** and **Command** objects. The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5834b-222">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="5834b-222">Property Name</span></span></p></th>
<th><p><span data-ttu-id="5834b-223">説明</span><span class="sxs-lookup"><span data-stu-id="5834b-223">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5834b-224">クエリベースの更新/削除/挿入</span><span class="sxs-lookup"><span data-stu-id="5834b-224">Query Based Updates/Deletes/Inserts</span></span><br />
<span data-ttu-id="5834b-225">(KAGPROP_QUERYBASEDUPDATES)</span><span class="sxs-lookup"><span data-stu-id="5834b-225">(KAGPROP_QUERYBASEDUPDATES)</span></span></p></td>
<td><p><span data-ttu-id="5834b-226">SQL クエリを使用して更新、削除、および挿入を実行できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="5834b-226">Indicates whether updates, deletions, and insertions can be performed using SQL queries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-227">ODBC の同時実行の種類</span><span class="sxs-lookup"><span data-stu-id="5834b-227">ODBC Concurrency Type</span></span><br />
<span data-ttu-id="5834b-228">(KAGPROP_CONCURRENCY)</span><span class="sxs-lookup"><span data-stu-id="5834b-228">(KAGPROP_CONCURRENCY)</span></span></p></td>
<td><p><span data-ttu-id="5834b-229">2 人のユーザーがデータ ソースの同じデータに同時にアクセスしようとしたときに発生する問題を減少させるための方法を示します。</span><span class="sxs-lookup"><span data-stu-id="5834b-229">Indicates the method used to reduce potential problems caused by two users attempting to access the same data from the data source simultaneously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-230">前方のみカーソルでの BLOB アクセシビリティ</span><span class="sxs-lookup"><span data-stu-id="5834b-230">BLOB accessibility on Forward-Only cursor</span></span><br />
<span data-ttu-id="5834b-231">(KAGPROP_BLOBSONFOCURSOR)</span><span class="sxs-lookup"><span data-stu-id="5834b-231">(KAGPROP_BLOBSONFOCURSOR)</span></span></p></td>
<td><p><span data-ttu-id="5834b-232">前方のみのカーソルの使用時に BLOB <strong>Fields</strong> にアクセスできるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="5834b-232">Indicates whether BLOB <strong>Fields</strong> can be accessed when using a forward-only cursor.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-233">SQL_FLOAT、SQL_DOUBLE、および SQL_REAL を qbu WHERE 句に含める</span><span class="sxs-lookup"><span data-stu-id="5834b-233">Include SQL_FLOAT, SQL_DOUBLE, and SQL_REAL in QBU WHERE clauses</span></span><br />
<span data-ttu-id="5834b-234">(KAGPROP_INCLUDENONEXACT)</span><span class="sxs-lookup"><span data-stu-id="5834b-234">(KAGPROP_INCLUDENONEXACT)</span></span></p></td>
<td><p><span data-ttu-id="5834b-235">SQL_FLOAT、SQL_DOUBLE、および SQL_REAL の値を QBU WHERE 句に含めることができるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="5834b-235">Indicates whether SQL_FLOAT, SQL_DOUBLE, and SQL_REAL values can be included in a QBU WHERE clause.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-236">挿入後の最終行の位置</span><span class="sxs-lookup"><span data-stu-id="5834b-236">Position on the last row after insert</span></span><br />
<span data-ttu-id="5834b-237">(KAGPROP_POSITIONONNEWROW)</span><span class="sxs-lookup"><span data-stu-id="5834b-237">(KAGPROP_POSITIONONNEWROW)</span></span></p></td>
<td><p><span data-ttu-id="5834b-238">新規レコードをテーブルに挿入した後、テーブルの最後の行が現在の行になるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="5834b-238">Indicates that after a new record has been inserted in a table, the last row in the table will be come the current row.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-239">IRowsetChangeExtInfo</span><span class="sxs-lookup"><span data-stu-id="5834b-239">IRowsetChangeExtInfo</span></span><br />
<span data-ttu-id="5834b-240">(KAGPROP_IROWSETCHANGEEXTINFO)</span><span class="sxs-lookup"><span data-stu-id="5834b-240">(KAGPROP_IROWSETCHANGEEXTINFO)</span></span></p></td>
<td><p><span data-ttu-id="5834b-241"><strong>IRowsetChange</strong> インターフェイスが拡張情報を提供するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="5834b-241">Indicates whether the <strong>IRowsetChange</strong> interface provides extended information support.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-242">ODBC カーソルの種類</span><span class="sxs-lookup"><span data-stu-id="5834b-242">ODBC Cursor Type</span></span><br />
<span data-ttu-id="5834b-243">(KAGPROP_CURSOR)</span><span class="sxs-lookup"><span data-stu-id="5834b-243">(KAGPROP_CURSOR)</span></span></p></td>
<td><p><span data-ttu-id="5834b-244"><strong>Recordset</strong> で使用されるカーソルの種類を示します。</span><span class="sxs-lookup"><span data-stu-id="5834b-244">Indicates the type of cursor used by the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-245">マーシャリングできる行セットを生成する</span><span class="sxs-lookup"><span data-stu-id="5834b-245">Generate a Rowset that can be marshaled</span></span><br />
<span data-ttu-id="5834b-246">(KAGPROP_MARSHALLABLE)</span><span class="sxs-lookup"><span data-stu-id="5834b-246">(KAGPROP_MARSHALLABLE)</span></span></p></td>
<td><p><span data-ttu-id="5834b-247">ODBC ドライバーがマーシャリング可能なレコードセットを生成することを示します。</span><span class="sxs-lookup"><span data-stu-id="5834b-247">Indicates that the ODBC driver generates a recordset that can be marshaled</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a><span data-ttu-id="5834b-248">コマンド テキスト</span><span class="sxs-lookup"><span data-stu-id="5834b-248">Command Text</span></span>

<span data-ttu-id="5834b-249">[Command](command-object-ado.md) オブジェクトの使用方法は、データ ソースおよび受け付けられるクエリまたはコマンド ステートメントの種類によって大きく異なります。</span><span class="sxs-lookup"><span data-stu-id="5834b-249">How you use the [Command](command-object-ado.md) object largely depends on the data source, and what type of query or command statement it will accept.</span></span>

<span data-ttu-id="5834b-p114">ODBC には、ストアド プロシージャを呼び出すための独自の構文があります。**Command** オブジェクトの [CommandText](commandtext-property-ado.md) プロパティ、[Connection](connection-object-ado.md) オブジェクトの **Execute** メソッドの *CommandText* 引数、または [Recordset](recordset-object-ado.md) オブジェクトの **Open** メソッドの *Source* 引数の場合は、次の構文で文字列を渡します。</span><span class="sxs-lookup"><span data-stu-id="5834b-p114">ODBC provides a specific syntax for calling stored procedures. For the [CommandText](commandtext-property-ado.md) property of a **Command** object, the *CommandText* argument to the **Execute** method on a [Connection](connection-object-ado.md) object, or the *Source* argument to the **Open** method on a [Recordset](recordset-object-ado.md) object, passes in a string with this syntax:</span></span>

`"{ [ ? = ] call procedure [ ( ? [, ? [ ,  ]] ) ] }"`

<span data-ttu-id="5834b-252">**?**</span><span class="sxs-lookup"><span data-stu-id="5834b-252">Each **?**</span></span> <span data-ttu-id="5834b-253">はそれぞれ [Parameters](parameters-collection-ado.md) コレクションのオブジェクトを参照します。</span><span class="sxs-lookup"><span data-stu-id="5834b-253">references an object in the [Parameters](parameters-collection-ado.md) collection.</span></span> <span data-ttu-id="5834b-254">最初の **?**</span><span class="sxs-lookup"><span data-stu-id="5834b-254">The first **?**</span></span> <span data-ttu-id="5834b-255">参照する**パラメーター**(0)、次に参照し**ます。**</span><span class="sxs-lookup"><span data-stu-id="5834b-255">references **Parameters**(0), the next **?**</span></span> <span data-ttu-id="5834b-256">**パラメーター**(1) などを参照します。</span><span class="sxs-lookup"><span data-stu-id="5834b-256">references **Parameters**(1), and so on.</span></span>

<span data-ttu-id="5834b-p116">パラメーターの参照は省略可能で、ストアド プロシージャの構造に依存します。パラメーターを定義していないストアド プロシージャを呼び出す場合の構文は、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="5834b-p116">The parameter references are optional and depend on the structure of the stored procedure. If you want to call a stored procedure that defines no parameters, your string would look like this:</span></span>

`"{ call procedure }"`

<span data-ttu-id="5834b-259">2 つのクエリ パラメーターを持つ場合は、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="5834b-259">If you have two query parameters, your string would look like this:</span></span>

`"{ call procedure ( ?, ? ) }"`

<span data-ttu-id="5834b-p117">ストアド プロシージャが値を返す場合、戻り値は別のパラメーターとして扱われます。クエリ パラメーターがなく、戻り値がある場合は、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="5834b-p117">If the stored procedure will return a value, the return value is treated as another parameter. If you have no query parameters but you do have a return value, your string would look like this:</span></span>

`"{ ? = call procedure }"`

<span data-ttu-id="5834b-262">戻り値があり、2 つのクエリ パラメーターがある場合は、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="5834b-262">Finally, if you have a return value and two query parameters, your string would look like this:</span></span>

`"{ ? = call procedure ( ?, ? ) }"`

## <a name="recordset-behavior"></a><span data-ttu-id="5834b-263">Recordset の動作</span><span class="sxs-lookup"><span data-stu-id="5834b-263">Recordset Behavior</span></span>

<span data-ttu-id="5834b-264">次の表は、このプロバイダーで開かれた **Recordset** オブジェクトで利用可能な標準の ADO メソッドと ADO プロパティの一覧です。</span><span class="sxs-lookup"><span data-stu-id="5834b-264">The following tables list the standard ADO methods and properties available on a **Recordset** object opened with this provider.</span></span>

<span data-ttu-id="5834b-265">プロバイダーの構成による **Recordset** の動作の詳細については、 [Supports](supports-method-ado.md) メソッドを実行し、 **Recordset** の **Properties** コレクションを列挙して、プロバイダー固有の動的プロパティが存在するかどうかを確認してください。</span><span class="sxs-lookup"><span data-stu-id="5834b-265">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the **Properties** collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="5834b-266">標準的な ADO **Recordset** のプロパティの利用可能性は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="5834b-266">Availability of standard ADO **Recordset** properties:</span></span>

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
<th><p><span data-ttu-id="5834b-267">プロパティ</span><span class="sxs-lookup"><span data-stu-id="5834b-267">Property</span></span></p></th>
<th><p><span data-ttu-id="5834b-268">ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="5834b-268">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="5834b-269">Dynamic</span><span class="sxs-lookup"><span data-stu-id="5834b-269">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="5834b-270">Keyset</span><span class="sxs-lookup"><span data-stu-id="5834b-270">Keyset</span></span></p></th>
<th><p><span data-ttu-id="5834b-271">Static</span><span class="sxs-lookup"><span data-stu-id="5834b-271">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5834b-272"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="5834b-272"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="5834b-273">使用不可</span><span class="sxs-lookup"><span data-stu-id="5834b-273">not available</span></span></p></td>
<td><p><span data-ttu-id="5834b-274">使用不可</span><span class="sxs-lookup"><span data-stu-id="5834b-274">not available</span></span></p></td>
<td><p><span data-ttu-id="5834b-275">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-275">read/write</span></span></p></td>
<td><p><span data-ttu-id="5834b-276">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-276">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-277"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="5834b-277"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="5834b-278">使用不可</span><span class="sxs-lookup"><span data-stu-id="5834b-278">not available</span></span></p></td>
<td><p><span data-ttu-id="5834b-279">使用不可</span><span class="sxs-lookup"><span data-stu-id="5834b-279">not available</span></span></p></td>
<td><p><span data-ttu-id="5834b-280">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-280">read/write</span></span></p></td>
<td><p><span data-ttu-id="5834b-281">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-281">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-282"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="5834b-282"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="5834b-283">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-283">read/write</span></span></p></td>
<td><p><span data-ttu-id="5834b-284">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-284">read/write</span></span></p></td>
<td><p><span data-ttu-id="5834b-285">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-285">read/write</span></span></p></td>
<td><p><span data-ttu-id="5834b-286">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-286">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-287"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="5834b-287"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="5834b-288">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="5834b-288">read-only</span></span></p></td>
<td><p><span data-ttu-id="5834b-289">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="5834b-289">read-only</span></span></p></td>
<td><p><span data-ttu-id="5834b-290">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="5834b-290">read-only</span></span></p></td>
<td><p><span data-ttu-id="5834b-291">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="5834b-291">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-292"><a href="bookmark-property-ado.md">Bookmark</a></span><span class="sxs-lookup"><span data-stu-id="5834b-292"><a href="bookmark-property-ado.md">Bookmark</a></span></span></p></td>
<td><p><span data-ttu-id="5834b-293">使用不可</span><span class="sxs-lookup"><span data-stu-id="5834b-293">not available</span></span></p></td>
<td><p><span data-ttu-id="5834b-294">使用不可</span><span class="sxs-lookup"><span data-stu-id="5834b-294">not available</span></span></p></td>
<td><p><span data-ttu-id="5834b-295">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-295">read/write</span></span></p></td>
<td><p><span data-ttu-id="5834b-296">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-296">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-297"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="5834b-297"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="5834b-298">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-298">read/write</span></span></p></td>
<td><p><span data-ttu-id="5834b-299">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-299">read/write</span></span></p></td>
<td><p><span data-ttu-id="5834b-300">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-300">read/write</span></span></p></td>
<td><p><span data-ttu-id="5834b-301">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-301">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-302"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="5834b-302"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="5834b-303">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-303">read/write</span></span></p></td>
<td><p><span data-ttu-id="5834b-304">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-304">read/write</span></span></p></td>
<td><p><span data-ttu-id="5834b-305">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-305">read/write</span></span></p></td>
<td><p><span data-ttu-id="5834b-306">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-306">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-307"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="5834b-307"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="5834b-308">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-308">read/write</span></span></p></td>
<td><p><span data-ttu-id="5834b-309">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-309">read/write</span></span></p></td>
<td><p><span data-ttu-id="5834b-310">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-310">read/write</span></span></p></td>
<td><p><span data-ttu-id="5834b-311">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-311">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-312"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="5834b-312"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="5834b-313">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="5834b-313">read-only</span></span></p></td>
<td><p><span data-ttu-id="5834b-314">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="5834b-314">read-only</span></span></p></td>
<td><p><span data-ttu-id="5834b-315">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="5834b-315">read-only</span></span></p></td>
<td><p><span data-ttu-id="5834b-316">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="5834b-316">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-317"><a href="filter-property-ado.md">Filter</a></span><span class="sxs-lookup"><span data-stu-id="5834b-317"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="5834b-318">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-318">read/write</span></span></p></td>
<td><p><span data-ttu-id="5834b-319">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-319">read/write</span></span></p></td>
<td><p><span data-ttu-id="5834b-320">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-320">read/write</span></span></p></td>
<td><p><span data-ttu-id="5834b-321">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-321">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-322"><a href="locktype-property-ado.md">LockType</a></span><span class="sxs-lookup"><span data-stu-id="5834b-322"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="5834b-323">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-323">read/write</span></span></p></td>
<td><p><span data-ttu-id="5834b-324">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-324">read/write</span></span></p></td>
<td><p><span data-ttu-id="5834b-325">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-325">read/write</span></span></p></td>
<td><p><span data-ttu-id="5834b-326">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-326">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-327"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span><span class="sxs-lookup"><span data-stu-id="5834b-327"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="5834b-328">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-328">read/write</span></span></p></td>
<td><p><span data-ttu-id="5834b-329">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-329">read/write</span></span></p></td>
<td><p><span data-ttu-id="5834b-330">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-330">read/write</span></span></p></td>
<td><p><span data-ttu-id="5834b-331">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-331">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-332"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="5834b-332"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="5834b-333">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-333">read/write</span></span></p></td>
<td><p><span data-ttu-id="5834b-334">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-334">read/write</span></span></p></td>
<td><p><span data-ttu-id="5834b-335">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-335">read/write</span></span></p></td>
<td><p><span data-ttu-id="5834b-336">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-336">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-337"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="5834b-337"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="5834b-338">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-338">read/write</span></span></p></td>
<td><p><span data-ttu-id="5834b-339">利用不可</span><span class="sxs-lookup"><span data-stu-id="5834b-339">not available</span></span></p></td>
<td><p><span data-ttu-id="5834b-340">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="5834b-340">read-only</span></span></p></td>
<td><p><span data-ttu-id="5834b-341">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="5834b-341">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-342"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="5834b-342"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="5834b-343">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-343">read/write</span></span></p></td>
<td><p><span data-ttu-id="5834b-344">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-344">read/write</span></span></p></td>
<td><p><span data-ttu-id="5834b-345">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-345">read/write</span></span></p></td>
<td><p><span data-ttu-id="5834b-346">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-346">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-347"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="5834b-347"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="5834b-348">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-348">read/write</span></span></p></td>
<td><p><span data-ttu-id="5834b-349">利用不可</span><span class="sxs-lookup"><span data-stu-id="5834b-349">not available</span></span></p></td>
<td><p><span data-ttu-id="5834b-350">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="5834b-350">read-only</span></span></p></td>
<td><p><span data-ttu-id="5834b-351">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="5834b-351">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-352"><a href="source-property-ado-recordset.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="5834b-352"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="5834b-353">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-353">read/write</span></span></p></td>
<td><p><span data-ttu-id="5834b-354">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-354">read/write</span></span></p></td>
<td><p><span data-ttu-id="5834b-355">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-355">read/write</span></span></p></td>
<td><p><span data-ttu-id="5834b-356">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5834b-356">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-357"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="5834b-357"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="5834b-358">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="5834b-358">read-only</span></span></p></td>
<td><p><span data-ttu-id="5834b-359">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="5834b-359">read-only</span></span></p></td>
<td><p><span data-ttu-id="5834b-360">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="5834b-360">read-only</span></span></p></td>
<td><p><span data-ttu-id="5834b-361">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="5834b-361">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-362"><a href="status-property-ado-recordset.md">状態</a></span><span class="sxs-lookup"><span data-stu-id="5834b-362"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="5834b-363">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="5834b-363">read-only</span></span></p></td>
<td><p><span data-ttu-id="5834b-364">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="5834b-364">read-only</span></span></p></td>
<td><p><span data-ttu-id="5834b-365">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="5834b-365">read-only</span></span></p></td>
<td><p><span data-ttu-id="5834b-366">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="5834b-366">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5834b-367">バージョン 1.0 の Microsoft OLE DB Provider for ODBC で ADO を使用する場合、[AbsolutePosition](absoluteposition-property-ado.md) プロパティと [AbsolutePage](absolutepage-property-ado.md) プロパティは値の設定のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="5834b-367">The [AbsolutePosition](absoluteposition-property-ado.md) and [AbsolutePage](absolutepage-property-ado.md) properties are write-only when ADO is used with version 1.0 of the Microsoft OLE DB Provider for ODBC.</span></span>

<span data-ttu-id="5834b-368">標準的な ADO **Recordset** のメソッドの利用可能性は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="5834b-368">Availability of standard ADO **Recordset** methods:</span></span>

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
<th><p><span data-ttu-id="5834b-369">メソッド</span><span class="sxs-lookup"><span data-stu-id="5834b-369">Method</span></span></p></th>
<th><p><span data-ttu-id="5834b-370">ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="5834b-370">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="5834b-371">Dynamic</span><span class="sxs-lookup"><span data-stu-id="5834b-371">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="5834b-372">Keyset</span><span class="sxs-lookup"><span data-stu-id="5834b-372">Keyset</span></span></p></th>
<th><p><span data-ttu-id="5834b-373">Static</span><span class="sxs-lookup"><span data-stu-id="5834b-373">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5834b-374"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="5834b-374"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="5834b-375">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-375">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-376">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-376">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-377">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-377">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-378">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-378">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-379"><a href="cancel-method-ado.md">Cancel</a></span><span class="sxs-lookup"><span data-stu-id="5834b-379"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="5834b-380">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-380">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-381">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-381">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-382">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-382">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-383">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-383">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-384"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="5834b-384"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="5834b-385">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-385">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-386">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-386">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-387">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-387">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-388">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-388">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-389"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="5834b-389"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="5834b-390">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-390">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-391">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-391">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-392">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-392">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-393">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-393">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-394"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="5834b-394"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="5834b-395">いいえ</span><span class="sxs-lookup"><span data-stu-id="5834b-395">No</span></span></p></td>
<td><p><span data-ttu-id="5834b-396">いいえ</span><span class="sxs-lookup"><span data-stu-id="5834b-396">No</span></span></p></td>
<td><p><span data-ttu-id="5834b-397">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-397">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-398">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-398">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-399"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="5834b-399"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="5834b-400">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-400">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-401">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-401">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-402">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-402">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-403">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-403">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-404"><a href="delete-method-ado-recordset.md">Delete</a></span><span class="sxs-lookup"><span data-stu-id="5834b-404"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="5834b-405">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-405">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-406">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-406">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-407">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-407">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-408">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-408">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-409"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="5834b-409"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="5834b-410">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-410">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-411">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-411">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-412">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-412">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-413">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-413">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-414"><a href="move-method-ado.md">Move</a></span><span class="sxs-lookup"><span data-stu-id="5834b-414"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="5834b-415">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-415">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-416">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-416">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-417">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-417">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-418">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-418">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-419"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="5834b-419"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="5834b-420">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-420">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-421">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-421">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-422">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-422">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-423">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-423">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-424"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span><span class="sxs-lookup"><span data-stu-id="5834b-424"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span></span></p></td>
<td><p><span data-ttu-id="5834b-425">いいえ</span><span class="sxs-lookup"><span data-stu-id="5834b-425">No</span></span></p></td>
<td><p><span data-ttu-id="5834b-426">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-426">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-427">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-427">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-428">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-428">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-429"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span><span class="sxs-lookup"><span data-stu-id="5834b-429"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span></span></p></td>
<td><p><span data-ttu-id="5834b-430">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-430">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-431">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-431">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-432">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-432">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-433">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-433">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-434"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="5834b-434"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="5834b-435">いいえ</span><span class="sxs-lookup"><span data-stu-id="5834b-435">No</span></span></p></td>
<td><p><span data-ttu-id="5834b-436">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-436">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-437">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-437">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-438">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-438">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-439"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span><span class="sxs-lookup"><span data-stu-id="5834b-439"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span></span></p></td>
<td><p><span data-ttu-id="5834b-440">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-440">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-441">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-441">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-442">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-442">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-443">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-443">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-444"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="5834b-444"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="5834b-445">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-445">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-446">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-446">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-447">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-447">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-448">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-448">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-449"><a href="requery-method-ado.md">Requery</a></span><span class="sxs-lookup"><span data-stu-id="5834b-449"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="5834b-450">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-450">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-451">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-451">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-452">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-452">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-453">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-453">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-454"><a href="resync-method-ado.md">Resync</a></span><span class="sxs-lookup"><span data-stu-id="5834b-454"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="5834b-455">いいえ</span><span class="sxs-lookup"><span data-stu-id="5834b-455">No</span></span></p></td>
<td><p><span data-ttu-id="5834b-456">いいえ</span><span class="sxs-lookup"><span data-stu-id="5834b-456">No</span></span></p></td>
<td><p><span data-ttu-id="5834b-457">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-457">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-458">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-458">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-459"><a href="supports-method-ado.md">機能</a></span><span class="sxs-lookup"><span data-stu-id="5834b-459"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="5834b-460">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-460">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-461">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-461">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-462">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-462">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-463">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-463">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-464"><a href="update-method-ado.md">Update</a></span><span class="sxs-lookup"><span data-stu-id="5834b-464"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="5834b-465">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-465">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-466">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-466">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-467">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-467">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-468">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-468">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-469"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="5834b-469"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="5834b-470">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-470">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-471">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-471">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-472">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-472">Yes</span></span></p></td>
<td><p><span data-ttu-id="5834b-473">はい</span><span class="sxs-lookup"><span data-stu-id="5834b-473">Yes</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5834b-474">\*Microsoft Access データベースではサポートされません。</span><span class="sxs-lookup"><span data-stu-id="5834b-474">\*Not supported for Microsoft Access databases.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="5834b-475">動的プロパティ</span><span class="sxs-lookup"><span data-stu-id="5834b-475">Dynamic Properties</span></span>

<span data-ttu-id="5834b-476">Microsoft OLE DB Provider for ODBC は、開かれていない [Connection](connection-object-ado.md) オブジェクト、[Recordset](recordset-object-ado.md) オブジェクト、および [Command](command-object-ado.md) オブジェクトの **Properties** コレクションに動的プロパティを挿入します。</span><span class="sxs-lookup"><span data-stu-id="5834b-476">The Microsoft OLE DB Provider for ODBC inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="5834b-p118">以下の表は、各動的プロパティの ADO 名と OLE DB 名の対応表です。 「OLE DB プログラマ リファレンス」では、「説明」欄に ADO プロパティ名が示されています。プロパティの詳細については、「OLE DB プログラマ リファレンス」を参照してください。OLE DB プロパティ名をキーワードとして検索するか、「付録 C: プロパティ表」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5834b-p118">The tables below are a cross-index of the ADO and OLE DB names for each dynamic property. The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description." You can find more information about these properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="5834b-481">Connection の動的プロパティ</span><span class="sxs-lookup"><span data-stu-id="5834b-481">Connection Dynamic Properties</span></span>

<span data-ttu-id="5834b-482">次に示すプロパティが **Connection** オブジェクトの **Properties** コレクションに追加されます。</span><span class="sxs-lookup"><span data-stu-id="5834b-482">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5834b-483">ADO プロパティ名</span><span class="sxs-lookup"><span data-stu-id="5834b-483">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="5834b-484">OLE DB プロパティ名</span><span class="sxs-lookup"><span data-stu-id="5834b-484">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5834b-485">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="5834b-485">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="5834b-486">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="5834b-486">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-487">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="5834b-487">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="5834b-488">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="5834b-488">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-489">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="5834b-489">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="5834b-490">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="5834b-490">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-491">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="5834b-491">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="5834b-492">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="5834b-492">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-493">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="5834b-493">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="5834b-494">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="5834b-494">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-495">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="5834b-495">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="5834b-496">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="5834b-496">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-497">Column Definition</span><span class="sxs-lookup"><span data-stu-id="5834b-497">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="5834b-498">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="5834b-498">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-499">Connect Timeout</span><span class="sxs-lookup"><span data-stu-id="5834b-499">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="5834b-500">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="5834b-500">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-501">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="5834b-501">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="5834b-502">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="5834b-502">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-503">Data Source</span><span class="sxs-lookup"><span data-stu-id="5834b-503">Data Source</span></span></p></td>
<td><p><span data-ttu-id="5834b-504">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="5834b-504">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-505">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="5834b-505">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="5834b-506">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="5834b-506">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-507">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="5834b-507">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="5834b-508">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="5834b-508">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-509">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="5834b-509">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="5834b-510">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="5834b-510">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-511">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="5834b-511">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="5834b-512">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="5834b-512">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-513">Extended Properties</span><span class="sxs-lookup"><span data-stu-id="5834b-513">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="5834b-514">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="5834b-514">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-515">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="5834b-515">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="5834b-516">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="5834b-516">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-517">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="5834b-517">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="5834b-518">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="5834b-518">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-519">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="5834b-519">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="5834b-520">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="5834b-520">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-521">Initial Catalog</span><span class="sxs-lookup"><span data-stu-id="5834b-521">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="5834b-522">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="5834b-522">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-523">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="5834b-523">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="5834b-524">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="5834b-524">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-525">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="5834b-525">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="5834b-526">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="5834b-526">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-527">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="5834b-527">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="5834b-528">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="5834b-528">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-529">場所</span><span class="sxs-lookup"><span data-stu-id="5834b-529">Location</span></span></p></td>
<td><p><span data-ttu-id="5834b-530">DBPROP_INIT_LOCATION</span><span class="sxs-lookup"><span data-stu-id="5834b-530">DBPROP_INIT_LOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-531">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="5834b-531">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="5834b-532">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="5834b-532">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-533">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="5834b-533">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="5834b-534">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="5834b-534">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-535">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="5834b-535">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="5834b-536">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="5834b-536">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-537">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="5834b-537">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="5834b-538">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="5834b-538">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-539">Mode</span><span class="sxs-lookup"><span data-stu-id="5834b-539">Mode</span></span></p></td>
<td><p><span data-ttu-id="5834b-540">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="5834b-540">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-541">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="5834b-541">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="5834b-542">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="5834b-542">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-543">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="5834b-543">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="5834b-544">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="5834b-544">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-545">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="5834b-545">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="5834b-546">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="5834b-546">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-547">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="5834b-547">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="5834b-548">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="5834b-548">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-549">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="5834b-549">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="5834b-550">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="5834b-550">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-551">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="5834b-551">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="5834b-552">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="5834b-552">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-553">OLE DB Services</span><span class="sxs-lookup"><span data-stu-id="5834b-553">OLE DB Services</span></span></p></td>
<td><p><span data-ttu-id="5834b-554">DBPROP_INIT_OLEDBSERVICES</span><span class="sxs-lookup"><span data-stu-id="5834b-554">DBPROP_INIT_OLEDBSERVICES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-555">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="5834b-555">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="5834b-556">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="5834b-556">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-557">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="5834b-557">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="5834b-558">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="5834b-558">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-559">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="5834b-559">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="5834b-560">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="5834b-560">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-561">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="5834b-561">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="5834b-562">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="5834b-562">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-563">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="5834b-563">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="5834b-564">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="5834b-564">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-565">Password</span><span class="sxs-lookup"><span data-stu-id="5834b-565">Password</span></span></p></td>
<td><p><span data-ttu-id="5834b-566">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="5834b-566">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-567">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="5834b-567">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="5834b-568">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="5834b-568">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-569">Persist Security Info</span><span class="sxs-lookup"><span data-stu-id="5834b-569">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="5834b-570">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="5834b-570">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-571">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="5834b-571">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="5834b-572">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="5834b-572">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-573">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="5834b-573">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="5834b-574">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="5834b-574">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-575">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="5834b-575">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="5834b-576">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="5834b-576">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-577">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="5834b-577">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="5834b-578">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="5834b-578">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-579">Prompt</span><span class="sxs-lookup"><span data-stu-id="5834b-579">Prompt</span></span></p></td>
<td><p><span data-ttu-id="5834b-580">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="5834b-580">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-581">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="5834b-581">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="5834b-582">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="5834b-582">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-583">Provider Name</span><span class="sxs-lookup"><span data-stu-id="5834b-583">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="5834b-584">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="5834b-584">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-585">Provider Version</span><span class="sxs-lookup"><span data-stu-id="5834b-585">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="5834b-586">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="5834b-586">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-587">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="5834b-587">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="5834b-588">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="5834b-588">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-589">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="5834b-589">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="5834b-590">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="5834b-590">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-591">Schema Term</span><span class="sxs-lookup"><span data-stu-id="5834b-591">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="5834b-592">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="5834b-592">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-593">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="5834b-593">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="5834b-594">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="5834b-594">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-595">SQL Support</span><span class="sxs-lookup"><span data-stu-id="5834b-595">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="5834b-596">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="5834b-596">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-597">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="5834b-597">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="5834b-598">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="5834b-598">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-599">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="5834b-599">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="5834b-600">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="5834b-600">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-601">Table Term</span><span class="sxs-lookup"><span data-stu-id="5834b-601">Table Term</span></span></p></td>
<td><p><span data-ttu-id="5834b-602">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="5834b-602">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-603">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="5834b-603">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="5834b-604">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="5834b-604">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-605">User ID</span><span class="sxs-lookup"><span data-stu-id="5834b-605">User ID</span></span></p></td>
<td><p><span data-ttu-id="5834b-606">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="5834b-606">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-607">User Name</span><span class="sxs-lookup"><span data-stu-id="5834b-607">User Name</span></span></p></td>
<td><p><span data-ttu-id="5834b-608">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="5834b-608">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-609">Window Handle</span><span class="sxs-lookup"><span data-stu-id="5834b-609">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="5834b-610">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="5834b-610">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="5834b-611">Recordset の動的プロパティ</span><span class="sxs-lookup"><span data-stu-id="5834b-611">Recordset Dynamic Properties</span></span>

<span data-ttu-id="5834b-612">次に示すプロパティが **Recordset** オブジェクトの **Properties** コレクションに追加されます。</span><span class="sxs-lookup"><span data-stu-id="5834b-612">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5834b-613">ADO プロパティ名</span><span class="sxs-lookup"><span data-stu-id="5834b-613">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="5834b-614">OLE DB プロパティ名</span><span class="sxs-lookup"><span data-stu-id="5834b-614">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5834b-615">Access Order</span><span class="sxs-lookup"><span data-stu-id="5834b-615">Access Order</span></span></p></td>
<td><p><span data-ttu-id="5834b-616">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="5834b-616">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-617">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="5834b-617">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="5834b-618">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="5834b-618">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-619">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="5834b-619">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="5834b-620">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="5834b-620">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-621">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="5834b-621">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="5834b-622">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="5834b-622">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-623">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="5834b-623">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="5834b-624">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="5834b-624">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-625">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="5834b-625">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="5834b-626">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="5834b-626">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-627">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="5834b-627">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="5834b-628">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="5834b-628">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-629">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="5834b-629">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="5834b-630">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="5834b-630">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-631">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="5834b-631">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="5834b-632">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="5834b-632">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-633">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="5834b-633">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="5834b-634">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="5834b-634">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-635">IAccessor</span><span class="sxs-lookup"><span data-stu-id="5834b-635">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="5834b-636">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="5834b-636">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-637">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="5834b-637">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="5834b-638">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="5834b-638">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-639">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="5834b-639">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="5834b-640">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="5834b-640">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-641">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="5834b-641">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="5834b-642">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="5834b-642">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-643">iconverttype</span><span class="sxs-lookup"><span data-stu-id="5834b-643">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="5834b-644">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="5834b-644">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-645">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="5834b-645">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="5834b-646">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="5834b-646">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-647">IRowset</span><span class="sxs-lookup"><span data-stu-id="5834b-647">IRowset</span></span></p></td>
<td><p><span data-ttu-id="5834b-648">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="5834b-648">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-649">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="5834b-649">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="5834b-650">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="5834b-650">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-651">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="5834b-651">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="5834b-652">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="5834b-652">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-653">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="5834b-653">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="5834b-654">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="5834b-654">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-655">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="5834b-655">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="5834b-656">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="5834b-656">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-657">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="5834b-657">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-658">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="5834b-658">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="5834b-659">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="5834b-659">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-660">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="5834b-660">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="5834b-661">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="5834b-661">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-662">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="5834b-662">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="5834b-663">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="5834b-663">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-664">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="5834b-664">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="5834b-665">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="5834b-665">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-666">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="5834b-666">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="5834b-667">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="5834b-667">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-668">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="5834b-668">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="5834b-669">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="5834b-669">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-670">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="5834b-670">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="5834b-671">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="5834b-671">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-672">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="5834b-672">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="5834b-673">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="5834b-673">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-674">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="5834b-674">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="5834b-675">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="5834b-675">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-676">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="5834b-676">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="5834b-677">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="5834b-677">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-678">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="5834b-678">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="5834b-679">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="5834b-679">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-680">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="5834b-680">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="5834b-681">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="5834b-681">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-682">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="5834b-682">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="5834b-683">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="5834b-683">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-684">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="5834b-684">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="5834b-685">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="5834b-685">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-686">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="5834b-686">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="5834b-687">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="5834b-687">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-688">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="5834b-688">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="5834b-689">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="5834b-689">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-690">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="5834b-690">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="5834b-691">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="5834b-691">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-692">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="5834b-692">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="5834b-693">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="5834b-693">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-694">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="5834b-694">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="5834b-695">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="5834b-695">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-696">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="5834b-696">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="5834b-697">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="5834b-697">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-698">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="5834b-698">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="5834b-699">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="5834b-699">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-700">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="5834b-700">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="5834b-701">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="5834b-701">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-702">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="5834b-702">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="5834b-703">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="5834b-703">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-704">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="5834b-704">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="5834b-705">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="5834b-705">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-706">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="5834b-706">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="5834b-707">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="5834b-707">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-708">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="5834b-708">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="5834b-709">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="5834b-709">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-710">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="5834b-710">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="5834b-711">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="5834b-711">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-712">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="5834b-712">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="5834b-713">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="5834b-713">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-714">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="5834b-714">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="5834b-715">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="5834b-715">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-716">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="5834b-716">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="5834b-717">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="5834b-717">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-718">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="5834b-718">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="5834b-719">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="5834b-719">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-720">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="5834b-720">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="5834b-721">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="5834b-721">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-722">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="5834b-722">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="5834b-723">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="5834b-723">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-724">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="5834b-724">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="5834b-725">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="5834b-725">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-726">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="5834b-726">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="5834b-727">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="5834b-727">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-728">Unique Rows</span><span class="sxs-lookup"><span data-stu-id="5834b-728">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="5834b-729">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="5834b-729">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-730">Updatability</span><span class="sxs-lookup"><span data-stu-id="5834b-730">Updatability</span></span></p></td>
<td><p><span data-ttu-id="5834b-731">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="5834b-731">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-732">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="5834b-732">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="5834b-733">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="5834b-733">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="5834b-734">Command の動的プロパティ</span><span class="sxs-lookup"><span data-stu-id="5834b-734">Command Dynamic Properties</span></span>

<span data-ttu-id="5834b-735">次に示すプロパティが **Command** オブジェクトの **Properties** コレクションに追加されます。</span><span class="sxs-lookup"><span data-stu-id="5834b-735">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5834b-736">ADO プロパティ名</span><span class="sxs-lookup"><span data-stu-id="5834b-736">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="5834b-737">OLE DB プロパティ名</span><span class="sxs-lookup"><span data-stu-id="5834b-737">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5834b-738">Access Order</span><span class="sxs-lookup"><span data-stu-id="5834b-738">Access Order</span></span></p></td>
<td><p><span data-ttu-id="5834b-739">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="5834b-739">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-740">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="5834b-740">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="5834b-741">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="5834b-741">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-742">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="5834b-742">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="5834b-743">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="5834b-743">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-744">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="5834b-744">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="5834b-745">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="5834b-745">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-746">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="5834b-746">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="5834b-747">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="5834b-747">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-748">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="5834b-748">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="5834b-749">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="5834b-749">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-750">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="5834b-750">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="5834b-751">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="5834b-751">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-752">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="5834b-752">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="5834b-753">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="5834b-753">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-754">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="5834b-754">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="5834b-755">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="5834b-755">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-756">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="5834b-756">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="5834b-757">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="5834b-757">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-758">IAccessor</span><span class="sxs-lookup"><span data-stu-id="5834b-758">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="5834b-759">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="5834b-759">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-760">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="5834b-760">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="5834b-761">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="5834b-761">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-762">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="5834b-762">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="5834b-763">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="5834b-763">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-764">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="5834b-764">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="5834b-765">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="5834b-765">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-766">iconverttype</span><span class="sxs-lookup"><span data-stu-id="5834b-766">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="5834b-767">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="5834b-767">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-768">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="5834b-768">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="5834b-769">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="5834b-769">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-770">IRowset</span><span class="sxs-lookup"><span data-stu-id="5834b-770">IRowset</span></span></p></td>
<td><p><span data-ttu-id="5834b-771">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="5834b-771">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-772">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="5834b-772">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="5834b-773">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="5834b-773">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-774">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="5834b-774">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="5834b-775">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="5834b-775">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-776">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="5834b-776">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="5834b-777">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="5834b-777">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-778">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="5834b-778">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="5834b-779">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="5834b-779">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-780">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="5834b-780">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-781">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="5834b-781">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="5834b-782">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="5834b-782">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-783">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="5834b-783">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="5834b-784">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="5834b-784">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-785">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="5834b-785">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="5834b-786">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="5834b-786">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-787">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="5834b-787">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="5834b-788">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="5834b-788">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-789">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="5834b-789">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="5834b-790">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="5834b-790">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-791">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="5834b-791">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="5834b-792">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="5834b-792">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-793">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="5834b-793">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="5834b-794">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="5834b-794">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-795">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="5834b-795">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="5834b-796">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="5834b-796">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-797">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="5834b-797">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="5834b-798">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="5834b-798">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-799">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="5834b-799">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="5834b-800">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="5834b-800">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-801">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="5834b-801">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="5834b-802">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="5834b-802">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-803">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="5834b-803">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="5834b-804">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="5834b-804">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-805">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="5834b-805">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="5834b-806">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="5834b-806">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-807">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="5834b-807">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="5834b-808">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="5834b-808">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-809">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="5834b-809">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="5834b-810">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="5834b-810">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-811">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="5834b-811">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="5834b-812">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="5834b-812">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-813">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="5834b-813">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="5834b-814">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="5834b-814">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-815">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="5834b-815">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="5834b-816">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="5834b-816">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-817">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="5834b-817">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="5834b-818">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="5834b-818">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-819">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="5834b-819">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="5834b-820">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="5834b-820">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-821">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="5834b-821">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="5834b-822">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="5834b-822">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-823">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="5834b-823">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="5834b-824">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="5834b-824">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-825">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="5834b-825">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="5834b-826">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="5834b-826">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-827">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="5834b-827">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="5834b-828">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="5834b-828">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-829">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="5834b-829">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="5834b-830">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="5834b-830">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-831">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="5834b-831">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="5834b-832">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="5834b-832">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-833">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="5834b-833">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="5834b-834">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="5834b-834">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-835">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="5834b-835">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="5834b-836">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="5834b-836">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-837">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="5834b-837">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="5834b-838">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="5834b-838">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-839">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="5834b-839">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="5834b-840">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="5834b-840">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-841">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="5834b-841">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="5834b-842">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="5834b-842">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-843">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="5834b-843">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="5834b-844">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="5834b-844">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-845">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="5834b-845">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="5834b-846">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="5834b-846">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-847">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="5834b-847">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="5834b-848">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="5834b-848">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-849">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="5834b-849">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="5834b-850">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="5834b-850">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5834b-851">Updatability</span><span class="sxs-lookup"><span data-stu-id="5834b-851">Updatability</span></span></p></td>
<td><p><span data-ttu-id="5834b-852">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="5834b-852">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5834b-853">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="5834b-853">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="5834b-854">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="5834b-854">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="5834b-855">関連項目</span><span class="sxs-lookup"><span data-stu-id="5834b-855">See also</span></span>

<span data-ttu-id="5834b-856">Microsoft ole db Provider for ODBC に関する特定の実装と機能に関する情報については、「 [OLE db プログラマガイド」](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85))または「[データプラットフォームデベロッパーセンター](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5834b-856">For details regarding specific implementation and functional information about the Microsoft OLE DB Provider for ODBC, consult the [OLE DB Programmer's Guide](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) or visit the [Data Platform Developer Center](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span></span>

