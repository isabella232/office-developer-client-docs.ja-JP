---
title: PSI が行うこと、行わないこと
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: eac6be6a-9a20-4bc0-8da2-b2fd93aab04f
description: プロジェクト Server インターフェイス (PSI) は、Project Server 2013 のオンプレミスのインストール環境で多くのサーバー側プロセスを自動化するのに役立ちます。 ですが、いくつかの関数は、Microsoft Project Professional 2013 の使用を要求します。
ms.openlocfilehash: 0afdcdf43c4748fff42f7b5bc74af6c4b59b0b07
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804694"
---
# <a name="what-the-psi-does-and-does-not-do"></a>PSI が行うこと、行わないこと

プロジェクト Server インターフェイス (PSI) は、Project Server 2013 のオンプレミスのインストール環境で多くのサーバー側プロセスを自動化するのに役立ちます。 ですが、いくつかの関数は、Microsoft Project Professional 2013 の使用を要求します。
  
|||
|:-----|:-----|
|||
   
PSI は、Project Professional のすべての機能は、サーバ ・ ベースの代替を提供するのではなく、プロジェクトの評価のための機能を補完するよう設計されています。 サード パーティの開発者は、PSI を使用して、設置の Project Web App の [プロジェクト ワークスペースの Web パーツを作成、カスタムの Windows アプリケーションとオンプレミスの Project Server のデータと対話する、ワークフローを開発する web アプリケーションの作成を支援するにはプロジェクト ポートフォリオ管理のためのロジックでは、ローカルの完全信頼のイベント ハンドラーを開発し、Project Server を他のアプリケーションに統合します。 Office ストア、モバイル デバイス、またはタブレットのためのアプリケーションを開発するため、PSI を使用することはできません。そのため、クライアント側オブジェクト モデル (CSOM) を使用できます。
  
> [!NOTE]
> PSI より包括的なプログラム インターフェイスを提供 Project Server 2013 は、CSOM で提供されます。 新しいアプリケーションを開発するのには、CSOM を使用することをお勧め、CSOM から、必要な機能が提供されない限り、します。 詳細については、[どのような CSOM しサポートしない](what-the-csom-does-and-does-not-do.md)を参照してください。 
  
## <a name="usage-scenarios-for-the-psi"></a>PSI の使用シナリオ
<a name="pj14_WhatPSIDoes_UsageScenarios"> </a>

以下に、PSI がサーバー側のプロジェクトおよび計算のためにサポートするアプリケーションの例をいくつか示します。
  
- **自動化、作成、または Project Server 内のエンティティの管理**カスタム アプリケーションが一括で時間を保存する場所の場合、多くの場合は、評価のためのプロジェクトと Project Web App には、管理し、プロジェクト、エンタープライズ リソース ユーザー設定フィールドなどのエンティティの作成を処理するために、または反復的なジョブです。 PSI には、CSOM が実行できないジョブのたとえば、OLAP キューブ、プロジェクト ポートフォリオ分析、ビジネス ドライバー、通知、オブジェクト リンク プロバイダー、セキュリティ、および SharePoint の相互運用性を持ついくつかの種類を自動化できます。 
    
- **プロジェクト データベースのアーカイブ テーブルまたは、パブリッシュされたデータを取得します。** テーブルはサポートされていないため、データベースに直接、公開、下書きにアクセスし、アーカイブがレポートのテーブルまたはビューで使用できないデータを読み取る PSI を使用することができます。 たとえば、プロジェクトのバージョン、日付、およびアーカイブ テーブルに格納されている変更に関する情報を取得し、情報を持つ web パーツ内の JS グリッド コントロールを作成し、します。 
    
- **状態管理とタイムシートのデータを検証します。** ローカルの前のイベント ハンドラーで PSI を使用すると、Project Web App でデータが保存される前に、ユーザーが入力した割り当ての状態] または [タイムシート データを検証します。 
    
- **メンテナンス プロジェクト**プロジェクトのリソース計画で使用するプレース ホルダーを作成します。 予約または本時間リソースに対する保守作業または基本業務です。 通常、保守プロジェクトにはタスクはありません。 
    
- **財務プロジェクトの作成**財務システムとの統合のためにタイムシートをタイム キャプチャ用のプロジェクトを作成します。 財務システムのコストの内訳構造を反映した、財務コードの階層を作成します。 財務プロジェクトでは、スケジュール設定やステータスの更新は必要ありません。 
    
- **会計システムとの統合**リソースのコストおよび関連する財務および請求システムをフィードするプロジェクトと予算の比較のための経費をキャプチャします。 タスク、リソース、およびシステム間での割り当てを同期します。 他のフィードを 1 つのシステムでタイムシート データをキャプチャ (組織または個々 のプロジェクトのニーズに依存するタイムシートが表示されます)。 
    
- **チーム メンバーから更新を自動化**積極的に管理されていないプロジェクトでは、進行状況とプロジェクト チームのメンバーからの他の変更をサーバー上のプロジェクトを自動的に更新します。 プロジェクトを更新し、プロジェクト管理者は、結果を確認するか、計画を調整することがなく再公開できます。 
    
- **ローカルの完全信頼のイベント ハンドラーでデータを Project Server の評価**プレ イベントの**ProjectCreating**のローカル イベント ハンドラーは、イベントをキャンセルするのにかどうかを判断するために PSI から Project Server データを使用できます。 たとえば、プロジェクトを作成する前に既存のプロジェクトとプロジェクトの提案を比較します。 
    
- **需要管理のユーザー定義ワークフロー活動を作成します。** 変更およびエンタープライズ プロジェクト テンプレートに基づいてプロジェクト提案書を更新する、ローカルの完全信頼ワークフロー アクティビティで、PSI を使用します。 開始および承認プロセスに必要な情報をプロジェクトにタグ付けするのにには、プロジェクトのユーザー設定フィールドを使用します。 主なマイルス トーンまたは成果物のプロジェクト フェーズを識別するタスクを追加します。 プロジェクトの提案が承認されると、ワークフローは、Project Professional で管理されている本格的なプロジェクトの提案を変更できます。 
    
- **作成の PSI 拡張機能**(**は使用されなくなりました**。 拡張機能で Project Server 2013 では、推奨されていませんし、将来のリリースではサポートされません。)Windows Communication Foundation (WCF) インターフェイスを使用してカスタム サービスを使用して、PSI を拡張できます。 PSI 拡張機能は、Project Server コンピューター上で実行し、組み込みの PSI サービスを使用するのと同じセキュリティ インフラストラクチャを使用することができます。 拡張機能はレポート テーブルのクエリを実行、別のデータベース テーブルを使用して、帯域幅を保存し、サードパーティ製のアプリケーションおよびその他のサーバー側コンポーネントとの統合の PSI 呼び出しを統合します。 詳細については、 [PSI 拡張機能の開発](http://msdn.microsoft.com/library/1b484623-94fb-47c9-84c1-3e68a9133042%28Office.15%29.aspx)を参照してください。
    
- **ローカルの完全信頼アプリケーションで偽装を使用**PSI の WCF インターフェイスを呼び出すことができますふりをする、できるように、アプリケーションには、偽装ユーザーのセキュリティ アクセス許可が前提としています。 注意して慎重に、偽装を使用する必要があります。 読み取りと他のユーザーの状態に関する情報を更新するには、偽装は不要です。 偽装を必要とする新しいアプリケーションでは、PSI ではなく、CSOM および OAuth プロトコルを使用する必要があります。 PSI の偽装の詳細については、 [WCF を使用して偽装](http://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)を参照してください。
    
> [!NOTE]
> いくつかの場合では、CSOM とオンライン プロジェクトでのクライアント アプリケーションで PSI を使用できます。 アプリケーションが、CSOM で[Microsoft.ProjectServer.Client.ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx)オブジェクトを認証する方法と、**を認証するためのメソッドを含める必要があります PSI の ASMX ベース web サービスを使用する場合System.Web.Services.Protocols.SoapHttpClientProtocol**クライアント オブジェクト。 SharePoint CSOM で web サービスを使用する例では、 [SharePoint Online Using Claims-Based 認証でリモートの認証](http://msdn.microsoft.com/library/49067f7a-3020-478f-ba97-4b7ce3ea9b87%28Office.15%29.aspx)を参照してください。 > 制約のあるアプリケーション ・ レベルのアクセス権があるためは Office のパブリック ストアでの配布の PSI に設計されたアプリケーションで使用できません。 その場合は、CSOM のみを使用できます。 
  
## <a name="what-the-psi-does-not-do"></a>PSI が行わないこと
<a name="pj14_WhatPSIDoes_DoesNotDo"> </a>

PSI が行えることはたくさんありますが、PSI が行えないこともあります。以下に、PSI では行えず、CSOM では行えることを 2 つ示します。
  
### <a name="project-online-and-remote-event-receivers"></a>オンラインおよびリモート イベント レシーバーをプロジェクトします。

プロジェクトをオンラインでは、PSI の主な制限です。 PSI を使用するアプリケーションでは、プロジェクトのサーバーの設置型インストールに完全信頼のアクセスが必要です。 たとえば、PSI では使用できませんリモート イベント レシーバーでは、イベント レシーバーが Microsoft Azure にサービスとしてインストールされています。
  
### <a name="workflows-and-claims-authentication"></a>ワークフローおよびクレーム認証

4 (WF4) する必要がありますクレーム認証では、PSI を直接サポートしていない Windows Workflow Foundation のバージョンを使用するためのワークフロー定義。 つまり、WF4 のワークフロー定義を使用してエンタープライズ プロジェクトの種類 (EPT) を持つ Project Server 2013 でプロジェクトを作成するのには、PSI を使用することはできません。
  
EPTs ワークフローがないとしているか、従来の WF3.5 定義 (Project Server 2010 のワークフローのバージョン) を使用するとプロジェクトを作成するのには、PSI を使用できます。 WF4 定義を持つ、EPT でプロジェクトを作成するには、CSOM を使用します。
  
 **Project Professional を必要とする操作。**
  
次のリストは、PSI と CSOM のどちらでも行うことのできない処理を示しています。
  
#### <a name="local-data"></a>ローカル データ

- ローカル プロジェクト (.mpp ファイル) でのデータの操作。たとえば、コスト単価表またはローカル リソースの利用可能時間の定義。 
    
- ローカル基本カレンダーまたはリソース カレンダー (カレンダーの例外を含む) の定義または編集。
    
- ローカル ユーザー設定フィールドの定義 (PSI で、タスク、リソース、および割り当てのローカル ユーザー設定フィールドの値を編集することは可能です)。
    
#### <a name="enterprise-data"></a>エンタープライズ データ

- チェック アウトするか、エンタープライズ グローバル テンプレートを編集します。 エンタープライズのグローバル データを Project Server 2013 では、Office Project Server 2007 と以前のバージョンのようにプロジェクト テンプレートではなく、プロジェクト データベース内のバイナリ データのテーブルのセットです。
    
- 定義またはエンタープライズ カレンダーを編集します。 [Calendar](https://msdn.microsoft.com/library/WebSvcCalendar.Calendar.aspx)のメソッドは、カレンダーの例外のみを管理します。 
    
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
    
#### <a name="cost-resources"></a>コスト型リソース

- 編集、作成、またはコスト単価型リソースと[プロジェクト](https://msdn.microsoft.com/library/WebSvcProject.Project.aspx)のメソッドを使用して、割り当てを削除します。 [リソース](https://msdn.microsoft.com/library/WebSvcResource.Resource.aspx)の方法は、コスト単価型リソースを作成できますが、編集はできません。 
    
#### <a name="work-contours"></a>作業配分

- タイムスケール データの編集。
    
    > [!NOTE]
    > [UpdateStatus](https://msdn.microsoft.com/library/WebSvcStatusing.Statusing.UpdateStatus.aspx) **状態管理**Web サービスのメソッドは、プロジェクト マネージャーが更新され、割り当てのデータを公開した後、割り当てのタイム スケール領域の実績作業時間を編集できます。 
  
- 割り当ての配分型 (均等型、増加型、減少型など) の設定または変更。
    
#### <a name="baselines-and-earned-value"></a>基準計画および達成額

- 基準計画の保存または基準計画データの編集。 
    
- 進捗日の設定。
    
- 差異および達成額の計算。 
    
#### <a name="interactive-scheduling"></a>対話型スケジューリング

- 対話型スケジューリングのサポート (Project Server は対話を非同期に処理するため、対話型スケジューリングは Project Professional を使用して行う必要があります)。
    
    > [!NOTE]
    > プログラムの動作を変更することを避けるためには、Project Server 2010 から前方に置かれる PSI メソッドの動作は Project Server 2013 でも同じ方法です。 やなどの[QueueUpdateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx)も同じ制限があります古いサーバー側のスケジュール エンジンを使用します。 新しい[QueueUpdateProject2](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject2.aspx)メソッドでは、これらの制限の多くを削除し、エンジンを使用して新しい Project Server 2013 のサーバー側スケジューリング、評価のためのプロジェクトに含まれるものと同じスケジュール エンジンであります。 
  
#### <a name="wbs"></a>WBS

- Work Breakdown Structure (WBS) コード マスクの定義。 
    
#### <a name="tasks"></a>タスク

- タスクの種類 (作業時間固定、期間固定、または単位数固定) の変更。
    
- タスクが残存作業優先であるかどうかの変更。
    
- タスクの固定コスト計上の時期の変更。
    
- [TASK_NOTES](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_NOTES.aspx)フィールドの内容を変更します。 PSI には、.rtf バイナリ データであるタスク メモのテキストの部分のみを読み取ることができます。 しかし、割り当てメモ ( [ASSN_NOTES](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.AssignmentRow.ASSN_NOTES.aspx) ) は、テキスト データを編集することができます。 レポート データベースは、タスクまたは割り当てのメモには含まれません。 
    
- 定期タスクの作成または編集。
    
- 既存のタスクでのタスク カレンダーの割り当てまたは変更。
    
- タスク カレンダーを使用した新しいタスクの作成。
    
- [TASK_IGNORES_RES_CAL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_IGNORES_RES_CAL.aspx)フィールドの値を変更する (タスクは、リソース カレンダーを無視します)。 
    
- 同じ呼び出しで追加の変更を加える場合は、 [QueueUpdateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx)を使用して、タスクの現在のステータスを変更します。 詳細については、 [Project Server プログラミング](project-server-programmability.md)する*サーバー上でプロジェクトのスケジュール設定*」を参照してください。
    
#### <a name="summary-tasks"></a>サマリー タスク

- サマリー タスクでの割り当ての作成または変更。
    
    > [!NOTE]
    > Project Professional またはその他の方法を使用して、サマリー タスクの割り当てを行わないことをお勧めします。 詳細については、 [Project Server プログラミング](project-server-programmability.md)する*サーバー上でプロジェクトのスケジュール設定*」を参照してください。 
  
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
    
  - [TASK_FIXED_COST_ACCRUAL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_FIXED_COST_ACCRUAL.aspx)(タスクを作成する場合にのみ値を設定) 
    
  - [TASK_WBS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_WBS.aspx)
    
プロジェクトのサマリー タスクについては、PSI の制限は、Project Professional に対するものと同じです。PSI は、予算割り当てを編集できます。これには、コスト型予算も含まれます。
  
#### <a name="project-level-calculation-options"></a>プロジェクト レベルの計算オプション

- Schedule From Start (SFS) と Schedule From Finish (SFF) の間でのプロジェクトの種類の変更 (PSI はプロジェクトを SFS または SFF として作成できますが、いったん作成したプロジェクトは、Project Professional でのみ変更できます)。
    
- プロジェクトの作成後、プロジェクトの基本カレンダー ([CAL_UID](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.CAL_UID.aspx) ) を変更します。 
    
- 計算のオプションを変更します。 プロジェクトが作成されるオプションを変更すると、Project Professional が必要ですと、次の計算オプションを設定するのには PSI を使用することができます。 (Backstage ビューで、**オプション**を選択、**プロジェクトのオプション**] ダイアログ ボックスで、[**スケジュール**] タブを選択) 
    
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
<a name="pj14_WhatPSIDoes_AR"> </a>

- [CSOM とものはありません。](what-the-csom-does-and-does-not-do.md)
    
- [プロジェクト サーバー プログラミング](project-server-programmability.md)
    
- [SharePoint のクレーム ベース認証を使用して、オンラインでリモートの認証](http://msdn.microsoft.com/library/49067f7a-3020-478f-ba97-4b7ce3ea9b87%28Office.15%29.aspx)
    
- [Office アドイン](http://msdn.microsoft.com/library/1e123201-6e70-45c1-a48c-d5b955896ddb%28Office.15%29.aspx)
    

