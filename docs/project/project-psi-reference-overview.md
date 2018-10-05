---
title: プロジェクト PSI リファレンスの概要
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
f1_keywords:
- Admin
- Archive
- Authentication
- Calendar
- CubeAdmin
- CustomFields
- Events
- LoginForms
- LoginWindows
- LookupTable
- Notifications
- ObjectLinkProvider
- Project
- Project Server Interface
- Project Server Web services
- PSI
- PSI reference
- PSI Web services
- PWA
- QueueSystem
- Resource
- ResourcePlan
- Rules
- Security
- Statusing
- StatusReports
- TimeSheet
- Version
- View
- Web service
- Web services
- WinProj
- WssInterop
keywords:
- web サービスを予定表では、認証、Web サービス、ResourcePlan、Web サービス、StatusReports、Web サービス、PSI、名前空間、イベント ハンドラーでは、Project Server では、Web サービス、通知、QueueSystem、Web サービスでは、Project 2013 では、プラットフォーム、LoginWindows、Webサービス、Web サービスでは、状態管理、Web サービス、リソース、WinProj、Web サービス、WssInterop、Web サービス、Web サービス、Winproj、イベント ハンドラー、LookupTable、Web サービス、PWA では、Web サービス、Web サービス、セキュリティ、通知、Web サービス、Web サービスの場合は、タイムシート、Web サービス、QueueSystem、PSI では、Web サービス、Web サービス、イベント、LookupTable、バージョン、Web サービスのプログラミングの PSI Web サービス、名、Web サービス、Web サービス、PWA、PSI、リソース、Web サービス、Web サービス、ResourcePlan、タイムシート、Webサービス、Web サービス、ルール、PSI では、マネージ コードの参照、セキュリティ、Web サービス、PSI のサービス名、URL を Web、Web サービス、WssInterop、Web サービス、管理、Web 参照、PSI では、Web サービス、CubeAdmin、表示、Web サービス、予定表、Web サービス、Web表示、管理、サービス、Web サービス、LoginForms、Web サービス、Web サービス、ObjectLinkProvider、LoginForms、PSI、Url、Web サービス、アーカイブ、Web サービス、CubeAdmin、Web サービス、ルール、Web サービス、Web サービス、認証、Web サービス、PSI では、プロジェクトのサーバー、イベント、イベント、Web サービス、Web サービス、プロジェクト、状態管理、Web サービス、Web サービス、ObjectLinkProvider、Project Server のインターフェイス、メソッド、PSI では、Web サービス、StatusReports、Web サービスを Web アーカイブ、プロジェクト、Web サービス、Web サービス、LoginWindows
localization_priority: Normal
ms.assetid: d3c33089-0cbe-48c3-bfc0-0be819ca4d73
description: プロジェクト Server インターフェイス (PSI) は、Project Server 2013 の設置と統合するアプリケーションを開発するために使用する API です。
ms.openlocfilehash: 58235e16afd208d0d4415e28ad200cc7ff62ac8b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390122"
---
# <a name="project-psi-reference-overview"></a>プロジェクト PSI リファレンスの概要

プロジェクト Server インターフェイス (PSI) は、Project Server 2013 の設置と統合するアプリケーションを開発するために使用する API です。
  
この資料は、文書化されているアセンブリ、名前空間、および PSI のサービスの概要です。 [Project Server 2013 のクラス ライブラリと web サービスの参照](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx)で、SDK には、PSI と Project Server 2013 で[Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx)名前空間のマネージ コードのドキュメントをすべて含まれています。 オンライン プロジェクト用のアプリケーションを開発するには、PSI ではなく**Microsoft.ProjectServer.Client**名前空間を使用してください。 

Project Server 2013 の PSI には、デュアル インターフェイスがあります。 検出 web サービスの ASMX インターフェイスが定義されているし、ファイルを Web サービス記述言語 (disco と WSDL)、 `https://ServerName/ProjectServerName/_vti_bin/psi/` (Projectdisco.aspx や Projectwsdl.aspx など) の仮想ディレクトリです。 ASMX インターフェイスは、Project Web App の設置型インストールの URL を通じてのみアクセスできます (たとえば、 `https://ServerName/ProjectServerName/_vti_bin/psi/project.asmx?wsdl)`。 ブラウザーで web サービスを表示する必要があります、 `?wsdl` [URL] です。 ASMX インターフェイスが構築されるため Windows Communication Foundation (WCF) インフラストラクチャを使用して、Project Server の web サービスの .asmx ファイルは実際にありません PSI の仮想ディレクトリ。 
  
WCF サービスのインタ フェースがバックエンド内の .svc ファイルで定義されている`https://ServerName:32843/GUID/PSI/`、SharePoint Web サービス アプリケーションの仮想ディレクトリです。 プロジェクト サービス アプリケーションの仮想ディレクトリの URL の PSI サービス (たとえば、 `https://ServerName:32843/GUID/PSI/project.svc`)、.svc ファイルが含まれています。 ただし、WCF サービス参照を設定するのには、バックエンドの URL を直接使用できません。 アプリケーションや PSI の WCF サービスを使用するコンポーネントを開発するには、プロキシ アセンブリまたはプロキシ ファイルを使用できます。 Project 2013 SDK ダウンロードには、Project Server 2013 では、[WCF サービスのプロキシ ファイルが含まれていて、WCF プロキシの更新されたファイルを取得して、ファイルがプロジェクトのより新しいサーバーのプロキシ アセンブリにコンパイルするのにはスクリプトを作成します。
  
プロジェクト サービス アプリケーションのディレクトリ名は、オンプレミスの Project Web App インスタンスの GUID と同じでは、GUID の値です。 **インターネット インフォメーション サービス (IIS) マネージャー** ] ウィンドウで、 **SharePoint Web サービス**] ノードを展開し、GUID のディレクトリ名を選択し、**仮想パス**の値をコピーするのには **[詳細設定**します。 
  
> [!IMPORTANT]
> PSI の ASMX web サービスのインタ フェースは、Project Server 2013 のでは使用されなくなりましたはまだサポートされています。 新しいアプリケーションは、PSI または、CSOM の WCF インターフェイスを使用する必要があります。 非推奨の機能の詳細については、 [Project 2013 の開発者用の更新プログラム](updates-for-developers-in-project-2013.md)を参照してください。
> 
> 新しいアプリケーション、およびプロジェクトのサーバーの設置型インストールでのみ実行されるミドルウェア コンポーネントは、ネットワーク通信のことをお勧めするテクノロジは、WCF インターフェイスの使用してください。 ASMX インターフェイスを使用するレガシ アプリケーションは、Project Web App は、Project Server のアクセス許可のチェックを使用して URL を使用する必要があります。 
> 
> ASMX インターフェイスおよび WCF インターフェイスを使用する方法の詳細については、[プロジェクト内の ASMX ベースのコード サンプルの前提条件](prerequisites-for-asmx-based-code-samples-in-project.md)と[プロジェクト内の WCF ベースのコード サンプルの前提条件](prerequisites-for-wcf-based-code-samples-in-project.md)を参照してください。 
  
WCF インターフェイスを使用するアプリケーションを開発するためには、Visual Studio 2010 または Visual Studio 2012 を使用できます。 Project Server の宣言型ワークフローを作成するには、SharePoint Designer 2013 を使用できます。 Visual Studio 2012 では、PSI または、CSOM へのアクセスを必要とするプロジェクトのサーバーのワークフローを開発できます。
  
### <a name="using-the-psi-reference"></a>PSI リファレンスの使用
<a name="pj15_PSIRefOverview_Using"> </a>

PSI オブジェクト モデルは、大規模なと多くのクラスおよびメンバーは内部使用のみ。 その結果、 [Project Server 2013 のクラス ライブラリと web サービスの参照](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx)するトピックを検索するのには混乱を招く場合ができます。 開発のために使用するリファレンス トピックのほとんどは、次のグループには。
  
- **プライマリ クラスのメソッド:** PSI の各サービスには、サービスの名前の名前は主クラスが含まれています。 たとえば、**リソース**サービスには、[リソース](https://msdn.microsoft.com/library/WebSvcResource.Resource.aspx)クラスには、 [WebSvcResource](https://msdn.microsoft.com/library/WebSvcResource.aspx)名前空間にが含まれています。 **リソース**クラスで使用可能なメソッドの一覧を表示するには、コンテンツ ペインで [クラス] ノードを展開して**リソース メソッド**のトピックを選択します。 
    
- **DataRow プロパティ:** プライマリ クラスのメソッドの多くを使用して、または、**データセット**を返します。 **データセット**内のそれぞれの**DataTable**オブジェクトには、1 つまたは複数の**DataRow**オブジェクト内のデータが含まれています。 ほとんどの場合は、 **DataSet**や**DataTable**、 **DataRow**クラスの他のメンバーのすべての行プロパティのみを参照してくださいする必要があります。 たとえば、 **ResourceAssignmentDataSet**クラスには、 **ResourceAssignmentDataTable**と[ResourceAssignmentDataSet.ResourceAssignmentRow](https://msdn.microsoft.com/library/WebSvcResource.ResourceAssignmentDataSet.ResourceAssignmentRow.aspx)クラスのサブクラスが含まれています。 **ResourceAssignmentRow**クラスに含まれるプロパティの一覧を表示するには、コンテンツ ペインで [クラス] ノードを展開し、 **ResourceAssignmentDataSet.ResourceAssignmentRow プロパティ**のトピックを選択し、します。 
    
サービスの名前空間だけでなく、 [Project Server 2013 のクラス ライブラリと web サービスの参照](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx)トピックへのリンクのサード ・ パーティ製ソリューションの開発で使用されている 3 つの Project Server アセンブリ設置型インストールします。 これらのアセンブリに、最小限のドキュメントのみを提供しています。 PSI リファレンスでは、主要なクラスおよび 23 の公開サービスのメンバーを説明します。 6 つの PSI サービスは、内部使用のみと、文書化されていません。 
  
> [!NOTE]
> クライアント側オブジェクト モデル (CSOM) 内のクラスは、他の Project Server アセンブリおよびサービスから独立して使用できます。 **Microsoft.ProjectServer.Client**名前空間を Project Server コンピューターからリモートの開発環境で使用し、プロジェクトをオンラインで、または Project Server のオンプレミスのインストールと統合するアプリケーションを開発できます。 ですが、完全な PSI の機能のサブセットが、CSOM に含まれています。 CSOM は、Project Server の統合のための最も一般的なシナリオの開発を有効にします。 詳細については、[どのような CSOM は行われない](what-the-csom-does-and-does-not-do.md)し、 [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx)を参照してください。 
  
PSI を使用するほとんどのアプリケーションの開発は、Project Server コンピューター上で開発または Project Server アセンブリへの参照をグローバル アセンブリ キャッシュに設定する必要はありません。 必要な Project Server アセンブリを開発用コンピューターにコピーできます。 Project Server 2013 の _[プログラム ファイル]_ で、次のアセンブリをインストールする`\Microsoft Office Servers\15.0\Bin`。 
  
- Microsoft.Office.Project.Server.Events.Receivers.dll 
- Microsoft.Office.Project.Server.Library.dll
- Microsoft.Office.Project.Server.Workflow.dll
    
PSI サービスの名前空間には、マニュアルの目的で生成される、ProjectServerServices.dll、PSI プロキシ アセンブリ用に作成された任意の名前があります。 PSI リファレンスでは、各サービスの名前空間があり、プレース ホルダー名 ( _[プロジェクトの web サービス]_) などの web 参照 (次のように`https://ServerName/ProjectServerName/_vti_bin/psi/Project.asmx?wsdl`)。 
  
## <a name="project-server-assemblies-and-namespaces"></a>Project Server のアセンブリと名前空間
<a name="pj15_PSIRefOverview_Assemblies"> </a>

プロジェクト サーバーをインストールするときに、多くのアセンブリがインストールされています。Project Server アセンブリの 4 つのだけが記載されています。 サード パーティの開発者では、それらのアセンブリに、いくつかのクラスとメンバーのみを通常使用します。 文書化されていない Project Server アセンブリには、名前空間、および Project Server は Project Web App で、ビジネス エンティティのクラスなどは内部で使用するクラスが含まれて、データ アクセス層 (DAL) とします。 Visual Studio で文書化された Project Server アセンブリのいずれかに参照を設定するときは、名前空間、クラス、および Visual Studio のオブジェクト ブラウザーのメンバーのすべてを表示できます。
  
> [!NOTE]
> 文書化されている Project Server の名前空間の多くのメンバーも内部使用専用で、ドキュメントは最小限です。 
  
オンライン プロジェクトを開発する場合は、Project Server の機能にアクセスするのには CSOM のみを使用できます。 PSI サービスまたはその他の Project Server アセンブリへのアクセス権がありません。
  
[Project Server 2013 のクラス ライブラリと web サービス参照](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx)の PSI には、次のアセンブリから名前空間が含まれます。 
  
- **Microsoft.Office.Project.Server.Library.dll**このアセンブリに含まれる 1 つの文書化された名前空間と 3 つの文書化されていない名前空間は、次のようになります。 
    
  - [Microsoft.Office.Project.Server.Library](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.aspx)名前空間には、Project Server のオンプレミス アプリケーションに多くの列挙体、およびクラスのフィールドおよび頻繁に使用されるプロパティが含まれます。 たとえば、開発者は通常**CustomField.Type**、 **PSClientError**、 **PSErrorInfo**、および**フィルター**のクラスなどの列挙体を使用します。 
    
    **Microsoft.Office.Project.Server.Library** 名前空間には、次の 7 つのプロパティ クラスと、3,200 以上のサブクラスも含まれます。 
    
      - **AssignmentProperties**  
      - **CalendarProperties**
      - **ConstraintProperties**
      - **LookupTableProperties**
      - **「プロジェクトプロパ ティー」**
      - **ResourceProperties**
      - **TaskProperties**
    
    プロパティ クラスは、内部的に使用され、文書化されていません。 プロパティ クラスは、評価のためのプロジェクトとプロジェクトのサーバー間のシリアル化に使用されます。 Visual Studio で**Microsoft.Office.Project.Server.Library**名前空間を使用するすべてのサードパーティの開発のために便利なクラスを見つけることが難しくなりますプロパティ クラス オブジェクト ブラウザーが表示されます。 プロパティ クラスを使用するサード パーティの開発者がいないため SDK はしない文書化します。 
    
  - **Microsoft.Office.Project.Server.DataServices**クラスと、この名前空間のメンバー内部的に使用されますプロジェクトをオンラインでの**OData**サービスがプロジェクト データベース内のレポートのテーブルにアクセスするためです。 **DataServices**クラスは記載されていません。 
    
  - **Microsoft.Office.Project.Server.Administration**クラスと、この名前空間のメンバーは、の診断ログは、内部的に使用され、文書化されていません。 
    
  - **Microsoft.Office.Project.Server.Base**クラスと、この名前空間のメンバーの基本クラスとして内部的に使用され、文書化されていません。 
    
  - **Microsoft.Office.Project.Server.Library.FilterSchema**この名前空間はフィルターのスキーマを生成する内部で使用され、文書化されていません。 
    
- **Microsoft.Office.Project.Server.Workflow.dll**このアセンブリは、Project Server 2013 で作業を続けることを従来の Project Server 2010 のワークフローに使用されます。 新しいワークフローを作成するには、SharePoint Designer 2013 を使用する必要があります。 または[Microsoft.ProjectServer.Client.WorkflowActivities](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.WorkflowActivities.aspx)クラスを Visual Studio 2012 を使用することもできます。 Microsoft.Office.Project.Server.Workflow.dll アセンブリには、次の 3 つの名前空間が含まれています。 
    
  - [Microsoft.Office.Project.Server.Workflow には](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Workflow.aspx)この名前空間には、Project Server のワークフロー活動で使用されるクラスが含まれています。 アクティビティには、データの読み取りと比較すると、プロジェクトのプロパティの更新が含まれます。 他のクラスは、ワークフローを管理し、プロジェクトが変更されるとバックアップ ・ ワークフローの呼び出しが含まれます。 
    
  - **Microsoft.Office.Project.PWA には**この名前空間には、Project Web App とカスタム ワークフロー アクティビティを使用するため、PSI の内部のプロキシが含まれていますそれが文書化されていません。 
    
    ユーザー定義ワークフロー活動には、すべての PSI サービスのクラスにアクセスするための**Microsoft.Office.Project.PWA**への参照が必要です。 たとえば、 **Microsoft.Office.Project.PWA.PSI**クラスには、 [WebSvcProject](https://msdn.microsoft.com/library/WebSvcProject.aspx)名前空間のプロキシを取得する、 **ProjectWebService**プロパティが含まれています。 
    
  - **Microsoft.Office.Project.Server.WebServiceProxy には**この名前空間には、各 PSI サービスのプライマリ クラスの内部のプロキシ クラスが含まれます。 ワークフロー ユーザーの昇格されたアクセス許可を使用すると、ワークフローは、プロキシ クラスを通じて PSI メソッドを呼び出すことができます。 プロキシ クラスは記載されていません。 
    
- **Microsoft.Office.Project.Server.Events.Receivers.dll**[Microsoft.Office.Project.Server.Events](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.aspx)は、このアセンブリ内で唯一の名前空間です。 イベント レシーバーと PSI サービス用のイベント引数クラスおよびその他の内部クラスが含まれています。 
    
  開発者は、イベント レシーバーのクラスを継承するイベント ハンドラーを作成します。PSI サービスのプライマリ クラスの多くには、対応するイベント レシーバー クラスがあります。たとえば、**ProjectEventReceiver** クラスには、PSI の **Project** クラスのメソッドに対応するプレイベント レシーバー メソッドとポストイベント レシーバー メソッドが含まれます。**OnCreating** メソッドと **OnCreated** メソッドは、**QueueCreateProject** メソッドのプレイベント レシーバー メソッドおよびポストイベント レシーバー メソッドです。 
    
  開発者は、通常、次のイベント レシーバー クラスを使用します。
  <br/>  
  - [AdminEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.AdminEventReceiver.aspx)
  - [CalendarEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.CalendarEventReceiver.aspx)
  - [CubeAdminEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.CubeAdminEventReceiver.aspx)
  - [CustomFieldsEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.CustomFieldsEventReceiver.aspx)
  - [LookupTableEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.LookupTableEventReceiver.aspx)
  - [ProjectEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.ProjectEventReceiver.aspx)
  - [OptimizerEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.OptimizerEventReceiver.aspx)
  - [ReportingEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.ReportingEventReceiver.aspx)
  - [ResourceEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.ResourceEventReceiver.aspx)
  - [SecurityEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.SecurityEventReceiver.aspx)
  - [StatusingEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.StatusingEventReceiver.aspx)
  - [TimesheetEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.TimesheetEventReceiver.aspx)
  - [UserDelegationEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.UserDelegationEventReceiver.aspx)
  - [WorkflowEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.WorkflowEventReceiver.aspx)
  - [WssInteropEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.WssInteropEventReceiver.aspx)
    
  **RulesEventReceiver**クラスと**StatusReportsEventReceiver**クラスは、Project Web App で内部的に使用されます。 
    
- **Microsoft.ProjectServer.Client.dll には**このアセンブリには、.NET Framework 4 での開発の CSOM が含まれています。 アセンブリである`%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\ISAPI\Microsoft.ProjectServer.Client.dll`。 **Microsoft.ProjectServer.Client**名前空間を持つアプリケーションの開発では、アプリケーションが使用するいずれかの設置、設置型のプロジェクトのサーバー Api、およびサービスの独立した、または Project Server のオンライン インストールします。 関連する CSOM web アプリを使用して Windows Phone 8、マイクロソフトの Silverlight、または JavaScript を使用することができるアセンブリは、 [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx)を参照してください。 
    
- **Microsoft.Office.Project.Server.Schema.dll** 「Project 2013 SDK は、 **Microsoft.Office.Project.Server.Schema**名前空間内にある文書化されません、`[Windows]\Microsoft.NET\assembly\GAC_MSIL\Microsoft.Office.Project.Schema\v4.0_15.0.0.0__71e9bce111e9429c\Microsoft.Office.Project.Schema.dll`のアセンブリです。 名前空間には、PSI で使用されているすべての**データセット****データ テーブル**の**DataRow**クラスと Project Server が内部的に使用する多くの他の類似したクラスの定義が含まれています。 各 PSI サービスのパブリック クラスは、特定のサービスの参照に記載されています。 たとえば、 **DriverDataSet.DriverRow**クラスは、 [WebSvcDriver](https://msdn.microsoft.com/library/WebSvcDriver.aspx)名前空間に記載されています。 
    
  > [!NOTE]
  > CSOM を使用して、リモート イベントのハンドラーを使用して、またはオンラインのプロジェクトにアクセスするアプリケーションでは、 **Microsoft.Office.Project.Server.Schema**名前空間は使用しません。 
  
  イベント ハンドラーが Project Server コンピューターにインストールされる完全信頼イベント ハンドラーを使用する一部のアプリケーションでは、Microsoft.Office.Project.Schema.dll アセンブリへの参照を設定する必要があります。次に、2 つの例を示します。
    
  - ユーザー設定フィールド用の完全信頼 **OnCreated** ポストイベント ハンドラーでは、**e.CustomFieldInformation** イベント引数を、**CustomFieldDataSet** および **CustomFieldsRow** の定義に対する **Microsoft.Office.Project.Server.Schema** 名前空間への参照と共に使用できます。 
   
     ```cs
        using PSLibrary = Microsoft.Office.Project.Server.Library;
        using Microsoft.Office.Project.Server.Schema;
        . . .
        // Event handler for the OnCreated event of a custom field.
        public override void OnCreated(
            PSLibrary.PSContextInfo contextInfo, 
            CustomFieldsPostEventArgs e)
        {
            // Get information from the event arguments. 
            string userName = contextInfo.UserName.ToString();
            CustomFieldDataSet customFieldDs = e.CustomFieldInformation;
            CustomFieldsRow customFieldRow = customFieldDs.CustomFields.Rows[0];
            string customFieldName = customFieldRow["MD_PROP_NAME"].ToString();
            byte customFieldType = (byte)customFieldRow["MD_PROP_TYPE_ENUM"];
            Guid customFieldUid = (Guid)customFieldRow["MD_PROP_UID"];
            . . .
        }
     ```

  - カスタム ワークフロー アクティビティでは、**DataSet** の定義に対する **Microsoft.Office.Project.Server.Schema** への参照が必要な場合があります。 
    
## <a name="psi-services"></a>PSI サービス
<a name="pj15_PSIRefOverview_PSI"> </a>

PSI は、WCF サービスおよび Project Server 2013 の同一の ASMX web サービスのセットです。 URL への参照を設定する、Visual Studio プロジェクトで、サービスを使用する、`.svc`ファイルまたは`.asmx?wsdl`、ネームの任意の名前を使用してサービス。 Wsdl.exe ユーティリティまたは svcutil.exe ユーティリティ、その名前空間のプロキシ ソース コードを生成し、コンパイラは、アプリケーションに含めるプロキシ サービス アセンブリを作成します。 
  
> [!NOTE]
> PSI リファレンスには、 _[web サービスの管理]_、 _[ドライバーの web サービス]_、 _[プロジェクトの web サービス]_ などの PSI サービスのネーム名プレース ホルダーにはが含まれています。 各 PSI ネームには、そのサービスの web メソッドが含まれる主なクラスが含まれています。 などの**管理**サービスへの参照を設定して、 **WebSvcAdmin**という名前を付けますし、 **WebSvcAdmin**アプリケーションでネームが含まれています**GetServerCurrency**の web メソッドを持つプライマリ**管理**クラスには**ListInstalledLanguages**、 **ReadServerVersion**というように。 非推奨の PSI サービスの一覧については、 [Project 2013 の開発者用の更新プログラム](updates-for-developers-in-project-2013.md)を参照してください。 
  
30 の合計の PSI サービスの**認証**、 **ExchangeSync**、 **OData**、 **P12Upgrade**、 **psiserviceapp**、 **PWA**、**ビュー**、および**WinProj**は、Project Web App およびプロジェクトによって内部で使用プロフェッショナルとは記載されていません。 プロキシ ファイルまたは PSI の内部サービスが含まれているプロキシ アセンブリを作成できますが、内部サービス用ではないサードパーティ製の使用中です。PSI リファレンスは、これらのサービスを文書化されません。 次の図は、インターネット インフォメーション サービス マネージャーで、バックエンドの PSI サービスの場所を示しています。 
  
**IIS の PSI サービスを検索します。**

![IIS マネージャーでの PSI サービス](media/pj15_PSIReference_IIS.gif "IIS マネージャーでの PSI サービス")
  
PSI サービスの Web メソッドを含むすべてのクラスは次のとおりです。
  
1. [管理](https://msdn.microsoft.com/library/WebSvcAdmin.Admin.aspx)Project Web App で**プロジェクトのサーバーの管理**] ページで使用されるメソッドが含まれています。 レポートの期間では、監査ログ、および Active Directory の設定、状態管理と通貨の設定を管理、会計年度を定義します。 
    
2. [アーカイブ](https://msdn.microsoft.com/library/WebSvcArchive.Archive.aspx)プロジェクト、セキュリティのカテゴリ、ユーザー設定フィールド、リソース、システム設定、ビュー、およびエンタープライズ グローバル プロジェクトのバックアップと復元を管理するメソッドが含まれています。 読み取り、アーカイブ スケジュールを更新します。 すべてのプロジェクトをアーカイブまたは指定されたアーカイブ済みのプロジェクトを削除します。 アーカイブ データベースのテーブルおよび発行済みデータベースのテーブルへのオブジェクトのバックアップをリストアするには、バックアップ ・ オブジェクトを保存します。 
    
3. **認証**Project Professional および Project Web App だけで内部的に使用するメソッドが含まれています。 
    
4. [予定表](https://msdn.microsoft.com/library/WebSvcCalendar.Calendar.aspx)エンタープライズ カレンダーの例外を管理します。 チェック アウトし、リソース カレンダーでチェックします。 作成、削除、すべてを一覧表示、更新、またはカレンダーの例外を返します。 
    
5. [CubeAdmin](https://msdn.microsoft.com/library/WebSvcCubeAdmin.CubeAdmin.aspx)OLAP キューブの設定を管理します。 分析サーバー、データベースの状態、およびキューブの一覧を取得します。 キューブ作成サービスの要求をキューに置きます。 読み取り、計算されるメンバー定義、およびキューブのディメンションとメジャーのフィールドの設定を更新します。 
    
6. [名](https://msdn.microsoft.com/library/WebSvcCustomFields.CustomFields.aspx)エンタープライズ ユーザー設定フィールドを管理します。 チェック アウトが含まれていて、メソッド、および作成、読み取り、更新、およびエンタープライズ ユーザー設定フィールドの削除 (CRUD) メソッドをチェックインします。 
    
7. [ドライバー](https://msdn.microsoft.com/library/WebSvcDriver.Driver.aspx)ポートフォリオ分析のドライバーとプロジェクトの作成と要求の管理のためのドライバーの優先順位付けを管理します。 プロジェクトのドライバーの CRUD メソッドが含まれています。 
    
8. [イベント](https://msdn.microsoft.com/library/WebSvcEvents.Events.aspx)Project Server イベント ハンドラーの関連付けを管理します。 Project Server イベント ハンドラーの関連付けの特定のイベントまたはイベント ハンドラーの関連付けをすべての CRUD メソッドが含まれています。 
    
9. **ExchangeSync**これは、Exchange Server のイベントを処理する内部のプロジェクトのサーバー サービスです。 Project Web App では、 **ExchangeSync**を使用して、Office Project Server 2007 と Outlook クライアントと直接同期する代わりに、Project Server と Exchange Server の間の割り当てを同期します。 
    
    **ExchangeSync** サービスへのアクセスは、**ProjectServiceApplication** URL を使用してだけ行えます。**ExchangeSync** のクラスとメンバーは、サードパーティの開発用としてはサポートされていません。 
    
10. [LoginForms](https://msdn.microsoft.com/library/WebSvcLoginForms.LoginForms.aspx)フォーム ベース認証での**ログイン**と**ログオフ**の方法を提供します。 **LoginForms**サービスへのアクセスは、Project Web App サイトをフロント エンド サーバー上でのみ使用できます。 
    
11. [LoginWindows](https://msdn.microsoft.com/library/WebSvcLoginWindows.LoginWindows.aspx)ASMX ベースのアプリケーションの複数の認証と Windows 認証に使用される**ログイン**と**ログオフ**の方法が用意されています (要求およびフォーム ベース) Project Server 2013 のインストールします。 **LoginWindows**サービスへのアクセスは、Project Web App サイトをフロント エンド サーバー上でのみ使用できます。 
    
    > [!CAUTION]
    > **LoginWindows** サービスは、WCF ベースのアプリケーションや、クレーム認証または **OAuth** のみを使用する Project Server インストールで実行するアプリケーションでは使用されません。これらの場合は、**Login** メソッドは常に **false** を返します。クレーム認証は統合 Windows 認証を処理します。 
  
12. [LookupTable](https://msdn.microsoft.com/library/WebSvcLookupTable.LookupTable.aspx)参照テーブル、多言語参照テーブル、およびその対応するコード マスクを管理します。 チェック アウト、チェックイン、読み取り、作成、削除、更新します。 
    
13. [通知](https://msdn.microsoft.com/library/WebSvcNotifications.Notifications.aspx)通知と事前通知を管理します。 取得、設定、登録、および通知結果の登録を解除するメソッドが含まれています。 
    
14. [ObjectLinkProvider](https://msdn.microsoft.com/library/WebSvcObjectLinkProvider.ObjectLinkProvider.aspx)Web オブジェクトとドキュメントと SharePoint サイト上のリスト アイテムへのリンクを管理します。 作成、削除、または、プロジェクト、プロジェクト リンク、タスク、またはタスクにリンクされた web オブジェクトを読み込みます。 
    
    > [!NOTE]
    > **ObjectLinkProvider**サービスは、Project Server 2013 で使用されていません。 詳細については、[ [Project 2013 の開発者用の更新プログラム](updates-for-developers-in-project-2013.md)の*非推奨機能*のセクションを参照してください。 
  
15. **OData**レポート テーブルおよびビューの内部の**OData**インターフェイスを提供します。 **OData**サービスへのアクセスは、バックエンド**ProjectServiceApplication** URL を通じてのみ使用できます。 PSI でプライベートの**OData**サービスは、 **ODataClient.ProcessOdataMessage**、レポートのデータに対する要求を処理するのには Project Server を内部的に使用する 1 つのメソッドを提供します。 **ProjectData**サービスをフロント エンド サーバーにより HTTP 要求を行います。 
    
    **ProjectData**サービスおよびレポートのデータを読み取るための OData プロトコルについては、 [ProjectData - プロジェクトの OData サービスの参照](https://msdn.microsoft.com/library/office/jj163015.aspx)を参照してください。
    
16. **P12Upgrade**Office Project Server 2007 インストールをアップグレードするのには Project Server 2013 のインストーラーの内部メソッドを提供します。 **P12Upgrade**サービスへのアクセスは、 **ProjectServiceApplication**の URL からのみ使用できます。 **P12Upgrade**メソッドは、サードパーティの開発はサポートされていません。 
    
17. [PortfolioAnalyses](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.aspx)オプティマイザー、プランナー、および分析ソリューションのプロジェクトの依存関係の CRUD メソッドが含まれています。 
    
18. [プロジェクト](https://msdn.microsoft.com/library/WebSvcProject.Project.aspx)プロジェクトを管理します。 チェック アウト、チェックイン、作成、削除を読み取ると、またはプロジェクトの下書きデータベース テーブルまたはパブリッシュされたテーブル内のプロジェクトを更新します。 発行のためにキューにメッセージを配置します。 
    
    作成または (タスク、リソース、割り当て、およびなど)、プロジェクト内のエンティティを削除します。 情報を取得または、プロジェクト チームまたはプロジェクトのサイト アドレスを更新します。 リソースが割り当てを持つプロジェクトのステータス、ドラフトのテーブル、すべてのサマリー タスク、指定されたリソースへの割り当てに利用可能なタスクまたはすべてのプロジェクト内のプロジェクトの一覧を取得します。
    
    コミットメントを作成および管理したり、SharePoint タスク リストからプロジェクトの提案とプロジェクトを作成したり、プロジェクト/マスター プロジェクトの関係を検索したりします。
    
19. **psiserviceapp**プロジェクトをオンラインで内部的に使用します。 **Psiserviceapp**クラスおよびメンバーは、サードパーティの開発はサポートされていません。 
    
20. **PWA**タスク更新承認ルールと進捗レポートを管理するためのメソッドを含む、Project Web App に対して最適化された多くのメソッドが含まれています。 **PWA**メソッドが特別なことがよくありますし、少し冗長に他の PSI サービスと同じメソッドと比較します。 **PWA**メソッドを使用して、または、他の PSI メソッドと同じデータセットの多くを取得します。 
    
    **PWA** サービスへのアクセスは、**ProjectServiceApplication** URL を使用してだけ行えます。**PWA** のクラスとメンバーは、サードパーティの開発用としてはサポートされていません。 
    
21. [QueueSystem](https://msdn.microsoft.com/library/WebSvcQueueSystem.QueueSystem.aspx)Project Server キューを管理します。 指定されたプロジェクトのジョブ数、ジョブやジョブ グループの待ち時間、すべてのジョブ、指定されたジョブ、呼び出し元が所有するジョブまたはジョブのステータスを取得します。 ジョブの相互関係を管理し、キューを構成します。 
    
22. [リソース](https://msdn.microsoft.com/library/WebSvcResource.Resource.aspx)エンタープライズ リソースを管理します。 チェック アウト、チェックイン、更新、またはリソース、または Project Server のユーザーと、承認の設定を作成します。名前または GUID でリソースを検索します。リソースまたはユーザー データとリソース分割構造 (RBS) と関連するセキュリティ情報を読み取りますリソースに対するすべての割り当てを取得します。およびユーザーのパスワードをリセットします。 **リソース**クラスには、ユーザーの委任の CRUD メソッドが含まれています。 
    
23. [ResourcePlan](https://msdn.microsoft.com/library/WebSvcResourcePlan.ResourcePlan.aspx)リソース計画を管理します。 チェック アウト、チェックイン、発行、およびリソース計画の CRUD メソッドが含まれています。 
    
24. [セキュリティ](https://msdn.microsoft.com/library/WebSvcSecurity.Security.aspx)セキュリティ テンプレート、セキュリティ カテゴリ、組織、およびグローバル アクセス許可、およびグループのアクセス許可の CRUD メソッドが含まれています。 **セキュリティ**クラスには、プロジェクトのカテゴリのメソッドが含まれています。 
    
25. [状態管理](https://msdn.microsoft.com/library/WebSvcStatusing.Statusing.aspx)ステータスの更新と割り当てを管理します。 進捗の更新または承認を適用、送信のステータスを更新、送信された更新のサマリー情報を設定、承認済みの更新プログラムまたは特定のユーザーの承認履歴を削除または一連のプロジェクトのすべての状態情報を削除します。 作成、取得、またはデリゲートの割り当てです。割り当ての作業期間を設定します。 現在のユーザーの新しい割り当てを取得します。割り当てまたはタスクのトランザクション履歴、時間単位の実績、またはサマリー タスク階層を取得します。 
    
    タイムシート データをプレビューまたはインポートしたり、ユーザーの稼働日および非稼働日のスケジュールを読み取ったりします。承認待ちの進捗状況の更新、提出された更新の情報、または提出された更新に含まれる変更のトランザクション レコードを検索します。チームの状態を読み取ります。
    
26. [タイムシート](https://msdn.microsoft.com/library/WebSvcTimeSheet.TimeSheet.aspx)タイムシートを管理します。 タイムシートの CRUD メソッドが含まれていて、またはタイムシートを取り消します。 や承認の保留中の遅延はタイムシートを検索します。日付または期間でタイムシートを検索します。 タイムシート承認者のリストを取得します。 タイムシートの実績作業時間をプリロードし、タイムシート行を検証します。 **タイムシート**のクラスには、 **ReadProjectTimesheetLines**メソッドと**SubmitTimesheetLines**メソッドの読み取りと、偽装を必要とせず、別のリソースのタイムシートを送信するが含まれています。 
    
27. **ビュー**サービスの**表示**は、Project Web App 内でのみ使用するよう設計されています。 **ビュー**クラスのメソッドは、ビューの管理しレポートを表示し、ビュー内のフィールドを参照します。 
    
    **View** サービスへのアクセスは、**ProjectServiceApplication** URL を使用してだけ行えます。**View** メソッドは、サードパーティの開発用にはサポートされていません。 
    
28. **WinProj****WinProj**サービスは、Project Professional でのみ使用するために設計されています。 サード パーティの開発者は、Project Server を使用するプログラミングの**WinProj**メソッドを使用しないでください。 
    
    一部の **WinProj** メソッドは、**Project** および **Resource** サービスでも使用される、**ProjectRelationsDataSet** や **ResourceDataSet** のようなデータセットを使用しますが、Project Professional の特定のプロパティと機能を必要とします。 
    
    **WinProj** サービスへのアクセスは、**ProjectServiceApplication** URL を使用してだけ行えます。**WinProj** メソッドは、サードパーティの開発用にはサポートされていません。 
    
29. [ワークフロー](https://msdn.microsoft.com/library/WebSvcWorkflow.Workflow.aspx)エンタープライズ プロジェクトの種類およびワークフローのフェーズおよびステージを管理する CRUD メソッドが含まれています。 ワークフローの実行、ステータス情報を設定し、需要管理ワークフローでのプロジェクト詳細ページ (PDP) の段階を管理します。 Project Server ワークフローを開発するには、開発者は宣言型ワークフローは SharePoint Designer 2013 を使用して、または、[Office 開発者ツールを使用して.NET Framework 4 と、[を使用して開発の Visual Studio 2012 のMicrosoft.ProjectServer.Client.WorkflowActivities](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.WorkflowActivities.aspx) 、CSOM のクラスです。 
    
30. [WssInterop](https://msdn.microsoft.com/library/WebSvcWssInterop.WssInterop.aspx)プロジェクト サイトを管理します。 作成し、プロジェクト サイトを削除します。 情報を取得し、SharePoint の設定および管理サイトを更新します。 同期し、[プロジェクト サイトのメンバーシップ、およびグループを更新します。 
    
各サービスの名前空間には、**データセット**スキーマおよびイベント ハンドラー クラスのサービスを使用するすべてが含まれます。 たとえば、 `Calendar.svc` (または`Calendar.asmx?wsdl`は、ASMX web サービス)**カレンダー**サービスについて説明します。 **WebSvcCalendar**の参照の名前を指定する場合、プライマリ**予定表** **CheckInCalendars**のメソッドを持つクラス、 **CheckOutCalendars**、およびようにプロキシの名前空間が含まれます。 **WebSvcCalendar**プロキシの名前空間には、 **CalendarDataSet**クラスとそのすべてのサブクラスも含まれています。 
  
一部の PSI サービスには、重複する **DataSet** クラスが含まれます。たとえば、**Project** サービスと **Statusing** サービスのどちらにも、**ProjectDataSet** クラスが含まれます。これは、**Project** サービスと **Statusing** サービスの両方のメソッドに **ProjectDataSet** への参照が含まれ、参照を設定してアプリケーションをコンパイルすると作成されるプロキシ アセンブリに関連するデータセットが含まれるためです。**Project** サービスと **Statusing** サービスでは、**ProjectDataSet.ProjectRow** クラスの異なるフィールドの値が必要になる場合があります。 
  
PSI リファレンスの名前空間とクラスをナビゲートするときは (たとえば、**Project** サービスの Web メソッドを参照するとき)、[**コンテンツ**] リストで [**Project Web サービス**] 名前空間を展開した後、**Project** クラスを展開します。 
  
## <a name="see-also"></a>関連項目

- [Project Server 2013 のアーキテクチャ](project-server-2013-architecture.md)
- [Project Server プログラミング](project-server-programmability.md)   
- [PSI のすること、しないこと](what-the-psi-does-and-does-not-do.md)   
- [プロジェクト内の ASMX ベースのコード サンプルの前提条件](prerequisites-for-asmx-based-code-samples-in-project.md)   
- [プロジェクト内の WCF ベースのコード サンプルの前提条件](prerequisites-for-wcf-based-code-samples-in-project.md)   
- [.NET Framework デベロッパー センター](https://msdn.microsoft.com/netframework/aa496123.aspx)
    

