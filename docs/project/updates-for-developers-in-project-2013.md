---
title: 開発者向けの更新プログラム (Project
manager: lindalu
ms.date: 12/03/2019
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 5b2b22cd-6e28-43a8-9092-b411da8bfb53
description: 新機能には、クライアント側のオブジェクト モデル (CSOM)、REST インターフェイス、レポート用 OData サービス、リモート イベント レシーバー、宣言型ワークフロー、および Project クライアント用作業ウィンドウ アドインなどがあります。
ms.openlocfilehash: 0f9cfc226e7ef4e5c2f81301812578e3ce9e58e9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59555000"
---
# <a name="updates-for-developers-in-project"></a>開発者向けの更新プログラム (Project

Project Server 2013 の機能拡張機能は、Project Onlineオンプレミス インストール用のアドインで動作します。 新機能には、クライアント側のオブジェクト モデル (CSOM)、REST インターフェイス、レポート用 OData サービス、リモート イベント レシーバー、宣言型ワークフロー、および Project クライアント用作業ウィンドウ アドインなどがあります。 さらに、新しい開発には使用しないほうがよい、使用されなくなった機能についても説明します。
  
Projectサーバー 2013 は、Microsoft Office Project Server 2007 で導入され、Project Server 2010 によって拡張されます。 Projectサーバー 2013 は、Project Server Interface (PSI) からリファクタリングおよび簡略化されたクライアント側オブジェクト モデル (CSOM) を追加し、Windows アプリ、Windows Phone 8、および Microsoft Silverlight 用の JavaScript ライブラリと .NET Framework 4 ライブラリを含む。 CSOM は、Project Online向け開発用に設計され、オンプレミスのサーバー インストールProject動作します。 

Project Server データベースは 1 つのデータベースに統合されており、OData サービスでオンラインのレポート テーブルおよびビューにアクセスできます。 CSOM および OData サービスには Representational State Transfer (REST) インターフェイスが含まれます。 Projectサーバー ワークフローは、Designer 2013 SharePoint使用して作成できます。 Project Professional 2013 では、作業ウィンドウの Office アドイン拡張モデルを使用して、Project Server レポート データ、SharePoint タスク リスト、その他の外部コンテンツと統合できます。 Project Standard 2013 では、作業ウィンドウ アドインを使用して一般的な外部コンテンツと統合できます。
  
Project Server 2013 の主な変更点の図と詳細については、「Project [Server 2013 アーキテクチャ」を参照してください](project-server-2013-architecture.md)。
  
> [!NOTE]
> Project Server 2013 は SharePoint Server 2013 プラットフォームに基づいて構築され、Project 2013 には他の Office 2013 アプリケーションと同じインストラクチャが数多く含まれています。 SharePoint アドイン、SharePoint ベースのワークフロー、Web パーツ、他の SharePoint 機能を使用した開発、Office アドインのドキュメントについては[、「SharePoint](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins)アドイン[、Office](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins)アドイン、および[SharePoint 2013 開発の概要](https://msdn.microsoft.com/library/jj164084%28office.15%29.aspx)。 
  
## <a name="major-new-features-in-project-2013"></a>Project 2013 の主な新機能
<a name="pj15_WhatsNew_MajorNewFeatures"> </a>

Project Standard 2013 および Project Professional 2013 の新機能には、他の Office 2013 アプリケーションと一致し、Windows 8 のモダン スタイルのユーザー インターフェイスをサポートする改善されたユーザー インターフェイス、Office Art オブジェクトとの統合によるレポート、バーンダウン レポート、および新機能が含まれます。レポートのプログラミング機能。 Project Professional 2013 では、SharePoint Server 2013 でのプロジェクトの広範な共有と同期、および Word、Excel、Outlook などの他の Office 2013 アプリケーションにも実装されている作業ウィンドウ アドインが有効になります。
  
サーバー 2013 には多くの新機能Projectがあります。 一部のユーザーには、新しいタイムラインなどの主要なプログラミングストーリー Project Web App。 それらの機能については、Microsoft Office Online の製品のヘルプとエンド ユーザー向けドキュメント、および Microsoft TechNet の管理者と IT 担当者を対象にしたトピックに記載される予定です。 その他にも、タイムシートの向上などの新機能によって、サード パーティの開発者がタイムシートと状態管理を Project Server Interface (PSI) で容易に操作できるようになりました。
  
Project Online および Office ストア (Project アドインの追加は、Project Server が Microsoft Azure を通じてアクセスできる、大まかな変更 https://office.microsoft.com/store) です。 Project Server へのクラウドベースのアクセスでは、JavaScript を使用する Microsoft .NET Framework、Microsoft Silverlight、Windows Phone、および Web アプリを使用したアドインの開発にクライアント側オブジェクト モデル (CSOM) を使用します。 以前のバージョンProject Online 4 つのサーバー データベースProject 1 つのデータベースにマージする必要があります。
  
Projectサーバー 2013 のパフォーマンスとスケーラビリティは、タスクの状態、タイムシート、プロジェクト管理など、多くの分野で向上しています。 Projectサーバー ワークフローは、バージョン 4 のワークフロー 基盤 (WF4) Windows再設計されています。 PSI で .NET Framework 4 および Windows通信ファンデーション (WCF) を使用すると、セキュリティ、パフォーマンス、およびスケーラビリティが向上します。 たとえば、WCF ベースのアプリケーションの転送プロトコルを変更する場合、アプリケーション コードを変更して再コンパイルすることなく、構成ファイルを使用して変更できます。 Project Web Appは、データが大きく変化しない PSI 呼び出しの多くをキャッシュします。
  
> [!NOTE]
> Project Server 2013 での開発では、Office および SharePoint ツール拡張機能を使用して Visual Studio を使用できます。Office 2013 製品のアドインをネイティブに作成できます。 ProjectServer 2013 では、Visual Studioページや WCF ベースのアプリケーションなどの機能の開発を完全に有効にする必要があります。 SharePointの SharePoint Web パーツ ツール拡張機能は、Visual Studio および他の SharePoint 機能を Project Web Appおよび他の SharePoint サイトに直接SharePointできます。 
>
> Visual Studioで管理できるカスタム フィールド、ステージ、フェーズ、およびエンタープライズ プロジェクトの種類を使用する Project Project Web App Server ワークフローを開発する必要がなくなりました。 ワークフローの開発にはVisual Studio使用することができますが、多くの場合、ワークフロー デザイナーを使用して簡単かつ迅速にSharePointできます。 Visual Studio は、CSOM または他の外部 API にアクセスする必要があるワークフローを開発する際に使用できます。 
  
### <a name="project-add-ins"></a>Project アドイン
<a name="pj15_WhatsNew_Apps"> </a>

ソフトウェアの配布とマーケティングは、アドインの概念によって大きく変化してきました。 2013 Project では、アドインをパブリック Office ストアから購入およびダウンロードしたり、SharePoint のプライベート カタログ内で配布したりできます。 通常、アドインは、少数の関連タスクを実行する自己完結型の対話型プログラムです。 Project アドインには、Project Standard 2013 または Project Standard 2013 クライアントの作業ウィンドウ アドイン、Project Server 2013 または Project Online のアドインを指定できます。
  
Project デスクトップ クライアント用アドインについては、「[Project の作業ウィンドウ アドイン](#pj15_WhatsNew_Agave)」を参照してください。 サーバー 2013 Projectの例については、「Create [a SharePointホストProjectサーバー アドイン」を参照してください](create-a-sharepoint-hosted-project-server-add-in.md)。 Office および SharePoint アドイン[SDK](https://msdn.microsoft.com/library/fp161507.aspx)の記事に加えて[、Office ブログ](https://blogs.office.com/dev/)には、Project および Project Online に関連する投稿が多数含まれています。 
  
サーバー 2013 Projectアドインは、オンプレミスのインストールとインストールの両方でProject Online。 Project Server アドインには、Web パーツ、リモート イベント レシーバー、およびビジネス ロジックを含めることができます。 アドインでの Project Server オブジェクト モデルへのアクセスは、PSI ではなく CSOM を介して行われます。 データ ストレージは、SQL Azure、Microsoft Business Connectivity Services (BCS) を介した外部、ローカル データベースを使用した内部、混在などのクラウドベースのストレージを使用できます。
  
#### <a name="add-in-security"></a>アドインのセキュリティ   通常、アドインが実行可能なアクションは、アドインを実行しているユーザーに代わって実行されます。

ユーザーが明示的に偽装を使用したり、アドインを実行可能なユーザーを指定したりすることはありません。 アドインを実行しているユーザーのアクセス許可レベルを超えるアクションは、実行できません。 
  
2012 Office Developer Tools for Visual Studio では、AppManifext.xml ファイルには、アクセス許可要求スコープを設定できるグラフィカル エディターがあります。 たとえば、プロジェクト マネージャーが自らのプロジェクトを更新できるアドインを作成するには、**AppManifest.xml** デザイナー ウィンドウの [**アクセス許可**] タブで、スコープは [**複数のプロジェクト**] を、アクセス許可は [**書き込み**] を選択します。 プロジェクト マネージャーの権限を持つアドイン ユーザーは、自らが管理しているプロジェクトでアドインを実行できます。 AppManifest.xml ファイル内のコードには、以下の記述が含まれます。 
  
```XML
  <AppPermissionRequests>
    <AppPermissionRequest Scope="https://sharepoint/projectserver/projects" Right="Write" />
  </AppPermissionRequests>
```

**表 1. Project Server アドイン用のアクセス許可リクエストのスコープ**

|範囲|アクセス許可|
|:-----|:-----|
|**Project Server** <br/> |**管理** (Project Server 管理者のアクセス許可が必要)  <br/> |
|**複数のプロジェクト** <br/> |**読み取り**、**書き込み** (一部の操作にはプロジェクト マネージャーのアクセス許可が必要となり、タスクの割り当てなどの基本の読み取り操作にはプロジェクト チーム メンバーのアクセス許可が必要となります。)  <br/> |
|**1 つのプロジェクト** <br/> |**読み取り**、**書き込み** (少なくともプロジェクト チーム メンバーのアクセス許可が必要。プロジェクト内のデータにアクセスできるかどうかは、他のアクセス許可レベルに依存します。)  <br/> |
|**エンタープライズ リソース** <br/> |**読み取り**、**書き込み** (リソース マネージャーのアクセス許可が必要)  <br/> |
|**Statusing** <br/> |**提出ステータス** (プロジェクトの状態を送信するためのアクセス許可が必要)  <br/> |
|**レポート** <br/> |**読み取り** (Project Server にログオンするためのアクセス許可が必要)  <br/> |
|**ワークフロー** <br/> |**昇格** (ワークフローを実行するためのアクセス許可が必要。ワークフローでのステージ間の移行を可能にするために、アドインは管理者特権で実行されます。ステージ遷移はアドイン内のビジネス ロジックによって制御されます。)<br/> |
   
> [!NOTE]
> Projectサーバー 2013 および Project Online は、SharePoint 2013 ではアプリ専用認証モデルを使用しません (「SharePoint [2013 のアドイン承認ポリシーの種類」を参照](https://msdn.microsoft.com/library/124879c7-a746-4c10-96a7-da76ad5327f0%28Office.15%29.aspx)してください)。 
  
アドインの開発、配布、ホスティング、管理については、「SharePoint アドインと Office アドイン」、および[「SharePoint](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins) Server 2013 および[Office](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins)2013 開発者向けドキュメント」を参照してください。 他のアドインのアクセス許可要求範囲[SharePoint、2013](https://msdn.microsoft.com/library/5f7a8440-3c09-4cf8-83ec-c236bfa2d6c4%28Office.15%29.aspx)年のアドインのアクセス許可SharePoint参照してください。
  
### <a name="integrating-with-sharepoint-server"></a>SharePoint Server との統合
<a name="pj15_WhatsNew_IntegrationWSS"> </a>

Project Web App の多くの機能では、OAuth やクレーム ベース認証、SharePoint グループによる Project Server の承認とアクセス許可、SharePoint タスク リストを使用したプロジェクトの同期、Project Server 宣言型ワークフローなど、SharePoint Server 2013 の新しいインフラストラクチャが必要です。 Project Service アプリケーションは、SharePoint ファーム内の任意のサイト コレクションと関連付けることができます。 プロジェクトを SharePoint タスク リストと同期し、SharePoint でプロジェクトを維持することができます。 エンタープライズ プロジェクトを SharePoint タスク リストと同期し、Project Server がフル コントロールを維持することもできます。 アーキテクチャ図とプロジェクト同期の説明については、「Project [Server 2013 アーキテクチャ」を参照してください](project-server-2013-architecture.md)。
  
サーバー 2013 には多くの新機能SharePointがあります。 詳細については、「開発者向[けSharePoint」を参照してください](https://msdn.microsoft.com/sharepoint)。
  
### <a name="integrating-with-workflows"></a>ワークフローとの統合
<a name="pj15_WhatsNew_Workflow"> </a>

ワークフローはプロジェクト ポートフォリオ管理のコア機能です。プロジェクトのライフ サイクルには、多くのフェーズにまたがる長期間のプロセスを含めることができます。ガバナンス フェーズには、プロジェクトの提案、ビジネスへの影響度の分析、およびプロジェクトの選択、作成、計画、管理、追跡が含まれます。
  
Projectサーバー 2013 ワークフローは、WF4 を使用SharePoint 2013 ワークフロー プラットフォーム上に構築されています。 以前のバージョンとは異なり、Project Server 2013 の宣言型ワークフローは、SharePoint Designer 2013 を使用して作成できます。オンプレミスとオンラインの両方でアクセスできます。 Projectサーバー ワークフローは、OAuth SharePointワークフロー セキュリティ モデルを使用し、そのワークフロー サイトにProject Web Appできます。 図 1 は、SharePoint Designer 2013 が需要管理のサイト ワークフローにステージを追加できる点を示しています。このワークフローでは、ステージは Project Web App。
  
**図 1. SharePoint Designer を使用した Project Web アプリ用ワークフローへのステージの追加**

![SPD でのワークフローへのステージの追加](media/pj15_CreateWorkflowSPD_AddStageInSPD.gif "SPD でのワークフローへのステージの追加")

<br/>

SharePoint Designer 2013 または Visual Studio 2012 のいずれかのワークフロー ステージ、アクション、条件、その他の要素をデザイン ツールに追加することで、宣言型ワークフローを構築します。 次に、デザイン ツールはワークフローを XAML コードとして保存し、実行時に解釈されます。 宣言型ワークフローは、サーバー 2013 Projectオンプレミスまたはオンプレミスで実行Project Online。 2012 Visual Studioを使用すると、追加のコントロール用にカスタム アクションとフォームを作成し、複数のインスタンスで再利用するためにワークフロー テンプレートを保存Project Web Appできます。 SharePointDesigner 2013 では、2012 年に作成されたカスタム アクションVisual Studioできます。
  
Project Server 2013 ワークフローはアプリとして機能し、管理者 (Project Web App の設計アクセス許可を持つ管理者) は宣言型ワークフローを発行し、それをエンタープライズ プロジェクトの種類 (EPT) に関連付けます。 EPT は Project Server がフル コントロールを維持するエンタープライズ プロジェクトにする必要があります。 SharePoint タスク リストでは Project Server ワークフローを使用できません。 
  
OAuth では、プロジェクト マネージャーはプロジェクト作成権限が与えられ、偽装を使用せずにワークフローを起動できます。 Project Server へのワークフローの呼び出し、たとえば、通過する分岐を選択するためのユーザー設定フィールド値の読み取りを、プロジェクト マネージャーを代理して実行します。 自動的に次のステージに進むワークフローをプロジェクト マネージャーが作成することを防ぐため、次のワークフロー ステージに移動するための呼び出しはワークフロー作成者 (管理者) 権限で実行されます。 これに対し、従来のサーバー 2010 Project ワークフローのユーザーは、ワークフロー プロキシ ユーザー アカウントを介して偽装された呼び出しを行い、ワークフロー全体で管理者アクセス権を取得します。
  
オンプレミスProjectサーバー 2013 では、コンパイル済みの WF3.5 ベースのワークフローを使用することができますが、従来のワークフローを WF4 に基づく宣言型ワークフローにアップグレードすることをお勧めします。 最新のテクノロジは、より拡張性があり堅牢です。 ビジネス アナリストと PMO スタッフは、Visio 2013 を使用してワークフロー デザインを作成または更新し、SharePoint Designer 2013 を使用してコーディングせずに Project Server ワークフローを実装できます。
  
宣言型ワークフローを作成する方法については、「Project Web App Server ワークフローの開発の[Project」を参照してください](getting-started-developing-project-server-workflows.md)。 ワークフローのデザイナー機能と SharePoint 機能Visual Studio比較については、「ワークフローを使用して SharePoint [2013](https://msdn.microsoft.com/library/office/jj163199.aspx)ワークフローを開発する」を参照Visual Studio。
  
### <a name="client-side-object-model"></a>クライアント側オブジェクト モデル
<a name="pj15_WhatsNew_CSOM"> </a>

プログラムによるアクセスには、Project Online CSOM 上に構築された CSOM が必要SharePointです。 Project Online認証は、サーバー フォーム認証やサーバー フォーム認証Windows認証ではなく、Windows Live Project ID を使用Windowsされます。
  
サーバー 2013 の CSOM の原則とProject次に示します。
  
- CSOM は使いやすさを考慮して設計されています。 たとえば、メソッドとプロパティは、多くの  _GUID、changeXml_ パラメーターを必要としたり、データセットを渡したりするのではなく、名前でデータを直接使用または提供します。 
    
- Project Server の CSOM はサードパーティのソリューションの一般的な要件に基づいて PSI 機能のサブセットを実装します。
    
- CSOM は PSI を内部的に呼び出しますが、その構造は変わったものになっています。たとえば、すべての状態変更の更新が **StatusAssignmentCollection.SubmitAllStatusUpdates** メソッドを使用して行われるようになっており、ユーザーについては PSI メソッドの **Statusing.SubmitStatus** を使用し、その他のリソースについては **SubmitStatusForResource** メソッドを使用する、というようにはなっていません。 
    
- PSI の 22 個のパブリック サービスを使用しなくても、1 つの WCF サービス (Client.svc) で CSOM に アクセスできます。
    
- サーバー CSOM Projectの初期化は、WCF 参照またはプロキシ アセンブリを使用するのではなく、Project Web App URL を持つ[ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx)クラスを介して直接行います。 
    
- CSOM は、内部 SharePoint CSOM インフラストラクチャでサポートされる複数のクライアント ライブラリおよびインターフェイスを実装します。クライアント ライブラリおよびインターフェイスには次のものが含まれます。
    
  - Microsoft.ProjectServer.Client.dll アセンブリ内の Microsoft .NET クライアント ライブラリ
    
  - アセンブリ内の Silverlight ライブラリMicrosoft.ProjectServer.Client.Silverlight.dllします。
    
  - Microsoft.ProjectServer.Client.Phone.dll アセンブリ内の Windows Phone 8 ライブラリ
    
  - Web アプリケーション用の JavaScript ライブラリ (PS.jsファイルまたは PS.debug.js ファイル内)
    
  - OData プロトコルを使用してアクセスするための REST エンドポイント
    
  - フィルター処理によって返されるデータ量を制限できる LINQ クエリのネイティブ サポート
    
- CSOM は、PSI や Microsoft.Office.Project.Server.Library.dll などの他の Project Server アセンブリとは別に、Project Online ソリューションとオンプレミス ソリューションの両方に使用できます。
    
- Project Server 2013 CSOM の追加機能は、Project Server パートナーと開発者コミュニティからの要求に基づいて、累積的な更新プログラムとサービス パックに対して考慮される場合があります。
    
> [!NOTE]
> CSOM はサードパーティの Project Server 開発者にお勧めのインターフェイスです。新しいアプリケーションを開発する際に、対象アプリケーションに必要な機能が CSOM に含まれている場合には、CSOM を使用することをお勧めします。 
  
CSOM の開発の詳細については、「クライアント側オブジェクト モデル[(CSOM) for Project 2013」を参照](client-side-object-model-csom-for-project-2013.md)してください。 SharePoint アプリケーションの REST インターフェイスの詳細については、SharePoint 2013 開発者向けドキュメントの *「SharePoint* SharePoint REST サービスを使用したプログラミング」を参照してください。 
  
### <a name="changes-in-the-reporting-database"></a>レポート データベースの変更点
<a name="pj15_WhatsNew_RDBChanges"> </a>

Project Server 2010 の 4 つのデータベースは、Project Server 2013 の単一Projectに組み合わされます。 Project データベースの既定の名前は ProjectService です。 レポート テーブルとビューは以前の名前を保持し、下書きデータベース、発行済みデータベース、アーカイブ データベースのテーブルとビューにはプレフィックス  `draft`  `pub`  `ver` 、ProjectService データベースがあります。 たとえば、発行済みプロジェクト テーブルの名前は pub.MSP_PROJECTS です。 
  
> [!IMPORTANT]
> 下書き (プレフィックス)、発行済み ( )、アーカイブ ( ) テーブルとビューでは直接 `draft` `pub` `ver` アクセスはサポートされていません。 レポートでは、プレフィックスを持つレポート テーブルとビューのみを使用 `dbo` する必要があります。 たとえば、dbo。MSP_EpmProjectには、インスタンス内のプロジェクトの一覧がProject Web Appされます。 
>
> Project データベースのテーブルおよびビューには、プログラムによってデータベースに直接アクセスしてデータを更新することを能動的に妨げるものは存在しません。Project Professional キャッシュ、下書きおよび発行済みデータ テーブル、およびレポート テーブルはすべてがキャッシュ同期プロトコルに依存しているので、直接データを編集すると同期が混乱する可能性があることに注意が必要です。直接アクセスしてデータを変更することによって、Project Server データベースや Project Professional クライアント側キャッシュが破損した場合、製品サポートは役に立てません。 
  
Projectサーバー 2013 では、オンラインおよびオンプレミス アクセス用の OData サービスが導入されています。 オンライン レポート テーブルとビューは、OData インターフェイスによってのみ公開されます。オンプレミスで使用する場合は、OData インターフェイスを使用するか、またはレポート テーブルとビューに直接アクセスSharePointできます。 Project Onlineマルチテナント データベースはサポートされていません。 つまり、データベースの複数のインスタンスProject Web AppデータベースがProjectされます。 OData サービスは、レポート テーブルSQLクエリを内部的に実行し、XML または JSON ペイロードを提供します。 Project Server 2013 でのレポート作成のための OData サービスの概要と **ProjectData** スキーマリファレンスについては [、「ProjectData -](https://msdn.microsoft.com/library/office/jj163015.aspx)Project OData サービス リファレンス」を参照してください。
  
OData クエリの一般的な情報については [、「OData: URI の規則」を参照してください](https://www.odata.org/documentation/)。 たとえば、ブラウザーで次のクエリを使用して、プロジェクト名が "Test" で始まる Project Web App のオンプレミス インスタンス内のすべてのプロジェクトを確認できます。 ブラウザーのページを右クリックし、[**ソースの表示**] をクリックします。
  
```html
https://ServerName /ProjectServerName /_api/ProjectData/Projects?$filter=startswith(ProjectName, 'Test') eq true
```

2013 年 PowerPivot Excel にプロジェクト データをインポートするには、[データ] リボンで、[その他のソースから]ドロップダウン メニューの **[OData** データ フィードから] を選択します。 [データ **接続ウィザード] ダイアログ** ボックスで、データ フィードの場所に入力し、[次へ] を選択し、ウィザードの [テーブルの選択] ページで [プロジェクト] テーブル https://ServerName/ProjectServerName/_api/ProjectData/ を選択します。    .odc ファイルに名前を付けて保存し、[**完了**] をクリックします。 [**データのインポート**] ダイアログ ボックスで [**ピボットテーブル レポート**] を選択します。 Excel ワークシートで、表示するピボット テーブルの行と列のフィールドを選択します。
  
適切なアクセス許可を持つオンプレミスの Project Server ユーザーは、Microsoft SQL Server を通じてレポート テーブルとビューに直接アクセスして、Project Server 2010 と同様にレポートを作成できます。 サーバー 2013 Project、ユーザーは OData インターフェイスを介してオンプレミスのレポート テーブルにアクセスすることもできます。 Project Server のデータは、OData サービス用の REST エンドポイントを使用して、オンラインまたはオンプレミスで取得できます。 たとえば、dbo.MSP_PROJECT テーブルと dbo.MSP_EpmProject_UserView ビューをレポートに使用できます。 、、またはプレフィックスを持つすべてのテーブルまたはビューは、Project サーバーによる内部使用用であり、レポート `draft` `pub` `ver` の使用には使用されません。 たとえば、draft.MSP_TASKS テーブルと pub.MSP_PROJECTS_WORKING_VIEW ビューはドキュメントに記載されておらず、内部使用専用です。 
  
> [!NOTE]
> オンプレミス レポートは、別のデータベース内のテーブル、ビュー、フィールド、およびストアド プロシージャを追加して拡張できます。Project Server データベース内の既存のレポート テーブルやレポート ビューは変更しないでください。 
  
Project データベース内のレポート テーブル、ビュー、およびフィールドは、2013 SDK ダウンロードの後の更新プログラムで HTML ヘルプ ファイルProjectされます。 **ProjectData** サービスの OData XML スキーマのドキュメントについては [、「ProjectData - OData サービスリファレンスProjectを参照してください](https://msdn.microsoft.com/library/office/jj163015.aspx)。 Project Server 2010 用に作成されたレポート テーブルとビューのクエリは、ほとんどの場合、Project Server 2013 の Project データベースで動作します。 オンプレミスのユーザーは、現在と同様に SQL Server Analysis Services で Project Server OLAP キューブにアクセスできます。 Project Online では、OLAP キューブは使用できません。
  
### <a name="task-pane-add-ins-in-project"></a>Project の作業ウィンドウ アドイン
<a name="pj15_WhatsNew_Agave"> </a>

2013 Project Standard 2013 および Project Professional 2013 の両方が作業ウィンドウ アドインをサポートしています。これは、Web ページに外部コンテンツを統合して表示するために使用できます。 作業ウィンドウには、JavaScript を介してタスク、リソース、ビュー、および一般的なプロジェクト データにアクセスできる Web ページ コンテンツが表示されます。 Project の JavaScript オブジェクト モデルは、選択したタスクまたはリソースに関する情報を取得し、ガント チャートなどのビューのグリッド内の選択したセル内のデータを取得できます。 タスク ウィンドウ アドインでは、タスクProject、またはビューの選択が変更されたイベントのイベント ハンドラーを実装することもできます。 
  
図 2 は **、ProjectData** サービスを照会し、現在のプロジェクトのデータとすべてのプロジェクトの平均を比較する **Hello ProjectData** 作業ウィンドウ アドインを示しています。 2013 Project SDK のダウンロードには、アドインの完全なソース コードが含まれています。 
  
**図 2. Project Professional 内の作業ウィンドウ アドインは Project Server 内のデータにアクセスできる**

![現在のプロジェクトとすべてのプロジェクトの比較](media/pj15_RestQueryApp_CompareProject.gif "現在のプロジェクトとすべてのプロジェクトの比較")
  
> [!NOTE]
> Project Standard 2013 では、作業ウィンドウ アドインをProjectサーバー 2013 と直接統合することはできません。 
  
Project Professional の作業ウィンドウ アドインは、Project Server 2013 用に構築された Web パーツ をサポートすることができるので、開発者は Project Web App と Project Professional の両方で実行されると拡張機能をビルドできます。 他の Office 2013 製品用に開発された一般的な作業ウィンドウ アドインは、Project Standard 2013 および Project Professional 2013 でも使用できます。 詳細については、「[Task pane add-ins for Project](task-pane-add-ins-for-project.md)」を参照してください。
  
### <a name="project-server-event-receivers"></a>Project Server イベント レシーバー
<a name="pj15_WhatsNew_Events"> </a>

SharePoint ファームには、Project Web App サービス アプリケーションを含む複数の Project Web App サーバー (Web フロントエンド サーバーまたは WFEs とも呼ばれる) をProjectできます。 イベント レシーバーはイベント ハンドラーとも呼ばれます。 ローカル イベント ハンドラーを完全な信頼コードで実装し、Project Server のローカル インストールですべての WFE に展開できます。 リモート イベント レシーバーをローカルまたはリモート サーバーの Web サービスに実装して複数の WFE および複数の Project Server インストールからアクセスできます。 Project Onlineはリモート イベント レシーバーのみを使用できます。
  
Projectサーバー イベント ハンドラーは、特定SharePointページではなく、Project Web AppインスタンスごとにProject Web App 設定されます。 SharePoint サーバーの全体管理アプリケーションで、[全般アプリケーション **設定]** を選択し **、[PWA 設定]** の [管理] を選択し **、[PWA 設定]** ページの Project Web App インスタンス ドロップダウン リストでインスタンスを選択します。  ローカル イベント ハンドラーまたはリモート イベント レシーバーを追加するには、[サーバー側イベント ハンドラー **] を選択します**。
  
Project Server のオンプレミス インストールでは、CSOM の[Microsoft.ProjectServer.Client.EventHandlerCreationInformation](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCreationInformation.aspx)クラスを使用する SharePoint 機能としてリモート イベント レシーバーを作成し[、EventHandlerCollection](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCollection.aspx)クラスのメソッドを使用してプログラムによってイベント レシーバーを管理できます。 リモート イベント レシーバーではプレイベントが同期、ポストイベントは非同期であり、リモート イベント レシーバーが制御を返さない場合はタイムアウトが発生します。 
  
> [!NOTE]
> SharePoint サーバーの全体管理は、オンプレミス インストールでのみ使用できます。 オンラインProject Online SharePoint、CSOM ベースのアプリ パッケージを使用してリモート イベント レシーバーを追加または削除できます。 
  
[サーバー側イベント ハンドラー] ページで、オンプレミスの Project Server インストール用のローカル イベント ハンドラーを追加するプロセスは[、「Project Server](https://msdn.microsoft.com/library/gg615466.aspx)イベント ハンドラーを作成し、Project Server 2010 のイベント トピックを記録する」で説明されているプロセスとほぼ同じです。 違いは、[新しいイベント ハンドラー] ページに追加のオプションがある点です。 たとえば、[イベント] リスト **で [Project作成**] を **選択** し **、[NEW EVENT HANDLER] を選択します**。 [新しいイベント ハンドラー] ページで、必要なフィールドは **Name** と **Order** の 2 つのみです (図 3 を参照)。 ローカルの完全信頼イベント ハンドラーを追加する場合は、[ **アセンブリ** 名] フィールドと [クラス名] **フィールドを追加** します。[ **エンドポイント URL] は空** のままにします。 リモート イベント レシーバーを追加する場合は **、Endpoint Url** を追加し、[アセンブリ名] と [クラス **名** ] を **空のままに** します。 
  
> [!CAUTION]
> アセンブリ名/*クラス名* とエンドポイント URL の両方を指定すると、Project サーバーはローカル (オンプレミス) イベント ハンドラーのみを呼び出します。 リモート イベント レシーバーは無視されます。 
> 
> 同じイベントに 2 つのイベント ハンドラー (一方のイベント ハンドラーがローカルで、もう一方がリモート イベント レシーバー) を作成する場合、**[Order]** の値が両方とも同じであれば、Project Server はリモート イベント レシーバーを無視します。 
  
**図 3. ローカル イベント ハンドラーまたはリモート イベント レシーバーの追加**

![イベント ハンドラーまたはイベント レシーバーの構成](media/pj15_EventHandlers_NewEventHandler.gif "イベント ハンドラーまたはイベント レシーバーの構成")
    
ローカル イベント ハンドラーの PSI データセットへのアクセスが必要な場合は、[Windows]\Microsoft.NET\assembly\GAC MSIL\Microsoft.Office から Microsoft.Office.Project.Schema.dll アセンブリをコピー \_ できます。Project。Schema\v4.0_15.0.0.0__71e9bce111e9429c ディレクトリ。 

PSI の代わりに **、Microsoft.ProjectServer.Client** 名前空間でイベント クラスを使用することをお勧めします。CSOM を使用した開発では、データセットの操作は不要です。 リモート イベント レシーバーを Project Onlineするには、CSOM で[](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.Event.aspx)Event クラスと[EventHandlerCreationInformation](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCreationInformation.aspx)クラスを使用する必要があります。 
  
Project Server のテスト インストールにイベント ハンドラーをインストールし、十分にテストしてから Project Server イベント ハンドラーを展開してください。 オンプレミスの Project Server インストールの場合、追加したローカル イベント ハンドラーが動作しなく場合、Project Server 2013 Events Service は他の有効なカスタム イベント ハンドラーを読み込めない。 その場合は、問題のあるイベント ハンドラーを削除して Events Service を再起動する必要があります。
  
> [!NOTE]
> オンプレミスの Project Server インストールでイベント レシーバーを開発するには、CSOM を使用してリモート イベント レシーバーに移行することをお勧めします。リモート イベント レシーバーには Project Server Events Service 内で実行するサードパーティのコードが存在しないため、リモート イベント レシーバーの方が安定しています。ローカル管理者は、Project Server Events Service のメンテナンスを行う責任が軽減されます。 
  
イベントの一般的な情報については、「アプリでイベントを処理[する」を参照SharePoint。](https://msdn.microsoft.com/library/jj220048%28office.15%29.aspx) 
  
## <a name="deprecated-features"></a>推奨されない機能
<a name="pj15_WhatsNew_Deprecated"> </a>

> [!NOTE]
> Project Server 2016 プレビューで非推奨または削除された機能と API の詳細については、「Project Server 2016 プレビューで廃止または[削除された機能」を参照してください](https://docs.microsoft.com/project/what-s-deprecated-or-removed-in-project-server-2016)。 
  
一部のソリューションでは、Project 2013 では非推奨の機能を使用できますが、新しい開発には使用できません。 次のほとんどの機能とプラクティスは、Project Online または Project Server 2013 の既定のオンプレミス インストール (SharePoint アクセス許可モード) では動作しません。 これらの機能を使用する既存のソリューションは、Project Server 2010 からサーバー 2013 へのProject場合があります。 非推奨の機能を使用するソリューションは、場合によっては引き続き機能しますが、2013 年のすべてのインストールで完全にサポートProjectではありません。
  
お客様のソリューションで非推奨になった機能を使用する場合は、展開する前に十分にテストする必要があり、サポートされる機能が実際に使用できるようになり次第サポートされる機能を使用するように変更する必要があります。 Project アクセス許可モード用にオンプレミス Project Server 2013 セキュリティを構成する方法については、「Project [Server 2013](https://docs.microsoft.com/project/what-s-new-for-it-pros-in-project-server-2016)の IT 管理者向け新機能」の *「SharePoint* アクセス許可モード」セクションを参照してください。
  
- **拡張機能** [PSI 拡張シナリオ](https://docs.microsoft.com/previous-versions/office/developer/office-2010/ff843378(v=office.14)) は非推奨であり、今後のリリースではサポートされません。 これらのオンプレミスのサーバー Project 2013 シナリオでは、カスタム 通信ファンデーション (WCF) Windowsを使用して統合が有効になっています。 
  
- **Project PSI** PSI [Projectクラス](https://docs.microsoft.com/office/client-developer/project/project-psi-reference-overview)は非推奨です。 すべての新しい開発では、[Project CSOM](client-side-object-model-csom-for-project-2013.md) を使用してください。 ProjectProject PSI を使用するサーバー 2013 アプリは引き続き動作しますが、Project Online アプリでは、Project クラスの PSI メソッドを同等の CSOM メソッドに置き換える必要があります。
  
- **リソース 計画 PSI** リソース [計画 PSI は](https://docs.microsoft.com/previous-versions/office/project-class/gg240019(v=office.15)) 非推奨です。 引き続き 2013 Projectサポートされますが、今後のリリースではサポートされません。 
  
- **PSI の ASMX インターフェイス** PSI には、オンプレミスのサーバー拡張機能を開発するための重複インターフェイスProject含まれています。 ASMX Web サービス インターフェイスは、サーバー 2007 で PSI の最初Office Projectされました。 Projectサーバー 2010 は、オブジェクト モデルが基本的に ASMX Web サービスを複製する WCF サービス インターフェイスを追加しました。 サーバー 2013 Project ASMX と WCF の両方を引き続きサポートしますが、PSI を必要とする新しいソリューションでは WCF サービスを使用する必要があります。 可能であれば、新しいソリューションは、CSOM を使用して記述することをお勧めします。 
  
  PSI の ASMX Web サービスは、サーバー 2013 Projectで廃止されました。 Project Server の今後のバージョンで機能するために、ASMX Web サービスを使用するソリューションは、WCF サービスまたは CSOM のいずれかを使用して書き換える必要があります。 詳細については、「Project Server プログラミング」の *「Projectアプリケーション* のアップグレード [Project」を参照してください](project-server-programmability.md)。
  
- **オブジェクト リンク プロバイダー (OLP)** Project Server の以前のバージョンでは、PSI の **ObjectLinkProvider** サービス [(「WebSvcObjectLinkProvider」](https://docs.microsoft.com/previous-versions/office/ms481347(v=office.14))を参照)は、問題、リスク、成果物、およびドキュメントについて、プロジェクト サイトのエンタープライズ プロジェクト タスクと特殊な SharePoint リスト間の Web オブジェクト リンクを管理する方法を提供しています。 サーバー 2013 Projectでは、OLP は非推奨です。 
  
  SharePoint CSOM の **[RelatedItemManager](https://docs.microsoft.com/previous-versions/office/sharepoint-server/jj168020(v=office.15))** クラスを使用して、タスク リスト内のアイテムとプロジェクト サイト内の他のリスト間の Web オブジェクト リンクを作成、読み取り、および削除できます。 たとえば、タスク アイテムから問題へのリンクを追加するには **[、AddSingleLink](https://docs.microsoft.com/previous-versions/office/sharepoint-server/jj166451(v=office.15))** メソッドを使用するか **、AddSingleLinkFromUrl** または **AddSingleLinkToUrl** という 2 つの同様のメソッドのいずれかを使用できます。 **RelatedItemManager** クラスには、Web オブジェクトのリンクを削除するメソッドと、関連する項目を読み取るメソッドも含まれています。 JSOM (JavaScript オブジェクト モデル) の同等のクラスについては [、「SP」を参照してください。RelatedItemManager オブジェクト (sp.js)](https://docs.microsoft.com/previous-versions/office/sharepoint-visio/jj838582(v=office.15))。
  
  SharePoint CSOM を使用して、Project Server 2013 および Project Online のオンプレミス インストール用の OLP 型アプリを作成することをお勧Project Online。 [Microsoft.SharePoint](https://docs.microsoft.com/previous-versions/office/sharepoint-server/ms464984(v=office.15))名前空間には **RelatedItemManager** **** クラスが含まれます。 
  
- **カスタムアクセス許可** Office Project Server 2007 では、特定の Project Server の機能または拡張機能にアクセスするためのカスタム セキュリティアクセス許可がサポートされ、SDK の記事では、発行済みデータベースを直接変更して作成する方法について説明しました。 このProject Server 2010 では、カスタムアクセス許可は引き続き機能しますが、非推奨です。 このProject Server 2013 では、カスタムアクセス許可は、オンプレミスインストールSharePoint既定のアクセス許可モードでは機能しません。 アクセス許可Project、カスタムアクセス許可がサポートされています。 このProject Online、データベースへの直接アクセスはできません。 
  
- **偽装** アプリのユーザーが別の Project Server ユーザーのセキュリティアクセス許可を引き受けできる PSI ベースのアプリでの偽装は、Project Server 2013 で廃止されました。 前に示した通り、既定のオンプレミス Project Server 2013 インストールでは SharePoint アクセス許可モードが使用され、Project Server セキュリティ グループでの偽装は許可されません。 詳細については、「[Authentication, authorization, and security in SharePoint 2013](https://docs.microsoft.com/sharepoint/dev/general-development/authentication-authorization-and-security-in-sharepoint)」を参照してください。
  
  Statusing アプリケーションは、以前のバージョンのサーバーで偽装を使用した可能性がある一般的Projectです。 Projectサーバー 2010 では **、PSI に ReadStatusForResource** メソッドと **SubmitStatusForResource** メソッドが導入され **、StatusBrokerPermission** グローバルアクセス許可が追加され、別のユーザーに代わって状態の読み取りおよび更新を偽装する必要がなくなります。 Project Server 2013 の CSOM は、基になる PSI を使用して、状態の拡張機能を透過的に有効にし、Project Online またはオンプレミスのインストールに使用できます。 
  
- **レポート データベース拡張機能** レポート データベースにカスタム テーブルとビューを追加する方法は、以前のバージョンの Projectです。 Project Server 2013 は、以前のバージョンの 4 つのデータベースを 1 つのデータベースに結合します。アップグレードでは、カスタム テーブル、ビュー、または SPROC を Project Server 2013 データベース内のレポート テーブルに転送しません。 
  
  データベースのバックアップと更新を管理SQL Azure、カスタム レポート テーブルとビュー SQL Server別のレポート データベースを使用することをお勧めします。 このProject Online必須です。
  
- **レポート** サーバー データベースのローカル レポート テーブルとビュー Project OLAP キューブは非推奨であり、完全にサポートされたままです。 ただし、レポート テーブルとビュー (以前のバージョンのサーバー Project Reporting データベース) にはアクセスProject Online。 同様に、OLAP キューブは、サーバー 2013 のオンプレミス インストールProject使用できます。 レポート アプリケーションに対 **Project Online、OData** プロトコルを使用して REST クエリを使用して ProjectData サービスを使用できます。 
  
- **Projectガイド** Project ガイドは、Office Project 2007 デスクトップ アプリケーションの標準機能であり、作業ウィンドウ内の HTML および JavaScript コンテンツは、プロジェクトの作成と管理に関する対話型ガイダンスを提供します。 2010 Projectでは、Project ガイドは既定のインストールでは使用できませんが、VBA または VSTO アドインを使用して有効にできます。 2010 Project SDK のダウンロードには、変更されたガイド ファイルProject含まれています。 
  
  VBA オブジェクト モデルと **Microsoft.Office。** Project 2013 の Interop.MSProject オブジェクト モデルには **、Application** クラスの 22 のメンバーと、Project ガイドを管理できる **Project** クラスが含まれています。 ただし、Project 2013 作業ウィンドウ アプリは、Project ガイド作業ウィンドウ内のアクションと競合する可能性があります。Project ガイドのコンテンツを Office ストアで簡単に配布または販売することはできません。 カスタム ガイド コンテンツではなく、Projectアドインを使用Office作業ウィンドウ ソリューションを開発Project強く推奨します。 このガイドの詳細については、「Project [Project 2010 SDK ドキュメント」を参照してください](https://msdn.microsoft.com/library/ms512767.aspx)。
  
## <a name="comparing-project-server-on-premises-with-project-online"></a>オンプレミスの Project Server と Project Online との比較
<a name="pj15_WhatsNew_Comparing"> </a>

Project Server をオンプレミスまたは Project Online で使用するかどうか、およびどちらの場合でも開発できる拡張機能の種類を決定するために、表 2 は、Project Server 2013 のオンプレミス インストールの拡張可能な機能と Project Online を比較します。 この表 2 には、開発、管理、または使用法の相違点は記載していません。 サーバー 2013 Project Onlineおよび Projectの詳細については[、「Project 2013 for developers and Project Online」](https://developer.microsoft.com/project/docs)を[参照してください](https://developer.microsoft.com/project)。
  
**表 2. オンプレミスの Project Server と Project Online の拡張性**

| 機能 |オンプレミスの Project Server | Project Online |
|:-----|:-----|:-----|
|**プログラミング** <br/> |CSOM ベースのアプリ (一貫性のあるプログラミング モデル)  <br/>- .NET、Silverlight、Windows Phone ライブラリ  <br/>- カスタム ページ、ページ、およびリボンWeb パーツ JavaScript ライブラリ  <br/>- OData および REST プロトコル<br/><br/> PSI ベースのアプリ (複雑なプログラミング モデル) では、管理、ポートフォリオ分析、通知、Project のモードのセキュリティ、キュー システム、およびその他の領域用アプリも作成できます。<br/><br/>PSI の拡張機能  <br/><br/>Project モードのセキュリティを含むユーザー設定のアクセス許可 (非推奨)  <br/><br/>PSI による偽装 (非推奨)  <br/><br/>完全信頼コード、SharePoint ファームへの機能拡張のインストール  <br/> |CSOM ベースのアプリ (一貫性のあるプログラミング モデル)  <br/>- .NET、Silverlight、Windows Phone ライブラリ<br/>- カスタム ページ、ページ、およびリボンWeb パーツ JavaScript ライブラリ<br/>- OData および REST プロトコル<br/><br/>PSI を使用できますが、サポートされていません。OAuth 接続とサービス間接続はありません<br/><br/>CSOM API の拡張機能はありません<br/><br/>ユーザー設定のアクセス許可はありません<br/><br/>偽装はありません<br/><br/>完全信頼コードはありません  <br/> |
|**カスタム データベース** <br/> |- SQL Azure  <br/>- SQL Server (サーバー データベース内のレポート テーブルとビュー Project変更はサポートされていません)  <br/> |- SQL Azure  <br/>- SQL Server (サーバー データベース内のレポート テーブルとビュー Project変更はサポートされていません)  <br/> |
|**レポート** <br/> |- **ProjectData** サービス。OData および REST プロトコル  <br/>- サーバー データベース内のレポート テーブルProjectビュー<br/>- OLAP データベース  <br/> |- **ProjectData** サービス。OData および REST プロトコル  <br/> |
|**イベント ハンドラー** <br/> |- WCF エンドポイントからアクセス可能なリモート イベント レシーバー<br/>- 完全信頼イベント ハンドラー (ファームにSharePoint)  <br/> | - WCF エンドポイントからアクセス可能なリモート イベント レシーバー  <br/> |
|**ワークフロー** <br/> |デザイナー 2013 で作成SharePoint宣言型ワークフロー<br/>- 特定のインスタンスでのみProject Web Appする<br/>- ワークフロー デザインを 2013 年Visioできます<br/>- カスタム アクションのインポートと使用が可能<br/><br/> 宣言型ワークフロー (2012 年Visual Studio作成)<br/>- ワークフローを含めるアプリを作成する<br/>- ワークフローをSharePointできるソリューション パッケージ (.wsp) を作成する<br/>- 再利用するワークフロー テンプレートを作成する<br/>- カスタム アクションの作成と使用  <br/><br/>WF3.5 で作成された従来のコンパイル済みワークフローを使用できます (宣言型の WF4 ワークフローへのアップグレードをお勧めします)  <br/> |デザイナー 2013 で作成SharePoint宣言型ワークフロー<br/>- 特定のインスタンスでのみProject Web Appする<br/>- ワークフロー デザインを 2013 年Visioできます<br/>- カスタム アクションのインポートと使用が可能  <br/><br/>宣言型ワークフロー (2012 年Visual Studio作成)<br/>- ワークフローを含めるアプリを作成する  <br/>- ワークフローをSharePointできるソリューション パッケージ (.wsp) を作成する<br/>- 再利用するワークフロー テンプレートを作成する <br/>- カスタム アクションの作成と使用  <br/> |
|**Distribution** <br/> |- Office ストア (CSOM ベースのアプリの場合)<br/>- プライベート アプリ カタログ (SharePoint<br/>- イントラネット ファイル共有  <br/> |- Office ストア<br/>- プライベート アプリ カタログ (SharePoint  <br/> |

   
## <a name="conclusion"></a>結論
<a name="pj15_WhatsNew_Conclusion"> </a>

ProjectServer 2013 には、パートナーと顧客が大規模企業や小規模組織における Project Server の機能と機能を拡張するために使用できる豊富な新しい開発機能とシナリオが用意されています。 Office 2013 および SharePoint 2013 のインフラストラクチャを使用すると、Project 2013 のアプリを作成および配布し、カスタム アプリケーションの市場性と使用を大幅に拡張できます。 以前のバージョンの一部の機能拡張機能とプラクティスは、Project 2013 では推奨されていません。特に PSI の ASMX Web サービスと、偽装や直接データベースの変更を伴う機能 (Project Online では使用できません)。
  
CSOM の導入により、さまざまなデバイスProject Online Web アプリケーションで JavaScript を使用して、プログラムによるアクセスが可能になります。 CSOM は PSI より一貫性に優れたプログラミング モデルです。 Project Server データへのアクセス方法も、オンライン OData サービスを使用する方法や Project データベース内のレポート データ用 REST インターフェイスを使用する方法など、以前のバージョンより多様になりました。 既存のレポートは今後もオンプレミスでの利用の場合と同様の方法で使用できますが、新しいレポートはさらに柔軟性が向上しています。
  
Officeアドインは、ソリューションを販売し、2013 年Project Standard Web コンテンツなどの 2013 製品と統合Office提供します。 また、2013 年 201 Project 3 年に Project Professional Server データと SharePoint リストを作業ウィンドウまたはアドインOffice統合する新しい方法を作成することもできます。
  
アプリの開発、および SharePoint Server 2013 のプログラミング機能と CSOM の使用の詳細については、「SharePoint [for](https://docs.microsoft.com/sharepoint/dev/) developers and [Office」を参照](https://developer.microsoft.com/office/docs)してください。
  
## <a name="see-also"></a>関連項目

- [Project Server 2013 のアーキテクチャ](project-server-2013-architecture.md)  
- [Project のプログラミング タスク](project-programming-tasks.md) 
- [Project 2013 のクライアント側オブジェクト モデル (CSOM)](client-side-object-model-csom-for-project-2013.md) 
- [ProjectData - Project OData サービス リファレンス](https://msdn.microsoft.com/library/office/jj163015.aspx)  
- [Project 用の作業ウィンドウ アドイン](task-pane-add-ins-for-project.md)   
- [OData: URI の規則](https://www.odata.org/documentation/uri-conventions#FilterSystemQueryOption)    
- [SharePoint デベロッパー センター](https://msdn.microsoft.com/sharepoint)    
- [Office開発者向け](https://msdn.microsoft.com/office)   
- [アプリでイベントを処理SharePoint](https://msdn.microsoft.com/library/jj220048%28office.15%29.aspx)   
- [AppSource](https://appsource.microsoft.com/marketplace/apps?product=office)   
- [Project Online](https://developer.microsoft.com/project)
    

