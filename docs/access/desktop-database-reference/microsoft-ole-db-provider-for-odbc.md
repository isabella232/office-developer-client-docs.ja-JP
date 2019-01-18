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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704561"
---
# <a name="microsoft-ole-db-provider-for-odbc"></a><span data-ttu-id="ea36a-102">Microsoft OLE DB Provider for ODBC</span><span class="sxs-lookup"><span data-stu-id="ea36a-102">Microsoft OLE DB Provider for ODBC</span></span>

<span data-ttu-id="ea36a-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="ea36a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ea36a-p101">ADO または RDS のプログラマにとって、すべてのデータ ソースで OLE DB インターフェイスが公開され、ADO で直接データ ソースを呼び出すことができるのが理想的です。OLE DB インターフェイスを実装するデータベース ベンダーは増えていますが、まだこのインターフェイスを公開していないデータ ソースもあります。ただし、現在使用されている事実上すべての DBMS システムは、ODBC によるアクセスが可能です。</span><span class="sxs-lookup"><span data-stu-id="ea36a-p101">To an ADO or RDS programmer, an ideal world would be one in which every data source exposes an OLE DB interface, so that ADO could call directly into the data source. Although increasingly more database vendors are implementing OLE DB interfaces, some data sources are not yet exposed this way. However, virtually all DBMS systems in use today can be accessed through ODBC.</span></span>

<span data-ttu-id="ea36a-107">ODBC ドライバーは、Microsoft SQL Server、Microsoft Access (Microsoft Jet データベース エンジン)、および Microsoft FoxPro だけでなく、Oracle などの Microsoft 以外のデータベース製品を含めた、現在使用されているすべての主要 DBMS で使用できます。</span><span class="sxs-lookup"><span data-stu-id="ea36a-107">ODBC drivers are available for every major DBMS in use today, including Microsoft SQL Server, Microsoft Access (Microsoft Jet database engine), and Microsoft FoxPro, in addition to non-Microsoft database products such as Oracle.</span></span>

<span data-ttu-id="ea36a-p102">ただし、Microsoft ODBC Provider を使用すると、ADO からすべての ODBC データ ソースに接続できます。このプロバイダーはフリースレッドであり、Unicode に対応しています。</span><span class="sxs-lookup"><span data-stu-id="ea36a-p102">The Microsoft ODBC Provider, however, allows ADO to connect to any ODBC data source. The provider is free-threaded and Unicode enabled.</span></span>

<span data-ttu-id="ea36a-p103">このプロバイダーはトランザクションをサポートしていますが、DBMS エンジンの種類によって、サポートするトランザクションの種類が異なります。たとえば、Microsoft Access は 5 レベルまでのネストされたトランザクションをサポートします。</span><span class="sxs-lookup"><span data-stu-id="ea36a-p103">The provider supports transactions, although different DBMS engines offer different types of transaction support. For example, Microsoft Access supports nested transactions up to five levels deep.</span></span>

<span data-ttu-id="ea36a-112">このプロバイダーは ADO の既定のプロバイダーであり、プロバイダーに依存するすべての ADO プロパティおよびメソッドをサポートします。</span><span class="sxs-lookup"><span data-stu-id="ea36a-112">This is the default provider for ADO, and all provider-dependent ADO properties and methods are supported.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="ea36a-113">接続文字列パラメーター</span><span class="sxs-lookup"><span data-stu-id="ea36a-113">Connection String Parameters</span></span>

<span data-ttu-id="ea36a-114">このプロバイダーに接続するには、**ConnectionString** プロパティの [Provider=](connectionstring-property-ado.md) 引数を次のように設定します。</span><span class="sxs-lookup"><span data-stu-id="ea36a-114">To connect to this provider, set the **Provider=** argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```sql 
 
MSDASQL 
```

<span data-ttu-id="ea36a-115">[Provider](provider-property-ado.md) プロパティを取得した場合も、この文字列が返されます。</span><span class="sxs-lookup"><span data-stu-id="ea36a-115">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="ea36a-116">標準的な接続文字列</span><span class="sxs-lookup"><span data-stu-id="ea36a-116">Typical Connection String</span></span>

<span data-ttu-id="ea36a-117">このプロバイダーの標準的な接続文字列を次に示します。</span><span class="sxs-lookup"><span data-stu-id="ea36a-117">A typical connection string for this provider is:</span></span>

```sql 
 
"Provider=MSDASQL;DSN=dsnName;UID=userName;PWD=userPassword;" 
```

<span data-ttu-id="ea36a-118">この文字列は、次に示すキーワードで構成されています。</span><span class="sxs-lookup"><span data-stu-id="ea36a-118">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ea36a-119">キーワード</span><span class="sxs-lookup"><span data-stu-id="ea36a-119">Keyword</span></span></p></th>
<th><p><span data-ttu-id="ea36a-120">説明</span><span class="sxs-lookup"><span data-stu-id="ea36a-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-121"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="ea36a-121"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="ea36a-122">OLE DB Provider for ODBC を指定します。</span><span class="sxs-lookup"><span data-stu-id="ea36a-122">Specifies the OLE DB Provider for ODBC.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-123"><strong>DSN</strong></span><span class="sxs-lookup"><span data-stu-id="ea36a-123"><strong>DSN</strong></span></span></p></td>
<td><p><span data-ttu-id="ea36a-124">データ ソース名を指定します。</span><span class="sxs-lookup"><span data-stu-id="ea36a-124">Specifies the data source name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-125"><strong>UID</strong></span><span class="sxs-lookup"><span data-stu-id="ea36a-125"><strong>UID</strong></span></span></p></td>
<td><p><span data-ttu-id="ea36a-126">ユーザー名を指定します。</span><span class="sxs-lookup"><span data-stu-id="ea36a-126">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-127"><strong>PWD</strong></span><span class="sxs-lookup"><span data-stu-id="ea36a-127"><strong>PWD</strong></span></span></p></td>
<td><p><span data-ttu-id="ea36a-128">ユーザー パスワードを指定します。</span><span class="sxs-lookup"><span data-stu-id="ea36a-128">Specifies the user password.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-129"><strong>URL</strong></span><span class="sxs-lookup"><span data-stu-id="ea36a-129"><strong>URL</strong></span></span></p></td>
<td><p><span data-ttu-id="ea36a-130">ファイルまたは web フォルダーで公開されているディレクトリの URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="ea36a-130">Specifies the URL of a file or directory published in a web folder.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ea36a-131">このプロバイダーは ADO の既定のプロバイダーであるため、接続文字列で **Provider=** パラメーターを省略すると、このプロバイダーへの接続の確立が試行されます。</span><span class="sxs-lookup"><span data-stu-id="ea36a-131">Because this is the default provider for ADO, if you omit the **Provider=** parameter from the connection string, ADO will attempt to establish a connection to this provider.</span></span>

<span data-ttu-id="ea36a-p104">このプロバイダーは、ADO で定義されたパラメーター以外に独自の接続パラメーターをサポートしません。ただし、ADO 以外の接続パラメーターが指定されている場合は、ODBC ドライバー マネージャーに渡します。</span><span class="sxs-lookup"><span data-stu-id="ea36a-p104">The provider does not support any specific connection parameters in addition to those defined by ADO. However, the provider will pass any non-ADO connection parameters to the ODBC driver manager.</span></span>

<span data-ttu-id="ea36a-p105">**Provider** パラメーターを省略できるので、同じデータ ソースに対して ODBC 接続文字列と同じ ADO 接続文字列を作成できます。ODBC 接続文字列を作成するときと同じパラメーター名 (**DRIVER=**、**DATABASE=**、**DSN=** など)、値、および構文を使用します。定義済みのデータ ソース名 (DSN) または FileDSN を指定してもしなくても接続できます。</span><span class="sxs-lookup"><span data-stu-id="ea36a-p105">Because you can omit the **Provider** parameter, you can therefore compose an ADO connection string that is identical to an ODBC connection string for the same data source. Use the same parameter names (**DRIVER=**, **DATABASE=**, **DSN=**, and so on), values, and syntax as you would when composing an ODBC connection string. You can connect with or without a predefined data source name (DSN) or FileDSN.</span></span>

<span data-ttu-id="ea36a-137">**DSN または FileDSN を指定する場合の構文:**</span><span class="sxs-lookup"><span data-stu-id="ea36a-137">**Syntax with a DSN or FileDSN:**</span></span>

`"[Provider=MSDASQL;] { DSN=name | FileDSN=filename } ; [DATABASE=database;] UID=user; PWD=password"`

<span data-ttu-id="ea36a-138">**DSN 指定しない場合の構文 (DSN なしの接続):**</span><span class="sxs-lookup"><span data-stu-id="ea36a-138">**Syntax without a DSN (DSN-less connection):**</span></span>

`"[Provider=MSDASQL;] DRIVER=driver; SERVER=server;DATABASE=database; UID=user; PWD=password"`

<span data-ttu-id="ea36a-139">**DSN**または**FileDSN**を使用する場合は Windows のコントロール パネルの [ODBC データ ソース アドミニストレーターを使用する必要があります定義します。</span><span class="sxs-lookup"><span data-stu-id="ea36a-139">If you use a **DSN** or **FileDSN**, it must be defined through the ODBC Data Source Administrator in the Windows Control Panel.</span></span> <span data-ttu-id="ea36a-140">Microsoft Windows 2000 では、odbc データ ソース アドミニストレーターは管理ツールの下にあります。</span><span class="sxs-lookup"><span data-stu-id="ea36a-140">In Microsoft Windows 2000, the ODBC Administrator is located under Administrative Tools.</span></span> <span data-ttu-id="ea36a-141">以前のバージョンの Windows では、odbc データ ソース アドミニストレーター アイコンは**32 ビット ODBC**または**ODBC**では単に呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="ea36a-141">In previous versions of Windows, the ODBC Administrator icon is named **32-bit ODBC** or simply **ODBC**.</span></span>

<span data-ttu-id="ea36a-142">**DSN** を設定する代わりに、"SQL Server" などの ODBC ドライバー (**DRIVER=**)、サーバー名 (**SERVER=**)、およびデータベース名 (**DATABASE=**) を指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="ea36a-142">As an alternative to setting a **DSN**, you can specify the ODBC driver (**DRIVER=**), such as "SQL Server;" the server name (**SERVER=**); and the database name (**DATABASE=**).</span></span>

<span data-ttu-id="ea36a-143">ユーザー アカウント名 (**UID=**) と、そのユーザー アカウントのパスワード (**PWD=**) を、ODBC 固有のパラメーターまたは ADO で定義された標準的な *user* パラメーターと *password* パラメーターで指定できます。</span><span class="sxs-lookup"><span data-stu-id="ea36a-143">You can also specify a user account name (**UID=**), and the password for the user account (**PWD=**) in the ODBC-specific parameters or in the standard ADO-defined *user* and *password* parameters.</span></span>

<span data-ttu-id="ea36a-144">**DSN**の定義が既にデータベースを指定して、*別のデータベースに接続する**DSN**に加えて*データベース*パラメーター*を指定できます。</span><span class="sxs-lookup"><span data-stu-id="ea36a-144">Although a **DSN** definition already specifies a database, you can specify *a* *database* parameter in addition to a **DSN** to connect to a different database.</span></span> <span data-ttu-id="ea36a-145">**DSN**を使用するときに常に\**データベース*パラメーター\*を含めることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ea36a-145">It is a good idea to always include *the* *database* parameter when you use a **DSN**.</span></span> <span data-ttu-id="ea36a-146">これは、ように**DSN**の定義を確認した後、他のユーザーがデータベースの既定のパラメーターを変更する適切なデータベースに接続すること。</span><span class="sxs-lookup"><span data-stu-id="ea36a-146">This will ensure that you connect to the proper database in the event that another user changed the default database parameter since you last checked the **DSN** definition.</span></span>

## <a name="provider-specific-connection-properties"></a><span data-ttu-id="ea36a-147">プロバイダー固有の Connection のプロパティ</span><span class="sxs-lookup"><span data-stu-id="ea36a-147">Provider-Specific Connection Properties</span></span>

<span data-ttu-id="ea36a-p108">OLE DB Provider for ODBC は、 [Connection](properties-collection-ado.md) オブジェクトの **Properties** コレクションにプロパティを追加します。次の表は、これらのプロパティの一覧で、かっこ内は対応する OLE DB プロパティ名です。</span><span class="sxs-lookup"><span data-stu-id="ea36a-p108">The OLE DB provider for ODBC adds several properties to the [Properties](properties-collection-ado.md) collection of the **Connection** object. The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ea36a-150">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="ea36a-150">Property Name</span></span></p></th>
<th><p><span data-ttu-id="ea36a-151">説明</span><span class="sxs-lookup"><span data-stu-id="ea36a-151">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-152">アクセス手順</span><span class="sxs-lookup"><span data-stu-id="ea36a-152">Accessible Procedures</span></span><br />
<span data-ttu-id="ea36a-153">(KAGPROP_ACCESSIBLEPROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="ea36a-153">(KAGPROP_ACCESSIBLEPROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="ea36a-154">ユーザーがストアド プロシージャにアクセスできるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="ea36a-154">Indicates whether the user has access to stored procedures.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-155">アクセス可能なテーブル</span><span class="sxs-lookup"><span data-stu-id="ea36a-155">Accessible Tables</span></span><br />
<span data-ttu-id="ea36a-156">(KAGPROP_ACCESSIBLETABLES)</span><span class="sxs-lookup"><span data-stu-id="ea36a-156">(KAGPROP_ACCESSIBLETABLES)</span></span></p></td>
<td><p><span data-ttu-id="ea36a-157">ユーザーがデータベースのテーブルに対して SELECT ステートメントを実行する権限を持つかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="ea36a-157">Indicates whether the user has permission to execute SELECT statements against the database tables.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-158">アクティブなステートメント</span><span class="sxs-lookup"><span data-stu-id="ea36a-158">Active Statements</span></span><br />
<span data-ttu-id="ea36a-159">(KAGPROP_ACTIVESTATEMENTS)</span><span class="sxs-lookup"><span data-stu-id="ea36a-159">(KAGPROP_ACTIVESTATEMENTS)</span></span></p></td>
<td><p><span data-ttu-id="ea36a-160">ODBC ドライバーが 1 つの接続でサポートできるハンドル数を示します。</span><span class="sxs-lookup"><span data-stu-id="ea36a-160">Indicates the number of handles an ODBC driver can support on a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-161">ドライバー名</span><span class="sxs-lookup"><span data-stu-id="ea36a-161">Driver Name</span></span><br />
<span data-ttu-id="ea36a-162">(KAGPROP_DRIVERNAME)</span><span class="sxs-lookup"><span data-stu-id="ea36a-162">(KAGPROP_DRIVERNAME)</span></span></p></td>
<td><p><span data-ttu-id="ea36a-163">ODBC ドライバーのファイル名を示します。</span><span class="sxs-lookup"><span data-stu-id="ea36a-163">Indicates the file name of the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-164">ドライバーの ODBC バージョン</span><span class="sxs-lookup"><span data-stu-id="ea36a-164">Driver ODBC Version</span></span><br />
<span data-ttu-id="ea36a-165">(KAGPROP_DRIVERODBCVER)</span><span class="sxs-lookup"><span data-stu-id="ea36a-165">(KAGPROP_DRIVERODBCVER)</span></span></p></td>
<td><p><span data-ttu-id="ea36a-166">このドライバーがサポートする ODBC のバージョンを示します。</span><span class="sxs-lookup"><span data-stu-id="ea36a-166">Indicates the version of ODBC that this driver supports.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-167">ファイルの使用状況</span><span class="sxs-lookup"><span data-stu-id="ea36a-167">File Usage</span></span><br />
<span data-ttu-id="ea36a-168">(KAGPROP_FILEUSAGE)</span><span class="sxs-lookup"><span data-stu-id="ea36a-168">(KAGPROP_FILEUSAGE)</span></span></p></td>
<td><p><span data-ttu-id="ea36a-169">ドライバーがデータ ソース内のファイルを、テーブルとして扱うか、カタログとして扱うかを示します。</span><span class="sxs-lookup"><span data-stu-id="ea36a-169">Indicates how the driver treats a file in a data source; as a table or as a catalog.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-170">エスケープ句のように</span><span class="sxs-lookup"><span data-stu-id="ea36a-170">Like Escape Clause</span></span><br />
<span data-ttu-id="ea36a-171">(KAGPROP_LIKEESCAPECLAUSE)</span><span class="sxs-lookup"><span data-stu-id="ea36a-171">(KAGPROP_LIKEESCAPECLAUSE)</span></span></p></td>
<td><p><span data-ttu-id="ea36a-172">ドライバーが、WHERE 句の LIKE 述語でパーセント記号 (%) および下線記号 (_) のエスケープ文字を定義および使用できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="ea36a-172">Indicates whether the driver supports the definition and use of an escape character for the percent character (%) and underline character (_) in the LIKE predicate of a WHERE clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-173">によるグループ内の最大列</span><span class="sxs-lookup"><span data-stu-id="ea36a-173">Max Columns in Group By</span></span><br />
<span data-ttu-id="ea36a-174">(KAGPROP_MAXCOLUMNSINGROUPBY)</span><span class="sxs-lookup"><span data-stu-id="ea36a-174">(KAGPROP_MAXCOLUMNSINGROUPBY)</span></span></p></td>
<td><p><span data-ttu-id="ea36a-175">SELECT ステートメントの GROUP BY 句に記述できる最大列数を示します。</span><span class="sxs-lookup"><span data-stu-id="ea36a-175">Indicates the maximum number of columns that can be listed in the GROUP BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-176">インデックスの最大列</span><span class="sxs-lookup"><span data-stu-id="ea36a-176">Max Columns in Index</span></span><br />
<span data-ttu-id="ea36a-177">(KAGPROP_MAXCOLUMNSININDEX)</span><span class="sxs-lookup"><span data-stu-id="ea36a-177">(KAGPROP_MAXCOLUMNSININDEX)</span></span></p></td>
<td><p><span data-ttu-id="ea36a-178">インデックスに格納できる最大列数を示します。</span><span class="sxs-lookup"><span data-stu-id="ea36a-178">Indicates the maximum number of columns that can be included in an index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-179">Order By の中の最大列</span><span class="sxs-lookup"><span data-stu-id="ea36a-179">Max Columns in Order By</span></span><br />
<span data-ttu-id="ea36a-180">(KAGPROP_MAXCOLUMNSINORDERBY)</span><span class="sxs-lookup"><span data-stu-id="ea36a-180">(KAGPROP_MAXCOLUMNSINORDERBY)</span></span></p></td>
<td><p><span data-ttu-id="ea36a-181">SELECT ステートメントの ORDER BY 句に記述できる最大列数を示します。</span><span class="sxs-lookup"><span data-stu-id="ea36a-181">Indicates the maximum number of columns that can be listed in the ORDER BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-182">選択中の最大列</span><span class="sxs-lookup"><span data-stu-id="ea36a-182">Max Columns in Select</span></span><br />
<span data-ttu-id="ea36a-183">(KAGPROP_MAXCOLUMNSINSELECT)</span><span class="sxs-lookup"><span data-stu-id="ea36a-183">(KAGPROP_MAXCOLUMNSINSELECT)</span></span></p></td>
<td><p><span data-ttu-id="ea36a-184">SELECT ステートメントの SELECT 部分に記述できる最大列数を示します。</span><span class="sxs-lookup"><span data-stu-id="ea36a-184">Indicates the maximum number of columns that can be listed in the SELECT portion of a SELECT statement.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-185">テーブルの最大列</span><span class="sxs-lookup"><span data-stu-id="ea36a-185">Max Columns in Table</span></span><br />
<span data-ttu-id="ea36a-186">(KAGPROP_MAXCOLUMNSINTABLE)</span><span class="sxs-lookup"><span data-stu-id="ea36a-186">(KAGPROP_MAXCOLUMNSINTABLE)</span></span></p></td>
<td><p><span data-ttu-id="ea36a-187">テーブルの最大列数を示します。</span><span class="sxs-lookup"><span data-stu-id="ea36a-187">Indicates the maximum number of columns allowed in a table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-188">数値を処理する関数</span><span class="sxs-lookup"><span data-stu-id="ea36a-188">Numeric Functions</span></span><br />
<span data-ttu-id="ea36a-189">(KAGPROP_NUMERICFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="ea36a-189">(KAGPROP_NUMERICFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="ea36a-p109">ODBC ドライバーがサポートする数値関数を示します。関数名とこのビットマスクで使用される関連付けられた値の一覧については、ODBC マニュアルの「Appendix E: Scalar Functions」 (英語) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ea36a-p109">Indicates which numeric functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-192">外部結合の機能</span><span class="sxs-lookup"><span data-stu-id="ea36a-192">Outer Join Capabilities</span></span><br />
<span data-ttu-id="ea36a-193">(KAGPROP_OJCAPABILITY)</span><span class="sxs-lookup"><span data-stu-id="ea36a-193">(KAGPROP_OJCAPABILITY)</span></span></p></td>
<td><p><span data-ttu-id="ea36a-194">プロバイダーがサポートする OUTER JOIN の種類を示します。</span><span class="sxs-lookup"><span data-stu-id="ea36a-194">Indicates the types of OUTER JOINs supported by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-195">外部結合</span><span class="sxs-lookup"><span data-stu-id="ea36a-195">Outer Joins</span></span><br />
<span data-ttu-id="ea36a-196">(KAGPROP_OUTERJOINS)</span><span class="sxs-lookup"><span data-stu-id="ea36a-196">(KAGPROP_OUTERJOINS)</span></span></p></td>
<td><p><span data-ttu-id="ea36a-197">プロバイダーが OUTER JOIN をサポートするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="ea36a-197">Indicates whether the provider supports OUTER JOINs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-198">特殊文字</span><span class="sxs-lookup"><span data-stu-id="ea36a-198">Special Characters</span></span><br />
<span data-ttu-id="ea36a-199">(KAGPROP_SPECIALCHARACTERS)</span><span class="sxs-lookup"><span data-stu-id="ea36a-199">(KAGPROP_SPECIALCHARACTERS)</span></span></p></td>
<td><p><span data-ttu-id="ea36a-200">ODBC ドライバーで特別な意味を持つ文字を示します。</span><span class="sxs-lookup"><span data-stu-id="ea36a-200">Indicates which characters have special meaning for the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-201">ストアド プロシージャ</span><span class="sxs-lookup"><span data-stu-id="ea36a-201">Stored Procedures</span></span><br />
<span data-ttu-id="ea36a-202">(KAGPROP_PROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="ea36a-202">(KAGPROP_PROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="ea36a-203">この ODBC ドライバーでストアド プロシージャを使用できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="ea36a-203">Indicates whether stored procedures are available for use with this ODBC driver.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-204">文字列を処理する関数</span><span class="sxs-lookup"><span data-stu-id="ea36a-204">String Functions</span></span><br />
<span data-ttu-id="ea36a-205">(KAGPROP_STRINGFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="ea36a-205">(KAGPROP_STRINGFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="ea36a-p110">ODBC ドライバーがサポートする文字列関数を示します。関数名とこのビットマスクで使用される関連付けられた値の一覧については、ODBC マニュアルの「Appendix E: Scalar Functions」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ea36a-p110">Indicates which string functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-208">システム関数</span><span class="sxs-lookup"><span data-stu-id="ea36a-208">System Functions</span></span><br />
<span data-ttu-id="ea36a-209">(KAGPROP_SYSTEMFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="ea36a-209">(KAGPROP_SYSTEMFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="ea36a-p111">ODBC ドライバーがサポートするシステム関数を示します。関数名とこのビットマスクで使用される関連付けられた値の一覧については、ODBC マニュアルの「Appendix E: Scalar Functions」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ea36a-p111">Indicates which system functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-212">日付/時刻関数</span><span class="sxs-lookup"><span data-stu-id="ea36a-212">Time/Date Functions</span></span><br />
<span data-ttu-id="ea36a-213">(KAGPROP_TIMEDATEFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="ea36a-213">(KAGPROP_TIMEDATEFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="ea36a-p112">ODBC ドライバーがサポートする時刻/日付関数を示します。関数名とこのビットマスクで使用される関連付けられた値の一覧については、ODBC マニュアルの「Appendix E: Scalar Functions」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ea36a-p112">Indicates which time and date functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-216">SQL の文法のサポート</span><span class="sxs-lookup"><span data-stu-id="ea36a-216">SQL Grammar Support</span></span><br />
<span data-ttu-id="ea36a-217">(KAGPROP_ODBCSQLCONFORMANCE)</span><span class="sxs-lookup"><span data-stu-id="ea36a-217">(KAGPROP_ODBCSQLCONFORMANCE)</span></span></p></td>
<td><p><span data-ttu-id="ea36a-218">ODBC ドライバーがサポートする SQL 文法を示します。</span><span class="sxs-lookup"><span data-stu-id="ea36a-218">Indicates the SQL grammar that the ODBC driver supports.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a><span data-ttu-id="ea36a-219">プロバイダー固有の Recordset および Command のプロパティ</span><span class="sxs-lookup"><span data-stu-id="ea36a-219">Provider-Specific Recordset and Command Properties</span></span>

<span data-ttu-id="ea36a-p113">OLE DB Provider for ODBC は、 **Recordset** オブジェクトと **Command** オブジェクトの **Properties** コレクションにプロパティを追加します。次の表は、これらのプロパティの一覧で、かっこ内は対応する OLE DB プロパティ名です。</span><span class="sxs-lookup"><span data-stu-id="ea36a-p113">The OLE DB provider for ODBC adds several properties to the **Properties** collection of the **Recordset** and **Command** objects. The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ea36a-222">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="ea36a-222">Property Name</span></span></p></th>
<th><p><span data-ttu-id="ea36a-223">説明</span><span class="sxs-lookup"><span data-stu-id="ea36a-223">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-224">クエリベースの更新/削除/挿入</span><span class="sxs-lookup"><span data-stu-id="ea36a-224">Query Based Updates/Deletes/Inserts</span></span><br />
<span data-ttu-id="ea36a-225">(KAGPROP_QUERYBASEDUPDATES)</span><span class="sxs-lookup"><span data-stu-id="ea36a-225">(KAGPROP_QUERYBASEDUPDATES)</span></span></p></td>
<td><p><span data-ttu-id="ea36a-226">SQL クエリを使用して更新、削除、および挿入を実行できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="ea36a-226">Indicates whether updates, deletions, and insertions can be performed using SQL queries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-227">ODBC の同時実行の種類</span><span class="sxs-lookup"><span data-stu-id="ea36a-227">ODBC Concurrency Type</span></span><br />
<span data-ttu-id="ea36a-228">(KAGPROP_CONCURRENCY)</span><span class="sxs-lookup"><span data-stu-id="ea36a-228">(KAGPROP_CONCURRENCY)</span></span></p></td>
<td><p><span data-ttu-id="ea36a-229">2 人のユーザーがデータ ソースの同じデータに同時にアクセスしようとしたときに発生する問題を減少させるための方法を示します。</span><span class="sxs-lookup"><span data-stu-id="ea36a-229">Indicates the method used to reduce potential problems caused by two users attempting to access the same data from the data source simultaneously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-230">順方向専用カーソルの BLOB のアクセシビリティ</span><span class="sxs-lookup"><span data-stu-id="ea36a-230">BLOB accessibility on Forward-Only cursor</span></span><br />
<span data-ttu-id="ea36a-231">(KAGPROP_BLOBSONFOCURSOR)</span><span class="sxs-lookup"><span data-stu-id="ea36a-231">(KAGPROP_BLOBSONFOCURSOR)</span></span></p></td>
<td><p><span data-ttu-id="ea36a-232">前方のみのカーソルの使用時に BLOB <strong>Fields</strong> にアクセスできるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="ea36a-232">Indicates whether BLOB <strong>Fields</strong> can be accessed when using a forward-only cursor.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-233">SQL_FLOAT、SQL_DOUBLE、および SQL_REAL を QBU WHERE 句に含める</span><span class="sxs-lookup"><span data-stu-id="ea36a-233">Include SQL_FLOAT, SQL_DOUBLE, and SQL_REAL in QBU WHERE clauses</span></span><br />
<span data-ttu-id="ea36a-234">(KAGPROP_INCLUDENONEXACT)</span><span class="sxs-lookup"><span data-stu-id="ea36a-234">(KAGPROP_INCLUDENONEXACT)</span></span></p></td>
<td><p><span data-ttu-id="ea36a-235">SQL_FLOAT、SQL_DOUBLE、および SQL_REAL の値を QBU WHERE 句に含めることができるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="ea36a-235">Indicates whether SQL_FLOAT, SQL_DOUBLE, and SQL_REAL values can be included in a QBU WHERE clause.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-236">挿入後の最後の行の位置</span><span class="sxs-lookup"><span data-stu-id="ea36a-236">Position on the last row after insert</span></span><br />
<span data-ttu-id="ea36a-237">(KAGPROP_POSITIONONNEWROW)</span><span class="sxs-lookup"><span data-stu-id="ea36a-237">(KAGPROP_POSITIONONNEWROW)</span></span></p></td>
<td><p><span data-ttu-id="ea36a-238">新規レコードをテーブルに挿入した後、テーブルの最後の行が現在の行になるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="ea36a-238">Indicates that after a new record has been inserted in a table, the last row in the table will be come the current row.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-239">IRowsetChangeExtInfo</span><span class="sxs-lookup"><span data-stu-id="ea36a-239">IRowsetChangeExtInfo</span></span><br />
<span data-ttu-id="ea36a-240">(KAGPROP_IROWSETCHANGEEXTINFO)</span><span class="sxs-lookup"><span data-stu-id="ea36a-240">(KAGPROP_IROWSETCHANGEEXTINFO)</span></span></p></td>
<td><p><span data-ttu-id="ea36a-241"><strong>IRowsetChange</strong> インターフェイスが拡張情報を提供するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="ea36a-241">Indicates whether the <strong>IRowsetChange</strong> interface provides extended information support.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-242">ODBC カーソルの種類</span><span class="sxs-lookup"><span data-stu-id="ea36a-242">ODBC Cursor Type</span></span><br />
<span data-ttu-id="ea36a-243">(KAGPROP_CURSOR)</span><span class="sxs-lookup"><span data-stu-id="ea36a-243">(KAGPROP_CURSOR)</span></span></p></td>
<td><p><span data-ttu-id="ea36a-244"><strong>Recordset</strong> で使用されるカーソルの種類を示します。</span><span class="sxs-lookup"><span data-stu-id="ea36a-244">Indicates the type of cursor used by the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-245">マーシャ リングできる行セットを生成します。</span><span class="sxs-lookup"><span data-stu-id="ea36a-245">Generate a Rowset that can be marshaled</span></span><br />
<span data-ttu-id="ea36a-246">(KAGPROP_MARSHALLABLE)</span><span class="sxs-lookup"><span data-stu-id="ea36a-246">(KAGPROP_MARSHALLABLE)</span></span></p></td>
<td><p><span data-ttu-id="ea36a-247">ODBC ドライバーがマーシャリング可能なレコードセットを生成することを示します。</span><span class="sxs-lookup"><span data-stu-id="ea36a-247">Indicates that the ODBC driver generates a recordset that can be marshaled</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a><span data-ttu-id="ea36a-248">コマンド テキスト</span><span class="sxs-lookup"><span data-stu-id="ea36a-248">Command Text</span></span>

<span data-ttu-id="ea36a-249">[Command](command-object-ado.md) オブジェクトの使用方法は、データ ソースおよび受け付けられるクエリまたはコマンド ステートメントの種類によって大きく異なります。</span><span class="sxs-lookup"><span data-stu-id="ea36a-249">How you use the [Command](command-object-ado.md) object largely depends on the data source, and what type of query or command statement it will accept.</span></span>

<span data-ttu-id="ea36a-250">ODBC には、ストアド プロシージャを呼び出すための独自の構文があります。</span><span class="sxs-lookup"><span data-stu-id="ea36a-250">ODBC provides a specific syntax for calling stored procedures.</span></span> <span data-ttu-id="ea36a-251">**コマンド**オブジェクト、 [Connection](connection-object-ado.md)オブジェクトの**Execute**メソッドの*CommandText*引数、または[Recordset](recordset-object-ado.md)の**Open**メソッドの*Source*引数の[CommandText](commandtext-property-ado.md)プロパティのオブジェクトは、この構文を使用して文字列に渡します。</span><span class="sxs-lookup"><span data-stu-id="ea36a-251">For the [CommandText](commandtext-property-ado.md) property of a **Command** object, the *CommandText* argument to the **Execute** method on a [Connection](connection-object-ado.md) object, or the *Source* argument to the **Open** method on a [Recordset](recordset-object-ado.md) object, passes in a string with this syntax:</span></span>

`"{ [ ? = ] call procedure [ ( ? [, ? [ ,  ]] ) ] }"`

<span data-ttu-id="ea36a-p115">**?** はそれぞれ [Parameters](parameters-collection-ado.md) コレクションのオブジェクトを参照します。最初の **?** は **Parameters**(0) を参照し、次の **?** は **Parameters**(1) を参照し、以下同様に続きます。</span><span class="sxs-lookup"><span data-stu-id="ea36a-p115">Each **?** references an object in the [Parameters](parameters-collection-ado.md) collection. The first **?** references **Parameters**(0), the next **?** references **Parameters**(1), and so on.</span></span>

<span data-ttu-id="ea36a-p116">パラメーターの参照は省略可能で、ストアド プロシージャの構造に依存します。パラメーターを定義していないストアド プロシージャを呼び出す場合の構文は、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="ea36a-p116">The parameter references are optional and depend on the structure of the stored procedure. If you want to call a stored procedure that defines no parameters, your string would look like this:</span></span>

`"{ call procedure }"`

<span data-ttu-id="ea36a-259">2 つのクエリ パラメーターを持つ場合は、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="ea36a-259">If you have two query parameters, your string would look like this:</span></span>

`"{ call procedure ( ?, ? ) }"`

<span data-ttu-id="ea36a-p117">ストアド プロシージャが値を返す場合、戻り値は別のパラメーターとして扱われます。クエリ パラメーターがなく、戻り値がある場合は、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="ea36a-p117">If the stored procedure will return a value, the return value is treated as another parameter. If you have no query parameters but you do have a return value, your string would look like this:</span></span>

`"{ ? = call procedure }"`

<span data-ttu-id="ea36a-262">戻り値があり、2 つのクエリ パラメーターがある場合は、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="ea36a-262">Finally, if you have a return value and two query parameters, your string would look like this:</span></span>

`"{ ? = call procedure ( ?, ? ) }"`

## <a name="recordset-behavior"></a><span data-ttu-id="ea36a-263">Recordset の動作</span><span class="sxs-lookup"><span data-stu-id="ea36a-263">Recordset Behavior</span></span>

<span data-ttu-id="ea36a-264">次の表は、このプロバイダーで開かれた **Recordset** オブジェクトで利用可能な標準の ADO メソッドと ADO プロパティの一覧です。</span><span class="sxs-lookup"><span data-stu-id="ea36a-264">The following tables list the standard ADO methods and properties available on a **Recordset** object opened with this provider.</span></span>

<span data-ttu-id="ea36a-265">プロバイダーの構成による **Recordset** の動作の詳細については、 [Supports](supports-method-ado.md) メソッドを実行し、 **Recordset** の **Properties** コレクションを列挙して、プロバイダー固有の動的プロパティが存在するかどうかを確認してください。</span><span class="sxs-lookup"><span data-stu-id="ea36a-265">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the **Properties** collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="ea36a-266">標準的な ADO **Recordset** のプロパティの利用可能性は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="ea36a-266">Availability of standard ADO **Recordset** properties:</span></span>

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
<th><p><span data-ttu-id="ea36a-267">プロパティ</span><span class="sxs-lookup"><span data-stu-id="ea36a-267">Property</span></span></p></th>
<th><p><span data-ttu-id="ea36a-268">前方向</span><span class="sxs-lookup"><span data-stu-id="ea36a-268">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="ea36a-269">動的</span><span class="sxs-lookup"><span data-stu-id="ea36a-269">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="ea36a-270">キーセット</span><span class="sxs-lookup"><span data-stu-id="ea36a-270">Keyset</span></span></p></th>
<th><p><span data-ttu-id="ea36a-271">静的</span><span class="sxs-lookup"><span data-stu-id="ea36a-271">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-272"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="ea36a-272"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="ea36a-273">利用不可</span><span class="sxs-lookup"><span data-stu-id="ea36a-273">not available</span></span></p></td>
<td><p><span data-ttu-id="ea36a-274">利用不可</span><span class="sxs-lookup"><span data-stu-id="ea36a-274">not available</span></span></p></td>
<td><p><span data-ttu-id="ea36a-275">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-275">read/write</span></span></p></td>
<td><p><span data-ttu-id="ea36a-276">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-276">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-277"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="ea36a-277"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="ea36a-278">利用不可</span><span class="sxs-lookup"><span data-stu-id="ea36a-278">not available</span></span></p></td>
<td><p><span data-ttu-id="ea36a-279">利用不可</span><span class="sxs-lookup"><span data-stu-id="ea36a-279">not available</span></span></p></td>
<td><p><span data-ttu-id="ea36a-280">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-280">read/write</span></span></p></td>
<td><p><span data-ttu-id="ea36a-281">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-281">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-282"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="ea36a-282"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="ea36a-283">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-283">read/write</span></span></p></td>
<td><p><span data-ttu-id="ea36a-284">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-284">read/write</span></span></p></td>
<td><p><span data-ttu-id="ea36a-285">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-285">read/write</span></span></p></td>
<td><p><span data-ttu-id="ea36a-286">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-286">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-287"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="ea36a-287"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="ea36a-288">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="ea36a-288">read-only</span></span></p></td>
<td><p><span data-ttu-id="ea36a-289">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="ea36a-289">read-only</span></span></p></td>
<td><p><span data-ttu-id="ea36a-290">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="ea36a-290">read-only</span></span></p></td>
<td><p><span data-ttu-id="ea36a-291">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="ea36a-291">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-292"><a href="bookmark-property-ado.md">Bookmark</a></span><span class="sxs-lookup"><span data-stu-id="ea36a-292"><a href="bookmark-property-ado.md">Bookmark</a></span></span></p></td>
<td><p><span data-ttu-id="ea36a-293">利用不可</span><span class="sxs-lookup"><span data-stu-id="ea36a-293">not available</span></span></p></td>
<td><p><span data-ttu-id="ea36a-294">利用不可</span><span class="sxs-lookup"><span data-stu-id="ea36a-294">not available</span></span></p></td>
<td><p><span data-ttu-id="ea36a-295">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-295">read/write</span></span></p></td>
<td><p><span data-ttu-id="ea36a-296">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-296">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-297"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="ea36a-297"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="ea36a-298">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-298">read/write</span></span></p></td>
<td><p><span data-ttu-id="ea36a-299">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-299">read/write</span></span></p></td>
<td><p><span data-ttu-id="ea36a-300">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-300">read/write</span></span></p></td>
<td><p><span data-ttu-id="ea36a-301">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-301">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-302"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="ea36a-302"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="ea36a-303">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-303">read/write</span></span></p></td>
<td><p><span data-ttu-id="ea36a-304">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-304">read/write</span></span></p></td>
<td><p><span data-ttu-id="ea36a-305">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-305">read/write</span></span></p></td>
<td><p><span data-ttu-id="ea36a-306">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-306">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-307"><a href="cursortype-property-ado.md">カーソル。</a></span><span class="sxs-lookup"><span data-stu-id="ea36a-307"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="ea36a-308">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-308">read/write</span></span></p></td>
<td><p><span data-ttu-id="ea36a-309">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-309">read/write</span></span></p></td>
<td><p><span data-ttu-id="ea36a-310">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-310">read/write</span></span></p></td>
<td><p><span data-ttu-id="ea36a-311">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-311">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-312"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="ea36a-312"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="ea36a-313">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="ea36a-313">read-only</span></span></p></td>
<td><p><span data-ttu-id="ea36a-314">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="ea36a-314">read-only</span></span></p></td>
<td><p><span data-ttu-id="ea36a-315">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="ea36a-315">read-only</span></span></p></td>
<td><p><span data-ttu-id="ea36a-316">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="ea36a-316">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-317"><a href="filter-property-ado.md">フィルター</a></span><span class="sxs-lookup"><span data-stu-id="ea36a-317"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="ea36a-318">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-318">read/write</span></span></p></td>
<td><p><span data-ttu-id="ea36a-319">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-319">read/write</span></span></p></td>
<td><p><span data-ttu-id="ea36a-320">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-320">read/write</span></span></p></td>
<td><p><span data-ttu-id="ea36a-321">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-321">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-322"><a href="locktype-property-ado.md">ロック。</a></span><span class="sxs-lookup"><span data-stu-id="ea36a-322"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="ea36a-323">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-323">read/write</span></span></p></td>
<td><p><span data-ttu-id="ea36a-324">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-324">read/write</span></span></p></td>
<td><p><span data-ttu-id="ea36a-325">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-325">read/write</span></span></p></td>
<td><p><span data-ttu-id="ea36a-326">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-326">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-327"><a href="marshaloptions-property-ado.md">スレッド</a></span><span class="sxs-lookup"><span data-stu-id="ea36a-327"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="ea36a-328">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-328">read/write</span></span></p></td>
<td><p><span data-ttu-id="ea36a-329">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-329">read/write</span></span></p></td>
<td><p><span data-ttu-id="ea36a-330">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-330">read/write</span></span></p></td>
<td><p><span data-ttu-id="ea36a-331">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-331">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-332"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="ea36a-332"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="ea36a-333">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-333">read/write</span></span></p></td>
<td><p><span data-ttu-id="ea36a-334">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-334">read/write</span></span></p></td>
<td><p><span data-ttu-id="ea36a-335">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-335">read/write</span></span></p></td>
<td><p><span data-ttu-id="ea36a-336">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-336">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-337"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="ea36a-337"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="ea36a-338">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-338">read/write</span></span></p></td>
<td><p><span data-ttu-id="ea36a-339">利用不可</span><span class="sxs-lookup"><span data-stu-id="ea36a-339">not available</span></span></p></td>
<td><p><span data-ttu-id="ea36a-340">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="ea36a-340">read-only</span></span></p></td>
<td><p><span data-ttu-id="ea36a-341">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="ea36a-341">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-342"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="ea36a-342"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="ea36a-343">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-343">read/write</span></span></p></td>
<td><p><span data-ttu-id="ea36a-344">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-344">read/write</span></span></p></td>
<td><p><span data-ttu-id="ea36a-345">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-345">read/write</span></span></p></td>
<td><p><span data-ttu-id="ea36a-346">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-346">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-347"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="ea36a-347"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="ea36a-348">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-348">read/write</span></span></p></td>
<td><p><span data-ttu-id="ea36a-349">利用不可</span><span class="sxs-lookup"><span data-stu-id="ea36a-349">not available</span></span></p></td>
<td><p><span data-ttu-id="ea36a-350">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="ea36a-350">read-only</span></span></p></td>
<td><p><span data-ttu-id="ea36a-351">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="ea36a-351">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-352"><a href="source-property-ado-recordset.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="ea36a-352"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="ea36a-353">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-353">read/write</span></span></p></td>
<td><p><span data-ttu-id="ea36a-354">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-354">read/write</span></span></p></td>
<td><p><span data-ttu-id="ea36a-355">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-355">read/write</span></span></p></td>
<td><p><span data-ttu-id="ea36a-356">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="ea36a-356">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-357"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="ea36a-357"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="ea36a-358">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="ea36a-358">read-only</span></span></p></td>
<td><p><span data-ttu-id="ea36a-359">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="ea36a-359">read-only</span></span></p></td>
<td><p><span data-ttu-id="ea36a-360">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="ea36a-360">read-only</span></span></p></td>
<td><p><span data-ttu-id="ea36a-361">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="ea36a-361">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-362"><a href="status-property-ado-recordset.md">状態</a></span><span class="sxs-lookup"><span data-stu-id="ea36a-362"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="ea36a-363">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="ea36a-363">read-only</span></span></p></td>
<td><p><span data-ttu-id="ea36a-364">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="ea36a-364">read-only</span></span></p></td>
<td><p><span data-ttu-id="ea36a-365">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="ea36a-365">read-only</span></span></p></td>
<td><p><span data-ttu-id="ea36a-366">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="ea36a-366">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ea36a-367">バージョン 1.0 の Microsoft OLE DB Provider for ODBC で ADO を使用する場合、[AbsolutePosition](absoluteposition-property-ado.md) プロパティと [AbsolutePage](absolutepage-property-ado.md) プロパティは値の設定のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="ea36a-367">The [AbsolutePosition](absoluteposition-property-ado.md) and [AbsolutePage](absolutepage-property-ado.md) properties are write-only when ADO is used with version 1.0 of the Microsoft OLE DB Provider for ODBC.</span></span>

<span data-ttu-id="ea36a-368">標準的な ADO **Recordset** のメソッドの利用可能性は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="ea36a-368">Availability of standard ADO **Recordset** methods:</span></span>

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
<th><p><span data-ttu-id="ea36a-369">メソッド</span><span class="sxs-lookup"><span data-stu-id="ea36a-369">Method</span></span></p></th>
<th><p><span data-ttu-id="ea36a-370">前方向</span><span class="sxs-lookup"><span data-stu-id="ea36a-370">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="ea36a-371">動的</span><span class="sxs-lookup"><span data-stu-id="ea36a-371">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="ea36a-372">キーセット</span><span class="sxs-lookup"><span data-stu-id="ea36a-372">Keyset</span></span></p></th>
<th><p><span data-ttu-id="ea36a-373">静的</span><span class="sxs-lookup"><span data-stu-id="ea36a-373">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-374"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="ea36a-374"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="ea36a-375">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-375">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-376">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-376">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-377">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-377">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-378">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-378">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-379"><a href="cancel-method-ado.md">Cancel</a></span><span class="sxs-lookup"><span data-stu-id="ea36a-379"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="ea36a-380">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-380">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-381">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-381">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-382">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-382">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-383">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-383">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-384"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="ea36a-384"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="ea36a-385">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-385">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-386">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-386">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-387">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-387">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-388">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-388">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-389"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="ea36a-389"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="ea36a-390">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-390">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-391">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-391">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-392">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-392">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-393">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-393">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-394"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="ea36a-394"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="ea36a-395">いいえ</span><span class="sxs-lookup"><span data-stu-id="ea36a-395">No</span></span></p></td>
<td><p><span data-ttu-id="ea36a-396">いいえ</span><span class="sxs-lookup"><span data-stu-id="ea36a-396">No</span></span></p></td>
<td><p><span data-ttu-id="ea36a-397">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-397">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-398">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-398">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-399"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="ea36a-399"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="ea36a-400">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-400">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-401">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-401">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-402">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-402">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-403">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-403">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-404"><a href="delete-method-ado-recordset.md">Delete</a></span><span class="sxs-lookup"><span data-stu-id="ea36a-404"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="ea36a-405">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-405">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-406">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-406">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-407">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-407">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-408">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-408">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-409"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="ea36a-409"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="ea36a-410">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-410">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-411">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-411">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-412">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-412">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-413">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-413">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-414"><a href="move-method-ado.md">Move</a></span><span class="sxs-lookup"><span data-stu-id="ea36a-414"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="ea36a-415">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-415">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-416">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-416">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-417">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-417">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-418">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-418">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-419"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="ea36a-419"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="ea36a-420">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-420">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-421">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-421">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-422">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-422">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-423">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-423">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-424"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span><span class="sxs-lookup"><span data-stu-id="ea36a-424"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span></span></p></td>
<td><p><span data-ttu-id="ea36a-425">いいえ</span><span class="sxs-lookup"><span data-stu-id="ea36a-425">No</span></span></p></td>
<td><p><span data-ttu-id="ea36a-426">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-426">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-427">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-427">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-428">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-428">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-429"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span><span class="sxs-lookup"><span data-stu-id="ea36a-429"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span></span></p></td>
<td><p><span data-ttu-id="ea36a-430">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-430">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-431">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-431">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-432">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-432">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-433">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-433">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-434"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="ea36a-434"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="ea36a-435">いいえ</span><span class="sxs-lookup"><span data-stu-id="ea36a-435">No</span></span></p></td>
<td><p><span data-ttu-id="ea36a-436">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-436">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-437">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-437">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-438">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-438">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-439"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span><span class="sxs-lookup"><span data-stu-id="ea36a-439"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span></span></p></td>
<td><p><span data-ttu-id="ea36a-440">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-440">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-441">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-441">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-442">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-442">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-443">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-443">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-444"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="ea36a-444"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="ea36a-445">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-445">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-446">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-446">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-447">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-447">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-448">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-448">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-449"><a href="requery-method-ado.md">Requery</a></span><span class="sxs-lookup"><span data-stu-id="ea36a-449"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="ea36a-450">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-450">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-451">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-451">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-452">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-452">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-453">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-453">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-454"><a href="resync-method-ado.md">再同期</a></span><span class="sxs-lookup"><span data-stu-id="ea36a-454"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="ea36a-455">いいえ</span><span class="sxs-lookup"><span data-stu-id="ea36a-455">No</span></span></p></td>
<td><p><span data-ttu-id="ea36a-456">いいえ</span><span class="sxs-lookup"><span data-stu-id="ea36a-456">No</span></span></p></td>
<td><p><span data-ttu-id="ea36a-457">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-457">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-458">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-458">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-459"><a href="supports-method-ado.md">サポートしています</a></span><span class="sxs-lookup"><span data-stu-id="ea36a-459"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="ea36a-460">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-460">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-461">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-461">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-462">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-462">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-463">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-463">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-464"><a href="update-method-ado.md">Update</a></span><span class="sxs-lookup"><span data-stu-id="ea36a-464"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="ea36a-465">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-465">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-466">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-466">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-467">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-467">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-468">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-468">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-469"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="ea36a-469"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="ea36a-470">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-470">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-471">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-471">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-472">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-472">Yes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-473">はい</span><span class="sxs-lookup"><span data-stu-id="ea36a-473">Yes</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ea36a-474">\*Microsoft Access データベースではサポートされません。</span><span class="sxs-lookup"><span data-stu-id="ea36a-474">\*Not supported for Microsoft Access databases.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="ea36a-475">動的プロパティ</span><span class="sxs-lookup"><span data-stu-id="ea36a-475">Dynamic Properties</span></span>

<span data-ttu-id="ea36a-476">Microsoft OLE DB Provider for ODBC は、開かれていない **Connection** オブジェクト、 [Recordset](connection-object-ado.md) オブジェクト、および [Command](recordset-object-ado.md) オブジェクトの [Properties](command-object-ado.md) コレクションに動的プロパティを挿入します。</span><span class="sxs-lookup"><span data-stu-id="ea36a-476">The Microsoft OLE DB Provider for ODBC inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="ea36a-p118">以下の表は、各動的プロパティの ADO 名と OLE DB 名の対応表です。 「OLE DB プログラマ リファレンス」では、「説明」欄に ADO プロパティ名が示されています。プロパティの詳細については、「OLE DB プログラマ リファレンス」を参照してください。OLE DB プロパティ名をキーワードとして検索するか、「付録 C: プロパティ表」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ea36a-p118">The tables below are a cross-index of the ADO and OLE DB names for each dynamic property. The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description." You can find more information about these properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="ea36a-481">Connection の動的プロパティ</span><span class="sxs-lookup"><span data-stu-id="ea36a-481">Connection Dynamic Properties</span></span>

<span data-ttu-id="ea36a-482">次に示すプロパティが **Connection** オブジェクトの **Properties** コレクションに追加されます。</span><span class="sxs-lookup"><span data-stu-id="ea36a-482">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ea36a-483">ADO プロパティ名</span><span class="sxs-lookup"><span data-stu-id="ea36a-483">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="ea36a-484">OLE DB プロパティ名</span><span class="sxs-lookup"><span data-stu-id="ea36a-484">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-485">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="ea36a-485">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="ea36a-486">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="ea36a-486">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-487">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="ea36a-487">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="ea36a-488">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="ea36a-488">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-489">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="ea36a-489">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="ea36a-490">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="ea36a-490">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-491">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="ea36a-491">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="ea36a-492">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="ea36a-492">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-493">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="ea36a-493">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="ea36a-494">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="ea36a-494">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-495">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="ea36a-495">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="ea36a-496">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="ea36a-496">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-497">Column Definition</span><span class="sxs-lookup"><span data-stu-id="ea36a-497">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="ea36a-498">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="ea36a-498">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-499">Connect Timeout</span><span class="sxs-lookup"><span data-stu-id="ea36a-499">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="ea36a-500">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="ea36a-500">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-501">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="ea36a-501">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="ea36a-502">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="ea36a-502">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-503">Data Source</span><span class="sxs-lookup"><span data-stu-id="ea36a-503">Data Source</span></span></p></td>
<td><p><span data-ttu-id="ea36a-504">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="ea36a-504">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-505">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="ea36a-505">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="ea36a-506">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="ea36a-506">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-507">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="ea36a-507">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="ea36a-508">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="ea36a-508">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-509">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="ea36a-509">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="ea36a-510">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="ea36a-510">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-511">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="ea36a-511">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="ea36a-512">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="ea36a-512">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-513">Extended Properties</span><span class="sxs-lookup"><span data-stu-id="ea36a-513">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="ea36a-514">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="ea36a-514">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-515">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="ea36a-515">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="ea36a-516">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="ea36a-516">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-517">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="ea36a-517">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="ea36a-518">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="ea36a-518">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-519">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="ea36a-519">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="ea36a-520">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="ea36a-520">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-521">Initial Catalog</span><span class="sxs-lookup"><span data-stu-id="ea36a-521">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="ea36a-522">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="ea36a-522">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-523">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="ea36a-523">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="ea36a-524">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="ea36a-524">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-525">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="ea36a-525">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="ea36a-526">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="ea36a-526">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-527">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="ea36a-527">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="ea36a-528">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="ea36a-528">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-529">Location</span><span class="sxs-lookup"><span data-stu-id="ea36a-529">Location</span></span></p></td>
<td><p><span data-ttu-id="ea36a-530">DBPROP_INIT_LOCATION</span><span class="sxs-lookup"><span data-stu-id="ea36a-530">DBPROP_INIT_LOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-531">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="ea36a-531">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="ea36a-532">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="ea36a-532">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-533">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="ea36a-533">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="ea36a-534">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="ea36a-534">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-535">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="ea36a-535">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="ea36a-536">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="ea36a-536">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-537">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="ea36a-537">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="ea36a-538">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="ea36a-538">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-539">Mode</span><span class="sxs-lookup"><span data-stu-id="ea36a-539">Mode</span></span></p></td>
<td><p><span data-ttu-id="ea36a-540">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="ea36a-540">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-541">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="ea36a-541">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="ea36a-542">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="ea36a-542">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-543">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="ea36a-543">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="ea36a-544">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="ea36a-544">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-545">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="ea36a-545">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="ea36a-546">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="ea36a-546">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-547">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="ea36a-547">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="ea36a-548">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="ea36a-548">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-549">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="ea36a-549">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="ea36a-550">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="ea36a-550">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-551">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="ea36a-551">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="ea36a-552">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="ea36a-552">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-553">OLE DB Services</span><span class="sxs-lookup"><span data-stu-id="ea36a-553">OLE DB Services</span></span></p></td>
<td><p><span data-ttu-id="ea36a-554">DBPROP_INIT_OLEDBSERVICES</span><span class="sxs-lookup"><span data-stu-id="ea36a-554">DBPROP_INIT_OLEDBSERVICES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-555">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="ea36a-555">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="ea36a-556">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="ea36a-556">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-557">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="ea36a-557">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="ea36a-558">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="ea36a-558">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-559">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="ea36a-559">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="ea36a-560">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="ea36a-560">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-561">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="ea36a-561">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="ea36a-562">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="ea36a-562">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-563">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="ea36a-563">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="ea36a-564">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="ea36a-564">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-565">Password</span><span class="sxs-lookup"><span data-stu-id="ea36a-565">Password</span></span></p></td>
<td><p><span data-ttu-id="ea36a-566">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="ea36a-566">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-567">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="ea36a-567">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="ea36a-568">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="ea36a-568">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-569">Persist Security Info</span><span class="sxs-lookup"><span data-stu-id="ea36a-569">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="ea36a-570">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="ea36a-570">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-571">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="ea36a-571">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="ea36a-572">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="ea36a-572">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-573">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="ea36a-573">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="ea36a-574">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="ea36a-574">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-575">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="ea36a-575">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="ea36a-576">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="ea36a-576">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-577">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="ea36a-577">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="ea36a-578">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="ea36a-578">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-579">Prompt</span><span class="sxs-lookup"><span data-stu-id="ea36a-579">Prompt</span></span></p></td>
<td><p><span data-ttu-id="ea36a-580">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="ea36a-580">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-581">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="ea36a-581">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="ea36a-582">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="ea36a-582">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-583">Provider Name</span><span class="sxs-lookup"><span data-stu-id="ea36a-583">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="ea36a-584">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="ea36a-584">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-585">Provider Version</span><span class="sxs-lookup"><span data-stu-id="ea36a-585">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="ea36a-586">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="ea36a-586">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-587">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="ea36a-587">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="ea36a-588">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="ea36a-588">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-589">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="ea36a-589">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="ea36a-590">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="ea36a-590">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-591">Schema Term</span><span class="sxs-lookup"><span data-stu-id="ea36a-591">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="ea36a-592">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="ea36a-592">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-593">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="ea36a-593">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="ea36a-594">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="ea36a-594">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-595">SQL Support</span><span class="sxs-lookup"><span data-stu-id="ea36a-595">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="ea36a-596">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="ea36a-596">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-597">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="ea36a-597">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="ea36a-598">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="ea36a-598">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-599">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="ea36a-599">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="ea36a-600">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="ea36a-600">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-601">Table Term</span><span class="sxs-lookup"><span data-stu-id="ea36a-601">Table Term</span></span></p></td>
<td><p><span data-ttu-id="ea36a-602">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="ea36a-602">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-603">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="ea36a-603">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="ea36a-604">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="ea36a-604">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-605">User ID</span><span class="sxs-lookup"><span data-stu-id="ea36a-605">User ID</span></span></p></td>
<td><p><span data-ttu-id="ea36a-606">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="ea36a-606">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-607">User Name</span><span class="sxs-lookup"><span data-stu-id="ea36a-607">User Name</span></span></p></td>
<td><p><span data-ttu-id="ea36a-608">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="ea36a-608">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-609">Window Handle</span><span class="sxs-lookup"><span data-stu-id="ea36a-609">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="ea36a-610">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="ea36a-610">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="ea36a-611">Recordset の動的プロパティ</span><span class="sxs-lookup"><span data-stu-id="ea36a-611">Recordset Dynamic Properties</span></span>

<span data-ttu-id="ea36a-612">次に示すプロパティが **Recordset** オブジェクトの **Properties** コレクションに追加されます。</span><span class="sxs-lookup"><span data-stu-id="ea36a-612">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ea36a-613">ADO プロパティ名</span><span class="sxs-lookup"><span data-stu-id="ea36a-613">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="ea36a-614">OLE DB プロパティ名</span><span class="sxs-lookup"><span data-stu-id="ea36a-614">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-615">Access Order</span><span class="sxs-lookup"><span data-stu-id="ea36a-615">Access Order</span></span></p></td>
<td><p><span data-ttu-id="ea36a-616">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="ea36a-616">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-617">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="ea36a-617">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="ea36a-618">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="ea36a-618">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-619">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="ea36a-619">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="ea36a-620">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="ea36a-620">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-621">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="ea36a-621">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="ea36a-622">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="ea36a-622">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-623">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="ea36a-623">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="ea36a-624">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="ea36a-624">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-625">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="ea36a-625">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="ea36a-626">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="ea36a-626">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-627">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="ea36a-627">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="ea36a-628">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="ea36a-628">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-629">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="ea36a-629">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="ea36a-630">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="ea36a-630">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-631">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="ea36a-631">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="ea36a-632">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="ea36a-632">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-633">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="ea36a-633">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="ea36a-634">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="ea36a-634">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-635">IAccessor</span><span class="sxs-lookup"><span data-stu-id="ea36a-635">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="ea36a-636">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="ea36a-636">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-637">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="ea36a-637">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="ea36a-638">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="ea36a-638">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-639">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="ea36a-639">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="ea36a-640">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="ea36a-640">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-641">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="ea36a-641">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="ea36a-642">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="ea36a-642">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-643">IConvertType</span><span class="sxs-lookup"><span data-stu-id="ea36a-643">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="ea36a-644">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="ea36a-644">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-645">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="ea36a-645">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="ea36a-646">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="ea36a-646">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-647">IRowset</span><span class="sxs-lookup"><span data-stu-id="ea36a-647">IRowset</span></span></p></td>
<td><p><span data-ttu-id="ea36a-648">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="ea36a-648">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-649">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="ea36a-649">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="ea36a-650">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="ea36a-650">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-651">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="ea36a-651">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="ea36a-652">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="ea36a-652">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-653">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="ea36a-653">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="ea36a-654">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="ea36a-654">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-655">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="ea36a-655">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="ea36a-656">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="ea36a-656">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-657">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="ea36a-657">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-658">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="ea36a-658">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="ea36a-659">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="ea36a-659">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-660">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="ea36a-660">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="ea36a-661">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="ea36a-661">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-662">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="ea36a-662">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="ea36a-663">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="ea36a-663">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-664">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="ea36a-664">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="ea36a-665">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="ea36a-665">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-666">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="ea36a-666">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="ea36a-667">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="ea36a-667">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-668">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="ea36a-668">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="ea36a-669">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="ea36a-669">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-670">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="ea36a-670">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="ea36a-671">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="ea36a-671">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-672">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="ea36a-672">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="ea36a-673">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="ea36a-673">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-674">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="ea36a-674">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="ea36a-675">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="ea36a-675">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-676">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="ea36a-676">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="ea36a-677">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="ea36a-677">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-678">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="ea36a-678">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="ea36a-679">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="ea36a-679">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-680">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="ea36a-680">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="ea36a-681">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="ea36a-681">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-682">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="ea36a-682">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="ea36a-683">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="ea36a-683">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-684">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="ea36a-684">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="ea36a-685">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="ea36a-685">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-686">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="ea36a-686">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="ea36a-687">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="ea36a-687">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-688">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="ea36a-688">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="ea36a-689">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="ea36a-689">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-690">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="ea36a-690">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="ea36a-691">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="ea36a-691">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-692">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="ea36a-692">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="ea36a-693">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="ea36a-693">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-694">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="ea36a-694">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-695">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="ea36a-695">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-696">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="ea36a-696">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="ea36a-697">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="ea36a-697">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-698">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="ea36a-698">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="ea36a-699">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="ea36a-699">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-700">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="ea36a-700">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="ea36a-701">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="ea36a-701">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-702">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="ea36a-702">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="ea36a-703">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="ea36a-703">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-704">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="ea36a-704">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="ea36a-705">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="ea36a-705">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-706">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="ea36a-706">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="ea36a-707">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="ea36a-707">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-708">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="ea36a-708">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="ea36a-709">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="ea36a-709">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-710">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="ea36a-710">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="ea36a-711">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="ea36a-711">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-712">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="ea36a-712">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="ea36a-713">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="ea36a-713">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-714">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="ea36a-714">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="ea36a-715">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="ea36a-715">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-716">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="ea36a-716">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="ea36a-717">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="ea36a-717">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-718">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="ea36a-718">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="ea36a-719">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="ea36a-719">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-720">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="ea36a-720">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="ea36a-721">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="ea36a-721">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-722">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="ea36a-722">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="ea36a-723">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="ea36a-723">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-724">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="ea36a-724">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="ea36a-725">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="ea36a-725">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-726">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="ea36a-726">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="ea36a-727">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="ea36a-727">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-728">Unique Rows</span><span class="sxs-lookup"><span data-stu-id="ea36a-728">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="ea36a-729">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="ea36a-729">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-730">Updatability</span><span class="sxs-lookup"><span data-stu-id="ea36a-730">Updatability</span></span></p></td>
<td><p><span data-ttu-id="ea36a-731">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="ea36a-731">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-732">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="ea36a-732">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="ea36a-733">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="ea36a-733">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="ea36a-734">Command の動的プロパティ</span><span class="sxs-lookup"><span data-stu-id="ea36a-734">Command Dynamic Properties</span></span>

<span data-ttu-id="ea36a-735">次に示すプロパティが **Command** オブジェクトの **Properties** コレクションに追加されます。</span><span class="sxs-lookup"><span data-stu-id="ea36a-735">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ea36a-736">ADO プロパティ名</span><span class="sxs-lookup"><span data-stu-id="ea36a-736">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="ea36a-737">OLE DB プロパティ名</span><span class="sxs-lookup"><span data-stu-id="ea36a-737">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-738">Access Order</span><span class="sxs-lookup"><span data-stu-id="ea36a-738">Access Order</span></span></p></td>
<td><p><span data-ttu-id="ea36a-739">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="ea36a-739">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-740">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="ea36a-740">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="ea36a-741">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="ea36a-741">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-742">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="ea36a-742">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="ea36a-743">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="ea36a-743">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-744">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="ea36a-744">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="ea36a-745">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="ea36a-745">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-746">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="ea36a-746">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="ea36a-747">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="ea36a-747">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-748">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="ea36a-748">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="ea36a-749">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="ea36a-749">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-750">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="ea36a-750">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="ea36a-751">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="ea36a-751">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-752">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="ea36a-752">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="ea36a-753">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="ea36a-753">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-754">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="ea36a-754">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="ea36a-755">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="ea36a-755">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-756">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="ea36a-756">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="ea36a-757">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="ea36a-757">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-758">IAccessor</span><span class="sxs-lookup"><span data-stu-id="ea36a-758">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="ea36a-759">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="ea36a-759">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-760">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="ea36a-760">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="ea36a-761">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="ea36a-761">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-762">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="ea36a-762">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="ea36a-763">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="ea36a-763">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-764">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="ea36a-764">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="ea36a-765">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="ea36a-765">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-766">IConvertType</span><span class="sxs-lookup"><span data-stu-id="ea36a-766">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="ea36a-767">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="ea36a-767">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-768">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="ea36a-768">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="ea36a-769">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="ea36a-769">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-770">IRowset</span><span class="sxs-lookup"><span data-stu-id="ea36a-770">IRowset</span></span></p></td>
<td><p><span data-ttu-id="ea36a-771">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="ea36a-771">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-772">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="ea36a-772">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="ea36a-773">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="ea36a-773">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-774">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="ea36a-774">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="ea36a-775">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="ea36a-775">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-776">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="ea36a-776">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="ea36a-777">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="ea36a-777">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-778">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="ea36a-778">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="ea36a-779">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="ea36a-779">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-780">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="ea36a-780">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-781">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="ea36a-781">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="ea36a-782">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="ea36a-782">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-783">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="ea36a-783">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="ea36a-784">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="ea36a-784">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-785">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="ea36a-785">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="ea36a-786">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="ea36a-786">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-787">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="ea36a-787">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="ea36a-788">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="ea36a-788">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-789">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="ea36a-789">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="ea36a-790">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="ea36a-790">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-791">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="ea36a-791">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="ea36a-792">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="ea36a-792">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-793">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="ea36a-793">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="ea36a-794">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="ea36a-794">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-795">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="ea36a-795">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="ea36a-796">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="ea36a-796">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-797">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="ea36a-797">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="ea36a-798">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="ea36a-798">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-799">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="ea36a-799">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="ea36a-800">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="ea36a-800">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-801">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="ea36a-801">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="ea36a-802">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="ea36a-802">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-803">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="ea36a-803">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="ea36a-804">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="ea36a-804">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-805">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="ea36a-805">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="ea36a-806">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="ea36a-806">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-807">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="ea36a-807">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="ea36a-808">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="ea36a-808">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-809">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="ea36a-809">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="ea36a-810">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="ea36a-810">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-811">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="ea36a-811">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="ea36a-812">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="ea36a-812">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-813">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="ea36a-813">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="ea36a-814">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="ea36a-814">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-815">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="ea36a-815">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="ea36a-816">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="ea36a-816">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-817">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="ea36a-817">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="ea36a-818">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="ea36a-818">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-819">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="ea36a-819">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="ea36a-820">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="ea36a-820">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-821">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="ea36a-821">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="ea36a-822">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="ea36a-822">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-823">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="ea36a-823">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="ea36a-824">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="ea36a-824">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-825">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="ea36a-825">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="ea36a-826">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="ea36a-826">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-827">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="ea36a-827">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="ea36a-828">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="ea36a-828">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-829">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="ea36a-829">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="ea36a-830">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="ea36a-830">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-831">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="ea36a-831">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="ea36a-832">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="ea36a-832">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-833">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="ea36a-833">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="ea36a-834">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="ea36a-834">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-835">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="ea36a-835">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="ea36a-836">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="ea36a-836">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-837">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="ea36a-837">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="ea36a-838">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="ea36a-838">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-839">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="ea36a-839">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="ea36a-840">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="ea36a-840">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-841">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="ea36a-841">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="ea36a-842">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="ea36a-842">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-843">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="ea36a-843">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="ea36a-844">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="ea36a-844">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-845">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="ea36a-845">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="ea36a-846">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="ea36a-846">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-847">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="ea36a-847">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="ea36a-848">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="ea36a-848">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-849">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="ea36a-849">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="ea36a-850">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="ea36a-850">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea36a-851">Updatability</span><span class="sxs-lookup"><span data-stu-id="ea36a-851">Updatability</span></span></p></td>
<td><p><span data-ttu-id="ea36a-852">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="ea36a-852">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea36a-853">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="ea36a-853">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="ea36a-854">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="ea36a-854">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="ea36a-855">関連項目</span><span class="sxs-lookup"><span data-stu-id="ea36a-855">See also</span></span>

<span data-ttu-id="ea36a-856">特定の実装および ODBC 用 Microsoft OLE DB プロバイダーの機能の情報に関する詳細については、 [OLE DB プログラマ ガイド」](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85))を参照してくださいまたは[データ プラットフォーム デベロッパー センター](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ea36a-856">For details regarding specific implementation and functional information about the Microsoft OLE DB Provider for ODBC, consult the [OLE DB Programmer's Guide](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) or visit the [Data Platform Developer Center](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span></span>

