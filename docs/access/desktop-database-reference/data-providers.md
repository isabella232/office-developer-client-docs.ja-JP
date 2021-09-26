---
title: データ プロバイダー (Access デスクトップ データベースリファレンス)
TOCTitle: Data Providers
ms:assetid: c1e36245-4ece-4986-db30-dc4be3daa794
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249946(v=office.15)
ms:contentKeyID: 48547540
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ecc26839906a4be89a76d8f42e9f0431e36851e7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589800"
---
# <a name="data-providers"></a>データ プロバイダー


**適用先**: Access 2013、Office 2013

データ プロバイダーは、SQL データベース、インデックス付きのシーケンシャル ファイル、スプレッドシート、ドキュメント ストア、メール ファイルなど、さまざまなデータ ソースを表します。プロバイダーは、行セットと呼ばれる共通の抽象概念を使用して、統一された方法でデータを公開します。

ADO は、高機能で柔軟性に富んでおり、いくつかのさまざまなデータ プロバイダーのうち任意のものに接続できるだけでなく、使用するプロバイダーに固有の機能に関係なく、同じプログラミング モデルを公開します。しかし、データ プロバイダーはそれぞれ異なっているため、アプリケーションが ADO と対話する方法は、データ プロバイダーによって異なります。

たとえば、Microsoft SQL Server データベースへのアクセスに使用される SQL Server 用 OLE DB プロバイダーの機能と機能は、Web サーバー上のファイル ストアにアクセスするために使用される Microsoft OLE DB Provider for Internet Publishing とは大きく異なります。

