---
title: アクセス (アクセス デスクトップ データベース参照) に変更
TOCTitle: Changes in Access
ms:assetid: 8dfc5fc9-a6a7-4a91-8e97-c3874e9b880f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ618413(v=office.15)
ms:contentKeyID: 49106417
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3363d1bc3e9b2157ce8d7855a588b98a819246e9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478677"
---
# <a name="changes-in-access"></a>アクセスの変更

**に適用されます:** Access 2013 |Office 2013

Access は、Access Data Projects (ADP) をサポートしていません。Access では、Web ベースの Access アプリを作成できるようにするための新しいアプリケーションの種類が導入されています。このアプリケーションの種類を使用すると、オンプレミスまたはクラウドにおいて SQL Server の機能を活用する Web ベースのアプリケーションを作成できます。

Access では、Web ベースの Access アプリを作成できるようにするための新しいアプリケーションの種類が導入されています。このアプリケーションの種類を使用すると、オンプレミスまたはクラウドにおいて SQL Server の機能を活用する Web ベースのアプリケーションを作成できます。

SharePoint Server 上の Access アプリにおいて、Access クライアントでテーブル、クエリ、またはデータ マクロを作成するときは、SQL Server データベースにテーブル、ビュー、またはトリガーが作成されることになります。Access クライアントを使用すると、使用しているデータベースを、SQL Server に接続する他のアプリケーションに対してオープンにすることができます。これにより、データを共有したり、他のシステムから Access アプリにデータをロードしたりすることが可能になります。

Office 365 と Access を使用すると、ユーザーに配信するアプリケーションを、展開に関する課題、ソフトウェア インストールの問題、オペレーティング システムの互換性などについて心配することなくビルドできます。1 つの場所でアプリをビルドし、それを SQL Azure や SQL Server の機能を活用して Web 上で共有します。

SQL Server のクラウド版である[SQL Azure](https://msdn.microsoft.com/library/azure/ee336279.aspx) は、Access Data Projects (ADP) が処理をするために依存する機能をサポートしていません。SQL Azure で ADP をサポートするには、Access にかなりの変更を加える必要があります。

これらの理由で、Access は ADP をサポートしていません。ADP はオンプレミス環境において SQL Server を用いて作業するための優れたツールでしたが、Access 2000 に ADP が導入されたときとは、状況がだいぶ異なってきています。今日では、ユーザーがどこにいてもデータベースを利用できることが必要となっています。

## <a name="adp-support-and-the-future"></a>ADP サポートと機能

ADP は旧バージョンの Access では引き続き機能します。ADP アプリケーションをこれまでとおり開発でき、旧バージョンの Access に関しては標準の[サポート ライフサイクル](https://support.microsoft.com/gp/lifeselect)に基づいてサポートが引き続き提供されます。新しいバージョンの SQL Server または SQL Azure をサポートするように旧バージョンの Access を更新する予定はありません。そのため、SQL Server 2012 以降のバージョンとともに ADP を使用すると、問題が生じる可能性があります。ADP は今後も SQL 2008 R2 以前をサポートします。

今後、ADP 開発者は次のようないくつかの可能性について考慮できます。

- **アクセス アプリケーションに変換する**-を使用してアクセス、アクセス アプリケーションを新規にテーブルをインポートすることし、アプリケーションのフォームが自動的に作成されます。 Access によって作成された基本的なフォームの機能を拡張し、ユーザーが Web 上でそのアプリケーションを使用できるようにすることができます。 ADP で使用している一部の機能は利用できなくなることがありますが、Microsoft はこのアプリケーションの種類の製品において引き続き鋭意改善を図っています。

- **リンクされているデスクトップ ・ データベースへの変換**: アクセスは、.accdb ファイル形式でのデスクトップのデータベースの作成をサポートするために継続します。 ご使用のアプリケーションを (すべての既存のフォームとレポートを含めて) .accdb 形式に変換し、データは SQL Server に残しておくことができます。 リンク テーブルを使用して SQL Server データベースにリンクできるため、アプリケーションは引き続き同じデータに対して操作を行えます。

- **ハイブリッド アプリケーションを作成する**– アプリケーションのサイズが大きく、すべてを同時に変換したくない場合、することができますからデータをインポート、Access アプリケーションとのリンクに SQL Server データベースに、.accdb です。 このようにすると、段階的な移行が可能で、Access アプリの背後にある SQL Server データベースにリンクされたテーブルを使用してクライアント アプリケーションを .accdb として保持しながら、Access アプリに対して徐々にフォームや機能を追加していくことができます。

- **.NET Framework へのアップグレード**: アプリケーションは複雑になる可能性がありますを.NET Framework などの本格的な開発プラットフォームへの移行を検討するための十分な。 SQL Server は、既に作成しているし、コードを大幅に書き直すことがなく、アプリケーションの機能を拡張する、既存のデータベース インフラストラクチャを使用することを簡単に設計されています。

## <a name="conclusion"></a>まとめ

Access は、SharePoint Server と SQL Server のテクノロジに基づいてデータベースをクラウドで接続し、Office 365 と円滑に連動するように設計されています。Access は、お客様のビジネス遂行に役立つデータに基づいたビジネス アプリを迅速に作成および共有できる設計になっています。

## <a name="see-also"></a>関連項目

- [Access 2013 の開発者向け新機能](https://msdn.microsoft.com/library/jj250134\(v=office.15\))
- [Microsoft サポート ライフサイクル](https://support.microsoft.com/lifecycle/)
- [Microsoft Azure SQL データベース](https://msdn.microsoft.com/library/azure/ee336279.aspx)

