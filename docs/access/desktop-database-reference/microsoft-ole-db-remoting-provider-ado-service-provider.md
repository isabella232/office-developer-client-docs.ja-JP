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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701901"
---
# <a name="microsoft-ole-db-remoting-provider-ado-service-provider"></a>Microsoft OLE DB Remoting Provider (ADO サービス プロバイダー)

**適用されます**Access 2013、Office 2013。

Microsoft OLE DB Remoting Provider を使用すると、クライアント コンピューター上のローカル ユーザーはリモート コンピューターのデータ プロバイダーを呼び出すことができます。リモート コンピューターのローカル ユーザーと同じように、リモート コンピューターのデータ プロバイダー パラメーターを指定します。次に、リモート コンピューターにアクセスするために Remoting Provider で使用するパラメーターを指定します。これによって、ローカル ユーザーと同じようにリモート コンピューターにアクセスすることができます。

## <a name="provider-keyword"></a>プロバイダー キーワード

OLE DB Remoting Provider を呼び出すには、接続文字列で次のキーワードと値を指定します。プロバイダー名に含まれるスペースに注意してください。

```sql 
 
"Provider=MS Remote" 
```

## <a name="additional-keywords"></a>その他のキーワード

このサービス プロバイダーを呼び出す場合は、次に示すキーワードも指定できます。

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
<td><p><strong>Data Source</strong></p></td>
<td><p>リモート データ ソースの名前を指定します。 処理のため、OLE DB リモート プロバイダーに渡されます。 このキーワードは <a href="datacontrol-object-rds.md">RDS.DataControl</a> オブジェクトの <a href="connect-property-rds.md">Connect</a> プロパティと同等です。</p></td>
</tr>
</tbody>
</table>


## <a name="dynamic-properties"></a>動的プロパティ

このサービス プロバイダーを呼び出すと、次に示す動的プロパティが [Connection](connection-object-ado.md) オブジェクトの [Properties](properties-collection-ado.md) コレクションに追加されます。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>動的プロパティ名</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>DFMode</strong></p></td>
<td><p>DataFactory モードを示します。 サーバー上の<a href="datafactory-object-rdsserver.md">DataFactory</a>オブジェクトの適切なバージョンを指定する文字列です。 <strong>DataFactory</strong>の特定のバージョンの要求への接続を開く前にこのプロパティを設定します。 要求されたバージョンが使用できない場合は、しようとしましたはする前のバージョンを使用します。 前のバージョンがない場合、エラーが発生します。 <strong>DFMode</strong>が利用可能なバージョンよりも小さい場合は、エラーが発生します。 このプロパティは、接続が確立した後は読み取り専用です。 次の文字列値のいずれかを指定できます。</p>
<p></p>
<ul>
<li><p>&quot;25&quot; -version 2.5 (既定値)</p></li>
<li><p>&quot;21&quot; -バージョン 2.1</p></li>
<li><p>&quot;20&quot; -バージョン 2.0</p></li>
<li><p>&quot;15&quot; -バージョン 1.5</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Command Properties</strong></p></td>
<td><p>MS Remote プロバイダーがサーバーに送信するコマンドの文字列 (行セット) プロパティに追加する値を示します。この文字列の既定値は vt_empty です。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Current DFMode</strong></p></td>
<td><p>サーバー上の<strong>DataFactory</strong>の実際のバージョン番号を示します。 <strong>DFMode</strong>プロパティで要求したバージョンが受け付けられたかどうかに表示するには、このプロパティを確認します。 次の有効な長整数型 (Long) の値のいずれかを指定できます。</p>
<p></p>
<ul>
<li><p>25 - Version 2.5 (既定)</p></li>
<li><p>21 - Version 2.1</p></li>
<li><p>20 - Version 2.0</p></li>
<li><p>15 - Version 1.5</p></li>
</ul>
<p></p>
<p>追加&quot;DFMode = 20;&quot;の接続に<strong>MSRemote</strong>プロバイダーを使用するときに文字列ことができますパフォーマンスを向上させる、サーバーのデータを更新するときです。 この設定によって、サーバー上の <strong>RDSServer.DataFactory</strong> オブジェクトはリソース消費量の少ないモードを使用します。 ただし、この設定では次の機能は使用できません。</p>
<p></p>
<ul>
<li><p>パラメーター クエリを使用する。</p></li>
<li><p><strong>Execute</strong> メソッドを呼び出す前に、パラメーターまたは列の情報を取得する。</p></li>
<li><p><strong>Transact Updates</strong> を <strong>True</strong> に設定する。</p></li>
<li><p>行のステータスを取得する。</p></li>
<li><p><strong>Resync</strong> メソッドを呼び出す。</p></li>
<li><p><strong>Update Resync</strong> プロパティによって明示的または自動的に更新する。</p></li>
<li><p><strong>Command</strong> プロパティまたは <strong>Recordset</strong> プロパティを設定する。</p></li>
<li><p><strong>adCmdTableDirect</strong> を使用する。</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>ハンドラー</strong></p></td>
<td><p><a href="datafactory-object-rdsserver.md">RDSServer.DataFactory</a>のおよびハンドラーによって使用、<em>、</em>すべてコンマで区切られたパラメーターの機能を拡張する、サーバー側のカスタマイズ プログラム (ハンドラー) の名前を示します (&quot;、&quot;)。 文字列型 ( <strong>String</strong> ) の値を返します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Internet Timeout</strong></p></td>
<td><p>サーバーとの間で要求をやり取りするときの最大待ち時間をミリ秒単位で示します。既定値は 5 分です。</p></td>
</tr>
<tr class="even">
<td><p><strong>Remote Provider</strong></p></td>
<td><p>リモート サーバーで使用されるデータ プロバイダーの名前を示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Remote Server</strong></p></td>
<td><p>この接続で使用されるサーバー名および通信プロトコルを示します。このプロパティは、<a href="datacontrol-object-rds.md">RDS.DataControl</a> オブジェクトの <a href="server-property-rds.md">Server</a> プロパティと同等です。</p></td>
</tr>
<tr class="even">
<td><p><strong>Transact Updates</strong></p></td>
<td><p>True に設定すると、<a href="updatebatch-method-ado.md">UpdateBatch</a> がサーバー上で実行されたときに、トランザクション内で処理が行われることを示します。このブール型 (Boolean) の動的プロパティの既定値は False です。</p></td>
</tr>
</tbody>
</table>


値の設定が可能な動的プロパティは、プロパティ名を接続文字列のキーワードとして指定して設定することもできます。たとえば、 **Internet Timeout** 動的プロパティを 5 秒に設定するには、次のように指定します。

```sql 
 
Dim cn as New ADODB.Connection 
cn.Open "Provider=MS Remote;Internet Timeout=5000" 
```

動的プロパティの名前を **Properties** プロパティのインデックスとして指定して、動的プロパティを設定または取得することもできます。たとえば、 **Internet Timeout** 動的プロパティの値を取得して出力した後、新しい値を設定するには、次のように指定します。

```sql 
 
Debug.Print cn.Properties("Internet Timeout") 
cn.Properties("Internet Timeout") = 5000 
```

## <a name="remarks"></a>解説

ADO 2.0 では、OLE DB リモート プロバイダーが[レコード セット](recordset-object-ado.md)オブジェクトの**Open**メソッドの*ActiveConnection*パラメーターにのみ指定します。 ADO 2.1 以降では、プロバイダーも指定できます[Connection](connection-object-ado.md)オブジェクトの**Open**メソッドの*接続文字列*パラメーターで。

**RDS.DataControl** オブジェクトの [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) プロパティと等価な動的プロパティはありません。 [レコード セット](recordset-object-ado.md)オブジェクトの**Open**メソッドの*Source*引数が使用されます。

"...;Remote Provider=MS Remote;..." のように指定すると 4 層のシナリオになります。3 層を超えるシナリオについてはテストは行われておらず、必要になることもありません。

## <a name="example"></a>使用例

この例では、*YourServer* という名前のサーバーにある **pubs** データベースの **authors** テーブルに対してクエリを実行します。リモート データ ソース名およびリモート サーバー名は、[Connection](connection-object-ado.md) オブジェクトの [Open](open-method-ado-connection.md) メソッドで指定し、SQL クエリは [Recordset](recordset-object-ado.md) オブジェクトの [Open](open-method-ado-recordset.md) メソッドで指定します。**Recordset** オブジェクトが返され、編集されて、データ ソースの更新に使用されます。

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

