---
title: Project Server プログラミング
manager: lindalu
ms.date: 12/03/2019
ms.audience: Developer
f1_keywords:
- events
- PDS
- PDS compatibility
- Project Server databases
- Project Server events
- Project Server Interface
- Project Server workflow
- Project workflow
- PSI
- PSI limitations
- PSI uses
- SharePoint Services
- WF
- workflow
- Workflow Foundation
- WSS
keywords:
- プロジェクト 2013、アーキテクチャとプログラミング、PSI、プロジェクト、バージョン、プログラミング、Project Server、PSI、制限、Project Server Interface、サポート対象外の機能、Project Server インターフェイス、PDS 互換性、Project Server Interface、汎用、Project Server、プロジェクトのバージョン、バージョン、プロジェクト、Project Server、データベース、Project 2013、プラットフォーム、Project Server Interface、シナリオの使用、Project Server、イベント、Project Server、Project Data Service、PSI との互換性、Project Server Interface
ms.assetid: a93d2153-5132-4289-af51-69350471e248
description: Project Server 2013 の主要なプログラミング機能について説明します。 この記事には、以前のバージョンの Project Server 用に構築されたアプリケーションの移植についての情報が含まれています。
ms.localizationpriority: high
ms.openlocfilehash: a45624c98a2bbd04353daa31eb47655e2c963012
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628998"
---
# <a name="project-server-programmability"></a>Project Server のプログラミング

Project Server 2013 の主要なプログラミング機能について説明します。 この記事には、以前のバージョンの Project Server 用に構築されたアプリケーションの移植についての情報が含まれています。

Project Server 2013 は、Project Server 2010 と複数のプラットフォームでは、アプリがアクセスできる場所両方オンラインおよびオンプレミスの Project Server のインストール用に新しいソリューションの開発されたほとんどのアプリケーションをサポートするよう設計されています。 Project Server 2003 以前用に開発されたアプリケーションと拡張機能は、クライアント側オブジェクト モデル (CSOM) または Project Server インターフェイス (PSI) を使用するように再設計する必要があります。 Office Project Server 2007 または Project Server 2010 用に開発されたアプリケーションでは、PSI を使用するためにいくつかの変更と再コンパイルが必要になる場合があります。CSOM を使用するには、これらのアプリケーションに再設計が必要です。
  
Project Server プラットフォームは、SharePoint Server 2013、.NET Framework 4、および OData プロトコル上に CSOM と共に構築することにより、プログラマの高レベルな生産性を実現します。 開発者は、アプリ、アプリ パーツ、および Web パーツを使用して Project Web App を拡張し、SharePoint Designer 2013 を使用してワークフローを定義し、Project Server イベントのリモート イベント レシーバーを使用してビジネス ルールを適用することができます。
  
## <a name="project-server-and-sharepoint-server"></a>Project Server と SharePoint Server
<a name="pj15_Programmability_MOSS"> </a>

Project Web App は SharePoint Server 2013 上に構築されます。マスター ページと Web パーツを使用すると、カスタム アプリと Project Web App ソリューションを簡単に構築できます。 Project Server 2013 は SharePoint Server 2013 と緊密に連携し、このプラットフォームの上にプロジェクト コラボレーション、レポート作成、サイト管理、セキュリティ、およびワークフロー管理を実現します。
  
プロジェクト サイトには、チームのメンバーに向けた多くの情報と共同作業のオプションが含まれています。ここには、プロジェクトの概要、タイムラインの付いたタスク用の特殊な SharePoint リスト、問題の追跡、リスク、プロジェクト成果物、チームの予定表などの既定のアプリを、ドキュメント ライブラリおよびチーム ディスカッションと一緒に追加できます。 Project Server 2013 のカスタム アプリでは、チームの共同作業のための拡張機能と柔軟性を提供します。 ページを編集するときに Web パーツを追加および編集するのと同じメカニズムを使用して、アプリをカスタマイズするためのアプリ パーツを追加することもできます。 プロジェクト サイトは、Project Server がインストールされている SharePoint ファーム内の任意の場所に配置できます。 Excel Services や Enterprise Search など、SharePoint Server 2013 の他のコア サービスを使用するために、管理者はサービスを有効にして構成できます。 
  
Project Server 2013 のインストール時には、SharePoint Web サービス サイトの Project Service アプリケーションを準備します。 Project Service アプリケーションには、PSI 用のローカルな Windows Communication Foundation (WCF) サービスや ASMX Web サービスが含まれます。 他のサービス アプリケーションとしては、SharePoint 検索や SharePoint ドキュメント管理などがあります。 詳細については、SharePoint Server 2013 の開発者ドキュメントを参照してください。
  
Project Service アプリケーションは、Project Web App の複数のインスタンスを管理できる論理的なサービス プロバイダーです。 Project Server のプロビジョニングにより、SharePoint Web アプリケーション内に特定の Project Web App サイトが作成されます。 Project Web App のホーム ページには、レポート作成用のプロジェクト センター ページ、リソース センター ページ、およびビジネス インテリジェンス センター ページへのリンクと、その他の標準アプリの一覧が含まれているページへのリンクがあります。 図 1 は、Project Web App のホーム ページの **[設定]** ドロップダウン リストにある **[ページの編集]** コマンドを示しています。これにより、Web パーツを追加または編集できます。 
  
> [!NOTE]
> Project Web App の一部の管理用ページ (PWA 設定ページなど) は編集できず、**[ページの編集]** コマンドが表示されません。 Project Web App では、SharePoint Designer 2013 を使用してページを編集することはできません。 SharePoint Designer 2013 を使用して、プロジェクト サイト ページを編集できます。 
  
**図 1. Project Web App の [ページの編集] メニューを使用する**

![Project Web Access でのホーム ページの編集](media/pj15_Programmability_PWAHome.gif "Project Web Access でのホーム ページの編集")
  
Project Web App の [サイトの設定] ページにアクセスするには、ページの右上隅にある **[設定]** アイコンをクリックします。 [サイト設定] ページ (  `https://ServerName/ProjectServerName/_layouts/15/settings.aspx`) では、ルック アンド フィールとサイトのテーマの変更、カスタム Web パーツの追加、およびプロジェクト サイトのマスター ページの変更または作成を行うことができます。
  
ASPX ページ内のコードのカスタマイズ、または SharePoint Designer 2013 を使用した Project Web App マスター ページのカスタマイズはサポートされていません。 Project Web App ページ内のコードをカスタマイズすると、Project Server の更新プログラムやサービス パックで問題が生じることがあります。 
  
### <a name="customization-of-project-web-app-with-sharepoint-packages"></a>SharePoint パッケージを使用した Project Web App のカスタマイズ
<a name="pj15_Programmability_CustomizationOfPWA"> </a>

Project Web App は SharePoint アプリケーションであり、プロジェクト サイトは SharePoint サイトであるため、カスタム アプリ、Web パーツ、イベント ハンドラー、ユーザー設定フィールドなどの機能を SharePoint パッケージ (.wsp ファイル) または SharePoint アプリ (.spapp ファイル) を使用して追加できます。 1 つの SharePoint パッケージまたはアプリ パッケージに複数の Project Server エンティティを含めることができ、エンティティ定義はパッケージ内の elements.xml ファイルで指定されます。
  
Project Online では Project Web App リボンにボタンを追加できます。ただし、既存の製品のボタンを削除したり、名前を変更することはできません。また、新しいリボン タブも作成できません。 詳細については、「[カスタム アクションを作成して SharePoint のアプリで展開する](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/create-custom-actions-to-deploy-with-sharepoint-add-ins)」を参照してください。
  
> [!CAUTION]
> SharePoint パッケージまたはアプリ パッケージのインストール時には、Project Server エンティティの種類が PSEntityProvision.xsd スキーマに指定された順序で出現する必要があります。そうでない場合、パッケージのスキーマ検証が失敗し、インストールは完了しません。 
  
PSEntityProvision.xsd スキーマ ファイルは、Project 2013 SDK ダウンロード (`Documentation\Schemas\AppProvisioning` サブディレクトリ内) にあります。 図 2 は、**PSEntityProvision** スキーマの Visual Studio での XML スキーマ エクスプローラー ビューを示しています。ここでは **LookupTable** シーケンスが展開されています。 
  
**図 2. Project Server エンティティのプロビジョニング スキーマの Visual Studio ビュー**

![Project Server エンティティ スキーマのビュー](media/pj15_Programmability_EntitySchema.gif "Project Server エンティティ スキーマのビュー")
  
Project Server 用の機能をインストールする SharePoint パッケージには、**PSEntityProvision** スキーマに従った elements.xml ファイルを 1 つまたは複数含めることができます。1 つの XML ファイル内の Project Server エンティティは、次の順序で出現する必要があります。 
  
1. ワークフロー フェーズ
    
2. 参照テーブル
    
3. カスタム フィールド
    
4. ワークフロー ステージ
    
5. エンタープライズ プロジェクトの種類
    
6. イベント ハンドラー
    
Project Server エンティティを含む SharePoint パッケージを作成するときに、複数の elements.xml ファイルにエンティティ定義を含めることができます。各 XML ファイルがスキーマ検証に合格しても、パッケージ全体ではエンティティの順序が正しくない可能性があります。たとえば、最初の XML ファイル内のユーザー設定フィールド エンティティが 2 番目の XML ファイル内の参照テーブルを参照している場合があります。インストール時には、参照テーブルがまだ作成されていないため、ユーザー設定フィールドを作成できません。
  
パッケージのインストールに失敗した場合、作成されたオブジェクトは Project Web App に残りますが、パッケージは完全にはインストールされません。 パッケージを再インストールすることはできますが、お客様にとって適切な方法ではありません。 エンティティ定義が複数の elements.xml ファイルにまたがる場合は、SharePoint パッケージ全体で Project Server エンティティを整理して、インストールが正しい順序に従っていることを確認します。 Project 2013 SDK ダウンロードの PSEntityProvision.xsd スキーマを使用すると、XML ファイル内のエンティティの規定の順序を確認するツールを開発できます。
  
## <a name="upgrading-applications-with-the-project-server-apis"></a>Project Server API を使用してアプリケーションをアップグレードする
<a name="pj15_Programmability_APIs"> </a>

前のバージョンの Project Server 向けに開発されたアプリケーションをアップグレードする場合は、プロジェクト エンティティの作成、読み取り、更新、および削除のためのメソッド (CRUD 操作) を含むプログラム インターフェイスとして CSOM と PSI のどちらを使用するかを選択できます。CSOM は内部で PSI を呼び出しますが、すべての PSI メソッドに完全に代わるものではありません。PSI と CSOM のシナリオと制約については、「[What the PSI does and does not do](what-the-psi-does-and-does-not-do.md)」および「[What the CSOM does and does not do](what-the-csom-does-and-does-not-do.md)」を参照してください。
  
> [!NOTE]
> CSOM に必要な機能が含まれている場合は、CSOM を使用するようにアプリケーションをアップグレードすることをお勧めします。 CSOM を使用すると、アプリケーションをオンプレミスとオンラインの両方の Project Server 2013 インストールで使用できるようになります。 
  
アプリケーションが主に Project Server からデータを読み取る場合は、社内のシナリオに Project Server データベースのレポート テーブルおよびビューを使用できます。 アプリケーションを Project Online と共に使用する場合は、レポート データへのオンプレミスとオンラインの両方のアクセスを提供する **ProjectData** サービス用の OData プロトコルを使用できます。 詳細については、「[ProjectData - Project OData サービス参照](https://docs.microsoft.com/previous-versions/office/project-odata/jj163015(v=office.15))」を参照してください。
  
### <a name="using-the-psi"></a>PSI を使用する
<a name="pj15_Programmability_PSI"> </a>

PSI は、Project Professional 2013、Project Web App、および LOB アプリケーションなどの完全信頼クライアント アプリケーションが SharePoint ファーム内で Project Server データにアクセスできるようにします。 PSI は .NET Framework 4 と共に構築および使用され、組み込みセキュリティを備えた馴染みのある開発環境、エラー処理、ガベージ コレクションなどの利点を提供します。
  
PSI には、WCF サービスまたは ASMX Web サービスを通じてアクセスします。 ASMX インターフェイスは WCF に基づいています。 各 PSI サービスには、通常、基本クラスと共に、そのクラス内のアイテム用の CRUD メソッドが含まれています。 アイテムは、関連する **DataSet** クラスによって指定されます。 たとえば、**CustomFields** サービスには、[CreateCustomFields2](https://docs.microsoft.com/previous-versions/office/ee767959(v=office.14)) などのメソッドを持つ **CustomFields** クラスが含まれています。 1 つまたは複数のエンタープライズ カスタム フィールドのデータが **CustomFieldDataSet** に指定されています。
  
> [!NOTE]
> PSI の ASMX Web サービスのインターフェイスは、Project Server 2013 で廃止されました。 ASMX インターフェイスは引き続き利用できますが、PSI を使用する新しいアプリケーションは WCF インターフェイスを使用する必要があります。可能であれば、新しいアプリケーションでは PSI の代わりに CSOM を使用してください。 Project Server の将来のバージョンでは、PSI の WCF インターフェイスを使用する場合や CSOM を使用する場合に、既存の ASMX ベースのアプリケーションをアップグレードする必要があります。 
  
文書化されたパブリック PSI サービスは 22 個あり、これらは WCF インターフェイスおよび ASMX インターフェイスに複製されています。 また、PSI には文書化されていない 8 個のプライベート インターフェイスも含まれています。 Project Web App および Project Professional は、パブリック PSI サービスとプライベート PSI サービスを使用します。 PSI は通常、ビジネス オブジェクトと一致するように組み込まれます。 つまり、各 PSI メソッドは、**カレンダー** や **リソース** などのビジネス オブジェクトに関連付けられています。 PSI は、ビジネス オブジェクトへのプライマリ インターフェイスです。 ビジネス層によって再利用可能なビジネス ロジック コンポーネントが提供されるため、Project Server データを処理するさまざまなアプリケーションで同じビジネス ロジックが使用されます。
  
Project Server と非同期で対話する PSI メソッドは、**Queue** で始まる名前を持ちます。 各 PSI メソッドは、厳密に型指定されたデータを使用する独立したインターフェイスによって実装されます。 たとえば、**Project** サービスの **QueueCreateProject** メソッドは、**ProjectDataSet** 型の _dataset_ パラメーターを受け取ります。 **ProjectDataSet** クラスは **DataSet** 型から派生しています。 .NET Framework の型チェックと Visual Studio の IntelliSense の完了は、PSI を使用した開発のエラーを減らすために役立ちます。 PSI の名前空間、クラス、メソッド、プロパティ、イベント、および関連アセンブリの詳細な参照の概要については、「[Project PSI リファレンスの概要](project-psi-reference-overview.md)」を参照してください。
  
Project Server 2013 は、.NET Framework の例外処理を使用します。 すべてのエラーは PSI スタックの上部にあるサーバーに記録されます。 エラーの中には、ASMX インターフェイスの **SoapException** オブジェクトや WCF インターフェイスの **FaultException** オブジェクトのように、クライアントへ簡単なレポートとして送信されるものもあります。 例外はアプリケーション イベント ログに記録することができ、一部のエラーでも、サーバーの統合ログ サービス (ULS) のトレース ログに詳細なレポートが記録されます。 
  
ローカルの完全信頼アプリケーションに対しても、PSI は拡張性に優れています。サービスを含む .NET アセンブリを追加し、そこで新しい機能を提供し、同じ Project Server セキュリティ インフラストラクチャを使用し、他の PSI メソッドを呼び出したり PSI のクラスを継承したりできます。PSI 拡張機能では、新しい機能で必要とされるビジネス ロジックとデータベース アクセスも提供できます。
  
### <a name="using-the-csom"></a>CSOM を使用する
<a name="pj15_Programmability_CSOM"> </a>

CSOM を使用すると、Project Online またはオンプレミスの Project Server 2013 インストールにアクセスするアプリを開発できます。 アプリはパブリックな Office ストアまたはプライベートなアプリ カタログで配布できます。 CSOM は、データセットを渡して _changeXml_ パラメーターまたは XML の _filter_ パラメーターを作成するのではなく、LINQ クエリを使用して名前でデータを直接使用または提供する使いやすい API として開発されています。 CSOM は、**Project**, **Task**、**EnterpriseResource**、**Assignment** といった主要エンティティ向けの Project Server Interface (PSI) の主な機能を実装しています。 CSOM には、他の一般的な Project Server 機能をサポートする、**CustomField**、**LookupTable**、**WorkflowActivities**、**EventHandler**、**QueueJob** などの追加エンティティも多数含まれます。
  
CSOM は、次のリソースを開発用のローカル コンピューターにコピーすることによって使用できます。
  
- .NET Framework 4 開発の場合は、`%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\ISAPI\Microsoft.ProjectServer.Client.dll` アセンブリをコピーします。 
    
  CSOM クラスおよびメンバーについては、[Microsoft.ProjectServer.Client](https://docs.microsoft.com/previous-versions/office/dn529530(v=office.15)) 名前空間のドキュメントを参照してください。 サンプル アプリケーションについては、[「CSOM と .NET の作業を開始する」](getting-started-with-the-project-server-csom-and-net.md)を参照してください。
    
- Microsoft Silverlight の開発の場合は、`%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\ClientBin\Microsoft.ProjectServer.Client.Silverlight.dll` アセンブリをコピーします。 
    
- Windows Phone 8 用のアプリを開発するには、`%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\ClientBin\Microsoft.ProjectServer.Client.Phone.dll` アセンブリをコピーします。 
    
- JavaScript を使用して Web アプリやその他のデバイスのアプリを開発するには、`%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.js` ファイルと `PS.debug.js` ファイルをコピーします。 サンプル Web アプリについては、「[Project Server 2013 JavaScript オブジェクト モデルの概要](getting-started-with-the-project-server-2013-javascript-object-model.md)」を参照してください。
    
CSOM は内部的に PSI を呼び出します。そのため、PSI がジョブを実行できない場合は CSOM もできません。 CSOM の制限については、「[CSOM ができること、できないこと](what-the-csom-does-and-does-not-do.md)」および「[PSI ができること、できないこと](what-the-psi-does-and-does-not-do.md)」を参照してください。 CSOM を使用した開発の詳細については、「[Project 2013 での開発者向けの更新プログラム](updates-for-developers-in-project-2013.md)」および「[Project 2013 のクライアント側オブジェクト モデル (CSOM)](client-side-object-model-csom-for-project-2013.md)」を参照してください。
  
### <a name="porting-applications-built-for-project-server-2003"></a>Project Server 2003 用に構築されたアプリケーションを移植する
<a name="pj15_Programmability_Porting2003"> </a>

Project Server 2003 では、データや機能を利用するためには、多くの場合、Project Professional 2003 を使用するか、データベースに直接アクセスするしかありませんでした。Project Server 2007 で導入された PSI では、こうした制約の多くが取り除かれています。Project Server 2003 の Project Data Service (PDS) と異なり、PSI および CSOM は Project Server のビジネス オブジェクトに対する包括的なインターフェイスを提供しています。
  
PDS 用に開発されたアプリケーションは、それ以降のバージョンの Project Server と互換性がありません。CSOM および PSI は PDS と同等の機能を提供していますが、PDS のメソッドやパラメーターと完全には対応していません。
  
> [!NOTE]
> PDS アプリケーションは Project Server 2013 用に完全に再設計する必要があるため、CSOM の使用をお勧めします。 
  
PDS の互換性と、PDS 拡張機能を PSI に移植するためのガイドラインの詳細については、「[PSI Web サービスでの PDS パリティー](https://docs.microsoft.com/previous-versions/office/developer/office-2007/ms197081(v=office.12))」を参照してください。
  
### <a name="porting-applications-built-for-project-server-2007-and-project-server-2010"></a>Project Server 2007 および Project Server 2010 用に構築されたアプリケーションを移植する
<a name="pj15_Programmability_Porting2007"> </a>

Project Server 2013 の PSI は、Office Project Server 2007 および Project Server 2010 の PSI オブジェクト モデルのスーパーセットです。 これらの 2 つの前バージョンの Project Server 用に構築されたアプリケーションの多くは、ローカルの完全に信頼できる、オンプレミスの Project Server 2013 インストールでも引き続き使用できます。 ただし、次の種類のアプリケーションは更新または再設計が必要です。
  
- Project Online での使用に適応させたアプリケーションには、CSOM を使用します。
    
- モバイル デバイスやタブレット コンピューターでの使用に適応させたアプリケーションには、CSOM を使用します。
    
- Office ストアまたはプライベートなアプリ カタログでアプリとして提供されるアプリケーションには、CSOM を使用します。
    
- プロジェクトのスケジュールを変更するアプリケーションの場合は、CSOM を使用するか、[QueueUpdateProject2](https://docs.microsoft.com/previous-versions/office/project-class/jj236245(v=office.15)) PSI メソッドを使用するようにアプリケーションを変更してください。 
    
- ユーザーが Project Web App の複数のインスタンスにログオンするローカル アプリケーションまたは Web アプリケーションでは、CSOM または PSI の WCF エンドポイント用のプログラム設定を使用する必要があります。 これらのメソッドは非推奨です。 アプリを Project Online で使用するには、フォーム認証の代わりに OAuth 認証を使用する必要があります。 詳細については、「[SharePoint 2013 アプリの承認と認証](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/authorization-and-authentication-of-sharepoint-add-ins)」を参照してください。
    
- 特定の Project Server セキュリティ設定に依存したり変更を加えたりするアプリケーション。
    
  > [!NOTE]
  > Project Server 2013 の既定のオンプレミスのインストールでは、SharePoint のアクセス許可モードが使用されます。ここでは、PSI から Project Server のセキュリティ設定にアクセスできません。 Project のアクセス許可モードに変更するには、「[Project Server 2013 の IT 担当者向け新機能](https://docs.microsoft.com/project/what-s-new-for-it-pros-in-project-server-2016)」の「*SharePoint のアクセス許可モード*」セクションを参照してください。 
  
- 多くのカスタム Project Server ワークフローでは、SharePoint Designer 2013 を使用して宣言型ワークフローを作成できます。 追加のプログラミングを必要とするカスタム ワークフローに対しては、**Microsoft.Office.Project.Server.Workflow** 名前空間内でクラスまたはメンバーを直接 *使用しないでください*。 その代わりに、CSOM で [Microsoft.ProjectServer.Client.WorkflowActivities](https://docs.microsoft.com/previous-versions/office/mt780562(v=office.15)) クラスを使用します。 
    
- 一般に、偽装を使用するアプリケーションは、PSI の WCF インターフェイスを使用するように書き直す必要があります。 他のユーザーの単純なステータス更新を行うアプリケーションでは、偽装は必要ありません。 CSOM の [StatusAssignment.SubmitStatusUpdates](https://docs.microsoft.com/previous-versions/office/project-class/jj235883(v=office.15)) メソッド、または PSI の [Statusing.SubmitStatusForResource](https://docs.microsoft.com/previous-versions/office/ee755393(v=office.14)) メソッドを使用できます。 
    
- Project Server コンピューター上で実行されるミドルウェア コンポーネントは社内用としてのみインストールでき、PSI の WCF インターフェイスを使用する必要があります。 たとえば、ASMX インターフェイスを使用してオンプレミスの Project Web App と外部のタイムシート アプリケーションの間のデータ交換を行うミドルウェア コンポーネントは、PSI の WCF インターフェイスを使用するように書き直す必要があります。 Project Online で使用するためには、コンポーネントをアプリとして再設計し、CSOM を使用する必要があります。
    
### <a name="migration-and-compatibility-of-custom-solutions"></a>カスタム ソリューションの移行と互換性
<a name="pj15_Programmability_CustomSolutions"> </a>

PSI のパブリック ASMX と WCF インターフェイスのクラスとメンバーは同じです。 ただし、PSI メソッドで使用されたり返されたりするデータベースの列の数とサイズは、Project Server 2013 と 2 つの前バージョンの Project Server とで異なる場合があります。 以前のバージョンのレポート データベースと比べて、レポートのテーブルとビューにも違いがあります。
  
> [!IMPORTANT]
> 運用サーバーに展開する前に、Project Server 2013 の非運用インストールでソリューション全体をテストすることを強くお勧めします。 
  
ソリューションを Project Server 2013 に移行する場合、またはソリューションが意図したとおりに動作しない場合は、少なくとも次のことを行う必要があります。
  
- Visual Studio 2012 で開くことにより、ソリューションを更新します。 一部のソリューションでは、Visual Studio 2010 も使用できます。
    
- ターゲットを .NET Framework 4 に変更します。
    
- Microsoft.Office.Project.Server.Library.dll、Microsoft.Office.Project.Server.Events.Receivers.dll などの Project Server 2013 アセンブリを使用するように、アセンブリ参照を変更します。
    
- ASMX Web 参照または WCF サービス参照と名前空間名の一覧を作成し、Project Server の参照を削除します。
    
- Project 2013 SDK ダウンロードで WCF プロキシのソース ファイルから構築できる ProjectServerServices.dll プロキシ アセンブリを追加するか、必要な WCF サービス用のプロキシのソース ファイルを追加します。 ASMX サービスの場合は、同じ名前空間名を使用して、フロントエンドの ASMX Web サービス参照を再度追加します。または、Project 2013 SDK ダウンロードの WSDL ソースから構築できる、ProjectServerServices.dll プロキシ アセンブリを追加します。
    
  > [!NOTE]
  > Project 2013 SDK ダウンロードでは、プロキシ ソース ファイルの名前空間はすべて *Svc* で始まります。 たとえば、WCF プロキシ ファイルおよび ASMX プロキシ ファイル内の **Resource** サービスの名前空間は、**SvcResource** になります。 > 異なる名前空間名をアプリケーションで使用している場合は、その名前空間を使用するようにプロキシ アセンブリを再コンパイルするか、アプリケーションで PSI 名前空間を変更することができます。 たとえば、SDK ダウンロードの CompileWCFProxyAssembly.cmd スクリプトを変更し、プロキシ ソース ファイルから ProjectServerServices.dll を再コンパイルすることができます。 
  
- PSI の ASMX インターフェイスから WCF インターフェイスを使用するように変更する場合は、プログラムによって、または app.config の WCF エンドポイントを使用して、クライアント クラスを初期化できます。プログラムによる初期化は、Project Web App の別のインスタンスにすばやく切り替える必要があるときや、PSI を使用する Web パーツを開発しているときに使用します。
    
- Project Server 2013 の PSI サービスには、いくつかの新しいメソッドとデータセットがあり、いくつかの **DataRow** クラスには新しいプロパティが含まれています。 たとえば、PSI の [QueueUpdateProject2](https://docs.microsoft.com/previous-versions/office/project-class/jj236245(v=office.15)) メソッドは、Project Server のスケジュール エンジンを使用して、Project Professional 2013 でプロジェクトを開かなくても、更新されたプロジェクトを再スケジュールします。また、同じ呼び出しでプロジェクト エンティティを追加または削除することもできます。 
    
- ソリューションをコンパイルしてテストします。
    
## <a name="project-scheduling-on-the-server"></a>サーバー上でのプロジェクト スケジューリング
<a name="pj15_Programmability_Scheduling"> </a>

Project Server 2013 には 2 つのスケジューリング エンジンがあります。 新しい方のスケジューリング エンジンは、Project Professional 2013 のスケジューリング エンジンと同じです。 Project Web App またはプロジェクト サイトの [スケジュール] Web パーツ ([プロジェクトの詳細] ページ) か CSOM を使用してスケジュールを変更し、その変更を発行した場合、日付、コスト、期間、残存作業時間、基準計画、およびスケジュールに関するその他の変更の計算は、Project Professional 2013 を使用して変更およびプロジェクトの発行を行った場合と同じになります。 ただし、PSI メソッドは Project Server 2010 から移行された古いスケジューリング エンジンを使用します ([QueueUpdateProject2](https://docs.microsoft.com/previous-versions/office/project-class/jj236245(v=office.15)) メソッド以外)。 これは、従来のアプリケーションが Project Server 2013 でも以前と同じように動作するようにするためです。 
  
> [!NOTE]
> 更新されたスケジューリング エンジンを Project Server 2013 で使用するために、アプリケーションは CSOM を使用できます。 
  
新旧両方のスケジューリング エンジンには、以下の制限があります。
  
- **1 つのプロジェクトのスケジューリングのみ** スケジューリングは、変更が PSI、CSOM、または Project Web App を使用して、タスク状態の更新を通じて行われたときに、現在のプロジェクトにのみ影響します。 現在のプロジェクトに他のプロジェクト、サブプロジェクト、またはマスター プロジェクトへのリンクが存在する場合、リンクされたプロジェクトは変更されません。 
    
- **サマリー タスク** 一般に、Project Server 上のサマリー タスクは読み取り専用です。たとえば、サマリー タスクに対する割り当てを作成したり、達成率を変更したりすることはできません。しかし、Project Server は手動でスケジュールされたサマリー タスクの日付や期間を編集することはサポートしています。 
    
    Project Server の実績作業時間がサマリー タスクの割り当てに自動的に追加されることはありません。それは Project Server の承認プロセスをバイパスすることになるからです。Project Professional では、サブタスクに追加した実績作業時間はサマリー タスクの割り当てにも追加されます。この動作の違いがユーザーを混乱させることがあります。
    
    Project Server は、サブタスクの期間が短縮されるか、終了日が変更された場合に、サマリー タスクの割り当ての実績作業時間を削除します。
    
    > [!CAUTION]
    > Project Professional ではサマリー タスク上で割り当てを作成できますが、作成しないことをお勧めします。 
  
古い Project Server スケジューリング エンジンでの PSI プログラミングの問題と制限事項は以下のとおりです。
  
- **タスクのアクティブ ステータスを変更する** [QueueUpdateProject](https://docs.microsoft.com/previous-versions/office/ms471014(v=office.14)) メソッドを使用してタスクのアクティブ ステータスを変更する場合、_dataset_ パラメーターに関して **ProjectDataSet** オブジェクトに複数の変更があると、古い Project Server スケジューリング エンジンは矛盾した開始時間または終了時間を表示することがあります。 **QueueUpdateProject** の _dataset_ パラメーターでの唯一の変更が **TASK_IS_ACTIVE** プロパティの場合は、プロジェクトを変更できます。
    
    非アクティブなタスクおよび古いスケジューリング エンジンの詳細については、ブログ記事の「[Project 2010 の非アクティブ タスクについて](https://blogs.msdn.com/b/project/archive/2010/06/10/introducing-inactive-tasks-in-project-2010.aspx)」および「[Project Server 2010: Web、Web、PSI および Project Professional でのスケジュール設定](https://blogs.msdn.com/b/brismith/archive/2010/09/10/project-server-2010-scheduling-on-the-web-the-psi-and-project-professional.aspx?wa=wsignin1.0)」を参照してください。 Project Professional 2010 と Project Web App の Project Server 2010 でのスケジューリングの比較については、「[Web ベースのスケジュール管理の比較](https://blogs.msdn.microsoft.com/brismith/2010/09/10/project-server-2010-scheduling-on-the-web-the-psi-and-project-professional/)」を参照してください。
    
- **達成額は計算されない** 以前のスケジューリング エンジンは、達成額フィールド (ACWP、BAC、BCWP、BCWS、CPI、CV、CV%、EAC、SPI、SV、SV%、TCPI、VAC、期間差異、開始日の差異、終了日の差異、コスト差異、および作業時間の差異) を計算しません。プロジェクトがこれらのフィールドに値を持ち、そのプロジェクトが **QueueUpdateProject** メソッドを使用して更新された場合、これらのフィールドの値は変更されません。この問題を回避するには、**QueueUpdateProject2** メソッドを使用します。 
    
PSI のスケジューリングの制限事項には、以下の方法で対処できます。
  
- アプリケーションで必要なメソッドが CSOM にある場合は、PSI ではなく CSOM を使用する。
    
- Project Professional でプロジェクトを開き、Project Server に保存する。
    
- レポートに、PSI が更新しないフィールドは含めない。
    
- レポートに、データが古くなっている可能性があるという注意を記す。
    
レポート テーブルとキューブには、プロジェクト データの一部が更新されていないことを検出できるフラグがあります。MSP_EpmProject テーブルと MSP_EpmProject_UserView のレポート データには次のフィールドがあります。 
  
-  _ProjectWbsIsStale_ &ndash; 作業分割構造 (タスク アウトライン階層) が古いことを示します。 
    
-  _ProjectEarnedValueIsStale_ &ndash; 達成額フィールドが古いことを示します。 
    
-  _ProjectRollupsAreStale_ &ndash; サブプロジェクトが下書きデータベースで更新されているのに、マスター プロジェクトが更新されていないことを示します。サブプロジェクトからの重ね合わせた値が古くなっています。 
    
-  _ProjectHierarchyNotSynchronized_ &ndash; マスター プロジェクトがその子と同期されていません。この状態は、子プロジェクトがマスター プロジェクトの発行の一部ではなく、明示的に発行されたときに発生します。 
    
-  _ProjectCalculationsAreStale_ &ndash; Project Professional がスケジュールを計算せずにプロジェクトを保存しました (つまり、**[Project のオプション]** ダイアログ ボックスの **[スケジュール]** タブで、計算モードが **[手動]** に設定されています)。 
    
-  _ProjectGhostTaskAreStale_ &ndash; _ProjectHierarchyNotSynchronized_ に似ていますが、プロジェクト間のリンクのデータについて警告します。マスター プロジェクトが存在しないのに、リンクの一方のプロジェクト データが他方よりも新しい可能性があります。
    
## <a name="about-accessing-the-project-server-database"></a>Project Server データベースへのアクセスについて
<a name="pj15_Programmability_Databases"> </a>

Microsoft SQL Server で Project Server データベースへのアクセス許可を持っている場合は、レポート テーブルとビューを読み取ることができます。 必要な Project Server のアクセス許可を持っている場合は、OData クエリを使用して、レポート テーブルからデータを読み取ることもできます。 開発者には、Project Server データベースで下書きテーブル、発行済みテーブル、またはアーカイブ テーブルに SQL Server のクエリを通じて直接アクセスしないことを強く推奨します。 Project Server データベースでいずれかのテーブルに直接変更を加えると、参照整合性が損なわれたり、Project Server キュー サービスを通じたデータベース アクセスと干渉したりする可能性があります。
  
> [!IMPORTANT]
> プログラムによってデータベースに直接アクセスしてデータを更新することを能動的に妨げるものは存在しません。Project Professional キャッシュ、発行済みテーブル、およびレポート テーブルはすべてがキャッシュ同期プロトコルに依存しているので、直接データを編集すると同期が混乱する可能性があることに注意が必要です。直接アクセスしてデータを変更することによって、Project Server データベースや Project Professional クライアント側キャッシュが破損した場合、製品サポートは役に立てません。 
  
下書きテーブル、発行済みテーブル、アーカイブ テーブル、およびビューに直接アクセスするアプリケーションは、データベース スキーマにも依存します。データベース スキーマは Project Server 2013 のサービス パックや将来のバージョンで変更される可能性があります。 データベースに直接アクセスするアプリケーションも、組み込みの Project Server セキュリティ、共通ビジネス ロジック、追跡、監査、エラー チェック、レポート、ワークフローなどの機能を利用できません。 こうしたアプリケーションは、Project Server 2013 の更新後に書き換える必要性が高くなります。 
  
以上の理由により、Project Professional と Project Web App は、下書きテーブル、発行済みテーブル、またはアーカイブ テーブルへの直接呼び出しを行いません。Project Server と統合される他のアプリケーションでも、そのような呼び出しは避ける必要があります。
  
下書きテーブル、発行済みテーブル、およびアーカイブ テーブルのスキーマは文書化されていません。 レポートの生成を支援するために、レポート テーブルを使用できます。レポート テーブルとビューのスキーマは Project 2013 SDK ダウンロードで文書化されています。 レポート データの OData スキーマについては、「[ProjectData - Project OData サービス参照](https://docs.microsoft.com/previous-versions/office/project-odata/jj163015(v=office.15))」を参照してください。
  
## <a name="see-also"></a>関連項目

- [Project 2013 における開発者向けの更新内容](updates-for-developers-in-project-2013.md)    
- [Project Server 2013 のアーキテクチャ](project-server-2013-architecture.md)    
- [PSI ができること、できないこと](what-the-psi-does-and-does-not-do.md)   
- [CSOM ができること、できないこと](what-the-csom-does-and-does-not-do.md)    
- [Project 2013 のクライアント側オブジェクト モデル (CSOM)](client-side-object-model-csom-for-project-2013.md)    
- [Project Server ワークフロー開発の作業開始](getting-started-developing-project-server-workflows.md)    
- [Project 2013 プログラミング リファレンス](project-2013-programming-references.md)    
- [Project PSI リファレンスの概要](project-psi-reference-overview.md)    
- [カスタム アクションを作成して SharePoint アプリで展開する](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/create-custom-actions-to-deploy-with-sharepoint-add-ins)    
- [Project 2010 の非アクティブなタスクの概要](https://blogs.msdn.com/b/project/archive/2010/06/10/introducing-inactive-tasks-in-project-2010.aspx)    
- [Project Server 2010: Web、PSI、および Project Professional でのスケジューリング](https://blogs.msdn.microsoft.com/brismith/2010/09/10/project-server-2010-scheduling-on-the-web-the-psi-and-project-professional/)

