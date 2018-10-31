---
title: '第 10 章: レコードとストリーム'
TOCTitle: 'Chapter 10: Records and Streams'
ms:assetid: 74862096-2273-3b61-f89c-06554ccf42cd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249477(v=office.15)
ms:contentKeyID: 48545663
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 92d0eafcb1930e7aa7014e3b120b34e2a8d64231
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25864088"
---
# <a name="chapter-10-records-and-streams"></a>第 10 章: レコードとストリーム


**適用されます**Access 2013 |。Office 2013

ADO には現在、リレーショナル データベースなどのデータ ソース内の情報にアクセスするための主な手段として、[Recordset](recordset-object-ado.md) オブジェクトがあります。ただし、プロバイダーによっては、プロバイダーからのデータを操作できる代替または補足オブジェクトとして、 [Record](record-object-ado.md) オブジェクトおよび [Stream](stream-object-ado.md) オブジェクトがサポートされています。 **Record** 動作の特性については、使用しているプロバイダーのマニュアルを参照してください。

## <a name="records"></a>レコード

**Record** オブジェクトは、**Recordset** の 1 つの行として主に使用されます。ただし、**Records** は、**Recordsets** に比べ機能的に制限され、プロパティやメソッドも異なります。**Record** オブジェクトのデータのソースは、プロバイダーから 1 行のデータを返すコマンドにすることができます。そのため、1 行のデータを返すクエリから結果を取り出す場合は、**Recordset** オブジェクトではなく **Record** オブジェクトを使用すると、より複雑な **Recordset** オブジェクトのインスタンス作成という負荷を排除することができます。

特に、従来のリレーショナル データベースではないデータ ソースのプロバイダー (**Microsoft OLE DB Provider for Internet Publishing**) を使用することで、 [Record](microsoft-ole-db-provider-for-internet-publishing.md) オブジェクトを他の目的に使用することもできます。処理する必要のある情報の多くは、データベース内のテーブルとしてではなく、電子メール システム内のメッセージおよび最新のファイル システム内のファイルとして存在していることがあります。このような場合、 **Record** オブジェクトと **Stream** オブジェクトを使用すると、リレーショナル データベース以外のソースに格納された情報に容易にアクセスできるようになります。

**Record** オブジェクトは、ファイル システム内のディレクトリやファイルなどのデータ、または電子メール システムのフォルダーやメッセージなどのデータを表したり、管理したりすることができます。このような目的の場合、 **Record** のソースは、開かれた **Connection** オブジェクトと連動する、開かれた [Recordset](connection-object-ado.md) のカレント行または絶対 URL や相対 URL にすることができます。

通常、 **Recordset** は、フォルダーやディレクトリなどの階層内のコンテナーや親を表すときに使用されます。 **Record** は、ファイルやドキュメントなど、親コンテナーの 1 つのノードについて特定の情報を返すときに使用されます。このような種類の情報を表すときに **Records** が使用される主な理由は、これらのデータ ソースが異なった要素を持つためです。これは、各 **Record** のフィールドのセットおよび数が、それぞれ異なっていることを意味します。データベースからの行を含む従来の **Recordsets** の要素は同種、つまり、各行のフィールドの数およびタイプは同じです。

**Record** オブジェクトを、Internet Publishing Provider などのプロバイダーからの異種データを処理するために使用する方法については、「 [インターネット発行に ADO を使用する](using-ado-for-internet-publishing.md)」を参照してください。

## <a name="streams"></a>ストリーム

**Stream** オブジェクトは、連続するバイトの読み取り、書き込み、および管理の手段を提供します。このバイト ストリームは、テキストやバイナリであることもあり、システム リソースによってのみサイズが制限されます。通常、ADO **Stream** オブジェクトは、次のような目的で使用されます。

  - 通常、Microsoft OLE DB Provider for Internet Publishing などのプロバイダーで使用される、ファイルやメッセージを構成するテキストやバイトを格納します。 **Stream** オブジェクトの使用の詳細については、「 [インターネット発行に ADO を使用する](using-ado-for-internet-publishing.md)」を参照してください。

**Stream** オブジェクトは、次のものに対して開くことができます。

  - URL で指定された単純なファイル。

  - **Stream** オブジェクトを含む **Record** または **Recordset** のフィールド。

  - ディレクトリまたは複合ファイルを表す **Record** オブジェクトまたは **Recordset** オブジェクトの既定のストリーム。

  - 単純なファイルの URL を含むリソース フィールド。

  - 特定のソースの指定なし。この場合、 **Stream** オブジェクトはメモリで開かれます。データを書き込み、別の **Stream** やファイルに保存できます。

  - **Recordset** 内の BLOB フィールド。

この章では、次のトピックについて説明します。

- [ストリームと永続性](streams-and-persistence.md)

- [レコードおよびプロバイダー提供のフィールド](records-and-provider-supplied-fields.md)

- [絶対 URL と相対 URL](absolute-and-relative-urls.md)

- [インターネット発行に ADO を使用する (ADO)](using-ado-for-internet-publishing.md)