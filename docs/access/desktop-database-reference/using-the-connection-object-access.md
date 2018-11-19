---
title: Connection オブジェクトを使用する (Access)
TOCTitle: Using the Connection Object
ms:assetid: e8786411-2be4-8d75-9df7-e345d5a6a7e8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250177(v=office.15)
ms:contentKeyID: 48548423
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c2f14be526100b1ffcbe34af89c1f72d0a64ff99
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025499"
---
# <a name="using-the-connection-object-access"></a>接続オブジェクト (Access) を使用してください。


**適用されます**Access 2013、Office 2013。

**Connection** オブジェクトは、データ ソースとの固有のセッションを表します。クライアント/サーバー データベース システムの場合、このオブジェクトは、サーバーへの実際のネットワーク接続に相当します。プロバイダーがサポートする機能によっては、 **Connection** オブジェクトの一部のコレクション、メソッド、またはプロパティを使用できない場合があります。

**Connection** オブジェクトを開く前に、データ ソース、および接続の種類について一定の情報を定義しておく必要があります。 **Connection**オブジェクトの**Open**メソッドの*接続文字列*パラメーター、または**接続**オブジェクトの**ConnectionString**プロパティ: 通常この情報のほとんどが含まれます。 接続文字列は、引数を定義する文字列で、引数の数は可変です。 引数には、ADO で必要な引数とプロバイダー固有の引数があり、 **Connection** オブジェクトが作業を実行するために必要な情報が含まれています。 *接続文字列*パラメーターを構成する引数は、セミコロン (;) で区切られます。

> [!NOTE]
> 接続文字列で ODBC データ ソース名 (DSN) やデータ リンク (UDL) ファイルを指定することもできます。 Dsn の詳細については、 *ODBC プログラマーズ リファレンス*の第 1 部でのデータ ソースを参照してください。 Udl の詳細については、 *OLE DB プログラマ リファレンス*データ リンクの API の概要を参照してください。

このセクションには、次のトピックが含まれています。

- [接続文字列の作成](creating-the-connection-string.md)
- [トランザクションを制御します。](controlling-transactions.md)
