---
title: Project での開発者向けの更新プログラム
manager: soliver
ms.date: 09/29/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5b2b22cd-6e28-43a8-9092-b411da8bfb53
description: 新機能には、クライアント側のオブジェクト モデル (CSOM)、REST インターフェイス、レポート用 OData サービス、リモート イベント レシーバー、宣言型ワークフロー、および Project クライアント用作業ウィンドウ アドインなどがあります。
ms.openlocfilehash: 0c4c3f9b4bb5852f2a620b2695c15de390ac9d78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315325"
---
# <a name="updates-for-developers-in-project"></a>Project での開発者向けの更新プログラム

project Server 2013 の拡張機能は、project Online 用のアドインとオンプレミスインストールを使用して機能します。 新機能には、クライアント側のオブジェクト モデル (CSOM)、REST インターフェイス、レポート用 OData サービス、リモート イベント レシーバー、宣言型ワークフロー、および Project クライアント用作業ウィンドウ アドインなどがあります。 さらに、新しい開発には使用しないほうがよい、使用されなくなった機能についても説明します。
  
project server 2013 は、Microsoft Office Project server 2007 で導入されたフレームワーク上にビルドされ、project server 2010 で拡張されています。 project server 2013 は、project server Interface (PSI) からリファクタリングおよび簡素化されるクライアント側オブジェクトモデル (csom) を追加します。また、windows アプリ、windows Phone 8、Microsoft Silverlight 用の JavaScript ライブラリと .net Framework 4 ライブラリを含みます。 csom は project Online 用の開発用に設計されており、オンプレミスの project Server のインストールでも動作します。 

Project Server データベースは 1 つのデータベースに統合されており、OData サービスでオンラインのレポート テーブルおよびビューにアクセスできます。 CSOM および OData サービスには Representational State Transfer (REST) インターフェイスが含まれます。 Project Server ワークフローは、SharePoint Designer 2013 を使用して作成できます。 project Professional 2013 は、project Server レポートデータ、SharePoint タスクリスト、およびその他の外部コンテンツと統合するために、作業ウィンドウの Office アドインの拡張モデルを使用できます。 Project Standard 2013 は、作業ウィンドウアドインを使用して一般的な外部コンテンツと統合できます。
  
図および project server 2013 の主な変更の詳細については、「 [project server 2013 architecture](project-server-2013-architecture.md)」を参照してください。
  
> [!NOTE]
> Project Server 2013 は SharePoint Server 2013 プラットフォームに基づいて構築され、Project 2013 には他の Office 2013 アプリケーションと同じインストラクチャが数多く含まれています。 sharepoint アドインのモデル、sharepoint ベースのワークフロー、Web パーツ、他の sharepoint 機能を使用した開発、office アドインのドキュメントのドキュメントについては、「 [sharepoint アドイン](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins)、 [office アドイン](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins)、および sharepoint」を参照してください。 [2013開発の概要](https://msdn.microsoft.com/library/jj164084%28office.15%29.aspx)。 
  
## <a name="major-new-features-in-project-2013"></a>Project 2013 の主な新機能
<a name="pj15_WhatsNew_MajorNewFeatures"> </a>

project Standard 2013 および project Professional 2013 の新機能には、他の Office 2013 アプリケーションと一致し、Windows 8 でのモダンスタイルのユーザーインターフェイスをサポートし、レポート用の office アートオブジェクトとの統合をサポートする、改良されたユーザーインターフェイスが含まれています。レポート、およびレポートの新しいプログラミング機能。 Project Professional 2013 を使用すると、SharePoint Server 2013 上でより広範な共有およびプロジェクトの同期を行うことができます。また、Word、Excel、Outlook などの他の Office 2013 アプリケーションにも実装されている作業ウィンドウアドインも利用できます。
  
Project Server 2013 には、多くの新機能があります。 Project Web App の新しいタイムラインのような主要なプログラミングストーリーはありません。 それらの機能については、Microsoft Office Online の製品のヘルプとエンド ユーザー向けドキュメント、および Microsoft TechNet の管理者と IT 担当者を対象にしたトピックに記載される予定です。 その他にも、タイムシートの向上などの新機能によって、サード パーティの開発者がタイムシートと状態管理を Project Server Interface (PSI) で容易に操作できるようになりました。
  
project Online と Office ストアの追加 (https://office.microsoft.com/store)プロジェクトアドインの場合) は、Microsoft Azure を使用して project Server にアクセスできる、大幅に変化します。 Project Server へのクラウドベースのアクセスは、JavaScript を使用する microsoft .net Framework、microsoft Silverlight、Windows Phone、および web アプリを使用したアドインの開発に、クライアント側オブジェクトモデル (csom) を使用します。 project Online の要件として、以前のバージョンの4つの Project Server データベースが1つのデータベースにマージされることが挙げられます。
  
project Server 2013 タスク状態、タイムシート、プロジェクト管理などの多くの分野で、パフォーマンスとスケーラビリティが向上しています。 Project Server ワークフローは、Windows Workflow Foundation (WF4) のバージョン4で再設計されています。 .net Framework 4 と Windows Communication Foundation (WCF) を PSI で使用すると、セキュリティ、パフォーマンス、スケーラビリティが向上します。 たとえば、WCF ベースのアプリケーションの転送プロトコルを変更する場合、アプリケーション コードを変更して再コンパイルすることなく、構成ファイルを使用して変更できます。 Project Web App では、データが大幅に変更されない PSI 呼び出しの多くがキャッシュされます。
  
> [!NOTE]
> Project Server 2013 を使用して開発する場合は、office および SharePoint のツール拡張機能を備えた Visual Studio を使用して、office 2013 製品のアドインをネイティブに作成することができます。 project Server 2013 では、Visual Studio がプロジェクト詳細ページや WCF ベースのアプリケーションなどの機能の開発を完全に有効にする必要があります。 Visual Studio の sharepoint ツール拡張機能は、web パーツやその他の sharepoint 機能を Project web App およびその他の sharepoint サイトに直接展開できます。 
>
> project Web App で管理できるユーザー設定フィールド、ステージ、フェーズ、およびエンタープライズプロジェクトの種類を使用する project Server ワークフローを開発するために Visual Studio は必要なくなりました。 Visual Studio を使用してワークフローを開発することもできますが、SharePoint Designer を使用すると、より簡単かつ迅速に作成できます。 Visual Studio は、CSOM または他の外部 API にアクセスする必要があるワークフローを開発する際に使用できます。 
  
### <a name="project-add-ins"></a>Project アドイン
<a name="pj15_WhatsNew_Apps"> </a>

ソフトウェアの配布とマーケティングは、アドインの概念によって大きく変化してきました。 Project 2013 では、アドインを購入して、パブリック Office ストアからダウンロードしたり、SharePoint のプライベートカタログ内で配布したりできます。 通常、アドインは、少数の関連タスクを実行する自己完結型の対話型プログラムです。 プロジェクトアドインは、project standard 2013 または project standard 2013 クライアント用の作業ウィンドウアドイン、または project Server 2013 または project Online 用のアドインにすることができます。
  
Project デスクトップ クライアント用アドインについては、「[Project の作業ウィンドウ アドイン](#pj15_WhatsNew_Agave)」を参照してください。 project server 2013 の例については、「 [SharePoint ホスト型の project Server アドインを作成する](create-a-sharepoint-hosted-project-server-add-in.md)」を参照してください。 office[と SharePoint アドイン SDK](https://msdn.microsoft.com/library/fp161507.aspx)の記事に加えて、 [office ブログ](https://blogs.office.com/dev/)には project 2013 および project Online に関連する多数の投稿が含まれています。 
  
project Server 2013 用のアドインは、オンプレミスのインストールと project Online の両方で機能します。 Project Server アドインには、Web パーツ、リモート イベント レシーバー、およびビジネス ロジックを含めることができます。 アドインでの Project Server オブジェクト モデルへのアクセスは、PSI ではなく CSOM を介して行われます。 データストレージは、Microsoft Business Connectivity Services (BCS)、ローカルデータベースでの内部、混合型など、SQL Azure のようなクラウドベースのものにすることができます。
  
#### <a name="add-in-security"></a>アドインのセキュリティ   通常、アドインが実行可能なアクションは、アドインを実行しているユーザーに代わって実行されます。

ユーザーが明示的に偽装を使用したり、アドインを実行可能なユーザーを指定したりすることはありません。 アドインを実行しているユーザーのアクセス許可レベルを超えるアクションは、実行できません。 
  
Office Developer Tools for Visual Studio 2012 では、AppManifext ファイルには、アクセス許可要求スコープを設定できるグラフィカルエディターがあります。 たとえば、プロジェクト マネージャーが自らのプロジェクトを更新できるアドインを作成するには、**AppManifest.xml** デザイナー ウィンドウの [**アクセス許可**] タブで、スコープは [**複数のプロジェクト**] を、アクセス許可は [**書き込み**] を選択します。 プロジェクト マネージャーの権限を持つアドイン ユーザーは、自らが管理しているプロジェクトでアドインを実行できます。 AppManifest.xml ファイル内のコードには、以下の記述が含まれます。 
  
```XML
  <AppPermissionRequests>
    <AppPermissionRequest Scope="https://sharepoint/projectserver/projects" Right="Write" />
  </AppPermissionRequests>
```

**表 1. Project Server アドイン用のアクセス許可リクエストのスコープ**

|Scope|アクセス許可|
|:-----|:-----|
|**Project Server** <br/> |**管理** (Project Server 管理者のアクセス許可が必要)  <br/> |
|**複数のプロジェクト ** <br/> |**読み取り**、**書き込み** (一部の操作にはプロジェクト マネージャーのアクセス許可が必要となり、タスクの割り当てなどの基本の読み取り操作にはプロジェクト チーム メンバーのアクセス許可が必要となります。)  <br/> |
|**1 つのプロジェクト ** <br/> |**読み取り**、**書き込み** (少なくともプロジェクト チーム メンバーのアクセス許可が必要。プロジェクト内のデータにアクセスできるかどうかは、他のアクセス許可レベルに依存します。)  <br/> |
|**エンタープライズ リソース** <br/> |**読み取り**、**書き込み** (リソース マネージャーのアクセス許可が必要)  <br/> |
|**Statusing** <br/> |**提出ステータス** (プロジェクトの状態を送信するためのアクセス許可が必要)  <br/> |
|**レポート** <br/> |**読み取り** (Project Server にログオンするためのアクセス許可が必要)  <br/> |
|**ワークフロー** <br/> |**昇格** (ワークフローを実行するためのアクセス許可が必要。ワークフローでのステージ間の移行を可能にするために、アドインは管理者特権で実行されます。ステージ遷移はアドイン内のビジネス ロジックによって制御されます。)<br/> |
   
> [!NOTE]
> project Server 2013 および project Online は、sharepoint 2013 でアプリ専用の認証モデルを使用しません (「 [sharepoint 2013 のアドイン承認ポリシーの種類」を](https://msdn.microsoft.com/library/124879c7-a746-4c10-96a7-da76ad5327f0%28Office.15%29.aspx)参照してください)。 
  
アドインの開発、配布、ホスティング、および管理の詳細については、sharepoint Server 2013 および office 2013 開発者向けドキュメントの「 [sharepoint アドイン](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins)と[office アドイン](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins)」および関連するトピックを参照してください。 他の sharepoint アドインのアクセス許可要求範囲の詳細については、「 [sharepoint 2013 でのアドインのアクセス許可](https://msdn.microsoft.com/library/5f7a8440-3c09-4cf8-83ec-c236bfa2d6c4%28Office.15%29.aspx)」を参照してください。
  
### <a name="integrating-with-sharepoint-server"></a>SharePoint Server との統合
<a name="pj15_WhatsNew_IntegrationWSS"> </a>

project Web App の多くの機能には、OAuth やクレームベース認証などの sharepoint server 2013 の新しいインフラストラクチャ、sharepoint グループによる Project Server の承認とアクセス許可、sharepoint タスクを使用したプロジェクトの同期が必要です。リスト、および Project Server の宣言型ワークフロー。 Project Service アプリケーションは、SharePoint ファーム内の任意のサイト コレクションと関連付けることができます。 プロジェクトを SharePoint タスク リストと同期し、SharePoint でプロジェクトを維持することができます。 エンタープライズ プロジェクトを SharePoint タスク リストと同期し、Project Server がフル コントロールを維持することもできます。 アーキテクチャ図とプロジェクトの同期の説明については、「 [project Server 2013 architecture](project-server-2013-architecture.md)」を参照してください。
  
SharePoint Server 2013 には、多くの新機能があります。 詳細については、「[開発者向け SharePoint](https://msdn.microsoft.com/sharepoint)」を参照してください。
  
### <a name="integrating-with-workflows"></a>ワークフローとの統合
<a name="pj15_WhatsNew_Workflow"> </a>

ワークフローはプロジェクト ポートフォリオ管理のコア機能です。プロジェクトのライフ サイクルには、多くのフェーズにまたがる長期間のプロセスを含めることができます。ガバナンス フェーズには、プロジェクトの提案、ビジネスへの影響度の分析、およびプロジェクトの選択、作成、計画、管理、追跡が含まれます。
  
Project Server 2013 ワークフローは、WF4 を使用する SharePoint 2013 ワークフロープラットフォーム上に構築されています。 以前のバージョンとは異なり、Project Server 2013 の宣言型ワークフローは、SharePoint Designer 2013 を使用して作成でき、オンプレミスとオンラインの両方で使用できます。 project Server ワークフローは、OAuth と共に SharePoint ワークフローセキュリティモデルを使用し、project Web App サイトにインストールできます。 図1は、SharePoint Designer 2013 が、Project Web App でステージが定義されている需要管理のサイトワークフローにステージを追加できることを示しています。
  
**図 1. SharePoint Designer を使用した Project Web アプリ用ワークフローへのステージの追加**

![SPD でワークフローにステージを追加する](media/pj15_CreateWorkflowSPD_AddStageInSPD.gif "SPD でワークフローにステージを追加する")

<br/>

宣言型ワークフローを構築するには、SharePoint Designer 2013 または Visual Studio 2012 のいずれかのデザインツールで、ワークフローステージ、アクション、条件、およびその他の要素を追加します。 その後、デザインツールはワークフローを XAML コードとして保存します。これは、実行時に解釈されます。 宣言型ワークフローは、オンプレミスの project Server 2013 で、または project Online で実行できます。 Visual Studio 2012 を使用すると、追加のコントロール用にカスタムアクションやフォームを作成したり、複数の Project Web App インスタンスで再利用するためのワークフローテンプレートを保存したりすることもできます。 SharePoint Designer 2013 は、Visual Studio 2012 で作成されたカスタムアクションを使用できます。
  
project Server 2013 ワークフローは、アプリケーションとして動作します。ここでは、project Web app のデザイン権限を持つ管理者が宣言型ワークフローを発行して、それをエンタープライズプロジェクトの種類 (EPT) に関連付けることができます。 EPT は Project Server がフル コントロールを維持するエンタープライズ プロジェクトにする必要があります。 SharePoint タスク リストでは Project Server ワークフローを使用できません。 
  
OAuth では、プロジェクト マネージャーはプロジェクト作成権限が与えられ、偽装を使用せずにワークフローを起動できます。 Project Server へのワークフローの呼び出し、たとえば、通過する分岐を選択するためのユーザー設定フィールド値の読み取りを、プロジェクト マネージャーを代理して実行します。 自動的に次のステージに進むワークフローをプロジェクト マネージャーが作成することを防ぐため、次のワークフロー ステージに移動するための呼び出しはワークフロー作成者 (管理者) 権限で実行されます。 これに対して、従来の Project Server 2010 ワークフローのユーザーは、ワークフロープロキシユーザーアカウントを介して偽装された呼び出しを行って、ワークフロー全体にわたる管理者アクセスを取得します。
  
オンプレミスの Project Server 2013 は、コンパイルされた wf 3.5 ベースのワークフローを使用できますが、従来のワークフローを WF4 に基づいて宣言型ワークフローにアップグレードすることをお勧めします。 最新のテクノロジは、より拡張性があり堅牢です。 ビジネスアナリストおよび PMO は、Visio 2013 を使用してワークフローデザインを作成または更新したり、SharePoint Designer 2013 を使用してコーディングせずに Project Server ワークフローを実装したりできます。
  
project Web App の宣言型ワークフローを作成する方法については、「 [project Server ワークフローの開発](getting-started-developing-project-server-workflows.md)作業の開始」を参照してください。 sharepoint Designer と visual studio のワークフローの機能の比較については、「 [visual studio を使用して sharepoint 2013 ワークフローを開発](https://msdn.microsoft.com/library/office/jj163199.aspx)する」を参照してください。
  
### <a name="client-side-object-model"></a>クライアント側オブジェクト モデル
<a name="pj15_WhatsNew_CSOM"> </a>

Project Online へのプログラムによるアクセスには、SharePoint csom 上に構築された csom が必要です。 project Online の認証は、project Server フォーム認証または windows 認証ではなく、windows Live ID を使用して OAuth によって行われます。
  
Project Server 2013 の csom の原則と機能は、次のとおりです。
  
- CSOM は使いやすさを考慮して設計されています。 たとえば、メソッドとプロパティは、多くの guid、 _changeXml_ parameters、またはデータセットを使用するのではなく、名前によってデータを直接使用または提供します。 
    
- Project Server の CSOM はサードパーティのソリューションの一般的な要件に基づいて PSI 機能のサブセットを実装します。
    
- CSOM は PSI を内部的に呼び出しますが、その構造は変わったものになっています。 たとえば、すべての状態変更の更新が **StatusAssignmentCollection.SubmitAllStatusUpdates** メソッドを使用して行われるようになっており、ユーザーについては PSI メソッドの **Statusing.SubmitStatus** を使用し、その他のリソースについては **SubmitStatusForResource** メソッドを使用する、というようにはなっていません。 
    
- PSI の 22 個のパブリック サービスを使用しなくても、1 つの WCF サービス (Client.svc) で CSOM に アクセスできます。
    
- project Server csom の初期化は、project Web App の URL を使用して[projectcontext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx)クラスを直接行うことができます。これは、WCF 参照またはプロキシアセンブリを使用したものではありません。 
    
- CSOM は、内部 SharePoint CSOM インフラストラクチャでサポートされる複数のクライアント ライブラリおよびインターフェイスを実装します。クライアント ライブラリおよびインターフェイスには次のものが含まれます。
    
  - Microsoft.ProjectServer.Client.dll アセンブリ内の Microsoft .NET クライアント ライブラリ
    
  - silverlight ライブラリ (microsoft.projectserver.client アセンブリ内のライブラリ)
    
  - Microsoft.ProjectServer.Client.Phone.dll アセンブリ内の Windows Phone 8 ライブラリ
    
  - .js ファイルまたは pcl ファイル内の web アプリケーションの JavaScript ライブラリ
    
  - OData プロトコルを使用してアクセスするための REST エンドポイント
    
  - フィルター処理によって返されるデータ量を制限できる LINQ クエリのネイティブ サポート
    
- csom は、project Online ソリューションとオンプレミスソリューションの両方で使用できます。これは、PSI やその他の project server アセンブリ (たとえば、) とは独立して使用できます。
    
- project server パートナーおよび開発者コミュニティからの要求に基づいて、project server 2013 csom の追加機能を考慮して、累積的な更新プログラムおよびサービスパックを検討することができます。
    
> [!NOTE]
> CSOM はサードパーティの Project Server 開発者にお勧めのインターフェイスです。新しいアプリケーションを開発する際に、対象アプリケーションに必要な機能が CSOM に含まれている場合には、CSOM を使用することをお勧めします。 
  
csom を使用した開発の詳細については、「 [Project 2013 のクライアント側オブジェクトモデル (csom)](client-side-object-model-csom-for-project-2013.md)」を参照してください。 sharepoint アプリケーションの rest インターフェイスの詳細については、「sharepoint 2013 開発者向けドキュメントの「 *sharepoint rest サービスを使用したプログラミング*」を参照してください。 
  
### <a name="changes-in-the-reporting-database"></a>レポート データベースの変更点
<a name="pj15_WhatsNew_RDBChanges"> </a>

project server 2010 の4つのデータベースは、project server 2013 の単一の project データベースに統合されています。 Project データベースの既定の名前は ProjectService です。 レポートテーブルとビューは、以前の名前を保持し、下書き、発行済み、アーカイブの各データベースからのテーブル`draft`と`pub`ビューは`ver` 、そのプレフィックス、、および projectservice データベースから取得されます。 たとえば、発行済みプロジェクト テーブルの名前は pub.MSP_PROJECTS です。 
  
> [!IMPORTANT]
> 下書き (`draft`プレフィックス)、発行済み (`pub`)、およびアーカイブ (`ver`) のテーブルとビューに対して直接アクセスはサポートされていません。 レポートでは、レポートテーブルおよびビューのみを使用し、 `dbo`接頭辞を設定する必要があります。 たとえば、dbo.MSP_EpmProject テーブルには、Project Web App インスタンスのプロジェクトの一覧が含まれています。 
>
> Project データベースのテーブルおよびビューには、プログラムによってデータベースに直接アクセスしてデータを更新することを能動的に妨げるものは存在しません。Project Professional キャッシュ、下書きおよび発行済みデータ テーブル、およびレポート テーブルはすべてがキャッシュ同期プロトコルに依存しているので、直接データを編集すると同期が混乱する可能性があることに注意が必要です。直接アクセスしてデータを変更することによって、Project Server データベースや Project Professional クライアント側キャッシュが破損した場合、製品サポートは役に立てません。 
  
Project Server 2013 には、オンラインおよびオンプレミスのアクセスのための OData サービスが導入されています。 オンラインのレポートテーブルとビューは、OData インターフェイスによってのみ公開されます。オンプレミスで使用する場合は、OData インターフェイスを使用するか、SharePoint ファームの projectservice データベースのレポートテーブルとビューに直接アクセスすることができます。 Project Online は、マルチテナントデータベースをサポートしていません。 つまり、project Web App の複数のインスタンスがそれぞれ独自のプロジェクトデータベースを持っています。 OData サービスは、レポートテーブルおよびビューに対して SQL クエリを内部的に実行し、XML または JSON ペイロードを配信します。 Project Server 2013 でのレポート用 OData サービスの概要、および**projectdata**スキーマの参照については、「 [projectdata-Project OData サービスリファレンス](https://msdn.microsoft.com/library/office/jj163015.aspx)」を参照してください。
  
odata クエリの概要については、「 [odata: URI の規則](https://www.odata.org/documentation/)」を参照してください。 たとえば、ブラウザーで次のクエリを使用すると、project Web App の社内インスタンスで、プロジェクト名が "Test" で始まるすべてのプロジェクトが表示されます。 ブラウザーのページを右クリックし、[**ソースの表示**] をクリックします。
  
```html
https://ServerName /ProjectServerName /_api/ProjectData/Projects?$filter=startswith(ProjectName, 'Test') eq true
```

Excel 2013 で project データを PowerPivot にインポートするには、[データ] リボンの [**その他のソースから**] ドロップダウンメニューから [ **OData データフィードから**] を選択します。 [**データ接続ウィザード**] ダイアログボックスで、 https://ServerName/ProjectServerName/_api/ProjectData/データフィードの場所を入力し、[**次へ**] を選択して、ウィザードの [**テーブルの選択**] ページで [**プロジェクト**] テーブルを選択します。 .odc ファイルに名前を付けて保存し、[**完了**] をクリックします。 [**データのインポート**] ダイアログ ボックスで [**ピボットテーブル レポート**] を選択します。 Excel ワークシートで、表示するピボット テーブルの行と列のフィールドを選択します。
  
オンプレミスの project server ユーザーは、適切なアクセス許可を持っている場合、Microsoft SQL Server を使用してレポートテーブルおよびビューに直接アクセスすることにより、レポートを作成できます (project server 2010 の場合など)。 Project Server 2013 では、OData インターフェイスを使用してオンプレミスのレポートテーブルにアクセスすることもできます。 Project Server のデータは、OData サービス用の REST エンドポイントを使用して、オンラインまたはオンプレミスで取得できます。 たとえば、dbo.MSP_PROJECT テーブルと dbo.MSP_EpmProject_UserView ビューをレポートに使用できます。 、、または`draft` `pub` `ver`プレフィックスを持つすべてのテーブルまたはビューは、Project Server のみで内部的に使用され、レポート用には使用できません。 たとえば、draft.MSP_TASKS テーブルと pub.MSP_PROJECTS_WORKING_VIEW ビューはドキュメントに記載されておらず、内部使用専用です。 
  
> [!NOTE]
> オンプレミス レポートは、別のデータベース内のテーブル、ビュー、フィールド、およびストアド プロシージャを追加して拡張できます。Project Server データベース内の既存のレポート テーブルやレポート ビューは変更しないでください。 
  
project データベースのレポートテーブル、ビュー、およびフィールドは、project 2013 SDK のダウンロードの後の更新プログラムで HTML ヘルプファイルに記載されています。 **projectdata**サービスの odata XML スキーマのドキュメントについては、「 [projectdata-Project odata サービスリファレンス](https://msdn.microsoft.com/library/office/jj163015.aspx)」を参照してください。 project server 2010 用に作成されたレポートテーブルおよびビューのクエリは、ほとんどの場合、project server 2013 でプロジェクトデータベースを操作します。 オンプレミスのユーザーは、現在と同様に SQL Server Analysis Services で Project Server OLAP キューブにアクセスできます。 Project Online では、OLAP キューブは使用できません。
  
### <a name="task-pane-add-ins-in-project"></a>Project の作業ウィンドウ アドイン
<a name="pj15_WhatsNew_Agave"> </a>

project Standard 2013 と project Professional 2013 はどちらも、作業ウィンドウアドインをサポートしています。これは、web ページに外部コンテンツを統合して表示するために使用できます。 作業ウィンドウには、JavaScript によってタスク、リソース、ビュー、および一般的なプロジェクトデータにアクセスできる web ページコンテンツが表示されます。 Project 用の JavaScript オブジェクトモデルは、選択されたタスクまたはリソースに関する情報を取得し、[ガントチャート] などのビューでグリッド内の選択したセルのデータを取得することができます。 Project 用の作業ウィンドウアドインでは、タスク、リソース、またはビューの選択変更イベントのイベントハンドラを実装することもできます。 
  
図2は、 **projectdata**サービスを照会する**Hello projectdata**作業ウィンドウアドインを示し、現在のプロジェクトのデータをすべてのプロジェクトの平均値と比較したものです。 Project 2013 SDK のダウンロードには、アドインの完全なソースコードが含まれています。 
  
**図 2. Project Professional 内の作業ウィンドウ アドインは Project Server 内のデータにアクセスできる**

![現在のプロジェクトとすべてのプロジェクトの比較](media/pj15_RestQueryApp_CompareProject.gif "現在のプロジェクトとすべてのプロジェクトの比較")
  
> [!NOTE]
> project Standard 2013 は、作業ウィンドウアドインを使用して project Server 2013 と直接統合することはできません。 
  
project professional の作業ウィンドウアドインは、project Server 2013 用に構築された Web パーツをサポートしているため、開発者は、project Web App と project Professional の両方を実行すると、拡張機能を作成できます。 他の Office 2013 製品用に開発された一般的な作業ウィンドウアドインは、project Standard 2013 および project Professional 2013 でも使用できます。 詳細については、「[Task pane add-ins for Project](task-pane-add-ins-for-project.md)」を参照してください。
  
### <a name="project-server-event-receivers"></a>Project Server イベント レシーバー
<a name="pj15_WhatsNew_Events"> </a>

バックエンド project サービスアプリケーションを含む SharePoint ファームには、複数の project web App サーバー (web フロントエンドサーバーまたは web フロントエンドサーバーとも呼ばれる) が存在することがあります。 イベント レシーバーはイベント ハンドラーとも呼ばれます。 ローカル イベント ハンドラーを完全な信頼コードで実装し、Project Server のローカル インストールですべての WFE に展開できます。 リモート イベント レシーバーをローカルまたはリモート サーバーの Web サービスに実装して複数の WFE および複数の Project Server インストールからアクセスできます。 Project Online では、リモートイベントレシーバーのみを使用できます。
  
project Server イベントハンドラは、特定の project web app 設定ページではなく、各 project web app インスタンスで SharePoint によって管理されます。 SharePoint サーバーの全体管理アプリケーションで、[**アプリケーションの全般設定**] を選択し、[ **pwa 設定**] の下にある [**管理**] を選択してから、pwa 設定の [ **Project Web App インスタンス**] ドロップダウンリストでインスタンスを選択します。page. ローカルイベントハンドラーまたはリモートイベントレシーバーを追加するには、[**サーバー側のイベントハンドラー**] を選択します。
  
Project Server のオンプレミスインストールでは、リモートイベントレシーバーを csom の[EventHandlerCreationInformation](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCreationInformation.aspx)クラスを使用する SharePoint フィーチャーとして作成し、プログラムによって管理することができます。[EventHandlerCollection](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCollection.aspx)クラスのメソッドを使用したイベントレシーバー。 リモート イベント レシーバーではプレイベントが同期、ポストイベントは非同期であり、リモート イベント レシーバーが制御を返さない場合はタイムアウトが発生します。 
  
> [!NOTE]
> SharePoint サーバーの全体管理は、オンプレミス インストールでのみ使用できます。 Project online と SharePoint online では、csom ベースのアプリパッケージを使用して、リモートイベントレシーバーを追加または削除することができます。 
  
[サーバー側のイベントハンドラ] ページでは、オンプレミスの project server インストール用のローカルイベントハンドラーを追加するプロセスは、「プロジェクトサーバー[イベントハンドラーを作成し](https://msdn.microsoft.com/library/gg615466.aspx)て、project server のイベントをログに記録する」の手順とほぼ同じです。2010 違いは、[新しいイベントハンドラー] ページに追加オプションがあるということです。 たとえば、[**イベント**] の一覧で [**プロジェクトの作成**] を選択し、[**新しいイベントハンドラー**] を選択します。 [新しいイベントハンドラー] ページでは、2つの必須フィールドが**名前**と**順序**になります (図3を参照)。 完全信頼のローカルイベントハンドラーを追加する場合は、[**アセンブリ名**] フィールドと [**クラス名**] フィールドを追加します。**エンドポイント Url**は空のままにします。 リモートイベントレシーバーを追加している場合は、**エンドポイント Url**を追加し、**アセンブリ名**と**クラス名**は空のままにします。 
  
> [!CAUTION]
> アセンブリ名/クラス名とエンドポイント URL の*両方*を指定すると、Project Server はローカル (社内) イベントハンドラーのみを呼び出します。 リモート イベント レシーバーは無視されます。 
> 
> 同じイベントに 2 つのイベント ハンドラー (一方のイベント ハンドラーがローカルで、もう一方がリモート イベント レシーバー) を作成する場合、**[Order]** の値が両方とも同じであれば、Project Server はリモート イベント レシーバーを無視します。 
  
**図 3. ローカル イベント ハンドラーまたはリモート イベント レシーバーの追加**

![イベントハンドラーまたはイベントレシーバーを構成する](media/pj15_EventHandlers_NewEventHandler.gif "イベントハンドラーまたはイベントレシーバーを構成する")
    
ローカルイベントハンドラーの PSI データセットにアクセスする必要がある場合は、[Windows] \Microsoft.NET\assembly\GAC\_MSIL\Microsoft.Office.Project.Schema\v4.0_15.0.0.0__ からそのアセンブリをコピーできます。71e9bce111e・ 71 29c ディレクトリ。 

PSI の代わりに、 **microsoft.projectserver.client**名前空間でイベントクラスを使用することをお勧めします。csom を使用した開発では、データセットを操作する必要はありません。 Project Online のリモートイベントレシーバーを開発するには、csom で[event](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.Event.aspx)クラスと[EventHandlerCreationInformation](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCreationInformation.aspx)クラスを使用する必要があります。 
  
Project Server のテスト インストールにイベント ハンドラーをインストールし、十分にテストしてから Project Server イベント ハンドラーを展開してください。 オンプレミスの Project server インストールの場合、追加するローカルイベントハンドラーが動作しない場合、Project Server 2013 Events Service は他の有効なカスタムイベントハンドラーの読み込みに失敗します。 その場合は、問題のあるイベント ハンドラーを削除して Events Service を再起動する必要があります。
  
> [!NOTE]
> オンプレミスの Project Server インストールでイベント レシーバーを開発するには、CSOM を使用してリモート イベント レシーバーに移行することをお勧めします。リモート イベント レシーバーには Project Server Events Service 内で実行するサードパーティのコードが存在しないため、リモート イベント レシーバーの方が安定しています。ローカル管理者は、Project Server Events Service のメンテナンスを行う責任が軽減されます。 
  
イベントに関する一般的な情報については、「 [SharePoint 用アプリでイベントを処理](https://msdn.microsoft.com/library/jj220048%28office.15%29.aspx)する」を参照してください。 
  
## <a name="deprecated-features"></a>推奨されない機能
<a name="pj15_WhatsNew_Deprecated"> </a>

> [!NOTE]
> project server 2016 preview で廃止または削除された機能と api については、「 [project server 2016 プレビューで廃止または削除](https://technet.microsoft.com/library/mt422816%28v=office.16%29.aspx)された機能」を参照してください。 
  
廃止された機能は、一部のソリューションでは引き続き Project 2013 で利用できますが、新しい開発には使用しないでください。 以下の機能とプラクティスのほとんどは、project Online では動作しないか、または SharePoint アクセス許可モードの project Server 2013 の既定のオンプレミスインストールでは機能しません。 これらの機能を使用する既存のソリューションは、project server 2010 から project server 2013 へのアップグレードでは動作しない可能性があります。 非推奨の機能を使用するソリューションは、一部の場合は引き続き機能しますが、すべての Project 2013 インストールで完全にサポートされているわけではありません。
  
お客様のソリューションで非推奨になった機能を使用する場合は、展開する前に十分にテストする必要があり、サポートされる機能が実際に使用できるようになり次第サポートされる機能を使用するように変更する必要があります。 project アクセス許可モードのオンプレミス project server 2013 セキュリティを構成する方法については、「 [project server 2013 の新機能の概要](https://technet.microsoft.com/en-us/library/ff631142%28office.15%29.aspx)」の「 *SharePoint アクセス許可モード*」セクションを参照してください。
  
- **拡張機能**[PSI 拡張機能のシナリオ](https://msdn.microsoft.com/library/office/ff843378%28v=office.14%29.aspx)は推奨されておらず、今後のリリースではサポートされません。 これらのオンプレミスの Project Server 2013 のシナリオでは、カスタムの Windows Communication Foundation (WCF) サービスを使用した統合が有効になっています。 
  
- **プロジェクト PSI**PSI の[Project クラス](https://docs.microsoft.com/office/client-developer/project/project-psi-reference-overview)は推奨されていません。 すべての新しい開発では、[Project CSOM](client-side-object-model-csom-for-project-2013.md) を使用してください。 project Server 2013 プロジェクト PSI を使用するアプリは引き続き動作しますが、project Online アプリはプロジェクトクラスの PSI メソッドを同等の csom メソッドに置き換える必要があります。
  
- **リソース計画 PSI**[リソース計画 PSI](https://msdn.microsoft.com/library/office/websvcresourceplan_di_pj14mref.aspx)は推奨されていません。 プロジェクト2013の開発では引き続きサポートされますが、今後のリリースではサポートされません。 
  
- **PSI の ASMX インターフェイス**PSI には、オンプレミスの Project Server extensions を開発するための、重複するインターフェイスが用意されています。 ASMX web サービスインターフェイスは、Office Project Server 2007 の PSI の最初の実装で導入されました。 Project Server 2010 には、オブジェクトモデルが ASMX web サービスを基本的に複製する WCF サービスインターフェイスが追加されました。 Project Server 2013 は ASMX と wcf の両方を引き続きサポートしていますが、PSI を必要とする新しいソリューションでは、wcf サービスを使用する必要があります。 可能であれば、新しいソリューションは、CSOM を使用して記述することをお勧めします。 
  
  PSI の ASMX web サービスは、Project Server 2013 で廃止されました。 Project Server の今後のバージョンで機能するために、ASMX Web サービスを使用するソリューションは、WCF サービスまたは CSOM のいずれかを使用して書き換える必要があります。 詳細については、「 [project server のプログラミング](project-server-programmability.md)」の「 *project server api を使用*してアプリケーションをアップグレードする」を参照してください。
  
- **オブジェクトリンクプロバイダー (olp)** 以前のバージョンの project Server では、PSI の**objectlinkprovider**サービス (「 [WebSvcObjectLinkProvider](https://msdn.microsoft.com/library/WebSvcObjectLinkProvider.aspx) 」を参照) を使用して、プロジェクトサイト内のエンタープライズプロジェクトタスクと特別な SharePoint リストとの間で web オブジェクトのリンクを管理することができます。懸案事項、リスク、成果物、およびドキュメントの場合。 Project Server 2013 では、olp は推奨されていません。 
  
  SharePoint csom の**[RelatedItemManager](https://msdn.microsoft.com/library/microsoft.sharepoint.client.relateditemmanager.aspx)** クラスを使用すると、タスクリスト内のアイテムとプロジェクトサイト内の他のリストの間で、web オブジェクトリンクを作成、読み取り、および削除できます。 たとえば、タスクアイテムから懸案事項へのリンクを追加するには、 **[AddSingleLink](https://msdn.microsoft.com/library/office/microsoft.sharepoint.client.relateditemmanager.addsinglelink.aspx)** メソッドを使用するか、または、 **AddSingleLinkFromUrl**または**AddSingleLinkToUrl**のどちらかの類似するメソッドを使用します。 **RelatedItemManager** クラスには、Web オブジェクトのリンクを削除するメソッドと、関連する項目を読み取るメソッドも含まれています。 jsom (JavaScript オブジェクトモデル) の同等のクラスについては、「SP」を参照してください[。RelatedItemManager オブジェクト (sp .js)](https://msdn.microsoft.com/library/jj838582.aspx)。
  
  SharePoint csom を使用して、project Server 2013 および project Online の社内インストール用に olp タイプのアプリを作成することをお勧めします。 RelatedItemManager ( [SharePoint](https://msdn.microsoft.com/library/microsoft.sharepoint.aspx) ) 名前空間には、 **** * * * * クラスは含まれていません。 
  
- **カスタムアクセス許可**特定の project server 機能または拡張機能にアクセスするためのカスタムセキュリティ権限が Office Project server 2007 でサポートされていました。ここでは、発行済みデータベースを直接変更して作成する方法について、SDK 記事で説明しています。 Project Server 2010 では、カスタムアクセス許可は引き続き機能しますが、廃止されました。 Project Server 2013 では、カスタムアクセス許可は、オンプレミスインストールの既定の SharePoint アクセス許可モードでは動作しません。 プロジェクトアクセス許可モードでは、カスタムアクセス許可がサポートされています。 Project Online では、直接データベースアクセスはできません。 
  
- **偽装**PSI ベースのアプリでの偽装。これは、アプリのユーザーが、project server 2013 で使用されなくなった別の project server ユーザーのセキュリティアクセス許可を引き受けることができるようにすることです。 前述したように、既定のオンプレミスの project server 2013 インストールは SharePoint アクセス許可モードを使用します。これにより、project server セキュリティグループでの偽装は許可されません。 詳細については、「[Authentication, authorization, and security in SharePoint 2013](https://msdn.microsoft.com/library/ms457529%28office.15%29.aspx)」を参照してください。
  
  Statusing アプリケーションは、以前のバージョンの Project Server で偽装を使用している可能性のある一般的な拡張機能です。 Project Server 2010 には、PSI に**readstatusforresource**メソッドと**submitstatusforresource**メソッドが導入されました。 **statusbrokerpermission**グローバルアクセス権に加えて、開封に対する偽装が不要になりました。別のユーザーの代わりに状態を更新します。 project Server 2013 の csom は、基礎となる PSI を使用して透過的に statusing 拡張機能を有効にし、project Online またはオンプレミスのインストールで使用できます。 
  
- **レポートデータベースの拡張機能**以前のバージョンの Project Server では、ユーザー設定のテーブルとビューをレポートデータベースに追加することは一般的な方法です。 project server 2013 では、以前のバージョンの4つのデータベースが1つのデータベースに結合されるので、アップグレードでは、カスタムテーブル、ビュー、または sprocs が project server 2013 データベースのレポートテーブルに転送されません。 
  
  カスタムレポートテーブルおよびビューには、sql Azure または別の sql Server データベースを使用することをお勧めします。これには、データベースのバックアップと更新を管理できます。 Project Online の場合、これは必須です。
  
- **レポート**Project Server データベースのローカルのレポートテーブルと OLAP キューブは非推奨になり、完全** にサポートされたままです。 ただし、レポートテーブルおよびビュー (以前の project Server バージョンのレポートデータベース) は、project Online ではアクセスできません。 同様に、OLAP キューブは、Project Server 2013 の社内インストールでのみ使用できます。 Project Online を使用したレポートアプリケーションでは、OData プロトコルを使用して REST クエリを実行することにより、 **projectdata**サービスを使用できます。 
  
- **プロジェクトガイド**プロジェクトガイドは、Office project 2007 デスクトップアプリケーションの標準機能です。ここでは、作業ウィンドウの HTML と JavaScript の内容によって、プロジェクトを作成および管理するための対話的なガイダンスが提供されます。 project 2010 では、プロジェクトガイドは既定のインストールでは使用できませんが、VBA または VSTO アドインを使用して有効にすることができます。 project 2010 SDK のダウンロードには、変更されたプロジェクトガイドファイルが含まれています。 
  
  プロジェクト2013の VBA オブジェクトモデルと**Microsoft Office**アプリケーションモデルは、プロジェクトガイドを管理するための22個のメンバー、 **Application**クラス、 **project**クラスを含んでいます。 ただし、project 2013 の作業ウィンドウアプリは、[プロジェクトガイド] 作業ウィンドウのアクションとは競合することがあります。また、プロジェクトガイドの内容は、Office ストアで簡単に配布または販売することはできません。 カスタムのプロジェクトガイドのコンテンツではなく、Office アドインを使用して project の作業ウィンドウソリューションを開発することを強くお勧めします。 プロジェクトガイドの詳細については、「 [project 2010 SDK のドキュメント](https://msdn.microsoft.com/library/ms512767.aspx)」を参照してください。
  
## <a name="comparing-project-server-on-premises-with-project-online"></a>オンプレミスの Project Server と Project Online との比較
<a name="pj15_WhatsNew_Comparing"> </a>

オンプレミスの project server と project online のどちらを使用するか、どのような種類の拡張機能を開発できるようにするかについては、表2では、project server 2013 のオンプレミスインストールの拡張機能と project online の機能を比較しています。 この表 2 には、開発、管理、または使用法の相違点は記載していません。 project online と project Server 2013 の詳細については、「 [project 2013 for 開発者](https://msdn.microsoft.com/office/fp161502)および[project Online](https://developer.microsoft.com/en-us/project)」を参照してください。
  
**表 2. オンプレミスの Project Server と Project Online の拡張性**

| 機能 |オンプレミスの Project Server | Project Online |
|:-----|:-----|:-----|
|**プログラミング** <br/> |CSOM ベースのアプリ (一貫性のあるプログラミング モデル)  <br/>-.net、Silverlight、Windows Phone クライアントライブラリ  <br/>-カスタムページ、Web パーツ、およびリボン拡張機能の JavaScript ライブラリ  <br/>-OData および REST プロトコル<br/><br/> PSI ベースのアプリ (複雑なプログラミング モデル) では、管理、ポートフォリオ分析、通知、Project のモードのセキュリティ、キュー システム、およびその他の領域用アプリも作成できます。<br/><br/>PSI の拡張機能  <br/><br/>Project モードのセキュリティを含むユーザー設定のアクセス許可 (非推奨)  <br/><br/>PSI による偽装 (非推奨)  <br/><br/>完全信頼コード、SharePoint ファームへの機能拡張のインストール  <br/> |CSOM ベースのアプリ (一貫性のあるプログラミング モデル)  <br/>-.net、Silverlight、Windows Phone クライアントライブラリ<br/>-カスタムページ、Web パーツ、およびリボン拡張機能の JavaScript ライブラリ<br/>-OData および REST プロトコル<br/><br/>PSI を使用できますが、サポートされていません。OAuth 接続とサービス間接続はありません<br/><br/>CSOM API の拡張機能はありません<br/><br/>ユーザー設定のアクセス許可はありません<br/><br/>偽装はありません<br/><br/>完全信頼コードはありません  <br/> |
|**カスタム データベース ** <br/> |-SQL Azure  <br/>-SQL server (Project Server データベースのレポートテーブルとビューの変更はサポートされていません)  <br/> |-SQL Azure  <br/>-SQL server (Project Server データベースのレポートテーブルとビューの変更はサポートされていません)  <br/> |
|**レポート** <br/> |- **projectdata**サービス、OData および REST プロトコル  <br/>-Project Server データベースのレポートテーブルとビュー<br/>-OLAP データベース  <br/> |- **projectdata**サービス、OData および REST プロトコル  <br/> |
|**イベント ハンドラー** <br/> |-WCF エンドポイントを介してアクセスできるリモートイベントレシーバー<br/>-SharePoint ファームにインストールされた完全信頼イベントハンドラー  <br/> | -WCF エンドポイントを介してアクセスできるリモートイベントレシーバー  <br/> |
|**ワークフロー** <br/> |宣言型ワークフロー (SharePoint Designer 2013 で作成)<br/>-特定の Project Web App インスタンスでのみ使用します。<br/>-Visio 2013 からワークフロー設計をインポートできます。<br/>-カスタムアクションをインポートして使用できます<br/><br/> Visual Studio 2012 を使用して作成された宣言型ワークフロー<br/>-ワークフローを含めることができるアプリを作成する<br/>-ワークフローを含めることができる SharePoint ソリューションパッケージ (.wsp) を作成する<br/>-再利用可能なワークフローテンプレートを作成する<br/>-カスタムアクションを作成して使用する  <br/><br/>WF3.5 で作成された従来のコンパイル済みワークフローを使用できます (宣言型の WF4 ワークフローへのアップグレードをお勧めします)  <br/> |宣言型ワークフロー (SharePoint Designer 2013 で作成)<br/>-特定の Project Web App インスタンスでのみ使用します。<br/>-Visio 2013 からワークフロー設計をインポートできます。<br/>-カスタムアクションをインポートして使用できます  <br/><br/>Visual Studio 2012 を使用して作成された宣言型ワークフロー<br/>-ワークフローを含めることができるアプリを作成する  <br/>-ワークフローを含めることができる SharePoint ソリューションパッケージ (.wsp) を作成する<br/>-再利用可能なワークフローテンプレートを作成する <br/>-カスタムアクションを作成して使用する  <br/> |
|**分配** <br/> |-Office ストア (csom ベースのアプリ用)<br/>-SharePoint 上のプライベートアプリカタログ<br/>-イントラネットファイル共有  <br/> |-Office ストア<br/>-SharePoint 上のプライベートアプリカタログ  <br/> |

   
## <a name="conclusion"></a>まとめ
<a name="pj15_WhatsNew_Conclusion"> </a>

project server 2013 には、大規模な企業や小規模な組織で project server の機能と有用性を適応および拡張するためにパートナーやお客様が使用できる豊富な新しい開発機能とシナリオが用意されています。 Office 2013 および SharePoint 2013 のインフラストラクチャを使用して、プロジェクト2013用のアプリを作成して配布することができます。これにより、ユーザー設定のアプリケーションを簡単に拡張し、使用することができます。 以前のバージョンの一部の拡張機能とプラクティスは、project 2013 で廃止されました。特に、PSI の ASMX web サービスと、偽装または直接的なデータベースの変更が含まれる機能 (project Online では使用できません)。
  
csom の導入により、さまざまなデバイスや web アプリケーションで JavaScript を使用して、Project Online へのプログラムによるアクセスが可能になります。 CSOM は PSI より一貫性に優れたプログラミング モデルです。 Project Server データへのアクセス方法も、オンライン OData サービスを使用する方法や Project データベース内のレポート データ用 REST インターフェイスを使用する方法など、以前のバージョンより多様になりました。 既存のレポートは今後もオンプレミスでの利用の場合と同様の方法で使用できますが、新しいレポートはさらに柔軟性が向上しています。
  
office アドインは、ソリューションを販売するための新しい手段を提供し、Project Standard 2013 を web コンテンツおよびその他の Office 2013 製品と統合します。 作業ウィンドウ Office アドインを使用して project Server データおよび SharePoint リストと project Professional 2013 を統合するための新しい方法を作成することもできます。
  
アプリの開発について、および sharepoint Server 2013 のプログラミング機能と csom を使用する方法については、「 [sharepoint for](https://msdn.microsoft.com/sharepoint)開発者向けの sharepoint」および「[開発者向け Office](https://msdn.microsoft.com/office)」を参照してください。
  
## <a name="see-also"></a>関連項目

- [Project Server 2013 のアーキテクチャ](project-server-2013-architecture.md)  
- [Project のプログラミング タスク](project-programming-tasks.md) 
- [Project 2013 のクライアント側オブジェクト モデル (CSOM)](client-side-object-model-csom-for-project-2013.md) 
- [ProjectData - Project OData サービス リファレンス](https://msdn.microsoft.com/library/office/jj163015.aspx)  
- [Project 用の作業ウィンドウ アドイン](task-pane-add-ins-for-project.md)   
- [OData: URI の規則](https://www.odata.org/documentation/uri-conventions#FilterSystemQueryOption)    
- [SharePoint デベロッパー センター](https://msdn.microsoft.com/sharepoint)    
- [開発者のための Office](https://msdn.microsoft.com/office)   
- [SharePoint 用アプリでのイベントの処理](https://msdn.microsoft.com/library/jj220048%28office.15%29.aspx)   
- [Office ストア](https://office.microsoft.com/en-us/store/)   
- [Project Online](https://developer.microsoft.com/en-us/project)
    

