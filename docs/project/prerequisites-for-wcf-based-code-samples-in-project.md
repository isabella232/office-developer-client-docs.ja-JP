---
title: プロジェクト内のWCFベースコードサンプルの前提条件
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 60d2afc8-10b6-465d-8ce8-c073da6e5054
description: Project Server Interface (PSI) リファレンス トピックに含まれる WCF ベースのコード サンプルを使用して、Visual Studio でプロジェクトを作成するのに役立つ情報について説明します。
ms.openlocfilehash: 2222e1b3651044c41f45e57481f80093aac67bdb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357167"
---
# <a name="prerequisites-for-wcf-based-code-samples-in-project"></a><span data-ttu-id="63ff0-103">プロジェクト内のWCFベースコードサンプルの前提条件</span><span class="sxs-lookup"><span data-stu-id="63ff0-103">Prerequisites for WCF-based code samples in Project</span></span>

<span data-ttu-id="63ff0-104">Project Server Interface (PSI) リファレンス トピックに含まれる WCF ベースのコード サンプルを使用して、Visual Studio でプロジェクトを作成するのに役立つ情報について説明します。</span><span class="sxs-lookup"><span data-stu-id="63ff0-104">Learn information to help you create projects in Visual Studio by using the WCF-based code samples that are included in the Project Server Interface (PSI) reference topics.</span></span>
   
<span data-ttu-id="63ff0-105">[Project Server 2013](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx)クラス ライブラリおよび Web サービスリファレンスに含まれる WCF ベースのコード サンプルの多くは、もともと Project 2010 開発者向けドキュメント用に作成され、WCF Web サービスの標準形式を使用しています。</span><span class="sxs-lookup"><span data-stu-id="63ff0-105">Many of the WCF-based code samples included in the [Project Server 2013 class library and web service reference](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) were originally created for the Project 2010 developer documentation, and use a standard format for WCF web services.</span></span> <span data-ttu-id="63ff0-106">サンプルは引き続き Project Server 2013 で動作し、コンソール アプリケーションにコピーされ、完全なユニットとして実行するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="63ff0-106">The samples still work in Project Server 2013 and are designed to be copied into a console application and run as a complete unit.</span></span> <span data-ttu-id="63ff0-107">例外はサンプルに記載されています。</span><span class="sxs-lookup"><span data-stu-id="63ff0-107">Exceptions are noted in the sample.</span></span> 
  
<span data-ttu-id="63ff0-108">Project Server 2007 用に開発されたサンプルから変更されていない Project 201 Office Project 3 開発者向けドキュメントのコード サンプルは、ASMX Web サービスを使用します。</span><span class="sxs-lookup"><span data-stu-id="63ff0-108">Code samples in the Project 2013 developer documentation that are unchanged from the samples developed for Office Project Server 2007 use ASMX Web services.</span></span> <span data-ttu-id="63ff0-109">この ASMX ベースのサンプルは、WCF サービスを使用するように調整することもできます。</span><span class="sxs-lookup"><span data-stu-id="63ff0-109">The ASMX-based samples can also be adapted to use WCF services.</span></span> <span data-ttu-id="63ff0-110">この記事では、このサンプルを WCF サービスで使用する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="63ff0-110">This article shows how to use the samples with WCF services.</span></span> <span data-ttu-id="63ff0-111">ASMX Web サービスでサンプルを使用する方法については[、「AsMX](prerequisites-for-asmx-based-code-samples-in-project.md)ベースのコード サンプルの前提条件」を参照Project。</span><span class="sxs-lookup"><span data-stu-id="63ff0-111">For information about how to use the samples with ASMX web services, see [Prerequisites for ASMX-based code samples in Project](prerequisites-for-asmx-based-code-samples-in-project.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="63ff0-112">クライアント側オブジェクト モデル (CSOM) にアプリケーションで必要なメソッドが含まれる場合は、CSOM を使用して新しいアプリケーションを開発する必要があります。</span><span class="sxs-lookup"><span data-stu-id="63ff0-112">If the client-side object model (CSOM) includes the methods that your application requires, new applications should be developed with the CSOM.</span></span> <span data-ttu-id="63ff0-113">CSOM を使用すると、アプリケーションはサーバーサーバー 2013 のProject Onlineまたはオンプレミスインストールで動作Projectできます。</span><span class="sxs-lookup"><span data-stu-id="63ff0-113">The CSOM enables applications to work with Project Online or an on-premises installation of Project Server 2013.</span></span> <span data-ttu-id="63ff0-114">それ以外の場合、アプリケーションで PSI を使用する場合は、ネットワーク通信に推奨されるテクノロジである WCF インターフェイスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="63ff0-114">Otherwise, if your application uses the PSI, it should use the WCF interface, which is the technology that we recommend for network communications.</span></span> <span data-ttu-id="63ff0-115">ASMX インターフェイスまたは WCF インターフェイスを使用するアプリケーションは、サーバー 2013 のオンプレミス インストールProjectできます。</span><span class="sxs-lookup"><span data-stu-id="63ff0-115">Applications that use the ASMX interface or the WCF interface can work only for on-premises installations of Project Server 2013.</span></span> 
>
> <span data-ttu-id="63ff0-116">CSOM の詳細については[、「Project Server 2013](project-server-2013-architecture.md)アーキテクチャとクライアント側オブジェクト モデル[(CSOM) for Project 2013」を参照](client-side-object-model-csom-for-project-2013.md)してください。</span><span class="sxs-lookup"><span data-stu-id="63ff0-116">For more information about the CSOM, see [Project Server 2013 architecture](project-server-2013-architecture.md) and [Client-side object model (CSOM) for Project 2013](client-side-object-model-csom-for-project-2013.md).</span></span> 
  
<span data-ttu-id="63ff0-117">コード サンプルを実行する前に、開発環境のセットアップ、アプリケーションの構成、サービス構成ファイルの追加 (またはプログラムによる WCF サービスの構成)、および環境に合わせた一般的な定数値の変更を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="63ff0-117">Before running the code samples, you must set up the development environment, configure the application, add a service configuration file (or configure the WCF services programmatically), and change generic constant values to match your environment.</span></span>
  
## <a name="setting-up-the-development-environment"></a><span data-ttu-id="63ff0-118">開発環境を設定する</span><span class="sxs-lookup"><span data-stu-id="63ff0-118">Setting up the development environment</span></span>
<span data-ttu-id="63ff0-119"><a name="pj15_PrerequisitesWCF_Setup"> </a></span><span class="sxs-lookup"><span data-stu-id="63ff0-119"><a name="pj15_PrerequisitesWCF_Setup"> </a></span></span>

1. <span data-ttu-id="63ff0-120">**テスト用の Project Server システムをセットアップする。**</span><span class="sxs-lookup"><span data-stu-id="63ff0-120">**Set up a test Project Server system.**</span></span>
    
    <span data-ttu-id="63ff0-p104">開発やテストを行う際には常にテスト Project Server システムを使用します。たとえコードが完全に動作しても、プロジェクト間の依存関係、レポート、またはその他の環境要因が意図しない結果を引き起こす可能性があります。</span><span class="sxs-lookup"><span data-stu-id="63ff0-p104">Use a test Project Server system whenever you are developing or testing. Even when your code works perfectly, interproject dependencies, reporting, or other environmental factors can cause unintended consequences.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="63ff0-123">サーバーの有効なユーザーであり、アプリケーションで使用する PSI 呼び出しのための十分な権限を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="63ff0-123">Ensure that you are a valid user on the server, and check that you have sufficient permissions for the PSI calls that your application uses.</span></span> <span data-ttu-id="63ff0-124">それぞれの PSI メソッドに関する開発者向けドキュメントのトピックには、Project Server 権限の表があります。</span><span class="sxs-lookup"><span data-stu-id="63ff0-124">The developer documentation topic for each PSI method includes a Project Server Permissions table.</span></span> <span data-ttu-id="63ff0-125">たとえば、次の [Project。QueueCreateProject メソッド](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx)には、**グローバルな NewProject** アクセス許可と **SaveProjectTemplate アクセス許可が必要** です。</span><span class="sxs-lookup"><span data-stu-id="63ff0-125">For example, the [Project.QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) method requires the global **NewProject** permission and the **SaveProjectTemplate** permission.</span></span> 
  
    <span data-ttu-id="63ff0-126">場合によっては、サーバーでのリモート デバッグが必要になることがあります。</span><span class="sxs-lookup"><span data-stu-id="63ff0-126">In some cases, you may have to do remote debugging on the server.</span></span> <span data-ttu-id="63ff0-127">SharePoint ファームの各 Project Server コンピューターにイベント ハンドラー アセンブリをインストールし、SharePoint サーバーの全体管理の全般アプリケーション 設定 の Project Server 設定 ページを使用して Project Web App インスタンスのイベント ハンドラーを構成することで、イベント ハンドラーをセットアップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="63ff0-127">You may also have to set up an event handler by installing an event handler assembly on each Project Server computer in the SharePoint farm, and then configuring the event handler for the Project Web App instance by using the Project Server Settings page in the General Application Settings of SharePoint Central Administration.</span></span>
    
2. <span data-ttu-id="63ff0-128">**開発用コンピューターをセットアップする。**</span><span class="sxs-lookup"><span data-stu-id="63ff0-128">**Set up a development computer.**</span></span>
    
    <span data-ttu-id="63ff0-p107">通常、PSI にはネットワーク経由でアクセスします。コード サンプルは、記載されている場合を除き、サーバーから分離されたクライアントで動作するように作られています。</span><span class="sxs-lookup"><span data-stu-id="63ff0-p107">You usually access the PSI through a network. The code samples are designed to be run on a client that is separate from the server, except where noted.</span></span>
    
    1. <span data-ttu-id="63ff0-131">**適切なバージョンの Visual Studio をインストールする。**</span><span class="sxs-lookup"><span data-stu-id="63ff0-131">**Install the correct version of Visual Studio.**</span></span> <span data-ttu-id="63ff0-132">記載されている場合を除き、コード サンプルは Visual C# で記述されています。</span><span class="sxs-lookup"><span data-stu-id="63ff0-132">Except where noted, the code samples are written in Visual C#.</span></span> <span data-ttu-id="63ff0-133">これらは、2010 年Visual Studio 2012 年Visual Studioできます。</span><span class="sxs-lookup"><span data-stu-id="63ff0-133">They can be used with Visual Studio 2010 or Visual Studio 2012.</span></span> <span data-ttu-id="63ff0-134">最新のサービス パックがインストールされていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="63ff0-134">Ensure that you have the most recent service pack installed.</span></span> 
    
    2. <span data-ttu-id="63ff0-135">**Project Server の DLL を開発用コンピューターにコピーする。**</span><span class="sxs-lookup"><span data-stu-id="63ff0-135">**Copy Project Server DLLs to the development computer.**</span></span> <span data-ttu-id="63ff0-136">サーバー コンピューター上の次の `[Program Files]\Microsoft Office Servers\15.0\Bin` アセンブリProject開発用コンピューターにコピーします。</span><span class="sxs-lookup"><span data-stu-id="63ff0-136">Copy the following assemblies from  `[Program Files]\Microsoft Office Servers\15.0\Bin` on the Project Server computer to the development computer:</span></span> 
    
       - <span data-ttu-id="63ff0-137">Microsoft.Office.Project.Server.Events.Receivers.dll</span><span class="sxs-lookup"><span data-stu-id="63ff0-137">Microsoft.Office.Project.Server.Events.Receivers.dll</span></span>
    
       - <span data-ttu-id="63ff0-138">Microsoft.Office.Project.Server.Library.dll</span><span class="sxs-lookup"><span data-stu-id="63ff0-138">Microsoft.Office.Project.Server.Library.dll</span></span>
    
    3. <span data-ttu-id="63ff0-139">PSI で WCF サービスの ProjectServerServices.dll プロキシ アセンブリをコンパイルして使用する方法に関する情報については、「[Intellisense の説明を備えた PSI プロキシ アセンブリを使用する](#pj15_PrerequisitesWCF_BuildingProxy)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="63ff0-139">For information about how to compile and use the ProjectServerServices.dll proxy assembly for the WCF services in the PSI, see [Using a PSI proxy assembly and IntelliSense descriptions](#pj15_PrerequisitesWCF_BuildingProxy).</span></span>
    
3. <span data-ttu-id="63ff0-140">**IntelliSense ファイルをインストールする。**</span><span class="sxs-lookup"><span data-stu-id="63ff0-140">**Install the IntelliSense files.**</span></span>
    
    <span data-ttu-id="63ff0-141">Project Server アセンブリのクラスとメンバーに IntelliSense の説明を使用するには、Project 2013 SDK のダウンロードから更新された IntelliSense XML ファイルを、Project Server アセンブリがある同じディレクトリにコピーします。</span><span class="sxs-lookup"><span data-stu-id="63ff0-141">To use IntelliSense descriptions for classes and members in Project Server assemblies, copy the updated IntelliSense XML files from the Project 2013 SDK download to the same directory where the Project Server assemblies are located.</span></span> <span data-ttu-id="63ff0-142">たとえば、アプリケーションで Microsoft.Office.Project.Server.Library.dll アセンブリへの参照を設定するディレクトリに、Microsoft.Office.Project.Server.Library.xml ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="63ff0-142">For example, copy the Microsoft.Office.Project.Server.Library.xml file to the directory where your application will set a reference to the Microsoft.Office.Project.Server.Library.dll assembly.</span></span>
    
    <span data-ttu-id="63ff0-143">IntelliSense PSI サービスの説明では、Project SDK ダウンロードのサブディレクトリで CompileWCFProxyAssembly.cmd スクリプトを使用して PSI プロキシ アセンブリを作成する必要があります。 `Documentation\IntelliSense\WCF`</span><span class="sxs-lookup"><span data-stu-id="63ff0-143">IntelliSense descriptions for the PSI services require that you create a PSI proxy assembly by using the CompileWCFProxyAssembly.cmd script in the  `Documentation\IntelliSense\WCF` subdirectory in the Project 2013 SDK download.</span></span> <span data-ttu-id="63ff0-144">このスクリプトを実行すると、WCF ベースの ProjectServerServices.dll プロキシ アセンブリが作成されます。</span><span class="sxs-lookup"><span data-stu-id="63ff0-144">The script creates the WCF-based ProjectServerServices.dll proxy assembly.</span></span> <span data-ttu-id="63ff0-145">詳細については、SDK ダウンロードに含まれる [ReadMe_IntelliSense].mht ファイルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="63ff0-145">For more information, see the [ReadMe_IntelliSense].mht file in the SDK download.</span></span> 
    
## <a name="creating-the-application-and-adding-a-service-reference"></a><span data-ttu-id="63ff0-146">アプリケーションを作成してサービス参照を追加する</span><span class="sxs-lookup"><span data-stu-id="63ff0-146">Creating the application and adding a service reference</span></span>
<span data-ttu-id="63ff0-147"><a name="pj15_PrerequisitesWCF_Configure"> </a></span><span class="sxs-lookup"><span data-stu-id="63ff0-147"><a name="pj15_PrerequisitesWCF_Configure"> </a></span></span>

1. <span data-ttu-id="63ff0-148">**コンソール アプリケーションを作成する。**</span><span class="sxs-lookup"><span data-stu-id="63ff0-148">**Create a console application.**</span></span>
    
    <span data-ttu-id="63ff0-p112">コンソール アプリケーションを作成するには、[**新しいプロジェクト**] ダイアログ ボックスのドロップダウン リストから [**.NET Framework 4**] を選択します。この新しいアプリケーションに PSI サンプル コードをコピーできます。</span><span class="sxs-lookup"><span data-stu-id="63ff0-p112">When you create a console application, in the drop-down list of the **New Project** dialog box, select **.NET Framework 4**. You can copy the PSI example code into the new application.</span></span>
    
2. <span data-ttu-id="63ff0-151">**WCF に必要な参照を追加する。**</span><span class="sxs-lookup"><span data-stu-id="63ff0-151">**Add references required for WCF.**</span></span>
    
    <span data-ttu-id="63ff0-152">ソリューション エクスプローラーで、**System.ServiceModel** への参照を追加します (図 1 を参照)。</span><span class="sxs-lookup"><span data-stu-id="63ff0-152">In Solution Explorer, add a reference to **System.ServiceModel** (see Figure 1).</span></span> <span data-ttu-id="63ff0-153">Web アプリケーションの場合は、**System.ServiceModel.Web** を使用します。</span><span class="sxs-lookup"><span data-stu-id="63ff0-153">A web application would use **System.ServiceModel.Web**.</span></span>
    
    <span data-ttu-id="63ff0-154">**System.Runtime.Serialization** への参照も追加します。</span><span class="sxs-lookup"><span data-stu-id="63ff0-154">Also add a reference to **System.Runtime.Serialization**.</span></span>
    
    <span data-ttu-id="63ff0-155">**図 1. Visual Studio での WCF ベースのアプリケーションへの参照の追加**</span><span class="sxs-lookup"><span data-stu-id="63ff0-155">**Figure 1. Adding the references in Visual Studio for a WCF-based application**</span></span>

    <span data-ttu-id="63ff0-156">![WCF 参照の追加 WCF](media/pj15_PrerequisitesWCF_AddReference.gif "の参照の追加")</span><span class="sxs-lookup"><span data-stu-id="63ff0-156">![Adding references for WCF](media/pj15_PrerequisitesWCF_AddReference.gif "Adding references for WCF")</span></span>
  
3. <span data-ttu-id="63ff0-157">**コードをコピーする。**</span><span class="sxs-lookup"><span data-stu-id="63ff0-157">**Copy the code**.</span></span>
    
    <span data-ttu-id="63ff0-158">コード サンプル全体をコンソール アプリケーションの Program.cs ファイルにコピーします。</span><span class="sxs-lookup"><span data-stu-id="63ff0-158">Copy the complete code example into the Program.cs file of the console application.</span></span>
    
4. <span data-ttu-id="63ff0-159">**サンプル アプリケーションの名前空間を設定する。**</span><span class="sxs-lookup"><span data-stu-id="63ff0-159">**Set the namespace for the sample application.**</span></span>
    
    <span data-ttu-id="63ff0-p114">サンプルの上部に記されている名前空間をアプリケーションの既定の名前空間に変更するか、アプリケーションの既定の名前空間をサンプルに合わせて変更することができます。アプリケーションの既定の名前空間は、アプリケーションのプロパティを変更することによって変更できます。</span><span class="sxs-lookup"><span data-stu-id="63ff0-p114">You can either change the namespace listed at the top of the sample to the application default namespace, or change the default application namespace to match the sample. You can change the default application namespace by changing the application properties.</span></span> 
    
    <span data-ttu-id="63ff0-162">たとえば [、ReadResource](https://msdn.microsoft.com/library/WebSvcResource.Resource.ReadResource.aspx)のコード サンプルには **、Microsoft.SDK.Project という名前空間があります。Samples.CreateResourceTest**.</span><span class="sxs-lookup"><span data-stu-id="63ff0-162">For example, the code sample for [ReadResource](https://msdn.microsoft.com/library/WebSvcResource.Resource.ReadResource.aspx) has the namespace **Microsoft.SDK.Project.Samples.CreateResourceTest**.</span></span> <span data-ttu-id="63ff0-163">Visual Studio プロジェクトの名前が **ResourceTest** である場合、Program.cs ファイルから名前空間をコピーし、プロジェクトの [**プロパティ**] ウィンドウを開きます ([**プロジェクト**] メニューで [**ResourceTest のプロパティ**] をクリック)。</span><span class="sxs-lookup"><span data-stu-id="63ff0-163">If the name of the Visual Studio project is **ResourceTest**, copy the namespace from the Program.cs file, and then open the project **Properties** pane (on the **Project** menu, choose **ResourceTest Properties**).</span></span> <span data-ttu-id="63ff0-164">[**アプリケーション**] タブで、その名前空間を [**既定の名前空間**] テキスト ボックスにコピーします。</span><span class="sxs-lookup"><span data-stu-id="63ff0-164">On the **Application** tab, copy the namespace into the **Default namespace** text box.</span></span> 
    
5. <span data-ttu-id="63ff0-165">**サービス参照を設定する。**</span><span class="sxs-lookup"><span data-stu-id="63ff0-165">**Set the service references.**</span></span>
    
    <span data-ttu-id="63ff0-p116">多くの例では、1 つ以上の PSI サービスへの参照が必要です。これらは、サンプル自体、またはサンプルの前にあるコメントに示されています。サービス参照の適切な名前空間を取得するには、最初にアプリケーションの既定の名前空間を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="63ff0-p116">Many examples require a reference to one or more of the PSI services. These are listed in the sample itself or in comments that precede the sample. To get the correct namespace of the service references, ensure that you first set the default application namespace.</span></span>
    
    <span data-ttu-id="63ff0-169">WCF サービス参照を追加する方法として次の 3 つがあります。</span><span class="sxs-lookup"><span data-stu-id="63ff0-169">There are three ways to add a WCF service reference:</span></span>
    
    - <span data-ttu-id="63ff0-p117">ProjectServerServices.dll という名前の PSI プロキシ アセンブリを作成してから、このアセンブリへの参照を設定します。詳細については「[Intellisense の説明を備えた PSI プロキシ アセンブリを使用する](#pj15_PrerequisitesWCF_BuildingProxy)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="63ff0-p117">Build a PSI proxy assembly named ProjectServerServices.dll, and then set a reference to the assembly. See [Using a PSI proxy assembly and IntelliSense descriptions](#pj15_PrerequisitesWCF_BuildingProxy).</span></span>
    
    - <span data-ttu-id="63ff0-p118">svcutil.exe 出力からのプロキシ ファイルを Visual Studio ソリューションに追加します。「[PSI プロキシ ファイルを追加する](#pj15_PrerequisitesWCF_AddingProxyFile)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="63ff0-p118">Add a proxy file from the svcutil.exe output to the Visual Studio solution. See [Adding a PSI proxy file](#pj15_PrerequisitesWCF_AddingProxyFile).</span></span>
    
    - <span data-ttu-id="63ff0-p119">Visual Studio を使用してサービス参照を追加します。「[サービス参照を追加する](#pj15_PrerequisitesWCF_AddingServiceReference)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="63ff0-p119">Add a service reference by using Visual Studio. See [Adding a service reference](#pj15_PrerequisitesWCF_AddingServiceReference).</span></span>
    
### <a name="using-a-psi-proxy-assembly-and-intellisense-descriptions"></a><span data-ttu-id="63ff0-176">Intellisense の説明を備えた PSI プロキシ アセンブリを使用する</span><span class="sxs-lookup"><span data-stu-id="63ff0-176">Using a PSI proxy assembly and IntelliSense descriptions</span></span>
<span data-ttu-id="63ff0-177"><a name="pj15_PrerequisitesWCF_BuildingProxy"> </a></span><span class="sxs-lookup"><span data-stu-id="63ff0-177"><a name="pj15_PrerequisitesWCF_BuildingProxy"> </a></span></span>

<span data-ttu-id="63ff0-178">PSI のすべてのパブリック WCF サービスには、プロキシ アセンブリを使用できます。</span><span class="sxs-lookup"><span data-stu-id="63ff0-178">You can use a proxy assembly for all public WCF services in the PSI.</span></span> <span data-ttu-id="63ff0-179">2013 ProjectServerServices.dll Project SDK ダウンロードのスクリプトを使用して、ProjectServerServices.dll プロキシ アセンブリをコンパイルし、プロキシ アセンブリを開発用コンピューター `Documentation\IntelliSense\WCF\CompileWCFProxyAssembly.cmd` にコピーします。</span><span class="sxs-lookup"><span data-stu-id="63ff0-179">Compile the ProjectServerServices.dll proxy assembly by using the  `Documentation\IntelliSense\WCF\CompileWCFProxyAssembly.cmd` script in the Project 2013 SDK download, and then copy the proxy assembly to your development computer.</span></span> <span data-ttu-id="63ff0-180">同じ場所に、Intellisense に関する ProjectServerServices.xml ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="63ff0-180">Copy the ProjectServerServices.xml file for IntelliSense to the same location.</span></span> <span data-ttu-id="63ff0-181">Visual Studio で、この ProjectServerServices.dll プロキシ アセンブリへの参照を設定します。</span><span class="sxs-lookup"><span data-stu-id="63ff0-181">In Visual Studio, set a reference to the ProjectServerServices.dll proxy assembly.</span></span> 
  
<span data-ttu-id="63ff0-182">Project Server のサービス パックおよび更新プログラムの場合は、同じ SDK ダウンロード フォルダーにある GenWCFProxyAssembly.cmd スクリプトを使用し、プロキシのソース ファイルを更新して新しいプロキシ アセンブリを作成できます。</span><span class="sxs-lookup"><span data-stu-id="63ff0-182">For Project Server service packs and updates, you can update the proxy source files and create a new proxy assembly by using the GenWCFProxyAssembly.cmd script in the same SDK download folder.</span></span> <span data-ttu-id="63ff0-183">SDK のダウンロードへのリンクについては[、2013 Projectドキュメントを参照してください](project-2013-developer-documentation.md)。</span><span class="sxs-lookup"><span data-stu-id="63ff0-183">For a link to the SDK download, see [Project 2013 developer documentation](project-2013-developer-documentation.md).</span></span> <span data-ttu-id="63ff0-184">詳細については、「[サービス参照を追加する](#pj15_PrerequisitesWCF_AddingServiceReference)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="63ff0-184">For more information, see the [Adding a service reference](#pj15_PrerequisitesWCF_AddingServiceReference) section.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="63ff0-185">Source.zip ファイルからプロキシ ソース ファイルを抽出すると、フォルダー内のファイルは、2013 SDK ダウンロードの発行日Project `Documentation\IntelliSense\WCF\Source` です。</span><span class="sxs-lookup"><span data-stu-id="63ff0-185">When you extract the proxy source files from the Source.zip file, the files in the  `Documentation\IntelliSense\WCF\Source` folder are current as of the publication date of the Project 2013 SDK download.</span></span> <span data-ttu-id="63ff0-186">更新された PSI プロキシ ソース ファイルを生成するには、Project Server コンピューターで GenASMXProxyAssembly.cmd スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="63ff0-186">To generate updated PSI proxy source files, run the GenASMXProxyAssembly.cmd script on the Project Server computer.</span></span> <span data-ttu-id="63ff0-187">詳細については、「[サービス参照を追加する](#pj15_PrerequisitesWCF_AddingServiceReference)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="63ff0-187">For more information, see [Adding a service reference](#pj15_PrerequisitesWCF_AddingServiceReference).</span></span> 
> 
> <span data-ttu-id="63ff0-188">フォルダー内のスクリプト  `Documentation\IntelliSense\ASMX` は、WCF ベースのアプリケーションでは機能しません。</span><span class="sxs-lookup"><span data-stu-id="63ff0-188">The scripts in the  `Documentation\IntelliSense\ASMX` folder do not work for WCF-based applications.</span></span> <span data-ttu-id="63ff0-189">GenASMXProxyAssembly.cmd スクリプトは Wsdl.exeを呼び出し、ASMX サービスのソース コード ファイルを生成します。</span><span class="sxs-lookup"><span data-stu-id="63ff0-189">The GenASMXProxyAssembly.cmd script calls Wsdl.exe, which generates source code files for the ASMX services.</span></span> <span data-ttu-id="63ff0-190">ASMX プロキシ ファイルには、さまざまなクラスとプロパティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="63ff0-190">The ASMX proxy files include different classes and properties.</span></span> <span data-ttu-id="63ff0-191">たとえば、ASMX ベースの Resource Web サービスには Resource クラスが含まれますが、WCF ベースの Resource サービスには Resource インターフェイス **、ResourceChannel** インターフェイス **、ResourceClient** クラスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="63ff0-191">For example, the ASMX-based Resource web service includes the **Resource** class, whereas the WCF-based Resource service includes the **Resource** interface, the **ResourceChannel** interface, and the **ResourceClient** class.</span></span> 
  
<span data-ttu-id="63ff0-p124">ASMX Web サービスと WCF サービスのために作成された恣意的な名前空間はどちらも同じなので、Intellisense 用の ProjectServerServices.xml ファイルはどちらのアセンブリでも動作します。たとえば、WCF ベースのプロキシ アセンブリでも ASMX ベースのプロキシ アセンブリでも、Resource サービスの名前空間は **SvcResource** です。もちろん、この名前空間の名前は変更できます。ただし、その名前はプロキシ アセンブリと ProjectServerServices.xml Intellisense ファイルで一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="63ff0-p124">The arbitrary namespaces created for both the ASMX web services and the WCF services are the same, so that the ProjectServerServices.xml file for IntelliSense works with either assembly. For example, the namespace of the Resource service in the WCF-based proxy assembly and in the ASMX-based proxy assembly is **SvcResource**. You can, of course, change the namespace names— if you ensure that they match in the proxy assembly and in the ProjectServerServices.xml IntelliSense file.</span></span>
  
<span data-ttu-id="63ff0-195">あるコード サンプルが PSI サービスの名前空間に別の名前 (**ProjectWebSvc** など) を使用している場合、IntelliSense が動作するためには、**SvcProject** を使用するようにそのサンプルを変更して、名前空間とプロキシ アセンブリを一致させる必要があります。</span><span class="sxs-lookup"><span data-stu-id="63ff0-195">If a code sample uses a different name for a PSI service namespace, for example **ProjectWebSvc**, for IntelliSense to work you must change the sample to use **SvcProject** so that the namespace matches the proxy assembly.</span></span> 
  
<span data-ttu-id="63ff0-196">WCF ベースのプロキシ アセンブリを使用する利点は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="63ff0-196">Advantages to using the WCF-based proxy assembly include the following:</span></span>
  
- <span data-ttu-id="63ff0-p125">ほとんどのソリューションを、Project Server コンピューターとは別のコンピューター上にあるプロキシ アセンブリで開発できます。ただし、個々のサービス参照の設定には、Project Server コンピューターでの開発が必要です。</span><span class="sxs-lookup"><span data-stu-id="63ff0-p125">You can develop most solutions with the proxy assembly on a different computer than the Project Server computer. Setting an individual service reference requires development on the Project Server computer.</span></span>
    
- <span data-ttu-id="63ff0-199">このプロキシ アセンブリにはすべての PSI サービス名前空間が含まれるので、複数のプロキシ ファイルを追加する必要がありません。</span><span class="sxs-lookup"><span data-stu-id="63ff0-199">The proxy assembly includes all PSI service namespaces, so you do not have to add multiple proxy files.</span></span>
    
- <span data-ttu-id="63ff0-200">ProjectServerServices.xml ファイルを ProjectServerServices.dll プロキシ アセンブリへの参照を設定するのと同じディレクトリに追加すれば、PSI クラスおよびメンバーに関する Intellisense 記述を取得できます。</span><span class="sxs-lookup"><span data-stu-id="63ff0-200">If you add the ProjectServerServices.xml file to the same directory where you set a reference to the ProjectServerServices.dll proxy assembly, you can get IntelliSense descriptions for the PSI classes and members.</span></span> <span data-ttu-id="63ff0-201">詳細については、2013 SDK ダウンロードのフォルダーにある [ReadMe_IntelliSense] ファイルProject `Documentation\IntelliSense` 参照してください。</span><span class="sxs-lookup"><span data-stu-id="63ff0-201">For more information, see the [ReadMe_IntelliSense] file in the  `Documentation\IntelliSense` folder of the Project 2013 SDK download.</span></span> 
    
<span data-ttu-id="63ff0-202">**図 2. Resource サービスのメソッドに対する IntelliSense の使用**</span><span class="sxs-lookup"><span data-stu-id="63ff0-202">**Figure 2. Using IntelliSense for a method in the Resource service**</span></span>

<span data-ttu-id="63ff0-203">![ReadResource メソッドに Intellisense を使用する ReadResource]メソッドに(media/pj15_PrerequisitesWCF_Intellisense.gif "Intellisense")を使用する</span><span class="sxs-lookup"><span data-stu-id="63ff0-203">![Using Intellisense for the ReadResource method](media/pj15_PrerequisitesWCF_Intellisense.gif "Using Intellisense for the ReadResource method")</span></span>
  
<span data-ttu-id="63ff0-p127">このプロキシ アセンブリを使用する場合の欠点は、ソリューションが大規模になることと、ソリューションと共にプロキシ アセンブリの配布とインストールが必要になることです。また、プロキシ アセンブリと Intellisense ファイルの中で同じ名前空間を使用する必要があります (ただし、スクリプトを修正して、独自のプロキシ アセンブリを作成し、別々の名前空間を使用するように ProjectServerServices.xml Intellisense ファイルを変更した場合は例外です)。</span><span class="sxs-lookup"><span data-stu-id="63ff0-p127">Disadvantages to using the proxy assembly are that the solution is larger and you must distribute and install the proxy assembly with the solution. You must also use the same namespaces that are in the proxy assembly and IntelliSense files, unless you change the script to build a proxy assembly and change the ProjectServerServices.xml IntelliSense file to use different namespaces.</span></span>
  
### <a name="adding-a-psi-proxy-file"></a><span data-ttu-id="63ff0-206">PSI プロキシ ファイルを追加する</span><span class="sxs-lookup"><span data-stu-id="63ff0-206">Adding a PSI proxy file</span></span>
<span data-ttu-id="63ff0-207"><a name="pj15_PrerequisitesWCF_AddingProxyFile"> </a></span><span class="sxs-lookup"><span data-stu-id="63ff0-207"><a name="pj15_PrerequisitesWCF_AddingProxyFile"> </a></span></span>

<span data-ttu-id="63ff0-208">2013 Project SDK のダウンロードには、プロキシ アセンブリの SvcUtil.exeコマンドによって生成されるソース ファイルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="63ff0-208">The Project 2013 SDK download includes the source files that are generated by the SvcUtil.exe command for the proxy assembly.</span></span> <span data-ttu-id="63ff0-209">ソース ファイルは、サブディレクトリSource.zipファイル  `Documentation\IntelliSense\WCF` に含めます。</span><span class="sxs-lookup"><span data-stu-id="63ff0-209">The source files are in the Source.zip file in the  `Documentation\IntelliSense\WCF` subdirectory.</span></span> <span data-ttu-id="63ff0-210">プロキシ アセンブリへの参照を設定する代わりに、1 つ以上のソース ファイルを別のソリューションにVisual Studioできます。</span><span class="sxs-lookup"><span data-stu-id="63ff0-210">Instead of setting a reference to the proxy assembly, you can add one or more of the source files to a Visual Studio solution.</span></span> <span data-ttu-id="63ff0-211">たとえば、Project サービスとリソース サービスを使用するには、wcf を追加します。Project.cs と wcf。ソリューションへの Resource.cs ファイル。</span><span class="sxs-lookup"><span data-stu-id="63ff0-211">For example, to use the Project service and the Resource service, add the wcf.Project.cs and wcf.Resource.cs files to the solution.</span></span> 
  
<span data-ttu-id="63ff0-p129">WCF では、それぞれの PSI サービスの主要なクラスが、インターフェイスによって定義され、そのメンバーにアクセスするためのクライアント クラス内で実装されます。たとえば、**SvcProject.Resource** インターフェイスは **SvcProject.ResourceClient** クラス内で実装されています。**ResourceClient** オブジェクトを、たとえば **resourceClient** という名前のクラス変数として定義するには、以下のコードを使用します。この例では、**SetClientEndpoints** メソッドによって、**basicHttp_Project** エンドポイントを使用する **resourceClient** オブジェクトが作成されます。このエンドポイントは app.config ファイルで定義されています。app.config ファイルの詳細については、「[サービス構成ファイルを追加する](#pj15_PrerequisitesWCF_AddConfig)」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="63ff0-p129">In WCF, the primary class in each PSI service is defined by an interface and implemented in a client class for access to the members. For example, the **SvcProject.Resource** interface is implemented in the **SvcProject.ResourceClient** class. To define a **ResourceClient** object as a class variable named **resourceClient**, for example, use the following code. In the example, the **SetClientEndpoints** method creates a **resourceClient** object that uses the **basicHttp_Project** endpoint, which is defined in the app.config file. For more information about the app.config file, see the [Adding a service configuration file](#pj15_PrerequisitesWCF_AddConfig) section.</span></span> 
  
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
> <span data-ttu-id="63ff0-217">PSI プロキシ アセンブリを使用する場合も、プロキシ ファイルを追加して **SvcResource** という名前の Project サービス参照を追加する場合も、**resourceClient** オブジェクトの作成と廃棄には同じコードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="63ff0-217">Whether you use a PSI proxy assembly or add a proxy file for a Project service reference named **SvcResource**, you would use the same code to create and dispose a **resourceClient** object.</span></span> 
  
### <a name="adding-a-service-reference"></a><span data-ttu-id="63ff0-218">サービス参照の追加</span><span class="sxs-lookup"><span data-stu-id="63ff0-218">Adding a service reference</span></span>
<span data-ttu-id="63ff0-219"><a name="pj15_PrerequisitesWCF_AddingServiceReference"> </a></span><span class="sxs-lookup"><span data-stu-id="63ff0-219"><a name="pj15_PrerequisitesWCF_AddingServiceReference"> </a></span></span>

<span data-ttu-id="63ff0-220">WCF ベースのプロキシ アセンブリを使用したり、PSI サービスのプロキシ ファイルを追加したりしない場合は、1 つ以上のサービス参照を Visual Studio 内で直接設定できます。</span><span class="sxs-lookup"><span data-stu-id="63ff0-220">If you do not use the WCF-based proxy assembly or add a proxy file for a PSI service, you can set one or more individual service references directly in Visual Studio.</span></span> <span data-ttu-id="63ff0-221">次の手順の手順 1 を使用して、更新されたプロキシ ファイルを作成し、Project SDK のダウンロードに含まれるスクリプト `Documentation\IntelliSense\WCF\GenWCFProxyAssembly.cmd` を準備することもできます。</span><span class="sxs-lookup"><span data-stu-id="63ff0-221">You can also use step 1 of the following procedure to create updated proxy files, to prepare for the  `Documentation\IntelliSense\WCF\GenWCFProxyAssembly.cmd` script that is included in the Project 2013 SDK download.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="63ff0-p131">サービス参照を設定するには、Project Server コンピューターで Visual Studio を使用する必要があります。Visual Studio 内でサービス参照を直接追加するよりも、ProjectServerServices.dll プロキシ アセンブリを使用するか、プロキシ ソース ファイルを追加することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="63ff0-p131">To set a service reference, you must use Visual Studio on the Project Server computer. We recommend that you use the ProjectServerServices.dll proxy assembly or add proxy source files, instead of directly adding service references in Visual Studio.</span></span> 
  
<span data-ttu-id="63ff0-224">次の手順は、サーバーのテスト インストールを実行しているコンピューターで Visual Studio 2012 を使用してサービス参照を設定するProjectします。</span><span class="sxs-lookup"><span data-stu-id="63ff0-224">The following steps show how to set a service reference by using Visual Studio 2012 on a computer running a test installation of Project Server:</span></span>
  
1. <span data-ttu-id="63ff0-225">バックエンド WCF サービスへのアクセスを取得するには、Project Server コンピューターで Visual Studio を実行します。</span><span class="sxs-lookup"><span data-stu-id="63ff0-225">To get access to the back-end WCF services, run Visual Studio on the Project Server computer.</span></span>
    
2. <span data-ttu-id="63ff0-226">**ソリューション エクスプローラー** で、[**参照設定**] フォルダーを右クリックし、[**サービス参照の追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="63ff0-226">In **Solution Explorer**, right-click the **References** folder, and then choose **Add Service Reference**.</span></span> 
    
3. <span data-ttu-id="63ff0-227">[サービス **参照の追加]** ダイアログ ボックスの [アドレス] テキスト ボックスに https://localhost:32843/ _「GUID_/psi/ _ServiceName_.svc」と入力し、Enter キーを **押します**。</span><span class="sxs-lookup"><span data-stu-id="63ff0-227">In the **Add Service Reference** dialog box, in the **Address** text box, type https://localhost:32843/ _GUID_/psi/ _ServiceName_.svc, and then press **Enter**.</span></span> <span data-ttu-id="63ff0-228">GUID _を_ 534c37eb00d74ccfadcecf9827e95239 などの Project Server サービス アプリケーションの仮想ディレクトリ名に置き換える。</span><span class="sxs-lookup"><span data-stu-id="63ff0-228">Replace  _GUID_ with the virtual directory name of the Project Server service application, such as 534c37eb00d74ccfadcecf9827e95239.</span></span> <span data-ttu-id="63ff0-229">_ServiceName を Resource_ などのサービスの名前に置き換えてください (図 3 を参照)。</span><span class="sxs-lookup"><span data-stu-id="63ff0-229">Replace  _ServiceName_ with the name of the service, such as Resource (see Figure 3).</span></span> 
    
   <span data-ttu-id="63ff0-230">Project Server Service 仮想ディレクトリの名前は、以下のどちらかの方法で取得できます。</span><span class="sxs-lookup"><span data-stu-id="63ff0-230">You can get the name of the Project Server Service virtual directory in one of the following ways:</span></span>
    
   - <span data-ttu-id="63ff0-231">ブラウザーで SharePoint 2013 サーバーの全体管理アプリケーションを開きます。</span><span class="sxs-lookup"><span data-stu-id="63ff0-231">Open the SharePoint 2013 Central Administration application in your browser.</span></span> <span data-ttu-id="63ff0-232">[**サービス アプリケーションの管理**] をクリックし、目的の Project Server PSI Service アプリケーションをクリックします。</span><span class="sxs-lookup"><span data-stu-id="63ff0-232">Choose **Manage service applications**, and then choose the Project Server PSI Service application that you want.</span></span> <span data-ttu-id="63ff0-233">たとえば、[**ProjectServerService**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="63ff0-233">For example, choose **ProjectServerService**.</span></span> <span data-ttu-id="63ff0-234">[サイトの管理] ページProject Web Appには、仮想ディレクトリ名が含まれます。</span><span class="sxs-lookup"><span data-stu-id="63ff0-234">The URL of the Manage Project Web App Sites page contains the virtual directory name.</span></span> <span data-ttu-id="63ff0-235">たとえば、仮想ディレクトリ名は次のようになります  `https://ServerName:8080/_admin/pwa/managepwa.aspx?appid=534c37eb-00d7-4ccf-adce-cf9827e95239`  `534c37eb00d74ccfadcecf9827e95239` (ディレクトリ名にはダッシュはありません)。</span><span class="sxs-lookup"><span data-stu-id="63ff0-235">For example, in  `https://ServerName:8080/_admin/pwa/managepwa.aspx?appid=534c37eb-00d7-4ccf-adce-cf9827e95239`, the virtual directory name is  `534c37eb00d74ccfadcecf9827e95239` (the directory name contains no dashes).</span></span> 
    
   - <span data-ttu-id="63ff0-p134">Project Server コンピューターで [**インターネット インフォメーション サービス (IIS) マネージャー**] ダイアログ ボックスを開きます。[**接続**] ウィンドウの [**SharePoint Web サービス**] ノードを展開し、PSI フォルダーを含むディレクトリが見つかるまで、その下位にあるサービス仮想ディレクトリを展開していきます。見つかったディレクトリを選択し、[**操作**] ウィンドウの [**詳細設定**] をクリックして、そのディレクトリ名を [**仮想パス**] フィールドにコピーします。</span><span class="sxs-lookup"><span data-stu-id="63ff0-p134">Open the **Internet Information Services (IIS) Manager** dialog box on the Project Server computer. Expand the **SharePoint Web Services** node in the **Connections** pane, and then expand the service virtual directories below that, until you find the directory that includes a PSI folder. Select the directory, choose **Advanced Settings** in the **Actions** pane, and then copy the directory name in the **Virtual Path** field.</span></span> 
    
      > [!NOTE]
      > <span data-ttu-id="63ff0-239">複数の Project Server Service 仮想ディレクトリが存在することがあります。</span><span class="sxs-lookup"><span data-stu-id="63ff0-239">There can be more than one Project Server Service virtual directory.</span></span> <span data-ttu-id="63ff0-240">必要なインスタンスを含む仮想ディレクトリをProject Web Appしてください。</span><span class="sxs-lookup"><span data-stu-id="63ff0-240">Ensure that you choose the virtual directory that contains the Project Web App instance that you want.</span></span> 
  
   - <span data-ttu-id="63ff0-241">**get-SPServiceApplication** コマンドレットは、Windows PowerShell 2013 と共にインストールされているSharePoint使用します。</span><span class="sxs-lookup"><span data-stu-id="63ff0-241">Use the **get-SPServiceApplication** cmdlet in Windows PowerShell that is installed with SharePoint 2013.</span></span> <span data-ttu-id="63ff0-242">タスク バーの [**スタート**] ボタンをクリックし、[**すべてのプログラム**]、[**Microsoft SharePoint 2013 製品**]、[**SharePoint 2013 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="63ff0-242">On the taskbar **Start** menu, choose **All Programs**, choose **Microsoft SharePoint 2013 Products**, and then choose **SharePoint 2013 Management Shell**.</span></span> <span data-ttu-id="63ff0-243">以下は、[**SharePoint 2013get- 管理シェル**] ウィンドウで定義済みサービス アプリケーション (GUID は異なります) に対してコマンドを実行した結果です。</span><span class="sxs-lookup"><span data-stu-id="63ff0-243">Following is the command and the results in the **SharePoint 2013get- Management Shell** window for the defined service applications (your GUIDs will be different).</span></span> <span data-ttu-id="63ff0-244">Project Server サービス アプリケーションの GUID をコピーします。</span><span class="sxs-lookup"><span data-stu-id="63ff0-244">Copy the GUID for the Project Server service application.</span></span> 
    
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

      <span data-ttu-id="63ff0-245">Project Server Service アプリケーションの完全な名前がわかる場合は、その名前に基づいて GUID 値を取得できます。次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="63ff0-245">If you know the full name of the Project Server Service application, you can use it to get the GUID value, for example:</span></span>
    
        ```powershell
        PS > $projectService = "ProjectServerService"
        PS > (get-SPServiceApplication -Name $projectService).Id
        Guid
        ----
        534c37eb-00d7-4ccf-adce-cf9827e95239
       ```

      > [!NOTE]
      > <span data-ttu-id="63ff0-246">GUID からダッシュを削除すると仮想ディレクトリ名になります。</span><span class="sxs-lookup"><span data-stu-id="63ff0-246">Remove the dashes in the GUID to get the virtual directory name.</span></span> 
  
   <span data-ttu-id="63ff0-247">サーバー サービスの標準のような URL `https://localhost:32843/534c37eb00d74ccfadcecf9827e95239/PSI/Resource.svc` Projectです。</span><span class="sxs-lookup"><span data-stu-id="63ff0-247">URLs such as  `https://localhost:32843/534c37eb00d74ccfadcecf9827e95239/PSI/Resource.svc` are standard for Project Server services.</span></span> 
    
4. <span data-ttu-id="63ff0-248">サービス参照の解決後、[**名前空間**] テキスト ボックスに参照名を入力します。</span><span class="sxs-lookup"><span data-stu-id="63ff0-248">After the service reference resolves, type the reference name in the **Namespace** text box.</span></span> <span data-ttu-id="63ff0-249">2013 年 2013 Projectのコード例では、任意の名前空間名 **Svc _ServiceName を使用します_**。</span><span class="sxs-lookup"><span data-stu-id="63ff0-249">Code examples in the Project 2013 developer documentation use the arbitrary namespace name **Svc _ServiceName_**.</span></span> <span data-ttu-id="63ff0-250">たとえば、このコード サンプルの Resource サービスは **SvcResource** という名前になっています。</span><span class="sxs-lookup"><span data-stu-id="63ff0-250">For example, the Resource service in the code examples is named **SvcResource**.</span></span>
    
    <span data-ttu-id="63ff0-251">**図 3. WCF ベースの Resource サービス参照の追加**</span><span class="sxs-lookup"><span data-stu-id="63ff0-251">**Figure 3. Adding the WCF-based Resource service reference**</span></span>

    <span data-ttu-id="63ff0-252">![WCF ベースのリソース サービス参照の追加](media/pj15_PrerequisitesWCF_AddSvcReference.gif "WCF ベースのリソース サービス参照の追加")</span><span class="sxs-lookup"><span data-stu-id="63ff0-252">![Adding the WCF-based Resource service reference](media/pj15_PrerequisitesWCF_AddSvcReference.gif "Adding the WCF-based Resource service reference")</span></span>
  
5. <span data-ttu-id="63ff0-253">web.config Service ディレクトリProject一時ファイルを元のファイルに置き換え (web.config に変更)、再実行します `iisreset` 。</span><span class="sxs-lookup"><span data-stu-id="63ff0-253">Replace the temporary web.config file in the Project Service directory with the original (renamed to web.config), and then rerun  `iisreset`.</span></span>
    
## <a name="setting-other-references"></a><span data-ttu-id="63ff0-254">その他の参照を設定する</span><span class="sxs-lookup"><span data-stu-id="63ff0-254">Setting other references</span></span>
<span data-ttu-id="63ff0-255"><a name="pj15_PrerequisitesWCF_OtherReferences"> </a></span><span class="sxs-lookup"><span data-stu-id="63ff0-255"><a name="pj15_PrerequisitesWCF_OtherReferences"> </a></span></span>

<span data-ttu-id="63ff0-256">Projectサーバー アプリケーションは、多くの場合、2013 Web サービスなどのSharePointサービスを使用します。</span><span class="sxs-lookup"><span data-stu-id="63ff0-256">Project Server applications often use other services, such as SharePoint 2013 web services.</span></span> <span data-ttu-id="63ff0-257">ほかのサービスや参照が必要な場合は、コード サンプルにそれらが記されています。</span><span class="sxs-lookup"><span data-stu-id="63ff0-257">If other services or references are required, they are noted in the code example.</span></span>
  
<span data-ttu-id="63ff0-258">コード サンプルのローカル参照は、サンプルの上部の **using** ステートメントに示されています。</span><span class="sxs-lookup"><span data-stu-id="63ff0-258">Local references for the code sample are listed in **using** statements at the top of the sample.</span></span> 
  
1. <span data-ttu-id="63ff0-259">**ソリューション エクスプローラー** で、[**参照設定**] フォルダーを右クリックし、[**参照の追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="63ff0-259">In **Solution Explorer**, right-click the **References** folder, and then choose **Add Reference**.</span></span>
    
2. <span data-ttu-id="63ff0-p139">[**参照**] をクリックして、以前にコピーした Project Server の DLL を格納した場所を参照します。必要な DLL を選択し、[**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="63ff0-p139">Choose **Browse**, and then browse to the location where you stored the Project Server DLLs that you copied previously. Choose the DLLs that you want, and then choose **OK**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="63ff0-262">開発用コンピューター上のアセンブリのバージョンがターゲット Project Server コンピューターのものと厳密に一致していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="63ff0-262">Ensure that the assembly versions on your development computer exactly match those on the target Project Server computer.</span></span> 
  
## <a name="adding-a-service-configuration-file"></a><span data-ttu-id="63ff0-263">サービス構成ファイルを追加する</span><span class="sxs-lookup"><span data-stu-id="63ff0-263">Adding a service configuration file</span></span>
<span data-ttu-id="63ff0-264"><a name="pj15_PrerequisitesWCF_AddConfig"> </a></span><span class="sxs-lookup"><span data-stu-id="63ff0-264"><a name="pj15_PrerequisitesWCF_AddConfig"> </a></span></span>

<span data-ttu-id="63ff0-p140">アプリケーションがプログラムによって WCF サービスを構成する場合、サービス構成ファイルは使用されません。それ以外の場合、Windows アプリケーションまたはコンソール アプリケーションでは app.config ファイルの **system.serviceModel** 要素を使用し、Web アプリケーションでは web.config ファイルの **system.serviceModel** をインクルードします。app.config ファイルの使用方法や、WCF サービスをプログラムで構成する方法については、「[[ウォークスルー] WCF を使用して PSI アプリケーションを開発する](https://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="63ff0-p140">If an application programmatically configures the WCF services, it does not use a service configuration file. Otherwise, a Windows application or console application uses the **system.serviceModel** element in an app.config file; a web application includes **system.serviceModel** in web.config. For more information about using an app.config file or programmatically configuring the WCF services, see [Walkthrough: Developing PSI applications using WCF](https://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx).</span></span>
  
<span data-ttu-id="63ff0-267">サービス プロキシ ソース ファイルを生成すると、SvcUtil.exe コマンドは、app.config ファイルまたは web.config ファイルの既定 **の system.serviceModel** 要素の基礎となる output.config ファイルも作成します。</span><span class="sxs-lookup"><span data-stu-id="63ff0-267">When it generates a service proxy source file, the SvcUtil.exe command also creates an output.config file that is the basis for the default **system.serviceModel** element in an app.config file or web.config file.</span></span> <span data-ttu-id="63ff0-268">2013 Project SDK のダウンロードには、2013 SDK のサンプル output.configが含まれています `Documentation\IntelliSense\WCF\Source.zip` 。</span><span class="sxs-lookup"><span data-stu-id="63ff0-268">The Project 2013 SDK download includes a sample output.config file in  `Documentation\IntelliSense\WCF\Source.zip`.</span></span> <span data-ttu-id="63ff0-269">たとえば、Resource サービスoutput.config作成SvcUtil.exe既定のファイルには、BasicHttpBinding_Resource と BasicHttpBinding_Resource1 という名前の 2 つの **バインドが含BasicHttpBinding_Resource1。**</span><span class="sxs-lookup"><span data-stu-id="63ff0-269">For example, the default output.config file that SvcUtil.exe creates for the Resource service includes two bindings, named **BasicHttpBinding_Resource** and **BasicHttpBinding_Resource1**.</span></span> <span data-ttu-id="63ff0-270">クライアント **要素には** 、2 つの既定のエンドポイントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="63ff0-270">The **client** element includes two default endpoints.</span></span> <span data-ttu-id="63ff0-271">1 つのエンドポイントは、ポート 32843 の HTTP アドレスへのセキュリティで保護されたアクセス用であり、もう 1 つはポート 32843 での通常のアクセス用です。次に示します。</span><span class="sxs-lookup"><span data-stu-id="63ff0-271">One endpoint is for the secure access to the HTTP address on port 32843 and the other is for normal access on port 32843, as follows:</span></span> 
  
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

<span data-ttu-id="63ff0-p142">PSI サービス構成では、既定のバインドやエンドポイントを使用しません。Project Server では、バックエンド サービスの呼び出しでルーターとして動作するフロントエンド ProjectServer.svc を介してアプリケーションが PSI サービスにアクセスする必要があります。app.config ファイルを作成するには、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="63ff0-p142">PSI service configuration does not use the default bindings and endpoints. Project Server requires that applications access PSI services through the front-end ProjectServer.svc, which acts as a router for calls to the back-end services. To create the app.config file, do the following steps:</span></span>
  
1. <span data-ttu-id="63ff0-275">ProjectServerServices.dll プロキシ アセンブリへの参照を設定したり、あるサービス用のプロキシ ソース ファイルを追加したりする場合、アプリケーションには app.config ファイルが含まれません。</span><span class="sxs-lookup"><span data-stu-id="63ff0-275">If you set a reference to the ProjectServerServices.dll proxy assembly, or add the proxy source file for a service, the application does not contain an app.config file.</span></span> <span data-ttu-id="63ff0-276">その場合は、新しいアイテムを Visual Studio に追加します。</span><span class="sxs-lookup"><span data-stu-id="63ff0-276">Add a new item to the Visual Studio project.</span></span> <span data-ttu-id="63ff0-277">[新しい **アイテムの追加]** ダイアログ ボックスで、[ **アプリケーション** 構成ファイル] テンプレートを選択し、そのテンプレートに名前を付app.config、[追加] を **選択します**。</span><span class="sxs-lookup"><span data-stu-id="63ff0-277">In the **Add New Item** dialog box, choose the **Application Configuration File** template, name it app.config, and then choose **Add**.</span></span>
    
2. <span data-ttu-id="63ff0-278">app.config ファイルのすべてのテキストを削除し、以下のコードをこのファイルにコピーします。</span><span class="sxs-lookup"><span data-stu-id="63ff0-278">Delete all text in the app.config file, and then copy the following code into the file.</span></span> <span data-ttu-id="63ff0-279">サービス エンドポイントごとに同じバインド (たとえば  `basicHttpConf` ) を使用できます。</span><span class="sxs-lookup"><span data-stu-id="63ff0-279">You can use the same binding, for example  `basicHttpConf`, for each service endpoint.</span></span> <span data-ttu-id="63ff0-280">複数のバインドを使用する場合 (たとえば、HTTP と HTTPS の両プロトコルをバインドする場合) は、プロトコルごとにバインドを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="63ff0-280">If you want to use more than one binding, for example, to bind both HTTP and HTTPS protocols, you must create a binding for each protocol.</span></span>
    
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

3. <span data-ttu-id="63ff0-281">クライアント `ServerName/ProjectServerName` エンドポイント のアドレスを、サーバーとインスタンスの名前に置きProject Web Appします。</span><span class="sxs-lookup"><span data-stu-id="63ff0-281">Replace  `ServerName/ProjectServerName` in the client endpoint address with the name of your server and Project Web App instance.</span></span> 
    
4. <span data-ttu-id="63ff0-282">リソース  `ServiceName` などの PSI サービスの名前に置き換える。</span><span class="sxs-lookup"><span data-stu-id="63ff0-282">Replace  `ServiceName` with the name of the PSI service, such as Resource.</span></span> <span data-ttu-id="63ff0-283">たとえば、次のようにサービス名の 3 つのインスタンスすべてを確実に置き換えてください。</span><span class="sxs-lookup"><span data-stu-id="63ff0-283">Ensure that you replace all three instances of the service name, for example:</span></span>
    
    ```XML
        <endpoint address="https://myserver/pwa/_vti_bin/PSI/ProjectServer.svc"
            behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
            bindingConfiguration="basicHttpConf" 
            contract="SvcResource.Resource"
            name="basicHttp_Resource" />
    ```

5. <span data-ttu-id="63ff0-p146">複数の PSI サービスを使用するには、サービスごとに、またサービスが使用する **binding** ごとに、1 つの **endpoint** 要素を作成します。たとえば、以下のエンドポイントでは、Project サービスと QueueSystem サービスで基本的な HTTP バインドを使用するようにクライアントを構成しています。</span><span class="sxs-lookup"><span data-stu-id="63ff0-p146">To use more than one PSI service, create one **endpoint** element for each service, and for each **binding** element that service uses. For example, the following endpoints configure the client to use the basic HTTP binding for the Project service and the QueueSystem service.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="63ff0-286">アプリケーションの実行時に、サーバーがビジー状態である、または HTTP 要求が許可されていないことを示すエラーが表示される場合は、app.config ファイルのエンドポイント アドレスが正しいことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="63ff0-286">If you run an application and get an error that the server is too busy, or that the HTTP request is unauthorized, ensure that the endpoint addresses are correct in the app.config file.</span></span> 
  
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

<span data-ttu-id="63ff0-287">Visual Studio の **WCF サービス構成エディター** ([**ツール**] メニューにあります) を使用すると、app.config ファイルを編集できます。</span><span class="sxs-lookup"><span data-stu-id="63ff0-287">You can edit an app.config file by using the **WCF Service Configuration Editor** in Visual Studio (on the **Tools** menu).</span></span> <span data-ttu-id="63ff0-288">図 4 は、[**Microsoft サービス構成エディター**] ダイアログ ボックスで **contract** 要素を設定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="63ff0-288">Figure 4 shows how to set the **contract** element in the **Microsoft Service Configuration Editor** dialog box.</span></span> <span data-ttu-id="63ff0-289">ソリューションで PSI プロキシ アセンブリを使用している場合は、ProjectServerServices.dllソリューションのディレクトリでVisual Studio `bin\debug` します。</span><span class="sxs-lookup"><span data-stu-id="63ff0-289">If the solution is using the PSI proxy assembly, open ProjectServerServices.dll in the  `bin\debug` directory of the Visual Studio solution.</span></span> <span data-ttu-id="63ff0-290">[**コントラクト型ブラウザー**] ダイアログ ボックスに、WCF サービス コントラクトのすべてが表示されます (図 5 を参照)。</span><span class="sxs-lookup"><span data-stu-id="63ff0-290">The **Contract Type Browser** dialog box shows all of the WCF service contracts (see Figure 5).</span></span> 
  
<span data-ttu-id="63ff0-291">**図 4. WCF サービス構成エディターの使用**</span><span class="sxs-lookup"><span data-stu-id="63ff0-291">**Figure 4. Using the WCF Service Configuration Editor**</span></span>

<span data-ttu-id="63ff0-292">![WCF サービス構成エディターを使用した](media/pj15_PrerequisitesWCF_ServiceConfigurationEditor.gif "WCF サービス構成エディターの使用")</span><span class="sxs-lookup"><span data-stu-id="63ff0-292">![Using the WCF Service Configuration Editor](media/pj15_PrerequisitesWCF_ServiceConfigurationEditor.gif "Using the WCF Service Configuration Editor")</span></span>
  
<span data-ttu-id="63ff0-293">ソリューションで wcfResource.cs などのサービス プロキシ ファイルを使用している場合は、アプリケーションをコンパイルし、ディレクトリで実行可能ファイルを開  `bin\debug` きます。</span><span class="sxs-lookup"><span data-stu-id="63ff0-293">If the solution is using a service proxy file, such as wcfResource.cs, compile the application and then open the executable file in the  `bin\debug` directory.</span></span> <span data-ttu-id="63ff0-294">app.config ファイルの編集の詳細については、「[[ウォークスルー] WCF を使用して PSI アプリケーションを開発する](https://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="63ff0-294">For more information about editing the app.config file, see [Walkthrough: Developing PSI applications using WCF](https://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx).</span></span>
  
<span data-ttu-id="63ff0-295">**図 5. WCF サービス構成エディターでのコントラクト型ブラウザーの使用**</span><span class="sxs-lookup"><span data-stu-id="63ff0-295">**Figure 5. Using the Contract Type Browser in the WCF Service Configuration Editor**</span></span>

<span data-ttu-id="63ff0-296">![コントラクトの種類ブラウザーを使用](media/pj15_PrerequisitesWCF_ContractTypeBrowser.gif "したコントラクトの種類ブラウザーの使用")</span><span class="sxs-lookup"><span data-stu-id="63ff0-296">![Using the Contract Type Browser](media/pj15_PrerequisitesWCF_ContractTypeBrowser.gif "Using the Contract Type Browser")</span></span>
  
## <a name="using-multiple-authentication"></a><span data-ttu-id="63ff0-297">複数の認証を使用する</span><span class="sxs-lookup"><span data-stu-id="63ff0-297">Using multiple authentication</span></span>
<span data-ttu-id="63ff0-298"><a name="pj15_PrerequisitesWCF_ClaimsMultiAuth"> </a></span><span class="sxs-lookup"><span data-stu-id="63ff0-298"><a name="pj15_PrerequisitesWCF_ClaimsMultiAuth"> </a></span></span>

<span data-ttu-id="63ff0-299">サーバーユーザーによるオンプレミスProject認証は、Windows認証またはフォーム認証の場合も、SharePoint でクレーム処理を行います。</span><span class="sxs-lookup"><span data-stu-id="63ff0-299">Authentication of on-premises Project Server users, whether by Windows authentication or Forms authentication, is done through claims processing in SharePoint.</span></span> <span data-ttu-id="63ff0-300">複数認証とは、プロビジョニングされている Web アプリケーションがProject Web App認証とフォーム ベース認証Windows両方をサポートします。</span><span class="sxs-lookup"><span data-stu-id="63ff0-300">Multiple authentication means that the web application on which Project Web App is provisioned supports both Windows authentication and Forms-based authentication.</span></span> <span data-ttu-id="63ff0-301">この場合、Windows 認証を使用する WCF サービスへの呼び出しは、クレーム プロセスで認証するユーザーの種類を決定できないので、次のエラーで失敗します。</span><span class="sxs-lookup"><span data-stu-id="63ff0-301">If that is the case, any call to a WCF service that uses Windows authentication will fail with the following error, because the claims process cannot determine which type of user to authenticate:</span></span>
  
`The server was unable to process the request due to an internal error. For more information about the error, either turn on Include ExceptionDetailInFaults (either from ServiceBehaviorAttribute or from the <serviceDebug> configuration behavior) on the server in order to send the exception information back to the client, or turn on tracing as per the Microsoft .NET Framework 3.0 SDK documentation and inspect the server trace logs.`

<span data-ttu-id="63ff0-p150">WCF のこの問題を修正するには、PSI メソッドのすべての呼び出しをそれぞれの PSI サービスに対して定義される **OperationContextScope** 内に置く必要があります。ただし、複数のサービスに対するスコープを入れ子にしないでください。たとえば、Resource サービスと Project サービスを使用する際には、それぞれの呼び出しセットを各自のスコープ内に置く必要があります。</span><span class="sxs-lookup"><span data-stu-id="63ff0-p150">To fix the problem for WCF, all calls to PSI methods should be within an **OperationContextScope** that is defined for each PSI service. Do not nest scopes for multiple services; for example, when using calls to the Resource and Project services, each set of calls should be within its own scope.</span></span> 
  
<span data-ttu-id="63ff0-304">以下の例では、アプリケーションのどの **OperationContextScope** セクションからでも **DisableFormsAuth** メソッドを呼び出せます。</span><span class="sxs-lookup"><span data-stu-id="63ff0-304">In the following example, the **DisableFormsAuth** method can be called from every **OperationContextScope** section in an application.</span></span> <span data-ttu-id="63ff0-305">このメソッドは、以前にフォーム認証を無効にしたヘッダー値を削除し  _、isWindowsAuth_ パラメーターが false の場合にフォーム認証を続行 **できます**。</span><span class="sxs-lookup"><span data-stu-id="63ff0-305">The method removes any header value that previously disabled Forms authentication, so that Forms authentication can proceed if the  _isWindowsAuth_ parameter is **false**.</span></span> <span data-ttu-id="63ff0-306">_isWindowsAuth が_ true **の場合\*\*\*\*、DisableFormsAuth** メソッドはフォーム認証を無効にします。</span><span class="sxs-lookup"><span data-stu-id="63ff0-306">If  _isWindowsAuth_ is **true**, the **DisableFormsAuth** method disables Forms authentication.</span></span> 
  
<span data-ttu-id="63ff0-307">**WcfSample** メソッド内の **projectClient** オブジェクトは、PSI の **SvcProject.ProjectClient** クラスのインスタンスです。</span><span class="sxs-lookup"><span data-stu-id="63ff0-307">In the **WcfSample** method, the **projectClient** object is an instance of the PSI **SvcProject.ProjectClient** class.</span></span> 
  
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
> <span data-ttu-id="63ff0-p152">**OperationContextScope** 内での PSI 呼び出しが必要になるのは、複数認証の環境で動作するアプリケーションのみです。Project Server で Windows 認証のみを使用する場合、スコープの設定や、フォーム認証を無効にする Web 要求ヘッダーの追加は不要です。</span><span class="sxs-lookup"><span data-stu-id="63ff0-p152">Making PSI calls within an **OperationContextScope** is required only for applications that run in a multiple authentication environment. If Project Server uses only Windows authentication, it is not necessary to set a scope and add a web request header that disables Forms authentication.</span></span> 
> 
> <span data-ttu-id="63ff0-310">ASMX ベースのアプリケーションの場合は、修正方法が異なります。</span><span class="sxs-lookup"><span data-stu-id="63ff0-310">The fix for an ASMX-based application is different.</span></span> <span data-ttu-id="63ff0-311">詳細については、「AsMXベースのコード サンプルの前提条件」の「複数認証の使用」[セクション](prerequisites-for-asmx-based-code-samples-in-project.md)を参照Project。</span><span class="sxs-lookup"><span data-stu-id="63ff0-311">For more information, see the  *Using multiple-authentication*  section in [Prerequisites for ASMX-based code samples in Project](prerequisites-for-asmx-based-code-samples-in-project.md).</span></span> 
  
## <a name="changing-values-of-generic-constants"></a><span data-ttu-id="63ff0-312">一般的な定数の値を変更する</span><span class="sxs-lookup"><span data-stu-id="63ff0-312">Changing values of generic constants</span></span>
<span data-ttu-id="63ff0-313"><a name="pj15_PrerequisitesWCF_ChangeValues"> </a></span><span class="sxs-lookup"><span data-stu-id="63ff0-313"><a name="pj15_PrerequisitesWCF_ChangeValues"> </a></span></span>

<span data-ttu-id="63ff0-314">大部分のサンプルには、サンプルが環境で正しく動作するために更新する必要がある 1 つ以上の変数があります。</span><span class="sxs-lookup"><span data-stu-id="63ff0-314">Most samples have one or more variables that you must update for the sample to work properly in your environment.</span></span> <span data-ttu-id="63ff0-315">次の例では、SSL がインストールされている場合に HTTP プロトコルではなく HTTPS プロトコルを使用します。</span><span class="sxs-lookup"><span data-stu-id="63ff0-315">In the following example, if you have SSL installed, use the HTTPS protocol instead of the HTTP protocol.</span></span> <span data-ttu-id="63ff0-316">_ServerName を_ 使用しているサーバーの名前に置き換える。</span><span class="sxs-lookup"><span data-stu-id="63ff0-316">Replace  _ServerName_ with the name of the server that you are using.</span></span> <span data-ttu-id="63ff0-317">_ProjectServerName を_、プロジェクト サーバー サイトの仮想ディレクトリ名 (ディレクトリ名など) に置き換PWA。</span><span class="sxs-lookup"><span data-stu-id="63ff0-317">Replace  _ProjectServerName_ with the virtual directory name of your project server site, such as PWA.</span></span> 
  
```cs
const string PROJECT_SERVER_URI = "https://ServerName/ProjectServerName/";
```

<span data-ttu-id="63ff0-318">ほかに変更が必要な変数があれば、コード サンプルの上部に記載されています。</span><span class="sxs-lookup"><span data-stu-id="63ff0-318">Any other variables that you must change are noted at the top of the code example.</span></span>
  
## <a name="verifying-the-results"></a><span data-ttu-id="63ff0-319">結果を確認する</span><span class="sxs-lookup"><span data-stu-id="63ff0-319">Verifying the results</span></span>
<span data-ttu-id="63ff0-320"><a name="pj15_PrerequisitesWCF_Verify"> </a></span><span class="sxs-lookup"><span data-stu-id="63ff0-320"><a name="pj15_PrerequisitesWCF_Verify"> </a></span></span>

<span data-ttu-id="63ff0-321">コード サンプルの結果の取得と解釈は、必ずしも簡単ではありません。</span><span class="sxs-lookup"><span data-stu-id="63ff0-321">Getting and interpreting results from a code sample is not always straightforward.</span></span> <span data-ttu-id="63ff0-322">たとえば、プロジェクトを作成する場合は、プロジェクトがプロジェクトの [センター] ページに表示される前にProject発行するProject Web App。</span><span class="sxs-lookup"><span data-stu-id="63ff0-322">For example, if you create a project, you must publish the project before it can appear on the Project Center page in Project Web App.</span></span>
  
<span data-ttu-id="63ff0-323">コード サンプルの結果は、いくつかの方法で確認できます。たとえば、次のような方法があります。</span><span class="sxs-lookup"><span data-stu-id="63ff0-323">You can verify code sample results in several ways, for example:</span></span>
  
- <span data-ttu-id="63ff0-324">2013 Project Professional 2013 クライアントを使用して、Project サーバー コンピューターからプロジェクトを開き、必要なアイテムを表示します。</span><span class="sxs-lookup"><span data-stu-id="63ff0-324">Use the Project Professional 2013 client to open the project from the Project Server computer, and view the items that you want.</span></span>
    
- <span data-ttu-id="63ff0-325">発行済みプロジェクトは、Project ( ) の [センター] ページProject Web App表示 `https://ServerName/ProjectServerName/projects.aspx` します。</span><span class="sxs-lookup"><span data-stu-id="63ff0-325">View published projects on the Project Center page of Project Web App ( `https://ServerName/ProjectServerName/projects.aspx`).</span></span>
    
- <span data-ttu-id="63ff0-326">[キュー ログ] を表示Project Web App。</span><span class="sxs-lookup"><span data-stu-id="63ff0-326">View the Queue log in Project Web App.</span></span> <span data-ttu-id="63ff0-327">[サーバーの設定] ページを開き (右上隅にある **[設定]** アイコンを選択し、[個人用のジョブ] セクション ( ) の [マイ キューに入っているジョブ]**を設定** します `https://ServerName/ProjectServerName/MyJobs.aspx` 。</span><span class="sxs-lookup"><span data-stu-id="63ff0-327">Open the Server Settings page (choose the **Settings** icon in the top-right corner), and then choose **My Queued Jobs** under the **Personal Settings** section (  `https://ServerName/ProjectServerName/MyJobs.aspx`).</span></span> <span data-ttu-id="63ff0-328">[**表示**] ドロップダウン リストでは、ジョブの状態による並べ替えができます。</span><span class="sxs-lookup"><span data-stu-id="63ff0-328">In the **View** drop-down list, you can sort by the job status.</span></span> <span data-ttu-id="63ff0-329">既定の状態は [**進行中または失敗した過去 1 週間のジョブ**] です。</span><span class="sxs-lookup"><span data-stu-id="63ff0-329">The default status is **In Progress and Failed Jobs in the Past Week**.</span></span> 
    
- <span data-ttu-id="63ff0-330">すべてのキュー ジョブ設定をProject Web App、エンタープライズ オブジェクトの削除または強制チェックインを行う場合は、() の [サーバー サーバー] `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx` ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="63ff0-330">Use the Server Settings page in Project Web App ( `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`) to manage all queue jobs and delete or force check-in enterprise objects.</span></span> <span data-ttu-id="63ff0-331">[サーバー設定] ページのこれらのリンクにアクセスするには、管理権限が必要です。</span><span class="sxs-lookup"><span data-stu-id="63ff0-331">You must have administrative permissions to access those links on the Server Settings page.</span></span>
    
- <span data-ttu-id="63ff0-p158">**Microsoft SQL Server Management Studio** を使用して、Project Server データベースのテーブルにクエリを実行します。たとえば、以下のクエリを使用して、MSP_WORKFLOW_STAGE_PDPS テーブルの先頭 200 行を選択し、ワークフロー ステージのプロジェクト詳細ページ (PDP) に関する情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="63ff0-p158">Use **Microsoft SQL Server Management Studio** to run a query on a table of a Project Server database. For example, use the following query to select the top 200 rows of the MSP_WORKFLOW_STAGE_PDPS table to show information about the project detail pages (PDPs) in workflow stages.</span></span> 
    
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

## <a name="cleaning-up"></a><span data-ttu-id="63ff0-334">クリーンアップ</span><span class="sxs-lookup"><span data-stu-id="63ff0-334">Cleaning up</span></span>
<span data-ttu-id="63ff0-335"><a name="pj15_PrerequisitesWCF_Cleanup"> </a></span><span class="sxs-lookup"><span data-stu-id="63ff0-335"><a name="pj15_PrerequisitesWCF_Cleanup"> </a></span></span>

<span data-ttu-id="63ff0-336">いくつかのコード サンプルをテストすると、エンタープライズ オブジェクトおよび設定の削除や再設定が必要になります。</span><span class="sxs-lookup"><span data-stu-id="63ff0-336">After you test some code samples, there are enterprise objects and settings that should be deleted or reset.</span></span> <span data-ttu-id="63ff0-337">エンタープライズ データ () を管理設定サーバー Project Web Appページを使用できます `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx` 。</span><span class="sxs-lookup"><span data-stu-id="63ff0-337">You can use the Server Settings page in Project Web App to manage enterprise data ( `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`).</span></span> <span data-ttu-id="63ff0-338">[サーバー設定] ページにあるリンクを使用して、古いアイテムを削除したり、チェックインを強制したり、すべてのユーザーのジョブ キューを管理したり、その他の管理タスクを実行したりできます。</span><span class="sxs-lookup"><span data-stu-id="63ff0-338">Links on the Server Settings page enable you to delete old items, force check-in projects, manage the job queue for all users, and perform other administrative tasks.</span></span>
  
<span data-ttu-id="63ff0-339">以下に、コード サンプル実行後の一般的なクリーンアップ作業で使用する、[サーバー設定] ページ上のリンクの一部を示します。</span><span class="sxs-lookup"><span data-stu-id="63ff0-339">Following are some of the links on the Server Settings page to use for typical cleanup activities after running code samples:</span></span>
  
- <span data-ttu-id="63ff0-340">**エンタープライズ ユーザー設定フィールドと参照テーブル**</span><span class="sxs-lookup"><span data-stu-id="63ff0-340">**Enterprise Custom Fields and Lookup Tables**</span></span>
    
- <span data-ttu-id="63ff0-341">**キュー ジョブの管理**</span><span class="sxs-lookup"><span data-stu-id="63ff0-341">**Manage Queue Jobs**</span></span>
    
- <span data-ttu-id="63ff0-342">**エンタープライズ オブジェクトの削除**</span><span class="sxs-lookup"><span data-stu-id="63ff0-342">**Delete Enterprise Objects**</span></span>
    
- <span data-ttu-id="63ff0-343">**エンタープライズ オブジェクトの強制チェックイン**</span><span class="sxs-lookup"><span data-stu-id="63ff0-343">**Force Check-in Enterprise Objects**</span></span>
    
- <span data-ttu-id="63ff0-344">**エンタープライズ プロジェクトの種類**</span><span class="sxs-lookup"><span data-stu-id="63ff0-344">**Enterprise Project Types**</span></span>
    
- <span data-ttu-id="63ff0-345">**ワークフロー フェーズ**</span><span class="sxs-lookup"><span data-stu-id="63ff0-345">**Workflow Phases**</span></span>
    
- <span data-ttu-id="63ff0-346">**ワークフロー ステージ**</span><span class="sxs-lookup"><span data-stu-id="63ff0-346">**Workflow Stages**</span></span>
    
- <span data-ttu-id="63ff0-347">**プロジェクト詳細ページ**</span><span class="sxs-lookup"><span data-stu-id="63ff0-347">**Project Detail Pages**</span></span>
    
- <span data-ttu-id="63ff0-348">**タイムシート期間**</span><span class="sxs-lookup"><span data-stu-id="63ff0-348">**Time Reporting Periods**</span></span>
    
- <span data-ttu-id="63ff0-349">**タイムシートの設定および既定値**</span><span class="sxs-lookup"><span data-stu-id="63ff0-349">**Timesheet Settings and Defaults**</span></span>
    
- <span data-ttu-id="63ff0-350">**管理用行の分類**</span><span class="sxs-lookup"><span data-stu-id="63ff0-350">**Line Classifications**</span></span>
    
<span data-ttu-id="63ff0-351">その他の設定は、SharePoint Server 2013 で特定の Project Web App インスタンスではなく、Project Web App Server 2013 設定 ページによって管理されます。</span><span class="sxs-lookup"><span data-stu-id="63ff0-351">Additional settings are managed by SharePoint Server 2013 for each Project Web App instance, rather than by a specific Project Web App Server Settings page.</span></span> <span data-ttu-id="63ff0-352">SharePoint サーバーの全体管理アプリケーションで、[全般アプリケーション **設定]** を選択し **、[Project Server 設定]** の [管理] を選択し、[サーバー 設定] ページのドロップダウン リストで Project Web App インスタンスを選択します。 </span><span class="sxs-lookup"><span data-stu-id="63ff0-352">In the SharePoint Central Administration application, choose **General Application Settings**, choose **Manage** under **Project Server Settings**, and then choose the Project Web App instance in the drop-down list on the Server Settings page.</span></span> <span data-ttu-id="63ff0-353">たとえば、[サーバー側 **イベント ハンドラー] を** 選択して、選択したインスタンスのイベント ハンドラーを追加またはProject Web Appします。</span><span class="sxs-lookup"><span data-stu-id="63ff0-353">For example, choose **Server Side Event Handlers** to add or delete event handlers for the selected Project Web App instance.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="63ff0-354">関連項目</span><span class="sxs-lookup"><span data-stu-id="63ff0-354">See also</span></span>

- [<span data-ttu-id="63ff0-355">プロジェクト内のASMXベースコードサンプルの前提条件</span><span class="sxs-lookup"><span data-stu-id="63ff0-355">Prerequisites for ASMX-based code samples in Project</span></span>](prerequisites-for-asmx-based-code-samples-in-project.md)   
- <span data-ttu-id="63ff0-356">[[ウォークスルー] WCF を使用して PSI アプリケーションを開発する](https://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="63ff0-356">[Walkthrough: Developing PSI applications using WCF](https://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx)</span></span>   
- [<span data-ttu-id="63ff0-357">WCF で偽装を使用する</span><span class="sxs-lookup"><span data-stu-id="63ff0-357">Use Impersonation with WCF</span></span>](https://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)  
- [<span data-ttu-id="63ff0-358">Project PSI リファレンスの概要</span><span class="sxs-lookup"><span data-stu-id="63ff0-358">Project PSI reference overview</span></span>](project-psi-reference-overview.md) 
- [<span data-ttu-id="63ff0-359">SharePoint デベロッパー センター</span><span class="sxs-lookup"><span data-stu-id="63ff0-359">SharePoint Developer Center</span></span>](https://msdn.microsoft.com/sharepoint/default.aspx)
    

