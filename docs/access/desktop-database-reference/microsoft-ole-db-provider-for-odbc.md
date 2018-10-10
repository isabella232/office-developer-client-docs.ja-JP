---
title: Microsoft OLE DB Provider for ODBC
TOCTitle: Microsoft OLE DB Provider for ODBC
ms:assetid: c507567e-5ad1-b32a-f6ad-5ba2c39aa4c2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249964(v=office.15)
ms:contentKeyID: 48547602
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 168799b517598211ca9de680730490a0a41d1dde
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479582"
---
# <a name="microsoft-ole-db-provider-for-odbc"></a><span data-ttu-id="b56d8-102">Microsoft OLE DB Provider for ODBC</span><span class="sxs-lookup"><span data-stu-id="b56d8-102">Microsoft OLE DB Provider for ODBC</span></span>

<span data-ttu-id="b56d8-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="b56d8-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b56d8-p101">ADO または RDS のプログラマにとって、すべてのデータ ソースで OLE DB インターフェイスが公開され、ADO で直接データ ソースを呼び出すことができるのが理想的です。OLE DB インターフェイスを実装するデータベース ベンダーは増えていますが、まだこのインターフェイスを公開していないデータ ソースもあります。ただし、現在使用されている事実上すべての DBMS システムは、ODBC によるアクセスが可能です。</span><span class="sxs-lookup"><span data-stu-id="b56d8-p101">To an ADO or RDS programmer, an ideal world would be one in which every data source exposes an OLE DB interface, so that ADO could call directly into the data source. Although increasingly more database vendors are implementing OLE DB interfaces, some data sources are not yet exposed this way. However, virtually all DBMS systems in use today can be accessed through ODBC.</span></span>

<span data-ttu-id="b56d8-107">ODBC ドライバーは、Microsoft SQL Server、Microsoft Access (Microsoft Jet データベース エンジン)、および Microsoft FoxPro だけでなく、Oracle などの Microsoft 以外のデータベース製品を含めた、現在使用されているすべての主要 DBMS で使用できます。</span><span class="sxs-lookup"><span data-stu-id="b56d8-107">ODBC drivers are available for every major DBMS in use today, including Microsoft SQL Server, Microsoft Access (Microsoft Jet database engine), and Microsoft FoxPro, in addition to non-Microsoft database products such as Oracle.</span></span>

<span data-ttu-id="b56d8-p102">ただし、Microsoft ODBC Provider を使用すると、ADO からすべての ODBC データ ソースに接続できます。このプロバイダーはフリースレッドであり、Unicode に対応しています。</span><span class="sxs-lookup"><span data-stu-id="b56d8-p102">The Microsoft ODBC Provider, however, allows ADO to connect to any ODBC data source. The provider is free-threaded and Unicode enabled.</span></span>

<span data-ttu-id="b56d8-p103">このプロバイダーはトランザクションをサポートしていますが、DBMS エンジンの種類によって、サポートするトランザクションの種類が異なります。たとえば、Microsoft Access は 5 レベルまでのネストされたトランザクションをサポートします。</span><span class="sxs-lookup"><span data-stu-id="b56d8-p103">The provider supports transactions, although different DBMS engines offer different types of transaction support. For example, Microsoft Access supports nested transactions up to five levels deep.</span></span>

<span data-ttu-id="b56d8-112">このプロバイダーは ADO の既定のプロバイダーであり、プロバイダーに依存するすべての ADO プロパティおよびメソッドをサポートします。</span><span class="sxs-lookup"><span data-stu-id="b56d8-112">This is the default provider for ADO, and all provider-dependent ADO properties and methods are supported.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="b56d8-113">接続文字列パラメーター</span><span class="sxs-lookup"><span data-stu-id="b56d8-113">Connection String Parameters</span></span>

<span data-ttu-id="b56d8-114">このプロバイダーに接続するには、**ConnectionString** プロパティの [Provider=](connectionstring-property-ado.md) 引数を次のように設定します。</span><span class="sxs-lookup"><span data-stu-id="b56d8-114">To connect to this provider, set the **Provider=** argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```sql 
 
MSDASQL 
```

<span data-ttu-id="b56d8-115">[Provider](provider-property-ado.md) プロパティを取得した場合も、この文字列が返されます。</span><span class="sxs-lookup"><span data-stu-id="b56d8-115">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="b56d8-116">標準的な接続文字列</span><span class="sxs-lookup"><span data-stu-id="b56d8-116">Typical Connection String</span></span>

<span data-ttu-id="b56d8-117">このプロバイダーの標準的な接続文字列を次に示します。</span><span class="sxs-lookup"><span data-stu-id="b56d8-117">A typical connection string for this provider is:</span></span>

```sql 
 
"Provider=MSDASQL;DSN=dsnName;UID=userName;PWD=userPassword;" 
```

<span data-ttu-id="b56d8-118">この文字列は、次に示すキーワードで構成されています。</span><span class="sxs-lookup"><span data-stu-id="b56d8-118">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b56d8-119">キーワード</span><span class="sxs-lookup"><span data-stu-id="b56d8-119">Keyword</span></span></p></th>
<th><p><span data-ttu-id="b56d8-120">説明</span><span class="sxs-lookup"><span data-stu-id="b56d8-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-121"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="b56d8-121"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="b56d8-122">OLE DB Provider for ODBC を指定します。</span><span class="sxs-lookup"><span data-stu-id="b56d8-122">Specifies the OLE DB Provider for ODBC.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-123"><strong>DSN</strong></span><span class="sxs-lookup"><span data-stu-id="b56d8-123"><strong>DSN</strong></span></span></p></td>
<td><p><span data-ttu-id="b56d8-124">データ ソース名を指定します。</span><span class="sxs-lookup"><span data-stu-id="b56d8-124">Specifies the data source name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-125"><strong>UID</strong></span><span class="sxs-lookup"><span data-stu-id="b56d8-125"><strong>UID</strong></span></span></p></td>
<td><p><span data-ttu-id="b56d8-126">ユーザー名を指定します。</span><span class="sxs-lookup"><span data-stu-id="b56d8-126">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-127"><strong>PWD</strong></span><span class="sxs-lookup"><span data-stu-id="b56d8-127"><strong>PWD</strong></span></span></p></td>
<td><p><span data-ttu-id="b56d8-128">ユーザー パスワードを指定します。</span><span class="sxs-lookup"><span data-stu-id="b56d8-128">Specifies the user password.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-129"><strong>URL</strong></span><span class="sxs-lookup"><span data-stu-id="b56d8-129"><strong>URL</strong></span></span></p></td>
<td><p><span data-ttu-id="b56d8-130">Web フォルダーに公開されているファイルまたはディレクトリの URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="b56d8-130">Specifies the URL of a file or directory published in a Web folder.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b56d8-131">このプロバイダーは ADO の既定のプロバイダーであるため、接続文字列で **Provider=** パラメーターを省略すると、このプロバイダーへの接続の確立が試行されます。</span><span class="sxs-lookup"><span data-stu-id="b56d8-131">Because this is the default provider for ADO, if you omit the **Provider=** parameter from the connection string, ADO will attempt to establish a connection to this provider.</span></span>

<span data-ttu-id="b56d8-p104">このプロバイダーは、ADO で定義されたパラメーター以外に独自の接続パラメーターをサポートしません。ただし、ADO 以外の接続パラメーターが指定されている場合は、ODBC ドライバー マネージャーに渡します。</span><span class="sxs-lookup"><span data-stu-id="b56d8-p104">The provider does not support any specific connection parameters in addition to those defined by ADO. However, the provider will pass any non-ADO connection parameters to the ODBC driver manager.</span></span>

<span data-ttu-id="b56d8-p105">**Provider** パラメーターを省略できるので、同じデータ ソースに対して ODBC 接続文字列と同じ ADO 接続文字列を作成できます。ODBC 接続文字列を作成するときと同じパラメーター名 (**DRIVER=**、**DATABASE=**、**DSN=** など)、値、および構文を使用します。定義済みのデータ ソース名 (DSN) または FileDSN を指定してもしなくても接続できます。</span><span class="sxs-lookup"><span data-stu-id="b56d8-p105">Because you can omit the **Provider** parameter, you can therefore compose an ADO connection string that is identical to an ODBC connection string for the same data source. Use the same parameter names (**DRIVER=**, **DATABASE=**, **DSN=**, and so on), values, and syntax as you would when composing an ODBC connection string. You can connect with or without a predefined data source name (DSN) or FileDSN.</span></span>

<span data-ttu-id="b56d8-137">**DSN または FileDSN を指定する場合の構文:**</span><span class="sxs-lookup"><span data-stu-id="b56d8-137">**Syntax with a DSN or FileDSN:**</span></span>

`"[Provider=MSDASQL;] { DSN=name | FileDSN=filename } ; [DATABASE=database;] UID=user; PWD=password"`

<span data-ttu-id="b56d8-138">**DSN 指定しない場合の構文 (DSN なしの接続):**</span><span class="sxs-lookup"><span data-stu-id="b56d8-138">**Syntax without a DSN (DSN-less connection):**</span></span>

`"[Provider=MSDASQL;] DRIVER=driver; SERVER=server;DATABASE=database; UID=user; PWD=password"`

<span data-ttu-id="b56d8-139">**DSN**または**FileDSN**を使用する場合は Windows のコントロール パネルの [ODBC データ ソース アドミニストレーターを使用する必要があります定義します。</span><span class="sxs-lookup"><span data-stu-id="b56d8-139">If you use a **DSN** or **FileDSN**, it must be defined through the ODBC Data Source Administrator in the Windows Control Panel.</span></span> <span data-ttu-id="b56d8-140">Microsoft Windows 2000 では、odbc データ ソース アドミニストレーターは管理ツールの下にあります。</span><span class="sxs-lookup"><span data-stu-id="b56d8-140">In Microsoft Windows 2000, the ODBC Administrator is located under Administrative Tools.</span></span> <span data-ttu-id="b56d8-141">以前のバージョンの Windows では、odbc データ ソース アドミニストレーター アイコンは**32 ビット ODBC**または**ODBC**では単に呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="b56d8-141">In previous versions of Windows, the ODBC Administrator icon is named **32-bit ODBC** or simply **ODBC**.</span></span>

<span data-ttu-id="b56d8-142">**DSN** を設定する代わりに、"SQL Server" などの ODBC ドライバー (**DRIVER=**)、サーバー名 (**SERVER=**)、およびデータベース名 (**DATABASE=**) を指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="b56d8-142">As an alternative to setting a **DSN**, you can specify the ODBC driver (**DRIVER=**), such as "SQL Server;" the server name (**SERVER=**); and the database name (**DATABASE=**).</span></span>

<span data-ttu-id="b56d8-143">ユーザー アカウント名 (**UID=**) と、そのユーザー アカウントのパスワード (**PWD=**) を、ODBC 固有のパラメーターまたは ADO で定義された標準的な *user* パラメーターと *password* パラメーターで指定できます。</span><span class="sxs-lookup"><span data-stu-id="b56d8-143">You can also specify a user account name (**UID=**), and the password for the user account (**PWD=**) in the ODBC-specific parameters or in the standard ADO-defined *user* and *password* parameters.</span></span>

<span data-ttu-id="b56d8-144">**DSN**の定義が既にデータベースを指定して、*別のデータベースに接続する**DSN**に加えて*データベース*パラメーター*を指定できます。</span><span class="sxs-lookup"><span data-stu-id="b56d8-144">Although a **DSN** definition already specifies a database, you can specify *a* *database* parameter in addition to a **DSN** to connect to a different database.</span></span> <span data-ttu-id="b56d8-145">**DSN**を使用するときに常に\**データベース*パラメーター\*を含めることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b56d8-145">It is a good idea to always include *the* *database* parameter when you use a **DSN**.</span></span> <span data-ttu-id="b56d8-146">これは、ように**DSN**の定義を確認した後、他のユーザーがデータベースの既定のパラメーターを変更する適切なデータベースに接続すること。</span><span class="sxs-lookup"><span data-stu-id="b56d8-146">This will ensure that you connect to the proper database in the event that another user changed the default database parameter since you last checked the **DSN** definition.</span></span>

## <a name="provider-specific-connection-properties"></a><span data-ttu-id="b56d8-147">プロバイダー固有の Connection のプロパティ</span><span class="sxs-lookup"><span data-stu-id="b56d8-147">Provider-Specific Connection Properties</span></span>

<span data-ttu-id="b56d8-p108">OLE DB Provider for ODBC は、 [Connection](properties-collection-ado.md) オブジェクトの **Properties** コレクションにプロパティを追加します。次の表は、これらのプロパティの一覧で、かっこ内は対応する OLE DB プロパティ名です。</span><span class="sxs-lookup"><span data-stu-id="b56d8-p108">The OLE DB provider for ODBC adds several properties to the [Properties](properties-collection-ado.md) collection of the **Connection** object. The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b56d8-150">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="b56d8-150">Property Name</span></span></p></th>
<th><p><span data-ttu-id="b56d8-151">説明</span><span class="sxs-lookup"><span data-stu-id="b56d8-151">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-152">アクセス手順</span><span class="sxs-lookup"><span data-stu-id="b56d8-152">Accessible Procedures</span></span><br />
<span data-ttu-id="b56d8-153">(KAGPROP_ACCESSIBLEPROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="b56d8-153">(KAGPROP_ACCESSIBLEPROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="b56d8-154">ユーザーがストアド プロシージャにアクセスできるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b56d8-154">Indicates whether the user has access to stored procedures.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-155">アクセス可能なテーブル</span><span class="sxs-lookup"><span data-stu-id="b56d8-155">Accessible Tables</span></span><br />
<span data-ttu-id="b56d8-156">(KAGPROP_ACCESSIBLETABLES)</span><span class="sxs-lookup"><span data-stu-id="b56d8-156">(KAGPROP_ACCESSIBLETABLES)</span></span></p></td>
<td><p><span data-ttu-id="b56d8-157">ユーザーがデータベースのテーブルに対して SELECT ステートメントを実行する権限を持つかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b56d8-157">Indicates whether the user has permission to execute SELECT statements against the database tables.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-158">アクティブなステートメント</span><span class="sxs-lookup"><span data-stu-id="b56d8-158">Active Statements</span></span><br />
<span data-ttu-id="b56d8-159">(KAGPROP_ACTIVESTATEMENTS)</span><span class="sxs-lookup"><span data-stu-id="b56d8-159">(KAGPROP_ACTIVESTATEMENTS)</span></span></p></td>
<td><p><span data-ttu-id="b56d8-160">ODBC ドライバーが 1 つの接続でサポートできるハンドル数を示します。</span><span class="sxs-lookup"><span data-stu-id="b56d8-160">Indicates the number of handles an ODBC driver can support on a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-161">ドライバー名</span><span class="sxs-lookup"><span data-stu-id="b56d8-161">Driver Name</span></span><br />
<span data-ttu-id="b56d8-162">(KAGPROP_DRIVERNAME)</span><span class="sxs-lookup"><span data-stu-id="b56d8-162">(KAGPROP_DRIVERNAME)</span></span></p></td>
<td><p><span data-ttu-id="b56d8-163">ODBC ドライバーのファイル名を示します。</span><span class="sxs-lookup"><span data-stu-id="b56d8-163">Indicates the file name of the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-164">ドライバーの ODBC バージョン</span><span class="sxs-lookup"><span data-stu-id="b56d8-164">Driver ODBC Version</span></span><br />
<span data-ttu-id="b56d8-165">(KAGPROP_DRIVERODBCVER)</span><span class="sxs-lookup"><span data-stu-id="b56d8-165">(KAGPROP_DRIVERODBCVER)</span></span></p></td>
<td><p><span data-ttu-id="b56d8-166">このドライバーがサポートする ODBC のバージョンを示します。</span><span class="sxs-lookup"><span data-stu-id="b56d8-166">Indicates the version of ODBC that this driver supports.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-167">ファイルの使用状況</span><span class="sxs-lookup"><span data-stu-id="b56d8-167">File Usage</span></span><br />
<span data-ttu-id="b56d8-168">(KAGPROP_FILEUSAGE)</span><span class="sxs-lookup"><span data-stu-id="b56d8-168">(KAGPROP_FILEUSAGE)</span></span></p></td>
<td><p><span data-ttu-id="b56d8-169">ドライバーがデータ ソース内のファイルを、テーブルとして扱うか、カタログとして扱うかを示します。</span><span class="sxs-lookup"><span data-stu-id="b56d8-169">Indicates how the driver treats a file in a data source; as a table or as a catalog.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-170">エスケープ句のように</span><span class="sxs-lookup"><span data-stu-id="b56d8-170">Like Escape Clause</span></span><br />
<span data-ttu-id="b56d8-171">(KAGPROP_LIKEESCAPECLAUSE)</span><span class="sxs-lookup"><span data-stu-id="b56d8-171">(KAGPROP_LIKEESCAPECLAUSE)</span></span></p></td>
<td><p><span data-ttu-id="b56d8-172">ドライバーが、WHERE 句の LIKE 述語でパーセント記号 (%) および下線記号 (_) のエスケープ文字を定義および使用できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b56d8-172">Indicates whether the driver supports the definition and use of an escape character for the percent character (%) and underline character (_) in the LIKE predicate of a WHERE clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-173">によるグループ内の最大列</span><span class="sxs-lookup"><span data-stu-id="b56d8-173">Max Columns in Group By</span></span><br />
<span data-ttu-id="b56d8-174">(KAGPROP_MAXCOLUMNSINGROUPBY)</span><span class="sxs-lookup"><span data-stu-id="b56d8-174">(KAGPROP_MAXCOLUMNSINGROUPBY)</span></span></p></td>
<td><p><span data-ttu-id="b56d8-175">SELECT ステートメントの GROUP BY 句に記述できる最大列数を示します。</span><span class="sxs-lookup"><span data-stu-id="b56d8-175">Indicates the maximum number of columns that can be listed in the GROUP BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-176">インデックスの最大列</span><span class="sxs-lookup"><span data-stu-id="b56d8-176">Max Columns in Index</span></span><br />
<span data-ttu-id="b56d8-177">(KAGPROP_MAXCOLUMNSININDEX)</span><span class="sxs-lookup"><span data-stu-id="b56d8-177">(KAGPROP_MAXCOLUMNSININDEX)</span></span></p></td>
<td><p><span data-ttu-id="b56d8-178">インデックスに格納できる最大列数を示します。</span><span class="sxs-lookup"><span data-stu-id="b56d8-178">Indicates the maximum number of columns that can be included in an index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-179">Order By の中の最大列</span><span class="sxs-lookup"><span data-stu-id="b56d8-179">Max Columns in Order By</span></span><br />
<span data-ttu-id="b56d8-180">(KAGPROP_MAXCOLUMNSINORDERBY)</span><span class="sxs-lookup"><span data-stu-id="b56d8-180">(KAGPROP_MAXCOLUMNSINORDERBY)</span></span></p></td>
<td><p><span data-ttu-id="b56d8-181">SELECT ステートメントの ORDER BY 句に記述できる最大列数を示します。</span><span class="sxs-lookup"><span data-stu-id="b56d8-181">Indicates the maximum number of columns that can be listed in the ORDER BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-182">選択中の最大列</span><span class="sxs-lookup"><span data-stu-id="b56d8-182">Max Columns in Select</span></span><br />
<span data-ttu-id="b56d8-183">(KAGPROP_MAXCOLUMNSINSELECT)</span><span class="sxs-lookup"><span data-stu-id="b56d8-183">(KAGPROP_MAXCOLUMNSINSELECT)</span></span></p></td>
<td><p><span data-ttu-id="b56d8-184">SELECT ステートメントの SELECT 部分に記述できる最大列数を示します。</span><span class="sxs-lookup"><span data-stu-id="b56d8-184">Indicates the maximum number of columns that can be listed in the SELECT portion of a SELECT statement.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-185">テーブルの最大列</span><span class="sxs-lookup"><span data-stu-id="b56d8-185">Max Columns in Table</span></span><br />
<span data-ttu-id="b56d8-186">(KAGPROP_MAXCOLUMNSINTABLE)</span><span class="sxs-lookup"><span data-stu-id="b56d8-186">(KAGPROP_MAXCOLUMNSINTABLE)</span></span></p></td>
<td><p><span data-ttu-id="b56d8-187">テーブルの最大列数を示します。</span><span class="sxs-lookup"><span data-stu-id="b56d8-187">Indicates the maximum number of columns allowed in a table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-188">数値を処理する関数</span><span class="sxs-lookup"><span data-stu-id="b56d8-188">Numeric Functions</span></span><br />
<span data-ttu-id="b56d8-189">(KAGPROP_NUMERICFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="b56d8-189">(KAGPROP_NUMERICFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="b56d8-p109">ODBC ドライバーがサポートする数値関数を示します。関数名とこのビットマスクで使用される関連付けられた値の一覧については、ODBC マニュアルの「Appendix E: Scalar Functions」 (英語) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b56d8-p109">Indicates which numeric functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-192">外部結合の機能</span><span class="sxs-lookup"><span data-stu-id="b56d8-192">Outer Join Capabilities</span></span><br />
<span data-ttu-id="b56d8-193">(KAGPROP_OJCAPABILITY)</span><span class="sxs-lookup"><span data-stu-id="b56d8-193">(KAGPROP_OJCAPABILITY)</span></span></p></td>
<td><p><span data-ttu-id="b56d8-194">プロバイダーがサポートする OUTER JOIN の種類を示します。</span><span class="sxs-lookup"><span data-stu-id="b56d8-194">Indicates the types of OUTER JOINs supported by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-195">外部結合</span><span class="sxs-lookup"><span data-stu-id="b56d8-195">Outer Joins</span></span><br />
<span data-ttu-id="b56d8-196">(KAGPROP_OUTERJOINS)</span><span class="sxs-lookup"><span data-stu-id="b56d8-196">(KAGPROP_OUTERJOINS)</span></span></p></td>
<td><p><span data-ttu-id="b56d8-197">プロバイダーが OUTER JOIN をサポートするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b56d8-197">Indicates whether the provider supports OUTER JOINs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-198">特殊文字</span><span class="sxs-lookup"><span data-stu-id="b56d8-198">Special Characters</span></span><br />
<span data-ttu-id="b56d8-199">(KAGPROP_SPECIALCHARACTERS)</span><span class="sxs-lookup"><span data-stu-id="b56d8-199">(KAGPROP_SPECIALCHARACTERS)</span></span></p></td>
<td><p><span data-ttu-id="b56d8-200">ODBC ドライバーで特別な意味を持つ文字を示します。</span><span class="sxs-lookup"><span data-stu-id="b56d8-200">Indicates which characters have special meaning for the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-201">ストアド プロシージャ</span><span class="sxs-lookup"><span data-stu-id="b56d8-201">Stored Procedures</span></span><br />
<span data-ttu-id="b56d8-202">(KAGPROP_PROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="b56d8-202">(KAGPROP_PROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="b56d8-203">この ODBC ドライバーでストアド プロシージャを使用できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b56d8-203">Indicates whether stored procedures are available for use with this ODBC driver.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-204">文字列を処理する関数</span><span class="sxs-lookup"><span data-stu-id="b56d8-204">String Functions</span></span><br />
<span data-ttu-id="b56d8-205">(KAGPROP_STRINGFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="b56d8-205">(KAGPROP_STRINGFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="b56d8-p110">ODBC ドライバーがサポートする文字列関数を示します。関数名とこのビットマスクで使用される関連付けられた値の一覧については、ODBC マニュアルの「Appendix E: Scalar Functions」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b56d8-p110">Indicates which string functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-208">システム関数</span><span class="sxs-lookup"><span data-stu-id="b56d8-208">System Functions</span></span><br />
<span data-ttu-id="b56d8-209">(KAGPROP_SYSTEMFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="b56d8-209">(KAGPROP_SYSTEMFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="b56d8-p111">ODBC ドライバーがサポートするシステム関数を示します。関数名とこのビットマスクで使用される関連付けられた値の一覧については、ODBC マニュアルの「Appendix E: Scalar Functions」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b56d8-p111">Indicates which system functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-212">日付/時刻関数</span><span class="sxs-lookup"><span data-stu-id="b56d8-212">Time/Date Functions</span></span><br />
<span data-ttu-id="b56d8-213">(KAGPROP_TIMEDATEFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="b56d8-213">(KAGPROP_TIMEDATEFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="b56d8-p112">ODBC ドライバーがサポートする時刻/日付関数を示します。関数名とこのビットマスクで使用される関連付けられた値の一覧については、ODBC マニュアルの「Appendix E: Scalar Functions」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b56d8-p112">Indicates which time and date functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-216">SQL の文法のサポート</span><span class="sxs-lookup"><span data-stu-id="b56d8-216">SQL Grammar Support</span></span><br />
<span data-ttu-id="b56d8-217">(KAGPROP_ODBCSQLCONFORMANCE)</span><span class="sxs-lookup"><span data-stu-id="b56d8-217">(KAGPROP_ODBCSQLCONFORMANCE)</span></span></p></td>
<td><p><span data-ttu-id="b56d8-218">ODBC ドライバーがサポートする SQL 文法を示します。</span><span class="sxs-lookup"><span data-stu-id="b56d8-218">Indicates the SQL grammar that the ODBC driver supports.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a><span data-ttu-id="b56d8-219">プロバイダー固有の Recordset および Command のプロパティ</span><span class="sxs-lookup"><span data-stu-id="b56d8-219">Provider-Specific Recordset and Command Properties</span></span>

<span data-ttu-id="b56d8-p113">OLE DB Provider for ODBC は、 **Recordset** オブジェクトと **Command** オブジェクトの **Properties** コレクションにプロパティを追加します。次の表は、これらのプロパティの一覧で、かっこ内は対応する OLE DB プロパティ名です。</span><span class="sxs-lookup"><span data-stu-id="b56d8-p113">The OLE DB provider for ODBC adds several properties to the **Properties** collection of the **Recordset** and **Command** objects. The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b56d8-222">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="b56d8-222">Property Name</span></span></p></th>
<th><p><span data-ttu-id="b56d8-223">説明</span><span class="sxs-lookup"><span data-stu-id="b56d8-223">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-224">クエリベースの更新/削除/挿入</span><span class="sxs-lookup"><span data-stu-id="b56d8-224">Query Based Updates/Deletes/Inserts</span></span><br />
<span data-ttu-id="b56d8-225">(KAGPROP_QUERYBASEDUPDATES)</span><span class="sxs-lookup"><span data-stu-id="b56d8-225">(KAGPROP_QUERYBASEDUPDATES)</span></span></p></td>
<td><p><span data-ttu-id="b56d8-226">SQL クエリを使用して更新、削除、および挿入を実行できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b56d8-226">Indicates whether updates, deletions, and insertions can be performed using SQL queries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-227">ODBC の同時実行の種類</span><span class="sxs-lookup"><span data-stu-id="b56d8-227">ODBC Concurrency Type</span></span><br />
<span data-ttu-id="b56d8-228">(KAGPROP_CONCURRENCY)</span><span class="sxs-lookup"><span data-stu-id="b56d8-228">(KAGPROP_CONCURRENCY)</span></span></p></td>
<td><p><span data-ttu-id="b56d8-229">2 人のユーザーがデータ ソースの同じデータに同時にアクセスしようとしたときに発生する問題を減少させるための方法を示します。</span><span class="sxs-lookup"><span data-stu-id="b56d8-229">Indicates the method used to reduce potential problems caused by two users attempting to access the same data from the data source simultaneously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-230">順方向専用カーソルの BLOB のアクセシビリティ</span><span class="sxs-lookup"><span data-stu-id="b56d8-230">BLOB accessibility on Forward-Only cursor</span></span><br />
<span data-ttu-id="b56d8-231">(KAGPROP_BLOBSONFOCURSOR)</span><span class="sxs-lookup"><span data-stu-id="b56d8-231">(KAGPROP_BLOBSONFOCURSOR)</span></span></p></td>
<td><p><span data-ttu-id="b56d8-232">前方のみのカーソルの使用時に BLOB <strong>Fields</strong> にアクセスできるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b56d8-232">Indicates whether BLOB <strong>Fields</strong> can be accessed when using a forward-only cursor.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-233">SQL_FLOAT、SQL_DOUBLE、および SQL_REAL を QBU WHERE 句に含める</span><span class="sxs-lookup"><span data-stu-id="b56d8-233">Include SQL_FLOAT, SQL_DOUBLE, and SQL_REAL in QBU WHERE clauses</span></span><br />
<span data-ttu-id="b56d8-234">(KAGPROP_INCLUDENONEXACT)</span><span class="sxs-lookup"><span data-stu-id="b56d8-234">(KAGPROP_INCLUDENONEXACT)</span></span></p></td>
<td><p><span data-ttu-id="b56d8-235">SQL_FLOAT、SQL_DOUBLE、および SQL_REAL の値を QBU WHERE 句に含めることができるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b56d8-235">Indicates whether SQL_FLOAT, SQL_DOUBLE, and SQL_REAL values can be included in a QBU WHERE clause.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-236">挿入後の最後の行の位置</span><span class="sxs-lookup"><span data-stu-id="b56d8-236">Position on the last row after insert</span></span><br />
<span data-ttu-id="b56d8-237">(KAGPROP_POSITIONONNEWROW)</span><span class="sxs-lookup"><span data-stu-id="b56d8-237">(KAGPROP_POSITIONONNEWROW)</span></span></p></td>
<td><p><span data-ttu-id="b56d8-238">新規レコードをテーブルに挿入した後、テーブルの最後の行が現在の行になるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b56d8-238">Indicates that after a new record has been inserted in a table, the last row in the table will be come the current row.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-239">IRowsetChangeExtInfo</span><span class="sxs-lookup"><span data-stu-id="b56d8-239">IRowsetChangeExtInfo</span></span><br />
<span data-ttu-id="b56d8-240">(KAGPROP_IROWSETCHANGEEXTINFO)</span><span class="sxs-lookup"><span data-stu-id="b56d8-240">(KAGPROP_IROWSETCHANGEEXTINFO)</span></span></p></td>
<td><p><span data-ttu-id="b56d8-241"><strong>IRowsetChange</strong> インターフェイスが拡張情報を提供するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b56d8-241">Indicates whether the <strong>IRowsetChange</strong> interface provides extended information support.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-242">ODBC カーソルの種類</span><span class="sxs-lookup"><span data-stu-id="b56d8-242">ODBC Cursor Type</span></span><br />
<span data-ttu-id="b56d8-243">(KAGPROP_CURSOR)</span><span class="sxs-lookup"><span data-stu-id="b56d8-243">(KAGPROP_CURSOR)</span></span></p></td>
<td><p><span data-ttu-id="b56d8-244"><strong>Recordset</strong> で使用されるカーソルの種類を示します。</span><span class="sxs-lookup"><span data-stu-id="b56d8-244">Indicates the type of cursor used by the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-245">マーシャ リングできる行セットを生成します。</span><span class="sxs-lookup"><span data-stu-id="b56d8-245">Generate a Rowset that can be marshaled</span></span><br />
<span data-ttu-id="b56d8-246">(KAGPROP_MARSHALLABLE)</span><span class="sxs-lookup"><span data-stu-id="b56d8-246">(KAGPROP_MARSHALLABLE)</span></span></p></td>
<td><p><span data-ttu-id="b56d8-247">ODBC ドライバーがマーシャリング可能なレコードセットを生成することを示します。</span><span class="sxs-lookup"><span data-stu-id="b56d8-247">Indicates that the ODBC driver generates a recordset that can be marshaled</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a><span data-ttu-id="b56d8-248">コマンド テキスト</span><span class="sxs-lookup"><span data-stu-id="b56d8-248">Command Text</span></span>

<span data-ttu-id="b56d8-249">[Command](command-object-ado.md) オブジェクトの使用方法は、データ ソースおよび受け付けられるクエリまたはコマンド ステートメントの種類によって大きく異なります。</span><span class="sxs-lookup"><span data-stu-id="b56d8-249">How you use the [Command](command-object-ado.md) object largely depends on the data source, and what type of query or command statement it will accept.</span></span>

<span data-ttu-id="b56d8-250">ODBC には、ストアド プロシージャを呼び出すための独自の構文があります。</span><span class="sxs-lookup"><span data-stu-id="b56d8-250">ODBC provides a specific syntax for calling stored procedures.</span></span> <span data-ttu-id="b56d8-251">**コマンド**オブジェクト、 [Connection](connection-object-ado.md)オブジェクトの**Execute**メソッドの*CommandText*引数、または[Recordset](recordset-object-ado.md)の**Open**メソッドの*Source*引数の[CommandText](commandtext-property-ado.md)プロパティのオブジェクトは、この構文を使用して文字列に渡します。</span><span class="sxs-lookup"><span data-stu-id="b56d8-251">For the [CommandText](commandtext-property-ado.md) property of a **Command** object, the *CommandText* argument to the **Execute** method on a [Connection](connection-object-ado.md) object, or the *Source* argument to the **Open** method on a [Recordset](recordset-object-ado.md) object, passes in a string with this syntax:</span></span>

`"{ [ ? = ] call procedure [ ( ? [, ? [ ,  ]] ) ] }"`

<span data-ttu-id="b56d8-p115">**?** はそれぞれ [Parameters](parameters-collection-ado.md) コレクションのオブジェクトを参照します。最初の **?** は **Parameters**(0) を参照し、次の **?** は **Parameters**(1) を参照し、以下同様に続きます。</span><span class="sxs-lookup"><span data-stu-id="b56d8-p115">Each **?** references an object in the [Parameters](parameters-collection-ado.md) collection. The first **?** references **Parameters**(0), the next **?** references **Parameters**(1), and so on.</span></span>

<span data-ttu-id="b56d8-p116">パラメーターの参照は省略可能で、ストアド プロシージャの構造に依存します。パラメーターを定義していないストアド プロシージャを呼び出す場合の構文は、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="b56d8-p116">The parameter references are optional and depend on the structure of the stored procedure. If you want to call a stored procedure that defines no parameters, your string would look like this:</span></span>

`"{ call procedure }"`

<span data-ttu-id="b56d8-259">2 つのクエリ パラメーターを持つ場合は、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="b56d8-259">If you have two query parameters, your string would look like this:</span></span>

`"{ call procedure ( ?, ? ) }"`

<span data-ttu-id="b56d8-p117">ストアド プロシージャが値を返す場合、戻り値は別のパラメーターとして扱われます。クエリ パラメーターがなく、戻り値がある場合は、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="b56d8-p117">If the stored procedure will return a value, the return value is treated as another parameter. If you have no query parameters but you do have a return value, your string would look like this:</span></span>

`"{ ? = call procedure }"`

<span data-ttu-id="b56d8-262">戻り値があり、2 つのクエリ パラメーターがある場合は、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="b56d8-262">Finally, if you have a return value and two query parameters, your string would look like this:</span></span>

`"{ ? = call procedure ( ?, ? ) }"`

## <a name="recordset-behavior"></a><span data-ttu-id="b56d8-263">Recordset の動作</span><span class="sxs-lookup"><span data-stu-id="b56d8-263">Recordset Behavior</span></span>

<span data-ttu-id="b56d8-264">次の表は、このプロバイダーで開かれた **Recordset** オブジェクトで利用可能な標準の ADO メソッドと ADO プロパティの一覧です。</span><span class="sxs-lookup"><span data-stu-id="b56d8-264">The following tables list the standard ADO methods and properties available on a **Recordset** object opened with this provider.</span></span>

<span data-ttu-id="b56d8-265">プロバイダーの構成による **Recordset** の動作の詳細については、 [Supports](supports-method-ado.md) メソッドを実行し、 **Recordset** の **Properties** コレクションを列挙して、プロバイダー固有の動的プロパティが存在するかどうかを確認してください。</span><span class="sxs-lookup"><span data-stu-id="b56d8-265">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the **Properties** collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="b56d8-266">標準的な ADO **Recordset** のプロパティの利用可能性は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="b56d8-266">Availability of standard ADO **Recordset** properties:</span></span>

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
<th><p><span data-ttu-id="b56d8-267">プロパティ</span><span class="sxs-lookup"><span data-stu-id="b56d8-267">Property</span></span></p></th>
<th><p><span data-ttu-id="b56d8-268">前方向</span><span class="sxs-lookup"><span data-stu-id="b56d8-268">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="b56d8-269">動的</span><span class="sxs-lookup"><span data-stu-id="b56d8-269">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="b56d8-270">キーセット</span><span class="sxs-lookup"><span data-stu-id="b56d8-270">Keyset</span></span></p></th>
<th><p><span data-ttu-id="b56d8-271">静的</span><span class="sxs-lookup"><span data-stu-id="b56d8-271">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-272"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="b56d8-272"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="b56d8-273">利用不可</span><span class="sxs-lookup"><span data-stu-id="b56d8-273">not available</span></span></p></td>
<td><p><span data-ttu-id="b56d8-274">利用不可</span><span class="sxs-lookup"><span data-stu-id="b56d8-274">not available</span></span></p></td>
<td><p><span data-ttu-id="b56d8-275">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-275">read/write</span></span></p></td>
<td><p><span data-ttu-id="b56d8-276">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-276">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-277"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="b56d8-277"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="b56d8-278">利用不可</span><span class="sxs-lookup"><span data-stu-id="b56d8-278">not available</span></span></p></td>
<td><p><span data-ttu-id="b56d8-279">利用不可</span><span class="sxs-lookup"><span data-stu-id="b56d8-279">not available</span></span></p></td>
<td><p><span data-ttu-id="b56d8-280">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-280">read/write</span></span></p></td>
<td><p><span data-ttu-id="b56d8-281">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-281">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-282"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="b56d8-282"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="b56d8-283">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-283">read/write</span></span></p></td>
<td><p><span data-ttu-id="b56d8-284">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-284">read/write</span></span></p></td>
<td><p><span data-ttu-id="b56d8-285">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-285">read/write</span></span></p></td>
<td><p><span data-ttu-id="b56d8-286">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-286">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-287"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="b56d8-287"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="b56d8-288">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="b56d8-288">read-only</span></span></p></td>
<td><p><span data-ttu-id="b56d8-289">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="b56d8-289">read-only</span></span></p></td>
<td><p><span data-ttu-id="b56d8-290">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="b56d8-290">read-only</span></span></p></td>
<td><p><span data-ttu-id="b56d8-291">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="b56d8-291">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-292"><a href="bookmark-property-ado.md">Bookmark</a></span><span class="sxs-lookup"><span data-stu-id="b56d8-292"><a href="bookmark-property-ado.md">Bookmark</a></span></span></p></td>
<td><p><span data-ttu-id="b56d8-293">利用不可</span><span class="sxs-lookup"><span data-stu-id="b56d8-293">not available</span></span></p></td>
<td><p><span data-ttu-id="b56d8-294">利用不可</span><span class="sxs-lookup"><span data-stu-id="b56d8-294">not available</span></span></p></td>
<td><p><span data-ttu-id="b56d8-295">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-295">read/write</span></span></p></td>
<td><p><span data-ttu-id="b56d8-296">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-296">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-297"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="b56d8-297"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="b56d8-298">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-298">read/write</span></span></p></td>
<td><p><span data-ttu-id="b56d8-299">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-299">read/write</span></span></p></td>
<td><p><span data-ttu-id="b56d8-300">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-300">read/write</span></span></p></td>
<td><p><span data-ttu-id="b56d8-301">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-301">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-302"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="b56d8-302"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="b56d8-303">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-303">read/write</span></span></p></td>
<td><p><span data-ttu-id="b56d8-304">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-304">read/write</span></span></p></td>
<td><p><span data-ttu-id="b56d8-305">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-305">read/write</span></span></p></td>
<td><p><span data-ttu-id="b56d8-306">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-306">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-307"><a href="cursortype-property-ado.md">カーソル。</a></span><span class="sxs-lookup"><span data-stu-id="b56d8-307"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="b56d8-308">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-308">read/write</span></span></p></td>
<td><p><span data-ttu-id="b56d8-309">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-309">read/write</span></span></p></td>
<td><p><span data-ttu-id="b56d8-310">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-310">read/write</span></span></p></td>
<td><p><span data-ttu-id="b56d8-311">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-311">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-312"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="b56d8-312"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="b56d8-313">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="b56d8-313">read-only</span></span></p></td>
<td><p><span data-ttu-id="b56d8-314">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="b56d8-314">read-only</span></span></p></td>
<td><p><span data-ttu-id="b56d8-315">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="b56d8-315">read-only</span></span></p></td>
<td><p><span data-ttu-id="b56d8-316">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="b56d8-316">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-317"><a href="filter-property-ado.md">Filter</a></span><span class="sxs-lookup"><span data-stu-id="b56d8-317"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="b56d8-318">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-318">read/write</span></span></p></td>
<td><p><span data-ttu-id="b56d8-319">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-319">read/write</span></span></p></td>
<td><p><span data-ttu-id="b56d8-320">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-320">read/write</span></span></p></td>
<td><p><span data-ttu-id="b56d8-321">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-321">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-322"><a href="locktype-property-ado.md">ロック。</a></span><span class="sxs-lookup"><span data-stu-id="b56d8-322"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="b56d8-323">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-323">read/write</span></span></p></td>
<td><p><span data-ttu-id="b56d8-324">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-324">read/write</span></span></p></td>
<td><p><span data-ttu-id="b56d8-325">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-325">read/write</span></span></p></td>
<td><p><span data-ttu-id="b56d8-326">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-326">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-327"><a href="marshaloptions-property-ado.md">スレッド</a></span><span class="sxs-lookup"><span data-stu-id="b56d8-327"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="b56d8-328">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-328">read/write</span></span></p></td>
<td><p><span data-ttu-id="b56d8-329">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-329">read/write</span></span></p></td>
<td><p><span data-ttu-id="b56d8-330">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-330">read/write</span></span></p></td>
<td><p><span data-ttu-id="b56d8-331">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-331">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-332"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="b56d8-332"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="b56d8-333">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-333">read/write</span></span></p></td>
<td><p><span data-ttu-id="b56d8-334">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-334">read/write</span></span></p></td>
<td><p><span data-ttu-id="b56d8-335">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-335">read/write</span></span></p></td>
<td><p><span data-ttu-id="b56d8-336">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-336">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-337"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="b56d8-337"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="b56d8-338">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-338">read/write</span></span></p></td>
<td><p><span data-ttu-id="b56d8-339">利用不可</span><span class="sxs-lookup"><span data-stu-id="b56d8-339">not available</span></span></p></td>
<td><p><span data-ttu-id="b56d8-340">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="b56d8-340">read-only</span></span></p></td>
<td><p><span data-ttu-id="b56d8-341">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="b56d8-341">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-342"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="b56d8-342"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="b56d8-343">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-343">read/write</span></span></p></td>
<td><p><span data-ttu-id="b56d8-344">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-344">read/write</span></span></p></td>
<td><p><span data-ttu-id="b56d8-345">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-345">read/write</span></span></p></td>
<td><p><span data-ttu-id="b56d8-346">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-346">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-347"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="b56d8-347"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="b56d8-348">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-348">read/write</span></span></p></td>
<td><p><span data-ttu-id="b56d8-349">利用不可</span><span class="sxs-lookup"><span data-stu-id="b56d8-349">not available</span></span></p></td>
<td><p><span data-ttu-id="b56d8-350">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="b56d8-350">read-only</span></span></p></td>
<td><p><span data-ttu-id="b56d8-351">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="b56d8-351">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-352"><a href="source-property-ado-recordset.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="b56d8-352"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="b56d8-353">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-353">read/write</span></span></p></td>
<td><p><span data-ttu-id="b56d8-354">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-354">read/write</span></span></p></td>
<td><p><span data-ttu-id="b56d8-355">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-355">read/write</span></span></p></td>
<td><p><span data-ttu-id="b56d8-356">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="b56d8-356">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-357"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="b56d8-357"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="b56d8-358">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="b56d8-358">read-only</span></span></p></td>
<td><p><span data-ttu-id="b56d8-359">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="b56d8-359">read-only</span></span></p></td>
<td><p><span data-ttu-id="b56d8-360">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="b56d8-360">read-only</span></span></p></td>
<td><p><span data-ttu-id="b56d8-361">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="b56d8-361">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-362"><a href="status-property-ado-recordset.md">Status</a></span><span class="sxs-lookup"><span data-stu-id="b56d8-362"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="b56d8-363">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="b56d8-363">read-only</span></span></p></td>
<td><p><span data-ttu-id="b56d8-364">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="b56d8-364">read-only</span></span></p></td>
<td><p><span data-ttu-id="b56d8-365">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="b56d8-365">read-only</span></span></p></td>
<td><p><span data-ttu-id="b56d8-366">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="b56d8-366">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b56d8-367">バージョン 1.0 の Microsoft OLE DB Provider for ODBC で ADO を使用する場合、[AbsolutePosition](absoluteposition-property-ado.md) プロパティと [AbsolutePage](absolutepage-property-ado.md) プロパティは値の設定のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="b56d8-367">The [AbsolutePosition](absoluteposition-property-ado.md) and [AbsolutePage](absolutepage-property-ado.md) properties are write-only when ADO is used with version 1.0 of the Microsoft OLE DB Provider for ODBC.</span></span>

<span data-ttu-id="b56d8-368">標準的な ADO **Recordset** のメソッドの利用可能性は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="b56d8-368">Availability of standard ADO **Recordset** methods:</span></span>

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
<th><p><span data-ttu-id="b56d8-369">メソッド</span><span class="sxs-lookup"><span data-stu-id="b56d8-369">Method</span></span></p></th>
<th><p><span data-ttu-id="b56d8-370">前方向</span><span class="sxs-lookup"><span data-stu-id="b56d8-370">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="b56d8-371">動的</span><span class="sxs-lookup"><span data-stu-id="b56d8-371">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="b56d8-372">キーセット</span><span class="sxs-lookup"><span data-stu-id="b56d8-372">Keyset</span></span></p></th>
<th><p><span data-ttu-id="b56d8-373">静的</span><span class="sxs-lookup"><span data-stu-id="b56d8-373">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-374"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="b56d8-374"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="b56d8-375">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-375">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-376">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-376">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-377">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-377">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-378">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-378">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-379"><a href="cancel-method-ado.md">Cancel</a></span><span class="sxs-lookup"><span data-stu-id="b56d8-379"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="b56d8-380">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-380">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-381">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-381">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-382">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-382">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-383">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-383">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-384"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="b56d8-384"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="b56d8-385">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-385">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-386">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-386">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-387">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-387">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-388">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-388">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-389"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="b56d8-389"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="b56d8-390">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-390">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-391">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-391">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-392">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-392">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-393">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-393">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-394"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="b56d8-394"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="b56d8-395">いいえ</span><span class="sxs-lookup"><span data-stu-id="b56d8-395">No</span></span></p></td>
<td><p><span data-ttu-id="b56d8-396">いいえ</span><span class="sxs-lookup"><span data-stu-id="b56d8-396">No</span></span></p></td>
<td><p><span data-ttu-id="b56d8-397">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-397">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-398">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-398">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-399"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="b56d8-399"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="b56d8-400">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-400">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-401">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-401">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-402">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-402">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-403">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-403">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-404"><a href="delete-method-ado-recordset.md">Delete</a></span><span class="sxs-lookup"><span data-stu-id="b56d8-404"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="b56d8-405">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-405">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-406">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-406">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-407">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-407">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-408">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-408">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-409"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="b56d8-409"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="b56d8-410">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-410">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-411">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-411">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-412">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-412">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-413">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-413">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-414"><a href="move-method-ado.md">Move</a></span><span class="sxs-lookup"><span data-stu-id="b56d8-414"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="b56d8-415">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-415">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-416">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-416">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-417">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-417">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-418">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-418">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-419"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="b56d8-419"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="b56d8-420">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-420">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-421">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-421">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-422">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-422">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-423">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-423">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-424"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span><span class="sxs-lookup"><span data-stu-id="b56d8-424"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span></span></p></td>
<td><p><span data-ttu-id="b56d8-425">いいえ</span><span class="sxs-lookup"><span data-stu-id="b56d8-425">No</span></span></p></td>
<td><p><span data-ttu-id="b56d8-426">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-426">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-427">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-427">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-428">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-428">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-429"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span><span class="sxs-lookup"><span data-stu-id="b56d8-429"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span></span></p></td>
<td><p><span data-ttu-id="b56d8-430">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-430">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-431">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-431">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-432">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-432">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-433">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-433">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-434"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="b56d8-434"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="b56d8-435">いいえ</span><span class="sxs-lookup"><span data-stu-id="b56d8-435">No</span></span></p></td>
<td><p><span data-ttu-id="b56d8-436">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-436">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-437">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-437">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-438">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-438">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-439"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span><span class="sxs-lookup"><span data-stu-id="b56d8-439"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span></span></p></td>
<td><p><span data-ttu-id="b56d8-440">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-440">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-441">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-441">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-442">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-442">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-443">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-443">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-444"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="b56d8-444"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="b56d8-445">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-445">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-446">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-446">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-447">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-447">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-448">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-448">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-449"><a href="requery-method-ado.md">Requery</a></span><span class="sxs-lookup"><span data-stu-id="b56d8-449"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="b56d8-450">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-450">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-451">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-451">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-452">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-452">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-453">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-453">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-454"><a href="resync-method-ado.md">再同期</a></span><span class="sxs-lookup"><span data-stu-id="b56d8-454"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="b56d8-455">いいえ</span><span class="sxs-lookup"><span data-stu-id="b56d8-455">No</span></span></p></td>
<td><p><span data-ttu-id="b56d8-456">いいえ</span><span class="sxs-lookup"><span data-stu-id="b56d8-456">No</span></span></p></td>
<td><p><span data-ttu-id="b56d8-457">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-457">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-458">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-458">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-459"><a href="supports-method-ado.md">サポートしています</a></span><span class="sxs-lookup"><span data-stu-id="b56d8-459"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="b56d8-460">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-460">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-461">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-461">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-462">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-462">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-463">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-463">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-464"><a href="update-method-ado.md">Update</a></span><span class="sxs-lookup"><span data-stu-id="b56d8-464"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="b56d8-465">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-465">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-466">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-466">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-467">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-467">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-468">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-468">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-469"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="b56d8-469"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="b56d8-470">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-470">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-471">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-471">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-472">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-472">Yes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-473">はい</span><span class="sxs-lookup"><span data-stu-id="b56d8-473">Yes</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b56d8-474">\*Microsoft Access データベースではサポートされません。</span><span class="sxs-lookup"><span data-stu-id="b56d8-474">\*Not supported for Microsoft Access databases.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="b56d8-475">動的プロパティ</span><span class="sxs-lookup"><span data-stu-id="b56d8-475">Dynamic Properties</span></span>

<span data-ttu-id="b56d8-476">Microsoft OLE DB Provider for ODBC は、開かれていない **Connection** オブジェクト、 [Recordset](connection-object-ado.md) オブジェクト、および [Command](recordset-object-ado.md) オブジェクトの [Properties](command-object-ado.md) コレクションに動的プロパティを挿入します。</span><span class="sxs-lookup"><span data-stu-id="b56d8-476">The Microsoft OLE DB Provider for ODBC inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="b56d8-p118">以下の表は、各動的プロパティの ADO 名と OLE DB 名の対応表です。 「OLE DB プログラマ リファレンス」では、「説明」欄に ADO プロパティ名が示されています。プロパティの詳細については、「OLE DB プログラマ リファレンス」を参照してください。OLE DB プロパティ名をキーワードとして検索するか、「付録 C: プロパティ表」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b56d8-p118">The tables below are a cross-index of the ADO and OLE DB names for each dynamic property. The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description." You can find more information about these properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="b56d8-481">Connection の動的プロパティ</span><span class="sxs-lookup"><span data-stu-id="b56d8-481">Connection Dynamic Properties</span></span>

<span data-ttu-id="b56d8-482">次に示すプロパティが **Connection** オブジェクトの **Properties** コレクションに追加されます。</span><span class="sxs-lookup"><span data-stu-id="b56d8-482">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b56d8-483">ADO プロパティ名</span><span class="sxs-lookup"><span data-stu-id="b56d8-483">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="b56d8-484">OLE DB プロパティ名</span><span class="sxs-lookup"><span data-stu-id="b56d8-484">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-485">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="b56d8-485">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="b56d8-486">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="b56d8-486">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-487">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="b56d8-487">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="b56d8-488">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="b56d8-488">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-489">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="b56d8-489">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="b56d8-490">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="b56d8-490">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-491">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="b56d8-491">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="b56d8-492">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="b56d8-492">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-493">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="b56d8-493">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="b56d8-494">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="b56d8-494">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-495">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="b56d8-495">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="b56d8-496">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="b56d8-496">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-497">Column Definition</span><span class="sxs-lookup"><span data-stu-id="b56d8-497">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="b56d8-498">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="b56d8-498">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-499">Connect Timeout</span><span class="sxs-lookup"><span data-stu-id="b56d8-499">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="b56d8-500">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="b56d8-500">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-501">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="b56d8-501">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="b56d8-502">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="b56d8-502">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-503">Data Source</span><span class="sxs-lookup"><span data-stu-id="b56d8-503">Data Source</span></span></p></td>
<td><p><span data-ttu-id="b56d8-504">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="b56d8-504">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-505">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="b56d8-505">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="b56d8-506">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="b56d8-506">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-507">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="b56d8-507">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="b56d8-508">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="b56d8-508">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-509">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="b56d8-509">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="b56d8-510">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="b56d8-510">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-511">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="b56d8-511">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="b56d8-512">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="b56d8-512">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-513">Extended Properties</span><span class="sxs-lookup"><span data-stu-id="b56d8-513">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="b56d8-514">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="b56d8-514">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-515">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="b56d8-515">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="b56d8-516">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="b56d8-516">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-517">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="b56d8-517">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="b56d8-518">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="b56d8-518">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-519">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="b56d8-519">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="b56d8-520">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="b56d8-520">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-521">Initial Catalog</span><span class="sxs-lookup"><span data-stu-id="b56d8-521">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="b56d8-522">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="b56d8-522">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-523">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="b56d8-523">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="b56d8-524">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="b56d8-524">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-525">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="b56d8-525">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="b56d8-526">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="b56d8-526">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-527">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="b56d8-527">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="b56d8-528">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="b56d8-528">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-529">Location</span><span class="sxs-lookup"><span data-stu-id="b56d8-529">Location</span></span></p></td>
<td><p><span data-ttu-id="b56d8-530">DBPROP_INIT_LOCATION</span><span class="sxs-lookup"><span data-stu-id="b56d8-530">DBPROP_INIT_LOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-531">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="b56d8-531">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="b56d8-532">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="b56d8-532">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-533">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="b56d8-533">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="b56d8-534">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="b56d8-534">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-535">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="b56d8-535">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="b56d8-536">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="b56d8-536">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-537">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="b56d8-537">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="b56d8-538">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="b56d8-538">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-539">Mode</span><span class="sxs-lookup"><span data-stu-id="b56d8-539">Mode</span></span></p></td>
<td><p><span data-ttu-id="b56d8-540">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="b56d8-540">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-541">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="b56d8-541">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="b56d8-542">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="b56d8-542">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-543">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="b56d8-543">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="b56d8-544">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="b56d8-544">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-545">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="b56d8-545">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="b56d8-546">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="b56d8-546">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-547">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="b56d8-547">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="b56d8-548">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="b56d8-548">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-549">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="b56d8-549">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="b56d8-550">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="b56d8-550">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-551">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="b56d8-551">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="b56d8-552">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="b56d8-552">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-553">OLE DB Services</span><span class="sxs-lookup"><span data-stu-id="b56d8-553">OLE DB Services</span></span></p></td>
<td><p><span data-ttu-id="b56d8-554">DBPROP_INIT_OLEDBSERVICES</span><span class="sxs-lookup"><span data-stu-id="b56d8-554">DBPROP_INIT_OLEDBSERVICES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-555">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="b56d8-555">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="b56d8-556">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="b56d8-556">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-557">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="b56d8-557">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="b56d8-558">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="b56d8-558">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-559">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="b56d8-559">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="b56d8-560">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="b56d8-560">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-561">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="b56d8-561">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="b56d8-562">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="b56d8-562">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-563">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="b56d8-563">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="b56d8-564">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="b56d8-564">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-565">Password</span><span class="sxs-lookup"><span data-stu-id="b56d8-565">Password</span></span></p></td>
<td><p><span data-ttu-id="b56d8-566">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="b56d8-566">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-567">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="b56d8-567">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="b56d8-568">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="b56d8-568">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-569">Persist Security Info</span><span class="sxs-lookup"><span data-stu-id="b56d8-569">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="b56d8-570">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="b56d8-570">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-571">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="b56d8-571">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="b56d8-572">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="b56d8-572">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-573">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="b56d8-573">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="b56d8-574">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="b56d8-574">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-575">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="b56d8-575">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="b56d8-576">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="b56d8-576">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-577">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="b56d8-577">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="b56d8-578">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="b56d8-578">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-579">Prompt</span><span class="sxs-lookup"><span data-stu-id="b56d8-579">Prompt</span></span></p></td>
<td><p><span data-ttu-id="b56d8-580">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="b56d8-580">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-581">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="b56d8-581">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="b56d8-582">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="b56d8-582">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-583">Provider Name</span><span class="sxs-lookup"><span data-stu-id="b56d8-583">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="b56d8-584">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="b56d8-584">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-585">Provider Version</span><span class="sxs-lookup"><span data-stu-id="b56d8-585">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="b56d8-586">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="b56d8-586">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-587">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="b56d8-587">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="b56d8-588">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="b56d8-588">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-589">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="b56d8-589">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="b56d8-590">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="b56d8-590">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-591">Schema Term</span><span class="sxs-lookup"><span data-stu-id="b56d8-591">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="b56d8-592">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="b56d8-592">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-593">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="b56d8-593">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="b56d8-594">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="b56d8-594">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-595">SQL Support</span><span class="sxs-lookup"><span data-stu-id="b56d8-595">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="b56d8-596">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="b56d8-596">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-597">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="b56d8-597">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="b56d8-598">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="b56d8-598">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-599">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="b56d8-599">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="b56d8-600">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="b56d8-600">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-601">Table Term</span><span class="sxs-lookup"><span data-stu-id="b56d8-601">Table Term</span></span></p></td>
<td><p><span data-ttu-id="b56d8-602">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="b56d8-602">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-603">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="b56d8-603">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="b56d8-604">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="b56d8-604">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-605">User ID</span><span class="sxs-lookup"><span data-stu-id="b56d8-605">User ID</span></span></p></td>
<td><p><span data-ttu-id="b56d8-606">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="b56d8-606">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-607">User Name</span><span class="sxs-lookup"><span data-stu-id="b56d8-607">User Name</span></span></p></td>
<td><p><span data-ttu-id="b56d8-608">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="b56d8-608">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-609">Window Handle</span><span class="sxs-lookup"><span data-stu-id="b56d8-609">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="b56d8-610">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="b56d8-610">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="b56d8-611">Recordset の動的プロパティ</span><span class="sxs-lookup"><span data-stu-id="b56d8-611">Recordset Dynamic Properties</span></span>

<span data-ttu-id="b56d8-612">次に示すプロパティが **Recordset** オブジェクトの **Properties** コレクションに追加されます。</span><span class="sxs-lookup"><span data-stu-id="b56d8-612">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b56d8-613">ADO プロパティ名</span><span class="sxs-lookup"><span data-stu-id="b56d8-613">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="b56d8-614">OLE DB プロパティ名</span><span class="sxs-lookup"><span data-stu-id="b56d8-614">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-615">Access Order</span><span class="sxs-lookup"><span data-stu-id="b56d8-615">Access Order</span></span></p></td>
<td><p><span data-ttu-id="b56d8-616">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="b56d8-616">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-617">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="b56d8-617">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="b56d8-618">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="b56d8-618">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-619">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="b56d8-619">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="b56d8-620">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="b56d8-620">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-621">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="b56d8-621">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="b56d8-622">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="b56d8-622">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-623">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="b56d8-623">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="b56d8-624">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="b56d8-624">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-625">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="b56d8-625">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="b56d8-626">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="b56d8-626">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-627">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="b56d8-627">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="b56d8-628">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="b56d8-628">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-629">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="b56d8-629">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="b56d8-630">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="b56d8-630">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-631">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="b56d8-631">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="b56d8-632">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="b56d8-632">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-633">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="b56d8-633">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="b56d8-634">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="b56d8-634">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-635">IAccessor</span><span class="sxs-lookup"><span data-stu-id="b56d8-635">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="b56d8-636">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="b56d8-636">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-637">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="b56d8-637">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="b56d8-638">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="b56d8-638">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-639">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="b56d8-639">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="b56d8-640">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="b56d8-640">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-641">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="b56d8-641">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="b56d8-642">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="b56d8-642">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-643">IConvertType</span><span class="sxs-lookup"><span data-stu-id="b56d8-643">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="b56d8-644">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="b56d8-644">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-645">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="b56d8-645">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="b56d8-646">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="b56d8-646">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-647">IRowset</span><span class="sxs-lookup"><span data-stu-id="b56d8-647">IRowset</span></span></p></td>
<td><p><span data-ttu-id="b56d8-648">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="b56d8-648">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-649">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="b56d8-649">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="b56d8-650">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="b56d8-650">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-651">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="b56d8-651">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="b56d8-652">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="b56d8-652">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-653">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="b56d8-653">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="b56d8-654">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="b56d8-654">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-655">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="b56d8-655">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="b56d8-656">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="b56d8-656">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-657">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="b56d8-657">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-658">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="b56d8-658">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="b56d8-659">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="b56d8-659">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-660">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="b56d8-660">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="b56d8-661">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="b56d8-661">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-662">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="b56d8-662">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="b56d8-663">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="b56d8-663">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-664">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="b56d8-664">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="b56d8-665">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="b56d8-665">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-666">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="b56d8-666">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="b56d8-667">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="b56d8-667">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-668">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="b56d8-668">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="b56d8-669">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="b56d8-669">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-670">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="b56d8-670">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="b56d8-671">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="b56d8-671">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-672">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="b56d8-672">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="b56d8-673">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="b56d8-673">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-674">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="b56d8-674">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="b56d8-675">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="b56d8-675">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-676">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="b56d8-676">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="b56d8-677">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="b56d8-677">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-678">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="b56d8-678">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="b56d8-679">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="b56d8-679">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-680">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="b56d8-680">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="b56d8-681">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="b56d8-681">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-682">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="b56d8-682">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="b56d8-683">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="b56d8-683">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-684">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="b56d8-684">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="b56d8-685">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="b56d8-685">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-686">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="b56d8-686">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="b56d8-687">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="b56d8-687">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-688">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="b56d8-688">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="b56d8-689">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="b56d8-689">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-690">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="b56d8-690">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="b56d8-691">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="b56d8-691">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-692">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="b56d8-692">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="b56d8-693">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="b56d8-693">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-694">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="b56d8-694">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-695">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="b56d8-695">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-696">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="b56d8-696">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="b56d8-697">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="b56d8-697">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-698">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="b56d8-698">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="b56d8-699">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="b56d8-699">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-700">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="b56d8-700">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="b56d8-701">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="b56d8-701">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-702">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="b56d8-702">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="b56d8-703">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="b56d8-703">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-704">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="b56d8-704">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="b56d8-705">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="b56d8-705">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-706">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="b56d8-706">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="b56d8-707">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="b56d8-707">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-708">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="b56d8-708">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="b56d8-709">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="b56d8-709">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-710">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="b56d8-710">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="b56d8-711">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="b56d8-711">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-712">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="b56d8-712">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="b56d8-713">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="b56d8-713">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-714">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="b56d8-714">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="b56d8-715">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="b56d8-715">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-716">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="b56d8-716">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="b56d8-717">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="b56d8-717">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-718">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="b56d8-718">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="b56d8-719">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="b56d8-719">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-720">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="b56d8-720">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="b56d8-721">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="b56d8-721">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-722">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="b56d8-722">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="b56d8-723">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="b56d8-723">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-724">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="b56d8-724">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="b56d8-725">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="b56d8-725">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-726">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="b56d8-726">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="b56d8-727">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="b56d8-727">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-728">Unique Rows</span><span class="sxs-lookup"><span data-stu-id="b56d8-728">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="b56d8-729">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="b56d8-729">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-730">Updatability</span><span class="sxs-lookup"><span data-stu-id="b56d8-730">Updatability</span></span></p></td>
<td><p><span data-ttu-id="b56d8-731">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="b56d8-731">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-732">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="b56d8-732">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="b56d8-733">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="b56d8-733">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="b56d8-734">Command の動的プロパティ</span><span class="sxs-lookup"><span data-stu-id="b56d8-734">Command Dynamic Properties</span></span>

<span data-ttu-id="b56d8-735">次に示すプロパティが **Command** オブジェクトの **Properties** コレクションに追加されます。</span><span class="sxs-lookup"><span data-stu-id="b56d8-735">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b56d8-736">ADO プロパティ名</span><span class="sxs-lookup"><span data-stu-id="b56d8-736">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="b56d8-737">OLE DB プロパティ名</span><span class="sxs-lookup"><span data-stu-id="b56d8-737">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-738">Access Order</span><span class="sxs-lookup"><span data-stu-id="b56d8-738">Access Order</span></span></p></td>
<td><p><span data-ttu-id="b56d8-739">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="b56d8-739">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-740">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="b56d8-740">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="b56d8-741">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="b56d8-741">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-742">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="b56d8-742">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="b56d8-743">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="b56d8-743">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-744">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="b56d8-744">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="b56d8-745">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="b56d8-745">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-746">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="b56d8-746">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="b56d8-747">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="b56d8-747">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-748">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="b56d8-748">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="b56d8-749">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="b56d8-749">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-750">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="b56d8-750">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="b56d8-751">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="b56d8-751">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-752">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="b56d8-752">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="b56d8-753">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="b56d8-753">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-754">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="b56d8-754">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="b56d8-755">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="b56d8-755">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-756">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="b56d8-756">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="b56d8-757">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="b56d8-757">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-758">IAccessor</span><span class="sxs-lookup"><span data-stu-id="b56d8-758">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="b56d8-759">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="b56d8-759">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-760">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="b56d8-760">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="b56d8-761">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="b56d8-761">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-762">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="b56d8-762">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="b56d8-763">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="b56d8-763">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-764">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="b56d8-764">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="b56d8-765">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="b56d8-765">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-766">IConvertType</span><span class="sxs-lookup"><span data-stu-id="b56d8-766">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="b56d8-767">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="b56d8-767">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-768">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="b56d8-768">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="b56d8-769">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="b56d8-769">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-770">IRowset</span><span class="sxs-lookup"><span data-stu-id="b56d8-770">IRowset</span></span></p></td>
<td><p><span data-ttu-id="b56d8-771">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="b56d8-771">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-772">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="b56d8-772">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="b56d8-773">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="b56d8-773">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-774">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="b56d8-774">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="b56d8-775">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="b56d8-775">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-776">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="b56d8-776">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="b56d8-777">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="b56d8-777">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-778">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="b56d8-778">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="b56d8-779">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="b56d8-779">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-780">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="b56d8-780">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-781">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="b56d8-781">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="b56d8-782">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="b56d8-782">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-783">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="b56d8-783">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="b56d8-784">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="b56d8-784">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-785">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="b56d8-785">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="b56d8-786">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="b56d8-786">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-787">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="b56d8-787">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="b56d8-788">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="b56d8-788">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-789">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="b56d8-789">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="b56d8-790">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="b56d8-790">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-791">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="b56d8-791">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="b56d8-792">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="b56d8-792">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-793">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="b56d8-793">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="b56d8-794">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="b56d8-794">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-795">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="b56d8-795">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="b56d8-796">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="b56d8-796">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-797">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="b56d8-797">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="b56d8-798">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="b56d8-798">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-799">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="b56d8-799">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="b56d8-800">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="b56d8-800">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-801">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="b56d8-801">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="b56d8-802">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="b56d8-802">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-803">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="b56d8-803">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="b56d8-804">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="b56d8-804">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-805">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="b56d8-805">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="b56d8-806">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="b56d8-806">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-807">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="b56d8-807">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="b56d8-808">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="b56d8-808">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-809">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="b56d8-809">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="b56d8-810">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="b56d8-810">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-811">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="b56d8-811">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="b56d8-812">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="b56d8-812">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-813">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="b56d8-813">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="b56d8-814">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="b56d8-814">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-815">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="b56d8-815">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="b56d8-816">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="b56d8-816">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-817">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="b56d8-817">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="b56d8-818">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="b56d8-818">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-819">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="b56d8-819">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="b56d8-820">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="b56d8-820">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-821">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="b56d8-821">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="b56d8-822">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="b56d8-822">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-823">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="b56d8-823">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="b56d8-824">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="b56d8-824">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-825">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="b56d8-825">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="b56d8-826">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="b56d8-826">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-827">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="b56d8-827">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="b56d8-828">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="b56d8-828">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-829">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="b56d8-829">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="b56d8-830">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="b56d8-830">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-831">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="b56d8-831">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="b56d8-832">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="b56d8-832">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-833">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="b56d8-833">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="b56d8-834">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="b56d8-834">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-835">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="b56d8-835">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="b56d8-836">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="b56d8-836">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-837">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="b56d8-837">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="b56d8-838">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="b56d8-838">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-839">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="b56d8-839">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="b56d8-840">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="b56d8-840">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-841">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="b56d8-841">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="b56d8-842">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="b56d8-842">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-843">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="b56d8-843">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="b56d8-844">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="b56d8-844">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-845">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="b56d8-845">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="b56d8-846">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="b56d8-846">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-847">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="b56d8-847">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="b56d8-848">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="b56d8-848">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-849">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="b56d8-849">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="b56d8-850">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="b56d8-850">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56d8-851">Updatability</span><span class="sxs-lookup"><span data-stu-id="b56d8-851">Updatability</span></span></p></td>
<td><p><span data-ttu-id="b56d8-852">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="b56d8-852">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56d8-853">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="b56d8-853">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="b56d8-854">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="b56d8-854">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="b56d8-855">関連項目</span><span class="sxs-lookup"><span data-stu-id="b56d8-855">See also</span></span>

<span data-ttu-id="b56d8-856">特定の実装および ODBC 用 Microsoft OLE DB プロバイダーの機能の情報に関する詳細については、 [OLE DB プログラマ ガイド」](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85))を参照してくださいまたは[データ プラットフォーム デベロッパー センター](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b56d8-856">For details regarding specific implementation and functional information about the Microsoft OLE DB Provider for ODBC, consult the [OLE DB Programmer's Guide](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) or visit the [Data Platform Developer Center](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span></span>

