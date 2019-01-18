---
title: Microsoft Active X データ オブジェクト (ADO) リファレンス
TOCTitle: Microsoft ActiveX Data Objects Reference
ms:assetid: 235fc575-8a2e-913c-fa3d-bb86256733f9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249010(v=office.15)
ms:contentKeyID: 48543728
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: c1fee657c0d6ecd319157f704df2b1c5a900be3b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698884"
---
# <a name="microsoft-activex-data-objects-reference"></a><span data-ttu-id="5b986-102">Microsoft Active X データ オブジェクト (ADO) リファレンス</span><span class="sxs-lookup"><span data-stu-id="5b986-102">Microsoft ActiveX Data Objects reference</span></span>

<span data-ttu-id="5b986-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="5b986-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="purpose"></a><span data-ttu-id="5b986-104">目的</span><span class="sxs-lookup"><span data-stu-id="5b986-104">Purpose</span></span>

<span data-ttu-id="5b986-105">Microsoft ActiveX Data Objects (ADO) により、クライアント アプリケーションが、OLE DB プロバイダーを通じてデータベース サーバーのデータにアクセスし、これを操作できるようになります。</span><span class="sxs-lookup"><span data-stu-id="5b986-105">Microsoft ActiveX Data Objects (ADO) enable your client applications to access and manipulate data from a database server through an OLE DB provider.</span></span> <span data-ttu-id="5b986-106">ADO の主な利点は、使用が簡単で、高速に動作し、メモリのオーバーヘッドが小さく、ディスクの使用量が少ないことです。</span><span class="sxs-lookup"><span data-stu-id="5b986-106">Its primary benefits are ease of use, high speed, low memory overhead, and a small disk footprint.</span></span> <span data-ttu-id="5b986-107">ADO には、クライアント/サーバーおよび web ベースのアプリケーションを構築するための主要な機能がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="5b986-107">ADO supports key features for building client/server and web-based applications.</span></span>

## <a name="rds"></a><span data-ttu-id="5b986-108">RDS</span><span class="sxs-lookup"><span data-stu-id="5b986-108">RDS</span></span>

<span data-ttu-id="5b986-109">ADO では、リモート データ サービス (RDS) をサーバーからクライアント アプリケーションまたは web ページへのデータは、クライアント上のデータを操作し、ラウンド トリップで 1 つのサーバーに更新プログラムを返すを移動することができますが機能もあります。</span><span class="sxs-lookup"><span data-stu-id="5b986-109">ADO also features Remote Data Service (RDS), by which you can move data from a server to a client application or webpage, manipulate the data on the client, and return updates to the server in a single round trip.</span></span>

## <a name="ado-md"></a><span data-ttu-id="5b986-110">ADO MD</span><span class="sxs-lookup"><span data-stu-id="5b986-110">ADO MD</span></span>

<span data-ttu-id="5b986-p102">Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) により、Microsoft Visual Basic、Microsoft Visual C++、Microsoft Visual J++ などの言語から、多次元データに簡単にアクセスできるようになります。ADO MD は、Microsoft ActiveX Data Objects (ADO) を拡張して、CubeDef オブジェクトや Cellset オブジェクトなどの多次元データ専用オブジェクトを使用できるようにしたものです。ADO MD を使用すると、多次元スキーマを参照し、キューブを照会して、その結果を取得できます。</span><span class="sxs-lookup"><span data-stu-id="5b986-p102">Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) provides easy access to multidimensional data from languages such as Microsoft Visual Basic, Microsoft Visual C++, and Microsoft Visual J++. ADO MD extends Microsoft ActiveX Data Objects (ADO) to include objects specific to multidimensional data, such as the CubeDef and Cellset objects. With ADO MD you can browse multidimensional schema, query a cube, and retrieve the results.</span></span>

<span data-ttu-id="5b986-p103">ADO と同様、ADO MD でも、基になる OLE DB プロバイダーを使用してデータにアクセスします。ADO MD を使用して作業するためには、プロバイダーが OLE DB for OLAP の仕様で定義された多次元データ プロバイダー (MDP) である必要があります。MDP は、データを表形式のビューで表示する表形式データ プロバイダー (TDP) とは異なり、データを多次元のビューで表示します。使用する OLAP OLE DB プロバイダーでサポートされている具体的な構文や動作の詳細については、そのプロバイダーのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5b986-p103">Like ADO, ADO MD uses an underlying OLE DB provider to gain access to data. To work with ADO MD, the provider must be a multidimensional data provider (MDP) as defined by the OLE DB for OLAP specification. MDPs present data in multidimensional views as opposed to tabular data providers (TDPs) that present data in tabular views. Refer to the documentation for your OLAP OLE DB provider for more detailed information on the specific syntax and behaviors supported by your provider.</span></span>

## <a name="adox"></a><span data-ttu-id="5b986-118">ADOX</span><span class="sxs-lookup"><span data-stu-id="5b986-118">ADOX</span></span>

<span data-ttu-id="5b986-p104">Microsoft ActiveX Data Objects Extensions for Data Definition Language and Security (ADOX) は、ADO のオブジェクトとプログラミング モデルを拡張したものです。ADOX には、セキュリティのためのオブジェクトに加え、スキーマの作成および修正のためのオブジェクトが用意されています。ADOX では、オブジェクト ベースの手法を使用してスキーマを操作するため、使用される構文の違いにかかわらず、さまざまなデータ ソースで動作するコードを記述できます。</span><span class="sxs-lookup"><span data-stu-id="5b986-p104">Microsoft ActiveX Data Objects Extensions for Data Definition Language and Security (ADOX) is an extension to the ADO objects and programming model. ADOX includes objects for schema creation and modification, as well as security. Because it is an object-based approach to schema manipulation, you can write code that will work against various data sources regardless of differences in their native syntaxes.</span></span>

<span data-ttu-id="5b986-p105">ADOX は、ADO のコア オブジェクトに添付されるライブラリで、テーブルやプロシージャなどのスキーマ オブジェクトを作成、修正、および削除するための追加のオブジェクトを公開します。また、ユーザーとグループを管理したり、オブジェクトに対する権限を付与および削除したりするためのセキュリティ オブジェクトも備えています。</span><span class="sxs-lookup"><span data-stu-id="5b986-p105">ADOX is a companion library to the core ADO objects. It exposes additional objects for creating, modifying, and deleting schema objects, such as tables and procedures. It also includes security objects to maintain users and groups and to grant and revoke permissions on objects.</span></span>

## <a name="ado-25-main-components"></a><span data-ttu-id="5b986-125">ADO 2.5 の主要なコンポーネント</span><span class="sxs-lookup"><span data-stu-id="5b986-125">ADO 2.5 main components</span></span>

- <span data-ttu-id="5b986-126">[プログラマ ガイド」](ado-programmer-s-guide.md): ADO、RDS、ADO MD、および ADOX を使用しています。</span><span class="sxs-lookup"><span data-stu-id="5b986-126">[Programmer's guide](ado-programmer-s-guide.md): An introduction to using ADO, RDS, ADO MD, and ADOX.</span></span>

- <span data-ttu-id="5b986-127">[プログラマーズ リファレンス](ado-programmer-s-reference-topics.md): ADO のドキュメントのこのセクションには、各 ADO、RDS、ADO MD、および ADOX オブジェクト、コレクション、プロパティ、動的プロパティ、メソッド、イベント、および列挙に関するトピックが含まれています。</span><span class="sxs-lookup"><span data-stu-id="5b986-127">[Programmer's reference](ado-programmer-s-reference-topics.md): This section of the ADO documentation contains topics for each ADO, RDS, ADO MD, and ADOX object, collection, property, dynamic property, method, event, and enumeration.</span></span>

## <a name="feedback"></a><span data-ttu-id="5b986-128">フィードバック</span><span class="sxs-lookup"><span data-stu-id="5b986-128">Feedback</span></span>

<span data-ttu-id="5b986-129">ADO のドキュメントまたはサンプルに関するフィードバックは、ADO ドキュメント チームに直接お送りください。</span><span class="sxs-lookup"><span data-stu-id="5b986-129">You can send feedback about ADO documentation or samples directly to the ADO documentation team.</span></span>

