---
title: Accessにおける変更点（Accessデスクトップデータベースリファレンス）
TOCTitle: Changes in Access
description: Access は、Access Data Projects (ADP) をサポートしていません。 Access では、Web ベースの Access アプリを作成できるようにするための新しいアプリケーションの種類が導入されています。
ms:assetid: 8dfc5fc9-a6a7-4a91-8e97-c3874e9b880f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ618413(v=office.15)
ms:contentKeyID: 49106417
ms.date: 10/16/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: de2ff21598639b445f5ff84240b115704b484209
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296501"
---
# <a name="changes-in-access"></a>Access における変更点

**適応対象**: Access 2013 | Office 2013

Access は、Access Data Projects (ADP) をサポートしていません。 Access では、Web ベースの Access アプリを作成できるようにするための新しいアプリケーションの種類が導入されています。 この種類のアプリケーションを使用すると、設置型またはクラウドSQL Serverの機能を使用するWebベースのアプリケーションを作成できます。

SharePoint Server上のAccessアプリケーションで、SQL Serverデータベースにテーブル、ビュー、またはトリガを作成するAccessクライアントを用いテーブル、クエリ、またはデータマクロを作成すると、 SQL Serverに接続する他のアプリケーションに対するデータベースを開くことができます。 これにより、データを共有したり、他のシステムから Access アプリにデータをロードしたりすることが可能になります。

Office 365 と Access を使用すると、ユーザーに配信するアプリケーションを、展開に関する課題、ソフトウェア インストールの問題、オペレーティング システムの互換性などについて心配することなくビルドできます。1 つの場所でアプリをビルドし、それを SQL Azure や SQL Server の機能を活用して Web 上で共有します。

SQL Server のクラウド版である[SQL Azure](https://docs.microsoft.com/azure/sql-database/sql-database-technical-overview) は、Access Data Projects (ADP) が処理をするために依存する機能をサポートしていません。SQL Azure で ADP をサポートするには、Access にかなりの変更を加える必要があります。

これらの理由から、AccessはADPをサポートしていません。 ADPは、設備内の環境でSQL Serverを操作するための優れたツールです。ただし、ADPがAccess 2000で導入されてから、多くの点が変わりました。 今日では、ユーザーがどこにいてもデータベースを利用できることが必要となっています。

## <a name="adp-support-and-the-future"></a>ADP サポートと機能

ADP は旧バージョンの Access では引き続き機能します。ADP アプリケーションをこれまでとおり開発でき、旧バージョンの Access に関しては標準の[サポート ライフサイクル](https://support.microsoft.com/lifecycle/search)に基づいてサポートが引き続き提供されます。新しいバージョンの SQL Server または SQL Azure をサポートするように旧バージョンの Access を更新する予定はありません。そのため、SQL Server 2012 以降のバージョンとともに ADP を使用すると、問題が生じる可能性があります。ADP は今後も SQL 2008 R2 以前をサポートします。

今後、ADP 開発者は次のようないくつかの可能性について考慮できます。

- **Accessアプリケーションへの変換**  -  Accessを使用すると、テーブルを新しいAccessアプリケーションにインポートできます。アプリケーション用のフォームが自動的に作成されます。 Accessが作成した基本型の機能を拡張したり、ユーザーがWeb上で自分のアプリケーションを使用したりできます。 ADP で使用している一部の機能は利用できなくなることがありますが、Microsoft はこのアプリケーションの種類の製品において引き続き鋭意改善を図っています。

- **接続済みデスクトップデータベースへの変換**  -  Accessは引き続き.accdbファイル形式のデスクトップデータベースの作成をサポートします。 ご使用のアプリケーションを (すべての既存のフォームとレポートを含めて) .accdb 形式に変換し、データは SQL Server に残しておくことができます。 リンクテーブルを使用してSQL Serverデータベースに接続すると、アプリケーションは引き続き同じデータに対して機能します。

- **ハイブリッドアプリケーションの作成**  - アプリケーションが大規模で、すべてを同時に変換したくない場合は、データをAccessアプリケーションにインポートし、.accdbからSQL Serverデータベースに接続できます。 これにより、Accessアプリケーションの直下にあるSQL Serverデータベースへのリンクテーブルを持つ.accdbとしてのクライアントアプリケーションを維持しながら、Accessアプリケーションにフォームと機能を追加し徐々に移行をしていくことができます。

- **.NET Frameworkへのアップグレード**  - ご使用のアプリケーションは、.NET Frameworkなどの専門的な開発プラットフォームへの移行を検討するのに十分な複雑さがあるかもしれません。 SQL Serverは、コードを大幅に書き直すことなく、既存のデータベースインフラストラクチャを簡単に使用してアプリケーションの機能を拡張できるように設計されています。

## <a name="conclusion"></a>まとめ

Access は、SharePoint Server と SQL Server のテクノロジに基づいてデータベースをクラウドで接続し、Office 365 と円滑に連動するように設計されています。Access は、お客様のビジネス遂行に役立つデータに基づいたビジネス アプリを迅速に作成および共有できる設計になっています。

## <a name="see-also"></a>関連項目

- [Access 2013 の開発者向け新機能](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/new-in-access-for-developers)


