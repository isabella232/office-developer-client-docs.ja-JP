---
title: データ プロバイダー (デスクトップ データベース参照のアクセス)
TOCTitle: Data Providers
ms:assetid: c1e36245-4ece-4986-db30-dc4be3daa794
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249946(v=office.15)
ms:contentKeyID: 48547540
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2b4b3497493627f5446055d50e525882e5187807
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886159"
---
# <a name="data-providers"></a>データ プロバイダー


**適用されます**Access 2013、Office 2013。

データ プロバイダーは、SQL データベース、インデックス付きのシーケンシャル ファイル、スプレッドシート、ドキュメント ストア、メール ファイルなど、さまざまなデータ ソースを表します。プロバイダーは、行セットと呼ばれる共通の抽象概念を使用して、統一された方法でデータを公開します。

ADO は、高機能で柔軟性に富んでおり、いくつかのさまざまなデータ プロバイダーのうち任意のものに接続できるだけでなく、使用するプロバイダーに固有の機能に関係なく、同じプログラミング モデルを公開します。しかし、データ プロバイダーはそれぞれ異なっているため、アプリケーションが ADO と対話する方法は、データ プロバイダーによって異なります。

などの機能と、Microsoft SQL Server データベースへのアクセスに使用される SQL Server の OLE DB プロバイダーの機能は、Microsoft OLE DB プロバイダーのインターネット公開ファイルへのアクセスに使用されるものと大きく異なるweb サーバー上のストアです。

