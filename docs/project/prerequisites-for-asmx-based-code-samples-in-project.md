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
# <a name="prerequisites-for-asmx-based-code-samples-in-project"></a><span data-ttu-id="a3c93-104">プロジェクト内の ASMX ベースのコード サンプルの前提条件</span><span class="sxs-lookup"><span data-stu-id="a3c93-104">Prerequisites for ASMX-based code samples in Project</span></span>

<span data-ttu-id="a3c93-105">プロジェクト Server インターフェイス (PSI) のリファレンス トピックに含まれている ASMX ベースのコード サンプルを使用して Visual Studio でプロジェクトを作成するための情報について説明します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-105">Learn information to help you create projects in Visual Studio by using the ASMX-based code samples that are included in the Project Server Interface (PSI) reference topics.</span></span>
  
<span data-ttu-id="a3c93-106">[Project Server 2013 のクラス ライブラリと web サービスを参照](http://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx)するに含まれているコード サンプルの多くは、Office プロジェクト 2007 SDK で作成され、ASMX web サービスの標準的な形式を使用します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-106">Many of the code samples included in the [Project Server 2013 class library and web service reference](http://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) were originally created for the Office Project 2007 SDK, and use a standard format for ASMX web services.</span></span> <span data-ttu-id="a3c93-107">まだサンプルは、Project Server 2013 での作業し、コンソール アプリケーションにコピーし、完全な単位として実行するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="a3c93-107">The samples still work in Project Server 2013 and are designed to be copied into a console application and run as a complete unit.</span></span> <span data-ttu-id="a3c93-108">サンプルで例外が記載されています。</span><span class="sxs-lookup"><span data-stu-id="a3c93-108">Exceptions are noted in the sample.</span></span> 
  
<span data-ttu-id="a3c93-109">Project 2013 SDK の新しい PSI のサンプルは、Windows Communication Foundation (WCF) サービスを使用する形式に準拠しています。</span><span class="sxs-lookup"><span data-stu-id="a3c93-109">New PSI samples in the Project 2013 SDK conform to a format that uses Windows Communication Foundation (WCF) services.</span></span> <span data-ttu-id="a3c93-110">ASMX ベースのサンプルは、WCF サービスの使用に適合させることができます。</span><span class="sxs-lookup"><span data-stu-id="a3c93-110">The ASMX-based samples can also be adapted to use WCF services.</span></span> <span data-ttu-id="a3c93-111">この資料では、ASMX web サービスのサンプルを使用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-111">This article shows how to use the samples with ASMX web services.</span></span> <span data-ttu-id="a3c93-112">サンプルの WCF サービスの使用方法の詳細については、[プロジェクト内の WCF ベースのコード サンプルの前提条件](prerequisites-for-wcf-based-code-samples-in-project.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a3c93-112">For information about using the samples with WCF services, see [Prerequisites for WCF-based code samples in Project](prerequisites-for-wcf-based-code-samples-in-project.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="a3c93-113">PSI の ASMX web サービスのインタ フェースは、Project Server 2013 のでは使用されなくなりましたはまだサポートされています。</span><span class="sxs-lookup"><span data-stu-id="a3c93-113">The ASMX web service interface of the PSI is deprecated in Project Server 2013, but is still supported.</span></span> <span data-ttu-id="a3c93-114">クライアント側オブジェクト モデル (CSOM) では、アプリケーションを必要とするメソッドが含まれている場合、CSOM で新しいアプリケーションを開発する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a3c93-114">If the client-side object model (CSOM) includes the methods that your application requires, new applications should be developed with the CSOM.</span></span> <span data-ttu-id="a3c93-115">CSOM は、プロジェクトのオンラインまたは Project Server 2013 のオンプレミス インストールを操作するアプリケーションを有効にします。</span><span class="sxs-lookup"><span data-stu-id="a3c93-115">The CSOM enables applications to work with Project Online or an on-premises installation of Project Server 2013.</span></span> <span data-ttu-id="a3c93-116">それ以外の場合、アプリケーションは、PSI を使用する場合は、WCF インターフェイスは、ネットワーク通信のことをお勧めする技術であるを使用してください。</span><span class="sxs-lookup"><span data-stu-id="a3c93-116">Otherwise, if your application uses the PSI, it should use the WCF interface, which is the technology that we recommend for network communications.</span></span> <span data-ttu-id="a3c93-117">ASMX インターフェイスまたは WCF インターフェイスを使用するアプリケーションは、Project Server 2013 のオンプレミスのインストールでのみ操作できます。</span><span class="sxs-lookup"><span data-stu-id="a3c93-117">Applications that use the ASMX interface or the WCF interface can work only for on-premises installations of Project Server 2013.</span></span> <span data-ttu-id="a3c93-118">CSOM の詳細については、 [Project Server 2013 のアーキテクチャ](project-server-2013-architecture.md)および[Project 2013 のクライアント側オブジェクト モデル (CSOM)](client-side-object-model-csom-for-project-2013.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a3c93-118">For more information about the CSOM, see [Project Server 2013 architecture](project-server-2013-architecture.md) and [Client-side object model (CSOM) for Project 2013](client-side-object-model-csom-for-project-2013.md).</span></span> 
  
<span data-ttu-id="a3c93-119">コード サンプルを実行する前には、開発環境を設定し、アプリケーションを構成し、環境に一致するように一般的な定数の値を変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a3c93-119">Before running the code samples, you must set up the development environment, configure the application, and change generic constant values to match your environment.</span></span>
  
## <a name="setting-up-the-development-environment"></a><span data-ttu-id="a3c93-120">開発環境を設定する</span><span class="sxs-lookup"><span data-stu-id="a3c93-120">Setting up the development environment</span></span>
<span data-ttu-id="a3c93-121"><a name="pj15_PrerequisitesASMX_Setup"> </a></span><span class="sxs-lookup"><span data-stu-id="a3c93-121"></span></span>

1. <span data-ttu-id="a3c93-122">**テスト プロジェクトのサーバー システムを設定**します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-122">**Set up a test Project Server system**.</span></span>
    
   <span data-ttu-id="a3c93-p104">開発やテストを行う際には常にテスト Project Server システムを使用します。たとえコードが完全に動作しても、プロジェクト間の依存関係、レポート、またはその他の環境要因が意図しない結果を引き起こす可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a3c93-p104">Use a test Project Server system whenever you are developing or testing. Even when your code works perfectly, interproject dependencies, reporting, or other environmental factors can cause unintended consequences.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="a3c93-125">確認して、サーバー上の有効なユーザーは、PSI の呼び出し、アプリケーションを使用するための十分なアクセス許可があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-125">Ensure that you are a valid user on the server, and check that you have sufficient permissions for the PSI calls that your application uses.</span></span> <span data-ttu-id="a3c93-126">各 PSI メソッドのリファレンス トピックには、プロジェクトのサーバーのアクセス許可のテーブルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="a3c93-126">The reference topic for each PSI method includes a Project Server Permissions table.</span></span> <span data-ttu-id="a3c93-127">などの[Project.QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx)メソッドには、**新しいプロジェクト**グローバル アクセス権と、 **SaveProjectTemplate**アクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="a3c93-127">For example, the [Project.QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) method requires the global **NewProject** permission and the **SaveProjectTemplate** permission.</span></span> 
  
   <span data-ttu-id="a3c93-128">場合によっては、サーバー上でリモート デバッグを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a3c93-128">In some cases, you may have to do remote debugging on the server.</span></span> <span data-ttu-id="a3c93-129">SharePoint ファーム内の各プロジェクトのサーバー コンピューター上のイベント ハンドラー アセンブリをインストールして、一般に、プロジェクトのサーバーの設定] ページを使用して、Project Web App インスタンスのイベント ハンドラーを構成して、イベント ハンドラーを設定する必要がありますもSharePoint サーバーの管理のアプリケーションの設定です。</span><span class="sxs-lookup"><span data-stu-id="a3c93-129">You may also have to set up an event handler by installing an event handler assembly on each Project Server computer in the SharePoint farm, and then configuring the event handler for the Project Web App instance by using the Project Server Settings page in the General Application Settings of SharePoint Central Administration.</span></span>
    
2. <span data-ttu-id="a3c93-130">**開発用コンピューターを設定します。**</span><span class="sxs-lookup"><span data-stu-id="a3c93-130">**Set up a development computer.**</span></span>
    
   <span data-ttu-id="a3c93-p107">通常、PSI にはネットワーク経由でアクセスします。コード サンプルは、記載されている場合を除き、サーバーから分離されたクライアントで動作するように作られています。</span><span class="sxs-lookup"><span data-stu-id="a3c93-p107">You usually access the PSI through a network. The code samples are designed to be run on a client that is separate from the server, except where noted.</span></span>
    
   1. <span data-ttu-id="a3c93-133">**Visual Studio の適切なバージョンをインストールします。**</span><span class="sxs-lookup"><span data-stu-id="a3c93-133">**Install the correct version of Visual Studio.**</span></span> <span data-ttu-id="a3c93-134">場合を除き、これらのコードが書き込まれます Visual C# で。</span><span class="sxs-lookup"><span data-stu-id="a3c93-134">Except where noted, the code samples are written in Visual C#.</span></span> <span data-ttu-id="a3c93-135">Visual Studio 2010 または Visual Studio 2012 では、それらを使用できます。</span><span class="sxs-lookup"><span data-stu-id="a3c93-135">They can be used with Visual Studio 2010 or Visual Studio 2012.</span></span> <span data-ttu-id="a3c93-136">最新のサービス パックのインストールがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-136">Ensure that you have the most recent service pack installed.</span></span> 
        
   2. <span data-ttu-id="a3c93-137">**プロジェクト サーバー Dll を開発用コンピューターにコピーします。**</span><span class="sxs-lookup"><span data-stu-id="a3c93-137">**Copy Project Server DLLs to the development computer.**</span></span> <span data-ttu-id="a3c93-138">次のアセンブリをコピーする`[Program Files]\Microsoft Office Servers\15.0\Bin`開発用コンピューターに Project Server コンピューターにします。</span><span class="sxs-lookup"><span data-stu-id="a3c93-138">Copy the following assemblies from  `[Program Files]\Microsoft Office Servers\15.0\Bin` on the Project Server computer to the development computer:</span></span> 
        
      - <span data-ttu-id="a3c93-139">Microsoft.Office.Project.Server.Events.Receivers.dll</span><span class="sxs-lookup"><span data-stu-id="a3c93-139">Microsoft.Office.Project.Server.Events.Receivers.dll</span></span>
      - <span data-ttu-id="a3c93-140">Microsoft.Office.Project.Server.Library.dll</span><span class="sxs-lookup"><span data-stu-id="a3c93-140">Microsoft.Office.Project.Server.Library.dll</span></span>
        
   3. <span data-ttu-id="a3c93-141">コンパイルし、PSI の ASMX web サービスの ProjectServerServices.dll のプロキシ アセンブリを使用する方法の詳細については、 [PSI プロキシ アセンブリおよび IntelliSense の説明を使用して](#pj15_PrerequisitesASMX_BuildingProxy)参照してください。</span><span class="sxs-lookup"><span data-stu-id="a3c93-141">For information about how to compile and use the ProjectServerServices.dll proxy assembly for the ASMX web services in the PSI, see [Using a PSI proxy assembly and IntelliSense descriptions](#pj15_PrerequisitesASMX_BuildingProxy).</span></span>
    
3. <span data-ttu-id="a3c93-142">**IntelliSense ファイルをインストールします。**</span><span class="sxs-lookup"><span data-stu-id="a3c93-142">**Install the IntelliSense files.**</span></span>
    
    <span data-ttu-id="a3c93-143">Project 2013 SDK から更新された IntelliSense XML ファイルは、コピーである Project Server アセンブリのクラスとメンバーの IntelliSense の説明を使用するには、Project Server アセンブリが配置されている同じディレクトリにダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="a3c93-143">To use IntelliSense descriptions for classes and members in Project Server assemblies, copy the updated IntelliSense XML files from the Project 2013 SDK download to the same directory where the Project Server assemblies are located.</span></span> <span data-ttu-id="a3c93-144">たとえば、アプリケーションが Microsoft.Office.Project.Server.Library.dll アセンブリへの参照に設定されているディレクトリに Microsoft.Office.Project.Server.Library.xml ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="a3c93-144">For example, copy the Microsoft.Office.Project.Server.Library.xml file to the directory where your application will set a reference to the Microsoft.Office.Project.Server.Library.dll assembly.</span></span>
    
    <span data-ttu-id="a3c93-145">PSI web サービス用の IntelliSense の説明で CompileASMXProxyAssembly.cmd スクリプトを使用して、PSI プロキシ アセンブリを作成することを必要とする、 `Documentation\IntelliSense\WSDL` Project 2013 SDK ダウンロードのサブディレクトリです。</span><span class="sxs-lookup"><span data-stu-id="a3c93-145">IntelliSense descriptions for the PSI web services require that you create a PSI proxy assembly by using the CompileASMXProxyAssembly.cmd script in the  `Documentation\IntelliSense\WSDL` subdirectory in the Project 2013 SDK download.</span></span> <span data-ttu-id="a3c93-146">スクリプトは、ProjectServerServices.dll の ASMX ベースのプロキシ アセンブリを作成します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-146">The script creates the ASMX-based ProjectServerServices.dll proxy assembly.</span></span> <span data-ttu-id="a3c93-147">詳細については、SDK ダウンロードの [ReadMe_IntelliSense] ファイルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a3c93-147">For more information, see the [ReadMe_IntelliSense] file in the SDK download.</span></span> 
    
## <a name="creating-the-application-and-adding-a-web-service-reference"></a><span data-ttu-id="a3c93-148">アプリケーションを作成して Web サービス参照を追加する</span><span class="sxs-lookup"><span data-stu-id="a3c93-148">Creating the application and adding a web service reference</span></span>
<span data-ttu-id="a3c93-149"><a name="pj15_PrerequisitesASMX_Configure"> </a></span><span class="sxs-lookup"><span data-stu-id="a3c93-149"></span></span>

1. <span data-ttu-id="a3c93-150">**コンソール アプリケーションを作成します**。</span><span class="sxs-lookup"><span data-stu-id="a3c93-150">**Create a console application**.</span></span>
    
   <span data-ttu-id="a3c93-151">**[新しいプロジェクト**] ダイアログ ボックスのドロップダウン ボックスの一覧で、コンソール アプリケーションを作成するときは、 **.NET Framework 4**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-151">When you create a console application, in the drop-down list of the **New Project** dialog box, select **.NET Framework 4**.</span></span> <span data-ttu-id="a3c93-152">新しいアプリケーションには、PSI のコード例をコピーできます。</span><span class="sxs-lookup"><span data-stu-id="a3c93-152">You can copy the PSI example code into the new application.</span></span>
    
2. <span data-ttu-id="a3c93-153">**Asmx サービスに必要な参照を追加します。**</span><span class="sxs-lookup"><span data-stu-id="a3c93-153">**Add the reference required for ASMX.**</span></span>
    
   <span data-ttu-id="a3c93-154">ソリューション エクスプ ローラーで、 **System.Web.Services**への参照を追加します (図 1 を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="a3c93-154">In Solution Explorer, add a reference to **System.Web.Services** (see Figure 1).</span></span> 
    
   <span data-ttu-id="a3c93-155">**図 1 です。Visual Studio で参照を追加します。**</span><span class="sxs-lookup"><span data-stu-id="a3c93-155">**Figure 1. Adding a reference in Visual Studio**</span></span>

   <span data-ttu-id="a3c93-156">![Visual Studio で参照を追加します。](media/pj15_PrerequisitesASMX_AddReference.gif "Visual Studio で参照を追加します。")</span><span class="sxs-lookup"><span data-stu-id="a3c93-156">![Adding a reference in Visual Studio](media/pj15_PrerequisitesASMX_AddReference.gif "Adding a reference in Visual Studio")</span></span>
  
3. <span data-ttu-id="a3c93-157">**コードをコピー**します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-157">**Copy the code**.</span></span>
    
   <span data-ttu-id="a3c93-158">コード サンプル全体をコンソール アプリケーションの Program.cs ファイルにコピーします。</span><span class="sxs-lookup"><span data-stu-id="a3c93-158">Copy the complete code example into the Program.cs file of the console application.</span></span>
    
4. <span data-ttu-id="a3c93-159">**サンプル アプリケーションの名前空間を設定**します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-159">**Set the namespace for the sample application**.</span></span>
    
   <span data-ttu-id="a3c93-p113">サンプルの上部に記されている名前空間をアプリケーションの既定の名前空間に変更するか、アプリケーションの既定の名前空間をサンプルに合わせて変更することができます。アプリケーションの既定の名前空間は、アプリケーションのプロパティを変更することによって変更できます。</span><span class="sxs-lookup"><span data-stu-id="a3c93-p113">You can either change the namespace listed at the top of the sample to the application default namespace, or change the default application namespace to match the sample. You can change the default application namespace by changing the application properties.</span></span>
    
   <span data-ttu-id="a3c93-162">たとえば、 [QueueRenameProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueRenameProject.aspx)のコード サンプルは、 **Microsoft.SDK.Project.Samples.RenameProject**名前空間を持っています。</span><span class="sxs-lookup"><span data-stu-id="a3c93-162">For example, the code sample for [QueueRenameProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueRenameProject.aspx) has the namespace **Microsoft.SDK.Project.Samples.RenameProject**.</span></span> <span data-ttu-id="a3c93-163">Visual Studio プロジェクトの名前が**RenameProject**の場合は、Program.cs ファイルから名前空間をコピーし、プロジェクト**のプロパティ**] ウィンドウを開きます ( **[プロジェクト**] メニューで、 **RenameProject のプロパティ**] をクリックすると)。</span><span class="sxs-lookup"><span data-stu-id="a3c93-163">If the name of the Visual Studio project is **RenameProject**, copy the namespace from the Program.cs file, and then open the project **Properties** pane (on the **Project** menu, choose **RenameProject Properties**).</span></span> <span data-ttu-id="a3c93-164">[**アプリケーション**] タブで、名前空間を**既定の名前空間**] テキスト ボックスにコピーします。</span><span class="sxs-lookup"><span data-stu-id="a3c93-164">On the **Application** tab, copy the namespace into the **Default namespace** text box.</span></span> 
    
5. <span data-ttu-id="a3c93-165">**Web 参照を設定**します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-165">**Set the web references**.</span></span>
    
   <span data-ttu-id="a3c93-p115">多くの例では、1 つ以上の PSI Web サービスへの参照が必要です。これらは、サンプル自体、またはサンプルの前にあるコメントに示されています。Web 参照の適切な名前空間を取得するには、最初にアプリケーションの既定の名前空間を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a3c93-p115">Most examples require a reference to one or more of the PSI web services. These are listed in the sample itself or in comments that precede the sample. To get the correct namespace of the web references, ensure that you first set the default application namespace.</span></span>
    
   <span data-ttu-id="a3c93-169">PSI の ASMX Web サービス参照を追加する方法として次の 3 つがあります。</span><span class="sxs-lookup"><span data-stu-id="a3c93-169">There are three ways to add an ASMX web service reference for the PSI:</span></span>
    
   - <span data-ttu-id="a3c93-170">という名前の ProjectServerServices.dll、PSI プロキシ アセンブリをビルドし、アセンブリへの参照を設定します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-170">Build a PSI proxy assembly named ProjectServerServices.dll, and then set a reference to the assembly.</span></span> <span data-ttu-id="a3c93-171">IntelliSense を取得するには、これは、PSI の参照を追加するのには推奨される方法です。</span><span class="sxs-lookup"><span data-stu-id="a3c93-171">To get IntelliSense, this is the recommended way to add a PSI reference.</span></span> <span data-ttu-id="a3c93-172">[PSI プロキシ アセンブリおよび IntelliSense の説明を使用して](#pj15_PrerequisitesASMX_BuildingProxy)参照してください。</span><span class="sxs-lookup"><span data-stu-id="a3c93-172">See [Using a PSI proxy assembly and IntelliSense descriptions](#pj15_PrerequisitesASMX_BuildingProxy).</span></span>
    
   - <span data-ttu-id="a3c93-173">Wsdl.exe 出力からプロキシ ファイルを Visual Studio ソリューションに追加します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-173">Add a proxy file from the wsdl.exe output to the Visual Studio solution.</span></span> <span data-ttu-id="a3c93-174">[PSI プロキシ ファイルを追加する](#pj15_PrerequisitesASMX_AddingProxyFile)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a3c93-174">See [Adding a PSI proxy file](#pj15_PrerequisitesASMX_AddingProxyFile).</span></span>
    
   - <span data-ttu-id="a3c93-175">Web サービス参照を追加するには、Visual Studio を使用します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-175">Add a web service reference by using Visual Studio.</span></span> <span data-ttu-id="a3c93-176">[サービス参照の追加、web](#pj15_PrerequisitesASMX_AddingServiceReference)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a3c93-176">See [Adding a web service reference](#pj15_PrerequisitesASMX_AddingServiceReference).</span></span>

<span data-ttu-id="a3c93-177"><a name="pj15_PrerequisitesASMX_BuildingProxy"> </a></span><span class="sxs-lookup"><span data-stu-id="a3c93-177"></span></span>

### <a name="using-a-psi-proxy-assembly-and-intellisense-descriptions"></a><span data-ttu-id="a3c93-178">Intellisense の説明を備えた PSI プロキシ アセンブリを使用する</span><span class="sxs-lookup"><span data-stu-id="a3c93-178">Using a PSI proxy assembly and IntelliSense descriptions</span></span>

<span data-ttu-id="a3c93-179">ビルドしてで CompileASMXProxyAssembly.cmd スクリプトを使用して、PSI の ASMX ベース web サービスをすべての ProjectServerServices.dll のプロキシ アセンブリを使用して、 `Documentation\IntelliSense\WSDL` Project 2013 SDK ダウンロードのフォルダーです。</span><span class="sxs-lookup"><span data-stu-id="a3c93-179">You can build and use the ProjectServerServices.dll proxy assembly for all ASMX-based web services in the PSI, by using the CompileASMXProxyAssembly.cmd script in the  `Documentation\IntelliSense\WSDL` folder of the Project 2013 SDK download.</span></span> <span data-ttu-id="a3c93-180">ダウンロードへのリンクでは、 [Project 2013 開発者向けドキュメント](project-2013-developer-documentation.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a3c93-180">For a link to the download, see [Project 2013 developer documentation](project-2013-developer-documentation.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="a3c93-181">Source.zip からプロキシ ソース ファイルを抽出するときにファイル内のファイル、`Documentation\IntelliSense\WSDL\Source`は、Project 2013 SDK ダウンロードの発行日時点で現在のフォルダーです。</span><span class="sxs-lookup"><span data-stu-id="a3c93-181">When you extract the proxy source files from the Source.zip file, the files in the  `Documentation\IntelliSense\WSDL\Source` folder are current as of the publication date of the Project 2013 SDK download.</span></span> <span data-ttu-id="a3c93-182">生成するには、PSI プロキシ ソース ファイルは、Project Server コンピューター上の GenASMXProxyAssembly.cmd スクリプトの実行を更新しました。</span><span class="sxs-lookup"><span data-stu-id="a3c93-182">To generate updated PSI proxy source files, run the GenASMXProxyAssembly.cmd script on the Project Server computer.</span></span> <span data-ttu-id="a3c93-183">内のスクリプト、`Documentation\IntelliSense\WCF`フォルダーは、ASMX ベースのアプリケーションでは機能しません。</span><span class="sxs-lookup"><span data-stu-id="a3c93-183">The scripts in the  `Documentation\IntelliSense\WCF` folder do not work for ASMX-based applications.</span></span> <span data-ttu-id="a3c93-184">GenWCFProxyAssembly.cmd スクリプトでは、WCF サービスのソース コード ファイルを生成する、SvcUtil.exe を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-184">The GenWCFProxyAssembly.cmd script calls SvcUtil.exe, which generates source code files for the WCF services.</span></span> <span data-ttu-id="a3c93-185">WCF プロキシ ファイルには、さまざまな属性、チャネル ・ インタ フェース、および各 PSI サービス用のクライアント クラスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="a3c93-185">The WCF proxy files include different attributes, the channel interface, and a client class for each PSI service.</span></span> <span data-ttu-id="a3c93-186">たとえば、WCF ベースのリソースのサービスには、 **ResourceChannel**インターフェイス、**リソース**インターフェイス、および**ResourceClient**のクラスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="a3c93-186">For example, the WCF-based Resource service includes the **ResourceChannel** interface, the **Resource** interface, and the **ResourceClient** class.</span></span> <span data-ttu-id="a3c93-187">リソースの ASMX ベース web には、いくつかの異なるプロパティを使用して**リソース**クラスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="a3c93-187">The ASMX-based Resource web includes the **Resource** class with some different properties.</span></span> 
  
<span data-ttu-id="a3c93-188">次に、GenASMXProxyAssembly.cmd スクリプトを示します。このスクリプトは、PSI Web サービスの WSDL 出力ファイルを生成した後、アセンブリをコンパイルします。</span><span class="sxs-lookup"><span data-stu-id="a3c93-188">Following is the GenASMXProxyAssembly.cmd script that generates WSDL output files for the PSI web services, and then compiles the assembly.</span></span>
  
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

<span data-ttu-id="a3c93-189">スクリプトは ClassList_asmx.txt ファイルを使用します。このファイルには、サードパーティのデベロッパーが使用できる Web サービスのリストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="a3c93-189">The script uses the ClassList_asmx.txt file, which contains the list of web services that are available for third-party developers.</span></span>
  
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

<span data-ttu-id="a3c93-p121">このスクリプトは ProjectServerServices.dll という名前のアセンブリを作成します。WCF ベースのアセンブリ用の ProjectServerServices.dll と混同しないようにしてください。ProjectServerServices.xml IntelliSense ファイルを使用していずれかのアセンブリの使用を有効にする場合、アセンブリ名は同じです。</span><span class="sxs-lookup"><span data-stu-id="a3c93-p121">The scripts create an assembly named ProjectServerServices.dll. Avoid confusing it with ProjectServerServices.dll for the WCF-based assembly. The assembly names are the same, to enable using either assembly with the ProjectServerServices.xml IntelliSense file.</span></span>
  
<span data-ttu-id="a3c93-193">ASMX web サービスと WCF サービスの両方のスクリプトが作成した任意の名前空間は、どちらかのアセンブリの IntelliSense の ProjectServerServices.xml ファイルが機能するようにします。</span><span class="sxs-lookup"><span data-stu-id="a3c93-193">The arbitrary namespace created by the scripts for both the ASMX web services and the WCF services is the same, so that the ProjectServerServices.xml IntelliSense file works with either assembly.</span></span> <span data-ttu-id="a3c93-194">ASMX ベースのプロキシ アセンブリの WCF ベースのプロキシ アセンブリ内のリソース サービスの名前空間は**SvcResource**です。</span><span class="sxs-lookup"><span data-stu-id="a3c93-194">For example, the namespace of the Resource service in the WCF-based proxy assembly and in the ASMX-based proxy assembly is **SvcResource**.</span></span> <span data-ttu-id="a3c93-195">名前空間の名前を変更することができます、もちろん、-プロキシ アセンブリおよび IntelliSense の ProjectServerServices.xml ファイルに一致しているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-195">You can, of course, change the namespace names—if you ensure that they match in the proxy assembly and in the ProjectServerServices.xml IntelliSense file.</span></span>
  
<span data-ttu-id="a3c93-196">コード サンプルでは、PSI web サービスの名前空間に別の名前を使用する場合など**ProjectWebSvc**IntelliSense を実行するには、名前空間がプロキシ アセンブリと一致するように**SvcProject**を使用するサンプルを変更しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="a3c93-196">If a code sample uses a different name for a PSI web service namespace, for example **ProjectWebSvc**, for IntelliSense to work you must change the sample to use **SvcProject** so that the namespace matches the proxy assembly.</span></span> 
  
<span data-ttu-id="a3c93-197">ASMX ベースのプロキシ アセンブリを使用する利点は、すべて PSI web サービス名前空間が含まれています。複数の web 参照を作成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="a3c93-197">An advantage to using the ASMX-based proxy assembly is that it includes all PSI web service namespaces; you do not have to create multiple web references.</span></span> <span data-ttu-id="a3c93-198">別の利点としては、ProjectServerServices.dll プロキシ アセンブリへの参照を設定するのと同じディレクトリに ProjectServerServices.xml ファイルを追加する場合ことができます IntelliSense の説明、PSI のクラスおよびメンバーの。</span><span class="sxs-lookup"><span data-stu-id="a3c93-198">Another advantage is that, if you add the ProjectServerServices.xml file to the same directory where you set a reference to the ProjectServerServices.dll proxy assembly, you can get IntelliSense descriptions for the PSI classes and members.</span></span> <span data-ttu-id="a3c93-199">図 2 は、 **Project.QueueCreateProject**メソッドの IntelliSense のテキストを示します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-199">Figure 2 shows the IntelliSense text for the **Project.QueueCreateProject** method.</span></span> <span data-ttu-id="a3c93-200">詳細については、Project 2013 SDK ダウンロードの [IntelliSense] フォルダーで [ReadMe_IntelliSense] ファイルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a3c93-200">For more information, see the [ReadMe_IntelliSense] file in the IntelliSense folder of the Project 2013 SDK download.</span></span> 
  
<span data-ttu-id="a3c93-201">**図 2 になります。プロジェクトの web サービスのメソッドの IntelliSense を使用します。**</span><span class="sxs-lookup"><span data-stu-id="a3c93-201">**Figure 2. Using IntelliSense for a method in the Project web service**</span></span>

<span data-ttu-id="a3c93-202">![PSI サービスのメソッドの Intellisense を使用します。](media/pj15_PrerequisitesASMX_Intellisense.gif "PSI サービスのメソッドの Intellisense を使用します。")</span><span class="sxs-lookup"><span data-stu-id="a3c93-202">![Using Intellisense for a method in a PSI service](media/pj15_PrerequisitesASMX_Intellisense.gif "Using Intellisense for a method in a PSI service")</span></span>
  
<span data-ttu-id="a3c93-p124">このプロキシ アセンブリを使用する場合の欠点は、ソリューションが大規模になることと、ソリューションと共にプロキシ アセンブリの配布とインストールが必要になることです。また、プロキシ アセンブリ内と IntelliSense ファイル内で同じ名前空間を使用する必要があります (ただし、スクリプトと ProjectServerServices.xml IntelliSense ファイルを変更して、別々の名前空間を使用するようにした場合は例外です)。</span><span class="sxs-lookup"><span data-stu-id="a3c93-p124">Disadvantages to using the proxy assembly are that the solution is larger and you must distribute and install the proxy assembly with the solution. You must also use the same namespaces that are in the proxy assembly and IntelliSense files, unless you change the script and ProjectServerServices.xml IntelliSense file to use different namespaces.</span></span>
  
### <a name="adding-a-psi-proxy-file"></a><span data-ttu-id="a3c93-205">PSI プロキシ ファイルを追加する</span><span class="sxs-lookup"><span data-stu-id="a3c93-205">Adding a PSI proxy file</span></span>
<span data-ttu-id="a3c93-206"><a name="pj15_PrerequisitesASMX_AddingProxyFile"> </a></span><span class="sxs-lookup"><span data-stu-id="a3c93-206"></span></span>

<span data-ttu-id="a3c93-207">Project 2013 SDK ダウンロードには、プロキシ アセンブリに対して Wsdl.exe コマンドによって生成されるソース ファイルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="a3c93-207">The Project 2013 SDK download includes the source files generated by the Wsdl.exe command for the proxy assembly.</span></span> <span data-ttu-id="a3c93-208">Source.zip 内では、ソース ファイル、`Documentation\IntelliSense\ASMX`のサブディレクトリです。</span><span class="sxs-lookup"><span data-stu-id="a3c93-208">The source files are in Source.zip in the  `Documentation\IntelliSense\ASMX` subdirectory.</span></span> <span data-ttu-id="a3c93-209">プロキシ アセンブリへの参照を設定する代わりに、Visual Studio のソリューションに 1 つまたは複数のソース ファイルを追加できます。</span><span class="sxs-lookup"><span data-stu-id="a3c93-209">Instead of setting a reference to the proxy assembly, you can add one or more of the source files to a Visual Studio solution.</span></span> <span data-ttu-id="a3c93-210">たとえば、GenASMXProxyAssembly.cmd スクリプトを実行すると、wsdl を追加します。ソリューションのファイルを Project.cs。</span><span class="sxs-lookup"><span data-stu-id="a3c93-210">For example, after running the GenASMXProxyAssembly.cmd script, add the wsdl.Project.cs file to the solution.</span></span> <span data-ttu-id="a3c93-211">スクリプトを実行するには、代わりに、たとえば、単一のソース ファイルを生成する次のコマンドを実行できます。</span><span class="sxs-lookup"><span data-stu-id="a3c93-211">Instead of running the script, you can run the following commands to generate a single source file, for example:</span></span> 
  
```MS-DOS
set VDIR=http://ServerName/ProjectServerName/_vti_bin/psi
set WSDL="C:\Program Files (x86)\Microsoft SDKs\Windows\v7.0A\Bin\x64\wsdl.exe"
%WSDL% /nologo /l:cs /namespace:SvcProject /out:wsdl.Project.cs %VDIR%/Project.asmx?wsdl
```

<span data-ttu-id="a3c93-212">クラス変数名の**プロジェクト**として、**プロジェクト**のオブジェクトを定義するには、次のコードを使用します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-212">To define a **Project** object as a class variable named **project**, use the following code.</span></span> <span data-ttu-id="a3c93-213">**AddContextInfo**メソッドでは、Windows 認証とフォーム ベース認証の**プロジェクト**のオブジェクトにコンテキスト情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-213">The **AddContextInfo** method adds the context information to the **project** object for Windows authentication and Forms-based authentication.</span></span> 
  
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
> <span data-ttu-id="a3c93-214">PSI プロキシ アセンブリを使用した場合、または**SvcProject**という名前のプロジェクトの [サービス参照のプロキシ ファイルを追加するかどうかは、**プロジェクト**のオブジェクトを作成するのには同じコードを使用します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-214">Whether you use a PSI proxy assembly or add a proxy file for a Project service reference named **SvcProject**, you would use the same code to create a **project** object.</span></span> 
  
### <a name="adding-a-web-service-reference"></a><span data-ttu-id="a3c93-215">Web サービス参照を追加する</span><span class="sxs-lookup"><span data-stu-id="a3c93-215">Adding a web service reference</span></span>
<span data-ttu-id="a3c93-216"><a name="pj15_PrerequisitesASMX_AddingServiceReference"> </a></span><span class="sxs-lookup"><span data-stu-id="a3c93-216"></span></span>

<span data-ttu-id="a3c93-217">ASMX ベースのプロキシ アセンブリを使用したり、WSDL 出力ファイルを追加しない、する場合は、1 つまたは複数の個別の web 参照を設定できます。</span><span class="sxs-lookup"><span data-stu-id="a3c93-217">If you do not use the ASMX-based proxy assembly or add a WSDL output file, you can set one or more individual web references.</span></span> <span data-ttu-id="a3c93-218">次の手順では、Visual Studio 2012 を使用して web 参照を設定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-218">The following steps show how to set a web reference by using Visual Studio 2012.</span></span>
  
1. <span data-ttu-id="a3c93-219">**ソリューション エクスプ ローラー**で、[**参照**] フォルダーを右クリックし、し、[**サービス参照の追加**」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-219">In **Solution Explorer**, right-click the **References** folder, and then choose **Add Service Reference**.</span></span> 
    
2. <span data-ttu-id="a3c93-220">**サービス参照の追加**] ダイアログ ボックスで、[**詳細設定**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-220">In the **Add Service Reference** dialog box, choose **Advanced**.</span></span>
    
3. <span data-ttu-id="a3c93-221">**[サービス参照設定**] ダイアログ ボックスで、[ **Web 参照の追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-221">In the **Service Reference Settings** dialog box, choose **Add Web Reference**.</span></span>
    
4. <span data-ttu-id="a3c93-222">[ **URL** ] テキスト ボックスに入力`http:// _ServerName_/ _ProjectServerName_/_vti_bin/psi/ _ServiceName_.asmx?wsdl`、および**Enter**キーを押してまたは、[**移動**] アイコンを選択します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-222">In the **URL** text box, type `http:// _ServerName_/ _ProjectServerName_/_vti_bin/psi/ _ServiceName_.asmx?wsdl`, and then press **Enter** or choose the **Go** icon.</span></span> <span data-ttu-id="a3c93-223">Secure Sockets Layer (SSL) がインストールされている場合は、HTTP プロトコルではなく HTTPS プロトコルを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a3c93-223">If you have Secure Sockets Layer (SSL) installed, you should use the HTTPS protocol instead of the HTTP protocol.</span></span> 

   <span data-ttu-id="a3c93-224">たとえば、プロジェクト サービスの次の URL を使用して、上の`http://MyServer/pwa`の Project Web App サイト。`http://MyServer/pwa/_vti_bin/psi/project.asmx?wsdl`</span><span class="sxs-lookup"><span data-stu-id="a3c93-224">For example, use the following URL for the Project service on the  `http://MyServer/pwa` site for Project Web App: `http://MyServer/pwa/_vti_bin/psi/project.asmx?wsdl`</span></span>
    
   <span data-ttu-id="a3c93-225">Web ブラウザーを開き、またはに移動`http://ServerName/ProjectServerName/_vti_bin/psi/ServiceName.asmx?wsdl`。</span><span class="sxs-lookup"><span data-stu-id="a3c93-225">Or, open your web browser, and navigate to `http://ServerName/ProjectServerName/_vti_bin/psi/ServiceName.asmx?wsdl`.</span></span> <span data-ttu-id="a3c93-226">ファイルをローカル ディレクトリでは、次のように`C:\Project\WebServices\ServiceName.wsdl`。</span><span class="sxs-lookup"><span data-stu-id="a3c93-226">Save the file to a local directory, such as `C:\Project\WebServices\ServiceName.wsdl`.</span></span> <span data-ttu-id="a3c93-227">**Web 参照の追加**] ダイアログ ボックスで、 **URL**のファイルのプロトコルとファイルへのパスを入力します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-227">In the **Add Web Reference** dialog box, for **URL**, type the file protocol and the path to the file.</span></span> <span data-ttu-id="a3c93-228">たとえば、 `file://C:\Project\WebServices\Project.wsdl`。</span><span class="sxs-lookup"><span data-stu-id="a3c93-228">For example, type `file://C:\Project\WebServices\Project.wsdl`.</span></span> 
    
5. <span data-ttu-id="a3c93-229">参照が解決した後は、 **Web 参照名**] テキスト ボックスに参照名を入力します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-229">After the reference resolves, type the reference name in the **Web reference name** text box.</span></span> <span data-ttu-id="a3c93-230">Project 2013 開発者向けドキュメントのコード例では、 **Svc _ServiceName_** の任意の標準的な参照名を使用します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-230">Code examples in the Project 2013 developer documentation use the arbitrary standard reference name **Svc _ServiceName_**.</span></span> <span data-ttu-id="a3c93-231">**SvcProject**の名前は、プロジェクトの web サービス (図 3 を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="a3c93-231">For example, the Project web service is named **SvcProject** (see Figure 3).</span></span> 
    
   <span data-ttu-id="a3c93-232">**図 3 です。ASMX web サービスの参照を追加します。**</span><span class="sxs-lookup"><span data-stu-id="a3c93-232">**Figure 3. Adding an ASMX web service reference**</span></span>

   <span data-ttu-id="a3c93-233">![ASMX web サービスの参照を追加します。](media/pj15_PrerequisitesASMX_AddWebSvcReference.gif "ASMX web サービスの参照を追加します。")</span><span class="sxs-lookup"><span data-stu-id="a3c93-233">![Adding an ASMX web service reference](media/pj15_PrerequisitesASMX_AddWebSvcReference.gif "Adding an ASMX web service reference")</span></span>
  
<span data-ttu-id="a3c93-234">Project Server コンピューター上で実行する必要があります、偽装を使用して、またはあるアプリケーション コンポーネントの管理者特権のアクセス許可は、ASMX web 参照の代わりに WCF サービス参照を使用します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-234">For application components that must run on the Project Server computer, use impersonation, or have elevated permissions, use a WCF service reference instead of an ASMX web reference.</span></span> <span data-ttu-id="a3c93-235">詳細については、[プロジェクト内の WCF ベースのコード サンプルの前提条件](prerequisites-for-wcf-based-code-samples-in-project.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a3c93-235">For more information, see [Prerequisites for WCF-based code samples in Project](prerequisites-for-wcf-based-code-samples-in-project.md).</span></span>
  
## <a name="setting-other-references"></a><span data-ttu-id="a3c93-236">その他の参照を設定する</span><span class="sxs-lookup"><span data-stu-id="a3c93-236">Setting other references</span></span>
<span data-ttu-id="a3c93-237"><a name="pj15_PrerequisitesASMX_OtherReferences"> </a></span><span class="sxs-lookup"><span data-stu-id="a3c93-237"></span></span>

<span data-ttu-id="a3c93-238">プロジェクトのサーバー アプリケーションは、多くの場合、SharePoint Server 2013 web サービスなどのサービスを使用します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-238">Project Server applications often use other services, such as SharePoint Server 2013 web services.</span></span> <span data-ttu-id="a3c93-239">その他のサービスが必要な場合は、例に記載されています。</span><span class="sxs-lookup"><span data-stu-id="a3c93-239">If other services are required, they are noted in the example.</span></span>
  
<span data-ttu-id="a3c93-240">コード サンプルのローカル参照は、サンプルの上部にある**using**ステートメントのとおりです。</span><span class="sxs-lookup"><span data-stu-id="a3c93-240">Local references for the code sample are listed in **using** statements at the top of the sample:</span></span> 
  
1. <span data-ttu-id="a3c93-241">**ソリューション エクスプ ローラー**で、[**参照**] フォルダーを右クリックし、**参照の追加**を選択し、</span><span class="sxs-lookup"><span data-stu-id="a3c93-241">In **Solution Explorer**, right-click the **References** folder, and then choose **Add Reference**.</span></span>
    
2. <span data-ttu-id="a3c93-242">**[参照**] を選択し、以前にコピーしたプロジェクトのサーバー Dll を格納する場所を参照します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-242">Choose **Browse**, and then browse to the location where you stored the Project Server DLLs that you copied previously.</span></span> <span data-ttu-id="a3c93-243">Dll する必要がある、し、[ **ok]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-243">Choose the DLLs you need, and then choose **OK**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="a3c93-244">開発用コンピューター上のアセンブリのバージョンがターゲット Project Server コンピューターのものと厳密に一致していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-244">Ensure that the assembly versions on your development computer exactly match those on the target Project Server computer.</span></span> 
  
## <a name="using-multiple-authentication"></a><span data-ttu-id="a3c93-245">複数の認証を使用する</span><span class="sxs-lookup"><span data-stu-id="a3c93-245">Using multiple authentication</span></span>
<span data-ttu-id="a3c93-246"><a name="pj15_PrerequisitesASMX_ClaimsMultiAuth"> </a></span><span class="sxs-lookup"><span data-stu-id="a3c93-246"></span></span>

<span data-ttu-id="a3c93-247">Windows 認証またはフォーム認証では、オンプレミスの Project Server のユーザーの認証はクレーム処理では、SharePoint Server 2013 によって行われます。</span><span class="sxs-lookup"><span data-stu-id="a3c93-247">Authentication of on-premises Project Server users, whether by Windows authentication or Forms authentication, is done through claims processing in SharePoint Server 2013.</span></span> <span data-ttu-id="a3c93-248">複数の認証では、Project Web App が提供されている web アプリケーションが Windows 認証とフォーム ベース認証の両方をサポートしていることを意味します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-248">Multiple authentication means that the web application on which Project Web App is provisioned supports both Windows authentication and Forms-based authentication.</span></span> <span data-ttu-id="a3c93-249">場合は、請求処理は、ユーザーの認証の種類を判断できないために次のエラーでは、Windows 認証を使用する ASMX web サービスへの呼び出しが失敗します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-249">If that is the case, a call to an ASMX web service that uses Windows authentication will fail with the following error, because the claims process cannot determine which type of user to authenticate:</span></span>
  
`The server was unable to process the request due to an internal error. . . .`

<span data-ttu-id="a3c93-250">ASMX の問題が解決するのには、各 PSI web サービスに対して定義されている派生クラスに PSI メソッドへのすべての呼び出しがあります。</span><span class="sxs-lookup"><span data-stu-id="a3c93-250">To fix the problem for ASMX, all calls to PSI methods should be to a derived class that is defined for each PSI web service.</span></span> <span data-ttu-id="a3c93-251">派生クラスは、派生の PSI サービス クラスの cookie を取得するのに**SvcLoginWindows.LoginWindows**クラスを使用する必要がありますもします。</span><span class="sxs-lookup"><span data-stu-id="a3c93-251">The derived class must also use the **SvcLoginWindows.LoginWindows** class to get a cookie for the derived PSI service class.</span></span> <span data-ttu-id="a3c93-252">次の例では、 **ProjectDerived**クラスは、 **SvcProject.Project**クラスから派生します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-252">In the following example, the **ProjectDerived** class derives from the **SvcProject.Project** class.</span></span> <span data-ttu-id="a3c93-253">**プロジェクト**のクラスのメソッドを呼び出すたびに web 要求ヘッダーをオーバーライドし、派生クラスの**EnforceWindowsAuth**プロパティを追加します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-253">The derived class adds the **EnforceWindowsAuth** property and overrides the web request header for every call to a method in the **Project** class.</span></span> <span data-ttu-id="a3c93-254">**EnforceWindowsAuth**プロパティが**true**の場合は、 **GetWebRequest**メソッドは、フォーム認証を無効にするヘッダーを追加します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-254">If the **EnforceWindowsAuth** property is **true**, the **GetWebRequest** method adds a header that disables Forms authentication.</span></span> <span data-ttu-id="a3c93-255">**EnforceWindowsAuth**が**false**の場合は、フォーム認証を続行できます。</span><span class="sxs-lookup"><span data-stu-id="a3c93-255">If **EnforceWindowsAuth** is **false**, Forms authentication can proceed.</span></span>
  
<span data-ttu-id="a3c93-256">次の**ASMXLogon_MultiAuth**サンプルを使用するには、コンソール アプリケーションを作成、手順を実行は[、アプリケーションを作成し web サービス参照の追加](#pj15_PrerequisitesASMX_Configure)、および wsdl を追加し。LoginWindows.cs プロキシ ファイルと wsdl です。プロキシ ファイルを Project.cs。</span><span class="sxs-lookup"><span data-stu-id="a3c93-256">To use the following **ASMXLogon_MultiAuth** sample, create a console application, follow the steps in [Creating the application and adding a web service reference](#pj15_PrerequisitesASMX_Configure), and then add the wsdl.LoginWindows.cs proxy file and the wsdl.Project.cs proxy file.</span></span> <span data-ttu-id="a3c93-257">**Main**メソッドでは、 **ProjectDerived**クラスの**プロジェクト**のインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-257">The **Main** method creates the **project** instance of the **ProjectDerived** class.</span></span> <span data-ttu-id="a3c93-258">サンプルでは、**プロジェクトの**CookieContainer**オブジェクトを取得するのに**LoginWindowsDerived**クラスを派生を使用する必要があります。CookieContainer**プロパティで、Windows 認証とフォーム認証を区別します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-258">The sample must use the derived **LoginWindowsDerived** class to get a **CookieContainer** object for the **project.CookieContainer** property, which distinguishes Forms authentication from Windows authentication.</span></span> <span data-ttu-id="a3c93-259">**プロジェクト**のオブジェクトは、 **SvcProject.Project**クラスの任意のメソッドへの呼び出しに使用できます。</span><span class="sxs-lookup"><span data-stu-id="a3c93-259">The **project** object can then be used to make calls to any method in the **SvcProject.Project** class.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a3c93-260">**LoginWindows**サービスは、複数認証環境でのアプリケーションの asmx サービスに対してのみ必要です。</span><span class="sxs-lookup"><span data-stu-id="a3c93-260">The **LoginWindows** service is required only for ASMX applications in a multiple authentication environment.</span></span> <span data-ttu-id="a3c93-261">サンプルでは、 **ASMXLogon_MultiAuth** 、 **GetLogonCookie**メソッドは、 **loginWindows**オブジェクトの cookie を取得します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-261">In the **ASMXLogon_MultiAuth** sample, the **GetLogonCookie** method gets a cookie for the **loginWindows** object.</span></span> <span data-ttu-id="a3c93-262">**プロジェクトです。CookieContainer** **loginWindows.CookieContainer**の値にプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-262">The **project.CookieContainer** property is set to the **loginWindows.CookieContainer** value.</span></span> 
  
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

<span data-ttu-id="a3c93-263">派生**LoginWindows**クラスを使用して、フォーム認証を無効にする web 要求ヘッダーの PSI 呼び出しを行うには、複数認証環境で実行されるアプリケーションに必要です。</span><span class="sxs-lookup"><span data-stu-id="a3c93-263">Using the derived **LoginWindows** class, and making PSI calls with a web request header that disables Forms authentication, is required for applications that run in a multiple authentication environment.</span></span> <span data-ttu-id="a3c93-264">Project Server では、クレーム認証のみを使用する場合は、web 要求のヘッダーを追加するクラスを派生させる必要はありません。</span><span class="sxs-lookup"><span data-stu-id="a3c93-264">If Project Server uses only claims authentication, it is not necessary to derive a class that adds a web request header.</span></span> <span data-ttu-id="a3c93-265">前の例は、両方の環境で実行されます。</span><span class="sxs-lookup"><span data-stu-id="a3c93-265">The previous example runs in both environments.</span></span> 
  
<span data-ttu-id="a3c93-266">WCF ベースのアプリケーション用の修正プログラムは、異なります。</span><span class="sxs-lookup"><span data-stu-id="a3c93-266">The fix for a WCF-based application is different.</span></span> <span data-ttu-id="a3c93-267">詳細については、[プロジェクト内の WCF ベースのコード サンプルの前提条件](prerequisites-for-wcf-based-code-samples-in-project.md)で*複数の認証を使用して*セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a3c93-267">For more information, see the  *Using multiple authentication*  section in [Prerequisites for WCF-based code samples in Project](prerequisites-for-wcf-based-code-samples-in-project.md).</span></span>
  
## <a name="changing-the-values-of-generic-constants"></a><span data-ttu-id="a3c93-268">一般的な定数の値を変更する</span><span class="sxs-lookup"><span data-stu-id="a3c93-268">Changing the values of generic constants</span></span>
<span data-ttu-id="a3c93-269"><a name="pj15_PrerequisitesASMX_ChangeValues"> </a></span><span class="sxs-lookup"><span data-stu-id="a3c93-269"></span></span>

<span data-ttu-id="a3c93-270">ほとんどのサンプルでは、更新する必要が、サンプルを動作させるため正しく、環境内の 1 つまたは複数の変数があります。</span><span class="sxs-lookup"><span data-stu-id="a3c93-270">Most samples have one or more variables that you must update for the sample to work properly in your environment.</span></span> <span data-ttu-id="a3c93-271">次の例では、SSL がインストールされている場合は HTTP プロトコルではなく HTTPS プロトコルを使用します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-271">In the following example, if you have SSL installed, use the HTTPS protocol instead of the HTTP protocol.</span></span> <span data-ttu-id="a3c93-272">_サーバー名_を使用しているサーバーの名前に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="a3c93-272">Replace  _ServerName_ with the name of the server that you are using.</span></span> <span data-ttu-id="a3c93-273">_ProjectServerName_を PWA など、Project Server サイトの仮想ディレクトリ名に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="a3c93-273">Replace  _ProjectServerName_ with the virtual directory name of your Project Server site, such as PWA.</span></span> 
  
```cs
const string PROJECT_SERVER_URI = "http://ServerName/ProjectServerName/";
```

<span data-ttu-id="a3c93-274">変更する必要があるその他の変数または必要条件は、コード サンプルの上部に記載されています。</span><span class="sxs-lookup"><span data-stu-id="a3c93-274">Any other variables that you must change or other prerequisites are noted at the top of the code example.</span></span>
  
## <a name="verifying-the-results"></a><span data-ttu-id="a3c93-275">結果を確認する</span><span class="sxs-lookup"><span data-stu-id="a3c93-275">Verifying the results</span></span>
<span data-ttu-id="a3c93-276"><a name="pj15_PrerequisitesASMX_Verify"> </a></span><span class="sxs-lookup"><span data-stu-id="a3c93-276"></span></span>

<span data-ttu-id="a3c93-277">取得し、コード サンプルの結果を解釈する常に簡単ではありません。</span><span class="sxs-lookup"><span data-stu-id="a3c93-277">Getting and interpreting results from a code sample is not always straightforward.</span></span> <span data-ttu-id="a3c93-278">たとえば、プロジェクトを作成する場合は、Project Web App の [プロジェクト センター] ページに表示するプロジェクトを発行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a3c93-278">For example, if you create a project, you must publish the project before it can appear on the Project Center page in Project Web App.</span></span>
  
<span data-ttu-id="a3c93-279">コード サンプルの結果は、いくつかの方法で確認できます。たとえば、次のような方法があります。</span><span class="sxs-lookup"><span data-stu-id="a3c93-279">You can verify code sample results in several ways, for example:</span></span>
  
- <span data-ttu-id="a3c93-280">プロジェクト評価のためのクライアントを使用して、Project Server コンピューターからプロジェクトを開くし、目的のアイテムを表示します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-280">Use the Project Professional 2013 client to open the project from the Project Server computer, and view the items that you want.</span></span>
    
- <span data-ttu-id="a3c93-281">Project Web App の [プロジェクト センター] ページで発行されたプロジェクトを表示する ( `http://ServerName/ProjectServerName/projects.aspx`)。</span><span class="sxs-lookup"><span data-stu-id="a3c93-281">View published projects on the Project Center page of Project Web App ( `http://ServerName/ProjectServerName/projects.aspx`).</span></span>
    
- <span data-ttu-id="a3c93-282">Project Web App では、キューのログを表示します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-282">View the Queue log in Project Web App.</span></span> <span data-ttu-id="a3c93-283">サーバー設定] ページを開く (右上隅で、[**設定**] アイコンを選択します)、**個人用の設定**] セクションで [**自分のキュー ジョブ**を選択し、( `http://ServerName/ProjectServerName/MyJobs.aspx`)。</span><span class="sxs-lookup"><span data-stu-id="a3c93-283">Open the Server Settings page (choose the **Settings** icon in the top-right corner), and then choose **My Queued Jobs** under the **Personal Settings** section (  `http://ServerName/ProjectServerName/MyJobs.aspx`).</span></span> <span data-ttu-id="a3c93-284">**ビュー** 」ドロップ ダウン リストで、ジョブの状態で並べ替えることができます。</span><span class="sxs-lookup"><span data-stu-id="a3c93-284">In the **View** drop-down list, you can sort by the job status.</span></span> <span data-ttu-id="a3c93-285">既定の状態が**進行中で過去 1 週間のジョブの失敗です**。</span><span class="sxs-lookup"><span data-stu-id="a3c93-285">The default status is **In Progress and Failed Jobs in the Past Week**.</span></span> 
    
- <span data-ttu-id="a3c93-286">Project Web App の [サーバー設定] ページを使用して ( `http://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`) とすべてのキュー ジョブの管理、削除、またはチェックインのエンタープライズ オブジェクトを強制的にします。</span><span class="sxs-lookup"><span data-stu-id="a3c93-286">Use the Server Settings page in Project Web App ( `http://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`) to manage all queue jobs and delete or force check-in enterprise objects.</span></span> <span data-ttu-id="a3c93-287">[サーバーの設定] ページで、これらのリンクにアクセスする管理者の権限がある必要があります。</span><span class="sxs-lookup"><span data-stu-id="a3c93-287">You must have administrative permissions to access those links on the Server Settings page.</span></span>
    
- <span data-ttu-id="a3c93-288">**Microsoft SQL Server Management Studio の**を使用して、プロジェクト データベース内のテーブルに対してクエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-288">Use **Microsoft SQL Server Management Studio** to run a query on a table in the Project database.</span></span> <span data-ttu-id="a3c93-289">たとえば、pub の上位 200 行を選択するのには次のクエリを使用します。ワークフロー ステージの詳細ページ (Pdp) のプロジェクトに関する情報を表示するのには MSP_WORKFLOW_STAGE_PDPS テーブルです。</span><span class="sxs-lookup"><span data-stu-id="a3c93-289">For example, use the following query to select the top 200 rows of the pub.MSP_WORKFLOW_STAGE_PDPS table to show information about the project detail pages (PDPs) in workflow stages.</span></span> 
    
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

## <a name="cleaning-up"></a><span data-ttu-id="a3c93-290">クリーンアップする</span><span class="sxs-lookup"><span data-stu-id="a3c93-290">Cleaning up</span></span>
<span data-ttu-id="a3c93-291"><a name="pj15_PrerequisitesASMX_Cleanup"> </a></span><span class="sxs-lookup"><span data-stu-id="a3c93-291"></span></span>

<span data-ttu-id="a3c93-292">一部のコード サンプルをテストした後、エンタープライズ オブジェクトと設定を削除またはリセットする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a3c93-292">After you test some code samples, there are enterprise objects and settings that should be deleted or reset.</span></span> <span data-ttu-id="a3c93-293">Project Web App の [サーバー設定] ページを使用するにはエンタープライズ ・ データを管理する ( `http://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`)。</span><span class="sxs-lookup"><span data-stu-id="a3c93-293">You can use the Server Settings page in Project Web App to manage enterprise data ( `http://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`).</span></span> <span data-ttu-id="a3c93-294">[サーバー設定] ページのリンクを使用すると、古いアイテムを削除する、強制的にチェックインのプロジェクト、すべてのユーザーのジョブ キューの管理、その他の管理タスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="a3c93-294">Links on the Server Settings page enable you to delete old items, force check-in projects, manage the job queue for all users, and perform other administrative tasks.</span></span>
  
<span data-ttu-id="a3c93-295">[サーバー設定] ページに表示されるリンクの一部を以下に示します。これらは、コード サンプルを実行した後に一般的なクリーンアップの操作を行うために使用できます。</span><span class="sxs-lookup"><span data-stu-id="a3c93-295">Following are some of the links on the Server Settings page that you can use for typical cleanup activities after running code samples:</span></span>
  
- <span data-ttu-id="a3c93-296">**エンタープライズ ユーザー設定フィールドと参照テーブル**</span><span class="sxs-lookup"><span data-stu-id="a3c93-296">**Enterprise Custom Fields and Lookup Tables**</span></span>
    
- <span data-ttu-id="a3c93-297">**キュー ジョブを管理します。**</span><span class="sxs-lookup"><span data-stu-id="a3c93-297">**Manage Queue Jobs**</span></span>
    
- <span data-ttu-id="a3c93-298">**エンタープライズ オブジェクトを削除します。**</span><span class="sxs-lookup"><span data-stu-id="a3c93-298">**Delete Enterprise Objects**</span></span>
    
- <span data-ttu-id="a3c93-299">**チェックインのエンタープライズ オブジェクトを強制的に**</span><span class="sxs-lookup"><span data-stu-id="a3c93-299">**Force Check-in Enterprise Objects**</span></span>
    
- <span data-ttu-id="a3c93-300">**エンタープライズ プロジェクトの種類**</span><span class="sxs-lookup"><span data-stu-id="a3c93-300">**Enterprise Project Types**</span></span>
    
- <span data-ttu-id="a3c93-301">**ワークフロー フェーズ**</span><span class="sxs-lookup"><span data-stu-id="a3c93-301">**Workflow Phases**</span></span>
    
- <span data-ttu-id="a3c93-302">**ワークフロー ステージ**</span><span class="sxs-lookup"><span data-stu-id="a3c93-302">**Workflow Stages**</span></span>
    
- <span data-ttu-id="a3c93-303">**プロジェクト詳細ページ**</span><span class="sxs-lookup"><span data-stu-id="a3c93-303">**Project Detail Pages**</span></span>
    
- <span data-ttu-id="a3c93-304">**タイムシート期間**</span><span class="sxs-lookup"><span data-stu-id="a3c93-304">**Time Reporting Periods**</span></span>
    
- <span data-ttu-id="a3c93-305">**タイムシートの設定と既定の設定**</span><span class="sxs-lookup"><span data-stu-id="a3c93-305">**Timesheet Settings and Defaults**</span></span>
    
- <span data-ttu-id="a3c93-306">**行の分類**</span><span class="sxs-lookup"><span data-stu-id="a3c93-306">**Line Classifications**</span></span>
    
<span data-ttu-id="a3c93-307">特定の Project Web App サーバーの設定ページではなく、Project Web App インスタンスごとに、SharePoint Server 2013 では、追加の設定が管理されます。</span><span class="sxs-lookup"><span data-stu-id="a3c93-307">Additional settings are managed by SharePoint Server 2013 for each Project Web App instance, rather than by a specific Project Web App Server Settings page.</span></span> <span data-ttu-id="a3c93-308">SharePoint サーバーの全体管理アプリケーションで、**アプリケーションの全般的な設定**を選択し、**プロジェクトのサーバーの設定**、[**管理**] を選択を [サーバーの設定] ページで、ドロップダウン ボックスの一覧で、Project Web App インスタンスを選択.</span><span class="sxs-lookup"><span data-stu-id="a3c93-308">In the SharePoint Central Administration application, choose **General Application Settings**, choose **Manage** under **Project Server Settings**, and then choose the Project Web App instance in the drop-down list on the Server Settings page.</span></span> <span data-ttu-id="a3c93-309">たとえば、選択した Project Web App インスタンスのイベント ハンドラーを追加、削除する**サーバー側のイベント ハンドラー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-309">For example, choose **Server Side Event Handlers** to add or delete event handlers for the selected Project Web App instance.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a3c93-310">関連項目</span><span class="sxs-lookup"><span data-stu-id="a3c93-310">See also</span></span>
<span data-ttu-id="a3c93-311"><a name="pj15_PrerequisitesASMX_AR"> </a></span><span class="sxs-lookup"><span data-stu-id="a3c93-311"></span></span>

- [<span data-ttu-id="a3c93-312">プロジェクト内の WCF ベースのコード サンプルの前提条件</span><span class="sxs-lookup"><span data-stu-id="a3c93-312">Prerequisites for WCF-based code samples in Project</span></span>](prerequisites-for-wcf-based-code-samples-in-project.md)
- [<span data-ttu-id="a3c93-313">WCF で偽装を使用します。</span><span class="sxs-lookup"><span data-stu-id="a3c93-313">Use Impersonation with WCF</span></span>](http://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)
- [<span data-ttu-id="a3c93-314">プロジェクト PSI リファレンスの概要</span><span class="sxs-lookup"><span data-stu-id="a3c93-314">Project PSI reference overview</span></span>](project-psi-reference-overview.md)
- [<span data-ttu-id="a3c93-315">SharePoint デベロッパー センター</span><span class="sxs-lookup"><span data-stu-id="a3c93-315">SharePoint Developer Center</span></span>](http://msdn.microsoft.com/ja-jp/sharepoint/default.aspx)
    

