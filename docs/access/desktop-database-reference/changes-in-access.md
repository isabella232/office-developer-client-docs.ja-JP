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
# <a name="changes-in-access"></a><span data-ttu-id="08868-104">Access における変更点</span><span class="sxs-lookup"><span data-stu-id="08868-104">Changes in Access</span></span>

<span data-ttu-id="08868-105">**に適用されます:** Access 2013 |Office 2013</span><span class="sxs-lookup"><span data-stu-id="08868-105">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="08868-106">Access は、Access Data Projects (ADP) をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="08868-106">Access does not include support for Access Data Projects (ADPs).</span></span> <span data-ttu-id="08868-107">Access では、Web ベースの Access アプリを作成できるようにするための新しいアプリケーションの種類が導入されています。</span><span class="sxs-lookup"><span data-stu-id="08868-107">Access introduces a new application type that enables you to create a web-based Access app.</span></span> <span data-ttu-id="08868-108">このアプリケーションの種類を使用すると、SQL Server の設置型またはクラウドでの電力を使用する web ベースのアプリケーションを作成できます。</span><span class="sxs-lookup"><span data-stu-id="08868-108">By using this application type, you can create web-based applications that use the power of SQL Server on-premises or in the cloud.</span></span>

<span data-ttu-id="08868-109">SharePoint サーバー上のアクセス アプリケーションを作成するテーブル、ビュー、または SQL Server データベース内のトリガー、アクセス クライアントを使用して、アクセス クライアントでテーブル、クエリ、またはデータ マクロを作成するときに開くことができます、データベースの他のアプリケーションを接続SQL Server への ect。</span><span class="sxs-lookup"><span data-stu-id="08868-109">In an Access app on SharePoint Server, when you create a table, a query, or a data macro in the Access client in which you are creating tables, views, or triggers in a SQL Server database, by using the Access client, you can open your database to other applications that connect to SQL Server.</span></span> <span data-ttu-id="08868-110">これにより、データを共有したり、他のシステムから Access アプリにデータをロードしたりすることが可能になります。</span><span class="sxs-lookup"><span data-stu-id="08868-110">This enables you to share your data or load data from other systems into your Access app.</span></span>

<span data-ttu-id="08868-p104">Office 365 と Access を使用すると、ユーザーに配信するアプリケーションを、展開に関する課題、ソフトウェア インストールの問題、オペレーティング システムの互換性などについて心配することなくビルドできます。1 つの場所でアプリをビルドし、それを SQL Azure や SQL Server の機能を活用して Web 上で共有します。</span><span class="sxs-lookup"><span data-stu-id="08868-p104">With Office 365 and Access, you can build applications that reach your users without having to worry about deployment challenges, software installation issues, or operating system compatibilities. Build your app in one location and share it across the web with the power of SQL Azure and SQL Server.</span></span>

<span data-ttu-id="08868-p105">SQL Server のクラウド版である[SQL Azure](https://docs.microsoft.com/azure/sql-database/sql-database-technical-overview) は、Access Data Projects (ADP) が処理をするために依存する機能をサポートしていません。SQL Azure で ADP をサポートするには、Access にかなりの変更を加える必要があります。</span><span class="sxs-lookup"><span data-stu-id="08868-p105">[SQL Azure](https://docs.microsoft.com/azure/sql-database/sql-database-technical-overview), the cloud version of SQL Server, does not support features that Access Data Projects (ADPs) rely on to operate. To support ADPs on SQL Azure, Access would require significant changes.</span></span>

<span data-ttu-id="08868-115">これらの理由で、Access は ADP をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="08868-115">For these reasons, Access does not support ADPs.</span></span> <span data-ttu-id="08868-116">Adp は、オンプレミス環境で SQL Server を使用するための優れたツールをされています。ただし、Adp が Access 2000 で導入されたために、多くが変更されました。</span><span class="sxs-lookup"><span data-stu-id="08868-116">ADPs have been a great tool for working with SQL Server in an on-premises environment; however, much has changed since ADPs were introduced in Access 2000.</span></span> <span data-ttu-id="08868-117">今日では、ユーザーがどこにいてもデータベースを利用できることが必要となっています。</span><span class="sxs-lookup"><span data-stu-id="08868-117">Users now expect their database to be available wherever they are.</span></span>

## <a name="adp-support-and-the-future"></a><span data-ttu-id="08868-118">ADP サポートと機能</span><span class="sxs-lookup"><span data-stu-id="08868-118">ADP support and the future</span></span>

<span data-ttu-id="08868-p107">ADP は旧バージョンの Access では引き続き機能します。ADP アプリケーションをこれまでとおり開発でき、旧バージョンの Access に関しては標準の[サポート ライフサイクル](https://support.microsoft.com/lifecycle/search)に基づいてサポートが引き続き提供されます。新しいバージョンの SQL Server または SQL Azure をサポートするように旧バージョンの Access を更新する予定はありません。そのため、SQL Server 2012 以降のバージョンとともに ADP を使用すると、問題が生じる可能性があります。ADP は今後も SQL 2008 R2 以前をサポートします。</span><span class="sxs-lookup"><span data-stu-id="08868-p107">ADPs continue to work in earlier versions of Access. You can continue to develop your ADP applications and we will continue to support earlier versions of Access under the standard [support lifecycle](https://support.microsoft.com/lifecycle/search). We will not update older versions of Access to support new versions of SQL Server or SQL Azure. Therefore, you may encounter issues if you use SQL Server 2012 or later versions with your ADP. ADPs will continue to support SQL 2008 R2 and earlier.</span></span>

<span data-ttu-id="08868-124">今後、ADP 開発者は次のようないくつかの可能性について考慮できます。</span><span class="sxs-lookup"><span data-stu-id="08868-124">For the future, ADP developers can consider several different possibilities:</span></span>

- <span data-ttu-id="08868-125">**アクセス アプリケーションに変換する**-を使用してアクセス、アクセスの新しいアプリケーションに、テーブルをインポートすることし、アプリケーションのフォームが自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="08868-125">**Convert to an Access app** – Using Access, you can import your tables into a new Access app, and forms for your application are automatically created for you.</span></span> <span data-ttu-id="08868-126">アクセスを作成するには、基本フォームの機能を拡張することができ、ユーザーは web 上で、アプリケーションを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="08868-126">You can extend the functionality of the base forms that Access creates for you, and users can use your application on the web.</span></span> <span data-ttu-id="08868-127">ADP で使用している一部の機能は利用できなくなることがありますが、Microsoft はこのアプリケーションの種類の製品において引き続き鋭意改善を図っています。</span><span class="sxs-lookup"><span data-stu-id="08868-127">Although some of the functionality that you use in ADPs may not be available now, expect Microsoft to continue to focus improvements in the product for this application type.</span></span>

- <span data-ttu-id="08868-128">**リンクされているデスクトップ ・ データベースへの変換**: アクセスは、.accdb ファイル形式でのデスクトップのデータベースの作成をサポートするために継続します。</span><span class="sxs-lookup"><span data-stu-id="08868-128">**Convert to a linked desktop database** – Access continues to support creating desktop databases in the .accdb file format.</span></span> <span data-ttu-id="08868-129">ご使用のアプリケーションを (すべての既存のフォームとレポートを含めて) .accdb 形式に変換し、データは SQL Server に残しておくことができます。</span><span class="sxs-lookup"><span data-stu-id="08868-129">You can convert your application to the .accdb format, including all of your existing forms and reports, and leave the data in SQL Server.</span></span> <span data-ttu-id="08868-130">リンク テーブルを使用して SQL Server データベースにリンクすることができ、同じデータを操作する、アプリケーションが続行されます。</span><span class="sxs-lookup"><span data-stu-id="08868-130">You can link to the SQL Server database by using linked tables, and your application will continue to operate against the same data.</span></span>

- <span data-ttu-id="08868-131">**ハイブリッド アプリケーションを作成する**– アプリケーションのサイズが大きく、すべてを同時に変換したくない場合、することができますからデータをインポート、Access アプリケーションとのリンクに SQL Server データベースに、.accdb です。</span><span class="sxs-lookup"><span data-stu-id="08868-131">**Create a hybrid application** – If your application is large and you don’t want to convert everything at the same time, you can import your data into an Access app and link to the SQL Server database from an .accdb.</span></span> <span data-ttu-id="08868-132">これにより、移行に追加するフォームおよび機能時間の経過と共にアクセス アプリでは、Access アプリケーションの背後にある SQL Server データベースにリンク テーブルを使用する .accdb ファイルとしてクライアント アプリケーションを維持しながら徐々 になります。</span><span class="sxs-lookup"><span data-stu-id="08868-132">This allows you migrate gradually, adding forms and functionality over time to your Access app, while maintaining your client application as an .accdb with linked tables to the SQL Server database behind the Access app.</span></span>

- <span data-ttu-id="08868-133">**.NET Framework へのアップグレード**: アプリケーションは、.NET Framework などの本格的な開発プラットフォームへの移行を検討するのに十分な複雑な可能性があります。</span><span class="sxs-lookup"><span data-stu-id="08868-133">**Upgrade to the .NET Framework** – Your application may be complex enough to consider moving to a professional development platform such as the .NET Framework.</span></span> <span data-ttu-id="08868-134">SQL Server は、既存のデータベース インフラストラクチャを使用し、コードを大幅に書き直すことがなく、アプリケーションの機能を拡張することを容易にできるように設計されています。</span><span class="sxs-lookup"><span data-stu-id="08868-134">SQL Server is designed to make it easier for you to use your existing database infrastructure and extend the functionality of your application without having to significantly rewrite your code.</span></span>

## <a name="conclusion"></a><span data-ttu-id="08868-135">まとめ</span><span class="sxs-lookup"><span data-stu-id="08868-135">Conclusion</span></span>

<span data-ttu-id="08868-p112">Access は、SharePoint Server と SQL Server のテクノロジに基づいてデータベースをクラウドで接続し、Office 365 と円滑に連動するように設計されています。Access は、お客様のビジネス遂行に役立つデータに基づいたビジネス アプリを迅速に作成および共有できる設計になっています。</span><span class="sxs-lookup"><span data-stu-id="08868-p112">Access is designed to connect databases with the cloud by building on SharePoint Server and SQL Server technologies and easily work with Office 365. Access is designed to help you quickly create and share data-driven business apps that help run your business.</span></span>

## <a name="see-also"></a><span data-ttu-id="08868-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="08868-138">See also</span></span>

- [<span data-ttu-id="08868-139">Access 2013 の開発者向け新機能</span><span class="sxs-lookup"><span data-stu-id="08868-139">New in Access 2013 for developers</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/new-in-access-for-developers)


