---
title: Project 2013 開発者向けドキュメント
manager: soliver
ms.date: 04/04/2016
ms.audience: Developer
f1_keywords:
- Project
- Project 2013
- Project 2013 SDK
- Project programmability
- Project SDK
- SDK
- SDK Project
keywords:
- sdk, project 2013,Project 2013, SDK の概要
ms.assetid: f66adbf1-5cb5-4dd0-be08-45e1c88c010c
description: ここには、Office ストア用またはプライベート アプリ カタログ用のアプリを構築するとき、また Project Server および Project クライアントをカスタマイズし、エンタープライズ プロジェクト マネジメント用の他のさまざまなデスクトップ アプリケーションやビジネス アプリケーションと統合するときに役立つドキュメント、コード サンプル、操作方法に関する記事、およびプログラミング リファレンスが含まれています。
localization_priority: Priority
ms.openlocfilehash: cb4dd31a76b897bb5dba39e6b20d0a238bd95293
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707823"
---
# <a name="project-2013-developer-documentation"></a>Project 2013 開発者向けドキュメント

ここには、Office ストア用またはプライベート アプリ カタログ用のアプリを構築するとき、また Project Server および Project クライアントをカスタマイズし、エンタープライズ プロジェクト マネジメント用の他のさまざまなデスクトップ アプリケーションやビジネス アプリケーションと統合するときに役立つドキュメント、コード サンプル、操作方法に関する記事、およびプログラミング リファレンスが含まれています。
  
Microsoft Project 2013 ソフトウェア開発キット (SDK) へようこそ。 この SDK には、パブリック ストア用またはプライベート アプリ カタログ用のアプリを構築するとき、また Project Server および Project クライアントをカスタマイズし、エンタープライズ プロジェクト マネジメント用の他のさまざまなデスクトップ アプリケーションやビジネス アプリケーションと統合するときに役立つドキュメント、コード サンプル、操作方法に関する記事、およびプログラミング リファレンスが含まれています。
  
> [!NOTE]
> Project Server 2013 は SharePoint Server 2013 プラットフォームに基づいて構築され、Project 2013 には他の Office 2013 アプリケーションと同じインストラクチャが数多く含まれています。 SharePoint アドイン、SharePoint ベースのワークフロー、Web パーツ、および他の SharePoint 機能を使用した開発モデルに関するドキュメントについては、「[SharePoint アドイン](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins)」および「[Office アドイン](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins)」をご覧ください。 
  
## <a name="introduction-to-the-project-sdk"></a>Project SDK の概要
<a name="pj15_Welcome_IntroToSDK"> </a>

Project Server 2013 は、オンプレミスまたはクラウド ベースのエンタープライズ プロジェクト管理ソリューションを構築したり、エンドユーザーがパブリック ストアまたはパブリック アプリ カタログを介して検索して取得できるアプリを構築したりするためのプラットフォームです。 Project Server 2013 アーキテクチャは、Microsoft Office Project Server 2007 で導入された、多くの追加機能や強化点が含まれるプラットフォームに基づいています。 新機能には、Project Online へのアクセスを可能にするクライアント側オブジェクト モデル (CSOM)、Project Server レポート データにオンラインでアクセスするための OData サービス、リモート イベント レシーバー、Windows Workflow Foundation バージョン 4 (WF4) に基づくワークフロー アーキテクチャ、Microsoft Office 2013 クライアント アプリケーションの作業ウィンドウ拡張機能で共通のアーキテクチャである Office アドインなどが含まれます。
  
Project Server 2013 における主要な変更点の 1 つは、Project Server 2010 での下書きデータベース、発行済みデータベース、アーカイブ データベース、レポート データベースに代わり単一のデータベースを使用するという点です。 新機能と廃止された機能について詳しくは、「[Project 2013 における開発者向けの更新内容](updates-for-developers-in-project-2013.md)」をご覧ください。 Project Server プラットフォームの変更点については、「[Project Server 2013 のアーキテクチャ](project-server-2013-architecture.md)」を参照してください。 Project Server 2010 に存在し、Project Server 2013 の基盤となっているプラットフォームの概要については、MSDN の 「[Project 2010 の開発を開始する](https://msdn.microsoft.com/library/gg607685.aspx)」をご覧ください。 
  
Project Server 2013 は Microsoft .NET Framework 4 と Microsoft SharePoint Server 2013 に基づいて構築されています。 この SDK に含まれる記事とサンプルは、カスタム ソリューションおよびアプリを開発するための開始点を提供するものであり、Project Server や Project Professional のすべてのプログラム機能が説明されているわけではありません。 [Project デベロッパー センター](https://msdn.microsoft.com/library/4e5245c3-4891-455b-b321-1819cdd77247.aspx)には、Project に関する記事、ブログ、ビデオ、Web キャスト、操作方法に関するビジュアルな記事、およびその他のリソースへのリンクが含まれています。 
  
Project 2013 SDK には、Project Server 2013、Project Web App、Project Professional 2013、Project Standard 2013 の開発者向けの情報が含まれています。 SDK の記事は、開発者や管理者が Project および Project Server の拡張性を評価して、カスタム ソリューションを計画できるようにすることを目的としています。
  
### <a name="feedback"></a>フィードバック
<a name="pj15_Welcome_Feedback"> </a>

皆さまからのご意見をぜひ伺いたいと考えています。 MSDN のオンライン トピックでは、コメントやコード サンプルを追加したり、各ページの下部にある **[コミュニティ コンテンツ]** セクションでコンテンツにバグのフラグを設定したりできます。 ダウンロードした Project 2013 SDK をインストールすると、それぞれのローカル ドキュメント記事には、タイトルの下に*フィードバックの送信*リンクが表示されます。 SDK を閲覧するときにはいつでも、このリンクを選択して SDK チームに電子メールを送信できます。 修正点、明確にしてほしい点に関するリクエスト、コード サンプル、他のコメントをお送りいただけます。こうして点はコンテンツをより優れたものにするのに役立ちます。 
  
### <a name="download"></a>ダウンロード
<a name="pj15_Welcome_Download"> </a>

Project 2013 SDK のダウンロードは [Microsoft ダウンロード センター](https://www.microsoft.com/en-us/download/details.aspx?id=30435%20) (`https://www.microsoft.com/en-us/download/details.aspx?id=30435%20`) で行えます。 ダウンロードには、Project2013SDK.HxS (この記事が含まれるファイル)、関連するコード サンプル、再頒布可能アセンブリなどのリソースが含まれています。 Project 2013 SDK にはレポート データベースに関するリファレンスはまだ含まれていません。
  
### <a name="whats-new-in-the-project-sdk"></a>Project SDK の新機能
<a name="pj15_Welcome_WhatsNew"> </a>

Project 2013 SDK の主要な目的は、アプリの作成、Project Server Interface (PSI) サービス、および Project Professional 2013 の作業ウィンドウ アプリに関する CSOM と関連機能のプログラミングの概要とドキュメントを提供することです。 Project 2013 SDK には、Project Server 2013 と Project クライアント (Project Standard 2013、Project Professional 2013、Project Web App) のカスタマイズに関する主要な分野についてのステップ別の例が含まれています。 このドキュメントは未完成で、今後のリリースでさらにコンテンツが追加される予定です。 
  
Project Server 2013 におけるネットワーク通信の基礎となるテクノロジは Windows Communication Foundation (WCF) です。これには、Project Server CSOM を使用するクラウド シナリオや PSI を使用したオンプレミスの開発が含まれます。 従来の ASMX Web サービス参照も WCF アーキテクチャに基づいています。 Project Server 2013 で PSI Web サービス (ASMX ファイル) に対する参照を設定するには、パスに `?wsdl` URL オプションを追加する必要があります。 例: `https://ServerName/ProjectServerName/_vti_bin/PSI/Resource.asmx?wsdl`。
  
> [!NOTE]
> 対応しているのはよく使用される Project Server 機能に限られていますが、オンプレミスとクラウドの両方に適用可能な CSOM を使用することをお勧めします。 PSI の ASMX インターフェイスは Project Server 2013 で引き続き使用できますが、非推奨になっています。 PSI にフル アクセスすることが必要なオンプレミスのアプリケーションの場合、PSI に ASMX インターフェイスではなく WSF インターフェイスを使用する必要があります。 
  
Windows 7 コンピューターでの開発は、Project Server 2013 と SharePoint Server 2013 用の CSOM アセンブリを対象の開発コンピューターにコピーすることによってサポートされます。 SDK ダウンロードには、Project Server 用の CSOM アセンブリと再頒布ライセンスが含まれています。 SharePoint CSOM アセンブリを取得する方法については、「[SharePoint Server 2013 クライアント コンポーネント SDK](https://www.microsoft.com/en-us/download/details.aspx?id=35585)」をご覧ください。
  
WCF サービスを使用する開発の場合は、PSI プロキシ アセンブリに対する参照を設定するか、または PSI プロキシ ファイルをソリューションに追加することができます。同じドメイン内のリモート コンピューターからフロントエンド Project Server ASMX Web サービスへの直接参照を設定したり、プロキシ アセンブリまたはプロキシ ファイルを使用できます。SDK のダウンロードには、WCF サービスおよび ASMX Web サービスのプロキシ ファイルに加えて、プロキシ アセンブリの構築および更新されたプロキシ ファイルの生成のためのスクリプトが含まれます。
  
Project Server 2013 では、Microsoft SharePoint Designer 2013 を使用して、オンプレミスとオンラインの両方で使用できる宣言型 Project Server ワークフローを作成できます。 SharePoint Designer 2013 は、CSOM のワークフロー アクティビティのプロパティとメソッドを使用します。 Project Server Web パーツや、Project Web App のカスタマイズが含まれる Visual Studio 2012 ソリューションの開発と展開は、Project Server コンピューターでのみサポートされています。
  
Project Server 2013 における新しいプログラミング機能と廃止された機能の概要については、「[Project 2013 における開発者向けの更新内容](updates-for-developers-in-project-2013.md)」をご覧ください。 Project Server 2013 でのもう 1 つの大きな変更点は、WF4 ベースのワークフローを使用した、エンタープライズ プロジェクト テンプレートに基づくプロジェクト提案の作成と承認の管理です。 
  
以下の新しいトピックがあります。
  
- 「[SharePoint をホストとする Project Server アドインを作成する](create-a-sharepoint-hosted-project-server-add-in.md)」には、Project Server 2013 と Project Online で使用できるアプリのリモート開発に Visual Studio を使用する方法が示されています。 
    
- 「[Project Server 2013 のアーキテクチャ](project-server-2013-architecture.md)」では、Project Server プラットフォームの主要な新機能が取り上げられています。 
    
- 「[Project Server 2013 JavaScript オブジェクト モデルの作業の開始](getting-started-with-the-project-server-2013-javascript-object-model.md)」では、Project Server にアクセスできる Web アプリケーションの開発方法を説明しています。 
    
- 「[Project Server CSOM と .NET の使用を開始する](getting-started-with-the-project-server-csom-and-net.md)」では、PSI サービスを使用するのではなく、クライアント側オブジェクト モデルを使用してアプリケーションを開発する方法を説明しています。 
    
- 「[Project Professional の作業ウィンドウ アプリ](task-pane-add-ins-for-project.md)」では、Project 2013 に適用できる Office アドインが紹介されています。 Office 2013 SDK には、Project と他の Office 2013 クライアント向けの作業ウィンドウ アプリを開発する方法を示す記事が含まれています。 
    
- 「[需要管理用の Project Server ワークフローの作成](create-a-project-server-workflow-for-demand-management.md)」には、SharePoint Designer 2013 を使用して Project Server ワークフローを作成する方法が示されています。 
    
- 「[ProjectData - Project OData サービス リファレンス](https://msdn.microsoft.com/library/office/jj163015.aspx)」には、Project Server レポート用の OData インターフェイスの概要、および **ProjectData** サービス用の XML に関するリファレンス トピックが含まれています。 
    
**Microsoft.ProjectServer.Client** 名前空間と PSI サービスの新しいメソッドに関するトピックには最小限のドキュメントのみが含まれています。 PSI サービスに関する参照トピックのほとんどは、2011 年 7 月リリースの Project 2010 SDK から変更がありません。 
  
### <a name="future-sdk-releases"></a>将来の SDK リリース
<a name="pj15_Welcome_FutureReleases"> </a>

Project 2013 SDK は、一般利用可能リリース向けに、新しい記事およびリファレンス コンテンツとともに更新される予定です。
  
## <a name="sections-in-the-project-sdk"></a>Project SDK のセクション
<a name="pj15_Welcome_SectionsInTheSDK"> </a>

Project 2013 SDK には最上位のセクションが 2 つあります。
  
- 「[Project の概念と方法に関する記事](project-conceptual-and-how-to-articles.md)」セクションには、主要機能の概要と、開発のステップごとの手順が書かれた記事が含まれています。 
    
- 「[Project Server 2013 クラス ライブラリと Web サービス リファレンス](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx)」セクションでは、パブリック アセンブリ、CSOM 用 Microsoft.ProjectServer.Client.dll アセンブリ、および PSI サービスのオブジェクト モデルが説明されています。 
    
「**概念と方法の記事**」セクションの内容は、以下のとおりです。 
  
- 「[開発者向けの新着情報](updates-for-developers-in-project-2013.md)」では、Project 2013 の主な新しいプログラム機能と非推奨となった機能が説明されています。 
    
- 「[開発者向けの Project 概要](https://msdn.microsoft.com/library/8da91ab0-af4f-429f-8241-490600e3f7bd%28Office.15%29.aspx)」には、Project Server のアーキテクチャに関する記事、CSOM での開発を始める方法を説明する記事、Project の VBA の新機能についての情報、および Project Professional 2013 用の作業ウィンドウ アプリの開発に関するトピックが含まれる Office 2013 SDK への参照が含まれます。 
    
- [Project のプログラミング タスク](project-programming-tasks.md)」には、Project Server 向けアプリの作成方法、CSOM での JavaScript の使用方法、および需要管理のためのプロジェクトの提案とワークフローの作成方法についての記事が含まれます。 
    
- 「[Project 2013 プログラミング リファレンス](project-2013-programming-references.md)」には、Project Server 2013 用の PSI リファレンス、Project Server のエラー コードについての情報、および **ProjectData** サービス用の OData スキーマ リファレンスの概要が含まれます。 
    
> [!NOTE]
>  Project Server 2013 と統合するパブリック Office ストアからの EPM ソリューションとアプリを開発して展開するための要件を以下に示します。>  開発コンピューターと展開コンピューター上に .NET Framework 4 と .NET Framework 4.5 のどちらかをインストールする必要があります。 正しいリリースがインストールされているか判別するには、Windows のコントール パネルで **[プログラムと機能]** を開きます。 >  Visual Studio 2012 では NET Framework 4.5 をインストールして使用する必要があります。 Visual Studio プロジェクトを作成するときに、**[新しいプロジェクト]** ダイアログ ボックスのドロップダウン リストで **[.NET Framework 4.0]** または **[NET Framework 4.5]** を選択できます。 また、プロジェクトの **[プロパティ]** ウィンドウの **[アプリケーション]** タブで **[ターゲット フレームワーク]** を選択することもできます。 >  CSOM または PSI を使用するアプリケーション、および Project 作業ウィンドウ アプリに Visual Studio 2010 を使用できます。 ただし、Visual Studio 2010 には Office アドイン テンプレート、Office 開発ツール、Office 2013 用の SharePoint 開発ツールは含まれていません。 Visual Studio 2012 と、Office と SharePoint の開発ツールが含まれる Web Platform Installer (WebPI) をダウンロードする方法については、「[Office および SharePoint 用アプリのダウンロード](https://msdn.microsoft.com/office/apps/fp123627)」をご覧ください。 >  テスト環境でカスタム ソリューションを開発することをお勧めします。 Project Server 2013 と Project 2013 の現在のビルド用ソリューションを開発する場合、更新されたリファレンスで再コンパイルする必要があります。新しいリリースで動作させるには追加の変更が必要になることがあります。 プレリリース バージョン用に開発されたソリューションはリリース バージョンでは動作しない可能性があります。 
  
## <a name="see-also"></a>関連項目
<a name="pj15_Welcome_AR"> </a>

- [Project 2013 における開発者向けの更新内容](updates-for-developers-in-project-2013.md)
    
- [Project Server 2013 のアーキテクチャ](project-server-2013-architecture.md)
    
- [Project 2013 SDK のダウンロード](https://www.microsoft.com/en-us/download/details.aspx?id=30435%20)
    
- [SharePoint Server 2013 クライアント コンポーネント SDK](https://www.microsoft.com/en-us/download/details.aspx?id=35585)
    
- [開発者向け Project](https://msdn.microsoft.com/project)
    
- [Office 開発者向けドキュメント](https://msdn.microsoft.com/office)
    
- [Project 2010 の開発を開始する](https://msdn.microsoft.com/library/gg607685.aspx)
    
- [ドキュメントの表記規則](https://msdn.microsoft.com/library/6b38829f-1a9d-4fb6-ad3b-01182628080a.aspx)
    
- [SharePoint 2013 のアクセシビリティ](https://msdn.microsoft.com/library/jj841103.aspx)
    
- [Microsoft Office 365 のアクセシビリティ](https://www.microsoft.com/enable/products/office365/)
    
- [Microsoft のプライバシーに関する声明](https://privacy.microsoft.com/ja-JP/privacystatement)
    

