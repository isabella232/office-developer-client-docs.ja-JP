---
title: JavaScript オブジェクトモデル (jsom) を使用して Project Online アドインを開発する
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4a4b1ad2-de46-421d-a698-53c20c90b93a
description: この記事では、project online の利便性を向上させるための Microsoft project online アドイン開発について説明します。 開発プロジェクトは、チュートリアルとして実装されています。 この記事で使用されているアドインでは、project Online アカウントから発行済みプロジェクトのプロジェクト名と id を読み込んで表示することができ、個々のプロジェクトに関連付けられたタスクを取得するためにドリルダウンすることができます。
ms.openlocfilehash: 0a472a6300f18aaa65649f44d944445642a59e1a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322691"
---
# <a name="developing-a-project-online-add-in-using-the-javascript-object-model-jsom"></a><span data-ttu-id="4de1f-105">JavaScript オブジェクトモデル (jsom) を使用して Project Online アドインを開発する</span><span class="sxs-lookup"><span data-stu-id="4de1f-105">Developing a Project Online add-in using the JavaScript Object Model (JSOM)</span></span>

<span data-ttu-id="4de1f-106">この記事では、project online の利便性を向上させるための Microsoft project online アドイン開発について説明します。</span><span class="sxs-lookup"><span data-stu-id="4de1f-106">This article describes Microsoft Project Online Add-in development to enhance your experience with the Project Online.</span></span> <span data-ttu-id="4de1f-107">開発プロジェクトは、チュートリアルとして実装されています。</span><span class="sxs-lookup"><span data-stu-id="4de1f-107">The development project is implemented as a walkthrough.</span></span> <span data-ttu-id="4de1f-108">この記事で使用されているアドインでは、project Online アカウントから発行済みプロジェクトのプロジェクト名と id を読み込んで表示することができ、個々のプロジェクトに関連付けられたタスクを取得するためにドリルダウンすることができます。</span><span class="sxs-lookup"><span data-stu-id="4de1f-108">The add-in used for this article reads and displays the project names and IDs of the published projects from your Project Online account and allows you to drill down to retrieve tasks associated with individual projects.</span></span>
  
<span data-ttu-id="4de1f-109">実行時に、アドインの一覧は次の図のようになります。</span><span class="sxs-lookup"><span data-stu-id="4de1f-109">At run time, the add-in listing looks similar to the following illustration:</span></span>
  
<span data-ttu-id="4de1f-110">![jsom のプロジェクトとタスクの一覧を示すスクリーンショット](media/766e5914-f048-48f4-9282-291f55e6e90d.png "jsom のプロジェクトとタスクの一覧を示すスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="4de1f-110">![Screen shot showing a listing of JSOM projects and tasks](media/766e5914-f048-48f4-9282-291f55e6e90d.png "Screen shot showing a listing of JSOM projects and tasks")</span></span>
  
<span data-ttu-id="4de1f-111">この例の目的は、Project Online との対話と、サービスからの要求ごとにクエリを実行してコンテキストを設定することです。</span><span class="sxs-lookup"><span data-stu-id="4de1f-111">The focus of the example is the interaction with the Project Online, making queries and setting the context for each request from the service.</span></span> <span data-ttu-id="4de1f-112">ユーザーインターフェイス (UI) 要素には、特に注意が払われません。</span><span class="sxs-lookup"><span data-stu-id="4de1f-112">User interface (UI) elements receive minimal attention.</span></span> <span data-ttu-id="4de1f-113">その代わりに、ソースリストには UI に関するコメントが記載されています。</span><span class="sxs-lookup"><span data-stu-id="4de1f-113">Instead, the source listings provide comments regarding the UI.</span></span>
  
> [!NOTE]
> <span data-ttu-id="4de1f-114">サンプルアドインのソースファイル (Visual Studio プロジェクト) は、から入手できhttps://github.com/OfficeDev/Project-JSOM-List-Projects-Tasks....ます。</span><span class="sxs-lookup"><span data-stu-id="4de1f-114">The source files for the example add-in, a Visual Studio project, are available at: https://github.com/OfficeDev/Project-JSOM-List-Projects-Tasks.....</span></span> <span data-ttu-id="4de1f-115">記事を読む際に、ソースファイルを参照できるようにしておきます。</span><span class="sxs-lookup"><span data-stu-id="4de1f-115">Keep the source files handy as a reference while you read the article, as each complements the other.</span></span> <span data-ttu-id="4de1f-116">Visual Studio プロジェクトのファイルがビルドされ、最小限の変更で実行可能になります。これは、project Online テナントの URL を PWA フォルダーに置き換えることです。</span><span class="sxs-lookup"><span data-stu-id="4de1f-116">The files in the Visual Studio project build and are executable with minimal changes—substituting the URL for your Project Online tenant down to the PWA folder.</span></span> 
  
## <a name="background"></a><span data-ttu-id="4de1f-117">背景</span><span class="sxs-lookup"><span data-stu-id="4de1f-117">Background</span></span>

<span data-ttu-id="4de1f-118">project Online は、ポートフォリオ、プログラム、プロジェクトを調整して管理するプロジェクトポートフォリオ管理 (PPM) および project management Office (PMO) ソリューションを企業に提供する Office 365 サービスです。</span><span class="sxs-lookup"><span data-stu-id="4de1f-118">Project Online is a Office 365 service that provides companies with a project portfolio management (PPM) and project management office (PMO) solution to coordinate and manage portfolios, programs, and projects.</span></span> <span data-ttu-id="4de1f-119">project Online は、project デスクトップエディションとは異なるオファーリングです。しかし、project Online には、プロジェクトのライフサイクルを通じてプロジェクトの詳細を維持および追跡する機能がまだ含まれています。</span><span class="sxs-lookup"><span data-stu-id="4de1f-119">Project Online is a different offering than the Project desktop editions; yet, Project Online still contains the functionality to maintain and track project details throughout the life of a project.</span></span> <span data-ttu-id="4de1f-120">Project online は SharePoint online 上に構築されています。</span><span class="sxs-lookup"><span data-stu-id="4de1f-120">Project Online is built on SharePoint Online.</span></span>
  
<span data-ttu-id="4de1f-121">Project Online のホスト型アドインは、クライアント側オブジェクトモデル API とやり取りする JavaScript およびリソースファイルで構成されています。</span><span class="sxs-lookup"><span data-stu-id="4de1f-121">A Project Online hosted add-in consists of JavaScript and resource files that interact with the Client-Side-Object-Model API.</span></span> <span data-ttu-id="4de1f-122">ユーザーがアドインを訪問すると、JavaScript とリソースがダウンロードされ、ブラウザー内で実行されます。</span><span class="sxs-lookup"><span data-stu-id="4de1f-122">When the user visits the add-in, the JavaScript and resources are downloaded and executed within the browser.</span></span> <span data-ttu-id="4de1f-123">このアドインは、データを作成、取得、更新、削除するかどうかにかかわらず、Project Online への非同期呼び出しを行い、サービスと対話します。</span><span class="sxs-lookup"><span data-stu-id="4de1f-123">The add-In makes asynchronous calls to Project Online to interact with the service, whether creating, retrieving, updating, or deleting data.</span></span> 
  
<span data-ttu-id="4de1f-124">Project Online は、アドインから他のテナントに属する情報を保護するためのもう1つのアクションを実行します。つまり、Project Online は、アドインからの要求を操作する分離されたサイトを作成します。</span><span class="sxs-lookup"><span data-stu-id="4de1f-124">Project Online performs one more action to protect information that belongs to other tenants from the add-in; namely, Project Online creates an isolated site to interact with the requests from the add-in.</span></span> <span data-ttu-id="4de1f-125">プロジェクトオンラインホスト上で実行されるカスタムコードはありません。</span><span class="sxs-lookup"><span data-stu-id="4de1f-125">No custom code runs on the Project Online host.</span></span> 
  
<span data-ttu-id="4de1f-126">project Online アドインの開発セットアップでは、Visual Studio SharePoint アドインプロジェクトの種類を使用します。</span><span class="sxs-lookup"><span data-stu-id="4de1f-126">The development setup for Project Online add-ins uses the Visual Studio SharePoint Add-in project type.</span></span> <span data-ttu-id="4de1f-127">アドインは javascript で記述され、プロジェクト javascript オブジェクトモデル (jsom) を使用して project Online サービスを操作します。</span><span class="sxs-lookup"><span data-stu-id="4de1f-127">The add-in is written in JavaScript, and uses the Project JavaScript object model (JSOM) to interact with the Project Online service.</span></span> <span data-ttu-id="4de1f-128">jsom は、SharePoint jsom から多くの機能を継承します。</span><span class="sxs-lookup"><span data-stu-id="4de1f-128">The JSOM inherits much of its functionality from the SharePoint JSOM.</span></span>
  
> [!NOTE]
> <span data-ttu-id="4de1f-129">アドインは、Office ストアで発行して販売したり、SharePoint 上のプライベートアプリカタログに展開したりできます。</span><span class="sxs-lookup"><span data-stu-id="4de1f-129">Add-ins can be published and sold in the Office Store or deployed to a private app catalog on SharePoint.</span></span> <span data-ttu-id="4de1f-130">詳細については、「 [Office アドインを展開して発行する](https://docs.microsoft.com/office/dev/add-ins/publish/publish)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4de1f-130">For more information, see [Deploy and publish your Office Add-in](https://docs.microsoft.com/office/dev/add-ins/publish/publish).</span></span>
> 
> <span data-ttu-id="4de1f-131">この記事で使用されているアドインは、開発者向けのサンプルです。これは、運用環境での使用を目的としたものではありません。</span><span class="sxs-lookup"><span data-stu-id="4de1f-131">The add-in used in this article is a sample for developers; it is not intended for use in a production environment.</span></span> <span data-ttu-id="4de1f-132">主な目的は、Project Online のアプリ開発の例を示すことです。</span><span class="sxs-lookup"><span data-stu-id="4de1f-132">The primary purpose is to show an example of app development for Project Online.</span></span> 
  
## <a name="prerequisites"></a><span data-ttu-id="4de1f-133">前提条件</span><span class="sxs-lookup"><span data-stu-id="4de1f-133">Prerequisites</span></span>

<span data-ttu-id="4de1f-134">サポートされている Windows 環境に以下の項目を追加します。</span><span class="sxs-lookup"><span data-stu-id="4de1f-134">Add the following items to a supported Windows environment:</span></span>
  
- <span data-ttu-id="4de1f-135">**.net Framework 4.0**以降: バージョン4.0 のフレームワークの完全なバージョンは互換性があります。</span><span class="sxs-lookup"><span data-stu-id="4de1f-135">**.NET Framework 4.0 or later**: Complete versions of the framework from version 4.0 are compatible.</span></span> <span data-ttu-id="4de1f-136">ダウンロード サイトは https://msdn.microsoft.com/vstudio/aa496123.aspx です。</span><span class="sxs-lookup"><span data-stu-id="4de1f-136">The download site is https://msdn.microsoft.com/vstudio/aa496123.aspx.</span></span>
    
- <span data-ttu-id="4de1f-137">**Visual Studio 2013 以降**:</span><span class="sxs-lookup"><span data-stu-id="4de1f-137">**Visual Studio 2013 or later**:</span></span>  
    
   - <span data-ttu-id="4de1f-138">Visual Studio 2015 のプロフェッショナルエディションは、すぐにご利用いただけhttps://www.visualstudio.com/en-us/products/visual-studio-professional-with-msdn-vs.aspxます。また、から入手できます。</span><span class="sxs-lookup"><span data-stu-id="4de1f-138">The professional edition of Visual Studio 2015 is ready to go out-of-the box and is available at https://www.visualstudio.com/en-us/products/visual-studio-professional-with-msdn-vs.aspx.</span></span>
    
   - <span data-ttu-id="4de1f-139">Visual Studio 2015 のコミュニティエディションは、でhttps://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx入手できます。</span><span class="sxs-lookup"><span data-stu-id="4de1f-139">The community edition of Visual Studio 2015 is available at https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx.</span></span> <span data-ttu-id="4de1f-140">このエディションでは、Microsoft Office Developer Tools for Visual Studio を手動でインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4de1f-140">This edition requires manual installation of the Microsoft Office Developer Tools for Visual Studio.</span></span>
    
   <span data-ttu-id="4de1f-141">Microsoft Office Developer Tools for Visual Studio は、からhttps://www.visualstudio.com/en-us/features/office-tools-vs.aspx入手できます。</span><span class="sxs-lookup"><span data-stu-id="4de1f-141">The Microsoft Office Developer Tools for Visual Studio are available at https://www.visualstudio.com/en-us/features/office-tools-vs.aspx.</span></span>
    
- <span data-ttu-id="4de1f-142">**Project Online アカウント**: これにより、ホスティングサービスへのアクセスが可能になります。</span><span class="sxs-lookup"><span data-stu-id="4de1f-142">**A Project Online account**: This provides access to the hosting service.</span></span> <span data-ttu-id="4de1f-143">Project Online アカウントの入手の詳細については、https://products.office.com/en-us/Project/project-online-portfolio-management をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="4de1f-143">For more information about obtaining a Project Online account, see https://products.office.com/en-us/Project/project-online-portfolio-management.</span></span>
    
   <span data-ttu-id="4de1f-144">アドインユーザーに、Project Online テナントの一部のプロジェクトにアクセスするための十分な権限があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4de1f-144">Ensure that the add-in user has sufficient authorization to access some projects in the Project Online tenant.</span></span> 
    
- <span data-ttu-id="4de1f-145">情報が格納されている**ホストサイト上のプロジェクト**。</span><span class="sxs-lookup"><span data-stu-id="4de1f-145">**Projects on the hosting site** that are populated with information.</span></span>
    
> [!NOTE]
> <span data-ttu-id="4de1f-146">標準の .net framework は、適切なフレームワークを使用します。</span><span class="sxs-lookup"><span data-stu-id="4de1f-146">The standard .NET Framework is the correct framework to use.</span></span> <span data-ttu-id="4de1f-147">".net Framework 4 クライアントプロファイル" は使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="4de1f-147">Do not use the ".NET Framework 4 Client Profile".</span></span> 
  
### <a name="set-up-the-visual-studio-project"></a><span data-ttu-id="4de1f-148">Visual Studio プロジェクトを設定する</span><span class="sxs-lookup"><span data-stu-id="4de1f-148">Set up the Visual Studio project</span></span>

<span data-ttu-id="4de1f-149">アプリケーションのセットアップでは、新しいプロジェクトを作成し、適切なライブラリをリンクし、必要な名前空間を宣言します。</span><span class="sxs-lookup"><span data-stu-id="4de1f-149">The application setup consists of creating a new project, linking the appropriate libraries and declaring the needed namespaces.</span></span> <span data-ttu-id="4de1f-150">Visual Studio では、複数の種類の開発プロジェクトが提供されています。</span><span class="sxs-lookup"><span data-stu-id="4de1f-150">Visual Studio presents several types of development projects.</span></span> <span data-ttu-id="4de1f-151">このセクションは短時間で、非常に基本的なものです。</span><span class="sxs-lookup"><span data-stu-id="4de1f-151">The section is brief and very basic.</span></span> <span data-ttu-id="4de1f-152">この値は、情報が1つの場所に結合されていることを示します。</span><span class="sxs-lookup"><span data-stu-id="4de1f-152">The value is having the information is coalesced in one place.</span></span>
  
#### <a name="select-a-visual-studio-project"></a><span data-ttu-id="4de1f-153">Visual Studio プロジェクトを選択する</span><span class="sxs-lookup"><span data-stu-id="4de1f-153">Select a Visual Studio project</span></span>

<span data-ttu-id="4de1f-154">アドインに適した種類のプロジェクトを作成するには、次の手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4de1f-154">To create a project of the appropriate type for the add-in, you must do the following steps.</span></span> <span data-ttu-id="4de1f-155">画面に表示されたキーワードには、**太字**の属性があります。</span><span class="sxs-lookup"><span data-stu-id="4de1f-155">Keywords encountered on the screen have a **bold** attribute:</span></span> 
  
1. <span data-ttu-id="4de1f-156">[ファイル] メニューの [ \*\*\*\* > **新しい** > **プロジェクト**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="4de1f-156">From the File menu, choose **File** > **New** > **Project**.</span></span> 
    
2. <span data-ttu-id="4de1f-157">インストールされているテンプレートの左側のウィンドウで、[ **C#** > **Office/SharePoint** > **Web アドイン**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="4de1f-157">From the Installed templates in the left pane, select **C#** > **Office/SharePoint** > **Web Add-ins**.</span></span> 
    
3. <span data-ttu-id="4de1f-158">中央のウィンドウの上部で、[ **.net Framework 4**以降] を選択します。現在のバージョンは4.6 です。</span><span class="sxs-lookup"><span data-stu-id="4de1f-158">At the top of the central pane, select **.NET Framework 4** or later; the current version is 4.6.</span></span> 
    
4. <span data-ttu-id="4de1f-159">中央のウィンドウの [アプリケーションの種類] で、[ **SharePoint アドイン**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="4de1f-159">From the application types in the central pane, choose **SharePoint Add-in**.</span></span> 
    
5. <span data-ttu-id="4de1f-160">下部のセクションで、プロジェクトの名前と場所、ソリューション名を指定します。</span><span class="sxs-lookup"><span data-stu-id="4de1f-160">In the bottom section, specify a name and location for the project, and a solution name.</span></span> 
    
6. <span data-ttu-id="4de1f-161">また、下部のセクションで、[**ソリューションのディレクトリを作成**] ボックスがオンになっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4de1f-161">Also in the bottom section, check the **Create directory for solution** box.</span></span> 
    
7. <span data-ttu-id="4de1f-162">[**OK**] をクリックして、初期プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="4de1f-162">Click **OK** to create the initial project.</span></span> 
    
<span data-ttu-id="4de1f-163">Visual Studio ウィザードは、次の2つのダイアログボックスで、Project Online 設定サイト (ダイアログ内の SharePoint 設定と呼ばれます) についてのいくつかの質問を行います。</span><span class="sxs-lookup"><span data-stu-id="4de1f-163">The Visual Studio Wizard asks a few follow-up questions about the Project Online settings site (called SharePoint settings in the dialogs) in a couple of dialogs that follow.</span></span> <span data-ttu-id="4de1f-164">質問は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="4de1f-164">Here are the questions:</span></span>
  
1. <span data-ttu-id="4de1f-165">アドインのデバッグに使用する SharePoint サイトを指定します。</span><span class="sxs-lookup"><span data-stu-id="4de1f-165">What SharePoint site do you want to use for debugging your add-in?</span></span> <span data-ttu-id="4de1f-166">のような PWA サイトの URL を指定しhttps://contoso.sharepoint.com/sites/pwaます。</span><span class="sxs-lookup"><span data-stu-id="4de1f-166">Specify the URL to your PWA site, such as https://contoso.sharepoint.com/sites/pwa.</span></span>
    
2. <span data-ttu-id="4de1f-167">SharePoint アドインをどのようにホストしますか?</span><span class="sxs-lookup"><span data-stu-id="4de1f-167">How do you want to host your SharePoint Add-in?</span></span> <span data-ttu-id="4de1f-168">[X] **SharePoint ホスト型**を選択します。</span><span class="sxs-lookup"><span data-stu-id="4de1f-168">Choose [X] **SharePoint-hosted**.</span></span>
    
   <span data-ttu-id="4de1f-169">ホスティングオプションを含む sharepoint アドインの詳細については、「 [sharepoint アドイン](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4de1f-169">For more information about SharePoint Add-ins, including hosting options, see [SharePoint Add-ins](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins).</span></span>
    
3. <span data-ttu-id="4de1f-170">**[次へ]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4de1f-170">Click **Next**.</span></span> 
    
<span data-ttu-id="4de1f-171">2番目の追加のダイアログで、アドインの SharePoint Online バージョンを指定するよう求められます。</span><span class="sxs-lookup"><span data-stu-id="4de1f-171">The second additional dialog asks you to specify the SharePoint Online version for the add-in:</span></span> 
  
1. <span data-ttu-id="4de1f-172">アドインの対象となる SharePoint の最も古いバージョンは何ですか。</span><span class="sxs-lookup"><span data-stu-id="4de1f-172">What's the earliest version of SharePoint that you want your add-in to target?</span></span> <span data-ttu-id="4de1f-173">[X] S **harePoint-Online**を選択します。</span><span class="sxs-lookup"><span data-stu-id="4de1f-173">Choose [X] S **harePoint-Online**.</span></span> 
    
2. <span data-ttu-id="4de1f-174">**[完了]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4de1f-174">Click **Finish**.</span></span> 
    
<span data-ttu-id="4de1f-175">Visual Studio によってプロジェクトが作成され、project Online サイトにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="4de1f-175">Visual Studio creates the project and accesses the Project Online site.</span></span> 
  
### <a name="enable-sideloading-on-the-project-online-site"></a><span data-ttu-id="4de1f-176">Project Online サイトでサイドローディングを有効にする</span><span class="sxs-lookup"><span data-stu-id="4de1f-176">Enable sideloading on the Project Online site</span></span>

<span data-ttu-id="4de1f-177">サイドローディングは、Project Online アドインをテストおよびデバッグするためのメカニズムです。サイドローディングには2つのスクリプトが必要です。1つは、Project Online サイトでサイドローディングを有効にする方法と、アドインのテストとデバッグを完了した後にサイドローディングを無効にするためのスクリプトです。</span><span class="sxs-lookup"><span data-stu-id="4de1f-177">Sideloading is the mechanism for testing and debugging Project Online add-ins. You need two scripts for sideloading: one to enable sideloading on your Project Online site and another to disable sideloading once you finish testing and debugging the add-in.</span></span>
  
<span data-ttu-id="4de1f-178">サイドローディングのセットアップの詳細については、「[開発者以外のサイトコレクションでアプリのサイドローディングを有効にする](https://blogs.msdn.microsoft.com/officeapps/2013/12/10/enable-app-sideloading-in-your-non-developer-site-collection/)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4de1f-178">For more information about setting up sideloading, see [Enable app SideLoading in your non-developer site collection](https://blogs.msdn.microsoft.com/officeapps/2013/12/10/enable-app-sideloading-in-your-non-developer-site-collection/).</span></span>
  
> [!NOTE]
> <span data-ttu-id="4de1f-179">サイドローディングアプリは開発/テストの機能です。</span><span class="sxs-lookup"><span data-stu-id="4de1f-179">Sideloading apps is a developer/test feature.</span></span> <span data-ttu-id="4de1f-180">これは、**運用環境での使用を目的**としたものではありません。</span><span class="sxs-lookup"><span data-stu-id="4de1f-180">It is **not intended for production use**.</span></span> <span data-ttu-id="4de1f-181">アプリを定期的にサイドロードさせないでください。または、アプリのサイドロードは、この機能を使用している時間よりも長く有効にしておきます。</span><span class="sxs-lookup"><span data-stu-id="4de1f-181">Do not sideload apps regularly, or keep app sideloading enabled for longer than you are actively using the feature.</span></span> 
  
## <a name="add-content-to-the-add-in-project"></a><span data-ttu-id="4de1f-182">アドインプロジェクトにコンテンツを追加する</span><span class="sxs-lookup"><span data-stu-id="4de1f-182">Add content to the add-in project</span></span>

<span data-ttu-id="4de1f-183">プロジェクトを作成し、デバッグ機構を設定した後、アプリにコンテンツを追加すると、次のタスクが実行されます。</span><span class="sxs-lookup"><span data-stu-id="4de1f-183">After creating a project and setting up the debugging mechanism, adding content to the app includes the following tasks:</span></span>
  
- <span data-ttu-id="4de1f-184">アプリケーションスコープの設定</span><span class="sxs-lookup"><span data-stu-id="4de1f-184">Setting the application scope</span></span>
    
- <span data-ttu-id="4de1f-185">jsom ライブラリのリンク</span><span class="sxs-lookup"><span data-stu-id="4de1f-185">Linking the JSOM library</span></span>
    
- <span data-ttu-id="4de1f-186">UI 要素をアドインに追加する</span><span class="sxs-lookup"><span data-stu-id="4de1f-186">Adding UI Elements to the add-in</span></span>
    
- <span data-ttu-id="4de1f-187">Project Online サービスを初期化して接続する</span><span class="sxs-lookup"><span data-stu-id="4de1f-187">Initializing and connecting to the Project Online service</span></span>
    
- <span data-ttu-id="4de1f-188">プロジェクトと詳細/プロパティを取得する</span><span class="sxs-lookup"><span data-stu-id="4de1f-188">Retrieving projects and details/properties</span></span>
    
- <span data-ttu-id="4de1f-189">プロジェクトの表示</span><span class="sxs-lookup"><span data-stu-id="4de1f-189">Displaying projects</span></span>
    
- <span data-ttu-id="4de1f-190">プロジェクトのタスクを表示する</span><span class="sxs-lookup"><span data-stu-id="4de1f-190">Displaying tasks for a Project</span></span>
    
<span data-ttu-id="4de1f-191">アドインプロジェクトは、多くのファイルで構成されています。</span><span class="sxs-lookup"><span data-stu-id="4de1f-191">The add-in project consists of many files.</span></span> <span data-ttu-id="4de1f-192">この例では、次のファイルを編集する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4de1f-192">In this example, you'll need to edit the following files:</span></span> 
  
- <span data-ttu-id="4de1f-193">appmanifest.xml</span><span class="sxs-lookup"><span data-stu-id="4de1f-193">AppManifest.xml</span></span>
    
- <span data-ttu-id="4de1f-194">default.aspx</span><span class="sxs-lookup"><span data-stu-id="4de1f-194">Default.aspx</span></span>
    
- <span data-ttu-id="4de1f-195">アプリケーション .js</span><span class="sxs-lookup"><span data-stu-id="4de1f-195">App.js</span></span>
    
- <span data-ttu-id="4de1f-196">app.xaml-省略可能。アドイン用に開発されたスタイル定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4de1f-196">App.css - optional; contains style definitions developed for the add-in</span></span>
    
<span data-ttu-id="4de1f-197">試用版からサブスクリプションサイトへの移動など、project Online テナントの変更によっては、[プロパティ] ウィンドウ\*\*\*\* > を使用して、サーバー接続やサイトの URL など、プロジェクトのプロパティを更新できます。**Window**コマンド</span><span class="sxs-lookup"><span data-stu-id="4de1f-197">If the Project Online tenant changes, such as moving from a trial to a subscription site, you can update the project properties, including the Server Connection and Site URL, using the Properties Window available through the **View** > **Properties Window** command.</span></span> 
  
<span data-ttu-id="4de1f-198">プロジェクトにファイルを追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="4de1f-198">You can also add files to the project.</span></span> <span data-ttu-id="4de1f-199">その場合は、同じグループ (コンテンツ、画像、ページ、またはスクリプト) にある要素の .xml ファイルを更新して、新しいファイルを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="4de1f-199">If so, you'll need to update the Elements.xml file located in the same group (Content, Images, Pages, or Scripts) to include the new files.</span></span> <span data-ttu-id="4de1f-200">プロジェクトファイルの詳細については、「 [SharePoint アドインのアプリマニフェスト構造とパッケージを調査](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/explore-the-app-manifest-structure-and-the-package-of-a-sharepoint-add-in)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4de1f-200">For more information about the project files, see [Explore the app manifest structure and the package of a SharePoint Add-in](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/explore-the-app-manifest-structure-and-the-package-of-a-sharepoint-add-in).</span></span>
  
### <a name="set-application-scope"></a><span data-ttu-id="4de1f-201">アプリケーションスコープの設定</span><span class="sxs-lookup"><span data-stu-id="4de1f-201">Set application scope</span></span>

<span data-ttu-id="4de1f-202">このアドインには、サービスがクエリ結果に情報を返す前に定義されたスコープまたはアクセス許可レベルが必要です。</span><span class="sxs-lookup"><span data-stu-id="4de1f-202">The add-in needs scope or permission levels defined before the service returns information in query results.</span></span> <span data-ttu-id="4de1f-203">このアドインでは、Visual Studio プロジェクトに対して次のスコープを使用します。</span><span class="sxs-lookup"><span data-stu-id="4de1f-203">For this add-in, use the following scope to the Visual Studio project.</span></span> <span data-ttu-id="4de1f-204">この変更は、[アクセス許可] タブの appmanifest.xml ファイルに対して行われます。</span><span class="sxs-lookup"><span data-stu-id="4de1f-204">This change is made to the AppManifest.xml file in the Permissions tab:</span></span>

|<span data-ttu-id="4de1f-205">Scope</span><span class="sxs-lookup"><span data-stu-id="4de1f-205">Scope</span></span>|<span data-ttu-id="4de1f-206">アクセス許可</span><span class="sxs-lookup"><span data-stu-id="4de1f-206">Permission</span></span>|
|:-----|:-----|
|<span data-ttu-id="4de1f-207">複数のプロジェクト (Project Server)</span><span class="sxs-lookup"><span data-stu-id="4de1f-207">Multiple Projects (Project Server)</span></span>  <br/> |<span data-ttu-id="4de1f-208">読み取り</span><span class="sxs-lookup"><span data-stu-id="4de1f-208">Read</span></span>  <br/> |
   
<span data-ttu-id="4de1f-209">アプリケーションスコープを設定した後、ファイルを保存します。</span><span class="sxs-lookup"><span data-stu-id="4de1f-209">Save the file after setting the application scope.</span></span> <span data-ttu-id="4de1f-210">それ以外の場合、サービスからデータは返されません。</span><span class="sxs-lookup"><span data-stu-id="4de1f-210">Otherwise, no data will be returned from the service.</span></span> 
  
### <a name="link-the-jsom-library"></a><span data-ttu-id="4de1f-211">jsom ライブラリをリンクする</span><span class="sxs-lookup"><span data-stu-id="4de1f-211">Link the JSOM library</span></span>

<span data-ttu-id="4de1f-212">実行時の project online ライブラリ (js および .ps) は project online で提供されており、常に最新のバージョンです。</span><span class="sxs-lookup"><span data-stu-id="4de1f-212">The runtime Project Online libraries, PS.js and PS.debug.js, are provided by Project Online and are always the most recent version.</span></span> <span data-ttu-id="4de1f-213">jsom を使用する JavaScript アドインは、これらのライブラリのいずれかとリンクする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4de1f-213">JavaScript add-ins that use JSOM must link with one of these libraries.</span></span> <span data-ttu-id="4de1f-214">リンク定義が default.aspx ファイルに追加されます。</span><span class="sxs-lookup"><span data-stu-id="4de1f-214">The linking definitions are added in the Default.aspx file.</span></span> <span data-ttu-id="4de1f-215">.js または pcl を使用するためのコマンドは、app.config ファイルにあるコードに含まれています。</span><span class="sxs-lookup"><span data-stu-id="4de1f-215">The commands to use the PS.js and/or PS.debug.js are part of the code located in the App.js file.</span></span>
  
<span data-ttu-id="4de1f-216">次のコマンドを、node.js の「SharePoint: scriptlink」の後にある`<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead"`要素に追加して、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="4de1f-216">Add the following command for PS.js or PS.debug.js definition in the  `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` element following the "SharePoint:ScriptLink" for sp.js.</span></span> 
  
```js
<SharePoint:ScriptLink name="PS.js" runat="server" OnDemand="false" LoadAfterUI="true" Localizable="false" />
```

> [!NOTE]
> <span data-ttu-id="4de1f-217">この場合、-js または-.js の**OnDemand**属性は**false**に設定されます。</span><span class="sxs-lookup"><span data-stu-id="4de1f-217">The **OnDemand** attribute for PS.js or PS.debug.js set to **false**.</span></span> 
  
### <a name="add-ui-elements-to-the-add-in"></a><span data-ttu-id="4de1f-218">UI 要素をアドインに追加する</span><span class="sxs-lookup"><span data-stu-id="4de1f-218">Add UI elements to the add-in</span></span>

<span data-ttu-id="4de1f-219">サンプルアドインは、いくつかのコンポーネントで構成されています。</span><span class="sxs-lookup"><span data-stu-id="4de1f-219">The example add-in consists of a few components.</span></span> <span data-ttu-id="4de1f-220">静的要素の説明は、default.aspx ファイルにあります。</span><span class="sxs-lookup"><span data-stu-id="4de1f-220">Static element descriptions are located in the Default.aspx file.</span></span> <span data-ttu-id="4de1f-221">すべてのコンポーネントの動的な要素の記述とコードは、アプリケーション .js ファイルにあります。</span><span class="sxs-lookup"><span data-stu-id="4de1f-221">Dynamic element descriptions and code for all components are located in the App.js file.</span></span> <span data-ttu-id="4de1f-222">コンポーネントに関するコメントについては、ソースコードの一覧を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4de1f-222">For comments regarding the components, refer to the source code listings.</span></span> <span data-ttu-id="4de1f-223">次に、アドインの UI コンポーネントの一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="4de1f-223">Here is a list of the UI components in the add-in:</span></span>
  
- <span data-ttu-id="4de1f-224">タイトル</span><span class="sxs-lookup"><span data-stu-id="4de1f-224">Title</span></span>
    
- <span data-ttu-id="4de1f-225">導入の説明</span><span class="sxs-lookup"><span data-stu-id="4de1f-225">Introductory verbiage</span></span>
    
- <span data-ttu-id="4de1f-226">テーブルからタスクを削除するボタン</span><span class="sxs-lookup"><span data-stu-id="4de1f-226">Button to remove tasks from the table</span></span>
    
- <span data-ttu-id="4de1f-227">プロジェクト ID と名前、およびタスク情報を一覧表示する表。</span><span class="sxs-lookup"><span data-stu-id="4de1f-227">Table that lists the project ID and name, and the task information.</span></span>
    
- <span data-ttu-id="4de1f-228">[タスク] ボタン (プロジェクトごとに1回複製されます)。タスクデータをテーブルにインポートします。</span><span class="sxs-lookup"><span data-stu-id="4de1f-228">Tasks Button (cloned once for each project) that imports task data into the table.</span></span>
    
<span data-ttu-id="4de1f-229">ユーザーインターフェイスの詳細 (プロジェクトテーブルのタイトル、ヘッダー部分など) については、default.aspx プロジェクトファイルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4de1f-229">For details of the user interface, such as the title and the header portion of the project table, see the Default.aspx project file.</span></span>
  
### <a name="initialize-and-connect-to-the-host-system"></a><span data-ttu-id="4de1f-230">ホストシステムを初期化して接続する</span><span class="sxs-lookup"><span data-stu-id="4de1f-230">Initialize and connect to the host system</span></span>

<span data-ttu-id="4de1f-231">app.config ファイルには、JavaScript コードが含まれています。</span><span class="sxs-lookup"><span data-stu-id="4de1f-231">The App.js file contains the JavaScript code.</span></span> <span data-ttu-id="4de1f-232">アドインはブラウザーで .ps を読み込み、initializepage 関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4de1f-232">The add-in loads PS.js in the browser, and then calls the initializePage function.</span></span> <span data-ttu-id="4de1f-233">initializepage は、Project Online エンドポイントへのコンテキストを取得し、loadprojects 関数を開始します。</span><span class="sxs-lookup"><span data-stu-id="4de1f-233">InitializePage retrieves a context to the Project Online endpoint and starts the loadProjects function.</span></span>
  
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

### <a name="retrieve-the-projects"></a><span data-ttu-id="4de1f-234">プロジェクトを取得する</span><span class="sxs-lookup"><span data-stu-id="4de1f-234">Retrieve the projects</span></span>

<span data-ttu-id="4de1f-235">loadprojects 関数は、プロジェクト名と id のサービスを照会します。</span><span class="sxs-lookup"><span data-stu-id="4de1f-235">The loadProjects function queries the service for the project names and IDs.</span></span> 
  
<span data-ttu-id="4de1f-236">アプリケーションは、プロジェクト名とプロジェクト Id を取得します。プロジェクトに関するその他の情報は、使用可能で、load メソッドを変更して、取得するプロパティを明示的に特定することによってアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="4de1f-236">The application retrieves the project name and project Id. Other information about the project is available and can be accessed by modifying the load method to identify explicitly the properties to retrieve.</span></span> <span data-ttu-id="4de1f-237">この例は、コメントとしてコードで提供されています。</span><span class="sxs-lookup"><span data-stu-id="4de1f-237">An example is provided in the code as a comment.</span></span> 
  
<span data-ttu-id="4de1f-238">クエリが成功した場合、アドインは displayprojects を呼び出すことによって続行されます。</span><span class="sxs-lookup"><span data-stu-id="4de1f-238">If the query succeeds, the add-in continues by calling displayProjects.</span></span> 
  
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

### <a name="display-the-projects"></a><span data-ttu-id="4de1f-239">プロジェクトを表示する</span><span class="sxs-lookup"><span data-stu-id="4de1f-239">Display the projects</span></span>

<span data-ttu-id="4de1f-240">displayprojects 関数は、テーブル、プロジェクトごとに1行、および特定のプロジェクトのタスクを表示するボタンを作成します。</span><span class="sxs-lookup"><span data-stu-id="4de1f-240">The displayProjects function creates a table, one row per project, and a button to show the tasks for the specific project.</span></span> 
  
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
> <span data-ttu-id="4de1f-241">while ループは、ID プロパティと name プロパティにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="4de1f-241">The while loop accesses the ID and name properties.</span></span> <span data-ttu-id="4de1f-242">これは、同じプロパティにアクセスする関数を呼び出すソースコードプロジェクトとはわずかに異なります。</span><span class="sxs-lookup"><span data-stu-id="4de1f-242">This is slightly different than the source code project that calls a function that, in turn, accesses the same properties.</span></span> 
  
### <a name="display-the-tasks-for-a-project"></a><span data-ttu-id="4de1f-243">プロジェクトのタスクを表示する</span><span class="sxs-lookup"><span data-stu-id="4de1f-243">Display the tasks for a project</span></span>

<span data-ttu-id="4de1f-244">アドインの一部であるタスクは、最初の読み込みの一部ではありません。</span><span class="sxs-lookup"><span data-stu-id="4de1f-244">The tasks, while part of the add-in, are not part of the initial loading.</span></span> <span data-ttu-id="4de1f-245">ユーザーがプロジェクトに関連付けられているタスクに関心を持っている場合は、[タスクの表示] ボタンをクリックすると、btnloadtasks イベントハンドラーを使用してタスクが一覧に表示されます。</span><span class="sxs-lookup"><span data-stu-id="4de1f-245">If the user is interested in the tasks associated with a project, clicking the "Show Tasks" button causes the tasks to display in the list using the btnLoadTasks event handler.</span></span> 
  
<span data-ttu-id="4de1f-246">btnloadtasks イベントハンドラーは、適切なプロジェクト ID を使用して、サーバーから指定したプロジェクトのタスクを要求します。</span><span class="sxs-lookup"><span data-stu-id="4de1f-246">The btnLoadTasks event handler, with the appropriate project ID, requests the tasks for the specified project from the server.</span></span> <span data-ttu-id="4de1f-247">取得した btnloadtasks は、タスクリストを表示タスクに渡して、タスクを画面に表示します。</span><span class="sxs-lookup"><span data-stu-id="4de1f-247">Once retrieved, btnLoadTasks passes the task list to displayTasks to present the tasks onscreen.</span></span>
  
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

<span data-ttu-id="4de1f-248">displaytasks 関数は、指定したプロジェクトに関連付けられているタスクをプロジェクトエントリのすぐ下に表示します。</span><span class="sxs-lookup"><span data-stu-id="4de1f-248">The displayTasks function displays the tasks associated with a specified project immediately beneath the project entry.</span></span>
  
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
> <span data-ttu-id="4de1f-249">while ループは、タスク ID と名前のプロパティにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="4de1f-249">The while loop accesses the task ID and name properties.</span></span> <span data-ttu-id="4de1f-250">これは、同じプロパティにアクセスする関数を呼び出すソースコードプロジェクトとはわずかに異なります。</span><span class="sxs-lookup"><span data-stu-id="4de1f-250">This is slightly different than the source code project that calls a function that, in turn, accesses the same properties.</span></span> 
  
<span data-ttu-id="4de1f-251">1つのプロジェクトのタスクの出力例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="4de1f-251">Sample output for the tasks of a single project follows.</span></span>
  
<span data-ttu-id="4de1f-252">![プロジェクトタスクの出力を示すスクリーンショット](media/f6500a3f-000b-4f3e-9be6-9a74d0bea15e.png "プロジェクトタスクの出力を示すスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="4de1f-252">![Screen shot showing the output for a project task](media/f6500a3f-000b-4f3e-9be6-9a74d0bea15e.png "Screen shot showing the output for a project task")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4de1f-253">関連項目</span><span class="sxs-lookup"><span data-stu-id="4de1f-253">See also</span></span>

<span data-ttu-id="4de1f-254">Project Online および CSOM を使用したアプリケーション開発に関するドキュメントとサンプルについては、[Project 開発ポータル](https://developer.microsoft.com/en-us/project)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="4de1f-254">For documentation and samples related to Project Online and application development using CSOM, see the [Project Development Portal](https://developer.microsoft.com/en-us/project).</span></span>
    


