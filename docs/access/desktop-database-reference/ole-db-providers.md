---
title: OLE DB プロバイダー (Access デスクトップ データベース リファレンス)
TOCTitle: OLE DB providers
ms:assetid: ef412198-eac5-bf86-73fd-574e67276408
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250215(v=office.15)
ms:contentKeyID: 48548576
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 8f7576e65298b8d9e641eb5ea1e16b6c5e3c084a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611946"
---
# <a name="ole-db-providers"></a>OLE DB プロバイダー


**適用先**: Access 2013、Office 2013

ADO プログラマ 向けガイド [の概要では](introduction-to-ado-programming.md) 、ADO と他の Microsoft Data Access アーキテクチャとの関係について説明します。 OLE DB は、さまざまな情報ソースに格納されているデータに各アプリケーションから同じようにアクセスできる、一連の COM インターフェイスを定義します。 このアプローチにより、データ ソースに適した豊富な DBMS 機能をサポートするインターフェイスを介して、データ ソースでデータを共有できます。 OLE DB の高パフォーマンスのアーキテクチャは、柔軟性のあるコンポーネント ベースのサービス モデルの使用に基づいて設計されています。 OLE DB では、アプリケーションとデータ間の中継層の数を指定せず、特定のタスクを実行するために必要な数のコンポーネントだけを必要とします。

たとえば、ユーザーがクエリを実行する場合を考えてみます。次のようなシナリオを考えてみましょう。

  - データがリレーショナル データベースにあり、現在そのデータベースには ODBC ドライバーがあるが、ネイティブ OLE DB プロバイダーがない場合、アプリケーションは ADO を使用して OLE DB Provider for ODBC と通信し、OLE DB Provider for ODBC により適切な ODBC ドライバーが読み込まれます。ドライバーは、DBMS に SQL ステートメントを渡し、DBMS はデータを取得します。

  - データが Microsoft SQL Server にあり、ネイティブ OLE DB プロバイダーがある場合、アプリケーションは ADO を使用して OLE DB Provider for Microsoft SQL Server と直接通信します。中継は不要です。

  - データが Microsoft Exchange Server にあり、OLE DB プロバイダーはあるが、SQL クエリを処理するエンジンが公開されていない場合、アプリケーションは ADO を使用して OLE DB Provider for Microsoft Exchange と通信し、OLE DB クエリ プロセッサ コンポーネントを呼び出してクエリを処理します。

  - データがドキュメント形式で Microsoft NTFS ファイル システムにある場合、Microsoft インデックス サービスでネイティブ OLE DB プロバイダーを使用してデータにアクセスし、Microsoft インデックス サービスにより、ファイル システム内のドキュメントの内容およびプロパティにインデックスが付けられて、内容を効率的に検索できます。

上記のすべての例で、アプリケーションはデータを照会できます。ユーザーのニーズは、最低数のコンポーネントで満たされます。いずれの場合にも、追加のコンポーネントは必要な場合のみ使用され、必要なコンポーネントのみが呼び出されます。この再利用可能で共有可能なコンポーネントを必要に応じて読み込む方法により、OLE DB の使用時に高いパフォーマンスが実現しています。

プロバイダーは、データ プロバイダーとサービス プロバイダーの 2 つのカテゴリに分類されます。[データ プロバイダー](data-providers.md)は独自のデータを所有し、そのデータを表形式でアプリケーションに表示します。[サービス プロバイダー](service-providers-and-components.md)は、データの作成と使用によりサービスをカプセル化して、ADO アプリケーションの機能を強化します。さらに、サービス プロバイダーは、他のサービス プロバイダーまたはコンポーネントと連携して動作する[サービス コンポーネント](service-providers-and-components.md)として定義されることもあります。

ADO は、さまざまな OLE DB プロバイダーに一貫した高レベルのインターフェイスを提供します。

このセクションでは、以下のトピックについて説明します。

- [データ プロバイダー](data-providers.md)

- [サービス プロバイダーとコンポーネント](service-providers-and-components.md)
