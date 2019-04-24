---
title: '第 10 章: レコードとストリーム'
TOCTitle: 'Chapter 10: Records and streams'
ms:assetid: 74862096-2273-3b61-f89c-06554ccf42cd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249477(v=office.15)
ms:contentKeyID: 48545663
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1a47ac1f850905546651ffbdd708887bf7d74940
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296494"
---
# <a name="chapter-10-records-and-streams"></a><span data-ttu-id="8697a-102">第 10 章: レコードとストリーム</span><span class="sxs-lookup"><span data-stu-id="8697a-102">Chapter 10: Records and streams</span></span>

<span data-ttu-id="8697a-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="8697a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8697a-p101">ADO には現在、リレーショナル データベースなどのデータ ソース内の情報にアクセスするための主な手段として、[Recordset](recordset-object-ado.md) オブジェクトがあります。ただし、プロバイダーによっては、プロバイダーからのデータを操作できる代替または補足オブジェクトとして、 [Record](record-object-ado.md) オブジェクトおよび [Stream](stream-object-ado.md) オブジェクトがサポートされています。 **Record** 動作の特性については、使用しているプロバイダーのマニュアルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8697a-p101">ADO currently provides the[Recordset](recordset-object-ado.md) object as the primary means of accessing information in data sources, such as relational databases. However, some providers support the [Record](record-object-ado.md) and [Stream](stream-object-ado.md) objects as alternative or complementary objects with which data from providers can be manipulated. For specifics on **Record** behavior, see your provider's documentation.</span></span>

## <a name="records"></a><span data-ttu-id="8697a-107">レコード</span><span class="sxs-lookup"><span data-stu-id="8697a-107">Records</span></span>

<span data-ttu-id="8697a-p102">**Record** オブジェクトは、**Recordset** の 1 つの行として主に使用されます。ただし、**Records** は、**Recordsets** に比べ機能的に制限され、プロパティやメソッドも異なります。**Record** オブジェクトのデータのソースは、プロバイダーから 1 行のデータを返すコマンドにすることができます。そのため、1 行のデータを返すクエリから結果を取り出す場合は、**Recordset** オブジェクトではなく **Record** オブジェクトを使用すると、より複雑な **Recordset** オブジェクトのインスタンス作成という負荷を排除することができます。</span><span class="sxs-lookup"><span data-stu-id="8697a-p102">**Record** objects essentially function as one-row **Recordset**s. However, **Records** have limited functionality compared to **Recordsets** and they have different properties and methods.The source for the data in a **Record** object can be a command which returns one row of data from the provider. Using **Record** objects rather than **Recordset** objects to receive the results from a query that returns one row of data eliminates the overhead of instantiating the more complex **Recordset** object.</span></span>

<span data-ttu-id="8697a-p103">特に、従来のリレーショナル データベースではないデータ ソースのプロバイダー ([Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)) を使用することで、**Record** オブジェクトを他の目的に使用することもできます。処理する必要のある情報の多くは、データベース内のテーブルとしてではなく、電子メール システム内のメッセージおよび最新のファイル システム内のファイルとして存在していることがあります。このような場合、**Record** オブジェクトと **Stream** オブジェクトを使用すると、リレーショナル データベース以外のソースに格納された情報に容易にアクセスできるようになります。</span><span class="sxs-lookup"><span data-stu-id="8697a-p103">**Record** objects can serve another purpose, particularly with providers for data sources other than traditional relational databases, such as the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Much of the information that must be processed exists, not as tables in databases, but as messages in electronic mail systems and files in modern file systems. The **Record** and **Stream** objects facilitate access to information stored in sources other than relational databases.</span></span>

<span data-ttu-id="8697a-114">**Record**オブジェクトは、ファイルシステム内のディレクトリやファイル、電子メールシステムのフォルダーやメッセージなどのデータを表すことができます。</span><span class="sxs-lookup"><span data-stu-id="8697a-114">The **Record** object can represent and manage data such as directories and files in a file system or folders and messages in an email system.</span></span> <span data-ttu-id="8697a-115">このような目的の場合、 **Record** のソースは、開かれた **Connection** オブジェクトと連動する、開かれた [Recordset](connection-object-ado.md) のカレント行または絶対 URL や相対 URL にすることができます。</span><span class="sxs-lookup"><span data-stu-id="8697a-115">For these purposes, the source for the **Record** can be the current row of an open **Recordset**, an absolute URL, or a relative URL in conjunction with an open [Connection](connection-object-ado.md) object.</span></span>

<span data-ttu-id="8697a-p105">通常、 **Recordset** は、フォルダーやディレクトリなどの階層内のコンテナーや親を表すときに使用されます。 **Record** は、ファイルやドキュメントなど、親コンテナーの 1 つのノードについて特定の情報を返すときに使用されます。このような種類の情報を表すときに **Records** が使用される主な理由は、これらのデータ ソースが異なった要素を持つためです。これは、各 **Record** のフィールドのセットおよび数が、それぞれ異なっていることを意味します。データベースからの行を含む従来の **Recordsets** の要素は同種、つまり、各行のフィールドの数およびタイプは同じです。</span><span class="sxs-lookup"><span data-stu-id="8697a-p105">Typically, a **Recordset** can be used to represent a container or parent in a hierarchy such as a folder or directory. A **Record** can be used to return specific information about one node in the parent container, such as a file or document. The primary reason **Records** are used to represent this type of information is that these sources of data are heterogenous. This means that each **Record** may have a different set and number of fields. Traditional **Recordsets** containing rows from a database are homogenous, which means that each row has the same number and type of fields.</span></span>

<span data-ttu-id="8697a-121">**Record** オブジェクトを、Internet Publishing Provider などのプロバイダーからの異種データを処理するために使用する方法については、「 [インターネット発行に ADO を使用する](using-ado-for-internet-publishing.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8697a-121">For more information about using the **Record** object for processing this heterogeneous data from providers such as the Internet Publishing Provider, see [Using ADO for Internet Publishing](using-ado-for-internet-publishing.md).</span></span>

## <a name="streams"></a><span data-ttu-id="8697a-122">ストリーム</span><span class="sxs-lookup"><span data-stu-id="8697a-122">Streams</span></span>

<span data-ttu-id="8697a-p106">**Stream** オブジェクトは、連続するバイトの読み取り、書き込み、および管理の手段を提供します。このバイト ストリームは、テキストやバイナリであることもあり、システム リソースによってのみサイズが制限されます。通常、ADO **Stream** オブジェクトは、次のような目的で使用されます。</span><span class="sxs-lookup"><span data-stu-id="8697a-p106">The **Stream** object provides the means to read, write, and manage a stream of bytes. This byte stream may be text or binary and is limited in size only by system resources. Typically, ADO **Stream** objects are used for the following purposes:</span></span>

- <span data-ttu-id="8697a-p107">通常、Microsoft OLE DB Provider for Internet Publishing などのプロバイダーで使用される、ファイルやメッセージを構成するテキストやバイトを格納します。 **Stream** オブジェクトの使用の詳細については、「 [インターネット発行に ADO を使用する](using-ado-for-internet-publishing.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8697a-p107">To contain the text or bytes that comprise a file or message, typically used with providers such as the Microsoft OLE DB Provider for Internet Publishing. For more information about this use of **Stream** objects, see [Using ADO for Internet Publishing](using-ado-for-internet-publishing.md).</span></span>

<span data-ttu-id="8697a-128">**Stream** オブジェクトは、次のものに対して開くことができます。</span><span class="sxs-lookup"><span data-stu-id="8697a-128">A **Stream** object can be opened on:</span></span>

- <span data-ttu-id="8697a-129">URL で指定された単純なファイル。</span><span class="sxs-lookup"><span data-stu-id="8697a-129">A simple file specified with a URL.</span></span>

- <span data-ttu-id="8697a-130">**Stream** オブジェクトを含む **Record** または **Recordset** のフィールド。</span><span class="sxs-lookup"><span data-stu-id="8697a-130">A field of a **Record** or **Recordset** containing a **Stream** object.</span></span>

- <span data-ttu-id="8697a-131">ディレクトリまたは複合ファイルを表す **Record** オブジェクトまたは **Recordset** オブジェクトの既定のストリーム。</span><span class="sxs-lookup"><span data-stu-id="8697a-131">The default stream of a **Record** or **Recordset** object representing a directory or compound file.</span></span>

- <span data-ttu-id="8697a-132">単純なファイルの URL を含むリソース フィールド。</span><span class="sxs-lookup"><span data-stu-id="8697a-132">A resource field containing the URL of a simple file.</span></span>

- <span data-ttu-id="8697a-p108">特定のソースの指定なし。この場合、 **Stream** オブジェクトはメモリで開かれます。データを書き込み、別の **Stream** やファイルに保存できます。</span><span class="sxs-lookup"><span data-stu-id="8697a-p108">No particular source at all. In this case, a **Stream** object is opened in memory. Data can be written to it and then saved in another **Stream** or file.</span></span>

- <span data-ttu-id="8697a-136">**Recordset** 内の BLOB フィールド。</span><span class="sxs-lookup"><span data-stu-id="8697a-136">A BLOB field in a **Recordset**.</span></span>

<span data-ttu-id="8697a-137">この章では、次のトピックについて説明します。</span><span class="sxs-lookup"><span data-stu-id="8697a-137">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="8697a-138">セッションと永続化</span><span class="sxs-lookup"><span data-stu-id="8697a-138">Streams and persistence</span></span>](streams-and-persistence.md)
- [<span data-ttu-id="8697a-139">レコードとプロバイダー供給のフィールド</span><span class="sxs-lookup"><span data-stu-id="8697a-139">Records and provider-supplied fields</span></span>](records-and-provider-supplied-fields.md)
- [<span data-ttu-id="8697a-140">絶対 URL と相対 URL</span><span class="sxs-lookup"><span data-stu-id="8697a-140">Absolute and relative URLs</span></span>](absolute-and-relative-urls.md)
- [<span data-ttu-id="8697a-141">インターネット発行に ado を使用する (ado)</span><span class="sxs-lookup"><span data-stu-id="8697a-141">Using ADO for Internet publishing (ADO)</span></span>](using-ado-for-internet-publishing.md)
