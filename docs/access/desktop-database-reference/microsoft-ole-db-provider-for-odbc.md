---
title: Microsoft OLE DB Provider for ODBC
TOCTitle: Microsoft OLE DB Provider for ODBC
ms:assetid: c507567e-5ad1-b32a-f6ad-5ba2c39aa4c2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249964(v=office.15)
ms:contentKeyID: 48547602
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0098e646ea48656f44bd3ccd380ae41efc94ffba
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606941"
---
# <a name="microsoft-ole-db-provider-for-odbc"></a><span data-ttu-id="0137b-102">Microsoft OLE DB Provider for ODBC</span><span class="sxs-lookup"><span data-stu-id="0137b-102">Microsoft OLE DB Provider for ODBC</span></span>

<span data-ttu-id="0137b-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="0137b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0137b-p101">ADO または RDS のプログラマにとって、すべてのデータ ソースで OLE DB インターフェイスが公開され、ADO で直接データ ソースを呼び出すことができるのが理想的です。OLE DB インターフェイスを実装するデータベース ベンダーは増えていますが、まだこのインターフェイスを公開していないデータ ソースもあります。ただし、現在使用されている事実上すべての DBMS システムは、ODBC によるアクセスが可能です。</span><span class="sxs-lookup"><span data-stu-id="0137b-p101">To an ADO or RDS programmer, an ideal world would be one in which every data source exposes an OLE DB interface, so that ADO could call directly into the data source. Although increasingly more database vendors are implementing OLE DB interfaces, some data sources are not yet exposed this way. However, virtually all DBMS systems in use today can be accessed through ODBC.</span></span>

<span data-ttu-id="0137b-107">ODBC ドライバーは、Microsoft SQL Server、Microsoft Access (Microsoft Jet データベース エンジン)、および Microsoft FoxPro だけでなく、Oracle などの Microsoft 以外のデータベース製品を含めた、現在使用されているすべての主要 DBMS で使用できます。</span><span class="sxs-lookup"><span data-stu-id="0137b-107">ODBC drivers are available for every major DBMS in use today, including Microsoft SQL Server, Microsoft Access (Microsoft Jet database engine), and Microsoft FoxPro, in addition to non-Microsoft database products such as Oracle.</span></span>

<span data-ttu-id="0137b-p102">ただし、Microsoft ODBC Provider を使用すると、ADO からすべての ODBC データ ソースに接続できます。このプロバイダーはフリースレッドであり、Unicode に対応しています。</span><span class="sxs-lookup"><span data-stu-id="0137b-p102">The Microsoft ODBC Provider, however, allows ADO to connect to any ODBC data source. The provider is free-threaded and Unicode enabled.</span></span>

<span data-ttu-id="0137b-p103">このプロバイダーはトランザクションをサポートしていますが、DBMS エンジンの種類によって、サポートするトランザクションの種類が異なります。たとえば、Microsoft Access は 5 レベルまでのネストされたトランザクションをサポートします。</span><span class="sxs-lookup"><span data-stu-id="0137b-p103">The provider supports transactions, although different DBMS engines offer different types of transaction support. For example, Microsoft Access supports nested transactions up to five levels deep.</span></span>

<span data-ttu-id="0137b-112">このプロバイダーは ADO の既定のプロバイダーであり、プロバイダーに依存するすべての ADO プロパティおよびメソッドをサポートします。</span><span class="sxs-lookup"><span data-stu-id="0137b-112">This is the default provider for ADO, and all provider-dependent ADO properties and methods are supported.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="0137b-113">接続文字列パラメーター</span><span class="sxs-lookup"><span data-stu-id="0137b-113">Connection String Parameters</span></span>

<span data-ttu-id="0137b-114">このプロバイダーに接続するには、**ConnectionString** プロパティの [Provider=](connectionstring-property-ado.md) 引数を次のように設定します。</span><span class="sxs-lookup"><span data-stu-id="0137b-114">To connect to this provider, set the **Provider=** argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```sql 
 
MSDASQL 
```

<span data-ttu-id="0137b-115">[Provider](provider-property-ado.md) プロパティを取得した場合も、この文字列が返されます。</span><span class="sxs-lookup"><span data-stu-id="0137b-115">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="0137b-116">標準的な接続文字列</span><span class="sxs-lookup"><span data-stu-id="0137b-116">Typical Connection String</span></span>

<span data-ttu-id="0137b-117">このプロバイダーの標準的な接続文字列を次に示します。</span><span class="sxs-lookup"><span data-stu-id="0137b-117">A typical connection string for this provider is:</span></span>

```sql 
 
"Provider=MSDASQL;DSN=dsnName;UID=userName;PWD=userPassword;" 
```

<span data-ttu-id="0137b-118">この文字列は、次に示すキーワードで構成されています。</span><span class="sxs-lookup"><span data-stu-id="0137b-118">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0137b-119">キーワード</span><span class="sxs-lookup"><span data-stu-id="0137b-119">Keyword</span></span></p></th>
<th><p><span data-ttu-id="0137b-120">説明</span><span class="sxs-lookup"><span data-stu-id="0137b-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0137b-121"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="0137b-121"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="0137b-122">OLE DB Provider for ODBC を指定します。</span><span class="sxs-lookup"><span data-stu-id="0137b-122">Specifies the OLE DB Provider for ODBC.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-123"><strong>DSN</strong></span><span class="sxs-lookup"><span data-stu-id="0137b-123"><strong>DSN</strong></span></span></p></td>
<td><p><span data-ttu-id="0137b-124">データ ソース名を指定します。</span><span class="sxs-lookup"><span data-stu-id="0137b-124">Specifies the data source name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-125"><strong>UID</strong></span><span class="sxs-lookup"><span data-stu-id="0137b-125"><strong>UID</strong></span></span></p></td>
<td><p><span data-ttu-id="0137b-126">ユーザー名を指定します。</span><span class="sxs-lookup"><span data-stu-id="0137b-126">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-127"><strong>PWD</strong></span><span class="sxs-lookup"><span data-stu-id="0137b-127"><strong>PWD</strong></span></span></p></td>
<td><p><span data-ttu-id="0137b-128">ユーザー パスワードを指定します。</span><span class="sxs-lookup"><span data-stu-id="0137b-128">Specifies the user password.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-129"><strong>URL</strong></span><span class="sxs-lookup"><span data-stu-id="0137b-129"><strong>URL</strong></span></span></p></td>
<span data-ttu-id="0137b-130"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="0137b-130"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="0137b-131">Web フォルダーに公開されているファイルまたはディレクトリの URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="0137b-131">Specifies the URL of a file or directory published in a Web folder.</span></span></p></td>
=======
<td><p><span data-ttu-id="0137b-132">ファイルまたは web フォルダーで公開されているディレクトリの URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="0137b-132">Specifies the URL of a file or directory published in a web folder.</span></span></p></td><span data-ttu-id="0137b-133">
>>>>>>>マスター</span><span class="sxs-lookup"><span data-stu-id="0137b-133">
>>>>>>> master</span></span>
</tr>
</tbody>
</table>


<span data-ttu-id="0137b-134">このプロバイダーは ADO の既定のプロバイダーであるため、接続文字列で **Provider=** パラメーターを省略すると、このプロバイダーへの接続の確立が試行されます。</span><span class="sxs-lookup"><span data-stu-id="0137b-134">Because this is the default provider for ADO, if you omit the **Provider=** parameter from the connection string, ADO will attempt to establish a connection to this provider.</span></span>

<span data-ttu-id="0137b-p104">このプロバイダーは、ADO で定義されたパラメーター以外に独自の接続パラメーターをサポートしません。ただし、ADO 以外の接続パラメーターが指定されている場合は、ODBC ドライバー マネージャーに渡します。</span><span class="sxs-lookup"><span data-stu-id="0137b-p104">The provider does not support any specific connection parameters in addition to those defined by ADO. However, the provider will pass any non-ADO connection parameters to the ODBC driver manager.</span></span>

<span data-ttu-id="0137b-p105">**Provider** パラメーターを省略できるので、同じデータ ソースに対して ODBC 接続文字列と同じ ADO 接続文字列を作成できます。ODBC 接続文字列を作成するときと同じパラメーター名 (**DRIVER=**、**DATABASE=**、**DSN=** など)、値、および構文を使用します。定義済みのデータ ソース名 (DSN) または FileDSN を指定してもしなくても接続できます。</span><span class="sxs-lookup"><span data-stu-id="0137b-p105">Because you can omit the **Provider** parameter, you can therefore compose an ADO connection string that is identical to an ODBC connection string for the same data source. Use the same parameter names (**DRIVER=**, **DATABASE=**, **DSN=**, and so on), values, and syntax as you would when composing an ODBC connection string. You can connect with or without a predefined data source name (DSN) or FileDSN.</span></span>

<span data-ttu-id="0137b-140">**DSN または FileDSN を指定する場合の構文:**</span><span class="sxs-lookup"><span data-stu-id="0137b-140">**Syntax with a DSN or FileDSN:**</span></span>

`"[Provider=MSDASQL;] { DSN=name | FileDSN=filename } ; [DATABASE=database;] UID=user; PWD=password"`

<span data-ttu-id="0137b-141">**DSN 指定しない場合の構文 (DSN なしの接続):**</span><span class="sxs-lookup"><span data-stu-id="0137b-141">**Syntax without a DSN (DSN-less connection):**</span></span>

`"[Provider=MSDASQL;] DRIVER=driver; SERVER=server;DATABASE=database; UID=user; PWD=password"`

<span data-ttu-id="0137b-142">**DSN**または**FileDSN**を使用する場合は Windows のコントロール パネルの [ODBC データ ソース アドミニストレーターを使用する必要があります定義します。</span><span class="sxs-lookup"><span data-stu-id="0137b-142">If you use a **DSN** or **FileDSN**, it must be defined through the ODBC Data Source Administrator in the Windows Control Panel.</span></span> <span data-ttu-id="0137b-143">Microsoft Windows 2000 では、odbc データ ソース アドミニストレーターは管理ツールの下にあります。</span><span class="sxs-lookup"><span data-stu-id="0137b-143">In Microsoft Windows 2000, the ODBC Administrator is located under Administrative Tools.</span></span> <span data-ttu-id="0137b-144">以前のバージョンの Windows では、odbc データ ソース アドミニストレーター アイコンは**32 ビット ODBC**または**ODBC**では単に呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="0137b-144">In previous versions of Windows, the ODBC Administrator icon is named **32-bit ODBC** or simply **ODBC**.</span></span>

<span data-ttu-id="0137b-145">**DSN** を設定する代わりに、"SQL Server" などの ODBC ドライバー (**DRIVER=**)、サーバー名 (**SERVER=**)、およびデータベース名 (**DATABASE=**) を指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="0137b-145">As an alternative to setting a **DSN**, you can specify the ODBC driver (**DRIVER=**), such as "SQL Server;" the server name (**SERVER=**); and the database name (**DATABASE=**).</span></span>

<span data-ttu-id="0137b-146">ユーザー アカウント名 (**UID=**) と、そのユーザー アカウントのパスワード (**PWD=**) を、ODBC 固有のパラメーターまたは ADO で定義された標準的な *user* パラメーターと *password* パラメーターで指定できます。</span><span class="sxs-lookup"><span data-stu-id="0137b-146">You can also specify a user account name (**UID=**), and the password for the user account (**PWD=**) in the ODBC-specific parameters or in the standard ADO-defined *user* and *password* parameters.</span></span>

<span data-ttu-id="0137b-147">**DSN**の定義が既にデータベースを指定して、*別のデータベースに接続する**DSN**に加えて*データベース*パラメーター*を指定できます。</span><span class="sxs-lookup"><span data-stu-id="0137b-147">Although a **DSN** definition already specifies a database, you can specify *a* *database* parameter in addition to a **DSN** to connect to a different database.</span></span> <span data-ttu-id="0137b-148">**DSN**を使用するときに常に\**データベース*パラメーター\*を含めることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="0137b-148">It is a good idea to always include *the* *database* parameter when you use a **DSN**.</span></span> <span data-ttu-id="0137b-149">これは、ように**DSN**の定義を確認した後、他のユーザーがデータベースの既定のパラメーターを変更する適切なデータベースに接続すること。</span><span class="sxs-lookup"><span data-stu-id="0137b-149">This will ensure that you connect to the proper database in the event that another user changed the default database parameter since you last checked the **DSN** definition.</span></span>

## <a name="provider-specific-connection-properties"></a><span data-ttu-id="0137b-150">プロバイダー固有の Connection のプロパティ</span><span class="sxs-lookup"><span data-stu-id="0137b-150">Provider-Specific Connection Properties</span></span>

<span data-ttu-id="0137b-p108">OLE DB Provider for ODBC は、 [Connection](properties-collection-ado.md) オブジェクトの **Properties** コレクションにプロパティを追加します。次の表は、これらのプロパティの一覧で、かっこ内は対応する OLE DB プロパティ名です。</span><span class="sxs-lookup"><span data-stu-id="0137b-p108">The OLE DB provider for ODBC adds several properties to the [Properties](properties-collection-ado.md) collection of the **Connection** object. The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0137b-153">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="0137b-153">Property Name</span></span></p></th>
<th><p><span data-ttu-id="0137b-154">説明</span><span class="sxs-lookup"><span data-stu-id="0137b-154">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0137b-155">アクセス手順</span><span class="sxs-lookup"><span data-stu-id="0137b-155">Accessible Procedures</span></span><br />
<span data-ttu-id="0137b-156">(KAGPROP_ACCESSIBLEPROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="0137b-156">(KAGPROP_ACCESSIBLEPROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="0137b-157">ユーザーがストアド プロシージャにアクセスできるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="0137b-157">Indicates whether the user has access to stored procedures.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-158">アクセス可能なテーブル</span><span class="sxs-lookup"><span data-stu-id="0137b-158">Accessible Tables</span></span><br />
<span data-ttu-id="0137b-159">(KAGPROP_ACCESSIBLETABLES)</span><span class="sxs-lookup"><span data-stu-id="0137b-159">(KAGPROP_ACCESSIBLETABLES)</span></span></p></td>
<td><p><span data-ttu-id="0137b-160">ユーザーがデータベースのテーブルに対して SELECT ステートメントを実行する権限を持つかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="0137b-160">Indicates whether the user has permission to execute SELECT statements against the database tables.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-161">アクティブなステートメント</span><span class="sxs-lookup"><span data-stu-id="0137b-161">Active Statements</span></span><br />
<span data-ttu-id="0137b-162">(KAGPROP_ACTIVESTATEMENTS)</span><span class="sxs-lookup"><span data-stu-id="0137b-162">(KAGPROP_ACTIVESTATEMENTS)</span></span></p></td>
<td><p><span data-ttu-id="0137b-163">ODBC ドライバーが 1 つの接続でサポートできるハンドル数を示します。</span><span class="sxs-lookup"><span data-stu-id="0137b-163">Indicates the number of handles an ODBC driver can support on a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-164">ドライバー名</span><span class="sxs-lookup"><span data-stu-id="0137b-164">Driver Name</span></span><br />
<span data-ttu-id="0137b-165">(KAGPROP_DRIVERNAME)</span><span class="sxs-lookup"><span data-stu-id="0137b-165">(KAGPROP_DRIVERNAME)</span></span></p></td>
<td><p><span data-ttu-id="0137b-166">ODBC ドライバーのファイル名を示します。</span><span class="sxs-lookup"><span data-stu-id="0137b-166">Indicates the file name of the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-167">ドライバーの ODBC バージョン</span><span class="sxs-lookup"><span data-stu-id="0137b-167">Driver ODBC Version</span></span><br />
<span data-ttu-id="0137b-168">(KAGPROP_DRIVERODBCVER)</span><span class="sxs-lookup"><span data-stu-id="0137b-168">(KAGPROP_DRIVERODBCVER)</span></span></p></td>
<td><p><span data-ttu-id="0137b-169">このドライバーがサポートする ODBC のバージョンを示します。</span><span class="sxs-lookup"><span data-stu-id="0137b-169">Indicates the version of ODBC that this driver supports.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-170">ファイルの使用状況</span><span class="sxs-lookup"><span data-stu-id="0137b-170">File Usage</span></span><br />
<span data-ttu-id="0137b-171">(KAGPROP_FILEUSAGE)</span><span class="sxs-lookup"><span data-stu-id="0137b-171">(KAGPROP_FILEUSAGE)</span></span></p></td>
<td><p><span data-ttu-id="0137b-172">ドライバーがデータ ソース内のファイルを、テーブルとして扱うか、カタログとして扱うかを示します。</span><span class="sxs-lookup"><span data-stu-id="0137b-172">Indicates how the driver treats a file in a data source; as a table or as a catalog.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-173">エスケープ句のように</span><span class="sxs-lookup"><span data-stu-id="0137b-173">Like Escape Clause</span></span><br />
<span data-ttu-id="0137b-174">(KAGPROP_LIKEESCAPECLAUSE)</span><span class="sxs-lookup"><span data-stu-id="0137b-174">(KAGPROP_LIKEESCAPECLAUSE)</span></span></p></td>
<td><p><span data-ttu-id="0137b-175">ドライバーが、WHERE 句の LIKE 述語でパーセント記号 (%) および下線記号 (_) のエスケープ文字を定義および使用できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="0137b-175">Indicates whether the driver supports the definition and use of an escape character for the percent character (%) and underline character (_) in the LIKE predicate of a WHERE clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-176">によるグループ内の最大列</span><span class="sxs-lookup"><span data-stu-id="0137b-176">Max Columns in Group By</span></span><br />
<span data-ttu-id="0137b-177">(KAGPROP_MAXCOLUMNSINGROUPBY)</span><span class="sxs-lookup"><span data-stu-id="0137b-177">(KAGPROP_MAXCOLUMNSINGROUPBY)</span></span></p></td>
<td><p><span data-ttu-id="0137b-178">SELECT ステートメントの GROUP BY 句に記述できる最大列数を示します。</span><span class="sxs-lookup"><span data-stu-id="0137b-178">Indicates the maximum number of columns that can be listed in the GROUP BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-179">インデックスの最大列</span><span class="sxs-lookup"><span data-stu-id="0137b-179">Max Columns in Index</span></span><br />
<span data-ttu-id="0137b-180">(KAGPROP_MAXCOLUMNSININDEX)</span><span class="sxs-lookup"><span data-stu-id="0137b-180">(KAGPROP_MAXCOLUMNSININDEX)</span></span></p></td>
<td><p><span data-ttu-id="0137b-181">インデックスに格納できる最大列数を示します。</span><span class="sxs-lookup"><span data-stu-id="0137b-181">Indicates the maximum number of columns that can be included in an index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-182">Order By の中の最大列</span><span class="sxs-lookup"><span data-stu-id="0137b-182">Max Columns in Order By</span></span><br />
<span data-ttu-id="0137b-183">(KAGPROP_MAXCOLUMNSINORDERBY)</span><span class="sxs-lookup"><span data-stu-id="0137b-183">(KAGPROP_MAXCOLUMNSINORDERBY)</span></span></p></td>
<td><p><span data-ttu-id="0137b-184">SELECT ステートメントの ORDER BY 句に記述できる最大列数を示します。</span><span class="sxs-lookup"><span data-stu-id="0137b-184">Indicates the maximum number of columns that can be listed in the ORDER BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-185">選択中の最大列</span><span class="sxs-lookup"><span data-stu-id="0137b-185">Max Columns in Select</span></span><br />
<span data-ttu-id="0137b-186">(KAGPROP_MAXCOLUMNSINSELECT)</span><span class="sxs-lookup"><span data-stu-id="0137b-186">(KAGPROP_MAXCOLUMNSINSELECT)</span></span></p></td>
<td><p><span data-ttu-id="0137b-187">SELECT ステートメントの SELECT 部分に記述できる最大列数を示します。</span><span class="sxs-lookup"><span data-stu-id="0137b-187">Indicates the maximum number of columns that can be listed in the SELECT portion of a SELECT statement.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-188">テーブルの最大列</span><span class="sxs-lookup"><span data-stu-id="0137b-188">Max Columns in Table</span></span><br />
<span data-ttu-id="0137b-189">(KAGPROP_MAXCOLUMNSINTABLE)</span><span class="sxs-lookup"><span data-stu-id="0137b-189">(KAGPROP_MAXCOLUMNSINTABLE)</span></span></p></td>
<td><p><span data-ttu-id="0137b-190">テーブルの最大列数を示します。</span><span class="sxs-lookup"><span data-stu-id="0137b-190">Indicates the maximum number of columns allowed in a table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-191">数値を処理する関数</span><span class="sxs-lookup"><span data-stu-id="0137b-191">Numeric Functions</span></span><br />
<span data-ttu-id="0137b-192">(KAGPROP_NUMERICFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="0137b-192">(KAGPROP_NUMERICFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="0137b-p109">ODBC ドライバーがサポートする数値関数を示します。関数名とこのビットマスクで使用される関連付けられた値の一覧については、ODBC マニュアルの「Appendix E: Scalar Functions」 (英語) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0137b-p109">Indicates which numeric functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-195">外部結合の機能</span><span class="sxs-lookup"><span data-stu-id="0137b-195">Outer Join Capabilities</span></span><br />
<span data-ttu-id="0137b-196">(KAGPROP_OJCAPABILITY)</span><span class="sxs-lookup"><span data-stu-id="0137b-196">(KAGPROP_OJCAPABILITY)</span></span></p></td>
<td><p><span data-ttu-id="0137b-197">プロバイダーがサポートする OUTER JOIN の種類を示します。</span><span class="sxs-lookup"><span data-stu-id="0137b-197">Indicates the types of OUTER JOINs supported by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-198">外部結合</span><span class="sxs-lookup"><span data-stu-id="0137b-198">Outer Joins</span></span><br />
<span data-ttu-id="0137b-199">(KAGPROP_OUTERJOINS)</span><span class="sxs-lookup"><span data-stu-id="0137b-199">(KAGPROP_OUTERJOINS)</span></span></p></td>
<td><p><span data-ttu-id="0137b-200">プロバイダーが OUTER JOIN をサポートするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="0137b-200">Indicates whether the provider supports OUTER JOINs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-201">特殊文字</span><span class="sxs-lookup"><span data-stu-id="0137b-201">Special Characters</span></span><br />
<span data-ttu-id="0137b-202">(KAGPROP_SPECIALCHARACTERS)</span><span class="sxs-lookup"><span data-stu-id="0137b-202">(KAGPROP_SPECIALCHARACTERS)</span></span></p></td>
<td><p><span data-ttu-id="0137b-203">ODBC ドライバーで特別な意味を持つ文字を示します。</span><span class="sxs-lookup"><span data-stu-id="0137b-203">Indicates which characters have special meaning for the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-204">ストアド プロシージャ</span><span class="sxs-lookup"><span data-stu-id="0137b-204">Stored Procedures</span></span><br />
<span data-ttu-id="0137b-205">(KAGPROP_PROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="0137b-205">(KAGPROP_PROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="0137b-206">この ODBC ドライバーでストアド プロシージャを使用できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="0137b-206">Indicates whether stored procedures are available for use with this ODBC driver.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-207">文字列を処理する関数</span><span class="sxs-lookup"><span data-stu-id="0137b-207">String Functions</span></span><br />
<span data-ttu-id="0137b-208">(KAGPROP_STRINGFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="0137b-208">(KAGPROP_STRINGFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="0137b-p110">ODBC ドライバーがサポートする文字列関数を示します。関数名とこのビットマスクで使用される関連付けられた値の一覧については、ODBC マニュアルの「Appendix E: Scalar Functions」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0137b-p110">Indicates which string functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-211">システム関数</span><span class="sxs-lookup"><span data-stu-id="0137b-211">System Functions</span></span><br />
<span data-ttu-id="0137b-212">(KAGPROP_SYSTEMFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="0137b-212">(KAGPROP_SYSTEMFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="0137b-p111">ODBC ドライバーがサポートするシステム関数を示します。関数名とこのビットマスクで使用される関連付けられた値の一覧については、ODBC マニュアルの「Appendix E: Scalar Functions」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0137b-p111">Indicates which system functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-215">日付/時刻関数</span><span class="sxs-lookup"><span data-stu-id="0137b-215">Time/Date Functions</span></span><br />
<span data-ttu-id="0137b-216">(KAGPROP_TIMEDATEFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="0137b-216">(KAGPROP_TIMEDATEFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="0137b-p112">ODBC ドライバーがサポートする時刻/日付関数を示します。関数名とこのビットマスクで使用される関連付けられた値の一覧については、ODBC マニュアルの「Appendix E: Scalar Functions」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0137b-p112">Indicates which time and date functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-219">SQL の文法のサポート</span><span class="sxs-lookup"><span data-stu-id="0137b-219">SQL Grammar Support</span></span><br />
<span data-ttu-id="0137b-220">(KAGPROP_ODBCSQLCONFORMANCE)</span><span class="sxs-lookup"><span data-stu-id="0137b-220">(KAGPROP_ODBCSQLCONFORMANCE)</span></span></p></td>
<td><p><span data-ttu-id="0137b-221">ODBC ドライバーがサポートする SQL 文法を示します。</span><span class="sxs-lookup"><span data-stu-id="0137b-221">Indicates the SQL grammar that the ODBC driver supports.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a><span data-ttu-id="0137b-222">プロバイダー固有の Recordset および Command のプロパティ</span><span class="sxs-lookup"><span data-stu-id="0137b-222">Provider-Specific Recordset and Command Properties</span></span>

<span data-ttu-id="0137b-p113">OLE DB Provider for ODBC は、 **Recordset** オブジェクトと **Command** オブジェクトの **Properties** コレクションにプロパティを追加します。次の表は、これらのプロパティの一覧で、かっこ内は対応する OLE DB プロパティ名です。</span><span class="sxs-lookup"><span data-stu-id="0137b-p113">The OLE DB provider for ODBC adds several properties to the **Properties** collection of the **Recordset** and **Command** objects. The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0137b-225">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="0137b-225">Property Name</span></span></p></th>
<th><p><span data-ttu-id="0137b-226">説明</span><span class="sxs-lookup"><span data-stu-id="0137b-226">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0137b-227">クエリベースの更新/削除/挿入</span><span class="sxs-lookup"><span data-stu-id="0137b-227">Query Based Updates/Deletes/Inserts</span></span><br />
<span data-ttu-id="0137b-228">(KAGPROP_QUERYBASEDUPDATES)</span><span class="sxs-lookup"><span data-stu-id="0137b-228">(KAGPROP_QUERYBASEDUPDATES)</span></span></p></td>
<td><p><span data-ttu-id="0137b-229">SQL クエリを使用して更新、削除、および挿入を実行できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="0137b-229">Indicates whether updates, deletions, and insertions can be performed using SQL queries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-230">ODBC の同時実行の種類</span><span class="sxs-lookup"><span data-stu-id="0137b-230">ODBC Concurrency Type</span></span><br />
<span data-ttu-id="0137b-231">(KAGPROP_CONCURRENCY)</span><span class="sxs-lookup"><span data-stu-id="0137b-231">(KAGPROP_CONCURRENCY)</span></span></p></td>
<td><p><span data-ttu-id="0137b-232">2 人のユーザーがデータ ソースの同じデータに同時にアクセスしようとしたときに発生する問題を減少させるための方法を示します。</span><span class="sxs-lookup"><span data-stu-id="0137b-232">Indicates the method used to reduce potential problems caused by two users attempting to access the same data from the data source simultaneously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-233">順方向専用カーソルの BLOB のアクセシビリティ</span><span class="sxs-lookup"><span data-stu-id="0137b-233">BLOB accessibility on Forward-Only cursor</span></span><br />
<span data-ttu-id="0137b-234">(KAGPROP_BLOBSONFOCURSOR)</span><span class="sxs-lookup"><span data-stu-id="0137b-234">(KAGPROP_BLOBSONFOCURSOR)</span></span></p></td>
<td><p><span data-ttu-id="0137b-235">前方のみのカーソルの使用時に BLOB <strong>Fields</strong> にアクセスできるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="0137b-235">Indicates whether BLOB <strong>Fields</strong> can be accessed when using a forward-only cursor.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-236">SQL_FLOAT、SQL_DOUBLE、および SQL_REAL を QBU WHERE 句に含める</span><span class="sxs-lookup"><span data-stu-id="0137b-236">Include SQL_FLOAT, SQL_DOUBLE, and SQL_REAL in QBU WHERE clauses</span></span><br />
<span data-ttu-id="0137b-237">(KAGPROP_INCLUDENONEXACT)</span><span class="sxs-lookup"><span data-stu-id="0137b-237">(KAGPROP_INCLUDENONEXACT)</span></span></p></td>
<td><p><span data-ttu-id="0137b-238">SQL_FLOAT、SQL_DOUBLE、および SQL_REAL の値を QBU WHERE 句に含めることができるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="0137b-238">Indicates whether SQL_FLOAT, SQL_DOUBLE, and SQL_REAL values can be included in a QBU WHERE clause.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-239">挿入後の最後の行の位置</span><span class="sxs-lookup"><span data-stu-id="0137b-239">Position on the last row after insert</span></span><br />
<span data-ttu-id="0137b-240">(KAGPROP_POSITIONONNEWROW)</span><span class="sxs-lookup"><span data-stu-id="0137b-240">(KAGPROP_POSITIONONNEWROW)</span></span></p></td>
<td><p><span data-ttu-id="0137b-241">新規レコードをテーブルに挿入した後、テーブルの最後の行が現在の行になるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="0137b-241">Indicates that after a new record has been inserted in a table, the last row in the table will be come the current row.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-242">IRowsetChangeExtInfo</span><span class="sxs-lookup"><span data-stu-id="0137b-242">IRowsetChangeExtInfo</span></span><br />
<span data-ttu-id="0137b-243">(KAGPROP_IROWSETCHANGEEXTINFO)</span><span class="sxs-lookup"><span data-stu-id="0137b-243">(KAGPROP_IROWSETCHANGEEXTINFO)</span></span></p></td>
<td><p><span data-ttu-id="0137b-244"><strong>IRowsetChange</strong> インターフェイスが拡張情報を提供するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="0137b-244">Indicates whether the <strong>IRowsetChange</strong> interface provides extended information support.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-245">ODBC カーソルの種類</span><span class="sxs-lookup"><span data-stu-id="0137b-245">ODBC Cursor Type</span></span><br />
<span data-ttu-id="0137b-246">(KAGPROP_CURSOR)</span><span class="sxs-lookup"><span data-stu-id="0137b-246">(KAGPROP_CURSOR)</span></span></p></td>
<td><p><span data-ttu-id="0137b-247"><strong>Recordset</strong> で使用されるカーソルの種類を示します。</span><span class="sxs-lookup"><span data-stu-id="0137b-247">Indicates the type of cursor used by the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-248">マーシャ リングできる行セットを生成します。</span><span class="sxs-lookup"><span data-stu-id="0137b-248">Generate a Rowset that can be marshaled</span></span><br />
<span data-ttu-id="0137b-249">(KAGPROP_MARSHALLABLE)</span><span class="sxs-lookup"><span data-stu-id="0137b-249">(KAGPROP_MARSHALLABLE)</span></span></p></td>
<td><p><span data-ttu-id="0137b-250">ODBC ドライバーがマーシャリング可能なレコードセットを生成することを示します。</span><span class="sxs-lookup"><span data-stu-id="0137b-250">Indicates that the ODBC driver generates a recordset that can be marshaled</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a><span data-ttu-id="0137b-251">コマンド テキスト</span><span class="sxs-lookup"><span data-stu-id="0137b-251">Command Text</span></span>

<span data-ttu-id="0137b-252">[Command](command-object-ado.md) オブジェクトの使用方法は、データ ソースおよび受け付けられるクエリまたはコマンド ステートメントの種類によって大きく異なります。</span><span class="sxs-lookup"><span data-stu-id="0137b-252">How you use the [Command](command-object-ado.md) object largely depends on the data source, and what type of query or command statement it will accept.</span></span>

<span data-ttu-id="0137b-253">ODBC には、ストアド プロシージャを呼び出すための独自の構文があります。</span><span class="sxs-lookup"><span data-stu-id="0137b-253">ODBC provides a specific syntax for calling stored procedures.</span></span> <span data-ttu-id="0137b-254">**コマンド**オブジェクト、 [Connection](connection-object-ado.md)オブジェクトの**Execute**メソッドの*CommandText*引数、または[Recordset](recordset-object-ado.md)の**Open**メソッドの*Source*引数の[CommandText](commandtext-property-ado.md)プロパティのオブジェクトは、この構文を使用して文字列に渡します。</span><span class="sxs-lookup"><span data-stu-id="0137b-254">For the [CommandText](commandtext-property-ado.md) property of a **Command** object, the *CommandText* argument to the **Execute** method on a [Connection](connection-object-ado.md) object, or the *Source* argument to the **Open** method on a [Recordset](recordset-object-ado.md) object, passes in a string with this syntax:</span></span>

`"{ [ ? = ] call procedure [ ( ? [, ? [ ,  ]] ) ] }"`

<span data-ttu-id="0137b-p115">**?** はそれぞれ [Parameters](parameters-collection-ado.md) コレクションのオブジェクトを参照します。最初の **?** は **Parameters**(0) を参照し、次の **?** は **Parameters**(1) を参照し、以下同様に続きます。</span><span class="sxs-lookup"><span data-stu-id="0137b-p115">Each **?** references an object in the [Parameters](parameters-collection-ado.md) collection. The first **?** references **Parameters**(0), the next **?** references **Parameters**(1), and so on.</span></span>

<span data-ttu-id="0137b-p116">パラメーターの参照は省略可能で、ストアド プロシージャの構造に依存します。パラメーターを定義していないストアド プロシージャを呼び出す場合の構文は、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="0137b-p116">The parameter references are optional and depend on the structure of the stored procedure. If you want to call a stored procedure that defines no parameters, your string would look like this:</span></span>

`"{ call procedure }"`

<span data-ttu-id="0137b-262">2 つのクエリ パラメーターを持つ場合は、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="0137b-262">If you have two query parameters, your string would look like this:</span></span>

`"{ call procedure ( ?, ? ) }"`

<span data-ttu-id="0137b-p117">ストアド プロシージャが値を返す場合、戻り値は別のパラメーターとして扱われます。クエリ パラメーターがなく、戻り値がある場合は、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="0137b-p117">If the stored procedure will return a value, the return value is treated as another parameter. If you have no query parameters but you do have a return value, your string would look like this:</span></span>

`"{ ? = call procedure }"`

<span data-ttu-id="0137b-265">戻り値があり、2 つのクエリ パラメーターがある場合は、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="0137b-265">Finally, if you have a return value and two query parameters, your string would look like this:</span></span>

`"{ ? = call procedure ( ?, ? ) }"`

## <a name="recordset-behavior"></a><span data-ttu-id="0137b-266">Recordset の動作</span><span class="sxs-lookup"><span data-stu-id="0137b-266">Recordset Behavior</span></span>

<span data-ttu-id="0137b-267">次の表は、このプロバイダーで開かれた **Recordset** オブジェクトで利用可能な標準の ADO メソッドと ADO プロパティの一覧です。</span><span class="sxs-lookup"><span data-stu-id="0137b-267">The following tables list the standard ADO methods and properties available on a **Recordset** object opened with this provider.</span></span>

<span data-ttu-id="0137b-268">プロバイダーの構成による **Recordset** の動作の詳細については、 [Supports](supports-method-ado.md) メソッドを実行し、 **Recordset** の **Properties** コレクションを列挙して、プロバイダー固有の動的プロパティが存在するかどうかを確認してください。</span><span class="sxs-lookup"><span data-stu-id="0137b-268">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the **Properties** collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="0137b-269">標準的な ADO **Recordset** のプロパティの利用可能性は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="0137b-269">Availability of standard ADO **Recordset** properties:</span></span>

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
<th><p><span data-ttu-id="0137b-270">プロパティ</span><span class="sxs-lookup"><span data-stu-id="0137b-270">Property</span></span></p></th>
<th><p><span data-ttu-id="0137b-271">前方向</span><span class="sxs-lookup"><span data-stu-id="0137b-271">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="0137b-272">動的</span><span class="sxs-lookup"><span data-stu-id="0137b-272">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="0137b-273">キーセット</span><span class="sxs-lookup"><span data-stu-id="0137b-273">Keyset</span></span></p></th>
<th><p><span data-ttu-id="0137b-274">静的</span><span class="sxs-lookup"><span data-stu-id="0137b-274">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0137b-275"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="0137b-275"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="0137b-276">利用不可</span><span class="sxs-lookup"><span data-stu-id="0137b-276">not available</span></span></p></td>
<td><p><span data-ttu-id="0137b-277">利用不可</span><span class="sxs-lookup"><span data-stu-id="0137b-277">not available</span></span></p></td>
<td><p><span data-ttu-id="0137b-278">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-278">read/write</span></span></p></td>
<td><p><span data-ttu-id="0137b-279">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-279">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-280"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="0137b-280"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="0137b-281">利用不可</span><span class="sxs-lookup"><span data-stu-id="0137b-281">not available</span></span></p></td>
<td><p><span data-ttu-id="0137b-282">利用不可</span><span class="sxs-lookup"><span data-stu-id="0137b-282">not available</span></span></p></td>
<td><p><span data-ttu-id="0137b-283">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-283">read/write</span></span></p></td>
<td><p><span data-ttu-id="0137b-284">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-284">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-285"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="0137b-285"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="0137b-286">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-286">read/write</span></span></p></td>
<td><p><span data-ttu-id="0137b-287">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-287">read/write</span></span></p></td>
<td><p><span data-ttu-id="0137b-288">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-288">read/write</span></span></p></td>
<td><p><span data-ttu-id="0137b-289">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-289">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-290"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="0137b-290"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="0137b-291">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="0137b-291">read-only</span></span></p></td>
<td><p><span data-ttu-id="0137b-292">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="0137b-292">read-only</span></span></p></td>
<td><p><span data-ttu-id="0137b-293">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="0137b-293">read-only</span></span></p></td>
<td><p><span data-ttu-id="0137b-294">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="0137b-294">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-295"><a href="bookmark-property-ado.md">Bookmark</a></span><span class="sxs-lookup"><span data-stu-id="0137b-295"><a href="bookmark-property-ado.md">Bookmark</a></span></span></p></td>
<td><p><span data-ttu-id="0137b-296">利用不可</span><span class="sxs-lookup"><span data-stu-id="0137b-296">not available</span></span></p></td>
<td><p><span data-ttu-id="0137b-297">利用不可</span><span class="sxs-lookup"><span data-stu-id="0137b-297">not available</span></span></p></td>
<td><p><span data-ttu-id="0137b-298">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-298">read/write</span></span></p></td>
<td><p><span data-ttu-id="0137b-299">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-299">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-300"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="0137b-300"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="0137b-301">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-301">read/write</span></span></p></td>
<td><p><span data-ttu-id="0137b-302">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-302">read/write</span></span></p></td>
<td><p><span data-ttu-id="0137b-303">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-303">read/write</span></span></p></td>
<td><p><span data-ttu-id="0137b-304">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-304">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-305"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="0137b-305"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="0137b-306">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-306">read/write</span></span></p></td>
<td><p><span data-ttu-id="0137b-307">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-307">read/write</span></span></p></td>
<td><p><span data-ttu-id="0137b-308">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-308">read/write</span></span></p></td>
<td><p><span data-ttu-id="0137b-309">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-309">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-310"><a href="cursortype-property-ado.md">カーソル。</a></span><span class="sxs-lookup"><span data-stu-id="0137b-310"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="0137b-311">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-311">read/write</span></span></p></td>
<td><p><span data-ttu-id="0137b-312">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-312">read/write</span></span></p></td>
<td><p><span data-ttu-id="0137b-313">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-313">read/write</span></span></p></td>
<td><p><span data-ttu-id="0137b-314">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-314">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-315"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="0137b-315"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="0137b-316">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="0137b-316">read-only</span></span></p></td>
<td><p><span data-ttu-id="0137b-317">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="0137b-317">read-only</span></span></p></td>
<td><p><span data-ttu-id="0137b-318">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="0137b-318">read-only</span></span></p></td>
<td><p><span data-ttu-id="0137b-319">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="0137b-319">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-320"><a href="filter-property-ado.md">Filter</a></span><span class="sxs-lookup"><span data-stu-id="0137b-320"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="0137b-321">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-321">read/write</span></span></p></td>
<td><p><span data-ttu-id="0137b-322">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-322">read/write</span></span></p></td>
<td><p><span data-ttu-id="0137b-323">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-323">read/write</span></span></p></td>
<td><p><span data-ttu-id="0137b-324">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-324">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-325"><a href="locktype-property-ado.md">ロック。</a></span><span class="sxs-lookup"><span data-stu-id="0137b-325"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="0137b-326">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-326">read/write</span></span></p></td>
<td><p><span data-ttu-id="0137b-327">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-327">read/write</span></span></p></td>
<td><p><span data-ttu-id="0137b-328">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-328">read/write</span></span></p></td>
<td><p><span data-ttu-id="0137b-329">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-329">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-330"><a href="marshaloptions-property-ado.md">スレッド</a></span><span class="sxs-lookup"><span data-stu-id="0137b-330"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="0137b-331">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-331">read/write</span></span></p></td>
<td><p><span data-ttu-id="0137b-332">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-332">read/write</span></span></p></td>
<td><p><span data-ttu-id="0137b-333">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-333">read/write</span></span></p></td>
<td><p><span data-ttu-id="0137b-334">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-334">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-335"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="0137b-335"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="0137b-336">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-336">read/write</span></span></p></td>
<td><p><span data-ttu-id="0137b-337">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-337">read/write</span></span></p></td>
<td><p><span data-ttu-id="0137b-338">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-338">read/write</span></span></p></td>
<td><p><span data-ttu-id="0137b-339">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-339">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-340"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="0137b-340"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="0137b-341">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-341">read/write</span></span></p></td>
<td><p><span data-ttu-id="0137b-342">利用不可</span><span class="sxs-lookup"><span data-stu-id="0137b-342">not available</span></span></p></td>
<td><p><span data-ttu-id="0137b-343">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="0137b-343">read-only</span></span></p></td>
<td><p><span data-ttu-id="0137b-344">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="0137b-344">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-345"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="0137b-345"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="0137b-346">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-346">read/write</span></span></p></td>
<td><p><span data-ttu-id="0137b-347">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-347">read/write</span></span></p></td>
<td><p><span data-ttu-id="0137b-348">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-348">read/write</span></span></p></td>
<td><p><span data-ttu-id="0137b-349">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-349">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-350"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="0137b-350"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="0137b-351">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-351">read/write</span></span></p></td>
<td><p><span data-ttu-id="0137b-352">利用不可</span><span class="sxs-lookup"><span data-stu-id="0137b-352">not available</span></span></p></td>
<td><p><span data-ttu-id="0137b-353">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="0137b-353">read-only</span></span></p></td>
<td><p><span data-ttu-id="0137b-354">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="0137b-354">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-355"><a href="source-property-ado-recordset.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="0137b-355"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="0137b-356">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-356">read/write</span></span></p></td>
<td><p><span data-ttu-id="0137b-357">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-357">read/write</span></span></p></td>
<td><p><span data-ttu-id="0137b-358">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-358">read/write</span></span></p></td>
<td><p><span data-ttu-id="0137b-359">値の取得および設定</span><span class="sxs-lookup"><span data-stu-id="0137b-359">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-360"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="0137b-360"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="0137b-361">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="0137b-361">read-only</span></span></p></td>
<td><p><span data-ttu-id="0137b-362">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="0137b-362">read-only</span></span></p></td>
<td><p><span data-ttu-id="0137b-363">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="0137b-363">read-only</span></span></p></td>
<td><p><span data-ttu-id="0137b-364">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="0137b-364">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-365"><a href="status-property-ado-recordset.md">Status</a></span><span class="sxs-lookup"><span data-stu-id="0137b-365"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="0137b-366">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="0137b-366">read-only</span></span></p></td>
<td><p><span data-ttu-id="0137b-367">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="0137b-367">read-only</span></span></p></td>
<td><p><span data-ttu-id="0137b-368">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="0137b-368">read-only</span></span></p></td>
<td><p><span data-ttu-id="0137b-369">値の取得のみ</span><span class="sxs-lookup"><span data-stu-id="0137b-369">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0137b-370">バージョン 1.0 の Microsoft OLE DB Provider for ODBC で ADO を使用する場合、[AbsolutePosition](absoluteposition-property-ado.md) プロパティと [AbsolutePage](absolutepage-property-ado.md) プロパティは値の設定のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="0137b-370">The [AbsolutePosition](absoluteposition-property-ado.md) and [AbsolutePage](absolutepage-property-ado.md) properties are write-only when ADO is used with version 1.0 of the Microsoft OLE DB Provider for ODBC.</span></span>

<span data-ttu-id="0137b-371">標準的な ADO **Recordset** のメソッドの利用可能性は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="0137b-371">Availability of standard ADO **Recordset** methods:</span></span>

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
<th><p><span data-ttu-id="0137b-372">メソッド</span><span class="sxs-lookup"><span data-stu-id="0137b-372">Method</span></span></p></th>
<th><p><span data-ttu-id="0137b-373">前方向</span><span class="sxs-lookup"><span data-stu-id="0137b-373">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="0137b-374">動的</span><span class="sxs-lookup"><span data-stu-id="0137b-374">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="0137b-375">キーセット</span><span class="sxs-lookup"><span data-stu-id="0137b-375">Keyset</span></span></p></th>
<th><p><span data-ttu-id="0137b-376">静的</span><span class="sxs-lookup"><span data-stu-id="0137b-376">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0137b-377"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="0137b-377"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="0137b-378">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-378">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-379">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-379">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-380">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-380">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-381">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-381">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-382"><a href="cancel-method-ado.md">Cancel</a></span><span class="sxs-lookup"><span data-stu-id="0137b-382"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="0137b-383">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-383">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-384">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-384">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-385">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-385">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-386">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-386">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-387"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="0137b-387"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="0137b-388">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-388">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-389">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-389">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-390">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-390">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-391">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-391">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-392"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="0137b-392"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="0137b-393">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-393">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-394">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-394">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-395">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-395">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-396">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-396">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-397"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="0137b-397"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="0137b-398">いいえ</span><span class="sxs-lookup"><span data-stu-id="0137b-398">No</span></span></p></td>
<td><p><span data-ttu-id="0137b-399">いいえ</span><span class="sxs-lookup"><span data-stu-id="0137b-399">No</span></span></p></td>
<td><p><span data-ttu-id="0137b-400">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-400">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-401">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-401">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-402"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="0137b-402"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="0137b-403">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-403">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-404">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-404">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-405">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-405">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-406">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-406">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-407"><a href="delete-method-ado-recordset.md">Delete</a></span><span class="sxs-lookup"><span data-stu-id="0137b-407"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="0137b-408">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-408">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-409">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-409">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-410">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-410">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-411">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-411">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-412"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="0137b-412"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="0137b-413">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-413">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-414">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-414">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-415">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-415">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-416">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-416">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-417"><a href="move-method-ado.md">Move</a></span><span class="sxs-lookup"><span data-stu-id="0137b-417"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="0137b-418">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-418">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-419">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-419">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-420">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-420">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-421">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-421">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-422"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="0137b-422"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="0137b-423">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-423">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-424">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-424">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-425">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-425">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-426">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-426">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-427"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span><span class="sxs-lookup"><span data-stu-id="0137b-427"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span></span></p></td>
<td><p><span data-ttu-id="0137b-428">いいえ</span><span class="sxs-lookup"><span data-stu-id="0137b-428">No</span></span></p></td>
<td><p><span data-ttu-id="0137b-429">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-429">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-430">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-430">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-431">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-431">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-432"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span><span class="sxs-lookup"><span data-stu-id="0137b-432"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span></span></p></td>
<td><p><span data-ttu-id="0137b-433">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-433">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-434">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-434">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-435">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-435">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-436">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-436">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-437"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="0137b-437"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="0137b-438">いいえ</span><span class="sxs-lookup"><span data-stu-id="0137b-438">No</span></span></p></td>
<td><p><span data-ttu-id="0137b-439">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-439">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-440">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-440">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-441">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-441">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-442"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span><span class="sxs-lookup"><span data-stu-id="0137b-442"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span></span></p></td>
<td><p><span data-ttu-id="0137b-443">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-443">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-444">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-444">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-445">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-445">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-446">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-446">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-447"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="0137b-447"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="0137b-448">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-448">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-449">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-449">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-450">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-450">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-451">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-451">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-452"><a href="requery-method-ado.md">Requery</a></span><span class="sxs-lookup"><span data-stu-id="0137b-452"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="0137b-453">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-453">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-454">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-454">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-455">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-455">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-456">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-456">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-457"><a href="resync-method-ado.md">再同期</a></span><span class="sxs-lookup"><span data-stu-id="0137b-457"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="0137b-458">いいえ</span><span class="sxs-lookup"><span data-stu-id="0137b-458">No</span></span></p></td>
<td><p><span data-ttu-id="0137b-459">いいえ</span><span class="sxs-lookup"><span data-stu-id="0137b-459">No</span></span></p></td>
<td><p><span data-ttu-id="0137b-460">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-460">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-461">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-461">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-462"><a href="supports-method-ado.md">サポートしています</a></span><span class="sxs-lookup"><span data-stu-id="0137b-462"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="0137b-463">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-463">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-464">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-464">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-465">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-465">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-466">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-466">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-467"><a href="update-method-ado.md">Update</a></span><span class="sxs-lookup"><span data-stu-id="0137b-467"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="0137b-468">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-468">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-469">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-469">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-470">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-470">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-471">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-471">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-472"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="0137b-472"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="0137b-473">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-473">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-474">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-474">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-475">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-475">Yes</span></span></p></td>
<td><p><span data-ttu-id="0137b-476">はい</span><span class="sxs-lookup"><span data-stu-id="0137b-476">Yes</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0137b-477">\*Microsoft Access データベースではサポートされません。</span><span class="sxs-lookup"><span data-stu-id="0137b-477">\*Not supported for Microsoft Access databases.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="0137b-478">動的プロパティ</span><span class="sxs-lookup"><span data-stu-id="0137b-478">Dynamic Properties</span></span>

<span data-ttu-id="0137b-479">Microsoft OLE DB Provider for ODBC は、開かれていない **Connection** オブジェクト、 [Recordset](connection-object-ado.md) オブジェクト、および [Command](recordset-object-ado.md) オブジェクトの [Properties](command-object-ado.md) コレクションに動的プロパティを挿入します。</span><span class="sxs-lookup"><span data-stu-id="0137b-479">The Microsoft OLE DB Provider for ODBC inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="0137b-p118">以下の表は、各動的プロパティの ADO 名と OLE DB 名の対応表です。 「OLE DB プログラマ リファレンス」では、「説明」欄に ADO プロパティ名が示されています。プロパティの詳細については、「OLE DB プログラマ リファレンス」を参照してください。OLE DB プロパティ名をキーワードとして検索するか、「付録 C: プロパティ表」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0137b-p118">The tables below are a cross-index of the ADO and OLE DB names for each dynamic property. The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description." You can find more information about these properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="0137b-484">Connection の動的プロパティ</span><span class="sxs-lookup"><span data-stu-id="0137b-484">Connection Dynamic Properties</span></span>

<span data-ttu-id="0137b-485">次に示すプロパティが **Connection** オブジェクトの **Properties** コレクションに追加されます。</span><span class="sxs-lookup"><span data-stu-id="0137b-485">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0137b-486">ADO プロパティ名</span><span class="sxs-lookup"><span data-stu-id="0137b-486">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="0137b-487">OLE DB プロパティ名</span><span class="sxs-lookup"><span data-stu-id="0137b-487">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0137b-488">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="0137b-488">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="0137b-489">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="0137b-489">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-490">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="0137b-490">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="0137b-491">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="0137b-491">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-492">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="0137b-492">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="0137b-493">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="0137b-493">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-494">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="0137b-494">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="0137b-495">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="0137b-495">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-496">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="0137b-496">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="0137b-497">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="0137b-497">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-498">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="0137b-498">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="0137b-499">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="0137b-499">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-500">Column Definition</span><span class="sxs-lookup"><span data-stu-id="0137b-500">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="0137b-501">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="0137b-501">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-502">Connect Timeout</span><span class="sxs-lookup"><span data-stu-id="0137b-502">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="0137b-503">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="0137b-503">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-504">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="0137b-504">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="0137b-505">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="0137b-505">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-506">Data Source</span><span class="sxs-lookup"><span data-stu-id="0137b-506">Data Source</span></span></p></td>
<td><p><span data-ttu-id="0137b-507">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="0137b-507">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-508">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="0137b-508">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="0137b-509">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="0137b-509">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-510">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="0137b-510">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="0137b-511">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="0137b-511">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-512">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="0137b-512">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="0137b-513">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="0137b-513">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-514">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="0137b-514">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="0137b-515">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="0137b-515">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-516">Extended Properties</span><span class="sxs-lookup"><span data-stu-id="0137b-516">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="0137b-517">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="0137b-517">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-518">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="0137b-518">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="0137b-519">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="0137b-519">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-520">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="0137b-520">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="0137b-521">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="0137b-521">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-522">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="0137b-522">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="0137b-523">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="0137b-523">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-524">Initial Catalog</span><span class="sxs-lookup"><span data-stu-id="0137b-524">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="0137b-525">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="0137b-525">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-526">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="0137b-526">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="0137b-527">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="0137b-527">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-528">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="0137b-528">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="0137b-529">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="0137b-529">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-530">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="0137b-530">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="0137b-531">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="0137b-531">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-532">Location</span><span class="sxs-lookup"><span data-stu-id="0137b-532">Location</span></span></p></td>
<td><p><span data-ttu-id="0137b-533">DBPROP_INIT_LOCATION</span><span class="sxs-lookup"><span data-stu-id="0137b-533">DBPROP_INIT_LOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-534">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="0137b-534">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="0137b-535">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="0137b-535">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-536">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="0137b-536">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="0137b-537">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="0137b-537">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-538">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="0137b-538">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="0137b-539">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="0137b-539">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-540">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="0137b-540">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="0137b-541">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="0137b-541">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-542">Mode</span><span class="sxs-lookup"><span data-stu-id="0137b-542">Mode</span></span></p></td>
<td><p><span data-ttu-id="0137b-543">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="0137b-543">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-544">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="0137b-544">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="0137b-545">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="0137b-545">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-546">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="0137b-546">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="0137b-547">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="0137b-547">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-548">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="0137b-548">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="0137b-549">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="0137b-549">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-550">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="0137b-550">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="0137b-551">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="0137b-551">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-552">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="0137b-552">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="0137b-553">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="0137b-553">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-554">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="0137b-554">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="0137b-555">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="0137b-555">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-556">OLE DB Services</span><span class="sxs-lookup"><span data-stu-id="0137b-556">OLE DB Services</span></span></p></td>
<td><p><span data-ttu-id="0137b-557">DBPROP_INIT_OLEDBSERVICES</span><span class="sxs-lookup"><span data-stu-id="0137b-557">DBPROP_INIT_OLEDBSERVICES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-558">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="0137b-558">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="0137b-559">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="0137b-559">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-560">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="0137b-560">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="0137b-561">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="0137b-561">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-562">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="0137b-562">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="0137b-563">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="0137b-563">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-564">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="0137b-564">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="0137b-565">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="0137b-565">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-566">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="0137b-566">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="0137b-567">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="0137b-567">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-568">Password</span><span class="sxs-lookup"><span data-stu-id="0137b-568">Password</span></span></p></td>
<td><p><span data-ttu-id="0137b-569">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="0137b-569">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-570">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="0137b-570">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="0137b-571">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="0137b-571">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-572">Persist Security Info</span><span class="sxs-lookup"><span data-stu-id="0137b-572">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="0137b-573">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="0137b-573">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-574">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="0137b-574">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="0137b-575">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="0137b-575">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-576">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="0137b-576">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="0137b-577">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="0137b-577">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-578">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="0137b-578">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="0137b-579">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="0137b-579">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-580">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="0137b-580">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="0137b-581">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="0137b-581">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-582">Prompt</span><span class="sxs-lookup"><span data-stu-id="0137b-582">Prompt</span></span></p></td>
<td><p><span data-ttu-id="0137b-583">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="0137b-583">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-584">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="0137b-584">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="0137b-585">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="0137b-585">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-586">Provider Name</span><span class="sxs-lookup"><span data-stu-id="0137b-586">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="0137b-587">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="0137b-587">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-588">Provider Version</span><span class="sxs-lookup"><span data-stu-id="0137b-588">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="0137b-589">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="0137b-589">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-590">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="0137b-590">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="0137b-591">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="0137b-591">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-592">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="0137b-592">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="0137b-593">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="0137b-593">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-594">Schema Term</span><span class="sxs-lookup"><span data-stu-id="0137b-594">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="0137b-595">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="0137b-595">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-596">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="0137b-596">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="0137b-597">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="0137b-597">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-598">SQL Support</span><span class="sxs-lookup"><span data-stu-id="0137b-598">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="0137b-599">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="0137b-599">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-600">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="0137b-600">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="0137b-601">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="0137b-601">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-602">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="0137b-602">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="0137b-603">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="0137b-603">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-604">Table Term</span><span class="sxs-lookup"><span data-stu-id="0137b-604">Table Term</span></span></p></td>
<td><p><span data-ttu-id="0137b-605">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="0137b-605">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-606">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="0137b-606">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="0137b-607">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="0137b-607">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-608">User ID</span><span class="sxs-lookup"><span data-stu-id="0137b-608">User ID</span></span></p></td>
<td><p><span data-ttu-id="0137b-609">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="0137b-609">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-610">User Name</span><span class="sxs-lookup"><span data-stu-id="0137b-610">User Name</span></span></p></td>
<td><p><span data-ttu-id="0137b-611">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="0137b-611">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-612">Window Handle</span><span class="sxs-lookup"><span data-stu-id="0137b-612">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="0137b-613">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="0137b-613">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="0137b-614">Recordset の動的プロパティ</span><span class="sxs-lookup"><span data-stu-id="0137b-614">Recordset Dynamic Properties</span></span>

<span data-ttu-id="0137b-615">次に示すプロパティが **Recordset** オブジェクトの **Properties** コレクションに追加されます。</span><span class="sxs-lookup"><span data-stu-id="0137b-615">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0137b-616">ADO プロパティ名</span><span class="sxs-lookup"><span data-stu-id="0137b-616">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="0137b-617">OLE DB プロパティ名</span><span class="sxs-lookup"><span data-stu-id="0137b-617">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0137b-618">Access Order</span><span class="sxs-lookup"><span data-stu-id="0137b-618">Access Order</span></span></p></td>
<td><p><span data-ttu-id="0137b-619">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="0137b-619">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-620">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="0137b-620">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="0137b-621">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="0137b-621">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-622">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="0137b-622">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="0137b-623">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="0137b-623">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-624">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="0137b-624">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="0137b-625">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="0137b-625">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-626">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="0137b-626">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="0137b-627">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="0137b-627">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-628">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="0137b-628">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="0137b-629">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="0137b-629">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-630">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="0137b-630">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="0137b-631">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="0137b-631">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-632">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="0137b-632">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="0137b-633">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="0137b-633">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-634">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="0137b-634">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="0137b-635">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="0137b-635">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-636">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="0137b-636">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="0137b-637">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="0137b-637">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-638">IAccessor</span><span class="sxs-lookup"><span data-stu-id="0137b-638">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="0137b-639">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="0137b-639">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-640">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="0137b-640">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="0137b-641">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="0137b-641">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-642">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="0137b-642">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="0137b-643">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="0137b-643">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-644">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="0137b-644">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="0137b-645">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="0137b-645">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-646">IConvertType</span><span class="sxs-lookup"><span data-stu-id="0137b-646">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="0137b-647">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="0137b-647">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-648">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="0137b-648">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="0137b-649">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="0137b-649">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-650">IRowset</span><span class="sxs-lookup"><span data-stu-id="0137b-650">IRowset</span></span></p></td>
<td><p><span data-ttu-id="0137b-651">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="0137b-651">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-652">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="0137b-652">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="0137b-653">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="0137b-653">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-654">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="0137b-654">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="0137b-655">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="0137b-655">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-656">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="0137b-656">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="0137b-657">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="0137b-657">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-658">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="0137b-658">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="0137b-659">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="0137b-659">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-660">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="0137b-660">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-661">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="0137b-661">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="0137b-662">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="0137b-662">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-663">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="0137b-663">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="0137b-664">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="0137b-664">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-665">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="0137b-665">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="0137b-666">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="0137b-666">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-667">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="0137b-667">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="0137b-668">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="0137b-668">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-669">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="0137b-669">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="0137b-670">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="0137b-670">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-671">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="0137b-671">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="0137b-672">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="0137b-672">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-673">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="0137b-673">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="0137b-674">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="0137b-674">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-675">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="0137b-675">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="0137b-676">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="0137b-676">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-677">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="0137b-677">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="0137b-678">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="0137b-678">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-679">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="0137b-679">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="0137b-680">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="0137b-680">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-681">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="0137b-681">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="0137b-682">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="0137b-682">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-683">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="0137b-683">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="0137b-684">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="0137b-684">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-685">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="0137b-685">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="0137b-686">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="0137b-686">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-687">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="0137b-687">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="0137b-688">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="0137b-688">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-689">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="0137b-689">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="0137b-690">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="0137b-690">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-691">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="0137b-691">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="0137b-692">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="0137b-692">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-693">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="0137b-693">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="0137b-694">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="0137b-694">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-695">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="0137b-695">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="0137b-696">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="0137b-696">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-697">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="0137b-697">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="0137b-698">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="0137b-698">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-699">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="0137b-699">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="0137b-700">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="0137b-700">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-701">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="0137b-701">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="0137b-702">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="0137b-702">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-703">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="0137b-703">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="0137b-704">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="0137b-704">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-705">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="0137b-705">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="0137b-706">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="0137b-706">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-707">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="0137b-707">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="0137b-708">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="0137b-708">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-709">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="0137b-709">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="0137b-710">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="0137b-710">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-711">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="0137b-711">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="0137b-712">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="0137b-712">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-713">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="0137b-713">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="0137b-714">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="0137b-714">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-715">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="0137b-715">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="0137b-716">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="0137b-716">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-717">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="0137b-717">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="0137b-718">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="0137b-718">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-719">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="0137b-719">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="0137b-720">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="0137b-720">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-721">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="0137b-721">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="0137b-722">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="0137b-722">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-723">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="0137b-723">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="0137b-724">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="0137b-724">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-725">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="0137b-725">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="0137b-726">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="0137b-726">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-727">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="0137b-727">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="0137b-728">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="0137b-728">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-729">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="0137b-729">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="0137b-730">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="0137b-730">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-731">Unique Rows</span><span class="sxs-lookup"><span data-stu-id="0137b-731">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="0137b-732">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="0137b-732">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-733">Updatability</span><span class="sxs-lookup"><span data-stu-id="0137b-733">Updatability</span></span></p></td>
<td><p><span data-ttu-id="0137b-734">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="0137b-734">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-735">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="0137b-735">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="0137b-736">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="0137b-736">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="0137b-737">Command の動的プロパティ</span><span class="sxs-lookup"><span data-stu-id="0137b-737">Command Dynamic Properties</span></span>

<span data-ttu-id="0137b-738">次に示すプロパティが **Command** オブジェクトの **Properties** コレクションに追加されます。</span><span class="sxs-lookup"><span data-stu-id="0137b-738">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0137b-739">ADO プロパティ名</span><span class="sxs-lookup"><span data-stu-id="0137b-739">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="0137b-740">OLE DB プロパティ名</span><span class="sxs-lookup"><span data-stu-id="0137b-740">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0137b-741">Access Order</span><span class="sxs-lookup"><span data-stu-id="0137b-741">Access Order</span></span></p></td>
<td><p><span data-ttu-id="0137b-742">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="0137b-742">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-743">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="0137b-743">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="0137b-744">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="0137b-744">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-745">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="0137b-745">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="0137b-746">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="0137b-746">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-747">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="0137b-747">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="0137b-748">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="0137b-748">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-749">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="0137b-749">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="0137b-750">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="0137b-750">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-751">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="0137b-751">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="0137b-752">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="0137b-752">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-753">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="0137b-753">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="0137b-754">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="0137b-754">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-755">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="0137b-755">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="0137b-756">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="0137b-756">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-757">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="0137b-757">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="0137b-758">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="0137b-758">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-759">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="0137b-759">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="0137b-760">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="0137b-760">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-761">IAccessor</span><span class="sxs-lookup"><span data-stu-id="0137b-761">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="0137b-762">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="0137b-762">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-763">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="0137b-763">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="0137b-764">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="0137b-764">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-765">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="0137b-765">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="0137b-766">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="0137b-766">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-767">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="0137b-767">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="0137b-768">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="0137b-768">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-769">IConvertType</span><span class="sxs-lookup"><span data-stu-id="0137b-769">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="0137b-770">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="0137b-770">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-771">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="0137b-771">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="0137b-772">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="0137b-772">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-773">IRowset</span><span class="sxs-lookup"><span data-stu-id="0137b-773">IRowset</span></span></p></td>
<td><p><span data-ttu-id="0137b-774">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="0137b-774">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-775">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="0137b-775">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="0137b-776">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="0137b-776">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-777">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="0137b-777">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="0137b-778">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="0137b-778">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-779">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="0137b-779">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="0137b-780">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="0137b-780">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-781">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="0137b-781">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="0137b-782">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="0137b-782">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-783">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="0137b-783">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-784">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="0137b-784">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="0137b-785">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="0137b-785">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-786">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="0137b-786">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="0137b-787">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="0137b-787">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-788">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="0137b-788">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="0137b-789">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="0137b-789">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-790">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="0137b-790">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="0137b-791">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="0137b-791">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-792">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="0137b-792">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="0137b-793">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="0137b-793">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-794">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="0137b-794">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="0137b-795">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="0137b-795">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-796">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="0137b-796">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="0137b-797">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="0137b-797">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-798">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="0137b-798">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="0137b-799">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="0137b-799">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-800">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="0137b-800">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="0137b-801">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="0137b-801">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-802">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="0137b-802">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="0137b-803">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="0137b-803">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-804">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="0137b-804">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="0137b-805">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="0137b-805">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-806">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="0137b-806">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="0137b-807">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="0137b-807">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-808">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="0137b-808">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="0137b-809">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="0137b-809">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-810">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="0137b-810">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="0137b-811">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="0137b-811">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-812">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="0137b-812">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="0137b-813">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="0137b-813">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-814">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="0137b-814">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="0137b-815">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="0137b-815">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-816">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="0137b-816">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="0137b-817">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="0137b-817">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-818">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="0137b-818">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="0137b-819">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="0137b-819">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-820">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="0137b-820">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="0137b-821">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="0137b-821">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-822">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="0137b-822">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="0137b-823">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="0137b-823">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-824">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="0137b-824">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="0137b-825">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="0137b-825">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-826">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="0137b-826">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="0137b-827">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="0137b-827">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-828">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="0137b-828">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="0137b-829">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="0137b-829">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-830">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="0137b-830">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="0137b-831">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="0137b-831">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-832">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="0137b-832">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="0137b-833">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="0137b-833">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-834">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="0137b-834">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="0137b-835">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="0137b-835">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-836">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="0137b-836">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="0137b-837">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="0137b-837">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-838">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="0137b-838">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="0137b-839">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="0137b-839">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-840">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="0137b-840">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="0137b-841">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="0137b-841">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-842">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="0137b-842">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="0137b-843">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="0137b-843">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-844">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="0137b-844">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="0137b-845">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="0137b-845">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-846">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="0137b-846">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="0137b-847">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="0137b-847">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-848">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="0137b-848">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="0137b-849">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="0137b-849">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-850">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="0137b-850">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="0137b-851">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="0137b-851">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-852">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="0137b-852">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="0137b-853">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="0137b-853">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0137b-854">Updatability</span><span class="sxs-lookup"><span data-stu-id="0137b-854">Updatability</span></span></p></td>
<td><p><span data-ttu-id="0137b-855">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="0137b-855">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0137b-856">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="0137b-856">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="0137b-857">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="0137b-857">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="0137b-858">関連項目</span><span class="sxs-lookup"><span data-stu-id="0137b-858">See also</span></span>

<span data-ttu-id="0137b-859">特定の実装および ODBC 用 Microsoft OLE DB プロバイダーの機能の情報に関する詳細については、 [OLE DB プログラマ ガイド」](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85))を参照してくださいまたは[データ プラットフォーム デベロッパー センター](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0137b-859">For details regarding specific implementation and functional information about the Microsoft OLE DB Provider for ODBC, consult the [OLE DB Programmer's Guide](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) or visit the [Data Platform Developer Center](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span></span>

