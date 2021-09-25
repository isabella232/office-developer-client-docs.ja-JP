---
title: CSOM のすること、しないこと
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 6828485c-040b-4278-923f-4cc7c8fe0fb1
description: クライアント側オブジェクト モデル (CSOM) は、Project Server 2013 用 API のセットです。これらは PC、モバイル デバイス、タブレット向けに開発可能なアプリケーションにおいて、オンラインと社内設置型の両方で使用するように設計されています。 この記事では、CSOM を使用する際のいつくかの一般的なシナリオと、CSOM の制限について説明します。
ms.localizationpriority: high
ms.openlocfilehash: b145e392eb66a38bd79a9a0aaa659ad8b2017835
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586713"
---
# <a name="what-the-csom-does-and-does-not-do"></a>CSOM のすること、しないこと

クライアント側オブジェクト モデル (CSOM) は、Project Server 2013 用 API のセットです。これらは PC、モバイル デバイス、タブレット向けに開発可能なアプリケーションにおいて、オンラインと社内設置型の両方で使用するように設計されています。 この記事では、CSOM を使用する際のいつくかの一般的なシナリオと、CSOM の制限について説明します。
  
|||
|:-----|:-----|
|||
   
CSOM を使用すると、Project Server 2013 用アプリの開発と Project Server と他のアプリケーションとの統合が可能になります。 PC、Windows Phone 7.5 などのモバイル デバイス、Windows 8 デバイスなどのタブレット、iOS デバイスや Android デバイスで実行するアプリを開発することができます。 CSOM は、Project Server で最もよく使用される 12 の PSI サービスの機能をカバーする API を提供します。 CSOM API は、ASMX ベースと WCF ベースの PSI サービスとは異なる方法で編成され、より使いやすくなっています。 CSOM は ADO.NET データセットを使用しないため、OData プロトコルを介してアクセスできます。 .NET Framework 4 ライブラリ、JavaScript、REST (Representational State Transfer) クエリを使用して、CSOM での開発が可能です。
  
CSOM の概要および JavaScript と .NET Framework 4 と合わせて CSOM を使用する方法について説明した記事については、「[Project Server のクライアント側オブジェクト モデル (CSOM)](client-side-object-model-csom-for-project-2013.md)」を参照してください。 CSOM のアセンブリ、クラス、メンバーの詳細については [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) 名前空間の参照をご覧ください。 
  
## <a name="usage-scenarios-for-the-csom"></a>CSOM の使用シナリオ
<a name="pj15_WhatTheCSOM_UsageScenarios"> </a>

以下に、CSOM でサポートされているアプリケーションの例をいくつか示します。CSOM は多くのシナリオで PSI の代わりに使用できます。
  
- **Project Server を拡張するアプリケーションの開発** CSOM の主な目的は Project Server 2013 用アプリケーションの開発であり、PC、モバイル デバイス、タブレットなどの多彩なデバイス向けのアプリケーションを作成できます。 アプリは、プライベートなアプリ カタログまたは一般公開されている Office ストアで配布できます。 
    
- **Project Server でのエンティティの作成または管理の自動化** CSOM ではプロジェクト、タスク、割り当て、エンタープライズ リソース、カスタム フィールド、参照テーブル、タイムシート、イベント ハンドラー、ワークフロー フェーズ、ワークフロー ステージなどのエンティティに対して CRUD 操作を実行できます。多くの場合、一括ジョブや反復ジョブにより、カスタム アプリケーションの時間を短縮できます。 
    
- **Project データベースの発行済みテーブル内のデータの取得** 下書き、発行済み、およびアーカイブのテーブルへの直接データベース アクセスはサポートされていないため、CSOM を使用して、レポート テーブルやビューで使用できないデータを読み取ることができます。たとえば、ワークフロー ステージ、ワークフロー フェーズ、アクティビティの情報を取得します。レポート テーブルのデータの読み取りには OData クエリを使用できます。 
    
- **状態およびタイムシート データの検証** ローカル イベント ハンドラーやプレイベントのリモート イベント レシーバーで CSOM を使用して、Project Web App にデータを保存する前に、ユーザーが入力する割り当ての状態やタイムシート データを検証します。 
    
- **財務プロジェクトの作成** 財務システムとの統合のためのタイムシートを通じて、タイム キャプチャ用のプロジェクトを作成します。財務システムの原価構成を反映する財務コードの階層を作成します。財務プロジェクトは、スケジューリングまたは状態の更新を必要としません。 
    
- **会計システムとの統合** 財務システムおよび請求システムに提供するために、または予算比較の目的で、プロジェクトに関連するリソースのコストおよび経費をキャプチャします。タスク、リソース、および割り当てをシステム間で同期させます。あるシステムでタイムシート データをキャプチャし、他のシステムに提供します (どのタイムシートを使用するかは、組織または個々のプロジェクトのニーズによって決まります)。 
    
- **チーム メンバーからの更新の自動化** 現在管理されていないプロジェクトについては、プロジェクト チームのメンバーからの進捗およびその他の変更により、サーバー上でプロジェクトを自動的に更新します。プロジェクトは、プロジェクト マネージャーが結果を確認したり、計画を調整したりすることなく、更新および再発行することができます。 
    
    > [!NOTE]
    > CSOM は、状態の更新の送信をサポートしていますが、現在、状態の承認はサポートしていません。 
  
- **リモート イベント レシーバーでの Project Server データの評価** **ProjectCreating** プレイベントのリモート イベント レシーバーは、CSOM からの Project Server データを使用して、イベントを取り消すかどうかの決定に役立てることができます。たとえば、プロジェクトを作成する前に、プロジェクト提案を既存のプロジェクトと比較します。 
    
- **宣言による Project Server ワークフローのサポート** CSOM により SharePoint Designer 2013 で作成した Project Server のワークフローが使用できるようになります。 CSOM は、Windows Workflow Foundation バージョン 4 (WF4) を使用したワークフロー定義をサポートしています。 (PSI は、WF4 ワークフローをサポートしていません。) 
    
- **複雑な Project Server ワークフローの作成** Visual Studio 2012 でワークフローを開発する場合は、ワークフロー ステージ内の複雑なアクションで CSOM を使用したり、カスタム ワークフロー アクションを作成したりすることができます。 
    
## <a name="what-the-csom-does-not-do"></a>CSOM でしないこと
<a name="pj15_WhatTheCSOM_DoesNotDo"> </a>

CSOM は PSI に完全に代わるものではありません。 CSOM は内部で PSI サービスを使用するので、CSOM は PSI と同じ機能制限が多数あります。 ローカル プロジェクト (.mpp ファイル) のデータへのアクセスできないなどの PSI の制限事項に加え、CSOM には Project Web App が通常処理する管理機能は含まれません。 たとえば、Project Web App のカスタム セキュリティ グループの作成はサイトの設定 (Project Web App のアクセス許可のページ) で処理できます。 
  
PSI でも CSOM でも処理されない操作のリストについては、「[PSI のすること、しないこと](what-the-psi-does-and-does-not-do.md)」の「*PSI がしないこと*」セクションを参照してください。
  
### <a name="psi-services-that-the-csom-does-not-cover"></a>CSOM がカバーしない PSI サービス
<a name="pj15_WhatTheCSOM_PSIServices"> </a>

CSOM には、次の PSI サービスの機能は含まれません。
  
- **管理サービス** 会計期間の作成やタイムシートの設定など、Project Server および関連するプロジェクト サイトの管理設定や操作を管理するには、[WebSvcAdmin.Admin](https://msdn.microsoft.com/library/WebSvcAdmin.Admin.aspx) クラスの PSI メソッドを使用します。 Project Web App でも、[サーバー設定] ページ (https://  *ServerName*  /  *ProjectServerName*  /_layouts/15/pwa/Admin/Admin.aspx) にリンクされているページの多くで、**管理** メソッドを使用します。 
    
- **アーカイブ サービス** アーカイブ テーブル内のプロジェクト、リソース、カスタム フィールドなどのエンティティを保存および管理するには、[Archive](https://msdn.microsoft.com/library/WebSvcArchive.Archive.aspx) クラスの PSI メソッドを使用します。 
    
- **CubeAdmin サービス** 社内インストールの OLAP キューブを作成および管理するには、[WebSvcCubeAdmin.CubeAdmin](https://msdn.microsoft.com/library/WebSvcCubeAdmin.CubeAdmin.aspx) クラスの PSI メソッドを使用するか、Project Web App の [OLAP データベースの管理] ページ (https://  *ServerName*  /  *ProjectServerName*  /_layouts/15/pwa/CubeAdmin/CubeAnalysisAdmin.aspx) を使用します。 
    
    > [!NOTE]
    > Project Online では OLAP キューブはサポートされていません。 
  
- **ドライバー サービス** プロジェクト ポートフォリオ分析用のビジネス ドライバーを作成および管理するには、[WebSvcDriver.Driver](https://msdn.microsoft.com/library/WebSvcDriver.Driver.aspx) クラスの PSI メソッドを使用します。 
    
- **LoginForms サービスと LoginWindows サービス** CSOM での認証は、OAuth または Windows 認証を使用して、**ProjectContext** オブジェクトの初期化中に行われます。 ローカルの完全信頼アプリケーションがフォーム認証と Windows 認証の両方を使用できる、複数認証のアプリケーションを作成するには、[WebSvcLoginForms.LoginForms](https://msdn.microsoft.com/library/WebSvcLoginForms.LoginForms.aspx) クラスと [WebSvcLoginWindows.LoginWindows](https://msdn.microsoft.com/library/WebSvcLoginWindows.LoginWindows.aspx) クラスの PSI メソッドを使用します。 
    
- **通知サービス** 警告とアラームを作成および管理するには、[WebSvcNotifications.Notifications](https://msdn.microsoft.com/library/WebSvcNotifications.Notifications.aspx) クラスの PSI メソッドを使用します。 
    
- **ObjectLinkProvider サービス** ドキュメントおよび SharePoint リスト アイテムへの Web オブジェクトとリンクを作成および管理するには、[WebSvcObjectLinkProvider.ObjectLinkProvider](https://msdn.microsoft.com/library/WebSvcObjectLinkProvider.ObjectLinkProvider.aspx) クラスの PSI メソッドを使用します。 
    
- **PortfolioAnalyses サービス** プランナー ソリューションやオプティマイザー ソリューションを含む、プロジェクト ポートフォリオ分析を作成および管理するには、[WebSvcPortfolioAnalyses.PortfolioAnalyses](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.aspx) クラスの PSI メソッドを使用します。 
    
- **QueueSystem サービス** CSOM では、Project Server キューの基本的な情報を入手することができ、[ProjectContext.WaitForQueue](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.WaitForQueue.aspx) メソッドも含まれています。 Project Server のキュー システムをより詳細に管理するには、[WebSvcQueueSystem.QueueSystem](https://msdn.microsoft.com/library/WebSvcQueueSystem.QueueSystem.aspx) クラスの PSI メソッドを使用します。 
    
- **セキュリティ サービス** Project Server のセキュリティ グループ、テンプレート、カテゴリを作成および管理し、現在のユーザーのアクセス許可を検査するには、[WebSvcSecurity.Security](https://msdn.microsoft.com/library/WebSvcSecurity.Security.aspx) クラスの PSI メソッドを使用します。 
    
- **WssInterop サービス** プロジェクト サイトの情報を取得し、管理するには、[WebSvcWssInterop.WssInterop](https://msdn.microsoft.com/library/WebSvcWssInterop.WssInterop.aspx) クラスの PSI メソッドを使用します。 
    
    > [!NOTE]
    > SharePoint Server 2013 で、CSOM を使用することができます。 プロジェクト サイトは、SharePoint サイトです。 
  
CSOM では、PSI で使用できる拡張機能などは使用できません。たとえば、ローカルで使用する PSI 拡張機能を作成した場合、CSOM を変更して PSI 拡張機能を使用することはできません。拡張機能のシナリオは、次のような方法で実装できます。
  
- ローカル コンポーネントまたは Microsoft Azure で実行するコンポーネント内で CSOM 呼び出しを集約します。
    
- Project Server データベースでレポート テーブルに直接アクセスする代わりに、レポート データの OData クエリを使用します。
    
- CSOM 呼び出しを Project Online の OAuth 認証を通じてサードパーティ アプリケーションと統合するか、社内使用のサーバー側コンポーネントと統合します。
    
- CSOM を使用するアプリケーションでは、社内設置型または SQL Azure を使用するカスタム データベースも使用できます。
    
### <a name="request-limits-of-the-csom"></a>CSOM の要求制限
<a name="pj15_WhatTheCSOM_RequestLimits"> </a>

Project Server 2013 の CSOM は、SharePoint Server 2013 の CSOM 実装に基づいて構築されており、要求の最大サイズの制限を継承しています。 SharePoint には、操作要求に 2 MB の制限、送信されるバイナリ オブジェクトのサイズに 50 MB の制限があります。 要求サイズが制限されているのは、操作のキューが極端に長くなることや、大きなバイナリ オブジェクトの処理で遅延が発生するのを防ぐためです。
  
たとえば、CSOM を使用してプロジェクトを作成してから、短い名前、タスク GUID、有効期間 1d などの最小限の情報で 252 個のタスクを追加した場合、**DraftProject.Update** 要求の合計のデータ量は 2 MB 未満になります。しかし、このようなタスクを空のプロジェクトに 253 個追加しようとすると、2 MB の制限を超過し、[**Microsoft.SharePoint.Client.ServerException: 要求で使用されているリソースが多すぎます**] という例外が発生します。
  
HTTP または HTTPS で CSOM 要求内のデータを取得するには、[Fiddler](https://www.fiddler2.com) (https://www.fiddler2.com)) などの Web デバッグ ツールを使用することができます。 要求サイズのテストを実装し、大きな要求を小さいグループに分割するソリューションを含むコード例については、[DraftProject.Update](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.DraftProject.Update.aspx) を参照してください。 
  
## <a name="see-also"></a>関連項目
<a name="pj15_WhatTheCSOM_AR"> </a>

- [Project Server のクライアント側オブジェクト モデル (CSOM)](client-side-object-model-csom-for-project-2013.md)
    
- [PSI のすること、しないこと](what-the-psi-does-and-does-not-do.md)
    
- [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx)
    

