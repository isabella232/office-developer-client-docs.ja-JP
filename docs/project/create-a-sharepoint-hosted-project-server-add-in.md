---
title: SharePoint をホストとする Project Server アドインを作成する
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: bb9c3c00-7121-41e1-9db3-75550d040ba8
description: Project Online (自動ホスト型、プロバイダーホスト型、および SharePoint ホスト型) 用に作成できる3種類のアプリの中から、SharePoint でホストされるアプリを作成して展開するのが最も簡単です。
ms.openlocfilehash: 0af2ab51266a01f682cd16382f2cd0fdfde3a416
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540841"
---
# <a name="create-a-sharepoint-hosted-project-server-add-in"></a><span data-ttu-id="b3112-103">SharePoint をホストとする Project Server アドインを作成する</span><span class="sxs-lookup"><span data-stu-id="b3112-103">Create a SharePoint-hosted Project Server add-in</span></span>

<span data-ttu-id="b3112-104">Project Online (自動ホスト型、プロバイダーホスト型、および SharePoint ホスト型) 用に作成できる3種類のアプリの中から、SharePoint でホストされるアプリを作成して展開するのが最も簡単です。</span><span class="sxs-lookup"><span data-stu-id="b3112-104">Of the three types of apps that you can create for Project Online (autohosted, provider-hosted, and SharePoint-hosted), the SharePoint-hosted app is the simplest to create and deploy.</span></span> <span data-ttu-id="b3112-105">SharePoint ホスト型アプリは、OAuth 認証を必要とせず、プロバイダーでホストされているリソースのために、Azure を使用したり、ローカルサイトのメンテナンスを必要としたりしません。</span><span class="sxs-lookup"><span data-stu-id="b3112-105">A SharePoint-hosted app does not require OAuth authentication, and does not use Azure or require maintenance of a local site for the provider-hosted resources.</span></span> <span data-ttu-id="b3112-106">Visual Studio の [2013 sharepoint 用アプリ] テンプレートは、Office ストアで発行および販売できるアプリを開発したり、sharepoint のプライベートアプリカタログに展開したりするための便利なフレームワークです。</span><span class="sxs-lookup"><span data-stu-id="b3112-106">The **App for SharePoint 2013** template in Visual Studio is a convenient framework for developing apps that can be published and sold in the Office Store or deployed to a private app catalog on SharePoint.</span></span> 
  
<span data-ttu-id="b3112-107">Project では、statusing は、チームメンバーが Project Web App の [タスク] ページを使用して、割り当てられたタスクの状態 (タスクの作業に費やした1週間の毎日の勤務時間数など) を送信するプロセスです。</span><span class="sxs-lookup"><span data-stu-id="b3112-107">In Project, statusing is a process where a team member can use the Tasks page in Project Web App to submit the status of an assigned task, such as the number of hours worked each day of a week spent working on the task.</span></span> <span data-ttu-id="b3112-108">割り当て所有者 (通常はプロジェクトマネージャー) は、状態を承認または拒否することができます。</span><span class="sxs-lookup"><span data-stu-id="b3112-108">The assignment owner (usually the project manager) can approve or reject the status.</span></span> <span data-ttu-id="b3112-109">ステータスが [承認済み] の場合、Project はスケジュールを再計算します。</span><span class="sxs-lookup"><span data-stu-id="b3112-109">When the status is approved, Project recalculates the schedule.</span></span> <span data-ttu-id="b3112-110">**Quickstatus**アプリには、割り当てられたタスクが表示され、ユーザーは、完了率をすばやく更新し、選択された割り当ての進捗状況を提出して承認を求めることができます。</span><span class="sxs-lookup"><span data-stu-id="b3112-110">The **QuickStatus** app displays assigned tasks, where the user can quickly update percent complete and submit status of the selected assignments for approval.</span></span> <span data-ttu-id="b3112-111">Project Web App の [タスク] ページには多くの機能がありますが、 **Quickstatus** App は簡単なインターフェイスを提供する例です。</span><span class="sxs-lookup"><span data-stu-id="b3112-111">Although the Tasks page in Project Web App has much more functionality, the **QuickStatus** app is an example that provides a simplified interface.</span></span> 
  
<span data-ttu-id="b3112-112">**Quickstatus**アプリは開発者のためのサンプルです。これは、運用環境での使用を目的としたものではありません。</span><span class="sxs-lookup"><span data-stu-id="b3112-112">The **QuickStatus** app is a sample for developers; it is not intended for use in a production environment.</span></span> <span data-ttu-id="b3112-113">主な目的は、完全に機能する statusing アプリを作成することではなく、Project Online のアプリ開発の例を示すことです。</span><span class="sxs-lookup"><span data-stu-id="b3112-113">The primary purpose is to show an example of app development for Project Online, not to create a fully functional statusing app.</span></span> <span data-ttu-id="b3112-114">Statusing のより良いアプローチについては、[次の手順](#pj15_StatusingApp_NextSteps)の推奨事項を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b3112-114">For a better approach to statusing, see the recommendation in [Next steps](#pj15_StatusingApp_NextSteps).</span></span>
  
<span data-ttu-id="b3112-115">Statusing の一般的な情報については、「[タスクの進行状況](https://support.office.com/article/Find-information-about-Project-Server-2013-8b08a414-15a7-4076-b2db-c90d0214ea7f?ui=en-US&rs=en-US&ad=US#BKMK_TaskProgress)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b3112-115">For general information about statusing, see [Task progress](https://support.office.com/article/Find-information-about-Project-Server-2013-8b08a414-15a7-4076-b2db-c90d0214ea7f?ui=en-US&rs=en-US&ad=US#BKMK_TaskProgress).</span></span> <span data-ttu-id="b3112-116">SharePoint および Project Server 用のアドインの開発の詳細については、「 [Sharepoint アドイン](https://msdn.microsoft.com/library/jj163230.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b3112-116">For more information about developing add-ins for SharePoint and Project Server, see [SharePoint Add-ins](https://msdn.microsoft.com/library/jj163230.aspx).</span></span>

<span data-ttu-id="b3112-117"><a name="pj15_StatusingApp_Prerequisites"> </a></span><span class="sxs-lookup"><span data-stu-id="b3112-117"></span></span>

## <a name="prerequisites-for-creating-an-app-for-project-server-2013"></a><span data-ttu-id="b3112-118">Project Server 2013 用アプリを作成するための前提条件</span><span class="sxs-lookup"><span data-stu-id="b3112-118">Prerequisites for creating an app for Project Server 2013</span></span>

<span data-ttu-id="b3112-119">Project Online またはオンプレミスの Project Server 2013 に展開できる比較的簡単なアプリを開発する場合は、オンライン開発環境を提供する Napa を使用できます。</span><span class="sxs-lookup"><span data-stu-id="b3112-119">To develop relatively simple apps that can be deployed to Project Online or to an on-premises installation of Project Server 2013, you can use the Napa, which provide an online development environment.</span></span> <span data-ttu-id="b3112-120">より複雑なアプリ、Project Web App のリボンの変更、および開発時の簡単なデバッグには、Visual Studio 2012 または Visual Studio 2013 を使用できます。</span><span class="sxs-lookup"><span data-stu-id="b3112-120">For more complex apps, modifying the Project Web App ribbon, and easier debugging during development, you can use Visual Studio 2012 or Visual Studio 2013.</span></span> <span data-ttu-id="b3112-121">たとえば、オンプレミスのインストールでは、Project Server データベースの変更について下書き datatable を手動で確認できます。</span><span class="sxs-lookup"><span data-stu-id="b3112-121">For example, with an on-premises installation, you can manually check the Drafts datatables for changes in the Project Server database.</span></span> <span data-ttu-id="b3112-122">この記事では、Visual Studio でアプリを開発する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b3112-122">This article shows how to do app development with Visual Studio.</span></span>
  
<span data-ttu-id="b3112-123">Visual Studio を使用して Project Server アプリを開発するには、次のものが必要です。</span><span class="sxs-lookup"><span data-stu-id="b3112-123">Development of Project Server apps with Visual Studio requires the following:</span></span>
  
- <span data-ttu-id="b3112-p106">使用するローカルの開発用コンピューターに最新のサービス パックと Windows 更新プログラムをインストールしてあることを確認します。オペレーティング システムは、Windows 7、Windows 8、Windows Server 2008、Windows Server 2012 のいずれでもかまいません。</span><span class="sxs-lookup"><span data-stu-id="b3112-p106">Ensure that you have installed the most recent service packs and Windows updates on your local development computer. The operating system can be Windows 7, Windows 8, Windows Server 2008, or Windows Server 2012.</span></span>
    
- <span data-ttu-id="b3112-126">SharePoint Server 2013 および Project Server 2013 がインストールされているコンピューターに、アプリの分離とアプリケーションのサイドロードが構成されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3112-126">You must have a computer that has SharePoint Server 2013 and Project Server 2013 installed, where the computer is configured for app isolation and sideloading of apps.</span></span> <span data-ttu-id="b3112-127">サイドロードを使用すると、Visual Studio が一時的にアプリをデバッグ用にインストールできるようになります。</span><span class="sxs-lookup"><span data-stu-id="b3112-127">Sideloading enables Visual Studio to temporarily install the app for debugging.</span></span> <span data-ttu-id="b3112-128">SharePoint および Project Server のオンプレミスインストールを使用できます。</span><span class="sxs-lookup"><span data-stu-id="b3112-128">You can use an on-premises installation of SharePoint and Project Server.</span></span> <span data-ttu-id="b3112-129">詳細については、「 [SharePoint 用アプリのオンプレミスの開発環境をセットアップする](https://msdn.microsoft.com/library/fp179923%28Office.15%29.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b3112-129">For more information, see [Set up an on-premises development environment for apps for SharePoint](https://msdn.microsoft.com/library/fp179923%28Office.15%29.aspx).</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="b3112-130">オンプレミスのインストールの場合は、企業のアプリカタログを作成する*前に*分離アプリドメインを構成します。</span><span class="sxs-lookup"><span data-stu-id="b3112-130">For an on-premises installation, configure an isolated app domain  *before*  you create a corporate app catalog.</span></span> 
  
- <span data-ttu-id="b3112-131">開発用コンピューターは、Office Developer Tools for Visual Studio 2012 がインストールされているリモートコンピューターの場合があります。</span><span class="sxs-lookup"><span data-stu-id="b3112-131">The development computer can be a remote computer that has Office Developer Tools for Visual Studio 2012 installed.</span></span> <span data-ttu-id="b3112-132">最新のバージョンがインストールされていることを確認します。[Office 用アプリおよび SharePoint 用アプリのダウンロード](https://msdn.microsoft.com/office/apps/fp123627.aspx)の [*ツール*] セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b3112-132">Ensure that you have installed the most recent version; see the  *Tools*  section of the [Apps for Office and SharePoint downloads](https://msdn.microsoft.com/office/apps/fp123627.aspx).</span></span>
    
- <span data-ttu-id="b3112-133">開発およびテストに使用する Project Web App インスタンスがブラウザーでアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b3112-133">Verify that the Project Web App instance you will be using for development and testing is accessible in the browser.</span></span>
    
<span data-ttu-id="b3112-134">オンラインツールの使用方法については、「 [Office 365 で SharePoint 用アプリを開発するための環境を設定する](https://msdn.microsoft.com/library/fp161179.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b3112-134">For information about using the online tools, see [Set up an environment for developing apps for SharePoint on Office 365](https://msdn.microsoft.com/library/fp161179.aspx).</span></span> <span data-ttu-id="b3112-135">オンラインツールを使用する Project Server 用の単純なアプリを構築する方法のチュートリアルについては、「EPMSource ブログシリーズ」を参照して、[最初の Project server アプリを作成](https://epmsource.com/2012/11/20/building-your-first-project-server-app-part-zerothe-introduction/)してください。</span><span class="sxs-lookup"><span data-stu-id="b3112-135">For a walkthrough of building a simple app for Project Server that uses the online tools, see the EPMSource blog series, [Building your first Project Server app](https://epmsource.com/2012/11/20/building-your-first-project-server-app-part-zerothe-introduction/).</span></span>

<span data-ttu-id="b3112-136"><a name="pj15_StatusingApp_UsingVisualStudio"> </a></span><span class="sxs-lookup"><span data-stu-id="b3112-136"></span></span>

## <a name="using-visual-studio-to-create-a-project-server-app"></a><span data-ttu-id="b3112-137">Visual Studio を使用して Project Server アプリを作成する</span><span class="sxs-lookup"><span data-stu-id="b3112-137">Using Visual Studio to create a Project Server app</span></span>

<span data-ttu-id="b3112-138">Office Developer Tools for Visual Studio 2012 には、Project Server 2013 で使用できる SharePoint アプリのテンプレートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b3112-138">Office Developer Tools for Visual Studio 2012 includes a template for SharePoint apps that can be used with Project Server 2013.</span></span> <span data-ttu-id="b3112-139">アプリソリューションを作成すると、ソリューションには、カスタムコードに次のファイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b3112-139">When you create an app solution, the solution includes the following files for your custom code:</span></span>
  
- <span data-ttu-id="b3112-140">**Appmanifest.xml**には、アプリタイトル、アクセス許可要求スコープ、およびその他のプロパティの設定が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b3112-140">**AppManifest.xml** includes settings for the app title, permission request scope, and other properties.</span></span> <span data-ttu-id="b3112-141">手順1では、マニフェストデザイナーを使用してプロパティを設定する手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="b3112-141">Procedure 1 includes steps to set the properties by using the Manifest Designer.</span></span> 
    
- <span data-ttu-id="b3112-142">Pages フォルダーの**default.aspx**は、アプリのメインページです。</span><span class="sxs-lookup"><span data-stu-id="b3112-142">**Default.aspx** in the Pages folder is the main page of the app.</span></span> <span data-ttu-id="b3112-143">手順2は、 **Quickstatus**アプリに HTML5 コンテンツを追加する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="b3112-143">Procedure 2 shows how to add HTML5 content for the **QuickStatus** app.</span></span> 
    
- <span data-ttu-id="b3112-144">Scripts フォルダー内の**app.config**は、カスタム JavaScript コードのプライマリファイルです。</span><span class="sxs-lookup"><span data-stu-id="b3112-144">**App.js** in the Scripts folder is the primary file for the custom JavaScript code.</span></span> <span data-ttu-id="b3112-145">手順3では、 **Quickstatus**アプリの JavaScript コードについて説明します。</span><span class="sxs-lookup"><span data-stu-id="b3112-145">Procedure 3 explains the JavaScript code for the **QuickStatus** app.</span></span> 
    
   <span data-ttu-id="b3112-146">JQuery ベースのグリッドまたは日付選択などの市販のコントロールを追加する場合は、default.aspx ファイルに追加の JavaScript ファイルへの参照を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="b3112-146">If you add commercial controls such as a jQuery-based grid or date picker, you can add references to additional JavaScript files in the Default.aspx file.</span></span>
    
- <span data-ttu-id="b3112-147">コンテンツフォルダー内の**app.xaml**は、カスタム CSS3 スタイルのプライマリファイルです。</span><span class="sxs-lookup"><span data-stu-id="b3112-147">**App.css** in the Content folder is the primary file for custom CSS3 styles.</span></span> <span data-ttu-id="b3112-148">手順2と手順3には、 **Quickstatus**アプリのカスケードスタイルシート (CSS) のスタイルに関する情報が記載されています。</span><span class="sxs-lookup"><span data-stu-id="b3112-148">Procedure 2 and Procedure 3 include information about cascading style sheets (CSS) styles for the **QuickStatus** app.</span></span> <span data-ttu-id="b3112-149">Default.aspx ファイルには、追加の CSS ファイルへの参照を追加できます。</span><span class="sxs-lookup"><span data-stu-id="b3112-149">You can add references to additional CSS files in the Default.aspx file.</span></span> 
    
- <span data-ttu-id="b3112-150">Images フォルダーの**AppIcon**は、アプリが Office ストアまたはアプリカタログに表示する 96 x 96 アイコンです。</span><span class="sxs-lookup"><span data-stu-id="b3112-150">**AppIcon.png** in the Images folder is the 96 x 96 icon that the app displays in the Office Store or the app catalog.</span></span> 
    
<span data-ttu-id="b3112-151">Project Web App のリボンを変更するには、リボンのカスタムアクションを追加します。</span><span class="sxs-lookup"><span data-stu-id="b3112-151">To modify the Project Web App ribbon, you can add a ribbon custom action.</span></span> <span data-ttu-id="b3112-152">[QuickStatus app セクションのコード例](#pj15_StatusingApp_Example)には、変更された Default.aspx、App.config、app.xaml、および appmanifest.xml ファイルの完全なコードが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b3112-152">The [Example code for the QuickStatus app](#pj15_StatusingApp_Example) section includes the complete code for the modified Default.aspx, App.js, App.css, Elements.xml, and AppManifest.xml files.</span></span> 
  
### <a name="procedure-1-to-create-an-app-project-in-visual-studio"></a><span data-ttu-id="b3112-153">手順 1.</span><span class="sxs-lookup"><span data-stu-id="b3112-153">Procedure 1.</span></span> <span data-ttu-id="b3112-154">Visual Studio でアプリプロジェクトを作成するには</span><span class="sxs-lookup"><span data-stu-id="b3112-154">To create an app project in Visual Studio</span></span>

1. <span data-ttu-id="b3112-155">管理者として Visual Studio 2012 を実行し、スタートページで [**新しいプロジェクト**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3112-155">Run Visual Studio 2012 as an administrator, and then select **New Project** on the Start page.</span></span> 
    
2. <span data-ttu-id="b3112-156">[**新しいプロジェクト**] ダイアログボックスで、[**テンプレート**]、[ **Visual C#**]、[ **Office/SharePoint** ] ノードを展開し、[**アプリ**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3112-156">In the **New Project** dialog box, expand the **Templates**, **Visual C#**, and **Office/SharePoint** nodes, and then select **Apps**.</span></span> <span data-ttu-id="b3112-157">中央のウィンドウの上部にある [ターゲットフレームワーク] ドロップダウンリストで、既定の **.Net framework 4.5**を使用し、[ **SharePoint 用アプリ 2013** ] を選択します (図1を参照)。</span><span class="sxs-lookup"><span data-stu-id="b3112-157">Use the default **.NET Framework 4.5** in the target framework drop-down list at the top of the center pane, and then select **App for SharePoint 2013** (see Figure 1).</span></span> 
    
3. <span data-ttu-id="b3112-158">[**名前**] フィールドに「quickstatus」と入力し、アプリを保存する場所を参照して、[ **OK]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3112-158">In the **Name** field, type QuickStatus, browse to the location where you want to save the app, and then choose **OK**.</span></span>
    
   <span data-ttu-id="b3112-159">**図1。Visual Studio で Project Server アプリを作成する**</span><span class="sxs-lookup"><span data-stu-id="b3112-159">**Figure 1. Creating a Project Server app in Visual Studio**</span></span>

   <span data-ttu-id="b3112-160">![Visual Studio で Project Server アプリを作成]する(media/pj15_CreateStatusingApp_NewProject.gif "Visual Studio で Project Server アプリを作成")する</span><span class="sxs-lookup"><span data-stu-id="b3112-160">![Creating a Project Server app in Visual Studio](media/pj15_CreateStatusingApp_NewProject.gif "Creating a Project Server app in Visual Studio")</span></span>
  
4. <span data-ttu-id="b3112-161">[**新しい SharePoint 用アプリ**] ダイアログボックスで、次の3つのフィールドに入力します。</span><span class="sxs-lookup"><span data-stu-id="b3112-161">In the **New app for SharePoint** dialog box, fill in the following three fields:</span></span> 
    
   - <span data-ttu-id="b3112-162">上部のテキストボックスに、Project Web App に表示するアプリの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="b3112-162">In the top text box, type the name that you want the app to display in Project Web App.</span></span> <span data-ttu-id="b3112-163">たとえば、「クイック状態の更新」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b3112-163">For example, type Quick Status Update.</span></span>
    
   - <span data-ttu-id="b3112-164">デバッグに使用するサイトには、Project Web App インスタンスの URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="b3112-164">For the site to use for debugging, type the URL of the Project Web App instance.</span></span> <span data-ttu-id="b3112-165">たとえば、「」 `https://ServerName/ProjectServerName`と入力して ( _Servername_と_projectservername_を独自の値に置き換え)、[**検証**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3112-165">For example, type  `https://ServerName/ProjectServerName` (replacing  _ServerName_ and  _ProjectServerName_ with your own values), and then choose **Validate**.</span></span> <span data-ttu-id="b3112-166">すべてが正常に実行されると、Visual Studio は**接続が成功**したことを示します。</span><span class="sxs-lookup"><span data-stu-id="b3112-166">If all goes well, Visual Studio shows **Connection successful**.</span></span> <span data-ttu-id="b3112-167">エラーメッセージが表示された場合は、Project Web App の URL が正しいことと、Project Server コンピュータがアプリの分離とアプリケーションのサイドロード用に構成されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="b3112-167">If you get an error message, ensure that the Project Web App URL is correct and that the Project Server computer is configured for app isolation and sideloading of apps.</span></span> <span data-ttu-id="b3112-168">詳細については、「 [Project Server 2013 用アプリを作成するための前提条件](#pj15_StatusingApp_Prerequisites)」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b3112-168">For more information, see the [Prerequisites for creating an app for Project Server 2013](#pj15_StatusingApp_Prerequisites) section.</span></span> 
    
   - <span data-ttu-id="b3112-169">[ **Sharepoint 用アプリをホストする方法**] ドロップダウンリストで、[ **sharepoint ホスト型**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3112-169">In the **How do you want to host your app for SharePoint** drop-down list, choose **SharePoint-hosted**.</span></span>
    
   > [!CAUTION]
   > <span data-ttu-id="b3112-170">**プロバイダーでホスト**される既定のプロジェクトの種類を誤って選択すると、Visual Studio によって、 **quickstatus**プロジェクトと**quickstatusweb**プロジェクトという2つのプロジェクトが作成されます。</span><span class="sxs-lookup"><span data-stu-id="b3112-170">If you choose the default **Provider-hosted** project type by mistake, Visual Studio creates two projects in the solution: a **QuickStatus** project and a **QuickStatusWeb** project.</span></span> <span data-ttu-id="b3112-171">2つのプロジェクトが表示された場合は、そのソリューションを削除し、もう一度開始します。</span><span class="sxs-lookup"><span data-stu-id="b3112-171">If you see two projects, delete that solution and start again.</span></span> 
  
5. <span data-ttu-id="b3112-172">**[OK]** を選択して、 **Quickstatus**ソリューション、 **quickstatus**プロジェクト、および既定のファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="b3112-172">Choose **OK** to create the **QuickStatus** solution, **QuickStatus** project, and default files.</span></span> 
    
6. <span data-ttu-id="b3112-173">[マニフェストデザイナー] ビューを開きます (たとえば、Appmanifest.xml ファイルをダブルクリックします)。</span><span class="sxs-lookup"><span data-stu-id="b3112-173">Open the Manifest Designer view (for example, double-click the AppManifest.xml file).</span></span> <span data-ttu-id="b3112-174">[**全般**] タブの [**タイトル**] テキストボックスに、手順4で入力したアプリ名が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b3112-174">On the **General** tab, the **Title** text box should show the app name that you typed in step 4.</span></span> <span data-ttu-id="b3112-175">[**アクセス許可**] タブを選択して、アプリに対して次のアクセス許可要求を追加します (図2を参照)。</span><span class="sxs-lookup"><span data-stu-id="b3112-175">Choose the **Permissions** tab to add the following permission requests for the app (see Figure 2):</span></span> 
    
   - <span data-ttu-id="b3112-176">[**アクセス許可要求**] リストの最初の行で、[**範囲**] 列のドロップダウンリストから [ **Statusing** ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3112-176">In the first row of the **Permission requests** list, in the **Scope** column, choose **Statusing** in the drop-down list.</span></span> <span data-ttu-id="b3112-177">[**アクセス許可**] 列で、[ **submitstatus**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3112-177">In the **Permission** column, choose **SubmitStatus**.</span></span>
    
   - <span data-ttu-id="b3112-178">**範囲**が**複数のプロジェクト**であり、**アクセス許可**が**読み取ら**れる行を追加します。</span><span class="sxs-lookup"><span data-stu-id="b3112-178">Add a row where the **Scope** is **Multiple Projects** and the **Permission** is **Read**.</span></span>
    
   <span data-ttu-id="b3112-179">**図2Statusing アプリのアクセス許可のスコープの設定**</span><span class="sxs-lookup"><span data-stu-id="b3112-179">**Figure 2. Setting the permission scope for a statusing app**</span></span>

   <span data-ttu-id="b3112-180">![Statusing アプリのアクセス許可のスコープの設定](media/pj15_CreateStatusingApp_PermissionScope.gif "Statusing アプリのアクセス許可のスコープの設定")</span><span class="sxs-lookup"><span data-stu-id="b3112-180">![Setting the permission scope for a statusing app](media/pj15_CreateStatusingApp_PermissionScope.gif "Setting the permission scope for a statusing app")</span></span>
  
<span data-ttu-id="b3112-181">**Quickstatus**アプリを使用すると、Project Web app のユーザーは、複数のプロジェクトからそのユーザーの割り当てを読み取り、割り当ての達成率を変更し、更新を送信することができます。</span><span class="sxs-lookup"><span data-stu-id="b3112-181">The **QuickStatus** app enables a Project Web App user to read assignments for that user from multiple projects, change the assignment percent complete, and submit the update.</span></span> <span data-ttu-id="b3112-182">図2のドロップダウンリストに表示されるその他のアクセス許可要求スコープは、このアプリでは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="b3112-182">The other permission request scopes shown in the drop-down list in Figure 2 are not required for this app.</span></span> <span data-ttu-id="b3112-183">アクセス許可要求スコープとは、アプリがユーザーに代わって要求するアクセス許可のことです。</span><span class="sxs-lookup"><span data-stu-id="b3112-183">The permission request scopes are the permissions that the app requests on behalf of the user.</span></span> <span data-ttu-id="b3112-184">ユーザーが Project Web App でこれらの権限を持っていない場合、アプリは実行されません。</span><span class="sxs-lookup"><span data-stu-id="b3112-184">If the user does not have those permissions in Project Web App, the app does not run.</span></span> <span data-ttu-id="b3112-185">アプリには、他の SharePoint アクセス許可の場合を含む複数のアクセス許可要求スコープを含めることができますが、アプリの機能に必要な最低限の要件のみを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3112-185">An app can have multiple permission request scopes, including those for other SharePoint permissions, but should have only the minimum necessary for the app functionality.</span></span> <span data-ttu-id="b3112-186">Project Server に関連付けられているアクセス許可要求の範囲を次に示します。</span><span class="sxs-lookup"><span data-stu-id="b3112-186">Following are the permission request scopes that are related to Project Server:</span></span> 

- <span data-ttu-id="b3112-187">**エンタープライズリソース**: 他の Project Web App ユーザーに関する情報を読み取りまたは書き込みを行うためのリソース管理者のアクセス許可。</span><span class="sxs-lookup"><span data-stu-id="b3112-187">**Enterprise Resources**: Resource manager permissions, to read or write information about other Project Web App users.</span></span>
    
- <span data-ttu-id="b3112-188">**複数のプロジェクト**: ユーザーがアクセス許可を要求した複数のプロジェクトに対して読み取りまたは書き込みを行います。</span><span class="sxs-lookup"><span data-stu-id="b3112-188">**Multiple Projects**: Read or write to more than one project, where the user has the permissions requested.</span></span>
    
- <span data-ttu-id="b3112-189">**Project Server**: アプリユーザーが Project Web app の管理者権限を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3112-189">**Project Server**: Requires the app user to have administrator permissions for Project Web App.</span></span>
    
- <span data-ttu-id="b3112-190">**レポート**: Project web App の**projectdata** OData サービスを確認します (project web app に対するログオン権限のみが必要です)。</span><span class="sxs-lookup"><span data-stu-id="b3112-190">**Reporting**: Read the **ProjectData** OData service for Project Web App (requires only log on permission for Project Web App).</span></span> 
    
- <span data-ttu-id="b3112-191">**単一プロジェクト**: ユーザーがアクセス許可を要求したプロジェクトに対して、読み取りまたは書き込みを行います。</span><span class="sxs-lookup"><span data-stu-id="b3112-191">**Single Project**: Read or write to a project where the user has the permissions requested.</span></span>
    
- <span data-ttu-id="b3112-192">**Statusing**: 作業時間、達成率、新しい割り当てなどの、割り当ての進捗状況の更新を提出します。</span><span class="sxs-lookup"><span data-stu-id="b3112-192">**Statusing**: Submit updates for status of assignments, such as times worked, percent complete, and new assignments.</span></span>
    
- <span data-ttu-id="b3112-193">**ワークフロー**: ユーザーが Project Server ワークフローを実行する権限を持っている場合、アプリはワークフローの引き上げられた権限で実行されます。</span><span class="sxs-lookup"><span data-stu-id="b3112-193">**Workflow**: If the user has permission to run Project Server workflows, the app then runs with elevated permissions for the workflow.</span></span>
    
<span data-ttu-id="b3112-194">Project Server 2013 のアクセス許可要求範囲の詳細については、「project [2013 の開発者向けの更新プログラム](updates-for-developers-in-project-2013.md)」および「 [SharePoint 2013 のアプリのアクセス許可](https://msdn.microsoft.com/library/fp142383.aspx)」の「*プロジェクトアプリ*」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b3112-194">For more information about permission request scopes for Project Server 2013, see the  *Project apps*  section in [Updates for developers in Project 2013](updates-for-developers-in-project-2013.md) and [App permissions in SharePoint 2013](https://msdn.microsoft.com/library/fp142383.aspx).</span></span>


<span data-ttu-id="b3112-195"><a name="pj15_StatusingApp_HTML"> </a></span><span class="sxs-lookup"><span data-stu-id="b3112-195"></span></span>

### <a name="creating-the-html-content-for-the-quickstatus-app"></a><span data-ttu-id="b3112-196">QuickStatus アプリの HTML コンテンツを作成する</span><span class="sxs-lookup"><span data-stu-id="b3112-196">Creating the HTML content for the QuickStatus app</span></span>

<span data-ttu-id="b3112-197">HTML コンテンツのコーディングを開始する前に、QuickStatus アプリのユーザーインターフェイスとユーザーの利便性を設計します (図3は、完成したページの例を示しています)。</span><span class="sxs-lookup"><span data-stu-id="b3112-197">Before you start coding the HTML content, design the user interface and user experience for the QuickStatus app (Figure 3 shows an example of the completed page).</span></span> <span data-ttu-id="b3112-198">デザインには、HTML コードを操作する JavaScript 関数のアウトラインを含めることもできます。</span><span class="sxs-lookup"><span data-stu-id="b3112-198">A design can also include an outline of the JavaScript functions that interact with the HTML code.</span></span> <span data-ttu-id="b3112-199">一般的な情報については、「 [SharePoint 2013 のアプリの UX 設計](https://msdn.microsoft.com/library/fp179934.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b3112-199">For general information, see [UX design for apps in SharePoint 2013](https://msdn.microsoft.com/library/fp179934.aspx).</span></span>
  
<span data-ttu-id="b3112-200">**図3QuickStatus app ページの設計**</span><span class="sxs-lookup"><span data-stu-id="b3112-200">**Figure 3. Design of the QuickStatus app page**</span></span>

<span data-ttu-id="b3112-201">![QuickStatus app ページの設計](media/pj15_CreateStatusingApp_AfterRefresh.gif "QuickStatus app ページの設計")</span><span class="sxs-lookup"><span data-stu-id="b3112-201">![Design of the QuickStatus app page](media/pj15_CreateStatusingApp_AfterRefresh.gif "Design of the QuickStatus app page")</span></span>
  
<span data-ttu-id="b3112-202">アプリでは、表示名が上部に表示されます。これは、Appmanifest.xml の**Title**要素の値です。</span><span class="sxs-lookup"><span data-stu-id="b3112-202">The app shows the display name at the top, which is the value of the **Title** element in AppManifest.xml.</span></span> 
  
<span data-ttu-id="b3112-203">既定では、ページは HTML5 を使用します。</span><span class="sxs-lookup"><span data-stu-id="b3112-203">By default, the page uses HTML5.</span></span> <span data-ttu-id="b3112-204">次に示すのは、 **Quickstatus**アプリによってページの本文に含まれるメイン UI オブジェクトの標準の HTML 要素です。</span><span class="sxs-lookup"><span data-stu-id="b3112-204">Following are the standard HTML elements for the main UI objects that the **QuickStatus** app contains in the body of the page:</span></span> 
  
- <span data-ttu-id="b3112-205">**Form**要素には、その他すべての UI 要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b3112-205">A **form** element contains all of the other UI elements.</span></span> 
    
- <span data-ttu-id="b3112-206">**Fieldset**要素は、割り当てのテーブルのコンテナーと枠線を作成します。子の**legend**要素は、コンテナーのラベルを提供します。</span><span class="sxs-lookup"><span data-stu-id="b3112-206">A **fieldset** element creates a container and border for the table of assignments; the child **legend** element provides a label for the container.</span></span> 
    
- <span data-ttu-id="b3112-207">**Table**要素には、キャプションとテーブルヘッダーのみが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b3112-207">A **table** element includes a caption and only a table header.</span></span> <span data-ttu-id="b3112-208">JavaScript 関数は、テーブルの標題を変更し、割り当ての行を追加します。</span><span class="sxs-lookup"><span data-stu-id="b3112-208">JavaScript functions change the table caption and add rows for the assignments.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="b3112-209">ページングと並べ替えを簡単に追加するために、運用アプリでは、テーブルではなく、商用の jQuery ベースのグリッドコントロールを使用する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b3112-209">To easily add paging and sorting, a production app would probably use a commercial jQuery-based grid control instead of a table.</span></span> 
  
   <span data-ttu-id="b3112-210">この表には、プロジェクト名、チェックボックスのあるタスク名、実績作業時間、達成率、残存作業時間、割り当て終了日の列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b3112-210">The table includes columns for the project name, task name with a check box, actual work, percent complete, remaining work, and the assignment finish date.</span></span> <span data-ttu-id="b3112-211">JavaScript 関数は、チェックボックスと、各タスクの達成率のテキスト入力フィールドを作成します。</span><span class="sxs-lookup"><span data-stu-id="b3112-211">JavaScript functions create the check box and the text input field for the percent complete of each task.</span></span>
    
- <span data-ttu-id="b3112-212">テキストボックスの**input**要素は、選択したすべての割り当てに対して達成率を設定します。</span><span class="sxs-lookup"><span data-stu-id="b3112-212">An **input** element for a text box sets percent complete for all selected assignments.</span></span> 
    
- <span data-ttu-id="b3112-213">**Button**要素は、状態の変更を送信します。</span><span class="sxs-lookup"><span data-stu-id="b3112-213">A **button** element submits the status changes.</span></span> 
    
- <span data-ttu-id="b3112-214">**Button**要素は、ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="b3112-214">A **button** element refreshes the page.</span></span> 
    
- <span data-ttu-id="b3112-215">**Button**要素は、アプリを終了し、Project Web app の [タスク] ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="b3112-215">A **button** element exits the app and returns to the Tasks page in Project Web App.</span></span> 
    
<span data-ttu-id="b3112-216">下部のテキストボックス要素と button 要素は**div**要素内にあるので、CSS は UI オブジェクトの位置と外観を簡単に管理できます。</span><span class="sxs-lookup"><span data-stu-id="b3112-216">The bottom text box and button elements are within **div** elements, so that CSS can easily manage the position and appearance of the UI objects.</span></span> <span data-ttu-id="b3112-217">JavaScript 関数は、ステータス更新の成功または失敗の結果が含まれるページの下部に段落を追加します。</span><span class="sxs-lookup"><span data-stu-id="b3112-217">A JavaScript function adds a paragraph at the bottom of the page that contains results for success or failure of the status update.</span></span> 
  
### <a name="procedure-2-to-create-the-html-content"></a><span data-ttu-id="b3112-218">手順 2.</span><span class="sxs-lookup"><span data-stu-id="b3112-218">Procedure 2.</span></span> <span data-ttu-id="b3112-219">HTML コンテンツを作成するには</span><span class="sxs-lookup"><span data-stu-id="b3112-219">To create the HTML content</span></span>

1. <span data-ttu-id="b3112-220">Visual Studio で、default.aspx ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="b3112-220">In Visual Studio, open the Default.aspx file.</span></span>
    
   <span data-ttu-id="b3112-221">このファイルには、2つの**asp: Content**要素が`ContentPlaceHolderID="PlaceHolderAdditionalPageHead"`含まれています。属性を持つ要素がページヘッダー `ContentPlaceHolderID="PlaceHolderMain"`内に追加され、その属性を持つ要素が page **body**要素内に配置されます。</span><span class="sxs-lookup"><span data-stu-id="b3112-221">The file includes two **asp:Content** elements: The element with the  `ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` attribute is added within the page header, and the element with the  `ContentPlaceHolderID="PlaceHolderMain"` attribute is placed within the page **body** element.</span></span> 
    
2. <span data-ttu-id="b3112-222">ページヘッダー `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead" runat="server">`のコントロールで、Project Server コンピュータ上のファイルへの参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="b3112-222">In the  `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead" runat="server">` control for the page header, add a reference to the PS.js file on the Project Server computer.</span></span> <span data-ttu-id="b3112-223">テストおよびデバッグの場合は、.PS を使用できます。</span><span class="sxs-lookup"><span data-stu-id="b3112-223">For testing and debugging, you can use PS.debug.js.</span></span> 
    
   ```HTML
     <script type="text/javascript" src="/_layouts/15/ps.debug.js"></script>
   ```

   <span data-ttu-id="b3112-224">アプリインフラストラクチャは、IIS `/_layouts/15/`の SharePoint サイトの仮想ディレクトリを使用します。</span><span class="sxs-lookup"><span data-stu-id="b3112-224">The app infrastructure uses the `/_layouts/15/` virtual directory for the SharePoint site in IIS.</span></span> <span data-ttu-id="b3112-225">物理ファイルは`%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.debug.js`です。</span><span class="sxs-lookup"><span data-stu-id="b3112-225">The physical file is  `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.debug.js`.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="b3112-226">運用のためにアプリを展開する前に`.debug` 、パフォーマンスを向上させるために、スクリプト参照からを削除してください。</span><span class="sxs-lookup"><span data-stu-id="b3112-226">Before you deploy the app for production use, remove  `.debug` from the script references to improve performance.</span></span> 
  
3. <span data-ttu-id="b3112-227">ページの`<asp:Content ContentPlaceHolderID="PlaceHolderMain" runat="server">`本文のコントロールで、生成された**div**要素を削除してから、UI オブジェクトの HTML コードを追加します。</span><span class="sxs-lookup"><span data-stu-id="b3112-227">In the  `<asp:Content ContentPlaceHolderID="PlaceHolderMain" runat="server">` control for the page body, delete the generated **div** element, and then add the HTML code for the UI objects.</span></span> <span data-ttu-id="b3112-228">**Table**要素には、ヘッダー行のみが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b3112-228">The **table** element contains only a header row.</span></span> <span data-ttu-id="b3112-229">[**タスク名**] 列には、チェックボックス入力コントロールが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b3112-229">The **Task name** column includes a check box input control.</span></span> <span data-ttu-id="b3112-230">**Caption**要素のテキストは、app.config ファイル内の**Getuserinfo**関数の**onGetUserNameSuccess**コールバックに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="b3112-230">Text for the **caption** element is replaced by the **onGetUserNameSuccess** callback for the **getUserInfo** function in the App.js file.</span></span> 
    
    ```HTML
    <form>
        <fieldset>
        <legend>Select assigned tasks</legend>
        <table id="assignmentsTable">
            <caption id="tableCaption">Replace caption</caption>
            <thead>
            <tr id="headerRow">
                <th>Project name</th>
                <th><input type="checkbox" id="headercheckbox" checked="checked" />Task name</th>
                <th>Actual work</th>
                <th>% complete</th>
                <th>Remaining work</th>
                <th>Due date</th>
            </tr>
            </thead>
        </table>
        </fieldset>
        <div id="inputPercentComplete" >
        Set percent complete for all selected assignments, or leave this
        <br /> field blank and set percent complete for individual assignments: 
        <input type="text" name="percentComplete" id="pctComplete" size="4"  maxlength="4" />
        </div>
        <div id="submitResult">
        <p><button id="btnSubmitUpdate" type="button" class="bottomButtons" ></button></p>
        <p id="message"></p>
        </div>
        <div id="refreshPage">
        <p><button id="btnRefresh" type="button" class="bottomButtons" >Refresh</button></p>
        </div>
        <div id="exitPage">
        <p><button id="btnExit" type="button" class="bottomButtons" >Exit</button></p>
        </div>
    </form>
    ```

4. <span data-ttu-id="b3112-231">App.xaml ファイルに、UI 要素の位置と外観の CSS コードを追加します。</span><span class="sxs-lookup"><span data-stu-id="b3112-231">In the App.css file, add CSS code for the position and appearance of the UI elements.</span></span> <span data-ttu-id="b3112-232">**Quickstatus**アプリの完全な CSS コードについては、「 [quickstatus app」セクションのコード例](#pj15_StatusingApp_Example)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b3112-232">For the complete CSS code of the **QuickStatus** app, see the [Example code for the QuickStatus app](#pj15_StatusingApp_Example) section.</span></span> 
    
<span data-ttu-id="b3112-233">手順 3 JavaScript 関数を追加して、割り当てを読み取り、テーブルの行を作成し、割り当ての達成率を変更して更新します。</span><span class="sxs-lookup"><span data-stu-id="b3112-233">Procedure 3 adds the JavaScript functions to read the assignments and create the table rows, and to change and update the assignment percent complete.</span></span> <span data-ttu-id="b3112-234">実際の手順は、さらに多くの場合、HTML コードを作成し、関連するスタイルと JavaScript 関数を追加してテストし、HTML コードを変更または追加し、そのプロセスを繰り返すことによって、アプリの開発において反復処理を行います。</span><span class="sxs-lookup"><span data-stu-id="b3112-234">The actual steps are more iterative in developing an app, where you alternately create some of the HTML code, add and test related styles and JavaScript functions, modify or add more HTML code, and then repeat the process.</span></span>

<span data-ttu-id="b3112-235"><a name="pj15_StatusingApp_JavaScript"> </a></span><span class="sxs-lookup"><span data-stu-id="b3112-235"></span></span>

### <a name="creating-the-javascript-functions-for-the-quickstatus-app"></a><span data-ttu-id="b3112-236">QuickStatus アプリ用の JavaScript 関数の作成</span><span class="sxs-lookup"><span data-stu-id="b3112-236">Creating the JavaScript functions for the QuickStatus app</span></span>

<span data-ttu-id="b3112-237">SharePoint アプリの Visual Studio テンプレートには、SharePoint クライアントコンテキストを取得する既定の初期化コードを含む App.config ファイルが含まれています。このファイルには、アプリページの基本的な get アクションおよび set アクションのデモが示されています。</span><span class="sxs-lookup"><span data-stu-id="b3112-237">The Visual Studio template for a SharePoint app includes the App.js file, which contains default initialization code that gets the SharePoint client context and demonstrates basic get and set actions for the app page.</span></span> <span data-ttu-id="b3112-238">SharePoint クライアント側の SP .js ライブラリの JavaScript 名前空間は**sp**です。</span><span class="sxs-lookup"><span data-stu-id="b3112-238">The JavaScript namespace for the SharePoint client-side SP.js library is **SP**.</span></span> <span data-ttu-id="b3112-239">Project Server アプリは、.PS ライブラリを使用するため、アプリは**ps**名前空間を使用してクライアントコンテキストを取得し、Project SERVER の jsom にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="b3112-239">Because a Project Server app uses the PS.js library, the app uses the **PS** namespace to get the client context and access the JSOM for Project Server.</span></span> 
  
<span data-ttu-id="b3112-240">**Quickstatus**アプリの JavaScript 関数には、次のようなものがあります。</span><span class="sxs-lookup"><span data-stu-id="b3112-240">JavaScript functions in the **QuickStatus** app include the following:</span></span> 
  
- <span data-ttu-id="b3112-241">Document **ready**イベントハンドラーは、ドキュメントオブジェクトモデル (DOM) のインスタンスが生成されたときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="b3112-241">The document **ready** event handler runs when the document object model (DOM) is instantiated.</span></span> <span data-ttu-id="b3112-242">**準備完了**イベントハンドラーは、次の4つの手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b3112-242">The **ready** event handler does the following four steps:</span></span> 
    
    1. <span data-ttu-id="b3112-243">プロジェクトサーバー JSOM および**Pwaweb**グローバル変数のクライアントコンテキストで**projcontext**グローバル変数を初期化します。</span><span class="sxs-lookup"><span data-stu-id="b3112-243">Initializes the **projContext** global variable with the client context for the Project Server JSOM and the **pwaWeb** global variable.</span></span> 
        
    2. <span data-ttu-id="b3112-244">**Getuserinfo**関数を呼び出して、 **projuser**グローバル変数を初期化します。</span><span class="sxs-lookup"><span data-stu-id="b3112-244">Calls the **getUserInfo** function to initialize the **projUser** global variable.</span></span> 
        
    3. <span data-ttu-id="b3112-245">ユーザーに対して指定された割り当てデータを取得する**getAssignments**関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b3112-245">Calls the **getAssignments** function, which gets specified assignment data for the user.</span></span> 
        
    4. <span data-ttu-id="b3112-246">[イベントハンドラー] を [テーブルヘッダー] チェックボックスに、[テーブルの各行のチェックボックスにバインドします。</span><span class="sxs-lookup"><span data-stu-id="b3112-246">Binds click event handlers to the table header check box, and to the check boxes in each row of the table.</span></span> <span data-ttu-id="b3112-247">Click イベントハンドラーは、ユーザーがテーブルのチェックボックスをオンまたはオフにしたときにチェックボックスのチェック**マークが付い**ている属性を管理します。</span><span class="sxs-lookup"><span data-stu-id="b3112-247">The click event handlers manage the **checked** attribute of the check boxes when the user selects or clears any check box in the table.</span></span> 
    
- <span data-ttu-id="b3112-248">**GetAssignments**関数が正常に実行された場合は、 **onGetAssignmentsSuccess**関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b3112-248">If the **getAssignments** function is successful, it calls the **onGetAssignmentsSuccess** function.</span></span> <span data-ttu-id="b3112-249">この関数は、各割り当てのテーブルに行を挿入し、各行の HTML コントロールを初期化してから、下部のボタンのプロパティを初期化します。</span><span class="sxs-lookup"><span data-stu-id="b3112-249">That function inserts a row in the table for each assignment, initializes the HTML controls in each row, and then initializes the bottom button properties.</span></span> 
    
- <span data-ttu-id="b3112-250">[**更新**] ボタンの**onClick**イベントハンドラーは、 **updateassignments**関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b3112-250">The **onClick** event handler for the **Update** button calls the **updateAssignments** function.</span></span> <span data-ttu-id="b3112-251">この関数は、選択された各割り当てに適用される達成率の値を取得します。または、[達成率] テキストボックスが空の場合、この関数は、テーブル内の選択された各割り当ての達成率を取得します。</span><span class="sxs-lookup"><span data-stu-id="b3112-251">That function gets the percent complete value that is applied to each selected assignment; or if the percent complete text box is empty, the function gets the percent complete of each selected assignment in the table.</span></span> <span data-ttu-id="b3112-252">**Updateassignments**関数は、状態の更新を保存して送信し、結果についてのメッセージをページの下部に書き込みます。</span><span class="sxs-lookup"><span data-stu-id="b3112-252">The **updateAssignments** function then saves and submits the status updates and writes a message about the results to the bottom of the page.</span></span> 
    
### <a name="procedure-3-to-create-the-javascript-functions"></a><span data-ttu-id="b3112-253">手順 3.</span><span class="sxs-lookup"><span data-stu-id="b3112-253">Procedure 3.</span></span> <span data-ttu-id="b3112-254">JavaScript 関数を作成するには</span><span class="sxs-lookup"><span data-stu-id="b3112-254">To create the JavaScript functions</span></span>

1. <span data-ttu-id="b3112-255">Visual Studio で、App.config ファイルを開き、ファイル内のすべてのコンテンツを削除します。</span><span class="sxs-lookup"><span data-stu-id="b3112-255">In Visual Studio, open the App.js file, and then delete all the content in the file.</span></span>
    
2. <span data-ttu-id="b3112-256">グローバル変数とドキュメント**準備**イベントハンドラーを追加します。</span><span class="sxs-lookup"><span data-stu-id="b3112-256">Add the global variables and the document **ready** event handler.</span></span> <span data-ttu-id="b3112-257">**Document**オブジェクトは、jQuery 関数を使用してアクセスされます。</span><span class="sxs-lookup"><span data-stu-id="b3112-257">The **document** object is accessed by using a jQuery function.</span></span> 
    
   <span data-ttu-id="b3112-258">[テーブルヘッダー] チェックボックスの click イベントハンドラーは、チェックボックスのオン/オフ状態を設定します。</span><span class="sxs-lookup"><span data-stu-id="b3112-258">The click event handler for the table header check box sets the checked state of the row check boxes.</span></span> <span data-ttu-id="b3112-259">すべての行のチェックボックスが選択されている場合、またはすべてオフになっている場合は、[行のクリックイベントハンドラー] チェックボックスをオンにして、ヘッダーのチェックボックスの状態を設定します。</span><span class="sxs-lookup"><span data-stu-id="b3112-259">If all of the row check boxes are selected or all are clear, the click event handler for the row check boxes sets the checked state of the header check box.</span></span> <span data-ttu-id="b3112-260">Click イベントハンドラーは、ページの下部にある結果メッセージも空の文字列に設定します。</span><span class="sxs-lookup"><span data-stu-id="b3112-260">The click event handlers also set the results message at the bottom of the page to an empty string.</span></span>
    
   ```js
    var projContext;
    var pwaWeb;
    var projUser;
    // This code runs when the DOM is ready and creates a ProjectContext object.
    // The ProjectContext object is required to use the JSOM for Project Server.
    $(document).ready(function () {
        projContext = PS.ProjectContext.get_current();
        pwaWeb = projContext.get_web();
        getUserInfo();
        getAssignments();
        // Bind a click event handler to the table header check box, which sets the row check boxes
        // to the checked state of the header check box, and sets the results message to an empty string.
        $('#headercheckbox').live('click', function (event) {
            $('input:checkbox:not(#headercheckbox)').attr('checked', this.checked);
            $get("message").innerText = "";
        });
        // Bind a click event handler to the row check boxes. If any row check box is cleared, clear
        // the header check box. If all of the row check boxes are selected, select the header check box.
        $('input:checkbox:not(#headercheckbox)').live('click', function (event) {
            var isChecked = true;
            $('input:checkbox:not(#headercheckbox)').each(function () {
                if (this.checked == false) isChecked = false;
                $get("message").innerText = "";
            });
            $("#headercheckbox").attr('checked', isChecked);
        });
    });
   ```

3. <span data-ttu-id="b3112-261">クエリが成功した場合は**onGetUserNameSuccess**を呼び出す**getuserinfo**関数を追加します。</span><span class="sxs-lookup"><span data-stu-id="b3112-261">Add the **getUserInfo** function, which calls **onGetUserNameSuccess** if the query is successful.</span></span> <span data-ttu-id="b3112-262">**OnGetUserNameSuccess**関数は、**キャプション**の段落の内容を、ユーザー名を含む表のキャプションに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="b3112-262">The **onGetUserNameSuccess** function replaces the contents of the **caption** paragraph with a table caption that includes the user name.</span></span> 
    
   ```js
        // Get information about the current user.
        function getUserInfo() {
            projUser = pwaWeb.get_currentUser();
            projContext.load(projUser);
            projContext.executeQueryAsync(onGetUserNameSuccess,
                // Anonymous function to execute if getUserInfo fails.
                function (sender, args) {
                    alert('Failed to get user name. Error: ' + args.get_message());
            });
        } 
        // This function is executed if the getUserInfo call is successful.
        function onGetUserNameSuccess() {
            var prefaceInfo = 'Assignments for ' + projUser.get_title();
            $('#tableCaption').text(prefaceInfo);
        }
   ```

4. <span data-ttu-id="b3112-263">割り当てクエリが成功した場合は、 **onGetAssignmentsSuccess**を呼び出す**getAssignments**関数を追加します (手順5を参照)。</span><span class="sxs-lookup"><span data-stu-id="b3112-263">Add the **getAssignments** function, which calls **onGetAssignmentsSuccess** (see step 5) if the assignment query is successful.</span></span> <span data-ttu-id="b3112-264">**Include**オプションは、指定されたフィールドのみを返すようにクエリを制限します。</span><span class="sxs-lookup"><span data-stu-id="b3112-264">The **Include** option limits the query to return only the fields specified.</span></span> 
    
   ```js
    // Get the collection of assignments for the current user.
    function getAssignments() {
        assignments = PS.EnterpriseResource.getSelf(projContext).get_assignments();
        // Register the request that you want to run on the server. The optional "Include" parameter 
        // requests only the specified properties for each assignment in the collection.
        projContext.load(assignments,
            'Include(Project, Name, ActualWork, ActualWorkMilliseconds, PercentComplete, RemainingWork, Finish, Task)');
        // Run the request on the server.
        projContext.executeQueryAsync(onGetAssignmentsSuccess,
            // Anonymous function to execute if getAssignments fails.
            function (sender, args) {
                alert('Failed to get assignments. Error: ' + args.get_message());
            });
    }
   ```

5. <span data-ttu-id="b3112-265">**OnGetAssignmentsSuccess**関数を追加します。この関数は、テーブルに割り当てごとに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="b3112-265">Add the **onGetAssignmentsSuccess** function, which adds a row for each assignment to the table.</span></span> <span data-ttu-id="b3112-266">**Prevprojname**変数は、ある行が別のプロジェクトに対してかどうかを判断するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b3112-266">The **prevProjName** variable is used to determine whether a row is for a different project.</span></span> <span data-ttu-id="b3112-267">その場合は、プロジェクト名が太字のフォントで表示されます。指定しない場合、プロジェクト名は空の文字列に設定されます。</span><span class="sxs-lookup"><span data-stu-id="b3112-267">If so, the project name is shown in a bold font; if not, the project name is set to an empty string.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="b3112-268">JSOM には、 **Actualwork timespan**など、csom に含まれる**TimeSpan**プロパティは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="b3112-268">The JSOM does not include **TimeSpan** properties that the CSOM includes, such as **ActualWorkTimeSpan**.</span></span> <span data-ttu-id="b3112-269">代わりに、JSOM は、PS などのミリ秒数のプロパティを使用し[ます。StatusAssignment プロパティ (Actualwork milliseconds)](https://msdn.microsoft.com/library/736bce1e-f734-0efe-6c5f-e0e891ab00ef%28Office.15%29.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="b3112-269">Instead, the JSOM uses properties for the number of milliseconds, such as the [PS.StatusAssignment.actualWorkMilliseconds](https://msdn.microsoft.com/library/736bce1e-f734-0efe-6c5f-e0e891ab00ef%28Office.15%29.aspx) property.</span></span> <span data-ttu-id="b3112-270">このプロパティを取得するメソッドは **、\_actualwork ミリ秒を取得**します。これは、整数値を返します。</span><span class="sxs-lookup"><span data-stu-id="b3112-270">The method to get that property is **get\_actualWorkMilliseconds**, which returns an integer value.</span></span> <span data-ttu-id="b3112-271">> **get_actualWork**メソッドは、"3h" などの文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="b3112-271">> The **get_actualWork** method returns a string such as "3h".</span></span> <span data-ttu-id="b3112-272">**Quickstatus**アプリではいずれの値も使用できますが、表示方法が異なります。</span><span class="sxs-lookup"><span data-stu-id="b3112-272">You could use either value in the **QuickStatus** app, but display it differently.</span></span> <span data-ttu-id="b3112-273">割り当てのクエリには両方のプロパティが含まれているため、デバッグ時に値をテストできます。</span><span class="sxs-lookup"><span data-stu-id="b3112-273">The assignments query includes both properties, so you can test the value during debugging.</span></span> <span data-ttu-id="b3112-274">**Actualwork**変数を削除した場合は、割り当てクエリで**actualwork**プロパティを削除することもできます。</span><span class="sxs-lookup"><span data-stu-id="b3112-274">If you remove the **actualWork** variable, you can also remove the **ActualWork** property in the assignments query.</span></span> 
  
   <span data-ttu-id="b3112-275">最後に、 **onGetAssignmentsSuccess**関数は、[**更新**] ボタン\*\*\*\* と [更新] ボタンをクリックして、click イベントハンドラーを初期化します。</span><span class="sxs-lookup"><span data-stu-id="b3112-275">Finally, the **onGetAssignmentsSuccess** function initializes the **Update** button and the **Refresh** button with click event handlers.</span></span> <span data-ttu-id="b3112-276">[**更新**] ボタンのテキスト値は、HTML コードで設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="b3112-276">The text value of the **Update** button could also be set in the HTML code.</span></span> 
    
   ```js
        // Get the enumerator, iterate through the assignment collection, 
        // and add each assignment to the table.
        function onGetAssignmentsSuccess(sender, args) {
            if (assignments.get_count() > 0) {
                var assignmentsEnumerator = assignments.getEnumerator();
                var projName = "";
                var prevProjName = "3D2A8045-4920-4B31-B3E7-9D0C5195FC70"; // Any unique name.
                var taskNum = 0;
                var chkTask = "";
                var txtPctComplete = "";
                // Constants for creating input controls in the table.
                var INPUTCHK = '<input type="checkbox" class="chkTask" checked="checked" id="chk';
                var LBLCHK = '<label for="chk';
                var INPUTTXT = '<input type="text" size="4"  maxlength="4" class="txtPctComplete" id="txt';
                while (assignmentsEnumerator.moveNext()) {
                    var statusAssignment = assignmentsEnumerator.get_current();
                    projName = statusAssignment.get_project().get_name();
                    // Get an integer, such as 3600000.
                    var actualWorkMilliseconds = statusAssignment.get_actualWorkMilliseconds(); 
                    // Get a string, such as "1h". Not used here.
                    var actualWork = statusAssignment.get_actualWork();
                    if (projName === prevProjName) {
                        projName = "";
                    }
                    prevProjName = statusAssignment.get_project().get_name();
                    // Create a row for the assignment information.
                    var row = assignmentsTable.insertRow();
                    taskNum++;
                    // Create an HTML string with a check box and task name label, for example:
                    // <input type="checkbox" class="chkTask" checked="checked" id="chk1" /> <label for="chk1">Task 1</label>
                    chkTask = INPUTCHK + taskNum + '" /> ' + LBLCHK + taskNum + '">' 
                        + statusAssignment.get_name() + '</label>';
                    txtPctComplete = INPUTTXT + taskNum + '" />';
                    // Insert cells for the assignment properties.
                    row.insertCell().innerHTML = '<strong>' + projName + '</strong>';
                    row.insertCell().innerHTML = chkTask;
                    row.insertCell().innerText = actualWorkMilliseconds / 3600000 + 'h';
                    row.insertCell().innerHTML = txtPctComplete;
                    row.insertCell().innerText = statusAssignment.get_remainingWork();
                    row.insertCell().innerText = statusAssignment.get_finish();
                    // Initialize the percent complete cell.
                    $get("txt" + taskNum).innerText = statusAssignment.get_percentComplete() + '%'
                }
            }
            else {
                $('p#message').attr('style', 'color: #0f3fdb');     // Blue text.
                $get("message").innerText = projUser.get_title() + ' has no assignments'
            }
            // Initialize the button properties.
            $get("btnSubmitUpdate").onclick = function() { updateAssignments(); };
            $get("btnSubmitUpdate").innerText = 'Update';
            $get('btnRefresh').onclick = function () { window.location.reload(true); };
            $get('btnExit').onclick = function () { exitToPwa(); };
        }
   ```

6. <span data-ttu-id="b3112-277">[**更新**] ボタンの**updateassignments**クリックイベントハンドラーを追加します。</span><span class="sxs-lookup"><span data-stu-id="b3112-277">Add the **updateAssignments** click event handler for the **Update** button.</span></span> <span data-ttu-id="b3112-278">ユーザーがタスクの達成率の値を変更したり、[**達成**率] テキストボックスに値を追加したりすると、"60"、"60%"、"60%" などのさまざまな形式で値を入力することができます。</span><span class="sxs-lookup"><span data-stu-id="b3112-278">When the user changes a value for percent complete of a task, or adds a value in the **percentComplete** text box, the value could be entered in several formats such as "60", "60%", or "60 %".</span></span> <span data-ttu-id="b3112-279">**Getnumericvalue**メソッドは、入力テキストの数値を返します。</span><span class="sxs-lookup"><span data-stu-id="b3112-279">The **getNumericValue** method returns the numeric value of the input text.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="b3112-280">運用環境で使用するように設計されているアプリでは、数値情報の入力値にフィールドの入力規則と追加のエラーチェックを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3112-280">In an app that is designed for production use, input values for numeric information should include field validation and additional error checking.</span></span> 
  
   <span data-ttu-id="b3112-281">**Updateassignments**の例には、基本的なエラーチェックが含まれており、ページの下部にある**メッセージ**の段落に情報が表示されます。更新クエリが成功した場合は緑色、入力エラーが発生した場合は赤、または更新クエリがいか.</span><span class="sxs-lookup"><span data-stu-id="b3112-281">The **updateAssignments** example includes some basic error checking, and displays information in the **message** paragraph at the bottom of the page—green if the update query is successful and red if there is an input error or the update query is unsuccessful.</span></span> 
    
   <span data-ttu-id="b3112-282">**Submitallstatusupdates**メソッドを使用する前に、アプリは PS を使用してサーバーに更新を保存する必要があり**ます。Status割り当てコレクション. update**メソッド。</span><span class="sxs-lookup"><span data-stu-id="b3112-282">Before using the **submitAllStatusUpdates** method, the app must save the updates to the server by using the **PS.StatusAssignmentCollection.update** method.</span></span> 
    
   ```js
        // Update all checked assignments. If the bottom percent complete field is blank,
        // use the value in the % complete field of each selected row in the table.
        function updateAssignments() {
            // Get percent complete from the bottom text box.
            var pctCompleteMain = getNumericValue($('#pctComplete').val()).trim();
            var pctComplete = pctCompleteMain;
            var assignmentsEnumerator = assignments.getEnumerator();
            var taskNum = 0;
            var taskRow = "";
            var indexPercent = "";
            var doSubmit = true;
            while (assignmentsEnumerator.moveNext()) {
                var pctCompleteRow = "";
                taskRow = "chk" + ++taskNum;
                if ($get(taskRow).checked) {
                    var statusAssignment = assignmentsEnumerator.get_current();
                    if (pctCompleteMain === "") {
                        // Get percent complete from the text box field in the table row.
                        pctCompleteRow = getNumericValue($('#txt' + taskNum).val());
                        pctComplete = pctCompleteRow;
                    }
                    // If both percent complete fields are empty, show an error.
                    if (pctCompleteMain === "" && pctCompleteRow === "") {
                        $('p#message').attr('style', 'color: #e11500');     // Red text.
                        $get("message").innerHTML =
                            '<b>Error:</b> Both <i>Percent complete</i> fields are empty, in row '
                            + taskNum
                            + ' and in the bottom textbox.<br/>One of those fields must have a valid percent.'
                            + '<p>Please refresh the page and try again.</p>';
                        doSubmit = false;
                        taskNum = 0;
                        break;
                    }
                    if (doSubmit) statusAssignment.set_percentComplete(pctComplete);
                }
            } 
            // Save and submit the assignment updates.
            if (doSubmit) {
                assignments.update();
                assignments.submitAllStatusUpdates();
                projContext.executeQueryAsync(function (source, args) {
                    $('p#message').attr('style', 'color: #0faa0d');     // Green text.
                    $get("message").innerText = 'Assignments have been updated.';
                }, function (source, args) {
                    $('p#message').attr('style', 'color: #e11500');     // Red text.
                    $get("message").innerText = 'Error updating assignments: ' + args.get_message();
                });
            }
        }
        // Get the numeric part for percent complete, from a string. For example, with "20 %", return "20".
        function getNumericValue(pctComplete) {
            pctComplete = pctComplete.trim();
            pctComplete = pctComplete.replace(/ /g, "");    // Remove interior spaces.
            indexPercent = pctComplete.indexOf('%', 0);
            if (indexPercent > -1) pctComplete = pctComplete.substring(0, indexPercent);
            return pctComplete;
        }
   ```

7. <span data-ttu-id="b3112-283">ホストプロジェクト Web App サイトの URL に**Sphosturl**クエリ文字列パラメーターを使用する**exittopwa**関数を追加します。</span><span class="sxs-lookup"><span data-stu-id="b3112-283">Add the **exitToPwa** function, which uses the **SPHostUrl** query string parameter for the URL of the host Project Web App site.</span></span> <span data-ttu-id="b3112-284">[タスク] ページに戻るには、 `"/Tasks.aspx"` URL にを追加します。</span><span class="sxs-lookup"><span data-stu-id="b3112-284">To navigate back to the Tasks page, append  `"/Tasks.aspx"` to the URL.</span></span> <span data-ttu-id="b3112-285">たとえば、 **Sphosturl**変数はに`https://ServerName/ProjectServerName/Tasks.aspx`設定します。</span><span class="sxs-lookup"><span data-stu-id="b3112-285">For example, the **spHostUrl** variable would be set to  `https://ServerName/ProjectServerName/Tasks.aspx`.</span></span>
    
   <span data-ttu-id="b3112-286">**Getquerystringparameter**関数は、 **quickstatus**ページの url を分割して、url オプションで指定されたパラメーターを抽出して返します。</span><span class="sxs-lookup"><span data-stu-id="b3112-286">The **getQueryStringParameter** function splits the URL of the **QuickStatus** page to extract and return the specified parameter in the URL options.</span></span> <span data-ttu-id="b3112-287">ドキュメントの例を次に示し**ます。** **Quickstatus**ドキュメントの URL 値 (すべて1行)。</span><span class="sxs-lookup"><span data-stu-id="b3112-287">Following is an example of the **document.URL** value for the **QuickStatus** document (all on one line):</span></span> 
    
   ```HTML
    https://app-ef98082fa37e3c.servername.officeapps.selfhost.corp.microsoft.com/pwa/
        QuickStatus/Pages/Default.aspx
        ?SPHostUrl=https%3A%2F%2Fsphvm%2D85178%2Fpwa
        &SPLanguage=en%2DUS
        &SPClientTag=1
        &SPProductNumber=15%2E0%2E4420%2E1022
        &SPAppWebUrl=https%3A%2F%2Fapp%2Def98082fa37e3c%2Eservername
            %2Eofficeapps%2Eselfhost%2Ecorp%2Emicrosoft%2Ecom%2Fpwa%2FQuickStatus
   ```

   <span data-ttu-id="b3112-288">前の URL の場合、 **Getquerystringparameter**関数は**sphosturl**クエリ文字列値を`https://ServerName/pwa`返します。</span><span class="sxs-lookup"><span data-stu-id="b3112-288">For the previous URL, the **getQueryStringParameter** function returns the **SPHostUrl** query string value,  `https://ServerName/pwa`.</span></span> 
    
   ```js
        // Exit the QuickStatus page and go back to the Tasks page in Project Web App.
        function exitToPwa() {
            // Get the SharePoint host URL, which is the top page of PWA, and add the Tasks page.
            var spHostUrl = decodeURIComponent(getQueryStringParameter('SPHostUrl'))
                            + "/Tasks.aspx";
            // Set the top window for the QuickStatus IFrame to the Tasks page.
            window.top.location.href = spHostUrl;
        }
        // Get a specified query string parameter from the {StandardTokens} URL option string.
        function getQueryStringParameter(urlParameterKey) {
            var docUrl = document.URL;
            var params = docUrl.split('?')[1].split('&');
            for (var i = 0; i < params.length; i++) {
                var theParam = params[i].split('=');
                if (theParam[0] == urlParameterKey)
                    return decodeURIComponent(theParam[1]);
            }
        }
   ```

<span data-ttu-id="b3112-289">この時点で**Quickstatus**アプリを発行して Project Web app に追加すると、アプリは [サイトコンテンツ] ページから実行できるようになりますが、ユーザーが簡単に使用できるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="b3112-289">If you publish the **QuickStatus** app at this point and add it to Project Web App, the app can be run from the Site Contents page, but it is not easily available to users.</span></span> <span data-ttu-id="b3112-290">ユーザーがアプリを見つけて実行できるようにするには、[タスク] ページのリボンにボタンを追加します。</span><span class="sxs-lookup"><span data-stu-id="b3112-290">To help users find and run the app, you can add a button for it to the ribbon on the Tasks page.</span></span> <span data-ttu-id="b3112-291">手順4は、リボンのカスタムアクションを追加する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="b3112-291">Procedure 4 shows how to add a ribbon custom action.</span></span> 

<span data-ttu-id="b3112-292"><a name="pj15_StatusingApp_ribbon"> </a></span><span class="sxs-lookup"><span data-stu-id="b3112-292"></span></span>

### <a name="adding-a-ribbon-custom-action"></a><span data-ttu-id="b3112-293">リボンのカスタム操作の追加</span><span class="sxs-lookup"><span data-stu-id="b3112-293">Adding a ribbon custom action</span></span>

<span data-ttu-id="b3112-294">Project Web App のリボンタブ、グループ、コントロールは、pwaribbon.xml ファイルで指定されています。このファイルは`[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\FEATURES\PWARibbon\listtemplates` 、project Server を実行しているコンピュータ上のディレクトリにインストールされます。</span><span class="sxs-lookup"><span data-stu-id="b3112-294">Ribbon tabs, groups, and controls for Project Web App are specified in the pwaribbon.xml file, which is installed in the  `[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\FEATURES\PWARibbon\listtemplates` directory on the computer running Project Server.</span></span> <span data-ttu-id="b3112-295">Project Web App のリボンのカスタムアクションを設計するために、Project 2013 SDK のダウンロードには pwaribbon.xml のコピーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b3112-295">To help design custom actions for the Project Web App ribbon, the Project 2013 SDK download includes a copy of pwaribbon.xml.</span></span> 
  
<span data-ttu-id="b3112-296">Project Web App では、[タスク] ページにさまざまなリボン定義が使用されています。これは、Project Web App インスタンスが、タイムシートとタスクの状態の両方の値を入力できるようにする単一入力モードを使用するかどうかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="b3112-296">Project Web App uses different ribbon definitions for the Tasks page, depending on whether the Project Web App instance uses single entry mode that enables users to enter values for both the timesheet and task status.</span></span> <span data-ttu-id="b3112-297">Project Web App の管理アクセス許可を持っている場合は、エントリモードを確認するには、ページの右上隅にあるドロップダウン設定メニューで [ **PWA 設定**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3112-297">If you have administrative permissions for Project Web App, to determine the entry mode, choose **PWA Settings** in the drop-down settings menu at the top-right corner of the page.</span></span> <span data-ttu-id="b3112-298">[PWA 設定] ページで、[**タイムシートの設定および既定値**] を選択し、ページの下部にある [**単一入力モード**] チェックボックスを確認します。</span><span class="sxs-lookup"><span data-stu-id="b3112-298">On the PWA Settings page, choose **Timesheet Settings and Defaults**, and then look at the **Single Entry Mode** check box at the bottom of the page.</span></span> 
  
<span data-ttu-id="b3112-299">単一入力モードがオフの場合、[タスク] ページのリボンは pwaribbon.xml の [自分の作業] 領域で定義されます。</span><span class="sxs-lookup"><span data-stu-id="b3112-299">When single entry mode is off, the ribbon on the Tasks page is defined by the My Work region in pwaribbon.xml:</span></span> 
  
```XML
   <!-- REGION My Work Ribbon-->
   <CustomAction
      Id="Ribbon.ContextualTabs.MyWork"
      . . .
```

<span data-ttu-id="b3112-300">単一入力モードがオンの場合、[タスク] ページのリボンは pwaribbon.xml の [結び付けられたモード] 領域で定義されます。</span><span class="sxs-lookup"><span data-stu-id="b3112-300">When single entry mode is on, the Tasks page ribbon is defined by the Tied Mode region in pwaribbon.xml:</span></span> 
  
```XML
   <!-- REGION Tied Mode Ribbon-->
   <CustomAction
      Id="Ribbon.ContextualTabs.TiedMode"
      . . .
```

<span data-ttu-id="b3112-301">各地域のグループとコントロールは似ていますが、結合されたモードのコントロールは、非連結モードの同じコントロールとは別の関数を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="b3112-301">Although the groups and controls in each region look similar, a control for the tied mode can call a different function than the same control for the non-tied mode.</span></span> <span data-ttu-id="b3112-302">手順4は、単一入力モードがオフのときに**Quickstatus**アプリにボタンコントロールを追加する方法を示しています ([**単一入力モード**] チェックボックスをオフにします)。</span><span class="sxs-lookup"><span data-stu-id="b3112-302">Procedure 4 shows how to add a button control for the **QuickStatus** app when single entry mode is off (the **Single Entry Mode** check box is clear).</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b3112-303">SharePoint アプリケーションのリボンまたはメニューにカスタムアクションを追加する方法の概要については、「 [sharepoint 用アプリを使用して展開するカスタムアクションを作成する](https://msdn.microsoft.com/library/jj163954.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b3112-303">For general information about adding custom actions to a ribbon or to a menu in a SharePoint application, see [Create custom actions to deploy with apps for SharePoint](https://msdn.microsoft.com/library/jj163954.aspx).</span></span> 
  
### <a name="procedure-4-to-add-a-ribbon-custom-action-to-the-tasks-page"></a><span data-ttu-id="b3112-304">手順 4.</span><span class="sxs-lookup"><span data-stu-id="b3112-304">Procedure 4.</span></span> <span data-ttu-id="b3112-305">[タスク] ページにリボンカスタムアクションを追加するには</span><span class="sxs-lookup"><span data-stu-id="b3112-305">To add a ribbon custom action to the Tasks page</span></span>

1. <span data-ttu-id="b3112-306">Project Web App の [タスク] ページでリボンを調べます。</span><span class="sxs-lookup"><span data-stu-id="b3112-306">Examine the ribbon on the Tasks page in Project Web App.</span></span> <span data-ttu-id="b3112-307">リボンの [**タスク**] タブを選択し、その変更方法を計画します。</span><span class="sxs-lookup"><span data-stu-id="b3112-307">Select the **TASKS** tab on the ribbon and plan how to modify it.</span></span> <span data-ttu-id="b3112-308">**提出**、**タスク**、**期間**など、7つのグループがあります。</span><span class="sxs-lookup"><span data-stu-id="b3112-308">There are seven groups, such as **Submit**, **Tasks**, and **Period**.</span></span> <span data-ttu-id="b3112-309">**Submit**グループには、[**保存**] ボタンと [**送信の状態**] ドロップダウンメニューという2つのコントロールがあります。</span><span class="sxs-lookup"><span data-stu-id="b3112-309">The **Submit** group has two controls, a **Save** button and a **Send Status** drop-down menu.</span></span> <span data-ttu-id="b3112-310">グループ内の任意の場所にコントロールを追加したり、[**タスク**] タブの任意の場所に新しいコントロールを含むグループを追加したり、ユーザー設定のグループとコントロールを持つ別のリボンタブを追加したりできます。</span><span class="sxs-lookup"><span data-stu-id="b3112-310">You can add a control at any location in a group, add a group with a new control at any location in the **TASKS** tab, or add another ribbon tab that has custom groups and controls.</span></span> <span data-ttu-id="b3112-311">この例では、3番目のボタンを**Submit**グループに追加します。ここでは、ボタンが**QUICKSTATUS**アプリの URL を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b3112-311">In this example, we add a third button to the **Submit** group, where the button invokes the URL of the **QuickStatus** app.</span></span> 
    
2. <span data-ttu-id="b3112-312">Visual Studio の [**ソリューションエクスプローラー** ] ウィンドウで、 **quickstatus**プロジェクトを右クリックして、新しいアイテムを追加します。</span><span class="sxs-lookup"><span data-stu-id="b3112-312">In the **Solution Explorer** pane in Visual Studio, right-click the **QuickStatus** project, and then add a new item.</span></span> <span data-ttu-id="b3112-313">[**新しいアイテムの追加**] ダイアログボックスで、[**リボンのカスタムアクション**] を選択します (図4を参照)。</span><span class="sxs-lookup"><span data-stu-id="b3112-313">In the **Add New Item** dialog box, choose **Ribbon Custom Action** (see Figure 4).</span></span> <span data-ttu-id="b3112-314">たとえば、ユーザー設定アクションの "Ribbonquick" アクションに名前を指定し、[**追加**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3112-314">For example, name the custom action RibbonQuickStatusAction, and then choose **Add**.</span></span>
    
   <span data-ttu-id="b3112-315">**図4リボンのカスタムアクションを追加する**</span><span class="sxs-lookup"><span data-stu-id="b3112-315">**Figure 4. Adding a ribbon custom action**</span></span>

   <span data-ttu-id="b3112-316">![リボンのカスタムアクションを追加]する(media/pj15_CreateStatusingApp_AddRibbonCustomAction.gif "リボンのカスタムアクションを追加")する</span><span class="sxs-lookup"><span data-stu-id="b3112-316">![Adding a ribbon custom action](media/pj15_CreateStatusingApp_AddRibbonCustomAction.gif "Adding a ribbon custom action")</span></span>
  
3. <span data-ttu-id="b3112-317">[**リボンのカスタムアクションの作成**] ウィザードの最初のページで、 **[ホスト Web** ] オプションが選択されたままにして、カスタムアクションのスコープのドロップダウンリストで [**なし**] を選択し、[**次へ**] を選択します (図5を参照)。</span><span class="sxs-lookup"><span data-stu-id="b3112-317">On the first page of the **Create Custom Action for Ribbon** wizard, leave the **Host Web** option selected, choose **None** in the drop-down list for the custom action scope, and then choose **Next** (see Figure 5).</span></span> <span data-ttu-id="b3112-318">ドロップダウンリスト内の項目は、Project Server ではなく、SharePoint に関連しています。</span><span class="sxs-lookup"><span data-stu-id="b3112-318">The items in the drop-down lists are relevant to SharePoint, not to Project Server.</span></span> <span data-ttu-id="b3112-319">カスタムアクションの生成された XML の大部分は、Project Server に適用されるように置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="b3112-319">We will replace most of the generated XML for the custom action so that it applies to Project Server.</span></span> 
    
   <span data-ttu-id="b3112-320">**図5リボンのカスタムアクションのプロパティを指定する**</span><span class="sxs-lookup"><span data-stu-id="b3112-320">**Figure 5. Specifying properties for the ribbon custom action**</span></span>

   <span data-ttu-id="b3112-321">![リボンのカスタムアクションのプロパティを指定する](media/pj15_CreateStatusingApp_RibbonCustomAction2.gif "リボンのカスタムアクションのプロパティを指定する")</span><span class="sxs-lookup"><span data-stu-id="b3112-321">![Specifying properties for the ribbon custom action](media/pj15_CreateStatusingApp_RibbonCustomAction2.gif "Specifying properties for the ribbon custom action")</span></span>
  
4. <span data-ttu-id="b3112-322">[**リボンのカスタムアクションの作成**] ウィザードの次のページで、設定のすべての既定値をそのまま使用し、[**完了**] を選択します (図6を参照)。</span><span class="sxs-lookup"><span data-stu-id="b3112-322">On the next page of the **Create Custom Action for Ribbon** wizard, leave all the default values for the settings, and then choose **Finish** (see Figure 6).</span></span> <span data-ttu-id="b3112-323">Visual Studio は、要素 .xml ファイルを含む**Ribbonquickstatusaction**フォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="b3112-323">Visual Studio creates the **RibbonQuickStatusAction** folder, which contains an Elements.xml file.</span></span> 
    
   <span data-ttu-id="b3112-324">**図6ボタンコントロールの設定を指定する**</span><span class="sxs-lookup"><span data-stu-id="b3112-324">**Figure 6. Specifying the settings for a button control**</span></span>

   <span data-ttu-id="b3112-325">![ボタンコントロールの設定を指定する](media/pj15_CreateStatusingApp_RibbonCustomAction3.gif "ボタンコントロールの設定を指定する")</span><span class="sxs-lookup"><span data-stu-id="b3112-325">![Specifying the settings for a button control](media/pj15_CreateStatusingApp_RibbonCustomAction3.gif "Specifying the settings for a button control")</span></span>
  
5. <span data-ttu-id="b3112-326">リボンカスタムアクションの要素 .xml ファイルで、既定で生成されたコードを変更します。</span><span class="sxs-lookup"><span data-stu-id="b3112-326">Modify the default generated code in the Elements.xml file for the ribbon custom action.</span></span> <span data-ttu-id="b3112-327">既定の XML コードは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="b3112-327">Following is the default XML code:</span></span>
    
   ```XML
    <?xml version="1.0" encoding="utf-8"?>
    <Elements xmlns="http://schemas.microsoft.com/sharepoint/">
        <CustomAction Id="21ea3aaf-79e5-4aac-9479-8eef14b4d9df.RibbonQuickStatusAction"
                    Location="CommandUI.Ribbon"
                    Sequence="10001"
                    Title="Invoke &apos;RibbonQuickStatusAction&apos; action">
        <CommandUIExtension>
            <!-- 
            Update the UI definitions below with the controls and the command actions
            that you want to enable for the custom action.
            -->
            <CommandUIDefinitions>
            <CommandUIDefinition Location="Ribbon.ListItem.Actions.Controls._children">
                <Button Id="Ribbon.ListItem.Actions.RibbonQuickStatusActionButton"
                        Alt="Request RibbonQuickStatusAction"
                        Sequence="100"
                        Command="Invoke_RibbonQuickStatusActionButtonRequest"
                        LabelText="Request RibbonQuickStatusAction"
                        TemplateAlias="o1"
                        Image32by32="_layouts/15/images/placeholder32x32.png"
                        Image16by16="_layouts/15/images/placeholder16x16.png" />
            </CommandUIDefinition>
            </CommandUIDefinitions>
            <CommandUIHandlers>
            <CommandUIHandler Command="Invoke_RibbonQuickStatusActionButtonRequest"
                                CommandAction="~appWebUrl/Pages/Default.aspx"/>
            </CommandUIHandlers>
        </CommandUIExtension >
        </CustomAction>
    </Elements>
   ```

   1. <span data-ttu-id="b3112-328">**CustomAction**要素で、 **Sequence**属性と**Title**属性を削除します。</span><span class="sxs-lookup"><span data-stu-id="b3112-328">In the **CustomAction** element, delete the **Sequence** attribute and the **Title** attribute.</span></span> 
    
   2. <span data-ttu-id="b3112-329">**送信**グループにコントロールを追加するには、pwaribbon.xml ファイル内の`Ribbon.ContextualTabs.MyWork.Home.Groups`コレクションの最初のグループ (を開始する要素) を検索`<Group Id="Ribbon.ContextualTabs.MyWork.Home.Page" Command="PageGroup" Sequence="10" Title="$Resources:pwafeatures,PAGE_PDP_CM_SUBMIT"`します。</span><span class="sxs-lookup"><span data-stu-id="b3112-329">To add a control to the **Submit** group, find the first group in the  `Ribbon.ContextualTabs.MyWork.Home.Groups` collection in the pwaribbon.xml file, which is the element that begins,  `<Group Id="Ribbon.ContextualTabs.MyWork.Home.Page" Command="PageGroup" Sequence="10" Title="$Resources:pwafeatures,PAGE_PDP_CM_SUBMIT"`.</span></span> <span data-ttu-id="b3112-330">子コントロールを**送信**グループに追加するために、次のコードは、Elements ファイル内の\*\*\*\* /////////////////の正しい**場所**の属性を示しています。</span><span class="sxs-lookup"><span data-stu-id="b3112-330">To add a child control to the **Submit** group, the following code shows the correct **Location** attribute of the **CommandUIDefinition** element in the Elements.xml file:</span></span> 
    
      ```XML
        <CommandUIDefinitions>
          <CommandUIDefinition Location="Ribbon.ContextualTabs.MyWork.Home.Page.Controls._children">
             . . .
          </CommandUIDefinition>
        </CommandUIDefinitions>
      ```

   3. <span data-ttu-id="b3112-331">子**Button**要素の属性値を次のように変更します。</span><span class="sxs-lookup"><span data-stu-id="b3112-331">Change the attribute values of the child **Button** element as follows:</span></span> 
    
       ```XML
            <Button Id="Ribbon.ContextualTabs.MyWork.Home.Page.QuickStatus"
                    Alt="Quick Status app"
                    Sequence="30"
                    Command="Invoke_QuickStatus"
                    LabelText="Quick Status"
                    TemplateAlias="o1"
                    Image16by16="_layouts/15/1033/images/ps16x16.png" 
                    Image16by16Left="-80"
                    Image16by16Top="-144"
                    Image32by32="_layouts/15/1033/images/ps32x32.png" 
                    Image32by32Left="-32"
                    Image32by32Top="-288" 
                    ToolTipTitle="QuickStatus"
                    ToolTipDescription="Run the QuickStatus app" />
       ```

       - <span data-ttu-id="b3112-332">このボタンをグループ内の3番目のコントロールにするには、 **Sequence**属性に既存の`Sequence="20"` **送信状態**コントロール (pwaribbon.xml の**FlyoutAnchor**要素) の値よりも大きい数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="b3112-332">To make the button the third control in the group, the **Sequence** attribute can be any number higher than the  `Sequence="20"` value of the existing **Send Status** control (which is a **FlyoutAnchor** element in pwaribbon.xml).</span></span> <span data-ttu-id="b3112-333">規則によって、グループとコントロールのシーケンス番号`10, 20, 30, …`がで、要素を中間位置に挿入できるようになります。</span><span class="sxs-lookup"><span data-stu-id="b3112-333">By convention, the sequence numbers of groups and controls are  `10, 20, 30, …`, which enables elements to be inserted in intermediate positions.</span></span>
    
       - <span data-ttu-id="b3112-334">**Command**属性には、コマンドを指定します\*\*\*\* 。このコマンドは、コマンドを指定します (次の手順5を参照)。</span><span class="sxs-lookup"><span data-stu-id="b3112-334">The **Command** attribute specifies the command to run in the **CommandUIHandler** element (see the following step 5.d).</span></span> <span data-ttu-id="b3112-335">次の開発者にとって簡単になるように、コマンド名を簡略化することができます。</span><span class="sxs-lookup"><span data-stu-id="b3112-335">You can simplify the command name to make it easier for the next developer.</span></span> <span data-ttu-id="b3112-336">たとえば`Command="Invoke_QuickStatus"` 、より`Command="Invoke_RibbonQuickStatusActionButtonRequest"`読みやすくなります。</span><span class="sxs-lookup"><span data-stu-id="b3112-336">For example  `Command="Invoke_QuickStatus"` is easier to read than  `Command="Invoke_RibbonQuickStatusActionButtonRequest"`.</span></span>
    
       - <span data-ttu-id="b3112-337">イメージ属性は、16 x 16 ピクセルアイコンと、ボタンコントロールの 32 x 32 ピクセルアイコンを指定します。</span><span class="sxs-lookup"><span data-stu-id="b3112-337">The image attributes specify the 16 x 16-pixel icon and the 32 x 32-pixel icon for the button control.</span></span> <span data-ttu-id="b3112-338">既定の要素 .xml ファイルで、 `Image32by32="_layouts/15/images/placeholder32x32.png"`オレンジ色のドットを指定します。</span><span class="sxs-lookup"><span data-stu-id="b3112-338">In the default Elements.xml file,  `Image32by32="_layouts/15/images/placeholder32x32.png"` specifies an orange dot.</span></span> <span data-ttu-id="b3112-339">Project Server を実行しているコンピューターの`[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\1033\IMAGES`ディレクトリにインストールされているイメージマップファイル (ps16x16 および ps32x32) からアイコンを抽出することができます。</span><span class="sxs-lookup"><span data-stu-id="b3112-339">You can extract icons from the image map files (ps16x16.png and ps32x32.png) that are installed in the  `[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\1033\IMAGES` directory on the computer running Project Server.</span></span> <span data-ttu-id="b3112-340">たとえば、32 x 32 ピクセルのアイコンは、左から10番目のアイコン、ps32x32 イメージマップの上部から10行下にスクロールされます (アイコンの上部は9行目の末尾の後、9行は32ピクセル/行 = 288 ピクセルです)。</span><span class="sxs-lookup"><span data-stu-id="b3112-340">For example, the 32 x 32-pixel icon is in the second column of icons from the left and the tenth row down from the top of the ps32x32.png image map (the top of the icon is after the end of the ninth row; 9 rows x 32 pixels/row = 288 pixels).</span></span> 
    
       - <span data-ttu-id="b3112-341">[ボタン] コントロールのツールヒントを表示するには、 **ToolTipTitle**属性と**ToolTipDescription**属性を追加します。</span><span class="sxs-lookup"><span data-stu-id="b3112-341">To show a tool tip for the button control, add the **ToolTipTitle** attribute and the **ToolTipDescription** attribute.</span></span> 
    
    4. <span data-ttu-id="b3112-342">//または**Ihandler**要素の属性を変更します。</span><span class="sxs-lookup"><span data-stu-id="b3112-342">Change the attributes of the **CommandUIHandler** element.</span></span> <span data-ttu-id="b3112-343">たとえば、 **command**属性が**Button**要素の**コマンド**属性値と一致することを確認します。</span><span class="sxs-lookup"><span data-stu-id="b3112-343">For example, ensure that the **Command** attribute matches the **Command** attribute value for the **Button** element.</span></span> <span data-ttu-id="b3112-344">**Commandaction**属性に`~appWebUrl`は、 **QUICKSTATUS** web ページの URL のプレースホルダーがあります。</span><span class="sxs-lookup"><span data-stu-id="b3112-344">For the **CommandAction** attribute,  `~appWebUrl` is a placeholder for the URL of the **QuickStatus** webpage.</span></span> <span data-ttu-id="b3112-345">リボンボタンが**Quickstatus**アプリを起動すると、 **{standardtokens}** トークンは、 **sphosturl**、 **SPLanguage**、 **Sphosturl**、 **sphosturl**、および SPAppWebUrl を含む URL オプションに置き換えられます。 \*\*\*\*.</span><span class="sxs-lookup"><span data-stu-id="b3112-345">When the ribbon button invokes the **QuickStatus** app, the **{StandardTokens}** token is replaced by URL options that include **SPHostUrl**, **SPLanguage**, **SPClientTag**, **SPProductNumber**, and **SPAppWebUrl**.</span></span>
    
        ```XML
            <CommandUIHandlers>
                <CommandUIHandler Command="Invoke_QuickStatus"
                                  CommandAction="~appWebUrl/Pages/Default.aspx?{StandardTokens}"/>
            </CommandUIHandlers>
        ```

6. <span data-ttu-id="b3112-346">**ソリューションエクスプローラー**で、 **Feature1**デザイナーを開き、[ソリューション] ウィンドウ**内の項目**から [機能] ウィンドウ内の**項目**に [ **ribbonquickstatusaction** ] アイテムを移動します。</span><span class="sxs-lookup"><span data-stu-id="b3112-346">In **Solution Explorer**, open the **Feature1.feature** designer, and move the **RibbonQuickStatusAction** item from the **Items in the Solution** pane to the **Items in the Feature** pane.</span></span> <span data-ttu-id="b3112-347">その後、パッケージデザイナー \*\*\*\* を開くと、[パッケージ] ウィンドウの**項目**に [ **ribbonquickstatusaction** ] アイテムが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b3112-347">If you then open the **Package.package** designer, the **RibbonQuickStatusAction** item will be in the **Items in the Package** pane.</span></span> 
    
<span data-ttu-id="b3112-348">アプリの開発とリボンボタンの追加では、通常、アプリをテストし、デバッグのために JavaScript コードでブレークポイントを設定します。</span><span class="sxs-lookup"><span data-stu-id="b3112-348">As you develop the app and add a ribbon button, you normally test the app and set breakpoints in the JavaScript code for debugging.</span></span> <span data-ttu-id="b3112-349">**F5**キーを押してデバッグを開始すると、Visual Studio によってアプリがコンパイルされ、 **quickstatus**プロジェクトの [**サイト URL** ] プロパティで指定されたサイトに展開され、アプリを信頼するかどうかを確認するページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b3112-349">When you press **F5** to start debugging, Visual Studio compiles the app, deploys it to the site that is specified in the **Site URL** property of the **QuickStatus** project, and displays a page that asks whether you trust the app.</span></span> <span data-ttu-id="b3112-350">作業を続行して**Quickstatus**アプリを終了すると、Project Web app の [タスク] ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="b3112-350">When you proceed and then exit the **QuickStatus** app, it returns to the Tasks page in Project Web App.</span></span> 

> [!NOTE]
> <span data-ttu-id="b3112-351">図7は、リボンの [**タスク**] タブの [**クイック状態**] ボタンが無効になっていることを示しています。</span><span class="sxs-lookup"><span data-stu-id="b3112-351">Figure 7 shows that the **Quick Status** button on the **TASKS** tab of the ribbon is disabled.</span></span> <span data-ttu-id="b3112-352">Visual Studio を使用して多数のデバッグを展開した後、同じテストサーバーで発行済みアプリのデバッグまたは展開を続行するときに、カスタムリボンコントロールをブロックすることができます。</span><span class="sxs-lookup"><span data-stu-id="b3112-352">After many debug deployments with Visual Studio, custom ribbon controls can be blocked when you continue to debug or deploy the published app on the same test server.</span></span> <span data-ttu-id="b3112-353">このボタンを有効にするには、Visual Studio の [ **Ribbonquickstatusaction アクション**アイテムを削除してから、名前と ID が異なる新しいリボンアクションを作成します。</span><span class="sxs-lookup"><span data-stu-id="b3112-353">To enable the button, delete the **RibbonQuickStatusAction** item in Visual Studio, and then create a new ribbon action that has a different name and ID.</span></span> <span data-ttu-id="b3112-354">それでも問題が解決しない場合は、Project Web App テストインスタンスからアプリを削除してから、別のアプリ ID を使用してアプリを再作成してみてください。</span><span class="sxs-lookup"><span data-stu-id="b3112-354">If that doesn't solve the problem, try removing the app from the Project Web App test instance, and then recreate the app with a different app ID.</span></span> 
  
<span data-ttu-id="b3112-355">**図7無効になっているクイック状態ボタンのツールヒントの表示**</span><span class="sxs-lookup"><span data-stu-id="b3112-355">**Figure 7. Viewing the tooltip of the disabled Quick Status button**</span></span>

<span data-ttu-id="b3112-356">![無効にされたボタンのツールヒントの表示](media/pj15_CreateStatusingApp_ButtonToolTipDisabled.gif "無効にされたボタンのツールヒントの表示")</span><span class="sxs-lookup"><span data-stu-id="b3112-356">![Viewing the tooltip of the disabled button](media/pj15_CreateStatusingApp_ButtonToolTipDisabled.gif "Viewing the tooltip of the disabled button")</span></span>
  
<span data-ttu-id="b3112-357">手順5は、 **Quickstatus**アプリを展開してインストールする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="b3112-357">Procedure 5 shows how to deploy and install the **QuickStatus** app.</span></span> <span data-ttu-id="b3112-358">手順6は、アプリをインストールした後にテストするための追加の手順を示しています。</span><span class="sxs-lookup"><span data-stu-id="b3112-358">Procedure 6 shows some additional steps in testing the app after you have installed it.</span></span> 

<span data-ttu-id="b3112-359"><a name="pj15_StatusingApp_Deploying"> </a></span><span class="sxs-lookup"><span data-stu-id="b3112-359"></span></span>

## <a name="deploying-the-quickstatus-app"></a><span data-ttu-id="b3112-360">QuickStatus アプリの展開</span><span class="sxs-lookup"><span data-stu-id="b3112-360">Deploying the QuickStatus app</span></span>

<span data-ttu-id="b3112-361">SharePoint web アプリケーション (Project Web App など) にアプリを展開するには、いくつかの方法があります。</span><span class="sxs-lookup"><span data-stu-id="b3112-361">There are several ways to deploy an app to a SharePoint web application such as Project Web App.</span></span> <span data-ttu-id="b3112-362">どの展開を使用するかは、アプリをプライベート SharePoint カタログに発行するか、パブリック Office ストアに発行するか、または SharePoint がオンプレミスでインストールされるか、またはオンラインテナントであるかによって決まります。</span><span class="sxs-lookup"><span data-stu-id="b3112-362">Which deployment you use will depend on whether you want to publish the app to a private SharePoint catalog or to the public Office Store, and whether SharePoint is installed on-premises or is an online tenancy.</span></span> <span data-ttu-id="b3112-363">手順5は、 **Quickstatus**アプリをプライベートアプリカタログの社内インストールに展開する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="b3112-363">Procedure 5 shows how to deploy the **QuickStatus** app to an on-premises installation in a private app catalog.</span></span> <span data-ttu-id="b3112-364">詳細については、「 [Install and manage apps For sharepoint 2013](https://technet.microsoft.com/library/fp161232.aspx) 」および「 [sharepoint 用アプリを発行](https://msdn.microsoft.com/library/jj164070.aspx)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b3112-364">For more information, see [Install and manage apps for SharePoint 2013](https://technet.microsoft.com/library/fp161232.aspx) and [Publish apps for SharePoint](https://msdn.microsoft.com/library/jj164070.aspx)</span></span>
  
> [!NOTE]
> <span data-ttu-id="b3112-365">SharePoint カタログにアプリを追加するには、SharePoint 管理者権限が必要です。</span><span class="sxs-lookup"><span data-stu-id="b3112-365">Adding an app to a SharePoint catalog requires SharePoint administrator permissions.</span></span> 
  
### <a name="procedure-5-to-deploy-the-quickstatus-app"></a><span data-ttu-id="b3112-366">手順 5.</span><span class="sxs-lookup"><span data-stu-id="b3112-366">Procedure 5.</span></span> <span data-ttu-id="b3112-367">QuickStatus アプリを展開するには</span><span class="sxs-lookup"><span data-stu-id="b3112-367">To deploy the QuickStatus app</span></span>

1. <span data-ttu-id="b3112-368">Visual Studio で、すべてのファイルを保存し、**ソリューションエクスプローラー**で**quickstatus**プロジェクトを右クリックして、[**発行**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3112-368">In Visual Studio, save all of the files, and then right-click the **QuickStatus** project in the **Solution Explorer** and choose **Publish**.</span></span>
    
2. <span data-ttu-id="b3112-369">**Quickstatus**アプリは SharePoint ホストされているため、発行に関するオプションはほとんどありません (図8を参照)。</span><span class="sxs-lookup"><span data-stu-id="b3112-369">Because the **QuickStatus** app is SharePoint-hosted, there are very few options for publishing (see Figure 8).</span></span> <span data-ttu-id="b3112-370">[ **Office 用アプリと SharePoint 用アプリの発行**] ダイアログボックスで、[**完了**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3112-370">In the **Publish apps for Office and SharePoint** dialog box, choose **Finish**.</span></span>
    
   <span data-ttu-id="b3112-371">**図8QuickStatus アプリの発行**</span><span class="sxs-lookup"><span data-stu-id="b3112-371">**Figure 8. Publishing the QuickStatus app**</span></span>

   <span data-ttu-id="b3112-372">![発行ウィザードの使用](media/pj15_CreateStatusingApp_PublishWizard.gif "発行ウィザードの使用")</span><span class="sxs-lookup"><span data-stu-id="b3112-372">![Using the Publish Wizard](media/pj15_CreateStatusingApp_PublishWizard.gif "Using the Publish Wizard")</span></span>
  
3. <span data-ttu-id="b3112-373">QuickStatus. app ファイルを、 `~\QuickStatus\bin\Debug\app.publish\1.0.0.0`ディレクトリからローカルコンピューター上の便利なディレクトリ (またはオンプレミスのインストールの場合は SharePoint コンピューター) にコピーします。</span><span class="sxs-lookup"><span data-stu-id="b3112-373">Copy the QuickStatus.app file from the  `~\QuickStatus\bin\Debug\app.publish\1.0.0.0` directory to a convenient directory on the local computer (or to the SharePoint computer for an on-premises installation).</span></span> 
    
4. <span data-ttu-id="b3112-374">SharePoint サーバーの全体管理で、サイドリンクバーの [**アプリ**] を選択し、[**アプリカタログの管理**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3112-374">In SharePoint Central Administration, choose **Apps** in the Quick Launch, and then choose **Manage App Catalog**.</span></span>
    
5. <span data-ttu-id="b3112-375">アプリカタログが存在しない場合は、「 [SharePoint 2013 でアプリカタログを管理](https://technet.microsoft.com/library/fp161234.aspx)する」の「 *Web アプリケーションのアプリカタログサイトを構成*する」セクションに従って、アプリカタログのサイトコレクションを作成します。</span><span class="sxs-lookup"><span data-stu-id="b3112-375">If an app catalog does not exist, create a site collection for the app catalog, by following the  *Configure the App Catalog site for a web application*  section in [Manage the App Catalog in SharePoint 2013](https://technet.microsoft.com/library/fp161234.aspx).</span></span>
    
   <span data-ttu-id="b3112-376">アプリカタログが存在する場合は、[アプリカタログの管理] ページでサイトの URL に移動します。</span><span class="sxs-lookup"><span data-stu-id="b3112-376">If an app catalog exists, navigate to the site URL on the Manage App Catalog page.</span></span> <span data-ttu-id="b3112-377">たとえば、次の手順では、アプリカタログサイトは`https://ServerName/sites/TestApps`です。</span><span class="sxs-lookup"><span data-stu-id="b3112-377">For example, in the following steps, the app catalog site is  `https://ServerName/sites/TestApps`.</span></span>
    
6. <span data-ttu-id="b3112-378">[アプリカタログ] ページで、サイドリンクバーの [ **SharePoint 用アプリ**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3112-378">On the app catalog page, choose **Apps for SharePoint** in the Quick Launch.</span></span> <span data-ttu-id="b3112-379">[SharePoint 用アプリ] ページのリボンの [**ファイル**] タブで、[**ドキュメントのアップロード**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3112-379">On the Apps for SharePoint page, on the **FILES** tab of the ribbon, choose **Upload Document**.</span></span>
    
7. <span data-ttu-id="b3112-380">[**ドキュメントの追加**] ダイアログボックスで、quickstatus. app ファイルを参照し、そのバージョンのコメントを追加して、[ **OK]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3112-380">In the **Add a document** dialog box, browse for the QuickStatus.app file, add comments for the version, and then choose **OK**.</span></span>
    
8. <span data-ttu-id="b3112-381">アプリを追加するときに、アプリの説明、アイコン、およびその他の情報のローカル情報を追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="b3112-381">When you add an app, you can also add local information for the app description, icon, and other information.</span></span> <span data-ttu-id="b3112-382">[ **Sharepoint 用アプリ-QuickStatus. app** ] ダイアログボックスで、アプリに対して表示する情報を sharepoint サイトコレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="b3112-382">In the **Apps for SharePoint - QuickStatus.app** dialog box, add the information that you want to show for the app in the SharePoint site collection.</span></span> <span data-ttu-id="b3112-383">たとえば、次の情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="b3112-383">For example, add the following information:</span></span> 
    
   1. <span data-ttu-id="b3112-384">**簡単な説明**フィールド: 「Quick Status test app」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b3112-384">**Short Description** field: Type Quick Status test app.</span></span>
    
   2. <span data-ttu-id="b3112-385">**説明**フィールド: 複数のプロジェクトのタスクの達成率を更新するには、「テストアプリ」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b3112-385">**Description** field: Type Test app to update percent complete for tasks in multiple projects.</span></span>
    
   3. <span data-ttu-id="b3112-386">**アイコンの URL**フィールド: アプリカタログのサイトアセットにアプリアイコン用の 96 x 96 ピクセルのイメージを追加します。</span><span class="sxs-lookup"><span data-stu-id="b3112-386">**Icon URL** fields: Add a 96 x 96-pixel image for the app icon to the site assets for the app catalog.</span></span> <span data-ttu-id="b3112-387">たとえば、に`https://ServerName/sites/TestApps`移動して、[**設定**] ドロップダウンメニューの [**サイトコンテンツ**] を選択し、[**サイトアセット**] を選択してから、quickstatusapp イメージを追加します。</span><span class="sxs-lookup"><span data-stu-id="b3112-387">For example, navigate to  `https://ServerName/sites/TestApps`, choose **Site contents** in the **Settings** drop-down menu, choose **Site Assets**, and then add the quickStatusApp.png image.</span></span> <span data-ttu-id="b3112-388">**Quickstatusapp**アイテムを右クリックし、[**プロパティ**] を選択して、[**プロパティ**] ダイアログボックスで**アドレス (URL)** 値をコピーします。</span><span class="sxs-lookup"><span data-stu-id="b3112-388">Right-click the **quickStatusApp** item, choose **Properties**, and then copy the **Address (URL)** value in the **Properties** dialog box.</span></span> <span data-ttu-id="b3112-389">たとえば、[アイコン`https://ServerName/sites/TestApps/SiteAssets/QuickStatusApp.png`の**URL**の web アドレス] フィールドに値をコピーして貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="b3112-389">For example, copy  `https://ServerName/sites/TestApps/SiteAssets/QuickStatusApp.png`, and then paste the value in the **Icon URL** web address field.</span></span> <span data-ttu-id="b3112-390">アイコンの説明を入力します (図9のように)、「簡易状態 app アイコン」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b3112-390">Type a description for the icon, for example (as in Figure 9), type QuickStatus app icon.</span></span> <span data-ttu-id="b3112-391">URL が有効であることをテストします。</span><span class="sxs-lookup"><span data-stu-id="b3112-391">Test that the URL is valid.</span></span>
    
      <span data-ttu-id="b3112-392">**図9QuickStatus アプリのアイコン URL を追加する**</span><span class="sxs-lookup"><span data-stu-id="b3112-392">**Figure 9. Adding an icon URL for the QuickStatus app**</span></span>

      <span data-ttu-id="b3112-393">![アプリの SharePoint でのプロパティの設定](media/pj15_CreateStatusingApp_AddAppToSharePointSettings.gif "アプリの SharePoint でのプロパティの設定")</span><span class="sxs-lookup"><span data-stu-id="b3112-393">![Setting properties in SharePoint for the app](media/pj15_CreateStatusingApp_AddAppToSharePointSettings.gif "Setting properties in SharePoint for the app")</span></span>
  
   4. <span data-ttu-id="b3112-394">**Category**フィールド: 既存のカテゴリを選択するか、独自の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="b3112-394">**Category** field: Choose an existing category, or specify your own value.</span></span> <span data-ttu-id="b3112-395">たとえば、「Statusing」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b3112-395">For example, type Statusing.</span></span>
    
      > [!NOTE]
      > <span data-ttu-id="b3112-396">**Statusing**という名前のカテゴリは、テスト目的でのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="b3112-396">A category named **Statusing** is just for testing purposes.</span></span> <span data-ttu-id="b3112-397">Project Server アプリの一般的なカテゴリは**プロジェクト管理**です。</span><span class="sxs-lookup"><span data-stu-id="b3112-397">A typical category for Project Server apps is **Project Management**.</span></span> 
  
   5. <span data-ttu-id="b3112-398">[**発行元の名前**] フィールド: 発行元の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="b3112-398">**Publisher name** field: Type the name of the publisher.</span></span> <span data-ttu-id="b3112-399">この例では、「Project SDK」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b3112-399">In this example, type Project SDK.</span></span>
    
   6. <span data-ttu-id="b3112-400">**有効になっている**フィールド: アプリを Project Web app サイト管理者がインストールできるようにするには、[**有効**] チェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="b3112-400">**Enabled** field: To make the app visible to Project Web App site administrators for installation, select the **Enabled** check box.</span></span> 
    
   7. <span data-ttu-id="b3112-401">その他のフィールドは省略可能です。</span><span class="sxs-lookup"><span data-stu-id="b3112-401">Additional fields are optional.</span></span> <span data-ttu-id="b3112-402">たとえば、[アプリの詳細] ページのサポート URL と複数のヘルプイメージを追加できます。</span><span class="sxs-lookup"><span data-stu-id="b3112-402">For example, you can add a support URL and multiple help images for the app details page.</span></span> <span data-ttu-id="b3112-403">図9では、**画像 url 1**フィールドには、アプリのスクリーンショットの url とスクリーンショットの説明が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b3112-403">In Figure 9, the **Image URL 1** fields include the URL for a screenshot of the app and a description of the screenshot.</span></span> 
    
   8. <span data-ttu-id="b3112-404">[ **SharePoint 用アプリ-quickstatus** ] ダイアログボックスで、[**保存**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3112-404">In the **Apps for SharePoint - QuickStatus.app** dialog box, choose **Save**.</span></span> <span data-ttu-id="b3112-405">図9では、SharePoint 用アプリライブラリの**クイックステータス更新**アイテムが編集用にチェックアウトされているので、ダイアログボックスのリボンの [**編集**] タブで、[**チェックイン**] を選択してプロセスを完了します (図10を参照)。</span><span class="sxs-lookup"><span data-stu-id="b3112-405">In Figure 9, the **Quick Status Update** item in the Apps for SharePoint library is checked out for editing, so on the **EDIT** tab of the dialog box ribbon, you would choose **Check In** to complete the process (see Figure 10).</span></span> 
    
      <span data-ttu-id="b3112-406">**図10QuickStatus アプリが SharePoint 用アプリライブラリに追加されます。**</span><span class="sxs-lookup"><span data-stu-id="b3112-406">**Figure 10. The QuickStatus app is added to the Apps for SharePoint library.**</span></span>

      <span data-ttu-id="b3112-407">![QuickStatus アプリが SharePoint に追加されます]。(media/pj15_CreateStatusingApp_AddAppToSharePoint.gif "QuickStatus アプリが SharePoint に追加されます")。</span><span class="sxs-lookup"><span data-stu-id="b3112-407">![The QuickStatus app is added to SharePoint](media/pj15_CreateStatusingApp_AddAppToSharePoint.gif "The QuickStatus app is added to SharePoint")</span></span>
  
9. <span data-ttu-id="b3112-408">Project Web App の [**設定**] ドロップダウンメニューで、[**アプリの追加**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3112-408">In Project Web App, in the **Settings** drop-down menu, choose **Add an app**.</span></span> <span data-ttu-id="b3112-409">[自分のアプリ] ページのサイドリンクバーで、[**組織から**] を選択し、**クイック進捗更新**アプリの [**アプリの詳細**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3112-409">On the Your Apps page, in the Quick Launch, choose **From Your Organization**, and then choose **App Details** for the **Quick Status Update** app.</span></span> <span data-ttu-id="b3112-410">図11は、前の手順で追加したアプリアイコン、スクリーンショット、およびその他の情報を含む詳細ページを示しています。</span><span class="sxs-lookup"><span data-stu-id="b3112-410">Figure 11 shows the details page with the app icon, screenshot, and other information that you added in the previous step.</span></span> 
    
   <span data-ttu-id="b3112-411">**図11Project Web App の [クイック進捗の更新の詳細] ページを使用する**</span><span class="sxs-lookup"><span data-stu-id="b3112-411">**Figure 11. Using the Quick Status Update details page in Project Web App**</span></span>

   <span data-ttu-id="b3112-412">![QuickStatus アプリを Project Web app に追加する](media/pj15_CreateStatusingApp_AddAppToPWA.gif "QuickStatus アプリを Project Web app に追加する")</span><span class="sxs-lookup"><span data-stu-id="b3112-412">![Adding the QuickStatus app to Project Web App](media/pj15_CreateStatusingApp_AddAppToPWA.gif "Adding the QuickStatus app to Project Web App")</span></span>
  
10. <span data-ttu-id="b3112-413">[クイック進捗状況の更新の詳細] ページで、[**追加**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3112-413">On the Quick Status Update details page, choose **ADD IT**.</span></span> <span data-ttu-id="b3112-414">[Project Web App] QuickStatus アプリが実行できる操作の一覧を示すダイアログボックスが表示されます (図12を参照)。</span><span class="sxs-lookup"><span data-stu-id="b3112-414">Project Web App displays a dialog box that lists the operations that the QuickStatus app can perform (see Figure 12).</span></span> <span data-ttu-id="b3112-415">操作の一覧は、Appmanifest.xml ファイルの**Apppermissionrequest**要素から派生します。</span><span class="sxs-lookup"><span data-stu-id="b3112-415">The list of operations is derived from the **AppPermissionRequest** elements in the AppManifest.xml file.</span></span> 
    
    <span data-ttu-id="b3112-416">**図12クイック進捗アプリを信頼するかどうかを確認する**</span><span class="sxs-lookup"><span data-stu-id="b3112-416">**Figure 12. Verifying that you trust the Quick Status app**</span></span>

    <span data-ttu-id="b3112-417">![QuickStatus アプリの信頼の検証](media/pj15_CreateStatusingApp_AddAppToPWA2Trust.gif "QuickStatus アプリの信頼の検証")</span><span class="sxs-lookup"><span data-stu-id="b3112-417">![Verifying trust for the QuickStatus app](media/pj15_CreateStatusingApp_AddAppToPWA2Trust.gif "Verifying trust for the QuickStatus app")</span></span>
  
11. <span data-ttu-id="b3112-418">[**実行するクイック状態の更新**] ダイアログボックスで、[**信頼**する] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3112-418">In the **Do you trust Quick Status Update** dialog box, choose **Trust It**.</span></span> <span data-ttu-id="b3112-419">[Project Web App サイトコンテンツ] ページにアプリが追加されます (図13を参照)。</span><span class="sxs-lookup"><span data-stu-id="b3112-419">The app is added to the Project Web App Site Contents page (see Figure 13).</span></span>
    
    <span data-ttu-id="b3112-420">**図13[サイトコンテンツ] ページでクイック進捗アプリを表示する**</span><span class="sxs-lookup"><span data-stu-id="b3112-420">**Figure 13. Viewing the Quick Status app on the Site Contents page**</span></span>

    <span data-ttu-id="b3112-421">![サイトコンテンツで QuickStatus アプリを表示する](media/pj15_CreateStatusingApp_AddAppToPWA3.gif "サイトコンテンツで QuickStatus アプリを表示する")</span><span class="sxs-lookup"><span data-stu-id="b3112-421">![Viewing the QuickStatus app in Site Contents](media/pj15_CreateStatusingApp_AddAppToPWA3.gif "Viewing the QuickStatus app in Site Contents")</span></span>
  
<span data-ttu-id="b3112-422">[サイトコンテンツ] ページで、[**クイック進捗状況の更新**] アイコンを選択してアプリを実行できます。</span><span class="sxs-lookup"><span data-stu-id="b3112-422">On the Site Contents page, you can select the **Quick Status Update** icon to run the app.</span></span>

> [!NOTE]
> <span data-ttu-id="b3112-423">アプリに関する情報を提供するその他のコマンドについては、[サイトコンテンツ] ページで、**クイック進捗の更新**名と省略記号 (...) を含む地域を選択します。アプリの [概要] ページで、アプリのエラーに関する情報が含まれているアプリの詳細ページを表示したり、[アプリの権限] ページを確認したり、Project Web App からアプリを削除したりできます。</span><span class="sxs-lookup"><span data-stu-id="b3112-423">For additional commands that provide information about the app, on the Site Contents page, choose the region that contains the **Quick Status Update** name and the ellipsis (...). You can review the About page for the app, view the App Details page that contains information about app errors, review the app permissions page, or remove the app from Project Web App.</span></span> 
  
<span data-ttu-id="b3112-424">Project Web App の [タスク] ページ (図14を参照) で、リボンの [**クイック状態**] ボタンを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3112-424">On the Tasks page in Project Web App (see Figure 14), the **QuickStatus** button should be enabled on the ribbon.</span></span> <span data-ttu-id="b3112-425">[**クイック状態**] ボタンが無効になっている場合は、図7のメモに記載されている操作を試してみてください。</span><span class="sxs-lookup"><span data-stu-id="b3112-425">If the **Quick Status** button is disabled, try the actions described in the note for Figure 7.</span></span> 

<span data-ttu-id="b3112-426">**図14[タスク] タブから QuickStatus アプリを開始する**</span><span class="sxs-lookup"><span data-stu-id="b3112-426">**Figure 14. Starting the QuickStatus app from the TASKS tab**</span></span>

<span data-ttu-id="b3112-427">![[タスク] タブから QuickStatus アプリを開始]する(media/pj15_CreateStatusingApp_TasksRibbon.gif "[タスク] タブから QuickStatus アプリを開始")する</span><span class="sxs-lookup"><span data-stu-id="b3112-427">![Starting the QuickStatus app from the TASKS tab](media/pj15_CreateStatusingApp_TasksRibbon.gif "Starting the QuickStatus app from the TASKS tab")</span></span>
  
<span data-ttu-id="b3112-428">手順6は、QuickStatus アプリで実行するいくつかのテストを示しています。</span><span class="sxs-lookup"><span data-stu-id="b3112-428">Procedure 6 shows some tests to make with the QuickStatus app.</span></span>

<span data-ttu-id="b3112-429"><a name="pj15_StatusingApp_Testing"> </a></span><span class="sxs-lookup"><span data-stu-id="b3112-429"></span></span>

## <a name="testing-the-quickstatus-app"></a><span data-ttu-id="b3112-430">QuickStatus アプリのテスト</span><span class="sxs-lookup"><span data-stu-id="b3112-430">Testing the QuickStatus app</span></span>

<span data-ttu-id="b3112-431">ユーザーが**Quickstatus**アプリで試行するすべての操作は、アプリケーションを運用サーバーに展開する前に、または project Online の運用テナントにテストする前に、project Server のテストインストールでテストする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3112-431">Every operation that a user might try in the **QuickStatus** app should be tested on a test installation of Project Server before deploying the app to a production server or to a production tenant of Project Online.</span></span> <span data-ttu-id="b3112-432">テストインストールでは、実際のプロジェクトに影響を与えずに、ユーザーの割り当てを変更および削除できます。</span><span class="sxs-lookup"><span data-stu-id="b3112-432">A test installation enables you to change and delete assignments for users without affecting actual projects.</span></span> <span data-ttu-id="b3112-433">また、テストには、管理者、プロジェクトマネージャー、チームメンバーなど、さまざまなアクセス許可のセットを持つ複数のユーザーが関与する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3112-433">Testing should also involve several users who have different sets of permissions, such as administrator, project manager, and team member.</span></span> <span data-ttu-id="b3112-434">完全なテストでは、アプリで行わなければならない変更を確認することができます。これは、開発中にテストされていませんでした。</span><span class="sxs-lookup"><span data-stu-id="b3112-434">Thorough testing can uncover changes that should be made in the app, which were not apparent in testing during development.</span></span> <span data-ttu-id="b3112-435">手順6では、 **Quickstatus**アプリのいくつかのテストを示していますが、一連のテストは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="b3112-435">Procedure 6 lists several tests for the **QuickStatus** app, but does not include an exhaustive series of tests.</span></span> 
  
### <a name="procedure-6-to-test-the-quickstatus-app"></a><span data-ttu-id="b3112-436">手順 6.</span><span class="sxs-lookup"><span data-stu-id="b3112-436">Procedure 6.</span></span> <span data-ttu-id="b3112-437">QuickStatus アプリをテストするには</span><span class="sxs-lookup"><span data-stu-id="b3112-437">To test the QuickStatus app</span></span>

1. <span data-ttu-id="b3112-438">ユーザーに割り当てられていない**Quickstatus**アプリを実行します。</span><span class="sxs-lookup"><span data-stu-id="b3112-438">Run the **QuickStatus** app where the user has no assignments.</span></span> <span data-ttu-id="b3112-439">アプリは、ページの下部に青色のメッセージを表示する必要があります。たとえば、**ユーザー名には割り当て**られていません。</span><span class="sxs-lookup"><span data-stu-id="b3112-439">The app should show a blue message at the bottom of the page, for example, **User Name has no assignments**.</span></span>
    
   <span data-ttu-id="b3112-440">[**更新**] を選択すると、緑色の割り当てに対するメッセージの変更**が更新されまし**た。</span><span class="sxs-lookup"><span data-stu-id="b3112-440">Choose **Update**, and the message changes to a green **Assignments have been updated**.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="b3112-441">割り当てがない場合に [**更新**] ボタンが無効になるように、アプリの動作を変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3112-441">The app behavior should be changed so that the **Update** button is disabled when there are no assignments.</span></span> 
  
2. <span data-ttu-id="b3112-442">複数の異なるプロジェクトにユーザーが複数の割り当てを行っていて、一部の割り当てが完了していない場合は、アプリを実行します。</span><span class="sxs-lookup"><span data-stu-id="b3112-442">Run the app where the user has multiple assignments in several different projects and some assignments are not complete.</span></span> <span data-ttu-id="b3112-443">アプリの外観を確認し、次のようにアクションを実行します (図15を参照)。</span><span class="sxs-lookup"><span data-stu-id="b3112-443">Notice the appearance of the app and perform actions as follows (see Figure 15):</span></span>
    
   1. <span data-ttu-id="b3112-444">**OnGetAssignmentsSuccess**関数は、現在のユーザーの割り当てごとに、テーブルに行を作成します。</span><span class="sxs-lookup"><span data-stu-id="b3112-444">The **onGetAssignmentsSuccess** function creates a row in the table for each assignment for the current user.</span></span> <span data-ttu-id="b3112-445">プロジェクト名には、各プロジェクトの最初の割り当てに対して1回だけ、太字のフォントで表示されます。</span><span class="sxs-lookup"><span data-stu-id="b3112-445">The project name shows only once, in a bold font, for the first assignment in each project.</span></span> 
    
   2. <span data-ttu-id="b3112-446">[**タスク名**] 列の見出しのチェックボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="b3112-446">Clear the check box in the **Task name** column header.</span></span> <span data-ttu-id="b3112-447">[テーブルヘッダー] click イベントハンドラーは、タスク行の他のすべてのチェックボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="b3112-447">The table header click event handler clears all of the other check boxes in the task rows.</span></span> 
    
   3. <span data-ttu-id="b3112-448">すべてのタスクを選択します。</span><span class="sxs-lookup"><span data-stu-id="b3112-448">Select all of the tasks.</span></span> <span data-ttu-id="b3112-449">各行の click イベントハンドラーは、すべての行が選択されているかどうかを判断し、その場合は、[**タスク名**] 列見出しを選択します。</span><span class="sxs-lookup"><span data-stu-id="b3112-449">The click event handler for each row determines whether all rows are selected, and if so, selects the **Task name** column header.</span></span> 
    
   4. <span data-ttu-id="b3112-450">再びすべてのチェックボックスをオフにし、残りの作業を行う1つの割り当てを選択します。</span><span class="sxs-lookup"><span data-stu-id="b3112-450">Clear all of the check boxes again, and then select one assignment that has some remaining work.</span></span> <span data-ttu-id="b3112-451">たとえば、図15は、T1 が 20% の残りの作業を完了したことを示しています。</span><span class="sxs-lookup"><span data-stu-id="b3112-451">For example, Figure 15 shows the top task T1 has 20% remaining work to complete.</span></span>
    
   5. <span data-ttu-id="b3112-452">[**達成率の設定**] テキストボックスに「80」と入力し、[**更新**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3112-452">In the **Set percent complete** text box, type 80, and then choose **Update**.</span></span> <span data-ttu-id="b3112-453">ページの下部に緑色のメッセージが表示され、**割り当てが更新されて**います。</span><span class="sxs-lookup"><span data-stu-id="b3112-453">The bottom of the page should show a green message, **Assignments have been updated**.</span></span>
    
      <span data-ttu-id="b3112-454">**図15QuickStatus アプリの割り当てを更新する**</span><span class="sxs-lookup"><span data-stu-id="b3112-454">**Figure 15. Updating an assignment in the QuickStatus app**</span></span>

      <span data-ttu-id="b3112-455">![QuickStatus アプリの割り当てを更新する](media/pj15_CreateStatusingApp_Testing1Update.gif "QuickStatus アプリの割り当てを更新する")</span><span class="sxs-lookup"><span data-stu-id="b3112-455">![Updating an assignment in the QuickStatus app](media/pj15_CreateStatusingApp_Testing1Update.gif "Updating an assignment in the QuickStatus app")</span></span>
  
3. <span data-ttu-id="b3112-456">[**更新**] を選択します (図16を参照)。</span><span class="sxs-lookup"><span data-stu-id="b3112-456">Choose **Refresh** (see Figure 16).</span></span> <span data-ttu-id="b3112-457">すべてのタスクが再度選択され、上部のタスクは 80% の完了を示します。</span><span class="sxs-lookup"><span data-stu-id="b3112-457">All of the tasks are selected again, and the top task shows 80% complete.</span></span> 
    
      <span data-ttu-id="b3112-458">**図16[クイック進捗状況の更新] ページの更新**</span><span class="sxs-lookup"><span data-stu-id="b3112-458">**Figure 16. Refreshing the Quick Status Update page**</span></span>

      <span data-ttu-id="b3112-459">![QuickStatus ページの更新](media/pj15_CreateStatusingApp_Testing2Refresh.gif "QuickStatus ページの更新")</span><span class="sxs-lookup"><span data-stu-id="b3112-459">![Refreshing the QuickStatus page](media/pj15_CreateStatusingApp_Testing2Refresh.gif "Refreshing the QuickStatus page")</span></span>
  
4. <span data-ttu-id="b3112-460">すべてのチェックボックスをオフにしてから、別のタスクを選択します。</span><span class="sxs-lookup"><span data-stu-id="b3112-460">Clear all of the check boxes, and then select another task.</span></span> <span data-ttu-id="b3112-461">たとえば、[新しいタスク] を [ **PWA から**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3112-461">For example, select **New task from PWA**.</span></span> <span data-ttu-id="b3112-462">[達成**率の設定**] テキストボックスは空のままにし\*\*\*\* 、選択したタスクの [達成率] 列のすべてのテキストを削除して、[**更新**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3112-462">Leave the **Set percent complete** text box empty, delete all text in the **% complete** column for the selected task, and then choose **Update**.</span></span> <span data-ttu-id="b3112-463">両方のテキストボックスが空であるため、アプリでは赤いエラーメッセージが表示されます (図17を参照)。</span><span class="sxs-lookup"><span data-stu-id="b3112-463">Because both text boxes are empty, the app shows a red error message (see Figure 17).</span></span>
    
      <span data-ttu-id="b3112-464">**図17エラーメッセージのテスト**</span><span class="sxs-lookup"><span data-stu-id="b3112-464">**Figure 17. Testing the error message**</span></span>

      <span data-ttu-id="b3112-465">![エラーメッセージのテスト](media/pj15_CreateStatusingApp_Testing3Error.gif "エラーメッセージのテスト")</span><span class="sxs-lookup"><span data-stu-id="b3112-465">![Testing the error message](media/pj15_CreateStatusingApp_Testing3Error.gif "Testing the error message")</span></span>
  
5. <span data-ttu-id="b3112-466">前のタスクを 80% 完了に更新してから、[**終了**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3112-466">Update the previous task to 80% complete, and then choose **Exit**.</span></span> <span data-ttu-id="b3112-467">**Exittopwa**関数は、ブラウザーウィンドウの場所を SharePoint ホストアプリケーションの [タスク] ページに変更します (つまり、URL https://ServerName/pwa/Tasks.aspx)はに変更されます)。</span><span class="sxs-lookup"><span data-stu-id="b3112-467">The **exitToPwa** function changes the browser window location to the Tasks page in the SharePoint host application (that is, the URL changes to https://ServerName/pwa/Tasks.aspx).</span></span> <span data-ttu-id="b3112-468">図18は、[ **T1**タスク] と [PWA タスク] の**新しいタスク**がそれぞれ 80% 完了したことを示しています。</span><span class="sxs-lookup"><span data-stu-id="b3112-468">Figure 18 shows that the **T1** task and the **New task from PWA** task each show 80% complete.</span></span> 
    
      <span data-ttu-id="b3112-469">**図18Project Web App でタスクが更新されたことを確認する**</span><span class="sxs-lookup"><span data-stu-id="b3112-469">**Figure 18. Verifying the tasks are updated in Project Web App**</span></span>

      <span data-ttu-id="b3112-470">![Project Web App で更新されたタスクを確認する](media/pj15_CreateStatusingApp_TasksUpdatedInPWA.gif "Project Web App で更新されたタスクを確認する")</span><span class="sxs-lookup"><span data-stu-id="b3112-470">![Verifying the updated tasks in Project Web App](media/pj15_CreateStatusingApp_TasksUpdatedInPWA.gif "Verifying the updated tasks in Project Web App")</span></span>
  
6. <span data-ttu-id="b3112-471">更新された状態が Project Professional 2013 に表示される前に、変更を承認のために提出し、プロジェクトマネージャーが承認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3112-471">Before the updated status shows in Project Professional 2013, the changes must be submitted for approval, and then approved by the project manager.</span></span>
    
<span data-ttu-id="b3112-472">テストでは、使いやすさを向上させるために**Quickstatus**アプリで行うべきその他のいくつかの変更が明らかになります。</span><span class="sxs-lookup"><span data-stu-id="b3112-472">Testing reveals several other changes that should be made in the **QuickStatus** app for improved usability.</span></span> <span data-ttu-id="b3112-473">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="b3112-473">For example:</span></span>

- <span data-ttu-id="b3112-474">エラーチェックとテキストボックス値の検証が追加されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3112-474">There should be additional error checks and validation of text box values.</span></span> <span data-ttu-id="b3112-475">現時点では、ユーザーは、達成率に数値以外の値または負の値を入力することができます。これにより、問題のないエラーメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b3112-475">Currently, a user can enter a non-numeric value or a negative value for percent complete, which results in an unfriendly error message.</span></span> <span data-ttu-id="b3112-476">たとえば、負の値を指定すると、エラーメッセージは割り当ての更新時にエラーになります。 **PJClientCallableException: StatusingSetDataValueInvalid**。</span><span class="sxs-lookup"><span data-stu-id="b3112-476">For example, with a negative value, the error message is **Error updating assignments: PJClientCallableException: StatusingSetDataValueInvalid**.</span></span>
    
- <span data-ttu-id="b3112-477">空白のテキストボックスに対するエラーメッセージには、行番号に加えて、プロジェクトとタスクを一覧表示することができます。</span><span class="sxs-lookup"><span data-stu-id="b3112-477">The error message for blank text boxes could list the project and task, in addition to the row number.</span></span>
    
- <span data-ttu-id="b3112-478">成功メッセージには、更新されたタスクのリストを含めることができます。または、 **Updateassignments**関数が成功した場合は、自動ページ更新を実行し、更新されたタスクまたはパーセンテージを別の色と太字のフォントで表示することができます。</span><span class="sxs-lookup"><span data-stu-id="b3112-478">The success message could include a list of the tasks updated; or if the **updateAssignments** function is successful, it could perform an automatic page refresh and show updated tasks or percentages in a different color and bold font.</span></span> 
    
- <span data-ttu-id="b3112-479">非常に大きなテーブルを使用しないようにするには、割り当てのテーブルを、達成率が 100% 未満のタスクに制限する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3112-479">To avoid a very large table, the table of assignments should be limited to tasks that are less than 100% complete.</span></span> <span data-ttu-id="b3112-480">または、すべてのタスクを表示するオプションを追加します。</span><span class="sxs-lookup"><span data-stu-id="b3112-480">Or, add an option to show all tasks.</span></span> <span data-ttu-id="b3112-481">この問題は、テーブルではなく、jQuery ベースのグリッドを使用して解決することができます。この場合、フィルター処理とグリッドページングを簡単に実装できます。</span><span class="sxs-lookup"><span data-stu-id="b3112-481">This problem could also be solved by using a jQuery-based grid instead of a table, where you can easily implement filtering and grid paging.</span></span>
    
- <span data-ttu-id="b3112-482">**Quickstatus**アプリは状態を送信しないため、リボンの [**タスク**] タブの [**クイック状態**] アイコンは、**送信**グループの最後のアイコンではなく、**タスク**グループの最初のアイコンになります。</span><span class="sxs-lookup"><span data-stu-id="b3112-482">Because the **QuickStatus** app does not submit status, the **Quick Status** icon on the **TASKS** tab of the ribbon would more logically be the first icon in the **Tasks** group, rather than the last icon in the **Submit** group.</span></span> 
    
- <span data-ttu-id="b3112-483">**OnGetAssignmentsSuccess**関数は**btnsubmitupdate**ボタンのテキストを初期化しますが、その他のボタンテキスト値は HTML で初期化されるので、 **getAssignments**の場合、ページは部分的に初期化された状態のままになります。関数が実行されます。</span><span class="sxs-lookup"><span data-stu-id="b3112-483">Because the **onGetAssignmentsSuccess** function initializes the **btnSubmitUpdate** button text, but the other button text values are initialized in HTML, the page is left in a partially initialized state while the **getAssignments** function runs.</span></span> <span data-ttu-id="b3112-484">HTML でテキスト値がすべて初期化されている場合、ページ上のボタンの一貫性が向上します。</span><span class="sxs-lookup"><span data-stu-id="b3112-484">Buttons on the page would appear more consistent if the text values were all initialized in HTML.</span></span> 
    
<span data-ttu-id="b3112-485">最も重要なことは、 **Quickstatus**アプリが使用するアプローチで、割り当ての達成率が変更された場合は、運用アプリで修正する必要があることです。</span><span class="sxs-lookup"><span data-stu-id="b3112-485">Most importantly, the approach that the **QuickStatus** app uses, where it changes percent complete for assignments, should be revised in a production app.</span></span> <span data-ttu-id="b3112-486">詳細については、「[次の手順](#pj15_StatusingApp_NextSteps)」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b3112-486">For more information, see the [Next steps](#pj15_StatusingApp_NextSteps) section.</span></span> 

<span data-ttu-id="b3112-487"><a name="pj15_StatusingApp_Example"> </a></span><span class="sxs-lookup"><span data-stu-id="b3112-487"></span></span>

## <a name="example-code-for-the-quickstatus-app"></a><span data-ttu-id="b3112-488">QuickStatus アプリのコード例</span><span class="sxs-lookup"><span data-stu-id="b3112-488">Example code for the QuickStatus app</span></span>

### <a name="defaultaspx-file"></a><span data-ttu-id="b3112-489">Default.aspx ファイルの既定値</span><span class="sxs-lookup"><span data-stu-id="b3112-489">Default.aspx file</span></span>

<span data-ttu-id="b3112-490">次のコードは、 `Pages\Default.aspx` **quickstatus**プロジェクトのファイルにあります。</span><span class="sxs-lookup"><span data-stu-id="b3112-490">The following code is in the  `Pages\Default.aspx` file of the **QuickStatus** project:</span></span> 
  
```HTML
    <%-- The following lines are ASP.NET directives needed when using SharePoint components --%>
    <%@ Page Inherits="Microsoft.SharePoint.WebPartPages.WebPartPage, Microsoft.SharePoint, Version=15.0.0.0, 
    Culture=neutral, PublicKeyToken=71e9bce111e9429c" MasterPageFile="~masterurl/default.master" Language="C#" %>
    <%@ Register TagPrefix="Utilities" Namespace="Microsoft.SharePoint.Utilities" Assembly="Microsoft.SharePoint, Version=15.0.0.0, 
    Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
    <%@ Register TagPrefix="WebPartPages" Namespace="Microsoft.SharePoint.WebPartPages" Assembly="Microsoft.SharePoint, Version=15.0.0.0, 
    Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
    <%@ Register TagPrefix="SharePoint" Namespace="Microsoft.SharePoint.WebControls" Assembly="Microsoft.SharePoint, Version=15.0.0.0, 
    Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
    <%-- The markup and script in the following Content element will be placed in the <head> of the page.
        For production deployment, change the .debug.js JavaScript references to .js. --%>
    <asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead" runat="server">
    <script type="text/javascript" src="../Scripts/jquery-1.7.1.min.js"></script>
    <script type="text/javascript" src="/_layouts/15/sp.runtime.debug.js"></script>
    <script type="text/javascript" src="/_layouts/15/sp.debug.js"></script>
    <script type="text/javascript" src="/_layouts/15/ps.debug.js"></script>
    <!-- CSS styles -->
    <link rel="Stylesheet" type="text/css" href="../Content/App.css" />
    <!-- Add your JavaScript to the following file -->
    <script type="text/javascript" src="../Scripts/App.js"></script>
    </asp:Content>
    <%-- The markup and script in the following Content element will be placed in the <body> of the page --%>
    <asp:Content ContentPlaceHolderID="PlaceHolderMain" runat="server">
    <form>
        <fieldset>
        <legend>Select assigned tasks</legend>
        <table id="assignmentsTable">
            <caption id="tableCaption">Replace caption</caption>
            <thead>
            <tr id="headerRow">
                <th>Project name</th>
                <th><input type="checkbox" id="headercheckbox" checked="checked" />Task name</th>
                <th>Actual work</th>
                <th>% complete</th>
                <th>Remaining work</th>
                <th>Due date</th>
            </tr>
            </thead>
        </table>
        </fieldset>
        <div id="inputPercentComplete" >
        Set percent complete for all selected assignments, or leave this
        <br /> field blank and set percent complete for individual assignments: 
        <input type="text" name="percentComplete" id="pctComplete" size="4"  maxlength="4" />
        </div>
        <div id="submitResult">
        <p><button id="btnSubmitUpdate" type="button" class="bottomButtons" ></button></p>
        <p id="message"></p>
        </div>
        <div id="refreshPage">
        <p><button id="btnRefresh" type="button" class="bottomButtons" >Refresh</button></p>
        </div>
    <div id="exitPage">
        <p><button id="btnExit" type="button" class="bottomButtons" >Exit</button></p>
    </div>
    </form>
    </asp:Content>
```

<br/>

### <a name="appjs-file"></a><span data-ttu-id="b3112-491">アプリケーション .js ファイル</span><span class="sxs-lookup"><span data-stu-id="b3112-491">App.js file</span></span>

<span data-ttu-id="b3112-492">次のコードは、 `Scripts\App.js` **quickstatus**プロジェクトのファイルにあります。</span><span class="sxs-lookup"><span data-stu-id="b3112-492">The following code is in the  `Scripts\App.js` file of the **QuickStatus** project:</span></span> 
  
```js
    var projContext;
    var pwaWeb;
    var projUser;
    // This code runs when the DOM is ready and creates a ProjectContext object.
    // The ProjectContext object is required to use the JSOM for Project Server.
    $(document).ready(function () {
        projContext = PS.ProjectContext.get_current();
        pwaWeb = projContext.get_web();
        getUserInfo();
        getAssignments();
        // Bind a click event handler to the table header check box, which sets the row check boxes
        // to the selected state of the header check box, and sets the results message to an empty string.
        $('#headercheckbox').live('click', function (event) {
            $('input:checkbox:not(#headercheckbox)').attr('checked', this.checked);
            $get("message").innerText = "";
        });
        // Bind a click event handler to the row check boxes. If any row check box is cleared, clear
        // the header check box. If all of the row check boxes are selected, select the header check box.
        $('input:checkbox:not(#headercheckbox)').live('click', function (event) {
            var isChecked = true;
            $('input:checkbox:not(#headercheckbox)').each(function () {
                if (this.checked == false) isChecked = false;
                $get("message").innerText = "";
            });
            $("#headercheckbox").attr('checked', isChecked);
        });
    });
    // Get information about the current user.
    function getUserInfo() {
        projUser = pwaWeb.get_currentUser();
        projContext.load(projUser);
        projContext.executeQueryAsync(onGetUserNameSuccess,
            // Anonymous function to execute if getUserInfo fails.
            function (sender, args) {
                alert('Failed to get user name. Error: ' + args.get_message());
        });
    }
    // This function is executed if the getUserInfo call is successful.
    // Replace the contents of the 'caption' paragraph with the project user name.
    function onGetUserNameSuccess() {
        var prefaceInfo = 'Assignments for ' + projUser.get_title();
        $('#tableCaption').text(prefaceInfo);
    }
    // Get the collection of assignments for the current user.
    function getAssignments() {
        assignments = PS.EnterpriseResource.getSelf(projContext).get_assignments();
        // Register the request that you want to run on the server. The optional "Include" parameter 
        // requests only the specified properties for each assignment in the collection.
        projContext.load(assignments,
            'Include(Project, Name, ActualWork, ActualWorkMilliseconds, PercentComplete, RemainingWork, Finish, Task)');
        // Run the request on the server.
        projContext.executeQueryAsync(onGetAssignmentsSuccess,
            // Anonymous function to execute if getAssignments fails.
            function (sender, args) {
                alert('Failed to get assignments. Error: ' + args.get_message());
            });
    }
    // Get the enumerator, iterate through the assignment collection, 
    // and add each assignment to the table.
    function onGetAssignmentsSuccess(sender, args) {
        if (assignments.get_count() > 0) {
            var assignmentsEnumerator = assignments.getEnumerator();
            var projName = "";
            var prevProjName = "3D2A8045-4920-4B31-B3E7-9D0C5195FC70"; // Any unique name.
            var taskNum = 0;
            var chkTask = "";
            var txtPctComplete = "";
            // Constants for creating input controls in the table.
            var INPUTCHK = '<input type="checkbox" class="chkTask" checked="checked" id="chk';
            var LBLCHK = '<label for="chk';
            var INPUTTXT = '<input type="text" size="4"  maxlength="4" class="txtPctComplete" id="txt';
            while (assignmentsEnumerator.moveNext()) {
                var statusAssignment = assignmentsEnumerator.get_current();
                projName = statusAssignment.get_project().get_name();
                // Get an integer value for the number of milliseconds of actual work, such as 3600000.
                var actualWorkMilliseconds = statusAssignment.get_actualWorkMilliseconds();
                // Get a string value for the assignment actual work, such as "1h". Not used here.
                var actualWork = statusAssignment.get_actualWork();                         
                if (projName === prevProjName) {
                    projName = "";
                }
                prevProjName = statusAssignment.get_project().get_name();
                // Create a row for the assignment information.
                var row = assignmentsTable.insertRow();
                taskNum++;
                // Create an HTML string with a check box and task name label, for example:
                //     <input type="checkbox" class="chkTask" checked="checked" id="chk1" /> 
                //     <label for="chk1">Task 1</label>
                chkTask = INPUTCHK + taskNum + '" /> ' + LBLCHK + taskNum + '">'
                    + statusAssignment.get_name() + '</label>';
                txtPctComplete = INPUTTXT + taskNum + '" />';
                // Insert cells for the assignment properties.
                row.insertCell().innerHTML = '<strong>' + projName + '</strong>';
                row.insertCell().innerHTML = chkTask;
                row.insertCell().innerText = actualWorkMilliseconds / 3600000 + 'h';
                row.insertCell().innerHTML = txtPctComplete;
                row.insertCell().innerText = statusAssignment.get_remainingWork();
                row.insertCell().innerText = statusAssignment.get_finish();
                // Initialize the percent complete cell.
                $get("txt" + taskNum).innerText = statusAssignment.get_percentComplete() + '%'
            }
        }
        else {
            $('p#message').attr('style', 'color: #0f3fdb');     // Blue text.
            $get("message").innerText = projUser.get_title() + ' has no assignments'
        }
        // Initialize the button properties.
        $get("btnSubmitUpdate").onclick = function() { updateAssignments(); };
        $get("btnSubmitUpdate").innerText = 'Update';
        $get('btnRefresh').onclick = function () { window.location.reload(true); };
        $get('btnExit').onclick = function () { exitToPwa(); };
    }
    // Update all selected assignments. If the bottom percent complete field is blank,
    // use the value in the % complete field of each selected row in the table.
    function updateAssignments() {
        // Get percent complete from the bottom text box.
        var pctCompleteMain = getNumericValue($('#pctComplete').val()).trim();
        var pctComplete = pctCompleteMain;
        var assignmentsEnumerator = assignments.getEnumerator();
        var taskNum = 0;
        var taskRow = "";
        var indexPercent = "";
        var doSubmit = true;
        while (assignmentsEnumerator.moveNext()) {
            var pctCompleteRow = "";
            taskRow = "chk" + ++taskNum;
            if ($get(taskRow).checked) {
                var statusAssignment = assignmentsEnumerator.get_current();
                if (pctCompleteMain === "") {
                    // Get percent complete from the text box field in the table row.
                    pctCompleteRow = getNumericValue($('#txt' + taskNum).val());
                    pctComplete = pctCompleteRow;
                }
                // If both percent complete fields are empty, show an error.
                if (pctCompleteMain === "" && pctCompleteRow === "") {
                    $('p#message').attr('style', 'color: #e11500');     // Red text.
                    $get("message").innerHTML =
                        '<b>Error:</b> Both <i>Percent complete</i> fields are empty, in row '
                        + taskNum
                        + ' and in the bottom textbox.<br/>One of those fields must have a valid percent.'
                        + '<p>Please refresh the page and try again.</p>';
                    doSubmit = false;
                    taskNum = 0;
                    break;
                }
                if (doSubmit) statusAssignment.set_percentComplete(pctComplete);
            }
        } 
        // Save and submit the assignment updates.
        if (doSubmit) {
            assignments.update();
            assignments.submitAllStatusUpdates();
            projContext.executeQueryAsync(function (source, args) {
                $('p#message').attr('style', 'color: #0faa0d');     // Green text.
                $get("message").innerText = 'Assignments have been updated.';
            }, function (source, args) {
                $('p#message').attr('style', 'color: #e11500');     // Red text.
                $get("message").innerText = 'Error updating assignments: ' + args.get_message();
            });
        }
    }
    // Get the numeric part for percent complete, from a string. 
    // For example, with "20 %", return "20".
    function getNumericValue(pctComplete) {
        pctComplete = pctComplete.trim();
        pctComplete = pctComplete.replace(/ /g, "");    // Remove interior spaces.
        indexPercent = pctComplete.indexOf('%', 0);
        if (indexPercent > -1) pctComplete = pctComplete.substring(0, indexPercent);
        return pctComplete;
    }
    // Exit the QuickStatus page and go back to the Tasks page in Project Web App.
    function exitToPwa() {
        // Get the SharePoint host URL, which is the top page of PWA, and add the Tasks page.
        var spHostUrl = decodeURIComponent(getQueryStringParameter('SPHostUrl'))
                        + "/Tasks.aspx";
        // Set the top window for the QuickStatus IFrame to the Tasks page.
        window.top.location.href = spHostUrl;
    }
    // Get a specified query string parameter from the {StandardTokens} URL option string.
    function getQueryStringParameter(urlParameterKey) {
        var docUrl = document.URL;
        var params = docUrl.split('?')[1].split('&');
        for (var i = 0; i < params.length; i++) {
            var theParam = params[i].split('=');
            if (theParam[0] == urlParameterKey)
                return decodeURIComponent(theParam[1]);
        }
    }
```

<br/>

### <a name="appcss-file"></a><span data-ttu-id="b3112-493">App.css ファイル</span><span class="sxs-lookup"><span data-stu-id="b3112-493">App.css file</span></span>

<span data-ttu-id="b3112-494">次の CSS コードは、 `Content\App.css` **quickstatus**プロジェクトのファイルにあります。</span><span class="sxs-lookup"><span data-stu-id="b3112-494">The following CSS code is in the  `Content\App.css` file of the **QuickStatus** project:</span></span> 
  
```css
    /* Custom styles for the QuickStatus app. */
    /*============= Table elements ========================================*/
    table {
        width: 90%;
    }
    caption {
        font-size: 16px;
        padding-bottom: 5px;
        font-weight: bold;
        color: gray;
    }
    table th {
        background-color: gray;
        color: white;
    }
    table td, th {
        width: auto;
        text-align: left;
        padding: 2px;
        border: solid 1px whitesmoke;
        color: gray;
    }
    /*=== Class for check boxes added to rows 
    */
    .chkTask {
        width: 12px;
        height: 12px;
        color: gray;
    }
    /*========== DIV id for the Percent Complete text box ================*/
    #inputPercentComplete {
        position: fixed;
        top: auto;
        height: auto;
        padding-top: 20px;
        margin-left: 30px;
    }
    /*========== DIV id for the Submit Result button ====================*/
    #submitResult {
        position: fixed;
        top: auto;
        height: auto;
        padding-top: 60px;
    }
    /*========== DIV id for the Refresh Page button ====================*/
    #refreshPage {
        position: fixed;
        top: auto;
        height: auto;
        padding-top: 60px;
        margin-left: 120px;
    }
    /*========== DIV id for the Exit Page button ====================*/
    #exitPage {
        position: fixed;
        top: auto;
        height: auto;
        padding-top: 60px;
        margin-left: 240px;
    }
    /*========== Class for the buttons at the bottom of the page =======*/
    .bottomButtons {
        color: gray;
        font-weight: bold; 
        font-size: 12px; 
        border-color: darkgreen;
        border-width: thin;
    }
```

<br/>

### <a name="elementsxml-file-for-the-ribbon"></a><span data-ttu-id="b3112-495">リボンの要素 .xml ファイル</span><span class="sxs-lookup"><span data-stu-id="b3112-495">Elements.xml file for the ribbon</span></span>

<span data-ttu-id="b3112-496">次の XML 定義は、リボンの [**タスク**] タブの [追加] ボタンに対して`RibbonQuickStatusAction\Elements.xml` 、 **quickstatus**プロジェクトのファイル内にあります。</span><span class="sxs-lookup"><span data-stu-id="b3112-496">The following XML definition, for the added button on the **TASKS** tab on the ribbon, is in the  `RibbonQuickStatusAction\Elements.xml` file of the **QuickStatus** project:</span></span> 
  
```XML
    <?xml version="1.0" encoding="utf-8"?>
    <Elements xmlns="http://schemas.microsoft.com/sharepoint/">
    <CustomAction Id="21ea3aaf-79e5-4aac-9479-8eef14b4d9df.RibbonQuickStatusAction"
                    Location="CommandUI.Ribbon">
        <CommandUIExtension>
        <!-- 
        Add a button that invokes the QuickStatus app. The Quick Status button is displayed as  
        the third control in the Page group (the group title is "Submit").
        -->
        <CommandUIDefinitions>
            <CommandUIDefinition Location="Ribbon.ContextualTabs.MyWork.Home.Page.Controls._children">
            <Button Id="Ribbon.ContextualTabs.MyWork.Home.Page.QuickStatus"
                    Alt="Quick Status app"
                    Sequence="30"
                    Command="Invokae_QuickStatus"
                    LabelText="Quick Status"
                    TemplateAlias="o1"
                    Image16by16="_layouts/15/1033/images/ps16x16.png" 
                    Image16by16Left="-80"
                    Image16by16Top="-144"
                    Image32by32="_layouts/15/1033/images/ps32x32.png" 
                    Image32by32Left="-32"
                    Image32by32Top="-288" 
                    ToolTipTitle="Quick Status"
                    ToolTipDescription="Run the QuickStatus app" />
            </CommandUIDefinition>
        </CommandUIDefinitions>
        <CommandUIHandlers>
            <CommandUIHandler Command="Invoke_QuickStatus"
                            CommandAction="~appWebUrl/Pages/Default.aspx?{StandardTokens}"/>
        </CommandUIHandlers>
        </CommandUIExtension >
    </CustomAction>
    </Elements>
```

<br/>

### <a name="appmanifestxml-file"></a><span data-ttu-id="b3112-497">AppManifest.xml ファイル</span><span class="sxs-lookup"><span data-stu-id="b3112-497">AppManifest.xml file</span></span>

<span data-ttu-id="b3112-498">次に示すのは、 **Quickstatus**プロジェクトのアプリマニフェスト用の XML で、これには、アプリユーザーの割り当て状態を複数のプロジェクトで更新するために必要な2つのアクセス許可要求スコープが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b3112-498">Following is the XML for the app manifest of the **QuickStatus** project, which includes the two permission request scopes that are necessary for updating the app user's assignment status in multiple projects:</span></span> 
  
```XML
    <?xml version="1.0" encoding="utf-8" ?>
    <!--Created:cb85b80c-f585-40ff-8bfc-12ff4d0e34a9-->
    <App xmlns="http://schemas.microsoft.com/sharepoint/2012/app/manifest"
        Name="QuickStatus"
        ProductID="{bbc497e7-1221-4d7b-a0ae-141a99546008}"
        Version="1.0.0.0"
        SharePointMinVersion="15.0.0.0"
    >
    <Properties>
        <Title>Quick Status Update</Title>
        <StartPage>~appWebUrl/Pages/Default.aspx?{StandardTokens}</StartPage>
    </Properties>
    <AppPrincipal>
        <Internal />
    </AppPrincipal>
    <AppPermissionRequests>
        <AppPermissionRequest Scope="https://sharepoint/projectserver/statusing" Right="SubmitStatus" />
        <AppPermissionRequest Scope="https://sharepoint/projectserver/projects" Right="Read" />
    </AppPermissionRequests>
    </App>
```

<br/>

### <a name="appiconpng-file"></a><span data-ttu-id="b3112-499">AppIcon ファイル</span><span class="sxs-lookup"><span data-stu-id="b3112-499">AppIcon.png file</span></span>

<span data-ttu-id="b3112-500">**Quickstatus**アプリの完全な Visual Studio ソリューションには、カスタムの AppIcon ファイルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b3112-500">The complete Visual Studio solution for the **QuickStatus** app includes a custom AppIcon.png file.</span></span> <span data-ttu-id="b3112-501">ソリューションは、Project 2013 SDK のダウンロードに含まれます。</span><span class="sxs-lookup"><span data-stu-id="b3112-501">The solution will be included in the Project 2013 SDK download.</span></span> 

<span data-ttu-id="b3112-502"><a name="pj15_StatusingApp_NextSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="b3112-502"></span></span>

## <a name="next-steps"></a><span data-ttu-id="b3112-503">次の手順</span><span class="sxs-lookup"><span data-stu-id="b3112-503">Next steps</span></span>

<span data-ttu-id="b3112-504">**Quickstatus**アプリは、project Server 2013 および project Online にインストールできるアプリの作成方法を示す比較的簡単な例です。</span><span class="sxs-lookup"><span data-stu-id="b3112-504">The **QuickStatus** app is a relatively simple example of how to write apps that can be installed on Project Server 2013 and Project Online.</span></span> <span data-ttu-id="b3112-505">「 [QuickStatus app のテスト](#pj15_StatusingApp_Testing)」セクションでは、利便性向上のために行うことができるいくつかの改良点を示します。</span><span class="sxs-lookup"><span data-stu-id="b3112-505">The [Testing the QuickStatus app](#pj15_StatusingApp_Testing) section lists several improvements that can be made for better usability.</span></span> <span data-ttu-id="b3112-506">**Quickstatus**アプリは、JavaScript 関数を使用して Project Web app の割り当て状態を更新します。</span><span class="sxs-lookup"><span data-stu-id="b3112-506">The **QuickStatus** app uses JavaScript functions to update assignment status for Project Web App.</span></span> <span data-ttu-id="b3112-507">しかし、割り当ての達成率を変更することは、推奨されるプロジェクト管理手法ではありません。</span><span class="sxs-lookup"><span data-stu-id="b3112-507">But, changing the assignment percent complete is not a recommended project management practice.</span></span> <span data-ttu-id="b3112-508">別の方法として、割り当てられたタスクの実績開始日と残存期間を更新することもできます。</span><span class="sxs-lookup"><span data-stu-id="b3112-508">Another approach would be to update the actual start date and remaining duration of assigned tasks.</span></span> <span data-ttu-id="b3112-509">この問題の詳細については、「MPUG ニュースレターの[更新プログラムの向上](https://www.mpug.com/articles/update-better)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b3112-509">For a discussion of the issues, see [Update Better](https://www.mpug.com/articles/update-better) in the MPUG newsletter.</span></span> 

<span data-ttu-id="b3112-510"><a name="pj15_StatusingApp_AdditionalResources"> </a></span><span class="sxs-lookup"><span data-stu-id="b3112-510"></span></span>

## <a name="see-also"></a><span data-ttu-id="b3112-511">関連項目</span><span class="sxs-lookup"><span data-stu-id="b3112-511">See also</span></span>

- [<span data-ttu-id="b3112-512">Project Server のプログラミング タスク</span><span class="sxs-lookup"><span data-stu-id="b3112-512">Project Server programming tasks</span></span>](project-programming-tasks.md)
- [<span data-ttu-id="b3112-513">SharePoint アドイン</span><span class="sxs-lookup"><span data-stu-id="b3112-513">SharePoint Add-ins</span></span>](https://msdn.microsoft.com/library/jj163230.aspx)
- [<span data-ttu-id="b3112-514">Project Web App でタスク更新を管理する</span><span class="sxs-lookup"><span data-stu-id="b3112-514">Managing task updates in Project Web App</span></span>](https://technet.microsoft.com/en-us/library/hh767481%28v=office.14%29.aspx)
- [<span data-ttu-id="b3112-515">カスタム アクションを作成して、SharePoint アドインで展開する</span><span class="sxs-lookup"><span data-stu-id="b3112-515">Create custom actions to deploy with SharePoint Add-ins</span></span>](https://msdn.microsoft.com/library/jj163954.aspx)
    

