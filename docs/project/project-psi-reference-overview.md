---
title: プロジェクトPSIリファレンスの概要
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
- Webサービス、カレンダー、認証、Webサービス、ResourcePlan、Webサービス、StatusReports、Webサービス、PSI、ネームスペース、イベントハンドラ、Project Server、Webサービス、通知、QueueSystem、Webサービス、Project 2013、プラットフォーム、LoginWindows、Webサービス、 Webサービス、Statusing、Webサービス、リソース、WinProj、Webサービス、WssInterop、Webサービス、Webサービス、Winproj、イベントハンドラ、LookupTable、Webサービス、PWA、Webサービス、Webサービス、セキュリティ、通知、Webサービス、Webサービスタイムシート、Webサービス、QueueSystem、PSI、Webサービス、Webサービス、イベント、PSI、プログラミング、Webサービス、LookupTable、バージョン、Webサービス、CustomFields、Webサービス、Webサービス、PWA、PSI、リソース、Webサービス、Web service、ResourcePlan、タイムシート、Webサービス、Webサービス、ルール、PSI、マネージコードリファレンス、セキュリティ、Webサービス、Webサービス、CustomFields、URL、PSI向け、Webサービス、WssInterop、Webサービス、Admin、Web参照、PSI 、Webサービス、CubeAdmin、ビュー、Webサービス、カレンダー、Webサービス、Webサービス、ビュー、管理者、Webサービス、LoginForms、Webサービス、Webサービス、LoginForms、PSI、URL、ObjectLinkProvider、Webサービス、アーカイブ、Webサービス、CubeAdmin、Webサービス、ルール、Webサービス、Webサービス、認証、Webサービス、PSI、Project Server、イベントイベント、Webサービス、Webサービス、プロジェクト、ステータス管理、Webサービス、Webサービス、ObjectLinkProvider、Project Serverインタフェース、Webメソッド、PSI、Webサービス、StatusReports、Webサービス、アーカイブ、プロジェクト、Webサービス、Webサービス、LoginWindows
ms.assetid: d3c33089-0cbe-48c3-bfc0-0be819ca4d73
description: Project Serverインターフェイス（PSI）は、社内のProject Server 2013と統合するアプリケーションを開発するために使用するAPIです。
localization_priority: Priority
ms.openlocfilehash: 178f050022916ac1d26bd3d71f0ac5210c92295d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301560"
---
# <a name="project-psi-reference-overview"></a>プロジェクトPSIリファレンスの概要

Project Serverインターフェイス（PSI）は、社内のProject Server 2013と統合するアプリケーションを開発するために使用するAPIです。
  
この記事は、PSIで文書化されているアセンブリ、名前空間、およびサービスの概要です。 SDKの[Project Server 2013クラスライブラリとWebサービス参照](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx)には、PSIのマネージコードドキュメントとProject Server 2013の[Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx)名前空間がすべて含まれています。 Project Online用のアプリケーションを開発するには、PSIの代わりに** Microsoft.ProjectServer.Client**名前空間を使用する必要があります。 

Project Server 2013のPSIにはデュアルインターフェイスがあります。 Webサービス用のASMXインターフェースは、仮想ディレクトリー`https://ServerName/ProjectServerName/_vti_bin/psi/`内のディスカバリーおよびWebサービス記述言語（discoおよびWSDL）ファイル（例えば、Projectdisco.aspxおよびProjectwsdl.aspx）によって定義されます。 ASMXインターフェイスにアクセスできるのは、手動設置式のProject Web App（たとえば、`https://ServerName/ProjectServerName/_vti_bin/psi/project.asmx?wsdl)`のURLを通じてのみです。 Webサービスをブラウザに表示するには、`?wsdl` URLオプションを含める必要があります。 ASMXインターフェイスはWindows Communication Foundation（WCF）インフラストラクチャを使用して構築されているため、Project Server Webサービス用の.asmxファイルは、実際には仮想PSIディレクトリに存在しません。 
  
WCFサービスインターフェースは、SharePoint Webサービスアプリケーションのバックエンド`https://ServerName:32843/GUID/PSI/`仮想ディレクトリー内の.svcファイルによって定義されています。 Project Service Application仮想ディレクトリ（たとえば`https://ServerName:32843/GUID/PSI/project.svc`）内のPSIサービスのURLには、.svcファイルが含まれています。 ただし、バックエンドURLを直接使用してWCFサービス参照を設定することはできません。 PSIのWCFサービスを使用するアプリケーションまたはコンポーネントを開発するには、プロキシアセンブリまたはプロキシファイルを使用できます。 Project 2013 SDKのダウンロードには、Project Server 2013のWCFサービス用のプロキシファイル、および更新されたWCFプロキシファイルを取得して直近のProject Serverビルド用のファイルをプロキシアセンブリにコンパイルするためのスクリプトが含まれています。
  
Project Serviceアプリケーションのディレクトリ名はGUID値で、これは設置型Project Web AppインスタンスのGUIDと同じです。 [**インターネット インフォメーション サービス (IIS) マネージャー**] ウィンドウで、[**SharePoint Web サービス**] 接続ポイントを展開し、GUID ディレクトリ名を選択し、[**詳細設定**] を選択して、[**仮想パス**] の値をコピーします。 
  
> [!IMPORTANT]
> PSIのASMX WebサービスインターフェイスはProject Server 2013では非推奨ですが、引き続きサポートされています。 新しいアプリケーションは、PSIまたはCSOMのWCFインターフェイスを使用する必要があります。 廃止予定の機能について詳しくは、[Project 2013における開発者向けの更新プログラム](updates-for-developers-in-project-2013.md)を参照してください。
> 
> 新しいアプリケーション、および手動設置式Project Serverでのみ実行されるミドルウェアコンポーネントは、WCFインターフェイスを使用する必要があります。これはネットワーク通信に推奨されるテクノロジです。 ASMXインターフェイスを使用するレガシアプリケーションは、Project Web Appを通じてURLを使用する必要があります。これにより、Project Serverのアクセス許可が確認されます。 
> 
> ASMXインターフェースおよびWCFインターフェースの使用方法について詳しくは、[プロジェクトにおけるASMXベースのコードサンプルの前提条件およびプロジェクトにおけるWCFベースのコードサンプルの前提条件を参照してください。 
  
WCFインターフェイスを使用するアプリケーションを開発する際は、Visual Studio 2010またはVisual Studio 2012を使用できます。 宣言型Project Serverワークフローを作成するために、SharePoint Designer 2013を使用できます。 PSIまたはCSOMへのアクセスを必要とするProject Serverワークフローは、Visual Studio 2012を使用して開発できます。
  
### <a name="using-the-psi-reference"></a>PSIリファレンスを使用する
<a name="pj15_PSIRefOverview_Using"> </a>

PSIオブジェクトモデルは大きく、多くのクラスとメンバは内部使用専用です。 その結果、[Project Server 2013クラスライブラリとWebサービスリファレンス](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx)の中で必要なトピックをうまく見つけられない場合があります。 開発に使用する参照用のトピックのほとんどは、以下のグループにあります。
  
- **基本クラス・メソッド：** PSI内の各サービスには、そのサービスの名前で命名された基本クラスが含まれています。 例えば、**Resource**サービスには、[WebSvcResource](https://msdn.microsoft.com/library/WebSvcResource.aspx)名前空間にある[Resource](https://msdn.microsoft.com/library/WebSvcResource.Resource.aspx)クラスが含まれています。 **Resource** クラスで使用できるメソッドの一覧を表示するには、コンテンツ ペインのクラス ノードを展開し、[**リソース メソッド**] トピックをクリックします。 
    
- **DataRowプロパティー：** 多くの基本クラスメソッドは、**DataSet**を使用、または返します。 ** DataSet**の各**DataTable **オブジェクトには、1つ以上の**DataRow**オブジェクトのデータが含まれています。 ほとんどの場合、見る必要があるのは行のプロパティだけであり、**DataSet**、**DataTable**、または **DataRow** クラスの他のすべてのメンバーを見る必要はありません。 例えば、**ResourceAssignmentDataSet**クラスには、**ResourceAssignmentDataTable**および[ResourceAssignmentDataSet.ResourceAssignmentRow](https://msdn.microsoft.com/library/WebSvcResource.ResourceAssignmentDataSet.ResourceAssignmentRow.aspx)クラスのサブクラスが含まれています。 **ResourceAssignmentRow** クラスのプロパティの一覧を表示するには、コンテンツ ペインでクラス ノードを展開し、[**ResourceAssignmentDataSet.ResourceAssignmentRow のプロパティ**] トピックをクリックします。 
    
サービスの名前空間に加えて、[Project Server 2013クラスライブラリとWebサービスリファレンス](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx)のトピックは、手動設置用のサードパーティソリューションの開発に使用される3つのProject Serverアセンブリにリンクしています。 これらのアセンブリについては、最小限のドキュメントだけが提供されています。 さらに、PSI リファレンスでは、23 のパブリック サービスの主なクラスとメンバーが説明されています。 6 つの PSI サービスは内部使用専用であり、文書化されていません。 
  
> [!NOTE]
> クライアントサイドオブジェクトモデル（CSOM）のクラスは、他のProject Serverアセンブリおよびサービスとは独立して使用できます。 Project Serverコンピューターから、リモート開発環境で**Microsoft.ProjectServer.Client**名前空間を使用して、Project Onlineまたは手動設置式のProject Serverと統合するアプリケーションを開発できます。 ただし、CSOM に含まれるのは完全な PSI の機能のサブセットです。 CSOM を使用すると、Project Server 統合の最も一般的なシナリオを開発できます。 詳しくは、[CSOMの挙動について](what-the-csom-does-and-does-not-do.md)および[Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx)を参照してください。 
  
PSI を使用するほとんどのアプリケーションの開発は、Project Server コンピューターで行わなくてもよく、グローバル アセンブリ キャッシュで Project Server アセンブリへの参照を設定する必要はありません。 必要な Project Server アセンブリを開発コンピューターにコピーできます。 Project Server 2013は、_[Program Files] _ `\Microsoft Office Servers\15.0\Bin`に次のアセンブリをインストールします。 
  
- Microsoft.Office.Project.Server.Events.Receivers.dll 
- Microsoft.Office.Project.Server.Library.dll
- Microsoft.Office.Project.Server.Workflow.dll
    
PSIサービスの名前空間には、PSIプロキシアセンブリProjectServerServices.dll用に作成された任意の名前があります。これは、文書化の目的で生成されたものです。 PSIの参照では、各サービス名前空間はプレースホルダー名（_ [Project Webサービス] _など）とWeb参照（`https://ServerName/ProjectServerName/_vti_bin/psi/Project.asmx?wsdl`など）を持ちます。 
  
## <a name="project-server-assemblies-and-namespaces"></a>Project Serverのアセンブリと名前空間
<a name="pj15_PSIRefOverview_Assemblies"> </a>

Project Serverをインストールすると、多くのアセンブリがインストールされます。文書化されているのは4つのProject Serverアセンブリのみです。 サードパーティの開発者は通常、これらのアセンブリでは少数のクラスとメンバのみを使用します。 文書化されていないProject Serverアセンブリには、Project Web Appのクラス、事業名、データアクセス層（DAL）など、Project Serverが内部で使用する名前空間とクラスが含まれています。 文書化されているいずれかのProject ServerアセンブリにVisual Studioで参照を設定すると、Visual Studioのオブジェクトブラウザですべての名前空間、クラス、およびメンバを表示できます。
  
> [!NOTE]
> 文書化されたProject Server名前空間の多くのメンバは内部でのみ使用され、文書化は最小限です。 
  
Project Online用に開発する場合は、CSOMのみを使用してProject Serverの機能にアクセスできます。 PSIサービスまたは他のProject Serverアセンブリにアクセスすることはできません。
  
PSIの[ Project Server 2013クラスライブラリとWebサービス参照](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx)には、次のアセンブリの名前空間が含まれています。 
  
- **Microsoft.Office.Project.Server.Library.dll**このアセンブリには、次のように、1つの文書化された名前空間と3つの文書化されていない名前空間が含まれています。 
    
  - [Microsoft.Office.Project.Server.Library](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.aspx)名前空間には、多数の列挙型、Project Serverの設置型アプリケーションで頻繁に使用されるクラスフィールドおよびプロパティが含まれています。 例えば、開発者はよく**CustomField.Type**、**PSClientError**、**PSErrorInfo**、**Filter**クラスなどの列挙型を使用します。 
    
    **Microsoft.Office.Project.Server.Library**名前空間には、3,200を超えるサブクラスを含む次の7つのプロパティクラスも含まれています。 
    
      - **AssignmentProperties**  
      - **CalendarProperties**
      - **ConstraintProperties**
      - **LookupTableProperties**
      - **ProjectProperties**
      - **ResourceProperties**
      - **TaskProperties**
    
    プロパティクラスは内部的に使用され、文書化されていません。 プロパティクラスは、Project Professional 2013とProject Serverの間の直列化に使用されます。 Visual Studioで**Microsoft.Office.Project.Server.Library**名前空間を操作すると、オブジェクトブラウザにすべてのプロパティクラスが表示されるため、他社環境での開発で有用なクラスを見つけるのがより難しくなってしまいます。 サードパーティーの開発者はプロパティクラスを使用する必要がないため、SDKではそれらを文書化していません。 
    
  - **Microsoft.Office.Project.Server.DataServices**この名前空間のクラスとメンバは、Project Onlineの**OData**サービスによって内部的に使用され、Projectデータベースのレポートテーブルにアクセスします。 **DataServices**クラスは文書化されていません。 
    
  - **Microsoft.Office.Project.Server.Administration**この名前空間のクラスとメンバーは診断ログのために内部で使用されているため、文書化されていません。 
    
  - **Microsoft.Office.Project.Server.Base**この名前空間のクラスとメンバは、基本クラスとして内部的に使用されており、文書化されていません。 
    
  - **Microsoft.Office.Project.Server.Library.FilterSchema**この名前空間は、フィルター図式を生成するために内部的に使用されているため、文書化されていません。 
    
- **Microsoft.Office.Project.Server.Workflow.dll**このアセンブリは、Project Server 2013で引き続き機能する旧Project Server 2010ワークフローに使用されます。 新しいワークフローを作成するには、SharePoint Designer 2013を使用するか、[Microsoft.ProjectServer.Client.WorkflowActivities](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.WorkflowActivities.aspx)クラスと共にVisual Studio 2012を使用することもできます。 Microsoft.Office.Project.Server.Workflow.dllアセンブリには、次の3つの名前空間が含まれています。 
    
  - [Microsoft.Office.Project.Server.Workflow](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Workflow.aspx)この名前空間には、Project Serverのワークフローアクティビティに使用されるクラスが含まれています。 アクティビティには、プロジェクトプロパティの読み取り、比較、および更新が含まれます。 他のクラスは作業手順を管理し、プロジェクトが変更されたときのワークフローコールバックも行います。 
    
  - **Microsoft.Office.Project.PWA**この名前空間には、Project Web Appおよびカスタムワークフローアクティビティで使用するためのPSIの内部プロキシが含まれています。これは文書化されていません。 
    
    カスタムワークフローアクティビティでは、PSIサービス内のすべてのクラスにアクセスするために**Microsoft.Office.Project.PWA**への参照が必要です。 例えば、**Microsoft.Office.Project.PWA.PSI**クラスには**ProjectWebService**プロパティーが含まれ、これは[WebSvcProject](https://msdn.microsoft.com/library/WebSvcProject.aspx)名前空間のプロキシーを取得します。 
    
  - **Microsoft.Office.Project.Server.WebServiceProxy**この名前空間には、各PSIサービスの基準クラスの内部プロキシクラスが含まれています。 ワークフローユーザーの昇格権限を使用することで、ワークフローはプロキシクラスを通じてPSIメソッドを呼び出すことができます。 プロキシクラスは文書化されていません。 
    
- **Microsoft.Office.Project.Server.Events.Receivers.dll** [Microsoft.Office.Project.Server.Events](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.aspx)は、このアセンブリの唯一の名前空間です。 ここにはPSIサービスと他の内部クラスのためのイベント受信子とイベント引数クラスが含まれています。 
    
  開発者は、イベント レシーバーのクラスを継承するイベント ハンドラーを作成します。 PSI サービスのプライマリ クラスの多くには、対応するイベント レシーバー クラスがあります。 たとえば、**ProjectEventReceiver**クラスには、PSIの**Project**クラスのメソッドに対応する前置イベントおよび後置イベントのレシーバメソッドが含まれています。 **OnCreating**メソッドおよび**OnCreated**メソッドは、**QueueCreateProject**メソッドの前置イベントおよび後置イベントの受信メソッドです。 
    
  開発者はよく、次のイベントレシーバークラスを使用します。
  <br/>  
  - [AdminEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.AdminEventReceiver.aspx)
  - [CalendarEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.CalendarEventReceiver.aspx)
  - [CubeAdminEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.CubeAdminEventReceiver.aspx)
  - [CustomFieldsEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.CustomFieldsEventReceiver.aspx)
  - [LookupTableEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.LookupTableEventReceiver.aspx)
  - [AdminEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.ProjectEventReceiver.aspx)
  - [CalendarEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.OptimizerEventReceiver.aspx)
  - [AdminEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.ReportingEventReceiver.aspx)
  - [ResourceEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.ResourceEventReceiver.aspx)
  - [SecurityEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.SecurityEventReceiver.aspx)
  - [StatusingEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.StatusingEventReceiver.aspx)
  - [TimesheetEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.TimesheetEventReceiver.aspx)
  - [UserDelegationEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.UserDelegationEventReceiver.aspx)
  - [WorkflowEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.WorkflowEventReceiver.aspx)
  - [WssInteropEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.WssInteropEventReceiver.aspx)
    
  **RulesEventReceiver**クラスと** StatusReportsEventReceiver **クラスは、Project Web Appの内部で使用されます。 
    
- **Microsoft.ProjectServer.Client.dll**このアセンブリには、.NET Framework 4で開発するためのCSOMが含まれています。 アセンブリは`%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\ISAPI\Microsoft.ProjectServer.Client.dll`に位置しています。 **Microsoft.ProjectServer.Client** 名前空間でのアプリの開発は社内設置型の Project Server API およびサービスとは独立していますが、アプリは Project Server の社内設置型インストールまたはオンライン インストールのどちらでも動作できます。 Windows Phone 8、Microsoft Silverlight、またはWebアプリケーションを備えたJavaScriptに使用できる関連CSOMアセンブリについては、[Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx)を参照してください。 
    
- **Microsoft.Office.Project.Server.Schema.dll** Project 2013 SDKでは、`[Windows]\Microsoft.NET\assembly\GAC_MSIL\Microsoft.Office.Project.Schema\v4.0_15.0.0.0__71e9bce111e9429c\Microsoft.Office.Project.Schema.dll`アセンブリ内にある**Microsoft.Office.Project.Server.Schema**名前空間は文書化されていません。 この名前空間には、PSI で使用されるすべての **DataSet**、**DataTable**、**DataRow** クラスの定義に加えて、Project Server 内部で使用されるその他の多くの類似クラスの定義が含まれます。 各PSIサービスのパブリッククラスは、特定のサービスリファレンスに記載されています。 例えば、**DriverDataSet.DriverRow**クラスは、[WebSvcDriver](https://msdn.microsoft.com/library/WebSvcDriver.aspx)名前空間に記載されています。 
    
  > [!NOTE]
  > CSOMを使用するアプリケーション、リモートイベントハンドラを使用するアプリケーション、またはProject Onlineにアクセスするアプリケーションは、**Microsoft.Office.Project.Server.Schema**名前空間を使用しません。 
  
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

  - カスタムワークフローアクティビティでは、**DataSet**定義に対して**Microsoft.Office.Project.Server.Schema**への参照が必要になる場合があります。 
    
## <a name="psi-services"></a>PSI サービス
<a name="pj15_PSIRefOverview_PSI"> </a>

PSIは、WCFサービスの集まりで、Project Server 2013用のASMX Webサービスと同一のものです。 Visual Studioプロジェクトでサービスを使用するには、ネームサービスに任意の名前を使用して、`.svc`ファイルまたは`.asmx?wsdl`サービスのURLへの参照を設定します。 wsdl.exe ユーティリティまたは svcutil.exe ユーティリティによってその名前空間のプロキシ ソース コードが生成され、コンパイラによりアプリケーションに含めるプロキシ サービス アセンブリが作成されます。 
  
> [!NOTE]
> PSIリファレンスには、_ [管理Webサービス] _、_ [ドライバーWebサービス] _、_ [プロジェクトWebサービス] _などのPSIサービスのプレースホルダーサービス名が含まれています。 各PSIネームサービスには、そのサービスのWebメソッドを含む基準クラスが含まれています。 たとえば、**Admin** サービスへの参照を設定し、それに **WebSvcAdmin** という名前を付けた場合、アプリケーションの **WebSvcAdmin** nameservice には、プライマリ クラス **Admin** とその **GetServerCurrency**、**ListInstalledLanguages**、**ReadServerVersion** などの Web メソッドが含まれます。 非推奨のPSIサービスのリストについては、[ Project 2013における開発者向け更新](updates-for-developers-in-project-2013.md)を参照してください。 
  
合計30のPSIサービスのうち、**認証**、**ExchangeSync**、**OData**、**P12アップグレード**、**psiserviceapp**、**PWA**、**表示**、および**WinProj**は、Project Web AppおよびProject Professionalによって内部的に使用されるものであり、文書化されていません。 PSI内部サービスを含むプロキシファイルまたはプロキシアセンブリを作成することはできますが、その内部サービスは他社環境による使用には適していません。 PSIリファレンスはそれらのサービスを文書化していません。 次の図は、インターネットインフォメーションサービスマネージャのバックエンドPSIサービスの場所を示しています。 
  
**IISのPSIサービスを設置する**

![IIS マネジャー内のPSIサービス](media/pj15_PSIReference_IIS.gif "IIS マネジャー内のPSIサービス")
  
以下は、PSIサービス内のWebメソッドを含むすべてのクラスです。
  
1. [Admin](https://msdn.microsoft.com/library/WebSvcAdmin.Admin.aspx)には、Project Web Appの**Project Server Administration**ページで使用されるメソッドが含まれています。 会計年度を定義し、ステータスと通貨設定、記録期間、監査ログ、およびActive Directoryの設定を管理します。 
    
2. [アーカイブ](https://msdn.microsoft.com/library/WebSvcArchive.Archive.aspx)には、プロジェクトのバックアップと復元、セキュリティの分類、カスタムフィールド、リソース、システム設定、ビュー、および事業の総括プロジェクトの管理方法が含まれます。 保管スケジュールを読み込んで更新します。 すべてのプロジェクトをアーカイブするか、指定されたアーカイブ済みプロジェクトを削除します。 バックアップオブジェクトを保管データベーステーブルに保存し、バックアップしたオブジェクトを発行済データベーステーブルに復元します。 
    
3. **認証**には、Project ProfessionalおよびProject Web Appのみによる内部使用のためのメソッドが含まれています。 
    
4. [カレンダー](https://msdn.microsoft.com/library/WebSvcCalendar.Calendar.aspx)事業カレンダーの例外を管理します。 リソースカレンダーをチェックアウトおよびチェックインします。 カレンダーの例外を作成、削除、一覧表示、更新、または戻します。 
    
5. [CubeAdmin](https://msdn.microsoft.com/library/WebSvcCubeAdmin.CubeAdmin.aspx) OLAPキューブ設定を管理します。 分析サーバー、データベースの状態、およびキューブのリストを取得します。 Cube Build Service 要求をキューに配置します。 キューブのディメンションおよびメジャーに関する計算済みのメンバー定義とフィールド設定を読み取り、更新します。 
    
6. [CustomFields](https://msdn.microsoft.com/library/WebSvcCustomFields.CustomFields.aspx)事業用カスタムフィールドを管理します。 チェックアウトおよびチェックイン方法、および事業用カスタムフィールドの作成、読み取り、更新、および削除（CRUD）メソッドが含まれます。 
    
7. [ドライバー](https://msdn.microsoft.com/library/WebSvcDriver.Driver.aspx)プロジェクト作成および需要管理のためのポートフォリオ分析ドライバーおよびドライバーの優先順位付けを管理します。 プロジェクトドライバー用のCRUDメソッドが含まれます。 
    
8. [イベント](https://msdn.microsoft.com/library/WebSvcEvents.Events.aspx) Project Serverイベントハンドラの関連付けを管理します。 特定のイベント、またはすべてのイベントハンドラの関連付けに対するProject Serverのイベントハンドラの関連付けに対するCRUDメソッドが含まれます。 
    
9. **ExchangeSync**これは、Exchange Serverイベントを処理する内部Project Serverサービスです。 Project Web Appは、Office Project Server 2007のようにOutlookクライアントと直接同期するのではなく、**ExchangeSync**を使用してProject ServerとExchange Serverの間の割り当てを同期します。 
    
    **ExchangeSync**サービスへのアクセスは、**ProjectServiceApplication** URLを通じてのみ可能です。 **ExchangeSync**のクラスとメンバは、他社環境での開発ではサポートされていません。 
    
10. [LoginForms](https://msdn.microsoft.com/library/WebSvcLoginForms.LoginForms.aspx)フォームベース認証で**Login**および**Logoff**メソッドを提供します。 **LoginForms**サービスへのアクセスは、フロントエンドのProject Web Appサイトでのみ利用可能です。 
    
11. [LoginWindows](https://msdn.microsoft.com/library/WebSvcLoginWindows.LoginWindows.aspx)複数認証（要求およびフォームベース）Project Server 2013の環境において、ASMXベースのアプリケーションを使ったWindows認証に使用される**Login**および**Logoff**メソッドを提供します。 **LoginWindows**サービスへのアクセスは、フロントエンドのProject Web Appサイトでのみ可能です。 
    
    > [!CAUTION]
    > **LoginWindows**サービスは、WCFベースのアプリケーション、または要求認証のみを使用するProject Server環境で実行されるアプリケーション、または**OAuth**では使用されません。そのような場合、**Login**メソッドは常に**false**を返します。 要求認証は、統合Windows認証を扱います。 
  
12. [LookupTable](https://msdn.microsoft.com/library/WebSvcLookupTable.LookupTable.aspx)参照テーブル、多言語参照テーブル、およびそれらに対応するコード定義を管理します。 チェックアウト、チェックイン、読み取り、作成、削除、および更新。 
    
13. [通知](https://msdn.microsoft.com/library/WebSvcNotifications.Notifications.aspx)アラートとリマインダーを管理します。 アラート結果を取得、設定、登録、および登録解除するメソッドが含まれています。 
    
14. [ObjectLinkProvider](https://msdn.microsoft.com/library/WebSvcObjectLinkProvider.ObjectLinkProvider.aspx) SharePointサイト上のドキュメントおよび一覧アイテムのWebオブジェクトおよびリンクを管理します。 プロジェクト、プロジェクトリンク、タスク、またはタスク関連Webオブジェクトを作成、削除、または読み取り。 
    
    > [!NOTE]
    > **ObjectLinkProvider**サービスは、Project Server 2013では推奨されていません。 詳しくは、[Project 2013における開発者向け更新](updates-for-developers-in-project-2013.md)の*非推奨機能*の部分を参照してください。 
  
15. **OData**記録テーブルおよびビューの内部**OData**インターフェースを提供します。 **OData**サービスへのアクセスは、バックエンドの**ProjectServiceApplication** URLを通じてのみ可能です。 PSIの個別**OData**サービスは、**ODataClient.ProcessOdataMessage**という1つのメソッドを提供します。これは、Project Serverがデータ記録を処理するために内部で使用するメソッドです。 HTTP要求はフロントエンド**ProjectData**サービスを通過します。 
    
    記録データを読み取るための**ProjectData**サービスおよびODataプロトコルについては、[ProjectData  -  Project ODataサービスの参照](https://msdn.microsoft.com/library/office/jj163015.aspx)をご覧ください。
    
16. **P12Upgrade** Project Server 2013インストーラーがOffice Project Server 2007の環境をアップグレードするための内部メソッドを提供します。 **P12Upgrade**サービスへのアクセスは、**ProjectServiceApplication** URLを通じてのみ可能です。 **P12Upgrade**メソッドは、他社環境での開発ではサポートされていません。 
    
17. [PortfolioAnalyses](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.aspx)プロジェクトの依存関係、およびオプティマイザー、プランナー、および分析方法のためのCRUDメソッドが含まれています。 
    
18. [Project](https://msdn.microsoft.com/library/WebSvcProject.Project.aspx)プロジェクトを管理します。 プロジェクトデータベースの仮テーブルまたは発行済テーブル内のプロジェクトをチェックアウト、チェックイン、作成、削除、読み取り、または更新します。 発行待ち状態にメッセージを入れます。 
    
    プロジェクト内の命名（タスク、リソース、割り当てなど）を作成または削除します。 プロジェクトチームまたはプロジェクトサイトのアドレスに関する情報を取得または更新します。 プロジェクトの状態、下書きテーブル内のプロジェクトのリスト、すべてのサマリー タスク、指定されたリソースに割り当てることができるタスク、またはリソースに割り当てがあるすべてのプロジェクトを取得します。
    
    コミットメントを作成および管理したり、SharePoint タスク リストからプロジェクトの提案とプロジェクトを作成したり、プロジェクト/マスター プロジェクトの関係を検索したりします。
    
19. **psiserviceapp** Project Onlineによって内部的に使用されます。 **psiserviceapp**のクラスとメンバは、他社環境での開発ではサポートされていません。 
    
20. **PWA** Project Web App用に最適化された多くのメソッドが含まれています。これには、タスク更新の承認規則やステータスレポートの管理方法などが含まれます。 **PWA**メソッドは多くの場合特殊化されており、他のPSIサービスの同等のメソッドと比べてやや冗長です。 **PWA**メソッドは、他のPSIメソッドと同じデータセットを多数使用するか返します。 
    
    **PWA**サービスへのアクセスは、**ProjectServiceApplication** URLを通じてのみ可能です。 **PWA**のクラスとメンバーは、他社環境での開発ではサポートされていません。 
    
21. [QueueSystem](https://msdn.microsoft.com/library/WebSvcQueueSystem.QueueSystem.aspx) Project Serverのキューを管理します。 ジョブ数、ジョブやジョブ グループの待ち時間、すべてのジョブの進捗状況、指定されたジョブ、呼び出し元が所有するジョブ、または指定されたプロジェクトのジョブを取得します。 ジョブの相互関係を管理し、キューを構成します。 
    
22. [Resource](https://msdn.microsoft.com/library/WebSvcResource.Resource.aspx)業務用リソースを管理します。 リソースまたはProject Serverユーザーとその認証設定をチェックアウト、チェックイン、更新、または作成。これは名前またはGUIDでリソースを見つけます。リソースまたはユーザーデータ、およびリソース細分化構造（RBS）と関連するセキュリティ情報の読み取り。これはリソースに対するすべての割り当てを取得し、またユーザーパスワードをリセットします。 **Resource**クラスには、ユーザー委任用のCRUDメソッドが含まれています。 
    
23. [ResourcePlan](https://msdn.microsoft.com/library/WebSvcResourcePlan.ResourcePlan.aspx)リソースプランを管理します。 リソースプランのチェックアウト、チェックイン、発行、およびCRUDメソッドの追加をします。 
    
24. [Security](https://msdn.microsoft.com/library/WebSvcSecurity.Security.aspx)セキュリティテンプレート、セキュリティカテゴリ、組織および総括権限、およびグループの権限に対するCRUDメソッドを含みます。 **Security**クラスにはプロジェクトカテゴリのメソッドが含まれています。 
    
25. [Statusing](https://msdn.microsoft.com/library/WebSvcStatusing.Statusing.aspx)状況の更新および割り当てを管理します。 割り当てを作成、取得、または代理します。 割り当ての動作期間を設定します。 現在のユーザーの新しい割り当てを取得したり、割り当てやタスクのトランザクション履歴、時間配分された実績作業時間、サマリー タスク階層を取得したりします。 
    
    タイムシート データをプレビューまたはインポートしたり、ユーザーの稼働日および非稼働日のスケジュールを読み取ったりします。承認待ちの進捗状況の更新、提出された更新の情報、または提出された更新に含まれる変更のトランザクション レコードを検索します。チームの状態を読み取ります。
    
26. [TimeSheet](https://msdn.microsoft.com/library/WebSvcTimeSheet.TimeSheet.aspx)タイムシートを管理します。 遅れている、または承認待ちのタイムシートを検索します。 日付または期間でタイムシートを検索します。 タイムシート承認者のリストを取得します。 実績をプリロードし、タイムシート行を検証します。 **TimeSheet** クラスには、偽装を必要としないで別のリソースのタイムシートを読み取ったり送信したりするための **ReadProjectTimesheetLines** メソッドおよび **SubmitTimesheetLines** メソッドが含まれます。 
    
27. **View** **View**サービスは、Project Web App内でのみ使用するように設計されています。 **View **クラスのメソッドは、ビューを管理し、レポートを表示し、ビュー内のフィールドを読み取ります。 
    
    **View**サービスへのアクセスは、**ProjectServiceApplication** URLを通じてのみ可能です。 **View**メソッドは、他社製環境での開発ではサポートされていません。 
    
28. **WinProj** **WinProj**サービスは、Project Professional専用のサービスです。 他社環境での開発者は、Project Serverでのプログラミングに**WinProj**メソッドを使用しないでください。 
    
    一部の **WinProj** メソッドは、**Project** および **Resource** サービスでも使用される、**ProjectRelationsDataSet** や **ResourceDataSet** のようなデータセットを使用しますが、Project Professional の特定のプロパティと機能を必要とします。 
    
                 **WinProj** サービスへのアクセスは、**ProjectServiceApplication** URL を使用してだけ行えます。              **WinProj** メソッドは、サードパーティの開発用にはサポートされていません。 
    
29. [Workflow](https://msdn.microsoft.com/library/WebSvcWorkflow.Workflow.aspx)業務プロジェクトタイプ、および作業のフェーズとステージを管理するためのCRUDメソッドが含まれています。 ワークフローを実行し、ステータス情報を設定し、需要管理ワークフローのプロジェクト詳細ページ（PDP）ステージを管理します。 Project Serverワークフローを構築するには、開発者は宣言型ワークフローにSharePoint Designer 2013を使用するか、.NET Framework 4での開発用にOffice Developer Tools for Visual Studio 2012を用い、CSOM内の[Microsoft.ProjectServer.Client.WorkflowActivities](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.WorkflowActivities.aspx) classクラスを使用できます。 
    
30. [WssInterop](https://msdn.microsoft.com/library/WebSvcWssInterop.WssInterop.aspx)プロジェクトサイトを管理します。 プロジェクトサイトを作成および削除します。 SharePoint設定と管理サイトに関する情報を取得して更新します。 プロジェクトサイトのメンバーシップとグループを同期して更新します。 
    
各サービスの名前空間には、サービスが使用するすべての**DataSet**スキーマとイベントハンドラクラスが含まれています。 例えば、`Calendar.svc`（またはASMX Webサービスの場合は`Calendar.asmx?wsdl`）は、**カレンダー**サービスを表します。 リファレンスに**WebSvcCalendar**という名前を付けると、プロキシ名前空間には、メソッド**CheckInCalendars**、**CheckOutCalendars**などを持つプライマリ**Calendar**クラスが含まれます。 **WebSvcCalendar**プロキシ名前空間には、**CalendarDataSet**クラスとそのすべてのサブクラスも含まれています。 
  
一部のPSIサービスには、重複した**DataSet**クラスが含まれています。 例えば、**Project**サービスと**Statusing**サービスはどちらも**ProjectDataSet**クラスを含みます。 これは、**Project** サービスと **Statusing** サービスの両方のメソッドに **ProjectDataSet** への参照が含まれ、参照を設定してアプリケーションをコンパイルすると作成されるプロキシ アセンブリに関連するデータセットが含まれるためです。 **Project**サービスおよび**Statusing**サービスでは、**ProjectDataSet.ProjectRow**クラスのさまざまなフィールドに値を指定できます。 
  
PSI リファレンスの名前空間とクラスをナビゲートするときは (たとえば、**Project** サービスの Web メソッドを参照するとき)、[**コンテンツ**] リストで [**Project Web サービス**] 名前空間を展開した後、**Project** クラスを展開します。 
  
## <a name="see-also"></a>関連項目

- [Project Server 2013 のアーキテクチャ](project-server-2013-architecture.md)
- [Project Server プログラミング](project-server-programmability.md)   
- [PSI ができること、できないこと](what-the-psi-does-and-does-not-do.md)   
- [プロジェクト内のASMXベースコードサンプルの前提条件](prerequisites-for-asmx-based-code-samples-in-project.md)   
- [プロジェクト内のWCFベースコードサンプルの前提条件](prerequisites-for-wcf-based-code-samples-in-project.md)   
- [.NET Framework デベロッパー センター](https://msdn.microsoft.com/netframework/aa496123.aspx)
    

