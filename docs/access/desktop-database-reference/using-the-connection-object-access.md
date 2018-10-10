---
title: Connection オブジェクトを使用する (Access)
TOCTitle: Using the Connection Object
ms:assetid: e8786411-2be4-8d75-9df7-e345d5a6a7e8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250177(v=office.15)
ms:contentKeyID: 48548423
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cd3e691258fe5950f40c36a1efcaed8e79810c7a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477406"
---
# <a name="using-the-connection-object-access"></a><span data-ttu-id="2945d-102">Connection オブジェクトを使用する (Access)</span><span class="sxs-lookup"><span data-stu-id="2945d-102">Using the Connection Object (Access)</span></span>


<span data-ttu-id="2945d-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="2945d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2945d-p101">**Connection** オブジェクトは、データ ソースとの固有のセッションを表します。クライアント/サーバー データベース システムの場合、このオブジェクトは、サーバーへの実際のネットワーク接続に相当します。プロバイダーがサポートする機能によっては、 **Connection** オブジェクトの一部のコレクション、メソッド、またはプロパティを使用できない場合があります。</span><span class="sxs-lookup"><span data-stu-id="2945d-p101">A **Connection** object represents a unique session with a data source. In the case of a client/server database system, it can be equivalent to an actual network connection to the server. Depending on the functionality supported by the provider, some collections, methods, or properties of a **Connection** object might not be available.</span></span>

<span data-ttu-id="2945d-107">**Connection** オブジェクトを開く前に、データ ソース、および接続の種類について一定の情報を定義しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="2945d-107">Before opening a **Connection** object, you must define certain information about the data source and type of connection.</span></span> <span data-ttu-id="2945d-108">**Connection**オブジェクトの**Open**メソッドの*接続文字列*パラメーター、または**接続**オブジェクトの**ConnectionString**プロパティ: 通常この情報のほとんどが含まれます。</span><span class="sxs-lookup"><span data-stu-id="2945d-108">The *ConnectionString* parameter of the **Connection** object **Open** method — or the **ConnectionString** property on the **Connection** object — usually contains most of this information.</span></span> <span data-ttu-id="2945d-109">接続文字列は、引数を定義する文字列で、引数の数は可変です。</span><span class="sxs-lookup"><span data-stu-id="2945d-109">A connection string is a string of characters that defines a variable number of arguments.</span></span> <span data-ttu-id="2945d-110">引数には、ADO で必要な引数とプロバイダー固有の引数があり、 **Connection** オブジェクトが作業を実行するために必要な情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2945d-110">The arguments — some required by ADO, but others provider-specific — contain information that the **Connection** object must have to carry out its work.</span></span> <span data-ttu-id="2945d-111">*接続文字列*パラメーターを構成する引数は、セミコロン (;) で区切られます。</span><span class="sxs-lookup"><span data-stu-id="2945d-111">The arguments that make up the *ConnectionString* parameter are separated with semicolons (;).</span></span>


> [!NOTE]
> <P><span data-ttu-id="2945d-112">接続文字列で ODBC データ ソース名 (DSN) やデータ リンク (UDL) ファイルを指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="2945d-112">You can also specify an ODBC Data Source Name (DSN) or a Data Link (UDL) file in a connection string.</span></span> <span data-ttu-id="2945d-113">Dsn の詳細については、 <EM>ODBC プログラマーズ リファレンス</EM>の第 1 部でのデータ ソースを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2945d-113">For more information about DSNs, see Data Sources in Part 1 of the <EM>ODBC Programmer's Reference</EM>.</span></span> <span data-ttu-id="2945d-114">Udl の詳細については、 <EM>OLE DB プログラマ リファレンス</EM>データ リンクの API の概要を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2945d-114">For more information about UDLs, see Data Link API Overview in the <EM>OLE DB Programmer's Reference</EM>.</span></span></P>


