---
title: プロジェクト内の WCF ベースのコード サンプルの前提条件
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 60d2afc8-10b6-465d-8ce8-c073da6e5054
description: プロジェクト Server インターフェイス (PSI) のリファレンス トピックに含まれている WCF ベースのコード サンプルを使用して Visual Studio でプロジェクトを作成するための情報について説明します。
ms.openlocfilehash: 43700a9db4445dacf366c7ca2efe1bfb10914372
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804686"
---
# <a name="prerequisites-for-wcf-based-code-samples-in-project"></a>プロジェクト内の WCF ベースのコード サンプルの前提条件

プロジェクト Server インターフェイス (PSI) のリファレンス トピックに含まれている WCF ベースのコード サンプルを使用して Visual Studio でプロジェクトを作成するための情報について説明します。
   
の[Project Server 2013 のクラス ライブラリと web サービスの参照](http://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx)に含まれている WCF ベースのコード サンプルの多くは、Project 2010 の開発者向けのドキュメント用に作成され、WCF web サービスの標準的な形式を使用します。 まだサンプルは、Project Server 2013 での作業し、コンソール アプリケーションにコピーし、完全な単位として実行するように設計されています。 サンプルで例外が記載されています。 
  
Office Project Server 2007 用に開発されたサンプルから変更されていない、Project 2013 開発者向けのドキュメントでのコード サンプルでは、ASMX Web サービスを使用します。 ASMX ベースのサンプルは、WCF サービスの使用に適合させることができます。 この資料では、WCF サービスを使用してサンプルを使用する方法を示します。 ASMX web サービスのサンプルを使用する方法の詳細については、[プロジェクト内の ASMX ベースのコード サンプルの前提条件](prerequisites-for-asmx-based-code-samples-in-project.md)を参照してください。
  
> [!NOTE]
> クライアント側オブジェクト モデル (CSOM) では、アプリケーションを必要とするメソッドが含まれている場合、CSOM で新しいアプリケーションを開発する必要があります。 CSOM は、プロジェクトのオンラインまたは Project Server 2013 のオンプレミス インストールを操作するアプリケーションを有効にします。 それ以外の場合、アプリケーションは、PSI を使用する場合は、WCF インターフェイスは、ネットワーク通信のことをお勧めする技術であるを使用してください。 ASMX インターフェイスまたは WCF インターフェイスを使用するアプリケーションは、Project Server 2013 のオンプレミスのインストールでのみ操作できます。 
>
> CSOM の詳細については、 [Project Server 2013 のアーキテクチャ](project-server-2013-architecture.md)および[Project 2013 のクライアント側オブジェクト モデル (CSOM)](client-side-object-model-csom-for-project-2013.md)を参照してください。 
  
コード サンプルを実行する前に、開発環境のセットアップ、アプリケーションの構成、サービス構成ファイルの追加 (またはプログラムによる WCF サービスの構成)、および環境に合わせた一般的な定数値の変更を行う必要があります。
  
## <a name="setting-up-the-development-environment"></a>開発環境を設定する
<a name="pj15_PrerequisitesWCF_Setup"> </a>

1. **テスト プロジェクトのサーバー システムを設定します。**
    
    開発やテストを行う際には常にテスト Project Server システムを使用します。たとえコードが完全に動作しても、プロジェクト間の依存関係、レポート、またはその他の環境要因が意図しない結果を引き起こす可能性があります。 
    
    > [!NOTE]
    > 確認して、サーバー上の有効なユーザーは、PSI の呼び出し、アプリケーションを使用するための十分なアクセス許可があることを確認します。 各 PSI メソッドの開発者ドキュメントのトピックには、プロジェクトのサーバーのアクセス許可のテーブルが含まれています。 などの[Project.QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx)メソッドには、**新しいプロジェクト**グローバル アクセス権と、 **SaveProjectTemplate**アクセス許可が必要です。 
  
    場合によっては、サーバー上でリモート デバッグを実行する必要があります。 SharePoint ファーム内の各プロジェクトのサーバー コンピューター上のイベント ハンドラー アセンブリをインストールして、一般に、プロジェクトのサーバーの設定] ページを使用して、Project Web App インスタンスのイベント ハンドラーを構成して、イベント ハンドラーを設定する必要がありますもSharePoint サーバーの管理のアプリケーションの設定です。
    
2. **開発用コンピューターを設定します。**
    
    通常、PSI にはネットワーク経由でアクセスします。コード サンプルは、記載されている場合を除き、サーバーから分離されたクライアントで動作するように作られています。
    
    1. **Visual Studio の適切なバージョンをインストールします。** 場合を除き、これらのコードが書き込まれます Visual C# で。 Visual Studio 2010 または Visual Studio 2012 では、それらを使用できます。 最新のサービス パックのインストールがあることを確認します。 
    
    2. **プロジェクト サーバー Dll を開発用コンピューターにコピーします。** 次のアセンブリをコピーする`[Program Files]\Microsoft Office Servers\15.0\Bin`開発用コンピューターに Project Server コンピューターにします。 
    
       - Microsoft.Office.Project.Server.Events.Receivers.dll
    
       - Microsoft.Office.Project.Server.Library.dll
    
    3. コンパイルし、PSI の WCF サービスの ProjectServerServices.dll プロキシ アセンブリを使用する方法の詳細については、 [PSI プロキシ アセンブリおよび IntelliSense の説明を使用して](#pj15_PrerequisitesWCF_BuildingProxy)参照してください。
    
3. **IntelliSense ファイルをインストールします。**
    
    Project 2013 SDK から更新された IntelliSense XML ファイルは、コピーである Project Server アセンブリのクラスとメンバーの IntelliSense の説明を使用するには、Project Server アセンブリが配置されている同じディレクトリにダウンロードします。 たとえば、アプリケーションが Microsoft.Office.Project.Server.Library.dll アセンブリへの参照に設定されているディレクトリに Microsoft.Office.Project.Server.Library.xml ファイルをコピーします。
    
    PSI サービス用の IntelliSense の説明で CompileWCFProxyAssembly.cmd スクリプトを使用して、PSI プロキシ アセンブリを作成することを必要とする、 `Documentation\IntelliSense\WCF` Project 2013 SDK ダウンロードのサブディレクトリです。 スクリプトは、ProjectServerServices.dll の WCF ベースのプロキシ アセンブリを作成します。 詳細については、SDK ダウンロードの [ReadMe_IntelliSense] .mht ファイルを参照してください。 
    
## <a name="creating-the-application-and-adding-a-service-reference"></a>アプリケーションを作成してサービス参照を追加する
<a name="pj15_PrerequisitesWCF_Configure"> </a>

1. **コンソール アプリケーションを作成します。**
    
    **[新しいプロジェクト**] ダイアログ ボックスのドロップダウン ボックスの一覧で、コンソール アプリケーションを作成するときは、 **.NET Framework 4**を選択します。 新しいアプリケーションには、PSI のコード例をコピーできます。
    
2. **WCF に必要な参照を追加します。**
    
    ソリューション エクスプ ローラーで、 **System.ServiceModel**への参照を追加します (図 1 を参照してください)。 Web アプリケーションでは、 **System.ServiceModel.Web**を使用します。
    
    **System.Runtime.Serialization**への参照を追加もできます。
    
    **図 1 です。WCF ベースのアプリケーション用の Visual Studio で参照を追加します。**

    ![WCF への参照を追加します。](media/pj15_PrerequisitesWCF_AddReference.gif "WCF への参照を追加します。")
  
3. **コードをコピー**します。
    
    コード サンプル全体をコンソール アプリケーションの Program.cs ファイルにコピーします。
    
4. **サンプル アプリケーションの名前空間を設定します。**
    
    サンプルの上部に記されている名前空間をアプリケーションの既定の名前空間に変更するか、アプリケーションの既定の名前空間をサンプルに合わせて変更することができます。アプリケーションの既定の名前空間は、アプリケーションのプロパティを変更することによって変更できます。 
    
    たとえば、 [ReadResource](https://msdn.microsoft.com/library/WebSvcResource.Resource.ReadResource.aspx)のコード サンプルは、 **Microsoft.SDK.Project.Samples.CreateResourceTest**名前空間を持っています。 **ResourceTest**の Visual Studio プロジェクトの名前が表示された場合、Program.cs ファイルから名前空間をコピーし、プロジェクト**のプロパティ**] ウィンドウを開きます ( **[プロジェクト**] メニューで、 **ResourceTest プロパティ**] をクリックすると)。 [**アプリケーション**] タブで、名前空間を**既定の名前空間**] テキスト ボックスにコピーします。 
    
5. **サービス参照を設定します。**
    
    多くの例では、1 つ以上の PSI サービスへの参照が必要です。これらは、サンプル自体、またはサンプルの前にあるコメントに示されています。サービス参照の適切な名前空間を取得するには、最初にアプリケーションの既定の名前空間を設定する必要があります。
    
    WCF サービス参照を追加する方法として次の 3 つがあります。
    
    - という名前の ProjectServerServices.dll、PSI プロキシ アセンブリをビルドし、アセンブリへの参照を設定します。 [PSI プロキシ アセンブリおよび IntelliSense の説明を使用して](#pj15_PrerequisitesWCF_BuildingProxy)参照してください。
    
    - Svcutil.exe 出力からプロキシ ファイルを Visual Studio ソリューションに追加します。 [PSI プロキシ ファイルを追加する](#pj15_PrerequisitesWCF_AddingProxyFile)を参照してください。
    
    - サービス参照を追加するには、Visual Studio を使用します。 [サービス参照の追加](#pj15_PrerequisitesWCF_AddingServiceReference)を参照してください。
    
### <a name="using-a-psi-proxy-assembly-and-intellisense-descriptions"></a>Intellisense の説明を備えた PSI プロキシ アセンブリを使用する
<a name="pj15_PrerequisitesWCF_BuildingProxy"> </a>

PSI のすべてのパブリック WCF サービスのプロキシ アセンブリを使用できます。 ProjectServerServices.dll プロキシ アセンブリを使用してコンパイルします`Documentation\IntelliSense\WCF\CompileWCFProxyAssembly.cmd`Project 2013 SDK のダウンロードのスクリプトを作成し、プロキシ アセンブリを開発用コンピューターにコピーします。 IntelliSense の同じ場所に ProjectServerServices.xml ファイルをコピーします。 Visual Studio は、ProjectServerServices.dll のプロキシ アセンブリへの参照を設定します。 
  
Project Server のサービス パックおよび更新プログラムの場合は、プロキシのソース ファイルを更新し、SDK ダウンロードの同じフォルダーに GenWCFProxyAssembly.cmd スクリプトを使用して、新しいプロキシ アセンブリを作成できます。 SDK をダウンロードするリンクは、 [Project 2013 開発者向けドキュメント](project-2013-developer-documentation.md)を参照してください。 詳細については、[サービス参照の追加](#pj15_PrerequisitesWCF_AddingServiceReference)を参照してください。 
  
> [!NOTE]
> Source.zip からプロキシ ソース ファイルを抽出するときにファイル内のファイル、`Documentation\IntelliSense\WCF\Source`は、Project 2013 SDK ダウンロードの発行日時点で現在のフォルダーです。 生成するには、PSI プロキシ ソース ファイルは、Project Server コンピューター上の GenASMXProxyAssembly.cmd スクリプトの実行を更新しました。 詳細については、[サービス参照の追加](#pj15_PrerequisitesWCF_AddingServiceReference)を参照してください。 
> 
> 内のスクリプト、`Documentation\IntelliSense\ASMX`フォルダーは、WCF ベースのアプリケーションでは機能しません。 GenASMXProxyAssembly.cmd スクリプトでは、ASMX サービスのソース コード ファイルを生成する、Wsdl.exe を呼び出します。 ASMX プロキシ ファイルには、さまざまなクラスとプロパティが含まれます。 などの資源の ASMX ベース web サービスには、WCF ベースのリソースのサービスには、**リソース**インターフェイス、 **ResourceChannel**インターフェイス、および**ResourceClient**のクラスが含まれていますに、**リソース**のクラスが含まれます。 
  
ASMX web サービスと WCF サービスの両方に対して作成された任意の名前空間は、IntelliSense の ProjectServerServices.xml ファイルは、どちらかのアセンブリで動作するよう、同じです。 ASMX ベースのプロキシ アセンブリの WCF ベースのプロキシ アセンブリ内のリソース サービスの名前空間は**SvcResource**です。 名前空間の名前を変更することができます、もちろん、-プロキシ アセンブリおよび IntelliSense の ProjectServerServices.xml ファイルに一致しているかどうかを確認します。
  
コード サンプルでは、PSI サービス名前空間に別の名前を使用する場合など**ProjectWebSvc**IntelliSense を実行するには、名前空間がプロキシ アセンブリと一致するように**SvcProject**を使用するサンプルを変更しなければなりません。 
  
WCF ベースのプロキシ アセンブリを使用する利点は、次のとおりです。
  
- ほとんどのソリューションを、Project Server コンピューターとは別のコンピューター上にあるプロキシ アセンブリで開発できます。ただし、個々のサービス参照の設定には、Project Server コンピューターでの開発が必要です。
    
- このプロキシ アセンブリにはすべての PSI サービス名前空間が含まれるので、複数のプロキシ ファイルを追加する必要がありません。
    
- ProjectServerServices.dll プロキシ アセンブリへの参照を設定するのと同じディレクトリに ProjectServerServices.xml ファイルを追加する場合は、PSI のクラスおよびメンバーの IntelliSense の説明を取得できます。 詳細についてを参照してください [ReadMe_IntelliSense] で、 `Documentation\IntelliSense` Project 2013 SDK ダウンロードのフォルダーです。 
    
**図 2 になります。リソース サービスのメソッドの IntelliSense を使用します。**

![ReadResource メソッドの Intellisense を使用します。](media/pj15_PrerequisitesWCF_Intellisense.gif "ReadResource メソッドの Intellisense を使用します。")
  
このプロキシ アセンブリを使用する場合の欠点は、ソリューションが大規模になることと、ソリューションと共にプロキシ アセンブリの配布とインストールが必要になることです。また、プロキシ アセンブリと Intellisense ファイルの中で同じ名前空間を使用する必要があります (ただし、スクリプトを修正して、独自のプロキシ アセンブリを作成し、別々の名前空間を使用するように ProjectServerServices.xml Intellisense ファイルを変更した場合は例外です)。
  
### <a name="adding-a-psi-proxy-file"></a>PSI プロキシ ファイルを追加する
<a name="pj15_PrerequisitesWCF_AddingProxyFile"> </a>

Project 2013 SDK ダウンロードには、プロキシ アセンブリの SvcUtil.exe コマンドによって生成されるソース ファイルが含まれています。 Source.zip ファイル内には、ソース ファイル、`Documentation\IntelliSense\WCF`のサブディレクトリです。 プロキシ アセンブリへの参照を設定する代わりに、Visual Studio のソリューションに 1 つまたは複数のソース ファイルを追加できます。 など、プロジェクトのサービスおよびリソースのサービスを使用するには、wcf を追加します。Project.cs と wcf。ソリューションのファイルを Resource.cs。 
  
WCF では、各 PSI サービスのプライマリ クラスがインターフェイスで定義されているし、クライアント クラスのメンバーにアクセスするために実装されています。 たとえば、 **SvcProject.Resource**インターフェイスは、 **SvcProject.ResourceClient**クラスに実装されます。 **ResourceClient**をという名前のクラス変数として**ResourceClient**オブジェクトを定義するには、次のコードを使用します。 この例では、 **SetClientEndpoints**メソッドは、app.config ファイルで定義されている**basicHttp_Project**のエンドポイントを使用する**resourceClient**オブジェクトを作成します。 App.config ファイルの詳細については、[サービス構成ファイルを追加する](#pj15_PrerequisitesWCF_AddConfig)を参照してください。 
  
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
> PSI プロキシ アセンブリを使用した場合、または**SvcResource**という名前のプロジェクトの [サービス参照のプロキシ ファイルを追加するかどうかは、 **resourceClient**オブジェクトを作成したりするに同じコードを使用します。 
  
### <a name="adding-a-service-reference"></a>サービス参照の追加
<a name="pj15_PrerequisitesWCF_AddingServiceReference"> </a>

PSI サービスのプロキシ ファイルを追加または WCF ベースのプロキシ アセンブリを使用するしないで場合、は、Visual Studio 内で直接 1 つ以上の個々 のサービス参照を設定できます。 準備するのには、更新されたプロキシ ファイルを作成するのには、次の手順のステップ 1 を使用することも、`Documentation\IntelliSense\WCF\GenWCFProxyAssembly.cmd`はスクリプト Project 2013 SDK ダウンロードに含まれています。 
  
> [!NOTE]
> サービス参照を設定するには、Project Server コンピューターで Visual Studio を使用する必要があります。Visual Studio 内でサービス参照を直接追加するよりも、ProjectServerServices.dll プロキシ アセンブリを使用するか、プロキシ ソース ファイルを追加することをお勧めします。 
  
次の手順では、Project Server のテスト インストールを実行するコンピューターに Visual Studio 2012 を使用してサービス参照を設定する方法を示しています。
  
1. バックエンド WCF サービスへのアクセスを取得するには、Project Server コンピューターで Visual Studio を実行します。
    
2. **ソリューション エクスプ ローラー**で、[**参照**] フォルダーを右クリックし、し、[**サービス参照の追加**」を選択します。 
    
3. [**サービス参照の追加**] ダイアログ ボックスの [**アドレス**] テキスト ボックスに、入力http://localhost:32843//psi/ _ServiceName_.svc の_GUID_、し、 **Enter**キーを押します。 _GUID_を 534c37eb00d74ccfadcecf9827e95239 など、Project Server サービス アプリケーションの仮想ディレクトリ名に置き換えます。 リソースなど、サービスの名前と_アドレス_を交換して (図 3 を参照してください)。 
    
   Project Server Service 仮想ディレクトリの名前は、以下のどちらかの方法で取得できます。
    
   - お使いのブラウザーでは、SharePoint 2013 のサーバーの管理アプリケーションを開きます。 **サービス アプリケーションの管理**を選択し、使用する Project Server の PSI サービス アプリケーションを選択します。 たとえば、 **ProjectServerService**を選択します。 Project Web App サイトの管理] ページの URL には、仮想ディレクトリ名が含まれています。 たとえば、 `http://ServerName:8080/_admin/pwa/managepwa.aspx?appid=534c37eb-00d7-4ccf-adce-cf9827e95239`、仮想ディレクトリ名は、 `534c37eb00d74ccfadcecf9827e95239` (ディレクトリ名にハイフンが含まれていません)。 
    
   - Project Server コンピューター上の**インターネット インフォメーション サービス (IIS) マネージャー** ] ダイアログ ボックスを開きます。 **[接続**] ウィンドウで [ **SharePoint Web サービス**] ノードを展開し、PSI フォルダーを含むディレクトリが見つかるまで、サービスの仮想ディレクトリを展開します。 ディレクトリを選択し、[**操作**] ウィンドウで、 **[詳細設定**を選択して、**仮想パス**] フィールドにディレクトリ名をコピーします。 
    
      > [!NOTE]
      > プロジェクト サーバーのサービスの 1 つ以上の仮想ディレクトリがあります。 Project Web App インスタンスが含まれている仮想ディレクトリを選択することを確認します。 
  
   - SharePoint 2013 がインストールされている Windows PowerShell で**get SPServiceApplication**コマンドレットを使用します。 タスク バーの [**開始**] メニューの**すべてのプログラム**を選択して、 **Microsoft SharePoint 2013 の製品**を選択し、 **SharePoint 2013 の管理シェル**します。 コマンドと (、Guid は異なるされます) に定義されたサービス アプリケーションを**SharePoint 2013get 管理シェル**ウィンドウで結果を次に示します。 Project Server サービス アプリケーションの GUID をコピーします。 
    
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
  
   Url など、`http://localhost:32843/534c37eb00d74ccfadcecf9827e95239/PSI/Resource.svc`は、Project Server サービスの標準的な。 
    
4. サービス参照が解決した後は、 **Namespace** ] テキスト ボックスに参照名を入力します。 Project 2013 開発者向けドキュメントのコード例では、任意の名前空間の名前**サービスの_アドレス_** を使用します。 たとえば、リソース サービスのコード例では**SvcResource**という名前します。
    
    **図 3 です。リソースの WCF ベースのサービス参照を追加します。**

    ![リソースの WCF ベースのサービス参照を追加します。](media/pj15_PrerequisitesWCF_AddSvcReference.gif "リソースの WCF ベースのサービス参照を追加します。")
  
5. (Web.config に変更)、元に、一時ディレクトリの web.config ファイル、プロジェクトのサービスを交換し、再実行`iisreset`。
    
## <a name="setting-other-references"></a>その他の参照を設定する
<a name="pj15_PrerequisitesWCF_OtherReferences"> </a>

プロジェクトのサーバー アプリケーションは、多くの場合、SharePoint 2013 web サービスなどのサービスを使用します。 他のサービスまたは参照する必要がある場合は、コード例に記載されています。
  
コード サンプルのローカル参照は、サンプルの上部の**using**ステートメントに表示されます。 
  
1. **ソリューション エクスプ ローラー**で、[**参照**] フォルダーを右クリックし、**参照の追加**を選択し、
    
2. **[参照**] を選択し、以前にコピーしたプロジェクトのサーバー Dll を格納する場所を参照します。 、必要な Dll を選択し、[ **ok]** をクリックします。
    
> [!NOTE]
> 開発用コンピューター上のアセンブリのバージョンがターゲット Project Server コンピューターのものと厳密に一致していることを確認します。 
  
## <a name="adding-a-service-configuration-file"></a>サービス構成ファイルを追加する
<a name="pj15_PrerequisitesWCF_AddConfig"> </a>

アプリケーションは、WCF サービスをプログラムによって構成、サービス構成ファイルを使用しません。 それ以外の場合、Windows アプリケーションやコンソール アプリケーションを使用して、 **system.serviceModel**要素、app.config ファイルにweb アプリケーションには、web.config ファイルでの**system.serviceModel**をが含まれています。App.config ファイルを使用してまたはプログラムを使用して WCF サービスの構成に関する詳細についてを参照してください[チュートリアル: PSI の開発アプリケーションが WCF を使用して](http://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx)。
  
サービス プロキシのソース ファイルが生成されると、SvcUtil.exe コマンドは、output.config ファイルに app.config ファイルで既定の**system.serviceModel**要素の基になるか、web.config ファイルにも作成されます。 Project 2013 SDK ダウンロードには、サンプルの output.config ファイルが含まれています`Documentation\IntelliSense\WCF\Source.zip`。 などの output.config の既定のファイル SvcUtil.exe を作成するリソースのサービスには、 **BasicHttpBinding_Resource**および**BasicHttpBinding_Resource1**という名前の 2 つのバインディングが含まれています。 **クライアント**要素には、2 つの既定のエンドポイントが含まれています。 1 つのエンドポイントは、セキュリティで保護されたアドレスへのアクセス、HTTP ポート 32843 では次のようにポート 32843、通常のアクセスは、他の. 
  
```XML
<client>
    <endpoint address="http://ServerName.domain:32843/GUID/PSI/Resource.svc/secure"
        binding="basicHttpBinding" bindingConfiguration="BasicHttpBinding_Resource"
        contract="SvcResource.Resource" name="BasicHttpBinding_Resource" />
address="http://ServerName.domain:32843/GUID/PSI/Resource.svc"
        binding="basicHttpBinding" bindingConfiguration="BasicHttpBinding_Resource1"
        contract="SvcResource.Resource" name="BasicHttpBinding_Resource1" />
</client>
```

PSI サービス構成では、既定のバインドやエンドポイントを使用しません。Project Server では、バックエンド サービスの呼び出しでルーターとして動作するフロントエンド ProjectServer.svc を介してアプリケーションが PSI サービスにアクセスする必要があります。app.config ファイルを作成するには、以下の手順を実行します。
  
1. ProjectServerServices.dll プロキシ アセンブリへの参照を設定した場合、またはサービスのプロキシのソース ファイルを追加する場合は、アプリケーションに app.config ファイルが含まれていません。 Visual Studio プロジェクトに新しい項目を追加します。 **新しい項目の追加**] ダイアログ ボックスで**アプリケーション構成ファイル**のテンプレートを選択、app.config という名前を付けますし、**追加**します。
    
2. App.config ファイル内のすべてのテキストを削除し、ファイルに次のコードをコピーします。 バインディングは同じ例を使用することができます`basicHttpConf`、サービス エンドポイントごとにします。 、複数のバインディングを使用する場合など、HTTP と HTTPS の両方のプロトコルをバインドするのには作成する必要があるプロトコルごとにバインドします。
    
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
                                <transport clientCredentialType="Ntlm" realm="http://SecurityDomain" />
                            </security>
                        </binding>
                    </basicHttpBinding>
                </bindings>
                <client>
                    <endpoint address="http://ServerName/ProjectServerName/_vti_bin/PSI/ProjectServer.svc"
                        behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
                        bindingConfiguration="basicHttpConf" 
                        contract="SvcServiceName.ServiceName"
                        name="basicHttp_ServiceName" />
                </client>
            </system.serviceModel>
        </configuration>
    ```

3. 交換`ServerName/ProjectServerName`サーバーに、Project Web App インスタンスの名前を持つクライアント エンドポイントのアドレスにします。 
    
4. 交換`ServiceName`リソースなど、PSI サービスの名前です。 たとえば、サービス名のすべての 3 つを交換することを確認します。
    
    ```XML
        <endpoint address="http://myserver/pwa/_vti_bin/PSI/ProjectServer.svc"
            behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
            bindingConfiguration="basicHttpConf" 
            contract="SvcResource.Resource"
            name="basicHttp_Resource" />
    ```

5. 使用するには複数の 1 つの PSI サービスにはの各サービスおよび各サービスを使用する**バインディング**要素の 1 つの**エンドポイント**要素を作成します。 たとえば、次のエンドポイントは、プロジェクトのサービスおよび QueueSystem サービスの基本的な HTTP バインディングを使用するクライアントを構成します。 
    
    > [!NOTE]
    > アプリケーションの実行時に、サーバーがビジー状態である、または HTTP 要求が許可されていないことを示すエラーが表示される場合は、app.config ファイルのエンドポイント アドレスが正しいことを確認してください。 
  
    ```XML
        <client>
        <endpoint address="http://ServerName/pwa/_vti_bin/PSI/ProjectServer.svc"
            behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
            bindingConfiguration="basicHttpConf" 
            contract="SvcProject.Project"
            name="basicHttp_Project" />
        <endpoint address="http://ServerName/pwa/_vti_bin/PSI/ProjectServer.svc"
            behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
            bindingConfiguration="basicHttpConf" 
            contract="SvcQueueSystem.QueueSystem"
            name="basicHttp_QueueSystem" />
        </client>
    ```

App.config ファイルを編集するには、Visual Studio で**WCF サービス構成エディター**を使用する ([**ツール**] メニュー)。 図 4 は、 **Microsoft のサービス構成エディター** ] ダイアログ ボックスで、**契約**の要素を設定する方法を示します。 ソリューションでは、PSI プロキシ アセンブリを使用されている場合に ProjectServerServices.dll を開き、 `bin\debug` Visual Studio のソリューションのディレクトリです。 **コントラクト型ブラウザー** ] ダイアログ ボックスには、(図 5 を参照)、WCF サービス コントラクトのすべてが表示されます。 
  
**図 4 です。WCF サービス構成エディターを使用してください。**

![WCF サービス構成エディターを使用してください。](media/pj15_PrerequisitesWCF_ServiceConfigurationEditor.gif "WCF サービス構成エディターを使用してください。")
  
ソリューションは、wcfResource.cs など、サービスのプロキシ ファイルを使用している場合アプリケーションをコンパイルし、実行可能ファイルを開き、`bin\debug`ディレクトリです。 App.config ファイルを編集の詳細についてを参照してください[チュートリアル: PSI の開発アプリケーションが WCF を使用して](http://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx)。
  
**図 5。コントラクト型ブラウザーには、WCF サービス構成エディターを使用します。**

![コントラクト型ブラウザーを使用してください。](media/pj15_PrerequisitesWCF_ContractTypeBrowser.gif "コントラクト型ブラウザーを使用してください。")
  
## <a name="using-multiple-authentication"></a>複数の認証を使用する
<a name="pj15_PrerequisitesWCF_ClaimsMultiAuth"> </a>

Windows 認証またはフォーム認証では、オンプレミスの Project Server のユーザーの認証はクレーム処理では、SharePoint によって行われます。 複数の認証では、Project Web App が提供されている web アプリケーションが Windows 認証とフォーム ベース認証の両方をサポートしていることを意味します。 場合は、請求処理は、ユーザーの認証の種類を判断できないために次のエラーでは、Windows 認証を使用する WCF サービスへの呼び出しが失敗します。
  
`The server was unable to process the request due to an internal error. For more information about the error, either turn on Include ExceptionDetailInFaults (either from ServiceBehaviorAttribute or from the <serviceDebug> configuration behavior) on the server in order to send the exception information back to the client, or turn on tracing as per the Microsoft .NET Framework 3.0 SDK documentation and inspect the server trace logs.`

WCF に対して、問題を解決するには、各 PSI サービス用に定義されている**OperationContextScope**内 PSI メソッドへのすべての呼び出しがあります。 複数サービスのスコープを入れ子にしないでたとえば、リソースとプロジェクトのサービスへの呼び出しを使用して、呼び出しの各セット必要がありますそのスコープ内で。 
  
次の例では、アプリケーション内のすべての**OperationContextScope**セクションから、 **DisableFormsAuth**メソッドを呼び出すことができます。 メソッドは、 _isWindowsAuth_パラメーターが**false**の場合、フォーム認証を行えるように、フォーム認証を無効に設定されているヘッダーの値を削除します。 _IsWindowsAuth_が**true**の場合、 **DisableFormsAuth**メソッドには、フォーム認証が無効になります。 
  
メソッドでは、 **WcfSample** 、 **projectClient**オブジェクトは、PSI の**SvcProject.ProjectClient**クラスのインスタンスです。 
  
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
> **OperationContextScope**内の PSI 呼び出しを実行することは、複数認証環境で実行されるアプリケーションでのみ必要があります。 Project Server は、Windows 認証のみを使用する場合は、スコープを設定し、フォーム認証を無効にする web 要求ヘッダーを追加する必要はありません。 
> 
> ASMX ベースのアプリケーション用の修正プログラムは、異なります。 詳細については、[プロジェクト内の ASMX ベースのコード サンプルの前提条件](prerequisites-for-asmx-based-code-samples-in-project.md)で*を使用する複数の認証*] セクションを参照してください。 
  
## <a name="changing-values-of-generic-constants"></a>一般的な定数の値を変更する
<a name="pj15_PrerequisitesWCF_ChangeValues"> </a>

ほとんどのサンプルでは、更新する必要が、サンプルを動作させるため正しく、環境内の 1 つまたは複数の変数があります。 次の例では、SSL がインストールされている場合は HTTP プロトコルではなく HTTPS プロトコルを使用します。 _サーバー名_を使用しているサーバーの名前に置き換えます。 _ProjectServerName_を PWA など、プロジェクトのサーバー サイトの仮想ディレクトリ名に置き換えます。 
  
```cs
const string PROJECT_SERVER_URI = "http://ServerName/ProjectServerName/";
```

ほかに変更が必要な変数があれば、コード サンプルの上部に記載されています。
  
## <a name="verifying-the-results"></a>結果を確認する
<a name="pj15_PrerequisitesWCF_Verify"> </a>

取得し、コード サンプルの結果を解釈する常に簡単ではありません。 たとえば、プロジェクトを作成する場合は、Project Web App の [プロジェクト センター] ページに表示するプロジェクトを発行する必要があります。
  
コード サンプルの結果は、いくつかの方法で確認できます。たとえば、次のような方法があります。
  
- プロジェクト評価のためのクライアントを使用して、Project Server コンピューターからプロジェクトを開くし、目的のアイテムを表示します。
    
- Project Web App の [プロジェクト センター] ページで発行されたプロジェクトを表示する ( `http://ServerName/ProjectServerName/projects.aspx`)。
    
- Project Web App では、キューのログを表示します。 サーバー設定] ページを開く (右上隅で、[**設定**] アイコンを選択します)、**個人用の設定**] セクションで [**自分のキュー ジョブ**を選択し、( `http://ServerName/ProjectServerName/MyJobs.aspx`)。 **ビュー** 」ドロップ ダウン リストで、ジョブの状態で並べ替えることができます。 既定の状態が**進行中で過去 1 週間のジョブの失敗です**。 
    
- Project Web App の [サーバー設定] ページを使用して ( `http://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`) とすべてのキュー ジョブの管理、削除、またはチェックインのエンタープライズ オブジェクトを強制的にします。 [サーバーの設定] ページで、これらのリンクにアクセスする管理者の権限がある必要があります。
    
- Project Server データベースのテーブルに対してクエリを実行するのにには、 **Microsoft SQL Server Management Studio の**を使用します。 たとえば、ワークフロー ステージでプロジェクト詳細ページ (Pdp) に関する情報を表示するのに MSP_WORKFLOW_STAGE_PDPS テーブルの上の 200 行を選択するのには次のクエリを使用します。 
    
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

## <a name="cleaning-up"></a>クリーンアップする
<a name="pj15_PrerequisitesWCF_Cleanup"> </a>

一部のコード サンプルをテストした後、エンタープライズ オブジェクトと設定を削除またはリセットする必要があります。 Project Web App の [サーバー設定] ページを使用するにはエンタープライズ ・ データを管理する ( `http://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`)。 [サーバー設定] ページのリンクを使用すると、古いアイテムを削除する、強制的にチェックインのプロジェクト、すべてのユーザーのジョブ キューの管理、その他の管理タスクを実行できます。
  
以下に、コード サンプル実行後の一般的なクリーンアップ作業で使用する、[サーバー設定] ページ上のリンクの一部を示します。
  
- **エンタープライズ ユーザー設定フィールドと参照テーブル**
    
- **キュー ジョブを管理します。**
    
- **エンタープライズ オブジェクトを削除します。**
    
- **チェックインのエンタープライズ オブジェクトを強制的に**
    
- **エンタープライズ プロジェクトの種類**
    
- **ワークフロー フェーズ**
    
- **ワークフロー ステージ**
    
- **プロジェクト詳細ページ**
    
- **タイムシート期間**
    
- **タイムシートの設定と既定の設定**
    
- **行の分類**
    
特定の Project Web App サーバーの設定ページではなく、Project Web App インスタンスごとに、SharePoint Server 2013 では、追加の設定が管理されます。 SharePoint サーバーの全体管理アプリケーションで、**アプリケーションの全般的な設定**を選択し、**プロジェクトのサーバーの設定**、[**管理**] を選択を [サーバーの設定] ページで、ドロップダウン ボックスの一覧で、Project Web App インスタンスを選択. たとえば、選択した Project Web App インスタンスのイベント ハンドラーを追加、削除する**サーバー側のイベント ハンドラー**を選択します。 
  
## <a name="see-also"></a>関連項目

- [プロジェクト内の ASMX ベースのコード サンプルの前提条件](prerequisites-for-asmx-based-code-samples-in-project.md)   
- [チュートリアル: WCF を使用して PSI アプリケーションを開発します。](http://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx)   
- [WCF で偽装を使用します。](http://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)  
- [プロジェクト PSI リファレンスの概要](project-psi-reference-overview.md) 
- [SharePoint デベロッパー センター](http://msdn.microsoft.com/en-us/sharepoint/default.aspx)
    

