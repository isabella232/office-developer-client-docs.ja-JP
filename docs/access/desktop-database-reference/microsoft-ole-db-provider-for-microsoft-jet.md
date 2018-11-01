---
title: Microsoft OLE DB Provider for Microsoft Jet
TOCTitle: Microsoft OLE DB Provider for Microsoft Jet
ms:assetid: 4a210d72-8c90-aa7c-4621-1a555a30a2d2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249228(v=office.15)
ms:contentKeyID: 48544660
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 39cb1288ef5e6be4f50d4ef976725122635db1dc
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884087"
---
# <a name="microsoft-ole-db-provider-for-microsoft-jet"></a><span data-ttu-id="e2c5a-102">Microsoft OLE DB Provider for Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="e2c5a-102">Microsoft OLE DB Provider for Microsoft Jet</span></span>

<span data-ttu-id="e2c5a-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e2c5a-104">OLE DB Provider for Microsoft Jet を使用すると、ADO から Microsoft Jet データベースにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-104">The OLE DB Provider for Microsoft Jet allows ADO to access Microsoft Jet databases.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="e2c5a-105">接続文字列のパラメーター</span><span class="sxs-lookup"><span data-stu-id="e2c5a-105">Connection String Parameters</span></span>

<span data-ttu-id="e2c5a-106">このプロバイダーに接続するには、*ConnectionString* プロパティの [Provider](connectionstring-property-ado.md) 引数を次のように設定します。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-106">To connect to this provider, set the *Provider* argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
Microsoft.Jet.OLEDB.4.0 
```

<span data-ttu-id="e2c5a-107">[Provider](provider-property-ado.md) プロパティを取得した場合も、この文字列が返されます。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-107">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="e2c5a-108">標準的な接続文字列</span><span class="sxs-lookup"><span data-stu-id="e2c5a-108">Typical Connection String</span></span>

<span data-ttu-id="e2c5a-109">このプロバイダーの標準的な接続文字列を次に示します。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-109">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=Microsoft.Jet.OLEDB.4.0;Data Source=databaseName;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="e2c5a-110">この文字列は、次に示すキーワードで構成されています。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-110">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e2c5a-111">キーワード</span><span class="sxs-lookup"><span data-stu-id="e2c5a-111">Keyword</span></span></p></th>
<th><p><span data-ttu-id="e2c5a-112">説明</span><span class="sxs-lookup"><span data-stu-id="e2c5a-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-113"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="e2c5a-113"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="e2c5a-114">OLE DB Provider for Microsoft Jet を指定します。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-114">Specifies the OLE DB Provider for Microsoft Jet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-115"><strong>Data Source</strong></span><span class="sxs-lookup"><span data-stu-id="e2c5a-115"><strong>Data Source</strong></span></span></p></td>
<td><p><span data-ttu-id="e2c5a-116">データベースのパスおよびファイル名を指定します (例: c:\Northwind.mdb)。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-116">Specifies the database path and file name (for example, c:\Northwind.mdb).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-117"><strong>User ID</strong></span><span class="sxs-lookup"><span data-stu-id="e2c5a-117"><strong>User ID</strong></span></span></p></td>
<td><p><span data-ttu-id="e2c5a-118">ユーザー名を指定します。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-118">Specifies the user name.</span></span> <span data-ttu-id="e2c5a-119">このキーワードを指定しない場合、文字列では、&quot;管理&quot;、既定で使用します。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-119">If this keyword is not specified, the string, &quot;admin&quot;, is used by default.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-120"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="e2c5a-120"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="e2c5a-121">ユーザー パスワードを指定します。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-121">Specifies the user password.</span></span> <span data-ttu-id="e2c5a-122">このキーワードを指定しない場合、空の文字列 (&quot;&quot;)、既定で使用します。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-122">If this keyword is not specified, the empty string (&quot;&quot;), is used by default.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a><span data-ttu-id="e2c5a-123">プロバイダー固有の接続パラメーター</span><span class="sxs-lookup"><span data-stu-id="e2c5a-123">Provider-Specific Connection Parameters</span></span>

<span data-ttu-id="e2c5a-p103">OLE DB Provider for Microsoft Jet は、ADO で定義されたプロパティに加えて、プロバイダー固有の動的プロパティをサポートしています。プロバイダー固有の接続パラメーターは他のすべての **Connection** パラメーターと同様に、 **Connection** オブジェクトの **Properties** コレクションで設定するか、接続文字列の一部として設定することができます。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-p103">The OLE DB Provider for Microsoft Jet supports several provider-specific dynamic properties in addition to those defined by ADO. As with all other **Connection** parameters, they can be set via the **Connection** object's **Properties** collection or as part of the connection string.</span></span>

<span data-ttu-id="e2c5a-126">次の表は、これらのプロパティの一覧で、かっこ内は対応する OLE DB プロパティ名です。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-126">The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e2c5a-127">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e2c5a-127">Parameter</span></span></p></th>
<th><p><span data-ttu-id="e2c5a-128">説明</span><span class="sxs-lookup"><span data-stu-id="e2c5a-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-129">Jet OLEDB:Compact 再生されるスペースの量</span><span class="sxs-lookup"><span data-stu-id="e2c5a-129">Jet OLEDB:Compact Reclaimed Space Amount</span></span><br />
<span data-ttu-id="e2c5a-130">(DBPROP_JETOLEDB_COMPACTFREESPACESIZE)</span><span class="sxs-lookup"><span data-stu-id="e2c5a-130">(DBPROP_JETOLEDB_COMPACTFREESPACESIZE)</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-p104">データベースの最適化によって増やすことができる空き領域の推定量をバイト単位で示します。この値は、データベース接続が確立した後でのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-p104">Indicates an estimate of the amount of space, in bytes, that can be reclaimed by compacting the database. This value is only valid after a database connection has been established.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-133">Jet OLEDB:Connection コントロール</span><span class="sxs-lookup"><span data-stu-id="e2c5a-133">Jet OLEDB:Connection Control</span></span><br />
<span data-ttu-id="e2c5a-134">(DBPROP_JETOLEDB_CONNECTIONCONTROL)</span><span class="sxs-lookup"><span data-stu-id="e2c5a-134">(DBPROP_JETOLEDB_CONNECTIONCONTROL)</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-135">ユーザーがデータベースに接続できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-135">Indicates whether users can connect to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-136">Jet OLEDB: システム データベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-136">Jet OLEDB:Create System Database</span></span><br />
<span data-ttu-id="e2c5a-137">(DBPROP_JETOLEDB_CREATESYSTEMDATABASE)</span><span class="sxs-lookup"><span data-stu-id="e2c5a-137">(DBPROP_JETOLEDB_CREATESYSTEMDATABASE)</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-138">新規データ ソースの作成時にシステム データベースを作成するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-138">Indicates whether a system database should be created when creating a new data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-139">Jet OLEDB:Database ロック モード</span><span class="sxs-lookup"><span data-stu-id="e2c5a-139">Jet OLEDB:Database Locking Mode</span></span><br />
<span data-ttu-id="e2c5a-140">(DBPROP_JETOLEDB_DATABASELOCKMODE)</span><span class="sxs-lookup"><span data-stu-id="e2c5a-140">(DBPROP_JETOLEDB_DATABASELOCKMODE)</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-p105">このデータベースのロック モードを示します。最初にデータベースを開いたユーザーが、データベースを開いているときに使用されるモードを決定します。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-p105">Indicates the locking mode for this database. The first user to open the database determines the mode used while the database is open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-143">Jet OLEDB:Database Password</span><span class="sxs-lookup"><span data-stu-id="e2c5a-143">Jet OLEDB:Database Password</span></span><br />
<span data-ttu-id="e2c5a-144">(DBPROP_JETOLEDB_DATABASEPASSWORD)</span><span class="sxs-lookup"><span data-stu-id="e2c5a-144">(DBPROP_JETOLEDB_DATABASEPASSWORD)</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-145">データベースのパスワードを示します。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-145">Indicates the database password.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-146">Jet OLEDB:Don't Copy Locale on Compact</span><span class="sxs-lookup"><span data-stu-id="e2c5a-146">Jet OLEDB:Don't Copy Locale on Compact</span></span><br />
<span data-ttu-id="e2c5a-147">(DBPROP_JETOLEDB_COMPACT_DONTCOPYLOCALE)</span><span class="sxs-lookup"><span data-stu-id="e2c5a-147">(DBPROP_JETOLEDB_COMPACT_DONTCOPYLOCALE)</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-148">データベースを最適化するときにロケール情報をコピーするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-148">Indicates whether Jet should copy locale information when compacting a database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-149">Jet OLEDB:Encrypt Database</span><span class="sxs-lookup"><span data-stu-id="e2c5a-149">Jet OLEDB:Encrypt Database</span></span><br />
<span data-ttu-id="e2c5a-150">(DBPROP_JETOLEDB_ENCRYPTDATABASE)</span><span class="sxs-lookup"><span data-stu-id="e2c5a-150">(DBPROP_JETOLEDB_ENCRYPTDATABASE)</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-p106">最適化したデータベースを暗号化するかどうかを示します。このプロパティを設定しない場合、元のデータベースが暗号化されている場合は、最適化したデータベースも暗号化されます。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-p106">Indicates whether a compacted database should be encrypted. If this property is not set, the compacted database will be encrypted if the original database was also encrypted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-153">Jet OLEDB:Engine Type</span><span class="sxs-lookup"><span data-stu-id="e2c5a-153">Jet OLEDB:Engine Type</span></span><br />
<span data-ttu-id="e2c5a-154">(DBPROP_JETOLEDB_ENGINE)</span><span class="sxs-lookup"><span data-stu-id="e2c5a-154">(DBPROP_JETOLEDB_ENGINE)</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-155">現在のデータ ストアにアクセスするために使用される記憶域エンジンを示します。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-155">Indicates the storage engine used to access the current data store.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-156">Jet OLEDB:Exclusive Async Delay</span><span class="sxs-lookup"><span data-stu-id="e2c5a-156">Jet OLEDB:Exclusive Async Delay</span></span><br />
<span data-ttu-id="e2c5a-157">(DBPROP_JETOLEDB_EXCLUSIVEASYNCDELAY)</span><span class="sxs-lookup"><span data-stu-id="e2c5a-157">(DBPROP_JETOLEDB_EXCLUSIVEASYNCDELAY)</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-p107">データベースが排他的に開かれている場合に、ディスクへの非同期書き込みで許容される最大遅延時間をミリ秒単位で示します。 <strong>Jet OLEDB:Flush Transaction Timeout</strong> が 0 に設定されていない場合、このプロパティは無視されます。  </span><span class="sxs-lookup"><span data-stu-id="e2c5a-p107">Indicates the maximum length of time, in milliseconds, that Jet can delay asynchronous writes to disk when the database is opened exclusively. This property is ignored unless <strong>Jet OLEDB:Flush Transaction Timeout</strong> is set to 0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-160">Jet OLEDB:Flush Transaction Timeout</span><span class="sxs-lookup"><span data-stu-id="e2c5a-160">Jet OLEDB:Flush Transaction Timeout</span></span><br />
<span data-ttu-id="e2c5a-161">(DBPROP_JETOLEDB_FLUSHTRANSACTIONTIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="e2c5a-161">(DBPROP_JETOLEDB_FLUSHTRANSACTIONTIMEOUT)</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-p108">非同期書き込みのためにキャッシュに保存されたデータが実際にディスクに書き込まれるまでの待ち時間を示します。この設定は、 <strong>Jet OLEDB:Shared Async Delay</strong> および <strong>Jet OLEDB:Exclusive Async Delay</strong> の値よりも優先されます。  </span><span class="sxs-lookup"><span data-stu-id="e2c5a-p108">Indicates the amount of time to wait before data stored in a cache for asynchronous writing is actually written to disk. This setting overrides the values for <strong>Jet OLEDB:Shared Async Delay</strong> and <strong>Jet OLEDB:Exclusive Async Delay</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-164">Jet OLEDB: グローバル一括トランザクション</span><span class="sxs-lookup"><span data-stu-id="e2c5a-164">Jet OLEDB:Global Bulk Transactions</span></span><br />
<span data-ttu-id="e2c5a-165">(DBPROP_JETOLEDB_GLOBALBULKNOTRANSACTIONS)</span><span class="sxs-lookup"><span data-stu-id="e2c5a-165">(DBPROP_JETOLEDB_GLOBALBULKNOTRANSACTIONS)</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-166">SQL 一括トランザクションが処理されるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-166">Indicates whether SQL bulk transactions are transacted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-167">Jet OLEDB: グローバル部分的な一括 Ops</span><span class="sxs-lookup"><span data-stu-id="e2c5a-167">Jet OLEDB:Global Partial Bulk Ops</span></span><br />
<span data-ttu-id="e2c5a-168">(DBPROP_JETOLEDB_GLOBALBULKPARTIAL)</span><span class="sxs-lookup"><span data-stu-id="e2c5a-168">(DBPROP_JETOLEDB_GLOBALBULKPARTIAL)</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-169">データベースを開くときに使用されるパスワードを示します。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-169">Indicates the password used to open the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-170">Jet OLEDB:Implicit Commit Sync</span><span class="sxs-lookup"><span data-stu-id="e2c5a-170">Jet OLEDB:Implicit Commit Sync</span></span><br />
<span data-ttu-id="e2c5a-171">(DBPROP_JETOLEDB_IMPLICITCOMMITSYNC)</span><span class="sxs-lookup"><span data-stu-id="e2c5a-171">(DBPROP_JETOLEDB_IMPLICITCOMMITSYNC)</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-172">暗黙の内部トランザクションで加えられた変更が、同期モードで書き込まれるか、非同期モードで書き込まれるかを示します。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-172">Indicates whether changes made in internal implicit transactions are written in synchronous or asynchronous mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-173">Jet OLEDB:Lock Delay</span><span class="sxs-lookup"><span data-stu-id="e2c5a-173">Jet OLEDB:Lock Delay</span></span><br />
<span data-ttu-id="e2c5a-174">(DBPROP_JETOLEDB_LOCKDELAY)</span><span class="sxs-lookup"><span data-stu-id="e2c5a-174">(DBPROP_JETOLEDB_LOCKDELAY)</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-175">ロックの取得に失敗した後、再試行までの待ち時間をミリ秒単位で示します。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-175">Indicates the number of milliseconds to wait before attempting to acquire a lock after a previous attempt has failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-176">Jet OLEDB:Lock Retry</span><span class="sxs-lookup"><span data-stu-id="e2c5a-176">Jet OLEDB:Lock Retry</span></span><br />
<span data-ttu-id="e2c5a-177">(DBPROP_JETOLEDB_LOCKRETRY)</span><span class="sxs-lookup"><span data-stu-id="e2c5a-177">(DBPROP_JETOLEDB_LOCKRETRY)</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-178">ロックされたページへのアクセスを試行する回数を示します。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-178">Indicates how many times an attempt to access a locked page is repeated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-179">Jet OLEDB:Max Buffer Size</span><span class="sxs-lookup"><span data-stu-id="e2c5a-179">Jet OLEDB:Max Buffer Size</span></span><br />
<span data-ttu-id="e2c5a-180">(DBPROP_JETOLEDB_MAXBUFFERSIZE)</span><span class="sxs-lookup"><span data-stu-id="e2c5a-180">(DBPROP_JETOLEDB_MAXBUFFERSIZE)</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-181">ディスクへの変更の反映を開始するまでに、Jet が使用できる最大メモリ量を KB 単位で示します。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-181">Indicates the maximum amount of memory, in kilobytes, Jet can use before it starts flushing changes to disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-182">Jet OLEDB:Max Locks Per File</span><span class="sxs-lookup"><span data-stu-id="e2c5a-182">Jet OLEDB:Max Locks Per File</span></span><br />
<span data-ttu-id="e2c5a-183">(DBPROP_JETOLEDB_MAXLOCKSPERFILE)</span><span class="sxs-lookup"><span data-stu-id="e2c5a-183">(DBPROP_JETOLEDB_MAXLOCKSPERFILE)</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-p109">データベースに配置できるロックの最大数を示します。既定値は 9500 です。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-p109">Indicates the maximum number of locks Jet can place on a database. The default value is 9500.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-186">Jet OLEDB: 新しいデータベースのパスワード</span><span class="sxs-lookup"><span data-stu-id="e2c5a-186">Jet OLEDB:New Database Password</span></span><br />
<span data-ttu-id="e2c5a-187">(DBPROP_JETOLEDB_NEWDATABASEPASSWORD)</span><span class="sxs-lookup"><span data-stu-id="e2c5a-187">(DBPROP_JETOLEDB_NEWDATABASEPASSWORD)</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-p110">このデータベースに設定する新しいパスワードを示します。元のパスワードは <strong>Jet OLEDB:Database Password</strong> に保存されます。  </span><span class="sxs-lookup"><span data-stu-id="e2c5a-p110">Indicates the new password to be set for this database. The old password is stored in <strong>Jet OLEDB:Database Password</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-190">Jet OLEDB:ODBC コマンドの時間切れ</span><span class="sxs-lookup"><span data-stu-id="e2c5a-190">Jet OLEDB:ODBC Command Time Out</span></span><br />
<span data-ttu-id="e2c5a-191">(DBPROP_JETOLEDB_ODBCCOMMANDTIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="e2c5a-191">(DBPROP_JETOLEDB_ODBCCOMMANDTIMEOUT)</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-192">Jet からのリモート ODBC クエリがタイムアウトになるまでの時間をミリ秒単位で示します。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-192">Indicates the number of milliseconds before a remote ODBC query from Jet will timeout.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-193">テーブル ロックに jet の OLEDB:Page ロック</span><span class="sxs-lookup"><span data-stu-id="e2c5a-193">Jet OLEDB:Page Locks to Table Lock</span></span><br />
<span data-ttu-id="e2c5a-194">(DBPROP_JETOLEDB_PAGELOCKSTOTABLELOCK)</span><span class="sxs-lookup"><span data-stu-id="e2c5a-194">(DBPROP_JETOLEDB_PAGELOCKSTOTABLELOCK)</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-p111">ロックからテーブル ロックへの昇格を試行するまでに、トランザクションでロックする必要があるページ数を示します。この値が 0 の場合、ロックは昇格されません。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-p111">Indicates how many pages need to be locked within a transaction before Jet attempts to promote the lock to a table lock. If this value is 0, then the lock is never promoted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-197">Jet OLEDB:Page Timeout</span><span class="sxs-lookup"><span data-stu-id="e2c5a-197">Jet OLEDB:Page Timeout</span></span><br />
<span data-ttu-id="e2c5a-198">(DBPROP_JETOLEDB_PAGETIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="e2c5a-198">(DBPROP_JETOLEDB_PAGETIMEOUT)</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-199">キャッシュが古くなっていないかどうかを確認するためにデータベース ファイルと照合するまでの待ち時間をミリ秒単位で示します。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-199">Indicates the number of milliseconds Jet will wait before checking to see if its cache is out of date with the database file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-200">Jet OLEDB:Recycle Long-Valued Pages</span><span class="sxs-lookup"><span data-stu-id="e2c5a-200">Jet OLEDB:Recycle Long-Valued Pages</span></span><br />
<span data-ttu-id="e2c5a-201">(DBPROP_JETOLEDB_RECYCLELONGVALUEPAGES)</span><span class="sxs-lookup"><span data-stu-id="e2c5a-201">(DBPROP_JETOLEDB_RECYCLELONGVALUEPAGES)</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-202">BLOB ページが解放されたときに、BLOB ページの再利用を積極的に試行するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-202">Indicates whether Jet should aggressively try to reclaim BLOB pages when they are freed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-203">Jet OLEDB:Registry Path</span><span class="sxs-lookup"><span data-stu-id="e2c5a-203">Jet OLEDB:Registry Path</span></span><br />
<span data-ttu-id="e2c5a-204">(DBPROP_JETOLEDB_REGPATH)</span><span class="sxs-lookup"><span data-stu-id="e2c5a-204">(DBPROP_JETOLEDB_REGPATH)</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-205">Jet データベース エンジンの値を格納する Windows レジストリ キーを示します。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-205">Indicates the Windows registry key that contains values for the Jet database engine.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-206">Jet OLEDB:Reset isam ドライバーの統計情報</span><span class="sxs-lookup"><span data-stu-id="e2c5a-206">Jet OLEDB:Reset ISAM Stats</span></span><br />
<span data-ttu-id="e2c5a-207">(DBPROP_JETOLEDB_RESETISAMSTATS)</span><span class="sxs-lookup"><span data-stu-id="e2c5a-207">(DBPROP_JETOLEDB_RESETISAMSTATS)</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-208">パフォーマンス情報を返した後、スキーマ <strong>Recordset</strong> DBSCHEMA_JETOLEDB_ISAMSTATS のパフォーマンス カウンターをリセットするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-208">Indicates whether the schema <strong>Recordset</strong> DBSCHEMA_JETOLEDB_ISAMSTATS should reset its performance counters after returning performance information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-209">Jet OLEDB:Shared Async Delay</span><span class="sxs-lookup"><span data-stu-id="e2c5a-209">Jet OLEDB:Shared Async Delay</span></span><br />
<span data-ttu-id="e2c5a-210">(DBPROP_JETOLEDB_SHAREDASYNCDELAY)</span><span class="sxs-lookup"><span data-stu-id="e2c5a-210">(DBPROP_JETOLEDB_SHAREDASYNCDELAY)</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-211">データベースがマルチユーザー モードで開かれている場合に、ディスクへの非同期書き込みで許容される最大遅延時間をミリ秒単位で示します。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-211">Indicates the maximum amount of time, in milliseconds, Jet can delay asynchronous writes to disk when the database is opened in multi-user mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-212">Jet OLEDB:System Database</span><span class="sxs-lookup"><span data-stu-id="e2c5a-212">Jet OLEDB:System Database</span></span><br />
<span data-ttu-id="e2c5a-213">(DBPROP_JETOLEDB_SYSDBPATH)</span><span class="sxs-lookup"><span data-stu-id="e2c5a-213">(DBPROP_JETOLEDB_SYSDBPATH)</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-214">ワークグループ情報ファイル (システム データベース) のパスおよびファイル名を示します。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-214">Indicates the path and file name for the workgroup information file (system database).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-215">Jet OLEDB:Transaction コミット ・ モード</span><span class="sxs-lookup"><span data-stu-id="e2c5a-215">Jet OLEDB:Transaction Commit Mode</span></span><br />
<span data-ttu-id="e2c5a-216">(DBPROP_JETOLEDB_TXNCOMMITMODE)</span><span class="sxs-lookup"><span data-stu-id="e2c5a-216">(DBPROP_JETOLEDB_TXNCOMMITMODE)</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-217">トランザクションがコミットされたときに、データをディスクに同期モードで書き込むか、非同期モードで書き込むかを示します。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-217">Indicates whether Jet writes data to disk synchronously or asynchronously when a transaction is committed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-218">Jet OLEDB:User Commit Sync</span><span class="sxs-lookup"><span data-stu-id="e2c5a-218">Jet OLEDB:User Commit Sync</span></span><br />
<span data-ttu-id="e2c5a-219">(DBPROP_JETOLEDB_USERCOMMITSYNC)</span><span class="sxs-lookup"><span data-stu-id="e2c5a-219">(DBPROP_JETOLEDB_USERCOMMITSYNC)</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-220">トランザクションで加えられた変更が、同期モードで書き込まれるか、非同期モードで書き込まれるかを示します。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-220">Indicates whether changes made in transactions are written in synchronous or asynchronous mode.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a><span data-ttu-id="e2c5a-221">プロバイダー固有の Recordset および Command のプロパティ</span><span class="sxs-lookup"><span data-stu-id="e2c5a-221">Provider-Specific Recordset and Command Properties</span></span>

<span data-ttu-id="e2c5a-p112">Jet プロバイダーは、プロバイダー固有の **Recordset** のプロパティと **Command** のプロパティもサポートしています。これらのプロパティは、 **Recordset** オブジェクトまたは **Command** オブジェクトの **Properties** コレクションをとおしてアクセスおよび設定します。次の表は、このプロバイダーに固有の ADO プロパティ名の一覧で、かっこ内は対応する OLE DB プロパティ名です。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-p112">The Jet provider also supports several provider-specific **Recordset** and **Command** properties. These properties are accessed and set through the **Properties** collection of the **Recordset** or **Command** object. The table lists the ADO property name and its corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e2c5a-225">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="e2c5a-225">Property Name</span></span></p></th>
<th><p><span data-ttu-id="e2c5a-226">説明</span><span class="sxs-lookup"><span data-stu-id="e2c5a-226">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-227">Jet OLEDB:Bulk トランザクション</span><span class="sxs-lookup"><span data-stu-id="e2c5a-227">Jet OLEDB:Bulk Transactions</span></span><br />
<span data-ttu-id="e2c5a-228">(DBPROP_JETOLEDB_BULKNOTRANSACTIONS)</span><span class="sxs-lookup"><span data-stu-id="e2c5a-228">(DBPROP_JETOLEDB_BULKNOTRANSACTIONS)</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-p113">SQL の一括操作が処理されるかどうかを示します。大量の一括操作は、リソース遅延のために、処理に失敗する場合があります。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-p113">Indicates whether SQL bulk operations are transacted. Large bulk operations might fail when transacted, due to resource delays.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-231">Jet OLEDB:Enable Fat カーソル</span><span class="sxs-lookup"><span data-stu-id="e2c5a-231">Jet OLEDB:Enable Fat Cursors</span></span><br />
<span data-ttu-id="e2c5a-232">(DBPROP_JETOLEDB_ENABLEFATCURSOR)</span><span class="sxs-lookup"><span data-stu-id="e2c5a-232">(DBPROP_JETOLEDB_ENABLEFATCURSOR)</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-233">リモートの行ソースのレコードセットを作成するときに、複数の行をキャッシュするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-233">Indicates whether Jet should cache multiple rows when populating a recordset for remote row sources.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-234">OLEDB:Fat jet カーソル ・ キャッシュ ・ サイズ</span><span class="sxs-lookup"><span data-stu-id="e2c5a-234">Jet OLEDB:Fat Cursor Cache Size</span></span><br />
<span data-ttu-id="e2c5a-235">(DBPROP_JETOLEDB_FATCURSORMAXROWS)</span><span class="sxs-lookup"><span data-stu-id="e2c5a-235">(DBPROP_JETOLEDB_FATCURSORMAXROWS)</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-p114">リモート データ ストアの行キャッシュを使用するときに、キャッシュする行数を示します。 <strong>Jet OLEDB:Enable Fat Cursors</strong> が True ではない場合、この値は無視されます。  </span><span class="sxs-lookup"><span data-stu-id="e2c5a-p114">Indicates the number of rows to cache when using remote data store row caching. This value is ignored unless <strong>Jet OLEDB:Enable Fat Cursors</strong> is True.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-238">Jet OLEDB: 一貫性のないです。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-238">Jet OLEDB:Inconsistent</span></span><br />
<span data-ttu-id="e2c5a-239">(DBPROP_JETOLEDB_INCONSISTENT)</span><span class="sxs-lookup"><span data-stu-id="e2c5a-239">(DBPROP_JETOLEDB_INCONSISTENT)</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-240">クエリの結果で、矛盾した更新を許容するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-240">Indicates whether query results allow inconsistent updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-241">Jet OLEDB: ロックの粒度</span><span class="sxs-lookup"><span data-stu-id="e2c5a-241">Jet OLEDB:Locking Granularity</span></span><br />
<span data-ttu-id="e2c5a-242">(DBPROP_JETOLEDB_LOCKGRANULARITY)</span><span class="sxs-lookup"><span data-stu-id="e2c5a-242">(DBPROP_JETOLEDB_LOCKGRANULARITY)</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-243">テーブルが行レベルのロックを使用して開かれているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-243">Indicates whether a table is opened using row-level locking.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-244">Jet OLEDB:ODBC パススルー ステートメント</span><span class="sxs-lookup"><span data-stu-id="e2c5a-244">Jet OLEDB:ODBC Pass-Through Statement</span></span><br />
<span data-ttu-id="e2c5a-245">(DBPROP_JETOLEDB_ODBCPASSTHROUGH)</span><span class="sxs-lookup"><span data-stu-id="e2c5a-245">(DBPROP_JETOLEDB_ODBCPASSTHROUGH)</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-246"><strong>Command</strong> オブジェクトの SQL テキストを変更せずにバックエンドに渡すかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-246">Indicates that Jet should pass the SQL text in a <strong>Command</strong> object to the back end unaltered.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-247">Jet OLEDB:Partial 一括 Ops</span><span class="sxs-lookup"><span data-stu-id="e2c5a-247">Jet OLEDB:Partial Bulk Ops</span></span><br />
<span data-ttu-id="e2c5a-248">(DBPROP_JETOLEDB_BULKPARTIAL)</span><span class="sxs-lookup"><span data-stu-id="e2c5a-248">(DBPROP_JETOLEDB_BULKPARTIAL)</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-249">SQL DML 操作に失敗したときの Jet の動作を示します。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-249">Indicates Jet's behavior when SQL DML operations fail.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-250">一括操作クエリを通じてジェット OLEDB:Pass</span><span class="sxs-lookup"><span data-stu-id="e2c5a-250">Jet OLEDB:Pass Through Query Bulk-Op</span></span><br />
<span data-ttu-id="e2c5a-251">(DBPROP_JETOLEDB_PASSTHROUGHBULKOP)</span><span class="sxs-lookup"><span data-stu-id="e2c5a-251">(DBPROP_JETOLEDB_PASSTHROUGHBULKOP)</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-252"><strong>Recordset</strong> を返さないクエリを変更せずにデータ ソースに渡すかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-252">Indicates whether queries that do not return a <strong>Recordset</strong> are passed unaltered to the data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-253">接続文字列はクエリを通じてジェット OLEDB:Pass</span><span class="sxs-lookup"><span data-stu-id="e2c5a-253">Jet OLEDB:Pass Through Query Connect String</span></span><br />
<span data-ttu-id="e2c5a-254">(DBPROP_JETOLEDB_ODBCPASSTHROUGHCONNECTSTRING)</span><span class="sxs-lookup"><span data-stu-id="e2c5a-254">(DBPROP_JETOLEDB_ODBCPASSTHROUGHCONNECTSTRING)</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-p115">リモート データ ストアへの接続に使用される Jet 接続文字列を示します。 <strong>Jet OLEDB:ODBC Pass-Through Statement</strong> が True ではない場合、この値は無視されます。  </span><span class="sxs-lookup"><span data-stu-id="e2c5a-p115">Indicates the Jet connect string used to connect to a remote data store. This value is ignored unless <strong>Jet OLEDB:ODBC Pass-Through Statement</strong> is True.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-257">Jet OLEDB: クエリの保存</span><span class="sxs-lookup"><span data-stu-id="e2c5a-257">Jet OLEDB:Stored Query</span></span><br />
<span data-ttu-id="e2c5a-258">(DBPROP_JETOLEDB_STOREDQUERY)</span><span class="sxs-lookup"><span data-stu-id="e2c5a-258">(DBPROP_JETOLEDB_STOREDQUERY)</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-259">コマンド テキストを、SQL コマンドではなく、ストアド クエリとして解釈するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-259">Indicates whether the command text should be interpreted as a stored query instead of an SQL command.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-260">Jet OLEDB: 一連のルールを検証</span><span class="sxs-lookup"><span data-stu-id="e2c5a-260">Jet OLEDB:Validate Rules On Set</span></span><br />
<span data-ttu-id="e2c5a-261">(DBPROP_JETOLEDB_VALIDATEONSET)</span><span class="sxs-lookup"><span data-stu-id="e2c5a-261">(DBPROP_JETOLEDB_VALIDATEONSET)</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-262">列データを設定するとき、または変更をデータベースにコミットするときに、Jet 入力規則を評価するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-262">Indicates whether the Jet validation rules are evaluated when column data is set or when the changes are committed to the database.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e2c5a-p116">既定では、OLE DB Provider for Microsoft Jet は Microsoft Jet データベースを読み取り/書き込み可能モードで開きます。データベースを読み取り専用モードで開くには、ADO [Connection](mode-property-ado.md) オブジェクトの **Mode** プロパティを **adModeRead** に設定します。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-p116">By default, the OLE DB Provider for Microsoft Jet opens Microsoft Jet databases in read/write mode. To open a database in read-only mode, set the [Mode](mode-property-ado.md) property on the ADO **Connection** object to **adModeRead**.</span></span>

## <a name="command-object-usage"></a><span data-ttu-id="e2c5a-265">Command オブジェクトの使用方法</span><span class="sxs-lookup"><span data-stu-id="e2c5a-265">Command Object Usage</span></span>

<span data-ttu-id="e2c5a-p117">[Command](command-object-ado.md) オブジェクトのコマンド テキストでは、Microsoft Jet SQL 言語を使用します。コマンド テキストでは、行を返すクエリ、アクション クエリ、およびテーブル名を指定できますが、ストアド プロシージャはサポートされていないので指定できません。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-p117">Command text in the [Command](command-object-ado.md) object uses the Microsoft Jet SQL dialect. You can specify row-returning queries, action queries, and table names in the command text; however, stored procedures are not supported and should not be specified.</span></span>

## <a name="recordset-behavior"></a><span data-ttu-id="e2c5a-268">Recordset の動作</span><span class="sxs-lookup"><span data-stu-id="e2c5a-268">Recordset Behavior</span></span>

<span data-ttu-id="e2c5a-p118">Microsoft Jet データベース エンジンは動的カーソルをサポートしていません。したがって、OLE DB Provider for Microsoft Jet は、カーソルの種類 **adLockDynamic** をサポートしていません。動的カーソルが要求された場合、プロバイダーはキーセット カーソルを返し、[CursorType](cursortype-property-ado.md) プロパティを、返された [Recordset](recordset-object-ado.md) の種類を示す値に設定し直します。また、更新可能な **Recordset** が要求された場合 (**LockType** が **adLockOptimistic**、**adLockBatchOptimistic**、または **adLockPessimistic**)、プロバイダーはキーセット カーソルを返し、**CursorType** プロパティを設定し直します。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-p118">The Microsoft Jet database engine does not support dynamic cursors. Therefore, the OLE DB Provider for Microsoft Jet does not support the **adLockDynamic** cursor type. When a dynamic cursor is requested, the provider will return a keyset cursor and reset the [CursorType](cursortype-property-ado.md) property to indicate the type of [Recordset](recordset-object-ado.md) returned. Further, if an updatable **Recordset** is requested (**LockType** is **adLockOptimistic**, **adLockBatchOptimistic**, or **adLockPessimistic**) the provider will also return a keyset cursor and reset the **CursorType** property.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="e2c5a-273">動的プロパティ</span><span class="sxs-lookup"><span data-stu-id="e2c5a-273">Dynamic Properties</span></span>

<span data-ttu-id="e2c5a-274">OLE DB Provider for Microsoft Jet は、開かれていない **Connection** オブジェクト、 [Recordset](connection-object-ado.md) オブジェクト、および [Command](recordset-object-ado.md) オブジェクトの [Properties](command-object-ado.md) コレクションに動的プロパティを挿入します。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-274">The OLE DB Provider for Microsoft Jet inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="e2c5a-p119">以下の表は、各動的プロパティの ADO 名と OLE DB 名の対応表です。「OLE DB プログラマ リファレンス」では、「説明」欄に ADO プロパティ名が示されています。プロパティの詳細については、「OLE DB プログラマ リファレンス」を参照してください。OLE DB プロパティ名をキーワードとして検索するか、「付録 C: プロパティ表」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-p119">The tables below are a cross-index of the ADO and OLE DB names for each dynamic property. The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description." You can find more information about these properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="e2c5a-279">Connection の動的プロパティ</span><span class="sxs-lookup"><span data-stu-id="e2c5a-279">Connection Dynamic Properties</span></span>

<span data-ttu-id="e2c5a-280">次に示すプロパティが **Connection** オブジェクトの **Properties** コレクションに追加されます。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-280">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e2c5a-281">ADO プロパティ名</span><span class="sxs-lookup"><span data-stu-id="e2c5a-281">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="e2c5a-282">OLE DB プロパティ名</span><span class="sxs-lookup"><span data-stu-id="e2c5a-282">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-283">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="e2c5a-283">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-284">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="e2c5a-284">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-285">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="e2c5a-285">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-286">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="e2c5a-286">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-287">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="e2c5a-287">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-288">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="e2c5a-288">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-289">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="e2c5a-289">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-290">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="e2c5a-290">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-291">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="e2c5a-291">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-292">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="e2c5a-292">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-293">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="e2c5a-293">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-294">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="e2c5a-294">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-295">Column Definition</span><span class="sxs-lookup"><span data-stu-id="e2c5a-295">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-296">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="e2c5a-296">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-297">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="e2c5a-297">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-298">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="e2c5a-298">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-299">Data Source</span><span class="sxs-lookup"><span data-stu-id="e2c5a-299">Data Source</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-300">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="e2c5a-300">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-301">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="e2c5a-301">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-302">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="e2c5a-302">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-303">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="e2c5a-303">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-304">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="e2c5a-304">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-305">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="e2c5a-305">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-306">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="e2c5a-306">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-307">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="e2c5a-307">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-308">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="e2c5a-308">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-309">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="e2c5a-309">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-310">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="e2c5a-310">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-311">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="e2c5a-311">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-312">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="e2c5a-312">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-313">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="e2c5a-313">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-314">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="e2c5a-314">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-315">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="e2c5a-315">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-316">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="e2c5a-316">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-317">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="e2c5a-317">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-318">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="e2c5a-318">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-319">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="e2c5a-319">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-320">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="e2c5a-320">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-321">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="e2c5a-321">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-322">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="e2c5a-322">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-323">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="e2c5a-323">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-324">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="e2c5a-324">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-325">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="e2c5a-325">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-326">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="e2c5a-326">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-327">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="e2c5a-327">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-328">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="e2c5a-328">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-329">Mode</span><span class="sxs-lookup"><span data-stu-id="e2c5a-329">Mode</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-330">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="e2c5a-330">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-331">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="e2c5a-331">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-332">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="e2c5a-332">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-333">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="e2c5a-333">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-334">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="e2c5a-334">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-335">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="e2c5a-335">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-336">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="e2c5a-336">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-337">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="e2c5a-337">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-338">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="e2c5a-338">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-339">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="e2c5a-339">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-340">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="e2c5a-340">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-341">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="e2c5a-341">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-342">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="e2c5a-342">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-343">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="e2c5a-343">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-344">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="e2c5a-344">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-345">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="e2c5a-345">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-346">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="e2c5a-346">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-347">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="e2c5a-347">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-348">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="e2c5a-348">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-349">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="e2c5a-349">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-350">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="e2c5a-350">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-351">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="e2c5a-351">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-352">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="e2c5a-352">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-353">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="e2c5a-353">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-354">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="e2c5a-354">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-355">Password</span><span class="sxs-lookup"><span data-stu-id="e2c5a-355">Password</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-356">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="e2c5a-356">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-357">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="e2c5a-357">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-358">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="e2c5a-358">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-359">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="e2c5a-359">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-360">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="e2c5a-360">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-361">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="e2c5a-361">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-362">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="e2c5a-362">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-363">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="e2c5a-363">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-364">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="e2c5a-364">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-365">Prompt</span><span class="sxs-lookup"><span data-stu-id="e2c5a-365">Prompt</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-366">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="e2c5a-366">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-367">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="e2c5a-367">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-368">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="e2c5a-368">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-369">Provider Name</span><span class="sxs-lookup"><span data-stu-id="e2c5a-369">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-370">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="e2c5a-370">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-371">Provider Version</span><span class="sxs-lookup"><span data-stu-id="e2c5a-371">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-372">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="e2c5a-372">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-373">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="e2c5a-373">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-374">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="e2c5a-374">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-375">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="e2c5a-375">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-376">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="e2c5a-376">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-377">Schema Term</span><span class="sxs-lookup"><span data-stu-id="e2c5a-377">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-378">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="e2c5a-378">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-379">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="e2c5a-379">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-380">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="e2c5a-380">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-381">SQL Support</span><span class="sxs-lookup"><span data-stu-id="e2c5a-381">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-382">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="e2c5a-382">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-383">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="e2c5a-383">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-384">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="e2c5a-384">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-385">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="e2c5a-385">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-386">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="e2c5a-386">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-387">Table Term</span><span class="sxs-lookup"><span data-stu-id="e2c5a-387">Table Term</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-388">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="e2c5a-388">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-389">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="e2c5a-389">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-390">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="e2c5a-390">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-391">User ID</span><span class="sxs-lookup"><span data-stu-id="e2c5a-391">User ID</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-392">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="e2c5a-392">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-393">User Name</span><span class="sxs-lookup"><span data-stu-id="e2c5a-393">User Name</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-394">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="e2c5a-394">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-395">Window Handle</span><span class="sxs-lookup"><span data-stu-id="e2c5a-395">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-396">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="e2c5a-396">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="e2c5a-397">Recordset の動的プロパティ</span><span class="sxs-lookup"><span data-stu-id="e2c5a-397">Recordset Dynamic Properties</span></span>

<span data-ttu-id="e2c5a-398">次に示すプロパティが **Recordset** オブジェクトの **Properties** コレクションに追加されます。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-398">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e2c5a-399">ADO プロパティ名</span><span class="sxs-lookup"><span data-stu-id="e2c5a-399">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="e2c5a-400">OLE DB プロパティ名</span><span class="sxs-lookup"><span data-stu-id="e2c5a-400">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-401">Access Order</span><span class="sxs-lookup"><span data-stu-id="e2c5a-401">Access Order</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-402">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="e2c5a-402">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-403">Append-Only Rowset</span><span class="sxs-lookup"><span data-stu-id="e2c5a-403">Append-Only Rowset</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-404">DBPROP_APPENDONLY</span><span class="sxs-lookup"><span data-stu-id="e2c5a-404">DBPROP_APPENDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-405">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="e2c5a-405">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-406">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="e2c5a-406">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-407">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="e2c5a-407">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-408">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="e2c5a-408">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-409">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="e2c5a-409">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-410">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="e2c5a-410">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-411">Bookmarks Ordered</span><span class="sxs-lookup"><span data-stu-id="e2c5a-411">Bookmarks Ordered</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-412">DBPROP_ORDEREDBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="e2c5a-412">DBPROP_ORDEREDBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-413">Cache Deferred Columns</span><span class="sxs-lookup"><span data-stu-id="e2c5a-413">Cache Deferred Columns</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-414">DBPROP_CACHEDEFERRED</span><span class="sxs-lookup"><span data-stu-id="e2c5a-414">DBPROP_CACHEDEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-415">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="e2c5a-415">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-416">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="e2c5a-416">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-417">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="e2c5a-417">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-418">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="e2c5a-418">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-419">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="e2c5a-419">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-420">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="e2c5a-420">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-421">Column Writable</span><span class="sxs-lookup"><span data-stu-id="e2c5a-421">Column Writable</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-422">DBPROP_MAYWRITECOLUMN</span><span class="sxs-lookup"><span data-stu-id="e2c5a-422">DBPROP_MAYWRITECOLUMN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-423">Defer Column</span><span class="sxs-lookup"><span data-stu-id="e2c5a-423">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-424">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="e2c5a-424">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-425">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="e2c5a-425">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-426">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="e2c5a-426">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-427">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="e2c5a-427">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-428">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="e2c5a-428">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-429">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="e2c5a-429">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-430">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="e2c5a-430">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-431">IAccessor</span><span class="sxs-lookup"><span data-stu-id="e2c5a-431">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-432">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="e2c5a-432">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-433">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="e2c5a-433">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-434">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="e2c5a-434">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-435">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="e2c5a-435">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-436">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="e2c5a-436">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-437">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="e2c5a-437">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-438">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="e2c5a-438">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-439">IConvertType</span><span class="sxs-lookup"><span data-stu-id="e2c5a-439">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-440">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="e2c5a-440">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-441">ILockBytes</span><span class="sxs-lookup"><span data-stu-id="e2c5a-441">ILockBytes</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-442">DBPROP_ILockBytes</span><span class="sxs-lookup"><span data-stu-id="e2c5a-442">DBPROP_ILockBytes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-443">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="e2c5a-443">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-444">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="e2c5a-444">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-445">IRowset</span><span class="sxs-lookup"><span data-stu-id="e2c5a-445">IRowset</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-446">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="e2c5a-446">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-447">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="e2c5a-447">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-448">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="e2c5a-448">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-449">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="e2c5a-449">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-450">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="e2c5a-450">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-451">IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="e2c5a-451">IRowsetIndex</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-452">DBPROP_IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="e2c5a-452">DBPROP_IRowsetIndex</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-453">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="e2c5a-453">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-454">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="e2c5a-454">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-455">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="e2c5a-455">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-456">DBPROP_IRowsestLocate</span><span class="sxs-lookup"><span data-stu-id="e2c5a-456">DBPROP_IRowsestLocate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-457">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="e2c5a-457">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-458">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="e2c5a-458">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-459">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="e2c5a-459">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-460">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="e2c5a-460">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-461">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="e2c5a-461">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-462">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="e2c5a-462">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-463">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="e2c5a-463">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-464">IStorage</span><span class="sxs-lookup"><span data-stu-id="e2c5a-464">IStorage</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-465">DBPROP_IStorage</span><span class="sxs-lookup"><span data-stu-id="e2c5a-465">DBPROP_IStorage</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-466">IStream</span><span class="sxs-lookup"><span data-stu-id="e2c5a-466">IStream</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-467">DBPROP_IStream</span><span class="sxs-lookup"><span data-stu-id="e2c5a-467">DBPROP_IStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-468">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="e2c5a-468">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-469">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="e2c5a-469">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-470">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="e2c5a-470">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-471">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="e2c5a-471">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-472">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="e2c5a-472">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-473">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="e2c5a-473">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-474">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="e2c5a-474">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-475">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="e2c5a-475">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-476">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="e2c5a-476">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-477">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="e2c5a-477">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-478">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="e2c5a-478">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-479">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="e2c5a-479">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-480">Memory Usage</span><span class="sxs-lookup"><span data-stu-id="e2c5a-480">Memory Usage</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-481">DBPROP_MEMORYUSAGE</span><span class="sxs-lookup"><span data-stu-id="e2c5a-481">DBPROP_MEMORYUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-482">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="e2c5a-482">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-483">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="e2c5a-483">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-484">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="e2c5a-484">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-485">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="e2c5a-485">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-486">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="e2c5a-486">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-487">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="e2c5a-487">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-488">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="e2c5a-488">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-489">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="e2c5a-489">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-490">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="e2c5a-490">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-491">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="e2c5a-491">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-492">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="e2c5a-492">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-493">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="e2c5a-493">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-494">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="e2c5a-494">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-495">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="e2c5a-495">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-496">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="e2c5a-496">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-497">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="e2c5a-497">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-498">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="e2c5a-498">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-499">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="e2c5a-499">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-500">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="e2c5a-500">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-501">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="e2c5a-501">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-502">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="e2c5a-502">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-503">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="e2c5a-503">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-504">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="e2c5a-504">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-505">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="e2c5a-505">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-506">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="e2c5a-506">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-507">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="e2c5a-507">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-508">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="e2c5a-508">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-509">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="e2c5a-509">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-510">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="e2c5a-510">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-511">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="e2c5a-511">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-512">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="e2c5a-512">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-513">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="e2c5a-513">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-514">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="e2c5a-514">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-515">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="e2c5a-515">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-516">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="e2c5a-516">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-517">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="e2c5a-517">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-518">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="e2c5a-518">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-519">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="e2c5a-519">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-520">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="e2c5a-520">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-521">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="e2c5a-521">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-522">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="e2c5a-522">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-523">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="e2c5a-523">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-524">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="e2c5a-524">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-525">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="e2c5a-525">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-526">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="e2c5a-526">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-527">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="e2c5a-527">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-528">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="e2c5a-528">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-529">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="e2c5a-529">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-530">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="e2c5a-530">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-531">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="e2c5a-531">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-532">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="e2c5a-532">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-533">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="e2c5a-533">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-534">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="e2c5a-534">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-535">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="e2c5a-535">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-536">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="e2c5a-536">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-537">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="e2c5a-537">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-538">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="e2c5a-538">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-539">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="e2c5a-539">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-540">Updatability</span><span class="sxs-lookup"><span data-stu-id="e2c5a-540">Updatability</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-541">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="e2c5a-541">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-542">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="e2c5a-542">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-543">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="e2c5a-543">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="e2c5a-544">Command の動的プロパティ</span><span class="sxs-lookup"><span data-stu-id="e2c5a-544">Command Dynamic Properties</span></span>

<span data-ttu-id="e2c5a-545">次に示すプロパティが **Command** オブジェクトの **Properties** コレクションに追加されます。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-545">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e2c5a-546">ADO プロパティ名</span><span class="sxs-lookup"><span data-stu-id="e2c5a-546">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="e2c5a-547">OLE DB プロパティ名</span><span class="sxs-lookup"><span data-stu-id="e2c5a-547">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-548">Access Order</span><span class="sxs-lookup"><span data-stu-id="e2c5a-548">Access Order</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-549">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="e2c5a-549">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-550">Append-Only Rowset</span><span class="sxs-lookup"><span data-stu-id="e2c5a-550">Append-Only Rowset</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-551">DBPROP_APPENDONLY</span><span class="sxs-lookup"><span data-stu-id="e2c5a-551">DBPROP_APPENDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-552">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="e2c5a-552">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-553">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="e2c5a-553">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-554">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="e2c5a-554">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-555">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="e2c5a-555">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-556">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="e2c5a-556">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-557">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="e2c5a-557">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-558">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="e2c5a-558">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-559">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="e2c5a-559">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-560">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="e2c5a-560">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-561">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="e2c5a-561">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-562">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="e2c5a-562">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-563">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="e2c5a-563">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-564">Defer Column</span><span class="sxs-lookup"><span data-stu-id="e2c5a-564">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-565">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="e2c5a-565">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-566">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="e2c5a-566">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-567">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="e2c5a-567">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-568">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="e2c5a-568">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-569">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="e2c5a-569">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-570">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="e2c5a-570">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-571">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="e2c5a-571">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-572">IAccessor</span><span class="sxs-lookup"><span data-stu-id="e2c5a-572">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-573">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="e2c5a-573">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-574">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="e2c5a-574">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-575">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="e2c5a-575">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-576">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="e2c5a-576">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-577">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="e2c5a-577">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-578">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="e2c5a-578">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-579">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="e2c5a-579">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-580">IConvertType</span><span class="sxs-lookup"><span data-stu-id="e2c5a-580">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-581">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="e2c5a-581">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-582">ILockBytes</span><span class="sxs-lookup"><span data-stu-id="e2c5a-582">ILockBytes</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-583">DBPROP_ILockBytes</span><span class="sxs-lookup"><span data-stu-id="e2c5a-583">DBPROP_ILockBytes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-584">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="e2c5a-584">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-585">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="e2c5a-585">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-586">IRowset</span><span class="sxs-lookup"><span data-stu-id="e2c5a-586">IRowset</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-587">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="e2c5a-587">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-588">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="e2c5a-588">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-589">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="e2c5a-589">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-590">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="e2c5a-590">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-591">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="e2c5a-591">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-592">IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="e2c5a-592">IRowsetIndex</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-593">DBPROP_IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="e2c5a-593">DBPROP_IRowsetIndex</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-594">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="e2c5a-594">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-595">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="e2c5a-595">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-596">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="e2c5a-596">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-597">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="e2c5a-597">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-598">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="e2c5a-598">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-599">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="e2c5a-599">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-600">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="e2c5a-600">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-601">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="e2c5a-601">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-602">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="e2c5a-602">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-603">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="e2c5a-603">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-604">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="e2c5a-604">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-605">IStorage</span><span class="sxs-lookup"><span data-stu-id="e2c5a-605">IStorage</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-606">DBPROP_IStorage</span><span class="sxs-lookup"><span data-stu-id="e2c5a-606">DBPROP_IStorage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-607">IStream</span><span class="sxs-lookup"><span data-stu-id="e2c5a-607">IStream</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-608">DBPROP_IStream</span><span class="sxs-lookup"><span data-stu-id="e2c5a-608">DBPROP_IStream</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-609">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="e2c5a-609">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-610">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="e2c5a-610">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-611">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="e2c5a-611">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-612">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="e2c5a-612">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-613">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="e2c5a-613">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-614">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="e2c5a-614">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-615">Lock Mode</span><span class="sxs-lookup"><span data-stu-id="e2c5a-615">Lock Mode</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-616">DBPROP_LOCKMODE</span><span class="sxs-lookup"><span data-stu-id="e2c5a-616">DBPROP_LOCKMODE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-617">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="e2c5a-617">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-618">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="e2c5a-618">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-619">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="e2c5a-619">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-620">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="e2c5a-620">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-621">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="e2c5a-621">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-622">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="e2c5a-622">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-623">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="e2c5a-623">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-624">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="e2c5a-624">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-625">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="e2c5a-625">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-626">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="e2c5a-626">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-627">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="e2c5a-627">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-628">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="e2c5a-628">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-629">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="e2c5a-629">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-630">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="e2c5a-630">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-631">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="e2c5a-631">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-632">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="e2c5a-632">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-633">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="e2c5a-633">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-634">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="e2c5a-634">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-635">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="e2c5a-635">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-636">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="e2c5a-636">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-637">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="e2c5a-637">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-638">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="e2c5a-638">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-639">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="e2c5a-639">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-640">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="e2c5a-640">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-641">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="e2c5a-641">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-642">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="e2c5a-642">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-643">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="e2c5a-643">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-644">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="e2c5a-644">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-645">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="e2c5a-645">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-646">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="e2c5a-646">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-647">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="e2c5a-647">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-648">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="e2c5a-648">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-649">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="e2c5a-649">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-650">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="e2c5a-650">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-651">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="e2c5a-651">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-652">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="e2c5a-652">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-653">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="e2c5a-653">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-654">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="e2c5a-654">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-655">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="e2c5a-655">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-656">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="e2c5a-656">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-657">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="e2c5a-657">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-658">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="e2c5a-658">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-659">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="e2c5a-659">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-660">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="e2c5a-660">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-661">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="e2c5a-661">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-662">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="e2c5a-662">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-663">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="e2c5a-663">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-664">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="e2c5a-664">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-665">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="e2c5a-665">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-666">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="e2c5a-666">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-667">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="e2c5a-667">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-668">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="e2c5a-668">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-669">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="e2c5a-669">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-670">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="e2c5a-670">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-671">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="e2c5a-671">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-672">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="e2c5a-672">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-673">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="e2c5a-673">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-674">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="e2c5a-674">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-675">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="e2c5a-675">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-676">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="e2c5a-676">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-677">Server Data on Insert</span><span class="sxs-lookup"><span data-stu-id="e2c5a-677">Server Data on Insert</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-678">DBPROP_SERVERDATAONINSERT</span><span class="sxs-lookup"><span data-stu-id="e2c5a-678">DBPROP_SERVERDATAONINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-679">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="e2c5a-679">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-680">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="e2c5a-680">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-681">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="e2c5a-681">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-682">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="e2c5a-682">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2c5a-683">Updatability</span><span class="sxs-lookup"><span data-stu-id="e2c5a-683">Updatability</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-684">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="e2c5a-684">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2c5a-685">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="e2c5a-685">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="e2c5a-686">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="e2c5a-686">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="e2c5a-687">関連項目</span><span class="sxs-lookup"><span data-stu-id="e2c5a-687">See also</span></span>

<span data-ttu-id="e2c5a-688">特定の実装の詳細については、Microsoft Jet の OLE DB プロバイダーの機能については、MDAC SDK のドキュメントを Microsoft Jet の OLE DB プロバイダーを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e2c5a-688">For specific implementation details and functional information about the OLE DB Provider for Microsoft Jet, consult the OLE DB Provider for Microsoft Jet documentation in the MDAC SDK.</span></span>

