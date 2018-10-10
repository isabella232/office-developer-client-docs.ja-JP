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
# <a name="changes-in-access"></a><span data-ttu-id="23e9f-102">アクセスの変更</span><span class="sxs-lookup"><span data-stu-id="23e9f-102">Changes in Access</span></span>

<span data-ttu-id="23e9f-103">**に適用されます:** Access 2013 |Office 2013</span><span class="sxs-lookup"><span data-stu-id="23e9f-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="23e9f-p101">Access は、Access Data Projects (ADP) をサポートしていません。Access では、Web ベースの Access アプリを作成できるようにするための新しいアプリケーションの種類が導入されています。このアプリケーションの種類を使用すると、オンプレミスまたはクラウドにおいて SQL Server の機能を活用する Web ベースのアプリケーションを作成できます。</span><span class="sxs-lookup"><span data-stu-id="23e9f-p101">Access does not include support for Access Data Projects (ADPs). Access introduces a new application type that enables you to create a web-based Access app. By using this application type, you can create web-based applications that use the power of SQL Server on premise or in the cloud.</span></span>

<span data-ttu-id="23e9f-p102">Access では、Web ベースの Access アプリを作成できるようにするための新しいアプリケーションの種類が導入されています。このアプリケーションの種類を使用すると、オンプレミスまたはクラウドにおいて SQL Server の機能を活用する Web ベースのアプリケーションを作成できます。</span><span class="sxs-lookup"><span data-stu-id="23e9f-p102">Access introduces a new application type that enables you to create a web-based Access app. By using this application type, you can create web-based applications that use the power of SQL Server on premise or in the cloud.</span></span>

<span data-ttu-id="23e9f-p103">SharePoint Server 上の Access アプリにおいて、Access クライアントでテーブル、クエリ、またはデータ マクロを作成するときは、SQL Server データベースにテーブル、ビュー、またはトリガーが作成されることになります。Access クライアントを使用すると、使用しているデータベースを、SQL Server に接続する他のアプリケーションに対してオープンにすることができます。これにより、データを共有したり、他のシステムから Access アプリにデータをロードしたりすることが可能になります。</span><span class="sxs-lookup"><span data-stu-id="23e9f-p103">In an Access app on SharePoint Server, when you create a table, a query or a data macro in the Access client in which you are creating tables, views or triggers in a SQL Server database. Using the Access client, you can open your database to other applications that connect to SQL Server. This enables you to share your data or load data from other systems into your Access app.</span></span>

<span data-ttu-id="23e9f-p104">Office 365 と Access を使用すると、ユーザーに配信するアプリケーションを、展開に関する課題、ソフトウェア インストールの問題、オペレーティング システムの互換性などについて心配することなくビルドできます。1 つの場所でアプリをビルドし、それを SQL Azure や SQL Server の機能を活用して Web 上で共有します。</span><span class="sxs-lookup"><span data-stu-id="23e9f-p104">With Office 365 and Access, you can build applications that reach your users without having to worry about deployment challenges, software installation issues, or operating system compatibilities. Build your app in one location and share it across the web with the power of SQL Azure and SQL Server.</span></span>

<span data-ttu-id="23e9f-p105">SQL Server のクラウド版である[SQL Azure](https://msdn.microsoft.com/library/azure/ee336279.aspx) は、Access Data Projects (ADP) が処理をするために依存する機能をサポートしていません。SQL Azure で ADP をサポートするには、Access にかなりの変更を加える必要があります。</span><span class="sxs-lookup"><span data-stu-id="23e9f-p105">[SQL Azure](https://msdn.microsoft.com/library/azure/ee336279.aspx), the cloud version of SQL Server, does not support features that Access Data Projects (ADPs) rely on to operate. To support ADPs on SQL Azure, Access would require significant changes.</span></span>

<span data-ttu-id="23e9f-p106">これらの理由で、Access は ADP をサポートしていません。ADP はオンプレミス環境において SQL Server を用いて作業するための優れたツールでしたが、Access 2000 に ADP が導入されたときとは、状況がだいぶ異なってきています。今日では、ユーザーがどこにいてもデータベースを利用できることが必要となっています。</span><span class="sxs-lookup"><span data-stu-id="23e9f-p106">For these reasons, Access does not support ADPs. ADPs have been a great tool for working with SQL Server in an on-premise environment, however much has changed since ADPs were introduced in Access 2000. Users now expect their database to be available wherever they are.</span></span>

## <a name="adp-support-and-the-future"></a><span data-ttu-id="23e9f-119">ADP サポートと機能</span><span class="sxs-lookup"><span data-stu-id="23e9f-119">ADP support and the future</span></span>

<span data-ttu-id="23e9f-p107">ADP は旧バージョンの Access では引き続き機能します。ADP アプリケーションをこれまでとおり開発でき、旧バージョンの Access に関しては標準の[サポート ライフサイクル](https://support.microsoft.com/gp/lifeselect)に基づいてサポートが引き続き提供されます。新しいバージョンの SQL Server または SQL Azure をサポートするように旧バージョンの Access を更新する予定はありません。そのため、SQL Server 2012 以降のバージョンとともに ADP を使用すると、問題が生じる可能性があります。ADP は今後も SQL 2008 R2 以前をサポートします。</span><span class="sxs-lookup"><span data-stu-id="23e9f-p107">ADPs continue to work in earlier versions of Access. You can continue to develop your ADP applications and we will continue to support earlier versions of Access under the standard [support lifecycle](https://support.microsoft.com/gp/lifeselect). We will not update older versions of Access to support new versions of SQL Server or SQL Azure. Therefore, you may encounter issues if you use SQL Server 2012 or later versions with your ADP. ADPs will continue to support SQL 2008 R2 and earlier.</span></span>

<span data-ttu-id="23e9f-125">今後、ADP 開発者は次のようないくつかの可能性について考慮できます。</span><span class="sxs-lookup"><span data-stu-id="23e9f-125">For the future, ADP developers can consider several different possibilities:</span></span>

- <span data-ttu-id="23e9f-126">**アクセス アプリケーションに変換する**-を使用してアクセス、アクセス アプリケーションを新規にテーブルをインポートすることし、アプリケーションのフォームが自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="23e9f-126">**Convert to an Access app** – Using Access, you can import your tables into a new Access app and forms for your application are automatically created for you.</span></span> <span data-ttu-id="23e9f-127">Access によって作成された基本的なフォームの機能を拡張し、ユーザーが Web 上でそのアプリケーションを使用できるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="23e9f-127">You can extend the functionality of the base forms Access creates for you and users can use your application on the web.</span></span> <span data-ttu-id="23e9f-128">ADP で使用している一部の機能は利用できなくなることがありますが、Microsoft はこのアプリケーションの種類の製品において引き続き鋭意改善を図っています。</span><span class="sxs-lookup"><span data-stu-id="23e9f-128">Although some of the functionality that you use in ADPs may not be available now, expect Microsoft to continue to focus improvements in the product for this application type.</span></span>

- <span data-ttu-id="23e9f-129">**リンクされているデスクトップ ・ データベースへの変換**: アクセスは、.accdb ファイル形式でのデスクトップのデータベースの作成をサポートするために継続します。</span><span class="sxs-lookup"><span data-stu-id="23e9f-129">**Convert to a linked desktop database** – Access continues to support creating desktop databases in the .accdb file format.</span></span> <span data-ttu-id="23e9f-130">ご使用のアプリケーションを (すべての既存のフォームとレポートを含めて) .accdb 形式に変換し、データは SQL Server に残しておくことができます。</span><span class="sxs-lookup"><span data-stu-id="23e9f-130">You can convert your application to the .accdb format, including all of your existing forms and reports, and leave the data in SQL Server.</span></span> <span data-ttu-id="23e9f-131">リンク テーブルを使用して SQL Server データベースにリンクできるため、アプリケーションは引き続き同じデータに対して操作を行えます。</span><span class="sxs-lookup"><span data-stu-id="23e9f-131">You can link to the SQL Server database using linked tables and your application will continue to operate against the same data.</span></span>

- <span data-ttu-id="23e9f-132">**ハイブリッド アプリケーションを作成する**– アプリケーションのサイズが大きく、すべてを同時に変換したくない場合、することができますからデータをインポート、Access アプリケーションとのリンクに SQL Server データベースに、.accdb です。</span><span class="sxs-lookup"><span data-stu-id="23e9f-132">**Create a hybrid application** – If your application is large and you don’t want to convert everything at the same time, you can import your data into an Access app and link to the SQL Server database from an .accdb.</span></span> <span data-ttu-id="23e9f-133">このようにすると、段階的な移行が可能で、Access アプリの背後にある SQL Server データベースにリンクされたテーブルを使用してクライアント アプリケーションを .accdb として保持しながら、Access アプリに対して徐々にフォームや機能を追加していくことができます。</span><span class="sxs-lookup"><span data-stu-id="23e9f-133">This allows you migrate gradually, adding forms and functionality over time to your Access app while maintaining your client application as an .accdb with linked tables to the SQL Server database behind the Access app.</span></span>

- <span data-ttu-id="23e9f-134">**.NET Framework へのアップグレード**: アプリケーションは複雑になる可能性がありますを.NET Framework などの本格的な開発プラットフォームへの移行を検討するための十分な。</span><span class="sxs-lookup"><span data-stu-id="23e9f-134">**Upgrade to the .NET Framework** – Your application may be complex enough that to consider moving to a professional development platform such as the .NET Framework.</span></span> <span data-ttu-id="23e9f-135">SQL Server は、既に作成しているし、コードを大幅に書き直すことがなく、アプリケーションの機能を拡張する、既存のデータベース インフラストラクチャを使用することを簡単に設計されています。</span><span class="sxs-lookup"><span data-stu-id="23e9f-135">SQL Server is designed to make it easier for you to use your existing database infrastructure you’ve already created and extend the functionality of your application without having to significantly rewrite your code.</span></span>

## <a name="conclusion"></a><span data-ttu-id="23e9f-136">まとめ</span><span class="sxs-lookup"><span data-stu-id="23e9f-136">Conclusion</span></span>

<span data-ttu-id="23e9f-p112">Access は、SharePoint Server と SQL Server のテクノロジに基づいてデータベースをクラウドで接続し、Office 365 と円滑に連動するように設計されています。Access は、お客様のビジネス遂行に役立つデータに基づいたビジネス アプリを迅速に作成および共有できる設計になっています。</span><span class="sxs-lookup"><span data-stu-id="23e9f-p112">Access is designed to connect databases with the cloud by building on SharePoint Server and SQL Server technologies and easily work with Office 365. Access is designed to help you quickly create and share data-driven business apps that help run your business.</span></span>

## <a name="see-also"></a><span data-ttu-id="23e9f-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="23e9f-139">See also</span></span>

- <span data-ttu-id="23e9f-140">[Access 2013 の開発者向け新機能](https://msdn.microsoft.com/library/jj250134\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="23e9f-140">[New in Access for developers](https://msdn.microsoft.com/library/jj250134\(v=office.15\))</span></span>
- [<span data-ttu-id="23e9f-141">Microsoft サポート ライフサイクル</span><span class="sxs-lookup"><span data-stu-id="23e9f-141">Microsoft Support Lifecycle</span></span>](https://support.microsoft.com/lifecycle/)
- [<span data-ttu-id="23e9f-142">Microsoft Azure SQL データベース</span><span class="sxs-lookup"><span data-stu-id="23e9f-142">Microsoft Azure SQL Database</span></span>](https://msdn.microsoft.com/library/azure/ee336279.aspx)

