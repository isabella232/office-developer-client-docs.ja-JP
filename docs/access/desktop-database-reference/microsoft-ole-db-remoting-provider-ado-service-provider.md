---
title: Microsoft OLE DB Remoting Provider (ADO サービス プロバイダー)
TOCTitle: Microsoft OLE DB Remoting Provider (ADO Service Provider)
ms:assetid: f39bd83d-8c2c-302e-16e3-0fae50f89fbc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250238(v=office.15)
ms:contentKeyID: 48548673
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54ea659aa5392dd4404ffb591eba06f1f9c2910b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288905"
---
# <a name="microsoft-ole-db-remoting-provider-ado-service-provider"></a><span data-ttu-id="ad6ff-102">Microsoft OLE DB Remoting Provider (ADO サービス プロバイダー)</span><span class="sxs-lookup"><span data-stu-id="ad6ff-102">Microsoft OLE DB Remoting Provider (ADO Service Provider)</span></span>

<span data-ttu-id="ad6ff-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="ad6ff-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ad6ff-p101">Microsoft OLE DB Remoting Provider を使用すると、クライアント コンピューター上のローカル ユーザーはリモート コンピューターのデータ プロバイダーを呼び出すことができます。リモート コンピューターのローカル ユーザーと同じように、リモート コンピューターのデータ プロバイダー パラメーターを指定します。次に、リモート コンピューターにアクセスするために Remoting Provider で使用するパラメーターを指定します。これによって、ローカル ユーザーと同じようにリモート コンピューターにアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-p101">The Microsoft OLE DB Remoting Provider enables a local user on a client machine to invoke data providers on a remote machine. Specify the data provider parameters for the remote machine as you would if you were a local user on the remote machine. Then specify the parameters used by the Remoting Provider to access the remote machine. The resulting effect is that you will access the remote machine as if you were a local user.</span></span>

## <a name="provider-keyword"></a><span data-ttu-id="ad6ff-108">プロバイダー キーワード</span><span class="sxs-lookup"><span data-stu-id="ad6ff-108">Provider Keyword</span></span>

<span data-ttu-id="ad6ff-p102">OLE DB Remoting Provider を呼び出すには、接続文字列で次のキーワードと値を指定します。プロバイダー名に含まれるスペースに注意してください。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-p102">To invoke the OLE DB Remoting Provider, specify the following keyword and value in the connection string. (Note the blank space in the provider name.)</span></span>

```sql 
 
"Provider=MS Remote" 
```

## <a name="additional-keywords"></a><span data-ttu-id="ad6ff-111">その他のキーワード</span><span class="sxs-lookup"><span data-stu-id="ad6ff-111">Additional Keywords</span></span>

<span data-ttu-id="ad6ff-112">このサービス プロバイダーを呼び出す場合は、次に示すキーワードも指定できます。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-112">When this service provider is invoked, the following additional keywords are relevant.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ad6ff-113">キーワード</span><span class="sxs-lookup"><span data-stu-id="ad6ff-113">Keyword</span></span></p></th>
<th><p><span data-ttu-id="ad6ff-114">説明</span><span class="sxs-lookup"><span data-stu-id="ad6ff-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ad6ff-115"><strong>Data Source</strong></span><span class="sxs-lookup"><span data-stu-id="ad6ff-115"><strong>Data Source</strong></span></span></p></td>
<td><p><span data-ttu-id="ad6ff-116">リモート データ ソース名を指定します。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-116">Specifies the name of the remote data source.</span></span> <span data-ttu-id="ad6ff-117">この値は、OLE DB Remoting Provider に渡されて処理されます。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-117">It is passed to the OLE DB Remoting Provider for processing.</span></span> <span data-ttu-id="ad6ff-118">このキーワードは <a href="datacontrol-object-rds.md">RDS.DataControl</a> オブジェクトの <a href="connect-property-rds.md">Connect</a> プロパティと同等です。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-118">This keyword is equivalent to the <a href="datacontrol-object-rds.md">RDS.DataControl</a> object's <a href="connect-property-rds.md">Connect</a> property.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="dynamic-properties"></a><span data-ttu-id="ad6ff-119">動的プロパティ</span><span class="sxs-lookup"><span data-stu-id="ad6ff-119">Dynamic Properties</span></span>

<span data-ttu-id="ad6ff-120">このサービス プロバイダーを呼び出すと、次に示す動的プロパティが [Connection](connection-object-ado.md) オブジェクトの [Properties](properties-collection-ado.md) コレクションに追加されます。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-120">When this service provider is invoked, the following dynamic properties are added to the [Connection](connection-object-ado.md) object's [Properties](properties-collection-ado.md) collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ad6ff-121">動的プロパティ名</span><span class="sxs-lookup"><span data-stu-id="ad6ff-121">Dynamic Property Name</span></span></p></th>
<th><p><span data-ttu-id="ad6ff-122">説明</span><span class="sxs-lookup"><span data-stu-id="ad6ff-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ad6ff-123"><strong>DFMode</strong></span><span class="sxs-lookup"><span data-stu-id="ad6ff-123"><strong>DFMode</strong></span></span></p></td>
<td><p><span data-ttu-id="ad6ff-124">DataFactory モードを示します。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-124">Indicates the DataFactory Mode.</span></span> <span data-ttu-id="ad6ff-125">サーバー上の <a href="datafactory-object-rdsserver.md">DataFactory</a> オブジェクトのバージョンを指定する文字列です。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-125">A string that specifies the desired version of the <a href="datafactory-object-rdsserver.md">DataFactory</a> object on the server.</span></span> <span data-ttu-id="ad6ff-126">このプロパティを設定した後、接続を開いて特定のバージョンの <strong>DataFactory</strong> を要求します。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-126">Set this property before opening a connection to request a particular version of the <strong>DataFactory</strong>.</span></span> <span data-ttu-id="ad6ff-127">要求したバージョンが使用できない場合、その前のバージョンの使用が試行されます。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-127">If the requested version is not available, an attempt will be made to use the preceding version.</span></span> <span data-ttu-id="ad6ff-128">前のバージョンが存在しない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-128">If there is no preceding version, an error will occur.</span></span> <span data-ttu-id="ad6ff-129"><strong>DFMode</strong> で指定するバージョンが使用可能なバージョンよりも古い場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-129">If <strong>DFMode</strong> is less than the available version, an error will occur.</span></span> <span data-ttu-id="ad6ff-130">このプロパティは、接続後は値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-130">This property is read-only after a connection is made.</span></span> <span data-ttu-id="ad6ff-131">次の文字列値のいずれかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-131">Can be one of the following valid string values:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="ad6ff-132">&quot;25&quot; -バージョン 2.5 (既定値)</span><span class="sxs-lookup"><span data-stu-id="ad6ff-132">&quot;25&quot; — Version 2.5 (Default)</span></span></p></li>
<li><p><span data-ttu-id="ad6ff-133">&quot;21&quot; -バージョン2.1</span><span class="sxs-lookup"><span data-stu-id="ad6ff-133">&quot;21&quot; — Version 2.1</span></span></p></li>
<li><p><span data-ttu-id="ad6ff-134">&quot;20&quot; -バージョン2.0</span><span class="sxs-lookup"><span data-stu-id="ad6ff-134">&quot;20&quot; — Version 2.0</span></span></p></li>
<li><p><span data-ttu-id="ad6ff-135">&quot;15&quot; -バージョン1.5</span><span class="sxs-lookup"><span data-stu-id="ad6ff-135">&quot;15&quot; — Version 1.5</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad6ff-136"><strong>Command Properties</strong></span><span class="sxs-lookup"><span data-stu-id="ad6ff-136"><strong>Command Properties</strong></span></span></p></td>
<td><p><span data-ttu-id="ad6ff-p105">MS Remote プロバイダーがサーバーに送信するコマンドの文字列 (行セット) プロパティに追加する値を示します。この文字列の既定値は vt_empty です。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-p105">Indicates values that will be added to the string of command (rowset) properties sent to the server by the MS Remote provider. The default value for this string is vt_empty.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad6ff-139"><strong>Current DFMode</strong></span><span class="sxs-lookup"><span data-stu-id="ad6ff-139"><strong>Current DFMode</strong></span></span></p></td>
<td><p><span data-ttu-id="ad6ff-140">サーバー上の <strong>DataFactory</strong> の実際のバージョン番号を示します。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-140">Indicates the actual version number of the <strong>DataFactory</strong> on the server.</span></span> <span data-ttu-id="ad6ff-141"><strong>DFMode</strong> プロパティで要求したバージョンが受け付けられたかどうかを調べるには、このプロパティを確認します。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-141">Check this property to see if the version requested in the <strong>DFMode</strong> property was honored.</span></span> <span data-ttu-id="ad6ff-142">次の有効な長整数型 (Long) の値のいずれかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-142">Can be one of the following valid Long integer values:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="ad6ff-143">25 - Version 2.5 (既定)</span><span class="sxs-lookup"><span data-stu-id="ad6ff-143">25 — Version 2.5 (Default)</span></span></p></li>
<li><p><span data-ttu-id="ad6ff-144">21 - Version 2.1</span><span class="sxs-lookup"><span data-stu-id="ad6ff-144">21 — Version 2.1</span></span></p></li>
<li><p><span data-ttu-id="ad6ff-145">20 - Version 2.0</span><span class="sxs-lookup"><span data-stu-id="ad6ff-145">20 — Version 2.0</span></span></p></li>
<li><p><span data-ttu-id="ad6ff-146">15 - Version 1.5</span><span class="sxs-lookup"><span data-stu-id="ad6ff-146">15 — Version 1.5</span></span></p></li>
</ul>
<p></p>
<p><span data-ttu-id="ad6ff-147">DFMode &quot;の追加 = 20;&quot; <strong>msremote</strong> provider を使用する場合は、接続文字列にデータを更新するときのサーバーのパフォーマンスを向上させることができます。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-147">Adding &quot;DFMode=20;&quot; to your connection string when using the <strong>MSRemote</strong> provider can improve your server's performance when updating data.</span></span> <span data-ttu-id="ad6ff-148">この設定によって、サーバー上の <strong>RDSServer.DataFactory</strong> オブジェクトはリソース消費量の少ないモードを使用します。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-148">With this setting, the <strong>RDSServer.DataFactory</strong> object on the server uses a less resource-intensive mode.</span></span> <span data-ttu-id="ad6ff-149">ただし、この設定では次の機能は使用できません。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-149">However, the following features are not available in this configuration:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="ad6ff-150">パラメーター クエリを使用する。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-150">Using parameterized queries.</span></span></p></li>
<li><p><span data-ttu-id="ad6ff-151"><strong>Execute</strong> メソッドを呼び出す前に、パラメーターまたは列の情報を取得する。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-151">Getting parameter or column information before calling the <strong>Execute</strong> method.</span></span></p></li>
<li><p><span data-ttu-id="ad6ff-152"><strong>Transact Updates</strong> を <strong>True</strong> に設定する。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-152">Setting <strong>Transact Updates</strong> to <strong>True</strong>.</span></span></p></li>
<li><p><span data-ttu-id="ad6ff-153">行のステータスを取得する。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-153">Getting row status.</span></span></p></li>
<li><p><span data-ttu-id="ad6ff-154"><strong>Resync</strong> メソッドを呼び出す。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-154">Calling the <strong>Resync</strong> method.</span></span></p></li>
<li><p><span data-ttu-id="ad6ff-155"><strong>Update Resync</strong> プロパティによって明示的または自動的に更新する。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-155">Refreshing (explicitly or automatically) via the <strong>Update Resync</strong> property.</span></span></p></li>
<li><p><span data-ttu-id="ad6ff-156"><strong>Command</strong> プロパティまたは <strong>Recordset</strong> プロパティを設定する。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-156">Setting <strong>Command</strong> or <strong>Recordset</strong> properties.</span></span></p></li>
<li><p><span data-ttu-id="ad6ff-157"><strong>adCmdTableDirect</strong> を使用する。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-157">Using <strong>adCmdTableDirect</strong>.</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad6ff-158"><strong>ハンドラー</strong></span><span class="sxs-lookup"><span data-stu-id="ad6ff-158"><strong>Handler</strong></span></span></p></td>
<td><p><span data-ttu-id="ad6ff-159"><a href="datafactory-object-rdsserver.md">rdsserver.datafactory</a>の機能を拡張するサーバー側のカスタマイズプログラム (またはハンドラー) の名前と、そのハンドラーで使用されるすべてのパラメーター<em>を</em>コンマ (&quot;,&quot;) で区切って指定します。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-159">Indicates the name of a server-side customization program (or handler) that extends the functionality of the <a href="datafactory-object-rdsserver.md">RDSServer.DataFactory</a>, and any parameters used by the handler<em>,</em> all separated by commas (&quot;,&quot;).</span></span> <span data-ttu-id="ad6ff-160">文字列型 ( <strong>String</strong> ) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-160">A <strong>String</strong> value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad6ff-161"><strong>Internet Timeout</strong></span><span class="sxs-lookup"><span data-stu-id="ad6ff-161"><strong>Internet Timeout</strong></span></span></p></td>
<td><p><span data-ttu-id="ad6ff-162">サーバーとの間で要求をやり取りするときの最大待ち時間をミリ秒単位で示します。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-162">Indicates the maximum number of milliseconds to wait for a request to travel to and from the server.</span></span> <span data-ttu-id="ad6ff-163">既定値は 5 分です。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-163">(The default is 5 minutes.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad6ff-164"><strong>Remote Provider</strong></span><span class="sxs-lookup"><span data-stu-id="ad6ff-164"><strong>Remote Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="ad6ff-165">リモート サーバーで使用されるデータ プロバイダーの名前を示します。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-165">Indicates the name of the data provider to be used on the remote server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad6ff-166"><strong>Remote Server</strong></span><span class="sxs-lookup"><span data-stu-id="ad6ff-166"><strong>Remote Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ad6ff-p110">この接続で使用されるサーバー名および通信プロトコルを示します。このプロパティは、<a href="datacontrol-object-rds.md">RDS.DataControl</a> オブジェクトの <a href="server-property-rds.md">Server</a> プロパティと同等です。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-p110">Indicates the server name and communication protocol to be used by this connection. This property is equivalent to the <a href="datacontrol-object-rds.md">RDS.DataControl</a> object <a href="server-property-rds.md">Server</a> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad6ff-169"><strong>Transact Updates</strong></span><span class="sxs-lookup"><span data-stu-id="ad6ff-169"><strong>Transact Updates</strong></span></span></p></td>
<td><p><span data-ttu-id="ad6ff-p111">True に設定すると、<a href="updatebatch-method-ado.md">UpdateBatch</a> がサーバー上で実行されたときに、トランザクション内で処理が行われることを示します。このブール型 (Boolean) の動的プロパティの既定値は False です。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-p111">When set to True, this value indicates that when <a href="updatebatch-method-ado.md">UpdateBatch</a> is performed on the server, it will be done inside a transaction. The default value for this Boolean dynamic property is False.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ad6ff-p112">値の設定が可能な動的プロパティは、プロパティ名を接続文字列のキーワードとして指定して設定することもできます。たとえば、 **Internet Timeout** 動的プロパティを 5 秒に設定するには、次のように指定します。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-p112">You may also set writable dynamic properties by specifying their names as keywords in the connection string. For example, set the **Internet Timeout** dynamic property to five seconds by specifying:</span></span>

```sql 
 
Dim cn as New ADODB.Connection 
cn.Open "Provider=MS Remote;Internet Timeout=5000" 
```

<span data-ttu-id="ad6ff-p113">動的プロパティの名前を **Properties** プロパティのインデックスとして指定して、動的プロパティを設定または取得することもできます。たとえば、 **Internet Timeout** 動的プロパティの値を取得して出力した後、新しい値を設定するには、次のように指定します。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-p113">You may also set or retrieve a dynamic property by specifying its name as the index to the **Properties** property. For example, get and print the current value of the **Internet Timeout** dynamic property, and then set a new value, like this:</span></span>

```sql 
 
Debug.Print cn.Properties("Internet Timeout") 
cn.Properties("Internet Timeout") = 5000 
```

## <a name="remarks"></a><span data-ttu-id="ad6ff-176">注釈</span><span class="sxs-lookup"><span data-stu-id="ad6ff-176">Remarks</span></span>

<span data-ttu-id="ad6ff-p114">ADO 2.0 では、OLE DB Remoting Provider は、[Recordset](recordset-object-ado.md) オブジェクトの **Open** メソッドの *ActiveConnection* パラメーターでのみ指定できます。ADO 2.1 以降では、[Connection](connection-object-ado.md) オブジェクトの **Open** メソッドの *ConnectionString* パラメーターでも、このプロバイダーを指定できます。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-p114">In ADO 2.0, the OLE DB Remoting Provider could only be specified in the *ActiveConnection* parameter of the [Recordset](recordset-object-ado.md) object **Open** method. Starting with ADO 2.1, the provider may also be specified in the *ConnectionString* parameter of the [Connection](connection-object-ado.md) object **Open** method.</span></span>

<span data-ttu-id="ad6ff-179">**RDS.DataControl** オブジェクトの [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) プロパティと等価な動的プロパティはありません。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-179">The equivalent of the **RDS.DataControl** object [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) property is not available.</span></span> <span data-ttu-id="ad6ff-180">代わりに、[Recordset](recordset-object-ado.md) オブジェクトの **Open** メソッドの *Source* 引数を使用します。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-180">The [Recordset](recordset-object-ado.md) object **Open** method *Source* argument is used instead.</span></span>

<span data-ttu-id="ad6ff-181">"...;Remote Provider=MS Remote;..." のように指定すると 4 層のシナリオになります。3 層を超えるシナリオについてはテストは行われておらず、必要になることもありません。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-181">Specifying "...;Remote Provider=MS Remote;..." would create a four-tier scenario.Scenarios beyond three tiers have not been tested and should not be needed.</span></span>

## <a name="example"></a><span data-ttu-id="ad6ff-182">例</span><span class="sxs-lookup"><span data-stu-id="ad6ff-182">Example</span></span>

<span data-ttu-id="ad6ff-p116">この例では、*YourServer* という名前のサーバーにある **pubs** データベースの **authors** テーブルに対してクエリを実行します。リモート データ ソース名およびリモート サーバー名は、[Connection](connection-object-ado.md) オブジェクトの [Open](open-method-ado-connection.md) メソッドで指定し、SQL クエリは [Recordset](recordset-object-ado.md) オブジェクトの [Open](open-method-ado-recordset.md) メソッドで指定します。**Recordset** オブジェクトが返され、編集されて、データ ソースの更新に使用されます。</span><span class="sxs-lookup"><span data-stu-id="ad6ff-p116">This example performs a query on the **authors** table of the **pubs** database on a server named, *YourServer*. The names of the remote data source and remote server are provided in the [Connection](connection-object-ado.md) object [Open](open-method-ado-connection.md) method, and the SQL query is specified in the [Recordset](recordset-object-ado.md) object [Open](open-method-ado-recordset.md) method. A **Recordset** object is returned, edited, and used to update the data source.</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
Dim cn as New ADODB.Connection 
cn.Open  "Provider=MS Remote;Data Source=pubs;" & _ 
         "Remote Server=https://YourServer" 
rs.Open "SELECT * FROM authors", cn 
...                'Edit the recordset 
rs.UpdateBatch     'Equivalent of RDS SubmitChanges 
... 
```

