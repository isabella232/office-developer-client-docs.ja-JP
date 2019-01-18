---
title: 接続文字列の作成
TOCTitle: Creating the connection string
ms:assetid: 0d34b1c6-bf2e-1299-9778-573ccd2da1c7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248853(v=office.15)
ms:contentKeyID: 48543214
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f43207edec0c0acb58c66318e5dc7668a28ea595
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719919"
---
# <a name="creating-the-connection-string"></a>接続文字列の作成

**適用されます**Access 2013、Office 2013。

ADO では、接続文字列内の 5 つの引数が直接サポートされています。その他の引数は、ADO によって処理されることなく、*Provider* 引数で指定されたプロバイダーに渡されます。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>引数</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Provider</em></p></td>
<td><p>接続に使用するプロバイダーの名前を指定します。</p></td>
</tr>
<tr class="even">
<td><p><em>ファイル名</em></p></td>
<td><p>設定済みの接続情報を格納したプロバイダー固有のファイル (たとえば、持続的なデータ ソース オブジェクト) の名前を指定します。</p></td>
</tr>
<tr class="odd">
<td><p><em>URL</em></p></td>
<td><p>接続文字列を、ファイルやディレクトリなどのリソースを識別する絶対 URL として指定します。</p></td>
</tr>
<tr class="even">
<td><p><em>Remote Provider</em></p></td>
<td><p>クライアント側の接続を開くときに使用するプロバイダーの名前を指定します (Remote Data Service のみ)。</p></td>
</tr>
<tr class="odd">
<td><p><em>Remote Server</em></p></td>
<td><p>クライアント側の接続を開くときに使用するサーバーのパス名を指定します (リモート データ サービスのみ)。</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> 次の例では、「ADO プログラマ ガイドでは"MyId"、パスワード"123 abc"のユーザー id は、サーバーに対して認証するために使用されます。 これらの値を、使用するサーバーの有効なログイン時の資格情報に置き換える必要があります。 また、"MySqlServer" は、使用するサーバーの名前に置き換えます。

1 章の HelloData アプリケーションでは、次の接続文字列が使用されていました。

```vb 
 
m_sConnStr = "Provider='SQLOLEDB';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Northwind';Integrated Security='SSPI';" 
```

唯一の ADO パラメーターがこの接続文字列で指定された"プロバイダー SQLOLEDB を ="、SQL Server の Microsoft OLE DB プロバイダーを指定します。 接続文字列で渡すことができるその他の有効なパラメーターは、各プロバイダーのマニュアルを参照して判断できます。 に従って、OLE DB プロバイダーの SQL Server のマニュアル、*初期カタログ*パラメーターの*データ ソース*のパラメーターおよび [データベース] の [サーバー] を置き換えることができます。 したがって、次の接続文字列は、最初と同じ結果を生成しました。

```vb 
 
m_sConnStr = "Provider='SQLOLEDB';Server='MySqlServer';" & _ 
 "Database='Northwind';Integrated Security='SSPI';" 
```

接続を開くには、次に示すように、 **Connection** オブジェクトの **Open** メソッドの最初の引数として接続文字列を渡すだけです。

```vb 
 
objConn.Open m_sConnStr 
```

接続を開く前に **Connection** オブジェクトのプロパティを設定することにより、接続文字列の情報の大部分を指定することもできます。たとえば、次のコードを使用して、前の接続文字列と同じ結果を得ることができます。

```vb 
 
With objConn 
 .Provider = "SQLOLEDB" 
 .DefaultDatabase = "Northwind" 
 .Properties("Data Source") = "MySqlServer" 
 .Properties("Integrated Security") = "SSPI" 
 .Open 
End With 
```

