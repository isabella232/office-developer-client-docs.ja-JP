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
# <a name="prerequisites-for-asmx-based-code-samples-in-project"></a><span data-ttu-id="86ad9-104">プロジェクト内のASMXベースコードサンプルの前提条件</span><span class="sxs-lookup"><span data-stu-id="86ad9-104">Prerequisites for ASMX-based code samples in Project</span></span>

<span data-ttu-id="86ad9-105">Project Server Interface (PSI) リファレンス トピックに含まれる ASMX ベースのコード サンプルを使用して、Visual Studio でプロジェクトを作成するのに役立つ情報について説明します。</span><span class="sxs-lookup"><span data-stu-id="86ad9-105">Learn information to help you create projects in Visual Studio by using the ASMX-based code samples that are included in the Project Server Interface (PSI) reference topics.</span></span>
  
<span data-ttu-id="86ad9-106">[Project Server 2013](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx)クラス ライブラリと Web サービスリファレンスに含まれるコード サンプルの多くは、もともと Office Project 2007 SDK 用に作成され、ASMX Web サービスの標準形式を使用しています。</span><span class="sxs-lookup"><span data-stu-id="86ad9-106">Many of the code samples included in the [Project Server 2013 class library and web service reference](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) were originally created for the Office Project 2007 SDK, and use a standard format for ASMX web services.</span></span> <span data-ttu-id="86ad9-107">サンプルは引き続き Project Server 2013 で動作し、コンソール アプリケーションにコピーされ、完全なユニットとして実行するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="86ad9-107">The samples still work in Project Server 2013 and are designed to be copied into a console application and run as a complete unit.</span></span> <span data-ttu-id="86ad9-108">例外はサンプルに記載されています。</span><span class="sxs-lookup"><span data-stu-id="86ad9-108">Exceptions are noted in the sample.</span></span> 
  
<span data-ttu-id="86ad9-109">2013 SDK Projectの新しい PSI サンプルは、WINDOWS (WCF) サービスを使用する形式に準拠しています。</span><span class="sxs-lookup"><span data-stu-id="86ad9-109">New PSI samples in the Project 2013 SDK conform to a format that uses Windows Communication Foundation (WCF) services.</span></span> <span data-ttu-id="86ad9-110">この ASMX ベースのサンプルは、WCF サービスを使用するように調整することもできます。</span><span class="sxs-lookup"><span data-stu-id="86ad9-110">The ASMX-based samples can also be adapted to use WCF services.</span></span> <span data-ttu-id="86ad9-111">この記事では、ASMX Web サービスでサンプルを使用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="86ad9-111">This article shows how to use the samples with ASMX web services.</span></span> <span data-ttu-id="86ad9-112">WCF サービスでサンプルを使用する方法については、「WCF ベースのコード サンプルの前提条件」を参照[Project。](prerequisites-for-wcf-based-code-samples-in-project.md)</span><span class="sxs-lookup"><span data-stu-id="86ad9-112">For information about using the samples with WCF services, see [Prerequisites for WCF-based code samples in Project](prerequisites-for-wcf-based-code-samples-in-project.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="86ad9-113">PSIのASMX WebサービスインターフェイスはProject Server 2013では非推奨ですが、引き続きサポートされています。</span><span class="sxs-lookup"><span data-stu-id="86ad9-113">The ASMX web service interface of the PSI is deprecated in Project Server 2013, but is still supported.</span></span> <span data-ttu-id="86ad9-114">クライアント側オブジェクト モデル (CSOM) にアプリケーションで必要なメソッドが含まれる場合は、CSOM を使用して新しいアプリケーションを開発する必要があります。</span><span class="sxs-lookup"><span data-stu-id="86ad9-114">If the client-side object model (CSOM) includes the methods that your application requires, new applications should be developed with the CSOM.</span></span> <span data-ttu-id="86ad9-115">CSOM を使用すると、アプリケーションはサーバーサーバー 2013 のProject Onlineまたはオンプレミスインストールで動作Projectできます。</span><span class="sxs-lookup"><span data-stu-id="86ad9-115">The CSOM enables applications to work with Project Online or an on-premises installation of Project Server 2013.</span></span> <span data-ttu-id="86ad9-116">それ以外の場合、アプリケーションで PSI を使用する場合は、ネットワーク通信に推奨されるテクノロジである WCF インターフェイスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="86ad9-116">Otherwise, if your application uses the PSI, it should use the WCF interface, which is the technology that we recommend for network communications.</span></span> <span data-ttu-id="86ad9-117">ASMX インターフェイスまたは WCF インターフェイスを使用するアプリケーションは、サーバー 2013 のオンプレミス インストールProjectできます。</span><span class="sxs-lookup"><span data-stu-id="86ad9-117">Applications that use the ASMX interface or the WCF interface can work only for on-premises installations of Project Server 2013.</span></span> <span data-ttu-id="86ad9-118">CSOM の詳細については[、「Project Server 2013](project-server-2013-architecture.md)アーキテクチャとクライアント側オブジェクト モデル[(CSOM) for Project 2013」を参照](client-side-object-model-csom-for-project-2013.md)してください。</span><span class="sxs-lookup"><span data-stu-id="86ad9-118">For more information about the CSOM, see [Project Server 2013 architecture](project-server-2013-architecture.md) and [Client-side object model (CSOM) for Project 2013](client-side-object-model-csom-for-project-2013.md).</span></span> 
  
<span data-ttu-id="86ad9-119">コード サンプルを実行する前には、開発環境を設定し、アプリケーションを構成し、環境に一致するように一般的な定数の値を変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="86ad9-119">Before running the code samples, you must set up the development environment, configure the application, and change generic constant values to match your environment.</span></span>
  
## <a name="setting-up-the-development-environment"></a><span data-ttu-id="86ad9-120">開発環境を設定する</span><span class="sxs-lookup"><span data-stu-id="86ad9-120">Setting up the development environment</span></span>
<span data-ttu-id="86ad9-121"><a name="pj15_PrerequisitesASMX_Setup"> </a></span><span class="sxs-lookup"><span data-stu-id="86ad9-121"><a name="pj15_PrerequisitesASMX_Setup"> </a></span></span>

1. <span data-ttu-id="86ad9-122">**テスト Project Server システムを設定する**。</span><span class="sxs-lookup"><span data-stu-id="86ad9-122">**Set up a test Project Server system**.</span></span>
    
   <span data-ttu-id="86ad9-p104">開発やテストを行う際には常にテスト Project Server システムを使用します。たとえコードが完全に動作しても、プロジェクト間の依存関係、レポート、またはその他の環境要因が意図しない結果を引き起こす可能性があります。</span><span class="sxs-lookup"><span data-stu-id="86ad9-p104">Use a test Project Server system whenever you are developing or testing. Even when your code works perfectly, interproject dependencies, reporting, or other environmental factors can cause unintended consequences.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="86ad9-125">サーバーの有効なユーザーであり、アプリケーションで使用する PSI 呼び出しのための十分な権限を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="86ad9-125">Ensure that you are a valid user on the server, and check that you have sufficient permissions for the PSI calls that your application uses.</span></span> <span data-ttu-id="86ad9-126">各 PSI メソッドのリファレンス トピックに、Project Server 権限の表があります。</span><span class="sxs-lookup"><span data-stu-id="86ad9-126">The reference topic for each PSI method includes a Project Server Permissions table.</span></span> <span data-ttu-id="86ad9-127">たとえば、次の [Project。QueueCreateProject メソッド](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx)には、**グローバルな NewProject** アクセス許可と **SaveProjectTemplate アクセス許可が必要** です。</span><span class="sxs-lookup"><span data-stu-id="86ad9-127">For example, the [Project.QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) method requires the global **NewProject** permission and the **SaveProjectTemplate** permission.</span></span> 
  
   <span data-ttu-id="86ad9-128">場合によっては、サーバーでのリモート デバッグが必要になることがあります。</span><span class="sxs-lookup"><span data-stu-id="86ad9-128">In some cases, you may have to do remote debugging on the server.</span></span> <span data-ttu-id="86ad9-129">SharePoint ファームの各 Project Server コンピューターにイベント ハンドラー アセンブリをインストールし、SharePoint サーバーの全体管理の全般アプリケーション 設定 の Project Server 設定 ページを使用して Project Web App インスタンスのイベント ハンドラーを構成することで、イベント ハンドラーをセットアップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="86ad9-129">You may also have to set up an event handler by installing an event handler assembly on each Project Server computer in the SharePoint farm, and then configuring the event handler for the Project Web App instance by using the Project Server Settings page in the General Application Settings of SharePoint Central Administration.</span></span>
    
2. <span data-ttu-id="86ad9-130">**開発用コンピューターをセットアップする。**</span><span class="sxs-lookup"><span data-stu-id="86ad9-130">**Set up a development computer.**</span></span>
    
   <span data-ttu-id="86ad9-p107">通常、PSI にはネットワーク経由でアクセスします。コード サンプルは、記載されている場合を除き、サーバーから分離されたクライアントで動作するように作られています。</span><span class="sxs-lookup"><span data-stu-id="86ad9-p107">You usually access the PSI through a network. The code samples are designed to be run on a client that is separate from the server, except where noted.</span></span>
    
   1. <span data-ttu-id="86ad9-133">**適切なバージョンの Visual Studio をインストールする。**</span><span class="sxs-lookup"><span data-stu-id="86ad9-133">**Install the correct version of Visual Studio.**</span></span> <span data-ttu-id="86ad9-134">記載されている場合を除き、コード サンプルは Visual C# で記述されています。</span><span class="sxs-lookup"><span data-stu-id="86ad9-134">Except where noted, the code samples are written in Visual C#.</span></span> <span data-ttu-id="86ad9-135">これらは、2010 年Visual Studio 2012 年Visual Studioできます。</span><span class="sxs-lookup"><span data-stu-id="86ad9-135">They can be used with Visual Studio 2010 or Visual Studio 2012.</span></span> <span data-ttu-id="86ad9-136">最新のサービス パックがインストールされていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="86ad9-136">Ensure that you have the most recent service pack installed.</span></span> 
        
   2. <span data-ttu-id="86ad9-137">**Project Server の DLL を開発用コンピューターにコピーする。**</span><span class="sxs-lookup"><span data-stu-id="86ad9-137">**Copy Project Server DLLs to the development computer.**</span></span> <span data-ttu-id="86ad9-138">サーバー コンピューター上の次の `[Program Files]\Microsoft Office Servers\15.0\Bin` アセンブリProject開発用コンピューターにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86ad9-138">Copy the following assemblies from  `[Program Files]\Microsoft Office Servers\15.0\Bin` on the Project Server computer to the development computer:</span></span> 
        
      - <span data-ttu-id="86ad9-139">Microsoft.Office.Project.Server.Events.Receivers.dll</span><span class="sxs-lookup"><span data-stu-id="86ad9-139">Microsoft.Office.Project.Server.Events.Receivers.dll</span></span>
      - <span data-ttu-id="86ad9-140">Microsoft.Office.Project.Server.Library.dll</span><span class="sxs-lookup"><span data-stu-id="86ad9-140">Microsoft.Office.Project.Server.Library.dll</span></span>
        
   3. <span data-ttu-id="86ad9-141">PSI で ASMX Web サービスの ProjectServerServices.dll プロキシ アセンブリをコンパイルして使用する方法については、「[IntelliSense の説明を備えた PSI プロキシ アセンブリを使用する](#pj15_PrerequisitesASMX_BuildingProxy)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="86ad9-141">For information about how to compile and use the ProjectServerServices.dll proxy assembly for the ASMX web services in the PSI, see [Using a PSI proxy assembly and IntelliSense descriptions](#pj15_PrerequisitesASMX_BuildingProxy).</span></span>
    
3. <span data-ttu-id="86ad9-142">**IntelliSense ファイルをインストールする。**</span><span class="sxs-lookup"><span data-stu-id="86ad9-142">**Install the IntelliSense files.**</span></span>
    
    <span data-ttu-id="86ad9-143">Project Server アセンブリのクラスとメンバーに IntelliSense の説明を使用するには、Project 2013 SDK のダウンロードから更新された IntelliSense XML ファイルを、Project Server アセンブリがある同じディレクトリにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86ad9-143">To use IntelliSense descriptions for classes and members in Project Server assemblies, copy the updated IntelliSense XML files from the Project 2013 SDK download to the same directory where the Project Server assemblies are located.</span></span> <span data-ttu-id="86ad9-144">たとえば、アプリケーションで Microsoft.Office.Project.Server.Library.dll アセンブリへの参照を設定するディレクトリに、Microsoft.Office.Project.Server.Library.xml ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="86ad9-144">For example, copy the Microsoft.Office.Project.Server.Library.xml file to the directory where your application will set a reference to the Microsoft.Office.Project.Server.Library.dll assembly.</span></span>
    
    <span data-ttu-id="86ad9-145">IntelliSense PSI Web サービスの説明では、Project SDK ダウンロードのサブディレクトリで CompileASMXProxyAssembly.cmd スクリプトを使用して PSI プロキシ アセンブリを作成する必要があります。 `Documentation\IntelliSense\WSDL`</span><span class="sxs-lookup"><span data-stu-id="86ad9-145">IntelliSense descriptions for the PSI web services require that you create a PSI proxy assembly by using the CompileASMXProxyAssembly.cmd script in the  `Documentation\IntelliSense\WSDL` subdirectory in the Project 2013 SDK download.</span></span> <span data-ttu-id="86ad9-146">このスクリプトを実行すると、ASMX ベースの ProjectServerServices.dll プロキシ アセンブリが作成されます。</span><span class="sxs-lookup"><span data-stu-id="86ad9-146">The script creates the ASMX-based ProjectServerServices.dll proxy assembly.</span></span> <span data-ttu-id="86ad9-147">詳細については、SDK ダウンロードの [ReadMe_IntelliSense] ファイルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="86ad9-147">For more information, see the [ReadMe_IntelliSense] file in the SDK download.</span></span> 
    
## <a name="creating-the-application-and-adding-a-web-service-reference"></a><span data-ttu-id="86ad9-148">アプリケーションを作成して Web サービス参照を追加する</span><span class="sxs-lookup"><span data-stu-id="86ad9-148">Creating the application and adding a web service reference</span></span>
<span data-ttu-id="86ad9-149"><a name="pj15_PrerequisitesASMX_Configure"> </a></span><span class="sxs-lookup"><span data-stu-id="86ad9-149"><a name="pj15_PrerequisitesASMX_Configure"> </a></span></span>

1. <span data-ttu-id="86ad9-150">**コンソール アプリケーションを作成する**。</span><span class="sxs-lookup"><span data-stu-id="86ad9-150">**Create a console application**.</span></span>
    
   <span data-ttu-id="86ad9-p112">コンソール アプリケーションを作成するには、[**新しいプロジェクト**] ダイアログ ボックスのドロップダウン リストから [**.NET Framework 4**] を選択します。この新しいアプリケーションに PSI サンプル コードをコピーできます。</span><span class="sxs-lookup"><span data-stu-id="86ad9-p112">When you create a console application, in the drop-down list of the **New Project** dialog box, select **.NET Framework 4**. You can copy the PSI example code into the new application.</span></span>
    
2. <span data-ttu-id="86ad9-153">**ASMX に必要な参照を追加する。**</span><span class="sxs-lookup"><span data-stu-id="86ad9-153">**Add the reference required for ASMX.**</span></span>
    
   <span data-ttu-id="86ad9-154">ソリューション エクスプローラーで、**System.Web.Services** への参照を追加します (図 1 を参照)。</span><span class="sxs-lookup"><span data-stu-id="86ad9-154">In Solution Explorer, add a reference to **System.Web.Services** (see Figure 1).</span></span> 
    
   <span data-ttu-id="86ad9-155">**図 1. Visual Studio での参照の追加**</span><span class="sxs-lookup"><span data-stu-id="86ad9-155">**Figure 1. Adding a reference in Visual Studio**</span></span>

   <span data-ttu-id="86ad9-156">![[参照の追加] Visual Studio](media/pj15_PrerequisitesASMX_AddReference.gif "に参照を追加Visual Studio")</span><span class="sxs-lookup"><span data-stu-id="86ad9-156">![Adding a reference in Visual Studio](media/pj15_PrerequisitesASMX_AddReference.gif "Adding a reference in Visual Studio")</span></span>
  
3. <span data-ttu-id="86ad9-157">**コードをコピーする。**</span><span class="sxs-lookup"><span data-stu-id="86ad9-157">**Copy the code**.</span></span>
    
   <span data-ttu-id="86ad9-158">コード サンプル全体をコンソール アプリケーションの Program.cs ファイルにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86ad9-158">Copy the complete code example into the Program.cs file of the console application.</span></span>
    
4. <span data-ttu-id="86ad9-159">**サンプル アプリケーションの名前空間を設定する**。</span><span class="sxs-lookup"><span data-stu-id="86ad9-159">**Set the namespace for the sample application**.</span></span>
    
   <span data-ttu-id="86ad9-p113">サンプルの上部に記されている名前空間をアプリケーションの既定の名前空間に変更するか、アプリケーションの既定の名前空間をサンプルに合わせて変更することができます。アプリケーションの既定の名前空間は、アプリケーションのプロパティを変更することによって変更できます。</span><span class="sxs-lookup"><span data-stu-id="86ad9-p113">You can either change the namespace listed at the top of the sample to the application default namespace, or change the default application namespace to match the sample. You can change the default application namespace by changing the application properties.</span></span>
    
   <span data-ttu-id="86ad9-162">たとえば [、QueueRenameProject のコード サンプルには](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueRenameProject.aspx)**、Microsoft.SDK.Project という名前空間があります。Samples.RenameProject**.</span><span class="sxs-lookup"><span data-stu-id="86ad9-162">For example, the code sample for [QueueRenameProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueRenameProject.aspx) has the namespace **Microsoft.SDK.Project.Samples.RenameProject**.</span></span> <span data-ttu-id="86ad9-163">Visual Studio プロジェクトの名前が **RenameProject** の場合、Program.cs ファイルから名前空間をコピーし、プロジェクトの [**プロパティ**] ウィンドウを表示します ([**プロジェクト**] メニューの [**RenameProject のプロパティ**] を選択)。</span><span class="sxs-lookup"><span data-stu-id="86ad9-163">If the name of the Visual Studio project is **RenameProject**, copy the namespace from the Program.cs file, and then open the project **Properties** pane (on the **Project** menu, choose **RenameProject Properties**).</span></span> <span data-ttu-id="86ad9-164">[**アプリケーション**] タブで、名前空間を [**既定の名前空間**] ボックスにコピーします。</span><span class="sxs-lookup"><span data-stu-id="86ad9-164">On the **Application** tab, copy the namespace into the **Default namespace** text box.</span></span> 
    
5. <span data-ttu-id="86ad9-165">**Web 参照を設定する。**</span><span class="sxs-lookup"><span data-stu-id="86ad9-165">**Set the web references**.</span></span>
    
   <span data-ttu-id="86ad9-p115">多くの例では、1 つ以上の PSI Web サービスへの参照が必要です。これらは、サンプル自体、またはサンプルの前にあるコメントに示されています。Web 参照の適切な名前空間を取得するには、最初にアプリケーションの既定の名前空間を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="86ad9-p115">Most examples require a reference to one or more of the PSI web services. These are listed in the sample itself or in comments that precede the sample. To get the correct namespace of the web references, ensure that you first set the default application namespace.</span></span>
    
   <span data-ttu-id="86ad9-169">PSI の ASMX Web サービス参照を追加する方法として次の 3 つがあります。</span><span class="sxs-lookup"><span data-stu-id="86ad9-169">There are three ways to add an ASMX web service reference for the PSI:</span></span>
    
   - <span data-ttu-id="86ad9-170">ProjectServerServices.dll という名前の PSI プロキシ アセンブリを作成してから、このアセンブリへの参照を設定します。</span><span class="sxs-lookup"><span data-stu-id="86ad9-170">Build a PSI proxy assembly named ProjectServerServices.dll, and then set a reference to the assembly.</span></span> <span data-ttu-id="86ad9-171">IntelliSense を取得するには、これが PSI 参照を追加する方法として推奨される方法です。</span><span class="sxs-lookup"><span data-stu-id="86ad9-171">To get IntelliSense, this is the recommended way to add a PSI reference.</span></span> <span data-ttu-id="86ad9-172">詳細については「[Intellisense の説明を備えた PSI プロキシ アセンブリを使用する](#pj15_PrerequisitesASMX_BuildingProxy)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="86ad9-172">See [Using a PSI proxy assembly and IntelliSense descriptions](#pj15_PrerequisitesASMX_BuildingProxy).</span></span>
    
   - <span data-ttu-id="86ad9-p117">wsdl.exe から出力されるプロキシ ファイルを Visual Studio ソリューションに追加します。 「[PSI プロキシ ファイルを追加する](#pj15_PrerequisitesASMX_AddingProxyFile)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="86ad9-p117">Add a proxy file from the wsdl.exe output to the Visual Studio solution. See [Adding a PSI proxy file](#pj15_PrerequisitesASMX_AddingProxyFile).</span></span>
    
   - <span data-ttu-id="86ad9-p118">Visual Studio を使用して Web サービス参照を追加します。「[Web サービス参照を追加する](#pj15_PrerequisitesASMX_AddingServiceReference)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="86ad9-p118">Add a web service reference by using Visual Studio. See [Adding a web service reference](#pj15_PrerequisitesASMX_AddingServiceReference).</span></span>

<span data-ttu-id="86ad9-177"><a name="pj15_PrerequisitesASMX_BuildingProxy"> </a></span><span class="sxs-lookup"><span data-stu-id="86ad9-177"><a name="pj15_PrerequisitesASMX_BuildingProxy"> </a></span></span>

### <a name="using-a-psi-proxy-assembly-and-intellisense-descriptions"></a><span data-ttu-id="86ad9-178">Intellisense の説明を備えた PSI プロキシ アセンブリを使用する</span><span class="sxs-lookup"><span data-stu-id="86ad9-178">Using a PSI proxy assembly and IntelliSense descriptions</span></span>

<span data-ttu-id="86ad9-179">Project SDK ダウンロードのフォルダーにある CompileASMXProxyAssembly.cmd スクリプトを使用して、PSI 内のすべての ASMX ベースの Web サービスに対して ProjectServerServices.dll プロキシ アセンブリを構築して使用できます。 `Documentation\IntelliSense\WSDL`</span><span class="sxs-lookup"><span data-stu-id="86ad9-179">You can build and use the ProjectServerServices.dll proxy assembly for all ASMX-based web services in the PSI, by using the CompileASMXProxyAssembly.cmd script in the  `Documentation\IntelliSense\WSDL` folder of the Project 2013 SDK download.</span></span> <span data-ttu-id="86ad9-180">ダウンロードへのリンクについては、「Project [2013 開発者向けドキュメント」を参照してください](project-2013-developer-documentation.md)。</span><span class="sxs-lookup"><span data-stu-id="86ad9-180">For a link to the download, see [Project 2013 developer documentation](project-2013-developer-documentation.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="86ad9-181">Source.zip ファイルからプロキシ ソース ファイルを抽出すると、フォルダー内のファイルは、2013 SDK ダウンロードの発行日Project `Documentation\IntelliSense\WSDL\Source` です。</span><span class="sxs-lookup"><span data-stu-id="86ad9-181">When you extract the proxy source files from the Source.zip file, the files in the  `Documentation\IntelliSense\WSDL\Source` folder are current as of the publication date of the Project 2013 SDK download.</span></span> <span data-ttu-id="86ad9-182">更新された PSI プロキシ ソース ファイルを生成するには、Project Server コンピューターで GenASMXProxyAssembly.cmd スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="86ad9-182">To generate updated PSI proxy source files, run the GenASMXProxyAssembly.cmd script on the Project Server computer.</span></span> <span data-ttu-id="86ad9-183">フォルダー内のスクリプト  `Documentation\IntelliSense\WCF` は、ASMX ベースのアプリケーションでは機能しません。</span><span class="sxs-lookup"><span data-stu-id="86ad9-183">The scripts in the  `Documentation\IntelliSense\WCF` folder do not work for ASMX-based applications.</span></span> <span data-ttu-id="86ad9-184">GenWCFProxyAssembly.cmd スクリプトは SvcUtil.exe を呼び出し、それによって WCF サービス用のソース コード ファイルが生成されます。</span><span class="sxs-lookup"><span data-stu-id="86ad9-184">The GenWCFProxyAssembly.cmd script calls SvcUtil.exe, which generates source code files for the WCF services.</span></span> <span data-ttu-id="86ad9-185">WCF プロキシ ファイルには、各 PSI サービス用の別の複数の属性、チャネル インターフェイス、およびクライアント クラスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="86ad9-185">The WCF proxy files include different attributes, the channel interface, and a client class for each PSI service.</span></span> <span data-ttu-id="86ad9-186">たとえば、WCF ベースの Resource サービスには **ResourceChannel** インターフェイス、**Resource** インターフェイス、および **ResourceClient** クラスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="86ad9-186">For example, the WCF-based Resource service includes the **ResourceChannel** interface, the **Resource** interface, and the **ResourceClient** class.</span></span> <span data-ttu-id="86ad9-187">ASMX ベースの Resource Web には **Resource** クラスといくつかの異なるプロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="86ad9-187">The ASMX-based Resource web includes the **Resource** class with some different properties.</span></span> 
  
<span data-ttu-id="86ad9-188">次に、GenASMXProxyAssembly.cmd スクリプトを示します。このスクリプトは、PSI Web サービスの WSDL 出力ファイルを生成した後、アセンブリをコンパイルします。</span><span class="sxs-lookup"><span data-stu-id="86ad9-188">Following is the GenASMXProxyAssembly.cmd script that generates WSDL output files for the PSI web services, and then compiles the assembly.</span></span>
  
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

<span data-ttu-id="86ad9-189">スクリプトは ClassList_asmx.txt ファイルを使用します。このファイルには、サードパーティのデベロッパーが使用できる Web サービスのリストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="86ad9-189">The script uses the ClassList_asmx.txt file, which contains the list of web services that are available for third-party developers.</span></span>
  
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

<span data-ttu-id="86ad9-p121">このスクリプトは ProjectServerServices.dll という名前のアセンブリを作成します。WCF ベースのアセンブリ用の ProjectServerServices.dll と混同しないようにしてください。ProjectServerServices.xml IntelliSense ファイルを使用していずれかのアセンブリの使用を有効にする場合、アセンブリ名は同じです。</span><span class="sxs-lookup"><span data-stu-id="86ad9-p121">The scripts create an assembly named ProjectServerServices.dll. Avoid confusing it with ProjectServerServices.dll for the WCF-based assembly. The assembly names are the same, to enable using either assembly with the ProjectServerServices.xml IntelliSense file.</span></span>
  
<span data-ttu-id="86ad9-p122">ASMX Web サービスと WCF サービスの両方について、スクリプトによって作成される任意の名前空間は同一です。そのため、ProjectServerServices.xml IntelliSense ファイルはどちらのアセンブリでも使用できます。たとえば、WCF ベースのプロキシ アセンブリと ASMX ベースのプロキシ アセンブリ内の Resource サービスの名前空間は、**SvcResource** です。名前空間の名前を変更することもできますが、プロキシ アセンブリ内と ProjectServerServices.xml IntelliSense ファイル内では一致している必要があります。</span><span class="sxs-lookup"><span data-stu-id="86ad9-p122">The arbitrary namespace created by the scripts for both the ASMX web services and the WCF services is the same, so that the ProjectServerServices.xml IntelliSense file works with either assembly. For example, the namespace of the Resource service in the WCF-based proxy assembly and in the ASMX-based proxy assembly is **SvcResource**. You can, of course, change the namespace names—if you ensure that they match in the proxy assembly and in the ProjectServerServices.xml IntelliSense file.</span></span>
  
<span data-ttu-id="86ad9-196">コード サンプルで PSI Web サービス名前空間の異なる名前を使用する場合 (たとえば **ProjectWebSvc**)、IntelliSense が機能するためには、**SvcProject** を使用するようにサンプルを変更し、名前空間がプロキシ アセンブリと一致するようにします。</span><span class="sxs-lookup"><span data-stu-id="86ad9-196">If a code sample uses a different name for a PSI web service namespace, for example **ProjectWebSvc**, for IntelliSense to work you must change the sample to use **SvcProject** so that the namespace matches the proxy assembly.</span></span> 
  
<span data-ttu-id="86ad9-197">ASMX ベースのプロキシ アセンブリを使用する利点は、すべての PSI Web サービス名前空間が含まれるという利点があります。複数の Web 参照を作成する必要はない。</span><span class="sxs-lookup"><span data-stu-id="86ad9-197">An advantage to using the ASMX-based proxy assembly is that it includes all PSI web service namespaces; you do not have to create multiple web references.</span></span> <span data-ttu-id="86ad9-198">もう 1 つの利点は、ProjectServerServices.dll プロキシ アセンブリへの参照を設定する同じディレクトリに ProjectServerServices.xml ファイルを追加すると、PSI クラスとメンバーの IntelliSense の説明を取得できるという利点があります。</span><span class="sxs-lookup"><span data-stu-id="86ad9-198">Another advantage is that, if you add the ProjectServerServices.xml file to the same directory where you set a reference to the ProjectServerServices.dll proxy assembly, you can get IntelliSense descriptions for the PSI classes and members.</span></span> <span data-ttu-id="86ad9-199">図 2 は、IntelliSenseのテキストを **Project。QueueCreateProject** メソッド。</span><span class="sxs-lookup"><span data-stu-id="86ad9-199">Figure 2 shows the IntelliSense text for the **Project.QueueCreateProject** method.</span></span> <span data-ttu-id="86ad9-200">詳細については、2013 SDK ダウンロードの IntelliSense Project フォルダーにある [ReadMe_IntelliSense] ファイルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="86ad9-200">For more information, see the [ReadMe_IntelliSense] file in the IntelliSense folder of the Project 2013 SDK download.</span></span> 
  
<span data-ttu-id="86ad9-201">**図 2. Project Web サービスのメソッドでの IntelliSense の使用**</span><span class="sxs-lookup"><span data-stu-id="86ad9-201">**Figure 2. Using IntelliSense for a method in the Project web service**</span></span>

<span data-ttu-id="86ad9-202">![PSI サービス内のメソッドに Intellisense]を使用する PSI サービス内のメソッドに(media/pj15_PrerequisitesASMX_Intellisense.gif "Intellisense")を使用する</span><span class="sxs-lookup"><span data-stu-id="86ad9-202">![Using Intellisense for a method in a PSI service](media/pj15_PrerequisitesASMX_Intellisense.gif "Using Intellisense for a method in a PSI service")</span></span>
  
<span data-ttu-id="86ad9-p124">このプロキシ アセンブリを使用する場合の欠点は、ソリューションが大規模になることと、ソリューションと共にプロキシ アセンブリの配布とインストールが必要になることです。また、プロキシ アセンブリ内と IntelliSense ファイル内で同じ名前空間を使用する必要があります (ただし、スクリプトと ProjectServerServices.xml IntelliSense ファイルを変更して、別々の名前空間を使用するようにした場合は例外です)。</span><span class="sxs-lookup"><span data-stu-id="86ad9-p124">Disadvantages to using the proxy assembly are that the solution is larger and you must distribute and install the proxy assembly with the solution. You must also use the same namespaces that are in the proxy assembly and IntelliSense files, unless you change the script and ProjectServerServices.xml IntelliSense file to use different namespaces.</span></span>
  
### <a name="adding-a-psi-proxy-file"></a><span data-ttu-id="86ad9-205">PSI プロキシ ファイルを追加する</span><span class="sxs-lookup"><span data-stu-id="86ad9-205">Adding a PSI proxy file</span></span>
<span data-ttu-id="86ad9-206"><a name="pj15_PrerequisitesASMX_AddingProxyFile"> </a></span><span class="sxs-lookup"><span data-stu-id="86ad9-206"><a name="pj15_PrerequisitesASMX_AddingProxyFile"> </a></span></span>

<span data-ttu-id="86ad9-207">2013 Project SDK のダウンロードには、プロキシ アセンブリの Wsdl.exe コマンドによって生成されたソース ファイルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="86ad9-207">The Project 2013 SDK download includes the source files generated by the Wsdl.exe command for the proxy assembly.</span></span> <span data-ttu-id="86ad9-208">ソース ファイルはサブディレクトリSource.zipに  `Documentation\IntelliSense\ASMX` 保存されます。</span><span class="sxs-lookup"><span data-stu-id="86ad9-208">The source files are in Source.zip in the  `Documentation\IntelliSense\ASMX` subdirectory.</span></span> <span data-ttu-id="86ad9-209">プロキシ アセンブリへの参照を設定する代わりに、1 つ以上のソース ファイルを別のソリューションにVisual Studioできます。</span><span class="sxs-lookup"><span data-stu-id="86ad9-209">Instead of setting a reference to the proxy assembly, you can add one or more of the source files to a Visual Studio solution.</span></span> <span data-ttu-id="86ad9-210">たとえば、GenASMXProxyAssembly.cmd スクリプトを実行した後、wsdl を追加します。Project.cs ファイルをソリューションに追加します。</span><span class="sxs-lookup"><span data-stu-id="86ad9-210">For example, after running the GenASMXProxyAssembly.cmd script, add the wsdl.Project.cs file to the solution.</span></span> <span data-ttu-id="86ad9-211">スクリプトを実行する代わりに、次のコマンドを実行して、たとえば 1 つのソース ファイルを生成できます。</span><span class="sxs-lookup"><span data-stu-id="86ad9-211">Instead of running the script, you can run the following commands to generate a single source file, for example:</span></span> 
  
```MS-DOS
set VDIR=https://ServerName/ProjectServerName/_vti_bin/psi
set WSDL="C:\Program Files (x86)\Microsoft SDKs\Windows\v7.0A\Bin\x64\wsdl.exe"
%WSDL% /nologo /l:cs /namespace:SvcProject /out:wsdl.Project.cs %VDIR%/Project.asmx?wsdl
```

<span data-ttu-id="86ad9-p126">**Project** オブジェクトを **project** という名前のクラス変数として定義するには、以下のコードを使用します。**AddContextInfo** メソッドによって、Windows 認証およびフォームベース認証を使用するためのコンテキスト情報が **project** オブジェクトに追加されます。</span><span class="sxs-lookup"><span data-stu-id="86ad9-p126">To define a **Project** object as a class variable named **project**, use the following code. The **AddContextInfo** method adds the context information to the **project** object for Windows authentication and Forms-based authentication.</span></span> 
  
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
> <span data-ttu-id="86ad9-214">PSI プロキシ アセンブリを使用する場合も、プロキシ ファイルを追加して **SvcProject** という名前の Project サービス参照を追加する場合も、同じコードを使用して **project** オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="86ad9-214">Whether you use a PSI proxy assembly or add a proxy file for a Project service reference named **SvcProject**, you would use the same code to create a **project** object.</span></span> 
  
### <a name="adding-a-web-service-reference"></a><span data-ttu-id="86ad9-215">Web サービス参照を追加する</span><span class="sxs-lookup"><span data-stu-id="86ad9-215">Adding a web service reference</span></span>
<span data-ttu-id="86ad9-216"><a name="pj15_PrerequisitesASMX_AddingServiceReference"> </a></span><span class="sxs-lookup"><span data-stu-id="86ad9-216"><a name="pj15_PrerequisitesASMX_AddingServiceReference"> </a></span></span>

<span data-ttu-id="86ad9-217">ASMX ベースのプロキシ アセンブリを使用したり、WSDL 出力ファイルを追加したりしない場合は、1 つ以上の個別 Web 参照を設定できます。</span><span class="sxs-lookup"><span data-stu-id="86ad9-217">If you do not use the ASMX-based proxy assembly or add a WSDL output file, you can set one or more individual web references.</span></span> <span data-ttu-id="86ad9-218">次の手順は、2012 年に Web リファレンスを使用して web 参照をVisual Studioします。</span><span class="sxs-lookup"><span data-stu-id="86ad9-218">The following steps show how to set a web reference by using Visual Studio 2012.</span></span>
  
1. <span data-ttu-id="86ad9-219">**ソリューション エクスプローラー** で、[**参照設定**] フォルダーを右クリックし、[**サービス参照の追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="86ad9-219">In **Solution Explorer**, right-click the **References** folder, and then choose **Add Service Reference**.</span></span> 
    
2. <span data-ttu-id="86ad9-220">[**サービス参照の追加**] ダイアログ ボックスで、[**詳細設定**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="86ad9-220">In the **Add Service Reference** dialog box, choose **Advanced**.</span></span>
    
3. <span data-ttu-id="86ad9-221">[**サービス参照の設定**] ダイアログ ボックスで、[**Web 参照の追加**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="86ad9-221">In the **Service Reference Settings** dialog box, choose **Add Web Reference**.</span></span>
    
4. <span data-ttu-id="86ad9-222">**[URL] テキスト ボックス** に `https:// _ServerName_/ _ProjectServerName_/_vti_bin/psi/ _ServiceName_.asmx?wsdl` 「」と入力し **、Enter** キーを押するか、[移動] アイコン **を選択** します。</span><span class="sxs-lookup"><span data-stu-id="86ad9-222">In the **URL** text box, type `https:// _ServerName_/ _ProjectServerName_/_vti_bin/psi/ _ServiceName_.asmx?wsdl`, and then press **Enter** or choose the **Go** icon.</span></span> <span data-ttu-id="86ad9-223">SSL (SSL) Secure Sockets Layerしている場合は、HTTP プロトコルの代わりに HTTPS プロトコルを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="86ad9-223">If you have Secure Sockets Layer (SSL) installed, you should use the HTTPS protocol instead of the HTTP protocol.</span></span> 

   <span data-ttu-id="86ad9-224">たとえば、次の URL をサイトの Projectサービスに使用して `https://MyServer/pwa` 、Project Web App。`https://MyServer/pwa/_vti_bin/psi/project.asmx?wsdl`</span><span class="sxs-lookup"><span data-stu-id="86ad9-224">For example, use the following URL for the Project service on the  `https://MyServer/pwa` site for Project Web App: `https://MyServer/pwa/_vti_bin/psi/project.asmx?wsdl`</span></span>
    
   <span data-ttu-id="86ad9-225">または、Web ブラウザーを開き、に移動します `https://ServerName/ProjectServerName/_vti_bin/psi/ServiceName.asmx?wsdl` 。</span><span class="sxs-lookup"><span data-stu-id="86ad9-225">Or, open your web browser, and navigate to `https://ServerName/ProjectServerName/_vti_bin/psi/ServiceName.asmx?wsdl`.</span></span> <span data-ttu-id="86ad9-226">ファイルをローカル ディレクトリ (など) に保存します `C:\Project\WebServices\ServiceName.wsdl` 。</span><span class="sxs-lookup"><span data-stu-id="86ad9-226">Save the file to a local directory, such as `C:\Project\WebServices\ServiceName.wsdl`.</span></span> <span data-ttu-id="86ad9-227">[**Web 参照の追加**] ダイアログ ボックスの [**URL**] にファイル プロトコルとファイルへのパスを入力します。</span><span class="sxs-lookup"><span data-stu-id="86ad9-227">In the **Add Web Reference** dialog box, for **URL**, type the file protocol and the path to the file.</span></span> <span data-ttu-id="86ad9-228">たとえば、と入力します `file://C:\Project\WebServices\Project.wsdl` 。</span><span class="sxs-lookup"><span data-stu-id="86ad9-228">For example, type `file://C:\Project\WebServices\Project.wsdl`.</span></span> 
    
5. <span data-ttu-id="86ad9-229">参照が解決した後、[**Web 参照名**] ボックスに参照名を入力します。</span><span class="sxs-lookup"><span data-stu-id="86ad9-229">After the reference resolves, type the reference name in the **Web reference name** text box.</span></span> <span data-ttu-id="86ad9-230">2013 年 2013 Projectのコード例では、任意の標準参照名 **Svc _ServiceName を使用します_**。</span><span class="sxs-lookup"><span data-stu-id="86ad9-230">Code examples in the Project 2013 developer documentation use the arbitrary standard reference name **Svc _ServiceName_**.</span></span> <span data-ttu-id="86ad9-231">たとえば、Project Web サービスは **SvcProject** という名前になっています (図 3 を参照)。</span><span class="sxs-lookup"><span data-stu-id="86ad9-231">For example, the Project web service is named **SvcProject** (see Figure 3).</span></span> 
    
   <span data-ttu-id="86ad9-232">**図 3. ASMX Web サービス参照の追加**</span><span class="sxs-lookup"><span data-stu-id="86ad9-232">**Figure 3. Adding an ASMX web service reference**</span></span>

   <span data-ttu-id="86ad9-233">![ASMX Web サービス参照の追加](media/pj15_PrerequisitesASMX_AddWebSvcReference.gif "ASMX Web サービス参照の追加")</span><span class="sxs-lookup"><span data-stu-id="86ad9-233">![Adding an ASMX web service reference](media/pj15_PrerequisitesASMX_AddWebSvcReference.gif "Adding an ASMX web service reference")</span></span>
  
<span data-ttu-id="86ad9-234">Project Server コンピューター上で実行する必要があるアプリケーション コンポーネントについては、偽装を使用するか、または引き上げられたアクセス許可を使用して、ASMX Web 参照の代わりに WCF サービス参照を使用します。</span><span class="sxs-lookup"><span data-stu-id="86ad9-234">For application components that must run on the Project Server computer, use impersonation, or have elevated permissions, use a WCF service reference instead of an ASMX web reference.</span></span> <span data-ttu-id="86ad9-235">詳細については、「Wcf ベースのコード サンプルの前提条件」を[参照Project。](prerequisites-for-wcf-based-code-samples-in-project.md)</span><span class="sxs-lookup"><span data-stu-id="86ad9-235">For more information, see [Prerequisites for WCF-based code samples in Project](prerequisites-for-wcf-based-code-samples-in-project.md).</span></span>
  
## <a name="setting-other-references"></a><span data-ttu-id="86ad9-236">その他の参照を設定する</span><span class="sxs-lookup"><span data-stu-id="86ad9-236">Setting other references</span></span>
<span data-ttu-id="86ad9-237"><a name="pj15_PrerequisitesASMX_OtherReferences"> </a></span><span class="sxs-lookup"><span data-stu-id="86ad9-237"><a name="pj15_PrerequisitesASMX_OtherReferences"> </a></span></span>

<span data-ttu-id="86ad9-238">Projectサーバー アプリケーションは、多くの場合、サーバー 2013 web サービスなどのSharePointサービスを使用します。</span><span class="sxs-lookup"><span data-stu-id="86ad9-238">Project Server applications often use other services, such as SharePoint Server 2013 web services.</span></span> <span data-ttu-id="86ad9-239">その他のサービスが必要である場合、サービスはサンプルに記載されています。</span><span class="sxs-lookup"><span data-stu-id="86ad9-239">If other services are required, they are noted in the example.</span></span>
  
<span data-ttu-id="86ad9-240">コード サンプルのローカル参照は、サンプルの上部の **using** ステートメントに一覧表示されています。</span><span class="sxs-lookup"><span data-stu-id="86ad9-240">Local references for the code sample are listed in **using** statements at the top of the sample:</span></span> 
  
1. <span data-ttu-id="86ad9-241">**ソリューション エクスプローラー** で、[**参照設定**] フォルダーを右クリックし、[**参照の追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="86ad9-241">In **Solution Explorer**, right-click the **References** folder, and then choose **Add Reference**.</span></span>
    
2. <span data-ttu-id="86ad9-p133">[**参照**] をクリックして、以前にコピーした Project Server の DLL を格納した場所を参照します。必要な DLL を選択して、[**OK**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="86ad9-p133">Choose **Browse**, and then browse to the location where you stored the Project Server DLLs that you copied previously. Choose the DLLs you need, and then choose **OK**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="86ad9-244">開発用コンピューター上のアセンブリのバージョンがターゲット Project Server コンピューターのものと厳密に一致していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="86ad9-244">Ensure that the assembly versions on your development computer exactly match those on the target Project Server computer.</span></span> 
  
## <a name="using-multiple-authentication"></a><span data-ttu-id="86ad9-245">複数の認証を使用する</span><span class="sxs-lookup"><span data-stu-id="86ad9-245">Using multiple authentication</span></span>
<span data-ttu-id="86ad9-246"><a name="pj15_PrerequisitesASMX_ClaimsMultiAuth"> </a></span><span class="sxs-lookup"><span data-stu-id="86ad9-246"><a name="pj15_PrerequisitesASMX_ClaimsMultiAuth"> </a></span></span>

<span data-ttu-id="86ad9-247">Windows 認証とフォーム認証のProject、オンプレミスのサーバー ユーザーの認証は、SharePoint Server 2013 で行われます。</span><span class="sxs-lookup"><span data-stu-id="86ad9-247">Authentication of on-premises Project Server users, whether by Windows authentication or Forms authentication, is done through claims processing in SharePoint Server 2013.</span></span> <span data-ttu-id="86ad9-248">複数認証とは、プロビジョニングされている Web アプリケーションがProject Web App認証とフォーム ベース認証Windows両方をサポートします。</span><span class="sxs-lookup"><span data-stu-id="86ad9-248">Multiple authentication means that the web application on which Project Web App is provisioned supports both Windows authentication and Forms-based authentication.</span></span> <span data-ttu-id="86ad9-249">この場合、Windows 認証を使用する ASMX Web サービスの呼び出しは、クレーム プロセスで認証するユーザーの種類を決定できないので、次のエラーで失敗します。</span><span class="sxs-lookup"><span data-stu-id="86ad9-249">If that is the case, a call to an ASMX web service that uses Windows authentication will fail with the following error, because the claims process cannot determine which type of user to authenticate:</span></span>
  
`The server was unable to process the request due to an internal error. . . .`

<span data-ttu-id="86ad9-p135">ASMX のこの問題を修正するには、PSI メソッドのすべての呼び出しをそれぞれの PSI Web サービスに対して定義される派生クラスに対して実行する必要があります。また、派生クラスは **SvcLoginWindows.LoginWindows** クラスを使用して派生 PSI サービス クラスの Cookie を取得する必要があります。以下の例で、**ProjectDerived** クラスは **SvcProject.Project** クラスから派生します。派生したクラスによって **EnforceWindowsAuth** プロパティが追加され、**Project** クラスのメソッドに対するすべての呼び出しの Web 要求ヘッダーが上書きされます。**EnforceWindowsAuth** プロパティが **true** の場合、**GetWebRequest** メソッドによって、フォーム認証を無効にするヘッダーが追加されます。**EnforceWindowsAuth** が **false** の場合、フォーム認証を続行できます。</span><span class="sxs-lookup"><span data-stu-id="86ad9-p135">To fix the problem for ASMX, all calls to PSI methods should be to a derived class that is defined for each PSI web service. The derived class must also use the **SvcLoginWindows.LoginWindows** class to get a cookie for the derived PSI service class. In the following example, the **ProjectDerived** class derives from the **SvcProject.Project** class. The derived class adds the **EnforceWindowsAuth** property and overrides the web request header for every call to a method in the **Project** class. If the **EnforceWindowsAuth** property is **true**, the **GetWebRequest** method adds a header that disables Forms authentication. If **EnforceWindowsAuth** is **false**, Forms authentication can proceed.</span></span>
  
<span data-ttu-id="86ad9-p136">以下の **ASMXLogon_MultiAuth** サンプルを使用するには、コンソール アプリケーションを作成し、「[アプリケーションを作成して Web サービス参照を追加する](#pj15_PrerequisitesASMX_Configure)」の手順に従います。その後、wsdl.LoginWindows.cs プロキシ ファイルと wsdl.Project.cs プロキシ ファイルを追加します。**Main** メソッドによって、**ProjectDerived** クラスの **project** インスタンスが作成されます。サンプルでは派生した **LoginWindowsDerived** クラスを使用して、**project.CookieContainer** プロパティの **CookieContainer** オブジェクトを取得する必要があります。このオブジェクトによって、フォーム認証と Windows 認証が識別されます。その後、**project** オブジェクトを使用して **SvcProject.Project** クラスの任意のメソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="86ad9-p136">To use the following **ASMXLogon_MultiAuth** sample, create a console application, follow the steps in [Creating the application and adding a web service reference](#pj15_PrerequisitesASMX_Configure), and then add the wsdl.LoginWindows.cs proxy file and the wsdl.Project.cs proxy file. The **Main** method creates the **project** instance of the **ProjectDerived** class. The sample must use the derived **LoginWindowsDerived** class to get a **CookieContainer** object for the **project.CookieContainer** property, which distinguishes Forms authentication from Windows authentication. The **project** object can then be used to make calls to any method in the **SvcProject.Project** class.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="86ad9-p137">**LoginWindows** サービスは、複数認証環境の ASMX アプリケーションでのみ必要です。**ASMXLogon_MultiAuth** サンプルでは、**GetLogonCookie** メソッドによって **loginWindows** オブジェクトの Cookie が取得されます。**project.CookieContainer** プロパティは **loginWindows.CookieContainer** 値に設定されます。</span><span class="sxs-lookup"><span data-stu-id="86ad9-p137">The **LoginWindows** service is required only for ASMX applications in a multiple authentication environment. In the **ASMXLogon_MultiAuth** sample, the **GetLogonCookie** method gets a cookie for the **loginWindows** object. The **project.CookieContainer** property is set to the **loginWindows.CookieContainer** value.</span></span> 
  
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

<span data-ttu-id="86ad9-p138">派生した **LoginWindows** クラスを使用して、フォーム認証を無効化する Web 要求ヘッダーを持つ PSI 呼び出しを行うことは、複数認証環境で実行されるアプリケーションでは必須です。Project Server がクレーム認証のみを使用している場合は、Web 要求ヘッダーを追加するクラスを派生させる必要はありません。前に示した例は両方の環境で動作します。</span><span class="sxs-lookup"><span data-stu-id="86ad9-p138">Using the derived **LoginWindows** class, and making PSI calls with a web request header that disables Forms authentication, is required for applications that run in a multiple authentication environment. If Project Server uses only claims authentication, it is not necessary to derive a class that adds a web request header. The previous example runs in both environments.</span></span> 
  
<span data-ttu-id="86ad9-266">WCF ベース アプリケーションについては、別の方法で対処します。</span><span class="sxs-lookup"><span data-stu-id="86ad9-266">The fix for a WCF-based application is different.</span></span> <span data-ttu-id="86ad9-267">詳細については、「Wcf ベースのコード サンプルの前提条件」の「複数認証を使用する」を参照[Project。](prerequisites-for-wcf-based-code-samples-in-project.md)</span><span class="sxs-lookup"><span data-stu-id="86ad9-267">For more information, see the  *Using multiple authentication*  section in [Prerequisites for WCF-based code samples in Project](prerequisites-for-wcf-based-code-samples-in-project.md).</span></span>
  
## <a name="changing-the-values-of-generic-constants"></a><span data-ttu-id="86ad9-268">一般的な定数の値を変更する</span><span class="sxs-lookup"><span data-stu-id="86ad9-268">Changing the values of generic constants</span></span>
<span data-ttu-id="86ad9-269"><a name="pj15_PrerequisitesASMX_ChangeValues"> </a></span><span class="sxs-lookup"><span data-stu-id="86ad9-269"><a name="pj15_PrerequisitesASMX_ChangeValues"> </a></span></span>

<span data-ttu-id="86ad9-270">大部分のサンプルには、サンプルが環境で正しく動作するために更新する必要がある 1 つ以上の変数があります。</span><span class="sxs-lookup"><span data-stu-id="86ad9-270">Most samples have one or more variables that you must update for the sample to work properly in your environment.</span></span> <span data-ttu-id="86ad9-271">次の例では、SSL がインストールされている場合に HTTP プロトコルではなく HTTPS プロトコルを使用します。</span><span class="sxs-lookup"><span data-stu-id="86ad9-271">In the following example, if you have SSL installed, use the HTTPS protocol instead of the HTTP protocol.</span></span> <span data-ttu-id="86ad9-272">_ServerName を_ 使用しているサーバーの名前に置き換える。</span><span class="sxs-lookup"><span data-stu-id="86ad9-272">Replace  _ServerName_ with the name of the server that you are using.</span></span> <span data-ttu-id="86ad9-273">_ProjectServerName を_ サーバー サイトの仮想ディレクトリProject置き換PWA。</span><span class="sxs-lookup"><span data-stu-id="86ad9-273">Replace  _ProjectServerName_ with the virtual directory name of your Project Server site, such as PWA.</span></span> 
  
```cs
const string PROJECT_SERVER_URI = "https://ServerName/ProjectServerName/";
```

<span data-ttu-id="86ad9-274">変更する必要があるその他の変数または必要条件は、コード サンプルの上部に記載されています。</span><span class="sxs-lookup"><span data-stu-id="86ad9-274">Any other variables that you must change or other prerequisites are noted at the top of the code example.</span></span>
  
## <a name="verifying-the-results"></a><span data-ttu-id="86ad9-275">結果を確認する</span><span class="sxs-lookup"><span data-stu-id="86ad9-275">Verifying the results</span></span>
<span data-ttu-id="86ad9-276"><a name="pj15_PrerequisitesASMX_Verify"> </a></span><span class="sxs-lookup"><span data-stu-id="86ad9-276"><a name="pj15_PrerequisitesASMX_Verify"> </a></span></span>

<span data-ttu-id="86ad9-277">コード サンプルの結果の取得と解釈は、必ずしも簡単ではありません。</span><span class="sxs-lookup"><span data-stu-id="86ad9-277">Getting and interpreting results from a code sample is not always straightforward.</span></span> <span data-ttu-id="86ad9-278">たとえば、プロジェクトを作成する場合は、プロジェクトがプロジェクトの [センター] ページに表示される前にProject発行するProject Web App。</span><span class="sxs-lookup"><span data-stu-id="86ad9-278">For example, if you create a project, you must publish the project before it can appear on the Project Center page in Project Web App.</span></span>
  
<span data-ttu-id="86ad9-279">コード サンプルの結果は、いくつかの方法で確認できます。たとえば、次のような方法があります。</span><span class="sxs-lookup"><span data-stu-id="86ad9-279">You can verify code sample results in several ways, for example:</span></span>
  
- <span data-ttu-id="86ad9-280">2013 Project Professional 2013 クライアントを使用して、Project サーバー コンピューターからプロジェクトを開き、必要なアイテムを表示します。</span><span class="sxs-lookup"><span data-stu-id="86ad9-280">Use the Project Professional 2013 client to open the project from the Project Server computer, and view the items that you want.</span></span>
    
- <span data-ttu-id="86ad9-281">発行済みプロジェクトは、Project ( ) の [センター] ページProject Web App表示 `https://ServerName/ProjectServerName/projects.aspx` します。</span><span class="sxs-lookup"><span data-stu-id="86ad9-281">View published projects on the Project Center page of Project Web App ( `https://ServerName/ProjectServerName/projects.aspx`).</span></span>
    
- <span data-ttu-id="86ad9-282">[キュー ログ] を表示Project Web App。</span><span class="sxs-lookup"><span data-stu-id="86ad9-282">View the Queue log in Project Web App.</span></span> <span data-ttu-id="86ad9-283">[サーバーの設定] ページを開き (右上隅にある **[設定]** アイコンを選択し、[個人用のジョブ] セクション ( ) の [マイ キューに入っているジョブ]**を設定** します `https://ServerName/ProjectServerName/MyJobs.aspx` 。</span><span class="sxs-lookup"><span data-stu-id="86ad9-283">Open the Server Settings page (choose the **Settings** icon in the top-right corner), and then choose **My Queued Jobs** under the **Personal Settings** section (  `https://ServerName/ProjectServerName/MyJobs.aspx`).</span></span> <span data-ttu-id="86ad9-284">[**表示**] ドロップダウン リストでは、ジョブの状態による並べ替えができます。</span><span class="sxs-lookup"><span data-stu-id="86ad9-284">In the **View** drop-down list, you can sort by the job status.</span></span> <span data-ttu-id="86ad9-285">既定の状態は [**進行中または失敗した過去 1 週間のジョブ**] です。</span><span class="sxs-lookup"><span data-stu-id="86ad9-285">The default status is **In Progress and Failed Jobs in the Past Week**.</span></span> 
    
- <span data-ttu-id="86ad9-286">すべてのキュー ジョブ設定をProject Web App、エンタープライズ オブジェクトの削除または強制チェックインを行う場合は、() の [サーバー サーバー] `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx` ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="86ad9-286">Use the Server Settings page in Project Web App ( `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`) to manage all queue jobs and delete or force check-in enterprise objects.</span></span> <span data-ttu-id="86ad9-287">[サーバー設定] ページのこれらのリンクにアクセスするには、管理権限が必要です。</span><span class="sxs-lookup"><span data-stu-id="86ad9-287">You must have administrative permissions to access those links on the Server Settings page.</span></span>
    
- <span data-ttu-id="86ad9-p144">**Microsoft SQL Server Management Studio** を使用して Project データベース内のテーブルに対するクエリを実行します。たとえば、次のクエリを使用して、pub.MSP_WORKFLOW_STAGE_PDPS テーブルの先頭から 200 行を選択し、ワークフロー ステージにプロジェクト詳細ページ (PDP) についての情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="86ad9-p144">Use **Microsoft SQL Server Management Studio** to run a query on a table in the Project database. For example, use the following query to select the top 200 rows of the pub.MSP_WORKFLOW_STAGE_PDPS table to show information about the project detail pages (PDPs) in workflow stages.</span></span> 
    
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

## <a name="cleaning-up"></a><span data-ttu-id="86ad9-290">クリーンアップ</span><span class="sxs-lookup"><span data-stu-id="86ad9-290">Cleaning up</span></span>
<span data-ttu-id="86ad9-291"><a name="pj15_PrerequisitesASMX_Cleanup"> </a></span><span class="sxs-lookup"><span data-stu-id="86ad9-291"><a name="pj15_PrerequisitesASMX_Cleanup"> </a></span></span>

<span data-ttu-id="86ad9-292">いくつかのコード サンプルをテストすると、エンタープライズ オブジェクトおよび設定の削除や再設定が必要になります。</span><span class="sxs-lookup"><span data-stu-id="86ad9-292">After you test some code samples, there are enterprise objects and settings that should be deleted or reset.</span></span> <span data-ttu-id="86ad9-293">エンタープライズ データ () を管理設定サーバー Project Web Appページを使用できます `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx` 。</span><span class="sxs-lookup"><span data-stu-id="86ad9-293">You can use the Server Settings page in Project Web App to manage enterprise data ( `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`).</span></span> <span data-ttu-id="86ad9-294">[サーバー設定] ページにあるリンクを使用して、古いアイテムを削除したり、チェックインを強制したり、すべてのユーザーのジョブ キューを管理したり、その他の管理タスクを実行したりできます。</span><span class="sxs-lookup"><span data-stu-id="86ad9-294">Links on the Server Settings page enable you to delete old items, force check-in projects, manage the job queue for all users, and perform other administrative tasks.</span></span>
  
<span data-ttu-id="86ad9-295">[サーバー設定] ページに表示されるリンクの一部を以下に示します。これらは、コード サンプルを実行した後に一般的なクリーンアップの操作を行うために使用できます。</span><span class="sxs-lookup"><span data-stu-id="86ad9-295">Following are some of the links on the Server Settings page that you can use for typical cleanup activities after running code samples:</span></span>
  
- <span data-ttu-id="86ad9-296">**エンタープライズ ユーザー設定フィールドと参照テーブル**</span><span class="sxs-lookup"><span data-stu-id="86ad9-296">**Enterprise Custom Fields and Lookup Tables**</span></span>
    
- <span data-ttu-id="86ad9-297">**キュー ジョブの管理**</span><span class="sxs-lookup"><span data-stu-id="86ad9-297">**Manage Queue Jobs**</span></span>
    
- <span data-ttu-id="86ad9-298">**エンタープライズ オブジェクトの削除**</span><span class="sxs-lookup"><span data-stu-id="86ad9-298">**Delete Enterprise Objects**</span></span>
    
- <span data-ttu-id="86ad9-299">**エンタープライズ オブジェクトの強制チェックイン**</span><span class="sxs-lookup"><span data-stu-id="86ad9-299">**Force Check-in Enterprise Objects**</span></span>
    
- <span data-ttu-id="86ad9-300">**エンタープライズ プロジェクトの種類**</span><span class="sxs-lookup"><span data-stu-id="86ad9-300">**Enterprise Project Types**</span></span>
    
- <span data-ttu-id="86ad9-301">**ワークフロー フェーズ**</span><span class="sxs-lookup"><span data-stu-id="86ad9-301">**Workflow Phases**</span></span>
    
- <span data-ttu-id="86ad9-302">**ワークフロー ステージ**</span><span class="sxs-lookup"><span data-stu-id="86ad9-302">**Workflow Stages**</span></span>
    
- <span data-ttu-id="86ad9-303">**プロジェクト詳細ページ**</span><span class="sxs-lookup"><span data-stu-id="86ad9-303">**Project Detail Pages**</span></span>
    
- <span data-ttu-id="86ad9-304">**タイムシート期間**</span><span class="sxs-lookup"><span data-stu-id="86ad9-304">**Time Reporting Periods**</span></span>
    
- <span data-ttu-id="86ad9-305">**タイムシートの設定および既定値**</span><span class="sxs-lookup"><span data-stu-id="86ad9-305">**Timesheet Settings and Defaults**</span></span>
    
- <span data-ttu-id="86ad9-306">**管理用行の分類**</span><span class="sxs-lookup"><span data-stu-id="86ad9-306">**Line Classifications**</span></span>
    
<span data-ttu-id="86ad9-307">その他の設定は、SharePoint Server 2013 で特定の Project Web App インスタンスではなく、Project Web App Server 2013 設定 ページによって管理されます。</span><span class="sxs-lookup"><span data-stu-id="86ad9-307">Additional settings are managed by SharePoint Server 2013 for each Project Web App instance, rather than by a specific Project Web App Server Settings page.</span></span> <span data-ttu-id="86ad9-308">SharePoint サーバーの全体管理アプリケーションで、[全般アプリケーション **設定]** を選択し **、[Project Server 設定]** の [管理] を選択し、[サーバー 設定] ページのドロップダウン リストで Project Web App インスタンスを選択します。 </span><span class="sxs-lookup"><span data-stu-id="86ad9-308">In the SharePoint Central Administration application, choose **General Application Settings**, choose **Manage** under **Project Server Settings**, and then choose the Project Web App instance in the drop-down list on the Server Settings page.</span></span> <span data-ttu-id="86ad9-309">たとえば、[サーバー側 **イベント ハンドラー] を** 選択して、選択したインスタンスのイベント ハンドラーを追加またはProject Web Appします。</span><span class="sxs-lookup"><span data-stu-id="86ad9-309">For example, choose **Server Side Event Handlers** to add or delete event handlers for the selected Project Web App instance.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="86ad9-310">関連項目</span><span class="sxs-lookup"><span data-stu-id="86ad9-310">See also</span></span>
<span data-ttu-id="86ad9-311"><a name="pj15_PrerequisitesASMX_AR"> </a></span><span class="sxs-lookup"><span data-stu-id="86ad9-311"><a name="pj15_PrerequisitesASMX_AR"> </a></span></span>

- [<span data-ttu-id="86ad9-312">プロジェクト内のWCFベースコードサンプルの前提条件</span><span class="sxs-lookup"><span data-stu-id="86ad9-312">Prerequisites for WCF-based code samples in Project</span></span>](prerequisites-for-wcf-based-code-samples-in-project.md)
- [<span data-ttu-id="86ad9-313">WCF で偽装を使用する</span><span class="sxs-lookup"><span data-stu-id="86ad9-313">Use Impersonation with WCF</span></span>](https://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)
- [<span data-ttu-id="86ad9-314">Project PSI リファレンスの概要</span><span class="sxs-lookup"><span data-stu-id="86ad9-314">Project PSI reference overview</span></span>](project-psi-reference-overview.md)
- [<span data-ttu-id="86ad9-315">SharePoint デベロッパー センター</span><span class="sxs-lookup"><span data-stu-id="86ad9-315">SharePoint Developer Center</span></span>](https://msdn.microsoft.com/sharepoint/default.aspx)
    

