---
title: データ プロバイダー (デスクトップ データベース参照のアクセス)
TOCTitle: Data Providers
ms:assetid: c1e36245-4ece-4986-db30-dc4be3daa794
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249946(v=office.15)
ms:contentKeyID: 48547540
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fd2f17bcc490031625cc8f6cd0ea6d369133fa06
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477069"
---
# <a name="data-providers"></a><span data-ttu-id="f4917-102">データ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="f4917-102">Data Providers</span></span>


<span data-ttu-id="f4917-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="f4917-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f4917-p101">データ プロバイダーは、SQL データベース、インデックス付きのシーケンシャル ファイル、スプレッドシート、ドキュメント ストア、メール ファイルなど、さまざまなデータ ソースを表します。プロバイダーは、行セットと呼ばれる共通の抽象概念を使用して、統一された方法でデータを公開します。</span><span class="sxs-lookup"><span data-stu-id="f4917-p101">Data providers represent diverse sources of data such as SQL databases, indexed-sequential files, spreadsheets, document stores, and mail files. Providers expose data uniformly using a common abstraction called the rowset.</span></span>

<span data-ttu-id="f4917-p102">ADO は、高機能で柔軟性に富んでおり、いくつかのさまざまなデータ プロバイダーのうち任意のものに接続できるだけでなく、使用するプロバイダーに固有の機能に関係なく、同じプログラミング モデルを公開します。しかし、データ プロバイダーはそれぞれ異なっているため、アプリケーションが ADO と対話する方法は、データ プロバイダーによって異なります。</span><span class="sxs-lookup"><span data-stu-id="f4917-p102">ADO is powerful and flexible because it can connect to any of several different data providers and still expose the same programming model, regardless of the specific features of any given provider. However, because each data provider is unique, how your application interacts with ADO will vary by data provider.</span></span>

<span data-ttu-id="f4917-108">たとえば、Microsoft SQL Server のデータベースにアクセスするときに使用される OLE DB Provider for SQL Server の機能は、Web サーバー上のファイル ストアにアクセスするときに使用される Microsoft OLE DB Provider for Internet Publishing の機能とは大きく異なります。</span><span class="sxs-lookup"><span data-stu-id="f4917-108">For example, the capabilities and features of the OLE DB Provider for SQL Server, which is used to access Microsoft SQL Server databases, are considerably different from those of the Microsoft OLE DB Provider for Internet Publishing, which is used to access file stores on a Web server.</span></span>

