---
title: Connection オブジェクトを使用する (Access)
TOCTitle: Using the Connection Object
ms:assetid: e8786411-2be4-8d75-9df7-e345d5a6a7e8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250177(v=office.15)
ms:contentKeyID: 48548423
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0ffc93c2d09c185ea7eaa4a9291ec87aaa72d5eb
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25943571"
---
# <a name="using-the-connection-object-access"></a><span data-ttu-id="3e1e7-102">接続オブジェクト (Access) を使用してください。</span><span class="sxs-lookup"><span data-stu-id="3e1e7-102">Using the Connection object (Access)</span></span>


<span data-ttu-id="3e1e7-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="3e1e7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3e1e7-p101">**Connection** オブジェクトは、データ ソースとの固有のセッションを表します。クライアント/サーバー データベース システムの場合、このオブジェクトは、サーバーへの実際のネットワーク接続に相当します。プロバイダーがサポートする機能によっては、 **Connection** オブジェクトの一部のコレクション、メソッド、またはプロパティを使用できない場合があります。</span><span class="sxs-lookup"><span data-stu-id="3e1e7-p101">A **Connection** object represents a unique session with a data source. In the case of a client/server database system, it can be equivalent to an actual network connection to the server. Depending on the functionality supported by the provider, some collections, methods, or properties of a **Connection** object might not be available.</span></span>

<span data-ttu-id="3e1e7-107">**Connection** オブジェクトを開く前に、データ ソース、および接続の種類について一定の情報を定義しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e1e7-107">Before opening a **Connection** object, you must define certain information about the data source and type of connection.</span></span> <span data-ttu-id="3e1e7-108">**Connection**オブジェクトの**Open**メソッドの*接続文字列*パラメーター、または**接続**オブジェクトの**ConnectionString**プロパティ: 通常この情報のほとんどが含まれます。</span><span class="sxs-lookup"><span data-stu-id="3e1e7-108">The *ConnectionString* parameter of the **Connection** object **Open** method — or the **ConnectionString** property on the **Connection** object — usually contains most of this information.</span></span> <span data-ttu-id="3e1e7-109">接続文字列は、引数を定義する文字列で、引数の数は可変です。</span><span class="sxs-lookup"><span data-stu-id="3e1e7-109">A connection string is a string of characters that defines a variable number of arguments.</span></span> <span data-ttu-id="3e1e7-110">引数には、ADO で必要な引数とプロバイダー固有の引数があり、 **Connection** オブジェクトが作業を実行するために必要な情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3e1e7-110">The arguments — some required by ADO, but others provider-specific — contain information that the **Connection** object must have to carry out its work.</span></span> <span data-ttu-id="3e1e7-111">*接続文字列*パラメーターを構成する引数は、セミコロン (;) で区切られます。</span><span class="sxs-lookup"><span data-stu-id="3e1e7-111">The arguments that make up the *ConnectionString* parameter are separated with semicolons (;).</span></span>

> [!NOTE]
> <span data-ttu-id="3e1e7-112">接続文字列で ODBC データ ソース名 (DSN) やデータ リンク (UDL) ファイルを指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="3e1e7-112">You can also specify an ODBC Data Source Name (DSN) or a Data Link (UDL) file in a connection string.</span></span> <span data-ttu-id="3e1e7-113">Dsn の詳細については、 *ODBC プログラマーズ リファレンス*の第 1 部でのデータ ソースを参照してください。</span><span class="sxs-lookup"><span data-stu-id="3e1e7-113">For more information about DSNs, see Data Sources in Part 1 of the *ODBC Programmer's Reference*.</span></span> <span data-ttu-id="3e1e7-114">Udl の詳細については、 *OLE DB プログラマ リファレンス*データ リンクの API の概要を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3e1e7-114">For more information about UDLs, see Data Link API Overview in the *OLE DB Programmer's Reference*.</span></span>

<span data-ttu-id="3e1e7-115">このセクションには、次のトピックが含まれています。</span><span class="sxs-lookup"><span data-stu-id="3e1e7-115">This section includes the following topics:</span></span>

- [<span data-ttu-id="3e1e7-116">接続文字列を作成する</span><span class="sxs-lookup"><span data-stu-id="3e1e7-116">Creating the Connection String</span></span>](creating-the-connection-string.md)

- [<span data-ttu-id="3e1e7-117">トランザクションを制御する</span><span class="sxs-lookup"><span data-stu-id="3e1e7-117">Controlling Transactions</span></span>](controlling-transactions.md)
