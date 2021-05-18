---
title: JavaScript オブジェクト Project Online (JSOM) を使用したアドインの開発
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4a4b1ad2-de46-421d-a698-53c20c90b93a
description: この記事では、Microsoft Project Onlineのエクスペリエンスを向上させるアドイン開発のProject Online。 開発プロジェクトは、チュートリアルとして実装されます。 この記事で使用するアドインは、Project Online アカウントから発行されたプロジェクトのプロジェクト名と ID を読み取って表示し、個々のプロジェクトに関連付けられたタスクを取得するためにドリルダウンできます。
ms.openlocfilehash: 0a472a6300f18aaa65649f44d944445642a59e1a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322691"
---
# <a name="developing-a-project-online-add-in-using-the-javascript-object-model-jsom"></a><span data-ttu-id="4e0e4-105">JavaScript オブジェクト Project Online (JSOM) を使用したアドインの開発</span><span class="sxs-lookup"><span data-stu-id="4e0e4-105">Developing a Project Online add-in using the JavaScript Object Model (JSOM)</span></span>

<span data-ttu-id="4e0e4-106">この記事では、Microsoft Project Onlineのエクスペリエンスを向上させるアドイン開発のProject Online。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-106">This article describes Microsoft Project Online Add-in development to enhance your experience with the Project Online.</span></span> <span data-ttu-id="4e0e4-107">開発プロジェクトは、チュートリアルとして実装されます。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-107">The development project is implemented as a walkthrough.</span></span> <span data-ttu-id="4e0e4-108">この記事で使用するアドインは、Project Online アカウントから発行されたプロジェクトのプロジェクト名と ID を読み取って表示し、個々のプロジェクトに関連付けられたタスクを取得するためにドリルダウンできます。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-108">The add-in used for this article reads and displays the project names and IDs of the published projects from your Project Online account and allows you to drill down to retrieve tasks associated with individual projects.</span></span>
  
<span data-ttu-id="4e0e4-109">実行時に、アドインの一覧は次の図のようになります。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-109">At run time, the add-in listing looks similar to the following illustration:</span></span>
  
<span data-ttu-id="4e0e4-110">![JSOM プロジェクトとタスクの一]覧を示すスクリーン ショット JSOM プロジェクトとタスクの一覧(media/766e5914-f048-48f4-9282-291f55e6e90d.png "を示す")スクリーン ショット</span><span class="sxs-lookup"><span data-stu-id="4e0e4-110">![Screen shot showing a listing of JSOM projects and tasks](media/766e5914-f048-48f4-9282-291f55e6e90d.png "Screen shot showing a listing of JSOM projects and tasks")</span></span>
  
<span data-ttu-id="4e0e4-111">この例の焦点は、Project Online要求ごとにクエリを行い、コンテキストを設定する方法です。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-111">The focus of the example is the interaction with the Project Online, making queries and setting the context for each request from the service.</span></span> <span data-ttu-id="4e0e4-112">ユーザー インターフェイス (UI) 要素は、最小限の注意を受け取る。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-112">User interface (UI) elements receive minimal attention.</span></span> <span data-ttu-id="4e0e4-113">代わりに、ソースリストには UI に関するコメントが表示されます。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-113">Instead, the source listings provide comments regarding the UI.</span></span>
  
> [!NOTE]
> <span data-ttu-id="4e0e4-114">アドインの例のソース ファイル (プロジェクトVisual Studio次の場所で使用できます https://github.com/OfficeDev/Project-JSOM-List-Projects-Tasks.... 。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-114">The source files for the example add-in, a Visual Studio project, are available at: https://github.com/OfficeDev/Project-JSOM-List-Projects-Tasks.....</span></span> <span data-ttu-id="4e0e4-115">ソース ファイルは、記事の読み取り中に参照として便利な状態に保ちます。それぞれが他のファイルを補完します。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-115">Keep the source files handy as a reference while you read the article, as each complements the other.</span></span> <span data-ttu-id="4e0e4-116">Visual Studio プロジェクト ビルド内のファイルは、最小限の変更で実行可能です。Project Online テナントの URL を PWA フォルダーに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-116">The files in the Visual Studio project build and are executable with minimal changes—substituting the URL for your Project Online tenant down to the PWA folder.</span></span> 
  
## <a name="background"></a><span data-ttu-id="4e0e4-117">背景</span><span class="sxs-lookup"><span data-stu-id="4e0e4-117">Background</span></span>

<span data-ttu-id="4e0e4-118">Project Onlineは、Office 365 ポートフォリオ管理 (PPM) およびプロジェクト管理オフィス (PMO) ソリューションを企業に提供し、ポートフォリオ、プログラム、プロジェクトを調整および管理する Office 365 サービスです。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-118">Project Online is a Office 365 service that provides companies with a project portfolio management (PPM) and project management office (PMO) solution to coordinate and manage portfolios, programs, and projects.</span></span> <span data-ttu-id="4e0e4-119">Project Onlineデスクトップ エディションとは異なるProjectです。しかし、Project Onlineプロジェクトの一生を通じてプロジェクトの詳細を維持および追跡する機能がまだ含まれている場合があります。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-119">Project Online is a different offering than the Project desktop editions; yet, Project Online still contains the functionality to maintain and track project details throughout the life of a project.</span></span> <span data-ttu-id="4e0e4-120">Project OnlineはオンラインでSharePointされます。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-120">Project Online is built on SharePoint Online.</span></span>
  
<span data-ttu-id="4e0e4-121">ホストProject Onlineは、クライアント側オブジェクト モデル API と対話する JavaScript ファイルとリソース ファイルで構成されます。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-121">A Project Online hosted add-in consists of JavaScript and resource files that interact with the Client-Side-Object-Model API.</span></span> <span data-ttu-id="4e0e4-122">ユーザーがアドインにアクセスすると、JavaScript とリソースがダウンロードされ、ブラウザー内で実行されます。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-122">When the user visits the add-in, the JavaScript and resources are downloaded and executed within the browser.</span></span> <span data-ttu-id="4e0e4-123">アドインは、データの作成、取得、更新、または削除Project Online、サービスを操作するための非同期呼び出しを行います。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-123">The add-In makes asynchronous calls to Project Online to interact with the service, whether creating, retrieving, updating, or deleting data.</span></span> 
  
<span data-ttu-id="4e0e4-124">Project Online、アドインから他のテナントに属する情報を保護するためのもう 1 つのアクションを実行します。つまり、Project Onlineアドインからの要求を操作するための分離サイトを作成します。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-124">Project Online performs one more action to protect information that belongs to other tenants from the add-in; namely, Project Online creates an isolated site to interact with the requests from the add-in.</span></span> <span data-ttu-id="4e0e4-125">カスタム コードは、カスタム ホストProject Online実行します。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-125">No custom code runs on the Project Online host.</span></span> 
  
<span data-ttu-id="4e0e4-126">アドインの開発Project Onlineは、アドイン のプロジェクトVisual Studio SharePointを使用します。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-126">The development setup for Project Online add-ins uses the Visual Studio SharePoint Add-in project type.</span></span> <span data-ttu-id="4e0e4-127">アドインは JavaScript で記述され、Project JavaScript オブジェクト モデル (JSOM) を使用して、Project Online サービスを操作します。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-127">The add-in is written in JavaScript, and uses the Project JavaScript object model (JSOM) to interact with the Project Online service.</span></span> <span data-ttu-id="4e0e4-128">JSOM は、その機能の多くを JSOM のSharePointします。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-128">The JSOM inherits much of its functionality from the SharePoint JSOM.</span></span>
  
> [!NOTE]
> <span data-ttu-id="4e0e4-129">アドインは、Office ストアで公開および販売するか、SharePoint のプライベート アプリ カタログに展開できます。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-129">Add-ins can be published and sold in the Office Store or deployed to a private app catalog on SharePoint.</span></span> <span data-ttu-id="4e0e4-130">詳細については、「Deploy [and publish your Office アドイン」を参照してください](https://docs.microsoft.com/office/dev/add-ins/publish/publish)。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-130">For more information, see [Deploy and publish your Office Add-in](https://docs.microsoft.com/office/dev/add-ins/publish/publish).</span></span>
> 
> <span data-ttu-id="4e0e4-131">この記事で使用するアドインは、開発者向けのサンプルです。これは、実稼働環境での使用を目的としていない。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-131">The add-in used in this article is a sample for developers; it is not intended for use in a production environment.</span></span> <span data-ttu-id="4e0e4-132">主な目的は、アプリ開発の例を示Project Online。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-132">The primary purpose is to show an example of app development for Project Online.</span></span> 
  
## <a name="prerequisites"></a><span data-ttu-id="4e0e4-133">前提条件</span><span class="sxs-lookup"><span data-stu-id="4e0e4-133">Prerequisites</span></span>

<span data-ttu-id="4e0e4-134">サポートされている環境に次のWindowsします。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-134">Add the following items to a supported Windows environment:</span></span>
  
- <span data-ttu-id="4e0e4-135">**.NET Framework 4.0 以降**: バージョン 4.0 のフレームワークの完全なバージョンは互換性があります。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-135">**.NET Framework 4.0 or later**: Complete versions of the framework from version 4.0 are compatible.</span></span> <span data-ttu-id="4e0e4-136">ダウンロード サイトは https://msdn.microsoft.com/vstudio/aa496123.aspx です。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-136">The download site is https://msdn.microsoft.com/vstudio/aa496123.aspx.</span></span>
    
- <span data-ttu-id="4e0e4-137">**Visual Studio 2013以降**:</span><span class="sxs-lookup"><span data-stu-id="4e0e4-137">**Visual Studio 2013 or later**:</span></span>  
    
   - <span data-ttu-id="4e0e4-138">2015 年 2015 Visual Studioのプロフェッショナル エディションは、すぐに使用できる状態で利用可能です https://www.visualstudio.com/en-us/products/visual-studio-professional-with-msdn-vs.aspx 。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-138">The professional edition of Visual Studio 2015 is ready to go out-of-the box and is available at https://www.visualstudio.com/en-us/products/visual-studio-professional-with-msdn-vs.aspx.</span></span>
    
   - <span data-ttu-id="4e0e4-139">2015 年 2015 Visual Studioのコミュニティ エディションはで利用できます https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx 。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-139">The community edition of Visual Studio 2015 is available at https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx.</span></span> <span data-ttu-id="4e0e4-140">このエディションでは、開発者向けツールを手動Microsoft Officeインストールする必要Visual Studio。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-140">This edition requires manual installation of the Microsoft Office Developer Tools for Visual Studio.</span></span>
    
   <span data-ttu-id="4e0e4-141">[Microsoft Office開発者ツール] は、Visual Studioで利用できます https://www.visualstudio.com/en-us/features/office-tools-vs.aspx 。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-141">The Microsoft Office Developer Tools for Visual Studio are available at https://www.visualstudio.com/en-us/features/office-tools-vs.aspx.</span></span>
    
- <span data-ttu-id="4e0e4-142">**アカウントProject Online:** ホスティング サービスへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-142">**A Project Online account**: This provides access to the hosting service.</span></span> <span data-ttu-id="4e0e4-143">Project Online アカウントの入手の詳細については、https://products.office.com/en-us/Project/project-online-portfolio-management をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-143">For more information about obtaining a Project Online account, see https://products.office.com/en-us/Project/project-online-portfolio-management.</span></span>
    
   <span data-ttu-id="4e0e4-144">アドイン ユーザーが、テナント内の一部のプロジェクトにアクセスするための十分なProject Onlineします。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-144">Ensure that the add-in user has sufficient authorization to access some projects in the Project Online tenant.</span></span> 
    
- <span data-ttu-id="4e0e4-145">**情報が設定されたホスティング** サイト上のプロジェクト。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-145">**Projects on the hosting site** that are populated with information.</span></span>
    
> [!NOTE]
> <span data-ttu-id="4e0e4-146">標準の.NET Framework使用する正しいフレームワークです。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-146">The standard .NET Framework is the correct framework to use.</span></span> <span data-ttu-id="4e0e4-147">".NET Framework 4 クライアント プロファイル" を使用しない。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-147">Do not use the ".NET Framework 4 Client Profile".</span></span> 
  
### <a name="set-up-the-visual-studio-project"></a><span data-ttu-id="4e0e4-148">Visual Studio プロジェクトを設定する</span><span class="sxs-lookup"><span data-stu-id="4e0e4-148">Set up the Visual Studio project</span></span>

<span data-ttu-id="4e0e4-149">アプリケーションのセットアップは、新しいプロジェクトを作成し、適切なライブラリをリンクし、必要な名前空間を宣言します。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-149">The application setup consists of creating a new project, linking the appropriate libraries and declaring the needed namespaces.</span></span> <span data-ttu-id="4e0e4-150">Visual Studio では、複数の種類の開発プロジェクトが提供されています。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-150">Visual Studio presents several types of development projects.</span></span> <span data-ttu-id="4e0e4-151">このセクションは簡潔で非常に基本的なセクションです。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-151">The section is brief and very basic.</span></span> <span data-ttu-id="4e0e4-152">この値は、情報が 1 か所に合体している場合です。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-152">The value is having the information is coalesced in one place.</span></span>
  
#### <a name="select-a-visual-studio-project"></a><span data-ttu-id="4e0e4-153">Visual Studio プロジェクトを選択する</span><span class="sxs-lookup"><span data-stu-id="4e0e4-153">Select a Visual Studio project</span></span>

<span data-ttu-id="4e0e4-154">アドインに適切な種類のプロジェクトを作成するには、次の手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-154">To create a project of the appropriate type for the add-in, you must do the following steps.</span></span> <span data-ttu-id="4e0e4-155">画面で検出されたキーワードには、 **太字の属性** があります。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-155">Keywords encountered on the screen have a **bold** attribute:</span></span> 
  
1. <span data-ttu-id="4e0e4-156">[ファイル] メニューの[ファイルの新  >  **しいファイル] を**  >  **Project。**</span><span class="sxs-lookup"><span data-stu-id="4e0e4-156">From the File menu, choose **File** > **New** > **Project**.</span></span> 
    
2. <span data-ttu-id="4e0e4-157">左側のウィンドウの [インストール済みテンプレート]で、[Web アドイン  >  **C#Office/SharePoint**  >  **を選択します**。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-157">From the Installed templates in the left pane, select **C#** > **Office/SharePoint** > **Web Add-ins**.</span></span> 
    
3. <span data-ttu-id="4e0e4-158">中央のウィンドウの上部で **、[4 .NET Framework]** を選択します。現在のバージョンは 4.6 です。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-158">At the top of the central pane, select **.NET Framework 4** or later; the current version is 4.6.</span></span> 
    
4. <span data-ttu-id="4e0e4-159">中央ウィンドウのアプリケーションの種類から、[アドイン] **SharePoint選択します**。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-159">From the application types in the central pane, choose **SharePoint Add-in**.</span></span> 
    
5. <span data-ttu-id="4e0e4-160">下部のセクションで、プロジェクトの名前と場所、ソリューション名を指定します。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-160">In the bottom section, specify a name and location for the project, and a solution name.</span></span> 
    
6. <span data-ttu-id="4e0e4-161">また、下部のセクションで、[**ソリューションのディレクトリを作成**] ボックスがオンになっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-161">Also in the bottom section, check the **Create directory for solution** box.</span></span> 
    
7. <span data-ttu-id="4e0e4-162">[**OK**] をクリックして、初期プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-162">Click **OK** to create the initial project.</span></span> 
    
<span data-ttu-id="4e0e4-163">Visual Studio ウィザードでは、Project Online 設定サイト (ダイアログの SharePoint 設定と呼ばれる) に関するいくつかのフォローアップ質問を、その後に続くいくつかのダイアログで確認します。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-163">The Visual Studio Wizard asks a few follow-up questions about the Project Online settings site (called SharePoint settings in the dialogs) in a couple of dialogs that follow.</span></span> <span data-ttu-id="4e0e4-164">質問は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-164">Here are the questions:</span></span>
  
1. <span data-ttu-id="4e0e4-165">アドインSharePointデバッグに使用するサイトは何ですか?</span><span class="sxs-lookup"><span data-stu-id="4e0e4-165">What SharePoint site do you want to use for debugging your add-in?</span></span> <span data-ttu-id="4e0e4-166">サイトの URL をPWAします https://contoso.sharepoint.com/sites/pwa 。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-166">Specify the URL to your PWA site, such as https://contoso.sharepoint.com/sites/pwa.</span></span>
    
2. <span data-ttu-id="4e0e4-167">アドインをホストするSharePoint方法</span><span class="sxs-lookup"><span data-stu-id="4e0e4-167">How do you want to host your SharePoint Add-in?</span></span> <span data-ttu-id="4e0e4-168">[X] を選択SharePoint **ホストされます**。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-168">Choose [X] **SharePoint-hosted**.</span></span>
    
   <span data-ttu-id="4e0e4-169">ホスティング オプションを含むSharePointアドインの詳細については[、「SharePoint」を参照してください](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins)。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-169">For more information about SharePoint Add-ins, including hosting options, see [SharePoint Add-ins](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins).</span></span>
    
3. <span data-ttu-id="4e0e4-170">**[次へ]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-170">Click **Next**.</span></span> 
    
<span data-ttu-id="4e0e4-171">2 番目の追加ダイアログでは、アドインSharePointオンライン バージョンを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-171">The second additional dialog asks you to specify the SharePoint Online version for the add-in:</span></span> 
  
1. <span data-ttu-id="4e0e4-172">アドインにターゲットを設定するSharePointの最も古いバージョンは何ですか?</span><span class="sxs-lookup"><span data-stu-id="4e0e4-172">What's the earliest version of SharePoint that you want your add-in to target?</span></span> <span data-ttu-id="4e0e4-173">[X] S **harePoint-Online を選択します**。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-173">Choose [X] S **harePoint-Online**.</span></span> 
    
2. <span data-ttu-id="4e0e4-174">**[完了]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-174">Click **Finish**.</span></span> 
    
<span data-ttu-id="4e0e4-175">Visual Studio作成し、プロジェクト サイトにProject Onlineします。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-175">Visual Studio creates the project and accesses the Project Online site.</span></span> 
  
### <a name="enable-sideloading-on-the-project-online-site"></a><span data-ttu-id="4e0e4-176">サイトでサイドローディングをProject Onlineする</span><span class="sxs-lookup"><span data-stu-id="4e0e4-176">Enable sideloading on the Project Online site</span></span>

<span data-ttu-id="4e0e4-177">サイドローディングは、アドインのテストとデバッグProject Onlineメカニズムです。サイドローディングには、Project Online サイトでサイドローディングを有効にするスクリプトと、アドインのテストとデバッグが完了したらサイドローディングを無効にするスクリプトの 2 つが必要です。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-177">Sideloading is the mechanism for testing and debugging Project Online add-ins. You need two scripts for sideloading: one to enable sideloading on your Project Online site and another to disable sideloading once you finish testing and debugging the add-in.</span></span>
  
<span data-ttu-id="4e0e4-178">サイドローディングの設定の詳細については、「開発者以外のサイト コレクションでアプリのサイドローディングを有効にする [」を参照してください](https://blogs.msdn.microsoft.com/officeapps/2013/12/10/enable-app-sideloading-in-your-non-developer-site-collection/)。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-178">For more information about setting up sideloading, see [Enable app SideLoading in your non-developer site collection](https://blogs.msdn.microsoft.com/officeapps/2013/12/10/enable-app-sideloading-in-your-non-developer-site-collection/).</span></span>
  
> [!NOTE]
> <span data-ttu-id="4e0e4-179">サイドローディング アプリは開発者/テスト機能です。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-179">Sideloading apps is a developer/test feature.</span></span> <span data-ttu-id="4e0e4-180">これは、 **実稼働環境での使用を目的としたものではありません**。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-180">It is **not intended for production use**.</span></span> <span data-ttu-id="4e0e4-181">アプリを定期的にサイドロードしたり、アプリのサイドローディングをアクティブに使用しているよりも長く有効にしたりしません。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-181">Do not sideload apps regularly, or keep app sideloading enabled for longer than you are actively using the feature.</span></span> 
  
## <a name="add-content-to-the-add-in-project"></a><span data-ttu-id="4e0e4-182">アドイン プロジェクトにコンテンツを追加する</span><span class="sxs-lookup"><span data-stu-id="4e0e4-182">Add content to the add-in project</span></span>

<span data-ttu-id="4e0e4-183">プロジェクトを作成し、デバッグ メカニズムを設定した後、アプリにコンテンツを追加するには、次のタスクが含まれます。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-183">After creating a project and setting up the debugging mechanism, adding content to the app includes the following tasks:</span></span>
  
- <span data-ttu-id="4e0e4-184">アプリケーション スコープの設定</span><span class="sxs-lookup"><span data-stu-id="4e0e4-184">Setting the application scope</span></span>
    
- <span data-ttu-id="4e0e4-185">JSOM ライブラリのリンク</span><span class="sxs-lookup"><span data-stu-id="4e0e4-185">Linking the JSOM library</span></span>
    
- <span data-ttu-id="4e0e4-186">アドインへの UI 要素の追加</span><span class="sxs-lookup"><span data-stu-id="4e0e4-186">Adding UI Elements to the add-in</span></span>
    
- <span data-ttu-id="4e0e4-187">サービスの初期化と接続Project Onlineする</span><span class="sxs-lookup"><span data-stu-id="4e0e4-187">Initializing and connecting to the Project Online service</span></span>
    
- <span data-ttu-id="4e0e4-188">プロジェクトと詳細/プロパティの取得</span><span class="sxs-lookup"><span data-stu-id="4e0e4-188">Retrieving projects and details/properties</span></span>
    
- <span data-ttu-id="4e0e4-189">プロジェクトの表示</span><span class="sxs-lookup"><span data-stu-id="4e0e4-189">Displaying projects</span></span>
    
- <span data-ttu-id="4e0e4-190">ユーザーのタスクを表示Project</span><span class="sxs-lookup"><span data-stu-id="4e0e4-190">Displaying tasks for a Project</span></span>
    
<span data-ttu-id="4e0e4-191">アドイン プロジェクトは、多数のファイルで構成されます。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-191">The add-in project consists of many files.</span></span> <span data-ttu-id="4e0e4-192">この例では、次のファイルを編集する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-192">In this example, you'll need to edit the following files:</span></span> 
  
- <span data-ttu-id="4e0e4-193">AppManifest.xml</span><span class="sxs-lookup"><span data-stu-id="4e0e4-193">AppManifest.xml</span></span>
    
- <span data-ttu-id="4e0e4-194">Default.aspx</span><span class="sxs-lookup"><span data-stu-id="4e0e4-194">Default.aspx</span></span>
    
- <span data-ttu-id="4e0e4-195">App.js</span><span class="sxs-lookup"><span data-stu-id="4e0e4-195">App.js</span></span>
    
- <span data-ttu-id="4e0e4-196">App.css - 省略可能。アドイン用に開発されたスタイル定義が含まれている</span><span class="sxs-lookup"><span data-stu-id="4e0e4-196">App.css - optional; contains style definitions developed for the add-in</span></span>
    
<span data-ttu-id="4e0e4-197">試用版からサブスクリプション サイトへの移行など、Project Online テナントが変更された場合は、[プロパティ ウィンドウの表示] コマンドで使用できる [プロパティ] ウィンドウを使用して、サーバー接続やサイト URL などのプロジェクト プロパティを更新できます。  >  </span><span class="sxs-lookup"><span data-stu-id="4e0e4-197">If the Project Online tenant changes, such as moving from a trial to a subscription site, you can update the project properties, including the Server Connection and Site URL, using the Properties Window available through the **View** > **Properties Window** command.</span></span> 
  
<span data-ttu-id="4e0e4-198">プロジェクトにファイルを追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-198">You can also add files to the project.</span></span> <span data-ttu-id="4e0e4-199">その場合は、同じグループ (コンテンツ、イメージ、ページ、またはスクリプト) にある Elements.xml ファイルを更新して、新しいファイルを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-199">If so, you'll need to update the Elements.xml file located in the same group (Content, Images, Pages, or Scripts) to include the new files.</span></span> <span data-ttu-id="4e0e4-200">プロジェクト ファイルの詳細については、「アプリ マニフェスト構造の探索」および「アドインのパッケージSharePoint[参照してください](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/explore-the-app-manifest-structure-and-the-package-of-a-sharepoint-add-in)。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-200">For more information about the project files, see [Explore the app manifest structure and the package of a SharePoint Add-in](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/explore-the-app-manifest-structure-and-the-package-of-a-sharepoint-add-in).</span></span>
  
### <a name="set-application-scope"></a><span data-ttu-id="4e0e4-201">アプリケーション スコープの設定</span><span class="sxs-lookup"><span data-stu-id="4e0e4-201">Set application scope</span></span>

<span data-ttu-id="4e0e4-202">サービスがクエリ結果に情報を返す前に、アドインにはスコープまたはアクセス許可レベルが定義されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-202">The add-in needs scope or permission levels defined before the service returns information in query results.</span></span> <span data-ttu-id="4e0e4-203">このアドインでは、次のスコープを使用してプロジェクトのVisual Studioします。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-203">For this add-in, use the following scope to the Visual Studio project.</span></span> <span data-ttu-id="4e0e4-204">この変更は、[アクセス許可] タブAppManifest.xmlファイルに対して行います。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-204">This change is made to the AppManifest.xml file in the Permissions tab:</span></span>

|<span data-ttu-id="4e0e4-205">範囲</span><span class="sxs-lookup"><span data-stu-id="4e0e4-205">Scope</span></span>|<span data-ttu-id="4e0e4-206">アクセス許可</span><span class="sxs-lookup"><span data-stu-id="4e0e4-206">Permission</span></span>|
|:-----|:-----|
|<span data-ttu-id="4e0e4-207">複数のプロジェクト (Project サーバー)</span><span class="sxs-lookup"><span data-stu-id="4e0e4-207">Multiple Projects (Project Server)</span></span>  <br/> |<span data-ttu-id="4e0e4-208">Read</span><span class="sxs-lookup"><span data-stu-id="4e0e4-208">Read</span></span>  <br/> |
   
<span data-ttu-id="4e0e4-209">アプリケーションスコープを設定した後にファイルを保存します。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-209">Save the file after setting the application scope.</span></span> <span data-ttu-id="4e0e4-210">それ以外の場合、サービスからデータは返されません。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-210">Otherwise, no data will be returned from the service.</span></span> 
  
### <a name="link-the-jsom-library"></a><span data-ttu-id="4e0e4-211">JSOM ライブラリのリンク</span><span class="sxs-lookup"><span data-stu-id="4e0e4-211">Link the JSOM library</span></span>

<span data-ttu-id="4e0e4-212">ランタイム ライブラリProject Online、PS.jsおよびPS.debug.jsは、Project Onlineによって提供され、常に最新のバージョンです。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-212">The runtime Project Online libraries, PS.js and PS.debug.js, are provided by Project Online and are always the most recent version.</span></span> <span data-ttu-id="4e0e4-213">JSOM を使用する JavaScript アドインは、これらのライブラリの 1 つとリンクする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-213">JavaScript add-ins that use JSOM must link with one of these libraries.</span></span> <span data-ttu-id="4e0e4-214">リンク定義は Default.aspx ファイルに追加されます。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-214">The linking definitions are added in the Default.aspx file.</span></span> <span data-ttu-id="4e0e4-215">このコマンドを使用PS.js、PS.debug.jsファイルにあるコードの一部App.jsします。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-215">The commands to use the PS.js and/or PS.debug.js are part of the code located in the App.js file.</span></span>
  
<span data-ttu-id="4e0e4-216">"PS.js:ScriptLink" PS.js SharePoint:ScriptLink" にPS.debug.jsの要素に、次のコマンドを追加 `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` sp.js。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-216">Add the following command for PS.js or PS.debug.js definition in the  `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` element following the "SharePoint:ScriptLink" for sp.js.</span></span> 
  
```js
<SharePoint:ScriptLink name="PS.js" runat="server" OnDemand="false" LoadAfterUI="true" Localizable="false" />
```

> [!NOTE]
> <span data-ttu-id="4e0e4-217">ユーザー **またはユーザーの OnDemand** 属性PS.js false にPS.debug.js設定 **されます**。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-217">The **OnDemand** attribute for PS.js or PS.debug.js set to **false**.</span></span> 
  
### <a name="add-ui-elements-to-the-add-in"></a><span data-ttu-id="4e0e4-218">アドインに UI 要素を追加する</span><span class="sxs-lookup"><span data-stu-id="4e0e4-218">Add UI elements to the add-in</span></span>

<span data-ttu-id="4e0e4-219">アドインの例は、いくつかのコンポーネントで構成されています。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-219">The example add-in consists of a few components.</span></span> <span data-ttu-id="4e0e4-220">静的要素の説明は、Default.aspx ファイルに保存されます。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-220">Static element descriptions are located in the Default.aspx file.</span></span> <span data-ttu-id="4e0e4-221">すべてのコンポーネントの動的要素の説明とコードは、App.jsファイルに保存されます。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-221">Dynamic element descriptions and code for all components are located in the App.js file.</span></span> <span data-ttu-id="4e0e4-222">コンポーネントに関するコメントについては、ソース コードの一覧を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-222">For comments regarding the components, refer to the source code listings.</span></span> <span data-ttu-id="4e0e4-223">アドインの UI コンポーネントの一覧を次に示します。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-223">Here is a list of the UI components in the add-in:</span></span>
  
- <span data-ttu-id="4e0e4-224">タイトル</span><span class="sxs-lookup"><span data-stu-id="4e0e4-224">Title</span></span>
    
- <span data-ttu-id="4e0e4-225">入門動詞</span><span class="sxs-lookup"><span data-stu-id="4e0e4-225">Introductory verbiage</span></span>
    
- <span data-ttu-id="4e0e4-226">テーブルからタスクを削除するボタン</span><span class="sxs-lookup"><span data-stu-id="4e0e4-226">Button to remove tasks from the table</span></span>
    
- <span data-ttu-id="4e0e4-227">プロジェクト ID と名前、およびタスク情報を一覧表示するテーブル。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-227">Table that lists the project ID and name, and the task information.</span></span>
    
- <span data-ttu-id="4e0e4-228">タスク データをテーブルにインポートするタスク ボタン (プロジェクトごとに 1 回複製)。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-228">Tasks Button (cloned once for each project) that imports task data into the table.</span></span>
    
<span data-ttu-id="4e0e4-229">プロジェクト テーブルのタイトルやヘッダー部分など、ユーザー インターフェイスの詳細については、「Default.aspx プロジェクト ファイル」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-229">For details of the user interface, such as the title and the header portion of the project table, see the Default.aspx project file.</span></span>
  
### <a name="initialize-and-connect-to-the-host-system"></a><span data-ttu-id="4e0e4-230">ホスト システムの初期化と接続</span><span class="sxs-lookup"><span data-stu-id="4e0e4-230">Initialize and connect to the host system</span></span>

<span data-ttu-id="4e0e4-231">このApp.jsには JavaScript コードが含まれている。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-231">The App.js file contains the JavaScript code.</span></span> <span data-ttu-id="4e0e4-232">アドインはブラウザーでPS.js読み込み、initializePage 関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-232">The add-in loads PS.js in the browser, and then calls the initializePage function.</span></span> <span data-ttu-id="4e0e4-233">InitializePage は、エンドポイントのコンテキストを取得Project Online loadProjects 関数を開始します。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-233">InitializePage retrieves a context to the Project Online endpoint and starts the loadProjects function.</span></span>
  
```js
    'use strict';
    SP.SOD.executeOrDelayUntilScriptLoaded(initializePage, "PS.js");
    //Project PWA Context and published projects in PWA
    var projContext;
    var projects;
    function initializePage() {
        //Get the Project context for this web
        projContext = PS.ProjectContext.get_current();
        loadProjects();
    }
    //General CSOM failure event handler
    //Invoked when ExecuteQueryAsync returns unsuccessfully
    function onRequestFailed(sender, args) {
        alert("Failed to execute: " + args.get_message());
        return;
    };

```

### <a name="retrieve-the-projects"></a><span data-ttu-id="4e0e4-234">プロジェクトを取得する</span><span class="sxs-lookup"><span data-stu-id="4e0e4-234">Retrieve the projects</span></span>

<span data-ttu-id="4e0e4-235">loadProjects 関数は、プロジェクト名と ID をサービスに照会します。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-235">The loadProjects function queries the service for the project names and IDs.</span></span> 
  
<span data-ttu-id="4e0e4-236">アプリケーションは、プロジェクト名とプロジェクト ID を取得します。プロジェクトに関するその他の情報は使用可能であり、取得するプロパティを明示的に識別するために load メソッドを変更することでアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-236">The application retrieves the project name and project Id. Other information about the project is available and can be accessed by modifying the load method to identify explicitly the properties to retrieve.</span></span> <span data-ttu-id="4e0e4-237">例は、コード内でコメントとして提供されます。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-237">An example is provided in the code as a comment.</span></span> 
  
<span data-ttu-id="4e0e4-238">クエリが成功すると、アドインは displayProjects を呼び出して続行されます。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-238">If the query succeeds, the add-in continues by calling displayProjects.</span></span> 
  
```js
    //Query CSOM and get the list of projects in PWA
    function loadProjects() {
        projects = projContext.get_projects();
    //Request to server - identifies what to retrieve
        projContext.load(projects, 'Include(Name, Id)');
        //Notice to server to execute query
        projContext.executeQueryAsync(displayProjects, onRequestFailed);
        // Syntax for requesting more fields to pull down from server
        // projContext.load(projects, 'Include(Name, Description, StartDate, 
        // Id, IsCheckedOut)');
    }

```

### <a name="display-the-projects"></a><span data-ttu-id="4e0e4-239">プロジェクトを表示する</span><span class="sxs-lookup"><span data-stu-id="4e0e4-239">Display the projects</span></span>

<span data-ttu-id="4e0e4-240">displayProjects 関数は、表、プロジェクトごとに 1 行、および特定のプロジェクトのタスクを表示するボタンを作成します。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-240">The displayProjects function creates a table, one row per project, and a button to show the tasks for the specific project.</span></span> 
  
```js
    //Display the projects with names and ids in a table
    function displayProjects() {
        //Current published project and ID
        var p, projId;
        //Project table rows to publish collectively
        var pTable = []; 
        var pEnum = projects.getEnumerator();
        //Build a 3-column table, with one project per row.
        while (pEnum.moveNext()) {
            p = pEnum.get_current();
        
            //Items used in getting information for table rows:
            //Current published project object, and ID and name
            // var project = p;
            // var projId = p.get_id();
            // var projName = p.get_name();
        
            //Continue processing/working with project object as needed.
        }
    }

```

> [!NOTE]
> <span data-ttu-id="4e0e4-241">while ループは ID と名前のプロパティにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-241">The while loop accesses the ID and name properties.</span></span> <span data-ttu-id="4e0e4-242">これは、同じプロパティにアクセスする関数を呼び出すソース コード プロジェクトとは若干異なります。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-242">This is slightly different than the source code project that calls a function that, in turn, accesses the same properties.</span></span> 
  
### <a name="display-the-tasks-for-a-project"></a><span data-ttu-id="4e0e4-243">プロジェクトのタスクを表示する</span><span class="sxs-lookup"><span data-stu-id="4e0e4-243">Display the tasks for a project</span></span>

<span data-ttu-id="4e0e4-244">アドインの一部であるタスクは、最初の読み込みの一部ではありません。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-244">The tasks, while part of the add-in, are not part of the initial loading.</span></span> <span data-ttu-id="4e0e4-245">ユーザーがプロジェクトに関連付けられているタスクに関心がある場合は、[タスクの表示] ボタンをクリックすると、タスクが btnLoadTasks イベント ハンドラーを使用してリストに表示されます。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-245">If the user is interested in the tasks associated with a project, clicking the "Show Tasks" button causes the tasks to display in the list using the btnLoadTasks event handler.</span></span> 
  
<span data-ttu-id="4e0e4-246">btnLoadTasks イベント ハンドラーは、適切なプロジェクト ID を持ち、指定したプロジェクトのタスクをサーバーから要求します。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-246">The btnLoadTasks event handler, with the appropriate project ID, requests the tasks for the specified project from the server.</span></span> <span data-ttu-id="4e0e4-247">取得されると、btnLoadTasks はタスク リストを displayTasks に渡し、タスクを画面上に表示します。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-247">Once retrieved, btnLoadTasks passes the task list to displayTasks to present the tasks onscreen.</span></span>
  
```js
    //Query CSOM and get the list of tasks for a specific project
    function btnLoadTasks(pid) {
        //Event handler for the "Show tasks" buttons. 
        //
        //The project ID is the sole argument and is used to get the appropriate task 
        //info from the service.
        //The project ID is also the button name, and is used to identify where to place
        //the task information in the table.
        //
        //Project ID to pass to the event handler
        var projId = pid;
        //
        //Get the project reference
        var pProj = projects.getById(projId);
        //
        //Get the tasks collection reference associated with the project.
        var tasks = pProj.get_tasks();
        //
        projContext.load(tasks, 'Include(Id, Name, Start, ScheduledStart, Completion)');
        //
        //If the query succeeds, displayTasks presents the tasks to the user.
        projContext.executeQueryAsync(function () { displayTasks(tasks, projId) }, onRequestFailed);
    }

```

<span data-ttu-id="4e0e4-248">displayTasks 関数は、指定したプロジェクトに関連付けられたタスクを、プロジェクト エントリの直下に表示します。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-248">The displayTasks function displays the tasks associated with a specified project immediately beneath the project entry.</span></span>
  
```js
    //Insert tasks for the specified project immediately underneath the project entry 
    //in the table.
    function displayTasks(tasks, projId) {
        //selected project ID
        var pId = projId;
        //individual task
        var t;
        //Task table rows to publish collectively
        var tTable = [];
        var tEnum = tasks.getEnumerator();
        //Build table one task per row.
        while (tEnum.moveNext()) {
            t = tEnum.get_current();
            //
            //Items used in getting information for table rows:
            //Current task object, and ID and name
            // var task = t;
            // var taskId = t.get_id();
            // var taskName = t.get_name();
            
            //Continue processing/working with task object as needed.
        }
    }

```

> [!NOTE]
> <span data-ttu-id="4e0e4-249">while ループは、タスク ID と名前のプロパティにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-249">The while loop accesses the task ID and name properties.</span></span> <span data-ttu-id="4e0e4-250">これは、同じプロパティにアクセスする関数を呼び出すソース コード プロジェクトとは若干異なります。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-250">This is slightly different than the source code project that calls a function that, in turn, accesses the same properties.</span></span> 
  
<span data-ttu-id="4e0e4-251">1 つのプロジェクトのタスクの出力例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-251">Sample output for the tasks of a single project follows.</span></span>
  
<span data-ttu-id="4e0e4-252">![プロジェクト タスクの出力を示す]スクリーン ショット プロジェクト タスクの出力(media/f6500a3f-000b-4f3e-9be6-9a74d0bea15e.png "を示すスクリーン")ショット</span><span class="sxs-lookup"><span data-stu-id="4e0e4-252">![Screen shot showing the output for a project task](media/f6500a3f-000b-4f3e-9be6-9a74d0bea15e.png "Screen shot showing the output for a project task")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4e0e4-253">関連項目</span><span class="sxs-lookup"><span data-stu-id="4e0e4-253">See also</span></span>

<span data-ttu-id="4e0e4-254">Project Online および CSOM を使用したアプリケーション開発に関するドキュメントとサンプルについては、[Project 開発ポータル](https://developer.microsoft.com/en-us/project)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-254">For documentation and samples related to Project Online and application development using CSOM, see the [Project Development Portal](https://developer.microsoft.com/en-us/project).</span></span>
    


