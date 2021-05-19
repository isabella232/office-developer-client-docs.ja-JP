---
title: PSI が行うこと、行わないこと
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: eac6be6a-9a20-4bc0-8da2-b2fd93aab04f
description: Project サーバー インターフェイス (PSI) は、サーバー 2013 のオンプレミス インストールで多くのサーバー側プロセスを自動化Projectできます。 ただし、いくつかの関数では、複数の関数を使用する必要Microsoft Project Professional 2013。
ms.openlocfilehash: b93c3535ca6693a84d11370de17bc18375f168ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346530"
---
# <a name="what-the-psi-does-and-does-not-do"></a>PSI のすること、しないこと

Project サーバー インターフェイス (PSI) は、サーバー 2013 のオンプレミス インストールで多くのサーバー側プロセスを自動化Projectできます。 ただし、いくつかの関数では、複数の関数を使用する必要Microsoft Project Professional 2013。
  
|||
|:-----|:-----|
|||
   
PSI は、すべての機能にサーバー ベースの代替手段を提供するのではなく、Project Professional 2013 の機能を補完Project Professionalされています。 サード パーティの開発者は、PSI を使用して、Project Web App およびプロジェクト ワークスペースのオンプレミス インストール用の Web パーツ の作成、オンプレミスの Project Server データを操作するカスタム Windows アプリケーションと Web アプリケーションの作成、プロジェクト ポートフォリオ管理のワークフロー ロジックの開発、ローカルの完全信頼イベント ハンドラーの開発、Project Server と他のアプリケーションの統合を支援できます。 PSI は、Office ストア、モバイル デバイス、またはタブレット用のアプリの開発には使用できません。このためには、クライアント側オブジェクト モデル (CSOM) を使用できます。
  
> [!NOTE]
> PSI は、CSOM が提供するよりも、Project Server 2013 に対してより包括的なプログラムインターフェイスを提供します。 ただし、CSOM に必要な機能がない場合を除き、新規アプリケーションの開発には CSOM を使用することをお勧めします。 詳細については、「[What the CSOM does and does not do](what-the-csom-does-and-does-not-do.md)」を参照してください。 
  
## <a name="usage-scenarios-for-the-psi"></a>PSI の使用シナリオ
<a name="pj14_WhatPSIDoes_UsageScenarios"> </a>

以下に、PSI がサーバー側のプロジェクトおよび計算のためにサポートするアプリケーションの例をいくつか示します。
  
- **サーバー内のエンティティ** の作成または管理をProjectするProject Professional 2013 と Project Web App は、プロジェクト、エンタープライズ リソース、ユーザー設定フィールドなどのエンティティの管理と作成を処理するように設計されていますが、多くの場合、カスタム アプリケーションは一括ジョブや繰り返しジョブで時間を節約できます。 PSI は、OLAP キューブ、プロジェクト ポートフォリオ分析、ビジネス ドライバー、通知、オブジェクト リンク プロバイダー、セキュリティ、SharePoint との相互運用性など、CSOM では不可能な、いくつかの種類のジョブの自動化を行うことができます。 
    
- **データベースの発行済みテーブルまたはアーカイブ テーブルのデータをProjectする** 下書き、発行済み、およびアーカイブ テーブルへの直接データベース アクセスはサポートされていないので、PSI を使用して、レポート テーブルまたはビューで使用できないデータを読み取りできます。 たとえば、アーカイブ テーブルに格納されているプロジェクトのバージョン、日付、変更に関する情報を取得し、Web パーツの JS Grid コントロールに情報を設定します。 
    
- **状態とタイムシートのデータを検証する** ローカルのプレイベント ハンドラーの PSI を使用して、ユーザーが入力した割り当て状態またはタイムシート データを検証してから、データをユーザーに保存Project Web App。 
    
- **保守プロジェクト** リソース計画と共に使用するプレースホルダー プロジェクトを作成します。リソースに対する保守作業または基本業務用の時間を確保または予約します。通常、保守プロジェクトはタスクを持っていません。 
    
- **財務プロジェクトの作成** 財務システムとの統合用にタイムシートを使用して、時間取得のためのプロジェクトを作成します。 財務システムのコスト ブレークダウン ストラクチャを反映した、財務コードの階層を作成します。 財務プロジェクトには、スケジュールや実績の更新は必要ありません。 
    
- **会計システムとの統合** 財務システムと課金システムに入力し、予算を比較する目的のために、プロジェクトに関連するリソース コストと経費を取得します。 システム間のタスク、リソース、および割り当てを同期します。 あるシステムのタイムシート データを取得して、他のタイムシート データに入力します (使用するタイムシートは、組織または個別のプロジェクトのニーズによって決まります)。 
    
- **チーム メンバーの更新の自動化** アクティブに管理されていないプロジェクトについて、プロジェクト チーム メンバーからの進捗およびその他の変更に関してサーバー上で自動的にプロジェクトが更新されるようにします。 プロジェクト管理者が結果を見直したり、計画を調整したりしなくても、プロジェクトを更新したり、再発行したりできます。 
    
- **ローカルProjectイベント ハンドラーの** サーバー データの評価ProjectCreating プレイベントのローカル イベント ハンドラーは **、PSI** Project Server データを使用して、イベントをキャンセルするかどうかを判断できます。 たとえば、プロジェクトを作成する前に、既存のプロジェクトとプロジェクトの提案を比較することができます。 
    
- **需要管理用のカスタム ワークフロー アクティビティを作成する** ローカルの完全信頼ワークフロー アクティビティの PSI を使用して、エンタープライズ プロジェクト テンプレートに基づいてプロジェクト提案を変更および更新します。 プロジェクト ユーザー設定フィールドを使用して開始および承認プロセスに必要な情報でプロジェクトにタグを付けます。 主要なマイルストーンまたは成果物のプロジェクト フェーズを識別するタスクを追加します。 承認された提案は、ワークフローによって Project Professional で管理される完全なプロジェクトに変更することができます。 
    
- **PSI 拡張機能を作成する** (**非推奨)。** 拡張機能は Server 2013 Project非推奨であり、今後のリリースではサポートされません)。PSI は、カスタム サービスを使用して、WINDOWS (WCF) インターフェイスを使用して拡張できます。 PSI 拡張機能は Project Server コンピューターで実行でき、組み込みの PSI サービスで使用するのと同じセキュリティ インフラストラクチャを使用できます。 拡張機能では、レポート テーブルのクエリ、別のデータベース テーブルの使用、帯域幅を節約するための PSI 呼び出しの統合、サードパーティ アプリケーションやその他のサーバー側コンポーネントとの統合を行うことができます。 詳細については、「[PSI 拡張機能の開発](https://msdn.microsoft.com/library/1b484623-94fb-47c9-84c1-3e68a9133042%28Office.15%29.aspx)」を参照してください。
    
- **ローカルの完全信頼アプリケーションで偽装を使用する** PSI の WCF インターフェイスへの呼び出しは偽装できます。そのため、アプリケーションは偽装されたユーザーのセキュリティアクセス許可を前提とします。 偽装は限定的かつ慎重に使用する必要があります。 他のユーザーの状態情報の読み取りと更新には、偽装は必要ありません。 偽装を必要とする新しいアプリケーションでは、PSI ではなく CSOM および OAuth プロトコルを使用する必要があります。 PSI での偽装の詳細については、「Use [Impersonation with WCF」を参照してください](https://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)。
    
> [!NOTE]
> 場合によっては、PSI は CSOM とクライアント アプリケーションで使用Project Online。 ASMX ベースの PSI Web サービスを使用する場合、アプリケーションには、CSOM で [Microsoft.ProjectServer.Client.ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) オブジェクトを認証するメソッドと **、System.Web.Services.Protocols.SoapHttpClientProtocol** クライアント オブジェクトを認証するメソッドが含まれる必要があります。 SharePoint CSOM で Web サービスを使用する例については、「[クレーム ベース認証を使用した SharePoint Online でのリモート認証](https://msdn.microsoft.com/library/49067f7a-3020-478f-ba97-4b7ce3ea9b87%28Office.15%29.aspx)」を参照してください。 >アプリ レベルのアクセス許可が制限されたため、パブリック ストアでの配布用に設計されたアプリでは PSI をOfficeできません。 その場合は、CSOM のみ使用できます。 
  
## <a name="what-the-psi-does-not-do"></a>PSI が行わないこと
<a name="pj14_WhatPSIDoes_DoesNotDo"> </a>

PSI が行えることはたくさんありますが、PSI が行えないこともあります。以下に、PSI では行えず、CSOM では行えることを 2 つ示します。
  
### <a name="project-online-and-remote-event-receivers"></a>Project Onlineリモート イベント レシーバー

PSI の主な制限は、次のProject Online。 PSI を使用するアプリケーションには、Project Server の社内インストールに対する完全信頼アクセス権が必要です。 たとえば、PSI はリモート イベント レシーバーでは使用できません。イベント レシーバーは、イベント レシーバーがサービスとしてインストールMicrosoft Azure。
  
### <a name="workflows-and-claims-authentication"></a>ワークフローおよびクレーム認証

ワークフロー Foundation バージョン 4 (WF4) Windowsを使用するワークフロー定義では、PSI が直接サポートしないクレーム認証が必要です。 つまり、PSI を使用して、WF4 ワークフロー定義を持つエンタープライズ プロジェクトタイプ (EPT) を持つ Project Server 2013 でプロジェクトを作成することはできません。
  
PSI を使用して、ワークフローがない EPT または従来の WF3.5 定義 (Project Server 2010 のワークフロー バージョン) を使用してプロジェクトを作成できます。 WF4 定義を持つ EPT でプロジェクトを作成するには、CSOM を使用します。
  
 **Project Professional を必要とするアクション:**
  
次のリストは、PSI と CSOM のどちらでも行うことのできない処理を示しています。
  
#### <a name="local-data"></a>ローカル データ

- ローカル プロジェクト (.mpp ファイル) でのデータの操作。たとえば、コスト単価表またはローカル リソースの利用可能時間の定義。 
    
- ローカル基本カレンダーまたはリソース カレンダー (カレンダーの例外を含む) の定義または編集。
    
- ローカル ユーザー設定フィールドの定義 (PSI で、タスク、リソース、および割り当てのローカル ユーザー設定フィールドの値を編集することは可能です)。
    
#### <a name="enterprise-data"></a>エンタープライズ データ

- エンタープライズ グローバル テンプレートのチェック アウトまたは編集。 Project Server 2013 のエンタープライズ グローバル データは、Project データベース内のバイナリ データ テーブルのセットであり、Office Project Server 2007 以前のバージョンのプロジェクト テンプレートではありません。
    
- エンタープライズ カレンダーの定義または編集。 [Calendar メソッドは](https://msdn.microsoft.com/library/WebSvcCalendar.Calendar.aspx)、予定表の例外のみを管理します。 
    
#### <a name="master-projects-and-cross-project-links"></a>マスター プロジェクトおよびプロジェクト間のリンク

- マスター プロジェクトの作成とサブプロジェクトの挿入。
    
- マスター プロジェクト全体にわたるクリティカル パスのスケジューリング。 
    
- プロジェクト間のリンクの作成。
    
#### <a name="resources"></a>リソース

- リソースの平準化の要求または実行。
    
- 割り当て上のリソースの変更 (PSI を使用して割り当てを削除し、新しい割り当てを作成することは可能です)。
    
- 認められた実際の作業 (実績) を持つリソースの削除または置換。
    
- 時間単価型、数量単価型、およびコスト型の間でのリソースの種類の変更。
    
- リソース カレンダーの作成または編集。
    
- タスクにリソースを追加する場合、PSI は Project Professional のように作業を自動的に再配布しません。割り当てで作業の配布を選択して明示的に設定するのは、開発者の役割です。
    
#### <a name="cost-resources"></a>Cost resources

- コスト リソースと割り当ての編集、作成、または削除は、Project[使用します](https://msdn.microsoft.com/library/WebSvcProject.Project.aspx)。 Resource [メソッドは](https://msdn.microsoft.com/library/WebSvcResource.Resource.aspx) コスト リソースを作成できますが、編集することはできません。 
    
#### <a name="work-contours"></a>作業配分

- タイムスケール データの編集。
    
    > [!NOTE]
    > [Statusing Web サービスの UpdateStatus](https://msdn.microsoft.com/library/WebSvcStatusing.Statusing.UpdateStatus.aspx)メソッドは、プロジェクト マネージャーが割り当てデータを更新して発行した後、割り当て時のタイムスケール実績を編集できます。  
  
- 割り当ての配分型 (均等型、増加型、減少型など) の設定または変更。
    
#### <a name="baselines-and-earned-value"></a>基準計画および達成額

- 基準計画の保存または基準計画データの編集。 
    
- 進捗日の設定。
    
- 差異および達成額の計算。 
    
#### <a name="interactive-scheduling"></a>対話型スケジューリング

- 対話型スケジューリングのサポート (Project Server は対話を非同期に処理するため、対話型スケジューリングは Project Professional を使用して行う必要があります)。
    
    > [!NOTE]
    > プログラムによる動作の変更を避けるため、Project Server 2010 から転送される PSI メソッドは、Project Server 2013 でも同様に動作します。 たとえば [、QueueUpdateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx) には引き続き同じ制限があり、以前のサーバー側スケジューリング エンジンを使用します。 新しい[QueueUpdateProject2](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject2.aspx)メソッドは、これらの制限の多くを削除し、Project Server 2013 サーバー側の新しいスケジューリング エンジン (Project Professional 2013 と同じスケジュール エンジン) を使用します。 
  
#### <a name="wbs"></a>WBS

- Work Breakdown Structure (WBS) コード マスクの定義。 
    
#### <a name="tasks"></a>タスク

- タスクの種類 (作業時間固定、期間固定、または単位数固定) の変更。
    
- タスクが残存作業優先であるかどうかの変更。
    
- タスクの固定コスト計上の時期の変更。
    
- [プロパティ] フィールドの [TASK_NOTES](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_NOTES.aspx) 変更します。 PSI は、.rtf バイナリ データであるタスク メモのテキスト部分のみを読み取ることができます。 ただし、テキスト データである割り当 [てメモ (ASSN_NOTES)](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.AssignmentRow.ASSN_NOTES.aspx) を編集できます。 レポート データベースは、タスク メモまたは割り当てメモを含みません。 
    
- 定期タスクの作成または編集。
    
- 既存のタスクでのタスク カレンダーの割り当てまたは変更。
    
- タスク カレンダーを使用した新しいタスクの作成。
    
- [タスク] フィールドの [値TASK_IGNORES_RES_CAL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_IGNORES_RES_CAL.aspx) 変更します (タスクはリソースカレンダーを無視します)。 
    
- 同じ呼び出しで追加の変更が行われた場合は [、QueueUpdateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx) を使用してタスクのアクティブな状態を変更します。 詳細については、「サーバーのプログラミング」*の「Project* のスケジュール設定 [」セクションProject参照してください](project-server-programmability.md)。
    
#### <a name="summary-tasks"></a>サマリー タスク

- サマリー タスクでの割り当ての作成または変更。
    
    > [!NOTE]
    > Project Professional またはその他の方法を使用してサマリー タスク上で割り当てを作成しないことをお勧めします。 詳細については、「サーバーのプログラミング」*の「Project* のスケジュール設定 [」セクションProject参照してください](project-server-programmability.md)。 
  
- 通常サブタスクから重ね合わされるサマリー タスク フィールドの編集。サーバー側プロジェクトは、サマリー タスクに情報を設定してサブタスクにプッシュする代わりに、常にサマリー情報を重ね合わせます。サマリー タスクでは、以下のフィールドのみを編集できます。
    
  - タスクの依存関係
    
  - 式ではないユーザー設定フィールド
    
  - [TASK_NAME](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_NAME.aspx)
    
  - [TASK_OUTLINE_LEVEL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_OUTLINE_LEVEL.aspx)
    
  - [TASK_IS_MARKED](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_IS_MARKED.aspx)
    
  - [TASK_CONSTRAINT_TYPE](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_CONSTRAINT_TYPE.aspx)
    
  - [TASK_CONSTRAINT_DATE](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_CONSTRAINT_DATE.aspx)
    
  - [TASK_PRIORITY](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_PRIORITY.aspx)
    
  - [TASK_DEADLINE](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_DEADLINE.aspx)
    
  - [TASK_FIXED_COST](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_FIXED_COST.aspx)
    
  - [TASK_FIXED_COST_ACCRUAL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_FIXED_COST_ACCRUAL.aspx) (タスクの作成時にのみ値を設定する) 
    
  - [TASK_WBS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_WBS.aspx)
    
プロジェクトのサマリー タスクについては、PSI の制限は、Project Professional に対するものと同じです。PSI は、予算割り当てを編集できます。これには、コスト型予算も含まれます。
  
#### <a name="project-level-calculation-options"></a>プロジェクト レベルの計算オプション

- Schedule From Start (SFS) と Schedule From Finish (SFF) の間でのプロジェクトの種類の変更 (PSI はプロジェクトを SFS または SFF として作成できますが、いったん作成したプロジェクトは、Project Professional でのみ変更できます)。
    
- プロジェクトの作成後にプロジェクトの基本カレンダー[(CAL_UID)](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.CAL_UID.aspx) を変更します。 
    
- 計算のオプションの変更。プロジェクトの作成時に、PSI を使用して以下の計算オプションを設定できますが、これらのオプションを変更するには Project Professional が必要です (Backstage ビューで、[**オプション**] を選択し、[**Project のオプション**] ダイアログ ボックスの [**スケジュール**] タブを選択します)。 
    
  - [PROJ_OPT_CALC_ACT_COSTS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_CALC_ACT_COSTS.aspx)
    
  - [PROJ_OPT_CRITICAL_SLACK_LIMIT](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_CRITICAL_SLACK_LIMIT.aspx)
    
  - [PROJ_OPT_HONOR_CONSTRAINTS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_HONOR_CONSTRAINTS.aspx)
    
  - [PROJ_OPT_MOVE_ACTUAL_IF_LATER](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_MOVE_ACTUAL_IF_LATER.aspx)
    
  - [PROJ_OPT_MOVE_ACTUAL_TO_STATUS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_MOVE_ACTUAL_TO_STATUS.aspx)
    
  - [PROJ_OPT_MOVE_REMAINING_IF_EARLIER](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_MOVE_REMAINING_IF_EARLIER.aspx)
    
  - [PROJ_OPT_MOVE_REMAINING_TO_STATUS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_MOVE_REMAINING_TO_STATUS.aspx)
    
  - [PROJ_OPT_MULT_CRITICAL_PATHS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_MULT_CRITICAL_PATHS.aspx)
    
  - [PROJ_OPT_SPLIT_IN_PROGRESS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_SPLIT_IN_PROGRESS.aspx)
    
  - [PROJ_OPT_SPREAD_ACT_COSTS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_SPREAD_ACT_COSTS.aspx)
    
  - [PROJ_OPT_SPREAD_PCT_COMP](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_SPREAD_PCT_COMP.aspx)
    
  - [PROJ_OPT_TASK_UPDATES_RES](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_TASK_UPDATES_RES.aspx)
    
## <a name="see-also"></a>関連項目

- [CSOM ができること、できないこと](what-the-csom-does-and-does-not-do.md)  
- [Project Server プログラミング](project-server-programmability.md)   
- [クレーム ベース認証を使用した SharePoint Online でのリモート認証](https://msdn.microsoft.com/library/49067f7a-3020-478f-ba97-4b7ce3ea9b87%28Office.15%29.aspx)  
- [Office アドイン](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins) 
    

