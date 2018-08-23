---
title: CSOM が行うこと、行わないこと
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6828485c-040b-4278-923f-4cc7c8fe0fb1
description: クライアント側オブジェクト モデル (CSOM) は、オンラインの両方に設計された Project Server 2013 の Api のセットと設置は Pc、モバイル デバイス、およびタブレットを開発できるアプリケーションで使用します。 この記事は、CSOM を使用するためのいくつかの一般的なシナリオが含まれていて、CSOM の制限事項の一覧も。
ms.openlocfilehash: 232152d3d2ee902b438bc1fe3ece06acca713175
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804693"
---
# <a name="what-the-csom-does-and-does-not-do"></a>CSOM のすること、しないこと

クライアント側オブジェクト モデル (CSOM) は、オンラインの両方に設計された Project Server 2013 の Api のセットと設置は Pc、モバイル デバイス、およびタブレットを開発できるアプリケーションで使用します。 この記事は、CSOM を使用するためのいくつかの一般的なシナリオが含まれていて、CSOM の制限事項の一覧も。
  
|||
|:-----|:-----|
|||
   
CSOM は、Project Server 2013 のアプリケーションの開発およびその他のアプリケーションと Project Server の統合を有効にします。 Pc、タブレットなど、Windows 8 のデバイスと iOS および Android デバイスなど、Windows Phone 7.5 では、モバイル デバイス上で実行するアプリケーションを開発できます。 CSOM は、Project Server の PSI サービスを使用して、12 個の機能を最もよく説明する Api を提供します。 CSOM Api は、異なる方法で編成され、ASMX と WCF ベースの PSI サービスよりも使いやすい。 CSOM は、ADO.NET のデータセットを使用しないとは、OData プロトコル経由でアクセスできます。 .NET Framework 4 のライブラリ、JavaScript を使用して、CSOM で開発することができますまたは主要な状態を転送 (REST) クエリ。
  
CSOM と JavaScript と.NET Framework 4 に、CSOM を使用する方法について説明した記事の概要については、 [Project Server のクライアント側オブジェクト モデル (CSOM)](client-side-object-model-csom-for-project-2013.md)を参照してください。 CSOM のアセンブリ、クラス、およびメンバーに関する詳細については、 [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx)名前空間の参照を参照してください。 
  
## <a name="usage-scenarios-for-the-csom"></a>CSOM を使用するシナリオ
<a name="pj15_WhatTheCSOM_UsageScenarios"> </a>

以下に、CSOM でサポートされているアプリケーションの例をいくつか示します。CSOM は多くのシナリオで PSI の代わりに使用できます。
  
- **開発アプリケーションのプロジェクトのサーバーを拡張します。** CSOM の主な目的は、Pc、モバイル デバイスは、タブレットなどのデバイスのさまざまなアプリケーションを作成する場所、Project Server 2013 のアプリケーションの開発です。 Office のパブリック ストアまたはプライベート アプリ カタログ内でアプリケーションを配布することができます。 
    
- **自動化、作成、または Project Server 内のエンティティの管理**CSOM には、プロジェクト、タスク、割り当て、エンタープライズ リソース、ユーザー設定フィールド、参照テーブル、タイムシート、イベント ハンドラーでは、ワークフローのフェーズおよびステージなどのエンティティに対して CRUD 操作を実行できます。 多くの場合は、カスタム アプリケーションは、一括または反復的なジョブの時間を節約できる場合があります。 
    
- **プロジェクト データベースのパブリッシュされたテーブル内のデータを取得します。** テーブルはサポートされていないため、データベースに直接、公開、下書きにアクセスし、アーカイブがレポートのテーブルまたはビューで使用できないデータを読み取るため、CSOM を使用することができます。 ワークフロー ステージ、フェーズ、および活動に関する情報を取得します。 レポート テーブル内のデータを読み取るには、OData クエリを使用できます。 
    
- **状態管理とタイムシートのデータを検証します。** ローカル イベント ハンドラーまたは前のイベントのリモート イベント レシーバーで CSOM を使用すると、Project Web App でデータが保存される前に、ユーザーが入力した割り当ての状態] または [タイムシート データを検証します。 
    
- **財務プロジェクトの作成**財務システムとの統合のためにタイムシートをタイム キャプチャ用のプロジェクトを作成します。 財務システムのコストの内訳構造を反映した、財務コードの階層を作成します。 財務プロジェクトでは、スケジュール設定やステータスの更新は必要ありません。 
    
- **会計システムとの統合**リソースのコストおよび関連する財務および請求システムをフィードするプロジェクトと予算の比較のための経費をキャプチャします。 タスク、リソース、およびシステム間での割り当てを同期します。 他のフィードを 1 つのシステムでタイムシート データをキャプチャ (組織または個々 のプロジェクトのニーズに依存するタイムシートが表示されます)。 
    
- **チーム メンバーから更新を自動化**積極的に管理されていないプロジェクトでは、進行状況とプロジェクト チームのメンバーからの他の変更をサーバー上のプロジェクトを自動的に更新します。 プロジェクトを更新し、プロジェクト管理者は、結果を確認するか、計画を調整することがなく再公開できます。 
    
    > [!NOTE]
    > CSOM は、送信のステータスの更新をサポートしますが、現在の状態の承認をサポートしていません。 
  
- **リモート イベント レシーバーでデータを Project Server の評価**イベントの前の**ProjectCreating**のリモート イベント レシーバーは、イベントをキャンセルするのにかどうかを判断するために Project Server のデータ、CSOM からを使用できます。 たとえば、プロジェクトを作成する前に既存のプロジェクトとプロジェクトの提案を比較します。 
    
- **宣言型の Project Server ワークフローをサポート**CSOM は、SharePoint Designer 2013 で作成された Project Server ワークフローを有効にします。 CSOM は、Windows ワークフロー Foundation バージョン 4 (WF4) を使用してワークフロー定義をサポートしています。 (PSI は、WF4 のワークフローをサポートしていない)。 
    
- **複雑な Project Server ワークフローを作成します。** Visual Studio 2012 でワークフローを開発するときに複雑なアクションをワークフロー ステージ内で、CSOM を使用したり、カスタム ワークフロー アクションを作成できます。 
    
## <a name="what-the-csom-does-not-do"></a>CSOM が行わないこと
<a name="pj15_WhatTheCSOM_DoesNotDo"> </a>

CSOM は、PSI を完全に置き換えるものではありません。 CSOM は、PSI サービスを内部的に使用するために、PSI を持つ同じ機能の制限事項の多くは、CSOM。 ローカル プロジェクト (.mpp ファイル) のデータへのアクセス権を持たないなど、PSI の制限だけでなく、CSOM では、Project Web App を処理する管理者用の機能は含まれません。 たとえば、[サイトの設定の Project Web App の [権限] ページには、カスタム セキュリティ グループを作成するを処理できます。 
  
PSI も、CSOM を処理するアクションのリストで[どのような PSI は行われない](what-the-psi-does-and-does-not-do.md)の*と、PSI を行いません*を参照してください。
  
### <a name="psi-services-that-the-csom-does-not-cover"></a>CSOM が対応していない PSI サービス
<a name="pj15_WhatTheCSOM_PSIServices"> </a>

CSOM には、次の PSI サービスの機能は含まれません。
  
- **管理サービス**管理用設定および Project Server で、会計年度期間を作成してをタイムシートの設定を行うなど、関連するプロジェクトのサイトの操作を管理するには、 [WebSvcAdmin.Admin](https://msdn.microsoft.com/library/WebSvcAdmin.Admin.aspx)クラスの PSI メソッドを使用します。 自体を Project Web App サーバー設定] ページにリンクされているページの多くの**管理**方法を使用する (*サーバー名*を http://  /  *ProjectServerName* /_layouts/15/pwa/Admin/Admin.aspx)。 
    
- **アーカイブ ・ サービス**保存し、プロジェクト、リソース、およびアーカイブ テーブルのユーザー設定フィールドなどのエンティティを管理、[アーカイブ](https://msdn.microsoft.com/library/WebSvcArchive.Archive.aspx)クラスの PSI メソッドを使用します。 
    
- **CubeAdmin サービス**作成し、設置の OLAP キューブの管理、PSI メソッドを使用して、クラスでは、 [WebSvcCubeAdmin.CubeAdmin](https://msdn.microsoft.com/library/WebSvcCubeAdmin.CubeAdmin.aspx) 、または、OLAP データベースの管理ページを使用して (*サーバー名*を http://  /  ** ProjectServerName/_layouts/15/pwa/CubeAdmin/CubeAnalysisAdmin.aspx) Project Web App で。 
    
    > [!NOTE]
    > プロジェクトのオンラインでは、OLAP キューブはサポートされていません。 
  
- **ドライバー サービス**作成し、プロジェクトのポートフォリオ分析用のビジネス ドライバーを管理する、 [WebSvcDriver.Driver](https://msdn.microsoft.com/library/WebSvcDriver.Driver.aspx)クラスの PSI メソッドを使用します。 
    
- **LoginForms サービスおよび LoginWindows サービス**OAuth または Windows 認証では、 **ProjectContext**オブジェクトの初期化中に、CSOM で認証が行われます。 [WebSvcLoginForms.LoginForms](https://msdn.microsoft.com/library/WebSvcLoginForms.LoginForms.aspx)クラスと、[の PSI メソッドを使用して、ローカルの完全信頼アプリケーションでは、フォーム認証と Windows 認証の両方を使用できます、複数の認証のためのアプリケーションを作成するにはWebSvcLoginWindows.LoginWindows](https://msdn.microsoft.com/library/WebSvcLoginWindows.LoginWindows.aspx)クラス。 
    
- **通知サービス**作成し、通知と事前通知の管理をするには、 [WebSvcNotifications.Notifications](https://msdn.microsoft.com/library/WebSvcNotifications.Notifications.aspx)クラスの PSI メソッドを使用します。 
    
- **ObjectLinkProvider サービス**作成し、web オブジェクトとドキュメントと SharePoint リスト アイテムへのリンクの管理、 [WebSvcObjectLinkProvider.ObjectLinkProvider](https://msdn.microsoft.com/library/WebSvcObjectLinkProvider.ObjectLinkProvider.aspx)クラスの PSI メソッドを使用します。 
    
- **PortfolioAnalyses サービス**作成し、ソリューションのプランナーとオプティマイザーのソリューションを含む、プロジェクト ポートフォリオ分析の管理には、 [WebSvcPortfolioAnalyses.PortfolioAnalyses](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.aspx)クラスの PSI メソッドを使用します。 
    
- **QueueSystem サービス**CSOM は、Project Server キューのジョブに関する基本的な情報を得ることができ、 [ProjectContext.WaitForQueue](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.WaitForQueue.aspx)メソッドが含まれています。 プロジェクト サーバーのキュー システムのより広範な管理のためには、 [WebSvcQueueSystem.QueueSystem](https://msdn.microsoft.com/library/WebSvcQueueSystem.QueueSystem.aspx)クラスの PSI メソッドを使用します。 
    
- **セキュリティ サービス**作成し、Project Server のセキュリティ グループ、テンプレート、およびカテゴリを管理して、現在のユーザーのアクセス許可を確認するには、 [WebSvcSecurity.Security](https://msdn.microsoft.com/library/WebSvcSecurity.Security.aspx)クラスの PSI メソッドを使用します。 
    
- **WssInterop サービス**に関する情報を取得し、プロジェクトのサイトを管理するには、 [WebSvcWssInterop.WssInterop](https://msdn.microsoft.com/library/WebSvcWssInterop.WssInterop.aspx)クラスの PSI メソッドを使用します。 
    
    > [!NOTE]
    > SharePoint Server 2013 では、CSOM を使用できます。 プロジェクト サイトは、SharePoint サイトです。 
  
CSOM では、PSI で使用できる拡張機能などは使用できません。たとえば、ローカルで使用する PSI 拡張機能を作成した場合、CSOM を変更して PSI 拡張機能を使用することはできません。拡張機能のシナリオは、次のような方法で実装できます。
  
- CSOM の集計は、ローカルのコンポーネントまたは Microsoft Azure 上で実行されるコンポーネント内で呼び出されます。
    
- Project Server データベースのレポート テーブルに直接アクセスする代わりに、レポート データの OData クエリを使用します。
    
- CSOM 呼び出しは、オンラインのプロジェクトからの OAuth 認証でサード パーティのアプリケーションや設置用のサーバー側コンポーネントに統合します。
    
- CSOM を使用するアプリケーションことができますもを使用してカスタム データベースか、設置型または SQL Azure とします。
    
### <a name="request-limits-of-the-csom"></a>CSOM の要求の制限
<a name="pj15_WhatTheCSOM_RequestLimits"> </a>

Project Server 2013 で CSOM は、CSOM 実装では、SharePoint Server 2013 は、上に構築し、要求の最大サイズの制限を継承します。 SharePoint では、操作要求には、2 MB の制限と、送信済みのバイナリ オブジェクトのサイズを 50 MB の制限があります。 要求のサイズは、バイナリ ラージ オブジェクトの遅延を処理および操作の極端に長いキューからサーバーを保護するために制限されています。
  
たとえば、CSOM を使用してプロジェクトを作成してから、短い名前、タスク GUID、有効期間 1d などの最小限の情報で 252 個のタスクを追加した場合、**DraftProject.Update** 要求の合計のデータ量は 2 MB 未満になります。しかし、このようなタスクを空のプロジェクトに 253 個追加しようとすると、2 MB の制限を超過し、[**Microsoft.SharePoint.Client.ServerException: 要求で使用されているリソースが多すぎます**] という例外が発生します。
  
HTTP または HTTPS では、CSOM 要求内のデータをキャプチャするには、 [Fiddler](http://www.fiddler2.com)などのツールをデバッグする web を使用することができます (http://www.fiddler2.com)。 コード例を要求のサイズのテストを実装しを小さなグループに大きな要求を分割するためのソリューションが含まれています、 [DraftProject.Update](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.DraftProject.Update.aspx)を参照してください。 
  
## <a name="see-also"></a>関連項目
<a name="pj15_WhatTheCSOM_AR"> </a>

- [Project Server のクライアント側オブジェクト モデル (CSOM)](client-side-object-model-csom-for-project-2013.md)
    
- [PSI のすること、しないこと](what-the-psi-does-and-does-not-do.md)
    
- [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx)
    

