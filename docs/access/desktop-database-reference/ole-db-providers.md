---
title: OLE DB プロバイダー (デスクトップ データベース参照のアクセス)
TOCTitle: OLE DB providers
ms:assetid: ef412198-eac5-bf86-73fd-574e67276408
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250215(v=office.15)
ms:contentKeyID: 48548576
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e80df3dad65edb23e7fcd4e6828f2435df405e70
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947778"
---
# <a name="ole-db-providers"></a><span data-ttu-id="15ef5-102">OLE DB プロバイダー</span><span class="sxs-lookup"><span data-stu-id="15ef5-102">OLE DB providers</span></span>


<span data-ttu-id="15ef5-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="15ef5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="15ef5-104">ADO プログラマ ガイド[の紹介](introduction-to-ado-programming.md)では、ADO と Microsoft Data Access アーキテクチャの残りの部分との間の関係について説明します。</span><span class="sxs-lookup"><span data-stu-id="15ef5-104">The ADO programmer's guide [Introduction](introduction-to-ado-programming.md) discusses the relationship between ADO and the rest of the Microsoft Data Access architecture.</span></span> <span data-ttu-id="15ef5-105">OLE DB は、さまざまな情報ソースに格納されているデータに各アプリケーションから同じようにアクセスできる、一連の COM インターフェイスを定義します。</span><span class="sxs-lookup"><span data-stu-id="15ef5-105">OLE DB defines a set of COM interfaces to provide applications with uniform access to data that is stored in diverse information sources.</span></span> <span data-ttu-id="15ef5-106">このアプローチにより、データ ソースに適した豊富な DBMS 機能をサポートするインターフェイスを介して、データ ソースでデータを共有できます。</span><span class="sxs-lookup"><span data-stu-id="15ef5-106">This approach allows a data source to share its data through the interfaces that support the amount of DBMS functionality appropriate to the data source.</span></span> <span data-ttu-id="15ef5-107">OLE DB の高パフォーマンスのアーキテクチャは、柔軟性のあるコンポーネント ベースのサービス モデルの使用に基づいて設計されています。</span><span class="sxs-lookup"><span data-stu-id="15ef5-107">By design, the high-performance architecture of OLE DB is based on its use of a flexible, component-based services model.</span></span> <span data-ttu-id="15ef5-108">OLE DB では、アプリケーションとデータ間の中継層の数を指定せず、特定のタスクを実行するために必要な数のコンポーネントだけを必要とします。</span><span class="sxs-lookup"><span data-stu-id="15ef5-108">Rather than having a prescribed number of intermediary layers between the application and the data, OLE DB requires only as many components as are needed to accomplish a particular task.</span></span>

<span data-ttu-id="15ef5-p102">たとえば、ユーザーがクエリを実行する場合を考えてみます。次のようなシナリオを考えてみましょう。</span><span class="sxs-lookup"><span data-stu-id="15ef5-p102">For example, suppose a user wants to run a query. Consider the following scenarios:</span></span>

  - <span data-ttu-id="15ef5-p103">データがリレーショナル データベースにあり、現在そのデータベースには ODBC ドライバーがあるが、ネイティブ OLE DB プロバイダーがない場合、アプリケーションは ADO を使用して OLE DB Provider for ODBC と通信し、OLE DB Provider for ODBC により適切な ODBC ドライバーが読み込まれます。ドライバーは、DBMS に SQL ステートメントを渡し、DBMS はデータを取得します。</span><span class="sxs-lookup"><span data-stu-id="15ef5-p103">The data resides in a relational database for which there currently exists an ODBC driver but no native OLE DB provider: The application uses ADO to talk to the OLE DB Provider for ODBC, which then loads the appropriate ODBC driver. The driver passes the SQL statement to the DBMS, which retrieves the data.</span></span>

  - <span data-ttu-id="15ef5-p104">データが Microsoft SQL Server にあり、ネイティブ OLE DB プロバイダーがある場合、アプリケーションは ADO を使用して OLE DB Provider for Microsoft SQL Server と直接通信します。中継は不要です。</span><span class="sxs-lookup"><span data-stu-id="15ef5-p104">The data resides in Microsoft SQL Server for which there is a native OLE DB provider: The application uses ADO to talk directly to the OLE DB Provider for Microsoft SQL Server. No intermediaries are required.</span></span>

  - <span data-ttu-id="15ef5-115">データが Microsoft Exchange Server にあり、OLE DB プロバイダーはあるが、SQL クエリを処理するエンジンが公開されていない場合、アプリケーションは ADO を使用して OLE DB Provider for Microsoft Exchange と通信し、OLE DB クエリ プロセッサ コンポーネントを呼び出してクエリを処理します。</span><span class="sxs-lookup"><span data-stu-id="15ef5-115">The data resides in Microsoft Exchange Server, for which there is an OLE DB provider but which does not expose an engine to process SQL queries: The application uses ADO to talk to the OLE DB Provider for Microsoft Exchange and calls upon an OLE DB query processor component to handle the querying.</span></span>

  - <span data-ttu-id="15ef5-116">データがドキュメント形式で Microsoft NTFS ファイル システムにある場合、Microsoft インデックス サービスでネイティブ OLE DB プロバイダーを使用してデータにアクセスし、Microsoft インデックス サービスにより、ファイル システム内のドキュメントの内容およびプロパティにインデックスが付けられて、内容を効率的に検索できます。</span><span class="sxs-lookup"><span data-stu-id="15ef5-116">The data resides in the Microsoft NTFS file system in the form of documents: Data is accessed by using a native OLE DB provider over Microsoft Indexing Service, which indexes the content and properties of documents in the file system to enable efficient content searches.</span></span>

<span data-ttu-id="15ef5-p105">上記のすべての例で、アプリケーションはデータを照会できます。ユーザーのニーズは、最低数のコンポーネントで満たされます。いずれの場合にも、追加のコンポーネントは必要な場合のみ使用され、必要なコンポーネントのみが呼び出されます。この再利用可能で共有可能なコンポーネントを必要に応じて読み込む方法により、OLE DB の使用時に高いパフォーマンスが実現しています。</span><span class="sxs-lookup"><span data-stu-id="15ef5-p105">In all of the preceding examples, the application can query the data. The user's needs are met with a minimum number of components. In each case, additional components are used only if needed, and only the required components are invoked. This demand-loading of reusable and shareable components greatly contributes to high performance when OLE DB is used.</span></span>

<span data-ttu-id="15ef5-p106">プロバイダーは、データ プロバイダーとサービス プロバイダーの 2 つのカテゴリに分類されます。[データ プロバイダー](data-providers.md)は独自のデータを所有し、そのデータを表形式でアプリケーションに表示します。[サービス プロバイダー](service-providers-and-components.md)は、データの作成と使用によりサービスをカプセル化して、ADO アプリケーションの機能を強化します。さらに、サービス プロバイダーは、他のサービス プロバイダーまたはコンポーネントと連携して動作する[サービス コンポーネント](service-providers-and-components.md)として定義されることもあります。</span><span class="sxs-lookup"><span data-stu-id="15ef5-p106">Providers fall into two categories: those providing data and those providing services. A [data provider](data-providers.md) owns its own data and exposes it in tabular form to your application. A [service provider](service-providers-and-components.md) encapsulates a service by producing and consuming data, augmenting features in your ADO applications. A service provider may also be further defined as a [service component](service-providers-and-components.md), which must work in conjunction with other service providers or components.</span></span>

<span data-ttu-id="15ef5-125">ADO は、さまざまな OLE DB プロバイダーに一貫した高レベルのインターフェイスを提供します。</span><span class="sxs-lookup"><span data-stu-id="15ef5-125">ADO provides a consistent, higher level interface to the various OLE DB providers.</span></span>

<span data-ttu-id="15ef5-126">このセクションには、次のトピックが含まれています。</span><span class="sxs-lookup"><span data-stu-id="15ef5-126">This section includes the following topics:</span></span>

- [<span data-ttu-id="15ef5-127">データ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="15ef5-127">Data Providers</span></span>](data-providers.md)

- [<span data-ttu-id="15ef5-128">サービス プロバイダーとコンポーネント</span><span class="sxs-lookup"><span data-stu-id="15ef5-128">Service Providers and Components</span></span>](service-providers-and-components.md)