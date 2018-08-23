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
# <a name="prerequisites-for-wcf-based-code-samples-in-project"></a><span data-ttu-id="544a4-103">プロジェクト内の WCF ベースのコード サンプルの前提条件</span><span class="sxs-lookup"><span data-stu-id="544a4-103">Prerequisites for WCF-based code samples in Project</span></span>

<span data-ttu-id="544a4-104">プロジェクト Server インターフェイス (PSI) のリファレンス トピックに含まれている WCF ベースのコード サンプルを使用して Visual Studio でプロジェクトを作成するための情報について説明します。</span><span class="sxs-lookup"><span data-stu-id="544a4-104">Learn information to help you create projects in Visual Studio by using the WCF-based code samples that are included in the Project Server Interface (PSI) reference topics.</span></span>
   
<span data-ttu-id="544a4-105">の[Project Server 2013 のクラス ライブラリと web サービスの参照](http://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx)に含まれている WCF ベースのコード サンプルの多くは、Project 2010 の開発者向けのドキュメント用に作成され、WCF web サービスの標準的な形式を使用します。</span><span class="sxs-lookup"><span data-stu-id="544a4-105">Many of the WCF-based code samples included in the [Project Server 2013 class library and web service reference](http://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) were originally created for the Project 2010 developer documentation, and use a standard format for WCF web services.</span></span> <span data-ttu-id="544a4-106">まだサンプルは、Project Server 2013 での作業し、コンソール アプリケーションにコピーし、完全な単位として実行するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="544a4-106">The samples still work in Project Server 2013 and are designed to be copied into a console application and run as a complete unit.</span></span> <span data-ttu-id="544a4-107">サンプルで例外が記載されています。</span><span class="sxs-lookup"><span data-stu-id="544a4-107">Exceptions are noted in the sample.</span></span> 
  
<span data-ttu-id="544a4-108">Office Project Server 2007 用に開発されたサンプルから変更されていない、Project 2013 開発者向けのドキュメントでのコード サンプルでは、ASMX Web サービスを使用します。</span><span class="sxs-lookup"><span data-stu-id="544a4-108">Code samples in the Project 2013 developer documentation that are unchanged from the samples developed for Office Project Server 2007 use ASMX Web services.</span></span> <span data-ttu-id="544a4-109">ASMX ベースのサンプルは、WCF サービスの使用に適合させることができます。</span><span class="sxs-lookup"><span data-stu-id="544a4-109">The ASMX-based samples can also be adapted to use WCF services.</span></span> <span data-ttu-id="544a4-110">この資料では、WCF サービスを使用してサンプルを使用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="544a4-110">This article shows how to use the samples with WCF services.</span></span> <span data-ttu-id="544a4-111">ASMX web サービスのサンプルを使用する方法の詳細については、[プロジェクト内の ASMX ベースのコード サンプルの前提条件](prerequisites-for-asmx-based-code-samples-in-project.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="544a4-111">For information about how to use the samples with ASMX web services, see [Prerequisites for ASMX-based code samples in Project](prerequisites-for-asmx-based-code-samples-in-project.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="544a4-112">クライアント側オブジェクト モデル (CSOM) では、アプリケーションを必要とするメソッドが含まれている場合、CSOM で新しいアプリケーションを開発する必要があります。</span><span class="sxs-lookup"><span data-stu-id="544a4-112">If the client-side object model (CSOM) includes the methods that your application requires, new applications should be developed with the CSOM.</span></span> <span data-ttu-id="544a4-113">CSOM は、プロジェクトのオンラインまたは Project Server 2013 のオンプレミス インストールを操作するアプリケーションを有効にします。</span><span class="sxs-lookup"><span data-stu-id="544a4-113">The CSOM enables applications to work with Project Online or an on-premises installation of Project Server 2013.</span></span> <span data-ttu-id="544a4-114">それ以外の場合、アプリケーションは、PSI を使用する場合は、WCF インターフェイスは、ネットワーク通信のことをお勧めする技術であるを使用してください。</span><span class="sxs-lookup"><span data-stu-id="544a4-114">Otherwise, if your application uses the PSI, it should use the WCF interface, which is the technology that we recommend for network communications.</span></span> <span data-ttu-id="544a4-115">ASMX インターフェイスまたは WCF インターフェイスを使用するアプリケーションは、Project Server 2013 のオンプレミスのインストールでのみ操作できます。</span><span class="sxs-lookup"><span data-stu-id="544a4-115">Applications that use the ASMX interface or the WCF interface can work only for on-premises installations of Project Server 2013.</span></span> 
>
> <span data-ttu-id="544a4-116">CSOM の詳細については、 [Project Server 2013 のアーキテクチャ](project-server-2013-architecture.md)および[Project 2013 のクライアント側オブジェクト モデル (CSOM)](client-side-object-model-csom-for-project-2013.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="544a4-116">For more information about the CSOM, see [Project Server 2013 architecture](project-server-2013-architecture.md) and [Client-side object model (CSOM) for Project 2013](client-side-object-model-csom-for-project-2013.md).</span></span> 
  
<span data-ttu-id="544a4-117">コード サンプルを実行する前に、開発環境のセットアップ、アプリケーションの構成、サービス構成ファイルの追加 (またはプログラムによる WCF サービスの構成)、および環境に合わせた一般的な定数値の変更を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="544a4-117">Before running the code samples, you must set up the development environment, configure the application, add a service configuration file (or configure the WCF services programmatically), and change generic constant values to match your environment.</span></span>
  
## <a name="setting-up-the-development-environment"></a><span data-ttu-id="544a4-118">開発環境を設定する</span><span class="sxs-lookup"><span data-stu-id="544a4-118">Setting up the development environment</span></span>
<span data-ttu-id="544a4-119"><a name="pj15_PrerequisitesWCF_Setup"> </a></span><span class="sxs-lookup"><span data-stu-id="544a4-119"></span></span>

1. <span data-ttu-id="544a4-120">**テスト プロジェクトのサーバー システムを設定します。**</span><span class="sxs-lookup"><span data-stu-id="544a4-120">**Set up a test Project Server system.**</span></span>
    
    <span data-ttu-id="544a4-p104">開発やテストを行う際には常にテスト Project Server システムを使用します。たとえコードが完全に動作しても、プロジェクト間の依存関係、レポート、またはその他の環境要因が意図しない結果を引き起こす可能性があります。</span><span class="sxs-lookup"><span data-stu-id="544a4-p104">Use a test Project Server system whenever you are developing or testing. Even when your code works perfectly, interproject dependencies, reporting, or other environmental factors can cause unintended consequences.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="544a4-123">確認して、サーバー上の有効なユーザーは、PSI の呼び出し、アプリケーションを使用するための十分なアクセス許可があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="544a4-123">Ensure that you are a valid user on the server, and check that you have sufficient permissions for the PSI calls that your application uses.</span></span> <span data-ttu-id="544a4-124">各 PSI メソッドの開発者ドキュメントのトピックには、プロジェクトのサーバーのアクセス許可のテーブルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="544a4-124">The developer documentation topic for each PSI method includes a Project Server Permissions table.</span></span> <span data-ttu-id="544a4-125">などの[Project.QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx)メソッドには、**新しいプロジェクト**グローバル アクセス権と、 **SaveProjectTemplate**アクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="544a4-125">For example, the [Project.QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) method requires the global **NewProject** permission and the **SaveProjectTemplate** permission.</span></span> 
  
    <span data-ttu-id="544a4-126">場合によっては、サーバー上でリモート デバッグを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="544a4-126">In some cases, you may have to do remote debugging on the server.</span></span> <span data-ttu-id="544a4-127">SharePoint ファーム内の各プロジェクトのサーバー コンピューター上のイベント ハンドラー アセンブリをインストールして、一般に、プロジェクトのサーバーの設定] ページを使用して、Project Web App インスタンスのイベント ハンドラーを構成して、イベント ハンドラーを設定する必要がありますもSharePoint サーバーの管理のアプリケーションの設定です。</span><span class="sxs-lookup"><span data-stu-id="544a4-127">You may also have to set up an event handler by installing an event handler assembly on each Project Server computer in the SharePoint farm, and then configuring the event handler for the Project Web App instance by using the Project Server Settings page in the General Application Settings of SharePoint Central Administration.</span></span>
    
2. <span data-ttu-id="544a4-128">**開発用コンピューターをセットアップする。**</span><span class="sxs-lookup"><span data-stu-id="544a4-128">**Set up a development computer.**</span></span>
    
    <span data-ttu-id="544a4-p107">通常、PSI にはネットワーク経由でアクセスします。コード サンプルは、記載されている場合を除き、サーバーから分離されたクライアントで動作するように作られています。</span><span class="sxs-lookup"><span data-stu-id="544a4-p107">You usually access the PSI through a network. The code samples are designed to be run on a client that is separate from the server, except where noted.</span></span>
    
    1. <span data-ttu-id="544a4-131">**Visual Studio の適切なバージョンをインストールします。**</span><span class="sxs-lookup"><span data-stu-id="544a4-131">**Install the correct version of Visual Studio.**</span></span> <span data-ttu-id="544a4-132">場合を除き、これらのコードが書き込まれます Visual C# で。</span><span class="sxs-lookup"><span data-stu-id="544a4-132">Except where noted, the code samples are written in Visual C#.</span></span> <span data-ttu-id="544a4-133">Visual Studio 2010 または Visual Studio 2012 では、それらを使用できます。</span><span class="sxs-lookup"><span data-stu-id="544a4-133">They can be used with Visual Studio 2010 or Visual Studio 2012.</span></span> <span data-ttu-id="544a4-134">最新のサービス パックのインストールがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="544a4-134">Ensure that you have the most recent service pack installed.</span></span> 
    
    2. <span data-ttu-id="544a4-135">**プロジェクト サーバー Dll を開発用コンピューターにコピーします。**</span><span class="sxs-lookup"><span data-stu-id="544a4-135">**Copy Project Server DLLs to the development computer.**</span></span> <span data-ttu-id="544a4-136">次のアセンブリをコピーする`[Program Files]\Microsoft Office Servers\15.0\Bin`開発用コンピューターに Project Server コンピューターにします。</span><span class="sxs-lookup"><span data-stu-id="544a4-136">Copy the following assemblies from  `[Program Files]\Microsoft Office Servers\15.0\Bin` on the Project Server computer to the development computer:</span></span> 
    
       - <span data-ttu-id="544a4-137">Microsoft.Office.Project.Server.Events.Receivers.dll</span><span class="sxs-lookup"><span data-stu-id="544a4-137">Microsoft.Office.Project.Server.Events.Receivers.dll</span></span>
    
       - <span data-ttu-id="544a4-138">Microsoft.Office.Project.Server.Library.dll</span><span class="sxs-lookup"><span data-stu-id="544a4-138">Microsoft.Office.Project.Server.Library.dll</span></span>
    
    3. <span data-ttu-id="544a4-139">PSI で WCF サービスの ProjectServerServices.dll プロキシ アセンブリをコンパイルして使用する方法に関する情報については、「[Intellisense の説明を備えた PSI プロキシ アセンブリを使用する](#pj15_PrerequisitesWCF_BuildingProxy)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="544a4-139">For information about how to compile and use the ProjectServerServices.dll proxy assembly for the WCF services in the PSI, see [Using a PSI proxy assembly and IntelliSense descriptions](#pj15_PrerequisitesWCF_BuildingProxy).</span></span>
    
3. <span data-ttu-id="544a4-140">**IntelliSense ファイルをインストールする。**</span><span class="sxs-lookup"><span data-stu-id="544a4-140">**Install the IntelliSense files.**</span></span>
    
    <span data-ttu-id="544a4-141">Project 2013 SDK から更新された IntelliSense XML ファイルは、コピーである Project Server アセンブリのクラスとメンバーの IntelliSense の説明を使用するには、Project Server アセンブリが配置されている同じディレクトリにダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="544a4-141">To use IntelliSense descriptions for classes and members in Project Server assemblies, copy the updated IntelliSense XML files from the Project 2013 SDK download to the same directory where the Project Server assemblies are located.</span></span> <span data-ttu-id="544a4-142">たとえば、アプリケーションが Microsoft.Office.Project.Server.Library.dll アセンブリへの参照に設定されているディレクトリに Microsoft.Office.Project.Server.Library.xml ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="544a4-142">For example, copy the Microsoft.Office.Project.Server.Library.xml file to the directory where your application will set a reference to the Microsoft.Office.Project.Server.Library.dll assembly.</span></span>
    
    <span data-ttu-id="544a4-143">PSI サービス用の IntelliSense の説明で CompileWCFProxyAssembly.cmd スクリプトを使用して、PSI プロキシ アセンブリを作成することを必要とする、 `Documentation\IntelliSense\WCF` Project 2013 SDK ダウンロードのサブディレクトリです。</span><span class="sxs-lookup"><span data-stu-id="544a4-143">IntelliSense descriptions for the PSI services require that you create a PSI proxy assembly by using the CompileWCFProxyAssembly.cmd script in the  `Documentation\IntelliSense\WCF` subdirectory in the Project 2013 SDK download.</span></span> <span data-ttu-id="544a4-144">スクリプトは、ProjectServerServices.dll の WCF ベースのプロキシ アセンブリを作成します。</span><span class="sxs-lookup"><span data-stu-id="544a4-144">The script creates the WCF-based ProjectServerServices.dll proxy assembly.</span></span> <span data-ttu-id="544a4-145">詳細については、SDK ダウンロードの [ReadMe_IntelliSense] .mht ファイルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="544a4-145">For more information, see the [ReadMe_IntelliSense].mht file in the SDK download.</span></span> 
    
## <a name="creating-the-application-and-adding-a-service-reference"></a><span data-ttu-id="544a4-146">アプリケーションを作成してサービス参照を追加する</span><span class="sxs-lookup"><span data-stu-id="544a4-146">Creating the application and adding a service reference</span></span>
<span data-ttu-id="544a4-147"><a name="pj15_PrerequisitesWCF_Configure"> </a></span><span class="sxs-lookup"><span data-stu-id="544a4-147"></span></span>

1. <span data-ttu-id="544a4-148">**コンソール アプリケーションを作成します。**</span><span class="sxs-lookup"><span data-stu-id="544a4-148">**Create a console application.**</span></span>
    
    <span data-ttu-id="544a4-p112">コンソール アプリケーションを作成するには、[**新しいプロジェクト**] ダイアログ ボックスのドロップダウン リストから [**.NET Framework 4**] を選択します。この新しいアプリケーションに PSI サンプル コードをコピーできます。</span><span class="sxs-lookup"><span data-stu-id="544a4-p112">When you create a console application, in the drop-down list of the **New Project** dialog box, select **.NET Framework 4**. You can copy the PSI example code into the new application.</span></span>
    
2. <span data-ttu-id="544a4-151">**WCF に必要な参照を追加する。**</span><span class="sxs-lookup"><span data-stu-id="544a4-151">**Add references required for WCF.**</span></span>
    
    <span data-ttu-id="544a4-152">ソリューション エクスプ ローラーで、 **System.ServiceModel**への参照を追加します (図 1 を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="544a4-152">In Solution Explorer, add a reference to **System.ServiceModel** (see Figure 1).</span></span> <span data-ttu-id="544a4-153">Web アプリケーションでは、 **System.ServiceModel.Web**を使用します。</span><span class="sxs-lookup"><span data-stu-id="544a4-153">A web application would use **System.ServiceModel.Web**.</span></span>
    
    <span data-ttu-id="544a4-154">**System.Runtime.Serialization** への参照も追加します。</span><span class="sxs-lookup"><span data-stu-id="544a4-154">Also add a reference to **System.Runtime.Serialization**.</span></span>
    
    <span data-ttu-id="544a4-155">**図 1. Visual Studio での WCF ベースのアプリケーションへの参照の追加**</span><span class="sxs-lookup"><span data-stu-id="544a4-155">**Figure 1. Adding the references in Visual Studio for a WCF-based application**</span></span>

    <span data-ttu-id="544a4-156">![WCF への参照を追加します。](media/pj15_PrerequisitesWCF_AddReference.gif "WCF への参照を追加します。")</span><span class="sxs-lookup"><span data-stu-id="544a4-156">![Adding references for WCF](media/pj15_PrerequisitesWCF_AddReference.gif "Adding references for WCF")</span></span>
  
3. <span data-ttu-id="544a4-157">**コードをコピーする。**</span><span class="sxs-lookup"><span data-stu-id="544a4-157">**Copy the code**.</span></span>
    
    <span data-ttu-id="544a4-158">コード サンプル全体をコンソール アプリケーションの Program.cs ファイルにコピーします。</span><span class="sxs-lookup"><span data-stu-id="544a4-158">Copy the complete code example into the Program.cs file of the console application.</span></span>
    
4. <span data-ttu-id="544a4-159">**サンプル アプリケーションの名前空間を設定します。**</span><span class="sxs-lookup"><span data-stu-id="544a4-159">**Set the namespace for the sample application.**</span></span>
    
    <span data-ttu-id="544a4-p114">サンプルの上部に記されている名前空間をアプリケーションの既定の名前空間に変更するか、アプリケーションの既定の名前空間をサンプルに合わせて変更することができます。アプリケーションの既定の名前空間は、アプリケーションのプロパティを変更することによって変更できます。</span><span class="sxs-lookup"><span data-stu-id="544a4-p114">You can either change the namespace listed at the top of the sample to the application default namespace, or change the default application namespace to match the sample. You can change the default application namespace by changing the application properties.</span></span> 
    
    <span data-ttu-id="544a4-162">たとえば、 [ReadResource](https://msdn.microsoft.com/library/WebSvcResource.Resource.ReadResource.aspx)のコード サンプルは、 **Microsoft.SDK.Project.Samples.CreateResourceTest**名前空間を持っています。</span><span class="sxs-lookup"><span data-stu-id="544a4-162">For example, the code sample for [ReadResource](https://msdn.microsoft.com/library/WebSvcResource.Resource.ReadResource.aspx) has the namespace **Microsoft.SDK.Project.Samples.CreateResourceTest**.</span></span> <span data-ttu-id="544a4-163">**ResourceTest**の Visual Studio プロジェクトの名前が表示された場合、Program.cs ファイルから名前空間をコピーし、プロジェクト**のプロパティ**] ウィンドウを開きます ( **[プロジェクト**] メニューで、 **ResourceTest プロパティ**] をクリックすると)。</span><span class="sxs-lookup"><span data-stu-id="544a4-163">If the name of the Visual Studio project is **ResourceTest**, copy the namespace from the Program.cs file, and then open the project **Properties** pane (on the **Project** menu, choose **ResourceTest Properties**).</span></span> <span data-ttu-id="544a4-164">[**アプリケーション**] タブで、名前空間を**既定の名前空間**] テキスト ボックスにコピーします。</span><span class="sxs-lookup"><span data-stu-id="544a4-164">On the **Application** tab, copy the namespace into the **Default namespace** text box.</span></span> 
    
5. <span data-ttu-id="544a4-165">**サービス参照を設定する。**</span><span class="sxs-lookup"><span data-stu-id="544a4-165">**Set the service references.**</span></span>
    
    <span data-ttu-id="544a4-p116">多くの例では、1 つ以上の PSI サービスへの参照が必要です。これらは、サンプル自体、またはサンプルの前にあるコメントに示されています。サービス参照の適切な名前空間を取得するには、最初にアプリケーションの既定の名前空間を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="544a4-p116">Many examples require a reference to one or more of the PSI services. These are listed in the sample itself or in comments that precede the sample. To get the correct namespace of the service references, ensure that you first set the default application namespace.</span></span>
    
    <span data-ttu-id="544a4-169">WCF サービス参照を追加する方法として次の 3 つがあります。</span><span class="sxs-lookup"><span data-stu-id="544a4-169">There are three ways to add a WCF service reference:</span></span>
    
    - <span data-ttu-id="544a4-p117">ProjectServerServices.dll という名前の PSI プロキシ アセンブリを作成してから、このアセンブリへの参照を設定します。詳細については「[Intellisense の説明を備えた PSI プロキシ アセンブリを使用する](#pj15_PrerequisitesWCF_BuildingProxy)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="544a4-p117">Build a PSI proxy assembly named ProjectServerServices.dll, and then set a reference to the assembly. See [Using a PSI proxy assembly and IntelliSense descriptions](#pj15_PrerequisitesWCF_BuildingProxy).</span></span>
    
    - <span data-ttu-id="544a4-p118">svcutil.exe 出力からのプロキシ ファイルを Visual Studio ソリューションに追加します。「[PSI プロキシ ファイルを追加する](#pj15_PrerequisitesWCF_AddingProxyFile)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="544a4-p118">Add a proxy file from the svcutil.exe output to the Visual Studio solution. See [Adding a PSI proxy file](#pj15_PrerequisitesWCF_AddingProxyFile).</span></span>
    
    - <span data-ttu-id="544a4-p119">Visual Studio を使用してサービス参照を追加します。「[サービス参照を追加する](#pj15_PrerequisitesWCF_AddingServiceReference)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="544a4-p119">Add a service reference by using Visual Studio. See [Adding a service reference](#pj15_PrerequisitesWCF_AddingServiceReference).</span></span>
    
### <a name="using-a-psi-proxy-assembly-and-intellisense-descriptions"></a><span data-ttu-id="544a4-176">Intellisense の説明を備えた PSI プロキシ アセンブリを使用する</span><span class="sxs-lookup"><span data-stu-id="544a4-176">Using a PSI proxy assembly and IntelliSense descriptions</span></span>
<span data-ttu-id="544a4-177"><a name="pj15_PrerequisitesWCF_BuildingProxy"> </a></span><span class="sxs-lookup"><span data-stu-id="544a4-177"></span></span>

<span data-ttu-id="544a4-178">PSI のすべてのパブリック WCF サービスのプロキシ アセンブリを使用できます。</span><span class="sxs-lookup"><span data-stu-id="544a4-178">You can use a proxy assembly for all public WCF services in the PSI.</span></span> <span data-ttu-id="544a4-179">ProjectServerServices.dll プロキシ アセンブリを使用してコンパイルします`Documentation\IntelliSense\WCF\CompileWCFProxyAssembly.cmd`Project 2013 SDK のダウンロードのスクリプトを作成し、プロキシ アセンブリを開発用コンピューターにコピーします。</span><span class="sxs-lookup"><span data-stu-id="544a4-179">Compile the ProjectServerServices.dll proxy assembly by using the  `Documentation\IntelliSense\WCF\CompileWCFProxyAssembly.cmd` script in the Project 2013 SDK download, and then copy the proxy assembly to your development computer.</span></span> <span data-ttu-id="544a4-180">IntelliSense の同じ場所に ProjectServerServices.xml ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="544a4-180">Copy the ProjectServerServices.xml file for IntelliSense to the same location.</span></span> <span data-ttu-id="544a4-181">Visual Studio は、ProjectServerServices.dll のプロキシ アセンブリへの参照を設定します。</span><span class="sxs-lookup"><span data-stu-id="544a4-181">In Visual Studio, set a reference to the ProjectServerServices.dll proxy assembly.</span></span> 
  
<span data-ttu-id="544a4-182">Project Server のサービス パックおよび更新プログラムの場合は、プロキシのソース ファイルを更新し、SDK ダウンロードの同じフォルダーに GenWCFProxyAssembly.cmd スクリプトを使用して、新しいプロキシ アセンブリを作成できます。</span><span class="sxs-lookup"><span data-stu-id="544a4-182">For Project Server service packs and updates, you can update the proxy source files and create a new proxy assembly by using the GenWCFProxyAssembly.cmd script in the same SDK download folder.</span></span> <span data-ttu-id="544a4-183">SDK をダウンロードするリンクは、 [Project 2013 開発者向けドキュメント](project-2013-developer-documentation.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="544a4-183">For a link to the SDK download, see [Project 2013 developer documentation](project-2013-developer-documentation.md).</span></span> <span data-ttu-id="544a4-184">詳細については、[サービス参照の追加](#pj15_PrerequisitesWCF_AddingServiceReference)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="544a4-184">For more information, see the [Adding a service reference](#pj15_PrerequisitesWCF_AddingServiceReference) section.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="544a4-185">Source.zip からプロキシ ソース ファイルを抽出するときにファイル内のファイル、`Documentation\IntelliSense\WCF\Source`は、Project 2013 SDK ダウンロードの発行日時点で現在のフォルダーです。</span><span class="sxs-lookup"><span data-stu-id="544a4-185">When you extract the proxy source files from the Source.zip file, the files in the  `Documentation\IntelliSense\WCF\Source` folder are current as of the publication date of the Project 2013 SDK download.</span></span> <span data-ttu-id="544a4-186">生成するには、PSI プロキシ ソース ファイルは、Project Server コンピューター上の GenASMXProxyAssembly.cmd スクリプトの実行を更新しました。</span><span class="sxs-lookup"><span data-stu-id="544a4-186">To generate updated PSI proxy source files, run the GenASMXProxyAssembly.cmd script on the Project Server computer.</span></span> <span data-ttu-id="544a4-187">詳細については、[サービス参照の追加](#pj15_PrerequisitesWCF_AddingServiceReference)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="544a4-187">For more information, see [Adding a service reference](#pj15_PrerequisitesWCF_AddingServiceReference).</span></span> 
> 
> <span data-ttu-id="544a4-188">内のスクリプト、`Documentation\IntelliSense\ASMX`フォルダーは、WCF ベースのアプリケーションでは機能しません。</span><span class="sxs-lookup"><span data-stu-id="544a4-188">The scripts in the  `Documentation\IntelliSense\ASMX` folder do not work for WCF-based applications.</span></span> <span data-ttu-id="544a4-189">GenASMXProxyAssembly.cmd スクリプトでは、ASMX サービスのソース コード ファイルを生成する、Wsdl.exe を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="544a4-189">The GenASMXProxyAssembly.cmd script calls Wsdl.exe, which generates source code files for the ASMX services.</span></span> <span data-ttu-id="544a4-190">ASMX プロキシ ファイルには、さまざまなクラスとプロパティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="544a4-190">The ASMX proxy files include different classes and properties.</span></span> <span data-ttu-id="544a4-191">などの資源の ASMX ベース web サービスには、WCF ベースのリソースのサービスには、**リソース**インターフェイス、 **ResourceChannel**インターフェイス、および**ResourceClient**のクラスが含まれていますに、**リソース**のクラスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="544a4-191">For example, the ASMX-based Resource web service includes the **Resource** class, whereas the WCF-based Resource service includes the **Resource** interface, the **ResourceChannel** interface, and the **ResourceClient** class.</span></span> 
  
<span data-ttu-id="544a4-p124">ASMX Web サービスと WCF サービスのために作成された恣意的な名前空間はどちらも同じなので、Intellisense 用の ProjectServerServices.xml ファイルはどちらのアセンブリでも動作します。たとえば、WCF ベースのプロキシ アセンブリでも ASMX ベースのプロキシ アセンブリでも、Resource サービスの名前空間は **SvcResource** です。もちろん、この名前空間の名前は変更できます。ただし、その名前はプロキシ アセンブリと ProjectServerServices.xml Intellisense ファイルで一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="544a4-p124">The arbitrary namespaces created for both the ASMX web services and the WCF services are the same, so that the ProjectServerServices.xml file for IntelliSense works with either assembly. For example, the namespace of the Resource service in the WCF-based proxy assembly and in the ASMX-based proxy assembly is **SvcResource**. You can, of course, change the namespace names— if you ensure that they match in the proxy assembly and in the ProjectServerServices.xml IntelliSense file.</span></span>
  
<span data-ttu-id="544a4-195">あるコード サンプルが PSI サービスの名前空間に別の名前 (**ProjectWebSvc** など) を使用している場合、IntelliSense が動作するためには、**SvcProject** を使用するようにそのサンプルを変更して、名前空間とプロキシ アセンブリを一致させる必要があります。</span><span class="sxs-lookup"><span data-stu-id="544a4-195">If a code sample uses a different name for a PSI service namespace, for example **ProjectWebSvc**, for IntelliSense to work you must change the sample to use **SvcProject** so that the namespace matches the proxy assembly.</span></span> 
  
<span data-ttu-id="544a4-196">WCF ベースのプロキシ アセンブリを使用する利点は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="544a4-196">Advantages to using the WCF-based proxy assembly include the following:</span></span>
  
- <span data-ttu-id="544a4-p125">ほとんどのソリューションを、Project Server コンピューターとは別のコンピューター上にあるプロキシ アセンブリで開発できます。ただし、個々のサービス参照の設定には、Project Server コンピューターでの開発が必要です。</span><span class="sxs-lookup"><span data-stu-id="544a4-p125">You can develop most solutions with the proxy assembly on a different computer than the Project Server computer. Setting an individual service reference requires development on the Project Server computer.</span></span>
    
- <span data-ttu-id="544a4-199">このプロキシ アセンブリにはすべての PSI サービス名前空間が含まれるので、複数のプロキシ ファイルを追加する必要がありません。</span><span class="sxs-lookup"><span data-stu-id="544a4-199">The proxy assembly includes all PSI service namespaces, so you do not have to add multiple proxy files.</span></span>
    
- <span data-ttu-id="544a4-200">ProjectServerServices.dll プロキシ アセンブリへの参照を設定するのと同じディレクトリに ProjectServerServices.xml ファイルを追加する場合は、PSI のクラスおよびメンバーの IntelliSense の説明を取得できます。</span><span class="sxs-lookup"><span data-stu-id="544a4-200">If you add the ProjectServerServices.xml file to the same directory where you set a reference to the ProjectServerServices.dll proxy assembly, you can get IntelliSense descriptions for the PSI classes and members.</span></span> <span data-ttu-id="544a4-201">詳細についてを参照してください [ReadMe_IntelliSense] で、 `Documentation\IntelliSense` Project 2013 SDK ダウンロードのフォルダーです。</span><span class="sxs-lookup"><span data-stu-id="544a4-201">For more information, see the [ReadMe_IntelliSense] file in the  `Documentation\IntelliSense` folder of the Project 2013 SDK download.</span></span> 
    
<span data-ttu-id="544a4-202">**図 2. Resource サービスのメソッドに対する IntelliSense の使用**</span><span class="sxs-lookup"><span data-stu-id="544a4-202">**Figure 2. Using IntelliSense for a method in the Resource service**</span></span>

<span data-ttu-id="544a4-203">![ReadResource メソッドの Intellisense を使用します。](media/pj15_PrerequisitesWCF_Intellisense.gif "ReadResource メソッドの Intellisense を使用します。")</span><span class="sxs-lookup"><span data-stu-id="544a4-203">![Using Intellisense for the ReadResource method](media/pj15_PrerequisitesWCF_Intellisense.gif "Using Intellisense for the ReadResource method")</span></span>
  
<span data-ttu-id="544a4-p127">このプロキシ アセンブリを使用する場合の欠点は、ソリューションが大規模になることと、ソリューションと共にプロキシ アセンブリの配布とインストールが必要になることです。また、プロキシ アセンブリと Intellisense ファイルの中で同じ名前空間を使用する必要があります (ただし、スクリプトを修正して、独自のプロキシ アセンブリを作成し、別々の名前空間を使用するように ProjectServerServices.xml Intellisense ファイルを変更した場合は例外です)。</span><span class="sxs-lookup"><span data-stu-id="544a4-p127">Disadvantages to using the proxy assembly are that the solution is larger and you must distribute and install the proxy assembly with the solution. You must also use the same namespaces that are in the proxy assembly and IntelliSense files, unless you change the script to build a proxy assembly and change the ProjectServerServices.xml IntelliSense file to use different namespaces.</span></span>
  
### <a name="adding-a-psi-proxy-file"></a><span data-ttu-id="544a4-206">PSI プロキシ ファイルを追加する</span><span class="sxs-lookup"><span data-stu-id="544a4-206">Adding a PSI proxy file</span></span>
<span data-ttu-id="544a4-207"><a name="pj15_PrerequisitesWCF_AddingProxyFile"> </a></span><span class="sxs-lookup"><span data-stu-id="544a4-207"></span></span>

<span data-ttu-id="544a4-208">Project 2013 SDK ダウンロードには、プロキシ アセンブリの SvcUtil.exe コマンドによって生成されるソース ファイルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="544a4-208">The Project 2013 SDK download includes the source files that are generated by the SvcUtil.exe command for the proxy assembly.</span></span> <span data-ttu-id="544a4-209">Source.zip ファイル内には、ソース ファイル、`Documentation\IntelliSense\WCF`のサブディレクトリです。</span><span class="sxs-lookup"><span data-stu-id="544a4-209">The source files are in the Source.zip file in the  `Documentation\IntelliSense\WCF` subdirectory.</span></span> <span data-ttu-id="544a4-210">プロキシ アセンブリへの参照を設定する代わりに、Visual Studio のソリューションに 1 つまたは複数のソース ファイルを追加できます。</span><span class="sxs-lookup"><span data-stu-id="544a4-210">Instead of setting a reference to the proxy assembly, you can add one or more of the source files to a Visual Studio solution.</span></span> <span data-ttu-id="544a4-211">など、プロジェクトのサービスおよびリソースのサービスを使用するには、wcf を追加します。Project.cs と wcf。ソリューションのファイルを Resource.cs。</span><span class="sxs-lookup"><span data-stu-id="544a4-211">For example, to use the Project service and the Resource service, add the wcf.Project.cs and wcf.Resource.cs files to the solution.</span></span> 
  
<span data-ttu-id="544a4-p129">WCF では、それぞれの PSI サービスの主要なクラスが、インターフェイスによって定義され、そのメンバーにアクセスするためのクライアント クラス内で実装されます。たとえば、**SvcProject.Resource** インターフェイスは **SvcProject.ResourceClient** クラス内で実装されています。**ResourceClient** オブジェクトを、たとえば **resourceClient** という名前のクラス変数として定義するには、以下のコードを使用します。この例では、**SetClientEndpoints** メソッドによって、**basicHttp_Project** エンドポイントを使用する **resourceClient** オブジェクトが作成されます。このエンドポイントは app.config ファイルで定義されています。app.config ファイルの詳細については、「[サービス構成ファイルを追加する](#pj15_PrerequisitesWCF_AddConfig)」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="544a4-p129">In WCF, the primary class in each PSI service is defined by an interface and implemented in a client class for access to the members. For example, the **SvcProject.Resource** interface is implemented in the **SvcProject.ResourceClient** class. To define a **ResourceClient** object as a class variable named **resourceClient**, for example, use the following code. In the example, the **SetClientEndpoints** method creates a **resourceClient** object that uses the **basicHttp_Project** endpoint, which is defined in the app.config file. For more information about the app.config file, see the [Adding a service configuration file](#pj15_PrerequisitesWCF_AddConfig) section.</span></span> 
  
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
> <span data-ttu-id="544a4-217">PSI プロキシ アセンブリを使用する場合も、プロキシ ファイルを追加して **SvcResource** という名前の Project サービス参照を追加する場合も、**resourceClient** オブジェクトの作成と廃棄には同じコードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="544a4-217">Whether you use a PSI proxy assembly or add a proxy file for a Project service reference named **SvcResource**, you would use the same code to create and dispose a **resourceClient** object.</span></span> 
  
### <a name="adding-a-service-reference"></a><span data-ttu-id="544a4-218">サービス参照の追加</span><span class="sxs-lookup"><span data-stu-id="544a4-218">Adding a service reference</span></span>
<span data-ttu-id="544a4-219"><a name="pj15_PrerequisitesWCF_AddingServiceReference"> </a></span><span class="sxs-lookup"><span data-stu-id="544a4-219"></span></span>

<span data-ttu-id="544a4-220">PSI サービスのプロキシ ファイルを追加または WCF ベースのプロキシ アセンブリを使用するしないで場合、は、Visual Studio 内で直接 1 つ以上の個々 のサービス参照を設定できます。</span><span class="sxs-lookup"><span data-stu-id="544a4-220">If you do not use the WCF-based proxy assembly or add a proxy file for a PSI service, you can set one or more individual service references directly in Visual Studio.</span></span> <span data-ttu-id="544a4-221">準備するのには、更新されたプロキシ ファイルを作成するのには、次の手順のステップ 1 を使用することも、`Documentation\IntelliSense\WCF\GenWCFProxyAssembly.cmd`はスクリプト Project 2013 SDK ダウンロードに含まれています。</span><span class="sxs-lookup"><span data-stu-id="544a4-221">You can also use step 1 of the following procedure to create updated proxy files, to prepare for the  `Documentation\IntelliSense\WCF\GenWCFProxyAssembly.cmd` script that is included in the Project 2013 SDK download.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="544a4-p131">サービス参照を設定するには、Project Server コンピューターで Visual Studio を使用する必要があります。Visual Studio 内でサービス参照を直接追加するよりも、ProjectServerServices.dll プロキシ アセンブリを使用するか、プロキシ ソース ファイルを追加することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="544a4-p131">To set a service reference, you must use Visual Studio on the Project Server computer. We recommend that you use the ProjectServerServices.dll proxy assembly or add proxy source files, instead of directly adding service references in Visual Studio.</span></span> 
  
<span data-ttu-id="544a4-224">次の手順では、Project Server のテスト インストールを実行するコンピューターに Visual Studio 2012 を使用してサービス参照を設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="544a4-224">The following steps show how to set a service reference by using Visual Studio 2012 on a computer running a test installation of Project Server:</span></span>
  
1. <span data-ttu-id="544a4-225">バックエンド WCF サービスへのアクセスを取得するには、Project Server コンピューターで Visual Studio を実行します。</span><span class="sxs-lookup"><span data-stu-id="544a4-225">To get access to the back-end WCF services, run Visual Studio on the Project Server computer.</span></span>
    
2. <span data-ttu-id="544a4-226">**ソリューション エクスプローラー**で、[**参照設定**] フォルダーを右クリックし、[**サービス参照の追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="544a4-226">In **Solution Explorer**, right-click the **References** folder, and then choose **Add Service Reference**.</span></span> 
    
3. <span data-ttu-id="544a4-227">[**サービス参照の追加**] ダイアログ ボックスの [**アドレス**] テキスト ボックスに、入力http://localhost:32843//psi/ _ServiceName_.svc の_GUID_、し、 **Enter**キーを押します。</span><span class="sxs-lookup"><span data-stu-id="544a4-227">In the **Add Service Reference** dialog box, in the **Address** text box, type http://localhost:32843/ _GUID_/psi/ _ServiceName_.svc, and then press **Enter**.</span></span> <span data-ttu-id="544a4-228">_GUID_を 534c37eb00d74ccfadcecf9827e95239 など、Project Server サービス アプリケーションの仮想ディレクトリ名に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="544a4-228">Replace  _GUID_ with the virtual directory name of the Project Server service application, such as 534c37eb00d74ccfadcecf9827e95239.</span></span> <span data-ttu-id="544a4-229">リソースなど、サービスの名前と_アドレス_を交換して (図 3 を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="544a4-229">Replace  _ServiceName_ with the name of the service, such as Resource (see Figure 3).</span></span> 
    
   <span data-ttu-id="544a4-230">Project Server Service 仮想ディレクトリの名前は、以下のどちらかの方法で取得できます。</span><span class="sxs-lookup"><span data-stu-id="544a4-230">You can get the name of the Project Server Service virtual directory in one of the following ways:</span></span>
    
   - <span data-ttu-id="544a4-231">お使いのブラウザーでは、SharePoint 2013 のサーバーの管理アプリケーションを開きます。</span><span class="sxs-lookup"><span data-stu-id="544a4-231">Open the SharePoint 2013 Central Administration application in your browser.</span></span> <span data-ttu-id="544a4-232">**サービス アプリケーションの管理**を選択し、使用する Project Server の PSI サービス アプリケーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="544a4-232">Choose **Manage service applications**, and then choose the Project Server PSI Service application that you want.</span></span> <span data-ttu-id="544a4-233">たとえば、 **ProjectServerService**を選択します。</span><span class="sxs-lookup"><span data-stu-id="544a4-233">For example, choose **ProjectServerService**.</span></span> <span data-ttu-id="544a4-234">Project Web App サイトの管理] ページの URL には、仮想ディレクトリ名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="544a4-234">The URL of the Manage Project Web App Sites page contains the virtual directory name.</span></span> <span data-ttu-id="544a4-235">たとえば、 `http://ServerName:8080/_admin/pwa/managepwa.aspx?appid=534c37eb-00d7-4ccf-adce-cf9827e95239`、仮想ディレクトリ名は、 `534c37eb00d74ccfadcecf9827e95239` (ディレクトリ名にハイフンが含まれていません)。</span><span class="sxs-lookup"><span data-stu-id="544a4-235">For example, in  `http://ServerName:8080/_admin/pwa/managepwa.aspx?appid=534c37eb-00d7-4ccf-adce-cf9827e95239`, the virtual directory name is  `534c37eb00d74ccfadcecf9827e95239` (the directory name contains no dashes).</span></span> 
    
   - <span data-ttu-id="544a4-p134">Project Server コンピューターで [**インターネット インフォメーション サービス (IIS) マネージャー**] ダイアログ ボックスを開きます。[**接続**] ウィンドウの [**SharePoint Web サービス**] ノードを展開し、PSI フォルダーを含むディレクトリが見つかるまで、その下位にあるサービス仮想ディレクトリを展開していきます。見つかったディレクトリを選択し、[**操作**] ウィンドウの [**詳細設定**] をクリックして、そのディレクトリ名を [**仮想パス**] フィールドにコピーします。</span><span class="sxs-lookup"><span data-stu-id="544a4-p134">Open the **Internet Information Services (IIS) Manager** dialog box on the Project Server computer. Expand the **SharePoint Web Services** node in the **Connections** pane, and then expand the service virtual directories below that, until you find the directory that includes a PSI folder. Select the directory, choose **Advanced Settings** in the **Actions** pane, and then copy the directory name in the **Virtual Path** field.</span></span> 
    
      > [!NOTE]
      > <span data-ttu-id="544a4-239">プロジェクト サーバーのサービスの 1 つ以上の仮想ディレクトリがあります。</span><span class="sxs-lookup"><span data-stu-id="544a4-239">There can be more than one Project Server Service virtual directory.</span></span> <span data-ttu-id="544a4-240">Project Web App インスタンスが含まれている仮想ディレクトリを選択することを確認します。</span><span class="sxs-lookup"><span data-stu-id="544a4-240">Ensure that you choose the virtual directory that contains the Project Web App instance that you want.</span></span> 
  
   - <span data-ttu-id="544a4-241">SharePoint 2013 がインストールされている Windows PowerShell で**get SPServiceApplication**コマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="544a4-241">Use the **get-SPServiceApplication** cmdlet in Windows PowerShell that is installed with SharePoint 2013.</span></span> <span data-ttu-id="544a4-242">タスク バーの [**開始**] メニューの**すべてのプログラム**を選択して、 **Microsoft SharePoint 2013 の製品**を選択し、 **SharePoint 2013 の管理シェル**します。</span><span class="sxs-lookup"><span data-stu-id="544a4-242">On the taskbar **Start** menu, choose **All Programs**, choose **Microsoft SharePoint 2013 Products**, and then choose **SharePoint 2013 Management Shell**.</span></span> <span data-ttu-id="544a4-243">コマンドと (、Guid は異なるされます) に定義されたサービス アプリケーションを**SharePoint 2013get 管理シェル**ウィンドウで結果を次に示します。</span><span class="sxs-lookup"><span data-stu-id="544a4-243">Following is the command and the results in the **SharePoint 2013get- Management Shell** window for the defined service applications (your GUIDs will be different).</span></span> <span data-ttu-id="544a4-244">Project Server サービス アプリケーションの GUID をコピーします。</span><span class="sxs-lookup"><span data-stu-id="544a4-244">Copy the GUID for the Project Server service application.</span></span> 
    
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

      <span data-ttu-id="544a4-245">Project Server Service アプリケーションの完全な名前がわかる場合は、その名前に基づいて GUID 値を取得できます。次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="544a4-245">If you know the full name of the Project Server Service application, you can use it to get the GUID value, for example:</span></span>
    
        ```powershell
        PS > $projectService = "ProjectServerService"
        PS > (get-SPServiceApplication -Name $projectService).Id
        Guid
        ----
        534c37eb-00d7-4ccf-adce-cf9827e95239
       ```

      > [!NOTE]
      > <span data-ttu-id="544a4-246">GUID からダッシュを削除すると仮想ディレクトリ名になります。</span><span class="sxs-lookup"><span data-stu-id="544a4-246">Remove the dashes in the GUID to get the virtual directory name.</span></span> 
  
   <span data-ttu-id="544a4-247">Url など、`http://localhost:32843/534c37eb00d74ccfadcecf9827e95239/PSI/Resource.svc`は、Project Server サービスの標準的な。</span><span class="sxs-lookup"><span data-stu-id="544a4-247">URLs such as  `http://localhost:32843/534c37eb00d74ccfadcecf9827e95239/PSI/Resource.svc` are standard for Project Server services.</span></span> 
    
4. <span data-ttu-id="544a4-248">サービス参照が解決した後は、 **Namespace** ] テキスト ボックスに参照名を入力します。</span><span class="sxs-lookup"><span data-stu-id="544a4-248">After the service reference resolves, type the reference name in the **Namespace** text box.</span></span> <span data-ttu-id="544a4-249">Project 2013 開発者向けドキュメントのコード例では、任意の名前空間の名前**サービスの_アドレス_** を使用します。</span><span class="sxs-lookup"><span data-stu-id="544a4-249">Code examples in the Project 2013 developer documentation use the arbitrary namespace name **Svc _ServiceName_**.</span></span> <span data-ttu-id="544a4-250">たとえば、リソース サービスのコード例では**SvcResource**という名前します。</span><span class="sxs-lookup"><span data-stu-id="544a4-250">For example, the Resource service in the code examples is named **SvcResource**.</span></span>
    
    <span data-ttu-id="544a4-251">**図 3. WCF ベースの Resource サービス参照の追加**</span><span class="sxs-lookup"><span data-stu-id="544a4-251">**Figure 3. Adding the WCF-based Resource service reference**</span></span>

    <span data-ttu-id="544a4-252">![リソースの WCF ベースのサービス参照を追加します。](media/pj15_PrerequisitesWCF_AddSvcReference.gif "リソースの WCF ベースのサービス参照を追加します。")</span><span class="sxs-lookup"><span data-stu-id="544a4-252">![Adding the WCF-based Resource service reference](media/pj15_PrerequisitesWCF_AddSvcReference.gif "Adding the WCF-based Resource service reference")</span></span>
  
5. <span data-ttu-id="544a4-253">(Web.config に変更)、元に、一時ディレクトリの web.config ファイル、プロジェクトのサービスを交換し、再実行`iisreset`。</span><span class="sxs-lookup"><span data-stu-id="544a4-253">Replace the temporary web.config file in the Project Service directory with the original (renamed to web.config), and then rerun  `iisreset`.</span></span>
    
## <a name="setting-other-references"></a><span data-ttu-id="544a4-254">その他の参照を設定する</span><span class="sxs-lookup"><span data-stu-id="544a4-254">Setting other references</span></span>
<span data-ttu-id="544a4-255"><a name="pj15_PrerequisitesWCF_OtherReferences"> </a></span><span class="sxs-lookup"><span data-stu-id="544a4-255"></span></span>

<span data-ttu-id="544a4-256">プロジェクトのサーバー アプリケーションは、多くの場合、SharePoint 2013 web サービスなどのサービスを使用します。</span><span class="sxs-lookup"><span data-stu-id="544a4-256">Project Server applications often use other services, such as SharePoint 2013 web services.</span></span> <span data-ttu-id="544a4-257">他のサービスまたは参照する必要がある場合は、コード例に記載されています。</span><span class="sxs-lookup"><span data-stu-id="544a4-257">If other services or references are required, they are noted in the code example.</span></span>
  
<span data-ttu-id="544a4-258">コード サンプルのローカル参照は、サンプルの上部の**using**ステートメントに表示されます。</span><span class="sxs-lookup"><span data-stu-id="544a4-258">Local references for the code sample are listed in **using** statements at the top of the sample.</span></span> 
  
1. <span data-ttu-id="544a4-259">**ソリューション エクスプローラー**で、[**参照設定**] フォルダーを右クリックし、[**参照の追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="544a4-259">In **Solution Explorer**, right-click the **References** folder, and then choose **Add Reference**.</span></span>
    
2. <span data-ttu-id="544a4-p139">[**参照**] をクリックして、以前にコピーした Project Server の DLL を格納した場所を参照します。必要な DLL を選択し、[**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="544a4-p139">Choose **Browse**, and then browse to the location where you stored the Project Server DLLs that you copied previously. Choose the DLLs that you want, and then choose **OK**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="544a4-262">開発用コンピューター上のアセンブリのバージョンがターゲット Project Server コンピューターのものと厳密に一致していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="544a4-262">Ensure that the assembly versions on your development computer exactly match those on the target Project Server computer.</span></span> 
  
## <a name="adding-a-service-configuration-file"></a><span data-ttu-id="544a4-263">サービス構成ファイルを追加する</span><span class="sxs-lookup"><span data-stu-id="544a4-263">Adding a service configuration file</span></span>
<span data-ttu-id="544a4-264"><a name="pj15_PrerequisitesWCF_AddConfig"> </a></span><span class="sxs-lookup"><span data-stu-id="544a4-264"></span></span>

<span data-ttu-id="544a4-p140">アプリケーションがプログラムによって WCF サービスを構成する場合、サービス構成ファイルは使用されません。それ以外の場合、Windows アプリケーションまたはコンソール アプリケーションでは app.config ファイルの **system.serviceModel** 要素を使用し、Web アプリケーションでは web.config ファイルの **system.serviceModel** をインクルードします。app.config ファイルの使用方法や、WCF サービスをプログラムで構成する方法については、「[[ウォークスルー] WCF を使用して PSI アプリケーションを開発する](http://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="544a4-p140">If an application programmatically configures the WCF services, it does not use a service configuration file. Otherwise, a Windows application or console application uses the **system.serviceModel** element in an app.config file; a web application includes **system.serviceModel** in web.config. For more information about using an app.config file or programmatically configuring the WCF services, see [Walkthrough: Developing PSI applications using WCF](http://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx).</span></span>
  
<span data-ttu-id="544a4-267">サービス プロキシのソース ファイルが生成されると、SvcUtil.exe コマンドは、output.config ファイルに app.config ファイルで既定の**system.serviceModel**要素の基になるか、web.config ファイルにも作成されます。</span><span class="sxs-lookup"><span data-stu-id="544a4-267">When it generates a service proxy source file, the SvcUtil.exe command also creates an output.config file that is the basis for the default **system.serviceModel** element in an app.config file or web.config file.</span></span> <span data-ttu-id="544a4-268">Project 2013 SDK ダウンロードには、サンプルの output.config ファイルが含まれています`Documentation\IntelliSense\WCF\Source.zip`。</span><span class="sxs-lookup"><span data-stu-id="544a4-268">The Project 2013 SDK download includes a sample output.config file in  `Documentation\IntelliSense\WCF\Source.zip`.</span></span> <span data-ttu-id="544a4-269">などの output.config の既定のファイル SvcUtil.exe を作成するリソースのサービスには、 **BasicHttpBinding_Resource**および**BasicHttpBinding_Resource1**という名前の 2 つのバインディングが含まれています。</span><span class="sxs-lookup"><span data-stu-id="544a4-269">For example, the default output.config file that SvcUtil.exe creates for the Resource service includes two bindings, named **BasicHttpBinding_Resource** and **BasicHttpBinding_Resource1**.</span></span> <span data-ttu-id="544a4-270">**クライアント**要素には、2 つの既定のエンドポイントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="544a4-270">The **client** element includes two default endpoints.</span></span> <span data-ttu-id="544a4-271">1 つのエンドポイントは、セキュリティで保護されたアドレスへのアクセス、HTTP ポート 32843 では次のようにポート 32843、通常のアクセスは、他の.</span><span class="sxs-lookup"><span data-stu-id="544a4-271">One endpoint is for the secure access to the HTTP address on port 32843 and the other is for normal access on port 32843, as follows:</span></span> 
  
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

<span data-ttu-id="544a4-p142">PSI サービス構成では、既定のバインドやエンドポイントを使用しません。Project Server では、バックエンド サービスの呼び出しでルーターとして動作するフロントエンド ProjectServer.svc を介してアプリケーションが PSI サービスにアクセスする必要があります。app.config ファイルを作成するには、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="544a4-p142">PSI service configuration does not use the default bindings and endpoints. Project Server requires that applications access PSI services through the front-end ProjectServer.svc, which acts as a router for calls to the back-end services. To create the app.config file, do the following steps:</span></span>
  
1. <span data-ttu-id="544a4-275">ProjectServerServices.dll プロキシ アセンブリへの参照を設定した場合、またはサービスのプロキシのソース ファイルを追加する場合は、アプリケーションに app.config ファイルが含まれていません。</span><span class="sxs-lookup"><span data-stu-id="544a4-275">If you set a reference to the ProjectServerServices.dll proxy assembly, or add the proxy source file for a service, the application does not contain an app.config file.</span></span> <span data-ttu-id="544a4-276">Visual Studio プロジェクトに新しい項目を追加します。</span><span class="sxs-lookup"><span data-stu-id="544a4-276">Add a new item to the Visual Studio project.</span></span> <span data-ttu-id="544a4-277">**新しい項目の追加**] ダイアログ ボックスで**アプリケーション構成ファイル**のテンプレートを選択、app.config という名前を付けますし、**追加**します。</span><span class="sxs-lookup"><span data-stu-id="544a4-277">In the **Add New Item** dialog box, choose the **Application Configuration File** template, name it app.config, and then choose **Add**.</span></span>
    
2. <span data-ttu-id="544a4-278">App.config ファイル内のすべてのテキストを削除し、ファイルに次のコードをコピーします。</span><span class="sxs-lookup"><span data-stu-id="544a4-278">Delete all text in the app.config file, and then copy the following code into the file.</span></span> <span data-ttu-id="544a4-279">バインディングは同じ例を使用することができます`basicHttpConf`、サービス エンドポイントごとにします。</span><span class="sxs-lookup"><span data-stu-id="544a4-279">You can use the same binding, for example  `basicHttpConf`, for each service endpoint.</span></span> <span data-ttu-id="544a4-280">、複数のバインディングを使用する場合など、HTTP と HTTPS の両方のプロトコルをバインドするのには作成する必要があるプロトコルごとにバインドします。</span><span class="sxs-lookup"><span data-stu-id="544a4-280">If you want to use more than one binding, for example, to bind both HTTP and HTTPS protocols, you must create a binding for each protocol.</span></span>
    
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

3. <span data-ttu-id="544a4-281">交換`ServerName/ProjectServerName`サーバーに、Project Web App インスタンスの名前を持つクライアント エンドポイントのアドレスにします。</span><span class="sxs-lookup"><span data-stu-id="544a4-281">Replace  `ServerName/ProjectServerName` in the client endpoint address with the name of your server and Project Web App instance.</span></span> 
    
4. <span data-ttu-id="544a4-282">交換`ServiceName`リソースなど、PSI サービスの名前です。</span><span class="sxs-lookup"><span data-stu-id="544a4-282">Replace  `ServiceName` with the name of the PSI service, such as Resource.</span></span> <span data-ttu-id="544a4-283">たとえば、サービス名のすべての 3 つを交換することを確認します。</span><span class="sxs-lookup"><span data-stu-id="544a4-283">Ensure that you replace all three instances of the service name, for example:</span></span>
    
    ```XML
        <endpoint address="http://myserver/pwa/_vti_bin/PSI/ProjectServer.svc"
            behaviorConfiguration="basicHttpBehavior" binding="basicHttpBinding"
            bindingConfiguration="basicHttpConf" 
            contract="SvcResource.Resource"
            name="basicHttp_Resource" />
    ```

5. <span data-ttu-id="544a4-p146">複数の PSI サービスを使用するには、サービスごとに、またサービスが使用する **binding** ごとに、1 つの **endpoint** 要素を作成します。たとえば、以下のエンドポイントでは、Project サービスと QueueSystem サービスで基本的な HTTP バインドを使用するようにクライアントを構成しています。</span><span class="sxs-lookup"><span data-stu-id="544a4-p146">To use more than one PSI service, create one **endpoint** element for each service, and for each **binding** element that service uses. For example, the following endpoints configure the client to use the basic HTTP binding for the Project service and the QueueSystem service.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="544a4-286">アプリケーションの実行時に、サーバーがビジー状態である、または HTTP 要求が許可されていないことを示すエラーが表示される場合は、app.config ファイルのエンドポイント アドレスが正しいことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="544a4-286">If you run an application and get an error that the server is too busy, or that the HTTP request is unauthorized, ensure that the endpoint addresses are correct in the app.config file.</span></span> 
  
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

<span data-ttu-id="544a4-287">App.config ファイルを編集するには、Visual Studio で**WCF サービス構成エディター**を使用する ([**ツール**] メニュー)。</span><span class="sxs-lookup"><span data-stu-id="544a4-287">You can edit an app.config file by using the **WCF Service Configuration Editor** in Visual Studio (on the **Tools** menu).</span></span> <span data-ttu-id="544a4-288">図 4 は、 **Microsoft のサービス構成エディター** ] ダイアログ ボックスで、**契約**の要素を設定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="544a4-288">Figure 4 shows how to set the **contract** element in the **Microsoft Service Configuration Editor** dialog box.</span></span> <span data-ttu-id="544a4-289">ソリューションでは、PSI プロキシ アセンブリを使用されている場合に ProjectServerServices.dll を開き、 `bin\debug` Visual Studio のソリューションのディレクトリです。</span><span class="sxs-lookup"><span data-stu-id="544a4-289">If the solution is using the PSI proxy assembly, open ProjectServerServices.dll in the  `bin\debug` directory of the Visual Studio solution.</span></span> <span data-ttu-id="544a4-290">**コントラクト型ブラウザー** ] ダイアログ ボックスには、(図 5 を参照)、WCF サービス コントラクトのすべてが表示されます。</span><span class="sxs-lookup"><span data-stu-id="544a4-290">The **Contract Type Browser** dialog box shows all of the WCF service contracts (see Figure 5).</span></span> 
  
<span data-ttu-id="544a4-291">**図 4. WCF サービス構成エディターの使用**</span><span class="sxs-lookup"><span data-stu-id="544a4-291">**Figure 4. Using the WCF Service Configuration Editor**</span></span>

<span data-ttu-id="544a4-292">![WCF サービス構成エディターを使用してください。](media/pj15_PrerequisitesWCF_ServiceConfigurationEditor.gif "WCF サービス構成エディターを使用してください。")</span><span class="sxs-lookup"><span data-stu-id="544a4-292">![Using the WCF Service Configuration Editor](media/pj15_PrerequisitesWCF_ServiceConfigurationEditor.gif "Using the WCF Service Configuration Editor")</span></span>
  
<span data-ttu-id="544a4-293">ソリューションは、wcfResource.cs など、サービスのプロキシ ファイルを使用している場合アプリケーションをコンパイルし、実行可能ファイルを開き、`bin\debug`ディレクトリです。</span><span class="sxs-lookup"><span data-stu-id="544a4-293">If the solution is using a service proxy file, such as wcfResource.cs, compile the application and then open the executable file in the  `bin\debug` directory.</span></span> <span data-ttu-id="544a4-294">App.config ファイルを編集の詳細についてを参照してください[チュートリアル: PSI の開発アプリケーションが WCF を使用して](http://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="544a4-294">For more information about editing the app.config file, see [Walkthrough: Developing PSI applications using WCF](http://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx).</span></span>
  
<span data-ttu-id="544a4-295">**図 5. WCF サービス構成エディターでのコントラクト型ブラウザーの使用**</span><span class="sxs-lookup"><span data-stu-id="544a4-295">**Figure 5. Using the Contract Type Browser in the WCF Service Configuration Editor**</span></span>

<span data-ttu-id="544a4-296">![コントラクト型ブラウザーを使用してください。](media/pj15_PrerequisitesWCF_ContractTypeBrowser.gif "コントラクト型ブラウザーを使用してください。")</span><span class="sxs-lookup"><span data-stu-id="544a4-296">![Using the Contract Type Browser](media/pj15_PrerequisitesWCF_ContractTypeBrowser.gif "Using the Contract Type Browser")</span></span>
  
## <a name="using-multiple-authentication"></a><span data-ttu-id="544a4-297">複数の認証を使用する</span><span class="sxs-lookup"><span data-stu-id="544a4-297">Using multiple authentication</span></span>
<span data-ttu-id="544a4-298"><a name="pj15_PrerequisitesWCF_ClaimsMultiAuth"> </a></span><span class="sxs-lookup"><span data-stu-id="544a4-298"></span></span>

<span data-ttu-id="544a4-299">Windows 認証またはフォーム認証では、オンプレミスの Project Server のユーザーの認証はクレーム処理では、SharePoint によって行われます。</span><span class="sxs-lookup"><span data-stu-id="544a4-299">Authentication of on-premises Project Server users, whether by Windows authentication or Forms authentication, is done through claims processing in SharePoint.</span></span> <span data-ttu-id="544a4-300">複数の認証では、Project Web App が提供されている web アプリケーションが Windows 認証とフォーム ベース認証の両方をサポートしていることを意味します。</span><span class="sxs-lookup"><span data-stu-id="544a4-300">Multiple authentication means that the web application on which Project Web App is provisioned supports both Windows authentication and Forms-based authentication.</span></span> <span data-ttu-id="544a4-301">場合は、請求処理は、ユーザーの認証の種類を判断できないために次のエラーでは、Windows 認証を使用する WCF サービスへの呼び出しが失敗します。</span><span class="sxs-lookup"><span data-stu-id="544a4-301">If that is the case, any call to a WCF service that uses Windows authentication will fail with the following error, because the claims process cannot determine which type of user to authenticate:</span></span>
  
`The server was unable to process the request due to an internal error. For more information about the error, either turn on Include ExceptionDetailInFaults (either from ServiceBehaviorAttribute or from the <serviceDebug> configuration behavior) on the server in order to send the exception information back to the client, or turn on tracing as per the Microsoft .NET Framework 3.0 SDK documentation and inspect the server trace logs.`

<span data-ttu-id="544a4-p150">WCF のこの問題を修正するには、PSI メソッドのすべての呼び出しをそれぞれの PSI サービスに対して定義される **OperationContextScope** 内に置く必要があります。ただし、複数のサービスに対するスコープを入れ子にしないでください。たとえば、Resource サービスと Project サービスを使用する際には、それぞれの呼び出しセットを各自のスコープ内に置く必要があります。</span><span class="sxs-lookup"><span data-stu-id="544a4-p150">To fix the problem for WCF, all calls to PSI methods should be within an **OperationContextScope** that is defined for each PSI service. Do not nest scopes for multiple services; for example, when using calls to the Resource and Project services, each set of calls should be within its own scope.</span></span> 
  
<span data-ttu-id="544a4-304">次の例では、アプリケーション内のすべての**OperationContextScope**セクションから、 **DisableFormsAuth**メソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="544a4-304">In the following example, the **DisableFormsAuth** method can be called from every **OperationContextScope** section in an application.</span></span> <span data-ttu-id="544a4-305">メソッドは、 _isWindowsAuth_パラメーターが**false**の場合、フォーム認証を行えるように、フォーム認証を無効に設定されているヘッダーの値を削除します。</span><span class="sxs-lookup"><span data-stu-id="544a4-305">The method removes any header value that previously disabled Forms authentication, so that Forms authentication can proceed if the  _isWindowsAuth_ parameter is **false**.</span></span> <span data-ttu-id="544a4-306">_IsWindowsAuth_が**true**の場合、 **DisableFormsAuth**メソッドには、フォーム認証が無効になります。</span><span class="sxs-lookup"><span data-stu-id="544a4-306">If  _isWindowsAuth_ is **true**, the **DisableFormsAuth** method disables Forms authentication.</span></span> 
  
<span data-ttu-id="544a4-307">**WcfSample** メソッド内の **projectClient** オブジェクトは、PSI の **SvcProject.ProjectClient** クラスのインスタンスです。</span><span class="sxs-lookup"><span data-stu-id="544a4-307">In the **WcfSample** method, the **projectClient** object is an instance of the PSI **SvcProject.ProjectClient** class.</span></span> 
  
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
> <span data-ttu-id="544a4-p152">**OperationContextScope** 内での PSI 呼び出しが必要になるのは、複数認証の環境で動作するアプリケーションのみです。Project Server で Windows 認証のみを使用する場合、スコープの設定や、フォーム認証を無効にする Web 要求ヘッダーの追加は不要です。</span><span class="sxs-lookup"><span data-stu-id="544a4-p152">Making PSI calls within an **OperationContextScope** is required only for applications that run in a multiple authentication environment. If Project Server uses only Windows authentication, it is not necessary to set a scope and add a web request header that disables Forms authentication.</span></span> 
> 
> <span data-ttu-id="544a4-310">ASMX ベースのアプリケーション用の修正プログラムは、異なります。</span><span class="sxs-lookup"><span data-stu-id="544a4-310">The fix for an ASMX-based application is different.</span></span> <span data-ttu-id="544a4-311">詳細については、[プロジェクト内の ASMX ベースのコード サンプルの前提条件](prerequisites-for-asmx-based-code-samples-in-project.md)で*を使用する複数の認証*] セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="544a4-311">For more information, see the  *Using multiple-authentication*  section in [Prerequisites for ASMX-based code samples in Project](prerequisites-for-asmx-based-code-samples-in-project.md).</span></span> 
  
## <a name="changing-values-of-generic-constants"></a><span data-ttu-id="544a4-312">一般的な定数の値を変更する</span><span class="sxs-lookup"><span data-stu-id="544a4-312">Changing values of generic constants</span></span>
<span data-ttu-id="544a4-313"><a name="pj15_PrerequisitesWCF_ChangeValues"> </a></span><span class="sxs-lookup"><span data-stu-id="544a4-313"></span></span>

<span data-ttu-id="544a4-314">ほとんどのサンプルでは、更新する必要が、サンプルを動作させるため正しく、環境内の 1 つまたは複数の変数があります。</span><span class="sxs-lookup"><span data-stu-id="544a4-314">Most samples have one or more variables that you must update for the sample to work properly in your environment.</span></span> <span data-ttu-id="544a4-315">次の例では、SSL がインストールされている場合は HTTP プロトコルではなく HTTPS プロトコルを使用します。</span><span class="sxs-lookup"><span data-stu-id="544a4-315">In the following example, if you have SSL installed, use the HTTPS protocol instead of the HTTP protocol.</span></span> <span data-ttu-id="544a4-316">_サーバー名_を使用しているサーバーの名前に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="544a4-316">Replace  _ServerName_ with the name of the server that you are using.</span></span> <span data-ttu-id="544a4-317">_ProjectServerName_を PWA など、プロジェクトのサーバー サイトの仮想ディレクトリ名に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="544a4-317">Replace  _ProjectServerName_ with the virtual directory name of your project server site, such as PWA.</span></span> 
  
```cs
const string PROJECT_SERVER_URI = "http://ServerName/ProjectServerName/";
```

<span data-ttu-id="544a4-318">ほかに変更が必要な変数があれば、コード サンプルの上部に記載されています。</span><span class="sxs-lookup"><span data-stu-id="544a4-318">Any other variables that you must change are noted at the top of the code example.</span></span>
  
## <a name="verifying-the-results"></a><span data-ttu-id="544a4-319">結果を確認する</span><span class="sxs-lookup"><span data-stu-id="544a4-319">Verifying the results</span></span>
<span data-ttu-id="544a4-320"><a name="pj15_PrerequisitesWCF_Verify"> </a></span><span class="sxs-lookup"><span data-stu-id="544a4-320"></span></span>

<span data-ttu-id="544a4-321">取得し、コード サンプルの結果を解釈する常に簡単ではありません。</span><span class="sxs-lookup"><span data-stu-id="544a4-321">Getting and interpreting results from a code sample is not always straightforward.</span></span> <span data-ttu-id="544a4-322">たとえば、プロジェクトを作成する場合は、Project Web App の [プロジェクト センター] ページに表示するプロジェクトを発行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="544a4-322">For example, if you create a project, you must publish the project before it can appear on the Project Center page in Project Web App.</span></span>
  
<span data-ttu-id="544a4-323">コード サンプルの結果は、いくつかの方法で確認できます。たとえば、次のような方法があります。</span><span class="sxs-lookup"><span data-stu-id="544a4-323">You can verify code sample results in several ways, for example:</span></span>
  
- <span data-ttu-id="544a4-324">プロジェクト評価のためのクライアントを使用して、Project Server コンピューターからプロジェクトを開くし、目的のアイテムを表示します。</span><span class="sxs-lookup"><span data-stu-id="544a4-324">Use the Project Professional 2013 client to open the project from the Project Server computer, and view the items that you want.</span></span>
    
- <span data-ttu-id="544a4-325">Project Web App の [プロジェクト センター] ページで発行されたプロジェクトを表示する ( `http://ServerName/ProjectServerName/projects.aspx`)。</span><span class="sxs-lookup"><span data-stu-id="544a4-325">View published projects on the Project Center page of Project Web App ( `http://ServerName/ProjectServerName/projects.aspx`).</span></span>
    
- <span data-ttu-id="544a4-326">Project Web App では、キューのログを表示します。</span><span class="sxs-lookup"><span data-stu-id="544a4-326">View the Queue log in Project Web App.</span></span> <span data-ttu-id="544a4-327">サーバー設定] ページを開く (右上隅で、[**設定**] アイコンを選択します)、**個人用の設定**] セクションで [**自分のキュー ジョブ**を選択し、( `http://ServerName/ProjectServerName/MyJobs.aspx`)。</span><span class="sxs-lookup"><span data-stu-id="544a4-327">Open the Server Settings page (choose the **Settings** icon in the top-right corner), and then choose **My Queued Jobs** under the **Personal Settings** section (  `http://ServerName/ProjectServerName/MyJobs.aspx`).</span></span> <span data-ttu-id="544a4-328">**ビュー** 」ドロップ ダウン リストで、ジョブの状態で並べ替えることができます。</span><span class="sxs-lookup"><span data-stu-id="544a4-328">In the **View** drop-down list, you can sort by the job status.</span></span> <span data-ttu-id="544a4-329">既定の状態が**進行中で過去 1 週間のジョブの失敗です**。</span><span class="sxs-lookup"><span data-stu-id="544a4-329">The default status is **In Progress and Failed Jobs in the Past Week**.</span></span> 
    
- <span data-ttu-id="544a4-330">Project Web App の [サーバー設定] ページを使用して ( `http://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`) とすべてのキュー ジョブの管理、削除、またはチェックインのエンタープライズ オブジェクトを強制的にします。</span><span class="sxs-lookup"><span data-stu-id="544a4-330">Use the Server Settings page in Project Web App ( `http://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`) to manage all queue jobs and delete or force check-in enterprise objects.</span></span> <span data-ttu-id="544a4-331">[サーバーの設定] ページで、これらのリンクにアクセスする管理者の権限がある必要があります。</span><span class="sxs-lookup"><span data-stu-id="544a4-331">You must have administrative permissions to access those links on the Server Settings page.</span></span>
    
- <span data-ttu-id="544a4-p158">**Microsoft SQL Server Management Studio** を使用して、Project Server データベースのテーブルにクエリを実行します。たとえば、以下のクエリを使用して、MSP_WORKFLOW_STAGE_PDPS テーブルの先頭 200 行を選択し、ワークフロー ステージのプロジェクト詳細ページ (PDP) に関する情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="544a4-p158">Use **Microsoft SQL Server Management Studio** to run a query on a table of a Project Server database. For example, use the following query to select the top 200 rows of the MSP_WORKFLOW_STAGE_PDPS table to show information about the project detail pages (PDPs) in workflow stages.</span></span> 
    
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

## <a name="cleaning-up"></a><span data-ttu-id="544a4-334">クリーンアップする</span><span class="sxs-lookup"><span data-stu-id="544a4-334">Cleaning up</span></span>
<span data-ttu-id="544a4-335"><a name="pj15_PrerequisitesWCF_Cleanup"> </a></span><span class="sxs-lookup"><span data-stu-id="544a4-335"></span></span>

<span data-ttu-id="544a4-336">一部のコード サンプルをテストした後、エンタープライズ オブジェクトと設定を削除またはリセットする必要があります。</span><span class="sxs-lookup"><span data-stu-id="544a4-336">After you test some code samples, there are enterprise objects and settings that should be deleted or reset.</span></span> <span data-ttu-id="544a4-337">Project Web App の [サーバー設定] ページを使用するにはエンタープライズ ・ データを管理する ( `http://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`)。</span><span class="sxs-lookup"><span data-stu-id="544a4-337">You can use the Server Settings page in Project Web App to manage enterprise data ( `http://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`).</span></span> <span data-ttu-id="544a4-338">[サーバー設定] ページのリンクを使用すると、古いアイテムを削除する、強制的にチェックインのプロジェクト、すべてのユーザーのジョブ キューの管理、その他の管理タスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="544a4-338">Links on the Server Settings page enable you to delete old items, force check-in projects, manage the job queue for all users, and perform other administrative tasks.</span></span>
  
<span data-ttu-id="544a4-339">以下に、コード サンプル実行後の一般的なクリーンアップ作業で使用する、[サーバー設定] ページ上のリンクの一部を示します。</span><span class="sxs-lookup"><span data-stu-id="544a4-339">Following are some of the links on the Server Settings page to use for typical cleanup activities after running code samples:</span></span>
  
- <span data-ttu-id="544a4-340">**エンタープライズ ユーザー設定フィールドと参照テーブル**</span><span class="sxs-lookup"><span data-stu-id="544a4-340">**Enterprise Custom Fields and Lookup Tables**</span></span>
    
- <span data-ttu-id="544a4-341">**キュー ジョブの管理**</span><span class="sxs-lookup"><span data-stu-id="544a4-341">**Manage Queue Jobs**</span></span>
    
- <span data-ttu-id="544a4-342">**エンタープライズ オブジェクトの削除**</span><span class="sxs-lookup"><span data-stu-id="544a4-342">**Delete Enterprise Objects**</span></span>
    
- <span data-ttu-id="544a4-343">**エンタープライズ オブジェクトの強制チェックイン**</span><span class="sxs-lookup"><span data-stu-id="544a4-343">**Force Check-in Enterprise Objects**</span></span>
    
- <span data-ttu-id="544a4-344">**エンタープライズ プロジェクトの種類**</span><span class="sxs-lookup"><span data-stu-id="544a4-344">**Enterprise Project Types**</span></span>
    
- <span data-ttu-id="544a4-345">**ワークフロー フェーズ**</span><span class="sxs-lookup"><span data-stu-id="544a4-345">**Workflow Phases**</span></span>
    
- <span data-ttu-id="544a4-346">**ワークフロー ステージ**</span><span class="sxs-lookup"><span data-stu-id="544a4-346">**Workflow Stages**</span></span>
    
- <span data-ttu-id="544a4-347">**プロジェクト詳細ページ**</span><span class="sxs-lookup"><span data-stu-id="544a4-347">**Project Detail Pages**</span></span>
    
- <span data-ttu-id="544a4-348">**タイムシート期間**</span><span class="sxs-lookup"><span data-stu-id="544a4-348">**Time Reporting Periods**</span></span>
    
- <span data-ttu-id="544a4-349">**タイムシートの設定および既定値**</span><span class="sxs-lookup"><span data-stu-id="544a4-349">**Timesheet Settings and Defaults**</span></span>
    
- <span data-ttu-id="544a4-350">**管理用行の分類**</span><span class="sxs-lookup"><span data-stu-id="544a4-350">**Line Classifications**</span></span>
    
<span data-ttu-id="544a4-351">特定の Project Web App サーバーの設定ページではなく、Project Web App インスタンスごとに、SharePoint Server 2013 では、追加の設定が管理されます。</span><span class="sxs-lookup"><span data-stu-id="544a4-351">Additional settings are managed by SharePoint Server 2013 for each Project Web App instance, rather than by a specific Project Web App Server Settings page.</span></span> <span data-ttu-id="544a4-352">SharePoint サーバーの全体管理アプリケーションで、**アプリケーションの全般的な設定**を選択し、**プロジェクトのサーバーの設定**、[**管理**] を選択を [サーバーの設定] ページで、ドロップダウン ボックスの一覧で、Project Web App インスタンスを選択.</span><span class="sxs-lookup"><span data-stu-id="544a4-352">In the SharePoint Central Administration application, choose **General Application Settings**, choose **Manage** under **Project Server Settings**, and then choose the Project Web App instance in the drop-down list on the Server Settings page.</span></span> <span data-ttu-id="544a4-353">たとえば、選択した Project Web App インスタンスのイベント ハンドラーを追加、削除する**サーバー側のイベント ハンドラー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="544a4-353">For example, choose **Server Side Event Handlers** to add or delete event handlers for the selected Project Web App instance.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="544a4-354">関連項目</span><span class="sxs-lookup"><span data-stu-id="544a4-354">See also</span></span>

- [<span data-ttu-id="544a4-355">プロジェクト内の ASMX ベースのコード サンプルの前提条件</span><span class="sxs-lookup"><span data-stu-id="544a4-355">Prerequisites for ASMX-based code samples in Project</span></span>](prerequisites-for-asmx-based-code-samples-in-project.md)   
- [<span data-ttu-id="544a4-356">チュートリアル: WCF を使用して PSI アプリケーションを開発します。</span><span class="sxs-lookup"><span data-stu-id="544a4-356">Walkthrough: Developing PSI applications using WCF</span></span>](http://msdn.microsoft.com/library/65707234-c3da-44e4-8364-32a6be28f645%28Office.15%29.aspx)   
- [<span data-ttu-id="544a4-357">WCF で偽装を使用します。</span><span class="sxs-lookup"><span data-stu-id="544a4-357">Use Impersonation with WCF</span></span>](http://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)  
- [<span data-ttu-id="544a4-358">プロジェクト PSI リファレンスの概要</span><span class="sxs-lookup"><span data-stu-id="544a4-358">Project PSI reference overview</span></span>](project-psi-reference-overview.md) 
- [<span data-ttu-id="544a4-359">SharePoint デベロッパー センター</span><span class="sxs-lookup"><span data-stu-id="544a4-359">SharePoint Developer Center</span></span>](http://msdn.microsoft.com/en-us/sharepoint/default.aspx)
    

