---
title: アクセス (アクセス デスクトップ データベース参照) に変更
TOCTitle: Changes in Access
description: Access は、Access Data Projects (ADP) をサポートしていません。 Access では、Web ベースの Access アプリを作成できるようにするための新しいアプリケーションの種類が導入されています。
ms:assetid: 8dfc5fc9-a6a7-4a91-8e97-c3874e9b880f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ618413(v=office.15)
ms:contentKeyID: 49106417
ms.date: 10/16/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: de2ff21598639b445f5ff84240b115704b484209
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698947"
---
# <a name="changes-in-access"></a>Access における変更点

**に適用されます:** Access 2013 |Office 2013

Access は、Access Data Projects (ADP) をサポートしていません。 Access では、Web ベースの Access アプリを作成できるようにするための新しいアプリケーションの種類が導入されています。 このアプリケーションの種類を使用すると、SQL Server の設置型またはクラウドでの電力を使用する web ベースのアプリケーションを作成できます。

SharePoint サーバー上のアクセス アプリケーションを作成するテーブル、ビュー、または SQL Server データベース内のトリガー、アクセス クライアントを使用して、アクセス クライアントでテーブル、クエリ、またはデータ マクロを作成するときに開くことができます、データベースの他のアプリケーションを接続SQL Server への ect。 これにより、データを共有したり、他のシステムから Access アプリにデータをロードしたりすることが可能になります。

Office 365 と Access を使用すると、ユーザーに配信するアプリケーションを、展開に関する課題、ソフトウェア インストールの問題、オペレーティング システムの互換性などについて心配することなくビルドできます。1 つの場所でアプリをビルドし、それを SQL Azure や SQL Server の機能を活用して Web 上で共有します。

SQL Server のクラウド版である[SQL Azure](https://docs.microsoft.com/azure/sql-database/sql-database-technical-overview) は、Access Data Projects (ADP) が処理をするために依存する機能をサポートしていません。SQL Azure で ADP をサポートするには、Access にかなりの変更を加える必要があります。

これらの理由で、Access は ADP をサポートしていません。 Adp は、オンプレミス環境で SQL Server を使用するための優れたツールをされています。ただし、Adp が Access 2000 で導入されたために、多くが変更されました。 今日では、ユーザーがどこにいてもデータベースを利用できることが必要となっています。

## <a name="adp-support-and-the-future"></a>ADP サポートと機能

ADP は旧バージョンの Access では引き続き機能します。ADP アプリケーションをこれまでとおり開発でき、旧バージョンの Access に関しては標準の[サポート ライフサイクル](https://support.microsoft.com/lifecycle/search)に基づいてサポートが引き続き提供されます。新しいバージョンの SQL Server または SQL Azure をサポートするように旧バージョンの Access を更新する予定はありません。そのため、SQL Server 2012 以降のバージョンとともに ADP を使用すると、問題が生じる可能性があります。ADP は今後も SQL 2008 R2 以前をサポートします。

今後、ADP 開発者は次のようないくつかの可能性について考慮できます。

- **アクセス アプリケーションに変換する**-を使用してアクセス、アクセスの新しいアプリケーションに、テーブルをインポートすることし、アプリケーションのフォームが自動的に作成されます。 アクセスを作成するには、基本フォームの機能を拡張することができ、ユーザーは web 上で、アプリケーションを使用することができます。 ADP で使用している一部の機能は利用できなくなることがありますが、Microsoft はこのアプリケーションの種類の製品において引き続き鋭意改善を図っています。

- **リンクされているデスクトップ ・ データベースへの変換**: アクセスは、.accdb ファイル形式でのデスクトップのデータベースの作成をサポートするために継続します。 ご使用のアプリケーションを (すべての既存のフォームとレポートを含めて) .accdb 形式に変換し、データは SQL Server に残しておくことができます。 リンク テーブルを使用して SQL Server データベースにリンクすることができ、同じデータを操作する、アプリケーションが続行されます。

- **ハイブリッド アプリケーションを作成する**– アプリケーションのサイズが大きく、すべてを同時に変換したくない場合、することができますからデータをインポート、Access アプリケーションとのリンクに SQL Server データベースに、.accdb です。 これにより、移行に追加するフォームおよび機能時間の経過と共にアクセス アプリでは、Access アプリケーションの背後にある SQL Server データベースにリンク テーブルを使用する .accdb ファイルとしてクライアント アプリケーションを維持しながら徐々 になります。

- **.NET Framework へのアップグレード**: アプリケーションは、.NET Framework などの本格的な開発プラットフォームへの移行を検討するのに十分な複雑な可能性があります。 SQL Server は、既存のデータベース インフラストラクチャを使用し、コードを大幅に書き直すことがなく、アプリケーションの機能を拡張することを容易にできるように設計されています。

## <a name="conclusion"></a>まとめ

Access は、SharePoint Server と SQL Server のテクノロジに基づいてデータベースをクラウドで接続し、Office 365 と円滑に連動するように設計されています。Access は、お客様のビジネス遂行に役立つデータに基づいたビジネス アプリを迅速に作成および共有できる設計になっています。

## <a name="see-also"></a>関連項目

- [Access 2013 の開発者向け新機能](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/new-in-access-for-developers)


