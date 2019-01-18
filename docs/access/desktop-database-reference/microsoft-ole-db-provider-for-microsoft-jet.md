---
title: Microsoft OLE DB Provider for Microsoft Jet
TOCTitle: Microsoft OLE DB Provider for Microsoft Jet
ms:assetid: 4a210d72-8c90-aa7c-4621-1a555a30a2d2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249228(v=office.15)
ms:contentKeyID: 48544660
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b4f1c46b390e1f059e57f3b7a70fc667da4b09b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712842"
---
# <a name="microsoft-ole-db-provider-for-microsoft-jet"></a><span data-ttu-id="48f77-102">Microsoft OLE DB Provider for Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="48f77-102">Microsoft OLE DB Provider for Microsoft Jet</span></span>

<span data-ttu-id="48f77-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="48f77-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="48f77-104">OLE DB Provider for Microsoft Jet を使用すると、ADO から Microsoft Jet データベースにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="48f77-104">The OLE DB Provider for Microsoft Jet allows ADO to access Microsoft Jet databases.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="48f77-105">接続文字列のパラメーター</span><span class="sxs-lookup"><span data-stu-id="48f77-105">Connection String Parameters</span></span>

<span data-ttu-id="48f77-106">このプロバイダーに接続するには、*ConnectionString* プロパティの [Provider](connectionstring-property-ado.md) 引数を次のように設定します。</span><span class="sxs-lookup"><span data-stu-id="48f77-106">To connect to this provider, set the *Provider* argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
Microsoft.Jet.OLEDB.4.0 
```

<span data-ttu-id="48f77-107">[Provider](provider-property-ado.md) プロパティを取得した場合も、この文字列が返されます。</span><span class="sxs-lookup"><span data-stu-id="48f77-107">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="48f77-108">標準的な接続文字列</span><span class="sxs-lookup"><span data-stu-id="48f77-108">Typical Connection String</span></span>

<span data-ttu-id="48f77-109">このプロバイダーの標準的な接続文字列を次に示します。</span><span class="sxs-lookup"><span data-stu-id="48f77-109">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=Microsoft.Jet.OLEDB.4.0;Data Source=databaseName;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="48f77-110">この文字列は、次に示すキーワードで構成されています。</span><span class="sxs-lookup"><span data-stu-id="48f77-110">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="48f77-111">キーワード</span><span class="sxs-lookup"><span data-stu-id="48f77-111">Keyword</span></span></p></th>
<th><p><span data-ttu-id="48f77-112">説明</span><span class="sxs-lookup"><span data-stu-id="48f77-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="48f77-113"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="48f77-113"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="48f77-114">OLE DB Provider for Microsoft Jet を指定します。</span><span class="sxs-lookup"><span data-stu-id="48f77-114">Specifies the OLE DB Provider for Microsoft Jet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-115"><strong>Data Source</strong></span><span class="sxs-lookup"><span data-stu-id="48f77-115"><strong>Data Source</strong></span></span></p></td>
<td><p><span data-ttu-id="48f77-116">データベースのパスおよびファイル名を指定します (例: c:\Northwind.mdb)。</span><span class="sxs-lookup"><span data-stu-id="48f77-116">Specifies the database path and file name (for example, c:\Northwind.mdb).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-117"><strong>User ID</strong></span><span class="sxs-lookup"><span data-stu-id="48f77-117"><strong>User ID</strong></span></span></p></td>
<td><p><span data-ttu-id="48f77-118">ユーザー名を指定します。</span><span class="sxs-lookup"><span data-stu-id="48f77-118">Specifies the user name.</span></span> <span data-ttu-id="48f77-119">このキーワードを指定しない場合、文字列では、&quot;管理&quot;、既定で使用します。</span><span class="sxs-lookup"><span data-stu-id="48f77-119">If this keyword is not specified, the string, &quot;admin&quot;, is used by default.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-120"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="48f77-120"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="48f77-121">ユーザー パスワードを指定します。</span><span class="sxs-lookup"><span data-stu-id="48f77-121">Specifies the user password.</span></span> <span data-ttu-id="48f77-122">このキーワードを指定しない場合、空の文字列 (&quot;&quot;)、既定で使用します。</span><span class="sxs-lookup"><span data-stu-id="48f77-122">If this keyword is not specified, the empty string (&quot;&quot;), is used by default.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a><span data-ttu-id="48f77-123">プロバイダー固有の接続パラメーター</span><span class="sxs-lookup"><span data-stu-id="48f77-123">Provider-Specific Connection Parameters</span></span>

<span data-ttu-id="48f77-p103">OLE DB Provider for Microsoft Jet は、ADO で定義されたプロパティに加えて、プロバイダー固有の動的プロパティをサポートしています。プロバイダー固有の接続パラメーターは他のすべての **Connection** パラメーターと同様に、 **Connection** オブジェクトの **Properties** コレクションで設定するか、接続文字列の一部として設定することができます。</span><span class="sxs-lookup"><span data-stu-id="48f77-p103">The OLE DB Provider for Microsoft Jet supports several provider-specific dynamic properties in addition to those defined by ADO. As with all other **Connection** parameters, they can be set via the **Connection** object's **Properties** collection or as part of the connection string.</span></span>

<span data-ttu-id="48f77-126">次の表は、これらのプロパティの一覧で、かっこ内は対応する OLE DB プロパティ名です。</span><span class="sxs-lookup"><span data-stu-id="48f77-126">The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="48f77-127">パラメーター</span><span class="sxs-lookup"><span data-stu-id="48f77-127">Parameter</span></span></p></th>
<th><p><span data-ttu-id="48f77-128">説明</span><span class="sxs-lookup"><span data-stu-id="48f77-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="48f77-129">Jet OLEDB:Compact 再生されるスペースの量</span><span class="sxs-lookup"><span data-stu-id="48f77-129">Jet OLEDB:Compact Reclaimed Space Amount</span></span><br />
<span data-ttu-id="48f77-130">(DBPROP_JETOLEDB_COMPACTFREESPACESIZE)</span><span class="sxs-lookup"><span data-stu-id="48f77-130">(DBPROP_JETOLEDB_COMPACTFREESPACESIZE)</span></span></p></td>
<td><p><span data-ttu-id="48f77-p104">データベースの最適化によって増やすことができる空き領域の推定量をバイト単位で示します。この値は、データベース接続が確立した後でのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="48f77-p104">Indicates an estimate of the amount of space, in bytes, that can be reclaimed by compacting the database. This value is only valid after a database connection has been established.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-133">Jet OLEDB:Connection コントロール</span><span class="sxs-lookup"><span data-stu-id="48f77-133">Jet OLEDB:Connection Control</span></span><br />
<span data-ttu-id="48f77-134">(DBPROP_JETOLEDB_CONNECTIONCONTROL)</span><span class="sxs-lookup"><span data-stu-id="48f77-134">(DBPROP_JETOLEDB_CONNECTIONCONTROL)</span></span></p></td>
<td><p><span data-ttu-id="48f77-135">ユーザーがデータベースに接続できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="48f77-135">Indicates whether users can connect to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-136">Jet OLEDB: システム データベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="48f77-136">Jet OLEDB:Create System Database</span></span><br />
<span data-ttu-id="48f77-137">(DBPROP_JETOLEDB_CREATESYSTEMDATABASE)</span><span class="sxs-lookup"><span data-stu-id="48f77-137">(DBPROP_JETOLEDB_CREATESYSTEMDATABASE)</span></span></p></td>
<td><p><span data-ttu-id="48f77-138">新規データ ソースの作成時にシステム データベースを作成するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="48f77-138">Indicates whether a system database should be created when creating a new data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-139">Jet OLEDB:Database ロック モード</span><span class="sxs-lookup"><span data-stu-id="48f77-139">Jet OLEDB:Database Locking Mode</span></span><br />
<span data-ttu-id="48f77-140">(DBPROP_JETOLEDB_DATABASELOCKMODE)</span><span class="sxs-lookup"><span data-stu-id="48f77-140">(DBPROP_JETOLEDB_DATABASELOCKMODE)</span></span></p></td>
<td><p><span data-ttu-id="48f77-p105">このデータベースのロック モードを示します。最初にデータベースを開いたユーザーが、データベースを開いているときに使用されるモードを決定します。</span><span class="sxs-lookup"><span data-stu-id="48f77-p105">Indicates the locking mode for this database. The first user to open the database determines the mode used while the database is open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-143">Jet OLEDB:Database Password</span><span class="sxs-lookup"><span data-stu-id="48f77-143">Jet OLEDB:Database Password</span></span><br />
<span data-ttu-id="48f77-144">(DBPROP_JETOLEDB_DATABASEPASSWORD)</span><span class="sxs-lookup"><span data-stu-id="48f77-144">(DBPROP_JETOLEDB_DATABASEPASSWORD)</span></span></p></td>
<td><p><span data-ttu-id="48f77-145">データベースのパスワードを示します。</span><span class="sxs-lookup"><span data-stu-id="48f77-145">Indicates the database password.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-146">Jet OLEDB:Don't Copy Locale on Compact</span><span class="sxs-lookup"><span data-stu-id="48f77-146">Jet OLEDB:Don't Copy Locale on Compact</span></span><br />
<span data-ttu-id="48f77-147">(DBPROP_JETOLEDB_COMPACT_DONTCOPYLOCALE)</span><span class="sxs-lookup"><span data-stu-id="48f77-147">(DBPROP_JETOLEDB_COMPACT_DONTCOPYLOCALE)</span></span></p></td>
<td><p><span data-ttu-id="48f77-148">データベースを最適化するときにロケール情報をコピーするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="48f77-148">Indicates whether Jet should copy locale information when compacting a database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-149">Jet OLEDB:Encrypt Database</span><span class="sxs-lookup"><span data-stu-id="48f77-149">Jet OLEDB:Encrypt Database</span></span><br />
<span data-ttu-id="48f77-150">(DBPROP_JETOLEDB_ENCRYPTDATABASE)</span><span class="sxs-lookup"><span data-stu-id="48f77-150">(DBPROP_JETOLEDB_ENCRYPTDATABASE)</span></span></p></td>
<td><p><span data-ttu-id="48f77-p106">最適化したデータベースを暗号化するかどうかを示します。このプロパティを設定しない場合、元のデータベースが暗号化されている場合は、最適化したデータベースも暗号化されます。</span><span class="sxs-lookup"><span data-stu-id="48f77-p106">Indicates whether a compacted database should be encrypted. If this property is not set, the compacted database will be encrypted if the original database was also encrypted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-153">Jet OLEDB:Engine Type</span><span class="sxs-lookup"><span data-stu-id="48f77-153">Jet OLEDB:Engine Type</span></span><br />
<span data-ttu-id="48f77-154">(DBPROP_JETOLEDB_ENGINE)</span><span class="sxs-lookup"><span data-stu-id="48f77-154">(DBPROP_JETOLEDB_ENGINE)</span></span></p></td>
<td><p><span data-ttu-id="48f77-155">現在のデータ ストアにアクセスするために使用される記憶域エンジンを示します。</span><span class="sxs-lookup"><span data-stu-id="48f77-155">Indicates the storage engine used to access the current data store.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-156">Jet OLEDB:Exclusive Async Delay</span><span class="sxs-lookup"><span data-stu-id="48f77-156">Jet OLEDB:Exclusive Async Delay</span></span><br />
<span data-ttu-id="48f77-157">(DBPROP_JETOLEDB_EXCLUSIVEASYNCDELAY)</span><span class="sxs-lookup"><span data-stu-id="48f77-157">(DBPROP_JETOLEDB_EXCLUSIVEASYNCDELAY)</span></span></p></td>
<td><p><span data-ttu-id="48f77-p107">データベースが排他的に開かれている場合に、ディスクへの非同期書き込みで許容される最大遅延時間をミリ秒単位で示します。 <strong>Jet OLEDB:Flush Transaction Timeout</strong> が 0 に設定されていない場合、このプロパティは無視されます。  </span><span class="sxs-lookup"><span data-stu-id="48f77-p107">Indicates the maximum length of time, in milliseconds, that Jet can delay asynchronous writes to disk when the database is opened exclusively. This property is ignored unless <strong>Jet OLEDB:Flush Transaction Timeout</strong> is set to 0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-160">Jet OLEDB:Flush Transaction Timeout</span><span class="sxs-lookup"><span data-stu-id="48f77-160">Jet OLEDB:Flush Transaction Timeout</span></span><br />
<span data-ttu-id="48f77-161">(DBPROP_JETOLEDB_FLUSHTRANSACTIONTIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="48f77-161">(DBPROP_JETOLEDB_FLUSHTRANSACTIONTIMEOUT)</span></span></p></td>
<td><p><span data-ttu-id="48f77-p108">非同期書き込みのためにキャッシュに保存されたデータが実際にディスクに書き込まれるまでの待ち時間を示します。この設定は、 <strong>Jet OLEDB:Shared Async Delay</strong> および <strong>Jet OLEDB:Exclusive Async Delay</strong> の値よりも優先されます。  </span><span class="sxs-lookup"><span data-stu-id="48f77-p108">Indicates the amount of time to wait before data stored in a cache for asynchronous writing is actually written to disk. This setting overrides the values for <strong>Jet OLEDB:Shared Async Delay</strong> and <strong>Jet OLEDB:Exclusive Async Delay</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-164">Jet OLEDB: グローバル一括トランザクション</span><span class="sxs-lookup"><span data-stu-id="48f77-164">Jet OLEDB:Global Bulk Transactions</span></span><br />
<span data-ttu-id="48f77-165">(DBPROP_JETOLEDB_GLOBALBULKNOTRANSACTIONS)</span><span class="sxs-lookup"><span data-stu-id="48f77-165">(DBPROP_JETOLEDB_GLOBALBULKNOTRANSACTIONS)</span></span></p></td>
<td><p><span data-ttu-id="48f77-166">SQL 一括トランザクションが処理されるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="48f77-166">Indicates whether SQL bulk transactions are transacted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-167">Jet OLEDB: グローバル部分的な一括 Ops</span><span class="sxs-lookup"><span data-stu-id="48f77-167">Jet OLEDB:Global Partial Bulk Ops</span></span><br />
<span data-ttu-id="48f77-168">(DBPROP_JETOLEDB_GLOBALBULKPARTIAL)</span><span class="sxs-lookup"><span data-stu-id="48f77-168">(DBPROP_JETOLEDB_GLOBALBULKPARTIAL)</span></span></p></td>
<td><p><span data-ttu-id="48f77-169">データベースを開くときに使用されるパスワードを示します。</span><span class="sxs-lookup"><span data-stu-id="48f77-169">Indicates the password used to open the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-170">Jet OLEDB:Implicit Commit Sync</span><span class="sxs-lookup"><span data-stu-id="48f77-170">Jet OLEDB:Implicit Commit Sync</span></span><br />
<span data-ttu-id="48f77-171">(DBPROP_JETOLEDB_IMPLICITCOMMITSYNC)</span><span class="sxs-lookup"><span data-stu-id="48f77-171">(DBPROP_JETOLEDB_IMPLICITCOMMITSYNC)</span></span></p></td>
<td><p><span data-ttu-id="48f77-172">暗黙の内部トランザクションで加えられた変更が、同期モードで書き込まれるか、非同期モードで書き込まれるかを示します。</span><span class="sxs-lookup"><span data-stu-id="48f77-172">Indicates whether changes made in internal implicit transactions are written in synchronous or asynchronous mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-173">Jet OLEDB:Lock Delay</span><span class="sxs-lookup"><span data-stu-id="48f77-173">Jet OLEDB:Lock Delay</span></span><br />
<span data-ttu-id="48f77-174">(DBPROP_JETOLEDB_LOCKDELAY)</span><span class="sxs-lookup"><span data-stu-id="48f77-174">(DBPROP_JETOLEDB_LOCKDELAY)</span></span></p></td>
<td><p><span data-ttu-id="48f77-175">ロックの取得に失敗した後、再試行までの待ち時間をミリ秒単位で示します。</span><span class="sxs-lookup"><span data-stu-id="48f77-175">Indicates the number of milliseconds to wait before attempting to acquire a lock after a previous attempt has failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-176">Jet OLEDB:Lock Retry</span><span class="sxs-lookup"><span data-stu-id="48f77-176">Jet OLEDB:Lock Retry</span></span><br />
<span data-ttu-id="48f77-177">(DBPROP_JETOLEDB_LOCKRETRY)</span><span class="sxs-lookup"><span data-stu-id="48f77-177">(DBPROP_JETOLEDB_LOCKRETRY)</span></span></p></td>
<td><p><span data-ttu-id="48f77-178">ロックされたページへのアクセスを試行する回数を示します。</span><span class="sxs-lookup"><span data-stu-id="48f77-178">Indicates how many times an attempt to access a locked page is repeated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-179">Jet OLEDB:Max Buffer Size</span><span class="sxs-lookup"><span data-stu-id="48f77-179">Jet OLEDB:Max Buffer Size</span></span><br />
<span data-ttu-id="48f77-180">(DBPROP_JETOLEDB_MAXBUFFERSIZE)</span><span class="sxs-lookup"><span data-stu-id="48f77-180">(DBPROP_JETOLEDB_MAXBUFFERSIZE)</span></span></p></td>
<td><p><span data-ttu-id="48f77-181">ディスクへの変更の反映を開始するまでに、Jet が使用できる最大メモリ量を KB 単位で示します。</span><span class="sxs-lookup"><span data-stu-id="48f77-181">Indicates the maximum amount of memory, in kilobytes, Jet can use before it starts flushing changes to disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-182">Jet OLEDB:Max Locks Per File</span><span class="sxs-lookup"><span data-stu-id="48f77-182">Jet OLEDB:Max Locks Per File</span></span><br />
<span data-ttu-id="48f77-183">(DBPROP_JETOLEDB_MAXLOCKSPERFILE)</span><span class="sxs-lookup"><span data-stu-id="48f77-183">(DBPROP_JETOLEDB_MAXLOCKSPERFILE)</span></span></p></td>
<td><p><span data-ttu-id="48f77-p109">データベースに配置できるロックの最大数を示します。既定値は 9500 です。</span><span class="sxs-lookup"><span data-stu-id="48f77-p109">Indicates the maximum number of locks Jet can place on a database. The default value is 9500.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-186">Jet OLEDB: 新しいデータベースのパスワード</span><span class="sxs-lookup"><span data-stu-id="48f77-186">Jet OLEDB:New Database Password</span></span><br />
<span data-ttu-id="48f77-187">(DBPROP_JETOLEDB_NEWDATABASEPASSWORD)</span><span class="sxs-lookup"><span data-stu-id="48f77-187">(DBPROP_JETOLEDB_NEWDATABASEPASSWORD)</span></span></p></td>
<td><p><span data-ttu-id="48f77-p110">このデータベースに設定する新しいパスワードを示します。元のパスワードは <strong>Jet OLEDB:Database Password</strong> に保存されます。  </span><span class="sxs-lookup"><span data-stu-id="48f77-p110">Indicates the new password to be set for this database. The old password is stored in <strong>Jet OLEDB:Database Password</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-190">Jet OLEDB:ODBC コマンドの時間切れ</span><span class="sxs-lookup"><span data-stu-id="48f77-190">Jet OLEDB:ODBC Command Time Out</span></span><br />
<span data-ttu-id="48f77-191">(DBPROP_JETOLEDB_ODBCCOMMANDTIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="48f77-191">(DBPROP_JETOLEDB_ODBCCOMMANDTIMEOUT)</span></span></p></td>
<td><p><span data-ttu-id="48f77-192">Jet からのリモート ODBC クエリがタイムアウトになるまでの時間をミリ秒単位で示します。</span><span class="sxs-lookup"><span data-stu-id="48f77-192">Indicates the number of milliseconds before a remote ODBC query from Jet will timeout.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-193">テーブル ロックに jet の OLEDB:Page ロック</span><span class="sxs-lookup"><span data-stu-id="48f77-193">Jet OLEDB:Page Locks to Table Lock</span></span><br />
<span data-ttu-id="48f77-194">(DBPROP_JETOLEDB_PAGELOCKSTOTABLELOCK)</span><span class="sxs-lookup"><span data-stu-id="48f77-194">(DBPROP_JETOLEDB_PAGELOCKSTOTABLELOCK)</span></span></p></td>
<td><p><span data-ttu-id="48f77-p111">ロックからテーブル ロックへの昇格を試行するまでに、トランザクションでロックする必要があるページ数を示します。この値が 0 の場合、ロックは昇格されません。</span><span class="sxs-lookup"><span data-stu-id="48f77-p111">Indicates how many pages need to be locked within a transaction before Jet attempts to promote the lock to a table lock. If this value is 0, then the lock is never promoted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-197">Jet OLEDB:Page Timeout</span><span class="sxs-lookup"><span data-stu-id="48f77-197">Jet OLEDB:Page Timeout</span></span><br />
<span data-ttu-id="48f77-198">(DBPROP_JETOLEDB_PAGETIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="48f77-198">(DBPROP_JETOLEDB_PAGETIMEOUT)</span></span></p></td>
<td><p><span data-ttu-id="48f77-199">キャッシュが古くなっていないかどうかを確認するためにデータベース ファイルと照合するまでの待ち時間をミリ秒単位で示します。</span><span class="sxs-lookup"><span data-stu-id="48f77-199">Indicates the number of milliseconds Jet will wait before checking to see if its cache is out of date with the database file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-200">Jet OLEDB:Recycle Long-Valued Pages</span><span class="sxs-lookup"><span data-stu-id="48f77-200">Jet OLEDB:Recycle Long-Valued Pages</span></span><br />
<span data-ttu-id="48f77-201">(DBPROP_JETOLEDB_RECYCLELONGVALUEPAGES)</span><span class="sxs-lookup"><span data-stu-id="48f77-201">(DBPROP_JETOLEDB_RECYCLELONGVALUEPAGES)</span></span></p></td>
<td><p><span data-ttu-id="48f77-202">BLOB ページが解放されたときに、BLOB ページの再利用を積極的に試行するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="48f77-202">Indicates whether Jet should aggressively try to reclaim BLOB pages when they are freed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-203">Jet OLEDB:Registry Path</span><span class="sxs-lookup"><span data-stu-id="48f77-203">Jet OLEDB:Registry Path</span></span><br />
<span data-ttu-id="48f77-204">(DBPROP_JETOLEDB_REGPATH)</span><span class="sxs-lookup"><span data-stu-id="48f77-204">(DBPROP_JETOLEDB_REGPATH)</span></span></p></td>
<td><p><span data-ttu-id="48f77-205">Jet データベース エンジンの値を格納する Windows レジストリ キーを示します。</span><span class="sxs-lookup"><span data-stu-id="48f77-205">Indicates the Windows registry key that contains values for the Jet database engine.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-206">Jet OLEDB:Reset isam ドライバーの統計情報</span><span class="sxs-lookup"><span data-stu-id="48f77-206">Jet OLEDB:Reset ISAM Stats</span></span><br />
<span data-ttu-id="48f77-207">(DBPROP_JETOLEDB_RESETISAMSTATS)</span><span class="sxs-lookup"><span data-stu-id="48f77-207">(DBPROP_JETOLEDB_RESETISAMSTATS)</span></span></p></td>
<td><p><span data-ttu-id="48f77-208">パフォーマンス情報を返した後、スキーマ <strong>Recordset</strong> DBSCHEMA_JETOLEDB_ISAMSTATS のパフォーマンス カウンターをリセットするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="48f77-208">Indicates whether the schema <strong>Recordset</strong> DBSCHEMA_JETOLEDB_ISAMSTATS should reset its performance counters after returning performance information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-209">Jet OLEDB:Shared Async Delay</span><span class="sxs-lookup"><span data-stu-id="48f77-209">Jet OLEDB:Shared Async Delay</span></span><br />
<span data-ttu-id="48f77-210">(DBPROP_JETOLEDB_SHAREDASYNCDELAY)</span><span class="sxs-lookup"><span data-stu-id="48f77-210">(DBPROP_JETOLEDB_SHAREDASYNCDELAY)</span></span></p></td>
<td><p><span data-ttu-id="48f77-211">データベースがマルチユーザー モードで開かれている場合に、ディスクへの非同期書き込みで許容される最大遅延時間をミリ秒単位で示します。</span><span class="sxs-lookup"><span data-stu-id="48f77-211">Indicates the maximum amount of time, in milliseconds, Jet can delay asynchronous writes to disk when the database is opened in multi-user mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-212">Jet OLEDB:System Database</span><span class="sxs-lookup"><span data-stu-id="48f77-212">Jet OLEDB:System Database</span></span><br />
<span data-ttu-id="48f77-213">(DBPROP_JETOLEDB_SYSDBPATH)</span><span class="sxs-lookup"><span data-stu-id="48f77-213">(DBPROP_JETOLEDB_SYSDBPATH)</span></span></p></td>
<td><p><span data-ttu-id="48f77-214">ワークグループ情報ファイル (システム データベース) のパスおよびファイル名を示します。</span><span class="sxs-lookup"><span data-stu-id="48f77-214">Indicates the path and file name for the workgroup information file (system database).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-215">Jet OLEDB:Transaction コミット ・ モード</span><span class="sxs-lookup"><span data-stu-id="48f77-215">Jet OLEDB:Transaction Commit Mode</span></span><br />
<span data-ttu-id="48f77-216">(DBPROP_JETOLEDB_TXNCOMMITMODE)</span><span class="sxs-lookup"><span data-stu-id="48f77-216">(DBPROP_JETOLEDB_TXNCOMMITMODE)</span></span></p></td>
<td><p><span data-ttu-id="48f77-217">トランザクションがコミットされたときに、データをディスクに同期モードで書き込むか、非同期モードで書き込むかを示します。</span><span class="sxs-lookup"><span data-stu-id="48f77-217">Indicates whether Jet writes data to disk synchronously or asynchronously when a transaction is committed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-218">Jet OLEDB:User Commit Sync</span><span class="sxs-lookup"><span data-stu-id="48f77-218">Jet OLEDB:User Commit Sync</span></span><br />
<span data-ttu-id="48f77-219">(DBPROP_JETOLEDB_USERCOMMITSYNC)</span><span class="sxs-lookup"><span data-stu-id="48f77-219">(DBPROP_JETOLEDB_USERCOMMITSYNC)</span></span></p></td>
<td><p><span data-ttu-id="48f77-220">トランザクションで加えられた変更が、同期モードで書き込まれるか、非同期モードで書き込まれるかを示します。</span><span class="sxs-lookup"><span data-stu-id="48f77-220">Indicates whether changes made in transactions are written in synchronous or asynchronous mode.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a><span data-ttu-id="48f77-221">プロバイダー固有の Recordset および Command のプロパティ</span><span class="sxs-lookup"><span data-stu-id="48f77-221">Provider-Specific Recordset and Command Properties</span></span>

<span data-ttu-id="48f77-p112">Jet プロバイダーは、プロバイダー固有の **Recordset** のプロパティと **Command** のプロパティもサポートしています。これらのプロパティは、 **Recordset** オブジェクトまたは **Command** オブジェクトの **Properties** コレクションをとおしてアクセスおよび設定します。次の表は、このプロバイダーに固有の ADO プロパティ名の一覧で、かっこ内は対応する OLE DB プロパティ名です。</span><span class="sxs-lookup"><span data-stu-id="48f77-p112">The Jet provider also supports several provider-specific **Recordset** and **Command** properties. These properties are accessed and set through the **Properties** collection of the **Recordset** or **Command** object. The table lists the ADO property name and its corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="48f77-225">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="48f77-225">Property Name</span></span></p></th>
<th><p><span data-ttu-id="48f77-226">説明</span><span class="sxs-lookup"><span data-stu-id="48f77-226">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="48f77-227">Jet OLEDB:Bulk トランザクション</span><span class="sxs-lookup"><span data-stu-id="48f77-227">Jet OLEDB:Bulk Transactions</span></span><br />
<span data-ttu-id="48f77-228">(DBPROP_JETOLEDB_BULKNOTRANSACTIONS)</span><span class="sxs-lookup"><span data-stu-id="48f77-228">(DBPROP_JETOLEDB_BULKNOTRANSACTIONS)</span></span></p></td>
<td><p><span data-ttu-id="48f77-p113">SQL の一括操作が処理されるかどうかを示します。大量の一括操作は、リソース遅延のために、処理に失敗する場合があります。</span><span class="sxs-lookup"><span data-stu-id="48f77-p113">Indicates whether SQL bulk operations are transacted. Large bulk operations might fail when transacted, due to resource delays.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-231">Jet OLEDB:Enable Fat カーソル</span><span class="sxs-lookup"><span data-stu-id="48f77-231">Jet OLEDB:Enable Fat Cursors</span></span><br />
<span data-ttu-id="48f77-232">(DBPROP_JETOLEDB_ENABLEFATCURSOR)</span><span class="sxs-lookup"><span data-stu-id="48f77-232">(DBPROP_JETOLEDB_ENABLEFATCURSOR)</span></span></p></td>
<td><p><span data-ttu-id="48f77-233">リモートの行ソースのレコードセットを作成するときに、複数の行をキャッシュするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="48f77-233">Indicates whether Jet should cache multiple rows when populating a recordset for remote row sources.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-234">OLEDB:Fat jet カーソル ・ キャッシュ ・ サイズ</span><span class="sxs-lookup"><span data-stu-id="48f77-234">Jet OLEDB:Fat Cursor Cache Size</span></span><br />
<span data-ttu-id="48f77-235">(DBPROP_JETOLEDB_FATCURSORMAXROWS)</span><span class="sxs-lookup"><span data-stu-id="48f77-235">(DBPROP_JETOLEDB_FATCURSORMAXROWS)</span></span></p></td>
<td><p><span data-ttu-id="48f77-p114">リモート データ ストアの行キャッシュを使用するときに、キャッシュする行数を示します。 <strong>Jet OLEDB:Enable Fat Cursors</strong> が True ではない場合、この値は無視されます。  </span><span class="sxs-lookup"><span data-stu-id="48f77-p114">Indicates the number of rows to cache when using remote data store row caching. This value is ignored unless <strong>Jet OLEDB:Enable Fat Cursors</strong> is True.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-238">Jet OLEDB: 一貫性のないです。</span><span class="sxs-lookup"><span data-stu-id="48f77-238">Jet OLEDB:Inconsistent</span></span><br />
<span data-ttu-id="48f77-239">(DBPROP_JETOLEDB_INCONSISTENT)</span><span class="sxs-lookup"><span data-stu-id="48f77-239">(DBPROP_JETOLEDB_INCONSISTENT)</span></span></p></td>
<td><p><span data-ttu-id="48f77-240">クエリの結果で、矛盾した更新を許容するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="48f77-240">Indicates whether query results allow inconsistent updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-241">Jet OLEDB: ロックの粒度</span><span class="sxs-lookup"><span data-stu-id="48f77-241">Jet OLEDB:Locking Granularity</span></span><br />
<span data-ttu-id="48f77-242">(DBPROP_JETOLEDB_LOCKGRANULARITY)</span><span class="sxs-lookup"><span data-stu-id="48f77-242">(DBPROP_JETOLEDB_LOCKGRANULARITY)</span></span></p></td>
<td><p><span data-ttu-id="48f77-243">テーブルが行レベルのロックを使用して開かれているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="48f77-243">Indicates whether a table is opened using row-level locking.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-244">Jet OLEDB:ODBC パススルー ステートメント</span><span class="sxs-lookup"><span data-stu-id="48f77-244">Jet OLEDB:ODBC Pass-Through Statement</span></span><br />
<span data-ttu-id="48f77-245">(DBPROP_JETOLEDB_ODBCPASSTHROUGH)</span><span class="sxs-lookup"><span data-stu-id="48f77-245">(DBPROP_JETOLEDB_ODBCPASSTHROUGH)</span></span></p></td>
<td><p><span data-ttu-id="48f77-246"><strong>Command</strong> オブジェクトの SQL テキストを変更せずにバックエンドに渡すかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="48f77-246">Indicates that Jet should pass the SQL text in a <strong>Command</strong> object to the back end unaltered.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-247">Jet OLEDB:Partial 一括 Ops</span><span class="sxs-lookup"><span data-stu-id="48f77-247">Jet OLEDB:Partial Bulk Ops</span></span><br />
<span data-ttu-id="48f77-248">(DBPROP_JETOLEDB_BULKPARTIAL)</span><span class="sxs-lookup"><span data-stu-id="48f77-248">(DBPROP_JETOLEDB_BULKPARTIAL)</span></span></p></td>
<td><p><span data-ttu-id="48f77-249">SQL DML 操作に失敗したときの Jet の動作を示します。</span><span class="sxs-lookup"><span data-stu-id="48f77-249">Indicates Jet's behavior when SQL DML operations fail.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-250">一括操作クエリを通じてジェット OLEDB:Pass</span><span class="sxs-lookup"><span data-stu-id="48f77-250">Jet OLEDB:Pass Through Query Bulk-Op</span></span><br />
<span data-ttu-id="48f77-251">(DBPROP_JETOLEDB_PASSTHROUGHBULKOP)</span><span class="sxs-lookup"><span data-stu-id="48f77-251">(DBPROP_JETOLEDB_PASSTHROUGHBULKOP)</span></span></p></td>
<td><p><span data-ttu-id="48f77-252"><strong>Recordset</strong> を返さないクエリを変更せずにデータ ソースに渡すかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="48f77-252">Indicates whether queries that do not return a <strong>Recordset</strong> are passed unaltered to the data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-253">接続文字列はクエリを通じてジェット OLEDB:Pass</span><span class="sxs-lookup"><span data-stu-id="48f77-253">Jet OLEDB:Pass Through Query Connect String</span></span><br />
<span data-ttu-id="48f77-254">(DBPROP_JETOLEDB_ODBCPASSTHROUGHCONNECTSTRING)</span><span class="sxs-lookup"><span data-stu-id="48f77-254">(DBPROP_JETOLEDB_ODBCPASSTHROUGHCONNECTSTRING)</span></span></p></td>
<td><p><span data-ttu-id="48f77-p115">リモート データ ストアへの接続に使用される Jet 接続文字列を示します。 <strong>Jet OLEDB:ODBC Pass-Through Statement</strong> が True ではない場合、この値は無視されます。  </span><span class="sxs-lookup"><span data-stu-id="48f77-p115">Indicates the Jet connect string used to connect to a remote data store. This value is ignored unless <strong>Jet OLEDB:ODBC Pass-Through Statement</strong> is True.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-257">Jet OLEDB: クエリの保存</span><span class="sxs-lookup"><span data-stu-id="48f77-257">Jet OLEDB:Stored Query</span></span><br />
<span data-ttu-id="48f77-258">(DBPROP_JETOLEDB_STOREDQUERY)</span><span class="sxs-lookup"><span data-stu-id="48f77-258">(DBPROP_JETOLEDB_STOREDQUERY)</span></span></p></td>
<td><p><span data-ttu-id="48f77-259">コマンド テキストを、SQL コマンドではなく、ストアド クエリとして解釈するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="48f77-259">Indicates whether the command text should be interpreted as a stored query instead of an SQL command.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-260">Jet OLEDB: 一連のルールを検証</span><span class="sxs-lookup"><span data-stu-id="48f77-260">Jet OLEDB:Validate Rules On Set</span></span><br />
<span data-ttu-id="48f77-261">(DBPROP_JETOLEDB_VALIDATEONSET)</span><span class="sxs-lookup"><span data-stu-id="48f77-261">(DBPROP_JETOLEDB_VALIDATEONSET)</span></span></p></td>
<td><p><span data-ttu-id="48f77-262">列データを設定するとき、または変更をデータベースにコミットするときに、Jet 入力規則を評価するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="48f77-262">Indicates whether the Jet validation rules are evaluated when column data is set or when the changes are committed to the database.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="48f77-p116">既定では、OLE DB Provider for Microsoft Jet は Microsoft Jet データベースを読み取り/書き込み可能モードで開きます。データベースを読み取り専用モードで開くには、ADO [Connection](mode-property-ado.md) オブジェクトの **Mode** プロパティを **adModeRead** に設定します。</span><span class="sxs-lookup"><span data-stu-id="48f77-p116">By default, the OLE DB Provider for Microsoft Jet opens Microsoft Jet databases in read/write mode. To open a database in read-only mode, set the [Mode](mode-property-ado.md) property on the ADO **Connection** object to **adModeRead**.</span></span>

## <a name="command-object-usage"></a><span data-ttu-id="48f77-265">Command オブジェクトの使用方法</span><span class="sxs-lookup"><span data-stu-id="48f77-265">Command Object Usage</span></span>

<span data-ttu-id="48f77-p117">[Command](command-object-ado.md) オブジェクトのコマンド テキストでは、Microsoft Jet SQL 言語を使用します。コマンド テキストでは、行を返すクエリ、アクション クエリ、およびテーブル名を指定できますが、ストアド プロシージャはサポートされていないので指定できません。</span><span class="sxs-lookup"><span data-stu-id="48f77-p117">Command text in the [Command](command-object-ado.md) object uses the Microsoft Jet SQL dialect. You can specify row-returning queries, action queries, and table names in the command text; however, stored procedures are not supported and should not be specified.</span></span>

## <a name="recordset-behavior"></a><span data-ttu-id="48f77-268">Recordset の動作</span><span class="sxs-lookup"><span data-stu-id="48f77-268">Recordset Behavior</span></span>

<span data-ttu-id="48f77-p118">Microsoft Jet データベース エンジンは動的カーソルをサポートしていません。したがって、OLE DB Provider for Microsoft Jet は、カーソルの種類 **adLockDynamic** をサポートしていません。動的カーソルが要求された場合、プロバイダーはキーセット カーソルを返し、[CursorType](cursortype-property-ado.md) プロパティを、返された [Recordset](recordset-object-ado.md) の種類を示す値に設定し直します。また、更新可能な **Recordset** が要求された場合 (**LockType** が **adLockOptimistic**、**adLockBatchOptimistic**、または **adLockPessimistic**)、プロバイダーはキーセット カーソルを返し、**CursorType** プロパティを設定し直します。</span><span class="sxs-lookup"><span data-stu-id="48f77-p118">The Microsoft Jet database engine does not support dynamic cursors. Therefore, the OLE DB Provider for Microsoft Jet does not support the **adLockDynamic** cursor type. When a dynamic cursor is requested, the provider will return a keyset cursor and reset the [CursorType](cursortype-property-ado.md) property to indicate the type of [Recordset](recordset-object-ado.md) returned. Further, if an updatable **Recordset** is requested (**LockType** is **adLockOptimistic**, **adLockBatchOptimistic**, or **adLockPessimistic**) the provider will also return a keyset cursor and reset the **CursorType** property.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="48f77-273">動的プロパティ</span><span class="sxs-lookup"><span data-stu-id="48f77-273">Dynamic Properties</span></span>

<span data-ttu-id="48f77-274">OLE DB Provider for Microsoft Jet は、開かれていない **Connection** オブジェクト、 [Recordset](connection-object-ado.md) オブジェクト、および [Command](recordset-object-ado.md) オブジェクトの [Properties](command-object-ado.md) コレクションに動的プロパティを挿入します。</span><span class="sxs-lookup"><span data-stu-id="48f77-274">The OLE DB Provider for Microsoft Jet inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="48f77-p119">以下の表は、各動的プロパティの ADO 名と OLE DB 名の対応表です。「OLE DB プログラマ リファレンス」では、「説明」欄に ADO プロパティ名が示されています。プロパティの詳細については、「OLE DB プログラマ リファレンス」を参照してください。OLE DB プロパティ名をキーワードとして検索するか、「付録 C: プロパティ表」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="48f77-p119">The tables below are a cross-index of the ADO and OLE DB names for each dynamic property. The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description." You can find more information about these properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="48f77-279">Connection の動的プロパティ</span><span class="sxs-lookup"><span data-stu-id="48f77-279">Connection Dynamic Properties</span></span>

<span data-ttu-id="48f77-280">次に示すプロパティが **Connection** オブジェクトの **Properties** コレクションに追加されます。</span><span class="sxs-lookup"><span data-stu-id="48f77-280">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="48f77-281">ADO プロパティ名</span><span class="sxs-lookup"><span data-stu-id="48f77-281">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="48f77-282">OLE DB プロパティ名</span><span class="sxs-lookup"><span data-stu-id="48f77-282">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="48f77-283">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="48f77-283">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="48f77-284">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="48f77-284">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-285">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="48f77-285">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="48f77-286">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="48f77-286">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-287">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="48f77-287">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="48f77-288">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="48f77-288">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-289">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="48f77-289">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="48f77-290">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="48f77-290">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-291">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="48f77-291">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="48f77-292">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="48f77-292">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-293">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="48f77-293">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="48f77-294">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="48f77-294">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-295">Column Definition</span><span class="sxs-lookup"><span data-stu-id="48f77-295">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="48f77-296">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="48f77-296">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-297">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="48f77-297">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="48f77-298">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="48f77-298">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-299">Data Source</span><span class="sxs-lookup"><span data-stu-id="48f77-299">Data Source</span></span></p></td>
<td><p><span data-ttu-id="48f77-300">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="48f77-300">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-301">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="48f77-301">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="48f77-302">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="48f77-302">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-303">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="48f77-303">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="48f77-304">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="48f77-304">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-305">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="48f77-305">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="48f77-306">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="48f77-306">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-307">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="48f77-307">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="48f77-308">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="48f77-308">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-309">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="48f77-309">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="48f77-310">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="48f77-310">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-311">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="48f77-311">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="48f77-312">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="48f77-312">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-313">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="48f77-313">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="48f77-314">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="48f77-314">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-315">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="48f77-315">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="48f77-316">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="48f77-316">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-317">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="48f77-317">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="48f77-318">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="48f77-318">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-319">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="48f77-319">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="48f77-320">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="48f77-320">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-321">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="48f77-321">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="48f77-322">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="48f77-322">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-323">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="48f77-323">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="48f77-324">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="48f77-324">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-325">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="48f77-325">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="48f77-326">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="48f77-326">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-327">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="48f77-327">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="48f77-328">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="48f77-328">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-329">Mode</span><span class="sxs-lookup"><span data-stu-id="48f77-329">Mode</span></span></p></td>
<td><p><span data-ttu-id="48f77-330">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="48f77-330">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-331">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="48f77-331">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="48f77-332">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="48f77-332">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-333">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="48f77-333">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="48f77-334">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="48f77-334">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-335">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="48f77-335">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="48f77-336">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="48f77-336">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-337">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="48f77-337">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="48f77-338">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="48f77-338">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-339">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="48f77-339">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="48f77-340">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="48f77-340">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-341">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="48f77-341">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="48f77-342">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="48f77-342">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-343">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="48f77-343">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="48f77-344">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="48f77-344">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-345">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="48f77-345">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="48f77-346">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="48f77-346">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-347">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="48f77-347">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="48f77-348">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="48f77-348">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-349">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="48f77-349">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="48f77-350">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="48f77-350">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-351">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="48f77-351">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="48f77-352">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="48f77-352">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-353">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="48f77-353">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="48f77-354">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="48f77-354">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-355">Password</span><span class="sxs-lookup"><span data-stu-id="48f77-355">Password</span></span></p></td>
<td><p><span data-ttu-id="48f77-356">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="48f77-356">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-357">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="48f77-357">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="48f77-358">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="48f77-358">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-359">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="48f77-359">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="48f77-360">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="48f77-360">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-361">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="48f77-361">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="48f77-362">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="48f77-362">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-363">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="48f77-363">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="48f77-364">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="48f77-364">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-365">Prompt</span><span class="sxs-lookup"><span data-stu-id="48f77-365">Prompt</span></span></p></td>
<td><p><span data-ttu-id="48f77-366">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="48f77-366">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-367">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="48f77-367">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="48f77-368">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="48f77-368">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-369">Provider Name</span><span class="sxs-lookup"><span data-stu-id="48f77-369">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="48f77-370">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="48f77-370">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-371">Provider Version</span><span class="sxs-lookup"><span data-stu-id="48f77-371">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="48f77-372">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="48f77-372">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-373">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="48f77-373">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="48f77-374">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="48f77-374">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-375">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="48f77-375">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="48f77-376">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="48f77-376">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-377">Schema Term</span><span class="sxs-lookup"><span data-stu-id="48f77-377">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="48f77-378">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="48f77-378">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-379">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="48f77-379">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="48f77-380">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="48f77-380">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-381">SQL Support</span><span class="sxs-lookup"><span data-stu-id="48f77-381">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="48f77-382">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="48f77-382">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-383">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="48f77-383">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="48f77-384">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="48f77-384">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-385">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="48f77-385">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="48f77-386">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="48f77-386">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-387">Table Term</span><span class="sxs-lookup"><span data-stu-id="48f77-387">Table Term</span></span></p></td>
<td><p><span data-ttu-id="48f77-388">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="48f77-388">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-389">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="48f77-389">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="48f77-390">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="48f77-390">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-391">User ID</span><span class="sxs-lookup"><span data-stu-id="48f77-391">User ID</span></span></p></td>
<td><p><span data-ttu-id="48f77-392">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="48f77-392">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-393">User Name</span><span class="sxs-lookup"><span data-stu-id="48f77-393">User Name</span></span></p></td>
<td><p><span data-ttu-id="48f77-394">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="48f77-394">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-395">Window Handle</span><span class="sxs-lookup"><span data-stu-id="48f77-395">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="48f77-396">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="48f77-396">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="48f77-397">Recordset の動的プロパティ</span><span class="sxs-lookup"><span data-stu-id="48f77-397">Recordset Dynamic Properties</span></span>

<span data-ttu-id="48f77-398">次に示すプロパティが **Recordset** オブジェクトの **Properties** コレクションに追加されます。</span><span class="sxs-lookup"><span data-stu-id="48f77-398">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="48f77-399">ADO プロパティ名</span><span class="sxs-lookup"><span data-stu-id="48f77-399">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="48f77-400">OLE DB プロパティ名</span><span class="sxs-lookup"><span data-stu-id="48f77-400">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="48f77-401">Access Order</span><span class="sxs-lookup"><span data-stu-id="48f77-401">Access Order</span></span></p></td>
<td><p><span data-ttu-id="48f77-402">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="48f77-402">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-403">Append-Only Rowset</span><span class="sxs-lookup"><span data-stu-id="48f77-403">Append-Only Rowset</span></span></p></td>
<td><p><span data-ttu-id="48f77-404">DBPROP_APPENDONLY</span><span class="sxs-lookup"><span data-stu-id="48f77-404">DBPROP_APPENDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-405">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="48f77-405">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="48f77-406">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="48f77-406">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-407">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="48f77-407">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="48f77-408">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="48f77-408">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-409">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="48f77-409">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="48f77-410">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="48f77-410">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-411">Bookmarks Ordered</span><span class="sxs-lookup"><span data-stu-id="48f77-411">Bookmarks Ordered</span></span></p></td>
<td><p><span data-ttu-id="48f77-412">DBPROP_ORDEREDBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="48f77-412">DBPROP_ORDEREDBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-413">Cache Deferred Columns</span><span class="sxs-lookup"><span data-stu-id="48f77-413">Cache Deferred Columns</span></span></p></td>
<td><p><span data-ttu-id="48f77-414">DBPROP_CACHEDEFERRED</span><span class="sxs-lookup"><span data-stu-id="48f77-414">DBPROP_CACHEDEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-415">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="48f77-415">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="48f77-416">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="48f77-416">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-417">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="48f77-417">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="48f77-418">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="48f77-418">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-419">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="48f77-419">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="48f77-420">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="48f77-420">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-421">Column Writable</span><span class="sxs-lookup"><span data-stu-id="48f77-421">Column Writable</span></span></p></td>
<td><p><span data-ttu-id="48f77-422">DBPROP_MAYWRITECOLUMN</span><span class="sxs-lookup"><span data-stu-id="48f77-422">DBPROP_MAYWRITECOLUMN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-423">Defer Column</span><span class="sxs-lookup"><span data-stu-id="48f77-423">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="48f77-424">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="48f77-424">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-425">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="48f77-425">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="48f77-426">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="48f77-426">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-427">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="48f77-427">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="48f77-428">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="48f77-428">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-429">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="48f77-429">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="48f77-430">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="48f77-430">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-431">IAccessor</span><span class="sxs-lookup"><span data-stu-id="48f77-431">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="48f77-432">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="48f77-432">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-433">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="48f77-433">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="48f77-434">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="48f77-434">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-435">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="48f77-435">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="48f77-436">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="48f77-436">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-437">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="48f77-437">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="48f77-438">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="48f77-438">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-439">IConvertType</span><span class="sxs-lookup"><span data-stu-id="48f77-439">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="48f77-440">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="48f77-440">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-441">ILockBytes</span><span class="sxs-lookup"><span data-stu-id="48f77-441">ILockBytes</span></span></p></td>
<td><p><span data-ttu-id="48f77-442">DBPROP_ILockBytes</span><span class="sxs-lookup"><span data-stu-id="48f77-442">DBPROP_ILockBytes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-443">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="48f77-443">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="48f77-444">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="48f77-444">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-445">IRowset</span><span class="sxs-lookup"><span data-stu-id="48f77-445">IRowset</span></span></p></td>
<td><p><span data-ttu-id="48f77-446">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="48f77-446">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-447">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="48f77-447">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="48f77-448">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="48f77-448">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-449">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="48f77-449">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="48f77-450">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="48f77-450">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-451">IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="48f77-451">IRowsetIndex</span></span></p></td>
<td><p><span data-ttu-id="48f77-452">DBPROP_IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="48f77-452">DBPROP_IRowsetIndex</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-453">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="48f77-453">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="48f77-454">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="48f77-454">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-455">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="48f77-455">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="48f77-456">DBPROP_IRowsestLocate</span><span class="sxs-lookup"><span data-stu-id="48f77-456">DBPROP_IRowsestLocate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-457">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="48f77-457">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-458">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="48f77-458">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="48f77-459">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="48f77-459">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-460">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="48f77-460">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="48f77-461">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="48f77-461">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-462">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="48f77-462">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="48f77-463">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="48f77-463">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-464">IStorage</span><span class="sxs-lookup"><span data-stu-id="48f77-464">IStorage</span></span></p></td>
<td><p><span data-ttu-id="48f77-465">DBPROP_IStorage</span><span class="sxs-lookup"><span data-stu-id="48f77-465">DBPROP_IStorage</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-466">IStream</span><span class="sxs-lookup"><span data-stu-id="48f77-466">IStream</span></span></p></td>
<td><p><span data-ttu-id="48f77-467">DBPROP_IStream</span><span class="sxs-lookup"><span data-stu-id="48f77-467">DBPROP_IStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-468">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="48f77-468">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="48f77-469">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="48f77-469">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-470">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="48f77-470">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="48f77-471">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="48f77-471">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-472">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="48f77-472">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="48f77-473">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="48f77-473">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-474">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="48f77-474">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="48f77-475">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="48f77-475">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-476">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="48f77-476">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="48f77-477">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="48f77-477">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-478">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="48f77-478">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="48f77-479">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="48f77-479">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-480">Memory Usage</span><span class="sxs-lookup"><span data-stu-id="48f77-480">Memory Usage</span></span></p></td>
<td><p><span data-ttu-id="48f77-481">DBPROP_MEMORYUSAGE</span><span class="sxs-lookup"><span data-stu-id="48f77-481">DBPROP_MEMORYUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-482">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="48f77-482">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="48f77-483">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="48f77-483">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-484">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="48f77-484">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="48f77-485">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="48f77-485">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-486">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="48f77-486">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="48f77-487">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="48f77-487">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-488">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="48f77-488">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="48f77-489">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="48f77-489">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-490">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="48f77-490">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="48f77-491">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="48f77-491">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-492">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="48f77-492">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="48f77-493">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="48f77-493">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-494">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="48f77-494">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="48f77-495">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="48f77-495">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-496">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="48f77-496">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="48f77-497">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="48f77-497">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-498">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="48f77-498">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="48f77-499">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="48f77-499">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-500">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="48f77-500">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="48f77-501">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="48f77-501">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-502">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="48f77-502">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="48f77-503">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="48f77-503">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-504">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="48f77-504">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="48f77-505">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="48f77-505">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-506">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="48f77-506">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="48f77-507">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="48f77-507">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-508">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="48f77-508">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="48f77-509">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="48f77-509">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-510">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="48f77-510">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="48f77-511">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="48f77-511">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-512">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="48f77-512">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="48f77-513">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="48f77-513">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-514">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="48f77-514">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="48f77-515">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="48f77-515">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-516">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="48f77-516">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="48f77-517">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="48f77-517">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-518">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="48f77-518">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="48f77-519">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="48f77-519">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-520">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="48f77-520">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="48f77-521">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="48f77-521">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-522">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="48f77-522">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="48f77-523">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="48f77-523">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-524">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="48f77-524">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="48f77-525">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="48f77-525">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-526">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="48f77-526">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="48f77-527">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="48f77-527">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-528">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="48f77-528">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="48f77-529">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="48f77-529">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-530">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="48f77-530">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="48f77-531">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="48f77-531">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-532">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="48f77-532">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="48f77-533">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="48f77-533">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-534">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="48f77-534">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="48f77-535">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="48f77-535">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-536">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="48f77-536">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="48f77-537">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="48f77-537">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-538">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="48f77-538">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="48f77-539">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="48f77-539">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-540">Updatability</span><span class="sxs-lookup"><span data-stu-id="48f77-540">Updatability</span></span></p></td>
<td><p><span data-ttu-id="48f77-541">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="48f77-541">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-542">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="48f77-542">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="48f77-543">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="48f77-543">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="48f77-544">Command の動的プロパティ</span><span class="sxs-lookup"><span data-stu-id="48f77-544">Command Dynamic Properties</span></span>

<span data-ttu-id="48f77-545">次に示すプロパティが **Command** オブジェクトの **Properties** コレクションに追加されます。</span><span class="sxs-lookup"><span data-stu-id="48f77-545">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="48f77-546">ADO プロパティ名</span><span class="sxs-lookup"><span data-stu-id="48f77-546">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="48f77-547">OLE DB プロパティ名</span><span class="sxs-lookup"><span data-stu-id="48f77-547">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="48f77-548">Access Order</span><span class="sxs-lookup"><span data-stu-id="48f77-548">Access Order</span></span></p></td>
<td><p><span data-ttu-id="48f77-549">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="48f77-549">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-550">Append-Only Rowset</span><span class="sxs-lookup"><span data-stu-id="48f77-550">Append-Only Rowset</span></span></p></td>
<td><p><span data-ttu-id="48f77-551">DBPROP_APPENDONLY</span><span class="sxs-lookup"><span data-stu-id="48f77-551">DBPROP_APPENDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-552">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="48f77-552">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="48f77-553">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="48f77-553">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-554">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="48f77-554">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="48f77-555">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="48f77-555">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-556">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="48f77-556">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="48f77-557">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="48f77-557">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-558">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="48f77-558">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="48f77-559">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="48f77-559">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-560">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="48f77-560">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="48f77-561">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="48f77-561">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-562">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="48f77-562">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="48f77-563">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="48f77-563">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-564">Defer Column</span><span class="sxs-lookup"><span data-stu-id="48f77-564">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="48f77-565">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="48f77-565">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-566">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="48f77-566">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="48f77-567">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="48f77-567">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-568">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="48f77-568">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="48f77-569">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="48f77-569">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-570">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="48f77-570">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="48f77-571">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="48f77-571">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-572">IAccessor</span><span class="sxs-lookup"><span data-stu-id="48f77-572">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="48f77-573">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="48f77-573">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-574">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="48f77-574">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="48f77-575">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="48f77-575">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-576">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="48f77-576">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="48f77-577">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="48f77-577">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-578">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="48f77-578">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="48f77-579">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="48f77-579">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-580">IConvertType</span><span class="sxs-lookup"><span data-stu-id="48f77-580">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="48f77-581">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="48f77-581">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-582">ILockBytes</span><span class="sxs-lookup"><span data-stu-id="48f77-582">ILockBytes</span></span></p></td>
<td><p><span data-ttu-id="48f77-583">DBPROP_ILockBytes</span><span class="sxs-lookup"><span data-stu-id="48f77-583">DBPROP_ILockBytes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-584">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="48f77-584">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="48f77-585">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="48f77-585">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-586">IRowset</span><span class="sxs-lookup"><span data-stu-id="48f77-586">IRowset</span></span></p></td>
<td><p><span data-ttu-id="48f77-587">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="48f77-587">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-588">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="48f77-588">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="48f77-589">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="48f77-589">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-590">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="48f77-590">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="48f77-591">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="48f77-591">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-592">IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="48f77-592">IRowsetIndex</span></span></p></td>
<td><p><span data-ttu-id="48f77-593">DBPROP_IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="48f77-593">DBPROP_IRowsetIndex</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-594">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="48f77-594">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="48f77-595">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="48f77-595">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-596">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="48f77-596">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="48f77-597">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="48f77-597">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-598">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="48f77-598">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-599">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="48f77-599">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="48f77-600">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="48f77-600">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-601">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="48f77-601">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="48f77-602">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="48f77-602">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-603">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="48f77-603">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="48f77-604">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="48f77-604">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-605">IStorage</span><span class="sxs-lookup"><span data-stu-id="48f77-605">IStorage</span></span></p></td>
<td><p><span data-ttu-id="48f77-606">DBPROP_IStorage</span><span class="sxs-lookup"><span data-stu-id="48f77-606">DBPROP_IStorage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-607">IStream</span><span class="sxs-lookup"><span data-stu-id="48f77-607">IStream</span></span></p></td>
<td><p><span data-ttu-id="48f77-608">DBPROP_IStream</span><span class="sxs-lookup"><span data-stu-id="48f77-608">DBPROP_IStream</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-609">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="48f77-609">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="48f77-610">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="48f77-610">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-611">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="48f77-611">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="48f77-612">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="48f77-612">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-613">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="48f77-613">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="48f77-614">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="48f77-614">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-615">Lock Mode</span><span class="sxs-lookup"><span data-stu-id="48f77-615">Lock Mode</span></span></p></td>
<td><p><span data-ttu-id="48f77-616">DBPROP_LOCKMODE</span><span class="sxs-lookup"><span data-stu-id="48f77-616">DBPROP_LOCKMODE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-617">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="48f77-617">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="48f77-618">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="48f77-618">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-619">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="48f77-619">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="48f77-620">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="48f77-620">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-621">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="48f77-621">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="48f77-622">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="48f77-622">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-623">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="48f77-623">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="48f77-624">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="48f77-624">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-625">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="48f77-625">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="48f77-626">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="48f77-626">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-627">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="48f77-627">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="48f77-628">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="48f77-628">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-629">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="48f77-629">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="48f77-630">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="48f77-630">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-631">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="48f77-631">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="48f77-632">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="48f77-632">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-633">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="48f77-633">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="48f77-634">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="48f77-634">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-635">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="48f77-635">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="48f77-636">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="48f77-636">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-637">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="48f77-637">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="48f77-638">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="48f77-638">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-639">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="48f77-639">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="48f77-640">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="48f77-640">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-641">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="48f77-641">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="48f77-642">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="48f77-642">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-643">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="48f77-643">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="48f77-644">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="48f77-644">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-645">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="48f77-645">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="48f77-646">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="48f77-646">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-647">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="48f77-647">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="48f77-648">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="48f77-648">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-649">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="48f77-649">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="48f77-650">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="48f77-650">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-651">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="48f77-651">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="48f77-652">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="48f77-652">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-653">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="48f77-653">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="48f77-654">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="48f77-654">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-655">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="48f77-655">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="48f77-656">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="48f77-656">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-657">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="48f77-657">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="48f77-658">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="48f77-658">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-659">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="48f77-659">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="48f77-660">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="48f77-660">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-661">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="48f77-661">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="48f77-662">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="48f77-662">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-663">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="48f77-663">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="48f77-664">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="48f77-664">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-665">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="48f77-665">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="48f77-666">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="48f77-666">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-667">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="48f77-667">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="48f77-668">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="48f77-668">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-669">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="48f77-669">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="48f77-670">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="48f77-670">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-671">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="48f77-671">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="48f77-672">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="48f77-672">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-673">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="48f77-673">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="48f77-674">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="48f77-674">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-675">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="48f77-675">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="48f77-676">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="48f77-676">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-677">Server Data on Insert</span><span class="sxs-lookup"><span data-stu-id="48f77-677">Server Data on Insert</span></span></p></td>
<td><p><span data-ttu-id="48f77-678">DBPROP_SERVERDATAONINSERT</span><span class="sxs-lookup"><span data-stu-id="48f77-678">DBPROP_SERVERDATAONINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-679">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="48f77-679">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="48f77-680">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="48f77-680">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-681">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="48f77-681">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="48f77-682">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="48f77-682">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48f77-683">Updatability</span><span class="sxs-lookup"><span data-stu-id="48f77-683">Updatability</span></span></p></td>
<td><p><span data-ttu-id="48f77-684">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="48f77-684">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48f77-685">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="48f77-685">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="48f77-686">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="48f77-686">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="48f77-687">関連項目</span><span class="sxs-lookup"><span data-stu-id="48f77-687">See also</span></span>

<span data-ttu-id="48f77-688">特定の実装の詳細については、Microsoft Jet の OLE DB プロバイダーの機能については、MDAC SDK のドキュメントを Microsoft Jet の OLE DB プロバイダーを参照してください。</span><span class="sxs-lookup"><span data-stu-id="48f77-688">For specific implementation details and functional information about the OLE DB Provider for Microsoft Jet, consult the OLE DB Provider for Microsoft Jet documentation in the MDAC SDK.</span></span>

