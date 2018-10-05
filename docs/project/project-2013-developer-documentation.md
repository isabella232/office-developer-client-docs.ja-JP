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
- sdk をプロジェクト 2013 では、Project 2013 では、SDK の概要
localization_priority: Normal
ms.assetid: f66adbf1-5cb5-4dd0-be08-45e1c88c010c
description: ドキュメント、コード サンプル、how-to 記事、および Office ストアまたはプライベート アプリ カタログ用のアプリケーションの構築を支援し、カスタマイズして、Project Server とクライアント プロジェクトとその他のデスクトップおよびビジネスのさまざまな統合のプログラミング リファレンスを検索します。エンタープライズ プロジェクト管理用のアプリケーションです。
ms.openlocfilehash: 887b5964d6fa0e4845156e13c7f49a399543c133
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398228"
---
# <a name="project-2013-developer-documentation"></a>Project 2013 開発者向けドキュメント

ドキュメント、コード サンプル、how-to 記事、および Office ストアまたはプライベート アプリ カタログ用のアプリケーションの構築を支援し、カスタマイズして、Project Server とクライアント プロジェクトとその他のデスクトップおよびビジネスのさまざまな統合のプログラミング リファレンスを検索します。エンタープライズ プロジェクト管理用のアプリケーションです。
  
Microsoft Project 2013 ソフトウェア開発キット (SDK) を開始します。 ドキュメント、コード サンプル、how-to 記事、SDK が含まれていて、パブリック ストアまたはプライベート アプリ カタログ用のアプリケーションの構築を支援し、カスタマイズし、統合のプログラミング リファレンス サーバーおよびその他のデスクトップのさまざまなプロジェクト、クライアントのプロジェクトとエンタープライズ プロジェクト管理のビジネス ・ アプリケーションです。
  
> [!NOTE]
> Project Server 2013 は、プラットフォーム上に構築、SharePoint Server 2013、および Project 2013 には、他の Office 2013 アプリケーションとインフラストラクチャの大部分が含まれています。 モデルのドキュメントを SharePoint のアドイン、SharePoint ベースのワークフローでは、Web パーツ、その他の SharePoint の機能、および Office アドインのドキュメントを使用して開発には、 [SharePoint アドイン](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins) [Office アドイン](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins)が参照してください。 
  
## <a name="introduction-to-the-project-sdk"></a>Project SDK の概要
<a name="pj15_Welcome_IntroToSDK"> </a>

Project Server 2013 は、設置型またはクラウド ベースのエンタープライズ プロジェクト管理ソリューションを構築するため、エンド ・ ユーザーが発見し、パブリック ストアまたはプライベート アプリ カタログから取得できるアプリケーションを構築するためのプラットフォームです。 Project Server 2013 のアーキテクチャは、多くの追加および改良されたのでは、Microsoft Office Project Server 2007 では、導入されたプラットフォームに基づいています。 新しい機能には、クライアント側オブジェクト モデル (CSOM) がプロジェクト オンライン、Project Server のデータ、リモート イベント レシーバー、ワークフロー アーキテクチャ Windows ワークフローのバージョン 4 を基にレポートを作成するオンライン ・ アクセスの OData サービスへのアクセスを有効にするのにが含まれます。基盤 (WF4)、および Office のアドイン、Microsoft Office 2013 のクライアント アプリケーションでの作業ウィンドウの拡張機能の一般的なアーキテクチャであります。
  
Project Server 2013 の主な変更は、Project Server 2010 の下書き、発行済み、アーカイブ、およびレポート データベースの代わりに 1 つのデータベースの使用です。 新機能および機能に関する詳細については、 [Project 2013 の開発者用の更新プログラム](updates-for-developers-in-project-2013.md)を参照してください。 Project Server プラットフォームの変更方法については、 [Project Server 2013 のアーキテクチャ](project-server-2013-architecture.md)を参照してください。 Project Server 2010 に存在して、Project Server 2013 は、に基づいて、開発プラットフォームの概要については、MSDN で[Project 2010 の開発を開始する](https://msdn.microsoft.com/library/gg607685.aspx)を参照してください。 
  
Project Server 2013 は、Microsoft.NET Framework 4 および Microsoft SharePoint Server 2013 で作成されます。 記事やこの SDK のサンプルは、カスタム ソリューションとアプリを開発するため基礎を提供します。Project Server または Project Professional のすべてのプログラミング機能は対応していません。 [プロジェクト デベロッパー センター](https://msdn.microsoft.com/library/4e5245c3-4891-455b-b321-1819cdd77247.aspx)には、プロジェクトの記事、ブログ、ビデオ、web キャスト、visual how-to 記事、およびその他のリソースへのリンクが含まれています。 
  
Project 2013 SDK には、Project Server 2013、Project Web App、評価のためのプロジェクト、およびプロジェクトの標準的な 2013 の開発者向けの情報が含まれています。 SDK の記事は、開発者および管理者の機能拡張、カスタム ソリューションの計画のプロジェクトと Project Server を評価するように設計されています。
  
### <a name="feedback"></a>フィードバック
<a name="pj15_Welcome_Feedback"> </a>

伺いたいと思います。 オンラインの MSDN のトピックでのコード サンプルでは、コメントを追加したり、各ページの下部にある**コミュニティ コンテンツ**セクションのバグと、コンテンツにフラグを設定できます。 Project 2013 SDK ダウンロードをインストールすると、ローカル ドキュメント記事は、タイトルの下にある*フィードバックの送信*リンクを持ちます。 SDK を参照することで任意の時点では、SDK チームに電子メールを送信するリンクを選択します。 送信、修正、明確化の要求やコード サンプルでは、またはその他のコメントより強力なコンテンツにしてできます。 
  
### <a name="download"></a>Download
<a name="pj15_Welcome_Download"> </a>

Project 2013 SDK のダウンロードは、 [Microsoft ダウンロード センター](https://www.microsoft.com/en-us/download/details.aspx?id=30435%20)で利用可能な ( `https://www.microsoft.com/en-us/download/details.aspx?id=30435%20`)。 ダウンロードには、Project2013SDK.HxS (この資料に含まれるファイル) が含まれているサンプル コード、再頒布可能なアセンブリ、およびその他のリソースに関連します。 Project 2013 SDK には、レポートのデータ テーブルの参照がまだ含まれません。
  
### <a name="whats-new-in-the-project-sdk"></a>Project SDK の新機能
<a name="pj15_Welcome_WhatsNew"> </a>

Project 2013 SDK の主な目的は、プロジェクトの評価のためのアプリケーション、プロジェクト Server インターフェイス (PSI) サービス、および作業ウィンドウのアプリケーションを作成するためのプログラミングの概要について説明し、CSOM および関連機能のマニュアルを提供します。 Project 2013 SDK には、Project Server 2013 と (プロジェクトの標準的な 2013、評価のためのプロジェクト、および Project Web App の) プロジェクトのクライアントのカスタマイズの主要な領域の例手順にはが含まれています。 ドキュメントが不完全です。以降のリリースより多くのコンテンツが追加されます。 
  
ネットワーク通信の基盤となるテクノロジーは、PSI を使用してオンプレミス開発プロジェクト サーバー CSOM を使用するクラウドのシナリオを含む、Project Server 2013 のように、Windows Communication Foundation (WCF) です。 従来の ASMX web サービス参照は、WCF アーキテクチャに基づきます。 Project Server 2013 の PSI web サービス (ASMX ファイル) への参照を設定する場合は、追加する必要があります、`?wsdl`のパスを [URL] です。 例: `https://ServerName/ProjectServerName/_vti_bin/PSI/Resource.asmx?wsdl`。
  
> [!NOTE]
> Project Server の機能を頻繁に使用されるのみに対応して、お勧めを使用すること、CSOM 可能なアプリケーションの両方に設置型とクラウドで。 Project Server 2013 では使用可能であるが、PSI の ASMX インターフェイスは使用されなくなりました。 PSI へのフル アクセスを必要とする設置型のアプリケーションでは、ASMX インターフェイスではなく、PSI の WCF インターフェイスを使用してください。 
  
Windows 7 コンピューター上の開発は、CSOM アセンブリを開発用コンピューターに Project Server 2013 と SharePoint Server 2013 のコピーでサポートされます。 SDK ダウンロードには、Project Server との再配布ライセンスの CSOM のアセンブリが含まれています。 SharePoint CSOM にアセンブリを得るには、 [SharePoint Server 2013 クライアント コンポーネント SDK](https://www.microsoft.com/en-us/download/details.aspx?id=35585)を参照してください。
  
WCF サービスを使用する開発の場合は、PSI プロキシ アセンブリに対する参照を設定するか、または PSI プロキシ ファイルをソリューションに追加することができます。同じドメイン内のリモート コンピューターからフロントエンド Project Server ASMX Web サービスへの直接参照を設定したり、プロキシ アセンブリまたはプロキシ ファイルを使用できます。SDK のダウンロードには、WCF サービスおよび ASMX Web サービスのプロキシ ファイルに加えて、プロキシ アセンブリの構築および更新されたプロキシ ファイルの生成のためのスクリプトが含まれます。
  
Project Server 2013 では、設置型の両方の Microsoft SharePoint Designer 2013 を使用して Project Server の宣言型ワークフローを作成し、オンラインを使用できます。 SharePoint Designer 2013 は、CSOM でのワークフロー アクティビティのプロパティとメソッドを使用します。 開発およびプロジェクト サーバーの Web パーツを含む Visual Studio 2012 のソリューションの配置、または Project Web App では、カスタマイズは、Project Server コンピューター上でのみサポートされています。
  
新しいプログラミング機能と Project Server 2013 で廃止された機能の概要については、 [Project 2013 の開発者用の更新プログラム](updates-for-developers-in-project-2013.md)を参照してください。 Project Server 2013 のもう 1 つの主要な変更は、WF4 ベースのワークフローの作成を管理するために使用して、エンタープライズ プロジェクト テンプレートに基づいてプロジェクト提案の承認です。 
  
以下の新しいトピックがあります。
  
- [プロジェクト SharePoint でホストされているサーバーを作成するアドイン](create-a-sharepoint-hosted-project-server-add-in.md)には、Project Server 2013 とオンライン プロジェクトで使用できるアプリケーションのリモートの開発に Visual Studio を使用する方法を示します。 
    
- 「[Project Server 2013 architecture](project-server-2013-architecture.md)」では、Project Server プラットフォームの主要な新機能について説明します。 
    
- [Project Server 2013 の JavaScript オブジェクト モデルを使うにあたって](getting-started-with-the-project-server-2013-javascript-object-model.md)は、Project Server にアクセスできる web アプリケーションを開発する方法を示します。 
    
- [プロジェクト サーバー CSOM および .NET の概要](getting-started-with-the-project-server-csom-and-net.md)では、クライアント側オブジェクト モデルを使用して、PSI サービスを使用する代わりに、アプリケーションを開発する方法を示します。 
    
- [Project Professional のタスク] ウィンドウのアプリケーション](task-pane-add-ins-for-project.md)は、Project 2013 に適用されると、Office アドインを紹介します。 Office 2013 SDK には、プロジェクトとその他の Office 2013 クライアントの作業ウィンドウのアプリケーションを開発する方法を説明する記事が含まれています。 
    
- [需要管理のために Project Server ワークフローの作成](create-a-project-server-workflow-for-demand-management.md)では、SharePoint Designer 2013 を使用して、Project Server のワークフローを作成する方法を示しています。 
    
- [ProjectData - プロジェクトの OData サービスの参照](https://msdn.microsoft.com/library/office/jj163015.aspx)には、Project Server のレポート、OData インターフェイスと**ProjectData**サービスの XML のリファレンス トピックの概要が含まれています。 
    
**Microsoft.ProjectServer.Client**名前空間のトピックおよび PSI サービスに新しいメソッドは、最小限のドキュメントのみにあります。 PSI サービスのリファレンス トピックのほとんどは、プロジェクト 2010 SDK の 2011 年 7 月のリリースから変更はありません。 
  
### <a name="future-sdk-releases"></a>将来の SDK リリース
<a name="pj15_Welcome_FutureReleases"> </a>

Project 2013 SDK は、新しい記事と一般の可用性リリースのコンテンツを参照は更新されます。
  
## <a name="sections-in-the-project-sdk"></a>Project SDK のセクション
<a name="pj15_Welcome_SectionsInTheSDK"> </a>

Project 2013 SDK には、最上位レベルの 2 つのセクションがあります。
  
- [プロジェクトの概念と操作方法の記事](project-conceptual-and-how-to-articles.md)のセクションには、主な機能と開発の詳細な手順が含まれる記事の概要が含まれています。 
    
- [Project Server 2013 のクラス ライブラリと web サービス参照](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx)のセクションでは、CSOM および PSI サービスのパブリック アセンブリ、Microsoft.ProjectServer.Client.dll アセンブリのオブジェクト モデルを説明します。 
    
「**概念と方法の記事**」セクションの内容は、以下のとおりです。 
  
- [新アウトは、どのような開発者向け](updates-for-developers-in-project-2013.md)新しいプログラミングの主な機能の説明および Project 2013 の機能は使用されなくなりました。 
    
- [開発者向けのプロジェクトの概要](https://msdn.microsoft.com/library/8da91ab0-af4f-429f-8241-490600e3f7bd%28Office.15%29.aspx)には、Project Server のアーキテクチャに関する記事、CSOM、vba プロジェクトの新機能に関する情報が含まれている Office 2013 の SDK への参照と開発を開始する方法を説明する記事が含まれています。評価のためのプロジェクトの作業ウィンドウのアプリの開発に関するトピックを示します。 
    
- [プロジェクト プログラミング タスクには](project-programming-tasks.md)には、需要管理の CSOM、および作成するプロジェクトの提案とワークフローの JavaScript を使用して、プロジェクトのサーバー アプリケーションを作成する方法に関する「方法」記事が含まれていますいます。 
    
- [Project 2013 の参照をプログラミングする](project-2013-programming-references.md)には、Project Server 2013、Project Server のエラー コードに関する情報、および**ProjectData**サービスの OData スキーマの参照の PSI リファレンスの概要が含まれています。 
    
> [!NOTE]
>  開発し、EPM ソリューションと Project Server 2013 に統合された Office のパブリック ストアからアプリケーションを配置するための要件を次に示します: > 開発用コンピューター、および、展開、.NET Framework 4] または [.NET Framework 4.5 をインストールする必要がありますコンピューターです。 正しいリリースがインストールされているかどうかを確認するのには、Windows のコントロール パネルで**プログラムと機能**を開きます。 > Visual Studio 2012 では、インストールし、.NET Framework 4.5 を使用します。 Visual Studio プロジェクトを作成するときに **[新しいプロジェクト**] ダイアログ ボックスのドロップダウン ボックスの一覧で **.NET Framework 4.0**または**NET Framework 4.5**のいずれかを選択できます。 プロジェクトの [**プロパティ**] ウィンドウの **[アプリケーション**] タブで、**ターゲット フレームワーク**を選択することもできます。 > Visual Studio 2010 を使用して、CSOM または、PSI を使用するアプリケーションおよびプロジェクトの作業ウィンドウ アプリすることができます。 ただし、Visual Studio 2010 が含まれていない Office のアドイン テンプレート、Office 開発ツール、または Office 2013 用の SharePoint 開発ツールです。 Visual Studio 2012 とを Office および SharePoint 開発ツールが含まれています Web プラットフォーム インストーラー (WebPI) をダウンロードするには、 [Office および SharePoint 用アプリのダウンロード](https://msdn.microsoft.com/office/apps/fp123627)を参照してください。 > 私たちは、テスト環境でのカスタム ソリューションを開発することをお勧めします。 開発する場合は、Project Server 2013 および Project 2013 の現在のソリューションを構築、更新された参照は、再コンパイルする必要があり、以降のリリースで動作する、追加の変更が必要な場合があります。 プレリリース バージョン用に開発されたソリューションは、製品版では動作しません。 
  
## <a name="see-also"></a>関連項目
<a name="pj15_Welcome_AR"> </a>

- [Project 2013 の開発者向けの新機能](updates-for-developers-in-project-2013.md)
    
- [Project Server 2013 のアーキテクチャ](project-server-2013-architecture.md)
    
- [Project 2013 SDK のダウンロード](https://www.microsoft.com/en-us/download/details.aspx?id=30435%20)
    
- [SharePoint Server 2013 クライアント コンポーネント SDK](https://www.microsoft.com/en-us/download/details.aspx?id=35585)
    
- [開発者のためのプロジェクト](https://msdn.microsoft.com/project)
    
- [Office 開発者向けドキュメント](https://msdn.microsoft.com/office)
    
- [Project 2010 の開発を開始する](https://msdn.microsoft.com/library/gg607685.aspx)
    
- [ドキュメントの表記規則](https://msdn.microsoft.com/library/6b38829f-1a9d-4fb6-ad3b-01182628080a.aspx)
    
- [SharePoint 2013 におけるアクセシビリティ](https://msdn.microsoft.com/library/jj841103.aspx)
    
- [Microsoft Office 365 のユーザー補助機能](https://www.microsoft.com/enable/products/office365/)
    
- [Microsoft オンライン プライバシーに関する注意](https://privacy.microsoft.com/en-us/privacystatement)
    

