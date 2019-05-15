---
title: Access の変更点 (Access デスクトップ データベース リファレンス)
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
# <a name="changes-in-access"></a><span data-ttu-id="1a641-104">Access の変更点</span><span class="sxs-lookup"><span data-stu-id="1a641-104">Changes in Access</span></span>

<span data-ttu-id="1a641-105">**適用対象:** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1a641-105">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1a641-106">Access は、Access Data Projects (ADP) をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="1a641-106">Access does not include support for Access Data Projects (ADPs).</span></span> <span data-ttu-id="1a641-107">Access では、Web ベースの Access アプリを作成できるようにするための新しいアプリケーションの種類が導入されています。</span><span class="sxs-lookup"><span data-stu-id="1a641-107">Access introduces a new application type that enables you to create a web-based Access app.</span></span> <span data-ttu-id="1a641-108">この種類のアプリケーションを使用すると、オンプレミスまたはクラウドで SQL Server の機能を使用する Web ベースのアプリケーションを作成できます。</span><span class="sxs-lookup"><span data-stu-id="1a641-108">By using this application type, you can create web-based applications that use the power of SQL Server on premise or in the cloud.</span></span>

<span data-ttu-id="1a641-109">SharePoint Server 上の Access アプリでは、Access クライアントでテーブル、クエリ、またはデータ マクロを作成するときは、SQL Server データベースにテーブル、ビュー、またはトリガーが作成されます。Access クライアントを使用すると、使用しているデータベースを、SQL Server に接続する他のアプリケーションに対してオープンにすることができます。</span><span class="sxs-lookup"><span data-stu-id="1a641-109">In an Access app on SharePoint Server, when you create a table, a query or a data macro in the Access client in which you are creating tables, views or triggers in a SQL Server database. Using the Access client, you can open your database to other applications that connect to SQL Server. This enables you to share your data or load data from other systems into your Access app.</span></span> <span data-ttu-id="1a641-110">これにより、データを共有したり、他のシステムから Access アプリにデータをロードしたりすることが可能になります。</span><span class="sxs-lookup"><span data-stu-id="1a641-110">This enables you to share your data or load data from other systems into your Access app.</span></span>

<span data-ttu-id="1a641-p104">Office 365 と Access を使用すると、ユーザーに配信するアプリケーションを、展開に関する課題、ソフトウェア インストールの問題、オペレーティング システムの互換性などについて心配することなくビルドできます。1 つの場所でアプリをビルドし、それを SQL Azure や SQL Server の機能を活用して Web 上で共有します。</span><span class="sxs-lookup"><span data-stu-id="1a641-p104">With Office 365 and Access, you can build applications that reach your users without having to worry about deployment challenges, software installation issues, or operating system compatibilities. Build your app in one location and share it across the web with the power of SQL Azure and SQL Server.</span></span>

<span data-ttu-id="1a641-p105">SQL Server のクラウド版である[SQL Azure](https://docs.microsoft.com/azure/sql-database/sql-database-technical-overview) は、Access Data Projects (ADP) が処理をするために依存する機能をサポートしていません。SQL Azure で ADP をサポートするには、Access にかなりの変更を加える必要があります。</span><span class="sxs-lookup"><span data-stu-id="1a641-p105">[SQL Azure](https://docs.microsoft.com/azure/sql-database/sql-database-technical-overview), the cloud version of SQL Server, does not support features that Access Data Projects (ADPs) rely on to operate. To support ADPs on SQL Azure, Access would require significant changes.</span></span>

<span data-ttu-id="1a641-115">このような理由から、Access は ADP をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="1a641-115">For these reasons, Access does not support ADPs.</span></span> <span data-ttu-id="1a641-116">ADP はオンプレミス環境で SQL Server を使用して作業するための優れたツールでしたが、Access 2000 に ADP が導入されたときとは、状況がだいぶ異なってきています。</span><span class="sxs-lookup"><span data-stu-id="1a641-116">ADPs have been a great tool for working with SQL Server in an on-premise environment, however much has changed since ADPs were introduced in Access 2000.</span></span> <span data-ttu-id="1a641-117">今日では、ユーザーがどこにいてもデータベースを利用できることが必要となっています。</span><span class="sxs-lookup"><span data-stu-id="1a641-117">Users now expect their database to be available wherever they are.</span></span>

## <a name="adp-support-and-the-future"></a><span data-ttu-id="1a641-118">ADP サポートと機能</span><span class="sxs-lookup"><span data-stu-id="1a641-118">ADP support and the future</span></span>

<span data-ttu-id="1a641-p107">ADP は旧バージョンの Access では引き続き機能します。ADP アプリケーションをこれまでとおり開発でき、旧バージョンの Access に関しては標準の[サポート ライフサイクル](https://support.microsoft.com/lifecycle/search)に基づいてサポートが引き続き提供されます。新しいバージョンの SQL Server または SQL Azure をサポートするように旧バージョンの Access を更新する予定はありません。そのため、SQL Server 2012 以降のバージョンとともに ADP を使用すると、問題が生じる可能性があります。ADP は今後も SQL 2008 R2 以前をサポートします。</span><span class="sxs-lookup"><span data-stu-id="1a641-p107">ADPs continue to work in earlier versions of Access. You can continue to develop your ADP applications and we will continue to support earlier versions of Access under the standard [support lifecycle](https://support.microsoft.com/lifecycle/search). We will not update older versions of Access to support new versions of SQL Server or SQL Azure. Therefore, you may encounter issues if you use SQL Server 2012 or later versions with your ADP. ADPs will continue to support SQL 2008 R2 and earlier.</span></span>

<span data-ttu-id="1a641-124">今後、ADP 開発者は次のようないくつかの可能性について考慮できます。</span><span class="sxs-lookup"><span data-stu-id="1a641-124">For the future, ADP developers can consider several different possibilities:</span></span>

- <span data-ttu-id="1a641-125">**Access アプリへの変換** - Access を使用してテーブルを新しい Access アプリにインポートすると、アプリケーション用のフォームが自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="1a641-125">**Convert to an Access app** - Using Access, you can import your tables into a new Access app and forms for your application are automatically created for you.</span></span> <span data-ttu-id="1a641-126">Access によって作成された基本的なフォームの機能を拡張し、ユーザーが Web 上でそのアプリケーションを使用できるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="1a641-126">You can extend the functionality of the base forms Access creates for you and users can use your application on the web.</span></span> <span data-ttu-id="1a641-127">ADP で使用している一部の機能は利用できなくなることがありますが、Microsoft はこのアプリケーションの種類の製品において引き続き鋭意改善を図っています。</span><span class="sxs-lookup"><span data-stu-id="1a641-127">Although some of the functionality that you use in ADPs may not be available now, expect Microsoft to continue to focus improvements in the product for this application type.</span></span>

- <span data-ttu-id="1a641-128">**リンクされたデスクトップ データベースへの変換** - Access では、.accdb ファイル形式のデスクトップ データベースの作成が引き続きサポートされています。</span><span class="sxs-lookup"><span data-stu-id="1a641-128">**Convert to a linked desktop database** - Access continues to support creating desktop databases in the .accdb file format.</span></span> <span data-ttu-id="1a641-129">ご使用のアプリケーションを (すべての既存のフォームとレポートを含めて) .accdb 形式に変換し、データは SQL Server に残しておくことができます。</span><span class="sxs-lookup"><span data-stu-id="1a641-129">You can convert your application to the .accdb format, including all of your existing forms and reports, and leave the data in SQL Server.</span></span> <span data-ttu-id="1a641-130">リンク テーブルを使用して SQL Server データベースにリンクできるため、アプリケーションは引き続き同じデータに対して操作を行えます。</span><span class="sxs-lookup"><span data-stu-id="1a641-130">You can link to the SQL Server database using linked tables and your application will continue to operate against the same data.</span></span>

- <span data-ttu-id="1a641-131">**ハイブリッド アプリケーションの作成** - アプリケーションが大規模で、一度にすべてを変換したくない場合は、Access アプリにデータをインポートし、.accdb から SQL Server データベースにリンクできます。</span><span class="sxs-lookup"><span data-stu-id="1a641-131">**Create a hybrid application** - If your application is large and you don't want to convert everything at the same time, you can import your data into an Access app and link to the SQL Server database from an .accdb.</span></span> <span data-ttu-id="1a641-132">これは、段階的な移行が可能で、Access アプリの背後にある SQL Server データベースにリンクされたテーブルを使用してクライアント アプリケーションを .accdb として保持しながら、Access アプリに対して徐々にフォームや機能を追加していくことができます。</span><span class="sxs-lookup"><span data-stu-id="1a641-132">This allows you migrate gradually, adding forms and functionality over time to your Access app while maintaining your client application as an .accdb with linked tables to the SQL Server database behind the Access app.</span></span>

- <span data-ttu-id="1a641-133">**.NET Framework へのアップグレード** - アプリケーションが複雑な場合は, .NET Framework などの専門的な開発プラットフォームへの移行を考慮することができます。</span><span class="sxs-lookup"><span data-stu-id="1a641-133">**Upgrade to the .NET Framework** - Your application may be complex enough that to consider moving to a professional development platform such as the .NET Framework.</span></span> <span data-ttu-id="1a641-134">SQL Server は、既存のデータベース インフラストラクチャを使用して、大規模なコード書き換えをせずにアプリケーションの機能を簡単に拡張できるように設計されています。</span><span class="sxs-lookup"><span data-stu-id="1a641-134">SQL Server is designed to make it easier for you to use your existing database infrastructure you've already created and extend the functionality of your application without having to significantly rewrite your code.</span></span>

## <a name="conclusion"></a><span data-ttu-id="1a641-135">まとめ</span><span class="sxs-lookup"><span data-stu-id="1a641-135">Conclusion</span></span>

<span data-ttu-id="1a641-p112">Access は、SharePoint Server と SQL Server のテクノロジに基づいてデータベースをクラウドで接続し、Office 365 と円滑に連動するように設計されています。Access は、お客様のビジネス遂行に役立つデータに基づいたビジネス アプリを迅速に作成および共有できる設計になっています。</span><span class="sxs-lookup"><span data-stu-id="1a641-p112">Access is designed to connect databases with the cloud by building on SharePoint Server and SQL Server technologies and easily work with Office 365. Access is designed to help you quickly create and share data-driven business apps that help run your business.</span></span>

## <a name="see-also"></a><span data-ttu-id="1a641-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="1a641-138">See also</span></span>

- [<span data-ttu-id="1a641-139">Access 2013 の開発者向け新機能</span><span class="sxs-lookup"><span data-stu-id="1a641-139">New in Access 2013 for developers</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/new-in-access-for-developers)


