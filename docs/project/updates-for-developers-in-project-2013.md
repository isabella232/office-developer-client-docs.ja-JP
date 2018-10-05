---
title: プロジェクトの開発者用の更新プログラム
manager: soliver
ms.date: 09/29/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5b2b22cd-6e28-43a8-9092-b411da8bfb53
description: 新しい機能には、プロジェクトのクライアント用のクライアント側オブジェクト モデル (CSOM)、残りのインターフェイス、レポート、リモート イベント レシーバー、宣言型ワークフローは、および作業ウィンドウ アドインの OData サービスが含まれます。
ms.openlocfilehash: 0c4c3f9b4bb5852f2a620b2695c15de390ac9d78
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401763"
---
# <a name="updates-for-developers-in-project"></a>プロジェクトの開発者用の更新プログラム

Project Server 2013 の機能を拡張を使用するアドイン プロジェクトをオンラインに設置します。 新しい機能には、プロジェクトのクライアント用のクライアント側オブジェクト モデル (CSOM)、残りのインターフェイス、レポート、リモート イベント レシーバー、宣言型ワークフローは、および作業ウィンドウ アドインの OData サービスが含まれます。 新しい開発のために使用する必要がありますはない機能についても学びます。
  
Project Server 2013 は、Project Server 2007 の Microsoft Office で導入し、Project Server 2010 で拡張フレームワークに基づいています。 Project Server 2013 では、リファクタリング、プロジェクト Server インターフェイス (PSI) からの簡略化し、JavaScript ライブラリと Windows アプリケーション、Windows Phone 8、および Microsoft Silverlight 用の.NET Framework 4 のライブラリが含まれています、クライアント側オブジェクト モデル (CSOM) を追加します。 CSOM はオンラインのプロジェクトの開発用に設計され、も設置した Project Server インストール機能します。 

Project Server データベースを結合して 1 つのデータベースにOData サービスをオンラインのレポート テーブルおよびビューにアクセスできます。 CSOM と OData サービスには、主要な状態を転送 (REST) インターフェイスが含まれます。 プロジェクト サーバーのワークフローは、SharePoint Designer 2013 を使用して作成できます。 プロジェクト 2013 の本格的なは、Project Server の作業ウィンドウに Office のアドインの機能拡張モデルを使用して、データ、SharePoint タスク リスト、およびその他の外部コンテンツをレポートに統合できます。 プロジェクト標準 2013 は、タスク ウィンドウ - アドインを使用して、一般的な外部コンテンツとの統合します。
  
図および Project Server 2013 の主な変更点の詳細については、 [Project Server 2013 のアーキテクチャ](project-server-2013-architecture.md)を参照してください。
  
> [!NOTE]
> Project Server 2013 は、プラットフォーム上に構築、SharePoint Server 2013、および Project 2013 には、他の Office 2013 アプリケーションとインフラストラクチャの大部分が含まれています。 モデルのドキュメントを SharePoint のアドイン、SharePoint ベースのワークフローでは、Web パーツ、その他の SharePoint の機能、および Office アドインのドキュメントを使用して開発を参照してください[SharePoint アドイン](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins)、 [Office アドイン](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins)、および SharePoint の[2013 開発の概要](https://msdn.microsoft.com/library/jj164084%28office.15%29.aspx)。 
  
## <a name="major-new-features-in-project-2013"></a>Project 2013 の主な新機能
<a name="pj15_WhatsNew_MajorNewFeatures"> </a>

標準 2013 のプロジェクトおよびプロジェクトの評価のための新機能は、ユーザー インターフェイスの改良を他の Office 2013 アプリケーションと一致して、Windows 8、バーンダウンのレポートで Office アート オブジェクトとの統合で、現代のスタイルのユーザー インターフェイスをサポートしています。レポート、およびレポート用の新しいプログラミング機能。 プロジェクト評価のため有効に共有して、作業ウィンドウのアドインも、Word、Excel、Outlook などの他の Office 2013 アプリケーションで実装されていると、SharePoint Server 2013 では、上のプロジェクトを同期するにはより多くします。
  
Project Server 2013 では、多くの新機能があります。 Project Web App で新しいタイムラインなどのプログラミングの主要なストーリーでは、いくつかはありません。 Microsoft Office オンラインの製品ヘルプとエンド ・ ユーザー マニュアルに、管理者および Microsoft TechNet の IT プロフェッショナル向けのトピックでそれらの機能を文書化します。 他の新機能、強化されたタイムシートなど簡単にタイムシートと状態管理のプロジェクト Server インターフェイス (PSI) をやり取りするサード パーティの開発者。
  
プロジェクトをオンラインで、Office ストアの追加 (https://office.microsoft.com/store)プロジェクトのアドインは、広範囲に及ぶ変更が、Project Server は、Microsoft Azure を使用してアクセスします。 Project Server へのクラウド ・ ベースのアクセスは、Microsoft.NET Framework、Microsoft Silverlight、Windows Phone では、JavaScript を使用する web アプリケーションとアドインを開発するため、クライアント側オブジェクト モデル (CSOM) を使用します。 オンライン プロジェクトの要件は、以前のバージョンの 4 つの Project Server データベースを 1 つのデータベースにマージされることです。
  
タスクの状態、タイムシート、プロジェクト管理などの多くの領域では、Project Server 2013 のパフォーマンスとスケーラビリティが向上します。 Windows Workflow Foundation (WF4) のバージョン 4 では、プロジェクトのサーバーのワークフローが再設計します。 .NET Framework 4 および PSI のように、Windows Communication Foundation (WCF) の使用には、セキュリティ、パフォーマンス、および拡張性が向上します。 たとえば、アプリケーション コードを変更または再コンパイルすることがなく、構成ファイルを使用して WCF ベースのアプリケーションの転送プロトコルを変更できます。 Project Web App では、データが大幅に変更されない、PSI の呼び出しの多くをキャッシュします。
  
> [!NOTE]
> Project Server 2013 の開発のため、Office および SharePoint ツールの拡張機能、ネイティブ Office 2013 製品用のアドインを作成すると Visual Studio を使用できます。 Project Server 2013 には、Visual Studio のプロジェクト詳細ページと WCF ベースのアプリケーションなどの機能の開発を有効にする必要があります。 Visual Studio で SharePoint ツールの拡張機能では、Project Web App およびその他の SharePoint サイトに直接 Web パーツおよびその他の SharePoint の機能を展開できます。 
>
> Visual Studio はユーザー設定フィールド、ステージ、フェーズ、および管理するのには、Project Web App のエンタープライズ プロジェクトの種類を使用して Project Server ワークフローを作成する必要なくなりました。 ワークフローを作成する Visual Studio を使用できますが頻繁にありますが簡単かつ速く SharePoint デザイナーを使用して作成します。 CSOM またはその他の外部 Api へのアクセスを必要とするワークフローでは、Visual Studio を使用できます。 
  
### <a name="project-add-ins"></a>Project アドイン
<a name="pj15_WhatsNew_Apps"> </a>

配布とソフトウェアのマーケティング革命的に変わりましたとアドインの概念です。 Project 2013 では、アドインを Office のパブリック ストアから購入し、ダウンロードできるようになりましたや SharePoint 上のプライベート カタログ内で配布することができます。 アドインは通常自己完結型、対話型のプログラムで、少数の関連するタスクを実行します。 プロジェクトの追加には、標準 2013 のプロジェクトまたはプロジェクトの標準的な 2013 のクライアントの作業ウィンドウ アドインまたは Project Server 2013 またはプロジェクトをオンラインで。
  
プロジェクトのデスクトップ クライアント用のアドインについては、[タスク ペインでアドイン プロジェクト](#pj15_WhatsNew_Agave)を参照してください。 Project Server 2013 の例では、 [Project Server の SharePoint によってホストされる作成アドインを](create-a-sharepoint-hosted-project-server-add-in.md)参照してください。 [Office および SharePoint アドイン SDK](https://msdn.microsoft.com/library/fp161507.aspx)の記事、[ブログの Office](https://blogs.office.com/dev/) Project 2013 とオンラインのプロジェクトに関連するも多くの投稿にあります。 
  
Project Server 2013 のでは、オンプレミスのインストールとオンライン プロジェクトを操作できます。 プロジェクト サーバーのアドインには、Web パーツ、リモート イベント レシーバー、およびビジネス ロジックを含めることができます。 追加の Project Server のオブジェクト モデルへのアクセスでは、CSOM、PSI ではない、です。 データ記憶域は、クラウド ・ ベースなど、SQL Azure の外部などを通じて Microsoft Business Connectivity Services (BCS)、ローカル データベースの内部で、または混合できます。
  
#### <a name="add-in-security"></a>アドインのセキュリティ

。 アドインを実行しているユーザーの代理としてアドインを実行するアクションを実行する一般的に、明示的に、偽装を使用して、アドインを実行できるユーザーを指定したりしないでください。 アクションには、アドインを実行しているユーザーのアクセス許可レベルを超えることはできません。 
  
Visual Studio 2012 ののための Office 開発ツール、AppManifext.xml ファイルがグラフィカル ・ エディターのアクセス許可要求のスコープを設定することができます。 などの**AppManifest.xml**デザイナー ウィンドウの [**アクセス許可**] タブで、プロジェクトを更新するプロジェクト マネージャーを有効にするアドインを作成する**複数のプロジェクト**の選択、スコープと [**書き込み**アクセス許可のします。 アドインをユーザーにプロジェクト マネージャーのアクセス許可がある場合は、彼女を彼女を管理するプロジェクトのアドインを実行できます。 AppManifest.xml ファイル内のコードは以下に示します。 
  
```XML
  <AppPermissionRequests>
    <AppPermissionRequest Scope="https://sharepoint/projectserver/projects" Right="Write" />
  </AppPermissionRequests>
```

**表 1. Project Server アドイン用のアクセス許可リクエストのスコープ**

|スコープ|アクセス許可|
|:-----|:-----|
|**Project Server** <br/> |**管理** (Project Server 管理者のアクセス許可が必要)  <br/> |
|**複数のプロジェクト ** <br/> |**読み取り**、**書き込み** (一部の操作にはプロジェクト マネージャーのアクセス許可が必要となり、タスクの割り当てなどの基本の読み取り操作にはプロジェクト チーム メンバーのアクセス許可が必要となります。)  <br/> |
|**1 つのプロジェクト ** <br/> |**読み取り**、**書き込み** (少なくともプロジェクト チーム メンバーのアクセス許可が必要。プロジェクト内のデータにアクセスできるかどうかは、他のアクセス許可レベルに依存します。)  <br/> |
|**エンタープライズ リソース** <br/> |**読み取り**、**書き込み** (リソース マネージャーのアクセス許可が必要)  <br/> |
|**状態管理** <br/> |**提出ステータス** (プロジェクトの状態を送信するためのアクセス許可が必要)  <br/> |
|**レポート** <br/> |**読み取り** (Project Server にログオンするためのアクセス許可が必要)  <br/> |
|**ワークフロー** <br/> |**昇格** (ワークフローを実行するためのアクセス許可が必要。ワークフローでのステージ間の移行を可能にするために、アドインは管理者特権で実行されます。ステージ遷移はアドイン内のビジネス ロジックによって制御されます。)<br/> |
   
> [!NOTE]
> Project Server 2013 とオンライン プロジェクトは、SharePoint 2013 の ( [SharePoint 2013 で追加の認証ポリシー型](https://msdn.microsoft.com/library/124879c7-a746-4c10-96a7-da76ad5327f0%28Office.15%29.aspx)を参照してください) のアプリケーション専用の認証モデルを使わないでください。 
  
開発方法の詳細については、配布する、ホスト、およびアドインを管理するを参照してください[SharePoint のアドイン](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins)と[Office アドイン](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins)、および SharePoint Server 2013 と Office 2013 の開発者向けドキュメントに関連するトピックです。 アクセス許可要求スコープの他の SharePoint のアドインについては、 [SharePoint 2013 で追加のアクセス許可](https://msdn.microsoft.com/library/5f7a8440-3c09-4cf8-83ec-c236bfa2d6c4%28Office.15%29.aspx)を参照してください。
  
### <a name="integrating-with-sharepoint-server"></a>SharePoint Server との統合
<a name="pj15_WhatsNew_IntegrationWSS"> </a>

Project Web App で多くの機能は、SharePoint Server 2013 OAuth とクレーム ベース認証、サーバーのプロジェクトの承認および SharePoint グループを使用してアクセス許可などの SharePoint のタスクとプロジェクトの同期の新しいインフラストラクチャを必要とします。リスト、および Project Server の宣言型ワークフローです。 プロジェクト サービス アプリケーションは、SharePoint ファーム内のすべてのサイト コレクションに関連付けることができます。 プロジェクトの同期は、SharePoint タスク リストでは、SharePoint プロジェクトを保持しています。 エンタープライズ プロジェクトは、Project Server がフル コントロールを保持して、SharePoint タスク リストとも同期できます。 アーキテクチャ ダイアグラムとプロジェクトの同期の詳細については、 [Project Server 2013 のアーキテクチャ](project-server-2013-architecture.md)を参照してください。
  
SharePoint Server 2013 では、多くの新機能があります。 詳細については、[開発者向けの SharePoint](https://msdn.microsoft.com/sharepoint)を参照してください。
  
### <a name="integrating-with-workflows"></a>ワークフローとの統合
<a name="pj15_WhatsNew_Workflow"> </a>

ワークフローはプロジェクト ポートフォリオ管理のコア機能です。プロジェクトのライフ サイクルには、多くのフェーズにまたがる長期間のプロセスを含めることができます。ガバナンス フェーズには、プロジェクトの提案、ビジネスへの影響度の分析、およびプロジェクトの選択、作成、計画、管理、追跡が含まれます。
  
WF4 を使用して、SharePoint 2013 ワークフロー プラットフォームでは、Project Server 2013 のワークフローが組み込まれています。 異なり以前のバージョンでは、Project Server 2013 の宣言型ワークフロー SharePoint Designer 2013 を使用して作成することができますはオンプレミスとオンラインの両方にアクセスできるようにします。 プロジェクト サーバーのワークフローでは、SharePoint ワークフローのセキュリティ モデルを使用して、OAuth を使用と、Project Web App サイトにインストールすることができます。 図 1 は、SharePoint Designer 2013 が需要の管理、各ステージが Project Web App で定義されているため、サイトのワークフローにステージを追加できることを示しています。
  
**図 1. SharePoint Designer を使用した Project Web アプリ用ワークフローへのステージの追加**

![SPD 内のワークフローにステージを追加します。](media/pj15_CreateWorkflowSPD_AddStageInSPD.gif "SPD 内のワークフローにステージを追加します。")

<br/>

宣言型ワークフローを構築するには、デザイン ツールで、SharePoint Designer 2013 または Visual Studio 2012 のいずれかのワークフロー ステージ、アクション、条件、およびその他の要素を追加します。 デザイン ツールは、実行時に解釈されますが、XAML のコードと、ワークフローを保存します。 宣言型ワークフローは、Project Server 2013 の設置またはプロジェクトをオンラインで実行できます。 Visual Studio 2012 を使用すると、またカスタム アクションは、追加のコントロールのフォームを作成し、複数の Project Web App インスタンスを再利用するためのワークフロー テンプレートを保存できます。 SharePoint Designer 2013 には、Visual Studio 2012 で作成されたカスタム アクションを使用できます。
  
Project Server 2013 のワークフローを果たし、アプリケーション、管理者は、Project Web App のデザイン権限を持つ-宣言型ワークフローを発行し、エンタープライズ プロジェクトの種類 (EPT) に関連付けることができます。 EPT では、エンタープライズ プロジェクトの Project Server がフル コントロールを保持する場所があります。 SharePoint タスク リストでは、Project Server ワークフローを使用することはできません。 
  
OAuth では、プロジェクト マネージャーは偽装を使用せずにワークフローを起動するには、プロジェクト作成の権限が有効にします。 例に従って、分岐を決定するユーザー設定フィールドの値を読み取るための Project server では、ワークフローの呼び出しは、プロジェクト マネージャーのために行われます。 プロジェクト マネージャーが自動的に次の段階へと進化するワークフローを作成することを防ぐには、次のワークフロー ステージに移動するための呼び出しは、ワークフローの作成者 (管理者) として実行されます。 対照的に、従来の Project Server 2010 のワークフローのユーザーは、ワークフロー全体を通して管理者のアクセス権を得るためにワークフロー プロキシ ユーザー アカウントを偽装の電話をかけます。
  
Project Server 2013 の設置には、コンパイル済みの WF3.5 ベースのワークフローを使用できますが、WF4 に基づく宣言型のワークフローには、従来のワークフローをアップグレードすることをお勧めします。 新しいテクノロジーよりスケーラブルで信頼性の高いです。 ビジネス アナリストおよび PMO スタッフ作成または Visio 2013 を使用して、ワークフローの設計を更新して SharePoint Designer 2013 を使用してコーディングせずに Project Server のワークフローを実装します。
  
Project Web App の宣言型ワークフローを作成する方法の詳細については、 [Project Server のワークフローの開発を開始する](getting-started-developing-project-server-workflows.md)を参照してください。 SharePoint デザイナーとワークフローを Visual Studio の機能の比較とは、 [Visual Studio を使用して SharePoint 2013 の開発のワークフロー](https://msdn.microsoft.com/library/office/jj163199.aspx)を参照してください。
  
### <a name="client-side-object-model"></a>クライアント側オブジェクト モデル
<a name="pj15_WhatsNew_CSOM"> </a>

オンライン プロジェクトにプログラムでアクセスには、SharePoint の CSOM に組み込まれている CSOM が必要です。 プロジェクトのオンライン認証は、Windows Live ID、プロジェクトのサーバーのフォーム認証ではない、または Windows 認証を使用して OAuth になります。
  
以下は、原則と Project Server 2013 で CSOM の機能です。
  
- CSOM は、使いやすさを設計されています。 メソッドとプロパティを直接使用など、名、Guid、 _changeXml_パラメーターの数を必要とするではなくまたはデータセットを渡すことによってデータを提供します。 
    
- Project Server の CSOM はサードパーティのソリューションの一般的な要件に基づいて PSI 機能のサブセットを実装します。
    
- CSOM は PSI を内部的に呼び出しますが、その構造は変わったものになっています。たとえば、すべての状態変更の更新が **StatusAssignmentCollection.SubmitAllStatusUpdates** メソッドを使用して行われるようになっており、ユーザーについては PSI メソッドの **Statusing.SubmitStatus** を使用し、その他のリソースについては **SubmitStatusForResource** メソッドを使用する、というようにはなっていません。 
    
- PSI の 22 個のパブリック サービスを使用しなくても、1 つの WCF サービス (Client.svc) で CSOM に アクセスできます。
    
- プロジェクトのサーバー CSOM の初期化は、Project Web App の URL を使用して[ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx)クラスを使用して直接 WCF 参照またはプロキシのアセンブリを使用しています。 
    
- CSOM は、内部 SharePoint CSOM インフラストラクチャでサポートされる複数のクライアント ライブラリおよびインターフェイスを実装します。クライアント ライブラリおよびインターフェイスには次のものが含まれます。
    
  - Microsoft.ProjectServer.Client.dll アセンブリ内の Microsoft .NET クライアント ライブラリ
    
  - Microsoft.ProjectServer.Client.Silverlight.dll アセンブリ内の Silverlight ライブラリ
    
  - Microsoft.ProjectServer.Client.Phone.dll アセンブリ内の Windows Phone 8 ライブラリ
    
  - PS.js ファイルまたは PS.debug.js ファイル内の web アプリケーション用の JavaScript ライブラリ
    
  - OData プロトコルを使用してアクセスするための REST エンドポイント
    
  - フィルター処理によって返されるデータ量を制限できる LINQ クエリのネイティブ サポート
    
- プロジェクト オンライン ソリューションと PSI や Microsoft.Office.Project.Server.Library.dll などの他の Project Server アセンブリとは別に、オンプレミスのソリューションの両方は、CSOM を使用できます。
    
- 累積的な更新と service pack、Project Server のパートナーからの要求と開発者コミュニティに基づく Project Server 2013 の CSOM の追加機能を考慮することがあります。
    
> [!NOTE]
> CSOM はサードパーティの Project Server 開発者にお勧めのインターフェイスです。新しいアプリケーションを開発する際に、対象アプリケーションに必要な機能が CSOM に含まれている場合には、CSOM を使用することをお勧めします。 
  
CSOM を使用した開発方法の詳細については、 [Project 2013 のクライアント側オブジェクト モデル (CSOM)](client-side-object-model-csom-for-project-2013.md)を参照してください。 SharePoint アプリケーションの残りの部分インターフェイスの詳細については、SharePoint 2013 の開発者向けドキュメントに*SharePoint の REST サービスを使用してプログラミング*を参照してください。 
  
### <a name="changes-in-the-reporting-database"></a>レポート データベースの変更点
<a name="pj15_WhatsNew_RDBChanges"> </a>

Project Server 2010 の 4 つのデータベースは、Project Server 2013 の 1 つのプロジェクト データベースに結合されます。 プロジェクト データベースの既定の名前は、ProjectService です。 テーブルとビューは、前の名前を保持して、下書き、発行済み、およびアーカイブ データベースからテーブルとビューの接頭番号を報告する`draft`、 `pub`、および`ver`ProjectService データベースにします。 たとえば、プロジェクトのパブリッシュされたテーブルは、pub です。MSP_PROJECTS。 
  
> [!IMPORTANT]
> 直接のアクセスが、ドラフトではサポートされていません (`draft`プレフィックス)、公開されている (`pub`)、およびアーカイブ (`ver`) テーブルとビューです。 のみ、レポート テーブルおよびビューを持つレポートを使用する必要があります、`dbo`のプレフィックスです。 たとえば、dbo です。MSP_EpmProject テーブルには、Project Web App インスタンス内のプロジェクトの一覧が含まれています。 
>
> Project データベースのテーブルおよびビューには、プログラムによってデータベースに直接アクセスしてデータを更新することを能動的に妨げるものは存在しません。Project Professional キャッシュ、下書きおよび発行済みデータ テーブル、およびレポート テーブルはすべてがキャッシュ同期プロトコルに依存しているので、直接データを編集すると同期が混乱する可能性があることに注意が必要です。直接アクセスしてデータを変更することによって、Project Server データベースや Project Professional クライアント側キャッシュが破損した場合、製品サポートは役に立てません。 
  
Project Server 2013 の OData サービスをオンラインに導入、設置型のアクセス。 オンラインのレポート テーブルおよびビューが、OData インターフェイスだけが公開されています。設置型で使用するため、odata を使用したり、レポートのテーブルと SharePoint ファーム内の ProjectService データベース内のビューに直接アクセスできます。 プロジェクトのオンラインでは、マルチ テナント データベースをサポートしていません。 それぞれの Project Web App の複数のインスタンスでは、独自のプロジェクトのデータベースがあります。 OData サービスは内部的にレポート テーブルおよびビュー、SQL クエリを実行し、XML または JSON ペイロードを提供します。 **ProjectData**スキーマの参照、Project Server 2013 に報告するために、OData サービスの概要については、 [ProjectData - プロジェクトの OData サービスの参照](https://msdn.microsoft.com/library/office/jj163015.aspx)を参照してください。
  
OData クエリに関する一般的な情報を参照してください[OData: URI 規則](https://www.odata.org/documentation/)。 たとえば、Project Web App のブラウザーで次のクエリを使用してプロジェクト名を"Test"で始まる場所の設置型のインスタンス内のプロジェクトのすべてを表示できます。 ブラウザーのページ内を右クリックし、**ソースの表示**] をクリックします。
  
```html
https://ServerName /ProjectServerName /_api/ProjectData/Projects?$filter=startswith(ProjectName, 'Test') eq true
```

Excel 2013 では、[PowerPivot に [データ] リボンのプロジェクト データをインポートするには、**その他のソースから**のドロップ ダウン メニューで**OData からのデータ フィード**を選択します。 [**データ接続ウィザード**ダイアログ ボックスで、https://ServerName/ProjectServerName/_api/ProjectData/データの場所のフィード**次へ**を選択し、ウィザードの [**テーブルの選択**] ページで、**プロジェクト**のテーブルを選択します。 名前および .odc ファイルを保存し、[**完了**] を選択します。 **データのインポート**] ダイアログ ボックスで、**ピボット テーブル レポート**を選択します。 Excel のワークシート上のピボット テーブルの行と列を表示するフィールドを選択します。
  
適切なアクセス許可を持つ、オンプレミス Project Server ユーザーは、直接アクセスできますレポート テーブルおよびビュー、レポートを作成するのには、Microsoft SQL Server から Project Server 2010 のように。 Project Server 2013 では、[ユーザーは OData インターフェイスを通じてレポートのテーブルをアクセス、オンプレミスでこともできます。 Project Server データをオンラインまたはオンプレミス OData サービスの REST エンドポイントを通じて取得できます。 たとえば、dbo です。MSP_PROJECT テーブル dbo.MSP_EpmProject_UserView ビューは、レポートに使用できます。 すべてのテーブルまたはビューを持つ、 `draft`、 `pub`、または`ver`プレフィックスは、Project Server によって内部使用のみ、および使用を報告するためではありません。 たとえば、下書きです。MSP_TASKS テーブル、pub.MSP_PROJECTS_WORKING_VIEW ビューでは、文書化されていないと、内部でのみ使用されます。 
  
> [!NOTE]
> オンプレミス レポートは、別のデータベース内のテーブル、ビュー、フィールド、およびストアド プロシージャを追加して拡張できます。Project Server データベース内の既存のレポート テーブルやレポート ビューは変更しないでください。 
  
レポートのテーブル、ビュー、およびプロジェクト データベース内のフィールドは、Project 2013 SDK ダウンロードの後で、更新プログラムで HTML ヘルプ ファイルに記載します。 **ProjectData**サービスの OData の XML スキーマのドキュメントについては、 [ProjectData - プロジェクトの OData サービスの参照](https://msdn.microsoft.com/library/office/jj163015.aspx)を参照してください。 レポートのテーブルと Project Server 2010 用に作成されたビューのクエリは、ほとんどの場合、データベースと連動プロジェクト Project Server 2013 にします。 ように現在、オンプレミスのユーザーは SQL Server Analysis Services では、[Project Server OLAP キューブにアクセスできます。 オンラインのプロジェクトの OLAP キューブでは使用できません。
  
### <a name="task-pane-add-ins-in-project"></a>Project の作業ウィンドウ アドイン
<a name="pj15_WhatsNew_Agave"> </a>

標準 2013 のプロジェクトとプロジェクトの評価のための両方は、作業ウィンドウのアドインと統合し、web ページ内の外部コンテンツを表示するに使用できるをサポートします。 作業ウィンドウには、javascript のタスク、リソース、ビュー、および一般的なプロジェクト データにアクセスを許可された web ページ コンテンツが表示されます。 プロジェクトの JavaScript オブジェクト モデルは、選択したタスクまたはリソースに関する情報を取得することができ、ガント チャート] ビューなどのビューのグリッドで選択したセルにデータを取得できます。 作業ウィンドウ用のアドイン プロジェクトはタスク、リソース、イベント ハンドラーを実装したり、選択変更イベントを表示できます。 
  
**こんにちは ProjectData**タスク ペインを追加で**ProjectData**サービスのクエリを実行し、すべてのプロジェクトの平均値と現在のプロジェクト内のデータを比較し、図 2 を示しています。 Project 2013 SDK ダウンロードには、アドインの完全なソース コードが含まれています。 
  
**図 2. Project Professional 内の作業ウィンドウ アドインは Project Server 内のデータにアクセスできる**

![現在のプロジェクトのすべてのプロジェクトとの比較](media/pj15_RestQueryApp_CompareProject.gif "現在のプロジェクトのすべてのプロジェクトとの比較")
  
> [!NOTE]
> プロジェクト 2013 の標準は、作業ウィンドウ - アドインを Project Server 2013 に直接統合できません。 
  
タスク ペインでアドイン プロジェクトの担当者には、Project Web App と Project Professional の両方を実行すると、開発者が拡張機能を構築できますので、Project Server 2013 では、用に構築された Web パーツをサポートできます。 全般的なタスク ペインのアドインが、他の Office 2013 製品の開発は、プロジェクトの標準的な 2013 と評価のためのプロジェクトにも使用できます。 詳細については、[作業ウィンドウ用のアドイン プロジェクト](task-pane-add-ins-for-project.md)を参照してください。
  
### <a name="project-server-event-receivers"></a>Project Server イベント レシーバー
<a name="pj15_WhatsNew_Events"> </a>

バックエンド プロジェクト サービス アプリケーションを含む SharePoint ファームに複数の Project Web App サーバー (フロント エンドの web サーバー、または WFEs とも呼ばれます) があります。 イベント レシーバーは、イベント ハンドラーをということができます。 ローカル イベント ハンドラーは、完全信頼のコードを使用して実装し、すべて Project Server のローカル インストール用の WFEs の上に展開できます。 リモート イベント レシーバーをローカル サーバーまたはリモート サーバー上の web サービスに実装されているし、複数の WFEs と Project Server の複数のインストールにアクセスできます。 プロジェクトのオンラインでは、リモート イベント レシーバーのみを使用できます。
  
プロジェクトのサーバー イベント ハンドラーは、特定の Project Web App の設定ページではなく、Project Web App インスタンスごとに SharePoint で管理されます。 SharePoint サーバーの全体管理アプリケーションで、**アプリケーションの全般的な設定**を選択、 **PWA の設定**、[**管理**] を選択および設定の PWA **Project Web App インスタンス**のドロップダウン リストで、インスタンスを選択ページです。 ローカル イベント ハンドラーまたはリモート イベント レシーバーを追加するには、**サーバー側のイベント ハンドラー**を選択します。
  
、プロジェクトのサーバーの設置型インストールの、CSOM で[Microsoft.ProjectServer.Client.EventHandlerCreationInformation](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCreationInformation.aspx)クラスを使用する SharePoint 機能として、リモート イベント レシーバーを作成および管理プログラムを使用して、[EventHandlerCollection](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCollection.aspx)クラスでメソッドを使用してイベント レシーバーです。 リモート イベント レシーバーの前のイベントは、同期後のイベントは、非同期で、リモート イベント レシーバーが返さない場合にタイムアウトが設定されています。 
  
> [!NOTE]
> SharePoint サーバーの全体管理は、オンプレミスのインストールでのみ使用可能です。 オンライン プロジェクトと SharePoint Online は、追加したり、CSOM ベースのアプリケーション パッケージを使用してリモート イベント レシーバーを削除します。 
  
設置 Project Server インストール用のローカルのイベント ハンドラーを追加するプロセスではサーバー側のイベント ハンドラー] ページで、Project Server の[プロジェクトのサーバー イベント ハンドラーを作成しイベントをログ出力](https://msdn.microsoft.com/library/gg615466.aspx)のトピックで説明したプロセスとほぼ同じ2010。 違いは、イベント ハンドラーを新しいページに追加のオプションがあります。 などの**イベント**の一覧で**プロジェクトを作成する**」を選択し、**新しいイベント ハンドラー**を選択し。 [新しいイベント ハンドラー] ページで 2 つだけ必要なフィールド**名**と**注文**(図 3 を参照してください)。 ローカルの完全信頼のイベント ハンドラーを追加する場合、[**アセンブリ名**] フィールドと、**クラス名**] フィールドを追加します。**エンドポイントの Url**は空のままにします。 リモート イベント レシーバーを追加する場合は、**エンドポイントの Url**を追加し、**アセンブリ名**と**クラス名**を空のままにします。 
  
> [!CAUTION]
> Project Server がローカル (設置型) のみを呼び出す場合は、アセンブリ名とクラス名、およびエンドポイントの URL に*両方*を指定するイベント ハンドラーです。 リモート イベント レシーバーは無視されます。 
> 
> 同じイベントに 2 つのイベント ハンドラー (一方のイベント ハンドラーがローカルで、もう一方がリモート イベント レシーバー) を作成する場合、**[Order]** の値が両方とも同じであれば、Project Server はリモート イベント レシーバーを無視します。 
  
**図 3. ローカル イベント ハンドラーまたはリモート イベント レシーバーの追加**

![イベント ハンドラーまたはイベントの受信機を構成します。](media/pj15_EventHandlers_NewEventHandler.gif "イベント ハンドラーまたはイベントの受信機を構成します。")
    
Microsoft.Office.Project.Schema.dll アセンブリをコピーするにはローカル イベント ハンドラーの PSI のデータセットへのアクセスを必要とする場合、[Windows]\Microsoft.NET\assembly\GAC\_MSIL\Microsoft.Office.Project.Schema\v4.0_15.0.0.0__71e9bce111e9429c ディレクトリです。 

、PSI の代わりにお勧め**Microsoft.ProjectServer.Client**名前空間内のイベント クラスを使用することCSOM を使用して開発には、データセットの操作は不要です。 プロジェクト オンラインのリモート イベント レシーバーを開発するのには、CSOM で[イベント](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.Event.aspx)クラスと[EventHandlerCreationInformation](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCreationInformation.aspx)クラスを使用してください。 
  
Project Server イベント ハンドラーを展開する前にインストールし、Project Server のテスト環境で徹底的にイベント ハンドラーをテストします。 設置プロジェクトのサーバー インストールの場合は、ローカル イベント ハンドラーを追加することになると動作していない場合、Project Server 2013 のイベント サービスが他の有効なカスタム イベント ハンドラーの読み込みに失敗します。 その場合は、問題のイベント ハンドラーを削除し、イベント サービスを再起動してください。
  
> [!NOTE]
> オンプレミスの Project Server インストールでイベント レシーバーを開発するには、CSOM を使用してリモート イベント レシーバーに移行することをお勧めします。リモート イベント レシーバーには Project Server Events Service 内で実行するサードパーティのコードが存在しないため、リモート イベント レシーバーの方が安定しています。ローカル管理者は、Project Server Events Service のメンテナンスを行う責任が軽減されます。 
  
イベントに関する一般情報は、 [SharePoint のアプリケーションでイベントを処理する](https://msdn.microsoft.com/library/jj220048%28office.15%29.aspx)を参照してください。 
  
## <a name="deprecated-features"></a>非推奨になった機能
<a name="pj15_WhatsNew_Deprecated"> </a>

> [!NOTE]
> 機能とプロジェクト サーバー 2016 のプレビューでは削除または廃止されている Api の詳細については、[プロジェクト サーバー 2016 のプレビューでは削除または廃止について](https://technet.microsoft.com/library/mt422816%28v=office.16%29.aspx)を参照してください。 
  
非推奨の機能は、いくつかのソリューションでは、Project 2013 で引き続き使用しますが、新たに開発には使用する必要があります。 プロジェクトがオンライン、または SharePoint アクセス許可モードで Project Server 2013 の既定のオンプレミスのインストールと、次の機能と手法のほとんどは動作しません。 Project Server 2013 に Project Server 2010 のアップグレードのこれらの機能を使用する既存のソリューションは使用できません。 使用するソリューションが推奨されない機能は、場合によっては作業を続けることがありますが、Project 2013 のすべてのインストールを完全にサポートされていません。
  
ソリューションは、非推奨の機能を使用する場合、展開する前に徹底的にテストする必要があり、必要がありますを変更することとしてすぐに使用がサポートされている機能としては実用的では。 プロジェクトのアクセス許可モードの設置型の Project Server 2013 のセキュリティの構成方法の詳細については、 [Project Server 2013 の IT プロフェッショナル向けの新規](https://technet.microsoft.com/en-us/library/ff631142%28office.15%29.aspx)の*SharePoint アクセス許可モード*を参照してください。
  
- **拡張機能**[PSI 拡張機能のシナリオ](https://msdn.microsoft.com/library/office/ff843378%28v=office.14%29.aspx)は推奨されていませんし、将来のリリースではサポートされません。 設置 Project Server 2013 のシナリオでは、カスタムの Windows Communication Foundation (WCF) サービスを使用して統合が有効になります。 
  
- **プロジェクト PSI**PSI の[プロジェクトのクラス](https://docs.microsoft.com/office/client-developer/project/project-psi-reference-overview)の使用は推奨されていません。 すべての新しい開発[プロジェクトの CSOM](client-side-object-model-csom-for-project-2013.md)を使用します。 プロジェクトの PSI を使用して Project Server 2013 のアプリケーションは引き続き動作が、プロジェクトのオンライン アプリケーションは CSOM と同じメソッドにすべてのプロジェクト クラスの PSI メソッドを置換する必要があります。
  
- **リソース計画の PSI**[リソース計画の PSI](https://msdn.microsoft.com/library/office/websvcresourceplan_di_pj14mref.aspx)の使用は推奨されていません。 Project 2013 の開発をサポートするのに続行されますが、将来のリリースではサポートされません。 
  
- **PSI の ASMX インターフェイス**PSI には、設置型のプロジェクトのサーバー拡張機能を開発するために重複するインターフェイスが含まれています。 ASMX web サービス インターフェイスは、Office Project Server 2007 で PSI の最初の実装で導入されました。 Project Server 2010 には、オブジェクト モデルが本質的には、ASMX web サービスを複製、WCF サービスのインターフェイスが追加されます。 ASMX と WCF の両方をサポートするために Project Server 2013 は続いていますが、PSI を必要とする新しいソリューションでは、WCF サービスを使用してください。 可能であれば、新しいソリューション、CSOM を使用して記述する必要があります。 
  
  PSI の ASMX web サービスは、Project Server 2013 で廃止されました。 Project Server のバージョンでは将来的に、WCF サービスまたは、CSOM を使用する ASMX web サービスを使用するソリューションを書き直す必要があります。 詳細については、 [Project Server プログラミング](project-server-programmability.md)する*プロジェクトのサーバー Api を使用してアプリケーションをアップグレードする*」を参照してください。
  
- **オブジェクト リンク プロバイダー (OLP)** Project Server の以前のバージョンで、PSI の**ObjectLinkProvider**サービスにはエンタープライズ プロジェクトのタスクとプロジェクトのサイトで専用の SharePoint リストとの間の web オブジェクトのリンクを管理する方法も用意されています ( [WebSvcObjectLinkProvider](https://msdn.microsoft.com/library/WebSvcObjectLinkProvider.aspx)を参照してください)懸案事項、リスク、成果物、およびドキュメントです。 Project Server 2013 で、OLP は使用されなくなりました。 
  
  クラスを使用して**[RelatedItemManager](https://msdn.microsoft.com/library/microsoft.sharepoint.client.relateditemmanager.aspx)** SharePoint CSOM で作成、読み取り、[タスク] リスト内の項目とプロジェクトのサイト内の他のリストとの間の web オブジェクトのリンクを削除できます。 たとえば、懸案事項作業項目からリンクを追加するに、 **[AddSingleLink](https://msdn.microsoft.com/library/office/microsoft.sharepoint.client.relateditemmanager.addsinglelink.aspx)** メソッドまたは**AddSingleLinkFromUrl**または**AddSingleLinkToUrl**、2 つのような方法のいずれかを使用できます。 **RelatedItemManager**クラスには、web オブジェクトのリンクを削除して、関連アイテムを読み取るのためのメソッドも含まれています。 JSOM (JavaScript オブジェクト モデル) に相当するクラスを参照してください[。RelatedItemManager オブジェクト (sp.js)](https://msdn.microsoft.com/library/jj838582.aspx)。
  
  OLP 型アプリケーションの Project Server 2013 の設置型インストールとオンライン プロジェクトを作成する SharePoint CSOM を使用することをお勧めします。 ["Microsoft.sharepoint"](https://msdn.microsoft.com/library/microsoft.sharepoint.aspx)の名前空間では、 **RelatedItemManager**は含まれません。 クラスです。 
  
- **カスタムのアクセス許可**Project Server の特定の機能や拡張機能にアクセスするためのカスタム セキュリティ アクセス許可は、SDK の資料が発行済みデータベースを直接変更することによってそれらを作成する方法を説明して、Office Project Server 2007 でサポートされていました。 Project Server 2010 でカスタムのアクセス許可も動作しますが推奨されていません。 Project Server 2013 では、[カスタムのアクセス許可は設置用の既定の SharePoint アクセス許可モードでは動作しません。 プロジェクトのアクセス許可モードは、カスタム アクセス許可がサポートされています。 Project online では、データベースに直接アクセスはできません。 
  
- **偽装**Project Server 2013 の PSI ベースのアプリケーションで偽装アプリのユーザーが、別の Project Server ユーザーのセキュリティのアクセス許可と見なすことが推奨されていません。 以前に指定されている場合既定設置 Project Server 2013 のインストールを使用して、SharePoint アクセス許可モードは、Project Server のセキュリティ グループの偽装を許可しません。 詳細については、[認証、承認、および SharePoint 2013 のセキュリティ](https://msdn.microsoft.com/library/ms457529%28office.15%29.aspx)を参照してください。
  
  状態管理アプリケーションは、Project Server の以前のバージョンの偽装を使用した可能性のある一般的な拡張機能です。 Project Server 2010 が**ReadStatusForResource**メソッドと**StatusBrokerPermission**グローバル アクセス許可の読み取りに偽装の必要性を排除するとともに、PSI の**SubmitStatusForResource**メソッドを導入およびほかのユーザーのステータスを更新します。 Project Server 2013 で CSOM は透過的に、状態管理の拡張機能を有効にする基になる PSI を使用しておよびプロジェクトでも、オンプレミスのインストールに使用できます。 
  
- **レポート データベースの拡張機能**追加のカスタム テーブルとビューをレポート データベースには、Project Server の以前のバージョンで一般的な方法です。 Project Server 2013 は、1 つのデータベースに以前のバージョンの 4 つのデータベースを結合、するためのアップグレードは転送されませんカスタム テーブル、ビュー、またはストアド プロシージャ、レポート データベース内のテーブル、Project Server 2013 に。 
  
  使用すること SQL Azure または別の SQL Server データベースのいずれかのカスタム レポートのテーブル、ビュー、データベースのバックアップと更新プログラムを管理することをお勧めします。 プロジェクト オンラインでは、これが必要です。
  
- **レポート**ローカルのレポート テーブルおよびビューでは、Project Server データベース、および OLAP キューブは*廃止、されず、完全にサポートされているままです。* ただし、レポート テーブルおよびビュー (Project Server の以前のバージョンのレポート データベース) はプロジェクトをオンラインでアクセスできるようにします。 同様に、OLAP キューブは、Project Server 2013 のオンプレミスのインストールでのみ利用できます。 プロジェクト オンラインを使用してアプリケーションを報告するには、OData プロトコルを使用して残りのクエリによって、 **ProjectData**サービスを使用できます。 
  
- **プロジェクト ガイド**プロジェクト ガイドは、Office Project 2007 のデスクトップ アプリケーションでの標準的な機能であり、作業ウィンドウの HTML と JavaScript のコンテンツが作成およびプロジェクトを管理するための対話型のガイダンスを提供します。 Project 2010 では、プロジェクト ガイドは、既定のインストールでは使用できませんが、VBA と VSTO アドインを有効にすることができます。 プロジェクト 2010 SDK ダウンロードには、変更後のプロジェクト ガイド ファイルが含まれています。 
  
  VBA オブジェクト モデルと、 **Microsoft.Office.Interop.MSProject**オブジェクト モデルでは、Project 2013 でも、**アプリケーション**クラスと、**プロジェクト**プロジェクト ガイドを管理できるは、22 のメンバーが含まれます。 ただし、Project 2013 の作業ウィンドウのアプリケーションは、プロジェクト ガイドの作業ウィンドウと [プロジェクト ガイドの内容の操作と競合があることはできません簡単に配布または Office ストアで販売します。 Office アドイン、ユーザー設定のプロジェクト ガイドのコンテンツを持つプロジェクトのタスク ペイン ソリューションを開発することを強くお勧めします。 プロジェクト ガイドの詳細については、[プロジェクト 2010 SDK のマニュアル](https://msdn.microsoft.com/library/ms512767.aspx)を参照してください。
  
## <a name="comparing-project-server-on-premises-with-project-online"></a>オンプレミスの Project Server と Project Online との比較
<a name="pj15_WhatsNew_Comparing"> </a>

プロジェクト サーバー設置型またはオンラインのプロジェクトを使用するかどうか、どのような種類の拡張を作成するいずれの場合を決定するために、表 2 のオンライン プロジェクトを Project Server 2013 の設置型インストールの拡張機能を比較します。 表 2 では、展開、管理、または使用法の相違点は含まれません。 オンライン プロジェクトと Project Server 2013 の詳細については、 [Project 2013 の開発者](https://msdn.microsoft.com/office/fp161502)と[オンライン プロジェクト](https://developer.microsoft.com/en-us/project)を参照してください。
  
**表 2. オンプレミスの Project Server と Project Online の拡張性**

| 機能 |オンプレミスの Project Server | Project Online |
|:-----|:-----|:-----|
|**プログラミング** <br/> |CSOM ベースのアプリ (一貫性のあるプログラミング モデル)  <br/>-.NET では、Silverlight、Windows Phone クライアント ライブラリ  <br/>のカスタム ページ、Web パーツ、およびリボンの拡張機能用 JavaScript ライブラリ  <br/>OData および他のプロトコル<br/><br/> PSI ベースのアプリ (複雑なプログラミング モデル) では、管理、ポートフォリオ分析、通知、Project のモードのセキュリティ、キュー システム、およびその他の領域用アプリも作成できます。<br/><br/>PSI の拡張機能  <br/><br/>Project モードのセキュリティを含むユーザー設定のアクセス許可 (非推奨)  <br/><br/>PSI による偽装 (非推奨)  <br/><br/>完全信頼コード、SharePoint ファームへの機能拡張のインストール  <br/> |CSOM ベースのアプリ (一貫性のあるプログラミング モデル)  <br/>-.NET では、Silverlight、Windows Phone クライアント ライブラリ<br/>のカスタム ページ、Web パーツ、およびリボンの拡張機能用 JavaScript ライブラリ<br/>OData および他のプロトコル<br/><br/>PSI を使用できますが、サポートされていません。OAuth 接続とサービス間接続はありません<br/><br/>CSOM API の拡張機能はありません<br/><br/>ユーザー設定のアクセス許可はありません<br/><br/>偽装はありません<br/><br/>完全信頼コードはありません  <br/> |
|**カスタム データベース ** <br/> |-SQL Azure  <br/>-SQL Server (変更のレポート テーブルおよびビューでは、Project Server データベースはサポートされていません)  <br/> |-SQL Azure  <br/>-SQL Server (変更のレポート テーブルおよびビューでは、Project Server データベースはサポートされていません)  <br/> |
|**レポート** <br/> |- **ProjectData**サービスです。OData と他のプロトコル  <br/>-レポートのテーブルと、Project Server データベース内のビュー<br/>OLAP データベース  <br/> |- **ProjectData**サービスです。OData と他のプロトコル  <br/> |
|**イベント ハンドラー** <br/> |-リモート イベント レシーバー、WCF エンドポイント経由でアクセスできます。<br/>-完全に信頼できるイベント ハンドラーは、SharePoint ファームにインストールされています。  <br/> | -リモート イベント レシーバー、WCF エンドポイント経由でアクセスできます。  <br/> |
|**ワークフロー** <br/> |宣言型ワークフローは、SharePoint Designer 2013 で作成されました。<br/>-特定の Project Web App インスタンスでのみ使用します。<br/>-Visio 2013 のワークフローのデザインをインポートすることができます。<br/>インポートし、カスタム アクションを使用します。<br/><br/> Visual Studio 2012 で作成された、宣言型ワークフロー<br/>-ワークフローを含むことができるアプリケーションを作成します。<br/>-ワークフローを含むことができる SharePoint ソリューション パッケージ (.wsp) を作成します。<br/>-再利用するためのワークフロー テンプレートを作成します。<br/>-を作成し、カスタム アクションを使用します。  <br/><br/>WF3.5 で作成された従来のコンパイル済みワークフローを使用できます (宣言型の WF4 ワークフローへのアップグレードをお勧めします)  <br/> |宣言型ワークフローは、SharePoint Designer 2013 で作成されました。<br/>-特定の Project Web App インスタンスでのみ使用します。<br/>-Visio 2013 のワークフローのデザインをインポートすることができます。<br/>インポートし、カスタム アクションを使用します。  <br/><br/>Visual Studio 2012 で作成された、宣言型ワークフロー<br/>-ワークフローを含むことができるアプリケーションを作成します。  <br/>-ワークフローを含むことができる SharePoint ソリューション パッケージ (.wsp) を作成します。<br/>-再利用するためのワークフロー テンプレートを作成します。 <br/>-を作成し、カスタム アクションを使用します。  <br/> |
|**配布 ** <br/> |、(CSOM ベースのアプリケーション) は Office ストア<br/>の SharePoint 上プライベートなアプリ カタログ<br/>-イントラネットのファイル共有  <br/> |-Office ストア<br/>の SharePoint 上プライベートなアプリ カタログ  <br/> |

   
## <a name="conclusion"></a>終わりに
<a name="pj15_WhatsNew_Conclusion"> </a>

Project Server 2013 は、豊富な開発の新機能を提供し、提携している状況や顧客を使用して対応し、機能と大企業と小規模な組織で Project Server の有用。 作成し、習得し、カスタム アプリケーションの使用を大幅に拡張可能な Project 2013 のアプリケーションを配布するのには、Office 2013 および SharePoint 2013 のインフラストラクチャを使用できます。 Project 2013 の、特に、ASMX web サービスの PSI と偽装またはオンライン プロジェクトでは使用できませんが、直接データベースへの変更に関連する機能では、いくつかの拡張機能と以前のバージョンの慣行が廃止されました。
  
CSOM の導入では、さまざまなデバイスや web アプリケーションで JavaScript を使用してプロジェクトをオンラインにプログラムからのアクセスを使用できます。 CSOM は、PSI と比較して、一貫性のあるプログラミング モデルを提供します。 プロジェクトのサーバーのデータは、オンラインの OData サービスを使用し、プロジェクト データベース内のレポートのデータの残りの部分の端点を含む、以前のバージョンより多くの方法の多くにアクセスできます。 設置型で使用する場合と同じ方法で既存のレポートがまだ動作します。新しいレポートには、柔軟性があります。
  
Office アドインでは、ソリューションを販売し、プロジェクトの標準的な 2013 web コンテンツおよびその他の Office 2013 製品との統合の新たな手段を提供します。 評価のためのプロジェクトを Project Server のデータと統合する新しい方法を作成することもでき、Office アドイン] 作業ウィンドウで [SharePoint のリストです。
  
アプリケーションの開発およびプログラミング機能と SharePoint Server 2013 の CSOM を使用する方法の詳細については、 [SharePoint 開発者向け](https://msdn.microsoft.com/sharepoint)、[開発者向けの Office](https://msdn.microsoft.com/office)を参照してください。
  
## <a name="see-also"></a>関連項目

- [Project Server 2013 のアーキテクチャ](project-server-2013-architecture.md)  
- [Project のプログラミング タスク](project-programming-tasks.md) 
- [Project 2013 のクライアント側オブジェクト モデル (CSOM)](client-side-object-model-csom-for-project-2013.md) 
- [ProjectData - Project OData サービス リファレンス](https://msdn.microsoft.com/library/office/jj163015.aspx)  
- [Project 用の作業ウィンドウ アドイン](task-pane-add-ins-for-project.md)   
- [OData: URI の表記規則](https://www.odata.org/documentation/uri-conventions#FilterSystemQueryOption)    
- [SharePoint (開発者向け)](https://msdn.microsoft.com/sharepoint)    
- [Office 開発者向け](https://msdn.microsoft.com/office)   
- [SharePoint のアプリケーションでイベントの処理](https://msdn.microsoft.com/library/jj220048%28office.15%29.aspx)   
- [Office ストア](https://office.microsoft.com/en-us/store/)   
- [Project Online](https://developer.microsoft.com/en-us/project)
    

