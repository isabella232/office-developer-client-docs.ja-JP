---
title: ADO ファミリのライブラリ
TOCTitle: The ADO family of libraries
ms:assetid: 9e794509-d0a8-2e5b-02a8-65e26f059c4e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249724(v=office.15)
ms:contentKeyID: 48546656
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 296e05118054ec045c23cd92a399afdc3cddd9a1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718218"
---
# <a name="the-ado-family-of-libraries"></a><span data-ttu-id="89435-102">ADO ファミリのライブラリ</span><span class="sxs-lookup"><span data-stu-id="89435-102">The ADO family of libraries</span></span>

<span data-ttu-id="89435-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="89435-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="89435-104">ADO ファミリは、ADO (RDS を含む)、ADO MD、および ADOX という 3 つの主要ライブラリで構成されています。</span><span class="sxs-lookup"><span data-stu-id="89435-104">Three major libraries make up the ADO family: ADO (including RDS), ADO MD, and ADOX.</span></span>

## <a name="ado"></a><span data-ttu-id="89435-105">ADO</span><span class="sxs-lookup"><span data-stu-id="89435-105">ADO</span></span>

<span data-ttu-id="89435-106">ADO により、クライアント アプリケーションが、OLE DB プロバイダーを通じてデータベース サーバーのデータにアクセスし、これを処理できるようになります。</span><span class="sxs-lookup"><span data-stu-id="89435-106">ADO enables your client applications to access and manipulate data from a database server through an OLE DB provider.</span></span> <span data-ttu-id="89435-107">ADO の主な利点は、使用が簡単で、高速に動作し、メモリのオーバーヘッドが小さく、ディスクの使用量が少ないことです。</span><span class="sxs-lookup"><span data-stu-id="89435-107">The primary benefits of ADO are ease of use, high speed, low memory overhead, and a small disk footprint.</span></span> <span data-ttu-id="89435-108">ADO には、クライアント/サーバーおよび web ベースのアプリケーションを構築するための主要な機能がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="89435-108">ADO supports key features for building client/server and web-based applications.</span></span>

<span data-ttu-id="89435-109">ADO では、リモート データ サービス (RDS) をサーバーからクライアント アプリケーションまたは web ページへのデータは、クライアント上のデータを操作し、ラウンド トリップで 1 つのサーバーに更新プログラムを返すを移動することができますが機能もあります。</span><span class="sxs-lookup"><span data-stu-id="89435-109">ADO also features Remote Data Service (RDS), by which you can move data from a server to a client application or webpage, manipulate the data on the client, and return updates to the server in a single round trip.</span></span>

## <a name="ado-md"></a><span data-ttu-id="89435-110">ADO MD</span><span class="sxs-lookup"><span data-stu-id="89435-110">ADO MD</span></span>

<span data-ttu-id="89435-p102">Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) により、Microsoft Visual Basic、Microsoft Visual C++、Microsoft Visual J++ などの言語から、多次元データに簡単にアクセスできるようになります。ADO MD は、ADO を拡張して、 **CubeDef** オブジェクトや **Cellset** オブジェクトなどの多次元データ専用オブジェクトを使用できるようにしたものです。ADO MD を使用すると、多次元スキーマを参照し、キューブを照会して、その結果を取得できます。</span><span class="sxs-lookup"><span data-stu-id="89435-p102">Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) provides easy access to multidimensional data from languages such as Microsoft Visual Basic, Microsoft Visual C++, and Microsoft Visual J++. ADO MD extends ADO to include objects specific to multidimensional data, such as the **CubeDef** and **Cellset** objects. With ADO MD you can browse multidimensional schema, query a cube, and retrieve the results.</span></span>

<span data-ttu-id="89435-p103">ADO と同様、ADO MD でも、基になる OLE DB プロバイダーを使用してデータにアクセスします。ADO MD を使用して作業するには、プロバイダーが OLE DB for OLAP 仕様で定義された多次元データ プロバイダー (MDP) である必要があります。MDP は、データを表形式のビューで表示する表形式データ プロバイダー (TDP) とは異なり、データを多次元のビューで表示します。使用する OLE DB for OLAP プロバイダーでサポートされている具体的な構文または動作の詳細については、そのプロバイダーのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="89435-p103">Like ADO, ADO MD uses an underlying OLE DB provider to gain access to data. To work with ADO MD, the provider must be a multidimensional data provider (MDP) as defined by the OLE DB for OLAP specification. MDPs present data in multidimensional views as opposed to tabular data providers (TDPs) that present data in tabular views. Refer to the documentation for your OLE DB for OLAP provider for more detailed information about the specific syntax and behaviors supported by your provider.</span></span>

## <a name="adox"></a><span data-ttu-id="89435-118">ADOX</span><span class="sxs-lookup"><span data-stu-id="89435-118">ADOX</span></span>

<span data-ttu-id="89435-p104">Microsoft ActiveX Data Objects Extensions for Data Definition Language and Security (ADOX) は、ADO のオブジェクトとプログラミング モデルを拡張したものです。ADOX には、セキュリティのためのオブジェクトに加え、スキーマの作成および修正のためのオブジェクトが用意されています。ADOX では、オブジェクト ベースの手法を使用してスキーマを操作するため、使用される構文の違いにかかわらず、さまざまなデータ ソースで動作するコードを記述できます。</span><span class="sxs-lookup"><span data-stu-id="89435-p104">Microsoft ActiveX Data Objects Extensions for Data Definition Language and Security (ADOX) is an extension to the ADO objects and programming model. ADOX includes objects for schema creation and modification as well as security. Because it is an object-based approach to schema manipulation, you can write code that will work against various data sources regardless of differences in their native syntaxes.</span></span>

<span data-ttu-id="89435-p105">ADOX は、ADO のコア オブジェクトに添付されるライブラリで、テーブルやプロシージャなどのスキーマ オブジェクトを作成、修正、および削除するための追加のオブジェクトを公開します。また、ユーザーとグループを管理したり、オブジェクトに対する権限を付与および削除したりするためのセキュリティ オブジェクトも備えています。</span><span class="sxs-lookup"><span data-stu-id="89435-p105">ADOX is a companion library to the core ADO objects. It exposes additional objects for creating, modifying, and deleting schema objects, such as tables and procedures. It also includes security objects to maintain users and groups, and to grant and revoke permissions on objects.</span></span>

