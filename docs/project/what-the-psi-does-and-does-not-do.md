---
title: PSI が行うこと、行わないこと
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: eac6be6a-9a20-4bc0-8da2-b2fd93aab04f
description: project server Interface (PSI) は、project server 2013 のオンプレミスのインストールで多くのサーバー側プロセスを自動化するのに役立ちます。 ただし、いくつかの関数では Microsoft Project Professional 2013 を使用する必要があります。
ms.openlocfilehash: b93c3535ca6693a84d11370de17bc18375f168ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346530"
---
# <a name="what-the-psi-does-and-does-not-do"></a>PSI のすること、しないこと

project server Interface (PSI) は、project server 2013 のオンプレミスのインストールで多くのサーバー側プロセスを自動化するのに役立ちます。 ただし、いくつかの関数では Microsoft Project Professional 2013 を使用する必要があります。
  
|||
|:-----|:-----|
|||
   
PSI は、project professional 2013 の機能を補完するように設計されており、project professional のすべての機能に、サーバーベースの代替手段を提供するものではありません。 サードパーティの開発者は、PSI を使用して、project web App とプロジェクトワークスペースのオンプレミスインストール用の Web パーツを作成したり、オンプレミスの project Server データを操作するカスタム Windows アプリケーションと web アプリケーションを作成したり、ワークフローを開発したりすることができます。プロジェクトポートフォリオ管理のロジック、ローカルの完全信頼イベントハンドラーの開発、および project Server と他のアプリケーションとの統合。 PSI は、Office ストア、モバイルデバイス、またはタブレット用アプリの開発には使用できません。そのためには、クライアント側オブジェクトモデル (csom) を使用できます。
  
> [!NOTE]
> PSI は、csom が提供するよりも、Project Server 2013 用のより包括的なプログラムインターフェイスを提供します。 ただし、CSOM に必要な機能がない場合を除き、新規アプリケーションの開発には CSOM を使用することをお勧めします。 詳細については、「[What the CSOM does and does not do](what-the-csom-does-and-does-not-do.md)」を参照してください。 
  
## <a name="usage-scenarios-for-the-psi"></a>PSI の使用シナリオ
<a name="pj14_WhatPSIDoes_UsageScenarios"> </a>

以下に、PSI がサーバー側のプロジェクトおよび計算のためにサポートするアプリケーションの例をいくつか示します。
  
- **Project Server でのエンティティの作成または管理を自動化する**project Professional 2013 と project Web App は、プロジェクト、エンタープライズリソース、ユーザー設定フィールドなどのエンティティの管理および作成を処理するように設計されていますが、カスタムアプリケーションがバルクまたは一括して時間を節約できる場合がよくあります。繰り返しジョブ。 PSI は、OLAP キューブ、プロジェクト ポートフォリオ分析、ビジネス ドライバー、通知、オブジェクト リンク プロバイダー、セキュリティ、SharePoint との相互運用性など、CSOM では不可能な、いくつかの種類のジョブの自動化を行うことができます。 
    
- **Project データベースの発行済みまたはアーカイブテーブル内のデータを取得する**下書き、発行済み、およびアーカイブテーブルへの直接データベースアクセスはサポートされていないため、PSI を使用して、レポートテーブルまたはビューで利用できないデータを読み取ることができます。 たとえば、アーカイブテーブルに格納されているプロジェクトのバージョン、日付、変更に関する情報を取得し、その情報を含む web パーツに JS Grid コントロールを設定します。 
    
- **statusing およびタイムシートデータを検証**するローカルのイベント前ハンドラーで PSI を使用して、データが Project Web App に保存される前に、ユーザーが入力した割り当て状態またはタイムシートデータを検証します。 
    
- **保守プロジェクト** リソース計画と共に使用するプレースホルダー プロジェクトを作成します。リソースに対する保守作業または基本業務用の時間を確保または予約します。通常、保守プロジェクトはタスクを持っていません。 
    
- **財務プロジェクトの作成** 財務システムとの統合用にタイムシートを使用して、時間取得のためのプロジェクトを作成します。 財務システムのコスト ブレークダウン ストラクチャを反映した、財務コードの階層を作成します。 財務プロジェクトには、スケジュールや実績の更新は必要ありません。 
    
- **会計システムとの統合** 財務システムと課金システムに入力し、予算を比較する目的のために、プロジェクトに関連するリソース コストと経費を取得します。 システム間のタスク、リソース、および割り当てを同期します。 あるシステムのタイムシート データを取得して、他のタイムシート データに入力します (使用するタイムシートは、組織または個別のプロジェクトのニーズによって決まります)。 
    
- **チーム メンバーの更新の自動化** アクティブに管理されていないプロジェクトについて、プロジェクト チーム メンバーからの進捗およびその他の変更に関してサーバー上で自動的にプロジェクトが更新されるようにします。 プロジェクト管理者が結果を見直したり、計画を調整したりしなくても、プロジェクトを更新したり、再発行したりできます。 
    
- **ローカルの完全信頼イベントハンドラーで Project Server データを評価**するイベントを**作成**するプロジェクトのローカルイベントハンドラーは、PSI の Project Server データを使用して、イベントをキャンセルするかどうかを判断することができます。 たとえば、プロジェクトを作成する前に、既存のプロジェクトとプロジェクトの提案を比較することができます。 
    
- **需要管理のためのカスタムワークフローアクティビティを作成する**エンタープライズプロジェクトテンプレートに基づいてプロジェクト提案を変更および更新するには、ローカルの完全信頼ワークフローアクティビティで PSI を使用します。 プロジェクト ユーザー設定フィールドを使用して開始および承認プロセスに必要な情報でプロジェクトにタグを付けます。 主要なマイルストーンまたは成果物のプロジェクト フェーズを識別するタスクを追加します。 承認された提案は、ワークフローによって Project Professional で管理される完全なプロジェクトに変更することができます。 
    
- **PSI 拡張機能を作成する**(**非推奨)。** 拡張機能は Project Server 2013 で廃止され、今後のリリースではサポートされなくなります。)PSI は、Windows Communication Foundation (WCF) インターフェイスを使用してカスタムサービスで拡張することができます。 PSI 拡張機能は Project Server コンピューターで実行でき、組み込みの PSI サービスで使用するのと同じセキュリティ インフラストラクチャを使用できます。 拡張機能では、レポート テーブルのクエリ、別のデータベース テーブルの使用、帯域幅を節約するための PSI 呼び出しの統合、サードパーティ アプリケーションやその他のサーバー側コンポーネントとの統合を行うことができます。 詳細については、「[PSI 拡張機能の開発](https://msdn.microsoft.com/library/1b484623-94fb-47c9-84c1-3e68a9133042%28Office.15%29.aspx)」を参照してください。
    
- **ローカルの完全信頼アプリケーションで偽装を使用する**PSI の WCF インターフェイスの呼び出しは偽装されることができるので、アプリケーションは偽装されたユーザーのセキュリティアクセス許可を引き受けることができます。 偽装は限定的かつ慎重に使用する必要があります。 他のユーザーの状態情報の読み取りと更新には、偽装は必要ありません。 偽装を必要とする新しいアプリケーションでは、PSI ではなく CSOM および OAuth プロトコルを使用する必要があります。 PSI を使用した偽装の詳細については、「 [WCF で偽装を使用する](https://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)」を参照してください。
    
> [!NOTE]
> 場合によっては、csom と Project Online を使用して、クライアントアプリケーションで PSI を使用することができます。 ASMX ベースの PSI web サービスを使用する場合、アプリケーションには、csom で[microsoft.projectserver.client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx)オブジェクトを認証するためのメソッドと、**を認証するメソッドが含まれている必要があります。SoapHttpClientProtocol**のクライアントオブジェクトを示します。 SharePoint CSOM で Web サービスを使用する例については、「[クレーム ベース認証を使用した SharePoint Online でのリモート認証](https://msdn.microsoft.com/library/49067f7a-3020-478f-ba97-4b7ce3ea9b87%28Office.15%29.aspx)」を参照してください。 > アプリレベルのアクセス許可が制限されているため、公開 Office ストアで配布するように設計されたアプリで PSI を使用することはできません。 その場合は、CSOM のみ使用できます。 
  
## <a name="what-the-psi-does-not-do"></a>PSI が行わないこと
<a name="pj14_WhatPSIDoes_DoesNotDo"> </a>

PSI が行えることはたくさんありますが、PSI が行えないこともあります。以下に、PSI では行えず、CSOM では行えることを 2 つ示します。
  
### <a name="project-online-and-remote-event-receivers"></a>Project Online とリモートイベントレシーバー

PSI の主な制限は Project Online を使用しています。 PSI を使用するアプリケーションには、Project Server の社内インストールに対する完全信頼アクセス権が必要です。 たとえば、Microsoft Azure でイベントレシーバーがサービスとしてインストールされているリモートイベントレシーバーでは、PSI を使用することはできません。
  
### <a name="workflows-and-claims-authentication"></a>ワークフローおよびクレーム認証

Windows workflow Foundation version 4 (WF4) を使用するワークフロー定義にはクレーム認証が必要です。これは、PSI が直接サポートしていません。 つまり、PSI を使用して project Server 2013 に、WF4 ワークフロー定義でエンタープライズプロジェクトの種類 (EPT) を含むプロジェクトを作成することはできません。
  
PSI を使用して、ワークフローを持たない ept でプロジェクトを作成するか、従来の wf 3.5 の定義 (Project Server 2010 のワークフローバージョン) を使用することができます。 WF4 定義を持つ EPT でプロジェクトを作成するには、CSOM を使用します。
  
 **Project Professional を必要とするアクション:**
  
次のリストは、PSI と CSOM のどちらでも行うことのできない処理を示しています。
  
#### <a name="local-data"></a>ローカル データ

- ローカル プロジェクト (.mpp ファイル) でのデータの操作。たとえば、コスト単価表またはローカル リソースの利用可能時間の定義。 
    
- ローカル基本カレンダーまたはリソース カレンダー (カレンダーの例外を含む) の定義または編集。
    
- ローカル ユーザー設定フィールドの定義 (PSI で、タスク、リソース、および割り当てのローカル ユーザー設定フィールドの値を編集することは可能です)。
    
#### <a name="enterprise-data"></a>エンタープライズ データ

- エンタープライズ グローバル テンプレートのチェック アウトまたは編集。 project server 2013 のエンタープライズグローバルデータは、project データベース内のバイナリデータテーブルのセットです。これは、Office project Server 2007 以前のバージョンの project テンプレートではありません。
    
- エンタープライズ カレンダーの定義または編集。 [カレンダー](https://msdn.microsoft.com/library/WebSvcCalendar.Calendar.aspx)メソッドは、予定表の例外のみを管理します。 
    
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

- [プロジェクト](https://msdn.microsoft.com/library/WebSvcProject.Project.aspx)の方法を使用して、コスト単価型リソースおよび割り当てを編集、作成、または削除できます。 [Resource](https://msdn.microsoft.com/library/WebSvcResource.Resource.aspx)メソッドは、コスト型リソースを作成することはできますが、編集することはできません。 
    
#### <a name="work-contours"></a>作業配分

- タイムスケール データの編集。
    
    > [!NOTE]
    > **Statusing** Web サービスの[updatestatus](https://msdn.microsoft.com/library/WebSvcStatusing.Statusing.UpdateStatus.aspx)メソッドは、プロジェクトマネージャーが割り当てデータを更新して発行した後に、割り当ての時間単位の実績を編集できます。 
  
- 割り当ての配分型 (均等型、増加型、減少型など) の設定または変更。
    
#### <a name="baselines-and-earned-value"></a>基準計画および達成額

- 基準計画の保存または基準計画データの編集。 
    
- 進捗日の設定。
    
- 差異および達成額の計算。 
    
#### <a name="interactive-scheduling"></a>対話型スケジューリング

- 対話型スケジューリングのサポート (Project Server は対話を非同期に処理するため、対話型スケジューリングは Project Professional を使用して行う必要があります)。
    
    > [!NOTE]
    > プログラムによる動作を変更しないようにするため、project server 2010 から転送される PSI メソッドは、project server 2013 でも同じように動作します。 たとえば、 [queueupdateproject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx)は依然として同じ制限を持っており、以前のサーバー側のスケジューリングエンジンを使用します。 新しい[QueueUpdateProject2](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject2.aspx)メソッドは、これらの制限の多くを削除し、新しい project Server 2013 サーバー側のスケジューリングエンジンを使用します。これは、project Professional 2013 と同じスケジューリングエンジンです。 
  
#### <a name="wbs"></a>WBS

- Work Breakdown Structure (WBS) コード マスクの定義。 
    
#### <a name="tasks"></a>タスク

- タスクの種類 (作業時間固定、期間固定、または単位数固定) の変更。
    
- タスクが残存作業優先であるかどうかの変更。
    
- タスクの固定コスト計上の時期の変更。
    
- [TASK_NOTES](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_NOTES.aspx)フィールドの内容を変更する。 PSI は、.rtf バイナリ データであるタスク メモのテキスト部分のみを読み取ることができます。 しかし、テキストデータである割り当てメモ ( [ASSN_NOTES](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.AssignmentRow.ASSN_NOTES.aspx) ) を編集できます。 レポート データベースは、タスク メモまたは割り当てメモを含みません。 
    
- 定期タスクの作成または編集。
    
- 既存のタスクでのタスク カレンダーの割り当てまたは変更。
    
- タスク カレンダーを使用した新しいタスクの作成。
    
- [TASK_IGNORES_RES_CAL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_IGNORES_RES_CAL.aspx)フィールドの値を変更する (リソースカレンダーを無視するタスク)。 
    
- 同じ呼び出しで追加の変更が加えられた場合、 [queueupdateproject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx)を使用して、タスクのアクティブな状態を変更します。 詳細については、「 [project server のプログラミング](project-server-programmability.md)」の「サーバー」セクション*で、プロジェクトのスケジュール*を参照してください。
    
#### <a name="summary-tasks"></a>サマリー タスク

- サマリー タスクでの割り当ての作成または変更。
    
    > [!NOTE]
    > Project Professional またはその他の方法を使用してサマリー タスク上で割り当てを作成しないことをお勧めします。 詳細については、「 [project server のプログラミング](project-server-programmability.md)」の「サーバー」セクション*で、プロジェクトのスケジュール*を参照してください。 
  
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
    
  - [TASK_FIXED_COST_ACCRUAL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_FIXED_COST_ACCRUAL.aspx)(タスクの作成時にのみ値を設定する) 
    
  - [TASK_WBS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_WBS.aspx)
    
プロジェクトのサマリー タスクについては、PSI の制限は、Project Professional に対するものと同じです。PSI は、予算割り当てを編集できます。これには、コスト型予算も含まれます。
  
#### <a name="project-level-calculation-options"></a>プロジェクト レベルの計算オプション

- Schedule From Start (SFS) と Schedule From Finish (SFF) の間でのプロジェクトの種類の変更 (PSI はプロジェクトを SFS または SFF として作成できますが、いったん作成したプロジェクトは、Project Professional でのみ変更できます)。
    
- プロジェクトの作成後にプロジェクトの基本カレンダー ([CAL_UID](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.CAL_UID.aspx) ) を変更する。 
    
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

- [CSOM のすること、しないこと](what-the-csom-does-and-does-not-do.md)  
- [Project Server プログラミング](project-server-programmability.md)   
- [クレーム ベース認証を使用した SharePoint Online でのリモート認証](https://msdn.microsoft.com/library/49067f7a-3020-478f-ba97-4b7ce3ea9b87%28Office.15%29.aspx)  
- [Office アドイン](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins) 
    

