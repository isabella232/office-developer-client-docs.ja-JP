---
title: Connection オブジェクトを使用する (Access)
TOCTitle: Using the Connection Object
ms:assetid: e8786411-2be4-8d75-9df7-e345d5a6a7e8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250177(v=office.15)
ms:contentKeyID: 48548423
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: a8c7a77903ef318b6ac802c4d1488cc053d4db9a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562056"
---
# <a name="using-the-connection-object-access"></a>Connection オブジェクトの使用 (Access)


**適用先:** Access 2013、Office 2013

**Connection** オブジェクトは、データ ソースとの固有のセッションを表します。クライアント/サーバー データベース システムの場合、このオブジェクトは、サーバーへの実際のネットワーク接続に相当します。プロバイダーがサポートする機能によっては、 **Connection** オブジェクトの一部のコレクション、メソッド、またはプロパティを使用できない場合があります。

**Connection** オブジェクトを開く前に、データ ソース、および接続の種類について一定の情報を定義しておく必要があります。通常は、**Connection** オブジェクトの **Open** メソッドの *ConnectionString* パラメーター、つまり **Connection** オブジェクトの **ConnectionString** プロパティにこの情報の大部分が含まれています。接続文字列は、引数を定義する文字列で、引数の数は可変です。引数には、ADO で必要な引数とプロバイダー固有の引数があり、**Connection** オブジェクトが作業を実行するために必要な情報が含まれています。*ConnectionString* パラメーターを構成する引数は、セミコロン (;) で区切られています。

> [!NOTE]
> 接続文字列には、ODBC データ ソース名 (DSN) やデータ リンク (UDL) ファイルを指定することもできます。DSN の詳細については、「ODBC Programmer's Reference」 (英語) の「Data Sources」 (英語) を参照してください。UDL の詳細については、「OLE DB Programmer's Reference」 (英語) の「Data Link API Overview」 (英語) を参照してください。

このセクションでは、以下のトピックについて説明します。

- [接続文字列の作成](creating-the-connection-string.md)
- [トランザクションの制御](controlling-transactions.md)
