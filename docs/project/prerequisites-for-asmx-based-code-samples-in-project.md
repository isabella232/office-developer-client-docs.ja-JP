---
title: プロジェクト内の ASMX ベースのコード サンプルの前提条件
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
- サンプル コード、プログラミングでは、PSI、PSI、コード サンプルをコンパイルする project server がプロジェクトのサーバー プログラミング
localization_priority: Normal
ms.assetid: df584b25-4460-46c8-89a8-3b2c94d20bba
description: プロジェクト Server インターフェイス (PSI) のリファレンス トピックに含まれている ASMX ベースのコード サンプルを使用して Visual Studio でプロジェクトを作成するための情報について説明します。
ms.openlocfilehash: 73d097211dc3c68e1066c2ea1ad8d51a616184d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804689"
---
# <a name="prerequisites-for-asmx-based-code-samples-in-project"></a>プロジェクト内の ASMX ベースのコード サンプルの前提条件

プロジェクト Server インターフェイス (PSI) のリファレンス トピックに含まれている ASMX ベースのコード サンプルを使用して Visual Studio でプロジェクトを作成するための情報について説明します。
  
[Project Server 2013 のクラス ライブラリと web サービスを参照](http://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx)するに含まれているコード サンプルの多くは、Office プロジェクト 2007 SDK で作成され、ASMX web サービスの標準的な形式を使用します。 まだサンプルは、Project Server 2013 での作業し、コンソール アプリケーションにコピーし、完全な単位として実行するように設計されています。 サンプルで例外が記載されています。 
  
Project 2013 SDK の新しい PSI のサンプルは、Windows Communication Foundation (WCF) サービスを使用する形式に準拠しています。 ASMX ベースのサンプルは、WCF サービスの使用に適合させることができます。 この資料では、ASMX web サービスのサンプルを使用する方法を示します。 サンプルの WCF サービスの使用方法の詳細については、[プロジェクト内の WCF ベースのコード サンプルの前提条件](prerequisites-for-wcf-based-code-samples-in-project.md)を参照してください。
  
> [!NOTE]
> PSI の ASMX web サービスのインタ フェースは、Project Server 2013 のでは使用されなくなりましたはまだサポートされています。 クライアント側オブジェクト モデル (CSOM) では、アプリケーションを必要とするメソッドが含まれている場合、CSOM で新しいアプリケーションを開発する必要があります。 CSOM は、プロジェクトのオンラインまたは Project Server 2013 のオンプレミス インストールを操作するアプリケーションを有効にします。 それ以外の場合、アプリケーションは、PSI を使用する場合は、WCF インターフェイスは、ネットワーク通信のことをお勧めする技術であるを使用してください。 ASMX インターフェイスまたは WCF インターフェイスを使用するアプリケーションは、Project Server 2013 のオンプレミスのインストールでのみ操作できます。 CSOM の詳細については、 [Project Server 2013 のアーキテクチャ](project-server-2013-architecture.md)および[Project 2013 のクライアント側オブジェクト モデル (CSOM)](client-side-object-model-csom-for-project-2013.md)を参照してください。 
  
コード サンプルを実行する前には、開発環境を設定し、アプリケーションを構成し、環境に一致するように一般的な定数の値を変更する必要があります。
  
## <a name="setting-up-the-development-environment"></a>開発環境を設定する
<a name="pj15_PrerequisitesASMX_Setup"> </a>

1. **テスト プロジェクトのサーバー システムを設定**します。
    
   開発やテストを行う際には常にテスト Project Server システムを使用します。たとえコードが完全に動作しても、プロジェクト間の依存関係、レポート、またはその他の環境要因が意図しない結果を引き起こす可能性があります。 
    
   > [!NOTE]
   > 確認して、サーバー上の有効なユーザーは、PSI の呼び出し、アプリケーションを使用するための十分なアクセス許可があることを確認します。 各 PSI メソッドのリファレンス トピックには、プロジェクトのサーバーのアクセス許可のテーブルが含まれています。 などの[Project.QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx)メソッドには、**新しいプロジェクト**グローバル アクセス権と、 **SaveProjectTemplate**アクセス許可が必要です。 
  
   場合によっては、サーバー上でリモート デバッグを実行する必要があります。 SharePoint ファーム内の各プロジェクトのサーバー コンピューター上のイベント ハンドラー アセンブリをインストールして、一般に、プロジェクトのサーバーの設定] ページを使用して、Project Web App インスタンスのイベント ハンドラーを構成して、イベント ハンドラーを設定する必要がありますもSharePoint サーバーの管理のアプリケーションの設定です。
    
2. **開発用コンピューターを設定します。**
    
   通常、PSI にはネットワーク経由でアクセスします。コード サンプルは、記載されている場合を除き、サーバーから分離されたクライアントで動作するように作られています。
    
   1. **Visual Studio の適切なバージョンをインストールします。** 場合を除き、これらのコードが書き込まれます Visual C# で。 Visual Studio 2010 または Visual Studio 2012 では、それらを使用できます。 最新のサービス パックのインストールがあることを確認します。 
        
   2. **プロジェクト サーバー Dll を開発用コンピューターにコピーします。** 次のアセンブリをコピーする`[Program Files]\Microsoft Office Servers\15.0\Bin`開発用コンピューターに Project Server コンピューターにします。 
        
      - Microsoft.Office.Project.Server.Events.Receivers.dll
      - Microsoft.Office.Project.Server.Library.dll
        
   3. コンパイルし、PSI の ASMX web サービスの ProjectServerServices.dll のプロキシ アセンブリを使用する方法の詳細については、 [PSI プロキシ アセンブリおよび IntelliSense の説明を使用して](#pj15_PrerequisitesASMX_BuildingProxy)参照してください。
    
3. **IntelliSense ファイルをインストールします。**
    
    Project 2013 SDK から更新された IntelliSense XML ファイルは、コピーである Project Server アセンブリのクラスとメンバーの IntelliSense の説明を使用するには、Project Server アセンブリが配置されている同じディレクトリにダウンロードします。 たとえば、アプリケーションが Microsoft.Office.Project.Server.Library.dll アセンブリへの参照に設定されているディレクトリに Microsoft.Office.Project.Server.Library.xml ファイルをコピーします。
    
    PSI web サービス用の IntelliSense の説明で CompileASMXProxyAssembly.cmd スクリプトを使用して、PSI プロキシ アセンブリを作成することを必要とする、 `Documentation\IntelliSense\WSDL` Project 2013 SDK ダウンロードのサブディレクトリです。 スクリプトは、ProjectServerServices.dll の ASMX ベースのプロキシ アセンブリを作成します。 詳細については、SDK ダウンロードの [ReadMe_IntelliSense] ファイルを参照してください。 
    
## <a name="creating-the-application-and-adding-a-web-service-reference"></a>アプリケーションを作成して Web サービス参照を追加する
<a name="pj15_PrerequisitesASMX_Configure"> </a>

1. **コンソール アプリケーションを作成します**。
    
   **[新しいプロジェクト**] ダイアログ ボックスのドロップダウン ボックスの一覧で、コンソール アプリケーションを作成するときは、 **.NET Framework 4**を選択します。 新しいアプリケーションには、PSI のコード例をコピーできます。
    
2. **Asmx サービスに必要な参照を追加します。**
    
   ソリューション エクスプ ローラーで、 **System.Web.Services**への参照を追加します (図 1 を参照してください)。 
    
   **図 1 です。Visual Studio で参照を追加します。**

   ![Visual Studio で参照を追加します。](media/pj15_PrerequisitesASMX_AddReference.gif "Visual Studio で参照を追加します。")
  
3. **コードをコピー**します。
    
   コード サンプル全体をコンソール アプリケーションの Program.cs ファイルにコピーします。
    
4. **サンプル アプリケーションの名前空間を設定**します。
    
   サンプルの上部に記されている名前空間をアプリケーションの既定の名前空間に変更するか、アプリケーションの既定の名前空間をサンプルに合わせて変更することができます。アプリケーションの既定の名前空間は、アプリケーションのプロパティを変更することによって変更できます。
    
   たとえば、 [QueueRenameProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueRenameProject.aspx)のコード サンプルは、 **Microsoft.SDK.Project.Samples.RenameProject**名前空間を持っています。 Visual Studio プロジェクトの名前が**RenameProject**の場合は、Program.cs ファイルから名前空間をコピーし、プロジェクト**のプロパティ**] ウィンドウを開きます ( **[プロジェクト**] メニューで、 **RenameProject のプロパティ**] をクリックすると)。 [**アプリケーション**] タブで、名前空間を**既定の名前空間**] テキスト ボックスにコピーします。 
    
5. **Web 参照を設定**します。
    
   多くの例では、1 つ以上の PSI Web サービスへの参照が必要です。これらは、サンプル自体、またはサンプルの前にあるコメントに示されています。Web 参照の適切な名前空間を取得するには、最初にアプリケーションの既定の名前空間を設定する必要があります。
    
   PSI の ASMX Web サービス参照を追加する方法として次の 3 つがあります。
    
   - という名前の ProjectServerServices.dll、PSI プロキシ アセンブリをビルドし、アセンブリへの参照を設定します。 IntelliSense を取得するには、これは、PSI の参照を追加するのには推奨される方法です。 [PSI プロキシ アセンブリおよび IntelliSense の説明を使用して](#pj15_PrerequisitesASMX_BuildingProxy)参照してください。
    
   - Wsdl.exe 出力からプロキシ ファイルを Visual Studio ソリューションに追加します。 [PSI プロキシ ファイルを追加する](#pj15_PrerequisitesASMX_AddingProxyFile)を参照してください。
    
   - Web サービス参照を追加するには、Visual Studio を使用します。 [サービス参照の追加、web](#pj15_PrerequisitesASMX_AddingServiceReference)を参照してください。

<a name="pj15_PrerequisitesASMX_BuildingProxy"> </a>

### <a name="using-a-psi-proxy-assembly-and-intellisense-descriptions"></a>Intellisense の説明を備えた PSI プロキシ アセンブリを使用する

ビルドしてで CompileASMXProxyAssembly.cmd スクリプトを使用して、PSI の ASMX ベース web サービスをすべての ProjectServerServices.dll のプロキシ アセンブリを使用して、 `Documentation\IntelliSense\WSDL` Project 2013 SDK ダウンロードのフォルダーです。 ダウンロードへのリンクでは、 [Project 2013 開発者向けドキュメント](project-2013-developer-documentation.md)を参照してください。
  
> [!NOTE]
> Source.zip からプロキシ ソース ファイルを抽出するときにファイル内のファイル、`Documentation\IntelliSense\WSDL\Source`は、Project 2013 SDK ダウンロードの発行日時点で現在のフォルダーです。 生成するには、PSI プロキシ ソース ファイルは、Project Server コンピューター上の GenASMXProxyAssembly.cmd スクリプトの実行を更新しました。 内のスクリプト、`Documentation\IntelliSense\WCF`フォルダーは、ASMX ベースのアプリケーションでは機能しません。 GenWCFProxyAssembly.cmd スクリプトでは、WCF サービスのソース コード ファイルを生成する、SvcUtil.exe を呼び出します。 WCF プロキシ ファイルには、さまざまな属性、チャネル ・ インタ フェース、および各 PSI サービス用のクライアント クラスが含まれます。 たとえば、WCF ベースのリソースのサービスには、 **ResourceChannel**インターフェイス、**リソース**インターフェイス、および**ResourceClient**のクラスが含まれています。 リソースの ASMX ベース web には、いくつかの異なるプロパティを使用して**リソース**クラスが含まれています。 
  
次に、GenASMXProxyAssembly.cmd スクリプトを示します。このスクリプトは、PSI Web サービスの WSDL 出力ファイルを生成した後、アセンブリをコンパイルします。
  
```MS-DOS
@echo off
@ECHO ---------------------------------------------------
@ECHO Creating C# files for the ASMX-based proxy assembly
@ECHO ---------------------------------------------------
REM Replace ServerName with the name of the server and 
REM the instance name of Project Web App. Do not use localhost.
(set VDIR=http://ServerName/pwa/_vti_bin/psi)
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
  
ASMX web サービスと WCF サービスの両方のスクリプトが作成した任意の名前空間は、どちらかのアセンブリの IntelliSense の ProjectServerServices.xml ファイルが機能するようにします。 ASMX ベースのプロキシ アセンブリの WCF ベースのプロキシ アセンブリ内のリソース サービスの名前空間は**SvcResource**です。 名前空間の名前を変更することができます、もちろん、-プロキシ アセンブリおよび IntelliSense の ProjectServerServices.xml ファイルに一致しているかどうかを確認します。
  
コード サンプルでは、PSI web サービスの名前空間に別の名前を使用する場合など**ProjectWebSvc**IntelliSense を実行するには、名前空間がプロキシ アセンブリと一致するように**SvcProject**を使用するサンプルを変更しなければなりません。 
  
ASMX ベースのプロキシ アセンブリを使用する利点は、すべて PSI web サービス名前空間が含まれています。複数の web 参照を作成する必要はありません。 別の利点としては、ProjectServerServices.dll プロキシ アセンブリへの参照を設定するのと同じディレクトリに ProjectServerServices.xml ファイルを追加する場合ことができます IntelliSense の説明、PSI のクラスおよびメンバーの。 図 2 は、 **Project.QueueCreateProject**メソッドの IntelliSense のテキストを示します。 詳細については、Project 2013 SDK ダウンロードの [IntelliSense] フォルダーで [ReadMe_IntelliSense] ファイルを参照してください。 
  
**図 2 になります。プロジェクトの web サービスのメソッドの IntelliSense を使用します。**

![PSI サービスのメソッドの Intellisense を使用します。](media/pj15_PrerequisitesASMX_Intellisense.gif "PSI サービスのメソッドの Intellisense を使用します。")
  
このプロキシ アセンブリを使用する場合の欠点は、ソリューションが大規模になることと、ソリューションと共にプロキシ アセンブリの配布とインストールが必要になることです。また、プロキシ アセンブリ内と IntelliSense ファイル内で同じ名前空間を使用する必要があります (ただし、スクリプトと ProjectServerServices.xml IntelliSense ファイルを変更して、別々の名前空間を使用するようにした場合は例外です)。
  
### <a name="adding-a-psi-proxy-file"></a>PSI プロキシ ファイルを追加する
<a name="pj15_PrerequisitesASMX_AddingProxyFile"> </a>

Project 2013 SDK ダウンロードには、プロキシ アセンブリに対して Wsdl.exe コマンドによって生成されるソース ファイルが含まれています。 Source.zip 内では、ソース ファイル、`Documentation\IntelliSense\ASMX`のサブディレクトリです。 プロキシ アセンブリへの参照を設定する代わりに、Visual Studio のソリューションに 1 つまたは複数のソース ファイルを追加できます。 たとえば、GenASMXProxyAssembly.cmd スクリプトを実行すると、wsdl を追加します。ソリューションのファイルを Project.cs。 スクリプトを実行するには、代わりに、たとえば、単一のソース ファイルを生成する次のコマンドを実行できます。 
  
```MS-DOS
set VDIR=http://ServerName/ProjectServerName/_vti_bin/psi
set WSDL="C:\Program Files (x86)\Microsoft SDKs\Windows\v7.0A\Bin\x64\wsdl.exe"
%WSDL% /nologo /l:cs /namespace:SvcProject /out:wsdl.Project.cs %VDIR%/Project.asmx?wsdl
```

クラス変数名の**プロジェクト**として、**プロジェクト**のオブジェクトを定義するには、次のコードを使用します。 **AddContextInfo**メソッドでは、Windows 認証とフォーム ベース認証の**プロジェクト**のオブジェクトにコンテキスト情報を追加します。 
  
```cs
private static SvcProject.Project project;
private static SvcLoginForms.LoginForms loginForms =
            new SvcLoginForms.LoginForms();
. . .
public void AddContextInfo()
{
    // Add the Url property.
    project.Url = "http://ServerName /ProjectServerName /_vti_bin/psi/project.asmx";
    // Add Windows credentials.
    project.Credentials = CredentialCache.DefaultCredentials;
    // If Forms authentication is used, add the Project Server cookie.
    project.CookieContainer = loginForms.CookieContainer;
}
```

> [!NOTE]
> PSI プロキシ アセンブリを使用した場合、または**SvcProject**という名前のプロジェクトの [サービス参照のプロキシ ファイルを追加するかどうかは、**プロジェクト**のオブジェクトを作成するのには同じコードを使用します。 
  
### <a name="adding-a-web-service-reference"></a>Web サービス参照を追加する
<a name="pj15_PrerequisitesASMX_AddingServiceReference"> </a>

ASMX ベースのプロキシ アセンブリを使用したり、WSDL 出力ファイルを追加しない、する場合は、1 つまたは複数の個別の web 参照を設定できます。 次の手順では、Visual Studio 2012 を使用して web 参照を設定する方法を示します。
  
1. **ソリューション エクスプ ローラー**で、[**参照**] フォルダーを右クリックし、し、[**サービス参照の追加**」を選択します。 
    
2. **サービス参照の追加**] ダイアログ ボックスで、[**詳細設定**を選択します。
    
3. **[サービス参照設定**] ダイアログ ボックスで、[ **Web 参照の追加**を選択します。
    
4. [ **URL** ] テキスト ボックスに入力`http:// _ServerName_/ _ProjectServerName_/_vti_bin/psi/ _ServiceName_.asmx?wsdl`、および**Enter**キーを押してまたは、[**移動**] アイコンを選択します。 Secure Sockets Layer (SSL) がインストールされている場合は、HTTP プロトコルではなく HTTPS プロトコルを使用する必要があります。 

   たとえば、プロジェクト サービスの次の URL を使用して、上の`http://MyServer/pwa`の Project Web App サイト。`http://MyServer/pwa/_vti_bin/psi/project.asmx?wsdl`
    
   Web ブラウザーを開き、またはに移動`http://ServerName/ProjectServerName/_vti_bin/psi/ServiceName.asmx?wsdl`。 ファイルをローカル ディレクトリでは、次のように`C:\Project\WebServices\ServiceName.wsdl`。 **Web 参照の追加**] ダイアログ ボックスで、 **URL**のファイルのプロトコルとファイルへのパスを入力します。 たとえば、 `file://C:\Project\WebServices\Project.wsdl`。 
    
5. 参照が解決した後は、 **Web 参照名**] テキスト ボックスに参照名を入力します。 Project 2013 開発者向けドキュメントのコード例では、 **Svc _ServiceName_** の任意の標準的な参照名を使用します。 **SvcProject**の名前は、プロジェクトの web サービス (図 3 を参照してください)。 
    
   **図 3 です。ASMX web サービスの参照を追加します。**

   ![ASMX web サービスの参照を追加します。](media/pj15_PrerequisitesASMX_AddWebSvcReference.gif "ASMX web サービスの参照を追加します。")
  
Project Server コンピューター上で実行する必要があります、偽装を使用して、またはあるアプリケーション コンポーネントの管理者特権のアクセス許可は、ASMX web 参照の代わりに WCF サービス参照を使用します。 詳細については、[プロジェクト内の WCF ベースのコード サンプルの前提条件](prerequisites-for-wcf-based-code-samples-in-project.md)を参照してください。
  
## <a name="setting-other-references"></a>その他の参照を設定する
<a name="pj15_PrerequisitesASMX_OtherReferences"> </a>

プロジェクトのサーバー アプリケーションは、多くの場合、SharePoint Server 2013 web サービスなどのサービスを使用します。 その他のサービスが必要な場合は、例に記載されています。
  
コード サンプルのローカル参照は、サンプルの上部にある**using**ステートメントのとおりです。 
  
1. **ソリューション エクスプ ローラー**で、[**参照**] フォルダーを右クリックし、**参照の追加**を選択し、
    
2. **[参照**] を選択し、以前にコピーしたプロジェクトのサーバー Dll を格納する場所を参照します。 Dll する必要がある、し、[ **ok]** を選択します。
    
> [!NOTE]
> 開発用コンピューター上のアセンブリのバージョンがターゲット Project Server コンピューターのものと厳密に一致していることを確認します。 
  
## <a name="using-multiple-authentication"></a>複数の認証を使用する
<a name="pj15_PrerequisitesASMX_ClaimsMultiAuth"> </a>

Windows 認証またはフォーム認証では、オンプレミスの Project Server のユーザーの認証はクレーム処理では、SharePoint Server 2013 によって行われます。 複数の認証では、Project Web App が提供されている web アプリケーションが Windows 認証とフォーム ベース認証の両方をサポートしていることを意味します。 場合は、請求処理は、ユーザーの認証の種類を判断できないために次のエラーでは、Windows 認証を使用する ASMX web サービスへの呼び出しが失敗します。
  
`The server was unable to process the request due to an internal error. . . .`

ASMX の問題が解決するのには、各 PSI web サービスに対して定義されている派生クラスに PSI メソッドへのすべての呼び出しがあります。 派生クラスは、派生の PSI サービス クラスの cookie を取得するのに**SvcLoginWindows.LoginWindows**クラスを使用する必要がありますもします。 次の例では、 **ProjectDerived**クラスは、 **SvcProject.Project**クラスから派生します。 **プロジェクト**のクラスのメソッドを呼び出すたびに web 要求ヘッダーをオーバーライドし、派生クラスの**EnforceWindowsAuth**プロパティを追加します。 **EnforceWindowsAuth**プロパティが**true**の場合は、 **GetWebRequest**メソッドは、フォーム認証を無効にするヘッダーを追加します。 **EnforceWindowsAuth**が**false**の場合は、フォーム認証を続行できます。
  
次の**ASMXLogon_MultiAuth**サンプルを使用するには、コンソール アプリケーションを作成、手順を実行は[、アプリケーションを作成し web サービス参照の追加](#pj15_PrerequisitesASMX_Configure)、および wsdl を追加し。LoginWindows.cs プロキシ ファイルと wsdl です。プロキシ ファイルを Project.cs。 **Main**メソッドでは、 **ProjectDerived**クラスの**プロジェクト**のインスタンスを作成します。 サンプルでは、**プロジェクトの**CookieContainer**オブジェクトを取得するのに**LoginWindowsDerived**クラスを派生を使用する必要があります。CookieContainer**プロパティで、Windows 認証とフォーム認証を区別します。 **プロジェクト**のオブジェクトは、 **SvcProject.Project**クラスの任意のメソッドへの呼び出しに使用できます。 
  
> [!NOTE]
> **LoginWindows**サービスは、複数認証環境でのアプリケーションの asmx サービスに対してのみ必要です。 サンプルでは、 **ASMXLogon_MultiAuth** 、 **GetLogonCookie**メソッドは、 **loginWindows**オブジェクトの cookie を取得します。 **プロジェクトです。CookieContainer** **loginWindows.CookieContainer**の値にプロパティを設定します。 
  
```cs
using System;
using System.Net;
using PSLibrary = Microsoft.Office.Project.Server.Library;
namespace ASMXLogon_MultiAuth
{
    class Program
    {
        private const string PROJECT_SERVER_URL = 
            "http://ServerName/ProjectServerName/_vti_bin/psi/";
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

派生**LoginWindows**クラスを使用して、フォーム認証を無効にする web 要求ヘッダーの PSI 呼び出しを行うには、複数認証環境で実行されるアプリケーションに必要です。 Project Server では、クレーム認証のみを使用する場合は、web 要求のヘッダーを追加するクラスを派生させる必要はありません。 前の例は、両方の環境で実行されます。 
  
WCF ベースのアプリケーション用の修正プログラムは、異なります。 詳細については、[プロジェクト内の WCF ベースのコード サンプルの前提条件](prerequisites-for-wcf-based-code-samples-in-project.md)で*複数の認証を使用して*セクションを参照してください。
  
## <a name="changing-the-values-of-generic-constants"></a>一般的な定数の値を変更する
<a name="pj15_PrerequisitesASMX_ChangeValues"> </a>

ほとんどのサンプルでは、更新する必要が、サンプルを動作させるため正しく、環境内の 1 つまたは複数の変数があります。 次の例では、SSL がインストールされている場合は HTTP プロトコルではなく HTTPS プロトコルを使用します。 _サーバー名_を使用しているサーバーの名前に置き換えます。 _ProjectServerName_を PWA など、Project Server サイトの仮想ディレクトリ名に置き換えます。 
  
```cs
const string PROJECT_SERVER_URI = "http://ServerName/ProjectServerName/";
```

変更する必要があるその他の変数または必要条件は、コード サンプルの上部に記載されています。
  
## <a name="verifying-the-results"></a>結果を確認する
<a name="pj15_PrerequisitesASMX_Verify"> </a>

取得し、コード サンプルの結果を解釈する常に簡単ではありません。 たとえば、プロジェクトを作成する場合は、Project Web App の [プロジェクト センター] ページに表示するプロジェクトを発行する必要があります。
  
コード サンプルの結果は、いくつかの方法で確認できます。たとえば、次のような方法があります。
  
- プロジェクト評価のためのクライアントを使用して、Project Server コンピューターからプロジェクトを開くし、目的のアイテムを表示します。
    
- Project Web App の [プロジェクト センター] ページで発行されたプロジェクトを表示する ( `http://ServerName/ProjectServerName/projects.aspx`)。
    
- Project Web App では、キューのログを表示します。 サーバー設定] ページを開く (右上隅で、[**設定**] アイコンを選択します)、**個人用の設定**] セクションで [**自分のキュー ジョブ**を選択し、( `http://ServerName/ProjectServerName/MyJobs.aspx`)。 **ビュー** 」ドロップ ダウン リストで、ジョブの状態で並べ替えることができます。 既定の状態が**進行中で過去 1 週間のジョブの失敗です**。 
    
- Project Web App の [サーバー設定] ページを使用して ( `http://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`) とすべてのキュー ジョブの管理、削除、またはチェックインのエンタープライズ オブジェクトを強制的にします。 [サーバーの設定] ページで、これらのリンクにアクセスする管理者の権限がある必要があります。
    
- **Microsoft SQL Server Management Studio の**を使用して、プロジェクト データベース内のテーブルに対してクエリを実行します。 たとえば、pub の上位 200 行を選択するのには次のクエリを使用します。ワークフロー ステージの詳細ページ (Pdp) のプロジェクトに関する情報を表示するのには MSP_WORKFLOW_STAGE_PDPS テーブルです。 
    
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
<a name="pj15_PrerequisitesASMX_Cleanup"> </a>

一部のコード サンプルをテストした後、エンタープライズ オブジェクトと設定を削除またはリセットする必要があります。 Project Web App の [サーバー設定] ページを使用するにはエンタープライズ ・ データを管理する ( `http://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`)。 [サーバー設定] ページのリンクを使用すると、古いアイテムを削除する、強制的にチェックインのプロジェクト、すべてのユーザーのジョブ キューの管理、その他の管理タスクを実行できます。
  
[サーバー設定] ページに表示されるリンクの一部を以下に示します。これらは、コード サンプルを実行した後に一般的なクリーンアップの操作を行うために使用できます。
  
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
<a name="pj15_PrerequisitesASMX_AR"> </a>

- [プロジェクト内の WCF ベースのコード サンプルの前提条件](prerequisites-for-wcf-based-code-samples-in-project.md)
- [WCF で偽装を使用します。](http://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)
- [プロジェクト PSI リファレンスの概要](project-psi-reference-overview.md)
- [SharePoint デベロッパー センター](http://msdn.microsoft.com/en-us/sharepoint/default.aspx)
    

