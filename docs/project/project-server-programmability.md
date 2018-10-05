---
title: Project Server プログラミング
manager: soliver
ms.date: 09/17/2015
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
- プロジェクト 2013、アーキテクチャおよびプログラミング、PSI、プロジェクト、バージョンでは、プログラミング、サーバーのプロジェクト、PSI では、Project Server のインターフェイスの制限事項には、機能では、Project Server インターフェイスでは、PDS の互換性のため、Project Server インターフェイスでは、ジェネリックがサポートされていません。サーバーのプロジェクト、プロジェクトのバージョンは、バージョンでは、プロジェクトでは、プロジェクトのサーバー、データベース、Project 2013 では、プラットフォームでは、Project Server のインターフェイスを使用して、シナリオでは、Project Server では、イベント、プロジェクトのサーバー、プロジェクト データ サービス、PSI、Project Server との互換性インタ フェース
localization_priority: Normal
ms.assetid: a93d2153-5132-4289-af51-69350471e248
description: Project Server 2013 の主なプログラミング機能について説明します。 この資料には、Project Server の以前のバージョンでビルドされたアプリケーションの移植に関する情報が含まれています。
ms.openlocfilehash: 57802cf8ce1597b759201ef1e2a0ea9bd1e394b1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386734"
---
# <a name="project-server-programmability"></a>Project Server プログラミング

Project Server 2013 の主なプログラミング機能について説明します。 この資料には、Project Server の以前のバージョンでビルドされたアプリケーションの移植に関する情報が含まれています。

Project Server 2013 は、Project Server 2010、新しいソリューションの複数のプラットフォームでは、アプリケーションがアクセスできる場所両方オンラインとプロジェクトのサーバー設置のために開発されたほとんどのアプリケーションをサポートするよう設計されています。 クライアント側オブジェクト モデル (CSOM) またはプロジェクト Server インターフェイス (PSI) を使用するのには、アプリケーションと Project Server 2003 またはそれ以前に開発された拡張機能を再設計する必要があります。 Office Project Server 2007 の Project Server 2010 で開発されたアプリケーションはいくつかの変更とは、PSI を使用して再コンパイルする必要があります。これらのアプリケーションでは、CSOM を使用するには、再設計が必要です。
  
Project Server プラットフォームでは、SharePoint Server 2013、.NET Framework 4、および、CSOM で OData プロトコルをベースにした高レベルのプログラマの生産性を使用できます。 開発者は、アプリケーション、アプリケーションの部分、および Web パーツを使用して Project Web App を拡張、SharePoint Designer 2013 を使用してワークフローを定義および Project Server のイベントのリモート イベント レシーバーを使用してビジネス ルールを適用することができます。
  
## <a name="project-server-and-sharepoint-server"></a>Project Server と SharePoint Server
<a name="pj15_Programmability_MOSS"> </a>

Project Web App は、SharePoint Server 2013 とマスター ページおよび Web パーツを使用して、カスタム アプリケーションと Project Web App のソリューションを構築しやすくします。 プロジェクトの共同作業、レポート作成、サイトの管理、セキュリティ、およびワークフローの管理のためのプラットフォームとして、Project Server 2013 が SharePoint Server 2013 では深く統合されます。
  
プロジェクト サイトの詳細を含めるし、成果物、プロジェクトのサマリー情報や専門的な SharePoint リストでは、タイムライン、追跡の問題、リスク、タスクのプロジェクトを含む既定のアプリケーションを追加するときは、チーム メンバーの共同作業のオプションと、チームの予定表、ドキュメント ライブラリ、およびチームのディスカッションとします。 Project Server 2013 のカスタム アプリケーションは、拡張機能と共同作業の柔軟性を提供します。 追加し、ページを編集するときに Web パーツを編集するのと同じメカニズムを使用して、アプリケーションをカスタマイズするのにはアプリケーションのパーツを追加することもできます。 Project Server がインストールされている SharePoint ファーム内の任意の場所のプロジェクトのサイトを見つけることができます。 Excel Services と、エンタープライズ検索など、SharePoint Server 2013 のコア サービスを使用するには、管理者を有効にして、サービスを構成します。 
  
Project Server 2013 をインストールするときに、SharePoint Web サービス サイトのプロジェクト サービス アプリケーションを準備します。 プロジェクト サービス アプリケーションには、ローカルの Windows Communication Foundation (WCF) サービスと、PSI の ASMX web サービスが含まれています。 サービス アプリケーションの他の例には、SharePoint の検索と SharePoint ドキュメントの管理が含まれます。 詳細については、SharePoint Server 2013 の開発者向けドキュメントを参照してください。
  
プロジェクト サービス アプリケーションは、Project Web App の複数のインスタンスを管理できる論理サービス プロバイダーです。 プロジェクト サーバーのプロビジョニングは、SharePoint web アプリケーション内で特定の Project Web App サイトを作成します。 Project Web App のホーム ページには、[プロジェクト センター] ページ、リソース センター] ページで、レポート、ビジネス インテリジェンス センターのページおよびその他の標準的なアプリケーションの一覧を含むページへのリンクが含まれています。 図 1 は、**設定**のドロップ ダウン リストを追加する Web パーツを編集することができる Project Web App のホーム ページ上で**の編集] ページ**のコマンドを示します。 
  
> [!NOTE]
> Project Web App でいくつかの管理ページ、PWA の設定] ページなど、編集可能にしていないし、**ページの編集**] コマンドを表示しません。 Project Web App では、SharePoint Designer 2013 を使用してページを編集できません。 SharePoint Designer 2013 を使用してプロジェクト サイトのページを編集することができます。 
  
**図 1. Project Web App の [ページの編集] メニューの使用**

![Project Web Access のホーム ページの編集](media/pj15_Programmability_PWAHome.gif "Project Web Access のホーム ページの編集")
  
Project Web App で [サイト設定] ページにアクセスするには、ページの右上隅で**設定**アイコンを選択します。 [サイト設定] ページ ( `https://ServerName/ProjectServerName/_layouts/15/settings.aspx`) の外観と印象およびサイトのテーマを変更することにより、カスタムの Web パーツを追加し、変更または作成マスター プロジェクト サイトのページです。
  
ASPX ページのコードをカスタマイズまたは SharePoint Designer 2013 では、Project Web App のマスター ページのカスタマイズはサポートされていません。 Project Web App ページ内のコードのカスタマイズには、Project Server の更新プログラムおよび service pack で問題が発生します。 
  
### <a name="customization-of-project-web-app-with-sharepoint-packages"></a>SharePoint パッケージによる Project Web App のカスタマイズ
<a name="pj15_Programmability_CustomizationOfPWA"> </a>

Project Web App では、SharePoint アプリケーションの場合は、プロジェクトのサイトは、SharePoint サイト、SharePoint パッケージ (.wsp ファイル) または SharePoint アプリケーション (.spapp ファイル) を使用して、カスタム アプリケーション、Web パーツ、イベント ハンドラー、カスタム フィールド、およびその他の機能を追加できます。 SharePoint パッケージまたは、アプリケーション パッケージには、elements.xml ファイル パッケージ内のエンティティの定義が指定されている、Project Server の複数のエンティティを含めることができます。
  
オンラインのプロジェクトの Project Web App のリボンにボタンを追加することができますが、削除または、既存の製品のボタンの名前を変更することはできず、新しいリボン タブを作成することはできません。 詳細については、 [SharePoint のアプリケーションと共に配置するカスタム アクションの作成](https://msdn.microsoft.com/library/office/apps/jj163954%28v=office.15%29.aspx)を参照してください。
  
> [!CAUTION]
> SharePoint パッケージまたはアプリ パッケージのインストール時には、Project Server エンティティの種類が PSEntityProvision.xsd スキーマに指定された順序で出現する必要があります。そうでない場合、パッケージのスキーマ検証が失敗し、インストールは完了しません。 
  
PSEntityProvision.xsd スキーマ ファイルは、Project 2013 SDK のダウンロードに使用可能で、`Documentation\Schemas\AppProvisioning`のサブディレクトリです。 図 2 は、 **LookupTable**シーケンスが展開されている、 **PSEntityProvision**スキーマの Visual Studio で XML スキーマのエクスプ ローラー ビューを示しています。 
  
**図 2. Project Server エンティティ準備スキーマの Visual Studio ビュー**

![Project Server エンティティのスキーマの表示](media/pj15_Programmability_EntitySchema.gif "Project Server エンティティのスキーマの表示")
  
Project Server 用の機能をインストールする SharePoint パッケージには、**PSEntityProvision** スキーマに従った elements.xml ファイルを 1 つまたは複数含めることができます。1 つの XML ファイル内の Project Server エンティティは、次の順序で出現する必要があります。 
  
1. ワークフロー フェーズ
    
2. 参照テーブル
    
3. ユーザー設定フィールド
    
4. ワークフロー ステージ
    
5. エンタープライズ プロジェクトの種類
    
6. イベント ハンドラー
    
Project Server エンティティを含む SharePoint パッケージを作成するときに、複数の elements.xml ファイルにエンティティ定義を含めることができます。各 XML ファイルがスキーマ検証に合格しても、パッケージ全体ではエンティティの順序が正しくない可能性があります。たとえば、最初の XML ファイル内のユーザー設定フィールド エンティティが 2 番目の XML ファイル内の参照テーブルを参照している場合があります。インストール時には、参照テーブルがまだ作成されていないため、ユーザー設定フィールドを作成できません。
  
パッケージのインストールが失敗した場合、Project Web App に作成されたオブジェクトがあるが、パッケージが完全にインストールされません。 パッケージを再インストールできる機能しますが、お客様にとって適切な環境ではありません。 エンティティの定義は、複数の elements.xml ファイルにまたがる、ときに、SharePoint パッケージのインストールが正しい順序に従っていることを確認するのには全体の Project Server エンティティを整理します。 Project 2013 SDK ダウンロードの PSEntityProvision.xsd スキーマには、XML ファイル内のエンティティの指定順序をチェックするツールを開発することです。
  
## <a name="upgrading-applications-with-the-project-server-apis"></a>Project Server API によるアプリケーションのアップグレード
<a name="pj15_Programmability_APIs"> </a>

前のバージョンの Project Server 向けに開発されたアプリケーションをアップグレードする場合は、プロジェクト エンティティの作成、読み取り、更新、および削除のためのメソッド (CRUD 操作) を含むプログラム インターフェイスとして CSOM と PSI のどちらを使用するかを選択できます。CSOM は内部で PSI を呼び出しますが、すべての PSI メソッドに完全に代わるものではありません。PSI と CSOM のシナリオと制約については、「[What the PSI does and does not do](what-the-psi-does-and-does-not-do.md)」および「[What the CSOM does and does not do](what-the-csom-does-and-does-not-do.md)」を参照してください。
  
> [!NOTE]
> CSOM には、必要な機能が含まれている場合は、CSOM を使用するアプリケーションをアップグレードすることをお勧めします。 CSOM は、オンプレミスと Project Server 2013 のオンライン インストールの両方に使用するアプリケーションを有効にします。 
  
主に、アプリケーションは、Project Server からデータを読み取り場合、は、社内設置型のシナリオでは、Project Server データベースにレポートのテーブルとビューを使用できます。 プロジェクトをオンラインでアプリケーションを使用する場合は、OData プロトコルを使用して、 **ProjectData**サービスは、設置型とレポートのデータをオンライン ・ アクセスの両方を提供することができます。 詳細については、 [ProjectData - プロジェクトの OData サービスの参照](https://msdn.microsoft.com/library/office/jj163015.aspx)を参照してください。
  
### <a name="using-the-psi"></a>PSI の使用
<a name="pj15_Programmability_PSI"> </a>

PSI には、SharePoint ファーム内の Project Server データにアクセスするのには、評価のためのプロジェクトを Project Web App では、LOB アプリケーションを含む、完全信頼クライアント アプリケーションが有効にします。 PSI がビルドされ、.NET Framework 4 で使用し、組み込みのセキュリティ、エラー処理、およびガベージ コレクションなどのよく知られている開発環境を提供します。
  
PSI は、WCF サービスまたは ASMX web サービスを介してアクセスされます。 ASMX インターフェイスは、WCF に基づいています。 各 PSI サービスには通常、そのクラス内の項目に対して CRUD メソッドを基本クラスが含まれます。 アイテムは、関連する**データセット**クラスによって指定されます。 など**名**サービスには、 [CreateCustomFields2](https://msdn.microsoft.com/library/WebSvcCustomFields.CustomFields.CreateCustomFields2.aspx)などの方法でクラス**名**が含まれています。 1 つまたは複数のエンタープライズ ユーザー設定フィールドのデータは、 **CustomFieldDataSet**で指定されます。
  
> [!NOTE]
> Project Server 2013 では、PSI は、ASMX web サービス インターフェイスは推奨されていません。 ASMX インターフェイスは利用できますが、PSI を使用する新しいアプリケーションは、WCF インターフェイスを使用する必要がありますか、可能であれば、新しいアプリケーションは PSI のではなく、CSOM を使用する必要があります。 Project Server の将来のバージョンには、既存の ASMX ベース アプリケーション、PSI の WCF インターフェイスを使用するか、CSOM を使用するアップグレードが必要です。 
  
22 があるパブリック PSI サービスは、WCF インターフェイスおよび ASMX インターフェイス内で重複して、文書化します。 PSI には、8 つのプライベートな非公開のサービスも含まれています。 Project Web App と Project Professional は、PSI サービスをパブリックとプライベートの PSI サービスを使用します。 PSI は、ビジネス オブジェクトに一致するように一般的に考慮されます。 各 PSI メソッドは、**カレンダー**や**リソース**などのビジネス オブジェクトに関連付けられています。 PSI は、ビジネス オブジェクトをプライマリ インターフェイスです。 ビジネス層では、再利用可能なビジネス ロジック コンポーネントを提供するため、Project Server データと対話するさまざまなアプリケーションは、同じビジネス ロジックを使用します。
  
Project Server で非同期的にデータをやり取りする PSI メソッドは、**キュー**で始まる名前を持ちます。 各 PSI メソッドは、別のインターフェイスを使用して厳密型指定されたデータで実装されます。 たとえば、**プロジェクト**のサービスの**QueueCreateProject**メソッドは、 **ProjectDataSet**の種類の_データセット_パラメーターを受け付けます。 **ProjectDataSet**クラスは**データセット**の型から派生します。 PSI を使用して開発で発生したエラーを減らすために、Visual Studio ヘルプの.NET Framework と IntelliSense の入力候補でチェックを入力します。 PSI の名前空間、クラス、メソッド、プロパティ、イベント、および関連アセンブリの詳細なリファレンスの概要については、[プロジェクトの PSI リファレンスの概要](project-psi-reference-overview.md)を参照してください。
  
Project Server 2013 では、.NET Framework の例外処理を使用します。 PSI スタックの最上部にある、サーバーでは、すべてのエラーが記録されます。 いくつかのエラーでは、ASMX インターフェイス用の**SoapException**オブジェクトまたは WCF インターフェイスの**FaultException**オブジェクトなどのクライアントに簡単なレポートを送信します。 例外は、アプリケーション イベント ログに記録でき、いくつかのエラーがサーバー上の詳細なレポートをユニファイド ログ サービス (ULS) トレース ログにも記録します。 
  
ローカルの完全信頼アプリケーションに対しても、PSI は拡張性に優れています。サービスを含む .NET アセンブリを追加し、そこで新しい機能を提供し、同じ Project Server セキュリティ インフラストラクチャを使用し、他の PSI メソッドを呼び出したり PSI のクラスを継承したりできます。PSI 拡張機能では、新しい機能で必要とされるビジネス ロジックとデータベース アクセスも提供できます。
  
### <a name="using-the-csom"></a>CSOM の使用
<a name="pj15_Programmability_CSOM"> </a>

CSOM では、プロジェクトのオンラインまたはオンプレミスの Project Server 2013 のインストールにアクセスするアプリケーションを開発できます。 Office のパブリック ストアまたはプライベート アプリ カタログでは、アプリケーションを配布できます。 CSOM は、使用する API を直接消費するデータセットを渡すと、 _changeXml_パラメーターまたは XML_フィルター_パラメーターを作成するではなく、LINQ クエリでは、名前によって、データを提供するよう設計されています。 CSOM は、**プロジェクト**、**タスク**、 **EnterpriseResource**、および**割り当て**などのプライマリ エンティティのプロジェクト Server インターフェイス (PSI) の主な機能を実装します。 CSOM には、**カスタム フィールド**など**LookupTable**、 **WorkflowActivities**、**イベント ハンドラー**、 **QueueJob**、その他の一般的なプロジェクトのサーバーの機能をサポートしているその他さまざまなエンティティが含まれています。
  
CSOM は、次のリソースをローカルの開発用コンピューターにコピーすることによって使用できます。
  
- .NET Framework 4 の開発のためのコピー、`%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\ISAPI\Microsoft.ProjectServer.Client.dll`のアセンブリです。 
    
  CSOM のクラスとメンバーのドキュメントについては、 [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx)名前空間を参照してください。 サンプル アプリケーションでは、 [CSOM および .NET の概要](getting-started-with-the-project-server-csom-and-net.md)を参照してください。
    
- Microsoft Silverlight の開発のためのコピー、`%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\ClientBin\Microsoft.ProjectServer.Client.Silverlight.dll`のアセンブリです。 
    
- Windows Phone 8 のアプリを開発するには、コピー、`%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\ClientBin\Microsoft.ProjectServer.Client.Phone.dll`のアセンブリです。 
    
- Web アプリケーションおよびその他のデバイス用のアプリケーションを開発するための JavaScript を使用するには、コピー、`%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.js`ファイルと`PS.debug.js`ファイルです。 例 web アプリケーションでは、 [Project Server 2013 の JavaScript オブジェクト モデルの概要](getting-started-with-the-project-server-2013-javascript-object-model.md)を参照してください。
    
は PSI を内部的に呼び出して、CSOMしたがって、PSI には、ジョブを実行できない、どちらもことができます、CSOM。 CSOM の制限については、[どのような「CSOM は行われない](what-the-csom-does-and-does-not-do.md)し、、[何の PSI を行い、実行できない](what-the-psi-does-and-does-not-do.md)を参照してください。 CSOM を使用した開発の詳細については、 [Project 2013 の開発者用の更新プログラム](updates-for-developers-in-project-2013.md)および[Project 2013 のクライアント側オブジェクト モデル (CSOM)](client-side-object-model-csom-for-project-2013.md)を参照してください。
  
### <a name="porting-applications-built-for-project-server-2003"></a>Project Server 2003 用に構築されたアプリケーションの移植
<a name="pj15_Programmability_Porting2003"> </a>

Project Server 2003 では、データや機能を利用するためには、多くの場合、Project Professional 2003 を使用するか、データベースに直接アクセスするしかありませんでした。Project Server 2007 で導入された PSI では、こうした制約の多くが取り除かれています。Project Server 2003 の Project Data Service (PDS) と異なり、PSI および CSOM は Project Server のビジネス オブジェクトに対する包括的なインターフェイスを提供しています。
  
PDS 用に開発されたアプリケーションは、それ以降のバージョンの Project Server と互換性がありません。CSOM および PSI は PDS と同等の機能を提供していますが、PDS のメソッドやパラメーターと完全には対応していません。
  
> [!NOTE]
> PDS アプリケーションは、Project Server 2013 を一新する必要があります、ため、CSOM を使用することをお勧めします。 
  
PDS の互換性の詳細と PDS 拡張機能を PSI に移植するときのガイドラインについては、「[PDS Parity in PSI Web Services](https://msdn.microsoft.com/library/61a0b0c7-9b74-46d1-87ed-66ffdd8017f8%28Office.15%29.aspx)」を参照してください。
  
### <a name="porting-applications-built-for-project-server-2007-and-project-server-2010"></a>Project Server 2007 および Project Server 2010 用に構築されたアプリケーションの移植
<a name="pj15_Programmability_Porting2007"> </a>

Project Server 2013 の PSI は、Office Project Server 2007 と Project Server 2010 のオブジェクト モデルに PSI のスーパー セットです。 Project Server の 2 つの以前のバージョン用に作成された多くのアプリケーションは、Project Server 2013 のローカルの完全信頼、オンプレミスのインストール環境で作業を続けます。 ただし、次のようなアプリケーションには、更新または再設計が必要です。
  
- プロジェクトをオンラインで使用するために適用されるアプリケーションは、CSOM を使用します。
    
- モバイル デバイスおよびタブレット コンピューターでの使用に適応させたアプリケーションには、CSOM を使用します。
    
- Office ストアまたはプライベート アプリ カタログでのアプリケーションとして利用可能なアプリケーションは、CSOM を使用します。
    
- アプリケーション プロジェクトのスケジュールを変更する場合は、CSOM を使用して、または[QueueUpdateProject2](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject2.aspx)の PSI メソッドを使用してアプリケーションを変更します。 
    
- ローカル ユーザーが Project Web App の別のインスタンスにログオンする web アプリケーションは、CSOM または PSI の WCF エンドポイントのプログラムの設定を使用する必要がありますか。 メソッドは推奨されていません。 アプリケーションは、プロジェクトをオンラインでフォーム認証の代わりに、使用するために、OAuth 認証を使用する必要があります。 詳細については、 [SharePoint 2013 でのアプリケーションの認証および承認](https://msdn.microsoft.com/library/fp142384%28office.15%29.aspx#FileName_uniquekeyword1)を参照してください。
    
- 特定の Project Server セキュリティ設定に依存するか、それを変更するアプリケーション。
    
  > [!NOTE]
  > Project Server 2013 の既定の設置型インストールでは、Project Server のセキュリティ設定は、PSI を使用してアクセスできない SharePoint アクセス許可モードを使用します。 プロジェクトのアクセス権モードに変更するには、 [Project Server 2013 の IT プロフェッショナル向けの新規](https://technet.microsoft.com/en-us/library/ff631142%28office.15%29.aspx#section13)の*SharePoint アクセス許可モード*を参照してください。 
  
- 多くのカスタム Project Server ワークフローの宣言型ワークフローを作成するのに SharePoint Designer 2013 を使用できます。 追加のプログラミングを必要とするカスタム ワークフローにする必要があります*いない*直接のクラスまたはメンバー **Microsoft.Office.Project.Server.Workflow**名前空間を使用します。 代わりに、CSOM で[Microsoft.ProjectServer.Client.WorkflowActivities](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.WorkflowActivities.aspx)クラスを使用します。 
    
- 一般に、偽装を使用するアプリケーションは、PSI の WCF インターフェイスを使用して書き直す必要があります。 他のユーザーの簡易ステータスの更新を行うアプリケーションでは、偽装は必要ありません。 [StatusAssignment.SubmitStatusUpdates](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.StatusAssignment.SubmitStatusUpdates.aspx) CSOM または PSI の[Statusing.SubmitStatusForResource](https://msdn.microsoft.com/library/WebSvcStatusing.Statusing.SubmitStatusForResource.aspx)メソッドを使用することができます。 
    
- Project Server コンピューター上で実行されるミドルウェア コンポーネントでは、設置型で使用するためだけにインストールすることができ、PSI の WCF インターフェイスを使用する必要があります。 たとえば、Project Web App の設置型の間でデータを交換するため、asmx サービスを使用しているミドルウェア コンポーネントのインターフェイスし、外部タイムシート アプリケーションは、PSI の WCF インターフェイスを使用して書き換える必要があります。 オンライン プロジェクトを操作するには、コンポーネントがアプリケーションとして再設計し、CSOM を使用する必要があります。
    
### <a name="migration-and-compatibility-of-custom-solutions"></a>カスタム ソリューションの移行と互換性
<a name="pj15_Programmability_CustomSolutions"> </a>

PSI のパブリック ASMX と WCF インターフェイスのクラスとメンバーと同じです。 列の数、または使用して、PSI メソッドによって返されるデータのテーブルのサイズは、Project Server 2013 の 2 つの以前のプロジェクトのサーバー バージョンでは異なる。 レポート テーブルおよびビューを以前のバージョンのレポート データベースと比較しての違いもあります。
  
> [!IMPORTANT]
> 運用サーバーに展開する前に Project Server 2013 の非本番環境でのソリューションを徹底的にテストすることを強くお勧めします。 
  
Project Server 2013 では、ソリューションに移行するか、期待どおりに解決策がうまくいかない場合は最低限にする必要があるときは、次の操作を行います。
  
- Visual Studio 2012 で開くことによってソリューションを更新します。 いくつかのソリューションは、Visual Studio 2010 を使用することもできます。
    
- ターゲットを.NET Framework 4 に変更します。
    
- Microsoft.Office.Project.Server.Library.dll および Microsoft.Office.Project.Server.Events.Receivers.dll など、Project Server 2013 のアセンブリを使用するには、アセンブリの参照を変更します。
    
- ASMX Web 参照または WCF サービス参照と名前空間名の一覧を作成し、Project Server 参照を削除します。
    
- Project 2013 SDK ダウンロードでは、WCF プロキシ ソース ファイルからビルドまたは必要な WCF サービスのプロキシのソース ファイルを追加することができます ProjectServerServices.dll プロキシ アセンブリを追加します。 ASMX サービスでは、ASMX web サービスの参照は、フロント エンド、もう一度を使用して追加、同じ名前空間の名前です。または、Project 2013 SDK ダウンロードの WSDL のソースからビルドすることができます ProjectServerServices.dll プロキシ アセンブリを追加します。
    
  > [!NOTE]
  > Project 2013 SDK ダウンロードには、プロキシ ファイルの名前空間は、 *Svc*のすべての開始をファイルします。 たとえば、**リソース**サービスの名前空間、ASMX プロキシ ファイルに WCF プロキシ ファイルには、 **SvcResource**です。 > アプリケーションでは、異なる名前空間の名前を使用する場合、名前空間を使用するプロキシ アセンブリを再コンパイルしてか、アプリケーションで PSI の名前空間を変更します。 たとえば、CompileWCFProxyAssembly.cmd スクリプトを変更し、SDK のダウンロードにプロキシのソース ファイルから ProjectServerServices.dll を再コンパイルできます。 
  
- インターフェイスを使用して、ASMX、PSI の WCF インターフェイスから変更する場合は、プログラムまたは app.config で WCF エンドポイントを使用してクライアント クラスを初期化できます。Project Web App では、別のインスタンスをすばやく切り替える必要があるとき、または、PSI を使用する web パーツを開発しているときは、プログラムの初期化を使用します。
    
- いくつかの新しい方法があるし、Project Server 2013 と**DataRow**クラスがいくつかの PSI サービス内のデータセットに新しいプロパティが含まれています。 PSI の[QueueUpdateProject2](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject2.aspx)メソッドの評価のためのプロジェクトでプロジェクトを開く必要はありません、更新されたプロジェクトのスケジュールを変更するのには Project Server スケジュール エンジンを使用して、追加またはプロジェクト内のエンティティを削除することができますなど同じ呼び出しします。 
    
- ソリューションをコンパイルしてテストします。
    
## <a name="project-scheduling-on-the-server"></a>サーバー上でのプロジェクト スケジューリング
<a name="pj15_Programmability_Scheduling"> </a>

Project Server 2013 には、2 つのスケジュール エンジンがあります。 新しいスケジューリング エンジンは、スケジュール エンジンは、評価のためのプロジェクトと同じです。 スケジュールの変更または、CSOM では、日付、コスト、期間の計算を使用して、Project Web App またはプロジェクトのサイトでは、スケジュールの web パーツ ([プロジェクトの詳細] ページ) を使用して変更内容を発行すると残りの作業時間、基準、および関連するその他の変更スケジュールには、同じ変更を行ったし、評価のためのプロジェクトを使用してプロジェクトを発行する場合とします。 ただし、PSI メソッドを除いて、 [QueueUpdateProject2](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject2.aspx)メソッドでは、Project Server 2010 を反映した古いスケジュール エンジンを使用してください。 理由は、従来のアプリケーションと同じ働きを Project Server 2013 で以前に行ったことを確認します。 
  
> [!NOTE]
> Project Server 2013 の更新のスケジュール管理エンジンを使用するには、アプリケーションは、CSOM を使用できます。 
  
古いスケジューリング エンジンと新しいスケジュール エンジンにはいずれも、以下の制約事項があります。
  
- **スケジューリングだけ 1 つのプロジェクト**スケジュール PSI または、CSOM または Project Web App のタスク ステータスの更新によって変更されると、現在のプロジェクトのみに影響します。 現在のプロジェクトに他のプロジェクト、サブプロジェクト、またはマスター プロジェクトへのリンクがある場合は、リンクされたプロジェクトは変更されません。 
    
- **サマリー タスク**サマリー タスクは一般に読み取り専用プロジェクト サーバーにします。 などのサマリー タスクの割り当てを作成することはできませんし、完了のパーセントを変更することはできません。 ただし、Project Server では、日付と手動でスケジュールされたサマリー タスクの期間を編集はサポートします。 
    
    Project Server の実績作業時間がサマリー タスクの割り当てに自動的に追加されることはありません。それは Project Server の承認プロセスをバイパスすることになるからです。Project Professional では、サブタスクに追加した実績作業時間はサマリー タスクの割り当てにも追加されます。この動作の違いがユーザーを混乱させることがあります。
    
    Project Server は、サブタスクの期間が短縮されるか、終了日が変更された場合に、サマリー タスクの割り当ての実績作業時間を削除します。
    
    > [!CAUTION]
    > Project Professional ではサマリー タスク上で割り当てを作成できますが、作成しないことをお勧めします。 
  
古い Project Server スケジューリング エンジンでの PSI プログラミングの問題と制限事項は以下のとおりです。
  
- **タスクの現在のステータスを変更します。** Project Server の以前のスケジュール エンジンが一貫性のないスタートを表示または終了時刻は、タスクの現在のステータスを変更するのには、 [QueueUpdateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx)メソッドを使用する場合、_の**ProjectDataSet**オブジェクトで複数の変更がある場合データセット_のパラメーターです。 **TASK_IS_ACTIVE**プロパティが**QueueUpdateProject**の_データセット_のパラメーターの変更のみの場合は、プロジェクトを更新することができます。
    
    非アクティブなタスクと古いスケジュール エンジンの詳細については、ブログ記事の[Project 2010 で使用頻度の低いタスクの概要](https://blogs.msdn.com/b/project/archive/2010/06/10/introducing-inactive-tasks-in-project-2010.aspx)を参照してくださいと[Project Server 2010: PSI と Project Professional は、web 上でスケジュールを設定する](https://blogs.msdn.com/b/brismith/archive/2010/09/10/project-server-2010-scheduling-on-the-web-the-psi-and-project-professional.aspx?wa=wsignin1.0)です。 Project Professional 2010 と Project Server 2010 で、Project Web App でのスケジュール設定の比較とは、 [Web ベースのスケジュール管理の比較](https://blogs.msdn.microsoft.com/brismith/2010/09/10/project-server-2010-scheduling-on-the-web-the-psi-and-project-professional/)を参照してください。
    
- **達成値は計算されません。** 古いスケジュール エンジンでは、達成額フィールドは計算されません。 ACWP、BAC、BCWP、BCWS、CPI、CV、CV %、EAC、SPI、SV、SV %、TCPI、VAC、[期間差異]、開始日の差異、終了日の差異、コストの差異、および作業時間の差異。 プロジェクトにこれらのフィールドの値があり、ユーザーが**QueueUpdateProject**メソッドを使用してプロジェクトを更新は、フィールドの値は変更されません。 問題を避けるためには、 **QueueUpdateProject2**メソッドを使用します。 
    
PSI のスケジューリングの制限事項には、以下の方法で対処できます。
  
- アプリケーションで必要なメソッドが CSOM にある場合は、PSI ではなく CSOM を使用する。
    
- Project Professional でプロジェクトを開き、Project Server に保存する。
    
- レポートに、PSI が更新しないフィールドは含めない。
    
- レポートに、データが古くなっている可能性があるという注意を記す。
    
レポート テーブルとキューブには、プロジェクト データの一部が更新されていないことを検出できるフラグがあります。MSP_EpmProject テーブルと MSP_EpmProject_UserView のレポート データには次のフィールドがあります。 
  
-  _ProjectWbsIsStale_&ndash;作業分割構造 (タスクのアウトラインの階層) が古いかどうかを示します。 
    
-  _ProjectEarnedValueIsStale_&ndash;達成額フィールドは、古くなったことを示します。 
    
-  _ProjectRollupsAreStale_&ndash;サブプロジェクトが下書きデータベースで更新されますが、マスター プロジェクトが更新されていないことを示します。 サブプロジェクトのロールアップ値は、古いです。 
    
-  _ProjectHierarchyNotSynchronized_&ndash;マスター プロジェクトはその子とは同期されません。 これは、子プロジェクトがマスター プロジェクトの発行の一部としてではなく、明示的に発行された場合に発生します。 
    
-  _ProjectCalculationsAreStale_&ndash; Project Professional のスケジュールを計算することがなく、プロジェクトを保存する **(つまり、計算モードが手動**] に設定 [**プロジェクト オプション**] ダイアログ ボックスで [**スケジュール**] タブ)。 
    
-  _ProjectGhostTaskAreStale_&ndash;と同様に_ProjectHierarchyNotSynchronized_プロジェクト間のリンクのデータでは警告が表示されます。 マスター プロジェクトが存在しないが、プロジェクトでのリンクの一方の側が反対側よりも新しいことは。
    
## <a name="about-accessing-the-project-server-database"></a>Project Server データベースへのアクセスについて
<a name="pj15_Programmability_Databases"> </a>

Project Server データベースにアクセスするための Microsoft SQL Server でアクセス許可がある場合は、レポート テーブルおよびビューを読み取ることができます。 Project Server に必要な権限があればは、OData クエリを使用してレポート テーブルからデータを参照することもできます。 開発者から発行されると、下書きに直接アクセスすることが推奨されます。 または、Project Server データベース内の SQL Server のクエリを使用してテーブルを保存します。 Project Server データベース内のテーブルのいずれかで直接変更を行うと、参照整合性を損傷し、Project Server キュー サービスからデータベースへのアクセスに干渉することができます。
  
> [!IMPORTANT]
> プログラムによってデータベースに直接アクセスしてデータを更新することを能動的に妨げるものは存在しません。Project Professional キャッシュ、発行済みテーブル、およびレポート テーブルはすべてがキャッシュ同期プロトコルに依存しているので、直接データを編集すると同期が混乱する可能性があることに注意が必要です。直接アクセスしてデータを変更することによって、Project Server データベースや Project Professional クライアント側キャッシュが破損した場合、製品サポートは役に立てません。 
  
下書きに直接アクセスするアプリケーションの公開、またはテーブルを保存し、ビューも、サービス パックまたは Project Server 2013 の以降のバージョンで変更できるデータベースのスキーマに依存します。 データベースに直接アクセスするアプリケーションは、組み込みの Project Server セキュリティ、共通のビジネス ロジック、追跡、監査、エラー チェック、レポート、ワークフロー、およびその他の機能も失われます。 多くの場合、Project Server 2013 を更新した後にこのようなアプリケーションを書き換える必要があります。 
  
すべてのこれらの理由から、Project Professional および Project Web App の操作を行いますしない、公開、下書きへの直接呼び出しを行うまたはアーカイブ テーブルです。Project Server との統合により、他のアプリケーションをもする必要があります。
  
ドラフトでは、発行されると、スキーマ アーカイブ テーブルに記載されていないとします。 レポート テーブルを使用するには、レポートの作成を支援して、レポート テーブルおよびビューのスキーマが記載されている Project 2013 SDK ダウンロードにします。 レポート データの OData スキーマ、 [ProjectData - プロジェクトの OData サービスの参照](https://msdn.microsoft.com/library/office/jj163015.aspx)を参照してください。
  
## <a name="see-also"></a>関連項目

- [Project 2013 の開発者向けの新機能](updates-for-developers-in-project-2013.md)    
- [Project Server 2013 のアーキテクチャ](project-server-2013-architecture.md)    
- [PSI のすること、しないこと](what-the-psi-does-and-does-not-do.md)   
- [CSOM のすること、しないこと](what-the-csom-does-and-does-not-do.md)    
- [Project 2013 のクライアント側オブジェクト モデル (CSOM)](client-side-object-model-csom-for-project-2013.md)    
- [Project Server ワークフロー開発の作業開始](getting-started-developing-project-server-workflows.md)    
- [Project 2013 プログラミング リファレンス](project-2013-programming-references.md)    
- [プロジェクト PSI リファレンスの概要](project-psi-reference-overview.md)    
- [SharePoint 用アプリを使用して配置するカスタム アクションを作成します。](https://msdn.microsoft.com/library/office/apps/jj163954%28v=office.15%29.aspx)    
- [Project 2010 での非アクティブなタスクの概要](https://blogs.msdn.com/b/project/archive/2010/06/10/introducing-inactive-tasks-in-project-2010.aspx)    
- [プロジェクトの Server 2010: Web PSI、Project Professional のスケジュール設定](https://blogs.msdn.microsoft.com/brismith/2010/09/10/project-server-2010-scheduling-on-the-web-the-psi-and-project-professional/)

