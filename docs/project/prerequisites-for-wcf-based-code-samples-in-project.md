---
title: プロジェクト内のWCFベースコードサンプルの前提条件
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 60d2afc8-10b6-465d-8ce8-c073da6e5054
description: Project Server Interface (PSI) リファレンス トピックに含まれる WCF ベースのコード サンプルを使用して、Visual Studio でプロジェクトを作成するのに役立つ情報について説明します。
ms.openlocfilehash: e41b16f653776d57de4961f591782ef27bce5b9d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619247"
---
# <a name="prerequisites-for-wcf-based-code-samples-in-project"></a>プロジェクト内のWCFベースコードサンプルの前提条件

Project Server Interface (PSI) リファレンス トピックに含まれる WCF ベースのコード サンプルを使用して、Visual Studio でプロジェクトを作成するのに役立つ情報について説明します。
   
[Project Server 2013](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx)クラス ライブラリおよび Web サービスリファレンスに含まれる WCF ベースのコード サンプルの多くは、もともと Project 2010 開発者向けドキュメント用に作成され、WCF Web サービスの標準形式を使用しています。 サンプルは引き続き Project Server 2013 で動作し、コンソール アプリケーションにコピーされ、完全なユニットとして実行するように設計されています。 例外はサンプルに記載されています。 
  
Project Server 2007 用に開発されたサンプルから変更されていない Project 201 Office Project 3 開発者向けドキュメントのコード サンプルは、ASMX Web サービスを使用します。 この ASMX ベースのサンプルは、WCF サービスを使用するように調整することもできます。 この記事では、このサンプルを WCF サービスで使用する方法を説明します。 ASMX Web サービスでサンプルを使用する方法については[、「AsMX](prerequisites-for-asmx-based-code-samples-in-project.md)ベースのコード サンプルの前提条件」を参照Project。
  
> [!NOTE]
> クライアント側オブジェクト モデル (CSOM) にアプリケーションで必要なメソッドが含まれる場合は、CSOM を使用して新しいアプリケーションを開発する必要があります。 CSOM を使用すると、アプリケーションはサーバーサーバー 2013 のProject Onlineまたはオンプレミスインストールで動作Projectできます。 それ以外の場合、アプリケーションで PSI を使用する場合は、ネットワーク通信に推奨されるテクノロジである WCF インターフェイスを使用する必要があります。 ASMX インターフェイスまたは WCF インターフェイスを使用するアプリケーションは、サーバー 2013 のオンプレミス インストールProjectできます。 
>
> CSOM の詳細については[、「Project Server 2013](project-server-2013-architecture.md)アーキテクチャとクライアント側オブジェクト モデル[(CSOM) for Project 2013」を参照](client-side-object-model-csom-for-project-2013.md)してください。 
  
コード サンプルを実行する前に、開発環境のセットアップ、アプリケーションの構成、サービス構成ファイルの追加 (またはプログラムによる WCF サービスの構成)、および環境に合わせた一般的な定数値の変更を行う必要があります。
  
## <a name="setting-up-the-development-environment"></a>開発環境を設定する
<a name="pj15_PrerequisitesWCF_Setup"> </a>

1. **テスト用の Project Server システムをセットアップする。**
    
    開発やテストを行う際には常にテスト Project Server システムを使用します。たとえコードが完全に動作しても、プロジェクト間の依存関係、レポート、またはその他の環境要因が意図しない結果を引き起こす可能性があります。 
    
    > [!NOTE]
    > サーバーの有効なユーザーであり、アプリケーションで使用する PSI 呼び出しのための十分な権限を持っていることを確認します。 それぞれの PSI メソッドに関する開発者向けドキュメントのトピックには、Project Server 権限の表があります。 たとえば、次の [Project。QueueCreateProject メソッド](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx)には、**グローバルな NewProject** アクセス許可と **SaveProjectTemplate アクセス許可が必要** です。 
  
    場合によっては、サーバーでのリモート デバッグが必要になることがあります。 SharePoint ファームの各 Project Server コンピューターにイベント ハンドラー アセンブリをインストールし、SharePoint サーバーの全体管理の全般アプリケーション 設定 の Project Server 設定 ページを使用して Project Web App インスタンスのイベント ハンドラーを構成することで、イベント ハンドラーをセットアップする必要があります。
    
2. **開発用コンピューターをセットアップする。**
    
    通常、PSI にはネットワーク経由でアクセスします。コード サンプルは、記載されている場合を除き、サーバーから分離されたクライアントで動作するように作られています。
    
    1. **適切なバージョンの Visual Studio をインストールする。** 記載されている場合を除き、コード サンプルは Visual C# で記述されています。 これらは、2010 年Visual Studio 2012 年Visual Studioできます。 最新のサービス パックがインストールされていることを確認してください。 
    
    2. **Project Server の DLL を開発用コンピューターにコピーする。** サーバー コンピューター上の次の `[Program Files]\Microsoft Office Servers\15.0\Bin` アセンブリProject開発用コンピューターにコピーします。 
    
       - Microsoft.Office.Project.Server.Events.Receivers.dll
    
       - Microsoft.Office.Project.Server.Library.dll
    
    3. PSI で WCF サービスの ProjectServerServices.dll プロキシ アセンブリをコンパイルして使用する方法に関する情報については、「[Intellisense の説明を備えた PSI プロキシ アセンブリを使用する](#pj15_PrerequisitesWCF_BuildingProxy)」を参照してください。
    
3. **IntelliSense ファイルをインストールする。**
    
    Project Server アセンブリのクラスとメンバーに IntelliSense の説明を使用するには、Project 2013 SDK のダウンロードから更新された IntelliSense XML ファイルを、Project Server アセンブリがある同じディレクトリにコピーします。 たとえば、アプリケーションで Microsoft.Office.Project.Server.Library.dll アセンブリへの参照を設定するディレクトリに、Microsoft.Office.Project.Server.Library.xml ファイルをコピーします。
    
    IntelliSense PSI サービスの説明では、Project SDK ダウンロードのサブディレクトリで CompileWCFProxyAssembly.cmd スクリプトを使用して PSI プロキシ アセンブリを作成する必要があります。 `Documentation\IntelliSense\WCF` このスクリプトを実行すると、WCF ベースの ProjectServerServices.dll プロキシ アセンブリが作成されます。 詳細については、SDK ダウンロードに含まれる [ReadMe_IntelliSense].mht ファイルを参照してください。 
    
## <a name="creating-the-application-and-adding-a-service-reference"></a>アプリケーションを作成してサービス参照を追加する
<a name="pj15_PrerequisitesWCF_Configure"> </a>

1. **コンソール アプリケーションを作成する。**
    
    コンソール アプリケーションを作成するには、[**新しいプロジェクト**] ダイアログ ボックスのドロップダウン リストから [**.NET Framework 4**] を選択します。この新しいアプリケーションに PSI サンプル コードをコピーできます。
    
2. **WCF に必要な参照を追加する。**
    
    ソリューション エクスプローラーで、**System.ServiceModel** への参照を追加します (図 1 を参照)。 Web アプリケーションの場合は、**System.ServiceModel.Web** を使用します。
    
    **System.Runtime.Serialization** への参照も追加します。
    
    **図 1. Visual Studio での WCF ベースのアプリケーションへの参照の追加**

    ![WCF への参照の追加](media/pj15_PrerequisitesWCF_AddReference.gif "WCF への参照の追加")
  
3. **コードをコピーする。**
    
    コード サンプル全体をコンソール アプリケーションの Program.cs ファイルにコピーします。
    
4. **サンプル アプリケーションの名前空間を設定する。**
    
    サンプルの上部に記されている名前空間をアプリケーションの既定の名前空間に変更するか、アプリケーションの既定の名前空間をサンプルに合わせて変更することができます。アプリケーションの既定の名前空間は、アプリケーションのプロパティを変更することによって変更できます。 
    
    たとえば [、ReadResource](https://msdn.microsoft.com/library/WebSvcResource.Resource.ReadResource.aspx)のコード サンプルには **、Microsoft.SDK.Project という名前空間があります。Samples.CreateResourceTest**. Visual Studio プロジェクトの名前が **ResourceTest** である場合、Program.cs ファイルから名前空間をコピーし、プロジェクトの [**プロパティ**] ウィンドウを開きます ([**プロジェクト**] メニューで [**ResourceTest のプロパティ**] をクリック)。 [**アプリケーション**] タブで、その名前空間を [**既定の名前空間**] テキスト ボックスにコピーします。 
    
5. **サービス参照を設定する。**
    
    多くの例では、1 つ以上の PSI サービスへの参照が必要です。これらは、サンプル自体、またはサンプルの前にあるコメントに示されています。サービス参照の適切な名前空間を取得するには、最初にアプリケーションの既定の名前空間を設定する必要があります。
    
    WCF サービス参照を追加する方法として次の 3 つがあります。
    
    - ProjectServerServices.dll という名前の PSI プロキシ アセンブリを作成してから、このアセンブリへの参照を設定します。詳細については「[Intellisense の説明を備えた PSI プロキシ アセンブリを使用する](#pj15_PrerequisitesWCF_BuildingProxy)」を参照してください。
    
    - svcutil.exe 出力からのプロキシ ファイルを Visual Studio ソリューションに追加します。「[PSI プロキシ ファイルを追加する](#pj15_PrerequisitesWCF_AddingProxyFile)」を参照してください。
    
    - Visual Studio を使用してサービス参照を追加します。「[サービス参照を追加する](#pj15_PrerequisitesWCF_AddingServiceReference)」を参照してください。
    
### <a name="using-a-psi-proxy-assembly-and-intellisense-descriptions"></a>Intellisense の説明を備えた PSI プロキシ アセンブリを使用する
<a name="pj15_PrerequisitesWCF_BuildingProxy"> </a>

PSI のすべてのパブリック WCF サービスには、プロキシ アセンブリを使用できます。 2013 ProjectServerServices.dll Project SDK ダウンロードのスクリプトを使用して、ProjectServerServices.dll プロキシ アセンブリをコンパイルし、プロキシ アセンブリを開発用コンピューター `Documentation\IntelliSense\WCF\CompileWCFProxyAssembly.cmd` にコピーします。 同じ場所に、Intellisense に関する ProjectServerServices.xml ファイルをコピーします。 Visual Studio で、この ProjectServerServices.dll プロキシ アセンブリへの参照を設定します。 
  
Project Server のサービス パックおよび更新プログラムの場合は、同じ SDK ダウンロード フォルダーにある GenWCFProxyAssembly.cmd スクリプトを使用し、プロキシのソース ファイルを更新して新しいプロキシ アセンブリを作成できます。 SDK のダウンロードへのリンクについては[、2013 Projectドキュメントを参照してください](project-2013-developer-documentation.md)。 詳細については、「[サービス参照を追加する](#pj15_PrerequisitesWCF_AddingServiceReference)」を参照してください。 
  
> [!NOTE]
> Source.zip ファイルからプロキシ ソース ファイルを抽出すると、フォルダー内のファイルは、2013 SDK ダウンロードの発行日Project `Documentation\IntelliSense\WCF\Source` です。 更新された PSI プロキシ ソース ファイルを生成するには、Project Server コンピューターで GenASMXProxyAssembly.cmd スクリプトを実行します。 詳細については、「[サービス参照を追加する](#pj15_PrerequisitesWCF_AddingServiceReference)」を参照してください。 
> 
> フォルダー内のスクリプト  `Documentation\IntelliSense\ASMX` は、WCF ベースのアプリケーションでは機能しません。 GenASMXProxyAssembly.cmd スクリプトは Wsdl.exeを呼び出し、ASMX サービスのソース コード ファイルを生成します。 ASMX プロキシ ファイルには、さまざまなクラスとプロパティが含まれます。 たとえば、ASMX ベースの Resource Web サービスには Resource クラスが含まれますが、WCF ベースの Resource サービスには Resource インターフェイス **、ResourceChannel** インターフェイス **、ResourceClient** クラスが含まれます。 
  
ASMX Web サービスと WCF サービスのために作成された恣意的な名前空間はどちらも同じなので、Intellisense 用の ProjectServerServices.xml ファイルはどちらのアセンブリでも動作します。たとえば、WCF ベースのプロキシ アセンブリでも ASMX ベースのプロキシ アセンブリでも、Resource サービスの名前空間は **SvcResource** です。もちろん、この名前空間の名前は変更できます。ただし、その名前はプロキシ アセンブリと ProjectServerServices.xml Intellisense ファイルで一致する必要があります。
  
あるコード サンプルが PSI サービスの名前空間に別の名前 (**ProjectWebSvc** など) を使用している場合、IntelliSense が動作するためには、**SvcProject** を使用するようにそのサンプルを変更して、名前空間とプロキシ アセンブリを一致させる必要があります。 
  
WCF ベースのプロキシ アセンブリを使用する利点は、次のとおりです。
  
- ほとんどのソリューションを、Project Server コンピューターとは別のコンピューター上にあるプロキシ アセンブリで開発できます。ただし、個々のサービス参照の設定には、Project Server コンピューターでの開発が必要です。
    
- このプロキシ アセンブリにはすべての PSI サービス名前空間が含まれるので、複数のプロキシ ファイルを追加する必要がありません。
    
- ProjectServerServices.xml ファイルを ProjectServerServices.dll プロキシ アセンブリへの参照を設定するのと同じディレクトリに追加すれば、PSI クラスおよびメンバーに関する Intellisense 記述を取得できます。 詳細については、2013 SDK ダウンロードのフォルダーにある [ReadMe_IntelliSense] ファイルProject `Documentation\IntelliSense` 参照してください。 
    
**図 2. Resource サービスのメソッドに対する IntelliSense の使用**

![ReadResource メソッドへの Intellisense の使用](media/pj15_PrerequisitesWCF_Intellisense.gif "ReadResource メソッドへの Intellisense の使用")
  
このプロキシ アセンブリを使用する場合の欠点は、ソリューションが大規模になることと、ソリューションと共にプロキシ アセンブリの配布とインストールが必要になることです。また、プロキシ アセンブリと Intellisense ファイルの中で同じ名前空間を使用する必要があります (ただし、スクリプトを修正して、独自のプロキシ アセンブリを作成し、別々の名前空間を使用するように ProjectServerServices.xml Intellisense ファイルを変更した場合は例外です)。
  
### <a name="adding-a-psi-proxy-file"></a>PSI プロキシ ファイルを追加する
<a name="pj15_PrerequisitesWCF_AddingProxyFile"> </a>

2013 Project SDK のダウンロードには、プロキシ アセンブリの SvcUtil.exeコマンドによって生成されるソース ファイルが含まれています。 ソース ファイルは、サブディレクトリSource.zipファイル  `Documentation\IntelliSense\WCF` に含めます。 プロキシ アセンブリへの参照を設定する代わりに、1 つ以上のソース ファイルを別のソリューションにVisual Studioできます。 たとえば、Project サービスとリソース サービスを使用するには、wcf を追加します。Project.cs と wcf。ソリューションへの Resource.cs ファイル。 
  
WCF では、それぞれの PSI サービスの主要なクラスが、インターフェイスによって定義され、そのメンバーにアクセスするためのクライアント クラス内で実装されます。たとえば、**SvcProject.Resource** インターフェイスは **SvcProject.ResourceClient** クラス内で実装されています。**ResourceClient** オブジェクトを、たとえば **resourceClient** という名前のクラス変数として定義するには、以下のコードを使用します。この例では、**SetClientEndpoints** メソッドによって、**basicHttp_Project** エンドポイントを使用する **resourceClient** オブジェクトが作成されます。このエンドポイントは app.config ファイルで定義されています。app.config ファイルの詳細については、「[サービス構成ファイルを追加する](#pj15_PrerequisitesWCF_AddConfig)」セクションを参照してください。 
  
```cs
private static SvcResource.ResourceClient resourceClient;
. . .
private static void SetClientEndpoints()
{
  resourceClient = new SvcResource.ResourceClient("basicHttp_Resource");
  . . .
}
public void DisposeClients()
{
  resourceClient.Close();
  . . .
}
```

> [!NOTE]
> PSI プロキシ アセンブリを使用する場合も、プロキシ ファイルを追加して **SvcResource** という名前の Project サービス参照を追加する場合も、**resourceClient** オブジェクトの作成と廃棄には同じコードが使用されます。 
  
### <a name="adding-a-service-reference"></a>サービス参照の追加
<a name="pj15_PrerequisitesWCF_AddingServiceReference"> </a>

WCF ベースのプロキシ アセンブリを使用したり、PSI サービスのプロキシ ファイルを追加したりしない場合は、1 つ以上のサービス参照を Visual Studio 内で直接設定できます。 次の手順の手順 1 を使用して、更新されたプロキシ ファイルを作成し、Project SDK のダウンロードに含まれるスクリプト `Documentation\IntelliSense\WCF\GenWCFProxyAssembly.cmd` を準備することもできます。 
  
> [!NOTE]
> サービス参照を設定するには、Project Server コンピューターで Visual Studio を使用する必要があります。Visual Studio 内でサービス参照を直接追加するよりも、ProjectServerServices.dll プロキシ アセンブリを使用するか、プロキシ ソース ファイルを追加することをお勧めします。 
  
次の手順は、サーバーのテスト インストールを実行しているコンピューターで Visual Studio 2012 を使用してサービス参照を設定するProjectします。
  
1. バックエンド WCF サービスへのアクセスを取得するには、Project Server コンピューターで Visual Studio を実行します。
    
2. **ソリューション エクスプローラー** で、[**参照設定**] フォルダーを右クリックし、[**サービス参照の追加**] をクリックします。 
    
3. [サービス **参照の追加]** ダイアログ ボックスの [アドレス] テキスト ボックスに https://localhost:32843/ _「GUID_/psi/ _ServiceName_.svc」と入力し、Enter キーを **押します**。 GUID _を_ 534c37eb00d74ccfadcecf9827e95239 などの Project Server サービス アプリケーションの仮想ディレクトリ名に置き換える。 _ServiceName を Resource_ などのサービスの名前に置き換えてください (図 3 を参照)。 
    
   Project Server Service 仮想ディレクトリの名前は、以下のどちらかの方法で取得できます。
    
   - ブラウザーで SharePoint 2013 サーバーの全体管理アプリケーションを開きます。 [**サービス アプリケーションの管理**] をクリックし、目的の Project Server PSI Service アプリケーションをクリックします。 たとえば、[**ProjectServerService**] をクリックします。 [サイトの管理] ページProject Web Appには、仮想ディレクトリ名が含まれます。 たとえば、仮想ディレクトリ名は次のようになります  `https://ServerName:8080/_admin/pwa/managepwa.aspx?appid=534c37eb-00d7-4ccf-adce-cf9827e95239`  `534c37eb00d74ccfadcecf9827e95239` (ディレクトリ名にはダッシュはありません)。 
    
   - Project Server コンピューターで [**インターネット インフォメーション サービス (IIS) マネージャー**] ダイアログ ボックスを開きます。[**接続**] ウィンドウの [**SharePoint Web サービス**] ノードを展開し、PSI フォルダーを含むディレクトリが見つかるまで、その下位にあるサービス仮想ディレクトリを展開していきます。見つかったディレクトリを選択し、[**操作**] ウィンドウの [**詳細設定**] をクリックして、そのディレクトリ名を [**仮想パス**] フィールドにコピーします。 
    
      > [!NOTE]
      > 複数の Project Server Service 仮想ディレクトリが存在することがあります。 必要なインスタンスを含む仮想ディレクトリをProject Web Appしてください。 
  
   - **get-SPServiceApplication** コマンドレットは、Windows PowerShell 2013 と共にインストールされているSharePoint使用します。 タスク バーの [**スタート**] ボタンをクリックし、[**すべてのプログラム**]、[**Microsoft SharePoint 2013 製品**]、[**SharePoint 2013 管理シェル**] の順にクリックします。 以下は、[**SharePoint 2013get- 管理シェル**] ウィンドウで定義済みサービス アプリケーション (GUID は異なります) に対してコマンドを実行した結果です。 Project Server サービス アプリケーションの GUID をコピーします。 
    
        ```powershell
            PS > get-SPServiceApplication
            DisplayName          TypeName             Id
            -----------          --------             --
            State Service        State Service        04041cfa-4ab3-4473-8bc8-3967b02eff39
            ProjectServerSer...  Project Server PS... 534c37eb-00d7-4ccf-adce-cf9827e95239
            Security Token Se... Security Token Se... 7243732e-edea-405d-8cc8-1716b99faef5
            Application Disco... Application Disco... 3bfbdeb0-bc20-4a21-801c-cc6f1ce6c643
            SharePoint Server... SharePoint Server... 09912f49-3b72-462f-a44c-6533b578286a  
        ```

      Project Server Service アプリケーションの完全な名前がわかる場合は、その名前に基づいて GUID 値を取得できます。次に例を示します。
    
        ```powershell
        PS > $projectService = "ProjectServerService"
        PS > (get-SPServiceApplication -Name $projectService).Id
        Guid
        ----
        534c37eb-00d7-4ccf-adce-cf9827e95239
       ```

      > [!NOTE]
      > GUID からダッシュを削除すると仮想ディレクトリ名になります。 
  
   サーバー サービスの標準のような URL `https://localhost:32843/534c37eb00d74ccfadcecf9827e95239/PSI/Resource.svc` Projectです。 
    
4. サービス参照の解決後、[**名前空間**] テキスト ボックスに参照名を入力します。 2013 年 2013 Projectのコード例では、任意の名前空間名 **Svc _ServiceName を使用します_**。 たとえば、このコード サンプルの Resource サービスは **SvcResource** という名前になっています。
    
    **図 3. WCF ベースの Resource サービス参照の追加**

    ![WCF ベースの Resource サービス参照の追加](media/pj15_PrerequisitesWCF_AddSvcReference.gif "WCF ベースの Resource サービス参照の追加")
  
5. web.config Service ディレクトリProject一時ファイルを元のファイルに置き換え (web.config に変更)、再実行します `iisreset` 。
    
## <a name="setting-other-references"></a>その他の参照を設定する
<a name="pj15_PrerequisitesWCF_OtherReferences"> </a>

Projectサーバー アプリケーションは、多くの場合、2013 Web サービスなどのSharePointサービスを使用します。 ほかのサービスや参照が必要な場合は、コード サンプルにそれらが記されています。
  
コード サンプルのローカル参照は、サンプルの上部の **using** ステートメントに示されています。 
  
1. **ソリューション エクスプローラー** で、[**参照設定**] フォルダーを右クリックし、[**参照の追加**] をクリックします。
    
2. [**参照**] をクリックして、以前にコピーした Project Server の DLL を格納した場所を参照します。必要な DLL を選択し、[**OK**] をクリックします。
    
> [!NOTE]
> 開発用コンピューター上のアセンブリのバージョンがターゲット Project Server コンピューターのものと厳密に一致していることを確認します。 
  
## <a name="adding-a-service-configuration-file"></a>サービス構成ファイルを追加する
<a name="pj15_PrerequisitesWCF_AddConfig"> </a>

アプリケーションがプログラムによって WCF サービスを構成する場合、サービス構成ファイルは使用されません。それ以外の場合、Windows アプリケーションまたはコンソール アプリケーションでは app.config ファイルの **system.serviceModel** 要素を使用し、Web アプリケーションでは web.config ファイルの **system.serviceModel** をインクルードします。app.config ファイルの使用方法や、WCF サービスをプログラムで構成する方法については、「[[ウォークスルー] WCF を使用して PSI アプリケーションを開発する](https://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx)」を参照してください。
  
サービス プロキシ ソース ファイルを生成すると、SvcUtil.exe コマンドは、app.config ファイルまたは web.config ファイルの既定 **の system.serviceModel** 要素の基礎となる output.config ファイルも作成します。 2013 Project SDK のダウンロードには、2013 SDK のサンプル output.configが含まれています `Documentation\IntelliSense\WCF\Source.zip` 。 たとえば、Resource サービスoutput.config作成SvcUtil.exe既定のファイルには、BasicHttpBinding_Resource と BasicHttpBinding_Resource1 という名前の 2 つの **バインドが含BasicHttpBinding_Resource1。** クライアント **要素には** 、2 つの既定のエンドポイントが含まれています。 1 つのエンドポイントは、ポート 32843 の HTTP アドレスへのセキュリティで保護されたアクセス用であり、もう 1 つはポート 32843 での通常のアクセス用です。次に示します。 
  
```XML
<client>
    <endpoint address="https://ServerName.domain:32843/GUID/PSI/Resource.svc/secure"
        binding="basicHttpBinding" bindingConfiguration="BasicHttpBinding_Resource"
        contract="SvcResource.Resource" name="BasicHttpBinding_Resource" />
address="https://ServerName.domain:32843/GUID/PSI/Resource.svc"
        binding="basicHttpBinding" bindingConfiguration="BasicHttpBinding_Resource1"
        contract="SvcResource.Resource" name="BasicHttpBinding_Resource1" />
</client>
```

PSI サービス構成では、既定のバインドやエンドポイントを使用しません。Project Server では、バックエンド サービスの呼び出しでルーターとして動作するフロントエンド ProjectServer.svc を介してアプリケーションが PSI サービスにアクセスする必要があります。app.config ファイルを作成するには、以下の手順を実行します。
  
1. ProjectServerServices.dll プロキシ アセンブリへの参照を設定したり、あるサービス用のプロキシ ソース ファイルを追加したりする場合、アプリケーションには app.config ファイルが含まれません。 その場合は、新しいアイテムを Visual Studio に追加します。 [新しい **アイテムの追加]** ダイアログ ボックスで、[ **アプリケーション** 構成ファイル] テンプレートを選択し、そのテンプレートに名前を付app.config、[追加] を **選択します**。
    
2. app.config ファイルのすべてのテキストを削除し、以下のコードをこのファイルにコピーします。 サービス エンドポイントごとに同じバインド (たとえば  `basicHttpConf` ) を使用できます。 複数のバインドを使用する場合 (たとえば、HTTP と HTTPS の両プロトコルをバインドする場合) は、プロトコルごとにバインドを作成する必要があります。
    
    ```XML
        <?xml version="1.0" encoding="utf-8" ?>
        <configuration>
            <system.serviceModel>
                <behaviors>
                    <endpointBehaviors>
                        <behavior name="basicHttpBehavior">
                            <clientCredentials>
                                <windows allowedImpersonationLevel="Impersonation" />
                            </clientCredentials>
                        </behavior>
                    </endpointBehaviors>
                </behaviors>
                <bindings>
                    <basicHttpBinding>
                        <binding name="basicHttpConf" sendTimeout="01:00:00" 
                            maxBufferSize="500000000" maxReceivedMessageSize="500000000">
                            <readerQuotas maxDepth="32" maxStringContentLength="8192" 
                                maxArrayLength="16384" maxBytesPerRead="4096" 
                                maxNameTableCharCount="500000000" />
                            <security mode="TransportCredentialOnly">
                                <transport clientCredentialType="Ntlm" realm="https://SecurityDomain" />
                            </security>
                        </binding>
                    </basicHttpBinding>
                </bindings>
                <client>
                    <endpoint address="https://ServerName/ProjectServerName/_vti_bin/PSI/ProjectServer.svc"
                        behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
                        bindingConfiguration="basicHttpConf" 
                        contract="SvcServiceName.ServiceName"
                        name="basicHttp_ServiceName" />
                </client>
            </system.serviceModel>
        </configuration>
    ```

3. クライアント `ServerName/ProjectServerName` エンドポイント のアドレスを、サーバーとインスタンスの名前に置きProject Web Appします。 
    
4. リソース  `ServiceName` などの PSI サービスの名前に置き換える。 たとえば、次のようにサービス名の 3 つのインスタンスすべてを確実に置き換えてください。
    
    ```XML
        <endpoint address="https://myserver/pwa/_vti_bin/PSI/ProjectServer.svc"
            behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
            bindingConfiguration="basicHttpConf" 
            contract="SvcResource.Resource"
            name="basicHttp_Resource" />
    ```

5. 複数の PSI サービスを使用するには、サービスごとに、またサービスが使用する **binding** ごとに、1 つの **endpoint** 要素を作成します。たとえば、以下のエンドポイントでは、Project サービスと QueueSystem サービスで基本的な HTTP バインドを使用するようにクライアントを構成しています。 
    
    > [!NOTE]
    > アプリケーションの実行時に、サーバーがビジー状態である、または HTTP 要求が許可されていないことを示すエラーが表示される場合は、app.config ファイルのエンドポイント アドレスが正しいことを確認してください。 
  
    ```XML
        <client>
        <endpoint address="https://ServerName/pwa/_vti_bin/PSI/ProjectServer.svc"
            behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
            bindingConfiguration="basicHttpConf" 
            contract="SvcProject.Project"
            name="basicHttp_Project" />
        <endpoint address="https://ServerName/pwa/_vti_bin/PSI/ProjectServer.svc"
            behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
            bindingConfiguration="basicHttpConf" 
            contract="SvcQueueSystem.QueueSystem"
            name="basicHttp_QueueSystem" />
        </client>
    ```

Visual Studio の **WCF サービス構成エディター** ([**ツール**] メニューにあります) を使用すると、app.config ファイルを編集できます。 図 4 は、[**Microsoft サービス構成エディター**] ダイアログ ボックスで **contract** 要素を設定する方法を示します。 ソリューションで PSI プロキシ アセンブリを使用している場合は、ProjectServerServices.dllソリューションのディレクトリでVisual Studio `bin\debug` します。 [**コントラクト型ブラウザー**] ダイアログ ボックスに、WCF サービス コントラクトのすべてが表示されます (図 5 を参照)。 
  
**図 4. WCF サービス構成エディターの使用**

![WCF サービス構成エディターの使用](media/pj15_PrerequisitesWCF_ServiceConfigurationEditor.gif "WCF サービス構成エディターの使用")
  
ソリューションで wcfResource.cs などのサービス プロキシ ファイルを使用している場合は、アプリケーションをコンパイルし、ディレクトリで実行可能ファイルを開  `bin\debug` きます。 app.config ファイルの編集の詳細については、「[[ウォークスルー] WCF を使用して PSI アプリケーションを開発する](https://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx)」を参照してください。
  
**図 5. WCF サービス構成エディターでのコントラクト型ブラウザーの使用**

![コントラクト型ブラウザーの使用](media/pj15_PrerequisitesWCF_ContractTypeBrowser.gif "コントラクト型ブラウザーの使用")
  
## <a name="using-multiple-authentication"></a>複数の認証を使用する
<a name="pj15_PrerequisitesWCF_ClaimsMultiAuth"> </a>

サーバーユーザーによるオンプレミスProject認証は、Windows認証またはフォーム認証の場合も、SharePoint でクレーム処理を行います。 複数認証とは、プロビジョニングされている Web アプリケーションがProject Web App認証とフォーム ベース認証Windows両方をサポートします。 この場合、Windows 認証を使用する WCF サービスへの呼び出しは、クレーム プロセスで認証するユーザーの種類を決定できないので、次のエラーで失敗します。
  
`The server was unable to process the request due to an internal error. For more information about the error, either turn on Include ExceptionDetailInFaults (either from ServiceBehaviorAttribute or from the <serviceDebug> configuration behavior) on the server in order to send the exception information back to the client, or turn on tracing as per the Microsoft .NET Framework 3.0 SDK documentation and inspect the server trace logs.`

WCF のこの問題を修正するには、PSI メソッドのすべての呼び出しをそれぞれの PSI サービスに対して定義される **OperationContextScope** 内に置く必要があります。ただし、複数のサービスに対するスコープを入れ子にしないでください。たとえば、Resource サービスと Project サービスを使用する際には、それぞれの呼び出しセットを各自のスコープ内に置く必要があります。 
  
以下の例では、アプリケーションのどの **OperationContextScope** セクションからでも **DisableFormsAuth** メソッドを呼び出せます。 このメソッドは、以前にフォーム認証を無効にしたヘッダー値を削除し  _、isWindowsAuth_ パラメーターが false の場合にフォーム認証を続行 **できます**。 _isWindowsAuth が_ true **の場合****、DisableFormsAuth** メソッドはフォーム認証を無効にします。 
  
**WcfSample** メソッド内の **projectClient** オブジェクトは、PSI の **SvcProject.ProjectClient** クラスのインスタンスです。 
  
```cs
// Class variable that determines whether to disable Forms authentication.
private bool isWindowsUser = true;
public void DisableFormsAuth(bool isWindowsAuth)
{
    WebOperationContext.Current.OutgoingRequest.Headers.Remove(
        "X-FORMS_BASED_AUTH_ACCEPTED");
    if (isWindowsAuth)
    {
        // Disable Forms authentication, to enable Windows authentication.
        WebOperationContext.Current.OutgoingRequest.Headers.Add(
            "X-FORMS_BASED_AUTH_ACCEPTED", "f");
    }
}
private void WcfSample()
{
    // Limit the scope of WCF calls to the client channel. 
    using (OperationContextScope scope = new OperationContextScope(projectClient.InnerChannel))
    {
        // Add a web request header to enable Windows authentication in 
        // multiple authentication installations.
        DisableFormsAuth(isWindowsUser);
        // Add calls to the projectClient methods here:
        // . . .
    }
}
```

> [!NOTE]
> **OperationContextScope** 内での PSI 呼び出しが必要になるのは、複数認証の環境で動作するアプリケーションのみです。Project Server で Windows 認証のみを使用する場合、スコープの設定や、フォーム認証を無効にする Web 要求ヘッダーの追加は不要です。 
> 
> ASMX ベースのアプリケーションの場合は、修正方法が異なります。 詳細については、「AsMXベースのコード サンプルの前提条件」の「複数認証の使用」[セクション](prerequisites-for-asmx-based-code-samples-in-project.md)を参照Project。 
  
## <a name="changing-values-of-generic-constants"></a>一般的な定数の値を変更する
<a name="pj15_PrerequisitesWCF_ChangeValues"> </a>

大部分のサンプルには、サンプルが環境で正しく動作するために更新する必要がある 1 つ以上の変数があります。 次の例では、SSL がインストールされている場合に HTTP プロトコルではなく HTTPS プロトコルを使用します。 _ServerName を_ 使用しているサーバーの名前に置き換える。 _ProjectServerName を_、プロジェクト サーバー サイトの仮想ディレクトリ名 (ディレクトリ名など) に置き換PWA。 
  
```cs
const string PROJECT_SERVER_URI = "https://ServerName/ProjectServerName/";
```

ほかに変更が必要な変数があれば、コード サンプルの上部に記載されています。
  
## <a name="verifying-the-results"></a>結果を確認する
<a name="pj15_PrerequisitesWCF_Verify"> </a>

コード サンプルの結果の取得と解釈は、必ずしも簡単ではありません。 たとえば、プロジェクトを作成する場合は、プロジェクトがプロジェクトの [センター] ページに表示される前にProject発行するProject Web App。
  
コード サンプルの結果は、いくつかの方法で確認できます。たとえば、次のような方法があります。
  
- 2013 Project Professional 2013 クライアントを使用して、Project サーバー コンピューターからプロジェクトを開き、必要なアイテムを表示します。
    
- 発行済みプロジェクトは、Project ( ) の [センター] ページProject Web App表示 `https://ServerName/ProjectServerName/projects.aspx` します。
    
- [キュー ログ] を表示Project Web App。 [サーバーの設定] ページを開き (右上隅にある **[設定]** アイコンを選択し、[個人用のジョブ] セクション ( ) の [マイ キューに入っているジョブ]**を設定** します `https://ServerName/ProjectServerName/MyJobs.aspx` 。 [**表示**] ドロップダウン リストでは、ジョブの状態による並べ替えができます。 既定の状態は [**進行中または失敗した過去 1 週間のジョブ**] です。 
    
- すべてのキュー ジョブ設定をProject Web App、エンタープライズ オブジェクトの削除または強制チェックインを行う場合は、() の [サーバー サーバー] `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx` ページを使用します。 [サーバー設定] ページのこれらのリンクにアクセスするには、管理権限が必要です。
    
- **Microsoft SQL Server Management Studio** を使用して、Project Server データベースのテーブルにクエリを実行します。たとえば、以下のクエリを使用して、MSP_WORKFLOW_STAGE_PDPS テーブルの先頭 200 行を選択し、ワークフロー ステージのプロジェクト詳細ページ (PDP) に関する情報を表示します。 
    
```sql
        SELECT TOP 200 [STAGE_UID]
                ,[PDP_UID]
                ,[PDP_NAME]
                ,[PDP_POSITION]
                ,[PDP_ID]
                ,[PDP_STAGE_DESCRIPTION]
                ,[PDP_REQUIRES_ATTENTION]
        FROM [ProjectService].[pub].[MSP_WORKFLOW_STAGE_PDPS]
```

## <a name="cleaning-up"></a>クリーンアップ
<a name="pj15_PrerequisitesWCF_Cleanup"> </a>

いくつかのコード サンプルをテストすると、エンタープライズ オブジェクトおよび設定の削除や再設定が必要になります。 エンタープライズ データ () を管理設定サーバー Project Web Appページを使用できます `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx` 。 [サーバー設定] ページにあるリンクを使用して、古いアイテムを削除したり、チェックインを強制したり、すべてのユーザーのジョブ キューを管理したり、その他の管理タスクを実行したりできます。
  
以下に、コード サンプル実行後の一般的なクリーンアップ作業で使用する、[サーバー設定] ページ上のリンクの一部を示します。
  
- **エンタープライズ ユーザー設定フィールドと参照テーブル**
    
- **キュー ジョブの管理**
    
- **エンタープライズ オブジェクトの削除**
    
- **エンタープライズ オブジェクトの強制チェックイン**
    
- **エンタープライズ プロジェクトの種類**
    
- **ワークフロー フェーズ**
    
- **ワークフロー ステージ**
    
- **プロジェクト詳細ページ**
    
- **タイムシート期間**
    
- **タイムシートの設定および既定値**
    
- **管理用行の分類**
    
その他の設定は、SharePoint Server 2013 で特定の Project Web App インスタンスではなく、Project Web App Server 2013 設定 ページによって管理されます。 SharePoint サーバーの全体管理アプリケーションで、[全般アプリケーション **設定]** を選択し **、[Project Server 設定]** の [管理] を選択し、[サーバー 設定] ページのドロップダウン リストで Project Web App インスタンスを選択します。  たとえば、[サーバー側 **イベント ハンドラー] を** 選択して、選択したインスタンスのイベント ハンドラーを追加またはProject Web Appします。 
  
## <a name="see-also"></a>関連項目

- [プロジェクト内のASMXベースコードサンプルの前提条件](prerequisites-for-asmx-based-code-samples-in-project.md)   
- [[ウォークスルー] WCF を使用して PSI アプリケーションを開発する](https://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx)   
- [WCF で偽装を使用する](https://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)  
- [Project PSI 参照の概要](project-psi-reference-overview.md) 
- [SharePoint デベロッパー センター](https://msdn.microsoft.com/sharepoint/default.aspx)
    

