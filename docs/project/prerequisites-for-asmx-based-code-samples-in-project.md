---
title: プロジェクト内のASMXベースコードサンプルの前提条件
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
f1_keywords:
- code samples
- Project Server code samples
- Project Server programming
- PSI code samples
- PSI programming
keywords:
- コード サンプル、プロジェクト サーバー、Project Server、プログラミング、PSI、コンパイル コード サンプル、PSI、プログラミング
localization_priority: Normal
ms.assetid: df584b25-4460-46c8-89a8-3b2c94d20bba
description: Project Server Interface (PSI) リファレンス トピックに含まれる ASMX ベースのコード サンプルを使用して、Visual Studio でプロジェクトを作成するのに役立つ情報について説明します。
ms.openlocfilehash: 26ad2e388b7e7f6f19e028b47c7f6d1a3fbd020c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357087"
---
# <a name="prerequisites-for-asmx-based-code-samples-in-project"></a>プロジェクト内のASMXベースコードサンプルの前提条件

Project Server Interface (PSI) リファレンス トピックに含まれる ASMX ベースのコード サンプルを使用して、Visual Studio でプロジェクトを作成するのに役立つ情報について説明します。
  
[Project Server 2013](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx)クラス ライブラリと Web サービスリファレンスに含まれるコード サンプルの多くは、もともと Office Project 2007 SDK 用に作成され、ASMX Web サービスの標準形式を使用しています。 サンプルは引き続き Project Server 2013 で動作し、コンソール アプリケーションにコピーされ、完全なユニットとして実行するように設計されています。 例外はサンプルに記載されています。 
  
2013 SDK Projectの新しい PSI サンプルは、WINDOWS (WCF) サービスを使用する形式に準拠しています。 この ASMX ベースのサンプルは、WCF サービスを使用するように調整することもできます。 この記事では、ASMX Web サービスでサンプルを使用する方法を示します。 WCF サービスでサンプルを使用する方法については、「WCF ベースのコード サンプルの前提条件」を参照[Project。](prerequisites-for-wcf-based-code-samples-in-project.md)
  
> [!NOTE]
> PSIのASMX WebサービスインターフェイスはProject Server 2013では非推奨ですが、引き続きサポートされています。 クライアント側オブジェクト モデル (CSOM) にアプリケーションで必要なメソッドが含まれる場合は、CSOM を使用して新しいアプリケーションを開発する必要があります。 CSOM を使用すると、アプリケーションはサーバーサーバー 2013 のProject Onlineまたはオンプレミスインストールで動作Projectできます。 それ以外の場合、アプリケーションで PSI を使用する場合は、ネットワーク通信に推奨されるテクノロジである WCF インターフェイスを使用する必要があります。 ASMX インターフェイスまたは WCF インターフェイスを使用するアプリケーションは、サーバー 2013 のオンプレミス インストールProjectできます。 CSOM の詳細については[、「Project Server 2013](project-server-2013-architecture.md)アーキテクチャとクライアント側オブジェクト モデル[(CSOM) for Project 2013」を参照](client-side-object-model-csom-for-project-2013.md)してください。 
  
コード サンプルを実行する前には、開発環境を設定し、アプリケーションを構成し、環境に一致するように一般的な定数の値を変更する必要があります。
  
## <a name="setting-up-the-development-environment"></a>開発環境を設定する
<a name="pj15_PrerequisitesASMX_Setup"> </a>

1. **テスト Project Server システムを設定する**。
    
   開発やテストを行う際には常にテスト Project Server システムを使用します。たとえコードが完全に動作しても、プロジェクト間の依存関係、レポート、またはその他の環境要因が意図しない結果を引き起こす可能性があります。 
    
   > [!NOTE]
   > サーバーの有効なユーザーであり、アプリケーションで使用する PSI 呼び出しのための十分な権限を持っていることを確認します。 各 PSI メソッドのリファレンス トピックに、Project Server 権限の表があります。 たとえば、次の [Project。QueueCreateProject メソッド](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx)には、**グローバルな NewProject** アクセス許可と **SaveProjectTemplate アクセス許可が必要** です。 
  
   場合によっては、サーバーでのリモート デバッグが必要になることがあります。 SharePoint ファームの各 Project Server コンピューターにイベント ハンドラー アセンブリをインストールし、SharePoint サーバーの全体管理の全般アプリケーション 設定 の Project Server 設定 ページを使用して Project Web App インスタンスのイベント ハンドラーを構成することで、イベント ハンドラーをセットアップする必要があります。
    
2. **開発用コンピューターをセットアップする。**
    
   通常、PSI にはネットワーク経由でアクセスします。コード サンプルは、記載されている場合を除き、サーバーから分離されたクライアントで動作するように作られています。
    
   1. **適切なバージョンの Visual Studio をインストールする。** 記載されている場合を除き、コード サンプルは Visual C# で記述されています。 これらは、2010 年Visual Studio 2012 年Visual Studioできます。 最新のサービス パックがインストールされていることを確認してください。 
        
   2. **Project Server の DLL を開発用コンピューターにコピーする。** サーバー コンピューター上の次の `[Program Files]\Microsoft Office Servers\15.0\Bin` アセンブリProject開発用コンピューターにコピーします。 
        
      - Microsoft.Office.Project.Server.Events.Receivers.dll
      - Microsoft.Office.Project.Server.Library.dll
        
   3. PSI で ASMX Web サービスの ProjectServerServices.dll プロキシ アセンブリをコンパイルして使用する方法については、「[IntelliSense の説明を備えた PSI プロキシ アセンブリを使用する](#pj15_PrerequisitesASMX_BuildingProxy)」を参照してください。
    
3. **IntelliSense ファイルをインストールする。**
    
    Project Server アセンブリのクラスとメンバーに IntelliSense の説明を使用するには、Project 2013 SDK のダウンロードから更新された IntelliSense XML ファイルを、Project Server アセンブリがある同じディレクトリにコピーします。 たとえば、アプリケーションで Microsoft.Office.Project.Server.Library.dll アセンブリへの参照を設定するディレクトリに、Microsoft.Office.Project.Server.Library.xml ファイルをコピーします。
    
    IntelliSense PSI Web サービスの説明では、Project SDK ダウンロードのサブディレクトリで CompileASMXProxyAssembly.cmd スクリプトを使用して PSI プロキシ アセンブリを作成する必要があります。 `Documentation\IntelliSense\WSDL` このスクリプトを実行すると、ASMX ベースの ProjectServerServices.dll プロキシ アセンブリが作成されます。 詳細については、SDK ダウンロードの [ReadMe_IntelliSense] ファイルを参照してください。 
    
## <a name="creating-the-application-and-adding-a-web-service-reference"></a>アプリケーションを作成して Web サービス参照を追加する
<a name="pj15_PrerequisitesASMX_Configure"> </a>

1. **コンソール アプリケーションを作成する**。
    
   コンソール アプリケーションを作成するには、[**新しいプロジェクト**] ダイアログ ボックスのドロップダウン リストから [**.NET Framework 4**] を選択します。この新しいアプリケーションに PSI サンプル コードをコピーできます。
    
2. **ASMX に必要な参照を追加する。**
    
   ソリューション エクスプローラーで、**System.Web.Services** への参照を追加します (図 1 を参照)。 
    
   **図 1. Visual Studio での参照の追加**

   ![[参照の追加] Visual Studio](media/pj15_PrerequisitesASMX_AddReference.gif "に参照を追加Visual Studio")
  
3. **コードをコピーする。**
    
   コード サンプル全体をコンソール アプリケーションの Program.cs ファイルにコピーします。
    
4. **サンプル アプリケーションの名前空間を設定する**。
    
   サンプルの上部に記されている名前空間をアプリケーションの既定の名前空間に変更するか、アプリケーションの既定の名前空間をサンプルに合わせて変更することができます。アプリケーションの既定の名前空間は、アプリケーションのプロパティを変更することによって変更できます。
    
   たとえば [、QueueRenameProject のコード サンプルには](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueRenameProject.aspx)**、Microsoft.SDK.Project という名前空間があります。Samples.RenameProject**. Visual Studio プロジェクトの名前が **RenameProject** の場合、Program.cs ファイルから名前空間をコピーし、プロジェクトの [**プロパティ**] ウィンドウを表示します ([**プロジェクト**] メニューの [**RenameProject のプロパティ**] を選択)。 [**アプリケーション**] タブで、名前空間を [**既定の名前空間**] ボックスにコピーします。 
    
5. **Web 参照を設定する。**
    
   多くの例では、1 つ以上の PSI Web サービスへの参照が必要です。これらは、サンプル自体、またはサンプルの前にあるコメントに示されています。Web 参照の適切な名前空間を取得するには、最初にアプリケーションの既定の名前空間を設定する必要があります。
    
   PSI の ASMX Web サービス参照を追加する方法として次の 3 つがあります。
    
   - ProjectServerServices.dll という名前の PSI プロキシ アセンブリを作成してから、このアセンブリへの参照を設定します。 IntelliSense を取得するには、これが PSI 参照を追加する方法として推奨される方法です。 詳細については「[Intellisense の説明を備えた PSI プロキシ アセンブリを使用する](#pj15_PrerequisitesASMX_BuildingProxy)」を参照してください。
    
   - wsdl.exe から出力されるプロキシ ファイルを Visual Studio ソリューションに追加します。 「[PSI プロキシ ファイルを追加する](#pj15_PrerequisitesASMX_AddingProxyFile)」を参照してください。
    
   - Visual Studio を使用して Web サービス参照を追加します。「[Web サービス参照を追加する](#pj15_PrerequisitesASMX_AddingServiceReference)」を参照してください。

<a name="pj15_PrerequisitesASMX_BuildingProxy"> </a>

### <a name="using-a-psi-proxy-assembly-and-intellisense-descriptions"></a>Intellisense の説明を備えた PSI プロキシ アセンブリを使用する

Project SDK ダウンロードのフォルダーにある CompileASMXProxyAssembly.cmd スクリプトを使用して、PSI 内のすべての ASMX ベースの Web サービスに対して ProjectServerServices.dll プロキシ アセンブリを構築して使用できます。 `Documentation\IntelliSense\WSDL` ダウンロードへのリンクについては、「Project [2013 開発者向けドキュメント」を参照してください](project-2013-developer-documentation.md)。
  
> [!NOTE]
> Source.zip ファイルからプロキシ ソース ファイルを抽出すると、フォルダー内のファイルは、2013 SDK ダウンロードの発行日Project `Documentation\IntelliSense\WSDL\Source` です。 更新された PSI プロキシ ソース ファイルを生成するには、Project Server コンピューターで GenASMXProxyAssembly.cmd スクリプトを実行します。 フォルダー内のスクリプト  `Documentation\IntelliSense\WCF` は、ASMX ベースのアプリケーションでは機能しません。 GenWCFProxyAssembly.cmd スクリプトは SvcUtil.exe を呼び出し、それによって WCF サービス用のソース コード ファイルが生成されます。 WCF プロキシ ファイルには、各 PSI サービス用の別の複数の属性、チャネル インターフェイス、およびクライアント クラスが含まれます。 たとえば、WCF ベースの Resource サービスには **ResourceChannel** インターフェイス、**Resource** インターフェイス、および **ResourceClient** クラスが含まれています。 ASMX ベースの Resource Web には **Resource** クラスといくつかの異なるプロパティが含まれています。 
  
次に、GenASMXProxyAssembly.cmd スクリプトを示します。このスクリプトは、PSI Web サービスの WSDL 出力ファイルを生成した後、アセンブリをコンパイルします。
  
```MS-DOS
@echo off
@ECHO ---------------------------------------------------
@ECHO Creating C# files for the ASMX-based proxy assembly
@ECHO ---------------------------------------------------
REM Replace ServerName with the name of the server and 
REM the instance name of Project Web App. Do not use localhost.
(set VDIR=https://ServerName/pwa/_vti_bin/psi)
(set OUTDIR=.\Source)
REM ** Wsdl.exe is the same version in the v6.0A and v7.0A subdirectories. 
(set WSDL="C:\Program Files (x86)\Microsoft SDKs\Windows\v7.0A\Bin\x64\wsdl.exe")
if not exist %OUTDIR% (
md %OUTDIR%
)
for /F %%i in (Classlist_asmx.txt) do %WSDL% /nologo /l:CS /namespace:Svc%%i /out:%OUTDIR%\wsdl.%%i.cs %VDIR%/%%i.asmx?wsdl 
@ECHO ----------------------------
@ECHO Compiling the proxy assembly
@ECHO ----------------------------
(set SOURCE=%OUTDIR%\wsdl)
(set CSC=%WINDIR%\Microsoft.NET\Framework64\v4.0.30319\csc.exe)
(set ASSEMBLY_NAME=ProjectServerServices.dll)
%CSC% /t:library /out:%ASSEMBLY_NAME% %SOURCE%*.cs
```

スクリプトは ClassList_asmx.txt ファイルを使用します。このファイルには、サードパーティのデベロッパーが使用できる Web サービスのリストが含まれています。
  
```text
Admin
Archive
Calendar
CubeAdmin
CustomFields
Driver
Events
LoginForms
LoginWindows
LookupTable
Notifications
ObjectLinkProvider
PortfolioAnalyses
Project
QueueSystem
ResourcePlan
Resource
Security
Statusing
TimeSheet
Workflow
WssInterop
```

このスクリプトは ProjectServerServices.dll という名前のアセンブリを作成します。WCF ベースのアセンブリ用の ProjectServerServices.dll と混同しないようにしてください。ProjectServerServices.xml IntelliSense ファイルを使用していずれかのアセンブリの使用を有効にする場合、アセンブリ名は同じです。
  
ASMX Web サービスと WCF サービスの両方について、スクリプトによって作成される任意の名前空間は同一です。そのため、ProjectServerServices.xml IntelliSense ファイルはどちらのアセンブリでも使用できます。たとえば、WCF ベースのプロキシ アセンブリと ASMX ベースのプロキシ アセンブリ内の Resource サービスの名前空間は、**SvcResource** です。名前空間の名前を変更することもできますが、プロキシ アセンブリ内と ProjectServerServices.xml IntelliSense ファイル内では一致している必要があります。
  
コード サンプルで PSI Web サービス名前空間の異なる名前を使用する場合 (たとえば **ProjectWebSvc**)、IntelliSense が機能するためには、**SvcProject** を使用するようにサンプルを変更し、名前空間がプロキシ アセンブリと一致するようにします。 
  
ASMX ベースのプロキシ アセンブリを使用する利点は、すべての PSI Web サービス名前空間が含まれるという利点があります。複数の Web 参照を作成する必要はない。 もう 1 つの利点は、ProjectServerServices.dll プロキシ アセンブリへの参照を設定する同じディレクトリに ProjectServerServices.xml ファイルを追加すると、PSI クラスとメンバーの IntelliSense の説明を取得できるという利点があります。 図 2 は、IntelliSenseのテキストを **Project。QueueCreateProject** メソッド。 詳細については、2013 SDK ダウンロードの IntelliSense Project フォルダーにある [ReadMe_IntelliSense] ファイルを参照してください。 
  
**図 2. Project Web サービスのメソッドでの IntelliSense の使用**

![PSI サービス内のメソッドに Intellisense]を使用する PSI サービス内のメソッドに(media/pj15_PrerequisitesASMX_Intellisense.gif "Intellisense")を使用する
  
このプロキシ アセンブリを使用する場合の欠点は、ソリューションが大規模になることと、ソリューションと共にプロキシ アセンブリの配布とインストールが必要になることです。また、プロキシ アセンブリ内と IntelliSense ファイル内で同じ名前空間を使用する必要があります (ただし、スクリプトと ProjectServerServices.xml IntelliSense ファイルを変更して、別々の名前空間を使用するようにした場合は例外です)。
  
### <a name="adding-a-psi-proxy-file"></a>PSI プロキシ ファイルを追加する
<a name="pj15_PrerequisitesASMX_AddingProxyFile"> </a>

2013 Project SDK のダウンロードには、プロキシ アセンブリの Wsdl.exe コマンドによって生成されたソース ファイルが含まれています。 ソース ファイルはサブディレクトリSource.zipに  `Documentation\IntelliSense\ASMX` 保存されます。 プロキシ アセンブリへの参照を設定する代わりに、1 つ以上のソース ファイルを別のソリューションにVisual Studioできます。 たとえば、GenASMXProxyAssembly.cmd スクリプトを実行した後、wsdl を追加します。Project.cs ファイルをソリューションに追加します。 スクリプトを実行する代わりに、次のコマンドを実行して、たとえば 1 つのソース ファイルを生成できます。 
  
```MS-DOS
set VDIR=https://ServerName/ProjectServerName/_vti_bin/psi
set WSDL="C:\Program Files (x86)\Microsoft SDKs\Windows\v7.0A\Bin\x64\wsdl.exe"
%WSDL% /nologo /l:cs /namespace:SvcProject /out:wsdl.Project.cs %VDIR%/Project.asmx?wsdl
```

**Project** オブジェクトを **project** という名前のクラス変数として定義するには、以下のコードを使用します。**AddContextInfo** メソッドによって、Windows 認証およびフォームベース認証を使用するためのコンテキスト情報が **project** オブジェクトに追加されます。 
  
```cs
private static SvcProject.Project project;
private static SvcLoginForms.LoginForms loginForms =
            new SvcLoginForms.LoginForms();
. . .
public void AddContextInfo()
{
    // Add the Url property.
    project.Url = "https://ServerName /ProjectServerName /_vti_bin/psi/project.asmx";
    // Add Windows credentials.
    project.Credentials = CredentialCache.DefaultCredentials;
    // If Forms authentication is used, add the Project Server cookie.
    project.CookieContainer = loginForms.CookieContainer;
}
```

> [!NOTE]
> PSI プロキシ アセンブリを使用する場合も、プロキシ ファイルを追加して **SvcProject** という名前の Project サービス参照を追加する場合も、同じコードを使用して **project** オブジェクトを使用します。 
  
### <a name="adding-a-web-service-reference"></a>Web サービス参照を追加する
<a name="pj15_PrerequisitesASMX_AddingServiceReference"> </a>

ASMX ベースのプロキシ アセンブリを使用したり、WSDL 出力ファイルを追加したりしない場合は、1 つ以上の個別 Web 参照を設定できます。 次の手順は、2012 年に Web リファレンスを使用して web 参照をVisual Studioします。
  
1. **ソリューション エクスプローラー** で、[**参照設定**] フォルダーを右クリックし、[**サービス参照の追加**] をクリックします。 
    
2. [**サービス参照の追加**] ダイアログ ボックスで、[**詳細設定**] を選択します。
    
3. [**サービス参照の設定**] ダイアログ ボックスで、[**Web 参照の追加**] を選択します。
    
4. **[URL] テキスト ボックス** に `https:// _ServerName_/ _ProjectServerName_/_vti_bin/psi/ _ServiceName_.asmx?wsdl` 「」と入力し **、Enter** キーを押するか、[移動] アイコン **を選択** します。 SSL (SSL) Secure Sockets Layerしている場合は、HTTP プロトコルの代わりに HTTPS プロトコルを使用する必要があります。 

   たとえば、次の URL をサイトの Projectサービスに使用して `https://MyServer/pwa` 、Project Web App。`https://MyServer/pwa/_vti_bin/psi/project.asmx?wsdl`
    
   または、Web ブラウザーを開き、に移動します `https://ServerName/ProjectServerName/_vti_bin/psi/ServiceName.asmx?wsdl` 。 ファイルをローカル ディレクトリ (など) に保存します `C:\Project\WebServices\ServiceName.wsdl` 。 [**Web 参照の追加**] ダイアログ ボックスの [**URL**] にファイル プロトコルとファイルへのパスを入力します。 たとえば、と入力します `file://C:\Project\WebServices\Project.wsdl` 。 
    
5. 参照が解決した後、[**Web 参照名**] ボックスに参照名を入力します。 2013 年 2013 Projectのコード例では、任意の標準参照名 **Svc _ServiceName を使用します_**。 たとえば、Project Web サービスは **SvcProject** という名前になっています (図 3 を参照)。 
    
   **図 3. ASMX Web サービス参照の追加**

   ![ASMX Web サービス参照の追加](media/pj15_PrerequisitesASMX_AddWebSvcReference.gif "ASMX Web サービス参照の追加")
  
Project Server コンピューター上で実行する必要があるアプリケーション コンポーネントについては、偽装を使用するか、または引き上げられたアクセス許可を使用して、ASMX Web 参照の代わりに WCF サービス参照を使用します。 詳細については、「Wcf ベースのコード サンプルの前提条件」を[参照Project。](prerequisites-for-wcf-based-code-samples-in-project.md)
  
## <a name="setting-other-references"></a>その他の参照を設定する
<a name="pj15_PrerequisitesASMX_OtherReferences"> </a>

Projectサーバー アプリケーションは、多くの場合、サーバー 2013 web サービスなどのSharePointサービスを使用します。 その他のサービスが必要である場合、サービスはサンプルに記載されています。
  
コード サンプルのローカル参照は、サンプルの上部の **using** ステートメントに一覧表示されています。 
  
1. **ソリューション エクスプローラー** で、[**参照設定**] フォルダーを右クリックし、[**参照の追加**] をクリックします。
    
2. [**参照**] をクリックして、以前にコピーした Project Server の DLL を格納した場所を参照します。必要な DLL を選択して、[**OK**] を選択します。
    
> [!NOTE]
> 開発用コンピューター上のアセンブリのバージョンがターゲット Project Server コンピューターのものと厳密に一致していることを確認します。 
  
## <a name="using-multiple-authentication"></a>複数の認証を使用する
<a name="pj15_PrerequisitesASMX_ClaimsMultiAuth"> </a>

Windows 認証とフォーム認証のProject、オンプレミスのサーバー ユーザーの認証は、SharePoint Server 2013 で行われます。 複数認証とは、プロビジョニングされている Web アプリケーションがProject Web App認証とフォーム ベース認証Windows両方をサポートします。 この場合、Windows 認証を使用する ASMX Web サービスの呼び出しは、クレーム プロセスで認証するユーザーの種類を決定できないので、次のエラーで失敗します。
  
`The server was unable to process the request due to an internal error. . . .`

ASMX のこの問題を修正するには、PSI メソッドのすべての呼び出しをそれぞれの PSI Web サービスに対して定義される派生クラスに対して実行する必要があります。また、派生クラスは **SvcLoginWindows.LoginWindows** クラスを使用して派生 PSI サービス クラスの Cookie を取得する必要があります。以下の例で、**ProjectDerived** クラスは **SvcProject.Project** クラスから派生します。派生したクラスによって **EnforceWindowsAuth** プロパティが追加され、**Project** クラスのメソッドに対するすべての呼び出しの Web 要求ヘッダーが上書きされます。**EnforceWindowsAuth** プロパティが **true** の場合、**GetWebRequest** メソッドによって、フォーム認証を無効にするヘッダーが追加されます。**EnforceWindowsAuth** が **false** の場合、フォーム認証を続行できます。
  
以下の **ASMXLogon_MultiAuth** サンプルを使用するには、コンソール アプリケーションを作成し、「[アプリケーションを作成して Web サービス参照を追加する](#pj15_PrerequisitesASMX_Configure)」の手順に従います。その後、wsdl.LoginWindows.cs プロキシ ファイルと wsdl.Project.cs プロキシ ファイルを追加します。**Main** メソッドによって、**ProjectDerived** クラスの **project** インスタンスが作成されます。サンプルでは派生した **LoginWindowsDerived** クラスを使用して、**project.CookieContainer** プロパティの **CookieContainer** オブジェクトを取得する必要があります。このオブジェクトによって、フォーム認証と Windows 認証が識別されます。その後、**project** オブジェクトを使用して **SvcProject.Project** クラスの任意のメソッドを呼び出すことができます。 
  
> [!NOTE]
> **LoginWindows** サービスは、複数認証環境の ASMX アプリケーションでのみ必要です。**ASMXLogon_MultiAuth** サンプルでは、**GetLogonCookie** メソッドによって **loginWindows** オブジェクトの Cookie が取得されます。**project.CookieContainer** プロパティは **loginWindows.CookieContainer** 値に設定されます。 
  
```cs
using System;
using System.Net;
using PSLibrary = Microsoft.Office.Project.Server.Library;
namespace ASMXLogon_MultiAuth
{
    class Program
    {
        private const string PROJECT_SERVER_URL = 
            "https://ServerName/ProjectServerName/_vti_bin/psi/";
        static void Main(string[] args)
        {
            bool isWindowsUser = true;
            // Create an instance of the project object.
            ProjectDerived project = new ProjectDerived();
            project.Url = PROJECT_SERVER_URL + "Project.asmx";
            project.Credentials = CredentialCache.DefaultCredentials;
            try
            {
                // The program works on a Windows-auth-only computer if you comment-out the
                // following line. The line is required for multiple authentication.
                project.CookieContainer = GetLogonCookie();
                project.EnforceWindowsAuth = isWindowsUser;
                // Get a list of all published projects. 
                // Use ReadProjectStatus instead of ReadProjectList,
                // because the permission requirements are lower.
                SvcProject.ProjectDataSet projectDs =
                    project.ReadProjectStatus(Guid.Empty,
                        SvcProject.DataStoreEnum.PublishedStore,
                        string.Empty,
                        (int)PSLibrary.Project.ProjectType.Project);
                Console.WriteLine(string.Format(
                    "There are {0} published projects.", 
                    projectDs.Project.Rows.Count));
            }
            catch (UnauthorizedAccessException ex)
            {
                Console.WriteLine(ex.Message);
            }
            catch (WebException ex)
            {
                Console.WriteLine(ex.Message);
            }
            finally
            {
                Console.Write("Press any key to continue...");
                Console.ReadKey(false);
            }
        }
        private static CookieContainer GetLogonCookie()
        {
            // Create an instance of the loginWindows object.
            LoginWindowsDerived loginWindows = new LoginWindowsDerived();
            loginWindows.EnforceWindowsAuth = true;
            loginWindows.Url = PROJECT_SERVER_URL + "LoginWindows.asmx";
            loginWindows.Credentials = CredentialCache.DefaultCredentials;
            loginWindows.CookieContainer = new CookieContainer();
            if (!loginWindows.Login())
            {
                // Login failed; throw an exception.
                throw new UnauthorizedAccessException("Login failed.");
            }
            return loginWindows.CookieContainer;
        }
    }
    // Derive from LoginWindows class; include additional property and 
    // override the web request header.
    class LoginWindowsDerived : SvcLoginWindows.LoginWindows
    {
        public bool EnforceWindowsAuth { get; set; }
        protected override WebRequest GetWebRequest(Uri uri)
        {
            WebRequest request = base.GetWebRequest(uri);
            if (this.EnforceWindowsAuth)
            {
                request.Headers.Add("X-FORMS_BASED_AUTH_ACCEPTED", "f");
            }
            return request;
        }
    }
    // Derive from Project class; include additional property and 
    // override the web request header.
    class ProjectDerived : SvcProject.Project
    {
        public bool EnforceWindowsAuth { get; set; }
        protected override WebRequest GetWebRequest(Uri uri)
        {
            WebRequest request = base.GetWebRequest(uri);
            if (this.EnforceWindowsAuth)
            {
                request.Headers.Add("X-FORMS_BASED_AUTH_ACCEPTED", "f");
            }
            return request;
        }
    }
}
```

派生した **LoginWindows** クラスを使用して、フォーム認証を無効化する Web 要求ヘッダーを持つ PSI 呼び出しを行うことは、複数認証環境で実行されるアプリケーションでは必須です。Project Server がクレーム認証のみを使用している場合は、Web 要求ヘッダーを追加するクラスを派生させる必要はありません。前に示した例は両方の環境で動作します。 
  
WCF ベース アプリケーションについては、別の方法で対処します。 詳細については、「Wcf ベースのコード サンプルの前提条件」の「複数認証を使用する」を参照[Project。](prerequisites-for-wcf-based-code-samples-in-project.md)
  
## <a name="changing-the-values-of-generic-constants"></a>一般的な定数の値を変更する
<a name="pj15_PrerequisitesASMX_ChangeValues"> </a>

大部分のサンプルには、サンプルが環境で正しく動作するために更新する必要がある 1 つ以上の変数があります。 次の例では、SSL がインストールされている場合に HTTP プロトコルではなく HTTPS プロトコルを使用します。 _ServerName を_ 使用しているサーバーの名前に置き換える。 _ProjectServerName を_ サーバー サイトの仮想ディレクトリProject置き換PWA。 
  
```cs
const string PROJECT_SERVER_URI = "https://ServerName/ProjectServerName/";
```

変更する必要があるその他の変数または必要条件は、コード サンプルの上部に記載されています。
  
## <a name="verifying-the-results"></a>結果を確認する
<a name="pj15_PrerequisitesASMX_Verify"> </a>

コード サンプルの結果の取得と解釈は、必ずしも簡単ではありません。 たとえば、プロジェクトを作成する場合は、プロジェクトがプロジェクトの [センター] ページに表示される前にProject発行するProject Web App。
  
コード サンプルの結果は、いくつかの方法で確認できます。たとえば、次のような方法があります。
  
- 2013 Project Professional 2013 クライアントを使用して、Project サーバー コンピューターからプロジェクトを開き、必要なアイテムを表示します。
    
- 発行済みプロジェクトは、Project ( ) の [センター] ページProject Web App表示 `https://ServerName/ProjectServerName/projects.aspx` します。
    
- [キュー ログ] を表示Project Web App。 [サーバーの設定] ページを開き (右上隅にある **[設定]** アイコンを選択し、[個人用のジョブ] セクション ( ) の [マイ キューに入っているジョブ]**を設定** します `https://ServerName/ProjectServerName/MyJobs.aspx` 。 [**表示**] ドロップダウン リストでは、ジョブの状態による並べ替えができます。 既定の状態は [**進行中または失敗した過去 1 週間のジョブ**] です。 
    
- すべてのキュー ジョブ設定をProject Web App、エンタープライズ オブジェクトの削除または強制チェックインを行う場合は、() の [サーバー サーバー] `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx` ページを使用します。 [サーバー設定] ページのこれらのリンクにアクセスするには、管理権限が必要です。
    
- **Microsoft SQL Server Management Studio** を使用して Project データベース内のテーブルに対するクエリを実行します。たとえば、次のクエリを使用して、pub.MSP_WORKFLOW_STAGE_PDPS テーブルの先頭から 200 行を選択し、ワークフロー ステージにプロジェクト詳細ページ (PDP) についての情報を表示します。 
    
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
<a name="pj15_PrerequisitesASMX_Cleanup"> </a>

いくつかのコード サンプルをテストすると、エンタープライズ オブジェクトおよび設定の削除や再設定が必要になります。 エンタープライズ データ () を管理設定サーバー Project Web Appページを使用できます `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx` 。 [サーバー設定] ページにあるリンクを使用して、古いアイテムを削除したり、チェックインを強制したり、すべてのユーザーのジョブ キューを管理したり、その他の管理タスクを実行したりできます。
  
[サーバー設定] ページに表示されるリンクの一部を以下に示します。これらは、コード サンプルを実行した後に一般的なクリーンアップの操作を行うために使用できます。
  
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
<a name="pj15_PrerequisitesASMX_AR"> </a>

- [プロジェクト内のWCFベースコードサンプルの前提条件](prerequisites-for-wcf-based-code-samples-in-project.md)
- [WCF で偽装を使用する](https://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)
- [Project PSI リファレンスの概要](project-psi-reference-overview.md)
- [SharePoint デベロッパー センター](https://msdn.microsoft.com/sharepoint/default.aspx)
    

