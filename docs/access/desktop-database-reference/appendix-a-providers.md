---
title: '付録 A: プロバイダー'
TOCTitle: 'Appendix A: Providers'
ms:assetid: b3f92279-8d66-ad59-71c4-c0448168125a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249857(v=office.15)
ms:contentKeyID: 48547207
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 45416c68d52a2ba20ba9adfa19a6ebd89d1e0240
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026205"
---
# <a name="appendix-a-providers"></a><span data-ttu-id="39bcc-102">付録 A: プロバイダー</span><span class="sxs-lookup"><span data-stu-id="39bcc-102">Appendix A: Providers</span></span>


<span data-ttu-id="39bcc-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="39bcc-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="39bcc-104">このセクションでは、次の 3 つの種類のプロバイダー: データ プロバイダー、サービス プロバイダー、およびサービスのコンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="39bcc-104">This section addresses three kinds of providers: data providers, service providers, and service components.</span></span> <span data-ttu-id="39bcc-105">プロバイダーは、2 つのカテゴリに分類されます: データとサービスを提供するものです。</span><span class="sxs-lookup"><span data-stu-id="39bcc-105">Providers fall into two categories: those providing data and those providing services.</span></span> <span data-ttu-id="39bcc-106">*データ プロバイダー*は、独自のデータを所有し、表形式でアプリケーションに公開します。</span><span class="sxs-lookup"><span data-stu-id="39bcc-106">A *data provider* owns its own data and exposes it in tabular form to your application.</span></span> <span data-ttu-id="39bcc-107">*サービス プロバイダー*では、作成や、ADO アプリケーションの機能を強化して、データの利用によってサービスをカプセル化します。</span><span class="sxs-lookup"><span data-stu-id="39bcc-107">A *service provider* encapsulates a service by producing and consuming data, augmenting features in your ADO applications.</span></span> <span data-ttu-id="39bcc-108">として*サービスのコンポーネント*、その他のサービス プロバイダーまたはコンポーネントと連携して動作するサービス プロバイダーはさらに定義も可能性があります。</span><span class="sxs-lookup"><span data-stu-id="39bcc-108">A service provider may also be further defined as a *service component*, which must work in conjunction with other service providers or components.</span></span>

## <a name="data-providers"></a><span data-ttu-id="39bcc-109">データ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="39bcc-109">Data providers</span></span>

<span data-ttu-id="39bcc-110">ADO は高性能で柔軟性に富んでおり、使用するプロバイダーの機能に関係なく、種類の異なる複数のデータ プロバイダーに接続した場合でも、同じプログラミング モデルを提供できます。</span><span class="sxs-lookup"><span data-stu-id="39bcc-110">ADO is powerful and flexible because it can connect to any of several different data providers and still expose the same programming model, regardless of the specific features of any given provider.</span></span>

<span data-ttu-id="39bcc-p102">ただし、各データ プロバイダーはそれぞれ異なるので、アプリケーションと ADO の間でどのようなやり取りが行われるかは、データ プロバイダーごとに少しずつ異なります。この相違点は、通常、次の 3 つのカテゴリのいずれかに分類されます。</span><span class="sxs-lookup"><span data-stu-id="39bcc-p102">However, because each data provider is unique, how your application interacts with ADO will vary slightly by data provider. The differences usually fall into one of three categories:</span></span>

- <span data-ttu-id="39bcc-113">[ConnectionString](connectionstring-property-ado.md) プロパティの接続パラメーター</span><span class="sxs-lookup"><span data-stu-id="39bcc-113">Connection parameters in the [ConnectionString](connectionstring-property-ado.md) property.</span></span>

- <span data-ttu-id="39bcc-114">[Command](command-object-ado.md) オブジェクトの使用方法</span><span class="sxs-lookup"><span data-stu-id="39bcc-114">[Command](command-object-ado.md) object usage.</span></span>

- <span data-ttu-id="39bcc-115">プロバイダー固有の [Recordset](recordset-object-ado.md) の動作</span><span class="sxs-lookup"><span data-stu-id="39bcc-115">Provider-specific [Recordset](recordset-object-ado.md) behavior.</span></span>

<span data-ttu-id="39bcc-116">Microsoft から現在入手可能な各データ プロバイダーの詳細については、次の各トピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="39bcc-116">Details for each of the data providers currently available from Microsoft are listed as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="39bcc-117">対象</span><span class="sxs-lookup"><span data-stu-id="39bcc-117">Area</span></span></p></th>
<th><p><span data-ttu-id="39bcc-118">トピック</span><span class="sxs-lookup"><span data-stu-id="39bcc-118">Topic</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="39bcc-119">ODBC データベース</span><span class="sxs-lookup"><span data-stu-id="39bcc-119">ODBC databases</span></span></p></td>
<td><p><span data-ttu-id="39bcc-120"><a href="microsoft-ole-db-provider-for-odbc.md">Microsoft OLE DB Provider for ODBC</a></span><span class="sxs-lookup"><span data-stu-id="39bcc-120"><a href="microsoft-ole-db-provider-for-odbc.md">Microsoft OLE DB Provider for ODBC</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39bcc-121">Microsoft インデックス サービス</span><span class="sxs-lookup"><span data-stu-id="39bcc-121">Microsoft Indexing Service</span></span></p></td>
<td><p><span data-ttu-id="39bcc-122"><a href="microsoft-ole-db-provider-for-microsoft-indexing-service.md">Microsoft OLE DB Provider for Microsoft Indexing Service</a></span><span class="sxs-lookup"><span data-stu-id="39bcc-122"><a href="microsoft-ole-db-provider-for-microsoft-indexing-service.md">Microsoft OLE DB Provider for Microsoft Indexing Service</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39bcc-123">Microsoft Active Directory サービス</span><span class="sxs-lookup"><span data-stu-id="39bcc-123">Microsoft Active Directory Service</span></span></p></td>
<td><p><span data-ttu-id="39bcc-124"><a href="microsoft-ole-db-provider-for-microsoft-active-directory-service.md">Microsoft OLE DB Provider for Microsoft Active Directory Service</a></span><span class="sxs-lookup"><span data-stu-id="39bcc-124"><a href="microsoft-ole-db-provider-for-microsoft-active-directory-service.md">Microsoft OLE DB Provider for Microsoft Active Directory Service</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39bcc-125">Microsoft Jet データベース</span><span class="sxs-lookup"><span data-stu-id="39bcc-125">Microsoft Jet databases</span></span></p></td>
<td><p><span data-ttu-id="39bcc-126"><a href="microsoft-ole-db-provider-for-microsoft-jet.md">Microsoft OLE DB Provider for Microsoft Jet</a></span><span class="sxs-lookup"><span data-stu-id="39bcc-126"><a href="microsoft-ole-db-provider-for-microsoft-jet.md">Microsoft OLE DB Provider for Microsoft Jet</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39bcc-127">Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="39bcc-127">Microsoft SQL Server</span></span></p></td>
<td><p><span data-ttu-id="39bcc-128"><a href="microsoft-ole-db-provider-for-sql-server.md">Microsoft OLE DB Provider for SQL Server</a></span><span class="sxs-lookup"><span data-stu-id="39bcc-128"><a href="microsoft-ole-db-provider-for-sql-server.md">Microsoft OLE DB Provider for SQL Server</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39bcc-129">Oracle データベース</span><span class="sxs-lookup"><span data-stu-id="39bcc-129">Oracle databases</span></span></p></td>
<td><p><span data-ttu-id="39bcc-130"><a href="microsoft-ole-db-provider-for-oracle.md">Microsoft OLE DB Provider for Oracle</a></span><span class="sxs-lookup"><span data-stu-id="39bcc-130"><a href="microsoft-ole-db-provider-for-oracle.md">Microsoft OLE DB Provider for Oracle</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39bcc-131">Internet Publishing</span><span class="sxs-lookup"><span data-stu-id="39bcc-131">Internet Publishing</span></span></p></td>
<td><p><span data-ttu-id="39bcc-132"><a href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</a></span><span class="sxs-lookup"><span data-stu-id="39bcc-132"><a href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</a></span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-dynamic-properties"></a><span data-ttu-id="39bcc-133">プロバイダー固有の動的プロパティ</span><span class="sxs-lookup"><span data-stu-id="39bcc-133">Provider-specific dynamic properties</span></span>

<span data-ttu-id="39bcc-p103">[Connection](properties-collection-ado.md) オブジェクト、 [Command](connection-object-ado.md) オブジェクト、および [Recordset](command-object-ado.md) オブジェクトの [Properties](recordset-object-ado.md) コレクションには、プロバイダー固有の動的プロパティが含まれています。これらのプロパティにより、ADO がサポートする組み込みプロパティでは入手できない、プロバイダー固有の機能に関する情報を入手できます。</span><span class="sxs-lookup"><span data-stu-id="39bcc-p103">The [Properties](properties-collection-ado.md) collections of the [Connection](connection-object-ado.md), [Command](command-object-ado.md), and [Recordset](recordset-object-ado.md) objects include dynamic properties specific to the provider. These properties provide information about functionality specific to the provider beyond the built-in properties that ADO supports.</span></span>

<span data-ttu-id="39bcc-p104">接続を確立してこれらのオブジェクトを作成した後、オブジェクトの [Properties](refresh-method-ado.md) コレクションに対して **Refresh** メソッドを使用して、プロバイダー固有のプロパティを取得できます。プロバイダー固有の動的プロパティの詳細については、各プロバイダーのマニュアルおよび「OLE DB Programmer's Reference」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39bcc-p104">After establishing the connection and creating these objects, use the [Refresh](refresh-method-ado.md) method on the object's **Properties** collection to obtain the provider-specific properties. Refer to the provider documentation and the OLE DB Programmer's Reference for detailed information about these dynamic properties.</span></span>

## <a name="service-providers"></a><span data-ttu-id="39bcc-138">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="39bcc-138">Service providers</span></span>

<span data-ttu-id="39bcc-p105">サービス プロバイダーを使用するには、キーワードを指定する必要があります。また、各サービス プロバイダーに関連付けられたプロバイダー固有の動的プロパティを理解しておく必要があります。Microsoft から現在入手可能な各サービス プロバイダーの詳細については、次の各トピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="39bcc-p105">To use a service provider, you must supply a keyword. You should also be aware of the provider-specific dynamic properties associated with each service provider. Provider-specific details are listed for each of the service providers currently available from Microsoft:</span></span>

- [<span data-ttu-id="39bcc-142">Microsoft Data Shaping Service for OLE DB (ADO サービス プロバイダー)</span><span class="sxs-lookup"><span data-stu-id="39bcc-142">Microsoft Data Shaping Service for OLE DB</span></span>](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md)

- [<span data-ttu-id="39bcc-143">Microsoft OLE DB Persistence Provider (ADO サービス プロバイダー)</span><span class="sxs-lookup"><span data-stu-id="39bcc-143">Microsoft OLE DB Persistence Provider</span></span>](microsoft-ole-db-persistence-provider-ado-service-provider.md)

- [<span data-ttu-id="39bcc-144">Microsoft OLE DB Remoting Provider (ADO サービス プロバイダー)</span><span class="sxs-lookup"><span data-stu-id="39bcc-144">Microsoft OLE DB Remoting Provider</span></span>](microsoft-ole-db-remoting-provider-ado-service-provider.md)

## <a name="service-components"></a><span data-ttu-id="39bcc-145">サービス コンポーネント</span><span class="sxs-lookup"><span data-stu-id="39bcc-145">Service components</span></span>

<span data-ttu-id="39bcc-p106">[Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) サービス コンポーネントは、データ プロバイダーのカーソル サポート機能を補完します。また、サービス コンポーネントはキーワードを必要とし、動的プロパティを持ちます。</span><span class="sxs-lookup"><span data-stu-id="39bcc-p106">The [Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) service component supplements the cursor support functions of data providers. It also requires a keyword and has dynamic properties.</span></span>

<span data-ttu-id="39bcc-148">プロバイダーの詳細については、Microsoft Data Access Components SDK の Microsoft OLE DB のマニュアルまたは「[データ プラットフォーム デベロッパー センター](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39bcc-148">For more information about providers, see the documentation for Microsoft OLE DB in the Microsoft Data Access Components SDK or visit the [Data Platform Developer Center](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span></span>

## <a name="provider-commands"></a><span data-ttu-id="39bcc-149">プロバイダーのコマンド</span><span class="sxs-lookup"><span data-stu-id="39bcc-149">Provider commands</span></span>

<span data-ttu-id="39bcc-150">プロバイダーごとに一覧表示、アプリケーションがプロバイダーのコマンドとして SQL ステートメントを入力するユーザーを許可する場合、常にユーザー入力を検証し、警戒をハッカーの攻撃の一部としてなど、危険性のある SQL ステートメントを使用して、ユーザーが入力します。</span><span class="sxs-lookup"><span data-stu-id="39bcc-150">For each provider listed here, if your applications allow users to enter SQL statements as the provider commands, you must always validate the user input and be vigilant of possible hacker attacks using potentially dangerous SQL statement, such as, , as part of the user input.</span></span>

