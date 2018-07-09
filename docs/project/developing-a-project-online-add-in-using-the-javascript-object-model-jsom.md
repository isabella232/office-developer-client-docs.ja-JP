---
title: プロジェクトのオンライン追加の JavaScript オブジェクト モデル (JSOM) を使用して開発
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4a4b1ad2-de46-421d-a698-53c20c90b93a
description: この資料では、オンラインのプロジェクトと、利便性を強化するためにプロジェクトをオンラインでマイクロソフトのアドインを開発について説明します。 開発プロジェクトは、チュートリアルとして実装されます。 アドインをこの資料の使用しプロジェクト名とプロジェクトのオンライン アカウントから発行されたプロジェクトの Id が表示されますを読み込んで使用すると、個々 のプロジェクトに関連付けられている取得タスクへのドリル ダウンします。
ms.openlocfilehash: 91d475afd5c4085b00ed06b66620f0d18174fd7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804551"
---
# <a name="developing-a-project-online-add-in-using-the-javascript-object-model-jsom"></a><span data-ttu-id="b3a04-105">プロジェクトのオンライン追加の JavaScript オブジェクト モデル (JSOM) を使用して開発</span><span class="sxs-lookup"><span data-stu-id="b3a04-105">Developing a Project Online add-in using the JavaScript Object Model (JSOM)</span></span>

<span data-ttu-id="b3a04-106">プロジェクト オンラインと、利便性を強化するためにプロジェクトをオンラインでマイクロソフトのアドインの開発について説明します。</span><span class="sxs-lookup"><span data-stu-id="b3a04-106">This article describes Microsoft Project Online Add-in development to enhance your experience with the Project Online.</span></span> <span data-ttu-id="b3a04-107">開発プロジェクトは、チュートリアルとして実装されます。</span><span class="sxs-lookup"><span data-stu-id="b3a04-107">The development project is implemented as a walkthrough.</span></span> <span data-ttu-id="b3a04-108">アドインをこの資料の使用しプロジェクト名とプロジェクトのオンライン アカウントから発行されたプロジェクトの Id が表示されますを読み込んで使用すると、個々 のプロジェクトに関連付けられている取得タスクへのドリル ダウンします。</span><span class="sxs-lookup"><span data-stu-id="b3a04-108">The add-in used for this article reads and displays the project names and IDs of the published projects from your Project Online account and allows you to drill down to retrieve tasks associated with individual projects.</span></span>
  
<span data-ttu-id="b3a04-109">実行時に、アドインの一覧は次の次の図に似ています。</span><span class="sxs-lookup"><span data-stu-id="b3a04-109">At run time, the add-in listing looks similar to the following illustration:</span></span>
  
<span data-ttu-id="b3a04-110">![スクリーン ショットは、JSOM プロジェクトとタスクの一覧を表示](media/766e5914-f048-48f4-9282-291f55e6e90d.png "スクリーン ショットは、JSOM プロジェクトとタスクの一覧を表示")</span><span class="sxs-lookup"><span data-stu-id="b3a04-110">![Screen shot showing a listing of JSOM projects and tasks](media/766e5914-f048-48f4-9282-291f55e6e90d.png "Screen shot showing a listing of JSOM projects and tasks")</span></span>
  
<span data-ttu-id="b3a04-111">この例の目的は、プロジェクト オンラインでクエリを実行して、サービスからの各要求のコンテキストを設定するとの相互作用です。</span><span class="sxs-lookup"><span data-stu-id="b3a04-111">The focus of the example is the interaction with the Project Online, making queries and setting the context for each request from the service.</span></span> <span data-ttu-id="b3a04-112">ユーザー インターフェイス (UI) 要素には、最低限の注意が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b3a04-112">User interface (UI) elements receive minimal attention.</span></span> <span data-ttu-id="b3a04-113">代わりに、ソースの一覧では、UI に関するコメントを提供します。</span><span class="sxs-lookup"><span data-stu-id="b3a04-113">Instead, the source listings provide comments regarding the UI.</span></span>
  
> [!NOTE]
> <span data-ttu-id="b3a04-114">例のアドインで、Visual Studio プロジェクトのソース ファイルがある: https://github.com/OfficeDev/Project-JSOM-List-Projects-Tasks....。</span><span class="sxs-lookup"><span data-stu-id="b3a04-114">The source files for the example add-in, a Visual Studio project, are available at: https://github.com/OfficeDev/Project-JSOM-List-Projects-Tasks.....</span></span> <span data-ttu-id="b3a04-115">手元ソース ファイルの参照として、資料を参照するときにそれぞれを補完するもの、もう一方に。</span><span class="sxs-lookup"><span data-stu-id="b3a04-115">Keep the source files handy as a reference while you read the article, as each complements the other.</span></span> <span data-ttu-id="b3a04-116">Visual Studio 内のファイルがプロジェクトのビルドとは、最小限の変更を実行可能: PWA のフォルダーに、プロジェクトのオンラインのテナントの代わりに、URL です。</span><span class="sxs-lookup"><span data-stu-id="b3a04-116">The files in the Visual Studio project build and are executable with minimal changes—substituting the URL for your Project Online tenant down to the PWA folder.</span></span> 
  
## <a name="background"></a><span data-ttu-id="b3a04-117">背景</span><span class="sxs-lookup"><span data-stu-id="b3a04-117">Background</span></span>

<span data-ttu-id="b3a04-118">オンラインのプロジェクトは、プロジェクト ポートフォリオ管理 (PPM) と調整し、ポートフォリオ、プログラム、およびプロジェクトを管理するプロジェクト管理オフィス (PMO) のソリューションを企業に提供している Office 365 サービスです。</span><span class="sxs-lookup"><span data-stu-id="b3a04-118">Project Online is a Office 365 service that provides companies with a project portfolio management (PPM) and project management office (PMO) solution to coordinate and manage portfolios, programs, and projects.</span></span> <span data-ttu-id="b3a04-119">オンラインのプロジェクトは、プロジェクトのデスクトップ エディションによりさまざまな製品まだ、オンライン プロジェクトも含まれていますを維持し、プロジェクトのライフ サイクル全体にわたってプロジェクトの詳細を追跡する機能。</span><span class="sxs-lookup"><span data-stu-id="b3a04-119">Project Online is a different offering than the Project desktop editions; yet, Project Online still contains the functionality to maintain and track project details throughout the life of a project.</span></span> <span data-ttu-id="b3a04-120">SharePoint Online のオンラインのプロジェクトがビルドされます。</span><span class="sxs-lookup"><span data-stu-id="b3a04-120">Project Online is built on SharePoint Online.</span></span>
  
<span data-ttu-id="b3a04-121">プロジェクト オンライン ホストされている追加のクライアント側オブジェクト モデル API とやり取りする JavaScript とリソース ・ ファイルで構成されます。</span><span class="sxs-lookup"><span data-stu-id="b3a04-121">A Project Online hosted add-in consists of JavaScript and resource files that interact with the Client-Side-Object-Model API.</span></span> <span data-ttu-id="b3a04-122">アドインをユーザーが訪問した、JavaScript とリソースがダウンロードされ、ブラウザー内で実行されます。</span><span class="sxs-lookup"><span data-stu-id="b3a04-122">When the user visits the add-in, the JavaScript and resources are downloaded and executed within the browser.</span></span> <span data-ttu-id="b3a04-123">アドイン プロジェクトをオンラインにする非同期の呼び出しは、サービスとの対話の作成、取得、更新、またはデータを削除するかどうかは、します。</span><span class="sxs-lookup"><span data-stu-id="b3a04-123">The add-In makes asynchronous calls to Project Online to interact with the service, whether creating, retrieving, updating, or deleting data.</span></span> 
  
<span data-ttu-id="b3a04-124">オンラインのプロジェクトは、アドインから他のテナントに属する情報を保護するために複数のアクションを 1 つを実行します。つまり、アドインからの要求と対話する、独立したサイトの作成はプロジェクトのオンラインのようにします。</span><span class="sxs-lookup"><span data-stu-id="b3a04-124">Project Online performs one more action to protect information that belongs to other tenants from the add-in; namely, Project Online creates an isolated site to interact with the requests from the add-in.</span></span> <span data-ttu-id="b3a04-125">オンライン プロジェクトのホストでは、カスタム コードが実行されません。</span><span class="sxs-lookup"><span data-stu-id="b3a04-125">No custom code runs on the Project Online host.</span></span> 
  
<span data-ttu-id="b3a04-126">オンライン プロジェクトのアドインの開発のセットアップでは、Visual Studio SharePoint アドイン プロジェクトの種類を使用します。</span><span class="sxs-lookup"><span data-stu-id="b3a04-126">The development setup for Project Online add-ins uses the Visual Studio SharePoint Add-in project type.</span></span> <span data-ttu-id="b3a04-127">アドインが、JavaScript で記述され、プロジェクトの JavaScript オブジェクト モデル (JSOM) を使用して、プロジェクトのオンライン サービスと対話します。</span><span class="sxs-lookup"><span data-stu-id="b3a04-127">The add-in is written in JavaScript, and uses the Project JavaScript object model (JSOM) to interact with the Project Online service.</span></span> <span data-ttu-id="b3a04-128">JSOM では、SharePoint の JSOM からの機能の多くを継承します。</span><span class="sxs-lookup"><span data-stu-id="b3a04-128">The JSOM inherits much of its functionality from the SharePoint JSOM.</span></span>
  
> [!NOTE]
> <span data-ttu-id="b3a04-129">アドインの発行し Office ストアで販売または SharePoint 上のプライベート アプリケーション カタログに配置できます。</span><span class="sxs-lookup"><span data-stu-id="b3a04-129">Add-ins can be published and sold in the Office Store or deployed to a private app catalog on SharePoint.</span></span> <span data-ttu-id="b3a04-130">詳細についてを参照してください[の展開、Office アドインを発行し、](http://dev.office.com/docs/add-ins/publish/publish.aspx)。</span><span class="sxs-lookup"><span data-stu-id="b3a04-130">For more information, see [Deploy and publish your Office Add-in](http://dev.office.com/docs/add-ins/publish/publish.aspx).</span></span> <span data-ttu-id="b3a04-131">> アドインをこの資料では、開発者のためのサンプル実稼働環境で使用するためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="b3a04-131">> The add-in used in this article is a sample for developers; it is not intended for use in a production environment.</span></span> <span data-ttu-id="b3a04-132">主な目的では、オンラインのプロジェクトのアプリケーション開発の例を示します。</span><span class="sxs-lookup"><span data-stu-id="b3a04-132">The primary purpose is to show an example of app development for Project Online.</span></span> 
  
## <a name="prerequisites"></a><span data-ttu-id="b3a04-133">前提条件</span><span class="sxs-lookup"><span data-stu-id="b3a04-133">Prerequisites</span></span>

<span data-ttu-id="b3a04-134">サポートされている Windows 環境には、次の項目を追加します。</span><span class="sxs-lookup"><span data-stu-id="b3a04-134">Add the following items to a supported Windows environment:</span></span>
  
- <span data-ttu-id="b3a04-135">**4.0 またはそれ以降の.NET Framework**: バージョン 4.0 フレームワークの完全なバージョンに互換性がします。</span><span class="sxs-lookup"><span data-stu-id="b3a04-135">**.NET Framework 4.0 or later**: Complete versions of the framework from version 4.0 are compatible.</span></span> <span data-ttu-id="b3a04-136">ダウンロード サイトは、 https://msdn.microsoft.com/en-us/vstudio/aa496123.aspx。</span><span class="sxs-lookup"><span data-stu-id="b3a04-136">The download site is https://msdn.microsoft.com/en-us/vstudio/aa496123.aspx.</span></span>
    
- <span data-ttu-id="b3a04-137">**2013 またはそれ以降の Visual Studio の**。</span><span class="sxs-lookup"><span data-stu-id="b3a04-137">**Visual Studio 2013 or later**:</span></span>  
    
   - <span data-ttu-id="b3a04-138">Visual Studio 2015 のプロフェッショナル ・ エディションはアウト - 標準の準備が、使用にhttps://www.visualstudio.com/en-us/products/visual-studio-professional-with-msdn-vs.aspx。</span><span class="sxs-lookup"><span data-stu-id="b3a04-138">The professional edition of Visual Studio 2015 is ready to go out-of-the box and is available at https://www.visualstudio.com/en-us/products/visual-studio-professional-with-msdn-vs.aspx.</span></span>
    
   - <span data-ttu-id="b3a04-139">Visual Studio 2015 の community edition は、 https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx。</span><span class="sxs-lookup"><span data-stu-id="b3a04-139">The community edition of Visual Studio 2015 is available at https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx.</span></span> <span data-ttu-id="b3a04-140">このエディションには、Visual Studio の Microsoft Office の開発ツールを手動でインストールが必要です。</span><span class="sxs-lookup"><span data-stu-id="b3a04-140">This edition requires manual installation of the Microsoft Office Developer Tools for Visual Studio.</span></span>
    
   <span data-ttu-id="b3a04-141">Visual Studio 用の Microsoft Office 開発ツールは、 https://www.visualstudio.com/en-us/features/office-tools-vs.aspx。</span><span class="sxs-lookup"><span data-stu-id="b3a04-141">The Microsoft Office Developer Tools for Visual Studio are available at https://www.visualstudio.com/en-us/features/office-tools-vs.aspx.</span></span>
    
- <span data-ttu-id="b3a04-142">**A プロジェクト オンライン アカウント**: これは、ホスティング サービスへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="b3a04-142">**A Project Online account**: This provides access to the hosting service.</span></span> <span data-ttu-id="b3a04-143">プロジェクトのオンライン アカウントを取得する方法についてを参照してくださいhttps://products.office.com/en-us/Project/project-online-portfolio-management。</span><span class="sxs-lookup"><span data-stu-id="b3a04-143">For more information about obtaining a Project Online account, see https://products.office.com/en-us/Project/project-online-portfolio-management.</span></span>
    
   <span data-ttu-id="b3a04-144">アドインのユーザーがプロジェクトのオンラインのテナントのいくつかのプロジェクトにアクセスするための十分な権限を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b3a04-144">Ensure that the add-in user has sufficient authorization to access some projects in the Project Online tenant.</span></span> 
    
- <span data-ttu-id="b3a04-145">**ホスト サイト上のプロジェクト**情報が挿入されます。</span><span class="sxs-lookup"><span data-stu-id="b3a04-145">**Projects on the hosting site** that are populated with information.</span></span>
    
> [!NOTE]
> <span data-ttu-id="b3a04-146">標準の.NET Framework は、使用する正しいフレームワークです。</span><span class="sxs-lookup"><span data-stu-id="b3a04-146">The standard .NET Framework is the correct framework to use.</span></span> <span data-ttu-id="b3a04-147">[.NET Framework 4 クライアント プロファイル] を使用することはしません。</span><span class="sxs-lookup"><span data-stu-id="b3a04-147">Do not use the ".NET Framework 4 Client Profile".</span></span> 
  
### <a name="set-up-the-visual-studio-project"></a><span data-ttu-id="b3a04-148">Visual Studio プロジェクトを設定します</span><span class="sxs-lookup"><span data-stu-id="b3a04-148">Set up the Visual Studio project</span></span>

<span data-ttu-id="b3a04-149">アプリケーションのセットアップは、新しいプロジェクトを作成する、適切なライブラリとリンク、および必要な名前空間を宣言することで構成されます。</span><span class="sxs-lookup"><span data-stu-id="b3a04-149">The application setup consists of creating a new project, linking the appropriate libraries and declaring the needed namespaces.</span></span> <span data-ttu-id="b3a04-150">Visual Studio には、いくつかの種類の開発プロジェクトが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b3a04-150">Visual Studio presents several types of development projects.</span></span> <span data-ttu-id="b3a04-151">セクションとは、簡単な非常に基本的なです。</span><span class="sxs-lookup"><span data-stu-id="b3a04-151">The section is brief and very basic.</span></span> <span data-ttu-id="b3a04-152">値の情報がある 1 つの場所に統合します。</span><span class="sxs-lookup"><span data-stu-id="b3a04-152">The value is having the information is coalesced in one place.</span></span>
  
#### <a name="select-a-visual-studio-project"></a><span data-ttu-id="b3a04-153">Visual Studio プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="b3a04-153">Select a Visual Studio project</span></span>

<span data-ttu-id="b3a04-154">アドインの適切な種類のプロジェクトを作成するには、次の手順を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3a04-154">To create a project of the appropriate type for the add-in, you must do the following steps.</span></span> <span data-ttu-id="b3a04-155">画面上で発生するキーワードは、**太字**属性を持ちます。</span><span class="sxs-lookup"><span data-stu-id="b3a04-155">Keywords encountered on the screen have a **bold** attribute:</span></span> 
  
1. <span data-ttu-id="b3a04-156">[ファイル] メニューから**ファイル**を選択して > **新規** > **プロジェクト**。</span><span class="sxs-lookup"><span data-stu-id="b3a04-156">From the File menu, choose **File** > **New** > **Project**.</span></span> 
    
2. <span data-ttu-id="b3a04-157">左側のウィンドウでインストールされたテンプレート] から選択して**C#** > **Office**SharePoint/ > **Web アドイン**です。</span><span class="sxs-lookup"><span data-stu-id="b3a04-157">From the Installed templates in the left pane, select **C#** > **Office/SharePoint** > **Web Add-ins**.</span></span> 
    
3. <span data-ttu-id="b3a04-158">中央のウィンドウの上部には、 **.NET Framework 4**を選択またはそれ以降です。4.6 を現在のバージョンには。</span><span class="sxs-lookup"><span data-stu-id="b3a04-158">At the top of the central pane, select **.NET Framework 4** or later; the current version is 4.6.</span></span> 
    
4. <span data-ttu-id="b3a04-159">中央のウィンドウでアプリケーションの種類を**SharePoint のアドインを**選択します。</span><span class="sxs-lookup"><span data-stu-id="b3a04-159">From the application types in the central pane, choose **SharePoint Add-in**.</span></span> 
    
5. <span data-ttu-id="b3a04-160">下部のセクションで、プロジェクトとソリューション名の場所と名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="b3a04-160">In the bottom section, specify a name and location for the project, and a solution name.</span></span> 
    
6. <span data-ttu-id="b3a04-161">下部のセクションで、**ソリューションのディレクトリを作成**チェック ボックスをオンします。</span><span class="sxs-lookup"><span data-stu-id="b3a04-161">Also in the bottom section, check the **Create directory for solution** box.</span></span> 
    
7. <span data-ttu-id="b3a04-162">初期プロジェクトを作成するのには **[ok]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3a04-162">Click **OK** to create the initial project.</span></span> 
    
<span data-ttu-id="b3a04-163">Visual Studio のウィザードは、以下のダイアログのいくつかのオンライン プロジェクトの設定サイト (と呼ばれる SharePoint 設定ダイアログ ボックス内) に関するフォロー アップの質問をいくつかを要求します。</span><span class="sxs-lookup"><span data-stu-id="b3a04-163">The Visual Studio Wizard asks a few follow-up questions about the Project Online settings site (called SharePoint settings in the dialogs) in a couple of dialogs that follow.</span></span> <span data-ttu-id="b3a04-164">質問を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="b3a04-164">Here are the questions:</span></span>
  
1. <span data-ttu-id="b3a04-165">SharePoint サイトはどのようなアドインをデバッグに使用しますか。</span><span class="sxs-lookup"><span data-stu-id="b3a04-165">What SharePoint site do you want to use for debugging your add-in?</span></span> <span data-ttu-id="b3a04-166">PWA サイトの URL を指定して次のようにhttps://contoso.sharepoint.com/sites/pwa。</span><span class="sxs-lookup"><span data-stu-id="b3a04-166">Specify the URL to your PWA site, such as https://contoso.sharepoint.com/sites/pwa.</span></span>
    
2. <span data-ttu-id="b3a04-167">SharePoint で、アドインをホストする方法を指定しますか。</span><span class="sxs-lookup"><span data-stu-id="b3a04-167">How do you want to host your SharePoint Add-in?</span></span> <span data-ttu-id="b3a04-168">[X] を選択して**SharePoint でホストされています**。</span><span class="sxs-lookup"><span data-stu-id="b3a04-168">Choose [X] **SharePoint-hosted**.</span></span>
    
   <span data-ttu-id="b3a04-169">SharePoint アドインに関する詳細については、ホスティングなどのオプションでは、 [SharePoint のアドイン](https://docs.microsoft.com/en-us/sharepoint/dev/sp-add-ins/sharepoint-add-ins)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b3a04-169">For more information about SharePoint Add-ins, including hosting options, see [SharePoint Add-ins](https://docs.microsoft.com/en-us/sharepoint/dev/sp-add-ins/sharepoint-add-ins).</span></span>
    
3. <span data-ttu-id="b3a04-170">[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3a04-170">Click **Next**.</span></span> 
    
<span data-ttu-id="b3a04-171">アドインの SharePoint のオンライン バージョンを指定する 2 つ目の追加のダイアログが表示されたら。</span><span class="sxs-lookup"><span data-stu-id="b3a04-171">The second additional dialog asks you to specify the SharePoint Online version for the add-in:</span></span> 
  
1. <span data-ttu-id="b3a04-172">対象とするように追加する SharePoint の最も古いバージョンとは何ですか。</span><span class="sxs-lookup"><span data-stu-id="b3a04-172">What's the earliest version of SharePoint that you want your add-in to target?</span></span> <span data-ttu-id="b3a04-173">[X] を選択して S **harePoint オンライン**。</span><span class="sxs-lookup"><span data-stu-id="b3a04-173">Choose [X] S **harePoint-Online**.</span></span> 
    
2. <span data-ttu-id="b3a04-174">[ **完了**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3a04-174">Click **Finish**.</span></span> 
    
<span data-ttu-id="b3a04-175">Visual Studio は、プロジェクトが作成され、プロジェクトのオンライン サイトにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="b3a04-175">Visual Studio creates the project and accesses the Project Online site.</span></span> 
  
### <a name="enable-sideloading-on-the-project-online-site"></a><span data-ttu-id="b3a04-176">プロジェクトのオンライン サイト上の sideloading を有効にします。</span><span class="sxs-lookup"><span data-stu-id="b3a04-176">Enable sideloading on the Project Online site</span></span>

<span data-ttu-id="b3a04-177">Sideloading は、テストとオンライン プロジェクトのアドインをデバッグするための機構です。Sideloading の 2 つのスクリプトが必要があります: テストおよびアドインのデバッグが完了したら、sideloading を無効にする別のプロジェクトのオンライン サイトで sideloading を有効にする 1 つ。</span><span class="sxs-lookup"><span data-stu-id="b3a04-177">Sideloading is the mechanism for testing and debugging Project Online add-ins. You need two scripts for sideloading: one to enable sideloading on your Project Online site and another to disable sideloading once you finish testing and debugging the add-in.</span></span>
  
<span data-ttu-id="b3a04-178">Sideloading を設定する方法の詳細については、[アプリケーション開発者以外のサイト コレクション内の SideLoading を有効にする](https://blogs.msdn.microsoft.com/officeapps/2013/12/10/enable-app-sideloading-in-your-non-developer-site-collection/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b3a04-178">For more information about setting up sideloading, see [Enable app SideLoading in your non-developer site collection](https://blogs.msdn.microsoft.com/officeapps/2013/12/10/enable-app-sideloading-in-your-non-developer-site-collection/).</span></span>
  
> [!NOTE]
> <span data-ttu-id="b3a04-179">Sideloading アプリケーションは、開発者とテスト機能です。</span><span class="sxs-lookup"><span data-stu-id="b3a04-179">Sideloading apps is a developer/test feature.</span></span> <span data-ttu-id="b3a04-180">**運用環境で使用しない目的**があります。</span><span class="sxs-lookup"><span data-stu-id="b3a04-180">It is **not intended for production use**.</span></span> <span data-ttu-id="b3a04-181">Sideload アプリケーションではありませんを定期的に行うか、機能を使用してアクティブにするよりも長時間の有効なアプリケーションの sideloading を維持します。</span><span class="sxs-lookup"><span data-stu-id="b3a04-181">Do not sideload apps regularly, or keep app sideloading enabled for longer than you are actively using the feature.</span></span> 
  
## <a name="add-content-to-the-add-in-project"></a><span data-ttu-id="b3a04-182">アドイン プロジェクトにコンテンツを追加します。</span><span class="sxs-lookup"><span data-stu-id="b3a04-182">Add content to the add-in project</span></span>

<span data-ttu-id="b3a04-183">プロジェクトを作成すると、デバッグの機構を設定する、アプリケーションにコンテンツを追加する次のタスクが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b3a04-183">After creating a project and setting up the debugging mechanism, adding content to the app includes the following tasks:</span></span>
  
- <span data-ttu-id="b3a04-184">アプリケーション スコープの設定</span><span class="sxs-lookup"><span data-stu-id="b3a04-184">Setting the application scope</span></span>
    
- <span data-ttu-id="b3a04-185">JSOM ライブラリをリンク</span><span class="sxs-lookup"><span data-stu-id="b3a04-185">Linking the JSOM library</span></span>
    
- <span data-ttu-id="b3a04-186">アドインに UI 要素を追加します。</span><span class="sxs-lookup"><span data-stu-id="b3a04-186">Adding UI Elements to the add-in</span></span>
    
- <span data-ttu-id="b3a04-187">初期化し、プロジェクトのオンライン サービスに接続します。</span><span class="sxs-lookup"><span data-stu-id="b3a04-187">Initializing and connecting to the Project Online service</span></span>
    
- <span data-ttu-id="b3a04-188">プロジェクトとの詳細とプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="b3a04-188">Retrieving projects and details/properties</span></span>
    
- <span data-ttu-id="b3a04-189">プロジェクトを表示します。</span><span class="sxs-lookup"><span data-stu-id="b3a04-189">Displaying projects</span></span>
    
- <span data-ttu-id="b3a04-190">プロジェクトのタスクを表示します。</span><span class="sxs-lookup"><span data-stu-id="b3a04-190">Displaying tasks for a Project</span></span>
    
<span data-ttu-id="b3a04-191">アドイン プロジェクトでは、多数のファイルで構成されます。</span><span class="sxs-lookup"><span data-stu-id="b3a04-191">The add-in project consists of many files.</span></span> <span data-ttu-id="b3a04-192">この例では、以下のファイルを編集する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3a04-192">In this example, you'll need to edit the following files:</span></span> 
  
- <span data-ttu-id="b3a04-193">AppManifest.xml</span><span class="sxs-lookup"><span data-stu-id="b3a04-193">AppManifest.xml</span></span>
    
- <span data-ttu-id="b3a04-194">Default.aspx</span><span class="sxs-lookup"><span data-stu-id="b3a04-194">Default.aspx</span></span>
    
- <span data-ttu-id="b3a04-195">App.js</span><span class="sxs-lookup"><span data-stu-id="b3a04-195">App.js</span></span>
    
- <span data-ttu-id="b3a04-196">App.css - 省略可能です。アドイン用に開発されたスタイルの定義が含まれています</span><span class="sxs-lookup"><span data-stu-id="b3a04-196">App.css - optional; contains style definitions developed for the add-in</span></span>
    
<span data-ttu-id="b3a04-197">移動など試用版からサブスクリプションのサイトでは、サーバー間の接続およびサイトの URL を含む、プロジェクトのプロパティを更新することができます、プロジェクトのオンラインのテナントが変更された場合は、[プロパティ] ウィンドウ**のビュー**で利用可能なを使用して > **のプロパティウィンドウ**コマンドです。</span><span class="sxs-lookup"><span data-stu-id="b3a04-197">If the Project Online tenant changes, such as moving from a trial to a subscription site, you can update the project properties, including the Server Connection and Site URL, using the Properties Window available through the **View** > **Properties Window** command.</span></span> 
  
<span data-ttu-id="b3a04-198">プロジェクトにファイルを追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="b3a04-198">You can also add files to the project.</span></span> <span data-ttu-id="b3a04-199">その場合は、(コンテンツ、イメージ、ページ、またはスクリプト) を新しいファイルを含めるには、同じグループ内にある、Elements.xml ファイルを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3a04-199">If so, you'll need to update the Elements.xml file located in the same group (Content, Images, Pages, or Scripts) to include the new files.</span></span> <span data-ttu-id="b3a04-200">プロジェクト ファイルの詳細については、 [SharePoint アドインのパッケージとアプリケーション マニフェストの構造を表示する](https://msdn.microsoft.com/ja-jp/library/office/fp179918.aspx.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b3a04-200">For more information about the project files, see [Explore the app manifest structure and the package of a SharePoint Add-in](https://msdn.microsoft.com/ja-jp/library/office/fp179918.aspx.aspx).</span></span>
  
### <a name="set-application-scope"></a><span data-ttu-id="b3a04-201">アプリケーション スコープの設定</span><span class="sxs-lookup"><span data-stu-id="b3a04-201">Set application scope</span></span>

<span data-ttu-id="b3a04-202">追加のサービス情報をクエリ結果に返される前に定義されたスコープまたはアクセス許可のレベルが必要です。</span><span class="sxs-lookup"><span data-stu-id="b3a04-202">The add-in needs scope or permission levels defined before the service returns information in query results.</span></span> <span data-ttu-id="b3a04-203">このアドインの場合、Visual Studio プロジェクトに次のスコープを使用します。</span><span class="sxs-lookup"><span data-stu-id="b3a04-203">For this add-in, use the following scope to the Visual Studio project.</span></span> <span data-ttu-id="b3a04-204">この変更は、AppManifest.xml ファイルを [アクセス許可] タブで使用します。</span><span class="sxs-lookup"><span data-stu-id="b3a04-204">This change is made to the AppManifest.xml file in the Permissions tab:</span></span>

|<span data-ttu-id="b3a04-205">スコープ</span><span class="sxs-lookup"><span data-stu-id="b3a04-205">Scope</span></span>|<span data-ttu-id="b3a04-206">アクセス許可</span><span class="sxs-lookup"><span data-stu-id="b3a04-206">Permission</span></span>|
|:-----|:-----|
|<span data-ttu-id="b3a04-207">複数のプロジェクト (Project Server)</span><span class="sxs-lookup"><span data-stu-id="b3a04-207">Multiple Projects (Project Server)</span></span>  <br/> |<span data-ttu-id="b3a04-208">読み取り</span><span class="sxs-lookup"><span data-stu-id="b3a04-208">Read</span></span>  <br/> |
   
<span data-ttu-id="b3a04-209">アプリケーションのスコープを設定した後、ファイルを保存します。</span><span class="sxs-lookup"><span data-stu-id="b3a04-209">Save the file after setting the application scope.</span></span> <span data-ttu-id="b3a04-210">それ以外の場合、データは返されません、サービスから。</span><span class="sxs-lookup"><span data-stu-id="b3a04-210">Otherwise, no data will be returned from the service.</span></span> 
  
### <a name="link-the-jsom-library"></a><span data-ttu-id="b3a04-211">JSOM ライブラリをリンクします。</span><span class="sxs-lookup"><span data-stu-id="b3a04-211">Link the JSOM library</span></span>

<span data-ttu-id="b3a04-212">ランタイム プロジェクト オンライン ライブラリ、PS.js、PS.debug.js は、プロジェクトをオンラインで提供されており、最新のバージョンは、常に。</span><span class="sxs-lookup"><span data-stu-id="b3a04-212">The runtime Project Online libraries, PS.js and PS.debug.js, are provided by Project Online and are always the most recent version.</span></span> <span data-ttu-id="b3a04-213">JavaScript 追加のプラグインを使用して、JSOM は、これらのライブラリのいずれかにリンクしなければなりません。</span><span class="sxs-lookup"><span data-stu-id="b3a04-213">JavaScript add-ins that use JSOM must link with one of these libraries.</span></span> <span data-ttu-id="b3a04-214">Default.aspx ファイルには、リンクの定義が追加されます。</span><span class="sxs-lookup"><span data-stu-id="b3a04-214">The linking definitions are added in the Default.aspx file.</span></span> <span data-ttu-id="b3a04-215">PS.js または PS.debug.js を使用するコマンドにあるコードの一部です。</span><span class="sxs-lookup"><span data-stu-id="b3a04-215">The commands to use the PS.js and/or PS.debug.js are part of the code located in the App.js file.</span></span>
  
<span data-ttu-id="b3a04-216">PS.js または PS.debug.js の定義については、次のコマンドを追加、 `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` sp.js の「SharePoint:ScriptLink」次の要素です。</span><span class="sxs-lookup"><span data-stu-id="b3a04-216">Add the following command for PS.js or PS.debug.js definition in the  `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` element following the "SharePoint:ScriptLink" for sp.js.</span></span> 
  
```js
<SharePoint:ScriptLink name="PS.js" runat="server" OnDemand="false" LoadAfterUI="true" Localizable="false" />
```

> [!NOTE]
> <span data-ttu-id="b3a04-217">PS.js または PS.debug.js の**オンデマンド ・** 属性が**false**に設定します。</span><span class="sxs-lookup"><span data-stu-id="b3a04-217">The **OnDemand** attribute for PS.js or PS.debug.js set to **false**.</span></span> 
  
### <a name="add-ui-elements-to-the-add-in"></a><span data-ttu-id="b3a04-218">アドインに UI 要素を追加します。</span><span class="sxs-lookup"><span data-stu-id="b3a04-218">Add UI elements to the add-in</span></span>

<span data-ttu-id="b3a04-219">使用例を追加でいくつかのコンポーネントで構成されます。</span><span class="sxs-lookup"><span data-stu-id="b3a04-219">The example add-in consists of a few components.</span></span> <span data-ttu-id="b3a04-220">Default.aspx ファイルには、静的な要素の説明があります。</span><span class="sxs-lookup"><span data-stu-id="b3a04-220">Static element descriptions are located in the Default.aspx file.</span></span> <span data-ttu-id="b3a04-221">動的な要素の説明とすべてのコンポーネントのコードがあります。</span><span class="sxs-lookup"><span data-stu-id="b3a04-221">Dynamic element descriptions and code for all components are located in the App.js file.</span></span> <span data-ttu-id="b3a04-222">コンポーネントに関するコメントは、ソース コードの一覧を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b3a04-222">For comments regarding the components, refer to the source code listings.</span></span> <span data-ttu-id="b3a04-223">アドインの UI コンポーネントの一覧を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="b3a04-223">Here is a list of the UI components in the add-in:</span></span>
  
- <span data-ttu-id="b3a04-224">Title</span><span class="sxs-lookup"><span data-stu-id="b3a04-224">Title</span></span>
    
- <span data-ttu-id="b3a04-225">紹介文言</span><span class="sxs-lookup"><span data-stu-id="b3a04-225">Introductory verbiage</span></span>
    
- <span data-ttu-id="b3a04-226">表からタスクを削除するボタン</span><span class="sxs-lookup"><span data-stu-id="b3a04-226">Button to remove tasks from the table</span></span>
    
- <span data-ttu-id="b3a04-227">プロジェクト ID、名前、およびタスクの情報を一覧表示するテーブルです。</span><span class="sxs-lookup"><span data-stu-id="b3a04-227">Table that lists the project ID and name, and the task information.</span></span>
    
- <span data-ttu-id="b3a04-228">タスクのタスクのデータをテーブルにインポートする (プロジェクトごとに 1 回クローン作成) ボタン。</span><span class="sxs-lookup"><span data-stu-id="b3a04-228">Tasks Button (cloned once for each project) that imports task data into the table.</span></span>
    
<span data-ttu-id="b3a04-229">タイトル、プロジェクトのテーブルのヘッダー部分など、ユーザー インターフェイスの詳細は、Default.aspx のプロジェクト ファイルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b3a04-229">For details of the user interface, such as the title and the header portion of the project table, see the Default.aspx project file.</span></span>
  
### <a name="initialize-and-connect-to-the-host-system"></a><span data-ttu-id="b3a04-230">初期化し、ホスト システムへの接続</span><span class="sxs-lookup"><span data-stu-id="b3a04-230">Initialize and connect to the host system</span></span>

<span data-ttu-id="b3a04-231">App.js ファイルには、JavaScript コードが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b3a04-231">The App.js file contains the JavaScript code.</span></span> <span data-ttu-id="b3a04-232">アドインの PS.js が、ブラウザーにロードし、initializePage 関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b3a04-232">The add-in loads PS.js in the browser, and then calls the initializePage function.</span></span> <span data-ttu-id="b3a04-233">InitializePage は、オンライン プロジェクトのエンドポイントへのコンテキストを取得し、loadProjects 関数を開始します。</span><span class="sxs-lookup"><span data-stu-id="b3a04-233">InitializePage retrieves a context to the Project Online endpoint and starts the loadProjects function.</span></span>
  
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

### <a name="retrieve-the-projects"></a><span data-ttu-id="b3a04-234">プロジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="b3a04-234">Retrieve the projects</span></span>

<span data-ttu-id="b3a04-235">LoadProjects 関数は、プロジェクトの名前と Id のサービスを照会します。</span><span class="sxs-lookup"><span data-stu-id="b3a04-235">The loadProjects function queries the service for the project names and IDs.</span></span> 
  
<span data-ttu-id="b3a04-236">アプリケーションの取得、プロジェクト名とプロジェクト id。プロジェクトに関するその他の情報は、利用可能なを取得するプロパティを明示的に識別するのには load メソッドを変更することによってアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="b3a04-236">The application retrieves the project name and project Id. Other information about the project is available and can be accessed by modifying the load method to identify explicitly the properties to retrieve.</span></span> <span data-ttu-id="b3a04-237">例は、コメントとしてコード内に提供されます。</span><span class="sxs-lookup"><span data-stu-id="b3a04-237">An example is provided in the code as a comment.</span></span> 
  
<span data-ttu-id="b3a04-238">クエリが成功すると、追加で displayProjects を呼び出すことで続行されます。</span><span class="sxs-lookup"><span data-stu-id="b3a04-238">If the query succeeds, the add-in continues by calling displayProjects.</span></span> 
  
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

### <a name="display-the-projects"></a><span data-ttu-id="b3a04-239">プロジェクトを表示します。</span><span class="sxs-lookup"><span data-stu-id="b3a04-239">Display the projects</span></span>

<span data-ttu-id="b3a04-240">DisplayProjects 関数は、テーブル、プロジェクトごとに 1 行と、特定のプロジェクトのタスクを表示するボタンを作成します。</span><span class="sxs-lookup"><span data-stu-id="b3a04-240">The displayProjects function creates a table, one row per project, and a button to show the tasks for the specific project.</span></span> 
  
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
> <span data-ttu-id="b3a04-241">While は、アクセス ID および名前のプロパティをループします。</span><span class="sxs-lookup"><span data-stu-id="b3a04-241">The while loop accesses the ID and name properties.</span></span> <span data-ttu-id="b3a04-242">これは、次に、同じプロパティにアクセスする関数を呼び出すソース コード プロジェクトと少し異なります。</span><span class="sxs-lookup"><span data-stu-id="b3a04-242">This is slightly different than the source code project that calls a function that, in turn, accesses the same properties.</span></span> 
  
### <a name="display-the-tasks-for-a-project"></a><span data-ttu-id="b3a04-243">プロジェクトのタスクを表示します。</span><span class="sxs-lookup"><span data-stu-id="b3a04-243">Display the tasks for a project</span></span>

<span data-ttu-id="b3a04-244">、アドインの一部の中に、タスクは、最初の読み込みの一部ではありません。</span><span class="sxs-lookup"><span data-stu-id="b3a04-244">The tasks, while part of the add-in, are not part of the initial loading.</span></span> <span data-ttu-id="b3a04-245">ユーザーがプロジェクトに関連付けられているタスクに関心を持っていない場合は、btnLoadTasks イベント ハンドラーを使用してリストに表示するタスクと、"タスクの表示] ボタンをクリックすると。</span><span class="sxs-lookup"><span data-stu-id="b3a04-245">If the user is interested in the tasks associated with a project, clicking the "Show Tasks" button causes the tasks to display in the list using the btnLoadTasks event handler.</span></span> 
  
<span data-ttu-id="b3a04-246">BtnLoadTasks イベント ハンドラーの適切なプロジェクトの ID を持つサーバーから、指定されたプロジェクトのタスクを要求します。</span><span class="sxs-lookup"><span data-stu-id="b3a04-246">The btnLoadTasks event handler, with the appropriate project ID, requests the tasks for the specified project from the server.</span></span> <span data-ttu-id="b3a04-247">取得した後 btnLoadTasks は、画面上のタスクを表示するのには displayTasks に、[タスク] ボックスの一覧を渡します。</span><span class="sxs-lookup"><span data-stu-id="b3a04-247">Once retrieved, btnLoadTasks passes the task list to displayTasks to present the tasks onscreen.</span></span>
  
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

<span data-ttu-id="b3a04-248">DisplayTasks 関数には、プロジェクト項目のすぐ下にある指定されたプロジェクトに関連付けられているタスクが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b3a04-248">The displayTasks function displays the tasks associated with a specified project immediately beneath the project entry.</span></span>
  
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
> <span data-ttu-id="b3a04-249">While は、タスク ID にアクセスし、名前のプロパティをループします。</span><span class="sxs-lookup"><span data-stu-id="b3a04-249">The while loop accesses the task ID and name properties.</span></span> <span data-ttu-id="b3a04-250">これは、次に、同じプロパティにアクセスする関数を呼び出すソース コード プロジェクトと少し異なります。</span><span class="sxs-lookup"><span data-stu-id="b3a04-250">This is slightly different than the source code project that calls a function that, in turn, accesses the same properties.</span></span> 
  
<span data-ttu-id="b3a04-251">1 つのプロジェクトのタスクの出力の例に従います。</span><span class="sxs-lookup"><span data-stu-id="b3a04-251">Sample output for the tasks of a single project follows.</span></span>
  
<span data-ttu-id="b3a04-252">![プロジェクトのタスクの出力を示すスクリーン ショット](media/f6500a3f-000b-4f3e-9be6-9a74d0bea15e.png "プロジェクトのタスクの出力を示すスクリーン ショット")</span><span class="sxs-lookup"><span data-stu-id="b3a04-252">![Screen shot showing the output for a project task](media/f6500a3f-000b-4f3e-9be6-9a74d0bea15e.png "Screen shot showing the output for a project task")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b3a04-253">関連項目</span><span class="sxs-lookup"><span data-stu-id="b3a04-253">See also</span></span>

<span data-ttu-id="b3a04-254">ドキュメントとオンライン プロジェクトと CSOM を使用したアプリケーション開発に関連するサンプルでは、[プロジェクト開発のポータル](http://dev.office.com/project.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b3a04-254">For documentation and samples related to Project Online and application development using CSOM, see the [Project Development Portal](http://dev.office.com/project.aspx).</span></span>
    

