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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295328"
---
# <a name="creating-the-connection-string"></a><span data-ttu-id="e0d37-102">接続文字列の作成</span><span class="sxs-lookup"><span data-stu-id="e0d37-102">Creating the connection string</span></span>

<span data-ttu-id="e0d37-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="e0d37-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e0d37-p101">ADO では、接続文字列内の 5 つの引数が直接サポートされています。その他の引数は、ADO によって処理されることなく、*Provider* 引数で指定されたプロバイダーに渡されます。</span><span class="sxs-lookup"><span data-stu-id="e0d37-p101">ADO directly supports five arguments in a connection string. Other arguments are passed to the provider that is named in the *Provider* argument without any processing by ADO.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e0d37-106">引数</span><span class="sxs-lookup"><span data-stu-id="e0d37-106">Argument</span></span></p></th>
<th><p><span data-ttu-id="e0d37-107">説明</span><span class="sxs-lookup"><span data-stu-id="e0d37-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e0d37-108"><em>Provider</em></span><span class="sxs-lookup"><span data-stu-id="e0d37-108"><em>Provider</em></span></span></p></td>
<td><p><span data-ttu-id="e0d37-109">接続に使用するプロバイダーの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="e0d37-109">Specifies the name of a provider to use for the connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0d37-110"><em>File Name</em></span><span class="sxs-lookup"><span data-stu-id="e0d37-110"><em>File Name</em></span></span></p></td>
<td><p><span data-ttu-id="e0d37-111">設定済みの接続情報を格納したプロバイダー固有のファイル (たとえば、持続的なデータ ソース オブジェクト) の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="e0d37-111">Specifies the name of a provider-specific file (for example, a persisted data source object) containing preset connection information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0d37-112"><em>URL</em></span><span class="sxs-lookup"><span data-stu-id="e0d37-112"><em>URL</em></span></span></p></td>
<td><p><span data-ttu-id="e0d37-113">接続文字列を、ファイルやディレクトリなどのリソースを識別する絶対 URL として指定します。</span><span class="sxs-lookup"><span data-stu-id="e0d37-113">Specifies the connection string as an absolute URL identifying a resource, such as a file or directory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0d37-114"><em>Remote Provider</em></span><span class="sxs-lookup"><span data-stu-id="e0d37-114"><em>Remote Provider</em></span></span></p></td>
<td><p><span data-ttu-id="e0d37-p102">クライアント側の接続を開くときに使用するプロバイダーの名前を指定します (Remote Data Service のみ)。</span><span class="sxs-lookup"><span data-stu-id="e0d37-p102">Specifies the name of a provider to use when opening a client-side connection. (Remote Data Service only.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0d37-117"><em>Remote Server</em></span><span class="sxs-lookup"><span data-stu-id="e0d37-117"><em>Remote Server</em></span></span></p></td>
<td><p><span data-ttu-id="e0d37-118">クライアント側の接続を開くときに使用するサーバーのパス名を指定します。</span><span class="sxs-lookup"><span data-stu-id="e0d37-118">Specifies the path name of the server to use when opening a client-side connection.</span></span> <span data-ttu-id="e0d37-119">(リモートデータサービスのみ)</span><span class="sxs-lookup"><span data-stu-id="e0d37-119">(Remote Data Service only.)</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="e0d37-120">次の例および「ADO プログラマーズガイド」では、サーバーに対する認証に "123abc" というパスワードを持つユーザー id "MyId" を使用しています。</span><span class="sxs-lookup"><span data-stu-id="e0d37-120">In the following examples and throughout the ADO programmer's guide, the user id "MyId" with a password of "123aBc" is used to authenticate against the server.</span></span> <span data-ttu-id="e0d37-121">これらの値を、使用するサーバーの有効なログイン時の資格情報に置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0d37-121">You should substitute these values with valid login credentials for your server.</span></span> <span data-ttu-id="e0d37-122">また、"MySqlServer" は、使用するサーバーの名前に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="e0d37-122">Also, substitute the name of your server for "MySqlServer".</span></span>

<span data-ttu-id="e0d37-123">1 章の HelloData アプリケーションでは、次の接続文字列が使用されていました。</span><span class="sxs-lookup"><span data-stu-id="e0d37-123">The HelloData application in Chapter 1 used the following connection string:</span></span>

```vb 
 
m_sConnStr = "Provider='SQLOLEDB';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Northwind';Integrated Security='SSPI';" 
```

<span data-ttu-id="e0d37-p105">この接続文字列で指定されている唯一の ADO パラメーターは、"Provider=SQLOLEDB" です。これは、Microsoft OLE DB Provider for SQL Server を表します。接続文字列で渡すことができるその他の有効なパラメーターについては、各プロバイダーのドキュメントを参照してください。OLE DB Provider for SQL Server のドキュメントによると、*Data Source* パラメーターを "Server" に、*Initial Catalog* パラメーターを "Database" に置き換えることができます。したがって、次の接続文字列では、最初の文字列と同じ結果が得られます。</span><span class="sxs-lookup"><span data-stu-id="e0d37-p105">The only ADO parameter supplied in this connection string was "Provider=SQLOLEDB", which indicated the Microsoft OLE DB Provider for SQL Server. Other valid parameters that can be passed in the connection string can be determined by referring to individual providers' documentation. According to the OLE DB Provider for SQL Server documentation, you can substitute "Server" for the *Data Source* parameter and "Database" for the *Initial Catalog* parameter. Thus, the following connection string would produce results identical to the first:</span></span>

```vb 
 
m_sConnStr = "Provider='SQLOLEDB';Server='MySqlServer';" & _ 
 "Database='Northwind';Integrated Security='SSPI';" 
```

<span data-ttu-id="e0d37-128">接続を開くには、次に示すように、**Connection** オブジェクトの **Open** メソッドの最初の引数として接続文字列を渡すだけです。</span><span class="sxs-lookup"><span data-stu-id="e0d37-128">To open the connection, simply pass the connection string as the first argument in the **Connection** object **Open** method:</span></span>

```vb 
 
objConn.Open m_sConnStr 
```

<span data-ttu-id="e0d37-p106">接続を開く前に **Connection** オブジェクトのプロパティを設定することにより、接続文字列の情報の大部分を指定することもできます。たとえば、次のコードを使用して、前の接続文字列と同じ結果を得ることができます。</span><span class="sxs-lookup"><span data-stu-id="e0d37-p106">It is also possible to supply much of this information by setting properties of the **Connection** object before opening the connection. For example, you could achieve the same effect as the connection string above by using the following code:</span></span>

```vb 
 
With objConn 
 .Provider = "SQLOLEDB" 
 .DefaultDatabase = "Northwind" 
 .Properties("Data Source") = "MySqlServer" 
 .Properties("Integrated Security") = "SSPI" 
 .Open 
End With 
```

