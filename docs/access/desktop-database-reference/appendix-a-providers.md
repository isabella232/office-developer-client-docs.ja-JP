---
title: '付録 A: プロバイダー'
TOCTitle: 'Appendix A: Providers'
ms:assetid: b3f92279-8d66-ad59-71c4-c0448168125a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249857(v=office.15)
ms:contentKeyID: 48547207
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f18af92724ff87263808cba2e8799bca2a558541
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861444"
---
# <a name="appendix-a-providers"></a>付録 A: プロバイダー


**適用されます**Access 2013 |。Office 2013


このセクションでは、次の 3 つの種類のプロバイダー: データ プロバイダー、サービス プロバイダー、およびサービスのコンポーネントです。 プロバイダーは、2 つのカテゴリに分類されます: データとサービスを提供するものです。 *データ プロバイダー*は、独自のデータを所有し、表形式でアプリケーションに公開します。 *サービス プロバイダー*では、作成や、ADO アプリケーションの機能を強化して、データの利用によってサービスをカプセル化します。 として*サービスのコンポーネント*、その他のサービス プロバイダーまたはコンポーネントと連携して動作するサービス プロバイダーはさらに定義も可能性があります。

## <a name="data-providers"></a>データ プロバイダー

ADO は高性能で柔軟性に富んでおり、使用するプロバイダーの機能に関係なく、種類の異なる複数のデータ プロバイダーに接続した場合でも、同じプログラミング モデルを提供できます。

ただし、各データ プロバイダーはそれぞれ異なるので、アプリケーションと ADO の間でどのようなやり取りが行われるかは、データ プロバイダーごとに少しずつ異なります。この相違点は、通常、次の 3 つのカテゴリのいずれかに分類されます。

  - [ConnectionString](connectionstring-property-ado.md) プロパティの接続パラメーター

  - [Command](command-object-ado.md) オブジェクトの使用方法

  - プロバイダー固有の [Recordset](recordset-object-ado.md) の動作

Microsoft から現在入手可能な各データ プロバイダーの詳細については、次の各トピックを参照してください。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>対象</p></th>
<th><p>トピック</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>ODBC データベース</p></td>
<td><p><a href="microsoft-ole-db-provider-for-odbc.md">Microsoft OLE DB Provider for ODBC</a></p></td>
</tr>
<tr class="even">
<td><p>Microsoft インデックス サービス</p></td>
<td><p><a href="microsoft-ole-db-provider-for-microsoft-indexing-service.md">Microsoft OLE DB Provider for Microsoft Indexing Service</a></p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Active Directory サービス</p></td>
<td><p><a href="microsoft-ole-db-provider-for-microsoft-active-directory-service.md">Microsoft OLE DB Provider for Microsoft Active Directory Service</a></p></td>
</tr>
<tr class="even">
<td><p>Microsoft Jet データベース</p></td>
<td><p><a href="microsoft-ole-db-provider-for-microsoft-jet.md">Microsoft OLE DB Provider for Microsoft Jet</a></p></td>
</tr>
<tr class="odd">
<td><p>Microsoft SQL Server</p></td>
<td><p><a href="microsoft-ole-db-provider-for-sql-server.md">Microsoft OLE DB Provider for SQL Server</a></p></td>
</tr>
<tr class="even">
<td><p>Oracle データベース</p></td>
<td><p><a href="microsoft-ole-db-provider-for-oracle.md">Microsoft OLE DB Provider for Oracle</a></p></td>
</tr>
<tr class="odd">
<td><p>Internet Publishing</p></td>
<td><p><a href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</a></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-dynamic-properties"></a>プロバイダー固有の動的プロパティ

[Connection](properties-collection-ado.md) オブジェクト、 [Command](connection-object-ado.md) オブジェクト、および [Recordset](command-object-ado.md) オブジェクトの [Properties](recordset-object-ado.md) コレクションには、プロバイダー固有の動的プロパティが含まれています。これらのプロパティにより、ADO がサポートする組み込みプロパティでは入手できない、プロバイダー固有の機能に関する情報を入手できます。

接続を確立してこれらのオブジェクトを作成した後、オブジェクトの [Properties](refresh-method-ado.md) コレクションに対して **Refresh** メソッドを使用して、プロバイダー固有のプロパティを取得できます。プロバイダー固有の動的プロパティの詳細については、各プロバイダーのマニュアルおよび「OLE DB Programmer's Reference」を参照してください。

## <a name="service-providers"></a>サービス プロバイダー

サービス プロバイダーを使用するには、キーワードを指定する必要があります。また、各サービス プロバイダーに関連付けられたプロバイダー固有の動的プロパティを理解しておく必要があります。Microsoft から現在入手可能な各サービス プロバイダーの詳細については、次の各トピックを参照してください。

  - [Microsoft Data Shaping Service for OLE DB (ADO サービス プロバイダー)](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md)

  - [Microsoft OLE DB Persistence Provider (ADO サービス プロバイダー)](microsoft-ole-db-persistence-provider-ado-service-provider.md)

  - [Microsoft OLE DB Remoting Provider (ADO サービス プロバイダー)](microsoft-ole-db-remoting-provider-ado-service-provider.md)

## <a name="service-components"></a>サービス コンポーネント

[Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) サービス コンポーネントは、データ プロバイダーのカーソル サポート機能を補完します。また、サービス コンポーネントはキーワードを必要とし、動的プロパティを持ちます。

プロバイダーの詳細については、Microsoft Data Access Components SDK の Microsoft OLE DB のマニュアルまたは「[データ プラットフォーム デベロッパー センター](https://msdn.microsoft.com/data/default.aspx)」を参照してください。

## <a name="provider-commands"></a>プロバイダーのコマンド

プロバイダーごとに一覧表示、アプリケーションがプロバイダーのコマンドとして SQL ステートメントを入力するユーザーを許可する場合、常にユーザー入力を検証し、警戒をハッカーの攻撃の一部としてなど、危険性のある SQL ステートメントを使用して、ユーザーが入力します。

